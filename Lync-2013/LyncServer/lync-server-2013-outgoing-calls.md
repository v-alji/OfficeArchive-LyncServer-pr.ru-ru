---
title: 'Lync Server 2013: исходящие звонки'
description: 'Lync Server 2013: исходящие вызовы.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Outgoing calls
ms:assetid: 885ffe6f-cd51-4f21-8d4f-a1ff8d818858
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994049(v=OCS.15)
ms:contentKeyID: 51803960
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e14f19dec35a6da47a2ddd62657d5d087a854f16
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424837"
---
# <a name="outgoing-calls-in-lync-server-2013"></a><span data-ttu-id="7df3a-103">Исходящие звонки в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7df3a-103">Outgoing calls in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7df3a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7df3a-104">

<span> </span></span></span>

<span data-ttu-id="7df3a-105">_**Тема последнего изменения:** 2013-03-09_</span><span class="sxs-lookup"><span data-stu-id="7df3a-105">_**Topic Last Modified:** 2013-03-09_</span></span>

<span data-ttu-id="7df3a-106">Маршрутизация исходящих вызовов пользователей, для которых разрешена Location-Based маршрутизация, зависит от расположения в сети для конечной точки пользователя.</span><span class="sxs-lookup"><span data-stu-id="7df3a-106">The routing of outbound calls of users enabled for Location-Based Routing is affected by the network location of the user’s endpoint.</span></span> <span data-ttu-id="7df3a-107">В следующей таблице показано, как маршрутизация Location-Based влияет на маршрутизацию исходящих вызовов в зависимости от расположения конечной точки вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="7df3a-107">The following table illustrates how Location-Based Routing affects the routing of outbound calls depending on the location of the caller’s endpoint.</span></span>

### <a name="caller-placing-an-outbound-call-to-the-pstn"></a><span data-ttu-id="7df3a-108">Абонент размещает исходящий звонок ТСОП</span><span class="sxs-lookup"><span data-stu-id="7df3a-108">Caller placing an outbound call to the PSTN</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="7df3a-109">Конечная точка пользователя расположена на сетевом сайте, для которого включена маршрутизация на основе расположения</span><span class="sxs-lookup"><span data-stu-id="7df3a-109">User endpoint located in a network site enabled for Location-Based Routing</span></span></th>
<th><span data-ttu-id="7df3a-110">Конечная точка пользователя расположена на неизвестном сетевом сайте или на сайте, для которого не включена маршрутизация на основе расположения</span><span class="sxs-lookup"><span data-stu-id="7df3a-110">User endpoint located in unknown network site or not enabled for Location-Based Routing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7df3a-111">Авторизация исходящих звонков</span><span class="sxs-lookup"><span data-stu-id="7df3a-111">Authorization of outbound calls</span></span></p></td>
<td><p><span data-ttu-id="7df3a-112">Звонок авторизован на основе политики голосовой связи пользователя</span><span class="sxs-lookup"><span data-stu-id="7df3a-112">Call is authorized based on user’s voice policy</span></span></p></td>
<td><p><span data-ttu-id="7df3a-113">Звонок авторизован на основе политики голосовой связи пользователя</span><span class="sxs-lookup"><span data-stu-id="7df3a-113">Call is authorized based on user’s voice policy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7df3a-114">Маршрутизация исходящего звонка</span><span class="sxs-lookup"><span data-stu-id="7df3a-114">Routing of outbound call</span></span></p></td>
<td><p><span data-ttu-id="7df3a-115">Звонок маршрутизируется в соответствии с политикой маршрутизации голосовой связи для данного сетевого сайта</span><span class="sxs-lookup"><span data-stu-id="7df3a-115">Call is routed according to the network site’s voice routing policy</span></span></p></td>
<td><p><span data-ttu-id="7df3a-116">Звонок маршрутизируется в соответствии с политикой голосовой связи пользователя и только через магистрали, для которых не включена маршрутизация на основе расположения (если они доступны)</span><span class="sxs-lookup"><span data-stu-id="7df3a-116">Call is routed according to user’s voice policy and only through trunks not enabled for Location-Based Routing (if available)</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="see-also"></a><span data-ttu-id="7df3a-117">См. также</span><span class="sxs-lookup"><span data-stu-id="7df3a-117">See Also</span></span>


[<span data-ttu-id="7df3a-118">Сценарии маршрутизации на основе местоположения в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7df3a-118">Scenarios for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-scenarios-for-location-based-routing.md)  
  

<span data-ttu-id="7df3a-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7df3a-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

