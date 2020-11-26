---
title: 'Lync Server 2013: резервное копирование и восстановление сервера Lync Server'
description: 'Lync Server 2013: резервное копирование и восстановление сервера Lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Backing up and restoring Lync Server 2013
ms:assetid: 07dc1f5e-af66-4e18-bf39-881dceff8bc3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202160(v=OCS.15)
ms:contentKeyID: 51541443
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c1a7024b2264fb895d1562a6da0775f9397644b4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438143"
---
# <a name="backing-up-and-restoring-lync-server-2013"></a><span data-ttu-id="f1172-103">Резервное копирование и восстановление Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f1172-103">Backing up and restoring Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f1172-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f1172-104">

<span> </span></span></span>

<span data-ttu-id="f1172-105">_**Тема последнего изменения:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="f1172-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="f1172-106">В этом разделе вы найдете рекомендации по резервному созданию данных Lync Server 2013 и их восстановления в случае сбоя.</span><span class="sxs-lookup"><span data-stu-id="f1172-106">In this section, you’ll find the best practices for backing up your Lync Server 2013 data, and for restoring it if you have a failure.</span></span> <span data-ttu-id="f1172-107">Эти рекомендации относятся к следующим ситуациям:</span><span class="sxs-lookup"><span data-stu-id="f1172-107">These best practices apply to the following situations:</span></span>

  - <span data-ttu-id="f1172-108">Весь пул серверов Lync Server любого типа (сервер переднего плана, пограничный сервер, сервер-посредник, сервер, на котором сохранен чат или режиссер) или отдельный сервер в одном из этих пулов.</span><span class="sxs-lookup"><span data-stu-id="f1172-108">An entire Lync Server pool of any type (Front End Server, Edge Server, Mediation Server, Persistent Chat Server, or Director), or an individual server in one of these pools.</span></span>

  - <span data-ttu-id="f1172-109">Центральный сервер управления</span><span class="sxs-lookup"><span data-stu-id="f1172-109">The Central Management Server</span></span>

  - <span data-ttu-id="f1172-110">Сервер стандартных выпусков</span><span class="sxs-lookup"><span data-stu-id="f1172-110">A Standard Edition server</span></span>

  - <span data-ttu-id="f1172-111">Сервер заднего выпуска Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="f1172-111">An Enterprise Edition Back End Server</span></span>

  - <span data-ttu-id="f1172-112">Хранилище файлов</span><span class="sxs-lookup"><span data-stu-id="f1172-112">A File Store</span></span>

  - <span data-ttu-id="f1172-113">База данных для архивации, база данных мониторинга или сохраняемая база данных чата</span><span class="sxs-lookup"><span data-stu-id="f1172-113">An Archiving database, Monitoring database, or Persistent Chat database</span></span>

<span data-ttu-id="f1172-114">Этот раздел не содержит сведений о восстановлении сайта целиком или для разработки резервного сайта.</span><span class="sxs-lookup"><span data-stu-id="f1172-114">This section does not include information about restoring an entire site or for developing a standby site.</span></span> <span data-ttu-id="f1172-115">Сведения о разработке решения аварийного восстановления с подключенными внешними пулами можно найти [в разделе Планирование обеспечения высокой доступности и аварийного восстановления в Lync Server 2013](lync-server-2013-planning-for-high-availability-and-disaster-recovery.md).</span><span class="sxs-lookup"><span data-stu-id="f1172-115">For details about developing a disaster recovery solution with paired Front End pools, see [Planning for high availability and disaster recovery in Lync Server 2013](lync-server-2013-planning-for-high-availability-and-disaster-recovery.md).</span></span> <span data-ttu-id="f1172-116">Это рекомендуемый способ планирования аварийного восстановления.</span><span class="sxs-lookup"><span data-stu-id="f1172-116">This is the recommended method for planning for disaster recovery.</span></span>

<span data-ttu-id="f1172-117">Если вы развернули Объединенные пулы интерфейсных элементов, то если один из этих пулов завершается сбоем и становится невосстанавливаемым, вы можете восстановить его с помощью нового полного доменного имени (FQDN) из его парного пула.</span><span class="sxs-lookup"><span data-stu-id="f1172-117">If you have deployed paired Front End pools, if one of these pools fails and becomes unrecoverable, you can restore this pool with a new fully qualified domain name (FQDN) from its paired pool.</span></span> <span data-ttu-id="f1172-118">Подробнее о том, как выполнить это восстановление, можно найти [в статье отказ пула в Lync Server 2013](lync-server-2013-failing-over-a-pool.md).</span><span class="sxs-lookup"><span data-stu-id="f1172-118">For details on the steps to perform this recovery, see [Failing over a pool in Lync Server 2013](lync-server-2013-failing-over-a-pool.md).</span></span> <span data-ttu-id="f1172-119">Кроме того, если позже вам потребуется повторно создать Невосстановленный пул, который являлся частью пары интерфейсов, вы можете выполнить действия, описанные в разделе [выполнение отработки отказа в пуле для интерфейса ABC на Lync Server 2013](lync-server-2013-performing-an-abc-front-end-pool-failover.md).</span><span class="sxs-lookup"><span data-stu-id="f1172-119">Additionally, if you later want to recreate a failed and unrecoverable pool that was part of a Front End pair, you can use the steps in [Performing an ABC Front End pool failover in Lync Server 2013](lync-server-2013-performing-an-abc-front-end-pool-failover.md).</span></span>

<span data-ttu-id="f1172-120">В описанной в этом документе методологии используются специальные моменты на этапе планирования.</span><span class="sxs-lookup"><span data-stu-id="f1172-120">The methodology described in this document involves special considerations during the planning phase.</span></span> <span data-ttu-id="f1172-121">Подробные сведения можно найти [в разделе Создание резервной копии и плана восстановления для Lync Server 2013](lync-server-2013-establishing-a-backup-and-restoration-plan.md).</span><span class="sxs-lookup"><span data-stu-id="f1172-121">For details, see [Establishing a backup and restoration plan for Lync Server 2013](lync-server-2013-establishing-a-backup-and-restoration-plan.md).</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="f1172-122">Содержание</span><span class="sxs-lookup"><span data-stu-id="f1172-122">In This Section</span></span>

  - [<span data-ttu-id="f1172-123">Подготовка к резервному копированию и восстановлению для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f1172-123">Preparing for Lync Server 2013 backup and restoration</span></span>](lync-server-2013-preparing-for-lync-server-backup-and-restoration.md)

  - [<span data-ttu-id="f1172-124">Резервное копирование данных и параметров в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f1172-124">Backing up data and settings in Lync Server 2013</span></span>](lync-server-2013-backing-up-data-and-settings.md)

  - [<span data-ttu-id="f1172-125">Восстановление данных и параметров в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f1172-125">Restoring data and settings in Lync Server 2013</span></span>](lync-server-2013-restoring-data-and-settings.md)

  - [<span data-ttu-id="f1172-126">Журналы резервного копирования и восстановления для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f1172-126">Backup and restoration worksheets for Lync Server 2013</span></span>](lync-server-2013-backup-and-restoration-worksheets.md)

<span data-ttu-id="f1172-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f1172-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

