---
title: Сводка по портам — единая консолидированная пограничная топология с закрытыми IP-адресами и трансляцией сетевых адресов
description: Общие сведения о портах — одинарный консолидированный край с частными IP-адресами с помощью NAT.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - Single consolidated edge with private IP addresses using NAT
ms:assetid: 3c1a389f-5f42-4719-a05b-e0b84aa3eb9e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425891(v=OCS.15)
ms:contentKeyID: 48183877
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a3fc182b9fbbd24d589feb7f73e3c0086fa23152
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424298"
---
# <a name="port-summary---single-consolidated-edge-with-private-ip-addresses-using-nat-in-lync-server-2013"></a><span data-ttu-id="d04ce-103">Сводка по портам — единая консолидированная пограничная топология с закрытыми IP-адресами и трансляцией сетевых адресов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d04ce-103">Port summary - Single consolidated edge with private IP addresses using NAT in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d04ce-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d04ce-104">

<span> </span></span></span>

<span data-ttu-id="d04ce-105">_**Тема последнего изменения:** 2013-04-03_</span><span class="sxs-lookup"><span data-stu-id="d04ce-105">_**Topic Last Modified:** 2013-04-03_</span></span>

<span data-ttu-id="d04ce-106">Функция пограничного сервера Lync Server 2013, описанная в этой архитектуре сценариев, очень похожа на ту, что была реализована в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d04ce-106">The Lync Server 2013, Edge Server functionality described in this scenario architecture is very similar to what was implemented in Lync Server 2010.</span></span> <span data-ttu-id="d04ce-107">Наиболее заметным дополнением является порт **5269 на TCP** для протокола расширенной обработки сообщений и присутствия (XMPP).</span><span class="sxs-lookup"><span data-stu-id="d04ce-107">The most noticeable addition is the port **5269 over TCP** entry for the extensible messaging and presence protocol (XMPP).</span></span> <span data-ttu-id="d04ce-108">Lync Server 2013 (при необходимости) можно развернуть прокси-сервер XMPP на пограничном или пограничном пуле, а также на сервере шлюзов XMPP на сервере переднего плана или в пуле внешних интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="d04ce-108">Lync Server 2013 optionally deploys an XMPP proxy on the Edge Server or Edge pool and the XMPP gateway server on the Front End Server or Front End pool.</span></span>

<span data-ttu-id="d04ce-109">В дополнение к протоколу IPv4, пограничный сервер теперь поддерживает IPv6.</span><span class="sxs-lookup"><span data-stu-id="d04ce-109">In addition to IPv4, the Edge Server now supports IPv6.</span></span> <span data-ttu-id="d04ce-110">Для ясности в сценариях используется только протокол IPv4.</span><span class="sxs-lookup"><span data-stu-id="d04ce-110">For clarity, only IPv4 is used in the scenarios.</span></span>

<span data-ttu-id="d04ce-111">**Периметр сети для единого консолидированного пограничного сервера с использованием протокола преобразования сетевых адресов (NAT)**</span><span class="sxs-lookup"><span data-stu-id="d04ce-111">**Network Perimeter for a Single Consolidated Edge Server with Private IP Addressing Using NAT**</span></span>

<span data-ttu-id="d04ce-112">![f8c144c5-e5fb-498a-823e-eb39f26b6847](images/Gg425891.f8c144c5-e5fb-498a-823e-eb39f26b6847(OCS.15).jpg "f8c144c5-e5fb-498a-823e-eb39f26b6847")</span><span class="sxs-lookup"><span data-stu-id="d04ce-112">![f8c144c5-e5fb-498a-823e-eb39f26b6847](images/Gg425891.f8c144c5-e5fb-498a-823e-eb39f26b6847(OCS.15).jpg "f8c144c5-e5fb-498a-823e-eb39f26b6847")</span></span>

<div>

## <a name="port-and-protocol-details"></a><span data-ttu-id="d04ce-113">Сведения о портах и протоколах</span><span class="sxs-lookup"><span data-stu-id="d04ce-113">Port and Protocol Details</span></span>

<span data-ttu-id="d04ce-114">Мы рекомендуем открывать только порты, необходимые для поддержки функций, для которых предоставляется внешний доступ.</span><span class="sxs-lookup"><span data-stu-id="d04ce-114">We recommend that you open only the ports required to support the functionality for which you are providing external access.</span></span>

