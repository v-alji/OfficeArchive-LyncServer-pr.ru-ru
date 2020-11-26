---
title: 'Lync Server 2013: представление McuJoinsAndLeaves'
description: 'Lync Server 2013: McuJoinsAndLeaves View.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: McuJoinsAndLeaves view
ms:assetid: 6f00b8e7-b8b6-4657-ac5e-d8a571806ae2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688088(v=OCS.15)
ms:contentKeyID: 49733687
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f7f2f51c340d5bd4824a6e8eff1a0da172a758c9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425733"
---
# <a name="mcujoinsandleaves-view-in-lync-server-2013"></a><span data-ttu-id="abce2-103">McuJoinsAndLeaves представления в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="abce2-103">McuJoinsAndLeaves view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="abce2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="abce2-104">

<span> </span></span></span>

<span data-ttu-id="abce2-105">_**Тема последнего изменения:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="abce2-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="abce2-106">В представлении McuJoinsAndLeaves хранятся сведения о присоединениях и выходе пользователей на один сервер конференции.</span><span class="sxs-lookup"><span data-stu-id="abce2-106">The McuJoinsAndLeaves view stores information about users join and leave information for one conference server.</span></span> <span data-ttu-id="abce2-107">Каждая запись в этом представлении включает в себя сведения о звонках для одной комбинации присоединения пользователя или выхода из него и сервера конференц-связи.</span><span class="sxs-lookup"><span data-stu-id="abce2-107">Each record in this view contains call details about one combination of a user join or leave and conferencing server.</span></span> <span data-ttu-id="abce2-108">Это представление было представлено в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="abce2-108">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="abce2-109">Столбец</span><span class="sxs-lookup"><span data-stu-id="abce2-109">Column</span></span></th>
<th><span data-ttu-id="abce2-110">Тип данных</span><span class="sxs-lookup"><span data-stu-id="abce2-110">Data Type</span></span></th>
<th><span data-ttu-id="abce2-111">Подробности</span><span class="sxs-lookup"><span data-stu-id="abce2-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="abce2-112"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="abce2-112"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="abce2-113">datetime</span><span class="sxs-lookup"><span data-stu-id="abce2-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="abce2-114">Время экземпляра Конференции.</span><span class="sxs-lookup"><span data-stu-id="abce2-114">Time of conference instance.</span></span> <span data-ttu-id="abce2-115">Используется в сочетании с SessionIdSeq для уникальной идентификации экземпляра Конференции.</span><span class="sxs-lookup"><span data-stu-id="abce2-115">Used in conjunction with SessionIdSeq to uniquely identify a conference instance.</span></span> <span data-ttu-id="abce2-116">Дополнительные сведения приведены <a href="lync-server-2013-conferences-table.md">в таблице конференции для Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="abce2-116">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="abce2-117"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="abce2-117"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="abce2-118">целое</span><span class="sxs-lookup"><span data-stu-id="abce2-118">int</span></span></p></td>
<td><p><span data-ttu-id="abce2-119">ИДЕНТИФИКАЦИОНный номер для идентификации экземпляра Конференции.</span><span class="sxs-lookup"><span data-stu-id="abce2-119">ID number to identify the conference instance.</span></span> <span data-ttu-id="abce2-120">Используется в сочетании с SessionIdTime для уникальной идентификации экземпляра Конференции.</span><span class="sxs-lookup"><span data-stu-id="abce2-120">Used in conjunction with SessionIdTime to uniquely identify a conference instance.</span></span> <span data-ttu-id="abce2-121">Дополнительные сведения приведены <a href="lync-server-2013-conferences-table.md">в таблице конференции для Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="abce2-121">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="abce2-122"><strong>McuUri</strong></span><span class="sxs-lookup"><span data-stu-id="abce2-122"><strong>McuUri</strong></span></span></p></td>
<td><p><span data-ttu-id="abce2-123">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="abce2-123">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="abce2-124">Универсальный код ресурса (URI) сервера конференций, к которому подключен пользователь.</span><span class="sxs-lookup"><span data-stu-id="abce2-124">The URI of the conferencing server that the user connected to.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="abce2-125"><strong>McuUriType</strong></span><span class="sxs-lookup"><span data-stu-id="abce2-125"><strong>McuUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="abce2-126">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="abce2-126">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="abce2-127">Универсальный код ресурса (URI) сервера конференций, к которому подключен пользователь.</span><span class="sxs-lookup"><span data-stu-id="abce2-127">The URI of the conferencing server that the user connected to.</span></span> <span data-ttu-id="abce2-128">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-uritypes-table.md">таблицей UriTypes в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="abce2-128">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="abce2-129"><strong>UserUri</strong></span><span class="sxs-lookup"><span data-stu-id="abce2-129"><strong>UserUri</strong></span></span></p></td>
<td><p><span data-ttu-id="abce2-130">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="abce2-130">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="abce2-131">Универсальный код ресурса (URI) пользователя, которому были собраны сведения о присоединении или выходе сервера конференций.</span><span class="sxs-lookup"><span data-stu-id="abce2-131">The URI of the user whose conferencing server join/leave information was captured.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="abce2-132"><strong>UserUriType</strong></span><span class="sxs-lookup"><span data-stu-id="abce2-132"><strong>UserUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="abce2-133">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="abce2-133">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="abce2-134">Тип универсального кода ресурса (URI), к которому были собраны сведения о присоединении или выходе сервера конференций.</span><span class="sxs-lookup"><span data-stu-id="abce2-134">The type of URI of the user whose conferencing server join/leave information was captured.</span></span> <span data-ttu-id="abce2-135">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-uritypes-table.md">таблицей UriTypes в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="abce2-135">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="abce2-136"><strong>UserTenant</strong></span><span class="sxs-lookup"><span data-stu-id="abce2-136"><strong>UserTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="abce2-137">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="abce2-137">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="abce2-138">Клиент пользователя, которому были собраны сведения о присоединении или выходе сервера конференций.</span><span class="sxs-lookup"><span data-stu-id="abce2-138">The tenant of the user whose conferencing server join/leave information was captured.</span></span> <span data-ttu-id="abce2-139">Дополнительные сведения приведены в <a href="lync-server-2013-tenants-table.md">таблице "клиенты" в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="abce2-139">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="abce2-140"><strong>UserClientVersion</strong></span><span class="sxs-lookup"><span data-stu-id="abce2-140"><strong>UserClientVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="abce2-141">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="abce2-141">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="abce2-142">Версия клиента, используемая пользователем, для которого была собрана информация о присоединении или выходе сервера конференций.</span><span class="sxs-lookup"><span data-stu-id="abce2-142">The version of client used by the user whose conferencing server join/leave information was captured.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="abce2-143"><strong>UserClientType</strong></span><span class="sxs-lookup"><span data-stu-id="abce2-143"><strong>UserClientType</strong></span></span></p></td>
<td><p><span data-ttu-id="abce2-144">целое</span><span class="sxs-lookup"><span data-stu-id="abce2-144">int</span></span></p></td>
<td><p><span data-ttu-id="abce2-145">Клиент, который использовался пользователем, которому присвоены данные для присоединения или выхода на сервер конференц-связи.</span><span class="sxs-lookup"><span data-stu-id="abce2-145">The client used by the user whose conferencing server join/leave information was captured.</span></span> <span data-ttu-id="abce2-146">Дополнительные сведения вы увидите <a href="lync-server-2013-useragentdef-table.md">в таблице UserAgentDef в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="abce2-146">See the <a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a> for more details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="abce2-147"><strong>UserClientCategory</strong></span><span class="sxs-lookup"><span data-stu-id="abce2-147"><strong>UserClientCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="abce2-148">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="abce2-148">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="abce2-149">Название категории клиента, используемой пользователем, для которого была получена информация о приходе и выходе сервера конференций.</span><span class="sxs-lookup"><span data-stu-id="abce2-149">The name of the category of the client used by the user whose conferencing server join/leave information was captured.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="abce2-150"><strong>McuUserInstance</strong></span><span class="sxs-lookup"><span data-stu-id="abce2-150"><strong>McuUserInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="abce2-151">целое</span><span class="sxs-lookup"><span data-stu-id="abce2-151">int</span></span></p></td>
<td><p><span data-ttu-id="abce2-152">Уникально определяет сочетание пользователей и устройств для пользователей, одновременно выполнивших вход на несколько устройств.</span><span class="sxs-lookup"><span data-stu-id="abce2-152">Uniquely identifies the user/device combination for users simultaneously logged on to multiple devices.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="abce2-153"><strong>IsUserFromPstn</strong></span><span class="sxs-lookup"><span data-stu-id="abce2-153"><strong>IsUserFromPstn</strong></span></span></p></td>
<td><p><span data-ttu-id="abce2-154">бит</span><span class="sxs-lookup"><span data-stu-id="abce2-154">bit</span></span></p></td>
<td><p><span data-ttu-id="abce2-155">Бит, обозначающий, является ли пользователь внутренним.</span><span class="sxs-lookup"><span data-stu-id="abce2-155">Bit that represents whether the user is an internal user or not.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="abce2-156"><strong>DialogSessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="abce2-156"><strong>DialogSessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="abce2-157">datetime</span><span class="sxs-lookup"><span data-stu-id="abce2-157">datetime</span></span></p></td>
<td><p><span data-ttu-id="abce2-158">Время запроса сеанса.</span><span class="sxs-lookup"><span data-stu-id="abce2-158">Time of session request.</span></span> <span data-ttu-id="abce2-159">Используется в сочетании с SessionIdSeq для уникальной идентификации сеанса.</span><span class="sxs-lookup"><span data-stu-id="abce2-159">Used in conjunction with SessionIdSeq to uniquely identify a session.</span></span> <span data-ttu-id="abce2-160">Дополнительные сведения приведены <a href="lync-server-2013-dialogs-table.md">в таблице диалоговые окна Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="abce2-160">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="abce2-161"><strong>DialogSessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="abce2-161"><strong>DialogSessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="abce2-162">целое</span><span class="sxs-lookup"><span data-stu-id="abce2-162">int</span></span></p></td>
<td><p><span data-ttu-id="abce2-163">ИДЕНТИФИКАЦИОНный номер для идентификации сеанса.</span><span class="sxs-lookup"><span data-stu-id="abce2-163">ID number to identify the session.</span></span> <span data-ttu-id="abce2-164">Используется в сочетании с SessionIdTime для уникальной идентификации сеанса.</span><span class="sxs-lookup"><span data-stu-id="abce2-164">Used in conjunction with SessionIdTime to uniquely identify a session.</span></span> <span data-ttu-id="abce2-165">Дополнительные сведения приведены <a href="lync-server-2013-dialogs-table.md">в таблице диалоговые окна Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="abce2-165">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="abce2-166"><strong>DialogId</strong></span><span class="sxs-lookup"><span data-stu-id="abce2-166"><strong>DialogId</strong></span></span></p></td>
<td><p><span data-ttu-id="abce2-167">varchar (775)</span><span class="sxs-lookup"><span data-stu-id="abce2-167">varchar(775)</span></span></p></td>
<td><p><span data-ttu-id="abce2-168">ИДЕНТИФИКАТОР диалогового окна SIP для сеанса.</span><span class="sxs-lookup"><span data-stu-id="abce2-168">SIP dialog ID of the session.</span></span> <span data-ttu-id="abce2-169">Формат: диалоговое окно; тег.</span><span class="sxs-lookup"><span data-stu-id="abce2-169">The format is: dialog;from-tag;to-tag.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="abce2-170"><strong>UserJoinTime</strong></span><span class="sxs-lookup"><span data-stu-id="abce2-170"><strong>UserJoinTime</strong></span></span></p></td>
<td><p><span data-ttu-id="abce2-171">datetime</span><span class="sxs-lookup"><span data-stu-id="abce2-171">datetime</span></span></p></td>
<td><p><span data-ttu-id="abce2-172">Время присоединения пользователя к серверу конференц-связи.</span><span class="sxs-lookup"><span data-stu-id="abce2-172">Time the user joined the conferencing server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="abce2-173"><strong>UserLeaveTime</strong></span><span class="sxs-lookup"><span data-stu-id="abce2-173"><strong>UserLeaveTime</strong></span></span></p></td>
<td><p><span data-ttu-id="abce2-174">datetime</span><span class="sxs-lookup"><span data-stu-id="abce2-174">datetime</span></span></p></td>
<td><p><span data-ttu-id="abce2-175">Время, когда пользователь оставил сервер конференц-связи.</span><span class="sxs-lookup"><span data-stu-id="abce2-175">Time the user left the conferencing server.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="abce2-176">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="abce2-176">


</div>

<span> </span>

</div>

</div>

</span></span></div>

