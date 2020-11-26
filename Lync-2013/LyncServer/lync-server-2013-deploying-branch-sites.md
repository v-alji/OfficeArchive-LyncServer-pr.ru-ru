---
title: 'Lync Server 2013: развертывание сайтов филиалов'
description: 'Lync Server 2013: развертывание сайтов филиалов.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying branch sites
ms:assetid: 1475dee0-66ae-4ee5-b6f1-7409b4bbff45
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398217(v=OCS.15)
ms:contentKeyID: 48183483
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d653e3f06de832693d97bfb229f122a67c28640e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430093"
---
# <a name="deploying-branch-sites-in-lync-server-2013"></a><span data-ttu-id="464a8-103">Развертывание сайтов филиалов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="464a8-103">Deploying branch sites in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="464a8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="464a8-104">

<span> </span></span></span>

<span data-ttu-id="464a8-105">_**Тема последнего изменения:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="464a8-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="464a8-106">Пользователи сайтов филиалов получают большинство функций Lync Server 2013 с сервера центрального сайта, с которым связан сайт филиала.</span><span class="sxs-lookup"><span data-stu-id="464a8-106">Branch site users get most of their Lync Server 2013 functionality from the server at the central site that the branch site is associated with.</span></span> <span data-ttu-id="464a8-107">Каждый сайт филиала связан только с одним центральным сайтом.</span><span class="sxs-lookup"><span data-stu-id="464a8-107">Each branch site is associated with exactly one central site.</span></span> <span data-ttu-id="464a8-108">Для передачи звонков из коммутируемой телефонной сети с открытым коммутируемым подключением сайт филиала может содержать любые из указанных ниже вариантов.</span><span class="sxs-lookup"><span data-stu-id="464a8-108">To provide calls to and from the public switched telephone network (PSTN), a branch site might contain any of the following:</span></span>

  - <span data-ttu-id="464a8-109">Шлюз PSTN и, возможно, сервер Meditation</span><span class="sxs-lookup"><span data-stu-id="464a8-109">A PSTN gateway and possibly a Meditation Server</span></span>

  - <span data-ttu-id="464a8-110">Магистральная линия SIP</span><span class="sxs-lookup"><span data-stu-id="464a8-110">A SIP trunk</span></span>

  - <span data-ttu-id="464a8-111">Существующая инфраструктура голосовой связи с частным обменом филиалов (АТС)</span><span class="sxs-lookup"><span data-stu-id="464a8-111">An existing voice infrastructure with a private branch exchange (PBX)</span></span>

  - <span data-ttu-id="464a8-112">Бесперебойно работающее устройство филиала</span><span class="sxs-lookup"><span data-stu-id="464a8-112">A Survivable Branch Appliance</span></span>

  - <span data-ttu-id="464a8-113">Бесперебойный сервер филиала</span><span class="sxs-lookup"><span data-stu-id="464a8-113">A Survivable Branch Server</span></span>

<span data-ttu-id="464a8-114">Сайты филиалов с бесперебойно работающими управляющими системами или работающими серверами филиалов более устойчивы во время многофакторной сети или сбоя центрального сайта, чем для сайтов филиалов без одного из этих решений.</span><span class="sxs-lookup"><span data-stu-id="464a8-114">Branch sites with a Survivable Branch Appliance or a Survivable Branch Server are more resilient in times of wide-area network or central site failures than branch sites without one of these solutions.</span></span> <span data-ttu-id="464a8-115">Например, на сайте с бесперебойно работающим управляющим устройством филиала или развернутом работающем сервере филиала пользователи по-прежнему могут совершать и принимать звонки PSTN, если сеть, соединяющая сайт ветви с центральным сайтом, не работает.</span><span class="sxs-lookup"><span data-stu-id="464a8-115">For example, in a site with a Survivable Branch Appliance or a Survivable Branch Server deployed, users can still make and receive PSTN calls if the network connecting the branch site to the central site is down.</span></span> <span data-ttu-id="464a8-116">Кроме того, вы можете достичь устойчивости сайта с помощью шлюза PSTN или магистральной магистрали SIP с полным развертыванием Lync Server на сайте филиала.</span><span class="sxs-lookup"><span data-stu-id="464a8-116">Another way to achieve branch-site resiliency is by using a PSTN gateway or a SIP trunk with a full-scale Lync Server deployment at the branch site.</span></span>

<span data-ttu-id="464a8-117">Сведения о том, какое развертывание сайтов филиалов подходит для вашей организации, в том числе о предварительных требованиях и других вопросах планирования, приведены в разделе [Планирование подключений PSTN в Lync server 2013](lync-server-2013-planning-for-pstn-connectivity.md) и [Планирование обеспечения устойчивости голоса на филиалах в Lync Server 2013](lync-server-2013-planning-for-branch-site-voice-resiliency.md) в документации по планированию.</span><span class="sxs-lookup"><span data-stu-id="464a8-117">For details about which branch site deployment is right for your organization, including prerequisites and other planning considerations, see [Planning for PSTN connectivity in Lync Server 2013](lync-server-2013-planning-for-pstn-connectivity.md) and [Planning for branch-site voice resiliency in Lync Server 2013](lync-server-2013-planning-for-branch-site-voice-resiliency.md) in the Planning documentation.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="464a8-118">Содержание</span><span class="sxs-lookup"><span data-stu-id="464a8-118">In This Section</span></span>

  - [<span data-ttu-id="464a8-119">Обеспечение подключения ТСОП в сайте филиала в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="464a8-119">Providing PSTN connectivity at a branch site in Lync Server 2013</span></span>](lync-server-2013-providing-pstn-connectivity-at-a-branch-site.md)

  - [<span data-ttu-id="464a8-120">Развертывание устройства или сервера обеспечения связи в филиалах с Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="464a8-120">Deploying a Survivable Branch Appliance or Server with Lync Server 2013</span></span>](lync-server-2013-deploying-a-survivable-branch-appliance-or-server.md)

<span data-ttu-id="464a8-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="464a8-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

