---
title: 'Lync Server 2013: запуск и остановка служб Lync Server'
description: 'Lync Server 2013: запуск и остановка служб Lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Start or stop Lync Server 2013 services
ms:assetid: 1c70b4ec-9de5-4f7a-a3c9-c0eb76710505
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520958(v=OCS.15)
ms:contentKeyID: 48183554
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1d6e6520cbf6fda38676beab984c2d006061b019
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423682"
---
# <a name="start-or-stop-lync-server-2013-services"></a><span data-ttu-id="09c27-103">Запуск и остановка служб Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="09c27-103">Start or stop Lync Server 2013 services</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="09c27-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="09c27-104">

<span> </span></span></span>

<span data-ttu-id="09c27-105">_**Тема последнего изменения:** 2014-02-05_</span><span class="sxs-lookup"><span data-stu-id="09c27-105">_**Topic Last Modified:** 2014-02-05_</span></span>

<span data-ttu-id="09c27-106">С помощью панели управления Lync Server можно запускать и останавливать все службы Lync Server 2013, запущенные на конкретном компьютере, а также запускать и останавливать определенную службу.</span><span class="sxs-lookup"><span data-stu-id="09c27-106">You can use Lync Server Control Panel to start or stop all the Lync Server 2013 services running on a specific computer or to start or stop a specific service.</span></span>

<div>

## <a name="to-start-or-stop-all-lync-server-services-on-a-computer"></a><span data-ttu-id="09c27-107">Запуск и остановка всех служб Lync Server на компьютере</span><span class="sxs-lookup"><span data-stu-id="09c27-107">To start or stop all Lync Server services on a computer</span></span>

1.  <span data-ttu-id="09c27-108">Войдите в учетную запись пользователя, которая является членом группы RTCUniversalServerAdmins (или имеет эквивалентные права пользователей) или назначьте роль CsServerAdministrator или CsAdministrator, выполните вход на любой компьютер в сети, в которой вы развернули Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="09c27-108">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or assigned to the CsServerAdministrator or CsAdministrator role, log on to any computer that is in the network in which you deployed Lync Server 2013.</span></span> <span data-ttu-id="09c27-109">Вы можете определить, назначена ли вам роль CsServerAdministrator или CsAdministrator RBAC, выполнив команду, подобную следующей:</span><span class="sxs-lookup"><span data-stu-id="09c27-109">You can determine whether you have been assigned the CsServerAdministrator or the CsAdministrator RBAC role by running a command similar to the following:</span></span>
    
        Get-CsAdminRoleAssignment -Identity "kenmyer"

2.  <span data-ttu-id="09c27-110">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="09c27-110">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="09c27-111">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="09c27-111">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="09c27-112">На панели навигации слева щелкните **топология** и выберите **состояние**.</span><span class="sxs-lookup"><span data-stu-id="09c27-112">In the left navigation bar, click **Topology** and then click **Status**.</span></span>

4.  <span data-ttu-id="09c27-113">На странице " **состояние** " выполните сортировку и поиск по списку, если это необходимо, чтобы найти компьютер, на котором запущены службы, которые вы хотите запустить или остановить, а затем щелкните его.</span><span class="sxs-lookup"><span data-stu-id="09c27-113">On the **Status** page, sort or search through the list as needed to find the computer that is running the services you want to start or stop, and then click it.</span></span>

5.  <span data-ttu-id="09c27-114">Нажмите кнопку **действие**.</span><span class="sxs-lookup"><span data-stu-id="09c27-114">Click **Action**.</span></span>

6.  <span data-ttu-id="09c27-115">Нажмите кнопку **начать все службы** или **остановить все службы**.</span><span class="sxs-lookup"><span data-stu-id="09c27-115">Click **Start All services** or **Stop All services**.</span></span>

</div>

<div>

## <a name="to-start-or-stop-a-specific-service"></a><span data-ttu-id="09c27-116">Запуск и остановка определенной службы</span><span class="sxs-lookup"><span data-stu-id="09c27-116">To start or stop a specific service</span></span>

1.  <span data-ttu-id="09c27-117">Войдите на любой компьютер во внутреннем развертывании с использованием учетной записи пользователя, назначенной роли CsUserAdministrator или CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="09c27-117">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="09c27-118">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="09c27-118">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="09c27-119">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="09c27-119">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="09c27-120">На панели навигации слева щелкните **топология** и выберите **состояние**.</span><span class="sxs-lookup"><span data-stu-id="09c27-120">In the left navigation bar, click **Topology** and then click **Status**.</span></span>

4.  <span data-ttu-id="09c27-121">На странице " **состояние** " выполните сортировку и поиск по списку, если это необходимо, чтобы найти компьютер, на котором запущена служба, которую вы хотите запустить или остановить, а затем щелкните ее.</span><span class="sxs-lookup"><span data-stu-id="09c27-121">On the **Status** page, sort or search through the list as needed to find the computer that is running the service you want to start or stop, and then click it.</span></span>

5.  <span data-ttu-id="09c27-122">Нажмите кнопку **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="09c27-122">Click **Properties**.</span></span>

6.  <span data-ttu-id="09c27-123">При необходимости отсортируйте список служб и выберите службу, которую вы хотите запустить или остановить.</span><span class="sxs-lookup"><span data-stu-id="09c27-123">Sort the list of services, if necessary, and click the service you want to start or stop.</span></span>

7.  <span data-ttu-id="09c27-124">Нажмите кнопку **действие**.</span><span class="sxs-lookup"><span data-stu-id="09c27-124">Click **Action**.</span></span>

8.  <span data-ttu-id="09c27-125">Нажмите кнопку **запустить службу** или **остановить службу**.</span><span class="sxs-lookup"><span data-stu-id="09c27-125">Click **Start service** or **Stop service**.</span></span>

9.  <span data-ttu-id="09c27-126">Нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="09c27-126">Click **Close**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="09c27-127">См. также</span><span class="sxs-lookup"><span data-stu-id="09c27-127">See Also</span></span>


[<span data-ttu-id="09c27-128">Предотвращение сеансов для служб в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="09c27-128">Prevent sessions for services in Lync Server 2013</span></span>](lync-server-2013-prevent-sessions-for-services.md)  


[<span data-ttu-id="09c27-129">Управление топологией Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="09c27-129">Managing the Lync Server 2013 topology</span></span>](lync-server-2013-managing-the-lync-server-topology.md)  
  

<span data-ttu-id="09c27-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="09c27-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

