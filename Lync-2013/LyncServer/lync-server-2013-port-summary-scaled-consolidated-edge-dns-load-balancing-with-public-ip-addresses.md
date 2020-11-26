---
title: 'Lync Server 2013: сводка по портам — масштабируемая консолидированная пограничная топология, балансировка нагрузки на DNS с общедоступными IP-адресами'
description: 'Lync Server 2013: масштабированный Объединенный край, балансировка нагрузки DNS с общедоступными IP-адресами.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - Scaled consolidated edge, DNS load balancing with public IP addresses
ms:assetid: f7cbd0f1-841d-4116-8d17-e9d991daa4a8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205394(v=OCS.15)
ms:contentKeyID: 48185865
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8090435485b4b6a183702a608b139cec91ae26a7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446341"
---
# <a name="port-summary---scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses-in-lync-server-2013"></a><span data-ttu-id="163ae-103">Сводка по портам — масштабируемая консолидированная пограничная топология, балансировка нагрузки на DNS с общедоступными IP-адресами в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="163ae-103">Port summary - Scaled consolidated edge, DNS load balancing with public IP addresses in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="163ae-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="163ae-104">

<span> </span></span></span>

<span data-ttu-id="163ae-105">_**Тема последнего изменения:** 2013-04-03_</span><span class="sxs-lookup"><span data-stu-id="163ae-105">_**Topic Last Modified:** 2013-04-03_</span></span>

<span data-ttu-id="163ae-106">Функция пограничного сервера Lync Server 2013, описанная в этой архитектуре сценариев, очень похожа на ту, что была реализована в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="163ae-106">The Lync Server 2013, Edge Server functionality described in this scenario architecture is very similar to what was implemented in Lync Server 2010.</span></span> <span data-ttu-id="163ae-107">Наиболее заметным дополнением является порт **5269 на TCP** для протокола расширенной обработки сообщений и присутствия (XMPP).</span><span class="sxs-lookup"><span data-stu-id="163ae-107">The most noticeable addition is the port **5269 over TCP** entry for the extensible messaging and presence protocol (XMPP).</span></span> <span data-ttu-id="163ae-108">Lync Server 2013 (при необходимости) можно развернуть прокси-сервер XMPP на пограничном или пограничном пуле, а также на сервере шлюзов XMPP на сервере переднего плана или в пуле внешних интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="163ae-108">Lync Server 2013 optionally deploys an XMPP proxy on the Edge Server or Edge pool and the XMPP gateway server on the Front End Server or Front End pool.</span></span>

<span data-ttu-id="163ae-109">В дополнение к протоколу IPv4, пограничный сервер теперь поддерживает IPv6.</span><span class="sxs-lookup"><span data-stu-id="163ae-109">In addition to IPv4, the Edge Server now supports IPv6.</span></span> <span data-ttu-id="163ae-110">Для ясности в сценариях используется только протокол IPv4.</span><span class="sxs-lookup"><span data-stu-id="163ae-110">For clarity, only IPv4 is used in the scenarios.</span></span>

<span data-ttu-id="163ae-111">**Корпоративная сеть периметра для масштабируемых консолидированных кромок, балансировка нагрузки DNS с общедоступными IP-адресами**</span><span class="sxs-lookup"><span data-stu-id="163ae-111">**Enterprise perimeter network for Scaled Consolidated Edge, DNS Load Balancing with Public IP Addresses**</span></span>

<span data-ttu-id="163ae-112">![96f5a8f5-16d2-464d-b86e-7c7ecfc89ead](images/JJ205394.96f5a8f5-16d2-464d-b86e-7c7ecfc89ead(OCS.15).jpg "96f5a8f5-16d2-464d-b86e-7c7ecfc89ead")</span><span class="sxs-lookup"><span data-stu-id="163ae-112">![96f5a8f5-16d2-464d-b86e-7c7ecfc89ead](images/JJ205394.96f5a8f5-16d2-464d-b86e-7c7ecfc89ead(OCS.15).jpg "96f5a8f5-16d2-464d-b86e-7c7ecfc89ead")</span></span>

<div>

## <a name="port-and-protocol-details"></a><span data-ttu-id="163ae-113">Сведения о портах и протоколах</span><span class="sxs-lookup"><span data-stu-id="163ae-113">Port and Protocol Details</span></span>

<span data-ttu-id="163ae-114">Рекомендуется открывать только порты, необходимые для поддержки функций, для которых предоставляется внешний доступ.</span><span class="sxs-lookup"><span data-stu-id="163ae-114">It is recommended that you open only the ports required to support the functionality for which you are providing external access.</span></span>

