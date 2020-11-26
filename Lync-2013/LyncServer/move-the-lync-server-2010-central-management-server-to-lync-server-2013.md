---
title: Перемещение сервера Lync Server 2010 на центральный сервер SMS на Lync Server 2013
description: Переместите сервер Lync Server 2010 на Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Move the Lync Server 2010 Central Management Server to Lync Server 2013
ms:assetid: 30cc98f2-1916-4dbe-99d0-8df5368ed3ec
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688013(v=OCS.15)
ms:contentKeyID: 49733602
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 19d53d797375b1eb8fde72f6b999e509b97f85ae
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443295"
---
# <a name="move-the-lync-server-2010-central-management-server-to-lync-server-2013"></a><span data-ttu-id="57e58-103">Перемещение сервера Lync Server 2010 на центральный сервер SMS на Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="57e58-103">Move the Lync Server 2010 Central Management Server to Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="57e58-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="57e58-104">

<span> </span></span></span>

<span data-ttu-id="57e58-105">_**Тема последнего изменения:** 2013-11-25_</span><span class="sxs-lookup"><span data-stu-id="57e58-105">_**Topic Last Modified:** 2013-11-25_</span></span>

<span data-ttu-id="57e58-106">После перехода с Lync Server 2010 на Lync Server 2013 вам потребуется переместить сервер центрального управления Lync Server 2010 на сервер Lync Server 2013 или в пул, прежде чем можно будет удалить старый сервер Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="57e58-106">After migrating from Lync Server 2010 to Lync Server 2013, you need to move the Lync Server 2010 Central Management Server to the Lync Server 2013 Front End Server or pool, before you can remove the legacy Lync Server 2010 server.</span></span>

<span data-ttu-id="57e58-107">Центральный сервер управления — это единая Главная или несколько реплик, где сервер переднего плана, на котором находится база данных для чтения и записи, находится на сервере, который содержит центральный сервер управления.</span><span class="sxs-lookup"><span data-stu-id="57e58-107">The Central Management Server is a single master/multiple replica system, where the read/write copy of the database is held by the Front End Server that contains the Central Management Server.</span></span> <span data-ttu-id="57e58-108">На каждом компьютере в топологии, включая сервер переднего плана, на котором находится центральный сервер управления, доступна только для чтения копия данных центрального хранилища в базе данных SQL Server (с именем RTCLOCAL по умолчанию), установленная на компьютере во время установки и развертывания.</span><span class="sxs-lookup"><span data-stu-id="57e58-108">Each computer in the topology, including the Front End Server that contains the Central Management Server, has a read-only copy of the Central Management store data in the SQL Server database (named RTCLOCAL by default) installed on the computer during setup and deployment.</span></span> <span data-ttu-id="57e58-109">Локальная база данных получает обновления реплики с помощью агента репликатора реплики Lync Server, который запускается как служба на всех компьютерах.</span><span class="sxs-lookup"><span data-stu-id="57e58-109">The local database receives replica updates by way of the Lync Server Replica Replicator Agent that runs as a service on all computers.</span></span> <span data-ttu-id="57e58-110">Имя реальной базы данных на центральном сервере управления и в локальной реплике — XDS, которая состоит из файлов XDS. mdf и XDS. ldf.</span><span class="sxs-lookup"><span data-stu-id="57e58-110">The name of the actual database on the Central Management Server and the local replica is XDS, which is made up of the xds.mdf and xds.ldf files.</span></span> <span data-ttu-id="57e58-111">На расположение базы данных Master ссылается точка управления службой (SCP) доменных служб Active Directory.</span><span class="sxs-lookup"><span data-stu-id="57e58-111">The master database location is referenced by a service control point (SCP) in Active Directory Domain Services.</span></span> <span data-ttu-id="57e58-112">Все средства, использующие центральный сервер управления для управления и настройки Lync Server, используют SCP для поиска хранилища центрального управления.</span><span class="sxs-lookup"><span data-stu-id="57e58-112">All tools that use the Central Management Server to manage and configure Lync Server use the SCP to locate the Central Management store.</span></span>

