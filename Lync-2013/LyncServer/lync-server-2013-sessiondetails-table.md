---
title: 'Lync Server 2013: таблица SessionDetails'
description: 'Таблица Lync Server 2013: SessionDetails.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: SessionDetails table
ms:assetid: 783d2508-e31f-4b54-be0c-63aa5ec21c04
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398589(v=OCS.15)
ms:contentKeyID: 48184559
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fd927f784fb0f2a835c896824105fe8bb112c7a1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444779"
---
# <a name="sessiondetails-table-in-lync-server-2013"></a><span data-ttu-id="7705a-103">Таблица SessionDetails в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7705a-103">SessionDetails table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7705a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7705a-104">

<span> </span></span></span>

<span data-ttu-id="7705a-105">_**Тема последнего изменения:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="7705a-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="7705a-106">Каждая запись представляет один одноранговый сеанс, и это может быть VoIP-VoIP телефонный звонок, сеанс обмена мгновенными сообщениями с двумя субъектами или сеанс другого типа.</span><span class="sxs-lookup"><span data-stu-id="7705a-106">Each record represents one peer-to-peer session, which could be a VoIP-VoIP phone call, two-party IM session, or other type of session.</span></span> <span data-ttu-id="7705a-107">Вы можете выполнить соединение таблицы с [таблицей мультимедиа в Lync Server 2013](lync-server-2013-media-table.md) , чтобы найти подробные сведения о каждом носителе, вовлеченном в этот сеанс.</span><span class="sxs-lookup"><span data-stu-id="7705a-107">You can perform a table join with the [Media table in Lync Server 2013](lync-server-2013-media-table.md) to find the details of each media involved in this session.</span></span>

