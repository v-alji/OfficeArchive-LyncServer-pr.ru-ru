---
title: 'Lync Server 2013: таблица VideoStream'
description: 'Таблица Lync Server 2013: VideoStream.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: VideoStream table
ms:assetid: 4275ede7-5467-4a97-b8c8-a4b00917bf32
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425928(v=OCS.15)
ms:contentKeyID: 48184014
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0d741478e1f6290685181bff471f143e41ce9ca1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444128"
---
# <a name="videostream-table-in-lync-server-2013"></a><span data-ttu-id="1bff7-103">Таблица VideoStream в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1bff7-103">VideoStream table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1bff7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1bff7-104">

<span> </span></span></span>

<span data-ttu-id="1bff7-105">_**Тема последнего изменения:** 2013-12-13_</span><span class="sxs-lookup"><span data-stu-id="1bff7-105">_**Topic Last Modified:** 2013-12-13_</span></span>

<span data-ttu-id="1bff7-106">Каждая запись представляет один поток видео.</span><span class="sxs-lookup"><span data-stu-id="1bff7-106">Each record represents one video stream.</span></span> <span data-ttu-id="1bff7-107">Одна линия видеофайла обычно состоит из двух видеопотоков.</span><span class="sxs-lookup"><span data-stu-id="1bff7-107">One video media line usually contains two video streams.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1bff7-108"><strong>Столбец</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="1bff7-109"><strong>Тип данных</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="1bff7-110"><strong>Ключ/индекс</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="1bff7-111"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1bff7-112"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-112"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-113">datetime</span><span class="sxs-lookup"><span data-stu-id="1bff7-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="1bff7-114">Primary</span><span class="sxs-lookup"><span data-stu-id="1bff7-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="1bff7-115">На которую ссылается <a href="lync-server-2013-medialine-table.md">Таблица MediaLine в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="1bff7-115">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bff7-116"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-116"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-117">целое</span><span class="sxs-lookup"><span data-stu-id="1bff7-117">int</span></span></p></td>
<td><p><span data-ttu-id="1bff7-118">Primary</span><span class="sxs-lookup"><span data-stu-id="1bff7-118">Primary</span></span></p></td>
<td><p><span data-ttu-id="1bff7-119">R, на который ссылается <a href="lync-server-2013-medialine-table.md">Таблица MediaLine в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="1bff7-119">R Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bff7-120"><strong>MediaLineLabel</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-120"><strong>MediaLineLabel</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-121">tinyint</span><span class="sxs-lookup"><span data-stu-id="1bff7-121">tinyint</span></span></p></td>
<td><p><span data-ttu-id="1bff7-122">Primary</span><span class="sxs-lookup"><span data-stu-id="1bff7-122">Primary</span></span></p></td>
<td><p><span data-ttu-id="1bff7-123">На которую ссылается <a href="lync-server-2013-medialine-table.md">Таблица MediaLine в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="1bff7-123">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bff7-124"><strong>StreamID</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-124"><strong>StreamID</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-125">целое</span><span class="sxs-lookup"><span data-stu-id="1bff7-125">int</span></span></p></td>
<td><p><span data-ttu-id="1bff7-126">Primary</span><span class="sxs-lookup"><span data-stu-id="1bff7-126">Primary</span></span></p></td>
<td><p><span data-ttu-id="1bff7-127">Уникальный идентификатор в строке мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="1bff7-127">Unique ID within a media line.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bff7-128"><strong>VideoPayloadDescription</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-128"><strong>VideoPayloadDescription</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-129">smallint</span><span class="sxs-lookup"><span data-stu-id="1bff7-129">smallint</span></span></p></td>
<td><p><span data-ttu-id="1bff7-130">Внешний, основной</span><span class="sxs-lookup"><span data-stu-id="1bff7-130">Foreign, Primary</span></span></p></td>
<td><p><span data-ttu-id="1bff7-131">Описание полезных данных.</span><span class="sxs-lookup"><span data-stu-id="1bff7-131">Payload description.</span></span> <span data-ttu-id="1bff7-132">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-payloaddescription-table.md">таблицей PayloadDescription в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="1bff7-132">See the <a href="lync-server-2013-payloaddescription-table.md">PayloadDescription table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bff7-133"><strong>JitterInterArrival</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-133"><strong>JitterInterArrival</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-134">целое</span><span class="sxs-lookup"><span data-stu-id="1bff7-134">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="1bff7-135">Средняя колебание сети из статистики протокола управления временем в реальном времени (RTCP).</span><span class="sxs-lookup"><span data-stu-id="1bff7-135">Average network jitter from Real Time Control Protocol (RTCP) statistics.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bff7-136"><strong>JitterInterArrivalMax</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-136"><strong>JitterInterArrivalMax</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-137">целое</span><span class="sxs-lookup"><span data-stu-id="1bff7-137">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="1bff7-138">Максимальная колебание сети во время видеосеанса.</span><span class="sxs-lookup"><span data-stu-id="1bff7-138">Maximum network jitter during the video session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bff7-139"><strong>RoundTrip</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-139"><strong>RoundTrip</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-140">целое</span><span class="sxs-lookup"><span data-stu-id="1bff7-140">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="1bff7-141">Время кругового приема из статистики RTCP.</span><span class="sxs-lookup"><span data-stu-id="1bff7-141">Round trip time from RTCP statistics.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bff7-142"><strong>RoundTripMax</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-142"><strong>RoundTripMax</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-143">целое</span><span class="sxs-lookup"><span data-stu-id="1bff7-143">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="1bff7-144">Максимальное время кругового сеанса для видеопотока.</span><span class="sxs-lookup"><span data-stu-id="1bff7-144">Maximum round trip time for the video stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bff7-145"><strong>PacketLossRate</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-145"><strong>PacketLossRate</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-146">десятичное число (5; 4)</span><span class="sxs-lookup"><span data-stu-id="1bff7-146">decimal(5,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="1bff7-147">Средняя скорость потерь пакетов во время звонка.</span><span class="sxs-lookup"><span data-stu-id="1bff7-147">Average packet loss rate during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bff7-148"><strong>PacketLossRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-148"><strong>PacketLossRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-149">десятичное число (5; 4)</span><span class="sxs-lookup"><span data-stu-id="1bff7-149">decimal(5,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="1bff7-150">Максимальное количество потерь пакетов, замеченное во время звонка.</span><span class="sxs-lookup"><span data-stu-id="1bff7-150">Maximum packet loss observed during the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bff7-151"><strong>PacketUtilization</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-151"><strong>PacketUtilization</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-152">целое</span><span class="sxs-lookup"><span data-stu-id="1bff7-152">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="1bff7-153">Число пакетов для видеопотока (транспортный протокол в реальном времени).</span><span class="sxs-lookup"><span data-stu-id="1bff7-153">Packet count for the video stream (Real Time Transport Protocol, RTP).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bff7-154"><strong>Самый пропускная способность</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-154"><strong>BandwidthEst</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-155">целое</span><span class="sxs-lookup"><span data-stu-id="1bff7-155">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="1bff7-156">Оценка пропускной способности для видеопотока.</span><span class="sxs-lookup"><span data-stu-id="1bff7-156">Bandwidth estimates for the video stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bff7-157"><strong>VideoResolution</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-157"><strong>VideoResolution</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-158">char (9)</span><span class="sxs-lookup"><span data-stu-id="1bff7-158">char(9)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="1bff7-159">Разрешение видео в пикселях, умноженное на высоту в пикселях.</span><span class="sxs-lookup"><span data-stu-id="1bff7-159">Resolution of the video in pixels width multiplied by pixels height.</span></span> <span data-ttu-id="1bff7-160">Отображается в виде строки.</span><span class="sxs-lookup"><span data-stu-id="1bff7-160">Reported as a string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bff7-161"><strong>VideoBitRateAvg</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-161"><strong>VideoBitRateAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-162">целое</span><span class="sxs-lookup"><span data-stu-id="1bff7-162">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="1bff7-163">Средняя скорость потока видео.</span><span class="sxs-lookup"><span data-stu-id="1bff7-163">Average bit rate of the video stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bff7-164"><strong>InboundVideoFrameRateAvg</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-164"><strong>InboundVideoFrameRateAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-165">десятичное число (9; 4)</span><span class="sxs-lookup"><span data-stu-id="1bff7-165">decimal(9,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="1bff7-166">Полученная частота кадров видео.</span><span class="sxs-lookup"><span data-stu-id="1bff7-166">The video frame rate received.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bff7-167"><strong>OutboundVideoFrameRateAvg</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-167"><strong>OutboundVideoFrameRateAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-168">десятичное число (9; 4)</span><span class="sxs-lookup"><span data-stu-id="1bff7-168">decimal(9,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="1bff7-169">Частота отправки кадров видео.</span><span class="sxs-lookup"><span data-stu-id="1bff7-169">The video frame rate sent.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bff7-170"><strong>VideoBitRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-170"><strong>VideoBitRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-171">целое</span><span class="sxs-lookup"><span data-stu-id="1bff7-171">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="1bff7-172">Максимальная скорость видеосигнала во время видеосеанса.</span><span class="sxs-lookup"><span data-stu-id="1bff7-172">The maximum video bit rate during the video session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bff7-173"><strong>VideoFrameLossRate</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-173"><strong>VideoFrameLossRate</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-174">десятичное число (9; 4)</span><span class="sxs-lookup"><span data-stu-id="1bff7-174">decimal(9,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="1bff7-175">Процент от общего числа потерянных кадров видео.</span><span class="sxs-lookup"><span data-stu-id="1bff7-175">The percentage of total video frames that are lost.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bff7-176"><strong>VideoFEC</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-176"><strong>VideoFEC</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-177">бит</span><span class="sxs-lookup"><span data-stu-id="1bff7-177">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="1bff7-178">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="1bff7-178">Not available.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bff7-179"><strong>VideoLocalFrameLossPercentageAvg</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-179"><strong>VideoLocalFrameLossPercentageAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-180">десятичное число (9; 4)</span><span class="sxs-lookup"><span data-stu-id="1bff7-180">decimal(9,4)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1bff7-181">Процент от общего числа потерянных кадров видео.</span><span class="sxs-lookup"><span data-stu-id="1bff7-181">The percentage of total video frames that are lost.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bff7-182"><strong>CIFQualityRatio</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-182"><strong>CIFQualityRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-183">tinyint</span><span class="sxs-lookup"><span data-stu-id="1bff7-183">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1bff7-184">Процент звонка, находился в разрешении общего формата обмена (CIF).</span><span class="sxs-lookup"><span data-stu-id="1bff7-184">The percentage of the call that was at the Common Interchange Format (CIF) resolution.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bff7-185"><strong>VGAQualityRatio</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-185"><strong>VGAQualityRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-186">tinyint</span><span class="sxs-lookup"><span data-stu-id="1bff7-186">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1bff7-187">Процент звонка, находился в режиме разрешающей способности VGA.</span><span class="sxs-lookup"><span data-stu-id="1bff7-187">The percentage of the call that was at VGA resolution.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bff7-188"><strong>HD720QualityRatio</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-188"><strong>HD720QualityRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-189">tinyint</span><span class="sxs-lookup"><span data-stu-id="1bff7-189">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1bff7-190">Процентное соотношение вызова, которое было установлено по адресу HD720.</span><span class="sxs-lookup"><span data-stu-id="1bff7-190">The percentage of the call that was at HD720 resolution.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bff7-191"><strong>NoneDropRatio</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-191"><strong>NoneDropRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-192">tinyint</span><span class="sxs-lookup"><span data-stu-id="1bff7-192">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1bff7-193">Процент продолжительности звонка без удаления кадров.</span><span class="sxs-lookup"><span data-stu-id="1bff7-193">Percentage of call duration with no frame drop.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bff7-194"><strong>BDropRatio</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-194"><strong>BDropRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-195">tinyint</span><span class="sxs-lookup"><span data-stu-id="1bff7-195">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1bff7-196">Процент продолжительности звонка с помощью функции B Frame Drop.</span><span class="sxs-lookup"><span data-stu-id="1bff7-196">Percentage of call duration with B frame drop.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bff7-197"><strong>BPDropRatio</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-197"><strong>BPDropRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-198">tinyint</span><span class="sxs-lookup"><span data-stu-id="1bff7-198">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1bff7-199">Процент продолжительности звонка с помощью перетаскивания рамки BP.</span><span class="sxs-lookup"><span data-stu-id="1bff7-199">Percentage of call duration with BP frame drop.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bff7-200"><strong>BPSPDropRatio</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-200"><strong>BPSPDropRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-201">tinyint</span><span class="sxs-lookup"><span data-stu-id="1bff7-201">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1bff7-202">Процент продолжительности звонка с помощью BPSP Frame Drop.</span><span class="sxs-lookup"><span data-stu-id="1bff7-202">Percentage of call duration with BPSP frame drop.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bff7-203"><strong>BPSPIDropRatio</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-203"><strong>BPSPIDropRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-204">tinyint</span><span class="sxs-lookup"><span data-stu-id="1bff7-204">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1bff7-205">Процент продолжительности звонка с помощью BPSPI Frame Drop.</span><span class="sxs-lookup"><span data-stu-id="1bff7-205">Percentage of call duration with BPSPI frame drop.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bff7-206"><strong>443</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-206"><strong>Inbound</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-207">бит</span><span class="sxs-lookup"><span data-stu-id="1bff7-207">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="1bff7-208">Получение потоковых данных на стороне получателя.</span><span class="sxs-lookup"><span data-stu-id="1bff7-208">Stream data on receiver side is received.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bff7-209"><strong>Исходящее</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-209"><strong>Outbound</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-210">бит</span><span class="sxs-lookup"><span data-stu-id="1bff7-210">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="1bff7-211">Получение данных потока на стороне отправителя.</span><span class="sxs-lookup"><span data-stu-id="1bff7-211">Stream data on sender side is received.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bff7-212"><strong>SenderIsCallerPAI</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-212"><strong>SenderIsCallerPAI</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-213">бит</span><span class="sxs-lookup"><span data-stu-id="1bff7-213">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="1bff7-214">1 — направление потока для вызываемого абонента.</span><span class="sxs-lookup"><span data-stu-id="1bff7-214">1 means the stream direction is from the caller to callee.</span></span></p>
<p><span data-ttu-id="1bff7-215">0 — направление потока из вызываемого объекта вызывающему абоненту.</span><span class="sxs-lookup"><span data-stu-id="1bff7-215">0 means the stream direction is from the callee to the caller.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bff7-216"><strong>LossCongestionPercent</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-216"><strong>LossCongestionPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-217">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="1bff7-217">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1bff7-218">Указывает процент времени, в течение которого Звонок находился в состоянии перегрузки с потерей.</span><span class="sxs-lookup"><span data-stu-id="1bff7-218">Indicates the percentage of the time when the call was in a loss congestion state.</span></span></p>
<p><span data-ttu-id="1bff7-219">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1bff7-219">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bff7-220"><strong>DelayCongestionPercent</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-220"><strong>DelayCongestionPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-221">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="1bff7-221">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1bff7-222">Указывает процент вызова, в течение которого перегрузка была вызвана отложенным поступлением сетевых пакетов.</span><span class="sxs-lookup"><span data-stu-id="1bff7-222">Indicates the percentage of the call during which congestion was caused by the delayed arrival of network packets.</span></span></p>
<p><span data-ttu-id="1bff7-223">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1bff7-223">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bff7-224"><strong>ContentionDetectedPercent</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-224"><strong>ContentionDetectedPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-225">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="1bff7-225">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1bff7-226">Указывает процент времени, в течение которого Звонок конкурирует за ресурсы сети.</span><span class="sxs-lookup"><span data-stu-id="1bff7-226">Indicates the percentage of the time when the call was competing for network resources.</span></span></p>
<p><span data-ttu-id="1bff7-227">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1bff7-227">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bff7-228"><strong>BandwidthEstMin</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-228"><strong>BandwidthEstMin</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-229">целое</span><span class="sxs-lookup"><span data-stu-id="1bff7-229">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1bff7-230">Минимальная сумма оценки пропускной способности, измеряемая во время звонка.</span><span class="sxs-lookup"><span data-stu-id="1bff7-230">Minimum amount of bandwidth estimation measured during the call.</span></span></p>
<p><span data-ttu-id="1bff7-231">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1bff7-231">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bff7-232"><strong>BandwidthEstMax</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-232"><strong>BandwidthEstMax</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-233">целое</span><span class="sxs-lookup"><span data-stu-id="1bff7-233">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1bff7-234">Максимальная степень оценки пропускной способности, измеряемая во время звонка.</span><span class="sxs-lookup"><span data-stu-id="1bff7-234">Maximum amount of bandwidth estimation measured during the call.</span></span></p>
<p><span data-ttu-id="1bff7-235">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1bff7-235">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bff7-236"><strong>BandwidthEstStdDev</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-236"><strong>BandwidthEstStdDev</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-237">целое</span><span class="sxs-lookup"><span data-stu-id="1bff7-237">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1bff7-238">Стандартное отклонение оценки пропускной способности, измеряемой во время звонка.</span><span class="sxs-lookup"><span data-stu-id="1bff7-238">Standard deviation of the bandwidth estimation measured during the call.</span></span></p>
<p><span data-ttu-id="1bff7-239">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1bff7-239">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bff7-240"><strong>BandwidthEstAvge</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-240"><strong>BandwidthEstAvge</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-241">целое</span><span class="sxs-lookup"><span data-stu-id="1bff7-241">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1bff7-242">Средняя сумма оценки пропускной способности, измеряемая во время звонка.</span><span class="sxs-lookup"><span data-stu-id="1bff7-242">Average amount of bandwidth estimation measured during the call.</span></span></p>
<p><span data-ttu-id="1bff7-243">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1bff7-243">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bff7-244"><strong>LowBandwidthForMultiview</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-244"><strong>LowBandwidthForMultiview</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-245">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="1bff7-245">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1bff7-246">Процент звонка, когда конечная точка определила, что сетевое подключение не поддерживало функцию просмотра видео.</span><span class="sxs-lookup"><span data-stu-id="1bff7-246">Percentage of the call where the endpoint determined that the network connection could not support multiview video.</span></span></p>
<p><span data-ttu-id="1bff7-247">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1bff7-247">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bff7-248"><strong>RelativeOneWayTotal</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-248"><strong>RelativeOneWayTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-249">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="1bff7-249">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1bff7-250">Общая сумма односторонней задержки.</span><span class="sxs-lookup"><span data-stu-id="1bff7-250">Total amount of one-way latency.</span></span> <span data-ttu-id="1bff7-251">Относительная односторонняя задержка измеряет задержку между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="1bff7-251">Relative one-way latency measures the delay between the client and the server.</span></span></p>
<p><span data-ttu-id="1bff7-252">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1bff7-252">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bff7-253"><strong>RelativeOneWayAverage</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-253"><strong>RelativeOneWayAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-254">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="1bff7-254">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1bff7-255">Средняя величина односторонней задержки.</span><span class="sxs-lookup"><span data-stu-id="1bff7-255">Average amount of one-way latency.</span></span> <span data-ttu-id="1bff7-256">Относительная односторонняя задержка измеряет задержку между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="1bff7-256">Relative one-way latency measures the delay between the client and the server.</span></span></p>
<p><span data-ttu-id="1bff7-257">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1bff7-257">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bff7-258"><strong>RelativeOneWayMax</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-258"><strong>RelativeOneWayMax</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-259">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="1bff7-259">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1bff7-260">Максимальная сумма односторонняя задержка.</span><span class="sxs-lookup"><span data-stu-id="1bff7-260">Maximum amount of one-way latency.</span></span> <span data-ttu-id="1bff7-261">Относительная односторонняя задержка измеряет задержку между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="1bff7-261">Relative one-way latency measures the delay between the client and the server.</span></span></p>
<p><span data-ttu-id="1bff7-262">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1bff7-262">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bff7-263"><strong>RelativeOneWayBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-263"><strong>RelativeOneWayBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-264">целое</span><span class="sxs-lookup"><span data-stu-id="1bff7-264">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1bff7-265">Общее количество односторонних вхождений.</span><span class="sxs-lookup"><span data-stu-id="1bff7-265">Total one-way burst occurrences.</span></span> <span data-ttu-id="1bff7-266">Одновременная передача данных — это передача, при которой данные передаются в непредсказуемые пакеты, а не в устойчивый поток.</span><span class="sxs-lookup"><span data-stu-id="1bff7-266">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="1bff7-267">Этот показатель измеряет поток данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="1bff7-267">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="1bff7-268">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1bff7-268">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bff7-269"><strong>RelativeOneWayBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-269"><strong>RelativeOneWayBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-270">целое</span><span class="sxs-lookup"><span data-stu-id="1bff7-270">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1bff7-271">Общая односторонняя плотность нагрузки.</span><span class="sxs-lookup"><span data-stu-id="1bff7-271">Total one-way burst density.</span></span> <span data-ttu-id="1bff7-272">Одновременная передача данных — это передача, при которой данные передаются в непредсказуемые пакеты, а не в устойчивый поток.</span><span class="sxs-lookup"><span data-stu-id="1bff7-272">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="1bff7-273">Этот показатель измеряет поток данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="1bff7-273">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="1bff7-274">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1bff7-274">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bff7-275"><strong>RelativeOneWayBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-275"><strong>RelativeOneWayBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-276">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="1bff7-276">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1bff7-277">Общая продолжительность односторонней длительности.</span><span class="sxs-lookup"><span data-stu-id="1bff7-277">Total one-way burst duration.</span></span> <span data-ttu-id="1bff7-278">Одновременная передача данных — это передача, при которой данные передаются в непредсказуемые пакеты, а не в устойчивый поток.</span><span class="sxs-lookup"><span data-stu-id="1bff7-278">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="1bff7-279">Этот показатель измеряет поток данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="1bff7-279">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="1bff7-280">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1bff7-280">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bff7-281"><strong>RelativeOneWayGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-281"><strong>RelativeOneWayGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-282">целое</span><span class="sxs-lookup"><span data-stu-id="1bff7-282">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1bff7-283">Общее количество односторонних вхождений.</span><span class="sxs-lookup"><span data-stu-id="1bff7-283">Total one-way gap occurrences.</span></span> <span data-ttu-id="1bff7-284">Одновременная передача данных — это передача, при которой данные передаются в непредсказуемые пакеты, а не в устойчивый поток. зазоры указывают на задержку между этими пакетами.</span><span class="sxs-lookup"><span data-stu-id="1bff7-284">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="1bff7-285">Этот показатель измеряет поток данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="1bff7-285">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="1bff7-286">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1bff7-286">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bff7-287"><strong>RelativeOneWayGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-287"><strong>RelativeOneWayGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-288">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="1bff7-288">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1bff7-289">Общая плотность односторонних зазоров.</span><span class="sxs-lookup"><span data-stu-id="1bff7-289">Total one-way gap density.</span></span> <span data-ttu-id="1bff7-290">Одновременная передача данных — это передача, при которой данные передаются в непредсказуемые пакеты, а не в устойчивый поток. зазоры указывают на задержку между этими пакетами.</span><span class="sxs-lookup"><span data-stu-id="1bff7-290">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="1bff7-291">Этот показатель измеряет поток данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="1bff7-291">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="1bff7-292">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1bff7-292">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bff7-293"><strong>RelativeOneWayGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-293"><strong>RelativeOneWayGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-294">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="1bff7-294">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1bff7-295">Общая продолжительность односторонних промежутков.</span><span class="sxs-lookup"><span data-stu-id="1bff7-295">Total one-way gap duration.</span></span> <span data-ttu-id="1bff7-296">Одновременная передача данных — это передача, при которой данные передаются в непредсказуемые пакеты, а не в устойчивый поток. зазоры указывают на задержку между этими пакетами.</span><span class="sxs-lookup"><span data-stu-id="1bff7-296">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="1bff7-297">Этот показатель измеряет поток данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="1bff7-297">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="1bff7-298">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1bff7-298">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bff7-299"><strong>VideoPacketLossRate</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-299"><strong>VideoPacketLossRate</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-300">десятичное число (9; 4)</span><span class="sxs-lookup"><span data-stu-id="1bff7-300">decimal(9,4)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1bff7-301">Частота потери видеопакетов.</span><span class="sxs-lookup"><span data-stu-id="1bff7-301">Rate at which video packets were lost.</span></span></p>
<p><span data-ttu-id="1bff7-302">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1bff7-302">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bff7-303"><strong>VideoAllocateBWAvg</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-303"><strong>VideoAllocateBWAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-304">целое</span><span class="sxs-lookup"><span data-stu-id="1bff7-304">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1bff7-305">Средний объем пропускной способности, выделенной для видео.</span><span class="sxs-lookup"><span data-stu-id="1bff7-305">Average amount of bandwidth allocated for video.</span></span></p>
<p><span data-ttu-id="1bff7-306">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1bff7-306">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bff7-307"><strong>SendCodecTypes</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-307"><strong>SendCodecTypes</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-308">smallint</span><span class="sxs-lookup"><span data-stu-id="1bff7-308">smallint</span></span></p></td>
<td><p><span data-ttu-id="1bff7-309">Другом</span><span class="sxs-lookup"><span data-stu-id="1bff7-309">Foreign</span></span></p></td>
<td><p><span data-ttu-id="1bff7-310">Тип видеокодеков, используемых отправителем.</span><span class="sxs-lookup"><span data-stu-id="1bff7-310">Type of video codecs used by the sender.</span></span> <span data-ttu-id="1bff7-311">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-codecdescription-table.md">таблицей CodecDescription в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="1bff7-311">See the <a href="lync-server-2013-codecdescription-table.md">CodecDescription table in Lync Server 2013</a> for more information.</span></span></p>
<p><span data-ttu-id="1bff7-312">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1bff7-312">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bff7-313"><strong>SendResolutionWidth</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-313"><strong>SendResolutionWidth</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-314">целое</span><span class="sxs-lookup"><span data-stu-id="1bff7-314">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1bff7-315">Ширина разрешения, используемая отправителем.</span><span class="sxs-lookup"><span data-stu-id="1bff7-315">Resolution width used by the sender.</span></span></p>
<p><span data-ttu-id="1bff7-316">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1bff7-316">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bff7-317"><strong>SendResolutionHeight</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-317"><strong>SendResolutionHeight</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-318">целое</span><span class="sxs-lookup"><span data-stu-id="1bff7-318">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1bff7-319">Высота разрешения, используемая отправителем.</span><span class="sxs-lookup"><span data-stu-id="1bff7-319">Resolution height used by the sender.</span></span></p>
<p><span data-ttu-id="1bff7-320">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1bff7-320">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bff7-321"><strong>SendFrameRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-321"><strong>SendFrameRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-322">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="1bff7-322">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1bff7-323">Средняя скорость кадров видео, используемая отправителем.</span><span class="sxs-lookup"><span data-stu-id="1bff7-323">Average video frame rate transmission used by the sender.</span></span></p>
<p><span data-ttu-id="1bff7-324">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1bff7-324">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bff7-325"><strong>SendBitRateMaximum</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-325"><strong>SendBitRateMaximum</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-326">целое</span><span class="sxs-lookup"><span data-stu-id="1bff7-326">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1bff7-327">Максимальная скорость для отправителя.</span><span class="sxs-lookup"><span data-stu-id="1bff7-327">Maximum bit rate for the sender.</span></span></p>
<p><span data-ttu-id="1bff7-328">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1bff7-328">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bff7-329"><strong>SendBitRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-329"><strong>SendBitRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-330">целое</span><span class="sxs-lookup"><span data-stu-id="1bff7-330">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1bff7-331">Средняя скорость в битах для отправителя.</span><span class="sxs-lookup"><span data-stu-id="1bff7-331">Average bit rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bff7-332"><strong>SendVideoStreamsMax</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-332"><strong>SendVideoStreamsMax</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-333">целое</span><span class="sxs-lookup"><span data-stu-id="1bff7-333">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1bff7-334">Максимальное количество видеопотоков, используемых отправителем.</span><span class="sxs-lookup"><span data-stu-id="1bff7-334">Maximum number of video streams used by the sender.</span></span></p>
<p><span data-ttu-id="1bff7-335">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1bff7-335">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bff7-336"><strong>RecvCodecTypes</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-336"><strong>RecvCodecTypes</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-337">smallint</span><span class="sxs-lookup"><span data-stu-id="1bff7-337">smallint</span></span></p></td>
<td><p><span data-ttu-id="1bff7-338">Другом</span><span class="sxs-lookup"><span data-stu-id="1bff7-338">Foreign</span></span></p></td>
<td><p><span data-ttu-id="1bff7-339">Видео коды, используемые получателем.</span><span class="sxs-lookup"><span data-stu-id="1bff7-339">Video codes used by the receiver.</span></span> <span data-ttu-id="1bff7-340">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-codecdescription-table.md">таблицей CodecDescription в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="1bff7-340">See the <a href="lync-server-2013-codecdescription-table.md">CodecDescription table in Lync Server 2013</a> for more information.</span></span></p>
<p><span data-ttu-id="1bff7-341">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1bff7-341">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bff7-342"><strong>RecvResolutionWidth</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-342"><strong>RecvResolutionWidth</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-343">целое</span><span class="sxs-lookup"><span data-stu-id="1bff7-343">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1bff7-344">Ширина разрешения, используемая получателем.</span><span class="sxs-lookup"><span data-stu-id="1bff7-344">Resolution width used by the receiver.</span></span></p>
<p><span data-ttu-id="1bff7-345">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1bff7-345">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bff7-346"><strong>RecvResolutionHeight</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-346"><strong>RecvResolutionHeight</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-347">целое</span><span class="sxs-lookup"><span data-stu-id="1bff7-347">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1bff7-348">Высота разрешения, используемая получателем.</span><span class="sxs-lookup"><span data-stu-id="1bff7-348">Resolution height used by the receiver.</span></span></p>
<p><span data-ttu-id="1bff7-349">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1bff7-349">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bff7-350"><strong>RecvFrameRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-350"><strong>RecvFrameRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-351">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="1bff7-351">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1bff7-352">Средняя частота кадров видео, используемая получателем.</span><span class="sxs-lookup"><span data-stu-id="1bff7-352">Average video frame rate used by the receiver.</span></span></p>
<p><span data-ttu-id="1bff7-353">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1bff7-353">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bff7-354"><strong>RecvBitRateMaximum</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-354"><strong>RecvBitRateMaximum</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-355">целое</span><span class="sxs-lookup"><span data-stu-id="1bff7-355">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1bff7-356">Максимальная скорость потока для получателя.</span><span class="sxs-lookup"><span data-stu-id="1bff7-356">Maximum bit rate for the receiver.</span></span></p>
<p><span data-ttu-id="1bff7-357">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1bff7-357">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bff7-358"><strong>RecvBitRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-358"><strong>RecvBitRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-359">целое</span><span class="sxs-lookup"><span data-stu-id="1bff7-359">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1bff7-360">Средняя скорость потока для получателя.</span><span class="sxs-lookup"><span data-stu-id="1bff7-360">Average bit rate for the receiver.</span></span></p>
<p><span data-ttu-id="1bff7-361">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1bff7-361">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bff7-362"><strong>RecvVideoStreamsMax</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-362"><strong>RecvVideoStreamsMax</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-363">целое</span><span class="sxs-lookup"><span data-stu-id="1bff7-363">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1bff7-364">Максимальное количество видеопотоков для получателя.</span><span class="sxs-lookup"><span data-stu-id="1bff7-364">Maximum video streams for the receiver.</span></span></p>
<p><span data-ttu-id="1bff7-365">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1bff7-365">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bff7-366"><strong>RecvVideoStreamsMin</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-366"><strong>RecvVideoStreamsMin</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-367">целое</span><span class="sxs-lookup"><span data-stu-id="1bff7-367">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1bff7-368">Минимальный поток видеозаписи для получателя.</span><span class="sxs-lookup"><span data-stu-id="1bff7-368">Minimum video streams for the receiver.</span></span></p>
<p><span data-ttu-id="1bff7-369">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1bff7-369">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bff7-370"><strong>RecvVideoStreamsMode</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-370"><strong>RecvVideoStreamsMode</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-371">целое</span><span class="sxs-lookup"><span data-stu-id="1bff7-371">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1bff7-372">Режим видео (например, коллекция или один поток) получателя.</span><span class="sxs-lookup"><span data-stu-id="1bff7-372">Video mode (for example, gallery or single stream) for the receiver.</span></span></p>
<p><span data-ttu-id="1bff7-373">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1bff7-373">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bff7-374"><strong>VideoPostFECPLR</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-374"><strong>VideoPostFECPLR</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-375">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="1bff7-375">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1bff7-376">Применена ставка потери пакетов после исправления ошибки переадресации.</span><span class="sxs-lookup"><span data-stu-id="1bff7-376">Packet loss rate after forward error correction has been applied.</span></span></p>
<p><span data-ttu-id="1bff7-377">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1bff7-377">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bff7-378"><strong>DynamicCapabilityPercent</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-378"><strong>DynamicCapabilityPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-379">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="1bff7-379">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1bff7-380">Процент времени, в течение которого был активен флаг динамической доступности.</span><span class="sxs-lookup"><span data-stu-id="1bff7-380">Percentage of time that the dynamic capability flag was active.</span></span></p>
<p><span data-ttu-id="1bff7-381">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1bff7-381">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bff7-382"><strong>ResolutionMin</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-382"><strong>ResolutionMin</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-383">char (9)</span><span class="sxs-lookup"><span data-stu-id="1bff7-383">char(9)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1bff7-384">Минимальное разрешение, измеряемое во время звонка.</span><span class="sxs-lookup"><span data-stu-id="1bff7-384">Minimum resolution measured during the call.</span></span></p>
<p><span data-ttu-id="1bff7-385">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1bff7-385">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bff7-386"><strong>LowBitRateCallPercent</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-386"><strong>LowBitRateCallPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-387">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="1bff7-387">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1bff7-388">Процент звонка ниже минимального порогового значения скорости (70 килобит в секунду).</span><span class="sxs-lookup"><span data-stu-id="1bff7-388">Percentage of the call below the low bit rate threshold (70 kilobits per second).</span></span></p>
<p><span data-ttu-id="1bff7-389">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1bff7-389">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bff7-390"><strong>LowFrameRateCallPercent</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-390"><strong>LowFrameRateCallPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-391">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="1bff7-391">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1bff7-392">Процент звонка ниже нижнего порогового значения частоты кадров (количество кадров в 7,5 в секунду, входящее).</span><span class="sxs-lookup"><span data-stu-id="1bff7-392">Percentage of the call below the low frame rate threshold (7.5 frames per second, inbound).</span></span></p>
<p><span data-ttu-id="1bff7-393">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1bff7-393">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bff7-394"><strong>LowResolutionCallPercent</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-394"><strong>LowResolutionCallPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-395">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="1bff7-395">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1bff7-396">Процент звонка, который выполнялся по низким разрешению.</span><span class="sxs-lookup"><span data-stu-id="1bff7-396">Percentage of the call that occurred at the lowest resolution.</span></span></p>
<p><span data-ttu-id="1bff7-397">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1bff7-397">This column was introduced in Microsoft Lync Server 2013.</span></span></p>
<p><span data-ttu-id="1bff7-398">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1bff7-398">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bff7-399"><strong>DurationSeconds</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-399"><strong>DurationSeconds</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-400">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="1bff7-400">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1bff7-401">Продолжительность звонка в секундах.</span><span class="sxs-lookup"><span data-stu-id="1bff7-401">Length of the call in seconds.</span></span></p>
<p><span data-ttu-id="1bff7-402">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1bff7-402">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bff7-403"><strong>IsAggregatedData</strong></span><span class="sxs-lookup"><span data-stu-id="1bff7-403"><strong>IsAggregatedData</strong></span></span></p></td>
<td><p><span data-ttu-id="1bff7-404">бит</span><span class="sxs-lookup"><span data-stu-id="1bff7-404">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1bff7-405">Указывает, были ли данные объединены из нескольких вызовов.</span><span class="sxs-lookup"><span data-stu-id="1bff7-405">Indicates whether the data has been aggregated from multiple calls.</span></span></p>
<p><span data-ttu-id="1bff7-406">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1bff7-406">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="1bff7-407">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1bff7-407">


</div>

<span> </span>

</div>

</div>

</span></span></div>

