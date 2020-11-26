---
title: 'Lync Server 2013: таблица ErrorReport'
description: 'Таблица Lync Server 2013: ErrorReport.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ErrorReport table
ms:assetid: ae0287b4-e8ca-4f8c-84ef-502897dcaa2a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412826(v=OCS.15)
ms:contentKeyID: 48185129
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9c1cc65c396c16dc137255438f7ef7c32b2d0b78
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428519"
---
# <a name="errorreport-table-in-lync-server-2013"></a><span data-ttu-id="0ea7a-103">Таблица ErrorReport в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0ea7a-103">ErrorReport table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0ea7a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0ea7a-104">

<span> </span></span></span>

<span data-ttu-id="0ea7a-105">_**Тема последнего изменения:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="0ea7a-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="0ea7a-106">В таблице ErrorReport хранятся сведения о возникших ошибках.</span><span class="sxs-lookup"><span data-stu-id="0ea7a-106">The ErrorReport table stores information about errors that have occurred.</span></span> <span data-ttu-id="0ea7a-107">Каждая запись содержит один экземпляр ошибки.</span><span class="sxs-lookup"><span data-stu-id="0ea7a-107">Each record is one error occurrence.</span></span> <span data-ttu-id="0ea7a-108">Эти ошибки регистрируются агентом CDR, который запущен на сервере переднего плана или отправлен клиентом.</span><span class="sxs-lookup"><span data-stu-id="0ea7a-108">The errors are captured either by the CDR agent running on the front-end server or sent from the client.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0ea7a-109">Столбец</span><span class="sxs-lookup"><span data-stu-id="0ea7a-109">Column</span></span></th>
<th><span data-ttu-id="0ea7a-110">Тип данных</span><span class="sxs-lookup"><span data-stu-id="0ea7a-110">Data Type</span></span></th>
<th><span data-ttu-id="0ea7a-111">Ключ/индекс</span><span class="sxs-lookup"><span data-stu-id="0ea7a-111">Key/Index</span></span></th>
<th><span data-ttu-id="0ea7a-112">Сведения</span><span class="sxs-lookup"><span data-stu-id="0ea7a-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0ea7a-113"><strong>ErrorTime</strong></span><span class="sxs-lookup"><span data-stu-id="0ea7a-113"><strong>ErrorTime</strong></span></span></p></td>
<td><p><span data-ttu-id="0ea7a-114">datetime</span><span class="sxs-lookup"><span data-stu-id="0ea7a-114">datetime</span></span></p></td>
<td><p><span data-ttu-id="0ea7a-115">Primary</span><span class="sxs-lookup"><span data-stu-id="0ea7a-115">Primary</span></span></p></td>
<td><p><span data-ttu-id="0ea7a-116">Дата и время, когда возникла ошибка.</span><span class="sxs-lookup"><span data-stu-id="0ea7a-116">Date and time the error occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ea7a-117"><strong>ErrorReportSeq</strong></span><span class="sxs-lookup"><span data-stu-id="0ea7a-117"><strong>ErrorReportSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="0ea7a-118">целое</span><span class="sxs-lookup"><span data-stu-id="0ea7a-118">int</span></span></p></td>
<td><p><span data-ttu-id="0ea7a-119">Primary</span><span class="sxs-lookup"><span data-stu-id="0ea7a-119">Primary</span></span></p></td>
<td><p><span data-ttu-id="0ea7a-120">ИДЕНТИФИКАЦИОНный номер для идентификации отчета об ошибке.</span><span class="sxs-lookup"><span data-stu-id="0ea7a-120">ID number to identify the error report.</span></span> <span data-ttu-id="0ea7a-121">Используется в сочетании с <strong>ErrorTime</strong> для уникальной идентификации отчета об ошибке.</span><span class="sxs-lookup"><span data-stu-id="0ea7a-121">Used in conjunction with <strong>ErrorTime</strong> to uniquely identify an error report.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ea7a-122"><strong>ErrorId</strong></span><span class="sxs-lookup"><span data-stu-id="0ea7a-122"><strong>ErrorId</strong></span></span></p></td>
<td><p><span data-ttu-id="0ea7a-123">целое</span><span class="sxs-lookup"><span data-stu-id="0ea7a-123">int</span></span></p></td>
<td><p><span data-ttu-id="0ea7a-124">Другом</span><span class="sxs-lookup"><span data-stu-id="0ea7a-124">Foreign</span></span></p></td>
<td><p><span data-ttu-id="0ea7a-125">Уникальный идентификатор типа ошибки.</span><span class="sxs-lookup"><span data-stu-id="0ea7a-125">Unique ID of the error type.</span></span> <span data-ttu-id="0ea7a-126">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-errordef-table.md">таблицей ErrorDef в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="0ea7a-126">See the <a href="lync-server-2013-errordef-table.md">ErrorDef table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ea7a-127"><strong>FromUserId</strong></span><span class="sxs-lookup"><span data-stu-id="0ea7a-127"><strong>FromUserId</strong></span></span></p></td>
<td><p><span data-ttu-id="0ea7a-128">целое</span><span class="sxs-lookup"><span data-stu-id="0ea7a-128">int</span></span></p></td>
<td><p><span data-ttu-id="0ea7a-129">Другом</span><span class="sxs-lookup"><span data-stu-id="0ea7a-129">Foreign</span></span></p></td>
<td><p><span data-ttu-id="0ea7a-130">Пользователь, который поступил на этот запрос, вызвавший ошибку.</span><span class="sxs-lookup"><span data-stu-id="0ea7a-130">User who originated the request that caused the error.</span></span> <span data-ttu-id="0ea7a-131">Дополнительные сведения <a href="lync-server-2013-users-table.md">можно найти в таблице Users (пользователи) в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="0ea7a-131">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ea7a-132"><strong>ToUserId</strong></span><span class="sxs-lookup"><span data-stu-id="0ea7a-132"><strong>ToUserId</strong></span></span></p></td>
<td><p><span data-ttu-id="0ea7a-133">целое</span><span class="sxs-lookup"><span data-stu-id="0ea7a-133">int</span></span></p></td>
<td><p><span data-ttu-id="0ea7a-134">Другом</span><span class="sxs-lookup"><span data-stu-id="0ea7a-134">Foreign</span></span></p></td>
<td><p><span data-ttu-id="0ea7a-135">Конечный пользователь для запроса, вызвавшего ошибку.</span><span class="sxs-lookup"><span data-stu-id="0ea7a-135">Destination user for the request that caused the error.</span></span> <span data-ttu-id="0ea7a-136">Дополнительные сведения <a href="lync-server-2013-users-table.md">можно найти в таблице Users (пользователи) в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="0ea7a-136">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ea7a-137"><strong>ConferenceUriId</strong></span><span class="sxs-lookup"><span data-stu-id="0ea7a-137"><strong>ConferenceUriId</strong></span></span></p></td>
<td><p><span data-ttu-id="0ea7a-138">целое</span><span class="sxs-lookup"><span data-stu-id="0ea7a-138">int</span></span></p></td>
<td><p><span data-ttu-id="0ea7a-139">Другом</span><span class="sxs-lookup"><span data-stu-id="0ea7a-139">Foreign</span></span></p></td>
<td><p><span data-ttu-id="0ea7a-140">Универсальный код ресурса (URI) для Конференции, связанный с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="0ea7a-140">Conference URI related to the error.</span></span> <span data-ttu-id="0ea7a-141">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-conferenceuris-table.md">таблицей ConferenceUris в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="0ea7a-141">See the <a href="lync-server-2013-conferenceuris-table.md">ConferenceUris table in Lync Server 2013</a> for more information.</span></span> <span data-ttu-id="0ea7a-142">Как правило, если ConferenceUriId не имеет значение null, то либо FromUserId, либо ToUserId будет NULL.</span><span class="sxs-lookup"><span data-stu-id="0ea7a-142">Typically, if ConferenceUriId is not null, then either FromUserId or ToUserId will be null.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ea7a-143"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="0ea7a-143"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="0ea7a-144">datetime</span><span class="sxs-lookup"><span data-stu-id="0ea7a-144">datetime</span></span></p></td>
<td><p><span data-ttu-id="0ea7a-145">Другом</span><span class="sxs-lookup"><span data-stu-id="0ea7a-145">Foreign</span></span></p></td>
<td><p><span data-ttu-id="0ea7a-146">Используется в сочетании с <strong>SessionIdSeq</strong> для уникальной идентификации сеанса.</span><span class="sxs-lookup"><span data-stu-id="0ea7a-146">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="0ea7a-147">Дополнительные сведения приведены <a href="lync-server-2013-dialogs-table.md">в таблице диалоговые окна Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="0ea7a-147">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ea7a-148"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="0ea7a-148"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="0ea7a-149">целое</span><span class="sxs-lookup"><span data-stu-id="0ea7a-149">int</span></span></p></td>
<td><p><span data-ttu-id="0ea7a-150">Другом</span><span class="sxs-lookup"><span data-stu-id="0ea7a-150">Foreign</span></span></p></td>
<td><p><span data-ttu-id="0ea7a-151">ИДЕНТИФИКАЦИОНный номер для идентификации сеанса.</span><span class="sxs-lookup"><span data-stu-id="0ea7a-151">ID number to identify the session.</span></span> <span data-ttu-id="0ea7a-152">Используется в сочетании с <strong>SessionIdTime</strong> для уникальной идентификации сеанса.</span><span class="sxs-lookup"><span data-stu-id="0ea7a-152">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.</span></span> <span data-ttu-id="0ea7a-153">Дополнительные сведения приведены <a href="lync-server-2013-dialogs-table.md">в таблице диалоговые окна Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="0ea7a-153">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ea7a-154"><strong>Источника</strong></span><span class="sxs-lookup"><span data-stu-id="0ea7a-154"><strong>SourceId</strong></span></span></p></td>
<td><p><span data-ttu-id="0ea7a-155">целое</span><span class="sxs-lookup"><span data-stu-id="0ea7a-155">int</span></span></p></td>
<td><p><span data-ttu-id="0ea7a-156">Другом</span><span class="sxs-lookup"><span data-stu-id="0ea7a-156">Foreign</span></span></p></td>
<td><p><span data-ttu-id="0ea7a-157">Сервер, отправивший отчет об ошибке (при отправке отчета из серверного компонента).</span><span class="sxs-lookup"><span data-stu-id="0ea7a-157">Server that sent the error report (if the report is being sent from a server component).</span></span> <span data-ttu-id="0ea7a-158">Более подробную информацию вы видите <a href="lync-server-2013-servers-table.md">в таблице Servers (серверы) в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="0ea7a-158">See the <a href="lync-server-2013-servers-table.md">Servers table in Lync Server 2013</a> for more information.</span></span></p>
<p><span data-ttu-id="0ea7a-159">Это поле было введено в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0ea7a-159">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ea7a-160"><strong>ApplicationId</strong></span><span class="sxs-lookup"><span data-stu-id="0ea7a-160"><strong>ApplicationId</strong></span></span></p></td>
<td><p><span data-ttu-id="0ea7a-161">целое</span><span class="sxs-lookup"><span data-stu-id="0ea7a-161">int</span></span></p></td>
<td><p><span data-ttu-id="0ea7a-162">Другом</span><span class="sxs-lookup"><span data-stu-id="0ea7a-162">Foreign</span></span></p></td>
<td><p><span data-ttu-id="0ea7a-163">Сервер, отправивший отчет об ошибке (при отправке отчета из серверного компонента).</span><span class="sxs-lookup"><span data-stu-id="0ea7a-163">Server that sent the error report (if the report is being sent from a server component).</span></span> <span data-ttu-id="0ea7a-164">Дополнительные сведения приведены <a href="lync-server-2013-application-table.md">в таблице приложение Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="0ea7a-164">See the <a href="lync-server-2013-application-table.md">Application table in Lync Server 2013</a> for more information.</span></span></p>
<p><span data-ttu-id="0ea7a-165">Это поле было введено в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0ea7a-165">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ea7a-166"><strong>MsDiagHeader</strong></span><span class="sxs-lookup"><span data-stu-id="0ea7a-166"><strong>MsDiagHeader</strong></span></span></p></td>
<td><p><span data-ttu-id="0ea7a-167">изображение</span><span class="sxs-lookup"><span data-stu-id="0ea7a-167">image</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="0ea7a-168">Дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="0ea7a-168">More information about the error.</span></span></p>
<p><span data-ttu-id="0ea7a-169">Эти данные можно преобразовать в текстовый формат, используя следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="0ea7a-169">This data can be converted to text format by using this syntax:</span></span></p>
<p><code>cast(cast(Detail as varbinary(max)) as varchar(max)) </code></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ea7a-170"><strong>ClientVersionId</strong></span><span class="sxs-lookup"><span data-stu-id="0ea7a-170"><strong>ClientVersionId</strong></span></span></p></td>
<td><p><span data-ttu-id="0ea7a-171">целое</span><span class="sxs-lookup"><span data-stu-id="0ea7a-171">int</span></span></p></td>
<td><p><span data-ttu-id="0ea7a-172">Другом</span><span class="sxs-lookup"><span data-stu-id="0ea7a-172">Foreign</span></span></p></td>
<td><p><span data-ttu-id="0ea7a-173">Клиентская версия конечной точки, отправляющей отчет об ошибке.</span><span class="sxs-lookup"><span data-stu-id="0ea7a-173">The client version of endpoint that sends the error report.</span></span> <span data-ttu-id="0ea7a-174">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-clientversions-table.md">таблицей ClientVersions в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="0ea7a-174">See the <a href="lync-server-2013-clientversions-table.md">ClientVersions table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ea7a-175"><strong>IsCapturedByServer</strong></span><span class="sxs-lookup"><span data-stu-id="0ea7a-175"><strong>IsCapturedByServer</strong></span></span></p></td>
<td><p><span data-ttu-id="0ea7a-176">бит</span><span class="sxs-lookup"><span data-stu-id="0ea7a-176">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0ea7a-177">Отчет об ошибке, записанный агентом CDR, который запущен на сервере переднего плана или отправляется клиентом.</span><span class="sxs-lookup"><span data-stu-id="0ea7a-177">Is the error report captured by the CDR agent running on the front-end server, or sent by the client.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ea7a-178"><strong>Пометка</strong></span><span class="sxs-lookup"><span data-stu-id="0ea7a-178"><strong>Flag</strong></span></span></p></td>
<td><p><span data-ttu-id="0ea7a-179">smallint</span><span class="sxs-lookup"><span data-stu-id="0ea7a-179">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0ea7a-180">Зарезервировано для будущего использования.</span><span class="sxs-lookup"><span data-stu-id="0ea7a-180">Reserved for future use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ea7a-181"><strong>TelemetryId</strong></span><span class="sxs-lookup"><span data-stu-id="0ea7a-181"><strong>TelemetryId</strong></span></span></p></td>
<td><p><span data-ttu-id="0ea7a-182">Идентификатора</span><span class="sxs-lookup"><span data-stu-id="0ea7a-182">uniqueIdentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0ea7a-183">Уникальный идентификатор, соответствующий сведениям о времени соединения для различных компонентов, участвующих в Конференции.</span><span class="sxs-lookup"><span data-stu-id="0ea7a-183">Unique identifier correlating join time information for the different components involved in a conference.</span></span></p>
<p><span data-ttu-id="0ea7a-184">Это поле было введено в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0ea7a-184">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ea7a-185"><strong>SessionSetupTime</strong></span><span class="sxs-lookup"><span data-stu-id="0ea7a-185"><strong>SessionSetupTime</strong></span></span></p></td>
<td><p><span data-ttu-id="0ea7a-186">целое</span><span class="sxs-lookup"><span data-stu-id="0ea7a-186">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0ea7a-187">Время (в миллисекундах), требуемое конкретным компонентом для присоединения к Конференции.</span><span class="sxs-lookup"><span data-stu-id="0ea7a-187">Time (in milliseconds) required for a specific component to join a conference.</span></span></p>
<p><span data-ttu-id="0ea7a-188">Это поле было введено в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0ea7a-188">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ea7a-189"><strong>ServerId</strong></span><span class="sxs-lookup"><span data-stu-id="0ea7a-189"><strong>ServerId</strong></span></span></p></td>
<td><p><span data-ttu-id="0ea7a-190">целое</span><span class="sxs-lookup"><span data-stu-id="0ea7a-190">int</span></span></p></td>
<td><p><span data-ttu-id="0ea7a-191">Другом</span><span class="sxs-lookup"><span data-stu-id="0ea7a-191">Foreign</span></span></p></td>
<td><p><span data-ttu-id="0ea7a-192">Представляет полное доменное имя сервера, который сгенерировал отчет об ошибке.</span><span class="sxs-lookup"><span data-stu-id="0ea7a-192">Represents the fully qualified domain name of the server that generated the error report.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ea7a-193"><strong>PoolId</strong></span><span class="sxs-lookup"><span data-stu-id="0ea7a-193"><strong>PoolId</strong></span></span></p></td>
<td><p><span data-ttu-id="0ea7a-194">целое</span><span class="sxs-lookup"><span data-stu-id="0ea7a-194">int</span></span></p></td>
<td><p><span data-ttu-id="0ea7a-195">Другом</span><span class="sxs-lookup"><span data-stu-id="0ea7a-195">Foreign</span></span></p></td>
<td><p><span data-ttu-id="0ea7a-196">Представляет полное доменное имя пула, в котором был создан отчет об ошибке.</span><span class="sxs-lookup"><span data-stu-id="0ea7a-196">Represents the fully qualified domain name of the pool where the error report was generated.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="0ea7a-197">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0ea7a-197">


</div>

<span> </span>

</div>

</div>

</span></span></div>

