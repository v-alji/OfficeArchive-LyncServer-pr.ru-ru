---
title: 'Lync Server 2013: исключения из антивирусной проверки'
description: 'Lync Server 2013: исключения антивирусной проверки.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Antivirus scanning exclusions for Lync Server 2013
ms:assetid: 71e1f1cc-2d16-4111-9864-9276bf24dfe0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn440138(v=OCS.15)
ms:contentKeyID: 57793042
ms.date: 11/03/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 20c395f529cad91993d003efdeb231bd66f4b9bc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440663"
---
# <a name="antivirus-scanning-exclusions-for-lync-server-2013"></a><span data-ttu-id="dac85-103">Исключения из антивирусной проверки для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dac85-103">Antivirus scanning exclusions for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="dac85-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="dac85-104">

<span> </span></span></span>

<span data-ttu-id="dac85-105">_**Тема последнего изменения:** 2015-11-02_</span><span class="sxs-lookup"><span data-stu-id="dac85-105">_**Topic Last Modified:** 2015-11-02_</span></span>

<span data-ttu-id="dac85-106">Чтобы антивирусная программа не мешала работе с Lync Server 2013, необходимо исключить определенные процессы и каталоги для каждого сервера или серверной роли Lync Server 2013, на которых вы запускаете антивирусную программу.</span><span class="sxs-lookup"><span data-stu-id="dac85-106">To ensure that the antivirus scanner does not interfere with the operation of Lync Server 2013, you must exclude specific processes and directories for each Lync Server 2013 server or server role on which you run an antivirus scanner.</span></span> <span data-ttu-id="dac85-107">Исключите перечисленные ниже процессы и каталоги.</span><span class="sxs-lookup"><span data-stu-id="dac85-107">The following processes and directories should be excluded:</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="dac85-108">Ниже указаны расположения файлов и папок для Lync Server 2013 по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="dac85-108">Folder and file locations listed below are the default locations for Lync Server 2013.</span></span> <span data-ttu-id="dac85-109">Если в вашей организации какие-либо из этих объектов расположены в других местах, укажите соответствующие пути.</span><span class="sxs-lookup"><span data-stu-id="dac85-109">For any locations for which you did not use the default, exclude the locations you specified for your organization instead of the default locations specified in this topic.</span></span>



</div>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="dac85-110">Обратите внимание, что в некоторых антивирусных программах в списке исключений необходимо указывать абсолютные пути, а не относительные.</span><span class="sxs-lookup"><span data-stu-id="dac85-110">Please note that some antivirus programs may need absolute, not relative paths, for their exclusion list.</span></span>



