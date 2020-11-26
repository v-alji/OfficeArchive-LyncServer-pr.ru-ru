---
title: 'Lync Server 2013: представление ProgressReport'
description: 'Lync Server 2013: ProgressReport View.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ProgressReport view
ms:assetid: b49f3fc7-0e2f-498f-8505-aaaf54e435f9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721857(v=OCS.15)
ms:contentKeyID: 49733790
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b95086012f254499644e778e43cafdf70ffc8f9c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436855"
---
# <a name="progressreport-view-in-lync-server-2013"></a><span data-ttu-id="88e9a-103">ProgressReport представления в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="88e9a-103">ProgressReport view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="88e9a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="88e9a-104">

<span> </span></span></span>

<span data-ttu-id="88e9a-105">_**Тема последнего изменения:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="88e9a-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="88e9a-106">В представлении ProgressReport хранятся сведения о завершенных сеансах.</span><span class="sxs-lookup"><span data-stu-id="88e9a-106">The ProgressReport view stores information about completed sessions.</span></span> <span data-ttu-id="88e9a-107">Отчеты о ходе выполнения будут записываться только для звонков и сеансов, которые определяет Lync Server 2013, может быть полезен в целях диагностики.</span><span class="sxs-lookup"><span data-stu-id="88e9a-107">Progress reports will be written only for calls and sessions that Lync Server 2013 determines might be useful for diagnostic purposes.</span></span> <span data-ttu-id="88e9a-108">Это представление было представлено в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="88e9a-108">This view was introduced in Microsoft Lync Server 2013.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="88e9a-109">Поля ErrorTime, ErrorReportSeq и ProgressReportSeq не обязательно ссылаются на ошибки, а также на сообщения, указывающие на состояние вызовов или сообщений.</span><span class="sxs-lookup"><span data-stu-id="88e9a-109">The ErrorTime, ErrorReportSeq and ProgressReportSeq fields don’t necessarily refer to errors but to messages that indicate the status of calls or messages.</span></span>



