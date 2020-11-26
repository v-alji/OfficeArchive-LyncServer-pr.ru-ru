---
title: 'Lync Server 2013: отчет о действиях пользователей'
description: 'Lync Server 2013: отчет о действиях пользователей.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: User Activity Report
ms:assetid: 3aa6fef2-ea02-4f0f-93e8-fa2e0a953d79
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558638(v=OCS.15)
ms:contentKeyID: 48183862
ms.date: 02/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0e959020e6ace6c72ecd570039d30a9ecc174c82
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440796"
---
# <a name="user-activity-report-in-lync-server-2013"></a><span data-ttu-id="e97f0-103">Отчет о действиях пользователей в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e97f0-103">User Activity Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e97f0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e97f0-104">

<span> </span></span></span>

<span data-ttu-id="e97f0-105">_**Тема последнего изменения:** 2015-02-27_</span><span class="sxs-lookup"><span data-stu-id="e97f0-105">_**Topic Last Modified:** 2015-02-27_</span></span>

<span data-ttu-id="e97f0-p101">Отчет об активности пользователей предоставляет подробный список одноранговых сеансов и сеансов конференц-связи, проведенных вашими пользователями за определенный период времени. В отличие от многих отчетов мониторинга отчет об активности пользователей связывает каждый звонок с отдельными пользователями. Например, одноранговые сеансы указывают универсальные коды ресурса (URI) SIP человека, который инициировал звонок (пользователь-отправитель), и человека, которому звонок был выполнен (пользователь-получатель). Если развернуть информацию по конференции вы увидите список всех участников конференции с указанием их роли.</span><span class="sxs-lookup"><span data-stu-id="e97f0-p101">The User Activity Report provides a detailed list of the peer-to-peer and conferencing sessions carried out by your users in a given time period. Unlike many of the Monitoring Reports, the User Activity Report ties each call to individual users. For example, peer-to-peer sessions specify the SIP URIs of the person who initiated the call (the From user) and the person who was being called (the To user). If you expand the information for a conference, you'll see a list of all the conference participants and the role they held for that conference.</span></span>

<span data-ttu-id="e97f0-p102">Отчет об активности пользователей иногда называют отчетом «службы технической поддержки». Это вызвано тем, что данный отчет часто используется сотрудниками службы технической поддержки для получения информации о сеансе для определенного пользователя. Вы можете отфильтровывать входящие и исходящие звонки для отдельного пользователя, просто введя URI SIP в поле «User URI prefix» (Префикс URI пользователя).</span><span class="sxs-lookup"><span data-stu-id="e97f0-p102">The User Activity Report is sometimes referred to as the "help desk" report. That's because the report is often used by help desk personnel to retrieve session information for a specific user. You can filter for calls made to or made by an individual user simply by typing the user's SIP URI in the User URI prefix box.</span></span>

<span data-ttu-id="e97f0-113">В этом случае в отчете об активности пользователей будут возвращаться сведения о пользователях, чей URI SIP начинается с указанной строки.</span><span class="sxs-lookup"><span data-stu-id="e97f0-113">If you do this, the User Activity Report will return information for any user whose SIP URI begins with the specified string.</span></span> <span data-ttu-id="e97f0-114">Например, если ввести в поле URI значение **ken**, отчет об активности пользователя найдет **Ken**.Myer@litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="e97f0-114">For example, if you type **ken** in the URI box, the User Activity Report will locate **Ken**.Myer@litwareinc.com.</span></span> <span data-ttu-id="e97f0-115">Однако при этом будут найдены и другие пользователи:</span><span class="sxs-lookup"><span data-stu-id="e97f0-115">However, it will also locate these users:</span></span>

  - <span data-ttu-id="e97f0-116">**ken** azi@litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="e97f0-116">**ken** azi@litwareinc.com</span></span>

  - <span data-ttu-id="e97f0-117">**ken** burg@litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="e97f0-117">**ken** burg@litwareinc.com</span></span>

  - <span data-ttu-id="e97f0-118">**Ken**.Sanchez@litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="e97f0-118">**Ken**.Sanchez@litwareinc.com</span></span>

  - <span data-ttu-id="e97f0-119">**Ken** nedy@litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="e97f0-119">**Ken** nedy@litwareinc.com</span></span>

<span data-ttu-id="e97f0-p104">Чтобы обеспечить возврат сведений только о пользователе Ken Myer, введите полный код URI (Ken.Myer@litwareinc.com) в поле поиска или несколько символов кода URI пользователя Ken, чтобы указать его уникальные отличия от других пользователей организации. Например:</span><span class="sxs-lookup"><span data-stu-id="e97f0-p104">To ensure that information only for Ken Myer is returned, either type his full URI (Ken.Myer@litwareinc.com) in the search box or at least enough type of Ken’s URI to uniquely distinguish him from other users in your organization. For example:</span></span>

<span data-ttu-id="e97f0-122">Ken.my</span><span class="sxs-lookup"><span data-stu-id="e97f0-122">Ken.my</span></span>

<div>

## <a name="to-access-the-user-activity-report"></a><span data-ttu-id="e97f0-123">Чтобы получить доступ к отчету о действиях пользователей, выполните следующие действия</span><span class="sxs-lookup"><span data-stu-id="e97f0-123">To access the user activity report</span></span>