</div>

  - <span data-ttu-id="dac85-111">Lync Server 2013 процессы:</span><span class="sxs-lookup"><span data-stu-id="dac85-111">Lync Server 2013 processes:</span></span>
    
      - <span data-ttu-id="dac85-112">ABServer.exe</span><span class="sxs-lookup"><span data-stu-id="dac85-112">ABServer.exe</span></span>
    
      - <span data-ttu-id="dac85-113">AcpMcuSvc.exe</span><span class="sxs-lookup"><span data-stu-id="dac85-113">AcpMcuSvc.exe</span></span>
    
      - <span data-ttu-id="dac85-114">ASMCUSvc.exe</span><span class="sxs-lookup"><span data-stu-id="dac85-114">ASMCUSvc.exe</span></span>
    
      - <span data-ttu-id="dac85-115">AVMCUSvc.exe</span><span class="sxs-lookup"><span data-stu-id="dac85-115">AVMCUSvc.exe</span></span>
    
      - <span data-ttu-id="dac85-116">ChannelService.exe</span><span class="sxs-lookup"><span data-stu-id="dac85-116">ChannelService.exe</span></span>
    
      - <span data-ttu-id="dac85-117">ClsAgent.exe</span><span class="sxs-lookup"><span data-stu-id="dac85-117">ClsAgent.exe</span></span>
    
      - <span data-ttu-id="dac85-118">ComplianceService.exe</span><span class="sxs-lookup"><span data-stu-id="dac85-118">ComplianceService.exe</span></span>
    
      - <span data-ttu-id="dac85-119">DataMCUSvc.exe</span><span class="sxs-lookup"><span data-stu-id="dac85-119">DataMCUSvc.exe</span></span>
    
      - <span data-ttu-id="dac85-120">DataProxy.exe</span><span class="sxs-lookup"><span data-stu-id="dac85-120">DataProxy.exe</span></span>
    
      - <span data-ttu-id="dac85-121">FileTransferAgent.exe</span><span class="sxs-lookup"><span data-stu-id="dac85-121">FileTransferAgent.exe</span></span>
    
      - <span data-ttu-id="dac85-122">IMMCUSvc.exe</span><span class="sxs-lookup"><span data-stu-id="dac85-122">IMMCUSvc.exe</span></span>
    
      - <span data-ttu-id="dac85-123">LysSvc.exe</span><span class="sxs-lookup"><span data-stu-id="dac85-123">LysSvc.exe</span></span>
    
      - <span data-ttu-id="dac85-124">MasterReplicatorAgent.exe</span><span class="sxs-lookup"><span data-stu-id="dac85-124">MasterReplicatorAgent.exe</span></span>
    
      - <span data-ttu-id="dac85-125">MediaRelaySvc.exe</span><span class="sxs-lookup"><span data-stu-id="dac85-125">MediaRelaySvc.exe</span></span>
    
      - <span data-ttu-id="dac85-126">MediationServerSvc.exe</span><span class="sxs-lookup"><span data-stu-id="dac85-126">MediationServerSvc.exe</span></span>
    
      - <span data-ttu-id="dac85-127">MRASSvc.exe</span><span class="sxs-lookup"><span data-stu-id="dac85-127">MRASSvc.exe</span></span>
    
      - <span data-ttu-id="dac85-128">OcsAppServerHost.exe</span><span class="sxs-lookup"><span data-stu-id="dac85-128">OcsAppServerHost.exe</span></span>
    
      - <span data-ttu-id="dac85-129">ReplicaReplicatorAgent.exe</span><span class="sxs-lookup"><span data-stu-id="dac85-129">ReplicaReplicatorAgent.exe</span></span>
    
      - <span data-ttu-id="dac85-130">ReplicationApp.exe</span><span class="sxs-lookup"><span data-stu-id="dac85-130">ReplicationApp.exe</span></span>
    
      - <span data-ttu-id="dac85-131">RtcHost.exe</span><span class="sxs-lookup"><span data-stu-id="dac85-131">RtcHost.exe</span></span>
    
      - <span data-ttu-id="dac85-132">RTCSrv.exe</span><span class="sxs-lookup"><span data-stu-id="dac85-132">RTCSrv.exe</span></span>
    
      - <span data-ttu-id="dac85-133">XmppProxy.exe</span><span class="sxs-lookup"><span data-stu-id="dac85-133">XmppProxy.exe</span></span>
    
      - <span data-ttu-id="dac85-134">XmppTGW.exe</span><span class="sxs-lookup"><span data-stu-id="dac85-134">XmppTGW.exe</span></span>

  - <span data-ttu-id="dac85-135">Процессы службы узла Windows Fabric</span><span class="sxs-lookup"><span data-stu-id="dac85-135">Windows Fabric Host Service processes:</span></span>
    
      - <span data-ttu-id="dac85-136">Fabric.exe</span><span class="sxs-lookup"><span data-stu-id="dac85-136">Fabric.exe</span></span>
    
      - <span data-ttu-id="dac85-137">FabricDCA.exe</span><span class="sxs-lookup"><span data-stu-id="dac85-137">FabricDCA.exe</span></span>
    
      - <span data-ttu-id="dac85-138">FabricHost.exe</span><span class="sxs-lookup"><span data-stu-id="dac85-138">FabricHost.exe</span></span>

  - <span data-ttu-id="dac85-139">Процессы IIS</span><span class="sxs-lookup"><span data-stu-id="dac85-139">IIS processes:</span></span>
    
      - <span data-ttu-id="dac85-140">% SystemRoot% \\ system32 \\ Inetsrv \\w3wp.exe</span><span class="sxs-lookup"><span data-stu-id="dac85-140">%systemroot%\\system32\\inetsrv\\w3wp.exe</span></span>
    
      - <span data-ttu-id="dac85-141">% SystemRoot% \\ SysWOW64 \\ Inetsrv \\w3wp.exe</span><span class="sxs-lookup"><span data-stu-id="dac85-141">%systemroot%\\SysWOW64\\inetsrv\\w3wp.exe</span></span>

  - <span data-ttu-id="dac85-142">Внутренние процессы сервера SQL Server</span><span class="sxs-lookup"><span data-stu-id="dac85-142">SQL Server Back-End processes:</span></span>
    
      - <span data-ttu-id="dac85-143">% ProgramFiles% \\ Microsoft SQL Server \\ MSSQL11. MSSQLSERVER \\ MSSQL \\ Binn \\SQLServr.exe</span><span class="sxs-lookup"><span data-stu-id="dac85-143">%ProgramFiles%\\Microsoft SQL Server\\MSSQL11.MSSQLSERVER\\MSSQL\\Binn\\SQLServr.exe</span></span>
    
      - <span data-ttu-id="dac85-144">% ProgramFiles% \\ Microsoft SQL Server \\ MSRS11. \\ \\ \\ReportingServicesService.exeной ЯЧЕЙКИ службы отчетов \\ MSSQLServer</span><span class="sxs-lookup"><span data-stu-id="dac85-144">%ProgramFiles%\\Microsoft SQL Server\\MSRS11.MSSQLSERVER\\Reporting Services\\ReportServer\\Bin\\ReportingServicesService.exe</span></span>
    
      - <span data-ttu-id="dac85-145">% ProgramFiles% \\ Microsoft SQL Server \\ MSAS11. \\ \\MSMDSrv.exe ЯЧЕЕК в MSSQLSERVER OLAP \\</span><span class="sxs-lookup"><span data-stu-id="dac85-145">%ProgramFiles%\\Microsoft SQL Server\\MSAS11.MSSQLSERVER\\OLAP\\Bin\\MSMDSrv.exe</span></span>

  - <span data-ttu-id="dac85-146">Внешние процессы сервера SQL Server</span><span class="sxs-lookup"><span data-stu-id="dac85-146">SQL Server Front-End processes:</span></span>
    
      - <span data-ttu-id="dac85-147">% ProgramFiles% \\ Microsoft SQL Server \\ MSSQL11. LYNCLOCAL \\ MSSQL \\ Binn \\SQLServr.exe</span><span class="sxs-lookup"><span data-stu-id="dac85-147">%ProgramFiles%\\Microsoft SQL Server\\MSSQL11.LYNCLOCAL\\MSSQL\\Binn\\SQLServr.exe</span></span>
    
      - <span data-ttu-id="dac85-148">% ProgramFiles% \\ Microsoft SQL Server \\ MSSQL11. RTCLOCAL \\ MSSQL \\ Binn \\SQLServr.exe</span><span class="sxs-lookup"><span data-stu-id="dac85-148">%ProgramFiles%\\Microsoft SQL Server\\MSSQL11.RTCLOCAL\\MSSQL\\Binn\\SQLServr.exe</span></span>

  - <span data-ttu-id="dac85-149">Каталоги и файлы</span><span class="sxs-lookup"><span data-stu-id="dac85-149">Directories and files:</span></span>
    
      - <span data-ttu-id="dac85-150">файлы журнала% systemroot% \\ system32 \\</span><span class="sxs-lookup"><span data-stu-id="dac85-150">%systemroot%\\System32\\LogFiles</span></span>
    
      - <span data-ttu-id="dac85-151">журналы% systemroot% \\ SysWOW64 \\</span><span class="sxs-lookup"><span data-stu-id="dac85-151">%systemroot%\\SysWow64\\LogFiles</span></span>
    
      - <span data-ttu-id="dac85-152">MSIL% systemroot% \\ Microsoft.NET \\ Assembly \\ GAC \_</span><span class="sxs-lookup"><span data-stu-id="dac85-152">%systemroot%\\Microsoft.NET\\assembly\\GAC\_MSIL</span></span>
    
      - <span data-ttu-id="dac85-153">% ProgramFiles% \\ Microsoft Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dac85-153">%programfiles%\\Microsoft Lync Server 2013</span></span>
    
      - <span data-ttu-id="dac85-154">% ProgramFiles% \\ Общие файлы, \\ \\ узел наблюдателя Microsoft Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dac85-154">%programfiles%\\Common Files\\Microsoft Lync Server 2013\\Watcher Node</span></span>
    
      - <span data-ttu-id="dac85-155">% ProgramFiles% \\ распространенных файлов в \\ Microsoft Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dac85-155">%programfiles%\\Common Files\\Microsoft Lync Server 2013</span></span>
    
      - <span data-ttu-id="dac85-156">% SystemDrive% \\ RtcReplicaRoot</span><span class="sxs-lookup"><span data-stu-id="dac85-156">%SystemDrive%\\RtcReplicaRoot</span></span>
    
      - <span data-ttu-id="dac85-157">Хранилище общих папок (указывается в построителе топологий).</span><span class="sxs-lookup"><span data-stu-id="dac85-157">File share store (specified in Topology Builder).</span></span> <span data-ttu-id="dac85-158">Хранилища файлов задаются в построителе топологий.</span><span class="sxs-lookup"><span data-stu-id="dac85-158">File stores are specified in Topology Builder.</span></span>
    
      - <span data-ttu-id="dac85-159">Файлы данных и журналов сервера SQL Server, включая объекты внутренней базы данных, хранилища пользователей, архивов, мониторинга и приложений.</span><span class="sxs-lookup"><span data-stu-id="dac85-159">SQL Server data and log files, including those for the back-end database, user store, archiving store, monitoring store, and application store.</span></span> <span data-ttu-id="dac85-160">Файлы баз данных и журналов можно указать в построителе топологий.</span><span class="sxs-lookup"><span data-stu-id="dac85-160">Database and log files can be specified in Topology Builder.</span></span> <span data-ttu-id="dac85-161">Дополнительные сведения о файлах данных и журналов для каждой базы данных, включая имена по умолчанию, можно найти в разделе [данные и расположение файлов журнала SQL Server для Lync Server 2013](lync-server-2013-sql-server-data-and-log-file-placement.md) в документации по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="dac85-161">For details about the data and log files for each database, including default names, see [SQL Server data and log file placement for Lync Server 2013](lync-server-2013-sql-server-data-and-log-file-placement.md) in the Deployment documentation.</span></span>
    
      - <span data-ttu-id="dac85-162">Файлы данных и журналов SQL Server, в том числе для интерфейсной базы данных, магазина Lync и RtcDatabase Store.</span><span class="sxs-lookup"><span data-stu-id="dac85-162">SQL Server data and log files, including those for the Front-end database, Lync store, and RtcDatabase store.</span></span> <span data-ttu-id="dac85-163">Обычно они находятся в рамках% localdrive% \\ CSData.</span><span class="sxs-lookup"><span data-stu-id="dac85-163">They are normally under %localdrive%\\CSData.</span></span>

<span data-ttu-id="dac85-164"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="dac85-164"></div>

<span> </span>

</div>

</div>

</span></span></div>

