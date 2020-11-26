---
title: 'Lync Server 2013: поддержка нескольких каналов'
description: 'Lync Server 2013: поддержка нескольких каналов.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Multiple trunk support
ms:assetid: a1309c09-ad9a-4c54-9650-4e3f5b2a4a00
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205127(v=OCS.15)
ms:contentKeyID: 48184948
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3bbabb90405b3fdae47a59ba8a0798743943216d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425207"
---
# <a name="multiple-trunk-support-in-lync-server-2013"></a><span data-ttu-id="2e46b-103">Поддержка нескольких каналов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2e46b-103">Multiple trunk support in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2e46b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2e46b-104">

<span> </span></span></span>

<span data-ttu-id="2e46b-105">_**Тема последнего изменения:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="2e46b-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="2e46b-106">Lync Server 2013 поддерживает множественные ассоциации между шлюзами и серверами исправлений.</span><span class="sxs-lookup"><span data-stu-id="2e46b-106">Lync Server 2013 functionality supports multiple associations between gateways and Mediation Servers.</span></span> <span data-ttu-id="2e46b-107">Эти связи выполняются путем определения канала, который является логической связью между пулом серверов «исправление» и шлюзом коммутируемой телефонной сети (КТСОП), контроллером границ сеансов (SBC) или IP-УАТС.</span><span class="sxs-lookup"><span data-stu-id="2e46b-107">These associations are made by defining a trunk, which is a logical association between a Mediation Server pool and a public switched telephone network (PSTN) gateway, Session Border Controller (SBC), or IP-PBX.</span></span> <span data-ttu-id="2e46b-108">С помощью построителя топологии свяжите шлюзы с серверами-посредниками (то есть магистральами).</span><span class="sxs-lookup"><span data-stu-id="2e46b-108">Use the Topology Builder to associate gateways with Mediation Servers (that is, trunks).</span></span>

  - <span data-ttu-id="2e46b-109">Чтобы назначить или удалить магистраль в Lync Server 2013, необходимо сначала определить магистраль в построителе топологии.</span><span class="sxs-lookup"><span data-stu-id="2e46b-109">To assign or remove a trunk in Lync Server 2013, you must first define a trunk in Topology Builder.</span></span> <span data-ttu-id="2e46b-110">Магистраль состоит из следующей ассоциации: полное доменное имя (FQDN) сервера исходящих сообщений, а также имя шлюза и порт для прослушивания шлюза.</span><span class="sxs-lookup"><span data-stu-id="2e46b-110">A trunk consists of the following association: Mediation Server fully qualified domain name (FQDN), the Mediation Server listening port, the gateway FQDN, and the gateway listening port.</span></span>

  - <span data-ttu-id="2e46b-111">Чтобы настроить несколько каналов связи, вы можете создать несколько ассоциаций между одним и тем же шлюзом и сервером обновлений.</span><span class="sxs-lookup"><span data-stu-id="2e46b-111">To configure multiple trunks, you can create multiple associations between the same gateway and the Mediation Server.</span></span> <span data-ttu-id="2e46b-112">Это обеспечивает дополнительную устойчивость к корпоративной инфраструктуре голосовой связи, которая особенно полезна в сценариях взаимодействия между частными филиалами (АТС).</span><span class="sxs-lookup"><span data-stu-id="2e46b-112">This provides additional resiliency to the Enterprise Voice infrastructure, which is especially useful in private branch exchange (PBX) interoperational scenarios.</span></span>

<span data-ttu-id="2e46b-113">When a trunk is defined, it must be associated to a route.</span><span class="sxs-lookup"><span data-stu-id="2e46b-113">When a trunk is defined, it must be associated to a route.</span></span> <span data-ttu-id="2e46b-114">Чтобы связать магистраль с маршрутом, вы определяете простое имя для магистрали в построителе топологии.</span><span class="sxs-lookup"><span data-stu-id="2e46b-114">To associate a trunk to a route, you define a simple name for the trunk in Topology Builder.</span></span> <span data-ttu-id="2e46b-115">Это простое имя используется в качестве наименования канала на панели управления Lync Server, где магистральные магистрали можно связывать с маршрутами.</span><span class="sxs-lookup"><span data-stu-id="2e46b-115">This simple name is used as the trunk name in the Lync Server Control Panel, where trunks can be associated with routes.</span></span> <span data-ttu-id="2e46b-116">Простое имя канала используется как имя шлюза в командной консоли Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="2e46b-116">The simple trunk name is used as the gateway name from the Lync Server Management Shell.</span></span>

    New-CsVoiceRoute -Identity <RouteId> -NumberPattern <String> -PstnUsages @{add="<UsageString>"} -PstnGatewayList @{add="<TrunkSimpleName>"}

<span data-ttu-id="2e46b-117">Администратор должен выбрать магистраль по умолчанию, связанный с сервером-посредником.</span><span class="sxs-lookup"><span data-stu-id="2e46b-117">The administrator must select a default trunk associated with a Mediation Server.</span></span> <span data-ttu-id="2e46b-118">В построителе топологии щелкните правой кнопкой мыши соответствующий сервер-посредник и выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="2e46b-118">From the Topology Builder, right-click the associated Mediation Server, and then click **Properties**.</span></span> <span data-ttu-id="2e46b-119">Укажите шлюз по умолчанию для сервера обновлений.</span><span class="sxs-lookup"><span data-stu-id="2e46b-119">Specify the default gateway for the Mediation Server.</span></span>

<span data-ttu-id="2e46b-120">На следующей схеме показаны несколько магистральных каналов, определенных для каждого сервера и шлюза.</span><span class="sxs-lookup"><span data-stu-id="2e46b-120">The following diagram illustrates the multiple trunks that are defined for each Mediation Server and gateway.</span></span>

<span data-ttu-id="2e46b-121">**Маршрутизация магистральных каналов M-N**</span><span class="sxs-lookup"><span data-stu-id="2e46b-121">**M-N Trunk Routing**</span></span>

<span data-ttu-id="2e46b-122">![Назначения нескольких распределений каналов.](images/JJ205127.c61cd9a7-d8d9-4e02-83b9-ab62519a48c4(OCS.15).jpg "Назначения нескольких распределений каналов.")</span><span class="sxs-lookup"><span data-stu-id="2e46b-122">![Multiple trunk assignments.](images/JJ205127.c61cd9a7-d8d9-4e02-83b9-ab62519a48c4(OCS.15).jpg "Multiple trunk assignments.")</span></span>

<span data-ttu-id="2e46b-123"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2e46b-123"></div>

<span> </span>

</div>

</div>

</span></span></div>

