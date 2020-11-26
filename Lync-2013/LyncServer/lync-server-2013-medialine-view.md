---
title: 'Lync Server 2013: представление MediaLine'
description: 'Lync Server 2013: MediaLine View.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: MediaLine view
ms:assetid: 132eca13-8913-4218-9eff-4960ced8c3dc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687972(v=OCS.15)
ms:contentKeyID: 49733560
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4c61fcc15b46958622e6cddd66427255a6def154
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445948"
---
# <a name="medialine-view-in-lync-server-2013"></a><span data-ttu-id="96bcf-103">MediaLine представления в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="96bcf-103">MediaLine view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="96bcf-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="96bcf-104">

<span> </span></span></span>

<span data-ttu-id="96bcf-105">_**Тема последнего изменения:** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="96bcf-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="96bcf-106">В представлении MediaLine хранятся сведения о каждой строке мультимедиа в базе данных.</span><span class="sxs-lookup"><span data-stu-id="96bcf-106">The MediaLine View stores information about each media line in the database.</span></span> <span data-ttu-id="96bcf-107">Один звуковой сеанс обычно состоит из одной линии звукового файла.</span><span class="sxs-lookup"><span data-stu-id="96bcf-107">One audio session typically contains one audio media line.</span></span> <span data-ttu-id="96bcf-108">Один из звуковых и видеофайлов (A/V) обычно состоит из одной линии звукового файла и одной линии видеоклипа; Тем не менее, в этом сеансе могут содержаться две строки видеофайла, если используется устройство конференц-связи или если используется представление коллекции.</span><span class="sxs-lookup"><span data-stu-id="96bcf-108">One audio and video (A/V) session typically contains one audio media line and one video media line; however, the session might contain two video media lines if a conferencing device is used or if Gallery View is used.</span></span> <span data-ttu-id="96bcf-109">Это представление было представлено в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="96bcf-109">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="96bcf-110">Столбец</span><span class="sxs-lookup"><span data-stu-id="96bcf-110">Column</span></span></th>
<th><span data-ttu-id="96bcf-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="96bcf-111">Data Type</span></span></th>
<th><span data-ttu-id="96bcf-112">сведения</span><span class="sxs-lookup"><span data-stu-id="96bcf-112">details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="96bcf-113">ConferenceDateTime</span><span class="sxs-lookup"><span data-stu-id="96bcf-113">ConferenceDateTime</span></span></p></td>
<td><p><span data-ttu-id="96bcf-114">datetime</span><span class="sxs-lookup"><span data-stu-id="96bcf-114">datetime</span></span></p></td>
<td><p><span data-ttu-id="96bcf-115">На которую ссылается <a href="lync-server-2013-medialine-table.md">Таблица MediaLine в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="96bcf-115">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96bcf-116">SessionSeq</span><span class="sxs-lookup"><span data-stu-id="96bcf-116">SessionSeq</span></span></p></td>
<td><p><span data-ttu-id="96bcf-117">целое</span><span class="sxs-lookup"><span data-stu-id="96bcf-117">int</span></span></p></td>
<td><p><span data-ttu-id="96bcf-118">На которую ссылается <a href="lync-server-2013-medialine-table.md">Таблица MediaLine в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="96bcf-118">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96bcf-119">MediaLineLabel</span><span class="sxs-lookup"><span data-stu-id="96bcf-119">MediaLineLabel</span></span></p></td>
<td><p><span data-ttu-id="96bcf-120">tinyint</span><span class="sxs-lookup"><span data-stu-id="96bcf-120">tinyint</span></span></p></td>
<td><p><span data-ttu-id="96bcf-121">На которую ссылается <a href="lync-server-2013-medialine-table.md">Таблица MediaLine в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="96bcf-121">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96bcf-122">CallerIceWarningFlags</span><span class="sxs-lookup"><span data-stu-id="96bcf-122">CallerIceWarningFlags</span></span></p></td>
<td><p><span data-ttu-id="96bcf-123">целое</span><span class="sxs-lookup"><span data-stu-id="96bcf-123">int</span></span></p></td>
<td><p><span data-ttu-id="96bcf-124">Сведения о процессе интерактивной установки подключения (ICE), описанные в разделе Флаги BITS для вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="96bcf-124">Information about Interactive Connectivity Establishment (ICE) process described in bits flags for the caller.</span></span> <span data-ttu-id="96bcf-125">Подробности можно найти в спецификации серверного протокола контроля качества обслуживания.</span><span class="sxs-lookup"><span data-stu-id="96bcf-125">For details, refer to the Quality of Experience Monitoring Server Protocol Specification.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96bcf-126">CalleeIceWarningFlags</span><span class="sxs-lookup"><span data-stu-id="96bcf-126">CalleeIceWarningFlags</span></span></p></td>
<td><p><span data-ttu-id="96bcf-127">целое</span><span class="sxs-lookup"><span data-stu-id="96bcf-127">int</span></span></p></td>
<td><p><span data-ttu-id="96bcf-128">Сведения о процессе установки интерактивной связи (ICE), описанные в флагах BITS для вызываемого абонента.</span><span class="sxs-lookup"><span data-stu-id="96bcf-128">Information about Interactive Connectivity Establishment (ICE) process described in bits flags for the callee.</span></span> <span data-ttu-id="96bcf-129">Подробности можно найти в спецификации серверного протокола контроля качества обслуживания.</span><span class="sxs-lookup"><span data-stu-id="96bcf-129">For details, refer to the Quality of Experience Monitoring Server Protocol Specification.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96bcf-130">Безопасность</span><span class="sxs-lookup"><span data-stu-id="96bcf-130">Security</span></span></p></td>
<td><p><span data-ttu-id="96bcf-131">tinyint</span><span class="sxs-lookup"><span data-stu-id="96bcf-131">tinyint</span></span></p></td>
<td><p><span data-ttu-id="96bcf-132">Профиль безопасности используется.</span><span class="sxs-lookup"><span data-stu-id="96bcf-132">Security profile in use.</span></span> <span data-ttu-id="96bcf-133">0 — NONE, 1 — SRTP, 2 — v1.</span><span class="sxs-lookup"><span data-stu-id="96bcf-133">0 is NONE, 1 is SRTP, 2 is V1.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96bcf-134">Transport</span><span class="sxs-lookup"><span data-stu-id="96bcf-134">Transport</span></span></p></td>
<td><p><span data-ttu-id="96bcf-135">tinyint</span><span class="sxs-lookup"><span data-stu-id="96bcf-135">tinyint</span></span></p></td>
<td><p><span data-ttu-id="96bcf-136">Тип транспорта.</span><span class="sxs-lookup"><span data-stu-id="96bcf-136">Transport type.</span></span> <span data-ttu-id="96bcf-137">0 — это UDP, а 1 — TCP.</span><span class="sxs-lookup"><span data-stu-id="96bcf-137">0 is UDP, 1 is TCP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96bcf-138">CallerIPAddr</span><span class="sxs-lookup"><span data-stu-id="96bcf-138">CallerIPAddr</span></span></p></td>
<td><p><span data-ttu-id="96bcf-139">var (50)</span><span class="sxs-lookup"><span data-stu-id="96bcf-139">var(50)</span></span></p></td>
<td><p><span data-ttu-id="96bcf-140">IP-адрес вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="96bcf-140">IP address of the caller.</span></span> <span data-ttu-id="96bcf-141">Это может быть либо адрес IPv4, либо IPv6.</span><span class="sxs-lookup"><span data-stu-id="96bcf-141">This can be either an IPv4 or IPv6 address.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96bcf-142">CallerPort</span><span class="sxs-lookup"><span data-stu-id="96bcf-142">CallerPort</span></span></p></td>
<td><p><span data-ttu-id="96bcf-143">целое</span><span class="sxs-lookup"><span data-stu-id="96bcf-143">int</span></span></p></td>
<td><p><span data-ttu-id="96bcf-144">Порт, используемый вызывающим абонентом.</span><span class="sxs-lookup"><span data-stu-id="96bcf-144">Port used by the caller.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96bcf-145">CallerInside</span><span class="sxs-lookup"><span data-stu-id="96bcf-145">CallerInside</span></span></p></td>
<td><p><span data-ttu-id="96bcf-146">бит</span><span class="sxs-lookup"><span data-stu-id="96bcf-146">bit</span></span></p></td>
<td><p><span data-ttu-id="96bcf-147">Указывает, находится ли вызывающий абонент в сети Организации.</span><span class="sxs-lookup"><span data-stu-id="96bcf-147">Indicates whether or not the caller is inside the organization network.</span></span> <span data-ttu-id="96bcf-148">1 означает, что вызывающий абонент входит в корпоративную сеть.</span><span class="sxs-lookup"><span data-stu-id="96bcf-148">1 means that the caller is inside the enterprise network.</span></span> <span data-ttu-id="96bcf-149">0 означает, что вызывающий абонент находится за пределами сети.</span><span class="sxs-lookup"><span data-stu-id="96bcf-149">0 means that the caller is outside the network.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96bcf-150">CallerMacAddress</span><span class="sxs-lookup"><span data-stu-id="96bcf-150">CallerMacAddress</span></span></p></td>
<td><p><span data-ttu-id="96bcf-151">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="96bcf-151">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="96bcf-152">MAC-адрес сетевого интерфейса, используемого вызывающим абонентом.</span><span class="sxs-lookup"><span data-stu-id="96bcf-152">MAC address of network interface used by caller.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96bcf-153">CallerRelayIPAddr</span><span class="sxs-lookup"><span data-stu-id="96bcf-153">CallerRelayIPAddr</span></span></p></td>
<td><p><span data-ttu-id="96bcf-154">var (50)</span><span class="sxs-lookup"><span data-stu-id="96bcf-154">var(50)</span></span></p></td>
<td><p><span data-ttu-id="96bcf-155">IP-адрес службы EDGE (/V), используемой вызывающим абонентом.</span><span class="sxs-lookup"><span data-stu-id="96bcf-155">IP Address of the A/V Edge service used by the caller.</span></span> <span data-ttu-id="96bcf-156">Дополнительные сведения приведены в <a href="lync-server-2013-ipaddress-table.md">таблице IP-адрес в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="96bcf-156">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96bcf-157">CalleeRelayPort</span><span class="sxs-lookup"><span data-stu-id="96bcf-157">CalleeRelayPort</span></span></p></td>
<td><p><span data-ttu-id="96bcf-158">целое</span><span class="sxs-lookup"><span data-stu-id="96bcf-158">int</span></span></p></td>
<td><p><span data-ttu-id="96bcf-159">Порт, используемый в службе EDGE (A/V), используемой вызывающим абонентом.</span><span class="sxs-lookup"><span data-stu-id="96bcf-159">Port used on the A/V Edge service used by the caller.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96bcf-160">CallerReflexiveIPAddr</span><span class="sxs-lookup"><span data-stu-id="96bcf-160">CallerReflexiveIPAddr</span></span></p></td>
<td><p><span data-ttu-id="96bcf-161">var (50)</span><span class="sxs-lookup"><span data-stu-id="96bcf-161">var(50)</span></span></p></td>
<td><p><span data-ttu-id="96bcf-162">IP-адрес вызывающего абонента, предоставленный службой EDGE (A/V).</span><span class="sxs-lookup"><span data-stu-id="96bcf-162">Caller’s IP address as reported by the A/V Edge service.</span></span> <span data-ttu-id="96bcf-163">Этот адрес может отличаться от CallerIPAddr, если клиент находится за пределами NAT, например.</span><span class="sxs-lookup"><span data-stu-id="96bcf-163">This address may be different that the CallerIPAddr if the client is located behind a NAT for example.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96bcf-164">CallerCaptureDev</span><span class="sxs-lookup"><span data-stu-id="96bcf-164">CallerCaptureDev</span></span></p></td>
<td><p><span data-ttu-id="96bcf-165">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="96bcf-165">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="96bcf-166">Имя устройства захвата вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="96bcf-166">Caller’s capture device name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96bcf-167">CallerRenderDev</span><span class="sxs-lookup"><span data-stu-id="96bcf-167">CallerRenderDev</span></span></p></td>
<td><p><span data-ttu-id="96bcf-168">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="96bcf-168">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="96bcf-169">Имя устройства отрисовки вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="96bcf-169">Caller’s render device name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96bcf-170">CallerCaptureDevDriver</span><span class="sxs-lookup"><span data-stu-id="96bcf-170">CallerCaptureDevDriver</span></span></p></td>
<td><p><span data-ttu-id="96bcf-171">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="96bcf-171">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="96bcf-172">Имя драйвера устройства захвата вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="96bcf-172">Caller’s capture device driver name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96bcf-173">CallerRenderDevDriver</span><span class="sxs-lookup"><span data-stu-id="96bcf-173">CallerRenderDevDriver</span></span></p></td>
<td><p><span data-ttu-id="96bcf-174">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="96bcf-174">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="96bcf-175">Имя драйвера устройства отрисовки вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="96bcf-175">Caller’s render device driver name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96bcf-176">CallerWifiDriverDeviceDesc</span><span class="sxs-lookup"><span data-stu-id="96bcf-176">CallerWifiDriverDeviceDesc</span></span></p></td>
<td><p><span data-ttu-id="96bcf-177">varchar (256</span><span class="sxs-lookup"><span data-stu-id="96bcf-177">varchar(256</span></span></p></td>
<td><p><span data-ttu-id="96bcf-178">Описание драйвера Wi-Fi вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="96bcf-178">Caller’s Wifi driver description.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96bcf-179">CallerWifiDriverVersion</span><span class="sxs-lookup"><span data-stu-id="96bcf-179">CallerWifiDriverVersion</span></span></p></td>
<td><p><span data-ttu-id="96bcf-180">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="96bcf-180">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="96bcf-181">Версия драйвера Wi-Fi вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="96bcf-181">Caller’s Wifi driver version.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96bcf-182">CalleeNetworkConnectionDetail</span><span class="sxs-lookup"><span data-stu-id="96bcf-182">CalleeNetworkConnectionDetail</span></span></p></td>
<td><p><span data-ttu-id="96bcf-183">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="96bcf-183">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="96bcf-184">Сведения о сетевом подключении вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="96bcf-184">Details of caller’s network connection.</span></span> <span data-ttu-id="96bcf-185">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-networkconnectiondetail-table.md">таблицей NetworkConnectionDetail в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="96bcf-185">See the <a href="lync-server-2013-networkconnectiondetail-table.md">NetworkConnectionDetail table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96bcf-186">CallerBssid</span><span class="sxs-lookup"><span data-stu-id="96bcf-186">CallerBssid</span></span></p></td>
<td><p><span data-ttu-id="96bcf-187">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="96bcf-187">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="96bcf-188">Основной идентификатор набора служб, используемый вызывающими абонентами WiFi-связи.</span><span class="sxs-lookup"><span data-stu-id="96bcf-188">Basic Service Set Identifier used by callers WiFi connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96bcf-189">CallerVPN</span><span class="sxs-lookup"><span data-stu-id="96bcf-189">CallerVPN</span></span></p></td>
<td><p><span data-ttu-id="96bcf-190">бит</span><span class="sxs-lookup"><span data-stu-id="96bcf-190">bit</span></span></p></td>
<td><p><span data-ttu-id="96bcf-191">Указывает, подключен ли вызывающий абонент к виртуальной частной сети.</span><span class="sxs-lookup"><span data-stu-id="96bcf-191">Indicates whether the caller connected over a virtual private network.</span></span> <span data-ttu-id="96bcf-192">1 — это виртуальная частная сеть (VPN), а 0 — не VPN.</span><span class="sxs-lookup"><span data-stu-id="96bcf-192">1 is virtual private network (VPN), 0 is non-VPN.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96bcf-193">CalleeIPAddr</span><span class="sxs-lookup"><span data-stu-id="96bcf-193">CalleeIPAddr</span></span></p></td>
<td><p><span data-ttu-id="96bcf-194">var (50)</span><span class="sxs-lookup"><span data-stu-id="96bcf-194">var(50)</span></span></p></td>
<td><p><span data-ttu-id="96bcf-195">IP-адрес вызываемого абонента.</span><span class="sxs-lookup"><span data-stu-id="96bcf-195">IP address of the callee.</span></span> <span data-ttu-id="96bcf-196">Это может быть либо адрес IPv4, либо IPv6.</span><span class="sxs-lookup"><span data-stu-id="96bcf-196">This can be either an IPv4 or IPv6 address.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96bcf-197">CalleePort</span><span class="sxs-lookup"><span data-stu-id="96bcf-197">CalleePort</span></span></p></td>
<td><p><span data-ttu-id="96bcf-198">целое</span><span class="sxs-lookup"><span data-stu-id="96bcf-198">int</span></span></p></td>
<td><p><span data-ttu-id="96bcf-199">Порт, используемый вызываемым абонентом.</span><span class="sxs-lookup"><span data-stu-id="96bcf-199">Port used by the callee.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96bcf-200">CalleeInside</span><span class="sxs-lookup"><span data-stu-id="96bcf-200">CalleeInside</span></span></p></td>
<td><p><span data-ttu-id="96bcf-201">бит</span><span class="sxs-lookup"><span data-stu-id="96bcf-201">bit</span></span></p></td>
<td><p><span data-ttu-id="96bcf-202">Указывает, входит ли вызывающий объект в корпоративную сеть.</span><span class="sxs-lookup"><span data-stu-id="96bcf-202">Indicates whether the callee is inside the enterprise network.</span></span> <span data-ttu-id="96bcf-203">1 означает, что вызываемый абонент входит в корпоративную сеть, а 0 означает, что вызываемый объект находится за пределами сети.</span><span class="sxs-lookup"><span data-stu-id="96bcf-203">1 means callee is inside the enterprise network, 0 means the callee is outside the network.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96bcf-204">CalleeMacAddress</span><span class="sxs-lookup"><span data-stu-id="96bcf-204">CalleeMacAddress</span></span></p></td>
<td><p><span data-ttu-id="96bcf-205">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="96bcf-205">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="96bcf-206">MAC-адрес сетевого интерфейса, используемого вызываемым абонентом.</span><span class="sxs-lookup"><span data-stu-id="96bcf-206">MAC address of network interface used by callee.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96bcf-207">CalleeRelayIPAddr</span><span class="sxs-lookup"><span data-stu-id="96bcf-207">CalleeRelayIPAddr</span></span></p></td>
<td><p><span data-ttu-id="96bcf-208">var (50)</span><span class="sxs-lookup"><span data-stu-id="96bcf-208">var(50)</span></span></p></td>
<td><p><span data-ttu-id="96bcf-209">IP-адрес службы EDGE (/V), используемой вызываемым абонентом.</span><span class="sxs-lookup"><span data-stu-id="96bcf-209">IP Address of the A/V Edge service used by the callee.</span></span> <span data-ttu-id="96bcf-210">Дополнительные сведения приведены в <a href="lync-server-2013-ipaddress-table.md">таблице IP-адрес в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="96bcf-210">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96bcf-211">CalleeRelayPort</span><span class="sxs-lookup"><span data-stu-id="96bcf-211">CalleeRelayPort</span></span></p></td>
<td><p><span data-ttu-id="96bcf-212">целое</span><span class="sxs-lookup"><span data-stu-id="96bcf-212">int</span></span></p></td>
<td><p><span data-ttu-id="96bcf-213">Порт, используемый в службе EDGE (A/V), используемой вызываемым абонентом.</span><span class="sxs-lookup"><span data-stu-id="96bcf-213">Port used on the A/V Edge service used by the callee.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96bcf-214">CalleeReflexiveIPAddr</span><span class="sxs-lookup"><span data-stu-id="96bcf-214">CalleeReflexiveIPAddr</span></span></p></td>
<td><p><span data-ttu-id="96bcf-215">var (50)</span><span class="sxs-lookup"><span data-stu-id="96bcf-215">var(50)</span></span></p></td>
<td><p><span data-ttu-id="96bcf-216">IP-адрес вызываемого абонента, предоставленный службой Edge/V.</span><span class="sxs-lookup"><span data-stu-id="96bcf-216">Callee’s IP address as reported by the A/V Edge service.</span></span> <span data-ttu-id="96bcf-217">Этот адрес может отличаться от CalleeIPAddr, если клиент находится за пределами NAT, например.</span><span class="sxs-lookup"><span data-stu-id="96bcf-217">This address may be different that the CalleeIPAddr if the client is located behind a NAT for example.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96bcf-218">CalleeCaptureDev</span><span class="sxs-lookup"><span data-stu-id="96bcf-218">CalleeCaptureDev</span></span></p></td>
<td><p><span data-ttu-id="96bcf-219">var (50)</span><span class="sxs-lookup"><span data-stu-id="96bcf-219">var(50)</span></span></p></td>
<td><p><span data-ttu-id="96bcf-220">Имя устройства захвата абонента.</span><span class="sxs-lookup"><span data-stu-id="96bcf-220">Callee’s capture device name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96bcf-221">CalleeRenderDev</span><span class="sxs-lookup"><span data-stu-id="96bcf-221">CalleeRenderDev</span></span></p></td>
<td><p><span data-ttu-id="96bcf-222">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="96bcf-222">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="96bcf-223">Имя устройства отрисовки вызываемого абонента.</span><span class="sxs-lookup"><span data-stu-id="96bcf-223">Callee’s render device name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96bcf-224">CalleeCaptureDevDriver</span><span class="sxs-lookup"><span data-stu-id="96bcf-224">CalleeCaptureDevDriver</span></span></p></td>
<td><p><span data-ttu-id="96bcf-225">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="96bcf-225">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="96bcf-226">Имя драйвера устройства захвата абонента.</span><span class="sxs-lookup"><span data-stu-id="96bcf-226">Callee’s capture device driver name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96bcf-227">CalleeRenderDevDriver</span><span class="sxs-lookup"><span data-stu-id="96bcf-227">CalleeRenderDevDriver</span></span></p></td>
<td><p><span data-ttu-id="96bcf-228">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="96bcf-228">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="96bcf-229">Имя драйвера устройства обработки вызываемого абонента.</span><span class="sxs-lookup"><span data-stu-id="96bcf-229">Callee’s render device driver name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96bcf-230">CalleeWifiDriverDeviceDesc</span><span class="sxs-lookup"><span data-stu-id="96bcf-230">CalleeWifiDriverDeviceDesc</span></span></p></td>
<td><p><span data-ttu-id="96bcf-231">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="96bcf-231">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="96bcf-232">Описание драйвера WiFi вызываемого абонента.</span><span class="sxs-lookup"><span data-stu-id="96bcf-232">Callee’s Wifi driver description.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96bcf-233">CalleeWifiDriverVersion</span><span class="sxs-lookup"><span data-stu-id="96bcf-233">CalleeWifiDriverVersion</span></span></p></td>
<td><p><span data-ttu-id="96bcf-234">varchar (256</span><span class="sxs-lookup"><span data-stu-id="96bcf-234">varchar(256</span></span></p></td>
<td><p><span data-ttu-id="96bcf-235">Версия драйвера Wi-Fi для вызываемого абонента.</span><span class="sxs-lookup"><span data-stu-id="96bcf-235">Callee’s Wifi driver version.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96bcf-236">CalleeNetworkConnectionDetail</span><span class="sxs-lookup"><span data-stu-id="96bcf-236">CalleeNetworkConnectionDetail</span></span></p></td>
<td><p><span data-ttu-id="96bcf-237">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="96bcf-237">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="96bcf-238">Сведения о сетевом подключении для вызываемого абонента.</span><span class="sxs-lookup"><span data-stu-id="96bcf-238">Details of callee’s network connection.</span></span> <span data-ttu-id="96bcf-239">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-networkconnectiondetail-table.md">таблицей NetworkConnectionDetail в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="96bcf-239">See the <a href="lync-server-2013-networkconnectiondetail-table.md">NetworkConnectionDetail table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96bcf-240">CalleeBssid</span><span class="sxs-lookup"><span data-stu-id="96bcf-240">CalleeBssid</span></span></p></td>
<td><p><span data-ttu-id="96bcf-241">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="96bcf-241">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="96bcf-242">Основной идентификатор набора служб, используемый для подключений WiFi.</span><span class="sxs-lookup"><span data-stu-id="96bcf-242">Basic Service Set Identifier used by callee’s WiFi connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96bcf-243">CalleeVPN</span><span class="sxs-lookup"><span data-stu-id="96bcf-243">CalleeVPN</span></span></p></td>
<td><p><span data-ttu-id="96bcf-244">бит</span><span class="sxs-lookup"><span data-stu-id="96bcf-244">bit</span></span></p></td>
<td><p><span data-ttu-id="96bcf-245">Указывает, подсоединен ли вызывающий объект к виртуальной частной сети.</span><span class="sxs-lookup"><span data-stu-id="96bcf-245">Indicates whether the callee connected over a virtual private network.</span></span> <span data-ttu-id="96bcf-246">1 — это виртуальная частная сеть (VPN), а 0 — не VPN.</span><span class="sxs-lookup"><span data-stu-id="96bcf-246">1 is virtual private network (VPN), 0 is non-VPN.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96bcf-247">ConversationalMOS</span><span class="sxs-lookup"><span data-stu-id="96bcf-247">ConversationalMOS</span></span></p></td>
<td><p><span data-ttu-id="96bcf-248">десятичное число (3, 2)</span><span class="sxs-lookup"><span data-stu-id="96bcf-248">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="96bcf-249">Narrowband MOS из сеансов голосовой связи (на основе обоих звуковых потоков).</span><span class="sxs-lookup"><span data-stu-id="96bcf-249">Narrowband Conversational MOS of the audio sessions (based on both audio streams).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96bcf-250">AppliedBandwidthLimit</span><span class="sxs-lookup"><span data-stu-id="96bcf-250">AppliedBandwidthLimit</span></span></p></td>
<td><p><span data-ttu-id="96bcf-251">целое</span><span class="sxs-lookup"><span data-stu-id="96bcf-251">int</span></span></p></td>
<td><p><span data-ttu-id="96bcf-252">Это фактическая пропускная способность, примененная к потоку отправки на стороне, для которой заданы различные параметры политики (TURN, API, SDP, сервер политики и т. д.).</span><span class="sxs-lookup"><span data-stu-id="96bcf-252">This is the actual bandwidth applied to the given send side stream given various policy settings (TURN, API, SDP, Policy Server, etc.).</span></span> <span data-ttu-id="96bcf-253">Это не следует путать с эффективной пропускной способностью, так как в зависимости от оценки пропускной способности может снизиться эффективная пропускная способность.</span><span class="sxs-lookup"><span data-stu-id="96bcf-253">This should not to be confused with the effective bandwidth because there can be a lower effective bandwidth based on the bandwidth estimate.</span></span> <span data-ttu-id="96bcf-254">Это является, по сути, максимальной пропускной способностью потока отправки, который может занимать ограничения пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="96bcf-254">This is basically the maximum bandwidth the send stream can take barring limits imposed by the bandwidth estimate.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96bcf-255">AppliedBandwidthSource</span><span class="sxs-lookup"><span data-stu-id="96bcf-255">AppliedBandwidthSource</span></span></p></td>
<td><p><span data-ttu-id="96bcf-256">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="96bcf-256">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="96bcf-257">Источник ограничения пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="96bcf-257">Source of the bandwidth cap being imposed.</span></span> <span data-ttu-id="96bcf-258">Она описывает, откуда поступают ограничения пропускной способности (например, "сервер политики", "превратить сервер" или "модальность").</span><span class="sxs-lookup"><span data-stu-id="96bcf-258">It describes where the bandwidth limit is coming from (for example, “Policy Server”, “TURN Server”, or “Modality”).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96bcf-259">Вызывающая сторона</span><span class="sxs-lookup"><span data-stu-id="96bcf-259">Caller</span></span></p></td>
<td><p><span data-ttu-id="96bcf-260">бит</span><span class="sxs-lookup"><span data-stu-id="96bcf-260">bit</span></span></p></td>
<td><p><span data-ttu-id="96bcf-261">Указывает, получены ли метрики от вызывающего абонента; 1 — Да, 0 — нет.</span><span class="sxs-lookup"><span data-stu-id="96bcf-261">Indicates whether metrics from the caller were received; 1 is yes, 0 is no.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96bcf-262">Вызываемая сторона</span><span class="sxs-lookup"><span data-stu-id="96bcf-262">Callee</span></span></p></td>
<td><p><span data-ttu-id="96bcf-263">бит</span><span class="sxs-lookup"><span data-stu-id="96bcf-263">bit</span></span></p></td>
<td><p><span data-ttu-id="96bcf-264">Указывает, получены ли метрики от приемника вызова; 1 — Да, 0 — нет.</span><span class="sxs-lookup"><span data-stu-id="96bcf-264">Indicates whether metrics from the call receiver were received; 1 is yes, 0 is no.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96bcf-265">MidCallReport</span><span class="sxs-lookup"><span data-stu-id="96bcf-265">MidCallReport</span></span></p></td>
<td><p><span data-ttu-id="96bcf-266">бит</span><span class="sxs-lookup"><span data-stu-id="96bcf-266">bit</span></span></p></td>
<td><p><span data-ttu-id="96bcf-267">Указывает, является ли отчет частью звонка или полным звонком.</span><span class="sxs-lookup"><span data-stu-id="96bcf-267">Indicates whether the report is for a portion of the call or for the complete call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96bcf-268">ClassifiedPoorCall</span><span class="sxs-lookup"><span data-stu-id="96bcf-268">ClassifiedPoorCall</span></span></p></td>
<td><p><span data-ttu-id="96bcf-269">бит</span><span class="sxs-lookup"><span data-stu-id="96bcf-269">bit</span></span></p></td>
<td><p><span data-ttu-id="96bcf-270">Указывает, был ли звонок классифицирован как некачественный звонок (1) или как хороший звонок (0).</span><span class="sxs-lookup"><span data-stu-id="96bcf-270">Indicates whether a call was classified as a poor call (1) or as a good call (0).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96bcf-271">CallerConnectivityICE</span><span class="sxs-lookup"><span data-stu-id="96bcf-271">CallerConnectivityICE</span></span></p></td>
<td><p><span data-ttu-id="96bcf-272">tinyint</span><span class="sxs-lookup"><span data-stu-id="96bcf-272">tinyint</span></span></p></td>
<td><p><span data-ttu-id="96bcf-273">Указывает, подключен ли вызывающий абонент к сети с помощью протокола ICE (установление подключения к Интернету).</span><span class="sxs-lookup"><span data-stu-id="96bcf-273">Indicates whether the caller connected to the network using the ICE protocol (Internet Connectivity Establishment).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96bcf-274">CalleeConnectivityICE</span><span class="sxs-lookup"><span data-stu-id="96bcf-274">CalleeConnectivityICE</span></span></p></td>
<td><p><span data-ttu-id="96bcf-275">tinyint</span><span class="sxs-lookup"><span data-stu-id="96bcf-275">tinyint</span></span></p></td>
<td><p><span data-ttu-id="96bcf-276">Указывает, вызывает ли пользователь подключение к сети с помощью протокола ICE (установление подключения к Интернету).</span><span class="sxs-lookup"><span data-stu-id="96bcf-276">Indicates whether the user called connected to the network using the ICE protocol (Internet Connectivity Establishment).</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="96bcf-277">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="96bcf-277">


</div>

<span> </span>

</div>

</div>

</span></span></div>

