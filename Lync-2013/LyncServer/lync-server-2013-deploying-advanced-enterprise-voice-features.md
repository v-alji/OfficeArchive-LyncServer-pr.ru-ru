---
title: 'Lync Server 2013: развертывание расширенных корпоративных голосовых функций'
description: 'Lync Server 2013: развертывание улучшенных функций голосовой связи в корпоративной среде.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying advanced Enterprise Voice features
ms:assetid: 286d9c0b-9442-448f-a6e5-95b3034278fe
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425753(v=OCS.15)
ms:contentKeyID: 48183675
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e5cab05de60e1df1611a14af1f5239c24402c6d9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430114"
---
# <a name="deploying-advanced-enterprise-voice-features-in-lync-server-2013"></a><span data-ttu-id="32b46-103">Развертывание улучшенных функций голосовой связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="32b46-103">Deploying advanced Enterprise Voice features in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="32b46-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="32b46-104">

<span> </span></span></span>

<span data-ttu-id="32b46-105">_**Тема последнего изменения:** 2012-09-22_</span><span class="sxs-lookup"><span data-stu-id="32b46-105">_**Topic Last Modified:** 2012-09-22_</span></span>

<span data-ttu-id="32b46-106">После настройки базовых функций Enterprise Voice для организации можно при необходимости развернуть одну или несколько расширенных функций Enterprise Voice, выполнив процедуры, описанные в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="32b46-106">After you have configured basic Enterprise Voice functionality for your organization, you can optionally deploy one or more advanced Enterprise Voice features by following the procedures in this section.</span></span>

<span data-ttu-id="32b46-107">Подробнее о расширенных функциях голосовой связи в разделе [планирование для Lync Server 2013](lync-server-2013-planning.md) можно найти в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="32b46-107">For details about the advanced Enterprise Voice features, see the following sections of the [Planning for Lync Server 2013](lync-server-2013-planning.md) documentation:</span></span>

  - [<span data-ttu-id="32b46-108">Планирование контроля допуска звонков в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="32b46-108">Planning for call admission control in Lync Server 2013</span></span>](lync-server-2013-planning-for-call-admission-control.md)

  - [<span data-ttu-id="32b46-109">Планирование чрезвычайных служб (E9-1-1) в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="32b46-109">Planning for emergency services (E9-1-1) in Lync Server 2013</span></span>](lync-server-2013-planning-for-emergency-services-e9-1-1.md)

  - [<span data-ttu-id="32b46-110">Планирование обхода серверов-посредников в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="32b46-110">Planning for media bypass in Lync Server 2013</span></span>](lync-server-2013-planning-for-media-bypass.md)

<div>

## <a name="in-this-section"></a><span data-ttu-id="32b46-111">Содержание</span><span class="sxs-lookup"><span data-stu-id="32b46-111">In This Section</span></span>

  - [<span data-ttu-id="32b46-112">О сетевых областях, сайтах и подсетях в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="32b46-112">About network regions, sites, and subnets in Lync Server 2013</span></span>](lync-server-2013-about-network-regions-sites-and-subnets.md)

  - [<span data-ttu-id="32b46-113">Создание или изменение сетевого региона в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="32b46-113">Create or modify a network region in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-network-region.md)

  - [<span data-ttu-id="32b46-114">Создание или изменение сетевого сайта в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="32b46-114">Create or modify a network site in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-network-site.md)

  - [<span data-ttu-id="32b46-115">Связь подсети с сетевым сайтом в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="32b46-115">Associate a subnet with a network site in Lync Server 2013</span></span>](lync-server-2013-associate-a-subnet-with-a-network-site.md)

  - [<span data-ttu-id="32b46-116">Настройка управления допуском звонков в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="32b46-116">Configure call admission control in Lync Server 2013</span></span>](lync-server-2013-configure-call-admission-control.md)

  - [<span data-ttu-id="32b46-117">Настройка службы Enhanced 9-1-1 в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="32b46-117">Configure Enhanced 9-1-1 in Lync Server 2013</span></span>](lync-server-2013-configure-enhanced-9-1-1.md)

  - [<span data-ttu-id="32b46-118">Настройка обхода сервера-посредника в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="32b46-118">Configure media bypass in Lync Server 2013</span></span>](lync-server-2013-configure-media-bypass.md)

<span data-ttu-id="32b46-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="32b46-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

