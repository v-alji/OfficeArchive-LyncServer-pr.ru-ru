---
title: 'Lync Server 2013: простая процедура отработки отказа для интерфейсного пула'
description: 'Lync Server 2013: процедура ABC для отработки отказа в пуле внешних интерфейсов.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Front End pool ABC failover procedure
ms:assetid: 67763ad3-6796-45eb-a486-901f21ac1a95
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945635(v=OCS.15)
ms:contentKeyID: 51541486
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b86f196d53afdc1dcad6fe41191c2aa1582f717e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399136"
---
# <a name="front-end-pool-abc-failover-procedure-in-lync-server-2013"></a><span data-ttu-id="e20f7-103">Простая процедура отработки отказа для интерфейсного пула в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e20f7-103">Front End pool ABC failover procedure in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e20f7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e20f7-104">

<span> </span></span></span>

<span data-ttu-id="e20f7-105">_**Тема последнего изменения:** 2014-05-22_</span><span class="sxs-lookup"><span data-stu-id="e20f7-105">_**Topic Last Modified:** 2014-05-22_</span></span>

<span data-ttu-id="e20f7-106">Чтобы выполнить процедуру ABC failover, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="e20f7-106">Use the following steps to perform the ABC failover procedure.</span></span> <span data-ttu-id="e20f7-107">Эта процедура включает подробное описание каждого шага, а затем команды и командлеты, которые необходимо выполнить для каждого шага.</span><span class="sxs-lookup"><span data-stu-id="e20f7-107">This procedure contains a high-level description of each step, followed by commands and cmdlets to be run for each step.</span></span>

<span data-ttu-id="e20f7-108">Чтобы запустить командлеты, откройте консоль управления Lync Server с помощью команды Запуск от имени администратора.</span><span class="sxs-lookup"><span data-stu-id="e20f7-108">To run the cmdlets, open a Lync Server Management Shell using Run as Administrator.</span></span>

<div>

## <a name="to-perform-an-abc-failover"></a><span data-ttu-id="e20f7-109">Выполнение ABC отработки отказа</span><span class="sxs-lookup"><span data-stu-id="e20f7-109">To Perform an ABC Failover</span></span>

1.  <span data-ttu-id="e20f7-110">Убедитесь, что пул A является узлом центрального сервера управления (CMS).</span><span class="sxs-lookup"><span data-stu-id="e20f7-110">Check whether the pool A is the host for the Central Management Server (CMS).</span></span>
    
      - <span data-ttu-id="e20f7-111">Выполнить следующий командлет:</span><span class="sxs-lookup"><span data-stu-id="e20f7-111">Run the following cmdlet:</span></span>
        
            Get-CsService -CentralManagement
        
        <span data-ttu-id="e20f7-112">Если поле Identity активного CMS указывает на полное доменное имя (FQDN) для пула A, вы можете сначала выполнить действия 2 и 3 для этой процедуры для основного сервера управления.</span><span class="sxs-lookup"><span data-stu-id="e20f7-112">If the Identity field of the active CMS points to the fully qualified domain name (FQDN) of Pool A, then you use steps 2 and 3 of this procedure to fail over the Central Management Server first.</span></span> <span data-ttu-id="e20f7-113">В противном случае перейдите к шагу 4.</span><span class="sxs-lookup"><span data-stu-id="e20f7-113">Otherwise, skip to step 4.</span></span>

