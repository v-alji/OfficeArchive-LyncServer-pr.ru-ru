---
title: 'Lync Server 2013: таблица AppSharingMetricsThreshold'
description: 'Таблица Lync Server 2013: AppSharingMetricsThreshold.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: AppSharingMetricsThreshold table
ms:assetid: 782cfab9-01a6-4843-aea1-28f47b0b51f7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205018(v=OCS.15)
ms:contentKeyID: 48184556
ms.date: 12/09/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 092c7d08026e6b736b81043a71b4ecaabc4d5f1b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439874"
---
# <a name="appsharingmetricsthreshold-table-in-lync-server-2013"></a><span data-ttu-id="49d1a-103">Таблица AppSharingMetricsThreshold в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="49d1a-103">AppSharingMetricsThreshold table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="49d1a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="49d1a-104">

<span> </span></span></span>

<span data-ttu-id="49d1a-105">_**Тема последнего изменения:** 2015-12-08_</span><span class="sxs-lookup"><span data-stu-id="49d1a-105">_**Topic Last Modified:** 2015-12-08_</span></span>

<span data-ttu-id="49d1a-106">В таблице AppSharingMetricsThreshold содержатся оптимальные и приемлемые значения для показателей качества взаимодействия, используемых совместно с приложением.</span><span class="sxs-lookup"><span data-stu-id="49d1a-106">The AppSharingMetricsThreshold table contains optimal and acceptable values for the Quality of Experience metrics used with application sharing.</span></span> <span data-ttu-id="49d1a-107">Эти пороговые значения используются, чтобы определить, следует ли классифицировать взаимодействие приложений как неудовлетворительные.</span><span class="sxs-lookup"><span data-stu-id="49d1a-107">These thresholds are used to determine if the application sharing experience should be classified as poor.</span></span>

