---
title: 'Lync Server 2013: tblPrincipalMemberDifference'
description: 'Lync Server 2013: tblPrincipalMemberDifference.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblPrincipalMemberDifference
ms:assetid: 0b94f555-6888-4fe0-a048-4660a2513276
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558612(v=OCS.15)
ms:contentKeyID: 48183379
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ce7c770a6fed02dc27d2493816fae58943d391a6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398116"
---
# <a name="tblprincipalmemberdifference-in-lync-server-2013"></a><span data-ttu-id="12999-103">tblPrincipalMemberDifference в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="12999-103">tblPrincipalMemberDifference in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="12999-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="12999-104">

<span> </span></span></span>

<span data-ttu-id="12999-105">_**Тема последнего изменения:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="12999-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="12999-106">tblPrincipalMemberDifference содержит изменения членства в группах (добавленные и удаленные участники), которые еще не были обработаны в последующих шагах синхронизации доменных служб Active Directory.</span><span class="sxs-lookup"><span data-stu-id="12999-106">tblPrincipalMemberDifference contains group membership changes (both added and removed members) that have not yet been processed by the later Active Directory Domain Services Sync steps.</span></span>

### <a name="columns"></a><span data-ttu-id="12999-107">Столбцов</span><span class="sxs-lookup"><span data-stu-id="12999-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="12999-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="12999-108">Column</span></span></th>
<th><span data-ttu-id="12999-109">Тип</span><span class="sxs-lookup"><span data-stu-id="12999-109">Type</span></span></th>
<th><span data-ttu-id="12999-110">Описание</span><span class="sxs-lookup"><span data-stu-id="12999-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="12999-111">prinGuid</span><span class="sxs-lookup"><span data-stu-id="12999-111">prinGuid</span></span></p></td>
<td><p><span data-ttu-id="12999-112">GUID, а не NULL</span><span class="sxs-lookup"><span data-stu-id="12999-112">GUID, not null</span></span></p></td>
<td><p><span data-ttu-id="12999-113">Идентификатор GUID участника измененной группы.</span><span class="sxs-lookup"><span data-stu-id="12999-113">Principal GUID of the group that changed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12999-114">memberADPath</span><span class="sxs-lookup"><span data-stu-id="12999-114">memberADPath</span></span></p></td>
<td><p><span data-ttu-id="12999-115">nvarchar (256)</span><span class="sxs-lookup"><span data-stu-id="12999-115">nvarchar (256)</span></span></p></td>
<td><p><span data-ttu-id="12999-116">Отличительное имя участника.</span><span class="sxs-lookup"><span data-stu-id="12999-116">Distinguished name of the member.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12999-117">memberRemoved</span><span class="sxs-lookup"><span data-stu-id="12999-117">memberRemoved</span></span></p></td>
<td><p><span data-ttu-id="12999-118">bit, NOT NULL</span><span class="sxs-lookup"><span data-stu-id="12999-118">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="12999-119">Значение false, если элемент был добавлен.</span><span class="sxs-lookup"><span data-stu-id="12999-119">False if the member was added.</span></span> <span data-ttu-id="12999-120">Значение true, если элемент удален.</span><span class="sxs-lookup"><span data-stu-id="12999-120">True if the member was removed.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="key"></a><span data-ttu-id="12999-121">Ключ</span><span class="sxs-lookup"><span data-stu-id="12999-121">Key</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="12999-122">Столбец</span><span class="sxs-lookup"><span data-stu-id="12999-122">Column</span></span></th>
<th><span data-ttu-id="12999-123">Описание</span><span class="sxs-lookup"><span data-stu-id="12999-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="12999-124">&lt;prinGuid, memberADPath&gt;</span><span class="sxs-lookup"><span data-stu-id="12999-124">&lt;prinGuid, memberADPath&gt;</span></span></p></td>
<td><p><span data-ttu-id="12999-125">Первичный ключ.</span><span class="sxs-lookup"><span data-stu-id="12999-125">Primary key.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="12999-126">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="12999-126">


</div>

<span> </span>

</div>

</div>

</span></span></div>

