---
title: Масштабируемый пул директоров — балансировка нагрузки на DNS и аппаратный балансировщик нагрузки
description: Масштабируемый пул режиссеров — балансировка нагрузки DNS и балансировщик нагрузки оборудования.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Scaled Director pool - DNS load balancing and hardware load balancer
ms:assetid: a1f6ffc0-9e6e-4217-a923-025c9679e154
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205142(v=OCS.15)
ms:contentKeyID: 48185023
ms.date: 03/29/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b30dfcc3515420ffb34343e4653e9518b1b9c3ed
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442060"
---
# <a name="scaled-director-pool---dns-load-balancing-and-hardware-load-balancer-in-lync-server-2013"></a><span data-ttu-id="b1e3b-103">Масштабируемый пул директоров — балансировка нагрузки на DNS и аппаратный балансировщик нагрузки в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b1e3b-103">Scaled Director pool - DNS load balancing and hardware load balancer in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b1e3b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b1e3b-104">

<span> </span></span></span>

<span data-ttu-id="b1e3b-105">_**Тема последнего изменения:** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="b1e3b-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="b1e3b-106">Масштабируемый пул режиссеров, на котором развернуты более одного режиссера для обработки дополнительной емкости и обеспечения высокой доступности, требуется балансировка нагрузки для распространения взаимодействия между клиентом и сервером со всеми участниками пула.</span><span class="sxs-lookup"><span data-stu-id="b1e3b-106">A scaled Director pool, where there are more than one Director deployed to handle additional capacity and to provide high availability, requires load balancing to distribute client and server communication to all members of the pool.</span></span> <span data-ttu-id="b1e3b-107">В режиссере веб-службы размещаются очень похоже на внешний интерфейс пула.</span><span class="sxs-lookup"><span data-stu-id="b1e3b-107">A Director hosts web services much like a Front End pool.</span></span> <span data-ttu-id="b1e3b-108">Для обеспечения балансировки нагрузки вы можете использовать аппаратную балансировку нагрузки или балансировку нагрузки DNS и аппаратную балансировку нагрузки.</span><span class="sxs-lookup"><span data-stu-id="b1e3b-108">To provide the load balancing, you can use either hardware load balancing or domain name system (DNS) load balancing and hardware load balancing.</span></span> <span data-ttu-id="b1e3b-109">Для веб-служб требуется балансировка нагрузки на оборудовании, а для балансировки нагрузки DNS — только возможности, необходимые для веб-служб.</span><span class="sxs-lookup"><span data-stu-id="b1e3b-109">Hardware load balancing is required for the web services, and DNS load balancing alone does not provide the capabilities required for the web services.</span></span>

<span data-ttu-id="b1e3b-110">В следующих разделах описаны вопросы планирования для развертывания пула с помощью балансировки нагрузки DNS в сочетании с аппаратным обеспечением балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="b1e3b-110">The following topics describe the planning considerations for deploying a Director pool using DNS load balancing in conjunction with hardware load balancing.</span></span> <span data-ttu-id="b1e3b-111">Если вы планируете использовать аппаратную балансировку нагрузки, но не балансировку нагрузки DNS для группового пула, ознакомьтесь с разделом [масштабированный пул пулов — подсистема подсистемы балансировки нагрузки оборудования в Lync Server 2013, в](lync-server-2013-scaled-director-pool-hardware-load-balancer.md) которой описаны требования к планированию для этой топологии.</span><span class="sxs-lookup"><span data-stu-id="b1e3b-111">If you intend to use hardware load balancing, but not DNS load balancing for the Director pool, see the topic [Scaled Director pool - hardware load balancer in Lync Server 2013](lync-server-2013-scaled-director-pool-hardware-load-balancer.md) that describes the planning requirements for that topology.</span></span>

<span data-ttu-id="b1e3b-112">![Масштабируемый пул режиссеров](images/JJ205142.35a78a7a-b781-4c8f-951e-168451ba6a65(OCS.15).jpg "Масштабируемый пул режиссеров")</span><span class="sxs-lookup"><span data-stu-id="b1e3b-112">![Scaled Director Pool](images/JJ205142.35a78a7a-b781-4c8f-951e-168451ba6a65(OCS.15).jpg "Scaled Director Pool")</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="b1e3b-113">Содержание</span><span class="sxs-lookup"><span data-stu-id="b1e3b-113">In This Section</span></span>

  - [<span data-ttu-id="b1e3b-114">Сводка по сертификатам — балансировка нагрузки на DNS и аппаратная балансировка нагрузки в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b1e3b-114">Certificate summary - DNS and HLB load balanced in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-dns-and-hlb-load-balanced.md)

  - [<span data-ttu-id="b1e3b-115">Сводка по портам — балансировка нагрузки на DNS и аппаратная балансировка нагрузки в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b1e3b-115">Port summary - DNS and HLB load balanced in Lync Server 2013</span></span>](lync-server-2013-port-summary-dns-and-hlb-load-balanced.md)

  - [<span data-ttu-id="b1e3b-116">Сводка по DNS — балансировка нагрузки на DNS и аппаратная балансировка нагрузки в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b1e3b-116">DNS summary - DNS and HLB load balanced in Lync Server 2013</span></span>](lync-server-2013-dns-summary-dns-and-hlb-load-balanced.md)

<span data-ttu-id="b1e3b-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b1e3b-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

