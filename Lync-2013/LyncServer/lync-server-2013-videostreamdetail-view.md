---
title: 'Lync Server 2013: представление VideoStreamDetail'
description: 'Lync Server 2013: VideoStreamDetail View.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: VideoStreamDetail view
ms:assetid: ec8c45e1-307d-40ec-a75e-6083306105f2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721928(v=OCS.15)
ms:contentKeyID: 49733863
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a3f420c292627d15fd0d54f2eba01c565a49a72d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443428"
---
# <a name="videostreamdetail-view-in-lync-server-2013"></a><span data-ttu-id="7090f-103">VideoStreamDetail представления в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7090f-103">VideoStreamDetail view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7090f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7090f-104">

<span> </span></span></span>

<span data-ttu-id="7090f-105">_**Тема последнего изменения:** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="7090f-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="7090f-106">В представлении VideoStreamDetail хранятся сведения о каждом видеопотоке в базе данных.</span><span class="sxs-lookup"><span data-stu-id="7090f-106">The VideoStreamDetail View stores information about each video stream in the database.</span></span> <span data-ttu-id="7090f-107">Это представление было представлено в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="7090f-107">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7090f-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="7090f-108">Column</span></span></th>
<th><span data-ttu-id="7090f-109">Тип данных</span><span class="sxs-lookup"><span data-stu-id="7090f-109">Data Type</span></span></th>
<th><span data-ttu-id="7090f-110">Описание</span><span class="sxs-lookup"><span data-stu-id="7090f-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7090f-111">SessionTime</span><span class="sxs-lookup"><span data-stu-id="7090f-111">SessionTime</span></span></p></td>
<td><p><span data-ttu-id="7090f-112">datetime</span><span class="sxs-lookup"><span data-stu-id="7090f-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="7090f-113">На которую ссылается <a href="lync-server-2013-medialine-table.md">Таблица MediaLine в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="7090f-113">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7090f-114">SessionSeq</span><span class="sxs-lookup"><span data-stu-id="7090f-114">SessionSeq</span></span></p></td>
<td><p><span data-ttu-id="7090f-115">целое</span><span class="sxs-lookup"><span data-stu-id="7090f-115">int</span></span></p></td>
<td><p><span data-ttu-id="7090f-116">На которую ссылается <a href="lync-server-2013-medialine-table.md">Таблица MediaLine в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="7090f-116">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7090f-117">MediaLineLabel</span><span class="sxs-lookup"><span data-stu-id="7090f-117">MediaLineLabel</span></span></p></td>
<td><p><span data-ttu-id="7090f-118">tinyint</span><span class="sxs-lookup"><span data-stu-id="7090f-118">tinyint</span></span></p></td>
<td><p><span data-ttu-id="7090f-119">На которую ссылается <a href="lync-server-2013-medialine-table.md">Таблица MediaLine в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="7090f-119">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7090f-120">StreamId</span><span class="sxs-lookup"><span data-stu-id="7090f-120">StreamId</span></span></p></td>
<td><p><span data-ttu-id="7090f-121">целое</span><span class="sxs-lookup"><span data-stu-id="7090f-121">int</span></span></p></td>
<td><p><span data-ttu-id="7090f-122">Уникальный идентификатор в строке мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7090f-122">Unique ID within a media line.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7090f-123">StartTime</span><span class="sxs-lookup"><span data-stu-id="7090f-123">StartTime</span></span></p></td>
<td><p><span data-ttu-id="7090f-124">datetime</span><span class="sxs-lookup"><span data-stu-id="7090f-124">datetime</span></span></p></td>
<td><p><span data-ttu-id="7090f-125">Время начала сеанса.</span><span class="sxs-lookup"><span data-stu-id="7090f-125">Start time of the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7090f-126">EndTime</span><span class="sxs-lookup"><span data-stu-id="7090f-126">EndTime</span></span></p></td>
<td><p><span data-ttu-id="7090f-127">datetime</span><span class="sxs-lookup"><span data-stu-id="7090f-127">datetime</span></span></p></td>
<td><p><span data-ttu-id="7090f-128">Время окончания сеанса.</span><span class="sxs-lookup"><span data-stu-id="7090f-128">End time of the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7090f-129">CallPriority</span><span class="sxs-lookup"><span data-stu-id="7090f-129">CallPriority</span></span></p></td>
<td><p><span data-ttu-id="7090f-130">целое</span><span class="sxs-lookup"><span data-stu-id="7090f-130">int</span></span></p></td>
<td><p><span data-ttu-id="7090f-131">Приоритет звонка.</span><span class="sxs-lookup"><span data-stu-id="7090f-131">Priority of the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7090f-132">CallerPool</span><span class="sxs-lookup"><span data-stu-id="7090f-132">CallerPool</span></span></p></td>
<td><p><span data-ttu-id="7090f-133">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="7090f-133">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7090f-134">Полное доменное имя пула вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="7090f-134">Caller pool FQDN.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7090f-135">CalleePool</span><span class="sxs-lookup"><span data-stu-id="7090f-135">CalleePool</span></span></p></td>
<td><p><span data-ttu-id="7090f-136">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="7090f-136">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7090f-137">Полное доменное имя пула вызываемых абонентов.</span><span class="sxs-lookup"><span data-stu-id="7090f-137">Callee pool FQDN.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7090f-138">Вызывающая сторона</span><span class="sxs-lookup"><span data-stu-id="7090f-138">Caller</span></span></p></td>
<td><p><span data-ttu-id="7090f-139">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="7090f-139">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="7090f-140">URI вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="7090f-140">Caller’s URI.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7090f-141">Вызываемая сторона</span><span class="sxs-lookup"><span data-stu-id="7090f-141">Callee</span></span></p></td>
<td><p><span data-ttu-id="7090f-142">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="7090f-142">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="7090f-143">Универсальный код ресурса (URI) вызываемого абонента.</span><span class="sxs-lookup"><span data-stu-id="7090f-143">Callee’s URI.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7090f-144">CallerUserAgent</span><span class="sxs-lookup"><span data-stu-id="7090f-144">CallerUserAgent</span></span></p></td>
<td><p><span data-ttu-id="7090f-145">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="7090f-145">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7090f-146">Строка агента пользователя вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="7090f-146">Caller’s user agent string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7090f-147">CallerUserAgentType</span><span class="sxs-lookup"><span data-stu-id="7090f-147">CallerUserAgentType</span></span></p></td>
<td><p><span data-ttu-id="7090f-148">smallint</span><span class="sxs-lookup"><span data-stu-id="7090f-148">smallint</span></span></p></td>
<td><p><span data-ttu-id="7090f-149">Тип агента пользователя вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="7090f-149">Type of caller’s user agent.</span></span> <span data-ttu-id="7090f-150">Дополнительные сведения: <a href="lync-server-2013-useragent-table.md">Таблица UserAgent в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="7090f-150">See the <a href="lync-server-2013-useragent-table.md">UserAgent table in Lync Server 2013</a> for details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7090f-151">CallerUserAgentCategory</span><span class="sxs-lookup"><span data-stu-id="7090f-151">CallerUserAgentCategory</span></span></p></td>
<td><p><span data-ttu-id="7090f-152">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="7090f-152">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="7090f-153">Категория агента пользователя вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="7090f-153">Category of caller’s user agent.</span></span> <span data-ttu-id="7090f-154">Дополнительные сведения <a href="lync-server-2013-useragentdef-table-qoe.md">UserAgentDef в таблице "QoE" в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="7090f-154">See the <a href="lync-server-2013-useragentdef-table-qoe.md">UserAgentDef table (QoE) in Lync Server 2013</a> for details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7090f-155">CalleeUserAgent</span><span class="sxs-lookup"><span data-stu-id="7090f-155">CalleeUserAgent</span></span></p></td>
<td><p><span data-ttu-id="7090f-156">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="7090f-156">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7090f-157">Строка агента пользователя вызываемого абонента.</span><span class="sxs-lookup"><span data-stu-id="7090f-157">Callee’s user agent string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7090f-158">CalleeUserAgentType</span><span class="sxs-lookup"><span data-stu-id="7090f-158">CalleeUserAgentType</span></span></p></td>
<td><p><span data-ttu-id="7090f-159">smallint</span><span class="sxs-lookup"><span data-stu-id="7090f-159">smallint</span></span></p></td>
<td><p><span data-ttu-id="7090f-160">Тип агента пользователя, вызываемого абонентом.</span><span class="sxs-lookup"><span data-stu-id="7090f-160">Type of callee’s user agent.</span></span> <span data-ttu-id="7090f-161">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-useragent-table.md">таблицей UserAgent в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="7090f-161">See the <a href="lync-server-2013-useragent-table.md">UserAgent table in Lync Server 2013</a> for information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7090f-162">CalleeUserAgentCategory</span><span class="sxs-lookup"><span data-stu-id="7090f-162">CalleeUserAgentCategory</span></span></p></td>
<td><p><span data-ttu-id="7090f-163">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="7090f-163">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="7090f-164">Категория агента пользователя вызываемого абонента.</span><span class="sxs-lookup"><span data-stu-id="7090f-164">Category of callee’s user agent.</span></span> <span data-ttu-id="7090f-165">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-useragentdef-table-qoe.md">таблицей UserAgentDef (QoE) в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="7090f-165">See the <a href="lync-server-2013-useragentdef-table-qoe.md">UserAgentDef table (QoE) in Lync Server 2013</a> for information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7090f-166">CallerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7090f-166">CallerEndpoint</span></span></p></td>
<td><p><span data-ttu-id="7090f-167">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="7090f-167">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7090f-168">Имя конечной точки вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="7090f-168">Caller’s endpoint name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7090f-169">CalleeEndpoint</span><span class="sxs-lookup"><span data-stu-id="7090f-169">CalleeEndpoint</span></span></p></td>
<td><p><span data-ttu-id="7090f-170">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="7090f-170">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7090f-171">Имя конечной точки вызываемого абонента.</span><span class="sxs-lookup"><span data-stu-id="7090f-171">Callee’s endpoint name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7090f-172">CallerOS</span><span class="sxs-lookup"><span data-stu-id="7090f-172">CallerOS</span></span></p></td>
<td><p><span data-ttu-id="7090f-173">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="7090f-173">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="7090f-174">Операционная система (ОС) конечной точки вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="7090f-174">Operating system (OS) of the caller’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7090f-175">CalleeOS</span><span class="sxs-lookup"><span data-stu-id="7090f-175">CalleeOS</span></span></p></td>
<td><p><span data-ttu-id="7090f-176">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="7090f-176">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="7090f-177">Операционная система (ОС) конечной точки вызываемого абонента.</span><span class="sxs-lookup"><span data-stu-id="7090f-177">Operating system (OS) of the callee’s endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7090f-178">CallerCPUName</span><span class="sxs-lookup"><span data-stu-id="7090f-178">CallerCPUName</span></span></p></td>
<td><p><span data-ttu-id="7090f-179">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="7090f-179">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="7090f-180">Имя ЦП конечной точки вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="7090f-180">CPU name of the caller’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7090f-181">CalleeCPUName</span><span class="sxs-lookup"><span data-stu-id="7090f-181">CalleeCPUName</span></span></p></td>
<td><p><span data-ttu-id="7090f-182">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="7090f-182">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="7090f-183">Имя ЦП конечной точки вызываемого абонента.</span><span class="sxs-lookup"><span data-stu-id="7090f-183">CPU name of the callee’s endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7090f-184">CallerCPUNumberOfCores</span><span class="sxs-lookup"><span data-stu-id="7090f-184">CallerCPUNumberOfCores</span></span></p></td>
<td><p><span data-ttu-id="7090f-185">smallint</span><span class="sxs-lookup"><span data-stu-id="7090f-185">smallint</span></span></p></td>
<td><p><span data-ttu-id="7090f-186">Количество ядер ЦП конечной точки вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="7090f-186">Number of CPU cores of the caller’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7090f-187">CalleeCPUNumberOfCores</span><span class="sxs-lookup"><span data-stu-id="7090f-187">CalleeCPUNumberOfCores</span></span></p></td>
<td><p><span data-ttu-id="7090f-188">smallint</span><span class="sxs-lookup"><span data-stu-id="7090f-188">smallint</span></span></p></td>
<td><p><span data-ttu-id="7090f-189">Количество ядер ЦП конечной точки вызываемого абонента.</span><span class="sxs-lookup"><span data-stu-id="7090f-189">Number of CPU cores of the callee’s endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7090f-190">CallerCPUProcessorSpeed</span><span class="sxs-lookup"><span data-stu-id="7090f-190">CallerCPUProcessorSpeed</span></span></p></td>
<td><p><span data-ttu-id="7090f-191">целое</span><span class="sxs-lookup"><span data-stu-id="7090f-191">int</span></span></p></td>
<td><p><span data-ttu-id="7090f-192">Частота процессора конечной точки вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="7090f-192">CPU processor speed of the caller’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7090f-193">CalleeCPUProcessorSpeed</span><span class="sxs-lookup"><span data-stu-id="7090f-193">CalleeCPUProcessorSpeed</span></span></p></td>
<td><p><span data-ttu-id="7090f-194">целое</span><span class="sxs-lookup"><span data-stu-id="7090f-194">int</span></span></p></td>
<td><p><span data-ttu-id="7090f-195">Тактовая частота процессора на конечной точке вызываемого абонента.</span><span class="sxs-lookup"><span data-stu-id="7090f-195">CPU processor speed of the callee’s endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7090f-196">CallerVirtualizationFlag</span><span class="sxs-lookup"><span data-stu-id="7090f-196">CallerVirtualizationFlag</span></span></p></td>
<td><p><span data-ttu-id="7090f-197">tinyint</span><span class="sxs-lookup"><span data-stu-id="7090f-197">tinyint</span></span></p></td>
<td><p><span data-ttu-id="7090f-198">Указывает, работает ли система вызывающего абонента в виртуализованной среде.</span><span class="sxs-lookup"><span data-stu-id="7090f-198">Indicates whether the caller’s system is running in a virtualized environment.</span></span> <span data-ttu-id="7090f-199">Дополнительные сведения приведены <a href="lync-server-2013-endpoint-table.md">в таблице конечная точка в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="7090f-199">See the <a href="lync-server-2013-endpoint-table.md">Endpoint table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7090f-200">CalleeVirtualizationFlag</span><span class="sxs-lookup"><span data-stu-id="7090f-200">CalleeVirtualizationFlag</span></span></p></td>
<td><p><span data-ttu-id="7090f-201">tinyint</span><span class="sxs-lookup"><span data-stu-id="7090f-201">tinyint</span></span></p></td>
<td><p><span data-ttu-id="7090f-202">Указывает, работает ли система вызываемого абонента в виртуализованной среде.</span><span class="sxs-lookup"><span data-stu-id="7090f-202">Indicates whether the callee’s system is running in a virtualized environment.</span></span> <span data-ttu-id="7090f-203">Дополнительные сведения приведены <a href="lync-server-2013-endpoint-table.md">в таблице конечная точка в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="7090f-203">See the <a href="lync-server-2013-endpoint-table.md">Endpoint table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7090f-204">ConnectivityIce</span><span class="sxs-lookup"><span data-stu-id="7090f-204">ConnectivityIce</span></span></p></td>
<td><p><span data-ttu-id="7090f-205">tinyint</span><span class="sxs-lookup"><span data-stu-id="7090f-205">tinyint</span></span></p></td>
<td><p><span data-ttu-id="7090f-206">Сведения о пути к носителю, например прямая или ретранслируемая.</span><span class="sxs-lookup"><span data-stu-id="7090f-206">Information about media path, such as direct or relayed.</span></span> <span data-ttu-id="7090f-207">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-medialine-table.md">таблицей MediaLine в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="7090f-207">See the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7090f-208">CallerIceWarningFlags</span><span class="sxs-lookup"><span data-stu-id="7090f-208">CallerIceWarningFlags</span></span></p></td>
<td><p><span data-ttu-id="7090f-209">целое</span><span class="sxs-lookup"><span data-stu-id="7090f-209">int</span></span></p></td>
<td><p><span data-ttu-id="7090f-210">Сведения о процессе интерактивной установки подключения (ICE), описанные в разделе Флаги BITS для вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="7090f-210">Information about Interactive Connectivity Establishment (ICE) process described in bits flags for the caller.</span></span> <span data-ttu-id="7090f-211">Подробности можно найти в спецификации серверного протокола контроля качества обслуживания.</span><span class="sxs-lookup"><span data-stu-id="7090f-211">For details, refer to the Quality of Experience Monitoring Server Protocol Specification.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7090f-212">CalleeIceWarningFlags</span><span class="sxs-lookup"><span data-stu-id="7090f-212">CalleeIceWarningFlags</span></span></p></td>
<td><p><span data-ttu-id="7090f-213">целое</span><span class="sxs-lookup"><span data-stu-id="7090f-213">int</span></span></p></td>
<td><p><span data-ttu-id="7090f-214">Сведения о процессе установки интерактивной связи (ICE), описанные в флагах BITS для вызываемого абонента.</span><span class="sxs-lookup"><span data-stu-id="7090f-214">Information about Interactive Connectivity Establishment (ICE) process described in bits flags for the callee.</span></span> <span data-ttu-id="7090f-215">Подробности можно найти в спецификации серверного протокола контроля качества обслуживания.</span><span class="sxs-lookup"><span data-stu-id="7090f-215">For details, refer to the Quality of Experience Monitoring Server Protocol Specification.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7090f-216">Transport</span><span class="sxs-lookup"><span data-stu-id="7090f-216">Transport</span></span></p></td>
<td><p><span data-ttu-id="7090f-217">целое</span><span class="sxs-lookup"><span data-stu-id="7090f-217">int</span></span></p></td>
<td><p><span data-ttu-id="7090f-218">Тип транспорта: 0 — UDP, 1 — TCP.</span><span class="sxs-lookup"><span data-stu-id="7090f-218">Transport type: 0 is UDP, 1 is TCP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7090f-219">CallerIPAddr</span><span class="sxs-lookup"><span data-stu-id="7090f-219">CallerIPAddr</span></span></p></td>
<td><p><span data-ttu-id="7090f-220">var (50)</span><span class="sxs-lookup"><span data-stu-id="7090f-220">var(50)</span></span></p></td>
<td><p><span data-ttu-id="7090f-221">IP-адрес вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="7090f-221">IP address of the caller.</span></span> <span data-ttu-id="7090f-222">Это может быть либо IPv4, либо IPv6-адрес.</span><span class="sxs-lookup"><span data-stu-id="7090f-222">This may be either an IPv4 or an IPv6 address.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7090f-223">CallerPort</span><span class="sxs-lookup"><span data-stu-id="7090f-223">CallerPort</span></span></p></td>
<td><p><span data-ttu-id="7090f-224">целое</span><span class="sxs-lookup"><span data-stu-id="7090f-224">int</span></span></p></td>
<td><p><span data-ttu-id="7090f-225">Порт, используемый вызывающим абонентом.</span><span class="sxs-lookup"><span data-stu-id="7090f-225">Port used by the caller.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7090f-226">CallerInside</span><span class="sxs-lookup"><span data-stu-id="7090f-226">CallerInside</span></span></p></td>
<td><p><span data-ttu-id="7090f-227">бит</span><span class="sxs-lookup"><span data-stu-id="7090f-227">bit</span></span></p></td>
<td><p><span data-ttu-id="7090f-228">Указывает, находится ли вызывающий абонент в сети Организации.</span><span class="sxs-lookup"><span data-stu-id="7090f-228">Indicates whether the caller is inside the organization network.</span></span> <span data-ttu-id="7090f-229">1 означает, что вызывающий абонент входит в корпоративную сеть, а 0 означает, что вызывающий абонент находится за пределами сети.</span><span class="sxs-lookup"><span data-stu-id="7090f-229">1 means caller is inside the enterprise network, 0 means the caller is outside the network.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7090f-230">CalleeIPAddr</span><span class="sxs-lookup"><span data-stu-id="7090f-230">CalleeIPAddr</span></span></p></td>
<td><p><span data-ttu-id="7090f-231">var (50)</span><span class="sxs-lookup"><span data-stu-id="7090f-231">var(50)</span></span></p></td>
<td><p><span data-ttu-id="7090f-232">IP-адрес вызываемого абонента.</span><span class="sxs-lookup"><span data-stu-id="7090f-232">IP address of the callee.</span></span> <span data-ttu-id="7090f-233">Это может быть либо IPv4, либо IPv6-адрес.</span><span class="sxs-lookup"><span data-stu-id="7090f-233">This may be either an IPv4 or an IPv6 address.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7090f-234">CalleePort</span><span class="sxs-lookup"><span data-stu-id="7090f-234">CalleePort</span></span></p></td>
<td><p><span data-ttu-id="7090f-235">целое</span><span class="sxs-lookup"><span data-stu-id="7090f-235">int</span></span></p></td>
<td><p><span data-ttu-id="7090f-236">Порт, используемый вызываемым абонентом.</span><span class="sxs-lookup"><span data-stu-id="7090f-236">Port used by the callee.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7090f-237">CalleeInside</span><span class="sxs-lookup"><span data-stu-id="7090f-237">CalleeInside</span></span></p></td>
<td><p><span data-ttu-id="7090f-238">бит</span><span class="sxs-lookup"><span data-stu-id="7090f-238">bit</span></span></p></td>
<td><p><span data-ttu-id="7090f-239">Указывает, входит ли вызывающий объект в сеть Организации. 1 означает вызываемый абонент в корпоративной сети, 0 означает, что вызываемый абонент находится за пределами сети.</span><span class="sxs-lookup"><span data-stu-id="7090f-239">Indicates whether the caller is inside the organization network.1 means callee is inside the enterprise network, 0 means the callee is outside the network.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7090f-240">CallerUserSite</span><span class="sxs-lookup"><span data-stu-id="7090f-240">CallerUserSite</span></span></p></td>
<td><p><span data-ttu-id="7090f-241">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="7090f-241">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="7090f-242">Имя сайта вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="7090f-242">Name of the caller’s site.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7090f-243">CallerRegion</span><span class="sxs-lookup"><span data-stu-id="7090f-243">CallerRegion</span></span></p></td>
<td><p><span data-ttu-id="7090f-244">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="7090f-244">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="7090f-245">Название страны или региона сайта вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="7090f-245">Name of the country/region of the caller’s site.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7090f-246">CalleeUserSite</span><span class="sxs-lookup"><span data-stu-id="7090f-246">CalleeUserSite</span></span></p></td>
<td><p><span data-ttu-id="7090f-247">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="7090f-247">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="7090f-248">Имя сайта вызываемого абонента.</span><span class="sxs-lookup"><span data-stu-id="7090f-248">Name of the callee’s site.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7090f-249">CalleeRegion</span><span class="sxs-lookup"><span data-stu-id="7090f-249">CalleeRegion</span></span></p></td>
<td><p><span data-ttu-id="7090f-250">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="7090f-250">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="7090f-251">Название страны или региона сайта вызываемого абонента.</span><span class="sxs-lookup"><span data-stu-id="7090f-251">Name of the country/region of the callee’s site.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7090f-252">CallerRelayIPAddr</span><span class="sxs-lookup"><span data-stu-id="7090f-252">CallerRelayIPAddr</span></span></p></td>
<td><p><span data-ttu-id="7090f-253">var (50)</span><span class="sxs-lookup"><span data-stu-id="7090f-253">var(50)</span></span></p></td>
<td><p><span data-ttu-id="7090f-254">IP-адрес службы EDGE (/V), используемой вызывающим абонентом.</span><span class="sxs-lookup"><span data-stu-id="7090f-254">IP Address of the A/V Edge service used by the caller.</span></span> <span data-ttu-id="7090f-255">Дополнительные сведения приведены в <a href="lync-server-2013-ipaddress-table.md">таблице IP-адрес в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="7090f-255">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7090f-256">CallerRelayPort</span><span class="sxs-lookup"><span data-stu-id="7090f-256">CallerRelayPort</span></span></p></td>
<td><p><span data-ttu-id="7090f-257">целое</span><span class="sxs-lookup"><span data-stu-id="7090f-257">int</span></span></p></td>
<td><p><span data-ttu-id="7090f-258">Порт для службы EDGE (A/V), используемой вызывающим абонентом.</span><span class="sxs-lookup"><span data-stu-id="7090f-258">Port on the A/V Edge service used by the caller.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7090f-259">CalleeRelayIPAddr</span><span class="sxs-lookup"><span data-stu-id="7090f-259">CalleeRelayIPAddr</span></span></p></td>
<td><p><span data-ttu-id="7090f-260">var (50)</span><span class="sxs-lookup"><span data-stu-id="7090f-260">var(50)</span></span></p></td>
<td><p><span data-ttu-id="7090f-261">Ключ IP-адреса для службы EDGE (/V), используемой вызываемым абонентом.</span><span class="sxs-lookup"><span data-stu-id="7090f-261">IP Address key of the A/V Edge service used by the callee.</span></span> <span data-ttu-id="7090f-262">Дополнительные сведения приведены в <a href="lync-server-2013-ipaddress-table.md">таблице IP-адрес в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="7090f-262">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7090f-263">CalleeRelayPort</span><span class="sxs-lookup"><span data-stu-id="7090f-263">CalleeRelayPort</span></span></p></td>
<td><p><span data-ttu-id="7090f-264">целое</span><span class="sxs-lookup"><span data-stu-id="7090f-264">int</span></span></p></td>
<td><p><span data-ttu-id="7090f-265">Порт для службы EDGE (A/V), используемой вызываемым абонентом.</span><span class="sxs-lookup"><span data-stu-id="7090f-265">Port on the A/V Edge service used by the callee.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7090f-266">CallerCaptureDev</span><span class="sxs-lookup"><span data-stu-id="7090f-266">CallerCaptureDev</span></span></p></td>
<td><p><span data-ttu-id="7090f-267">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="7090f-267">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7090f-268">Имя устройства захвата вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="7090f-268">Caller’s capture device name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7090f-269">CallerRenderDev</span><span class="sxs-lookup"><span data-stu-id="7090f-269">CallerRenderDev</span></span></p></td>
<td><p><span data-ttu-id="7090f-270">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="7090f-270">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7090f-271">Имя устройства отрисовки вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="7090f-271">Caller’s render device name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7090f-272">CallerCaptureDevDriver</span><span class="sxs-lookup"><span data-stu-id="7090f-272">CallerCaptureDevDriver</span></span></p></td>
<td><p><span data-ttu-id="7090f-273">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="7090f-273">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7090f-274">Имя драйвера устройства захвата вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="7090f-274">Caller’s capture device driver name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7090f-275">CallerRenderDevDriver</span><span class="sxs-lookup"><span data-stu-id="7090f-275">CallerRenderDevDriver</span></span></p></td>
<td><p><span data-ttu-id="7090f-276">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="7090f-276">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7090f-277">Имя драйвера устройства отрисовки вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="7090f-277">Caller’s render device driver name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7090f-278">CalleeCaptureDev</span><span class="sxs-lookup"><span data-stu-id="7090f-278">CalleeCaptureDev</span></span></p></td>
<td><p><span data-ttu-id="7090f-279">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="7090f-279">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7090f-280">Имя устройства захвата абонента.</span><span class="sxs-lookup"><span data-stu-id="7090f-280">Callee’s capture device name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7090f-281">CalleeRenderDev</span><span class="sxs-lookup"><span data-stu-id="7090f-281">CalleeRenderDev</span></span></p></td>
<td><p><span data-ttu-id="7090f-282">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="7090f-282">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7090f-283">Имя устройства отрисовки вызываемого абонента.</span><span class="sxs-lookup"><span data-stu-id="7090f-283">Callee’s render device name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7090f-284">CalleCaptureDevDriver</span><span class="sxs-lookup"><span data-stu-id="7090f-284">CalleCaptureDevDriver</span></span></p></td>
<td><p><span data-ttu-id="7090f-285">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="7090f-285">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7090f-286">Имя драйвера устройства захвата абонента.</span><span class="sxs-lookup"><span data-stu-id="7090f-286">Callee’s capture device driver name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7090f-287">CalleeRenderDevDriver</span><span class="sxs-lookup"><span data-stu-id="7090f-287">CalleeRenderDevDriver</span></span></p></td>
<td><p><span data-ttu-id="7090f-288">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="7090f-288">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7090f-289">Имя драйвера устройства обработки вызываемого абонента.</span><span class="sxs-lookup"><span data-stu-id="7090f-289">Callee’s render device driver name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7090f-290">CallerNetworkConnectionType</span><span class="sxs-lookup"><span data-stu-id="7090f-290">CallerNetworkConnectionType</span></span></p></td>
<td><p><span data-ttu-id="7090f-291">tinyint</span><span class="sxs-lookup"><span data-stu-id="7090f-291">tinyint</span></span></p></td>
<td><p><span data-ttu-id="7090f-292">Тип сетевого подключения вызывающего абонента: 0 проводное соединение, 1 — Беспроводная связь.</span><span class="sxs-lookup"><span data-stu-id="7090f-292">Caller’s network connection type: 0 is wired, 1 is wireless.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7090f-293">CallerVPN</span><span class="sxs-lookup"><span data-stu-id="7090f-293">CallerVPN</span></span></p></td>
<td><p><span data-ttu-id="7090f-294">бит</span><span class="sxs-lookup"><span data-stu-id="7090f-294">bit</span></span></p></td>
<td><p><span data-ttu-id="7090f-295">Указывает, подключен ли вызывающий абонент к виртуальной частной сети.</span><span class="sxs-lookup"><span data-stu-id="7090f-295">Indicates whether or not the caller connected over a virtual private network.</span></span> <span data-ttu-id="7090f-296">1 — это виртуальная частная сеть (VPN), а 0 — не VPN.</span><span class="sxs-lookup"><span data-stu-id="7090f-296">1 is virtual private network (VPN), 0 is non-VPN.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7090f-297">CallerLinkSpeed</span><span class="sxs-lookup"><span data-stu-id="7090f-297">CallerLinkSpeed</span></span></p></td>
<td><p><span data-ttu-id="7090f-298">десятичное число (18;)</span><span class="sxs-lookup"><span data-stu-id="7090f-298">decimal(18,)</span></span></p></td>
<td><p><span data-ttu-id="7090f-299">Скорость сетевого соединения для конечной точки вызывающего абонента бит/с.</span><span class="sxs-lookup"><span data-stu-id="7090f-299">Network link speed for the caller's endpoint in bps.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7090f-300">CalleeNetworkConnectionType</span><span class="sxs-lookup"><span data-stu-id="7090f-300">CalleeNetworkConnectionType</span></span></p></td>
<td><p><span data-ttu-id="7090f-301">tinyint</span><span class="sxs-lookup"><span data-stu-id="7090f-301">tinyint</span></span></p></td>
<td><p><span data-ttu-id="7090f-302">Тип сетевого подключения абонента: 0 – проводное, 1 — Беспроводная связь.</span><span class="sxs-lookup"><span data-stu-id="7090f-302">Callee’s network connection type: 0 is wired, 1 is wireless.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7090f-303">CalleeVPN</span><span class="sxs-lookup"><span data-stu-id="7090f-303">CalleeVPN</span></span></p></td>
<td><p><span data-ttu-id="7090f-304">бит</span><span class="sxs-lookup"><span data-stu-id="7090f-304">bit</span></span></p></td>
<td><p><span data-ttu-id="7090f-305">Указывает, подсоединен ли вызывающий абонент к виртуальной частной сети.</span><span class="sxs-lookup"><span data-stu-id="7090f-305">Indicates whether or not the callee connected over a virtual private network.</span></span> <span data-ttu-id="7090f-306">1 — это виртуальная частная сеть (VPN), а 0 — не VPN.</span><span class="sxs-lookup"><span data-stu-id="7090f-306">1 is virtual private network (VPN), 0 is non-VPN.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7090f-307">CalleeLinkSpeed</span><span class="sxs-lookup"><span data-stu-id="7090f-307">CalleeLinkSpeed</span></span></p></td>
<td><p><span data-ttu-id="7090f-308">десятичное число (18; 0)</span><span class="sxs-lookup"><span data-stu-id="7090f-308">decimal(18,0)</span></span></p></td>
<td><p><span data-ttu-id="7090f-309">Скорость сетевого соединения для конечной точки вызываемого абонента (бит/с).</span><span class="sxs-lookup"><span data-stu-id="7090f-309">Network link speed for the callee’s endpoint (in bps).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7090f-310">ConversationalMOS</span><span class="sxs-lookup"><span data-stu-id="7090f-310">ConversationalMOS</span></span></p></td>
<td><p><span data-ttu-id="7090f-311">десятичное число (3, 2)</span><span class="sxs-lookup"><span data-stu-id="7090f-311">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="7090f-312">Narrowband MOS из сеансов голосовой связи (на основе обоих звуковых потоков).</span><span class="sxs-lookup"><span data-stu-id="7090f-312">Narrowband Conversational MOS of the audio sessions (based on both audio streams).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7090f-313">AppliedBandwidthLimit</span><span class="sxs-lookup"><span data-stu-id="7090f-313">AppliedBandwidthLimit</span></span></p></td>
<td><p><span data-ttu-id="7090f-314">целое</span><span class="sxs-lookup"><span data-stu-id="7090f-314">int</span></span></p></td>
<td><p><span data-ttu-id="7090f-315">Реальная пропускная способность, примененная к потоку отправки данных в соответствии с различными параметрами политики (например, "повернуть", "API", SDP, сервер политики и т. д.).</span><span class="sxs-lookup"><span data-stu-id="7090f-315">Actual bandwidth applied to the given send side stream given various policy settings (TURN, API, SDP, Policy Server, and so on).</span></span> <span data-ttu-id="7090f-316">Это не следует путать с эффективной пропускной способностью, так как в зависимости от оценки пропускной способности может снизиться эффективная пропускная способность.</span><span class="sxs-lookup"><span data-stu-id="7090f-316">This is not to be confused with the effective bandwidth because there can be a lower effective bandwidth based on the bandwidth estimate.</span></span> <span data-ttu-id="7090f-317">Это является, по сути, максимальной пропускной способностью потока отправки, который может занимать ограничения пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="7090f-317">This is basically the maximum bandwidth the send stream can take barring limits imposed by the bandwidth estimate.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7090f-318">JitterInterArrival</span><span class="sxs-lookup"><span data-stu-id="7090f-318">JitterInterArrival</span></span></p></td>
<td><p><span data-ttu-id="7090f-319">целое</span><span class="sxs-lookup"><span data-stu-id="7090f-319">int</span></span></p></td>
<td><p><span data-ttu-id="7090f-320">Средняя колебание сети из статистики протокола управления временем в реальном времени (RTCP).</span><span class="sxs-lookup"><span data-stu-id="7090f-320">Average network jitter from Real Time Control Protocol (RTCP) statistics.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7090f-321">JitterInterArrivalMax</span><span class="sxs-lookup"><span data-stu-id="7090f-321">JitterInterArrivalMax</span></span></p></td>
<td><p><span data-ttu-id="7090f-322">целое</span><span class="sxs-lookup"><span data-stu-id="7090f-322">int</span></span></p></td>
<td><p><span data-ttu-id="7090f-323">Максимальная колебание сети во время звонка.</span><span class="sxs-lookup"><span data-stu-id="7090f-323">Maximum network jitter during the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7090f-324">RoundTrip</span><span class="sxs-lookup"><span data-stu-id="7090f-324">RoundTrip</span></span></p></td>
<td><p><span data-ttu-id="7090f-325">целое</span><span class="sxs-lookup"><span data-stu-id="7090f-325">int</span></span></p></td>
<td><p><span data-ttu-id="7090f-326">Время кругового приема из статистики RTCP.</span><span class="sxs-lookup"><span data-stu-id="7090f-326">Round trip time from RTCP statistics.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7090f-327">RoundTripMax</span><span class="sxs-lookup"><span data-stu-id="7090f-327">RoundTripMax</span></span></p></td>
<td><p><span data-ttu-id="7090f-328">целое</span><span class="sxs-lookup"><span data-stu-id="7090f-328">int</span></span></p></td>
<td><p><span data-ttu-id="7090f-329">Максимальное время кругового приема для звукового потока.</span><span class="sxs-lookup"><span data-stu-id="7090f-329">Maximum round trip time for the audio stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7090f-330">PacketLossRate</span><span class="sxs-lookup"><span data-stu-id="7090f-330">PacketLossRate</span></span></p></td>
<td><p><span data-ttu-id="7090f-331">десятичное число (5; 4)</span><span class="sxs-lookup"><span data-stu-id="7090f-331">decimal(5,4)</span></span></p></td>
<td><p><span data-ttu-id="7090f-332">Средняя скорость потерь пакетов во время звонка.</span><span class="sxs-lookup"><span data-stu-id="7090f-332">Average packet loss rate during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7090f-333">PacketLossRateMax</span><span class="sxs-lookup"><span data-stu-id="7090f-333">PacketLossRateMax</span></span></p></td>
<td><p><span data-ttu-id="7090f-334">десятичное число (5; 4)</span><span class="sxs-lookup"><span data-stu-id="7090f-334">decimal(5,4)</span></span></p></td>
<td><p><span data-ttu-id="7090f-335">Максимальное количество потерь пакетов, замеченное во время звонка.</span><span class="sxs-lookup"><span data-stu-id="7090f-335">Maximum packet loss observed during the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7090f-336">PacketUtilization</span><span class="sxs-lookup"><span data-stu-id="7090f-336">PacketUtilization</span></span></p></td>
<td><p><span data-ttu-id="7090f-337">целое</span><span class="sxs-lookup"><span data-stu-id="7090f-337">int</span></span></p></td>
<td><p><span data-ttu-id="7090f-338">Число пакетов для видеопотока (транспортный протокол в реальном времени).</span><span class="sxs-lookup"><span data-stu-id="7090f-338">Packet count for the video stream (Real Time Transport Protocol, RTP).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7090f-339">Самый пропускная способность</span><span class="sxs-lookup"><span data-stu-id="7090f-339">BandwidthEst</span></span></p></td>
<td><p><span data-ttu-id="7090f-340">целое</span><span class="sxs-lookup"><span data-stu-id="7090f-340">int</span></span></p></td>
<td><p><span data-ttu-id="7090f-341">Оценка пропускной способности для аудиопотока.</span><span class="sxs-lookup"><span data-stu-id="7090f-341">Bandwidth estimates for the audio stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7090f-342">PayloadDescription</span><span class="sxs-lookup"><span data-stu-id="7090f-342">PayloadDescription</span></span></p></td>
<td><p><span data-ttu-id="7090f-343">целое</span><span class="sxs-lookup"><span data-stu-id="7090f-343">int</span></span></p></td>
<td><p><span data-ttu-id="7090f-344">Аудиокодек, использованный для звонка, указан из <a href="lync-server-2013-payloaddescription-table.md">таблицы PayloadDescription в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="7090f-344">Audio codec used for the call, referenced from the <a href="lync-server-2013-payloaddescription-table.md">PayloadDescription table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7090f-345">VideoResolution</span><span class="sxs-lookup"><span data-stu-id="7090f-345">VideoResolution</span></span></p></td>
<td><p><span data-ttu-id="7090f-346">char (9)</span><span class="sxs-lookup"><span data-stu-id="7090f-346">char(9)</span></span></p></td>
<td><p><span data-ttu-id="7090f-347">Разрешение видео в пикселях, умноженное на высоту в пикселях.</span><span class="sxs-lookup"><span data-stu-id="7090f-347">Resolution of the video in pixels width multiplied by pixels height.</span></span> <span data-ttu-id="7090f-348">Отображается в виде строки.</span><span class="sxs-lookup"><span data-stu-id="7090f-348">Reported as a string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7090f-349">VideoBitRateAvg</span><span class="sxs-lookup"><span data-stu-id="7090f-349">VideoBitRateAvg</span></span></p></td>
<td><p><span data-ttu-id="7090f-350">целое</span><span class="sxs-lookup"><span data-stu-id="7090f-350">int</span></span></p></td>
<td><p><span data-ttu-id="7090f-351">Средняя скорость потока видео.</span><span class="sxs-lookup"><span data-stu-id="7090f-351">Average bit rate of the video stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7090f-352">InboundVideoFrameRateAvg</span><span class="sxs-lookup"><span data-stu-id="7090f-352">InboundVideoFrameRateAvg</span></span></p></td>
<td><p><span data-ttu-id="7090f-353">десятичное число (9; 4)</span><span class="sxs-lookup"><span data-stu-id="7090f-353">decimal(9,4)</span></span></p></td>
<td><p><span data-ttu-id="7090f-354">Частота кадров, полученных в видеоролике.</span><span class="sxs-lookup"><span data-stu-id="7090f-354">Frame rate of video received.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7090f-355">OutboundVideoFrameRateAvg</span><span class="sxs-lookup"><span data-stu-id="7090f-355">OutboundVideoFrameRateAvg</span></span></p></td>
<td><p><span data-ttu-id="7090f-356">десятичное число (9; 4)</span><span class="sxs-lookup"><span data-stu-id="7090f-356">decimal(9,4)</span></span></p></td>
<td><p><span data-ttu-id="7090f-357">Частота кадров, отправленных видео.</span><span class="sxs-lookup"><span data-stu-id="7090f-357">Frame rate of video sent.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7090f-358">ViideoBitRateMax</span><span class="sxs-lookup"><span data-stu-id="7090f-358">ViideoBitRateMax</span></span></p></td>
<td><p><span data-ttu-id="7090f-359">целое</span><span class="sxs-lookup"><span data-stu-id="7090f-359">int</span></span></p></td>
<td><p><span data-ttu-id="7090f-360">Максимальная скорость видеосигнала во время видеосеанса.</span><span class="sxs-lookup"><span data-stu-id="7090f-360">Maximum video bit rate during the video session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7090f-361">VideoPacketLossRate</span><span class="sxs-lookup"><span data-stu-id="7090f-361">VideoPacketLossRate</span></span></p></td>
<td><p><span data-ttu-id="7090f-362">десятичное число (9; 4)</span><span class="sxs-lookup"><span data-stu-id="7090f-362">decimal(9,4)</span></span></p></td>
<td><p><span data-ttu-id="7090f-363">Частота потери видеопакетов.</span><span class="sxs-lookup"><span data-stu-id="7090f-363">Rate at which video packets were lost.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7090f-364">VideoFrameLossRate</span><span class="sxs-lookup"><span data-stu-id="7090f-364">VideoFrameLossRate</span></span></p></td>
<td><p><span data-ttu-id="7090f-365">Decimal (9.4)</span><span class="sxs-lookup"><span data-stu-id="7090f-365">decimal(9.4)</span></span></p></td>
<td><p><span data-ttu-id="7090f-366">Процент от общего числа потерянных кадров видео.</span><span class="sxs-lookup"><span data-stu-id="7090f-366">Percentage of total video frames that are lost.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7090f-367">VideoFEC</span><span class="sxs-lookup"><span data-stu-id="7090f-367">VideoFEC</span></span></p></td>
<td><p><span data-ttu-id="7090f-368">бит</span><span class="sxs-lookup"><span data-stu-id="7090f-368">bit</span></span></p></td>
<td><p><span data-ttu-id="7090f-369">Не используется.</span><span class="sxs-lookup"><span data-stu-id="7090f-369">Not used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7090f-370">VideoAllocateBWAvg</span><span class="sxs-lookup"><span data-stu-id="7090f-370">VideoAllocateBWAvg</span></span></p></td>
<td><p><span data-ttu-id="7090f-371">целое</span><span class="sxs-lookup"><span data-stu-id="7090f-371">int</span></span></p></td>
<td><p><span data-ttu-id="7090f-372">Средний объем пропускной способности, выделенной для видео.</span><span class="sxs-lookup"><span data-stu-id="7090f-372">Average amount of bandwidth allocated for video.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7090f-373">VideoLocalFrameLossPercentageAvg</span><span class="sxs-lookup"><span data-stu-id="7090f-373">VideoLocalFrameLossPercentageAvg</span></span></p></td>
<td><p><span data-ttu-id="7090f-374">Decimal (9.4)</span><span class="sxs-lookup"><span data-stu-id="7090f-374">decimal(9.4)</span></span></p></td>
<td><p><span data-ttu-id="7090f-375">Процент от общего количества кадров видео, которые были утрачены.</span><span class="sxs-lookup"><span data-stu-id="7090f-375">Percentage of total video frames that were lost.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7090f-376">SenderIsCallerPAI</span><span class="sxs-lookup"><span data-stu-id="7090f-376">SenderIsCallerPAI</span></span></p></td>
<td><p><span data-ttu-id="7090f-377">бит</span><span class="sxs-lookup"><span data-stu-id="7090f-377">bit</span></span></p></td>
<td><p><span data-ttu-id="7090f-378">Направление потока для идентификационной информации, утвержденной p.</span><span class="sxs-lookup"><span data-stu-id="7090f-378">Stream direction for p-asserted identity information.</span></span> <span data-ttu-id="7090f-379">1 — направление потока на вызываемый абонентом. 0 — направление потока из вызываемого объекта вызывающему абоненту.</span><span class="sxs-lookup"><span data-stu-id="7090f-379">1 means the stream direction is from the caller to the callee; 0 means the stream direction is from the callee to the caller.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="7090f-380">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7090f-380">


</div>

<span> </span>

</div>

</div>

</span></span></div>