<span data-ttu-id="e97f0-124">Доступ к отчету об активности пользователей осуществляется с домашней страницы отчетов мониторинга.</span><span class="sxs-lookup"><span data-stu-id="e97f0-124">The User Activity Report is accessed from the Monitoring Reports home page.</span></span> <span data-ttu-id="e97f0-125">Вы также можете связаться с отчетом об активности пользователей, щелкнув метрику URI пользователя в [отчете Инвентаризация IP-телефона в Lync Server 2013](lync-server-2013-ip-phone-inventory-report.md).</span><span class="sxs-lookup"><span data-stu-id="e97f0-125">You can also reach the User Activity Report by clicking the User URI metric on the [IP Phone Inventory Report in Lync Server 2013](lync-server-2013-ip-phone-inventory-report.md).</span></span> <span data-ttu-id="e97f0-126">Щелкнув элемент «Conference URI» (URI конференции) в отчете об активности пользователей вы откроете подробный отчет о конференции.</span><span class="sxs-lookup"><span data-stu-id="e97f0-126">From within the User Activity Report, clicking the Conference URI (for a conference) takes you to the Conference Detail Report.</span></span> <span data-ttu-id="e97f0-127">Аналогичным образом, если щелкнуть детальную метрику для однорангового звонка, вы можете перейти к [отчету сведения о одноранговых сеансах в Lync Server 2013](lync-server-2013-peer-to-peer-session-detail-report.md).</span><span class="sxs-lookup"><span data-stu-id="e97f0-127">Similarly, clicking the Detail metric for a peer-to-peer call takes you to the [Peer-to-Peer Session Detail Report in Lync Server 2013](lync-server-2013-peer-to-peer-session-detail-report.md).</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-user-activity-report"></a><span data-ttu-id="e97f0-128">Эффективное использование отчета об активности пользователей</span><span class="sxs-lookup"><span data-stu-id="e97f0-128">Making the best use of the user activity report</span></span>

<span data-ttu-id="e97f0-129">Хотя отчет об активности пользователей содержит много полезной информации, ее бывает сложно найти.</span><span class="sxs-lookup"><span data-stu-id="e97f0-129">Although there is a lot of good information in the User Activity Report, that information can sometimes be difficult to locate.</span></span> <span data-ttu-id="e97f0-130">Например, все действия пользователя, которые выполняются в вашей организации в течение определенного периода времени, включаются в отчет об активности пользователей; Это означает, что в составе отчета переводятся сведения о том, какие пользователи действительно использовали Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e97f0-130">For example, all the user activity that takes place in your organization during a specified period is included in the User Activity Report; that means that, buried, within the report is information about which users actually used Microsoft Lync Server 2013 in some way.</span></span>

<div>


> [!WARNING]  
> <span data-ttu-id="e97f0-131">Технически, возможно, некоторые действия пользователя могут быть незаписанными: в то время как Lync Server стремится хранить сведения обо всех телефонных звонках, что может привести к тому, что вызов не будет записан в базу данных.</span><span class="sxs-lookup"><span data-stu-id="e97f0-131">Technically, it’s possible that some user activity might go unrecorded: while Lync Server strives to keep information about all phone calls it's possible that a call could have been made without the information about that call being written to the database.</span></span> <span data-ttu-id="e97f0-132">Lync Server разработан таким образом, чтобы получить очень точную и необязательное представление о том, как используется Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e97f0-132">Lync Server is designed to give an extremely accurate but not necessarily perfect look at how Lync Server 2013 is being used.</span></span> <span data-ttu-id="e97f0-133">(Факт отсутствия гарантии, что 100% всех звонков будет записано объяснением того, почему в качестве системы выставления счетов не используется Мониторинг сервера Lync Server.)</span><span class="sxs-lookup"><span data-stu-id="e97f0-133">(The fact that there is no guarantee that 100% of all calls are recorded explains why Lync Server monitoring should not be used as a billing system.)</span></span><BR><span data-ttu-id="e97f0-134">Во-вторых, отчет в отчете мониторинга можно отобразить только в 1 000 записях.</span><span class="sxs-lookup"><span data-stu-id="e97f0-134">Second, a Monitoring Report report can only display, at most, 1,000 records.</span></span> <span data-ttu-id="e97f0-135">Таким образом, в зависимости от уровня активности пользователей и обрабатываемого периода запрос может возвращать не все данные, находящиеся в базе данных.</span><span class="sxs-lookup"><span data-stu-id="e97f0-135">Depending on the amount of user activity you have, and depending on the time period you are working with, that means your query might not return all the data actually stored in the database.</span></span>



</div>

  - <span data-ttu-id="e97f0-136">Какие именно пользователи использовали систему в определенный период?</span><span class="sxs-lookup"><span data-stu-id="e97f0-136">Which users actually used the system during this time period?</span></span>

  - <span data-ttu-id="e97f0-137">Какие именно пользователи были наиболее активными в определенный период?</span><span class="sxs-lookup"><span data-stu-id="e97f0-137">Which of my users were the most active during this time period?</span></span>

  - <span data-ttu-id="e97f0-138">Являются ли пользователи, выполнившие наиболее количество звонков, так же и пользователями, принявшими участие в большинстве сеансов обмена мгновенными сообщениями?</span><span class="sxs-lookup"><span data-stu-id="e97f0-138">Are the users who make the most phone calls also the users who participate in the most instant messaging sessions?</span></span>

