---
title: 'Lync Server 2013: tblPrincipalRole'
description: 'Lync Server 2013: tblPrincipalRole.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblPrincipalRole
ms:assetid: dcd16dc1-a66c-4720-a48f-ec8b28337383
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615039(v=OCS.15)
ms:contentKeyID: 48185597
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f58ffda3136c254ee77f14d33dcb42af5d172c4a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398086"
---
# <a name="tblprincipalrole-in-lync-server-2013"></a><span data-ttu-id="1361e-103">tblPrincipalRole в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1361e-103">tblPrincipalRole in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1361e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1361e-104">

<span> </span></span></span>

<span data-ttu-id="1361e-105">_**Тема последнего изменения:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="1361e-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="1361e-106">tblPrincipalRole включает явные роли, назначенные узлам.</span><span class="sxs-lookup"><span data-stu-id="1361e-106">tblPrincipalRole contains explicit roles assigned to nodes.</span></span>

### <a name="columns"></a><span data-ttu-id="1361e-107">Столбцов</span><span class="sxs-lookup"><span data-stu-id="1361e-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1361e-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="1361e-108">Column</span></span></th>
<th><span data-ttu-id="1361e-109">Тип</span><span class="sxs-lookup"><span data-stu-id="1361e-109">Type</span></span></th>
<th><span data-ttu-id="1361e-110">Описание</span><span class="sxs-lookup"><span data-stu-id="1361e-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1361e-111">prinRoleNodeID</span><span class="sxs-lookup"><span data-stu-id="1361e-111">prinRoleNodeID</span></span></p></td>
<td><p><span data-ttu-id="1361e-112">int, NOT NULL</span><span class="sxs-lookup"><span data-stu-id="1361e-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="1361e-113">Идентификатор узла, к которому относится роль.</span><span class="sxs-lookup"><span data-stu-id="1361e-113">Node ID that the role applies to.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1361e-114">prinRolePrinID</span><span class="sxs-lookup"><span data-stu-id="1361e-114">prinRolePrinID</span></span></p></td>
<td><p><span data-ttu-id="1361e-115">int, NOT NULL</span><span class="sxs-lookup"><span data-stu-id="1361e-115">int, not null</span></span></p></td>
<td><p><span data-ttu-id="1361e-116">Идентификатор участника.</span><span class="sxs-lookup"><span data-stu-id="1361e-116">Principal ID.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1361e-117">prinRoleTypeID</span><span class="sxs-lookup"><span data-stu-id="1361e-117">prinRoleTypeID</span></span></p></td>
<td><p><span data-ttu-id="1361e-118">int, NOT NULL</span><span class="sxs-lookup"><span data-stu-id="1361e-118">int, not null</span></span></p></td>
<td><p><span data-ttu-id="1361e-119">Идентификатор типа роли (из tblRoleType).</span><span class="sxs-lookup"><span data-stu-id="1361e-119">Role type ID (from tblRoleType).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1361e-120">prinRoleUpdatedBy</span><span class="sxs-lookup"><span data-stu-id="1361e-120">prinRoleUpdatedBy</span></span></p></td>
<td><p><span data-ttu-id="1361e-121">int, NOT NULL</span><span class="sxs-lookup"><span data-stu-id="1361e-121">int, not null</span></span></p></td>
<td><p><span data-ttu-id="1361e-122">Идентификатор участника, который последним обновил эту запись.</span><span class="sxs-lookup"><span data-stu-id="1361e-122">ID of the principal that last updated this entry.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="1361e-123">Параметры</span><span class="sxs-lookup"><span data-stu-id="1361e-123">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1361e-124">Столбец</span><span class="sxs-lookup"><span data-stu-id="1361e-124">Column</span></span></th>
<th><span data-ttu-id="1361e-125">Описание</span><span class="sxs-lookup"><span data-stu-id="1361e-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1361e-126">&lt;prinRoleNodeID, prinRolePrinID, prinRoleTypeID&gt;</span><span class="sxs-lookup"><span data-stu-id="1361e-126">&lt;prinRoleNodeID, prinRolePrinID, prinRoleTypeID&gt;</span></span></p></td>
<td><p><span data-ttu-id="1361e-127">Первичный ключ.</span><span class="sxs-lookup"><span data-stu-id="1361e-127">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1361e-128">prinRoleNodeID</span><span class="sxs-lookup"><span data-stu-id="1361e-128">prinRoleNodeID</span></span></p></td>
<td><p><span data-ttu-id="1361e-129">Внешний ключ с подстановкой в таблице tblNode. nodeID.</span><span class="sxs-lookup"><span data-stu-id="1361e-129">Foreign key with lookup in tblNode.nodeID table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1361e-130">prinRolePrinID</span><span class="sxs-lookup"><span data-stu-id="1361e-130">prinRolePrinID</span></span></p></td>
<td><p><span data-ttu-id="1361e-131">Внешний ключ с подстановкой в таблице tblPrincipal. prinID.</span><span class="sxs-lookup"><span data-stu-id="1361e-131">Foreign key with lookup in tblPrincipal.prinID table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1361e-132">prinRoleTypeID</span><span class="sxs-lookup"><span data-stu-id="1361e-132">prinRoleTypeID</span></span></p></td>
<td><p><span data-ttu-id="1361e-133">Внешний ключ с подстановкой в таблице tblRoleType. rtypeID.</span><span class="sxs-lookup"><span data-stu-id="1361e-133">Foreign key with lookup in tblRoleType.rtypeID table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="1361e-134">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1361e-134">


</div>

<span> </span>

</div>

</div>

</span></span></div>

