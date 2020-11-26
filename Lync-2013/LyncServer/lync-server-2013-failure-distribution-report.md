---
title: 'Lync Server 2013: отчет о распределении сбоев'
description: 'Lync Server 2013: отчет о распределении отказов.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Failure Distribution Report
ms:assetid: 365c7beb-24d4-40f5-92e7-4978b9688916
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558635(v=OCS.15)
ms:contentKeyID: 48183849
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f5a87f779f87d6b7002fa108f1969c33739eed9b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428218"
---
# <a name="failure-distribution-report-in-lync-server-2013"></a><span data-ttu-id="49a32-103">Отчет о распределении отказов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="49a32-103">Failure Distribution Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="49a32-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="49a32-104">

<span> </span></span></span>

<span data-ttu-id="49a32-105">_**Тема последнего изменения:** 2012-10-21_</span><span class="sxs-lookup"><span data-stu-id="49a32-105">_**Topic Last Modified:** 2012-10-21_</span></span>

<span data-ttu-id="49a32-106">В отчете о распределении сбоев неудачные сеансы оцениваются в следующих категориях:</span><span class="sxs-lookup"><span data-stu-id="49a32-106">The Failure Distribution Report ranks failed sessions in the following categories:</span></span>

  - <span data-ttu-id="49a32-107">Самые распространенные причины диагностики</span><span class="sxs-lookup"><span data-stu-id="49a32-107">Top diagnostic reasons</span></span>

  - <span data-ttu-id="49a32-108">Самые распространенные модальности</span><span class="sxs-lookup"><span data-stu-id="49a32-108">Top modalities</span></span>

  - <span data-ttu-id="49a32-109">Самые распространенные пулы</span><span class="sxs-lookup"><span data-stu-id="49a32-109">Top pools</span></span>

  - <span data-ttu-id="49a32-110">Самые распространенные источники</span><span class="sxs-lookup"><span data-stu-id="49a32-110">Top sources</span></span>

  - <span data-ttu-id="49a32-111">Самые распространенные компоненты</span><span class="sxs-lookup"><span data-stu-id="49a32-111">Top components</span></span>

  - <span data-ttu-id="49a32-112">Самые распространенные вызывающие пользователи</span><span class="sxs-lookup"><span data-stu-id="49a32-112">Top from users</span></span>

  - <span data-ttu-id="49a32-113">Самые распространенные вызываемые пользователи</span><span class="sxs-lookup"><span data-stu-id="49a32-113">Top to users</span></span>

  - <span data-ttu-id="49a32-114">самые распространенные вызывающие агенты пользователей.</span><span class="sxs-lookup"><span data-stu-id="49a32-114">Top from user agents</span></span>

<span data-ttu-id="49a32-p101">С помощью этих категорий вы можете точно определить, где именно возникла проблема (а в некоторых случаях и причину ее возникновения). Предположим, что вы записали 242 аудио- или видеосеанса с ошибками за день. В отчете о распределении сбоев может быть показано, что 237 неудачных сеансов состоялись в пуле Дублин. Это дает вам хорошую отправную точку для отслеживания и диагностики причин этих сбоев. Если выбрать пул Дублин в категории **Основные пулы**, вы увидите отчет о распределении сбоев только для этого пула. Затем вы можете начать анализировать, почему в пуле Дублин было так много проблем.</span><span class="sxs-lookup"><span data-stu-id="49a32-p101">You can use these categories to determine exactly where a problem is occurring and, in some cases, why the problem is occurring. For example, suppose you recorded 242 failed audio/video sessions during a given day. If you look at the Failure Distribution Report, it might show that 237 of those failed sessions took place in your Dublin pool. That gives you a good place to start when it comes to tracking down and diagnosing the causes behind those failures. If you click on the Dublin pool under the **Top pools** category, you will see a Failure Distribution Report just for that pool. You can then begin analyzing why the Dublin pool was experiencing so many difficulties.</span></span>

<div>

## <a name="viewing-the-failure-distribution-report"></a><span data-ttu-id="49a32-121">Просмотр отчета о распределении сбоев</span><span class="sxs-lookup"><span data-stu-id="49a32-121">Viewing the Failure Distribution Report</span></span>

<span data-ttu-id="49a32-122">Обратиться к отчету о распределении сбоев можно из любого из следующих отчетов, щелкнув показатель **Том ожидаемого сбоя** или **Том неожиданного сбоя**:</span><span class="sxs-lookup"><span data-stu-id="49a32-122">You can access the Failure Distribution Report from any of the following reports by clicking either the **Expected failure volume** or the **Unexpected failure volume** metric:</span></span>

  - [<span data-ttu-id="49a32-123">Отчет об ошибках верхнего уровня в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="49a32-123">Top Failures Report in Lync Server 2013</span></span>](lync-server-2013-top-failures-report.md)

  - [<span data-ttu-id="49a32-124">Диагностический отчет на Конференции в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="49a32-124">Conference Diagnostic Report in Lync Server 2013</span></span>](lync-server-2013-conference-diagnostic-report.md)

  - [<span data-ttu-id="49a32-125">Диагностический отчет о действиях одноранговой сети в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="49a32-125">Peer-to-Peer Activity Diagnostic Report in Lync Server 2013</span></span>](lync-server-2013-peer-to-peer-activity-diagnostic-report.md)

