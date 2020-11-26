---
title: Подключение Survivable Branch Appliance к пулу переднего плана Lync Server 2013
description: Подключение устройства с бесперебойной подразделением к пуле внешних интерфейсов Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Connecting Survivable Branch Appliance to Lync Server 2013 Front End pool
ms:assetid: 3c7ca33f-5295-4d82-9152-41d8bc6f35cf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688026(v=OCS.15)
ms:contentKeyID: 49733616
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6ef917d3db6a1d653ac716d6c078e1df240fb31d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432263"
---
# <a name="connecting-survivable-branch-appliance-to-lync-server-2013-front-end-pool"></a><span data-ttu-id="7c000-103">Подключение Survivable Branch Appliance к пулу переднего плана Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7c000-103">Connecting Survivable Branch Appliance to Lync Server 2013 Front End pool</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7c000-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7c000-104">

<span> </span></span></span>

<span data-ttu-id="7c000-105">_**Тема последнего изменения:** 2012-10-05_</span><span class="sxs-lookup"><span data-stu-id="7c000-105">_**Topic Last Modified:** 2012-10-05_</span></span>

<span data-ttu-id="7c000-106">Каждое работающее устройство филиала (SBA) связано с пулом переднего плана, который выступает в качестве регистратора резервных копий для SBA.</span><span class="sxs-lookup"><span data-stu-id="7c000-106">Every Survivable Branch Appliance (SBA) is associated with a Front End pool, which serves as a backup Registrar for the SBA.</span></span> <span data-ttu-id="7c000-107">Когда пул переднего плана обновляется до Lync Server 2013, SBA должен быть связан с пулом переднего плана, пока пул переднего плана будет обновлен.</span><span class="sxs-lookup"><span data-stu-id="7c000-107">When the Front End pool is upgraded to Lync Server 2013, the SBA must be disassociated from the Front End pool while the Front End pool is upgraded.</span></span> <span data-ttu-id="7c000-108">После обновления пула переднего плана SBA можно связать с пулом переднего плана.</span><span class="sxs-lookup"><span data-stu-id="7c000-108">After the Front End pool is upgraded, the SBA can be reassociated with the Front End pool.</span></span> <span data-ttu-id="7c000-109">Это связано с тем, что удаление SBA из топологии в построителе топологии и повторное добавление SBA для Topology Builder.</span><span class="sxs-lookup"><span data-stu-id="7c000-109">This involves deleting the SBA from the topology in Topology Builder and then adding the SBA, again, to Topology Builder.</span></span> <span data-ttu-id="7c000-110">Пользователи, размещенные на SBA, должны быть перемещены в другой пул переднего плана, прежде чем удалять SBA из топологии.</span><span class="sxs-lookup"><span data-stu-id="7c000-110">Users homed on the SBA must be moved to another Front End pool before removing the SBA from the topology.</span></span> <span data-ttu-id="7c000-111">После того как SBA снова добавится в топологию, эти пользователи могут быть возвращены в SBA.</span><span class="sxs-lookup"><span data-stu-id="7c000-111">After the SBA is added back to the topology, those users can be moved back to the SBA.</span></span>

<span data-ttu-id="7c000-112">Эти действия описаны ниже.</span><span class="sxs-lookup"><span data-stu-id="7c000-112">These steps are summarized below:</span></span>

1.  <span data-ttu-id="7c000-113">Перемещение пользователей филиалов, размещенных на SBA, в другой пул переднего плана.</span><span class="sxs-lookup"><span data-stu-id="7c000-113">Move branch users homed on SBA to another Front End pool.</span></span>

2.  <span data-ttu-id="7c000-114">Удалите SBA из топологии, чтобы разорвать существующий пул переднего плана в качестве регистратора резервных копий.</span><span class="sxs-lookup"><span data-stu-id="7c000-114">Remove SBA from your topology to disassociate the existing Front End pool as the backup Registrar.</span></span>

3.  <span data-ttu-id="7c000-115">Обновите пул переднего плана до Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="7c000-115">Upgrade Front End pool to Microsoft Lync Server 2013.</span></span>

4.  <span data-ttu-id="7c000-116">Добавьте SBA обратно в топологию.</span><span class="sxs-lookup"><span data-stu-id="7c000-116">Add SBA back into your topology.</span></span>

5.  <span data-ttu-id="7c000-117">Свяжите новый пул переднего плана с SBA в качестве регистратора резервных копий.</span><span class="sxs-lookup"><span data-stu-id="7c000-117">Associate the new Front End pool to the SBA as a backup Registrar.</span></span>

6.  <span data-ttu-id="7c000-118">Переместить пользователей филиалов обратно в SBA.</span><span class="sxs-lookup"><span data-stu-id="7c000-118">Move branch users back to the SBA.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="7c000-119">Содержание</span><span class="sxs-lookup"><span data-stu-id="7c000-119">In This Section</span></span>

  - [<span data-ttu-id="7c000-120">Добавление в топологию сайта филиала устройства для обеспечения связи в филиалах Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7c000-120">Add Lync Server 2013 Survivable Branch Appliance branch site to your topology</span></span>](lync-server-2013-add-lync-server-2013-survivable-branch-appliance-branch-site-to-your-topology.md)

  - [<span data-ttu-id="7c000-121">Добавление сайта филиала Lync Server 2010 Survivable Branch Appliance в топологию</span><span class="sxs-lookup"><span data-stu-id="7c000-121">Add Lync Server 2010 Survivable Branch Appliance branch site to your topology</span></span>](lync-server-2013-add-lync-server-2010-survivable-branch-appliance-branch-site-to-your-topology.md)

<span data-ttu-id="7c000-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7c000-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

