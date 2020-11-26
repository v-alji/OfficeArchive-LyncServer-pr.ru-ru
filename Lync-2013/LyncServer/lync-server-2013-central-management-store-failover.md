---
title: 'Lync Server 2013: отработка отказа центральным хранилищем управления'
description: Отработка отказа в магазине Lync Server 2013 Central Management.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Central Management store failover
ms:assetid: f464d715-68a4-462c-9584-00f41ab10db0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205376(v=OCS.15)
ms:contentKeyID: 48185809
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d2960a55d6bdc49e00bf22997bc53946d4770fde
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435469"
---
# <a name="central-management-store-failover-in-lync-server-2013"></a><span data-ttu-id="e5de1-103">Отработка отказа центральным хранилищем управления в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e5de1-103">Central Management store failover in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e5de1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e5de1-104">

<span> </span></span></span>

<span data-ttu-id="e5de1-105">_**Тема последнего изменения:** 2012-10-18_</span><span class="sxs-lookup"><span data-stu-id="e5de1-105">_**Topic Last Modified:** 2012-10-18_</span></span>

<span data-ttu-id="e5de1-106">В хранилище Центрального управления содержатся данные о конфигурации серверов и служб в развертывании Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="e5de1-106">The Central Management store contains configuration data about servers and services in your Lync 2013 deployment.</span></span> <span data-ttu-id="e5de1-107">Она предоставляет надежное хранилище schematized данных, необходимых для определения, настройки, обслуживания, администрирования, описания и работы с развертыванием Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="e5de1-107">It provides a robust, schematized storage of the data needed to define, set up, maintain, administer, describe, and operate a Lync 2013 deployment.</span></span> <span data-ttu-id="e5de1-108">Кроме того, оно обеспечивает проверку этих данных на предмет внутренней согласованности.</span><span class="sxs-lookup"><span data-stu-id="e5de1-108">It also validates the data to ensure configuration consistency.</span></span>

<span data-ttu-id="e5de1-109">Каждое развертывание Lync включает в себя единое центральное хранилище, которое размещается на сервере переднего плана для первого пула.</span><span class="sxs-lookup"><span data-stu-id="e5de1-109">Each Lync deployment includes one Central Management store, which is hosted by the Back End Server of one Front End pool.</span></span>

<span data-ttu-id="e5de1-110">Если вы установили пару пулов, включающую пул, в котором размещено хранилище Центрального управления, в пуле архивации настраивается база данных централизованного управления резервным копированием, а также в обоих пулах устанавливаются службы централизованного управления хранилищем.</span><span class="sxs-lookup"><span data-stu-id="e5de1-110">When you establish a pool pairing that includes the pool hosting the Central Management store, a backup Central Management store database is set up in the backup pool, and Central Management store services are installed in both pools.</span></span> <span data-ttu-id="e5de1-111">В любой момент времени одна из двух баз данных центрального хранилища может быть активной, а другая — в режиме ожидания.</span><span class="sxs-lookup"><span data-stu-id="e5de1-111">At any point in time, one of the two Central Management store databases is the active master, and the other is a standby.</span></span> <span data-ttu-id="e5de1-112">Содержимое реплицируется службой резервного копирования из активного образца в ждущий режим.</span><span class="sxs-lookup"><span data-stu-id="e5de1-112">The content is replicated by the Backup Service from the active master to the standby.</span></span>

<span data-ttu-id="e5de1-113">Во время отработки отказа пула, включающего в себя пулы, в которых размещено центральное хранилище, администратор должен отдать сбой на центральное хранилище управления, прежде чем переходить на пул переднего плана.</span><span class="sxs-lookup"><span data-stu-id="e5de1-113">During a pool failover that involves the pools hosting the Central Management store, the administrator must fail over the Central Management store before failing over the Front End pool.</span></span>

<span data-ttu-id="e5de1-114">После ликвидации аварийной ситуации восстановление размещения центрального хранилища управления не требуется.</span><span class="sxs-lookup"><span data-stu-id="e5de1-114">After the disaster is repaired, it is not necessary to fail back the Central Management store.</span></span> <span data-ttu-id="e5de1-115">После восстановления хранилище Центрального управления в исходном пуле резервных копий может оставаться активным.</span><span class="sxs-lookup"><span data-stu-id="e5de1-115">After repair, the Central Management store in the original backup pool can remain as the active master.</span></span>

<span data-ttu-id="e5de1-116">В соответствии с проектными задачами при отработке отказа для центрального хранилища управления целевое время восстановления (RTO) составляет 5 минут, а целевая точка восстановления (RPO) — 5 минут.</span><span class="sxs-lookup"><span data-stu-id="e5de1-116">The engineering targets for Central Management store failover are 5 minutes for recovery time objective (RTO) and 5 minutes for recovery point objective (RPO).</span></span>

<span data-ttu-id="e5de1-117"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e5de1-117"></div>

<span> </span>

</div>

</div>

</span></span></div>

