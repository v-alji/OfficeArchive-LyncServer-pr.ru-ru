---
title: 'Lync Server 2013: сервер-посредник и обход сервера посредника'
description: 'Lync Server 2013: сервер обходит и исходящие мультимедиа.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Media bypass and Mediation Server
ms:assetid: 8ed35f95-05cd-4b5d-8470-442d2323df71
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398719(v=OCS.15)
ms:contentKeyID: 48184774
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ebb005d3d52fa9e5a38fdf56a65dfcbd73616d87
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425705"
---
# <a name="media-bypass-and-mediation-server-in-lync-server-2013"></a><span data-ttu-id="2dd7a-103">Сервер-посредник и обход сервера посредника в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2dd7a-103">Media bypass and Mediation Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2dd7a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2dd7a-104">

<span> </span></span></span>

<span data-ttu-id="2dd7a-105">_**Тема последнего изменения:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="2dd7a-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="2dd7a-106">Обтекание мультимедиа — это возможность Lync Server, которая позволяет администратору настроить маршрутизацию звонков прямо между конечной точкой пользователя и шлюзом коммутируемой телефонной сети (PSTN) без обхода сервера-посредника.</span><span class="sxs-lookup"><span data-stu-id="2dd7a-106">Media bypass is a Lync Server capability that enables an administrator to configure call routing to flow directly between the user endpoint and the public switched telephone network (PSTN) gateway without traversing the Mediation Server.</span></span> <span data-ttu-id="2dd7a-107">Обход мультимедиа улучшает качество связи, уменьшая задержку, ненужные переводы, вероятность потери пакетов и количество возможных точек сбоя.</span><span class="sxs-lookup"><span data-stu-id="2dd7a-107">Media bypass improves call quality by reducing latency, unnecessary translation, possibility of packet loss, and the number of potential points of failure.</span></span> <span data-ttu-id="2dd7a-108">Если удаленный сайт без сервера-посредника подключен к центральному сайту по одной или нескольким ГЛОБАЛЬным каналам связи с ограниченной пропускной способностью, пропустите требования к пропускной способности, разрешив доступ к мультимедиа с клиента на удаленном сайте для непосредственного подключения к серверу-источнику и обратно. Это сокращение в обработке мультимедиа также дополняет возможности сервера-посредника для управления несколькими шлюзами.</span><span class="sxs-lookup"><span data-stu-id="2dd7a-108">Where a remote site without a Mediation Server is connected to a central site by one or more WAN links with constrained bandwidth, media bypass lowers the bandwidth requirement by enabling media from a client at a remote site to flow directly to its local gateway without first having to flow across the WAN link to a Mediation Server at the central site and back.This reduction in media processing also complements the Mediation Server’s ability to control multiple gateways.</span></span>

<span data-ttu-id="2dd7a-p102">Обход сервера-посредника и контроль допуска звонков являются взаимоисключающими функциями. Если для вызова применяется обход сервера-посредника, то для него не применяется контроль допуска звонков. Предполагается, что нет никакой связи с ограниченной пропускной способностью сторон, участвующих в вызове.</span><span class="sxs-lookup"><span data-stu-id="2dd7a-p102">Media bypass and call admission control (CAC) are mutually exclusive. If media bypass is employed for a call, CAC is not performed for that call. The assumption is that there are no links with constrained bandwidth involved in the call.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="2dd7a-112">См. также</span><span class="sxs-lookup"><span data-stu-id="2dd7a-112">See Also</span></span>


[<span data-ttu-id="2dd7a-113">Контроль допуска звонков и сервер-посредник в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2dd7a-113">Call admission control and Mediation Server in Lync Server 2013</span></span>](lync-server-2013-call-admission-control-and-mediation-server.md)  


[<span data-ttu-id="2dd7a-114">Планирование обхода серверов-посредников в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2dd7a-114">Planning for media bypass in Lync Server 2013</span></span>](lync-server-2013-planning-for-media-bypass.md)  
  

<span data-ttu-id="2dd7a-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2dd7a-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

