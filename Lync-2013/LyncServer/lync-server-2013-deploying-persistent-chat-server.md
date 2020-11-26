---
title: 'Lync Server 2013: развертывание сервера сохраняемого чата'
description: 'Lync Server 2013: развертывание сервера сохраняемого чата.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying Persistent Chat Server
ms:assetid: e3b930fb-6855-47f0-b6b3-7dfae386540d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205357(v=OCS.15)
ms:contentKeyID: 48185717
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b85c0070ab4bcd60d80d57738c25daac1de4faf1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429813"
---
# <a name="deploying-persistent-chat-server-in-lync-server-2013"></a><span data-ttu-id="20968-103">Развертывание сервера сохраняемого чата в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="20968-103">Deploying Persistent Chat Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="20968-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="20968-104">

<span> </span></span></span>

<span data-ttu-id="20968-105">_**Тема последнего изменения:** 2014-03-31_</span><span class="sxs-lookup"><span data-stu-id="20968-105">_**Topic Last Modified:** 2014-03-31_</span></span>

<span data-ttu-id="20968-106">Lync Server 2013, сервер сохраняемого чата входит в состав инфраструктуры Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="20968-106">Lync Server 2013, Persistent Chat Server is part of the Lync Server 2013 infrastructure.</span></span>

<span data-ttu-id="20968-107">Для развертывания сохраняемого сервера чата необходимо:</span><span class="sxs-lookup"><span data-stu-id="20968-107">Deploying Persistent Chat Server requires that you:</span></span>

  - <span data-ttu-id="20968-108">С помощью Topology Builder вы можете определить (или импортировать) и затем опубликовать свою топологию и компоненты, которые вы хотите развернуть.</span><span class="sxs-lookup"><span data-stu-id="20968-108">Use Topology Builder to define, or import, and subsequently publish your topology and the components that you want to deploy.</span></span>

  - <span data-ttu-id="20968-109">Подготовка среды для развертывания постоянных серверных компонентов чата.</span><span class="sxs-lookup"><span data-stu-id="20968-109">Prepare your environment for deploying Persistent Chat Server components.</span></span>

  - <span data-ttu-id="20968-110">Установите и настройте компоненты сервера сохраняемого чата для развертывания.</span><span class="sxs-lookup"><span data-stu-id="20968-110">Install and configure Persistent Chat Server components for your deployment.</span></span>

<span data-ttu-id="20968-111">Сервер для Lync Server 2013 Enterprise Edition доступен в виде отдельного пула (не размещается вместе с серверами переднего плана Enterprise Edition).</span><span class="sxs-lookup"><span data-stu-id="20968-111">Persistent Chat Server is available with Lync Server 2013 Enterprise Edition as a separate pool (not collocated with the Enterprise Edition Front End Servers).</span></span> <span data-ttu-id="20968-112">Для хранения содержимого комнаты чата и других нужных метаданных сервер для работы с сохраняемым чат требуется сервер SQL Server из пула Enterprise Edition.</span><span class="sxs-lookup"><span data-stu-id="20968-112">Persistent Chat Server requires a SQL Server Back End Server in your Enterprise Edition pool to store the chat room content and other relevant metadata.</span></span> <span data-ttu-id="20968-113">Мы рекомендуем установить **PersistentChatStore** на выделенный сервер SQL Server, несмотря на то, что размещение сервера Lync Server 2013 и **PersistentChatStore** на одном и том же экземпляре SQL Server поддерживается.</span><span class="sxs-lookup"><span data-stu-id="20968-113">We recommend that you install the **PersistentChatStore** on a dedicated SQL Server Back End Server, although collocating Lync Server 2013 Back End Server and **PersistentChatStore** on the same SQL Server instance is supported.</span></span>

<span data-ttu-id="20968-114">Кроме того, с помощью Lync Server 2013 Standard Edition можно развернуть сервер сохраняемого чата.</span><span class="sxs-lookup"><span data-stu-id="20968-114">Persistent Chat Server can also be deployed with Lync Server 2013 Standard Edition.</span></span> <span data-ttu-id="20968-115">В этом случае сервер переднего плана **PersistentChatService** размещается на компьютере Standard Edition, а сервер **PersistentChatStore** Server можно развернуть на локальном экземпляре SQL Server Express.</span><span class="sxs-lookup"><span data-stu-id="20968-115">In this case, the **PersistentChatService** Front End Server is collocated on the Standard Edition computer, and the **PersistentChatStore** Back End Server can be deployed on the local SQL Server Express instance.</span></span>

