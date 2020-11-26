---
title: 'Lync Server 2013: одноранговый отчет о мгновенных сообщениях'
description: 'Lync Server 2013: одноранговый отчет о мгновенных сообщениях.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Peer-to-Peer IM Report
ms:assetid: 19ec0145-2398-437b-8989-f780c179b798
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558620(v=OCS.15)
ms:contentKeyID: 48183533
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: eac6291d0f099af8269ed15f7dc8c654ac944ed0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424687"
---
# <a name="peer-to-peer-im-report-in-lync-server-2013"></a><span data-ttu-id="2bb53-103">Одноранговый отчет о мгновенных сообщениях в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2bb53-103">Peer-to-Peer IM Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2bb53-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2bb53-104">

<span> </span></span></span>

<span data-ttu-id="2bb53-105">_**Тема последнего изменения:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="2bb53-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="2bb53-p101">Отчет об одноранговом обмене мгновенными сообщениями предоставляет сведения о тенденциях, связанных с сеансами однорангового обмена мгновенными сообщениями. Эти сведения разбиты по пулам и типам проверки подлинности. В отчете может отображаться либо общее число сеансов, проведенных за указанный период времени (например, день или час), либо общее число мгновенных сообщений, отправленных за этот период.</span><span class="sxs-lookup"><span data-stu-id="2bb53-p101">The Peer-to-Peer IM Report provides trend information about peer-to-peer instant messaging (IM) sessions, broken down by pool and by authentication type. The report can show either the total number of sessions held during the specified time period (for example, day-by-day or hour-by-hour), or it can show the total number of instant messages sent during that time period.</span></span>

<div>

## <a name="accessing-the-peer-to-peer-im-report"></a><span data-ttu-id="2bb53-108">Доступ к отчету об одноранговом обмене мгновенными сообщениями</span><span class="sxs-lookup"><span data-stu-id="2bb53-108">Accessing the Peer-to-Peer IM Report</span></span>

<span data-ttu-id="2bb53-109">Вы можете получить доступ к отчету о одноранговых СООБЩЕНИЯх только в том случае, если открыть [сводный отчет о действиях одноранговых узлов в Lync Server 2013](lync-server-2013-peer-to-peer-activity-summary-report.md) и выбрать один из следующих метрик:</span><span class="sxs-lookup"><span data-stu-id="2bb53-109">You can access the Peer-to-Peer IM Report only by opening the [Peer-to-Peer Activity Summary Report in Lync Server 2013](lync-server-2013-peer-to-peer-activity-summary-report.md) and then clicking either of the following metrics:</span></span>

  - <span data-ttu-id="2bb53-110">Общее количество одноранговых сеансов обмена мгновенными сообщениями</span><span class="sxs-lookup"><span data-stu-id="2bb53-110">Total peer-to-peer IM sessions</span></span>

  - <span data-ttu-id="2bb53-111">Общее количество одноранговых мгновенных сообщений</span><span class="sxs-lookup"><span data-stu-id="2bb53-111">Total peer-to-peer IM messages</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-peer-to-peer-im-report"></a><span data-ttu-id="2bb53-112">Рекомендации по использованию отчета об одноранговом обмене мгновенными сообщениями</span><span class="sxs-lookup"><span data-stu-id="2bb53-112">Making the Best Use of the Peer-to-Peer IM Report</span></span>

<span data-ttu-id="2bb53-p102">По умолчанию в отчете об одноранговом обмене мгновенными сообщениями приводится количество сообщений за час (или за день в зависимости от параметров). Однако вы также можете просмотреть почасовое количество сеансов в день. Для этого нажмите кнопку **Показать или скрыть параметры** в правом верхнем углу окна отчетов. После этого вы можете выбрать в раскрывающемся списке **Отчет по** пункт **Число сеансов**.</span><span class="sxs-lookup"><span data-stu-id="2bb53-p102">By default, the Peer-to-Peer IM Report shows you the message count per-hour (or day, depending on your settings). However, you can also choose to view the day by sessions per hour. To do that, click **Hide/Show Parameters** in the upper-right corner of the Reports window, and then click **Session Count** from the **Report by** list.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="2bb53-116">Фильтры</span><span class="sxs-lookup"><span data-stu-id="2bb53-116">Filters</span></span>

