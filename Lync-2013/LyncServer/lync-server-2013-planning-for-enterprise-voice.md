---
title: 'Lync Server 2013: планирование для корпоративного голосовой связи'
description: 'Lync Server 2013: планирование для корпоративного голосовой связи.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for Enterprise Voice
ms:assetid: fd8d5867-0ac9-47f8-94f0-1c3ee5e25575
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413081(v=OCS.15)
ms:contentKeyID: 48185959
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4dfa0d91fe8270e49524d648ef403cd69ede2407
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424585"
---
# <a name="planning-for-enterprise-voice-in-lync-server-2013"></a><span data-ttu-id="9a339-103">Планирование для корпоративного голосовой связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9a339-103">Planning for Enterprise Voice in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9a339-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9a339-104">

<span> </span></span></span>

<span data-ttu-id="9a339-105">_**Тема последнего изменения:** 2013-11-01_</span><span class="sxs-lookup"><span data-stu-id="9a339-105">_**Topic Last Modified:** 2013-11-01_</span></span>

<span data-ttu-id="9a339-106">Процесс развертывания для корпоративной голосовой связи зависит от существующей топологии, инфраструктуры и функций корпоративной голосовой связи, которые требуется поддерживать.</span><span class="sxs-lookup"><span data-stu-id="9a339-106">The deployment process for Enterprise Voice depends on your existing topology, infrastructure, and the Enterprise Voice functionality that you want to support.</span></span> <span data-ttu-id="9a339-107">Необходимые процедуры будут зависеть от выбранных функций, но есть и другие вопросы планирования, которые необходимо выполнить на высоком уровне.</span><span class="sxs-lookup"><span data-stu-id="9a339-107">The required procedures will depend on what features you choose, but there are other planning considerations that you must make at a high level.</span></span>

<span data-ttu-id="9a339-108">Общие рекомендации состоят в том, чтобы учесть тип и количество развертываемых сайтов и их географическое положение, интенсивность вызовов на каждом сайте, типы сетевых каналов связи между сайтами, необходимость в избыточности и отработке отказов для функций голосовой связи на каждом сайте, а также потребность в использовании существующего оборудования УАТС.</span><span class="sxs-lookup"><span data-stu-id="9a339-108">In general, consider the type and number of sites that you want to deploy and their geographical locations, the call volume at each site, the types of network links that connect sites, whether you want to provide redundancy and failover for voice functionality for each site, and whether you want to use existing PBX equipment.</span></span> <span data-ttu-id="9a339-109">Существуют некоторые особенности, например высокая доступность, которые следует учитывать при планировании общего программного обеспечения для связи Lync Server.</span><span class="sxs-lookup"><span data-stu-id="9a339-109">There are certain considerations, such as high availability, that you should consider when you plan for Lync Server  communications software as a whole.</span></span> <span data-ttu-id="9a339-110">Эти аспекты рассматриваются в данном разделе по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="9a339-110">These considerations are discussed in topics throughout this section, as needed.</span></span>

<div>

## <a name="planning-considerations"></a><span data-ttu-id="9a339-111">Вопросы планирования</span><span class="sxs-lookup"><span data-stu-id="9a339-111">Planning Considerations</span></span>

<span data-ttu-id="9a339-112">Сведения о планировании решений, относящихся к развертыванию определенной возможности голосовой связи или сценарии развертывания или компоненту, можно найти в темах этого раздела.</span><span class="sxs-lookup"><span data-stu-id="9a339-112">For planning decisions that pertain to the deployment of a particular Enterprise Voice capability or deployment scenario or component, consult the topics in this section.</span></span>

  - [<span data-ttu-id="9a339-113">Определение своих требований к корпоративной голосовой связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9a339-113">Defining your requirements for Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-defining-your-requirements-for-enterprise-voice.md)

  - [<span data-ttu-id="9a339-114">Оценка объема использования и трафика голосовой связи для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9a339-114">Estimating voice usage and traffic for Lync Server 2013</span></span>](lync-server-2013-estimating-voice-usage-and-traffic.md)

  - [<span data-ttu-id="9a339-115">Network settings for the advanced Enterprise Voice features in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9a339-115">Network settings for the advanced Enterprise Voice features in Lync Server 2013</span></span>](lync-server-2013-network-settings-for-the-advanced-enterprise-voice-features.md)

  - [<span data-ttu-id="9a339-116">Components required for Enterprise Voice in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9a339-116">Components required for Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-components-required-for-enterprise-voice.md)

  - [<span data-ttu-id="9a339-117">Планирование устойчивости корпоративной голосовой связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9a339-117">Planning for Enterprise Voice resiliency in Lync Server 2013</span></span>](lync-server-2013-planning-for-enterprise-voice-resiliency.md)

  - [<span data-ttu-id="9a339-118">Планирование интеграции единой системы обмена сообщениями Exchange в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9a339-118">Planning for Exchange Unified Messaging integration in Lync Server 2013</span></span>](lync-server-2013-planning-for-exchange-unified-messaging-integration.md)

  - [<span data-ttu-id="9a339-119">Планирование контроля допуска звонков в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9a339-119">Planning for call admission control in Lync Server 2013</span></span>](lync-server-2013-planning-for-call-admission-control.md)

  - [<span data-ttu-id="9a339-120">Планирование чрезвычайных служб (E9-1-1) в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9a339-120">Planning for emergency services (E9-1-1) in Lync Server 2013</span></span>](lync-server-2013-planning-for-emergency-services-e9-1-1.md)

  - [<span data-ttu-id="9a339-121">Планирование обхода серверов-посредников в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9a339-121">Planning for media bypass in Lync Server 2013</span></span>](lync-server-2013-planning-for-media-bypass.md)

  - [<span data-ttu-id="9a339-122">Планирование частных телефонных линий с помощью Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9a339-122">Planning for private telephone lines with Lync Server 2013</span></span>](lync-server-2013-planning-for-private-telephone-lines.md)

  - [<span data-ttu-id="9a339-123">Планирование маршрутизации на основе местоположения в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9a339-123">Planning for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-planning-for-location-based-routing.md)

  - [<span data-ttu-id="9a339-124">Планирование устойчивости корпоративной голосовой связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9a339-124">Planning for Enterprise Voice resiliency in Lync Server 2013</span></span>](lync-server-2013-planning-for-enterprise-voice-resiliency.md)

  - [<span data-ttu-id="9a339-125">Рекомендации по развертыванию для корпоративной голосовой связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9a339-125">Deployment guidelines for Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-deployment-guidelines-for-enterprise-voice.md)

  - [<span data-ttu-id="9a339-126">Обзор процесса развертывания для корпоративной голосовой связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9a339-126">Deployment process overview for Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-deployment-process-overview-for-enterprise-voice.md)

  - [<span data-ttu-id="9a339-127">Перемещение пользователей на корпоративную голосовую связь в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9a339-127">Moving users to Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-moving-users-to-enterprise-voice.md)

  - [<span data-ttu-id="9a339-128">Средство диагностики предзвонков для Lync в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9a339-128">Lync PreCall Diagnostics Tool in Lync Server 2013</span></span>](lync-server-2013-lync-precall-diagnostics-tool.md)

<span data-ttu-id="9a339-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9a339-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

