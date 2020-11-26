---
title: 'Lync Server 2013: сводный отчет о качестве качества мультимедиа'
description: 'Lync Server 2013: сводный отчет о качестве качества мультимедиа.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Media Quality Summary Report
ms:assetid: 8bd59ad6-3087-49c8-b692-5573fe2ffcd8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615012(v=OCS.15)
ms:contentKeyID: 48184776
ms.date: 06/29/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2616b7e3cdea9df7b004745a5c407188870903c7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446047"
---
# <a name="media-quality-summary-report-in-lync-server-2013"></a><span data-ttu-id="ea3ef-103">Сводный отчет о качестве качества мультимедиа в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ea3ef-103">Media Quality Summary Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ea3ef-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ea3ef-104">

<span> </span></span></span>

<span data-ttu-id="ea3ef-105">_**Тема последнего изменения:** 2016-06-29_</span><span class="sxs-lookup"><span data-stu-id="ea3ef-105">_**Topic Last Modified:** 2016-06-29_</span></span>

<span data-ttu-id="ea3ef-106">Сводный отчет по качеству мультимедиа, возможно, является лучшим предложением для анализа качества звонков в организации: он предоставляет подробные метрики качества взаимодействия при вызовах, распределенные по следующим категориям:</span><span class="sxs-lookup"><span data-stu-id="ea3ef-106">The Media Quality Summary Report is perhaps your best bet for analyzing call quality in your organization: this report provides detailed Quality of Experience (QoE) call metrics broken down into the following categories:</span></span>

  - <span data-ttu-id="ea3ef-107">Одноранговые вызовы Объединенных коммуникаций (например, Microsoft Lync 2013 to Microsoft Lync 2013)</span><span class="sxs-lookup"><span data-stu-id="ea3ef-107">UC Peer to Peer Calls (such as a Microsoft Lync 2013 to Microsoft Lync 2013 call)</span></span>

  - <span data-ttu-id="ea3ef-108">Сеансы конференц-связи по объединенным коммуникациям</span><span class="sxs-lookup"><span data-stu-id="ea3ef-108">UC Conference Sessions</span></span>

  - <span data-ttu-id="ea3ef-109">Сеансы конференц-связи по ТСОП</span><span class="sxs-lookup"><span data-stu-id="ea3ef-109">PSTN Conference Sessions</span></span>

  - <span data-ttu-id="ea3ef-110">Звонки по ТСОП: обходной канал передачи медиаданных</span><span class="sxs-lookup"><span data-stu-id="ea3ef-110">PSTN Calls: Media Bypass</span></span>

  - <span data-ttu-id="ea3ef-111">Звонки по ТСОП (без обхода): ветвь объединенных коммуникаций</span><span class="sxs-lookup"><span data-stu-id="ea3ef-111">PSTN Calls (Non-Bypass): UC Leg</span></span>

  - <span data-ttu-id="ea3ef-112">Звонки по ТСОП (без обхода): ветвь шлюза</span><span class="sxs-lookup"><span data-stu-id="ea3ef-112">PSTN Calls (Non-Bypass): Gateway Leg</span></span>

  - <span data-ttu-id="ea3ef-113">Другие типы звонков</span><span class="sxs-lookup"><span data-stu-id="ea3ef-113">Other Call Types</span></span>

<span data-ttu-id="ea3ef-114">При первом открытии отчета отображается сводка по каждой из этих категорий.</span><span class="sxs-lookup"><span data-stu-id="ea3ef-114">When you first open the report, you see summary information for each of these categories.</span></span> <span data-ttu-id="ea3ef-115">Не выходя из отчета, вы можете развернуть каждую категорию, чтобы просмотреть подкатегории, такие как звонки из Office Communicator 2007 R2 в Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="ea3ef-115">Without leaving the report, you can expand each category to look at subcategories such as calls made from Office Communicator 2007 R2 to Lync 2013.</span></span> <span data-ttu-id="ea3ef-116">Затем можно также детализировать эти подкатегории, чтобы просмотреть сведения о каждом вызове, сделанном в этой подкатегории.</span><span class="sxs-lookup"><span data-stu-id="ea3ef-116">In turn, you can then drill down into these subcategories to see details about each call made within that subcategory.</span></span>

<span data-ttu-id="ea3ef-117">В Microsoft Lync Server 2013 в отчете "Обзор качества мультимедиа" дополнительно разбиваются данные на три типа звонков: голосовые звонки, видеозвонки и обмен звонками между приложениями.</span><span class="sxs-lookup"><span data-stu-id="ea3ef-117">In Microsoft Lync Server 2013 the Media Quality Summary Report further breaks the data down into three call types: audio calls, video calls, and application sharing calls.</span></span> <span data-ttu-id="ea3ef-118">Для каждого типа вызова в отчете имеется свой собственный раздел и свой собственный ряд метрик вызова.</span><span class="sxs-lookup"><span data-stu-id="ea3ef-118">Each call type has its own section in the report, and its own custom set of call metrics.</span></span>

<span data-ttu-id="ea3ef-119">Кроме того, сводный отчет по качеству мультимедиа позволяет применять фильтры, чтобы сравнивать качество проводных и беспроводных вызовов, внутренних и внешних вызовов, а также вызовов с использованием VPN и вызовов без VPN.</span><span class="sxs-lookup"><span data-stu-id="ea3ef-119">The Media Quality Summary Report also allows you to apply filters that enable you to compare the call quality of wired calls vs. wireless calls, internal calls vs. external calls, and VPN calls vs. non-VPN calls.</span></span>

<div>

## <a name="accessing-the-media-quality-summary-report"></a><span data-ttu-id="ea3ef-120">Доступ к сводному отчету по качеству мультимедиа</span><span class="sxs-lookup"><span data-stu-id="ea3ef-120">Accessing the Media Quality Summary Report</span></span>

<span data-ttu-id="ea3ef-121">Сводный отчет по качеству мультимедиа можно вызвать на домашней странице отчетов наблюдения.</span><span class="sxs-lookup"><span data-stu-id="ea3ef-121">The Media Quality Summary Report is accessed from the Monitoring Reports home page.</span></span> <span data-ttu-id="ea3ef-122">Вы можете перейти к [отчету список обзвона в Lync Server 2013](lync-server-2013-call-list-report.md) , щелкнув один из следующих метрик:</span><span class="sxs-lookup"><span data-stu-id="ea3ef-122">You can drill down to the [Call List Report in Lync Server 2013](lync-server-2013-call-list-report.md) by clicking either of the following metrics:</span></span>

  - <span data-ttu-id="ea3ef-123">Громкость вызова</span><span class="sxs-lookup"><span data-stu-id="ea3ef-123">Call volume</span></span>

  - <span data-ttu-id="ea3ef-124">Процент звонков низкого качества</span><span class="sxs-lookup"><span data-stu-id="ea3ef-124">Poor call percentage</span></span>

