---
title: 'Lync Server 2013: восстановление сервера, на котором размещается хранилище Центрального управления'
description: 'Lync Server 2013: восстановление сервера, на котором размещается хранилище Центрального управления.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Restoring the server hosting the Central Management store
ms:assetid: 3bd6c82c-07fb-4798-b8f9-e7c78a5a83d5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202172(v=OCS.15)
ms:contentKeyID: 51541464
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c0c07e4c6722695b2bfb4cb478a1f3eefa86b4eb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442518"
---
# <a name="restoring-the-server-hosting-the-central-management-store-in-lync-server-2013"></a><span data-ttu-id="79695-103">Восстановление сервера, на котором размещается центральное хранилище для управления в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="79695-103">Restoring the server hosting the Central Management store in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="79695-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="79695-104">

<span> </span></span></span>

<span data-ttu-id="79695-105">_**Тема последнего изменения:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="79695-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="79695-106">В развертывании Lync Server есть единое центральное хранилище, копия которого реплицируется на каждый сервер, на котором запущена роль сервера Lync Server.</span><span class="sxs-lookup"><span data-stu-id="79695-106">A Lync Server deployment has a single Central Management store, a copy of which is replicated to each server running a Lync Server server role.</span></span> <span data-ttu-id="79695-107">В этой статье описано, как восстановить сервер или сервер Standard Edition, на котором размещается хранилище Центрального управления.</span><span class="sxs-lookup"><span data-stu-id="79695-107">This topic describes how to restore a Back End Server or Standard Edition server that hosts the Central Management store.</span></span>

<span data-ttu-id="79695-108">Чтобы найти пул, в котором расположен центральный сервер управления, откройте конфигуратор топологии, выберите пункт **Lync Server** и просмотрите область справа на **центральном сервере управления**.</span><span class="sxs-lookup"><span data-stu-id="79695-108">To find the pool where the Central Management Server is located, open Topology Builder, click **Lync Server**, and look in the right pane under **Central Management Server**.</span></span>

<span data-ttu-id="79695-109">Если сервер, на котором размещено центральное хранилище, находится в зеркальной установке, а зеркальная база данных по-прежнему работает, мы рекомендуем сделать резервную копию этого зеркального отражения, а затем выполнить полное восстановление как в базе данных-источнике, так и в зеркальной базе данных с помощью этой резервной копии, следуя приведенной ниже процедуре восстановления.</span><span class="sxs-lookup"><span data-stu-id="79695-109">If the Back End Server that hosts the Central Management store is in a mirrored setup and the mirror database is still functional, we recommend that you make a backup of this still-functioning mirror, and then perform a full restore on both the primary database and the mirror database, using this backup, by following the restoration procedure below.</span></span> <span data-ttu-id="79695-110">Это необходимо, так как для обратного восстановления требуется изменить и опубликовать топологию, и это можно сделать только в том случае, если сервер CMS размещен на базе данных-источнике.</span><span class="sxs-lookup"><span data-stu-id="79695-110">This is necessary because Back End restore requires modifying and publishing the topology, and this can be done only if the primary database hosting CMS is operational.</span></span> <span data-ttu-id="79695-111">Также обратите внимание на то, что роли основной и зеркальной баз данных невозможно изменить, если топология не может быть опубликована.</span><span class="sxs-lookup"><span data-stu-id="79695-111">Also note that the primary and mirror database roles cannot be interchanged if the topology cannot be published.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="79695-112">Если сервер или сервер Standard Edition, на котором не размещено центральное хранилище управления, не удалось найти, ознакомьтесь со сведениями о <A href="lync-server-2013-restoring-an-enterprise-edition-back-end-server.md">восстановлении сервера выпуска Enterprise Edition в Lync server 2013</A> или <A href="lync-server-2013-restoring-a-standard-edition-server.md">восстановлении стандартного сервера выпуска в Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="79695-112">If a Back End Server or Standard Edition server that does not host the Central Management store failed, see <A href="lync-server-2013-restoring-an-enterprise-edition-back-end-server.md">Restoring an Enterprise Edition Back End Server in Lync Server 2013</A> or <A href="lync-server-2013-restoring-a-standard-edition-server.md">Restoring a Standard Edition server in Lync Server 2013</A>.</span></span> <span data-ttu-id="79695-113">Если сервер, на котором размещен Центральный центр управления, находится в зеркальной конфигурации, а зеркальный сервер не прошел, ознакомьтесь со сведениями о <A href="lync-server-2013-restoring-a-mirrored-enterprise-edition-back-end-server-mirror.md">восстановлении зеркального сервера выпуска Enterprise Edition в Lync server 2013 — Mirror</A>.</span><span class="sxs-lookup"><span data-stu-id="79695-113">If a Back End Server that hosts the Central Management store is in a mirrored configuration and only the mirror failed, see <A href="lync-server-2013-restoring-a-mirrored-enterprise-edition-back-end-server-mirror.md">Restoring a mirrored Enterprise Edition Back End Server in Lync Server 2013 - mirror</A>.</span></span> <span data-ttu-id="79695-114">В случае сбоя любого другого сервера ознакомьтесь со сведениями о <A href="lync-server-2013-restoring-an-enterprise-edition-member-server.md">восстановлении рядового сервера выпуска Enterprise Edition в Lync server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="79695-114">If any other server failed, see <A href="lync-server-2013-restoring-an-enterprise-edition-member-server.md">Restoring an Enterprise Edition member server in Lync Server 2013</A>.</span></span>



