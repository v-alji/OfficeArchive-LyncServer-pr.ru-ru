---
title: 'Lync Server 2013: таблица ConferenceSessionDetails'
description: 'Таблица Lync Server 2013: ConferenceSessionDetails.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ConferenceSessionDetails table
ms:assetid: 9eae6a54-69fd-4966-aa17-7ecee1297ad8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412741(v=OCS.15)
ms:contentKeyID: 48184925
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0d101eb1607e366ab814e60acaeee80820fe87c5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434419"
---
# <a name="conferencesessiondetails-table-in-lync-server-2013"></a><span data-ttu-id="b6456-103">Таблица ConferenceSessionDetails в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b6456-103">ConferenceSessionDetails table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b6456-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b6456-104">

<span> </span></span></span>

<span data-ttu-id="b6456-105">_**Тема последнего изменения:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="b6456-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="b6456-106">Каждая запись представляет один сеанс конференции, который может быть либо сеансом с фокусом, либо сеансом с определенным сервером конференц-связи.</span><span class="sxs-lookup"><span data-stu-id="b6456-106">Each record represents one conference session, which could be either the session with Focus or the session with a specific conferencing server.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b6456-107">Столбец</span><span class="sxs-lookup"><span data-stu-id="b6456-107">Column</span></span></th>
<th><span data-ttu-id="b6456-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="b6456-108">Data Type</span></span></th>
<th><span data-ttu-id="b6456-109">Ключ/индекс</span><span class="sxs-lookup"><span data-stu-id="b6456-109">Key/Index</span></span></th>
<th><span data-ttu-id="b6456-110">Сведения</span><span class="sxs-lookup"><span data-stu-id="b6456-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b6456-111"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="b6456-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="b6456-112">Датой</span><span class="sxs-lookup"><span data-stu-id="b6456-112">Datetime</span></span></p></td>
<td><p><span data-ttu-id="b6456-113">Основной, внешний</span><span class="sxs-lookup"><span data-stu-id="b6456-113">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="b6456-114">Время запроса сеанса; используется в сочетании с <strong>SessionIdSeq</strong> для уникальной идентификации сеанса конференц-связи.</span><span class="sxs-lookup"><span data-stu-id="b6456-114">Time of session request; used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a conference session.</span></span> <span data-ttu-id="b6456-115">Дополнительные сведения приведены <a href="lync-server-2013-dialogs-table.md">в таблице диалоговые окна Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="b6456-115">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6456-116"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="b6456-116"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="b6456-117">целое</span><span class="sxs-lookup"><span data-stu-id="b6456-117">int</span></span></p></td>
<td><p><span data-ttu-id="b6456-118">Основной, внешний</span><span class="sxs-lookup"><span data-stu-id="b6456-118">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="b6456-119">ИДЕНТИФИКАЦИОНный номер для идентификации сеанса.</span><span class="sxs-lookup"><span data-stu-id="b6456-119">ID number to identify the session.</span></span> <span data-ttu-id="b6456-120">Используется в сочетании с <strong>SessionIdTime</strong> для уникальной идентификации сеанса конференц-связи.</span><span class="sxs-lookup"><span data-stu-id="b6456-120">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a conference session.</span></span> <span data-ttu-id="b6456-121">Дополнительные сведения приведены <a href="lync-server-2013-dialogs-table.md">в таблице диалоговые окна Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="b6456-121">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span> *</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b6456-122"><strong>ConferenceUriId</strong></span><span class="sxs-lookup"><span data-stu-id="b6456-122"><strong>ConferenceUriId</strong></span></span></p></td>
<td><p><span data-ttu-id="b6456-123">целое</span><span class="sxs-lookup"><span data-stu-id="b6456-123">int</span></span></p></td>
<td><p><span data-ttu-id="b6456-124">Другом</span><span class="sxs-lookup"><span data-stu-id="b6456-124">Foreign</span></span></p></td>
<td><p><span data-ttu-id="b6456-125">КОД URI конференции Focus, связанный с этим сеансом.</span><span class="sxs-lookup"><span data-stu-id="b6456-125">Focus conference URI related to this session.</span></span> <span data-ttu-id="b6456-126">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-conferenceuris-table.md">таблицей ConferenceUris в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="b6456-126">See the <a href="lync-server-2013-conferenceuris-table.md">ConferenceUris table in Lync Server 2013</a> for more information.</span></span> <span data-ttu-id="b6456-127">Этот URI является универсальным кодом ресурса конференции на основе фокуса.</span><span class="sxs-lookup"><span data-stu-id="b6456-127">This URI is a Focus-based conference URI.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6456-128"><strong>ConfInstance</strong></span><span class="sxs-lookup"><span data-stu-id="b6456-128"><strong>ConfInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="b6456-129">Идентификатора</span><span class="sxs-lookup"><span data-stu-id="b6456-129">uniqueIdentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b6456-130">Идентификатор, отличающийся между экземплярами повторяющихся конференций.</span><span class="sxs-lookup"><span data-stu-id="b6456-130">Identifier that differentiates between instances of recurring conferences.</span></span> <span data-ttu-id="b6456-131">Каждый экземпляр повторяющейся Конференции имеет один и тот же ConferenceURI, но другое значение ConfInstance.</span><span class="sxs-lookup"><span data-stu-id="b6456-131">Each recurring conference instance has the same ConferenceURI but a different ConfInstance value.</span></span></p>
<p><span data-ttu-id="b6456-132">Это поле было введено в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b6456-132">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b6456-133"><strong>McuConferenceUriId</strong></span><span class="sxs-lookup"><span data-stu-id="b6456-133"><strong>McuConferenceUriId</strong></span></span></p></td>
<td><p><span data-ttu-id="b6456-134">целое</span><span class="sxs-lookup"><span data-stu-id="b6456-134">int</span></span></p></td>
<td><p><span data-ttu-id="b6456-135">Другом</span><span class="sxs-lookup"><span data-stu-id="b6456-135">Foreign</span></span></p></td>
<td><p><span data-ttu-id="b6456-136">URI конференции сервера конференций, связанный с этим сеансом.</span><span class="sxs-lookup"><span data-stu-id="b6456-136">Conferencing server conference URI related to this session.</span></span> <span data-ttu-id="b6456-137">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-conferenceuris-table.md">таблицей ConferenceUris в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="b6456-137">See the <a href="lync-server-2013-conferenceuris-table.md">ConferenceUris table in Lync Server 2013</a> for more information.</span></span> <span data-ttu-id="b6456-138">Этот универсальный код ресурса (URI) Конференции на базе сервера конференций.</span><span class="sxs-lookup"><span data-stu-id="b6456-138">This URI is the conferencing server-based conference URI.</span></span> <span data-ttu-id="b6456-139">Для сеансов опроса в фокусе этот столбец будет иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="b6456-139">For Focus conference sessions, this column will be null.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6456-140"><strong>Идентификатора пользователя</strong></span><span class="sxs-lookup"><span data-stu-id="b6456-140"><strong>UserId</strong></span></span></p></td>
<td><p><span data-ttu-id="b6456-141">целое</span><span class="sxs-lookup"><span data-stu-id="b6456-141">int</span></span></p></td>
<td><p><span data-ttu-id="b6456-142">Другом</span><span class="sxs-lookup"><span data-stu-id="b6456-142">Foreign</span></span></p></td>
<td><p><span data-ttu-id="b6456-143">ИДЕНТИФИКАТОР одного пользователя в сеансе Конференции.</span><span class="sxs-lookup"><span data-stu-id="b6456-143">ID of one user in the conference session.</span></span> <span data-ttu-id="b6456-144">Дополнительные сведения <a href="lync-server-2013-users-table.md">можно найти в таблице Users (пользователи) в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="b6456-144">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b6456-145"><strong>UserEndpointId</strong></span><span class="sxs-lookup"><span data-stu-id="b6456-145"><strong>UserEndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="b6456-146">идентификатора</span><span class="sxs-lookup"><span data-stu-id="b6456-146">uniqueidentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b6456-147">GUID для идентификации экземпляра конечной точки.</span><span class="sxs-lookup"><span data-stu-id="b6456-147">A GUID to identify the instance of endpoint.</span></span> <span data-ttu-id="b6456-148">Например, если один пользователь входит в систему на разных компьютерах с одной и той же учетной записью, каждый из них будет иметь другой идентификатор конечной точки.</span><span class="sxs-lookup"><span data-stu-id="b6456-148">For example, if one user logs on to different machines with the same account, then each machine will have a different endpoint ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6456-149"><strong>OnBehalfOfId</strong></span><span class="sxs-lookup"><span data-stu-id="b6456-149"><strong>OnBehalfOfId</strong></span></span></p></td>
<td><p><span data-ttu-id="b6456-150">целое</span><span class="sxs-lookup"><span data-stu-id="b6456-150">int</span></span></p></td>
<td><p><span data-ttu-id="b6456-151">Другом</span><span class="sxs-lookup"><span data-stu-id="b6456-151">Foreign</span></span></p></td>
<td><p><span data-ttu-id="b6456-152">Идентификатор пользователя, от имени которого вызывающим абонентом является.</span><span class="sxs-lookup"><span data-stu-id="b6456-152">Indicates the ID of the user of who the caller is on behalf.</span></span> <span data-ttu-id="b6456-153">Дополнительные сведения <a href="lync-server-2013-users-table.md">можно найти в таблице Users (пользователи) в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="b6456-153">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b6456-154"><strong>ReferredById</strong></span><span class="sxs-lookup"><span data-stu-id="b6456-154"><strong>ReferredById</strong></span></span></p></td>
<td><p><span data-ttu-id="b6456-155">целое</span><span class="sxs-lookup"><span data-stu-id="b6456-155">int</span></span></p></td>
<td><p><span data-ttu-id="b6456-156">Другом</span><span class="sxs-lookup"><span data-stu-id="b6456-156">Foreign</span></span></p></td>
<td><p><span data-ttu-id="b6456-157">Идентификационный номер пользователя, на который ссылается вызов.</span><span class="sxs-lookup"><span data-stu-id="b6456-157">ID of the user by who the call is referred.</span></span> <span data-ttu-id="b6456-158">Дополнительные сведения <a href="lync-server-2013-users-table.md">можно найти в таблице Users (пользователи) в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="b6456-158">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6456-159"><strong>UserClientVersionId</strong></span><span class="sxs-lookup"><span data-stu-id="b6456-159"><strong>UserClientVersionId</strong></span></span></p></td>
<td><p><span data-ttu-id="b6456-160">целое</span><span class="sxs-lookup"><span data-stu-id="b6456-160">int</span></span></p></td>
<td><p><span data-ttu-id="b6456-161">Другом</span><span class="sxs-lookup"><span data-stu-id="b6456-161">Foreign</span></span></p></td>
<td><p><span data-ttu-id="b6456-162">Версия клиента, используемая пользователем Конференции.</span><span class="sxs-lookup"><span data-stu-id="b6456-162">Client version used by the conference user.</span></span> <span data-ttu-id="b6456-163">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-clientversions-table.md">таблицей ClientVersions в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="b6456-163">See the <a href="lync-server-2013-clientversions-table.md">ClientVersions table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b6456-164"><strong>ConfClientVersionId</strong></span><span class="sxs-lookup"><span data-stu-id="b6456-164"><strong>ConfClientVersionId</strong></span></span></p></td>
<td><p><span data-ttu-id="b6456-165">целое</span><span class="sxs-lookup"><span data-stu-id="b6456-165">int</span></span></p></td>
<td><p><span data-ttu-id="b6456-166">Другом</span><span class="sxs-lookup"><span data-stu-id="b6456-166">Foreign</span></span></p></td>
<td><p><span data-ttu-id="b6456-167">Версия клиента, используемая сервером Конференции.</span><span class="sxs-lookup"><span data-stu-id="b6456-167">Client version used by the conference server.</span></span> <span data-ttu-id="b6456-168">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-clientversions-table.md">таблицей ClientVersions в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="b6456-168">See the <a href="lync-server-2013-clientversions-table.md">ClientVersions table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6456-169"><strong>ReplaceDialogIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="b6456-169"><strong>ReplaceDialogIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="b6456-170">datetime</span><span class="sxs-lookup"><span data-stu-id="b6456-170">datetime</span></span></p></td>
<td><p><span data-ttu-id="b6456-171">Другом</span><span class="sxs-lookup"><span data-stu-id="b6456-171">Foreign</span></span></p></td>
<td><p><span data-ttu-id="b6456-172">ИДЕНТИФИКАЦИОНный номер, определяющий диалоговое окно, которое было заменено текущим сеансом.</span><span class="sxs-lookup"><span data-stu-id="b6456-172">ID number to identify the dialog which was replaced by current session.</span></span> <span data-ttu-id="b6456-173">Дополнительные сведения приведены <a href="lync-server-2013-dialogs-table.md">в таблице диалоговые окна Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="b6456-173">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b6456-174"><strong>ReplaceDialogIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="b6456-174"><strong>ReplaceDialogIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="b6456-175">целое</span><span class="sxs-lookup"><span data-stu-id="b6456-175">int</span></span></p></td>
<td><p><span data-ttu-id="b6456-176">Другом</span><span class="sxs-lookup"><span data-stu-id="b6456-176">Foreign</span></span></p></td>
<td><p><span data-ttu-id="b6456-177">ИДЕНТИФИКАЦИОНный номер для идентификации сеанса.</span><span class="sxs-lookup"><span data-stu-id="b6456-177">ID number to identify the session.</span></span> <span data-ttu-id="b6456-178">Используется в сочетании с <strong>ReplacesDialogIdTime</strong> для уникальной идентификации сеанса, который заменяется этим сеансом.</span><span class="sxs-lookup"><span data-stu-id="b6456-178">Used in conjunction with <strong>ReplacesDialogIdTime</strong> to uniquely identify a session that is replaced by this session.</span></span> <span data-ttu-id="b6456-179">Дополнительные сведения приведены <a href="lync-server-2013-dialogs-table.md">в таблице диалоговые окна Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="b6456-179">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6456-180"><strong>IsStartedByConfServer</strong></span><span class="sxs-lookup"><span data-stu-id="b6456-180"><strong>IsStartedByConfServer</strong></span></span></p></td>
<td><p><span data-ttu-id="b6456-181">бит</span><span class="sxs-lookup"><span data-stu-id="b6456-181">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b6456-182">Указывает, был ли сеанс запущен сервером конференц-связи.</span><span class="sxs-lookup"><span data-stu-id="b6456-182">Indicates if the session started by the conferencing Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b6456-183"><strong>IsEndedByConfServer</strong></span><span class="sxs-lookup"><span data-stu-id="b6456-183"><strong>IsEndedByConfServer</strong></span></span></p></td>
<td><p><span data-ttu-id="b6456-184">бит</span><span class="sxs-lookup"><span data-stu-id="b6456-184">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b6456-185">Указывает, завершился ли сеанс сервером конференций.</span><span class="sxs-lookup"><span data-stu-id="b6456-185">Indicates if the session ended by the conferencing server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6456-186"><strong>IsUserInternal</strong></span><span class="sxs-lookup"><span data-stu-id="b6456-186"><strong>IsUserInternal</strong></span></span></p></td>
<td><p><span data-ttu-id="b6456-187">бит</span><span class="sxs-lookup"><span data-stu-id="b6456-187">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b6456-188">Вход пользователя из внутреннего режима или нет.</span><span class="sxs-lookup"><span data-stu-id="b6456-188">Whether user is logged on from internal or not.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b6456-189"><strong>ResponseCode</strong></span><span class="sxs-lookup"><span data-stu-id="b6456-189"><strong>ResponseCode</strong></span></span></p></td>
<td><p><span data-ttu-id="b6456-190">целое</span><span class="sxs-lookup"><span data-stu-id="b6456-190">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b6456-191">Код ответа протокола запуска сеансов (SIP) в приглашение на сеанс.</span><span class="sxs-lookup"><span data-stu-id="b6456-191">Session Initiation Protocol (SIP) response code to the session invitation.</span></span> <span data-ttu-id="b6456-192">Это поле обычно заполняется данными, созданными на основе исходного сообщения INVITE в сеансе.</span><span class="sxs-lookup"><span data-stu-id="b6456-192">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="b6456-193">Если сообщение приглашения отсутствует, поле заполняется датой и временем первого соответствующего сообщения SIP (пока, CANCEL, MESSAGE или INFO).</span><span class="sxs-lookup"><span data-stu-id="b6456-193">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6456-194"><strong>DiagnosticId</strong></span><span class="sxs-lookup"><span data-stu-id="b6456-194"><strong>DiagnosticId</strong></span></span></p></td>
<td><p><span data-ttu-id="b6456-195">целое</span><span class="sxs-lookup"><span data-stu-id="b6456-195">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b6456-196">Идентификатор диагностики, полученный в заголовке SIP.</span><span class="sxs-lookup"><span data-stu-id="b6456-196">Diagnostic ID captured from SIP header.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b6456-197"><strong>ServerId</strong></span><span class="sxs-lookup"><span data-stu-id="b6456-197"><strong>ServerId</strong></span></span></p></td>
<td><p><span data-ttu-id="b6456-198">целое</span><span class="sxs-lookup"><span data-stu-id="b6456-198">int</span></span></p></td>
<td><p><span data-ttu-id="b6456-199">Другом</span><span class="sxs-lookup"><span data-stu-id="b6456-199">Foreign</span></span></p></td>
<td><p><span data-ttu-id="b6456-200">Идентификатор сервера переднего плана, используемого для этого сеанса.</span><span class="sxs-lookup"><span data-stu-id="b6456-200">ID of the front-end server used for this session.</span></span> <span data-ttu-id="b6456-201">Более подробную информацию вы видите <a href="lync-server-2013-servers-table.md">в таблице Servers (серверы) в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="b6456-201">See the <a href="lync-server-2013-servers-table.md">Servers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6456-202"><strong>PoolId</strong></span><span class="sxs-lookup"><span data-stu-id="b6456-202"><strong>PoolId</strong></span></span></p></td>
<td><p><span data-ttu-id="b6456-203">целое</span><span class="sxs-lookup"><span data-stu-id="b6456-203">int</span></span></p></td>
<td><p><span data-ttu-id="b6456-204">Другом</span><span class="sxs-lookup"><span data-stu-id="b6456-204">Foreign</span></span></p></td>
<td><p><span data-ttu-id="b6456-205">Идентификатор пула, в котором был собран сеанс.</span><span class="sxs-lookup"><span data-stu-id="b6456-205">ID of the pool in which the session was captured.</span></span> <span data-ttu-id="b6456-206">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-pools-table.md">таблицей пулы в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="b6456-206">See the <a href="lync-server-2013-pools-table.md">Pools table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b6456-207"><strong>MediationServerId</strong></span><span class="sxs-lookup"><span data-stu-id="b6456-207"><strong>MediationServerId</strong></span></span></p></td>
<td><p><span data-ttu-id="b6456-208">целое</span><span class="sxs-lookup"><span data-stu-id="b6456-208">int</span></span></p></td>
<td><p><span data-ttu-id="b6456-209">Другом</span><span class="sxs-lookup"><span data-stu-id="b6456-209">Foreign</span></span></p></td>
<td><p><span data-ttu-id="b6456-210">Сервер, на котором используется этот звонок.</span><span class="sxs-lookup"><span data-stu-id="b6456-210">The Mediation Server the call is using.</span></span> <span data-ttu-id="b6456-211">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-mediationservers-table.md">таблицей MediationServers в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="b6456-211">See the <a href="lync-server-2013-mediationservers-table.md">MediationServers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6456-212"><strong>GatewayId</strong></span><span class="sxs-lookup"><span data-stu-id="b6456-212"><strong>GatewayId</strong></span></span></p></td>
<td><p><span data-ttu-id="b6456-213">целое</span><span class="sxs-lookup"><span data-stu-id="b6456-213">int</span></span></p></td>
<td><p><span data-ttu-id="b6456-214">Другом</span><span class="sxs-lookup"><span data-stu-id="b6456-214">Foreign</span></span></p></td>
<td><p><span data-ttu-id="b6456-215">Шлюз, который использует этот звонок.</span><span class="sxs-lookup"><span data-stu-id="b6456-215">The gateway the call is using.</span></span> <span data-ttu-id="b6456-216">Более подробную информацию вы увидите <a href="lync-server-2013-gateways-table.md">в таблице шлюзов в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="b6456-216">See the <a href="lync-server-2013-gateways-table.md">Gateways table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b6456-217"><strong>EdgeServerId</strong></span><span class="sxs-lookup"><span data-stu-id="b6456-217"><strong>EdgeServerId</strong></span></span></p></td>
<td><p><span data-ttu-id="b6456-218">целое</span><span class="sxs-lookup"><span data-stu-id="b6456-218">int</span></span></p></td>
<td><p><span data-ttu-id="b6456-219">Другом</span><span class="sxs-lookup"><span data-stu-id="b6456-219">Foreign</span></span></p></td>
<td><p><span data-ttu-id="b6456-220">Пограничный сервер, на котором используется звонок.</span><span class="sxs-lookup"><span data-stu-id="b6456-220">The Edge Server the call is using.</span></span> <span data-ttu-id="b6456-221">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-edgeservers-table.md">таблицей EdgeServers в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="b6456-221">See the <a href="lync-server-2013-edgeservers-table.md">EdgeServers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6456-222"><strong>ContentTypeId</strong></span><span class="sxs-lookup"><span data-stu-id="b6456-222"><strong>ContentTypeId</strong></span></span></p></td>
<td><p><span data-ttu-id="b6456-223">целое</span><span class="sxs-lookup"><span data-stu-id="b6456-223">int</span></span></p></td>
<td><p><span data-ttu-id="b6456-224">Другом</span><span class="sxs-lookup"><span data-stu-id="b6456-224">Foreign</span></span></p></td>
<td><p><span data-ttu-id="b6456-225">Тип контента, используемый в сеансе.</span><span class="sxs-lookup"><span data-stu-id="b6456-225">Content type used in the session.</span></span> <span data-ttu-id="b6456-226">Дополнительные сведения приведены <a href="lync-server-2013-contenttypes-table.md">в таблице ContentTypes в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="b6456-226">See the <a href="lync-server-2013-contenttypes-table.md">ContentTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b6456-227"><strong>InviteTime</strong></span><span class="sxs-lookup"><span data-stu-id="b6456-227"><strong>InviteTime</strong></span></span></p></td>
<td><p><span data-ttu-id="b6456-228">datetime</span><span class="sxs-lookup"><span data-stu-id="b6456-228">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b6456-229">Время первого запроса приглашения.</span><span class="sxs-lookup"><span data-stu-id="b6456-229">The time of the first INVITE request.</span></span> <span data-ttu-id="b6456-230">Это поле обычно заполняется данными, созданными на основе исходного сообщения INVITE в сеансе.</span><span class="sxs-lookup"><span data-stu-id="b6456-230">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="b6456-231">Если сообщение приглашения отсутствует, поле заполняется датой и временем первого соответствующего сообщения SIP (пока, CANCEL, MESSAGE или INFO).</span><span class="sxs-lookup"><span data-stu-id="b6456-231">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6456-232"><strong>ResponseTime</strong></span><span class="sxs-lookup"><span data-stu-id="b6456-232"><strong>ResponseTime</strong></span></span></p></td>
<td><p><span data-ttu-id="b6456-233">datetime</span><span class="sxs-lookup"><span data-stu-id="b6456-233">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b6456-234">Время первого ответа SIP.</span><span class="sxs-lookup"><span data-stu-id="b6456-234">Time of the first SIP RESPONSE.</span></span> <span data-ttu-id="b6456-235">Это поле обычно заполняется данными, созданными на основе исходного сообщения INVITE в сеансе.</span><span class="sxs-lookup"><span data-stu-id="b6456-235">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="b6456-236">Если сообщение приглашения отсутствует, поле заполняется датой и временем первого соответствующего сообщения SIP (пока, CANCEL, MESSAGE или INFO).</span><span class="sxs-lookup"><span data-stu-id="b6456-236">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b6456-237"><strong>SessionEndTime</strong></span><span class="sxs-lookup"><span data-stu-id="b6456-237"><strong>SessionEndTime</strong></span></span></p></td>
<td><p><span data-ttu-id="b6456-238">datetime</span><span class="sxs-lookup"><span data-stu-id="b6456-238">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b6456-239">Время завершения сеанса.</span><span class="sxs-lookup"><span data-stu-id="b6456-239">The time when the session is ended.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6456-240"><strong>UriTypeId</strong></span><span class="sxs-lookup"><span data-stu-id="b6456-240"><strong>UriTypeId</strong></span></span></p></td>
<td><p><span data-ttu-id="b6456-241">tinyint</span><span class="sxs-lookup"><span data-stu-id="b6456-241">tinyint</span></span></p></td>
<td><p><span data-ttu-id="b6456-242">Другом</span><span class="sxs-lookup"><span data-stu-id="b6456-242">Foreign</span></span></p></td>
<td><p><span data-ttu-id="b6456-243">Имеет значение типа URI MCU из <a href="lync-server-2013-uritypes-table.md">таблицы UriTypes в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="b6456-243">Contains the MCU URI type value from the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a>.</span></span> <span data-ttu-id="b6456-244">Это поле используется для повышения производительности запроса.</span><span class="sxs-lookup"><span data-stu-id="b6456-244">This field is used for improving query performance.</span></span></p>
<p><span data-ttu-id="b6456-245">Это поле было введено в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b6456-245">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b6456-246"><strong>UserFlag</strong></span><span class="sxs-lookup"><span data-stu-id="b6456-246"><strong>UserFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="b6456-247">smallint</span><span class="sxs-lookup"><span data-stu-id="b6456-247">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b6456-248">Битовый набор, обозначающий атрибуты пользователя.</span><span class="sxs-lookup"><span data-stu-id="b6456-248">A bit set that indicates the user attributes.</span></span> <span data-ttu-id="b6456-249">Следующие определения атрибутов перечислены ниже.</span><span class="sxs-lookup"><span data-stu-id="b6456-249">The following attribute definitions are listed:</span></span></p>
<ul>
<li><p><span data-ttu-id="b6456-250">Интеграция с настольным телефоном 1</span><span class="sxs-lookup"><span data-stu-id="b6456-250">Integrated with desktop phone - 1</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6456-251"><strong>CallFlag</strong></span><span class="sxs-lookup"><span data-stu-id="b6456-251"><strong>CallFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="b6456-252">smallint</span><span class="sxs-lookup"><span data-stu-id="b6456-252">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b6456-253">Битовый набор, обозначающий атрибуты вызова.</span><span class="sxs-lookup"><span data-stu-id="b6456-253">A bit set that indicates the call attributes.</span></span> <span data-ttu-id="b6456-254">Следующие определения атрибутов перечислены ниже.</span><span class="sxs-lookup"><span data-stu-id="b6456-254">The following attribute definitions are listed:</span></span></p>
<ul>
<li><p><span data-ttu-id="b6456-255">Сеанс с повторной попыткой 1</span><span class="sxs-lookup"><span data-stu-id="b6456-255">Retried Session - 1</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b6456-256">\* Для большинства сеансов для SessionIdSeq будет задано значение 1.</span><span class="sxs-lookup"><span data-stu-id="b6456-256">\* For most sessions, SessionIdSeq will have the value of 1.</span></span> <span data-ttu-id="b6456-257">Если несколько сеансов начинаются в одно и то же время, SessionIdSeq для одного из них будет равен 1, а для другого — 2 и т. д.</span><span class="sxs-lookup"><span data-stu-id="b6456-257">If multiple sessions start at exactly the same time, the SessionIdSeq for one will be 1, for another will be 2, and so on.</span></span>

<span data-ttu-id="b6456-258"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b6456-258"></div>

<span> </span>

</div>

</div>

</span></span></div>

