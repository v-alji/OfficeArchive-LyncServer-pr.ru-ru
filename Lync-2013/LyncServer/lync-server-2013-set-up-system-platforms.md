---
title: 'Lync Server 2013: настройка системных платформ'
description: 'Lync Server 2013: Настройка платформ системы.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Set up system platforms
ms:assetid: 2e72e49d-2737-4b5b-8c0a-60f6ecb15bf1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204783(v=OCS.15)
ms:contentKeyID: 48183756
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bd02c519d5632b7aa5732fbd9b880f7d1084b50f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423974"
---
# <a name="set-up-system-platforms-in-lync-server-2013"></a><span data-ttu-id="29eac-103">Настройка системных платформ в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="29eac-103">Set up system platforms in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="29eac-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="29eac-104">

<span> </span></span></span>

<span data-ttu-id="29eac-105">_**Тема последнего изменения:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="29eac-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="29eac-106">Прежде чем приступать к развертыванию сервера сохраняемого чата, необходимо установить требуемую операционную систему на оборудовании, удовлетворяющем требованиям к системе для серверов.</span><span class="sxs-lookup"><span data-stu-id="29eac-106">Before starting the deployment of Persistent Chat Server, you must install the required operating system on hardware that meets system requirements on servers:</span></span>

<span data-ttu-id="29eac-107">Сведения о поддерживаемом оборудовании для серверов с Lync Server 2013, серверами баз данных и файловыми серверами можно найти в документации поддержка [Lync server 2013](lync-server-2013-supported-hardware.md) .</span><span class="sxs-lookup"><span data-stu-id="29eac-107">For details about supported hardware for servers running Lync Server 2013, database servers, and file servers, see [Supported hardware for Lync Server 2013](lync-server-2013-supported-hardware.md) in the Supportability documentation.</span></span> <span data-ttu-id="29eac-108">Подробнее о поддерживаемых операционных системах и программах для работы с базами данных можно найти в документации по поддержке [серверного программного обеспечения и поддержки инфраструктуры в Lync Server 2013](lync-server-2013-server-software-and-infrastructure-support.md) .</span><span class="sxs-lookup"><span data-stu-id="29eac-108">For details about supported operating systems and database software, see [Server software and infrastructure support in Lync Server 2013](lync-server-2013-server-software-and-infrastructure-support.md) in the Supportability documentation.</span></span> <span data-ttu-id="29eac-109">Подробные сведения о требованиях к обновлению для Windows можно найти в статьях [дополнительные серверные службы и требования в Lync server 2013](lync-server-2013-additional-server-support-and-requirements.md) в документации по поддержке.</span><span class="sxs-lookup"><span data-stu-id="29eac-109">For details about Windows update requirements, see [Additional server support and requirements in Lync Server 2013](lync-server-2013-additional-server-support-and-requirements.md) in the Supportability documentation.</span></span>

<span data-ttu-id="29eac-110">Сервер клиентского **PersistentChatService**, на котором установлен сервер, может быть развернут на одном или нескольких отдельных компьютерах в пуле Lync Server 2013 Enterprise Edition.</span><span class="sxs-lookup"><span data-stu-id="29eac-110">The Persistent Chat Server Front End Server, **PersistentChatService**, can be deployed on one or more stand-alone computers in a Lync Server 2013 Enterprise Edition pool.</span></span> <span data-ttu-id="29eac-111">Они не могут быть выровнены на внешних серверах Lync Server Enterprise Edition.</span><span class="sxs-lookup"><span data-stu-id="29eac-111">They cannot be collocated on the Lync Server Enterprise Edition Front End Servers.</span></span> <span data-ttu-id="29eac-112">Сервер сохраняемого чата может развертываться загрузчиком так же, как и другие роли Lync Server.</span><span class="sxs-lookup"><span data-stu-id="29eac-112">Persistent Chat Server can be deployed by the Bootstrapper, just like other Lync Server roles.</span></span> <span data-ttu-id="29eac-113">Веб **-службы сохраняемого или загружаемого файла**, а также **веб-службы сохраняемого чата для управления комнатой** — это веб-компоненты, развернутые на серверах переднего плана Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="29eac-113">The **Persistent Chat Web Services for File Upload/Download**, and **Persistent Chat Web Services for Chat Room Management** are web components deployed on the Lync Server 2013 Front End Servers.</span></span>

