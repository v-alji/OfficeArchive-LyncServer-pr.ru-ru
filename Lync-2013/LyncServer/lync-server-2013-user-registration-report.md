---
title: 'Lync Server 2013: отчет о регистрации пользователей'
description: 'Lync Server 2013: отчет о регистрации пользователя.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: User Registration Report
ms:assetid: 151d5cc9-cc1b-4cfa-be9c-55ebe321f7a4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558614(v=OCS.15)
ms:contentKeyID: 48183486
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7adb8ef7e94a24f0fd088f12e009fc9d63f3be9d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398665"
---
# <a name="user-registration-report-in-lync-server-2013"></a><span data-ttu-id="62809-103">Отчет о регистрации пользователей в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="62809-103">User Registration Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="62809-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="62809-104">

<span> </span></span></span>

<span data-ttu-id="62809-105">_**Тема последнего изменения:** 2012-10-21_</span><span class="sxs-lookup"><span data-stu-id="62809-105">_**Topic Last Modified:** 2012-10-21_</span></span>

<span data-ttu-id="62809-106">Отчет о регистрации пользователей содержит общие сведения о действиях входа в систему, наиболее часто заданных о количестве пользователей, которые вошли в Microsoft Lync Server 2013 в течение определенного периода времени (ежечасно, ежедневно, еженедельно, ежемесячно).</span><span class="sxs-lookup"><span data-stu-id="62809-106">The User Registration Report provides an overview of user logon activity, most notably information about the number of users who logged on to Microsoft Lync Server 2013 during a specified time period (hourly, daily, weekly, monthly).</span></span> <span data-ttu-id="62809-107">Следует иметь в виду, что в отчете лишь сообщается, сколько людей входило в систему.</span><span class="sxs-lookup"><span data-stu-id="62809-107">Keep in mind that the report only tells you how many people logged on.</span></span> <span data-ttu-id="62809-108">В нем не указывается, *какие* люди входили в систему.</span><span class="sxs-lookup"><span data-stu-id="62809-108">It does not tell you *which* people logged on.</span></span> <span data-ttu-id="62809-109">Отчеты мониторинга не предоставляют сведения о том, какие пользователи используют Lync Server 2013 (и какие из них не являются).</span><span class="sxs-lookup"><span data-stu-id="62809-109">Monitoring Reports do not provide information about which specific users are using Lync Server 2013 (and which ones are not).</span></span> <span data-ttu-id="62809-110">Тем не менее с помощью отчета об активности пользователей можно получить грубую оценку пользовательской информации.</span><span class="sxs-lookup"><span data-stu-id="62809-110">However, you can get a rough estimate of user information by using the User Activity Report.</span></span>

<span data-ttu-id="62809-111">При предоставлении сведений о входах пользователей в систему в отчете о регистрации пользователей делается два важных разграничения.</span><span class="sxs-lookup"><span data-stu-id="62809-111">When providing information about user logons, the User Registration Report draws two important distinctions.</span></span> <span data-ttu-id="62809-112">Во-первых, в отчете входы в систему разбиваются на две основные категории: внутренние и внешние входы в систему.</span><span class="sxs-lookup"><span data-stu-id="62809-112">First, it breaks logons down into two primary categories: internal logons and external logons.</span></span> <span data-ttu-id="62809-113">Внутренние входы представляют пользователей, вошедших в систему с внутренней стороны брандмауэра организации (то есть, с компьютера, подключенного к корпоративной сети).</span><span class="sxs-lookup"><span data-stu-id="62809-113">Internal logons represent users who logged on from inside your organization's firewall (that is, while connected to the corporate network).</span></span> <span data-ttu-id="62809-114">Внешние входы — это пользователи, которые вошли в систему за пределами брандмауэра через пограничный сервер (например, пользователь, выполнивший вход из Интернет-кафе, считает внешним входом).</span><span class="sxs-lookup"><span data-stu-id="62809-114">External logons represent users who logged on from outside the firewall through an Edge Server (for example, a user who logged on from an Internet café counts as an external logon).</span></span> <span data-ttu-id="62809-115">Если необходимо узнать, сколько пользователей входит в систему с внешней стороны брандмауэра, эти сведения можно найти в отчете о регистрации пользователей.</span><span class="sxs-lookup"><span data-stu-id="62809-115">If you need to know how many of your users are logging on from outside the firewall, the User Registration Report can provide you with this information.</span></span>

