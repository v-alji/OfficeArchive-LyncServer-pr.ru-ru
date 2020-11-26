---
title: 'Lync Server 2013: таблица FileTransfers'
description: 'Таблица Lync Server 2013: FileTransfers.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: FileTransfers table
ms:assetid: 5368e67c-d8a9-43a1-9472-a839950dedb3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398353(v=OCS.15)
ms:contentKeyID: 48184118
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ccde45fa3743a809499273676d567846ef292ecc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428169"
---
# <a name="filetransfers-table-in-lync-server-2013"></a><span data-ttu-id="84244-103">Таблица FileTransfers в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="84244-103">FileTransfers table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="84244-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="84244-104">

<span> </span></span></span>

<span data-ttu-id="84244-105">_**Тема последнего изменения:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="84244-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="84244-106">Каждая запись представляет собой один сеанс передачи файлов.</span><span class="sxs-lookup"><span data-stu-id="84244-106">Each record represents one file transfer session.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="84244-107">Столбец</span><span class="sxs-lookup"><span data-stu-id="84244-107">Column</span></span></th>
<th><span data-ttu-id="84244-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="84244-108">Data Type</span></span></th>
<th><span data-ttu-id="84244-109">Ключ/индекс</span><span class="sxs-lookup"><span data-stu-id="84244-109">Key/Index</span></span></th>
<th><span data-ttu-id="84244-110">Сведения</span><span class="sxs-lookup"><span data-stu-id="84244-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="84244-111"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="84244-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="84244-112">datetime</span><span class="sxs-lookup"><span data-stu-id="84244-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="84244-113">Основной, внешний</span><span class="sxs-lookup"><span data-stu-id="84244-113">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="84244-114">Время запроса сеанса.</span><span class="sxs-lookup"><span data-stu-id="84244-114">Time of session request.</span></span> <span data-ttu-id="84244-115">Используется в сочетании с <strong>SessionIdSeq</strong> для уникальной идентификации сеанса.</span><span class="sxs-lookup"><span data-stu-id="84244-115">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="84244-116">Дополнительные сведения приведены <a href="lync-server-2013-dialogs-table.md">в таблице диалоговые окна Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="84244-116">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84244-117"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="84244-117"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="84244-118">целое</span><span class="sxs-lookup"><span data-stu-id="84244-118">int</span></span></p></td>
<td><p><span data-ttu-id="84244-119">Основной, внешний</span><span class="sxs-lookup"><span data-stu-id="84244-119">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="84244-120">ИДЕНТИФИКАЦИОНный номер для идентификации сеанса.</span><span class="sxs-lookup"><span data-stu-id="84244-120">ID number to identify the session.</span></span> <span data-ttu-id="84244-121">Используется в сочетании с <strong>SessionIdTime</strong> для уникальной идентификации сеанса.</span><span class="sxs-lookup"><span data-stu-id="84244-121">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.</span></span> <span data-ttu-id="84244-122">Дополнительные сведения приведены <a href="lync-server-2013-dialogs-table.md">в таблице диалоговые окна Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="84244-122">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84244-123"><strong>Имя файла</strong></span><span class="sxs-lookup"><span data-stu-id="84244-123"><strong>File Name</strong></span></span></p></td>
<td><p><span data-ttu-id="84244-124">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="84244-124">nvarchar(256)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="84244-125">Имя файла.</span><span class="sxs-lookup"><span data-stu-id="84244-125">Name of the file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84244-126"><strong>FileIdentity</strong></span><span class="sxs-lookup"><span data-stu-id="84244-126"><strong>FileIdentity</strong></span></span></p></td>
<td><p><span data-ttu-id="84244-127">идентификатора</span><span class="sxs-lookup"><span data-stu-id="84244-127">uniqueidentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="84244-128">Уникальный идентификатор, позволяющий отличать передачу файлов с одним и тем же именем файла.</span><span class="sxs-lookup"><span data-stu-id="84244-128">Unique identifier to distinguish between file transfers involving the same file name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84244-129"><strong>Файлах</strong></span><span class="sxs-lookup"><span data-stu-id="84244-129"><strong>Cookie</strong></span></span></p></td>
<td><p><span data-ttu-id="84244-130">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="84244-130">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="84244-131">Primary</span><span class="sxs-lookup"><span data-stu-id="84244-131">Primary</span></span></p></td>
<td><p><span data-ttu-id="84244-132">Используется для идентификации каждого сообщения к исполнению, связанного с этим сообщением.</span><span class="sxs-lookup"><span data-stu-id="84244-132">Used to identify every follow-up message as being associated with this one.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84244-133"><strong>Отвечать</strong></span><span class="sxs-lookup"><span data-stu-id="84244-133"><strong>Accept</strong></span></span></p></td>
<td><p><span data-ttu-id="84244-134">бит</span><span class="sxs-lookup"><span data-stu-id="84244-134">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="84244-135">Может иметь значение истина или NULL.</span><span class="sxs-lookup"><span data-stu-id="84244-135">Can be TRUE or NULL.</span></span> <span data-ttu-id="84244-136">Если значение равно TRUE, то значение "отклонить" и "Отмена" будет равно NULL.</span><span class="sxs-lookup"><span data-stu-id="84244-136">If TRUE, then Reject and Cancel will be NULL.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84244-137"><strong>Отклонил</strong></span><span class="sxs-lookup"><span data-stu-id="84244-137"><strong>Reject</strong></span></span></p></td>
<td><p><span data-ttu-id="84244-138">бит</span><span class="sxs-lookup"><span data-stu-id="84244-138">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="84244-139">Может иметь значение истина или NULL.</span><span class="sxs-lookup"><span data-stu-id="84244-139">Can be TRUE or NULL.</span></span> <span data-ttu-id="84244-140">Если значение равно TRUE, то "принимать" и "Отмена" будут иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="84244-140">If TRUE, then Accept and Cancel will be NULL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84244-141"><strong>Отмена</strong>.</span><span class="sxs-lookup"><span data-stu-id="84244-141"><strong>Cancel</strong></span></span></p></td>
<td><p><span data-ttu-id="84244-142">бит</span><span class="sxs-lookup"><span data-stu-id="84244-142">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="84244-143">Может иметь значение истина или NULL.</span><span class="sxs-lookup"><span data-stu-id="84244-143">Can be TRUE or NULL.</span></span> <span data-ttu-id="84244-144">Если значение равно TRUE, то принять и отклонить будет значение NULL.</span><span class="sxs-lookup"><span data-stu-id="84244-144">If TRUE, then Accept and Reject will be NULL.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="84244-145">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="84244-145">


</div>

<span> </span>

</div>

</div>

</span></span></div>

