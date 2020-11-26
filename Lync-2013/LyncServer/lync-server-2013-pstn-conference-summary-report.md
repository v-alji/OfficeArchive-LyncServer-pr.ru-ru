---
title: 'Lync Server 2013: сводный отчет о конференции по КТСОП'
description: 'Lync Server 2013: сводный отчет о конференции по КТСОП.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: PSTN Conference Summary Report
ms:assetid: 8e2f0862-4dfa-4c2b-bf8d-ad71419f15d2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615014(v=OCS.15)
ms:contentKeyID: 48184764
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c3bc468e494577c229562a1cb7cfddaf839f946f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436729"
---
# <a name="pstn-conference-summary-report-in-lync-server-2013"></a><span data-ttu-id="e6ba8-103">Сводный отчет о конференции по PSTN в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e6ba8-103">PSTN Conference Summary Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e6ba8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e6ba8-104">

<span> </span></span></span>

<span data-ttu-id="e6ba8-105">_**Тема последнего изменения:** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="e6ba8-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="e6ba8-106">В Microsoft Lync Server 2013 — конференция PSTN — это любая конференция, в которой по крайней мере один абонент звонит на звуковую часть с помощью телефонной сети PSTN (телефонная сеть с открытым коммутируемым подключением).</span><span class="sxs-lookup"><span data-stu-id="e6ba8-106">In Microsoft Lync Server 2013, a PSTN conference is any conference in which at least one participant dials in to the audio portion by a using a PSTN (public switched telephone network) phone.</span></span> <span data-ttu-id="e6ba8-107">(КОММУТИРУЕМый телефон – это "стационарные", "сотовый телефон" или любой другой телефон, который не использует голосовую связь по IP-адресу.) Несмотря на то, что в отчетах мониторинга используются сети PSTN-конференции, эти конференции, возможно, более часто известны как конференции с телефонным подключением.</span><span class="sxs-lookup"><span data-stu-id="e6ba8-107">(A PSTN phone is a "landline," a cell phone, or any other phone which does not make use of Voice over IP.) Although referred to as PSTN conferences in the Monitoring Reports, these conferences are perhaps more-commonly known as dial-in conferences.</span></span>

<span data-ttu-id="e6ba8-p102">Сводный отчет по конференциям ТСОП (PSTN Conference Summary Report) предоставляет сведения обо всех конференциях ТСОП, происходивших в вашей организации (т.е. о всех конференциях, хотя бы один участник которых использовал телефонное подключение). В этом отчете содержатся сведения об общем количестве конференций ТСОП, общем количестве участников этих конференций и, что возможно самое важное, об общем количестве пользователей с телефонным подключением (метрика "Total PSTN participants" ("Общее количество участников ТСОП")).</span><span class="sxs-lookup"><span data-stu-id="e6ba8-p102">The PSTN Conference Summary Report provides information about all the PSTN conferences held in your organization (that is, all the conferences that had at least one dial-in user). The report includes information about the total number of PSTN conferences, the total number of people who participated in those conferences, and, perhaps, most important, the total number of dial-in users (the Total PSTN participants metric).</span></span>

<div>

## <a name="accessing-the-pstn-conference-summary-report"></a><span data-ttu-id="e6ba8-110">Доступ к сводному отчету по конференциям ТСОП</span><span class="sxs-lookup"><span data-stu-id="e6ba8-110">Accessing the PSTN Conference Summary Report</span></span>

<span data-ttu-id="e6ba8-p103">Сводный отчет по конференциям ТСОП можно вызвать только с домашней страницы отчетов мониторинга. Этот отчет не привязан ни к каким другим отчетам. Следует отметить, что невозможно получить подробные сведения о вызове для конференции ТСОП, в частности потому, что за предоставление этих сведений отвечают конечные точки, а телефоны ТСОП не имеют возможности отслеживать и отправлять подробные сведения о вызове.</span><span class="sxs-lookup"><span data-stu-id="e6ba8-p103">The PSTN Conference Summary Report can only be accessed from the Monitoring Reports home page. This report is not linked to any other reports. Note that you cannot retrieve detailed call information for a PSTN conference, in part because individual endpoints are responsible for submitting this information. PSTN phones are not capable of tracking or submitting call detail information.</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-pstn-conference-summary-report"></a><span data-ttu-id="e6ba8-115">Оптимальное использование сводного отчета по конференциям ТСОП</span><span class="sxs-lookup"><span data-stu-id="e6ba8-115">Making the Best Use of the PSTN Conference Summary Report</span></span>

