---
title: 'Lync Server 2013: таблица Conference'
description: 'Lync Server 2013: таблица конференций.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Conference table
ms:assetid: 2a2c327c-4719-42dc-a3bb-6dbc0864d9af
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425762(v=OCS.15)
ms:contentKeyID: 48183700
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 565725b527399cb3be55c649dfd74d8bcb5f13a2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434468"
---
# <a name="conference-table-in-lync-server-2013"></a><span data-ttu-id="4bbed-103">Таблица Conference в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4bbed-103">Conference table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4bbed-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4bbed-104">

<span> </span></span></span>

<span data-ttu-id="4bbed-105">_**Тема последнего изменения:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="4bbed-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="4bbed-106">Таблица конференции — это вспомогательная таблица.</span><span class="sxs-lookup"><span data-stu-id="4bbed-106">The Conference table is a supporting table.</span></span> <span data-ttu-id="4bbed-107">Каждая запись представляет одну конференцию или одноранговый сеанс.</span><span class="sxs-lookup"><span data-stu-id="4bbed-107">Each record represents one conference or peer-to-peer session.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4bbed-108"><strong>Столбец</strong></span><span class="sxs-lookup"><span data-stu-id="4bbed-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="4bbed-109"><strong>Тип данных</strong></span><span class="sxs-lookup"><span data-stu-id="4bbed-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="4bbed-110"><strong>Ключ/индекс</strong></span><span class="sxs-lookup"><span data-stu-id="4bbed-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="4bbed-111"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="4bbed-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4bbed-112"><strong>ConferenceKey</strong></span><span class="sxs-lookup"><span data-stu-id="4bbed-112"><strong>ConferenceKey</strong></span></span></p></td>
<td><p><span data-ttu-id="4bbed-113">целое</span><span class="sxs-lookup"><span data-stu-id="4bbed-113">int</span></span></p></td>
<td><p><span data-ttu-id="4bbed-114">Primary</span><span class="sxs-lookup"><span data-stu-id="4bbed-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="4bbed-115">Уникальный номер, идентифицирующий эту запись конференции.</span><span class="sxs-lookup"><span data-stu-id="4bbed-115">Unique number identifying this conference record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bbed-116"><strong>ConfURI</strong></span><span class="sxs-lookup"><span data-stu-id="4bbed-116"><strong>ConfURI</strong></span></span></p></td>
<td><p><span data-ttu-id="4bbed-117">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="4bbed-117">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="4bbed-118">повторя</span><span class="sxs-lookup"><span data-stu-id="4bbed-118">unique</span></span></p></td>
<td><p><span data-ttu-id="4bbed-119">Универсальный код ресурса (URI) для Конференции, если это конференция, или DialogID, если это одноранговый сеанс.</span><span class="sxs-lookup"><span data-stu-id="4bbed-119">Conference URI if this is a conference, or DialogID if this is a peer-to-peer session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4bbed-120"><strong>Счет</strong></span><span class="sxs-lookup"><span data-stu-id="4bbed-120"><strong>Checksum</strong></span></span></p></td>
<td><p><span data-ttu-id="4bbed-121">целое</span><span class="sxs-lookup"><span data-stu-id="4bbed-121">int</span></span></p></td>
<td><p><span data-ttu-id="4bbed-122">индекса</span><span class="sxs-lookup"><span data-stu-id="4bbed-122">index</span></span></p></td>
<td><p><span data-ttu-id="4bbed-123">Контрольная сумма URI конференции.</span><span class="sxs-lookup"><span data-stu-id="4bbed-123">Checksum of the conference URI.</span></span> <span data-ttu-id="4bbed-124">Используется для внутренних целей.</span><span class="sxs-lookup"><span data-stu-id="4bbed-124">This is used internally.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bbed-125"><strong>NextUpdateTS</strong></span><span class="sxs-lookup"><span data-stu-id="4bbed-125"><strong>NextUpdateTS</strong></span></span></p></td>
<td><p><span data-ttu-id="4bbed-126">datetime</span><span class="sxs-lookup"><span data-stu-id="4bbed-126">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="4bbed-127">Только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="4bbed-127">For internal use only.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="4bbed-128">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4bbed-128">


</div>

<span> </span>

</div>

</div>

</span></span></div>

