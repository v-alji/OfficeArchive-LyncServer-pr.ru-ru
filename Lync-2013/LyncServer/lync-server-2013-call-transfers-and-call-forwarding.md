---
title: 'Lync Server 2013: переключение и переадресация звонков'
description: 'Lync Server 2013: передача звонков и переадресация звонков.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Call transfers and call forwarding
ms:assetid: 978610ec-63c7-4cf6-ad7a-9ef91559bf12
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994051(v=OCS.15)
ms:contentKeyID: 51803962
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d9359cb64b386d022eab33e4523dfaccf784075b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435686"
---
# <a name="call-transfers-and-call-forwarding-in-lync-server-2013"></a><span data-ttu-id="9f94e-103">Переключение и переадресация звонков в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9f94e-103">Call transfers and call forwarding in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9f94e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9f94e-104">

<span> </span></span></span>

<span data-ttu-id="9f94e-105">_**Тема последнего изменения:** 2013-03-09_</span><span class="sxs-lookup"><span data-stu-id="9f94e-105">_**Topic Last Modified:** 2013-03-09_</span></span>

<span data-ttu-id="9f94e-106">При использовании конечной точки PSTN Location-Based служба маршрутизации анализирует расположение конечной точки лиственничный и конечную точку, в которую передается или пересылается звонок (например, передача и переадресация).</span><span class="sxs-lookup"><span data-stu-id="9f94e-106">When a PSTN endpoint is involved, Location-Based Routing analyzes the location of the calle’s endpoint and the endpoint where the call will be transferred or forwarded to (i.e. transfer/forward target).</span></span> <span data-ttu-id="9f94e-107">Location-Based маршрутизации определяет, следует ли передавать или пересылать Звонок в зависимости от расположения обеих конечных точек.</span><span class="sxs-lookup"><span data-stu-id="9f94e-107">Location-Based Routing determines whether the call should be transferred or forwarded depending on the location of both endpoints.</span></span>

<span data-ttu-id="9f94e-108">В приведенной ниже таблице показан сценарий пользователя Lync в звонке с конечной точкой PSTN, и пользователь Lync передает звонок другому пользователю Lync.</span><span class="sxs-lookup"><span data-stu-id="9f94e-108">The following table illustrates the scenario of a Lync user in a call with a PSTN endpoint, and the Lync user transfers the call to another Lync user.</span></span> <span data-ttu-id="9f94e-109">В зависимости от расположения сетевого сайта для конечной точки получателя, Location-Based маршрутизация влияет на маршрут перемещения и переадресации звонков.</span><span class="sxs-lookup"><span data-stu-id="9f94e-109">Depending on the network site location of the transferee’s endpoint, Location-Based Routing affects the routing of the call transfer or forward.</span></span>

### <a name="initiating-call-transfer-or-forward"></a><span data-ttu-id="9f94e-110">Инициирование переключения или переадресации звонка</span><span class="sxs-lookup"><span data-stu-id="9f94e-110">Initiating call transfer or forward</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9f94e-111">Пользователь, инициирующий переключение или переадресацию звонка</span><span class="sxs-lookup"><span data-stu-id="9f94e-111">User initiating the call transfer/forward</span></span></th>
<th><span data-ttu-id="9f94e-112">Целевая конечная точка расположена на том же сетевом сайте, что и пользователь, инициирующий переключение или переадресацию звонка</span><span class="sxs-lookup"><span data-stu-id="9f94e-112">Target endpoint is in same network site as user initiating call transfer or forward</span></span></th>
<th><span data-ttu-id="9f94e-113">Целевая конечная точка расположена на сетевом сайте, отличном от того, где находится пользователь, инициирующий переключение или переадресацию звонка</span><span class="sxs-lookup"><span data-stu-id="9f94e-113">Target endpoint is in different network site as user initiating call transfer or forward</span></span></th>
<th><span data-ttu-id="9f94e-114">Целевая конечная точка находится в неизвестном сетевом сайте или на сайте сети не включена маршрутизация Location-Based</span><span class="sxs-lookup"><span data-stu-id="9f94e-114">Target endpoint is in unknown network site or network site not enabled for Location-Based Routing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9f94e-115">Пользователь Lync</span><span class="sxs-lookup"><span data-stu-id="9f94e-115">Lync user</span></span></p></td>
<td><p><span data-ttu-id="9f94e-116">Переключение или переадресация звонка разрешены</span><span class="sxs-lookup"><span data-stu-id="9f94e-116">Call forward or transfer is allowed</span></span></p></td>
<td><p><span data-ttu-id="9f94e-117">Переключение или переадресация звонка не разрешены</span><span class="sxs-lookup"><span data-stu-id="9f94e-117">Call forward or transfer is not allowed</span></span></p></td>
<td><p><span data-ttu-id="9f94e-118">Переключение или переадресация звонка не разрешены</span><span class="sxs-lookup"><span data-stu-id="9f94e-118">Call forward or transfer is not allowed</span></span></p></td>
</tr>
</tbody>
</table>

  

