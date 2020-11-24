---
title: 'Lync Server 2013: подробный отчет о Конференции'
description: 'Lync Server 2013: подробный отчет о Конференции.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Conference Detail Report
ms:assetid: 1d61cd81-dcfe-40b4-9a41-a73b038bc216
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204728(v=OCS.15)
ms:contentKeyID: 48183565
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 07c50b545f4a9ee3308a840fc2aa5a15e617a5bd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398518"
---
# <a name="conference-detail-report-in-lync-server-2013"></a><span data-ttu-id="37ad8-103">Подробный отчет о конференции в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="37ad8-103">Conference Detail Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="37ad8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="37ad8-104">

<span> </span></span></span>

<span data-ttu-id="37ad8-105">_**Тема последнего изменения:** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="37ad8-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="37ad8-p101">Подробный отчет по конференции содержит подробную информацию обо всех пользователях, принимавших участие в конференции. Например, вы можете просматривать такую информацию, как дата и время присоединения пользователя к конференции, дата и время покидания конференции, а также агент пользователя конечной точки, использованный для подключения этого пользователя к конференции. Вы также можете просмотреть информацию о роли пользователя в каждой конференции (например, выступающий или участник). Возможно, еще важнее то, что вы можете быстро просмотреть, какие пользователи успешно присоединились к конференции и участвовали в ней и какие пользователи не смогли этого сделать.</span><span class="sxs-lookup"><span data-stu-id="37ad8-p101">The Conference Detail Report provides detailed information about all the users who participated in a conference. For example, you can see such information as the date and time that a user joined the conference, the date and time that the user left the conference, and the user agent of the endpoint that was used to connect that user to the conference. You can also see information the user's role in each conference (for example, Presenter or Attendee). Perhaps most important, you get quickly see which users successfully join and complete the conference, and which users were not able to successfully join and complete the conference.</span></span>

<div>

## <a name="accessing-the-conference-detail-report"></a><span data-ttu-id="37ad8-110">Доступ к подробному отчету по конференции</span><span class="sxs-lookup"><span data-stu-id="37ad8-110">Accessing the Conference Detail Report</span></span>

<span data-ttu-id="37ad8-111">Подробный отчет по конференции можно открыть из следующих отчетов:</span><span class="sxs-lookup"><span data-stu-id="37ad8-111">The Conference Detail Report can be accessed from the following reports:</span></span>

  - <span data-ttu-id="37ad8-112">[Отчет по контролю за допуском звонков в Lync Server 2013](lync-server-2013-call-admission-control-report.md) (с помощью которого можно выбрать детальную метрику конференции)</span><span class="sxs-lookup"><span data-stu-id="37ad8-112">The [Call Admission Control Report in Lync Server 2013](lync-server-2013-call-admission-control-report.md) (by clicking the Detail metric for a conference)</span></span>

  - <span data-ttu-id="37ad8-113">[Отчет о списке отказов в Lync Server 2013](lync-server-2013-failure-list-report.md) (щелчок метрики конференции)</span><span class="sxs-lookup"><span data-stu-id="37ad8-113">The [Failure List Report in Lync Server 2013](lync-server-2013-failure-list-report.md) (by clicking the Conference metric)</span></span>

  - <span data-ttu-id="37ad8-114">[Отчет о действиях пользователей в Lync Server 2013](lync-server-2013-user-activity-report.md) (щелчок метрики URI конференции)</span><span class="sxs-lookup"><span data-stu-id="37ad8-114">The [User Activity Report in Lync Server 2013](lync-server-2013-user-activity-report.md) (by clicking the Conference URI metric)</span></span>

<span data-ttu-id="37ad8-115">В отчете сведения о конференции вы можете получить доступ к [отчету о диагностике в Lync Server 2013](lync-server-2013-diagnostic-report.md) , щелкнув метрику диагностического отчета (подробности).</span><span class="sxs-lookup"><span data-stu-id="37ad8-115">From the Conference Detail Report you can access the [Diagnostic Report in Lync Server 2013](lync-server-2013-diagnostic-report.md) by clicking the Diagnostic Report (Detail) metric.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="37ad8-116">Фильтры</span><span class="sxs-lookup"><span data-stu-id="37ad8-116">Filters</span></span>

<span data-ttu-id="37ad8-p102">Нет. Вы не можете фильтровать подробный отчет по конференции.</span><span class="sxs-lookup"><span data-stu-id="37ad8-p102">None. You cannot filter on the Conference Detail Report.</span></span>

</div>

<div>

## <a name="metrics"></a><span data-ttu-id="37ad8-119">Показатели</span><span class="sxs-lookup"><span data-stu-id="37ad8-119">Metrics</span></span>

