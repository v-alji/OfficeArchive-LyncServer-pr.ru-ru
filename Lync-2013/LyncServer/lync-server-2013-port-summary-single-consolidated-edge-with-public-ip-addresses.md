---
title: Сводка по портам — единая консолидированная пограничная топология с общедоступными IP-адресами
description: Общие сведения о портах — одинарный консолидированный край с общедоступными IP-адресами.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - Single consolidated edge with public IP addresses
ms:assetid: 28407acc-8b92-4f78-875c-fd6b4323b602
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204756(v=OCS.15)
ms:contentKeyID: 48183685
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 82ab2d89404fb174994d8e5b798f64bb68768326
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424262"
---
# <a name="port-summary---single-consolidated-edge-with-public-ip-addresses-in-lync-server-2013"></a><span data-ttu-id="80189-103">Сводка по портам — единая консолидированная пограничная топология с общедоступными IP-адресами в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="80189-103">Port summary - Single consolidated edge with public IP addresses in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="80189-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="80189-104">

<span> </span></span></span>

<span data-ttu-id="80189-105">_**Тема последнего изменения:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="80189-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="80189-106">Функция пограничного сервера Lync Server 2013, описанная в этой архитектуре сценариев, очень похожа на ту, что была реализована в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="80189-106">The Lync Server 2013, Edge Server functionality described in this scenario architecture is very similar to what was implemented in Lync Server 2010.</span></span> <span data-ttu-id="80189-107">Наиболее заметным дополнением является порт **5269 на TCP** для протокола расширенной обработки сообщений и присутствия (XMPP).</span><span class="sxs-lookup"><span data-stu-id="80189-107">The most noticeable addition is the port **5269 over TCP** entry for the extensible messaging and presence protocol (XMPP).</span></span> <span data-ttu-id="80189-108">Lync Server 2013 (при необходимости) можно развернуть прокси-сервер XMPP на пограничном или пограничном пуле, а также на сервере шлюзов XMPP на сервере переднего плана или в пуле внешних интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="80189-108">Lync Server 2013 optionally deploys an XMPP proxy on the Edge Server or Edge pool and the XMPP gateway server on the Front End Server or Front End pool.</span></span> <span data-ttu-id="80189-109">Сведения о планировании для обратного прокси-сервера и Федерации находятся в [сценариях обратного прокси-сервера в Lync server 2013](lync-server-2013-scenarios-for-reverse-proxy.md) и [планировании SIP, XMPP Federation и общедоступных мгновенных сообщений в разделах Lync Server 2013](lync-server-2013-planning-for-sip-xmpp-federation-and-public-instant-messaging.md) соответственно.</span><span class="sxs-lookup"><span data-stu-id="80189-109">Planning information for the reverse proxy and federation are found in [Scenarios for reverse proxy in Lync Server 2013](lync-server-2013-scenarios-for-reverse-proxy.md) and [Planning for SIP, XMPP federation, and public instant messaging in Lync Server 2013](lync-server-2013-planning-for-sip-xmpp-federation-and-public-instant-messaging.md) sections, respectively.</span></span>

<span data-ttu-id="80189-110">В дополнение к протоколу IPv4, пограничный сервер теперь поддерживает IPv6.</span><span class="sxs-lookup"><span data-stu-id="80189-110">In addition to IPv4, the Edge Server now supports IPv6.</span></span> <span data-ttu-id="80189-111">Для ясности в сценариях используется только протокол IPv4.</span><span class="sxs-lookup"><span data-stu-id="80189-111">For clarity, only IPv4 is used in the scenarios.</span></span>

<span data-ttu-id="80189-112">**Корпоративная сеть периметра для единого консолидированного края с общедоступными IP-адресами**</span><span class="sxs-lookup"><span data-stu-id="80189-112">**Enterprise perimeter network for single consolidated edge with public IP addressing**</span></span>

<span data-ttu-id="80189-113">![f8c144c5-e5fb-498a-823e-eb39f26b6847](images/Gg425891.f8c144c5-e5fb-498a-823e-eb39f26b6847(OCS.15).jpg "f8c144c5-e5fb-498a-823e-eb39f26b6847")</span><span class="sxs-lookup"><span data-stu-id="80189-113">![f8c144c5-e5fb-498a-823e-eb39f26b6847](images/Gg425891.f8c144c5-e5fb-498a-823e-eb39f26b6847(OCS.15).jpg "f8c144c5-e5fb-498a-823e-eb39f26b6847")</span></span>

