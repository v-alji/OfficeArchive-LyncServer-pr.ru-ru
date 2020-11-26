---
title: 'Lync Server 2013: подготовка инфраструктуры и систем'
description: 'Lync Server 2013: подготовка инфраструктуры и систем.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Preparing the infrastructure and systems
ms:assetid: 1254ee38-0679-4714-b293-1050f107c158
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398205(v=OCS.15)
ms:contentKeyID: 48183458
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bfabdda9d117af1534578c8543f9ce72808d5a53
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424102"
---
# <a name="preparing-the-infrastructure-and-systems-for-lync-server-2013"></a><span data-ttu-id="f2ec6-103">Подготовка инфраструктуры и систем для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f2ec6-103">Preparing the infrastructure and systems for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f2ec6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f2ec6-104">

<span> </span></span></span>

<span data-ttu-id="f2ec6-105">_**Тема последнего изменения:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="f2ec6-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="f2ec6-106">Для развертывания Lync Server 2013 требуется использование построителя топологии для определения и публикации структуры топологии.</span><span class="sxs-lookup"><span data-stu-id="f2ec6-106">Deployment of Lync Server 2013 requires the use of Topology Builder to define and publish the topology design.</span></span> <span data-ttu-id="f2ec6-107">Чтобы определить компоненты, необходимые для вашей топологии, вы используете Topology Builder для создания и сохранения структуры топологии.</span><span class="sxs-lookup"><span data-stu-id="f2ec6-107">To identify the components required for your topology, you use Topology Builder to create and save a topology design.</span></span> <span data-ttu-id="f2ec6-108">Прежде чем публиковать топологию в построителе топологии, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="f2ec6-108">Prior to publishing your topology in Topology Builder, you do the following:</span></span>

  - <span data-ttu-id="f2ec6-109">Загружайте и устанавливайте оборудование для каждого компонента в структуре топологии, которая была создана и сохранена с помощью построителя топологии, включая все необходимые компьютеры (серверы с Lync Server 2013, серверы баз данных, серверы служб IIS и обратные прокси-серверы), сетевые адаптеры, подсистемы балансировки нагрузки оборудования и запоминающие устройства (например, файловые серверы).</span><span class="sxs-lookup"><span data-stu-id="f2ec6-109">Acquire and install the hardware for each component in the topology design that you created and saved by using Topology Builder, including all required computers (servers running Lync Server 2013, database servers, servers running Internet Information Services (IIS), and reverse proxy servers, as appropriate), network adapters, hardware load balancers, and storage devices (such as file servers).</span></span> <span data-ttu-id="f2ec6-110">Подробные сведения о том, как определить топологию, указывающую компоненты, необходимые для вашего развертывания, приведены [в разделе Определение и Настройка топологии в Lync Server 2013](lync-server-2013-defining-and-configuring-the-topology.md).</span><span class="sxs-lookup"><span data-stu-id="f2ec6-110">For details about how to define a topology that specifies the components needed for your deployment, see [Defining and configuring the topology in Lync Server 2013](lync-server-2013-defining-and-configuring-the-topology.md).</span></span> <span data-ttu-id="f2ec6-111">Дополнительные сведения о требованиях к оборудованию для серверов можно найти в документации о поддержке [оборудования для Lync Server 2013](lync-server-2013-supported-hardware.md) .</span><span class="sxs-lookup"><span data-stu-id="f2ec6-111">For details about hardware requirements for servers, see [Supported hardware for Lync Server 2013](lync-server-2013-supported-hardware.md) in the Supportability documentation.</span></span>

  - <span data-ttu-id="f2ec6-112">Убедитесь, что сетевая инфраструктура соответствует требованиям.</span><span class="sxs-lookup"><span data-stu-id="f2ec6-112">Make sure that the networking infrastructure meets requirements.</span></span> <span data-ttu-id="f2ec6-113">Подробности можно найти в разделе [требования к сетевой инфраструктуре для Lync Server 2013](lync-server-2013-network-infrastructure-requirements.md) в документации по планированию.</span><span class="sxs-lookup"><span data-stu-id="f2ec6-113">For details, see [Network infrastructure requirements for Lync Server 2013](lync-server-2013-network-infrastructure-requirements.md) in the Planning documentation.</span></span>

  - <span data-ttu-id="f2ec6-114">Настройте доменные службы Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f2ec6-114">Set up Active Directory Domain Services.</span></span> <span data-ttu-id="f2ec6-115">Для публикации и включения топологии необходимы внутренние серверы, которые должны быть представлены учетными записями компьютеров в доменных СЛУЖБах Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f2ec6-115">To publish and enable the topology, you need the internal servers to be represented by computer accounts in AD DS.</span></span> <span data-ttu-id="f2ec6-116">Это можно сделать, присоединяя компьютеры к доменной службе Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f2ec6-116">This is accomplished by joining the computers to AD DS.</span></span> <span data-ttu-id="f2ec6-117">Дополнительные сведения о подготовке доменных служб Active Directory можно найти в статьях [Подготовка службы AD DS для Lync Server 2013](lync-server-2013-preparing-active-directory-domain-services.md).</span><span class="sxs-lookup"><span data-stu-id="f2ec6-117">For details about preparing AD DS, see [Preparing Active Directory Domain Services for Lync Server 2013](lync-server-2013-preparing-active-directory-domain-services.md).</span></span>

  - <span data-ttu-id="f2ec6-118">Создайте файловый общий доступ.</span><span class="sxs-lookup"><span data-stu-id="f2ec6-118">Create a file share.</span></span> <span data-ttu-id="f2ec6-119">Сервер стандартных выпусков может размещать общую файловую систему для нужного файла, в корпоративной среде общий доступ к файлам не может размещаться на сервере переднего плана.</span><span class="sxs-lookup"><span data-stu-id="f2ec6-119">Standard Edition servers can host the file share for the required file, while in an Enterprise deployment the file share cannot be hosted on the front end server.</span></span> <span data-ttu-id="f2ec6-120">Разрешения и членство в группах, необходимые для развертывания и настройки списка управления доступом (ACL) в папке, и общий доступ должны быть правильно заданы для успешного завершения построителя топологии.</span><span class="sxs-lookup"><span data-stu-id="f2ec6-120">The permissions and group memberships required for deploying and setting the access control list (ACL) on the folder and the share must be set correctly for Topology Builder to complete successfully.</span></span> <span data-ttu-id="f2ec6-121">Необходимо убедиться в том, что у пользователя, выполняющего Topology Builder, есть следующие разрешения и членство в группах.</span><span class="sxs-lookup"><span data-stu-id="f2ec6-121">You should make sure that the person running Topology Builder has the following permissions and group memberships:</span></span>
    
      - <span data-ttu-id="f2ec6-122">Член локальных администраторов</span><span class="sxs-lookup"><span data-stu-id="f2ec6-122">Member of Local Administrators</span></span>
    
      - <span data-ttu-id="f2ec6-123">Член группы пользователей домена</span><span class="sxs-lookup"><span data-stu-id="f2ec6-123">Member of Domain Users</span></span>
    
      - <span data-ttu-id="f2ec6-124">Полный контроль над папкой "общий доступ" и "папка" в хранилище файлов</span><span class="sxs-lookup"><span data-stu-id="f2ec6-124">Full Control on share and folder of file store</span></span>

  - <span data-ttu-id="f2ec6-125">Для выпуска Enterprise Edition установите и настройте SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f2ec6-125">For Enterprise Edition, install and configure SQL Server.</span></span> <span data-ttu-id="f2ec6-126">Для успешного завершения установки SQL Server необходимо, чтобы сервер SQL Server был подключен к сети, а пользователь, публикующий топологию, был локальным администратором SQL Server и должен быть членом группы sysadmin SQL Server в экземпляре SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f2ec6-126">For SQL Server setup to succeed the SQL Server-based server must be online and the person publishing the topology be a local admin on the SQL Server and must be a member of the SQL Server sysadmin group on the SQL Server instance.</span></span>

