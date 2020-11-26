---
title: 'Lync Server 2013: таблица Server'
description: 'Серверная таблица Lync Server 2013: Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Server table
ms:assetid: 9af89d08-d35a-48e8-b56d-6df292f973cc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398801(v=OCS.15)
ms:contentKeyID: 48184890
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 00990a91aec64063480d96a16380171990913ad4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441853"
---
# <a name="server-table-in-lync-server-2013"></a><span data-ttu-id="4b8dc-103">Таблица Server в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4b8dc-103">Server table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4b8dc-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4b8dc-104">

<span> </span></span></span>

<span data-ttu-id="4b8dc-105">_**Тема последнего изменения:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="4b8dc-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="4b8dc-106">Серверная таблица является вспомогательной таблицей.</span><span class="sxs-lookup"><span data-stu-id="4b8dc-106">The Server table is a supporting table.</span></span> <span data-ttu-id="4b8dc-107">Каждая запись представляет один сервер.</span><span class="sxs-lookup"><span data-stu-id="4b8dc-107">Each record represents one server.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4b8dc-108"><strong>Столбец</strong></span><span class="sxs-lookup"><span data-stu-id="4b8dc-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="4b8dc-109"><strong>Тип данных</strong></span><span class="sxs-lookup"><span data-stu-id="4b8dc-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="4b8dc-110"><strong>Ключ/индекс</strong></span><span class="sxs-lookup"><span data-stu-id="4b8dc-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="4b8dc-111"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="4b8dc-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4b8dc-112"><strong>ServerKey</strong></span><span class="sxs-lookup"><span data-stu-id="4b8dc-112"><strong>ServerKey</strong></span></span></p></td>
<td><p><span data-ttu-id="4b8dc-113">целое</span><span class="sxs-lookup"><span data-stu-id="4b8dc-113">int</span></span></p></td>
<td><p><span data-ttu-id="4b8dc-114">Primary</span><span class="sxs-lookup"><span data-stu-id="4b8dc-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="4b8dc-115">Уникальный номер, идентифицирующий сервер.</span><span class="sxs-lookup"><span data-stu-id="4b8dc-115">Unique number identifying the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b8dc-116"><strong>FQDNOrIP</strong></span><span class="sxs-lookup"><span data-stu-id="4b8dc-116"><strong>FQDNOrIP</strong></span></span></p></td>
<td><p><span data-ttu-id="4b8dc-117">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="4b8dc-117">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="4b8dc-118">индекса</span><span class="sxs-lookup"><span data-stu-id="4b8dc-118">index</span></span></p></td>
<td><p><span data-ttu-id="4b8dc-119">Строка MAC-адреса.</span><span class="sxs-lookup"><span data-stu-id="4b8dc-119">MAC address string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b8dc-120"><strong>ServerType</strong></span><span class="sxs-lookup"><span data-stu-id="4b8dc-120"><strong>ServerType</strong></span></span></p></td>
<td><p><span data-ttu-id="4b8dc-121">целое</span><span class="sxs-lookup"><span data-stu-id="4b8dc-121">int</span></span></p></td>
<td><p><span data-ttu-id="4b8dc-122">Другом</span><span class="sxs-lookup"><span data-stu-id="4b8dc-122">Foreign</span></span></p></td>
<td><p><span data-ttu-id="4b8dc-123">1: сервер исправлений</span><span class="sxs-lookup"><span data-stu-id="4b8dc-123">1: Mediation Server</span></span></p>
<p><span data-ttu-id="4b8dc-124">2: Server16394 конференции/V-service32769: шлюз</span><span class="sxs-lookup"><span data-stu-id="4b8dc-124">2: A/V Conferencing Server16394: A/V Edge service32769: Gateway</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b8dc-125"><strong>PoolName</strong></span><span class="sxs-lookup"><span data-stu-id="4b8dc-125"><strong>PoolName</strong></span></span></p></td>
<td><p><span data-ttu-id="4b8dc-126">nvarchar (512)</span><span class="sxs-lookup"><span data-stu-id="4b8dc-126">nvarchar(512)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="4b8dc-127">Группа, к которой принадлежит сервер.</span><span class="sxs-lookup"><span data-stu-id="4b8dc-127">Pool the server belongs to.</span></span> <span data-ttu-id="4b8dc-128">Применимо только для сервера конференц-связи A/V.</span><span class="sxs-lookup"><span data-stu-id="4b8dc-128">Only applicable for the A/V Conferencing Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b8dc-129"><strong>NextUpdateTS</strong></span><span class="sxs-lookup"><span data-stu-id="4b8dc-129"><strong>NextUpdateTS</strong></span></span></p></td>
<td><p><span data-ttu-id="4b8dc-130">datetime</span><span class="sxs-lookup"><span data-stu-id="4b8dc-130">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="4b8dc-131">Только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="4b8dc-131">For internal use only.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="4b8dc-132">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4b8dc-132">


</div>

<span> </span>

</div>

</div>

</span></span></div>