<div>

## <a name="port-and-protocol-details"></a><span data-ttu-id="80189-114">Сведения о портах и протоколах</span><span class="sxs-lookup"><span data-stu-id="80189-114">Port and Protocol Details</span></span>

<span data-ttu-id="80189-115">Мы рекомендуем открывать только порты, необходимые для поддержки функций, для которых предоставляется внешний доступ.</span><span class="sxs-lookup"><span data-stu-id="80189-115">We recommend that you open only the ports required to support the functionality for which you are providing external access.</span></span>

<span data-ttu-id="80189-116">Для удаленного доступа к работе в любой службе пограничного сервера необходимо, чтобы трафик SIP был разрешен по двунаправленному потоку, как показано на рисунке входящего и исходящего трафика пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="80189-116">For remote access to work for any edge service, it is mandatory that SIP traffic is allowed to flow bidirectionally as shown in the Inbound/Outbound edge traffic figure.</span></span> <span data-ttu-id="80189-117">Другими словами, Обмен сообщениями SIP и из службы Edge для Access осуществляется в обмене мгновенными сообщениями, присутствии, веб-конференциях, аудио-и видеосвязи (A/V) и Федерации.</span><span class="sxs-lookup"><span data-stu-id="80189-117">Stated another way, the SIP messaging to and from the Access Edge service is involved in instant messaging (IM), presence, web conferencing, audio/video (A/V) and federation.</span></span>