</div>

<div>


> [!TIP]  
> <span data-ttu-id="79695-115">Прежде чем начать восстановление, мы рекомендуем использовать копию системы с изображением.</span><span class="sxs-lookup"><span data-stu-id="79695-115">We recommend that you take an image copy of the system before you start restoration.</span></span> <span data-ttu-id="79695-116">Вы можете использовать это изображение как точку отката, если что-то пойдет не так во время восстановления.</span><span class="sxs-lookup"><span data-stu-id="79695-116">You can use this image as a rollback point, in case something goes wrong during restoration.</span></span> <span data-ttu-id="79695-117">После установки операционной системы и сервера SQL Server вы можете использовать копию изображения, а также восстановить или подать заявку на сертификаты.</span><span class="sxs-lookup"><span data-stu-id="79695-117">You might want to take the image copy after you install the operating system and SQL Server, and restore or reenroll the certificates.</span></span>



</div>

<div>

## <a name="to-restore-the-central-management-store"></a><span data-ttu-id="79695-118">Восстановление хранилища центрального управления</span><span class="sxs-lookup"><span data-stu-id="79695-118">To restore the Central Management store</span></span>

1.  <span data-ttu-id="79695-119">Начните с чистого или нового сервера с таким же полным доменным именем (FQDN), как и у компьютера, на котором произошел сбой, установите операционную систему, а затем восстановите или порегистрируйте сертификаты.</span><span class="sxs-lookup"><span data-stu-id="79695-119">Start with a clean or new server that has the same fully qualified domain name (FQDN) as the failed computer, install the operating system, and then restore or reenroll the certificates.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="79695-120">Следуйте инструкциям по развертыванию сервера в своей организации, чтобы выполнить этот шаг.</span><span class="sxs-lookup"><span data-stu-id="79695-120">Follow your organization's server deployment procedures to perform this step.</span></span>

    
    </div>

2.  <span data-ttu-id="79695-121">Войдите в свою учетную запись пользователя, которая входит в группу RTCUniversalServerAdmins и локальную группу администраторов, войдя на сервер, который вы хотите восстановить.</span><span class="sxs-lookup"><span data-stu-id="79695-121">From a user account that is a member of the RTCUniversalServerAdmins group and the Local Administrators group, log on to the server that you are restoring.</span></span>

3.  <span data-ttu-id="79695-122">Если вы восстанавливаете Стандартный сервер выпуска, восстановите хранилище файлов, скопировав соответствующее хранилище файлов из $Backup в расположение хранилища файлов на сервере, а затем предоставьте доступ к папке.</span><span class="sxs-lookup"><span data-stu-id="79695-122">If you are restoring a Standard Edition server, restore the File Store by copying the appropriate File Store from $Backup to the File Store location on the server, and then share the folder.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="79695-123">Путь и имя файла для восстановленного хранилища файлов должны совпадать с заархивированным хранилищем файлов, чтобы компоненты, использующие эти файлы, могли получать к ним доступ.</span><span class="sxs-lookup"><span data-stu-id="79695-123">The path and file name for the restored File Store should be exactly the same as the backed up File Store so that components that use the files can access them.</span></span>

    
    </div>

