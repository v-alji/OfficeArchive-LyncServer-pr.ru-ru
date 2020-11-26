---
title: 'Lync Server 2013: отчет управления допуском звонков'
description: 'Lync Server 2013: отчет управления допуском звонков.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Call Admission Control Report
ms:assetid: ea4b0c9f-7f93-4b8a-b901-01e1636c44fb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615043(v=OCS.15)
ms:contentKeyID: 48185933
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8764e51603e7097095894bc1230c2a2bb1126b9c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435784"
---
# <a name="call-admission-control-report-in-lync-server-2013"></a><span data-ttu-id="da8d3-103">Отчет по контролю за допуском звонков в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="da8d3-103">Call Admission Control Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="da8d3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="da8d3-104">

<span> </span></span></span>

<span data-ttu-id="da8d3-105">_**Тема последнего изменения:** 2012-06-29_</span><span class="sxs-lookup"><span data-stu-id="da8d3-105">_**Topic Last Modified:** 2012-06-29_</span></span>

<span data-ttu-id="da8d3-106">Отчет по контролю допуска звонков (Call Admission Control Report) содержит сведения о сеансах связи между одноранговыми узлами и конференц-связи, которые были проведены в рамках ограничений, наложенных с помощью функции контроля допуска звонков.</span><span class="sxs-lookup"><span data-stu-id="da8d3-106">The Call Admission Control Report provides information about peer-to-peer and conferencing sessions that were conducted under restrictions set in place by Call Admission Control.</span></span> <span data-ttu-id="da8d3-107">Управление допуском звонков, представленное в Microsoft Lync Server 2010, позволяет администраторам разрешать (или не разрешать) сеансы связи на основе ограничений пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="da8d3-107">Call Admission Control, introduced in Microsoft Lync Server 2010, provides a way for administrators to allow (or not allow) communication sessions based on bandwidth constraints.</span></span> <span data-ttu-id="da8d3-108">Например, администраторы могут создавать политики, ограничивающие полосу пропускания для вызовов видео- и голосовой связи.</span><span class="sxs-lookup"><span data-stu-id="da8d3-108">For example, administrators can create policies that impose a limit on the amount of bandwidth available for voice and video calls.</span></span> <span data-ttu-id="da8d3-109">По достижении предельной полосы пропускания новые вызовы видео- и голосовой связи размещаются только после завершения одного из текущих вызовов и освобождения необходимых сетевых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="da8d3-109">If that bandwidth limit has been reached, then no new voice or video calls can be placed until one of the current calls has ended and freed up the required network resources.</span></span>

<div>

## <a name="accessing-the-call-admission-control-report"></a><span data-ttu-id="da8d3-110">Доступ к отчету по контролю допуска звонков</span><span class="sxs-lookup"><span data-stu-id="da8d3-110">Accessing the Call Admission Control Report</span></span>

<span data-ttu-id="da8d3-p102">Отчет по контролю допуска звонков можно вызвать на домашней странице отчетов мониторинга. Из отчета по контролю допуска звонков можно перейти в следующие отчеты.</span><span class="sxs-lookup"><span data-stu-id="da8d3-p102">The Call Admission Control Report is accessed from the Monitoring Reports home page. From the Call Admission Control Report you can drill down to either of the following reports:</span></span>

  - <span data-ttu-id="da8d3-113">Отчет по деталям конференции – чтобы вызвать этот отчет, нажмите метрику Детали в сеансе конференц-связи.</span><span class="sxs-lookup"><span data-stu-id="da8d3-113">Conference Detail Report – To access this report, click the Details metric from a conference session.</span></span>

  - <span data-ttu-id="da8d3-114">Отчет по деталям однорангового сеанса – чтобы вызвать этот отчет, нажмите метрику Детали для однорангового сеанса.</span><span class="sxs-lookup"><span data-stu-id="da8d3-114">Peer-to-Peer Session Detail Report – To access this report, click the Details metric for a peer-to-peer session.</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-call-admission-control-report"></a><span data-ttu-id="da8d3-115">Оптимальное использование отчета по контролю допуска звонков</span><span class="sxs-lookup"><span data-stu-id="da8d3-115">Making the Best Use of the Call Admission Control Report</span></span>