</div>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="88e9a-110">Столбец</span><span class="sxs-lookup"><span data-stu-id="88e9a-110">Column</span></span></th>
<th><span data-ttu-id="88e9a-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="88e9a-111">Data Type</span></span></th>
<th><span data-ttu-id="88e9a-112">Подробности</span><span class="sxs-lookup"><span data-stu-id="88e9a-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="88e9a-113"><strong>ErrorTime</strong></span><span class="sxs-lookup"><span data-stu-id="88e9a-113"><strong>ErrorTime</strong></span></span></p></td>
<td><p><span data-ttu-id="88e9a-114">datetime</span><span class="sxs-lookup"><span data-stu-id="88e9a-114">datetime</span></span></p></td>
<td><p><span data-ttu-id="88e9a-115">Время возникновения ошибки.</span><span class="sxs-lookup"><span data-stu-id="88e9a-115">Time of error occurred.</span></span> <span data-ttu-id="88e9a-116">Используется в сочетании с ErrorReportSeq для уникальной идентификации ошибки.</span><span class="sxs-lookup"><span data-stu-id="88e9a-116">Used in conjunction with ErrorReportSeq to uniquely identify an error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88e9a-117"><strong>ErrorReportSeq</strong></span><span class="sxs-lookup"><span data-stu-id="88e9a-117"><strong>ErrorReportSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="88e9a-118">целое</span><span class="sxs-lookup"><span data-stu-id="88e9a-118">int</span></span></p></td>
<td><p><span data-ttu-id="88e9a-119">ИДЕНТИФИКАЦИОНный номер для идентификации ошибки.</span><span class="sxs-lookup"><span data-stu-id="88e9a-119">ID number to identify the error.</span></span> <span data-ttu-id="88e9a-120">Используется в сочетании с ErrorTime для уникальной идентификации ошибки.</span><span class="sxs-lookup"><span data-stu-id="88e9a-120">Used in conjunction with ErrorTime to uniquely identify an error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88e9a-121"><strong>ProgressReportSeq</strong></span><span class="sxs-lookup"><span data-stu-id="88e9a-121"><strong>ProgressReportSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="88e9a-122">целое</span><span class="sxs-lookup"><span data-stu-id="88e9a-122">int</span></span></p></td>
<td><p><span data-ttu-id="88e9a-123">Идентификатор для идентификации отчета о ходе выполнения.</span><span class="sxs-lookup"><span data-stu-id="88e9a-123">ID to identify the progress report.</span></span> <span data-ttu-id="88e9a-124">Используется, чтобы отличать отчеты о ходе выполнения одного отчета об ошибках.</span><span class="sxs-lookup"><span data-stu-id="88e9a-124">Used to distinguish progress reports of the same error report.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88e9a-125"><strong>MsDiagId</strong></span><span class="sxs-lookup"><span data-stu-id="88e9a-125"><strong>MsDiagId</strong></span></span></p></td>
<td><p><span data-ttu-id="88e9a-126">целое</span><span class="sxs-lookup"><span data-stu-id="88e9a-126">int</span></span></p></td>
<td><p><span data-ttu-id="88e9a-127">Идентификатор диагностики для отчета об ошибке.</span><span class="sxs-lookup"><span data-stu-id="88e9a-127">Diagnostic ID for the error report.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88e9a-128"><strong>Источник</strong></span><span class="sxs-lookup"><span data-stu-id="88e9a-128"><strong>Source</strong></span></span></p></td>
<td><p><span data-ttu-id="88e9a-129">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="88e9a-129">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="88e9a-130">Имя сервера, отправившего ошибку (при отправке отчета из серверного компонента).</span><span class="sxs-lookup"><span data-stu-id="88e9a-130">Name of server that originated the error (if report was sent from a server component).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88e9a-131"><strong>Приложение</strong></span><span class="sxs-lookup"><span data-stu-id="88e9a-131"><strong>Application</strong></span></span></p></td>
<td><p><span data-ttu-id="88e9a-132">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="88e9a-132">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="88e9a-133">Имя приложения, которое поступило об ошибке (при отправке отчета из серверного компонента).</span><span class="sxs-lookup"><span data-stu-id="88e9a-133">Name of application that originated the error (if report was sent from a server component).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88e9a-134"><strong>TelemetryId</strong></span><span class="sxs-lookup"><span data-stu-id="88e9a-134"><strong>TelemetryId</strong></span></span></p></td>
<td><p><span data-ttu-id="88e9a-135">идентификатора</span><span class="sxs-lookup"><span data-stu-id="88e9a-135">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="88e9a-136">Уникальный идентификатор, соответствующий сведениям о времени соединения для различных компонентов, участвующих в Конференции.</span><span class="sxs-lookup"><span data-stu-id="88e9a-136">Unique identifier correlating join time information for the different components involved in a conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88e9a-137"><strong>SessionSetupTime</strong></span><span class="sxs-lookup"><span data-stu-id="88e9a-137"><strong>SessionSetupTime</strong></span></span></p></td>
<td><p><span data-ttu-id="88e9a-138">целое</span><span class="sxs-lookup"><span data-stu-id="88e9a-138">int</span></span></p></td>
<td><p><span data-ttu-id="88e9a-139">Время (в миллисекундах), требуемое конкретным компонентом для присоединения к Конференции.</span><span class="sxs-lookup"><span data-stu-id="88e9a-139">Time (in milliseconds) required for a specific component to join a conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88e9a-140"><strong>MsDiagHeader</strong></span><span class="sxs-lookup"><span data-stu-id="88e9a-140"><strong>MsDiagHeader</strong></span></span></p></td>
<td><p><span data-ttu-id="88e9a-141">varchar (max)</span><span class="sxs-lookup"><span data-stu-id="88e9a-141">varchar(max)</span></span></p></td>
<td><p><span data-ttu-id="88e9a-142">Дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="88e9a-142">Additional error information.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="88e9a-143">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="88e9a-143">


</div>

<span> </span>

</div>

</div>

</span></span></div>

