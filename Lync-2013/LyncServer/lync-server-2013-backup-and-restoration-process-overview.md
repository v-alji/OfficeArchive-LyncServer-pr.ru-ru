---
title: 'Lync Server 2013: Общие сведения о процессе резервного копирования и восстановления'
description: 'Lync Server 2013: Общие сведения о процессе резервного копирования и восстановления.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Backup and restoration process overview
ms:assetid: e0f23b21-070f-4df5-b795-cea2f5338d85
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202192(v=OCS.15)
ms:contentKeyID: 51541524
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 77b833a05021d3a848e9de1ee8768f7daa194c6a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437996"
---
# <a name="backup-and-restoration-process-overview-for-lync-server-2013"></a><span data-ttu-id="503cb-103">Обзор процесса резервного копирования и восстановления для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="503cb-103">Backup and restoration process overview for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="503cb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="503cb-104">

<span> </span></span></span>

<span data-ttu-id="503cb-105">_**Тема последнего изменения:** 2013-03-26_</span><span class="sxs-lookup"><span data-stu-id="503cb-105">_**Topic Last Modified:** 2013-03-26_</span></span>

<span data-ttu-id="503cb-106">В этом разделе приводятся общие сведения о том, как выполняется резервное копирование и восстановление для Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="503cb-106">This section provides an overview of how the backup and restoration process works for Lync Server 2013.</span></span> <span data-ttu-id="503cb-107">Вы используете один и тот же процесс для всех серверов стандартных выпусков и серверов выпуска Enterprise Edition, независимо от того, где они находятся.</span><span class="sxs-lookup"><span data-stu-id="503cb-107">You use the same process for all Standard Edition servers and Enterprise Edition servers, regardless of their location.</span></span>

<span data-ttu-id="503cb-108">Как правило, процесс резервного копирования выполняется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="503cb-108">In general, the backup process works as follows:</span></span>

  - <span data-ttu-id="503cb-109">Расположение резервной копии создается как общая папка на отдельном компьютере, который не входит ни в один пул.</span><span class="sxs-lookup"><span data-stu-id="503cb-109">You create a backup location as a shared folder on a stand-alone computer that is not part of any pool.</span></span> <span data-ttu-id="503cb-110">Ссылка на расположение резервной копии содержится в **$BACKUP**.</span><span class="sxs-lookup"><span data-stu-id="503cb-110">The location of the backup is referenced in **$Backup**.</span></span>

  - <span data-ttu-id="503cb-111">Регулярное создание резервных копий всех баз данных Lync Server и всех хранилищ файлов, описанных в статье [требования к резервному копированию и восстановлению в Lync server 2013: данные](lync-server-2013-backup-and-restoration-requirements-data.md) , выполнив действия, описанные в статье [Создание резервной копии Lync Server 2013](lync-server-2013-backing-up-lync-server.md) . Центральное хранилище содержит все параметры и конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="503cb-111">On a regular, scheduled basis, you back up all the Lync Server databases and all the file stores that are described in [Backup and restoration requirements in Lync Server 2013: data](lync-server-2013-backup-and-restoration-requirements-data.md) by following the procedures described in [Backing up Lync Server 2013](lync-server-2013-backing-up-lync-server.md) The Central Management store includes all the server settings and configurations.</span></span>

  - <span data-ttu-id="503cb-112">Каждый раз, когда вы запускаете последующую архивацию, вы создаете новую общую папку и изменяете путь, который **$BACKUP** ссылок.</span><span class="sxs-lookup"><span data-stu-id="503cb-112">Each time you run a subsequent backup, you create a new shared folder and change the path that **$Backup** references.</span></span>

