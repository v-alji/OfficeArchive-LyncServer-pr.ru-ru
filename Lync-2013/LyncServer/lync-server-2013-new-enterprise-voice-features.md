---
title: 'Lync Server 2013: новые возможности корпоративной голосовой связи'
description: 'Lync Server 2013: новые возможности корпоративного голосовой связи.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: New Enterprise Voice features
ms:assetid: db0ad7b9-e469-4c29-89d9-52fed018ef08
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398964(v=OCS.15)
ms:contentKeyID: 48185591
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e1fc0c0970fe22fb6a56eaf0d950f1d49d210826
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445423"
---
# <a name="new-enterprise-voice-features-in-lync-server-2013"></a><span data-ttu-id="088cf-103">Новые возможности корпоративной голосовой связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="088cf-103">New Enterprise Voice features in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="088cf-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="088cf-104">

<span> </span></span></span>

<span data-ttu-id="088cf-105">_**Тема последнего изменения:** 2013-05-01_</span><span class="sxs-lookup"><span data-stu-id="088cf-105">_**Topic Last Modified:** 2013-05-01_</span></span>

<span data-ttu-id="088cf-106">Lync Server 2013 предлагает несколько новых функций маршрутизации и управления звонками, повышающих эффективность работы с корпоративной голосовой связью.</span><span class="sxs-lookup"><span data-stu-id="088cf-106">Lync Server 2013 introduces several new routing and call management features that enhance Enterprise Voice.</span></span>

<span data-ttu-id="088cf-107">Lync Server 2013 поддерживает несколько каналов связи между серверами и шлюзами обновлений.</span><span class="sxs-lookup"><span data-stu-id="088cf-107">Lync Server 2013 supports multiple trunks between Mediation Servers and gateways.</span></span> <span data-ttu-id="088cf-108">*Магистраль* — это логическая связь между номером порта и сервером-посредником с номером порта и шлюзом.</span><span class="sxs-lookup"><span data-stu-id="088cf-108">A *trunk* is a logical association between a port number and Mediation Server with a port number and gateway.</span></span> <span data-ttu-id="088cf-109">Это означает, что сервер-посредник может иметь несколько магистральных каналов для разных шлюзов, и шлюз может иметь несколько магистральных каналов для разных серверов-исправлений.</span><span class="sxs-lookup"><span data-stu-id="088cf-109">This means that a Mediation Server can have multiple trunks to different gateways, and a gateway can have multiple trunks to different Mediation Servers.</span></span> <span data-ttu-id="088cf-110">Межсетевая маршрутизация позволяет Lync Server 2013 использовать IP-УАТС для связи с шлюзом КОММУТИРУЕМой телефонной сети или межсетевым подключением к нескольким системам IP-УАТС.</span><span class="sxs-lookup"><span data-stu-id="088cf-110">Intertrunk routing makes it possible for Lync Server 2013 to interconnect an IP-PBX to a public switched telephone network (PSTN) gateway or to interconnect multiple IP-PBX systems.</span></span> <span data-ttu-id="088cf-111">Lync Server 2013 является связующим (т. е. межсоединением) между различными системами телефонной связи.</span><span class="sxs-lookup"><span data-stu-id="088cf-111">Lync Server 2013 serves as the glue (that is, the interconnection) between different telephony systems.</span></span>

<span data-ttu-id="088cf-112">Microsoft Lync Server 2013 вносит улучшения в области переадресации звонков, одновременных звонков, обработки голосовой почты и презентации идентификации вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="088cf-112">Microsoft Lync Server 2013 makes improvements in the areas of call forwarding, simultaneous ringing, voice mail handling, and caller ID presentation.</span></span> <span data-ttu-id="088cf-113">Эти функции улучшают возможности корпоративного голосовой связи.</span><span class="sxs-lookup"><span data-stu-id="088cf-113">These features enrich the Enterprise Voice call experience.</span></span>

<span data-ttu-id="088cf-114">В Lync Server 2013 появились следующие усовершенствования, повышающие эффективность корпоративной голосовой связи:</span><span class="sxs-lookup"><span data-stu-id="088cf-114">Lync Server 2013 introduces the following new enhancements to Enterprise Voice:</span></span>

  - [<span data-ttu-id="088cf-115">Новые функции звонков в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="088cf-115">New call features in Lync Server 2013</span></span>](lync-server-2013-new-call-features.md)

  - [<span data-ttu-id="088cf-116">Новая функция АОН в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="088cf-116">New caller ID feature in Lync Server 2013</span></span>](lync-server-2013-new-caller-id-feature.md)

  - [<span data-ttu-id="088cf-117">Новая функция голосовой почты в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="088cf-117">New voice mail feature in Lync Server 2013</span></span>](lync-server-2013-new-voice-mail-feature.md)

  - [<span data-ttu-id="088cf-118">Новая функция магистрали в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="088cf-118">New trunk feature in Lync Server 2013</span></span>](lync-server-2013-new-trunk-feature.md)

  - [<span data-ttu-id="088cf-119">Новая функция промежуточной магистрали в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="088cf-119">New intertrunk feature in Lync Server 2013</span></span>](lync-server-2013-new-intertrunk-feature.md)

  - [<span data-ttu-id="088cf-120">Новые функции управления звонками в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="088cf-120">New call management features in Lync Server 2013</span></span>](lync-server-2013-new-call-management-features.md)

<span data-ttu-id="088cf-121"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="088cf-121"></div>

<span> </span>

</div>

</div>

</span></span></div>

