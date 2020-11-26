---
title: 'Lync Server 2013: планирование мониторинга'
description: 'Lync Server 2013: Планирование мониторинга.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for monitoring
ms:assetid: 26cead5a-183c-42f1-a4b0-0e8d61c6159d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204752(v=OCS.15)
ms:contentKeyID: 48183671
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f8ee78f06423bc167e26455d399ce2dd16f24262
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442931"
---
# <a name="planning-for-monitoring-in-lync-server-2013"></a><span data-ttu-id="7a28e-103">Планирование мониторинга в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7a28e-103">Planning for monitoring in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7a28e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7a28e-104">

<span> </span></span></span>

<span data-ttu-id="7a28e-105">_**Тема последнего изменения:** 2012-09-05_</span><span class="sxs-lookup"><span data-stu-id="7a28e-105">_**Topic Last Modified:** 2012-09-05_</span></span>

<span data-ttu-id="7a28e-106">Служба мониторинга в Microsoft Lync Server 2013 предоставляет администраторам способ сбора данных об использовании, тенденциях и качества обслуживания для сеансов связи, выполняемых в своей организации.</span><span class="sxs-lookup"><span data-stu-id="7a28e-106">The monitoring service in Microsoft Lync Server 2013 provides a way for administrators to collect usage, trend, and quality of service data for the communication sessions that take place in their organization.</span></span> <span data-ttu-id="7a28e-107">Для наблюдения в Lync Server 2013 больше не требуется отдельная серверная роль; Вместо этого служба мониторинга встроена в каждый сервер переднего плана.</span><span class="sxs-lookup"><span data-stu-id="7a28e-107">Monitoring in Lync Server 2013 no longer requires a separate server role; instead, the monitoring service is built into each Front End server.</span></span> <span data-ttu-id="7a28e-108">Однако наблюдение по умолчанию не включено в Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="7a28e-108">However, by default monitoring is not enabled in Lync Server 2013.</span></span> <span data-ttu-id="7a28e-109">Этот документ поможет вам определить, следует ли включить мониторинг в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="7a28e-109">This document will help you determine whether or not monitoring should be enabled in your organization.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="7a28e-110">Содержание</span><span class="sxs-lookup"><span data-stu-id="7a28e-110">In This Section</span></span>

  - [<span data-ttu-id="7a28e-111">Общие сведения об отслеживании в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7a28e-111">Overview of monitoring in Lync Server 2013</span></span>](lync-server-2013-overview-of-monitoring.md)

  - [<span data-ttu-id="7a28e-112">Определение требований к мониторингу в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7a28e-112">Defining your requirements for monitoring in Lync Server 2013</span></span>](lync-server-2013-defining-your-requirements-for-monitoring.md)

  - [<span data-ttu-id="7a28e-113">Включение мониторинга в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7a28e-113">Enabling monitoring in Lync Server 2013</span></span>](lync-server-2013-enabling-monitoring.md)

  - [<span data-ttu-id="7a28e-114">Доступ к данным мониторинга в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7a28e-114">Accessing monitoring data in Lync Server 2013</span></span>](lync-server-2013-accessing-monitoring-data.md)

  - [<span data-ttu-id="7a28e-115">Компоненты и топологии для мониторинга в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7a28e-115">Components and topologies for monitoring in Lync Server 2013</span></span>](lync-server-2013-components-and-topologies-for-monitoring.md)

  - [<span data-ttu-id="7a28e-116">Развертывание контрольного списка для мониторинга в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7a28e-116">Deployment checklist for monitoring in Lync Server 2013</span></span>](lync-server-2013-deployment-checklist-for-monitoring.md)

<span data-ttu-id="7a28e-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7a28e-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