<span data-ttu-id="e97f0-139">Если вам нужно ответить на подобные вопросы, вы можете экспортировать данные, полученные с помощью отчетов мониторинга, в электронную таблицу Excel.</span><span class="sxs-lookup"><span data-stu-id="e97f0-139">If you need to answer questions like this, you can export the data retrieved by the Monitoring Reports to an Excel spreadsheet.</span></span> <span data-ttu-id="e97f0-140">Затем вы можете использовать эту электронную таблицу и (или) файл значений, разделенных запятыми, чтобы проанализировать данные таким образом, как отчет об активности пользователей.</span><span class="sxs-lookup"><span data-stu-id="e97f0-140">You then use that spreadsheet and/or a comma-separated values file to analyze the data in ways that the User Activity Report.</span></span> <span data-ttu-id="e97f0-141">Например, предположим, что данные отчета экспортированы в Excel, а затем — в файл значений, разделенных запятыми.</span><span class="sxs-lookup"><span data-stu-id="e97f0-141">For example, suppose you have exported the report data to Excel and then to a comma-separated values file.</span></span> <span data-ttu-id="e97f0-142">На этом этапе вы можете импортировать данные из. CSV-файл в Windows PowerShell с помощью следующей команды:</span><span class="sxs-lookup"><span data-stu-id="e97f0-142">At that point, you can import the data from the .CSV file to Windows PowerShell by using a command similar to this:</span></span>

    $x = Import-Csv -Path "C:\Data\User_Activity_Report.csv"

<span data-ttu-id="e97f0-143">После импорта данных вы можете использовать простые команды Windows PowerShell, которые помогут вам получить ответы на свои вопросы.</span><span class="sxs-lookup"><span data-stu-id="e97f0-143">After the data has been imported you can then use simple Windows PowerShell commands to help answer your questions.</span></span> <span data-ttu-id="e97f0-144">Например, эта команда возвращает список уникальных пользователей, являвшихся пользователем-отправителем хотя бы в одном сеансе:</span><span class="sxs-lookup"><span data-stu-id="e97f0-144">For example, this command returns a list of unique users who served as the "From user" in at least one session:</span></span>

    $x | Group-Object "From user" | Select Name | Sort-Object Name

<span data-ttu-id="e97f0-145">Другими словами:</span><span class="sxs-lookup"><span data-stu-id="e97f0-145">In other words:</span></span>

    Name
    ----
    David.Ahs@litwareinc.com
    Gilead.Amosnino@litwareinc.com
    Henrik.Jensen@litwareinc.com
    Ken.Myer@litwareinc.com
    Pilar.Ackerman@litwareinc.com

