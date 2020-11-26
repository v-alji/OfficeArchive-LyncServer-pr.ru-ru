---
title: 'Lync Server 2013: таблица User'
description: 'Lync Server 2013: пользовательская таблица.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: User table
ms:assetid: 6b52047e-286d-47ab-b7bc-a9b266f62d82
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398505(v=OCS.15)
ms:contentKeyID: 48184437
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 15d1ac08a229f4afea35a2727ef1105a5f24b826
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444170"
---
# <a name="user-table-in-lync-server-2013"></a><span data-ttu-id="749a1-103">Таблица User в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="749a1-103">User table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="749a1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="749a1-104">

<span> </span></span></span>

<span data-ttu-id="749a1-105">_**Тема последнего изменения:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="749a1-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="749a1-106">Таблица user — это вспомогательная таблица, в которой хранится список различных пользователей, которые участвовали в сеансах, записанных в базе данных.</span><span class="sxs-lookup"><span data-stu-id="749a1-106">The User table is a supporting table that stores a list of the various users who have participated in sessions recorded in the database.</span></span> <span data-ttu-id="749a1-107">Каждая запись в таблице представляет одного пользователя.</span><span class="sxs-lookup"><span data-stu-id="749a1-107">Each record in the table represents one user.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="749a1-108"><strong>Столбец</strong></span><span class="sxs-lookup"><span data-stu-id="749a1-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="749a1-109"><strong>Тип данных</strong></span><span class="sxs-lookup"><span data-stu-id="749a1-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="749a1-110"><strong>Ключ/индекс</strong></span><span class="sxs-lookup"><span data-stu-id="749a1-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="749a1-111"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="749a1-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="749a1-112"><strong>UserKey</strong></span><span class="sxs-lookup"><span data-stu-id="749a1-112"><strong>UserKey</strong></span></span></p></td>
<td><p><span data-ttu-id="749a1-113">целое</span><span class="sxs-lookup"><span data-stu-id="749a1-113">int</span></span></p></td>
<td><p><span data-ttu-id="749a1-114">Primary</span><span class="sxs-lookup"><span data-stu-id="749a1-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="749a1-115">Уникальный номер, идентифицирующий этого пользователя.</span><span class="sxs-lookup"><span data-stu-id="749a1-115">Unique number identifying this user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="749a1-116"><strong>КОД</strong></span><span class="sxs-lookup"><span data-stu-id="749a1-116"><strong>URI</strong></span></span></p></td>
<td><p><span data-ttu-id="749a1-117">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="749a1-117">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="749a1-118">Повторя</span><span class="sxs-lookup"><span data-stu-id="749a1-118">Unique</span></span></p></td>
<td><p><span data-ttu-id="749a1-119">Строка URI.</span><span class="sxs-lookup"><span data-stu-id="749a1-119">URI string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="749a1-120"><strong>URIType</strong></span><span class="sxs-lookup"><span data-stu-id="749a1-120"><strong>URIType</strong></span></span></p></td>
<td><p><span data-ttu-id="749a1-121">целое</span><span class="sxs-lookup"><span data-stu-id="749a1-121">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="749a1-122">1 — неизвестный тип URI.</span><span class="sxs-lookup"><span data-stu-id="749a1-122">1 is unknown URI type.</span></span></p>
<p><span data-ttu-id="749a1-123">2 — это универсальный код ресурса пользователя.</span><span class="sxs-lookup"><span data-stu-id="749a1-123">2 is user URI.</span></span></p>
<p><span data-ttu-id="749a1-124">4 — универсальный код ресурса Конференции.</span><span class="sxs-lookup"><span data-stu-id="749a1-124">4 is conference URI.</span></span></p>
<p><span data-ttu-id="749a1-125">8 — это универсальный код ресурса (URI) телефона.</span><span class="sxs-lookup"><span data-stu-id="749a1-125">8 is phone URI.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="749a1-126"><strong>TenantKey</strong></span><span class="sxs-lookup"><span data-stu-id="749a1-126"><strong>TenantKey</strong></span></span></p></td>
<td><p><span data-ttu-id="749a1-127">целое</span><span class="sxs-lookup"><span data-stu-id="749a1-127">int</span></span></p></td>
<td><p><span data-ttu-id="749a1-128">Другом</span><span class="sxs-lookup"><span data-stu-id="749a1-128">Foreign</span></span></p></td>
<td><p><span data-ttu-id="749a1-129">Клиент для пользователя, на который ссылается таблица "клиент".</span><span class="sxs-lookup"><span data-stu-id="749a1-129">Tenant of the user, referenced from tenant table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="749a1-130"><strong>LastPoorCallTime</strong></span><span class="sxs-lookup"><span data-stu-id="749a1-130"><strong>LastPoorCallTime</strong></span></span></p></td>
<td><p><span data-ttu-id="749a1-131">datetime</span><span class="sxs-lookup"><span data-stu-id="749a1-131">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="749a1-132">Самая поздняя метка времени, когда пользователь приходил к вызову неудовлетворительного звука.</span><span class="sxs-lookup"><span data-stu-id="749a1-132">Latest time stamp when the user had a poor audio call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="749a1-133"><strong>NextUpdateTS</strong></span><span class="sxs-lookup"><span data-stu-id="749a1-133"><strong>NextUpdateTS</strong></span></span></p></td>
<td><p><span data-ttu-id="749a1-134">datetime</span><span class="sxs-lookup"><span data-stu-id="749a1-134">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="749a1-135">Только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="749a1-135">For internal use only.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="749a1-136">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="749a1-136">


</div>

<span> </span>

</div>

</div>

</span></span></div>

