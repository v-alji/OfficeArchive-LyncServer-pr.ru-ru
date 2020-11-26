---
title: 'Lync Server 2013: tblComplianceParticipant'
description: 'Lync Server 2013: tblComplianceParticipant.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblComplianceParticipant
ms:assetid: 5d7e0dea-74f7-46d1-badf-b94abc8f066d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558655(v=OCS.15)
ms:contentKeyID: 48184262
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c1385b0a635f003a72de93f10f72642314ad7ebd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444457"
---
# <a name="tblcomplianceparticipant-in-lync-server-2013"></a><span data-ttu-id="68367-103">tblComplianceParticipant в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="68367-103">tblComplianceParticipant in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="68367-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="68367-104">

<span> </span></span></span>

<span data-ttu-id="68367-105">_**Тема последнего изменения:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="68367-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="68367-106">tblComplianceParticipant включает текущих участников на канал и на сервер.</span><span class="sxs-lookup"><span data-stu-id="68367-106">tblComplianceParticipant contains the current participants per channel and per server.</span></span>

### <a name="columns"></a><span data-ttu-id="68367-107">Столбцов</span><span class="sxs-lookup"><span data-stu-id="68367-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="68367-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="68367-108">Column</span></span></th>
<th><span data-ttu-id="68367-109">Тип</span><span class="sxs-lookup"><span data-stu-id="68367-109">Type</span></span></th>
<th><span data-ttu-id="68367-110">Описание</span><span class="sxs-lookup"><span data-stu-id="68367-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="68367-111">channelUri</span><span class="sxs-lookup"><span data-stu-id="68367-111">channelUri</span></span></p></td>
<td><p><span data-ttu-id="68367-112">nvarchar (255), NOT NULL</span><span class="sxs-lookup"><span data-stu-id="68367-112">nvarchar (255), not null</span></span></p></td>
<td><p><span data-ttu-id="68367-113">Универсальный код ресурса (URI) канала.</span><span class="sxs-lookup"><span data-stu-id="68367-113">Channel Uniform Resource Identifier (URI).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="68367-114">Идентификатора пользователя</span><span class="sxs-lookup"><span data-stu-id="68367-114">userId</span></span></p></td>
<td><p><span data-ttu-id="68367-115">int, NOT NULL</span><span class="sxs-lookup"><span data-stu-id="68367-115">int, not null</span></span></p></td>
<td><p><span data-ttu-id="68367-116">Идентификатор участника (соответствующий таблице tblPrincipal. prinID).</span><span class="sxs-lookup"><span data-stu-id="68367-116">Principal ID of the participant (corresponding to tblPrincipal.prinID table).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="68367-117">joinedAt</span><span class="sxs-lookup"><span data-stu-id="68367-117">joinedAt</span></span></p></td>
<td><p><span data-ttu-id="68367-118">bigint, NOT NULL</span><span class="sxs-lookup"><span data-stu-id="68367-118">bigint, not null</span></span></p></td>
<td><p><span data-ttu-id="68367-119">Метка времени присоединения к событию.</span><span class="sxs-lookup"><span data-stu-id="68367-119">Time stamp of the joining event.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="68367-120">partedAt</span><span class="sxs-lookup"><span data-stu-id="68367-120">partedAt</span></span></p></td>
<td><p><span data-ttu-id="68367-121">bigint</span><span class="sxs-lookup"><span data-stu-id="68367-121">bigint</span></span></p></td>
<td><p><span data-ttu-id="68367-122">NULL, если участник все еще присоединен.</span><span class="sxs-lookup"><span data-stu-id="68367-122">Null if participant is still joined.</span></span> <span data-ttu-id="68367-123">Метка времени события выхода канала, если значение не равно null.</span><span class="sxs-lookup"><span data-stu-id="68367-123">The time stamp of the channel leaving event if not null.</span></span></p>
<p><span data-ttu-id="68367-124">Эти записи в конечном итоге удаляются, когда все переводчики обрабатывают событие.</span><span class="sxs-lookup"><span data-stu-id="68367-124">These entries are eventually removed when all translators process the event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="68367-125">userUri</span><span class="sxs-lookup"><span data-stu-id="68367-125">userUri</span></span></p></td>
<td><p><span data-ttu-id="68367-126">nvarchar (255), NOT NULL</span><span class="sxs-lookup"><span data-stu-id="68367-126">nvarchar(255), not null</span></span></p></td>
<td><p><span data-ttu-id="68367-127">URI пользователя.</span><span class="sxs-lookup"><span data-stu-id="68367-127">User URI.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="68367-128">serverID</span><span class="sxs-lookup"><span data-stu-id="68367-128">serverID</span></span></p></td>
<td><p><span data-ttu-id="68367-129">целое</span><span class="sxs-lookup"><span data-stu-id="68367-129">int</span></span></p></td>
<td><p><span data-ttu-id="68367-130">Идентификация сервера (как в таблице tblServerIdentity. serverID).</span><span class="sxs-lookup"><span data-stu-id="68367-130">Server identity (as in tblServerIdentity.serverID table).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="68367-131">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="68367-131">sessionId</span></span></p></td>
<td><p><span data-ttu-id="68367-132">bigint</span><span class="sxs-lookup"><span data-stu-id="68367-132">bigint</span></span></p></td>
<td><p><span data-ttu-id="68367-133">Сеанс сервера.</span><span class="sxs-lookup"><span data-stu-id="68367-133">Server session.</span></span> <span data-ttu-id="68367-134">Это случайное число, которое генерируется каждый раз, когда запускается служба чата.</span><span class="sxs-lookup"><span data-stu-id="68367-134">This is a random number generated each time a Chat service starts.</span></span> <span data-ttu-id="68367-135">Она используется для различения сеансов в целях идентификации потерянных участников.</span><span class="sxs-lookup"><span data-stu-id="68367-135">It is used to differentiate sessions for the purpose of identifying orphaned participants.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="key"></a><span data-ttu-id="68367-136">Ключ</span><span class="sxs-lookup"><span data-stu-id="68367-136">Key</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="68367-137">Столбец</span><span class="sxs-lookup"><span data-stu-id="68367-137">Column</span></span></th>
<th><span data-ttu-id="68367-138">Описание</span><span class="sxs-lookup"><span data-stu-id="68367-138">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="68367-139">&lt;channelUri, userId, joinedAt&gt;</span><span class="sxs-lookup"><span data-stu-id="68367-139">&lt;channelUri, userId, joinedAt&gt;</span></span></p></td>
<td><p><span data-ttu-id="68367-140">Первичный ключ.</span><span class="sxs-lookup"><span data-stu-id="68367-140">Primary key.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="68367-141">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="68367-141">


</div>

<span> </span>

</div>

</div>

</span></span></div>

