---
title: 'Lync Server 2013: представление FocusJoinsAndLeaves'
description: 'Lync Server 2013: FocusJoinsAndLeaves View.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: FocusJoinsAndLeaves view
ms:assetid: 226460ef-766f-4d61-80cb-f332b65a210d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687992(v=OCS.15)
ms:contentKeyID: 49733582
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c6f68c44461e378e9ebedce1305ee6b384a7a8a7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428112"
---
# <a name="focusjoinsandleaves-view-in-lync-server-2013"></a><span data-ttu-id="67f66-103">FocusJoinsAndLeaves представления в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="67f66-103">FocusJoinsAndLeaves view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="67f66-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="67f66-104">

<span> </span></span></span>

<span data-ttu-id="67f66-105">_**Тема последнего изменения:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="67f66-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="67f66-106">В представлении FocusJoinsAndLeaves хранятся сведения о присоединениях и оставлении данных для одной конференции.</span><span class="sxs-lookup"><span data-stu-id="67f66-106">The FocusJoinsAndLeaves view stores information about join and leave information for one conference.</span></span> <span data-ttu-id="67f66-107">Каждое собрание представлено в этом представлении записью, которая записывается каждый раз, когда пользователь присоединяется к Конференции, и оставляет ее.</span><span class="sxs-lookup"><span data-stu-id="67f66-107">Each conference is represented in this view by a record written each time a user joins and leaves the conference.</span></span> <span data-ttu-id="67f66-108">Это представление было представлено в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="67f66-108">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="67f66-109">Столбец</span><span class="sxs-lookup"><span data-stu-id="67f66-109">Column</span></span></th>
<th><span data-ttu-id="67f66-110">Тип данных</span><span class="sxs-lookup"><span data-stu-id="67f66-110">Data Type</span></span></th>
<th><span data-ttu-id="67f66-111">Подробности</span><span class="sxs-lookup"><span data-stu-id="67f66-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="67f66-112"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="67f66-112"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="67f66-113">datetime</span><span class="sxs-lookup"><span data-stu-id="67f66-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="67f66-114">Время экземпляра Конференции.</span><span class="sxs-lookup"><span data-stu-id="67f66-114">Time of conference instance.</span></span> <span data-ttu-id="67f66-115">Используется в сочетании с SessionIdSeq для уникальной идентификации экземпляра Конференции.</span><span class="sxs-lookup"><span data-stu-id="67f66-115">Used in conjunction with SessionIdSeq to uniquely identify a conference instance.</span></span> <span data-ttu-id="67f66-116">Дополнительные сведения приведены <a href="lync-server-2013-conferences-table.md">в таблице конференции для Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="67f66-116">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67f66-117"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="67f66-117"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="67f66-118">целое</span><span class="sxs-lookup"><span data-stu-id="67f66-118">int</span></span></p></td>
<td><p><span data-ttu-id="67f66-119">ИДЕНТИФИКАЦИОНный номер для идентификации экземпляра Конференции.</span><span class="sxs-lookup"><span data-stu-id="67f66-119">ID number to identify the conference instance.</span></span> <span data-ttu-id="67f66-120">Используется в сочетании с SessionIdTime для уникальной идентификации экземпляра Конференции.</span><span class="sxs-lookup"><span data-stu-id="67f66-120">Used in conjunction with SessionIdTime to uniquely identify a conference instance.</span></span> <span data-ttu-id="67f66-121">Дополнительные сведения приведены <a href="lync-server-2013-conferences-table.md">в таблице конференции для Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="67f66-121">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67f66-122"><strong>UserUri</strong></span><span class="sxs-lookup"><span data-stu-id="67f66-122"><strong>UserUri</strong></span></span></p></td>
<td><p><span data-ttu-id="67f66-123">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="67f66-123">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="67f66-124">Универсальный код ресурса (URI), на который были собраны сведения о присоединении или закрытии Конференции.</span><span class="sxs-lookup"><span data-stu-id="67f66-124">URI of the user whose conference join/leave information was captured.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67f66-125"><strong>UserUriType</strong></span><span class="sxs-lookup"><span data-stu-id="67f66-125"><strong>UserUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="67f66-126">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="67f66-126">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="67f66-127">Тип универсального кода ресурса (URI), на который были собраны сведения о приходе или закрытии Конференции.</span><span class="sxs-lookup"><span data-stu-id="67f66-127">Type of URI of the user whose conference join/leave information was captured.</span></span> <span data-ttu-id="67f66-128">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-uritypes-table.md">таблицей UriTypes в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="67f66-128">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67f66-129"><strong>UserTenant</strong></span><span class="sxs-lookup"><span data-stu-id="67f66-129"><strong>UserTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="67f66-130">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="67f66-130">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="67f66-131">Клиент для пользователя, которому были собраны сведения о присоединении к Конференции или выходе из нее.</span><span class="sxs-lookup"><span data-stu-id="67f66-131">Tenant of the user whose conference join/leave information was captured.</span></span> <span data-ttu-id="67f66-132">Дополнительные сведения приведены в <a href="lync-server-2013-tenants-table.md">таблице "клиенты" в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="67f66-132">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67f66-133"><strong>UserEndpointId</strong></span><span class="sxs-lookup"><span data-stu-id="67f66-133"><strong>UserEndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="67f66-134">идентификатора</span><span class="sxs-lookup"><span data-stu-id="67f66-134">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="67f66-135">Уникальный идентификатор пользователя, для которого была собрана информация о присоединении к Конференции или выходе из нее.</span><span class="sxs-lookup"><span data-stu-id="67f66-135">Unique identifier of the user whose conference join/leave information was captured.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67f66-136"><strong>UserClientVersion</strong></span><span class="sxs-lookup"><span data-stu-id="67f66-136"><strong>UserClientVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="67f66-137">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="67f66-137">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="67f66-138">Версия клиента, используемая пользователем, для которого была собрана информация о присоединении к Конференции или выходе из нее.</span><span class="sxs-lookup"><span data-stu-id="67f66-138">Version of client used by the user whose conference join/leave information was captured.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67f66-139"><strong>UserClientType</strong></span><span class="sxs-lookup"><span data-stu-id="67f66-139"><strong>UserClientType</strong></span></span></p></td>
<td><p><span data-ttu-id="67f66-140">целое</span><span class="sxs-lookup"><span data-stu-id="67f66-140">int</span></span></p></td>
<td><p><span data-ttu-id="67f66-141">Клиент, используемый пользователем, для которого были собраны сведения о присоединении к Конференции или выходе из нее.</span><span class="sxs-lookup"><span data-stu-id="67f66-141">Client used by the user whose conference join/leave information was captured.</span></span> <span data-ttu-id="67f66-142">Для получения дополнительных сведений ознакомьтесь <a href="lync-server-2013-useragentdef-table.md">с таблицей UserAgentDef в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="67f66-142">See <a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a> for more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67f66-143"><strong>UserClientCategory</strong></span><span class="sxs-lookup"><span data-stu-id="67f66-143"><strong>UserClientCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="67f66-144">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="67f66-144">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="67f66-145">Имя категории клиента, используемой пользователем, для которого были собраны сведения о приходе или закрытии Конференции.</span><span class="sxs-lookup"><span data-stu-id="67f66-145">Name of the category of the client used by the user whose conference join/leave information was captured.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67f66-146"><strong>FocusUserInstance</strong></span><span class="sxs-lookup"><span data-stu-id="67f66-146"><strong>FocusUserInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="67f66-147">целое</span><span class="sxs-lookup"><span data-stu-id="67f66-147">int</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67f66-148"><strong>IsuserInternal</strong></span><span class="sxs-lookup"><span data-stu-id="67f66-148"><strong>IsuserInternal</strong></span></span></p></td>
<td><p><span data-ttu-id="67f66-149">бит</span><span class="sxs-lookup"><span data-stu-id="67f66-149">bit</span></span></p></td>
<td><p><span data-ttu-id="67f66-150">Бит, обозначающий, является ли пользователь внутренним.</span><span class="sxs-lookup"><span data-stu-id="67f66-150">Bit that represents whether the user is an internal user or not.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67f66-151"><strong>DialogSessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="67f66-151"><strong>DialogSessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="67f66-152">datetime</span><span class="sxs-lookup"><span data-stu-id="67f66-152">datetime</span></span></p></td>
<td><p><span data-ttu-id="67f66-153">Время запроса сеанса.</span><span class="sxs-lookup"><span data-stu-id="67f66-153">Time of session request.</span></span> <span data-ttu-id="67f66-154">Используется в сочетании с SessionIdSeq для уникальной идентификации сеанса.</span><span class="sxs-lookup"><span data-stu-id="67f66-154">Used in conjunction with SessionIdSeq to uniquely identify a session.</span></span> <span data-ttu-id="67f66-155">Дополнительные сведения приведены <a href="lync-server-2013-dialogs-table.md">в таблице диалоговые окна Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="67f66-155">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67f66-156"><strong>DialogSessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="67f66-156"><strong>DialogSessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="67f66-157">целое</span><span class="sxs-lookup"><span data-stu-id="67f66-157">int</span></span></p></td>
<td><p><span data-ttu-id="67f66-158">Если пользователь входит в систему на нескольких компьютерах или устройствах одновременно, UserInstance используется для уникальной идентификации комбинации пользователей и устройств.</span><span class="sxs-lookup"><span data-stu-id="67f66-158">If a user is logged on at multiple computers or devices at the same time, UserInstance is used to uniquely identify the user/device combination.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67f66-159"><strong>DialogId</strong></span><span class="sxs-lookup"><span data-stu-id="67f66-159"><strong>DialogId</strong></span></span></p></td>
<td><p><span data-ttu-id="67f66-160">varchar (775)</span><span class="sxs-lookup"><span data-stu-id="67f66-160">varchar(775)</span></span></p></td>
<td><p><span data-ttu-id="67f66-161">ИДЕНТИФИКАТОР диалогового окна SIP для сеанса.</span><span class="sxs-lookup"><span data-stu-id="67f66-161">SIP dialog ID of the session.</span></span> <span data-ttu-id="67f66-162">Формат: диалоговое окно; тег.</span><span class="sxs-lookup"><span data-stu-id="67f66-162">The format is: dialog;from-tag;to-tag.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67f66-163"><strong>UserJoinTime</strong></span><span class="sxs-lookup"><span data-stu-id="67f66-163"><strong>UserJoinTime</strong></span></span></p></td>
<td><p><span data-ttu-id="67f66-164">datetime</span><span class="sxs-lookup"><span data-stu-id="67f66-164">datetime</span></span></p></td>
<td><p><span data-ttu-id="67f66-165">Время, в которое пользователь присоединился к Конференции.</span><span class="sxs-lookup"><span data-stu-id="67f66-165">Time that the user joined the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67f66-166"><strong>UserLeaveTime</strong></span><span class="sxs-lookup"><span data-stu-id="67f66-166"><strong>UserLeaveTime</strong></span></span></p></td>
<td><p><span data-ttu-id="67f66-167">datetime</span><span class="sxs-lookup"><span data-stu-id="67f66-167">datetime</span></span></p></td>
<td><p><span data-ttu-id="67f66-168">Время, когда пользователь оставил Конференцию.</span><span class="sxs-lookup"><span data-stu-id="67f66-168">Time that the user left the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67f66-169"><strong>UserRole</strong></span><span class="sxs-lookup"><span data-stu-id="67f66-169"><strong>UserRole</strong></span></span></p></td>
<td><p><span data-ttu-id="67f66-170">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="67f66-170">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="67f66-171">Роль пользователя на Конференции, например докладчика или участника.</span><span class="sxs-lookup"><span data-stu-id="67f66-171">User’s role in the conference, such as Presenter or Attendee.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="67f66-172">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="67f66-172">


</div>

<span> </span>

</div>

</div>

</span></span></div>

