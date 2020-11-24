---
title: 'Lync Server 2013: таблица PurgeSettings'
description: 'Таблица Lync Server 2013: PurgeSettings.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: PurgeSettings table
ms:assetid: 9ff2c8fc-4ae8-4f22-96a8-1f4d5eecbf2d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205121(v=OCS.15)
ms:contentKeyID: 48184932
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1ec2d1508d8362988bddbab2fe7303a23a8ee2d8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399013"
---
# <a name="purgesettings-table-in-lync-server-2013"></a><span data-ttu-id="6a376-103">Таблица PurgeSettings в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6a376-103">PurgeSettings table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6a376-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6a376-104">

<span> </span></span></span>

<span data-ttu-id="6a376-105">_**Тема последнего изменения:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="6a376-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="6a376-106">В таблице PurgeSettings содержатся сведения о том, что (и когда) устаревшая запись о вызовах будет автоматически удалена из базы данных CDR.</span><span class="sxs-lookup"><span data-stu-id="6a376-106">The PurgeSettings table contains information that specifies if (and when) outdated call detail records will automatically be deleted from the CDR database.</span></span> <span data-ttu-id="6a376-107">Обратите внимание, что в командной консоли Microsoft Lync Server 2013 также можно получить сведения об очистке, выполнив следующую команду:</span><span class="sxs-lookup"><span data-stu-id="6a376-107">Note that purging-related information can also be obtained from within the Microsoft Lync Server 2013 Management Shell by running the following command:</span></span>

    Get-CsCdrConfiguration