<span data-ttu-id="62809-116">Кроме того, в отчете о регистрации пользователей отмечается, сколько *активных* пользователей присутствовало в течение заданного периода времени.</span><span class="sxs-lookup"><span data-stu-id="62809-116">In addition, the User Registration Report notes how many *active* users were present during a given time period.</span></span> <span data-ttu-id="62809-117">Активный пользователь — это пользователь, который потратил участие в сеансе обмена мгновенными сообщениями, принял участие в собрании Lync, сделал или получил телефонный звонок, или иным образом использовал Lync Server в течение этого периода времени.</span><span class="sxs-lookup"><span data-stu-id="62809-117">An active user is a user who took part in an instant messaging (IM) session, participated in a Lync Meeting, made or received a phone call, or otherwise used Lync Server during that period of time.</span></span> <span data-ttu-id="62809-118">Такой пользователь отличается от пользователя, вошедшего в систему, но не проявлявшего никакой активности в системе.</span><span class="sxs-lookup"><span data-stu-id="62809-118">This is different from a user who logged on, but never actually used the system.</span></span>

<div>

## <a name="accessing-the-user-registration-report"></a><span data-ttu-id="62809-119">Доступ к отчету о регистрации пользователей</span><span class="sxs-lookup"><span data-stu-id="62809-119">Accessing the User Registration Report</span></span>

<span data-ttu-id="62809-p104">Доступ к отчету о регистрации пользователей предоставляется только на домашней странице отчетов мониторинга. Отчет о регистрации пользователей не связан с какими-либо другими отчетами.</span><span class="sxs-lookup"><span data-stu-id="62809-p104">You access the User Registration Report only from the Monitoring Reports home page. The User Registration Report does not link to any other reports.</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-user-registration-report"></a><span data-ttu-id="62809-122">Оптимальное использование отчета о регистрации пользователей</span><span class="sxs-lookup"><span data-stu-id="62809-122">Making the Best Use of the User Registration Report</span></span>

<span data-ttu-id="62809-123">После развертывания сервера Lync Server вы можете сделать следующее: как узнать, действительно ли мои пользователи используют эту новую технологию?</span><span class="sxs-lookup"><span data-stu-id="62809-123">After you've deployed Lync Server one commonly-asked question is this: How do I know if my users are actually using this new technology?</span></span> <span data-ttu-id="62809-124">Хотя в этом отношении есть определенные ограничения, отчет о регистрации пользователей позволяет ответить на этот вопрос.</span><span class="sxs-lookup"><span data-stu-id="62809-124">Although it has a few limitations in this regard, the User Registration Report can help you answer this question.</span></span> <span data-ttu-id="62809-125">Чтобы определить, используете ли пользователи Lync Server, необходимо выполнить два действия.</span><span class="sxs-lookup"><span data-stu-id="62809-125">To determine whether or not users are using Lync Server, you need to do two things.</span></span> <span data-ttu-id="62809-126">Во-первых, нужно получить значение показателя уникальных входов пользователей из отчета о регистрации пользователей.</span><span class="sxs-lookup"><span data-stu-id="62809-126">First, get the value of the Unique logon users metric from the User Registration Report.</span></span> <span data-ttu-id="62809-127">В этом параметре указывается количество отдельных пользователей, выполнивших вход на сервер Lync Server.</span><span class="sxs-lookup"><span data-stu-id="62809-127">This value tells you how many distinct individuals logged on to Lync Server.</span></span>

