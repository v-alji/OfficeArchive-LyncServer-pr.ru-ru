---
title: 'Lync Server 2013: таблица AudioSignal'
description: 'Таблица Lync Server 2013: AudioSignal.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: AudioSignal table
ms:assetid: 0013c8c6-cdf9-4d70-bc2a-cddd1560f66b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398064(v=OCS.15)
ms:contentKeyID: 48183217
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 82f3b3119eaccfe56c4706cff07469bc3434461f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438208"
---
# <a name="audiosignal-table-in-lync-server-2013"></a><span data-ttu-id="4d3f5-103">Таблица AudioSignal в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4d3f5-103">AudioSignal table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4d3f5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4d3f5-104">

<span> </span></span></span>

<span data-ttu-id="4d3f5-105">_**Тема последнего изменения:** 2013-11-12_</span><span class="sxs-lookup"><span data-stu-id="4d3f5-105">_**Topic Last Modified:** 2013-11-12_</span></span>

<span data-ttu-id="4d3f5-106">Каждая запись представляет метрики звукового сигнала для одной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-106">Each record represents audio signal metrics for one endpoint.</span></span> <span data-ttu-id="4d3f5-107">Обычно каждый звонок состоит из двух записей: одной из них, а другая — для вызываемого абонента.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-107">Usually, each call has two records, one is for caller, and one is for callee.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4d3f5-108"><strong>Столбец</strong></span><span class="sxs-lookup"><span data-stu-id="4d3f5-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="4d3f5-109"><strong>Тип данных</strong></span><span class="sxs-lookup"><span data-stu-id="4d3f5-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="4d3f5-110"><strong>Ключ/индекс</strong></span><span class="sxs-lookup"><span data-stu-id="4d3f5-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="4d3f5-111"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="4d3f5-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4d3f5-112"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="4d3f5-112"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="4d3f5-113">datetime</span><span class="sxs-lookup"><span data-stu-id="4d3f5-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="4d3f5-114">Primary</span><span class="sxs-lookup"><span data-stu-id="4d3f5-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="4d3f5-115">На которую ссылается <a href="lync-server-2013-medialine-table.md">Таблица MediaLine в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-115">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d3f5-116"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="4d3f5-116"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="4d3f5-117">целое</span><span class="sxs-lookup"><span data-stu-id="4d3f5-117">int</span></span></p></td>
<td><p><span data-ttu-id="4d3f5-118">Primary</span><span class="sxs-lookup"><span data-stu-id="4d3f5-118">Primary</span></span></p></td>
<td><p><span data-ttu-id="4d3f5-119">На которую ссылается <a href="lync-server-2013-medialine-table.md">Таблица MediaLine в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-119">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d3f5-120"><strong>MediaLineLabel</strong></span><span class="sxs-lookup"><span data-stu-id="4d3f5-120"><strong>MediaLineLabel</strong></span></span></p></td>
<td><p><span data-ttu-id="4d3f5-121">tinyint</span><span class="sxs-lookup"><span data-stu-id="4d3f5-121">tinyint</span></span></p></td>
<td><p><span data-ttu-id="4d3f5-122">Primary</span><span class="sxs-lookup"><span data-stu-id="4d3f5-122">Primary</span></span></p></td>
<td><p><span data-ttu-id="4d3f5-123">На которую ссылается <a href="lync-server-2013-medialine-table.md">Таблица MediaLine в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-123">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d3f5-124"><strong>FromCaller</strong></span><span class="sxs-lookup"><span data-stu-id="4d3f5-124"><strong>FromCaller</strong></span></span></p></td>
<td><p><span data-ttu-id="4d3f5-125">бит</span><span class="sxs-lookup"><span data-stu-id="4d3f5-125">bit</span></span></p></td>
<td><p><span data-ttu-id="4d3f5-126">Primary</span><span class="sxs-lookup"><span data-stu-id="4d3f5-126">Primary</span></span></p></td>
<td><p><span data-ttu-id="4d3f5-127">0: данные вызывающего абонента</span><span class="sxs-lookup"><span data-stu-id="4d3f5-127">0: Callee’s data</span></span></p>
<p><span data-ttu-id="4d3f5-128">1: данные вызывающего абонента</span><span class="sxs-lookup"><span data-stu-id="4d3f5-128">1: Caller’s data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d3f5-129"><strong>SendSignalLevel</strong></span><span class="sxs-lookup"><span data-stu-id="4d3f5-129"><strong>SendSignalLevel</strong></span></span></p></td>
<td><p><span data-ttu-id="4d3f5-130">целое</span><span class="sxs-lookup"><span data-stu-id="4d3f5-130">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="4d3f5-131">Обозначает уровень звукового сигнала после аналогового усиления контроля.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-131">Represents the Post-Analog Gain Control audio signal level.</span></span> <span data-ttu-id="4d3f5-132">Единицей измерения для этой метрики является dBmo.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-132">The unit for this metric is dBmo.</span></span> <span data-ttu-id="4d3f5-133">Для приемлемого качества оно должно быть не менее 30 dBmo.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-133">For acceptable quality, it should be at least 30 dBmo.</span></span> <span data-ttu-id="4d3f5-134">Этот показатель не передается сервером Конференции и IP-телефонами по протоколу A/V.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-134">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d3f5-135"><strong>RecvSignalLevel</strong></span><span class="sxs-lookup"><span data-stu-id="4d3f5-135"><strong>RecvSignalLevel</strong></span></span></p></td>
<td><p><span data-ttu-id="4d3f5-136">целое</span><span class="sxs-lookup"><span data-stu-id="4d3f5-136">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="4d3f5-137">Смотрите SendSignalLevel.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-137">See SendSignalLevel.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d3f5-138"><strong>SendNoiseLevel</strong></span><span class="sxs-lookup"><span data-stu-id="4d3f5-138"><strong>SendNoiseLevel</strong></span></span></p></td>
<td><p><span data-ttu-id="4d3f5-139">целое</span><span class="sxs-lookup"><span data-stu-id="4d3f5-139">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="4d3f5-140">Обозначает уровень звукового шума, поступающего после аналогового усиления.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-140">Represents the Post-Analog Gain Control audio noise level.</span></span> <span data-ttu-id="4d3f5-141">Единицей измерения для этой метрики является dBmo.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-141">The unit for this metric is dBmo.</span></span> <span data-ttu-id="4d3f5-142">Для приемлемого качества оно должно быть менее 35 dBmo.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-142">For acceptable quality, it should be less than 35 dBmo.</span></span> <span data-ttu-id="4d3f5-143">Этот показатель не передается сервером Конференции и IP-телефонами по протоколу A/V.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-143">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d3f5-144"><strong>RecvNoiseLevel</strong></span><span class="sxs-lookup"><span data-stu-id="4d3f5-144"><strong>RecvNoiseLevel</strong></span></span></p></td>
<td><p><span data-ttu-id="4d3f5-145">целое</span><span class="sxs-lookup"><span data-stu-id="4d3f5-145">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="4d3f5-146">Смотрите SendNoiseLevel.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-146">See SendNoiseLevel.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d3f5-147"><strong>EchoReturn</strong></span><span class="sxs-lookup"><span data-stu-id="4d3f5-147"><strong>EchoReturn</strong></span></span></p></td>
<td><p><span data-ttu-id="4d3f5-148">целое</span><span class="sxs-lookup"><span data-stu-id="4d3f5-148">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="4d3f5-149">Показатель возвращающего потери при возврате эха.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-149">Echo Return Loss Enhancement metric.</span></span> <span data-ttu-id="4d3f5-150">Единицей измерения для этой метрики является dB.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-150">The unit for this metric is dB.</span></span> <span data-ttu-id="4d3f5-151">Более низкие значения представляют менее эхо.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-151">Lower values represent less echo.</span></span> <span data-ttu-id="4d3f5-152">Этот показатель не передается сервером Конференции и IP-телефонами по протоколу A/V.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-152">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d3f5-153"><strong>AudioSpeakerGlitchRate</strong></span><span class="sxs-lookup"><span data-stu-id="4d3f5-153"><strong>AudioSpeakerGlitchRate</strong></span></span></p></td>
<td><p><span data-ttu-id="4d3f5-154">целое</span><span class="sxs-lookup"><span data-stu-id="4d3f5-154">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="4d3f5-155">Среднее число сбоев в течение пяти минут для отрисовки динамик.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-155">Average glitches per five minutes for the loudspeaker rendering.</span></span> <span data-ttu-id="4d3f5-156">Для хорошего качества это должно быть меньше, чем один за пять минут.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-156">For good quality, this should be less than one per five minutes.</span></span> <span data-ttu-id="4d3f5-157">Не сообщается серверам конференц-связи, серверам или IP-телефонам.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-157">Not reported by A/V Conferencing Servers, Mediation Servers, or IP phones.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d3f5-158"><strong>AudioMicGlitchRate</strong></span><span class="sxs-lookup"><span data-stu-id="4d3f5-158"><strong>AudioMicGlitchRate</strong></span></span></p></td>
<td><p><span data-ttu-id="4d3f5-159">целое</span><span class="sxs-lookup"><span data-stu-id="4d3f5-159">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="4d3f5-160">Среднее число сбоев в течение пяти минут для захвата микрофона.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-160">Average glitches per five minutes for the microphone capture.</span></span> <span data-ttu-id="4d3f5-161">Для хорошего качества это должно быть менее чем на одну 5 минут.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-161">For good quality this should be less than one per five minutes.</span></span> <span data-ttu-id="4d3f5-162">Не сообщается серверам конференц-связи, серверам или IP-телефонам.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-162">Not reported by A/V Conferencing Servers, Mediation Servers, or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d3f5-163"><strong>AudioTimestampDriftRateMic</strong></span><span class="sxs-lookup"><span data-stu-id="4d3f5-163"><strong>AudioTimestampDriftRateMic</strong></span></span></p></td>
<td><p><span data-ttu-id="4d3f5-164">десятичное число (9, 2)</span><span class="sxs-lookup"><span data-stu-id="4d3f5-164">decimal(9,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="4d3f5-165">Частота расхождения синхронизирующих сигналов для микрофона, относящихся к тактовой частоте процессора.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-165">Microphone device clock drift rate, relative to CPU clock.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d3f5-166"><strong>AudioTimestampDriftRateSpk</strong></span><span class="sxs-lookup"><span data-stu-id="4d3f5-166"><strong>AudioTimestampDriftRateSpk</strong></span></span></p></td>
<td><p><span data-ttu-id="4d3f5-167">десятичное число (9, 2)</span><span class="sxs-lookup"><span data-stu-id="4d3f5-167">decimal(9,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="4d3f5-168">Частота расхождения синхронизирующих импульсов устройства для динамиков относительно часов процессора.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-168">Speaker device clock drift rate, relative to CPU clock.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d3f5-169"><strong>AudioTimestampErrorMicMs</strong></span><span class="sxs-lookup"><span data-stu-id="4d3f5-169"><strong>AudioTimestampErrorMicMs</strong></span></span></p></td>
<td><p><span data-ttu-id="4d3f5-170">десятичное число (9, 2)</span><span class="sxs-lookup"><span data-stu-id="4d3f5-170">decimal(9,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="4d3f5-171">Частота расхождения синхронизирующих импульсов устройства для динамиков относительно часов процессора.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-171">Speaker device clock drift rate, relative to CPU clock.</span></span></p>
<p><span data-ttu-id="4d3f5-172">Средняя пометка времени потока захвата микрофона в миллисекундах за последние 20 секунд звонка.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-172">Average microphone capture stream time stamp error, in milliseconds, in the last 20 seconds of the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d3f5-173"><strong>AudioTimestampErrorSpkMs</strong></span><span class="sxs-lookup"><span data-stu-id="4d3f5-173"><strong>AudioTimestampErrorSpkMs</strong></span></span></p></td>
<td><p><span data-ttu-id="4d3f5-174">десятичное число (9, 2)</span><span class="sxs-lookup"><span data-stu-id="4d3f5-174">decimal(9,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="4d3f5-175">Средняя отметка времени линейного потока обработки динамиков в миллисекундах за последние 20 секунд вызова.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-175">Average speaker render stream time stamp error, in milliseconds, in the last 20 seconds of the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d3f5-176"><strong>VsEntryCauses</strong></span><span class="sxs-lookup"><span data-stu-id="4d3f5-176"><strong>VsEntryCauses</strong></span></span></p></td>
<td><p><span data-ttu-id="4d3f5-177">smallint</span><span class="sxs-lookup"><span data-stu-id="4d3f5-177">smallint</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="4d3f5-178">Голосовая связь — это режим двусторонней печати с ограниченными возможностями перерывов.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-178">Voice switch is a half-duplex mode with reduced interruption ability.</span></span> <span data-ttu-id="4d3f5-179">Причины для записи голосового переключателя:</span><span class="sxs-lookup"><span data-stu-id="4d3f5-179">Causes of voice switch entry:</span></span></p>
<p><span data-ttu-id="4d3f5-180">ENTER_VS_BADTS 0x01</span><span class="sxs-lookup"><span data-stu-id="4d3f5-180">ENTER_VS_BADTS 0x01</span></span></p>
<p><span data-ttu-id="4d3f5-181">ENTER_VS_ECHO 0x02</span><span class="sxs-lookup"><span data-stu-id="4d3f5-181">ENTER_VS_ECHO 0x02</span></span></p>
<p><span data-ttu-id="4d3f5-182">ENTER_VS_FORCEORCONVERGENCE 0x04</span><span class="sxs-lookup"><span data-stu-id="4d3f5-182">ENTER_VS_FORCEORCONVERGENCE 0x04</span></span></p>
<p><span data-ttu-id="4d3f5-183">ENTER_VS_DNLP 0x08</span><span class="sxs-lookup"><span data-stu-id="4d3f5-183">ENTER_VS_DNLP 0x08</span></span></p>
<p><span data-ttu-id="4d3f5-184">Причина может быть сочетанием отдельных причин.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-184">The cause can be a combination of those individual causes.</span></span> <span data-ttu-id="4d3f5-185">ENTER_VS_FORCEORCONVERGENCE может быть включена только в RegKey для целей тестирования.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-185">ENTER_VS_FORCEORCONVERGENCE can only be enabled by regkey for test purpose.</span></span></p>
<p><span data-ttu-id="4d3f5-186">Тип данных этого столбца изменен в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-186">The data type for this column was changed in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d3f5-187"><strong>EchoEventCauses</strong></span><span class="sxs-lookup"><span data-stu-id="4d3f5-187"><strong>EchoEventCauses</strong></span></span></p></td>
<td><p><span data-ttu-id="4d3f5-188">tinyint</span><span class="sxs-lookup"><span data-stu-id="4d3f5-188">tinyint</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="4d3f5-189">Причины возникновения события echo:</span><span class="sxs-lookup"><span data-stu-id="4d3f5-189">Causes of an echo event:</span></span></p>
<p><span data-ttu-id="4d3f5-190">ECHO_EVENT_BAD_TIMESTAMP 0x01</span><span class="sxs-lookup"><span data-stu-id="4d3f5-190">ECHO_EVENT_BAD_TIMESTAMP 0x01</span></span></p>
<p><span data-ttu-id="4d3f5-191">ECHO_EVENT_POSTAEC_ECHO 0x02</span><span class="sxs-lookup"><span data-stu-id="4d3f5-191">ECHO_EVENT_POSTAEC_ECHO 0x02</span></span></p>
<p><span data-ttu-id="4d3f5-192">ECHO_EVENT_ANLP 0x04</span><span class="sxs-lookup"><span data-stu-id="4d3f5-192">ECHO_EVENT_ANLP 0x04</span></span></p>
<p><span data-ttu-id="4d3f5-193">ECHO_EVENT_DNLP 0x08</span><span class="sxs-lookup"><span data-stu-id="4d3f5-193">ECHO_EVENT_DNLP 0x08</span></span></p>
<p><span data-ttu-id="4d3f5-194">ECHO_EVENT_MIC_CLIPPING 0x10</span><span class="sxs-lookup"><span data-stu-id="4d3f5-194">ECHO_EVENT_MIC_CLIPPING 0x10</span></span></p>
<p><span data-ttu-id="4d3f5-195">ECHO_EVENT_BAD_STATE 0x20</span><span class="sxs-lookup"><span data-stu-id="4d3f5-195">ECHO_EVENT_BAD_STATE 0x20</span></span></p>
<p><span data-ttu-id="4d3f5-196">Причина может быть сочетанием отдельных причин.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-196">The cause can be a combination of those individual causes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d3f5-197"><strong>EchoPercentMicIn</strong></span><span class="sxs-lookup"><span data-stu-id="4d3f5-197"><strong>EchoPercentMicIn</strong></span></span></p></td>
<td><p><span data-ttu-id="4d3f5-198">десятичное число (5; 2)</span><span class="sxs-lookup"><span data-stu-id="4d3f5-198">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="4d3f5-p109">Процент времени, когда в потоке захвата микрофоном обнаруживался эхосигнал. Обычно низкие значения отображаются для гарнитур или телефонных трубок, а высокие значения – для телефонных или автономных динамиков. Для устройств, которые поддерживают встроенную возможность подавления акустического эхосигнала, высокие значения указывают утечку эхосигнала. Для других устройств эти единицы измерения не должны использоваться для оценки качества устройства.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-p109">Percentage of time when echo was detected in the microphone capture stream. Typically, values are low for headsets or handsets, and higher for speaker phones or stand-alone speakers. For devices that support on-board acoustic echo cancellation, high values indicate echo leak. For other devices, this metric should not be used to evaluate device quality.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d3f5-203"><strong>EchoPercentSend</strong></span><span class="sxs-lookup"><span data-stu-id="4d3f5-203"><strong>EchoPercentSend</strong></span></span></p></td>
<td><p><span data-ttu-id="4d3f5-204">десятичное число (5; 2)</span><span class="sxs-lookup"><span data-stu-id="4d3f5-204">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="4d3f5-205">Процент времени, в течение которого обнаружено Эхо-сообщение в отправленном потоке.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-205">Percentage of time when echo is detected in sent stream.</span></span> <span data-ttu-id="4d3f5-206">Высокий процент эха в потоках отправки указывает на наличие утечки эха.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-206">High echo percentage in send streams an indication of echo leak.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d3f5-207"><strong>RxAGCSignalLevel</strong></span><span class="sxs-lookup"><span data-stu-id="4d3f5-207"><strong>RxAGCSignalLevel</strong></span></span></p></td>
<td><p><span data-ttu-id="4d3f5-208">целое</span><span class="sxs-lookup"><span data-stu-id="4d3f5-208">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="4d3f5-209">Уровень сигнала на сервере обновлений от шлюза; Это относится только к серверу обновлений.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-209">Received signal level on the Mediation Server from the Gateway; this applies only to the Mediation Server.</span></span> <span data-ttu-id="4d3f5-210">Единица измерения этой метрики — dBoV.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-210">The unit of this metric is dBoV.</span></span> <span data-ttu-id="4d3f5-211">Для хорошего качества допустимый диапазон должен составлять от [-30 до-18] dBoV.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-211">For good quality, the acceptable range should be [-30 to -18] dBoV.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d3f5-212"><strong>RxAGCNoiseLevel</strong></span><span class="sxs-lookup"><span data-stu-id="4d3f5-212"><strong>RxAGCNoiseLevel</strong></span></span></p></td>
<td><p><span data-ttu-id="4d3f5-213">целое</span><span class="sxs-lookup"><span data-stu-id="4d3f5-213">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="4d3f5-214">Уровень сигнала на сервере обновлений от шлюза.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-214">Received signal level on the Mediation Server from the Gateway.</span></span> <span data-ttu-id="4d3f5-215">Это относится только к серверу обновлений.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-215">This applies only to the Mediation Server.</span></span> <span data-ttu-id="4d3f5-216">Единица измерения этой метрики — dBoV.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-216">The unit of this metric is dBoV.</span></span> <span data-ttu-id="4d3f5-217">Для хорошего качества допустимый диапазон должен быть меньше, чем-50 dBoV.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-217">For good quality, the acceptable range should be less than -50 dBoV.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d3f5-218"><strong>RxAvgAGCGain</strong></span><span class="sxs-lookup"><span data-stu-id="4d3f5-218"><strong>RxAvgAGCGain</strong></span></span></p></td>
<td><p><span data-ttu-id="4d3f5-219">целое</span><span class="sxs-lookup"><span data-stu-id="4d3f5-219">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="4d3f5-220">Автоматический контроль усиления (AGC) на стороне сервера-посредника.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-220">Automatic gain control (AGC) on the Mediation Server side.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d3f5-221"><strong>InitialSignalLevelRMS</strong></span><span class="sxs-lookup"><span data-stu-id="4d3f5-221"><strong>InitialSignalLevelRMS</strong></span></span></p></td>
<td><p><span data-ttu-id="4d3f5-222">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="4d3f5-222">float</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="4d3f5-223">Среднее значение среднего квадрата для входящего сигнала, которое составляет до первых 30 секунд звонка.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-223">The root mean square (RMS) of the incoming signal of up to the first 30 seconds of the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d3f5-224"><strong>RecvSignalLevelCh1</strong></span><span class="sxs-lookup"><span data-stu-id="4d3f5-224"><strong>RecvSignalLevelCh1</strong></span></span></p></td>
<td><p><span data-ttu-id="4d3f5-225">целое</span><span class="sxs-lookup"><span data-stu-id="4d3f5-225">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="4d3f5-226">Уровень сигнала, полученный на канале 1.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-226">Signal level as received on channel 1.</span></span></p>
<p><span data-ttu-id="4d3f5-227">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-227">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d3f5-228"><strong>RecvSignalLevelCh2</strong></span><span class="sxs-lookup"><span data-stu-id="4d3f5-228"><strong>RecvSignalLevelCh2</strong></span></span></p></td>
<td><p><span data-ttu-id="4d3f5-229">целое</span><span class="sxs-lookup"><span data-stu-id="4d3f5-229">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="4d3f5-230">Уровень сигнала, полученный на канале 2.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-230">Signal level as received on channel 2.</span></span></p>
<p><span data-ttu-id="4d3f5-231">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-231">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d3f5-232"><strong>RecvNoiseLevelCh1</strong></span><span class="sxs-lookup"><span data-stu-id="4d3f5-232"><strong>RecvNoiseLevelCh1</strong></span></span></p></td>
<td><p><span data-ttu-id="4d3f5-233">целое</span><span class="sxs-lookup"><span data-stu-id="4d3f5-233">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="4d3f5-234">Уровень шума, полученный на канале 1.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-234">Noise level as received on channel 1.</span></span></p>
<p><span data-ttu-id="4d3f5-235">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-235">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d3f5-236"><strong>RecvNoiseLevelCh2</strong></span><span class="sxs-lookup"><span data-stu-id="4d3f5-236"><strong>RecvNoiseLevelCh2</strong></span></span></p></td>
<td><p><span data-ttu-id="4d3f5-237">целое</span><span class="sxs-lookup"><span data-stu-id="4d3f5-237">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="4d3f5-238">Уровень шума, полученный на канале 2.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-238">Noise level as received on channel 2.</span></span></p>
<p><span data-ttu-id="4d3f5-239">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-239">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d3f5-240"><strong>SendSignalLevelCh1</strong></span><span class="sxs-lookup"><span data-stu-id="4d3f5-240"><strong>SendSignalLevelCh1</strong></span></span></p></td>
<td><p><span data-ttu-id="4d3f5-241">целое</span><span class="sxs-lookup"><span data-stu-id="4d3f5-241">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="4d3f5-242">Уровень сигнала, отправленный на канале 1.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-242">Signal level as sent on channel 1.</span></span></p>
<p><span data-ttu-id="4d3f5-243">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-243">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d3f5-244"><strong>SendSignalLevelCh2</strong></span><span class="sxs-lookup"><span data-stu-id="4d3f5-244"><strong>SendSignalLevelCh2</strong></span></span></p></td>
<td><p><span data-ttu-id="4d3f5-245">целое</span><span class="sxs-lookup"><span data-stu-id="4d3f5-245">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="4d3f5-246">Уровень сигнала, отправленный на канале 2.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-246">Signal level as sent on channel 2.</span></span></p>
<p><span data-ttu-id="4d3f5-247">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-247">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d3f5-248"><strong>SendNoiseLevelCh1</strong></span><span class="sxs-lookup"><span data-stu-id="4d3f5-248"><strong>SendNoiseLevelCh1</strong></span></span></p></td>
<td><p><span data-ttu-id="4d3f5-249">целое</span><span class="sxs-lookup"><span data-stu-id="4d3f5-249">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="4d3f5-250">Уровень шума, отправленный на канале 1.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-250">Noise level as sent on channel 1.</span></span></p>
<p><span data-ttu-id="4d3f5-251">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-251">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d3f5-252"><strong>SendNoiseLevelCh2</strong></span><span class="sxs-lookup"><span data-stu-id="4d3f5-252"><strong>SendNoiseLevelCh2</strong></span></span></p></td>
<td><p><span data-ttu-id="4d3f5-253">целое</span><span class="sxs-lookup"><span data-stu-id="4d3f5-253">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="4d3f5-254">Уровень шума, отправленный на канале 2.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-254">Noise level as sent on channel 2.</span></span></p>
<p><span data-ttu-id="4d3f5-255">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-255">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="4d3f5-256">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4d3f5-256">


</div>

<span> </span>

</div>

</div>

</span></span></div>

