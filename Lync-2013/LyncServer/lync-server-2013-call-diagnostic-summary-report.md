---
title: 'Lync Server 2013: сводный отчет о звонке'
description: 'Lync Server 2013: сводный отчет о вызове.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Call Diagnostic Summary Report
ms:assetid: 9091de56-13e6-440e-9353-f57c10c906fe
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615016(v=OCS.15)
ms:contentKeyID: 48184789
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b444a176c06974a9eb9827006e078c17b54047a3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49397996"
---
# <a name="call-diagnostic-summary-report-in-lync-server-2013"></a><span data-ttu-id="ae16f-103">Сводный отчет о звонке в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ae16f-103">Call Diagnostic Summary Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ae16f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ae16f-104">

<span> </span></span></span>

<span data-ttu-id="ae16f-105">_**Тема последнего изменения:** 2012-06-06_</span><span class="sxs-lookup"><span data-stu-id="ae16f-105">_**Topic Last Modified:** 2012-06-06_</span></span>

<span data-ttu-id="ae16f-p101">Сводный диагностический отчет по вызовам предоставляет полную сводку по неудачным одноранговым сеансам и сеансам конференц-связи. Этот отчет показывает общее количество сбоев для обоих типов сеансов, и далее разбивает сведения о сбое по следующим типам модальности сеанса:</span><span class="sxs-lookup"><span data-stu-id="ae16f-p101">The Call Diagnostic Summary Report provides an overall look at failed peer-to-peer and conferencing sessions. The report shows the overall failure rate for both types of sessions, and further breaks the failure information down by session modality type:</span></span>

  - <span data-ttu-id="ae16f-108">Обмен мгновенными сообщениями</span><span class="sxs-lookup"><span data-stu-id="ae16f-108">Instant messaging</span></span>

  - <span data-ttu-id="ae16f-109">Общий доступ к приложениям</span><span class="sxs-lookup"><span data-stu-id="ae16f-109">Application sharing</span></span>

  - <span data-ttu-id="ae16f-110">Передача файлов</span><span class="sxs-lookup"><span data-stu-id="ae16f-110">File transfer</span></span>

  - <span data-ttu-id="ae16f-111">Аудио</span><span class="sxs-lookup"><span data-stu-id="ae16f-111">Audio</span></span>

  - <span data-ttu-id="ae16f-112">Видео</span><span class="sxs-lookup"><span data-stu-id="ae16f-112">Video</span></span>

<div>

## <a name="accessing-the-call-diagnostic-summary-report"></a><span data-ttu-id="ae16f-113">Доступ к сводному диагностическому отчету по вызовам</span><span class="sxs-lookup"><span data-stu-id="ae16f-113">Accessing the Call Diagnostic Summary Report</span></span>

<span data-ttu-id="ae16f-114">The Call Diagnostic Summary Report is accessed from the Monitoring Reports Home page.</span><span class="sxs-lookup"><span data-stu-id="ae16f-114">The Call Diagnostic Summary Report is accessed from the Monitoring Reports Home page.</span></span> <span data-ttu-id="ae16f-115">Из сводного отчета "Диагностика звонков" вы можете получить доступ к [диагностическим отчету о действиях одноранговых групп в Lync Server 2013](lync-server-2013-peer-to-peer-activity-diagnostic-report.md) , щелкнув метрику частота сбоя в разделе "одноранговый сеанс" в сводном отчете.</span><span class="sxs-lookup"><span data-stu-id="ae16f-115">From the Call Diagnostic Summary Report you can access the [Peer-to-Peer Activity Diagnostic Report in Lync Server 2013](lync-server-2013-peer-to-peer-activity-diagnostic-report.md) by clicking the Failure rate metric under the Peer-to-Peer Session Summary section of the report.</span></span> <span data-ttu-id="ae16f-116">Вы также можете получить доступ к [диагностическим отчетам на Конференции в Lync Server 2013](lync-server-2013-conference-diagnostic-report.md) , щелкнув одну из следующих метрик конференции:</span><span class="sxs-lookup"><span data-stu-id="ae16f-116">You can also access the [Conference Diagnostic Report in Lync Server 2013](lync-server-2013-conference-diagnostic-report.md) by clicking any of the following conference metrics:</span></span>

  - <span data-ttu-id="ae16f-117">Общее количество неудачных сеансов</span><span class="sxs-lookup"><span data-stu-id="ae16f-117">Overall session failure rate</span></span>

  - <span data-ttu-id="ae16f-118">Неудачные сеансы с центром</span><span class="sxs-lookup"><span data-stu-id="ae16f-118">Focus failure rate</span></span>

  - <span data-ttu-id="ae16f-119">Неудачные сеансы с MCU</span><span class="sxs-lookup"><span data-stu-id="ae16f-119">MCU failure rate</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-call-diagnostic-summary-report"></a><span data-ttu-id="ae16f-120">Эффективное использование сводного диагностического отчета по вызовам</span><span class="sxs-lookup"><span data-stu-id="ae16f-120">Making the Best Use of the Call Diagnostic Summary Report</span></span>

