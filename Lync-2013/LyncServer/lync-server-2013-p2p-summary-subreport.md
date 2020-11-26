---
title: 'Сводный отчет о Lync Server 2013: P2P'
description: 'Сводный отчет Lync Server 2013: P2P.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: P2P Summary Subreport
ms:assetid: fc36185a-3cc5-4167-8c93-8a755fa75ac7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205416(v=OCS.15)
ms:contentKeyID: 48185950
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: eda51e76c4ed7b62535a2a2e4ab52982aa6381f3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424704"
---
# <a name="p2p-summary-subreport-in-lync-server-2013"></a><span data-ttu-id="279d3-103">Сводный отчет P2P в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="279d3-103">P2P Summary Subreport in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="279d3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="279d3-104">

<span> </span></span></span>

<span data-ttu-id="279d3-105">_**Тема последнего изменения:** 2012-10-21_</span><span class="sxs-lookup"><span data-stu-id="279d3-105">_**Topic Last Modified:** 2012-10-21_</span></span>

<span data-ttu-id="279d3-106">Вложенный сводный отчет по одноранговым подключениям содержит общий обзор одноранговых сеансов связи, завершившихся с ошибками.</span><span class="sxs-lookup"><span data-stu-id="279d3-106">The P2P Summary Subreport provides an overall view of your failed peer-to-peer communication sessions.</span></span>

<div>

## <a name="filters"></a><span data-ttu-id="279d3-107">Фильтры</span><span class="sxs-lookup"><span data-stu-id="279d3-107">Filters</span></span>

<span data-ttu-id="279d3-p101">Фильтры позволяют возвращать более точный набор данных или различными способами просматривать возвращенные данные. В следующей таблице представлены фильтры, которые вы можете использовать со сводным вложенным отчетом P2P.</span><span class="sxs-lookup"><span data-stu-id="279d3-p101">Filters provide a way for you to return a more finely targeted set of data or to view the returned data in different ways. The following table lists the filters that you can use with the P2P Summary Subreport.</span></span>

### <a name="p2p-summary-subreport-filters"></a><span data-ttu-id="279d3-110">Фильтры вложенного сводного отчета по одноранговым подключениям</span><span class="sxs-lookup"><span data-stu-id="279d3-110">P2P Summary Subreport Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="279d3-111">Имя</span><span class="sxs-lookup"><span data-stu-id="279d3-111">Name</span></span></th>
<th><span data-ttu-id="279d3-112">Описание</span><span class="sxs-lookup"><span data-stu-id="279d3-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="279d3-113"><strong>От</strong></span><span class="sxs-lookup"><span data-stu-id="279d3-113"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="279d3-p102">Начальная дата и начальное время для диапазона времени. Чтобы просмотреть данные по часам, введите начальную дату и начальное время в следующем формате:</span><span class="sxs-lookup"><span data-stu-id="279d3-p102">Start date and time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="279d3-116">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="279d3-116">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="279d3-p103">Если вы не вводите начальное время, отчет автоматически начинается с 12:00 AM указанного дня. Чтобы просмотреть данные по дням, просто введите дату:</span><span class="sxs-lookup"><span data-stu-id="279d3-p103">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="279d3-119">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="279d3-119">7/7/2012</span></span></p>
<p><span data-ttu-id="279d3-120">Чтобы просмотреть данные за неделю или месяц, введите дату, выпадающую на любое время в рамках недели или месяца, которые вы хотите просмотреть (вам не требуется вводить первый день недели или месяца):</span><span class="sxs-lookup"><span data-stu-id="279d3-120">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="279d3-121">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="279d3-121">7/3/2012</span></span></p>
<p><span data-ttu-id="279d3-122">Недели всегда отсчитываются с воскресенья по субботу.</span><span class="sxs-lookup"><span data-stu-id="279d3-122">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="279d3-123"><strong>До</strong></span><span class="sxs-lookup"><span data-stu-id="279d3-123"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="279d3-p104">Конечная дата и конечное время для диапазона времени. Чтобы просмотреть данные по часам, введите конечную дату и конечное время в следующем формате:</span><span class="sxs-lookup"><span data-stu-id="279d3-p104">End date and time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="279d3-126">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="279d3-126">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="279d3-p105">Если вы не вводите конечное время, отчет автоматически заканчивается в 12:00 AM указанного дня. Чтобы просмотреть данные по дням, просто введите дату:</span><span class="sxs-lookup"><span data-stu-id="279d3-p105">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="279d3-129">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="279d3-129">7/7/2012</span></span></p>
<p><span data-ttu-id="279d3-130">Чтобы просмотреть данные за неделю или месяц, введите дату, выпадающую на любое время в рамках недели или месяца, которые вы хотите просмотреть (вам не требуется вводить первый день недели или месяца):</span><span class="sxs-lookup"><span data-stu-id="279d3-130">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="279d3-131">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="279d3-131">7/3/2012</span></span></p>
<p><span data-ttu-id="279d3-132">Недели всегда отсчитываются с воскресенья по субботу.</span><span class="sxs-lookup"><span data-stu-id="279d3-132">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="279d3-133"><strong>Пул</strong></span><span class="sxs-lookup"><span data-stu-id="279d3-133"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="279d3-p106">Полное доменное имя пула регистратора или пограничного сервера. Можно выбрать отдельный пул или нажать <strong>[Все]</strong>, чтобы просмотреть данные для всех пулов. Этот раскрывающийся список автоматически заполняется на основе записей в базе данных.</span><span class="sxs-lookup"><span data-stu-id="279d3-p106">Fully qualified domain name (FQDN) of the Registrar pool or Edge Server. You can either select an individual pool or click <strong>[All]</strong> to view data for all the pools. This drop-down list is automatically populated for you based on the records in the database.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics"></a><span data-ttu-id="279d3-137">Показатели</span><span class="sxs-lookup"><span data-stu-id="279d3-137">Metrics</span></span>

