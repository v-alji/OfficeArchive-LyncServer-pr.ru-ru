---
title: 'Lync Server 2013: отчет о списке сбоев'
description: 'Lync Server 2013: отчет о списке отказов.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Failure List Report
ms:assetid: b6f3a605-e0c6-461e-b17a-41d8039ace9d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615446(v=OCS.15)
ms:contentKeyID: 48185194
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7467144fe207ab61fd086cd35aac74779fd4f771
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398179"
---
# <a name="failure-list-report-in-lync-server-2013"></a><span data-ttu-id="e275a-103">Отчет о списке отказов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e275a-103">Failure List Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e275a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e275a-104">

<span> </span></span></span>

<span data-ttu-id="e275a-105">_**Тема последнего изменения:** 2012-07-02_</span><span class="sxs-lookup"><span data-stu-id="e275a-105">_**Topic Last Modified:** 2012-07-02_</span></span>

<span data-ttu-id="e275a-p101">Отчет Failure List (Список ошибок) предоставляет сведения об участниках однорангового сеанса (конференции), завершившегося с ошибкой. Эти сведения содержат URI пользователя, у которого возникла ошибка, а также код ответа SIP и ИД диагностики, связанные с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="e275a-p101">The Failure List report provides information about the individual participants who took part in a failed peer-to-peer or conferencing session. This information includes the URI of the user who experienced the problem, as well as the SIP Response code and Diagnostic ID associated with the failure.</span></span>

<div>

## <a name="accessing-the-failure-list-report"></a><span data-ttu-id="e275a-108">Доступ к отчету Failure List (Список ошибок)</span><span class="sxs-lookup"><span data-stu-id="e275a-108">Accessing the Failure List Report</span></span>

<span data-ttu-id="e275a-109">Для доступа к отчету о списке отказов достаточно щелкнуть один из указанных ниже метрик в [отчете о распределении неисправностей в Lync Server 2013](lync-server-2013-failure-distribution-report.md):</span><span class="sxs-lookup"><span data-stu-id="e275a-109">The Failure List Report is accessed by clicking any of the following metrics on the [Failure Distribution Report in Lync Server 2013](lync-server-2013-failure-distribution-report.md):</span></span>

  - <span data-ttu-id="e275a-110">Top diagnostic reasons (sessions) (Основные причины диагностики (сеансы))</span><span class="sxs-lookup"><span data-stu-id="e275a-110">Top diagnostic reasons (sessions)</span></span>

  - <span data-ttu-id="e275a-111">Top modalities (sessions) (Основные условия (сеансы))</span><span class="sxs-lookup"><span data-stu-id="e275a-111">Top modalities (sessions)</span></span>

  - <span data-ttu-id="e275a-112">Top pools (sessions) (Основные пулы (сеансы))</span><span class="sxs-lookup"><span data-stu-id="e275a-112">Top pools (sessions)</span></span>

  - <span data-ttu-id="e275a-113">Top sources (sessions) (Основные источники (сеансы))</span><span class="sxs-lookup"><span data-stu-id="e275a-113">Top sources (sessions)</span></span>

  - <span data-ttu-id="e275a-114">Top components (sessions) (Основные компоненты (сеансы))</span><span class="sxs-lookup"><span data-stu-id="e275a-114">Top components (sessions)</span></span>

  - <span data-ttu-id="e275a-115">Top from users (sessions) (Основные пользователи с ошибками исходящей связи (сеансы))</span><span class="sxs-lookup"><span data-stu-id="e275a-115">Top from users (sessions)</span></span>

  - <span data-ttu-id="e275a-116">Top to users (sessions) (Основные пользователи с ошибками входящей связи (сеансы))</span><span class="sxs-lookup"><span data-stu-id="e275a-116">Top to users (sessions)</span></span>

  - <span data-ttu-id="e275a-117">Top from user agents (sessions) (Основные агенты пользователей, используемые в сеансах, завершившихся с ошибками (сеансы))</span><span class="sxs-lookup"><span data-stu-id="e275a-117">Top from user agents (sessions)</span></span>

