---
title: 'Lync Server 2013: таблица использованием Traceroute'
description: 'Таблица Lync Server 2013: использованием Traceroute.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: TraceRoute table
ms:assetid: b9493cef-6ece-4f13-bf68-dbf132aab4f4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205205(v=OCS.15)
ms:contentKeyID: 48185242
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8af33e572065fbab1eaaaef684997e7f95edaed9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440838"
---
# <a name="traceroute-table-in-lync-server-2013"></a><span data-ttu-id="9099c-103">Таблица использованием Traceroute в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9099c-103">TraceRoute table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9099c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9099c-104">

<span> </span></span></span>

<span data-ttu-id="9099c-105">_**Тема последнего изменения:** 2014-02-21_</span><span class="sxs-lookup"><span data-stu-id="9099c-105">_**Topic Last Modified:** 2014-02-21_</span></span>

<span data-ttu-id="9099c-106">В таблице использованием Traceroute содержатся сведения о маршрутизации из звонков.</span><span class="sxs-lookup"><span data-stu-id="9099c-106">The TraceRoute table contains routing information from calls.</span></span> <span data-ttu-id="9099c-107">Эта таблица введена в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="9099c-107">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9099c-108"><strong>Столбец</strong></span><span class="sxs-lookup"><span data-stu-id="9099c-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="9099c-109"><strong>Тип данных</strong></span><span class="sxs-lookup"><span data-stu-id="9099c-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="9099c-110"><strong>Ключ/индекс</strong></span><span class="sxs-lookup"><span data-stu-id="9099c-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="9099c-111"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="9099c-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9099c-112"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="9099c-112"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="9099c-113">datetime</span><span class="sxs-lookup"><span data-stu-id="9099c-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="9099c-114">Основной, внешний</span><span class="sxs-lookup"><span data-stu-id="9099c-114">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="9099c-115">Дата и время начала звонка.</span><span class="sxs-lookup"><span data-stu-id="9099c-115">Date and time that the call began.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9099c-116"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="9099c-116"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="9099c-117">целое</span><span class="sxs-lookup"><span data-stu-id="9099c-117">int</span></span></p></td>
<td><p><span data-ttu-id="9099c-118">Основной, внешний</span><span class="sxs-lookup"><span data-stu-id="9099c-118">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="9099c-119">Уникальный идентификатор, который используется для различения нескольких звонков, которые могли приступили к одной и той же дате и в то же время.</span><span class="sxs-lookup"><span data-stu-id="9099c-119">Unique identifier used to distinguish between multiple calls that might have begun on the same date and at the same time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9099c-120"><strong>MediaLineLabel</strong></span><span class="sxs-lookup"><span data-stu-id="9099c-120"><strong>MediaLineLabel</strong></span></span></p></td>
<td><p><span data-ttu-id="9099c-121">tinyint</span><span class="sxs-lookup"><span data-stu-id="9099c-121">tinyint</span></span></p></td>
<td><p><span data-ttu-id="9099c-122">Основной, внешний</span><span class="sxs-lookup"><span data-stu-id="9099c-122">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="9099c-123">Представляет тип видеостроки, используемой в звонке.</span><span class="sxs-lookup"><span data-stu-id="9099c-123">Represents the type of video line used in the call.</span></span> <span data-ttu-id="9099c-124">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="9099c-124">Allowed values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="9099c-125">0 – звук</span><span class="sxs-lookup"><span data-stu-id="9099c-125">0 – Audio</span></span></p></li>
<li><p><span data-ttu-id="9099c-126">1 – видео</span><span class="sxs-lookup"><span data-stu-id="9099c-126">1 – Video</span></span></p></li>
<li><p><span data-ttu-id="9099c-127">2 — панорамное видео</span><span class="sxs-lookup"><span data-stu-id="9099c-127">2 – Panoramic video</span></span></p></li>
<li><p><span data-ttu-id="9099c-128">3 — общий доступ к приложениям и рабочим столам</span><span class="sxs-lookup"><span data-stu-id="9099c-128">3 – Application/Desktop sharing</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9099c-129"><strong>FromCaller</strong></span><span class="sxs-lookup"><span data-stu-id="9099c-129"><strong>FromCaller</strong></span></span></p></td>
<td><p><span data-ttu-id="9099c-130">бит</span><span class="sxs-lookup"><span data-stu-id="9099c-130">bit</span></span></p></td>
<td><p><span data-ttu-id="9099c-131">Primary</span><span class="sxs-lookup"><span data-stu-id="9099c-131">Primary</span></span></p></td>
<td><p><span data-ttu-id="9099c-132">Конечная точка, в которой был помещен звонок.</span><span class="sxs-lookup"><span data-stu-id="9099c-132">Endpoint that placed the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9099c-133"><strong>Участк</strong></span><span class="sxs-lookup"><span data-stu-id="9099c-133"><strong>Hop</strong></span></span></p></td>
<td><p><span data-ttu-id="9099c-134">целое</span><span class="sxs-lookup"><span data-stu-id="9099c-134">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="9099c-135">Транзитный сетевой переход/</span><span class="sxs-lookup"><span data-stu-id="9099c-135">Network hop/</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9099c-136"><strong>IPAddressKey</strong></span><span class="sxs-lookup"><span data-stu-id="9099c-136"><strong>IPAddressKey</strong></span></span></p></td>
<td><p><span data-ttu-id="9099c-137">целое</span><span class="sxs-lookup"><span data-stu-id="9099c-137">int</span></span></p></td>
<td><p><span data-ttu-id="9099c-138">Другом</span><span class="sxs-lookup"><span data-stu-id="9099c-138">Foreign</span></span></p></td>
<td><p><span data-ttu-id="9099c-139">Уникальный идентификатор IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="9099c-139">Unique identifier for the IP address.</span></span> <span data-ttu-id="9099c-140">Информация об IP-адресах хранится в <a href="lync-server-2013-ipaddress-table.md">таблице IPAddress в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="9099c-140">IP address information is stored in the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9099c-141"><strong>ПЕРЕДАЧИ</strong></span><span class="sxs-lookup"><span data-stu-id="9099c-141"><strong>RTT</strong></span></span></p></td>
<td><p><span data-ttu-id="9099c-142">целое</span><span class="sxs-lookup"><span data-stu-id="9099c-142">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="9099c-143">Время обмена данными.</span><span class="sxs-lookup"><span data-stu-id="9099c-143">Roundtrip time.</span></span> <span data-ttu-id="9099c-144">Время для обмена данными измеряет время, затрачиваемое на передачу голосового пакета получателю, а затем отправляет уведомление о том, что оно получено.</span><span class="sxs-lookup"><span data-stu-id="9099c-144">The roundtrip time measures the amount of time it takes for a voice packet to reach its destination and then send back notification that it was received.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="9099c-145">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9099c-145">


</div>

<span> </span>

</div>

</div>

</span></span></div>