<span data-ttu-id="ae16f-121">Сводный отчет о звонке содержит графики, которые сравнивают тарифы на ошибки для различных модальностей, используемых в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ae16f-121">The Call Diagnostic Summary Report includes graphs that compare failure rates for the various modalities used in Microsoft Lync Server 2013.</span></span> <span data-ttu-id="ae16f-122">Столбцы на этих графах фактически Hotlinks; Например, если щелкнуть столбец "мгновенные сообщения" для одноранговых сеансов, вы узнаете, как перейти к экземпляру [диагностического отчета о действиях одноранговых участников в Lync Server 2013](lync-server-2013-peer-to-peer-activity-diagnostic-report.md), который содержит дополнительные сведения о всех сеансах обмена мгновенными сообщениями, включенных в сводный отчет о звонке.</span><span class="sxs-lookup"><span data-stu-id="ae16f-122">The columns in these graphs are actually hotlinks; for example, if you click the Instant messaging column for peer-to-peer sessions, you'll drill down to an instance of the [Peer-to-Peer Activity Diagnostic Report in Lync Server 2013](lync-server-2013-peer-to-peer-activity-diagnostic-report.md), a report that provides additional details about all the instant messaging sessions included in the Call Diagnostic Summary Report.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="ae16f-123">Фильтры</span><span class="sxs-lookup"><span data-stu-id="ae16f-123">Filters</span></span>

<span data-ttu-id="ae16f-p104">Фильтры позволяют получать более адресный набор данных или просматривать полученные данные разными способами. Например, в сводном диагностическом отчете по вызовам можно выполнять фильтрацию по пулу регистратора или по пограничному серверу, использовавшемуся в сеансе. Можно также выбрать способ группирования данных. В этом случае вызовы группируются по часу, дню, неделе или месяцу.</span><span class="sxs-lookup"><span data-stu-id="ae16f-p104">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. For example, the Call Diagnostic Summary Report enables you to filter on such things as the Registrar pool or Edge Server used in the session. You can also choose how data should be grouped. In this case, calls are grouped by hour, day, week, or month.</span></span>

<span data-ttu-id="ae16f-128">В следующей таблице перечислены фильтры, которые можно использовать в сводном диагностическом отчете по вызовам.</span><span class="sxs-lookup"><span data-stu-id="ae16f-128">The following table lists the filters that you can use with the Call Diagnostic Summary Report.</span></span>