<span data-ttu-id="20968-116">Подробные сведения о поддерживаемых конфигурациях сорасположений можно найти в разделе Поддерживаемые параметры совместного расположения [серверов в Lync server 2013](lync-server-2013-supported-server-collocation.md).</span><span class="sxs-lookup"><span data-stu-id="20968-116">For details about supported colocation configurations, see [Supported server collocation in Lync Server 2013](lync-server-2013-supported-server-collocation.md).</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="20968-117">Мы не поддерживаем высокий уровень доступности сохраняемого сервера для работы с &nbsp; версией Standard Chat.</span><span class="sxs-lookup"><span data-stu-id="20968-117">We do not support high availability for Persistent Chat Server&nbsp;Standard Edition.</span></span> <span data-ttu-id="20968-118">Производительность и масштаб будут ограничены.</span><span class="sxs-lookup"><span data-stu-id="20968-118">Performance and scale will be limited.</span></span> <span data-ttu-id="20968-119">Кроме того, мы поддерживаем только новый сервер стандартный выпуск для версии для постоянного чата &nbsp; .</span><span class="sxs-lookup"><span data-stu-id="20968-119">Furthermore, we support only new Persistent Chat Server&nbsp;Standard Edition server.</span></span> <span data-ttu-id="20968-120">Мы не поддерживаем обновление Lync Server 2010, групповой чат с сервером для Lync Server 2013 для &nbsp; обычного чата Server &nbsp; Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="20968-120">We do not support upgrading Lync Server 2010, Group Chat Server to a Lync Server 2013&nbsp;Persistent Chat Server&nbsp;Standard Edition.</span></span>



</div>

<span data-ttu-id="20968-121">Если в вашей организации требуется поддержка соответствия требованиям, вы можете установить службу соответствия требованиям сервера для разговора на сервер переднего плана с постоянным участием.</span><span class="sxs-lookup"><span data-stu-id="20968-121">If your organization requires compliance support, you can install the Persistent Chat Server Compliance service on the Persistent Chat Server Front End Server.</span></span> <span data-ttu-id="20968-122">Для обеспечения соответствия требованиям требуется отдельная база данных.</span><span class="sxs-lookup"><span data-stu-id="20968-122">A separate database is required for compliance.</span></span>

<span data-ttu-id="20968-123">Для каждой топологии требуется сервер с установленным Lync Server 2013 и сервер с установленным программным обеспечением базы данных SQL Server.</span><span class="sxs-lookup"><span data-stu-id="20968-123">At a minimum, each topology requires a server with Lync Server 2013 installed and a server with SQL Server database software installed.</span></span>

<span data-ttu-id="20968-124">Используйте построитель топологии, чтобы добавить сохраняемый сервер чата в развертывание Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="20968-124">Use Topology Builder to add Persistent Chat Server to your Lync Server 2013 deployments.</span></span> <span data-ttu-id="20968-125">Вы можете добавить один или несколько пулов серверов для постоянного чата с помощью Topology Builder.</span><span class="sxs-lookup"><span data-stu-id="20968-125">You can choose to add one or more Persistent Chat Server pools using Topology Builder.</span></span> <span data-ttu-id="20968-126">Следуйте тем же инструкциям по развертыванию, чтобы развернуть несколько пулов серверов сохраняемого чата, как и в случае с пулом.</span><span class="sxs-lookup"><span data-stu-id="20968-126">Follow the same deployment instructions for deploying multiple Persistent Chat Server pools as you would for any pool.</span></span> <span data-ttu-id="20968-127">Подробные сведения можно найти в разделе [развертывание Lync Server 2013](lync-server-2013-deploying-lync-server.md) в документации по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="20968-127">For details, see [Deploying Lync Server 2013](lync-server-2013-deploying-lync-server.md) in the Deployment documentation.</span></span>

<span data-ttu-id="20968-128">Сведения о доступных топологиях, требованиях к техническим и программному обеспечению для установки постоянного сервера чата, приведены в разделе [планирование сохраняемого сервера чата в Lync server 2013](lync-server-2013-planning-for-persistent-chat-server.md) в документации по планированию, [как сервер сохраняемого чата используется в Lync Server 2013](lync-server-2013-how-persistent-chat-server-works.md) в документации по планированию, документации по развертыванию, документации по операциям и [поддерживаемому оборудованию для Lync Server 2013](lync-server-2013-supported-hardware.md) в документации по поддержке.</span><span class="sxs-lookup"><span data-stu-id="20968-128">For details about available topologies and the technical and software requirements for installing Persistent Chat Server, see [Planning for Persistent Chat Server in Lync Server 2013](lync-server-2013-planning-for-persistent-chat-server.md) in the Planning documentation, [How Persistent Chat Server works in Lync Server 2013](lync-server-2013-how-persistent-chat-server-works.md) in the Planning documentation, Deployment documentation, or Operations documentation, and [Supported hardware for Lync Server 2013](lync-server-2013-supported-hardware.md) in the Supportability documentation.</span></span>

<span data-ttu-id="20968-129">Подробные сведения о получении сертификатов, создании базы данных SQL Server и создании хранилищ файлов можно найти в разделе [развертывание Lync Server 2013](lync-server-2013-deploying-lync-server.md) в документации по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="20968-129">For details about acquiring certificates, creating the SQL Server database, and creating file stores, see [Deploying Lync Server 2013](lync-server-2013-deploying-lync-server.md) in the Deployment documentation.</span></span>