<span data-ttu-id="57e58-113">После успешного перемещения центрального сервера управления необходимо удалить базы данных центрального сервера управления с исходного сервера переднего плана.</span><span class="sxs-lookup"><span data-stu-id="57e58-113">After you have successfully moved the Central Management Server, you should remove the Central Management Server databases from the original Front End Server.</span></span> <span data-ttu-id="57e58-114">Сведения об удалении баз данных центрального сервера управления можно найти в разделе [Удаление базы данных SQL Server для пула переднего плана](remove-the-sql-server-database-for-a-front-end-pool.md).</span><span class="sxs-lookup"><span data-stu-id="57e58-114">For information on removing the Central Management Server databases, see [Remove the SQL Server database for a Front End pool](remove-the-sql-server-database-for-a-front-end-pool.md).</span></span>

<span data-ttu-id="57e58-115">С помощью командлета Windows PowerShell **Remove-CsManagementServer** в командной консоли Lync Server Management Shell можно переместить базу данных из базы данных lync Server 2010 SQL Server в базу данных сервера lync Server 2013 и затем обновить SCP, чтобы она указывала на расположение сервера lync Server 2013 Central Management Server.</span><span class="sxs-lookup"><span data-stu-id="57e58-115">You use the Windows PowerShell cmdlet **Move-CsManagementServer** in the Lync Server Management Shell to move the database from the Lync Server 2010 SQL Server database to the Lync Server 2013 SQL Server database, and then update the SCP to point to the Lync Server 2013 Central Management Server location.</span></span>

<div>

## <a name="preparing-lync-server-2013-front-end-servers-before-moving-the-central-management-server"></a><span data-ttu-id="57e58-116">Подготовка серверов переднего плана Lync Server 2013 перед перемещением центрального сервера управления</span><span class="sxs-lookup"><span data-stu-id="57e58-116">Preparing Lync Server 2013 Front End Servers before moving the Central Management Server</span></span>

<span data-ttu-id="57e58-117">С помощью описанных в этом разделе процедур вы сможете подготовить серверы переднего плана Lync Server 2013, прежде чем переносить сервер центрального управления Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="57e58-117">Use the procedures in this section to prepare the Lync Server 2013 Front End Servers before you move the Lync Server 2010 Central Management Server.</span></span>

<div>

## <a name="to-prepare-an-enterprise-edition-front-end-pool"></a><span data-ttu-id="57e58-118">Подготовка пула переднего плана Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="57e58-118">To prepare an Enterprise Edition Front End pool</span></span>

1.  <span data-ttu-id="57e58-119">В пуле внешних интерфейсов Lync Server 2013 Enterprise Edition, где вы хотите переместить сервер центрального управления: Войдите в систему с компьютера, на котором установлена консоль управления Lync Server, в качестве участника группы **RTCUniversalServerAdmins** .</span><span class="sxs-lookup"><span data-stu-id="57e58-119">On the Lync Server 2013 Enterprise Edition Front End pool where you want to relocate the Central Management Server: Log on to the computer where the Lync Server Management Shell is installed as a member of the **RTCUniversalServerAdmins** group.</span></span> <span data-ttu-id="57e58-120">Кроме того, необходимо иметь права и разрешения администратора базы данных SQL Server для базы данных, в которой вы хотите установить хранилище Центрального управления.</span><span class="sxs-lookup"><span data-stu-id="57e58-120">You must also have SQL Server database sysadmin user rights and permissions on the database where you want to install the Central Management store.</span></span>

2.  <span data-ttu-id="57e58-121">Откройте командную консоль Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="57e58-121">Open the Lync Server Management Shell.</span></span>

3.  <span data-ttu-id="57e58-122">Чтобы создать новое хранилище Central Management в базе данных SQL Server в Lync Server 2013, в командной консоли Lync Server введите:</span><span class="sxs-lookup"><span data-stu-id="57e58-122">To create the new Central Management store in the Lync Server 2013 SQL Server database, in the Lync Server Management Shell, type:</span></span>
    
        Install-CsDatabase -CentralManagementDatabase -SQLServerFQDN <FQDN of your SQL Server> -SQLInstanceName <name of instance>

4.  <span data-ttu-id="57e58-123">Убедитесь в том, что **запущена** служба **переднего плана Lync Server** .</span><span class="sxs-lookup"><span data-stu-id="57e58-123">Confirm that the status of the **Lync Server Front-End** service is **Started**.</span></span>

</div>

<div>

## <a name="to-prepare-a-standard-edition-front-end-server"></a><span data-ttu-id="57e58-124">Подготовка сервера переднего плана Standard Edition к выпуску</span><span class="sxs-lookup"><span data-stu-id="57e58-124">To prepare a Standard Edition Front End Server</span></span>