<span data-ttu-id="da8d3-p103">Чтобы получить полный список вызовов, отклоненных из-за недостаточной пропускной способности, выберите пункт "Вызовы, отклоненные контролем допуска звонков" в раскрывающемся списке категорий вызова. Большая часть отклоненных звонков скорее всего будет иметь диагностический идентификатор 5:</span><span class="sxs-lookup"><span data-stu-id="da8d3-p103">To get a list of calls that failed because of insufficient bandwidth, select Calls rejected because of call admission control from the Call category dropdown list. Most of the returned calls will likely have a diagnostic ID of 5:</span></span>

<span data-ttu-id="da8d3-p104">Недостаточная пропускная способность для установки сеанса. Попытка перенаправить в ТСОП.</span><span class="sxs-lookup"><span data-stu-id="da8d3-p104">Insufficient bandwidth to establish session. Attempt PSTN re-route.</span></span>

<span data-ttu-id="da8d3-120">Это указывает, что ограничения контроля допуска звонков запретили выполнение этого вызова в сети VoIP.</span><span class="sxs-lookup"><span data-stu-id="da8d3-120">That indicates that Call Admission Control limitations were preventing the call from being made on the VoIP network.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="da8d3-121">Фильтры</span><span class="sxs-lookup"><span data-stu-id="da8d3-121">Filters</span></span>

<span data-ttu-id="da8d3-p105">Фильтры позволяют получать более адресный набор данных или просматривать полученные данные разными способами. Например, контроль допуска звонков позволяет фильтровать вызовы по вызывающему пользователю или по вызываемому пользователю. Можно также выбрать способ группирования данных. В этом случае вызовы группируются по часу, дню, неделе или месяцу.</span><span class="sxs-lookup"><span data-stu-id="da8d3-p105">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. For example, the Call Admission Control Report enables you to filter calls by the user who initiated the call or by the user who was being called. You can also choose how data should be grouped. In this case, calls are grouped by hour, day, week, or month.</span></span>

<span data-ttu-id="da8d3-126">В следующей таблице приведены фильтры, которые можно использовать в отчете по контролю допуска звонков.</span><span class="sxs-lookup"><span data-stu-id="da8d3-126">The following table lists the filters that you can use with the Call Admission Control Report.</span></span>