<span data-ttu-id="37ad8-120">В следующей таблице приведены сведения из раздела информации о конференции, входящего в подробный отчет по конференции.</span><span class="sxs-lookup"><span data-stu-id="37ad8-120">The following table lists the information provided in the Conference Information section of the Conference Detail Report.</span></span>

### <a name="conference-information-metrics"></a><span data-ttu-id="37ad8-121">Метрики информации о конференции</span><span class="sxs-lookup"><span data-stu-id="37ad8-121">Conference Information Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="37ad8-122">Имя</span><span class="sxs-lookup"><span data-stu-id="37ad8-122">Name</span></span></th>
<th><span data-ttu-id="37ad8-123">Поддержка сортировки</span><span class="sxs-lookup"><span data-stu-id="37ad8-123">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="37ad8-124">Описание</span><span class="sxs-lookup"><span data-stu-id="37ad8-124">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="37ad8-125"><strong>Идентификатор URI конференции</strong></span><span class="sxs-lookup"><span data-stu-id="37ad8-125"><strong>Conference URI</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="37ad8-p103">URI, назначенный конференции. Например:</span><span class="sxs-lookup"><span data-stu-id="37ad8-p103">URI assigned to the conference. For example:</span></span></p>
<p><span data-ttu-id="37ad8-128">sip:kmyer@litwareinc.com;gruu;opaque=app:conf:focus:id:drg2y8v4</span><span class="sxs-lookup"><span data-stu-id="37ad8-128">sip:kmyer@litwareinc.com;gruu;opaque=app:conf:focus:id:drg2y8v4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37ad8-129"><strong>Полное доменное имя пула</strong></span><span class="sxs-lookup"><span data-stu-id="37ad8-129"><strong>Pool FQDN</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="37ad8-130">Полное доменное имя пула Регистратора или участвующего в сеансе пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="37ad8-130">Fully-qualified domain name of the Registrar pool or Edge Server involved in a session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37ad8-131"><strong>Время начала</strong></span><span class="sxs-lookup"><span data-stu-id="37ad8-131"><strong>Start time</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="37ad8-132">Дата и время начала конференции.</span><span class="sxs-lookup"><span data-stu-id="37ad8-132">Date and time that the conference started.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37ad8-133"><strong>Организатор</strong></span><span class="sxs-lookup"><span data-stu-id="37ad8-133"><strong>Organizer</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="37ad8-134">SIP-адрес пользователя, организовавшего конференцию.</span><span class="sxs-lookup"><span data-stu-id="37ad8-134">SIP address of the user who organized the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37ad8-135"><strong>Время окончания</strong></span><span class="sxs-lookup"><span data-stu-id="37ad8-135"><strong>End time</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="37ad8-136">Дата и время завершения конференции.</span><span class="sxs-lookup"><span data-stu-id="37ad8-136">Date and time that the conference ended.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="37ad8-137">В следующей таблице приведены сведения из раздела участия в конференции, входящего в подробный отчет по конференции.</span><span class="sxs-lookup"><span data-stu-id="37ad8-137">The following table lists the information provided in the Conference Participation Section of the Conference Detail Report.</span></span>

