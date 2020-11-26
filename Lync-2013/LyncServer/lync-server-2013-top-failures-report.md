---
title: 'Lync Server 2013: отчет об ошибках Top'
description: 'Lync Server 2013: отчет об ошибках Top.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Top Failures Report
ms:assetid: 438942e2-580a-4b67-9d42-f116111fb26a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558640(v=OCS.15)
ms:contentKeyID: 48184021
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 768c9a99916dece9eb76877b0cd65b057697ff95
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440915"
---
# <a name="top-failures-report-in-lync-server-2013"></a><span data-ttu-id="ecba8-103">Отчет об ошибках верхнего уровня в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ecba8-103">Top Failures Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ecba8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ecba8-104">

<span> </span></span></span>

<span data-ttu-id="ecba8-105">_**Тема последнего изменения:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="ecba8-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="ecba8-p101">Отчет по основным сбоям позволяет узнать о наиболее частых сбоях и характере их изменения с течением времени. Сбои основаны на сочетании двух следующих метрик:</span><span class="sxs-lookup"><span data-stu-id="ecba8-p101">The Top Failures Report provides a look at the most-commonly reported failures and their trends over time. Failures are based on a combination of the following two metrics:</span></span>

  - <span data-ttu-id="ecba8-p102">**Код диагностики**. Уникальный идентификатор (в виде заголовка ms-diagnostics), прикрепленный к сообщению SIP. Коды диагностики предоставляют информацию, полезную при устранении проблем со звонками.</span><span class="sxs-lookup"><span data-stu-id="ecba8-p102">**Diagnostic ID**. Unique identifier (in the form of an ms-diagnostics header) that is attached to a SIP message. Diagnostic IDs provide information useful in troubleshooting call-related problems.</span></span>

  - <span data-ttu-id="ecba8-111">**Код ответа**.</span><span class="sxs-lookup"><span data-stu-id="ecba8-111">**Response code**.</span></span> <span data-ttu-id="ecba8-112">Коды ответа используются в сеансах связи SIP для ответы на запросы SIP.</span><span class="sxs-lookup"><span data-stu-id="ecba8-112">Response codes are used in SIP communication sessions to respond to SIP requests.</span></span> <span data-ttu-id="ecba8-113">Предположим, что пользователь Ken отправляет запрос INVITE пользователю Pilar Ackerman (например, пользователь Ken Myer звонит пользователю Pilar Ackerman).</span><span class="sxs-lookup"><span data-stu-id="ecba8-113">For example, suppose Ken sends the INVITE request to Pilar Ackerman (that is, suppose Ken Myer calls Pilar Ackerman).</span></span> <span data-ttu-id="ecba8-114">Если Pilar отвечает, ее телефон отправляет код ответа 200 (OK), позволяя телефону Ken узнать об ответе Pilar.</span><span class="sxs-lookup"><span data-stu-id="ecba8-114">If Pilar answers, her phone will send the response code 200 (OK), letting Ken's phone know that Pilar has answered.</span></span> <span data-ttu-id="ecba8-115">Отчет об ошибках Top содержит только коды ответов, отправленные в ответ на сбой звонка; Lync Server не отслеживает все коды ответа, выданные в ходе звонка.</span><span class="sxs-lookup"><span data-stu-id="ecba8-115">The Top Failures Report only includes response codes that were sent in response to a call failure; Lync Server does not keep track of all the response codes issued during the course of a call.</span></span>

<span data-ttu-id="ecba8-116">Приводится информация не только об общем числе сеансов, в которых возник сбой, но и об общем числе пользователей, столкнувшихся с этим сбоем.</span><span class="sxs-lookup"><span data-stu-id="ecba8-116">Information is reported not only for the total number of sessions where a failure occurred but also for the total number of users who were impacted by the failure.</span></span>

<div>

## <a name="accessing-the-top-failures-report"></a><span data-ttu-id="ecba8-117">Доступ к отчету по основным сбоям</span><span class="sxs-lookup"><span data-stu-id="ecba8-117">Accessing the Top Failures Report</span></span>