1.  <span data-ttu-id="57e58-125">На сервере Lync Server 2013 Standard Edition, на котором вы хотите переместить сервер центрального управления: Войдите в систему с компьютера, на котором установлена консоль управления Lync Server, в качестве участника группы **RTCUniversalServerAdmins** .</span><span class="sxs-lookup"><span data-stu-id="57e58-125">On the Lync Server 2013 Standard Edition Front End Server where you want to relocate the Central Management Server: Log on to the computer where the Lync Server Management Shell is installed as a member of the **RTCUniversalServerAdmins** group.</span></span>

2.  <span data-ttu-id="57e58-126">Запустите мастер развертывания Lync Server.</span><span class="sxs-lookup"><span data-stu-id="57e58-126">Open the Lync Server Deployment Wizard.</span></span>

3.  <span data-ttu-id="57e58-127">В мастере развертывания Lync Server нажмите кнопку **подготовить первый сервер Standard Edition**.</span><span class="sxs-lookup"><span data-stu-id="57e58-127">In the Lync Server Deployment Wizard, click **Prepare first Standard Edition server**.</span></span>

4.  <span data-ttu-id="57e58-128">На странице **выполнение команд** SQL Server Express установлен в качестве центрального сервера управления.</span><span class="sxs-lookup"><span data-stu-id="57e58-128">On the **Executing Commands** page, SQL Server Express is installed as the Central Management Server.</span></span> <span data-ttu-id="57e58-129">Создаются необходимые правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="57e58-129">Necessary firewall rules are created.</span></span> <span data-ttu-id="57e58-130">После завершения установки базы данных и необходимого программного обеспечения нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="57e58-130">When the installation of the database and prerequisite software is completed, click **Finish**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="57e58-131">Начальная установка может занять некоторое время и не отменять заметные обновления экрана сводки вывода команды.</span><span class="sxs-lookup"><span data-stu-id="57e58-131">The initial installation may take some time with no visible updates to the command output summary screen.</span></span> <span data-ttu-id="57e58-132">Это происходит из-за установки SQL Server Express.</span><span class="sxs-lookup"><span data-stu-id="57e58-132">This is due to the installation of the SQL Server Express.</span></span> <span data-ttu-id="57e58-133">Если вам нужно наблюдать за установкой базы данных, используйте диспетчер задач для наблюдения за настройкой.</span><span class="sxs-lookup"><span data-stu-id="57e58-133">If you need to monitor the installation of the database, use Task Manager to monitor the setup.</span></span>

    
    </div>

5.  <span data-ttu-id="57e58-134">Чтобы создать новое хранилище Central Management на сервере переднего плана Lync Server 2013 Standard Edition, в командной консоли Lync Server введите:</span><span class="sxs-lookup"><span data-stu-id="57e58-134">To create the new Central Management store on the Lync Server 2013 Standard Edition Front End Server, in the Lync Server Management Shell, type:</span></span>
    
        Install-CsDatabase -CentralManagementDatabase -SQLServerFQDN <FQDN of your Standard Edition Server> -SQLInstanceName <name of instance - RTC by default>

6.  <span data-ttu-id="57e58-135">Убедитесь в том, что **запущена** служба **переднего плана Lync Server** .</span><span class="sxs-lookup"><span data-stu-id="57e58-135">Confirm that the status of the **Lync Server Front-End** service is **Started**.</span></span>

</div>

</div>

<div>

## <a name="to-move-the-lync-server-2010-central-management-server-to-lync-server-2013"></a><span data-ttu-id="57e58-136">Перемещение сервера Lync Server 2010 на Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="57e58-136">To move the Lync Server 2010 Central Management Server to Lync Server 2013</span></span>

1.  <span data-ttu-id="57e58-137">На сервере Lync Server 2013, который будет основным сервером управления: Войдите в систему с компьютера, на котором установлена консоль управления Lync Server, в качестве участника группы **RTCUniversalServerAdmins** .</span><span class="sxs-lookup"><span data-stu-id="57e58-137">On the Lync Server 2013 server that will be the Central Management Server: Log on to the computer where the Lync Server Management Shell is installed as a member of the **RTCUniversalServerAdmins** group.</span></span> <span data-ttu-id="57e58-138">Кроме того, необходимо иметь права и разрешения администратора базы данных SQL Server.</span><span class="sxs-lookup"><span data-stu-id="57e58-138">You must also have the SQL Server database administrator user rights and permissions.</span></span>

2.  <span data-ttu-id="57e58-139">Откройте командную консоль Lync Server.</span><span class="sxs-lookup"><span data-stu-id="57e58-139">Open Lync Server Management Shell.</span></span>

