---
title: 'Lync Server 2013: функции, не поддерживаемые маршрутизацией на основе расположения'
description: 'Lync Server 2013: возможности, не поддерживаемые службой маршрутизации Location-Based.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Capabilities not supported by Location-Based Routing
ms:assetid: c3d54953-a7d6-4465-a6c3-ae411b2d8ea9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994071(v=OCS.15)
ms:contentKeyID: 51803982
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bf9cd03a8cbdd50e136605c4f172598b2ad3f523
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435609"
---
# <a name="capabilities-not-supported-by-location-based-routing-in-lync-server-2013"></a><span data-ttu-id="83d52-103">Функции, не поддерживаемые маршрутизацией на основе расположения в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="83d52-103">Capabilities not supported by Location-Based Routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="83d52-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="83d52-104">

<span> </span></span></span>

<span data-ttu-id="83d52-105">_**Тема последнего изменения:** 2014-03-12_</span><span class="sxs-lookup"><span data-stu-id="83d52-105">_**Topic Last Modified:** 2014-03-12_</span></span>

<span data-ttu-id="83d52-106">Location-Based маршрутизация не применяется к следующим типам взаимодействий.</span><span class="sxs-lookup"><span data-stu-id="83d52-106">Location-Based Routing does not apply to the following types of interactions.</span></span> <span data-ttu-id="83d52-107">Если конечные точки Lync взаимодействуют с конечными точками PSTN с помощью этих возможностей, маршрутизация Location-Based не выполняется принудительно.</span><span class="sxs-lookup"><span data-stu-id="83d52-107">Location-Based Routing is not enforced when Lync endpoints interact with PSTN endpoints using these capabilities.</span></span>

  - <span data-ttu-id="83d52-108">Конференции с телефонным подключением</span><span class="sxs-lookup"><span data-stu-id="83d52-108">PSTN dial-in to conferences</span></span>

  - <span data-ttu-id="83d52-109">Входящие и исходящие вызовы ТСОП через группу ответов</span><span class="sxs-lookup"><span data-stu-id="83d52-109">Incoming and outgoing PSTN calls through Response Group</span></span>

  - <span data-ttu-id="83d52-110">Парковка вызовов или преобразование вызовов ТСОП с помощью функции парковки вызовов</span><span class="sxs-lookup"><span data-stu-id="83d52-110">Call park or retrieval of PSTN calls through Call Park</span></span>

  - <span data-ttu-id="83d52-111">Входящие вызовы ТСОП в службу оповещений</span><span class="sxs-lookup"><span data-stu-id="83d52-111">Incoming PSTN calls to Announcement Service</span></span>

  - <span data-ttu-id="83d52-112">Входящие вызовы ТСОП, преобразованные через групповой ответ на вызовы</span><span class="sxs-lookup"><span data-stu-id="83d52-112">Incoming PSTN calls retrieved via Group Call Pickup</span></span>

<span data-ttu-id="83d52-113">Чтобы применить правила маршрутизации Location-Based к типам взаимодействия в следующем списке, необходимо включить Location-Based маршрутизацию для конференц-связи.</span><span class="sxs-lookup"><span data-stu-id="83d52-113">To enforce Location-Based Routing rules to the types of interactions in the following list, you must enable Location-Based Routing for Conferencing:</span></span>

  - <span data-ttu-id="83d52-114">Исходящие вызовы по ТСОП из конференций</span><span class="sxs-lookup"><span data-stu-id="83d52-114">PSTN dial-out from conferences</span></span>

  - <span data-ttu-id="83d52-115">Эскалации из сеансов одноранговой голосовой связи к сеансам конференций с привлечением конечных точек ТСОП</span><span class="sxs-lookup"><span data-stu-id="83d52-115">Escalations from peer-to-peer audio conversations to conferencing involving PSTN endpoints</span></span>

  - <span data-ttu-id="83d52-116">Передачи после консультации с привлечением конечных точек ТСОП</span><span class="sxs-lookup"><span data-stu-id="83d52-116">Consultative transfers involving PSTN endpoints</span></span>

<span data-ttu-id="83d52-117">Чтобы включить Location-Basedную маршрутизацию для конференц-связи, ознакомьтесь со сведениями [о маршрутизации на основе местоположения для конференций в Lync Server 2013](lync-server-2013-location-based-routing-for-conferencing.md).</span><span class="sxs-lookup"><span data-stu-id="83d52-117">To enable Location-Based Routing for Conferencing, see [Location-Based Routing for conferencing in Lync Server 2013](lync-server-2013-location-based-routing-for-conferencing.md).</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="83d52-118">См. также</span><span class="sxs-lookup"><span data-stu-id="83d52-118">See Also</span></span>


[<span data-ttu-id="83d52-119">Планирование маршрутизации на основе местоположения в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="83d52-119">Planning for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-planning-for-location-based-routing.md)  
  

<span data-ttu-id="83d52-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="83d52-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

