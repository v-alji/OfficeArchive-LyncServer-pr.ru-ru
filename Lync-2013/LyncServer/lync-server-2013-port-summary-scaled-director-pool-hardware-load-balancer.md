---
title: 'Lync Server 2013: сводка по портам — vасштабируемый пул директоров, аппаратный балансировщик нагрузки'
description: 'Lync Server 2013: "Сводка по порту — масштабируемый Режиссерный пул, подсистема балансировки нагрузки для оборудования".'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - Scaled Director pool, hardware load balancer
ms:assetid: 6ae2f4ac-5b64-4e45-8253-133308f5812d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204983(v=OCS.15)
ms:contentKeyID: 48184434
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 10bfb3a3ad3a38b6cb0e46414bf22deecc71d7b5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442798"
---
# <a name="port-summary---scaled-director-pool-hardware-load-balancer-in-lync-server-2013"></a><span data-ttu-id="b036f-103">Сводка по портам — vасштабируемый пул директоров, аппаратный балансировщик нагрузки в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b036f-103">Port summary - Scaled Director pool, hardware load balancer in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b036f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b036f-104">

<span> </span></span></span>

<span data-ttu-id="b036f-105">_**Тема последнего изменения:** 2012-10-21_</span><span class="sxs-lookup"><span data-stu-id="b036f-105">_**Topic Last Modified:** 2012-10-21_</span></span>

<span data-ttu-id="b036f-106">Требования к порту межсетевого экрана для пула режиссера состоят из портов, используемых для установления связи с режиссером из внутреннего интерфейса пограничного сервера или внутреннего интерфейса обратного прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="b036f-106">Firewall port requirements for a Director pool consist of the ports that are used to establish communication with the Director from the internal interface of the Edge Server or internal-facing interface of the reverse proxy.</span></span> <span data-ttu-id="b036f-107">По умолчанию Microsoft Lync Server 2013 ожидает, что порты HTTP/TCP 8080 и HTTPS/TCP 4443 будут открыты из обратного прокси-сервера в директор, а также с интерфейсом пула и сервера переднего плана.</span><span class="sxs-lookup"><span data-stu-id="b036f-107">Microsoft Lync Server 2013 by default expects ports HTTP/TCP 8080 and HTTPS/TCP 4443 to be open from the reverse proxy to the Director, as well as the Front End pool and Front End Server.</span></span> <span data-ttu-id="b036f-108">Кроме того, между внутренним интерфейсом пограничного сервера и пулом, а также интерфейсом сервера и переднего плана должен быть установлен протокол SIP.</span><span class="sxs-lookup"><span data-stu-id="b036f-108">Additionally, there must be session initiation protocol (SIP) communication from the Edge Server internal interface to the Director and to the Front End pool and Front End Server.</span></span> <span data-ttu-id="b036f-109">Протокол SIP использует интерфейс SIP/MTLS/TCP 5061 с пограничного сервера до пула переднего плана и сервера переднего плана.</span><span class="sxs-lookup"><span data-stu-id="b036f-109">The SIP protocol uses SIP/MTLS/TCP 5061 from the Edge Server to the Front End pool and Front End Server.</span></span> <span data-ttu-id="b036f-110">Кроме того, необходимо также создать правило, которое позволяет использовать интерфейс SIP/MTLS/TCP 5061, входящий в состав внешнего интерфейса пограничного сервера и сервера переднего плана.</span><span class="sxs-lookup"><span data-stu-id="b036f-110">A rule that allows SIP/MTLS/TCP 5061 communication from the Director, Front End pool and Front End Server to the Edge Server internal interface must be created as well.</span></span>