<span data-ttu-id="ecba8-118">Доступ к отчету по основным сбоям можно получить с домашней страницы отчетов по мониторингу.</span><span class="sxs-lookup"><span data-stu-id="ecba8-118">The Top Failures Report is accessed from the Monitoring Reports home page.</span></span> <span data-ttu-id="ecba8-119">Если щелкнуть метрику зарегистрированных сеансов, вы перейдете к [отчету распределение сбоев в Lync Server 2013](lync-server-2013-failure-distribution-report.md).</span><span class="sxs-lookup"><span data-stu-id="ecba8-119">Clicking the Reported sessions metric will take you to the [Failure Distribution Report in Lync Server 2013](lync-server-2013-failure-distribution-report.md).</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-top-failures-report"></a><span data-ttu-id="ecba8-120">Рекомендации по использованию отчета по основным сбоям</span><span class="sxs-lookup"><span data-stu-id="ecba8-120">Making the Best Use of the Top Failures Report</span></span>

<span data-ttu-id="ecba8-p105">Отчет по основным сбоям имеет одну необычную особенность: он позволяет одновременно выполнять фильтрацию по 5 кодам диагностики. (Обычно одновременно вы можете выполнять фильтрацию только по одному из них, например по SIP-адресу пользователя.) Чтобы выполнить фильтрацию по нескольким кодам диагностики, просто введите каждый код в поле "Diagnostic IDs" (Коды диагностики), отделяя его запятой. (При необходимости вы можете ставить после каждой запятой пробел.) Например:</span><span class="sxs-lookup"><span data-stu-id="ecba8-p105">The Top Failures Report is unusual in one regard: it allows you to filter on as many as 5 diagnostic IDs at once. (Typically you can only filter on one item – such as one user SIP address – at a time.) To filter on multiple diagnostic IDs, simply enter each ID in the Diagnostic IDs box, separating the IDs by using commas. (If you want to, you can leave a blank space after each comma.) For example:</span></span>

<span data-ttu-id="ecba8-124">1011, 2412, 1033, 52116, 1008</span><span class="sxs-lookup"><span data-stu-id="ecba8-124">1011, 2412, 1033, 52116, 1008</span></span>

<span data-ttu-id="ecba8-125">Сделайте это, и будут отображаться только неудачные звонки, в которых возник один из данных кодов диагностики.</span><span class="sxs-lookup"><span data-stu-id="ecba8-125">Do that, and only failed calls that reported at least one of those five diagnostic IDs will be displayed.</span></span>

<span data-ttu-id="ecba8-p106">Если навести указатель на код диагностики, отображается подсказка с описание его значения. Например, если навести указатель на код ответа 486, отображается следующее сообщение:</span><span class="sxs-lookup"><span data-stu-id="ecba8-p106">If you hold your mouse over a Response code you'll see a tooltip that tells you what the Response code in question means. For example, if you hold the mouse over the Response code 486 you'll see this message:</span></span>

<span data-ttu-id="ecba8-128">Busy Here (Занято).</span><span class="sxs-lookup"><span data-stu-id="ecba8-128">Busy Here.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="ecba8-129">Фильтры</span><span class="sxs-lookup"><span data-stu-id="ecba8-129">Filters</span></span>

<span data-ttu-id="ecba8-p107">Фильтры позволяют получать более адресный набор данных или просматривать полученные данные разными способами. Например, в отчете по основным сбоям можно фильтровать возвращенные данные по типу действия (одноранговый сеанс или сеанс конференц-связи) или по коду ответа SIP, выданному для неудачного сеанса. Кроме того, можно выбрать способ группирования данных. В данном случае вызовы использования по часу, дню, неделе или месяцу.</span><span class="sxs-lookup"><span data-stu-id="ecba8-p107">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. For example, the Top Failures Report enables you to filter the returned data based on such things as the activity type (peer-to-peer session or conferencing session) or by the SIP response code that accompanied the failed session. You can also choose how data should be grouped. In this case, usages are grouped by hour, day, week, or month.</span></span>

<span data-ttu-id="ecba8-134">В следующей таблице приведены фильтры, которые можно использовать с отчетом по основным сбоям.</span><span class="sxs-lookup"><span data-stu-id="ecba8-134">The following table lists the filters that you can use with the Top Failures Report.</span></span>