3.  <span data-ttu-id="57e58-140">В командной консоли Lync Server введите:</span><span class="sxs-lookup"><span data-stu-id="57e58-140">In the Lync Server Management Shell, type:</span></span>
    
        Enable-CsTopology
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="57e58-141">Если <CODE>Enable-CsTopology</CODE> это не помогло, устраните проблему, так как она не может завершиться, прежде чем продолжить.</span><span class="sxs-lookup"><span data-stu-id="57e58-141">If <CODE>Enable-CsTopology</CODE> is not successful, resolve the problem preventing the command from completing before continuing.</span></span> <span data-ttu-id="57e58-142">Если <STRONG>параметр Enable-CsTopology</STRONG> не прошел успешно, перемещение завершится сбоем, и ваша топология может остаться в состоянии, в котором нет центрального хранилища управления.</span><span class="sxs-lookup"><span data-stu-id="57e58-142">If <STRONG>Enable-CsTopology</STRONG> is not successful, the move will fail and it may leave your topology in a state where there is no Central Management store.</span></span>

    
    </div>

4.  <span data-ttu-id="57e58-143">На сервере переднего плана Lync Server 2013 или пуле переднего плана в командной консоли Lync Server Management Shell введите:</span><span class="sxs-lookup"><span data-stu-id="57e58-143">On the Lync Server 2013 Front End Server or Front End pool, in the Lync Server Management Shell, type:</span></span>
    
        Move-CsManagementServer

5.  <span data-ttu-id="57e58-144">Консоль управления Lync Server отображает серверы, хранилища файлов, хранилища баз данных и точки соединения служб для текущего состояния и предлагаемого состояния.</span><span class="sxs-lookup"><span data-stu-id="57e58-144">Lync Server Management Shell displays the servers, file stores, database stores, and the service connection points of the Current State and the Proposed State.</span></span> <span data-ttu-id="57e58-145">Внимательно прочтите информацию и подтвердите, что это предполагаемый источник и назначение.</span><span class="sxs-lookup"><span data-stu-id="57e58-145">Read the information carefully and confirm that this is the intended source and destination.</span></span> <span data-ttu-id="57e58-146">Введите **Y** , чтобы продолжить, или **N** , чтобы прервать перемещение.</span><span class="sxs-lookup"><span data-stu-id="57e58-146">Type **Y** to continue, or **N** to stop the move.</span></span>

6.  <span data-ttu-id="57e58-147">Проверьте все предупреждения и ошибки, созданные командой **Move-CsManagementServer** , и устраните их.</span><span class="sxs-lookup"><span data-stu-id="57e58-147">Review any warnings or errors generated by the **Move-CsManagementServer** command and resolve them.</span></span>

7.  <span data-ttu-id="57e58-148">На сервере Lync Server 2013 откройте мастер развертывания Lync Server.</span><span class="sxs-lookup"><span data-stu-id="57e58-148">On the Lync Server 2013 server, open the Lync Server Deployment Wizard.</span></span>

8.  <span data-ttu-id="57e58-149">В мастере развертывания Lync Server нажмите кнопку **Установка или обновление системы Lync** Server, выберите **Шаг 2: Настройка или удаление компонентов Lync Server**, нажмите кнопку **Далее**, просмотрите сводку и нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="57e58-149">In Lync Server Deployment Wizard, click **Install or Update Lync Server System**, click **Step 2: Setup or Remove Lync Server Components**, click **Next**, review the summary, and then click **Finish**.</span></span>

9.  <span data-ttu-id="57e58-150">На сервере Lync Server 2010 откройте мастер развертывания Lync Server.</span><span class="sxs-lookup"><span data-stu-id="57e58-150">On the Lync Server 2010 server, open the Lync Server Deployment Wizard.</span></span>

10. <span data-ttu-id="57e58-151">В мастере развертывания Lync Server нажмите кнопку **Установка или обновление системы Lync** Server, выберите **Шаг 2: Настройка или удаление компонентов Lync Server**, нажмите кнопку **Далее**, просмотрите сводку и нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="57e58-151">In Lync Server Deployment Wizard, click **Install or Update Lync Server System**, click **Step 2: Setup or Remove Lync Server Components**, click **Next**, review the summary, and then click **Finish**.</span></span>

