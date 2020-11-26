---
title: 'Lync Server 2013: сводка по портам — масштабируемая консолидированная пограничная топология, балансировка нагрузки на DNS с закрытыми IP-адресами и трансляцией сетевых адресов'
description: 'Lync Server 2013: суммарный порт — масштабированный, поддерживая балансировку нагрузки DNS с частными IP-адресами с помощью NAT.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - Scaled consolidated edge, DNS load balancing with private IP addresses using NAT
ms:assetid: a296c2af-54d4-4b4f-9795-9191baf688cb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412756(v=OCS.15)
ms:contentKeyID: 48184955
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e0402b6682e86e5edf263fca78dfbe0f8fa070b4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424290"
---
# <a name="port-summary---scaled-consolidated-edge-dns-load-balancing-with-private-ip-addresses-using-nat-in-lync-server-2013"></a><span data-ttu-id="709ad-103">Сводка по портам — масштабируемая консолидированная пограничная топология, балансировка нагрузки на DNS с закрытыми IP-адресами и трансляцией сетевых адресов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="709ad-103">Port summary - Scaled consolidated edge, DNS load balancing with private IP addresses using NAT in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="709ad-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="709ad-104">

<span> </span></span></span>

<span data-ttu-id="709ad-105">_**Тема последнего изменения:** 2012-12-04_</span><span class="sxs-lookup"><span data-stu-id="709ad-105">_**Topic Last Modified:** 2012-12-04_</span></span>

<span data-ttu-id="709ad-106">Функция пограничного сервера Lync Server 2013, описанная в этой архитектуре сценариев, очень похожа на ту, что была реализована в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="709ad-106">The Lync Server 2013, Edge Server functionality described in this scenario architecture is very similar to what was implemented in Lync Server 2010.</span></span> <span data-ttu-id="709ad-107">Наиболее заметным дополнением является порт **5269 на TCP** для протокола расширенной обработки сообщений и присутствия (XMPP).</span><span class="sxs-lookup"><span data-stu-id="709ad-107">The most noticeable addition is the port **5269 over TCP** entry for the extensible messaging and presence protocol (XMPP).</span></span> <span data-ttu-id="709ad-108">Lync Server 2013 (при необходимости) можно развернуть прокси-сервер XMPP на пограничном или пограничном пуле, а также на сервере шлюзов XMPP на сервере переднего плана или в пуле внешних интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="709ad-108">Lync Server 2013 optionally deploys an XMPP proxy on the Edge Server or Edge pool and the XMPP gateway server on the Front End Server or Front End pool.</span></span>

<span data-ttu-id="709ad-109">В дополнение к протоколу IPv4, пограничный сервер теперь поддерживает IPv6.</span><span class="sxs-lookup"><span data-stu-id="709ad-109">In addition to IPv4, the Edge Server now supports IPv6.</span></span> <span data-ttu-id="709ad-110">Для ясности в сценариях используется только протокол IPv4.</span><span class="sxs-lookup"><span data-stu-id="709ad-110">For clarity, only IPv4 is used in the scenarios.</span></span>

<span data-ttu-id="709ad-111">**Корпоративная сеть периметра для масштабируемой консолидированной кромки с частными IP-адресами с помощью NAT**</span><span class="sxs-lookup"><span data-stu-id="709ad-111">**Enterprise perimeter network for scaled consolidated edge with private IP addresses using NAT**</span></span>

<span data-ttu-id="709ad-112">![96f5a8f5-16d2-464d-b86e-7c7ecfc89ead](images/JJ205394.96f5a8f5-16d2-464d-b86e-7c7ecfc89ead(OCS.15).jpg "96f5a8f5-16d2-464d-b86e-7c7ecfc89ead")</span><span class="sxs-lookup"><span data-stu-id="709ad-112">![96f5a8f5-16d2-464d-b86e-7c7ecfc89ead](images/JJ205394.96f5a8f5-16d2-464d-b86e-7c7ecfc89ead(OCS.15).jpg "96f5a8f5-16d2-464d-b86e-7c7ecfc89ead")</span></span>

<div>

## <a name="port-and-protocol-details"></a><span data-ttu-id="709ad-113">Сведения о портах и протоколах</span><span class="sxs-lookup"><span data-stu-id="709ad-113">Port and Protocol Details</span></span>

<span data-ttu-id="709ad-114">Рекомендуется открывать только порты, необходимые для поддержки функций, для которых предоставляется внешний доступ.</span><span class="sxs-lookup"><span data-stu-id="709ad-114">It is recommended that you open only the ports required to support the functionality for which you are providing external access.</span></span>

