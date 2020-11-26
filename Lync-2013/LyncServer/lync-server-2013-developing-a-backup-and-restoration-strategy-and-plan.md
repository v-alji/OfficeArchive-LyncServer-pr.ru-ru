---
title: 'Lync Server 2013: Разработка стратегии резервного копирования и восстановления и плана'
description: 'Lync Server 2013: Разработка стратегии резервного копирования и восстановления и планирование.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Developing a backup and restoration strategy and plan
ms:assetid: 17599b76-1a84-4dd6-b695-c19637deb8a6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202164(v=OCS.15)
ms:contentKeyID: 51541447
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3d55eeb541cdde5c43d7d680ceb212d87da0d517
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429454"
---
# <a name="developing-a-backup-and-restoration-strategy-and-plan-for-lync-server-2013"></a><span data-ttu-id="88b68-103">Разработка стратегии резервного копирования и восстановления и планирование для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="88b68-103">Developing a backup and restoration strategy and plan for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="88b68-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="88b68-104">

<span> </span></span></span>

<span data-ttu-id="88b68-105">_**Тема последнего изменения:** 2013-02-17_</span><span class="sxs-lookup"><span data-stu-id="88b68-105">_**Topic Last Modified:** 2013-02-17_</span></span>

<span data-ttu-id="88b68-106">Эффективность резервного копирования и восстановления сервера Lync Server зависит от стратегии и резервного копирования и плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="88b68-106">The effectiveness of your Lync Server backup and restoration operations depends on your backup and restoration strategy and plan.</span></span> <span data-ttu-id="88b68-107">Вы должны создать стратегию резервного копирования и восстановления сервера Lync, который подходит для общей стратегии Организации, и подробный, краткий план резервного копирования данных и параметров, а также в случае сбоя план восстановления служб.</span><span class="sxs-lookup"><span data-stu-id="88b68-107">You should establish a strategy for backing up and restoring Lync Server that fits with your organization's overall strategy, and a comprehensive, concise plan for backing up data and settings, and, in the event of an outage, a plan for restoring service.</span></span>

<span data-ttu-id="88b68-108">Для наиболее надежной аварийной ситуации, которая появилась в Lync Server 2013, используйте топологию аварийного восстановления с сопряженными пулами.</span><span class="sxs-lookup"><span data-stu-id="88b68-108">For the most robust disaster recovery of a Front End Pool, use the paired-pool disaster recovery topology introduced in Lync Server 2013.</span></span> <span data-ttu-id="88b68-109">Дополнительные сведения можно найти [в разделе Планирование обеспечения высокой доступности и аварийного восстановления в Lync Server 2013](lync-server-2013-planning-for-high-availability-and-disaster-recovery.md).</span><span class="sxs-lookup"><span data-stu-id="88b68-109">For more information, see [Planning for high availability and disaster recovery in Lync Server 2013](lync-server-2013-planning-for-high-availability-and-disaster-recovery.md).</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="88b68-110">Содержание</span><span class="sxs-lookup"><span data-stu-id="88b68-110">In This Section</span></span>

  - [<span data-ttu-id="88b68-111">Установка стратегии резервного копирования и восстановления для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="88b68-111">Establishing a backup and restoration strategy for Lync Server 2013</span></span>](lync-server-2013-establishing-a-backup-and-restoration-strategy.md)

  - [<span data-ttu-id="88b68-112">Установка плана резервного копирования и восстановления для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="88b68-112">Establishing a backup and restoration plan for Lync Server 2013</span></span>](lync-server-2013-establishing-a-backup-and-restoration-plan.md)

  - [<span data-ttu-id="88b68-113">Настройка расположения резервной копии для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="88b68-113">Setting up a backup location for Lync Server 2013</span></span>](lync-server-2013-setting-up-a-backup-location.md)

<span data-ttu-id="88b68-114"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="88b68-114"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

