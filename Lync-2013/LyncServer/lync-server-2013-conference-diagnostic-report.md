---
title: 'Lync Server 2013: диагностический отчет по конференциям'
description: 'Lync Server 2013: диагностический отчет по конференциям.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Conference Diagnostic Report
ms:assetid: e9edc23c-8ce8-4ab8-8786-9d22e1e51e14
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615042(v=OCS.15)
ms:contentKeyID: 48185901
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9d3ef3c78bc2145d907d5a40e1aed95a2f4cb4c4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434547"
---
# <a name="conference-diagnostic-report-in-lync-server-2013"></a><span data-ttu-id="8101d-103">Диагностический отчет на Конференции в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8101d-103">Conference Diagnostic Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8101d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8101d-104">

<span> </span></span></span>

<span data-ttu-id="8101d-105">_**Тема последнего изменения:** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="8101d-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="8101d-106">Диагностический отчет о конференц-связи содержит сведения об успешности или сбое всех сеансов конференц-связи.</span><span class="sxs-lookup"><span data-stu-id="8101d-106">The Conference Diagnostic Report provides information about the success and failure of all conferencing sessions.</span></span> <span data-ttu-id="8101d-107">Обратите внимание, что в Microsoft Lync Server различаются различные типы сбоев.</span><span class="sxs-lookup"><span data-stu-id="8101d-107">Note that Microsoft Lync Server distinguishes between different kinds of failure:</span></span>

  - <span data-ttu-id="8101d-p102">**Ожидаемый сбой**. Ожидаемый сбой можно назвать сбоем исключительно с технической точки зрения. Например, предположим, что кто-то запускает конференцию, но вешает трубку прежде, чем другие пользователи могут присоединиться к этой конференции. С технической точки зрения это сбой ? конференция была инициализирована, но не завершена. Однако это сбой, которого можно было ожидать: если организатор отменяет конференцию до присоединения других пользователей, ожидать завершения конференции нельзя.</span><span class="sxs-lookup"><span data-stu-id="8101d-p102">**Expected failure**. An expected failure is typically a failure only in the most technical sense. For example, suppose someone starts a conference but hangs up before anyone can join. Technically that's a failure: the conference was initiated, but not completed. However, that's a failure that you would expect to happen: if the organizer cancels the conference before anyone can join then you would not expect that conference to be completed.</span></span>

  - <span data-ttu-id="8101d-p103">**Неожиданный сбой**. Неожиданный сбой полностью соответствует своему названию ? это ошибка, возникновение которой вы в данных обстоятельствах не ожидали. Например, предположим, что конференцию нельзя провести, так как не удается получить политику собраний организатора. Это неожиданная ошибка: возможность получения политики собраний организатора должна быть доступна всегда.</span><span class="sxs-lookup"><span data-stu-id="8101d-p103">**Unexpected failure**. An unexpected error is exactly what the name implies: an error that, based on the circumstances, you would not expect to occur. For example, suppose a conference could not be held because the organizer's meeting policy could not be retrieved. That's an unexpected error: after all, you should always be able to retrieve a user's meeting policy.</span></span>

