---
title: 'Lync Server 2013: расположение шлюза ТСОП'
description: 'Lync Server 2013: расположение шлюза PSTN.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: PSTN gateway's location
ms:assetid: 49693a35-fad3-49ee-a71e-c7e4537b79aa
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994031(v=OCS.15)
ms:contentKeyID: 51803940
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4f793249908bd1f064f9038ddd90c7f5b01a61d5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399094"
---
# <a name="pstn-gateways-location-in-lync-server-2013"></a><span data-ttu-id="c6ea0-103">Расположение шлюза ТСОП в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c6ea0-103">PSTN gateway's location in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c6ea0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c6ea0-104">

<span> </span></span></span>

<span data-ttu-id="c6ea0-105">_**Тема последнего изменения:** 2013-03-09_</span><span class="sxs-lookup"><span data-stu-id="c6ea0-105">_**Topic Last Modified:** 2013-03-09_</span></span>

<span data-ttu-id="c6ea0-106">Для звонков по маршрутам через шлюзы PSTN и АТС может потребоваться Location-Based ограничения маршрутизации в зависимости от расположения таких систем.</span><span class="sxs-lookup"><span data-stu-id="c6ea0-106">Calls routed via PSTN gateways and PBXs might require Location-Based Routing restrictions depending on the location of such systems.</span></span> <span data-ttu-id="c6ea0-107">Маршрутизация Location-Based может быть включена на уровне детализации для каждой магистрали.</span><span class="sxs-lookup"><span data-stu-id="c6ea0-107">Location-Based Routing can be enabled at the granularity on a per trunk basis.</span></span>

<span data-ttu-id="c6ea0-108">При включении для магистрали Location-Based маршрутизация вводит следующий набор правил:</span><span class="sxs-lookup"><span data-stu-id="c6ea0-108">Location-Based Routing introduces the following set of rules when enabled on a trunk:</span></span>

  - <span data-ttu-id="c6ea0-109">Если для каждой магистрали включена Location-Based маршрутизация, правила, определенные на этой магистральной магистрали, будут применяться только к вызовам, направляемым через эту магистральную линию.</span><span class="sxs-lookup"><span data-stu-id="c6ea0-109">When Location-Based Routing is enabled on a per trunk basis, the rules define on that trunk will be applied only to calls routed through that trunk.</span></span>

  - <span data-ttu-id="c6ea0-110">Чтобы не допустить беспроводного тарифа на звонки с сетевого сайта, на котором размещается сетевой сайт, на котором расположен шлюз PSTN, Location-Based маршрутизация вводит связь сетевого сайта с заданной магистральной связью.</span><span class="sxs-lookup"><span data-stu-id="c6ea0-110">To prevent PSTN tolls bypass where calls originate from a network site different that the network site where the PSTN gateway is located, Location-Based Routing introduces the association of a network site to a given trunk.</span></span> <span data-ttu-id="c6ea0-111">Таким образом, определяется сетевой сайт, который позволяет осуществлять маршрутизацию звонков на данную магистраль.</span><span class="sxs-lookup"><span data-stu-id="c6ea0-111">This defines the network site that allows calls to be routed to a given trunk.</span></span>

