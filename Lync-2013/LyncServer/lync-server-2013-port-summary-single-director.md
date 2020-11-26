---
title: 'Lync Server 2013: сводка по портам — единственный директор'
description: 'Lync Server 2013: Общие сведения о портах — единый режиссер.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - Single Director
ms:assetid: 079c1414-723f-4499-b7d4-a0d7121c1626
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204648(v=OCS.15)
ms:contentKeyID: 48183322
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a46e394121dbc7dd6158016d39511e9487cec1ff
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436981"
---
# <a name="port-summary---single-director-in-lync-server-2013"></a><span data-ttu-id="5985f-103">Сводка по портам — единственный директор в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5985f-103">Port summary - Single Director in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5985f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5985f-104">

<span> </span></span></span>

<span data-ttu-id="5985f-105">_**Тема последнего изменения:** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="5985f-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="5985f-106">Требования к порту брандмауэра для единого режиссера состоят из портов, используемых для установления связи с режиссером из внутреннего интерфейса или внутренней сети обратного прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="5985f-106">Firewall port requirements for a single Director consist of the ports that are used to establish communication with the Director from the internal interface or internal-facing network of the reverse proxy.</span></span> <span data-ttu-id="5985f-107">По умолчанию Microsoft Lync Server 2013 ожидает, что порты HTTP/TCP 8080 и HTTPS/TCP 4443 будут открыты из обратного прокси-сервера в директор, а также с интерфейсом пула и сервера переднего плана.</span><span class="sxs-lookup"><span data-stu-id="5985f-107">Microsoft Lync Server 2013 by default expects ports HTTP/TCP 8080 and HTTPS/TCP 4443 to be open from the reverse proxy to the Director, as well as the Front End pool and Front End Server.</span></span> <span data-ttu-id="5985f-108">Кроме того, между внутренним интерфейсом пограничного сервера и пулом, а также интерфейсом сервера и переднего плана должен быть установлен протокол SIP.</span><span class="sxs-lookup"><span data-stu-id="5985f-108">Additionally, there must be session initiation protocol (SIP) communication from the Edge Server internal interface to the Director and to the Front End pool and Front End Server.</span></span> <span data-ttu-id="5985f-109">Протокол SIP использует интерфейс SIP/MTLS/TCP 5061 с пограничного сервера до пула переднего плана и сервера переднего плана.</span><span class="sxs-lookup"><span data-stu-id="5985f-109">The SIP protocol uses SIP/MTLS/TCP 5061 from the Edge Server to the Front End pool and Front End Server.</span></span> <span data-ttu-id="5985f-110">Кроме того, необходимо также создать правило, которое позволяет использовать интерфейс SIP/MTLS/TCP 5061, входящий в состав внешнего интерфейса пограничного сервера и сервера переднего плана.</span><span class="sxs-lookup"><span data-stu-id="5985f-110">A rule that allows SIP/MTLS/TCP 5061 communication from the Director, Front End pool and Front End Server to the Edge Server internal interface must be created as well.</span></span>

