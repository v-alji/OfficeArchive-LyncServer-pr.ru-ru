---
title: 'Lync Server 2013: необходимые ресурсы для сервера сохраняемого чата'
description: 'Lync Server 2013: необходимые ресурсы для сервера сохраняемого чата.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Required resources
ms:assetid: bce50b95-f3c8-407e-963a-d8896ee77fbc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205211(v=OCS.15)
ms:contentKeyID: 48185255
ms.date: 02/05/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 18c81f0017428e4305e46fbcf5580a83af38accf
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442706"
---
# <a name="required-resources-for-persistent-chat-server-in-lync-server-2013"></a><span data-ttu-id="fe119-103">Необходимые ресурсы для сервера сохраняемого чата в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fe119-103">Required resources for Persistent Chat Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fe119-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fe119-104">

<span> </span></span></span>

<span data-ttu-id="fe119-105">_**Тема последнего изменения:** 2016-02-05_</span><span class="sxs-lookup"><span data-stu-id="fe119-105">_**Topic Last Modified:** 2016-02-05_</span></span>

<span data-ttu-id="fe119-106">Для обеспечения высокой доступности и аварийного восстановления на сервере сохраняемого чата требуются дополнительные ресурсы, помимо тех, которые обычно требуются для выполнения полных операций.</span><span class="sxs-lookup"><span data-stu-id="fe119-106">High availability and disaster recovery for Persistent Chat Server requires additional resources beyond what is typically needed for full operation.</span></span> <span data-ttu-id="fe119-107">Прежде чем настраивать сохраняемый сервер чата для обеспечения высокой доступности и аварийного восстановления, убедитесь, что у вас есть указанные ниже ресурсы, а также возможности, необходимые для стандартной работы сервера сохраняемого чата.</span><span class="sxs-lookup"><span data-stu-id="fe119-107">Before configuring Persistent Chat Server for high availability and disaster recovery, ensure that you have the following resources in addition to what is required for standard Persistent Chat Server operation.</span></span> <span data-ttu-id="fe119-108">Дополнительные сведения о настройке можно найти [в разделе Настройка сервера сохраняемого чата в Lync server 2013](lync-server-2013-configuring-persistent-chat-server.md).</span><span class="sxs-lookup"><span data-stu-id="fe119-108">For additional configuration information, see [Configuring Persistent Chat Server in Lync Server 2013](lync-server-2013-configuring-persistent-chat-server.md).</span></span>

  - <span data-ttu-id="fe119-109">Один выделенный экземпляр базы данных, находящийся в том же физическом центре обработки данных, на котором находится домашняя страница службы сервера сохраняемого чата.</span><span class="sxs-lookup"><span data-stu-id="fe119-109">One dedicated database instance located in the same physical data center in which the home front end of the Persistent Chat Server service is located.</span></span> <span data-ttu-id="fe119-110">Эта база данных будет служить зеркалом SQL Server для основной сохраняемой базы данных чата.</span><span class="sxs-lookup"><span data-stu-id="fe119-110">This database will serve as the SQL Server mirror for the primary Persistent Chat database.</span></span> <span data-ttu-id="fe119-111">При необходимости назначьте дополнительный сервер SQL Server, который будет использоваться в качестве следящего сервера, если вы хотите автоматически отработка отказа в зеркальной базе данных.</span><span class="sxs-lookup"><span data-stu-id="fe119-111">Optionally, designate an additional SQL Server to serve as the mirroring witness if you want an automated failover to the mirror database.</span></span>

  - <span data-ttu-id="fe119-112">Один выделенный экземпляр базы данных, расположенный в другом физическом центре обработки данных.</span><span class="sxs-lookup"><span data-stu-id="fe119-112">One dedicated database instance located in the other physical data center.</span></span> <span data-ttu-id="fe119-113">Эта база данных будет служить базой данных сервера SQL Server для доставки журналов базы данных в основном центре обработки данных.</span><span class="sxs-lookup"><span data-stu-id="fe119-113">This database will serve as the SQL Server Log Shipping secondary database for the database in the primary data center.</span></span>

  - <span data-ttu-id="fe119-114">Один выделенный экземпляр базы данных, который будет служить зеркалом SQL Server для базы данных получателя.</span><span class="sxs-lookup"><span data-stu-id="fe119-114">One dedicated database instance to serve as the SQL Server mirror for the secondary database.</span></span> <span data-ttu-id="fe119-115">При необходимости назначьте дополнительный сервер SQL Server в качестве следящего сервера зеркального отображения.</span><span class="sxs-lookup"><span data-stu-id="fe119-115">Optionally, designate an additional SQL Server to server as the mirroring witness.</span></span> <span data-ttu-id="fe119-116">Обе базы данных должны быть расположены в том же физическом центре обработки данных, что и база данных-получатель.</span><span class="sxs-lookup"><span data-stu-id="fe119-116">Both of these must be located in the same physical data center as the secondary database.</span></span>

  - <span data-ttu-id="fe119-117">Если включено соответствие требованиям сервера сохраняемого чата, требуется дополнительно три выделенных экземпляра базы данных.</span><span class="sxs-lookup"><span data-stu-id="fe119-117">If Persistent Chat Server compliance is enabled, an additional three dedicated database instances are required.</span></span> <span data-ttu-id="fe119-118">Их распространение так же, как и для базы данных "сохраняемый чат".</span><span class="sxs-lookup"><span data-stu-id="fe119-118">Their distribution is the same as those previously outlined for the Persistent Chat database.</span></span> <span data-ttu-id="fe119-119">Несмотря на то, что база данных соответствия может использовать тот же экземпляр SQL Server, что и база данных сохраняемого чата, мы рекомендуем использовать отдельные экземпляры для обеспечения высокой доступности и аварийного восстановления.</span><span class="sxs-lookup"><span data-stu-id="fe119-119">While it is possible for the compliance database to share the same SQL Server instance as the Persistent Chat database, we recommend standalone instances for high availability and disaster recovery.</span></span>

  - <span data-ttu-id="fe119-120">Файловый общий доступ должен создаваться и назначаться для журналов транзакций по доставке журналов SQL Server.</span><span class="sxs-lookup"><span data-stu-id="fe119-120">A file share must be created and designated for the SQL Server Log Shipping transaction logs.</span></span> <span data-ttu-id="fe119-121">У всех серверов SQL в обоих центрах обработки данных, которые выполняют сохраняемые базы данных чата, должен быть доступ для чтения и записи в этой общей папке.</span><span class="sxs-lookup"><span data-stu-id="fe119-121">All SQL Servers in both data centers that run Persistent Chat databases must have read/write access to this file share.</span></span> <span data-ttu-id="fe119-122">This share is not defined as part of a FileStore role.</span><span class="sxs-lookup"><span data-stu-id="fe119-122">This share is not defined as part of a FileStore role.</span></span>

  - <span data-ttu-id="fe119-123">Файловый общий доступ на сервере-получателе, который будет использоваться в качестве целевой папки для журналов транзакций SQL Server, которые копируются из файлового общего сервера-источника.</span><span class="sxs-lookup"><span data-stu-id="fe119-123">A file share on the secondary database server to serve as the destination folder for the SQL Server transaction logs that are copied from the primary server file share.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="fe119-124">Активные серверы для работы с сохраняемым подключением в пуле сервера в постоянном чате должны находиться в том же часовом поясе, что и пул Lync следующего прыжка, определенный в топологии.</span><span class="sxs-lookup"><span data-stu-id="fe119-124">Active Persistent Chat servers in a Persistent Chat Server pool MUST reside in the same time zone as the next hop Lync Pool defined in the topology.</span></span>



