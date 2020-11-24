---
title: 'Lync Server 2013: масштабируемый пул директоров — аппаратный балансировщик нагрузки'
description: 'Lync Server 2013: масштабируемый Режиссерный пул — подсистема балансировки нагрузки оборудования.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Scaled Director pool - hardware load balancer
ms:assetid: cf34759a-b384-479c-855f-ea5e80a234b6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205316(v=OCS.15)
ms:contentKeyID: 48185585
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 022c5afb67687149f8ba24655be2a1461d4371f2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398137"
---
# <a name="scaled-director-pool---hardware-load-balancer-in-lync-server-2013"></a><span data-ttu-id="abfb3-103">Масштабируемый пул директоров — аппаратный балансировщик нагрузки в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="abfb3-103">Scaled Director pool - hardware load balancer in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="abfb3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="abfb3-104">

<span> </span></span></span>

<span data-ttu-id="abfb3-105">_**Тема последнего изменения:** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="abfb3-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="abfb3-106">Масштабируемый пул, на котором развернуто несколько режиссеров для обработки дополнительной мощности и обеспечения высокой доступности, требуется балансировка нагрузки для распространения взаимодействия между клиентом и сервером со всеми участниками пула.</span><span class="sxs-lookup"><span data-stu-id="abfb3-106">A scaled Director pool, where there are more than one Director is deployed to handle additional capacity and to provide high availability, requires load balancing to distribute client and server communication to all members of the pool.</span></span> <span data-ttu-id="abfb3-107">В режиссере веб-службы размещаются очень похоже на внешний интерфейс пула.</span><span class="sxs-lookup"><span data-stu-id="abfb3-107">A Director hosts web services much like a Front End pool.</span></span> <span data-ttu-id="abfb3-108">Для веб-служб требуется балансировка нагрузки оборудования.</span><span class="sxs-lookup"><span data-stu-id="abfb3-108">Hardware load balancing is required for the web services.</span></span>

<span data-ttu-id="abfb3-109">В следующих разделах описаны вопросы планирования для развертывания пула с помощью аппаратной балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="abfb3-109">The following topics describe the planning considerations for deploying a Director pool using hardware load balancing.</span></span> <span data-ttu-id="abfb3-110">Если вы планируете использовать аппаратную балансировку нагрузки и балансировку нагрузки DNS для пула ресурсов, ознакомьтесь с разделом [масштабированный пул режиссеров — балансировка нагрузки DNS и балансировщик нагрузки оборудования в Lync Server 2013, в](lync-server-2013-scaled-director-pool-dns-load-balancing-and-hardware-load-balancer.md) котором описаны требования к планированию для этой топологии.</span><span class="sxs-lookup"><span data-stu-id="abfb3-110">If you intend to use hardware load balancing and DNS load balancing for the Director pool, see the topic [Scaled Director pool - DNS load balancing and hardware load balancer in Lync Server 2013](lync-server-2013-scaled-director-pool-dns-load-balancing-and-hardware-load-balancer.md) that describes the planning requirements for that topology.</span></span>

<span data-ttu-id="abfb3-111">![cfa892b9-5b24-4245-b5bd-c5da21984eeb](images/JJ205316.cfa892b9-5b24-4245-b5bd-c5da21984eeb(OCS.15).jpg "cfa892b9-5b24-4245-b5bd-c5da21984eeb")</span><span class="sxs-lookup"><span data-stu-id="abfb3-111">![cfa892b9-5b24-4245-b5bd-c5da21984eeb](images/JJ205316.cfa892b9-5b24-4245-b5bd-c5da21984eeb(OCS.15).jpg "cfa892b9-5b24-4245-b5bd-c5da21984eeb")</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="abfb3-112">Содержание</span><span class="sxs-lookup"><span data-stu-id="abfb3-112">In This Section</span></span>

  - [<span data-ttu-id="abfb3-113">Сводка по сертификатам — масштабированный пул директоров, аппаратный балансировщик нагрузки в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="abfb3-113">Certificate summary - Scaled Director pool, hardware load balancer in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-scaled-director-pool-hardware-load-balancer.md)

  - [<span data-ttu-id="abfb3-114">Сводка по портам — vасштабируемый пул директоров, аппаратный балансировщик нагрузки в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="abfb3-114">Port summary - Scaled Director pool, hardware load balancer in Lync Server 2013</span></span>](lync-server-2013-port-summary-scaled-director-pool-hardware-load-balancer.md)

  - [<span data-ttu-id="abfb3-115">Сводка по DNS — масштабируемый пул директоров, аппаратный балансировщик нагрузки в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="abfb3-115">DNS summary - Scaled Director pool, hardware load balancer in Lync Server 2013</span></span>](lync-server-2013-dns-summary-scaled-director-pool-hardware-load-balancer.md)

<span data-ttu-id="abfb3-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="abfb3-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

