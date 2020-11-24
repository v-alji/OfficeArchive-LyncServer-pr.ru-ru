---
title: 'Lync Server 2013: таблица PurgeSettings (QoE)'
description: 'Lync Server 2013: PurgeSettings Table (QoE).'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: PurgeSettings table (QoE)
ms:assetid: 31b85d1c-3f32-4f67-94bf-9389cdd282c5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204788(v=OCS.15)
ms:contentKeyID: 48183777
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d515d799a7cc442dc6d34f2ece1a968de51cdad6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399016"
---
# <a name="purgesettings-table-qoe-in-lync-server-2013"></a><span data-ttu-id="a0627-103">PurgeSettings Table (QoE) в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a0627-103">PurgeSettings table (QoE) in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a0627-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a0627-104">

<span> </span></span></span>

<span data-ttu-id="a0627-105">_**Тема последнего изменения:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="a0627-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="a0627-106">В таблице PurgeSettings содержатся сведения о том, что (и когда) устаревшие записи качества обслуживания будут автоматически удалены из базы данных QoE.</span><span class="sxs-lookup"><span data-stu-id="a0627-106">The PurgeSettings table contains information that specifies if (and when) outdated Quality of Experience records will automatically be deleted from the QoE database.</span></span> <span data-ttu-id="a0627-107">Обратите внимание, что в командной консоли Microsoft Lync Server 2013 также можно получить сведения об очистке, выполнив следующую команду:</span><span class="sxs-lookup"><span data-stu-id="a0627-107">Note that purging-related information can also be obtained from within the Microsoft Lync Server 2013 Management Shell by running the following command:</span></span>

    Get-CsQoEConfiguration