<span data-ttu-id="ea3ef-125">Кроме того, можно вызвать отчет по распределению метрик качества мультимедиа, щелкнув какую-либо из метрик звонка:</span><span class="sxs-lookup"><span data-stu-id="ea3ef-125">In addition, you can access the Media Quality Metrics Distribution Report by clicking any of the following audio call metrics:</span></span>

  - <span data-ttu-id="ea3ef-126">Круговой путь (мс)</span><span class="sxs-lookup"><span data-stu-id="ea3ef-126">Round trip (ms)</span></span>

  - <span data-ttu-id="ea3ef-127">Падение качества (средняя оценка)</span><span class="sxs-lookup"><span data-stu-id="ea3ef-127">Degradation (MOS)</span></span>

  - <span data-ttu-id="ea3ef-128">Потеря пакетов</span><span class="sxs-lookup"><span data-stu-id="ea3ef-128">Packet loss</span></span>

  - <span data-ttu-id="ea3ef-129">Колебание (мс)</span><span class="sxs-lookup"><span data-stu-id="ea3ef-129">Jitter (ms)</span></span>

  - <span data-ttu-id="ea3ef-130">Степень маскированных аудиообразцов</span><span class="sxs-lookup"><span data-stu-id="ea3ef-130">Healer concealed ratio</span></span>

  - <span data-ttu-id="ea3ef-131">Степень растянутых образцов</span><span class="sxs-lookup"><span data-stu-id="ea3ef-131">Healer stretched ratio</span></span>

  - <span data-ttu-id="ea3ef-132">Степень сжатых аудиообразцов</span><span class="sxs-lookup"><span data-stu-id="ea3ef-132">Healer compressed ratio</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="ea3ef-133">Фильтры</span><span class="sxs-lookup"><span data-stu-id="ea3ef-133">Filters</span></span>

<span data-ttu-id="ea3ef-p104">Фильтры позволяют получать более адресный набор данных или просматривать полученные данные разными способами. Например, в сводном отчете по качеству мультимедиа можно фильтровать данные по типу доступа (т.е. по внутреннему или внешнему доступу), а также по проводному или беспроводному типу подключения. Кроме того, можно выбрать способ группирования данных. В данном случае вызовы группируются по часу, дню, неделе или месяцу.</span><span class="sxs-lookup"><span data-stu-id="ea3ef-p104">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. For example, the Media Quality Summary Report enables you to filter the returned data by such things as access type (that is, interval access vs. external access) or by wired/wireless network connection. You can also choose how data should be grouped. In this case, calls are grouped by hour, day, week, or month.</span></span>

<span data-ttu-id="ea3ef-138">В следующей таблице приведены фильтры, которые можно использовать в сводном отчете по качеству мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="ea3ef-138">The following table lists the filters that you can use with the Media Quality Summary Report.</span></span>

### <a name="media-quality-summary-report-filters"></a><span data-ttu-id="ea3ef-139">Фильтры сводного отчета по качеству мультимедиа</span><span class="sxs-lookup"><span data-stu-id="ea3ef-139">Media Quality Summary Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ea3ef-140">Имя</span><span class="sxs-lookup"><span data-stu-id="ea3ef-140">Name</span></span></th>
<th><span data-ttu-id="ea3ef-141">Описание</span><span class="sxs-lookup"><span data-stu-id="ea3ef-141">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ea3ef-142"><strong>От</strong></span><span class="sxs-lookup"><span data-stu-id="ea3ef-142"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="ea3ef-p105">Начальные дата/время для временного диапазона. Чтобы просмотреть данные по часам, введите начальные дату и время следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ea3ef-p105">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="ea3ef-145">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="ea3ef-145">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="ea3ef-p106">Если вы не вводите начальное время, отчет автоматически начинается с 12:00 AM указанного дня. Чтобы просмотреть данные по дням, просто введите дату:</span><span class="sxs-lookup"><span data-stu-id="ea3ef-p106">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="ea3ef-148">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="ea3ef-148">7/7/2012</span></span></p>
<p><span data-ttu-id="ea3ef-149">Чтобы просмотреть данные за неделю или месяц, введите дату, выпадающую на любое время в рамках недели или месяца, которые вы хотите просмотреть (вам не требуется вводить первый день недели или месяца):</span><span class="sxs-lookup"><span data-stu-id="ea3ef-149">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="ea3ef-150">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="ea3ef-150">7/3/2012</span></span></p>
<p><span data-ttu-id="ea3ef-151">Недели всегда отсчитываются с воскресенья по субботу.</span><span class="sxs-lookup"><span data-stu-id="ea3ef-151">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea3ef-152"><strong>До</strong></span><span class="sxs-lookup"><span data-stu-id="ea3ef-152"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="ea3ef-p107">Конечные дата/время для временного диапазона. Чтобы просмотреть данные по часам, введите конечные дату и время следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ea3ef-p107">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="ea3ef-155">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="ea3ef-155">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="ea3ef-p108">Если вы не вводите конечное время, отчет автоматически заканчивается в 12:00 AM указанного дня. Чтобы просмотреть данные по дням, просто введите дату:</span><span class="sxs-lookup"><span data-stu-id="ea3ef-p108">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="ea3ef-158">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="ea3ef-158">7/7/2012</span></span></p>
<p><span data-ttu-id="ea3ef-159">Чтобы просмотреть данные за неделю или месяц, введите дату, выпадающую на любое время в рамках недели или месяца, которые вы хотите просмотреть (вам не требуется вводить первый день недели или месяца):</span><span class="sxs-lookup"><span data-stu-id="ea3ef-159">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="ea3ef-160">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="ea3ef-160">7/3/2012</span></span></p>
<p><span data-ttu-id="ea3ef-161">Недели всегда отсчитываются с воскресенья по субботу.</span><span class="sxs-lookup"><span data-stu-id="ea3ef-161">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea3ef-162"><strong>Тип доступа</strong></span><span class="sxs-lookup"><span data-stu-id="ea3ef-162"><strong>Access type</strong></span></span></p></td>
<td><p><span data-ttu-id="ea3ef-p109">Определяет, был ли клиент зарегистрирован во внутренней сети или внешней сети при выполнении вызова. Выберите один из следующих вариантов:</span><span class="sxs-lookup"><span data-stu-id="ea3ef-p109">Indicates whether the client was logged on to the internal network or the external network when the call was placed. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="ea3ef-165">[All] (Все)</span><span class="sxs-lookup"><span data-stu-id="ea3ef-165">[All]</span></span></p></li>
<li><p><span data-ttu-id="ea3ef-166">Internal</span><span class="sxs-lookup"><span data-stu-id="ea3ef-166">Internal</span></span></p></li>
<li><p><span data-ttu-id="ea3ef-167">Внешняя</span><span class="sxs-lookup"><span data-stu-id="ea3ef-167">External</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea3ef-168"><strong>Тип сети</strong></span><span class="sxs-lookup"><span data-stu-id="ea3ef-168"><strong>Network type</strong></span></span></p></td>
<td><p><span data-ttu-id="ea3ef-p110">Определяет тип сети, к которой был подключен клиент при выполнении вызова. Выберите один из следующих вариантов:</span><span class="sxs-lookup"><span data-stu-id="ea3ef-p110">Indicates the type of network the client was connected to when the call was placed. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="ea3ef-171">[All] (Все)</span><span class="sxs-lookup"><span data-stu-id="ea3ef-171">[All]</span></span></p></li>
<li><p><span data-ttu-id="ea3ef-172">Проводная</span><span class="sxs-lookup"><span data-stu-id="ea3ef-172">Wired</span></span></p></li>
<li><p><span data-ttu-id="ea3ef-173">Беспроводная</span><span class="sxs-lookup"><span data-stu-id="ea3ef-173">Wireless</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea3ef-174"><strong>VPN</strong></span><span class="sxs-lookup"><span data-stu-id="ea3ef-174"><strong>VPN</strong></span></span></p></td>
<td><p><span data-ttu-id="ea3ef-p111">Указывает, использовал ли внешний клиент подключение посредством виртуальной частной сети (VPN) при выполнении вызова. Выберите один из следующих вариантов:</span><span class="sxs-lookup"><span data-stu-id="ea3ef-p111">Indicates whether an external client was using a virtual private network (VPN) connection when the call was placed. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="ea3ef-177">[All] (Все)</span><span class="sxs-lookup"><span data-stu-id="ea3ef-177">[All]</span></span></p></li>
<li><p><span data-ttu-id="ea3ef-178">VPN</span><span class="sxs-lookup"><span data-stu-id="ea3ef-178">VPN</span></span></p></li>
<li><p><span data-ttu-id="ea3ef-179">Не VPN</span><span class="sxs-lookup"><span data-stu-id="ea3ef-179">Non-VPN</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics"></a><span data-ttu-id="ea3ef-180">Показатели</span><span class="sxs-lookup"><span data-stu-id="ea3ef-180">Metrics</span></span>

