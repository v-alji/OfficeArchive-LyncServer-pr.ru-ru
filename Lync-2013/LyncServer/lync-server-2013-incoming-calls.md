---
title: 'Lync Server 2013: входящие звонки'
description: 'Lync Server 2013: входящие звонки.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Incoming calls
ms:assetid: 65b9c1b4-6af7-4527-8c33-22c4442bd209
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994038(v=OCS.15)
ms:contentKeyID: 51803948
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3a72c7fc378240f9751eae8e6c24e9cc601b08d3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427301"
---
# <a name="incoming-calls-in-lync-server-2013"></a><span data-ttu-id="d435f-103">Входящие звонки в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d435f-103">Incoming calls in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d435f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d435f-104">

<span> </span></span></span>

<span data-ttu-id="d435f-105">_**Тема последнего изменения:** 2013-03-09_</span><span class="sxs-lookup"><span data-stu-id="d435f-105">_**Topic Last Modified:** 2013-03-09_</span></span>

<span data-ttu-id="d435f-106">Маршрутизация входящих вызовов пользователей, включенных для Location-Based маршрутизации, зависит от расположения конечной точки пользователя.</span><span class="sxs-lookup"><span data-stu-id="d435f-106">The routing of incoming calls to users enabled for Location-Based Routing depends on the location of the user’s endpoint.</span></span> <span data-ttu-id="d435f-107">Маршрутизация входящих звонков подвергается влиянию следующим образом.</span><span class="sxs-lookup"><span data-stu-id="d435f-107">The routing of incoming calls is affected in the following way.</span></span> <span data-ttu-id="d435f-108">Если у пользователя есть входящий звонок на конечную точку, расположенную на сайте сети с поддержкой маршрутизации Location-Based, а конечная точка находится на том же сайте сети, что и шлюз PSTN, Звонок будет перенаправлен.</span><span class="sxs-lookup"><span data-stu-id="d435f-108">If a user has an incoming call to an endpoint located in a Location-Based Routing enabled network site, and the endpoint is located in the same network site as the PSTN gateway, the call will be routed.</span></span> <span data-ttu-id="d435f-109">Если у пользователя есть входящий звонок на конечную точку, расположенную на сайте сети с поддержкой маршрутизации Location-Based, а конечная точка находится на другом сайте сети, чем шлюз PSTN, Звонок не будет маршрутизироваться.</span><span class="sxs-lookup"><span data-stu-id="d435f-109">If a user has an incoming call to an endpoint located in a Location-Based Routing enabled network site, and the endpoint is located in a different network site than the PSTN gateway, the call will not be routed.</span></span> <span data-ttu-id="d435f-110">Если пользователь не имеет конечных точек, расположенных на том же сетевом сайте, что и шлюз ТСОП, с которого происходит входящий звонок, этот звонок будет переадресован на голосовую почту пользователя, а уведомление о пропущенном звонке будет отправлено вызываемому абоненту.</span><span class="sxs-lookup"><span data-stu-id="d435f-110">When a user has no endpoints located in the same network site as the PSTN gateway where the incoming call is originating from, the incoming call will be routed directly to the user’s voicemail and a missed call notification will be sent to the called party.</span></span>

<span data-ttu-id="d435f-111">Параметры переадресации звонков для пользователя, для которого включена Location-Based маршрутизация, будут по-прежнему применяться, однако переадресация звонков будет выполняться Location-Based ограничениях маршрутизации для пользователя.</span><span class="sxs-lookup"><span data-stu-id="d435f-111">The call forwarding settings of a user that is enabled for Location-Based Routing will continue to be enforced, however, calls forwarded will be subject to Location-Based Routing restrictions of the user.</span></span>

<span data-ttu-id="d435f-112">В следующей таблице показано, как маршрутизация Location-Based влияет на маршрутизацию входящих вызовов в зависимости от расположения конечной точки вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="d435f-112">The following table illustrates how Location-Based Routing affects the routing of inbound calls depending on the location of the callee’s endpoint.</span></span> <span data-ttu-id="d435f-113">Сетевая сеть шлюза PSTN включена для маршрутизации Location-Based, а Location-Based маршрутизация разрешает только маршрутизацию звонков по PSTN в конечные точки на том же сайте сети.</span><span class="sxs-lookup"><span data-stu-id="d435f-113">The network site of the PSTN gateway is enabled for Location-Based Routing, and Location-Based Routing only permits routing of PSTN calls to endpoints within the same network site.</span></span>

### <a name="callee-receiving-an-inbound-call-from-the-pstn"></a><span data-ttu-id="d435f-114">Вызываемый абонент получает входящий звонок от ТСОП</span><span class="sxs-lookup"><span data-stu-id="d435f-114">Callee receiving an inbound call from the PSTN</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="d435f-115">Конечная точка вызываемого абонента расположена на том же сетевом сайте, что и шлюз ТСОП</span><span class="sxs-lookup"><span data-stu-id="d435f-115">Callee’s endpoint located in the same network site as PSTN gateway</span></span></th>
<th><span data-ttu-id="d435f-116">Конечная точка вызываемого абонента не расположена на том же сетевом сайте, что и шлюз ТСОП</span><span class="sxs-lookup"><span data-stu-id="d435f-116">Callee’s endpoint not located in the same network site as PSTN gateway</span></span></th>
<th><span data-ttu-id="d435f-117">Конечная точка вызываемого абонента расположена на неизвестном сетевом сайте или не включена для маршрутизации на основе расположения</span><span class="sxs-lookup"><span data-stu-id="d435f-117">Callee’s endpoint located in unknown network site or not enabled for Location-Based Routing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d435f-118">Маршрутизация входящих звонков ТСОП</span><span class="sxs-lookup"><span data-stu-id="d435f-118">Routing of inbound PSTN call</span></span></p></td>
<td><p><span data-ttu-id="d435f-119">Входящий звонок направляется в конечные точки вызываемого абонента</span><span class="sxs-lookup"><span data-stu-id="d435f-119">Incoming call is routed to callee’s endpoints</span></span></p></td>
<td><p><span data-ttu-id="d435f-120">Входящий звонок не направляется в конечные точки вызываемого абонента</span><span class="sxs-lookup"><span data-stu-id="d435f-120">Incoming call is not routed to callee’s endpoints</span></span></p></td>
<td><p><span data-ttu-id="d435f-121">Входящий звонок не направляется в конечные точки вызываемого абонента</span><span class="sxs-lookup"><span data-stu-id="d435f-121">Incoming call is not routed to callee’s endpoints</span></span></p></td>
</tr>
</tbody>
</table>

  

<div>

## <a name="see-also"></a><span data-ttu-id="d435f-122">См. также</span><span class="sxs-lookup"><span data-stu-id="d435f-122">See Also</span></span>


[<span data-ttu-id="d435f-123">Сценарии маршрутизации на основе местоположения в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d435f-123">Scenarios for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-scenarios-for-location-based-routing.md)  
  

<span data-ttu-id="d435f-124"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d435f-124"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