<span data-ttu-id="62809-128">По сравнению с общим показателем количества входов в систему показано общее количество пользователей, которые вошли в Lync Server.</span><span class="sxs-lookup"><span data-stu-id="62809-128">By comparison, the Total logons metric shows how many total times anyone logged on to Lync Server.</span></span> <span data-ttu-id="62809-129">Например, предположим, что Кен Myer вошел на сервер Lync Server пять разных случаев за один день.</span><span class="sxs-lookup"><span data-stu-id="62809-129">For example, suppose Ken Myer logged on to Lync Server five different times in a single day.</span></span> <span data-ttu-id="62809-130">В этом случае для Кен Майера было бы подсчитано пять отдельных сеансов входа в показателе общего числа входов, но лишь один зарегистрированный пользователь в показателе уникальных зарегистрированных пользователей.</span><span class="sxs-lookup"><span data-stu-id="62809-130">In that case, Ken Myer would count as five separate logon sessions for the Total logons metric, but just one logon user for the Unique logon users metric.</span></span> <span data-ttu-id="62809-131">Аналогично, пользователи нередко входят в систему с нескольких устройств или из нескольких мест.</span><span class="sxs-lookup"><span data-stu-id="62809-131">Likewise, it's not uncommon for a user to log on from multiple devices or multiple locations.</span></span> <span data-ttu-id="62809-132">Например, пользователь может войти в систему с помощью настольного компьютера, ноутбука и компьютера, на котором есть IP-телефон, который автоматически входит на Lync Server.</span><span class="sxs-lookup"><span data-stu-id="62809-132">For example, a user can log on using her desktop computer, her laptop computer, and she can have an IP phone that automatically logs on to Lync Server.</span></span> <span data-ttu-id="62809-133">В этом примере имеется один уникальный пользователь с тремя входами в систему.</span><span class="sxs-lookup"><span data-stu-id="62809-133">In this example, there is one unique user with three logons.</span></span>

<span data-ttu-id="62809-134">Для дальнейшего пояснения разницы между общим количеством входов и уникальными входами рассмотрим входы в систему для заданного периода времени, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="62809-134">To further explain the difference between total logons and unique logons, consider the logons for a given time period in the following table.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="62809-135">Пользователь</span><span class="sxs-lookup"><span data-stu-id="62809-135">User</span></span></th>
<th><span data-ttu-id="62809-136">Время входа</span><span class="sxs-lookup"><span data-stu-id="62809-136">Logon time</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="62809-137">Кен Майер</span><span class="sxs-lookup"><span data-stu-id="62809-137">Ken Myer</span></span></p></td>
<td><p><span data-ttu-id="62809-138">7/7/2012 8:45 AM</span><span class="sxs-lookup"><span data-stu-id="62809-138">7/7/2012 8:45 AM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62809-139">Ken Myer</span><span class="sxs-lookup"><span data-stu-id="62809-139">Ken Myer</span></span></p></td>
<td><p><span data-ttu-id="62809-140">7/7/2012 8:46 AM</span><span class="sxs-lookup"><span data-stu-id="62809-140">7/7/2012 8:46 AM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62809-141">Pilar Ackerman</span><span class="sxs-lookup"><span data-stu-id="62809-141">Pilar Ackerman</span></span></p></td>
<td><p><span data-ttu-id="62809-142">7/7/2012 9:17 AM</span><span class="sxs-lookup"><span data-stu-id="62809-142">7/7/2012 9:17 AM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62809-143">Ken Myer</span><span class="sxs-lookup"><span data-stu-id="62809-143">Ken Myer</span></span></p></td>
<td><p><span data-ttu-id="62809-144">7/7/2012 9:22 AM</span><span class="sxs-lookup"><span data-stu-id="62809-144">7/7/2012 9:22 AM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62809-145">Pilar Ackerman</span><span class="sxs-lookup"><span data-stu-id="62809-145">Pilar Ackerman</span></span></p></td>
<td><p><span data-ttu-id="62809-146">7/7/2012 9:31 AM</span><span class="sxs-lookup"><span data-stu-id="62809-146">7/7/2012 9:31 AM</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="62809-p107">Обратите внимание, что общее количество входов в систему равно пяти; однако существует только два уникальных регистрировавшихся пользователя: Кен Майер (входивший в систему три раза) и Пилар Аккерман (заходивший в систему дважды). В этом разница между входами в систему и уникальными регистрировавшимися пользователями.</span><span class="sxs-lookup"><span data-stu-id="62809-p107">Notice that there is a total of five logons; however, there are only two unique logon users: Ken Myer (who logged on three times) and Pilar Ackerman (who logged on twice). That's the difference between logons and unique logon users.</span></span>