### <a name="firewall-summary-for-single-consolidated-edge-with-public-ip-addresses-external-interface"></a><span data-ttu-id="80189-118">Сводка по межсетевому экрану единого консолидированного края с общедоступными IP-адресами: внешний интерфейс</span><span class="sxs-lookup"><span data-stu-id="80189-118">Firewall Summary for Single Consolidated Edge with Public IP Addresses: External Interface</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="80189-119">Role/Protocol/TCP/UDP/порт</span><span class="sxs-lookup"><span data-stu-id="80189-119">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="80189-120">IP-адрес источника</span><span class="sxs-lookup"><span data-stu-id="80189-120">Source IP address</span></span></th>
<th><span data-ttu-id="80189-121">IP-адрес назначения</span><span class="sxs-lookup"><span data-stu-id="80189-121">Destination IP address</span></span></th>
<th><span data-ttu-id="80189-122">Примечания.</span><span class="sxs-lookup"><span data-stu-id="80189-122">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="80189-123">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="80189-123">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="80189-124">Любой</span><span class="sxs-lookup"><span data-stu-id="80189-124">Any</span></span></p></td>
<td><p><span data-ttu-id="80189-125">Прокси-служба XMPP (доступ к IP-адресу для общих ресурсов с помощью службы Edge Access)</span><span class="sxs-lookup"><span data-stu-id="80189-125">XMPP Proxy service (shares IP address with Access Edge service)</span></span></p></td>
<td><p><span data-ttu-id="80189-126">Прокси-служба XMPP принимает трафик от XMPP контактов в определенных XMPP федерациях.</span><span class="sxs-lookup"><span data-stu-id="80189-126">XMPP Proxy service accepts traffic from XMPP contacts in defined XMPP federations</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80189-127">Access/HTTP/TCP/80</span><span class="sxs-lookup"><span data-stu-id="80189-127">Access/HTTP/TCP/80</span></span></p></td>
<td><p><span data-ttu-id="80189-128">Пограничный сервер, общедоступный IP-адрес пограничной службы доступа</span><span class="sxs-lookup"><span data-stu-id="80189-128">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="80189-129">Любой</span><span class="sxs-lookup"><span data-stu-id="80189-129">Any</span></span></p></td>
<td><p><span data-ttu-id="80189-130">Проверка отзыва сертификатов и получения CRL</span><span class="sxs-lookup"><span data-stu-id="80189-130">Certificate revocation/CRL check and retrieval</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80189-131">Access/DNS/TCP/53</span><span class="sxs-lookup"><span data-stu-id="80189-131">Access/DNS/TCP/53</span></span></p></td>
<td><p><span data-ttu-id="80189-132">Пограничный сервер, общедоступный IP-адрес пограничной службы доступа</span><span class="sxs-lookup"><span data-stu-id="80189-132">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="80189-133">Любой</span><span class="sxs-lookup"><span data-stu-id="80189-133">Any</span></span></p></td>
<td><p><span data-ttu-id="80189-134">Запрос DNS по протоколу TCP</span><span class="sxs-lookup"><span data-stu-id="80189-134">DNS query over TCP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80189-135">Access/DNS/UDP/53</span><span class="sxs-lookup"><span data-stu-id="80189-135">Access/DNS/UDP/53</span></span></p></td>
<td><p><span data-ttu-id="80189-136">Пограничный сервер, общедоступный IP-адрес пограничной службы доступа</span><span class="sxs-lookup"><span data-stu-id="80189-136">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="80189-137">Любой</span><span class="sxs-lookup"><span data-stu-id="80189-137">Any</span></span></p></td>
<td><p><span data-ttu-id="80189-138">Запрос DNS по протоколу UDP</span><span class="sxs-lookup"><span data-stu-id="80189-138">DNS query over UDP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80189-139">Access/SIP (TLS)/TCP/443</span><span class="sxs-lookup"><span data-stu-id="80189-139">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="80189-140">Любой</span><span class="sxs-lookup"><span data-stu-id="80189-140">Any</span></span></p></td>
<td><p><span data-ttu-id="80189-141">Пограничный сервер, общедоступный IP-адрес пограничной службы доступа</span><span class="sxs-lookup"><span data-stu-id="80189-141">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="80189-142">Трафик SIP "клиент-сервер" для доступа внешних пользователей</span><span class="sxs-lookup"><span data-stu-id="80189-142">Client-to-server SIP traffic for external user access</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80189-143">Access/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="80189-143">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="80189-144">Любой</span><span class="sxs-lookup"><span data-stu-id="80189-144">Any</span></span></p></td>
<td><p><span data-ttu-id="80189-145">Пограничный сервер, общедоступный IP-адрес пограничной службы доступа</span><span class="sxs-lookup"><span data-stu-id="80189-145">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="80189-146">Для Федеративной и общедоступной службы обмена мгновенными сообщениями с помощью SIP</span><span class="sxs-lookup"><span data-stu-id="80189-146">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80189-147">Access/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="80189-147">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="80189-148">Пограничный сервер, общедоступный IP-адрес пограничной службы доступа</span><span class="sxs-lookup"><span data-stu-id="80189-148">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="80189-149">Любой</span><span class="sxs-lookup"><span data-stu-id="80189-149">Any</span></span></p></td>
<td><p><span data-ttu-id="80189-150">Для Федеративной и общедоступной службы обмена мгновенными сообщениями с помощью SIP</span><span class="sxs-lookup"><span data-stu-id="80189-150">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80189-151">Веб-конференции/PSOM (TLS)/TCP/443</span><span class="sxs-lookup"><span data-stu-id="80189-151">Web Conferencing/PSOM(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="80189-152">Любой</span><span class="sxs-lookup"><span data-stu-id="80189-152">Any</span></span></p></td>
<td><p><span data-ttu-id="80189-153">Общедоступный IP-адрес службы пограничного сервера для веб-конференций Edge</span><span class="sxs-lookup"><span data-stu-id="80189-153">Edge Server Web Conferencing Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="80189-154">Мультимедиа для веб-конференций</span><span class="sxs-lookup"><span data-stu-id="80189-154">Web Conferencing media</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80189-155">A/V/RTP/TCP/50000-59,999</span><span class="sxs-lookup"><span data-stu-id="80189-155">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="80189-156">Пограничный сервер, общедоступный IP-адрес пограничной службы доступа</span><span class="sxs-lookup"><span data-stu-id="80189-156">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="80189-157">Любой</span><span class="sxs-lookup"><span data-stu-id="80189-157">Any</span></span></p></td>
<td><p><span data-ttu-id="80189-158">Требуется для Федерации с партнерами, работающими под управлением Office Communications Server 2007, Office Communications Server 2007 R2, Lync Server 2010 и Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="80189-158">Required for federating with partners running Office Communications Server 2007, Office Communications Server 2007 R2, Lync Server 2010 and Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80189-159">A/V/RTP/UDP/50000-59,999</span><span class="sxs-lookup"><span data-stu-id="80189-159">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="80189-160">Пограничный сервер, общедоступный IP-адрес пограничной службы аудио- и видеоданных</span><span class="sxs-lookup"><span data-stu-id="80189-160">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="80189-161">Любой</span><span class="sxs-lookup"><span data-stu-id="80189-161">Any</span></span></p></td>
<td><p><span data-ttu-id="80189-162">Требуется только для Федерации с партнерами, работающими под управлением Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="80189-162">Required only for federation with partners running Office Communications Server 2007</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80189-163">A/V/RTP/TCP/50000-59,999</span><span class="sxs-lookup"><span data-stu-id="80189-163">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="80189-164">Любой</span><span class="sxs-lookup"><span data-stu-id="80189-164">Any</span></span></p></td>
<td><p><span data-ttu-id="80189-165">Пограничный сервер, общедоступный IP-адрес пограничной службы аудио- и видеоданных</span><span class="sxs-lookup"><span data-stu-id="80189-165">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="80189-166">Требуется только для Федерации с партнерами, работающими под управлением Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="80189-166">Required only for federation with partners running Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80189-167">A/V/RTP/UDP/50000-59,999</span><span class="sxs-lookup"><span data-stu-id="80189-167">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="80189-168">Любой</span><span class="sxs-lookup"><span data-stu-id="80189-168">Any</span></span></p></td>
<td><p><span data-ttu-id="80189-169">Пограничный сервер, общедоступный IP-адрес пограничной службы аудио- и видеоданных</span><span class="sxs-lookup"><span data-stu-id="80189-169">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="80189-170">Требуется только для Федерации с партнерами, работающими под управлением Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="80189-170">Required only for federation with partners running Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80189-171">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="80189-171">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="80189-172">Пограничный сервер, общедоступный IP-адрес пограничной службы аудио- и видеоданных</span><span class="sxs-lookup"><span data-stu-id="80189-172">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="80189-173">Любой</span><span class="sxs-lookup"><span data-stu-id="80189-173">Any</span></span></p></td>
<td><p><span data-ttu-id="80189-174">3478 Outbound используется для определения версии пограничного сервера, с которым обменивается данными Lync Server, а также для мультимедийного трафика от пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="80189-174">3478 outbound is used to determine the version of Edge Server that Lync Server is communicating with and also for media traffic from Edge Server-to-Edge Server.</span></span> <span data-ttu-id="80189-175">Требуется для Федерации с Lync Server 2010, Windows Live Messenger и Office Communications Server 2007 R2, а также в том случае, если в компании развернуты несколько пулов Edge.</span><span class="sxs-lookup"><span data-stu-id="80189-175">Required for federation with Lync Server 2010, Windows Live Messenger, and Office Communications Server 2007 R2, and also if multiple Edge pools are deployed within a company.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80189-176">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="80189-176">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="80189-177">Любой</span><span class="sxs-lookup"><span data-stu-id="80189-177">Any</span></span></p></td>
<td><p><span data-ttu-id="80189-178">Пограничный сервер, общедоступный IP-адрес пограничной службы аудио- и видеоданных</span><span class="sxs-lookup"><span data-stu-id="80189-178">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="80189-179">STUN/отключите согласование кандидатов по протоколу UDP/3478</span><span class="sxs-lookup"><span data-stu-id="80189-179">STUN/TURN negotiation of candidates over UDP/3478</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80189-180">A/V/STUN, MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="80189-180">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="80189-181">Любой</span><span class="sxs-lookup"><span data-stu-id="80189-181">Any</span></span></p></td>
<td><p><span data-ttu-id="80189-182">Пограничный сервер, общедоступный IP-адрес пограничной службы аудио- и видеоданных</span><span class="sxs-lookup"><span data-stu-id="80189-182">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="80189-183">STUN/отключите согласование кандидатов по протоколу TCP/443</span><span class="sxs-lookup"><span data-stu-id="80189-183">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80189-184">A/V/STUN, MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="80189-184">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="80189-185">Пограничный сервер, общедоступный IP-адрес пограничной службы аудио- и видеоданных</span><span class="sxs-lookup"><span data-stu-id="80189-185">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="80189-186">Любой</span><span class="sxs-lookup"><span data-stu-id="80189-186">Any</span></span></p></td>
<td><p><span data-ttu-id="80189-187">STUN/отключите согласование кандидатов по протоколу TCP/443</span><span class="sxs-lookup"><span data-stu-id="80189-187">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="firewall-summary-for-single-consolidated-edge-with-public-ip-addresses-internal-interface"></a><span data-ttu-id="80189-188">Сводка по межсетевому экрану отдельного консолидированного края с общедоступными IP-адресами: внутренний интерфейс</span><span class="sxs-lookup"><span data-stu-id="80189-188">Firewall Summary for Single Consolidated Edge with Public IP Addresses: Internal Interface</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="80189-189">Протокол/TCP или UDP/порт</span><span class="sxs-lookup"><span data-stu-id="80189-189">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="80189-190">IP-адрес источника</span><span class="sxs-lookup"><span data-stu-id="80189-190">Source IP address</span></span></th>
<th><span data-ttu-id="80189-191">IP-адрес назначения</span><span class="sxs-lookup"><span data-stu-id="80189-191">Destination IP address</span></span></th>
<th><span data-ttu-id="80189-192">Комментарии</span><span class="sxs-lookup"><span data-stu-id="80189-192">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="80189-193">XMPP/MTLS/TCP/23456</span><span class="sxs-lookup"><span data-stu-id="80189-193">XMPP/MTLS/TCP/23456</span></span></p></td>
<td><p><span data-ttu-id="80189-194">Any (может быть определен как IP-адрес сервера Standard Edition, IP-адреса стандартного выпуска или IP-адрес пула, на котором запущена служба шлюза XMPP).</span><span class="sxs-lookup"><span data-stu-id="80189-194">Any (can be defined as Standard Edition server IP, Standard Edition server IP address, or pool IP address running the XMPP Gateway service)</span></span></p></td>
<td><p><span data-ttu-id="80189-195">Внутренний интерфейс пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="80189-195">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="80189-196">Исходящий трафик XMPP от службы шлюза XMPP, работающей на сервере переднего плана или в пуле внешних интерфейсов</span><span class="sxs-lookup"><span data-stu-id="80189-196">Outbound XMPP traffic from XMPP Gateway service running on Front End Server or Front End pool</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80189-197">SIP/MTLS/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="80189-197">SIP/MTLS/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="80189-198">Any (может быть определено как режиссер, IP-адрес пула режиссера, сервер клиентского доступа или IP-адрес пула переднего плана)</span><span class="sxs-lookup"><span data-stu-id="80189-198">Any (can be defined as Director, Director pool IP address, Front End Server or Front End pool IP address)</span></span></p></td>
<td><p><span data-ttu-id="80189-199">IP-адрес пограничного сервера или пул, хранящий внутренний интерфейс.</span><span class="sxs-lookup"><span data-stu-id="80189-199">Edge Server IP, or pool that holds the internal interface</span></span></p></td>
<td><p><span data-ttu-id="80189-200">Исходящий трафик SIP (от режиссера, IP-адреса пула, сервера переднего плана или IP-адреса пула переднего плана) к внутреннему интерфейсу пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="80189-200">Outbound SIP traffic (from Director, Director pool IP address, Front End Server or Front End pool IP address) to Edge Server internal interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80189-201">SIP/MTLS/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="80189-201">SIP/MTLS/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="80189-202">Внутренний интерфейс пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="80189-202">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="80189-203">Any (может быть определено как режиссер, IP-адрес пула режиссера, сервер переднего плана или адрес пула переднего плана).</span><span class="sxs-lookup"><span data-stu-id="80189-203">Any (can be defined as Director, Director pool IP address, Front End Server or Front End pool address)</span></span></p></td>
<td><p><span data-ttu-id="80189-204">Входящий трафик SIP (для режиссера, IP-адреса пула, сервера переднего плана или IP-адреса пула переднего плана) от внутреннего интерфейса пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="80189-204">Inbound SIP traffic (to Director, Director pool IP address, Front End Server or Front End pool IP address) from Edge Server internal interface</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80189-205">PSOM/MTLS/TCP/8057</span><span class="sxs-lookup"><span data-stu-id="80189-205">PSOM/MTLS/TCP/8057</span></span></p></td>
<td><p><span data-ttu-id="80189-206">Any (может быть IP-адресом сервера переднего плана или IP-адресом серверного переднего плана в пуле переднего плана)</span><span class="sxs-lookup"><span data-stu-id="80189-206">Any (can be defined as Front End Server IP address, or each Front End Server IP address in a Front End pool)</span></span></p></td>
<td><p><span data-ttu-id="80189-207">Внутренний интерфейс пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="80189-207">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="80189-208">Трафик веб-конференций от сервера переднего плана или каждого серверного переднего плана, если он находится в пуле и является внутренним интерфейсом пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="80189-208">Web conferencing traffic from Front End Server or each Front End Server if in a pool, to Edge Server internal interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80189-209">SIP/MTLS/TCP/5062</span><span class="sxs-lookup"><span data-stu-id="80189-209">SIP/MTLS/TCP/5062</span></span></p></td>
<td><p><span data-ttu-id="80189-210">Any (может быть как IP-адресом переднего сервера, так и IP-адресом пула переднего плана либо любым бесперебойно работающее устройство филиала или с помощью этого пограничного сервера).</span><span class="sxs-lookup"><span data-stu-id="80189-210">Any (can be defined as Front End Server IP address, or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server)</span></span></p></td>
<td><p><span data-ttu-id="80189-211">Внутренний интерфейс пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="80189-211">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="80189-212">Проверка подлинности пользователей/V (служба проверки подлинности A/V) от IP-адреса сервера переднего плана или переднего плана, а также от любого работающего филиала или сервера с бесперебойной подразделением с помощью этого пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="80189-212">Authentication of A/V users (A/V authentication service) from Front End Server or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80189-213">STUN/MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="80189-213">STUN/MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="80189-214">Любой</span><span class="sxs-lookup"><span data-stu-id="80189-214">Any</span></span></p></td>
<td><p><span data-ttu-id="80189-215">Внутренний интерфейс пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="80189-215">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="80189-216">Предпочтительный путь для передачи мультимедиа между внутренними и внешними пользователями, бесперебойно работающем устройстве филиалов или бесперебойно работающем сервере филиала</span><span class="sxs-lookup"><span data-stu-id="80189-216">Preferred path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80189-217">STUN/MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="80189-217">STUN/MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="80189-218">Любой</span><span class="sxs-lookup"><span data-stu-id="80189-218">Any</span></span></p></td>
<td><p><span data-ttu-id="80189-219">Внутренний интерфейс пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="80189-219">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="80189-220">Резервный путь для передачи мультимедиа между внутренними и внешними пользователями, бесперебойно работающее устройство филиала или бесперебойный сервер филиала, если не удается установить UDP-связь, используется протокол TCP для обмена файлами и демонстрации рабочего стола</span><span class="sxs-lookup"><span data-stu-id="80189-220">Fallback path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server if UDP communication cannot be established, TCP is used for file transfer and desktop sharing</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80189-221">HTTPS/TCP/4443</span><span class="sxs-lookup"><span data-stu-id="80189-221">HTTPS/TCP/4443</span></span></p></td>
<td><p><span data-ttu-id="80189-222">Any (может быть указан в качестве IP-адреса сервера переднего плана или пула, содержащего центральное хранилище управления).</span><span class="sxs-lookup"><span data-stu-id="80189-222">Any (can be defined as the Front End Server IP address, or pool that holds the Central Management store)</span></span></p></td>
<td><p><span data-ttu-id="80189-223">Внутренний интерфейс пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="80189-223">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="80189-224">Репликация изменений из хранилища центрального управления на пограничный сервер</span><span class="sxs-lookup"><span data-stu-id="80189-224">Replication of changes from the Central Management store to the Edge Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80189-225">MTLS/TCP/50001</span><span class="sxs-lookup"><span data-stu-id="80189-225">MTLS/TCP/50001</span></span></p></td>
<td><p><span data-ttu-id="80189-226">Любой</span><span class="sxs-lookup"><span data-stu-id="80189-226">Any</span></span></p></td>
<td><p><span data-ttu-id="80189-227">Внутренний интерфейс пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="80189-227">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="80189-228">Централизованное ведение журналов, использование команд командной строки Lync Server Management Shell и централизованной службы ведения журналов, команды ClsController (ClsController.exe) или агента (ClsAgent.exe) и коллекции журналов</span><span class="sxs-lookup"><span data-stu-id="80189-228">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80189-229">MTLS/TCP/50002</span><span class="sxs-lookup"><span data-stu-id="80189-229">MTLS/TCP/50002</span></span></p></td>
<td><p><span data-ttu-id="80189-230">Любой</span><span class="sxs-lookup"><span data-stu-id="80189-230">Any</span></span></p></td>
<td><p><span data-ttu-id="80189-231">Внутренний интерфейс пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="80189-231">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="80189-232">Централизованное ведение журналов, использование команд командной строки Lync Server Management Shell и централизованной службы ведения журналов, команды ClsController (ClsController.exe) или агента (ClsAgent.exe) и коллекции журналов</span><span class="sxs-lookup"><span data-stu-id="80189-232">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80189-233">MTLS/TCP/50003</span><span class="sxs-lookup"><span data-stu-id="80189-233">MTLS/TCP/50003</span></span></p></td>
<td><p><span data-ttu-id="80189-234">Любой</span><span class="sxs-lookup"><span data-stu-id="80189-234">Any</span></span></p></td>
<td><p><span data-ttu-id="80189-235">Внутренний интерфейс пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="80189-235">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="80189-236">Централизованное ведение журналов, использование команд командной строки Lync Server Management Shell и централизованной службы ведения журналов, команды ClsController (ClsController.exe) или агента (ClsAgent.exe) и коллекции журналов</span><span class="sxs-lookup"><span data-stu-id="80189-236">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary-for-federation"></a><span data-ttu-id="80189-237">Сводка по межсетевому экрану для Федерации</span><span class="sxs-lookup"><span data-stu-id="80189-237">Firewall Summary for Federation</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="80189-238">Role/Protocol/TCP/UDP/порт</span><span class="sxs-lookup"><span data-stu-id="80189-238">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="80189-239">IP-адрес источника</span><span class="sxs-lookup"><span data-stu-id="80189-239">Source IP address</span></span></th>
<th><span data-ttu-id="80189-240">IP-адрес назначения</span><span class="sxs-lookup"><span data-stu-id="80189-240">Destination IP address</span></span></th>
<th><span data-ttu-id="80189-241">Примечания.</span><span class="sxs-lookup"><span data-stu-id="80189-241">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="80189-242">Access/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="80189-242">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="80189-243">Общедоступный IP-адрес службы пограничного доступа</span><span class="sxs-lookup"><span data-stu-id="80189-243">Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="80189-244">Любой</span><span class="sxs-lookup"><span data-stu-id="80189-244">Any</span></span></p></td>
<td><p><span data-ttu-id="80189-245">Для Федеративной и общедоступной службы обмена мгновенными сообщениями с помощью SIP</span><span class="sxs-lookup"><span data-stu-id="80189-245">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary--public-instant-messaging-connectivity"></a><span data-ttu-id="80189-246">Сводка по брандмауэрам: общедоступная служба обмена мгновенными сообщениями</span><span class="sxs-lookup"><span data-stu-id="80189-246">Firewall Summary – Public Instant Messaging Connectivity</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="80189-247">Role/Protocol/TCP/UDP/порт</span><span class="sxs-lookup"><span data-stu-id="80189-247">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="80189-248">IP-адрес источника</span><span class="sxs-lookup"><span data-stu-id="80189-248">Source IP address</span></span></th>
<th><span data-ttu-id="80189-249">IP-адрес назначения</span><span class="sxs-lookup"><span data-stu-id="80189-249">Destination IP address</span></span></th>
<th><span data-ttu-id="80189-250">Примечания.</span><span class="sxs-lookup"><span data-stu-id="80189-250">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="80189-251">Access/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="80189-251">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="80189-252">Партнеры по подключению общедоступных мгновенных сообщений</span><span class="sxs-lookup"><span data-stu-id="80189-252">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="80189-253">Служба пограничного доступа к пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="80189-253">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="80189-254">Для Федеративной и общедоступной службы обмена мгновенными сообщениями с помощью SIP</span><span class="sxs-lookup"><span data-stu-id="80189-254">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80189-255">Access/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="80189-255">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="80189-256">Служба пограничного доступа к пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="80189-256">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="80189-257">Партнеры по подключению общедоступных мгновенных сообщений</span><span class="sxs-lookup"><span data-stu-id="80189-257">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="80189-258">Для Федеративной и общедоступной службы обмена мгновенными сообщениями с помощью SIP</span><span class="sxs-lookup"><span data-stu-id="80189-258">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80189-259">Access/SIP (TLS)/TCP/443</span><span class="sxs-lookup"><span data-stu-id="80189-259">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="80189-260">Клиенты</span><span class="sxs-lookup"><span data-stu-id="80189-260">Clients</span></span></p></td>
<td><p><span data-ttu-id="80189-261">Служба пограничного доступа к пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="80189-261">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="80189-262">Трафик SIP "клиент-сервер" для доступа внешних пользователей</span><span class="sxs-lookup"><span data-stu-id="80189-262">Client-to-server SIP traffic for external user access</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80189-263">A/V/RTP/TCP/50000-59,999</span><span class="sxs-lookup"><span data-stu-id="80189-263">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="80189-264">Служба Edge для пограничного сервера A/V</span><span class="sxs-lookup"><span data-stu-id="80189-264">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="80189-265">Клиенты Live Messenger</span><span class="sxs-lookup"><span data-stu-id="80189-265">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="80189-266">Используется для сеансов обмена мгновенными сообщениями с помощью Windows Live Messenger, если настроена служба общего доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="80189-266">Used for A/V sessions with Windows Live Messenger if public IM connectivity is configured.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80189-267">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="80189-267">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="80189-268">Служба Edge для пограничного сервера A/V</span><span class="sxs-lookup"><span data-stu-id="80189-268">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="80189-269">Клиенты Live Messenger</span><span class="sxs-lookup"><span data-stu-id="80189-269">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="80189-270">Требуется для общедоступной службы обмена мгновенными сообщениями в Windows Live Messenger</span><span class="sxs-lookup"><span data-stu-id="80189-270">Required for public IM connectivity with Windows Live Messenger</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80189-271">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="80189-271">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="80189-272">Клиенты Live Messenger</span><span class="sxs-lookup"><span data-stu-id="80189-272">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="80189-273">Служба Edge для пограничного сервера A/V</span><span class="sxs-lookup"><span data-stu-id="80189-273">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="80189-274">Требуется для общедоступной службы обмена мгновенными сообщениями в Windows Live Messenger</span><span class="sxs-lookup"><span data-stu-id="80189-274">Required for public IM connectivity with Windows Live Messenger</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary-for-extensible-messaging-and-presence-protocol"></a><span data-ttu-id="80189-275">Сводка брандмауэра по протоколу расширенного обмена сообщениями и присутствия</span><span class="sxs-lookup"><span data-stu-id="80189-275">Firewall Summary for Extensible Messaging and Presence Protocol</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="80189-276">Протокол/TCP или UDP/порт</span><span class="sxs-lookup"><span data-stu-id="80189-276">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="80189-277">Источник (IP-адрес)</span><span class="sxs-lookup"><span data-stu-id="80189-277">Source (IP address)</span></span></th>
<th><span data-ttu-id="80189-278">Назначение (IP-адрес)</span><span class="sxs-lookup"><span data-stu-id="80189-278">Destination (IP address)</span></span></th>
<th><span data-ttu-id="80189-279">Комментарии</span><span class="sxs-lookup"><span data-stu-id="80189-279">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="80189-280">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="80189-280">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="80189-281">Любой</span><span class="sxs-lookup"><span data-stu-id="80189-281">Any</span></span></p></td>
<td><p><span data-ttu-id="80189-282">IP-адрес интерфейса службы пограничного доступа к серверу Edge</span><span class="sxs-lookup"><span data-stu-id="80189-282">Edge Server Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="80189-283">Стандартный коммуникационный порт "сервер-сервер" для XMPP.</span><span class="sxs-lookup"><span data-stu-id="80189-283">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="80189-284">Разрешает связь с прокси-сервером пограничного сервера XMPP от федеративных XMPP партнеров</span><span class="sxs-lookup"><span data-stu-id="80189-284">Allows communication to the Edge Server XMPP proxy from federated XMPP partners</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80189-285">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="80189-285">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="80189-286">IP-адрес интерфейса службы пограничного доступа к серверу Edge</span><span class="sxs-lookup"><span data-stu-id="80189-286">Edge Server Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="80189-287">Любой</span><span class="sxs-lookup"><span data-stu-id="80189-287">Any</span></span></p></td>
<td><p><span data-ttu-id="80189-288">Стандартный коммуникационный порт "сервер-сервер" для XMPP.</span><span class="sxs-lookup"><span data-stu-id="80189-288">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="80189-289">Разрешает взаимодействие с XMPP прокси-сервером для федеративных XMPP партнеров</span><span class="sxs-lookup"><span data-stu-id="80189-289">Allows communication from the Edge Server XMPP proxy to federated XMPP partners</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80189-290">XMPP/MTLS/TCP/23456</span><span class="sxs-lookup"><span data-stu-id="80189-290">XMPP/MTLS/TCP/23456</span></span></p></td>
<td><p><span data-ttu-id="80189-291">Любой</span><span class="sxs-lookup"><span data-stu-id="80189-291">Any</span></span></p></td>
<td><p><span data-ttu-id="80189-292">Каждый внутренний IP-адрес интерфейса пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="80189-292">Each internal Edge Server Interface IP</span></span></p></td>
<td><p><span data-ttu-id="80189-293">Внутренний IP-адрес XMPP, входящий в состав шлюза XMPP на сервере переднего плана или в пуле переднего плана, в адрес внутренней сети пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="80189-293">Internal XMPP traffic from the XMPP Gateway on the Front End Server or Front End pool to the Edge Server internal IP address or each Edge pool member’s internal IP address</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="80189-294">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="80189-294">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

