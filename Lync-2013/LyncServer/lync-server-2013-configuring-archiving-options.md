---
title: 'Lync Server 2013: Настройка параметров архивации'
description: 'Lync Server 2013: Настройка параметров архивирования.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Archiving options
ms:assetid: b2f7f74d-e1ad-494e-9d46-5eb0efe5fb29
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205182(v=OCS.15)
ms:contentKeyID: 48185158
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 99d57f016d76f9ae6a538ef28663a4b4c965b0a6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433313"
---
# <a name="configuring-archiving-options-in-lync-server-2013"></a><span data-ttu-id="65495-103">Настройка параметров архивации в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="65495-103">Configuring Archiving options in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="65495-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="65495-104">

<span> </span></span></span>

<span data-ttu-id="65495-105">_**Тема последнего изменения:** 2012-10-10_</span><span class="sxs-lookup"><span data-stu-id="65495-105">_**Topic Last Modified:** 2012-10-10_</span></span>

<span data-ttu-id="65495-106">В панели управления Lync Server 2013 вы можете настроить способ реализации архивации с помощью конфигураций архивации.</span><span class="sxs-lookup"><span data-stu-id="65495-106">In Lync Server 2013 Control Panel, you use Archiving configurations to specify how archiving is implemented.</span></span> <span data-ttu-id="65495-107">К ним относятся следующие конфигурации архивации:</span><span class="sxs-lookup"><span data-stu-id="65495-107">This includes the following Archiving configurations:</span></span>

  - <span data-ttu-id="65495-108">Глобальная конфигурация, создаваемая по умолчанию при развертывании Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="65495-108">A global configuration that is created by default when you deploy Lync Server 2013.</span></span>

  - <span data-ttu-id="65495-109">Необязательные конфигурации уровня сайта и пула, которые можно создать и использовать для определения способа реализации архивации для конкретных сайтов или пулов.</span><span class="sxs-lookup"><span data-stu-id="65495-109">Optional site-level and pool-level configurations that you can create and use to specify how archiving is implemented for specific sites or pools.</span></span>