### <a name="call-admission-control-report-filters"></a><span data-ttu-id="da8d3-127">Фильтры отчета по контролю допуска звонков</span><span class="sxs-lookup"><span data-stu-id="da8d3-127">Call Admission Control Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="da8d3-128">Имя</span><span class="sxs-lookup"><span data-stu-id="da8d3-128">Name</span></span></th>
<th><span data-ttu-id="da8d3-129">Описание</span><span class="sxs-lookup"><span data-stu-id="da8d3-129">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="da8d3-130"><strong>От</strong></span><span class="sxs-lookup"><span data-stu-id="da8d3-130"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="da8d3-p106">Начальные дата/время для временного диапазона. Чтобы просмотреть данные по часам, введите начальные дату и время следующим образом:</span><span class="sxs-lookup"><span data-stu-id="da8d3-p106">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="da8d3-133">7/17/12012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="da8d3-133">7/17/12012 1:00 PM</span></span></p>
<p><span data-ttu-id="da8d3-p107">Если вы не вводите начальное время, отчет автоматически начинается с 12:00 AM указанного дня. Чтобы просмотреть данные по дням, просто введите дату:</span><span class="sxs-lookup"><span data-stu-id="da8d3-p107">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="da8d3-136">7/17/12012</span><span class="sxs-lookup"><span data-stu-id="da8d3-136">7/17/12012</span></span></p>
<p><span data-ttu-id="da8d3-137">Чтобы просмотреть данные за неделю или месяц, введите дату, выпадающую на любое время в рамках недели или месяца, которые вы хотите просмотреть (вам не требуется вводить первый день недели или месяца):</span><span class="sxs-lookup"><span data-stu-id="da8d3-137">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="da8d3-138">7/13/2012</span><span class="sxs-lookup"><span data-stu-id="da8d3-138">7/13/2012</span></span></p>
<p><span data-ttu-id="da8d3-139">Недели всегда отсчитываются с воскресенья по субботу.</span><span class="sxs-lookup"><span data-stu-id="da8d3-139">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da8d3-140"><strong>До</strong></span><span class="sxs-lookup"><span data-stu-id="da8d3-140"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="da8d3-p108">Конечные дата/время для временного диапазона. Чтобы просмотреть данные по часам, введите конечные дату и время следующим образом:</span><span class="sxs-lookup"><span data-stu-id="da8d3-p108">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="da8d3-143">7/17/12012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="da8d3-143">7/17/12012 1:00 PM</span></span></p>
<p><span data-ttu-id="da8d3-p109">Если вы не вводите конечное время, отчет автоматически заканчивается в 12:00 AM указанного дня. Чтобы просмотреть данные по дням, просто введите дату:</span><span class="sxs-lookup"><span data-stu-id="da8d3-p109">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="da8d3-146">7/17/12012</span><span class="sxs-lookup"><span data-stu-id="da8d3-146">7/17/12012</span></span></p>
<p><span data-ttu-id="da8d3-147">Чтобы просмотреть данные за неделю или месяц, введите дату, выпадающую на любое время в рамках недели или месяца, которые вы хотите просмотреть (вам не требуется вводить первый день недели или месяца):</span><span class="sxs-lookup"><span data-stu-id="da8d3-147">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="da8d3-148">7/13/2012</span><span class="sxs-lookup"><span data-stu-id="da8d3-148">7/13/2012</span></span></p>
<p><span data-ttu-id="da8d3-149">Недели всегда отсчитываются с воскресенья по субботу.</span><span class="sxs-lookup"><span data-stu-id="da8d3-149">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da8d3-150"><strong>Пул</strong></span><span class="sxs-lookup"><span data-stu-id="da8d3-150"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="da8d3-p110">Полное доменное имя пула регистратора или пограничного сервера. Можно выбрать отдельный пул или нажать <strong>[Все]</strong>, чтобы просмотреть данные для всех пулов. Этот раскрывающийся список автоматически заполняется на основе записей в базе данных.</span><span class="sxs-lookup"><span data-stu-id="da8d3-p110">Fully qualified domain name (FQDN) of the Registrar pool or Edge Server. You can either select an individual pool or click <strong>[All]</strong> to view data for all the pools. This drop-down list is automatically populated for you based on the records in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da8d3-154"><strong>Тип сеанса</strong></span><span class="sxs-lookup"><span data-stu-id="da8d3-154"><strong>Activity type</strong></span></span></p></td>
<td><p><span data-ttu-id="da8d3-p111">Тип действия. Выберите одно из следующих действий:</span><span class="sxs-lookup"><span data-stu-id="da8d3-p111">Type of activity. Select one of the following activities:</span></span></p>
<ul>
<li><p><span data-ttu-id="da8d3-157">[All] (Все)</span><span class="sxs-lookup"><span data-stu-id="da8d3-157">[All]</span></span></p></li>
<li><p><span data-ttu-id="da8d3-158">Одноранговый сеанс</span><span class="sxs-lookup"><span data-stu-id="da8d3-158">Peer-to-Peer</span></span></p></li>
<li><p><span data-ttu-id="da8d3-159">Конференция</span><span class="sxs-lookup"><span data-stu-id="da8d3-159">Conference</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da8d3-160"><strong>Категория вызова</strong></span><span class="sxs-lookup"><span data-stu-id="da8d3-160"><strong>Call category</strong></span></span></p></td>
<td><p><span data-ttu-id="da8d3-p112">Указывает причину, которую контроль допуска звонков использовал для вызова. Выберите один из следующих вариантов:</span><span class="sxs-lookup"><span data-stu-id="da8d3-p112">Indicates the reason that CAC was used for the call. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="da8d3-163">[All] (Все)</span><span class="sxs-lookup"><span data-stu-id="da8d3-163">[All]</span></span></p></li>
<li><p><span data-ttu-id="da8d3-164">Вызов отклонен контролем допуска звонков</span><span class="sxs-lookup"><span data-stu-id="da8d3-164">Call rejected because of call admission control</span></span></p></li>
<li><p><span data-ttu-id="da8d3-165">Вызовы перенаправлены через ТСОП вследствие контроля допуска звонков</span><span class="sxs-lookup"><span data-stu-id="da8d3-165">Calls rerouted through PSTN because of call admission control</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-peer-to-peer-sessions"></a><span data-ttu-id="da8d3-166">Метрики для одноранговых сеансов</span><span class="sxs-lookup"><span data-stu-id="da8d3-166">Metrics for Peer-to-Peer Sessions</span></span>

