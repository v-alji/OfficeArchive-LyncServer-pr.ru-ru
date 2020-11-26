---
title: 'Lync Server 2013: отчет о соотношении качества мультимедиа'
description: 'Lync Server 2013: отчет о соотношении качества мультимедиа.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Media Quality Comparison Report
ms:assetid: c1d0b5a8-98ff-455a-b78b-a05a21cf066d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205236(v=OCS.15)
ms:contentKeyID: 48185317
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b2c4c5c948d167ce5210f9814c4e0625ffaa9152
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425684"
---
# <a name="media-quality-comparison-report-in-lync-server-2013"></a><span data-ttu-id="138da-103">Отчет о сравнении качества мультимедиа в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="138da-103">Media Quality Comparison Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="138da-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="138da-104">

<span> </span></span></span>

<span data-ttu-id="138da-105">_**Тема последнего изменения:** 2014-04-22_</span><span class="sxs-lookup"><span data-stu-id="138da-105">_**Topic Last Modified:** 2014-04-22_</span></span>

<span data-ttu-id="138da-106">Сравнительный отчет качества мультимедиа-данных позволяет сравнить значения качества звонков для различных типов аудиозвонков (например, звонков, выполненных через беспроводные сети и звонков, выполненных через проводное соединение).</span><span class="sxs-lookup"><span data-stu-id="138da-106">The Media Quality Comparison Report enables you to compare call quality values for different types of audio calls (for example, calls made over a wireless network vs. calls made across a wired connection).</span></span>

<div>

## <a name="accessing-the-media-quality-comparison-report"></a><span data-ttu-id="138da-107">Доступ к сравнительному отчету качества мультимедиа-данных</span><span class="sxs-lookup"><span data-stu-id="138da-107">Accessing the Media Quality Comparison Report</span></span>

<span data-ttu-id="138da-108">Сравнительный отчет качества мультимедиа-данных доступен на домашней странице отчетов мониторинга.</span><span class="sxs-lookup"><span data-stu-id="138da-108">The Media Quality Comparison Report is accessed from the Monitoring Reports home page.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="138da-109">Фильтры</span><span class="sxs-lookup"><span data-stu-id="138da-109">Filters</span></span>

<span data-ttu-id="138da-p101">Фильтры предоставляют способ получения более точно настроенного набора данных или просмотра возвращенных данных различными способами. В следующей таблице перечислены фильтры, которые можно использовать в сравнительном отчете качества мультимедиа-данных.</span><span class="sxs-lookup"><span data-stu-id="138da-p101">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. The following table lists the filters that you can use with the Media Quality Comparison Report.</span></span>