<span data-ttu-id="c6ea0-112">Для маршрутизации Location-Based можно включить магистраль двумя способами:</span><span class="sxs-lookup"><span data-stu-id="c6ea0-112">Trunks can be enabled for Location-Based Routing in two ways:</span></span>

  - <span data-ttu-id="c6ea0-p103">Магистраль определяется для шлюза ТСОП, который переадресовывает звонки на номер ТСОП. Входящие звонки, перенаправленные на магистраль данного типа, будут перенаправлены только на конечные точки, расположенные на том же сайте сети, что и эта магистраль.</span><span class="sxs-lookup"><span data-stu-id="c6ea0-p103">The trunk is defined for a PSTN gateway that egresses calls to the PSTN. Incoming calls routed by a trunk of this type will be routed only to endpoints located within the same network site as the trunk.</span></span>

  - <span data-ttu-id="c6ea0-115">Магистраль определен для однорангового сервера-посредника, не исходящих вызовы для пользователей PSTN и Services со старыми телефонами в статических расположениях (например, телефоны УАТС).</span><span class="sxs-lookup"><span data-stu-id="c6ea0-115">The trunk is defined for a Mediation Server peer that doesn’t egress calls to the PSTN and services users with legacy phones in a static locations (i.e. PBX phones).</span></span> <span data-ttu-id="c6ea0-116">При данной конкретной конфигурации все входящие звонки, перенаправленные на магистраль данного типа, будут считаться исходящими из того же сетевого сайта, что и эта магистраль.</span><span class="sxs-lookup"><span data-stu-id="c6ea0-116">For this particular configuration, all incoming calls routed by a trunk of this type will be considered to be originating from the same network site as the trunk.</span></span> <span data-ttu-id="c6ea0-117">Звонки от пользователей УАТС будут иметь тот же Location-Based принудительная маршрутизация, как и пользователи Lync, которые находятся на том же сайте сети, что и магистраль.</span><span class="sxs-lookup"><span data-stu-id="c6ea0-117">Calls from PBX users will have the same Location-Based Routing enforcement as Lync users who are located in the same network site as the trunk.</span></span> <span data-ttu-id="c6ea0-118">Если две системы УАТС, расположенные на разных сетевых сайтах, подключены к серверу Lync Server, Location-Based маршрутизация разрешит маршрутизацию из одной конечной точки УАТС на другую конечную точку УАТС на другом сайте сети.</span><span class="sxs-lookup"><span data-stu-id="c6ea0-118">If two PBX systems located in separate network sites are connected through Lync Server, Location-Based Routing will allow routing from one PBX endpoint in one network site to another PBX endpoint in the other network site.</span></span> <span data-ttu-id="c6ea0-119">Этот сценарий не будет заблокирован Location-Basedной маршрутизацией.</span><span class="sxs-lookup"><span data-stu-id="c6ea0-119">This scenario will not be blocked by Location-Based Routing.</span></span> <span data-ttu-id="c6ea0-120">В дополнение к этому сценарию и тому же, как пользователь Lync в той же папке, конечные точки, связанные с одноранговым узлом сервера-посредником с помощью этой конфигурации, смогут совершать и принимать звонки и от другого однорангового сервера-посредника, не направлять звонки в КТСОП (например, конечную точку, подключенную к другой УАТС) независимо от сетевого сайта, с которым связан</span><span class="sxs-lookup"><span data-stu-id="c6ea0-120">In addition to this scenario and in a similar way as a Lync user in the same location, endpoints connected to a Mediation Server peer with this configuration will be able to make or receive calls to and from other Mediation Server peer that do not route calls to the PSTN (i.e. an endpoint connected to a different PBX) regardless of the network site to which the Mediation Server peer is associated.</span></span> <span data-ttu-id="c6ea0-121">Все входящие звонки, исходящие звонки, передачи звонков и переадресации звонков с конечными точками PSTN будут подвергаться маршрутизации на основе местоположения, чтобы использовать только шлюзы PSTN, определенные как локальные для такого сервера.</span><span class="sxs-lookup"><span data-stu-id="c6ea0-121">All inbound calls, outbound calls, call transfers and call forwards involving PSTN endpoints will be subject to Location Based Routing to use only PSTN gateways that are defined as local to such Mediation Server peer.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="c6ea0-122">См. также</span><span class="sxs-lookup"><span data-stu-id="c6ea0-122">See Also</span></span>


[<span data-ttu-id="c6ea0-123">Инструкции по маршрутизации на основе местоположения в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c6ea0-123">Guidance for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-guidance-for-location-based-routing.md)  
  

<span data-ttu-id="c6ea0-124"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c6ea0-124"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

