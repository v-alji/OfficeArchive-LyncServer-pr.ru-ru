---
title: 'Lync Server 2013: одноранговый голосовой и видео отчет'
description: 'Lync Server 2013: одноранговый голосовой и видеоотчет.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Peer-to-Peer Voice and Video Report
ms:assetid: e17c36b5-5a2f-4673-9696-3b2d31c2bb2f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615040(v=OCS.15)
ms:contentKeyID: 48185535
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 43041926b3d6b57508b6ee4c53ca9cb055bcb348
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424696"
---
# <a name="peer-to-peer-voice-and-video-report-in-lync-server-2013"></a><span data-ttu-id="4b336-103">Одноранговый голосовой и Видеоотчет в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4b336-103">Peer-to-Peer Voice and Video Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4b336-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4b336-104">

<span> </span></span></span>

<span data-ttu-id="4b336-105">_**Тема последнего изменения:** 2012-10-21_</span><span class="sxs-lookup"><span data-stu-id="4b336-105">_**Topic Last Modified:** 2012-10-21_</span></span>

<span data-ttu-id="4b336-p101">Отчет об одноранговой голосовой связи и видеосвязи дает подробное представление о распределении голосовых звонках и видеозвонках за указанный период (например, число звонков в час или в день). Кроме того, этот отчет позволяет просматривать все выполненные голосовые звонки и видеозвонки или только те из них, которые были успешными или завершились со сбоем. Сведения о звонках в отчете упорядочены по следующим группам:</span><span class="sxs-lookup"><span data-stu-id="4b336-p101">The Peer-to-Peer Voice and Video Report provides a detailed look at the distribution of voice and video calls over a specified period of time (for example, calls per hour or calls per day). The report also gives you the option of viewing all the voice and video calls that were made, or of viewing only the successful or failed calls. The reports shows call information broken down into the following groupings:</span></span>

  - <span data-ttu-id="4b336-109">Число звонков на пул</span><span class="sxs-lookup"><span data-stu-id="4b336-109">Calls per pool</span></span>

  - <span data-ttu-id="4b336-110">Звонки на тип звонка (например, Lync для звонков по Lync и вызов Lync для абонента в сети PSTN).</span><span class="sxs-lookup"><span data-stu-id="4b336-110">Calls per call type (for example, a Lync to Lync call vs. a Lync call to a person on the PSTN network)</span></span>

  - <span data-ttu-id="4b336-111">Звонки по типу доступа (пользователи, выполнившие вход во внутреннюю сеть, либо пользователи, выполнившие вход во внешнюю сеть)</span><span class="sxs-lookup"><span data-stu-id="4b336-111">Calls per access type (users logged on to the internal network vs. users logged on to the external network)</span></span>

  - <span data-ttu-id="4b336-112">Звонки на сервер по исправлению</span><span class="sxs-lookup"><span data-stu-id="4b336-112">Calls per Mediation Server</span></span>

<div>

## <a name="to-access-the-peer-to-peer-voice-and-video-report"></a><span data-ttu-id="4b336-113">Доступ к отчету об одноранговой голосовой связи и видеосвязи</span><span class="sxs-lookup"><span data-stu-id="4b336-113">To access the peer-to-peer voice and video report</span></span>

<span data-ttu-id="4b336-114">Отчет об одноранговой голосовой связи и видеосвязи можно просмотреть, открыв сводный отчет об одноранговых операциях и щелкнув одну из следующих метрик:</span><span class="sxs-lookup"><span data-stu-id="4b336-114">You can access the Peer-to-Peer Voice and Video Report only by opening the Peer-to-Peer Activity Summary Report and then clicking any of the following metrics:</span></span>

  - <span data-ttu-id="4b336-115">Общее количество одноранговых сеансов аудиосвязи</span><span class="sxs-lookup"><span data-stu-id="4b336-115">Total peer-to-peer audio sessions</span></span>

  - <span data-ttu-id="4b336-116">Общее число минут одноранговой аудиосвязи (Общее число минут одноранговой аудиосвязи)</span><span class="sxs-lookup"><span data-stu-id="4b336-116">Total peer-to-peer audio minutes</span></span>

  - <span data-ttu-id="4b336-117">Общее количество одноранговых сеансов видеосвязи</span><span class="sxs-lookup"><span data-stu-id="4b336-117">Total peer-to-peer video sessions</span></span>

  - <span data-ttu-id="4b336-118">Общее число минут одноранговой видеосвязи (Общее число минут одноранговой видеосвязи)</span><span class="sxs-lookup"><span data-stu-id="4b336-118">Total peer-to-peer video minutes</span></span>