<span data-ttu-id="8101d-p104">Обратите внимание на то, что метрики успешного выполнения, ожидаемого сбоя и неожиданного сбоя могут не учитываться в метрике итогового числа сеансов. Например, вы можете увидеть в отчете следующие значения:</span><span class="sxs-lookup"><span data-stu-id="8101d-p104">Note that the Success, Expected failure, and Unexpected failure metrics might not add up to the Total sessions metric. For example, you might see the following values in the Report:</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8101d-119">Число успешных выполнений</span><span class="sxs-lookup"><span data-stu-id="8101d-119">Successes</span></span></th>
<th><span data-ttu-id="8101d-120">Число ожидаемых сбоев</span><span class="sxs-lookup"><span data-stu-id="8101d-120">Expected failures</span></span></th>
<th><span data-ttu-id="8101d-121">Число неожиданных сбоев</span><span class="sxs-lookup"><span data-stu-id="8101d-121">Unexpected failures</span></span></th>
<th><span data-ttu-id="8101d-122">Всего сеансов</span><span class="sxs-lookup"><span data-stu-id="8101d-122">Total sessions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8101d-123">2024</span><span class="sxs-lookup"><span data-stu-id="8101d-123">2024</span></span></p></td>
<td><p><span data-ttu-id="8101d-124">469</span><span class="sxs-lookup"><span data-stu-id="8101d-124">469</span></span></p></td>
<td><p><span data-ttu-id="8101d-125">шестнадцат</span><span class="sxs-lookup"><span data-stu-id="8101d-125">16</span></span></p></td>
<td><p><span data-ttu-id="8101d-126">2521</span><span class="sxs-lookup"><span data-stu-id="8101d-126">2521</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8101d-127">Если сложить 2024 + 469 + 16 получается 2509 сеансов, однако в столбце итогового числа сеансов стоит значение 2521.</span><span class="sxs-lookup"><span data-stu-id="8101d-127">If you add 2024 + 469 + 16 you get a total of 2,509 sessions and yet, the Total sessions column shows a total of 2,521 sessions.</span></span> <span data-ttu-id="8101d-128">Для 12 «отсутствующих» сеансов системе не удалось отнести сеанс к категории успешных или неуспешных.</span><span class="sxs-lookup"><span data-stu-id="8101d-128">The "missing" 12 sessions for are sessions that the system was unable to categorize as successful or unsuccessful.</span></span> <span data-ttu-id="8101d-129">Это иногда является случайом, когда сторонний продукт представляет новый диагностический код, незнакомый с сервером мониторинга.</span><span class="sxs-lookup"><span data-stu-id="8101d-129">That will sometimes be the case when a third-party product introduces a new diagnostic code that is unfamiliar to Monitoring Server.</span></span> <span data-ttu-id="8101d-130">В этом случае звонки, выполненные с использованием этого продукта и отчетность по этому диагностическому коду не всегда можно отнести к категории успешного выполнения, ожидаемого сбоя или неожиданного сбоя.</span><span class="sxs-lookup"><span data-stu-id="8101d-130">When that happens, calls made using that product, and reporting that diagnostic code, cannot always be categorized as being a Success, an Expected failure, or an Unexpected failure.</span></span>

<div>

## <a name="accessing-the-conference-diagnostic-report"></a><span data-ttu-id="8101d-131">Доступ к диагностическому отчету по конференциям</span><span class="sxs-lookup"><span data-stu-id="8101d-131">Accessing the Conference Diagnostic Report</span></span>

<span data-ttu-id="8101d-132">Доступ к диагностическому отчету по конференциям осуществляется с домашней страницы отчетов мониторинга.</span><span class="sxs-lookup"><span data-stu-id="8101d-132">The Conference Diagnostic Report is accessed from the Monitoring Reports home page.</span></span> <span data-ttu-id="8101d-133">Вы можете получить доступ к [отчету о распределении отказов в Lync Server 2013](lync-server-2013-failure-distribution-report.md) , выбрав один из указанных ниже метрик.</span><span class="sxs-lookup"><span data-stu-id="8101d-133">You can access the [Failure Distribution Report in Lync Server 2013](lync-server-2013-failure-distribution-report.md) by clicking either of the following metrics:</span></span>

  - <span data-ttu-id="8101d-134">Unexpected failure volume (Объем неожиданных сбоев)</span><span class="sxs-lookup"><span data-stu-id="8101d-134">Unexpected failure volume</span></span>

  - <span data-ttu-id="8101d-135">Expected failure volume (Ожидаемый сбой, объем)</span><span class="sxs-lookup"><span data-stu-id="8101d-135">Expected failure volume</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-conference-diagnostic-report"></a><span data-ttu-id="8101d-136">Эффективное использование диагностического отчета по конференциям</span><span class="sxs-lookup"><span data-stu-id="8101d-136">Making the Best Use of the Conference Diagnostic Report</span></span>