<span data-ttu-id="7705a-108">Обратите внимание, что поля IsUser1IntegratedWithDeskPhone и IsUser2IntegratedWithDeskPhone удалены из таблицы SessionDetails, используемой в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="7705a-108">Note that the IsUser1IntegratedWithDeskPhone and the IsUser2IntegratedWithDeskPhone fields have been dropped from the SessionDetails table used in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7705a-109">Столбец</span><span class="sxs-lookup"><span data-stu-id="7705a-109">Column</span></span></th>
<th><span data-ttu-id="7705a-110">Тип данных</span><span class="sxs-lookup"><span data-stu-id="7705a-110">Data Type</span></span></th>
<th><span data-ttu-id="7705a-111">Ключ/индекс</span><span class="sxs-lookup"><span data-stu-id="7705a-111">Key/Index</span></span></th>
<th><span data-ttu-id="7705a-112">Сведения</span><span class="sxs-lookup"><span data-stu-id="7705a-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7705a-113"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="7705a-113"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="7705a-114">datetime</span><span class="sxs-lookup"><span data-stu-id="7705a-114">datetime</span></span></p></td>
<td><p><span data-ttu-id="7705a-115">Основной, внешний</span><span class="sxs-lookup"><span data-stu-id="7705a-115">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="7705a-116">Время запроса сеанса.</span><span class="sxs-lookup"><span data-stu-id="7705a-116">Time of session request.</span></span> <span data-ttu-id="7705a-117">Используется в сочетании с <strong>SessionIdSeq</strong> для уникальной идентификации сеанса.</span><span class="sxs-lookup"><span data-stu-id="7705a-117">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="7705a-118">Дополнительные сведения приведены <a href="lync-server-2013-dialogs-table.md">в таблице диалоговые окна Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="7705a-118">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7705a-119"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="7705a-119"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="7705a-120">целое</span><span class="sxs-lookup"><span data-stu-id="7705a-120">int</span></span></p></td>
<td><p><span data-ttu-id="7705a-121">Основной, внешний</span><span class="sxs-lookup"><span data-stu-id="7705a-121">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="7705a-122">ИДЕНТИФИКАЦИОНный номер для идентификации сеанса.</span><span class="sxs-lookup"><span data-stu-id="7705a-122">ID number to identify the session.</span></span> <span data-ttu-id="7705a-123">Используется в сочетании с <strong>SessionIdTime</strong> для уникальной идентификации сеанса. \* Дополнительные сведения можно найти <a href="lync-server-2013-dialogs-table.md">в таблице диалоговые окна Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="7705a-123">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.\* See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7705a-124"><strong>Корреляци</strong></span><span class="sxs-lookup"><span data-stu-id="7705a-124"><strong>CorrelationId</strong></span></span></p></td>
<td><p><span data-ttu-id="7705a-125">идентификатора</span><span class="sxs-lookup"><span data-stu-id="7705a-125">uniqueidentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="7705a-126">Идентификатор GUID для корреляции нескольких сеансов.</span><span class="sxs-lookup"><span data-stu-id="7705a-126">A GUID to correlate multiple sessions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7705a-127"><strong>ReplaceDialogIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="7705a-127"><strong>ReplaceDialogIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="7705a-128">datetime</span><span class="sxs-lookup"><span data-stu-id="7705a-128">datetime</span></span></p></td>
<td><p><span data-ttu-id="7705a-129">Другом</span><span class="sxs-lookup"><span data-stu-id="7705a-129">Foreign</span></span></p></td>
<td><p><span data-ttu-id="7705a-130">ИДЕНТИФИКАЦИОНный номер, определяющий диалоговое окно, которое было заменено текущим сеансом.</span><span class="sxs-lookup"><span data-stu-id="7705a-130">ID number to identify the dialog which was replaced by current session.</span></span> <span data-ttu-id="7705a-131">Дополнительные сведения приведены <a href="lync-server-2013-dialogs-table.md">в таблице диалоговые окна Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="7705a-131">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7705a-132"><strong>ReplaceDialogIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="7705a-132"><strong>ReplaceDialogIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="7705a-133">целое</span><span class="sxs-lookup"><span data-stu-id="7705a-133">int</span></span></p></td>
<td><p><span data-ttu-id="7705a-134">Другом</span><span class="sxs-lookup"><span data-stu-id="7705a-134">Foreign</span></span></p></td>
<td><p><span data-ttu-id="7705a-135">ИДЕНТИФИКАЦИОНный номер для идентификации сеанса.</span><span class="sxs-lookup"><span data-stu-id="7705a-135">ID number to identify the session.</span></span> <span data-ttu-id="7705a-136">Используется в сочетании с <strong>ReplacesDialogIdTime</strong> для уникальной идентификации сеанса, который заменяется этим сеансом.</span><span class="sxs-lookup"><span data-stu-id="7705a-136">Used in conjunction with <strong>ReplacesDialogIdTime</strong> to uniquely identify a session that is replaced by this session.</span></span> <span data-ttu-id="7705a-137">Дополнительные сведения приведены <a href="lync-server-2013-dialogs-table.md">в таблице диалоговые окна Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="7705a-137">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7705a-138"><strong>User1Id</strong></span><span class="sxs-lookup"><span data-stu-id="7705a-138"><strong>User1Id</strong></span></span></p></td>
<td><p><span data-ttu-id="7705a-139">целое</span><span class="sxs-lookup"><span data-stu-id="7705a-139">int</span></span></p></td>
<td><p><span data-ttu-id="7705a-140">Другом</span><span class="sxs-lookup"><span data-stu-id="7705a-140">Foreign</span></span></p></td>
<td><p><span data-ttu-id="7705a-141">ИДЕНТИФИКАТОР одного пользователя в сеансе.</span><span class="sxs-lookup"><span data-stu-id="7705a-141">ID of one user in the session.</span></span> <span data-ttu-id="7705a-142">Дополнительные сведения <a href="lync-server-2013-users-table.md">можно найти в таблице Users (пользователи) в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="7705a-142">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7705a-143"><strong>User2Id</strong></span><span class="sxs-lookup"><span data-stu-id="7705a-143"><strong>User2Id</strong></span></span></p></td>
<td><p><span data-ttu-id="7705a-144">целое</span><span class="sxs-lookup"><span data-stu-id="7705a-144">int</span></span></p></td>
<td><p><span data-ttu-id="7705a-145">Другом</span><span class="sxs-lookup"><span data-stu-id="7705a-145">Foreign</span></span></p></td>
<td><p><span data-ttu-id="7705a-146">ИДЕНТИФИКАТОР другого пользователя в сеансе.</span><span class="sxs-lookup"><span data-stu-id="7705a-146">ID of the other user in the session.</span></span> <span data-ttu-id="7705a-147">Дополнительные сведения <a href="lync-server-2013-users-table.md">можно найти в таблице Users (пользователи) в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="7705a-147">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7705a-148"><strong>User1EndpointId</strong></span><span class="sxs-lookup"><span data-stu-id="7705a-148"><strong>User1EndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="7705a-149">Идентификатора</span><span class="sxs-lookup"><span data-stu-id="7705a-149">uniqueIdentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="7705a-150">Идентификатор GUID, который определяет конечную точку, используемую первым пользователем сеанса.</span><span class="sxs-lookup"><span data-stu-id="7705a-150">GUID that identifies the endpoint used by the first user in the session.</span></span></p>
<p><span data-ttu-id="7705a-151">Это поле было введено в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="7705a-151">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7705a-152"><strong>User2EndpointId</strong></span><span class="sxs-lookup"><span data-stu-id="7705a-152"><strong>User2EndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="7705a-153">Идентификатора</span><span class="sxs-lookup"><span data-stu-id="7705a-153">uniqueIdentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="7705a-154">Идентификатор GUID, который определяет конечную точку, используемую вторым пользователем в сеансе.</span><span class="sxs-lookup"><span data-stu-id="7705a-154">GUID that identifies the endpoint used by the second user in the session.</span></span></p>
<p><span data-ttu-id="7705a-155">Это поле было введено в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="7705a-155">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7705a-156"><strong>TargetUserId</strong></span><span class="sxs-lookup"><span data-stu-id="7705a-156"><strong>TargetUserId</strong></span></span></p></td>
<td><p><span data-ttu-id="7705a-157">целое</span><span class="sxs-lookup"><span data-stu-id="7705a-157">int</span></span></p></td>
<td><p><span data-ttu-id="7705a-158">Другом</span><span class="sxs-lookup"><span data-stu-id="7705a-158">Foreign</span></span></p></td>
<td><p><span data-ttu-id="7705a-159">Исходный код ресурса (URI) пользователя в запросе SIP.</span><span class="sxs-lookup"><span data-stu-id="7705a-159">The original To user URI in the SIP request.</span></span> <span data-ttu-id="7705a-160">Дополнительные сведения <a href="lync-server-2013-users-table.md">можно найти в таблице Users (пользователи) в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="7705a-160">see the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7705a-161"><strong>SessionStartedById</strong></span><span class="sxs-lookup"><span data-stu-id="7705a-161"><strong>SessionStartedById</strong></span></span></p></td>
<td><p><span data-ttu-id="7705a-162">целое</span><span class="sxs-lookup"><span data-stu-id="7705a-162">int</span></span></p></td>
<td><p><span data-ttu-id="7705a-163">Другом</span><span class="sxs-lookup"><span data-stu-id="7705a-163">Foreign</span></span></p></td>
<td><p><span data-ttu-id="7705a-164">Идентификатор пользователя, запустившего сеанс.</span><span class="sxs-lookup"><span data-stu-id="7705a-164">ID of the user who started the session.</span></span> <span data-ttu-id="7705a-165">Дополнительные сведения <a href="lync-server-2013-users-table.md">можно найти в таблице Users (пользователи) в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="7705a-165">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7705a-166"><strong>OnBehalfOfId</strong></span><span class="sxs-lookup"><span data-stu-id="7705a-166"><strong>OnBehalfOfId</strong></span></span></p></td>
<td><p><span data-ttu-id="7705a-167">целое</span><span class="sxs-lookup"><span data-stu-id="7705a-167">int</span></span></p></td>
<td><p><span data-ttu-id="7705a-168">Другом</span><span class="sxs-lookup"><span data-stu-id="7705a-168">Foreign</span></span></p></td>
<td><p><span data-ttu-id="7705a-169">Идентификатор пользователя, от имени которого вызывающим абонентом является.</span><span class="sxs-lookup"><span data-stu-id="7705a-169">Indicates the ID of the user of who the caller is on behalf.</span></span> <span data-ttu-id="7705a-170">Дополнительные сведения <a href="lync-server-2013-users-table.md">можно найти в таблице Users (пользователи) в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="7705a-170">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7705a-171"><strong>ReferredById</strong></span><span class="sxs-lookup"><span data-stu-id="7705a-171"><strong>ReferredById</strong></span></span></p></td>
<td><p><span data-ttu-id="7705a-172">целое</span><span class="sxs-lookup"><span data-stu-id="7705a-172">int</span></span></p></td>
<td><p><span data-ttu-id="7705a-173">Другом</span><span class="sxs-lookup"><span data-stu-id="7705a-173">Foreign</span></span></p></td>
<td><p><span data-ttu-id="7705a-174">Идентификационный номер пользователя, на который ссылается вызов.</span><span class="sxs-lookup"><span data-stu-id="7705a-174">ID of the user by who the call is referred.</span></span> <span data-ttu-id="7705a-175">Дополнительные сведения <a href="lync-server-2013-users-table.md">можно найти в таблице Users (пользователи) в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="7705a-175">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7705a-176"><strong>ServerId</strong></span><span class="sxs-lookup"><span data-stu-id="7705a-176"><strong>ServerId</strong></span></span></p></td>
<td><p><span data-ttu-id="7705a-177">целое</span><span class="sxs-lookup"><span data-stu-id="7705a-177">int</span></span></p></td>
<td><p><span data-ttu-id="7705a-178">Другом</span><span class="sxs-lookup"><span data-stu-id="7705a-178">Foreign</span></span></p></td>
<td><p><span data-ttu-id="7705a-179">Идентификатор сервера переднего плана, используемого для этого сеанса.</span><span class="sxs-lookup"><span data-stu-id="7705a-179">ID of the front-end server used for this session.</span></span> <span data-ttu-id="7705a-180">Более подробную информацию вы видите <a href="lync-server-2013-servers-table.md">в таблице Servers (серверы) в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="7705a-180">See the <a href="lync-server-2013-servers-table.md">Servers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7705a-181"><strong>PoolId</strong></span><span class="sxs-lookup"><span data-stu-id="7705a-181"><strong>PoolId</strong></span></span></p></td>
<td><p><span data-ttu-id="7705a-182">целое</span><span class="sxs-lookup"><span data-stu-id="7705a-182">int</span></span></p></td>
<td><p><span data-ttu-id="7705a-183">Другом</span><span class="sxs-lookup"><span data-stu-id="7705a-183">Foreign</span></span></p></td>
<td><p><span data-ttu-id="7705a-184">Идентификатор пула, в котором был собран сеанс.</span><span class="sxs-lookup"><span data-stu-id="7705a-184">ID of the pool in which the session was captured.</span></span> <span data-ttu-id="7705a-185">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-pools-table.md">таблицей пулы в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="7705a-185">See the <a href="lync-server-2013-pools-table.md">Pools table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7705a-186"><strong>ContentTypeID</strong></span><span class="sxs-lookup"><span data-stu-id="7705a-186"><strong>ContentTypeID</strong></span></span></p></td>
<td><p><span data-ttu-id="7705a-187">целое</span><span class="sxs-lookup"><span data-stu-id="7705a-187">int</span></span></p></td>
<td><p><span data-ttu-id="7705a-188">Другом</span><span class="sxs-lookup"><span data-stu-id="7705a-188">Foreign</span></span></p></td>
<td><p><span data-ttu-id="7705a-189">Тип контента, используемый в сеансе.</span><span class="sxs-lookup"><span data-stu-id="7705a-189">Content type used in the session.</span></span> <span data-ttu-id="7705a-190">Дополнительные сведения приведены <a href="lync-server-2013-contenttypes-table.md">в таблице ContentTypes в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="7705a-190">See the <a href="lync-server-2013-contenttypes-table.md">ContentTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7705a-191"><strong>User1ClientVerId</strong></span><span class="sxs-lookup"><span data-stu-id="7705a-191"><strong>User1ClientVerId</strong></span></span></p></td>
<td><p><span data-ttu-id="7705a-192">целое</span><span class="sxs-lookup"><span data-stu-id="7705a-192">int</span></span></p></td>
<td><p><span data-ttu-id="7705a-193">Другом</span><span class="sxs-lookup"><span data-stu-id="7705a-193">Foreign</span></span></p></td>
<td><p><span data-ttu-id="7705a-194">Версия клиента, используемая Пользователь1.</span><span class="sxs-lookup"><span data-stu-id="7705a-194">Client version used by User1.</span></span> <span data-ttu-id="7705a-195">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-clientversions-table.md">таблицей ClientVersions в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="7705a-195">See the <a href="lync-server-2013-clientversions-table.md">ClientVersions table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7705a-196"><strong>User2ClientVerId</strong></span><span class="sxs-lookup"><span data-stu-id="7705a-196"><strong>User2ClientVerId</strong></span></span></p></td>
<td><p><span data-ttu-id="7705a-197">целое</span><span class="sxs-lookup"><span data-stu-id="7705a-197">int</span></span></p></td>
<td><p><span data-ttu-id="7705a-198">Другом</span><span class="sxs-lookup"><span data-stu-id="7705a-198">Foreign</span></span></p></td>
<td><p><span data-ttu-id="7705a-199">Версия клиента, используемая Пользователь2.</span><span class="sxs-lookup"><span data-stu-id="7705a-199">Client version used by User2.</span></span> <span data-ttu-id="7705a-200">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-clientversions-table.md">таблицей ClientVersions в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="7705a-200">See the <a href="lync-server-2013-clientversions-table.md">ClientVersions table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7705a-201"><strong>User1EdgeServerid</strong></span><span class="sxs-lookup"><span data-stu-id="7705a-201"><strong>User1EdgeServerid</strong></span></span></p></td>
<td><p><span data-ttu-id="7705a-202">целое</span><span class="sxs-lookup"><span data-stu-id="7705a-202">int</span></span></p></td>
<td><p><span data-ttu-id="7705a-203">Другом</span><span class="sxs-lookup"><span data-stu-id="7705a-203">Foreign</span></span></p></td>
<td><p><span data-ttu-id="7705a-204">Пограничный сервер, используемый Пользователь1.</span><span class="sxs-lookup"><span data-stu-id="7705a-204">Edge Server used by User1.</span></span> <span data-ttu-id="7705a-205">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-edgeservers-table.md">таблицей EdgeServers в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="7705a-205">See the <a href="lync-server-2013-edgeservers-table.md">EdgeServers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7705a-206"><strong>User2EdgeServerid</strong></span><span class="sxs-lookup"><span data-stu-id="7705a-206"><strong>User2EdgeServerid</strong></span></span></p></td>
<td><p><span data-ttu-id="7705a-207">целое</span><span class="sxs-lookup"><span data-stu-id="7705a-207">int</span></span></p></td>
<td><p><span data-ttu-id="7705a-208">Другом</span><span class="sxs-lookup"><span data-stu-id="7705a-208">Foreign</span></span></p></td>
<td><p><span data-ttu-id="7705a-209">Пограничный сервер, используемый Пользователь2.</span><span class="sxs-lookup"><span data-stu-id="7705a-209">Edge Server used by User2.</span></span> <span data-ttu-id="7705a-210">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-edgeservers-table.md">таблицей EdgeServers в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="7705a-210">See the <a href="lync-server-2013-edgeservers-table.md">EdgeServers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7705a-211"><strong>IsUser1Internal</strong></span><span class="sxs-lookup"><span data-stu-id="7705a-211"><strong>IsUser1Internal</strong></span></span></p></td>
<td><p><span data-ttu-id="7705a-212">бит</span><span class="sxs-lookup"><span data-stu-id="7705a-212">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="7705a-213">Есть ли у пользователя Пользователь1 вход из внутренней сети или нет.</span><span class="sxs-lookup"><span data-stu-id="7705a-213">Whether User1 is logged on from internal or not.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7705a-214"><strong>IsUser2Internal</strong></span><span class="sxs-lookup"><span data-stu-id="7705a-214"><strong>IsUser2Internal</strong></span></span></p></td>
<td><p><span data-ttu-id="7705a-215">бит</span><span class="sxs-lookup"><span data-stu-id="7705a-215">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="7705a-216">, Вошел ли Пользователь2 из внутреннего или нет.</span><span class="sxs-lookup"><span data-stu-id="7705a-216">Whether User2 is logged on from internal or not.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7705a-217"><strong>InviteTime</strong></span><span class="sxs-lookup"><span data-stu-id="7705a-217"><strong>InviteTime</strong></span></span></p></td>
<td><p><span data-ttu-id="7705a-218">datetime</span><span class="sxs-lookup"><span data-stu-id="7705a-218">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="7705a-219">Время первого запроса приглашения.</span><span class="sxs-lookup"><span data-stu-id="7705a-219">The time of the first INVITE request.</span></span> <span data-ttu-id="7705a-220">Это поле обычно заполняется данными, созданными на основе исходного сообщения INVITE в сеансе.</span><span class="sxs-lookup"><span data-stu-id="7705a-220">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="7705a-221">Если сообщение приглашения отсутствует, поле заполняется датой и временем первого соответствующего сообщения SIP (пока, CANCEL, MESSAGE или INFO).</span><span class="sxs-lookup"><span data-stu-id="7705a-221">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span> <span data-ttu-id="7705a-222">Это поле обычно заполняется данными, созданными на основе исходного сообщения INVITE в сеансе.</span><span class="sxs-lookup"><span data-stu-id="7705a-222">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="7705a-223">Если сообщение приглашения отсутствует, поле заполняется датой и временем первого соответствующего сообщения SIP (пока, CANCEL, MESSAGE или INFO).</span><span class="sxs-lookup"><span data-stu-id="7705a-223">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7705a-224"><strong>ResponseTime</strong></span><span class="sxs-lookup"><span data-stu-id="7705a-224"><strong>ResponseTime</strong></span></span></p></td>
<td><p><span data-ttu-id="7705a-225">datetime</span><span class="sxs-lookup"><span data-stu-id="7705a-225">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="7705a-226">Время ответа на первое сообщение приглашения.</span><span class="sxs-lookup"><span data-stu-id="7705a-226">The time of the response to the first INVITE message.</span></span> <span data-ttu-id="7705a-227">Это поле обычно заполняется данными, созданными на основе исходного сообщения INVITE в сеансе.</span><span class="sxs-lookup"><span data-stu-id="7705a-227">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="7705a-228">Если сообщение приглашения отсутствует, поле заполняется датой и временем первого соответствующего сообщения SIP (пока, CANCEL, MESSAGE или INFO).</span><span class="sxs-lookup"><span data-stu-id="7705a-228">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7705a-229"><strong>ResponseCode</strong></span><span class="sxs-lookup"><span data-stu-id="7705a-229"><strong>ResponseCode</strong></span></span></p></td>
<td><p><span data-ttu-id="7705a-230">целое</span><span class="sxs-lookup"><span data-stu-id="7705a-230">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="7705a-231">Код ответа SIP на приглашение на сеанс.</span><span class="sxs-lookup"><span data-stu-id="7705a-231">SIP response code to the session invitation.</span></span> <span data-ttu-id="7705a-232">Это поле обычно заполняется данными, созданными на основе исходного сообщения INVITE в сеансе.</span><span class="sxs-lookup"><span data-stu-id="7705a-232">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="7705a-233">Если сообщение приглашения отсутствует, поле заполняется датой и временем первого соответствующего сообщения SIP (пока, CANCEL, MESSAGE или INFO).</span><span class="sxs-lookup"><span data-stu-id="7705a-233">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7705a-234"><strong>DiagnosticId</strong></span><span class="sxs-lookup"><span data-stu-id="7705a-234"><strong>DiagnosticId</strong></span></span></p></td>
<td><p><span data-ttu-id="7705a-235">целое</span><span class="sxs-lookup"><span data-stu-id="7705a-235">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="7705a-236">Идентификатор диагностики, полученный в заголовке SIP.</span><span class="sxs-lookup"><span data-stu-id="7705a-236">Diagnostic ID captured from SIP header.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7705a-237"><strong>CallPriority</strong></span><span class="sxs-lookup"><span data-stu-id="7705a-237"><strong>CallPriority</strong></span></span></p></td>
<td><p><span data-ttu-id="7705a-238">целое</span><span class="sxs-lookup"><span data-stu-id="7705a-238">int</span></span></p></td>
<td><p><span data-ttu-id="7705a-239">Другом</span><span class="sxs-lookup"><span data-stu-id="7705a-239">Foreign</span></span></p></td>
<td><p><span data-ttu-id="7705a-240">Приоритет звонка.</span><span class="sxs-lookup"><span data-stu-id="7705a-240">Call priority.</span></span> <span data-ttu-id="7705a-241">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-callpriorities-table.md">таблицей CallPriorities в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="7705a-241">See the <a href="lync-server-2013-callpriorities-table.md">CallPriorities table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7705a-242"><strong>User1MessageCount</strong></span><span class="sxs-lookup"><span data-stu-id="7705a-242"><strong>User1MessageCount</strong></span></span></p></td>
<td><p><span data-ttu-id="7705a-243">целое</span><span class="sxs-lookup"><span data-stu-id="7705a-243">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="7705a-244">Количество сообщений, отправленных Пользователь1 в течение сеанса.</span><span class="sxs-lookup"><span data-stu-id="7705a-244">Number of messages sent by User1 during the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7705a-245"><strong>User2MessageCount</strong></span><span class="sxs-lookup"><span data-stu-id="7705a-245"><strong>User2MessageCount</strong></span></span></p></td>
<td><p><span data-ttu-id="7705a-246">целое</span><span class="sxs-lookup"><span data-stu-id="7705a-246">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="7705a-247">Количество сообщений, отправленных Пользователь2 во время сеанса.</span><span class="sxs-lookup"><span data-stu-id="7705a-247">Number of messages sent by User2 during the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7705a-248"><strong>SessionEndTime</strong></span><span class="sxs-lookup"><span data-stu-id="7705a-248"><strong>SessionEndTime</strong></span></span></p></td>
<td><p><span data-ttu-id="7705a-249">datetime</span><span class="sxs-lookup"><span data-stu-id="7705a-249">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="7705a-250">Время окончания сеанса.</span><span class="sxs-lookup"><span data-stu-id="7705a-250">Time at the end of the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7705a-251"><strong>MediaTypes</strong></span><span class="sxs-lookup"><span data-stu-id="7705a-251"><strong>MediaTypes</strong></span></span></p></td>
<td><p><span data-ttu-id="7705a-252">целое</span><span class="sxs-lookup"><span data-stu-id="7705a-252">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="7705a-253">Битовый набор, указывающий тип мультимедиа для этого сеанса.</span><span class="sxs-lookup"><span data-stu-id="7705a-253">A bit set that indicates the media type of this session.</span></span> <span data-ttu-id="7705a-254">Ниже перечислены определения типов.</span><span class="sxs-lookup"><span data-stu-id="7705a-254">Listed are the definitions of the types:</span></span></p>
<h3 id="section-1"> </h3>
<div>
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7705a-255">Сообщения</span><span class="sxs-lookup"><span data-stu-id="7705a-255">IM</span></span></p></td>
<td><p><span data-ttu-id="7705a-256">1</span><span class="sxs-lookup"><span data-stu-id="7705a-256">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7705a-257">FILE_TRANSFER</span><span class="sxs-lookup"><span data-stu-id="7705a-257">FILE_TRANSFER</span></span></p></td>
<td><p><span data-ttu-id="7705a-258">2</span><span class="sxs-lookup"><span data-stu-id="7705a-258">2</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7705a-259">REMOTE_ASSISTANCE</span><span class="sxs-lookup"><span data-stu-id="7705a-259">REMOTE_ASSISTANCE</span></span></p></td>
<td><p><span data-ttu-id="7705a-260">4</span><span class="sxs-lookup"><span data-stu-id="7705a-260">4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7705a-261">APP_SHARING</span><span class="sxs-lookup"><span data-stu-id="7705a-261">APP_SHARING</span></span></p></td>
<td><p><span data-ttu-id="7705a-262">No8</span><span class="sxs-lookup"><span data-stu-id="7705a-262">8</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7705a-263">ЗВУКОВ</span><span class="sxs-lookup"><span data-stu-id="7705a-263">AUDIO</span></span></p></td>
<td><p><span data-ttu-id="7705a-264">шестнадцат</span><span class="sxs-lookup"><span data-stu-id="7705a-264">16</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7705a-265">ВИЗУАЛИЗАЦИИ</span><span class="sxs-lookup"><span data-stu-id="7705a-265">VIDEO</span></span></p></td>
<td><p><span data-ttu-id="7705a-266">32</span><span class="sxs-lookup"><span data-stu-id="7705a-266">32</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7705a-267">APP_INVITE</span><span class="sxs-lookup"><span data-stu-id="7705a-267">APP_INVITE</span></span></p></td>
<td><p><span data-ttu-id="7705a-268">64</span><span class="sxs-lookup"><span data-stu-id="7705a-268">64</span></span></p></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7705a-269"><strong>User1Flag</strong></span><span class="sxs-lookup"><span data-stu-id="7705a-269"><strong>User1Flag</strong></span></span></p></td>
<td><p><span data-ttu-id="7705a-270">smallint</span><span class="sxs-lookup"><span data-stu-id="7705a-270">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="7705a-271">Битовый набор, обозначающий атрибуты User1.</span><span class="sxs-lookup"><span data-stu-id="7705a-271">A bit set that indicates the User1 attributes.</span></span> <span data-ttu-id="7705a-272">Следующие определения атрибутов перечислены ниже.</span><span class="sxs-lookup"><span data-stu-id="7705a-272">The following attribute definitions are listed:</span></span></p>
<ul>
<li><p><span data-ttu-id="7705a-273">0x01 — интеграция с настольным телефоном</span><span class="sxs-lookup"><span data-stu-id="7705a-273">0x01 - Integrated with desktop phone</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7705a-274"><strong>User2Flag</strong></span><span class="sxs-lookup"><span data-stu-id="7705a-274"><strong>User2Flag</strong></span></span></p></td>
<td><p><span data-ttu-id="7705a-275">smallint</span><span class="sxs-lookup"><span data-stu-id="7705a-275">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="7705a-276">Битовый набор, обозначающий атрибуты Пользователь2.</span><span class="sxs-lookup"><span data-stu-id="7705a-276">A bit set that indicates the User2 attributes.</span></span> <span data-ttu-id="7705a-277">Следующие определения атрибутов перечислены ниже.</span><span class="sxs-lookup"><span data-stu-id="7705a-277">The following attribute definitions are listed:</span></span></p>
<ul>
<li><p><span data-ttu-id="7705a-278">0x01 — интеграция с настольным телефоном</span><span class="sxs-lookup"><span data-stu-id="7705a-278">0x01 - Integrated with desktop phone</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7705a-279"><strong>CallFlag</strong></span><span class="sxs-lookup"><span data-stu-id="7705a-279"><strong>CallFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="7705a-280">smallint</span><span class="sxs-lookup"><span data-stu-id="7705a-280">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="7705a-281">Битовый набор, обозначающий атрибуты вызова.</span><span class="sxs-lookup"><span data-stu-id="7705a-281">A bit set that indicates the call attributes.</span></span> <span data-ttu-id="7705a-282">Следующие определения атрибутов перечислены ниже.</span><span class="sxs-lookup"><span data-stu-id="7705a-282">The following attribute definitions are listed:</span></span></p>
<ul>
<li><p><span data-ttu-id="7705a-283">0x01 — сеанс повторной попытки</span><span class="sxs-lookup"><span data-stu-id="7705a-283">0x01 - Retried Session</span></span></p></li>
<li><p><span data-ttu-id="7705a-284">0x02 — вызов, сделанный агентом от имени группы ответа</span><span class="sxs-lookup"><span data-stu-id="7705a-284">0x02 - A call made by agent on behalf of a response group</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7705a-285"><strong>Обработка</strong></span><span class="sxs-lookup"><span data-stu-id="7705a-285"><strong>Processed</strong></span></span></p></td>
<td><p><span data-ttu-id="7705a-286">бит</span><span class="sxs-lookup"><span data-stu-id="7705a-286">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="7705a-287">Для внутреннего использования службой мониторинга.</span><span class="sxs-lookup"><span data-stu-id="7705a-287">For internal use by the Monitoring service.</span></span></p>
<p><span data-ttu-id="7705a-288">Это поле было введено в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="7705a-288">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7705a-289">\* Для большинства сеансов для SessionIdSeq будет задано значение 1.</span><span class="sxs-lookup"><span data-stu-id="7705a-289">\* For most sessions, SessionIdSeq will have the value of 1.</span></span> <span data-ttu-id="7705a-290">Если несколько сеансов начинаются в одно и то же время, SessionIdSeq для одного из них будет равен 1, а для другого — 2 и т. д.</span><span class="sxs-lookup"><span data-stu-id="7705a-290">If multiple sessions start at exactly the same time, the SessionIdSeq for one will be 1, for another will be 2, and so on.</span></span>

<span data-ttu-id="7705a-291"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7705a-291"></div>

<span> </span>

</div>

</div>

</span></span></div>

