---
title: 'Lync Server 2013: таблица ProgressReport'
description: 'Таблица Lync Server 2013: ProgressReport.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ProgressReport table
ms:assetid: 38e5f060-5e9b-4185-87b2-7ef61c4bb75f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425864(v=OCS.15)
ms:contentKeyID: 48183847
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d36ee2ab75410ea2462da4b647ef5b45afefb1bb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436869"
---
# <a name="progressreport-table-in-lync-server-2013"></a><span data-ttu-id="41a38-103">Таблица ProgressReport в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="41a38-103">ProgressReport table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="41a38-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="41a38-104">

<span> </span></span></span>

<span data-ttu-id="41a38-105">_**Тема последнего изменения:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="41a38-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="41a38-106">Отчеты о состоянии основываются на данных, отправленных клиентом в базу данных после завершения вызова или сеанса.</span><span class="sxs-lookup"><span data-stu-id="41a38-106">Progress reports are based on data uploaded by the client to the database after a call or session is completed.</span></span> <span data-ttu-id="41a38-107">Отчеты о ходе выполнения будут записываться только для звонков и сеансов, которые определяет Lync Server 2013, может быть полезен в целях диагностики.</span><span class="sxs-lookup"><span data-stu-id="41a38-107">Progress reports will be written only for calls and sessions that Lync Server 2013 determines might be useful for diagnostic purposes.</span></span>

