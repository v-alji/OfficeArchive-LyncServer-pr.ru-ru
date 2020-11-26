---
title: 'Lync Server 2013: Настройка поддержки архивации'
description: 'Lync Server 2013: Настройка поддержки архивации.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring support for Archiving
ms:assetid: 579283fe-909c-46f2-a0c9-52ca1e7d63d8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204905(v=OCS.15)
ms:contentKeyID: 48184187
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4209614ed1248ab0caf3cf438a922d569ba79630
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432634"
---
# <a name="configuring-support-for-archiving-in-lync-server-2013"></a><span data-ttu-id="9369e-103">Настройка поддержки архивации в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9369e-103">Configuring support for Archiving in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9369e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9369e-104">

<span> </span></span></span>

<span data-ttu-id="9369e-105">_**Тема последнего изменения:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="9369e-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="9369e-106">После добавления архивации в топологию и публикации новой топологии необходимо настроить параметры первоначальной реализации архивации в развертывании, а затем настроить одну или несколько политик архивации для включения архивирования для развертывания и, при необходимости, для определенных сайтов и пользователей.</span><span class="sxs-lookup"><span data-stu-id="9369e-106">After adding Archiving to your topology and publishing the new topology, you need to configure options for how Archiving is initially implemented in your deployment, and then configure one or more Archiving policies to enable Archiving for your deployment and, optionally, for specific sites and users.</span></span> <span data-ttu-id="9369e-107">Это можно сделать с помощью панели управления Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="9369e-107">You can use Lync Server 2013 Control Panel to do this.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="9369e-108">После развертывания вы можете изменить параметры архивации, чтобы отключить или включить архивацию.</span><span class="sxs-lookup"><span data-stu-id="9369e-108">After deployment, you can change Archiving settings to disable or enable Archiving.</span></span> <span data-ttu-id="9369e-109">Подробнее о том, как реализовать поддержку архивации для повседневного управления или для соблюдения новых требований в вашей организации после развертывания, вы можете найти в разделе <A href="lync-server-2013-managing-archiving.md">Управление архивацией Lync Server 2013</A> в документации по эксплуатации.</span><span class="sxs-lookup"><span data-stu-id="9369e-109">For details about how to implement archiving support for day-to-day management or to meet new requirements in your organization after deployment, see <A href="lync-server-2013-managing-archiving.md">Managing Lync Server 2013 Archiving</A> in the Operations documentation.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="9369e-110">Содержание</span><span class="sxs-lookup"><span data-stu-id="9369e-110">In This Section</span></span>

  - [<span data-ttu-id="9369e-111">Настройка параметров архивации в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9369e-111">Configuring Archiving options in Lync Server 2013</span></span>](lync-server-2013-configuring-archiving-options.md)

  - [<span data-ttu-id="9369e-112">Настройка и назначение политик архивации в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9369e-112">Configuring and assigning Archiving policies in Lync Server 2013</span></span>](lync-server-2013-configuring-and-assigning-archiving-policies.md)

  - [<span data-ttu-id="9369e-113">Включение и отключение отправки отказа от архивирования федеративным партнерам в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9369e-113">Enable or disable sending an Archiving disclaimer to federated partners in Lync Server 2013</span></span>](lync-server-2013-enable-or-disable-sending-an-archiving-disclaimer-to-federated-partners.md)

<span data-ttu-id="9369e-114"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9369e-114"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

