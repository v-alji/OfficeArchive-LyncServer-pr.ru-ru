---
title: 'Lync Server 2013: технические рекомендации для маршрутизации на основе расположения'
description: 'Lync Server 2013: технические рекомендации для маршрутизации Location-Based.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Technical considerations for Location-Based Routing
ms:assetid: 2e2a9199-7c6f-48d3-9adb-3873fc4f8c4e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994027(v=OCS.15)
ms:contentKeyID: 51803936
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 54a025af81ab148ad41f95d0a8cf4f900beb7e00
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423430"
---
# <a name="technical-considerations-for-location-based-routing-in-lync-server-2013"></a><span data-ttu-id="1aa92-103">Технические рекомендации для маршрутизации на основе расположения в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1aa92-103">Technical considerations for Location-Based Routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1aa92-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1aa92-104">

<span> </span></span></span>

<span data-ttu-id="1aa92-105">_**Тема последнего изменения:** 2013-03-09_</span><span class="sxs-lookup"><span data-stu-id="1aa92-105">_**Topic Last Modified:** 2013-03-09_</span></span>

<span data-ttu-id="1aa92-106">При планировании Location-Based маршрутизации следует принять во тронутые ниже ситуации.</span><span class="sxs-lookup"><span data-stu-id="1aa92-106">When planning Location-Based Routing, you should consider the impact to the following scenarios.</span></span>

<div>

## <a name="disaster-recovery"></a><span data-ttu-id="1aa92-107">Аварийное восстановление</span><span class="sxs-lookup"><span data-stu-id="1aa92-107">Disaster Recovery</span></span>

<span data-ttu-id="1aa92-108">При отработке отказа из основного пула в пул резервного копирования, а также при восстановлении обычных операций для основного пула, Location-Based маршрутизация всегда будет принудительно применена во время аварийной ситуации и процедуры восстановления.</span><span class="sxs-lookup"><span data-stu-id="1aa92-108">During a failover from the primary pool to a backup pool as well as when restoring normal operations to the primary pool, Location-Based Routing remains enforced at all times during a disaster and recovery procedure.</span></span>

</div>

<div>

## <a name="survivable-branch-appliance"></a><span data-ttu-id="1aa92-109">для обеспечения связи в филиалах</span><span class="sxs-lookup"><span data-stu-id="1aa92-109">Survivable Branch Appliance</span></span>

<span data-ttu-id="1aa92-110">Настройка маршрутизации Location-Based влияет на планирование развертывания шлюзов, связанных с работающими устройствами филиалов.</span><span class="sxs-lookup"><span data-stu-id="1aa92-110">Configuring Location-Based Routing impacts the planning of where you deploy the gateways associated to your Survivable Branch Appliances.</span></span> <span data-ttu-id="1aa92-111">Шлюз, связанный с вашим SBA, должен находиться на том же сетевом сайте, что и работающее устройство филиала. в противном случае пользователи, работающие на устройстве с бесперебойной подразделением, не смогут выполнять исходящие вызовы, если настроена Location-Based маршрутизация.</span><span class="sxs-lookup"><span data-stu-id="1aa92-111">The gateway associated to your SBA must be located in the same network site as your Survivable Branch Appliance; otherwise, users homed on your Survivable Branch Appliance will not be permitted to place outbound calls if Location-Based Routing is configured.</span></span> <span data-ttu-id="1aa92-112">Если подключение к глобальной сети между бесперебойно используемым устройством филиала и центральным сайтом не работает, Location-Based ограничения маршрутизации будут действовать принудительно.</span><span class="sxs-lookup"><span data-stu-id="1aa92-112">When the WAN connection between your Survivable Branch Appliance and the central site is down, Location-Based Routing restrictions remains enforced.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="1aa92-113">См. также</span><span class="sxs-lookup"><span data-stu-id="1aa92-113">See Also</span></span>


[<span data-ttu-id="1aa92-114">Планирование маршрутизации на основе местоположения в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1aa92-114">Planning for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-planning-for-location-based-routing.md)  
  

<span data-ttu-id="1aa92-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1aa92-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