</div>

<span data-ttu-id="fe119-125">На приведенных ниже рисунках приведены примеры того, как можно настроить весь пул серверов для постоянного чата в двух различных топологиях пула с растяжением.</span><span class="sxs-lookup"><span data-stu-id="fe119-125">The following figures provide examples about how the entire Persistent Chat Server pool can be configured in the two different stretched pool topologies:</span></span>

  - <span data-ttu-id="fe119-126">Пул серверов сохраняемого постоянного чата, когда центры обработки данных находятся на высоком уровне пропускной способности и малой задержке.</span><span class="sxs-lookup"><span data-stu-id="fe119-126">Stretched Persistent Chat Server pool when data centers are geo-located with high bandwidth/low latency.</span></span>

  - <span data-ttu-id="fe119-127">Пул серверов сохраняемого постоянного чата, когда центры обработки данных находятся в географической пропускной способности и большую задержку.</span><span class="sxs-lookup"><span data-stu-id="fe119-127">Stretched Persistent Chat Server pool when data centers are geo-located with low bandwidth/high latency.</span></span>

<span data-ttu-id="fe119-128">На приведенном ниже рисунке показана топология пула серверов сохраняемого постоянного чата, в которой центры обработки данных географически распределены с высокой пропускной способностью и низкой задержкой.</span><span class="sxs-lookup"><span data-stu-id="fe119-128">The following figure shows a stretched Persistent Chat Server pool topology where data centers are geo-located with high bandwidth/low latency.</span></span>

