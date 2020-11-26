---
title: 'Lync Server 2013: таблица ErrorDef'
description: 'Таблица Lync Server 2013: ErrorDef.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ErrorDef table
ms:assetid: 6acf3b86-da61-4923-9812-300db6f66dec
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398503(v=OCS.15)
ms:contentKeyID: 48184403
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e58980a671b54007012bbbf6780e24c162aebe00
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428540"
---
# <a name="errordef-table-in-lync-server-2013"></a><span data-ttu-id="edd3b-103">Таблица ErrorDef в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="edd3b-103">ErrorDef table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="edd3b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="edd3b-104">

<span> </span></span></span>

<span data-ttu-id="edd3b-105">_**Тема последнего изменения:** 2012-05-25_</span><span class="sxs-lookup"><span data-stu-id="edd3b-105">_**Topic Last Modified:** 2012-05-25_</span></span>

<span data-ttu-id="edd3b-106">В таблице ErrorDef хранятся сведения о каждом типе ошибки, которые могут возникать.</span><span class="sxs-lookup"><span data-stu-id="edd3b-106">The ErrorDef table stores information about each type of error that may occur.</span></span> <span data-ttu-id="edd3b-107">Каждая запись имеет один тип ошибки.</span><span class="sxs-lookup"><span data-stu-id="edd3b-107">Each record is one type of error.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="edd3b-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="edd3b-108">Column</span></span></th>
<th><span data-ttu-id="edd3b-109">Тип данных</span><span class="sxs-lookup"><span data-stu-id="edd3b-109">Data Type</span></span></th>
<th><span data-ttu-id="edd3b-110">Ключ/индекс</span><span class="sxs-lookup"><span data-stu-id="edd3b-110">Key/Index</span></span></th>
<th><span data-ttu-id="edd3b-111">Сведения</span><span class="sxs-lookup"><span data-stu-id="edd3b-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="edd3b-112"><strong>ErrorId</strong></span><span class="sxs-lookup"><span data-stu-id="edd3b-112"><strong>ErrorId</strong></span></span></p></td>
<td><p><span data-ttu-id="edd3b-113">целое</span><span class="sxs-lookup"><span data-stu-id="edd3b-113">int</span></span></p></td>
<td><p><span data-ttu-id="edd3b-114">Primary</span><span class="sxs-lookup"><span data-stu-id="edd3b-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="edd3b-115">Уникальный ИДЕНТИФИКАЦИОНный номер, показывающий этот тип ошибки.</span><span class="sxs-lookup"><span data-stu-id="edd3b-115">Unique ID number identifying this type of error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="edd3b-116"><strong>ResponseCode</strong></span><span class="sxs-lookup"><span data-stu-id="edd3b-116"><strong>ResponseCode</strong></span></span></p></td>
<td><p><span data-ttu-id="edd3b-117">целое</span><span class="sxs-lookup"><span data-stu-id="edd3b-117">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="edd3b-118">Стандартный код ответа SIP, связанный с этой ошибкой.</span><span class="sxs-lookup"><span data-stu-id="edd3b-118">Standard SIP response code associated with this error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="edd3b-119"><strong>MsDiagId</strong></span><span class="sxs-lookup"><span data-stu-id="edd3b-119"><strong>MsDiagId</strong></span></span></p></td>
<td><p><span data-ttu-id="edd3b-120">целое</span><span class="sxs-lookup"><span data-stu-id="edd3b-120">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="edd3b-121">Идентификатор диагностики (Майкрософт).</span><span class="sxs-lookup"><span data-stu-id="edd3b-121">Microsoft Diagnostic ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="edd3b-122"><strong>CallTypeId</strong></span><span class="sxs-lookup"><span data-stu-id="edd3b-122"><strong>CallTypeId</strong></span></span></p></td>
<td><p><span data-ttu-id="edd3b-123">Типом</span><span class="sxs-lookup"><span data-stu-id="edd3b-123">Int</span></span></p></td>
<td><p><span data-ttu-id="edd3b-124">Другом</span><span class="sxs-lookup"><span data-stu-id="edd3b-124">Foreign</span></span></p></td>
<td><p><span data-ttu-id="edd3b-125">Тип звонка.</span><span class="sxs-lookup"><span data-stu-id="edd3b-125">Type of the call.</span></span> <span data-ttu-id="edd3b-126">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-calltype-table.md">таблицей CallType в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="edd3b-126">See the <a href="lync-server-2013-calltype-table.md">CallType table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="edd3b-127"><strong>RequestType</strong></span><span class="sxs-lookup"><span data-stu-id="edd3b-127"><strong>RequestType</strong></span></span></p></td>
<td><p><span data-ttu-id="edd3b-128">varbinary (33)</span><span class="sxs-lookup"><span data-stu-id="edd3b-128">varbinary(33)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="edd3b-129">Тип запроса, который завершился сбоем.</span><span class="sxs-lookup"><span data-stu-id="edd3b-129">Type of request that failed.</span></span></p>
<p><span data-ttu-id="edd3b-130">Эти данные можно преобразовать в текстовый формат, используя следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="edd3b-130">This data can be converted to text format by using this syntax:</span></span></p>
<p><code>cast(cast(RequestType as varbinary(max)) as varchar(max))</code></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="edd3b-131"><strong>Контента</strong></span><span class="sxs-lookup"><span data-stu-id="edd3b-131"><strong>ContentType</strong></span></span></p></td>
<td><p><span data-ttu-id="edd3b-132">varbinary (257)</span><span class="sxs-lookup"><span data-stu-id="edd3b-132">varbinary(257)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="edd3b-133">Тип контента запроса, который завершился сбоем.</span><span class="sxs-lookup"><span data-stu-id="edd3b-133">Content type of the request that failed.</span></span></p>
<p><span data-ttu-id="edd3b-134">Эти данные можно преобразовать в текстовый формат с помощью синтаксиса:</span><span class="sxs-lookup"><span data-stu-id="edd3b-134">This data can be converted to text format by using this syntaxt:</span></span></p>
<p><code>cast(cast(ContentType as varbinary(max)) as varchar(max))</code></p></td>
</tr>
</tbody>
</table><span data-ttu-id="edd3b-135">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="edd3b-135">


</div>

<span> </span>

</div>

</div>

</span></span></div>