<span data-ttu-id="41a38-108">Поля ErrorTime, ErrorReportSeq и ProgressReportSeq не обязательно ссылаются на ошибки, а также на сообщения, указывающие на состояние вызовов или сообщений.</span><span class="sxs-lookup"><span data-stu-id="41a38-108">The ErrorTime, ErrorReportSeq and ProgressReportSeq fields don’t necessarily refer to errors but to messages that indicate the status of calls or messages.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="41a38-109">Столбец</span><span class="sxs-lookup"><span data-stu-id="41a38-109">Column</span></span></th>
<th><span data-ttu-id="41a38-110">Тип данных</span><span class="sxs-lookup"><span data-stu-id="41a38-110">Data Type</span></span></th>
<th><span data-ttu-id="41a38-111">Ключ/индекс</span><span class="sxs-lookup"><span data-stu-id="41a38-111">Key/Index</span></span></th>
<th><span data-ttu-id="41a38-112">Сведения</span><span class="sxs-lookup"><span data-stu-id="41a38-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="41a38-113"><strong>ErrorTime</strong></span><span class="sxs-lookup"><span data-stu-id="41a38-113"><strong>ErrorTime</strong></span></span></p></td>
<td><p><span data-ttu-id="41a38-114">datetime</span><span class="sxs-lookup"><span data-stu-id="41a38-114">datetime</span></span></p></td>
<td><p><span data-ttu-id="41a38-115">Основной, внешний</span><span class="sxs-lookup"><span data-stu-id="41a38-115">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="41a38-116">Дата и время отчета об ошибках хода выполнения, который включает этот отчет о ходе выполнения.</span><span class="sxs-lookup"><span data-stu-id="41a38-116">Date and time of the progress error report that contains this progress report.</span></span> <span data-ttu-id="41a38-117">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-errorreport-table.md">таблицей errorreport в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="41a38-117">See the <a href="lync-server-2013-errorreport-table.md">ErrorReport table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41a38-118"><strong>ErrorId</strong></span><span class="sxs-lookup"><span data-stu-id="41a38-118"><strong>ErrorId</strong></span></span></p></td>
<td><p><span data-ttu-id="41a38-119">целое</span><span class="sxs-lookup"><span data-stu-id="41a38-119">int</span></span></p></td>
<td><p><span data-ttu-id="41a38-120">Основной, внешний</span><span class="sxs-lookup"><span data-stu-id="41a38-120">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="41a38-121">ИДЕНТИФИКАЦИОНный номер, используемый в сочетании с ErrorTime, ProgressReportSeq для уникальной идентификации отчета о ходе выполнения.</span><span class="sxs-lookup"><span data-stu-id="41a38-121">ID number used in conjunction with ErrorTime, ProgressReportSeq to uniquely identify a progress report.</span></span> <span data-ttu-id="41a38-122">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-errorreport-table.md">таблицей errorreport в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="41a38-122">See the <a href="lync-server-2013-errorreport-table.md">ErrorReport table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="41a38-123"><strong>ErrorReportSeq</strong></span><span class="sxs-lookup"><span data-stu-id="41a38-123"><strong>ErrorReportSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="41a38-124">целое</span><span class="sxs-lookup"><span data-stu-id="41a38-124">int</span></span></p></td>
<td><p><span data-ttu-id="41a38-125">Основной, внешний</span><span class="sxs-lookup"><span data-stu-id="41a38-125">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="41a38-126">ИДЕНТИФИКАЦИОНный номер, идентифицирующий отчет об ошибке.</span><span class="sxs-lookup"><span data-stu-id="41a38-126">ID number that identifies the error report.</span></span> <span data-ttu-id="41a38-127">ErrorReporSeq используется в сочетании с ErrorTime для уникальной идентификации отчета об ошибке.</span><span class="sxs-lookup"><span data-stu-id="41a38-127">ErrorReporSeq is used in conjunction with ErrorTime to uniquely identify an error report.</span></span> <span data-ttu-id="41a38-128">Дополнительные сведения приведены <a href="lync-server-2013-errorreport-table.md">в таблице errorreport в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="41a38-128">See the <a href="lync-server-2013-errorreport-table.md">ErrorReport table in Lync Server 2013</a> for more information</span></span></p>
<p><span data-ttu-id="41a38-129">Это поле было введено в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="41a38-129">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41a38-130"><strong>ProgressReportSeq</strong></span><span class="sxs-lookup"><span data-stu-id="41a38-130"><strong>ProgressReportSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="41a38-131">целое</span><span class="sxs-lookup"><span data-stu-id="41a38-131">int</span></span></p></td>
<td><p><span data-ttu-id="41a38-132">Primary</span><span class="sxs-lookup"><span data-stu-id="41a38-132">Primary</span></span></p></td>
<td><p><span data-ttu-id="41a38-133">ИДЕНТИФИКАЦИОНный номер для идентификации отчета о ходе выполнения.</span><span class="sxs-lookup"><span data-stu-id="41a38-133">ID number to identify the progress report.</span></span> <span data-ttu-id="41a38-134">Используется совместно с ErrorTime и ErrorReportSeq для уникальной идентификации отчета о ходе выполнения.</span><span class="sxs-lookup"><span data-stu-id="41a38-134">Used in conjunction with ErrorTime and ErrorReportSeq to uniquely identify a progress report.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="41a38-135"><strong>MsDiagId</strong></span><span class="sxs-lookup"><span data-stu-id="41a38-135"><strong>MsDiagId</strong></span></span></p></td>
<td><p><span data-ttu-id="41a38-136">целое</span><span class="sxs-lookup"><span data-stu-id="41a38-136">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="41a38-137">Идентификатор диагностики отчета о ходе выполнения.</span><span class="sxs-lookup"><span data-stu-id="41a38-137">Diagnostic ID of the progress report.</span></span></p>
<p><span data-ttu-id="41a38-138">Это поле было введено в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="41a38-138">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41a38-139"><strong>Источника</strong></span><span class="sxs-lookup"><span data-stu-id="41a38-139"><strong>SourceId</strong></span></span></p></td>
<td><p><span data-ttu-id="41a38-140">целое</span><span class="sxs-lookup"><span data-stu-id="41a38-140">int</span></span></p></td>
<td><p><span data-ttu-id="41a38-141">Другом</span><span class="sxs-lookup"><span data-stu-id="41a38-141">Foreign</span></span></p></td>
<td><p><span data-ttu-id="41a38-142">Сервер, отправивший отчет об ошибке (при отправке отчета из серверного компонента).</span><span class="sxs-lookup"><span data-stu-id="41a38-142">Server that sent the error report (if the report was sent from a server component).</span></span> <span data-ttu-id="41a38-143">Более подробную информацию вы видите <a href="lync-server-2013-servers-table.md">в таблице Servers (серверы) в Lync Server 2013</a> . Это поле было введено в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="41a38-143">See the <a href="lync-server-2013-servers-table.md">Servers table in Lync Server 2013</a> for more information.This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="41a38-144"><strong>ApplicationId</strong></span><span class="sxs-lookup"><span data-stu-id="41a38-144"><strong>ApplicationId</strong></span></span></p></td>
<td><p><span data-ttu-id="41a38-145">целое</span><span class="sxs-lookup"><span data-stu-id="41a38-145">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="41a38-146">Процесс Lync Server, к которому относится отчет.</span><span class="sxs-lookup"><span data-stu-id="41a38-146">The Lync Server process that the report is about.</span></span> <span data-ttu-id="41a38-147">Для получения дополнительных сведений ознакомьтесь с таблицей Application.</span><span class="sxs-lookup"><span data-stu-id="41a38-147">See the Application Table for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41a38-148"><strong>Подробности</strong></span><span class="sxs-lookup"><span data-stu-id="41a38-148"><strong>Detail</strong></span></span></p></td>
<td><p><span data-ttu-id="41a38-149">изображение</span><span class="sxs-lookup"><span data-stu-id="41a38-149">image</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="41a38-150">Сведения о отчете о состоянии, сохраняемые в двоичном формате для экономии места. Эти данные можно преобразовать в текстовый формат, используя следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="41a38-150">Progress report details, stored in binary format to save space.This data can be converted to text format using this syntax:</span></span></p>
<p><span data-ttu-id="41a38-151">Cast (CAST (данные в формате varbinary (max)) AS varchar (max))</span><span class="sxs-lookup"><span data-stu-id="41a38-151">cast(cast(Detail as varbinary(max)) as varchar(max))</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="41a38-152"><strong>TelemetryId</strong></span><span class="sxs-lookup"><span data-stu-id="41a38-152"><strong>TelemetryId</strong></span></span></p></td>
<td><p><span data-ttu-id="41a38-153">Идентификатора</span><span class="sxs-lookup"><span data-stu-id="41a38-153">uniqueIdentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="41a38-154">Уникальный идентификатор, который соответствует сведениям о времени соединения для различных компонентов, участвующих в Конференции.</span><span class="sxs-lookup"><span data-stu-id="41a38-154">Unique identifier that correlates join time information for the different components involved in a conference.</span></span></p>
<p><span data-ttu-id="41a38-155">Это поле было введено в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="41a38-155">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41a38-156"><strong>SessionSetupTime</strong></span><span class="sxs-lookup"><span data-stu-id="41a38-156"><strong>SessionSetupTime</strong></span></span></p></td>
<td><p><span data-ttu-id="41a38-157">целое</span><span class="sxs-lookup"><span data-stu-id="41a38-157">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="41a38-158">Время (в миллисекундах), в течение которого конкретный компонент присоединяется к Конференции.</span><span class="sxs-lookup"><span data-stu-id="41a38-158">Time (in milliseconds) for a specific component to join a conference.</span></span></p>
<p><span data-ttu-id="41a38-159">Это поле было введено в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="41a38-159">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="41a38-160">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="41a38-160">


</div>

<span> </span>

</div>

</div>

</span></span></div>

