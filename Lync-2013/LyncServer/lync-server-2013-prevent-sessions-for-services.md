---
title: 'Lync Server 2013: предотвращение сеансов для служб'
description: 'Lync Server 2013: предотвращение сеансов для служб.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Prevent sessions for services
ms:assetid: 977dcc5c-2aac-48ef-86a1-a8d47b4d9e74
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182553(v=OCS.15)
ms:contentKeyID: 48184866
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 846a9da5330c3e64f61c27dfadd883f0c43a0ffa
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436904"
---
# <a name="prevent-sessions-for-services-in-lync-server-2013"></a><span data-ttu-id="d831b-103">Предотвращение сеансов для служб в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d831b-103">Prevent sessions for services in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d831b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d831b-104">

<span> </span></span></span>

<span data-ttu-id="d831b-105">_**Тема последнего изменения:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="d831b-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="d831b-106">Панель управления Lync Server можно использовать для предотвращения новых сеансов для всех служб Lync Server 2013, запущенных на определенном компьютере, или для предотвращения новых сеансов для конкретной службы Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d831b-106">You can use Lync Server Control Panel to prevent new sessions for all the Lync Server 2013 services running on a specific computer or to prevent new sessions for a specific Lync Server 2013 service.</span></span>

<div>

## <a name="to-prevent-new-sessions-for-all-lync-server-services-on-a-computer"></a><span data-ttu-id="d831b-107">Запрещение новых сеансов для всех служб Lync Server на компьютере</span><span class="sxs-lookup"><span data-stu-id="d831b-107">To prevent new sessions for all Lync Server services on a computer</span></span>

1.  <span data-ttu-id="d831b-108">Войдите в учетную запись пользователя, которая является членом группы RTCUniversalServerAdmins (или имеет эквивалентные права пользователей) или назначьте роль CsServerAdministrator или CsAdministrator, выполните вход на любой компьютер в сети, в которой вы развернули Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d831b-108">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or assigned to the CsServerAdministrator or CsAdministrator role, log on to any computer that is in the network in which you deployed Lync Server 2013.</span></span>

2.  <span data-ttu-id="d831b-109">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="d831b-109">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="d831b-110">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="d831b-110">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="d831b-111">На панели навигации слева щелкните **топология** и выберите **состояние**.</span><span class="sxs-lookup"><span data-stu-id="d831b-111">In the left navigation bar, click **Topology** and then click **Status**.</span></span>

4.  <span data-ttu-id="d831b-112">На странице " **состояние** " выполните сортировку или поиск по списку, если это необходимо, чтобы найти компьютер, на котором запущены службы, для которых вы хотите запретить новые сеансы, а затем щелкните его.</span><span class="sxs-lookup"><span data-stu-id="d831b-112">On the **Status** page, sort or search through the list as needed to find the computer that is running the services for which you want to prevent new sessions, and then click it.</span></span>

5.  <span data-ttu-id="d831b-113">Нажмите кнопку **действие**.</span><span class="sxs-lookup"><span data-stu-id="d831b-113">Click **Action**.</span></span>

6.  <span data-ttu-id="d831b-114">Нажмите кнопку **запретить новые сеансы для всех служб**.</span><span class="sxs-lookup"><span data-stu-id="d831b-114">Click **Prevent new sessions for all services**.</span></span>

</div>

<div>

## <a name="to-prevent-new-sessions-for-a-specific-service"></a><span data-ttu-id="d831b-115">Запрещение новых сеансов для конкретной службы</span><span class="sxs-lookup"><span data-stu-id="d831b-115">To prevent new sessions for a specific service</span></span>

1.  <span data-ttu-id="d831b-116">Войдите в учетную запись пользователя, которая является членом группы RTCUniversalServerAdmins (или имеет эквивалентные права пользователей) или назначьте роль CsServerAdministrator или CsAdministrator, выполните вход на любой компьютер в сети, в которой вы развернули Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d831b-116">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or assigned to the CsServerAdministrator or CsAdministrator role, log on to any computer that is in the network in which you deployed Lync Server 2013.</span></span>

2.  <span data-ttu-id="d831b-117">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="d831b-117">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="d831b-118">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="d831b-118">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="d831b-119">На панели навигации слева щелкните **топология** и выберите **состояние**.</span><span class="sxs-lookup"><span data-stu-id="d831b-119">In the left navigation bar, click **Topology** and then click **Status**.</span></span>

4.  <span data-ttu-id="d831b-120">На странице " **состояние** " выполните сортировку и поиск по списку, если это необходимо, чтобы найти компьютер, на котором запущена служба, которую вы хотите запустить или остановить, а затем щелкните ее.</span><span class="sxs-lookup"><span data-stu-id="d831b-120">On the **Status** page, sort or search through the list as needed to find the computer that is running the service you want to start or stop, and then click it.</span></span>

5.  <span data-ttu-id="d831b-121">Нажмите кнопку **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="d831b-121">Click **Properties**.</span></span>

6.  <span data-ttu-id="d831b-122">При необходимости отсортируйте список служб и выберите службу, для которой вы хотите запретить новые сеансы.</span><span class="sxs-lookup"><span data-stu-id="d831b-122">Sort the list of services, if necessary, and click the service for which you want to prevent new sessions.</span></span>

7.  <span data-ttu-id="d831b-123">Нажмите кнопку **действие**.</span><span class="sxs-lookup"><span data-stu-id="d831b-123">Click **Action**.</span></span>

8.  <span data-ttu-id="d831b-124">Выберите команду **запретить новые сеансы для службы**.</span><span class="sxs-lookup"><span data-stu-id="d831b-124">Click **Prevent new sessions for service**.</span></span>

9.  <span data-ttu-id="d831b-125">Нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="d831b-125">Click **Close**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="d831b-126">См. также</span><span class="sxs-lookup"><span data-stu-id="d831b-126">See Also</span></span>


[<span data-ttu-id="d831b-127">Управление топологией Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d831b-127">Managing the Lync Server 2013 topology</span></span>](lync-server-2013-managing-the-lync-server-topology.md)  
  

<span data-ttu-id="d831b-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d831b-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