### <a name="single-director-ports-and-protocols-for-firewall-definitions"></a><span data-ttu-id="5985f-111">Порты и протоколы для отдельных режиссеров для определения брандмауэра</span><span class="sxs-lookup"><span data-stu-id="5985f-111">Single Director Ports and Protocols for Firewall Definitions</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5985f-112">Role/Protocol/TCP/UDP/порт</span><span class="sxs-lookup"><span data-stu-id="5985f-112">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="5985f-113">IP-адрес источника</span><span class="sxs-lookup"><span data-stu-id="5985f-113">Source IP address</span></span></th>
<th><span data-ttu-id="5985f-114">IP-адрес назначения</span><span class="sxs-lookup"><span data-stu-id="5985f-114">Destination IP address</span></span></th>
<th><span data-ttu-id="5985f-115">Примечания.</span><span class="sxs-lookup"><span data-stu-id="5985f-115">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5985f-116">HTTP/TCP 8080</span><span class="sxs-lookup"><span data-stu-id="5985f-116">HTTP/TCP 8080</span></span></p></td>
<td><p><span data-ttu-id="5985f-117">Внутренний прокси-интерфейс обратной стороне</span><span class="sxs-lookup"><span data-stu-id="5985f-117">Reverse proxy internal interface</span></span></p></td>
<td><p><span data-ttu-id="5985f-118">Директор</span><span class="sxs-lookup"><span data-stu-id="5985f-118">Director</span></span></p></td>
<td><p><span data-ttu-id="5985f-119">По внешнему каналу на обратной стороне обратных посредников связь передается на веб-службы Director и Front Server.</span><span class="sxs-lookup"><span data-stu-id="5985f-119">Initially received by the external side of the reverse proxy, the communication is sent on to the Director and Front End Server web services</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5985f-120">HTTPS/TCP 4443</span><span class="sxs-lookup"><span data-stu-id="5985f-120">HTTPS/TCP 4443</span></span></p></td>
<td><p><span data-ttu-id="5985f-121">Внутренний прокси-интерфейс обратной стороне</span><span class="sxs-lookup"><span data-stu-id="5985f-121">Reverse proxy internal interface</span></span></p></td>
<td><p><span data-ttu-id="5985f-122">Директор</span><span class="sxs-lookup"><span data-stu-id="5985f-122">Director</span></span></p></td>
<td><p><span data-ttu-id="5985f-123">По внешнему каналу на обратной стороне обратных посредников связь передается на веб-службы Director и Front Server.</span><span class="sxs-lookup"><span data-stu-id="5985f-123">Initially received by the external side of the reverse proxy, the communication is sent on to the Director and Front End Server web services</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5985f-124">HTTPS/TCP 444</span><span class="sxs-lookup"><span data-stu-id="5985f-124">HTTPS/TCP 444</span></span></p></td>
<td><p><span data-ttu-id="5985f-125">Директор</span><span class="sxs-lookup"><span data-stu-id="5985f-125">Director</span></span></p></td>
<td><p><span data-ttu-id="5985f-126">Пул переднего плана на сервере или внешнем интерфейсе</span><span class="sxs-lookup"><span data-stu-id="5985f-126">Front End server or Front End pool</span></span></p></td>
<td><p><span data-ttu-id="5985f-127">Обмен данными между сервером и сервером переднего плана</span><span class="sxs-lookup"><span data-stu-id="5985f-127">Inter-server communication between the Director and the Front End Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5985f-128">HTTP/TCP 80</span><span class="sxs-lookup"><span data-stu-id="5985f-128">HTTP/TCP 80</span></span></p></td>
<td><p><span data-ttu-id="5985f-129">Внутренние клиенты</span><span class="sxs-lookup"><span data-stu-id="5985f-129">Internal Clients</span></span></p></td>
<td><p><span data-ttu-id="5985f-130">Веб-службы режиссера</span><span class="sxs-lookup"><span data-stu-id="5985f-130">Director web services</span></span></p></td>
<td><p><span data-ttu-id="5985f-131">Режиссер предоставляет веб-службы внутренним и внешним клиентам.</span><span class="sxs-lookup"><span data-stu-id="5985f-131">The Director provides web services to internal and external clients.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5985f-132">HTTPS/TCP 443</span><span class="sxs-lookup"><span data-stu-id="5985f-132">HTTPS/TCP 443</span></span></p></td>
<td><p><span data-ttu-id="5985f-133">Внутренние клиенты</span><span class="sxs-lookup"><span data-stu-id="5985f-133">Internal Clients</span></span></p></td>
<td><p><span data-ttu-id="5985f-134">Веб-службы режиссера</span><span class="sxs-lookup"><span data-stu-id="5985f-134">Director web services</span></span></p></td>
<td><p><span data-ttu-id="5985f-135">Режиссер предоставляет веб-службы внутренним и внешним клиентам.</span><span class="sxs-lookup"><span data-stu-id="5985f-135">The Director provides web services to internal and external clients.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5985f-136">SIP/MTLS/TCP 5061</span><span class="sxs-lookup"><span data-stu-id="5985f-136">SIP/MTLS/TCP 5061</span></span></p></td>
<td><p><span data-ttu-id="5985f-137">Внутренний интерфейс пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="5985f-137">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="5985f-138">Директор</span><span class="sxs-lookup"><span data-stu-id="5985f-138">Director</span></span></p></td>
<td><p><span data-ttu-id="5985f-139">Обмен данными SIP от пограничного сервера к директоре и внешнему серверу.</span><span class="sxs-lookup"><span data-stu-id="5985f-139">SIP communication from the Edge Server to the Director, and the Front End Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5985f-140">MTLS/TCP/50001</span><span class="sxs-lookup"><span data-stu-id="5985f-140">MTLS/TCP/50001</span></span></p></td>
<td><p><span data-ttu-id="5985f-141">Любой</span><span class="sxs-lookup"><span data-stu-id="5985f-141">Any</span></span></p></td>
<td><p><span data-ttu-id="5985f-142">Внутренний интерфейс пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="5985f-142">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="5985f-143">Команды для централизованного ведения журналов (ClsController.exe) или агента (ClasAgent.exe) и сбора журналов</span><span class="sxs-lookup"><span data-stu-id="5985f-143">Centralized Logging Service controller (ClsController.exe) or agent (ClasAgent.exe)commands and log collection</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5985f-144">MTLS/TCP/50002</span><span class="sxs-lookup"><span data-stu-id="5985f-144">MTLS/TCP/50002</span></span></p></td>
<td><p><span data-ttu-id="5985f-145">Любой</span><span class="sxs-lookup"><span data-stu-id="5985f-145">Any</span></span></p></td>
<td><p><span data-ttu-id="5985f-146">Внутренний интерфейс пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="5985f-146">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="5985f-147">Команды для централизованного ведения журналов (ClsController.exe) или агента (ClasAgent.exe) и сбора журналов</span><span class="sxs-lookup"><span data-stu-id="5985f-147">Centralized Logging Service controller (ClsController.exe) or agent (ClasAgent.exe)commands and log collection</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5985f-148">MTLS/TCP/50003</span><span class="sxs-lookup"><span data-stu-id="5985f-148">MTLS/TCP/50003</span></span></p></td>
<td><p><span data-ttu-id="5985f-149">Любой</span><span class="sxs-lookup"><span data-stu-id="5985f-149">Any</span></span></p></td>
<td><p><span data-ttu-id="5985f-150">Внутренний интерфейс пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="5985f-150">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="5985f-151">Команды для централизованного ведения журналов (ClsController.exe) или агента (ClasAgent.exe) и сбора журналов</span><span class="sxs-lookup"><span data-stu-id="5985f-151">Centralized Logging Service controller (ClsController.exe) or agent (ClasAgent.exe)commands and log collection</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="5985f-152">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5985f-152">


</div>

<span> </span>

</div>

</div>

</span></span></div>