<span data-ttu-id="da8d3-167">В следующей таблице приведены сведения, предоставляемые отчетом по контролю допуска звонков для одноранговых сеансов (т.е. сеансов, в которых только два участника).</span><span class="sxs-lookup"><span data-stu-id="da8d3-167">The following table lists the information provided in the Call Admission Control Report for peer-to-peer sessions (that is, sessions involving just two participants).</span></span>

### <a name="metrics-for-peer-to-peer-sessions"></a><span data-ttu-id="da8d3-168">Метрики для одноранговых сеансов</span><span class="sxs-lookup"><span data-stu-id="da8d3-168">Metrics for Peer-to-Peer Sessions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="da8d3-169">Имя</span><span class="sxs-lookup"><span data-stu-id="da8d3-169">Name</span></span></th>
<th><span data-ttu-id="da8d3-170">Поддержка сортировки</span><span class="sxs-lookup"><span data-stu-id="da8d3-170">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="da8d3-171">Описание</span><span class="sxs-lookup"><span data-stu-id="da8d3-171">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="da8d3-172"><strong>Подробности</strong></span><span class="sxs-lookup"><span data-stu-id="da8d3-172"><strong>Detail</strong></span></span></p></td>
<td><p><span data-ttu-id="da8d3-173">Нет</span><span class="sxs-lookup"><span data-stu-id="da8d3-173">No</span></span></p></td>
<td><p><span data-ttu-id="da8d3-174">При нажатии этой метрики появится отчет по деталям однорангового сеанса для указанного сеанса.</span><span class="sxs-lookup"><span data-stu-id="da8d3-174">When you click this item, the report shows you a Peer-to-Peer Session Detail Report for the specified session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da8d3-175"><strong>От пользователя</strong></span><span class="sxs-lookup"><span data-stu-id="da8d3-175"><strong>From user</strong></span></span></p></td>
<td><p><span data-ttu-id="da8d3-176">Да</span><span class="sxs-lookup"><span data-stu-id="da8d3-176">Yes</span></span></p></td>
<td><p><span data-ttu-id="da8d3-177">SIP-адрес пользователя, инициировавшего сеанс.</span><span class="sxs-lookup"><span data-stu-id="da8d3-177">SIP address of the user who initiated the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da8d3-178"><strong>Пользователю</strong></span><span class="sxs-lookup"><span data-stu-id="da8d3-178"><strong>To user</strong></span></span></p></td>
<td><p><span data-ttu-id="da8d3-179">Да</span><span class="sxs-lookup"><span data-stu-id="da8d3-179">Yes</span></span></p></td>
<td><p><span data-ttu-id="da8d3-180">SIP-адрес пользователя, приглашенного принять участие в сеансе.</span><span class="sxs-lookup"><span data-stu-id="da8d3-180">SIP address of the user who was invited to join the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da8d3-181"><strong>Модальности</strong></span><span class="sxs-lookup"><span data-stu-id="da8d3-181"><strong>Modalities</strong></span></span></p></td>
<td><p><span data-ttu-id="da8d3-182">Да</span><span class="sxs-lookup"><span data-stu-id="da8d3-182">Yes</span></span></p></td>
<td><p><span data-ttu-id="da8d3-183">Модальности взаимодействия (например звук и видео), использовавшиеся во время сеанса.</span><span class="sxs-lookup"><span data-stu-id="da8d3-183">Communication modalities (such as audio and video) that were used during the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da8d3-184"><strong>Время приглашения</strong></span><span class="sxs-lookup"><span data-stu-id="da8d3-184"><strong>Invite time</strong></span></span></p></td>
<td><p><span data-ttu-id="da8d3-185">Да</span><span class="sxs-lookup"><span data-stu-id="da8d3-185">Yes</span></span></p></td>
<td><p><span data-ttu-id="da8d3-186">Дата и время отправки пользователем-инициатором исходного приглашения принять участие в сеансе.</span><span class="sxs-lookup"><span data-stu-id="da8d3-186">Date and time the initial session invitation was sent to the From user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da8d3-187"><strong>Время ответа</strong></span><span class="sxs-lookup"><span data-stu-id="da8d3-187"><strong>Response time</strong></span></span></p></td>
<td><p><span data-ttu-id="da8d3-188">Да</span><span class="sxs-lookup"><span data-stu-id="da8d3-188">Yes</span></span></p></td>
<td><p><span data-ttu-id="da8d3-189">Дата и время, когда было получено принятие приглашения.</span><span class="sxs-lookup"><span data-stu-id="da8d3-189">Date and time that the invitation acceptance was received.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da8d3-190"><strong>Время окончания</strong></span><span class="sxs-lookup"><span data-stu-id="da8d3-190"><strong>End time</strong></span></span></p></td>
<td><p><span data-ttu-id="da8d3-191">Да</span><span class="sxs-lookup"><span data-stu-id="da8d3-191">Yes</span></span></p></td>
<td><p><span data-ttu-id="da8d3-192">Дата и время окончания сеанса.</span><span class="sxs-lookup"><span data-stu-id="da8d3-192">Date and time that the session ended.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da8d3-193"><strong>Диагностический идентификатор</strong></span><span class="sxs-lookup"><span data-stu-id="da8d3-193"><strong>Diagnostic ID</strong></span></span></p></td>
<td><p><span data-ttu-id="da8d3-194">Да</span><span class="sxs-lookup"><span data-stu-id="da8d3-194">Yes</span></span></p></td>
<td><p><span data-ttu-id="da8d3-p113">Прикрепленный к SIP-сообщению уникальный идентификатор (в форме заголовка ms-diagnostics), который часто содержит информацию, полезную при поиске и устранении ошибок. Заголовки диагностики не являются обязательными (можно иметь сеансы SIP без таких заголовков), а идентификаторы диагностики указываются только для сеансов, в которых возникли какие-либо проблемы.</span><span class="sxs-lookup"><span data-stu-id="da8d3-p113">Unique identifier (in the form of an ms-diagnostics header) attached to a SIP message that often provides information useful in troubleshooting errors. Diagnostics headers are optional (it is possible to have SIP sessions that do not include these headers), and diagnostic IDs are reported only for sessions that experienced problems of some kind.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-conferencing-sessions"></a><span data-ttu-id="da8d3-197">Метрики для сеансов конференц-связи</span><span class="sxs-lookup"><span data-stu-id="da8d3-197">Metrics for Conferencing Sessions</span></span>