</div>

<div>

## <a name="to-make-the-best-use-of-the-peer-to-peer-voice-and-video-report"></a><span data-ttu-id="4b336-119">Доступ к отчету об одноранговой голосовой связи и видеосвязи</span><span class="sxs-lookup"><span data-stu-id="4b336-119">To make the best use of the peer-to-peer voice and video report</span></span>

<span data-ttu-id="4b336-p102">Существует несколько способ фильтрации отчета об одноранговой голосовой связи и видеосвязи. Однако по умолчанию эти параметры фильтрации скрыты. Чтобы просмотреть их, нажмите кнопку **Показать/скрыть параметры** в верхнем правом углу окна отчета.</span><span class="sxs-lookup"><span data-stu-id="4b336-p102">There are a number of ways you can filter the Peer-to-Peer Voice and Video Report. However, those filtering options are hidden from view by default. To view the filtering options available to you, click **Show/Hide Parameters** button in the upper-right corner of the Report window.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="4b336-123">Фильтры</span><span class="sxs-lookup"><span data-stu-id="4b336-123">Filters</span></span>

<span data-ttu-id="4b336-p103">Фильтры позволяют вам возвратить уточненный набор данных или просматривать возвращенные данные различными способами. В следующей таблице перечислены фильтры, которые вы можете использовать в отчете об одноранговой голосовой связи и видеосвязи.</span><span class="sxs-lookup"><span data-stu-id="4b336-p103">Filters provide a way for you to return a more finely targeted set of data or to view the data in different ways. The following table lists the filters that you can use with the Peer-to-Peer Voice and Video Report.</span></span>

