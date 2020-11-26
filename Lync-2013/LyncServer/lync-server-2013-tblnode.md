---
title: 'Lync Server 2013: tblNode'
description: 'Lync Server 2013: tblNode.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblNode
ms:assetid: a31d2961-aa83-4286-a12e-15d279c95f19
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615024(v=OCS.15)
ms:contentKeyID: 48184960
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d0a5d630621c32cbc54501249c7a679bf4023c60
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423521"
---
# <a name="tblnode-in-lync-server-2013"></a><span data-ttu-id="718aa-103">tblNode в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="718aa-103">tblNode in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="718aa-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="718aa-104">

<span> </span></span></span>

<span data-ttu-id="718aa-105">_**Тема последнего изменения:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="718aa-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="718aa-106">tblNode включает дерево объектов (с узлами "Категория" или "комната чата") как управляемое на панели управления Lync Server 2013 и административных командлетов.</span><span class="sxs-lookup"><span data-stu-id="718aa-106">tblNode contains the object tree (with category or chat room nodes) as managed in the Lync Server 2013 Control Panel and administrative cmdlets.</span></span>

### <a name="columns"></a><span data-ttu-id="718aa-107">Столбцов</span><span class="sxs-lookup"><span data-stu-id="718aa-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="718aa-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="718aa-108">Column</span></span></th>
<th><span data-ttu-id="718aa-109">Тип</span><span class="sxs-lookup"><span data-stu-id="718aa-109">Type</span></span></th>
<th><span data-ttu-id="718aa-110">Описание</span><span class="sxs-lookup"><span data-stu-id="718aa-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="718aa-111">nodeID</span><span class="sxs-lookup"><span data-stu-id="718aa-111">nodeID</span></span></p></td>
<td><p><span data-ttu-id="718aa-112">int, NOT NULL</span><span class="sxs-lookup"><span data-stu-id="718aa-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="718aa-113">Идентификатор узла (уникальный номер).</span><span class="sxs-lookup"><span data-stu-id="718aa-113">Node ID (unique number).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="718aa-114">nodeGuid</span><span class="sxs-lookup"><span data-stu-id="718aa-114">nodeGuid</span></span></p></td>
<td><p><span data-ttu-id="718aa-115">GUID, а не NULL</span><span class="sxs-lookup"><span data-stu-id="718aa-115">GUID, not null</span></span></p></td>
<td><p><span data-ttu-id="718aa-116">GUID узла.</span><span class="sxs-lookup"><span data-stu-id="718aa-116">Node GUID.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="718aa-117">parentID</span><span class="sxs-lookup"><span data-stu-id="718aa-117">parentID</span></span></p></td>
<td><p><span data-ttu-id="718aa-118">целое</span><span class="sxs-lookup"><span data-stu-id="718aa-118">int</span></span></p></td>
<td><p><span data-ttu-id="718aa-119">Идентификатор узла родителя.</span><span class="sxs-lookup"><span data-stu-id="718aa-119">Node ID of parent.</span></span> <span data-ttu-id="718aa-120">Корневой узел (с ИДЕНТИФИКАТОРом 1) также включает себя как родительский.</span><span class="sxs-lookup"><span data-stu-id="718aa-120">The root node (with ID 1) includes itself as parent as well.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="718aa-121">Узла</span><span class="sxs-lookup"><span data-stu-id="718aa-121">nodeType</span></span></p></td>
<td><p><span data-ttu-id="718aa-122">bit, NOT NULL</span><span class="sxs-lookup"><span data-stu-id="718aa-122">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="718aa-123">Значение true, если узел является категорией.</span><span class="sxs-lookup"><span data-stu-id="718aa-123">True if the node is a category.</span></span></p>
<p><span data-ttu-id="718aa-124">Значение false, если узел является комнатой чата.</span><span class="sxs-lookup"><span data-stu-id="718aa-124">False if the node is a chat room.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="718aa-125">nodeName</span><span class="sxs-lookup"><span data-stu-id="718aa-125">nodeName</span></span></p></td>
<td><p><span data-ttu-id="718aa-126">nvarchar (256), NOT NULL</span><span class="sxs-lookup"><span data-stu-id="718aa-126">nvarchar (256), not null</span></span></p></td>
<td><p><span data-ttu-id="718aa-127">Имя узла.</span><span class="sxs-lookup"><span data-stu-id="718aa-127">Node name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="718aa-128">nodeDesc</span><span class="sxs-lookup"><span data-stu-id="718aa-128">nodeDesc</span></span></p></td>
<td><p><span data-ttu-id="718aa-129">nvarchar (256), NOT NULL</span><span class="sxs-lookup"><span data-stu-id="718aa-129">nvarchar (256), not null</span></span></p></td>
<td><p><span data-ttu-id="718aa-130">Описание узла.</span><span class="sxs-lookup"><span data-stu-id="718aa-130">Node description.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="718aa-131">сообщение</span><span class="sxs-lookup"><span data-stu-id="718aa-131">invite</span></span></p></td>
<td><p><span data-ttu-id="718aa-132">бит</span><span class="sxs-lookup"><span data-stu-id="718aa-132">bit</span></span></p></td>
<td><p><span data-ttu-id="718aa-133">Для категорий:</span><span class="sxs-lookup"><span data-stu-id="718aa-133">For categories:</span></span></p>
<ul>
<li><p><span data-ttu-id="718aa-134">Значение true, если приглашения включены.</span><span class="sxs-lookup"><span data-stu-id="718aa-134">True if invites are on.</span></span></p></li>
<li><p><span data-ttu-id="718aa-135">Значение false, если приглашения отключены.</span><span class="sxs-lookup"><span data-stu-id="718aa-135">False if invites are off.</span></span></p></li>
</ul>
<p><span data-ttu-id="718aa-136">Для комнат:</span><span class="sxs-lookup"><span data-stu-id="718aa-136">For rooms:</span></span></p>
<ul>
<li><p><span data-ttu-id="718aa-137">Значение false, если приглашения отключены (переопределяет родительскую категорию).</span><span class="sxs-lookup"><span data-stu-id="718aa-137">False if invites are off (overrides the parent category).</span></span></p></li>
<li><p><span data-ttu-id="718aa-138">Значение null, если параметр приглашения наследуется от родительской категории.</span><span class="sxs-lookup"><span data-stu-id="718aa-138">Null if the invites setting is inherited from the parent category.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="718aa-139">войдет</span><span class="sxs-lookup"><span data-stu-id="718aa-139">logged</span></span></p></td>
<td><p><span data-ttu-id="718aa-140">бит</span><span class="sxs-lookup"><span data-stu-id="718aa-140">bit</span></span></p></td>
<td><p><span data-ttu-id="718aa-141">Для категорий:</span><span class="sxs-lookup"><span data-stu-id="718aa-141">For categories:</span></span></p>
<ul>
<li><p><span data-ttu-id="718aa-142">Значение true, если история чата включена.</span><span class="sxs-lookup"><span data-stu-id="718aa-142">True if chat history is on.</span></span></p></li>
<li><p><span data-ttu-id="718aa-143">Значение false, если ведение журнала чата отключено.</span><span class="sxs-lookup"><span data-stu-id="718aa-143">False if chat history is off.</span></span></p></li>
</ul>
<p><span data-ttu-id="718aa-144">Для комнат:</span><span class="sxs-lookup"><span data-stu-id="718aa-144">For rooms:</span></span></p>
<ul>
<li><p><span data-ttu-id="718aa-145">Значения.</span><span class="sxs-lookup"><span data-stu-id="718aa-145">Null.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="718aa-146">filePost</span><span class="sxs-lookup"><span data-stu-id="718aa-146">filePost</span></span></p></td>
<td><p><span data-ttu-id="718aa-147">бит</span><span class="sxs-lookup"><span data-stu-id="718aa-147">bit</span></span></p></td>
<td><p><span data-ttu-id="718aa-148">Для категорий:</span><span class="sxs-lookup"><span data-stu-id="718aa-148">For categories:</span></span></p>
<ul>
<li><p><span data-ttu-id="718aa-149">Значение true, если отправка файлов разрешена.</span><span class="sxs-lookup"><span data-stu-id="718aa-149">True if file uploads are allowed.</span></span></p></li>
<li><p><span data-ttu-id="718aa-150">Значение false, если отправка файлов запрещена.</span><span class="sxs-lookup"><span data-stu-id="718aa-150">False if file uploads are disallowed.</span></span></p></li>
</ul>
<p><span data-ttu-id="718aa-151">Для комнат:</span><span class="sxs-lookup"><span data-stu-id="718aa-151">For rooms:</span></span></p>
<ul>
<li><p><span data-ttu-id="718aa-152">Значения.</span><span class="sxs-lookup"><span data-stu-id="718aa-152">Null.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="718aa-153">отключает</span><span class="sxs-lookup"><span data-stu-id="718aa-153">disabled</span></span></p></td>
<td><p><span data-ttu-id="718aa-154">bit, NOT NULL</span><span class="sxs-lookup"><span data-stu-id="718aa-154">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="718aa-155">Значение true, если комната чата отключена.</span><span class="sxs-lookup"><span data-stu-id="718aa-155">True if the chat room is disabled.</span></span> <span data-ttu-id="718aa-156">Применимо только к комнатам чата.</span><span class="sxs-lookup"><span data-stu-id="718aa-156">Applies only to chat rooms.</span></span> <span data-ttu-id="718aa-157">(Ложь для категорий.)</span><span class="sxs-lookup"><span data-stu-id="718aa-157">(False for categories.)</span></span></p></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="718aa-158">расширения</span><span class="sxs-lookup"><span data-stu-id="718aa-158">behavior</span></span></p></td>
<td><p><span data-ttu-id="718aa-159">smallint, NOT NULL</span><span class="sxs-lookup"><span data-stu-id="718aa-159">smallint, not null</span></span></p></td>
<td><p><span data-ttu-id="718aa-160">Поведение (Поиск в таблице EnumValue):</span><span class="sxs-lookup"><span data-stu-id="718aa-160">Behavior (looked up in EnumValue table):</span></span></p>
<ul>
<li><p><span data-ttu-id="718aa-161">4: обычный (обычные комнаты чата).</span><span class="sxs-lookup"><span data-stu-id="718aa-161">4: Normal (normal chat rooms).</span></span></p></li>
<li><p><span data-ttu-id="718aa-162">5: Auditorium (Auditorium) — комнаты чата только выступающие могут участвовать в программе.</span><span class="sxs-lookup"><span data-stu-id="718aa-162">5: Auditorium (auditorium chat rooms, only presenters can contribute).</span></span></p></li>
</ul>
<p><span data-ttu-id="718aa-163">Применимо только к комнатам чата.</span><span class="sxs-lookup"><span data-stu-id="718aa-163">Applies only to chat rooms.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="718aa-164">Отображение</span><span class="sxs-lookup"><span data-stu-id="718aa-164">visibility</span></span></p></td>
<td><p><span data-ttu-id="718aa-165">smallint, NOT NULL</span><span class="sxs-lookup"><span data-stu-id="718aa-165">smallint, not null</span></span></p></td>
<td><p><span data-ttu-id="718aa-166">Visibility (Поиск в таблице EnumValue):</span><span class="sxs-lookup"><span data-stu-id="718aa-166">Visibility (looked up on EnumValue table):</span></span></p>
<ul>
<li><p><span data-ttu-id="718aa-167">2: частный</span><span class="sxs-lookup"><span data-stu-id="718aa-167">2: Private</span></span></p></li>
<li><p><span data-ttu-id="718aa-168">3: область охвата</span><span class="sxs-lookup"><span data-stu-id="718aa-168">3: Scoped</span></span></p></li>
<li><p><span data-ttu-id="718aa-169">6: открыть</span><span class="sxs-lookup"><span data-stu-id="718aa-169">6: Open</span></span></p></li>
</ul>
<p><span data-ttu-id="718aa-170">Применимо только к комнатам чата.</span><span class="sxs-lookup"><span data-stu-id="718aa-170">Applies only to chat rooms.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="718aa-171">siopID</span><span class="sxs-lookup"><span data-stu-id="718aa-171">siopID</span></span></p></td>
<td><p><span data-ttu-id="718aa-172">Глобальный уникальный идентификатор (GUID)</span><span class="sxs-lookup"><span data-stu-id="718aa-172">GUID</span></span></p></td>
<td><p><span data-ttu-id="718aa-173">Add-In GUID, если надстройка связана с этой комнатой чата.</span><span class="sxs-lookup"><span data-stu-id="718aa-173">Add-In GUID if an add-in is associated with this chat room.</span></span> <span data-ttu-id="718aa-174">(В категориях нет надстроек.)</span><span class="sxs-lookup"><span data-stu-id="718aa-174">(Categories do not have add-ins.)</span></span></p>
<p><span data-ttu-id="718aa-175">Сведения о надстройке ищутся в таблице SiopWhiteList.</span><span class="sxs-lookup"><span data-stu-id="718aa-175">The add-in information is looked up in SiopWhiteList table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="718aa-176">nodeAddedBy</span><span class="sxs-lookup"><span data-stu-id="718aa-176">nodeAddedBy</span></span></p></td>
<td><p><span data-ttu-id="718aa-177">int, NOT NULL</span><span class="sxs-lookup"><span data-stu-id="718aa-177">int, not null</span></span></p></td>
<td><p><span data-ttu-id="718aa-178">Идентификатор участника, который создал этот узел.</span><span class="sxs-lookup"><span data-stu-id="718aa-178">ID of the principal that created this node.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="718aa-179">nodeAddedOn</span><span class="sxs-lookup"><span data-stu-id="718aa-179">nodeAddedOn</span></span></p></td>
<td><p><span data-ttu-id="718aa-180">bigint, NOT NULL</span><span class="sxs-lookup"><span data-stu-id="718aa-180">bigint, not null</span></span></p></td>
<td><p><span data-ttu-id="718aa-181">Метка времени создания узла.</span><span class="sxs-lookup"><span data-stu-id="718aa-181">Time stamp of the node creation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="718aa-182">nodeUpdatedBy</span><span class="sxs-lookup"><span data-stu-id="718aa-182">nodeUpdatedBy</span></span></p></td>
<td><p><span data-ttu-id="718aa-183">int, NOT NULL</span><span class="sxs-lookup"><span data-stu-id="718aa-183">int, not null</span></span></p></td>
<td><p><span data-ttu-id="718aa-184">Идентификатор участника, который последним обновил этот узел.</span><span class="sxs-lookup"><span data-stu-id="718aa-184">ID of the principal that did the latest update of this node.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="718aa-185">nodeUpdatedOn</span><span class="sxs-lookup"><span data-stu-id="718aa-185">nodeUpdatedOn</span></span></p></td>
<td><p><span data-ttu-id="718aa-186">bigint, NOT NULL</span><span class="sxs-lookup"><span data-stu-id="718aa-186">bigint, not null</span></span></p></td>
<td><p><span data-ttu-id="718aa-187">Метка времени последнего обновления этого узла.</span><span class="sxs-lookup"><span data-stu-id="718aa-187">Time stamp of the latest update of this node.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="718aa-188">purgedOn</span><span class="sxs-lookup"><span data-stu-id="718aa-188">purgedOn</span></span></p></td>
<td><p><span data-ttu-id="718aa-189">datetime</span><span class="sxs-lookup"><span data-stu-id="718aa-189">datetime</span></span></p></td>
<td><p><span data-ttu-id="718aa-190">Время последней операции очистки (удаления областей из таблицы tblScopedPrincipal и ролей из tblPrincipalRole таблицы), которые затронули этот узел.</span><span class="sxs-lookup"><span data-stu-id="718aa-190">Time of the latest purge operation (removal of scopes from tblScopedPrincipal table and roles from tblPrincipalRole table) that affected this node.</span></span> <span data-ttu-id="718aa-191">Это используется механизмом обновления внутреннего кэша в службе чата.</span><span class="sxs-lookup"><span data-stu-id="718aa-191">This is used by the Chat service’s internal cache update mechanism.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="718aa-192">Параметры</span><span class="sxs-lookup"><span data-stu-id="718aa-192">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="718aa-193">Столбец</span><span class="sxs-lookup"><span data-stu-id="718aa-193">Column</span></span></th>
<th><span data-ttu-id="718aa-194">Описание</span><span class="sxs-lookup"><span data-stu-id="718aa-194">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="718aa-195">nodeID</span><span class="sxs-lookup"><span data-stu-id="718aa-195">nodeID</span></span></p></td>
<td><p><span data-ttu-id="718aa-196">Первичный ключ.</span><span class="sxs-lookup"><span data-stu-id="718aa-196">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="718aa-197">расширения</span><span class="sxs-lookup"><span data-stu-id="718aa-197">behavior</span></span></p></td>
<td><p><span data-ttu-id="718aa-198">Внешний ключ с подстановкой в таблице tblEnumValue. valueID.</span><span class="sxs-lookup"><span data-stu-id="718aa-198">Foreign key with lookup in tblEnumValue.valueID table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="718aa-199">Отображение</span><span class="sxs-lookup"><span data-stu-id="718aa-199">visibility</span></span></p></td>
<td><p><span data-ttu-id="718aa-200">Внешний ключ с подстановкой в таблице tblEnumValue. valueID.</span><span class="sxs-lookup"><span data-stu-id="718aa-200">Foreign key with lookup in tblEnumValue.valueID table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="718aa-201">parentID</span><span class="sxs-lookup"><span data-stu-id="718aa-201">parentID</span></span></p></td>
<td><p><span data-ttu-id="718aa-202">Внешний ключ с подстановкой в таблице tblNode. nodeID.</span><span class="sxs-lookup"><span data-stu-id="718aa-202">Foreign key with lookup in tblNode.nodeID table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="718aa-203">siopID</span><span class="sxs-lookup"><span data-stu-id="718aa-203">siopID</span></span></p></td>
<td><p><span data-ttu-id="718aa-204">Внешний ключ с подстановкой в таблице tblSiopWhiteList. siopId.</span><span class="sxs-lookup"><span data-stu-id="718aa-204">Foreign key with lookup in tblSiopWhiteList.siopId table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="718aa-205">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="718aa-205">


</div>

<span> </span>

</div>

</div>

</span></span></div>