4.  <span data-ttu-id="79695-124">Выполните одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="79695-124">Do one of the following:</span></span>
    
      - <span data-ttu-id="79695-125">Если вы устанавливаете сервер Standard Edition, перейдите в папку установки Lync Server или мультимедиа, а затем запустите мастер развертывания Lync Server, расположенный на странице \\ Setup \\ amd64 \\Setup.exe.</span><span class="sxs-lookup"><span data-stu-id="79695-125">If you are installing a Standard Edition server, browse to the Lync Server installation folder or media, and then start the Lync Server Deployment Wizard located at \\setup\\amd64\\Setup.exe.</span></span> <span data-ttu-id="79695-126">В мастере развертывания нажмите кнопку **подготовить первый сервер Standard Edition** и следуйте указаниям мастера, чтобы установить хранилище Центрального управления.</span><span class="sxs-lookup"><span data-stu-id="79695-126">In the Deployment Wizard, click **Prepare first Standard Edition server** and follow the wizard to install the Central Management store.</span></span>
    
      - <span data-ttu-id="79695-127">Если вы устанавливаете сервер корпоративного уровня, установите SQL Server 2012 или SQL Server 2008 R2, сохранив имена экземпляров так же, как и до сбоя.</span><span class="sxs-lookup"><span data-stu-id="79695-127">If you are installing an Enterprise Back End Server, install SQL Server 2012 or SQL Server 2008 R2, keeping the instance names the same as before the failure.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="79695-128">В зависимости от сервера, который вы восстанавливаете, и при развертывании сервер может включать несколько размещенных или отдельных баз данных.</span><span class="sxs-lookup"><span data-stu-id="79695-128">Depending on the server that you are restoring and on your deployment, the server might include multiple collocated or separate databases.</span></span> <span data-ttu-id="79695-129">Выполните те же действия, чтобы установить SQL Server, который использовался изначально для развертывания сервера, включая разрешения SQL Server и учетные записи.</span><span class="sxs-lookup"><span data-stu-id="79695-129">Follow the same procedure to install SQL Server that you used originally to deploy the server, including SQL Server permissions and logins.</span></span>

        
        </div>

5.  <span data-ttu-id="79695-130">На сервере переднего плана запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите пункт **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="79695-130">From a Front End Server, Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

6.  <span data-ttu-id="79695-131">Повторно создайте хранилище Центрального управления.</span><span class="sxs-lookup"><span data-stu-id="79695-131">Re-create the Central Management store.</span></span> <span data-ttu-id="79695-132">В командной строке введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="79695-132">At the command line, type:</span></span>
    
        Install-CsDatabase -CentralManagementDatabase -Clean -SqlServerFqdn <FQDN> -SqlInstanceName <instance name> -Verbose
    
    <span data-ttu-id="79695-133">Например:</span><span class="sxs-lookup"><span data-stu-id="79695-133">For example:</span></span>
    
        Install-CsDatabase -CentralManagementDatabase -Clean -SqlServerFqdn Server01.contoso.com -SqlInstanceName cms -Verbose

7.  <span data-ttu-id="79695-134">Настройте контрольную точку доменных служб Active Directory для хранилища центрального управления.</span><span class="sxs-lookup"><span data-stu-id="79695-134">Set the Active Directory Domain Services control point for the Central Management store.</span></span> <span data-ttu-id="79695-135">В командной строке введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="79695-135">At the command line, type:</span></span>
    
        Set-CsConfigurationStoreLocation -SqlServerFqdn <FQDN> -SqlInstanceName <instance name> -Verbose
    
    <span data-ttu-id="79695-136">Например:</span><span class="sxs-lookup"><span data-stu-id="79695-136">For example:</span></span>
    
        Set-CsConfigurationStoreLocation -SqlServerFqdn Server01.contoso.com -SqlInstanceName cms -Verbose
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="79695-137">Если вы потеряли точку соединения, вы можете повторно запустить этот командлет.</span><span class="sxs-lookup"><span data-stu-id="79695-137">If you lose the connection point, you can rerun this cmdlet.</span></span>

    
    </div>