<span data-ttu-id="29eac-114">Один сервер-сервер для входа в чате может поддерживать 20 000 активных пользователей.</span><span class="sxs-lookup"><span data-stu-id="29eac-114">A single Persistent Chat Server Front End Server can support 20,000 active users.</span></span> <span data-ttu-id="29eac-115">Вы можете использовать серверный пул для постоянного чата с четырьмя активными интерфейсами, поддерживающими общее количество одновременных пользователей 80 000.</span><span class="sxs-lookup"><span data-stu-id="29eac-115">You can have a Persistent Chat Server pool with up to 4 active front ends supporting a total of 80,000 concurrent users.</span></span> <span data-ttu-id="29eac-116">Сохраняемый сервер обратного чата, **PersistentChatStore**, сохраняет комнаты чата и категории.</span><span class="sxs-lookup"><span data-stu-id="29eac-116">The Persistent Chat Back End Server, **PersistentChatStore**, stores the chat rooms and categories.</span></span> <span data-ttu-id="29eac-117">Рекомендуем установить **PersistentChatStore** на выделенный сервер SQL Server в пуле выпуска Enterprise Edition; Несмотря на то что мы поддерживаем размещение сервера Lync Server 2013 на обратном стороне и **PersistentChatStore** на одном и том же экземпляре SQL Server.</span><span class="sxs-lookup"><span data-stu-id="29eac-117">We recommend that you install the **PersistentChatStore** on a dedicated SQL Server Back End Server in your Enterprise Edition pool; although we support collocating Lync Server 2013 Back End Server and **PersistentChatStore** on the same SQL Server instance.</span></span>

<span data-ttu-id="29eac-118">Если ваша организация требует поддержки соответствия требованиям, вы можете установить ее с помощью построителя топологии.</span><span class="sxs-lookup"><span data-stu-id="29eac-118">If your organization requires compliance support, you can install it by using Topology Builder.</span></span> <span data-ttu-id="29eac-119">Служба соответствия требованиям сервера, установленная на сервере постоянного чата, устанавливается на том же компьютере, что и сервер клиентского доступа.</span><span class="sxs-lookup"><span data-stu-id="29eac-119">The Persistent Chat Server Compliance service is installed on the same computer as the Persistent Chat Server Front End Server.</span></span> <span data-ttu-id="29eac-120">Для обеспечения соответствия требованиям требуется отдельная база данных.</span><span class="sxs-lookup"><span data-stu-id="29eac-120">A separate database is required for compliance.</span></span> <span data-ttu-id="29eac-121">Подробные сведения о требованиях к соответствию требованиям для постоянного сервера чата приведены в разделе [планирование сохраняемого сервера чата в Lync server 2013](lync-server-2013-planning-for-persistent-chat-server.md) в документации по планированию.</span><span class="sxs-lookup"><span data-stu-id="29eac-121">For details about compliance requirements for Persistent Chat Server, see [Planning for Persistent Chat Server in Lync Server 2013](lync-server-2013-planning-for-persistent-chat-server.md) in the Planning documentation.</span></span>

