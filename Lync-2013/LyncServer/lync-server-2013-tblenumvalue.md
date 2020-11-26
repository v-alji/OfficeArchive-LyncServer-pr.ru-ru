---
title: 'Lync Server 2013: tblEnumValue'
description: 'Lync Server 2013: tblEnumValue.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblEnumValue
ms:assetid: a33df20c-d19d-4f5c-b012-29dab8fb9200
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615025(v=OCS.15)
ms:contentKeyID: 48185040
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 159f90bb96c367fcb3e11725a582a9993080d3fd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444450"
---
# <a name="tblenumvalue-in-lync-server-2013"></a><span data-ttu-id="a3e93-103">tblEnumValue в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a3e93-103">tblEnumValue in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a3e93-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a3e93-104">

<span> </span></span></span>

<span data-ttu-id="a3e93-105">_**Тема последнего изменения:** 2012-06-28_</span><span class="sxs-lookup"><span data-stu-id="a3e93-105">_**Topic Last Modified:** 2012-06-28_</span></span>

<span data-ttu-id="a3e93-106">tblEnumValue — это жесткая таблица, содержащая значения видимости и поведения атрибутов, используемых в таблице node.</span><span class="sxs-lookup"><span data-stu-id="a3e93-106">tblEnumValue is a hardcoded table that contains the Visibility and Behavior values of the attributes that are used in the Node table.</span></span>

### <a name="columns"></a><span data-ttu-id="a3e93-107">Столбцов</span><span class="sxs-lookup"><span data-stu-id="a3e93-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a3e93-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="a3e93-108">Column</span></span></th>
<th><span data-ttu-id="a3e93-109">Тип</span><span class="sxs-lookup"><span data-stu-id="a3e93-109">Type</span></span></th>
<th><span data-ttu-id="a3e93-110">Описание</span><span class="sxs-lookup"><span data-stu-id="a3e93-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a3e93-111">valueID</span><span class="sxs-lookup"><span data-stu-id="a3e93-111">valueID</span></span></p></td>
<td><p><span data-ttu-id="a3e93-112">smallint, NOT NULL</span><span class="sxs-lookup"><span data-stu-id="a3e93-112">smallint, not null</span></span></p></td>
<td><p><span data-ttu-id="a3e93-113">Идентификатор значения.</span><span class="sxs-lookup"><span data-stu-id="a3e93-113">ID of the value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3e93-114">attributeID</span><span class="sxs-lookup"><span data-stu-id="a3e93-114">attributeID</span></span></p></td>
<td><p><span data-ttu-id="a3e93-115">smallint, NOT NULL</span><span class="sxs-lookup"><span data-stu-id="a3e93-115">smallint, not null</span></span></p></td>
<td><p><span data-ttu-id="a3e93-116">Идентификатор атрибута.</span><span class="sxs-lookup"><span data-stu-id="a3e93-116">ID of the attribute.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3e93-117">attributeValue</span><span class="sxs-lookup"><span data-stu-id="a3e93-117">attributeValue</span></span></p></td>
<td><p><span data-ttu-id="a3e93-118">nvarchar (256), NOT NULL</span><span class="sxs-lookup"><span data-stu-id="a3e93-118">nvarchar (256), not null</span></span></p></td>
<td><p><span data-ttu-id="a3e93-119">Имя значения.</span><span class="sxs-lookup"><span data-stu-id="a3e93-119">Name of the value.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="a3e93-120">Параметры</span><span class="sxs-lookup"><span data-stu-id="a3e93-120">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a3e93-121">Столбец</span><span class="sxs-lookup"><span data-stu-id="a3e93-121">Column</span></span></th>
<th><span data-ttu-id="a3e93-122">Описание</span><span class="sxs-lookup"><span data-stu-id="a3e93-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a3e93-123">valueID</span><span class="sxs-lookup"><span data-stu-id="a3e93-123">valueID</span></span></p></td>
<td><p><span data-ttu-id="a3e93-124">Первичный ключ.</span><span class="sxs-lookup"><span data-stu-id="a3e93-124">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3e93-125">attributeID</span><span class="sxs-lookup"><span data-stu-id="a3e93-125">attributeID</span></span></p></td>
<td><p><span data-ttu-id="a3e93-126">Внешний ключ с подстановкой в таблице tblEnumAttribute. attributeID.</span><span class="sxs-lookup"><span data-stu-id="a3e93-126">Foreign key with lookup in tblEnumAttribute.attributeID table.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="table-values"></a><span data-ttu-id="a3e93-127">Значения таблицы</span><span class="sxs-lookup"><span data-stu-id="a3e93-127">Table Values</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a3e93-128">valueID</span><span class="sxs-lookup"><span data-stu-id="a3e93-128">valueID</span></span></th>
<th><span data-ttu-id="a3e93-129">attributeID</span><span class="sxs-lookup"><span data-stu-id="a3e93-129">attributeID</span></span></th>
<th><span data-ttu-id="a3e93-130">attributeValue</span><span class="sxs-lookup"><span data-stu-id="a3e93-130">attributeValue</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a3e93-131">2</span><span class="sxs-lookup"><span data-stu-id="a3e93-131">2</span></span></p></td>
<td><p><span data-ttu-id="a3e93-132">1</span><span class="sxs-lookup"><span data-stu-id="a3e93-132">1</span></span></p></td>
<td><p><span data-ttu-id="a3e93-133">закрытые</span><span class="sxs-lookup"><span data-stu-id="a3e93-133">private</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3e93-134">3</span><span class="sxs-lookup"><span data-stu-id="a3e93-134">3</span></span></p></td>
<td><p><span data-ttu-id="a3e93-135">1</span><span class="sxs-lookup"><span data-stu-id="a3e93-135">1</span></span></p></td>
<td><p><span data-ttu-id="a3e93-136">област</span><span class="sxs-lookup"><span data-stu-id="a3e93-136">scope</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3e93-137">4</span><span class="sxs-lookup"><span data-stu-id="a3e93-137">4</span></span></p></td>
<td><p><span data-ttu-id="a3e93-138">2</span><span class="sxs-lookup"><span data-stu-id="a3e93-138">2</span></span></p></td>
<td><p><span data-ttu-id="a3e93-139">нормальный</span><span class="sxs-lookup"><span data-stu-id="a3e93-139">normal</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3e93-140">5</span><span class="sxs-lookup"><span data-stu-id="a3e93-140">5</span></span></p></td>
<td><p><span data-ttu-id="a3e93-141">2</span><span class="sxs-lookup"><span data-stu-id="a3e93-141">2</span></span></p></td>
<td><p><span data-ttu-id="a3e93-142">auditorium</span><span class="sxs-lookup"><span data-stu-id="a3e93-142">auditorium</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3e93-143">6</span><span class="sxs-lookup"><span data-stu-id="a3e93-143">6</span></span></p></td>
<td><p><span data-ttu-id="a3e93-144">1</span><span class="sxs-lookup"><span data-stu-id="a3e93-144">1</span></span></p></td>
<td><p><span data-ttu-id="a3e93-145">запуска</span><span class="sxs-lookup"><span data-stu-id="a3e93-145">open</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="see-also"></a><span data-ttu-id="a3e93-146">См. также</span><span class="sxs-lookup"><span data-stu-id="a3e93-146">See Also</span></span>


[<span data-ttu-id="a3e93-147">tblNode в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a3e93-147">tblNode in Lync Server 2013</span></span>](lync-server-2013-tblnode.md)  
  

<span data-ttu-id="a3e93-148"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a3e93-148"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