### <a name="top-failures-report-filters"></a><span data-ttu-id="ecba8-135">Фильтры отчета по основным сбоям</span><span class="sxs-lookup"><span data-stu-id="ecba8-135">Top Failures Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ecba8-136">Имя</span><span class="sxs-lookup"><span data-stu-id="ecba8-136">Name</span></span></th>
<th><span data-ttu-id="ecba8-137">Описание</span><span class="sxs-lookup"><span data-stu-id="ecba8-137">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ecba8-138"><strong>От</strong></span><span class="sxs-lookup"><span data-stu-id="ecba8-138"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="ecba8-p108">Начальные дата/время для временного диапазона. Чтобы просмотреть данные по часам, введите начальные дату и время следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ecba8-p108">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="ecba8-141">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="ecba8-141">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="ecba8-p109">Если вы не вводите начальное время, отчет автоматически начинается с 12:00 AM указанного дня. Чтобы просмотреть данные по дням, просто введите дату:</span><span class="sxs-lookup"><span data-stu-id="ecba8-p109">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="ecba8-144">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="ecba8-144">7/7/2012</span></span></p>
<p><span data-ttu-id="ecba8-145">Чтобы просмотреть данные за неделю или месяц, введите дату, выпадающую на любое время в рамках недели или месяца, которые вы хотите просмотреть (вам не требуется вводить первый день недели или месяца):</span><span class="sxs-lookup"><span data-stu-id="ecba8-145">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="ecba8-146">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="ecba8-146">7/3/2012</span></span></p>
<p><span data-ttu-id="ecba8-147">Недели всегда отсчитываются с воскресенья по субботу.</span><span class="sxs-lookup"><span data-stu-id="ecba8-147">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ecba8-148"><strong>До</strong></span><span class="sxs-lookup"><span data-stu-id="ecba8-148"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="ecba8-p110">Конечные дата/время для временного диапазона. Чтобы просмотреть данные по часам, введите конечные дату и время следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ecba8-p110">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="ecba8-151">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="ecba8-151">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="ecba8-p111">Если вы не вводите конечное время, отчет автоматически заканчивается в 12:00 AM указанного дня. Чтобы просмотреть данные по дням, просто введите дату:</span><span class="sxs-lookup"><span data-stu-id="ecba8-p111">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="ecba8-154">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="ecba8-154">7/7/2012</span></span></p>
<p><span data-ttu-id="ecba8-155">Чтобы просмотреть данные за неделю или месяц, введите дату, выпадающую на любое время в рамках недели или месяца, которые вы хотите просмотреть (вам не требуется вводить первый день недели или месяца):</span><span class="sxs-lookup"><span data-stu-id="ecba8-155">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="ecba8-156">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="ecba8-156">7/3/2012</span></span></p>
<p><span data-ttu-id="ecba8-157">Недели всегда отсчитываются с воскресенья по субботу.</span><span class="sxs-lookup"><span data-stu-id="ecba8-157">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ecba8-158"><strong>Activity type (Тип активности)</strong></span><span class="sxs-lookup"><span data-stu-id="ecba8-158"><strong>Activity type</strong></span></span></p></td>
<td><p><span data-ttu-id="ecba8-p112">Тип активности. Выберите одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="ecba8-p112">Type of activity. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="ecba8-161">[All] (Все)</span><span class="sxs-lookup"><span data-stu-id="ecba8-161">[All]</span></span></p></li>
<li><p><span data-ttu-id="ecba8-162">Одноранговая</span><span class="sxs-lookup"><span data-stu-id="ecba8-162">Peer-to-peer</span></span></p></li>
<li><p><span data-ttu-id="ecba8-163">Конференция</span><span class="sxs-lookup"><span data-stu-id="ecba8-163">Conference</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ecba8-164"><strong>Modality (Модальность)</strong></span><span class="sxs-lookup"><span data-stu-id="ecba8-164"><strong>Modality</strong></span></span></p></td>
<td><p><span data-ttu-id="ecba8-165">В настоящее время доступен только параметр <strong>[All]</strong> (Все).</span><span class="sxs-lookup"><span data-stu-id="ecba8-165">At this time the only option available is <strong>[All]</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ecba8-166"><strong>Pool (Пул)</strong></span><span class="sxs-lookup"><span data-stu-id="ecba8-166"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="ecba8-p113">Полное доменное имя пула регистратора или пограничного сервера. Можно выбрать отдельный пул или нажать <strong>[Все]</strong>, чтобы просмотреть данные для всех пулов. Этот раскрывающийся список автоматически заполняется на основе записей в базе данных.</span><span class="sxs-lookup"><span data-stu-id="ecba8-p113">Fully qualified domain name (FQDN) of the Registrar pool or Edge Server. You can either select an individual pool or click <strong>[All]</strong> to view data for all the pools. This drop-down list is automatically populated for you based on the records in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ecba8-170"><strong>Категория</strong></span><span class="sxs-lookup"><span data-stu-id="ecba8-170"><strong>Category</strong></span></span></p></td>
<td><p><span data-ttu-id="ecba8-p114">Тип возникшего сбоя. Выберите одно из следующих действий:</span><span class="sxs-lookup"><span data-stu-id="ecba8-p114">Type of failure experienced. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="ecba8-173">Как ожидаемый сбой, так и непредвиденный сбой</span><span class="sxs-lookup"><span data-stu-id="ecba8-173">Both expected and unexpected failure</span></span></p></li>
<li><p><span data-ttu-id="ecba8-174">Unexpected failure (Неожиданный сбой)</span><span class="sxs-lookup"><span data-stu-id="ecba8-174">Unexpected failure</span></span></p></li>
</ul>
<p><span data-ttu-id="ecba8-175">&quot;Ожидаемый сбой &quot; — это сбой, который должен выполняться.</span><span class="sxs-lookup"><span data-stu-id="ecba8-175">An &quot;expected failure&quot; is a failure that is expected to happen.</span></span> <span data-ttu-id="ecba8-176">Например, если пользователь установил статус «Не беспокоить», то ожидаемое, что все вызовы этого пользователя завершатся неудачно.</span><span class="sxs-lookup"><span data-stu-id="ecba8-176">For example, if a user has set his or her status to Do Not Disturb you would expect any call to that user to fail.</span></span> <span data-ttu-id="ecba8-177">Произошла &quot; непредвиденная ошибка &quot; , возникающая в том, что может выглядеть как подсистема, которая в противном случае является работоспособной.</span><span class="sxs-lookup"><span data-stu-id="ecba8-177">An &quot;unexpected failure&quot; is a failure that occurs in what would appear to be an otherwise healthy system.</span></span> <span data-ttu-id="ecba8-178">Например, вызов не должен прерываться, если вызывающий абонент помещается на удержание.</span><span class="sxs-lookup"><span data-stu-id="ecba8-178">For example, a call should not be terminated if the caller is placed on hold.</span></span> <span data-ttu-id="ecba8-179">В этом случае это считается непредвиденным сбоем.</span><span class="sxs-lookup"><span data-stu-id="ecba8-179">If that occurs, that would be flagged as an unexpected failure.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ecba8-180"><strong>Response code (Код ответа)</strong></span><span class="sxs-lookup"><span data-stu-id="ecba8-180"><strong>Response code</strong></span></span></p></td>
<td><p><span data-ttu-id="ecba8-p116">Код ответа SIP, отправленный при сбое конференции. Введите полный код ответа, например:</span><span class="sxs-lookup"><span data-stu-id="ecba8-p116">SIP response code sent when the conference failed. Enter the entire response code For example:</span></span></p>
<p><span data-ttu-id="ecba8-183">400</span><span class="sxs-lookup"><span data-stu-id="ecba8-183">400</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ecba8-184"><strong>Diagnostic ID (ИД диагностики)</strong></span><span class="sxs-lookup"><span data-stu-id="ecba8-184"><strong>Diagnostic ID</strong></span></span></p></td>
<td><p><span data-ttu-id="ecba8-p117">Прикрепленный к SIP-сообщению уникальный идентификатор (в форме заголовка ms-diagnostics), который часто содержит информацию, полезную при поиске и устранении ошибок. Заголовки диагностики не являются обязательными (можно иметь сеансы SIP без таких заголовков), а идентификаторы диагностики указываются только для сеансов, в которых возникли какие-либо проблемы.</span><span class="sxs-lookup"><span data-stu-id="ecba8-p117">Unique identifier (in the form of an ms-diagnostics header) attached to a SIP message that often provides information useful in troubleshooting errors. Diagnostics headers are optional (it is possible to have SIP sessions that do not include these headers), and diagnostic IDs are reported only for sessions that experienced problems of some kind.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics"></a><span data-ttu-id="ecba8-187">Показатели</span><span class="sxs-lookup"><span data-stu-id="ecba8-187">Metrics</span></span>