<span data-ttu-id="503cb-113">Как правило, процесс восстановления выполняется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="503cb-113">In general, the restoration process works as follows:</span></span>

  - <span data-ttu-id="503cb-114">При возникновении ошибки или сбоя вы восстанавливаете данные в расположении, на которое ссылается **$BACKUP** , на новые или чистые компьютеры.</span><span class="sxs-lookup"><span data-stu-id="503cb-114">When a failure or outage occurs, you restore the data in the location referenced by **$Backup** to new or clean computers.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="503cb-115">Этот процесс восстановления не восстанавливает данные на существующем состоянии сервера.</span><span class="sxs-lookup"><span data-stu-id="503cb-115">This restoration process does not restore data onto an existing server state.</span></span> <span data-ttu-id="503cb-116">Это значит, что для этого процесса требуется, чтобы сервер был чистым или новым.</span><span class="sxs-lookup"><span data-stu-id="503cb-116">That is, this process requires that the server is clean or new.</span></span>

    
    </div>

  - <span data-ttu-id="503cb-117">Чтобы обеспечить возможность восстановления сведений о пользователях и конференциях в точке сбоя, вы можете реализовать топологию аварийной проверки с помощью связанных пулов переднего плана, как описано в разделе [Планирование обеспечения высокой доступности и аварийного восстановления в Lync Server 2013](lync-server-2013-planning-for-high-availability-and-disaster-recovery.md).</span><span class="sxs-lookup"><span data-stu-id="503cb-117">To enable your user and conference information to be recoverable to the point of failure, you can implement a disaster recovery topology with paired Front End pools, as described in [Planning for high availability and disaster recovery in Lync Server 2013](lync-server-2013-planning-for-high-availability-and-disaster-recovery.md).</span></span>

  - <span data-ttu-id="503cb-118">Все конфигурации системы доменных имен (DNS), конфигурации протокола DHCP (Dynamic Host Configuration Protocol), доменные имена, полные доменные имена (FQDN), пути к файлам и т. п. должны быть одинаковыми во время резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="503cb-118">All Domain Name System (DNS) configuration, Dynamic Host Configuration Protocol (DHCP) configuration, domain names, computer fully qualified domain names (FQDNs), file store paths, and so on must be the same at the time of restoration that they were at the time of back up.</span></span>

<span data-ttu-id="503cb-119">Если сервер, на котором работает Lync Server, не проходит, восстановление включает в себя следующие шаги:</span><span class="sxs-lookup"><span data-stu-id="503cb-119">If a server running Lync Server fails, recovery includes the following steps:</span></span>

  - <span data-ttu-id="503cb-120">Установите операционную систему на новом компьютере или удалите его с полным доменным именем, совпадающим с неисправной компьютером.</span><span class="sxs-lookup"><span data-stu-id="503cb-120">Install the operating system on a new or clean computer with the same FQDN as the failed computer.</span></span>

  - <span data-ttu-id="503cb-121">Переустановите сертификаты.</span><span class="sxs-lookup"><span data-stu-id="503cb-121">Reinstall certificates.</span></span>

  - <span data-ttu-id="503cb-122">Если сервер размещается в базе данных, установите Microsoft SQL Server 2012 или Microsoft SQL Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="503cb-122">If the server hosted a database, install Microsoft SQL Server 2012 or Microsoft SQL Server 2008 R2.</span></span>

  - <span data-ttu-id="503cb-123">Как правило, если сервер размещает базу данных, запустите Topology Builder, чтобы создать и установить базу данных и настроить списки управления доступом (ACL).</span><span class="sxs-lookup"><span data-stu-id="503cb-123">In general, if the server hosted a database, run Topology Builder to create and install the database and set up access control lists (ACLs).</span></span>

  - <span data-ttu-id="503cb-124">В общем случае сервер, на котором размещена роль сервера, выполните шаг 1 до шага 4 мастера развертывания Lync Server для установки локальных файлов конфигурации, установки компонентов роли сервера, назначения сертификатов и запуска служб.</span><span class="sxs-lookup"><span data-stu-id="503cb-124">In general, if the server hosted a server role, run step 1 through step 4 of the Lync Server Deployment Wizard to install the local configuration files, install the server role components, assign certificates, and start the services.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="503cb-125">Если сервер размещает базу данных, сопоставленную с ролью сервера, при выполнении шага 2 мастера развертывания Lync Server повторно создается база данных.</span><span class="sxs-lookup"><span data-stu-id="503cb-125">If the server hosted a database collocated with the server role, running step 2 of the Lync Server Deployment Wizard recreates the database.</span></span>

    
    </div>

  - <span data-ttu-id="503cb-126">Если сервер размещает базу данных, Восстановите резервные копии данных.</span><span class="sxs-lookup"><span data-stu-id="503cb-126">If the server hosted a database, restore the backed up data.</span></span>

<span data-ttu-id="503cb-127"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="503cb-127"></div>

<span> </span>

</div>

</div>

</span></span></div>

