---
title: 'Lync Server 2013: tblComplianceData'
description: 'Lync Server 2013: tblComplianceData.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblComplianceData
ms:assetid: 05b28f9b-4aba-4b69-ba8d-2ceeb6cbfaac
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558606(v=OCS.15)
ms:contentKeyID: 48183308
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3c597d67054303de2753182b37419f68051d3af8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444478"
---
# <a name="tblcompliancedata-in-lync-server-2013"></a><span data-ttu-id="7ec24-103">tblComplianceData в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7ec24-103">tblComplianceData in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7ec24-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7ec24-104">

<span> </span></span></span>

<span data-ttu-id="7ec24-105">_**Тема последнего изменения:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="7ec24-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="7ec24-106">tblComplianceData содержит события соответствия требованиям, которые пока не обрабатывались адаптером соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="7ec24-106">tblComplianceData contains the compliance events that have not been processed by the compliance adapter yet.</span></span>

### <a name="columns"></a><span data-ttu-id="7ec24-107">Столбцов</span><span class="sxs-lookup"><span data-stu-id="7ec24-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7ec24-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="7ec24-108">Column</span></span></th>
<th><span data-ttu-id="7ec24-109">Тип</span><span class="sxs-lookup"><span data-stu-id="7ec24-109">Type</span></span></th>
<th><span data-ttu-id="7ec24-110">Описание</span><span class="sxs-lookup"><span data-stu-id="7ec24-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7ec24-111">cmplEventID</span><span class="sxs-lookup"><span data-stu-id="7ec24-111">cmplEventID</span></span></p></td>
<td><p><span data-ttu-id="7ec24-112">bigint, NOT NULL</span><span class="sxs-lookup"><span data-stu-id="7ec24-112">bigint, not null</span></span></p></td>
<td><p><span data-ttu-id="7ec24-113">Код события.</span><span class="sxs-lookup"><span data-stu-id="7ec24-113">Event ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ec24-114">entryDate</span><span class="sxs-lookup"><span data-stu-id="7ec24-114">entryDate</span></span></p></td>
<td><p><span data-ttu-id="7ec24-115">smalldatetime, NOT NULL</span><span class="sxs-lookup"><span data-stu-id="7ec24-115">smalldatetime, not null</span></span></p></td>
<td><p><span data-ttu-id="7ec24-116">Время вставки (может быть в будущем для cmplType = 9, так как в этом случае запись является заполнителем в этом случае).</span><span class="sxs-lookup"><span data-stu-id="7ec24-116">Time of insertion (may be far in the future for cmplType=9 because the entry is just a placeholder in that case).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ec24-117">cmplType</span><span class="sxs-lookup"><span data-stu-id="7ec24-117">cmplType</span></span></p></td>
<td><p><span data-ttu-id="7ec24-118">int, NOT NULL</span><span class="sxs-lookup"><span data-stu-id="7ec24-118">int, not null</span></span></p></td>
<td><p><span data-ttu-id="7ec24-119">Тип события соответствия:</span><span class="sxs-lookup"><span data-stu-id="7ec24-119">Type of compliance event:</span></span></p>
<ul>
<li><p><span data-ttu-id="7ec24-120">1: чат</span><span class="sxs-lookup"><span data-stu-id="7ec24-120">1: Chat</span></span></p></li>
<li><p><span data-ttu-id="7ec24-121">2: чат</span><span class="sxs-lookup"><span data-stu-id="7ec24-121">2: Backchat</span></span></p></li>
<li><p><span data-ttu-id="7ec24-122">3: Загрузка файла</span><span class="sxs-lookup"><span data-stu-id="7ec24-122">3: File download</span></span></p></li>
<li><p><span data-ttu-id="7ec24-123">4: Отправка файлов</span><span class="sxs-lookup"><span data-stu-id="7ec24-123">4: File upload</span></span></p></li>
<li><p><span data-ttu-id="7ec24-124">9: подготовка к передаче файлов</span><span class="sxs-lookup"><span data-stu-id="7ec24-124">9: Provisional file transfer</span></span></p></li>
<li><p><span data-ttu-id="7ec24-125">10: удаление чата (с заменой)</span><span class="sxs-lookup"><span data-stu-id="7ec24-125">10: Chat deletion (with replace)</span></span></p></li>
<li><p><span data-ttu-id="7ec24-126">11: Очистка чата</span><span class="sxs-lookup"><span data-stu-id="7ec24-126">11: Chat purging</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ec24-127">cmplTime</span><span class="sxs-lookup"><span data-stu-id="7ec24-127">cmplTime</span></span></p></td>
<td><p><span data-ttu-id="7ec24-128">bigint, NOT NULL</span><span class="sxs-lookup"><span data-stu-id="7ec24-128">bigint, not null</span></span></p></td>
<td><p><span data-ttu-id="7ec24-129">Метка времени для события.</span><span class="sxs-lookup"><span data-stu-id="7ec24-129">Time stamp for the event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ec24-130">cmplChannelUri</span><span class="sxs-lookup"><span data-stu-id="7ec24-130">cmplChannelUri</span></span></p></td>
<td><p><span data-ttu-id="7ec24-131">nvarchar (255), NOT NULL</span><span class="sxs-lookup"><span data-stu-id="7ec24-131">nvarchar (255), not null</span></span></p></td>
<td><p><span data-ttu-id="7ec24-132">Универсальный код ресурса (URI) канала.</span><span class="sxs-lookup"><span data-stu-id="7ec24-132">Channel Uniform Resource Identifier (URI).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ec24-133">cmplChatID</span><span class="sxs-lookup"><span data-stu-id="7ec24-133">cmplChatID</span></span></p></td>
<td><p><span data-ttu-id="7ec24-134">bigint</span><span class="sxs-lookup"><span data-stu-id="7ec24-134">bigint</span></span></p></td>
<td><p><span data-ttu-id="7ec24-135">ИДЕНТИФИКАТОР чата (соответствующая таблице tblChat. chatId).</span><span class="sxs-lookup"><span data-stu-id="7ec24-135">Chat ID (corresponding to tblChat.chatId table).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ec24-136">cmplUserID</span><span class="sxs-lookup"><span data-stu-id="7ec24-136">cmplUserID</span></span></p></td>
<td><p><span data-ttu-id="7ec24-137">int, NOT NULL</span><span class="sxs-lookup"><span data-stu-id="7ec24-137">int, not null</span></span></p></td>
<td><p><span data-ttu-id="7ec24-138">Идентификатор участника афиши (соответствующий таблице tblPrincipal. prinID).</span><span class="sxs-lookup"><span data-stu-id="7ec24-138">Principal ID of the poster (corresponding to tblPrincipal.prinID table).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ec24-139">cmplUserUri</span><span class="sxs-lookup"><span data-stu-id="7ec24-139">cmplUserUri</span></span></p></td>
<td><p><span data-ttu-id="7ec24-140">nvarchar (255), NOT NULL</span><span class="sxs-lookup"><span data-stu-id="7ec24-140">nvarchar (255), not null</span></span></p></td>
<td><p><span data-ttu-id="7ec24-141">URI пользователя.</span><span class="sxs-lookup"><span data-stu-id="7ec24-141">User URI.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ec24-142">cmplMessage</span><span class="sxs-lookup"><span data-stu-id="7ec24-142">cmplMessage</span></span></p></td>
<td><p><span data-ttu-id="7ec24-143">nvarchar (max)</span><span class="sxs-lookup"><span data-stu-id="7ec24-143">nvarchar (max)</span></span></p></td>
<td><p><span data-ttu-id="7ec24-144">Сообщение (Кодировка зависит от cmplType).</span><span class="sxs-lookup"><span data-stu-id="7ec24-144">Message (encoding depends on cmplType).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="key"></a><span data-ttu-id="7ec24-145">Ключ</span><span class="sxs-lookup"><span data-stu-id="7ec24-145">Key</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7ec24-146">Столбец</span><span class="sxs-lookup"><span data-stu-id="7ec24-146">Column</span></span></th>
<th><span data-ttu-id="7ec24-147">Описание</span><span class="sxs-lookup"><span data-stu-id="7ec24-147">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7ec24-148">cmplEventID</span><span class="sxs-lookup"><span data-stu-id="7ec24-148">cmplEventID</span></span></p></td>
<td><p><span data-ttu-id="7ec24-149">Первичный ключ.</span><span class="sxs-lookup"><span data-stu-id="7ec24-149">Primary key.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="7ec24-150">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7ec24-150">


</div>

<span> </span>

</div>

</div>

</span></span></div>

