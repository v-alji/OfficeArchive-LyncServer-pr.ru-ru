---
title: Замечания по сосуществованию
description: Рекомендации по сосуществованию.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Coexistence considerations
ms:assetid: 9d1a3c0f-492a-4e37-bc2f-63509e328785
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205131(v=OCS.15)
ms:contentKeyID: 48184990
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fd1f9525b37bdee3249e0e47352fdea1bc7f012f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399181"
---
# <a name="coexistence-considerations"></a><span data-ttu-id="270b0-103">Замечания по сосуществованию</span><span class="sxs-lookup"><span data-stu-id="270b0-103">Coexistence considerations</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="270b0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="270b0-104">

<span> </span></span></span>

<span data-ttu-id="270b0-105">_**Тема последнего изменения:** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="270b0-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="270b0-106">После миграции будет существовать только сервер Lync Server 2013, пул серверов сохраняемого чата, и вы можете списать устаревшее развертывание.</span><span class="sxs-lookup"><span data-stu-id="270b0-106">After migration, only a Lync Server 2013, Persistent Chat Server pool will exist, and you can decommission your legacy deployment.</span></span>

<span data-ttu-id="270b0-107">Перед тем как вы завершите миграцию и до того, как вы полностью намерены списать текущее развертывание сервера группового чата, вы можете использовать любое из указанных ниже развертываний.</span><span class="sxs-lookup"><span data-stu-id="270b0-107">Before migration completes and before you have decommissioned your current Group Chat Server deployment completely, you may have any of the following deployments:</span></span>

  - <span data-ttu-id="270b0-108">Сервер Lync Server 2013, пул серверов сохраняемого чата, который должен находиться в пуле Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="270b0-108">Lync Server 2013, Persistent Chat Server pool, which must be homed on a Lync Server 2013 pool.</span></span>

  - <span data-ttu-id="270b0-109">Lync Server 2010, пул группового чата, который должен быть расположен в пуле Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="270b0-109">Lync Server 2010, Group Chat pool, which must be homed on a Lync Server 2010 pool.</span></span>

  - <span data-ttu-id="270b0-110">Пул группового чата Office Communications Server 2007 R2, который должен быть расположен в пуле Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="270b0-110">Office Communications Server 2007 R2 Group Chat pool, which must be homed on an Office Communications Server 2007 R2 pool.</span></span>

<span data-ttu-id="270b0-111">Эти развертывания могут находиться рядом друг с другом.</span><span class="sxs-lookup"><span data-stu-id="270b0-111">These deployments can exist side by side.</span></span> <span data-ttu-id="270b0-112">Однако категории, комнаты и надстройки в одном развертывании не взаимодействуют с теми, которые находятся в сопутствующем развертывании.</span><span class="sxs-lookup"><span data-stu-id="270b0-112">However the categories, rooms, and add-ins in one deployment do not interact with those in the accompanying deployment.</span></span>

<span data-ttu-id="270b0-113">При использовании ручного конфигурирования для Office Communications Server 2007 R2, Lync Server 2010, группового чата или Lync Server 2013 вы можете подключаться к одному пулу за один из стандартных клиентов (клиент группового чата).</span><span class="sxs-lookup"><span data-stu-id="270b0-113">Using manual configuration, a legacy client (Group Chat client) can connect to one pool at a time for Office Communications Server 2007 R2, Lync Server 2010, Group Chat, or Lync Server 2013.</span></span>

<span data-ttu-id="270b0-114">Lync 2013 (клиент) может взаимодействовать только с серверным пулом Lync Server 2013, сохраняемым чат, а не с пулами серверов группового чата.</span><span class="sxs-lookup"><span data-stu-id="270b0-114">The Lync 2013 (client) can interact only with the Lync Server 2013, Persistent Chat Server pool, not with legacy Group Chat Server pools.</span></span> <span data-ttu-id="270b0-115">Для использования сохраняемого чата в Lync 2013 (клиент) пользователь должен быть расположен в Lync 2013 и включен в соответствии с политикой.</span><span class="sxs-lookup"><span data-stu-id="270b0-115">To use Persistent Chat in a Lync 2013 (client), the user must be homed on Lync 2013 and enabled by policy.</span></span>

<span data-ttu-id="270b0-116"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="270b0-116"></div>

<span> </span>

</div>

</div>

</span></span></div>

