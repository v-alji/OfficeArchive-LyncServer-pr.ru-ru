---
title: 'Lync Server 2013: таблица ContentTypes'
description: 'Lync Server 2013: таблицы ContentType.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ContentTypes table
ms:assetid: e3e38035-457c-4173-bdb9-d53a7420eba2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399007(v=OCS.15)
ms:contentKeyID: 48185723
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 446623ae0ef15d70cd6d85019dfe8eb999f3b2fe
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432256"
---
# <a name="contenttypes-table-in-lync-server-2013"></a><span data-ttu-id="5899b-103">Таблица ContentTypes в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5899b-103">ContentTypes table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5899b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5899b-104">

<span> </span></span></span>

<span data-ttu-id="5899b-105">_**Тема последнего изменения:** 2010-11-07_</span><span class="sxs-lookup"><span data-stu-id="5899b-105">_**Topic Last Modified:** 2010-11-07_</span></span>

<span data-ttu-id="5899b-106">Таблица ContentTypes является вспомогательной таблицей, в которой хранится список типов контента, используемых в одноранговых сеансах и сеансах конференц-связи.</span><span class="sxs-lookup"><span data-stu-id="5899b-106">The ContentTypes table is a supporting table that stores a list of the content types used in both peer-to-peer sessions and conference sessions.</span></span> <span data-ttu-id="5899b-107">Каждая запись в таблице представляет один тип контента.</span><span class="sxs-lookup"><span data-stu-id="5899b-107">Each record in the table represents one content type.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5899b-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="5899b-108">Column</span></span></th>
<th><span data-ttu-id="5899b-109">Тип данных</span><span class="sxs-lookup"><span data-stu-id="5899b-109">Data Type</span></span></th>
<th><span data-ttu-id="5899b-110">Ключ/индекс</span><span class="sxs-lookup"><span data-stu-id="5899b-110">Key/Index</span></span></th>
<th><span data-ttu-id="5899b-111">Сведения</span><span class="sxs-lookup"><span data-stu-id="5899b-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5899b-112"><strong>ContentTypeId</strong></span><span class="sxs-lookup"><span data-stu-id="5899b-112"><strong>ContentTypeId</strong></span></span></p></td>
<td><p><span data-ttu-id="5899b-113">целое</span><span class="sxs-lookup"><span data-stu-id="5899b-113">int</span></span></p></td>
<td><p><span data-ttu-id="5899b-114">Primary</span><span class="sxs-lookup"><span data-stu-id="5899b-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="5899b-115">Уникальный номер, определяющий тип контента.</span><span class="sxs-lookup"><span data-stu-id="5899b-115">Unique number identifying the content type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5899b-116"><strong>Контента</strong></span><span class="sxs-lookup"><span data-stu-id="5899b-116"><strong>ContentType</strong></span></span></p></td>
<td><p><span data-ttu-id="5899b-117">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="5899b-117">nvarchar(256)</span></span></p></td>
<td> </td>
<td><p><span data-ttu-id="5899b-118">Имя типа контента.</span><span class="sxs-lookup"><span data-stu-id="5899b-118">Content type name.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="5899b-119">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5899b-119">


</div>

<span> </span>

</div>

</div>

</span></span></div>

