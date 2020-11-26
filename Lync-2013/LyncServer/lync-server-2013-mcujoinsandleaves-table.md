---
title: 'Lync Server 2013: таблица McuJoinsAndLeaves'
description: 'Таблица Lync Server 2013: McuJoinsAndLeaves.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: McuJoinsAndLeaves table
ms:assetid: 4e073366-0b5d-45b4-a3f6-d63dd5fd9f25
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398316(v=OCS.15)
ms:contentKeyID: 48184115
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ee7d9473892ac357dcefd80b0d52382c5dd7d930
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425754"
---
# <a name="mcujoinsandleaves-table-in-lync-server-2013"></a><span data-ttu-id="6ac67-103">Таблица McuJoinsAndLeaves в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6ac67-103">McuJoinsAndLeaves table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6ac67-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6ac67-104">

<span> </span></span></span>

<span data-ttu-id="6ac67-105">_**Тема последнего изменения:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="6ac67-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="6ac67-106">Каждая запись в этой таблице включает сведения о звонках для одной комбинации присоединения или выхода из нее и сервера конференций.</span><span class="sxs-lookup"><span data-stu-id="6ac67-106">Each record in this table contains call details about one combination of a user join or leave and conferencing server.</span></span> <span data-ttu-id="6ac67-107">Например, если пользователь присоединяется к Конференции, которая включает веб-конференции и звуковые и видеоэлементы, для подключения к веб-конференции пользователя будет создана одна запись, а для голосовых и видеоконференций пользователя будет создана другая запись.</span><span class="sxs-lookup"><span data-stu-id="6ac67-107">For example, if a user joins a conference that includes web conferencing and audio/video elements, one record would be created for that user’s web conferencing join, and another record would be created for the user’s audio/video conferencing join.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6ac67-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="6ac67-108">Column</span></span></th>
<th><span data-ttu-id="6ac67-109">Тип данных</span><span class="sxs-lookup"><span data-stu-id="6ac67-109">Data Type</span></span></th>
<th><span data-ttu-id="6ac67-110">Ключ/индекс</span><span class="sxs-lookup"><span data-stu-id="6ac67-110">Key/Index</span></span></th>
<th><span data-ttu-id="6ac67-111">Сведения</span><span class="sxs-lookup"><span data-stu-id="6ac67-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6ac67-112"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="6ac67-112"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="6ac67-113">datetime</span><span class="sxs-lookup"><span data-stu-id="6ac67-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="6ac67-114">Основной, внешний</span><span class="sxs-lookup"><span data-stu-id="6ac67-114">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="6ac67-115">Время экземпляра Конференции.</span><span class="sxs-lookup"><span data-stu-id="6ac67-115">Time of conference instance.</span></span> <span data-ttu-id="6ac67-116">Используется в сочетании с <strong>SessionIdSeq</strong> для уникальной идентификации экземпляра Конференции.</span><span class="sxs-lookup"><span data-stu-id="6ac67-116">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a conference instance.</span></span> <span data-ttu-id="6ac67-117">Дополнительные сведения приведены <a href="lync-server-2013-conferences-table.md">в таблице конференции для Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="6ac67-117">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ac67-118"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="6ac67-118"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="6ac67-119">целое</span><span class="sxs-lookup"><span data-stu-id="6ac67-119">int</span></span></p></td>
<td><p><span data-ttu-id="6ac67-120">Основной, внешний</span><span class="sxs-lookup"><span data-stu-id="6ac67-120">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="6ac67-121">ИДЕНТИФИКАЦИОНный номер для идентификации экземпляра Конференции.</span><span class="sxs-lookup"><span data-stu-id="6ac67-121">ID number to identify the conference instance.</span></span> <span data-ttu-id="6ac67-122">Используется в сочетании с <strong>SessionIdTime</strong> для уникальной идентификации экземпляра Конференции.</span><span class="sxs-lookup"><span data-stu-id="6ac67-122">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a conference instance.</span></span> <span data-ttu-id="6ac67-123">Дополнительные сведения приведены <a href="lync-server-2013-conferences-table.md">в таблице конференции для Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="6ac67-123">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ac67-124"><strong>Идентификатора пользователя</strong></span><span class="sxs-lookup"><span data-stu-id="6ac67-124"><strong>UserId</strong></span></span></p></td>
<td><p><span data-ttu-id="6ac67-125">целое</span><span class="sxs-lookup"><span data-stu-id="6ac67-125">int</span></span></p></td>
<td><p><span data-ttu-id="6ac67-126">Основной, внешний</span><span class="sxs-lookup"><span data-stu-id="6ac67-126">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="6ac67-127">Уникальный номер, идентифицирующий этого пользователя.</span><span class="sxs-lookup"><span data-stu-id="6ac67-127">Unique number identifying this user.</span></span> <span data-ttu-id="6ac67-128">Дополнительные сведения <a href="lync-server-2013-users-table.md">можно найти в таблице Users (пользователи) в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="6ac67-128">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ac67-129"><strong>McuUserInstance</strong></span><span class="sxs-lookup"><span data-stu-id="6ac67-129"><strong>McuUserInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="6ac67-130">целое</span><span class="sxs-lookup"><span data-stu-id="6ac67-130">int</span></span></p></td>
<td><p><span data-ttu-id="6ac67-131">Primary</span><span class="sxs-lookup"><span data-stu-id="6ac67-131">Primary</span></span></p></td>
<td><p><span data-ttu-id="6ac67-132">Если пользователь входит в систему на нескольких компьютерах или устройствах одновременно, McuUserInstance однозначно определяет сочетание пользователей и устройств.</span><span class="sxs-lookup"><span data-stu-id="6ac67-132">If a user is logged on at multiple computers or devices at once, McuUserInstance uniquely identifies the user/device combination.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ac67-133"><strong>IsFromPstn</strong></span><span class="sxs-lookup"><span data-stu-id="6ac67-133"><strong>IsFromPstn</strong></span></span></p></td>
<td><p><span data-ttu-id="6ac67-134">бит</span><span class="sxs-lookup"><span data-stu-id="6ac67-134">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6ac67-135">Присоединение пользователя к сети PSTN или нет.</span><span class="sxs-lookup"><span data-stu-id="6ac67-135">Whether the user is joining from a PSTN or not.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ac67-136"><strong>McuId</strong></span><span class="sxs-lookup"><span data-stu-id="6ac67-136"><strong>McuId</strong></span></span></p></td>
<td><p><span data-ttu-id="6ac67-137">целое</span><span class="sxs-lookup"><span data-stu-id="6ac67-137">int</span></span></p></td>
<td><p><span data-ttu-id="6ac67-138">Основной, внешний</span><span class="sxs-lookup"><span data-stu-id="6ac67-138">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="6ac67-139">Уникальный номер, идентифицирующий этот сервер конференц-связи.</span><span class="sxs-lookup"><span data-stu-id="6ac67-139">Unique number identifying this conferencing server.</span></span> <span data-ttu-id="6ac67-140">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-mcus-table.md">таблицей MCUs в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="6ac67-140">See the <a href="lync-server-2013-mcus-table.md">Mcus table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ac67-141"><strong>DialogSessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="6ac67-141"><strong>DialogSessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="6ac67-142">datetime</span><span class="sxs-lookup"><span data-stu-id="6ac67-142">datetime</span></span></p></td>
<td><p><span data-ttu-id="6ac67-143">Другом</span><span class="sxs-lookup"><span data-stu-id="6ac67-143">Foreign</span></span></p></td>
<td><p><span data-ttu-id="6ac67-144">Время запроса сеанса.</span><span class="sxs-lookup"><span data-stu-id="6ac67-144">Time of session request.</span></span> <span data-ttu-id="6ac67-145">Используется в сочетании с <strong>SessionIdSeq</strong> для уникальной идентификации сеанса.</span><span class="sxs-lookup"><span data-stu-id="6ac67-145">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="6ac67-146">Дополнительные сведения приведены <a href="lync-server-2013-dialogs-table.md">в таблице диалоговые окна Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="6ac67-146">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ac67-147"><strong>DialogSessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="6ac67-147"><strong>DialogSessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="6ac67-148">целое</span><span class="sxs-lookup"><span data-stu-id="6ac67-148">int</span></span></p></td>
<td><p><span data-ttu-id="6ac67-149">Другом</span><span class="sxs-lookup"><span data-stu-id="6ac67-149">Foreign</span></span></p></td>
<td><p><span data-ttu-id="6ac67-150">ИДЕНТИФИКАЦИОНный номер для идентификации сеанса.</span><span class="sxs-lookup"><span data-stu-id="6ac67-150">ID number to identify the session.</span></span> <span data-ttu-id="6ac67-151">Используется в сочетании с <strong>SessionIdTime</strong> для уникальной идентификации сеанса.</span><span class="sxs-lookup"><span data-stu-id="6ac67-151">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.</span></span> <span data-ttu-id="6ac67-152">Дополнительные сведения приведены <a href="lync-server-2013-dialogs-table.md">в таблице диалоговые окна Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="6ac67-152">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ac67-153"><strong>UserJoinTime</strong></span><span class="sxs-lookup"><span data-stu-id="6ac67-153"><strong>UserJoinTime</strong></span></span></p></td>
<td><p><span data-ttu-id="6ac67-154">datetime</span><span class="sxs-lookup"><span data-stu-id="6ac67-154">datetime</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6ac67-155">Время присоединения пользователя к этому серверу конференций.</span><span class="sxs-lookup"><span data-stu-id="6ac67-155">The time this user joins this conferencing server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ac67-156"><strong>UserLeaveTime</strong></span><span class="sxs-lookup"><span data-stu-id="6ac67-156"><strong>UserLeaveTime</strong></span></span></p></td>
<td><p><span data-ttu-id="6ac67-157">datetime</span><span class="sxs-lookup"><span data-stu-id="6ac67-157">datetime</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6ac67-158">Время, когда этот пользователь покидает этот сервер конференц-связи.</span><span class="sxs-lookup"><span data-stu-id="6ac67-158">The time this user leaves this conferencing server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ac67-159"><strong>ClientVerId</strong></span><span class="sxs-lookup"><span data-stu-id="6ac67-159"><strong>ClientVerId</strong></span></span></p></td>
<td><p><span data-ttu-id="6ac67-160">целое</span><span class="sxs-lookup"><span data-stu-id="6ac67-160">int</span></span></p></td>
<td><p><span data-ttu-id="6ac67-161">Другом</span><span class="sxs-lookup"><span data-stu-id="6ac67-161">Foreign</span></span></p></td>
<td><p><span data-ttu-id="6ac67-162">Идентификатор, указывающий номер версии клиентского программного обеспечения, используемого на Конференции.</span><span class="sxs-lookup"><span data-stu-id="6ac67-162">Identifier that specifies the version number of the client software use in the conference.</span></span> <span data-ttu-id="6ac67-163">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-clientversions-table.md">таблицей ClientVersions в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="6ac67-163">See the <a href="lync-server-2013-clientversions-table.md">ClientVersions table in Lync Server 2013</a> for more information.</span></span></p>
<p><span data-ttu-id="6ac67-164">Это поле было введено в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6ac67-164">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="6ac67-165">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6ac67-165">


</div>

<span> </span>

</div>

</div>

</span></span></div>