2.  <span data-ttu-id="e20f7-114">Для переключения CMS на пул B в режиме аварийного восстановления запустите следующий командлет:</span><span class="sxs-lookup"><span data-stu-id="e20f7-114">Fail over the CMS to Pool B in disaster recovery mode by running the following cmdlet:</span></span>
    
        Invoke-CsManagementServerFailover -BackupSqlServerFqdn <Pool B BE FQDN> -BackupSqlInstanceName <Pool B BE instance name> [-BackupMirrorSqlServerFqdn <Pool B Mirror BE FQDN> -BackupMirrorSqlInstanceName <Pool B Mirror BE Instance name>] -Force -Verbose
    
    <span data-ttu-id="e20f7-115">После этого мы рекомендуем вам переместить CMS из пула B в другой существующий Объединенный пул для дополнительной устойчивости.</span><span class="sxs-lookup"><span data-stu-id="e20f7-115">After you do this, we recommend that you move the CMS from pool B to another existing paired pool for extra resiliency.</span></span> <span data-ttu-id="e20f7-116">Подробности можно найти в разделе [Move-CsManagementServer](https://docs.microsoft.com/powershell/module/skype/Move-CsManagementServer)..</span><span class="sxs-lookup"><span data-stu-id="e20f7-116">For details, see [Move-CsManagementServer](https://docs.microsoft.com/powershell/module/skype/Move-CsManagementServer)..</span></span>

3.  <span data-ttu-id="e20f7-117">Если в пуле A содержится CMS, импортируйте конфигурацию LIS из группы A в базу данных LIS (LIS. mdf) пула.</span><span class="sxs-lookup"><span data-stu-id="e20f7-117">If Pool A contains CMS, import the LIS configuration from pool A into pool B’s LIS database (Lis.mdf).</span></span> <span data-ttu-id="e20f7-118">Это действие будет работать только в том случае, если вы регулярно заархивированные данные LIS.</span><span class="sxs-lookup"><span data-stu-id="e20f7-118">This will work only if you have been backing up LIS data on a regular basis.</span></span> <span data-ttu-id="e20f7-119">Чтобы импортировать конфигурацию LIS, выполните следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="e20f7-119">To import the LIS configuration, run the following cmdlets:</span></span>
    
        Import-CsLisConfiguration -FileName <String> 
        Publish-CsLisConfiguration

4.  <span data-ttu-id="e20f7-120">Импортируйте резервные копии рабочих процессов службы группы ответа сервера Lync из пула A в пул B.</span><span class="sxs-lookup"><span data-stu-id="e20f7-120">Import backed-up Lync Server Response Group service workflows from pool A into pool B.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="e20f7-121">В настоящее время командлет <STRONG>Import-CsRgsConfiguration</STRONG> требует, чтобы имена очереди и рабочего процесса в пуле A отличаются от имен очереди и рабочего процесса в пуле B. Если имена не являются уникальными, при запуске командлета <STRONG>Import-CsRgsConfiguration</STRONG> возникает ошибка, а перед выполнением командлета <STRONG>Import-CsRgsConfiguration</STRONG> вы должны будете переименовать очереди и рабочие процессы в пуле B.</span><span class="sxs-lookup"><span data-stu-id="e20f7-121">Currently, the <STRONG>Import-CsRgsConfiguration</STRONG> cmdlet requires that the queue and workflow names on pool A are distinct from the queue and workflow names on pool B. If the names are not distinct, you will get an error when running the <STRONG>Import-CsRgsConfiguration</STRONG> cmdlet, and the queues and workflows will need to be renamed in pool B before proceeding with <STRONG>Import-CsRgsConfiguration</STRONG> cmdlet.</span></span>

    
    </div>
    
    <span data-ttu-id="e20f7-122">У вас есть два варианта импорта конфигурации группы ответа из пула A в пул B. Выбор используемого параметра зависит от того, хотите ли вы заменить параметры уровня приложения для пула B с параметрами уровня приложения в пуле A.</span><span class="sxs-lookup"><span data-stu-id="e20f7-122">You have two options for importing the Response Group configuration from pool A to pool B. Which option you use depends on whether you want to overwrite the application-level settings of pool B with the application-level settings in pool A.</span></span>
    
      - <span data-ttu-id="e20f7-123">Если вы хотите перезаписать параметры пула (B), выполните командлет **Import-CsRgsConfiguration** с параметром **ReplaceExistingSettings** :</span><span class="sxs-lookup"><span data-stu-id="e20f7-123">If you want to overwrite the Pool B settings, run the **Import-CsRgsConfiguration** cmdlet with the **ReplaceExistingSettings** option:</span></span>
        
            Import-CsRgsConfiguration -Destination "service:ApplicationServer:<Pool B FQDN>" -FileName "C:\RgsExportPrimary.zip"  -ReplaceExistingRgsSettings
    
      - <span data-ttu-id="e20f7-124">Если вы не хотите перезаписывать параметры пула (B), используйте командлет **Import-CsRgsConfiguration** без параметра **ReplaceExistingSettings** .</span><span class="sxs-lookup"><span data-stu-id="e20f7-124">If you do not want to overwrite the Pool B settings, use the **Import-CsRgsConfiguration** cmdlet without the **ReplaceExistingSettings** option.</span></span>
        
            Import-CsRgsConfiguration -Destination "service:ApplicationServer:<Pool B FQDN>" -FileName "C:\RgsExportPrimary.zip"
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="e20f7-125">Имейте в виду, что если вы не хотите перезаписывать параметры уровня приложения для пула резервных копий (пул B) с параметрами основного пула (пул A), параметры уровня приложения для пула A будут потеряны, так как в приложении группы ответа может храниться только один набор параметров уровня приложения для каждого пула.</span><span class="sxs-lookup"><span data-stu-id="e20f7-125">Keep in mind that if you do not want to overwrite the application-level settings of the backup pool (pool B) with the settings of the primary pool (pool A), pool A’s application-level settings will be lost if pool A is lost, because the Response Group application can store only one set of application-level settings per pool.</span></span> <span data-ttu-id="e20f7-126">Если группа C развернута для замены пула A, параметры на уровне приложения должны быть перенастроены, в том числе с аудиофайлом по умолчанию для хранения музыкальных файлов.</span><span class="sxs-lookup"><span data-stu-id="e20f7-126">When pool C is deployed to replace pool A, the application-level settings must be reconfigured, including the default music-on-hold audio file.</span></span>

    
    </div>

5.  <span data-ttu-id="e20f7-127">Убедитесь, что импорт конфигурации группы ответа выполнен успешно, выполнив следующие командлеты, чтобы отобразить импортированные группы ответа.</span><span class="sxs-lookup"><span data-stu-id="e20f7-127">Verify that the Response Group configuration import was successful by running the following cmdlets to display the imported response groups.</span></span> <span data-ttu-id="e20f7-128">Обратите внимание на то, что импортированные группы ответов по-прежнему принадлежат группе A.</span><span class="sxs-lookup"><span data-stu-id="e20f7-128">Note that the imported response groups are still owned by pool A.</span></span>
    
        Get-CsRgsWorkflow -Identity "service:ApplicationServer:<Pool B FQDN>" -Owner "service:ApplicationServer:<Pool A FQDN>"
        
        Get-CsRgsQueue -Identity "service:ApplicationServer:<Pool B FQDN>" -Owner "service:ApplicationServer:<Pool A FQDN>"
        
        Get-CsRgsAgentGroup -Identity "service:ApplicationServer:<Pool B FQDN>" -Owner "service:ApplicationServer:<Pool A FQDN>"

6.  <span data-ttu-id="e20f7-129">Для неназначенных номеров переместите неназначенные диапазоны номеров, которые используют "извещение", в качестве выбранной службы объявлений из пула A в пул B. Для этого выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="e20f7-129">For Unassigned Numbers, move the Unassigned Number ranges that are using "Announcement" as the selected announcement service from pool A to pool B. To do so:</span></span>
    
      - <span data-ttu-id="e20f7-130">Повторное создание всех объявлений, развернутых в пуле A, в пуле B. Если при развертывании объявлений в пуле A использовались какие-либо звуковые файлы, эти файлы понадобятся вам для повторного создания объявлений в пуле B. Для повторного создания объявлений в пуле B используйте командлеты **New-CsAnnouncement** с пулом b в качестве родительской службы.</span><span class="sxs-lookup"><span data-stu-id="e20f7-130">Re-create all announcements that were deployed in pool A on pool B. If any audio files were used when deploying the announcements in pool A, these files will be needed to re-create the announcements in pool B. To re-create the announcements in pool B, use the **New-CsAnnouncement** cmdlets, with pool B as the Parent service.</span></span>
    
      - <span data-ttu-id="e20f7-131">Переназначьте все диапазоны неназначенных номеров, предназначенные для объявления в пуле A, в новые развернутые объявления в пуле B. выполните следующий командлет для каждого неназначенного диапазона номеров, предназначенного для объявления пула а.</span><span class="sxs-lookup"><span data-stu-id="e20f7-131">Retarget all the Unassigned Number ranges that are targeting an announcement in pool A to the newly deployed announcements in pool B. Run the following cmdlet for every Unassigned Number range targeting an announcement of pool A:</span></span>
        
            Set-CsUnassignedNumber -Identity "<Range Name>" -AnnouncementService "<Pool B FQDN>" -AnnouncementName "<New Announcement in pool B>"
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="e20f7-132">Этот шаг не требуется для неназначенных диапазонов номеров, в которых в качестве выбранной службы объявлений используется "Exchange UM".</span><span class="sxs-lookup"><span data-stu-id="e20f7-132">This step is not required for unassigned number ranges that use "Exchange UM" as the selected announcement service.</span></span>

    
    </div>

7.  <span data-ttu-id="e20f7-133">Переключиться из пула A в пул B в режиме аварийного восстановления (DR), выполнив следующий командлет:</span><span class="sxs-lookup"><span data-stu-id="e20f7-133">Fail over Pool A to Pool B in Disaster Recovery (DR) mode, by running the following cmdlet:</span></span>
    
        Invoke-CsPoolFailover -PoolFqdn <Pool A FQDN> -DisasterMode

8.  <span data-ttu-id="e20f7-134">Создание пула в пуле C, но не запуск служб в пуле C.</span><span class="sxs-lookup"><span data-stu-id="e20f7-134">Build pool C, but do not start any services on pool C.</span></span>
    
    <span data-ttu-id="e20f7-135">Обратите внимание на то, что это действие можно выполнить одновременно с действиями 5 и 6.</span><span class="sxs-lookup"><span data-stu-id="e20f7-135">Note that this step can be carried out concurrently with steps 5 and 6.</span></span>

9.  <span data-ttu-id="e20f7-136">Принудительное перемещение пользователей из пула а в группу C, выполнив следующий командлет:</span><span class="sxs-lookup"><span data-stu-id="e20f7-136">Force users homed on pool A to move to pool C by running the following cmdlet:</span></span>
    
        Get-csuser -Filter {RegistrarPool -eq "<Pool A FQDN>"} | Move-CsUser -Target <Pool C FQDN> -Force
    
    <span data-ttu-id="e20f7-137">На этом этапе пользователи, работающие в пуле "A", начнут испытывать сбой в работе службы.</span><span class="sxs-lookup"><span data-stu-id="e20f7-137">At this point, users homed on pool A will begin to experience a service outage.</span></span> <span data-ttu-id="e20f7-138">Этот сбой будет продолжен до этапа 16, после чего службы будут запущены в пуле C.</span><span class="sxs-lookup"><span data-stu-id="e20f7-138">This outage will continue until step 16, at which point services are started on pool C.</span></span>

10. <span data-ttu-id="e20f7-139">Сделайте Каталог конференций пула а для перемещения на группу C, выполнив следующий командлет:</span><span class="sxs-lookup"><span data-stu-id="e20f7-139">Force the conference directory of pool A to move to pool C by running the following cmdlet:</span></span>
    
        Move-CsConferenceDirectory -Identity <Conference Directory ID of Pool A> -TargetPool <Pool C FQDN> -Force

11. <span data-ttu-id="e20f7-140">Запросите объект контакта автосекретаря конференции (CAA) для перемещения из пула A в пул C, выполнив следующий командлет:</span><span class="sxs-lookup"><span data-stu-id="e20f7-140">Force the Conference Auto Attendant (CAA) Contact Object to move from pool A to pool C by running the following cmdlet:</span></span>
    
        Move-csApplicationEndpoint -Identity "<Pool A CAA Uri>" -targetApplicationPool <Pool C FQDN> -force

12. <span data-ttu-id="e20f7-141">Копирование содержимого конференции из пула B в пул C.</span><span class="sxs-lookup"><span data-stu-id="e20f7-141">Copy conference content from pool B to pool C.</span></span>

13. <span data-ttu-id="e20f7-142">Экспортируйте пользовательские данные из пула B и импортируйте данные пользователя в пул C, выполнив следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="e20f7-142">Export user data from pool B and import the user data into pool C by running the following cmdlets:</span></span>
    
        Export-CsUserData -PoolFqdn <Pool B Fqdn> -FileName <String>
        Import-CsUserData -PoolFqdn <Pool C Fqdn> -FileName <String>

14. <span data-ttu-id="e20f7-143">Восстановление резервных копий данных приложения из пула A в пул C и назначение диапазонов на орбиту на вкладке "а" в пул C.</span><span class="sxs-lookup"><span data-stu-id="e20f7-143">Restore backed-up Call Park application data from pool A into pool C and assign the Call Park orbit ranges of pool A to pool C.</span></span>
    
      - <span data-ttu-id="e20f7-144">Вы можете переназначить диапазон орбиты для группы A в пул C на панели управления Lync Server или в командной консоли Lync Server Management.</span><span class="sxs-lookup"><span data-stu-id="e20f7-144">You can reassign a Call Park orbit range of pool A to pool C either through the Lync Server Control Panel or the Lync Server Management Shell.</span></span> <span data-ttu-id="e20f7-145">Для командной консоли Lync Server выполните следующий командлет для каждого диапазона орбит на приостановку звонков, назначенного пулу A (Обратите внимание, что параметр Identity указывает на диапазоны орбиты на приостановку звонков, которые входят в пул A).</span><span class="sxs-lookup"><span data-stu-id="e20f7-145">For the Lync Server Management Shell, run the following cmdlet for every Call Park orbit range assigned to pool A (note that the Identity parameter refers to the Call Park Orbit Ranges that belong to pool A):</span></span>
        
            Set-CsCallParkOrbit -Identity "<Call Park Orbit Identity>" -CallParkService "service:ApplicationServer:<Pool C FQDN>"
    
      - <span data-ttu-id="e20f7-146">Если настроенная музыка заблокирована для приостановки звонков в пуле A, восстановите в группе C файл, настроенный для парковки звонков.</span><span class="sxs-lookup"><span data-stu-id="e20f7-146">If a customized music-on-hold has been configured for Call Park in pool A, restore the Call Park customized music-on-hold file in pool C.</span></span>
        
            Xcopy <Source> <Destination: Pool C CPS File Store Path>
        
        <span data-ttu-id="e20f7-147">Например:</span><span class="sxs-lookup"><span data-stu-id="e20f7-147">For example:</span></span>
        
            Xcopy "Source Path" "<Pool C File Store Path>\OcsFileStore\coX-ApplicationServer-X\AppServerFiles\CPS\"
    
      - <span data-ttu-id="e20f7-148">Наконец, настройте параметры парковки для пула C с помощью командлета **Set-CsCpsConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="e20f7-148">Finally, reconfigure the Call Park settings on pool C by using the **Set-CsCpsConfiguration** cmdlet.</span></span> <span data-ttu-id="e20f7-149">Приложение для парковки звонков может хранить только один набор параметров и один настроенный звуковой файл на хранение музыки для каждого пула, и эти параметры не будут заархивированы или сохранены в случае аварии.</span><span class="sxs-lookup"><span data-stu-id="e20f7-149">The Call Park application can store only one set of settings and one customized music-on-hold audio file per pool, and these settings are not backed up or preserved in the event of a disaster.</span></span>

15. <span data-ttu-id="e20f7-150">Если в качестве следующего пула переходов для сохраняемого чата указана группа A, настройте и опубликуйте изменения топологии, чтобы сервер следующего прыжка указывал на пул C.</span><span class="sxs-lookup"><span data-stu-id="e20f7-150">If the next hop pool for Persistent Chat is pointing to pool A, make and publish topology changes so that the next hop server points to pool C.</span></span>
    
      - <span data-ttu-id="e20f7-151">В построителе топологии измените пул сохраняемого чата таким образом, чтобы он указывал на пул C в качестве следующего прыжка.</span><span class="sxs-lookup"><span data-stu-id="e20f7-151">In Topology Builder, change the Persistent Chat pool to point to Pool C as its next hop.</span></span> <span data-ttu-id="e20f7-152">Для этого щелкните правой кнопкой мыши группу постоянного чата, а затем откройте вкладку **Общие** и введите имя пула C в **следующей версии пула прыжков**.</span><span class="sxs-lookup"><span data-stu-id="e20f7-152">To do so, right-click on the Persistent Chat pool, then click the **General** tab, and then type the name of Pool C in **Next Hop Pool**.</span></span>
    
      - <span data-ttu-id="e20f7-153">Запустите службу на пуле C, выполнив следующий командлет:</span><span class="sxs-lookup"><span data-stu-id="e20f7-153">Start services on pool C by running the following cmdlet:</span></span>
        
            Start-csWindowsService
    
    <span data-ttu-id="e20f7-154">На этом этапе служба завершает работу для пользователей, первоначально размещенных в пуле A.</span><span class="sxs-lookup"><span data-stu-id="e20f7-154">At this point, the service outage ends for users originally homed on pool A.</span></span>

16. <span data-ttu-id="e20f7-155">Экспортируйте рабочие процессы службы ответов сервера Lync Server из пула B, владельца которого является группа A, для импорта в пул C, выполнив следующий командлет:</span><span class="sxs-lookup"><span data-stu-id="e20f7-155">Export Lync Server Response Group service workflows from pool B owned by pool A for import into pool C by running the following cmdlet:</span></span>
    
        Export-CsRgsConfiguration -Source "service:ApplicationServer:<Pool B FQDN>" -Owner "service:ApplicationServer:<Pool A FQDN>" -FileName "C:\RgsExportPrimaryUpdated.zip" 

17. <span data-ttu-id="e20f7-156">Импорт рабочих процессов службы групп ответов Lync Server в пул C из пула B.</span><span class="sxs-lookup"><span data-stu-id="e20f7-156">Import Lync Server Response Group service workflows into pool C from pool B.</span></span>
    
    <span data-ttu-id="e20f7-157">Существует два варианта импорта конфигурации группы ответа из группы B в группу C. Выбор используемого параметра зависит от того, хотите ли вы заменить параметры уровня приложения для пула C с параметрами уровня приложения в пуле B.</span><span class="sxs-lookup"><span data-stu-id="e20f7-157">You have two options are for importing the Response Group configuration from pool B to pool C. Which option you use depends on whether you want to overwrite the application-level settings of pool C with the application-level settings in pool B.</span></span>
    
      - <span data-ttu-id="e20f7-158">Если вы хотите перезаписать параметры пула C, выполните командлет **Import-CsRgsConfiguration** с параметром **ReplaceExistingSettings** :</span><span class="sxs-lookup"><span data-stu-id="e20f7-158">If you want to overwrite the Pool C settings, run the **Import-CsRgsConfiguration** cmdlet with the **ReplaceExistingSettings** option:</span></span>
        
            Import-CsRgsConfiguration -Destination "service:ApplicationServer:<Pool C FQDN>" -FileName "C:\RgsExportPrimary.zip"  -ReplaceExistingRgsSettings
    
      - <span data-ttu-id="e20f7-159">Если вы не хотите перезаписывать параметры пула в, используйте командлет **Import-CsRgsConfiguration** без параметра **ReplaceExistingSettings** .</span><span class="sxs-lookup"><span data-stu-id="e20f7-159">If you do not want to overwrite the Pool C settings, use the **Import-CsRgsConfiguration** cmdlet without the **ReplaceExistingSettings** option.</span></span>
        
            Import-CsRgsConfiguration -Destination "service:ApplicationServer:<Pool B FQDN>" -FileName "C:\RgsExportPrimary.zip"
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="e20f7-160">Имейте в виду, что если вы не хотите перезаписывать параметры уровня приложения для пула C с параметрами пула резервного копирования (пула B), параметры уровня приложения пула B будут потеряны, так как приложение группы ответа может хранить только один набор параметров уровня приложения для каждого пула.</span><span class="sxs-lookup"><span data-stu-id="e20f7-160">Keep in mind that if you do not want to overwrite the application-level settings of Pool C with the settings of the backup pool (pool B), pool B’s application-level settings will be lost because the Response Group application can store only one set of application-level settings per pool.</span></span>

    
    </div>

18. <span data-ttu-id="e20f7-161">Убедитесь, что импорт конфигурации группы ответа прошел успешно, выполнив следующие командлеты для отображения групп ответов, которые были импортированы в пул C.</span><span class="sxs-lookup"><span data-stu-id="e20f7-161">Verify that the Response Group configuration import was successful by running the following cmdlets to display the response groups that have been imported to Pool C.</span></span>
    
        Get-CsRgsWorkflow -Identity "service:ApplicationServer:<Pool C FQDN>" -ShowAll
         Get-CsRgsQueue -Identity "service:ApplicationServer:<Pool C FQDN>" -ShowAll
        Get-CsRgsAgentGroup -Identity "service:ApplicationServer:<Pool C FQDN>" -ShowAll

19. <span data-ttu-id="e20f7-162">После проверки импортированной конфигурации в пуле C удалите группы ответа, принадлежащие основным пулам из пула B. Это сократит время простоя групп ответов.</span><span class="sxs-lookup"><span data-stu-id="e20f7-162">When the imported configuration has been verified in pool C, remove the response groups owned by the primary pool from pool B. This will minimize the downtime of the response groups.</span></span>
    
    <span data-ttu-id="e20f7-163">На этом этапе создается новый файл с экспортированной конфигурацией, а затем этот файл удаляется из пула B.</span><span class="sxs-lookup"><span data-stu-id="e20f7-163">This step creates a new file with the exported configuration, and then removes the file from pool B.</span></span>
    
        Export-CsRgsConfiguration -Source "service:ApplicationServer:<Pool B FQDN>" -Owner "service:ApplicationServer:<Pool A FQDN>" -FileName "C:\RgsExportPrimaryUpdated.zip" -RemoveExportedConfiguration

20. <span data-ttu-id="e20f7-164">Переместить в пул C: неназначенные диапазоны номеров, перенесенных из пула A в пул B.</span><span class="sxs-lookup"><span data-stu-id="e20f7-164">Move to pool C the Unassigned Number ranges that were moved from pool A to pool B.</span></span>
    
      - <span data-ttu-id="e20f7-165">Повторное создание в пуле из всех объявлений, которые были повторно созданы из пула A в пуле B. Если при развертывании извещений использовались какие-либо звуковые файлы, для повторного создания объявлений в пуле C необходимо использовать эти файлы. Для повторного создания объявлений в пуле C используйте командлеты **New-CsAnnouncement** с пулом C в качестве родительской службы.</span><span class="sxs-lookup"><span data-stu-id="e20f7-165">Re-create in pool C all announcements that were re-created from pool A in pool B. If any audio files were used when deploying the announcements to be moved, you will need to use these files to re-create the announcements in pool C. To re-create the announcements in pool C, use the **New-CsAnnouncement** cmdlets, with pool C as the Parent service.</span></span>
    
      - <span data-ttu-id="e20f7-166">Переназначение в пул C все неназначенные диапазоны номеров, перенацеленные из пула A в пул B. выполните следующий командлет для всех неназначенных диапазонов номеров, которые необходимо переадресовать:</span><span class="sxs-lookup"><span data-stu-id="e20f7-166">Retarget to pool C all the unassigned number ranges that were retargeted from pool A to pool B. Run the following cmdlet for every Unassigned Number range that needs to be retargeted:</span></span>
        
            Set-CsUnassignedNumber -Identity "<Range Name>" -AnnouncementService "<Pool C FQDN>" -AnnouncementName "<New Announcement in pool C>"
    
      - <span data-ttu-id="e20f7-167">Необязательно Удалите из пула B объявления, которые были повторно созданы в пуле C, если они больше не используются в пуле B. Для удаления объявлений используйте командлет **Remove-CsAnnouncement** .</span><span class="sxs-lookup"><span data-stu-id="e20f7-167">(Optional) Remove from pool B the announcements that were re-created in pool C if they are no longer in use in pool B. To remove announcements, use the **Remove-CsAnnouncement** cmdlet.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="e20f7-168">Этот шаг не требуется для неназначенных диапазонов номеров, в которых служба извещения использует сообщение "Exchange UM".</span><span class="sxs-lookup"><span data-stu-id="e20f7-168">This step is not required for unassigned number ranges that use "Exchange UM" as the announcement service.</span></span>

        
        </div>

21. <span data-ttu-id="e20f7-169">Очистите данные пользователя пула A в пуле B, выполнив следующий командлет:</span><span class="sxs-lookup"><span data-stu-id="e20f7-169">Clean up user data of pool A in pool B by running the following cmdlet:</span></span>
    
        Remove-CsUserStoreBackupData -PoolFqdn <Pool B FQDN> -Verbose

22. <span data-ttu-id="e20f7-170">В построителе топологии выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="e20f7-170">Do the following in Topology Builder:</span></span>
    
      - <span data-ttu-id="e20f7-171">Отмена связывания пула A и пула B. Свяжите пул B и пул C. Затем удалите пул A из топологии и опубликуйте его.</span><span class="sxs-lookup"><span data-stu-id="e20f7-171">Unpair pool A and pool B. Pair pool B and pool C. Then remove Pool A from the topology and publish it.</span></span> <span data-ttu-id="e20f7-172">Для этого:</span><span class="sxs-lookup"><span data-stu-id="e20f7-172">To do so:</span></span>
        
          - <span data-ttu-id="e20f7-173">В построителе топологии щелкните пул B правой кнопкой мыши и выберите команду **изменить свойства**.</span><span class="sxs-lookup"><span data-stu-id="e20f7-173">In Topology Builder, right-click on Pool B, and then click **Edit Properties**.</span></span>
        
          - <span data-ttu-id="e20f7-174">На левой панели выберите пункт **устойчивость** .</span><span class="sxs-lookup"><span data-stu-id="e20f7-174">Click **Resiliency** in the left pane.</span></span>
        
          - <span data-ttu-id="e20f7-175">В поле под **сопоставленным пулом резервных копий** выберите Pool C. Обратите внимание на то, что в поле выбора связанного пула резервных копий первоначально отображается пул A, так как пул B уже был связан с этим пулом.</span><span class="sxs-lookup"><span data-stu-id="e20f7-175">In the box below **Associated Backup Pool**, select Pool C. Note that the Associated Backup Pool selection box will initially display pool A, because pool B was previously associated with this pool.</span></span>
        
          - <span data-ttu-id="e20f7-176">Выберите **Автоматическая обработка отказов и восстановление после отказа для голосовой связи** и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="e20f7-176">Select **Automatic failover and failback for Voice**, and then click **OK**.</span></span>
            
            <span data-ttu-id="e20f7-177">Теперь при просмотре сведений о данном пуле связанный с ним пул отображается на правой панели в области **Устойчивость**. </span><span class="sxs-lookup"><span data-stu-id="e20f7-177">When you view the details about this pool, the associated pool now appears in the right pane under **Resiliency**.</span></span>
        
          - <span data-ttu-id="e20f7-178">В дереве консоли щелкните правой кнопкой мыши группу и выберите команду Удалить.</span><span class="sxs-lookup"><span data-stu-id="e20f7-178">In the console tree, right-click pool A, and then click Delete.</span></span>
        
          - <span data-ttu-id="e20f7-179">Опубликуйте топологию.</span><span class="sxs-lookup"><span data-stu-id="e20f7-179">Publish the topology.</span></span>

23. <span data-ttu-id="e20f7-180">Запустите приложение начальной загрузки в пуле C, чтобы установить приложение службы резервного копирования, а затем запустите приложение службы резервного копирования, выполнив следующие действия из папки развертывание на локальном компьютере в пуле C:</span><span class="sxs-lookup"><span data-stu-id="e20f7-180">Run the bootstrapping application on pool C to install the backup service application, and then start the backup service application by running the following from the deployment folder on a local machine in pool C:</span></span>
    
        Run "%SYSTEMROOT%\Program Files\Microsoft Lync Server 2013\Deployment\Bootstrapper.exe"
        Start-CsWindowsService -name LyncBackup

24. <span data-ttu-id="e20f7-181">Перезапустите приложение службы резервного копирования в пуле B, выполнив следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="e20f7-181">Restart the backup service application on pool B by running the following cmdlets:</span></span>
    
        Stop-CsWindowsService -name LyncBackup
        Start-CsWindowsService -name LyncBackup

25. <span data-ttu-id="e20f7-182">Если в качестве пула пулов C используется стандартный выпуск (SE) и в пуле B есть сервер CMS, установите базу данных CMS вручную для пула C, выполнив следующий командлет:</span><span class="sxs-lookup"><span data-stu-id="e20f7-182">If pool C is a Standard Edition (SE) Pool and pool B has CMS, install the CMS database manually on pool C by running the following cmdlet:</span></span>
    
        Install-CsDatabase -CentralManagementDatabase -SqlServerFqdn <Pool C FQDN> -SqlInstanceName rtc

26. <span data-ttu-id="e20f7-183">Вызовите службу резервного копирования для синхронизации старых данных конференций из пула B с пулом C, созданным до объединения B и C, и для синхронизации нового содержимого конференций из пула C с группой B, созданной после того, как вы собрались с помощью групп C и before.</span><span class="sxs-lookup"><span data-stu-id="e20f7-183">Invoke the backup service to sync old conferencing content from pool B to pool C that was generated before pairing B and C together, and to sync new conferencing content from pool C to pool B that was generated after starting pool C and before B and C were paired together.</span></span> <span data-ttu-id="e20f7-184">Для этого выполните следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="e20f7-184">To do so, run the following cmdlets:</span></span>
    
        Invoke-CsBackupServiceSync -PoolFqdn <Pool C FQDN>
        Invoke-CsBackupServiceSync -PoolFqdn <Pool B FQDN>

27. <span data-ttu-id="e20f7-185">Для каждого устройства с бесперебойной подразделением X, связанного с пулом A:</span><span class="sxs-lookup"><span data-stu-id="e20f7-185">For each Survivable Branch Appliance X associated with pool A:</span></span>
    
      - <span data-ttu-id="e20f7-186">Завершите работу SBA X, выполнив следующий командлет:</span><span class="sxs-lookup"><span data-stu-id="e20f7-186">Shut down SBA X by running the following cmdlet:</span></span>
        
            Stop-CsWindowsService
    
      - <span data-ttu-id="e20f7-187">Создание файла, содержащего список пользователей, размещенных на SBA X. Этот список будет нужен, когда пользователи будут перенесены в SBA X на этапе 30.</span><span class="sxs-lookup"><span data-stu-id="e20f7-187">Create a file that contains a list of users homed on SBA X. The list will be needed when the users are moved back to SBA X in step 30.</span></span> <span data-ttu-id="e20f7-188">Для этого выполните следующий командлет:</span><span class="sxs-lookup"><span data-stu-id="e20f7-188">To do so, run the following cmdlet:</span></span>
        
            Get-CsUser -Filter {RegistrarPool -eq "<SBA X FQDN>"} | Export-Csv d:\sbaxusers.txt
    
      - <span data-ttu-id="e20f7-189">Принудительный переход пользователей на SBA X на пул C, выполнив следующий командлет:</span><span class="sxs-lookup"><span data-stu-id="e20f7-189">Force users homed on SBA X to move to pool C by running the following cmdlet:</span></span>
        
            Get-CsUser -Filter {RegistrarPool -eq "<SBA X FQDN>"} | Move-CsUser -Target <Pool C FQDN> -Force -Verbose
    
      - <span data-ttu-id="e20f7-190">Обновите данные этих пользователей, предварительно выполнив следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="e20f7-190">Update the data of these users by first running the following cmdlets:</span></span>
        
            Convert-csUserData -InputFile <Data file exported from PoolB> -OutputFile c:\Logs\ExportedUserData.xml -TargetVersionLync2010 
            $a=get-csuser -Filter {RegistrarPool -eq "FQDN of SBA X"} | select SipAddress
            foreach($x in $a) {$x.SipAddress.Substring(4) >> users.txt}
        
        <span data-ttu-id="e20f7-191">А затем выполните следующий сценарий:</span><span class="sxs-lookup"><span data-stu-id="e20f7-191">And then run this script:</span></span>
        
            $users=gc c:\logs\users.txt
            foreach ($user in $users)
            {
            Update-CsUserData -FileName c:\logs\exportedUserDAta.xml -UserFilter $user - 
            }
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="e20f7-192">Для пользователей, использующих SBAs, которые связаны с пулом A до тех пор, пока эти пользователи не будут перемещены в пул C, произойдет сбой службы.</span><span class="sxs-lookup"><span data-stu-id="e20f7-192">A service outage will occur for users who are homed on SBAs that are associated with pool A until these users are moved to pool C.</span></span>

        
        </div>

28. <span data-ttu-id="e20f7-193">В построителе топологии для каждого SBA X, ранее связанного с пулом A, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="e20f7-193">In Topology Builder, for each SBA X previously associated with Pool A, do the following:</span></span>
    
      - <span data-ttu-id="e20f7-194">Измените связь на пул C. Для этого щелкните сайт филиала, разверните узел, который можно использовать, и выберите пункт бесперебойно работающее **устройство филиала**.</span><span class="sxs-lookup"><span data-stu-id="e20f7-194">Change the association to Pool C. To do so, click the branch site, expand the Survivable Branch Appliances or Servers node, and click **Survivable Branch Appliance**.</span></span> <span data-ttu-id="e20f7-195">Затем выберите **пул переднего плана, пул служб пользователя** , который будет подключаться к этому работающему устройству филиала в качестве пула, и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="e20f7-195">Then select the **Front End pool, User Services Pool** that this Survivable Branch Appliance will connect to as Pool C, and then click **Next**.</span></span>
    
      - <span data-ttu-id="e20f7-196">Опубликуйте топологию.</span><span class="sxs-lookup"><span data-stu-id="e20f7-196">Publish the topology.</span></span> <span data-ttu-id="e20f7-197">Для этого в дереве консоли щелкните правой кнопкой мыши новое работающее **устройство филиала**, выберите пункт **топология** и нажмите кнопку **опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="e20f7-197">To do so, in the console tree, right-click the new **Survivable Branch Appliance**, click **Topology**, and then click **Publish**.</span></span>

29. <span data-ttu-id="e20f7-198">Для каждого SBA X теперь сопоставлены с пулом C:</span><span class="sxs-lookup"><span data-stu-id="e20f7-198">For each SBA X now associated with pool C:</span></span>
    
      - <span data-ttu-id="e20f7-199">Запустите SBA X, выполнив следующий командлет на устройстве для бесперебойной работы филиалов:</span><span class="sxs-lookup"><span data-stu-id="e20f7-199">Start SBA X by running the following cmdlet on the survivable branch appliance:</span></span>
        
            Start-CsWindowsService
    
      - <span data-ttu-id="e20f7-200">Перемещайте пользователей, которые изначально разработали на SBA X из пула C в SBA X, выполнив следующий командлет.</span><span class="sxs-lookup"><span data-stu-id="e20f7-200">Move users who were originally homed on SBA X from pool C to SBA X by running the following cmdlet.</span></span>
        
            Import-Csv d:\sbaxusers.txt | Move-CsUser -Target <SBA X FQDN> -Force

<span data-ttu-id="e20f7-201"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e20f7-201"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