<span data-ttu-id="9f94e-119">Например: пользователь Lync в звонке с конечной точкой PSTN передает звонок другому пользователю Lync, который находится на том же сайте сети.</span><span class="sxs-lookup"><span data-stu-id="9f94e-119">For example: a Lync user in a call with a PSTN endpoint transfers the call to another Lync user that is in the same network site.</span></span> <span data-ttu-id="9f94e-120">В этом случае переключение звонка разрешено.</span><span class="sxs-lookup"><span data-stu-id="9f94e-120">In this case, the call transfer is allowed.</span></span>

<span data-ttu-id="9f94e-121">В приведенной ниже таблице показан сценарий пользователя Lync в вызове с другим пользователем Lync, а один из пользователей передает Звонок в конечную точку PSTN.</span><span class="sxs-lookup"><span data-stu-id="9f94e-121">The following table illustrates the scenario of a Lync user in a call with another Lync user, and one of the users transfers the call to a PSTN endpoint.</span></span> <span data-ttu-id="9f94e-122">В таблице подробно показано, как маршрутизация на основе расположения обрабатывает звонок в зависимости от расположения пользователя, на которого переключается этот звонок.</span><span class="sxs-lookup"><span data-stu-id="9f94e-122">Depending on the location of the user the call is being transferred to, the table details how Location-Based Routing affects the call.</span></span>

### <a name="call-transfer-or-forward-to-pstn-endpoint"></a><span data-ttu-id="9f94e-123">Переключение или переадресация звонка на конечную точку ТСОП</span><span class="sxs-lookup"><span data-stu-id="9f94e-123">Call transfer or forward to PSTN endpoint</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9f94e-124">Целевая конечная точка переключения/переадресации звонка</span><span class="sxs-lookup"><span data-stu-id="9f94e-124">Call transfer/forward endpoint target</span></span></th>
<th><span data-ttu-id="9f94e-125">Пользователи Lync на одном и том же сайте сети</span><span class="sxs-lookup"><span data-stu-id="9f94e-125">Lync users in same network site</span></span></th>
<th><span data-ttu-id="9f94e-126">Пользователи Lync на разных сетевых сайтах</span><span class="sxs-lookup"><span data-stu-id="9f94e-126">Lync users in different network sites</span></span></th>
<th><span data-ttu-id="9f94e-127">Один или оба пользователя Lync на неизвестном сетевом сайте или сайте сети не включены для маршрутизации Location-Based</span><span class="sxs-lookup"><span data-stu-id="9f94e-127">One or both Lync users in unknown network site or network site not enabled for Location-Based Routing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9f94e-128">Конечная точка ТСОП</span><span class="sxs-lookup"><span data-stu-id="9f94e-128">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="9f94e-129">Переключение или переадресация звонка разрешены политикой маршрутизации голосовых звонков сайта передаваемого пользователя</span><span class="sxs-lookup"><span data-stu-id="9f94e-129">Call forward or transfer allowed by the transferred user’s site voice routing policy</span></span></p></td>
<td><p><span data-ttu-id="9f94e-130">Переключение или переадресация звонка разрешены политикой маршрутизации голосовых звонков сайта передаваемого пользователя</span><span class="sxs-lookup"><span data-stu-id="9f94e-130">Call forward or transfer allowed by the transferred user’s site voice routing policy</span></span></p></td>
<td><p><span data-ttu-id="9f94e-131">Переключение или переадресация звонка разрешены политикой маршрутизации голосовых звонков передаваемого пользователя, но только через магистрали, для которых не включена маршрутизация на основе расположения</span><span class="sxs-lookup"><span data-stu-id="9f94e-131">Call forward or transfer allowed by the transferred user’s voice policy only through trunks not enabled for Location-Based Routing</span></span></p></td>
</tr>
</tbody>
</table>

  
<span data-ttu-id="9f94e-132">Например: пользователь Lync в звонке с другим пользователем Lync, который находится на том же сайте сети, передает Звонок в конечную точку PSTN, и передача вызова разрешена.</span><span class="sxs-lookup"><span data-stu-id="9f94e-132">For example: a Lync user in a call with another Lync user that is in the same network site transfers the call to a PSTN endpoint and the call transfer is allowed.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="9f94e-133">См. также</span><span class="sxs-lookup"><span data-stu-id="9f94e-133">See Also</span></span>


[<span data-ttu-id="9f94e-134">Сценарии маршрутизации на основе местоположения в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9f94e-134">Scenarios for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-scenarios-for-location-based-routing.md)  
  

<span data-ttu-id="9f94e-135"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9f94e-135"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

