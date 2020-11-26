---
title: 'Lync Server 2013: создание политики маршрутизации VoIP для пользователей филиалов'
description: 'Lync Server 2013: Создание политики маршрутизации VoIP для пользователей филиалов.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create the VoIP routing policy for branch users
ms:assetid: 10deca9f-f870-4a42-b25d-e4fc53108658
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398196(v=OCS.15)
ms:contentKeyID: 48183435
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c39cff86d9ede957fa99e7955d8a87172380f963
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431556"
---
# <a name="create-the-voip-routing-policy-for-branch-users-in-lync-server-2013"></a><span data-ttu-id="359ea-103">Создание политики маршрутизации VoIP для пользователей филиалов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="359ea-103">Create the VoIP routing policy for branch users in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="359ea-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="359ea-104">

<span> </span></span></span>

<span data-ttu-id="359ea-105">_**Тема последнего изменения:** 2012-09-23_</span><span class="sxs-lookup"><span data-stu-id="359ea-105">_**Topic Last Modified:** 2012-09-23_</span></span>

<span data-ttu-id="359ea-106">Мы рекомендуем создать отдельную политику передачи голоса по протоколу IP (VoIP) для пользователей на сайтах филиалов.</span><span class="sxs-lookup"><span data-stu-id="359ea-106">We recommend creating a separate voice over IP (VoIP) policy for users at branch sites.</span></span> <span data-ttu-id="359ea-107">Эта политика должна содержать маршруты для выхода из бесперебойно работающего устройства филиала или из внешнего шлюза сервера филиалов и маршрутов резервного копирования для выхода из шлюза на центральном сайте.</span><span class="sxs-lookup"><span data-stu-id="359ea-107">This policy should contain routes to egress from the Survivable Branch Appliance gateway or the Survivable Branch Server external gateway and backup routes to egress from a gateway at the central site.</span></span> <span data-ttu-id="359ea-108">Вне зависимости от того, где зарегистрирован пользователь, либо в регистраторе на устройстве с бесперебойной подразделением, либо в кластере регистратора резервного копирования на центральном сайте, политика VoIP пользователя действует всегда.</span><span class="sxs-lookup"><span data-stu-id="359ea-108">Regardless of where the user is registered, either on the Registrar on the Survivable Branch Appliance or Survivable Branch Server or on the backup Registrar cluster at the central site, the user’s VoIP policy is always in effect.</span></span>

<div>

## <a name="to-configure-the-voip-routing-policy-for-branch-users"></a><span data-ttu-id="359ea-109">Настройка политики маршрутизации VoIP для пользователей филиалов</span><span class="sxs-lookup"><span data-stu-id="359ea-109">To configure the VoIP routing policy for branch users</span></span>

1.  <span data-ttu-id="359ea-110">Создание абонентской группы на уровне пользователя и назначение ее пользователям ответвления.</span><span class="sxs-lookup"><span data-stu-id="359ea-110">Create a user-level dial plan and assign it to branch users.</span></span> <span data-ttu-id="359ea-111">(См. раздел [Создание абонентской группы в Lync Server 2013](lync-server-2013-create-a-dial-plan.md) в документации по эксплуатации).</span><span class="sxs-lookup"><span data-stu-id="359ea-111">(See [Create a dial plan in Lync Server 2013](lync-server-2013-create-a-dial-plan.md) in the Operations documentation.)</span></span>

2.  <span data-ttu-id="359ea-112">Назначьте правила нормализации для пользователей, находящихся на этом сайте.</span><span class="sxs-lookup"><span data-stu-id="359ea-112">Assign normalization rules corresponding to the dialing habits of users at that site.</span></span> <span data-ttu-id="359ea-113">Если бесперебойно работающее устройство филиала или сервер, который может быть подключен к сети, не переключается на пул регистратора резервного копирования на центральном сайте, будет применена та же самая абонентская группа.</span><span class="sxs-lookup"><span data-stu-id="359ea-113">If the Survivable Branch Appliance or Survivable Branch Server user fails over to the backup Registrar pool at the central site, the same dial plan will be in effect.</span></span> <span data-ttu-id="359ea-114">(См. раздел [Создание абонентской группы в Lync Server 2013](lync-server-2013-create-a-dial-plan.md) в документации по эксплуатации).</span><span class="sxs-lookup"><span data-stu-id="359ea-114">(See [Create a dial plan in Lync Server 2013](lync-server-2013-create-a-dial-plan.md) in the Operations documentation.)</span></span>

3.  <span data-ttu-id="359ea-115">Настройте маршрут голосовой связи, egresses с работающего шлюза устройства филиала или с работающего внешнего шлюза сервера филиала.</span><span class="sxs-lookup"><span data-stu-id="359ea-115">Configure a voice route that egresses from the Survivable Branch Appliance gateway or the Survivable Branch Server external gateway.</span></span> <span data-ttu-id="359ea-116">(См. раздел [Создание голосового маршрута в Lync Server 2013](lync-server-2013-create-a-voice-route.md) в документации по эксплуатации).</span><span class="sxs-lookup"><span data-stu-id="359ea-116">(See [Create a voice route in Lync Server 2013](lync-server-2013-create-a-voice-route.md) in the Operations documentation.)</span></span>

4.  <span data-ttu-id="359ea-117">Настройте маршрут для резервного копирования на устройстве, работающем в сети, или в бесперебойно работающем шлюзе, чтобы он указывал на пул регистратора архивации (сопоставленный с сервером исправлений) на центральном сайте.</span><span class="sxs-lookup"><span data-stu-id="359ea-117">Set a backup call route on the Survivable Branch Appliance or Survivable Branch Server gateway to point to the backup Registrar pool (collocated with Mediation Server) at the central site.</span></span> <span data-ttu-id="359ea-118">(Просмотрите сведения о работающем устройстве филиалов или о работающей в сети компании поставщика серверов филиалов.)</span><span class="sxs-lookup"><span data-stu-id="359ea-118">(See your Survivable Branch Appliance or Survivable Branch Server vendor documentation.)</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="359ea-119">Этот параметр маршрутизации для резервного копирования помогает гарантировать, что входящие звонки пользователю филиала будут работать, когда недоступно работающее устройство филиала или неактивный сервер филиала (например, если он отключен для обслуживания).</span><span class="sxs-lookup"><span data-stu-id="359ea-119">This backup call route setup helps ensure that inbound calls to the branch user will work when the Survivable Branch Appliance or Survivable Branch Server is not available (for example, if it is down for maintenance).</span></span> <span data-ttu-id="359ea-120">Если сервер регистраторов и исправлений на неработающем устройстве филиалов или работающем неработающем филиале недоступен, а пользователь зарегистрирован в пуле регистратора резервных копий на центральном сайте, входящие звонки могут перенаправляться пользователю.</span><span class="sxs-lookup"><span data-stu-id="359ea-120">If the Registrar and Mediation Server on the Survivable Branch Appliance or Survivable Branch Server are not available, and the user is registered with the backup Registrar pool at the central site, inbound calls can still be routed to the user.</span></span>

    
    </div>

<span data-ttu-id="359ea-121">**Следующий шаг**: [Настройка параметров перенаправления голосовой почты в Lync Server 2013](lync-server-2013-configure-voice-mail-rerouting-settings.md)</span><span class="sxs-lookup"><span data-stu-id="359ea-121">**Next step**: [Configure voice mail rerouting settings in Lync Server 2013](lync-server-2013-configure-voice-mail-rerouting-settings.md)</span></span>

<span data-ttu-id="359ea-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="359ea-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