<span data-ttu-id="20968-130">Один сервер-сервер для входа в чате может поддерживать 20 000 активных пользователей.</span><span class="sxs-lookup"><span data-stu-id="20968-130">A single Persistent Chat Server Front End Server can support 20,000 active users.</span></span> <span data-ttu-id="20968-131">Вы можете использовать серверный пул для постоянного чата с четырьмя активными серверами переднего плана, поддерживающими общее количество одновременных пользователей 80 000.</span><span class="sxs-lookup"><span data-stu-id="20968-131">You can have a Persistent Chat Server pool with up to 4 active Front End Servers supporting a total of 80,000 concurrent users.</span></span>

<span data-ttu-id="20968-132">На виртуальном сервере также поддерживается сохраняемый сервер чатов.</span><span class="sxs-lookup"><span data-stu-id="20968-132">Persistent Chat Server is also supported on a virtual server.</span></span> <span data-ttu-id="20968-133">Виртуальный сервер может поддерживать до 20 000 одновременных пользователей, если он соответствует спецификациям физического сервера.</span><span class="sxs-lookup"><span data-stu-id="20968-133">The virtual server can support up to 20,000 concurrent users if it matches the specifications of the physical server.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="20968-134">Для обеспечения безопасности файловой системы необходимо установить сохраняемый сервер чата в файловой системе NTFS.</span><span class="sxs-lookup"><span data-stu-id="20968-134">Persistent Chat Server must be installed on an NTFS file system to help enforce file system security.</span></span> <span data-ttu-id="20968-135">Файловая система FAT32 не поддерживается для сервера сохраняемого чата.</span><span class="sxs-lookup"><span data-stu-id="20968-135">FAT32 is not a supported file system for Persistent Chat Server.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="20968-136">Содержание</span><span class="sxs-lookup"><span data-stu-id="20968-136">In This Section</span></span>

  - [<span data-ttu-id="20968-137">Как работает сервер сохраняемого чата в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="20968-137">How Persistent Chat Server works in Lync Server 2013</span></span>](lync-server-2013-how-persistent-chat-server-works.md)

  - [<span data-ttu-id="20968-138">Контрольный список развертывания для сервера сохраняемого чата в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="20968-138">Deployment checklist for Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-deployment-checklist-for-persistent-chat-server.md)

  - [<span data-ttu-id="20968-139">Технические требования для постоянного сервера чата в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="20968-139">Technical requirements for Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-technical-requirements-for-persistent-chat-server.md)

  - [<span data-ttu-id="20968-140">Настройка систем и инфраструктуры для сервера сохраняемого чата в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="20968-140">Setting up systems and infrastructure for Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-setting-up-systems-and-infrastructure-for-persistent-chat-server.md)

  - [<span data-ttu-id="20968-141">Добавление сервера сохраняемого сеанса беседы в развертывание в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="20968-141">Adding Persistent Chat Server to your deployment in Lync Server 2013</span></span>](lync-server-2013-adding-persistent-chat-server-to-your-deployment.md)

  - [<span data-ttu-id="20968-142">Установка сервера сохраняемого чата в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="20968-142">Installing Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-installing-persistent-chat-server.md)

  - [<span data-ttu-id="20968-143">Добавление администратора сохраняемого чата в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="20968-143">Adding a Persistent Chat administrator in Lync Server 2013</span></span>](lync-server-2013-adding-a-persistent-chat-administrator.md)

  - [<span data-ttu-id="20968-144">Настройка сервера сохраняемого чата в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="20968-144">Configuring Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-configuring-persistent-chat-server.md)

  - [<span data-ttu-id="20968-145">Настройка сервера сохраняемого сеанса беседы с помощью командлетов Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="20968-145">Configuring Persistent Chat Server by using Windows PowerShell cmdlets</span></span>](configuring-persistent-chat-server-by-using-windows-powershell-cmdlets.md)

  - [<span data-ttu-id="20968-146">Устранение неполадок конфигурации сервера сохраняемого чата с помощью командлетов Windows PowerShell в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="20968-146">Troubleshooting Persistent Chat Server configuration using Windows PowerShell cmdlets in Lync Server 2013</span></span>](lync-server-2013-troubleshooting-persistent-chat-server-configuration-using-windows-powershell-cmdlets.md)

  - [<span data-ttu-id="20968-147">Настройка сервера сохраняемого чата для обеспечения высокой доступности и аварийного восстановления в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="20968-147">Configuring Persistent Chat Server for high availability and disaster recovery in Lync Server 2013</span></span>](lync-server-2013-configuring-persistent-chat-server-for-high-availability-and-disaster-recovery.md)

  - [<span data-ttu-id="20968-148">Отработка отказа и восстановление после сбоя сервера сохраняемого чата в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="20968-148">Failing over and failing back Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-failing-over-and-failing-back-persistent-chat-server.md)

<span data-ttu-id="20968-149"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="20968-149"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

