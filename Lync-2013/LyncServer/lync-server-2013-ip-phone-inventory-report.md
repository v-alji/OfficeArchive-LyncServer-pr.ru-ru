---
title: 'Lync Server 2013: отчет о запасах IP-телефона'
description: 'Lync Server 2013: отчет "Инвентаризация IP-телефона".'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: IP Phone Inventory Report
ms:assetid: aa7d6b31-cb09-4e68-b020-aa5dd0081c20
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615027(v=OCS.15)
ms:contentKeyID: 48185044
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3bc05017775ad64e0e18f876215aa2c6b3882bd7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426741"
---
# <a name="ip-phone-inventory-report-in-lync-server-2013"></a><span data-ttu-id="7221d-103">Отчет о запасах IP-телефона в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7221d-103">IP Phone Inventory Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7221d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7221d-104">

<span> </span></span></span>

<span data-ttu-id="7221d-105">_**Тема последнего изменения:** 2012-11-12_</span><span class="sxs-lookup"><span data-stu-id="7221d-105">_**Topic Last Modified:** 2012-11-12_</span></span>

<span data-ttu-id="7221d-p101">Отчет по IP-телефонам предоставляет сведения о IP-телефонах, используемых в организации. В отчете по IP-телефонам содержится список IP-телефонов, которые использовались в течение периода, заданного при создании отчета. С помощью этого отчета администраторы могут получить сведения об устаревших телефонах, которые требуется заменить, а также сведения о редко используемых дорогостоящих телефонах. Эти данные могут использоваться при планировании покупки новых телефонов или перераспределении имеющихся телефонов. (Например, пользователь, который редко использует дорогостоящий телефон, может поменяться телефоном с пользователем, который использует телефон чаще.)</span><span class="sxs-lookup"><span data-stu-id="7221d-p101">The IP Phone Inventory Report reports information about the IP phones currently in use in your organization. The IP Inventory Report provides a detailed list of the IP phones that were actually used during the specified reporting period. Among other things, this report lets administrators know if there are any old, outdated phones still in use that should be replaced; it can also alert administrators to the fact that there are expensive phones in the organization that are rarely being used. That type of information can be invaluable when it comes time to purchase new phones or to redistribute existing phones. (For example, a user who rarely uses his or her expensive phone might be asked to swap phones with a user who uses his or her phone much more frequently.)</span></span>

<span data-ttu-id="7221d-111">Следует отметить, что этот отчет имеет некоторые ограничения для случая использования данных отчета в реальном складском учете.</span><span class="sxs-lookup"><span data-stu-id="7221d-111">It should be noted that this report does have a few limitations when it comes to being used as a true inventory report.</span></span> <span data-ttu-id="7221d-112">В одном случае в отчете IP Phone отображаются все телефоны, которые вошли на сервер Lync Server за указанный период времени, отсортированный по времени последнего входа.</span><span class="sxs-lookup"><span data-stu-id="7221d-112">For one thing, the IP Phone Report simply lists all the phones that logged on to Lync Server during the specified time period, sorted by their last logon time.</span></span> <span data-ttu-id="7221d-113">Если телефон не выполнял вход в течение указанного периода времени, он будет отсутствовать в этом отчете.</span><span class="sxs-lookup"><span data-stu-id="7221d-113">If a phone did not log on during the specified time period then it will not be listed in the inventory report.</span></span> <span data-ttu-id="7221d-114">Это относится также к телефонам, которые выполнили вход до начального периода создания отчета и остаются в системе в течение указанного периода времени.</span><span class="sxs-lookup"><span data-stu-id="7221d-114">That includes phones that logged on before the time period started and were still logged on during the specified time interval.</span></span> <span data-ttu-id="7221d-115">Например, предположим, что вы хотели бы просмотреть все запасы на телефоне за Июль 2012.</span><span class="sxs-lookup"><span data-stu-id="7221d-115">For example, suppose you wanted to look at all the phone inventory for July, 2012.</span></span> <span data-ttu-id="7221d-116">Предположим, что несколько телефонов вошли в Lync Server 30 июня 2012, и они все еще вошли в систему на 1 июля.</span><span class="sxs-lookup"><span data-stu-id="7221d-116">Suppose, as well, that several phones logged on to Lync Server on June 30, 2012 and were still logged on as of July 1st.</span></span> <span data-ttu-id="7221d-117">Эти телефоны не будут добавлены в отчет за 1 июля 2012 г.</span><span class="sxs-lookup"><span data-stu-id="7221d-117">Those phones will not show up on the inventory report for July 1st.</span></span>

