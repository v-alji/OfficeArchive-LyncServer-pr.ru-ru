---
title: 'Lync Server 2013: таблица AudioStream'
description: 'Таблица Lync Server 2013: AudioStream.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: AudioStream table
ms:assetid: 49ccbbc3-2f73-45fc-80a6-e612535cbc10
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425961(v=OCS.15)
ms:contentKeyID: 48184077
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8af2e622e14c54fa4f9a6313e1b0dae8f2483132
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438178"
---
# <a name="audiostream-table-in-lync-server-2013"></a><span data-ttu-id="6d46e-103">Таблица AudioStream в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6d46e-103">AudioStream table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6d46e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6d46e-104">

<span> </span></span></span>

<span data-ttu-id="6d46e-105">_**Тема последнего изменения:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="6d46e-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="6d46e-106">Каждая запись представляет собой один звуковой поток.</span><span class="sxs-lookup"><span data-stu-id="6d46e-106">Each record represents one audio stream.</span></span> <span data-ttu-id="6d46e-107">Одна линейка звуковых файлов обычно состоит из двух звуковых потоков.</span><span class="sxs-lookup"><span data-stu-id="6d46e-107">One audio media line usually contains two audio streams.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6d46e-108"><strong>Столбец</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="6d46e-109"><strong>Тип данных</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="6d46e-110"><strong>Ключ/индекс</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="6d46e-111"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6d46e-112"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-112"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="6d46e-113">datetime</span><span class="sxs-lookup"><span data-stu-id="6d46e-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="6d46e-114">Primary</span><span class="sxs-lookup"><span data-stu-id="6d46e-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="6d46e-115">На которую ссылается <a href="lync-server-2013-medialine-table.md">Таблица MediaLine в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="6d46e-115">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d46e-116"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-116"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="6d46e-117">целое</span><span class="sxs-lookup"><span data-stu-id="6d46e-117">int</span></span></p></td>
<td><p><span data-ttu-id="6d46e-118">Primary</span><span class="sxs-lookup"><span data-stu-id="6d46e-118">Primary</span></span></p></td>
<td><p><span data-ttu-id="6d46e-119">На которую ссылается <a href="lync-server-2013-medialine-table.md">Таблица MediaLine в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="6d46e-119">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d46e-120"><strong>MediaLineLabel</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-120"><strong>MediaLineLabel</strong></span></span></p></td>
<td><p><span data-ttu-id="6d46e-121">tinyint</span><span class="sxs-lookup"><span data-stu-id="6d46e-121">tinyint</span></span></p></td>
<td><p><span data-ttu-id="6d46e-122">Primary</span><span class="sxs-lookup"><span data-stu-id="6d46e-122">Primary</span></span></p></td>
<td><p><span data-ttu-id="6d46e-123">На которую ссылается <a href="lync-server-2013-medialine-table.md">Таблица MediaLine в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="6d46e-123">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d46e-124"><strong>StreamID</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-124"><strong>StreamID</strong></span></span></p></td>
<td><p><span data-ttu-id="6d46e-125">целое</span><span class="sxs-lookup"><span data-stu-id="6d46e-125">int</span></span></p></td>
<td><p><span data-ttu-id="6d46e-126">Primary</span><span class="sxs-lookup"><span data-stu-id="6d46e-126">Primary</span></span></p></td>
<td><p><span data-ttu-id="6d46e-127">Уникальный идентификатор в строке мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="6d46e-127">Unique ID within a media line.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d46e-128"><strong>JitterInterArrival</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-128"><strong>JitterInterArrival</strong></span></span></p></td>
<td><p><span data-ttu-id="6d46e-129">целое</span><span class="sxs-lookup"><span data-stu-id="6d46e-129">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6d46e-130">Средняя колебание сети из статистики протокола управления временем в реальном времени (RTCP).</span><span class="sxs-lookup"><span data-stu-id="6d46e-130">Average network jitter from Real Time Control Protocol (RTCP) statistics.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d46e-131"><strong>JitterInterArrivalMax</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-131"><strong>JitterInterArrivalMax</strong></span></span></p></td>
<td><p><span data-ttu-id="6d46e-132">целое</span><span class="sxs-lookup"><span data-stu-id="6d46e-132">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6d46e-133">Максимальная колебание сети во время звонка.</span><span class="sxs-lookup"><span data-stu-id="6d46e-133">Maximum network jitter during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d46e-134"><strong>PacketLossRate</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-134"><strong>PacketLossRate</strong></span></span></p></td>
<td><p><span data-ttu-id="6d46e-135">десятичное число (5; 4)</span><span class="sxs-lookup"><span data-stu-id="6d46e-135">decimal(5,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6d46e-136">Средняя скорость потерь пакетов во время звонка.</span><span class="sxs-lookup"><span data-stu-id="6d46e-136">Average packet loss rate during the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d46e-137"><strong>PacketLossRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-137"><strong>PacketLossRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="6d46e-138">десятичное число (5; 4)</span><span class="sxs-lookup"><span data-stu-id="6d46e-138">decimal(5,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6d46e-139">Максимальное количество потерь пакетов, замеченное во время звонка.</span><span class="sxs-lookup"><span data-stu-id="6d46e-139">Maximum packet loss observed during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d46e-140"><strong>BurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-140"><strong>BurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="6d46e-141">десятичное число (9; 4)</span><span class="sxs-lookup"><span data-stu-id="6d46e-141">decimal(9,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6d46e-142">Средняя плотность потери пакетов во время звонка.</span><span class="sxs-lookup"><span data-stu-id="6d46e-142">Average density of packet Loss during bursts of losses during the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d46e-143"><strong>BurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-143"><strong>BurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="6d46e-144">целое</span><span class="sxs-lookup"><span data-stu-id="6d46e-144">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6d46e-145">Средняя продолжительность потери пакетов в течение заданных потерь во время звонка.</span><span class="sxs-lookup"><span data-stu-id="6d46e-145">Average duration of packet loss during bursts of losses during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d46e-146"><strong>BurstGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-146"><strong>BurstGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="6d46e-147">десятичное число (9; 4)</span><span class="sxs-lookup"><span data-stu-id="6d46e-147">decimal(9,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6d46e-148">Средняя плотность потери пакетов при пропуске между пакетами потери данных.</span><span class="sxs-lookup"><span data-stu-id="6d46e-148">Average density of packet loss during gaps between bursts of packet loss.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d46e-149"><strong>BurstGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-149"><strong>BurstGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="6d46e-150">целое</span><span class="sxs-lookup"><span data-stu-id="6d46e-150">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6d46e-151">Средняя продолжительность промежутков между пакетами потери данных.</span><span class="sxs-lookup"><span data-stu-id="6d46e-151">Average duration of gaps between bursts of packet loss.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d46e-152"><strong>PacketUtilization</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-152"><strong>PacketUtilization</strong></span></span></p></td>
<td><p><span data-ttu-id="6d46e-153">Типом</span><span class="sxs-lookup"><span data-stu-id="6d46e-153">Int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6d46e-154">Число пакетов для аудиопотока.</span><span class="sxs-lookup"><span data-stu-id="6d46e-154">Packet count for the audio stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d46e-155"><strong>Самый пропускная способность</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-155"><strong>BandwidthEst</strong></span></span></p></td>
<td><p><span data-ttu-id="6d46e-156">Типом</span><span class="sxs-lookup"><span data-stu-id="6d46e-156">Int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6d46e-157">Оценка пропускной способности для аудиопотока.</span><span class="sxs-lookup"><span data-stu-id="6d46e-157">Bandwidth estimates for the audio stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d46e-158"><strong>DegradationAvg</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-158"><strong>DegradationAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="6d46e-159">десятичное число (3, 2)</span><span class="sxs-lookup"><span data-stu-id="6d46e-159">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6d46e-160">Сетевое MOS падение на весь звонок.</span><span class="sxs-lookup"><span data-stu-id="6d46e-160">Network MOS Degradation for the whole call.</span></span> <span data-ttu-id="6d46e-161">Диапазон от 0,0 до 5,0.</span><span class="sxs-lookup"><span data-stu-id="6d46e-161">Range is 0.0 to 5.0.</span></span> <span data-ttu-id="6d46e-162">Этот показатель показывает объем сетевого MOS уменьшился из-за колебаний и потери пакетов.</span><span class="sxs-lookup"><span data-stu-id="6d46e-162">This metric shows the amount the Network MOS was reduced because of jitter and packet loss.</span></span> <span data-ttu-id="6d46e-163">Для приемлемого качества оно должно быть менее 0,5.</span><span class="sxs-lookup"><span data-stu-id="6d46e-163">For acceptable quality it should less than 0.5.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d46e-164"><strong>DegradationMax</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-164"><strong>DegradationMax</strong></span></span></p></td>
<td><p><span data-ttu-id="6d46e-165">десятичное число (3, 2)</span><span class="sxs-lookup"><span data-stu-id="6d46e-165">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6d46e-166">Максимальная длина сетевого MOS во время звонка.</span><span class="sxs-lookup"><span data-stu-id="6d46e-166">Maximum Network MOS degradation during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d46e-167"><strong>DegradationJitterAvg</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-167"><strong>DegradationJitterAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="6d46e-168">десятичное число (3, 2)</span><span class="sxs-lookup"><span data-stu-id="6d46e-168">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6d46e-169">Снижение производительности сети MOS из – за колебаний.</span><span class="sxs-lookup"><span data-stu-id="6d46e-169">Network MOS degradation caused by jitter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d46e-170"><strong>DegradationPacketLossAvg</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-170"><strong>DegradationPacketLossAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="6d46e-171">десятичное число (3, 2)</span><span class="sxs-lookup"><span data-stu-id="6d46e-171">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6d46e-172">Снижение производительности сети MOS из – за потери пакетов.</span><span class="sxs-lookup"><span data-stu-id="6d46e-172">Network MOS degradation caused by packet loss.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d46e-173"><strong>AudioPayloadDescription</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-173"><strong>AudioPayloadDescription</strong></span></span></p></td>
<td><p><span data-ttu-id="6d46e-174">целое</span><span class="sxs-lookup"><span data-stu-id="6d46e-174">int</span></span></p></td>
<td><p><span data-ttu-id="6d46e-175">Другом</span><span class="sxs-lookup"><span data-stu-id="6d46e-175">Foreign</span></span></p></td>
<td><p><span data-ttu-id="6d46e-176">Аудиокодек, использованный для вызова, на который ссылается таблица PayloadDescription.</span><span class="sxs-lookup"><span data-stu-id="6d46e-176">The audio Codec used for the call, referenced from PayloadDescription Table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d46e-177"><strong>AudioSampleRate</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-177"><strong>AudioSampleRate</strong></span></span></p></td>
<td><p><span data-ttu-id="6d46e-178">целое</span><span class="sxs-lookup"><span data-stu-id="6d46e-178">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6d46e-179">Частота дискретизации для аудиопотока.</span><span class="sxs-lookup"><span data-stu-id="6d46e-179">Sampling rate for the audio stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d46e-180"><strong>RoundTrip</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-180"><strong>RoundTrip</strong></span></span></p></td>
<td><p><span data-ttu-id="6d46e-181">целое</span><span class="sxs-lookup"><span data-stu-id="6d46e-181">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6d46e-182">Время кругового приема из статистики RTCP.</span><span class="sxs-lookup"><span data-stu-id="6d46e-182">Round trip time from RTCP statistics.</span></span> <span data-ttu-id="6d46e-183">Для приемлемого качества оно должно быть меньше 100ms.</span><span class="sxs-lookup"><span data-stu-id="6d46e-183">For acceptable quality this should be less than 100ms.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d46e-184"><strong>RoundTripMax</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-184"><strong>RoundTripMax</strong></span></span></p></td>
<td><p><span data-ttu-id="6d46e-185">целое</span><span class="sxs-lookup"><span data-stu-id="6d46e-185">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6d46e-186">Максимальное время кругового приема для звукового потока.</span><span class="sxs-lookup"><span data-stu-id="6d46e-186">Maximum round trip time for the audio stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d46e-187"><strong>OverallAvgNetworkMOS</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-187"><strong>OverallAvgNetworkMOS</strong></span></span></p></td>
<td><p><span data-ttu-id="6d46e-188">десятичное число (3, 2)</span><span class="sxs-lookup"><span data-stu-id="6d46e-188">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6d46e-189">Средняя сетевая MOS широкополосному для звонка.</span><span class="sxs-lookup"><span data-stu-id="6d46e-189">Average wideband Network MOS for the call.</span></span> <span data-ttu-id="6d46e-190">Эта метрика зависит от потерь пакетов, колебаний и используемого кодека.</span><span class="sxs-lookup"><span data-stu-id="6d46e-190">This metric depends on the packet loss, jitter, and codec used.</span></span> <span data-ttu-id="6d46e-191">Диапазон: [1,0 – 5,0].</span><span class="sxs-lookup"><span data-stu-id="6d46e-191">Range is [1.0 to 5.0].</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d46e-192"><strong>OverallMinNetworkMOS</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-192"><strong>OverallMinNetworkMOS</strong></span></span></p></td>
<td><p><span data-ttu-id="6d46e-193">десятичное число (3, 2)</span><span class="sxs-lookup"><span data-stu-id="6d46e-193">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6d46e-194">Минимальная широкополосному сеть MOS для звонка.</span><span class="sxs-lookup"><span data-stu-id="6d46e-194">The minimum wideband Network MOS for the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d46e-195"><strong>SendListenMOS</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-195"><strong>SendListenMOS</strong></span></span></p></td>
<td><p><span data-ttu-id="6d46e-196">десятичное число (3, 2)</span><span class="sxs-lookup"><span data-stu-id="6d46e-196">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6d46e-197">Средний прогнозируемый широкополосному прослушивания MOS для звукового сигнала, в том числе уровней речи, уровней шума и характеристик устройства захвата.</span><span class="sxs-lookup"><span data-stu-id="6d46e-197">The average predicted wideband Listening MOS score for audio sent, including speech level, noise level and capture device characteristics.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d46e-198"><strong>SendListenMOSMin</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-198"><strong>SendListenMOSMin</strong></span></span></p></td>
<td><p><span data-ttu-id="6d46e-199">десятичное число (3, 2)</span><span class="sxs-lookup"><span data-stu-id="6d46e-199">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6d46e-200">Минимальная SendListenMOS для звонка.</span><span class="sxs-lookup"><span data-stu-id="6d46e-200">The minimum SendListenMOS for the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d46e-201"><strong>RecvListenMOS</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-201"><strong>RecvListenMOS</strong></span></span></p></td>
<td><p><span data-ttu-id="6d46e-202">десятичное число (3, 2)</span><span class="sxs-lookup"><span data-stu-id="6d46e-202">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6d46e-203">Средний прогнозируемый широкополосному прослушивания MOS для звукового сигнала, получаемого из сети, включая уровень речи, уровень шума, кодек, условия сети и характеристики устройства захвата.</span><span class="sxs-lookup"><span data-stu-id="6d46e-203">The average predicted wideband Listening MOS score for audio received from the network including speech level, noise level, codec, network conditions and capture device characteristics.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d46e-204"><strong>RecvListenMOSMin</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-204"><strong>RecvListenMOSMin</strong></span></span></p></td>
<td><p><span data-ttu-id="6d46e-205">десятичное число (3, 2)</span><span class="sxs-lookup"><span data-stu-id="6d46e-205">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6d46e-206">Минимальная RecvListenMOS для звонка.</span><span class="sxs-lookup"><span data-stu-id="6d46e-206">The minimum RecvListenMOS for the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d46e-207"><strong>AudioFECUsed</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-207"><strong>AudioFECUsed</strong></span></span></p></td>
<td><p><span data-ttu-id="6d46e-208">бит</span><span class="sxs-lookup"><span data-stu-id="6d46e-208">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6d46e-209">Флаг, указывающий, использовался ли для звонка звуковой FEC.</span><span class="sxs-lookup"><span data-stu-id="6d46e-209">Flag indicating if audio FEC was used for the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d46e-210"><strong>RatioConcealedSamplesAvg</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-210"><strong>RatioConcealedSamplesAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="6d46e-211">десятичное число (5; 2)</span><span class="sxs-lookup"><span data-stu-id="6d46e-211">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6d46e-212">Среднее отношение количества преобразованных образцов, созданных при воспроизведении звука, на обычные выборки.</span><span class="sxs-lookup"><span data-stu-id="6d46e-212">Average ratio of concealed samples generated by audio healing to typical samples.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d46e-213"><strong>RatioStretchedSamplesAvg</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-213"><strong>RatioStretchedSamplesAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="6d46e-214">десятичное число (5; 2)</span><span class="sxs-lookup"><span data-stu-id="6d46e-214">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6d46e-215">Среднее отношение растянутых образцов, созданных при воспроизведении звука, на обычные выборки.</span><span class="sxs-lookup"><span data-stu-id="6d46e-215">Average ratio of stretched samples generated by audio healing to typical samples.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d46e-216"><strong>RatioCompressedSamplesAvg</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-216"><strong>RatioCompressedSamplesAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="6d46e-217">десятичное число (5; 2)</span><span class="sxs-lookup"><span data-stu-id="6d46e-217">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6d46e-218">Среднее отношение количества сжатых образцов, созданных при восстановлении звука, на обычные образцы.</span><span class="sxs-lookup"><span data-stu-id="6d46e-218">Average ratio of compressed samples generated by audio healing to typical samples.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d46e-219"><strong>443</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-219"><strong>Inbound</strong></span></span></p></td>
<td><p><span data-ttu-id="6d46e-220">бит</span><span class="sxs-lookup"><span data-stu-id="6d46e-220">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6d46e-221">Получение потоковых данных на стороне получателя.</span><span class="sxs-lookup"><span data-stu-id="6d46e-221">Stream data on receiver side is received.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d46e-222"><strong>Исходящее</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-222"><strong>Outbound</strong></span></span></p></td>
<td><p><span data-ttu-id="6d46e-223">бит</span><span class="sxs-lookup"><span data-stu-id="6d46e-223">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6d46e-224">Получение данных потока на стороне отправителя.</span><span class="sxs-lookup"><span data-stu-id="6d46e-224">Stream data on sender side is received.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d46e-225"><strong>SenderIsCallerPAI</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-225"><strong>SenderIsCallerPAI</strong></span></span></p></td>
<td><p><span data-ttu-id="6d46e-226">бит</span><span class="sxs-lookup"><span data-stu-id="6d46e-226">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6d46e-227">1 — направление потока на вызываемый абонентом.</span><span class="sxs-lookup"><span data-stu-id="6d46e-227">1 means the stream direction is from the caller to the callee.</span></span></p>
<p><span data-ttu-id="6d46e-228">0 — направление потока из вызываемого объекта вызывающему абоненту.</span><span class="sxs-lookup"><span data-stu-id="6d46e-228">0 means the stream direction is from the callee to the caller.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d46e-229"><strong>JitterInterArrivalSD</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-229"><strong>JitterInterArrivalSD</strong></span></span></p></td>
<td><p><span data-ttu-id="6d46e-230">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="6d46e-230">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6d46e-231">Стандартное отклонение для наступления интервала ожидания.</span><span class="sxs-lookup"><span data-stu-id="6d46e-231">Standard deviation for jitter arrival times.</span></span></p>
<p><span data-ttu-id="6d46e-232">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6d46e-232">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d46e-233"><strong>ConcealRatioMax</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-233"><strong>ConcealRatioMax</strong></span></span></p></td>
<td><p><span data-ttu-id="6d46e-234">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="6d46e-234">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6d46e-235">Максимальное соотношение пакетов, которые скрываются с помощью восстанавливаемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="6d46e-235">Maximum ratio of packets concealed by the healer.</span></span></p>
<p><span data-ttu-id="6d46e-236">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6d46e-236">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d46e-237"><strong>ConcealRatioSD</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-237"><strong>ConcealRatioSD</strong></span></span></p></td>
<td><p><span data-ttu-id="6d46e-238">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="6d46e-238">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6d46e-239">Стандартное отклонение для соотношения пакетов, которые скрываются с помощью восстанавливаемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="6d46e-239">Standard deviation for the ratio of packets concealed by the healer.</span></span></p>
<p><span data-ttu-id="6d46e-240">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6d46e-240">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d46e-241"><strong>HealerPacketDropRatio</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-241"><strong>HealerPacketDropRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="6d46e-242">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="6d46e-242">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6d46e-243">Доля пакетов, отброшенных с помощью восстанавливаемого экземпляра по сравнению с общим количеством полученных пакетов.</span><span class="sxs-lookup"><span data-stu-id="6d46e-243">Ratio of packets dropped by the healer compared to the total number of packets received.</span></span></p>
<p><span data-ttu-id="6d46e-244">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6d46e-244">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d46e-245"><strong>HealerFECPacketUsedRatio</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-245"><strong>HealerFECPacketUsedRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="6d46e-246">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="6d46e-246">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6d46e-247">Отношение использованных пакетов исправлений ошибок переадресации к общему количеству полученных пакетов.</span><span class="sxs-lookup"><span data-stu-id="6d46e-247">Ratio of used forward error correction packets compared to the total number of packets received.</span></span></p>
<p><span data-ttu-id="6d46e-248">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6d46e-248">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d46e-249"><strong>MaxCompressedSamples</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-249"><strong>MaxCompressedSamples</strong></span></span></p></td>
<td><p><span data-ttu-id="6d46e-250">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="6d46e-250">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6d46e-251">Максимальное количество звуковых пакетов, сжатых с помощью восстанавливаемого архива.</span><span class="sxs-lookup"><span data-stu-id="6d46e-251">Maximum number of audio packets that were compressed by the healer.</span></span></p>
<p><span data-ttu-id="6d46e-252">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6d46e-252">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d46e-253"><strong>LossCongestionPercent</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-253"><strong>LossCongestionPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="6d46e-254">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="6d46e-254">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6d46e-255">Указывает процент времени, в течение которого Звонок находился в состоянии перегрузки с потерей.</span><span class="sxs-lookup"><span data-stu-id="6d46e-255">Indicates the percentage of the time when the call was in a loss congestion state.</span></span></p>
<p><span data-ttu-id="6d46e-256">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6d46e-256">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d46e-257"><strong>DelayCongestionPercent</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-257"><strong>DelayCongestionPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="6d46e-258">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="6d46e-258">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6d46e-259">Указывает процент вызова, в течение которого перегрузка была вызвана отложенным поступлением сетевых пакетов.</span><span class="sxs-lookup"><span data-stu-id="6d46e-259">Indicates the percentage of the call during which congestion was caused by the delayed arrival of network packets.</span></span></p>
<p><span data-ttu-id="6d46e-260">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6d46e-260">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d46e-261"><strong>ContentionDetectedPercent</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-261"><strong>ContentionDetectedPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="6d46e-262">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="6d46e-262">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6d46e-263">Указывает процент времени, в течение которого Звонок конкурирует за ресурсы сети.</span><span class="sxs-lookup"><span data-stu-id="6d46e-263">Indicates the percentage of the time when the call was competing for network resources.</span></span></p>
<p><span data-ttu-id="6d46e-264">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6d46e-264">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d46e-265"><strong>BandwidthEstMin</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-265"><strong>BandwidthEstMin</strong></span></span></p></td>
<td><p><span data-ttu-id="6d46e-266">целое</span><span class="sxs-lookup"><span data-stu-id="6d46e-266">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6d46e-267">Минимальная сумма оценки пропускной способности, измеряемая во время звонка.</span><span class="sxs-lookup"><span data-stu-id="6d46e-267">Minimum amount of bandwidth estimation measured during the call.</span></span></p>
<p><span data-ttu-id="6d46e-268">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6d46e-268">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d46e-269"><strong>BandwidthEstMax</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-269"><strong>BandwidthEstMax</strong></span></span></p></td>
<td><p><span data-ttu-id="6d46e-270">целое</span><span class="sxs-lookup"><span data-stu-id="6d46e-270">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6d46e-271">Максимальная степень оценки пропускной способности, измеряемая во время звонка.</span><span class="sxs-lookup"><span data-stu-id="6d46e-271">Maximum amount of bandwidth estimation measured during the call.</span></span></p>
<p><span data-ttu-id="6d46e-272">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6d46e-272">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d46e-273"><strong>BandwidthEstStdDev</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-273"><strong>BandwidthEstStdDev</strong></span></span></p></td>
<td><p><span data-ttu-id="6d46e-274">целое</span><span class="sxs-lookup"><span data-stu-id="6d46e-274">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6d46e-275">Стандартное отклонение оценки пропускной способности, измеряемой во время звонка.</span><span class="sxs-lookup"><span data-stu-id="6d46e-275">Standard deviation of the bandwidth estimation measured during the call.</span></span></p>
<p><span data-ttu-id="6d46e-276">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6d46e-276">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d46e-277"><strong>BandwidthEstAvge</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-277"><strong>BandwidthEstAvge</strong></span></span></p></td>
<td><p><span data-ttu-id="6d46e-278">целое</span><span class="sxs-lookup"><span data-stu-id="6d46e-278">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6d46e-279">Средняя сумма оценки пропускной способности, измеряемая во время звонка.</span><span class="sxs-lookup"><span data-stu-id="6d46e-279">Average amount of bandwidth estimation measured during the call.</span></span></p>
<p><span data-ttu-id="6d46e-280">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6d46e-280">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d46e-281"><strong>RelativeOneWayTotal</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-281"><strong>RelativeOneWayTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="6d46e-282">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="6d46e-282">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6d46e-283">Общая сумма односторонней задержки.</span><span class="sxs-lookup"><span data-stu-id="6d46e-283">Total amount of one-way latency.</span></span> <span data-ttu-id="6d46e-284">Относительная односторонняя задержка измеряет задержку между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="6d46e-284">Relative one-way latency measures the delay between the client and the server.</span></span></p>
<p><span data-ttu-id="6d46e-285">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6d46e-285">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d46e-286"><strong>RelativeOneWayAverage</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-286"><strong>RelativeOneWayAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="6d46e-287">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="6d46e-287">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6d46e-288">Средняя величина односторонней задержки.</span><span class="sxs-lookup"><span data-stu-id="6d46e-288">Average amount of one-way latency.</span></span> <span data-ttu-id="6d46e-289">Относительная односторонняя задержка измеряет задержку между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="6d46e-289">Relative one-way latency measures the delay between the client and the server.</span></span></p>
<p><span data-ttu-id="6d46e-290">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6d46e-290">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d46e-291"><strong>RelativeOneWayMax</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-291"><strong>RelativeOneWayMax</strong></span></span></p></td>
<td><p><span data-ttu-id="6d46e-292">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="6d46e-292">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6d46e-293">Максимальная сумма односторонняя задержка.</span><span class="sxs-lookup"><span data-stu-id="6d46e-293">Maximum amount of one-way latency.</span></span> <span data-ttu-id="6d46e-294">Относительная односторонняя задержка измеряет задержку между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="6d46e-294">Relative one-way latency measures the delay between the client and the server.</span></span></p>
<p><span data-ttu-id="6d46e-295">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6d46e-295">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d46e-296"><strong>RelativeOneWayBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-296"><strong>RelativeOneWayBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="6d46e-297">целое</span><span class="sxs-lookup"><span data-stu-id="6d46e-297">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6d46e-298">Общее количество односторонних вхождений.</span><span class="sxs-lookup"><span data-stu-id="6d46e-298">Total one-way burst occurrences.</span></span> <span data-ttu-id="6d46e-299">Одновременная передача данных — это передача, при которой данные передаются в непредсказуемые пакеты, а не в устойчивый поток.</span><span class="sxs-lookup"><span data-stu-id="6d46e-299">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="6d46e-300">Этот показатель измеряет поток данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="6d46e-300">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="6d46e-301">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6d46e-301">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d46e-302"><strong>RelativeOneWayBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-302"><strong>RelativeOneWayBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="6d46e-303">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="6d46e-303">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6d46e-304">Общая односторонняя плотность нагрузки.</span><span class="sxs-lookup"><span data-stu-id="6d46e-304">Total one-way burst density.</span></span> <span data-ttu-id="6d46e-305">Одновременная передача данных — это передача, при которой данные передаются в непредсказуемые пакеты, а не в устойчивый поток.</span><span class="sxs-lookup"><span data-stu-id="6d46e-305">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="6d46e-306">Этот показатель измеряет поток данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="6d46e-306">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="6d46e-307">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6d46e-307">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d46e-308"><strong>RelativeOneWayBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-308"><strong>RelativeOneWayBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="6d46e-309">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="6d46e-309">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6d46e-310">Общая продолжительность односторонней длительности.</span><span class="sxs-lookup"><span data-stu-id="6d46e-310">Total one-way burst duration.</span></span> <span data-ttu-id="6d46e-311">Одновременная передача данных — это передача, при которой данные передаются в непредсказуемые пакеты, а не в устойчивый поток.</span><span class="sxs-lookup"><span data-stu-id="6d46e-311">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="6d46e-312">Этот показатель измеряет поток данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="6d46e-312">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="6d46e-313">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6d46e-313">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d46e-314"><strong>RelativeOneWayGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-314"><strong>RelativeOneWayGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="6d46e-315">целое</span><span class="sxs-lookup"><span data-stu-id="6d46e-315">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6d46e-316">Общее количество односторонних вхождений.</span><span class="sxs-lookup"><span data-stu-id="6d46e-316">Total one-way gap occurrences.</span></span> <span data-ttu-id="6d46e-317">Одновременная передача данных — это передача, при которой данные передаются в непредсказуемые пакеты, а не в устойчивый поток. зазоры указывают на задержку между этими пакетами.</span><span class="sxs-lookup"><span data-stu-id="6d46e-317">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="6d46e-318">Этот показатель измеряет поток данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="6d46e-318">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="6d46e-319">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6d46e-319">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d46e-320"><strong>RelativeOneWayGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-320"><strong>RelativeOneWayGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="6d46e-321">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="6d46e-321">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6d46e-322">Общая плотность односторонних зазоров.</span><span class="sxs-lookup"><span data-stu-id="6d46e-322">Total one-way gap density.</span></span> <span data-ttu-id="6d46e-323">Одновременная передача данных — это передача, при которой данные передаются в непредсказуемые пакеты, а не в устойчивый поток. зазоры указывают на задержку между этими пакетами.</span><span class="sxs-lookup"><span data-stu-id="6d46e-323">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="6d46e-324">Этот показатель измеряет поток данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="6d46e-324">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="6d46e-325">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6d46e-325">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d46e-326"><strong>RelativeOneWayGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-326"><strong>RelativeOneWayGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="6d46e-327">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="6d46e-327">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6d46e-328">Общая продолжительность односторонних промежутков.</span><span class="sxs-lookup"><span data-stu-id="6d46e-328">Total one-way gap duration.</span></span> <span data-ttu-id="6d46e-329">Одновременная передача данных — это передача, при которой данные передаются в непредсказуемые пакеты, а не в устойчивый поток. зазоры указывают на задержку между этими пакетами.</span><span class="sxs-lookup"><span data-stu-id="6d46e-329">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="6d46e-330">Этот показатель измеряет поток данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="6d46e-330">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="6d46e-331">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6d46e-331">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d46e-332"><strong>DecodeStereoPercent</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-332"><strong>DecodeStereoPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="6d46e-333">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="6d46e-333">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6d46e-334">Процент звонка, декодированный как стерео.</span><span class="sxs-lookup"><span data-stu-id="6d46e-334">Percentage of the call decoded as stereo.</span></span></p>
<p><span data-ttu-id="6d46e-335">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6d46e-335">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d46e-336"><strong>AecRenderStereoPercent</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-336"><strong>AecRenderStereoPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="6d46e-337">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="6d46e-337">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6d46e-338">Процент звонка, выводимого в качестве стерео, с помощью отдавления акустического эха.</span><span class="sxs-lookup"><span data-stu-id="6d46e-338">Percentage of the call rendered as stereo by the acoustic echo canceller.</span></span></p>
<p><span data-ttu-id="6d46e-339">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6d46e-339">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d46e-340"><strong>AudioPostFECPLR</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-340"><strong>AudioPostFECPLR</strong></span></span></p></td>
<td><p><span data-ttu-id="6d46e-341">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="6d46e-341">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6d46e-342">Применена ставка потери пакетов после исправления ошибки переадресации.</span><span class="sxs-lookup"><span data-stu-id="6d46e-342">Packet loss rate after forward error correction has been applied.</span></span></p>
<p><span data-ttu-id="6d46e-343">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6d46e-343">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d46e-344"><strong>EncodeStereoPercent</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-344"><strong>EncodeStereoPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="6d46e-345">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="6d46e-345">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6d46e-346">Процент звонка, закодированный как стерео.</span><span class="sxs-lookup"><span data-stu-id="6d46e-346">Percentage of the call encoded as stereo.</span></span></p>
<p><span data-ttu-id="6d46e-347">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6d46e-347">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d46e-348"><strong>AecCaptureStereoPercent</strong></span><span class="sxs-lookup"><span data-stu-id="6d46e-348"><strong>AecCaptureStereoPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="6d46e-349">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="6d46e-349">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6d46e-350">Процент звонка, захваченного как стерео, с помощью функции отмены акустического эха.</span><span class="sxs-lookup"><span data-stu-id="6d46e-350">Percentage of the call captured as stereo by the acoustic echo canceller.</span></span></p>
<p><span data-ttu-id="6d46e-351">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6d46e-351">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="6d46e-352">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6d46e-352">


</div>

<span> </span>

</div>

</div>

</span></span></div>

