---
title: 'Lync Server 2013: представление SessionDetails'
description: 'Lync Server 2013: SessionDetails View.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: SessionDetails view
ms:assetid: ea328c6f-cf22-48dd-8f7f-f1666c9148c8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721924(v=OCS.15)
ms:contentKeyID: 49733859
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4c9f657257e54389defb805919be61adbdecad74
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424032"
---
# <a name="sessiondetails-view-in-lync-server-2013"></a><span data-ttu-id="5ce29-103">SessionDetails представления в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5ce29-103">SessionDetails view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5ce29-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5ce29-104">

<span> </span></span></span>

<span data-ttu-id="5ce29-105">_**Тема последнего изменения:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="5ce29-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="5ce29-106">В представлении SessionDetails хранятся сведения о одноранговых сеансах, VoIP-VoIP а также о телефонном звонке, о двустороннем сеансе обмена мгновенными сообщениями или сеансах другого типа.</span><span class="sxs-lookup"><span data-stu-id="5ce29-106">The SessionDetails view stores information about peer-to-peer sessions, which could be a VoIP-VoIP phone call, two-party IM session, or other type of session.</span></span> <span data-ttu-id="5ce29-107">Это представление было представлено в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="5ce29-107">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5ce29-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="5ce29-108">Column</span></span></th>
<th><span data-ttu-id="5ce29-109">Тип данных</span><span class="sxs-lookup"><span data-stu-id="5ce29-109">Data Type</span></span></th>
<th><span data-ttu-id="5ce29-110">Подробности</span><span class="sxs-lookup"><span data-stu-id="5ce29-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5ce29-111"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="5ce29-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="5ce29-112">datetime</span><span class="sxs-lookup"><span data-stu-id="5ce29-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="5ce29-113">Время запроса сеанса.</span><span class="sxs-lookup"><span data-stu-id="5ce29-113">Time of session request.</span></span> <span data-ttu-id="5ce29-114">Используется в сочетании с SessionIdSeq для уникальной идентификации сеанса.</span><span class="sxs-lookup"><span data-stu-id="5ce29-114">Used in conjunction with SessionIdSeq to uniquely identify a session.</span></span> <span data-ttu-id="5ce29-115">Дополнительные сведения приведены <a href="lync-server-2013-dialogs-table.md">в таблице диалоговые окна в таблице Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="5ce29-115">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> Table for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ce29-116"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="5ce29-116"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="5ce29-117">целое</span><span class="sxs-lookup"><span data-stu-id="5ce29-117">int</span></span></p></td>
<td><p><span data-ttu-id="5ce29-118">ИДЕНТИФИКАЦИОНный номер для идентификации сеанса.</span><span class="sxs-lookup"><span data-stu-id="5ce29-118">ID number to identify the session.</span></span> <span data-ttu-id="5ce29-119">Используется в сочетании с SessionIdTime для уникальной идентификации сеанса.</span><span class="sxs-lookup"><span data-stu-id="5ce29-119">Used in conjunction with SessionIdTime to uniquely identify a session.</span></span> <span data-ttu-id="5ce29-120">Дополнительные сведения приведены <a href="lync-server-2013-dialogs-table.md">в таблице диалоговые окна Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="5ce29-120">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ce29-121"><strong>InviteTime</strong></span><span class="sxs-lookup"><span data-stu-id="5ce29-121"><strong>InviteTime</strong></span></span></p></td>
<td><p><span data-ttu-id="5ce29-122">datetime</span><span class="sxs-lookup"><span data-stu-id="5ce29-122">datetime</span></span></p></td>
<td><p><span data-ttu-id="5ce29-123">Время первого запроса приглашения.</span><span class="sxs-lookup"><span data-stu-id="5ce29-123">Time of the first INVITE request.</span></span> <span data-ttu-id="5ce29-124">Это поле обычно заполняется данными, созданными на основе исходного сообщения INVITE в сеансе.</span><span class="sxs-lookup"><span data-stu-id="5ce29-124">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="5ce29-125">Если сообщение приглашения отсутствует, поле заполняется датой и временем первого соответствующего сообщения SIP (пока, CANCEL, MESSAGE или INFO).</span><span class="sxs-lookup"><span data-stu-id="5ce29-125">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span> <span data-ttu-id="5ce29-126">Это поле обычно заполняется данными, созданными на основе исходного сообщения INVITE в сеансе.</span><span class="sxs-lookup"><span data-stu-id="5ce29-126">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="5ce29-127">Если сообщение приглашения отсутствует, поле заполняется датой и временем первого соответствующего сообщения SIP (пока, CANCEL, MESSAGE или INFO).</span><span class="sxs-lookup"><span data-stu-id="5ce29-127">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ce29-128"><strong>FromUri</strong></span><span class="sxs-lookup"><span data-stu-id="5ce29-128"><strong>FromUri</strong></span></span></p></td>
<td><p><span data-ttu-id="5ce29-129">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="5ce29-129">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="5ce29-130">URI пользователя, запустившего сеанс.</span><span class="sxs-lookup"><span data-stu-id="5ce29-130">URI of the user who started the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ce29-131"><strong>ToUri</strong></span><span class="sxs-lookup"><span data-stu-id="5ce29-131"><strong>ToUri</strong></span></span></p></td>
<td><p><span data-ttu-id="5ce29-132">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="5ce29-132">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="5ce29-133">Универсальный код ресурса (URI) пользователя, который присоединился к сеансу.</span><span class="sxs-lookup"><span data-stu-id="5ce29-133">URI of the user who joined the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ce29-134"><strong>FromUriType</strong></span><span class="sxs-lookup"><span data-stu-id="5ce29-134"><strong>FromUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="5ce29-135">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="5ce29-135">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="5ce29-136">Тип URI пользователя, запустившего сеанс.</span><span class="sxs-lookup"><span data-stu-id="5ce29-136">Type of URI of the user who started the session.</span></span> <span data-ttu-id="5ce29-137">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-uritypes-table.md">таблицей UriTypes в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="5ce29-137">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ce29-138"><strong>ToUriType</strong></span><span class="sxs-lookup"><span data-stu-id="5ce29-138"><strong>ToUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="5ce29-139">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="5ce29-139">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="5ce29-140">Тип URI пользователя, который присоединился к сеансу.</span><span class="sxs-lookup"><span data-stu-id="5ce29-140">Type of URI of the user who joined the session.</span></span> <span data-ttu-id="5ce29-141">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-uritypes-table.md">таблицей UriTypes в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="5ce29-141">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ce29-142"><strong>FromTenant</strong></span><span class="sxs-lookup"><span data-stu-id="5ce29-142"><strong>FromTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="5ce29-143">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="5ce29-143">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="5ce29-144">Клиент пользователя, который запустил сеанс.</span><span class="sxs-lookup"><span data-stu-id="5ce29-144">Tenant of the user who started the session.</span></span> <span data-ttu-id="5ce29-145">Дополнительные сведения приведены в <a href="lync-server-2013-tenants-table.md">таблице "клиенты" в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="5ce29-145">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ce29-146"><strong>ToTenant</strong></span><span class="sxs-lookup"><span data-stu-id="5ce29-146"><strong>ToTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="5ce29-147">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="5ce29-147">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="5ce29-148">Клиент пользователя, который присоединил сеанс.</span><span class="sxs-lookup"><span data-stu-id="5ce29-148">The tenant of the user who joined the session.</span></span> <span data-ttu-id="5ce29-149">Дополнительные сведения приведены в <a href="lync-server-2013-tenants-table.md">таблице "клиенты" в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="5ce29-149">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ce29-150"><strong>FromEndpointId</strong></span><span class="sxs-lookup"><span data-stu-id="5ce29-150"><strong>FromEndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="5ce29-151">идентификатора</span><span class="sxs-lookup"><span data-stu-id="5ce29-151">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="5ce29-152">Уникальный идентификатор конечной точки пользователя, который запустил сеанс.</span><span class="sxs-lookup"><span data-stu-id="5ce29-152">Unique identifier of the endpoint of the user who started the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ce29-153"><strong>ToEndpointId</strong></span><span class="sxs-lookup"><span data-stu-id="5ce29-153"><strong>ToEndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="5ce29-154">идентификатора</span><span class="sxs-lookup"><span data-stu-id="5ce29-154">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="5ce29-155">Уникальный идентификатор конечной точки пользователя, который присоединился к сеансу.</span><span class="sxs-lookup"><span data-stu-id="5ce29-155">Unique identifier of the endpoint of the user who joined the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ce29-156"><strong>EndTime</strong></span><span class="sxs-lookup"><span data-stu-id="5ce29-156"><strong>EndTime</strong></span></span></p></td>
<td><p><span data-ttu-id="5ce29-157">datetime</span><span class="sxs-lookup"><span data-stu-id="5ce29-157">datetime</span></span></p></td>
<td><p><span data-ttu-id="5ce29-158">Время окончания сеанса.</span><span class="sxs-lookup"><span data-stu-id="5ce29-158">End time of the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ce29-159"><strong>FromMessageCount</strong></span><span class="sxs-lookup"><span data-stu-id="5ce29-159"><strong>FromMessageCount</strong></span></span></p></td>
<td><p><span data-ttu-id="5ce29-160">целое</span><span class="sxs-lookup"><span data-stu-id="5ce29-160">int</span></span></p></td>
<td><p><span data-ttu-id="5ce29-161">Количество сообщений, отправленных пользователем, который запустил сеанс.</span><span class="sxs-lookup"><span data-stu-id="5ce29-161">Number of messages sent by the user who started the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ce29-162"><strong>ToMessageCount</strong></span><span class="sxs-lookup"><span data-stu-id="5ce29-162"><strong>ToMessageCount</strong></span></span></p></td>
<td><p><span data-ttu-id="5ce29-163">целое</span><span class="sxs-lookup"><span data-stu-id="5ce29-163">int</span></span></p></td>
<td><p><span data-ttu-id="5ce29-164">Количество сообщений, отправленных пользователем, который присоединился к сеансу.</span><span class="sxs-lookup"><span data-stu-id="5ce29-164">Number of messages sent by the user who joined the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ce29-165"><strong>FromClientVersion</strong></span><span class="sxs-lookup"><span data-stu-id="5ce29-165"><strong>FromClientVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="5ce29-166">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="5ce29-166">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="5ce29-167">Версия клиента, используемая пользователем, который запустил сеанс.</span><span class="sxs-lookup"><span data-stu-id="5ce29-167">Version of client used by the user who started the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ce29-168"><strong>FromClientType</strong></span><span class="sxs-lookup"><span data-stu-id="5ce29-168"><strong>FromClientType</strong></span></span></p></td>
<td><p><span data-ttu-id="5ce29-169">целое</span><span class="sxs-lookup"><span data-stu-id="5ce29-169">int</span></span></p></td>
<td><p><span data-ttu-id="5ce29-170">Клиент, используемый пользователем, который запустил сеанс.</span><span class="sxs-lookup"><span data-stu-id="5ce29-170">Client used by the user who started the session.</span></span> <span data-ttu-id="5ce29-171">Дополнительные сведения вы увидите <a href="lync-server-2013-useragentdef-table.md">в таблице UserAgentDef в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="5ce29-171">See the <a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a> for more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ce29-172"><strong>FromClientCategory</strong></span><span class="sxs-lookup"><span data-stu-id="5ce29-172"><strong>FromClientCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="5ce29-173">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="5ce29-173">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="5ce29-174">Имя категории клиента, используемой пользователем, который запустил сеанс.</span><span class="sxs-lookup"><span data-stu-id="5ce29-174">Name of the category of the client used by the user who started the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ce29-175"><strong>ToClientVersion</strong></span><span class="sxs-lookup"><span data-stu-id="5ce29-175"><strong>ToClientVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="5ce29-176">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="5ce29-176">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="5ce29-177">Версия клиента, используемая пользователем, который присоединился к сеансу</span><span class="sxs-lookup"><span data-stu-id="5ce29-177">Version of client used by the user who joined the session</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ce29-178"><strong>ToClientType</strong></span><span class="sxs-lookup"><span data-stu-id="5ce29-178"><strong>ToClientType</strong></span></span></p></td>
<td><p><span data-ttu-id="5ce29-179">целое</span><span class="sxs-lookup"><span data-stu-id="5ce29-179">int</span></span></p></td>
<td><p><span data-ttu-id="5ce29-180">Клиент, используемый пользователем, который присоединился к сеансу.</span><span class="sxs-lookup"><span data-stu-id="5ce29-180">Client used by the user who joined the session.</span></span> <span data-ttu-id="5ce29-181">Дополнительные сведения вы увидите <a href="lync-server-2013-useragentdef-table.md">в таблице UserAgentDef в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="5ce29-181">See the <a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a> for more details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ce29-182"><strong>ToClientCategory</strong></span><span class="sxs-lookup"><span data-stu-id="5ce29-182"><strong>ToClientCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="5ce29-183">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="5ce29-183">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="5ce29-184">Имя категории клиента, используемой пользователем, который присоединился к сеансу.</span><span class="sxs-lookup"><span data-stu-id="5ce29-184">Name of the category of the client used by the user who joined the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ce29-185"><strong>TargetUri</strong></span><span class="sxs-lookup"><span data-stu-id="5ce29-185"><strong>TargetUri</strong></span></span></p></td>
<td><p><span data-ttu-id="5ce29-186">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="5ce29-186">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="5ce29-187">Универсальный код ресурса (URI) целевого пользователя сеанса.</span><span class="sxs-lookup"><span data-stu-id="5ce29-187">URI of the target user of the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ce29-188"><strong>TargetUriType</strong></span><span class="sxs-lookup"><span data-stu-id="5ce29-188"><strong>TargetUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="5ce29-189">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="5ce29-189">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="5ce29-190">Тип универсального кода ресурса (URI) целевого пользователя для сеанса.</span><span class="sxs-lookup"><span data-stu-id="5ce29-190">Type of URI of the target user for the session.</span></span> <span data-ttu-id="5ce29-191">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-uritypes-table.md">таблицей UriTypes в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="5ce29-191">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ce29-192"><strong>OnBehalfOfUri</strong></span><span class="sxs-lookup"><span data-stu-id="5ce29-192"><strong>OnBehalfOfUri</strong></span></span></p></td>
<td><p><span data-ttu-id="5ce29-193">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="5ce29-193">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="5ce29-194">Универсальный код ресурса (URI) пользователя, от имени которого был запущен сеанс.</span><span class="sxs-lookup"><span data-stu-id="5ce29-194">URI of the user on whose behalf the session was started.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ce29-195"><strong>OnnnBehalfOfUriType</strong></span><span class="sxs-lookup"><span data-stu-id="5ce29-195"><strong>OnnnBehalfOfUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="5ce29-196">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="5ce29-196">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="5ce29-197">Тип универсального кода ресурса (URI) пользователя, от имени которого был запущен сеанс.</span><span class="sxs-lookup"><span data-stu-id="5ce29-197">Type of URI of the user on whose behalf the session was started.</span></span> <span data-ttu-id="5ce29-198">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-uritypes-table.md">таблицей UriTypes в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="5ce29-198">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ce29-199"><strong>OnBehalfOfTenant</strong></span><span class="sxs-lookup"><span data-stu-id="5ce29-199"><strong>OnBehalfOfTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="5ce29-200">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="5ce29-200">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="5ce29-201">Клиент пользователя, от имени которого был запущен сеанс.</span><span class="sxs-lookup"><span data-stu-id="5ce29-201">Tenant of the user whose on behalf the session was started.</span></span> <span data-ttu-id="5ce29-202">Дополнительные сведения приведены в <a href="lync-server-2013-tenants-table.md">таблице "клиенты" в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="5ce29-202">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ce29-203"><strong>ReferredByUri</strong></span><span class="sxs-lookup"><span data-stu-id="5ce29-203"><strong>ReferredByUri</strong></span></span></p></td>
<td><p><span data-ttu-id="5ce29-204">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="5ce29-204">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="5ce29-205">URI пользователя, который ссылался на сеанс.</span><span class="sxs-lookup"><span data-stu-id="5ce29-205">URI of the user who referred the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ce29-206"><strong>ReferredByUriType</strong></span><span class="sxs-lookup"><span data-stu-id="5ce29-206"><strong>ReferredByUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="5ce29-207">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="5ce29-207">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="5ce29-208">Тип URI пользователя, который ссылался на сеанс.</span><span class="sxs-lookup"><span data-stu-id="5ce29-208">Type of URI of the user who referred the session.</span></span> <span data-ttu-id="5ce29-209">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-uritypes-table.md">таблицей UriTypes в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="5ce29-209">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ce29-210"><strong>ReferredByTenant</strong></span><span class="sxs-lookup"><span data-stu-id="5ce29-210"><strong>ReferredByTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="5ce29-211">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="5ce29-211">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="5ce29-212">Клиент пользователя, который ссылался на сеанс.</span><span class="sxs-lookup"><span data-stu-id="5ce29-212">Tenant of the user who referred the session.</span></span> <span data-ttu-id="5ce29-213">Дополнительные сведения приведены в <a href="lync-server-2013-tenants-table.md">таблице "клиенты" в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="5ce29-213">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ce29-214"><strong>DialogId</strong></span><span class="sxs-lookup"><span data-stu-id="5ce29-214"><strong>DialogId</strong></span></span></p></td>
<td><p><span data-ttu-id="5ce29-215">varchar (775)</span><span class="sxs-lookup"><span data-stu-id="5ce29-215">varchar(775)</span></span></p></td>
<td><p><span data-ttu-id="5ce29-216">ИДЕНТИФИКАТОР диалогового окна SIP.</span><span class="sxs-lookup"><span data-stu-id="5ce29-216">SIP dialog ID.</span></span> <span data-ttu-id="5ce29-217">Формат:</span><span class="sxs-lookup"><span data-stu-id="5ce29-217">The format is:</span></span></p>
<p><span data-ttu-id="5ce29-218">диалоговое окно; тег "from-Tag"</span><span class="sxs-lookup"><span data-stu-id="5ce29-218">dialog;from-tag;to-tag</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ce29-219"><strong>Корреляци</strong></span><span class="sxs-lookup"><span data-stu-id="5ce29-219"><strong>CorrelationId</strong></span></span></p></td>
<td><p><span data-ttu-id="5ce29-220">идентификатора</span><span class="sxs-lookup"><span data-stu-id="5ce29-220">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="5ce29-221">GUID, используемый для корреляции нескольких сеансов.</span><span class="sxs-lookup"><span data-stu-id="5ce29-221">GUID used to correlate multiple sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ce29-222"><strong>ReplaceDialogIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="5ce29-222"><strong>ReplaceDialogIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="5ce29-223">datetime</span><span class="sxs-lookup"><span data-stu-id="5ce29-223">datetime</span></span></p></td>
<td><p><span data-ttu-id="5ce29-224">Время, когда диалоговое окно было заменено сеансом.</span><span class="sxs-lookup"><span data-stu-id="5ce29-224">Time of the dialog which was replaced by the session.</span></span> <span data-ttu-id="5ce29-225">Используется в сочетании с ReplaceDialogIdSeq для уникальной идентификации диалогового окна, которое заменяется сеансом.</span><span class="sxs-lookup"><span data-stu-id="5ce29-225">Used in conjunction with ReplaceDialogIdSeq to uniquely identify a dialog that is replaced by the session.</span></span> <span data-ttu-id="5ce29-226">Дополнительные сведения приведены <a href="lync-server-2013-dialogs-table.md">в таблице диалоговые окна Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="5ce29-226">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ce29-227"><strong>ReplaceDialogIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="5ce29-227"><strong>ReplaceDialogIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="5ce29-228">целое</span><span class="sxs-lookup"><span data-stu-id="5ce29-228">int</span></span></p></td>
<td><p><span data-ttu-id="5ce29-229">ИДЕНТИФИКАЦИОНный номер для идентификации сеанса.</span><span class="sxs-lookup"><span data-stu-id="5ce29-229">ID number to identify the session.</span></span> <span data-ttu-id="5ce29-230">Используется в сочетании с ReplaceDialogIdTime для уникальной идентификации диалогового окна, которое заменяется сеансом.</span><span class="sxs-lookup"><span data-stu-id="5ce29-230">Used in conjunction with ReplaceDialogIdTime to uniquely identify a dialog that is replaced by the session.</span></span> <span data-ttu-id="5ce29-231">Дополнительные сведения приведены <a href="lync-server-2013-dialogs-table.md">в таблице диалоговые окна Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="5ce29-231">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ce29-232"><strong>ReplacesDialogId</strong></span><span class="sxs-lookup"><span data-stu-id="5ce29-232"><strong>ReplacesDialogId</strong></span></span></p></td>
<td><p><span data-ttu-id="5ce29-233">varchar (775)</span><span class="sxs-lookup"><span data-stu-id="5ce29-233">varchar(775)</span></span></p></td>
<td><p><span data-ttu-id="5ce29-234">ИДЕНТИФИКАТОР диалогового окна SIP, в котором будет заменяться сеанс.</span><span class="sxs-lookup"><span data-stu-id="5ce29-234">SIP dialog ID the session replaces.</span></span> <span data-ttu-id="5ce29-235">Формат:</span><span class="sxs-lookup"><span data-stu-id="5ce29-235">The format is:</span></span></p>
<p><span data-ttu-id="5ce29-236">диалоговое окно; тег "from-Tag"</span><span class="sxs-lookup"><span data-stu-id="5ce29-236">dialog;from-tag;to-tag</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ce29-237"><strong>ResponseTime</strong></span><span class="sxs-lookup"><span data-stu-id="5ce29-237"><strong>ResponseTime</strong></span></span></p></td>
<td><p><span data-ttu-id="5ce29-238">datetime</span><span class="sxs-lookup"><span data-stu-id="5ce29-238">datetime</span></span></p></td>
<td><p><span data-ttu-id="5ce29-239">Время ответа на первое сообщение приглашения.</span><span class="sxs-lookup"><span data-stu-id="5ce29-239">Time of the response to the first INVITE message.</span></span> <span data-ttu-id="5ce29-240">Это поле обычно заполняется данными, созданными на основе исходного сообщения INVITE в сеансе.</span><span class="sxs-lookup"><span data-stu-id="5ce29-240">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="5ce29-241">Если сообщение приглашения отсутствует, поле заполняется датой и временем первого соответствующего сообщения SIP (пока, CANCEL, MESSAGE или INFO).</span><span class="sxs-lookup"><span data-stu-id="5ce29-241">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ce29-242"><strong>ResponseCode</strong></span><span class="sxs-lookup"><span data-stu-id="5ce29-242"><strong>ResponseCode</strong></span></span></p></td>
<td><p><span data-ttu-id="5ce29-243">целое</span><span class="sxs-lookup"><span data-stu-id="5ce29-243">int</span></span></p></td>
<td><p><span data-ttu-id="5ce29-244">Код ответа SIP на приглашение на сеанс.</span><span class="sxs-lookup"><span data-stu-id="5ce29-244">SIP response code to the session invitation.</span></span> <span data-ttu-id="5ce29-245">Это поле обычно заполняется данными, созданными на основе исходного сообщения INVITE в сеансе.</span><span class="sxs-lookup"><span data-stu-id="5ce29-245">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="5ce29-246">Если сообщение приглашения отсутствует, поле заполняется датой и временем первого соответствующего сообщения SIP (пока, CANCEL, MESSAGE или INFO).</span><span class="sxs-lookup"><span data-stu-id="5ce29-246">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ce29-247"><strong>DiagnosticId</strong></span><span class="sxs-lookup"><span data-stu-id="5ce29-247"><strong>DiagnosticId</strong></span></span></p></td>
<td><p><span data-ttu-id="5ce29-248">целое</span><span class="sxs-lookup"><span data-stu-id="5ce29-248">int</span></span></p></td>
<td><p><span data-ttu-id="5ce29-249">Идентификатор диагностики, полученный из заголовков SIP.</span><span class="sxs-lookup"><span data-stu-id="5ce29-249">Diagnostic ID captured from SIP headers.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ce29-250"><strong>Контента</strong></span><span class="sxs-lookup"><span data-stu-id="5ce29-250"><strong>ContentType</strong></span></span></p></td>
<td><p><span data-ttu-id="5ce29-251">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="5ce29-251">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="5ce29-252">Тип контента для сеанса.</span><span class="sxs-lookup"><span data-stu-id="5ce29-252">Type of content for the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ce29-253"><strong>FrontEnd</strong></span><span class="sxs-lookup"><span data-stu-id="5ce29-253"><strong>FrontEnd</strong></span></span></p></td>
<td><p><span data-ttu-id="5ce29-254">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="5ce29-254">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="5ce29-255">Полное доменное имя сервера переднего плана, который захватил данные для сеанса.</span><span class="sxs-lookup"><span data-stu-id="5ce29-255">FQDN of the Front End server that captured the data for the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ce29-256"><strong>Pool</strong></span><span class="sxs-lookup"><span data-stu-id="5ce29-256"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="5ce29-257">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="5ce29-257">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="5ce29-258">Полное доменное имя пула, который захватывает данные для сеанса.</span><span class="sxs-lookup"><span data-stu-id="5ce29-258">FQDN of the pool that captured the data for the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ce29-259"><strong>FromEdgeServer</strong></span><span class="sxs-lookup"><span data-stu-id="5ce29-259"><strong>FromEdgeServer</strong></span></span></p></td>
<td><p><span data-ttu-id="5ce29-260">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="5ce29-260">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="5ce29-261">Полное доменное имя пограничного сервера, используемое пользователем, который запустил сеанс.</span><span class="sxs-lookup"><span data-stu-id="5ce29-261">FQDN of the Edge server used by the user who started the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ce29-262"><strong>ToEdgeServer</strong></span><span class="sxs-lookup"><span data-stu-id="5ce29-262"><strong>ToEdgeServer</strong></span></span></p></td>
<td><p><span data-ttu-id="5ce29-263">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="5ce29-263">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="5ce29-264">Полное доменное имя пограничного сервера, используемое пользователем, который запустил сеанс</span><span class="sxs-lookup"><span data-stu-id="5ce29-264">FQDN of the Edge server used by the user who started the session</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ce29-265"><strong>IsFromInternal</strong></span><span class="sxs-lookup"><span data-stu-id="5ce29-265"><strong>IsFromInternal</strong></span></span></p></td>
<td><p><span data-ttu-id="5ce29-266">бит</span><span class="sxs-lookup"><span data-stu-id="5ce29-266">bit</span></span></p></td>
<td><p><span data-ttu-id="5ce29-267">Указывает, вошел ли пользователь, запустивший сеанс, с помощью внутренней сети.</span><span class="sxs-lookup"><span data-stu-id="5ce29-267">Indicates whether the user who started the session logged on from the internal network.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ce29-268"><strong>IsToInternal</strong></span><span class="sxs-lookup"><span data-stu-id="5ce29-268"><strong>IsToInternal</strong></span></span></p></td>
<td><p><span data-ttu-id="5ce29-269">бит</span><span class="sxs-lookup"><span data-stu-id="5ce29-269">bit</span></span></p></td>
<td><p><span data-ttu-id="5ce29-270">Указывает, вошел ли пользователь, который присоединился к сеансу, из внутренней сети.</span><span class="sxs-lookup"><span data-stu-id="5ce29-270">Indicates whether the user who joined the session logged on from the internal network.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ce29-271"><strong>CallPriority</strong></span><span class="sxs-lookup"><span data-stu-id="5ce29-271"><strong>CallPriority</strong></span></span></p></td>
<td><p><span data-ttu-id="5ce29-272">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="5ce29-272">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="5ce29-273">Приоритет звонка для сеанса.</span><span class="sxs-lookup"><span data-stu-id="5ce29-273">Call priority of the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ce29-274"><strong>FromUserFlag</strong></span><span class="sxs-lookup"><span data-stu-id="5ce29-274"><strong>FromUserFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="5ce29-275">smallint</span><span class="sxs-lookup"><span data-stu-id="5ce29-275">smallint</span></span></p></td>
<td><p><span data-ttu-id="5ce29-276">Указывает атрибуты пользователя, который запустил сеанс.</span><span class="sxs-lookup"><span data-stu-id="5ce29-276">Indicates the attributes of the user who started the session.</span></span> <span data-ttu-id="5ce29-277">Допустимы следующие определения атрибутов:</span><span class="sxs-lookup"><span data-stu-id="5ce29-277">The following attribute definitions are allowed:</span></span></p>
<p><span data-ttu-id="5ce29-278">0x01 — интеграция с настольным телефоном</span><span class="sxs-lookup"><span data-stu-id="5ce29-278">0x01 - Integrated with desktop phone</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ce29-279"><strong>ToUserFlag</strong></span><span class="sxs-lookup"><span data-stu-id="5ce29-279"><strong>ToUserFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="5ce29-280">smallint</span><span class="sxs-lookup"><span data-stu-id="5ce29-280">smallint</span></span></p></td>
<td><p><span data-ttu-id="5ce29-281">Указывает атрибуты пользователя, который запустил сеанс.</span><span class="sxs-lookup"><span data-stu-id="5ce29-281">Indicates the attributes of the user who started the session.</span></span> <span data-ttu-id="5ce29-282">Допустимы следующие определения атрибутов:</span><span class="sxs-lookup"><span data-stu-id="5ce29-282">The following attribute definitions are allowed:</span></span></p>
<p><span data-ttu-id="5ce29-283">0x01 — интеграция с настольным телефоном</span><span class="sxs-lookup"><span data-stu-id="5ce29-283">0x01 - Integrated with desktop phone</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ce29-284"><strong>CallFlag</strong></span><span class="sxs-lookup"><span data-stu-id="5ce29-284"><strong>CallFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="5ce29-285">smallint</span><span class="sxs-lookup"><span data-stu-id="5ce29-285">smallint</span></span></p></td>
<td><p><span data-ttu-id="5ce29-286">Указывает атрибуты вызова.</span><span class="sxs-lookup"><span data-stu-id="5ce29-286">Indicates the call attributes.</span></span> <span data-ttu-id="5ce29-287">Допустимы следующие определения атрибутов:</span><span class="sxs-lookup"><span data-stu-id="5ce29-287">The following attribute definitions are allowed:</span></span></p>
<p><span data-ttu-id="5ce29-288">0x01 — сеанс повторной попытки</span><span class="sxs-lookup"><span data-stu-id="5ce29-288">0x01 - Retried Session</span></span></p>
<p><span data-ttu-id="5ce29-289">0x02 — вызов, сделанный агентом от имени группы ответа</span><span class="sxs-lookup"><span data-stu-id="5ce29-289">0x02 - A call made by agent on behalf of a Response Group</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ce29-290"><strong>Расположение</strong></span><span class="sxs-lookup"><span data-stu-id="5ce29-290"><strong>Location</strong></span></span></p></td>
<td><p><span data-ttu-id="5ce29-291">varchar (max)</span><span class="sxs-lookup"><span data-stu-id="5ce29-291">varchar(max)</span></span></p></td>
<td><p><span data-ttu-id="5ce29-292">Место вызова экстренной помощи.</span><span class="sxs-lookup"><span data-stu-id="5ce29-292">Location of emergency call.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="5ce29-293">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5ce29-293">


</div>

<span> </span>

</div>

</div>

</span></span></div>