<span data-ttu-id="da8d3-198">В следующей таблице приведены сведения, которые предоставляются в отчете по контролю допуска звонков для сеансов конференц-связи (т.е. сеансов, в которых не менее трех участников).</span><span class="sxs-lookup"><span data-stu-id="da8d3-198">The following table lists the information provided in the Call Admission Control Report for conferencing sessions (that is, sessions involving three or more participants).</span></span>

### <a name="metrics-for-conferencing-sessions"></a><span data-ttu-id="da8d3-199">Метрики для сеансов конференц-связи</span><span class="sxs-lookup"><span data-stu-id="da8d3-199">Metrics for Conferencing Sessions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="da8d3-200">Имя</span><span class="sxs-lookup"><span data-stu-id="da8d3-200">Name</span></span></th>
<th><span data-ttu-id="da8d3-201">Поддержка сортировки</span><span class="sxs-lookup"><span data-stu-id="da8d3-201">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="da8d3-202">Описание</span><span class="sxs-lookup"><span data-stu-id="da8d3-202">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="da8d3-203"><strong>Идентификатор URI конференции</strong></span><span class="sxs-lookup"><span data-stu-id="da8d3-203"><strong>Conference URI</strong></span></span></p></td>
<td><p><span data-ttu-id="da8d3-204">Да</span><span class="sxs-lookup"><span data-stu-id="da8d3-204">Yes</span></span></p></td>
<td><p><span data-ttu-id="da8d3-p114">Уникальный идентификатор конференции. Если нажать этот элемент, будут отображены отдельные участники конференции.</span><span class="sxs-lookup"><span data-stu-id="da8d3-p114">Unique identifier for the conference. When you click this item, the report shows the individual conference participants.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da8d3-207"><strong>Инициатор</strong></span><span class="sxs-lookup"><span data-stu-id="da8d3-207"><strong>Organizer</strong></span></span></p></td>
<td><p><span data-ttu-id="da8d3-208">Да</span><span class="sxs-lookup"><span data-stu-id="da8d3-208">Yes</span></span></p></td>
<td><p><span data-ttu-id="da8d3-209">SIP-адрес пользователя, организовавшего конференцию.</span><span class="sxs-lookup"><span data-stu-id="da8d3-209">SIP address of the user who organized the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da8d3-210"><strong>Пул</strong></span><span class="sxs-lookup"><span data-stu-id="da8d3-210"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="da8d3-211">Да</span><span class="sxs-lookup"><span data-stu-id="da8d3-211">Yes</span></span></p></td>
<td><p><span data-ttu-id="da8d3-212">пограничный сервер, использовавшийся в конференции.</span><span class="sxs-lookup"><span data-stu-id="da8d3-212">Edge Server used in the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da8d3-213"><strong>Время начала</strong></span><span class="sxs-lookup"><span data-stu-id="da8d3-213"><strong>Start time</strong></span></span></p></td>
<td><p><span data-ttu-id="da8d3-214">Да</span><span class="sxs-lookup"><span data-stu-id="da8d3-214">Yes</span></span></p></td>
<td><p><span data-ttu-id="da8d3-215">Дата и время начала конференции.</span><span class="sxs-lookup"><span data-stu-id="da8d3-215">Date and time that the conference started.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da8d3-216"><strong>Время окончания</strong></span><span class="sxs-lookup"><span data-stu-id="da8d3-216"><strong>End time</strong></span></span></p></td>
<td><p><span data-ttu-id="da8d3-217">Да</span><span class="sxs-lookup"><span data-stu-id="da8d3-217">Yes</span></span></p></td>
<td><p><span data-ttu-id="da8d3-218">Дата и время завершения конференции.</span><span class="sxs-lookup"><span data-stu-id="da8d3-218">Date and time that the conference ended.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-individual-conference-participants"></a><span data-ttu-id="da8d3-219">Метрики для отдельных участников конференции</span><span class="sxs-lookup"><span data-stu-id="da8d3-219">Metrics for Individual Conference Participants</span></span>

