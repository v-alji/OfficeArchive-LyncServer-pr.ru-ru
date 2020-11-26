---
title: 'Lync Server 2013: настройка оборудования'
description: 'Lync Server 2013: Настройка оборудования.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Hardware setup
ms:assetid: 37a9f295-cde3-4beb-9a6a-2580082798ab
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425852(v=OCS.15)
ms:contentKeyID: 48183834
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4e798ce32c1f89bba40ad9245426492b0489e7b4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427693"
---
# <a name="hardware-setup-for-lync-server-2013"></a><span data-ttu-id="3451d-103">Настройка оборудования для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3451d-103">Hardware setup for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3451d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3451d-104">

<span> </span></span></span>

<span data-ttu-id="3451d-105">_**Тема последнего изменения:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="3451d-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="3451d-106">Настройка оборудования и других компонентов, необходимых для реализации топологии, необходимо, прежде чем публиковать топологию в построителе топологии, вы можете сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="3451d-106">Setting up the hardware and other components required in the infrastructure that you need to implement your topology requires that, prior to publishing your topology in Topology Builder, you do the following:</span></span>

  - <span data-ttu-id="3451d-107">Установите оборудование для каждого компонента в структуре топологии, которая была создана и сохранена с помощью построителя топологии, включая все необходимые компьютеры (серверы с Lync Server 2013, серверы баз данных, серверы служб IIS и обратные прокси-серверы), сетевые адаптеры, подсистемы балансировки нагрузки оборудования и запоминающие устройства (например, файловые серверы).</span><span class="sxs-lookup"><span data-stu-id="3451d-107">Install the hardware for each component in the topology design that you created and saved by using Topology Builder, including all required computers (servers running Lync Server 2013, database servers, servers running Internet Information Services (IIS), and reverse proxy servers, as appropriate), network adapters, hardware load balancers, and storage devices (such as file servers).</span></span> <span data-ttu-id="3451d-108">Убедитесь, что вы проследовали рекомендации для номера и скорости для сетевых адаптеров.</span><span class="sxs-lookup"><span data-stu-id="3451d-108">Confirm that you have followed the recommendations for the number and speed for network adapters.</span></span> <span data-ttu-id="3451d-109">Если вы будете использовать подсистемы балансировки нагрузки для оборудования, убедитесь, что у вас есть правильная информация от поставщика, чтобы настроить их для использования с Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3451d-109">If you will be using hardware load balancers, make sure that you have the proper information from the vendor to configure them for use with Lync Server 2013.</span></span> <span data-ttu-id="3451d-110">Если вы будете использовать файловый сервер или другой сервер для размещения общего файлового файла, необходимого для Lync Server, убедитесь, что сервер доступен и готов к настройке общего файлового доступа.</span><span class="sxs-lookup"><span data-stu-id="3451d-110">If you will be using a file server or other server to house the file share required by Lync Server, make sure that the server is available and ready for the configuration of the file share.</span></span> <span data-ttu-id="3451d-111">Подробные сведения о том, как определить топологию, указывающую компоненты, необходимые для вашего развертывания, приведены [в разделе Определение и Настройка топологии в Lync Server 2013](lync-server-2013-defining-and-configuring-the-topology.md).</span><span class="sxs-lookup"><span data-stu-id="3451d-111">For details about how to define a topology that specifies the components needed for your deployment, see [Defining and configuring the topology in Lync Server 2013](lync-server-2013-defining-and-configuring-the-topology.md).</span></span> <span data-ttu-id="3451d-112">Дополнительные сведения о требованиях к оборудованию для серверов можно найти в документации о поддержке [оборудования для Lync Server 2013](lync-server-2013-supported-hardware.md) .</span><span class="sxs-lookup"><span data-stu-id="3451d-112">For details about hardware requirements for servers, see [Supported hardware for Lync Server 2013](lync-server-2013-supported-hardware.md) in the Supportability documentation.</span></span>

  - <span data-ttu-id="3451d-113">Убедитесь, что сетевая инфраструктура соответствует требованиям.</span><span class="sxs-lookup"><span data-stu-id="3451d-113">Make sure that the networking infrastructure meets requirements.</span></span> <span data-ttu-id="3451d-114">Подробности можно найти в разделе [требования к сетевой инфраструктуре для Lync Server 2013](lync-server-2013-network-infrastructure-requirements.md) в документации по планированию.</span><span class="sxs-lookup"><span data-stu-id="3451d-114">For details, see [Network infrastructure requirements for Lync Server 2013](lync-server-2013-network-infrastructure-requirements.md) in the Planning documentation.</span></span>

  - <span data-ttu-id="3451d-115">Настройте доменные службы Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3451d-115">Set up Active Directory Domain Services.</span></span> <span data-ttu-id="3451d-116">Настройка AD DS включает подготовку AD DS и определение всех компонентов, которые требуется развернуть в AD DS.</span><span class="sxs-lookup"><span data-stu-id="3451d-116">Setting up AD DS includes preparing AD DS and defining all components that you want to deploy in AD DS.</span></span> <span data-ttu-id="3451d-117">Дополнительные сведения о подготовке доменных служб Active Directory можно найти в документации по развертыванию службы AD DS [для Lync Server 2013](lync-server-2013-preparing-active-directory-domain-services.md) .</span><span class="sxs-lookup"><span data-stu-id="3451d-117">For details about preparing AD DS, see [Preparing Active Directory Domain Services for Lync Server 2013](lync-server-2013-preparing-active-directory-domain-services.md) in the Deployment documentation.</span></span>

  - <span data-ttu-id="3451d-118">Настройте необходимые разрешения для создания общего файлового файла.</span><span class="sxs-lookup"><span data-stu-id="3451d-118">Set up the required permissions for creating the file share.</span></span> <span data-ttu-id="3451d-119">Разрешения на использование файловых ресурсов Lync Server 2013 автоматически настраиваются построителем топологии при публикации топологии.</span><span class="sxs-lookup"><span data-stu-id="3451d-119">Permissions for use of file shares by Lync Server 2013 are automatically configured by Topology Builder when you publish your topology.</span></span> <span data-ttu-id="3451d-120">Тем не менее, учетная запись пользователя, используемая для публикации топологии, должна иметь полный контроль (чтение/запись и изменение) в общей папке, чтобы построитель топологии настроил необходимые разрешения.</span><span class="sxs-lookup"><span data-stu-id="3451d-120">However, the user account used to publish the topology must have full control (read/write/modify) on the file share in order for Topology Builder to configure the required permissions.</span></span> <span data-ttu-id="3451d-121">Чтобы обеспечить правильную работу общего файлового файла во время публикации построителя топологии, пользователь или группа домена, участником которой является пользователь, должны быть членами локальной группы администраторов на компьютере, на котором находится файловый общий доступ.</span><span class="sxs-lookup"><span data-stu-id="3451d-121">To make sure that the file share can be managed properly during the Topology Builder publishing process, the user or domain group that the user is a member of should be made a member of the local Administrators group on the machine where the file share is located.</span></span> <span data-ttu-id="3451d-122">В сценарии с несколькими доменами пользователь или группа должны быть членами локальной группы администраторов на компьютере в домене B, где будет находиться файловый общий доступ.</span><span class="sxs-lookup"><span data-stu-id="3451d-122">In a multi-domain scenario, Domain A user or group should be made a member of the local Administrators group on the machine in Domain B where the file share will be located.</span></span>
    
    <span data-ttu-id="3451d-123">Дополнительные сведения об обновлении с помощью общих папок в распределенной файловой системе (DFS) можно найти в разделе [Настройка хранилища файлов для Lync Server 2013](lync-server-2013-configure-dfs-file-storage.md).</span><span class="sxs-lookup"><span data-stu-id="3451d-123">For details about updating using file shares in a Distributed File System (DFS), see [Configure file storage for Lync Server 2013](lync-server-2013-configure-dfs-file-storage.md).</span></span>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="3451d-124">Не удается найти общую файловую систему для Lync Server 2013, Enterprise Edition на сервере переднего плана.</span><span class="sxs-lookup"><span data-stu-id="3451d-124">The file share for Lync Server 2013, Enterprise Edition cannot be located on the Front End Server.</span></span>

    
    </div>

  - <span data-ttu-id="3451d-125">Установка и Настройка аппаратной подсистемы балансировки нагрузки для веб-служб.</span><span class="sxs-lookup"><span data-stu-id="3451d-125">Install and set up the hardware load balancer for Web Services.</span></span> <span data-ttu-id="3451d-126">При развернутой службе доменных имен (DNS) для этих пулов также необходимо использовать балансировку нагрузки для оборудования, но только для трафика HTTP/HTTPS.</span><span class="sxs-lookup"><span data-stu-id="3451d-126">With Domain Name System (DNS) load balancing deployed, you still need to also use hardware load balancers for these pools, but only for HTTP/HTTPS traffic.</span></span> <span data-ttu-id="3451d-127">Подсистема балансировки нагрузки аппаратных средств используется для трафика HTTPS от клиентов через порты 443 и 80.</span><span class="sxs-lookup"><span data-stu-id="3451d-127">The hardware load balancer is used for HTTPS traffic from clients over ports 443 and 80.</span></span> <span data-ttu-id="3451d-128">Несмотря на то, что для этих пулов по-прежнему нужны подсистемы балансировки нагрузки, их настройка и администрирование будут главным образом для трафика HTTP/HTTPS, с которым связаны администраторы подсистемы балансировки нагрузки для оборудования.</span><span class="sxs-lookup"><span data-stu-id="3451d-128">Although you still need hardware load balancers for these pools, their setup and administration will be primarily for HTTP/HTTPS traffic, which the administrators of the hardware load balancers are accustomed to.</span></span>

