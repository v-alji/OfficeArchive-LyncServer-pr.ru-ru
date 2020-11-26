---
title: Сводка по портам — масштабируемая консолидированная пограничная топология с аппаратными балансировщиками нагрузки
description: Линейный Объединенный край для порта с подсистемы балансировки нагрузки оборудования.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - Scaled consolidated edge with hardware load balancers
ms:assetid: 91213b1e-f875-464b-83e8-fe3a351595a4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398739(v=OCS.15)
ms:contentKeyID: 48184841
ms.date: 04/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1a03acb3644d83669bcf0065ebb20c526ef5fa32
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424318"
---
# <a name="port-summary---scaled-consolidated-edge-with-hardware-load-balancers-in-lync-server-2013"></a><span data-ttu-id="9f6da-103">Сводка по портам — масштабируемая консолидированная пограничная топология с аппаратными балансировщиками нагрузки в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9f6da-103">Port summary - Scaled consolidated edge with hardware load balancers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9f6da-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9f6da-104">

<span> </span></span></span>

<span data-ttu-id="9f6da-105">_**Тема последнего изменения:** 2015-04-27_</span><span class="sxs-lookup"><span data-stu-id="9f6da-105">_**Topic Last Modified:** 2015-04-27_</span></span>

<span data-ttu-id="9f6da-106">Функция пограничного сервера Lync Server 2013, описанная в этой архитектуре сценариев, очень похожа на ту, что была реализована в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="9f6da-106">The Lync Server 2013, Edge Server functionality described in this scenario architecture is very similar to what was implemented in Lync Server 2010.</span></span> <span data-ttu-id="9f6da-107">Наиболее заметным дополнением является порт **5269 на TCP** для протокола расширенной обработки сообщений и присутствия (XMPP).</span><span class="sxs-lookup"><span data-stu-id="9f6da-107">The most noticeable addition is the port **5269 over TCP** entry for the extensible messaging and presence protocol (XMPP).</span></span> <span data-ttu-id="9f6da-108">Lync Server 2013 (при необходимости) можно развернуть прокси-сервер XMPP на пограничном или пограничном пуле, а также на сервере шлюзов XMPP на сервере переднего плана или в пуле внешних интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="9f6da-108">Lync Server 2013 optionally deploys an XMPP proxy on the Edge Server or Edge pool and the XMPP gateway server on the Front End Server or Front End pool.</span></span>

<span data-ttu-id="9f6da-109">В дополнение к протоколу IPv4, пограничный сервер теперь поддерживает IPv6.</span><span class="sxs-lookup"><span data-stu-id="9f6da-109">In addition to IPv4, the Edge Server now supports IPv6.</span></span> <span data-ttu-id="9f6da-110">Для ясности в сценариях используется только протокол IPv4.</span><span class="sxs-lookup"><span data-stu-id="9f6da-110">For clarity, only IPv4 is used in the scenarios.</span></span>

<span data-ttu-id="9f6da-111">**Масштабируемый Объединенный край с использованием аппаратной балансировки нагрузки**</span><span class="sxs-lookup"><span data-stu-id="9f6da-111">**Scaled Consolidated Edge using Hardware Load Balancing**</span></span>

<span data-ttu-id="9f6da-112">![Порты и протоколы сети периметра пограничного сервера](images/Gg398739.063f7dd1-16db-4cc7-8708-bca9bc41184d(OCS.15).jpg "Порты и протоколы сети периметра пограничного сервера")</span><span class="sxs-lookup"><span data-stu-id="9f6da-112">![Edge Server Perimeter Network ports and protocols](images/Gg398739.063f7dd1-16db-4cc7-8708-bca9bc41184d(OCS.15).jpg "Edge Server Perimeter Network ports and protocols")</span></span>

<div>

## <a name="port-and-protocol-details"></a><span data-ttu-id="9f6da-113">Сведения о портах и протоколах</span><span class="sxs-lookup"><span data-stu-id="9f6da-113">Port and Protocol Details</span></span>

<span data-ttu-id="9f6da-114">Рекомендуется открывать только порты, необходимые для поддержки функций, для которых предоставляется внешний доступ.</span><span class="sxs-lookup"><span data-stu-id="9f6da-114">It is recommended that you open only the ports required to support the functionality for which you are providing external access.</span></span>

<span data-ttu-id="9f6da-115">Для удаленного доступа к работе в любой службе пограничного сервера необходимо, чтобы трафик SIP был в направлении на один и тот же трафик по внешнему потоку, как показано на рисунке входящего и исходящего трафика пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="9f6da-115">For remote access to work for any edge service, it is mandatory that SIP traffic is allowed to flow bi-directionally as shown in the Inbound/Outbound edge traffic figure.</span></span> <span data-ttu-id="9f6da-116">Другими словами, Обмен сообщениями SIP и из службы Edge для Access осуществляется в обмене мгновенными сообщениями, присутствии, веб-конференциях, аудио-и видеосвязи (A/V) и Федерации.</span><span class="sxs-lookup"><span data-stu-id="9f6da-116">Stated another way, the SIP messaging to and from the Access Edge service is involved in instant messaging (IM), presence, web conferencing, audio/video (A/V) and federation.</span></span>

