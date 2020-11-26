---
title: 'Lync Server 2013: представление ConferenceSessionDetails'
description: 'Lync Server 2013: ConferenceSessionDetails View.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ConferenceSessionDetails view
ms:assetid: 5858c84d-baed-421d-ad1d-3726e150e256
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688066(v=OCS.15)
ms:contentKeyID: 49733660
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d1c62f020413efecdbc0f909618256ccc7308d4f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434398"
---
# <a name="conferencesessiondetails-view-in-lync-server-2013"></a><span data-ttu-id="d219b-103">ConferenceSessionDetails представления в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d219b-103">ConferenceSessionDetails view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d219b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d219b-104">

<span> </span></span></span>

<span data-ttu-id="d219b-105">_**Тема последнего изменения:** 2012-11-12_</span><span class="sxs-lookup"><span data-stu-id="d219b-105">_**Topic Last Modified:** 2012-11-12_</span></span>

<span data-ttu-id="d219b-106">В представлении ConferenceSessionDetails хранятся сведения о многокомпонентных сеансах.</span><span class="sxs-lookup"><span data-stu-id="d219b-106">The ConferenceSessionDetails view stores information about multiparty sessions.</span></span> <span data-ttu-id="d219b-107">Каждая запись представляет один сеанс конференции, который может быть либо сеансом с фокусом, либо сеансом с определенным сервером конференц-связи.</span><span class="sxs-lookup"><span data-stu-id="d219b-107">Each record represents one conference session, which could be either the session with Focus or the session with a specific conferencing server.</span></span> <span data-ttu-id="d219b-108">Это представление было представлено в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d219b-108">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d219b-109">Столбец</span><span class="sxs-lookup"><span data-stu-id="d219b-109">Column</span></span></th>
<th><span data-ttu-id="d219b-110">Тип данных</span><span class="sxs-lookup"><span data-stu-id="d219b-110">Data Type</span></span></th>
<th><span data-ttu-id="d219b-111">Подробности</span><span class="sxs-lookup"><span data-stu-id="d219b-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d219b-112"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="d219b-112"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="d219b-113">datetime</span><span class="sxs-lookup"><span data-stu-id="d219b-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="d219b-114">Время запроса сеанса.</span><span class="sxs-lookup"><span data-stu-id="d219b-114">Time of session request.</span></span> <span data-ttu-id="d219b-115">Используется в сочетании с SessionIdSeq для уникальной идентификации сеанса.</span><span class="sxs-lookup"><span data-stu-id="d219b-115">Used in conjunction with SessionIdSeq to uniquely identify a session.</span></span> <span data-ttu-id="d219b-116">Дополнительные сведения приведены <a href="lync-server-2013-dialogs-table.md">в таблице диалоговые окна Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="d219b-116">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d219b-117"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="d219b-117"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="d219b-118">целое</span><span class="sxs-lookup"><span data-stu-id="d219b-118">int</span></span></p></td>
<td><p><span data-ttu-id="d219b-119">ИДЕНТИФИКАЦИОНный номер для идентификации сеанса.</span><span class="sxs-lookup"><span data-stu-id="d219b-119">ID number to identify the session.</span></span> <span data-ttu-id="d219b-120">Используется в сочетании с SessionIdTime для уникальной идентификации сеанса.</span><span class="sxs-lookup"><span data-stu-id="d219b-120">Used in conjunction with SessionIdTime to uniquely identify a session.</span></span> <span data-ttu-id="d219b-121">Дополнительные сведения приведены <a href="lync-server-2013-dialogs-table.md">в таблице диалоговые окна Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="d219b-121">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d219b-122"><strong>InviteTime</strong></span><span class="sxs-lookup"><span data-stu-id="d219b-122"><strong>InviteTime</strong></span></span></p></td>
<td><p><span data-ttu-id="d219b-123">datetime</span><span class="sxs-lookup"><span data-stu-id="d219b-123">datetime</span></span></p></td>
<td><p><span data-ttu-id="d219b-124">Время первого запроса приглашения.</span><span class="sxs-lookup"><span data-stu-id="d219b-124">Time of the first INVITE request.</span></span> <span data-ttu-id="d219b-125">Это поле обычно заполняется данными, созданными на основе исходного сообщения INVITE в сеансе.</span><span class="sxs-lookup"><span data-stu-id="d219b-125">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="d219b-126">Если сообщение приглашения отсутствует, поле заполняется датой и временем первого соответствующего сообщения SIP (пока, CANCEL, MESSAGE или INFO).</span><span class="sxs-lookup"><span data-stu-id="d219b-126">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d219b-127"><strong>ConferenceUri</strong></span><span class="sxs-lookup"><span data-stu-id="d219b-127"><strong>ConferenceUri</strong></span></span></p></td>
<td><p><span data-ttu-id="d219b-128">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="d219b-128">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="d219b-129">Универсальный код ресурса (URI) Конференции.</span><span class="sxs-lookup"><span data-stu-id="d219b-129">URI of the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d219b-130"><strong>ConferenceUriType</strong></span><span class="sxs-lookup"><span data-stu-id="d219b-130"><strong>ConferenceUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="d219b-131">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d219b-131">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d219b-132">Тип URI конференции.</span><span class="sxs-lookup"><span data-stu-id="d219b-132">Type of conference URI.</span></span> <span data-ttu-id="d219b-133">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-uritypes-table.md">таблицей UriTypes в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="d219b-133">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d219b-134"><strong>ConfInstance</strong></span><span class="sxs-lookup"><span data-stu-id="d219b-134"><strong>ConfInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="d219b-135">идентификатора</span><span class="sxs-lookup"><span data-stu-id="d219b-135">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="d219b-136">Идентификатор, отличающийся между экземплярами повторяющихся конференций.</span><span class="sxs-lookup"><span data-stu-id="d219b-136">Identifier that differentiates between instances of recurring conferences.</span></span> <span data-ttu-id="d219b-137">Каждый экземпляр повторяющейся Конференции имеет один и тот же ConferenceURI, но другое значение ConfInstance.</span><span class="sxs-lookup"><span data-stu-id="d219b-137">Each recurring conference instance has the same ConferenceURI but a different ConfInstance value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d219b-138"><strong>McuConferenceUri</strong></span><span class="sxs-lookup"><span data-stu-id="d219b-138"><strong>McuConferenceUri</strong></span></span></p></td>
<td><p><span data-ttu-id="d219b-139">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="d219b-139">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="d219b-140">Универсальный код ресурса (URI) сервера конференц-связи.</span><span class="sxs-lookup"><span data-stu-id="d219b-140">URI of the conferencing server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d219b-141"><strong>McuConferenceUriType</strong></span><span class="sxs-lookup"><span data-stu-id="d219b-141"><strong>McuConferenceUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="d219b-142">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d219b-142">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d219b-143">Тип URI сервера конференц-связи.</span><span class="sxs-lookup"><span data-stu-id="d219b-143">Type of conferencing server URI.</span></span> <span data-ttu-id="d219b-144">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-uritypes-table.md">таблицей UriTypes в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="d219b-144">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d219b-145"><strong>UserUri</strong></span><span class="sxs-lookup"><span data-stu-id="d219b-145"><strong>UserUri</strong></span></span></p></td>
<td><p><span data-ttu-id="d219b-146">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="d219b-146">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="d219b-147">Универсальный код ресурса (URI) пользователя, участвующего в сеансе.</span><span class="sxs-lookup"><span data-stu-id="d219b-147">URI of the user involved in the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d219b-148"><strong>UserUriType</strong></span><span class="sxs-lookup"><span data-stu-id="d219b-148"><strong>UserUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="d219b-149">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d219b-149">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d219b-150">Тип URI пользователя, который является частью сеанса.</span><span class="sxs-lookup"><span data-stu-id="d219b-150">Type of URI of the user whose was part of the session.</span></span> <span data-ttu-id="d219b-151">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-uritypes-table.md">таблицей UriTypes в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="d219b-151">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d219b-152"><strong>UserTenant</strong></span><span class="sxs-lookup"><span data-stu-id="d219b-152"><strong>UserTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="d219b-153">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d219b-153">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d219b-154">Клиент пользователя, который является частью сеанса.</span><span class="sxs-lookup"><span data-stu-id="d219b-154">Tenant of the user whose was part of the session.</span></span> <span data-ttu-id="d219b-155">Дополнительные сведения приведены в <a href="lync-server-2013-tenants-table.md">таблице "клиенты" в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="d219b-155">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d219b-156"><strong>UserEndpointId</strong></span><span class="sxs-lookup"><span data-stu-id="d219b-156"><strong>UserEndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="d219b-157">идентификатора</span><span class="sxs-lookup"><span data-stu-id="d219b-157">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="d219b-158">Уникальный идентификатор пользователя, который является частью сеанса.</span><span class="sxs-lookup"><span data-stu-id="d219b-158">Unique identifier of the user whose was part of the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d219b-159"><strong>EndTime</strong></span><span class="sxs-lookup"><span data-stu-id="d219b-159"><strong>EndTime</strong></span></span></p></td>
<td><p><span data-ttu-id="d219b-160">datetime</span><span class="sxs-lookup"><span data-stu-id="d219b-160">datetime</span></span></p></td>
<td><p><span data-ttu-id="d219b-161">Время окончания сеанса.</span><span class="sxs-lookup"><span data-stu-id="d219b-161">End time of the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d219b-162"><strong>ConferenceClientVersion</strong></span><span class="sxs-lookup"><span data-stu-id="d219b-162"><strong>ConferenceClientVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="d219b-163">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d219b-163">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d219b-164">Версия сервера конференций.</span><span class="sxs-lookup"><span data-stu-id="d219b-164">Version of conference server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d219b-165"><strong>ConferenceClientType</strong></span><span class="sxs-lookup"><span data-stu-id="d219b-165"><strong>ConferenceClientType</strong></span></span></p></td>
<td><p><span data-ttu-id="d219b-166">целое</span><span class="sxs-lookup"><span data-stu-id="d219b-166">int</span></span></p></td>
<td><p><span data-ttu-id="d219b-167">Тип сервера конференций.</span><span class="sxs-lookup"><span data-stu-id="d219b-167">Type of conference server.</span></span> <span data-ttu-id="d219b-168">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-useragentdef-table.md">таблицей UserAgentDef в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="d219b-168">See the <a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d219b-169"><strong>ConferenceCategory</strong></span><span class="sxs-lookup"><span data-stu-id="d219b-169"><strong>ConferenceCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="d219b-170">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="d219b-170">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="d219b-171">Категория "сервер конференции".</span><span class="sxs-lookup"><span data-stu-id="d219b-171">Conference server category.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d219b-172"><strong>UserClientVersion</strong></span><span class="sxs-lookup"><span data-stu-id="d219b-172"><strong>UserClientVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="d219b-173">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d219b-173">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d219b-174">Версия клиента, используемая пользователем, который принимал участие в сеансе.</span><span class="sxs-lookup"><span data-stu-id="d219b-174">Version of client used by the user who participated in the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d219b-175"><strong>UserClientType</strong></span><span class="sxs-lookup"><span data-stu-id="d219b-175"><strong>UserClientType</strong></span></span></p></td>
<td><p><span data-ttu-id="d219b-176">целое</span><span class="sxs-lookup"><span data-stu-id="d219b-176">int</span></span></p></td>
<td><p><span data-ttu-id="d219b-177">Клиент, используемый пользователем, который участвовал в сеансе.</span><span class="sxs-lookup"><span data-stu-id="d219b-177">Client used by the user who participated in the session.</span></span> <span data-ttu-id="d219b-178">Дополнительные сведения вы увидите <a href="lync-server-2013-useragentdef-table.md">в таблице UserAgentDef в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="d219b-178">See the <a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a> for more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d219b-179"><strong>UserClientCategory</strong></span><span class="sxs-lookup"><span data-stu-id="d219b-179"><strong>UserClientCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="d219b-180">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="d219b-180">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="d219b-181">Имя категории клиента, используемой пользователем, который является частью сеанса.</span><span class="sxs-lookup"><span data-stu-id="d219b-181">Name of the category of the client used by the user who was part of the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d219b-182"><strong>OnBehalfOfUri</strong></span><span class="sxs-lookup"><span data-stu-id="d219b-182"><strong>OnBehalfOfUri</strong></span></span></p></td>
<td><p><span data-ttu-id="d219b-183">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="d219b-183">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="d219b-184">Универсальный код ресурса (URI) пользователя, от имени которого был запущен сеанс.</span><span class="sxs-lookup"><span data-stu-id="d219b-184">URI of the user on whose behalf the session was started.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d219b-185"><strong>OnBehalfOfUriType</strong></span><span class="sxs-lookup"><span data-stu-id="d219b-185"><strong>OnBehalfOfUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="d219b-186">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d219b-186">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d219b-187">Тип универсального кода ресурса (URI) пользователя, от имени которого был запущен сеанс.</span><span class="sxs-lookup"><span data-stu-id="d219b-187">Type of URI of the user on whose behalf the session was started.</span></span> <span data-ttu-id="d219b-188">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-uritypes-table.md">таблицей UriTypes в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="d219b-188">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d219b-189"><strong>OnBehalfOfTenant</strong></span><span class="sxs-lookup"><span data-stu-id="d219b-189"><strong>OnBehalfOfTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="d219b-190">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d219b-190">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d219b-191">Клиент пользователя, от имени которого был запущен сеанс.</span><span class="sxs-lookup"><span data-stu-id="d219b-191">Tenant of the user whose on behalf the session was started.</span></span> <span data-ttu-id="d219b-192">Дополнительные сведения приведены в <a href="lync-server-2013-tenants-table.md">таблице "клиенты" в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="d219b-192">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d219b-193"><strong>ReferredByUri</strong></span><span class="sxs-lookup"><span data-stu-id="d219b-193"><strong>ReferredByUri</strong></span></span></p></td>
<td><p><span data-ttu-id="d219b-194">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="d219b-194">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="d219b-195">URI пользователя, который ссылался на сеанс.</span><span class="sxs-lookup"><span data-stu-id="d219b-195">URI of the user who referred the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d219b-196"><strong>ReferredByUriType</strong></span><span class="sxs-lookup"><span data-stu-id="d219b-196"><strong>ReferredByUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="d219b-197">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d219b-197">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d219b-198">Тип URI пользователя, который ссылался на сеанс.</span><span class="sxs-lookup"><span data-stu-id="d219b-198">Type of URI of the user who referred the session.</span></span> <span data-ttu-id="d219b-199">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-uritypes-table.md">таблицей UriTypes в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="d219b-199">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d219b-200"><strong>ReferredByUriTenant</strong></span><span class="sxs-lookup"><span data-stu-id="d219b-200"><strong>ReferredByUriTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="d219b-201">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d219b-201">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d219b-202">Клиент пользователя, который ссылался на сеанс.</span><span class="sxs-lookup"><span data-stu-id="d219b-202">Tenant of the user who referred the session.</span></span> <span data-ttu-id="d219b-203">Дополнительные сведения приведены в <a href="lync-server-2013-tenants-table.md">таблице "клиенты" в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="d219b-203">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d219b-204"><strong>DialogId</strong></span><span class="sxs-lookup"><span data-stu-id="d219b-204"><strong>DialogId</strong></span></span></p></td>
<td><p><span data-ttu-id="d219b-205">varstring (775)</span><span class="sxs-lookup"><span data-stu-id="d219b-205">varstring(775)</span></span></p></td>
<td><p><span data-ttu-id="d219b-206">ИДЕНТИФИКАТОР диалогового окна SIP.</span><span class="sxs-lookup"><span data-stu-id="d219b-206">SIP dialog ID.</span></span> <span data-ttu-id="d219b-207">Формат</span><span class="sxs-lookup"><span data-stu-id="d219b-207">The format is</span></span></p>
<p><span data-ttu-id="d219b-208">:d ialog; to-Tag</span><span class="sxs-lookup"><span data-stu-id="d219b-208">:dialog;from-tag;to-tag</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d219b-209"><strong>ReplaceDialogIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="d219b-209"><strong>ReplaceDialogIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="d219b-210">datetime</span><span class="sxs-lookup"><span data-stu-id="d219b-210">datetime</span></span></p></td>
<td><p><span data-ttu-id="d219b-211">ИДЕНТИФИКАЦИОНный номер, определяющий диалоговое окно, которое было заменено текущим сеансом.</span><span class="sxs-lookup"><span data-stu-id="d219b-211">ID number to identify the dialog which was replaced by current session.</span></span> <span data-ttu-id="d219b-212">Дополнительные сведения приведены <a href="lync-server-2013-dialogs-table.md">в таблице диалоговые окна Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="d219b-212">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d219b-213"><strong>ReplaceDialogIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="d219b-213"><strong>ReplaceDialogIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="d219b-214">целое</span><span class="sxs-lookup"><span data-stu-id="d219b-214">int</span></span></p></td>
<td><p><span data-ttu-id="d219b-215">ИДЕНТИФИКАЦИОНный номер для идентификации сеанса.</span><span class="sxs-lookup"><span data-stu-id="d219b-215">ID number to identify the session.</span></span> <span data-ttu-id="d219b-216">Используется в сочетании с ReplaceDialogIdTime для уникальной идентификации сеанса, который заменяется этим сеансом.</span><span class="sxs-lookup"><span data-stu-id="d219b-216">Used in conjunction with ReplaceDialogIdTime to uniquely identify a session that is replaced by this session.</span></span> <span data-ttu-id="d219b-217">Дополнительные сведения приведены <a href="lync-server-2013-dialogs-table.md">в таблице диалоговые окна Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="d219b-217">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d219b-218"><strong>ReplacesDialogId</strong></span><span class="sxs-lookup"><span data-stu-id="d219b-218"><strong>ReplacesDialogId</strong></span></span></p></td>
<td><p><span data-ttu-id="d219b-219">varchar (775)</span><span class="sxs-lookup"><span data-stu-id="d219b-219">varchar(775)</span></span></p></td>
<td><p><span data-ttu-id="d219b-220">ИДЕНТИФИКАТОР диалогового окна SIP, в котором будет заменяться сеанс.</span><span class="sxs-lookup"><span data-stu-id="d219b-220">SIP dialog ID the session replaces.</span></span> <span data-ttu-id="d219b-221">Формат:</span><span class="sxs-lookup"><span data-stu-id="d219b-221">The format of the is:</span></span></p>
<p><span data-ttu-id="d219b-222">диалоговое окно; тег "from-Tag"</span><span class="sxs-lookup"><span data-stu-id="d219b-222">dialog;from-tag;to-tag</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d219b-223"><strong>IsStartedByConfServer</strong></span><span class="sxs-lookup"><span data-stu-id="d219b-223"><strong>IsStartedByConfServer</strong></span></span></p></td>
<td><p><span data-ttu-id="d219b-224">бит</span><span class="sxs-lookup"><span data-stu-id="d219b-224">bit</span></span></p></td>
<td><p><span data-ttu-id="d219b-225">Указывает, был ли запущен сервер конференц-связи.</span><span class="sxs-lookup"><span data-stu-id="d219b-225">Indicates whether the session was started by the conferencing server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d219b-226"><strong>IsEndedByConfServer</strong></span><span class="sxs-lookup"><span data-stu-id="d219b-226"><strong>IsEndedByConfServer</strong></span></span></p></td>
<td><p><span data-ttu-id="d219b-227">бит</span><span class="sxs-lookup"><span data-stu-id="d219b-227">bit</span></span></p></td>
<td><p><span data-ttu-id="d219b-228">Указывает, завершен ли сеанс на сервере конференций.</span><span class="sxs-lookup"><span data-stu-id="d219b-228">Indicates whether the session was ended by the conferencing server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d219b-229"><strong>IsUserInternal</strong></span><span class="sxs-lookup"><span data-stu-id="d219b-229"><strong>IsUserInternal</strong></span></span></p></td>
<td><p><span data-ttu-id="d219b-230">бит</span><span class="sxs-lookup"><span data-stu-id="d219b-230">bit</span></span></p></td>
<td><p><span data-ttu-id="d219b-231">Указывает, вошел ли пользователь из внутренней сети.</span><span class="sxs-lookup"><span data-stu-id="d219b-231">Indicates whether the user logged on from the internal network.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d219b-232"><strong>ResponseTime</strong></span><span class="sxs-lookup"><span data-stu-id="d219b-232"><strong>ResponseTime</strong></span></span></p></td>
<td><p><span data-ttu-id="d219b-233">datetime</span><span class="sxs-lookup"><span data-stu-id="d219b-233">datetime</span></span></p></td>
<td><p><span data-ttu-id="d219b-234">Время ответа на первое сообщение приглашения.</span><span class="sxs-lookup"><span data-stu-id="d219b-234">Time of the response to the first INVITE message.</span></span> <span data-ttu-id="d219b-235">Это поле обычно заполняется данными, созданными на основе исходного сообщения INVITE в сеансе.</span><span class="sxs-lookup"><span data-stu-id="d219b-235">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="d219b-236">Если сообщение приглашения отсутствует, поле заполняется датой и временем первого соответствующего сообщения SIP (пока, CANCEL, MESSAGE или INFO).</span><span class="sxs-lookup"><span data-stu-id="d219b-236">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d219b-237"><strong>ResponseCode</strong></span><span class="sxs-lookup"><span data-stu-id="d219b-237"><strong>ResponseCode</strong></span></span></p></td>
<td><p><span data-ttu-id="d219b-238">целое</span><span class="sxs-lookup"><span data-stu-id="d219b-238">int</span></span></p></td>
<td><p><span data-ttu-id="d219b-239">Код ответа SIP на приглашение на сеанс.</span><span class="sxs-lookup"><span data-stu-id="d219b-239">SIP response code to the session invitation.</span></span> <span data-ttu-id="d219b-240">Это поле обычно заполняется данными, созданными на основе исходного сообщения INVITE в сеансе.</span><span class="sxs-lookup"><span data-stu-id="d219b-240">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="d219b-241">Если сообщение приглашения отсутствует, поле заполняется датой и временем первого соответствующего сообщения SIP (пока, CANCEL, MESSAGE или INFO).</span><span class="sxs-lookup"><span data-stu-id="d219b-241">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d219b-242"><strong>DiagnosticId</strong></span><span class="sxs-lookup"><span data-stu-id="d219b-242"><strong>DiagnosticId</strong></span></span></p></td>
<td><p><span data-ttu-id="d219b-243">целое</span><span class="sxs-lookup"><span data-stu-id="d219b-243">int</span></span></p></td>
<td><p><span data-ttu-id="d219b-244">Идентификатор диагностики, полученный от заголовков SIP сеанса.</span><span class="sxs-lookup"><span data-stu-id="d219b-244">Diagnostic ID captured from session SIP headers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d219b-245"><strong>Контента</strong></span><span class="sxs-lookup"><span data-stu-id="d219b-245"><strong>ContentType</strong></span></span></p></td>
<td><p><span data-ttu-id="d219b-246">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d219b-246">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d219b-247">Тип контента для сеанса.</span><span class="sxs-lookup"><span data-stu-id="d219b-247">Content type for the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d219b-248"><strong>FrontEnd</strong></span><span class="sxs-lookup"><span data-stu-id="d219b-248"><strong>FrontEnd</strong></span></span></p></td>
<td><p><span data-ttu-id="d219b-249">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d219b-249">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d219b-250">Полное доменное имя сервера переднего плана, который захватил данные для сеанса.</span><span class="sxs-lookup"><span data-stu-id="d219b-250">FQDN of the Front End server that captured the data for the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d219b-251"><strong>Pool</strong></span><span class="sxs-lookup"><span data-stu-id="d219b-251"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="d219b-252">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d219b-252">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d219b-253">Полное доменное имя пула, который захватывает данные для сеанса.</span><span class="sxs-lookup"><span data-stu-id="d219b-253">FQDN of the pool that captured the data for the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d219b-254"><strong>MediationServer</strong></span><span class="sxs-lookup"><span data-stu-id="d219b-254"><strong>MediationServer</strong></span></span></p></td>
<td><p><span data-ttu-id="d219b-255">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d219b-255">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d219b-256">Сервер исправлений, используемый пользователем, который принимал участие в сеансе.</span><span class="sxs-lookup"><span data-stu-id="d219b-256">Mediation Server used by the user who participated in the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d219b-257"><strong>Шлюз</strong></span><span class="sxs-lookup"><span data-stu-id="d219b-257"><strong>Gateway</strong></span></span></p></td>
<td><p><span data-ttu-id="d219b-258">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d219b-258">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d219b-259">Шлюз, используемый пользователем, который участвовал в сеансе.</span><span class="sxs-lookup"><span data-stu-id="d219b-259">Gateway used by the user who participated the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d219b-260"><strong>Пограничный сервер</strong></span><span class="sxs-lookup"><span data-stu-id="d219b-260"><strong>EdgeServer</strong></span></span></p></td>
<td><p><span data-ttu-id="d219b-261">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d219b-261">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d219b-262">Полное доменное имя пограничного сервера, используемое пользователем, который принимал участие в сеансе.</span><span class="sxs-lookup"><span data-stu-id="d219b-262">FQDN of the Edge server used by the user who participated in the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d219b-263"><strong>UserFlag</strong></span><span class="sxs-lookup"><span data-stu-id="d219b-263"><strong>UserFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="d219b-264">smallint</span><span class="sxs-lookup"><span data-stu-id="d219b-264">smallint</span></span></p></td>
<td><p><span data-ttu-id="d219b-265">Указывает атрибуты пользователя, который принимал участие в сеансе.</span><span class="sxs-lookup"><span data-stu-id="d219b-265">Indicates the attributes of the user who participated in the session.</span></span> <span data-ttu-id="d219b-266">Допустимы следующие определения атрибутов:</span><span class="sxs-lookup"><span data-stu-id="d219b-266">The following attribute definitions allowed:</span></span></p>
<p><span data-ttu-id="d219b-267">0x01 — интеграция с настольным телефоном</span><span class="sxs-lookup"><span data-stu-id="d219b-267">0x01 - Integrated with desktop phone</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d219b-268"><strong>CallFlag</strong></span><span class="sxs-lookup"><span data-stu-id="d219b-268"><strong>CallFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="d219b-269">smallint</span><span class="sxs-lookup"><span data-stu-id="d219b-269">smallint</span></span></p></td>
<td><p><span data-ttu-id="d219b-270">Указывает атрибуты вызова.</span><span class="sxs-lookup"><span data-stu-id="d219b-270">Indicates the call attributes.</span></span> <span data-ttu-id="d219b-271">Допустимы следующие определения атрибутов:</span><span class="sxs-lookup"><span data-stu-id="d219b-271">The following attribute definitions are allowed:</span></span></p>
<p><span data-ttu-id="d219b-272">0x01 — повторное попыток Session0</span><span class="sxs-lookup"><span data-stu-id="d219b-272">0x01 - Retried Session0</span></span></p>
<p><span data-ttu-id="d219b-273">x02 — вызов, сделанный агентом от имени группы ответа</span><span class="sxs-lookup"><span data-stu-id="d219b-273">x02 - A call made by agent on behalf of a Response Group</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="d219b-274">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d219b-274">


</div>

<span> </span>

</div>

</div>

</span></span></div>

