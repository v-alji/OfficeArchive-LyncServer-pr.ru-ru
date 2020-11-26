---
title: 'Lync Server 2013: таблица MediaLine'
description: 'Таблица Lync Server 2013: MediaLine.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: MediaLine table
ms:assetid: 414b1d63-ae97-4c27-bac0-c9ad0f808ff0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425920(v=OCS.15)
ms:contentKeyID: 48183956
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2acea8e14ba0608d9ebf72a48f888bfc4501fae3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425621"
---
# <a name="medialine-table-in-lync-server-2013"></a><span data-ttu-id="04795-103">Таблица MediaLine в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="04795-103">MediaLine table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="04795-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="04795-104">

<span> </span></span></span>

<span data-ttu-id="04795-105">_**Тема последнего изменения:** 2014-02-21_</span><span class="sxs-lookup"><span data-stu-id="04795-105">_**Topic Last Modified:** 2014-02-21_</span></span>

<span data-ttu-id="04795-106">Каждая запись представляет одну сеть мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="04795-106">Each record represents one media line.</span></span> <span data-ttu-id="04795-107">(Один звуковой сеанс обычно состоит из одной линии звукового файла.</span><span class="sxs-lookup"><span data-stu-id="04795-107">(One audio session usually contains one audio media line.</span></span> <span data-ttu-id="04795-108">Один из звуковых и видеофайлов (A/V) обычно содержит одну строку звукового файла и одну строку видеофайла, хотя в этом сеансе может быть две видеоустройства, если используется устройство конференц-связи или режим галереи.</span><span class="sxs-lookup"><span data-stu-id="04795-108">One audio and video (A/V) session usually contains one audio media line and one video media line, although the session might contain two video media lines if a conferencing device is used or if Gallery View is used.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="04795-109"><strong>Столбец</strong></span><span class="sxs-lookup"><span data-stu-id="04795-109"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="04795-110"><strong>Тип данных</strong></span><span class="sxs-lookup"><span data-stu-id="04795-110"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="04795-111"><strong>Ключ/индекс</strong></span><span class="sxs-lookup"><span data-stu-id="04795-111"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="04795-112"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="04795-112"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="04795-113"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="04795-113"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="04795-114">datetime</span><span class="sxs-lookup"><span data-stu-id="04795-114">datetime</span></span></p></td>
<td><p><span data-ttu-id="04795-115">Primary</span><span class="sxs-lookup"><span data-stu-id="04795-115">Primary</span></span></p></td>
<td><p><span data-ttu-id="04795-116">Ссылка из <a href="lync-server-2013-session-table.md">таблицы Sessions в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="04795-116">Referenced from the <a href="lync-server-2013-session-table.md">Session table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04795-117"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="04795-117"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="04795-118">целое</span><span class="sxs-lookup"><span data-stu-id="04795-118">int</span></span></p></td>
<td><p><span data-ttu-id="04795-119">Primary</span><span class="sxs-lookup"><span data-stu-id="04795-119">Primary</span></span></p></td>
<td><p><span data-ttu-id="04795-120">Ссылка из <a href="lync-server-2013-session-table.md">таблицы Sessions в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="04795-120">Referenced from the <a href="lync-server-2013-session-table.md">Session table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04795-121"><strong>MediaLineLabel</strong></span><span class="sxs-lookup"><span data-stu-id="04795-121"><strong>MediaLineLabel</strong></span></span></p></td>
<td><p><span data-ttu-id="04795-122">tinyint</span><span class="sxs-lookup"><span data-stu-id="04795-122">tinyint</span></span></p></td>
<td><p><span data-ttu-id="04795-123">Primary</span><span class="sxs-lookup"><span data-stu-id="04795-123">Primary</span></span></p></td>
<td><p><span data-ttu-id="04795-124">0 — основной звук, 1 — основной видеофайл, а 2 — панорамный видеоролик, а 3 — общий доступ к приложениям и рабочему столу.</span><span class="sxs-lookup"><span data-stu-id="04795-124">0 is main audio, 1 is main video, and 2 is panoramic video, 3 is Application/Desktop Sharing.</span></span> <span data-ttu-id="04795-125">Эта метка должна быть уникальной в пределах одного сеанса.</span><span class="sxs-lookup"><span data-stu-id="04795-125">This label must be unique within a single session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04795-126"><strong>ConnectivityIce</strong></span><span class="sxs-lookup"><span data-stu-id="04795-126"><strong>ConnectivityIce</strong></span></span></p></td>
<td><p><span data-ttu-id="04795-127">tinyint</span><span class="sxs-lookup"><span data-stu-id="04795-127">tinyint</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="04795-128">Этот столбец присутствует в Microsoft Lync Server 2013, но не используется.</span><span class="sxs-lookup"><span data-stu-id="04795-128">This column is present but not used in Microsoft Lync Server 2013.</span></span> <span data-ttu-id="04795-129">Сведения о подключении, используемом для линии мультимедиа, записываются в столбцах CallerConnectivityICE и CalleeConnectivityICE.</span><span class="sxs-lookup"><span data-stu-id="04795-129">Information about the connectivity used for a media line is captured in the CallerConnectivityICE and CalleeConnectivityICE columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04795-130"><strong>CallerIceWarningFlags</strong></span><span class="sxs-lookup"><span data-stu-id="04795-130"><strong>CallerIceWarningFlags</strong></span></span></p></td>
<td><p><span data-ttu-id="04795-131">целое</span><span class="sxs-lookup"><span data-stu-id="04795-131">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="04795-132">Сведения о процессе установки интерактивной связи (ICE), описанные в разделе Флаги BITS.</span><span class="sxs-lookup"><span data-stu-id="04795-132">Information about Interactive Connectivity Establishment (ICE) process described in bits flags.</span></span> <span data-ttu-id="04795-133">Подробные сведения можно найти в <em>спецификации протоколов сервера контроля качества обслуживания</em>, которую можно загрузить.</span><span class="sxs-lookup"><span data-stu-id="04795-133">For details, refer to the <em>Quality of Experience Monitoring Server Protocol Specification</em>, available for download.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04795-134"><strong>CalleeIceWarningFlags</strong></span><span class="sxs-lookup"><span data-stu-id="04795-134"><strong>CalleeIceWarningFlags</strong></span></span></p></td>
<td><p><span data-ttu-id="04795-135">целое</span><span class="sxs-lookup"><span data-stu-id="04795-135">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="04795-136">То же, что и CallerIceWarningFlags, но на стороне вызываемого абонента.</span><span class="sxs-lookup"><span data-stu-id="04795-136">Same as CallerIceWarningFlags, but on the callee side.</span></span> <span data-ttu-id="04795-137">Подробные сведения можно найти в <em>спецификации протоколов сервера контроля качества обслуживания</em>, которую можно загрузить.</span><span class="sxs-lookup"><span data-stu-id="04795-137">For details, refer to the <em>Quality of Experience Monitoring Server Protocol Specification</em>, available for download.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04795-138"><strong>Безопасность</strong></span><span class="sxs-lookup"><span data-stu-id="04795-138"><strong>Security</strong></span></span></p></td>
<td><p><span data-ttu-id="04795-139">tinyint</span><span class="sxs-lookup"><span data-stu-id="04795-139">tinyint</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="04795-140">Используемый профиль безопасности.</span><span class="sxs-lookup"><span data-stu-id="04795-140">The security profile in use.</span></span> <span data-ttu-id="04795-141">0 — NONE, 1 — SRTP, 2 — v1.</span><span class="sxs-lookup"><span data-stu-id="04795-141">0 is NONE, 1 is SRTP, 2 is V1.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04795-142"><strong>Transport</strong></span><span class="sxs-lookup"><span data-stu-id="04795-142"><strong>Transport</strong></span></span></p></td>
<td><p><span data-ttu-id="04795-143">tinyint</span><span class="sxs-lookup"><span data-stu-id="04795-143">tinyint</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="04795-144">0 — это UDP, а 1 — TCP.</span><span class="sxs-lookup"><span data-stu-id="04795-144">0 is UDP, 1 is TCP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04795-145"><strong>CallerIPAddr</strong></span><span class="sxs-lookup"><span data-stu-id="04795-145"><strong>CallerIPAddr</strong></span></span></p></td>
<td><p><span data-ttu-id="04795-146">целое</span><span class="sxs-lookup"><span data-stu-id="04795-146">int</span></span></p></td>
<td><p><span data-ttu-id="04795-147">Другом</span><span class="sxs-lookup"><span data-stu-id="04795-147">Foreign</span></span></p></td>
<td><p><span data-ttu-id="04795-148">IP-адрес вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="04795-148">IP Address of the caller.</span></span> <span data-ttu-id="04795-149">Дополнительные сведения приведены в <a href="lync-server-2013-ipaddress-table.md">таблице IP-адрес в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="04795-149">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04795-150"><strong>CallerPort</strong></span><span class="sxs-lookup"><span data-stu-id="04795-150"><strong>CallerPort</strong></span></span></p></td>
<td><p><span data-ttu-id="04795-151">целое</span><span class="sxs-lookup"><span data-stu-id="04795-151">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="04795-152">Порт, используемый вызывающим абонентом.</span><span class="sxs-lookup"><span data-stu-id="04795-152">Port used by the caller.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04795-153"><strong>CallerSubnet</strong></span><span class="sxs-lookup"><span data-stu-id="04795-153"><strong>CallerSubnet</strong></span></span></p></td>
<td><p><span data-ttu-id="04795-154">целое</span><span class="sxs-lookup"><span data-stu-id="04795-154">int</span></span></p></td>
<td><p> <span data-ttu-id="04795-155">Другом</span><span class="sxs-lookup"><span data-stu-id="04795-155">Foreign</span></span></p></td>
<td><p><span data-ttu-id="04795-156">Подсеть вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="04795-156">The subnet of the caller.</span></span> <span data-ttu-id="04795-157">Дополнительные сведения приведены в <a href="lync-server-2013-ipaddress-table.md">таблице IP-адрес в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="04795-157">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04795-158"><strong>CallerInside</strong></span><span class="sxs-lookup"><span data-stu-id="04795-158"><strong>CallerInside</strong></span></span></p></td>
<td><p><span data-ttu-id="04795-159">бит</span><span class="sxs-lookup"><span data-stu-id="04795-159">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="04795-160">1 означает, что вызывающий абонент входит в корпоративную сеть, а 0 означает, что вызывающий абонент находится за пределами сети.</span><span class="sxs-lookup"><span data-stu-id="04795-160">1 means caller is inside the enterprise network, 0 means the caller is outside the network.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04795-161"><strong>CallerMacAddress</strong></span><span class="sxs-lookup"><span data-stu-id="04795-161"><strong>CallerMacAddress</strong></span></span></p></td>
<td><p><span data-ttu-id="04795-162">целое</span><span class="sxs-lookup"><span data-stu-id="04795-162">int</span></span></p></td>
<td><p><span data-ttu-id="04795-163">Другом</span><span class="sxs-lookup"><span data-stu-id="04795-163">Foreign</span></span></p></td>
<td><p><span data-ttu-id="04795-164">Mac-адрес вызывающего абонента, на который ссылается <a href="lync-server-2013-macaddress-table.md">Таблица MacAddress в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="04795-164">Caller’s mac address, referenced from <a href="lync-server-2013-macaddress-table.md">MacAddress table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04795-165"><strong>CallerRelayIPAddr</strong></span><span class="sxs-lookup"><span data-stu-id="04795-165"><strong>CallerRelayIPAddr</strong></span></span></p></td>
<td><p><span data-ttu-id="04795-166">целое</span><span class="sxs-lookup"><span data-stu-id="04795-166">int</span></span></p></td>
<td><p><span data-ttu-id="04795-167">Другом</span><span class="sxs-lookup"><span data-stu-id="04795-167">Foreign</span></span></p></td>
<td><p><span data-ttu-id="04795-168">IP-адрес службы Edge сервера Lync/V, используемой вызывающим абонентом.</span><span class="sxs-lookup"><span data-stu-id="04795-168">IP Address of the Lync Server A/V Edge service used by the caller.</span></span> <span data-ttu-id="04795-169">Дополнительные сведения приведены в <a href="lync-server-2013-ipaddress-table.md">таблице IP-адрес в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="04795-169">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04795-170"><strong>CallerRelayPort</strong></span><span class="sxs-lookup"><span data-stu-id="04795-170"><strong>CallerRelayPort</strong></span></span></p></td>
<td><p><span data-ttu-id="04795-171">целое</span><span class="sxs-lookup"><span data-stu-id="04795-171">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="04795-172">Порт, используемый вызывающим абонентом для службы Edge A/V.</span><span class="sxs-lookup"><span data-stu-id="04795-172">Port used on the A/V Edge service by the caller.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04795-173"><strong>CallerCaptureDev</strong></span><span class="sxs-lookup"><span data-stu-id="04795-173"><strong>CallerCaptureDev</strong></span></span></p></td>
<td><p><span data-ttu-id="04795-174">целое</span><span class="sxs-lookup"><span data-stu-id="04795-174">int</span></span></p></td>
<td><p><span data-ttu-id="04795-175">Другом</span><span class="sxs-lookup"><span data-stu-id="04795-175">Foreign</span></span></p></td>
<td><p><span data-ttu-id="04795-176">Устройство захвата, используемое вызывающим абонентом.</span><span class="sxs-lookup"><span data-stu-id="04795-176">Capture device used by the caller.</span></span> <span data-ttu-id="04795-177">Ссылка из <a href="lync-server-2013-device-table.md">таблицы устройств в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="04795-177">Referenced from the <a href="lync-server-2013-device-table.md">Device table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04795-178"><strong>CallerRenderDev</strong></span><span class="sxs-lookup"><span data-stu-id="04795-178"><strong>CallerRenderDev</strong></span></span></p></td>
<td><p><span data-ttu-id="04795-179">целое</span><span class="sxs-lookup"><span data-stu-id="04795-179">int</span></span></p></td>
<td><p><span data-ttu-id="04795-180">Другом</span><span class="sxs-lookup"><span data-stu-id="04795-180">Foreign</span></span></p></td>
<td><p><span data-ttu-id="04795-181">Устройство обработки, используемое вызывающим абонентом.</span><span class="sxs-lookup"><span data-stu-id="04795-181">Render device used by caller.</span></span> <span data-ttu-id="04795-182">Ссылка из <a href="lync-server-2013-device-table.md">таблицы устройств в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="04795-182">Referenced from the <a href="lync-server-2013-device-table.md">Device table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04795-183"><strong>CallerCaptureDevDriver</strong></span><span class="sxs-lookup"><span data-stu-id="04795-183"><strong>CallerCaptureDevDriver</strong></span></span></p></td>
<td><p><span data-ttu-id="04795-184">целое</span><span class="sxs-lookup"><span data-stu-id="04795-184">int</span></span></p></td>
<td><p><span data-ttu-id="04795-185">Другом</span><span class="sxs-lookup"><span data-stu-id="04795-185">Foreign</span></span></p></td>
<td><p><span data-ttu-id="04795-186">Драйвер устройства захвата вызывающего абонента, на который ссылается <a href="lync-server-2013-devicedriver-table.md">Таблица DeviceDriver в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="04795-186">Driver for the caller’s capture device, referenced from the <a href="lync-server-2013-devicedriver-table.md">DeviceDriver table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04795-187"><strong>CallerRenderDevDriver</strong></span><span class="sxs-lookup"><span data-stu-id="04795-187"><strong>CallerRenderDevDriver</strong></span></span></p></td>
<td><p><span data-ttu-id="04795-188">целое</span><span class="sxs-lookup"><span data-stu-id="04795-188">int</span></span></p></td>
<td><p><span data-ttu-id="04795-189">Другом</span><span class="sxs-lookup"><span data-stu-id="04795-189">Foreign</span></span></p></td>
<td><p><span data-ttu-id="04795-190">Драйвер для устройства отрисовки вызывающего абонента, на который ссылается <a href="lync-server-2013-devicedriver-table.md">Таблица DeviceDriver в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="04795-190">Driver for the caller’s render device, referenced from the <a href="lync-server-2013-devicedriver-table.md">DeviceDriver table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04795-191"><strong>CallerNetworkConnectionType</strong></span><span class="sxs-lookup"><span data-stu-id="04795-191"><strong>CallerNetworkConnectionType</strong></span></span></p></td>
<td><p><span data-ttu-id="04795-192">tinyint</span><span class="sxs-lookup"><span data-stu-id="04795-192">tinyint</span></span></p></td>
<td><p><span data-ttu-id="04795-193">Другом</span><span class="sxs-lookup"><span data-stu-id="04795-193">Foreign</span></span></p></td>
<td><p><span data-ttu-id="04795-194">Показывает, как вызывающий абонент подключился к сети.</span><span class="sxs-lookup"><span data-stu-id="04795-194">Indicates how the caller connected to the network.</span></span> <span data-ttu-id="04795-195">Значения извлекаются из <a href="lync-server-2013-networkconnectiondetail-table.md">таблицы NetworkConnectionDetail в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="04795-195">Values are obtained from the <a href="lync-server-2013-networkconnectiondetail-table.md">NetworkConnectionDetail table in Lync Server 2013</a>.</span></span> <span data-ttu-id="04795-196">Типичные значения: 0 для проводного подключения 1 для подключения WiFi; и 3 для подключения Ethernet.</span><span class="sxs-lookup"><span data-stu-id="04795-196">Typical values are 0 for a wired connection’ 1 for a WiFi connection; and 3 for an Ethernet connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04795-197"><strong>CallerBssid</strong></span><span class="sxs-lookup"><span data-stu-id="04795-197"><strong>CallerBssid</strong></span></span></p></td>
<td><p><span data-ttu-id="04795-198">целое</span><span class="sxs-lookup"><span data-stu-id="04795-198">int</span></span></p></td>
<td><p><span data-ttu-id="04795-199">Другом</span><span class="sxs-lookup"><span data-stu-id="04795-199">Foreign</span></span></p></td>
<td><p><span data-ttu-id="04795-200">BSSID для вызывающего абонента, если используется беспроводная связь.</span><span class="sxs-lookup"><span data-stu-id="04795-200">Caller’s BSSID if wireless is used.</span></span> <span data-ttu-id="04795-201">Ссылка из <a href="lync-server-2013-macaddress-table.md">таблицы MacAddress в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="04795-201">Referenced from <a href="lync-server-2013-macaddress-table.md">MacAddress table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04795-202"><strong>CallerVPN</strong></span><span class="sxs-lookup"><span data-stu-id="04795-202"><strong>CallerVPN</strong></span></span></p></td>
<td><p><span data-ttu-id="04795-203">бит</span><span class="sxs-lookup"><span data-stu-id="04795-203">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="04795-204">Ссылка вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="04795-204">The caller's link.</span></span> <span data-ttu-id="04795-205">1 — это виртуальная частная сеть (VPN), а 0 — не VPN.</span><span class="sxs-lookup"><span data-stu-id="04795-205">1 is virtual private network (VPN), 0 is non-VPN.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04795-206"><strong>CallerLinkSpeed</strong></span><span class="sxs-lookup"><span data-stu-id="04795-206"><strong>CallerLinkSpeed</strong></span></span></p></td>
<td><p><span data-ttu-id="04795-207">десятичное число (18; 0)</span><span class="sxs-lookup"><span data-stu-id="04795-207">decimal(18,0)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="04795-208">Скорость сетевого соединения (в бит/с) для конечной точки вызывающего объекта.</span><span class="sxs-lookup"><span data-stu-id="04795-208">The network link speed, in bps, for the caller's endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04795-209"><strong>CalleeIPAddr</strong></span><span class="sxs-lookup"><span data-stu-id="04795-209"><strong>CalleeIPAddr</strong></span></span></p></td>
<td><p><span data-ttu-id="04795-210">целое</span><span class="sxs-lookup"><span data-stu-id="04795-210">int</span></span></p></td>
<td><p><span data-ttu-id="04795-211">Другом</span><span class="sxs-lookup"><span data-stu-id="04795-211">Foreign</span></span></p></td>
<td><p><span data-ttu-id="04795-212">IP-адрес получателя звонка.</span><span class="sxs-lookup"><span data-stu-id="04795-212">IP Address of the call receiver.</span></span> <span data-ttu-id="04795-213">Дополнительные сведения приведены в <a href="lync-server-2013-ipaddress-table.md">таблице IP-адрес в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="04795-213">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04795-214"><strong>CalleePort</strong></span><span class="sxs-lookup"><span data-stu-id="04795-214"><strong>CalleePort</strong></span></span></p></td>
<td><p><span data-ttu-id="04795-215">бит</span><span class="sxs-lookup"><span data-stu-id="04795-215">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="04795-216">Порт, используемый получателем звонка.</span><span class="sxs-lookup"><span data-stu-id="04795-216">Port used by the call receiver.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04795-217"><strong>CalleeSubnet</strong></span><span class="sxs-lookup"><span data-stu-id="04795-217"><strong>CalleeSubnet</strong></span></span></p></td>
<td><p><span data-ttu-id="04795-218">целое</span><span class="sxs-lookup"><span data-stu-id="04795-218">int</span></span></p></td>
<td><p><span data-ttu-id="04795-219">Другом</span><span class="sxs-lookup"><span data-stu-id="04795-219">Foreign</span></span></p></td>
<td><p><span data-ttu-id="04795-220">Подсеть вызываемого абонента.</span><span class="sxs-lookup"><span data-stu-id="04795-220">Subnet of callee.</span></span> <span data-ttu-id="04795-221">Дополнительные сведения приведены в <a href="lync-server-2013-ipaddress-table.md">таблице IP-адрес в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="04795-221">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04795-222"><strong>CalleeInside</strong></span><span class="sxs-lookup"><span data-stu-id="04795-222"><strong>CalleeInside</strong></span></span></p></td>
<td><p><span data-ttu-id="04795-223">бит</span><span class="sxs-lookup"><span data-stu-id="04795-223">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="04795-224">1 — Получатель звонка входит в корпоративную сеть, а 0 означает, что получатель звонка находится за пределами сети.</span><span class="sxs-lookup"><span data-stu-id="04795-224">1 means call receiver is inside the enterprise network, 0 means the call receiver is outside the network.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04795-225"><strong>CalleeMacAddress</strong></span><span class="sxs-lookup"><span data-stu-id="04795-225"><strong>CalleeMacAddress</strong></span></span></p></td>
<td><p><span data-ttu-id="04795-226">целое</span><span class="sxs-lookup"><span data-stu-id="04795-226">int</span></span></p></td>
<td><p><span data-ttu-id="04795-227">Другом</span><span class="sxs-lookup"><span data-stu-id="04795-227">Foreign</span></span></p></td>
<td><p><span data-ttu-id="04795-228">Абонентский Mac-адрес.</span><span class="sxs-lookup"><span data-stu-id="04795-228">Callee Mac address.</span></span> <span data-ttu-id="04795-229">Ссылка на <a href="lync-server-2013-macaddress-table.md">таблицу MacAddress в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="04795-229">Referenced from the <a href="lync-server-2013-macaddress-table.md">MacAddress table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04795-230"><strong>CalleeRelayIPAddr</strong></span><span class="sxs-lookup"><span data-stu-id="04795-230"><strong>CalleeRelayIPAddr</strong></span></span></p></td>
<td><p><span data-ttu-id="04795-231">целое</span><span class="sxs-lookup"><span data-stu-id="04795-231">int</span></span></p></td>
<td><p><span data-ttu-id="04795-232">Другом</span><span class="sxs-lookup"><span data-stu-id="04795-232">Foreign</span></span></p></td>
<td><p><span data-ttu-id="04795-233">IP-адрес службы EDGE (/V), используемой приемником вызова.</span><span class="sxs-lookup"><span data-stu-id="04795-233">IP Address of the A/V Edge service used by the call receiver.</span></span> <span data-ttu-id="04795-234">Дополнительные сведения приведены в <a href="lync-server-2013-ipaddress-table.md">таблице IP-адрес в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="04795-234">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04795-235"><strong>CalleeRelayPort</strong></span><span class="sxs-lookup"><span data-stu-id="04795-235"><strong>CalleeRelayPort</strong></span></span></p></td>
<td><p><span data-ttu-id="04795-236">целое</span><span class="sxs-lookup"><span data-stu-id="04795-236">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="04795-237">Порт, используемый приемником вызова для службы Edge/V.</span><span class="sxs-lookup"><span data-stu-id="04795-237">Port used on the A/V Edge Service by the call receiver.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04795-238"><strong>CalleeCaptureDev</strong></span><span class="sxs-lookup"><span data-stu-id="04795-238"><strong>CalleeCaptureDev</strong></span></span></p></td>
<td><p><span data-ttu-id="04795-239">целое</span><span class="sxs-lookup"><span data-stu-id="04795-239">int</span></span></p></td>
<td><p><span data-ttu-id="04795-240">другом</span><span class="sxs-lookup"><span data-stu-id="04795-240">foreign</span></span></p></td>
<td><p><span data-ttu-id="04795-241">Устройство захвата, используемое получателем звонка.</span><span class="sxs-lookup"><span data-stu-id="04795-241">Capture device used by the call receiver.</span></span> <span data-ttu-id="04795-242">Ссылка из <a href="lync-server-2013-device-table.md">таблицы устройств в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="04795-242">Referenced from the <a href="lync-server-2013-device-table.md">Device table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04795-243"><strong>CalleeRenderDev</strong></span><span class="sxs-lookup"><span data-stu-id="04795-243"><strong>CalleeRenderDev</strong></span></span></p></td>
<td><p><span data-ttu-id="04795-244">целое</span><span class="sxs-lookup"><span data-stu-id="04795-244">int</span></span></p></td>
<td><p><span data-ttu-id="04795-245">Другом</span><span class="sxs-lookup"><span data-stu-id="04795-245">Foreign</span></span></p></td>
<td><p><span data-ttu-id="04795-246">Устройство обработки, используемое получателем звонка.</span><span class="sxs-lookup"><span data-stu-id="04795-246">Render device used by the call receiver.</span></span> <span data-ttu-id="04795-247">Ссылка из <a href="lync-server-2013-device-table.md">таблицы устройств в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="04795-247">Referenced from the <a href="lync-server-2013-device-table.md">Device table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04795-248"><strong>CalleeCaptureDevDriver</strong></span><span class="sxs-lookup"><span data-stu-id="04795-248"><strong>CalleeCaptureDevDriver</strong></span></span></p></td>
<td><p><span data-ttu-id="04795-249">целое</span><span class="sxs-lookup"><span data-stu-id="04795-249">int</span></span></p></td>
<td><p><span data-ttu-id="04795-250">Другом</span><span class="sxs-lookup"><span data-stu-id="04795-250">Foreign</span></span></p></td>
<td><p><span data-ttu-id="04795-251">Драйвер устройства захвата приемника звонков.</span><span class="sxs-lookup"><span data-stu-id="04795-251">Driver for the call receiver’s capture device.</span></span> <span data-ttu-id="04795-252">Ссылка из <a href="lync-server-2013-devicedriver-table.md">таблицы DeviceDriver в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="04795-252">Referenced from <a href="lync-server-2013-devicedriver-table.md">DeviceDriver table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04795-253"><strong>CalleeRenderDevDriver</strong></span><span class="sxs-lookup"><span data-stu-id="04795-253"><strong>CalleeRenderDevDriver</strong></span></span></p></td>
<td><p><span data-ttu-id="04795-254">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="04795-254">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="04795-255">Другом</span><span class="sxs-lookup"><span data-stu-id="04795-255">Foreign</span></span></p></td>
<td><p><span data-ttu-id="04795-256">Драйвер устройства отрисовки приемника звонков.</span><span class="sxs-lookup"><span data-stu-id="04795-256">Driver for the call receiver’s render device.</span></span> <span data-ttu-id="04795-257">Ссылка из <a href="lync-server-2013-devicedriver-table.md">таблицы DeviceDriver в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="04795-257">Referenced from <a href="lync-server-2013-devicedriver-table.md">DeviceDriver table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04795-258"><strong>CalleeNetworkConnectionType</strong></span><span class="sxs-lookup"><span data-stu-id="04795-258"><strong>CalleeNetworkConnectionType</strong></span></span></p></td>
<td><p><span data-ttu-id="04795-259">tinyint</span><span class="sxs-lookup"><span data-stu-id="04795-259">tinyint</span></span></p></td>
<td><p><span data-ttu-id="04795-260">Другом</span><span class="sxs-lookup"><span data-stu-id="04795-260">Foreign</span></span></p></td>
<td><p><span data-ttu-id="04795-261">Показывает, как вызывающий абонент подключился к сети.</span><span class="sxs-lookup"><span data-stu-id="04795-261">Indicates how the callee connected to the network.</span></span> <span data-ttu-id="04795-262">Значения извлекаются из <a href="lync-server-2013-networkconnectiondetail-table.md">таблицы NetworkConnectionDetail в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="04795-262">Values are obtained from the <a href="lync-server-2013-networkconnectiondetail-table.md">NetworkConnectionDetail table in Lync Server 2013</a>.</span></span> <span data-ttu-id="04795-263">Типичные значения: 0 для проводного подключения 1 для подключения WiFi; и 3 для подключения Ethernet.</span><span class="sxs-lookup"><span data-stu-id="04795-263">Typical values are 0 for a wired connection’ 1 for a WiFi connection; and 3 for an Ethernet connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04795-264"><strong>CalleeBssid</strong></span><span class="sxs-lookup"><span data-stu-id="04795-264"><strong>CalleeBssid</strong></span></span></p></td>
<td><p><span data-ttu-id="04795-265">целое</span><span class="sxs-lookup"><span data-stu-id="04795-265">int</span></span></p></td>
<td><p><span data-ttu-id="04795-266">Другом</span><span class="sxs-lookup"><span data-stu-id="04795-266">Foreign</span></span></p></td>
<td><p><span data-ttu-id="04795-267">Если используется беспроводная связь, вызовите BSSID.</span><span class="sxs-lookup"><span data-stu-id="04795-267">Callee’s BSSID if wireless is used.</span></span> <span data-ttu-id="04795-268">Ссылка из <a href="lync-server-2013-macaddress-table.md">таблицы MacAddress в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="04795-268">Referenced from <a href="lync-server-2013-macaddress-table.md">MacAddress table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04795-269"><strong>CalleeVPN</strong></span><span class="sxs-lookup"><span data-stu-id="04795-269"><strong>CalleeVPN</strong></span></span></p></td>
<td><p><span data-ttu-id="04795-270">бит</span><span class="sxs-lookup"><span data-stu-id="04795-270">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="04795-271">Ссылка на приемник звонка; 1 — это виртуальная частная сеть (VPN), а 0 — не VPN.</span><span class="sxs-lookup"><span data-stu-id="04795-271">The call receiver’s link; 1 is virtual private network (VPN), 0 is non-VPN.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04795-272"><strong>CalleeLinkSpeed</strong></span><span class="sxs-lookup"><span data-stu-id="04795-272"><strong>CalleeLinkSpeed</strong></span></span></p></td>
<td><p><span data-ttu-id="04795-273">десятичное число (18; 0)</span><span class="sxs-lookup"><span data-stu-id="04795-273">decimal(18,0)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="04795-274">Скорость сетевого соединения (в бит/с) для конечной точки получателя звонка.</span><span class="sxs-lookup"><span data-stu-id="04795-274">The network link speed, in bps, for the call receiver’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04795-275"><strong>ConversationalMOS</strong></span><span class="sxs-lookup"><span data-stu-id="04795-275"><strong>ConversationalMOS</strong></span></span></p></td>
<td><p><span data-ttu-id="04795-276">десятичное число (3, 2)</span><span class="sxs-lookup"><span data-stu-id="04795-276">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="04795-277">Narrowband MOS из сеансов голосовой связи (на основе обоих звуковых потоков).</span><span class="sxs-lookup"><span data-stu-id="04795-277">Narrowband Conversational MOS of the audio sessions (based on both audio streams).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04795-278"><strong>AppliedBandwidthLimit</strong></span><span class="sxs-lookup"><span data-stu-id="04795-278"><strong>AppliedBandwidthLimit</strong></span></span></p></td>
<td><p><span data-ttu-id="04795-279">целое</span><span class="sxs-lookup"><span data-stu-id="04795-279">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="04795-280">Это фактическая пропускная способность, примененная к данному потоку отправки на стороне, для которой заданы различные параметры политики (повернуть, API, SDP, сервер политики и т. д.).</span><span class="sxs-lookup"><span data-stu-id="04795-280">This is the actual bandwidth applied to the given send side stream given various policy settings (TURN, API, SDP, Policy Server, and so on).</span></span> <span data-ttu-id="04795-281">Это не следует путать с эффективной пропускной способностью, так как в зависимости от оценки пропускной способности может снизиться эффективная пропускная способность.</span><span class="sxs-lookup"><span data-stu-id="04795-281">This is not to be confused with the effective bandwidth because there can be a lower effective bandwidth based on the bandwidth estimate.</span></span> <span data-ttu-id="04795-282">Это является, по сути, максимальной пропускной способностью потока отправки, который может занимать ограничения пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="04795-282">This is basically the maximum bandwidth the send stream can take barring limits imposed by the bandwidth estimate.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04795-283"><strong>AppliedBandwidthSourceKey</strong></span><span class="sxs-lookup"><span data-stu-id="04795-283"><strong>AppliedBandwidthSourceKey</strong></span></span></p></td>
<td><p><span data-ttu-id="04795-284">smallint</span><span class="sxs-lookup"><span data-stu-id="04795-284">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="04795-285">Это источник установленного места для пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="04795-285">This is the source of the bandwidth cap being imposed.</span></span> <span data-ttu-id="04795-286">Она описывает, откуда поступают ограничения пропускной способности ("сервер политики", "превратить сервер", "модальность" и т. д.).</span><span class="sxs-lookup"><span data-stu-id="04795-286">It describes where the bandwidth limit is coming from (“Policy Server”, “TURN Server”, “Modality”, and so on).</span></span> <span data-ttu-id="04795-287">На которую ссылается <a href="lync-server-2013-appliedbandwidthsource-table.md">Таблица AppliedBandwidthSource в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="04795-287">Referenced from the <a href="lync-server-2013-appliedbandwidthsource-table.md">AppliedBandwidthSource table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04795-288"><strong>Вызывающая сторона</strong></span><span class="sxs-lookup"><span data-stu-id="04795-288"><strong>Caller</strong></span></span></p></td>
<td><p><span data-ttu-id="04795-289">бит</span><span class="sxs-lookup"><span data-stu-id="04795-289">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="04795-290">Указывает, получены ли метрики от вызывающего абонента; 1 — это "Да", значение null — "нет".</span><span class="sxs-lookup"><span data-stu-id="04795-290">Indicates whether metrics from the caller were received; 1 is yes, a null value is no.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04795-291"><strong>Вызываемая сторона</strong></span><span class="sxs-lookup"><span data-stu-id="04795-291"><strong>Callee</strong></span></span></p></td>
<td><p><span data-ttu-id="04795-292">бит</span><span class="sxs-lookup"><span data-stu-id="04795-292">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="04795-293">Указывает, получены ли метрики от приемника вызова; 1 — это "Да", значение null — "нет".</span><span class="sxs-lookup"><span data-stu-id="04795-293">Indicates whether metrics from the call receiver were received; 1 is yes, a null value is no.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04795-294"><strong>MidCallReport</strong></span><span class="sxs-lookup"><span data-stu-id="04795-294"><strong>MidCallReport</strong></span></span></p></td>
<td><p><span data-ttu-id="04795-295">бит</span><span class="sxs-lookup"><span data-stu-id="04795-295">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="04795-296">Указывает, является ли отчет частью сеанса или для полного сеанса.</span><span class="sxs-lookup"><span data-stu-id="04795-296">Indicates whether the report is for a portion of the session or for the complete session.</span></span></p>
<p><span data-ttu-id="04795-297">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="04795-297">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04795-298"><strong>ClassifiedPoorCall</strong></span><span class="sxs-lookup"><span data-stu-id="04795-298"><strong>ClassifiedPoorCall</strong></span></span></p></td>
<td><p><span data-ttu-id="04795-299">бит</span><span class="sxs-lookup"><span data-stu-id="04795-299">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="04795-300">Указывает, был ли звонок классифицирован как неудовлетворительный (значение 1) или как хороший звонок (0).</span><span class="sxs-lookup"><span data-stu-id="04795-300">Indicates whether a call was classified as a poor call (value of 1) or as a good call (0).</span></span></p>
<p><span data-ttu-id="04795-301">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="04795-301">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04795-302"><strong>CallerConnectivityICE</strong></span><span class="sxs-lookup"><span data-stu-id="04795-302"><strong>CallerConnectivityICE</strong></span></span></p></td>
<td><p><span data-ttu-id="04795-303">tinyInt</span><span class="sxs-lookup"><span data-stu-id="04795-303">tinyInt</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="04795-304">Указывает, подключен ли вызывающий абонент к сети с помощью протокола ICE (установление подключения к Интернету).</span><span class="sxs-lookup"><span data-stu-id="04795-304">Indicates whether the caller connected to the network using the ICE protocol (Internet Connectivity Establishment).</span></span></p>
<p><span data-ttu-id="04795-305">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="04795-305">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04795-306"><strong>CalleeConnectivityICE</strong></span><span class="sxs-lookup"><span data-stu-id="04795-306"><strong>CalleeConnectivityICE</strong></span></span></p></td>
<td><p><span data-ttu-id="04795-307">tinyint</span><span class="sxs-lookup"><span data-stu-id="04795-307">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="04795-308">Указывает, подключен ли вызывающий абонент к сети с помощью протокола ICE (установление подключения к Интернету).</span><span class="sxs-lookup"><span data-stu-id="04795-308">Indicates whether the caller connected to the network using the ICE protocol (Internet Connectivity Establishment).</span></span></p>
<p><span data-ttu-id="04795-309">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="04795-309">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04795-310"><strong>CallerReflexiveLocalIPAddr</strong></span><span class="sxs-lookup"><span data-stu-id="04795-310"><strong>CallerReflexiveLocalIPAddr</strong></span></span></p></td>
<td><p><span data-ttu-id="04795-311">целое</span><span class="sxs-lookup"><span data-stu-id="04795-311">int</span></span></p></td>
<td><p><span data-ttu-id="04795-312">Другом</span><span class="sxs-lookup"><span data-stu-id="04795-312">Foreign</span></span></p></td>
<td><p><span data-ttu-id="04795-313">IP-адрес пользователя, который поместил звонок.</span><span class="sxs-lookup"><span data-stu-id="04795-313">Reflexive IP address of the user who placed the call.</span></span> <span data-ttu-id="04795-314">В организациях, использующих NAT (преобразование сетевых адресов), можно использовать IP-адрес прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="04795-314">In organizations that use NAT (network address translation), the reflexive IP address is the IP address of the proxy server.</span></span></p>
<p><span data-ttu-id="04795-315">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="04795-315">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04795-316"><strong>CallerWiFiDriverDevicesDesc</strong></span><span class="sxs-lookup"><span data-stu-id="04795-316"><strong>CallerWiFiDriverDevicesDesc</strong></span></span></p></td>
<td><p><span data-ttu-id="04795-317">целое</span><span class="sxs-lookup"><span data-stu-id="04795-317">int</span></span></p></td>
<td><p><span data-ttu-id="04795-318">Другом</span><span class="sxs-lookup"><span data-stu-id="04795-318">Foreign</span></span></p></td>
<td><p><span data-ttu-id="04795-319">Описание устройства для драйвера Wi-Fi, задействованного пользовательским абонентом.</span><span class="sxs-lookup"><span data-stu-id="04795-319">Device description for the WiFi driver employed by the user who placed the call.</span></span></p>
<p><span data-ttu-id="04795-320">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="04795-320">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04795-321"><strong>CallerWiFiDriverVersion</strong></span><span class="sxs-lookup"><span data-stu-id="04795-321"><strong>CallerWiFiDriverVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="04795-322">целое</span><span class="sxs-lookup"><span data-stu-id="04795-322">int</span></span></p></td>
<td><p><span data-ttu-id="04795-323">Другом</span><span class="sxs-lookup"><span data-stu-id="04795-323">Foreign</span></span></p></td>
<td><p><span data-ttu-id="04795-324">Номер версии для драйвера Wi-Fi, используемый пользователем, который присоединил звонок.</span><span class="sxs-lookup"><span data-stu-id="04795-324">Version number for the WiFi driver employed by the user who placed the call.</span></span></p>
<p><span data-ttu-id="04795-325">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="04795-325">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04795-326"><strong>CalleReflexiveLocalIPAddr</strong></span><span class="sxs-lookup"><span data-stu-id="04795-326"><strong>CalleReflexiveLocalIPAddr</strong></span></span></p></td>
<td><p><span data-ttu-id="04795-327">целое</span><span class="sxs-lookup"><span data-stu-id="04795-327">int</span></span></p></td>
<td><p><span data-ttu-id="04795-328">Другом</span><span class="sxs-lookup"><span data-stu-id="04795-328">Foreign</span></span></p></td>
<td><p><span data-ttu-id="04795-329">IP-адрес пользователя, который получил звонок.</span><span class="sxs-lookup"><span data-stu-id="04795-329">Reflexive IP address of the user who received the call.</span></span> <span data-ttu-id="04795-330">В организациях, использующих NAT (преобразование сетевых адресов), можно использовать IP-адрес прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="04795-330">In organizations that use NAT (network address translation), the reflexive IP address is the IP address of the proxy server.</span></span></p>
<p><span data-ttu-id="04795-331">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="04795-331">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04795-332"><strong>CalleeWiFiDriverDevicesDesc</strong></span><span class="sxs-lookup"><span data-stu-id="04795-332"><strong>CalleeWiFiDriverDevicesDesc</strong></span></span></p></td>
<td><p><span data-ttu-id="04795-333">целое</span><span class="sxs-lookup"><span data-stu-id="04795-333">int</span></span></p></td>
<td><p><span data-ttu-id="04795-334">Другом</span><span class="sxs-lookup"><span data-stu-id="04795-334">Foreign</span></span></p></td>
<td><p><span data-ttu-id="04795-335">Описание устройства для драйвера Wi-Fi, применяемого пользователем, который получил звонок.</span><span class="sxs-lookup"><span data-stu-id="04795-335">Device description for the WiFi driver employed by the user who received the call.</span></span></p>
<p><span data-ttu-id="04795-336">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="04795-336">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04795-337"><strong>CalleeWiFiDriverVersion</strong></span><span class="sxs-lookup"><span data-stu-id="04795-337"><strong>CalleeWiFiDriverVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="04795-338">целое</span><span class="sxs-lookup"><span data-stu-id="04795-338">int</span></span></p></td>
<td><p><span data-ttu-id="04795-339">Другом</span><span class="sxs-lookup"><span data-stu-id="04795-339">Foreign</span></span></p></td>
<td><p><span data-ttu-id="04795-340">Номер версии для драйвера Wi-Fi, используемый пользователем, который получил звонок.</span><span class="sxs-lookup"><span data-stu-id="04795-340">Version number for the WiFi driver employed by the user who received the call.</span></span></p>
<p><span data-ttu-id="04795-341">Этот столбец появился в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="04795-341">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="04795-342">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="04795-342">


</div>

<span> </span>

</div>

</div>

</span></span></div>