<span data-ttu-id="e6ba8-116">Чтобы определить процентную долю всех ваших конференций, включающих пользователей с телефонным подключением, Сравните значение из общей метрики конференций по КТСОП с общей метрикой конференций [в сводном отчете о конференции в Lync Server 2013](lync-server-2013-conference-summary-report.md).</span><span class="sxs-lookup"><span data-stu-id="e6ba8-116">To determine the percentage of all your conferences that include dial-in users, compare the value of the Total PSTN conferences metric with the Total conferences metric found on the [Conference Summary Report in Lync Server 2013](lync-server-2013-conference-summary-report.md).</span></span>

<span data-ttu-id="e6ba8-117">If you don't see as many PSTN conferences as you might have expected to see, keep in mind that the ability to organize a conference that allows dial-in users depends on the conferencing policy that has been assigned to a user: if very few of your users are allowed to hold PSTN conferences you would obviously see very few PSTN conferences.</span><span class="sxs-lookup"><span data-stu-id="e6ba8-117">If you don't see as many PSTN conferences as you might have expected to see, keep in mind that the ability to organize a conference that allows dial-in users depends on the conferencing policy that has been assigned to a user: if very few of your users are allowed to hold PSTN conferences you would obviously see very few PSTN conferences.</span></span> <span data-ttu-id="e6ba8-118">Вы можете быстро проверить, какие из политик конференц-связи (если они есть) разрешают пользователям планировать конференции PSTN, выполнив следующую команду в командной консоли Lync Server.</span><span class="sxs-lookup"><span data-stu-id="e6ba8-118">You can quickly verify which of your conferencing policies (if any) allow users to schedule PSTN conferences by running the following command from within the Lync Server Management Shell:</span></span>

    Get-CsConferencingPolicy | Select-Object Identity, EnableDialInConferencing

<span data-ttu-id="e6ba8-119">Эти команды возвращают сведения, схожие со следующими:</span><span class="sxs-lookup"><span data-stu-id="e6ba8-119">That will return data similar to this:</span></span>

    Identity                                EnableDialInConferencing
    --------                                ------------------------
    Global                                                      True
    site:Redmond                                               False
    site:Dublin                                                False
    Tag:RedmondDialInUsers                                      True
    Tag:DublinDialInUsers                                       True

<span data-ttu-id="e6ba8-120">Эти команды возвращают сведения, схожие со следующими:</span><span class="sxs-lookup"><span data-stu-id="e6ba8-120">That will return data similar to this:</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="e6ba8-121">Фильтры</span><span class="sxs-lookup"><span data-stu-id="e6ba8-121">Filters</span></span>

<span data-ttu-id="e6ba8-122">Фильтры предоставляют способ возврата более точного набора данных в соответствии с заданными критериями или просмотра возвращенных данных другими способами.</span><span class="sxs-lookup"><span data-stu-id="e6ba8-122">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways.</span></span> <span data-ttu-id="e6ba8-123">Например, сводный отчет по конференциям ТСОП позволяет выбрать способ группирования данных.</span><span class="sxs-lookup"><span data-stu-id="e6ba8-123">For example, the PSTN Conference Summary Report enables you to choose how data should be grouped.</span></span> <span data-ttu-id="e6ba8-124">В этом случае конференции группируются по часу, дню, неделе или месяцу.</span><span class="sxs-lookup"><span data-stu-id="e6ba8-124">In this case, conferences are grouped by hour, day, week, or month.</span></span>

<span data-ttu-id="e6ba8-125">В следующей таблице приведены фильтры, которые можно использовать в сводном отчете по конференциям ТСОП.</span><span class="sxs-lookup"><span data-stu-id="e6ba8-125">The following table lists the filters that you can use with the PSTN Conference Summary Report.</span></span>