<span data-ttu-id="da8d3-220">В следующей таблице приведены сведения, которые предоставляются в отчете по контролю допуска звонков для отдельных участников конференции.</span><span class="sxs-lookup"><span data-stu-id="da8d3-220">The following table lists the information provided in the Call Admission Control Report for individual conference participants.</span></span>

### <a name="metrics-for-individual-conference-participants"></a><span data-ttu-id="da8d3-221">Метрики для отдельных участников конференции</span><span class="sxs-lookup"><span data-stu-id="da8d3-221">Metrics for Individual Conference Participants</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="da8d3-222">Имя</span><span class="sxs-lookup"><span data-stu-id="da8d3-222">Name</span></span></th>
<th><span data-ttu-id="da8d3-223">Поддержка сортировки</span><span class="sxs-lookup"><span data-stu-id="da8d3-223">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="da8d3-224">Описание</span><span class="sxs-lookup"><span data-stu-id="da8d3-224">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="da8d3-225"><strong>Роль</strong></span><span class="sxs-lookup"><span data-stu-id="da8d3-225"><strong>Role</strong></span></span></p></td>
<td><p><span data-ttu-id="da8d3-226">Нет</span><span class="sxs-lookup"><span data-stu-id="da8d3-226">No</span></span></p></td>
<td><p><span data-ttu-id="da8d3-227">Роль (например, докладчик), которую играл участник конференции.</span><span class="sxs-lookup"><span data-stu-id="da8d3-227">Role (for example, Presenter) played by the conference participant.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da8d3-228"><strong>Участник</strong></span><span class="sxs-lookup"><span data-stu-id="da8d3-228"><strong>Participant</strong></span></span></p></td>
<td><p><span data-ttu-id="da8d3-229">Нет</span><span class="sxs-lookup"><span data-stu-id="da8d3-229">No</span></span></p></td>
<td><p><span data-ttu-id="da8d3-230">SIP-адрес участника конференции.</span><span class="sxs-lookup"><span data-stu-id="da8d3-230">SIP address of the conference participant.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da8d3-231"><strong>Соединение</strong></span><span class="sxs-lookup"><span data-stu-id="da8d3-231"><strong>Connectivity</strong></span></span></p></td>
<td><p><span data-ttu-id="da8d3-232">Нет</span><span class="sxs-lookup"><span data-stu-id="da8d3-232">No</span></span></p></td>
<td><p><span data-ttu-id="da8d3-233">Подключение участника к сети, обычно из внутренней сети или из внешней сети.</span><span class="sxs-lookup"><span data-stu-id="da8d3-233">Network connectivity (typically From Internal or From External) for the participant.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da8d3-234"><strong>Модальность</strong></span><span class="sxs-lookup"><span data-stu-id="da8d3-234"><strong>Modality</strong></span></span></p></td>
<td><p><span data-ttu-id="da8d3-235">Нет</span><span class="sxs-lookup"><span data-stu-id="da8d3-235">No</span></span></p></td>
<td><p><span data-ttu-id="da8d3-236">Тип конференции (например, аудио- и видеоконференция).</span><span class="sxs-lookup"><span data-stu-id="da8d3-236">Conference type (for example, A/V conferencing).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da8d3-237"><strong>Время присоединения к конференциям</strong></span><span class="sxs-lookup"><span data-stu-id="da8d3-237"><strong>Join time</strong></span></span></p></td>
<td><p><span data-ttu-id="da8d3-238">Нет</span><span class="sxs-lookup"><span data-stu-id="da8d3-238">No</span></span></p></td>
<td><p><span data-ttu-id="da8d3-239">Дата и время присоединения участника к конференции.</span><span class="sxs-lookup"><span data-stu-id="da8d3-239">Date and time that the participant joined the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da8d3-240"><strong>Время выхода</strong></span><span class="sxs-lookup"><span data-stu-id="da8d3-240"><strong>Leave time</strong></span></span></p></td>
<td><p><span data-ttu-id="da8d3-241">Нет</span><span class="sxs-lookup"><span data-stu-id="da8d3-241">No</span></span></p></td>
<td><p><span data-ttu-id="da8d3-242">Дата и время, когда участник покинул конференцию.</span><span class="sxs-lookup"><span data-stu-id="da8d3-242">Date and time that the participant left the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da8d3-243"><strong>Диагностический идентификатор</strong></span><span class="sxs-lookup"><span data-stu-id="da8d3-243"><strong>Diagnostic ID</strong></span></span></p></td>
<td><p><span data-ttu-id="da8d3-244">Нет</span><span class="sxs-lookup"><span data-stu-id="da8d3-244">No</span></span></p></td>
<td><p><span data-ttu-id="da8d3-p115">Прикрепленный к SIP-сообщению уникальный идентификатор (в форме заголовка ms-diagnostics), который часто содержит информацию, полезную при поиске и устранении ошибок. Заголовки диагностики не являются обязательными (можно иметь сеансы SIP без таких заголовков), а идентификаторы диагностики указываются только для сеансов, в которых возникли какие-либо проблемы.</span><span class="sxs-lookup"><span data-stu-id="da8d3-p115">Unique identifier (in the form of an ms-diagnostics header) attached to a SIP message that often provides information useful in troubleshooting errors. Diagnostics headers are optional (it is possible to have SIP sessions that do not include these headers), and diagnostic IDs are reported only for sessions that experienced problems of some kind.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="da8d3-247">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="da8d3-247">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

