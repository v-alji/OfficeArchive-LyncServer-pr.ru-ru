---
title: 'Lync Server 2013: tblPrincipalAffiliations'
description: 'Lync Server 2013: tblPrincipalAffiliations.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblPrincipalAffiliations
ms:assetid: 45fd8484-5837-44d2-85bb-45c83546607c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558642(v=OCS.15)
ms:contentKeyID: 48183993
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 01c373147a58300e64f22e60e989a777c59b2653
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441370"
---
# <a name="tblprincipalaffiliations-in-lync-server-2013"></a><span data-ttu-id="a736d-103">tblPrincipalAffiliations в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a736d-103">tblPrincipalAffiliations in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a736d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a736d-104">

<span> </span></span></span>

<span data-ttu-id="a736d-105">_**Тема последнего изменения:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="a736d-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="a736d-106">tblPrincipalAffiliations содержит основные сведения о членстве в расположениях, в том числе о группах безопасности доменных служб Active Directory, в контейнерах Active Directory в доменах.</span><span class="sxs-lookup"><span data-stu-id="a736d-106">tblPrincipalAffiliations contains the principal affiliations that describe memberships in locations, including Active Directory Domain Services security groups, in Active Directory containers, in domains.</span></span>

### <a name="columns"></a><span data-ttu-id="a736d-107">Столбцов</span><span class="sxs-lookup"><span data-stu-id="a736d-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a736d-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="a736d-108">Column</span></span></th>
<th><span data-ttu-id="a736d-109">Тип</span><span class="sxs-lookup"><span data-stu-id="a736d-109">Type</span></span></th>
<th><span data-ttu-id="a736d-110">Описание</span><span class="sxs-lookup"><span data-stu-id="a736d-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a736d-111">principalID</span><span class="sxs-lookup"><span data-stu-id="a736d-111">principalID</span></span></p></td>
<td><p><span data-ttu-id="a736d-112">int, NOT NULL</span><span class="sxs-lookup"><span data-stu-id="a736d-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="a736d-113">Идентификатор присоединенного участника.</span><span class="sxs-lookup"><span data-stu-id="a736d-113">ID of the affiliated principal.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a736d-114">affiliationID</span><span class="sxs-lookup"><span data-stu-id="a736d-114">affiliationID</span></span></p></td>
<td><p><span data-ttu-id="a736d-115">int, NOT NULL</span><span class="sxs-lookup"><span data-stu-id="a736d-115">int, not null</span></span></p></td>
<td><p><span data-ttu-id="a736d-116">Идентификатор участника, представляющего назначение.</span><span class="sxs-lookup"><span data-stu-id="a736d-116">ID of the principal representing the affiliation.</span></span> <span data-ttu-id="a736d-117">Каждый принципал (за исключением системных типов пользователей) также имеет свое Самоназначение.</span><span class="sxs-lookup"><span data-stu-id="a736d-117">Each principal (except system-user-types) has a self-affiliation as well.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a736d-118">индекса</span><span class="sxs-lookup"><span data-stu-id="a736d-118">index</span></span></p></td>
<td><p><span data-ttu-id="a736d-119">int, NOT NULL</span><span class="sxs-lookup"><span data-stu-id="a736d-119">int, not null</span></span></p></td>
<td><p><span data-ttu-id="a736d-120">Индекса.</span><span class="sxs-lookup"><span data-stu-id="a736d-120">Index.</span></span> <span data-ttu-id="a736d-121">Значение для самостоятельных принадлежностей —-1, а для других — для других — в пределах от 1 в каждом &lt; principalID, affiliationId &gt; сегмент.</span><span class="sxs-lookup"><span data-stu-id="a736d-121">The value for self-affiliations is -1, and for the other affiliations it increases sequentially from 1 within each &lt;principalID, affiliationId&gt; bucket.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a736d-122">updatedBy</span><span class="sxs-lookup"><span data-stu-id="a736d-122">updatedBy</span></span></p></td>
<td><p><span data-ttu-id="a736d-123">int, NOT NULL</span><span class="sxs-lookup"><span data-stu-id="a736d-123">int, not null</span></span></p></td>
<td><p><span data-ttu-id="a736d-124">Основной участник, который обновил Последнее обновление.</span><span class="sxs-lookup"><span data-stu-id="a736d-124">Principal that did the latest update.</span></span> <span data-ttu-id="a736d-125">Обычно это 1, что означает синхронизацию Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a736d-125">This is usually 1, which means Active Directory Sync.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="a736d-126">Параметры</span><span class="sxs-lookup"><span data-stu-id="a736d-126">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a736d-127">Столбцов</span><span class="sxs-lookup"><span data-stu-id="a736d-127">Columns</span></span></th>
<th><span data-ttu-id="a736d-128">Описание</span><span class="sxs-lookup"><span data-stu-id="a736d-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a736d-129">&lt;principalID, index, affiliationID&gt;</span><span class="sxs-lookup"><span data-stu-id="a736d-129">&lt;principalID, index, affiliationID&gt;</span></span></p></td>
<td><p><span data-ttu-id="a736d-130">Первичный ключ.</span><span class="sxs-lookup"><span data-stu-id="a736d-130">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a736d-131">principalID</span><span class="sxs-lookup"><span data-stu-id="a736d-131">principalID</span></span></p></td>
<td><p><span data-ttu-id="a736d-132">Внешний ключ с подстановкой в таблице tblPrincipal. prinID.</span><span class="sxs-lookup"><span data-stu-id="a736d-132">Foreign key with lookup in tblPrincipal.prinID table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a736d-133">affiliationID</span><span class="sxs-lookup"><span data-stu-id="a736d-133">affiliationID</span></span></p></td>
<td><p><span data-ttu-id="a736d-134">Внешний ключ с подстановкой в таблице tblPrincipal. prinID.</span><span class="sxs-lookup"><span data-stu-id="a736d-134">Foreign key with lookup in tblPrincipal.prinID table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="a736d-135">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a736d-135">


</div>

<span> </span>

</div>

</div>

</span></span></div>