<span data-ttu-id="62809-149">Помимо количества уникальных входов в систему, необходимо знать общее количество пользователей, которые были включены в Lync Server.</span><span class="sxs-lookup"><span data-stu-id="62809-149">In addition to knowing the number of unique logons, you need to know the total number of users who have been enabled for Lync Server.</span></span> <span data-ttu-id="62809-150">Это значение можно получить, открыв командную консоль Lync Server 2013 и выполнив следующую команду Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="62809-150">That value can be retrieved by opening the Lync Server 2013 Management Shell and running the following Windows PowerShell command:</span></span>

    (Get-CsUser).Count

<span data-ttu-id="62809-151">Если предыдущая команда возвращает значение 1 236 и уникальный вход Users, функция метрика Возвращает среднее значение 667, что предполагает, что в системе для работы в Lync будет вести себя несколько раз в день (например, 667 на 1 236, который составляет примерно 54%).</span><span class="sxs-lookup"><span data-stu-id="62809-151">If the preceding command returns a value of 1,236 and Unique logon users metric returns an average value of 667, that suggests that a little over half of your users enable for Lync are actually logging on to the system each day (that is, 667 divided by 1,236, which is approximately 54%).</span></span>

<div>


> [!WARNING]  
> <span data-ttu-id="62809-152">Следует иметь в виду, что показателями входов учитываются пользователи, которые на самом деле входили в систему в указанный период времени.</span><span class="sxs-lookup"><span data-stu-id="62809-152">Keep in mind that the logon metrics record users who actually logged on during the specified time period.</span></span> <span data-ttu-id="62809-153">Они не учитывают пользователей, которые уже были зарегистрированы в системе.</span><span class="sxs-lookup"><span data-stu-id="62809-153">They don't keep track of users who were already logged on to the system.</span></span> <span data-ttu-id="62809-154">Например, если показатель количества уникальных регистрировавшихся пользователей равен 667 и имеется 1236 пользователей, это свидетельствует о том, что около половины пользователей входят в систему.</span><span class="sxs-lookup"><span data-stu-id="62809-154">For example, if your Unique logon users metric shows 667 logons and you have 1,236 users, that suggests that about half your users are logging on to the system.</span></span> <span data-ttu-id="62809-155">Однако предположим, что 300 пользователей уже находились в системе на момент, когда началась проверка данных о регистрации.</span><span class="sxs-lookup"><span data-stu-id="62809-155">However, suppose 300 users were already logged on to the system at the time you began checking the logon data.</span></span> <span data-ttu-id="62809-156">Это означает, что у тебя есть почти 1 000 пользователей, выполнивших вход на сервер Lync Server, что означает, что ближе к 80% ваших пользователей.</span><span class="sxs-lookup"><span data-stu-id="62809-156">That would mean that you actually had nearly 1,000 users logged on to Lync Server, which would mean that closer to 80% of your users were logged on.</span></span>



</div>