<span data-ttu-id="8101d-137">В отчете диагностика Конференции есть ряд диаграмм.</span><span class="sxs-lookup"><span data-stu-id="8101d-137">The Conference Diagnostic Report includes a series of graphs.</span></span> <span data-ttu-id="8101d-138">Каждый столбец, показанный на диаграмме, действительно является гиперссылкой.</span><span class="sxs-lookup"><span data-stu-id="8101d-138">Each of the columns shown in the graph is actually a hyperlink.</span></span> <span data-ttu-id="8101d-139">Если щелкнуть столбец, в Lync Server 2013 в течение этого периода времени и типа конференции будет детально рассмотрен [отчет о распределении отказов](lync-server-2013-failure-distribution-report.md) .</span><span class="sxs-lookup"><span data-stu-id="8101d-139">If you click a column, you'll drill down to the [Failure Distribution Report in Lync Server 2013](lync-server-2013-failure-distribution-report.md) for that time period and that conference type.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="8101d-140">Фильтры</span><span class="sxs-lookup"><span data-stu-id="8101d-140">Filters</span></span>

<span data-ttu-id="8101d-p108">Фильтры позволяют вам возвратить уточненный набор данных или просматривать возвращенные данные различными способами. Например, диагностический отчет по конференциям позволяет вам выполнять фильтрацию по таким условиям, как тип проводимой конференции (например, конференция Focus) или используемый для конференции пограничный сервер. Вы также можете определить группировку данных. В данном случае конференции группируются по часу, дню, неделе или месяцу.</span><span class="sxs-lookup"><span data-stu-id="8101d-p108">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. For example, the Conference Diagnostic Report enables you to filter on such things as the type of conference being conducted (for example, a Focus-based conference) or by the Edge Server used in the conference. You can also choose how data should be grouped. In this case, conferences are grouped by hour, day, week, or month.</span></span>

<span data-ttu-id="8101d-145">В следующей таблице перечислены фильтры, которые вы можете использовать в диагностическом отчете по конференциям.</span><span class="sxs-lookup"><span data-stu-id="8101d-145">The following table lists the filters that you can use with the Conference Diagnostic Report.</span></span>

