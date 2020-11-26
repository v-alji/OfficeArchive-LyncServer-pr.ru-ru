---
title: 'Lync Server 2013: таблица SessionCorrelation'
description: 'Таблица Lync Server 2013: CallPriorities.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: CallPriorities table
ms:assetid: 043b63ae-2d64-4f38-a0df-18aa08d6caf5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398093(v=OCS.15)
ms:contentKeyID: 48183275
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fe3cd1639921c63630e157744dbc8af22c50fac7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435644"
---
# <a name="callpriorities-table-in-lync-server-2013"></a><span data-ttu-id="faf41-103">Таблица SessionCorrelation в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="faf41-103">CallPriorities table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="faf41-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="faf41-104">

<span> </span></span></span>

<span data-ttu-id="faf41-105">_**Тема последнего изменения:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="faf41-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="faf41-106">Таблица CallPriorities — это статическая таблица, в которой хранится список возможных приоритетов звонков, например "экстренная", "срочно" или "Обычная".</span><span class="sxs-lookup"><span data-stu-id="faf41-106">The CallPriorities table is a static table that stores the list of possible call priorities, such as ‘emergency’, ‘urgent’, or ‘normal’.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="faf41-107">Столбец</span><span class="sxs-lookup"><span data-stu-id="faf41-107">Column</span></span></th>
<th><span data-ttu-id="faf41-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="faf41-108">Data Type</span></span></th>
<th><span data-ttu-id="faf41-109">Ключ/индекс</span><span class="sxs-lookup"><span data-stu-id="faf41-109">Key/Index</span></span></th>
<th><span data-ttu-id="faf41-110">Сведения</span><span class="sxs-lookup"><span data-stu-id="faf41-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="faf41-111"><strong>PriorityId</strong></span><span class="sxs-lookup"><span data-stu-id="faf41-111"><strong>PriorityId</strong></span></span></p></td>
<td><p><span data-ttu-id="faf41-112">tinyint</span><span class="sxs-lookup"><span data-stu-id="faf41-112">tinyint</span></span></p></td>
<td><p><span data-ttu-id="faf41-113">Primary</span><span class="sxs-lookup"><span data-stu-id="faf41-113">Primary</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faf41-114"><strong>Priority</strong></span><span class="sxs-lookup"><span data-stu-id="faf41-114"><strong>Priority</strong></span></span></p></td>
<td><p><span data-ttu-id="faf41-115">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="faf41-115">nvarchar(256)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="faf41-116">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="faf41-116">Allowed values:</span></span></p>
<ul>
<li><p><span data-ttu-id="faf41-117">0 — неизвестно</span><span class="sxs-lookup"><span data-stu-id="faf41-117">0 - Unknown</span></span></p></li>
<li><p><span data-ttu-id="faf41-118">1 — не срочно</span><span class="sxs-lookup"><span data-stu-id="faf41-118">1 – Non-Urgent</span></span></p></li>
<li><p><span data-ttu-id="faf41-119">2-обычный</span><span class="sxs-lookup"><span data-stu-id="faf41-119">2 - Normal</span></span></p></li>
<li><p><span data-ttu-id="faf41-120">3-Срочный</span><span class="sxs-lookup"><span data-stu-id="faf41-120">3 - Urgent</span></span></p></li>
<li><p><span data-ttu-id="faf41-121">4-экстренная ситуация</span><span class="sxs-lookup"><span data-stu-id="faf41-121">4 - Emergency</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table><span data-ttu-id="faf41-122">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="faf41-122">


</div>

<span> </span>

</div>

</div>

</span></span></div>

