---
title: Запрет сеансов для служб
description: Предотвращение сеансов для служб.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Prevent sessions for services
ms:assetid: 4b541c72-cdc1-4f86-a5a8-c43c24f41d8b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688049(v=OCS.15)
ms:contentKeyID: 49733642
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a452f8091716daa0a15967e2a278e82c5bc8c4f3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438465"
---
# <a name="prevent-sessions-for-services"></a><span data-ttu-id="17bcb-103">Запрет сеансов для служб</span><span class="sxs-lookup"><span data-stu-id="17bcb-103">Prevent sessions for services</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="17bcb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="17bcb-104">

<span> </span></span></span>

<span data-ttu-id="17bcb-105">_**Тема последнего изменения:** 2012-10-04_</span><span class="sxs-lookup"><span data-stu-id="17bcb-105">_**Topic Last Modified:** 2012-10-04_</span></span>

<span data-ttu-id="17bcb-106">С помощью панели управления Microsoft Lync Server 2010 можно запретить новые сеансы для всех служб Lync Server 2010, запущенных на определенном компьютере, или запретить новые сеансы для конкретной службы Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="17bcb-106">You can use Microsoft Lync Server 2010 Control Panel to prevent new sessions for all the Lync Server 2010 services running on a specific computer or to prevent new sessions for a specific Lync Server 2010 service.</span></span>

<div>

## <a name="to-prevent-new-sessions-for-all-lync-server-services-on-a-computer"></a><span data-ttu-id="17bcb-107">Запрещение новых сеансов для всех служб Lync Server на компьютере</span><span class="sxs-lookup"><span data-stu-id="17bcb-107">To prevent new sessions for all Lync Server services on a computer</span></span>

1.  <span data-ttu-id="17bcb-108">Войдите в учетную запись пользователя, которая является членом группы RTCUniversalServerAdmins (или имеет эквивалентные права пользователей) или назначьте роль CsServerAdministrator или CsAdministrator, выполните вход на любой компьютер в сети, в которой вы развернули Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="17bcb-108">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or assigned to the CsServerAdministrator or CsAdministrator role, log on to any computer that is in the network in which you deployed Lync Server 2013.</span></span>

2.  <span data-ttu-id="17bcb-109">Откройте Панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="17bcb-109">Open Lync Server Control Panel.</span></span>

3.  <span data-ttu-id="17bcb-110">На панели навигации слева щелкните **топология** и выберите **состояние**.</span><span class="sxs-lookup"><span data-stu-id="17bcb-110">In the left navigation bar, click **Topology** and then click **Status**.</span></span>

4.  <span data-ttu-id="17bcb-111">На странице " **состояние** " выполните сортировку или поиск по списку, если это необходимо, чтобы найти компьютер, на котором запущены службы, для которых вы хотите запретить новые сеансы, а затем щелкните его.</span><span class="sxs-lookup"><span data-stu-id="17bcb-111">On the **Status** page, sort or search through the list as needed to find the computer that is running the services for which you want to prevent new sessions, and then click it.</span></span>

5.  <span data-ttu-id="17bcb-112">Нажмите кнопку **действие**.</span><span class="sxs-lookup"><span data-stu-id="17bcb-112">Click **Action**.</span></span>

6.  <span data-ttu-id="17bcb-113">Нажмите кнопку **запретить новые сеансы для всех служб**.</span><span class="sxs-lookup"><span data-stu-id="17bcb-113">Click **Prevent new sessions for all services**.</span></span>

</div>

<div>

## <a name="to-prevent-new-sessions-for-a-specific-service"></a><span data-ttu-id="17bcb-114">Запрещение новых сеансов для конкретной службы</span><span class="sxs-lookup"><span data-stu-id="17bcb-114">To prevent new sessions for a specific service</span></span>

1.  <span data-ttu-id="17bcb-115">Войдите в учетную запись пользователя, которая является членом группы RTCUniversalServerAdmins (или имеет эквивалентные права пользователей) или назначьте роль CsServerAdministrator или CsAdministrator, выполните вход на любой компьютер в сети, в которой вы развернули Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="17bcb-115">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or assigned to the CsServerAdministrator or CsAdministrator role, log on to any computer that is in the network in which you deployed Lync Server 2013.</span></span>

2.  <span data-ttu-id="17bcb-116">Откройте Панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="17bcb-116">Open Lync Server Control Panel.</span></span>

3.  <span data-ttu-id="17bcb-117">На панели навигации слева щелкните **топология** и выберите **состояние**.</span><span class="sxs-lookup"><span data-stu-id="17bcb-117">In the left navigation bar, click **Topology** and then click **Status**.</span></span>

4.  <span data-ttu-id="17bcb-118">На странице " **состояние** " выполните сортировку и поиск по списку, если это необходимо, чтобы найти компьютер, на котором запущена служба, которую вы хотите запустить или остановить, а затем щелкните ее.</span><span class="sxs-lookup"><span data-stu-id="17bcb-118">On the **Status** page, sort or search through the list as needed to find the computer that is running the service you want to start or stop, and then click it.</span></span>

5.  <span data-ttu-id="17bcb-119">Нажмите кнопку **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="17bcb-119">Click **Properties**.</span></span>

6.  <span data-ttu-id="17bcb-120">При необходимости отсортируйте список служб и выберите службу, для которой вы хотите запретить новые сеансы.</span><span class="sxs-lookup"><span data-stu-id="17bcb-120">Sort the list of services, if necessary, and click the service for which you want to prevent new sessions.</span></span>

7.  <span data-ttu-id="17bcb-121">Нажмите кнопку **действие**.</span><span class="sxs-lookup"><span data-stu-id="17bcb-121">Click **Action**.</span></span>

8.  <span data-ttu-id="17bcb-122">Выберите команду **запретить новые сеансы для службы**.</span><span class="sxs-lookup"><span data-stu-id="17bcb-122">Click **Prevent new sessions for service**.</span></span>

9.  <span data-ttu-id="17bcb-123">Нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="17bcb-123">Click **Close**.</span></span>

<span data-ttu-id="17bcb-124"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="17bcb-124"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

