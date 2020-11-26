---
title: 'Lync Server 2013: представление FileTransfers'
description: 'Lync Server 2013: FileTransfers View.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: FileTransfers view
ms:assetid: e52c3ad0-152e-4a18-af1c-1aff0d205151
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721914(v=OCS.15)
ms:contentKeyID: 49733848
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dd2b084274a4d5daa093f2269617214f703ac03e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428155"
---
# <a name="filetransfers-view-in-lync-server-2013"></a><span data-ttu-id="75e5a-103">FileTransfers представления в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="75e5a-103">FileTransfers view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="75e5a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="75e5a-104">

<span> </span></span></span>

<span data-ttu-id="75e5a-105">_**Тема последнего изменения:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="75e5a-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="75e5a-106">В представлении FileTransfer хранятся сведения о одноранговых сеансах передачи файлов.</span><span class="sxs-lookup"><span data-stu-id="75e5a-106">The FileTransfer view stores information about peer-to-peer file transfer sessions.</span></span> <span data-ttu-id="75e5a-107">Это представление было представлено в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="75e5a-107">This view was introduced in Microsoft Lync Server 2013.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="75e5a-108">В представлении FileTransfers содержатся все столбцы в <A href="lync-server-2013-sessiondetails-view.md">представлении SessionDetails в Lync Server 2013</A> в дополнение к столбцам, перечисленным ниже.</span><span class="sxs-lookup"><span data-stu-id="75e5a-108">The FileTransfers view contains all of the columns in the <A href="lync-server-2013-sessiondetails-view.md">SessionDetails view in Lync Server 2013</A> in addition the columns listed below.</span></span>



</div>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="75e5a-109">Столбец</span><span class="sxs-lookup"><span data-stu-id="75e5a-109">Column</span></span></th>
<th><span data-ttu-id="75e5a-110">Тип данных</span><span class="sxs-lookup"><span data-stu-id="75e5a-110">Data Type</span></span></th>
<th><span data-ttu-id="75e5a-111">Подробности</span><span class="sxs-lookup"><span data-stu-id="75e5a-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="75e5a-112"><strong>FileName</strong></span><span class="sxs-lookup"><span data-stu-id="75e5a-112"><strong>FileName</strong></span></span></p></td>
<td><p><span data-ttu-id="75e5a-113">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="75e5a-113">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="75e5a-114">Имя перенесенного файла.</span><span class="sxs-lookup"><span data-stu-id="75e5a-114">Name of the file transferred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75e5a-115"><strong>Файлах</strong></span><span class="sxs-lookup"><span data-stu-id="75e5a-115"><strong>Cookie</strong></span></span></p></td>
<td><p><span data-ttu-id="75e5a-116">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="75e5a-116">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="75e5a-117">Используется для идентификации каждого сообщения к исполнению, связанного с этим сообщением.</span><span class="sxs-lookup"><span data-stu-id="75e5a-117">Used to identify every follow-up message as being associated with this one.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75e5a-118"><strong>FileIdentity</strong></span><span class="sxs-lookup"><span data-stu-id="75e5a-118"><strong>FileIdentity</strong></span></span></p></td>
<td><p><span data-ttu-id="75e5a-119">идентификатора</span><span class="sxs-lookup"><span data-stu-id="75e5a-119">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="75e5a-120">Уникальный идентификатор, позволяющий отличать передачу файлов с одним и тем же именем файла.</span><span class="sxs-lookup"><span data-stu-id="75e5a-120">Unique identifier to distinguish between file transfers involving the same file name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75e5a-121"><strong>Отвечать</strong></span><span class="sxs-lookup"><span data-stu-id="75e5a-121"><strong>Accept</strong></span></span></p></td>
<td><p><span data-ttu-id="75e5a-122">бит</span><span class="sxs-lookup"><span data-stu-id="75e5a-122">bit</span></span></p></td>
<td><p><span data-ttu-id="75e5a-123">Может иметь значение истина или NULL.</span><span class="sxs-lookup"><span data-stu-id="75e5a-123">Can be TRUE or NULL.</span></span> <span data-ttu-id="75e5a-124">Если значение равно TRUE, то значение "отклонить" и "Отмена" будет равно NULL.</span><span class="sxs-lookup"><span data-stu-id="75e5a-124">If TRUE, then Reject and Cancel will be NULL.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75e5a-125"><strong>Отклонил</strong></span><span class="sxs-lookup"><span data-stu-id="75e5a-125"><strong>Reject</strong></span></span></p></td>
<td><p><span data-ttu-id="75e5a-126">бит</span><span class="sxs-lookup"><span data-stu-id="75e5a-126">bit</span></span></p></td>
<td><p><span data-ttu-id="75e5a-127">Может иметь значение истина или NULL.</span><span class="sxs-lookup"><span data-stu-id="75e5a-127">Can be TRUE or NULL.</span></span> <span data-ttu-id="75e5a-128">Если значение равно TRUE, то "принимать" и "Отмена" будут иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="75e5a-128">If TRUE, then Accept and Cancel will be NULL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75e5a-129"><strong>Отмена</strong>.</span><span class="sxs-lookup"><span data-stu-id="75e5a-129"><strong>Cancel</strong></span></span></p></td>
<td><p><span data-ttu-id="75e5a-130">бит</span><span class="sxs-lookup"><span data-stu-id="75e5a-130">bit</span></span></p></td>
<td><p><span data-ttu-id="75e5a-131">Может иметь значение истина или NULL.</span><span class="sxs-lookup"><span data-stu-id="75e5a-131">Can be TRUE or NULL.</span></span> <span data-ttu-id="75e5a-132">Если значение равно TRUE, то принять и отклонить будет значение NULL.</span><span class="sxs-lookup"><span data-stu-id="75e5a-132">If TRUE, then Accept and Reject will be NULL.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="75e5a-133">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="75e5a-133">


</div>

<span> </span>

</div>

</div>

</span></span></div>

