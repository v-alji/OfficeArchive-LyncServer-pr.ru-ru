---
title: Требования к портам Lync Server 2013
description: Требования к портам Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port requirements
ms:assetid: 9a6c1300-ef88-4181-a8f1-43cd3093962b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398798(v=OCS.15)
ms:contentKeyID: 48184886
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ba7ae9a1ee098f55c61ae476f12c3b856c69f90e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424396"
---
# <a name="port-requirements-for-lync-server-2013"></a><span data-ttu-id="4c89b-103">Требования к портам для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4c89b-103">Port requirements for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4c89b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4c89b-104">

<span> </span></span></span>

<span data-ttu-id="4c89b-105">_**Тема последнего изменения:** 2013-03-27_</span><span class="sxs-lookup"><span data-stu-id="4c89b-105">_**Topic Last Modified:** 2013-03-27_</span></span>

<span data-ttu-id="4c89b-106">На Lync Server необходимо открыть определенные порты брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="4c89b-106">Lync Server requires that specific ports on the firewall be open.</span></span> <span data-ttu-id="4c89b-107">Кроме того, если в организации развернут протокол IPsec, то он должен быть отключен в диапазоне портов, используемых для доставки звука, видео и панорамного видео.</span><span class="sxs-lookup"><span data-stu-id="4c89b-107">Additionally, if Internet Protocol security (IPsec) is deployed in your organization, IPsec must be disabled over the range of ports used for the delivery of audio, video, and panorama video.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="4c89b-108">Содержание</span><span class="sxs-lookup"><span data-stu-id="4c89b-108">In This Section</span></span>

<span data-ttu-id="4c89b-109">Этот раздел содержит следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="4c89b-109">This section includes the following topics:</span></span>

  - [<span data-ttu-id="4c89b-110">Порты и протоколы для внутренних серверов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4c89b-110">Ports and protocols for internal servers in Lync Server 2013</span></span>](lync-server-2013-ports-and-protocols-for-internal-servers.md)

  - [<span data-ttu-id="4c89b-111">Исключения IPsec в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4c89b-111">IPsec exceptions in Lync Server 2013</span></span>](lync-server-2013-ipsec-exceptions.md)

  - [<span data-ttu-id="4c89b-112">Сводка по портам — единая консолидированная пограничная топология с закрытыми IP-адресами и трансляцией сетевых адресов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4c89b-112">Port summary - Single consolidated edge with private IP addresses using NAT in Lync Server 2013</span></span>](lync-server-2013-port-summary-single-consolidated-edge-with-private-ip-addresses-using-nat.md)

  - [<span data-ttu-id="4c89b-113">Сводка по портам — единая консолидированная пограничная топология с общедоступными IP-адресами в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4c89b-113">Port summary - Single consolidated edge with public IP addresses in Lync Server 2013</span></span>](lync-server-2013-port-summary-single-consolidated-edge-with-public-ip-addresses.md)

  - [<span data-ttu-id="4c89b-114">Сводка по портам — масштабируемая консолидированная пограничная топология, балансировка нагрузки на DNS с закрытыми IP-адресами и трансляцией сетевых адресов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4c89b-114">Port summary - Scaled consolidated edge, DNS load balancing with private IP addresses using NAT in Lync Server 2013</span></span>](lync-server-2013-port-summary-scaled-consolidated-edge-dns-load-balancing-with-private-ip-addresses-using-nat.md)

  - [<span data-ttu-id="4c89b-115">Сводка по портам — масштабируемая консолидированная пограничная топология, балансировка нагрузки на DNS с общедоступными IP-адресами в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4c89b-115">Port summary - Scaled consolidated edge, DNS load balancing with public IP addresses in Lync Server 2013</span></span>](lync-server-2013-port-summary-scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses.md)

  - [<span data-ttu-id="4c89b-116">Сводка по портам — масштабируемая консолидированная пограничная топология с аппаратными балансировщиками нагрузки в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4c89b-116">Port summary - Scaled consolidated edge with hardware load balancers in Lync Server 2013</span></span>](lync-server-2013-port-summary-scaled-consolidated-edge-with-hardware-load-balancers.md)

  - [<span data-ttu-id="4c89b-117">Сводка по портам — обратный прокси-сервер в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4c89b-117">Port summary - Reverse proxy in Lync Server 2013</span></span>](lync-server-2013-port-summary-reverse-proxy.md)

  - [<span data-ttu-id="4c89b-118">Общие сведения о портах: SIP, Федерация XMPP и общедоступная служба обмена мгновенными сообщениями в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4c89b-118">Port summary - SIP, XMPP federation, and public instant messaging in Lync Server 2013</span></span>](lync-server-2013-port-summary-sip-xmpp-federation-and-public-instant-messaging.md)

<span data-ttu-id="4c89b-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4c89b-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

