---
title: 'Lync Server 2013: управление архивированием'
description: 'Lync Server 2013: Управление архивацией.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing Lync Server 2013 Archiving
ms:assetid: 48c6cc8c-c2c1-4534-9a8a-fd5eb738076a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520990(v=OCS.15)
ms:contentKeyID: 48184003
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9c7010645f36a7144ea508447d2c628bc8feacb0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425978"
---
# <a name="managing-lync-server-2013-archiving"></a><span data-ttu-id="e988c-103">Управление архивированием Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e988c-103">Managing Lync Server 2013 Archiving</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e988c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e988c-104">

<span> </span></span></span>

<span data-ttu-id="e988c-105">_**Тема последнего изменения:** 2012-10-10_</span><span class="sxs-lookup"><span data-stu-id="e988c-105">_**Topic Last Modified:** 2012-10-10_</span></span>

<span data-ttu-id="e988c-106">При развертывании архивации для организации вы указываете начальную конфигурацию во время развертывания.</span><span class="sxs-lookup"><span data-stu-id="e988c-106">When you deploy Archiving for your organization, you specify the initial configuration during deployment.</span></span> <span data-ttu-id="e988c-107">Тем не менее иногда требуется изменить способ реализации поддержки архивации для повседневного управления или для соблюдения новых требований в Организации.</span><span class="sxs-lookup"><span data-stu-id="e988c-107">However, there may be times when you want to change how you implement archiving support for day-to-day management or to meet new requirements in your organization.</span></span> <span data-ttu-id="e988c-108">Например, может потребоваться настройка поддержки архивации по-разному для определенного сайта, пула или пользователей в Организации.</span><span class="sxs-lookup"><span data-stu-id="e988c-108">For example, you may need to set up archiving support differently for a specific site, pool, or users within your organization.</span></span> <span data-ttu-id="e988c-109">Для пользователей, размещенных на Lync Server 2013, необходимо создать и настроить политики архивации и конфигурации.</span><span class="sxs-lookup"><span data-stu-id="e988c-109">For users homed on Lync Server 2013, you do this be creating and customizing archiving policies and configurations.</span></span> <span data-ttu-id="e988c-110">Если вы используете Microsoft Exchange Integration, необходимо также настроить параметры Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="e988c-110">If you use Microsoft Exchange integration, you must also configure Exchange 2013 settings.</span></span> <span data-ttu-id="e988c-111">В этом разделе приведены сведения и процедуры, которые позволят вам вносить изменения в развертывание архивирования.</span><span class="sxs-lookup"><span data-stu-id="e988c-111">This section provides information and procedures to enable you to make changes to your Archiving deployment.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="e988c-112">Содержание</span><span class="sxs-lookup"><span data-stu-id="e988c-112">In This Section</span></span>

  - [<span data-ttu-id="e988c-113">Как работает архивация в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e988c-113">How Archiving works in Lync Server 2013</span></span>](lync-server-2013-how-archiving-works.md)

  - [<span data-ttu-id="e988c-114">Управление архивированием внутренней и внешней связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e988c-114">Managing the Archiving of internal and external communications in Lync Server 2013</span></span>](lync-server-2013-managing-the-archiving-of-internal-and-external-communications.md)

  - [<span data-ttu-id="e988c-115">Управление параметрами конфигурации архивации в Lync Server 2013 для Организации, сайтов и пулов</span><span class="sxs-lookup"><span data-stu-id="e988c-115">Managing Archiving configuration options in Lync Server 2013 for your organization, sites, and pools</span></span>](lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md)

  - [<span data-ttu-id="e988c-116">Изменение параметров базы данных для архивации в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e988c-116">Changing Archiving database options in Lync Server 2013</span></span>](lync-server-2013-changing-archiving-database-options.md)

  - [<span data-ttu-id="e988c-117">Экспорт архивных данных из Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e988c-117">Exporting archived data from Lync Server 2013</span></span>](lync-server-2013-exporting-archived-data.md)

<span data-ttu-id="e988c-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e988c-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

