---
title: 'Lync Server 2013: новые функции'
description: Lync Server 2013 новые возможности.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: New server features
ms:assetid: 2e6f8a57-ab84-4578-b358-870796cddf31
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425795(v=OCS.15)
ms:contentKeyID: 48183722
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6731bc38b4c2a75f5ca564f92656e490945f709a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425047"
---
# <a name="new-features-in-lync-server-2013"></a><span data-ttu-id="6f535-103">Новые серверные функции в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6f535-103">New features in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6f535-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6f535-104">

<span> </span></span></span>

<span data-ttu-id="6f535-105">_**Тема последнего изменения:** 2012-10-04_</span><span class="sxs-lookup"><span data-stu-id="6f535-105">_**Topic Last Modified:** 2012-10-04_</span></span>

<span data-ttu-id="6f535-106">Lync Server 2013 предлагает множество новых функций, а также существенные улучшения в существующих функциях.</span><span class="sxs-lookup"><span data-stu-id="6f535-106">Lync Server 2013 introduces many new features, along with significant enhancements to existing functionality.</span></span> <span data-ttu-id="6f535-107">В этом разделе приводятся общие сведения о новых возможностях и улучшениях.</span><span class="sxs-lookup"><span data-stu-id="6f535-107">This section provides a high-level introduction to these new features and enhancements.</span></span>

<span data-ttu-id="6f535-108">Обсуждения новых функций в Lync Server 2013 группируются по темам, описанным в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="6f535-108">Discussions of new features in Lync Server 2013 are grouped among the topics in this section.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="6f535-109">Содержание</span><span class="sxs-lookup"><span data-stu-id="6f535-109">In This Section</span></span>

  - [<span data-ttu-id="6f535-110">Новые функции управления и администрирования в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6f535-110">New management and administration features in Lync Server 2013</span></span>](lync-server-2013-new-management-and-administration-features.md)

  - [<span data-ttu-id="6f535-111">Изменения топологии в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6f535-111">Topology changes in Lync Server 2013</span></span>](lync-server-2013-topology-changes.md)

  - [<span data-ttu-id="6f535-112">Новые возможности высокой доступности и аварийного восстановления в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6f535-112">New disaster recovery and high availability features in Lync Server 2013</span></span>](lync-server-2013-new-disaster-recovery-and-high-availability-features.md)

  - [<span data-ttu-id="6f535-113">Новые функции виртуализации в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6f535-113">New virtualization features in Lync Server 2013</span></span>](lync-server-2013-new-virtualization-features.md)

  - [<span data-ttu-id="6f535-114">Новые функции обмена мгновенными сообщениями и сведениями о присутствии в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6f535-114">New IM and presence features in Lync Server 2013</span></span>](lync-server-2013-new-im-and-presence-features.md)

  - [<span data-ttu-id="6f535-115">Новые возможности конференц-связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6f535-115">New conferencing features in Lync Server 2013</span></span>](lync-server-2013-new-conferencing-features.md)

  - [<span data-ttu-id="6f535-116">Новые функции для доступа внешних пользователей в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6f535-116">New features for external user access in Lync Server 2013</span></span>](lync-server-2013-new-features-for-external-user-access.md)

  - [<span data-ttu-id="6f535-117">Новые возможности корпоративной голосовой связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6f535-117">New Enterprise Voice features in Lync Server 2013</span></span>](lync-server-2013-new-enterprise-voice-features.md)

  - [<span data-ttu-id="6f535-118">Новые возможности мониторинга в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6f535-118">New Monitoring features in Lync Server 2013</span></span>](lync-server-2013-new-monitoring-features.md)

  - [<span data-ttu-id="6f535-119">Новые функции архивации в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6f535-119">New Archiving features in Lync Server 2013</span></span>](lync-server-2013-new-archiving-features.md)

  - [<span data-ttu-id="6f535-120">Новые возможности интеграции с Exchange Server в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6f535-120">New Exchange Server integration features in Lync Server 2013</span></span>](lync-server-2013-new-exchange-server-integration-features.md)

  - [<span data-ttu-id="6f535-121">Новые функции сервера сохраняемого чата в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6f535-121">New Persistent Chat Server features in Lync Server 2013</span></span>](lync-server-2013-new-persistent-chat-server-features.md)

  - [<span data-ttu-id="6f535-122">Новые возможности IPv6 в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6f535-122">New IPv6 features in Lync Server 2013</span></span>](lync-server-2013-new-ipv6-features.md)

  - [<span data-ttu-id="6f535-123">Новое единое хранилище контактов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6f535-123">New unified contact store feature in Lync Server 2013</span></span>](lync-server-2013-new-unified-contact-store-feature.md)

  - [<span data-ttu-id="6f535-124">Новые функции видео в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6f535-124">New video features in Lync Server 2013</span></span>](lync-server-2013-new-video-features.md)

<span data-ttu-id="6f535-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6f535-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