### <a name="pstn-conference-summary-report-filters"></a><span data-ttu-id="e6ba8-126">Фильтры сводного отчета по конференциям ТСОП</span><span class="sxs-lookup"><span data-stu-id="e6ba8-126">PSTN Conference Summary Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e6ba8-127">Имя</span><span class="sxs-lookup"><span data-stu-id="e6ba8-127">Name</span></span></th>
<th><span data-ttu-id="e6ba8-128">Описание</span><span class="sxs-lookup"><span data-stu-id="e6ba8-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e6ba8-129"><strong>От</strong></span><span class="sxs-lookup"><span data-stu-id="e6ba8-129"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="e6ba8-p106">Начальные дата/время для временного диапазона. Чтобы просмотреть данные по часам, введите начальные дату и время следующим образом:</span><span class="sxs-lookup"><span data-stu-id="e6ba8-p106">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="e6ba8-132">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="e6ba8-132">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="e6ba8-p107">Если вы не вводите начальное время, отчет автоматически начинается с 12:00 AM указанного дня. Чтобы просмотреть данные по дням, просто введите дату:</span><span class="sxs-lookup"><span data-stu-id="e6ba8-p107">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="e6ba8-135">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="e6ba8-135">7/7/2012</span></span></p>
<p><span data-ttu-id="e6ba8-136">Чтобы просмотреть данные за неделю или месяц, введите дату, выпадающую на любое время в рамках недели или месяца, которые вы хотите просмотреть (вам не требуется вводить первый день недели или месяца):</span><span class="sxs-lookup"><span data-stu-id="e6ba8-136">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="e6ba8-137">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="e6ba8-137">7/3/2012</span></span></p>
<p><span data-ttu-id="e6ba8-138">Недели всегда отсчитываются с воскресенья по субботу.</span><span class="sxs-lookup"><span data-stu-id="e6ba8-138">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6ba8-139"><strong>До</strong></span><span class="sxs-lookup"><span data-stu-id="e6ba8-139"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="e6ba8-p108">Конечные дата/время для временного диапазона. Чтобы просмотреть данные по часам, введите конечные дату и время следующим образом:</span><span class="sxs-lookup"><span data-stu-id="e6ba8-p108">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="e6ba8-142">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="e6ba8-142">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="e6ba8-p109">Если вы не вводите конечное время, отчет автоматически заканчивается в 12:00 AM указанного дня. Чтобы просмотреть данные по дням, просто введите дату:</span><span class="sxs-lookup"><span data-stu-id="e6ba8-p109">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="e6ba8-145">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="e6ba8-145">7/7/2012</span></span></p>
<p><span data-ttu-id="e6ba8-146">Чтобы просмотреть данные за неделю или месяц, введите дату, выпадающую на любое время в рамках недели или месяца, которые вы хотите просмотреть (вам не требуется вводить первый день недели или месяца):</span><span class="sxs-lookup"><span data-stu-id="e6ba8-146">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="e6ba8-147">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="e6ba8-147">7/3/2012</span></span></p>
<p><span data-ttu-id="e6ba8-148">Недели всегда отсчитываются с воскресенья по субботу.</span><span class="sxs-lookup"><span data-stu-id="e6ba8-148">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6ba8-149"><strong>Интервал</strong></span><span class="sxs-lookup"><span data-stu-id="e6ba8-149"><strong>Interval</strong></span></span></p></td>
<td><p><span data-ttu-id="e6ba8-p110">Временной интервал. Выберите одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="e6ba8-p110">Time interval. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="e6ba8-152">Ежечасно (можно отобразить не более 25 часов)</span><span class="sxs-lookup"><span data-stu-id="e6ba8-152">Hourly (a maximum of 25 hours can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="e6ba8-153">Ежедневно (можно отобразить не более 31 дня)</span><span class="sxs-lookup"><span data-stu-id="e6ba8-153">Daily (a maximum of 31 days can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="e6ba8-154">Еженедельно (можно отобразить не более 12 недель)</span><span class="sxs-lookup"><span data-stu-id="e6ba8-154">Weekly (a maximum of 12 weeks can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="e6ba8-155">Ежемесячно (можно отобразить не более 12 месяцев)</span><span class="sxs-lookup"><span data-stu-id="e6ba8-155">Monthly (a maximum of 12 months can be displayed)</span></span></p></li>
</ul>
<p><span data-ttu-id="e6ba8-156">Если количество значений между начальной и конечной датами превышает максимально допустимое для выбранного интервала, отображается максимальное возможное количество значений (от начальной даты и далее).</span><span class="sxs-lookup"><span data-stu-id="e6ba8-156">If the start and end dates exceed the maximum number of values allowed for the selected interval, only the maximum number of values (starting from the start date) is displayed.</span></span> <span data-ttu-id="e6ba8-157">Например, если выбрать ежедневный интервал с датой начала 7/7/2012 и датой окончания 2/28/2012, данные будут выводиться для дней 8/7/2012 12:00 – 9/7/2012 12:00 AM (то есть, всего за 31 дня).</span><span class="sxs-lookup"><span data-stu-id="e6ba8-157">For example, if you select the Daily interval with a start date of 7/7/2012 and an end date of 2/28/2012, data is displayed for the days 8/7/2012 12:00 AM to 9/7/2012 12:00 AM (that is, a total of 31 days' worth of data).</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics"></a><span data-ttu-id="e6ba8-158">Показатели</span><span class="sxs-lookup"><span data-stu-id="e6ba8-158">Metrics</span></span>

<span data-ttu-id="e6ba8-159">В следующей таблице приведены сведения, которые предоставляются в сводном отчете по конференциям ТСОП.</span><span class="sxs-lookup"><span data-stu-id="e6ba8-159">The following table lists the information in the PSTN Conference Summary Report.</span></span>

### <a name="pstn-conference-summary-report-metrics"></a><span data-ttu-id="e6ba8-160">Метрики сводного отчета по конференциям ТСОП</span><span class="sxs-lookup"><span data-stu-id="e6ba8-160">PSTN Conference Summary Report Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e6ba8-161">Имя</span><span class="sxs-lookup"><span data-stu-id="e6ba8-161">Name</span></span></th>
<th><span data-ttu-id="e6ba8-162">Поддержка сортировки</span><span class="sxs-lookup"><span data-stu-id="e6ba8-162">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="e6ba8-163">Описание</span><span class="sxs-lookup"><span data-stu-id="e6ba8-163">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e6ba8-164"><strong>Ежечасно</strong></span><span class="sxs-lookup"><span data-stu-id="e6ba8-164"><strong>Hourly</strong></span></span></p>
<p><span data-ttu-id="e6ba8-165"><strong>Ежедневно</strong></span><span class="sxs-lookup"><span data-stu-id="e6ba8-165"><strong>Daily</strong></span></span></p>
<p><span data-ttu-id="e6ba8-166"><strong>Еженедельно</strong></span><span class="sxs-lookup"><span data-stu-id="e6ba8-166"><strong>Weekly</strong></span></span></p>
<p><span data-ttu-id="e6ba8-167"><strong>Ежемесячно</strong></span><span class="sxs-lookup"><span data-stu-id="e6ba8-167"><strong>Monthly</strong></span></span></p></td>
<td><p><span data-ttu-id="e6ba8-168">Нет</span><span class="sxs-lookup"><span data-stu-id="e6ba8-168">No</span></span></p></td>
<td><p><span data-ttu-id="e6ba8-169">Указывает выбранный интервал времени.</span><span class="sxs-lookup"><span data-stu-id="e6ba8-169">Indicates the selected time interval.</span></span> <span data-ttu-id="e6ba8-170">В применимых случаях можно щелкнуть конкретный интервал времени, чтобы просмотреть подробные сведения для этого интервала.</span><span class="sxs-lookup"><span data-stu-id="e6ba8-170">Where applicable, you can click a given time interval to view detailed information for that interval.</span></span> <span data-ttu-id="e6ba8-171">Например, если вы используете ежедневный интервал и нажимайте 7/7/2012, появится Почасовая подразделение действия регистрации пользователя для этой даты.</span><span class="sxs-lookup"><span data-stu-id="e6ba8-171">For example, if you are using the Daily interval and you click 7/7/2012, you see an hourly breakdown of user registration activity for that date.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6ba8-172"><strong>Общее количество конференций ТСОП</strong></span><span class="sxs-lookup"><span data-stu-id="e6ba8-172"><strong>Total PSTN conferences</strong></span></span></p></td>
<td><p><span data-ttu-id="e6ba8-173">Нет</span><span class="sxs-lookup"><span data-stu-id="e6ba8-173">No</span></span></p></td>
<td><p><span data-ttu-id="e6ba8-174">Общее количество конференций, в которых разрешен телефонный доступ.</span><span class="sxs-lookup"><span data-stu-id="e6ba8-174">Total number conferences that allowed dial-in access.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6ba8-175"><strong>Общее количество участников</strong></span><span class="sxs-lookup"><span data-stu-id="e6ba8-175"><strong>Total participants</strong></span></span></p></td>
<td><p><span data-ttu-id="e6ba8-176">Нет</span><span class="sxs-lookup"><span data-stu-id="e6ba8-176">No</span></span></p></td>
<td><p><span data-ttu-id="e6ba8-177">Общее количество людей, принявших участие в конференциях с разрешенным телефонным доступом.</span><span class="sxs-lookup"><span data-stu-id="e6ba8-177">Total number of people who participated in conferences that allowed dial-in access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6ba8-178"><strong>Общее время аудио- и видеоконференций (в минутах)</strong></span><span class="sxs-lookup"><span data-stu-id="e6ba8-178"><strong>Total A/V conference minutes</strong></span></span></p></td>
<td><p><span data-ttu-id="e6ba8-179">Нет</span><span class="sxs-lookup"><span data-stu-id="e6ba8-179">No</span></span></p></td>
<td><p><span data-ttu-id="e6ba8-180">Общее время аудио- и видеоконференций.</span><span class="sxs-lookup"><span data-stu-id="e6ba8-180">Total amount of audio/visual conference time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6ba8-181"><strong>Общее время участия в аудио- или видеоконференции (в минутах)</strong></span><span class="sxs-lookup"><span data-stu-id="e6ba8-181"><strong>Total A/V conference participant minutes</strong></span></span></p></td>
<td><p><span data-ttu-id="e6ba8-182">Нет</span><span class="sxs-lookup"><span data-stu-id="e6ba8-182">No</span></span></p></td>
<td><p><span data-ttu-id="e6ba8-p113">Общее время, затраченное участниками в аудио- или видеоконференции. Например, если один участник потратил пять, а другой – три минуты в одной и той же аудио- или видеоконференции, то общее время участия в аудио- или видеоконференции составит восемь минут.</span><span class="sxs-lookup"><span data-stu-id="e6ba8-p113">Total amount of audio/visual participant time. For example, if one participant spent five minutes in an A/V conference and another participant spent three minutes in the same conference, the total A/V conference participant time would be eight minutes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6ba8-185"><strong>Общее количество участников ТСОП</strong></span><span class="sxs-lookup"><span data-stu-id="e6ba8-185"><strong>Total PSTN participants</strong></span></span></p></td>
<td><p><span data-ttu-id="e6ba8-186">Нет</span><span class="sxs-lookup"><span data-stu-id="e6ba8-186">No</span></span></p></td>
<td><p><span data-ttu-id="e6ba8-187">Общее количество пользователей, подключившихся по телефону к конференциям, в которых разрешен телефонный доступ.</span><span class="sxs-lookup"><span data-stu-id="e6ba8-187">Total number of users who dialed in to conferences that allowed dial-in access.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6ba8-188"><strong>Общее время участников ТСОП в минутах</strong></span><span class="sxs-lookup"><span data-stu-id="e6ba8-188"><strong>Total PSTN participant minutes</strong></span></span></p></td>
<td><p><span data-ttu-id="e6ba8-189">Нет</span><span class="sxs-lookup"><span data-stu-id="e6ba8-189">No</span></span></p></td>
<td><p><span data-ttu-id="e6ba8-p114">Общее время, затраченное на конференцию участниками с телефонным подключением. Например, если один участник с телефонным подключением провел пять минут, а другой – три минуты в одной и той же конференции, то общее время участников ТСОП составит восемь минут.</span><span class="sxs-lookup"><span data-stu-id="e6ba8-p114">Total amount of conference time spent by dial-in users. For example, if one dial-in participant spent five minutes in a conference and another participant spent three minutes in the same conference, the total PSTN participant time would be eight minutes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6ba8-192"><strong>Общее количество уникальных организаторов конференций</strong></span><span class="sxs-lookup"><span data-stu-id="e6ba8-192"><strong>Unique conference organizers</strong></span></span></p></td>
<td><p><span data-ttu-id="e6ba8-193">Нет</span><span class="sxs-lookup"><span data-stu-id="e6ba8-193">No</span></span></p></td>
<td><p><span data-ttu-id="e6ba8-p115">Общее количество пользователей, организовавших хотя бы одну конференцию с разрешенным телефонным доступом. Пользователь, организовавший несколько таких конференций, учитывается как один уникальный организатор, как те, кто организовал только одну конференцию.</span><span class="sxs-lookup"><span data-stu-id="e6ba8-p115">Total number of users who organized at least one conference that allowed dial-in access. Users who organized more than one conference are counted as one unique organizer, just like users who only organized a single conference.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="e6ba8-196">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e6ba8-196">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

