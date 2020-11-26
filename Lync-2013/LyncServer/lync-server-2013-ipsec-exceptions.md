---
title: Исключения для Lync Server 2013 IPsec
description: Исключения для Lync Server 2013 IPsec.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: IPsec exceptions
ms:assetid: 241f1eca-6f2f-44de-90b1-2cb659cbe27c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425719(v=OCS.15)
ms:contentKeyID: 48183627
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9b01264171592ec352b778e1aa7eee5861801991
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426727"
---
# <a name="ipsec-exceptions-in-lync-server-2013"></a><span data-ttu-id="08f6a-103">Исключения IPsec в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="08f6a-103">IPsec exceptions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="08f6a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="08f6a-104">

<span> </span></span></span>

<span data-ttu-id="08f6a-105">_**Тема последнего изменения:** 2012-06-27_</span><span class="sxs-lookup"><span data-stu-id="08f6a-105">_**Topic Last Modified:** 2012-06-27_</span></span>

<span data-ttu-id="08f6a-106">Для корпоративных сетей, где развернута безопасность протокола IP (IPsec) (ознакомьтесь со статьей IETF RFC 4301-4309), необходимо отключить IPsec для диапазона портов, используемых для доставки звуковых, видеофайлов и панорамных видео.</span><span class="sxs-lookup"><span data-stu-id="08f6a-106">For enterprise networks where Internet Protocol security (IPsec) (see IETF RFC 4301-4309) has been deployed, IPsec must be disabled over the range of ports used for the delivery of audio, video, and panorama video.</span></span> <span data-ttu-id="08f6a-107">Это связано с необходимостью избежать каких-либо задержек при распределении портов мультимедиа из-за согласования IPsec.</span><span class="sxs-lookup"><span data-stu-id="08f6a-107">The recommendation is motivated by the need to avoid any delay in the allocation of media ports due to IPsec negotiation.</span></span>

<span data-ttu-id="08f6a-108">В следующей таблице описаны рекомендуемые исключения IPsec.</span><span class="sxs-lookup"><span data-stu-id="08f6a-108">The following table explains the recommended IPsec exception settings.</span></span>

