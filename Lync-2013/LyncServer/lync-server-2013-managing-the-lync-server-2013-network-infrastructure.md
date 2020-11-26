---
title: 'Lync Server 2013: управление инфраструктурой сети Lync Server 2013'
description: 'Lync Server 2013: управление инфраструктурой сети Lync Server 2013.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing the Lync Server 2013 network infrastructure
ms:assetid: cb13456a-8f66-4595-be21-8887f30ad4eb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182585(v=OCS.15)
ms:contentKeyID: 48185638
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ab1b5c6fe52374b012063ac26640e9bb25496ad7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425859"
---
# <a name="managing-the-lync-server-2013-network-infrastructure"></a><span data-ttu-id="64282-103">Управление инфраструктурой сети Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="64282-103">Managing the Lync Server 2013 network infrastructure</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="64282-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="64282-104">

<span> </span></span></span>

<span data-ttu-id="64282-105">_**Тема последнего изменения:** 2014-02-11_</span><span class="sxs-lookup"><span data-stu-id="64282-105">_**Topic Last Modified:** 2014-02-11_</span></span>

<span data-ttu-id="64282-106">Microsoft Lync Server 2013 включает поддержку управления допуском звонков (CAC) и обход мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="64282-106">Microsoft Lync Server 2013 includes support for call admission control (CAC) and media bypass.</span></span> <span data-ttu-id="64282-107">Для реализации этих функций необходимо настроить сеть регионов, сайтов, подсетей и т. д., благодаря которой вы сможете управлять пропускной способностью в ситуациях, когда необходимо ограничить передачу звука и видео.</span><span class="sxs-lookup"><span data-stu-id="64282-107">To implement these features you must configure a network of regions, sites, subnets, and so on that will allow you to manage bandwidth in situations where audio and video transmissions need to be restricted.</span></span> <span data-ttu-id="64282-108">Кроме того, вы можете использовать сетевую технологию качества обслуживания (QoS) для обеспечения оптимального взаимодействия с конечными пользователями для голосовой и видеосвязи.</span><span class="sxs-lookup"><span data-stu-id="64282-108">You can also use the Quality of Service (QoS) networking technology to help provide an optimal end-user experience for audio and video communications.</span></span>

<span data-ttu-id="64282-109">С помощью панели управления Lync Server вы можете настроить CAC, обход мультимедиа и качество обслуживания, а также управлять ими.</span><span class="sxs-lookup"><span data-stu-id="64282-109">You can use the Lync Server Control Panel to set up and manage CAC, media bypass, and QoS.</span></span> <span data-ttu-id="64282-110">В следующих разделах приведены инструкции по выполнению этой задачи.</span><span class="sxs-lookup"><span data-stu-id="64282-110">The following topics provide steps for how to do this.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="64282-111">Содержание</span><span class="sxs-lookup"><span data-stu-id="64282-111">In This Section</span></span>

  - [<span data-ttu-id="64282-112">Управление качеством обслуживания (QoS) в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="64282-112">Managing Quality of Service (QoS) in Lync Server 2013</span></span>](lync-server-2013-managing-quality-of-service-qos.md)

  - [<span data-ttu-id="64282-113">Управление допуском звонков в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="64282-113">Managing call admission control in Lync Server 2013</span></span>](lync-server-2013-managing-call-admission-control.md)

  - [<span data-ttu-id="64282-114">Сетевые интерфейсы Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="64282-114">Lync Server 2013 network interfaces</span></span>](lync-server-2013-lync-server-network-interfaces.md)

  - [<span data-ttu-id="64282-115">Запрещение новых подключений к Lync Server 2013 для обслуживания сервера</span><span class="sxs-lookup"><span data-stu-id="64282-115">Prevent new connections to Lync Server 2013 for server maintenance</span></span>](lync-server-2013-prevent-new-connections-to-lync-server-for-server-maintenance.md)

  - [<span data-ttu-id="64282-116">Методология качества звонков Lync в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="64282-116">Lync Call Quality Methodology in Lync Server 2013</span></span>](lync-server-2013-poster-lync-call-quality-methodology.md)

  - [<span data-ttu-id="64282-117">Индикаторы работоспособности ключа в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="64282-117">Key Health Indicators in Lync Server 2013</span></span>](lync-server-2013-poster-key-health-indicators.md)

<span data-ttu-id="64282-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="64282-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