<span data-ttu-id="e97f0-146">Эта команда выводит список уникальных пользователей (на основании общего числа сеансов, в которых они приняли участие:</span><span class="sxs-lookup"><span data-stu-id="e97f0-146">This command lists the unique users (based on the total number of sessions that they participated in:</span></span>

    $x | Group-Object "From user" | Select Count, Name | Sort-Object Count -Descending

<span data-ttu-id="e97f0-147">При этом возвращаются данные, аналогичные следующим:</span><span class="sxs-lookup"><span data-stu-id="e97f0-147">That returns data similar to this:</span></span>

    Count    Name
    -----    ----
      523    Ken.Myer@litwareinc.com
       63    David.Ahs@litwareinc.com
       29    Pilar.Ackerman@litwareinc.com
       17    Gilead.Amosnino@litwareinc.com
       10    Henrik.Jensen@litwareinc.com

<span data-ttu-id="e97f0-148">Эта команда ограничивает область поиска только сеансами, имевшими звуковую модальность:</span><span class="sxs-lookup"><span data-stu-id="e97f0-148">This command limits the reported sessions to those that included audio as a modality:</span></span>

    $x | Where-Object {$_.Modalities -match "audio"} | Group-Object "From user" | Select Count, Name | Sort-Object Count -Descending

<span data-ttu-id="e97f0-149">При наведении указателя на любой идентификатор диагностики в отчете отображается подсказка с описанием этого идентификатора.</span><span class="sxs-lookup"><span data-stu-id="e97f0-149">If you hold your mouse over any Diagnostic ID shown on the report, a tooltip will appear describing that ID.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="e97f0-150">Фильтры</span><span class="sxs-lookup"><span data-stu-id="e97f0-150">Filters</span></span>

<span data-ttu-id="e97f0-p111">Фильтры позволяют вам возвратить уточненный набор данных или просматривать возвращенные данные различными способами. Например, отчет об активности пользователей позволяет вам фильтровать возвращенные данные, например, по типу активности (одноранговые сеансы или сеансы конференц-связи) или по SIP-адресу пользователя (позволяя вам просматривать активность одного пользователя). Вы также можете определить группировку данных. В данном случае сведения об использовании группируются по часу, дню, неделе или месяцу.</span><span class="sxs-lookup"><span data-stu-id="e97f0-p111">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. For example, the User Activity Report enables you to filter the returned data based on such things as activity type (that is, peer-to-peer sessions or conferencing sessions) or by the user's SIP address (allowing you to view the activities for one user). You can also choose how data should be grouped. In this case, usages are grouped by hour, day, week, or month.</span></span>

<span data-ttu-id="e97f0-155">В следующей таблице перечислены фильтры, которые вы можете использовать в отчете об активности пользователей.</span><span class="sxs-lookup"><span data-stu-id="e97f0-155">The following table lists the filters that you can use with the User Activity Report.</span></span>

### <a name="user-activity-report-filters"></a><span data-ttu-id="e97f0-156">Фильтры отчета активности пользователя</span><span class="sxs-lookup"><span data-stu-id="e97f0-156">User activity report filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e97f0-157">Имя</span><span class="sxs-lookup"><span data-stu-id="e97f0-157">Name</span></span></th>
<th><span data-ttu-id="e97f0-158">Описание</span><span class="sxs-lookup"><span data-stu-id="e97f0-158">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e97f0-159"><strong>От</strong></span><span class="sxs-lookup"><span data-stu-id="e97f0-159"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="e97f0-p112">Начальные дата/время для временного диапазона. Чтобы просмотреть данные по часам, введите начальные дату и время следующим образом:</span><span class="sxs-lookup"><span data-stu-id="e97f0-p112">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="e97f0-162">7/17/12012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="e97f0-162">7/17/12012 1:00 PM</span></span></p>
<p><span data-ttu-id="e97f0-p113">Если вы не вводите начальное время, отчет автоматически начинается с 12:00 AM указанного дня. Чтобы просмотреть данные по дням, просто введите дату:</span><span class="sxs-lookup"><span data-stu-id="e97f0-p113">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="e97f0-165">7/17/12012</span><span class="sxs-lookup"><span data-stu-id="e97f0-165">7/17/12012</span></span></p>
<p><span data-ttu-id="e97f0-166">Чтобы просмотреть данные за неделю или месяц, введите дату, выпадающую на любое время в рамках недели или месяца, которые вы хотите просмотреть (вам не требуется вводить первый день недели или месяца):</span><span class="sxs-lookup"><span data-stu-id="e97f0-166">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="e97f0-167">7/13/2012</span><span class="sxs-lookup"><span data-stu-id="e97f0-167">7/13/2012</span></span></p>
<p><span data-ttu-id="e97f0-168">Недели всегда отсчитываются с воскресенья по субботу.</span><span class="sxs-lookup"><span data-stu-id="e97f0-168">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e97f0-169"><strong>До</strong></span><span class="sxs-lookup"><span data-stu-id="e97f0-169"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="e97f0-p114">Конечные дата/время для временного диапазона. Чтобы просмотреть данные по часам, введите конечные дату и время следующим образом:</span><span class="sxs-lookup"><span data-stu-id="e97f0-p114">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="e97f0-172">7/17/12012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="e97f0-172">7/17/12012 1:00 PM</span></span></p>
<p><span data-ttu-id="e97f0-p115">Если вы не вводите конечное время, отчет автоматически заканчивается в 12:00 AM указанного дня. Чтобы просмотреть данные по дням, просто введите дату:</span><span class="sxs-lookup"><span data-stu-id="e97f0-p115">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="e97f0-175">7/17/12012</span><span class="sxs-lookup"><span data-stu-id="e97f0-175">7/17/12012</span></span></p>
<p><span data-ttu-id="e97f0-176">Чтобы просмотреть данные за неделю или месяц, введите дату, выпадающую на любое время в рамках недели или месяца, которые вы хотите просмотреть (вам не требуется вводить первый день недели или месяца):</span><span class="sxs-lookup"><span data-stu-id="e97f0-176">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="e97f0-177">7/13/2012</span><span class="sxs-lookup"><span data-stu-id="e97f0-177">7/13/2012</span></span></p>
<p><span data-ttu-id="e97f0-178">Недели всегда отсчитываются с воскресенья по субботу.</span><span class="sxs-lookup"><span data-stu-id="e97f0-178">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e97f0-179"><strong>Activity type (Тип активности)</strong></span><span class="sxs-lookup"><span data-stu-id="e97f0-179"><strong>Activity type</strong></span></span></p></td>
<td><p><span data-ttu-id="e97f0-p116">Тип активности. Выберите одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="e97f0-p116">Type of activity. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="e97f0-182">[All] (Все)</span><span class="sxs-lookup"><span data-stu-id="e97f0-182">[All]</span></span></p></li>
<li><p><span data-ttu-id="e97f0-183">Одноранговая</span><span class="sxs-lookup"><span data-stu-id="e97f0-183">Peer-to-peer</span></span></p></li>
<li><p><span data-ttu-id="e97f0-184">Конференция</span><span class="sxs-lookup"><span data-stu-id="e97f0-184">Conference</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e97f0-185"><strong>Modality (Модальность)</strong></span><span class="sxs-lookup"><span data-stu-id="e97f0-185"><strong>Modality</strong></span></span></p></td>
<td><p><span data-ttu-id="e97f0-186">Доступный уровень модальности меняется в зависимости от выбранного типа действия.</span><span class="sxs-lookup"><span data-stu-id="e97f0-186">The Modality available to you varies depending on the select Activity Type.</span></span> <span data-ttu-id="e97f0-187">Если тип действия — одноранговый, вы можете выбрать сообщение. Передача файлов; Общий доступ к приложениям; Ставит или видео в качестве модальности.</span><span class="sxs-lookup"><span data-stu-id="e97f0-187">If the Activity Type is Peer-to-Peer, you can select IM; File Transfer; Application Sharing; Voice; or Video as the modality.</span></span></p>
<p><span data-ttu-id="e97f0-188">Если типом действия является конференция, можно выбрать телефонную конференцию с обменом мгновенными сообщениями; веб-конференцию; общий доступ к приложениям; голосовую/видеоконференцию или телефонную конференцию.</span><span class="sxs-lookup"><span data-stu-id="e97f0-188">If the Activity Type is Conference, you can select IM Phone conference; Web conference; Application Sharing; Voice/Video conference; or Telephony conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e97f0-189"><strong>Session category (Категория сеанса)</strong></span><span class="sxs-lookup"><span data-stu-id="e97f0-189"><strong>Session category</strong></span></span></p></td>
<td><p><span data-ttu-id="e97f0-p118">Указывает, была ли рассматриваемая активность успешна. Выберите одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="e97f0-p118">Indicates whether the activity in question succeeded or failed. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="e97f0-192">[All] (Все)</span><span class="sxs-lookup"><span data-stu-id="e97f0-192">[All]</span></span></p></li>
<li><p><span data-ttu-id="e97f0-193">Success (Успешно)</span><span class="sxs-lookup"><span data-stu-id="e97f0-193">Success</span></span></p></li>
<li><p><span data-ttu-id="e97f0-194">Expected failure (Ожидаемый сбой)</span><span class="sxs-lookup"><span data-stu-id="e97f0-194">Expected failure</span></span></p></li>
<li><p><span data-ttu-id="e97f0-195">Unexpected failure (Неожиданный сбой)</span><span class="sxs-lookup"><span data-stu-id="e97f0-195">Unexpected failure</span></span></p></li>
</ul>
<p><span data-ttu-id="e97f0-196">&quot;Ожидаемый сбой &quot; — это сбой, который может возникнуть, например, если пользователь установил состояние "не беспокоить", и вы не можете ожидать, что какой-либо вызов этого пользователя завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="e97f0-196">An &quot;expected failure&quot; is a failure that is expected to happen; for example, if a user has set his or her status to Do Not Disturb you would expect any call to that user to fail.</span></span> <span data-ttu-id="e97f0-197">Произошла &quot; непредвиденная ошибка &quot; , возникающая в том, что может выглядеть как подсистема, которая в противном случае является работоспособной.</span><span class="sxs-lookup"><span data-stu-id="e97f0-197">An &quot;unexpected failure&quot; is a failure that occurs in what would appear to be an otherwise healthy system.</span></span> <span data-ttu-id="e97f0-198">Например, вызов не должен прерываться, если вызывающий абонент помещается на удержание.</span><span class="sxs-lookup"><span data-stu-id="e97f0-198">For example, a call should not be terminated if the caller is placed on hold.</span></span> <span data-ttu-id="e97f0-199">В этом случае это считается непредвиденным сбоем.</span><span class="sxs-lookup"><span data-stu-id="e97f0-199">If that occurs, that would be flagged as an unexpected failure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e97f0-200"><strong>User URI prefix (Префикс URI пользователя)</strong></span><span class="sxs-lookup"><span data-stu-id="e97f0-200"><strong>User URI prefix</strong></span></span></p></td>
<td><p><span data-ttu-id="e97f0-p120">Адрес SIP пользователя. Чтобы просмотреть только записи для пользователя Ken Myer, вам необходимо ввести SIP-адрес этого пользователя. Например:</span><span class="sxs-lookup"><span data-stu-id="e97f0-p120">SIP address for the user. To view records only for the user Ken Myer you need to enter Ken Myer's SIP address. For example:</span></span></p>
<p><span data-ttu-id="e97f0-204">sip:kenmyer@litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="e97f0-204">sip:kenmyer@litwareinc.com</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-peer-to-peer-sessions"></a><span data-ttu-id="e97f0-205">Метрики для одноранговых сеансов</span><span class="sxs-lookup"><span data-stu-id="e97f0-205">Metrics for peer-to-peer sessions</span></span>

<span data-ttu-id="e97f0-206">В следующей таблице приведены сведения из отчета об активности пользователей для одноранговых сеансов (то есть сеансов, включающих всего двух участников).</span><span class="sxs-lookup"><span data-stu-id="e97f0-206">The following table lists the information provided in the User Activity Report for peer-to-peer sessions (that is, sessions involving just two participants).</span></span>

### <a name="metrics-for-peer-to-peer-sessions"></a><span data-ttu-id="e97f0-207">Метрики для одноранговых сеансов</span><span class="sxs-lookup"><span data-stu-id="e97f0-207">Metrics for peer-to-peer sessions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e97f0-208">Имя</span><span class="sxs-lookup"><span data-stu-id="e97f0-208">Name</span></span></th>
<th><span data-ttu-id="e97f0-209">Поддержка сортировки</span><span class="sxs-lookup"><span data-stu-id="e97f0-209">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="e97f0-210">Описание</span><span class="sxs-lookup"><span data-stu-id="e97f0-210">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e97f0-211"><strong>Подробности</strong></span><span class="sxs-lookup"><span data-stu-id="e97f0-211"><strong>Detail</strong></span></span></p></td>
<td><p><span data-ttu-id="e97f0-212">Нет</span><span class="sxs-lookup"><span data-stu-id="e97f0-212">No</span></span></p></td>
<td><p><span data-ttu-id="e97f0-213">При щелчке данного элемента отчет отображает для выбранного сеанса подробный отчет об одноранговом сеансе.</span><span class="sxs-lookup"><span data-stu-id="e97f0-213">When you click this item, the report shows you the Peer-to-Peer Session Detail Report for the selected session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e97f0-214"><strong>From user (Пользователь-отправитель)</strong></span><span class="sxs-lookup"><span data-stu-id="e97f0-214"><strong>From user</strong></span></span></p></td>
<td><p><span data-ttu-id="e97f0-215">Да</span><span class="sxs-lookup"><span data-stu-id="e97f0-215">Yes</span></span></p></td>
<td><p><span data-ttu-id="e97f0-216">SIP-адрес пользователя, который инициировал данный одноранговый сеанс.</span><span class="sxs-lookup"><span data-stu-id="e97f0-216">SIP address of the user who initiated the peer-to-peer session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e97f0-217"><strong>To user (Пользователь-получатель)</strong></span><span class="sxs-lookup"><span data-stu-id="e97f0-217"><strong>To user</strong></span></span></p></td>
<td><p><span data-ttu-id="e97f0-218">Да</span><span class="sxs-lookup"><span data-stu-id="e97f0-218">Yes</span></span></p></td>
<td><p><span data-ttu-id="e97f0-219">SIP-адрес пользователя, который присоединился к данному одноранговому сеансу.</span><span class="sxs-lookup"><span data-stu-id="e97f0-219">SIP address of the user who joined the peer-to-peer session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e97f0-220"><strong>Modalities (Модальности)</strong></span><span class="sxs-lookup"><span data-stu-id="e97f0-220"><strong>Modalities</strong></span></span></p></td>
<td><p><span data-ttu-id="e97f0-221">Да</span><span class="sxs-lookup"><span data-stu-id="e97f0-221">Yes</span></span></p></td>
<td><p><span data-ttu-id="e97f0-p121">Тип коммуникации, использованный в сеансе. Например, мгновенные сообщения, звук или передача файлов.</span><span class="sxs-lookup"><span data-stu-id="e97f0-p121">Type of communication used in the session. For example, IM, audio, or file transfer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e97f0-224"><strong>Invite time (Время приглашения)</strong></span><span class="sxs-lookup"><span data-stu-id="e97f0-224"><strong>Invite time</strong></span></span></p></td>
<td><p><span data-ttu-id="e97f0-225">Да</span><span class="sxs-lookup"><span data-stu-id="e97f0-225">Yes</span></span></p></td>
<td><p><span data-ttu-id="e97f0-226">Дата и время отправки начального приглашения присоединиться к одноранговому сеансу.</span><span class="sxs-lookup"><span data-stu-id="e97f0-226">Date and time the initial invitation to join the peer-to-peer session was sent.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e97f0-227"><strong>Response time (Время ответа)</strong></span><span class="sxs-lookup"><span data-stu-id="e97f0-227"><strong>Response time</strong></span></span></p></td>
<td><p><span data-ttu-id="e97f0-228">Да</span><span class="sxs-lookup"><span data-stu-id="e97f0-228">Yes</span></span></p></td>
<td><p><span data-ttu-id="e97f0-229">Дата и время, когда &quot; &quot; пользователь отпринял приглашение на сеанс.</span><span class="sxs-lookup"><span data-stu-id="e97f0-229">Date and time that the &quot;To&quot; user accepted the session invitation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e97f0-230"><strong>Время окончания</strong></span><span class="sxs-lookup"><span data-stu-id="e97f0-230"><strong>End time</strong></span></span></p></td>
<td><p><span data-ttu-id="e97f0-231">Да</span><span class="sxs-lookup"><span data-stu-id="e97f0-231">Yes</span></span></p></td>
<td><p><span data-ttu-id="e97f0-232">Дата и время окончания однорангового сеанса.</span><span class="sxs-lookup"><span data-stu-id="e97f0-232">Date and time the peer-to-peer session ended.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e97f0-233"><strong>Diagnostic ID (ИД диагностики)</strong></span><span class="sxs-lookup"><span data-stu-id="e97f0-233"><strong>Diagnostic ID</strong></span></span></p></td>
<td><p><span data-ttu-id="e97f0-234">Да</span><span class="sxs-lookup"><span data-stu-id="e97f0-234">Yes</span></span></p></td>
<td><p><span data-ttu-id="e97f0-p122">Прикрепленный к SIP-сообщению уникальный идентификатор (в форме заголовка ms-diagnostics), который часто содержит информацию, полезную при поиске и устранении ошибок. Заголовки диагностики не являются обязательными (можно иметь сеансы SIP без таких заголовков), а идентификаторы диагностики указываются только для сеансов, в которых возникли какие-либо проблемы.</span><span class="sxs-lookup"><span data-stu-id="e97f0-p122">Unique identifier (in the form of an ms-diagnostics header) attached to a SIP message that often provides information useful in troubleshooting errors. Diagnostics headers are optional (it is possible to have SIP sessions that do not include these headers), and diagnostic IDs are reported only for sessions that experienced problems of some kind.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-conferencing-sessions"></a><span data-ttu-id="e97f0-237">Метрики для сеансов конференц-связи</span><span class="sxs-lookup"><span data-stu-id="e97f0-237">Metrics for conferencing sessions</span></span>

<span data-ttu-id="e97f0-238">В следующей таблице приведены сведения из отчета об активности пользователей для сеансов конференц-связи (то есть сеансов, включающих трех и более участников).</span><span class="sxs-lookup"><span data-stu-id="e97f0-238">The following table lists the information provided in the User Activity Report for conferencing sessions (that is, sessions involving three or more participants).</span></span>

### <a name="metrics-for-conferencing-sessions"></a><span data-ttu-id="e97f0-239">Метрики для сеансов конференц-связи</span><span class="sxs-lookup"><span data-stu-id="e97f0-239">Metrics for conferencing sessions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e97f0-240">Имя</span><span class="sxs-lookup"><span data-stu-id="e97f0-240">Name</span></span></th>
<th><span data-ttu-id="e97f0-241">Поддержка сортировки</span><span class="sxs-lookup"><span data-stu-id="e97f0-241">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="e97f0-242">Описание</span><span class="sxs-lookup"><span data-stu-id="e97f0-242">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e97f0-243"><strong>Идентификатор URI конференции</strong></span><span class="sxs-lookup"><span data-stu-id="e97f0-243"><strong>Conference URI</strong></span></span></p></td>
<td><p><span data-ttu-id="e97f0-244">Да</span><span class="sxs-lookup"><span data-stu-id="e97f0-244">Yes</span></span></p></td>
<td><p><span data-ttu-id="e97f0-245">Уникальный идентификатор конференции.</span><span class="sxs-lookup"><span data-stu-id="e97f0-245">Unique conference identifier.</span></span> <span data-ttu-id="e97f0-246">При щелчке данного элемента отчет отображает для выбранного сеанса подробный отчет о конференции.</span><span class="sxs-lookup"><span data-stu-id="e97f0-246">When you click this item, the report shows you the Conference Detail Report for the selected session.</span></span> <span data-ttu-id="e97f0-247">При развертывании этого элемента отчет отображает информацию об участниках конференции.</span><span class="sxs-lookup"><span data-stu-id="e97f0-247">When you expand this item, the report shows you information about the conference participants.</span></span> <span data-ttu-id="e97f0-248">Дополнительные сведения можно найти &quot; в разделе метрики участников конференции &quot; ниже в этой статье.</span><span class="sxs-lookup"><span data-stu-id="e97f0-248">For details, see the &quot;Metrics for Conference Participants&quot; section later in this topic.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e97f0-249"><strong>Инициатор</strong></span><span class="sxs-lookup"><span data-stu-id="e97f0-249"><strong>Organizer</strong></span></span></p></td>
<td><p><span data-ttu-id="e97f0-250">Да</span><span class="sxs-lookup"><span data-stu-id="e97f0-250">Yes</span></span></p></td>
<td><p><span data-ttu-id="e97f0-251">SIP-адрес пользователя, организовавшего конференцию.</span><span class="sxs-lookup"><span data-stu-id="e97f0-251">SIP address of the user who organized the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e97f0-252"><strong>Пул</strong></span><span class="sxs-lookup"><span data-stu-id="e97f0-252"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="e97f0-253">Да</span><span class="sxs-lookup"><span data-stu-id="e97f0-253">Yes</span></span></p></td>
<td><p><span data-ttu-id="e97f0-254">Имя используемого в конференции пограничного сервера (при его наличии).</span><span class="sxs-lookup"><span data-stu-id="e97f0-254">Name of the Edge Server (if any) used in the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e97f0-255"><strong>Start time (Время начала)</strong></span><span class="sxs-lookup"><span data-stu-id="e97f0-255"><strong>Start time</strong></span></span></p></td>
<td><p><span data-ttu-id="e97f0-256">Да</span><span class="sxs-lookup"><span data-stu-id="e97f0-256">Yes</span></span></p></td>
<td><p><span data-ttu-id="e97f0-257">Дата и время начала конференции.</span><span class="sxs-lookup"><span data-stu-id="e97f0-257">Date and time that the conference began.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e97f0-258"><strong>End time (Время окончания)</strong></span><span class="sxs-lookup"><span data-stu-id="e97f0-258"><strong>End time</strong></span></span></p></td>
<td><p><span data-ttu-id="e97f0-259">Да</span><span class="sxs-lookup"><span data-stu-id="e97f0-259">Yes</span></span></p></td>
<td><p><span data-ttu-id="e97f0-260">Дата и время завершения конференции.</span><span class="sxs-lookup"><span data-stu-id="e97f0-260">Date and time that the conference ended.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-conference-participants"></a><span data-ttu-id="e97f0-261">Метрики для участников конференции</span><span class="sxs-lookup"><span data-stu-id="e97f0-261">Metrics for conference participants</span></span>

<span data-ttu-id="e97f0-262">В следующей таблице приведены сведения из отчета об активности пользователей для каждого из участников конференции.</span><span class="sxs-lookup"><span data-stu-id="e97f0-262">The following table lists the information provided in the User Activity Report provides for each participant in a conference.</span></span>

### <a name="metrics-for-conference-participants"></a><span data-ttu-id="e97f0-263">Метрики для участников конференции</span><span class="sxs-lookup"><span data-stu-id="e97f0-263">Metrics for conference participants</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e97f0-264">Имя</span><span class="sxs-lookup"><span data-stu-id="e97f0-264">Name</span></span></th>
<th><span data-ttu-id="e97f0-265">Поддержка сортировки</span><span class="sxs-lookup"><span data-stu-id="e97f0-265">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="e97f0-266">Описание</span><span class="sxs-lookup"><span data-stu-id="e97f0-266">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e97f0-267"><strong>Роль</strong></span><span class="sxs-lookup"><span data-stu-id="e97f0-267"><strong>Role</strong></span></span></p></td>
<td><p><span data-ttu-id="e97f0-268">Нет</span><span class="sxs-lookup"><span data-stu-id="e97f0-268">No</span></span></p></td>
<td><p><span data-ttu-id="e97f0-269">Роль (например, выступающий) пользователя на конференции.</span><span class="sxs-lookup"><span data-stu-id="e97f0-269">Conference role (for example, Presenter) for the user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e97f0-270"><strong>Participant (Участник)</strong></span><span class="sxs-lookup"><span data-stu-id="e97f0-270"><strong>Participant</strong></span></span></p></td>
<td><p><span data-ttu-id="e97f0-271">Нет</span><span class="sxs-lookup"><span data-stu-id="e97f0-271">No</span></span></p></td>
<td><p><span data-ttu-id="e97f0-272">Адрес SIP пользователя.</span><span class="sxs-lookup"><span data-stu-id="e97f0-272">SIP address of the user.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e97f0-273"><strong>Connectivity (Подключение)</strong></span><span class="sxs-lookup"><span data-stu-id="e97f0-273"><strong>Connectivity</strong></span></span></p></td>
<td><p><span data-ttu-id="e97f0-274">Нет</span><span class="sxs-lookup"><span data-stu-id="e97f0-274">No</span></span></p></td>
<td><p><span data-ttu-id="e97f0-275">Тип подключения к сети.</span><span class="sxs-lookup"><span data-stu-id="e97f0-275">Network connection type.</span></span> <span data-ttu-id="e97f0-276">Например &quot; , от внутренних &quot; для внутреннего или &quot; от КТСОП &quot; для пользователей с телефонным подключением.</span><span class="sxs-lookup"><span data-stu-id="e97f0-276">For example &quot;From Internal&quot; for internal connection or &quot;From PSTN&quot; for dial-in users.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e97f0-277"><strong>Время присоединения к конференциям</strong></span><span class="sxs-lookup"><span data-stu-id="e97f0-277"><strong>Join time</strong></span></span></p></td>
<td><p><span data-ttu-id="e97f0-278">Нет</span><span class="sxs-lookup"><span data-stu-id="e97f0-278">No</span></span></p></td>
<td><p><span data-ttu-id="e97f0-279">Дата и время присоединения пользователя к конференции.</span><span class="sxs-lookup"><span data-stu-id="e97f0-279">Date and time that the user joined the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e97f0-280"><strong>Leave time (Время ухода)</strong></span><span class="sxs-lookup"><span data-stu-id="e97f0-280"><strong>Leave time</strong></span></span></p></td>
<td><p><span data-ttu-id="e97f0-281">Нет</span><span class="sxs-lookup"><span data-stu-id="e97f0-281">No</span></span></p></td>
<td><p><span data-ttu-id="e97f0-282">Дата и время покидания пользователем конференции.</span><span class="sxs-lookup"><span data-stu-id="e97f0-282">Date and time that the user left the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e97f0-283"><strong>Diagnostic ID (ИД диагностики)</strong></span><span class="sxs-lookup"><span data-stu-id="e97f0-283"><strong>Diagnostic ID</strong></span></span></p></td>
<td><p><span data-ttu-id="e97f0-284">Нет</span><span class="sxs-lookup"><span data-stu-id="e97f0-284">No</span></span></p></td>
<td><p><span data-ttu-id="e97f0-p125">Прикрепленный к SIP-сообщению уникальный идентификатор (в форме заголовка ms-diagnostics), который часто содержит информацию, полезную при поиске и устранении ошибок. Заголовки диагностики не являются обязательными (можно иметь сеансы SIP без таких заголовков), а идентификаторы диагностики указываются только для сеансов, в которых возникли какие-либо проблемы.</span><span class="sxs-lookup"><span data-stu-id="e97f0-p125">Unique identifier (in the form of an ms-diagnostics header) attached to a SIP message that often provides information useful in troubleshooting errors. Diagnostics headers are optional (it is possible to have SIP sessions that do not include these headers), and diagnostic IDs are reported only for sessions that experienced problems of some kind.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="e97f0-287">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e97f0-287">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

