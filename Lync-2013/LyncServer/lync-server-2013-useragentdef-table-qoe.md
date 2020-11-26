---
title: 'Lync Server 2013: таблица UserAgentDef (QoE)'
description: 'Lync Server 2013: UserAgentDef Table (QoE).'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: UserAgentDef table (QoE)
ms:assetid: cfd8e3e0-4076-4162-9381-5276da8316d9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205259(v=OCS.15)
ms:contentKeyID: 48185394
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8546a33e607524b23755e9abf3edb2d5e2e417d7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439046"
---
# <a name="useragentdef-table-qoe-in-lync-server-2013"></a><span data-ttu-id="c9ae8-103">UserAgentDef Table (QoE) в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c9ae8-103">UserAgentDef table (QoE) in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c9ae8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c9ae8-104">

<span> </span></span></span>

<span data-ttu-id="c9ae8-105">_**Тема последнего изменения:** 2014-03-25_</span><span class="sxs-lookup"><span data-stu-id="c9ae8-105">_**Topic Last Modified:** 2014-03-25_</span></span>

<span data-ttu-id="c9ae8-106">В таблице UserAgentDef идентификаторы агентов пользователя сопоставлены с описательными именами агента.</span><span class="sxs-lookup"><span data-stu-id="c9ae8-106">The UserAgentDef table maps user agent identifiers to the agent’s descriptive names.</span></span> <span data-ttu-id="c9ae8-107">Агенты пользователей — это клиенты программного обеспечения, используемые для подключения к Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c9ae8-107">User agents are software clients used to connect to Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c9ae8-108">UAType</span><span class="sxs-lookup"><span data-stu-id="c9ae8-108">UAType</span></span></th>
<th><span data-ttu-id="c9ae8-109">UAName</span><span class="sxs-lookup"><span data-stu-id="c9ae8-109">UAName</span></span></th>
<th><span data-ttu-id="c9ae8-110">UACategory</span><span class="sxs-lookup"><span data-stu-id="c9ae8-110">UACategory</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c9ae8-111">1</span><span class="sxs-lookup"><span data-stu-id="c9ae8-111">1</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-112">MediationServer</span><span class="sxs-lookup"><span data-stu-id="c9ae8-112">MediationServer</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-113">MediationServer</span><span class="sxs-lookup"><span data-stu-id="c9ae8-113">MediationServer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9ae8-114">2</span><span class="sxs-lookup"><span data-stu-id="c9ae8-114">2</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-115">AV-MCU</span><span class="sxs-lookup"><span data-stu-id="c9ae8-115">AV-MCU</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-116">AV-MCU</span><span class="sxs-lookup"><span data-stu-id="c9ae8-116">AV-MCU</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9ae8-117">4</span><span class="sxs-lookup"><span data-stu-id="c9ae8-117">4</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-118">OC</span><span class="sxs-lookup"><span data-stu-id="c9ae8-118">OC</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-119">OC</span><span class="sxs-lookup"><span data-stu-id="c9ae8-119">OC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9ae8-120">No8</span><span class="sxs-lookup"><span data-stu-id="c9ae8-120">8</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-121">OCPhone</span><span class="sxs-lookup"><span data-stu-id="c9ae8-121">OCPhone</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-122">OCPhone</span><span class="sxs-lookup"><span data-stu-id="c9ae8-122">OCPhone</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9ae8-123">шестнадцат</span><span class="sxs-lookup"><span data-stu-id="c9ae8-123">16</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-124">LMC</span><span class="sxs-lookup"><span data-stu-id="c9ae8-124">LMC</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-125">LMC</span><span class="sxs-lookup"><span data-stu-id="c9ae8-125">LMC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9ae8-126">32</span><span class="sxs-lookup"><span data-stu-id="c9ae8-126">32</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-127">DVT</span><span class="sxs-lookup"><span data-stu-id="c9ae8-127">DVT</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-128">DVT</span><span class="sxs-lookup"><span data-stu-id="c9ae8-128">DVT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9ae8-129">64</span><span class="sxs-lookup"><span data-stu-id="c9ae8-129">64</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-130">ММ</span><span class="sxs-lookup"><span data-stu-id="c9ae8-130">MM</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-131">ММ</span><span class="sxs-lookup"><span data-stu-id="c9ae8-131">MM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9ae8-132">64</span><span class="sxs-lookup"><span data-stu-id="c9ae8-132">64</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-133">MC</span><span class="sxs-lookup"><span data-stu-id="c9ae8-133">MC</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-134">ММ</span><span class="sxs-lookup"><span data-stu-id="c9ae8-134">MM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9ae8-135">128</span><span class="sxs-lookup"><span data-stu-id="c9ae8-135">128</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-136">Attendant</span><span class="sxs-lookup"><span data-stu-id="c9ae8-136">Attendant</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-137">Attendant</span><span class="sxs-lookup"><span data-stu-id="c9ae8-137">Attendant</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9ae8-138">256</span><span class="sxs-lookup"><span data-stu-id="c9ae8-138">256</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-139">Conferencing_Announcement_Service_1.0</span><span class="sxs-lookup"><span data-stu-id="c9ae8-139">Conferencing_Announcement_Service_1.0</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-140">УСТАРЕВШ</span><span class="sxs-lookup"><span data-stu-id="c9ae8-140">CAS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9ae8-141">512</span><span class="sxs-lookup"><span data-stu-id="c9ae8-141">512</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-142">Conferencing_Attendant_1.0</span><span class="sxs-lookup"><span data-stu-id="c9ae8-142">Conferencing_Attendant_1.0</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-143">CAA</span><span class="sxs-lookup"><span data-stu-id="c9ae8-143">CAA</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9ae8-144">512</span><span class="sxs-lookup"><span data-stu-id="c9ae8-144">512</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-145">Conference_Auto_Attendant_1.0</span><span class="sxs-lookup"><span data-stu-id="c9ae8-145">Conference_Auto_Attendant_1.0</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-146">CAA</span><span class="sxs-lookup"><span data-stu-id="c9ae8-146">CAA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9ae8-147">1024</span><span class="sxs-lookup"><span data-stu-id="c9ae8-147">1024</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-148">Response_Group_Service</span><span class="sxs-lookup"><span data-stu-id="c9ae8-148">Response_Group_Service</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-149">ГРУППЫ ответа</span><span class="sxs-lookup"><span data-stu-id="c9ae8-149">RGS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9ae8-150">1032</span><span class="sxs-lookup"><span data-stu-id="c9ae8-150">1032</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-151">Call_Park_Service_1.0</span><span class="sxs-lookup"><span data-stu-id="c9ae8-151">Call_Park_Service_1.0</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-152">ПОДКЛЮЧЕНИЙ</span><span class="sxs-lookup"><span data-stu-id="c9ae8-152">CPS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9ae8-153">1040</span><span class="sxs-lookup"><span data-stu-id="c9ae8-153">1040</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-154">Response_Group_Service Announcement_Service</span><span class="sxs-lookup"><span data-stu-id="c9ae8-154">Response_Group_Service Announcement_Service</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-155">ФАЙЛА</span><span class="sxs-lookup"><span data-stu-id="c9ae8-155">AS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9ae8-156">2048</span><span class="sxs-lookup"><span data-stu-id="c9ae8-156">2048</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-157">Microsoft. RTC. Applications. CCS</span><span class="sxs-lookup"><span data-stu-id="c9ae8-157">Microsoft.Rtc.Applications.Ccs</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-158">СЕТЕВ</span><span class="sxs-lookup"><span data-stu-id="c9ae8-158">CCS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9ae8-159">16386</span><span class="sxs-lookup"><span data-stu-id="c9ae8-159">16386</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-160">CoMo</span><span class="sxs-lookup"><span data-stu-id="c9ae8-160">CoMo</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-161">CoMo</span><span class="sxs-lookup"><span data-stu-id="c9ae8-161">CoMo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9ae8-162">16387</span><span class="sxs-lookup"><span data-stu-id="c9ae8-162">16387</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-163">CWA</span><span class="sxs-lookup"><span data-stu-id="c9ae8-163">CWA</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-164">CWA</span><span class="sxs-lookup"><span data-stu-id="c9ae8-164">CWA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9ae8-165">16388</span><span class="sxs-lookup"><span data-stu-id="c9ae8-165">16388</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-166">InboundRouting</span><span class="sxs-lookup"><span data-stu-id="c9ae8-166">InboundRouting</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-167">InboundRouting</span><span class="sxs-lookup"><span data-stu-id="c9ae8-167">InboundRouting</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9ae8-168">16389</span><span class="sxs-lookup"><span data-stu-id="c9ae8-168">16389</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-169">ComoSvc</span><span class="sxs-lookup"><span data-stu-id="c9ae8-169">ComoSvc</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-170">ComoSvc</span><span class="sxs-lookup"><span data-stu-id="c9ae8-170">ComoSvc</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9ae8-171">16393</span><span class="sxs-lookup"><span data-stu-id="c9ae8-171">16393</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-172">MSExchangeUM</span><span class="sxs-lookup"><span data-stu-id="c9ae8-172">MSExchangeUM</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-173">ExUM</span><span class="sxs-lookup"><span data-stu-id="c9ae8-173">ExUM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9ae8-174">16395</span><span class="sxs-lookup"><span data-stu-id="c9ae8-174">16395</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-175">ArchivingAgent</span><span class="sxs-lookup"><span data-stu-id="c9ae8-175">ArchivingAgent</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-176">ARCHAGENT</span><span class="sxs-lookup"><span data-stu-id="c9ae8-176">ARCHAGENT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9ae8-177">16396</span><span class="sxs-lookup"><span data-stu-id="c9ae8-177">16396</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-178">ST</span><span class="sxs-lookup"><span data-stu-id="c9ae8-178">ST</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-179">ST</span><span class="sxs-lookup"><span data-stu-id="c9ae8-179">ST</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9ae8-180">16397</span><span class="sxs-lookup"><span data-stu-id="c9ae8-180">16397</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-181">applicationsharing</span><span class="sxs-lookup"><span data-stu-id="c9ae8-181">applicationsharing</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-182">ASMCU</span><span class="sxs-lookup"><span data-stu-id="c9ae8-182">ASMCU</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9ae8-183">16398</span><span class="sxs-lookup"><span data-stu-id="c9ae8-183">16398</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-184">WPLync</span><span class="sxs-lookup"><span data-stu-id="c9ae8-184">WPLync</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-185">WPLync</span><span class="sxs-lookup"><span data-stu-id="c9ae8-185">WPLync</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9ae8-186">16399</span><span class="sxs-lookup"><span data-stu-id="c9ae8-186">16399</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-187">iPhoneLync</span><span class="sxs-lookup"><span data-stu-id="c9ae8-187">iPhoneLync</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-188">iPhoneLync</span><span class="sxs-lookup"><span data-stu-id="c9ae8-188">iPhoneLync</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9ae8-189">16400</span><span class="sxs-lookup"><span data-stu-id="c9ae8-189">16400</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-190">AndroidLync</span><span class="sxs-lookup"><span data-stu-id="c9ae8-190">AndroidLync</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-191">AndroidLync</span><span class="sxs-lookup"><span data-stu-id="c9ae8-191">AndroidLync</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9ae8-192">16401</span><span class="sxs-lookup"><span data-stu-id="c9ae8-192">16401</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-193">iPadLync</span><span class="sxs-lookup"><span data-stu-id="c9ae8-193">iPadLync</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-194">iPadLync</span><span class="sxs-lookup"><span data-stu-id="c9ae8-194">iPadLync</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9ae8-195">16402</span><span class="sxs-lookup"><span data-stu-id="c9ae8-195">16402</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-196">NokiaLync</span><span class="sxs-lookup"><span data-stu-id="c9ae8-196">NokiaLync</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-197">NokiaLync</span><span class="sxs-lookup"><span data-stu-id="c9ae8-197">NokiaLync</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9ae8-198">16403</span><span class="sxs-lookup"><span data-stu-id="c9ae8-198">16403</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-199">LyncImm</span><span class="sxs-lookup"><span data-stu-id="c9ae8-199">LyncImm</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-200">LyncImm</span><span class="sxs-lookup"><span data-stu-id="c9ae8-200">LyncImm</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9ae8-201">16404</span><span class="sxs-lookup"><span data-stu-id="c9ae8-201">16404</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-202">КОМПЬЮТЕРАХ</span><span class="sxs-lookup"><span data-stu-id="c9ae8-202">PCS</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-203">КОМПЬЮТЕРАХ</span><span class="sxs-lookup"><span data-stu-id="c9ae8-203">PCS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9ae8-204">16405</span><span class="sxs-lookup"><span data-stu-id="c9ae8-204">16405</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-205">LWA</span><span class="sxs-lookup"><span data-stu-id="c9ae8-205">LWA</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-206">LWA</span><span class="sxs-lookup"><span data-stu-id="c9ae8-206">LWA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9ae8-207">16406</span><span class="sxs-lookup"><span data-stu-id="c9ae8-207">16406</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-208">Outlook</span><span class="sxs-lookup"><span data-stu-id="c9ae8-208">OWA</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-209">Outlook</span><span class="sxs-lookup"><span data-stu-id="c9ae8-209">OWA</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9ae8-210">16407</span><span class="sxs-lookup"><span data-stu-id="c9ae8-210">16407</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-211">AOC</span><span class="sxs-lookup"><span data-stu-id="c9ae8-211">AOC</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-212">AOC</span><span class="sxs-lookup"><span data-stu-id="c9ae8-212">AOC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9ae8-213">16408</span><span class="sxs-lookup"><span data-stu-id="c9ae8-213">16408</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-214">GCC</span><span class="sxs-lookup"><span data-stu-id="c9ae8-214">GCC</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-215">GCC</span><span class="sxs-lookup"><span data-stu-id="c9ae8-215">GCC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9ae8-216">16409</span><span class="sxs-lookup"><span data-stu-id="c9ae8-216">16409</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-217">IMMCU</span><span class="sxs-lookup"><span data-stu-id="c9ae8-217">IMMCU</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-218">IMMCU</span><span class="sxs-lookup"><span data-stu-id="c9ae8-218">IMMCU</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9ae8-219">16410</span><span class="sxs-lookup"><span data-stu-id="c9ae8-219">16410</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-220">XmppTGW</span><span class="sxs-lookup"><span data-stu-id="c9ae8-220">XmppTGW</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-221">XmppGateway</span><span class="sxs-lookup"><span data-stu-id="c9ae8-221">XmppGateway</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9ae8-222">32769</span><span class="sxs-lookup"><span data-stu-id="c9ae8-222">32769</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-223">Шлюз</span><span class="sxs-lookup"><span data-stu-id="c9ae8-223">Gateway</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-224">Шлюз</span><span class="sxs-lookup"><span data-stu-id="c9ae8-224">Gateway</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9ae8-225">32770</span><span class="sxs-lookup"><span data-stu-id="c9ae8-225">32770</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-226">GatewayMediationServerPair</span><span class="sxs-lookup"><span data-stu-id="c9ae8-226">GatewayMediationServerPair</span></span></p></td>
<td><p><span data-ttu-id="c9ae8-227">GatewayMediationServerPair</span><span class="sxs-lookup"><span data-stu-id="c9ae8-227">GatewayMediationServerPair</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="c9ae8-228">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c9ae8-228">


</div>

<span> </span>

</div>

</div>

</span></span></div>