<span data-ttu-id="e275a-118">Из отчета "список отказов" можно получить доступ к [отчету о одноранговых сеансах в Lync Server 2013](lync-server-2013-peer-to-peer-session-detail-report.md) , щелкнув метрику "подробности сеанса" однорангового сеанса.</span><span class="sxs-lookup"><span data-stu-id="e275a-118">From the Failure List Report you can access the [Peer-to-Peer Session Detail Report in Lync Server 2013](lync-server-2013-peer-to-peer-session-detail-report.md) by clicking the Session detail metric for a peer-to-peer session.</span></span> <span data-ttu-id="e275a-119">Чтобы открыть отчет сведений о конференции, нажмите показатель «Конференция» для конференции.</span><span class="sxs-lookup"><span data-stu-id="e275a-119">You can also access the Conference Detail Report by clicking the Conference metric for a conference.</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-failure-list-report"></a><span data-ttu-id="e275a-120">Рекомендации по использованию отчета Failure List (Список ошибок)</span><span class="sxs-lookup"><span data-stu-id="e275a-120">Making the Best Use of the Failure List Report</span></span>

<span data-ttu-id="e275a-p103">Чтобы просмотреть описание кода ответа или ИД диагностики, наведите указатель мыши на значение. Например, если вы наведете указатель мыши на Diagnostic ID (ИД диагностики) 7 025, то вы увидите следующую всплывающую подсказку:</span><span class="sxs-lookup"><span data-stu-id="e275a-p103">In the Failure List Report, you can view a description for each Response code or each Diagnostic ID simply by holding your mouse over that value. For example, if you hold your mouse over Diagnostic ID 7025 you'll see the following displayed in a tooltip:</span></span>

<span data-ttu-id="e275a-123">Internal server error creating media for user (Внутренняя ошибка сервера при создании среды для пользователя).</span><span class="sxs-lookup"><span data-stu-id="e275a-123">Internal server error creating media for user.</span></span>

<span data-ttu-id="e275a-124">Важно отметить, что отчет по списку ошибок не предоставляет прямой способ получения списка всех пользователей, принимавших участие в хотя бы одном сеансе, закончившемся с ошибкой, или способ определения пользователей, которые наиболее часто участвовали в сеансах, закончившихся с ошибками.</span><span class="sxs-lookup"><span data-stu-id="e275a-124">It's important to note that the Failure List Report does not provide a straightforward way to directly retrieve a list of all the users who participated in at least one failed session, nor does it provide a way to determine which users were most-often involved in a failed session.</span></span> <span data-ttu-id="e275a-125">(В одном случае у отчета "список отказов" нет возможностей фильтрации.) Однако если вы экспортируете данные, а затем преобразуете их в файл с разделителями-запятыми, вы можете использовать Windows PowerShell для поиска ответов на такие вопросы, как, например,.</span><span class="sxs-lookup"><span data-stu-id="e275a-125">(For one thing, the Failure List Report has no filtering capabilities.) However, if you export the data and then convert it to a comma-separated values file, you can use Windows PowerShell to find the answers to questions like those.</span></span> <span data-ttu-id="e275a-126">Например, предположим, что вы сохраняете данные в. CSV-файл с именем C: \\ \\ сбой данных \_List.csv.</span><span class="sxs-lookup"><span data-stu-id="e275a-126">For example, suppose you save the data to a .CSV file named C:\\Data\\Failure\_List.csv.</span></span> <span data-ttu-id="e275a-127">Чтобы получить список пользователей, принимавших участие в хотя бы одном сеансе, закончившемся с ошибкой, используйте следующие команды:</span><span class="sxs-lookup"><span data-stu-id="e275a-127">Based on the data saved in that file, this command lists all the users who were involved in at least one failed session:</span></span>

    $failures = Import-Csv -Path " C:\Data\Failure_List.csv"
    $failure |Sort-Object "From user" | Select-Object "From user" -Unique