<span data-ttu-id="ea3ef-181">В следующей таблице приведены сведения, которые предоставляют сводный отчет по качеству мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="ea3ef-181">The following table lists the information provided in the Media Quality Summary Report.</span></span>

### <a name="media-quality-summary-report-metrics-audio-call-summary"></a><span data-ttu-id="ea3ef-182">Метрики сводного отчета по качеству мультимедиа: сводка по голосовым вызовам</span><span class="sxs-lookup"><span data-stu-id="ea3ef-182">Media Quality Summary Report Metrics: Audio Call Summary</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ea3ef-183">Имя</span><span class="sxs-lookup"><span data-stu-id="ea3ef-183">Name</span></span></th>
<th><span data-ttu-id="ea3ef-184">Поддержка сортировки</span><span class="sxs-lookup"><span data-stu-id="ea3ef-184">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="ea3ef-185">Описание</span><span class="sxs-lookup"><span data-stu-id="ea3ef-185">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ea3ef-186"><strong>Тип звонка и конечной точки</strong></span><span class="sxs-lookup"><span data-stu-id="ea3ef-186"><strong>Call type/Endpoint type</strong></span></span></p></td>
<td><p><span data-ttu-id="ea3ef-187">Нет</span><span class="sxs-lookup"><span data-stu-id="ea3ef-187">No</span></span></p></td>
<td><p><span data-ttu-id="ea3ef-p112">При щелчке этого элемента отчет предоставляет подробные сведения о звонках, основанных на этом типе. Типы звонков:</span><span class="sxs-lookup"><span data-stu-id="ea3ef-p112">When you click this item, the report shows detailed information about calls based on that type. Call types include:</span></span></p>
<ul>
<li><p><span data-ttu-id="ea3ef-190">Одноранговые звонки по объединенным коммуникациям</span><span class="sxs-lookup"><span data-stu-id="ea3ef-190">UC Peer-to-Peer Calls</span></span></p></li>
<li><p><span data-ttu-id="ea3ef-191">Сеансы конференц-связи по объединенным коммуникациям</span><span class="sxs-lookup"><span data-stu-id="ea3ef-191">UC Conference Sessions</span></span></p></li>
<li><p><span data-ttu-id="ea3ef-192">Сеансы конференц-связи по ТСОП</span><span class="sxs-lookup"><span data-stu-id="ea3ef-192">PSTN Conference Sessions</span></span></p></li>
<li><p><span data-ttu-id="ea3ef-193">Звонки по ТСОП: обходной канал передачи медиаданных</span><span class="sxs-lookup"><span data-stu-id="ea3ef-193">PSTN Calls: Media Bypass</span></span></p></li>
<li><p><span data-ttu-id="ea3ef-194">Звонки по ТСОП (без обхода): ветвь объединенных коммуникаций</span><span class="sxs-lookup"><span data-stu-id="ea3ef-194">PSTN Calls (Non-Bypass): UC Leg</span></span></p></li>
<li><p><span data-ttu-id="ea3ef-195">Звонки по ТСОП (без обхода): ветвь шлюза</span><span class="sxs-lookup"><span data-stu-id="ea3ef-195">PSTN Calls (Non-Bypass): Gateway Leg</span></span></p></li>
<li><p><span data-ttu-id="ea3ef-196">Другие типы звонков</span><span class="sxs-lookup"><span data-stu-id="ea3ef-196">Other Call Types</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea3ef-197"><strong>Громкость вызова</strong></span><span class="sxs-lookup"><span data-stu-id="ea3ef-197"><strong>Call volume</strong></span></span></p></td>
<td><p><span data-ttu-id="ea3ef-198">Нет</span><span class="sxs-lookup"><span data-stu-id="ea3ef-198">No</span></span></p></td>
<td><p><span data-ttu-id="ea3ef-199">Общее количество звонков на тип звонка.</span><span class="sxs-lookup"><span data-stu-id="ea3ef-199">Total number of calls per call type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea3ef-200"><strong>Процент звонков низкого качества</strong></span><span class="sxs-lookup"><span data-stu-id="ea3ef-200"><strong>Poor call percentage</strong></span></span></p></td>
<td><p><span data-ttu-id="ea3ef-201">Нет</span><span class="sxs-lookup"><span data-stu-id="ea3ef-201">No</span></span></p></td>
<td><p><span data-ttu-id="ea3ef-p113">Общее количество звонков, классифицированных как звонки низкого качества. Звонок низкого качества – это любой звонок, хотя бы одна метрика которого превышает допустимое значение (например, звонок с чрезмерным дрожанием).</span><span class="sxs-lookup"><span data-stu-id="ea3ef-p113">Total number of calls classified as poor. A poor call is any call which at least one of the measured metrics exceeded the allowed value (for example, a call that experienced excessive jitter).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea3ef-204"><strong>Объем звонков (звонок по беспроводной сети)</strong></span><span class="sxs-lookup"><span data-stu-id="ea3ef-204"><strong>Call volume (wireless call)</strong></span></span></p></td>
<td><p><span data-ttu-id="ea3ef-205">Нет</span><span class="sxs-lookup"><span data-stu-id="ea3ef-205">No</span></span></p></td>
<td><p><span data-ttu-id="ea3ef-206">Общее количество звонков, при которых используется беспроводное подключение.</span><span class="sxs-lookup"><span data-stu-id="ea3ef-206">Total number of calls that used a wireless connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea3ef-207"><strong>Объем звонков (звонок по сети VPN)</strong></span><span class="sxs-lookup"><span data-stu-id="ea3ef-207"><strong>Call volume (VPN call)</strong></span></span></p></td>
<td><p><span data-ttu-id="ea3ef-208">Нет</span><span class="sxs-lookup"><span data-stu-id="ea3ef-208">No</span></span></p></td>
<td><p><span data-ttu-id="ea3ef-209">Общее количество звонков, при которых используется подключение по сети VPN.</span><span class="sxs-lookup"><span data-stu-id="ea3ef-209">Total number of calls that used a VPN connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea3ef-210"><strong>Объем звонков (внешний звонок)</strong></span><span class="sxs-lookup"><span data-stu-id="ea3ef-210"><strong>Call volume (external call)</strong></span></span></p></td>
<td><p><span data-ttu-id="ea3ef-211">Нет</span><span class="sxs-lookup"><span data-stu-id="ea3ef-211">No</span></span></p></td>
<td><p><span data-ttu-id="ea3ef-212">Количество звонков, при которых используется внешнее подключение (то есть подключение за пределами внутренней сети).</span><span class="sxs-lookup"><span data-stu-id="ea3ef-212">Number of calls that used an external connection (that is, a connection outside the internal network).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea3ef-213"><strong>Круговой путь (мс)</strong></span><span class="sxs-lookup"><span data-stu-id="ea3ef-213"><strong>Round trip (ms)</strong></span></span></p></td>
<td><p><span data-ttu-id="ea3ef-214">Нет</span><span class="sxs-lookup"><span data-stu-id="ea3ef-214">No</span></span></p></td>
<td><p><span data-ttu-id="ea3ef-p114">Среднее время (в миллисекундах) требуемое для передачи пакета протокола транспорта реального времени (RTP) в другую конечную точку и обратно. Круговой путь в 100 и меньше миллисекунд считается допустимым.</span><span class="sxs-lookup"><span data-stu-id="ea3ef-p114">Average amount of (in milliseconds) required for a real-time transport protocol (RTP) packet to travel to another endpoint and then back. Round-trip times of 100 milliseconds or less are considered of acceptable quality.</span></span></p>
<p><span data-ttu-id="ea3ef-p115">Высокие значения прохождения кругового пути могут быть вызваны маршрутизацией международных звонков, неправильной настройкой маршрутизацией или перегрузкой сервера-посредника. Большое время кругового пути приводит к трудностям при обслуживании двунаправленных аудиоразговоров.</span><span class="sxs-lookup"><span data-stu-id="ea3ef-p115">High round-trip values can be caused by international call routing, a routing misconfiguration, or an overloaded media server. High round-trip times result in difficulties with two-way, real-time audio conversations.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea3ef-219"><strong>Падение качества (средняя оценка)</strong></span><span class="sxs-lookup"><span data-stu-id="ea3ef-219"><strong>Degradation (MOS)</strong></span></span></p></td>
<td><p><span data-ttu-id="ea3ef-220">Нет</span><span class="sxs-lookup"><span data-stu-id="ea3ef-220">No</span></span></p></td>
<td><p><span data-ttu-id="ea3ef-221">Средняя экспертная оценка падения качества связи во время звонка.</span><span class="sxs-lookup"><span data-stu-id="ea3ef-221">Average amount of mean opinion score (MOS) degradation experienced during a call.</span></span> <span data-ttu-id="ea3ef-222">Значения лежат в диапазоне от 0,0 до 5,0.</span><span class="sxs-lookup"><span data-stu-id="ea3ef-222">Degradation values can range from a low of 0.0 to a high of 5.0.</span></span> <span data-ttu-id="ea3ef-223">Значение 0,5 или меньшее обозначает допустимое падение качества.</span><span class="sxs-lookup"><span data-stu-id="ea3ef-223">A value of 0.5 or less represents acceptable degradation.</span></span> <span data-ttu-id="ea3ef-224">Изначально средние оценки рассчитывались на основе оценок, даваемых звонкам пользователями по шкале от 1 до 5.</span><span class="sxs-lookup"><span data-stu-id="ea3ef-224">Historically, mean options scores were calculated by having users rate the quality of a call on a scale of 1-to-5.</span></span> <span data-ttu-id="ea3ef-225">В Lync Server Lync Server использует набор алгоритмов для прогнозирования того, как пользователи будут оценены при звонке.</span><span class="sxs-lookup"><span data-stu-id="ea3ef-225">In Lync Server, Lync Server uses a set of algorithms to predict how users would have rated a call.</span></span></p>
<p><span data-ttu-id="ea3ef-p117">Большие оценки падения качества могут быть вызваны перегрузкой сети, недостатком пропускной способности, помехами в беспроводной среде, перегрузкой на сервере-посреднике или конечной точке. Падение качества приводит к искажению или потере аудиосигнала.</span><span class="sxs-lookup"><span data-stu-id="ea3ef-p117">High degradation values can be caused by congestion, lack of bandwidth, wireless congestion or interference, or an overloaded media server or endpoint. High degradation results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea3ef-228"><strong>Потеря пакетов</strong></span><span class="sxs-lookup"><span data-stu-id="ea3ef-228"><strong>Packet loss</strong></span></span></p></td>
<td><p><span data-ttu-id="ea3ef-229">Нет</span><span class="sxs-lookup"><span data-stu-id="ea3ef-229">No</span></span></p></td>
<td><p><span data-ttu-id="ea3ef-p118">Среднее значение потери RTP-пакетов. (Пакет считается потерянным, если он не дошел до назначения). Большие значения потери пакетов могут быть вызваны перегрузкой сети, недостатком пропускной способности, помехами в беспроводной среде, перегрузкой на сервере-посреднике. Обычно это приводит к искажению или потере аудиосигнала.</span><span class="sxs-lookup"><span data-stu-id="ea3ef-p118">Average rate of RTP packet loss. (Packet loss occurs when RTP packets, a protocol used for transmitting audio and video across the Internet, failed to reach their destination.) High loss rates are generally caused by congestion, lack of bandwidth, wireless congestion or interference, or an overloaded media server. Packet loss typically results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea3ef-233"><strong>Колебание (мс)</strong></span><span class="sxs-lookup"><span data-stu-id="ea3ef-233"><strong>Jitter (ms)</strong></span></span></p></td>
<td><p><span data-ttu-id="ea3ef-234">Нет</span><span class="sxs-lookup"><span data-stu-id="ea3ef-234">No</span></span></p></td>
<td><p><span data-ttu-id="ea3ef-235">Среднее значение колебаний, зарегистрированных между прибытиями пакетов RTP.</span><span class="sxs-lookup"><span data-stu-id="ea3ef-235">Average jitter detected between RTP packet arrivals.</span></span> <span data-ttu-id="ea3ef-236">(Колебание — это мера &quot; shakiness &quot; звонка). Обычно значения с высокой степенью колебаний заключаются в результате перегруженности или перегруженного сервера мультимедиа, что приводит к искажению или потере звука.</span><span class="sxs-lookup"><span data-stu-id="ea3ef-236">(Jitter is a measure of the &quot;shakiness&quot; of a call.) High jitter values are typically caused by congestion or an overloaded media server, and result in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea3ef-237"><strong>Степень маскированных аудиообразцов</strong></span><span class="sxs-lookup"><span data-stu-id="ea3ef-237"><strong>Healer concealed ratio</strong></span></span></p></td>
<td><p><span data-ttu-id="ea3ef-238">Нет</span><span class="sxs-lookup"><span data-stu-id="ea3ef-238">No</span></span></p></td>
<td><p><span data-ttu-id="ea3ef-p120">Средняя степень маскированных аудиообразцов по отношению к общему числу образцов. (Маскирование аудио - это методика, которая применяется для сглаживания оборванной передачи, которая обычно происходит при потери сетевых пакетов). Большие значения обозначают частое применение данной методики, вызванной из-за потери пакетов или искажений сигнала.</span><span class="sxs-lookup"><span data-stu-id="ea3ef-p120">Average ratio of concealed audio samples to the total to the total number of samples. (A concealed audio sample is a technique used to smooth out the abrupt transition that would usually be caused by dropped network packets.) High values indicate significant levels of loss concealment applied caused by packet loss or jitter, and results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea3ef-241"><strong>Степень растянутых образцов</strong></span><span class="sxs-lookup"><span data-stu-id="ea3ef-241"><strong>Healer stretched ratio</strong></span></span></p></td>
<td><p><span data-ttu-id="ea3ef-242">Нет</span><span class="sxs-lookup"><span data-stu-id="ea3ef-242">No</span></span></p></td>
<td><p><span data-ttu-id="ea3ef-p121">Средняя степень растянутых аудиообразцов по отношению к общему числу образцов. (Растягивание аудиопакета - это методика, которая применяется для поддержания качества звонка при обнаружении потери сетевого пакета). Большие значения обозначают частое применение данной методики, вызванное большими искажениями – аудиосигнал звучит как роботизированный.</span><span class="sxs-lookup"><span data-stu-id="ea3ef-p121">Average ratio of stretched audio samples to the total to the total number of samples. (Stretched audio is audio that has been expanded to help maintain call quality when a dropped network packet has been detected.) High values indicate significant levels of sample stretching caused by jitter, and result in audio sounding robotic or distorted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea3ef-245"><strong>Степень сжатых аудиообразцов</strong></span><span class="sxs-lookup"><span data-stu-id="ea3ef-245"><strong>Healer compressed ratio</strong></span></span></p></td>
<td><p><span data-ttu-id="ea3ef-246">Нет</span><span class="sxs-lookup"><span data-stu-id="ea3ef-246">No</span></span></p></td>
<td><p><span data-ttu-id="ea3ef-p122">Средняя степень растянутых аудиообразцов по отношению к общему числу образцов. (Сжатие аудиопакета - это методика, которая применяется для поддержания качества звонка при обнаружении потери сетевого пакета). Большие значения обозначают частое применение данной методики, вызванное большими искажениями – аудиосигнал звучит как ускоренный или искаженный.</span><span class="sxs-lookup"><span data-stu-id="ea3ef-p122">Average ratio of compressed audio samples to the total number of samples. (Compressed audio is audio that has been compressed to help maintain call quality when a dropped network packet has been detected.) High values indicate significant levels of sample compression caused by jitter, and result in audio sounding accelerated or distorted.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="media-quality-summary-report-metrics-video-call-summary"></a><span data-ttu-id="ea3ef-249">Метрики сводного отчета по качеству мультимедиа: сводка по видеовызовам</span><span class="sxs-lookup"><span data-stu-id="ea3ef-249">Media Quality Summary Report Metrics: Video Call Summary</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ea3ef-250">Имя</span><span class="sxs-lookup"><span data-stu-id="ea3ef-250">Name</span></span></th>
<th><span data-ttu-id="ea3ef-251">Поддержка сортировки</span><span class="sxs-lookup"><span data-stu-id="ea3ef-251">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="ea3ef-252">Описание</span><span class="sxs-lookup"><span data-stu-id="ea3ef-252">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ea3ef-253"><strong>Тип звонка и конечной точки</strong></span><span class="sxs-lookup"><span data-stu-id="ea3ef-253"><strong>Call type/Endpoint type</strong></span></span></p></td>
<td><p><span data-ttu-id="ea3ef-254">Нет</span><span class="sxs-lookup"><span data-stu-id="ea3ef-254">No</span></span></p></td>
<td><p><span data-ttu-id="ea3ef-p123">При щелчке этого элемента отчет предоставляет подробные сведения о звонках, основанных на этом типе. Типы звонков:</span><span class="sxs-lookup"><span data-stu-id="ea3ef-p123">When you click this item, the report shows detailed information about calls based on that type. Call types include:</span></span></p>
<ul>
<li><p><span data-ttu-id="ea3ef-257">Одноранговые звонки по объединенным коммуникациям</span><span class="sxs-lookup"><span data-stu-id="ea3ef-257">UC Peer-to-Peer Calls</span></span></p></li>
<li><p><span data-ttu-id="ea3ef-258">Сеансы конференц-связи по объединенным коммуникациям</span><span class="sxs-lookup"><span data-stu-id="ea3ef-258">UC Conference Sessions</span></span></p></li>
<li><p><span data-ttu-id="ea3ef-259">Сеансы конференц-связи по ТСОП</span><span class="sxs-lookup"><span data-stu-id="ea3ef-259">PSTN Conference Sessions</span></span></p></li>
<li><p><span data-ttu-id="ea3ef-260">Звонки по ТСОП: обходной канал передачи медиаданных</span><span class="sxs-lookup"><span data-stu-id="ea3ef-260">PSTN Calls: Media Bypass</span></span></p></li>
<li><p><span data-ttu-id="ea3ef-261">Звонки по ТСОП (без обхода): ветвь объединенных коммуникаций</span><span class="sxs-lookup"><span data-stu-id="ea3ef-261">PSTN Calls (Non-Bypass): UC Leg</span></span></p></li>
<li><p><span data-ttu-id="ea3ef-262">Звонки по ТСОП (без обхода): ветвь шлюза</span><span class="sxs-lookup"><span data-stu-id="ea3ef-262">PSTN Calls (Non-Bypass): Gateway Leg</span></span></p></li>
<li><p><span data-ttu-id="ea3ef-263">Другие типы звонков</span><span class="sxs-lookup"><span data-stu-id="ea3ef-263">Other Call Types</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea3ef-264"><strong>Громкость вызова</strong></span><span class="sxs-lookup"><span data-stu-id="ea3ef-264"><strong>Call volume</strong></span></span></p></td>
<td><p><span data-ttu-id="ea3ef-265">Нет</span><span class="sxs-lookup"><span data-stu-id="ea3ef-265">No</span></span></p></td>
<td><p><span data-ttu-id="ea3ef-266">Общее количество звонков на тип звонка.</span><span class="sxs-lookup"><span data-stu-id="ea3ef-266">Total number of calls per call type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea3ef-267"><strong>Процент звонков низкого качества</strong></span><span class="sxs-lookup"><span data-stu-id="ea3ef-267"><strong>Poor call percentage</strong></span></span></p></td>
<td><p><span data-ttu-id="ea3ef-268">Нет</span><span class="sxs-lookup"><span data-stu-id="ea3ef-268">No</span></span></p></td>
<td><p><span data-ttu-id="ea3ef-p124">Общее количество звонков, классифицированных как звонки низкого качества. Звонок низкого качества – это любой звонок, хотя бы одна метрика которого превышает допустимое значение (например, звонок с чрезмерным дрожанием).</span><span class="sxs-lookup"><span data-stu-id="ea3ef-p124">Total number of calls classified as poor. A poor call is any call which at least one of the measured metrics exceeded the allowed value (for example, a call that experienced excessive jitter).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea3ef-271"><strong>Объем звонков (звонок по беспроводной сети)</strong></span><span class="sxs-lookup"><span data-stu-id="ea3ef-271"><strong>Call volume (wireless call)</strong></span></span></p></td>
<td><p><span data-ttu-id="ea3ef-272">Нет</span><span class="sxs-lookup"><span data-stu-id="ea3ef-272">No</span></span></p></td>
<td><p><span data-ttu-id="ea3ef-273">Общее количество звонков, при которых используется беспроводное подключение.</span><span class="sxs-lookup"><span data-stu-id="ea3ef-273">Total number of calls that used a wireless connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea3ef-274"><strong>Объем звонков (звонок по сети VPN)</strong></span><span class="sxs-lookup"><span data-stu-id="ea3ef-274"><strong>Call volume (VPN call)</strong></span></span></p></td>
<td><p><span data-ttu-id="ea3ef-275">Нет</span><span class="sxs-lookup"><span data-stu-id="ea3ef-275">No</span></span></p></td>
<td><p><span data-ttu-id="ea3ef-276">Общее количество звонков, при которых используется подключение по сети VPN.</span><span class="sxs-lookup"><span data-stu-id="ea3ef-276">Total number of calls that used a VPN connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea3ef-277"><strong>Объем звонков (внешний звонок)</strong></span><span class="sxs-lookup"><span data-stu-id="ea3ef-277"><strong>Call volume (external call)</strong></span></span></p></td>
<td><p><span data-ttu-id="ea3ef-278">Нет</span><span class="sxs-lookup"><span data-stu-id="ea3ef-278">No</span></span></p></td>
<td><p><span data-ttu-id="ea3ef-279">Количество звонков, при которых используется внешнее подключение (то есть подключение за пределами внутренней сети).</span><span class="sxs-lookup"><span data-stu-id="ea3ef-279">Number of calls that used an external connection (that is, a connection outside the internal network).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea3ef-280"><strong>Средняя скорость потока (кбит/с)</strong></span><span class="sxs-lookup"><span data-stu-id="ea3ef-280"><strong>Avg bit-rate (Kbits/s)</strong></span></span></p></td>
<td><p><span data-ttu-id="ea3ef-281">Нет</span><span class="sxs-lookup"><span data-stu-id="ea3ef-281">No</span></span></p></td>
<td><p><span data-ttu-id="ea3ef-282">Средняя скорость видеопотока (кбит/с).</span><span class="sxs-lookup"><span data-stu-id="ea3ef-282">Average video bit rate (in kilobits per second).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea3ef-283"><strong>Процент низкой скорости потока</strong></span><span class="sxs-lookup"><span data-stu-id="ea3ef-283"><strong>Low bit-rate %</strong></span></span></p></td>
<td><p><span data-ttu-id="ea3ef-284">Нет</span><span class="sxs-lookup"><span data-stu-id="ea3ef-284">No</span></span></p></td>
<td><p><span data-ttu-id="ea3ef-285">Процент звонков с низкой скоростью потока.</span><span class="sxs-lookup"><span data-stu-id="ea3ef-285">Percentage of the call where the bit rate was low.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea3ef-286"><strong>Потеря исходящих пакетов</strong></span><span class="sxs-lookup"><span data-stu-id="ea3ef-286"><strong>Outbound packet loss</strong></span></span></p></td>
<td><p><span data-ttu-id="ea3ef-287">Нет</span><span class="sxs-lookup"><span data-stu-id="ea3ef-287">No</span></span></p></td>
<td><p><span data-ttu-id="ea3ef-p125">Потеря исходящих пакетов транспортного протокола в режиме реального времени (пакетов протокола RTP). (Потеря пакетов происходит, когда пакеты протокола RTP, который используется для передачи звука и видео в Интернете, не достигают места своего назначения.) Высокие уровни потерь обычно бывают следствием перегруженности, нехватки пропускной способности, перегруженности или помех в беспроводной сети, а также перегруженности сервера мультимедиа. Потеря пакетов обычно приводит к искажению или потере звука.</span><span class="sxs-lookup"><span data-stu-id="ea3ef-p125">Real-Time Transport Protocol (RTP) packet loss for outbound packets. (Packet loss occurs when RTP packets, a protocol used for transmitting audio and video across the Internet, failed to reach their destination.) High loss rates are generally caused by congestion, lack of bandwidth, wireless congestion or interference, or an overloaded media server. Packet loss typically results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea3ef-291"><strong>Процент остановленных кадров</strong></span><span class="sxs-lookup"><span data-stu-id="ea3ef-291"><strong>Frozen frame %</strong></span></span></p></td>
<td><p><span data-ttu-id="ea3ef-292">Нет</span><span class="sxs-lookup"><span data-stu-id="ea3ef-292">No</span></span></p></td>
<td><p><span data-ttu-id="ea3ef-p126">Процент "остановленных" кадров. При остановке кадров видео не воспроизводится, а звук продолжает воспроизводиться.</span><span class="sxs-lookup"><span data-stu-id="ea3ef-p126">Percentage of “frozen” frames. In a frozen frame, the video stops advancing while the audio portion of the call continues.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea3ef-295"><strong>Средняя частота кадров исходящего сигнала</strong></span><span class="sxs-lookup"><span data-stu-id="ea3ef-295"><strong>Outbound avg frame rate</strong></span></span></p></td>
<td><p><span data-ttu-id="ea3ef-296">Нет</span><span class="sxs-lookup"><span data-stu-id="ea3ef-296">No</span></span></p></td>
<td><p><span data-ttu-id="ea3ef-297">Средняя частота кадров исходящей передачи во время вызова.</span><span class="sxs-lookup"><span data-stu-id="ea3ef-297">Average frame rate for outbound transmissions during the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea3ef-298"><strong>Средняя частота входящих кадров (%)</strong></span><span class="sxs-lookup"><span data-stu-id="ea3ef-298"><strong>Inbound avg frame rate</strong></span></span></p></td>
<td><p><span data-ttu-id="ea3ef-299">Нет</span><span class="sxs-lookup"><span data-stu-id="ea3ef-299">No</span></span></p></td>
<td><p><span data-ttu-id="ea3ef-300">Средняя частота кадров входящей передачи во время вызова.</span><span class="sxs-lookup"><span data-stu-id="ea3ef-300">Average frame rate for incoming transmissions during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea3ef-301"><strong>Низкая частота входящих кадров (%)</strong></span><span class="sxs-lookup"><span data-stu-id="ea3ef-301"><strong>Inbound low frame rate %</strong></span></span></p></td>
<td><p><span data-ttu-id="ea3ef-302">Нет</span><span class="sxs-lookup"><span data-stu-id="ea3ef-302">No</span></span></p></td>
<td><p><span data-ttu-id="ea3ef-303">Процент звонков с низкой скоростью входящего видеопотока.</span><span class="sxs-lookup"><span data-stu-id="ea3ef-303">Percentage of the call where the bit rate for incoming video was low.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea3ef-304"><strong>Работоспособность клиента (%)</strong></span><span class="sxs-lookup"><span data-stu-id="ea3ef-304"><strong>Client health %</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ea3ef-305">Показывает относительную работоспособность клиентского устройства во время вызова.</span><span class="sxs-lookup"><span data-stu-id="ea3ef-305">Indicates the relative health of the client device during the call.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="media-quality-summary-report-metrics-application-sharing-call-summary"></a><span data-ttu-id="ea3ef-306">Метрики сводного отчета по качеству мультимедиа: сводка по вызовам с общим доступом к приложениям</span><span class="sxs-lookup"><span data-stu-id="ea3ef-306">Media Quality Summary Report Metrics: Application Sharing Call Summary</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ea3ef-307">Имя</span><span class="sxs-lookup"><span data-stu-id="ea3ef-307">Name</span></span></th>
<th><span data-ttu-id="ea3ef-308">Поддержка сортировки</span><span class="sxs-lookup"><span data-stu-id="ea3ef-308">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="ea3ef-309">Описание</span><span class="sxs-lookup"><span data-stu-id="ea3ef-309">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ea3ef-310"><strong>Тип звонка и конечной точки</strong></span><span class="sxs-lookup"><span data-stu-id="ea3ef-310"><strong>Call type/Endpoint type</strong></span></span></p></td>
<td><p><span data-ttu-id="ea3ef-311">Нет</span><span class="sxs-lookup"><span data-stu-id="ea3ef-311">No</span></span></p></td>
<td><p><span data-ttu-id="ea3ef-p127">При щелчке этого элемента отчет предоставляет подробные сведения о звонках, основанных на этом типе. Типы звонков:</span><span class="sxs-lookup"><span data-stu-id="ea3ef-p127">When you click this item, the report shows detailed information about calls based on that type. Call types include:</span></span></p>
<ul>
<li><p><span data-ttu-id="ea3ef-314">Одноранговые звонки по объединенным коммуникациям</span><span class="sxs-lookup"><span data-stu-id="ea3ef-314">UC Peer-to-Peer Calls</span></span></p></li>
<li><p><span data-ttu-id="ea3ef-315">Сеансы конференц-связи по объединенным коммуникациям</span><span class="sxs-lookup"><span data-stu-id="ea3ef-315">UC Conference Sessions</span></span></p></li>
<li><p><span data-ttu-id="ea3ef-316">Сеансы конференц-связи по ТСОП</span><span class="sxs-lookup"><span data-stu-id="ea3ef-316">PSTN Conference Sessions</span></span></p></li>
<li><p><span data-ttu-id="ea3ef-317">Звонки по ТСОП: обходной канал передачи медиаданных</span><span class="sxs-lookup"><span data-stu-id="ea3ef-317">PSTN Calls: Media Bypass</span></span></p></li>
<li><p><span data-ttu-id="ea3ef-318">Звонки по ТСОП (без обхода): ветвь объединенных коммуникаций</span><span class="sxs-lookup"><span data-stu-id="ea3ef-318">PSTN Calls (Non-Bypass): UC Leg</span></span></p></li>
<li><p><span data-ttu-id="ea3ef-319">Звонки по ТСОП (без обхода): ветвь шлюза</span><span class="sxs-lookup"><span data-stu-id="ea3ef-319">PSTN Calls (Non-Bypass): Gateway Leg</span></span></p></li>
<li><p><span data-ttu-id="ea3ef-320">Другие типы звонков</span><span class="sxs-lookup"><span data-stu-id="ea3ef-320">Other Call Types</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea3ef-321"><strong>Громкость вызова</strong></span><span class="sxs-lookup"><span data-stu-id="ea3ef-321"><strong>Call volume</strong></span></span></p></td>
<td><p><span data-ttu-id="ea3ef-322">Нет</span><span class="sxs-lookup"><span data-stu-id="ea3ef-322">No</span></span></p></td>
<td><p><span data-ttu-id="ea3ef-323">Общее количество звонков на тип звонка.</span><span class="sxs-lookup"><span data-stu-id="ea3ef-323">Total number of calls per call type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea3ef-324"><strong>Процент звонков низкого качества</strong></span><span class="sxs-lookup"><span data-stu-id="ea3ef-324"><strong>Poor call percentage</strong></span></span></p></td>
<td><p><span data-ttu-id="ea3ef-325">Нет</span><span class="sxs-lookup"><span data-stu-id="ea3ef-325">No</span></span></p></td>
<td><p><span data-ttu-id="ea3ef-p128">Общее количество звонков, классифицированных как звонки низкого качества. Звонок низкого качества – это любой звонок, хотя бы одна метрика которого превышает допустимое значение (например, звонок с чрезмерным дрожанием).</span><span class="sxs-lookup"><span data-stu-id="ea3ef-p128">Total number of calls classified as poor. A poor call is any call which at least one of the measured metrics exceeded the allowed value (for example, a call that experienced excessive jitter).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea3ef-328"><strong>Объем звонков (звонок по беспроводной сети)</strong></span><span class="sxs-lookup"><span data-stu-id="ea3ef-328"><strong>Call volume (wireless call)</strong></span></span></p></td>
<td><p><span data-ttu-id="ea3ef-329">Нет</span><span class="sxs-lookup"><span data-stu-id="ea3ef-329">No</span></span></p></td>
<td><p><span data-ttu-id="ea3ef-330">Общее количество звонков, при которых используется беспроводное подключение.</span><span class="sxs-lookup"><span data-stu-id="ea3ef-330">Total number of calls that used a wireless connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea3ef-331"><strong>Объем звонков (звонок по сети VPN)</strong></span><span class="sxs-lookup"><span data-stu-id="ea3ef-331"><strong>Call volume (VPN call)</strong></span></span></p></td>
<td><p><span data-ttu-id="ea3ef-332">Нет</span><span class="sxs-lookup"><span data-stu-id="ea3ef-332">No</span></span></p></td>
<td><p><span data-ttu-id="ea3ef-333">Общее количество звонков, при которых используется подключение по сети VPN.</span><span class="sxs-lookup"><span data-stu-id="ea3ef-333">Total number of calls that used a VPN connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea3ef-334"><strong>Объем звонков (внешний звонок)</strong></span><span class="sxs-lookup"><span data-stu-id="ea3ef-334"><strong>Call volume (external call)</strong></span></span></p></td>
<td><p><span data-ttu-id="ea3ef-335">Нет</span><span class="sxs-lookup"><span data-stu-id="ea3ef-335">No</span></span></p></td>
<td><p><span data-ttu-id="ea3ef-336">Количество звонков, при которых используется внешнее подключение (то есть подключение за пределами внутренней сети).</span><span class="sxs-lookup"><span data-stu-id="ea3ef-336">Number of calls that used an external connection (that is, a connection outside the internal network).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea3ef-337"><strong>Дрожание (мс)</strong></span><span class="sxs-lookup"><span data-stu-id="ea3ef-337"><strong>Jitter (ms)</strong></span></span></p></td>
<td><p><span data-ttu-id="ea3ef-338">Нет</span><span class="sxs-lookup"><span data-stu-id="ea3ef-338">No</span></span></p></td>
<td><p><span data-ttu-id="ea3ef-339">Среднее значение колебаний, зарегистрированных между прибытиями пакетов RTP.</span><span class="sxs-lookup"><span data-stu-id="ea3ef-339">Average jitter detected between RTP packet arrivals.</span></span> <span data-ttu-id="ea3ef-340">(Колебание — это мера &quot; shakiness &quot; звонка). Обычно значения с высокой степенью колебаний заключаются в результате перегруженности или перегруженного сервера мультимедиа, что приводит к искажению или потере звука.</span><span class="sxs-lookup"><span data-stu-id="ea3ef-340">(Jitter is a measure of the &quot;shakiness&quot; of a call.) High jitter values are typically caused by congestion or an overloaded media server, and result in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea3ef-341"><strong>Средняя относительная задержка в одну сторону</strong></span><span class="sxs-lookup"><span data-stu-id="ea3ef-341"><strong>Avg. relative one way</strong></span></span></p></td>
<td><p><span data-ttu-id="ea3ef-342">Нет</span><span class="sxs-lookup"><span data-stu-id="ea3ef-342">No</span></span></p></td>
<td><p><span data-ttu-id="ea3ef-p130">Средняя относительная задержка в одну сторону между двумя конечными точками медиаданных. Это мера односкачковой задержки.</span><span class="sxs-lookup"><span data-stu-id="ea3ef-p130">Average relative one-way delay between two media endpoints. This is a single-hop latency measure.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea3ef-345"><strong>Средняя задержка обработки элемента RDP</strong></span><span class="sxs-lookup"><span data-stu-id="ea3ef-345"><strong>Avg. RDP tile processing latency</strong></span></span></p></td>
<td><p><span data-ttu-id="ea3ef-346">Нет</span><span class="sxs-lookup"><span data-stu-id="ea3ef-346">No</span></span></p></td>
<td><p><span data-ttu-id="ea3ef-p131">Среднее значение задержки обработки элементов RDP на сервере конференц-связи общего доступа к приложениям во время сеанса просмотра. Высокое среднее значение отражает более длительную задержку при просмотре и включает задержку сети. На перегруженном сервере конференц-связи могут происходить в среднем более длительные задержки.</span><span class="sxs-lookup"><span data-stu-id="ea3ef-p131">The average RDP tile processing latency in the AS Conferencing Server over the duration of the viewing session. A high average reflects a longer delay in the viewing experience, and includes network latency. An overloaded conferencing server may experience higher average delays.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea3ef-350"><strong>Процент испорченных элементов</strong></span><span class="sxs-lookup"><span data-stu-id="ea3ef-350"><strong>Total spoiled tile %</strong></span></span></p></td>
<td><p><span data-ttu-id="ea3ef-351">Нет</span><span class="sxs-lookup"><span data-stu-id="ea3ef-351">No</span></span></p></td>
<td><p><span data-ttu-id="ea3ef-352">Итоговый процент испорченных элементов RDP.</span><span class="sxs-lookup"><span data-stu-id="ea3ef-352">Total percentage of spoiled RDP tiles.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="ea3ef-353">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ea3ef-353">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

