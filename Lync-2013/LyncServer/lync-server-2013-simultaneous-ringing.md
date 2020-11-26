---
title: 'Lync Server 2013: одновременный звонок'
description: 'Lync Server 2013: Одновременный звонок.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Simultaneous ringing
ms:assetid: df02f919-4d50-4832-9300-6c51f8b4fc56
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994079(v=OCS.15)
ms:contentKeyID: 51803990
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 595c8c1d4ce105e2189002f18733ffae92cff8bf
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423822"
---
# <a name="simultaneous-ringing-in-lync-server-2013"></a><span data-ttu-id="3e59c-103">Одновременный звонок в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3e59c-103">Simultaneous ringing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3e59c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3e59c-104">

<span> </span></span></span>

<span data-ttu-id="3e59c-105">_**Тема последнего изменения:** 2013-03-09_</span><span class="sxs-lookup"><span data-stu-id="3e59c-105">_**Topic Last Modified:** 2013-03-09_</span></span>

<span data-ttu-id="3e59c-106">Если у вызывающего абонента есть одновременные звонки, Location-Based маршрутизация анализирует расположение вызывающего абонента и конечных точек вызываемого абонента, чтобы определить, следует ли маршрутизировать звонок.</span><span class="sxs-lookup"><span data-stu-id="3e59c-106">When the called party has simultaneous ringing enabled, Location-Based Routing analyzes the location of the calling party and the endpoints of the called parties to determine whether the call should be routed.</span></span>

<span data-ttu-id="3e59c-107">В нижеприведенной таблице продемонстрированы варианты ситуации для пользователя, у которого настроен одновременный звонок, и различных типов вызываемых абонентов (пользователя в том же сайте сети, в другом сайте сети или на неизвестном сайте).</span><span class="sxs-lookup"><span data-stu-id="3e59c-107">The following table illustrates a user configured with simultaneous ringing, and the simultaneous ringing target is a user in the same network site, in a different network site, or in an unknown network site.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3e59c-108">Входящий звонок ТСОП для абонента</span><span class="sxs-lookup"><span data-stu-id="3e59c-108">Incoming PSTN call for</span></span></th>
<th><span data-ttu-id="3e59c-109">на том же сетевом сайте, что и вызываемый абонент;</span><span class="sxs-lookup"><span data-stu-id="3e59c-109">Located in the same network site as callee</span></span></th>
<th><span data-ttu-id="3e59c-110">на сетевом сайте, отличном от сайта вызываемого абонента;</span><span class="sxs-lookup"><span data-stu-id="3e59c-110">Located in different network site than callee</span></span></th>
<th><span data-ttu-id="3e59c-111">Размещен на неизвестном сетевом сайте или не включен для маршрутизации Location-Based</span><span class="sxs-lookup"><span data-stu-id="3e59c-111">Located in unknown network site or not enabled for Location-Based Routing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3e59c-112">Пользователь Lync</span><span class="sxs-lookup"><span data-stu-id="3e59c-112">Lync user</span></span></p></td>
<td><p><span data-ttu-id="3e59c-113">Одновременный вызов разрешен</span><span class="sxs-lookup"><span data-stu-id="3e59c-113">Simultaneous ring allowed</span></span></p></td>
<td><p><span data-ttu-id="3e59c-114">Одновременный вызов не разрешен</span><span class="sxs-lookup"><span data-stu-id="3e59c-114">Simultaneous ring not allowed</span></span></p></td>
<td><p><span data-ttu-id="3e59c-115">Одновременный вызов не разрешен</span><span class="sxs-lookup"><span data-stu-id="3e59c-115">Simultaneous ring not allowed</span></span></p></td>
</tr>
</tbody>
</table>

  
<span data-ttu-id="3e59c-116">В следующей таблице показан вызов из пользователя Lync (например, вызывающего абонента Lync) на том же сайте сети, на другом сайте сети или неизвестном сетевому сайту.</span><span class="sxs-lookup"><span data-stu-id="3e59c-116">The following table illustrates a call from a Lync user (i.e. Lync caller) in the same network site, in a different network site, or from an unknown network site.</span></span> <span data-ttu-id="3e59c-117">Конечная точка ТСОП вызываемого абонента (т. е. мобильный телефон) настроена как место назначения для одновременного поступления вызова.</span><span class="sxs-lookup"><span data-stu-id="3e59c-117">The callee has a PSTN endpoint (i.e. cellphone) configured as a simultaneous ring target.</span></span> <span data-ttu-id="3e59c-118">В этом сценарии Location-Based маршрутизация определит, нужно ли перенаправлять вызов в цель одновременных звонков (например, телефона) вызываемого абонента.</span><span class="sxs-lookup"><span data-stu-id="3e59c-118">In this scenario, Location-Based Routing will determine whether the call should be routed to the simultaneous ring target (i.e. cellphone) of the callee or not.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3e59c-119">Цель одновременного вызова</span><span class="sxs-lookup"><span data-stu-id="3e59c-119">Simultaneous ring target</span></span></th>
<th><span data-ttu-id="3e59c-120">на том же сетевом сайте, что и вызываемый абонент;</span><span class="sxs-lookup"><span data-stu-id="3e59c-120">Located in the same network site as callee</span></span></th>
<th><span data-ttu-id="3e59c-121">на сетевом сайте, отличном от сайта вызываемого абонента;</span><span class="sxs-lookup"><span data-stu-id="3e59c-121">Located in different network site than callee</span></span></th>
<th><span data-ttu-id="3e59c-122">Размещен на неизвестном сетевом сайте или не включен для маршрутизации Location-Based</span><span class="sxs-lookup"><span data-stu-id="3e59c-122">Located in unknown network site or not enabled for Location-Based Routing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3e59c-123">Конечная точка ТСОП</span><span class="sxs-lookup"><span data-stu-id="3e59c-123">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="3e59c-124">Одновременный вызов разрешен политикой маршрутизации голосовой связи сайта вызывающего абонента</span><span class="sxs-lookup"><span data-stu-id="3e59c-124">Simultaneous ring allowed through the caller’s site voice routing policy</span></span></p></td>
<td><p><span data-ttu-id="3e59c-125">Одновременный вызов разрешен политикой маршрутизации голосовой связи сайта вызывающего абонента</span><span class="sxs-lookup"><span data-stu-id="3e59c-125">Simultaneous ring allowed through the caller’s site voice routing policy</span></span></p></td>
<td><p><span data-ttu-id="3e59c-126">Одновременный вызов разрешен политикой голосовой связи вызывающего абонента на магистральные каналы, для которых не включена маршрутизация на основе местоположения</span><span class="sxs-lookup"><span data-stu-id="3e59c-126">Simultaneous ring allowed through the caller’s voice policy to trunks not enabled for Location-Based Routing</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="see-also"></a><span data-ttu-id="3e59c-127">См. также</span><span class="sxs-lookup"><span data-stu-id="3e59c-127">See Also</span></span>


[<span data-ttu-id="3e59c-128">Сценарии маршрутизации на основе местоположения в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3e59c-128">Scenarios for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-scenarios-for-location-based-routing.md)  
  

<span data-ttu-id="3e59c-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3e59c-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

