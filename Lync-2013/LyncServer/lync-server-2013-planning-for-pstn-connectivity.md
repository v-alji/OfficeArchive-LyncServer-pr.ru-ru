---
title: 'Lync Server 2013: Планирование подключений PSTN'
description: 'Lync Server 2013: Планирование подключений PSTN.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for PSTN connectivity
ms:assetid: 280f684a-740a-443d-8ecf-574241382a42
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425749(v=OCS.15)
ms:contentKeyID: 48183684
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 45c0df6aa6dc9d9cc8522223056f1834849e6ddb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424438"
---
# <a name="planning-for-pstn-connectivity-in-lync-server-2013"></a><span data-ttu-id="89f28-103">Планирование подключений PSTN в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="89f28-103">Planning for PSTN connectivity in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="89f28-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="89f28-104">

<span> </span></span></span>

<span data-ttu-id="89f28-105">_**Тема последнего изменения:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="89f28-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="89f28-106">Решение VoIP корпоративного уровня должно предусматривать входящие и исходящие вызовы на телефонную сеть общего пользования (ТСОП) без какого-либо снижения качества обслуживания (QoS).</span><span class="sxs-lookup"><span data-stu-id="89f28-106">An enterprise-grade VoIP solution must provide for calls to and from the public switched telephone network (PSTN) without any decline in Quality of Service (QoS).</span></span> <span data-ttu-id="89f28-107">Пользователи, которые размещаются и принимают звонки, не должны знать о базовой технологии: с точки зрения пользователя, Звонок между корпоративной инфраструктурой голосовой связи и PSTN должен казаться просто другим телефонным звонком.</span><span class="sxs-lookup"><span data-stu-id="89f28-107">Users who place and receive calls should not be aware of the underlying technology: from the user's perspective, a call between the Enterprise Voice infrastructure and the PSTN should seem like just another phone call.</span></span>

<span data-ttu-id="89f28-108">Lync Server 2013 обеспечивает надежную и масштабируемую КОММУТИРУЕМую связь с помощью следующих параметров:</span><span class="sxs-lookup"><span data-stu-id="89f28-108">Lync Server 2013 provides reliable, scalable PSTN connectivity by using the following options:</span></span>

  - <span data-ttu-id="89f28-109">**магистрали SIP**, соединяющие с оператором телефонной связи по сети Интернет;</span><span class="sxs-lookup"><span data-stu-id="89f28-109">**SIP trunks** to an Internet telephony service provider (ITSP)</span></span>

  - <span data-ttu-id="89f28-110">**прямые подключения SIP** к шлюзу ТСОП;</span><span class="sxs-lookup"><span data-stu-id="89f28-110">**Direct SIP connections** to a PSTN gateway</span></span>

  - <span data-ttu-id="89f28-111">**прямые подключения SIP** к УАТС.</span><span class="sxs-lookup"><span data-stu-id="89f28-111">**Direct SIP connections** to a PBX</span></span>

<span data-ttu-id="89f28-112">В зависимости от размеров предприятия, охватываемой территории и существующей инфраструктуры голосовой связи можно применять один и тот же способ на всем предприятии либо два или все три способа в разных подразделениях.</span><span class="sxs-lookup"><span data-stu-id="89f28-112">Depending on its size, geographic coverage, and existing voice infrastructure, an enterprise may use one, two, or even all three of these options at various locations.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="89f28-113">Содержание</span><span class="sxs-lookup"><span data-stu-id="89f28-113">In This Section</span></span>

  - [<span data-ttu-id="89f28-114">Магистральные линии SIP в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="89f28-114">SIP trunking in Lync Server 2013</span></span>](lync-server-2013-sip-trunking.md)

  - [<span data-ttu-id="89f28-115">Прямые подключения по протоколу SIP в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="89f28-115">Direct SIP connections in Lync Server 2013</span></span>](lync-server-2013-direct-sip-connections.md)

  - [<span data-ttu-id="89f28-116">M:N магистраль в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="89f28-116">M:N trunk in Lync Server 2013</span></span>](lync-server-2013-m-n-trunk.md)

  - [<span data-ttu-id="89f28-117">Правила перевода в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="89f28-117">Translation rules in Lync Server 2013</span></span>](lync-server-2013-translation-rules.md)

  - [<span data-ttu-id="89f28-118">Планирование маршрутизации исходящей голосовой почты в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="89f28-118">Planning outbound voice routing in Lync Server 2013</span></span>](lync-server-2013-planning-outbound-voice-routing.md)

<span data-ttu-id="89f28-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="89f28-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

