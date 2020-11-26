---
title: 'Lync Server 2013: таблица Endpoint'
description: 'Lync Server 2013: таблица Endpoint.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Endpoint table
ms:assetid: 500f330d-4d7d-4e88-b1cc-fef9a9de6b5c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398327(v=OCS.15)
ms:contentKeyID: 48184098
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 614872eee41b5d8e56da4b96cf5bbe3a4a1cf4d2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428680"
---
# <a name="endpoint-table-in-lync-server-2013"></a><span data-ttu-id="408c0-103">Таблица Endpoint в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="408c0-103">Endpoint table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="408c0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="408c0-104">

<span> </span></span></span>

<span data-ttu-id="408c0-105">_**Тема последнего изменения:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="408c0-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="408c0-106">Таблица конечных точек — это вспомогательная таблица, в которой хранятся сведения о конечных точках, участвующих в сеансах, записанных в базе данных.</span><span class="sxs-lookup"><span data-stu-id="408c0-106">The Endpoint table is a supporting table that stores information about the endpoints that have participated in sessions recorded in the database.</span></span> <span data-ttu-id="408c0-107">Каждая запись в таблице представляет одну конечную точку.</span><span class="sxs-lookup"><span data-stu-id="408c0-107">Each record in the table represents one endpoint.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="408c0-108"><strong>Столбец</strong></span><span class="sxs-lookup"><span data-stu-id="408c0-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="408c0-109"><strong>Тип данных</strong></span><span class="sxs-lookup"><span data-stu-id="408c0-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="408c0-110"><strong>Ключ/индекс</strong></span><span class="sxs-lookup"><span data-stu-id="408c0-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="408c0-111"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="408c0-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="408c0-112"><strong>EndpointKey</strong></span><span class="sxs-lookup"><span data-stu-id="408c0-112"><strong>EndpointKey</strong></span></span></p></td>
<td><p><span data-ttu-id="408c0-113">целое</span><span class="sxs-lookup"><span data-stu-id="408c0-113">int</span></span></p></td>
<td><p><span data-ttu-id="408c0-114">Primary</span><span class="sxs-lookup"><span data-stu-id="408c0-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="408c0-115">Уникальный номер, идентифицирующий эту конечную точку.</span><span class="sxs-lookup"><span data-stu-id="408c0-115">Unique number identifying this endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="408c0-116"><strong>Имя</strong></span><span class="sxs-lookup"><span data-stu-id="408c0-116"><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="408c0-117">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="408c0-117">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="408c0-118">Повторя</span><span class="sxs-lookup"><span data-stu-id="408c0-118">Unique</span></span></p></td>
<td><p><span data-ttu-id="408c0-119">Имя конечной точки.</span><span class="sxs-lookup"><span data-stu-id="408c0-119">Endpoint name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="408c0-120"><strong>OS</strong></span><span class="sxs-lookup"><span data-stu-id="408c0-120"><strong>OS</strong></span></span></p></td>
<td><p><span data-ttu-id="408c0-121">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="408c0-121">nvarchar(128)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="408c0-122">Операционная система (ОС) конечной точки.</span><span class="sxs-lookup"><span data-stu-id="408c0-122">Operating system (OS) of the endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="408c0-123"><strong>CPUName</strong></span><span class="sxs-lookup"><span data-stu-id="408c0-123"><strong>CPUName</strong></span></span></p></td>
<td><p><span data-ttu-id="408c0-124">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="408c0-124">nvarchar(128)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="408c0-125">Имя ЦП конечной точки.</span><span class="sxs-lookup"><span data-stu-id="408c0-125">CPU name of the endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="408c0-126"><strong>CPUNumberOfCores</strong></span><span class="sxs-lookup"><span data-stu-id="408c0-126"><strong>CPUNumberOfCores</strong></span></span></p></td>
<td><p><span data-ttu-id="408c0-127">smallint</span><span class="sxs-lookup"><span data-stu-id="408c0-127">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="408c0-128">Количество ядер ЦП конечной точки.</span><span class="sxs-lookup"><span data-stu-id="408c0-128">Number of CPU cores of the endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="408c0-129"><strong>CPUProcessorSpeed</strong></span><span class="sxs-lookup"><span data-stu-id="408c0-129"><strong>CPUProcessorSpeed</strong></span></span></p></td>
<td><p><span data-ttu-id="408c0-130">целое</span><span class="sxs-lookup"><span data-stu-id="408c0-130">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="408c0-131">Тактовая частота процессора для конечной точки.</span><span class="sxs-lookup"><span data-stu-id="408c0-131">CPU processor speed of the endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="408c0-132"><strong>VirtualizationFlag</strong></span><span class="sxs-lookup"><span data-stu-id="408c0-132"><strong>VirtualizationFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="408c0-133">tinyint</span><span class="sxs-lookup"><span data-stu-id="408c0-133">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="408c0-134">Битовый флаг, указывающий на то, что система работает в виртуализованной среде.</span><span class="sxs-lookup"><span data-stu-id="408c0-134">Bit flag that indicates if the system is running in a virtualized environment:</span></span></p>
<ul>
<li><p><span data-ttu-id="408c0-135">0x0000 — None (нет)</span><span class="sxs-lookup"><span data-stu-id="408c0-135">0x0000 – None</span></span></p></li>
<li><p><span data-ttu-id="408c0-136">0x0001 — HyperV</span><span class="sxs-lookup"><span data-stu-id="408c0-136">0x0001 – HyperV</span></span></p></li>
<li><p><span data-ttu-id="408c0-137">0x0002 — VMWare</span><span class="sxs-lookup"><span data-stu-id="408c0-137">0x0002 – VMWare</span></span></p></li>
<li><p><span data-ttu-id="408c0-138">0x0004 — Virtual PC</span><span class="sxs-lookup"><span data-stu-id="408c0-138">0x0004 – Virtual PC</span></span></p></li>
<li><p><span data-ttu-id="408c0-139">0x0008 – ПК с Xen</span><span class="sxs-lookup"><span data-stu-id="408c0-139">0x0008 – Xen PC</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table><span data-ttu-id="408c0-140">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="408c0-140">


</div>

<span> </span>

</div>

</div>

</span></span></div>