<span data-ttu-id="7221d-118">Кроме того, отчет может содержать телефоны, которые уже не используются в организации.</span><span class="sxs-lookup"><span data-stu-id="7221d-118">It's also important to note that the inventory report could include phones that your organization no longer uses.</span></span> <span data-ttu-id="7221d-119">Например, предположим, что несколько телефонов Fabrikam вошли в систему 1 июля 2012 г. за 5 дней после того, как ваша организация заменила все телефоны Fabrikam и заменяет их новой моделью contoso.</span><span class="sxs-lookup"><span data-stu-id="7221d-119">For example, suppose a number of Fabrikam phones logged on to the system on July 1, 2012; 5 days later your organization got rid of all those Fabrikam phones and replaced them with a newer Contoso model.</span></span> <span data-ttu-id="7221d-120">Телефоны Fabrikam будут отображаться в отчете, поскольку они выполнили вход в систему в течение июля.</span><span class="sxs-lookup"><span data-stu-id="7221d-120">The Fabrikam phones will still appear on the "inventory" report simply because they logged on to the system during the month of July.</span></span>

<span data-ttu-id="7221d-p104">Кроме того, в отчете отсутствуют сведения о количестве разных моделей телефонов. Например, в организации установлено 105 телефонов модели Polycom CX600. В отчете вместо общего количества телефонов этой модели вы увидите 105 отдельных записей для телефонов Polycom Cx600. Чтобы узнать количество телефонов модели Polycom Cx600, потребуется посчитать количество строк вручную.</span><span class="sxs-lookup"><span data-stu-id="7221d-p104">In addition, the IP Phone Inventory Report does not report summary totals for the different types of phones. For example, suppose you have 105 Polycom CX600 phones. The report will not tell you that you have 105 of these phones; instead, you will simply see 105 separate entries for the Polycom Cx600. The only way to know that there are 105 entries for the Polycom Cx600 would be to count each of those entries manually.</span></span>

<div>


> [!WARNING]  
> <span data-ttu-id="7221d-125">В качестве альтернативного варианта можно экспортировать данные в Microsoft Excel или Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7221d-125">Or, export the data and use Microsoft Excel or Windows PowerShell to do that counting for you.</span></span>



</div>

<div>

## <a name="accessing-the-ip-phone-inventory-report"></a><span data-ttu-id="7221d-126">Доступ к отчету по IP-телефонам</span><span class="sxs-lookup"><span data-stu-id="7221d-126">Accessing the IP Phone Inventory Report</span></span>

<span data-ttu-id="7221d-p105">Для доступа к отчету по IP-телефонам используется домашняя страница Monitoring Reports (Отчеты мониторинга). При выборе показателя User URI (URI пользователя) откроется отчет User Activity Report (Действия пользователя). При выборе показателя Last activity (Последнее действие) для одноранговых звонков откроется отчет Peer-to-Peer Session Detail Report (Сведения об одноранговом сеансе). При выборе того же показателя для конференции откроется отчет Conference Detail Report (Сведения о конференции).</span><span class="sxs-lookup"><span data-stu-id="7221d-p105">The IP Phone Inventory Report is accessed from the Monitoring Reports home page. If you click the User URI metric you can access the User Activity Report for that user. Clicking the Last activity metric for a peer-to-peer call will take you to the Peer-to-Peer Session Detail Report; clicking that same metric for a conference will take you to the Conference Detail Report.</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-ip-phone-inventory-report"></a><span data-ttu-id="7221d-130">Рекомендации по использованию отчета по IP-телефонам</span><span class="sxs-lookup"><span data-stu-id="7221d-130">Making the Best Use of the IP Phone Inventory Report</span></span>