<span data-ttu-id="e275a-128">Эти команды возвращают сведения, схожие со следующими:</span><span class="sxs-lookup"><span data-stu-id="e275a-128">That command will return a list similar to this:</span></span>

    From user
    ----
    Pilar.Ackerman@litwareinc.com
    Henrik.Jensen@litwareinc.com
    Gilead.Amosnino@litwareinc.com
    David.Ahs@litwareinc.com
    Ken.Myer@litwareinc.com

<span data-ttu-id="e275a-129">Следующие команды возвращают общее число сеансов каждого пользователя, завершившихся с ошибкой:</span><span class="sxs-lookup"><span data-stu-id="e275a-129">These two commands report back the total number of failed sessions that each user was involved in:</span></span>

    $failures = Import-Csv -Path "C:\Data\Failure_List.csv"
    $failures | Group-Object "From user" | Select-Object Count, Name | Sort-Object -Property Count -Descending

<span data-ttu-id="e275a-130">Эти команды возвращают сведения, схожие со следующими:</span><span class="sxs-lookup"><span data-stu-id="e275a-130">That will return data similar to this:</span></span>

    Count    Name
     -----    ----
        20    Pilar.Ackerman@litwareinc.com
        20    David.Ahs@litwareinc.com
        16    Gilead.Amosnino@litwareinc.com
        16    Ken.Myero@litwareinc.com
        14    Henrik.Jensen@litwareinc.com

</div>

<div>

## <a name="filters"></a><span data-ttu-id="e275a-131">Фильтры</span><span class="sxs-lookup"><span data-stu-id="e275a-131">Filters</span></span>

<span data-ttu-id="e275a-p105">Нет. В отчете Failure List (Список ошибок) нельзя использовать фильтр.</span><span class="sxs-lookup"><span data-stu-id="e275a-p105">None. You cannot filter the Failure List Report.</span></span>

</div>

<div>

## <a name="metrics"></a><span data-ttu-id="e275a-134">Показатели</span><span class="sxs-lookup"><span data-stu-id="e275a-134">Metrics</span></span>

<span data-ttu-id="e275a-135">В следующей таблице приведены сведения, содержащиеся в отчете Failure List (Список ошибок) для каждого звонка, завершившегося с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="e275a-135">The following table lists the information provided in the Failure List Report for each failed call.</span></span>