<span data-ttu-id="163ae-115">Для удаленного доступа к работе в любой службе пограничного сервера необходимо, чтобы трафик SIP был в направлении на один и тот же трафик по внешнему потоку, как показано на рисунке входящего и исходящего трафика пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="163ae-115">For remote access to work for any edge service, it is mandatory that SIP traffic is allowed to flow bi-directionally as shown in the Inbound/Outbound edge traffic figure.</span></span> <span data-ttu-id="163ae-116">Другими словами, Обмен сообщениями SIP и из службы Edge для Access осуществляется в обмене мгновенными сообщениями, присутствии, веб-конференциях, аудио-и видеосвязи (A/V) и Федерации.</span><span class="sxs-lookup"><span data-stu-id="163ae-116">Stated another way, the SIP messaging to and from the Access Edge service is involved in instant messaging (IM), presence, web conferencing, audio/video (A/V) and federation.</span></span>

### <a name="firewall-summary-for-scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses-external-interface--node-1-and-node-2-example"></a><span data-ttu-id="163ae-117">Сводка по межсетевому экрану для масштабируемой консолидированной границы, балансировка нагрузки DNS с общедоступными IP-адресами: внешний интерфейс — узел 1 и узел 2 (пример)</span><span class="sxs-lookup"><span data-stu-id="163ae-117">Firewall Summary for Scaled Consolidated Edge, DNS Load Balancing with Public IP Addresses: External Interface – Node 1 and Node 2 (Example)</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="163ae-118">Role/Protocol/TCP/UDP/порт</span><span class="sxs-lookup"><span data-stu-id="163ae-118">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="163ae-119">IP-адрес источника</span><span class="sxs-lookup"><span data-stu-id="163ae-119">Source IP address</span></span></th>
<th><span data-ttu-id="163ae-120">IP-адрес назначения</span><span class="sxs-lookup"><span data-stu-id="163ae-120">Destination IP address</span></span></th>
<th><span data-ttu-id="163ae-121">Примечания.</span><span class="sxs-lookup"><span data-stu-id="163ae-121">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="163ae-122">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="163ae-122">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="163ae-123">Любой</span><span class="sxs-lookup"><span data-stu-id="163ae-123">Any</span></span></p></td>
<td><p><span data-ttu-id="163ae-124">Прокси-служба XMPP (доступ к IP-адресу для общих ресурсов с помощью службы Edge Access)</span><span class="sxs-lookup"><span data-stu-id="163ae-124">XMPP Proxy service (shares IP address with Access Edge service)</span></span></p></td>
<td><p><span data-ttu-id="163ae-125">Прокси-служба XMPP принимает трафик от XMPP контактов в определенных XMPP федерациях.</span><span class="sxs-lookup"><span data-stu-id="163ae-125">XMPP Proxy service accepts traffic from XMPP contacts in defined XMPP federations</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="163ae-126">Access/HTTP/TCP/80</span><span class="sxs-lookup"><span data-stu-id="163ae-126">Access/HTTP/TCP/80</span></span></p></td>
<td><p><span data-ttu-id="163ae-127">Пограничный сервер, общедоступный IP-адрес пограничной службы доступа</span><span class="sxs-lookup"><span data-stu-id="163ae-127">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="163ae-128">Любой</span><span class="sxs-lookup"><span data-stu-id="163ae-128">Any</span></span></p></td>
<td><p><span data-ttu-id="163ae-129">Проверка отзыва сертификатов и получения CRL</span><span class="sxs-lookup"><span data-stu-id="163ae-129">Certificate revocation/CRL check and retrieval</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="163ae-130">Access/DNS/TCP/53</span><span class="sxs-lookup"><span data-stu-id="163ae-130">Access/DNS/TCP/53</span></span></p></td>
<td><p><span data-ttu-id="163ae-131">Пограничный сервер, общедоступный IP-адрес пограничной службы доступа</span><span class="sxs-lookup"><span data-stu-id="163ae-131">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="163ae-132">Любой</span><span class="sxs-lookup"><span data-stu-id="163ae-132">Any</span></span></p></td>
<td><p><span data-ttu-id="163ae-133">Запрос DNS по протоколу TCP</span><span class="sxs-lookup"><span data-stu-id="163ae-133">DNS query over TCP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="163ae-134">Access/DNS/UDP/53</span><span class="sxs-lookup"><span data-stu-id="163ae-134">Access/DNS/UDP/53</span></span></p></td>
<td><p><span data-ttu-id="163ae-135">Пограничный сервер, общедоступный IP-адрес пограничной службы доступа</span><span class="sxs-lookup"><span data-stu-id="163ae-135">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="163ae-136">Любой</span><span class="sxs-lookup"><span data-stu-id="163ae-136">Any</span></span></p></td>
<td><p><span data-ttu-id="163ae-137">Запрос DNS по протоколу UDP</span><span class="sxs-lookup"><span data-stu-id="163ae-137">DNS query over UDP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="163ae-138">Access/SIP (TLS)/TCP/443</span><span class="sxs-lookup"><span data-stu-id="163ae-138">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="163ae-139">Любой</span><span class="sxs-lookup"><span data-stu-id="163ae-139">Any</span></span></p></td>
<td><p><span data-ttu-id="163ae-140">Пограничный сервер, общедоступный IP-адрес пограничной службы доступа</span><span class="sxs-lookup"><span data-stu-id="163ae-140">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="163ae-141">Трафик SIP "клиент-сервер" для доступа внешних пользователей</span><span class="sxs-lookup"><span data-stu-id="163ae-141">Client-to-server SIP traffic for external user access</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="163ae-142">Access/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="163ae-142">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="163ae-143">Любой</span><span class="sxs-lookup"><span data-stu-id="163ae-143">Any</span></span></p></td>
<td><p><span data-ttu-id="163ae-144">Пограничный сервер, общедоступный IP-адрес пограничной службы доступа</span><span class="sxs-lookup"><span data-stu-id="163ae-144">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="163ae-145">Для Федеративной и общедоступной службы обмена мгновенными сообщениями с помощью SIP</span><span class="sxs-lookup"><span data-stu-id="163ae-145">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="163ae-146">Access/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="163ae-146">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="163ae-147">Пограничный сервер, общедоступный IP-адрес пограничной службы доступа</span><span class="sxs-lookup"><span data-stu-id="163ae-147">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="163ae-148">Любой</span><span class="sxs-lookup"><span data-stu-id="163ae-148">Any</span></span></p></td>
<td><p><span data-ttu-id="163ae-149">Для Федеративной и общедоступной службы обмена мгновенными сообщениями с помощью SIP</span><span class="sxs-lookup"><span data-stu-id="163ae-149">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="163ae-150">Веб-конференции/PSOM (TLS) TCP/443</span><span class="sxs-lookup"><span data-stu-id="163ae-150">Web Conferencing/PSOM(TLS)TCP/443</span></span></p></td>
<td><p><span data-ttu-id="163ae-151">Любой</span><span class="sxs-lookup"><span data-stu-id="163ae-151">Any</span></span></p></td>
<td><p><span data-ttu-id="163ae-152">Общедоступный IP-адрес службы пограничного сервера для веб-конференций Edge</span><span class="sxs-lookup"><span data-stu-id="163ae-152">Edge Server Web Conferencing Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="163ae-153">Мультимедиа для веб-конференций</span><span class="sxs-lookup"><span data-stu-id="163ae-153">Web Conferencing media</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="163ae-154">A/V/RTP/TCP/50000-59,999</span><span class="sxs-lookup"><span data-stu-id="163ae-154">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="163ae-155">Пограничный сервер, общедоступный IP-адрес пограничной службы аудио- и видеоданных</span><span class="sxs-lookup"><span data-stu-id="163ae-155">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="163ae-156">Любой</span><span class="sxs-lookup"><span data-stu-id="163ae-156">Any</span></span></p></td>
<td><p><span data-ttu-id="163ae-157">Требуется для Федерации с партнерами, работающими под управлением Office Communications Server 2007, Office Communications Server 2007 R2, Lync Server 2010 и Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="163ae-157">Required for federating with partners running Office Communications Server 2007, Office Communications Server 2007 R2, Lync Server 2010 and Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="163ae-158">A/V/RTP/UDP/50000-59,999</span><span class="sxs-lookup"><span data-stu-id="163ae-158">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="163ae-159">Пограничный сервер, общедоступный IP-адрес пограничной службы аудио- и видеоданных</span><span class="sxs-lookup"><span data-stu-id="163ae-159">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="163ae-160">Любой</span><span class="sxs-lookup"><span data-stu-id="163ae-160">Any</span></span></p></td>
<td><p><span data-ttu-id="163ae-161">Требуется только для Федерации с партнерами, работающими под управлением Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="163ae-161">Required only for federation with partners running Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="163ae-162">A/V/RTP/TCP/50000-59,999</span><span class="sxs-lookup"><span data-stu-id="163ae-162">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="163ae-163">Любой</span><span class="sxs-lookup"><span data-stu-id="163ae-163">Any</span></span></p></td>
<td><p><span data-ttu-id="163ae-164">Пограничный сервер, общедоступный IP-адрес пограничной службы аудио- и видеоданных</span><span class="sxs-lookup"><span data-stu-id="163ae-164">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="163ae-165">Требуется только для Федерации с партнерами, работающими под управлением Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="163ae-165">Required only for federation with partners running Office Communications Server 2007</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="163ae-166">A/V/RTP/UDP/50000-59,999</span><span class="sxs-lookup"><span data-stu-id="163ae-166">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="163ae-167">Любой</span><span class="sxs-lookup"><span data-stu-id="163ae-167">Any</span></span></p></td>
<td><p><span data-ttu-id="163ae-168">Пограничный сервер, общедоступный IP-адрес пограничной службы аудио- и видеоданных</span><span class="sxs-lookup"><span data-stu-id="163ae-168">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="163ae-169">Требуется только для Федерации с партнерами, работающими под управлением Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="163ae-169">Required only for federation with partners running Office Communications Server 2007</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="163ae-170">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="163ae-170">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="163ae-171">Пограничный сервер, общедоступный IP-адрес пограничной службы аудио- и видеоданных</span><span class="sxs-lookup"><span data-stu-id="163ae-171">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="163ae-172">Любой</span><span class="sxs-lookup"><span data-stu-id="163ae-172">Any</span></span></p></td>
<td><p><span data-ttu-id="163ae-173">3478 Outbound используется для определения версии пограничного сервера, с которым обменивается данными Lync Server, а также для мультимедийного трафика от пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="163ae-173">3478 outbound is used to determine the version of Edge Server that Lync Server is communicating with and also for media traffic from Edge Server-to-Edge Server.</span></span> <span data-ttu-id="163ae-174">Требуется для Федерации с Lync Server 2010, Windows Live Messenger и Office Communications Server 2007 R2, а также в том случае, если в компании развернуты несколько пулов Edge.</span><span class="sxs-lookup"><span data-stu-id="163ae-174">Required for federation with Lync Server 2010, Windows Live Messenger, and Office Communications Server 2007 R2, and also if multiple Edge pools are deployed within a company.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="163ae-175">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="163ae-175">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="163ae-176">Любой</span><span class="sxs-lookup"><span data-stu-id="163ae-176">Any</span></span></p></td>
<td><p><span data-ttu-id="163ae-177">Пограничный сервер, общедоступный IP-адрес пограничной службы аудио- и видеоданных</span><span class="sxs-lookup"><span data-stu-id="163ae-177">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="163ae-178">STUN/отключите согласование кандидатов по протоколу UDP/3478</span><span class="sxs-lookup"><span data-stu-id="163ae-178">STUN/TURN negotiation of candidates over UDP/3478</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="163ae-179">A/V/STUN, MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="163ae-179">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="163ae-180">Любой</span><span class="sxs-lookup"><span data-stu-id="163ae-180">Any</span></span></p></td>
<td><p><span data-ttu-id="163ae-181">Пограничный сервер, общедоступный IP-адрес пограничной службы аудио- и видеоданных</span><span class="sxs-lookup"><span data-stu-id="163ae-181">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="163ae-182">STUN/отключите согласование кандидатов по протоколу TCP/443</span><span class="sxs-lookup"><span data-stu-id="163ae-182">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="163ae-183">A/V/STUN, MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="163ae-183">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="163ae-184">Служба Edge для пограничного сервера A/V</span><span class="sxs-lookup"><span data-stu-id="163ae-184">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="163ae-185">Любой</span><span class="sxs-lookup"><span data-stu-id="163ae-185">Any</span></span></p></td>
<td><p><span data-ttu-id="163ae-186">STUN/отключите согласование кандидатов по протоколу TCP/443</span><span class="sxs-lookup"><span data-stu-id="163ae-186">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="firewall-summary-for-scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses-internal-interface--node-1-and-node-2-example"></a><span data-ttu-id="163ae-187">Сводка по межсетевому экрану для масштабируемой консолидированной границы, балансировка нагрузки DNS с общедоступными IP-адресами: внутренний интерфейс — узел 1 и узел 2 (пример)</span><span class="sxs-lookup"><span data-stu-id="163ae-187">Firewall Summary for Scaled Consolidated Edge, DNS Load Balancing with Public IP Addresses: Internal Interface – Node 1 and Node 2 (Example)</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="163ae-188">Протокол/TCP или UDP/порт</span><span class="sxs-lookup"><span data-stu-id="163ae-188">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="163ae-189">IP-адрес источника</span><span class="sxs-lookup"><span data-stu-id="163ae-189">Source IP address</span></span></th>
<th><span data-ttu-id="163ae-190">IP-адрес назначения</span><span class="sxs-lookup"><span data-stu-id="163ae-190">Destination IP address</span></span></th>
<th><span data-ttu-id="163ae-191">Комментарии</span><span class="sxs-lookup"><span data-stu-id="163ae-191">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="163ae-192">XMPP/MTLS/TCP/23456</span><span class="sxs-lookup"><span data-stu-id="163ae-192">XMPP/MTLS/TCP/23456</span></span></p></td>
<td><p><span data-ttu-id="163ae-193">Any (может быть определено как адрес сервера переднего плана или IP-адрес пула переднего плана, на котором запущена служба шлюза XMPP)</span><span class="sxs-lookup"><span data-stu-id="163ae-193">Any (can be defined as Front End Server address, or Front End pool IP address running the XMPP Gateway service)</span></span></p></td>
<td><p><span data-ttu-id="163ae-194">Внутренний интерфейс пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="163ae-194">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="163ae-195">Исходящий трафик XMPP от службы шлюза XMPP, работающей на сервере переднего плана или в пуле внешних интерфейсов</span><span class="sxs-lookup"><span data-stu-id="163ae-195">Outbound XMPP traffic from XMPP Gateway service running on Front End Server or Front End pool</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="163ae-196">SIP/MTLS/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="163ae-196">SIP/MTLS/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="163ae-197">Any (может быть определено как режиссер, IP-адрес пула режиссера, сервер клиентского доступа или IP-адрес пула переднего плана)</span><span class="sxs-lookup"><span data-stu-id="163ae-197">Any (can be defined as Director, Director pool IP address, Front End Server or Front End pool IP address)</span></span></p></td>
<td><p><span data-ttu-id="163ae-198">Внутренний интерфейс пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="163ae-198">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="163ae-199">Исходящий трафик SIP (от режиссера, IP-адреса пула, сервера переднего плана или IP-адреса пула переднего плана) к внутреннему интерфейсу пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="163ae-199">Outbound SIP traffic (from Director, Director pool IP address, Front End Server or Front End pool IP address) to Edge Server internal interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="163ae-200">SIP/MTLS/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="163ae-200">SIP/MTLS/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="163ae-201">Внутренний интерфейс пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="163ae-201">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="163ae-202">Any (может быть определено как режиссер, IP-адрес пула режиссера, сервер клиентского доступа или IP-адрес пула переднего плана)</span><span class="sxs-lookup"><span data-stu-id="163ae-202">Any (can be defined as Director, Director pool IP address, Front End Server or Front End pool IP address)</span></span></p></td>
<td><p><span data-ttu-id="163ae-203">Входящий трафик SIP (для режиссера, IP-адреса пула, сервера переднего плана или IP-адреса пула переднего плана) от внутреннего интерфейса пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="163ae-203">Inbound SIP traffic (to Director, Director pool IP address, Front End Server or Front End pool IP address) from Edge Server internal interface</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="163ae-204">PSOM/MTLS/TCP/8057</span><span class="sxs-lookup"><span data-stu-id="163ae-204">PSOM/MTLS/TCP/8057</span></span></p></td>
<td><p><span data-ttu-id="163ae-205">Any (может быть IP-адресом сервера переднего плана или IP-адресом серверного переднего плана в пуле переднего плана)</span><span class="sxs-lookup"><span data-stu-id="163ae-205">Any (can be defined as Front End Server IP address, or each Front End Server IP address in a Front End pool)</span></span></p></td>
<td><p><span data-ttu-id="163ae-206">Внутренний интерфейс пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="163ae-206">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="163ae-207">Трафик веб-конференций от сервера переднего плана или каждого серверного переднего плана, если он находится в пуле и является внутренним интерфейсом пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="163ae-207">Web conferencing traffic from Front End Server or each Front End Server if in a pool, to Edge Server internal interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="163ae-208">SIP/MTLS/TCP/5062</span><span class="sxs-lookup"><span data-stu-id="163ae-208">SIP/MTLS/TCP/5062</span></span></p></td>
<td><p><span data-ttu-id="163ae-209">Any (может быть как IP-адресом переднего сервера, так и IP-адресом пула переднего плана либо любым бесперебойно работающее устройство филиала или с помощью этого пограничного сервера).</span><span class="sxs-lookup"><span data-stu-id="163ae-209">Any (can be defined as Front End Server IP address, or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server)</span></span></p></td>
<td><p><span data-ttu-id="163ae-210">Внутренний интерфейс пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="163ae-210">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="163ae-211">Проверка подлинности пользователей/V (служба проверки подлинности A/V) от IP-адреса сервера переднего плана или переднего плана, а также от любого работающего филиала или сервера с бесперебойной подразделением с помощью этого пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="163ae-211">Authentication of A/V users (A/V authentication service) from Front End Server or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="163ae-212">STUN/MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="163ae-212">STUN/MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="163ae-213">Любой</span><span class="sxs-lookup"><span data-stu-id="163ae-213">Any</span></span></p></td>
<td><p><span data-ttu-id="163ae-214">Внутренний интерфейс пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="163ae-214">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="163ae-215">Предпочтительный путь для передачи мультимедиа между внутренними и внешними пользователями, бесперебойно работающем устройстве филиалов или бесперебойно работающем сервере филиала</span><span class="sxs-lookup"><span data-stu-id="163ae-215">Preferred path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="163ae-216">STUN/MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="163ae-216">STUN/MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="163ae-217">Любой</span><span class="sxs-lookup"><span data-stu-id="163ae-217">Any</span></span></p></td>
<td><p><span data-ttu-id="163ae-218">Внутренний интерфейс пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="163ae-218">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="163ae-219">Резервный путь для передачи мультимедиа между внутренними и внешними пользователями, бесперебойно работающее устройство филиала или бесперебойный сервер филиала, если не удается установить UDP-связь, используется протокол TCP для обмена файлами и демонстрации рабочего стола</span><span class="sxs-lookup"><span data-stu-id="163ae-219">Fallback path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server if UDP communication cannot be established, TCP is used for file transfer and desktop sharing</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="163ae-220">HTTPS/TCP/4443</span><span class="sxs-lookup"><span data-stu-id="163ae-220">HTTPS/TCP/4443</span></span></p></td>
<td><p><span data-ttu-id="163ae-221">Any (может быть указан в качестве IP-адреса сервера переднего плана или пула, содержащего центральное хранилище управления).</span><span class="sxs-lookup"><span data-stu-id="163ae-221">Any (can be defined as the Front End Server IP address, or pool that holds the Central Management store)</span></span></p></td>
<td><p><span data-ttu-id="163ae-222">Внутренний интерфейс пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="163ae-222">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="163ae-223">Репликация изменений из хранилища центрального управления на пограничный сервер</span><span class="sxs-lookup"><span data-stu-id="163ae-223">Replication of changes from the Central Management store to the Edge Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="163ae-224">MTLS/TCP/50001</span><span class="sxs-lookup"><span data-stu-id="163ae-224">MTLS/TCP/50001</span></span></p></td>
<td><p><span data-ttu-id="163ae-225">Любой</span><span class="sxs-lookup"><span data-stu-id="163ae-225">Any</span></span></p></td>
<td><p><span data-ttu-id="163ae-226">Внутренний интерфейс пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="163ae-226">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="163ae-227">Централизованное ведение журналов, использование команд командной строки Lync Server Management Shell и централизованной службы ведения журналов, команды ClsController (ClsController.exe) или агента (ClsAgent.exe) и коллекции журналов</span><span class="sxs-lookup"><span data-stu-id="163ae-227">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="163ae-228">MTLS/TCP/50002</span><span class="sxs-lookup"><span data-stu-id="163ae-228">MTLS/TCP/50002</span></span></p></td>
<td><p><span data-ttu-id="163ae-229">Любой</span><span class="sxs-lookup"><span data-stu-id="163ae-229">Any</span></span></p></td>
<td><p><span data-ttu-id="163ae-230">Внутренний интерфейс пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="163ae-230">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="163ae-231">Централизованное ведение журналов, использование команд командной строки Lync Server Management Shell и централизованной службы ведения журналов, команды ClsController (ClsController.exe) или агента (ClsAgent.exe) и коллекции журналов</span><span class="sxs-lookup"><span data-stu-id="163ae-231">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="163ae-232">MTLS/TCP/50003</span><span class="sxs-lookup"><span data-stu-id="163ae-232">MTLS/TCP/50003</span></span></p></td>
<td><p><span data-ttu-id="163ae-233">Любой</span><span class="sxs-lookup"><span data-stu-id="163ae-233">Any</span></span></p></td>
<td><p><span data-ttu-id="163ae-234">Внутренний интерфейс пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="163ae-234">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="163ae-235">Централизованное ведение журналов, использование команд командной строки Lync Server Management Shell и централизованной службы ведения журналов, команды ClsController (ClsController.exe) или агента (ClsAgent.exe) и коллекции журналов</span><span class="sxs-lookup"><span data-stu-id="163ae-235">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary-for-federation"></a><span data-ttu-id="163ae-236">Сводка по межсетевому экрану для Федерации</span><span class="sxs-lookup"><span data-stu-id="163ae-236">Firewall Summary for Federation</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="163ae-237">Role/Protocol/TCP/UDP/порт</span><span class="sxs-lookup"><span data-stu-id="163ae-237">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="163ae-238">IP-адрес источника</span><span class="sxs-lookup"><span data-stu-id="163ae-238">Source IP address</span></span></th>
<th><span data-ttu-id="163ae-239">IP-адрес назначения</span><span class="sxs-lookup"><span data-stu-id="163ae-239">Destination IP address</span></span></th>
<th><span data-ttu-id="163ae-240">Примечания.</span><span class="sxs-lookup"><span data-stu-id="163ae-240">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="163ae-241">Access/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="163ae-241">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="163ae-242">Общедоступный IP-адрес службы пограничного доступа</span><span class="sxs-lookup"><span data-stu-id="163ae-242">Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="163ae-243">Любой</span><span class="sxs-lookup"><span data-stu-id="163ae-243">Any</span></span></p></td>
<td><p><span data-ttu-id="163ae-244">Для Федеративной и общедоступной службы обмена мгновенными сообщениями с помощью SIP</span><span class="sxs-lookup"><span data-stu-id="163ae-244">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary--public-instant-messaging-connectivity"></a><span data-ttu-id="163ae-245">Сводка по брандмауэрам: общедоступная служба обмена мгновенными сообщениями</span><span class="sxs-lookup"><span data-stu-id="163ae-245">Firewall Summary – Public Instant Messaging Connectivity</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="163ae-246">Role/Protocol/TCP/UDP/порт</span><span class="sxs-lookup"><span data-stu-id="163ae-246">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="163ae-247">IP-адрес источника</span><span class="sxs-lookup"><span data-stu-id="163ae-247">Source IP address</span></span></th>
<th><span data-ttu-id="163ae-248">IP-адрес назначения</span><span class="sxs-lookup"><span data-stu-id="163ae-248">Destination IP address</span></span></th>
<th><span data-ttu-id="163ae-249">Примечания.</span><span class="sxs-lookup"><span data-stu-id="163ae-249">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="163ae-250">Access/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="163ae-250">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="163ae-251">Партнеры по подключению общедоступных мгновенных сообщений</span><span class="sxs-lookup"><span data-stu-id="163ae-251">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="163ae-252">Служба пограничного доступа к пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="163ae-252">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="163ae-253">Для Федеративной и общедоступной службы обмена мгновенными сообщениями с помощью SIP</span><span class="sxs-lookup"><span data-stu-id="163ae-253">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="163ae-254">Access/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="163ae-254">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="163ae-255">Служба пограничного доступа к пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="163ae-255">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="163ae-256">Партнеры по подключению общедоступных мгновенных сообщений</span><span class="sxs-lookup"><span data-stu-id="163ae-256">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="163ae-257">Для Федеративной и общедоступной службы обмена мгновенными сообщениями с помощью SIP</span><span class="sxs-lookup"><span data-stu-id="163ae-257">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="163ae-258">Access/SIP (TLS)/TCP/443</span><span class="sxs-lookup"><span data-stu-id="163ae-258">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="163ae-259">Клиенты</span><span class="sxs-lookup"><span data-stu-id="163ae-259">Clients</span></span></p></td>
<td><p><span data-ttu-id="163ae-260">Служба пограничного доступа к пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="163ae-260">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="163ae-261">Трафик SIP "клиент-сервер" для доступа внешних пользователей</span><span class="sxs-lookup"><span data-stu-id="163ae-261">Client-to-server SIP traffic for external user access</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="163ae-262">A/V/RTP/TCP/50000-59,999</span><span class="sxs-lookup"><span data-stu-id="163ae-262">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="163ae-263">Служба Edge для пограничного сервера A/V</span><span class="sxs-lookup"><span data-stu-id="163ae-263">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="163ae-264">Клиенты Live Messenger</span><span class="sxs-lookup"><span data-stu-id="163ae-264">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="163ae-265">Используется для сеансов обмена мгновенными сообщениями с помощью Windows Live Messenger, если настроена служба общего доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="163ae-265">Used for A/V sessions with Windows Live Messenger if public IM connectivity is configured.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="163ae-266">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="163ae-266">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="163ae-267">Служба Edge для пограничного сервера A/V</span><span class="sxs-lookup"><span data-stu-id="163ae-267">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="163ae-268">Клиенты Live Messenger</span><span class="sxs-lookup"><span data-stu-id="163ae-268">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="163ae-269">Требуется для общедоступной службы обмена мгновенными сообщениями в Windows Live Messenger</span><span class="sxs-lookup"><span data-stu-id="163ae-269">Required for public IM connectivity with Windows Live Messenger</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="163ae-270">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="163ae-270">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="163ae-271">Клиенты Live Messenger</span><span class="sxs-lookup"><span data-stu-id="163ae-271">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="163ae-272">Служба Edge для пограничного сервера A/V</span><span class="sxs-lookup"><span data-stu-id="163ae-272">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="163ae-273">Требуется для общедоступной службы обмена мгновенными сообщениями в Windows Live Messenger</span><span class="sxs-lookup"><span data-stu-id="163ae-273">Required for public IM connectivity with Windows Live Messenger</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary-for-extensible-messaging-and-presence-protocol"></a><span data-ttu-id="163ae-274">Сводка брандмауэра по протоколу расширенного обмена сообщениями и присутствия</span><span class="sxs-lookup"><span data-stu-id="163ae-274">Firewall Summary for Extensible Messaging and Presence Protocol</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="163ae-275">Протокол/TCP или UDP/порт</span><span class="sxs-lookup"><span data-stu-id="163ae-275">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="163ae-276">Источник (IP-адрес)</span><span class="sxs-lookup"><span data-stu-id="163ae-276">Source (IP address)</span></span></th>
<th><span data-ttu-id="163ae-277">Назначение (IP-адрес)</span><span class="sxs-lookup"><span data-stu-id="163ae-277">Destination (IP address)</span></span></th>
<th><span data-ttu-id="163ae-278">Комментарии</span><span class="sxs-lookup"><span data-stu-id="163ae-278">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="163ae-279">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="163ae-279">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="163ae-280">Любой</span><span class="sxs-lookup"><span data-stu-id="163ae-280">Any</span></span></p></td>
<td><p><span data-ttu-id="163ae-281">IP-адрес интерфейса службы пограничного доступа к серверу Edge</span><span class="sxs-lookup"><span data-stu-id="163ae-281">Edge Server Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="163ae-282">Стандартный коммуникационный порт "сервер-сервер" для XMPP.</span><span class="sxs-lookup"><span data-stu-id="163ae-282">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="163ae-283">Разрешает связь с прокси-сервером пограничного сервера XMPP от федеративных XMPP партнеров</span><span class="sxs-lookup"><span data-stu-id="163ae-283">Allows communication to the Edge Server XMPP proxy from federated XMPP partners</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="163ae-284">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="163ae-284">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="163ae-285">IP-адрес интерфейса службы пограничного доступа к серверу Edge</span><span class="sxs-lookup"><span data-stu-id="163ae-285">Edge Server Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="163ae-286">Любой</span><span class="sxs-lookup"><span data-stu-id="163ae-286">Any</span></span></p></td>
<td><p><span data-ttu-id="163ae-287">Стандартный коммуникационный порт "сервер-сервер" для XMPP.</span><span class="sxs-lookup"><span data-stu-id="163ae-287">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="163ae-288">Разрешает взаимодействие с XMPP прокси-сервером для федеративных XMPP партнеров</span><span class="sxs-lookup"><span data-stu-id="163ae-288">Allows communication from the Edge Server XMPP proxy to federated XMPP partners</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="163ae-289">XMPP/MTLS/TCP/23456</span><span class="sxs-lookup"><span data-stu-id="163ae-289">XMPP/MTLS/TCP/23456</span></span></p></td>
<td><p><span data-ttu-id="163ae-290">Любой</span><span class="sxs-lookup"><span data-stu-id="163ae-290">Any</span></span></p></td>
<td><p><span data-ttu-id="163ae-291">Каждый внутренний IP-адрес интерфейса пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="163ae-291">Each internal Edge Server Interface IP</span></span></p></td>
<td><p><span data-ttu-id="163ae-292">Внутренний IP-адрес XMPP, входящий в состав шлюза XMPP на сервере переднего плана или в пуле переднего плана, в адрес внутренней сети пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="163ae-292">Internal XMPP traffic from the XMPP Gateway on the Front End Server or Front End pool to the Edge Server internal IP address or each Edge pool member’s internal IP address</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="163ae-293">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="163ae-293">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