<span data-ttu-id="29eac-122">Для каждой топологии требуется сервер с установленным Lync Server 2013 и сервер с установленным программным обеспечением базы данных SQL Server.</span><span class="sxs-lookup"><span data-stu-id="29eac-122">At a minimum, each topology requires a server with Lync Server 2013 installed and a server with SQL Server database software installed.</span></span> <span data-ttu-id="29eac-123">В построителе топологии поддерживается несколько пулов серверов сохраняемого чата.</span><span class="sxs-lookup"><span data-stu-id="29eac-123">Topology Builder supports multiple Persistent Chat Server pools.</span></span> <span data-ttu-id="29eac-124">Следуйте тем же инструкциям по развертыванию, чтобы развернуть несколько пулов серверов сохраняемого чата, как и в случае с [развертыванием сервера Lync server 2013](lync-server-2013-deploying-lync-server.md) в документации по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="29eac-124">Follow the same deployment instructions for deploying multiple Persistent Chat Server pools as you would for any pool from [Deploying Lync Server 2013](lync-server-2013-deploying-lync-server.md) in the Deployment documentation.</span></span>

<span data-ttu-id="29eac-125">Кроме того, вы можете развернуть сервер с помощью Lync Server 2013 Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="29eac-125">You can also deploy Persistent Chat Server with Lync Server 2013 Standard Edition.</span></span> <span data-ttu-id="29eac-126">В этом случае сервер переднего плана **PersistentChatService** размещается на сервере Standard Edition, и вы можете развернуть сервер **PersistentChatStore** Back на локальном экземпляре SQL Server Express.</span><span class="sxs-lookup"><span data-stu-id="29eac-126">In this case, the **PersistentChatService** Front End Server is collocated on the Standard Edition server, and you can deploy the **PersistentChatStore** Back End Server on the local SQL Server Express instance.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="29eac-127">Для обеспечения высокой доступности не поддерживается постоянная версия сервера Chat &nbsp; Standard.</span><span class="sxs-lookup"><span data-stu-id="29eac-127">We do not support Persistent Chat Server&nbsp;Standard Edition for high availability.</span></span> <span data-ttu-id="29eac-128">Производительность и масштаб будут ограничены.</span><span class="sxs-lookup"><span data-stu-id="29eac-128">Performance and scale will be limited.</span></span> <span data-ttu-id="29eac-129">Кроме того, мы поддерживаем только новые версии сервера &nbsp; Standard чата.</span><span class="sxs-lookup"><span data-stu-id="29eac-129">Furthermore, we support only new Persistent Chat Server&nbsp;Standard Edition server deployments.</span></span> <span data-ttu-id="29eac-130">Корпорация Майкрософт не поддерживает обновление для Lync Server 2010, групповой чат с сервером в Lync Server 2013 для &nbsp; сервера Standard Chat &nbsp; стандартный выпуск.</span><span class="sxs-lookup"><span data-stu-id="29eac-130">We do not support an upgrade of Lync Server 2010, Group Chat Server to a Lync Server 2013&nbsp;Persistent Chat Server&nbsp;Standard Edition.</span></span>



</div>

<div>

## <a name="see-also"></a><span data-ttu-id="29eac-131">См. также</span><span class="sxs-lookup"><span data-stu-id="29eac-131">See Also</span></span>


[<span data-ttu-id="29eac-132">Поддержка дополнительных серверов и соответствующие требования в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="29eac-132">Additional server support and requirements in Lync Server 2013</span></span>](lync-server-2013-additional-server-support-and-requirements.md)  


[<span data-ttu-id="29eac-133">Поддерживаемое оборудование для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="29eac-133">Supported hardware for Lync Server 2013</span></span>](lync-server-2013-supported-hardware.md)  
[<span data-ttu-id="29eac-134">Поддержка серверного программного обеспечения и инфраструктуры в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="29eac-134">Server software and infrastructure support in Lync Server 2013</span></span>](lync-server-2013-server-software-and-infrastructure-support.md)  
[<span data-ttu-id="29eac-135">Планирование сервера сохраняемого чата в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="29eac-135">Planning for Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-planning-for-persistent-chat-server.md)  
[<span data-ttu-id="29eac-136">Развертывание Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="29eac-136">Deploying Lync Server 2013</span></span>](lync-server-2013-deploying-lync-server.md)  
  

<span data-ttu-id="29eac-137"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="29eac-137"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

