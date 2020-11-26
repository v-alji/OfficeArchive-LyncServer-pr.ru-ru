---
title: 'Lync Server 2013: подчиненный отчет по конференциям'
description: 'Lync Server 2013: подчиненный отчет по конференциям.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Conference Summary Subreport
ms:assetid: 2fc1d2bf-34f5-4093-a6e2-250ec1f1b004
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204779(v=OCS.15)
ms:contentKeyID: 48183742
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0612ce1adb8a6b0fdea5e3bf70b88346f7c08044
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434489"
---
# <a name="conference-summary-subreport-in-lync-server-2013"></a><span data-ttu-id="bdcd0-103">Подчиненный отчет по конференциям в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bdcd0-103">Conference Summary Subreport in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bdcd0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bdcd0-104">

<span> </span></span></span>

<span data-ttu-id="bdcd0-105">_**Тема последнего изменения:** 2012-06-06_</span><span class="sxs-lookup"><span data-stu-id="bdcd0-105">_**Topic Last Modified:** 2012-06-06_</span></span>

<span data-ttu-id="bdcd0-p101">Вложенный сводный отчет о конференции содержит обзор неудачных сеансов конференц-связи. Такие неудачные сеансы дополнительно делятся по типу — сеансы Focus и сеансы MCU.</span><span class="sxs-lookup"><span data-stu-id="bdcd0-p101">The Conference Summary Subreport provides an overall view of failed conference sessions. These failed sessions are further broken down by session type: Focus sessions and MCU sessions.</span></span>

<div>

## <a name="filters"></a><span data-ttu-id="bdcd0-108">Фильтры</span><span class="sxs-lookup"><span data-stu-id="bdcd0-108">Filters</span></span>

<span data-ttu-id="bdcd0-p102">Фильтры позволяют вам возвратить уточненный набор данных или просматривать возвращенные данные различными способами. В следующей таблице перечислены фильтры, которые вы можете использовать во вложенном сводном отчете о конференции.</span><span class="sxs-lookup"><span data-stu-id="bdcd0-p102">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. The following table lists the filters that you can use with the Conference Summary Subreport.</span></span>

### <a name="conference-summary-subreport-filters"></a><span data-ttu-id="bdcd0-111">Фильтры вложенного сводного отчета о конференции</span><span class="sxs-lookup"><span data-stu-id="bdcd0-111">Conference Summary Subreport Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bdcd0-112">Имя</span><span class="sxs-lookup"><span data-stu-id="bdcd0-112">Name</span></span></th>
<th><span data-ttu-id="bdcd0-113">Описание</span><span class="sxs-lookup"><span data-stu-id="bdcd0-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bdcd0-114"><strong>От</strong></span><span class="sxs-lookup"><span data-stu-id="bdcd0-114"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="bdcd0-p103">Начальные дата/время для временного диапазона. Чтобы просмотреть данные по часам, введите начальные дату и время следующим образом:</span><span class="sxs-lookup"><span data-stu-id="bdcd0-p103">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="bdcd0-117">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="bdcd0-117">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="bdcd0-p104">Если вы не вводите начальное время, отчет автоматически начинается с 12:00 AM указанного дня. Чтобы просмотреть данные по дням, просто введите дату:</span><span class="sxs-lookup"><span data-stu-id="bdcd0-p104">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="bdcd0-120">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="bdcd0-120">7/7/2012</span></span></p>
<p><span data-ttu-id="bdcd0-121">Чтобы просмотреть данные за неделю или месяц, введите дату, выпадающую на любое время в рамках недели или месяца, которые вы хотите просмотреть (вам не требуется вводить первый день недели или месяца):</span><span class="sxs-lookup"><span data-stu-id="bdcd0-121">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="bdcd0-122">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="bdcd0-122">7/3/2012</span></span></p>
<p><span data-ttu-id="bdcd0-123">Недели всегда отсчитываются с воскресенья по субботу.</span><span class="sxs-lookup"><span data-stu-id="bdcd0-123">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bdcd0-124"><strong>До</strong></span><span class="sxs-lookup"><span data-stu-id="bdcd0-124"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="bdcd0-p105">Конечные дата/время для временного диапазона. Чтобы просмотреть данные по часам, введите конечные дату и время следующим образом:</span><span class="sxs-lookup"><span data-stu-id="bdcd0-p105">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="bdcd0-127">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="bdcd0-127">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="bdcd0-p106">Если вы не вводите конечное время, отчет автоматически заканчивается в 12:00 AM указанного дня. Чтобы просмотреть данные по дням, просто введите дату:</span><span class="sxs-lookup"><span data-stu-id="bdcd0-p106">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="bdcd0-130">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="bdcd0-130">7/7/2012</span></span></p>
<p><span data-ttu-id="bdcd0-131">Чтобы просмотреть данные за неделю или месяц, введите дату, выпадающую на любое время в рамках недели или месяца, которые вы хотите просмотреть (вам не требуется вводить первый день недели или месяца):</span><span class="sxs-lookup"><span data-stu-id="bdcd0-131">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="bdcd0-132">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="bdcd0-132">7/3/2012</span></span></p>
<p><span data-ttu-id="bdcd0-133">Недели всегда отсчитываются с воскресенья по субботу.</span><span class="sxs-lookup"><span data-stu-id="bdcd0-133">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bdcd0-134"><strong>Пул</strong></span><span class="sxs-lookup"><span data-stu-id="bdcd0-134"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="bdcd0-p107">Полное доменное имя пула регистратора или пограничного сервера. Можно выбрать отдельный пул или нажать <strong>[Все]</strong>, чтобы просмотреть данные для всех пулов. Этот раскрывающийся список автоматически заполняется на основе записей в базе данных.</span><span class="sxs-lookup"><span data-stu-id="bdcd0-p107">Fully qualified domain name (FQDN) of the Registrar pool or Edge Server. You can either select an individual pool or click <strong>[All]</strong> to view data for all the pools. This drop-down list is automatically populated for you based on the records in the database.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics"></a><span data-ttu-id="bdcd0-138">Показатели</span><span class="sxs-lookup"><span data-stu-id="bdcd0-138">Metrics</span></span>

