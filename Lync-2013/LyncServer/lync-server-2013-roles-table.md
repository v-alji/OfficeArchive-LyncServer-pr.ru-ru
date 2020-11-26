---
title: 'Lync Server 2013: таблица Roles'
description: 'Таблица "роли" Lync Server 2013: Roles.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Roles table
ms:assetid: e8eb8a10-26b5-488b-bc8c-f9ef93f98bdb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399043(v=OCS.15)
ms:contentKeyID: 48185893
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d16f9483fc97145d82faf7e8f1175772f10f9a4b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442357"
---
# <a name="roles-table-in-lync-server-2013"></a><span data-ttu-id="379cf-103">Таблица Roles в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="379cf-103">Roles table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="379cf-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="379cf-104">

<span> </span></span></span>

<span data-ttu-id="379cf-105">_**Тема последнего изменения:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="379cf-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="379cf-106">Таблица ролей — это статическая таблица, в которой хранится список возможных ролей конференции, таких как участники и выступающие.</span><span class="sxs-lookup"><span data-stu-id="379cf-106">The Roles table is a static table that stores the list of possible conference roles, such as attendee and presenter.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="379cf-107">Столбец</span><span class="sxs-lookup"><span data-stu-id="379cf-107">Column</span></span></th>
<th><span data-ttu-id="379cf-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="379cf-108">Data Type</span></span></th>
<th><span data-ttu-id="379cf-109">Ключ/индекс</span><span class="sxs-lookup"><span data-stu-id="379cf-109">Key/Index</span></span></th>
<th><span data-ttu-id="379cf-110">Сведения</span><span class="sxs-lookup"><span data-stu-id="379cf-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="379cf-111"><strong>RoleId</strong></span><span class="sxs-lookup"><span data-stu-id="379cf-111"><strong>RoleId</strong></span></span></p></td>
<td><p><span data-ttu-id="379cf-112">tinyint</span><span class="sxs-lookup"><span data-stu-id="379cf-112">tinyint</span></span></p></td>
<td><p><span data-ttu-id="379cf-113">Primary</span><span class="sxs-lookup"><span data-stu-id="379cf-113">Primary</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="379cf-114"><strong>Роль</strong></span><span class="sxs-lookup"><span data-stu-id="379cf-114"><strong>Role</strong></span></span></p></td>
<td><p><span data-ttu-id="379cf-115">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="379cf-115">nvarchar(256)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="379cf-116">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="379cf-116">Allowed values:</span></span></p>
<ul>
<li><p><span data-ttu-id="379cf-117">0 — неизвестно</span><span class="sxs-lookup"><span data-stu-id="379cf-117">0 - Unknown</span></span></p></li>
<li><p><span data-ttu-id="379cf-118">1 — выступающий</span><span class="sxs-lookup"><span data-stu-id="379cf-118">1 - Presenter</span></span></p></li>
<li><p><span data-ttu-id="379cf-119">2 участника</span><span class="sxs-lookup"><span data-stu-id="379cf-119">2 - Attendee</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table><span data-ttu-id="379cf-120">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="379cf-120">


</div>

<span> </span>

</div>

</div>

</span></span></div>