<span data-ttu-id="fe119-129">**Пул серверов сохраняемого постоянного чата, когда центры обработки данных находятся на высоком уровне пропускной способности и малой задержке.**</span><span class="sxs-lookup"><span data-stu-id="fe119-129">**Stretched Persistent Chat Server pool when data centers are geo-located with high bandwidth/low latency.**</span></span>

<span data-ttu-id="fe119-130">![Экзамен на конфигурацию HBW пула серверов для постоянного чата](images/JJ205211.55d10910-c824-41e6-bed2-08d13a2abd65(OCS.15).jpg "Экзамен на конфигурацию HBW пула серверов для постоянного чата")</span><span class="sxs-lookup"><span data-stu-id="fe119-130">![Persistent Chat Server pool HBW configuration exam](images/JJ205211.55d10910-c824-41e6-bed2-08d13a2abd65(OCS.15).jpg "Persistent Chat Server pool HBW configuration exam")</span></span>

<span data-ttu-id="fe119-131">На приведенном ниже рисунке показана топология пула серверов сохраняемого постоянного чата, в которой центры обработки данных находятся на низком уровне пропускной способности и большую задержку.</span><span class="sxs-lookup"><span data-stu-id="fe119-131">The following figure shows a stretched Persistent Chat Server pool topology where data centers are geo-located with low bandwidth/high latency.</span></span>

<span data-ttu-id="fe119-132">**Пул серверов сохраняемого постоянного чата, когда центры обработки данных находятся в географической пропускной способности и большую задержку.**</span><span class="sxs-lookup"><span data-stu-id="fe119-132">**Stretched Persistent Chat Server pool when data centers are geo-located with low bandwidth/high latency.**</span></span>

<span data-ttu-id="fe119-133">![Экзамен на конфигурацию LBW пула серверов для постоянного чата](images/JJ205211.586b0a3a-3767-4991-944f-ee54389512aa(OCS.15).jpg "Экзамен на конфигурацию LBW пула серверов для постоянного чата")</span><span class="sxs-lookup"><span data-stu-id="fe119-133">![Persistent Chat Server pool LBW configuration exam](images/JJ205211.586b0a3a-3767-4991-944f-ee54389512aa(OCS.15).jpg "Persistent Chat Server pool LBW configuration exam")</span></span>

<span data-ttu-id="fe119-134"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fe119-134"></div>

<span> </span>

</div>

</div>

</span></span></div>

