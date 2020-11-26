---
title: 'Lync Server 2013: представление ErrorReport'
description: 'Lync Server 2013: ErrorReport View.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ErrorReport view
ms:assetid: ca873f7e-b18b-4eaf-8db0-5f9d5a9b60a1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721887(v=OCS.15)
ms:contentKeyID: 49733821
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 50fb0a362c71d8dfb5873157e7b1ed3d3eb680ae
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428526"
---
# <a name="errorreport-view-in-lync-server-2013"></a><span data-ttu-id="eb400-103">ErrorReport представления в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="eb400-103">ErrorReport view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="eb400-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="eb400-104">

<span> </span></span></span>

<span data-ttu-id="eb400-105">_**Тема последнего изменения:** 2013-01-22_</span><span class="sxs-lookup"><span data-stu-id="eb400-105">_**Topic Last Modified:** 2013-01-22_</span></span>

<span data-ttu-id="eb400-106">В представлении ErrorReport хранятся сведения об ошибках, о которых сообщается.</span><span class="sxs-lookup"><span data-stu-id="eb400-106">The ErrorReport view stores information about errors reported.</span></span> <span data-ttu-id="eb400-107">Каждая запись содержит один экземпляр ошибки.</span><span class="sxs-lookup"><span data-stu-id="eb400-107">Each record is one error occurrence.</span></span> <span data-ttu-id="eb400-108">Эти ошибки регистрируются агентом CDR, который запущен на сервере переднего плана или отправлен клиентом.</span><span class="sxs-lookup"><span data-stu-id="eb400-108">The errors are captured either by the CDR agent running on the front-end server or sent from the client.</span></span> <span data-ttu-id="eb400-109">Это представление было представлено в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="eb400-109">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="eb400-110">Столбец</span><span class="sxs-lookup"><span data-stu-id="eb400-110">Column</span></span></th>
<th><span data-ttu-id="eb400-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="eb400-111">Data Type</span></span></th>
<th><span data-ttu-id="eb400-112">Подробности</span><span class="sxs-lookup"><span data-stu-id="eb400-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eb400-113"><strong>ErrorTime</strong></span><span class="sxs-lookup"><span data-stu-id="eb400-113"><strong>ErrorTime</strong></span></span></p></td>
<td><p><span data-ttu-id="eb400-114">datetime</span><span class="sxs-lookup"><span data-stu-id="eb400-114">datetime</span></span></p></td>
<td><p><span data-ttu-id="eb400-115">Время возникновения ошибки.</span><span class="sxs-lookup"><span data-stu-id="eb400-115">Time of error occurred.</span></span> <span data-ttu-id="eb400-116">Используется в сочетании с ErrorReportSeq для уникальной идентификации ошибки.</span><span class="sxs-lookup"><span data-stu-id="eb400-116">Used in conjunction with ErrorReportSeq to uniquely identify an error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb400-117"><strong>ErrorReportSeq</strong></span><span class="sxs-lookup"><span data-stu-id="eb400-117"><strong>ErrorReportSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="eb400-118">целое</span><span class="sxs-lookup"><span data-stu-id="eb400-118">int</span></span></p></td>
<td><p><span data-ttu-id="eb400-119">ИДЕНТИФИКАЦИОНный номер для идентификации ошибки.</span><span class="sxs-lookup"><span data-stu-id="eb400-119">ID number to identify the error.</span></span> <span data-ttu-id="eb400-120">Используется в сочетании с ErrorTime для уникальной идентификации ошибки.</span><span class="sxs-lookup"><span data-stu-id="eb400-120">Used in conjunction with ErrorTime to uniquely identify an error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb400-121"><strong>MsDiagId</strong></span><span class="sxs-lookup"><span data-stu-id="eb400-121"><strong>MsDiagId</strong></span></span></p></td>
<td><p><span data-ttu-id="eb400-122">целое</span><span class="sxs-lookup"><span data-stu-id="eb400-122">int</span></span></p></td>
<td><p><span data-ttu-id="eb400-123">Идентификатор диагностики для отчета об ошибке.</span><span class="sxs-lookup"><span data-stu-id="eb400-123">Diagnostic ID for the error report.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb400-124"><strong>FromUri</strong></span><span class="sxs-lookup"><span data-stu-id="eb400-124"><strong>FromUri</strong></span></span></p></td>
<td><p><span data-ttu-id="eb400-125">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="eb400-125">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="eb400-126">URI пользователя, который поступил с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="eb400-126">URI of the user who originated the error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb400-127"><strong>FromUriType</strong></span><span class="sxs-lookup"><span data-stu-id="eb400-127"><strong>FromUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="eb400-128">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="eb400-128">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="eb400-129">Тип URI пользователя, который поступил на ошибку.</span><span class="sxs-lookup"><span data-stu-id="eb400-129">Type of URI of the user who originated the error.</span></span> <span data-ttu-id="eb400-130">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-uritypes-table.md">таблицей UriTypes в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="eb400-130">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb400-131"><strong>FromTenant</strong></span><span class="sxs-lookup"><span data-stu-id="eb400-131"><strong>FromTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="eb400-132">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="eb400-132">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="eb400-133">Клиент пользователя, который поступил с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="eb400-133">Tenant of the user who originated the error.</span></span> <span data-ttu-id="eb400-134">Дополнительные сведения приведены в <a href="lync-server-2013-tenants-table.md">таблице "клиенты" в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="eb400-134">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb400-135"><strong>ToUri</strong></span><span class="sxs-lookup"><span data-stu-id="eb400-135"><strong>ToUri</strong></span></span></p></td>
<td><p><span data-ttu-id="eb400-136">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="eb400-136">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="eb400-137">Универсальный код ресурса (URI) пользователя, который является целью отчета об ошибке.</span><span class="sxs-lookup"><span data-stu-id="eb400-137">URI of the user who was the target of the error report.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb400-138"><strong>ToUriType</strong></span><span class="sxs-lookup"><span data-stu-id="eb400-138"><strong>ToUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="eb400-139">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="eb400-139">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="eb400-140">Тип URI пользователя, который является конечным лицом отчета об ошибке.</span><span class="sxs-lookup"><span data-stu-id="eb400-140">Type of URI of the user who target of the error report.</span></span> <span data-ttu-id="eb400-141">Для получения дополнительных сведений ознакомьтесь с таблицей UriTypes.</span><span class="sxs-lookup"><span data-stu-id="eb400-141">See the UriTypes Table for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb400-142"><strong>ToTenant</strong></span><span class="sxs-lookup"><span data-stu-id="eb400-142"><strong>ToTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="eb400-143">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="eb400-143">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="eb400-144">Клиент пользователя, который является конечным лицом отчета об ошибке.</span><span class="sxs-lookup"><span data-stu-id="eb400-144">Tenant of the user who target of the error report.</span></span> <span data-ttu-id="eb400-145">Дополнительные сведения приведены в <a href="lync-server-2013-tenants-table.md">таблице "клиенты" в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="eb400-145">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb400-146"><strong>ConferenceUri</strong></span><span class="sxs-lookup"><span data-stu-id="eb400-146"><strong>ConferenceUri</strong></span></span></p></td>
<td><p><span data-ttu-id="eb400-147">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="eb400-147">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="eb400-148">Универсальный код ресурса (URI) Конференции, которая была целью отчета об ошибке.</span><span class="sxs-lookup"><span data-stu-id="eb400-148">URI of the conference that was the target of the error report.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb400-149"><strong>ConferenceUriType</strong></span><span class="sxs-lookup"><span data-stu-id="eb400-149"><strong>ConferenceUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="eb400-150">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="eb400-150">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="eb400-151">Тип URI конференции, которая была целью отчета об ошибке.</span><span class="sxs-lookup"><span data-stu-id="eb400-151">URI type of the conference that was the target of the error report.</span></span> <span data-ttu-id="eb400-152">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-uritypes-table.md">таблицей UriTypes в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="eb400-152">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb400-153"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="eb400-153"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="eb400-154">datetime</span><span class="sxs-lookup"><span data-stu-id="eb400-154">datetime</span></span></p></td>
<td><p><span data-ttu-id="eb400-155">Время запроса сеанса, в котором был создан отчет об ошибке.</span><span class="sxs-lookup"><span data-stu-id="eb400-155">Time of session request that originated the error report.</span></span> <span data-ttu-id="eb400-156">Используется в сочетании с SessionIdSeq для уникальной идентификации сеанса.</span><span class="sxs-lookup"><span data-stu-id="eb400-156">Used in conjunction with SessionIdSeq to uniquely identify a session.</span></span> <span data-ttu-id="eb400-157">Дополнительные сведения приведены <a href="lync-server-2013-dialogs-table.md">в таблице диалоговые окна Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="eb400-157">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb400-158"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="eb400-158"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="eb400-159">целое</span><span class="sxs-lookup"><span data-stu-id="eb400-159">int</span></span></p></td>
<td><p><span data-ttu-id="eb400-160">ИДЕНТИФИКАЦИОНный номер для идентификации запроса на сеанс, который является источником отчета об ошибке.</span><span class="sxs-lookup"><span data-stu-id="eb400-160">ID number to identify the session request that originated the error report.</span></span> <span data-ttu-id="eb400-161">Используется в сочетании с SessionIdTime для уникальной идентификации сеанса.</span><span class="sxs-lookup"><span data-stu-id="eb400-161">Used in conjunction with SessionIdTime to uniquely identify a session.</span></span> <span data-ttu-id="eb400-162">Дополнительные сведения приведены <a href="lync-server-2013-dialogs-table.md">в таблице диалоговые окна Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="eb400-162">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb400-163"><strong>DialogId</strong></span><span class="sxs-lookup"><span data-stu-id="eb400-163"><strong>DialogId</strong></span></span></p></td>
<td><p><span data-ttu-id="eb400-164">varstring (775)</span><span class="sxs-lookup"><span data-stu-id="eb400-164">varstring(775)</span></span></p></td>
<td><p><span data-ttu-id="eb400-165">ИДЕНТИФИКАТОР диалогового окна SIP сеанса, на который поступила ошибка.</span><span class="sxs-lookup"><span data-stu-id="eb400-165">SIP dialog ID of session that originated the error.</span></span> <span data-ttu-id="eb400-166">Формат:</span><span class="sxs-lookup"><span data-stu-id="eb400-166">The format is:</span></span></p>
<p><span data-ttu-id="eb400-167">диалоговое окно; тег "from-Tag"</span><span class="sxs-lookup"><span data-stu-id="eb400-167">dialog;from-tag;to-tag</span></span></p>
<p><span data-ttu-id="eb400-168">Эти данные можно преобразовать в текстовый формат, используя следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="eb400-168">This data can be converted to text format by using this syntax:</span></span></p>
<p><span data-ttu-id="eb400-169">Cast (CAST (ExternalId AS varbinary (max)) AS varchar (max))</span><span class="sxs-lookup"><span data-stu-id="eb400-169">cast(cast(ExternalId as varbinary(max)) as varchar(max))</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb400-170"><strong>ClientVersion</strong></span><span class="sxs-lookup"><span data-stu-id="eb400-170"><strong>ClientVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="eb400-171">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="eb400-171">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="eb400-172">Версия клиента, используемая пользователем, который поступил с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="eb400-172">Version of client used by the user who originated the error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb400-173"><strong>ClientType</strong></span><span class="sxs-lookup"><span data-stu-id="eb400-173"><strong>ClientType</strong></span></span></p></td>
<td><p><span data-ttu-id="eb400-174">целое</span><span class="sxs-lookup"><span data-stu-id="eb400-174">int</span></span></p></td>
<td><p><span data-ttu-id="eb400-175">Клиент, использованный пользователем, который поступил с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="eb400-175">Client used by the user who originated the error.</span></span> <span data-ttu-id="eb400-176">Дополнительные сведения вы увидите <a href="lync-server-2013-useragentdef-table.md">в таблице UserAgentDef в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="eb400-176">See the <a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a> for more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb400-177"><strong>ClientCategory</strong></span><span class="sxs-lookup"><span data-stu-id="eb400-177"><strong>ClientCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="eb400-178">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="eb400-178">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="eb400-179">Имя категории клиента, используемой пользователем, который поступил с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="eb400-179">Name of the category of the client used by the user who originated the error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb400-180"><strong>Источник</strong></span><span class="sxs-lookup"><span data-stu-id="eb400-180"><strong>Source</strong></span></span></p></td>
<td><p><span data-ttu-id="eb400-181">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="eb400-181">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="eb400-182">Имя сервера, отправившего ошибку (при отправке отчета из серверного компонента).</span><span class="sxs-lookup"><span data-stu-id="eb400-182">Name of server that originated the error (if report was sent from a server component).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb400-183"><strong>Приложение</strong></span><span class="sxs-lookup"><span data-stu-id="eb400-183"><strong>Application</strong></span></span></p></td>
<td><p><span data-ttu-id="eb400-184">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="eb400-184">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="eb400-185">Имя приложения, которое поступило об ошибке (при отправке отчета из серверного компонента).</span><span class="sxs-lookup"><span data-stu-id="eb400-185">Name of application that originated the error (if report was sent from a server component).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb400-186"><strong>ResponseCode</strong></span><span class="sxs-lookup"><span data-stu-id="eb400-186"><strong>ResponseCode</strong></span></span></p></td>
<td><p><span data-ttu-id="eb400-187">целое</span><span class="sxs-lookup"><span data-stu-id="eb400-187">int</span></span></p></td>
<td><p><span data-ttu-id="eb400-188">Код ответа SIP в сеанс сообщения SIP с отчетом об ошибке.</span><span class="sxs-lookup"><span data-stu-id="eb400-188">SIP response code to the session of the SIP message containing the error report.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb400-189"><strong>RequestType</strong></span><span class="sxs-lookup"><span data-stu-id="eb400-189"><strong>RequestType</strong></span></span></p></td>
<td><p><span data-ttu-id="eb400-190">varchar (max)</span><span class="sxs-lookup"><span data-stu-id="eb400-190">varchar(max)</span></span></p></td>
<td><p><span data-ttu-id="eb400-191">Тип запроса, который завершился сбоем.</span><span class="sxs-lookup"><span data-stu-id="eb400-191">Type of request that failed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb400-192"><strong>Контента</strong></span><span class="sxs-lookup"><span data-stu-id="eb400-192"><strong>ContentType</strong></span></span></p></td>
<td><p><span data-ttu-id="eb400-193">varchar (max)</span><span class="sxs-lookup"><span data-stu-id="eb400-193">varchar(max)</span></span></p></td>
<td><p><span data-ttu-id="eb400-194">Тип контента запроса, который завершился сбоем.</span><span class="sxs-lookup"><span data-stu-id="eb400-194">Content type of the request that failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb400-195"><strong>CallType</strong></span><span class="sxs-lookup"><span data-stu-id="eb400-195"><strong>CallType</strong></span></span></p></td>
<td><p><span data-ttu-id="eb400-196">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="eb400-196">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="eb400-197">Тип сеанса.</span><span class="sxs-lookup"><span data-stu-id="eb400-197">Type of session.</span></span> <span data-ttu-id="eb400-198">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-calltype-table.md">таблицей CallType в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="eb400-198">See the <a href="lync-server-2013-calltype-table.md">CallType table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb400-199"><strong>TelemetryId</strong></span><span class="sxs-lookup"><span data-stu-id="eb400-199"><strong>TelemetryId</strong></span></span></p></td>
<td><p><span data-ttu-id="eb400-200">идентификатора</span><span class="sxs-lookup"><span data-stu-id="eb400-200">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="eb400-201">Уникальный идентификатор, соответствующий сведениям о времени соединения для различных компонентов, участвующих в Конференции.</span><span class="sxs-lookup"><span data-stu-id="eb400-201">Unique identifier correlating join time information for the different components involved in a conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb400-202"><strong>SetupTime</strong></span><span class="sxs-lookup"><span data-stu-id="eb400-202"><strong>SetupTime</strong></span></span></p></td>
<td><p><span data-ttu-id="eb400-203">целое</span><span class="sxs-lookup"><span data-stu-id="eb400-203">int</span></span></p></td>
<td><p><span data-ttu-id="eb400-204">Время (в миллисекундах), требуемое конкретным компонентом для присоединения к Конференции.</span><span class="sxs-lookup"><span data-stu-id="eb400-204">Time (in milliseconds) required for a specific component to join a conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb400-205"><strong>IsCapturedByServer</strong></span><span class="sxs-lookup"><span data-stu-id="eb400-205"><strong>IsCapturedByServer</strong></span></span></p></td>
<td><p><span data-ttu-id="eb400-206">бит</span><span class="sxs-lookup"><span data-stu-id="eb400-206">bit</span></span></p></td>
<td><p><span data-ttu-id="eb400-207">Указывает, был ли отчет об ошибке записан агентом CDR, запущенным на сервере переднего плана или отправлен клиентом.</span><span class="sxs-lookup"><span data-stu-id="eb400-207">Indicates whether the error report was captured by the CDR agent running on the Front End server, or sent by the client.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb400-208"><strong>Пометка</strong></span><span class="sxs-lookup"><span data-stu-id="eb400-208"><strong>Flag</strong></span></span></p></td>
<td><p><span data-ttu-id="eb400-209">smallint</span><span class="sxs-lookup"><span data-stu-id="eb400-209">smallint</span></span></p></td>
<td><p><span data-ttu-id="eb400-210">Зарезервировано для будущего использования.</span><span class="sxs-lookup"><span data-stu-id="eb400-210">Reserved for future use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb400-211"><strong>MsDiagHeader</strong></span><span class="sxs-lookup"><span data-stu-id="eb400-211"><strong>MsDiagHeader</strong></span></span></p></td>
<td><p><span data-ttu-id="eb400-212">varchar (max)</span><span class="sxs-lookup"><span data-stu-id="eb400-212">varchar(max)</span></span></p></td>
<td><p><span data-ttu-id="eb400-213">Дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="eb400-213">Additional information about the error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb400-214"><strong>FrontEnd</strong></span><span class="sxs-lookup"><span data-stu-id="eb400-214"><strong>FrontEnd</strong></span></span></p></td>
<td><p><span data-ttu-id="eb400-215">nvarchar</span><span class="sxs-lookup"><span data-stu-id="eb400-215">nvarchar</span></span></p></td>
<td><p><span data-ttu-id="eb400-216">Полное доменное имя сервера переднего плана, отправившего отчет.</span><span class="sxs-lookup"><span data-stu-id="eb400-216">Fully qualified domain name of the Front End server that submitted the report.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb400-217"><strong>Pool</strong></span><span class="sxs-lookup"><span data-stu-id="eb400-217"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="eb400-218">nvarchar</span><span class="sxs-lookup"><span data-stu-id="eb400-218">nvarchar</span></span></p></td>
<td><p><span data-ttu-id="eb400-219">Полное доменное имя пула, содержащего сервер переднего плана, отправивший отчет.</span><span class="sxs-lookup"><span data-stu-id="eb400-219">Fully qualified domain name of the pool containing the Front End server that submitted the report.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="eb400-220">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="eb400-220">


</div>

<span> </span>

</div>

</div>

</span></span></div>