<span data-ttu-id="62809-157">Следует также сравнить значение показателя количества уникальных регистрировавшихся пользователей со значением показателя количества уникальных активных пользователей.</span><span class="sxs-lookup"><span data-stu-id="62809-157">You should also compare the Unique logon users value with the value of the Unique active users metric.</span></span> <span data-ttu-id="62809-158">Метрика "уникальные активные пользователи" показывает, сколько уникальных пользователей использует Lync Server: они были присоединены к собранию Lync или участвуют в сеансе обмена мгновенными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="62809-158">The Unique active users metric tells you how many unique users actually used Lync Server: they made a phone call, they joined a Lync Meeting, or they participated in an IM session.</span></span> <span data-ttu-id="62809-159">Это полезные сведения, так как Microsoft Lync 2013 может автоматически запускаться каждый раз при запуске Windows.</span><span class="sxs-lookup"><span data-stu-id="62809-159">This is useful information, because Microsoft Lync 2013 can be configured to automatically start each time a user starts Windows.</span></span> <span data-ttu-id="62809-160">Из-за этого у вас может быть большое количество пользователей, которые автоматически подключаются к Lync при каждом входе в Windows каждый день, но не используют Lync Server в течение этого периода времени.</span><span class="sxs-lookup"><span data-stu-id="62809-160">Because of that, you might have a large number of users who automatically log on to Lync when they log on to Windows each day, but then never actually use Lync Server during that time period.</span></span>

<span data-ttu-id="62809-161">Метрика уникальных активных пользователей также предоставляет более осмысленные данные в Организации, где пользователи обычно не завершают работу с Windows в конце дня.</span><span class="sxs-lookup"><span data-stu-id="62809-161">The Unique active users metric also provides more meaningful data in an organization where users typically do not log off Windows at the end of the day.</span></span> <span data-ttu-id="62809-162">Вместо этого они просто заблокировали свои компьютеры, оставив Windows и Lync запущенными.</span><span class="sxs-lookup"><span data-stu-id="62809-162">Instead, they simply lock their computers and leave Windows and Lync running.</span></span> <span data-ttu-id="62809-163">В подобной ситуации каждый день может происходить всего несколько входов в систему, так как пользователи зарегистрировались несколько дней назад и с тех пор не выходили из системы.</span><span class="sxs-lookup"><span data-stu-id="62809-163">In a situation like that, you might end up with very few logons per day because your users logged on several days ago and never logged off.</span></span> <span data-ttu-id="62809-164">Однако уникальные активные пользователи сообщают, активно ли пользователи с помощью Lync или другого клиента сервера Lync Server.</span><span class="sxs-lookup"><span data-stu-id="62809-164">However, Unique active users tells you whether users are actively using Lync or another Lync Server client.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="62809-165">Фильтры</span><span class="sxs-lookup"><span data-stu-id="62809-165">Filters</span></span>

<span data-ttu-id="62809-166">Фильтры позволяют возвращать более точный набор данных или различными способами просматривать возвращенные данные.</span><span class="sxs-lookup"><span data-stu-id="62809-166">Filters provide a way for you to return a more finely targeted set of data or to view the returned data in different ways.</span></span> <span data-ttu-id="62809-167">Например, с помощью отчета регистрация пользователей можно просматривать данные всех пулов регистраторов и пограничных серверов, а также просматривать данные для отдельного пула.</span><span class="sxs-lookup"><span data-stu-id="62809-167">For example, the User Registration Report enables you to view data for all your Registrar pool and Edge Servers or to view data for an individual pool.</span></span> <span data-ttu-id="62809-168">Можно также выбрать порядок группирования данных.</span><span class="sxs-lookup"><span data-stu-id="62809-168">You can also choose how data should be grouped.</span></span> <span data-ttu-id="62809-169">В этом случае регистрации группируются по времени, дням, неделям или месяцам.</span><span class="sxs-lookup"><span data-stu-id="62809-169">In this case, registrations grouped by hour, day, week, or month.</span></span>

<span data-ttu-id="62809-170">В следующей таблице приведены фильтры, которые можно использовать с отчетом о регистрации пользователей.</span><span class="sxs-lookup"><span data-stu-id="62809-170">The following table lists the filters that you can use with the User Registration Report.</span></span>