<span data-ttu-id="65495-110">Первоначально конфигурации архивации задаются при развертывании архивации, но вы можете изменить, добавить и удалить настройки после развертывания.</span><span class="sxs-lookup"><span data-stu-id="65495-110">You initially set up Archiving configurations when you deploy Archiving, but you can change, add, and delete configurations after deployment.</span></span> <span data-ttu-id="65495-111">В панели управления Lync Server 2013 можно использовать страницу **Конфигурация архивации** в группе **Архивация и мониторинг** для управления конфигурациями на глобальном уровне, уровне сайта и уровне пула.</span><span class="sxs-lookup"><span data-stu-id="65495-111">In Lync Server 2013 Control Panel, you can use the **Archiving Configuration** page of the **Archiving and Monitoring** group to manage configurations at the global level, site level, and pool level.</span></span> <span data-ttu-id="65495-112">Сведения о том, как работают конфигурации архивации, в том числе о параметрах, которые можно указать и в иерархии конфигураций архивации, описаны в разделе [Использование архивации в Lync Server 2013](lync-server-2013-how-archiving-works.md) в документации по планированию, документации по развертыванию или документации по операциям.</span><span class="sxs-lookup"><span data-stu-id="65495-112">For details about how Archiving configurations are implemented, including which options you can specify and the hierarchy of Archiving configurations, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) in the Planning documentation, Deployment documentation, or Operations documentation.</span></span> <span data-ttu-id="65495-113">Дополнительные сведения об управлении конфигурацией после развертывания можно найти в разделе [Управление параметрами конфигурации архивации в Lync Server 2013 для Организации, сайты и пулы](lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md) в документации по эксплуатации.</span><span class="sxs-lookup"><span data-stu-id="65495-113">For details about how to manage configurations after deployment, see [Managing Archiving configuration options in Lync Server 2013 for your organization, sites, and pools](lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md) in the Operations documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="65495-114">Чтобы использовать архивацию, необходимо настроить политики архивации, чтобы указать, следует ли включать архивирование для внутренней связи, для внешней связи или для пользователей, расположенных на Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="65495-114">To use archiving, you must configure Archiving policies to specify whether to enable archiving for internal communications, for external communications, or for both for users homed on Lync Server 2013.</span></span> <span data-ttu-id="65495-115">По умолчанию архивация не включена для внутренней и внешней связи.</span><span class="sxs-lookup"><span data-stu-id="65495-115">By default, archiving is not enabled for either internal or external communications.</span></span> <span data-ttu-id="65495-116">Перед включением архивации в любых политиках следует задать соответствующие конфигурации архивации для развертывания и (необязательно) для определенных сайтов и пулов, как описано в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="65495-116">Before enabling Archiving in any policies, you should specify the appropriate Archiving configurations for your deployment and, optionally, for specific sites and pools, as described in this section.</span></span> <span data-ttu-id="65495-117">Подробнее о том, как включить архивацию, можно найти <A href="lync-server-2013-configuring-and-assigning-archiving-policies.md">в разделе Настройка и назначение политик архивации в Lync Server 2013</A> в документации по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="65495-117">For details about enabling Archiving, see <A href="lync-server-2013-configuring-and-assigning-archiving-policies.md">Configuring and assigning Archiving policies in Lync Server 2013</A> in the Deployment documentation.</span></span><BR><span data-ttu-id="65495-118">Если вы не используете интеграцию Microsoft Exchange для всех пользователей в развертывании, необходимо настроить политики архивации, чтобы указать, следует ли включать архивирование для внутренней связи, для внешней связи или для обоих.</span><span class="sxs-lookup"><span data-stu-id="65495-118">If you do not use Microsoft Exchange integration for all users in your deployment, you must configure Archiving policies to specify whether to enable archiving for internal communications, for external communications, or for both.</span></span> <span data-ttu-id="65495-119">По умолчанию при использовании баз данных Lync Server 2013 для архивации данных архивация не поддерживает внутренние и внешние сообщения.</span><span class="sxs-lookup"><span data-stu-id="65495-119">By default, archiving is not enabled for either internal or external communications for archiving of data when using Lync Server 2013 Archiving databases.</span></span> <span data-ttu-id="65495-120">Перед включением архивации в любых политиках следует задать соответствующие конфигурации архивации для развертывания и (необязательно) для определенных сайтов и пулов, как описано в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="65495-120">Prior to enabling Archiving in any policies, you should specify the appropriate Archiving configurations for your deployment and, optionally, for specific sites and pools, as described in this section.</span></span> <span data-ttu-id="65495-121">Подробные сведения о том, как включить архивацию для баз данных Lync Server 2013, можно найти в разделе <A href="lync-server-2013-configuring-and-assigning-archiving-policies.md">Настройка и назначение политик архивации в Lync server 2013</A> в документации по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="65495-121">For details about enabling Archiving for use with Lync Server 2013 Archiving databases, see <A href="lync-server-2013-configuring-and-assigning-archiving-policies.md">Configuring and assigning Archiving policies in Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="65495-122">Содержание</span><span class="sxs-lookup"><span data-stu-id="65495-122">In This Section</span></span>

  - [<span data-ttu-id="65495-123">Настройка параметров архивации на глобальном уровне в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="65495-123">Configuring Archiving options at the global level in Lync Server 2013</span></span>](lync-server-2013-configuring-archiving-options-at-the-global-level.md)

  - [<span data-ttu-id="65495-124">Настройка параметров архивации для сайта в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="65495-124">Configuring Archiving options for a site in Lync Server 2013</span></span>](lync-server-2013-configuring-archiving-options-for-a-site.md)

  - [<span data-ttu-id="65495-125">Настройка параметров архивации для пула в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="65495-125">Configuring Archiving options for a pool in Lync Server 2013</span></span>](lync-server-2013-configuring-archiving-options-for-a-pool.md)

<span data-ttu-id="65495-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="65495-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