### <a name="conference-participation-metrics"></a><span data-ttu-id="37ad8-138">Метрики участия в конференции</span><span class="sxs-lookup"><span data-stu-id="37ad8-138">Conference Participation Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="37ad8-139">Имя</span><span class="sxs-lookup"><span data-stu-id="37ad8-139">Name</span></span></th>
<th><span data-ttu-id="37ad8-140">Поддержка сортировки</span><span class="sxs-lookup"><span data-stu-id="37ad8-140">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="37ad8-141">Описание</span><span class="sxs-lookup"><span data-stu-id="37ad8-141">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="37ad8-142"><strong>Пользователь</strong></span><span class="sxs-lookup"><span data-stu-id="37ad8-142"><strong>User</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="37ad8-143">SIP-адрес пользователя, участвовавшего в конференции.</span><span class="sxs-lookup"><span data-stu-id="37ad8-143">SIP address of the user who participated in the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37ad8-144"><strong>Роль</strong></span><span class="sxs-lookup"><span data-stu-id="37ad8-144"><strong>Role</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="37ad8-145">Роль (например, докладчик), которую играл участник конференции.</span><span class="sxs-lookup"><span data-stu-id="37ad8-145">Role (for example, Presenter) played by the conference participant.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37ad8-146"><strong>Подключение</strong></span><span class="sxs-lookup"><span data-stu-id="37ad8-146"><strong>Connectivity</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="37ad8-147">Подключение участника к сети, обычно из внутренней сети или из внешней сети.</span><span class="sxs-lookup"><span data-stu-id="37ad8-147">Network connectivity (typically From Internal or From External) for the participant.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37ad8-148">Время присоединения</span><span class="sxs-lookup"><span data-stu-id="37ad8-148">Join time</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="37ad8-149">Дата и время присоединения участника к конференции.</span><span class="sxs-lookup"><span data-stu-id="37ad8-149">Date and time that the participant joined the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37ad8-150"><strong>Время ухода</strong></span><span class="sxs-lookup"><span data-stu-id="37ad8-150"><strong>Leave time</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="37ad8-151">Дата и время, когда участник покинул конференцию.</span><span class="sxs-lookup"><span data-stu-id="37ad8-151">Date and time that the participant left the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37ad8-152"><strong>Агент пользователя</strong></span><span class="sxs-lookup"><span data-stu-id="37ad8-152"><strong>User agent</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="37ad8-153">Идентификатор для программного обеспечения, используемого конечной точкой участника.</span><span class="sxs-lookup"><span data-stu-id="37ad8-153">Identifier for the software used by the participant’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37ad8-154"><strong>Диагностический отчет</strong></span><span class="sxs-lookup"><span data-stu-id="37ad8-154"><strong>Diagnostic reports</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="37ad8-p104">Предоставляет сведения о диагностике и о поиске и устранении неполадок, включая коды отклика SIP, диагностические заголовки, значения времени присоединения к конференции и диагностические идентификаторы для неудачных сеансов.</span><span class="sxs-lookup"><span data-stu-id="37ad8-p104">Provides diagnostic and troubleshooting information. Including SIP response codes, diagnostic headers, conference join times, and diagnostic IDs for failed sessions.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="37ad8-157">В таблице ниже приведены сведения, указанные в разделе Conference модальностей в отчете "сведения о конференции".</span><span class="sxs-lookup"><span data-stu-id="37ad8-157">The following table lists the information provided in the Conference Modalities section of the Conference Detail Report.</span></span>

### <a name="conference-modalities-metrics"></a><span data-ttu-id="37ad8-158">Метрики модальностей конференции</span><span class="sxs-lookup"><span data-stu-id="37ad8-158">Conference Modalities Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="37ad8-159">Имя</span><span class="sxs-lookup"><span data-stu-id="37ad8-159">Name</span></span></th>
<th><span data-ttu-id="37ad8-160">Поддержка сортировки</span><span class="sxs-lookup"><span data-stu-id="37ad8-160">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="37ad8-161">Описание</span><span class="sxs-lookup"><span data-stu-id="37ad8-161">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="37ad8-162"><strong>Пользователь</strong></span><span class="sxs-lookup"><span data-stu-id="37ad8-162"><strong>User</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="37ad8-163">SIP-адрес пользователя, участвовавшего в конференции.</span><span class="sxs-lookup"><span data-stu-id="37ad8-163">SIP address of the user who participated in the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37ad8-164"><strong>Время присоединения</strong></span><span class="sxs-lookup"><span data-stu-id="37ad8-164"><strong>Join time</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="37ad8-165">Дата и время присоединения участника к конференции.</span><span class="sxs-lookup"><span data-stu-id="37ad8-165">Date and time that the participant joined the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37ad8-166"><strong>Время ухода</strong></span><span class="sxs-lookup"><span data-stu-id="37ad8-166"><strong>Leave time</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="37ad8-167">Дата и время покидания участником конференции.</span><span class="sxs-lookup"><span data-stu-id="37ad8-167">Date and time that a participant left the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37ad8-168"><strong>URI сервера конференций</strong></span><span class="sxs-lookup"><span data-stu-id="37ad8-168"><strong>Conferencing server URI</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="37ad8-169">URI для используемого в конференции сервера конференций.</span><span class="sxs-lookup"><span data-stu-id="37ad8-169">URI for the Conferencing server used in the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37ad8-170"><strong>Диагностический отчет</strong></span><span class="sxs-lookup"><span data-stu-id="37ad8-170"><strong>Diagnostic reports</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="37ad8-p105">Предоставляет сведения о диагностике и о поиске и устранении неполадок, включая коды отклика SIP, диагностические заголовки, значения времени присоединения к конференции и диагностические идентификаторы для неудачных сеансов.</span><span class="sxs-lookup"><span data-stu-id="37ad8-p105">Provides diagnostic and troubleshooting information. Including SIP response codes, diagnostic headers, conference join times, and diagnostic IDs for failed sessions.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="37ad8-173">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="37ad8-173">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

