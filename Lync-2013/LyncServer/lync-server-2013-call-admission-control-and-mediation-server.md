---
title: 'Lync Server 2013: контроль допуска звонков и сервер-посредник'
description: 'Lync Server 2013: управление допуском звонков и сервер исправлений.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Call admission control and Mediation Server
ms:assetid: 76faccdc-67d0-4c8b-8e47-1e23c93b02c6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398585(v=OCS.15)
ms:contentKeyID: 48184546
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 77e4b12a11f941923d50f3ffcab7a8f9b6a9edc5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435931"
---
# <a name="call-admission-control-and-mediation-server-in-lync-server-2013"></a><span data-ttu-id="f1fca-103">Контроль допуска звонков и сервер-посредник в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f1fca-103">Call admission control and Mediation Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f1fca-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f1fca-104">

<span> </span></span></span>

<span data-ttu-id="f1fca-105">_**Тема последнего изменения:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="f1fca-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="f1fca-106">Управление допуском звонков (CAC), впервые введенное в Lync Server 2010, управляет набором сеансов в реальном времени, основываясь на доступной пропускной способности, чтобы предотвратить низкое качество работы (QoE) для пользователей в перегруженных сетях.</span><span class="sxs-lookup"><span data-stu-id="f1fca-106">Call admission control (CAC), first introduced in Lync Server 2010, manages real-time session establishment, based on available bandwidth, to help prevent poor Quality of Experience (QoE) for users on congested networks.</span></span> <span data-ttu-id="f1fca-107">Для поддержки этой возможности сервер-посредник, который обеспечивает передачу сигналов и трансляцию мультимедиа между корпоративной инфраструктурой голосовой связи и провайдером по магистрали SIP, несет ответственность за управление пропускной способностью двух видов взаимодействия на стороне Lync Server и на стороне шлюза.</span><span class="sxs-lookup"><span data-stu-id="f1fca-107">To support this capability, the Mediation Server, which provides signaling and media translation between the Enterprise Voice infrastructure and a gateway or SIP trunking provider, is responsible for bandwidth management for its two interactions on the Lync Server side and on the gateway side.</span></span> <span data-ttu-id="f1fca-108">При управлении допуском звонков оконечная сущность для вызова обрабатывает резервирование пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="f1fca-108">In call admission control, the terminating entity for a call handles the bandwidth reservation.</span></span> <span data-ttu-id="f1fca-109">Узлы шлюзов (шлюз PSTN, IP-УАТС, SBC), с помощью которого сервер-посредник взаимодействует на стороне шлюза, не поддерживают управление допуском звонков в Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f1fca-109">The gateway peers (PSTN gateway, IP-PBX, SBC) that the Mediation Server interacts with on the gateway side do not support Lync Server 2013 call admission control.</span></span> <span data-ttu-id="f1fca-110">Таким образом, сервер обновлений должен обрабатывать взаимодействие с пропускной способностью от имени ее партнера.</span><span class="sxs-lookup"><span data-stu-id="f1fca-110">Thus, the Mediation Server has to handle bandwidth interactions on behalf of its gateway peer.</span></span> <span data-ttu-id="f1fca-111">По мере возможности сервер, на котором выполняется исправление, резервирует пропускную способность заранее.</span><span class="sxs-lookup"><span data-stu-id="f1fca-111">Whenever possible, the Mediation Server will reserve bandwidth in advance.</span></span> <span data-ttu-id="f1fca-112">Если это невозможно (например, если локальная конечная точка Media на стороне шлюза неизвестна для исходящего звонка на узел шлюза), при помещении звонка пропускная способность резервируется.</span><span class="sxs-lookup"><span data-stu-id="f1fca-112">If that is not possible (for example, if the locality of the ultimate media endpoint on the gateway side is unknown for an outgoing call to the gateway peer), bandwidth is reserved when the call is placed.</span></span> <span data-ttu-id="f1fca-113">Это может привести к превышению подписку на использование пропускной способности, но это единственный способ предотвратить ложный звонок.</span><span class="sxs-lookup"><span data-stu-id="f1fca-113">This behavior can result in oversubscription of bandwidth, but it is the only way to prevent false rings.</span></span>

<span data-ttu-id="f1fca-114">Обход сервера-посредника и резервирование пропускной способности являются взаимоисключающими подходами.</span><span class="sxs-lookup"><span data-stu-id="f1fca-114">Media bypass and bandwidth reservation are mutually exclusive.</span></span> <span data-ttu-id="f1fca-115">Если для вызова используются обходные номера мультимедиа, управление допуском звонков для этого звонка не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f1fca-115">If a media bypass is employed for a call, call admission control is not performed for that call.</span></span> <span data-ttu-id="f1fca-116">Предполагается, что при выполнении вызова отсутствуют каналы с ограниченной пропускной способностью.</span><span class="sxs-lookup"><span data-stu-id="f1fca-116">The assumption here is that there are no links with constrained bandwidth involved in the call.</span></span> <span data-ttu-id="f1fca-117">Если для определенного звонка, включающего сервер-посредника, используется управление допуском звонков, этот звонок не может использовать функцию обхода мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="f1fca-117">If call admission control is used for a particular call that involves the Mediation Server, that call cannot employ media bypass.</span></span>

<span data-ttu-id="f1fca-118">Дополнительные сведения об управлении мультимедийными данными и допуском звонков можно найти в разделе [Планирование обхода мультимедиа в Lync server 2013](lync-server-2013-planning-for-media-bypass.md) или [Планирование управления допуском звонков в Lync Server 2013](lync-server-2013-planning-for-call-admission-control.md) в документации по планированию.</span><span class="sxs-lookup"><span data-stu-id="f1fca-118">For details about media bypass or call admission control, see [Planning for media bypass in Lync Server 2013](lync-server-2013-planning-for-media-bypass.md) or [Planning for call admission control in Lync Server 2013](lync-server-2013-planning-for-call-admission-control.md) in the Planning documentation.</span></span>

<span data-ttu-id="f1fca-119"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f1fca-119"></div>

<span> </span>

</div>

</div>

</span></span></div>

