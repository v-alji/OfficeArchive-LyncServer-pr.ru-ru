---
title: 'Lync Server 2013: таблица ErrorCategory'
description: 'Таблица Lync Server 2013: ErrorCategory.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ErrorCategory table
ms:assetid: 0fde3b73-9a2f-44dd-b8dc-6df512303ff1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204675(v=OCS.15)
ms:contentKeyID: 48183425
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8154c73f33b5dad62a338335a960553cfc06ec13
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428568"
---
# <a name="errorcategory-table-in-lync-server-2013"></a><span data-ttu-id="ea40a-103">Таблица ErrorCategory в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ea40a-103">ErrorCategory table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ea40a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ea40a-104">

<span> </span></span></span>

<span data-ttu-id="ea40a-105">_**Тема последнего изменения:** 2012-08-20_</span><span class="sxs-lookup"><span data-stu-id="ea40a-105">_**Topic Last Modified:** 2012-08-20_</span></span>

<span data-ttu-id="ea40a-106">В таблице ErrorCategory содержится понятное имя для каждого диагностического классификация Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ea40a-106">The ErrorCategory table contains the friendly name for each Microsoft Lync Server 2013 diagnostic classification.</span></span> <span data-ttu-id="ea40a-107">По умолчанию Lync Server 2013 использует следующие классификации:</span><span class="sxs-lookup"><span data-stu-id="ea40a-107">By default, Lync Server 2013 uses the following classifications:</span></span>

  - <span data-ttu-id="ea40a-108">0 — успех</span><span class="sxs-lookup"><span data-stu-id="ea40a-108">0 -- Success</span></span>

  - <span data-ttu-id="ea40a-109">1 — ожидаемый сбой</span><span class="sxs-lookup"><span data-stu-id="ea40a-109">1 -- Expected failure</span></span>

  - <span data-ttu-id="ea40a-110">2 — непредвиденный сбой</span><span class="sxs-lookup"><span data-stu-id="ea40a-110">2 – Unexpected failure</span></span>

<span data-ttu-id="ea40a-111">Эта таблица введена в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ea40a-111">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ea40a-112">Столбец</span><span class="sxs-lookup"><span data-stu-id="ea40a-112">Column</span></span></th>
<th><span data-ttu-id="ea40a-113">Тип данных</span><span class="sxs-lookup"><span data-stu-id="ea40a-113">Data Type</span></span></th>
<th><span data-ttu-id="ea40a-114">Ключ/индекс</span><span class="sxs-lookup"><span data-stu-id="ea40a-114">Key/Index</span></span></th>
<th><span data-ttu-id="ea40a-115">Сведения</span><span class="sxs-lookup"><span data-stu-id="ea40a-115">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ea40a-116"><strong>КодТипа</strong></span><span class="sxs-lookup"><span data-stu-id="ea40a-116"><strong>CategoryId</strong></span></span></p></td>
<td><p><span data-ttu-id="ea40a-117">tinyint</span><span class="sxs-lookup"><span data-stu-id="ea40a-117">tinyint</span></span></p></td>
<td><p><span data-ttu-id="ea40a-118">Primary</span><span class="sxs-lookup"><span data-stu-id="ea40a-118">Primary</span></span></p></td>
<td><p><span data-ttu-id="ea40a-119">Уникальный идентификатор для классификации.</span><span class="sxs-lookup"><span data-stu-id="ea40a-119">Unique identifier for the classification.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea40a-120"><strong>Имя</strong></span><span class="sxs-lookup"><span data-stu-id="ea40a-120"><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="ea40a-121">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="ea40a-121">nvarchar(256)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ea40a-122">Значение и понятное имя, присвоенное классификации.</span><span class="sxs-lookup"><span data-stu-id="ea40a-122">Value and friendly name assigned to the classification.</span></span> <span data-ttu-id="ea40a-123">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="ea40a-123">Allowed values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="ea40a-124">0 — успех</span><span class="sxs-lookup"><span data-stu-id="ea40a-124">0 -- Success</span></span></p></li>
<li><p><span data-ttu-id="ea40a-125">1 — ожидаемый сбой</span><span class="sxs-lookup"><span data-stu-id="ea40a-125">1 -- Expected failure</span></span></p></li>
<li><p><span data-ttu-id="ea40a-126">2 — непредвиденный сбой</span><span class="sxs-lookup"><span data-stu-id="ea40a-126">2 – Unexpected failure</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table><span data-ttu-id="ea40a-127">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ea40a-127">


</div>

<span> </span>

</div>

</div>

</span></span></div>