### <a name="firewall-summary-for-scaled-consolidated-edge-hardware-load-balanced-external-interface--node-1-and-node-2-example"></a><span data-ttu-id="9f6da-117">Сводка по межсетевому экрану для масштабируемой консолидированной границы, аппаратной балансировки нагрузки: внешний интерфейс — узел 1 и узел 2 (пример)</span><span class="sxs-lookup"><span data-stu-id="9f6da-117">Firewall Summary for Scaled Consolidated Edge, Hardware Load Balanced: External Interface – Node 1 and Node 2 (Example)</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9f6da-118">Role/Protocol/TCP/UDP/порт</span><span class="sxs-lookup"><span data-stu-id="9f6da-118">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="9f6da-119">IP-адрес источника</span><span class="sxs-lookup"><span data-stu-id="9f6da-119">Source IP address</span></span></th>
<th><span data-ttu-id="9f6da-120">IP-адрес назначения</span><span class="sxs-lookup"><span data-stu-id="9f6da-120">Destination IP address</span></span></th>
<th><span data-ttu-id="9f6da-121">Примечания.</span><span class="sxs-lookup"><span data-stu-id="9f6da-121">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9f6da-122">Access/HTTP/TCP/80</span><span class="sxs-lookup"><span data-stu-id="9f6da-122">Access/HTTP/TCP/80</span></span></p></td>
<td><p><span data-ttu-id="9f6da-123">Пограничный сервер, общедоступный IP-адрес пограничной службы доступа</span><span class="sxs-lookup"><span data-stu-id="9f6da-123">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="9f6da-124">Любой</span><span class="sxs-lookup"><span data-stu-id="9f6da-124">Any</span></span></p></td>
<td><p><span data-ttu-id="9f6da-125">Проверка отзыва сертификатов и получения CRL</span><span class="sxs-lookup"><span data-stu-id="9f6da-125">Certificate revocation/CRL check and retrieval</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f6da-126">Access/DNS/TCP/53</span><span class="sxs-lookup"><span data-stu-id="9f6da-126">Access/DNS/TCP/53</span></span></p></td>
<td><p><span data-ttu-id="9f6da-127">Пограничный сервер, общедоступный IP-адрес пограничной службы доступа</span><span class="sxs-lookup"><span data-stu-id="9f6da-127">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="9f6da-128">Любой</span><span class="sxs-lookup"><span data-stu-id="9f6da-128">Any</span></span></p></td>
<td><p><span data-ttu-id="9f6da-129">Запрос DNS по протоколу TCP</span><span class="sxs-lookup"><span data-stu-id="9f6da-129">DNS query over TCP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f6da-130">Access/DNS/UDP/53</span><span class="sxs-lookup"><span data-stu-id="9f6da-130">Access/DNS/UDP/53</span></span></p></td>
<td><p><span data-ttu-id="9f6da-131">Пограничный сервер, общедоступный IP-адрес пограничной службы доступа</span><span class="sxs-lookup"><span data-stu-id="9f6da-131">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="9f6da-132">Любой</span><span class="sxs-lookup"><span data-stu-id="9f6da-132">Any</span></span></p></td>
<td><p><span data-ttu-id="9f6da-133">Запрос DNS по протоколу UDP</span><span class="sxs-lookup"><span data-stu-id="9f6da-133">DNS query over UDP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f6da-134">A/V/RTP/TCP/50000-59,999</span><span class="sxs-lookup"><span data-stu-id="9f6da-134">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="9f6da-135">Пограничный сервер, IP-адрес пограничной службы аудио- и видеоданных</span><span class="sxs-lookup"><span data-stu-id="9f6da-135">Edge Server A/V Edge service IP address</span></span></p></td>
<td><p><span data-ttu-id="9f6da-136">Любой</span><span class="sxs-lookup"><span data-stu-id="9f6da-136">Any</span></span></p></td>
<td><p><span data-ttu-id="9f6da-137">Требуется для Федерации с партнерами, работающими под управлением Office Communications Server 2007, Office Communications Server 2007 R2, Lync Server 2010 и Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="9f6da-137">Required for federating with partners running Office Communications Server 2007, Office Communications Server 2007 R2, Lync Server 2010 and Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f6da-138">A/V/RTP/UDP/50000-59,999</span><span class="sxs-lookup"><span data-stu-id="9f6da-138">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="9f6da-139">Пограничный сервер, общедоступный IP-адрес пограничной службы аудио- и видеоданных</span><span class="sxs-lookup"><span data-stu-id="9f6da-139">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="9f6da-140">Любой</span><span class="sxs-lookup"><span data-stu-id="9f6da-140">Any</span></span></p></td>
<td><p><span data-ttu-id="9f6da-141">Требуется только для Федерации с партнерами, работающими под управлением Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="9f6da-141">Required only for federation with partners running Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f6da-142">A/V/RTP/TCP/50000-59,999</span><span class="sxs-lookup"><span data-stu-id="9f6da-142">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="9f6da-143">Любой</span><span class="sxs-lookup"><span data-stu-id="9f6da-143">Any</span></span></p></td>
<td><p><span data-ttu-id="9f6da-144">Пограничный сервер, общедоступный IP-адрес пограничной службы аудио- и видеоданных</span><span class="sxs-lookup"><span data-stu-id="9f6da-144">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="9f6da-145">Требуется только для Федерации с партнерами, работающими под управлением Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="9f6da-145">Required only for federation with partners running Office Communications Server 2007</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f6da-146">A/V/RTP/UDP/50000-59,999</span><span class="sxs-lookup"><span data-stu-id="9f6da-146">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="9f6da-147">Любой</span><span class="sxs-lookup"><span data-stu-id="9f6da-147">Any</span></span></p></td>
<td><p><span data-ttu-id="9f6da-148">Пограничный сервер, общедоступный IP-адрес пограничной службы аудио- и видеоданных</span><span class="sxs-lookup"><span data-stu-id="9f6da-148">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="9f6da-149">Требуется только для Федерации с партнерами, работающими под управлением Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="9f6da-149">Required only for federation with partners running Office Communications Server 2007</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f6da-150">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="9f6da-150">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="9f6da-151">Пограничный сервер, общедоступный IP-адрес пограничной службы аудио- и видеоданных</span><span class="sxs-lookup"><span data-stu-id="9f6da-151">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="9f6da-152">Любой</span><span class="sxs-lookup"><span data-stu-id="9f6da-152">Any</span></span></p></td>
<td><p><span data-ttu-id="9f6da-153">3478 Outbound используется для определения версии пограничного сервера, с которым обменивается данными Lync Server, а также для мультимедийного трафика от пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="9f6da-153">3478 outbound is used to determine the version of Edge Server that Lync Server is communicating with and also for media traffic from Edge Server-to-Edge Server.</span></span> <span data-ttu-id="9f6da-154">Требуется для Федерации с Lync Server 2010, Windows Live Messenger и Office Communications Server 2007 R2, а также в том случае, если в компании развернуты несколько пулов Edge.</span><span class="sxs-lookup"><span data-stu-id="9f6da-154">Required for federation with Lync Server 2010, Windows Live Messenger, and Office Communications Server 2007 R2, and also if multiple Edge pools are deployed within a company.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f6da-155">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="9f6da-155">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="9f6da-156">Любой</span><span class="sxs-lookup"><span data-stu-id="9f6da-156">Any</span></span></p></td>
<td><p><span data-ttu-id="9f6da-157">Пограничный сервер, общедоступный IP-адрес пограничной службы аудио- и видеоданных</span><span class="sxs-lookup"><span data-stu-id="9f6da-157">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="9f6da-158">STUN/отключите согласование кандидатов по протоколу UDP/3478</span><span class="sxs-lookup"><span data-stu-id="9f6da-158">STUN/TURN negotiation of candidates over UDP/3478</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f6da-159">A/V/STUN, MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="9f6da-159">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="9f6da-160">Любой</span><span class="sxs-lookup"><span data-stu-id="9f6da-160">Any</span></span></p></td>
<td><p><span data-ttu-id="9f6da-161">Пограничный сервер, общедоступный IP-адрес пограничной службы аудио- и видеоданных</span><span class="sxs-lookup"><span data-stu-id="9f6da-161">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="9f6da-162">STUN/отключите согласование кандидатов по протоколу TCP/443</span><span class="sxs-lookup"><span data-stu-id="9f6da-162">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f6da-163">A/V/STUN, MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="9f6da-163">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="9f6da-164">Пограничный сервер, общедоступный IP-адрес пограничной службы аудио- и видеоданных</span><span class="sxs-lookup"><span data-stu-id="9f6da-164">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="9f6da-165">Любой</span><span class="sxs-lookup"><span data-stu-id="9f6da-165">Any</span></span></p></td>
<td><p><span data-ttu-id="9f6da-166">STUN/отключите согласование кандидатов по протоколу TCP/443</span><span class="sxs-lookup"><span data-stu-id="9f6da-166">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="firewall-summary-for-scaled-consolidated-edge-hardware-load-balanced-internal-interface-node-1-and-node-2"></a><span data-ttu-id="9f6da-167">Сводка по межсетевому экрану для масштабируемой консолидированной границы, аппаратной балансировки нагрузки: внутренний интерфейс, узел 1 и узел 2</span><span class="sxs-lookup"><span data-stu-id="9f6da-167">Firewall Summary for Scaled Consolidated Edge, Hardware Load Balanced: Internal Interface Node 1 and Node 2</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9f6da-168">Role/Protocol/TCP/UDP/порт</span><span class="sxs-lookup"><span data-stu-id="9f6da-168">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="9f6da-169">IP-адрес источника</span><span class="sxs-lookup"><span data-stu-id="9f6da-169">Source IP address</span></span></th>
<th><span data-ttu-id="9f6da-170">IP-адрес назначения</span><span class="sxs-lookup"><span data-stu-id="9f6da-170">Destination IP address</span></span></th>
<th><span data-ttu-id="9f6da-171">Примечания.</span><span class="sxs-lookup"><span data-stu-id="9f6da-171">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9f6da-172">XMPP/MTLS/TCP/23456</span><span class="sxs-lookup"><span data-stu-id="9f6da-172">XMPP/MTLS/TCP/23456</span></span></p></td>
<td><p><span data-ttu-id="9f6da-173">Any (может быть определено как адрес сервера переднего плана или виртуальный IP-адрес пула переднего плана, на котором запущена служба шлюза XMPP)</span><span class="sxs-lookup"><span data-stu-id="9f6da-173">Any (can be defined as Front End Server address, or Front End pool virtual IP address running the XMPP Gateway service)</span></span></p></td>
<td><p><span data-ttu-id="9f6da-174">Внутренний интерфейс пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="9f6da-174">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="9f6da-175">Исходящий трафик XMPP от службы шлюза XMPP, работающей на сервере переднего плана или в пуле внешних интерфейсов</span><span class="sxs-lookup"><span data-stu-id="9f6da-175">Outbound XMPP traffic from XMPP Gateway service running on Front End Server or Front End pool</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f6da-176">HTTPS/TCP/4443</span><span class="sxs-lookup"><span data-stu-id="9f6da-176">HTTPS/TCP/4443</span></span></p></td>
<td><p><span data-ttu-id="9f6da-177">Any (может быть задан как IP-адрес серверного сервера переднего плана или пул, хранящий центральное хранилище управления).</span><span class="sxs-lookup"><span data-stu-id="9f6da-177">Any (can be defined as the Front End Server server IP or pool that holds the Central Management store)</span></span></p></td>
<td><p><span data-ttu-id="9f6da-178">Внутренний интерфейс пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="9f6da-178">Edge Server Internal interface</span></span></p></td>
<td><p><span data-ttu-id="9f6da-179">Репликация изменений из хранилища центрального управления на пограничный сервер</span><span class="sxs-lookup"><span data-stu-id="9f6da-179">Replication of changes from the Central Management store to the Edge Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f6da-180">PSOM/MTLS/TCP/8057</span><span class="sxs-lookup"><span data-stu-id="9f6da-180">PSOM/MTLS/TCP/8057</span></span></p></td>
<td><p><span data-ttu-id="9f6da-181">Any (может быть определено как режиссер (IP-адрес), IP-адрес внешнего сервера или пул виртуальных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="9f6da-181">Any (can be defined as Director IP, Front End Server IP or Pool virtual IP)</span></span></p></td>
<td><p><span data-ttu-id="9f6da-182">Внутренний интерфейс пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="9f6da-182">Edge Server Internal interface</span></span></p></td>
<td><p><span data-ttu-id="9f6da-183">Трафик веб-конференций из внутреннего развертывания в внутренний интерфейс пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="9f6da-183">Web conferencing traffic from Internal deployment to Internal Edge Server interface</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f6da-184">STUN/MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="9f6da-184">STUN/MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="9f6da-185">Any (может быть определено как режиссер (IP-адрес), IP-адрес внешнего сервера или пул виртуальных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="9f6da-185">Any (can be defined as Director IP, Front End Server IP or Pool virtual IP)</span></span></p></td>
<td><p><span data-ttu-id="9f6da-186">Внутренний интерфейс пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="9f6da-186">Edge Server Internal interface</span></span></p></td>
<td><p><span data-ttu-id="9f6da-187">Предпочтительный путь для передачи мультимедиа между внутренними и внешними пользователями, бесперебойно работающем устройстве филиалов или бесперебойно работающем сервере филиала</span><span class="sxs-lookup"><span data-stu-id="9f6da-187">Preferred path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f6da-188">STUN/MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="9f6da-188">STUN/MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="9f6da-189">Any (может быть определено как режиссер (IP-адрес), IP-адрес внешнего сервера или пул виртуальных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="9f6da-189">Any (can be defined as Director IP, Front End Server IP or Pool virtual IP)</span></span></p></td>
<td><p><span data-ttu-id="9f6da-190">Внутренний интерфейс пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="9f6da-190">Edge Server Internal interface</span></span></p></td>
<td><p><span data-ttu-id="9f6da-191">Резервный путь для передачи мультимедиа между внутренними и внешними пользователями, бесперебойно работающее устройство филиала или бесперебойный сервер филиала, если не удается установить UDP-связь, используется протокол TCP для обмена файлами и демонстрации рабочего стола</span><span class="sxs-lookup"><span data-stu-id="9f6da-191">Fallback path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server if UDP communication cannot be established, TCP is used for file transfer and desktop sharing</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f6da-192">MTLS/TCP/50001</span><span class="sxs-lookup"><span data-stu-id="9f6da-192">MTLS/TCP/50001</span></span></p></td>
<td><p><span data-ttu-id="9f6da-193">Любой</span><span class="sxs-lookup"><span data-stu-id="9f6da-193">Any</span></span></p></td>
<td><p><span data-ttu-id="9f6da-194">Внутренний интерфейс пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="9f6da-194">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="9f6da-195">Централизованное ведение журналов, использование команд командной строки Lync Server Management Shell и централизованной службы ведения журналов, команды ClsController (ClsController.exe) или агента (ClsAgent.exe) и коллекции журналов</span><span class="sxs-lookup"><span data-stu-id="9f6da-195">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f6da-196">MTLS/TCP/50002</span><span class="sxs-lookup"><span data-stu-id="9f6da-196">MTLS/TCP/50002</span></span></p></td>
<td><p><span data-ttu-id="9f6da-197">Любой</span><span class="sxs-lookup"><span data-stu-id="9f6da-197">Any</span></span></p></td>
<td><p><span data-ttu-id="9f6da-198">Внутренний интерфейс пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="9f6da-198">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="9f6da-199">Централизованное ведение журналов, использование команд командной строки Lync Server Management Shell и централизованной службы ведения журналов, команды ClsController (ClsController.exe) или агента (ClsAgent.exe) и коллекции журналов</span><span class="sxs-lookup"><span data-stu-id="9f6da-199">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f6da-200">MTLS/TCP/50003</span><span class="sxs-lookup"><span data-stu-id="9f6da-200">MTLS/TCP/50003</span></span></p></td>
<td><p><span data-ttu-id="9f6da-201">Любой</span><span class="sxs-lookup"><span data-stu-id="9f6da-201">Any</span></span></p></td>
<td><p><span data-ttu-id="9f6da-202">Внутренний интерфейс пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="9f6da-202">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="9f6da-203">Централизованное ведение журналов, использование команд командной строки Lync Server Management Shell и централизованной службы ведения журналов, команды ClsController (ClsController.exe) или агента (ClsAgent.exe) и коллекции журналов</span><span class="sxs-lookup"><span data-stu-id="9f6da-203">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9f6da-204">При развертывании для обеспечения доступности и балансировки нагрузки для Lync Server аппаратные подсистемы балансировки нагрузки предъявляют определенные требования.</span><span class="sxs-lookup"><span data-stu-id="9f6da-204">Hardware load balancers have specific requirements when deployed to provide availability and load balancing for Lync Server.</span></span> <span data-ttu-id="9f6da-205">Требования определяются на приведенных ниже рисунках и таблицах.</span><span class="sxs-lookup"><span data-stu-id="9f6da-205">The requirements are defined in the following figure and tables.</span></span> <span data-ttu-id="9f6da-206">Сторонние производители могут использовать различные термины, которые определяются в соответствии с требованиями.</span><span class="sxs-lookup"><span data-stu-id="9f6da-206">Third party vendors may use different terminology for the requirements defined here.</span></span> <span data-ttu-id="9f6da-207">Вам потребуется сопоставить требования к серверу Lync Server функциям и параметрам конфигурации, предоставляемым поставщиком подсистемы балансировки нагрузки для оборудования.</span><span class="sxs-lookup"><span data-stu-id="9f6da-207">It will be necessary to map the requirements of Lync Server to the features and configuration options provided by your hardware load balancer vendor.</span></span>

<span data-ttu-id="9f6da-208">При настройке подсистемы балансировки нагрузки для оборудования учитывайте следующие требования:</span><span class="sxs-lookup"><span data-stu-id="9f6da-208">When configuring hardware load balancers, consider the following requirements:</span></span>

  - <span data-ttu-id="9f6da-209">Для службы пограничного сервера Access и службы Edge для веб-конференций можно настроить трансляцию сетевых адресов (SNAT) на оборудовании (HLB).</span><span class="sxs-lookup"><span data-stu-id="9f6da-209">Source Network Address Translation (SNAT) can be configured on the hardware load balancer (HLB) for Access Edge service and Web Conferencing Edge service</span></span>

  - <span data-ttu-id="9f6da-210">Не удается настроить SNAT в службе Edge/V: служба Edge может отвечать на запросы, не являющиеся виртуальным IP-адресом HLB (VIP), для простого обхода UDP по NAT (STUN)/Traversal с помощью ретрансляции NAT (переключение)/Federation (FTURN) для правильной работы</span><span class="sxs-lookup"><span data-stu-id="9f6da-210">SNAT cannot be configured on the A/V Edge service– the A/V Edge service must respond with the real server address, not the HLB virtual IP (VIP), for simple traversal of UDP over NAT (STUN)/traversal using relay NAT (TURN)/federation TURN (FTURN) to work properly</span></span>
    
      - <span data-ttu-id="9f6da-211">Если клиент отправляет запрос на HLB, ответ должен возвращаться из IP-адреса HLB</span><span class="sxs-lookup"><span data-stu-id="9f6da-211">If the client sends a request to the HLB, the response must come back from the HLB VIP</span></span>
    
      - <span data-ttu-id="9f6da-212">Если клиент отправляет запрос на ребро, ответ должен возвращаться из IP-адреса Edge.</span><span class="sxs-lookup"><span data-stu-id="9f6da-212">If the client sends a request to the Edge, the response must come back from the Edge IP</span></span>

  - <span data-ttu-id="9f6da-213">Общедоступные IP-адреса используются на каждом интерфейсе сервера и виртуальных IP-адресах в HLB, а требования к общедоступной сети — в N + 1, где есть общедоступный IP-адрес для каждого сервера реального времени и один для каждого из HLB VIP.</span><span class="sxs-lookup"><span data-stu-id="9f6da-213">Public IP addresses are used on each server interface and on the VIPs of the HLB, and your public IP address requirements are N+1, where there is a public IP address for each real server interface and one for each HLB VIP.</span></span> <span data-ttu-id="9f6da-214">Если у вас есть 2 пограничные сервера в пуле, это приводит к 9 общим IP-адресам, где 3 используются для VIP HLB и для каждого интерфейса пограничного сервера (общее количество шести для серверов).</span><span class="sxs-lookup"><span data-stu-id="9f6da-214">Where you have 2 Edge servers in the pool, this results in 9 public IP addresses, where 3 are used for the HLB VIPs, and one for each Edge server interface (a total of six for the servers)</span></span>

  - <span data-ttu-id="9f6da-215">Для службы пограничного доступа и службы Edge для веб-конференций (и с помощью NAT на HLB) клиент обращается к VIP, IP-адрес источника меняется с клиента на собственный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="9f6da-215">For the Access Edge service and Web Conferencing Edge service, (and using NAT on the HLB) the client contacts the VIP, the VIP changes the source IP address from the client to its own IP address.</span></span> <span data-ttu-id="9f6da-216">Интерфейс сервера отправляет в VIP-сервер адрес, возвращенный по протоколу IP, VIP изменяет адрес источника из IP адресного интерфейса сервера и направляет пакет клиенту.</span><span class="sxs-lookup"><span data-stu-id="9f6da-216">The server interface addresses the return address to the VIP, the VIP changes the source address from the server interface IP address and sends the packet to the client</span></span>

  - <span data-ttu-id="9f6da-217">Для службы EDGE (/V) VIP не должен изменять IP-адрес источника, а реальный адрес сервера возвращается клиенту напрямую — вы не можете настроить NAT для трафика HLB для AV</span><span class="sxs-lookup"><span data-stu-id="9f6da-217">For the A/V Edge service, the VIP must NOT change the source IP address, and the real server address is returned to the client directly – you cannot configure NAT on the HLB for AV traffic</span></span>
    
      - <span data-ttu-id="9f6da-218">Если клиент отправляет запрос в HLB VIP, ответ должен возвращаться из виртуального IP-адреса HLB</span><span class="sxs-lookup"><span data-stu-id="9f6da-218">If the client sends a request to the HLB VIP, the response must come back from the HLB VIP</span></span>
    
      - <span data-ttu-id="9f6da-219">Если клиент отправляет запрос на Граничный IP-адрес, ответ должен возвращаться из IP-адреса Edge.</span><span class="sxs-lookup"><span data-stu-id="9f6da-219">If the client sends a request to the Edge IP, the response must come back from the Edge IP</span></span>

  - <span data-ttu-id="9f6da-220">Для протоколов AV Внешний брандмауэр сохранит общедоступный IP-адрес сервера для всех пакетов.</span><span class="sxs-lookup"><span data-stu-id="9f6da-220">For AV, the external firewall will retain the real server public IP address for all packets</span></span>

  - <span data-ttu-id="9f6da-221">После того как вы установили подключение к службе EDGE, клиент может связаться с реальным сервером, а не HLB</span><span class="sxs-lookup"><span data-stu-id="9f6da-221">Once established, client to A/V Edge service communication is to the real server, not the HLB</span></span>

  - <span data-ttu-id="9f6da-222">Внутренний доступ к внутренним серверам и клиентам должен маршрутизироваться, а для всех внутренних сетей, которые размещаются на серверах или клиентах, должны быть установлены постоянные маршруты.</span><span class="sxs-lookup"><span data-stu-id="9f6da-222">Internal edge to internal servers and clients must be routed, and persistent routes are set for all internal networks that host servers or clients</span></span>

  - <span data-ttu-id="9f6da-223">Виртуальные IP-адреса службы пограничного доступа HLB будут выступать в качестве шлюза по умолчанию для каждого интерфейса пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="9f6da-223">The HLB Access Edge service VIP will act as the default gateway for each Edge server interface</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="9f6da-224">Для получения дополнительной информации о планировании и функциональных возможностях NAT ознакомьтесь с <A href="lync-server-2013-hardware-load-balancer-requirements.md">требованиями к подсистеме балансировки нагрузки для Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="9f6da-224">For further information on NAT planning and functionality, please refer to <A href="lync-server-2013-hardware-load-balancer-requirements.md">Hardware load balancer requirements for Lync Server 2013</A>.</span></span>



</div>

<span data-ttu-id="9f6da-225">![Сведения о портах и протоколах пограничного сервера](images/Gg398739.1c193b80-98ab-4d59-a854-dbfdb5e209e2(OCS.15).jpg "Сведения о портах и протоколах пограничного сервера")</span><span class="sxs-lookup"><span data-stu-id="9f6da-225">![Edge Server ports and protocols details](images/Gg398739.1c193b80-98ab-4d59-a854-dbfdb5e209e2(OCS.15).jpg "Edge Server ports and protocols details")</span></span>

### <a name="external-port-settings-required-for-scaled-consolidated-edge-hardware-load-balanced-external-interface-virtual-ips"></a><span data-ttu-id="9f6da-226">Параметры внешнего порта, необходимые для масштабируемой консолидированной границы, аппаратной балансировки нагрузки: внешние IP адресных интерфейсов</span><span class="sxs-lookup"><span data-stu-id="9f6da-226">External Port Settings Required for Scaled Consolidated Edge, Hardware Load Balanced: External Interface Virtual IPs</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9f6da-227">Role/Protocol/TCP/UDP/порт</span><span class="sxs-lookup"><span data-stu-id="9f6da-227">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="9f6da-228">IP-адрес источника</span><span class="sxs-lookup"><span data-stu-id="9f6da-228">Source IP address</span></span></th>
<th><span data-ttu-id="9f6da-229">IP-адрес назначения</span><span class="sxs-lookup"><span data-stu-id="9f6da-229">Destination IP address</span></span></th>
<th><span data-ttu-id="9f6da-230">Примечания.</span><span class="sxs-lookup"><span data-stu-id="9f6da-230">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9f6da-231">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="9f6da-231">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="9f6da-232">Любой</span><span class="sxs-lookup"><span data-stu-id="9f6da-232">Any</span></span></p></td>
<td><p><span data-ttu-id="9f6da-233">Прокси-служба XMPP (доступ к IP-адресу для общих ресурсов с помощью службы Edge Access)</span><span class="sxs-lookup"><span data-stu-id="9f6da-233">XMPP Proxy service (shares IP address with Access Edge service)</span></span></p></td>
<td><p><span data-ttu-id="9f6da-234">Прокси-служба XMPP принимает трафик от XMPP контактов в определенных XMPP федерациях.</span><span class="sxs-lookup"><span data-stu-id="9f6da-234">XMPP Proxy service accepts traffic from XMPP contacts in defined XMPP federations</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f6da-235">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="9f6da-235">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="9f6da-236">Прокси-служба XMPP (доступ к IP-адресу для общих ресурсов с помощью службы Edge Access)</span><span class="sxs-lookup"><span data-stu-id="9f6da-236">XMPP Proxy service (shares IP address with Access Edge service)</span></span></p></td>
<td><p><span data-ttu-id="9f6da-237">Любой</span><span class="sxs-lookup"><span data-stu-id="9f6da-237">Any</span></span></p></td>
<td><p><span data-ttu-id="9f6da-238">Служба прокси XMPP отправляет трафик на XMPPные контакты в определенных XMPP Федерации</span><span class="sxs-lookup"><span data-stu-id="9f6da-238">XMPP Proxy service sends traffic to XMPP contacts in defined XMPP federations</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f6da-239">Access/SIP (TLS)/TCP/443</span><span class="sxs-lookup"><span data-stu-id="9f6da-239">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="9f6da-240">Любой</span><span class="sxs-lookup"><span data-stu-id="9f6da-240">Any</span></span></p></td>
<td><p><span data-ttu-id="9f6da-241">Общедоступный виртуальный IP-адрес службы пограничного доступа</span><span class="sxs-lookup"><span data-stu-id="9f6da-241">Access Edge service public VIP address</span></span></p></td>
<td><p><span data-ttu-id="9f6da-242">Трафик SIP "клиент-сервер" для доступа внешних пользователей</span><span class="sxs-lookup"><span data-stu-id="9f6da-242">Client-to-server SIP traffic for external user access</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f6da-243">Access/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="9f6da-243">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="9f6da-244">Любой</span><span class="sxs-lookup"><span data-stu-id="9f6da-244">Any</span></span></p></td>
<td><p><span data-ttu-id="9f6da-245">Общедоступный виртуальный IP-адрес службы пограничного доступа</span><span class="sxs-lookup"><span data-stu-id="9f6da-245">Access Edge service public VIP address</span></span></p></td>
<td><p><span data-ttu-id="9f6da-246">Передача сигналов SIP, Федеративные и общедоступные возможности обмена мгновенными сообщениями с помощью SIP</span><span class="sxs-lookup"><span data-stu-id="9f6da-246">SIP signaling, federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f6da-247">Access/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="9f6da-247">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="9f6da-248">Общедоступный виртуальный IP-адрес службы пограничного доступа</span><span class="sxs-lookup"><span data-stu-id="9f6da-248">Access Edge service public VIP address</span></span></p></td>
<td><p><span data-ttu-id="9f6da-249">Федеративный партнер</span><span class="sxs-lookup"><span data-stu-id="9f6da-249">Federated partner</span></span></p></td>
<td><p><span data-ttu-id="9f6da-250">Передача сигналов SIP, Федеративные и общедоступные возможности обмена мгновенными сообщениями с помощью SIP</span><span class="sxs-lookup"><span data-stu-id="9f6da-250">SIP signaling, federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f6da-251">Веб-конференции/PSOM (TLS)/TCP/443</span><span class="sxs-lookup"><span data-stu-id="9f6da-251">Web Conferencing/PSOM(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="9f6da-252">Любой</span><span class="sxs-lookup"><span data-stu-id="9f6da-252">Any</span></span></p></td>
<td><p><span data-ttu-id="9f6da-253">Общедоступный виртуальный IP-адрес службы пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="9f6da-253">Edge Server Web Conferencing Edge service public VIP address</span></span></p></td>
<td><p><span data-ttu-id="9f6da-254">Мультимедиа для веб-конференций</span><span class="sxs-lookup"><span data-stu-id="9f6da-254">Web Conferencing media</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f6da-255">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="9f6da-255">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="9f6da-256">Любой</span><span class="sxs-lookup"><span data-stu-id="9f6da-256">Any</span></span></p></td>
<td><p><span data-ttu-id="9f6da-257">Сервер пограничного сервера A/V (внешний IP-адрес для службы EDGE)</span><span class="sxs-lookup"><span data-stu-id="9f6da-257">Edge Server A/V Edge service public VIP address</span></span></p></td>
<td><p><span data-ttu-id="9f6da-258">STUN/отключите согласование кандидатов по протоколу UDP/3478</span><span class="sxs-lookup"><span data-stu-id="9f6da-258">STUN/TURN negotiation of candidates over UDP/3478</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f6da-259">A/V/STUN, MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="9f6da-259">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="9f6da-260">Любой</span><span class="sxs-lookup"><span data-stu-id="9f6da-260">Any</span></span></p></td>
<td><p><span data-ttu-id="9f6da-261">Сервер пограничного сервера A/V (внешний IP-адрес для службы EDGE)</span><span class="sxs-lookup"><span data-stu-id="9f6da-261">Edge Server A/V Edge service public VIP address</span></span></p></td>
<td><p><span data-ttu-id="9f6da-262">STUN/отключите согласование кандидатов по протоколу TCP/443</span><span class="sxs-lookup"><span data-stu-id="9f6da-262">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="firewall-summary-for-scaled-consolidated-edge-hardware-load-balanced-internal-interface-virtual-ips"></a><span data-ttu-id="9f6da-263">Сводка по межсетевому экрану для масштабируемой консолидированной границы, аппаратной балансировки нагрузки: Внутренние виртуальные IP – адреса интерфейса</span><span class="sxs-lookup"><span data-stu-id="9f6da-263">Firewall Summary for Scaled Consolidated Edge, Hardware Load Balanced: Internal Interface Virtual IPs</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9f6da-264">Role/Protocol/TCP/UDP/порт</span><span class="sxs-lookup"><span data-stu-id="9f6da-264">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="9f6da-265">IP-адрес источника</span><span class="sxs-lookup"><span data-stu-id="9f6da-265">Source IP address</span></span></th>
<th><span data-ttu-id="9f6da-266">IP-адрес назначения</span><span class="sxs-lookup"><span data-stu-id="9f6da-266">Destination IP address</span></span></th>
<th><span data-ttu-id="9f6da-267">Примечания.</span><span class="sxs-lookup"><span data-stu-id="9f6da-267">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9f6da-268">Access/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="9f6da-268">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="9f6da-269">Any (может быть определено как режиссер, виртуальный IP-адрес пула режиссера, виртуальный IP-адрес внешнего сервера или пула переднего плана)</span><span class="sxs-lookup"><span data-stu-id="9f6da-269">Any (can be defined as Director, Director pool virtual IP address, Front End Server or Front End pool virtual IP address)</span></span></p></td>
<td><p><span data-ttu-id="9f6da-270">Интерфейс внутренних виртуальных IP-адресов пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="9f6da-270">Edge Server Internal VIP interface</span></span></p></td>
<td><p><span data-ttu-id="9f6da-271">Исходящий трафик SIP (от режиссера, виртуальный IP-адрес пула, сервер переднего плана, виртуальный IP-адрес пула переднего плана) до внутреннего граничного сервера.</span><span class="sxs-lookup"><span data-stu-id="9f6da-271">Outbound SIP traffic (from Director, Director pool virtual IP address, Front End Server or Front End pool virtual IP address)to Internal Edge VIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f6da-272">Access/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="9f6da-272">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="9f6da-273">Интерфейс внутренних виртуальных IP-адресов пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="9f6da-273">Edge Server Internal VIP interface</span></span></p></td>
<td><p><span data-ttu-id="9f6da-274">Any (может быть определено как режиссер, виртуальный IP-адрес пула режиссера, виртуальный IP-адрес внешнего сервера или пула переднего плана)</span><span class="sxs-lookup"><span data-stu-id="9f6da-274">Any (can be defined as Director, Director pool virtual IP address, Front End Server or Front End pool virtual IP address)</span></span></p></td>
<td><p><span data-ttu-id="9f6da-275">Входящий трафик SIP (для режиссера, виртуального IP-адреса пула пулов, сервер переднего плана и виртуальный IP-адрес пула переднего плана) от внутреннего интерфейса пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="9f6da-275">Inbound SIP traffic (to Director, Director pool virtual IP address, Front End Server or Front End pool virtual IP address) from Edge Server internal interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f6da-276">SIP/MTLS/TCP/5062</span><span class="sxs-lookup"><span data-stu-id="9f6da-276">SIP/MTLS/TCP/5062</span></span></p></td>
<td><p><span data-ttu-id="9f6da-277">Any (может быть как IP-адресом переднего сервера, так и IP-адресом пула переднего плана либо любым бесперебойно работающее устройство филиала или с помощью этого пограничного сервера).</span><span class="sxs-lookup"><span data-stu-id="9f6da-277">Any (can be defined as Front End Server IP address, or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server)</span></span></p></td>
<td><p><span data-ttu-id="9f6da-278">Интерфейс внутренних виртуальных IP-адресов пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="9f6da-278">Edge Server Internal VIP interface</span></span></p></td>
<td><p><span data-ttu-id="9f6da-279">Проверка подлинности пользователей/V (служба проверки подлинности A/V) от IP-адреса сервера переднего плана или переднего плана, а также от любого работающего филиала или сервера с бесперебойной подразделением с помощью этого пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="9f6da-279">Authentication of A/V users (A/V authentication service) from Front End Server or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f6da-280">STUN/MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="9f6da-280">STUN/MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="9f6da-281">Любой</span><span class="sxs-lookup"><span data-stu-id="9f6da-281">Any</span></span></p></td>
<td><p><span data-ttu-id="9f6da-282">Интерфейс внутренних виртуальных IP-адресов пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="9f6da-282">Edge Server Internal VIP interface</span></span></p></td>
<td><p><span data-ttu-id="9f6da-283">Предпочтительный путь для передачи мультимедиа между внутренними и внешними пользователями</span><span class="sxs-lookup"><span data-stu-id="9f6da-283">Preferred path for A/V media transfer between internal and external users</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f6da-284">STUN/MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="9f6da-284">STUN/MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="9f6da-285">Любой</span><span class="sxs-lookup"><span data-stu-id="9f6da-285">Any</span></span></p></td>
<td><p><span data-ttu-id="9f6da-286">Интерфейс внутренних виртуальных IP-адресов пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="9f6da-286">Edge Server Internal VIP interface</span></span></p></td>
<td><p><span data-ttu-id="9f6da-287">Резервный путь для передачи мультимедиа между внутренними и внешними пользователями если не удается установить UDP-связь, используется протокол TCP для обмена файлами и демонстрации рабочего стола</span><span class="sxs-lookup"><span data-stu-id="9f6da-287">Fallback path for A/V media transfer between internal and external users if UDP communication cannot be established, TCP is used for file transfer and desktop sharing</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f6da-288">STUN/MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="9f6da-288">STUN/MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="9f6da-289">Интерфейс внутренних виртуальных IP-адресов пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="9f6da-289">Edge Server Internal VIP interface</span></span></p></td>
<td><p><span data-ttu-id="9f6da-290">Любой</span><span class="sxs-lookup"><span data-stu-id="9f6da-290">Any</span></span></p></td>
<td><p><span data-ttu-id="9f6da-291">Резервный путь для передачи мультимедиа между внутренними и внешними пользователями если не удается установить UDP-связь, используется протокол TCP для обмена файлами и демонстрации рабочего стола</span><span class="sxs-lookup"><span data-stu-id="9f6da-291">Fallback path for A/V media transfer between internal and external users if UDP communication cannot be established, TCP is used for file transfer and desktop sharing</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="9f6da-292">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9f6da-292">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