### <a name="failure-list-report-metrics"></a><span data-ttu-id="e275a-136">Показатели отчета Failure List (Список ошибок)</span><span class="sxs-lookup"><span data-stu-id="e275a-136">Failure List Report Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e275a-137">Имя</span><span class="sxs-lookup"><span data-stu-id="e275a-137">Name</span></span></th>
<th><span data-ttu-id="e275a-138">Поддержка сортировки</span><span class="sxs-lookup"><span data-stu-id="e275a-138">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="e275a-139">Описание</span><span class="sxs-lookup"><span data-stu-id="e275a-139">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e275a-140"><strong>Время создания отчета</strong></span><span class="sxs-lookup"><span data-stu-id="e275a-140"><strong>Reported time</strong></span></span></p></td>
<td><p><span data-ttu-id="e275a-141">Нет</span><span class="sxs-lookup"><span data-stu-id="e275a-141">No</span></span></p></td>
<td><p><span data-ttu-id="e275a-142">Дата и время создания отчета.</span><span class="sxs-lookup"><span data-stu-id="e275a-142">Date and time the report was recorded.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e275a-143"><strong>Запрос</strong></span><span class="sxs-lookup"><span data-stu-id="e275a-143"><strong>Request</strong></span></span></p></td>
<td><p><span data-ttu-id="e275a-144">Нет</span><span class="sxs-lookup"><span data-stu-id="e275a-144">No</span></span></p></td>
<td><p><span data-ttu-id="e275a-p106">Тип запроса SIP, завершившегося с ошибкой. Например, INVITE или BYE.</span><span class="sxs-lookup"><span data-stu-id="e275a-p106">SIP request type that failed. For example, INVITE or BYE.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e275a-147"><strong>Код ответа</strong></span><span class="sxs-lookup"><span data-stu-id="e275a-147"><strong>Response code</strong></span></span></p></td>
<td><p><span data-ttu-id="e275a-148">Нет</span><span class="sxs-lookup"><span data-stu-id="e275a-148">No</span></span></p></td>
<td><p><span data-ttu-id="e275a-149">Код ответа SIP, отправленный при сбое конференции.</span><span class="sxs-lookup"><span data-stu-id="e275a-149">SIP response code sent when the conference failed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e275a-150"><strong>ИД диагностики</strong></span><span class="sxs-lookup"><span data-stu-id="e275a-150"><strong>Diagnostic ID</strong></span></span></p></td>
<td><p><span data-ttu-id="e275a-151">Нет</span><span class="sxs-lookup"><span data-stu-id="e275a-151">No</span></span></p></td>
<td><p><span data-ttu-id="e275a-152">Прикрепленный к SIP-сообщению уникальный идентификатор (в форме заголовка ms-diagnostics), который часто содержит информацию, полезную при поиске и устранении ошибок.</span><span class="sxs-lookup"><span data-stu-id="e275a-152">Unique identifier (in the form of an ms-diagnostics header) attached to a SIP message that often provides information useful in troubleshooting errors.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e275a-153"><strong>Время присоединения (мс)</strong></span><span class="sxs-lookup"><span data-stu-id="e275a-153"><strong>Join cost time (ms)</strong></span></span></p></td>
<td><p><span data-ttu-id="e275a-154">Нет</span><span class="sxs-lookup"><span data-stu-id="e275a-154">No</span></span></p></td>
<td><p><span data-ttu-id="e275a-155">Период времени (в миллисекундах), требуемый для присоединения пользователя к конференции.</span><span class="sxs-lookup"><span data-stu-id="e275a-155">Amount of time (in milliseconds) required for the user to join the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e275a-156"><strong>Пользователь-отправитель</strong></span><span class="sxs-lookup"><span data-stu-id="e275a-156"><strong>From user</strong></span></span></p></td>
<td><p><span data-ttu-id="e275a-157">Нет</span><span class="sxs-lookup"><span data-stu-id="e275a-157">No</span></span></p></td>
<td><p><span data-ttu-id="e275a-158">SIP-адрес пользователя, инициировавшего вызов.</span><span class="sxs-lookup"><span data-stu-id="e275a-158">SIP address of the user who initiated the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e275a-159"><strong>Агент пользователя, инициатора сеанса</strong></span><span class="sxs-lookup"><span data-stu-id="e275a-159"><strong>From user agent</strong></span></span></p></td>
<td><p><span data-ttu-id="e275a-160">Нет</span><span class="sxs-lookup"><span data-stu-id="e275a-160">No</span></span></p></td>
<td><p><span data-ttu-id="e275a-161">Программное обеспечение, используемое конечной точкой пользователя, инициировавшего звонок.</span><span class="sxs-lookup"><span data-stu-id="e275a-161">Software used by the endpoint of the user who initiated the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e275a-162"><strong>Пользователь-получатель</strong></span><span class="sxs-lookup"><span data-stu-id="e275a-162"><strong>To user</strong></span></span></p></td>
<td><p><span data-ttu-id="e275a-163">Нет</span><span class="sxs-lookup"><span data-stu-id="e275a-163">No</span></span></p></td>
<td><p><span data-ttu-id="e275a-164">SIP-адрес пользователя, принявшего звонок.</span><span class="sxs-lookup"><span data-stu-id="e275a-164">SIP address of the user who was being called.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="e275a-165">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e275a-165">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