<span data-ttu-id="ecba8-188">Следующая таблица содержит сведения, приведенные в отчете по основным сбоям.</span><span class="sxs-lookup"><span data-stu-id="ecba8-188">The following table lists the information provided in the Top Failures Report.</span></span>

### <a name="top-failures-report-metrics"></a><span data-ttu-id="ecba8-189">Метрики отчета по основным сбоям</span><span class="sxs-lookup"><span data-stu-id="ecba8-189">Top Failures Report Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ecba8-190">Имя</span><span class="sxs-lookup"><span data-stu-id="ecba8-190">Name</span></span></th>
<th><span data-ttu-id="ecba8-191">Поддержка сортировки</span><span class="sxs-lookup"><span data-stu-id="ecba8-191">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="ecba8-192">Описание</span><span class="sxs-lookup"><span data-stu-id="ecba8-192">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ecba8-193"><strong>Rank (Ранг)</strong></span><span class="sxs-lookup"><span data-stu-id="ecba8-193"><strong>Rank</strong></span></span></p></td>
<td><p><span data-ttu-id="ecba8-194">Да</span><span class="sxs-lookup"><span data-stu-id="ecba8-194">Yes</span></span></p></td>
<td><p><span data-ttu-id="ecba8-195">Относительный ранг, основанный на количестве включенных в отчет сеансов.</span><span class="sxs-lookup"><span data-stu-id="ecba8-195">Relative rank based on the number of reported sessions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ecba8-196"><strong>Reported sessions (Отчетные сеансы)</strong></span><span class="sxs-lookup"><span data-stu-id="ecba8-196"><strong>Reported sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="ecba8-197">Да</span><span class="sxs-lookup"><span data-stu-id="ecba8-197">Yes</span></span></p></td>
<td><p><span data-ttu-id="ecba8-198">Общее число неудачных сеансов на основе кода диагностики и кода ответа SIP.</span><span class="sxs-lookup"><span data-stu-id="ecba8-198">Total number of failed sessions based on diagnostic ID and SIP response code.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ecba8-199"><strong>Users impacted (Затронутые пользователи)</strong></span><span class="sxs-lookup"><span data-stu-id="ecba8-199"><strong>Users impacted</strong></span></span></p></td>
<td><p><span data-ttu-id="ecba8-200">Да</span><span class="sxs-lookup"><span data-stu-id="ecba8-200">Yes</span></span></p></td>
<td><p><span data-ttu-id="ecba8-201">Общее число пользователей, столкнувшихся с неудачным сеансом.</span><span class="sxs-lookup"><span data-stu-id="ecba8-201">Total number of users affected by the failed session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ecba8-202"><strong>Failure information (Информация о сбое)</strong></span><span class="sxs-lookup"><span data-stu-id="ecba8-202"><strong>Failure information</strong></span></span></p></td>
<td><p><span data-ttu-id="ecba8-203">Нет</span><span class="sxs-lookup"><span data-stu-id="ecba8-203">No</span></span></p></td>
<td><p><span data-ttu-id="ecba8-204">Подробные сведения о сбое, включая код диагностики, код ответа SIP и описание причины сбоя сеанса.</span><span class="sxs-lookup"><span data-stu-id="ecba8-204">Detailed information about the failure, including diagnostic ID, SIP response code, and description of why the session failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ecba8-205"><strong>Trend in the past (Прошлая тенденция)</strong></span><span class="sxs-lookup"><span data-stu-id="ecba8-205"><strong>Trend in the past</strong></span></span></p></td>
<td><p><span data-ttu-id="ecba8-206">Нет</span><span class="sxs-lookup"><span data-stu-id="ecba8-206">No</span></span></p></td>
<td><p><span data-ttu-id="ecba8-207">График, показывающий зависимость неудачных сеансов от времени.</span><span class="sxs-lookup"><span data-stu-id="ecba8-207">Graphs failed sessions over time.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="ecba8-208">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ecba8-208">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

