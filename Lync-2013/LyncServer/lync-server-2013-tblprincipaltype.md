---
title: 'Lync Server 2013: tblPrincipalType'
description: 'Lync Server 2013: tblPrincipalType.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblPrincipalType
ms:assetid: 32e1c1d6-80f4-4624-bf4e-b4c77d3982fa
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558633(v=OCS.15)
ms:contentKeyID: 48183787
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ba0f607d4499b54b16d7ecf8a4e7de603e874788
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398074"
---
# <a name="tblprincipaltype-in-lync-server-2013"></a><span data-ttu-id="946a7-103">tblPrincipalType в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="946a7-103">tblPrincipalType in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="946a7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="946a7-104">

<span> </span></span></span>

<span data-ttu-id="946a7-105">_**Тема последнего изменения:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="946a7-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="946a7-106">tblPrincipalType содержит основные типы для классификации содержимого в таблице tblPrincipal.</span><span class="sxs-lookup"><span data-stu-id="946a7-106">tblPrincipalType contains principal types to categorize what is in the tblPrincipal table.</span></span>

### <a name="columns"></a><span data-ttu-id="946a7-107">Столбцов</span><span class="sxs-lookup"><span data-stu-id="946a7-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="946a7-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="946a7-108">Column</span></span></th>
<th><span data-ttu-id="946a7-109">Тип</span><span class="sxs-lookup"><span data-stu-id="946a7-109">Type</span></span></th>
<th><span data-ttu-id="946a7-110">Описание</span><span class="sxs-lookup"><span data-stu-id="946a7-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="946a7-111">ptypeID</span><span class="sxs-lookup"><span data-stu-id="946a7-111">ptypeID</span></span></p></td>
<td><p><span data-ttu-id="946a7-112">smallint, NOT NULL</span><span class="sxs-lookup"><span data-stu-id="946a7-112">smallint, not null</span></span></p></td>
<td><p><span data-ttu-id="946a7-113">Идентификатор типа участника.</span><span class="sxs-lookup"><span data-stu-id="946a7-113">Principal type ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="946a7-114">ptypeDesc</span><span class="sxs-lookup"><span data-stu-id="946a7-114">ptypeDesc</span></span></p></td>
<td><p><span data-ttu-id="946a7-115">nvarchar (256), NOT NULL</span><span class="sxs-lookup"><span data-stu-id="946a7-115">nvarchar (256), not null</span></span></p></td>
<td><p><span data-ttu-id="946a7-116">Описание типа.</span><span class="sxs-lookup"><span data-stu-id="946a7-116">Description of the type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="946a7-117">ptypeIsSystemUser</span><span class="sxs-lookup"><span data-stu-id="946a7-117">ptypeIsSystemUser</span></span></p></td>
<td><p><span data-ttu-id="946a7-118">bit, NOT NULL</span><span class="sxs-lookup"><span data-stu-id="946a7-118">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="946a7-119">Значение true, если тип соответствует участникам, которые используются для внутренних целей.</span><span class="sxs-lookup"><span data-stu-id="946a7-119">True if the type corresponds to the principals that are used for internal purposes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="946a7-120">ptypeIsUser</span><span class="sxs-lookup"><span data-stu-id="946a7-120">ptypeIsUser</span></span></p></td>
<td><p><span data-ttu-id="946a7-121">bit, NOT NULL</span><span class="sxs-lookup"><span data-stu-id="946a7-121">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="946a7-122">Значение true, если тип является пользовательским типом.</span><span class="sxs-lookup"><span data-stu-id="946a7-122">True if the type is a user type.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="key"></a><span data-ttu-id="946a7-123">Ключ</span><span class="sxs-lookup"><span data-stu-id="946a7-123">Key</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="946a7-124">Столбец</span><span class="sxs-lookup"><span data-stu-id="946a7-124">Column</span></span></th>
<th><span data-ttu-id="946a7-125">Описание</span><span class="sxs-lookup"><span data-stu-id="946a7-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="946a7-126">ptypeID</span><span class="sxs-lookup"><span data-stu-id="946a7-126">ptypeID</span></span></p></td>
<td><p><span data-ttu-id="946a7-127">Первичный ключ.</span><span class="sxs-lookup"><span data-stu-id="946a7-127">Primary key.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="principal-values"></a><span data-ttu-id="946a7-128">Основные значения</span><span class="sxs-lookup"><span data-stu-id="946a7-128">Principal Values</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="946a7-129">ID</span><span class="sxs-lookup"><span data-stu-id="946a7-129">ID</span></span></th>
<th><span data-ttu-id="946a7-130">Должность</span><span class="sxs-lookup"><span data-stu-id="946a7-130">Role</span></span></th>
<th><span data-ttu-id="946a7-131">Описание</span><span class="sxs-lookup"><span data-stu-id="946a7-131">Description</span></span></th>
<th><span data-ttu-id="946a7-132">Пользователь</span><span class="sxs-lookup"><span data-stu-id="946a7-132">User</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="946a7-133">1</span><span class="sxs-lookup"><span data-stu-id="946a7-133">1</span></span></p></td>
<td><p><span data-ttu-id="946a7-134">Любой</span><span class="sxs-lookup"><span data-stu-id="946a7-134">Any</span></span></p></td>
<td><p><span data-ttu-id="946a7-135">Универсальный принципал без известного типа.</span><span class="sxs-lookup"><span data-stu-id="946a7-135">Generic principal with no known type.</span></span> <span data-ttu-id="946a7-136">Не используется в таблице tblPrincipal.</span><span class="sxs-lookup"><span data-stu-id="946a7-136">Not used in tblPrincipal table.</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="946a7-137">2</span><span class="sxs-lookup"><span data-stu-id="946a7-137">2</span></span></p></td>
<td><p><span data-ttu-id="946a7-138">AnyUser</span><span class="sxs-lookup"><span data-stu-id="946a7-138">AnyUser</span></span></p></td>
<td><p><span data-ttu-id="946a7-139">Универсальный принципал для типа пользователя.</span><span class="sxs-lookup"><span data-stu-id="946a7-139">Generic principal of user type.</span></span> <span data-ttu-id="946a7-140">Не используется в таблице tblPrincipal.</span><span class="sxs-lookup"><span data-stu-id="946a7-140">Not used in tblPrincipal table.</span></span></p></td>
<td><p><span data-ttu-id="946a7-141">Да</span><span class="sxs-lookup"><span data-stu-id="946a7-141">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="946a7-142">3</span><span class="sxs-lookup"><span data-stu-id="946a7-142">3</span></span></p></td>
<td><p><span data-ttu-id="946a7-143">AnyGroup</span><span class="sxs-lookup"><span data-stu-id="946a7-143">AnyGroup</span></span></p></td>
<td><p><span data-ttu-id="946a7-144">Универсальный принципал с семантикой группы.</span><span class="sxs-lookup"><span data-stu-id="946a7-144">Generic principal with group semantic.</span></span> <span data-ttu-id="946a7-145">Не используется в таблице tblPrincipal.</span><span class="sxs-lookup"><span data-stu-id="946a7-145">Not used in tblPrincipal table.</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="946a7-146">4</span><span class="sxs-lookup"><span data-stu-id="946a7-146">4</span></span></p></td>
<td><p><span data-ttu-id="946a7-147">SystemUser</span><span class="sxs-lookup"><span data-stu-id="946a7-147">SystemUser</span></span></p></td>
<td><p><span data-ttu-id="946a7-148">Основной сервер, который используется для внутренних целей с помощью сохраняемого сервера чата.</span><span class="sxs-lookup"><span data-stu-id="946a7-148">Principal used internally by Persistent Chat Server.</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="946a7-149">5</span><span class="sxs-lookup"><span data-stu-id="946a7-149">5</span></span></p></td>
<td><p><span data-ttu-id="946a7-150">Пользователь</span><span class="sxs-lookup"><span data-stu-id="946a7-150">User</span></span></p></td>
<td><p><span data-ttu-id="946a7-151">Обычный пользователь.</span><span class="sxs-lookup"><span data-stu-id="946a7-151">Regular user.</span></span></p></td>
<td><p><span data-ttu-id="946a7-152">Да</span><span class="sxs-lookup"><span data-stu-id="946a7-152">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="946a7-153">No8</span><span class="sxs-lookup"><span data-stu-id="946a7-153">8</span></span></p></td>
<td><p><span data-ttu-id="946a7-154">NУДАЛЕННЫЙ</span><span class="sxs-lookup"><span data-stu-id="946a7-154">DC</span></span></p></td>
<td><p><span data-ttu-id="946a7-155">Контроллер домена доменных служб Active Directory.</span><span class="sxs-lookup"><span data-stu-id="946a7-155">Active Directory Domain Services domain controller.</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="946a7-156">@</span><span class="sxs-lookup"><span data-stu-id="946a7-156">9</span></span></p></td>
<td><p><span data-ttu-id="946a7-157">Сгруппирован</span><span class="sxs-lookup"><span data-stu-id="946a7-157">Group</span></span></p></td>
<td><p><span data-ttu-id="946a7-158">Группа безопасности Active Directory.</span><span class="sxs-lookup"><span data-stu-id="946a7-158">Active Directory security group.</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="946a7-159">5-10</span><span class="sxs-lookup"><span data-stu-id="946a7-159">10</span></span></p></td>
<td><p><span data-ttu-id="946a7-160">Folder</span><span class="sxs-lookup"><span data-stu-id="946a7-160">Folder</span></span></p></td>
<td><p><span data-ttu-id="946a7-161">Контейнер Active Directory или подразделение.</span><span class="sxs-lookup"><span data-stu-id="946a7-161">Active Directory container or organizational unit.</span></span></p></td>
<td></td>
</tr>
</tbody>
</table>


<div>

## <a name="see-also"></a><span data-ttu-id="946a7-162">См. также</span><span class="sxs-lookup"><span data-stu-id="946a7-162">See Also</span></span>


[<span data-ttu-id="946a7-163">tblPrincipal в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="946a7-163">tblPrincipal in Lync Server 2013</span></span>](lync-server-2013-tblprincipal.md)  
  

<span data-ttu-id="946a7-164"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="946a7-164"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

