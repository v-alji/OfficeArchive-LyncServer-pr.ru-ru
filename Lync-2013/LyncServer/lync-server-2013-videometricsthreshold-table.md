---
title: 'Lync Server 2013: таблица VideoMetricsThreshold'
description: 'Таблица Lync Server 2013: VideoMetricsThreshold.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: VideoMetricsThreshold table
ms:assetid: 2e2f4711-35ba-48c6-b15b-5aba61c4eb75
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204778(v=OCS.15)
ms:contentKeyID: 48183736
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 93cdd6fb4c3c54ac1470499490f36fee87ba283d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438871"
---
# <a name="videometricsthreshold-table-in-lync-server-2013"></a><span data-ttu-id="d2451-103">Таблица VideoMetricsThreshold в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d2451-103">VideoMetricsThreshold table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d2451-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d2451-104">

<span> </span></span></span>

<span data-ttu-id="d2451-105">_**Тема последнего изменения:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="d2451-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="d2451-106">Таблица VideoMetricsThreshold имеет оптимальные и приемлемые значения для показателей качества взаимодействия, используемых с видеозвонками.</span><span class="sxs-lookup"><span data-stu-id="d2451-106">The VideoMetricsThreshold table contains optimal and acceptable values for the Quality of Experience metrics used with video calls.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d2451-107"><strong>Столбец</strong></span><span class="sxs-lookup"><span data-stu-id="d2451-107"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="d2451-108"><strong>Тип данных</strong></span><span class="sxs-lookup"><span data-stu-id="d2451-108"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="d2451-109"><strong>Ключ/индекс</strong></span><span class="sxs-lookup"><span data-stu-id="d2451-109"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="d2451-110"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="d2451-110"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d2451-111"><strong>CallType</strong></span><span class="sxs-lookup"><span data-stu-id="d2451-111"><strong>CallType</strong></span></span></p></td>
<td><p><span data-ttu-id="d2451-112">целое</span><span class="sxs-lookup"><span data-stu-id="d2451-112">int</span></span></p></td>
<td><p><span data-ttu-id="d2451-113">Primary</span><span class="sxs-lookup"><span data-stu-id="d2451-113">Primary</span></span></p></td>
<td><p><span data-ttu-id="d2451-114">Тип размещенного звонка.</span><span class="sxs-lookup"><span data-stu-id="d2451-114">Type of call that was placed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2451-115"><strong>VideoPostFECPLROptimal</strong></span><span class="sxs-lookup"><span data-stu-id="d2451-115"><strong>VideoPostFECPLROptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="d2451-116">десятичное число (5; 2)</span><span class="sxs-lookup"><span data-stu-id="d2451-116">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d2451-117">Значение по умолчанию — 0,05.</span><span class="sxs-lookup"><span data-stu-id="d2451-117">The default value is 0.05.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2451-118"><strong>VideoPostFECPLRAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="d2451-118"><strong>VideoPostFECPLRAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="d2451-119">десятичное число (5; 2)</span><span class="sxs-lookup"><span data-stu-id="d2451-119">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d2451-120">Значение по умолчанию — 0,10.</span><span class="sxs-lookup"><span data-stu-id="d2451-120">The default value is 0.10.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2451-121"><strong>VideoLocalFrameLostPercentageAverageOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="d2451-121"><strong>VideoLocalFrameLostPercentageAverageOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="d2451-122">десятичное число (5; 2)</span><span class="sxs-lookup"><span data-stu-id="d2451-122">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d2451-123">Значение по умолчанию — 5,0.</span><span class="sxs-lookup"><span data-stu-id="d2451-123">The default value is 5.0.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2451-124"><strong>VideoLocalFrameLostPercentageAverageAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="d2451-124"><strong>VideoLocalFrameLostPercentageAverageAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="d2451-125">десятичное число (5; 2)</span><span class="sxs-lookup"><span data-stu-id="d2451-125">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d2451-126">Значение по умолчанию — 10,0.</span><span class="sxs-lookup"><span data-stu-id="d2451-126">The default value is 10.0.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2451-127"><strong>RecvFrameRateAverageOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="d2451-127"><strong>RecvFrameRateAverageOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="d2451-128">десятичное число (9; 4)</span><span class="sxs-lookup"><span data-stu-id="d2451-128">decimal(9,4)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d2451-129">Значение по умолчанию — 12,0000.</span><span class="sxs-lookup"><span data-stu-id="d2451-129">The default value is 12.0000.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2451-130"><strong>RecvFramerateAverageAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="d2451-130"><strong>RecvFramerateAverageAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="d2451-131">десятичное число (9; 4)</span><span class="sxs-lookup"><span data-stu-id="d2451-131">decimal(9,4)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d2451-132">Значение по умолчанию — 7,0000.</span><span class="sxs-lookup"><span data-stu-id="d2451-132">The default value is 7.0000.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2451-133"><strong>LowFrameRateCallPercentOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="d2451-133"><strong>LowFrameRateCallPercentOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="d2451-134">десятичное число (5; 2)</span><span class="sxs-lookup"><span data-stu-id="d2451-134">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d2451-135">Значение по умолчанию — 5,0.</span><span class="sxs-lookup"><span data-stu-id="d2451-135">The default value is 5.0.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2451-136"><strong>LowFrameRateCallPercentAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="d2451-136"><strong>LowFrameRateCallPercentAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="d2451-137">десятичное число (5; 2)</span><span class="sxs-lookup"><span data-stu-id="d2451-137">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d2451-138">Значение по умолчанию — 10.0/</span><span class="sxs-lookup"><span data-stu-id="d2451-138">The default value is 10.0/</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2451-139"><strong>LowResolutionCallPercentOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="d2451-139"><strong>LowResolutionCallPercentOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="d2451-140">десятичное число (5; 2)</span><span class="sxs-lookup"><span data-stu-id="d2451-140">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d2451-141">Значение по умолчанию — 5,0.</span><span class="sxs-lookup"><span data-stu-id="d2451-141">The default value is 5.0.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2451-142"><strong>LowResolutionCallPercentAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="d2451-142"><strong>LowResolutionCallPercentAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="d2451-143">десятичное число (5; 2)</span><span class="sxs-lookup"><span data-stu-id="d2451-143">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d2451-144">Значение по умолчанию — 10,0.</span><span class="sxs-lookup"><span data-stu-id="d2451-144">The default value is 10.0.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2451-145"><strong>VideoPacketLossRateOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="d2451-145"><strong>VideoPacketLossRateOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="d2451-146">foat</span><span class="sxs-lookup"><span data-stu-id="d2451-146">foat</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d2451-147">Значение по умолчанию — 0,05.</span><span class="sxs-lookup"><span data-stu-id="d2451-147">The default value is 0.05.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2451-148"><strong>VideoPacketLossRateAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="d2451-148"><strong>VideoPacketLossRateAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="d2451-149">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="d2451-149">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d2451-150">Значение по умолчанию — 0,10.</span><span class="sxs-lookup"><span data-stu-id="d2451-150">The default value is 0.10.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2451-151"><strong>VideoFrameRateAvgOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="d2451-151"><strong>VideoFrameRateAvgOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="d2451-152">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="d2451-152">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d2451-153">Значением по умолчанию является 12.</span><span class="sxs-lookup"><span data-stu-id="d2451-153">The default value is 12.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2451-154"><strong>VideoFrameRateAvgAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="d2451-154"><strong>VideoFrameRateAvgAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="d2451-155">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="d2451-155">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d2451-156">Значением по умолчанию является 7.</span><span class="sxs-lookup"><span data-stu-id="d2451-156">The default value is 7.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2451-157"><strong>DynamicCapabilityPercentOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="d2451-157"><strong>DynamicCapabilityPercentOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="d2451-158">десятичное число (5; 2)</span><span class="sxs-lookup"><span data-stu-id="d2451-158">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d2451-159">Значение по умолчанию — 5,00.</span><span class="sxs-lookup"><span data-stu-id="d2451-159">The default value is 5.00.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2451-160"><strong>DynamicCapabilityPercentAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="d2451-160"><strong>DynamicCapabilityPercentAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="d2451-161">десятичное число (5; 2)</span><span class="sxs-lookup"><span data-stu-id="d2451-161">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d2451-162">Значение по умолчанию — 10,00.</span><span class="sxs-lookup"><span data-stu-id="d2451-162">The default value is 10.00.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="d2451-163">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d2451-163">


</div>

<span> </span>

</div>

</div>

</span></span></div>

