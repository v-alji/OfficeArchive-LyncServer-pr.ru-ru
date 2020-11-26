---
title: 'Lync Server 2013: представление AudioStreamDetail'
description: 'Lync Server 2013: AudioStreamDetail View.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: AudioStreamDetail view
ms:assetid: b6a435b3-103c-41c4-96ed-33c3784534c0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721859(v=OCS.15)
ms:contentKeyID: 49733792
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 92c4c9bbb4f126e242e28d835222f6ba2af89d8b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438164"
---
# <a name="audiostreamdetail-view-in-lync-server-2013"></a><span data-ttu-id="55085-103">AudioStreamDetail представления в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="55085-103">AudioStreamDetail view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="55085-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="55085-104">

<span> </span></span></span>

<span data-ttu-id="55085-105">_**Тема последнего изменения:** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="55085-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="55085-106">В представлении AudioStreamDetail хранятся сведения о каждом звуковом потоке в базе данных.</span><span class="sxs-lookup"><span data-stu-id="55085-106">The AudioStreamDetail View stores information about each audio stream in the database.</span></span> <span data-ttu-id="55085-107">Это представление было представлено в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="55085-107">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="55085-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="55085-108">Column</span></span></th>
<th><span data-ttu-id="55085-109">Тип данных</span><span class="sxs-lookup"><span data-stu-id="55085-109">Data Type</span></span></th>
<th><span data-ttu-id="55085-110">Подробности</span><span class="sxs-lookup"><span data-stu-id="55085-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="55085-111">SessionTime</span><span class="sxs-lookup"><span data-stu-id="55085-111">SessionTime</span></span></p></td>
<td><p><span data-ttu-id="55085-112">datetime</span><span class="sxs-lookup"><span data-stu-id="55085-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="55085-113">На которую ссылается <a href="lync-server-2013-medialine-table.md">Таблица MediaLine в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="55085-113">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-114">SessionSeq</span><span class="sxs-lookup"><span data-stu-id="55085-114">SessionSeq</span></span></p></td>
<td><p><span data-ttu-id="55085-115">целое</span><span class="sxs-lookup"><span data-stu-id="55085-115">int</span></span></p></td>
<td><p><span data-ttu-id="55085-116">На которую ссылается <a href="lync-server-2013-medialine-table.md">Таблица MediaLine в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="55085-116">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-117">StreamId</span><span class="sxs-lookup"><span data-stu-id="55085-117">StreamId</span></span></p></td>
<td><p><span data-ttu-id="55085-118">целое</span><span class="sxs-lookup"><span data-stu-id="55085-118">int</span></span></p></td>
<td><p><span data-ttu-id="55085-119">Уникальный идентификатор в строке мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="55085-119">Unique ID within a media line.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-120">StartTime</span><span class="sxs-lookup"><span data-stu-id="55085-120">StartTime</span></span></p></td>
<td><p><span data-ttu-id="55085-121">datetime</span><span class="sxs-lookup"><span data-stu-id="55085-121">datetime</span></span></p></td>
<td><p><span data-ttu-id="55085-122">Время начала сеанса.</span><span class="sxs-lookup"><span data-stu-id="55085-122">Start time of the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-123">EndTime</span><span class="sxs-lookup"><span data-stu-id="55085-123">EndTime</span></span></p></td>
<td><p><span data-ttu-id="55085-124">datetime</span><span class="sxs-lookup"><span data-stu-id="55085-124">datetime</span></span></p></td>
<td><p><span data-ttu-id="55085-125">Время окончания сеанса.</span><span class="sxs-lookup"><span data-stu-id="55085-125">End time of the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-126">DialogCategory</span><span class="sxs-lookup"><span data-stu-id="55085-126">DialogCategory</span></span></p></td>
<td><p><span data-ttu-id="55085-127">бит</span><span class="sxs-lookup"><span data-stu-id="55085-127">bit</span></span></p></td>
<td><p><span data-ttu-id="55085-128">Категория диалоговых окон: 0 — сервер Lync Server — серверное средство для устранения проблем; 1 — это сервер, на котором выдается посредник для шлюза PSTN.</span><span class="sxs-lookup"><span data-stu-id="55085-128">Dialog category: 0 is the Lync Server to Mediation Server leg; 1 is the Mediation Server to PSTN gateway leg.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-129">MediationServerBypassFlag</span><span class="sxs-lookup"><span data-stu-id="55085-129">MediationServerBypassFlag</span></span></p></td>
<td><p><span data-ttu-id="55085-130">бит</span><span class="sxs-lookup"><span data-stu-id="55085-130">bit</span></span></p></td>
<td><p><span data-ttu-id="55085-131">Флаг, указывающий, обходит ли звонок.</span><span class="sxs-lookup"><span data-stu-id="55085-131">Flag indicating if the call was bypassed or not.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-132">MediaBypassWarningFlag</span><span class="sxs-lookup"><span data-stu-id="55085-132">MediaBypassWarningFlag</span></span></p></td>
<td><p><span data-ttu-id="55085-133">целое</span><span class="sxs-lookup"><span data-stu-id="55085-133">int</span></span></p></td>
<td><p><span data-ttu-id="55085-134">Если указано, указывает, почему звонок не обходится, даже если идентификаторы обхода не совпадают.</span><span class="sxs-lookup"><span data-stu-id="55085-134">If present, indicates why a call was not bypassed even if the bypass IDs matched.</span></span> <span data-ttu-id="55085-135">Определено только одно значение:</span><span class="sxs-lookup"><span data-stu-id="55085-135">Only one value is defined:</span></span></p>
<p><span data-ttu-id="55085-136">0x0001 — Неизвестный идентификатор обхода для сетевого адаптера по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="55085-136">0x0001 – Unknown bypass ID for Default network adapter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-137">CallPriority</span><span class="sxs-lookup"><span data-stu-id="55085-137">CallPriority</span></span></p></td>
<td><p><span data-ttu-id="55085-138">целое</span><span class="sxs-lookup"><span data-stu-id="55085-138">int</span></span></p></td>
<td><p><span data-ttu-id="55085-139">Приоритет звонка.</span><span class="sxs-lookup"><span data-stu-id="55085-139">Priority of the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-140">CallerPool</span><span class="sxs-lookup"><span data-stu-id="55085-140">CallerPool</span></span></p></td>
<td><p><span data-ttu-id="55085-141">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="55085-141">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="55085-142">Полное доменное имя пула вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="55085-142">Caller pool FQDN.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-143">CalleePool</span><span class="sxs-lookup"><span data-stu-id="55085-143">CalleePool</span></span></p></td>
<td><p><span data-ttu-id="55085-144">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="55085-144">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="55085-145">Полное доменное имя пула вызываемых абонентов.</span><span class="sxs-lookup"><span data-stu-id="55085-145">Callee pool FQDN.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-146">Вызывающая сторона</span><span class="sxs-lookup"><span data-stu-id="55085-146">Caller</span></span></p></td>
<td><p><span data-ttu-id="55085-147">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="55085-147">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="55085-148">URI вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="55085-148">Caller’s URI.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-149">Вызываемая сторона</span><span class="sxs-lookup"><span data-stu-id="55085-149">Callee</span></span></p></td>
<td><p><span data-ttu-id="55085-150">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="55085-150">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="55085-151">Универсальный код ресурса (URI) вызываемого абонента.</span><span class="sxs-lookup"><span data-stu-id="55085-151">Callee’s URI.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-152">CallerUserAgent</span><span class="sxs-lookup"><span data-stu-id="55085-152">CallerUserAgent</span></span></p></td>
<td><p><span data-ttu-id="55085-153">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="55085-153">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="55085-154">Строка агента пользователя вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="55085-154">Caller’s user agent string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-155">CallerUserAgentType</span><span class="sxs-lookup"><span data-stu-id="55085-155">CallerUserAgentType</span></span></p></td>
<td><p><span data-ttu-id="55085-156">smallint</span><span class="sxs-lookup"><span data-stu-id="55085-156">smallint</span></span></p></td>
<td><p><span data-ttu-id="55085-157">Тип агента пользователя вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="55085-157">Type of the caller’s user agent.</span></span> <span data-ttu-id="55085-158">Дополнительные сведения: <a href="lync-server-2013-useragent-table.md">Таблица UserAgent в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="55085-158">See the <a href="lync-server-2013-useragent-table.md">UserAgent table in Lync Server 2013</a> for details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-159">CallerUserAgentCategory</span><span class="sxs-lookup"><span data-stu-id="55085-159">CallerUserAgentCategory</span></span></p></td>
<td><p><span data-ttu-id="55085-160">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="55085-160">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="55085-161">Категория агента пользователя вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="55085-161">Category of the caller’s user agent.</span></span> <span data-ttu-id="55085-162">Дополнительные сведения <a href="lync-server-2013-useragentdef-table-qoe.md">UserAgentDef в таблице "QoE" в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="55085-162">See the <a href="lync-server-2013-useragentdef-table-qoe.md">UserAgentDef table (QoE) in Lync Server 2013</a> for details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-163">CalleeUserAgent</span><span class="sxs-lookup"><span data-stu-id="55085-163">CalleeUserAgent</span></span></p></td>
<td><p><span data-ttu-id="55085-164">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="55085-164">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="55085-165">Строка агента пользователя вызываемого абонента.</span><span class="sxs-lookup"><span data-stu-id="55085-165">Callee’s user agent string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-166">CalleeUserAgentType</span><span class="sxs-lookup"><span data-stu-id="55085-166">CalleeUserAgentType</span></span></p></td>
<td><p><span data-ttu-id="55085-167">smallint</span><span class="sxs-lookup"><span data-stu-id="55085-167">smallint</span></span></p></td>
<td><p><span data-ttu-id="55085-168">Тип агента пользователя, вызываемого абонентом.</span><span class="sxs-lookup"><span data-stu-id="55085-168">Type of callee’s user agent.</span></span> <span data-ttu-id="55085-169">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-useragent-table.md">таблицей UserAgent в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="55085-169">See the <a href="lync-server-2013-useragent-table.md">UserAgent table in Lync Server 2013</a> for information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-170">CalleeUserAgentCategory</span><span class="sxs-lookup"><span data-stu-id="55085-170">CalleeUserAgentCategory</span></span></p></td>
<td><p><span data-ttu-id="55085-171">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="55085-171">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="55085-172">Категория агента пользователя вызываемого абонента.</span><span class="sxs-lookup"><span data-stu-id="55085-172">Category of callee’s user agent.</span></span> <span data-ttu-id="55085-173">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-useragentdef-table-qoe.md">таблицей UserAgentDef (QoE) в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="55085-173">See the <a href="lync-server-2013-useragentdef-table-qoe.md">UserAgentDef table (QoE) in Lync Server 2013</a> for information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-174">CallerEndpoint</span><span class="sxs-lookup"><span data-stu-id="55085-174">CallerEndpoint</span></span></p></td>
<td><p><span data-ttu-id="55085-175">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="55085-175">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="55085-176">Имя конечной точки вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="55085-176">Caller’s endpoint name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-177">CalleeEndpoint</span><span class="sxs-lookup"><span data-stu-id="55085-177">CalleeEndpoint</span></span></p></td>
<td><p><span data-ttu-id="55085-178">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="55085-178">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="55085-179">Имя конечной точки вызываемого абонента.</span><span class="sxs-lookup"><span data-stu-id="55085-179">Callee’s endpoint name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-180">CallerOS</span><span class="sxs-lookup"><span data-stu-id="55085-180">CallerOS</span></span></p></td>
<td><p><span data-ttu-id="55085-181">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="55085-181">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="55085-182">Операционная система (ОС) конечной точки вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="55085-182">Operating system (OS) of the caller’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-183">CalleeOS</span><span class="sxs-lookup"><span data-stu-id="55085-183">CalleeOS</span></span></p></td>
<td><p><span data-ttu-id="55085-184">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="55085-184">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="55085-185">Операционная система (ОС) конечной точки вызываемого абонента.</span><span class="sxs-lookup"><span data-stu-id="55085-185">Operating system (OS) of the callee’s endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-186">CallerCPUName</span><span class="sxs-lookup"><span data-stu-id="55085-186">CallerCPUName</span></span></p></td>
<td><p><span data-ttu-id="55085-187">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="55085-187">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="55085-188">Имя ЦП конечной точки вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="55085-188">CPU name of the caller’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-189">CalleeCPUName</span><span class="sxs-lookup"><span data-stu-id="55085-189">CalleeCPUName</span></span></p></td>
<td><p><span data-ttu-id="55085-190">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="55085-190">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="55085-191">Имя ЦП конечной точки вызываемого абонента.</span><span class="sxs-lookup"><span data-stu-id="55085-191">CPU name of the callee’s endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-192">CallerCPUNumberOfCores</span><span class="sxs-lookup"><span data-stu-id="55085-192">CallerCPUNumberOfCores</span></span></p></td>
<td><p><span data-ttu-id="55085-193">smallint</span><span class="sxs-lookup"><span data-stu-id="55085-193">smallint</span></span></p></td>
<td><p><span data-ttu-id="55085-194">Количество ядер ЦП в конечной точке вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="55085-194">Number of CPU cores in the caller’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-195">CalleeCPUNumberOfCores</span><span class="sxs-lookup"><span data-stu-id="55085-195">CalleeCPUNumberOfCores</span></span></p></td>
<td><p><span data-ttu-id="55085-196">smallint</span><span class="sxs-lookup"><span data-stu-id="55085-196">smallint</span></span></p></td>
<td><p><span data-ttu-id="55085-197">Количество ядер ЦП в конечной точке вызываемого абонента.</span><span class="sxs-lookup"><span data-stu-id="55085-197">Number of CPU cores in the callee’s endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-198">CallerCPUProcessorSpeed</span><span class="sxs-lookup"><span data-stu-id="55085-198">CallerCPUProcessorSpeed</span></span></p></td>
<td><p><span data-ttu-id="55085-199">целое</span><span class="sxs-lookup"><span data-stu-id="55085-199">int</span></span></p></td>
<td><p><span data-ttu-id="55085-200">Частота процессора конечной точки вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="55085-200">CPU processor speed of the caller’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-201">CalleeCPUProcessorSpeed</span><span class="sxs-lookup"><span data-stu-id="55085-201">CalleeCPUProcessorSpeed</span></span></p></td>
<td><p><span data-ttu-id="55085-202">целое</span><span class="sxs-lookup"><span data-stu-id="55085-202">int</span></span></p></td>
<td><p><span data-ttu-id="55085-203">Тактовая частота процессора на конечной точке вызываемого абонента.</span><span class="sxs-lookup"><span data-stu-id="55085-203">CPU processor speed of the callee’s endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-204">CallerVirtualizationFlag</span><span class="sxs-lookup"><span data-stu-id="55085-204">CallerVirtualizationFlag</span></span></p></td>
<td><p><span data-ttu-id="55085-205">tinyint</span><span class="sxs-lookup"><span data-stu-id="55085-205">tinyint</span></span></p></td>
<td><p><span data-ttu-id="55085-206">Указывает, работает ли система вызывающего абонента в виртуализованной среде.</span><span class="sxs-lookup"><span data-stu-id="55085-206">Indicates whether the caller’s system is running in a virtualized environment.</span></span> <span data-ttu-id="55085-207">Дополнительные сведения приведены <a href="lync-server-2013-endpoint-table.md">в таблице конечная точка в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="55085-207">See the <a href="lync-server-2013-endpoint-table.md">Endpoint table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-208">CalleeVirtualizationFlag</span><span class="sxs-lookup"><span data-stu-id="55085-208">CalleeVirtualizationFlag</span></span></p></td>
<td><p><span data-ttu-id="55085-209">tinyint</span><span class="sxs-lookup"><span data-stu-id="55085-209">tinyint</span></span></p></td>
<td><p><span data-ttu-id="55085-210">Указывает, работает ли система вызываемого абонента в виртуализованной среде.</span><span class="sxs-lookup"><span data-stu-id="55085-210">Indicates whether the callee’s system is running in a virtualized environment.</span></span> <span data-ttu-id="55085-211">Дополнительные сведения приведены <a href="lync-server-2013-endpoint-table.md">в таблице конечная точка в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="55085-211">See the <a href="lync-server-2013-endpoint-table.md">Endpoint table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-212">CorrelationKey</span><span class="sxs-lookup"><span data-stu-id="55085-212">CorrelationKey</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="55085-213">Ключ корреляции.</span><span class="sxs-lookup"><span data-stu-id="55085-213">Correlation key.</span></span> <span data-ttu-id="55085-214">На которую ссылается <a href="lync-server-2013-sessioncorrelation-table.md">Таблица SessionCorrelation в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="55085-214">Referenced from the <a href="lync-server-2013-sessioncorrelation-table.md">SessionCorrelation table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-215">ConnectivityIce</span><span class="sxs-lookup"><span data-stu-id="55085-215">ConnectivityIce</span></span></p></td>
<td><p><span data-ttu-id="55085-216">tinyint</span><span class="sxs-lookup"><span data-stu-id="55085-216">tinyint</span></span></p></td>
<td><p><span data-ttu-id="55085-217">Информация о пути к носителю, например прямая или ретранслируемая.</span><span class="sxs-lookup"><span data-stu-id="55085-217">Information about the media path, such as direct or relayed.</span></span> <span data-ttu-id="55085-218">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-medialine-table.md">таблицей MediaLine в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="55085-218">See the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-219">CallerIceWarningFlags</span><span class="sxs-lookup"><span data-stu-id="55085-219">CallerIceWarningFlags</span></span></p></td>
<td><p><span data-ttu-id="55085-220">целое</span><span class="sxs-lookup"><span data-stu-id="55085-220">int</span></span></p></td>
<td><p><span data-ttu-id="55085-221">Сведения о процессе интерактивной установки подключения (ICE), описанные в разделе Флаги BITS для вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="55085-221">Information about Interactive Connectivity Establishment (ICE) process described in bits flags for the caller.</span></span> <span data-ttu-id="55085-222">Подробности можно найти в спецификации серверного протокола контроля качества обслуживания.</span><span class="sxs-lookup"><span data-stu-id="55085-222">For details, refer to the Quality of Experience Monitoring Server Protocol Specification.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-223">CalleeIceWarningFlags</span><span class="sxs-lookup"><span data-stu-id="55085-223">CalleeIceWarningFlags</span></span></p></td>
<td><p><span data-ttu-id="55085-224">целое</span><span class="sxs-lookup"><span data-stu-id="55085-224">int</span></span></p></td>
<td><p><span data-ttu-id="55085-225">Сведения о процессе установки интерактивной связи (ICE), описанные в флагах BITS для вызываемого абонента.</span><span class="sxs-lookup"><span data-stu-id="55085-225">Information about Interactive Connectivity Establishment (ICE) process described in bits flags for the callee.</span></span> <span data-ttu-id="55085-226">Подробности можно найти в спецификации серверного протокола контроля качества обслуживания.</span><span class="sxs-lookup"><span data-stu-id="55085-226">For details, refer to the Quality of Experience Monitoring Server Protocol Specification.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-227">Transport</span><span class="sxs-lookup"><span data-stu-id="55085-227">Transport</span></span></p></td>
<td><p><span data-ttu-id="55085-228">tinyint</span><span class="sxs-lookup"><span data-stu-id="55085-228">tinyint</span></span></p></td>
<td><p><span data-ttu-id="55085-229">Тип транспорта: 0 — UDP, 1 — TCP.</span><span class="sxs-lookup"><span data-stu-id="55085-229">Transport type: 0 is UDP, 1 is TCP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-230">CallerIPAddr</span><span class="sxs-lookup"><span data-stu-id="55085-230">CallerIPAddr</span></span></p></td>
<td><p><span data-ttu-id="55085-231">var (50)</span><span class="sxs-lookup"><span data-stu-id="55085-231">var(50)</span></span></p></td>
<td><p><span data-ttu-id="55085-232">IP-адрес вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="55085-232">IP address of the caller.</span></span> <span data-ttu-id="55085-233">Это может быть либо IPv4, либо IPv6-адрес.</span><span class="sxs-lookup"><span data-stu-id="55085-233">This may be either an IPv4 or an IPv6 address.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-234">CallerPort</span><span class="sxs-lookup"><span data-stu-id="55085-234">CallerPort</span></span></p></td>
<td><p><span data-ttu-id="55085-235">целое</span><span class="sxs-lookup"><span data-stu-id="55085-235">int</span></span></p></td>
<td><p><span data-ttu-id="55085-236">Порт, используемый вызывающим абонентом.</span><span class="sxs-lookup"><span data-stu-id="55085-236">Port used by the caller.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-237">CallerInside</span><span class="sxs-lookup"><span data-stu-id="55085-237">CallerInside</span></span></p></td>
<td><p><span data-ttu-id="55085-238">бит</span><span class="sxs-lookup"><span data-stu-id="55085-238">bit</span></span></p></td>
<td><p><span data-ttu-id="55085-239">Указывает, находится ли вызывающий объект в сети Interval: 1 означает, что вызывающий абонент входит в корпоративную сеть, а 0 означает, что вызывающий абонент находится за пределами сети.</span><span class="sxs-lookup"><span data-stu-id="55085-239">Indicates whether the caller is inside the interval network: 1 means caller is inside the enterprise network, 0 means the caller is outside the network.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-240">CalleeIPAddr</span><span class="sxs-lookup"><span data-stu-id="55085-240">CalleeIPAddr</span></span></p></td>
<td><p><span data-ttu-id="55085-241">var (50)</span><span class="sxs-lookup"><span data-stu-id="55085-241">var(50)</span></span></p></td>
<td><p><span data-ttu-id="55085-242">IP-адрес вызываемого абонента.</span><span class="sxs-lookup"><span data-stu-id="55085-242">IP address of the callee.</span></span> <span data-ttu-id="55085-243">Это может быть либо IPv4, либо IPv6-адрес.</span><span class="sxs-lookup"><span data-stu-id="55085-243">This may be either an IPv4 or an IPv6 address.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-244">CalleePort</span><span class="sxs-lookup"><span data-stu-id="55085-244">CalleePort</span></span></p></td>
<td><p><span data-ttu-id="55085-245">целое</span><span class="sxs-lookup"><span data-stu-id="55085-245">int</span></span></p></td>
<td><p><span data-ttu-id="55085-246">Порт, используемый вызываемым абонентом.</span><span class="sxs-lookup"><span data-stu-id="55085-246">Port used by the callee.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-247">CalleeInside</span><span class="sxs-lookup"><span data-stu-id="55085-247">CalleeInside</span></span></p></td>
<td><p><span data-ttu-id="55085-248">бит</span><span class="sxs-lookup"><span data-stu-id="55085-248">bit</span></span></p></td>
<td><p><span data-ttu-id="55085-249">Указывает, находится ли вызывающий объект в сети Interval: 1 означает, что вызываемый абонент входит в корпоративную сеть, а 0 означает, что вызываемый объект находится за пределами сети.</span><span class="sxs-lookup"><span data-stu-id="55085-249">Indicates whether the callee is inside the interval network: 1 means callee is inside the enterprise network, 0 means the callee is outside the network.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-250">CallerUserSite</span><span class="sxs-lookup"><span data-stu-id="55085-250">CallerUserSite</span></span></p></td>
<td><p><span data-ttu-id="55085-251">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="55085-251">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="55085-252">Имя сайта вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="55085-252">Name of the caller’s site.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-253">CallerRegion</span><span class="sxs-lookup"><span data-stu-id="55085-253">CallerRegion</span></span></p></td>
<td><p><span data-ttu-id="55085-254">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="55085-254">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="55085-255">Название страны или региона сайта вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="55085-255">Name of the country/region of the caller’s site.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-256">CalleeUserSite</span><span class="sxs-lookup"><span data-stu-id="55085-256">CalleeUserSite</span></span></p></td>
<td><p><span data-ttu-id="55085-257">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="55085-257">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="55085-258">Имя сайта вызываемого абонента.</span><span class="sxs-lookup"><span data-stu-id="55085-258">Name of the callee’s site.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-259">CalleeRegion</span><span class="sxs-lookup"><span data-stu-id="55085-259">CalleeRegion</span></span></p></td>
<td><p><span data-ttu-id="55085-260">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="55085-260">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="55085-261">Название страны или региона сайта вызываемого абонента.</span><span class="sxs-lookup"><span data-stu-id="55085-261">Name of the country/region of the callee’s site.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-262">CallerRelayIPAddr</span><span class="sxs-lookup"><span data-stu-id="55085-262">CallerRelayIPAddr</span></span></p></td>
<td><p><span data-ttu-id="55085-263">var (50)</span><span class="sxs-lookup"><span data-stu-id="55085-263">var(50)</span></span></p></td>
<td><p><span data-ttu-id="55085-264">IP-адрес службы EDGE (/V), используемой вызывающим абонентом.</span><span class="sxs-lookup"><span data-stu-id="55085-264">IP Address of the A/V Edge service used by the caller.</span></span> <span data-ttu-id="55085-265">Дополнительные сведения приведены в <a href="lync-server-2013-ipaddress-table.md">таблице IP-адрес в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="55085-265">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-266">CallerRelayPort</span><span class="sxs-lookup"><span data-stu-id="55085-266">CallerRelayPort</span></span></p></td>
<td><p><span data-ttu-id="55085-267">целое</span><span class="sxs-lookup"><span data-stu-id="55085-267">int</span></span></p></td>
<td><p><span data-ttu-id="55085-268">Порт, используемый в службе EDGE (A/V), используемой вызывающим абонентом.</span><span class="sxs-lookup"><span data-stu-id="55085-268">Port used on the A/V Edge service used by the caller.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-269">CalleeRelayIPAddr</span><span class="sxs-lookup"><span data-stu-id="55085-269">CalleeRelayIPAddr</span></span></p></td>
<td><p><span data-ttu-id="55085-270">var (50)</span><span class="sxs-lookup"><span data-stu-id="55085-270">var(50)</span></span></p></td>
<td><p><span data-ttu-id="55085-271">Ключ IP-адреса для службы EDGE (/V), используемой вызываемым абонентом.</span><span class="sxs-lookup"><span data-stu-id="55085-271">IP Address key of the A/V Edge service used by the callee.</span></span> <span data-ttu-id="55085-272">Дополнительные сведения приведены в <a href="lync-server-2013-ipaddress-table.md">таблице IP-адрес в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="55085-272">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-273">CalleeRelayPort</span><span class="sxs-lookup"><span data-stu-id="55085-273">CalleeRelayPort</span></span></p></td>
<td><p><span data-ttu-id="55085-274">целое</span><span class="sxs-lookup"><span data-stu-id="55085-274">int</span></span></p></td>
<td><p><span data-ttu-id="55085-275">Порт, используемый в службе EDGE (A/V), используемой вызываемым абонентом.</span><span class="sxs-lookup"><span data-stu-id="55085-275">Port used on the A/V Edge service used by the callee.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-276">CallerCaptureDev</span><span class="sxs-lookup"><span data-stu-id="55085-276">CallerCaptureDev</span></span></p></td>
<td><p><span data-ttu-id="55085-277">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="55085-277">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="55085-278">Имя устройства захвата вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="55085-278">Caller’s capture device name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-279">CallerRenderDev</span><span class="sxs-lookup"><span data-stu-id="55085-279">CallerRenderDev</span></span></p></td>
<td><p><span data-ttu-id="55085-280">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="55085-280">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="55085-281">Имя устройства отрисовки вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="55085-281">Caller’s render device name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-282">CallerCaptureDevDriver</span><span class="sxs-lookup"><span data-stu-id="55085-282">CallerCaptureDevDriver</span></span></p></td>
<td><p><span data-ttu-id="55085-283">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="55085-283">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="55085-284">Имя драйвера устройства захвата вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="55085-284">Caller’s capture device driver name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-285">CallerRenderDriver</span><span class="sxs-lookup"><span data-stu-id="55085-285">CallerRenderDriver</span></span></p></td>
<td><p><span data-ttu-id="55085-286">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="55085-286">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="55085-287">Имя драйвера устройства отрисовки вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="55085-287">Caller’s render device driver name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-288">CalleeCaptureDev</span><span class="sxs-lookup"><span data-stu-id="55085-288">CalleeCaptureDev</span></span></p></td>
<td><p><span data-ttu-id="55085-289">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="55085-289">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="55085-290">Имя устройства захвата абонента.</span><span class="sxs-lookup"><span data-stu-id="55085-290">Callee’s capture device name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-291">CalleeRenderDev</span><span class="sxs-lookup"><span data-stu-id="55085-291">CalleeRenderDev</span></span></p></td>
<td><p><span data-ttu-id="55085-292">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="55085-292">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="55085-293">Имя устройства отрисовки вызываемого абонента.</span><span class="sxs-lookup"><span data-stu-id="55085-293">Callee’s render device name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-294">CalleeCaptureDevDriver</span><span class="sxs-lookup"><span data-stu-id="55085-294">CalleeCaptureDevDriver</span></span></p></td>
<td><p><span data-ttu-id="55085-295">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="55085-295">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="55085-296">Имя драйвера устройства захвата абонента.</span><span class="sxs-lookup"><span data-stu-id="55085-296">Callee’s capture device driver name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-297">CalleeRenderDevDriver</span><span class="sxs-lookup"><span data-stu-id="55085-297">CalleeRenderDevDriver</span></span></p></td>
<td><p><span data-ttu-id="55085-298">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="55085-298">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="55085-299">Имя драйвера устройства обработки вызываемого абонента.</span><span class="sxs-lookup"><span data-stu-id="55085-299">Callee’s render device driver name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-300">CallerNetworkConnectionType</span><span class="sxs-lookup"><span data-stu-id="55085-300">CallerNetworkConnectionType</span></span></p></td>
<td><p><span data-ttu-id="55085-301">tinyint</span><span class="sxs-lookup"><span data-stu-id="55085-301">tinyint</span></span></p></td>
<td><p><span data-ttu-id="55085-302">Тип сетевого подключения вызывающего абонента: 0 проводное соединение, 1 — Беспроводная связь.</span><span class="sxs-lookup"><span data-stu-id="55085-302">Caller’s network connection type: 0 is wired, 1 is wireless.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-303">CallerVPN</span><span class="sxs-lookup"><span data-stu-id="55085-303">CallerVPN</span></span></p></td>
<td><p><span data-ttu-id="55085-304">бит</span><span class="sxs-lookup"><span data-stu-id="55085-304">bit</span></span></p></td>
<td><p><span data-ttu-id="55085-305">Указывает, подключен ли вызывающий абонент к виртуальной частной сети: 1 — виртуальная частная сеть (VPN), 0 — не VPN.</span><span class="sxs-lookup"><span data-stu-id="55085-305">Indicates whether the caller connected over a virtual private network: 1 is virtual private network (VPN), 0 is non-VPN.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-306">CallerLinkSpeed</span><span class="sxs-lookup"><span data-stu-id="55085-306">CallerLinkSpeed</span></span></p></td>
<td><p><span data-ttu-id="55085-307">десятичное число (18; 0)</span><span class="sxs-lookup"><span data-stu-id="55085-307">decimal(18,0)</span></span></p></td>
<td><p><span data-ttu-id="55085-308">Скорость сетевого соединения для конечной точки вызывающего абонента бит/с.</span><span class="sxs-lookup"><span data-stu-id="55085-308">Network link speed for the caller's endpoint in bps.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-309">CalleeNetworkConnectionType</span><span class="sxs-lookup"><span data-stu-id="55085-309">CalleeNetworkConnectionType</span></span></p></td>
<td><p><span data-ttu-id="55085-310">tinyint</span><span class="sxs-lookup"><span data-stu-id="55085-310">tinyint</span></span></p></td>
<td><p><span data-ttu-id="55085-311">Тип сетевого подключения абонента: 0 – проводное, 1 — Беспроводная связь.</span><span class="sxs-lookup"><span data-stu-id="55085-311">Callee’s network connection type: 0 is wired, 1 is wireless.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-312">CalleeVPN</span><span class="sxs-lookup"><span data-stu-id="55085-312">CalleeVPN</span></span></p></td>
<td><p><span data-ttu-id="55085-313">бит</span><span class="sxs-lookup"><span data-stu-id="55085-313">bit</span></span></p></td>
<td><p><span data-ttu-id="55085-314">Указывает, подключен ли вызывающий абонент к виртуальной частной сети: 1 — виртуальная частная сеть (VPN), 0 — не VPN.</span><span class="sxs-lookup"><span data-stu-id="55085-314">Indicates whether the caller connected over a virtual private network: 1 is virtual private network (VPN), 0 is non-VPN.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-315">CalleeLinkSpeed</span><span class="sxs-lookup"><span data-stu-id="55085-315">CalleeLinkSpeed</span></span></p></td>
<td><p><span data-ttu-id="55085-316">десятичное число (18; 0)</span><span class="sxs-lookup"><span data-stu-id="55085-316">decimal(18,0)</span></span></p></td>
<td><p><span data-ttu-id="55085-317">Скорость сетевого соединения для конечной точки вызываемого абонента бит/с.</span><span class="sxs-lookup"><span data-stu-id="55085-317">Network link speed for the callee's endpoint in bps.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-318">ConversationalMOS</span><span class="sxs-lookup"><span data-stu-id="55085-318">ConversationalMOS</span></span></p></td>
<td><p><span data-ttu-id="55085-319">десятичное число (3, 2)</span><span class="sxs-lookup"><span data-stu-id="55085-319">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="55085-320">Narrowband MOS из сеансов голосовой связи (на основе обоих звуковых потоков).</span><span class="sxs-lookup"><span data-stu-id="55085-320">Narrowband Conversational MOS of the audio sessions (based on both audio streams).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-321">AppliedBandwidthLimit</span><span class="sxs-lookup"><span data-stu-id="55085-321">AppliedBandwidthLimit</span></span></p></td>
<td><p><span data-ttu-id="55085-322">целое</span><span class="sxs-lookup"><span data-stu-id="55085-322">int</span></span></p></td>
<td><p><span data-ttu-id="55085-323">Реальная пропускная способность, примененная к потоку отправки данных в соответствии с различными параметрами политики (например, "повернуть", "API", SDP, сервер политики и т. д.).</span><span class="sxs-lookup"><span data-stu-id="55085-323">Actual bandwidth applied to the given send side stream given various policy settings (TURN, API, SDP, Policy Server, and so on).</span></span> <span data-ttu-id="55085-324">Это не следует путать с эффективной пропускной способностью, так как в зависимости от оценки пропускной способности может снизиться эффективная пропускная способность.</span><span class="sxs-lookup"><span data-stu-id="55085-324">This is not to be confused with the effective bandwidth because there can be a lower effective bandwidth based on the bandwidth estimate.</span></span> <span data-ttu-id="55085-325">Это является, по сути, максимальной пропускной способностью потока отправки, который может занимать ограничения пропускной способности, наложенные на эту оценку.</span><span class="sxs-lookup"><span data-stu-id="55085-325">This is basically the maximum bandwidth the send stream can take barring limits imposed by the bandwidth estimate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-326">JitterInterArrival</span><span class="sxs-lookup"><span data-stu-id="55085-326">JitterInterArrival</span></span></p></td>
<td><p><span data-ttu-id="55085-327">целое</span><span class="sxs-lookup"><span data-stu-id="55085-327">int</span></span></p></td>
<td><p><span data-ttu-id="55085-328">Средняя колебание сети из статистики протокола управления временем в реальном времени (RTCP).</span><span class="sxs-lookup"><span data-stu-id="55085-328">Average network jitter from Real Time Control Protocol (RTCP) statistics.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-329">JitterInterArrivalMax</span><span class="sxs-lookup"><span data-stu-id="55085-329">JitterInterArrivalMax</span></span></p></td>
<td><p><span data-ttu-id="55085-330">целое</span><span class="sxs-lookup"><span data-stu-id="55085-330">int</span></span></p></td>
<td><p><span data-ttu-id="55085-331">Максимальная колебание сети во время звонка.</span><span class="sxs-lookup"><span data-stu-id="55085-331">Maximum network jitter during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-332">PacketLossRate</span><span class="sxs-lookup"><span data-stu-id="55085-332">PacketLossRate</span></span></p></td>
<td><p><span data-ttu-id="55085-333">десятичное число (5; 4)</span><span class="sxs-lookup"><span data-stu-id="55085-333">decimal(5,4)</span></span></p></td>
<td><p><span data-ttu-id="55085-334">Средняя скорость потерь пакетов во время звонка.</span><span class="sxs-lookup"><span data-stu-id="55085-334">Average packet loss rate during the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-335">PacketLossRateMax</span><span class="sxs-lookup"><span data-stu-id="55085-335">PacketLossRateMax</span></span></p></td>
<td><p><span data-ttu-id="55085-336">десятичное число (5; 4)</span><span class="sxs-lookup"><span data-stu-id="55085-336">decimal(5,4)</span></span></p></td>
<td><p><span data-ttu-id="55085-337">Максимальное количество потерь пакетов, замеченное во время звонка.</span><span class="sxs-lookup"><span data-stu-id="55085-337">Maximum packet loss observed during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-338">BurstDensity</span><span class="sxs-lookup"><span data-stu-id="55085-338">BurstDensity</span></span></p></td>
<td><p><span data-ttu-id="55085-339">десятичное число (9; 4)</span><span class="sxs-lookup"><span data-stu-id="55085-339">decimal(9,4)</span></span></p></td>
<td><p><span data-ttu-id="55085-340">Средняя плотность потери пакетов во время звонка.</span><span class="sxs-lookup"><span data-stu-id="55085-340">Average density of packet loss during bursts of losses during the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-341">BurstDuration</span><span class="sxs-lookup"><span data-stu-id="55085-341">BurstDuration</span></span></p></td>
<td><p><span data-ttu-id="55085-342">целое</span><span class="sxs-lookup"><span data-stu-id="55085-342">int</span></span></p></td>
<td><p><span data-ttu-id="55085-343">Средняя продолжительность потери пакетов в течение заданных потерь во время звонка.</span><span class="sxs-lookup"><span data-stu-id="55085-343">Average duration of packet loss during bursts of losses during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-344">BurstGapDensity</span><span class="sxs-lookup"><span data-stu-id="55085-344">BurstGapDensity</span></span></p></td>
<td><p><span data-ttu-id="55085-345">десятичное число (9; 4)</span><span class="sxs-lookup"><span data-stu-id="55085-345">decimal(9,4)</span></span></p></td>
<td><p><span data-ttu-id="55085-346">Средняя плотность потери пакетов при пропуске между пакетами потери данных.</span><span class="sxs-lookup"><span data-stu-id="55085-346">Average density of packet loss during gaps between bursts of packet loss.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-347">BurstGapDuration</span><span class="sxs-lookup"><span data-stu-id="55085-347">BurstGapDuration</span></span></p></td>
<td><p><span data-ttu-id="55085-348">целое</span><span class="sxs-lookup"><span data-stu-id="55085-348">int</span></span></p></td>
<td><p><span data-ttu-id="55085-349">Средняя продолжительность промежутков между пакетами потери данных.</span><span class="sxs-lookup"><span data-stu-id="55085-349">Average duration of gaps between bursts of packet loss.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-350">PacketUtilization</span><span class="sxs-lookup"><span data-stu-id="55085-350">PacketUtilization</span></span></p></td>
<td><p><span data-ttu-id="55085-351">целое</span><span class="sxs-lookup"><span data-stu-id="55085-351">int</span></span></p></td>
<td><p><span data-ttu-id="55085-352">Число пакетов для аудиопотока.</span><span class="sxs-lookup"><span data-stu-id="55085-352">Packet count for the audio stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-353">Самый пропускная способность</span><span class="sxs-lookup"><span data-stu-id="55085-353">BandwidthEst</span></span></p></td>
<td><p><span data-ttu-id="55085-354">целое</span><span class="sxs-lookup"><span data-stu-id="55085-354">int</span></span></p></td>
<td><p><span data-ttu-id="55085-355">Оценка пропускной способности для аудиопотока.</span><span class="sxs-lookup"><span data-stu-id="55085-355">Bandwidth estimates for the audio stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-356">DegradationAvg</span><span class="sxs-lookup"><span data-stu-id="55085-356">DegradationAvg</span></span></p></td>
<td><p><span data-ttu-id="55085-357">десятичное число (3, 2)</span><span class="sxs-lookup"><span data-stu-id="55085-357">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="55085-358">Сетевое MOS падение на весь звонок.</span><span class="sxs-lookup"><span data-stu-id="55085-358">Network MOS Degradation for the whole call.</span></span> <span data-ttu-id="55085-359">Диапазон от 0,0 до 5,0.</span><span class="sxs-lookup"><span data-stu-id="55085-359">Range is 0.0 to 5.0.</span></span> <span data-ttu-id="55085-360">Этот показатель показывает объем сетевого MOS уменьшился из-за колебаний и потери пакетов.</span><span class="sxs-lookup"><span data-stu-id="55085-360">This metric shows the amount the Network MOS was reduced because of jitter and packet loss.</span></span> <span data-ttu-id="55085-361">Для приемлемого качества оно должно быть менее 0,5.</span><span class="sxs-lookup"><span data-stu-id="55085-361">For acceptable quality it should less than 0.5.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-362">DegradationMax</span><span class="sxs-lookup"><span data-stu-id="55085-362">DegradationMax</span></span></p></td>
<td><p><span data-ttu-id="55085-363">десятичное число (3, 2)</span><span class="sxs-lookup"><span data-stu-id="55085-363">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="55085-364">Максимальная длина сетевого MOS во время звонка.</span><span class="sxs-lookup"><span data-stu-id="55085-364">Maximum Network MOS degradation during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-365">DegradationJitterAvg</span><span class="sxs-lookup"><span data-stu-id="55085-365">DegradationJitterAvg</span></span></p></td>
<td><p><span data-ttu-id="55085-366">десятичное число (3, 2)</span><span class="sxs-lookup"><span data-stu-id="55085-366">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="55085-367">Снижение производительности сети MOS из – за колебаний.</span><span class="sxs-lookup"><span data-stu-id="55085-367">Network MOS degradation caused by jitter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-368">DegradationPacketLossAvg</span><span class="sxs-lookup"><span data-stu-id="55085-368">DegradationPacketLossAvg</span></span></p></td>
<td><p><span data-ttu-id="55085-369">десятичное число (3, 2)</span><span class="sxs-lookup"><span data-stu-id="55085-369">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="55085-370">Снижение производительности сети MOS из – за потери пакетов.</span><span class="sxs-lookup"><span data-stu-id="55085-370">Network MOS degradation caused by packet loss.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-371">PayloadDescription</span><span class="sxs-lookup"><span data-stu-id="55085-371">PayloadDescription</span></span></p></td>
<td><p><span data-ttu-id="55085-372">целое</span><span class="sxs-lookup"><span data-stu-id="55085-372">int</span></span></p></td>
<td><p><span data-ttu-id="55085-373">Аудиокодек, использованный для вызова, на который ссылается <a href="lync-server-2013-payloaddescription-table.md">Таблица PayloadDescription в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="55085-373">The audio codec used for the call, referenced from the <a href="lync-server-2013-payloaddescription-table.md">PayloadDescription table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-374">AudioSampleRate</span><span class="sxs-lookup"><span data-stu-id="55085-374">AudioSampleRate</span></span></p></td>
<td><p><span data-ttu-id="55085-375">целое</span><span class="sxs-lookup"><span data-stu-id="55085-375">int</span></span></p></td>
<td><p><span data-ttu-id="55085-376">Частота дискретизации для аудиопотока.</span><span class="sxs-lookup"><span data-stu-id="55085-376">Sampling rate for the audio stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-377">CallerSendSignalLevel</span><span class="sxs-lookup"><span data-stu-id="55085-377">CallerSendSignalLevel</span></span></p></td>
<td><p><span data-ttu-id="55085-378">целое</span><span class="sxs-lookup"><span data-stu-id="55085-378">int</span></span></p></td>
<td><p><span data-ttu-id="55085-379">Уровень звукового сигнала, выступающем после аналогового усиления, для звука, отправленного вызывающим абонентом.</span><span class="sxs-lookup"><span data-stu-id="55085-379">Post-Analog Gain Control audio signal level for the audio the caller sent.</span></span> <span data-ttu-id="55085-380">Единицей измерения для этой метрики является dBmo.</span><span class="sxs-lookup"><span data-stu-id="55085-380">The unit for this metric is dBmo.</span></span> <span data-ttu-id="55085-381">Для приемлемого качества оно должно быть не менее 30 dBmo.</span><span class="sxs-lookup"><span data-stu-id="55085-381">For acceptable quality, it should be at least 30 dBmo.</span></span> <span data-ttu-id="55085-382">Этот показатель не передается сервером Конференции и IP-телефонами по протоколу A/V.</span><span class="sxs-lookup"><span data-stu-id="55085-382">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-383">CallerRecvSignalLevel</span><span class="sxs-lookup"><span data-stu-id="55085-383">CallerRecvSignalLevel</span></span></p></td>
<td><p><span data-ttu-id="55085-384">целое</span><span class="sxs-lookup"><span data-stu-id="55085-384">int</span></span></p></td>
<td><p><span data-ttu-id="55085-385">Уровень звукового сигнала для звука, полученного вызывающим абонентом.</span><span class="sxs-lookup"><span data-stu-id="55085-385">Audio signal level for the audio the caller received.</span></span> <span data-ttu-id="55085-386">Единицей измерения для этой метрики является dBmo.</span><span class="sxs-lookup"><span data-stu-id="55085-386">The unit for this metric is dBmo.</span></span> <span data-ttu-id="55085-387">Для приемлемого качества оно должно быть не менее 30 dBmo.</span><span class="sxs-lookup"><span data-stu-id="55085-387">For acceptable quality, it should be at least 30 dBmo.</span></span> <span data-ttu-id="55085-388">Этот показатель не передается сервером Конференции и IP-телефонами по протоколу A/V.</span><span class="sxs-lookup"><span data-stu-id="55085-388">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-389">CallerSendNoiseLevel</span><span class="sxs-lookup"><span data-stu-id="55085-389">CallerSendNoiseLevel</span></span></p></td>
<td><p><span data-ttu-id="55085-390">целое</span><span class="sxs-lookup"><span data-stu-id="55085-390">int</span></span></p></td>
<td><p><span data-ttu-id="55085-391">После аналогового усиления контрольного шума для звука, который отправляет вызывающий абонент.</span><span class="sxs-lookup"><span data-stu-id="55085-391">Post-Analog Gain Control audio noise level for the audio the caller sent.</span></span> <span data-ttu-id="55085-392">Единицей измерения для этой метрики является dBmo.</span><span class="sxs-lookup"><span data-stu-id="55085-392">The unit for this metric is dBmo.</span></span> <span data-ttu-id="55085-393">Для приемлемого качества оно должно быть менее 35 dBmo.</span><span class="sxs-lookup"><span data-stu-id="55085-393">For acceptable quality, it should be less than 35 dBmo.</span></span> <span data-ttu-id="55085-394">Этот показатель не передается сервером Конференции и IP-телефонами по протоколу A/V.</span><span class="sxs-lookup"><span data-stu-id="55085-394">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-395">CallerRecvNoiseLevel</span><span class="sxs-lookup"><span data-stu-id="55085-395">CallerRecvNoiseLevel</span></span></p></td>
<td><p><span data-ttu-id="55085-396">целое</span><span class="sxs-lookup"><span data-stu-id="55085-396">int</span></span></p></td>
<td><p><span data-ttu-id="55085-397">Звуковой шум по контролю звукового сопровождения для звукового сигнала, полученного вызывающим абонентом.</span><span class="sxs-lookup"><span data-stu-id="55085-397">Post-Analog Gain Control audio noise level for the audio the caller received.</span></span> <span data-ttu-id="55085-398">Единицей измерения для этой метрики является dBmo.</span><span class="sxs-lookup"><span data-stu-id="55085-398">The unit for this metric is dBmo.</span></span> <span data-ttu-id="55085-399">Для приемлемого качества оно должно быть менее 35 dBmo.</span><span class="sxs-lookup"><span data-stu-id="55085-399">For acceptable quality, it should be less than 35 dBmo.</span></span> <span data-ttu-id="55085-400">Этот показатель не передается сервером Конференции и IP-телефонами по протоколу A/V.</span><span class="sxs-lookup"><span data-stu-id="55085-400">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-401">CallerEchoReturn</span><span class="sxs-lookup"><span data-stu-id="55085-401">CallerEchoReturn</span></span></p></td>
<td><p><span data-ttu-id="55085-402">целое</span><span class="sxs-lookup"><span data-stu-id="55085-402">int</span></span></p></td>
<td><p><span data-ttu-id="55085-403">Для вызывающего абонента возводится расширение возвращающего эха.</span><span class="sxs-lookup"><span data-stu-id="55085-403">Echo Return Loss Enhancement for the caller.</span></span> <span data-ttu-id="55085-404">Единицей измерения для этой метрики является dB.</span><span class="sxs-lookup"><span data-stu-id="55085-404">The unit for this metric is dB.</span></span> <span data-ttu-id="55085-405">Более низкие значения представляют менее эхо.</span><span class="sxs-lookup"><span data-stu-id="55085-405">Lower values represent less echo.</span></span> <span data-ttu-id="55085-406">Этот показатель не передается сервером Конференции и IP-телефонами по протоколу A/V.</span><span class="sxs-lookup"><span data-stu-id="55085-406">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-407">CallerSpeakerGlitchRate</span><span class="sxs-lookup"><span data-stu-id="55085-407">CallerSpeakerGlitchRate</span></span></p></td>
<td><p><span data-ttu-id="55085-408">целое</span><span class="sxs-lookup"><span data-stu-id="55085-408">int</span></span></p></td>
<td><p><span data-ttu-id="55085-409">Среднее число сбоев в течение пяти минут для отрисовки динамик вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="55085-409">Average glitches per five minutes for the caller’s loudspeaker rendering.</span></span> <span data-ttu-id="55085-410">Для хорошего качества это должно быть меньше, чем один за пять минут.</span><span class="sxs-lookup"><span data-stu-id="55085-410">For good quality, this should be less than one per five minutes.</span></span> <span data-ttu-id="55085-411">Не сообщается серверам конференц-связи, серверам или IP-телефонам.</span><span class="sxs-lookup"><span data-stu-id="55085-411">Not reported by A/V Conferencing Servers, Mediation Servers, or IP phones.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-412">CallerMicGlitchRate</span><span class="sxs-lookup"><span data-stu-id="55085-412">CallerMicGlitchRate</span></span></p></td>
<td><p><span data-ttu-id="55085-413">целое</span><span class="sxs-lookup"><span data-stu-id="55085-413">int</span></span></p></td>
<td><p><span data-ttu-id="55085-414">Среднее число сбоев в течение пяти минут для захвата микрофона вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="55085-414">Average glitches per five minutes for the caller’s microphone capture.</span></span> <span data-ttu-id="55085-415">Для хорошего качества это должно быть менее чем на одну 5 минут.</span><span class="sxs-lookup"><span data-stu-id="55085-415">For good quality this should be less than one per five minutes.</span></span> <span data-ttu-id="55085-416">Не сообщается серверам конференц-связи, серверам или IP-телефонам.</span><span class="sxs-lookup"><span data-stu-id="55085-416">Not reported by A/V Conferencing Servers, Mediation Servers, or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-417">CallerTimestampDriftRateMic</span><span class="sxs-lookup"><span data-stu-id="55085-417">CallerTimestampDriftRateMic</span></span></p></td>
<td><p><span data-ttu-id="55085-418">десятичное число (9, 2)</span><span class="sxs-lookup"><span data-stu-id="55085-418">decimal(9,2)</span></span></p></td>
<td><p><span data-ttu-id="55085-419">Частота отсчета часов микрофона вызывающего устройства, относящихся к тактовой частоте процессора.</span><span class="sxs-lookup"><span data-stu-id="55085-419">Caller’s microphone device clock drift rate, relative to CPU clock.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-420">CallerTimestampDriftRateSpk</span><span class="sxs-lookup"><span data-stu-id="55085-420">CallerTimestampDriftRateSpk</span></span></p></td>
<td><p><span data-ttu-id="55085-421">десятичное число (9, 2)</span><span class="sxs-lookup"><span data-stu-id="55085-421">decimal(9,2)</span></span></p></td>
<td><p><span data-ttu-id="55085-422">Частота отсчета сигналов для динамиков устройства выступающего в сторону от времени ЦП.</span><span class="sxs-lookup"><span data-stu-id="55085-422">Caller’s speaker device clock drift rate, relative to CPU clock.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-423">CallerTimestampErrorMicMs</span><span class="sxs-lookup"><span data-stu-id="55085-423">CallerTimestampErrorMicMs</span></span></p></td>
<td><p><span data-ttu-id="55085-424">десятичное число (9, 2)</span><span class="sxs-lookup"><span data-stu-id="55085-424">decimal(9,2)</span></span></p></td>
<td><p><span data-ttu-id="55085-425">Средняя пометка времени потока захвата микрофона в миллисекундах за последние 20 секунд звонка.</span><span class="sxs-lookup"><span data-stu-id="55085-425">Average microphone capture stream time stamp error, in milliseconds, in the last 20 seconds of the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-426">CallerTimestampErrorSpkMs</span><span class="sxs-lookup"><span data-stu-id="55085-426">CallerTimestampErrorSpkMs</span></span></p></td>
<td><p><span data-ttu-id="55085-427">десятичное число (9, 2)</span><span class="sxs-lookup"><span data-stu-id="55085-427">decimal(9,2)</span></span></p></td>
<td><p><span data-ttu-id="55085-428">Среднее значение ошибки метки времени линейного отображения динамика вызывающего абонента в миллисекундах за последние 20 секунд звонка.</span><span class="sxs-lookup"><span data-stu-id="55085-428">Average of the caller’s speaker render stream time stamp error, in milliseconds, in the last 20 seconds of the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-429">CallerVsEntryCauses</span><span class="sxs-lookup"><span data-stu-id="55085-429">CallerVsEntryCauses</span></span></p></td>
<td><p><span data-ttu-id="55085-430">smallint</span><span class="sxs-lookup"><span data-stu-id="55085-430">smallint</span></span></p></td>
<td><p><span data-ttu-id="55085-431">Голосовая связь — это режим двусторонней печати с ограниченными возможностями перерывов.</span><span class="sxs-lookup"><span data-stu-id="55085-431">Voice switch is a half-duplex mode with reduced interruption ability.</span></span> <span data-ttu-id="55085-432">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-medialine-table.md">таблицей MediaLine в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="55085-432">See the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-433">CallerEchoEventCauses</span><span class="sxs-lookup"><span data-stu-id="55085-433">CallerEchoEventCauses</span></span></p></td>
<td><p><span data-ttu-id="55085-434">tinyint</span><span class="sxs-lookup"><span data-stu-id="55085-434">tinyint</span></span></p></td>
<td><p><span data-ttu-id="55085-435">Причины возникновения события echo для вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="55085-435">Causes of an echo event for the caller.</span></span> <span data-ttu-id="55085-436">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-medialine-table.md">таблицей MediaLine в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="55085-436">See the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-437">CallerEchoPercentMicIn</span><span class="sxs-lookup"><span data-stu-id="55085-437">CallerEchoPercentMicIn</span></span></p></td>
<td><p><span data-ttu-id="55085-438">десятичное число (5; 2)</span><span class="sxs-lookup"><span data-stu-id="55085-438">decimal(5,2)</span></span></p></td>
<td><p><span data-ttu-id="55085-439">Процент времени, в течение которого обнаружено эхо в потоке захвата микрофона вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="55085-439">Percentage of time when echo is detected in the caller’s microphone capture stream.</span></span> <span data-ttu-id="55085-440">Если используется гарнитура, значение должно быть низким.</span><span class="sxs-lookup"><span data-stu-id="55085-440">If headset is used, the value should be low.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-441">CallerEchoPercentSend</span><span class="sxs-lookup"><span data-stu-id="55085-441">CallerEchoPercentSend</span></span></p></td>
<td><p><span data-ttu-id="55085-442">десятичное число (5; 2)</span><span class="sxs-lookup"><span data-stu-id="55085-442">decimal(5,2)</span></span></p></td>
<td><p><span data-ttu-id="55085-443">Процент времени, в течение которого обнаружено эхо в потоке, отправленном вызывающим абонентом.</span><span class="sxs-lookup"><span data-stu-id="55085-443">Percentage of time when echo is detected in the caller’s sent stream.</span></span> <span data-ttu-id="55085-444">Высокий процент эха в потоках отправки указывает на наличие утечки эха.</span><span class="sxs-lookup"><span data-stu-id="55085-444">High echo percentage in send streams an indication of echo leak.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-445">CallerRxAGCSignalLevel</span><span class="sxs-lookup"><span data-stu-id="55085-445">CallerRxAGCSignalLevel</span></span></p></td>
<td><p><span data-ttu-id="55085-446">целое</span><span class="sxs-lookup"><span data-stu-id="55085-446">int</span></span></p></td>
<td><p><span data-ttu-id="55085-447">Уровень сигнала на сервере-источнике сообщений от шлюза к звуку вызывающего абонента; Это относится только к серверу обновлений.</span><span class="sxs-lookup"><span data-stu-id="55085-447">Received signal level on the Mediation Server from the Gateway for the caller’s audio; this applies only to the Mediation Server.</span></span> <span data-ttu-id="55085-448">Единица измерения этой метрики — dBoV.</span><span class="sxs-lookup"><span data-stu-id="55085-448">The unit of this metric is dBoV.</span></span> <span data-ttu-id="55085-449">Для хорошего качества допустимый диапазон должен составлять от-30 до-18 dBoV.</span><span class="sxs-lookup"><span data-stu-id="55085-449">For good quality, the acceptable range should be -30 to -18 dBoV.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-450">CallerRxAGCNoiseLevel</span><span class="sxs-lookup"><span data-stu-id="55085-450">CallerRxAGCNoiseLevel</span></span></p></td>
<td><p><span data-ttu-id="55085-451">целое</span><span class="sxs-lookup"><span data-stu-id="55085-451">int</span></span></p></td>
<td><p><span data-ttu-id="55085-452">Уровень сигнала на сервере-источнике от шлюза для звука вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="55085-452">Received signal level on the Mediation Server from the Gateway for the caller’s audio.</span></span> <span data-ttu-id="55085-453">Это относится только к серверу обновлений.</span><span class="sxs-lookup"><span data-stu-id="55085-453">This applies only to the Mediation Server.</span></span> <span data-ttu-id="55085-454">Единица измерения этой метрики — dBoV.</span><span class="sxs-lookup"><span data-stu-id="55085-454">The unit of this metric is dBoV.</span></span> <span data-ttu-id="55085-455">Для хорошего качества допустимый диапазон должен быть меньше, чем-50 dBoV.</span><span class="sxs-lookup"><span data-stu-id="55085-455">For good quality, the acceptable range should be less than -50 dBoV.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-456">CallerRxAGCGain</span><span class="sxs-lookup"><span data-stu-id="55085-456">CallerRxAGCGain</span></span></p></td>
<td><p><span data-ttu-id="55085-457">целое</span><span class="sxs-lookup"><span data-stu-id="55085-457">int</span></span></p></td>
<td><p><span data-ttu-id="55085-458">Автоматический контроль усиления (AGC) на стороне сервера-посредника, примененной к звуковому каналу вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="55085-458">Automatic gain control (AGC) on the Mediation Server side applied to the caller’s audio.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-459">CallerInitialSignalLevelRMS</span><span class="sxs-lookup"><span data-stu-id="55085-459">CallerInitialSignalLevelRMS</span></span></p></td>
<td><p><span data-ttu-id="55085-460">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="55085-460">float</span></span></p></td>
<td><p><span data-ttu-id="55085-461">Среднее значение среднего квадрата входящего сигнала для вызывающего абонента до первых 30 секунд звонка.</span><span class="sxs-lookup"><span data-stu-id="55085-461">Root mean square (RMS) of the incoming signal to the caller for up to the first 30 seconds of the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-462">CalleeSendSignalLevel</span><span class="sxs-lookup"><span data-stu-id="55085-462">CalleeSendSignalLevel</span></span></p></td>
<td><p><span data-ttu-id="55085-463">целое</span><span class="sxs-lookup"><span data-stu-id="55085-463">int</span></span></p></td>
<td><p><span data-ttu-id="55085-464">Представляет уровень звукового сигнала после аналогового усиления для звука, отправленного вызываемым абонентом.</span><span class="sxs-lookup"><span data-stu-id="55085-464">Represents the Post-Analog Gain Control audio signal level for the audio the callee sent.</span></span> <span data-ttu-id="55085-465">Единицей измерения для этой метрики является dBmo.</span><span class="sxs-lookup"><span data-stu-id="55085-465">The unit for this metric is dBmo.</span></span> <span data-ttu-id="55085-466">Для приемлемого качества оно должно быть не менее 30 dBmo.</span><span class="sxs-lookup"><span data-stu-id="55085-466">For acceptable quality, it should be at least 30 dBmo.</span></span> <span data-ttu-id="55085-467">Этот показатель не передается сервером Конференции и IP-телефонами по протоколу A/V.</span><span class="sxs-lookup"><span data-stu-id="55085-467">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-468">CalleeRecvSignalLevel</span><span class="sxs-lookup"><span data-stu-id="55085-468">CalleeRecvSignalLevel</span></span></p></td>
<td><p><span data-ttu-id="55085-469">целое</span><span class="sxs-lookup"><span data-stu-id="55085-469">int</span></span></p></td>
<td><p><span data-ttu-id="55085-470">Уровень звукового сигнала для звука, полученного вызываемым абонентом.</span><span class="sxs-lookup"><span data-stu-id="55085-470">Audio signal level for the audio the callee received.</span></span> <span data-ttu-id="55085-471">Единицей измерения для этой метрики является dBmo.</span><span class="sxs-lookup"><span data-stu-id="55085-471">The unit for this metric is dBmo.</span></span> <span data-ttu-id="55085-472">Для приемлемого качества оно должно быть не менее 30 dBmo.</span><span class="sxs-lookup"><span data-stu-id="55085-472">For acceptable quality, it should be at least 30 dBmo.</span></span> <span data-ttu-id="55085-473">Этот показатель не передается сервером Конференции и IP-телефонами по протоколу A/V.</span><span class="sxs-lookup"><span data-stu-id="55085-473">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-474">CalleeSendNoiseLevel</span><span class="sxs-lookup"><span data-stu-id="55085-474">CalleeSendNoiseLevel</span></span></p></td>
<td><p><span data-ttu-id="55085-475">целое</span><span class="sxs-lookup"><span data-stu-id="55085-475">int</span></span></p></td>
<td><p><span data-ttu-id="55085-476">После аналогового усиления контрольного шума для звука, отправленного вызываемым абонентом.</span><span class="sxs-lookup"><span data-stu-id="55085-476">Post-Analog Gain Control audio noise level for the audio the callee sent.</span></span> <span data-ttu-id="55085-477">Единицей измерения для этой метрики является dBmo.</span><span class="sxs-lookup"><span data-stu-id="55085-477">The unit for this metric is dBmo.</span></span> <span data-ttu-id="55085-478">Для приемлемого качества оно должно быть менее 35 dBmo.</span><span class="sxs-lookup"><span data-stu-id="55085-478">For acceptable quality, it should be less than 35 dBmo.</span></span> <span data-ttu-id="55085-479">Этот показатель не передается сервером Конференции и IP-телефонами по протоколу A/V.</span><span class="sxs-lookup"><span data-stu-id="55085-479">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-480">CalleeRecvNoiseLevel</span><span class="sxs-lookup"><span data-stu-id="55085-480">CalleeRecvNoiseLevel</span></span></p></td>
<td><p><span data-ttu-id="55085-481">целое</span><span class="sxs-lookup"><span data-stu-id="55085-481">int</span></span></p></td>
<td><p><span data-ttu-id="55085-482">После аналогового усиления контрольного шума для звука, полученного вызывающим абонентом, на уровне звука.</span><span class="sxs-lookup"><span data-stu-id="55085-482">Post-Analog Gain Control audio noise level for the audio the callee received.</span></span> <span data-ttu-id="55085-483">Единицей измерения для этой метрики является dBmo.</span><span class="sxs-lookup"><span data-stu-id="55085-483">The unit for this metric is dBmo.</span></span> <span data-ttu-id="55085-484">Для приемлемого качества оно должно быть менее 35 dBmo.</span><span class="sxs-lookup"><span data-stu-id="55085-484">For acceptable quality, it should be less than 35 dBmo.</span></span> <span data-ttu-id="55085-485">Этот показатель не передается сервером Конференции и IP-телефонами по протоколу A/V.</span><span class="sxs-lookup"><span data-stu-id="55085-485">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-486">CalleeEchoReturn</span><span class="sxs-lookup"><span data-stu-id="55085-486">CalleeEchoReturn</span></span></p></td>
<td><p><span data-ttu-id="55085-487">целое</span><span class="sxs-lookup"><span data-stu-id="55085-487">int</span></span></p></td>
<td><p><span data-ttu-id="55085-488">Для вызываемого функции возвращаются улучшения с потерей эха.</span><span class="sxs-lookup"><span data-stu-id="55085-488">Echo Return Loss Enhancement for the callee.</span></span> <span data-ttu-id="55085-489">Единицей измерения для этой метрики является dB.</span><span class="sxs-lookup"><span data-stu-id="55085-489">The unit for this metric is dB.</span></span> <span data-ttu-id="55085-490">Более низкие значения представляют менее эхо.</span><span class="sxs-lookup"><span data-stu-id="55085-490">Lower values represent less echo.</span></span> <span data-ttu-id="55085-491">Этот показатель не передается сервером Конференции и IP-телефонами по протоколу A/V.</span><span class="sxs-lookup"><span data-stu-id="55085-491">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-492">CalleeSpeakerGlitchRate</span><span class="sxs-lookup"><span data-stu-id="55085-492">CalleeSpeakerGlitchRate</span></span></p></td>
<td><p><span data-ttu-id="55085-493">целое</span><span class="sxs-lookup"><span data-stu-id="55085-493">int</span></span></p></td>
<td><p><span data-ttu-id="55085-494">Среднее число сбоев в течение пяти минут для отрисовки динамик вызываемого абонента.</span><span class="sxs-lookup"><span data-stu-id="55085-494">Average glitches per five minutes for the callee’s loudspeaker rendering.</span></span> <span data-ttu-id="55085-495">Для хорошего качества это должно быть меньше, чем один за пять минут.</span><span class="sxs-lookup"><span data-stu-id="55085-495">For good quality, this should be less than one per five minutes.</span></span> <span data-ttu-id="55085-496">Не сообщается серверам конференц-связи, серверам или IP-телефонам.</span><span class="sxs-lookup"><span data-stu-id="55085-496">Not reported by A/V Conferencing Servers, Mediation Servers, or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-497">CalleeMicGlitchRate</span><span class="sxs-lookup"><span data-stu-id="55085-497">CalleeMicGlitchRate</span></span></p></td>
<td><p><span data-ttu-id="55085-498">целое</span><span class="sxs-lookup"><span data-stu-id="55085-498">int</span></span></p></td>
<td><p><span data-ttu-id="55085-499">Среднее число сбоев в течение пяти минут для захвата микрофона вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="55085-499">Average glitches per five minutes for the callee’s microphone capture.</span></span> <span data-ttu-id="55085-500">Для хорошего качества это должно быть менее чем на одну 5 минут.</span><span class="sxs-lookup"><span data-stu-id="55085-500">For good quality this should be less than one per five minutes.</span></span> <span data-ttu-id="55085-501">Не сообщается серверам конференц-связи, серверам или IP-телефонам.</span><span class="sxs-lookup"><span data-stu-id="55085-501">Not reported by A/V Conferencing Servers, Mediation Servers, or IP phones.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-502">CalleeTimestampDriftRateMic</span><span class="sxs-lookup"><span data-stu-id="55085-502">CalleeTimestampDriftRateMic</span></span></p></td>
<td><p><span data-ttu-id="55085-503">десятичное число (9, 2)</span><span class="sxs-lookup"><span data-stu-id="55085-503">decimal(9,2)</span></span></p></td>
<td><p><span data-ttu-id="55085-504">Частота отсчета часов микрофона для вызываемого абонента в соответствии с тактовой частотой процессора.</span><span class="sxs-lookup"><span data-stu-id="55085-504">Callee’s microphone device clock drift rate, relative to CPU clock.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-505">CalleeTimestampDriftRateSpk</span><span class="sxs-lookup"><span data-stu-id="55085-505">CalleeTimestampDriftRateSpk</span></span></p></td>
<td><p><span data-ttu-id="55085-506">десятичное число (9, 2)</span><span class="sxs-lookup"><span data-stu-id="55085-506">decimal(9,2)</span></span></p></td>
<td><p><span data-ttu-id="55085-507">Частота отсчета звукового сигнала устройства вызываемого абонента в соответствии с тактовой частотой процессора.</span><span class="sxs-lookup"><span data-stu-id="55085-507">Callee’s speaker device clock drift rate, relative to CPU clock.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-508">CalleeTimestampErrorMicMs</span><span class="sxs-lookup"><span data-stu-id="55085-508">CalleeTimestampErrorMicMs</span></span></p></td>
<td><p><span data-ttu-id="55085-509">десятичное число (9, 2)</span><span class="sxs-lookup"><span data-stu-id="55085-509">decimal(9,2)</span></span></p></td>
<td><p><span data-ttu-id="55085-510">Средняя пометка времени потока захвата микрофона в миллисекундах за последние 20 секунд звонка.</span><span class="sxs-lookup"><span data-stu-id="55085-510">Average microphone capture stream time stamp error, in milliseconds, in the last 20 seconds of the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-511">CalleeTimestampErrorSpkMs</span><span class="sxs-lookup"><span data-stu-id="55085-511">CalleeTimestampErrorSpkMs</span></span></p></td>
<td><p><span data-ttu-id="55085-512">десятичное число (9, 2)</span><span class="sxs-lookup"><span data-stu-id="55085-512">decimal(9,2)</span></span></p></td>
<td><p><span data-ttu-id="55085-513">Среднее сообщение об ошибке пометки времени линейного отображения динамика в миллисекундах за последние 20 секунд звонка.</span><span class="sxs-lookup"><span data-stu-id="55085-513">Average of the callee’s speaker render stream time stamp error, in milliseconds, in the last 20 seconds of the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-514">CalleeVsEntryCauses</span><span class="sxs-lookup"><span data-stu-id="55085-514">CalleeVsEntryCauses</span></span></p></td>
<td><p><span data-ttu-id="55085-515">smallint</span><span class="sxs-lookup"><span data-stu-id="55085-515">smallint</span></span></p></td>
<td><p><span data-ttu-id="55085-516">Голосовая связь — это режим двусторонней печати с ограниченными возможностями перерывов.</span><span class="sxs-lookup"><span data-stu-id="55085-516">Voice switch is a half-duplex mode with reduced interruption ability.</span></span> <span data-ttu-id="55085-517">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-medialine-table.md">таблицей MediaLine в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="55085-517">See the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-518">CalleeEchoEventCauses</span><span class="sxs-lookup"><span data-stu-id="55085-518">CalleeEchoEventCauses</span></span></p></td>
<td><p><span data-ttu-id="55085-519">tinyint</span><span class="sxs-lookup"><span data-stu-id="55085-519">tinyint</span></span></p></td>
<td><p><span data-ttu-id="55085-520">Причины возникновения события echo для вызываемого объекта.</span><span class="sxs-lookup"><span data-stu-id="55085-520">Causes of an echo event for the callee.</span></span> <span data-ttu-id="55085-521">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-medialine-table.md">таблицей MediaLine в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="55085-521">See the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-522">CalleeEchoPercentMicIn</span><span class="sxs-lookup"><span data-stu-id="55085-522">CalleeEchoPercentMicIn</span></span></p></td>
<td><p><span data-ttu-id="55085-523">десятичное число (5; 2)</span><span class="sxs-lookup"><span data-stu-id="55085-523">decimal(5,2)</span></span></p></td>
<td><p><span data-ttu-id="55085-524">Процент времени, когда в потоке захвата микрофона вызываемого абонента будет обнаружено эхо.</span><span class="sxs-lookup"><span data-stu-id="55085-524">Percentage of time when echo is detected in the callee’s microphone capture stream.</span></span> <span data-ttu-id="55085-525">Если используется гарнитура, значение должно быть низким.</span><span class="sxs-lookup"><span data-stu-id="55085-525">If headset is used, the value should be low.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-526">CalleeEchoPercentSend</span><span class="sxs-lookup"><span data-stu-id="55085-526">CalleeEchoPercentSend</span></span></p></td>
<td><p><span data-ttu-id="55085-527">десятичное число (5; 2)</span><span class="sxs-lookup"><span data-stu-id="55085-527">decimal(5,2)</span></span></p></td>
<td><p><span data-ttu-id="55085-528">Процент времени, в течение которого обнаружено эхо в потоке, отправленном вызываемым абонентом.</span><span class="sxs-lookup"><span data-stu-id="55085-528">Percentage of time when echo is detected in the callee’s sent stream.</span></span> <span data-ttu-id="55085-529">Высокий процент эха в потоках отправки указывает на наличие утечки эха.</span><span class="sxs-lookup"><span data-stu-id="55085-529">High echo percentage in send streams an indication of echo leak.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-530">CalleeRxAGCSignalLevel</span><span class="sxs-lookup"><span data-stu-id="55085-530">CalleeRxAGCSignalLevel</span></span></p></td>
<td><p><span data-ttu-id="55085-531">целое</span><span class="sxs-lookup"><span data-stu-id="55085-531">int</span></span></p></td>
<td><p><span data-ttu-id="55085-532">Уровень сигнала на сервере-посреднике от шлюза для звука вызываемого абонента; Это относится только к серверу обновлений.</span><span class="sxs-lookup"><span data-stu-id="55085-532">Received signal level on the Mediation Server from the Gateway for the callee’s audio; this applies only to the Mediation Server.</span></span> <span data-ttu-id="55085-533">Единица измерения этой метрики — dBoV.</span><span class="sxs-lookup"><span data-stu-id="55085-533">The unit of this metric is dBoV.</span></span> <span data-ttu-id="55085-534">Для хорошего качества допустимый диапазон должен составлять от [-30 до-18] dBoV.</span><span class="sxs-lookup"><span data-stu-id="55085-534">For good quality, the acceptable range should be [-30 to -18] dBoV.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-535">CalleeRxAGCNoiseLevel</span><span class="sxs-lookup"><span data-stu-id="55085-535">CalleeRxAGCNoiseLevel</span></span></p></td>
<td><p><span data-ttu-id="55085-536">целое</span><span class="sxs-lookup"><span data-stu-id="55085-536">int</span></span></p></td>
<td><p><span data-ttu-id="55085-537">Уровень сигнала на сервере-посреднике от шлюза к звуковому каналу вызываемого абонента.</span><span class="sxs-lookup"><span data-stu-id="55085-537">Received signal level on the Mediation Server from the Gateway for the callee’s audio.</span></span> <span data-ttu-id="55085-538">Это относится только к серверу обновлений.</span><span class="sxs-lookup"><span data-stu-id="55085-538">This applies only to the Mediation Server.</span></span> <span data-ttu-id="55085-539">Единица измерения этой метрики — dBoV.</span><span class="sxs-lookup"><span data-stu-id="55085-539">The unit of this metric is dBoV.</span></span> <span data-ttu-id="55085-540">Для хорошего качества допустимый диапазон должен быть меньше, чем-50 dBoV.</span><span class="sxs-lookup"><span data-stu-id="55085-540">For good quality, the acceptable range should be less than -50 dBoV.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-541">CalleeRxAGCGain</span><span class="sxs-lookup"><span data-stu-id="55085-541">CalleeRxAGCGain</span></span></p></td>
<td><p><span data-ttu-id="55085-542">целое</span><span class="sxs-lookup"><span data-stu-id="55085-542">int</span></span></p></td>
<td><p><span data-ttu-id="55085-543">Функция автоматического усиления доступа (AGC) на стороне сервера-посредника, примененная к звуковому каналу вызываемого абонента.</span><span class="sxs-lookup"><span data-stu-id="55085-543">Automatic gain control (AGC) on the Mediation Server side applied to the callee’s audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-544">CalleeInitialSignalLevelRMS</span><span class="sxs-lookup"><span data-stu-id="55085-544">CalleeInitialSignalLevelRMS</span></span></p></td>
<td><p><span data-ttu-id="55085-545">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="55085-545">float</span></span></p></td>
<td><p><span data-ttu-id="55085-546">Среднее значение среднего квадрата (RMS) входящего сигнала для вызываемого абонента до первых 30 секунд звонка.</span><span class="sxs-lookup"><span data-stu-id="55085-546">Root mean square (RMS) of the incoming signal to the callee for up to the first 30 seconds of the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-547">RatioConcealedSamplesAvg</span><span class="sxs-lookup"><span data-stu-id="55085-547">RatioConcealedSamplesAvg</span></span></p></td>
<td><p><span data-ttu-id="55085-548">десятичное число (5; 2)</span><span class="sxs-lookup"><span data-stu-id="55085-548">decimal(5,2)</span></span></p></td>
<td><p><span data-ttu-id="55085-549">Среднее отношение количества преобразованных образцов, созданных при воспроизведении звука, на обычные выборки.</span><span class="sxs-lookup"><span data-stu-id="55085-549">Average ratio of concealed samples generated by audio healing to typical samples.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-550">RatioStretchedSamplesAvg</span><span class="sxs-lookup"><span data-stu-id="55085-550">RatioStretchedSamplesAvg</span></span></p></td>
<td><p><span data-ttu-id="55085-551">десятичное число (5; 2)</span><span class="sxs-lookup"><span data-stu-id="55085-551">decimal(5,2)</span></span></p></td>
<td><p><span data-ttu-id="55085-552">Среднее отношение растянутых образцов, созданных при воспроизведении звука, на обычные выборки.</span><span class="sxs-lookup"><span data-stu-id="55085-552">Average ratio of stretched samples generated by audio healing to typical samples.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-553">RatioCompressedSamplesAvg</span><span class="sxs-lookup"><span data-stu-id="55085-553">RatioCompressedSamplesAvg</span></span></p></td>
<td><p><span data-ttu-id="55085-554">десятичное число (5; 2)</span><span class="sxs-lookup"><span data-stu-id="55085-554">decimal(5,2)</span></span></p></td>
<td><p><span data-ttu-id="55085-555">Среднее отношение количества сжатых образцов, созданных при восстановлении звука, на обычные образцы.</span><span class="sxs-lookup"><span data-stu-id="55085-555">Average ratio of compressed samples generated by audio healing to typical samples.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-556">RoundTrip</span><span class="sxs-lookup"><span data-stu-id="55085-556">RoundTrip</span></span></p></td>
<td><p><span data-ttu-id="55085-557">целое</span><span class="sxs-lookup"><span data-stu-id="55085-557">int</span></span></p></td>
<td><p><span data-ttu-id="55085-558">Время кругового приема из статистики RTCP.</span><span class="sxs-lookup"><span data-stu-id="55085-558">Round trip time from RTCP statistics.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-559">RoundTripMax</span><span class="sxs-lookup"><span data-stu-id="55085-559">RoundTripMax</span></span></p></td>
<td><p><span data-ttu-id="55085-560">целое</span><span class="sxs-lookup"><span data-stu-id="55085-560">int</span></span></p></td>
<td><p><span data-ttu-id="55085-561">Максимальное время кругового приема для звукового потока.</span><span class="sxs-lookup"><span data-stu-id="55085-561">Maximum round trip time for the audio stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-562">OverallAvgNetworkMOS</span><span class="sxs-lookup"><span data-stu-id="55085-562">OverallAvgNetworkMOS</span></span></p></td>
<td><p><span data-ttu-id="55085-563">десятичное число (3, 2)</span><span class="sxs-lookup"><span data-stu-id="55085-563">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="55085-564">Средняя сетевая MOS широкополосному для звонка.</span><span class="sxs-lookup"><span data-stu-id="55085-564">Average wideband Network MOS for the call.</span></span> <span data-ttu-id="55085-565">Эта метрика зависит от потерь пакетов, колебаний и используемого кодека.</span><span class="sxs-lookup"><span data-stu-id="55085-565">This metric depends on the packet loss, jitter, and codec used.</span></span> <span data-ttu-id="55085-566">Диапазон от 1,0 до 5,0.</span><span class="sxs-lookup"><span data-stu-id="55085-566">Range is 1.0 to 5.0.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-567">OverallMinNetworkMOS</span><span class="sxs-lookup"><span data-stu-id="55085-567">OverallMinNetworkMOS</span></span></p></td>
<td><p><span data-ttu-id="55085-568">десятичное число (3, 2)</span><span class="sxs-lookup"><span data-stu-id="55085-568">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="55085-569">Минимальная широкополосному сети MOS для звонка.</span><span class="sxs-lookup"><span data-stu-id="55085-569">Minimum wideband Network MOS for the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-570">SendListenMOS</span><span class="sxs-lookup"><span data-stu-id="55085-570">SendListenMOS</span></span></p></td>
<td><p><span data-ttu-id="55085-571">десятичное число (3, 2)</span><span class="sxs-lookup"><span data-stu-id="55085-571">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="55085-572">Средняя прогнозируемая широкополосному прослушивания MOS для звукового сигнала, в том числе уровней речи, шума и характеристик устройства захвата.</span><span class="sxs-lookup"><span data-stu-id="55085-572">Average predicted wideband Listening MOS score for audio sent, including speech level, noise level and capture device characteristics.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-573">SendListenMOSMin</span><span class="sxs-lookup"><span data-stu-id="55085-573">SendListenMOSMin</span></span></p></td>
<td><p><span data-ttu-id="55085-574">десятичное число (3, 2)</span><span class="sxs-lookup"><span data-stu-id="55085-574">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="55085-575">Минимальная SendListenMOS для звонка.</span><span class="sxs-lookup"><span data-stu-id="55085-575">Minimum SendListenMOS for the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-576">RecvListenMOS</span><span class="sxs-lookup"><span data-stu-id="55085-576">RecvListenMOS</span></span></p></td>
<td><p><span data-ttu-id="55085-577">десятичное число (3, 2)</span><span class="sxs-lookup"><span data-stu-id="55085-577">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="55085-578">Средняя прогнозируемая широкополосному прослушивания MOS для звуковых сообщений, полученных из сети, включая уровень речи, уровень шума, кодек, условия сети и характеристики устройства захвата.</span><span class="sxs-lookup"><span data-stu-id="55085-578">Average predicted wideband Listening MOS score for audio received from the network including speech level, noise level, codec, network conditions and capture device characteristics.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-579">RecvListenMOSMin</span><span class="sxs-lookup"><span data-stu-id="55085-579">RecvListenMOSMin</span></span></p></td>
<td><p><span data-ttu-id="55085-580">десятичное число (3, 2)</span><span class="sxs-lookup"><span data-stu-id="55085-580">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="55085-581">Минимальная RecvListenMOS для звонка.</span><span class="sxs-lookup"><span data-stu-id="55085-581">Minimum RecvListenMOS for the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55085-582">AudioFECUsed</span><span class="sxs-lookup"><span data-stu-id="55085-582">AudioFECUsed</span></span></p></td>
<td><p><span data-ttu-id="55085-583">бит</span><span class="sxs-lookup"><span data-stu-id="55085-583">bit</span></span></p></td>
<td><p><span data-ttu-id="55085-584">Указывает, был ли использован голосовой FEC для звонка.</span><span class="sxs-lookup"><span data-stu-id="55085-584">Indicates whether audio FEC was used for the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55085-585">SenderIsCallerPAI</span><span class="sxs-lookup"><span data-stu-id="55085-585">SenderIsCallerPAI</span></span></p></td>
<td><p><span data-ttu-id="55085-586">бит</span><span class="sxs-lookup"><span data-stu-id="55085-586">bit</span></span></p></td>
<td><p><span data-ttu-id="55085-587">Указывает направление, в котором определяются p-утвержденные сведения; 1 — направление потока на вызываемый абонентом. 0 — направление потока из вызываемого объекта вызывающему абоненту.</span><span class="sxs-lookup"><span data-stu-id="55085-587">Indicates direction of the p-asserted identify information; 1 means the stream direction is from the caller to the callee; 0 means the stream direction is from the callee to the caller.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="55085-588">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="55085-588">


</div>

<span> </span>

</div>

</div>

</span></span></div>