<span data-ttu-id="bdcd0-139">В следующей таблице перечислены сведения, представленные во вложенном сводном отчете о конференции.</span><span class="sxs-lookup"><span data-stu-id="bdcd0-139">The following table lists the information provided in the Conference Summary Subreport.</span></span>

### <a name="conference-summary-subreport-metrics"></a><span data-ttu-id="bdcd0-140">Метрики вложенного сводного отчета о конференции</span><span class="sxs-lookup"><span data-stu-id="bdcd0-140">Conference Summary Subreport Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bdcd0-141">Имя</span><span class="sxs-lookup"><span data-stu-id="bdcd0-141">Name</span></span></th>
<th><span data-ttu-id="bdcd0-142">Поддержка сортировки</span><span class="sxs-lookup"><span data-stu-id="bdcd0-142">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="bdcd0-143">Описание</span><span class="sxs-lookup"><span data-stu-id="bdcd0-143">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bdcd0-144"><strong>Всего конференций</strong></span><span class="sxs-lookup"><span data-stu-id="bdcd0-144"><strong>Total conferences</strong></span></span></p></td>
<td><p><span data-ttu-id="bdcd0-145">Нет</span><span class="sxs-lookup"><span data-stu-id="bdcd0-145">No</span></span></p></td>
<td><p><span data-ttu-id="bdcd0-146">Общее количество проведенных конференций.</span><span class="sxs-lookup"><span data-stu-id="bdcd0-146">Total number of conferences held.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bdcd0-147"><strong>Всего сеансов конференц-связи</strong></span><span class="sxs-lookup"><span data-stu-id="bdcd0-147"><strong>Total conference sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="bdcd0-148">Нет</span><span class="sxs-lookup"><span data-stu-id="bdcd0-148">No</span></span></p></td>
<td><p><span data-ttu-id="bdcd0-p108">Общее количество сеансов конференций. Отдельная конференция может иметь несколько сеансов; например, конференция может включать в себя как сеанс Focus, так и сеанс MCU.</span><span class="sxs-lookup"><span data-stu-id="bdcd0-p108">Total number of conference sessions. A single conference can have multiple sessions; for example, a conference might include both a Focus session and an MCU session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bdcd0-151"><strong>Общая доля сбоев сеансов</strong></span><span class="sxs-lookup"><span data-stu-id="bdcd0-151"><strong>Overall session failure rate</strong></span></span></p></td>
<td><p><span data-ttu-id="bdcd0-152">Нет</span><span class="sxs-lookup"><span data-stu-id="bdcd0-152">No</span></span></p></td>
<td><p><span data-ttu-id="bdcd0-153">Процентное отношение всех конференций, завершившихся со сбоем.</span><span class="sxs-lookup"><span data-stu-id="bdcd0-153">Percentage of all conferences that failed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bdcd0-154"><strong>Сеансы центра конференций</strong></span><span class="sxs-lookup"><span data-stu-id="bdcd0-154"><strong>Focus sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="bdcd0-155">Нет</span><span class="sxs-lookup"><span data-stu-id="bdcd0-155">No</span></span></p></td>
<td><p><span data-ttu-id="bdcd0-156">Общее количество сеансов Focus.</span><span class="sxs-lookup"><span data-stu-id="bdcd0-156">Total number of Focus sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bdcd0-157"><strong>Доля сбоев центра конференций</strong></span><span class="sxs-lookup"><span data-stu-id="bdcd0-157"><strong>Focus failure rate</strong></span></span></p></td>
<td><p><span data-ttu-id="bdcd0-158">Нет</span><span class="sxs-lookup"><span data-stu-id="bdcd0-158">No</span></span></p></td>
<td><p><span data-ttu-id="bdcd0-159">Процентное отношение сеансов Focus, завершившихся со сбоем.</span><span class="sxs-lookup"><span data-stu-id="bdcd0-159">Percentage of Focus sessions that failed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bdcd0-160">Сеансы MCU</span><span class="sxs-lookup"><span data-stu-id="bdcd0-160">MCU sessions</span></span></p></td>
<td><p><span data-ttu-id="bdcd0-161">Нет</span><span class="sxs-lookup"><span data-stu-id="bdcd0-161">No</span></span></p></td>
<td><p><span data-ttu-id="bdcd0-162">Общее количество сеансов MCU.</span><span class="sxs-lookup"><span data-stu-id="bdcd0-162">Total number of MCU sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bdcd0-163"><strong>Доля сбоев MCU</strong></span><span class="sxs-lookup"><span data-stu-id="bdcd0-163"><strong>MCU failure rate</strong></span></span></p></td>
<td><p><span data-ttu-id="bdcd0-164">Нет</span><span class="sxs-lookup"><span data-stu-id="bdcd0-164">No</span></span></p></td>
<td><p><span data-ttu-id="bdcd0-165">Процентное отношение сеансов MCU, завершившихся со сбоем.</span><span class="sxs-lookup"><span data-stu-id="bdcd0-165">Percentage of MCU sessions that failed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bdcd0-166"><strong>Сеансы MCU по модальности</strong></span><span class="sxs-lookup"><span data-stu-id="bdcd0-166"><strong>MCU sessions by modality</strong></span></span></p></td>
<td><p><span data-ttu-id="bdcd0-167">Нет</span><span class="sxs-lookup"><span data-stu-id="bdcd0-167">No</span></span></p></td>
<td><p><span data-ttu-id="bdcd0-168">Общее количество сеансов MCU, сгруппированных по модальности (например, конференции с обменом мгновенными сообщениями).</span><span class="sxs-lookup"><span data-stu-id="bdcd0-168">Total number of MCU sessions, grouped by modality (for example, IM conferencing).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bdcd0-169"><strong>Доля сбоев по модальности</strong></span><span class="sxs-lookup"><span data-stu-id="bdcd0-169"><strong>Failure rate by modality</strong></span></span></p></td>
<td><p><span data-ttu-id="bdcd0-170">Нет</span><span class="sxs-lookup"><span data-stu-id="bdcd0-170">No</span></span></p></td>
<td><p><span data-ttu-id="bdcd0-171">Процентное отношение неудачных сеансов MCU, сгруппированных по модальности (например, конференции с обменом мгновенными сообщениями).</span><span class="sxs-lookup"><span data-stu-id="bdcd0-171">Percentage of MCU sessions that failed, grouped by modality (for example, IM conferencing).</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="bdcd0-172">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bdcd0-172">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