8.  <span data-ttu-id="79695-138">Импортируйте данные из хранилища Central Management Store из $Backup.</span><span class="sxs-lookup"><span data-stu-id="79695-138">Import the Central Management store data from $Backup.</span></span> <span data-ttu-id="79695-139">В командной строке введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="79695-139">At the command line, type:</span></span>
    
        Import-CsConfiguration -FileName <CMS backup file name>
    
    <span data-ttu-id="79695-140">Например:</span><span class="sxs-lookup"><span data-stu-id="79695-140">For example:</span></span>
    
        Import-CsConfiguration -FileName "C:\Config.zip"

9.  <span data-ttu-id="79695-141">Включите только что сделанные изменения.</span><span class="sxs-lookup"><span data-stu-id="79695-141">Enable the changes you have just made.</span></span> <span data-ttu-id="79695-142">В командной строке выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="79695-142">At the command line, type:</span></span>
    
        Enable-CsTopology
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="79695-143">После включения топологии вы можете найти документ Topology в базе данных.</span><span class="sxs-lookup"><span data-stu-id="79695-143">After you enable the topology, you can find the topology document in the database.</span></span>

    
    </div>

10. <span data-ttu-id="79695-144">Если вы восстанавливаете сервер, на котором размещена версия Enterprise Edition, который также является сервером CMS, или вам нужно повторно создать зеркало для CMS, выполните это действие.</span><span class="sxs-lookup"><span data-stu-id="79695-144">If you are restoring an Enterprise Edition Back End Server that also hosted the CMS, or if you need to re-create a mirror of the CMS, then follow this step.</span></span> <span data-ttu-id="79695-145">В противном случае перейдите к шагу 11.</span><span class="sxs-lookup"><span data-stu-id="79695-145">Otherwise, skip to step 11.</span></span>
    
    <span data-ttu-id="79695-146">Установите автономные базы данных, выполнив указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="79695-146">Install the stand-alone databases by doing the following:</span></span>
    
    1.  <span data-ttu-id="79695-147">Запустить построитель топологии: нажмите кнопку **Пуск**, выберите пункт **все программы**, а затем — **Microsoft Lync Server 2013** и нажмите кнопку **Построитель топологии Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="79695-147">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>
    
    2.  <span data-ttu-id="79695-148">Нажмите кнопку **загрузить топологию из существующего развертывания** и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="79695-148">Click **Download Topology from existing deployment**, and then click **OK**.</span></span>
    
    3.  <span data-ttu-id="79695-149">Выберите топологию и нажмите кнопку **сохранить**.</span><span class="sxs-lookup"><span data-stu-id="79695-149">Select the topology, and then click **Save**.</span></span> <span data-ttu-id="79695-150">Нажмите кнопку **Да** , чтобы подтвердить выбор.</span><span class="sxs-lookup"><span data-stu-id="79695-150">Click **Yes** to confirm your selection.</span></span>
    
    4.  <span data-ttu-id="79695-151">Щелкните правой кнопкой мыши узел **Lync Server 2013** и выберите команду **установить базу данных**.</span><span class="sxs-lookup"><span data-stu-id="79695-151">Right-click the **Lync Server 2013** node, and then click **Install Database**.</span></span>
    
    5.  <span data-ttu-id="79695-152">Следуйте указаниям мастера **установки базы данных** .</span><span class="sxs-lookup"><span data-stu-id="79695-152">Follow the **Install Database** wizard.</span></span> <span data-ttu-id="79695-153">Если вы восстанавливаете базу данных, отличную от хранилища Central Management на этом сервере, на странице **Создание баз данных** выберите базы данных, которые вы хотите повторно создать.</span><span class="sxs-lookup"><span data-stu-id="79695-153">If you are restoring a database other than the Central Management store on this server, on the **Create databases** page, select the databases you want to recreate.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="79695-154">На странице <STRONG>Создание баз данных</STRONG> отображаются только отдельные базы данных.</span><span class="sxs-lookup"><span data-stu-id="79695-154">Only stand-alone databases are displayed on the <STRONG>Create databases</STRONG> page.</span></span> <span data-ttu-id="79695-155">Выровненные базы данных создаются при запуске мастера развертывания Lync Server.</span><span class="sxs-lookup"><span data-stu-id="79695-155">Collocated databases are created when you run the Lync Server Deployment Wizard.</span></span>

        
        </div>
    
    6.  <span data-ttu-id="79695-156">Если вы восстанавливаете зеркальный сервер, продолжайте подписаться на работу мастера, пока не появится запрос на создание зеркальной базы данных.</span><span class="sxs-lookup"><span data-stu-id="79695-156">If you are restoring a mirrored Back End Server, continue to follow the rest of the wizard until you come to a prompt of Create Mirror Database.</span></span> <span data-ttu-id="79695-157">Выберите базу данных, которую вы хотите установить, и выполните описанные выше действия.</span><span class="sxs-lookup"><span data-stu-id="79695-157">Select the database you want to install, and complete the process.</span></span>
    
    7.  <span data-ttu-id="79695-158">Следуйте дальнейшим указаниям мастера, а затем нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="79695-158">Follow the rest of the wizard, and then click **Finish**.</span></span>
    
    <div>
    

    > [!TIP]  
    > <span data-ttu-id="79695-159">Вместо того чтобы запустить построитель топологии, вы можете использовать командлет <STRONG>Install-CsDatabase</STRONG> для создания каждой базы данных и командлет <STRONG>Install-CsMirrorDatabase</STRONG> для настройки зеркального отображения.</span><span class="sxs-lookup"><span data-stu-id="79695-159">Instead of running Topology Builder, you can use the <STRONG>Install-CsDatabase</STRONG> cmdlet to create each database, and the <STRONG>Install-CsMirrorDatabase</STRONG> cmdlet to configure mirroring.</span></span> <span data-ttu-id="79695-160">Подробные сведения можно найти в разделе <A href="https://docs.microsoft.com/powershell/module/skype/Install-CsDatabase">Install-CsDatabase</A> и <A href="https://docs.microsoft.com/powershell/module/skype/Install-CsMirrorDatabase">Install-CsMirrorDatabase</A>.</span><span class="sxs-lookup"><span data-stu-id="79695-160">For details, see <A href="https://docs.microsoft.com/powershell/module/skype/Install-CsDatabase">Install-CsDatabase</A> and <A href="https://docs.microsoft.com/powershell/module/skype/Install-CsMirrorDatabase">Install-CsMirrorDatabase</A>.</span></span>

    
    </div>