<span data-ttu-id="279d3-138">Следующая таблица содержит сведения, приведенные во вложенном сводном отчете по одноранговым подключениям.</span><span class="sxs-lookup"><span data-stu-id="279d3-138">The following table lists the information provided in the P2P Summary Subreport.</span></span>

### <a name="p2p-summary-subreport-metrics"></a><span data-ttu-id="279d3-139">Метрики вложенного сводного отчета по одноранговым подключениям</span><span class="sxs-lookup"><span data-stu-id="279d3-139">P2P Summary Subreport Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="279d3-140">Имя</span><span class="sxs-lookup"><span data-stu-id="279d3-140">Name</span></span></th>
<th><span data-ttu-id="279d3-141">Поддержка сортировки</span><span class="sxs-lookup"><span data-stu-id="279d3-141">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="279d3-142">Описание</span><span class="sxs-lookup"><span data-stu-id="279d3-142">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="279d3-143"><strong>Всего сеансов</strong></span><span class="sxs-lookup"><span data-stu-id="279d3-143"><strong>Total sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="279d3-144">Нет</span><span class="sxs-lookup"><span data-stu-id="279d3-144">No</span></span></p></td>
<td><p><span data-ttu-id="279d3-145">Общее число сеансов, включая успешные и завершившиеся сбоем (как ожидаемые, так и непредвиденные сбои) и сеансы без категорий.</span><span class="sxs-lookup"><span data-stu-id="279d3-145">Total number of sessions, including successful sessions, failed sessions (both expected failures and unexpected failures), and uncategorized sessions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="279d3-146"><strong>Доля сбоев</strong></span><span class="sxs-lookup"><span data-stu-id="279d3-146"><strong>Failure rate</strong></span></span></p></td>
<td><p><span data-ttu-id="279d3-147">Нет</span><span class="sxs-lookup"><span data-stu-id="279d3-147">No</span></span></p></td>
<td><p><span data-ttu-id="279d3-148">Процент неудачных одноранговых сеансов.</span><span class="sxs-lookup"><span data-stu-id="279d3-148">Percentage of peer-to-peer sessions that failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="279d3-149"><strong>Сеансы по модальности</strong></span><span class="sxs-lookup"><span data-stu-id="279d3-149"><strong>Sessions by Modality</strong></span></span></p></td>
<td><p><span data-ttu-id="279d3-150">Нет</span><span class="sxs-lookup"><span data-stu-id="279d3-150">No</span></span></p></td>
<td><p><span data-ttu-id="279d3-151">Общее число сеансов, сгруппированных по модальности (например, обмен мгновенными сообщениями).</span><span class="sxs-lookup"><span data-stu-id="279d3-151">Total number of sessions grouped by modality (for example, instant messaging).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="279d3-152"><strong>Доля сбоев по модальности</strong></span><span class="sxs-lookup"><span data-stu-id="279d3-152"><strong>Failure rate by modality</strong></span></span></p></td>
<td><p><span data-ttu-id="279d3-153">Нет</span><span class="sxs-lookup"><span data-stu-id="279d3-153">No</span></span></p></td>
<td><p><span data-ttu-id="279d3-154">Общее число неудачных сеансов, сгруппированных по модальности (например, обмен мгновенными сообщениями).</span><span class="sxs-lookup"><span data-stu-id="279d3-154">Total number of failed sessions grouped by modality (for example, instant messaging).</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="279d3-155">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="279d3-155">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