<span data-ttu-id="a0627-108">Эта таблица введена в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a0627-108">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a0627-109"><strong>Столбец</strong></span><span class="sxs-lookup"><span data-stu-id="a0627-109"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="a0627-110"><strong>Тип данных</strong></span><span class="sxs-lookup"><span data-stu-id="a0627-110"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="a0627-111"><strong>Ключ/индекс</strong></span><span class="sxs-lookup"><span data-stu-id="a0627-111"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="a0627-112"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="a0627-112"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a0627-113"><strong>ID</strong></span><span class="sxs-lookup"><span data-stu-id="a0627-113"><strong>ID</strong></span></span></p></td>
<td><p><span data-ttu-id="a0627-114">целое</span><span class="sxs-lookup"><span data-stu-id="a0627-114">int</span></span></p></td>
<td><p><span data-ttu-id="a0627-115">Primary</span><span class="sxs-lookup"><span data-stu-id="a0627-115">Primary</span></span></p></td>
<td><p><span data-ttu-id="a0627-116">Уникальный идентификатор коллекции параметров очистки QoE.</span><span class="sxs-lookup"><span data-stu-id="a0627-116">Unique identifier for the collection of QoE purge settings.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0627-117"><strong>EnablePurge</strong></span><span class="sxs-lookup"><span data-stu-id="a0627-117"><strong>EnablePurge</strong></span></span></p></td>
<td><p><span data-ttu-id="a0627-118">бит</span><span class="sxs-lookup"><span data-stu-id="a0627-118">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="a0627-119">Если установлено значение true (1), Microsoft Lync Server 2013 будет периодически очищать устаревшие записи из базы данных QoE.</span><span class="sxs-lookup"><span data-stu-id="a0627-119">When set to True (1) Microsoft Lync Server 2013 will periodically purge outdated records from the QoE database.</span></span> <span data-ttu-id="a0627-120">Очистка будет выполняться каждый день в томе, указанном в параметре PurgeHour.</span><span class="sxs-lookup"><span data-stu-id="a0627-120">Purging will take place each day at the tome specified by the PurgeHour setting.</span></span> <span data-ttu-id="a0627-121">Если для этого свойства задано значение false (0), записи не будут автоматически удалены из базы данных.</span><span class="sxs-lookup"><span data-stu-id="a0627-121">If set to False (0) then records will not be automatically purged from the database.</span></span> <span data-ttu-id="a0627-122">По умолчанию используется значение True.</span><span class="sxs-lookup"><span data-stu-id="a0627-122">The default value is True.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0627-123"><strong>KeepQoEDataForDays</strong></span><span class="sxs-lookup"><span data-stu-id="a0627-123"><strong>KeepQoEDataForDays</strong></span></span></p></td>
<td><p><span data-ttu-id="a0627-124">целое</span><span class="sxs-lookup"><span data-stu-id="a0627-124">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="a0627-125">Указывает возраст QoE записей (в днях), которые будут очищены из базы данных: Если включена очистка, QoE записи, возраст которых превышает это значение, будут удалены из базы данных.</span><span class="sxs-lookup"><span data-stu-id="a0627-125">Specifies the age of QoE records (in days) that will be purged from the database: if purging is enabled, QoE records older than this value will be removed from the database.</span></span> <span data-ttu-id="a0627-126">Значение по умолчанию — 60 дней.</span><span class="sxs-lookup"><span data-stu-id="a0627-126">The default value is 60 days.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0627-127"><strong>PurgeHour</strong></span><span class="sxs-lookup"><span data-stu-id="a0627-127"><strong>PurgeHour</strong></span></span></p></td>
<td><p><span data-ttu-id="a0627-128">целое</span><span class="sxs-lookup"><span data-stu-id="a0627-128">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="a0627-129">Указывает местное время суток, когда будет выполняться очистка базы данных.</span><span class="sxs-lookup"><span data-stu-id="a0627-129">Specifies the local time of day when database purging will take place.</span></span> <span data-ttu-id="a0627-130">Время суток задается в 24-часовом формате (0 соответствует полуночи (00:00), а 23 — 23:00 часам вечера).</span><span class="sxs-lookup"><span data-stu-id="a0627-130">The time of day is specified using a 24-hour clock, with 0 representing midnight (12:00 AM) and 23 representing 11:00 PM.</span></span> <span data-ttu-id="a0627-131">Обратите внимание, что вы можете указать только час дня: значение 10 (указывает на 10:00 AM) разрешено, но значение 10:30 от 10,5 (это означает 10:30 AM) не разрешено.</span><span class="sxs-lookup"><span data-stu-id="a0627-131">Note that you can only specify the hour of the day: a value of 10 (indicating 10:00 AM) is allowed, but a value of 10:30 of 10.5 (indicating 10:30 AM) is not allowed.</span></span> <span data-ttu-id="a0627-132">Значение по умолчанию — 1 (1:00 AM).</span><span class="sxs-lookup"><span data-stu-id="a0627-132">The default value is 1 (1:00 AM).</span></span> <span data-ttu-id="a0627-133">Указывает местное время суток, когда будет выполняться очистка базы данных.</span><span class="sxs-lookup"><span data-stu-id="a0627-133">Specifies the local time of day when database purging will take place.</span></span> <span data-ttu-id="a0627-134">Время суток задается в 24-часовом формате (0 соответствует полуночи (00:00), а 23 — 23:00 часам вечера).</span><span class="sxs-lookup"><span data-stu-id="a0627-134">The time of day is specified using a 24-hour clock, with 0 representing midnight (12:00 AM) and 23 representing 11:00 PM.</span></span> <span data-ttu-id="a0627-135">Обратите внимание, что вы можете указать только час дня: значение 10 (указывает на 10:00 AM) разрешено, но значение 10:30 от 10,5 (это означает 10:30 AM) не разрешено.</span><span class="sxs-lookup"><span data-stu-id="a0627-135">Note that you can only specify the hour of the day: a value of 10 (indicating 10:00 AM) is allowed, but a value of 10:30 of 10.5 (indicating 10:30 AM) is not allowed.</span></span> <span data-ttu-id="a0627-136">Значение по умолчанию — 1 (1:00 AM).</span><span class="sxs-lookup"><span data-stu-id="a0627-136">The default value is 1 (1:00 AM).</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="a0627-137">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a0627-137">


</div>

<span> </span>

</div>

</div>

</span></span></div>

