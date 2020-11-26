---
title: 'Lync Server 2013: таблица ConferenceJoinTimeThresholds'
description: 'Таблица Lync Server 2013: ConferenceJoinTimeThresholds.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ConferenceJoinTimeThresholds table
ms:assetid: 3944d724-bdd8-4d1c-a2af-933ee8141529
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204809(v=OCS.15)
ms:contentKeyID: 48183855
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5e38c8b99f444e16309882b6a8885d166fdceb9b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434461"
---
# <a name="conferencejointimethresholds-table-in-lync-server-2013"></a><span data-ttu-id="f22d3-103">Таблица ConferenceJoinTimeThresholds в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f22d3-103">ConferenceJoinTimeThresholds table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f22d3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f22d3-104">

<span> </span></span></span>

<span data-ttu-id="f22d3-105">_**Тема последнего изменения:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="f22d3-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="f22d3-106">В таблице ConferenceJoinTimeThresholds содержатся ограничители классификации, используемые в сводном отчете "время присоединения к Конференции".</span><span class="sxs-lookup"><span data-stu-id="f22d3-106">The ConferenceJoinTimeThresholds table contains the classification boundaries used by the Conference Join Time Summary Report.</span></span> <span data-ttu-id="f22d3-107">Сводный отчет о времени присоединения к Конференции суммирует количество времени, необходимого для успешного присоединения пользователей к Конференции; Эти значения времени выводятся как среднее значение и в одной из следующих категорий:</span><span class="sxs-lookup"><span data-stu-id="f22d3-107">The Conference Join Time Summary Report summarizes the amount time required for users to successfully join a conference; these time values are reported both as an average and in one of the following categories:</span></span>

  - <span data-ttu-id="f22d3-108">Менее 2 секунд.</span><span class="sxs-lookup"><span data-stu-id="f22d3-108">Less than 2 seconds.</span></span>

  - <span data-ttu-id="f22d3-109">От 2 секунды до 5 секунд.</span><span class="sxs-lookup"><span data-stu-id="f22d3-109">Between 2 second and 5 seconds.</span></span>

  - <span data-ttu-id="f22d3-110">От 5 секунд до 10 секунд.</span><span class="sxs-lookup"><span data-stu-id="f22d3-110">Between 5 seconds and 10 seconds.</span></span>

  - <span data-ttu-id="f22d3-111">Более 10 секунд.</span><span class="sxs-lookup"><span data-stu-id="f22d3-111">More than 10 seconds.</span></span>

<span data-ttu-id="f22d3-112">В таблице ConferenceJoinTimeThresholds содержатся значения классификации 2 секунды, 5 секунд и 10 секунд.</span><span class="sxs-lookup"><span data-stu-id="f22d3-112">The ConferenceJoinTimeThresholds table contains the classification values 2 seconds, 5 seconds, and 10 seconds.</span></span>

<span data-ttu-id="f22d3-113">Эта таблица введена в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f22d3-113">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f22d3-114">Столбец</span><span class="sxs-lookup"><span data-stu-id="f22d3-114">Column</span></span></th>
<th><span data-ttu-id="f22d3-115">Тип данных</span><span class="sxs-lookup"><span data-stu-id="f22d3-115">Data Type</span></span></th>
<th><span data-ttu-id="f22d3-116">Ключ/индекс</span><span class="sxs-lookup"><span data-stu-id="f22d3-116">Key/Index</span></span></th>
<th><span data-ttu-id="f22d3-117">Сведения</span><span class="sxs-lookup"><span data-stu-id="f22d3-117">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f22d3-118"><strong>ThresholdId</strong></span><span class="sxs-lookup"><span data-stu-id="f22d3-118"><strong>ThresholdId</strong></span></span></p></td>
<td><p><span data-ttu-id="f22d3-119">целое</span><span class="sxs-lookup"><span data-stu-id="f22d3-119">int</span></span></p></td>
<td><p><span data-ttu-id="f22d3-120">Primary</span><span class="sxs-lookup"><span data-stu-id="f22d3-120">Primary</span></span></p></td>
<td><p><span data-ttu-id="f22d3-121">Уникальный идентификатор для классификации.</span><span class="sxs-lookup"><span data-stu-id="f22d3-121">Unique identifier for the classification.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f22d3-122"><strong>ThresholdValue</strong></span><span class="sxs-lookup"><span data-stu-id="f22d3-122"><strong>ThresholdValue</strong></span></span></p></td>
<td><p><span data-ttu-id="f22d3-123">целое</span><span class="sxs-lookup"><span data-stu-id="f22d3-123">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="f22d3-124">Верхний предел для классификации.</span><span class="sxs-lookup"><span data-stu-id="f22d3-124">Upper limit for the classification.</span></span> <span data-ttu-id="f22d3-125">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="f22d3-125">Allowed values are:</span></span></p>
<ol>
<li><p><span data-ttu-id="f22d3-126">2</span><span class="sxs-lookup"><span data-stu-id="f22d3-126">2</span></span></p></li>
<li><p><span data-ttu-id="f22d3-127">5</span><span class="sxs-lookup"><span data-stu-id="f22d3-127">5</span></span></p></li>
<li><p><span data-ttu-id="f22d3-128">5-10</span><span class="sxs-lookup"><span data-stu-id="f22d3-128">10</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table><span data-ttu-id="f22d3-129">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f22d3-129">


</div>

<span> </span>

</div>

</div>

</span></span></div>

