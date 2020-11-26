---
title: Требования к балансировке нагрузки для Lync Server 2013
description: Требования к балансировке нагрузки для Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Load balancing requirements
ms:assetid: 84489328-64a4-486c-9384-a3e5c8ed9c8b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615011(v=OCS.15)
ms:contentKeyID: 48184697
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a768b2cbfe444e6915c932835d3cc2abaf6a98c3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426566"
---
# <a name="load-balancing-requirements-for-lync-server-2013"></a><span data-ttu-id="01ac7-103">Требования балансировки нагрузки для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="01ac7-103">Load balancing requirements for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="01ac7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="01ac7-104">

<span> </span></span></span>

<span data-ttu-id="01ac7-105">_**Тема последнего изменения:** 2012-10-05_</span><span class="sxs-lookup"><span data-stu-id="01ac7-105">_**Topic Last Modified:** 2012-10-05_</span></span>

<span data-ttu-id="01ac7-106">Если у вас есть пулы, пулы или пограничные серверы, вам потребуется развернуть балансировку нагрузки для этих пулов.</span><span class="sxs-lookup"><span data-stu-id="01ac7-106">If you have Front End pools, Director pools, or Edge Server pools, you need to deploy load balancing for these pools.</span></span> <span data-ttu-id="01ac7-107">Load balancing distributes the traffic among the servers in a pool.</span><span class="sxs-lookup"><span data-stu-id="01ac7-107">Load balancing distributes the traffic among the servers in a pool.</span></span>

<span data-ttu-id="01ac7-108">Lync Server 2013 поддерживает два типа решений для балансировки нагрузки при обмене данными между клиентами: Балансировка нагрузки DNS и балансировка нагрузки оборудования.</span><span class="sxs-lookup"><span data-stu-id="01ac7-108">Lync Server 2013 supports two types of load balancing solutions for client-to-server traffic: Domain Name System (DNS) load balancing and hardware load balancing.</span></span> <span data-ttu-id="01ac7-109">Балансировка нагрузки DNS обеспечивает ряд преимуществ, включая упрощенное администрирование, более эффективное устранение неполадок и возможность изолировать весь трафик Lync Server от любых потенциальных проблем системы балансировки нагрузки оборудования.</span><span class="sxs-lookup"><span data-stu-id="01ac7-109">DNS load balancing offers several advantages including simpler administration, more efficient troubleshooting, and the ability to isolate much of your Lync Server traffic from any potential hardware load balancer problems.</span></span>

<span data-ttu-id="01ac7-110">Выберите решение балансировки нагрузки для каждого пула в развертывании, учитывая следующие ограничения:</span><span class="sxs-lookup"><span data-stu-id="01ac7-110">Decide which load balancing solution is appropriate for each pool in your deployment, keeping in mind the following restrictions:</span></span>

  - <span data-ttu-id="01ac7-p103">Внутренний и внешний пограничные интерфейсы должны использовать одинаковые типы решений балансировки нагрузки. Вы не можете использовать балансировку нагрузки на DNS на одном интерфейсе и аппаратную балансировку на другом.</span><span class="sxs-lookup"><span data-stu-id="01ac7-p103">The internal Edge interface and external Edge interface must use the same type of load balancing. You cannot use DNS load balancing on one interface and hardware load balancing on the other.</span></span>

  - <span data-ttu-id="01ac7-p104">Для некоторых типов трафика требуется аппаратный балансировщик нагрузки. Например для трафика HTTP вместо балансировки нагрузки на DNS требуется аппаратный балансировщик нагрузки. Балансировка нагрузки на DNS не работает с веб-трафиком "клиент-сервер".</span><span class="sxs-lookup"><span data-stu-id="01ac7-p104">Some types of traffic require a hardware load balancer. For example, HTTP traffic requires a hardware load balancer instead of DNS load balancing. DNS load balancing does not work with client-to-server web traffic.</span></span>

<span data-ttu-id="01ac7-116">Дополнительные сведения о выборе решения для аппаратной подсистемы балансировки нагрузки можно найти в разделе [требования к оборудованию балансировки нагрузки для Lync Server 2013](lync-server-2013-hardware-load-balancer-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="01ac7-116">For more details about choosing a hardware load balancer solution, see [Hardware load balancer requirements for Lync Server 2013](lync-server-2013-hardware-load-balancer-requirements.md).</span></span>

<span data-ttu-id="01ac7-117">Если в качестве решения для пула вы выбрали балансировку нагрузки на DNS, но вам по-прежнему требуются аппаратные балансировщики нагрузки для определенных видов трафика, например HTTP, то администрирование аппаратных балансировщиков нагрузки существенно упрощается.</span><span class="sxs-lookup"><span data-stu-id="01ac7-117">If you choose to use DNS load balancing for a pool but still need to implement hardware load balancers for traffic such as HTTP traffic, the administration of the hardware load balancers is greatly simplified.</span></span> <span data-ttu-id="01ac7-118">Например настройка аппаратного балансировщика нагрузки будет упрощена, поскольку потребуется управлять только трафиком HTTP и HTTPS, а для управления остальными протоколами будет использоваться балансировка нагрузки на DNS.</span><span class="sxs-lookup"><span data-stu-id="01ac7-118">For example, configuring the hardware load balancer will be simpler as it will only manage the HTTP and HTTPS traffic, while all other protocols will be managed by DNS load balancing.</span></span> <span data-ttu-id="01ac7-119">Дополнительные сведения можно найти [в разделе Балансировка нагрузки DNS в Lync Server 2013](lync-server-2013-dns-load-balancing.md).</span><span class="sxs-lookup"><span data-stu-id="01ac7-119">For details, see [DNS load balancing in Lync Server 2013](lync-server-2013-dns-load-balancing.md).</span></span>

<span data-ttu-id="01ac7-120">Для трафика "сервер-сервер" в Lync Server 2013 используется балансировка нагрузки, учитывающая топологию.</span><span class="sxs-lookup"><span data-stu-id="01ac7-120">For server-to-server traffic, Lync Server 2013 uses topology-aware load balancing.</span></span> <span data-ttu-id="01ac7-121">Серверы считывают опубликованную топологию в хранилище Центрального управления для получения полных доменных имен серверов в топологии и автоматически распространяют трафик между серверами.</span><span class="sxs-lookup"><span data-stu-id="01ac7-121">Servers read the published topology in the Central Management store to obtain the FQDNs of servers in the topology, and automatically distribute the traffic among the servers.</span></span> <span data-ttu-id="01ac7-122">Administrators do not need to set up or manage this type of load balancing.</span><span class="sxs-lookup"><span data-stu-id="01ac7-122">Administrators do not need to set up or manage this type of load balancing.</span></span>

<span data-ttu-id="01ac7-p107">Если используется балансировка DNS-нагрузки и требуется блокировать трафик на конкретный компьютер, недостаточно просто удалить записи IP-адреса из полного имени домена пула. Необходимо также удалить DNS-запись для этого компьютера.</span><span class="sxs-lookup"><span data-stu-id="01ac7-p107">If you use DNS load balancing and you need to block traffic to a specific computer, it is not sufficient to just remove the IP address entries from the Pool FQDN. You must remove the DNS entry for the computer as well.</span></span>

<span data-ttu-id="01ac7-125"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="01ac7-125"></div>

<span> </span>

</div>

</div>

</span></span></div>