### <a name="director-ports-and-protocols-for-firewall-definitions"></a><span data-ttu-id="b036f-111">Сетевые порты и протоколы для определений брандмауэра</span><span class="sxs-lookup"><span data-stu-id="b036f-111">Director Ports and Protocols for Firewall Definitions</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b036f-112">Role/Protocol/TCP/UDP/порт</span><span class="sxs-lookup"><span data-stu-id="b036f-112">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="b036f-113">IP-адрес источника</span><span class="sxs-lookup"><span data-stu-id="b036f-113">Source IP address</span></span></th>
<th><span data-ttu-id="b036f-114">IP-адрес назначения</span><span class="sxs-lookup"><span data-stu-id="b036f-114">Destination IP address</span></span></th>
<th><span data-ttu-id="b036f-115">Примечания.</span><span class="sxs-lookup"><span data-stu-id="b036f-115">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b036f-116">HTTP/TCP 8080</span><span class="sxs-lookup"><span data-stu-id="b036f-116">HTTP/TCP 8080</span></span></p></td>
<td><p><span data-ttu-id="b036f-117">Внутренний прокси-интерфейс обратной стороне</span><span class="sxs-lookup"><span data-stu-id="b036f-117">Reverse proxy internal interface</span></span></p></td>
<td><p><span data-ttu-id="b036f-118">IP-адрес подсистемы балансировки нагрузки для режиссера</span><span class="sxs-lookup"><span data-stu-id="b036f-118">Director Hardware Load Balancer VIP</span></span></p></td>
<td><p><span data-ttu-id="b036f-119">По умолчанию получил внешняя сторона обратного прокси-сервера, связь передается в каталог HLB VIP и на сервер переднего плана.</span><span class="sxs-lookup"><span data-stu-id="b036f-119">Initially received by the external side of the reverse proxy, the communication is sent on to the Director HLB VIP and Front End Servers web services</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b036f-120">HTTPS/TCP 4443</span><span class="sxs-lookup"><span data-stu-id="b036f-120">HTTPS/TCP 4443</span></span></p></td>
<td><p><span data-ttu-id="b036f-121">Внутренний прокси-интерфейс обратной стороне</span><span class="sxs-lookup"><span data-stu-id="b036f-121">Reverse proxy internal interface</span></span></p></td>
<td><p><span data-ttu-id="b036f-122">IP-адрес подсистемы балансировки нагрузки для режиссера</span><span class="sxs-lookup"><span data-stu-id="b036f-122">Director Hardware Load Balancer VIP</span></span></p></td>
<td><p><span data-ttu-id="b036f-123">По умолчанию получил внешняя сторона обратного прокси-сервера, связь передается в каталог HLB VIP и на сервер переднего плана.</span><span class="sxs-lookup"><span data-stu-id="b036f-123">Initially received by the external side of the reverse proxy, the communication is sent on to the Director HLB VIP and Front End Servers web services</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b036f-124">HTTPS/TCP 444</span><span class="sxs-lookup"><span data-stu-id="b036f-124">HTTPS/TCP 444</span></span></p></td>
<td><p><span data-ttu-id="b036f-125">Директор</span><span class="sxs-lookup"><span data-stu-id="b036f-125">Director</span></span></p></td>
<td><p><span data-ttu-id="b036f-126">Пул переднего плана на сервере или внешнем интерфейсе</span><span class="sxs-lookup"><span data-stu-id="b036f-126">Front End Server or Front End pool</span></span></p></td>
<td><p><span data-ttu-id="b036f-127">Межсерверная связь между директором HLB VIP и серверами переднего плана</span><span class="sxs-lookup"><span data-stu-id="b036f-127">Inter-server communication between the Director HLB VIP and the Front End Servers</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b036f-128">HTTP/TCP 80</span><span class="sxs-lookup"><span data-stu-id="b036f-128">HTTP/TCP 80</span></span></p></td>
<td><p><span data-ttu-id="b036f-129">Внутренние клиенты</span><span class="sxs-lookup"><span data-stu-id="b036f-129">Internal Clients</span></span></p></td>
<td><p><span data-ttu-id="b036f-130">IP-адрес подсистемы балансировки нагрузки для режиссера</span><span class="sxs-lookup"><span data-stu-id="b036f-130">Director Hardware Load Balancer VIP</span></span></p></td>
<td><p><span data-ttu-id="b036f-131">Режиссер предоставляет веб-службы внутренним и внешним клиентам.</span><span class="sxs-lookup"><span data-stu-id="b036f-131">The Director provides web services to internal as well as external clients.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b036f-132">HTTPS/TCP 443</span><span class="sxs-lookup"><span data-stu-id="b036f-132">HTTPS/TCP 443</span></span></p></td>
<td><p><span data-ttu-id="b036f-133">Внутренние клиенты</span><span class="sxs-lookup"><span data-stu-id="b036f-133">Internal Clients</span></span></p></td>
<td><p><span data-ttu-id="b036f-134">IP-адрес подсистемы балансировки нагрузки для режиссера</span><span class="sxs-lookup"><span data-stu-id="b036f-134">Director Hardware Load Balancer VIP</span></span></p></td>
<td><p><span data-ttu-id="b036f-135">Режиссер предоставляет веб-службы внутренним и внешним клиентам.</span><span class="sxs-lookup"><span data-stu-id="b036f-135">The Director provides web services to internal as well as external clients.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b036f-136">SIP/MTLS/TCP 5061</span><span class="sxs-lookup"><span data-stu-id="b036f-136">SIP/MTLS/TCP 5061</span></span></p></td>
<td><p><span data-ttu-id="b036f-137">Внутренний интерфейс пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="b036f-137">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="b036f-138">IP-адрес подсистемы балансировки нагрузки для режиссера</span><span class="sxs-lookup"><span data-stu-id="b036f-138">Director Hardware Load Balancer VIP</span></span></p></td>
<td><p><span data-ttu-id="b036f-139">Обмен данными SIP от пограничного сервера к директору и к серверам переднего плана.</span><span class="sxs-lookup"><span data-stu-id="b036f-139">SIP communication from the Edge Server to the Director, and Front End Servers.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b036f-140">MTLS/TCP/50001</span><span class="sxs-lookup"><span data-stu-id="b036f-140">MTLS/TCP/50001</span></span></p></td>
<td><p><span data-ttu-id="b036f-141">Любой</span><span class="sxs-lookup"><span data-stu-id="b036f-141">Any</span></span></p></td>
<td><p><span data-ttu-id="b036f-142">Директор</span><span class="sxs-lookup"><span data-stu-id="b036f-142">Director</span></span></p></td>
<td><p><span data-ttu-id="b036f-143">Команды для централизованного ведения журналов (ClsController.exe) или агента (ClsAgent.exe) и сбора журналов</span><span class="sxs-lookup"><span data-stu-id="b036f-143">Centralized Logging Service controller (ClsController.exe) or agent (ClsAgent.exe)commands and log collection</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b036f-144">MTLS/TCP/50002</span><span class="sxs-lookup"><span data-stu-id="b036f-144">MTLS/TCP/50002</span></span></p></td>
<td><p><span data-ttu-id="b036f-145">Любой</span><span class="sxs-lookup"><span data-stu-id="b036f-145">Any</span></span></p></td>
<td><p><span data-ttu-id="b036f-146">Директор</span><span class="sxs-lookup"><span data-stu-id="b036f-146">Director</span></span></p></td>
<td><p><span data-ttu-id="b036f-147">Команды для централизованного ведения журналов (ClsController.exe) или агента (ClsAgent.exe) и сбора журналов</span><span class="sxs-lookup"><span data-stu-id="b036f-147">Centralized Logging Service controller (ClsController.exe) or agent (ClsAgent.exe)commands and log collection</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b036f-148">MTLS/TCP/50003</span><span class="sxs-lookup"><span data-stu-id="b036f-148">MTLS/TCP/50003</span></span></p></td>
<td><p><span data-ttu-id="b036f-149">Любой</span><span class="sxs-lookup"><span data-stu-id="b036f-149">Any</span></span></p></td>
<td><p><span data-ttu-id="b036f-150">Директор</span><span class="sxs-lookup"><span data-stu-id="b036f-150">Director</span></span></p></td>
<td><p><span data-ttu-id="b036f-151">Команды для централизованного ведения журналов (ClsController.exe) или агента (ClsAgent.exe) и сбора журналов</span><span class="sxs-lookup"><span data-stu-id="b036f-151">Centralized Logging Service controller (ClsController.exe) or agent (ClsAgent.exe)commands and log collection</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="b036f-152">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b036f-152">


</div>

<span> </span>

</div>

</div>

</span></span></div>