11. <span data-ttu-id="79695-161">Если вы восстанавливаете Стандартный сервер выпуска, перейдите в папку установки Lync Server или мультимедиа, а затем запустите мастер развертывания Lync Server, расположенный на странице \\ Setup \\ amd64 \\Setup.exe.</span><span class="sxs-lookup"><span data-stu-id="79695-161">If you are restoring a Standard Edition server, browse to the Lync Server installation folder or media, and start the Lync Server Deployment Wizard located at \\setup\\amd64\\Setup.exe.</span></span> <span data-ttu-id="79695-162">С помощью мастера развертывания Lync Server выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="79695-162">Use the Lync Server Deployment Wizard to do the following:</span></span>
    
    1.  <span data-ttu-id="79695-163">Выполните **Шаг 1: установите локальное хранилище конфигураций** , чтобы установить локальные файлы конфигурации.</span><span class="sxs-lookup"><span data-stu-id="79695-163">Run **Step 1: Install Local Configuration Store** to install the local configuration files.</span></span>
    
    2.  <span data-ttu-id="79695-164">Запустите **Шаг 2: Настройка или удаление компонентов Lync Server** для установки ролей сервера Lync Server.</span><span class="sxs-lookup"><span data-stu-id="79695-164">Run **Step 2: Setup or Remove Lync Server Components** to install the Lync Server server roles.</span></span>
    
    3.  <span data-ttu-id="79695-165">Запустите **Шаг 3: запросите, установите или назначьте сертификаты** для назначения сертификатов.</span><span class="sxs-lookup"><span data-stu-id="79695-165">Run **Step 3: Request, Install or Assign Certificates** to assign the certificates.</span></span>
    
    4.  <span data-ttu-id="79695-166">Выполните **Шаг 4: запуск служб** для запуска служб на сервере.</span><span class="sxs-lookup"><span data-stu-id="79695-166">Run **Step 4: Start Services** to start services on the server.</span></span>
    
    <span data-ttu-id="79695-167">Дополнительные сведения о запуске мастера развертывания можно найти в документации по развертыванию роли сервера, которую вы восстанавливаете.</span><span class="sxs-lookup"><span data-stu-id="79695-167">For details about running the Deployment Wizard, see the Deployment documentation for the server role that you are restoring.</span></span>