<span data-ttu-id="6a376-108">Администраторы должны рассматривать таблицу PurgeSettings как доступную только для чтения: изменения в параметрах очистки сведений о вызовах следует вносить только с помощью командлетов [New-CsCdrConfiguration](https://docs.microsoft.com/powershell/module/skype/New-CsCdrConfiguration) или [Set-CsCdrConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsCdrConfiguration) .</span><span class="sxs-lookup"><span data-stu-id="6a376-108">Administrators should treat the PurgeSettings table as read-only: changes to the call detail purge settings should only be made using the [New-CsCdrConfiguration](https://docs.microsoft.com/powershell/module/skype/New-CsCdrConfiguration) or [Set-CsCdrConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsCdrConfiguration) cmdlets.</span></span>

<span data-ttu-id="6a376-109">Эта таблица введена в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6a376-109">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6a376-110">Столбец</span><span class="sxs-lookup"><span data-stu-id="6a376-110">Column</span></span></th>
<th><span data-ttu-id="6a376-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="6a376-111">Data Type</span></span></th>
<th><span data-ttu-id="6a376-112">Ключ/индекс</span><span class="sxs-lookup"><span data-stu-id="6a376-112">Key/Index</span></span></th>
<th><span data-ttu-id="6a376-113">Сведения</span><span class="sxs-lookup"><span data-stu-id="6a376-113">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6a376-114"><strong>Номер</strong></span><span class="sxs-lookup"><span data-stu-id="6a376-114"><strong>Id</strong></span></span></p></td>
<td><p><span data-ttu-id="6a376-115">целое</span><span class="sxs-lookup"><span data-stu-id="6a376-115">int</span></span></p></td>
<td><p><span data-ttu-id="6a376-116">Primary</span><span class="sxs-lookup"><span data-stu-id="6a376-116">Primary</span></span></p></td>
<td><p><span data-ttu-id="6a376-117">Уникальный идентификатор коллекции параметров очистки CDR.</span><span class="sxs-lookup"><span data-stu-id="6a376-117">Unique identifier for the collection of CDR purge settings.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a376-118"><strong>EnablePurge</strong></span><span class="sxs-lookup"><span data-stu-id="6a376-118"><strong>EnablePurge</strong></span></span></p></td>
<td><p><span data-ttu-id="6a376-119">бит</span><span class="sxs-lookup"><span data-stu-id="6a376-119">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6a376-120">Если установлено значение true (1), Microsoft Lync Server 2013 будет периодически очищать устаревшие записи из базы данных CDR.</span><span class="sxs-lookup"><span data-stu-id="6a376-120">When set to True (1) Microsoft Lync Server 2013 will periodically purge outdated records from the CDR database.</span></span> <span data-ttu-id="6a376-121">Очистка будет выполняться каждый день в томе, указанном в параметре PurgeHour.</span><span class="sxs-lookup"><span data-stu-id="6a376-121">Purging will take place each day at the tome specified by the PurgeHour setting.</span></span> <span data-ttu-id="6a376-122">Если для этого свойства задано значение false (0), записи не будут автоматически удалены из базы данных.</span><span class="sxs-lookup"><span data-stu-id="6a376-122">If set to False (0) then records will not be automatically purged from the database.</span></span> <span data-ttu-id="6a376-123">По умолчанию используется значение True.</span><span class="sxs-lookup"><span data-stu-id="6a376-123">The default value is True.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a376-124"><strong>KeepCallDetailForDays</strong></span><span class="sxs-lookup"><span data-stu-id="6a376-124"><strong>KeepCallDetailForDays</strong></span></span></p></td>
<td><p><span data-ttu-id="6a376-125">целое</span><span class="sxs-lookup"><span data-stu-id="6a376-125">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6a376-126">Указывает возраст CDR записей (в днях), которые будут очищены из базы данных: Если включена очистка, CDR записи, возраст которых превышает это значение, будут удалены из базы данных.</span><span class="sxs-lookup"><span data-stu-id="6a376-126">Specifies the age of CDR records (in days) that will be purged from the database: if purging is enabled, CDR records older than this value will be removed from the database.</span></span> <span data-ttu-id="6a376-127">Значение по умолчанию — 60 дней.</span><span class="sxs-lookup"><span data-stu-id="6a376-127">The default value is 60 days.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a376-128"><strong>KeepErrorReportForDays</strong></span><span class="sxs-lookup"><span data-stu-id="6a376-128"><strong>KeepErrorReportForDays</strong></span></span></p></td>
<td><p><span data-ttu-id="6a376-129">целое</span><span class="sxs-lookup"><span data-stu-id="6a376-129">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6a376-130">Указывает возраст записей отчета об ошибках (в днях), которые будут очищены из базы данных: Если включена очистка, записи отчета об ошибках старше этого значения будут удалены из базы данных.</span><span class="sxs-lookup"><span data-stu-id="6a376-130">Specifies the age of error report records (in days) that will be purged from the database: if purging is enabled, error report records older than this value will be removed from the database.</span></span> <span data-ttu-id="6a376-131">Значение по умолчанию — 60 дней.</span><span class="sxs-lookup"><span data-stu-id="6a376-131">The default value is 60 days.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a376-132"><strong>PurgeHour</strong></span><span class="sxs-lookup"><span data-stu-id="6a376-132"><strong>PurgeHour</strong></span></span></p></td>
<td><p><span data-ttu-id="6a376-133">целое</span><span class="sxs-lookup"><span data-stu-id="6a376-133">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6a376-134">Указывает местное время суток, когда будет выполняться очистка базы данных.</span><span class="sxs-lookup"><span data-stu-id="6a376-134">Specifies the local time of day when database purging will take place.</span></span> <span data-ttu-id="6a376-135">Время суток задается в 24-часовом формате (0 соответствует полуночи (00:00), а 23 — 23:00 часам вечера).</span><span class="sxs-lookup"><span data-stu-id="6a376-135">The time of day is specified using a 24-hour clock, with 0 representing midnight (12:00 AM) and 23 representing 11:00 PM.</span></span> <span data-ttu-id="6a376-136">Обратите внимание, что вы можете указать только час дня: значение 10 (указывает на 10:00 AM) разрешено, но значение 10:30 от 10,5 (это означает 10:30 AM) не разрешено.</span><span class="sxs-lookup"><span data-stu-id="6a376-136">Note that you can only specify the hour of the day: a value of 10 (indicating 10:00 AM) is allowed, but a value of 10:30 of 10.5 (indicating 10:30 AM) is not allowed.</span></span> <span data-ttu-id="6a376-137">Значение по умолчанию — 2 часа утра (02:00).</span><span class="sxs-lookup"><span data-stu-id="6a376-137">The default value is 2 (2:00 AM).</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="6a376-138">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6a376-138">


</div>

<span> </span>

</div>

</div>

</span></span></div>

