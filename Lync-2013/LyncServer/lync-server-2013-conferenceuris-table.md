---
title: 'Lync Server 2013: таблица ConferenceUris'
description: 'Таблица Lync Server 2013: ConferenceUris.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ConferenceUris table
ms:assetid: b1721d52-3c65-45ea-8997-06af8fef93fc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412854(v=OCS.15)
ms:contentKeyID: 48185160
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a142aa9ad1fe4d3ae92aa3e21aa9eee505457cbe
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434391"
---
# <a name="conferenceuris-table-in-lync-server-2013"></a><span data-ttu-id="40953-103">Таблица ConferenceUris в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="40953-103">ConferenceUris table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="40953-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="40953-104">

<span> </span></span></span>

<span data-ttu-id="40953-105">_**Тема последнего изменения:** 2012-05-25_</span><span class="sxs-lookup"><span data-stu-id="40953-105">_**Topic Last Modified:** 2012-05-25_</span></span>

<span data-ttu-id="40953-106">Таблица ConfereneUris является вспомогательной таблицей, в которой хранится список различных URI конференций, участвующих в сеансах конференц-связи, записанных в базу данных.</span><span class="sxs-lookup"><span data-stu-id="40953-106">The ConfereneUris table is a supporting table that stores a list of the various conference URIs that have participated in conference sessions recorded in the database.</span></span> <span data-ttu-id="40953-107">Каждая запись в таблице представляет один URI конференции.</span><span class="sxs-lookup"><span data-stu-id="40953-107">Each record in the table represents one conference URI.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="40953-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="40953-108">Column</span></span></th>
<th><span data-ttu-id="40953-109">Тип данных</span><span class="sxs-lookup"><span data-stu-id="40953-109">Data Type</span></span></th>
<th><span data-ttu-id="40953-110">Ключ/индекс</span><span class="sxs-lookup"><span data-stu-id="40953-110">Key/Index</span></span></th>
<th><span data-ttu-id="40953-111">Сведения</span><span class="sxs-lookup"><span data-stu-id="40953-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="40953-112"><strong>NextUpdateTS</strong></span><span class="sxs-lookup"><span data-stu-id="40953-112"><strong>NextUpdateTS</strong></span></span></p></td>
<td><p><span data-ttu-id="40953-113">datetime</span><span class="sxs-lookup"><span data-stu-id="40953-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="40953-114">Primary</span><span class="sxs-lookup"><span data-stu-id="40953-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="40953-115">Метка времени, используемая в качестве внутренней.</span><span class="sxs-lookup"><span data-stu-id="40953-115">Time stamp, Internal used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40953-116"><strong>ConferenceUriId</strong></span><span class="sxs-lookup"><span data-stu-id="40953-116"><strong>ConferenceUriId</strong></span></span></p></td>
<td><p><span data-ttu-id="40953-117">целое</span><span class="sxs-lookup"><span data-stu-id="40953-117">int</span></span></p></td>
<td><p><span data-ttu-id="40953-118">Primary</span><span class="sxs-lookup"><span data-stu-id="40953-118">Primary</span></span></p></td>
<td><p><span data-ttu-id="40953-119">Уникальный номер, идентифицирующий этот URI конференции.</span><span class="sxs-lookup"><span data-stu-id="40953-119">Unique number identifying this conference URI.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40953-120"><strong>ConferenceUri</strong></span><span class="sxs-lookup"><span data-stu-id="40953-120"><strong>ConferenceUri</strong></span></span></p></td>
<td><p><span data-ttu-id="40953-121">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="40953-121">nvarchar(450)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="40953-122">Универсальный код ресурса (URI) Конференции.</span><span class="sxs-lookup"><span data-stu-id="40953-122">Conference URI.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40953-123"><strong>Счет</strong></span><span class="sxs-lookup"><span data-stu-id="40953-123"><strong>Checksum</strong></span></span></p></td>
<td><p><span data-ttu-id="40953-124">целое</span><span class="sxs-lookup"><span data-stu-id="40953-124">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="40953-125">Контрольная сумма для ConferenceUri.</span><span class="sxs-lookup"><span data-stu-id="40953-125">Checksum of ConferenceUri.</span></span> <span data-ttu-id="40953-126">Используется для увеличения скорости поиска в базе данных.</span><span class="sxs-lookup"><span data-stu-id="40953-126">Used to increases the speed of database searches.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40953-127"><strong>UriTypeId</strong></span><span class="sxs-lookup"><span data-stu-id="40953-127"><strong>UriTypeId</strong></span></span></p></td>
<td><p><span data-ttu-id="40953-128">целое</span><span class="sxs-lookup"><span data-stu-id="40953-128">int</span></span></p></td>
<td><p><span data-ttu-id="40953-129">Другом</span><span class="sxs-lookup"><span data-stu-id="40953-129">Foreign</span></span></p></td>
<td><p><span data-ttu-id="40953-130">Тип URI, например conf: чат для Конференции с помощью мгновенных сообщений или conf: аудио-видео для голосовой и видеоконференции.</span><span class="sxs-lookup"><span data-stu-id="40953-130">URI type, such as conf:chat for IM conference, or conf:audio-video for audio/video conference.</span></span> <span data-ttu-id="40953-131">Более подробную информацию вы увидите в <a href="lync-server-2013-uritypes-table.md">таблице UriTypes в таблице Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="40953-131">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> table for more information.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="40953-132">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="40953-132">


</div>

<span> </span>

</div>

</div>

</span></span></div>