<span data-ttu-id="49a32-126">В отчете распределение сбоев можно выбрать любую из указанных ниже метрик, чтобы просмотреть [отчет о списке отказов в Lync Server 2013](lync-server-2013-failure-list-report.md):</span><span class="sxs-lookup"><span data-stu-id="49a32-126">From the Failure Distribution Report, you can click any of the following metrics to view the [Failure List Report in Lync Server 2013](lync-server-2013-failure-list-report.md):</span></span>

  - <span data-ttu-id="49a32-127">Top diagnostic reasons (sessions) (Основные причины диагностики (сеансы))</span><span class="sxs-lookup"><span data-stu-id="49a32-127">Top diagnostic reasons (sessions)</span></span>

  - <span data-ttu-id="49a32-128">Top modalities (sessions) (Основные условия (сеансы))</span><span class="sxs-lookup"><span data-stu-id="49a32-128">Top modalities (sessions)</span></span>

  - <span data-ttu-id="49a32-129">Top pools (sessions) (Основные пулы (сеансы))</span><span class="sxs-lookup"><span data-stu-id="49a32-129">Top pools (sessions)</span></span>

  - <span data-ttu-id="49a32-130">Top sources (sessions) (Основные источники (сеансы))</span><span class="sxs-lookup"><span data-stu-id="49a32-130">Top sources (sessions)</span></span>

  - <span data-ttu-id="49a32-131">Top components (sessions) (Основные компоненты (сеансы))</span><span class="sxs-lookup"><span data-stu-id="49a32-131">Top components (sessions)</span></span>

  - <span data-ttu-id="49a32-132">Top from users (sessions) (Основные пользователи с ошибками исходящей связи (сеансы))</span><span class="sxs-lookup"><span data-stu-id="49a32-132">Top from users (sessions)</span></span>

  - <span data-ttu-id="49a32-133">Top to users (sessions) (Основные пользователи с ошибками входящей связи (сеансы))</span><span class="sxs-lookup"><span data-stu-id="49a32-133">Top to users (sessions)</span></span>

  - <span data-ttu-id="49a32-134">Top from user agents (sessions) (Основные агенты пользователей, используемые в сеансах, завершившихся с ошибками (сеансы))</span><span class="sxs-lookup"><span data-stu-id="49a32-134">Top from user agents (sessions)</span></span>

</div>

<div>

## <a name="using-the-failure-distribution-report"></a><span data-ttu-id="49a32-135">Использование отчета о распределении сбоев</span><span class="sxs-lookup"><span data-stu-id="49a32-135">Using the Failure Distribution Report</span></span>

<span data-ttu-id="49a32-p102">В зависимости от размера и разрешения экрана некоторые данные в отчете о распределении сбоев при просмотре на экране могут усекаться. Это особенно актуально для таких показателей, как агенты пользователя, у которых могут быть очень длинные метки. Например, агент пользователя с именем UCCAPI/4.0.7400.0 OC/4.0.7400.0 (Microsoft Lync 2013) может только частично появится на экране:</span><span class="sxs-lookup"><span data-stu-id="49a32-p102">Depending on your monitor size and screen resolution, it's possible that some of the data shown in the Failure Distribution Report might be truncated when you view it onscreen. This is especially true for metrics such as user agents, which can have very long labels. For example, a user agent with a name like "UCCAPI/4.0.7400.0 OC/4.0.7400.0 (Microsoft Lync 2013)" might only partially appear onscreen:</span></span>

