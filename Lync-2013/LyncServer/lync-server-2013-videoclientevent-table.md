---
title: 'Lync Server 2013: таблица VideoClientEvent'
description: 'Таблица Lync Server 2013: VideoClientEvent.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: VideoClientEvent table
ms:assetid: e8ab963b-fe1d-45b3-b9bd-66a5f44c1629
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399039(v=OCS.15)
ms:contentKeyID: 48185891
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ae73ac2548e838241febe60a2d31f80983b01de5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399997"
---
# <a name="videoclientevent-table-in-lync-server-2013"></a><span data-ttu-id="911ff-103">Таблица VideoClientEvent в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="911ff-103">VideoClientEvent table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="911ff-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="911ff-104">

<span> </span></span></span>

<span data-ttu-id="911ff-105">_**Тема последнего изменения:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="911ff-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="911ff-106">Каждая запись имеет событие клиента для одной конечной точки во время видеозвонка.</span><span class="sxs-lookup"><span data-stu-id="911ff-106">Each record contains client event for one endpoint in a video call.</span></span> <span data-ttu-id="911ff-107">Обычно один звонок состоит из двух записей: одного для вызывающего и для вызываемого абонента.</span><span class="sxs-lookup"><span data-stu-id="911ff-107">Usually, one call has two records, one for caller and one for callee.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="911ff-108"><strong>Столбец</strong></span><span class="sxs-lookup"><span data-stu-id="911ff-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="911ff-109"><strong>Тип данных</strong></span><span class="sxs-lookup"><span data-stu-id="911ff-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="911ff-110"><strong>Ключ/индекс</strong></span><span class="sxs-lookup"><span data-stu-id="911ff-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="911ff-111"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="911ff-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="911ff-112"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="911ff-112"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="911ff-113">datetime</span><span class="sxs-lookup"><span data-stu-id="911ff-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="911ff-114">Primary</span><span class="sxs-lookup"><span data-stu-id="911ff-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="911ff-115">На которую ссылается <a href="lync-server-2013-medialine-table.md">Таблица MediaLine в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="911ff-115">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="911ff-116"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="911ff-116"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="911ff-117">целое</span><span class="sxs-lookup"><span data-stu-id="911ff-117">int</span></span></p></td>
<td><p><span data-ttu-id="911ff-118">Primary</span><span class="sxs-lookup"><span data-stu-id="911ff-118">Primary</span></span></p></td>
<td><p><span data-ttu-id="911ff-119">На которую ссылается <a href="lync-server-2013-medialine-table.md">Таблица MediaLine в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="911ff-119">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="911ff-120"><strong>MediaLineLabel</strong></span><span class="sxs-lookup"><span data-stu-id="911ff-120"><strong>MediaLineLabel</strong></span></span></p></td>
<td><p><span data-ttu-id="911ff-121">tinyint</span><span class="sxs-lookup"><span data-stu-id="911ff-121">tinyint</span></span></p></td>
<td><p><span data-ttu-id="911ff-122">Primary</span><span class="sxs-lookup"><span data-stu-id="911ff-122">Primary</span></span></p></td>
<td><p><span data-ttu-id="911ff-123">На которую ссылается <a href="lync-server-2013-medialine-table.md">Таблица MediaLine в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="911ff-123">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="911ff-124"><strong>FromCaller</strong></span><span class="sxs-lookup"><span data-stu-id="911ff-124"><strong>FromCaller</strong></span></span></p></td>
<td><p><span data-ttu-id="911ff-125">бит</span><span class="sxs-lookup"><span data-stu-id="911ff-125">bit</span></span></p></td>
<td><p><span data-ttu-id="911ff-126">Primary</span><span class="sxs-lookup"><span data-stu-id="911ff-126">Primary</span></span></p></td>
<td><p><span data-ttu-id="911ff-127">0: данные вызывающего абонента</span><span class="sxs-lookup"><span data-stu-id="911ff-127">0: Callee’s data</span></span></p>
<p><span data-ttu-id="911ff-128">1: данные вызывающего абонента</span><span class="sxs-lookup"><span data-stu-id="911ff-128">1: Caller’s data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="911ff-129"><strong>NetworkBandwidthLowEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="911ff-129"><strong>NetworkBandwidthLowEventRatio</strong></span></span></p></td>
<td></td>
<td><p> </p></td>
<td><p><span data-ttu-id="911ff-130">Процент сеанса, когда событие LowBandwidth было инициировано для состояния "Bad".</span><span class="sxs-lookup"><span data-stu-id="911ff-130">Percentage of session the LowBandwidth event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="911ff-131">Доступная пропускная способность недостаточна для приемлемого голосового интерфейса.</span><span class="sxs-lookup"><span data-stu-id="911ff-131">The available bandwidth is insufficient for an acceptable voice experience.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="911ff-132"><strong>NetworkReceiveQualityEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="911ff-132"><strong>NetworkReceiveQualityEventRatio</strong></span></span></p></td>
<td></td>
<td><p> </p></td>
<td><p><span data-ttu-id="911ff-133">Процент сеанса, когда событие ReceiveSendQuality было инициировано для состояния "Bad".</span><span class="sxs-lookup"><span data-stu-id="911ff-133">Percentage of session the ReceiveSendQuality event was fired for ‘Bad’ state.</span></span></p>
<p><span data-ttu-id="911ff-134">Качество сети в условиях нарушения или потери пакетов является существенным и влияет на качество получаемого звука.</span><span class="sxs-lookup"><span data-stu-id="911ff-134">Network quality in terms of jitter or packet loss is severe and impacts the quality of audio being received.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="911ff-135">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="911ff-135">


</div>

<span> </span>

</div>

</div>

</span></span></div>