12. <span data-ttu-id="79695-168">Восстановите данные пользователя, выполнив указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="79695-168">Restore user data by performing the following:</span></span>
    
    1.  <span data-ttu-id="79695-169">Копирование ExportedUserData.zip из $Backup \\ в локальный каталог.</span><span class="sxs-lookup"><span data-stu-id="79695-169">Copy ExportedUserData.zip from $Backup\\ to a local directory.</span></span>
    
    2.  <span data-ttu-id="79695-170">Прежде чем восстанавливать данные пользователя, необходимо остановить службы Lync.</span><span class="sxs-lookup"><span data-stu-id="79695-170">Before you restore the user data, you must stop Lync services.</span></span> <span data-ttu-id="79695-171">Для этого введите:</span><span class="sxs-lookup"><span data-stu-id="79695-171">To do so, type:</span></span>
        
            Stop-CsWindowsService
    
    3.  <span data-ttu-id="79695-172">Чтобы восстановить данные пользователя, в командной строке введите:</span><span class="sxs-lookup"><span data-stu-id="79695-172">To restore the user data, at the command line, type:</span></span>
        
            Import-CsUserData -PoolFqdn <Fqdn> -FileName <String>
        
        <span data-ttu-id="79695-173">Например:</span><span class="sxs-lookup"><span data-stu-id="79695-173">For example:</span></span>
        
            Import-CsUserData -PoolFqdn "atl0cs-001.litwareinc.com" -FileName "C:\Logs\ExportedUserDatal.zip"
    
    4.  <span data-ttu-id="79695-174">Перезапустите службы Lync, введя:</span><span class="sxs-lookup"><span data-stu-id="79695-174">Restart Lync services by typing:</span></span>
        
            Start-CsWindowsService

13. <span data-ttu-id="79695-175">Восстановите данные о расположении в хранилище Центрального управления.</span><span class="sxs-lookup"><span data-stu-id="79695-175">Restore Location Information data to the Central Management store.</span></span> <span data-ttu-id="79695-176">В командной строке введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="79695-176">At the command line, type:</span></span>
    
        Import-CsLisConfiguration -FileName <LIS backup file name>
    
    <span data-ttu-id="79695-177">Например:</span><span class="sxs-lookup"><span data-stu-id="79695-177">For example:</span></span>
    
        Import-CsLisConfiguration -FileName "D:\E911Config.zip"

14. <span data-ttu-id="79695-178">Если вы развернули группу ответа в этом пуле или на сервере Standard Edition, восстановите данные конфигурации группы ответа.</span><span class="sxs-lookup"><span data-stu-id="79695-178">If you deployed Response Group on this pool or Standard Edition server, restore the Response Group configuration data.</span></span> <span data-ttu-id="79695-179">Подробности можно найти [в разделе Восстановление параметров группы ответов в Lync Server 2013](lync-server-2013-restoring-response-group-settings.md).</span><span class="sxs-lookup"><span data-stu-id="79695-179">For details, see [Restoring Response Group settings in Lync Server 2013](lync-server-2013-restoring-response-group-settings.md).</span></span>

15. <span data-ttu-id="79695-180">Если вы восстанавливаете резервный сервер, который включает в себя архивирование и мониторинг баз данных, восстановите данные архивации или наблюдения с помощью средства управления SQL Server, например SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="79695-180">If you are restoring a Back End Server that includes Archiving or Monitoring databases, restore the Archiving or Monitoring data by using a SQL Server management tool, such as SQL Server Management Studio.</span></span> <span data-ttu-id="79695-181">Подробности можно найти [в разделе Восстановление мониторинга или архивация данных в Lync Server 2013](lync-server-2013-restoring-monitoring-or-archiving-data.md).</span><span class="sxs-lookup"><span data-stu-id="79695-181">For details, see [Restoring monitoring or archiving data in Lync Server 2013](lync-server-2013-restoring-monitoring-or-archiving-data.md).</span></span>

<span data-ttu-id="79695-182"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="79695-182"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