<span data-ttu-id="49a32-139">UCCAPI/4.0.7400.0 OC/4.0.7400.0 (Microsoft Ly...</span><span class="sxs-lookup"><span data-stu-id="49a32-139">UCCAPI/4.0.7400.0 OC/4.0.7400.0 (Microsoft Ly...</span></span>

<span data-ttu-id="49a32-140">К счастью, всю метку можно увидеть, просто удерживая указатель мыши над усеченным значением.</span><span class="sxs-lookup"><span data-stu-id="49a32-140">Fortunately, you can see the entire label simply by holding your mouse over the truncated value.</span></span>

<span data-ttu-id="49a32-p103">Один из интересных показателей, который можно использовать для фильтрации с помощью отчета распределения сбоев – это код диагностики. Если вы видите один и тот же код в других отчетах, можно отфильтровать отчет по этому коду и получить очень подробные сведения о том, где именно и как часто этот код появлялся в ошибочном сеансе.</span><span class="sxs-lookup"><span data-stu-id="49a32-p103">One interesting metric that you can filter on by using the Failure Distribution Report is Diagnostic ID. If you see the same Diagnostic ID cropping up in other reports you can filter on that ID in the Failure Distribution Report and get a very detailed look at exactly where, and how often, that ID has been reported during a failed session.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="49a32-143">Фильтры</span><span class="sxs-lookup"><span data-stu-id="49a32-143">Filters</span></span>

<span data-ttu-id="49a32-p104">Фильтры позволяют получать более точный набор данных или просматривать данные различными способами. Например, отчет распределения сбоев позволяет фильтровать данные по таким элементам, как тип деятельности (одноранговый сеанс или сеанс конференц-связи) или код диагностики, связанный с каждым ошибочным сеансом.</span><span class="sxs-lookup"><span data-stu-id="49a32-p104">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. For example, the Failed Distribution Report enables you to filter on such things as the activity type (peer-to-peer session or conferencing session) or by the diagnostic ID that accompanied each failed session.</span></span>

<span data-ttu-id="49a32-146">В следующей таблице приведены фильтры, которые можно использовать с отчетом распределения сбоев.</span><span class="sxs-lookup"><span data-stu-id="49a32-146">The following table lists the filters that you can use with the Failure Distribution Report.</span></span>

### <a name="failure-distribution-report-filters"></a><span data-ttu-id="49a32-147">Фильтры отчета распределения сбоев</span><span class="sxs-lookup"><span data-stu-id="49a32-147">Failure Distribution Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="49a32-148">Имя</span><span class="sxs-lookup"><span data-stu-id="49a32-148">Name</span></span></th>
<th><span data-ttu-id="49a32-149">Описание</span><span class="sxs-lookup"><span data-stu-id="49a32-149">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49a32-150"><strong>От</strong></span><span class="sxs-lookup"><span data-stu-id="49a32-150"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="49a32-p105">Начальные дата/время для временного диапазона. Чтобы просмотреть данные по часам, введите начальные дату и время следующим образом:</span><span class="sxs-lookup"><span data-stu-id="49a32-p105">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="49a32-153">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="49a32-153">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="49a32-p106">Если вы не вводите начальное время, отчет автоматически начинается с 12:00 AM указанного дня. Чтобы просмотреть данные по дням, просто введите дату:</span><span class="sxs-lookup"><span data-stu-id="49a32-p106">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="49a32-156">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="49a32-156">7/7/2012</span></span></p>
<p><span data-ttu-id="49a32-157">Чтобы просмотреть данные за неделю или месяц, введите дату, выпадающую на любое время в рамках недели или месяца, которые вы хотите просмотреть (вам не требуется вводить первый день недели или месяца):</span><span class="sxs-lookup"><span data-stu-id="49a32-157">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="49a32-158">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="49a32-158">7/3/2012</span></span></p>
<p><span data-ttu-id="49a32-159">Недели всегда отсчитываются с воскресенья по субботу.</span><span class="sxs-lookup"><span data-stu-id="49a32-159">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49a32-160"><strong>До</strong></span><span class="sxs-lookup"><span data-stu-id="49a32-160"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="49a32-p107">Конечные дата/время для временного диапазона. Чтобы просмотреть данные по часам, введите конечные дату и время следующим образом:</span><span class="sxs-lookup"><span data-stu-id="49a32-p107">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="49a32-163">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="49a32-163">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="49a32-p108">Если вы не вводите конечное время, отчет автоматически заканчивается в 12:00 AM указанного дня. Чтобы просмотреть данные по дням, просто введите дату:</span><span class="sxs-lookup"><span data-stu-id="49a32-p108">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="49a32-166">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="49a32-166">7/7/2012</span></span></p>
<p><span data-ttu-id="49a32-167">Чтобы просмотреть данные за неделю или месяц, введите дату, выпадающую на любое время в рамках недели или месяца, которые вы хотите просмотреть (вам не требуется вводить первый день недели или месяца):</span><span class="sxs-lookup"><span data-stu-id="49a32-167">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="49a32-168">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="49a32-168">7/3/2012</span></span></p>
<p><span data-ttu-id="49a32-169">Недели всегда отсчитываются с воскресенья по субботу.</span><span class="sxs-lookup"><span data-stu-id="49a32-169">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49a32-170"><strong>Пул</strong></span><span class="sxs-lookup"><span data-stu-id="49a32-170"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="49a32-p109">Полное доменное имя пула регистратора или пограничного сервера. Можно выбрать отдельный пул или нажать <strong>[Все]</strong>, чтобы просмотреть данные для всех пулов. Этот раскрывающийся список автоматически заполняется на основе записей в базе данных.</span><span class="sxs-lookup"><span data-stu-id="49a32-p109">Fully qualified domain name (FQDN) of the Registrar pool or Edge Server. You can either select an individual pool or click <strong>[All]</strong> to view data for all the pools. This drop-down list is automatically populated for you based on the records in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49a32-174"><strong>Тип сеанса</strong></span><span class="sxs-lookup"><span data-stu-id="49a32-174"><strong>Activity type</strong></span></span></p></td>
<td><p><span data-ttu-id="49a32-p110">Тип деятельности, к которому требуется применить фильтр. Выберите один из следующих параметров:</span><span class="sxs-lookup"><span data-stu-id="49a32-p110">Type of activity to filter on. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="49a32-177">[All] (Все)</span><span class="sxs-lookup"><span data-stu-id="49a32-177">[All]</span></span></p></li>
<li><p><span data-ttu-id="49a32-178">Одноранговая</span><span class="sxs-lookup"><span data-stu-id="49a32-178">Peer-to-peer</span></span></p></li>
<li><p><span data-ttu-id="49a32-179">Конференция</span><span class="sxs-lookup"><span data-stu-id="49a32-179">Conference</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49a32-180"><strong>Session category (Категория сеанса)</strong></span><span class="sxs-lookup"><span data-stu-id="49a32-180"><strong>Session category</strong></span></span></p></td>
<td><p><span data-ttu-id="49a32-p111">Указывает, была ли рассматриваемая активность успешна. Выберите одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="49a32-p111">Indicates whether the activity in question succeeded or failed. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="49a32-183">[All] (Все)</span><span class="sxs-lookup"><span data-stu-id="49a32-183">[All]</span></span></p></li>
<li><p><span data-ttu-id="49a32-184">Success (Успешно)</span><span class="sxs-lookup"><span data-stu-id="49a32-184">Success</span></span></p></li>
<li><p><span data-ttu-id="49a32-185">Expected failure (Ожидаемый сбой)</span><span class="sxs-lookup"><span data-stu-id="49a32-185">Expected failure</span></span></p></li>
<li><p><span data-ttu-id="49a32-186">Unexpected failure (Неожиданный сбой)</span><span class="sxs-lookup"><span data-stu-id="49a32-186">Unexpected failure</span></span></p></li>
</ul>
<p><span data-ttu-id="49a32-187">&quot;Ожидаемый сбой &quot; — это сбой, который должен выполняться.</span><span class="sxs-lookup"><span data-stu-id="49a32-187">An &quot;expected failure&quot; is a failure that is expected to happen.</span></span> <span data-ttu-id="49a32-188">Например, если пользователь установил статус «Не беспокоить», то ожидаемое, что все вызовы этого пользователя завершатся неудачно.</span><span class="sxs-lookup"><span data-stu-id="49a32-188">For example, if a user has set his or her status to Do Not Disturb you would expect any call to that user to fail.</span></span> <span data-ttu-id="49a32-189">Произошла &quot; непредвиденная ошибка &quot; , возникающая в том, что может выглядеть как подсистема, которая в противном случае является работоспособной.</span><span class="sxs-lookup"><span data-stu-id="49a32-189">An &quot;unexpected failure&quot; is a failure that occurs in what would appear to be an otherwise healthy system.</span></span> <span data-ttu-id="49a32-190">Например, вызов не должен прерываться, если вызывающий абонент помещается на удержание.</span><span class="sxs-lookup"><span data-stu-id="49a32-190">For example, a call should not be terminated if the caller is placed on hold.</span></span> <span data-ttu-id="49a32-191">В этом случае это считается непредвиденным сбоем.</span><span class="sxs-lookup"><span data-stu-id="49a32-191">If that occurs, that would be flagged as an unexpected failure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49a32-192"><strong>Diagnostic ID (ИД диагностики)</strong></span><span class="sxs-lookup"><span data-stu-id="49a32-192"><strong>Diagnostic ID</strong></span></span></p></td>
<td><p><span data-ttu-id="49a32-p113">Прикрепленный к SIP-сообщению уникальный идентификатор (в форме заголовка ms-diagnostics), который часто содержит информацию, полезную при поиске и устранении ошибок. Заголовки диагностики не являются обязательными (можно иметь сеансы SIP без таких заголовков), а идентификаторы диагностики указываются только для сеансов, в которых возникли какие-либо проблемы.</span><span class="sxs-lookup"><span data-stu-id="49a32-p113">Unique identifier (in the form of an ms-diagnostics header) attached to a SIP message that often provides information useful in troubleshooting errors. Diagnostics headers are optional (it is possible to have SIP sessions that do not include these headers), and diagnostic IDs are reported only for sessions that experienced problems of some kind.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-top-diagnostic-reasons"></a><span data-ttu-id="49a32-195">Показатели для самых распространенных причин диагностики</span><span class="sxs-lookup"><span data-stu-id="49a32-195">Metrics for Top Diagnostic Reasons</span></span>

<span data-ttu-id="49a32-196">В следующей таблице представлены сведения, приведенные в отчете распределения сбоев на основе самых распространенных кодов диагностики.</span><span class="sxs-lookup"><span data-stu-id="49a32-196">The following table lists the information provided in the Failure Distribution Report based on the most frequently reported diagnostic ID.</span></span>

### <a name="metrics-for-top-diagnostic-reasons"></a><span data-ttu-id="49a32-197">Показатели для самых распространенных причин диагностики</span><span class="sxs-lookup"><span data-stu-id="49a32-197">Metrics for Top Diagnostic Reasons</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="49a32-198">Имя</span><span class="sxs-lookup"><span data-stu-id="49a32-198">Name</span></span></th>
<th><span data-ttu-id="49a32-199">Поддержка сортировки</span><span class="sxs-lookup"><span data-stu-id="49a32-199">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="49a32-200">Описание</span><span class="sxs-lookup"><span data-stu-id="49a32-200">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49a32-201"><strong>Rank (Ранг)</strong></span><span class="sxs-lookup"><span data-stu-id="49a32-201"><strong>Rank</strong></span></span></p></td>
<td><p><span data-ttu-id="49a32-202">Нет</span><span class="sxs-lookup"><span data-stu-id="49a32-202">No</span></span></p></td>
<td><p><span data-ttu-id="49a32-p114">Относительное ранжирование неудачных сеансов на основе кодов диагностики. Код диагностики – это уникальный идентификатор (в виде заголовка ms-diagnostics), прикрепленный к сообщению SIP, которое часто содержит полезные сведения для устранения ошибок.</span><span class="sxs-lookup"><span data-stu-id="49a32-p114">Relative ranking of failed sessions based on diagnostic IDs. The diagnostic ID is a unique identifier (in the form of an ms-diagnostics header) attached to a SIP message that often provides information useful in troubleshooting errors.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49a32-205"><strong>Самые распространенные причины диагностики</strong></span><span class="sxs-lookup"><span data-stu-id="49a32-205"><strong>Top diagnostic reasons</strong></span></span></p></td>
<td><p><span data-ttu-id="49a32-206">Нет</span><span class="sxs-lookup"><span data-stu-id="49a32-206">No</span></span></p></td>
<td><p><span data-ttu-id="49a32-207">Код, созданный во время сеанса.</span><span class="sxs-lookup"><span data-stu-id="49a32-207">Diagnostic ID generated in a session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49a32-208"><strong>Сеансы</strong></span><span class="sxs-lookup"><span data-stu-id="49a32-208"><strong>Sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="49a32-209">Нет</span><span class="sxs-lookup"><span data-stu-id="49a32-209">No</span></span></p></td>
<td><p><span data-ttu-id="49a32-210">Общее количество неудачных сеансов, в которых был создан указанный код диагностики.</span><span class="sxs-lookup"><span data-stu-id="49a32-210">Total number of failed sessions where the specified diagnostic ID was generated.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-top-modalities"></a><span data-ttu-id="49a32-211">Показатели для самых распространенных модальностей</span><span class="sxs-lookup"><span data-stu-id="49a32-211">Metrics for Top Modalities</span></span>

<span data-ttu-id="49a32-212">В следующей таблице содержатся сведения, приведенные в отчете распределения сбоев на основе модальностей сеансов, в которых произошло больше всего ошибок.</span><span class="sxs-lookup"><span data-stu-id="49a32-212">The following table lists the information provided in the Failure Distribution Report based on the session modalities that experienced the most failures.</span></span>

### <a name="metrics-for-top-modalities"></a><span data-ttu-id="49a32-213">Показатели для самых распространенных модальностей</span><span class="sxs-lookup"><span data-stu-id="49a32-213">Metrics for Top Modalities</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="49a32-214">Имя</span><span class="sxs-lookup"><span data-stu-id="49a32-214">Name</span></span></th>
<th><span data-ttu-id="49a32-215">Поддержка сортировки</span><span class="sxs-lookup"><span data-stu-id="49a32-215">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="49a32-216">Описание</span><span class="sxs-lookup"><span data-stu-id="49a32-216">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49a32-217"><strong>Rank (Ранг)</strong></span><span class="sxs-lookup"><span data-stu-id="49a32-217"><strong>Rank</strong></span></span></p></td>
<td><p><span data-ttu-id="49a32-218">Нет</span><span class="sxs-lookup"><span data-stu-id="49a32-218">No</span></span></p></td>
<td><p><span data-ttu-id="49a32-219">Относительное ранжирование неудачных сеансов на основе типа сеанса (например, аудио- или видеоконференция или одноранговый сеанс передачи файлов).</span><span class="sxs-lookup"><span data-stu-id="49a32-219">Relative ranking based of failed session based on session type (for example, an audio/video conference or a peer-to-peer file transfer session).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49a32-220"><strong>Самые распространенные модальности</strong></span><span class="sxs-lookup"><span data-stu-id="49a32-220"><strong>Top modalities</strong></span></span></p></td>
<td><p><span data-ttu-id="49a32-221">Нет</span><span class="sxs-lookup"><span data-stu-id="49a32-221">No</span></span></p></td>
<td><p><span data-ttu-id="49a32-222">Тип сеанса.</span><span class="sxs-lookup"><span data-stu-id="49a32-222">Session type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49a32-223"><strong>Сеансы</strong></span><span class="sxs-lookup"><span data-stu-id="49a32-223"><strong>Sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="49a32-224">Нет</span><span class="sxs-lookup"><span data-stu-id="49a32-224">No</span></span></p></td>
<td><p><span data-ttu-id="49a32-225">Общее количество неудачных сеансов с указанной модальностью.</span><span class="sxs-lookup"><span data-stu-id="49a32-225">Total number of failed sessions involving the specified modality.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-top-pools"></a><span data-ttu-id="49a32-226">Показатели для самых распространенных пулов</span><span class="sxs-lookup"><span data-stu-id="49a32-226">Metrics for Top Pools</span></span>

<span data-ttu-id="49a32-227">В следующей таблице содержатся сведения, приведенные в отчете распределения сбоев на основе пулов, в которых произошло больше всего ошибок.</span><span class="sxs-lookup"><span data-stu-id="49a32-227">The following table lists the information provided in the Failure Distribution Report based on the pools that experienced the most failures.</span></span>

### <a name="metrics-for-top-pools"></a><span data-ttu-id="49a32-228">Показатели для самых распространенных пулов</span><span class="sxs-lookup"><span data-stu-id="49a32-228">Metrics for Top Pools</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="49a32-229">Имя</span><span class="sxs-lookup"><span data-stu-id="49a32-229">Name</span></span></th>
<th><span data-ttu-id="49a32-230">Поддержка сортировки</span><span class="sxs-lookup"><span data-stu-id="49a32-230">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="49a32-231">Описание</span><span class="sxs-lookup"><span data-stu-id="49a32-231">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49a32-232"><strong>Rank (Ранг)</strong></span><span class="sxs-lookup"><span data-stu-id="49a32-232"><strong>Rank</strong></span></span></p></td>
<td><p><span data-ttu-id="49a32-233">Нет</span><span class="sxs-lookup"><span data-stu-id="49a32-233">No</span></span></p></td>
<td><p><span data-ttu-id="49a32-234">Относительная ранжирование неудачных сеансов на основе регистратора или пограничного сервера, на котором выполнялся сеанс.</span><span class="sxs-lookup"><span data-stu-id="49a32-234">Relative ranking of failed sessions based on the Registrar pool or Edge Server where the session was conducted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49a32-235"><strong>Самые распространенные пулы</strong></span><span class="sxs-lookup"><span data-stu-id="49a32-235"><strong>Top pools</strong></span></span></p></td>
<td><p><span data-ttu-id="49a32-236">Нет</span><span class="sxs-lookup"><span data-stu-id="49a32-236">No</span></span></p></td>
<td><p><span data-ttu-id="49a32-237">Имя пула регистраторов или пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="49a32-237">Name of the Registrar pool or Edge Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49a32-238"><strong>Сеансы</strong></span><span class="sxs-lookup"><span data-stu-id="49a32-238"><strong>Sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="49a32-239">Нет</span><span class="sxs-lookup"><span data-stu-id="49a32-239">No</span></span></p></td>
<td><p><span data-ttu-id="49a32-240">Общее количество неудачных сеансов на каждом из групп регистраторов или пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="49a32-240">Total number of failed sessions per Registrar pool or Edge Server.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-top-sources"></a><span data-ttu-id="49a32-241">Показатели для самых распространенных источников</span><span class="sxs-lookup"><span data-stu-id="49a32-241">Metrics for Top Sources</span></span>

<span data-ttu-id="49a32-242">В следующей таблице содержатся сведения, приведенные в отчете распределения сбоев на основе компьютеров, в которых произошло больше всего ошибок.</span><span class="sxs-lookup"><span data-stu-id="49a32-242">The following table lists the information provided in the Failure Distribution Report based on the computers that experienced the most failures.</span></span>

### <a name="metrics-for-top-sources"></a><span data-ttu-id="49a32-243">Показатели для самых распространенных источников</span><span class="sxs-lookup"><span data-stu-id="49a32-243">Metrics for Top Sources</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="49a32-244">Имя</span><span class="sxs-lookup"><span data-stu-id="49a32-244">Name</span></span></th>
<th><span data-ttu-id="49a32-245">Поддержка сортировки</span><span class="sxs-lookup"><span data-stu-id="49a32-245">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="49a32-246">Описание</span><span class="sxs-lookup"><span data-stu-id="49a32-246">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49a32-247"><strong>Rank (Ранг)</strong></span><span class="sxs-lookup"><span data-stu-id="49a32-247"><strong>Rank</strong></span></span></p></td>
<td><p><span data-ttu-id="49a32-248">Нет</span><span class="sxs-lookup"><span data-stu-id="49a32-248">No</span></span></p></td>
<td><p><span data-ttu-id="49a32-249">Относительное ранжирование неудачных сеансов на компьютер.</span><span class="sxs-lookup"><span data-stu-id="49a32-249">Relative ranking failed sessions per computer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49a32-250"><strong>Самые распространенные источники</strong></span><span class="sxs-lookup"><span data-stu-id="49a32-250"><strong>Top sources</strong></span></span></p></td>
<td><p><span data-ttu-id="49a32-251">Нет</span><span class="sxs-lookup"><span data-stu-id="49a32-251">No</span></span></p></td>
<td><p><span data-ttu-id="49a32-252">Имя компьютера, используемого в неудачном сеансе.</span><span class="sxs-lookup"><span data-stu-id="49a32-252">Name of the computer involved in the failed session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49a32-253"><strong>Сеансы</strong></span><span class="sxs-lookup"><span data-stu-id="49a32-253"><strong>Sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="49a32-254">Нет</span><span class="sxs-lookup"><span data-stu-id="49a32-254">No</span></span></p></td>
<td><p><span data-ttu-id="49a32-255">Общее количество неудачных сеансов на компьютер.</span><span class="sxs-lookup"><span data-stu-id="49a32-255">Total number of failed sessions per computer.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-top-components"></a><span data-ttu-id="49a32-256">Показатели для самых распространенных компонентов</span><span class="sxs-lookup"><span data-stu-id="49a32-256">Metrics for Top Components</span></span>

<span data-ttu-id="49a32-257">В таблице ниже приведены сведения, которые содержатся в отчете о распределении неисправностей, основанном на компонентах Microsoft Lync Server 2010, в которых произошел сбой.</span><span class="sxs-lookup"><span data-stu-id="49a32-257">The following table lists the information provided in the Failure Distribution Report based on the Microsoft Lync Server 2010 components that experienced the most failures.</span></span>

### <a name="metrics-for-top-components"></a><span data-ttu-id="49a32-258">Показатели для самых распространенных компонентов</span><span class="sxs-lookup"><span data-stu-id="49a32-258">Metrics for Top Components</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="49a32-259">Имя</span><span class="sxs-lookup"><span data-stu-id="49a32-259">Name</span></span></th>
<th><span data-ttu-id="49a32-260">Поддержка сортировки</span><span class="sxs-lookup"><span data-stu-id="49a32-260">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="49a32-261">Описание</span><span class="sxs-lookup"><span data-stu-id="49a32-261">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49a32-262"><strong>Rank (Ранг)</strong></span><span class="sxs-lookup"><span data-stu-id="49a32-262"><strong>Rank</strong></span></span></p></td>
<td><p><span data-ttu-id="49a32-263">Нет</span><span class="sxs-lookup"><span data-stu-id="49a32-263">No</span></span></p></td>
<td><p><span data-ttu-id="49a32-264">Относительная ранжирование неудачных сеансов на основе компонента Lync Server 2010 (например, ExumRouting, GroupChat или MediationServer).</span><span class="sxs-lookup"><span data-stu-id="49a32-264">Relative ranking of failed sessions based on Lync Server 2010 component (for example, ExumRouting, GroupChat, or MediationServer).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49a32-265"><strong>Самые распространенные компоненты</strong></span><span class="sxs-lookup"><span data-stu-id="49a32-265"><strong>Top components</strong></span></span></p></td>
<td><p><span data-ttu-id="49a32-266">Нет</span><span class="sxs-lookup"><span data-stu-id="49a32-266">No</span></span></p></td>
<td><p><span data-ttu-id="49a32-267">Имя компонента, используемого в неудачном сеансе.</span><span class="sxs-lookup"><span data-stu-id="49a32-267">Name of the component involved in the failed session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49a32-268"><strong>Сеансы</strong></span><span class="sxs-lookup"><span data-stu-id="49a32-268"><strong>Sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="49a32-269">Нет</span><span class="sxs-lookup"><span data-stu-id="49a32-269">No</span></span></p></td>
<td><p><span data-ttu-id="49a32-270">Общее количество неудачных сеансов на компонент.</span><span class="sxs-lookup"><span data-stu-id="49a32-270">Total number of failed sessions per component.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-top-from-users"></a><span data-ttu-id="49a32-271">Показатели для самых распространенных вызывающих пользователей</span><span class="sxs-lookup"><span data-stu-id="49a32-271">Metrics for Top From Users</span></span>

<span data-ttu-id="49a32-272">В следующей таблице представлены сведения, приведенные в отчете распределения сбоев на основе числа пользователей, у которых возникло больше всего ошибок, когда они пытались звонить кому-нибудь еще (которых также называют "вызывающими" пользователями).</span><span class="sxs-lookup"><span data-stu-id="49a32-272">The following table lists the information provided in the Failure Distribution Report based on users who experienced the most failures when they tried to call someone else (known as "From" users).</span></span>

### <a name="metrics-for-top-from-users"></a><span data-ttu-id="49a32-273">Показатели для самых распространенных вызывающих пользователей</span><span class="sxs-lookup"><span data-stu-id="49a32-273">Metrics for Top From Users</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="49a32-274">Имя</span><span class="sxs-lookup"><span data-stu-id="49a32-274">Name</span></span></th>
<th><span data-ttu-id="49a32-275">Поддержка сортировки</span><span class="sxs-lookup"><span data-stu-id="49a32-275">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="49a32-276">Описание</span><span class="sxs-lookup"><span data-stu-id="49a32-276">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49a32-277"><strong>Rank (Ранг)</strong></span><span class="sxs-lookup"><span data-stu-id="49a32-277"><strong>Rank</strong></span></span></p></td>
<td><p><span data-ttu-id="49a32-278">Нет</span><span class="sxs-lookup"><span data-stu-id="49a32-278">No</span></span></p></td>
<td><p><span data-ttu-id="49a32-279">Относительно ранжирование неудачных сеансов на основе пользователя, который был приглашен для присоединения к сеансу.</span><span class="sxs-lookup"><span data-stu-id="49a32-279">Relative ranking of failed sessions based on the user who was invited to join the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49a32-280"><strong>Самые распространенные вызывающие пользователи</strong></span><span class="sxs-lookup"><span data-stu-id="49a32-280"><strong>Top from users</strong></span></span></p></td>
<td><p><span data-ttu-id="49a32-281">Нет</span><span class="sxs-lookup"><span data-stu-id="49a32-281">No</span></span></p></td>
<td><p><span data-ttu-id="49a32-282">SIP-адрес пользователя, приглашенного в сеанс.</span><span class="sxs-lookup"><span data-stu-id="49a32-282">SIP address of the user invited to join the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49a32-283"><strong>Сеансы</strong></span><span class="sxs-lookup"><span data-stu-id="49a32-283"><strong>Sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="49a32-284">Нет</span><span class="sxs-lookup"><span data-stu-id="49a32-284">No</span></span></p></td>
<td><p><span data-ttu-id="49a32-285">Общее количество неудачных сеансов на пользователя.</span><span class="sxs-lookup"><span data-stu-id="49a32-285">Total number of failed sessions per user.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-top-to-users"></a><span data-ttu-id="49a32-286">Показатели для самых распространенных вызываемых пользователей</span><span class="sxs-lookup"><span data-stu-id="49a32-286">Metrics for Top To Users</span></span>

<span data-ttu-id="49a32-287">В следующей таблице представлены сведения, приведенные в отчете распределения сбоев на основе пользователей, у которых возникло больше всего ошибок, когда кто-то другой пытался позвонить им (их также называют "вызываемыми" пользователями).</span><span class="sxs-lookup"><span data-stu-id="49a32-287">The following table lists the information provided in the Failure Distribution Report based on the users who experienced the most failures when another user tried to call them (known as "To" users).</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="49a32-288">Имя</span><span class="sxs-lookup"><span data-stu-id="49a32-288">Name</span></span></th>
<th><span data-ttu-id="49a32-289">Поддержка сортировки</span><span class="sxs-lookup"><span data-stu-id="49a32-289">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="49a32-290">Описание</span><span class="sxs-lookup"><span data-stu-id="49a32-290">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49a32-291"><strong>Rank (Ранг)</strong></span><span class="sxs-lookup"><span data-stu-id="49a32-291"><strong>Rank</strong></span></span></p></td>
<td><p><span data-ttu-id="49a32-292">Нет</span><span class="sxs-lookup"><span data-stu-id="49a32-292">No</span></span></p></td>
<td><p><span data-ttu-id="49a32-293">Относительно ранжирование неудачных сеансов на основе пользователя, инициировавшего сеанс.</span><span class="sxs-lookup"><span data-stu-id="49a32-293">Relative ranking of failed sessions based on the user who initiated the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49a32-294"><strong>Самые распространенные вызываемые пользователи</strong></span><span class="sxs-lookup"><span data-stu-id="49a32-294"><strong>Top to users</strong></span></span></p></td>
<td><p><span data-ttu-id="49a32-295">Нет</span><span class="sxs-lookup"><span data-stu-id="49a32-295">No</span></span></p></td>
<td><p><span data-ttu-id="49a32-296">SIP-адрес пользователя, инициировавшего сеанс.</span><span class="sxs-lookup"><span data-stu-id="49a32-296">SIP address of the user who initiated the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49a32-297"><strong>Сеансы</strong></span><span class="sxs-lookup"><span data-stu-id="49a32-297"><strong>Sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="49a32-298">Нет</span><span class="sxs-lookup"><span data-stu-id="49a32-298">No</span></span></p></td>
<td><p><span data-ttu-id="49a32-299">Общее количество неудачных сеансов на пользователя.</span><span class="sxs-lookup"><span data-stu-id="49a32-299">Total number of failed sessions per user.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-top-user-agents"></a><span data-ttu-id="49a32-300">Показатели для самых распространенных агентов пользователей</span><span class="sxs-lookup"><span data-stu-id="49a32-300">Metrics for Top User Agents</span></span>

<span data-ttu-id="49a32-301">В следующей таблице содержатся сведения, приведенные в отчете распределения сбоев на основе программного обеспечения конечных точек, в которых произошло больше всего ошибок.</span><span class="sxs-lookup"><span data-stu-id="49a32-301">The following table lists the information provided in the Failure Distribution Report based on the endpoint software that experienced the most failures.</span></span>

### <a name="metrics-for-top-user-agents"></a><span data-ttu-id="49a32-302">Показатели для самых распространенных агентов пользователей</span><span class="sxs-lookup"><span data-stu-id="49a32-302">Metrics for Top User Agents</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="49a32-303">Имя</span><span class="sxs-lookup"><span data-stu-id="49a32-303">Name</span></span></th>
<th><span data-ttu-id="49a32-304">Поддержка сортировки</span><span class="sxs-lookup"><span data-stu-id="49a32-304">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="49a32-305">Описание</span><span class="sxs-lookup"><span data-stu-id="49a32-305">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49a32-306"><strong>Rank (Ранг)</strong></span><span class="sxs-lookup"><span data-stu-id="49a32-306"><strong>Rank</strong></span></span></p></td>
<td><p><span data-ttu-id="49a32-307">Нет</span><span class="sxs-lookup"><span data-stu-id="49a32-307">No</span></span></p></td>
<td><p><span data-ttu-id="49a32-p115">Относительное ранжирование неудачных сеансов на основе агента пользователя (программного обеспечения), применяемого в сеансе. Например: RTCC/4.0.0.0 Входящее перенаправление/4.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="49a32-p115">Relative ranking of failed sessions based on the user agent (software) involved in the session. For example: RTCC/4.0.0.0 Inbound Routing/4.0.0.0.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49a32-310"><strong>Самые распространенные агенты пользователей</strong></span><span class="sxs-lookup"><span data-stu-id="49a32-310"><strong>Top user agents</strong></span></span></p></td>
<td><p><span data-ttu-id="49a32-311">Нет</span><span class="sxs-lookup"><span data-stu-id="49a32-311">No</span></span></p></td>
<td><p><span data-ttu-id="49a32-312">Имя агента пользователя, применяемого в неудачном сеансе.</span><span class="sxs-lookup"><span data-stu-id="49a32-312">Name of the user agent involved in the failed session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49a32-313"><strong>Сеансы</strong></span><span class="sxs-lookup"><span data-stu-id="49a32-313"><strong>Sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="49a32-314">Нет</span><span class="sxs-lookup"><span data-stu-id="49a32-314">No</span></span></p></td>
<td><p><span data-ttu-id="49a32-315">Общее количество неудачных сеансов на агента пользователя.</span><span class="sxs-lookup"><span data-stu-id="49a32-315">Total number of failed sessions per user agent.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="49a32-316">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="49a32-316">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

