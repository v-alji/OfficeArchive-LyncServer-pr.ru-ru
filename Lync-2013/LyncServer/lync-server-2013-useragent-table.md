---
title: 'Lync Server 2013: таблица UserAgent'
description: 'Таблица Lync Server 2013: UserAgent.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: UserAgent table
ms:assetid: d6bda1c0-b053-457a-9ffa-2ae859788775
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398939(v=OCS.15)
ms:contentKeyID: 48185582
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b701d8384313d0267dd566e0c32242f6cc077472
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439130"
---
# <a name="useragent-table-in-lync-server-2013"></a><span data-ttu-id="cdeff-103">Таблица UserAgent в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cdeff-103">UserAgent table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cdeff-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cdeff-104">

<span> </span></span></span>

<span data-ttu-id="cdeff-105">_**Тема последнего изменения:** 2012-05-25_</span><span class="sxs-lookup"><span data-stu-id="cdeff-105">_**Topic Last Modified:** 2012-05-25_</span></span>

<span data-ttu-id="cdeff-106">Таблица UserAgent является вспомогательной таблицей, в которой хранится список различных агентов пользователей, которые участвовали в сеансах, записанных в базе данных.</span><span class="sxs-lookup"><span data-stu-id="cdeff-106">The UserAgent table is a supporting table that stores a list of the various user agents that have participated in sessions recorded in the database.</span></span> <span data-ttu-id="cdeff-107">Каждая запись в таблице представляет одного агента пользователя</span><span class="sxs-lookup"><span data-stu-id="cdeff-107">Each record in the table represents one user agent</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cdeff-108"><strong>Столбец</strong></span><span class="sxs-lookup"><span data-stu-id="cdeff-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="cdeff-109"><strong>Тип данных</strong></span><span class="sxs-lookup"><span data-stu-id="cdeff-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="cdeff-110"><strong>Ключ/индекс</strong></span><span class="sxs-lookup"><span data-stu-id="cdeff-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="cdeff-111"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="cdeff-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cdeff-112"><strong>UserAgentKey</strong></span><span class="sxs-lookup"><span data-stu-id="cdeff-112"><strong>UserAgentKey</strong></span></span></p></td>
<td><p><span data-ttu-id="cdeff-113">целое</span><span class="sxs-lookup"><span data-stu-id="cdeff-113">int</span></span></p></td>
<td><p><span data-ttu-id="cdeff-114">Primary</span><span class="sxs-lookup"><span data-stu-id="cdeff-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="cdeff-115">Уникальный номер, идентифицирующий агент пользователя.</span><span class="sxs-lookup"><span data-stu-id="cdeff-115">Unique number identifying this user agent.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdeff-116"><strong>UserAgent</strong></span><span class="sxs-lookup"><span data-stu-id="cdeff-116"><strong>UserAgent</strong></span></span></p></td>
<td><p><span data-ttu-id="cdeff-117">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="cdeff-117">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="cdeff-118">Повторя</span><span class="sxs-lookup"><span data-stu-id="cdeff-118">Unique</span></span></p></td>
<td><p><span data-ttu-id="cdeff-119">Строка агента пользователя.</span><span class="sxs-lookup"><span data-stu-id="cdeff-119">User Agent string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdeff-120"><strong>UAType</strong></span><span class="sxs-lookup"><span data-stu-id="cdeff-120"><strong>UAType</strong></span></span></p></td>
<td><p><span data-ttu-id="cdeff-121">smallint</span><span class="sxs-lookup"><span data-stu-id="cdeff-121">smallint</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="cdeff-122">1 — сервер исправлений.</span><span class="sxs-lookup"><span data-stu-id="cdeff-122">1 is Mediation Server.</span></span></p>
<p><span data-ttu-id="cdeff-123">2 — это сервер конференц-связи с/V.</span><span class="sxs-lookup"><span data-stu-id="cdeff-123">2 is A/V Conferencing Server.</span></span></p>
<p><span data-ttu-id="cdeff-124">4 — Lync.</span><span class="sxs-lookup"><span data-stu-id="cdeff-124">4 is Lync.</span></span></p>
<p><span data-ttu-id="cdeff-125">8 — это IP-телефон.</span><span class="sxs-lookup"><span data-stu-id="cdeff-125">8 is IP Phone.</span></span></p>
<p><span data-ttu-id="cdeff-126">16 — консоль Live Meeting.</span><span class="sxs-lookup"><span data-stu-id="cdeff-126">16 is Live Meeting Console.</span></span></p>
<p><span data-ttu-id="cdeff-127">32 — средство проверки развертывания (DVT).</span><span class="sxs-lookup"><span data-stu-id="cdeff-127">32 is Deployment Validation Tool (DVT).</span></span></p>
<p><span data-ttu-id="cdeff-128">64 — Lync на компьютерах Macintosh.</span><span class="sxs-lookup"><span data-stu-id="cdeff-128">64 is Lync on Macintosh computers.</span></span></p>
<p><span data-ttu-id="cdeff-129">128 – это Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="cdeff-129">128 is Office Communications Server 2007 R2 Attendant.</span></span></p>
<p><span data-ttu-id="cdeff-130">256 является службой объявлений конференций.</span><span class="sxs-lookup"><span data-stu-id="cdeff-130">256 is Conferencing Announcement service.</span></span></p>
<p><span data-ttu-id="cdeff-131">512 — автоматический секретарь конференц-связи.</span><span class="sxs-lookup"><span data-stu-id="cdeff-131">512 is Conferencing Auto Attendant.</span></span></p>
<p><span data-ttu-id="cdeff-132">1024 является приложением группы ответа.</span><span class="sxs-lookup"><span data-stu-id="cdeff-132">1024 is Response Group application.</span></span></p>
<p><span data-ttu-id="cdeff-133">2048 находится за пределами голосового контроля.</span><span class="sxs-lookup"><span data-stu-id="cdeff-133">2048 is Outside Voice Control.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="cdeff-134">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cdeff-134">


</div>

<span> </span>

</div>

</div>

</span></span></div>

