---
title: 'Lync Server 2013: tblEnumAttribute'
description: 'Lync Server 2013: tblEnumAttribute.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblEnumAttribute
ms:assetid: 17f8b87e-36a6-4f6a-8630-7c76b61a7595
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558617(v=OCS.15)
ms:contentKeyID: 48183523
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ca979a68e758ad47b691ac704f24c68c1841938a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423542"
---
# <a name="tblenumattribute-in-lync-server-2013"></a><span data-ttu-id="39257-103">tblEnumAttribute в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="39257-103">tblEnumAttribute in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="39257-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="39257-104">

<span> </span></span></span>

<span data-ttu-id="39257-105">_**Тема последнего изменения:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="39257-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="39257-106">tblEnumAttribute — это жесткая таблица, которая содержит атрибуты видимости и поведения, которые используются в таблице node.</span><span class="sxs-lookup"><span data-stu-id="39257-106">tblEnumAttribute is a hardcoded table that contains the Visibility and Behavior attributes that are used in the Node table.</span></span>

### <a name="columns"></a><span data-ttu-id="39257-107">Столбцов</span><span class="sxs-lookup"><span data-stu-id="39257-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="39257-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="39257-108">Column</span></span></th>
<th><span data-ttu-id="39257-109">Тип</span><span class="sxs-lookup"><span data-stu-id="39257-109">Type</span></span></th>
<th><span data-ttu-id="39257-110">Описание</span><span class="sxs-lookup"><span data-stu-id="39257-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="39257-111">attributeID</span><span class="sxs-lookup"><span data-stu-id="39257-111">attributeID</span></span></p></td>
<td><p><span data-ttu-id="39257-112">smallint, NOT NULL</span><span class="sxs-lookup"><span data-stu-id="39257-112">smallint, not null</span></span></p></td>
<td><p><span data-ttu-id="39257-113">Идентификатор атрибута.</span><span class="sxs-lookup"><span data-stu-id="39257-113">ID of the attribute.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39257-114">attributeName</span><span class="sxs-lookup"><span data-stu-id="39257-114">attributeName</span></span></p></td>
<td><p><span data-ttu-id="39257-115">nvarchar (256), NOT NULL</span><span class="sxs-lookup"><span data-stu-id="39257-115">nvarchar (256), not null</span></span></p></td>
<td><p><span data-ttu-id="39257-116">Имя атрибута.</span><span class="sxs-lookup"><span data-stu-id="39257-116">Name of the attribute.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="key"></a><span data-ttu-id="39257-117">Ключ</span><span class="sxs-lookup"><span data-stu-id="39257-117">Key</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="39257-118">Столбец</span><span class="sxs-lookup"><span data-stu-id="39257-118">Column</span></span></th>
<th><span data-ttu-id="39257-119">Описание</span><span class="sxs-lookup"><span data-stu-id="39257-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="39257-120">attributeID</span><span class="sxs-lookup"><span data-stu-id="39257-120">attributeID</span></span></p></td>
<td><p><span data-ttu-id="39257-121">Первичный ключ.</span><span class="sxs-lookup"><span data-stu-id="39257-121">Primary key.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="table-values"></a><span data-ttu-id="39257-122">Значения таблицы</span><span class="sxs-lookup"><span data-stu-id="39257-122">Table Values</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="39257-123">attributeID</span><span class="sxs-lookup"><span data-stu-id="39257-123">attributeID</span></span></th>
<th><span data-ttu-id="39257-124">attributeName</span><span class="sxs-lookup"><span data-stu-id="39257-124">attributeName</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="39257-125">1</span><span class="sxs-lookup"><span data-stu-id="39257-125">1</span></span></p></td>
<td><p><span data-ttu-id="39257-126">Отображение.</span><span class="sxs-lookup"><span data-stu-id="39257-126">Visibility.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39257-127">2</span><span class="sxs-lookup"><span data-stu-id="39257-127">2</span></span></p></td>
<td><p><span data-ttu-id="39257-128">Расширения.</span><span class="sxs-lookup"><span data-stu-id="39257-128">Behavior.</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="see-also"></a><span data-ttu-id="39257-129">См. также</span><span class="sxs-lookup"><span data-stu-id="39257-129">See Also</span></span>


[<span data-ttu-id="39257-130">tblNode в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="39257-130">tblNode in Lync Server 2013</span></span>](lync-server-2013-tblnode.md)  
  

<span data-ttu-id="39257-131"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="39257-131"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