<span data-ttu-id="d04ce-115">Для удаленного доступа к работе в любой службе пограничного сервера необходимо, чтобы трафик SIP был в направлении на один и тот же трафик по внешнему потоку, как показано на рисунке входящего и исходящего трафика пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="d04ce-115">For remote access to work for any edge service, it is mandatory that SIP traffic is allowed to flow bi-directionally as shown in the Inbound/Outbound edge traffic figure.</span></span> <span data-ttu-id="d04ce-116">Другими словами, Обмен сообщениями SIP и из службы Edge для Access осуществляется в обмене мгновенными сообщениями, присутствии, веб-конференциях, аудио-и видеосвязи (A/V) и Федерации.</span><span class="sxs-lookup"><span data-stu-id="d04ce-116">Stated another way, the SIP messaging to and from the Access Edge service is involved in instant messaging (IM), presence, web conferencing, audio/video (A/V), and federation.</span></span>

### <a name="firewall-summary-for-single-consolidated-edge-with-private-ip-addresses-using-nat-external-interface"></a><span data-ttu-id="d04ce-117">Сводка по межсетевому экрану для отдельного консолидированного края с частными IP-адресами с использованием NAT: внешний интерфейс</span><span class="sxs-lookup"><span data-stu-id="d04ce-117">Firewall Summary for Single Consolidated Edge with Private IP Addresses using NAT: External Interface</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d04ce-118">Role/Protocol/TCP/UDP/порт</span><span class="sxs-lookup"><span data-stu-id="d04ce-118">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="d04ce-119">IP-адрес источника</span><span class="sxs-lookup"><span data-stu-id="d04ce-119">Source IP address</span></span></th>
<th><span data-ttu-id="d04ce-120">IP-адрес назначения</span><span class="sxs-lookup"><span data-stu-id="d04ce-120">Destination IP address</span></span></th>
<th><span data-ttu-id="d04ce-121">Примечания.</span><span class="sxs-lookup"><span data-stu-id="d04ce-121">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d04ce-122">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="d04ce-122">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="d04ce-123">Любой</span><span class="sxs-lookup"><span data-stu-id="d04ce-123">Any</span></span></p></td>
<td><p><span data-ttu-id="d04ce-124">Прокси-служба XMPP (доступ к IP-адресу для общих ресурсов с помощью службы Edge Access)</span><span class="sxs-lookup"><span data-stu-id="d04ce-124">XMPP Proxy service (shares IP address with Access Edge service)</span></span></p></td>
<td><p><span data-ttu-id="d04ce-125">Прокси-служба XMPP принимает трафик от XMPP контактов в определенных XMPP федерациях.</span><span class="sxs-lookup"><span data-stu-id="d04ce-125">XMPP Proxy service accepts traffic from XMPP contacts in defined XMPP federations</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d04ce-126">Access/HTTP/TCP/80</span><span class="sxs-lookup"><span data-stu-id="d04ce-126">Access/HTTP/TCP/80</span></span></p></td>
<td><p><span data-ttu-id="d04ce-127">Служба пограничного доступа к пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="d04ce-127">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="d04ce-128">Любой</span><span class="sxs-lookup"><span data-stu-id="d04ce-128">Any</span></span></p></td>
<td><p><span data-ttu-id="d04ce-129">Проверка отзыва сертификатов и получения CRL</span><span class="sxs-lookup"><span data-stu-id="d04ce-129">Certificate revocation/CRL check and retrieval</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d04ce-130">Access/DNS/TCP/53</span><span class="sxs-lookup"><span data-stu-id="d04ce-130">Access/DNS/TCP/53</span></span></p></td>
<td><p><span data-ttu-id="d04ce-131">Служба пограничного доступа к пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="d04ce-131">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="d04ce-132">Любой</span><span class="sxs-lookup"><span data-stu-id="d04ce-132">Any</span></span></p></td>
<td><p><span data-ttu-id="d04ce-133">Запрос DNS по протоколу TCP</span><span class="sxs-lookup"><span data-stu-id="d04ce-133">DNS query over TCP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d04ce-134">Access/DNS/UDP/53</span><span class="sxs-lookup"><span data-stu-id="d04ce-134">Access/DNS/UDP/53</span></span></p></td>
<td><p><span data-ttu-id="d04ce-135">Служба пограничного доступа к пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="d04ce-135">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="d04ce-136">Любой</span><span class="sxs-lookup"><span data-stu-id="d04ce-136">Any</span></span></p></td>
<td><p><span data-ttu-id="d04ce-137">Запрос DNS по протоколу UDP</span><span class="sxs-lookup"><span data-stu-id="d04ce-137">DNS query over UDP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d04ce-138">Access/SIP (TLS)/TCP/443</span><span class="sxs-lookup"><span data-stu-id="d04ce-138">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="d04ce-139">Любой</span><span class="sxs-lookup"><span data-stu-id="d04ce-139">Any</span></span></p></td>
<td><p><span data-ttu-id="d04ce-140">Служба пограничного доступа к пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="d04ce-140">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="d04ce-141">Трафик SIP "клиент-сервер" для доступа внешних пользователей</span><span class="sxs-lookup"><span data-stu-id="d04ce-141">Client-to-server SIP traffic for external user access</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d04ce-142">Access/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="d04ce-142">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="d04ce-143">Любой</span><span class="sxs-lookup"><span data-stu-id="d04ce-143">Any</span></span></p></td>
<td><p><span data-ttu-id="d04ce-144">Служба пограничного доступа к пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="d04ce-144">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="d04ce-145">Для Федеративной и общедоступной службы обмена мгновенными сообщениями с помощью SIP</span><span class="sxs-lookup"><span data-stu-id="d04ce-145">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d04ce-146">Access/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="d04ce-146">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="d04ce-147">Служба пограничного доступа к пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="d04ce-147">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="d04ce-148">Любой</span><span class="sxs-lookup"><span data-stu-id="d04ce-148">Any</span></span></p></td>
<td><p><span data-ttu-id="d04ce-149">Для Федеративной и общедоступной службы обмена мгновенными сообщениями с помощью SIP</span><span class="sxs-lookup"><span data-stu-id="d04ce-149">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d04ce-150">Веб-конференции/PSOM (TLS)/TCP/443</span><span class="sxs-lookup"><span data-stu-id="d04ce-150">Web Conferencing/PSOM(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="d04ce-151">Любой</span><span class="sxs-lookup"><span data-stu-id="d04ce-151">Any</span></span></p></td>
<td><p><span data-ttu-id="d04ce-152">Служба веб-конференций пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="d04ce-152">Edge Server Web Conferencing Edge service</span></span></p></td>
<td><p><span data-ttu-id="d04ce-153">Мультимедиа для веб-конференций</span><span class="sxs-lookup"><span data-stu-id="d04ce-153">Web Conferencing media</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d04ce-154">A/V/RTP/TCP/50000-59,999</span><span class="sxs-lookup"><span data-stu-id="d04ce-154">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="d04ce-155">Служба Edge для пограничного сервера A/V</span><span class="sxs-lookup"><span data-stu-id="d04ce-155">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="d04ce-156">Любой</span><span class="sxs-lookup"><span data-stu-id="d04ce-156">Any</span></span></p></td>
<td><p><span data-ttu-id="d04ce-157">Требуется для Федерации с партнерами, работающими под управлением Office Communications Server 2007, Office Communications Server 2007 R2, Lync Server 2010 и Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d04ce-157">Required for federating with partners running Office Communications Server 2007, Office Communications Server 2007 R2, Lync Server 2010 and Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d04ce-158">A/V/RTP/UDP/50000-59,999</span><span class="sxs-lookup"><span data-stu-id="d04ce-158">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="d04ce-159">Служба Edge для пограничного сервера A/V</span><span class="sxs-lookup"><span data-stu-id="d04ce-159">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="d04ce-160">Любой</span><span class="sxs-lookup"><span data-stu-id="d04ce-160">Any</span></span></p></td>
<td><p><span data-ttu-id="d04ce-161">Требуется только для Федерации с партнерами, работающими под управлением Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="d04ce-161">Required only for federation with partners running Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d04ce-162">A/V/RTP/TCP/50000-59,999</span><span class="sxs-lookup"><span data-stu-id="d04ce-162">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="d04ce-163">Любой</span><span class="sxs-lookup"><span data-stu-id="d04ce-163">Any</span></span></p></td>
<td><p><span data-ttu-id="d04ce-164">Служба Edge для пограничного сервера A/V</span><span class="sxs-lookup"><span data-stu-id="d04ce-164">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="d04ce-165">Требуется только для Федерации с партнерами, работающими под управлением Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="d04ce-165">Required only for federation with partners running Office Communications Server 2007</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d04ce-166">A/V/RTP/UDP/50000-59,999</span><span class="sxs-lookup"><span data-stu-id="d04ce-166">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="d04ce-167">Любой</span><span class="sxs-lookup"><span data-stu-id="d04ce-167">Any</span></span></p></td>
<td><p><span data-ttu-id="d04ce-168">Служба Edge для пограничного сервера A/V</span><span class="sxs-lookup"><span data-stu-id="d04ce-168">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="d04ce-169">Требуется только для Федерации с партнерами, работающими под управлением Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="d04ce-169">Required only for federation with partners running Office Communications Server 2007</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d04ce-170">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="d04ce-170">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="d04ce-171">Служба Edge для пограничного сервера A/V</span><span class="sxs-lookup"><span data-stu-id="d04ce-171">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="d04ce-172">Любой</span><span class="sxs-lookup"><span data-stu-id="d04ce-172">Any</span></span></p></td>
<td><p><span data-ttu-id="d04ce-173">3478 Outbound используется для определения версии пограничного сервера, с которым обменивается данными Lync Server, а также для мультимедийного трафика от пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="d04ce-173">3478 outbound is used to determine the version of Edge Server that Lync Server is communicating with and also for media traffic from Edge Server-to-Edge Server.</span></span> <span data-ttu-id="d04ce-174">Требуется для Федерации с Lync Server 2010, Windows Live Messenger и Office Communications Server 2007 R2, а также в том случае, если в компании развернуты несколько пулов Edge.</span><span class="sxs-lookup"><span data-stu-id="d04ce-174">Required for federation with Lync Server 2010, Windows Live Messenger, and Office Communications Server 2007 R2, and also if multiple Edge pools are deployed within a company.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d04ce-175">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="d04ce-175">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="d04ce-176">Любой</span><span class="sxs-lookup"><span data-stu-id="d04ce-176">Any</span></span></p></td>
<td><p><span data-ttu-id="d04ce-177">Служба Edge для пограничного сервера A/V</span><span class="sxs-lookup"><span data-stu-id="d04ce-177">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="d04ce-178">STUN/отключите согласование кандидатов по протоколу UDP/3478</span><span class="sxs-lookup"><span data-stu-id="d04ce-178">STUN/TURN negotiation of candidates over UDP/3478</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d04ce-179">A/V/STUN, MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="d04ce-179">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="d04ce-180">Любой</span><span class="sxs-lookup"><span data-stu-id="d04ce-180">Any</span></span></p></td>
<td><p><span data-ttu-id="d04ce-181">Служба Edge для пограничного сервера A/V</span><span class="sxs-lookup"><span data-stu-id="d04ce-181">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="d04ce-182">STUN/отключите согласование кандидатов по протоколу TCP/443</span><span class="sxs-lookup"><span data-stu-id="d04ce-182">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d04ce-183">A/V/STUN, MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="d04ce-183">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="d04ce-184">Служба Edge для пограничного сервера A/V</span><span class="sxs-lookup"><span data-stu-id="d04ce-184">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="d04ce-185">Любой</span><span class="sxs-lookup"><span data-stu-id="d04ce-185">Any</span></span></p></td>
<td><p><span data-ttu-id="d04ce-186">STUN/отключите согласование кандидатов по протоколу TCP/443</span><span class="sxs-lookup"><span data-stu-id="d04ce-186">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="firewall-summary-for-single-consolidated-edge-with-private-ip-addresses-using-nat-internal-interface"></a><span data-ttu-id="d04ce-187">Сводка по межсетевому экрану для отдельного консолидированного края с частными IP-адресами с использованием NAT: внутренний интерфейс</span><span class="sxs-lookup"><span data-stu-id="d04ce-187">Firewall Summary for Single Consolidated Edge with Private IP Addresses Using NAT: Internal Interface</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d04ce-188">Протокол/TCP или UDP/порт</span><span class="sxs-lookup"><span data-stu-id="d04ce-188">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="d04ce-189">IP-адрес источника</span><span class="sxs-lookup"><span data-stu-id="d04ce-189">Source IP address</span></span></th>
<th><span data-ttu-id="d04ce-190">IP-адрес назначения</span><span class="sxs-lookup"><span data-stu-id="d04ce-190">Destination IP address</span></span></th>
<th><span data-ttu-id="d04ce-191">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d04ce-191">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d04ce-192">XMPP/MTLS/TCP/23456</span><span class="sxs-lookup"><span data-stu-id="d04ce-192">XMPP/MTLS/TCP/23456</span></span></p></td>
<td><p><span data-ttu-id="d04ce-193">Any (может быть определен как IP-адрес сервера Standard Edition, IP-адреса стандартного выпуска или IP-адрес пула, на котором запущена служба шлюза XMPP).</span><span class="sxs-lookup"><span data-stu-id="d04ce-193">Any (can be defined as Standard Edition server IP, Standard Edition server IP address, or pool IP address running the XMPP Gateway service)</span></span></p></td>
<td><p><span data-ttu-id="d04ce-194">Внутренний интерфейс пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="d04ce-194">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="d04ce-195">Исходящий трафик XMPP от службы шлюза XMPP, работающей на сервере переднего плана или в пуле внешних интерфейсов</span><span class="sxs-lookup"><span data-stu-id="d04ce-195">Outbound XMPP traffic from XMPP Gateway service running on Front End Server or Front End pool</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d04ce-196">SIP/MTLS/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="d04ce-196">SIP/MTLS/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="d04ce-197">Any (может быть определено как режиссер, IP-адрес пула режиссера, сервер клиентского доступа или IP-адрес пула переднего плана)</span><span class="sxs-lookup"><span data-stu-id="d04ce-197">Any (can be defined as Director, Director pool IP address, Front End Server or Front End pool IP address)</span></span></p></td>
<td><p><span data-ttu-id="d04ce-198">Внутренний интерфейс пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="d04ce-198">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="d04ce-199">Исходящий трафик SIP (от режиссера, IP-адреса пула, сервера переднего плана или IP-адреса пула переднего плана) к внутреннему интерфейсу пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="d04ce-199">Outbound SIP traffic (from Director, Director pool IP address, Front End Server or Front End pool IP address) to Edge Server internal interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d04ce-200">SIP/MTLS/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="d04ce-200">SIP/MTLS/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="d04ce-201">Внутренний интерфейс пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="d04ce-201">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="d04ce-202">Any (может быть определено как режиссер, IP-адрес пула режиссера, сервер клиентского доступа или IP-адрес пула переднего плана)</span><span class="sxs-lookup"><span data-stu-id="d04ce-202">Any (can be defined as Director, Director pool IP address, Front End Server or Front End pool IP address)</span></span></p></td>
<td><p><span data-ttu-id="d04ce-203">Входящий трафик SIP (для режиссера, IP-адреса пула, сервера переднего плана или IP-адреса пула переднего плана) от внутреннего интерфейса пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="d04ce-203">Inbound SIP traffic (to Director, Director pool IP address, Front End Server or Front End pool IP address) from Edge Server internal interface</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d04ce-204">PSOM/MTLS/TCP/8057</span><span class="sxs-lookup"><span data-stu-id="d04ce-204">PSOM/MTLS/TCP/8057</span></span></p></td>
<td><p><span data-ttu-id="d04ce-205">Any (может быть IP-адресом сервера переднего плана или IP-адресом серверного переднего плана в пуле переднего плана)</span><span class="sxs-lookup"><span data-stu-id="d04ce-205">Any (can be defined as Front End Server IP address, or each Front End Server IP address in a Front End pool)</span></span></p></td>
<td><p><span data-ttu-id="d04ce-206">Внутренний интерфейс пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="d04ce-206">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="d04ce-207">Трафик веб-конференций от сервера переднего плана или каждого серверного переднего плана, если он находится в пуле и является внутренним интерфейсом пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="d04ce-207">Web conferencing traffic from Front End Server or each Front End Server if in a pool, to Edge Server internal interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d04ce-208">SIP/MTLS/TCP/5062</span><span class="sxs-lookup"><span data-stu-id="d04ce-208">SIP/MTLS/TCP/5062</span></span></p></td>
<td><p><span data-ttu-id="d04ce-209">Any (может быть как IP-адресом переднего сервера, так и IP-адресом пула переднего плана либо любым бесперебойно работающее устройство филиала или с помощью этого пограничного сервера).</span><span class="sxs-lookup"><span data-stu-id="d04ce-209">Any (can be defined as Front End Server IP address, or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server)</span></span></p></td>
<td><p><span data-ttu-id="d04ce-210">Внутренний интерфейс пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="d04ce-210">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="d04ce-211">Проверка подлинности пользователей/V (служба проверки подлинности A/V) от IP-адреса сервера переднего плана или переднего плана, а также от любого работающего филиала или сервера с бесперебойной подразделением с помощью этого пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="d04ce-211">Authentication of A/V users (A/V authentication service) from Front End Server or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d04ce-212">STUN/MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="d04ce-212">STUN/MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="d04ce-213">Любой</span><span class="sxs-lookup"><span data-stu-id="d04ce-213">Any</span></span></p></td>
<td><p><span data-ttu-id="d04ce-214">Внутренний интерфейс пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="d04ce-214">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="d04ce-215">Предпочтительный путь для передачи мультимедиа между внутренними и внешними пользователями, бесперебойно работающем устройстве филиалов или бесперебойно работающем сервере филиала</span><span class="sxs-lookup"><span data-stu-id="d04ce-215">Preferred path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d04ce-216">STUN/MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="d04ce-216">STUN/MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="d04ce-217">Любой</span><span class="sxs-lookup"><span data-stu-id="d04ce-217">Any</span></span></p></td>
<td><p><span data-ttu-id="d04ce-218">Внутренний интерфейс пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="d04ce-218">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="d04ce-219">Резервный путь для передачи мультимедиа между внутренними и внешними пользователями, бесперебойно работающее устройство филиала или бесперебойный сервер филиала, если не удается установить UDP-связь, используется протокол TCP для обмена файлами и демонстрации рабочего стола</span><span class="sxs-lookup"><span data-stu-id="d04ce-219">Fallback path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server if UDP communication cannot be established, TCP is used for file transfer and desktop sharing</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d04ce-220">HTTPS/TCP/4443</span><span class="sxs-lookup"><span data-stu-id="d04ce-220">HTTPS/TCP/4443</span></span></p></td>
<td><p><span data-ttu-id="d04ce-221">Any (может быть указан в качестве IP-адреса сервера переднего плана или пула, содержащего центральное хранилище управления).</span><span class="sxs-lookup"><span data-stu-id="d04ce-221">Any (can be defined as the Front End Server IP address, or pool that holds the Central Management store)</span></span></p></td>
<td><p><span data-ttu-id="d04ce-222">Внутренний интерфейс пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="d04ce-222">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="d04ce-223">Репликация изменений из хранилища центрального управления на пограничный сервер</span><span class="sxs-lookup"><span data-stu-id="d04ce-223">Replication of changes from the Central Management store to the Edge Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d04ce-224">MTLS/TCP/50001</span><span class="sxs-lookup"><span data-stu-id="d04ce-224">MTLS/TCP/50001</span></span></p></td>
<td><p><span data-ttu-id="d04ce-225">Любой</span><span class="sxs-lookup"><span data-stu-id="d04ce-225">Any</span></span></p></td>
<td><p><span data-ttu-id="d04ce-226">Внутренний интерфейс пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="d04ce-226">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="d04ce-227">Централизованное ведение журналов, использование команд командной строки Lync Server Management Shell и централизованной службы ведения журналов, команды ClsController (ClsController.exe) или агента (ClsAgent.exe) и коллекции журналов</span><span class="sxs-lookup"><span data-stu-id="d04ce-227">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d04ce-228">MTLS/TCP/50002</span><span class="sxs-lookup"><span data-stu-id="d04ce-228">MTLS/TCP/50002</span></span></p></td>
<td><p><span data-ttu-id="d04ce-229">Любой</span><span class="sxs-lookup"><span data-stu-id="d04ce-229">Any</span></span></p></td>
<td><p><span data-ttu-id="d04ce-230">Внутренний интерфейс пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="d04ce-230">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="d04ce-231">Централизованное ведение журналов, использование команд командной строки Lync Server Management Shell и централизованной службы ведения журналов, команды ClsController (ClsController.exe) или агента (ClsAgent.exe) и коллекции журналов</span><span class="sxs-lookup"><span data-stu-id="d04ce-231">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d04ce-232">MTLS/TCP/50003</span><span class="sxs-lookup"><span data-stu-id="d04ce-232">MTLS/TCP/50003</span></span></p></td>
<td><p><span data-ttu-id="d04ce-233">Любой</span><span class="sxs-lookup"><span data-stu-id="d04ce-233">Any</span></span></p></td>
<td><p><span data-ttu-id="d04ce-234">Внутренний интерфейс пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="d04ce-234">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="d04ce-235">Централизованное ведение журналов, использование команд командной строки Lync Server Management Shell и централизованной службы ведения журналов, команды ClsController (ClsController.exe) или агента (ClsAgent.exe) и коллекции журналов</span><span class="sxs-lookup"><span data-stu-id="d04ce-235">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary-for-federation"></a><span data-ttu-id="d04ce-236">Сводка по межсетевому экрану для Федерации</span><span class="sxs-lookup"><span data-stu-id="d04ce-236">Firewall Summary for Federation</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d04ce-237">Role/Protocol/TCP/UDP/порт</span><span class="sxs-lookup"><span data-stu-id="d04ce-237">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="d04ce-238">IP-адрес источника</span><span class="sxs-lookup"><span data-stu-id="d04ce-238">Source IP address</span></span></th>
<th><span data-ttu-id="d04ce-239">IP-адрес назначения</span><span class="sxs-lookup"><span data-stu-id="d04ce-239">Destination IP address</span></span></th>
<th><span data-ttu-id="d04ce-240">Примечания.</span><span class="sxs-lookup"><span data-stu-id="d04ce-240">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d04ce-241">Access/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="d04ce-241">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="d04ce-242">Общедоступный IP-адрес службы пограничного доступа</span><span class="sxs-lookup"><span data-stu-id="d04ce-242">Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="d04ce-243">Любой</span><span class="sxs-lookup"><span data-stu-id="d04ce-243">Any</span></span></p></td>
<td><p><span data-ttu-id="d04ce-244">Для Федеративной и общедоступной службы обмена мгновенными сообщениями с помощью SIP</span><span class="sxs-lookup"><span data-stu-id="d04ce-244">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary--public-instant-messaging-connectivity"></a><span data-ttu-id="d04ce-245">Сводка по брандмауэрам: общедоступная служба обмена мгновенными сообщениями</span><span class="sxs-lookup"><span data-stu-id="d04ce-245">Firewall Summary – Public Instant Messaging Connectivity</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d04ce-246">Role/Protocol/TCP/UDP/порт</span><span class="sxs-lookup"><span data-stu-id="d04ce-246">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="d04ce-247">IP-адрес источника</span><span class="sxs-lookup"><span data-stu-id="d04ce-247">Source IP address</span></span></th>
<th><span data-ttu-id="d04ce-248">IP-адрес назначения</span><span class="sxs-lookup"><span data-stu-id="d04ce-248">Destination IP address</span></span></th>
<th><span data-ttu-id="d04ce-249">Примечания.</span><span class="sxs-lookup"><span data-stu-id="d04ce-249">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d04ce-250">Access/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="d04ce-250">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="d04ce-251">Партнеры по подключению общедоступных мгновенных сообщений</span><span class="sxs-lookup"><span data-stu-id="d04ce-251">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="d04ce-252">Служба пограничного доступа к пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="d04ce-252">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="d04ce-253">Для Федеративной и общедоступной службы обмена мгновенными сообщениями с помощью SIP</span><span class="sxs-lookup"><span data-stu-id="d04ce-253">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d04ce-254">Access/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="d04ce-254">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="d04ce-255">Служба пограничного доступа к пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="d04ce-255">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="d04ce-256">Партнеры по подключению общедоступных мгновенных сообщений</span><span class="sxs-lookup"><span data-stu-id="d04ce-256">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="d04ce-257">Для Федеративной и общедоступной службы обмена мгновенными сообщениями с помощью SIP</span><span class="sxs-lookup"><span data-stu-id="d04ce-257">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d04ce-258">Access/SIP (TLS)/TCP/443</span><span class="sxs-lookup"><span data-stu-id="d04ce-258">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="d04ce-259">Клиенты</span><span class="sxs-lookup"><span data-stu-id="d04ce-259">Clients</span></span></p></td>
<td><p><span data-ttu-id="d04ce-260">Служба пограничного доступа к пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="d04ce-260">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="d04ce-261">Трафик SIP "клиент-сервер" для доступа внешних пользователей</span><span class="sxs-lookup"><span data-stu-id="d04ce-261">Client-to-server SIP traffic for external user access</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d04ce-262">A/V/RTP/TCP/50000-59,999</span><span class="sxs-lookup"><span data-stu-id="d04ce-262">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="d04ce-263">Служба Edge для пограничного сервера A/V</span><span class="sxs-lookup"><span data-stu-id="d04ce-263">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="d04ce-264">Клиенты Live Messenger</span><span class="sxs-lookup"><span data-stu-id="d04ce-264">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="d04ce-265">Используется для сеансов обмена мгновенными сообщениями с помощью Windows Live Messenger, если настроена служба общего доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="d04ce-265">Used for A/V sessions with Windows Live Messenger if public IM connectivity is configured.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d04ce-266">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="d04ce-266">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="d04ce-267">Служба Edge для пограничного сервера A/V</span><span class="sxs-lookup"><span data-stu-id="d04ce-267">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="d04ce-268">Клиенты Live Messenger</span><span class="sxs-lookup"><span data-stu-id="d04ce-268">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="d04ce-269">Требуется для общедоступной службы обмена мгновенными сообщениями в Windows Live Messenger</span><span class="sxs-lookup"><span data-stu-id="d04ce-269">Required for public IM connectivity with Windows Live Messenger</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d04ce-270">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="d04ce-270">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="d04ce-271">Клиенты Live Messenger</span><span class="sxs-lookup"><span data-stu-id="d04ce-271">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="d04ce-272">Служба Edge для пограничного сервера A/V</span><span class="sxs-lookup"><span data-stu-id="d04ce-272">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="d04ce-273">Требуется для общедоступной службы обмена мгновенными сообщениями в Windows Live Messenger</span><span class="sxs-lookup"><span data-stu-id="d04ce-273">Required for public IM connectivity with Windows Live Messenger</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary-for-extensible-messaging-and-presence-protocol"></a><span data-ttu-id="d04ce-274">Сводка брандмауэра по протоколу расширенного обмена сообщениями и присутствия</span><span class="sxs-lookup"><span data-stu-id="d04ce-274">Firewall Summary for Extensible Messaging and Presence Protocol</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d04ce-275">Протокол/TCP или UDP/порт</span><span class="sxs-lookup"><span data-stu-id="d04ce-275">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="d04ce-276">Источник (IP-адрес)</span><span class="sxs-lookup"><span data-stu-id="d04ce-276">Source (IP address)</span></span></th>
<th><span data-ttu-id="d04ce-277">Назначение (IP-адрес)</span><span class="sxs-lookup"><span data-stu-id="d04ce-277">Destination (IP address)</span></span></th>
<th><span data-ttu-id="d04ce-278">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d04ce-278">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d04ce-279">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="d04ce-279">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="d04ce-280">Любой</span><span class="sxs-lookup"><span data-stu-id="d04ce-280">Any</span></span></p></td>
<td><p><span data-ttu-id="d04ce-281">IP-адрес интерфейса службы пограничного доступа к серверу Edge</span><span class="sxs-lookup"><span data-stu-id="d04ce-281">Edge Server Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="d04ce-282">Стандартный коммуникационный порт "сервер-сервер" для XMPP.</span><span class="sxs-lookup"><span data-stu-id="d04ce-282">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="d04ce-283">Разрешает связь с прокси-сервером пограничного сервера XMPP от федеративных XMPP партнеров</span><span class="sxs-lookup"><span data-stu-id="d04ce-283">Allows communication to the Edge Server XMPP proxy from federated XMPP partners</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d04ce-284">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="d04ce-284">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="d04ce-285">IP-адрес интерфейса службы пограничного доступа к серверу Edge</span><span class="sxs-lookup"><span data-stu-id="d04ce-285">Edge Server Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="d04ce-286">Любой</span><span class="sxs-lookup"><span data-stu-id="d04ce-286">Any</span></span></p></td>
<td><p><span data-ttu-id="d04ce-287">Стандартный коммуникационный порт "сервер-сервер" для XMPP.</span><span class="sxs-lookup"><span data-stu-id="d04ce-287">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="d04ce-288">Разрешает взаимодействие с XMPP прокси-сервером для федеративных XMPP партнеров</span><span class="sxs-lookup"><span data-stu-id="d04ce-288">Allows communication from the Edge Server XMPP proxy to federated XMPP partners</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d04ce-289">XMPP/MTLS/TCP/23456</span><span class="sxs-lookup"><span data-stu-id="d04ce-289">XMPP/MTLS/TCP/23456</span></span></p></td>
<td><p><span data-ttu-id="d04ce-290">Любой</span><span class="sxs-lookup"><span data-stu-id="d04ce-290">Any</span></span></p></td>
<td><p><span data-ttu-id="d04ce-291">Каждый внутренний IP-адрес интерфейса пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="d04ce-291">Each internal Edge Server Interface IP</span></span></p></td>
<td><p><span data-ttu-id="d04ce-292">Внутренний IP-адрес XMPP, входящий в состав шлюза XMPP на сервере переднего плана или в пуле переднего плана, в адрес внутренней сети пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="d04ce-292">Internal XMPP traffic from the XMPP Gateway on the Front End Server or Front End pool to the Edge Server internal IP address or each Edge pool member’s internal IP address</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="d04ce-293">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d04ce-293">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

