---
title: 'Lync Server 2013: таблица AudioClientEvent'
description: 'Таблица Lync Server 2013: AudioClientEvent.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: AudioClientEvent table
ms:assetid: fef73d8f-7261-4e5b-9769-82435b007979
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413086(v=OCS.15)
ms:contentKeyID: 48185967
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2200cd9567bdd10ac4ad8f5c269062c2f5614dcb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438212"
---
# <a name="audioclientevent-table-in-lync-server-2013"></a><span data-ttu-id="d09b4-103">Таблица AudioClientEvent в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d09b4-103">AudioClientEvent table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d09b4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d09b4-104">

<span> </span></span></span>

<span data-ttu-id="d09b4-105">_**Тема последнего изменения:** 2012-10-17_</span><span class="sxs-lookup"><span data-stu-id="d09b4-105">_**Topic Last Modified:** 2012-10-17_</span></span>

<span data-ttu-id="d09b4-106">Каждая запись имеет событие клиента для одной конечной точки в голосовой видеозвонке.</span><span class="sxs-lookup"><span data-stu-id="d09b4-106">Each record contains a client event for one endpoint in an audio call.</span></span> <span data-ttu-id="d09b4-107">Обычно один звонок состоит из двух записей: одного для вызывающего и для вызываемого абонента.</span><span class="sxs-lookup"><span data-stu-id="d09b4-107">Usually, one call has two records, one for caller and one for callee.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d09b4-108"><strong>Столбец</strong></span><span class="sxs-lookup"><span data-stu-id="d09b4-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="d09b4-109"><strong>Тип данных</strong></span><span class="sxs-lookup"><span data-stu-id="d09b4-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="d09b4-110"><strong>Ключ/индекс</strong></span><span class="sxs-lookup"><span data-stu-id="d09b4-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="d09b4-111"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="d09b4-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d09b4-112"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="d09b4-112"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="d09b4-113">datetime</span><span class="sxs-lookup"><span data-stu-id="d09b4-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="d09b4-114">Primary</span><span class="sxs-lookup"><span data-stu-id="d09b4-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="d09b4-115">На которую ссылается <a href="lync-server-2013-medialine-table.md">Таблица MediaLine в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="d09b4-115">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d09b4-116"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="d09b4-116"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="d09b4-117">целое</span><span class="sxs-lookup"><span data-stu-id="d09b4-117">int</span></span></p></td>
<td><p><span data-ttu-id="d09b4-118">Primary</span><span class="sxs-lookup"><span data-stu-id="d09b4-118">Primary</span></span></p></td>
<td><p><span data-ttu-id="d09b4-119">На которую ссылается <a href="lync-server-2013-medialine-table.md">Таблица MediaLine в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="d09b4-119">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d09b4-120"><strong>MediaLineLabel</strong></span><span class="sxs-lookup"><span data-stu-id="d09b4-120"><strong>MediaLineLabel</strong></span></span></p></td>
<td><p><span data-ttu-id="d09b4-121">tinyint</span><span class="sxs-lookup"><span data-stu-id="d09b4-121">tinyint</span></span></p></td>
<td><p><span data-ttu-id="d09b4-122">Primary</span><span class="sxs-lookup"><span data-stu-id="d09b4-122">Primary</span></span></p></td>
<td><p><span data-ttu-id="d09b4-123">На которую ссылается <a href="lync-server-2013-medialine-table.md">Таблица MediaLine в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="d09b4-123">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d09b4-124"><strong>FromCaller</strong></span><span class="sxs-lookup"><span data-stu-id="d09b4-124"><strong>FromCaller</strong></span></span></p></td>
<td><p><span data-ttu-id="d09b4-125">бит</span><span class="sxs-lookup"><span data-stu-id="d09b4-125">bit</span></span></p></td>
<td><p><span data-ttu-id="d09b4-126">Primary</span><span class="sxs-lookup"><span data-stu-id="d09b4-126">Primary</span></span></p></td>
<td><p><span data-ttu-id="d09b4-127">0: данные вызывающего абонента</span><span class="sxs-lookup"><span data-stu-id="d09b4-127">0: Callee’s data</span></span></p>
<p><span data-ttu-id="d09b4-128">1: данные вызывающего абонента</span><span class="sxs-lookup"><span data-stu-id="d09b4-128">1: Caller’s data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d09b4-129"><strong>NetworkSendQualityEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="d09b4-129"><strong>NetworkSendQualityEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="d09b4-130">десятичное число (5; 2)</span><span class="sxs-lookup"><span data-stu-id="d09b4-130">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="d09b4-131">Процент сеанса, когда событие NetworkSendQuality было инициировано для состояния "Bad".</span><span class="sxs-lookup"><span data-stu-id="d09b4-131">Percentage of session the NetworkSendQuality event was fired for ‘Bad’ state.</span></span></p>
<p><span data-ttu-id="d09b4-132">Качество сети в условиях нарушения или потери пакетов является серьезным и повлияет на качество отправляемого звука.</span><span class="sxs-lookup"><span data-stu-id="d09b4-132">Network quality in terms of jitter or packet loss is severe and impacting the quality of audio being sent.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d09b4-133"><strong>NetworkReceiveQualityEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="d09b4-133"><strong>NetworkReceiveQualityEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="d09b4-134">десятичное число (5; 2)</span><span class="sxs-lookup"><span data-stu-id="d09b4-134">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="d09b4-135">Процент сеанса, когда событие ReceiveSendQuality было инициировано для состояния "Bad".</span><span class="sxs-lookup"><span data-stu-id="d09b4-135">Percentage of session the ReceiveSendQuality event was fired for ‘Bad’ state.</span></span></p>
<p><span data-ttu-id="d09b4-136">Качество сети в условиях нарушения или потери пакетов является серьезным и повлияет на качество получаемого звука.</span><span class="sxs-lookup"><span data-stu-id="d09b4-136">Network quality in terms of jitter or packet loss is severe and impacting the quality of audio being received.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d09b4-137"><strong>NetworkDelayEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="d09b4-137"><strong>NetworkDelayEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="d09b4-138">десятичное число (5; 2)</span><span class="sxs-lookup"><span data-stu-id="d09b4-138">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="d09b4-139">Процент сеанса. событие задержки было инициировано для состояния "Bad".</span><span class="sxs-lookup"><span data-stu-id="d09b4-139">Percentage of session the Delay event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="d09b4-140">Задержка сети является серьезной и повлияет на работу, предотвращая интерактивную связь</span><span class="sxs-lookup"><span data-stu-id="d09b4-140">Network latency is severe and impacting the experience by preventing interactive communication</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d09b4-141"><strong>NetworkBandwidthLowEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="d09b4-141"><strong>NetworkBandwidthLowEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="d09b4-142">десятичное число (5; 2)</span><span class="sxs-lookup"><span data-stu-id="d09b4-142">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="d09b4-143">Процент сеанса, когда событие LowBandwidth было инициировано для состояния "Bad".</span><span class="sxs-lookup"><span data-stu-id="d09b4-143">Percentage of session the LowBandwidth event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="d09b4-144">Доступная пропускная способность недостаточна для приемлемого голосового интерфейса.</span><span class="sxs-lookup"><span data-stu-id="d09b4-144">The available bandwidth is insufficient for an acceptable voice experience.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d09b4-145"><strong>CPUInsufficientEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="d09b4-145"><strong>CPUInsufficientEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="d09b4-146">десятичное число (5; 2)</span><span class="sxs-lookup"><span data-stu-id="d09b4-146">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="d09b4-147">Процент пропускной ошибки ЦП, недостаточный для состояния "Bad".</span><span class="sxs-lookup"><span data-stu-id="d09b4-147">Percentage of session the insufficient CPU event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="d09b4-148">Недостаточно циклов ЦП для обработки с текущими модальностей и используемыми приложениями.</span><span class="sxs-lookup"><span data-stu-id="d09b4-148">There are insufficient CPU cycles for processing with the current modalities and applications in use.</span></span> <span data-ttu-id="d09b4-149">Это приводит к искажениям канала звука.</span><span class="sxs-lookup"><span data-stu-id="d09b4-149">This causes distortions with the audio channel.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d09b4-150"><strong>DeviceHalfDuplexAECEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="d09b4-150"><strong>DeviceHalfDuplexAECEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="d09b4-151">десятичное число (5; 2)</span><span class="sxs-lookup"><span data-stu-id="d09b4-151">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="d09b4-152">Процент сеанса, когда событие DeviceHalfDuplexAEC было инициировано для состояния "Bad".</span><span class="sxs-lookup"><span data-stu-id="d09b4-152">Percentage of session the DeviceHalfDuplexAEC event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="d09b4-153">В целях предотвращения эхо-эха система вводит двухстороннюю двустороннюю печать.</span><span class="sxs-lookup"><span data-stu-id="d09b4-153">In order to prevent echo, the system has enter half duplex.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d09b4-154"><strong>DeviceRenderNotFunctioningEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="d09b4-154"><strong>DeviceRenderNotFunctioningEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="d09b4-155">десятичное число (5; 2)</span><span class="sxs-lookup"><span data-stu-id="d09b4-155">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="d09b4-156">Процент сеанса, когда событие DeviceRenderNotFunctioning было инициировано для состояния "Bad".</span><span class="sxs-lookup"><span data-stu-id="d09b4-156">Percentage of session the DeviceRenderNotFunctioning event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="d09b4-157">Устройство рендеринга, используемое в данный момент для сеанса, работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="d09b4-157">The render device currently being used for the session is not functioning correctly.</span></span> <span data-ttu-id="d09b4-158">Это может привести к появлению односторонней голосовой проблемы.</span><span class="sxs-lookup"><span data-stu-id="d09b4-158">This can cause one-way audio issues.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d09b4-159"><strong>DeviceCaptureNotFunctioningEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="d09b4-159"><strong>DeviceCaptureNotFunctioningEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="d09b4-160">десятичное число (5; 2)</span><span class="sxs-lookup"><span data-stu-id="d09b4-160">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="d09b4-161">Процент сеанса, когда событие DeviceCaptureNotFunctioning было инициировано для состояния "Bad".</span><span class="sxs-lookup"><span data-stu-id="d09b4-161">Percentage of session the DeviceCaptureNotFunctioning event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="d09b4-162">Устройство захвата, используемое в сеансе, не работает должным образом.</span><span class="sxs-lookup"><span data-stu-id="d09b4-162">The capture device currently being used for the session is not functioning correctly.</span></span> <span data-ttu-id="d09b4-163">Это может привести к появлению односторонней голосовой проблемы.</span><span class="sxs-lookup"><span data-stu-id="d09b4-163">This can cause one-way audio issues.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d09b4-164"><strong>DeviceGlitchesEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="d09b4-164"><strong>DeviceGlitchesEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="d09b4-165">десятичное число (5; 2)</span><span class="sxs-lookup"><span data-stu-id="d09b4-165">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="d09b4-166">Процент сеанса, когда событие DeviceGlitches было инициировано для состояния "Bad".</span><span class="sxs-lookup"><span data-stu-id="d09b4-166">Percentage of session the DeviceGlitches event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="d09b4-167">При отрисовке звука возникают серьезные проблемы, вызывающие искажения.</span><span class="sxs-lookup"><span data-stu-id="d09b4-167">There are severe glitches in the rendering of audio which is causing distortions.</span></span> <span data-ttu-id="d09b4-168">Это может быть вызвано проблемами с драйверами, отложенными вызовами процедур (DPC) (Drivers) и высокой загрузкой ЦП.</span><span class="sxs-lookup"><span data-stu-id="d09b4-168">These glitches can be caused by driver issues, deferred procedure calls (DPC) storm (drivers), and high CPU usage.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d09b4-169"><strong>DeviceLowSNREventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="d09b4-169"><strong>DeviceLowSNREventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="d09b4-170">десятичное число (5; 2)</span><span class="sxs-lookup"><span data-stu-id="d09b4-170">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="d09b4-171">Процент сеанса, когда событие DeviceLowSNR было инициировано для состояния "Bad".</span><span class="sxs-lookup"><span data-stu-id="d09b4-171">Percentage of session the DeviceLowSNR event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="d09b4-172">Качество захвата очень низкое, но очень шумный или пользовательский разговор слишком далеко от микрофона.</span><span class="sxs-lookup"><span data-stu-id="d09b4-172">The capture quality is very poor, either very noisy or user is talking too far away from the microphone.</span></span> <span data-ttu-id="d09b4-173">Это вызовет искажения.</span><span class="sxs-lookup"><span data-stu-id="d09b4-173">This will cause distortions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d09b4-174"><strong>DeviceLowSpeechLevelEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="d09b4-174"><strong>DeviceLowSpeechLevelEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="d09b4-175">десятичное число (5; 2)</span><span class="sxs-lookup"><span data-stu-id="d09b4-175">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="d09b4-176">Процент сеанса, когда событие DeviceLowSpeechLevel было инициировано для состояния "Bad".</span><span class="sxs-lookup"><span data-stu-id="d09b4-176">Percentage of session the DeviceLowSpeechLevel event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="d09b4-177">Слишком низкий уровень речи пользователя, система не может увеличить его.</span><span class="sxs-lookup"><span data-stu-id="d09b4-177">User‘s speech level is too low and the system cannot increase it any further.</span></span> <span data-ttu-id="d09b4-178">Это может вызвать либо искажение или восприятие в качестве односторонней голосовой.</span><span class="sxs-lookup"><span data-stu-id="d09b4-178">This can either cause distortions or perceived as one-way audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d09b4-179"><strong>DeviceClippingEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="d09b4-179"><strong>DeviceClippingEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="d09b4-180">Десятичное число (5; 2)</span><span class="sxs-lookup"><span data-stu-id="d09b4-180">Decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="d09b4-181">Процент сеанса, когда событие DeviceClipping было инициировано для состояния "Bad".</span><span class="sxs-lookup"><span data-stu-id="d09b4-181">Percentage of session the DeviceClipping event was fired for ‘Bad’ state.</span></span></p>
<p><span data-ttu-id="d09b4-182">При использовании близких между собой видеороликов микрофон прозвучит искажения из-за обрезки.</span><span class="sxs-lookup"><span data-stu-id="d09b4-182">When near-end speech clips the microphone, far-end hears distortion due to clipping.</span></span> <span data-ttu-id="d09b4-183">Важно избегать вырезки близких микрофонов.</span><span class="sxs-lookup"><span data-stu-id="d09b4-183">It is important to avoid near-end microphone clipping.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d09b4-184"><strong>DeviceEchoEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="d09b4-184"><strong>DeviceEchoEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="d09b4-185">десятичное число (5; 2)</span><span class="sxs-lookup"><span data-stu-id="d09b4-185">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="d09b4-186">Процент сеанса, когда событие DeviceEchoEvent было инициировано для состояния "Bad".</span><span class="sxs-lookup"><span data-stu-id="d09b4-186">Percentage of session the DeviceEchoEvent event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="d09b4-187">Устройство или Настройка вызывают эхо за пределами способности системы компенсировать.</span><span class="sxs-lookup"><span data-stu-id="d09b4-187">Device or setup is causing echo beyond the ability of the system to compensate.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d09b4-188"><strong>DeviceNearEndToEchoRatioEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="d09b4-188"><strong>DeviceNearEndToEchoRatioEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="d09b4-189">десятичное число (5; 2)</span><span class="sxs-lookup"><span data-stu-id="d09b4-189">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="d09b4-190">Процент сеанса, когда событие DeviceNearEndToEchoRatio было инициировано для состояния "Bad".</span><span class="sxs-lookup"><span data-stu-id="d09b4-190">Percentage of session the DeviceNearEndToEchoRatio event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="d09b4-191">Голосовая речь пользователя слишком мала по сравнению с записанным эхо-эффектом, что влияет на работу пользователей, так как оно ограничивает возможности прерывания пользователя.</span><span class="sxs-lookup"><span data-stu-id="d09b4-191">The user’s speech is too low compared to the echo being captured which impacts the users experience because it limits how easy it is to interrupt a user.</span></span> <span data-ttu-id="d09b4-192">Уменьшить громкость динамика, передвиньте микрофон ближе к разговору.</span><span class="sxs-lookup"><span data-stu-id="d09b4-192">Reduce speaker volume, move the microphone closer to the talker.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d09b4-193"><strong>DeviceMultipleEndpointsEventCount</strong></span><span class="sxs-lookup"><span data-stu-id="d09b4-193"><strong>DeviceMultipleEndpointsEventCount</strong></span></span></p></td>
<td><p><span data-ttu-id="d09b4-194">целое</span><span class="sxs-lookup"><span data-stu-id="d09b4-194">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d09b4-195">Количество ситуаций, в которых событие DeviceMultipleEndpoints было инициировано для состояния "Bad".</span><span class="sxs-lookup"><span data-stu-id="d09b4-195">Number of times during session the DeviceMultipleEndpoints event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="d09b4-196">Обнаружено несколько конечных точек звука в одном сеансе и компенсация системы была произведена с помощью уменьшения объема рендеринга.</span><span class="sxs-lookup"><span data-stu-id="d09b4-196">Multiple audio endpoints in the same session detected and the system has compensated by reducing render volume.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d09b4-197"><strong>DeviceHowlingEventCount</strong></span><span class="sxs-lookup"><span data-stu-id="d09b4-197"><strong>DeviceHowlingEventCount</strong></span></span></p></td>
<td><p><span data-ttu-id="d09b4-198">целое</span><span class="sxs-lookup"><span data-stu-id="d09b4-198">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="d09b4-199">Количество ситуаций, в которых событие DeviceHowlingEvent было инициировано для состояния "Bad".</span><span class="sxs-lookup"><span data-stu-id="d09b4-199">Number of times during session the DeviceHowlingEvent event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="d09b4-200">Обнаружен цикл обратной связи (это связано с тем, что несколько конечных точек совместно поддерживают звуковой путь).</span><span class="sxs-lookup"><span data-stu-id="d09b4-200">Audio feedback loop detected (caused by multiple endpoints sharing audio path).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d09b4-201"><strong>DeviceRenderZeroVolumeEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="d09b4-201"><strong>DeviceRenderZeroVolumeEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="d09b4-202">десятичное число (5; 2)</span><span class="sxs-lookup"><span data-stu-id="d09b4-202">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d09b4-203">Процент сеанса. событие DeviceRenderZeroVolume было инициировано в состоянии Bad.</span><span class="sxs-lookup"><span data-stu-id="d09b4-203">Percentage of session the DeviceRenderZeroVolume event was fired for being in the “Bad’ state.</span></span> <span data-ttu-id="d09b4-204">Для устройства обработки было установлено нулевое значение "Громкость".</span><span class="sxs-lookup"><span data-stu-id="d09b4-204">The render device was set to zero volume.</span></span></p>
<p><span data-ttu-id="d09b4-205">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d09b4-205">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d09b4-206"><strong>DeviceRenderMuteEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="d09b4-206"><strong>DeviceRenderMuteEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="d09b4-207">десятичное число (5; 2)</span><span class="sxs-lookup"><span data-stu-id="d09b4-207">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d09b4-208">Процент сеанса. событие DeviceRenderMute было инициировано в состоянии Bad.</span><span class="sxs-lookup"><span data-stu-id="d09b4-208">Percentage of session the DeviceRenderMute event was fired for being in the “Bad’ state.</span></span> <span data-ttu-id="d09b4-209">Устройство рендеринга отключено.</span><span class="sxs-lookup"><span data-stu-id="d09b4-209">The render device was muted.</span></span></p>
<p><span data-ttu-id="d09b4-210">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d09b4-210">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="d09b4-211">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d09b4-211">


</div>

<span> </span>

</div>

</div>

</span></span></div>