### <a name="media-quality-comparison-report-filters"></a><span data-ttu-id="138da-112">Фильтры сравнительного отчета качества мультимедиа-данных</span><span class="sxs-lookup"><span data-stu-id="138da-112">Media Quality Comparison Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="138da-113">Имя</span><span class="sxs-lookup"><span data-stu-id="138da-113">Name</span></span></th>
<th><span data-ttu-id="138da-114">Описание</span><span class="sxs-lookup"><span data-stu-id="138da-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="138da-115"><strong>От</strong></span><span class="sxs-lookup"><span data-stu-id="138da-115"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="138da-p102">Начальные дата/время для временного диапазона. Чтобы просмотреть данные по часам, введите начальные дату и время следующим образом:</span><span class="sxs-lookup"><span data-stu-id="138da-p102">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="138da-118">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="138da-118">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="138da-p103">Если вы не вводите начальное время, отчет автоматически начинается с 12:00 AM указанного дня. Чтобы просмотреть данные по дням, просто введите дату:</span><span class="sxs-lookup"><span data-stu-id="138da-p103">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="138da-121">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="138da-121">7/7/2012</span></span></p>
<p><span data-ttu-id="138da-122">Чтобы просмотреть данные за неделю или месяц, введите дату, выпадающую на любое время в рамках недели или месяца, которые вы хотите просмотреть (вам не требуется вводить первый день недели или месяца):</span><span class="sxs-lookup"><span data-stu-id="138da-122">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="138da-123">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="138da-123">7/3/2012</span></span></p>
<p><span data-ttu-id="138da-124">Недели всегда отсчитываются с воскресенья по субботу.</span><span class="sxs-lookup"><span data-stu-id="138da-124">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="138da-125"><strong>До</strong></span><span class="sxs-lookup"><span data-stu-id="138da-125"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="138da-p104">Конечные дата/время для временного диапазона. Чтобы просмотреть данные по часам, введите конечные дату и время следующим образом:</span><span class="sxs-lookup"><span data-stu-id="138da-p104">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="138da-128">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="138da-128">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="138da-p105">Если вы не вводите конечное время, отчет автоматически заканчивается в 12:00 AM указанного дня. Чтобы просмотреть данные по дням, просто введите дату:</span><span class="sxs-lookup"><span data-stu-id="138da-p105">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="138da-131">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="138da-131">7/7/2012</span></span></p>
<p><span data-ttu-id="138da-132">Чтобы просмотреть данные за неделю или месяц, введите дату, выпадающую на любое время в рамках недели или месяца, которые вы хотите просмотреть (вам не требуется вводить первый день недели или месяца):</span><span class="sxs-lookup"><span data-stu-id="138da-132">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="138da-133">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="138da-133">7/3/2012</span></span></p>
<p><span data-ttu-id="138da-134">Недели всегда отсчитываются с воскресенья по субботу.</span><span class="sxs-lookup"><span data-stu-id="138da-134">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="138da-135"><strong>Звонки</strong></span><span class="sxs-lookup"><span data-stu-id="138da-135"><strong>Calls</strong></span></span></p></td>
<td><p><span data-ttu-id="138da-p106">Тип звонка, который будет использоваться в качестве основного элемента для сравнения. Допускаются следующие значения:</span><span class="sxs-lookup"><span data-stu-id="138da-p106">Type of call to be used as the main comparison item. Allowed values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="138da-138">[All] (Все)</span><span class="sxs-lookup"><span data-stu-id="138da-138">[All]</span></span></p></li>
<li><p><span data-ttu-id="138da-139">Внешний</span><span class="sxs-lookup"><span data-stu-id="138da-139">External</span></span></p></li>
<li><p><span data-ttu-id="138da-140">Internal</span><span class="sxs-lookup"><span data-stu-id="138da-140">Internal</span></span></p></li>
<li><p><span data-ttu-id="138da-141">VPN</span><span class="sxs-lookup"><span data-stu-id="138da-141">VPN</span></span></p></li>
<li><p><span data-ttu-id="138da-142">Не VPN</span><span class="sxs-lookup"><span data-stu-id="138da-142">Non-VPN</span></span></p></li>
<li><p><span data-ttu-id="138da-143">Проводная</span><span class="sxs-lookup"><span data-stu-id="138da-143">Wired</span></span></p></li>
<li><p><span data-ttu-id="138da-144">Беспроводная</span><span class="sxs-lookup"><span data-stu-id="138da-144">Wireless</span></span></p></li>
<li><p><span data-ttu-id="138da-145">Внешние и проводные</span><span class="sxs-lookup"><span data-stu-id="138da-145">External and wired</span></span></p></li>
<li><p><span data-ttu-id="138da-146">Внешние и беспроводные</span><span class="sxs-lookup"><span data-stu-id="138da-146">External and wireless</span></span></p></li>
<li><p><span data-ttu-id="138da-147">Внешние и VPN</span><span class="sxs-lookup"><span data-stu-id="138da-147">External and VPN</span></span></p></li>
<li><p><span data-ttu-id="138da-148">Внешние и не VPN</span><span class="sxs-lookup"><span data-stu-id="138da-148">External and non-VPN</span></span></p></li>
<li><p><span data-ttu-id="138da-149">Внутренние и проводные</span><span class="sxs-lookup"><span data-stu-id="138da-149">Internal and wired</span></span></p></li>
<li><p><span data-ttu-id="138da-150">Внутренние и беспроводные</span><span class="sxs-lookup"><span data-stu-id="138da-150">Internal and wireless</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="138da-151"><strong>Сравнить со звонками</strong></span><span class="sxs-lookup"><span data-stu-id="138da-151"><strong>Compare with calls</strong></span></span></p></td>
<td><p><span data-ttu-id="138da-p107">Тип звонка, который будет использоваться в качестве второго элемента для сравнения. Допускаются следующие значения:</span><span class="sxs-lookup"><span data-stu-id="138da-p107">Type of call to be used as the secondary comparison item. Allowed values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="138da-154">[All] (Все)</span><span class="sxs-lookup"><span data-stu-id="138da-154">[All]</span></span></p></li>
<li><p><span data-ttu-id="138da-155">Внешний</span><span class="sxs-lookup"><span data-stu-id="138da-155">External</span></span></p></li>
<li><p><span data-ttu-id="138da-156">Internal</span><span class="sxs-lookup"><span data-stu-id="138da-156">Internal</span></span></p></li>
<li><p><span data-ttu-id="138da-157">VPN</span><span class="sxs-lookup"><span data-stu-id="138da-157">VPN</span></span></p></li>
<li><p><span data-ttu-id="138da-158">Не VPN</span><span class="sxs-lookup"><span data-stu-id="138da-158">Non-VPN</span></span></p></li>
<li><p><span data-ttu-id="138da-159">Проводная</span><span class="sxs-lookup"><span data-stu-id="138da-159">Wired</span></span></p></li>
<li><p><span data-ttu-id="138da-160">Беспроводная</span><span class="sxs-lookup"><span data-stu-id="138da-160">Wireless</span></span></p></li>
<li><p><span data-ttu-id="138da-161">Внешние и проводные</span><span class="sxs-lookup"><span data-stu-id="138da-161">External and wired</span></span></p></li>
<li><p><span data-ttu-id="138da-162">Внешние и беспроводные</span><span class="sxs-lookup"><span data-stu-id="138da-162">External and wireless</span></span></p></li>
<li><p><span data-ttu-id="138da-163">Внешние и VPN</span><span class="sxs-lookup"><span data-stu-id="138da-163">External and VPN</span></span></p></li>
<li><p><span data-ttu-id="138da-164">Внешние и не VPN</span><span class="sxs-lookup"><span data-stu-id="138da-164">External and non-VPN</span></span></p></li>
<li><p><span data-ttu-id="138da-165">Внутренние и проводные</span><span class="sxs-lookup"><span data-stu-id="138da-165">Internal and wired</span></span></p></li>
<li><p><span data-ttu-id="138da-166">Внутренние и беспроводные</span><span class="sxs-lookup"><span data-stu-id="138da-166">Internal and wireless</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="138da-167"><strong>Интервал</strong></span><span class="sxs-lookup"><span data-stu-id="138da-167"><strong>Interval</strong></span></span></p></td>
<td><p><span data-ttu-id="138da-p108">Временной интервал. Выберите одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="138da-p108">Time interval. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="138da-170">Ежечасно (можно отобразить не более 25 часов)</span><span class="sxs-lookup"><span data-stu-id="138da-170">Hourly (a maximum of 25 hours can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="138da-171">Ежедневно (можно отобразить не более 31 дня)</span><span class="sxs-lookup"><span data-stu-id="138da-171">Daily (a maximum of 31 days can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="138da-172">Еженедельно (можно отобразить не более 12 недель)</span><span class="sxs-lookup"><span data-stu-id="138da-172">Weekly (a maximum of 12 weeks can be displayed)</span></span></p></li>
</ul>
<p><span data-ttu-id="138da-173">Если число значений между начальной и конечной датами превышает максимальное допустимое для выбранного интервала, отображается максимальное возможное число значений (с начальной даты).</span><span class="sxs-lookup"><span data-stu-id="138da-173">If the start and end dates exceed the maximum number of values allowed for the selected interval, only the maximum number of values (starting from the start date) is displayed.</span></span> <span data-ttu-id="138da-174">Например, если выбрать ежедневный интервал с датой начала 7/7/2012 и датой окончания 2/28/2012, данные будут выводиться для дней 8/7/2012 12:00 – 9/7/2012 12:00 AM (то есть, всего за 31 дня).</span><span class="sxs-lookup"><span data-stu-id="138da-174">For example, if you select the Daily interval with a start date of 7/7/2012 and an end date of 2/28/2012, data is displayed for the days 8/7/2012 12:00 AM to 9/7/2012 12:00 AM (that is, a total of 31 days' worth of data).</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics"></a><span data-ttu-id="138da-175">Показатели</span><span class="sxs-lookup"><span data-stu-id="138da-175">Metrics</span></span>

<span data-ttu-id="138da-176">В следующей таблице приведены сведения, предоставляемые сравнительным отчетом качества мультимедиа-данных</span><span class="sxs-lookup"><span data-stu-id="138da-176">The following table lists the information provided in the Media Quality Comparison Report.</span></span>

### <a name="media-quality-comparison-report-metrics"></a><span data-ttu-id="138da-177">Метрики сравнительного отчета качества мультимедиа-данных</span><span class="sxs-lookup"><span data-stu-id="138da-177">Media Quality Comparison Report Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="138da-178">Имя</span><span class="sxs-lookup"><span data-stu-id="138da-178">Name</span></span></th>
<th><span data-ttu-id="138da-179">Поддержка сортировки</span><span class="sxs-lookup"><span data-stu-id="138da-179">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="138da-180">Описание</span><span class="sxs-lookup"><span data-stu-id="138da-180">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="138da-181"><strong>Громкость вызова</strong></span><span class="sxs-lookup"><span data-stu-id="138da-181"><strong>Call volume</strong></span></span></p></td>
<td><p><span data-ttu-id="138da-182">Нет</span><span class="sxs-lookup"><span data-stu-id="138da-182">No</span></span></p></td>
<td><p><span data-ttu-id="138da-183">Полное число звонков.</span><span class="sxs-lookup"><span data-stu-id="138da-183">Total number of calls.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="138da-184"><strong>Падение качества (средняя оценка)</strong></span><span class="sxs-lookup"><span data-stu-id="138da-184"><strong>Degradation (MOS)</strong></span></span></p></td>
<td><p><span data-ttu-id="138da-185">Нет</span><span class="sxs-lookup"><span data-stu-id="138da-185">No</span></span></p></td>
<td><p><span data-ttu-id="138da-186">Среднее значение числа MOS (средней экспертной оценки разборчивости речи), показывающей ухудшение качества связи во время звонка.</span><span class="sxs-lookup"><span data-stu-id="138da-186">Average amount of MOS (mean opinion score) degradation experienced during a call.</span></span> <span data-ttu-id="138da-187">Значения ухудшения качества могут находиться в диапазоне от 0,0 до 5,0; значение 0,5 или ниже соответствует приемлемому ухудшению.</span><span class="sxs-lookup"><span data-stu-id="138da-187">Degradation values can range from a low of 0.0 to a high of 5.0; a value of 0.5 or less represents acceptable degradation.</span></span> <span data-ttu-id="138da-188">Исторически средние экспертные оценки разборчивости речи вычислялись при помощи пользователей, которые оценивали качество звонка по шкале от 1 до 5.</span><span class="sxs-lookup"><span data-stu-id="138da-188">Historically, mean opinion scores were calculated by having users rate the quality of a call on a scale of 1-to-5.</span></span> <span data-ttu-id="138da-189">Lync Server использует набор алгоритмов для прогнозирования того, как пользователи будут оценены при звонке.</span><span class="sxs-lookup"><span data-stu-id="138da-189">Lync Server uses a set of algorithms to predict how users would have rated a call.</span></span></p>
<p><span data-ttu-id="138da-p111">Высокие значения ухудшения могут быть вызваны перегрузкой; недостаточной пропускной способностью; перегрузкой беспроводной сети или интерференцией; перегрузкой сервера мультимедиа или конечной точки. Сильное ухудшение приводит к повреждению или потере аудиосигнала.</span><span class="sxs-lookup"><span data-stu-id="138da-p111">High degradation values can be caused by congestion; lack of bandwidth; wireless congestion or interference, or an overloaded media server or endpoint. High degradation results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="138da-192"><strong>Процент звонков низкого качества</strong></span><span class="sxs-lookup"><span data-stu-id="138da-192"><strong>Poor call percentage</strong></span></span></p></td>
<td><p><span data-ttu-id="138da-193">Нет</span><span class="sxs-lookup"><span data-stu-id="138da-193">No</span></span></p></td>
<td><p><span data-ttu-id="138da-p112">Полное число звонков, классифицированных как неудовлетворительные. Неудовлетворительный звонок — это любой звонок, в котором хотя бы одна измеренная метрика превысила допустимое значение (например, звонок, подверженный слишком сильному дрожанию).</span><span class="sxs-lookup"><span data-stu-id="138da-p112">The total number of calls classified as poor. A poor call is any call which at least one of the measured metrics exceeded the allowed value (for example, a call that experienced excessive jitter).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="138da-196"><strong>Круговой путь (мс)</strong></span><span class="sxs-lookup"><span data-stu-id="138da-196"><strong>Round trip (ms)</strong></span></span></p></td>
<td><p><span data-ttu-id="138da-197">Нет</span><span class="sxs-lookup"><span data-stu-id="138da-197">No</span></span></p></td>
<td><p><span data-ttu-id="138da-p113">Среднее время (в миллисекундах), необходимое для перемещения пакета Real-Time Transport Protocol в другую конечную точку и его возврата. Приемлемым считается время двусторонней передачи, равное 200 мс (или менее).</span><span class="sxs-lookup"><span data-stu-id="138da-p113">Average amount of (in milliseconds) required for a Real-Time Transport Protocol packet to travel to another endpoint and then back. Round-trip times of 200 milliseconds or less are considered of acceptable quality.</span></span></p>
<p><span data-ttu-id="138da-p114">Высокие значения времени двусторонней передачи могут быть обусловлены международной маршрутизацией вызовов, неправильной конфигурацией маршрутизации или перегрузкой сервера-посредника. Длительное время двусторонней передачи приводит к возникновению проблем при двусторонних аудиоразговорах в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="138da-p114">High round-trip values can be caused by international call routing; a routing misconfiguration; or an overloaded media server. High round-trip times result in difficulties with two-way, real-time audio conversations.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="138da-202"><strong>Потеря пакетов</strong></span><span class="sxs-lookup"><span data-stu-id="138da-202"><strong>Packet loss</strong></span></span></p></td>
<td><p><span data-ttu-id="138da-203">Нет</span><span class="sxs-lookup"><span data-stu-id="138da-203">No</span></span></p></td>
<td><p><span data-ttu-id="138da-p115">Средняя частота потери пакетов RTP. (Потеря пакетов происходит, когда пакеты RTP (Real-Time Transport Protocol — протокол, используемый для передачи аудио- и видеопакетов через Интернет) не достигают места назначения.) Высокие показатели потерь обычно вызваны перегрузкой, недостаточной полосой пропускания, помехами или перегрузкой беспроводной сети, а также перегрузкой сервера-посредника. Потеря пакетов обычно приводит к искажению звука или потере аудиосигналов.</span><span class="sxs-lookup"><span data-stu-id="138da-p115">Average rate of Real-Time Transport Protocol (RTP) packet loss. (Packet loss occurs when RTP packets, a protocol used for transmitting audio and video across the Internet, failed to reach their destination.) High loss rates are generally caused by congestion; lack of bandwidth; wireless congestion or interference; or an overloaded media server. Packet loss typically results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="138da-207"><strong>Дрожание (мс)</strong></span><span class="sxs-lookup"><span data-stu-id="138da-207"><strong>Jitter (ms)</strong></span></span></p></td>
<td><p><span data-ttu-id="138da-208">Нет</span><span class="sxs-lookup"><span data-stu-id="138da-208">No</span></span></p></td>
<td><p><span data-ttu-id="138da-209">Среднее значение колебаний, зарегистрированных между прибытиями пакетов RTP.</span><span class="sxs-lookup"><span data-stu-id="138da-209">Average jitter detected between RTP packet arrivals.</span></span> <span data-ttu-id="138da-210">(Колебание — это мера &quot; shakiness &quot; звонка). Обычно значения с высокой степенью колебаний заключаются в результате перегруженности или перегруженного сервера мультимедиа, что приводит к искажению или потере звука.</span><span class="sxs-lookup"><span data-stu-id="138da-210">(Jitter is a measure of the &quot;shakiness&quot; of a call.) High jitter values are typically caused by congestion or an overloaded media server, and result in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="138da-211"><strong>Степень маскированных аудиообразцов</strong></span><span class="sxs-lookup"><span data-stu-id="138da-211"><strong>Healer concealed ratio</strong></span></span></p></td>
<td><p><span data-ttu-id="138da-212">Нет</span><span class="sxs-lookup"><span data-stu-id="138da-212">No</span></span></p></td>
<td><p><span data-ttu-id="138da-p117">Средняя степень маскированных аудиообразцов по отношению к общему числу образцов. (Маскирование аудио - это методика, которая применяется для сглаживания оборванной передачи, которая обычно происходит при потери сетевых пакетов). Большие значения обозначают частое применение данной методики, вызванной из-за потери пакетов или искажений сигнала.</span><span class="sxs-lookup"><span data-stu-id="138da-p117">Average ratio of concealed audio samples to the total to the total number of samples. (A concealed audio sample is a technique used to smooth out the abrupt transition that would usually be caused by dropped network packets.) High values indicate significant levels of loss concealment applied caused by packet loss or jitter, and results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="138da-215"><strong>Степень растянутых образцов</strong></span><span class="sxs-lookup"><span data-stu-id="138da-215"><strong>Healer stretched ratio</strong></span></span></p></td>
<td><p><span data-ttu-id="138da-216">Нет</span><span class="sxs-lookup"><span data-stu-id="138da-216">No</span></span></p></td>
<td><p><span data-ttu-id="138da-p118">Средняя степень растянутых аудиообразцов по отношению к общему числу образцов. (Растягивание аудиопакета - это методика, которая применяется для поддержания качества звонка при обнаружении потери сетевого пакета). Большие значения обозначают частое применение данной методики, вызванное большими искажениями – аудиосигнал звучит как роботизированный.</span><span class="sxs-lookup"><span data-stu-id="138da-p118">Average ratio of stretched audio samples to the total to the total number of samples. (Stretched audio is audio that has been expanded to help maintain call quality when a dropped network packet has been detected.) High values indicate significant levels of sample stretching caused by jitter, and result in audio sounding robotic or distorted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="138da-219"><strong>Степень сжатых аудиообразцов</strong></span><span class="sxs-lookup"><span data-stu-id="138da-219"><strong>Healer compressed ratio</strong></span></span></p></td>
<td><p><span data-ttu-id="138da-220">Нет</span><span class="sxs-lookup"><span data-stu-id="138da-220">No</span></span></p></td>
<td><p><span data-ttu-id="138da-p119">Средняя степень растянутых аудиообразцов по отношению к общему числу образцов. (Сжатие аудиопакета - это методика, которая применяется для поддержания качества звонка при обнаружении потери сетевого пакета). Большие значения обозначают частое применение данной методики, вызванное большими искажениями – аудиосигнал звучит как ускоренный или искаженный.</span><span class="sxs-lookup"><span data-stu-id="138da-p119">Average ratio of compressed audio samples to the total number of samples. (Compressed audio is audio that has been compressed to help maintain call quality when a dropped network packet has been detected.) High values indicate significant levels of sample compression caused by jitter, and result in audio sounding accelerated or distorted.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="138da-223">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="138da-223">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