<span data-ttu-id="f2ec6-127">После выполнения всех задач подготовки, описанных в этой статье, но прежде чем публиковать топологию, вам также потребуется выполнить другие задачи подготовки, в том числе установка операционной системы Windows и другого необходимого программного обеспечения, Настройка служб IIS и настройка DNS.</span><span class="sxs-lookup"><span data-stu-id="f2ec6-127">After you complete all of the preparation tasks as described in this topic, but prior to publishing the topology, you also need to perform the other preparation tasks, including installing the Windows operating systems and other prerequisite software, setting up IIS, and configuring DNS.</span></span> <span data-ttu-id="f2ec6-128">Подробнее об этих задачах можно узнать в разделе [требования к системе для серверов с Lync server 2013](lync-server-2013-system-requirements-for-servers-running-lync-server-2013.md), [Настройка служб IIS для Lync Server 2013](lync-server-2013-configure-iis.md)и [Подготовка инфраструктуры и систем для Lync Server 2013](lync-server-2013-preparing-the-infrastructure-and-systems.md).</span><span class="sxs-lookup"><span data-stu-id="f2ec6-128">For details about these tasks, see [System requirements for servers running Lync Server 2013](lync-server-2013-system-requirements-for-servers-running-lync-server-2013.md), [Configure IIS for Lync Server 2013](lync-server-2013-configure-iis.md), and [Preparing the infrastructure and systems for Lync Server 2013](lync-server-2013-preparing-the-infrastructure-and-systems.md).</span></span> <span data-ttu-id="f2ec6-129">Кроме того, вы должны ознакомиться с требованиями клиентов и клиентов.</span><span class="sxs-lookup"><span data-stu-id="f2ec6-129">Additionally, you should familiarize yourself with the clients and client requirements.</span></span> <span data-ttu-id="f2ec6-130">Подробные сведения можно найти [в разделе Развертывание клиентов и устройств в Lync Server 2013](lync-server-2013-deploying-clients-and-devices.md).</span><span class="sxs-lookup"><span data-stu-id="f2ec6-130">For details, see [Deploying clients and devices in Lync Server 2013](lync-server-2013-deploying-clients-and-devices.md).</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="f2ec6-131">Содержание</span><span class="sxs-lookup"><span data-stu-id="f2ec6-131">In This Section</span></span>

  - [<span data-ttu-id="f2ec6-132">Настройка оборудования для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f2ec6-132">Hardware setup for Lync Server 2013</span></span>](lync-server-2013-hardware-setup.md)

  - [<span data-ttu-id="f2ec6-133">Установка программного обеспечения для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f2ec6-133">Software setup for Lync Server 2013</span></span>](lync-server-2013-software-setup.md)

  - [<span data-ttu-id="f2ec6-134">Подготовка доменных служб Active Directory для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f2ec6-134">Preparing Active Directory Domain Services for Lync Server 2013</span></span>](lync-server-2013-preparing-active-directory-domain-services.md)

  - [<span data-ttu-id="f2ec6-135">Настройка SQL Server для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f2ec6-135">Configure SQL Server for Lync Server 2013</span></span>](lync-server-2013-configure-sql-server-for-lync-server.md)

  - [<span data-ttu-id="f2ec6-136">Настройка DNS-записей в Lync Server 2013 для пула переднего плана или сервера Standard Edition</span><span class="sxs-lookup"><span data-stu-id="f2ec6-136">Configure DNS records in Lync Server 2013 for a Front End pool or Standard Edition server</span></span>](lync-server-2013-configure-dns-records-for-a-front-end-pool-or-standard-edition-server.md)

  - [<span data-ttu-id="f2ec6-137">Установка средств администрирования Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f2ec6-137">Install Lync Server 2013 administrative tools</span></span>](lync-server-2013-install-lync-server-administrative-tools.md)

<span data-ttu-id="f2ec6-138"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f2ec6-138"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