### <a name="conference-diagnostic-report-filters"></a><span data-ttu-id="8101d-146">Фильтры диагностического отчета по конференциям</span><span class="sxs-lookup"><span data-stu-id="8101d-146">Conference Diagnostic Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8101d-147">Имя</span><span class="sxs-lookup"><span data-stu-id="8101d-147">Name</span></span></th>
<th><span data-ttu-id="8101d-148">Описание</span><span class="sxs-lookup"><span data-stu-id="8101d-148">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8101d-149"><strong>От</strong></span><span class="sxs-lookup"><span data-stu-id="8101d-149"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="8101d-p109">Начальные дата/время для временного диапазона. Чтобы просмотреть данные по часам, введите начальные дату и время следующим образом:</span><span class="sxs-lookup"><span data-stu-id="8101d-p109">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="8101d-152">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="8101d-152">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="8101d-p110">Если вы не вводите начальное время, отчет автоматически начинается с 12:00 AM указанного дня. Чтобы просмотреть данные по дням, просто введите дату:</span><span class="sxs-lookup"><span data-stu-id="8101d-p110">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="8101d-155">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="8101d-155">7/7/2012</span></span></p>
<p><span data-ttu-id="8101d-156">Чтобы просмотреть данные за неделю или месяц, введите дату, выпадающую на любое время в рамках недели или месяца, которые вы хотите просмотреть (вам не требуется вводить первый день недели или месяца):</span><span class="sxs-lookup"><span data-stu-id="8101d-156">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="8101d-157">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="8101d-157">7/3/2012</span></span></p>
<p><span data-ttu-id="8101d-158">Недели всегда отсчитываются с воскресенья по субботу.</span><span class="sxs-lookup"><span data-stu-id="8101d-158">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8101d-159"><strong>До</strong></span><span class="sxs-lookup"><span data-stu-id="8101d-159"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="8101d-p111">Конечные дата/время для временного диапазона. Чтобы просмотреть данные по часам, введите конечные дату и время следующим образом:</span><span class="sxs-lookup"><span data-stu-id="8101d-p111">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="8101d-162">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="8101d-162">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="8101d-p112">Если вы не вводите конечное время, отчет автоматически заканчивается в 12:00 AM указанного дня. Чтобы просмотреть данные по дням, просто введите дату:</span><span class="sxs-lookup"><span data-stu-id="8101d-p112">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="8101d-165">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="8101d-165">7/7/2012</span></span></p>
<p><span data-ttu-id="8101d-166">Чтобы просмотреть данные за неделю или месяц, введите дату, выпадающую на любое время в рамках недели или месяца, которые вы хотите просмотреть (вам не требуется вводить первый день недели или месяца):</span><span class="sxs-lookup"><span data-stu-id="8101d-166">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="8101d-167">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="8101d-167">7/3/2012</span></span></p>
<p><span data-ttu-id="8101d-168">Недели всегда отсчитываются с воскресенья по субботу.</span><span class="sxs-lookup"><span data-stu-id="8101d-168">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8101d-169"><strong>Интервал</strong></span><span class="sxs-lookup"><span data-stu-id="8101d-169"><strong>Interval</strong></span></span></p></td>
<td><p><span data-ttu-id="8101d-p113">Временной интервал. Выберите одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="8101d-p113">Time interval. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="8101d-172">Ежечасно (можно отобразить не более 25 часов)</span><span class="sxs-lookup"><span data-stu-id="8101d-172">Hourly (a maximum of 25 hours can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="8101d-173">Ежедневно (можно отобразить не более 31 дня)</span><span class="sxs-lookup"><span data-stu-id="8101d-173">Daily (a maximum of 31 days can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="8101d-174">Еженедельно (можно отобразить не более 12 недель)</span><span class="sxs-lookup"><span data-stu-id="8101d-174">Weekly (a maximum of 12 weeks can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="8101d-175">Ежемесячно (можно отобразить не более 12 месяцев)</span><span class="sxs-lookup"><span data-stu-id="8101d-175">Monthly (a maximum of 12 months can be displayed)</span></span></p></li>
</ul>
<p><span data-ttu-id="8101d-176">Если количество значений между начальной и конечной датами превышает максимально допустимое для выбранного интервала, отображается максимальное возможное количество значений (от начальной даты и далее).</span><span class="sxs-lookup"><span data-stu-id="8101d-176">If the start and end dates exceed the maximum number of values allowed for the selected interval, only the maximum number of values (starting from the start date) is displayed.</span></span> <span data-ttu-id="8101d-177">Например, если выбрать ежедневный интервал с датой начала 7/7/2012 и датой окончания 2/28/2012, данные будут выводиться для дней 8/7/2012 12:00 – 9/7/2012 12:00 AM (то есть, всего за 31 дня).</span><span class="sxs-lookup"><span data-stu-id="8101d-177">For example, if you select the Daily interval with a start date of 7/7/2012 and an end date of 2/28/2012, data is displayed for the days 8/7/2012 12:00 AM to 9/7/2012 12:00 AM (that is, a total of 31 days' worth of data).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8101d-178"><strong>Пул</strong></span><span class="sxs-lookup"><span data-stu-id="8101d-178"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="8101d-p115">Полное доменное имя пула регистратора или пограничного сервера. Можно выбрать отдельный пул или нажать <strong>[Все]</strong>, чтобы просмотреть данные для всех пулов. Этот раскрывающийся список автоматически заполняется на основе записей в базе данных.</span><span class="sxs-lookup"><span data-stu-id="8101d-p115">Fully qualified domain name (FQDN) of the Registrar pool or Edge Server. You can either select an individual pool or click <strong>[All]</strong> to view data for all the pools. This drop-down list is automatically populated for you based on the records in the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8101d-182"><strong>Сеансы конференц-связи</strong></span><span class="sxs-lookup"><span data-stu-id="8101d-182"><strong>Conference sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="8101d-p116">Указывает тип сеанса конференц-связи. Выберите одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="8101d-p116">Indicates the type of conferencing session. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="8101d-185">[All] (Все)</span><span class="sxs-lookup"><span data-stu-id="8101d-185">[All]</span></span></p></li>
<li><p><span data-ttu-id="8101d-186">Сеансы центра конференций</span><span class="sxs-lookup"><span data-stu-id="8101d-186">Focus sessions</span></span></p></li>
<li><p><span data-ttu-id="8101d-187">All MCU sessions (Все сеансы MCU)</span><span class="sxs-lookup"><span data-stu-id="8101d-187">All MCU sessions</span></span></p></li>
<li><p><span data-ttu-id="8101d-188">IM conferencing (Конференции с обменом мгновенными сообщениями)</span><span class="sxs-lookup"><span data-stu-id="8101d-188">IM conferencing</span></span></p></li>
<li><p><span data-ttu-id="8101d-189">Общий доступ к приложениям</span><span class="sxs-lookup"><span data-stu-id="8101d-189">Application sharing</span></span></p></li>
<li><p><span data-ttu-id="8101d-190">A/V conferencing (Аудио- и видеоконференции)</span><span class="sxs-lookup"><span data-stu-id="8101d-190">A/V conferencing</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics"></a><span data-ttu-id="8101d-191">Показатели</span><span class="sxs-lookup"><span data-stu-id="8101d-191">Metrics</span></span>

<span data-ttu-id="8101d-192">В следующей таблице перечислены сведения, представленные в диагностическом отчете по конференциям.</span><span class="sxs-lookup"><span data-stu-id="8101d-192">The following table lists the information provided in the Conference Diagnostic Report for each type of conferencing session.</span></span>

### <a name="conference-diagnostic-report-metrics"></a><span data-ttu-id="8101d-193">Метрики диагностического отчета по конференциям</span><span class="sxs-lookup"><span data-stu-id="8101d-193">Conference Diagnostic Report Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8101d-194">Имя</span><span class="sxs-lookup"><span data-stu-id="8101d-194">Name</span></span></th>
<th><span data-ttu-id="8101d-195">Поддержка сортировки</span><span class="sxs-lookup"><span data-stu-id="8101d-195">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="8101d-196">Описание</span><span class="sxs-lookup"><span data-stu-id="8101d-196">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8101d-197"><strong>Success volume (Объем успешной связи)</strong></span><span class="sxs-lookup"><span data-stu-id="8101d-197"><strong>Success volume</strong></span></span></p></td>
<td><p><span data-ttu-id="8101d-198">Нет</span><span class="sxs-lookup"><span data-stu-id="8101d-198">No</span></span></p></td>
<td><p><span data-ttu-id="8101d-199">Общее число успешных конференций.</span><span class="sxs-lookup"><span data-stu-id="8101d-199">Total number of successful conferences.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8101d-200"><strong>Доля успешной связи</strong></span><span class="sxs-lookup"><span data-stu-id="8101d-200"><strong>Success percentage</strong></span></span></p></td>
<td><p><span data-ttu-id="8101d-201">Нет</span><span class="sxs-lookup"><span data-stu-id="8101d-201">No</span></span></p></td>
<td><p><span data-ttu-id="8101d-p117">Процентное отношение конференций, которые были завершены со значительными проблемами. Значение вычисляется путем деления значения «Success volume» (Успех, процент) на значение «Total sessions» (Всего сеансов).</span><span class="sxs-lookup"><span data-stu-id="8101d-p117">Percentage of conferences that completed with significant problems. Calculated by dividing the Success volume by the Total sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8101d-204"><strong>Unexpected failure volume (Объем неожиданных сбоев)</strong></span><span class="sxs-lookup"><span data-stu-id="8101d-204"><strong>Expected failure volume</strong></span></span></p></td>
<td><p><span data-ttu-id="8101d-205">Нет</span><span class="sxs-lookup"><span data-stu-id="8101d-205">No</span></span></p></td>
<td><p><span data-ttu-id="8101d-206">Общее количество конференций, в которых &quot; произошла ожидаемая ошибка &quot; .</span><span class="sxs-lookup"><span data-stu-id="8101d-206">Total number of conferences where an &quot;expected failure&quot; occurred.</span></span></p>
<p><span data-ttu-id="8101d-p118">Ожидаемый сбой ? это сбой, возникновение которого ожидаемо. Например, если пользователь задал для себя состояние «Не беспокоить», можно ожидать, что любой звонок этому пользователю будет неудачным.</span><span class="sxs-lookup"><span data-stu-id="8101d-p118">An expected failure is a failure that is expected to happen. For example, if a user has set his or her status to Do Not Disturb you would expect any call to that user to fail.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8101d-209"><strong>Expected failure percentage (Доля ожидаемых сбоев)</strong></span><span class="sxs-lookup"><span data-stu-id="8101d-209"><strong>Expected failure percentage</strong></span></span></p></td>
<td><p><span data-ttu-id="8101d-210">Нет</span><span class="sxs-lookup"><span data-stu-id="8101d-210">No</span></span></p></td>
<td><p><span data-ttu-id="8101d-p119">Процентное отношение конференций, для которых возник ожидаемый сбой. Значение вычисляется путем деления значения «Expected failure volume» (Ожидаемый сбой, объем) на значение «Total sessions» (Всего сеансов).</span><span class="sxs-lookup"><span data-stu-id="8101d-p119">Percentage of conferences that experienced an expected error. Calculated by dividing the Expected failure volume by the Total sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8101d-213"><strong>Unexpected failure volume (Объем неожиданных сбоев)</strong></span><span class="sxs-lookup"><span data-stu-id="8101d-213"><strong>Unexpected failure volume</strong></span></span></p></td>
<td><p><span data-ttu-id="8101d-214">Нет</span><span class="sxs-lookup"><span data-stu-id="8101d-214">No</span></span></p></td>
<td><p><span data-ttu-id="8101d-215">Общее количество конференций, в которых &quot; произошла непредвиденная ошибка &quot; .</span><span class="sxs-lookup"><span data-stu-id="8101d-215">Total number of conferences where an &quot;unexpected failure&quot; occurred.</span></span></p>
<p><span data-ttu-id="8101d-p120">Неожиданный сбой ? это событие, которое в других условиях считалось бы нормальной работой системы. Например, звонок не следует завершать, если звонящий переведен в режим удержания. Если такое произошло, данное событие будет обозначено как неожиданный сбой.</span><span class="sxs-lookup"><span data-stu-id="8101d-p120">An unexpected failure is a failure that occurs in what would appear to be an otherwise healthy system. For example, a call should not be terminated if the caller is placed on hold. If that occurs, that would be flagged as an unexpected failure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8101d-219"><strong>Unexpected failure percentage (Доля неожиданных сбоев)</strong></span><span class="sxs-lookup"><span data-stu-id="8101d-219"><strong>Unexpected failure percentage</strong></span></span></p></td>
<td><p><span data-ttu-id="8101d-220">Нет</span><span class="sxs-lookup"><span data-stu-id="8101d-220">No</span></span></p></td>
<td><p><span data-ttu-id="8101d-p121">Процентное отношение конференций, для которых возник неожиданный сбой. Значение вычисляется путем деления значения «Unexpected failure volume» (Неожиданный сбой, объем) на значение «Total sessions» (Всего сеансов).</span><span class="sxs-lookup"><span data-stu-id="8101d-p121">Percentage of conferences that experienced an unexpected error. Calculated by dividing the Unexpected failure volume by the Total sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8101d-223"><strong>Всего сеансов</strong></span><span class="sxs-lookup"><span data-stu-id="8101d-223"><strong>Total sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="8101d-224">Нет</span><span class="sxs-lookup"><span data-stu-id="8101d-224">No</span></span></p></td>
<td><p><span data-ttu-id="8101d-225">Общее число конференций, включая успешные конференции, неуспешные (как с ожидаемыми, так и с неожиданными сбоями) конференции и конференции, не отнесенные ни к одной из категорий.</span><span class="sxs-lookup"><span data-stu-id="8101d-225">Total number of conferences, including successful conferences, failed conferences (both expected failures and unexpected failures), and uncategorized conferences.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="8101d-226">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8101d-226">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