### <a name="peer-to-peer-voice-and-video-report-filters"></a><span data-ttu-id="4b336-126">Фильтры отчета об одноранговой голосовой связи и видеосвязи</span><span class="sxs-lookup"><span data-stu-id="4b336-126">Peer-to-peer voice and video report filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4b336-127">Имя</span><span class="sxs-lookup"><span data-stu-id="4b336-127">Name</span></span></th>
<th><span data-ttu-id="4b336-128">Описание</span><span class="sxs-lookup"><span data-stu-id="4b336-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4b336-129"><strong>От</strong></span><span class="sxs-lookup"><span data-stu-id="4b336-129"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="4b336-p104">Начальная дата и начальное время для диапазона времени. Чтобы просмотреть данные по часам, введите начальную дату и начальное время в следующем формате:</span><span class="sxs-lookup"><span data-stu-id="4b336-p104">Start date and time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="4b336-132">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="4b336-132">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="4b336-p105">Если вы не вводите начальное время, отчет автоматически начинается с 12:00 AM указанного дня. Чтобы просмотреть данные по дням, просто введите дату:</span><span class="sxs-lookup"><span data-stu-id="4b336-p105">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="4b336-135">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="4b336-135">7/7/2012</span></span></p>
<p><span data-ttu-id="4b336-136">Чтобы просмотреть данные за неделю или месяц, введите дату, выпадающую на любое время в рамках недели или месяца, которые вы хотите просмотреть (вам не требуется вводить первый день недели или месяца):</span><span class="sxs-lookup"><span data-stu-id="4b336-136">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="4b336-137">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="4b336-137">7/3/2012</span></span></p>
<p><span data-ttu-id="4b336-138">Недели всегда отсчитываются с воскресенья по субботу.</span><span class="sxs-lookup"><span data-stu-id="4b336-138">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b336-139"><strong>До</strong></span><span class="sxs-lookup"><span data-stu-id="4b336-139"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="4b336-p106">Конечные дата/время для временного диапазона. Чтобы просмотреть данные по часам, введите конечные дату и время следующим образом:</span><span class="sxs-lookup"><span data-stu-id="4b336-p106">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="4b336-142">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="4b336-142">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="4b336-p107">Если вы не вводите конечное время, отчет автоматически заканчивается в 12:00 AM указанного дня. Чтобы просмотреть данные по дням, просто введите дату:</span><span class="sxs-lookup"><span data-stu-id="4b336-p107">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="4b336-145">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="4b336-145">7/7/2012</span></span></p>
<p><span data-ttu-id="4b336-146">Чтобы просмотреть данные за неделю или месяц, введите дату, выпадающую на любое время в рамках недели или месяца, которые вы хотите просмотреть (вам не требуется вводить первый день недели или месяца):</span><span class="sxs-lookup"><span data-stu-id="4b336-146">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="4b336-147">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="4b336-147">7/3/2012</span></span></p>
<p><span data-ttu-id="4b336-148">Недели всегда отсчитываются с воскресенья по субботу.</span><span class="sxs-lookup"><span data-stu-id="4b336-148">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b336-149"><strong>Интервал</strong></span><span class="sxs-lookup"><span data-stu-id="4b336-149"><strong>Interval</strong></span></span></p></td>
<td><p><span data-ttu-id="4b336-p108">Временной интервал. Выберите одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="4b336-p108">Time interval. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="4b336-152">Ежечасно (можно отобразить не более 25 часов)</span><span class="sxs-lookup"><span data-stu-id="4b336-152">Hourly (a maximum of 25 hours can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="4b336-153">Ежедневно (можно отобразить не более 31 дня)</span><span class="sxs-lookup"><span data-stu-id="4b336-153">Daily (a maximum of 31 days can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="4b336-154">Еженедельно (можно отобразить не более 12 недель)</span><span class="sxs-lookup"><span data-stu-id="4b336-154">Weekly (a maximum of 12 weeks can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="4b336-155">Ежемесячно (можно отобразить не более 12 месяцев)</span><span class="sxs-lookup"><span data-stu-id="4b336-155">Monthly (a maximum of 12 months can be displayed)</span></span></p></li>
</ul>
<p><span data-ttu-id="4b336-156">Если количество значений между начальной и конечной датами превышает максимально допустимое для выбранного интервала, отображается максимальное возможное количество значений (от начальной даты и далее).</span><span class="sxs-lookup"><span data-stu-id="4b336-156">If the start and end dates exceed the maximum number of values allowed for the selected interval, only the maximum number of values (starting from the start date) is displayed.</span></span> <span data-ttu-id="4b336-157">Например, если выбрать ежедневный интервал с датой начала 7/7/2012 и датой окончания 2/28/2012, данные будут выводиться для дней 8/7/2012 12:00 – 9/7/2012 12:00 AM (то есть, всего за 31 дня).</span><span class="sxs-lookup"><span data-stu-id="4b336-157">For example, if you select the Daily interval with a start date of 7/7/2012 and an end date of 2/28/2012, data is displayed for the days 8/7/2012 12:00 AM to 9/7/2012 12:00 AM (that is, a total of 31 days' worth of data).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b336-158"><strong>Тип мультимедиа</strong></span><span class="sxs-lookup"><span data-stu-id="4b336-158"><strong>Media type</strong></span></span></p></td>
<td><p><span data-ttu-id="4b336-p110">Указывает используемый в сеансе тип мультимедиа. Выберите одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="4b336-p110">Indicates the type of media used in the session. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="4b336-161">Both</span><span class="sxs-lookup"><span data-stu-id="4b336-161">Both</span></span></p></li>
<li><p><span data-ttu-id="4b336-162">Аудио</span><span class="sxs-lookup"><span data-stu-id="4b336-162">Audio</span></span></p></li>
<li><p><span data-ttu-id="4b336-163">Видео</span><span class="sxs-lookup"><span data-stu-id="4b336-163">Video</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b336-164"><strong>Расположение звонка</strong></span><span class="sxs-lookup"><span data-stu-id="4b336-164"><strong>Call disposition</strong></span></span></p></td>
<td><p><span data-ttu-id="4b336-p111">Указывает, был ли сеанс успешным. Выберите одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="4b336-p111">Indicates the success or failure of the session. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="4b336-167">[All] (Все)</span><span class="sxs-lookup"><span data-stu-id="4b336-167">[All]</span></span></p></li>
<li><p><span data-ttu-id="4b336-168">Success Calls (Успешные звонки)</span><span class="sxs-lookup"><span data-stu-id="4b336-168">Success Calls</span></span></p></li>
<li><p><span data-ttu-id="4b336-169">Failed Calls (Звонки со сбоем)</span><span class="sxs-lookup"><span data-stu-id="4b336-169">Failed Calls</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b336-170"><strong>Report by (Отчетность)</strong></span><span class="sxs-lookup"><span data-stu-id="4b336-170"><strong>Report by</strong></span></span></p></td>
<td><p><span data-ttu-id="4b336-p112">Указывает значения для использования в отчете. Выберите одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="4b336-p112">Indicates the values to be used in the report. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="4b336-173">Session count (Число сеансов)</span><span class="sxs-lookup"><span data-stu-id="4b336-173">Session count</span></span></p></li>
<li><p><span data-ttu-id="4b336-174">Call minutes (Число минут звонков)</span><span class="sxs-lookup"><span data-stu-id="4b336-174">Call minutes</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-peer-to-peer-voice-and-video-activity-by-pool"></a><span data-ttu-id="4b336-175">Метрики для операций одноранговой голосовой связи и видеосвязи по пулам</span><span class="sxs-lookup"><span data-stu-id="4b336-175">Metrics for peer-to-peer voice and video activity by Pool</span></span>

<span data-ttu-id="4b336-176">В следующей таблице перечислены сведения, представленные в отчете об одноранговой голосовой связи и видеосвязи для каждого пула.</span><span class="sxs-lookup"><span data-stu-id="4b336-176">The following table lists the information provided in the Peer-to-Peer Voice and Video Report for each pool.</span></span>

### <a name="metrics-for-peer-to-peer-voice-and-video-activity-by-pool"></a><span data-ttu-id="4b336-177">Метрики для операций одноранговой голосовой связи и видеосвязи по пулам</span><span class="sxs-lookup"><span data-stu-id="4b336-177">Metrics for peer-to-peer voice and video activity by pool</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4b336-178">Имя</span><span class="sxs-lookup"><span data-stu-id="4b336-178">Name</span></span></th>
<th><span data-ttu-id="4b336-179">Поддержка сортировки</span><span class="sxs-lookup"><span data-stu-id="4b336-179">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="4b336-180">Описание</span><span class="sxs-lookup"><span data-stu-id="4b336-180">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4b336-181"><strong>Пул</strong></span><span class="sxs-lookup"><span data-stu-id="4b336-181"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="4b336-182">Нет</span><span class="sxs-lookup"><span data-stu-id="4b336-182">No</span></span></p></td>
<td><p><span data-ttu-id="4b336-183">Имя пула регистраторов или пограничного сервера, используемого для звонка.</span><span class="sxs-lookup"><span data-stu-id="4b336-183">Name of the Registrar pool or Edge Server used for the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b336-184"><strong>Дата/время</strong></span><span class="sxs-lookup"><span data-stu-id="4b336-184"><strong>Date/Time</strong></span></span></p></td>
<td><p><span data-ttu-id="4b336-185">Нет</span><span class="sxs-lookup"><span data-stu-id="4b336-185">No</span></span></p></td>
<td><p><span data-ttu-id="4b336-186">Дата и период времени, когда был выполнен звонок.</span><span class="sxs-lookup"><span data-stu-id="4b336-186">Date and time period in which the call took place.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b336-187"><strong>Всего</strong></span><span class="sxs-lookup"><span data-stu-id="4b336-187"><strong>Total</strong></span></span></p></td>
<td><p><span data-ttu-id="4b336-188">Нет</span><span class="sxs-lookup"><span data-stu-id="4b336-188">No</span></span></p></td>
<td><p><span data-ttu-id="4b336-189">Общее число сеансов или сообщений.</span><span class="sxs-lookup"><span data-stu-id="4b336-189">Total number of sessions or total message count.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-peer-to-peer-voice-and-video-activity-by-call-type"></a><span data-ttu-id="4b336-190">Метрики для операций одноранговой голосовой связи и видеосвязи по типу вызова</span><span class="sxs-lookup"><span data-stu-id="4b336-190">Metrics for peer-to-peer voice and video activity by call type</span></span>

<span data-ttu-id="4b336-191">В следующей таблице перечислены сведения, представленные в отчете об одноранговой голосовой связи и видеосвязи для каждого типа выполненных звонков.</span><span class="sxs-lookup"><span data-stu-id="4b336-191">The following table lists the information provided in the Peer-to-Peer Voice and Video Report for each type of call that was made.</span></span>

### <a name="metrics-for-peer-to-peer-voice-and-video-activity-by-call-type"></a><span data-ttu-id="4b336-192">Метрики для операций одноранговой голосовой связи и видеосвязи по типу вызова</span><span class="sxs-lookup"><span data-stu-id="4b336-192">Metrics for peer-to-peer voice and video activity by call type</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4b336-193">Имя</span><span class="sxs-lookup"><span data-stu-id="4b336-193">Name</span></span></th>
<th><span data-ttu-id="4b336-194">Поддержка сортировки</span><span class="sxs-lookup"><span data-stu-id="4b336-194">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="4b336-195">Описание</span><span class="sxs-lookup"><span data-stu-id="4b336-195">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4b336-196"><strong>Тип вызова</strong></span><span class="sxs-lookup"><span data-stu-id="4b336-196"><strong>Call type</strong></span></span></p></td>
<td><p><span data-ttu-id="4b336-197">Нет</span><span class="sxs-lookup"><span data-stu-id="4b336-197">No</span></span></p></td>
<td><p><span data-ttu-id="4b336-p113">Указывает тип выполненного звонка. Доступны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="4b336-p113">Indicates the type of call that was made. Values are one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="4b336-200">UC-to-UC (Из объединенных коммуникаций в объединенные коммуникации)</span><span class="sxs-lookup"><span data-stu-id="4b336-200">UC-to-UC</span></span></p></li>
<li><p><span data-ttu-id="4b336-201">UC-to-PSTN (Из объединенных коммуникаций в ТСОП)</span><span class="sxs-lookup"><span data-stu-id="4b336-201">UC-to-PSTN</span></span></p></li>
<li><p><span data-ttu-id="4b336-202">PSTN-to-UC (Из ТСОП в объединенные коммуникации)</span><span class="sxs-lookup"><span data-stu-id="4b336-202">PSTN-to-UC</span></span></p></li>
<li><p><span data-ttu-id="4b336-203">PSTN-to-PSTN (Из ТСОП в ТСОП)</span><span class="sxs-lookup"><span data-stu-id="4b336-203">PSTN-to-PSTN</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b336-204"><strong>Дата/время</strong></span><span class="sxs-lookup"><span data-stu-id="4b336-204"><strong>Date/Time</strong></span></span></p></td>
<td><p><span data-ttu-id="4b336-205">Нет</span><span class="sxs-lookup"><span data-stu-id="4b336-205">No</span></span></p></td>
<td><p><span data-ttu-id="4b336-206">Дата и период времени, когда был выполнен звонок.</span><span class="sxs-lookup"><span data-stu-id="4b336-206">Date and time period in which the call took place.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b336-207"><strong>Всего</strong></span><span class="sxs-lookup"><span data-stu-id="4b336-207"><strong>Total</strong></span></span></p></td>
<td><p><span data-ttu-id="4b336-208">Нет</span><span class="sxs-lookup"><span data-stu-id="4b336-208">No</span></span></p></td>
<td><p><span data-ttu-id="4b336-209">Общее число сеансов или сообщений.</span><span class="sxs-lookup"><span data-stu-id="4b336-209">Total number of sessions or total message count.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-peer-to-peer-voice-and-video-activity-by-access-type"></a><span data-ttu-id="4b336-210">Метрики для операций одноранговой голосовой связи и видеосвязи по типу доступа</span><span class="sxs-lookup"><span data-stu-id="4b336-210">Metrics for peer-to-peer voice and video activity by access type</span></span>

<span data-ttu-id="4b336-211">В следующей таблице перечислены сведения, представленные в отчете об одноранговой голосовой связи и видеосвязи для каждого типа сетевого доступа.</span><span class="sxs-lookup"><span data-stu-id="4b336-211">The following table lists the information provided in the Peer-to-Peer Voice and Video Report for each network access type.</span></span>

### <a name="metrics-for-peer-to-peer-voice-and-video-activity-by-access-type"></a><span data-ttu-id="4b336-212">Метрики для операций одноранговой голосовой связи и видеосвязи по типу доступа</span><span class="sxs-lookup"><span data-stu-id="4b336-212">Metrics for peer-to-peer voice and video activity by access type</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4b336-213">Имя</span><span class="sxs-lookup"><span data-stu-id="4b336-213">Name</span></span></th>
<th><span data-ttu-id="4b336-214">Поддержка сортировки</span><span class="sxs-lookup"><span data-stu-id="4b336-214">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="4b336-215">Описание</span><span class="sxs-lookup"><span data-stu-id="4b336-215">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4b336-216"><strong>Тип сеанса</strong></span><span class="sxs-lookup"><span data-stu-id="4b336-216"><strong>Activity type</strong></span></span></p></td>
<td><p><span data-ttu-id="4b336-217">Нет</span><span class="sxs-lookup"><span data-stu-id="4b336-217">No</span></span></p></td>
<td><p><span data-ttu-id="4b336-p114">Указывает, выполняли ли клиенты вход во внутреннюю или во внешнюю сеть при совершении звонка. Обычно доступны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="4b336-p114">Indicates whether the clients were logged on to the internal network or the external network when the call was placed. Values are typically one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="4b336-220">Internal</span><span class="sxs-lookup"><span data-stu-id="4b336-220">Internal</span></span></p></li>
<li><p><span data-ttu-id="4b336-221">Внешняя</span><span class="sxs-lookup"><span data-stu-id="4b336-221">External</span></span></p></li>
<li><p><span data-ttu-id="4b336-222">Mixed (Обе)</span><span class="sxs-lookup"><span data-stu-id="4b336-222">Mixed</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b336-223"><strong>Дата/время</strong></span><span class="sxs-lookup"><span data-stu-id="4b336-223"><strong>Date/Time</strong></span></span></p></td>
<td><p><span data-ttu-id="4b336-224">Нет</span><span class="sxs-lookup"><span data-stu-id="4b336-224">No</span></span></p></td>
<td><p><span data-ttu-id="4b336-225">Дата и период времени, когда был выполнен звонок.</span><span class="sxs-lookup"><span data-stu-id="4b336-225">Date and time period in which the call took place.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b336-226"><strong>Всего</strong></span><span class="sxs-lookup"><span data-stu-id="4b336-226"><strong>Total</strong></span></span></p></td>
<td><p><span data-ttu-id="4b336-227">Нет</span><span class="sxs-lookup"><span data-stu-id="4b336-227">No</span></span></p></td>
<td><p><span data-ttu-id="4b336-228">Общее число сеансов или сообщений.</span><span class="sxs-lookup"><span data-stu-id="4b336-228">Total number of sessions or total message count.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-peer-to-peer-voice-and-video-activity-by-mediation-server"></a><span data-ttu-id="4b336-229">Метрики для операций одноранговой голосовой связи и видеосвязи по серверу-посреднику</span><span class="sxs-lookup"><span data-stu-id="4b336-229">Metrics for peer-to-peer voice and video activity by mediation server</span></span>

<span data-ttu-id="4b336-230">В таблице ниже приведены сведения, которые содержатся в видеоотчетах одноранговых и видеофайлов для каждого сервера-посредника.</span><span class="sxs-lookup"><span data-stu-id="4b336-230">The following table lists the information provided in the Peer-to-Peer Voice and Video Report for each Mediation Server.</span></span>

### <a name="metrics-for-peer-to-peer-voice-and-video-activity-by-mediation-server"></a><span data-ttu-id="4b336-231">Метрики для операций одноранговой голосовой связи и видеосвязи по серверу-посреднику</span><span class="sxs-lookup"><span data-stu-id="4b336-231">Metrics for peer-to-peer voice and video activity by mediation server</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4b336-232">Имя</span><span class="sxs-lookup"><span data-stu-id="4b336-232">Name</span></span></th>
<th><span data-ttu-id="4b336-233">Поддержка сортировки</span><span class="sxs-lookup"><span data-stu-id="4b336-233">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="4b336-234">Описание</span><span class="sxs-lookup"><span data-stu-id="4b336-234">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4b336-235"><strong>посредник</strong></span><span class="sxs-lookup"><span data-stu-id="4b336-235"><strong>Mediation Server</strong></span></span></p></td>
<td><p><span data-ttu-id="4b336-236">Нет</span><span class="sxs-lookup"><span data-stu-id="4b336-236">No</span></span></p></td>
<td><p><span data-ttu-id="4b336-237">Имя сервера обновлений.</span><span class="sxs-lookup"><span data-stu-id="4b336-237">Name of the Mediation Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b336-238"><strong>Дата/время</strong></span><span class="sxs-lookup"><span data-stu-id="4b336-238"><strong>Date/Time</strong></span></span></p></td>
<td><p><span data-ttu-id="4b336-239">Нет</span><span class="sxs-lookup"><span data-stu-id="4b336-239">No</span></span></p></td>
<td><p><span data-ttu-id="4b336-240">Дата и период времени, когда был выполнен звонок.</span><span class="sxs-lookup"><span data-stu-id="4b336-240">Date and time period in which the call took place.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b336-241"><strong>Всего</strong></span><span class="sxs-lookup"><span data-stu-id="4b336-241"><strong>Total</strong></span></span></p></td>
<td><p><span data-ttu-id="4b336-242">Нет</span><span class="sxs-lookup"><span data-stu-id="4b336-242">No</span></span></p></td>
<td><p><span data-ttu-id="4b336-243">Общее число сеансов или сообщений.</span><span class="sxs-lookup"><span data-stu-id="4b336-243">Total number of sessions or total message count.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="4b336-244">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4b336-244">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

