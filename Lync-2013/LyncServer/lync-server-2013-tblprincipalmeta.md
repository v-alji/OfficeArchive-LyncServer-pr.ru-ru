---
title: 'Lync Server 2013: tblPrincipalMeta'
description: 'Lync Server 2013: tblPrincipalMeta.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblPrincipalMeta
ms:assetid: 808490d4-7d6d-47a2-b8af-b5940d47073b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615009(v=OCS.15)
ms:contentKeyID: 48184648
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 899fd1e450dac52afa56c1ee1de86da82b2db309
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398107"
---
# <a name="tblprincipalmeta-in-lync-server-2013"></a><span data-ttu-id="d2180-103">tblPrincipalMeta в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d2180-103">tblPrincipalMeta in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d2180-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d2180-104">

<span> </span></span></span>

<span data-ttu-id="d2180-105">_**Тема последнего изменения:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="d2180-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="d2180-106">tblPrincipalMeta содержит участников, которые необходимо обновлять из доменных служб Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d2180-106">tblPrincipalMeta contains the principals that have to be refreshed from Active Directory Domain Services.</span></span>

### <a name="columns"></a><span data-ttu-id="d2180-107">Столбцов</span><span class="sxs-lookup"><span data-stu-id="d2180-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d2180-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="d2180-108">Column</span></span></th>
<th><span data-ttu-id="d2180-109">Тип</span><span class="sxs-lookup"><span data-stu-id="d2180-109">Type</span></span></th>
<th><span data-ttu-id="d2180-110">Описание</span><span class="sxs-lookup"><span data-stu-id="d2180-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d2180-111">prinID</span><span class="sxs-lookup"><span data-stu-id="d2180-111">prinID</span></span></p></td>
<td><p><span data-ttu-id="d2180-112">int, NOT NULL</span><span class="sxs-lookup"><span data-stu-id="d2180-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="d2180-113">Идентификатор участника.</span><span class="sxs-lookup"><span data-stu-id="d2180-113">Principal ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2180-114">prinAffiliationsDirty</span><span class="sxs-lookup"><span data-stu-id="d2180-114">prinAffiliationsDirty</span></span></p></td>
<td><p><span data-ttu-id="d2180-115">bit, NOT NULL</span><span class="sxs-lookup"><span data-stu-id="d2180-115">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="d2180-116">Значение true, если присвоить участникам участники необходимо обновлять.</span><span class="sxs-lookup"><span data-stu-id="d2180-116">True if principal affiliations have to be refreshed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2180-117">prinAttributesDirty</span><span class="sxs-lookup"><span data-stu-id="d2180-117">prinAttributesDirty</span></span></p></td>
<td><p><span data-ttu-id="d2180-118">bit, NOT NULL</span><span class="sxs-lookup"><span data-stu-id="d2180-118">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="d2180-119">Значение true, если атрибуты участника нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="d2180-119">True if principal attributes have to be refreshed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2180-120">prinDeleted</span><span class="sxs-lookup"><span data-stu-id="d2180-120">prinDeleted</span></span></p></td>
<td><p><span data-ttu-id="d2180-121">bit, NOT NULL</span><span class="sxs-lookup"><span data-stu-id="d2180-121">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="d2180-122">Значение true, если участник удален.</span><span class="sxs-lookup"><span data-stu-id="d2180-122">True if the principal has been deleted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2180-123">tryCount</span><span class="sxs-lookup"><span data-stu-id="d2180-123">tryCount</span></span></p></td>
<td><p><span data-ttu-id="d2180-124">целое</span><span class="sxs-lookup"><span data-stu-id="d2180-124">int</span></span></p></td>
<td><p><span data-ttu-id="d2180-125">Количество попыток обновления участника из доменных служб Active Directory, произошедших в данный момент.</span><span class="sxs-lookup"><span data-stu-id="d2180-125">Number of attempts to refresh the principal from AD DS that have happened so far.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2180-126">lastTry</span><span class="sxs-lookup"><span data-stu-id="d2180-126">lastTry</span></span></p></td>
<td><p><span data-ttu-id="d2180-127">datetime</span><span class="sxs-lookup"><span data-stu-id="d2180-127">datetime</span></span></p></td>
<td><p><span data-ttu-id="d2180-128">Метка времени последней попытки обновить участника.</span><span class="sxs-lookup"><span data-stu-id="d2180-128">Time stamp from the latest attempt to refresh the principal.</span></span> <span data-ttu-id="d2180-129">Может иметь значение null, если вы еще не пытались обновить обновление.</span><span class="sxs-lookup"><span data-stu-id="d2180-129">Can be null if no refresh has been attempted yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2180-130">nextTry</span><span class="sxs-lookup"><span data-stu-id="d2180-130">nextTry</span></span></p></td>
<td><p><span data-ttu-id="d2180-131">datetime</span><span class="sxs-lookup"><span data-stu-id="d2180-131">datetime</span></span></p></td>
<td><p><span data-ttu-id="d2180-132">Метка времени для следующего запланированного обновления.</span><span class="sxs-lookup"><span data-stu-id="d2180-132">Time stamp for the next scheduled refresh.</span></span> <span data-ttu-id="d2180-133">Может иметь значение null, если дальнейшее обновление не запланировано.</span><span class="sxs-lookup"><span data-stu-id="d2180-133">Can be null if no further refresh has been scheduled.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="d2180-134">Параметры</span><span class="sxs-lookup"><span data-stu-id="d2180-134">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d2180-135">Столбец</span><span class="sxs-lookup"><span data-stu-id="d2180-135">Column</span></span></th>
<th><span data-ttu-id="d2180-136">Описание</span><span class="sxs-lookup"><span data-stu-id="d2180-136">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d2180-137">prinID</span><span class="sxs-lookup"><span data-stu-id="d2180-137">prinID</span></span></p></td>
<td><p><span data-ttu-id="d2180-138">Первичный ключ.</span><span class="sxs-lookup"><span data-stu-id="d2180-138">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2180-139">prinID</span><span class="sxs-lookup"><span data-stu-id="d2180-139">prinID</span></span></p></td>
<td><p><span data-ttu-id="d2180-140">Внешний ключ с подстановкой в таблице tblPrincipal. prinID.</span><span class="sxs-lookup"><span data-stu-id="d2180-140">Foreign key with lookup in tblPrincipal.prinID table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="d2180-141">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d2180-141">


</div>

<span> </span>

</div>

</div>

</span></span></div>