11. <span data-ttu-id="57e58-152">Перезагрузите сервер Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="57e58-152">Reboot the Lync Server 2013 server.</span></span> <span data-ttu-id="57e58-153">Это необходимо из-за изменения членства в группе на доступ к базе данных центрального сервера управления.</span><span class="sxs-lookup"><span data-stu-id="57e58-153">This is required because of a group membership change to access Central Management Server database.</span></span>

12. <span data-ttu-id="57e58-154">Чтобы убедиться в том, что репликация с новым хранилищем централизованного управления выполняется, в командной консоли Lync Server введите:</span><span class="sxs-lookup"><span data-stu-id="57e58-154">To confirm that replication with the new Central Management store is occurring, in the Lync Server Management Shell, type:</span></span>
    
        Get-CsManagementStoreReplicationStatus
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="57e58-155">Для обновления всех текущих реплик репликации может потребоваться некоторое время.</span><span class="sxs-lookup"><span data-stu-id="57e58-155">The replication may take some time to update all current replicas.</span></span>

    
    </div>

</div>

<div>

## <a name="to-remove-lync-server-2010-central-management-store-files-after-a-move"></a><span data-ttu-id="57e58-156">Удаление файлов Lync Server 2010 Central Management Store после перемещения</span><span class="sxs-lookup"><span data-stu-id="57e58-156">To remove Lync Server 2010 Central Management store files after a move</span></span>

1.  <span data-ttu-id="57e58-157">На сервере Lync Server 2010: Войдите в систему с компьютера, на котором установлена консоль управления Lync Server, в качестве участника группы **RTCUniversalServerAdmins** .</span><span class="sxs-lookup"><span data-stu-id="57e58-157">On the Lync Server 2010 server: Log on to the computer where the Lync Server Management Shell is installed as a member of the **RTCUniversalServerAdmins** group.</span></span> <span data-ttu-id="57e58-158">Кроме того, необходимо иметь права и разрешения администратора базы данных SQL Server.</span><span class="sxs-lookup"><span data-stu-id="57e58-158">You must also have the SQL Server database administrator user rights and permissions.</span></span>

2.  <span data-ttu-id="57e58-159">Открытие командной консоли Lync Server</span><span class="sxs-lookup"><span data-stu-id="57e58-159">Open Lync Server Management Shell</span></span>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="57e58-160">Не продолжайте удалять предыдущие файлы базы данных, пока репликация не будет завершена и является стабильной.</span><span class="sxs-lookup"><span data-stu-id="57e58-160">Do not proceed with the removal of the previous database files until replication is complete and is stable.</span></span> <span data-ttu-id="57e58-161">Если вы удалите файлы перед выполнением репликации, процесс репликации будет прерван, а новый сервер центрального управления останется в неизвестном состоянии.</span><span class="sxs-lookup"><span data-stu-id="57e58-161">If you remove the files prior to completing replication, you will disrupt the replication process and leave the newly moved Central Management Server in an unknown state.</span></span> <span data-ttu-id="57e58-162">С помощью командлета <STRONG>Get-CsManagementStoreReplicationStatus</STRONG> можно подтвердить состояние репликации.</span><span class="sxs-lookup"><span data-stu-id="57e58-162">Use the cmdlet <STRONG>Get-CsManagementStoreReplicationStatus</STRONG> to confirm the replication status.</span></span>

    
    </div>

3.  <span data-ttu-id="57e58-163">Чтобы удалить файлы базы данных центра администрирования из Lync Server 2010 на центральном сервере Management Server, введите:</span><span class="sxs-lookup"><span data-stu-id="57e58-163">To remove the Central Management store database files from the Lync Server 2010 Central Management Server, type:</span></span>
    
        Uninstall-CsDatabase -CentralManagementDatabase -SqlServerFqdn <FQDN of SQL Server> -SqlInstanceName <Name of source server>
    
    <span data-ttu-id="57e58-164">Например:</span><span class="sxs-lookup"><span data-stu-id="57e58-164">For example:</span></span>
    
        Uninstall-CsDatabase -CentralManagementDatabase -SqlServerFqdn sql.contoso.net -SqlInstanceName rtc
    
    <span data-ttu-id="57e58-165">Где \<FQDN of SQL Server\> можно задать сервер Lync server 2010 в развертывании Enterprise Edition или полное доменное имя сервера Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="57e58-165">Where the \<FQDN of SQL Server\> is either the Lync Server 2010 Back End Server in an Enterprise Edition deployment or the FQDN of the Standard Edition server.</span></span>

<span data-ttu-id="57e58-166"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="57e58-166"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