<span data-ttu-id="2bb53-p103">Фильтры позволяют получить более конкретные наборы возвращаемых данных. В следующей таблице перечислены фильтры, которые можно использовать с отчетом об одноранговом обмене мгновенными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="2bb53-p103">Filters provide a way for you to return a more finely targeted set of data or to view the returned data in different ways. The following table lists the filters that you can use with the Peer-to-Peer IM Report.</span></span>

### <a name="peer-to-peer-im-report-filters"></a><span data-ttu-id="2bb53-119">Фильтры отчета об одноранговом обмене мгновенными сообщениями</span><span class="sxs-lookup"><span data-stu-id="2bb53-119">Peer-to-Peer IM Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2bb53-120">Имя</span><span class="sxs-lookup"><span data-stu-id="2bb53-120">Name</span></span></th>
<th><span data-ttu-id="2bb53-121">Описание</span><span class="sxs-lookup"><span data-stu-id="2bb53-121">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2bb53-122"><strong>От</strong></span><span class="sxs-lookup"><span data-stu-id="2bb53-122"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="2bb53-p104">Начальная дата и начальное время для диапазона времени. Чтобы просмотреть данные по часам, введите начальную дату и начальное время в следующем формате:</span><span class="sxs-lookup"><span data-stu-id="2bb53-p104">Start date and time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="2bb53-125">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="2bb53-125">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="2bb53-p105">Если вы не вводите начальное время, отчет автоматически начинается с 12:00 AM указанного дня. Чтобы просмотреть данные по дням, просто введите дату:</span><span class="sxs-lookup"><span data-stu-id="2bb53-p105">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="2bb53-128">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="2bb53-128">7/7/2012</span></span></p>
<p><span data-ttu-id="2bb53-129">Чтобы просмотреть данные за неделю или месяц, введите любую дату соответствующей недели или месяца (необязательно первую их дату):</span><span class="sxs-lookup"><span data-stu-id="2bb53-129">To view by week or by month, enter a date that falls anywhere within the week or month (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="2bb53-130">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="2bb53-130">7/3/2012</span></span></p>
<p><span data-ttu-id="2bb53-131">Недели всегда отсчитываются с воскресенья по субботу.</span><span class="sxs-lookup"><span data-stu-id="2bb53-131">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2bb53-132"><strong>До</strong></span><span class="sxs-lookup"><span data-stu-id="2bb53-132"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="2bb53-p106">Конечная дата и конечное время для диапазона времени. Чтобы просмотреть данные по часам, введите конечную дату и конечное время в следующем формате:</span><span class="sxs-lookup"><span data-stu-id="2bb53-p106">End date and time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="2bb53-135">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="2bb53-135">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="2bb53-p107">Если вы не вводите конечное время, отчет автоматически заканчивается в 12:00 AM указанного дня. Чтобы просмотреть данные по дням, просто введите дату:</span><span class="sxs-lookup"><span data-stu-id="2bb53-p107">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="2bb53-138">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="2bb53-138">7/7/2012</span></span></p>
<p><span data-ttu-id="2bb53-139">Чтобы просмотреть данные за неделю или месяц, введите дату, выпадающую на любое время в рамках недели или месяца, которые вы хотите просмотреть (вам не требуется вводить первый день недели или месяца):</span><span class="sxs-lookup"><span data-stu-id="2bb53-139">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="2bb53-140">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="2bb53-140">7/3/2012</span></span></p>
<p><span data-ttu-id="2bb53-141">Недели всегда отсчитываются с воскресенья по субботу.</span><span class="sxs-lookup"><span data-stu-id="2bb53-141">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2bb53-142"><strong>Интервал</strong></span><span class="sxs-lookup"><span data-stu-id="2bb53-142"><strong>Interval</strong></span></span></p></td>
<td><p><span data-ttu-id="2bb53-p108">Временной интервал. Выберите одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="2bb53-p108">Time interval. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="2bb53-145">Ежечасно (можно отобразить не более 25 часов)</span><span class="sxs-lookup"><span data-stu-id="2bb53-145">Hourly (a maximum of 25 hours can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="2bb53-146">Ежедневно (можно отобразить не более 31 дня)</span><span class="sxs-lookup"><span data-stu-id="2bb53-146">Daily (a maximum of 31 days can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="2bb53-147">Еженедельно (можно отобразить не более 12 недель)</span><span class="sxs-lookup"><span data-stu-id="2bb53-147">Weekly (a maximum of 12 weeks can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="2bb53-148">Ежемесячно (можно отобразить не более 12 месяцев)</span><span class="sxs-lookup"><span data-stu-id="2bb53-148">Monthly (a maximum of 12 months can be displayed)</span></span></p></li>
</ul>
<p><span data-ttu-id="2bb53-149">Если число значений между начальной и конечной датами превышает максимальное допустимое для выбранного интервала, отображается максимальное возможное число значений (с начальной даты).</span><span class="sxs-lookup"><span data-stu-id="2bb53-149">If the start and end dates exceed the maximum number of values allowed for the selected interval then only the maximum number of values (starting from the start date) are displayed.</span></span> <span data-ttu-id="2bb53-150">Например, если выбрать ежедневный интервал с датой начала 7/7/2012 и датой окончания 2/28/2012, данные будут выводиться для дней 8/7/2012 12:00 – 9/7/2012 12:00 AM (то есть, всего за 31 дня).</span><span class="sxs-lookup"><span data-stu-id="2bb53-150">For example, if you select the Daily interval with a start date of 7/7/2012 and an end date of 2/28/2012, data is displayed for the days 8/7/2012 12:00 AM to 9/7/2012 12:00 AM (that is, a total of 31 days' worth of data).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2bb53-151"><strong>Report by (Отчетность)</strong></span><span class="sxs-lookup"><span data-stu-id="2bb53-151"><strong>Report by</strong></span></span></p></td>
<td><p><span data-ttu-id="2bb53-p110">Указывает значения для использования в отчете. Выберите одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="2bb53-p110">Indicates the values to be used in the report. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="2bb53-154">Session count (Число сеансов)</span><span class="sxs-lookup"><span data-stu-id="2bb53-154">Session count</span></span></p></li>
<li><p><span data-ttu-id="2bb53-155">Число сообщений</span><span class="sxs-lookup"><span data-stu-id="2bb53-155">Message count</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-peer-to-peer-im-session-by-pool"></a><span data-ttu-id="2bb53-156">Показатели сеансов однорангового обмена мгновенными сообщениями по пулу</span><span class="sxs-lookup"><span data-stu-id="2bb53-156">Metrics for Peer-to-Peer IM Session by Pool</span></span>

<span data-ttu-id="2bb53-157">В следующей таблице показаны сведения, содержащиеся в отчете об одноранговом обмене мгновенными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="2bb53-157">The following table lists the information provided in the Peer-to-Peer IM Report.</span></span>

### <a name="metrics-for-peer-to-peer-im-session-by-pool"></a><span data-ttu-id="2bb53-158">Показатели сеансов однорангового обмена мгновенными сообщениями по пулу</span><span class="sxs-lookup"><span data-stu-id="2bb53-158">Metrics for Peer-to-Peer IM Session by Pool</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2bb53-159">Имя</span><span class="sxs-lookup"><span data-stu-id="2bb53-159">Name</span></span></th>
<th><span data-ttu-id="2bb53-160">Поддержка сортировки</span><span class="sxs-lookup"><span data-stu-id="2bb53-160">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="2bb53-161">Описание</span><span class="sxs-lookup"><span data-stu-id="2bb53-161">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2bb53-162"><strong>Пул</strong></span><span class="sxs-lookup"><span data-stu-id="2bb53-162"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="2bb53-163">Нет</span><span class="sxs-lookup"><span data-stu-id="2bb53-163">No</span></span></p></td>
<td><p><span data-ttu-id="2bb53-164">Имя пула регистраторов или пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="2bb53-164">Name of the Registrar pool or Edge Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2bb53-165"><strong>Дата/время</strong></span><span class="sxs-lookup"><span data-stu-id="2bb53-165"><strong>Date/Time</strong></span></span></p></td>
<td><p><span data-ttu-id="2bb53-166">Нет</span><span class="sxs-lookup"><span data-stu-id="2bb53-166">No</span></span></p></td>
<td><p><span data-ttu-id="2bb53-167">Дата и время, когда состоялся сеанс.</span><span class="sxs-lookup"><span data-stu-id="2bb53-167">Date and time that the sessions took place.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2bb53-168"><strong>Всего</strong></span><span class="sxs-lookup"><span data-stu-id="2bb53-168"><strong>Total</strong></span></span></p></td>
<td><p><span data-ttu-id="2bb53-169">Нет</span><span class="sxs-lookup"><span data-stu-id="2bb53-169">No</span></span></p></td>
<td><p><span data-ttu-id="2bb53-170">Общее число сеансов или сообщений.</span><span class="sxs-lookup"><span data-stu-id="2bb53-170">Total number of sessions or total message count.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-peer-to-peer-im-session-by-authentication-type"></a><span data-ttu-id="2bb53-171">Показатели сеансов однорангового обмена мгновенными сообщениями по типу проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="2bb53-171">Metrics for Peer-to-Peer IM Session by Authentication Type</span></span>

<span data-ttu-id="2bb53-172">В следующей таблице показаны сведения, содержащиеся в отчете об одноранговом обмене мгновенными сообщениями для каждого типа проверки подлинности, используемого участниками однорангового сеанса.</span><span class="sxs-lookup"><span data-stu-id="2bb53-172">The following table lists the information provided in the Peer-to-Peer IM Report for each type of authentication used by the participants in a peer-to-peer session.</span></span>

### <a name="metrics-for-peer-to-peer-im-session-by-authentication-type"></a><span data-ttu-id="2bb53-173">Показатели сеансов однорангового обмена мгновенными сообщениями по типу проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="2bb53-173">Metrics for Peer-to-Peer IM Session by Authentication Type</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2bb53-174">Имя</span><span class="sxs-lookup"><span data-stu-id="2bb53-174">Name</span></span></th>
<th><span data-ttu-id="2bb53-175">Поддержка сортировки</span><span class="sxs-lookup"><span data-stu-id="2bb53-175">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="2bb53-176">Описание</span><span class="sxs-lookup"><span data-stu-id="2bb53-176">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2bb53-177"><strong>Тип проверки подлинности</strong></span><span class="sxs-lookup"><span data-stu-id="2bb53-177"><strong>Authentication type</strong></span></span></p></td>
<td><p><span data-ttu-id="2bb53-178">Нет</span><span class="sxs-lookup"><span data-stu-id="2bb53-178">No</span></span></p></td>
<td><p><span data-ttu-id="2bb53-p111">Тип проверки подлинности, используемый участниками сеанса. Как правило, используются следующие значения:</span><span class="sxs-lookup"><span data-stu-id="2bb53-p111">Type of authentication used by the session participants. Values are typically one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="2bb53-181">Enterprise</span><span class="sxs-lookup"><span data-stu-id="2bb53-181">Enterprise</span></span></p></li>
<li><p><span data-ttu-id="2bb53-182">Federated</span><span class="sxs-lookup"><span data-stu-id="2bb53-182">Federated</span></span></p></li>
<li><p><span data-ttu-id="2bb53-183">PIC</span><span class="sxs-lookup"><span data-stu-id="2bb53-183">PIC</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2bb53-184"><strong>Дата/время</strong></span><span class="sxs-lookup"><span data-stu-id="2bb53-184"><strong>Date/Time</strong></span></span></p></td>
<td><p><span data-ttu-id="2bb53-185">Нет</span><span class="sxs-lookup"><span data-stu-id="2bb53-185">No</span></span></p></td>
<td><p><span data-ttu-id="2bb53-186">Дата и время, когда состоялся сеанс.</span><span class="sxs-lookup"><span data-stu-id="2bb53-186">Date and time that the sessions took place.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2bb53-187"><strong>Всего</strong></span><span class="sxs-lookup"><span data-stu-id="2bb53-187"><strong>Total</strong></span></span></p></td>
<td><p><span data-ttu-id="2bb53-188">Нет</span><span class="sxs-lookup"><span data-stu-id="2bb53-188">No</span></span></p></td>
<td><p><span data-ttu-id="2bb53-189">Общее число сеансов или сообщений.</span><span class="sxs-lookup"><span data-stu-id="2bb53-189">Total number of sessions or total message count.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="2bb53-190">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2bb53-190">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

