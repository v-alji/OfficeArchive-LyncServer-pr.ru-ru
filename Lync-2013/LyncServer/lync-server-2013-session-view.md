---
title: 'Lync Server 2013: представление сеанса'
description: 'Lync Server 2013: представление сеанса.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Session view
ms:assetid: 49e33f5b-45d0-4146-a5a4-76954d895a98
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688048(v=OCS.15)
ms:contentKeyID: 49733641
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ff4bc4abbd55e073006693d28f092f077698ef75
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444793"
---
# <a name="session-view-in-lync-server-2013"></a><span data-ttu-id="253f3-103">Представление сеанса в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="253f3-103">Session view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="253f3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="253f3-104">

<span> </span></span></span>

<span data-ttu-id="253f3-105">_**Тема последнего изменения:** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="253f3-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="253f3-106">В представлении сеанса хранятся сведения о сеансах с записями в базе данных.</span><span class="sxs-lookup"><span data-stu-id="253f3-106">The Session View stores information about sessions that have records in the database.</span></span> <span data-ttu-id="253f3-107">Это представление было представлено в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="253f3-107">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="253f3-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="253f3-108">Column</span></span></th>
<th><span data-ttu-id="253f3-109">Тип данных</span><span class="sxs-lookup"><span data-stu-id="253f3-109">Data Type</span></span></th>
<th><span data-ttu-id="253f3-110">Подробности</span><span class="sxs-lookup"><span data-stu-id="253f3-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="253f3-111">ConferenceDateTime</span><span class="sxs-lookup"><span data-stu-id="253f3-111">ConferenceDateTime</span></span></p></td>
<td><p><span data-ttu-id="253f3-112">datetime</span><span class="sxs-lookup"><span data-stu-id="253f3-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="253f3-113">На которую ссылается таблица MediaLine.</span><span class="sxs-lookup"><span data-stu-id="253f3-113">Referenced from the MediaLine Table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="253f3-114">ConferenceURI</span><span class="sxs-lookup"><span data-stu-id="253f3-114">ConferenceURI</span></span></p></td>
<td><p><span data-ttu-id="253f3-115">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="253f3-115">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="253f3-116">Универсальный код ресурса (URI) для Конференции, если это конференция, или DialogID, если это одноранговый сеанс.</span><span class="sxs-lookup"><span data-stu-id="253f3-116">Conference URI if this is a conference, or DialogID if this is a peer-to-peer session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="253f3-117">Анализ</span><span class="sxs-lookup"><span data-stu-id="253f3-117">Correlation</span></span></p></td>
<td><p><span data-ttu-id="253f3-118">varchar (max)</span><span class="sxs-lookup"><span data-stu-id="253f3-118">varchar(max)</span></span></p></td>
<td><p><span data-ttu-id="253f3-119">Идентификатор корреляции для сеанса.</span><span class="sxs-lookup"><span data-stu-id="253f3-119">Correlation ID of the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="253f3-120">DialogCategory</span><span class="sxs-lookup"><span data-stu-id="253f3-120">DialogCategory</span></span></p></td>
<td><p><span data-ttu-id="253f3-121">бит</span><span class="sxs-lookup"><span data-stu-id="253f3-121">bit</span></span></p></td>
<td><p><span data-ttu-id="253f3-122">Категория диалогового окна; 0 — это сервер Lync Server для устранения проблем; 1 — это сервер исправлений для шлюза PSTN Gateway.</span><span class="sxs-lookup"><span data-stu-id="253f3-122">Dialog category; 0 is Lync Server to Mediation Server leg; 1 is Mediation Server to PSTN gateway leg.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="253f3-123">MediationServerBypassFlag</span><span class="sxs-lookup"><span data-stu-id="253f3-123">MediationServerBypassFlag</span></span></p></td>
<td><p><span data-ttu-id="253f3-124">бит</span><span class="sxs-lookup"><span data-stu-id="253f3-124">bit</span></span></p></td>
<td><p><span data-ttu-id="253f3-125">Указывает, был ли звонок пропущен.</span><span class="sxs-lookup"><span data-stu-id="253f3-125">Indicates whether or not the call was bypassed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="253f3-126">MediaBypassWarningFlag</span><span class="sxs-lookup"><span data-stu-id="253f3-126">MediaBypassWarningFlag</span></span></p></td>
<td><p><span data-ttu-id="253f3-127">целое</span><span class="sxs-lookup"><span data-stu-id="253f3-127">int</span></span></p></td>
<td><p><span data-ttu-id="253f3-128">Это поле, если оно указано, указывает, почему звонок не обходится даже в том случае, если идентификаторы обхода не совпадают.</span><span class="sxs-lookup"><span data-stu-id="253f3-128">This field, if present, indicates why a call was not bypassed even if the bypass IDs matched.</span></span> <span data-ttu-id="253f3-129">Для Lync Server определено только одно значение:</span><span class="sxs-lookup"><span data-stu-id="253f3-129">For Lync Server, only one value is defined:</span></span></p>
<p><span data-ttu-id="253f3-130">0x0001 — Неизвестный идентификатор обхода для сетевого адаптера по умолчанию</span><span class="sxs-lookup"><span data-stu-id="253f3-130">0x0001 – Unknown bypass ID for Default network adapter</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="253f3-131">StartTime</span><span class="sxs-lookup"><span data-stu-id="253f3-131">StartTime</span></span></p></td>
<td><p><span data-ttu-id="253f3-132">datetime</span><span class="sxs-lookup"><span data-stu-id="253f3-132">datetime</span></span></p></td>
<td><p><span data-ttu-id="253f3-133">Время начала звонка.</span><span class="sxs-lookup"><span data-stu-id="253f3-133">Call start time.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="253f3-134">EndTime</span><span class="sxs-lookup"><span data-stu-id="253f3-134">EndTime</span></span></p></td>
<td><p><span data-ttu-id="253f3-135">datetime</span><span class="sxs-lookup"><span data-stu-id="253f3-135">datetime</span></span></p></td>
<td><p><span data-ttu-id="253f3-136">Время окончания звонка.</span><span class="sxs-lookup"><span data-stu-id="253f3-136">Call end time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="253f3-137">CallerPool</span><span class="sxs-lookup"><span data-stu-id="253f3-137">CallerPool</span></span></p></td>
<td><p><span data-ttu-id="253f3-138">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="253f3-138">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="253f3-139">Полное доменное имя пула вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="253f3-139">Caller pool FQDN.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="253f3-140">CalleePool</span><span class="sxs-lookup"><span data-stu-id="253f3-140">CalleePool</span></span></p></td>
<td><p><span data-ttu-id="253f3-141">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="253f3-141">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="253f3-142">Полное доменное имя пула вызываемых абонентов.</span><span class="sxs-lookup"><span data-stu-id="253f3-142">Callee pool FQDN.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="253f3-143">CallerPAI</span><span class="sxs-lookup"><span data-stu-id="253f3-143">CallerPAI</span></span></p></td>
<td><p><span data-ttu-id="253f3-144">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="253f3-144">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="253f3-145">Универсальный код ресурса (URI) удостоверения вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="253f3-145">Caller’s p-asserted identity URI.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="253f3-146">CalleePAI</span><span class="sxs-lookup"><span data-stu-id="253f3-146">CalleePAI</span></span></p></td>
<td><p><span data-ttu-id="253f3-147">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="253f3-147">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="253f3-148">КОД URI удостоверения, утвержденный вызываемым p.</span><span class="sxs-lookup"><span data-stu-id="253f3-148">Callee’s p-asserted identity URI.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="253f3-149">CallerEndpoint</span><span class="sxs-lookup"><span data-stu-id="253f3-149">CallerEndpoint</span></span></p></td>
<td><p><span data-ttu-id="253f3-150">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="253f3-150">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="253f3-151">Имя конечной точки вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="253f3-151">Caller’s endpoint name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="253f3-152">CalleeEndpoint</span><span class="sxs-lookup"><span data-stu-id="253f3-152">CalleeEndpoint</span></span></p></td>
<td><p><span data-ttu-id="253f3-153">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="253f3-153">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="253f3-154">Имя конечной точки вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="253f3-154">Caller’s endpoint name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="253f3-155">CallerUserAgent</span><span class="sxs-lookup"><span data-stu-id="253f3-155">CallerUserAgent</span></span></p></td>
<td><p><span data-ttu-id="253f3-156">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="253f3-156">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="253f3-157">Строка агента пользователя вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="253f3-157">Caller’s user agent string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="253f3-158">CallerUserAgentType</span><span class="sxs-lookup"><span data-stu-id="253f3-158">CallerUserAgentType</span></span></p></td>
<td><p><span data-ttu-id="253f3-159">smallint</span><span class="sxs-lookup"><span data-stu-id="253f3-159">smallint</span></span></p></td>
<td><p><span data-ttu-id="253f3-160">Тип агента пользователя вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="253f3-160">Type of caller’s user agent.</span></span> <span data-ttu-id="253f3-161">Дополнительные сведения: <a href="lync-server-2013-useragent-table.md">Таблица UserAgent в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="253f3-161">See the <a href="lync-server-2013-useragent-table.md">UserAgent table in Lync Server 2013</a> for details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="253f3-162">CallerUserAgentCategory</span><span class="sxs-lookup"><span data-stu-id="253f3-162">CallerUserAgentCategory</span></span></p></td>
<td><p><span data-ttu-id="253f3-163">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="253f3-163">nvarchar (64)</span></span></p></td>
<td><p><span data-ttu-id="253f3-164">Категория агента пользователя вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="253f3-164">Category of caller’s user agent.</span></span> <span data-ttu-id="253f3-165">Дополнительные сведения <a href="lync-server-2013-useragentdef-table-qoe.md">UserAgentDef в таблице "QoE" в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="253f3-165">See the <a href="lync-server-2013-useragentdef-table-qoe.md">UserAgentDef table (QoE) in Lync Server 2013</a> for details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="253f3-166">CalleeUserAgent</span><span class="sxs-lookup"><span data-stu-id="253f3-166">CalleeUserAgent</span></span></p></td>
<td><p><span data-ttu-id="253f3-167">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="253f3-167">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="253f3-168">Строка агента пользователя вызываемого абонента.</span><span class="sxs-lookup"><span data-stu-id="253f3-168">Callee’s user agent string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="253f3-169">CalleeUserAgentType</span><span class="sxs-lookup"><span data-stu-id="253f3-169">CalleeUserAgentType</span></span></p></td>
<td><p><span data-ttu-id="253f3-170">smallint</span><span class="sxs-lookup"><span data-stu-id="253f3-170">smallint</span></span></p></td>
<td><p><span data-ttu-id="253f3-171">Тип агента пользователя для вызываемого абонента.</span><span class="sxs-lookup"><span data-stu-id="253f3-171">Type of user agent for the callee.</span></span> <span data-ttu-id="253f3-172">Дополнительные сведения: <a href="lync-server-2013-useragent-table.md">Таблица UserAgent в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="253f3-172">See the <a href="lync-server-2013-useragent-table.md">UserAgent table in Lync Server 2013</a> for details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="253f3-173">CalleeUserAgentCategory</span><span class="sxs-lookup"><span data-stu-id="253f3-173">CalleeUserAgentCategory</span></span></p></td>
<td><p><span data-ttu-id="253f3-174">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="253f3-174">nvarchar (64)</span></span></p></td>
<td><p><span data-ttu-id="253f3-175">Категория агента пользователя для вызываемого абонента.</span><span class="sxs-lookup"><span data-stu-id="253f3-175">User agent category for the callee.</span></span> <span data-ttu-id="253f3-176">Дополнительные сведения <a href="lync-server-2013-useragentdef-table-qoe.md">UserAgentDef в таблице "QoE" в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="253f3-176">See the <a href="lync-server-2013-useragentdef-table-qoe.md">UserAgentDef table (QoE) in Lync Server 2013</a> for details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="253f3-177">CallerURI</span><span class="sxs-lookup"><span data-stu-id="253f3-177">CallerURI</span></span></p></td>
<td><p><span data-ttu-id="253f3-178">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="253f3-178">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="253f3-179">URI вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="253f3-179">Caller’s URI.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="253f3-180">CalleeURI</span><span class="sxs-lookup"><span data-stu-id="253f3-180">CalleeURI</span></span></p></td>
<td><p><span data-ttu-id="253f3-181">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="253f3-181">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="253f3-182">Универсальный код ресурса (URI) вызываемого абонента.</span><span class="sxs-lookup"><span data-stu-id="253f3-182">Callee’s URI.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="253f3-183">CallPrioirty</span><span class="sxs-lookup"><span data-stu-id="253f3-183">CallPrioirty</span></span></p></td>
<td><p><span data-ttu-id="253f3-184">целое</span><span class="sxs-lookup"><span data-stu-id="253f3-184">int</span></span></p></td>
<td><p><span data-ttu-id="253f3-185">Приоритет звонка.</span><span class="sxs-lookup"><span data-stu-id="253f3-185">Priority of the call.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="253f3-186">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="253f3-186">


</div>

<span> </span>

</div>

</div>

</span></span></div>