<span data-ttu-id="3451d-129">После выполнения всех задач подготовки, описанных в этой статье, но перед публикацией топологии, вам также потребуется выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="3451d-129">After you complete all of the preparation tasks as described in this topic, but prior to publishing the topology, you also need to:</span></span>

  - [<span data-ttu-id="3451d-130">Установка операционных систем и необходимого программного обеспечения на серверы для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3451d-130">Install operating systems and prerequisite software on servers for Lync Server 2013</span></span>](lync-server-2013-install-operating-systems-and-prerequisite-software-on-servers.md)

  - [<span data-ttu-id="3451d-131">Настройка IIS для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3451d-131">Configure IIS for Lync Server 2013</span></span>](lync-server-2013-configure-iis.md)

  - [<span data-ttu-id="3451d-132">Настройка SQL Server для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3451d-132">Configure SQL Server for Lync Server 2013</span></span>](lync-server-2013-configure-sql-server-for-lync-server.md)

  - [<span data-ttu-id="3451d-133">Настройка DNS-записей в Lync Server 2013 для пула переднего плана или сервера Standard Edition</span><span class="sxs-lookup"><span data-stu-id="3451d-133">Configure DNS records in Lync Server 2013 for a Front End pool or Standard Edition server</span></span>](lync-server-2013-configure-dns-records-for-a-front-end-pool-or-standard-edition-server.md)

<span data-ttu-id="3451d-134"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3451d-134"></div>

<span> </span>

</div>

</div>

</span></span></div>