<span data-ttu-id="709ad-115">Для удаленного доступа к работе в любой службе пограничного сервера необходимо, чтобы трафик SIP был в направлении на один и тот же трафик по внешнему потоку, как показано на рисунке входящего и исходящего трафика пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="709ad-115">For remote access to work for any edge service, it is mandatory that SIP traffic is allowed to flow bi-directionally as shown in the Inbound/Outbound edge traffic figure.</span></span> <span data-ttu-id="709ad-116">Другими словами, Обмен сообщениями SIP и из службы Edge для Access осуществляется в обмене мгновенными сообщениями, присутствии, веб-конференциях, аудио-и видеосвязи (A/V) и Федерации.</span><span class="sxs-lookup"><span data-stu-id="709ad-116">Stated another way, the SIP messaging to and from the Access Edge service is involved in instant messaging (IM), presence, web conferencing, audio/video (A/V) and federation.</span></span>

### <a name="firewall-summary-for-scaled-consolidated-edge-dns-load-balancing-with-private-ip-addresses-using-nat-external-interface--node-1-and-node-2-example"></a><span data-ttu-id="709ad-117">Сводка по межсетевому экрану для масштабируемой консолидированной границы, балансировка нагрузки DNS с частными IP-адресами с использованием NAT: внешний интерфейс — узел 1 и узел 2 (пример).</span><span class="sxs-lookup"><span data-stu-id="709ad-117">Firewall Summary for Scaled Consolidated Edge, DNS Load Balancing with Private IP Addresses Using NAT: External Interface – Node 1 and Node 2 (Example)</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="709ad-118">Role/Protocol/TCP/UDP/порт</span><span class="sxs-lookup"><span data-stu-id="709ad-118">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="709ad-119">IP-адрес источника</span><span class="sxs-lookup"><span data-stu-id="709ad-119">Source IP address</span></span></th>
<th><span data-ttu-id="709ad-120">IP-адрес назначения</span><span class="sxs-lookup"><span data-stu-id="709ad-120">Destination IP address</span></span></th>
<th><span data-ttu-id="709ad-121">Примечания.</span><span class="sxs-lookup"><span data-stu-id="709ad-121">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="709ad-122">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="709ad-122">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="709ad-123">Любой</span><span class="sxs-lookup"><span data-stu-id="709ad-123">Any</span></span></p></td>
<td><p><span data-ttu-id="709ad-124">Прокси-служба XMPP (доступ к IP-адресу для общих ресурсов с помощью службы Edge Access)</span><span class="sxs-lookup"><span data-stu-id="709ad-124">XMPP Proxy service (shares IP address with Access Edge service)</span></span></p></td>
<td><p><span data-ttu-id="709ad-125">Прокси-служба XMPP принимает трафик от XMPP контактов в определенных XMPP федерациях.</span><span class="sxs-lookup"><span data-stu-id="709ad-125">XMPP Proxy service accepts traffic from XMPP contacts in defined XMPP federations</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="709ad-126">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="709ad-126">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="709ad-127">Прокси-служба XMPP (доступ к IP-адресу для общих ресурсов с помощью службы Edge Access)</span><span class="sxs-lookup"><span data-stu-id="709ad-127">XMPP Proxy service (shares IP address with Access Edge service)</span></span></p></td>
<td><p><span data-ttu-id="709ad-128">Любой</span><span class="sxs-lookup"><span data-stu-id="709ad-128">Any</span></span></p></td>
<td><p><span data-ttu-id="709ad-129">Служба прокси XMPP отправляет трафик на XMPPные контакты в определенных XMPP Федерации</span><span class="sxs-lookup"><span data-stu-id="709ad-129">XMPP Proxy service sends traffic to XMPP contacts in defined XMPP federations</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="709ad-130">Access/HTTP/TCP/80</span><span class="sxs-lookup"><span data-stu-id="709ad-130">Access/HTTP/TCP/80</span></span></p></td>
<td><p><span data-ttu-id="709ad-131">Служба пограничного доступа к пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="709ad-131">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="709ad-132">Любой</span><span class="sxs-lookup"><span data-stu-id="709ad-132">Any</span></span></p></td>
<td><p><span data-ttu-id="709ad-133">Проверка отзыва сертификатов и получения CRL</span><span class="sxs-lookup"><span data-stu-id="709ad-133">Certificate revocation/CRL check and retrieval</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="709ad-134">Access/DNS/TCP/53</span><span class="sxs-lookup"><span data-stu-id="709ad-134">Access/DNS/TCP/53</span></span></p></td>
<td><p><span data-ttu-id="709ad-135">Служба пограничного доступа к пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="709ad-135">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="709ad-136">Любой</span><span class="sxs-lookup"><span data-stu-id="709ad-136">Any</span></span></p></td>
<td><p><span data-ttu-id="709ad-137">Запрос DNS по протоколу TCP</span><span class="sxs-lookup"><span data-stu-id="709ad-137">DNS query over TCP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="709ad-138">Access/DNS/UDP/53</span><span class="sxs-lookup"><span data-stu-id="709ad-138">Access/DNS/UDP/53</span></span></p></td>
<td><p><span data-ttu-id="709ad-139">Служба пограничного доступа к пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="709ad-139">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="709ad-140">Любой</span><span class="sxs-lookup"><span data-stu-id="709ad-140">Any</span></span></p></td>
<td><p><span data-ttu-id="709ad-141">Запрос DNS по протоколу UDP</span><span class="sxs-lookup"><span data-stu-id="709ad-141">DNS query over UDP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="709ad-142">Access/SIP (TLS)/TCP/443</span><span class="sxs-lookup"><span data-stu-id="709ad-142">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="709ad-143">Любой</span><span class="sxs-lookup"><span data-stu-id="709ad-143">Any</span></span></p></td>
<td><p><span data-ttu-id="709ad-144">Служба пограничного доступа к пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="709ad-144">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="709ad-145">Трафик SIP "клиент-сервер" для доступа внешних пользователей</span><span class="sxs-lookup"><span data-stu-id="709ad-145">Client-to-server SIP traffic for external user access</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="709ad-146">Access/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="709ad-146">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="709ad-147">Любой</span><span class="sxs-lookup"><span data-stu-id="709ad-147">Any</span></span></p></td>
<td><p><span data-ttu-id="709ad-148">Служба пограничного доступа к пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="709ad-148">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="709ad-149">Для Федеративной и общедоступной службы обмена мгновенными сообщениями с помощью SIP</span><span class="sxs-lookup"><span data-stu-id="709ad-149">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="709ad-150">Access/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="709ad-150">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="709ad-151">Служба пограничного доступа к пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="709ad-151">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="709ad-152">Любой</span><span class="sxs-lookup"><span data-stu-id="709ad-152">Any</span></span></p></td>
<td><p><span data-ttu-id="709ad-153">Для Федеративной и общедоступной службы обмена мгновенными сообщениями с помощью SIP</span><span class="sxs-lookup"><span data-stu-id="709ad-153">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="709ad-154">Веб-конференции/PSOM (TLS)/TCP/443</span><span class="sxs-lookup"><span data-stu-id="709ad-154">Web Conferencing/PSOM(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="709ad-155">Любой</span><span class="sxs-lookup"><span data-stu-id="709ad-155">Any</span></span></p></td>
<td><p><span data-ttu-id="709ad-156">Служба веб-конференций пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="709ad-156">Edge Server Web Conferencing Edge service</span></span></p></td>
<td><p><span data-ttu-id="709ad-157">Мультимедиа для веб-конференций</span><span class="sxs-lookup"><span data-stu-id="709ad-157">Web Conferencing media</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="709ad-158">A/V/RTP/TCP/50000-59,999</span><span class="sxs-lookup"><span data-stu-id="709ad-158">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="709ad-159">Служба Edge для пограничного сервера A/V</span><span class="sxs-lookup"><span data-stu-id="709ad-159">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="709ad-160">Любой</span><span class="sxs-lookup"><span data-stu-id="709ad-160">Any</span></span></p></td>
<td><p><span data-ttu-id="709ad-161">Требуется для Федерации с партнерами, работающими под управлением Office Communications Server 2007, Office Communications Server 2007 R2, Lync Server 2010 и Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="709ad-161">Required for federating with partners running Office Communications Server 2007, Office Communications Server 2007 R2, Lync Server 2010 and Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="709ad-162">A/V/RTP/UDP/50000-59,999</span><span class="sxs-lookup"><span data-stu-id="709ad-162">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="709ad-163">Служба Edge для пограничного сервера A/V</span><span class="sxs-lookup"><span data-stu-id="709ad-163">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="709ad-164">Любой</span><span class="sxs-lookup"><span data-stu-id="709ad-164">Any</span></span></p></td>
<td><p><span data-ttu-id="709ad-165">Требуется только для Федерации с партнерами, работающими под управлением Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="709ad-165">Required only for federation with partners running Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="709ad-166">A/V/RTP/TCP/50000-59,999</span><span class="sxs-lookup"><span data-stu-id="709ad-166">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="709ad-167">Любой</span><span class="sxs-lookup"><span data-stu-id="709ad-167">Any</span></span></p></td>
<td><p><span data-ttu-id="709ad-168">Служба Edge для пограничного сервера A/V</span><span class="sxs-lookup"><span data-stu-id="709ad-168">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="709ad-169">Требуется только для Федерации с партнерами, работающими под управлением Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="709ad-169">Required only for federation with partners running Office Communications Server 2007</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="709ad-170">A/V/RTP/UDP/50000-59,999</span><span class="sxs-lookup"><span data-stu-id="709ad-170">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="709ad-171">Любой</span><span class="sxs-lookup"><span data-stu-id="709ad-171">Any</span></span></p></td>
<td><p><span data-ttu-id="709ad-172">Служба Edge для пограничного сервера A/V</span><span class="sxs-lookup"><span data-stu-id="709ad-172">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="709ad-173">Требуется только для Федерации с партнерами, работающими под управлением Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="709ad-173">Required only for federation with partners running Office Communications Server 2007</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="709ad-174">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="709ad-174">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="709ad-175">Служба Edge для пограничного сервера A/V</span><span class="sxs-lookup"><span data-stu-id="709ad-175">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="709ad-176">Любой</span><span class="sxs-lookup"><span data-stu-id="709ad-176">Any</span></span></p></td>
<td><p><span data-ttu-id="709ad-177">3478 Outbound используется для определения версии пограничного сервера, с которым обменивается данными Lync Server, а также для мультимедийного трафика от пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="709ad-177">3478 outbound is used to determine the version of Edge Server that Lync Server is communicating with and also for media traffic from Edge Server-to-Edge Server.</span></span> <span data-ttu-id="709ad-178">Требуется для Федерации с Lync Server 2010, Windows Live Messenger и Office Communications Server 2007 R2, а также в том случае, если в компании развернуты несколько пулов Edge.</span><span class="sxs-lookup"><span data-stu-id="709ad-178">Required for federation with Lync Server 2010, Windows Live Messenger, and Office Communications Server 2007 R2, and also if multiple Edge pools are deployed within a company.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="709ad-179">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="709ad-179">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="709ad-180">Любой</span><span class="sxs-lookup"><span data-stu-id="709ad-180">Any</span></span></p></td>
<td><p><span data-ttu-id="709ad-181">Служба Edge для пограничного сервера A/V</span><span class="sxs-lookup"><span data-stu-id="709ad-181">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="709ad-182">STUN/отключите согласование кандидатов по протоколу UDP/3478</span><span class="sxs-lookup"><span data-stu-id="709ad-182">STUN/TURN negotiation of candidates over UDP/3478</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="709ad-183">A/V/STUN, MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="709ad-183">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="709ad-184">Любой</span><span class="sxs-lookup"><span data-stu-id="709ad-184">Any</span></span></p></td>
<td><p><span data-ttu-id="709ad-185">Служба Edge для пограничного сервера A/V</span><span class="sxs-lookup"><span data-stu-id="709ad-185">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="709ad-186">STUN/отключите согласование кандидатов по протоколу TCP/443</span><span class="sxs-lookup"><span data-stu-id="709ad-186">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="709ad-187">A/V/STUN, MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="709ad-187">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="709ad-188">Служба Edge для пограничного сервера A/V</span><span class="sxs-lookup"><span data-stu-id="709ad-188">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="709ad-189">Любой</span><span class="sxs-lookup"><span data-stu-id="709ad-189">Any</span></span></p></td>
<td><p><span data-ttu-id="709ad-190">STUN/отключите согласование кандидатов по протоколу TCP/443</span><span class="sxs-lookup"><span data-stu-id="709ad-190">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="firewall-summary-for-scaled-consolidated-edge-dns-load-balancing-with-private-ip-addresses-using-nat-internal-interface--node-1-and-node-2-example"></a><span data-ttu-id="709ad-191">Сводка по межсетевому экрану для масштабируемой консолидированной границы, балансировки нагрузки DNS с частными IP-адресами с использованием NAT: внутренний интерфейс — узел 1 и узел 2 (пример)</span><span class="sxs-lookup"><span data-stu-id="709ad-191">Firewall Summary for Scaled Consolidated Edge, DNS Load Balancing with Private IP Addresses Using NAT: Internal Interface – Node 1 and Node 2 (Example)</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="709ad-192">Протокол/TCP или UDP/порт</span><span class="sxs-lookup"><span data-stu-id="709ad-192">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="709ad-193">IP-адрес источника</span><span class="sxs-lookup"><span data-stu-id="709ad-193">Source IP address</span></span></th>
<th><span data-ttu-id="709ad-194">IP-адрес назначения</span><span class="sxs-lookup"><span data-stu-id="709ad-194">Destination IP address</span></span></th>
<th><span data-ttu-id="709ad-195">Комментарии</span><span class="sxs-lookup"><span data-stu-id="709ad-195">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="709ad-196">XMPP/MTLS/TCP/23456</span><span class="sxs-lookup"><span data-stu-id="709ad-196">XMPP/MTLS/TCP/23456</span></span></p></td>
<td><p><span data-ttu-id="709ad-197">Any (может быть определено как адрес сервера переднего плана или IP-адрес пула переднего плана, на котором запущена служба шлюза XMPP)</span><span class="sxs-lookup"><span data-stu-id="709ad-197">Any (can be defined as Front End Server address, or Front End pool IP address running the XMPP Gateway service)</span></span></p></td>
<td><p><span data-ttu-id="709ad-198">IP-адрес внутреннего интерфейса пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="709ad-198">Edge Server internal interface IP address</span></span></p></td>
<td><p><span data-ttu-id="709ad-199">Исходящий трафик XMPP от службы шлюза XMPP, работающей на сервере переднего плана или в пуле внешних интерфейсов</span><span class="sxs-lookup"><span data-stu-id="709ad-199">Outbound XMPP traffic from XMPP Gateway service running on Front End Server or Front End pool</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="709ad-200">SIP/MTLS/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="709ad-200">SIP/MTLS/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="709ad-201">Any (может быть определено как режиссер, IP-адрес пула режиссера, сервер клиентского доступа или IP-адрес пула переднего плана)</span><span class="sxs-lookup"><span data-stu-id="709ad-201">Any (can be defined as Director, Director pool IP address, Front End Server or Front End pool IP address)</span></span></p></td>
<td><p><span data-ttu-id="709ad-202">Внутренний интерфейс пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="709ad-202">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="709ad-203">Исходящий трафик SIP (от режиссера, IP-адреса пула, сервера переднего плана или IP-адреса пула переднего плана) к внутреннему интерфейсу пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="709ad-203">Outbound SIP traffic (from Director, Director pool IP address, Front End Server or Front End pool IP address) to Edge Server internal interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="709ad-204">SIP/MTLS/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="709ad-204">SIP/MTLS/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="709ad-205">Внутренний интерфейс пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="709ad-205">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="709ad-206">Any (может быть определено как режиссер, IP-адрес пула режиссера, сервер клиентского доступа или IP-адрес пула переднего плана)</span><span class="sxs-lookup"><span data-stu-id="709ad-206">Any (can be defined as Director, Director pool IP address, Front End Server or Front End pool IP address)</span></span></p></td>
<td><p><span data-ttu-id="709ad-207">Входящий трафик SIP (для режиссера, IP-адреса пула, сервера переднего плана или IP-адреса пула переднего плана) от внутреннего интерфейса пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="709ad-207">Inbound SIP traffic (to Director, Director pool IP address, Front End Server or Front End pool IP address) from Edge Server internal interface</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="709ad-208">PSOM/MTLS/TCP/8057</span><span class="sxs-lookup"><span data-stu-id="709ad-208">PSOM/MTLS/TCP/8057</span></span></p></td>
<td><p><span data-ttu-id="709ad-209">Any (может быть IP-адресом сервера переднего плана или IP-адресом серверного переднего плана в пуле переднего плана)</span><span class="sxs-lookup"><span data-stu-id="709ad-209">Any (can be defined as Front End Server IP address, or each Front End Server IP address in a Front End pool)</span></span></p></td>
<td><p><span data-ttu-id="709ad-210">Внутренний интерфейс пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="709ad-210">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="709ad-211">Трафик веб-конференций от сервера переднего плана или каждого серверного переднего плана, если он находится в пуле и является внутренним интерфейсом пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="709ad-211">Web conferencing traffic from Front End Server or each Front End Server if in a pool, to Edge Server internal interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="709ad-212">SIP/MTLS/TCP/5062</span><span class="sxs-lookup"><span data-stu-id="709ad-212">SIP/MTLS/TCP/5062</span></span></p></td>
<td><p><span data-ttu-id="709ad-213">Any (может быть как IP-адресом переднего сервера, так и IP-адресом пула переднего плана либо любым бесперебойно работающее устройство филиала или с помощью этого пограничного сервера).</span><span class="sxs-lookup"><span data-stu-id="709ad-213">Any (can be defined as Front End Server IP address, or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server)</span></span></p></td>
<td><p><span data-ttu-id="709ad-214">Внутренний интерфейс пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="709ad-214">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="709ad-215">Проверка подлинности пользователей/V (служба проверки подлинности A/V) от IP-адреса сервера переднего плана или переднего плана, а также от любого работающего филиала или сервера с бесперебойной подразделением с помощью этого пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="709ad-215">Authentication of A/V users (A/V authentication service) from Front End Server or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="709ad-216">STUN/MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="709ad-216">STUN/MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="709ad-217">Любой</span><span class="sxs-lookup"><span data-stu-id="709ad-217">Any</span></span></p></td>
<td><p><span data-ttu-id="709ad-218">Внутренний интерфейс пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="709ad-218">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="709ad-219">Предпочтительный путь для передачи мультимедиа между внутренними и внешними пользователями, бесперебойно работающем устройстве филиалов или бесперебойно работающем сервере филиала</span><span class="sxs-lookup"><span data-stu-id="709ad-219">Preferred path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="709ad-220">STUN/MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="709ad-220">STUN/MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="709ad-221">Любой</span><span class="sxs-lookup"><span data-stu-id="709ad-221">Any</span></span></p></td>
<td><p><span data-ttu-id="709ad-222">Внутренний интерфейс пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="709ad-222">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="709ad-223">Резервный путь для передачи мультимедиа между внутренними и внешними пользователями, бесперебойно работающее устройство филиала или бесперебойный сервер филиала, если не удается установить UDP-связь, используется протокол TCP для обмена файлами и демонстрации рабочего стола</span><span class="sxs-lookup"><span data-stu-id="709ad-223">Fallback path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server if UDP communication cannot be established, TCP is used for file transfer and desktop sharing</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="709ad-224">HTTPS/TCP/4443</span><span class="sxs-lookup"><span data-stu-id="709ad-224">HTTPS/TCP/4443</span></span></p></td>
<td><p><span data-ttu-id="709ad-225">Any (может быть указан в качестве IP-адреса сервера переднего плана или пула, содержащего центральное хранилище управления).</span><span class="sxs-lookup"><span data-stu-id="709ad-225">Any (can be defined as the Front End Server IP address, or pool that holds the Central Management store)</span></span></p></td>
<td><p><span data-ttu-id="709ad-226">Внутренний интерфейс пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="709ad-226">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="709ad-227">Репликация изменений из хранилища центрального управления на пограничный сервер</span><span class="sxs-lookup"><span data-stu-id="709ad-227">Replication of changes from the Central Management store to the Edge Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="709ad-228">MTLS/TCP/50001</span><span class="sxs-lookup"><span data-stu-id="709ad-228">MTLS/TCP/50001</span></span></p></td>
<td><p><span data-ttu-id="709ad-229">Любой</span><span class="sxs-lookup"><span data-stu-id="709ad-229">Any</span></span></p></td>
<td><p><span data-ttu-id="709ad-230">Внутренний интерфейс пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="709ad-230">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="709ad-231">Централизованное ведение журналов, использование команд командной строки Lync Server Management Shell и централизованной службы ведения журналов, команды ClsController (ClsController.exe) или агента (ClsAgent.exe) и коллекции журналов</span><span class="sxs-lookup"><span data-stu-id="709ad-231">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="709ad-232">MTLS/TCP/50002</span><span class="sxs-lookup"><span data-stu-id="709ad-232">MTLS/TCP/50002</span></span></p></td>
<td><p><span data-ttu-id="709ad-233">Любой</span><span class="sxs-lookup"><span data-stu-id="709ad-233">Any</span></span></p></td>
<td><p><span data-ttu-id="709ad-234">Внутренний интерфейс пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="709ad-234">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="709ad-235">Централизованное ведение журналов, использование команд командной строки Lync Server Management Shell и централизованной службы ведения журналов, команды ClsController (ClsController.exe) или агента (ClsAgent.exe) и коллекции журналов</span><span class="sxs-lookup"><span data-stu-id="709ad-235">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="709ad-236">MTLS/TCP/50003</span><span class="sxs-lookup"><span data-stu-id="709ad-236">MTLS/TCP/50003</span></span></p></td>
<td><p><span data-ttu-id="709ad-237">Любой</span><span class="sxs-lookup"><span data-stu-id="709ad-237">Any</span></span></p></td>
<td><p><span data-ttu-id="709ad-238">Внутренний интерфейс пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="709ad-238">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="709ad-239">Централизованное ведение журналов, использование команд командной строки Lync Server Management Shell и централизованной службы ведения журналов, команды ClsController (ClsController.exe) или агента (ClsAgent.exe) и коллекции журналов</span><span class="sxs-lookup"><span data-stu-id="709ad-239">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary-for-federation"></a><span data-ttu-id="709ad-240">Сводка по межсетевому экрану для Федерации</span><span class="sxs-lookup"><span data-stu-id="709ad-240">Firewall Summary for Federation</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="709ad-241">Role/Protocol/TCP/UDP/порт</span><span class="sxs-lookup"><span data-stu-id="709ad-241">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="709ad-242">IP-адрес источника</span><span class="sxs-lookup"><span data-stu-id="709ad-242">Source IP address</span></span></th>
<th><span data-ttu-id="709ad-243">IP-адрес назначения</span><span class="sxs-lookup"><span data-stu-id="709ad-243">Destination IP address</span></span></th>
<th><span data-ttu-id="709ad-244">Примечания.</span><span class="sxs-lookup"><span data-stu-id="709ad-244">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="709ad-245">Access/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="709ad-245">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="709ad-246">Общедоступный IP-адрес службы пограничного доступа</span><span class="sxs-lookup"><span data-stu-id="709ad-246">Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="709ad-247">Любой</span><span class="sxs-lookup"><span data-stu-id="709ad-247">Any</span></span></p></td>
<td><p><span data-ttu-id="709ad-248">Для Федеративной и общедоступной службы обмена мгновенными сообщениями с помощью SIP</span><span class="sxs-lookup"><span data-stu-id="709ad-248">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary--public-instant-messaging-connectivity"></a><span data-ttu-id="709ad-249">Сводка по брандмауэрам: общедоступная служба обмена мгновенными сообщениями</span><span class="sxs-lookup"><span data-stu-id="709ad-249">Firewall Summary – Public Instant Messaging Connectivity</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="709ad-250">Role/Protocol/TCP/UDP/порт</span><span class="sxs-lookup"><span data-stu-id="709ad-250">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="709ad-251">IP-адрес источника</span><span class="sxs-lookup"><span data-stu-id="709ad-251">Source IP address</span></span></th>
<th><span data-ttu-id="709ad-252">IP-адрес назначения</span><span class="sxs-lookup"><span data-stu-id="709ad-252">Destination IP address</span></span></th>
<th><span data-ttu-id="709ad-253">Примечания.</span><span class="sxs-lookup"><span data-stu-id="709ad-253">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="709ad-254">Access/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="709ad-254">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="709ad-255">Партнеры по подключению общедоступных мгновенных сообщений</span><span class="sxs-lookup"><span data-stu-id="709ad-255">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="709ad-256">Служба пограничного доступа к пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="709ad-256">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="709ad-257">Для Федеративной и общедоступной службы обмена мгновенными сообщениями с помощью SIP</span><span class="sxs-lookup"><span data-stu-id="709ad-257">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="709ad-258">Access/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="709ad-258">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="709ad-259">Служба пограничного доступа к пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="709ad-259">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="709ad-260">Партнеры по подключению общедоступных мгновенных сообщений</span><span class="sxs-lookup"><span data-stu-id="709ad-260">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="709ad-261">Для Федеративной и общедоступной службы обмена мгновенными сообщениями с помощью SIP</span><span class="sxs-lookup"><span data-stu-id="709ad-261">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="709ad-262">Access/SIP (TLS)/TCP/443</span><span class="sxs-lookup"><span data-stu-id="709ad-262">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="709ad-263">Клиенты</span><span class="sxs-lookup"><span data-stu-id="709ad-263">Clients</span></span></p></td>
<td><p><span data-ttu-id="709ad-264">Служба пограничного доступа к пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="709ad-264">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="709ad-265">Трафик SIP "клиент-сервер" для доступа внешних пользователей</span><span class="sxs-lookup"><span data-stu-id="709ad-265">Client-to-server SIP traffic for external user access</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="709ad-266">A/V/RTP/TCP/50000-59,999</span><span class="sxs-lookup"><span data-stu-id="709ad-266">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="709ad-267">Служба Edge для пограничного сервера A/V</span><span class="sxs-lookup"><span data-stu-id="709ad-267">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="709ad-268">Клиенты Live Messenger</span><span class="sxs-lookup"><span data-stu-id="709ad-268">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="709ad-269">Используется для сеансов обмена мгновенными сообщениями с помощью Windows Live Messenger, если настроена служба общего доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="709ad-269">Used for A/V sessions with Windows Live Messenger if public IM connectivity is configured.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="709ad-270">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="709ad-270">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="709ad-271">Служба Edge для пограничного сервера A/V</span><span class="sxs-lookup"><span data-stu-id="709ad-271">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="709ad-272">Клиенты Live Messenger</span><span class="sxs-lookup"><span data-stu-id="709ad-272">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="709ad-273">Требуется для общедоступной службы обмена мгновенными сообщениями в Windows Live Messenger</span><span class="sxs-lookup"><span data-stu-id="709ad-273">Required for public IM connectivity with Windows Live Messenger</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="709ad-274">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="709ad-274">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="709ad-275">Клиенты Live Messenger</span><span class="sxs-lookup"><span data-stu-id="709ad-275">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="709ad-276">Служба Edge для пограничного сервера A/V</span><span class="sxs-lookup"><span data-stu-id="709ad-276">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="709ad-277">Требуется для общедоступной службы обмена мгновенными сообщениями в Windows Live Messenger</span><span class="sxs-lookup"><span data-stu-id="709ad-277">Required for public IM connectivity with Windows Live Messenger</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary-for-extensible-messaging-and-presence-protocol"></a><span data-ttu-id="709ad-278">Сводка брандмауэра по протоколу расширенного обмена сообщениями и присутствия</span><span class="sxs-lookup"><span data-stu-id="709ad-278">Firewall Summary for Extensible Messaging and Presence Protocol</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="709ad-279">Протокол/TCP или UDP/порт</span><span class="sxs-lookup"><span data-stu-id="709ad-279">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="709ad-280">Источник (IP-адрес)</span><span class="sxs-lookup"><span data-stu-id="709ad-280">Source (IP address)</span></span></th>
<th><span data-ttu-id="709ad-281">Назначение (IP-адрес)</span><span class="sxs-lookup"><span data-stu-id="709ad-281">Destination (IP address)</span></span></th>
<th><span data-ttu-id="709ad-282">Комментарии</span><span class="sxs-lookup"><span data-stu-id="709ad-282">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="709ad-283">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="709ad-283">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="709ad-284">Любой</span><span class="sxs-lookup"><span data-stu-id="709ad-284">Any</span></span></p></td>
<td><p><span data-ttu-id="709ad-285">IP-адрес интерфейса службы пограничного доступа к серверу Edge</span><span class="sxs-lookup"><span data-stu-id="709ad-285">Edge Server Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="709ad-286">Стандартный коммуникационный порт "сервер-сервер" для XMPP.</span><span class="sxs-lookup"><span data-stu-id="709ad-286">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="709ad-287">Разрешает связь с прокси-сервером пограничного сервера XMPP от федеративных XMPP партнеров</span><span class="sxs-lookup"><span data-stu-id="709ad-287">Allows communication to the Edge Server XMPP proxy from federated XMPP partners</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="709ad-288">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="709ad-288">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="709ad-289">IP-адрес интерфейса службы пограничного доступа к серверу Edge</span><span class="sxs-lookup"><span data-stu-id="709ad-289">Edge Server Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="709ad-290">Любой</span><span class="sxs-lookup"><span data-stu-id="709ad-290">Any</span></span></p></td>
<td><p><span data-ttu-id="709ad-291">Стандартный коммуникационный порт "сервер-сервер" для XMPP.</span><span class="sxs-lookup"><span data-stu-id="709ad-291">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="709ad-292">Разрешает взаимодействие с XMPP прокси-сервером для федеративных XMPP партнеров</span><span class="sxs-lookup"><span data-stu-id="709ad-292">Allows communication from the Edge Server XMPP proxy to federated XMPP partners</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="709ad-293">XMPP/MTLS/TCP/23456</span><span class="sxs-lookup"><span data-stu-id="709ad-293">XMPP/MTLS/TCP/23456</span></span></p></td>
<td><p><span data-ttu-id="709ad-294">Любой</span><span class="sxs-lookup"><span data-stu-id="709ad-294">Any</span></span></p></td>
<td><p><span data-ttu-id="709ad-295">Каждый внутренний IP-адрес интерфейса пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="709ad-295">Each internal Edge Server interface IP</span></span></p></td>
<td><p><span data-ttu-id="709ad-296">Внутренний IP-адрес XMPP, входящий в состав шлюза XMPP на сервере переднего плана или в пуле переднего плана, в адрес внутренней сети пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="709ad-296">Internal XMPP traffic from the XMPP Gateway on the Front End Server or Front End pool to the Edge Server internal IP address or each Edge pool member’s internal IP address</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="709ad-297">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="709ad-297">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