### <a name="recommended-ipsec-exceptions"></a><span data-ttu-id="08f6a-109">Рекомендуемые исключения IPsec</span><span class="sxs-lookup"><span data-stu-id="08f6a-109">Recommended IPsec Exceptions</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="08f6a-110">Имя правила</span><span class="sxs-lookup"><span data-stu-id="08f6a-110">Rule name</span></span></th>
<th><span data-ttu-id="08f6a-111">Исходный IP-адрес</span><span class="sxs-lookup"><span data-stu-id="08f6a-111">Source IP</span></span></th>
<th><span data-ttu-id="08f6a-112">Конечный IP-адрес</span><span class="sxs-lookup"><span data-stu-id="08f6a-112">Destination IP</span></span></th>
<th><span data-ttu-id="08f6a-113">Протокол</span><span class="sxs-lookup"><span data-stu-id="08f6a-113">Protocol</span></span></th>
<th><span data-ttu-id="08f6a-114">Исходный порт</span><span class="sxs-lookup"><span data-stu-id="08f6a-114">Source port</span></span></th>
<th><span data-ttu-id="08f6a-115">Конечный порт</span><span class="sxs-lookup"><span data-stu-id="08f6a-115">Destination port</span></span></th>
<th><span data-ttu-id="08f6a-116">Требование проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="08f6a-116">Authentication Requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="08f6a-117">Внутренние входящие данные пограничного сервера аудио- и видеоданных</span><span class="sxs-lookup"><span data-stu-id="08f6a-117">A/V Edge Server Internal Inbound</span></span></p></td>
<td><p><span data-ttu-id="08f6a-118">Любой</span><span class="sxs-lookup"><span data-stu-id="08f6a-118">Any</span></span></p></td>
<td><p><span data-ttu-id="08f6a-119">Внутренние данные пограничного сервера аудио- и видеоданных</span><span class="sxs-lookup"><span data-stu-id="08f6a-119">A/V Edge Server Internal</span></span></p></td>
<td><p><span data-ttu-id="08f6a-120">UDP и TCP</span><span class="sxs-lookup"><span data-stu-id="08f6a-120">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="08f6a-121">Любой</span><span class="sxs-lookup"><span data-stu-id="08f6a-121">Any</span></span></p></td>
<td><p><span data-ttu-id="08f6a-122">Любой</span><span class="sxs-lookup"><span data-stu-id="08f6a-122">Any</span></span></p></td>
<td><p><span data-ttu-id="08f6a-123">Не выполнять проверку подлинности</span><span class="sxs-lookup"><span data-stu-id="08f6a-123">Do not authenticate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08f6a-124">Внешние входящие данные пограничного сервера аудио- и видеоданных</span><span class="sxs-lookup"><span data-stu-id="08f6a-124">A/V Edge Server External Inbound</span></span></p></td>
<td><p><span data-ttu-id="08f6a-125">Любой</span><span class="sxs-lookup"><span data-stu-id="08f6a-125">Any</span></span></p></td>
<td><p><span data-ttu-id="08f6a-126">Внешние данные пограничного сервера аудио- и видеоданных</span><span class="sxs-lookup"><span data-stu-id="08f6a-126">A/V Edge Server External</span></span></p></td>
<td><p><span data-ttu-id="08f6a-127">UDP и TCP</span><span class="sxs-lookup"><span data-stu-id="08f6a-127">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="08f6a-128">Любой</span><span class="sxs-lookup"><span data-stu-id="08f6a-128">Any</span></span></p></td>
<td><p><span data-ttu-id="08f6a-129">Любой</span><span class="sxs-lookup"><span data-stu-id="08f6a-129">Any</span></span></p></td>
<td><p><span data-ttu-id="08f6a-130">Не выполнять проверку подлинности</span><span class="sxs-lookup"><span data-stu-id="08f6a-130">Do not authenticate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08f6a-131">Внутренние исходящие данные пограничного сервера аудио- и видеоданных</span><span class="sxs-lookup"><span data-stu-id="08f6a-131">A/V Edge Server Internal Outbound</span></span></p></td>
<td><p><span data-ttu-id="08f6a-132">Внутренние данные пограничного сервера аудио- и видеоданных</span><span class="sxs-lookup"><span data-stu-id="08f6a-132">A/V Edge Server Internal</span></span></p></td>
<td><p><span data-ttu-id="08f6a-133">Любой</span><span class="sxs-lookup"><span data-stu-id="08f6a-133">Any</span></span></p></td>
<td><p><span data-ttu-id="08f6a-134">UDP и TCP</span><span class="sxs-lookup"><span data-stu-id="08f6a-134">UDP &amp; TCP</span></span></p></td>
<td><p><span data-ttu-id="08f6a-135">Любой</span><span class="sxs-lookup"><span data-stu-id="08f6a-135">Any</span></span></p></td>
<td><p><span data-ttu-id="08f6a-136">Любой</span><span class="sxs-lookup"><span data-stu-id="08f6a-136">Any</span></span></p></td>
<td><p><span data-ttu-id="08f6a-137">Не выполнять проверку подлинности</span><span class="sxs-lookup"><span data-stu-id="08f6a-137">Do not authenticate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08f6a-138">Внешние исходящие данные пограничного сервера аудио- и видеоданных</span><span class="sxs-lookup"><span data-stu-id="08f6a-138">A/V Edge Server External Outbound</span></span></p></td>
<td><p><span data-ttu-id="08f6a-139">Внешние данные пограничного сервера аудио- и видеоданных</span><span class="sxs-lookup"><span data-stu-id="08f6a-139">A/V Edge Server External</span></span></p></td>
<td><p><span data-ttu-id="08f6a-140">Любой</span><span class="sxs-lookup"><span data-stu-id="08f6a-140">Any</span></span></p></td>
<td><p><span data-ttu-id="08f6a-141">UDP и TCP</span><span class="sxs-lookup"><span data-stu-id="08f6a-141">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="08f6a-142">Любой</span><span class="sxs-lookup"><span data-stu-id="08f6a-142">Any</span></span></p></td>
<td><p><span data-ttu-id="08f6a-143">Любой</span><span class="sxs-lookup"><span data-stu-id="08f6a-143">Any</span></span></p></td>
<td><p><span data-ttu-id="08f6a-144">Не выполнять проверку подлинности</span><span class="sxs-lookup"><span data-stu-id="08f6a-144">Do not authenticate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08f6a-145">Входящие данные сервера-посредника</span><span class="sxs-lookup"><span data-stu-id="08f6a-145">Mediation Server Inbound</span></span></p></td>
<td><p><span data-ttu-id="08f6a-146">Любой</span><span class="sxs-lookup"><span data-stu-id="08f6a-146">Any</span></span></p></td>
<td><p><span data-ttu-id="08f6a-147">Серверы-</span><span class="sxs-lookup"><span data-stu-id="08f6a-147">Mediation</span></span></p>
<p><span data-ttu-id="08f6a-148">посредники</span><span class="sxs-lookup"><span data-stu-id="08f6a-148">Server(s)</span></span></p></td>
<td><p><span data-ttu-id="08f6a-149">UDP и TCP</span><span class="sxs-lookup"><span data-stu-id="08f6a-149">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="08f6a-150">Любой</span><span class="sxs-lookup"><span data-stu-id="08f6a-150">Any</span></span></p></td>
<td><p><span data-ttu-id="08f6a-151">Любой</span><span class="sxs-lookup"><span data-stu-id="08f6a-151">Any</span></span></p></td>
<td><p><span data-ttu-id="08f6a-152">Не выполнять проверку подлинности</span><span class="sxs-lookup"><span data-stu-id="08f6a-152">Do not authenticate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08f6a-153">Исходящие данные сервера-посредника</span><span class="sxs-lookup"><span data-stu-id="08f6a-153">Mediation Server Outbound</span></span></p></td>
<td><p><span data-ttu-id="08f6a-154">Серверы-</span><span class="sxs-lookup"><span data-stu-id="08f6a-154">Mediation</span></span></p>
<p><span data-ttu-id="08f6a-155">посредники</span><span class="sxs-lookup"><span data-stu-id="08f6a-155">Server(s)</span></span></p></td>
<td><p><span data-ttu-id="08f6a-156">Любой</span><span class="sxs-lookup"><span data-stu-id="08f6a-156">Any</span></span></p></td>
<td><p><span data-ttu-id="08f6a-157">UDP и TCP</span><span class="sxs-lookup"><span data-stu-id="08f6a-157">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="08f6a-158">Любой</span><span class="sxs-lookup"><span data-stu-id="08f6a-158">Any</span></span></p></td>
<td><p><span data-ttu-id="08f6a-159">Любой</span><span class="sxs-lookup"><span data-stu-id="08f6a-159">Any</span></span></p></td>
<td><p><span data-ttu-id="08f6a-160">Не выполнять проверку подлинности</span><span class="sxs-lookup"><span data-stu-id="08f6a-160">Do not authenticate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08f6a-161">Входящие данные помощника по конференц-связи</span><span class="sxs-lookup"><span data-stu-id="08f6a-161">Conferencing Attendant Inbound</span></span></p></td>
<td><p><span data-ttu-id="08f6a-162">Любой</span><span class="sxs-lookup"><span data-stu-id="08f6a-162">Any</span></span></p></td>
<td><p><span data-ttu-id="08f6a-163">Сервер переднего плана с помощником по конференц-связи</span><span class="sxs-lookup"><span data-stu-id="08f6a-163">Front End Server running Conferencing Attendant</span></span></p></td>
<td><p><span data-ttu-id="08f6a-164">UDP и TCP</span><span class="sxs-lookup"><span data-stu-id="08f6a-164">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="08f6a-165">Любой</span><span class="sxs-lookup"><span data-stu-id="08f6a-165">Any</span></span></p></td>
<td><p><span data-ttu-id="08f6a-166">Любой</span><span class="sxs-lookup"><span data-stu-id="08f6a-166">Any</span></span></p></td>
<td><p><span data-ttu-id="08f6a-167">Не выполнять проверку подлинности</span><span class="sxs-lookup"><span data-stu-id="08f6a-167">Do not authenticate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08f6a-168">Исходящие данные помощника по конференц-связи</span><span class="sxs-lookup"><span data-stu-id="08f6a-168">Conferencing Attendant Outbound</span></span></p></td>
<td><p><span data-ttu-id="08f6a-169">Сервер переднего плана с помощником по конференц-связи</span><span class="sxs-lookup"><span data-stu-id="08f6a-169">Front End Server running Conferencing Attendant</span></span></p></td>
<td><p><span data-ttu-id="08f6a-170">Любой</span><span class="sxs-lookup"><span data-stu-id="08f6a-170">Any</span></span></p></td>
<td><p><span data-ttu-id="08f6a-171">UDP и TCP</span><span class="sxs-lookup"><span data-stu-id="08f6a-171">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="08f6a-172">Любой</span><span class="sxs-lookup"><span data-stu-id="08f6a-172">Any</span></span></p></td>
<td><p><span data-ttu-id="08f6a-173">Любой</span><span class="sxs-lookup"><span data-stu-id="08f6a-173">Any</span></span></p></td>
<td><p><span data-ttu-id="08f6a-174">Не выполнять проверку подлинности</span><span class="sxs-lookup"><span data-stu-id="08f6a-174">Do not authenticate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08f6a-175">Входящие данные аудио- и видеоконференций</span><span class="sxs-lookup"><span data-stu-id="08f6a-175">A/V Conferencing Inbound</span></span></p></td>
<td><p><span data-ttu-id="08f6a-176">Любой</span><span class="sxs-lookup"><span data-stu-id="08f6a-176">Any</span></span></p></td>
<td><p><span data-ttu-id="08f6a-177">Серверы переднего плана</span><span class="sxs-lookup"><span data-stu-id="08f6a-177">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="08f6a-178">UDP и TCP</span><span class="sxs-lookup"><span data-stu-id="08f6a-178">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="08f6a-179">Любой</span><span class="sxs-lookup"><span data-stu-id="08f6a-179">Any</span></span></p></td>
<td><p><span data-ttu-id="08f6a-180">Любой</span><span class="sxs-lookup"><span data-stu-id="08f6a-180">Any</span></span></p></td>
<td><p><span data-ttu-id="08f6a-181">Не выполнять проверку подлинности</span><span class="sxs-lookup"><span data-stu-id="08f6a-181">Do not authenticate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08f6a-182">Исходящие данные аудио- и видеоконференций</span><span class="sxs-lookup"><span data-stu-id="08f6a-182">A/V Conferencing Outbound</span></span></p></td>
<td><p><span data-ttu-id="08f6a-183">Серверы переднего плана</span><span class="sxs-lookup"><span data-stu-id="08f6a-183">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="08f6a-184">Любой</span><span class="sxs-lookup"><span data-stu-id="08f6a-184">Any</span></span></p></td>
<td><p><span data-ttu-id="08f6a-185">UDP и TCP</span><span class="sxs-lookup"><span data-stu-id="08f6a-185">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="08f6a-186">Любой</span><span class="sxs-lookup"><span data-stu-id="08f6a-186">Any</span></span></p></td>
<td><p><span data-ttu-id="08f6a-187">Любой</span><span class="sxs-lookup"><span data-stu-id="08f6a-187">Any</span></span></p></td>
<td><p><span data-ttu-id="08f6a-188">Не выполнять проверку подлинности</span><span class="sxs-lookup"><span data-stu-id="08f6a-188">Do not authenticate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08f6a-189">Входящие данные Exchange</span><span class="sxs-lookup"><span data-stu-id="08f6a-189">Exchange Inbound</span></span></p></td>
<td><p><span data-ttu-id="08f6a-190">Любой</span><span class="sxs-lookup"><span data-stu-id="08f6a-190">Any</span></span></p></td>
<td><p><span data-ttu-id="08f6a-191">Единая система обмена сообщениями Exchange</span><span class="sxs-lookup"><span data-stu-id="08f6a-191">Exchange Unified Messaging</span></span></p></td>
<td><p><span data-ttu-id="08f6a-192">UDP и TCP</span><span class="sxs-lookup"><span data-stu-id="08f6a-192">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="08f6a-193">Любой</span><span class="sxs-lookup"><span data-stu-id="08f6a-193">Any</span></span></p></td>
<td><p><span data-ttu-id="08f6a-194">Любой</span><span class="sxs-lookup"><span data-stu-id="08f6a-194">Any</span></span></p></td>
<td><p><span data-ttu-id="08f6a-195">Не выполнять проверку подлинности</span><span class="sxs-lookup"><span data-stu-id="08f6a-195">Do not authenticate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08f6a-196">Входящие данные серверов совместного использования приложений</span><span class="sxs-lookup"><span data-stu-id="08f6a-196">Application Sharing Servers Inbound</span></span></p></td>
<td><p><span data-ttu-id="08f6a-197">Любой</span><span class="sxs-lookup"><span data-stu-id="08f6a-197">Any</span></span></p></td>
<td><p><span data-ttu-id="08f6a-198">Серверы совместного использования приложений</span><span class="sxs-lookup"><span data-stu-id="08f6a-198">Application Sharing Servers</span></span></p></td>
<td><p><span data-ttu-id="08f6a-199">TCP</span><span class="sxs-lookup"><span data-stu-id="08f6a-199">TCP</span></span></p></td>
<td><p><span data-ttu-id="08f6a-200">Любой</span><span class="sxs-lookup"><span data-stu-id="08f6a-200">Any</span></span></p></td>
<td><p><span data-ttu-id="08f6a-201">Любой</span><span class="sxs-lookup"><span data-stu-id="08f6a-201">Any</span></span></p></td>
<td><p><span data-ttu-id="08f6a-202">Не выполнять проверку подлинности</span><span class="sxs-lookup"><span data-stu-id="08f6a-202">Do not authenticate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08f6a-203">Исходящие данные серверов совместного использования приложений</span><span class="sxs-lookup"><span data-stu-id="08f6a-203">Application Sharing Server Outbound</span></span></p></td>
<td><p><span data-ttu-id="08f6a-204">Серверы совместного использования приложений</span><span class="sxs-lookup"><span data-stu-id="08f6a-204">Application Sharing Servers</span></span></p></td>
<td><p><span data-ttu-id="08f6a-205">Любой</span><span class="sxs-lookup"><span data-stu-id="08f6a-205">Any</span></span></p></td>
<td><p><span data-ttu-id="08f6a-206">TCP</span><span class="sxs-lookup"><span data-stu-id="08f6a-206">TCP</span></span></p></td>
<td><p><span data-ttu-id="08f6a-207">Любой</span><span class="sxs-lookup"><span data-stu-id="08f6a-207">Any</span></span></p></td>
<td><p><span data-ttu-id="08f6a-208">Любой</span><span class="sxs-lookup"><span data-stu-id="08f6a-208">Any</span></span></p></td>
<td><p><span data-ttu-id="08f6a-209">Не выполнять проверку подлинности</span><span class="sxs-lookup"><span data-stu-id="08f6a-209">Do not authenticate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08f6a-210">Исходящие данные Exchange</span><span class="sxs-lookup"><span data-stu-id="08f6a-210">Exchange Outbound</span></span></p></td>
<td><p><span data-ttu-id="08f6a-211">Единая система обмена сообщениями Exchange</span><span class="sxs-lookup"><span data-stu-id="08f6a-211">Exchange Unified Messaging</span></span></p></td>
<td><p><span data-ttu-id="08f6a-212">Любой</span><span class="sxs-lookup"><span data-stu-id="08f6a-212">Any</span></span></p></td>
<td><p><span data-ttu-id="08f6a-213">UDP и TCP</span><span class="sxs-lookup"><span data-stu-id="08f6a-213">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="08f6a-214">Любой</span><span class="sxs-lookup"><span data-stu-id="08f6a-214">Any</span></span></p></td>
<td><p><span data-ttu-id="08f6a-215">Любой</span><span class="sxs-lookup"><span data-stu-id="08f6a-215">Any</span></span></p></td>
<td><p><span data-ttu-id="08f6a-216">Не выполнять проверку подлинности</span><span class="sxs-lookup"><span data-stu-id="08f6a-216">Do not authenticate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08f6a-217">Клиенты</span><span class="sxs-lookup"><span data-stu-id="08f6a-217">Clients</span></span></p></td>
<td><p><span data-ttu-id="08f6a-218">Любой</span><span class="sxs-lookup"><span data-stu-id="08f6a-218">Any</span></span></p></td>
<td><p><span data-ttu-id="08f6a-219">Любой</span><span class="sxs-lookup"><span data-stu-id="08f6a-219">Any</span></span></p></td>
<td><p><span data-ttu-id="08f6a-220">UDP</span><span class="sxs-lookup"><span data-stu-id="08f6a-220">UDP</span></span></p></td>
<td><p><span data-ttu-id="08f6a-221">Указанный диапазон портов мультимедиа</span><span class="sxs-lookup"><span data-stu-id="08f6a-221">Specified media port range</span></span></p></td>
<td><p><span data-ttu-id="08f6a-222">Любой</span><span class="sxs-lookup"><span data-stu-id="08f6a-222">Any</span></span></p></td>
<td><p><span data-ttu-id="08f6a-223">Не выполнять проверку подлинности</span><span class="sxs-lookup"><span data-stu-id="08f6a-223">Do not authenticate</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="08f6a-224">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="08f6a-224">


</div>

<span> </span>

</div>

</div>

</span></span></div>

