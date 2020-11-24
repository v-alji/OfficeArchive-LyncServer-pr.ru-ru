---
title: Использование построителя топологий для настройки высокой доступности и аварийного восстановления
description: Использование построителя топологии для настройки высокой доступности и аварийного восстановления.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Using Topology Builder to configure high availability and disaster recovery
ms:assetid: abc1a25d-1f5e-46ef-91d2-0144fc847206
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205172(v=OCS.15)
ms:contentKeyID: 48185113
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 04764a58ac3ae1bbe0df97aadeabb03158ce8100
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49400117"
---
# <a name="using-topology-builder-to-configure-high-availability-and-disaster-recovery-in-lync-server-2013"></a><span data-ttu-id="b299e-103">Использование построителя топологий для настройки высокой доступности и аварийного восстановления в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b299e-103">Using Topology Builder to configure high availability and disaster recovery in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b299e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b299e-104">

<span> </span></span></span>

<span data-ttu-id="b299e-105">_**Тема последнего изменения:** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="b299e-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="b299e-106">Выполните указанные ниже действия в построителе топологии для настройки высокой доступности и аварийного восстановления для постоянного сервера чата.</span><span class="sxs-lookup"><span data-stu-id="b299e-106">Perform the following steps within Topology Builder to configure high availability and disaster recovery for Persistent Chat Server.</span></span>

1.  <span data-ttu-id="b299e-107">Добавьте зеркальные базы данных и хранилище журналов SQL Server, которые являются получателями.</span><span class="sxs-lookup"><span data-stu-id="b299e-107">Add the mirror databases and the log shipping secondary database SQL Server stores.</span></span>

2.  <span data-ttu-id="b299e-108">Измените параметры службы сервера для сохраняемого чата следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b299e-108">Edit the Persistent Chat Server service properties to:</span></span>
    
    1.  <span data-ttu-id="b299e-109">Включите зеркальное отображение для базы данных-источника.</span><span class="sxs-lookup"><span data-stu-id="b299e-109">Enable mirroring for the primary database.</span></span>
    
    2.  <span data-ttu-id="b299e-110">Добавьте основное зеркальное хранилище SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b299e-110">Add the primary mirror SQL Server store.</span></span>
    
    3.  <span data-ttu-id="b299e-111">Включите базу данных доставки журналов SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b299e-111">Enable the SQL Server Log Shipping database.</span></span>
    
    4.  <span data-ttu-id="b299e-112">Добавьте хранилище журналов SQL Server с дополнительной доставкой.</span><span class="sxs-lookup"><span data-stu-id="b299e-112">Add the SQL Server Log Shipping secondary SQL Server store.</span></span>
    
    5.  <span data-ttu-id="b299e-113">Добавьте зеркало хранилища SQL Server для базы данных получателя.</span><span class="sxs-lookup"><span data-stu-id="b299e-113">Add the SQL Server store mirror for the secondary database.</span></span>
    
    6.  <span data-ttu-id="b299e-114">Опубликуйте топологию.</span><span class="sxs-lookup"><span data-stu-id="b299e-114">Publish the topology.</span></span>

<span data-ttu-id="b299e-115"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b299e-115"></div>

<span> </span>

</div>

</div>

</span></span></div>

