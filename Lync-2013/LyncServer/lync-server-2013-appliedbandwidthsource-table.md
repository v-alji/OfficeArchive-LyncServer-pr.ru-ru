---
title: 'Lync Server 2013: таблица AppliedBandwidthSource'
description: 'Таблица Lync Server 2013: AppliedBandwidthSource.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: AppliedBandwidthSource table
ms:assetid: 24fb3caf-19b3-4c0a-90d7-ca5d53de32ad
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425725(v=OCS.15)
ms:contentKeyID: 48183638
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3dc22d3a978a99cb13317e2a32fdb65382ce106c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440600"
---
# <a name="appliedbandwidthsource-table-in-lync-server-2013"></a><span data-ttu-id="b7fbf-103">Таблица AppliedBandwidthSource в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b7fbf-103">AppliedBandwidthSource table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b7fbf-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b7fbf-104">

<span> </span></span></span>

<span data-ttu-id="b7fbf-105">_**Тема последнего изменения:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="b7fbf-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="b7fbf-106">Таблица AppliedBandwidthSource является вспомогательной таблицей.</span><span class="sxs-lookup"><span data-stu-id="b7fbf-106">The AppliedBandwidthSource table is a supporting table.</span></span> <span data-ttu-id="b7fbf-107">Каждая запись представляет один источник.</span><span class="sxs-lookup"><span data-stu-id="b7fbf-107">Each record represents one source.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b7fbf-108"><strong>Столбец</strong></span><span class="sxs-lookup"><span data-stu-id="b7fbf-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="b7fbf-109"><strong>Тип данных</strong></span><span class="sxs-lookup"><span data-stu-id="b7fbf-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="b7fbf-110"><strong>Ключ/индекс</strong></span><span class="sxs-lookup"><span data-stu-id="b7fbf-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="b7fbf-111"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="b7fbf-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b7fbf-112"><strong>AppliedBandwidthSourceKey</strong></span><span class="sxs-lookup"><span data-stu-id="b7fbf-112"><strong>AppliedBandwidthSourceKey</strong></span></span></p></td>
<td><p><span data-ttu-id="b7fbf-113">целое</span><span class="sxs-lookup"><span data-stu-id="b7fbf-113">int</span></span></p></td>
<td><p><span data-ttu-id="b7fbf-114">Primary</span><span class="sxs-lookup"><span data-stu-id="b7fbf-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="b7fbf-115">Уникальный номер, идентифицирующий источник.</span><span class="sxs-lookup"><span data-stu-id="b7fbf-115">Unique number identifying the source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7fbf-116"><strong>AppliedBandwidthSource</strong></span><span class="sxs-lookup"><span data-stu-id="b7fbf-116"><strong>AppliedBandwidthSource</strong></span></span></p></td>
<td><p><span data-ttu-id="b7fbf-117">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="b7fbf-117">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="b7fbf-118">Повторя</span><span class="sxs-lookup"><span data-stu-id="b7fbf-118">Unique</span></span></p></td>
<td><p><span data-ttu-id="b7fbf-119">Это источник установленного места для пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="b7fbf-119">This is the source of the bandwidth cap being imposed.</span></span> <span data-ttu-id="b7fbf-120">Она описывает, откуда поступают ограничения пропускной способности (например, "сервер политики", "превратить сервер" или "модальность").</span><span class="sxs-lookup"><span data-stu-id="b7fbf-120">It describes where the bandwidth limit is coming from (for example, “Policy Server”, “TURN Server”, or “Modality”).</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="b7fbf-121">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b7fbf-121">


</div>

<span> </span>

</div>

</div>

</span></span></div>

