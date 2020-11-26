---
title: 'Lync Server 2013: делегирование'
description: 'Lync Server 2013: делегирование.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delegation
ms:assetid: 89e76e5c-3cfb-4504-8d0d-7509c8ba9815
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994045(v=OCS.15)
ms:contentKeyID: 51803956
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6dc25d0ea3dfd64ee1b71677e6bac55c1cb1ca32
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430744"
---
# <a name="delegation-in-lync-server-2013"></a><span data-ttu-id="e4f6b-103">Делегирование в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e4f6b-103">Delegation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e4f6b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e4f6b-104">

<span> </span></span></span>

<span data-ttu-id="e4f6b-105">_**Тема последнего изменения:** 2013-03-09_</span><span class="sxs-lookup"><span data-stu-id="e4f6b-105">_**Topic Last Modified:** 2013-03-09_</span></span>

<span data-ttu-id="e4f6b-106">Возможности делегирования в Lync влияют на Location-Based маршрутизации следующим образом:</span><span class="sxs-lookup"><span data-stu-id="e4f6b-106">The delegation capabilities in Lync are affected by Location-Based Routing in the following manner:</span></span>

  - <span data-ttu-id="e4f6b-107">Если представитель, включенный для Location-Based маршрутизации, помещает звонок от имени руководителя, для авторизации звонка используется политика голосовой связи представителя, а для направления звонка используется политика маршрутизации голосовой связи на сайте.</span><span class="sxs-lookup"><span data-stu-id="e4f6b-107">When a delegate enabled for Location-Based Routing places a call on behalf of a manager, the delegate’s voice policy is used to authorize the call and the delegate’s site voice routing policy will be used to route the call</span></span>

  - <span data-ttu-id="e4f6b-108">Что касается исходящих звонков ТСОП диспетчеру, действуют те же правила, регламентирующие переадресацию звонков и порядок обработки одновременных звонков, что и в соответствующих разделах.</span><span class="sxs-lookup"><span data-stu-id="e4f6b-108">For incoming PSTN calls to a manager, the same rules applicable for call forwarding or simultaneously ringing will apply as described in the Call transfers and forwarding and Simultaneous ringing topics.</span></span>

  - <span data-ttu-id="e4f6b-109">Когда делегат устанавливает конечную точку ТСОП в качестве точки назначения одновременных звонков для входящих звонков в адрес диспетчера, для маршрутизации звонка на конечную точку ТСОП делегата используется политика маршрутизации голосовых звонков сетевого сайта, связанного с входящей магистралью.</span><span class="sxs-lookup"><span data-stu-id="e4f6b-109">When a delegate sets a PSTN endpoint as a simultaneous ring target, for an incoming call to the manager, the voice routing policy of the site that is associated to the incoming trunk will be used to route the call to the delegate’s PSTN endpoint.</span></span>

  - <span data-ttu-id="e4f6b-110">Для целей делегирования, как правило, рекомендуется, чтобы диспетчер и связанные с ним делегаты находились на одном сетевом сайте.</span><span class="sxs-lookup"><span data-stu-id="e4f6b-110">For delegation, it’s recommended that the manager and his associated delegates to be usually located in the same network site.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="e4f6b-111">См. также</span><span class="sxs-lookup"><span data-stu-id="e4f6b-111">See Also</span></span>


[<span data-ttu-id="e4f6b-112">Сценарии маршрутизации на основе местоположения в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e4f6b-112">Scenarios for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-scenarios-for-location-based-routing.md)  
  

<span data-ttu-id="e4f6b-113"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e4f6b-113"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