### <a name="call-diagnostic-summary-report-filters"></a><span data-ttu-id="ae16f-129">Фильтры сводного диагностического отчета по вызовам</span><span class="sxs-lookup"><span data-stu-id="ae16f-129">Call Diagnostic Summary Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ae16f-130">Имя</span><span class="sxs-lookup"><span data-stu-id="ae16f-130">Name</span></span></th>
<th><span data-ttu-id="ae16f-131">Описание</span><span class="sxs-lookup"><span data-stu-id="ae16f-131">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ae16f-132"><strong>От</strong></span><span class="sxs-lookup"><span data-stu-id="ae16f-132"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="ae16f-p105">Начальные дата/время для временного диапазона. Чтобы просмотреть данные по часам, введите начальные дату и время следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ae16f-p105">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="ae16f-135">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="ae16f-135">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="ae16f-p106">Если вы не вводите начальное время, отчет автоматически начинается с 12:00 AM указанного дня. Чтобы просмотреть данные по дням, просто введите дату:</span><span class="sxs-lookup"><span data-stu-id="ae16f-p106">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="ae16f-138">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="ae16f-138">7/7/2012</span></span></p>
<p><span data-ttu-id="ae16f-139">Чтобы просмотреть данные за неделю или месяц, введите дату, выпадающую на любое время в рамках недели или месяца, которые вы хотите просмотреть (вам не требуется вводить первый день недели или месяца):</span><span class="sxs-lookup"><span data-stu-id="ae16f-139">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="ae16f-140">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="ae16f-140">7/3/2012</span></span></p>
<p><span data-ttu-id="ae16f-141">Недели всегда отсчитываются с воскресенья по субботу.</span><span class="sxs-lookup"><span data-stu-id="ae16f-141">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae16f-142"><strong>До</strong></span><span class="sxs-lookup"><span data-stu-id="ae16f-142"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="ae16f-p107">Конечные дата/время для временного диапазона. Чтобы просмотреть данные по часам, введите конечные дату и время следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ae16f-p107">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="ae16f-145">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="ae16f-145">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="ae16f-p108">Если вы не вводите конечное время, отчет автоматически заканчивается в 12:00 AM указанного дня. Чтобы просмотреть данные по дням, просто введите дату:</span><span class="sxs-lookup"><span data-stu-id="ae16f-p108">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="ae16f-148">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="ae16f-148">7/7/2012</span></span></p>
<p><span data-ttu-id="ae16f-149">Чтобы просмотреть данные за неделю или месяц, введите дату, выпадающую на любое время в рамках недели или месяца, которые вы хотите просмотреть (вам не требуется вводить первый день недели или месяца):</span><span class="sxs-lookup"><span data-stu-id="ae16f-149">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="ae16f-150">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="ae16f-150">7/3/2012</span></span></p>
<p><span data-ttu-id="ae16f-151">Недели всегда отсчитываются с воскресенья по субботу.</span><span class="sxs-lookup"><span data-stu-id="ae16f-151">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae16f-152"><strong>Интервал</strong></span><span class="sxs-lookup"><span data-stu-id="ae16f-152"><strong>Interval</strong></span></span></p></td>
<td><p><span data-ttu-id="ae16f-p109">Временной интервал. Выберите одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="ae16f-p109">Time interval. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="ae16f-155">Ежечасно (можно отобразить не более 25 часов)</span><span class="sxs-lookup"><span data-stu-id="ae16f-155">Hourly (a maximum of 25 hours can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="ae16f-156">Ежедневно (можно отобразить не более 31 дня)</span><span class="sxs-lookup"><span data-stu-id="ae16f-156">Daily (a maximum of 31 days can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="ae16f-157">Еженедельно (можно отобразить не более 12 недель)</span><span class="sxs-lookup"><span data-stu-id="ae16f-157">Weekly (a maximum of 12 weeks can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="ae16f-158">Ежемесячно (можно отобразить не более 12 месяцев)</span><span class="sxs-lookup"><span data-stu-id="ae16f-158">Monthly (a maximum of 12 months can be displayed)</span></span></p></li>
</ul>
<p><span data-ttu-id="ae16f-159">Если количество значений между начальной и конечной датами превышает максимально допустимое для выбранного интервала, отображается максимальное возможное количество значений (от начальной даты и далее).</span><span class="sxs-lookup"><span data-stu-id="ae16f-159">If the start and end dates exceed the maximum number of values allowed for the selected interval, only the maximum number of values (starting from the start date) is displayed.</span></span> <span data-ttu-id="ae16f-160">Например, если выбрать ежедневный интервал с датой начала 7/7/2012 и датой окончания 2/28/2012, данные будут выводиться для дней 8/7/2012 12:00 – 9/7/2012 12:00 AM (то есть, всего за 31 дня).</span><span class="sxs-lookup"><span data-stu-id="ae16f-160">For example, if you select the Daily interval with a start date of 7/7/2012 and an end date of 2/28/2012, data is displayed for the days 8/7/2012 12:00 AM to 9/7/2012 12:00 AM (that is, a total of 31 days' worth of data).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae16f-161"><strong>Пул</strong></span><span class="sxs-lookup"><span data-stu-id="ae16f-161"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="ae16f-p111">Полное доменное имя пула регистратора или пограничного сервера. Можно выбрать отдельный пул или нажать <strong>[Все]</strong>, чтобы просмотреть данные для всех пулов. Этот раскрывающийся список автоматически заполняется на основе записей в базе данных.</span><span class="sxs-lookup"><span data-stu-id="ae16f-p111">Fully qualified domain name (FQDN) of the Registrar pool or Edge Server. You can either select an individual pool or click <strong>[All]</strong> to view data for all the pools. This drop-down list is automatically populated for you based on the records in the database.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-peer-to-peer-sessions"></a><span data-ttu-id="ae16f-165">Метрики для одноранговых сеансов</span><span class="sxs-lookup"><span data-stu-id="ae16f-165">Metrics for Peer-to-Peer Sessions</span></span>

<span data-ttu-id="ae16f-166">В следующей таблице приведены сведения, предоставляемые отчетом по контролю допуска звонков для одноранговых сеансов (т.е. сеансов, в которых только два участника).</span><span class="sxs-lookup"><span data-stu-id="ae16f-166">The following table lists the information provided in the Call Diagnostic Summary Report for peer-to-peer sessions (that is, sessions involving just two participants).</span></span>

### <a name="metrics-for-peer-to-peer-sessions"></a><span data-ttu-id="ae16f-167">Метрики для одноранговых сеансов</span><span class="sxs-lookup"><span data-stu-id="ae16f-167">Metrics for Peer-to-Peer Sessions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ae16f-168">Имя</span><span class="sxs-lookup"><span data-stu-id="ae16f-168">Name</span></span></th>
<th><span data-ttu-id="ae16f-169">Поддержка сортировки</span><span class="sxs-lookup"><span data-stu-id="ae16f-169">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="ae16f-170">Описание</span><span class="sxs-lookup"><span data-stu-id="ae16f-170">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ae16f-171"><strong>Всего сеансов</strong></span><span class="sxs-lookup"><span data-stu-id="ae16f-171"><strong>Total sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="ae16f-172">Нет</span><span class="sxs-lookup"><span data-stu-id="ae16f-172">No</span></span></p></td>
<td><p><span data-ttu-id="ae16f-173">Общее количество проведенных одноранговых сеансов.</span><span class="sxs-lookup"><span data-stu-id="ae16f-173">Total number of peer-to-peer sessions conducted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae16f-174"><strong>Процент сбоев</strong></span><span class="sxs-lookup"><span data-stu-id="ae16f-174"><strong>Failure rate</strong></span></span></p></td>
<td><p><span data-ttu-id="ae16f-175">Нет</span><span class="sxs-lookup"><span data-stu-id="ae16f-175">No</span></span></p></td>
<td><p><span data-ttu-id="ae16f-p112">Процент неудачных одноранговых сеансов. Если щелкнуть этот элемент, то появится диагностический отчет по одноранговым действиям, отображающий более подробные сведения о неудачных одноранговых сеансах.</span><span class="sxs-lookup"><span data-stu-id="ae16f-p112">Percentage of peer-to-peer sessions that failed. When you click this item, the report shows the Peer-to-Peer Activity Diagnostic report, which displays more detailed information about the failed peer-to-peer sessions.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-conferencing-sessions"></a><span data-ttu-id="ae16f-178">Метрики для сеансов конференц-связи</span><span class="sxs-lookup"><span data-stu-id="ae16f-178">Metrics for Conferencing Sessions</span></span>

<span data-ttu-id="ae16f-179">В следующей таблице приведены сведения, которые предоставляются в диагностическом отчете по вызовам для сеансов конференц-связи (т.е. сеансов, в которых не менее трех участников).</span><span class="sxs-lookup"><span data-stu-id="ae16f-179">The following table lists the information provided in the Call Diagnostic Report for conferencing sessions (that is, sessions involving three or more participants).</span></span>

### <a name="metrics-for-conferencing-sessions"></a><span data-ttu-id="ae16f-180">Метрики для сеансов конференц-связи</span><span class="sxs-lookup"><span data-stu-id="ae16f-180">Metrics for Conferencing Sessions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ae16f-181">Имя</span><span class="sxs-lookup"><span data-stu-id="ae16f-181">Name</span></span></th>
<th><span data-ttu-id="ae16f-182">Поддержка сортировки</span><span class="sxs-lookup"><span data-stu-id="ae16f-182">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="ae16f-183">Описание</span><span class="sxs-lookup"><span data-stu-id="ae16f-183">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ae16f-184"><strong>Всего конференций</strong></span><span class="sxs-lookup"><span data-stu-id="ae16f-184"><strong>Total conferences</strong></span></span></p></td>
<td><p><span data-ttu-id="ae16f-185">Нет</span><span class="sxs-lookup"><span data-stu-id="ae16f-185">No</span></span></p></td>
<td><p><span data-ttu-id="ae16f-186">Общее количество проведенных конференций.</span><span class="sxs-lookup"><span data-stu-id="ae16f-186">Total number of conferences conducted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae16f-187"><strong>Общее количество сеансов конференц-связи</strong></span><span class="sxs-lookup"><span data-stu-id="ae16f-187"><strong>Total conference sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="ae16f-188">Нет</span><span class="sxs-lookup"><span data-stu-id="ae16f-188">No</span></span></p></td>
<td><p><span data-ttu-id="ae16f-189">Общее количество проведенных сеансов конференц-связи.</span><span class="sxs-lookup"><span data-stu-id="ae16f-189">Total number of conferencing sessions conducted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae16f-190"><strong>Общее количество неудачных сеансов</strong></span><span class="sxs-lookup"><span data-stu-id="ae16f-190"><strong>Overall session failure rate</strong></span></span></p></td>
<td><p><span data-ttu-id="ae16f-191">Нет</span><span class="sxs-lookup"><span data-stu-id="ae16f-191">No</span></span></p></td>
<td><p><span data-ttu-id="ae16f-192">Процент неудачных сеансов конференц-связи.</span><span class="sxs-lookup"><span data-stu-id="ae16f-192">Percentage of the total conferencing sessions that failed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae16f-193"><strong>Сеансы центра конференций</strong></span><span class="sxs-lookup"><span data-stu-id="ae16f-193"><strong>Focus sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="ae16f-194">Нет</span><span class="sxs-lookup"><span data-stu-id="ae16f-194">No</span></span></p></td>
<td><p><span data-ttu-id="ae16f-195">Общее количество неудачных сеансов конференц-связи с центром.</span><span class="sxs-lookup"><span data-stu-id="ae16f-195">Total number of Focus-based conferencing sessions that failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae16f-196"><strong>Неудачные сеансы с центром</strong></span><span class="sxs-lookup"><span data-stu-id="ae16f-196"><strong>Focus failure rate</strong></span></span></p></td>
<td><p><span data-ttu-id="ae16f-197">Нет</span><span class="sxs-lookup"><span data-stu-id="ae16f-197">No</span></span></p></td>
<td><p><span data-ttu-id="ae16f-198">Процент неудачных сеансов конференц-связи с центром.</span><span class="sxs-lookup"><span data-stu-id="ae16f-198">Percentage of the Focus-based conferencing sessions that failed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae16f-199"><strong>Сеансы MCU</strong></span><span class="sxs-lookup"><span data-stu-id="ae16f-199"><strong>MCU sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="ae16f-200">Нет</span><span class="sxs-lookup"><span data-stu-id="ae16f-200">No</span></span></p></td>
<td><p><span data-ttu-id="ae16f-201">Общее количество неудачных сеансов конференц-связи для конференций на основе сервера (ранее называвшегося узлом управления многосторонней связью или MCU).</span><span class="sxs-lookup"><span data-stu-id="ae16f-201">Total number of conferencing server-based (formerly known as Multipoint Control Unit or MCU) conferences that failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae16f-202"><strong>Неудачные сеансы с MCU</strong></span><span class="sxs-lookup"><span data-stu-id="ae16f-202"><strong>MCU failure rate</strong></span></span></p></td>
<td><p><span data-ttu-id="ae16f-203">Нет</span><span class="sxs-lookup"><span data-stu-id="ae16f-203">No</span></span></p></td>
<td><p><span data-ttu-id="ae16f-204">Процент неудачных сеансов конференц-связи для конференций на основе сервера (ранее называвшегося узлом управления многосторонней связью или MCU).</span><span class="sxs-lookup"><span data-stu-id="ae16f-204">Percentage of the conferencing server-based (formerly known as Multipoint Control Unit or MCU) conferences that failed.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="ae16f-205">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ae16f-205">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