### <a name="user-registration-report-filters"></a><span data-ttu-id="62809-171">Фильтры отчета о регистрации пользователей</span><span class="sxs-lookup"><span data-stu-id="62809-171">User Registration Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="62809-172">Имя</span><span class="sxs-lookup"><span data-stu-id="62809-172">Name</span></span></th>
<th><span data-ttu-id="62809-173">Описание</span><span class="sxs-lookup"><span data-stu-id="62809-173">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="62809-174"><strong>От</strong></span><span class="sxs-lookup"><span data-stu-id="62809-174"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="62809-p113">Начальная дата и начальное время для диапазона времени. Чтобы просмотреть данные по часам, введите начальную дату и начальное время в следующем формате:</span><span class="sxs-lookup"><span data-stu-id="62809-p113">Start date and time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="62809-177">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="62809-177">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="62809-p114">Если вы не вводите начальное время, отчет автоматически начинается с 12:00 AM указанного дня. Чтобы просмотреть данные по дням, просто введите дату:</span><span class="sxs-lookup"><span data-stu-id="62809-p114">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="62809-180">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="62809-180">7/7/2012</span></span></p>
<p><span data-ttu-id="62809-181">Чтобы просмотреть данные за неделю или месяц, введите дату, выпадающую на любое время в рамках недели или месяца, которые вы хотите просмотреть (вам не требуется вводить первый день недели или месяца):</span><span class="sxs-lookup"><span data-stu-id="62809-181">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="62809-182">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="62809-182">7/3/2012</span></span></p>
<p><span data-ttu-id="62809-183">Недели всегда отсчитываются с воскресенья по субботу.</span><span class="sxs-lookup"><span data-stu-id="62809-183">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62809-184"><strong>До</strong></span><span class="sxs-lookup"><span data-stu-id="62809-184"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="62809-p115">Конечная дата и конечное время для диапазона времени. Чтобы просмотреть данные по часам, введите конечную дату и конечное время в следующем формате:</span><span class="sxs-lookup"><span data-stu-id="62809-p115">End date and time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="62809-187">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="62809-187">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="62809-p116">Если вы не вводите конечное время, отчет автоматически заканчивается в 12:00 AM указанного дня. Чтобы просмотреть данные по дням, просто введите дату:</span><span class="sxs-lookup"><span data-stu-id="62809-p116">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="62809-190">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="62809-190">7/7/2012</span></span></p>
<p><span data-ttu-id="62809-191">Чтобы просмотреть данные за неделю или месяц, введите дату, выпадающую на любое время в рамках недели или месяца, которые вы хотите просмотреть (вам не требуется вводить первый день недели или месяца):</span><span class="sxs-lookup"><span data-stu-id="62809-191">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="62809-192">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="62809-192">7/3/2012</span></span></p>
<p><span data-ttu-id="62809-193">Недели всегда отсчитываются с воскресенья по субботу.</span><span class="sxs-lookup"><span data-stu-id="62809-193">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62809-194"><strong>Интервал</strong></span><span class="sxs-lookup"><span data-stu-id="62809-194"><strong>Interval</strong></span></span></p></td>
<td><p><span data-ttu-id="62809-p117">Временной интервал. Выберите одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="62809-p117">Time interval. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="62809-197">Ежечасно (можно отобразить не более 25 часов)</span><span class="sxs-lookup"><span data-stu-id="62809-197">Hourly (a maximum of 25 hours can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="62809-198">Ежедневно (можно отобразить не более 31 дня)</span><span class="sxs-lookup"><span data-stu-id="62809-198">Daily (a maximum of 31 days can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="62809-199">Еженедельно (можно отобразить не более 12 недель)</span><span class="sxs-lookup"><span data-stu-id="62809-199">Weekly (a maximum of 12 weeks can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="62809-200">Ежемесячно (можно отобразить не более 12 месяцев)</span><span class="sxs-lookup"><span data-stu-id="62809-200">Monthly (a maximum of 12 months can be displayed)</span></span></p></li>
</ul>
<p><span data-ttu-id="62809-201">Если число значений между начальной и конечной датами превышает максимальное допустимое для выбранного интервала, отображается максимальное возможное число значений (с начальной даты).</span><span class="sxs-lookup"><span data-stu-id="62809-201">If the start and end dates exceed the maximum number of values allowed for the selected interval, only the maximum number of values (starting from the start date) are displayed.</span></span> <span data-ttu-id="62809-202">Например, если выбрать ежедневный интервал с датой начала 7/7/2012 и датой окончания 2/28/2012, данные будут выводиться для дней 8/7/2012 12:00 – 9/7/2012 12:00 AM (то есть, всего за 31 дня).</span><span class="sxs-lookup"><span data-stu-id="62809-202">For example, if you select the Daily interval with a start date of 7/7/2012 and an end date of 2/28/2012, data is displayed for the days 8/7/2012 12:00 AM to 9/7/2012 12:00 AM (that is, a total of 31 days' worth of data).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62809-203"><strong>Pool</strong></span><span class="sxs-lookup"><span data-stu-id="62809-203"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="62809-204">Полное доменное имя пула регистратора или пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="62809-204">Fully qualified domain name (FQDN) of the Registrar pool or Edge Server.</span></span> <span data-ttu-id="62809-205">Можно выбрать отдельный пул или выбрать <strong>[Все]</strong>, чтобы просмотреть данные для всех пулов.</span><span class="sxs-lookup"><span data-stu-id="62809-205">You can either select an individual pool or choose <strong>[All]</strong> to view data for all the pools.</span></span> <span data-ttu-id="62809-206">Данный раскрывающийся список заполняется автоматически на основе записей, имеющихся в базе данных.</span><span class="sxs-lookup"><span data-stu-id="62809-206">This drop-down list is automatically populated for you based on the records in the database.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics"></a><span data-ttu-id="62809-207">Показатели</span><span class="sxs-lookup"><span data-stu-id="62809-207">Metrics</span></span>

<span data-ttu-id="62809-208">В следующей таблице представлены сведения, приведенные в отчете о регистрации пользователей.</span><span class="sxs-lookup"><span data-stu-id="62809-208">The following table lists the information provided in the User Registration Report.</span></span>

### <a name="user-registration-report-metrics"></a><span data-ttu-id="62809-209">Показатели отчета о регистрации пользователей</span><span class="sxs-lookup"><span data-stu-id="62809-209">User Registration Report Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="62809-210">Имя</span><span class="sxs-lookup"><span data-stu-id="62809-210">Name</span></span></th>
<th><span data-ttu-id="62809-211">Поддержка сортировки</span><span class="sxs-lookup"><span data-stu-id="62809-211">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="62809-212">Описание</span><span class="sxs-lookup"><span data-stu-id="62809-212">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="62809-213"><strong>Ежечасно</strong></span><span class="sxs-lookup"><span data-stu-id="62809-213"><strong>Hourly</strong></span></span></p>
<p><span data-ttu-id="62809-214"><strong>Ежедневно</strong></span><span class="sxs-lookup"><span data-stu-id="62809-214"><strong>Daily</strong></span></span></p>
<p><span data-ttu-id="62809-215"><strong>Еженедельно</strong></span><span class="sxs-lookup"><span data-stu-id="62809-215"><strong>Weekly</strong></span></span></p>
<p><span data-ttu-id="62809-216"><strong>Ежемесячно</strong></span><span class="sxs-lookup"><span data-stu-id="62809-216"><strong>Monthly</strong></span></span></p></td>
<td><p><span data-ttu-id="62809-217">Нет</span><span class="sxs-lookup"><span data-stu-id="62809-217">No</span></span></p></td>
<td><p><span data-ttu-id="62809-218">Указывает на временной интервал, выбранный на панели фильтров.</span><span class="sxs-lookup"><span data-stu-id="62809-218">Indicates the time interval that you selected on the filter toolbar.</span></span> <span data-ttu-id="62809-219">Вы можете щелкнуть временной интервал, чтобы просмотреть подробные сведения для него, если они доступны.</span><span class="sxs-lookup"><span data-stu-id="62809-219">Where applicable, you can click a given time interval to view detailed information for that interval.</span></span> <span data-ttu-id="62809-220">Например, если вы используете ежедневный интервал и нажимайте 7/7/2012, появится Почасовая подразделение действия регистрации пользователя для этой даты.</span><span class="sxs-lookup"><span data-stu-id="62809-220">For example, if you are using the Daily interval and you click 7/7/2012, you see an hourly breakdown of user registration activity for that date.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62809-221"><strong>Общее количество входов</strong></span><span class="sxs-lookup"><span data-stu-id="62809-221"><strong>Total logons</strong></span></span></p></td>
<td><p><span data-ttu-id="62809-222">Нет</span><span class="sxs-lookup"><span data-stu-id="62809-222">No</span></span></p></td>
<td><p><span data-ttu-id="62809-223">Общее количество успешных сеансов входа.</span><span class="sxs-lookup"><span data-stu-id="62809-223">Total number of successful logon sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62809-224"><strong>Количество внутренних входов</strong></span><span class="sxs-lookup"><span data-stu-id="62809-224"><strong>Internal logons</strong></span></span></p></td>
<td><p><span data-ttu-id="62809-225">Нет</span><span class="sxs-lookup"><span data-stu-id="62809-225">No</span></span></p></td>
<td><p><span data-ttu-id="62809-226">Общее количество входов в систему в пределах внутренней сети.</span><span class="sxs-lookup"><span data-stu-id="62809-226">Total number of logons within the internal network.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62809-227"><strong>Количество внешних входов</strong></span><span class="sxs-lookup"><span data-stu-id="62809-227"><strong>External logons</strong></span></span></p></td>
<td><p><span data-ttu-id="62809-228">Нет</span><span class="sxs-lookup"><span data-stu-id="62809-228">No</span></span></p></td>
<td><p><span data-ttu-id="62809-229">Общее количество входов в систему из внешних сетей с использованием пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="62809-229">Total number of logons from outside the internal network, using the Edge Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62809-230"><strong>Количество уникальных входов пользователей</strong></span><span class="sxs-lookup"><span data-stu-id="62809-230"><strong>Unique logon users</strong></span></span></p></td>
<td><p><span data-ttu-id="62809-231">Нет</span><span class="sxs-lookup"><span data-stu-id="62809-231">No</span></span></p></td>
<td><p><span data-ttu-id="62809-p121">Общее количество пользователей хотя бы с одним сеансом входа. Пользователь с несколькими сеансами входа считается как один пользователь, так же, как и пользователь с одним сеансом входа.</span><span class="sxs-lookup"><span data-stu-id="62809-p121">Total number of users who had at least one logon session. A user who had multiple logon sessions counts as one user, the same as a person who had just a single logon session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62809-234"><strong>Количество активных пользователей</strong></span><span class="sxs-lookup"><span data-stu-id="62809-234"><strong>Unique active users</strong></span></span></p></td>
<td><p><span data-ttu-id="62809-235">Нет</span><span class="sxs-lookup"><span data-stu-id="62809-235">No</span></span></p></td>
<td><p><span data-ttu-id="62809-p122">Общее количество пользователей, участвующих в одноранговом сеансе или сеансе конференции. Пользователь с несколькими сеансами считается как один пользователь, так же, как и пользователь с одним сеансом входа.</span><span class="sxs-lookup"><span data-stu-id="62809-p122">Total number of users who were involved in a peer-to-peer or conferencing session. A user who had multiple sessions counts as one user, the same as a person who had just a single session.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="62809-238">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="62809-238">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