<span data-ttu-id="49d1a-108">Эта таблица введена в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="49d1a-108">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="49d1a-109"><strong>Столбец</strong></span><span class="sxs-lookup"><span data-stu-id="49d1a-109"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="49d1a-110"><strong>Тип данных</strong></span><span class="sxs-lookup"><span data-stu-id="49d1a-110"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="49d1a-111"><strong>Ключ/индекс</strong></span><span class="sxs-lookup"><span data-stu-id="49d1a-111"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="49d1a-112"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="49d1a-112"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49d1a-113"><strong>CallType</strong></span><span class="sxs-lookup"><span data-stu-id="49d1a-113"><strong>CallType</strong></span></span></p></td>
<td><p><span data-ttu-id="49d1a-114">целое</span><span class="sxs-lookup"><span data-stu-id="49d1a-114">int</span></span></p></td>
<td><p><span data-ttu-id="49d1a-115">Primary</span><span class="sxs-lookup"><span data-stu-id="49d1a-115">Primary</span></span></p></td>
<td><p><span data-ttu-id="49d1a-116">Тип размещенного звонка.</span><span class="sxs-lookup"><span data-stu-id="49d1a-116">Type of call that was placed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49d1a-117"><strong>AppliedBandwidthLimitOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="49d1a-117"><strong>AppliedBandwidthLimitOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="49d1a-118">целое</span><span class="sxs-lookup"><span data-stu-id="49d1a-118">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="49d1a-119">Оптимальное ограничение пропускной способности для совместного использования приложений.</span><span class="sxs-lookup"><span data-stu-id="49d1a-119">Optimal bandwidth limitation for application sharing.</span></span> <span data-ttu-id="49d1a-120">Значение по умолчанию — 1000000.</span><span class="sxs-lookup"><span data-stu-id="49d1a-120">The default value is 1000000.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49d1a-121"><strong>AppliedBandwidthLimitAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="49d1a-121"><strong>AppliedBandwidthLimitAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="49d1a-122">целое</span><span class="sxs-lookup"><span data-stu-id="49d1a-122">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="49d1a-123">Допустимое ограничение пропускной способности для совместного использования приложений.</span><span class="sxs-lookup"><span data-stu-id="49d1a-123">Acceptable bandwidth limitation for application sharing.</span></span> <span data-ttu-id="49d1a-124">Значение по умолчанию — 500000.</span><span class="sxs-lookup"><span data-stu-id="49d1a-124">The default value is 500000.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49d1a-125"><strong>SpoiledTilePercentTotalOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="49d1a-125"><strong>SpoiledTilePercentTotalOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="49d1a-126">десятичное число (5; 2)</span><span class="sxs-lookup"><span data-stu-id="49d1a-126">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="49d1a-127">Оптимальная процентная ставка для плиток "spoiled" для классификации качества общего использования приложения.</span><span class="sxs-lookup"><span data-stu-id="49d1a-127">Optimal percentage rate for “spoiled” tiles for classifying an Application Sharing quality.</span></span> <span data-ttu-id="49d1a-128">Это значение — процент содержимого от общего доступа, которое не было доступно для просмотра.</span><span class="sxs-lookup"><span data-stu-id="49d1a-128">This value is the percentage of the content from the sharer that did not reach the viewer.</span></span> <span data-ttu-id="49d1a-129">Содержимое может быть удалено (или spoiled), когда общий доступ отбрасывает плитки из источника графики, или ASMCU плитки отбрасывают плитки от общего доступа, соответственно.</span><span class="sxs-lookup"><span data-stu-id="49d1a-129">Content may be discarded (or spoiled) when the sharer discards tiles from the graphics source or the ASMCU tiles discards tiles from Sharer respectively.</span></span> <span data-ttu-id="49d1a-130">Значение по умолчанию составляет 11 процентов.</span><span class="sxs-lookup"><span data-stu-id="49d1a-130">The default value is 11 percent.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49d1a-131"><strong>SpoiledTilePercentTotalAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="49d1a-131"><strong>SpoiledTilePercentTotalAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="49d1a-132">десятичное число (5; 2)</span><span class="sxs-lookup"><span data-stu-id="49d1a-132">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="49d1a-133">cceptable процентная ставка для плиток "spoiled" для классификации качества общего использования приложения.</span><span class="sxs-lookup"><span data-stu-id="49d1a-133">cceptable percentage rate for “spoiled” tiles for classifying an Application Sharing quality.</span></span> <span data-ttu-id="49d1a-134">Это значение — процент содержимого от общего доступа, которое не было доступно для просмотра.</span><span class="sxs-lookup"><span data-stu-id="49d1a-134">This value is the percentage of the content from the sharer that did not reach the viewer.</span></span> <span data-ttu-id="49d1a-135">Содержимое может быть удалено (или spoiled), когда общий доступ отбрасывает плитки из источника графики, или ASMCU плитки отбрасывают плитки от общего доступа, соответственно.</span><span class="sxs-lookup"><span data-stu-id="49d1a-135">Content may be discarded (or spoiled) when the sharer discards tiles from the graphics source or the ASMCU tiles discards tiles from Sharer respectively.</span></span> <span data-ttu-id="49d1a-136">Значение по умолчанию составляет 36%.</span><span class="sxs-lookup"><span data-stu-id="49d1a-136">The default value is 36 percent.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49d1a-137"><strong>JitterInterArrivalOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="49d1a-137"><strong>JitterInterArrivalOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="49d1a-138">целое</span><span class="sxs-lookup"><span data-stu-id="49d1a-138">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="49d1a-139">Этот столбец не используется в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="49d1a-139">This column is not used in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49d1a-140"><strong>JitterInterArrivalAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="49d1a-140"><strong>JitterInterArrivalAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="49d1a-141">целое</span><span class="sxs-lookup"><span data-stu-id="49d1a-141">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="49d1a-142">Этот столбец не используется в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="49d1a-142">This column is not used in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49d1a-143"><strong>RelativeOneWayBurstDensityOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="49d1a-143"><strong>RelativeOneWayBurstDensityOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="49d1a-144">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="49d1a-144">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="49d1a-145">Этот столбец не используется в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="49d1a-145">This column is not used in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49d1a-146"><strong>RelativeOneWayBurstDensityAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="49d1a-146"><strong>RelativeOneWayBurstDensityAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="49d1a-147">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="49d1a-147">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="49d1a-148">Этот столбец не используется в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="49d1a-148">This column is not used in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49d1a-149"><strong>RDPTileProcessingLatencyBurstDensityOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="49d1a-149"><strong>RDPTileProcessingLatencyBurstDensityOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="49d1a-150">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="49d1a-150">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="49d1a-151">Этот столбец не используется в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="49d1a-151">This column is not used in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49d1a-152"><strong>RDPTileProcessingLatencyBurstDensityAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="49d1a-152"><strong>RDPTileProcessingLatencyBurstDensityAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="49d1a-153">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="49d1a-153">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="49d1a-154">Этот столбец не используется в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="49d1a-154">This column is not used in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49d1a-155"><strong>RelativeOneWayAverageOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="49d1a-155"><strong>RelativeOneWayAverageOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="49d1a-156">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="49d1a-156">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="49d1a-157">Оптимальное значение для относительной односторонней задержки между двумя конечными точками мультимедиа, задействованными в общем доступе к приложению.</span><span class="sxs-lookup"><span data-stu-id="49d1a-157">Optimal value for the relative one-way delay between the two media endpoints involved in the application sharing.</span></span> <span data-ttu-id="49d1a-158">Это мера односкачковой задержки.</span><span class="sxs-lookup"><span data-stu-id="49d1a-158">This is a single-hop latency measure.</span></span> <span data-ttu-id="49d1a-159">Значение по умолчанию — 1,0 секунд.</span><span class="sxs-lookup"><span data-stu-id="49d1a-159">The default value is 1.0 seconds.</span></span></p>
<p><span data-ttu-id="49d1a-160">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="49d1a-160">The column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49d1a-161"><strong>RelativeOneWayAverageAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="49d1a-161"><strong>RelativeOneWayAverageAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="49d1a-162">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="49d1a-162">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="49d1a-163">Оптимальное значение для относительной односторонней задержки между двумя конечными точками мультимедиа, задействованными в общем доступе к приложению.</span><span class="sxs-lookup"><span data-stu-id="49d1a-163">Optimal value for the relative one-way delay between the two media endpoints involved in the application sharing.</span></span> <span data-ttu-id="49d1a-164">Это мера односкачковой задержки.</span><span class="sxs-lookup"><span data-stu-id="49d1a-164">This is a single-hop latency measure.</span></span> <span data-ttu-id="49d1a-165">Значение по умолчанию — 1,75 секунд.</span><span class="sxs-lookup"><span data-stu-id="49d1a-165">The default value is 1.75 seconds.</span></span></p>
<p><span data-ttu-id="49d1a-166">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="49d1a-166">The column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49d1a-167"><strong>RDPTileProcessingLatencyAverageOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="49d1a-167"><strong>RDPTileProcessingLatencyAverageOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="49d1a-168">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="49d1a-168">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="49d1a-169">Оптимальное значение средней задержки обработки плитки RDP на сервере конференций в течение сеанса просмотра.</span><span class="sxs-lookup"><span data-stu-id="49d1a-169">Optimal value of the average RDP tile processing latency in the AS Conferencing Server over the duration of the viewing session.</span></span> <span data-ttu-id="49d1a-170">Задержка — это разница во времени между моментом, когда начальный кадр кодируется на сервере (в зависимости от сценария, или MCU, а также с помощью того же начального кадра декодируется в средстве просмотра).</span><span class="sxs-lookup"><span data-stu-id="49d1a-170">Latency is the time difference between when the Start Frame is encoded on the server (sharer or MCU depending on the scenario) and the same Start Frame is decoded on the viewer.</span></span></p>
<p><span data-ttu-id="49d1a-171">Высокое среднее значение отражает более длительную задержку при просмотре.</span><span class="sxs-lookup"><span data-stu-id="49d1a-171">A high average reflects a longer delay in the viewing experience.</span></span> <span data-ttu-id="49d1a-172">На перегруженном сервере конференц-связи могут происходить в среднем более длительные задержки.</span><span class="sxs-lookup"><span data-stu-id="49d1a-172">An overloaded conferencing server may experience higher average delays.</span></span> <span data-ttu-id="49d1a-173">Значением по умолчанию является 200ms.</span><span class="sxs-lookup"><span data-stu-id="49d1a-173">The default value is 200ms.</span></span></p>
<p><span data-ttu-id="49d1a-174">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="49d1a-174">The column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49d1a-175"><strong>RDPTileProcessingLatencyAverageAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="49d1a-175"><strong>RDPTileProcessingLatencyAverageAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="49d1a-176">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="49d1a-176">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="49d1a-177">Допустимое значение средней задержки обработки плитки RDP на сервере конференций в течение сеанса просмотра.</span><span class="sxs-lookup"><span data-stu-id="49d1a-177">Acceptable value of the average RDP tile processing latency in the AS Conferencing Server over the duration of the viewing session.</span></span> <span data-ttu-id="49d1a-178">Задержка — это разница во времени между моментом, когда начальный кадр кодируется на сервере (в зависимости от сценария, или MCU, а также с помощью того же начального кадра декодируется в средстве просмотра).</span><span class="sxs-lookup"><span data-stu-id="49d1a-178">Latency is the time difference between when the Start Frame is encoded on the server (sharer or MCU depending on the scenario) and the same Start Frame is decoded on the viewer.</span></span></p>
<p><span data-ttu-id="49d1a-179">Высокое среднее значение отражает более длительную задержку при просмотре.</span><span class="sxs-lookup"><span data-stu-id="49d1a-179">A high average reflects a longer delay in the viewing experience.</span></span> <span data-ttu-id="49d1a-180">На перегруженном сервере конференц-связи могут происходить в среднем более длительные задержки.</span><span class="sxs-lookup"><span data-stu-id="49d1a-180">An overloaded conferencing server may experience higher average delays.</span></span> <span data-ttu-id="49d1a-181">Значением по умолчанию является 200ms.</span><span class="sxs-lookup"><span data-stu-id="49d1a-181">The default value is 200ms.</span></span></p>
<p><span data-ttu-id="49d1a-182">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="49d1a-182">The column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="49d1a-183">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="49d1a-183">


</div>

<span> </span>

</div>

</div>

</span></span></div>

