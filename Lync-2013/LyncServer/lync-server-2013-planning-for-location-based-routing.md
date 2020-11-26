---
title: 'Lync Server 2013: планирование маршрутизации на основе местоположения'
description: 'Lync Server 2013: планирование Location-Based маршрутизации.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for Location-Based Routing
ms:assetid: bb035924-6b52-4f0f-8e05-b76864fb9ef3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994068(v=OCS.15)
ms:contentKeyID: 51803979
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 894a596e998fe07b97ad7911441eced670ba85b2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442952"
---
# <a name="planning-for-location-based-routing-in-lync-server-2013"></a><span data-ttu-id="93e6c-103">Планирование маршрутизации на основе местоположения в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="93e6c-103">Planning for Location-Based Routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="93e6c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="93e6c-104">

<span> </span></span></span>

<span data-ttu-id="93e6c-105">_**Тема последнего изменения:** 2013-07-31_</span><span class="sxs-lookup"><span data-stu-id="93e6c-105">_**Topic Last Modified:** 2013-07-31_</span></span>

<span data-ttu-id="93e6c-106">Сведения, представленные в данной теме, относятся к накопительным обновлениям для Lync Server 2013: февраль 2013 г.</span><span class="sxs-lookup"><span data-stu-id="93e6c-106">The information in this topic pertains to Cumulative Updates for Lync Server 2013: February 2013.</span></span>

<span data-ttu-id="93e6c-107">Маршрутизация Location-Based позволяет ограничить маршрутизацию звонков между конечными точками VoIP и КОММУТИРУЕМыми конечными точками, основываясь на местоположении сторон в звонке.</span><span class="sxs-lookup"><span data-stu-id="93e6c-107">Location-Based Routing makes it possible to restrict the routing of calls between VoIP endpoints and PSTN endpoints based on the location of the parties in the call.</span></span> <span data-ttu-id="93e6c-108">Location-Based маршрутизация входит в корпоративную инфраструктуру голосовой связи Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="93e6c-108">Location-Based Routing is part of the Lync Server 2013 Enterprise Voice infrastructure.</span></span> <span data-ttu-id="93e6c-109">Location-Based маршрутизация — это функция управления звонками, определяющая способ маршрутизации звонков Lync Server 2013 CU1.</span><span class="sxs-lookup"><span data-stu-id="93e6c-109">Location-Based Routing is a call management feature that controls how calls are routed by Lync Server 2013 CU1.</span></span> <span data-ttu-id="93e6c-110">Он принудительно устанавливает правила авторизации вызовов для направления звонков в конечные точки УАТС или PSTN, основываясь на географическом расположении вызывающего абонента Lync.</span><span class="sxs-lookup"><span data-stu-id="93e6c-110">It enforces call authorization rules on whether calls can be routed to PBX or PSTN endpoints based on the Lync caller’s geographic location.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="93e6c-111">Содержание</span><span class="sxs-lookup"><span data-stu-id="93e6c-111">In This Section</span></span>

  - [<span data-ttu-id="93e6c-112">Общие сведения о маршрутизации Location-Based в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="93e6c-112">Overview of Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-overview-of-location-based-routing.md)

  - [<span data-ttu-id="93e6c-113">Инструкции по маршрутизации на основе местоположения в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="93e6c-113">Guidance for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-guidance-for-location-based-routing.md)

  - [<span data-ttu-id="93e6c-114">Сценарии маршрутизации на основе местоположения в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="93e6c-114">Scenarios for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-scenarios-for-location-based-routing.md)

  - [<span data-ttu-id="93e6c-115">Технические рекомендации для маршрутизации на основе расположения в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="93e6c-115">Technical considerations for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-technical-considerations-for-location-based-routing.md)

  - [<span data-ttu-id="93e6c-116">Поддержка маршрутизации на основе расположения клиентами и серверами в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="93e6c-116">Client and server support for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-client-and-server-support-for-location-based-routing.md)

  - [<span data-ttu-id="93e6c-117">Функции, не поддерживаемые маршрутизацией на основе расположения в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="93e6c-117">Capabilities not supported by Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-capabilities-not-supported-by-location-based-routing.md)

  - [<span data-ttu-id="93e6c-118">Процесс развертывания функции маршрутизации на основе местоположения в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="93e6c-118">Deployment process for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-deployment-process-for-location-based-routing.md)

  - [<span data-ttu-id="93e6c-119">Маршрутизация на основе местоположения для конференц-связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="93e6c-119">Location-Based Routing for conferencing in Lync Server 2013</span></span>](lync-server-2013-location-based-routing-for-conferencing.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="93e6c-120">См. также</span><span class="sxs-lookup"><span data-stu-id="93e6c-120">See Also</span></span>


[<span data-ttu-id="93e6c-121">Планирование для корпоративного голосовой связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="93e6c-121">Planning for Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-planning-for-enterprise-voice.md)  
  

<span data-ttu-id="93e6c-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="93e6c-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

