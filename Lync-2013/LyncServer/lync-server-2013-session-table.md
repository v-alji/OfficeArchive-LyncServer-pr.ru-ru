---
title: 'Lync Server 2013: таблица Session'
description: 'Lync Server 2013: таблица сеанса.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Session table
ms:assetid: 7f05529c-794d-41ed-bca4-2e85b87b2dec
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398635(v=OCS.15)
ms:contentKeyID: 48184626
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e1a52813dfea808253cc934f71a9d4c846c2dbbd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441818"
---
# <a name="session-table-in-lync-server-2013"></a><span data-ttu-id="364b8-103">Таблица Session в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="364b8-103">Session table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="364b8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="364b8-104">

<span> </span></span></span>

<span data-ttu-id="364b8-105">_**Тема последнего изменения:** 2013-09-09_</span><span class="sxs-lookup"><span data-stu-id="364b8-105">_**Topic Last Modified:** 2013-09-09_</span></span>

<span data-ttu-id="364b8-106">Каждая запись представляет собой один сеанс, в котором задействовано звуковое сопровождение, звук и видео.</span><span class="sxs-lookup"><span data-stu-id="364b8-106">Each record represents one session which involves audio or audio and video.</span></span> <span data-ttu-id="364b8-107">В нем содержатся общие сведения о сеансе.</span><span class="sxs-lookup"><span data-stu-id="364b8-107">It contains overall information about the session.</span></span> <span data-ttu-id="364b8-108">Сеанс определяется как диалоговое окно с помощью звукового или видеосигнала (SIP) между двумя конечными точками.</span><span class="sxs-lookup"><span data-stu-id="364b8-108">A session is defined as an audio or video Session Initiation Protocol (SIP) dialog between two endpoints.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="364b8-109"><strong>Столбец</strong></span><span class="sxs-lookup"><span data-stu-id="364b8-109"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="364b8-110"><strong>Тип данных</strong></span><span class="sxs-lookup"><span data-stu-id="364b8-110"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="364b8-111"><strong>Ключ/индекс</strong></span><span class="sxs-lookup"><span data-stu-id="364b8-111"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="364b8-112"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="364b8-112"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="364b8-113"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="364b8-113"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="364b8-114">datetime</span><span class="sxs-lookup"><span data-stu-id="364b8-114">datetime</span></span></p></td>
<td><p><span data-ttu-id="364b8-115">Primary</span><span class="sxs-lookup"><span data-stu-id="364b8-115">Primary</span></span></p></td>
<td><p><span data-ttu-id="364b8-116">Ссылка из <a href="lync-server-2013-dialog-table.md">таблицы диалогов в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="364b8-116">Referenced from the <a href="lync-server-2013-dialog-table.md">Dialog table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="364b8-117"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="364b8-117"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="364b8-118">целое</span><span class="sxs-lookup"><span data-stu-id="364b8-118">int</span></span></p></td>
<td><p><span data-ttu-id="364b8-119">Primary</span><span class="sxs-lookup"><span data-stu-id="364b8-119">Primary</span></span></p></td>
<td><p><span data-ttu-id="364b8-120">Ссылка из <a href="lync-server-2013-dialog-table.md">таблицы диалогов в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="364b8-120">Referenced from the <a href="lync-server-2013-dialog-table.md">Dialog table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="364b8-121"><strong>ConferenceKey</strong></span><span class="sxs-lookup"><span data-stu-id="364b8-121"><strong>ConferenceKey</strong></span></span></p></td>
<td><p><span data-ttu-id="364b8-122">целое</span><span class="sxs-lookup"><span data-stu-id="364b8-122">int</span></span></p></td>
<td><p><span data-ttu-id="364b8-123">Другом</span><span class="sxs-lookup"><span data-stu-id="364b8-123">Foreign</span></span></p></td>
<td><p><span data-ttu-id="364b8-124">Клавиша Конференции.</span><span class="sxs-lookup"><span data-stu-id="364b8-124">Conference key.</span></span> <span data-ttu-id="364b8-125">На которую ссылается <a href="lync-server-2013-conference-table.md">Таблица конференции в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="364b8-125">Referenced from the <a href="lync-server-2013-conference-table.md">Conference table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="364b8-126"><strong>CorrelationKey</strong></span><span class="sxs-lookup"><span data-stu-id="364b8-126"><strong>CorrelationKey</strong></span></span></p></td>
<td><p><span data-ttu-id="364b8-127">целое</span><span class="sxs-lookup"><span data-stu-id="364b8-127">int</span></span></p></td>
<td><p><span data-ttu-id="364b8-128">Другом</span><span class="sxs-lookup"><span data-stu-id="364b8-128">Foreign</span></span></p></td>
<td><p><span data-ttu-id="364b8-129">Ключ корреляции.</span><span class="sxs-lookup"><span data-stu-id="364b8-129">Correlation key.</span></span> <span data-ttu-id="364b8-130">На которую ссылается <a href="lync-server-2013-sessioncorrelation-table.md">Таблица SessionCorrelation в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="364b8-130">Referenced from the <a href="lync-server-2013-sessioncorrelation-table.md">SessionCorrelation table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="364b8-131"><strong>DialogCategory</strong></span><span class="sxs-lookup"><span data-stu-id="364b8-131"><strong>DialogCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="364b8-132">бит</span><span class="sxs-lookup"><span data-stu-id="364b8-132">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="364b8-133">Категория диалогового окна; 0 — это сервер Lync Server для устранения проблем; 1 — это сервер исправлений для шлюза PSTN Gateway.</span><span class="sxs-lookup"><span data-stu-id="364b8-133">Dialog category; 0 is Lync Server to Mediation Server leg; 1 is Mediation Server to PSTN gateway leg.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="364b8-134"><strong>MediationServerBypassFlag</strong></span><span class="sxs-lookup"><span data-stu-id="364b8-134"><strong>MediationServerBypassFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="364b8-135">бит</span><span class="sxs-lookup"><span data-stu-id="364b8-135">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="364b8-136">Флаг, указывающий, обходит ли звонок.</span><span class="sxs-lookup"><span data-stu-id="364b8-136">Flag indicating if the call was bypassed or not.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="364b8-137"><strong>MediaBypassWarningFlag</strong></span><span class="sxs-lookup"><span data-stu-id="364b8-137"><strong>MediaBypassWarningFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="364b8-138">целое</span><span class="sxs-lookup"><span data-stu-id="364b8-138">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="364b8-139">Это поле, если оно указано, указывает, почему звонок не обходится даже в том случае, если идентификаторы обхода не совпадают.</span><span class="sxs-lookup"><span data-stu-id="364b8-139">This field, if present, indicates why a call was not bypassed even if the bypass IDs matched.</span></span> <span data-ttu-id="364b8-140">Для Lync Server определено только одно значение.</span><span class="sxs-lookup"><span data-stu-id="364b8-140">For Lync Server, only one value is defined.</span></span></p>
<p><span data-ttu-id="364b8-141">0x0001 — Неизвестный идентификатор обхода для сетевого адаптера по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="364b8-141">0x0001 – Unknown bypass ID for Default network adapter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="364b8-142"><strong>StartTime</strong></span><span class="sxs-lookup"><span data-stu-id="364b8-142"><strong>StartTime</strong></span></span></p></td>
<td><p><span data-ttu-id="364b8-143">datetime</span><span class="sxs-lookup"><span data-stu-id="364b8-143">datetime</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="364b8-144">Время начала звонка.</span><span class="sxs-lookup"><span data-stu-id="364b8-144">Call start time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="364b8-145"><strong>EndTime</strong></span><span class="sxs-lookup"><span data-stu-id="364b8-145"><strong>EndTime</strong></span></span></p></td>
<td><p><span data-ttu-id="364b8-146">datetime</span><span class="sxs-lookup"><span data-stu-id="364b8-146">datetime</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="364b8-147">Время окончания звонка.</span><span class="sxs-lookup"><span data-stu-id="364b8-147">Call end time.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="364b8-148"><strong>CallerPool</strong></span><span class="sxs-lookup"><span data-stu-id="364b8-148"><strong>CallerPool</strong></span></span></p></td>
<td><p><span data-ttu-id="364b8-149">целое</span><span class="sxs-lookup"><span data-stu-id="364b8-149">int</span></span></p></td>
<td><p><span data-ttu-id="364b8-150">Другом</span><span class="sxs-lookup"><span data-stu-id="364b8-150">Foreign</span></span></p></td>
<td><p><span data-ttu-id="364b8-151">Пул вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="364b8-151">The pool of the caller.</span></span> <span data-ttu-id="364b8-152">Указана <a href="lync-server-2013-pool-table.md">Таблица пула в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="364b8-152">Referenced from the <a href="lync-server-2013-pool-table.md">Pool table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="364b8-153"><strong>CalleePool</strong></span><span class="sxs-lookup"><span data-stu-id="364b8-153"><strong>CalleePool</strong></span></span></p></td>
<td><p><span data-ttu-id="364b8-154">целое</span><span class="sxs-lookup"><span data-stu-id="364b8-154">int</span></span></p></td>
<td><p><span data-ttu-id="364b8-155">Другом</span><span class="sxs-lookup"><span data-stu-id="364b8-155">Foreign</span></span></p></td>
<td><p><span data-ttu-id="364b8-156">Пул приемника вызова.</span><span class="sxs-lookup"><span data-stu-id="364b8-156">The pool of the call receiver.</span></span> <span data-ttu-id="364b8-157">Указана <a href="lync-server-2013-pool-table.md">Таблица пула в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="364b8-157">Referenced from the <a href="lync-server-2013-pool-table.md">Pool table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="364b8-158"><strong>CalleePAI</strong></span><span class="sxs-lookup"><span data-stu-id="364b8-158"><strong>CalleePAI</strong></span></span></p></td>
<td><p><span data-ttu-id="364b8-159">целое</span><span class="sxs-lookup"><span data-stu-id="364b8-159">int</span></span></p></td>
<td><p><span data-ttu-id="364b8-160">Другом</span><span class="sxs-lookup"><span data-stu-id="364b8-160">Foreign</span></span></p></td>
<td><p><span data-ttu-id="364b8-161">Универсальный код ресурса (URI) SIP в удостоверении SIP (PAI) принимающей конечной точки.</span><span class="sxs-lookup"><span data-stu-id="364b8-161">SIP URI in the SIP p-asserted identity (PAI) of the receiving endpoint.</span></span> <span data-ttu-id="364b8-162">Ссылка на которую имеется <a href="lync-server-2013-user-table.md">в таблице Users в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="364b8-162">Referenced from the <a href="lync-server-2013-user-table.md">User table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="364b8-163"><strong>CallerURI</strong></span><span class="sxs-lookup"><span data-stu-id="364b8-163"><strong>CallerURI</strong></span></span></p></td>
<td><p><span data-ttu-id="364b8-164">целое</span><span class="sxs-lookup"><span data-stu-id="364b8-164">int</span></span></p></td>
<td><p><span data-ttu-id="364b8-165">Другом</span><span class="sxs-lookup"><span data-stu-id="364b8-165">Foreign</span></span></p></td>
<td><p><span data-ttu-id="364b8-166">URI вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="364b8-166">Caller’s URI.</span></span> <span data-ttu-id="364b8-167">Ссылка на которую имеется <a href="lync-server-2013-user-table.md">в таблице Users в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="364b8-167">Referenced from the <a href="lync-server-2013-user-table.md">User table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="364b8-168"><strong>CallerEndpoint</strong></span><span class="sxs-lookup"><span data-stu-id="364b8-168"><strong>CallerEndpoint</strong></span></span></p></td>
<td><p><span data-ttu-id="364b8-169">целое</span><span class="sxs-lookup"><span data-stu-id="364b8-169">int</span></span></p></td>
<td><p><span data-ttu-id="364b8-170">Другом</span><span class="sxs-lookup"><span data-stu-id="364b8-170">Foreign</span></span></p></td>
<td><p><span data-ttu-id="364b8-171">Конечная точка вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="364b8-171">Caller’s endpoint.</span></span> <span data-ttu-id="364b8-172">На которую ссылается <a href="lync-server-2013-endpoint-table.md">Таблица конечная точка в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="364b8-172">Referenced from the <a href="lync-server-2013-endpoint-table.md">Endpoint table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="364b8-173"><strong>CallerUserAgent</strong></span><span class="sxs-lookup"><span data-stu-id="364b8-173"><strong>CallerUserAgent</strong></span></span></p></td>
<td><p><span data-ttu-id="364b8-174">бит</span><span class="sxs-lookup"><span data-stu-id="364b8-174">bit</span></span></p></td>
<td><p><span data-ttu-id="364b8-175">Другом</span><span class="sxs-lookup"><span data-stu-id="364b8-175">Foreign</span></span></p></td>
<td><p><span data-ttu-id="364b8-176">Агент пользователя вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="364b8-176">Caller’s user agent.</span></span> <span data-ttu-id="364b8-177">Ссылка из <a href="lync-server-2013-useragent-table.md">таблицы UserAgent в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="364b8-177">Referenced from the <a href="lync-server-2013-useragent-table.md">UserAgent table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="364b8-178"><strong>CallPriority</strong></span><span class="sxs-lookup"><span data-stu-id="364b8-178"><strong>CallPriority</strong></span></span></p></td>
<td><p><span data-ttu-id="364b8-179">smallint</span><span class="sxs-lookup"><span data-stu-id="364b8-179">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="364b8-180">Приоритет этого звонка.</span><span class="sxs-lookup"><span data-stu-id="364b8-180">The priority of this call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="364b8-181"><strong>ClassifiedPoorCall</strong></span><span class="sxs-lookup"><span data-stu-id="364b8-181"><strong>ClassifiedPoorCall</strong></span></span></p></td>
<td><p><span data-ttu-id="364b8-182">бит</span><span class="sxs-lookup"><span data-stu-id="364b8-182">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="364b8-183">Этот столбец устарел и не используется в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="364b8-183">This column has been deprecated and is not used in Microsoft Lync Server 2013.</span></span> <span data-ttu-id="364b8-184">Вместо этого эти сведения выводятся в виде линий для отдельных носителей.</span><span class="sxs-lookup"><span data-stu-id="364b8-184">Instead, this information is reported on a per-media line bases.</span></span> <span data-ttu-id="364b8-185">Дополнительные сведения можно найти в <a href="lync-server-2013-medialine-table.md">таблице MediaLine в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="364b8-185">Refer to the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="364b8-186"><strong>CallerPAI</strong></span><span class="sxs-lookup"><span data-stu-id="364b8-186"><strong>CallerPAI</strong></span></span></p></td>
<td><p><span data-ttu-id="364b8-187">целое</span><span class="sxs-lookup"><span data-stu-id="364b8-187">int</span></span></p></td>
<td><p><span data-ttu-id="364b8-188">Другом</span><span class="sxs-lookup"><span data-stu-id="364b8-188">Foreign</span></span></p></td>
<td><p><span data-ttu-id="364b8-189">P-утвержденные-идентификационные данные пользователя, который присоединил звонок.</span><span class="sxs-lookup"><span data-stu-id="364b8-189">P-Asserted-Identity of the user who placed the call.</span></span> <span data-ttu-id="364b8-190">Идентификатор P-Assert (PAI) используется для передачи истинного удостоверения пользователя, который находил звонок.</span><span class="sxs-lookup"><span data-stu-id="364b8-190">The P-Asserted-Identity (PAI) is used to convey the true identity of the user who placed the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="364b8-191"><strong>CalleeEndpoint</strong></span><span class="sxs-lookup"><span data-stu-id="364b8-191"><strong>CalleeEndpoint</strong></span></span></p></td>
<td><p><span data-ttu-id="364b8-192">целое</span><span class="sxs-lookup"><span data-stu-id="364b8-192">int</span></span></p></td>
<td><p><span data-ttu-id="364b8-193">Другом</span><span class="sxs-lookup"><span data-stu-id="364b8-193">Foreign</span></span></p></td>
<td><p><span data-ttu-id="364b8-194">Конечная точка, в которой был получен звонок.</span><span class="sxs-lookup"><span data-stu-id="364b8-194">Endpoint that received the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="364b8-195"><strong>CalleeUserAgent</strong></span><span class="sxs-lookup"><span data-stu-id="364b8-195"><strong>CalleeUserAgent</strong></span></span></p></td>
<td><p><span data-ttu-id="364b8-196">целое</span><span class="sxs-lookup"><span data-stu-id="364b8-196">int</span></span></p></td>
<td><p><span data-ttu-id="364b8-197">Другом</span><span class="sxs-lookup"><span data-stu-id="364b8-197">Foreign</span></span></p></td>
<td><p><span data-ttu-id="364b8-198">Агент пользователя, который использовался пользователем, который получил звонок.</span><span class="sxs-lookup"><span data-stu-id="364b8-198">User agent employed by the user who received the call.</span></span> <span data-ttu-id="364b8-199">Агенты пользователей представляют собой клиентскую конечную точку.</span><span class="sxs-lookup"><span data-stu-id="364b8-199">User agents represent the client endpoint device.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="364b8-200"><strong>CalleeUri</strong></span><span class="sxs-lookup"><span data-stu-id="364b8-200"><strong>CalleeUri</strong></span></span></p></td>
<td><p><span data-ttu-id="364b8-201">целое</span><span class="sxs-lookup"><span data-stu-id="364b8-201">int</span></span></p></td>
<td><p><span data-ttu-id="364b8-202">Другом</span><span class="sxs-lookup"><span data-stu-id="364b8-202">Foreign</span></span></p></td>
<td><p><span data-ttu-id="364b8-203">Универсальный код ресурса (URI) SIP пользователя, который получил звонок.</span><span class="sxs-lookup"><span data-stu-id="364b8-203">SIP URI of the user who received the call.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="364b8-204">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="364b8-204">


</div>

<span> </span>

</div>

</div>

</span></span></div>

