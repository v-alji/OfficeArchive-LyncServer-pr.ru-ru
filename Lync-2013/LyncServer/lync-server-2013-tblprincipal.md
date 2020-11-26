---
title: 'Lync Server 2013: tblPrincipal'
description: 'Lync Server 2013: tblPrincipal.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblPrincipal
ms:assetid: 79a24502-b4ce-41f0-8979-8caddf535338
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558667(v=OCS.15)
ms:contentKeyID: 48184571
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0f07b37ac4c8ceed5c044b5c263eeee6370adfdc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444415"
---
# <a name="tblprincipal-in-lync-server-2013"></a><span data-ttu-id="878c2-103">tblPrincipal в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="878c2-103">tblPrincipal in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="878c2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="878c2-104">

<span> </span></span></span>

<span data-ttu-id="878c2-105">_**Тема последнего изменения:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="878c2-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="878c2-106">tblPrincipal содержит всех участников, в том числе пользователей, папок и групп.</span><span class="sxs-lookup"><span data-stu-id="878c2-106">tblPrincipal contains all principals, including users, folders, and groups.</span></span>

### <a name="columns"></a><span data-ttu-id="878c2-107">Столбцов</span><span class="sxs-lookup"><span data-stu-id="878c2-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="878c2-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="878c2-108">Column</span></span></th>
<th><span data-ttu-id="878c2-109">Тип</span><span class="sxs-lookup"><span data-stu-id="878c2-109">Type</span></span></th>
<th><span data-ttu-id="878c2-110">Описание</span><span class="sxs-lookup"><span data-stu-id="878c2-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="878c2-111">prinID</span><span class="sxs-lookup"><span data-stu-id="878c2-111">prinID</span></span></p></td>
<td><p><span data-ttu-id="878c2-112">int, NOT NULL</span><span class="sxs-lookup"><span data-stu-id="878c2-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="878c2-113">Идентификатор участника.</span><span class="sxs-lookup"><span data-stu-id="878c2-113">Principal ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="878c2-114">prinGuid</span><span class="sxs-lookup"><span data-stu-id="878c2-114">prinGuid</span></span></p></td>
<td><p><span data-ttu-id="878c2-115">GUID, а не NULL</span><span class="sxs-lookup"><span data-stu-id="878c2-115">GUID, not null</span></span></p></td>
<td><p><span data-ttu-id="878c2-116">Идентификатор GUID участника.</span><span class="sxs-lookup"><span data-stu-id="878c2-116">Principal GUID.</span></span> <span data-ttu-id="878c2-117">Это широко используется как альтернативный первичный ключ, так как его значение пересекается с пространством доменных служб Active Directory.</span><span class="sxs-lookup"><span data-stu-id="878c2-117">This is broadly used as an alternate primary key because its meaning crosses over into the Active Directory Domain Services space.</span></span> <span data-ttu-id="878c2-118">(GUID для кэшированного участника равен GUID соответствующего объекта Active Directory.)</span><span class="sxs-lookup"><span data-stu-id="878c2-118">(The GUID for a cached principal is equal to the corresponding Active Directory object GUID.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="878c2-119">prinUri</span><span class="sxs-lookup"><span data-stu-id="878c2-119">prinUri</span></span></p></td>
<td><p><span data-ttu-id="878c2-120">nvarchar (256), NOT NULL</span><span class="sxs-lookup"><span data-stu-id="878c2-120">nvarchar (256), not null</span></span></p></td>
<td><p><span data-ttu-id="878c2-121">Универсальный код ресурса (URI) участника.</span><span class="sxs-lookup"><span data-stu-id="878c2-121">Principal URI.</span></span> <span data-ttu-id="878c2-122">Схема SIP используется для пользователей, а MA-GRP используется практически всеми остальными.</span><span class="sxs-lookup"><span data-stu-id="878c2-122">The SIP scheme is used for users, and ma-grp is used for almost everything else.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="878c2-123">prinName</span><span class="sxs-lookup"><span data-stu-id="878c2-123">prinName</span></span></p></td>
<td><p><span data-ttu-id="878c2-124">nvarchar (256)</span><span class="sxs-lookup"><span data-stu-id="878c2-124">nvarchar (256)</span></span></p></td>
<td><p><span data-ttu-id="878c2-125">Обычное имя.</span><span class="sxs-lookup"><span data-stu-id="878c2-125">Common name.</span></span> <span data-ttu-id="878c2-126">Используется только для пользовательских типов.</span><span class="sxs-lookup"><span data-stu-id="878c2-126">Used only by user types.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="878c2-127">prinDisplayName</span><span class="sxs-lookup"><span data-stu-id="878c2-127">prinDisplayName</span></span></p></td>
<td><p><span data-ttu-id="878c2-128">Nvarchar (256)</span><span class="sxs-lookup"><span data-stu-id="878c2-128">Nvarchar (256)</span></span></p></td>
<td><p><span data-ttu-id="878c2-129">Отображаемое имя.</span><span class="sxs-lookup"><span data-stu-id="878c2-129">Display name.</span></span> <span data-ttu-id="878c2-130">Используется только для пользовательских типов.</span><span class="sxs-lookup"><span data-stu-id="878c2-130">Used only by user types.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="878c2-131">prinCompanyName</span><span class="sxs-lookup"><span data-stu-id="878c2-131">prinCompanyName</span></span></p></td>
<td><p><span data-ttu-id="878c2-132">nvarchar (256)</span><span class="sxs-lookup"><span data-stu-id="878c2-132">nvarchar (256)</span></span></p></td>
<td><p><span data-ttu-id="878c2-133">Название компании.</span><span class="sxs-lookup"><span data-stu-id="878c2-133">Company name.</span></span> <span data-ttu-id="878c2-134">Используется только для пользовательских типов.</span><span class="sxs-lookup"><span data-stu-id="878c2-134">Used only by user types.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="878c2-135">prinEmail</span><span class="sxs-lookup"><span data-stu-id="878c2-135">prinEmail</span></span></p></td>
<td><p><span data-ttu-id="878c2-136">nvarchar (256)</span><span class="sxs-lookup"><span data-stu-id="878c2-136">nvarchar (256)</span></span></p></td>
<td><p><span data-ttu-id="878c2-137">Отправить по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="878c2-137">Email.</span></span> <span data-ttu-id="878c2-138">Используется только для пользовательских типов.</span><span class="sxs-lookup"><span data-stu-id="878c2-138">Used only by user types.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="878c2-139">prinADPath</span><span class="sxs-lookup"><span data-stu-id="878c2-139">prinADPath</span></span></p></td>
<td><p><span data-ttu-id="878c2-140">nvarchar (384)</span><span class="sxs-lookup"><span data-stu-id="878c2-140">nvarchar (384)</span></span></p></td>
<td><p><span data-ttu-id="878c2-141">Доменное имя объекта Active Directory, который является кэшированной версией участника.</span><span class="sxs-lookup"><span data-stu-id="878c2-141">Domain name of the Active Directory object that the principal is a cached version of.</span></span> <span data-ttu-id="878c2-142">Может принимать значение NULL для типов, которые не являются объектами службы каталогов Active Directory (например, пользователи системы).</span><span class="sxs-lookup"><span data-stu-id="878c2-142">Can be Null for types that are not Active Directory objects (such as system users).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="878c2-143">prinADUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="878c2-143">prinADUserPrincipalName</span></span></p></td>
<td><p><span data-ttu-id="878c2-144">nvarchar (256)</span><span class="sxs-lookup"><span data-stu-id="878c2-144">nvarchar (256)</span></span></p></td>
<td><p><span data-ttu-id="878c2-145">Имя участника-пользователя (UPN) пользователя.</span><span class="sxs-lookup"><span data-stu-id="878c2-145">User’s user principal name (UPN).</span></span> <span data-ttu-id="878c2-146">Используется только обычными типами пользователей.</span><span class="sxs-lookup"><span data-stu-id="878c2-146">Used only by regular user types.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="878c2-147">prinDisabled</span><span class="sxs-lookup"><span data-stu-id="878c2-147">prinDisabled</span></span></p></td>
<td><p><span data-ttu-id="878c2-148">smallint, NOT NULL</span><span class="sxs-lookup"><span data-stu-id="878c2-148">smallint, not null</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="878c2-149">0: участник активен.</span><span class="sxs-lookup"><span data-stu-id="878c2-149">0: Principal is active.</span></span></p></li>
<li><p><span data-ttu-id="878c2-150">1: участник отключен, поскольку возможности SIP пользователя отключены.</span><span class="sxs-lookup"><span data-stu-id="878c2-150">1: Principal is disabled because user’s SIP capabilities are disabled.</span></span></p></li>
<li><p><span data-ttu-id="878c2-151">2: участник удален, так как связанный объект рекламы удален.</span><span class="sxs-lookup"><span data-stu-id="878c2-151">2: Principal is deleted because associated AD object has been deleted.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="878c2-152">prinTypeID</span><span class="sxs-lookup"><span data-stu-id="878c2-152">prinTypeID</span></span></p></td>
<td><p><span data-ttu-id="878c2-153">smallint, NOT NULL</span><span class="sxs-lookup"><span data-stu-id="878c2-153">smallint, not null</span></span></p></td>
<td><p><span data-ttu-id="878c2-154">Тип участника (из таблицы tblPrincipalType).</span><span class="sxs-lookup"><span data-stu-id="878c2-154">Principal type (from tblPrincipalType table).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="878c2-155">prinPoolID</span><span class="sxs-lookup"><span data-stu-id="878c2-155">prinPoolID</span></span></p></td>
<td><p><span data-ttu-id="878c2-156">Типом</span><span class="sxs-lookup"><span data-stu-id="878c2-156">Int</span></span></p></td>
<td><p><span data-ttu-id="878c2-157">Назначение пула Lync для участника.</span><span class="sxs-lookup"><span data-stu-id="878c2-157">Lync pool assignment for the principal.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="878c2-158">prinPolicyID</span><span class="sxs-lookup"><span data-stu-id="878c2-158">prinPolicyID</span></span></p></td>
<td><p><span data-ttu-id="878c2-159">Типом</span><span class="sxs-lookup"><span data-stu-id="878c2-159">Int</span></span></p></td>
<td><p><span data-ttu-id="878c2-160">Значение политики сервера сохраняемого чата для пользователя, если указана политика типа тега.</span><span class="sxs-lookup"><span data-stu-id="878c2-160">Persistent Chat Server policy value for user, if tag type policy is present.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="878c2-161">prinAddedBy</span><span class="sxs-lookup"><span data-stu-id="878c2-161">prinAddedBy</span></span></p></td>
<td><p><span data-ttu-id="878c2-162">целое</span><span class="sxs-lookup"><span data-stu-id="878c2-162">int</span></span></p></td>
<td><p><span data-ttu-id="878c2-163">Идентификатор участника создателя.</span><span class="sxs-lookup"><span data-stu-id="878c2-163">Principal ID of the creator.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="878c2-164">prinAddedOn</span><span class="sxs-lookup"><span data-stu-id="878c2-164">prinAddedOn</span></span></p></td>
<td><p><span data-ttu-id="878c2-165">bigint, NOT NULL</span><span class="sxs-lookup"><span data-stu-id="878c2-165">bigint, not null</span></span></p></td>
<td><p><span data-ttu-id="878c2-166">Метка времени для времени создания.</span><span class="sxs-lookup"><span data-stu-id="878c2-166">Time stamp for the creation time.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="878c2-167">prinUpdatedBy</span><span class="sxs-lookup"><span data-stu-id="878c2-167">prinUpdatedBy</span></span></p></td>
<td><p><span data-ttu-id="878c2-168">целое</span><span class="sxs-lookup"><span data-stu-id="878c2-168">int</span></span></p></td>
<td><p><span data-ttu-id="878c2-169">Идентификатор участника, который последним обновил это.</span><span class="sxs-lookup"><span data-stu-id="878c2-169">ID of the principal that last updated this.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="878c2-170">prinUpdatedOn</span><span class="sxs-lookup"><span data-stu-id="878c2-170">prinUpdatedOn</span></span></p></td>
<td><p><span data-ttu-id="878c2-171">bigint, NOT NULL</span><span class="sxs-lookup"><span data-stu-id="878c2-171">bigint, not null</span></span></p></td>
<td><p><span data-ttu-id="878c2-172">Метка времени для последнего обновления.</span><span class="sxs-lookup"><span data-stu-id="878c2-172">Time stamp for the last update.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="878c2-173">prinVerifiedOn</span><span class="sxs-lookup"><span data-stu-id="878c2-173">prinVerifiedOn</span></span></p></td>
<td><p><span data-ttu-id="878c2-174">DateTime, NOT NULL</span><span class="sxs-lookup"><span data-stu-id="878c2-174">datetime, not null</span></span></p></td>
<td><p><span data-ttu-id="878c2-175">Дата и время последнего обновления службы синхронизации Active Directory для участника.</span><span class="sxs-lookup"><span data-stu-id="878c2-175">Date and time of the last Active Directory Sync refresh for the principal.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="878c2-176">Параметры</span><span class="sxs-lookup"><span data-stu-id="878c2-176">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="878c2-177">Столбец</span><span class="sxs-lookup"><span data-stu-id="878c2-177">Column</span></span></th>
<th><span data-ttu-id="878c2-178">Описание</span><span class="sxs-lookup"><span data-stu-id="878c2-178">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="878c2-179">prinID</span><span class="sxs-lookup"><span data-stu-id="878c2-179">prinID</span></span></p></td>
<td><p><span data-ttu-id="878c2-180">Первичный ключ.</span><span class="sxs-lookup"><span data-stu-id="878c2-180">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="878c2-181">prinTypeID</span><span class="sxs-lookup"><span data-stu-id="878c2-181">prinTypeID</span></span></p></td>
<td><p><span data-ttu-id="878c2-182">Внешний ключ с подстановкой в таблице tblPrincipalType. ptypeID.</span><span class="sxs-lookup"><span data-stu-id="878c2-182">Foreign key with lookup in tblPrincipalType.ptypeID table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="878c2-183">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="878c2-183">


</div>

<span> </span>

</div>

</div>

</span></span></div>

