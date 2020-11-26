---
title: Этапы миграции
description: Этапы миграции.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migration phases
ms:assetid: cb7747ba-b872-42ca-ab41-76e3c4e77d06
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205336(v=OCS.15)
ms:contentKeyID: 48185642
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 72ef47cb9b6c9eba75c395eb9bd94c887ca5a433
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443337"
---
# <a name="migration-phases"></a><span data-ttu-id="9d6bf-103">Этапы миграции</span><span class="sxs-lookup"><span data-stu-id="9d6bf-103">Migration phases</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9d6bf-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9d6bf-104">

<span> </span></span></span>

<span data-ttu-id="9d6bf-105">_**Тема последнего изменения:** 2012-09-17_</span><span class="sxs-lookup"><span data-stu-id="9d6bf-105">_**Topic Last Modified:** 2012-09-17_</span></span>

<span data-ttu-id="9d6bf-106">В Lync Server 2013 вы определяете сайты в сети, которые содержат компоненты Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="9d6bf-106">In Lync Server 2013, you define sites on your network that contain Lync Server 2013 components.</span></span> <span data-ttu-id="9d6bf-107">Сайт — это набор компьютеров, которые надежно соединены в высокоскоростной сети с небольшой задержкой, например в локальной сети или в двух сетях, Соединенных высокоскоростной оптоволоконной одноранговой сетью.</span><span class="sxs-lookup"><span data-stu-id="9d6bf-107">A site is a set of computers that are well-connected by a high-speed, low-latency network, such as a single local area network (LAN) or two networks connected by a high-speed fiber optic network.</span></span>

<span data-ttu-id="9d6bf-108">*Пул переднего плана* — это набор серверных интерфейсов, которые настроены одинаково и работают вместе для предоставления служб для общей группы пользователей.</span><span class="sxs-lookup"><span data-stu-id="9d6bf-108">A *Front End pool* is a set of Front End Servers that are configured identically and work together to provide services for a common group of users.</span></span> <span data-ttu-id="9d6bf-109">Пул обеспечивает возможности масштабирования и отработки отказа для пользователей.</span><span class="sxs-lookup"><span data-stu-id="9d6bf-109">A pool provides scalability and failover capability to your users.</span></span> <span data-ttu-id="9d6bf-110">Каждый сервер в пуле должен выполнять одну и ту же роль (или роли).</span><span class="sxs-lookup"><span data-stu-id="9d6bf-110">Each server in a pool must run an identical server role or roles.</span></span> <span data-ttu-id="9d6bf-111">Сервер Standard Edition, разработанный для малых организаций, также определяет пул и выполняется на одном сервере.</span><span class="sxs-lookup"><span data-stu-id="9d6bf-111">A Standard Edition server, designed for small organizations, also defines a pool and runs on a single server.</span></span> <span data-ttu-id="9d6bf-112">Это позволяет использовать функциональность Lync Server 2013 для меньшей стоимости, но не предоставляет полноценное решение для высокой доступности.</span><span class="sxs-lookup"><span data-stu-id="9d6bf-112">This enables you to have Lync Server 2013 functionality for a lesser cost, but does not provide a true high-availability solution.</span></span>

<span data-ttu-id="9d6bf-113">Следующие этапы описывают процесс миграции пула с Lync Server 2010 на Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="9d6bf-113">The following phases describe the process of a pool migration from Lync Server 2010 to Lync Server 2013.</span></span> <span data-ttu-id="9d6bf-114">Для нескольких сайтов с несколькими пулами каждый из них должен следовать этому поэтапному подходу.</span><span class="sxs-lookup"><span data-stu-id="9d6bf-114">For multiple sites containing multiple pools, each individual pool should follow this phased approach.</span></span>

1.  [<span data-ttu-id="9d6bf-115">Этап 1: планирование перехода с Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="9d6bf-115">Phase 1: Plan your migration from Lync Server 2010</span></span>](phase-1-plan-your-migration-from-lync-server-2010.md)

2.  [<span data-ttu-id="9d6bf-116">Этап 2: подготовка к миграции</span><span class="sxs-lookup"><span data-stu-id="9d6bf-116">Phase 2: Prepare for migration</span></span>](phase-2-prepare-for-migration.md)

3.  [<span data-ttu-id="9d6bf-117">Этап 3: развертывание пула Lync Server 2013 Pilot</span><span class="sxs-lookup"><span data-stu-id="9d6bf-117">Phase 3: Deploy Lync Server 2013 pilot pool</span></span>](phase-3-deploy-lync-server-2013-pilot-pool.md)

4.  [<span data-ttu-id="9d6bf-118">Этап 4: перемещение тестовых пользователей в пилотный пул</span><span class="sxs-lookup"><span data-stu-id="9d6bf-118">Phase 4: Move test users to the pilot pool</span></span>](phase-4-move-test-users-to-the-pilot-pool.md)

5.  [<span data-ttu-id="9d6bf-119">Этап 5: Добавление сервера Lync Server 2013 EDGE на пилотный пул</span><span class="sxs-lookup"><span data-stu-id="9d6bf-119">Phase 5: Add Lync Server 2013 Edge Server to pilot pool</span></span>](phase-5-add-lync-server-2013-edge-server-to-pilot-pool.md)

6.  [<span data-ttu-id="9d6bf-120">Этап 6: переход от пилотного развертывания к рабочей версии</span><span class="sxs-lookup"><span data-stu-id="9d6bf-120">Phase 6: Move from pilot deployment into production</span></span>](phase-6-move-from-pilot-deployment-into-production.md)

7.  [<span data-ttu-id="9d6bf-121">Этап 7: необходимые действия после миграции</span><span class="sxs-lookup"><span data-stu-id="9d6bf-121">Phase 7: Complete post-migration tasks</span></span>](phase-7-complete-post-migration-tasks.md)

8.  [<span data-ttu-id="9d6bf-122">Этап 8: ликвидация старых пулов</span><span class="sxs-lookup"><span data-stu-id="9d6bf-122">Phase 8: Decommission legacy pools</span></span>](phase-8-decommission-legacy-pools.md)

<span data-ttu-id="9d6bf-123"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9d6bf-123"></div>

<span> </span>

</div>

</div>

</span></span></div>