<span data-ttu-id="7221d-131">Если вы заинтересованы в сведениях об использовании только для одного определенного типа телефона (например, "как часто пользователи работают с Polycom CX600), вы можете получить эту информацию непосредственно из отчета" Инвентаризация IP-телефона "с помощью фильтрации для определенного типа телефона.</span><span class="sxs-lookup"><span data-stu-id="7221d-131">If you're only interested in usage information for one particular kind of phone (for example, "How often are users using a Polycom CX600 phone?") you can get that information directly from the IP Phone Inventory Report by filtering for that particular kind of phone.</span></span> <span data-ttu-id="7221d-132">Тем не менее, если вы хотите получить сводную информацию для всех своих телефонов (количество людей, использующих Polycom CX600, количество используемых LG-Nortel IP8540 и т. д.), тогда вам потребуется экспортировать данные и использовать другое приложение (например, Windows PowerShell) для выполнения этого типа анализа.</span><span class="sxs-lookup"><span data-stu-id="7221d-132">However, if you want summary information for all your phones (how many people are using a Polycom CX600, how many are using an LG-Nortel IP8540, etc.) then you will need to export the data and use another application (such as Windows PowerShell) to do that type of analysis.</span></span> <span data-ttu-id="7221d-133">Например, предположим, что вы экспортируете данные в файл с разделителями-запятыми (C: \\ \\ \_ Инвентаризация IP-номеров \_ \_Report.csv).</span><span class="sxs-lookup"><span data-stu-id="7221d-133">For example, suppose you export the data to a comma-separated values file (C:\\Data\\IP\_Phone\_Inventory\_Report.csv).</span></span> <span data-ttu-id="7221d-134">В этом случае вы можете использовать эти две команды для предоставления сводных данных для всех телефонов.</span><span class="sxs-lookup"><span data-stu-id="7221d-134">In that case, you could use these two commands to provide summary data for all your phones:</span></span>

    $phones = Import-Csv "C:\Data\IP_Phone_Inventory_Report.csv"
    $phones |Group-Object Manufacturer, "Hardware version" | Select-Object Count, Name | Sort-Object Count -Descending

<span data-ttu-id="7221d-135">Эти команды возвращают сведения, схожие со следующими:</span><span class="sxs-lookup"><span data-stu-id="7221d-135">That will return data similar to this:</span></span>

    Count    Name
    -----    ----
      267    POLYCOM, CX700
      267    POLYCOM, CX600
      166    POLYCOM, C
       68    Microsoft, CPE
       64    LG-Nortel, IP8540
       59    Aastra, 6725ip
       37    LG-Nortel, IP
       22    POLYCOM, CX3000
       11    Microsoft, CPE_A
        9    POLYCOM, CX500
        7    Aastra, 6721ip

<span data-ttu-id="7221d-136">Следующие команды возвращают сведения о телефонах, которые выполнили вход в систему, но никогда не использовались для звонков (на это указывает отсутствие значения показателя Last activity (Последнее действие)):</span><span class="sxs-lookup"><span data-stu-id="7221d-136">Similarly, these two commands tell you which phones logged on to the system but were never actually used to make a call (the value of the Last activity metric is blank, indicating that there hasn't been any last activity):</span></span>

    $phones = Import-Csv "C:\Data\IP_Phone_Inventory_Report.csv"
    $phones | Where-Object {$_."Last activity" -eq ""}

<span data-ttu-id="7221d-137">Команды возвращают данные, схожие со следующими:</span><span class="sxs-lookup"><span data-stu-id="7221d-137">That returns data similar to this for each phone that has not been used:</span></span>

    Manufacturer     : POLYCOM
    Hardware version : CX600
    MAC address      : 00-04-F2-00-01-76
    User URI         : 422
    User agent       : CPE/4.0.7423.1 OCPhone/4.0.7423.1 (Microsoft Lync 2010 (Beta) Phone Edition)
    Last logon time  : 8/30/2010 4:44:48 PM
    Last logoff time : 8/30/2010 5:59:07 PM
    Last activity    :

<span data-ttu-id="7221d-138">Другой интересный способ использования отчета по IP-телефонам: если у IP-телефона есть MAC-адрес, то для получения сведений о пользователе, который использовал этот телефон последним, введите требуемый MAC-адрес в соответствующее поле.</span><span class="sxs-lookup"><span data-stu-id="7221d-138">Another interesting way to use the IP Phone Inventory Report is this: if you have the MAC address of an IP Phone you can find out the user who last used that phone simply by entering that address in the MAC address text box.</span></span> <span data-ttu-id="7221d-139">Отчет по IP-телефонам вернет SIP-адрес последнего пользователя, выполнившего вход в систему.</span><span class="sxs-lookup"><span data-stu-id="7221d-139">The IP Phone Inventory report will then report back (among other things) the SIP address of the user who last logged on with that phone.</span></span> <span data-ttu-id="7221d-140">В качестве альтернативного варианта для поиска всех телефонов, используемых этим пользователем, введите SIP-адрес пользователя (в поле User URI (URI пользователя)).</span><span class="sxs-lookup"><span data-stu-id="7221d-140">Alternatively, you can enter a user SIP address (in the User URI prefix box) to find out all the phones that have been used by that user.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="7221d-141">Фильтры</span><span class="sxs-lookup"><span data-stu-id="7221d-141">Filters</span></span>

<span data-ttu-id="7221d-p108">Фильтры позволяют получить более детализированный набор данных или изменить способ просмотра возвращаемых данных. Например, с помощью отчета по IP-телефонам можно получить сведения о телефонах определенного производителя или телефонах конкретной модели. Кроме того, вы можете задать параметры группировки данных. В этом случае регистрации группируются по часам, дням, неделям или месяцам.</span><span class="sxs-lookup"><span data-stu-id="7221d-p108">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. For example, the IP Phone Inventory enables you to view only the phones manufactured by a specific company, or even a specific version of those phones. You can also choose how data should be grouped. In this case, registrations are grouped by hour, day, week, or month.</span></span>

<span data-ttu-id="7221d-146">В следующей таблице перечислены фильтры, доступные в отчете по IP-телефонам.</span><span class="sxs-lookup"><span data-stu-id="7221d-146">The following table lists the filters that you can use with the IP Phone Inventory Report.</span></span>

### <a name="ip-phone-inventory-report-filters"></a><span data-ttu-id="7221d-147">Фильтры отчета по IP-телефонам</span><span class="sxs-lookup"><span data-stu-id="7221d-147">IP Phone Inventory Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7221d-148">Имя</span><span class="sxs-lookup"><span data-stu-id="7221d-148">Name</span></span></th>
<th><span data-ttu-id="7221d-149">Описание</span><span class="sxs-lookup"><span data-stu-id="7221d-149">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7221d-150"><strong>От</strong></span><span class="sxs-lookup"><span data-stu-id="7221d-150"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="7221d-p109">Начальные дата/время для временного диапазона. Чтобы просмотреть данные по часам, введите начальные дату и время следующим образом:</span><span class="sxs-lookup"><span data-stu-id="7221d-p109">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="7221d-153">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="7221d-153">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="7221d-p110">Если вы не вводите начальное время, отчет автоматически начинается с 12:00 AM указанного дня. Чтобы просмотреть данные по дням, просто введите дату:</span><span class="sxs-lookup"><span data-stu-id="7221d-p110">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="7221d-156">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="7221d-156">7/7/2012</span></span></p>
<p><span data-ttu-id="7221d-157">Чтобы просмотреть данные за неделю или месяц, введите дату, выпадающую на любое время в рамках недели или месяца, которые вы хотите просмотреть (вам не требуется вводить первый день недели или месяца):</span><span class="sxs-lookup"><span data-stu-id="7221d-157">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="7221d-158">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="7221d-158">7/3/2012</span></span></p>
<p><span data-ttu-id="7221d-159">Недели всегда отсчитываются с воскресенья по субботу.</span><span class="sxs-lookup"><span data-stu-id="7221d-159">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7221d-160"><strong>До</strong></span><span class="sxs-lookup"><span data-stu-id="7221d-160"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="7221d-p111">Конечные дата/время для временного диапазона. Чтобы просмотреть данные по часам, введите конечные дату и время следующим образом:</span><span class="sxs-lookup"><span data-stu-id="7221d-p111">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="7221d-163">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="7221d-163">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="7221d-p112">Если вы не вводите конечное время, отчет автоматически заканчивается в 12:00 AM указанного дня. Чтобы просмотреть данные по дням, просто введите дату:</span><span class="sxs-lookup"><span data-stu-id="7221d-p112">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="7221d-166">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="7221d-166">7/7/2012</span></span></p>
<p><span data-ttu-id="7221d-167">Чтобы просмотреть данные за неделю или месяц, введите дату, выпадающую на любое время в рамках недели или месяца, которые вы хотите просмотреть (вам не требуется вводить первый день недели или месяца):</span><span class="sxs-lookup"><span data-stu-id="7221d-167">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="7221d-168">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="7221d-168">7/3/2012</span></span></p>
<p><span data-ttu-id="7221d-169">Недели всегда отсчитываются с воскресенья по субботу.</span><span class="sxs-lookup"><span data-stu-id="7221d-169">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7221d-170"><strong>Производитель</strong></span><span class="sxs-lookup"><span data-stu-id="7221d-170"><strong>Manufacturer</strong></span></span></p></td>
<td><p><span data-ttu-id="7221d-p113">Название компании, создавшей IP-телефон. Значения для данного фильтра заполняются автоматически на основе данных об IP-телефонах, хранящихся в базе данных.</span><span class="sxs-lookup"><span data-stu-id="7221d-p113">Name of the company that manufactured the IP phone. The values for this filter are automatically populated for you based on the IP phones that are currently in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7221d-173"><strong>Версия оборудования</strong></span><span class="sxs-lookup"><span data-stu-id="7221d-173"><strong>Hardware version</strong></span></span></p></td>
<td><p><span data-ttu-id="7221d-174">Номер версии IP-телефона; используя изготовитель и фильтры аппаратных версий, вы можете уникальным образом идентифицировать конкретный тип телефона.</span><span class="sxs-lookup"><span data-stu-id="7221d-174">Version number of the IP phone; by using the Manufacturer and the Hardware version filters you can uniquely identity a particular type of phone.</span></span> <span data-ttu-id="7221d-175">Значения для данного фильтра заполняются автоматически на основе данных об IP-телефонах, хранящихся в базе данных.</span><span class="sxs-lookup"><span data-stu-id="7221d-175">The values for this filter are automatically populated for you based on the IP phones that are currently in the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7221d-176"><strong>Агент пользователя</strong></span><span class="sxs-lookup"><span data-stu-id="7221d-176"><strong>User agent</strong></span></span></p></td>
<td><p><span data-ttu-id="7221d-p115">Идентификатор программного обеспечения, используемого IP-телефоном. Значения для данного фильтра заполняются автоматически на основе данных об IP-телефонах, хранящихся в базе данных.</span><span class="sxs-lookup"><span data-stu-id="7221d-p115">Identifier for the software used by the IP phone. The values for this filter are automatically populated for you based on the IP phones currently in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7221d-179"><strong>MAC-адрес</strong></span><span class="sxs-lookup"><span data-stu-id="7221d-179"><strong>MAC address</strong></span></span></p></td>
<td><p><span data-ttu-id="7221d-p116">Уникальный идентификатор сетевого интерфейса IP-телефона. Обычно MAC-адрес задается производителем и не поддерживает изменение.</span><span class="sxs-lookup"><span data-stu-id="7221d-p116">Unique identifier for the network interface on the IP phone. The Media Access Control (MAC) address is typically assigned at the time the phone is manufactured and is hard-wired into the device hardware.</span></span></p>
<p><span data-ttu-id="7221d-p117">Чтобы найти записи, относящиеся к определенному MAC-адресу, введите требуемый MAC-адрес. Пример:</span><span class="sxs-lookup"><span data-stu-id="7221d-p117">To search for records pertaining to a specific MAC address simply enter that address. For example:</span></span></p>
<p><span data-ttu-id="7221d-184">00-08-5D-16-16-48</span><span class="sxs-lookup"><span data-stu-id="7221d-184">00-08-5D-16-16-48</span></span></p>
<p><span data-ttu-id="7221d-p118">Требуется вводить полные адреса. При вводе части адреса (например, 00-08-5D) данные не будут возвращены.</span><span class="sxs-lookup"><span data-stu-id="7221d-p118">You must enter the complete address. A partial address (for example 00-08-5D) does not return any data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7221d-187"><strong>Последние действия за период</strong></span><span class="sxs-lookup"><span data-stu-id="7221d-187"><strong>Last activity before days</strong></span></span></p></td>
<td><p><span data-ttu-id="7221d-188">Выберите одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="7221d-188">Select one of the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="7221d-189">[All] (Все)</span><span class="sxs-lookup"><span data-stu-id="7221d-189">[All]</span></span></p></li>
<li><p><span data-ttu-id="7221d-190">5-10</span><span class="sxs-lookup"><span data-stu-id="7221d-190">10</span></span></p></li>
<li><p><span data-ttu-id="7221d-191">средняя</span><span class="sxs-lookup"><span data-stu-id="7221d-191">20</span></span></p></li>
<li><p><span data-ttu-id="7221d-192">30</span><span class="sxs-lookup"><span data-stu-id="7221d-192">30</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7221d-193"><strong>Последние выходы за период</strong></span><span class="sxs-lookup"><span data-stu-id="7221d-193"><strong>Last logoff time before days</strong></span></span></p></td>
<td><p><span data-ttu-id="7221d-194">Выберите одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="7221d-194">Select one of the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="7221d-195">[All] (Все)</span><span class="sxs-lookup"><span data-stu-id="7221d-195">[All]</span></span></p></li>
<li><p><span data-ttu-id="7221d-196">5-10</span><span class="sxs-lookup"><span data-stu-id="7221d-196">10</span></span></p></li>
<li><p><span data-ttu-id="7221d-197">средняя</span><span class="sxs-lookup"><span data-stu-id="7221d-197">20</span></span></p></li>
<li><p><span data-ttu-id="7221d-198">30</span><span class="sxs-lookup"><span data-stu-id="7221d-198">30</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7221d-199"><strong>Префикс URI пользователя</strong></span><span class="sxs-lookup"><span data-stu-id="7221d-199"><strong>User URI prefix</strong></span></span></p></td>
<td><p><span data-ttu-id="7221d-200">SIP-адрес пользователя, который использует IP-телефон.</span><span class="sxs-lookup"><span data-stu-id="7221d-200">SIP address of the user who used the IP phone.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics"></a><span data-ttu-id="7221d-201">Показатели</span><span class="sxs-lookup"><span data-stu-id="7221d-201">Metrics</span></span>

<span data-ttu-id="7221d-202">В следующей таблице перечислены сведения, доступные в отчете по IP-телефонам.</span><span class="sxs-lookup"><span data-stu-id="7221d-202">The following table lists the information provided in the IP Phone Inventory Report.</span></span>

### <a name="ip-phone-inventory-report-metrics"></a><span data-ttu-id="7221d-203">Показатели отчета по IP-телефонам</span><span class="sxs-lookup"><span data-stu-id="7221d-203">IP Phone Inventory Report Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7221d-204">Имя</span><span class="sxs-lookup"><span data-stu-id="7221d-204">Name</span></span></th>
<th><span data-ttu-id="7221d-205">Поддержка сортировки</span><span class="sxs-lookup"><span data-stu-id="7221d-205">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="7221d-206">Описание</span><span class="sxs-lookup"><span data-stu-id="7221d-206">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7221d-207"><strong>Производитель</strong></span><span class="sxs-lookup"><span data-stu-id="7221d-207"><strong>Manufacturer</strong></span></span></p></td>
<td><p><span data-ttu-id="7221d-208">Да</span><span class="sxs-lookup"><span data-stu-id="7221d-208">Yes</span></span></p></td>
<td><p><span data-ttu-id="7221d-209">Название компании, создавшей IP-телефон.</span><span class="sxs-lookup"><span data-stu-id="7221d-209">Name of the company that manufactured the IP phone.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7221d-210"><strong>Версия оборудования</strong></span><span class="sxs-lookup"><span data-stu-id="7221d-210"><strong>Hardware version</strong></span></span></p></td>
<td><p><span data-ttu-id="7221d-211">Да</span><span class="sxs-lookup"><span data-stu-id="7221d-211">Yes</span></span></p></td>
<td><p><span data-ttu-id="7221d-212">Номер версии IP-телефона.</span><span class="sxs-lookup"><span data-stu-id="7221d-212">Version number of the IP phone.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7221d-213"><strong>MAC-адрес</strong></span><span class="sxs-lookup"><span data-stu-id="7221d-213"><strong>MAC address</strong></span></span></p></td>
<td><p><span data-ttu-id="7221d-214">Да</span><span class="sxs-lookup"><span data-stu-id="7221d-214">Yes</span></span></p></td>
<td><p><span data-ttu-id="7221d-p119">Уникальный идентификатор сетевого интерфейса IP-телефона. Обычно MAC-адрес задается производителем и не поддерживает изменение.</span><span class="sxs-lookup"><span data-stu-id="7221d-p119">Unique identifier for the network interface on the IP phone. The MAC address is typically assigned at the time the phone is manufactured and is hard-wired into the device hardware.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7221d-217"><strong>URI пользователя</strong></span><span class="sxs-lookup"><span data-stu-id="7221d-217"><strong>User URI</strong></span></span></p></td>
<td><p><span data-ttu-id="7221d-218">Да</span><span class="sxs-lookup"><span data-stu-id="7221d-218">Yes</span></span></p></td>
<td><p><span data-ttu-id="7221d-219">SIP-адрес пользователя, который использует IP-телефон.</span><span class="sxs-lookup"><span data-stu-id="7221d-219">SIP address of the user who used the IP phone.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7221d-220"><strong>Агент пользователя</strong></span><span class="sxs-lookup"><span data-stu-id="7221d-220"><strong>User agent</strong></span></span></p></td>
<td><p><span data-ttu-id="7221d-221">Да</span><span class="sxs-lookup"><span data-stu-id="7221d-221">Yes</span></span></p></td>
<td><p><span data-ttu-id="7221d-222">Идентификатор программного обеспечения, используемого IP-телефоном.</span><span class="sxs-lookup"><span data-stu-id="7221d-222">Identifier for the software used by the IP phone.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7221d-223"><strong>Время последнего входа</strong></span><span class="sxs-lookup"><span data-stu-id="7221d-223"><strong>Last logon time</strong></span></span></p></td>
<td><p><span data-ttu-id="7221d-224">Да</span><span class="sxs-lookup"><span data-stu-id="7221d-224">Yes</span></span></p></td>
<td><p><span data-ttu-id="7221d-225">Дата и время последнего входа на сервер Lync с IP-телефона.</span><span class="sxs-lookup"><span data-stu-id="7221d-225">Date and time that the IP phone last logged on to Lync Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7221d-226"><strong>Last logoff time (Время последнего выхода)</strong></span><span class="sxs-lookup"><span data-stu-id="7221d-226"><strong>Last logoff time</strong></span></span></p></td>
<td><p><span data-ttu-id="7221d-227">Да</span><span class="sxs-lookup"><span data-stu-id="7221d-227">Yes</span></span></p></td>
<td><p><span data-ttu-id="7221d-228">Дата и время последнего выхода из среды Lync Server для IP-телефона.</span><span class="sxs-lookup"><span data-stu-id="7221d-228">Date and time that the IP phone last logged off from Lync Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7221d-229"><strong>Last activity (Последние действия)</strong></span><span class="sxs-lookup"><span data-stu-id="7221d-229"><strong>Last activity</strong></span></span></p></td>
<td><p><span data-ttu-id="7221d-230">Да</span><span class="sxs-lookup"><span data-stu-id="7221d-230">Yes</span></span></p></td>
<td><p><span data-ttu-id="7221d-231">Дата и время последнего использования IP-телефона.</span><span class="sxs-lookup"><span data-stu-id="7221d-231">Date and time that the IP phone was last used.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="7221d-232">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7221d-232">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

