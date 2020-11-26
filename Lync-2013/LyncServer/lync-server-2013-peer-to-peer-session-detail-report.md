---
title: 'Lync Server 2013: одноранговый отчет о сеансе'
description: 'Lync Server 2013: одноранговый отчет о сеансе.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Peer-to-Peer Session Detail Report
ms:assetid: 6be1d676-68f7-4a53-a72a-de73296c5571
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558659(v=OCS.15)
ms:contentKeyID: 48184416
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e712225fddabb646cc3b862f59601857a7df8eff
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445038"
---
# <a name="peer-to-peer-session-detail-report-in-lync-server-2013"></a><span data-ttu-id="94949-103">Отчет о одноранговых сеансах в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="94949-103">Peer-to-Peer Session Detail Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="94949-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="94949-104">

<span> </span></span></span>

<span data-ttu-id="94949-105">_**Тема последнего изменения:** 2012-06-06_</span><span class="sxs-lookup"><span data-stu-id="94949-105">_**Topic Last Modified:** 2012-06-06_</span></span>

<span data-ttu-id="94949-p101">Отчет по деталям однорангового сеанса (Peer-to-Peer Session Detail Report) предоставляет подробные сведения об одноранговом сеансе. Например, если выбрать сеанс обмена мгновенными сообщениями, то отчет предоставит сведения о количестве сообщений, отправленных в этом сеансе каждым из двух пользователей.</span><span class="sxs-lookup"><span data-stu-id="94949-p101">The Peer-to-Peer Session Detail Report returns detailed information about a peer-to-peer session. For example, if you select an instant messaging session, the report will tell you the number of messages sent by each of the two users in the session.</span></span>

<div>

## <a name="accessing-the-peer-to-peer-session-detail-report"></a><span data-ttu-id="94949-108">Доступ к отчету по деталям однорангового сеанса</span><span class="sxs-lookup"><span data-stu-id="94949-108">Accessing the Peer-to-Peer Session Detail Report</span></span>

<span data-ttu-id="94949-109">Отчет по деталям однорангового сеанса можно вызвать в любом из следующих отчетов (все они доступны на домашней странице отчетов мониторинга).</span><span class="sxs-lookup"><span data-stu-id="94949-109">The Peer-to-Peer Session Detail Report can be accessed from any of the following reports (all of which can be accessed from the Monitoring Reports home page):</span></span>

  - <span data-ttu-id="94949-110">Отчет по инвентарю IP-телефонов</span><span class="sxs-lookup"><span data-stu-id="94949-110">IP Phone Inventory Report</span></span>

  - <span data-ttu-id="94949-111">Отчет по активности пользователей</span><span class="sxs-lookup"><span data-stu-id="94949-111">User Activity Report</span></span>

  - <span data-ttu-id="94949-112">Отчет по контролю допуска звонков</span><span class="sxs-lookup"><span data-stu-id="94949-112">Call Admission Control Report</span></span>

  - <span data-ttu-id="94949-113">Отчет по списку отказов</span><span class="sxs-lookup"><span data-stu-id="94949-113">Failure List Report</span></span>

<span data-ttu-id="94949-114">В отчете сведения о одноранговых сеансах вы можете получить доступ к [отчету диагностики в Lync Server 2013](lync-server-2013-diagnostic-report.md) , щелкнув метрику диагностического отчета (подробности).</span><span class="sxs-lookup"><span data-stu-id="94949-114">From within the Peer-to-Peer Session Detail Report you can access the [Diagnostic Report in Lync Server 2013](lync-server-2013-diagnostic-report.md) by clicking the Diagnostic Report (Details) metric.</span></span> <span data-ttu-id="94949-115">Можно также вызвать отчет по основным сбоям (Top Failures Report), щелкнув одну из следующих метрик:</span><span class="sxs-lookup"><span data-stu-id="94949-115">You can also access the Top Failures Report by clicking either of these two metrics:</span></span>

  - <span data-ttu-id="94949-116">Response (Ответ)</span><span class="sxs-lookup"><span data-stu-id="94949-116">Response</span></span>

  - <span data-ttu-id="94949-117">Diagnostic ID (ИД диагностики)</span><span class="sxs-lookup"><span data-stu-id="94949-117">Diagnostic ID</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-peer-to-peer-session-detail-report"></a><span data-ttu-id="94949-118">Оптимальное использование отчета по деталям однорангового сеанса</span><span class="sxs-lookup"><span data-stu-id="94949-118">Making the Best Use of the Peer-to-Peer session Detail Report</span></span>

<span data-ttu-id="94949-p103">В отчете по деталям однорангового сеанса имеется большое количество метрик, многие из которых могут быть незнакомы системным администраторам. Однако во многих случаях при наведении указателя мыши на метку метрики отображаются всплывающие подсказки, дающие краткое описание этой метрики.</span><span class="sxs-lookup"><span data-stu-id="94949-p103">The Peer-to-Peer Session Detail Report includes a large number of metrics, many of which might not be familiar to system administrators. Often-times, however, you can view a tooltip that offers a brief description of that metric simply by holding your mouse over the metric label.</span></span>

<span data-ttu-id="94949-p104">Следует отметить, что фактические метрики, которые отображаются в конкретном отчете, будут зависеть от типа выбранного однорангового сеанса. Для сеанса аудио- или видеосвязи и для сеанса обмена мгновенными сообщениями будут отображаться разные наборы метрик.</span><span class="sxs-lookup"><span data-stu-id="94949-p104">Note that the actual metrics shown on a given report will depend on the type of peer-to-peer session you selected. An audio/video session will report a different set of metrics than an instant messaging session.</span></span>

<span data-ttu-id="94949-123">Кроме того, поместив указатель мыши на метрику Response code (Код ответа) или Diagnostic ID (ИД диагностики), можно получить описание следующих значений.</span><span class="sxs-lookup"><span data-stu-id="94949-123">You can also hold your mouse over the Response code and Diagnostic ID metrics in order to obtain a description of those values:</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="94949-124">Фильтры</span><span class="sxs-lookup"><span data-stu-id="94949-124">Filters</span></span>

<span data-ttu-id="94949-p105">Фильтры отсутствуют. Фильтрация отчета по деталям однорангового сеанса не предусмотрена.</span><span class="sxs-lookup"><span data-stu-id="94949-p105">None. You cannot filter the Peer-to-Peer Session Detail Report.</span></span>

</div>

<div>

## <a name="session-information-metrics"></a><span data-ttu-id="94949-127">Метрики сведений о сеансе</span><span class="sxs-lookup"><span data-stu-id="94949-127">Session Information Metrics</span></span>

<span data-ttu-id="94949-128">В следующей таблице приведены сведения, которые предоставляются отчетом по деталям однорангового сеанса для каждого сеанса.</span><span class="sxs-lookup"><span data-stu-id="94949-128">The following table lists the information provided in the Peer-to-Peer Session Detail Report for each session.</span></span>

### <a name="session-information-metrics"></a><span data-ttu-id="94949-129">Метрики сведений о сеансе</span><span class="sxs-lookup"><span data-stu-id="94949-129">Session Information Metrics</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="94949-130">Имя</span><span class="sxs-lookup"><span data-stu-id="94949-130">Name</span></span></th>
<th><span data-ttu-id="94949-131">Описание</span><span class="sxs-lookup"><span data-stu-id="94949-131">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="94949-132"><strong>Полное доменное имя пула</strong></span><span class="sxs-lookup"><span data-stu-id="94949-132"><strong>Pool FQDN</strong></span></span></p></td>
<td><p><span data-ttu-id="94949-133">Полное доменное имя пула регистратора или пограничного сервера, участвующего в сеансе.</span><span class="sxs-lookup"><span data-stu-id="94949-133">Fully qualified domain name (FQDN) of the Registrar pool or Edge Server involved in the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94949-134"><strong>Invite time (Время приглашения)</strong></span><span class="sxs-lookup"><span data-stu-id="94949-134"><strong>Invite time</strong></span></span></p></td>
<td><p><span data-ttu-id="94949-135">Дата и время, когда было отправлено приглашение принять участие в сеансе.</span><span class="sxs-lookup"><span data-stu-id="94949-135">Date and time the session invitation was originally sent.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94949-136"><strong>Response time (Время ответа)</strong></span><span class="sxs-lookup"><span data-stu-id="94949-136"><strong>Response time</strong></span></span></p></td>
<td><p><span data-ttu-id="94949-137">Дата и время, когда было получено принятие приглашения.</span><span class="sxs-lookup"><span data-stu-id="94949-137">Date and time that the invitation acceptance was received.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94949-138"><strong>From user (Пользователь-отправитель)</strong></span><span class="sxs-lookup"><span data-stu-id="94949-138"><strong>From user</strong></span></span></p></td>
<td><p><span data-ttu-id="94949-139">SIP-адрес пользователя, инициировавшего сеанс.</span><span class="sxs-lookup"><span data-stu-id="94949-139">SIP address of the user who initiated the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94949-140"><strong>From user agent (Агент пользователя, инициатора сеанса)</strong></span><span class="sxs-lookup"><span data-stu-id="94949-140"><strong>From user agent</strong></span></span></p></td>
<td><p><span data-ttu-id="94949-141">Программное обеспечение, используемое конечной точкой пользователя, инициировавшего сеанс.</span><span class="sxs-lookup"><span data-stu-id="94949-141">Software used by the endpoint of the user who initiated the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94949-142"><strong>Is From user internal (Пользователь-инициатор внутренний?)</strong></span><span class="sxs-lookup"><span data-stu-id="94949-142"><strong>Is From user internal</strong></span></span></p></td>
<td><p><span data-ttu-id="94949-143">Указывает, вошел ли пользователь, начавший сеанс, во внутреннюю сеть.</span><span class="sxs-lookup"><span data-stu-id="94949-143">Indicates whether the user who initiated the session was logged on to the internal network.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94949-144"><strong>Is From user integrated with desk phone (Пользователь-инициатор интегрирован со стационарным телефоном?)</strong></span><span class="sxs-lookup"><span data-stu-id="94949-144"><strong>Is From user integrated with desk phone</strong></span></span></p></td>
<td><p><span data-ttu-id="94949-145">Указывает, интегрирована ли конечная точка пользователя, начавшего сеанс, с его стационарным телефоном.</span><span class="sxs-lookup"><span data-stu-id="94949-145">Indicates whether the endpoint used by the user who initiated the session is integrated with his or her desktop phone.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94949-146"><strong>Session Priority (Приоритет сеанса)</strong></span><span class="sxs-lookup"><span data-stu-id="94949-146"><strong>Session Priority</strong></span></span></p></td>
<td><p><span data-ttu-id="94949-p106">Приоритет, назначенный сеансу. Возможные приоритеты: Unknown (Неизвестно); Non-Urgent (Несрочный); Normal (Обычный); Urgent (Срочный) и Emergency (Экстренный).</span><span class="sxs-lookup"><span data-stu-id="94949-p106">Priority assigned to the session. Valid priorities are: Unknown; Non-Urgent; Normal; Urgent; and Emergency.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94949-149"><strong>Response code (Код ответа)</strong></span><span class="sxs-lookup"><span data-stu-id="94949-149"><strong>Response code</strong></span></span></p></td>
<td><p><span data-ttu-id="94949-150">Код ответа SIP, отправленный при сбое сеанса.</span><span class="sxs-lookup"><span data-stu-id="94949-150">SIP response code sent when the session failed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94949-151"><strong>Front end (Сервер переднего плана)</strong></span><span class="sxs-lookup"><span data-stu-id="94949-151"><strong>Front end</strong></span></span></p></td>
<td><p><span data-ttu-id="94949-152">Имя сервера переднего плана, использовавшегося в конференции.</span><span class="sxs-lookup"><span data-stu-id="94949-152">Name of the Front End Server used in the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94949-153"><strong>Capture time (Время регистрации)</strong></span><span class="sxs-lookup"><span data-stu-id="94949-153"><strong>Capture time</strong></span></span></p></td>
<td><p><span data-ttu-id="94949-154">Дата и время регистрации сведений о сеансе.</span><span class="sxs-lookup"><span data-stu-id="94949-154">Date and time that the session information was recorded.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94949-155"><strong>End time (Время окончания)</strong></span><span class="sxs-lookup"><span data-stu-id="94949-155"><strong>End time</strong></span></span></p></td>
<td><p><span data-ttu-id="94949-156">Дата и время окончания сеанса.</span><span class="sxs-lookup"><span data-stu-id="94949-156">Date and time the session ended.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94949-157"><strong>To user (Пользователь-получатель)</strong></span><span class="sxs-lookup"><span data-stu-id="94949-157"><strong>To user</strong></span></span></p></td>
<td><p><span data-ttu-id="94949-158">SIP-адрес пользователя, получившего приглашение к сеансу.</span><span class="sxs-lookup"><span data-stu-id="94949-158">SIP address of the user who was invited to the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94949-159"><strong>To user agent (Агент пользователя-получателя)</strong></span><span class="sxs-lookup"><span data-stu-id="94949-159"><strong>To user agent</strong></span></span></p></td>
<td><p><span data-ttu-id="94949-160">Программное обеспечение, использовавшееся конечной точкой пользователя, приглашенного принять участие в сеансе.</span><span class="sxs-lookup"><span data-stu-id="94949-160">Software used by the endpoint of the user who was invited to the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94949-161"><strong>Is To user internal (Пользователь-получатель внутренний?)</strong></span><span class="sxs-lookup"><span data-stu-id="94949-161"><strong>Is To user internal</strong></span></span></p></td>
<td><p><span data-ttu-id="94949-162">Указывает, вошел ли пользователь, приглашенный принять участие в сеансе, во внутреннюю сеть.</span><span class="sxs-lookup"><span data-stu-id="94949-162">Indicates whether the user who was invited to the session was logged on to the internal network.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94949-163"><strong>Is To user integrated with desk phone (Пользователь-получатель интегрирован со стационарным телефоном?)</strong></span><span class="sxs-lookup"><span data-stu-id="94949-163"><strong>Is To user integrated with desk phone</strong></span></span></p></td>
<td><p><span data-ttu-id="94949-164">Указывает, интегрирована ли конечная точка пользователя, приглашенного принять участие в сеансе, с его стационарным телефоном.</span><span class="sxs-lookup"><span data-stu-id="94949-164">Indicates whether the endpoint used by the user who was invited to the session is integrated with his or her desktop phone.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94949-165"><strong>Is retried session (Повторный сеанс?)</strong></span><span class="sxs-lookup"><span data-stu-id="94949-165"><strong>Is retried session</strong></span></span></p></td>
<td><p><span data-ttu-id="94949-166">Указывает, являлся ли этот сеанс попыткой повтора сеанса, который завершился неудачно.</span><span class="sxs-lookup"><span data-stu-id="94949-166">Indicates whether the session is an attempt to retry a session that previously failed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94949-167"><strong>Diagnostic ID (ИД диагностики)</strong></span><span class="sxs-lookup"><span data-stu-id="94949-167"><strong>Diagnostic ID</strong></span></span></p></td>
<td><p><span data-ttu-id="94949-p107">Уникальный идентификатор (в форме заголовка ms-diagnostics), присоединенный к сообщению SIP, который часто содержит сведения, помогающий устранять ошибки. Поместите указатель мыши на этот идентификатор, чтобы увидеть дополнительные сведения о нем.</span><span class="sxs-lookup"><span data-stu-id="94949-p107">Unique identifier (in the form of an ms-diagnostics header) attached to a SIP message that often provides information useful in troubleshooting errors. Hold the mouse over the ID number to view additional information about that ID.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-modalities"></a><span data-ttu-id="94949-170">Метрики для модальностей</span><span class="sxs-lookup"><span data-stu-id="94949-170">Metrics for Modalities</span></span>

<span data-ttu-id="94949-171">В следующей таблице приведены сведения, которые предоставляются отчетом по деталям однорангового сеанса для всех модальностей сеанса.</span><span class="sxs-lookup"><span data-stu-id="94949-171">The following table lists the information provided in the Peer-to-Peer Session Detail Report for each session modality.</span></span>

### <a name="metrics-for-modalities"></a><span data-ttu-id="94949-172">Метрики для модальностей</span><span class="sxs-lookup"><span data-stu-id="94949-172">Metrics for Modalities</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="94949-173">Имя</span><span class="sxs-lookup"><span data-stu-id="94949-173">Name</span></span></th>
<th><span data-ttu-id="94949-174">Поддержка сортировки</span><span class="sxs-lookup"><span data-stu-id="94949-174">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="94949-175">Описание</span><span class="sxs-lookup"><span data-stu-id="94949-175">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="94949-176"><strong>Modalities (Модальности)</strong></span><span class="sxs-lookup"><span data-stu-id="94949-176"><strong>Modalities</strong></span></span></p></td>
<td><p><span data-ttu-id="94949-177">Нет</span><span class="sxs-lookup"><span data-stu-id="94949-177">No</span></span></p></td>
<td><p><span data-ttu-id="94949-p108">Модальности, использованные в сеансе, например, обмен мгновенными сообщениями или передача файла.</span><span class="sxs-lookup"><span data-stu-id="94949-p108">Modalities used in the session. For example, instant messaging (IM) or file transfer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94949-180"><strong>From user messages (Сообщения пользователя-инициатора)</strong></span><span class="sxs-lookup"><span data-stu-id="94949-180"><strong>From user messages</strong></span></span></p></td>
<td><p><span data-ttu-id="94949-181">Нет</span><span class="sxs-lookup"><span data-stu-id="94949-181">No</span></span></p></td>
<td><p><span data-ttu-id="94949-182">Количество сообщений, отправленных пользователем, начавшим сеанс.</span><span class="sxs-lookup"><span data-stu-id="94949-182">Number of messages sent by the user who initiated the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94949-183"><strong>To user messages (Сообщения пользователя-получателя)</strong></span><span class="sxs-lookup"><span data-stu-id="94949-183"><strong>To user messages</strong></span></span></p></td>
<td><p><span data-ttu-id="94949-184">Нет</span><span class="sxs-lookup"><span data-stu-id="94949-184">No</span></span></p></td>
<td><p><span data-ttu-id="94949-185">Количество сообщений, отправленных пользователем, приглашенным принять участие в сеансе.</span><span class="sxs-lookup"><span data-stu-id="94949-185">Number of messages sent by the user who was invited to join the session.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-diagnostic-reports"></a><span data-ttu-id="94949-186">Метрики для диагностических отчетов</span><span class="sxs-lookup"><span data-stu-id="94949-186">Metrics for Diagnostic Reports</span></span>

<span data-ttu-id="94949-187">В следующей таблице приведены сведения, которые отчет по деталям однорангового сеанса предоставляет для каждого диагностического отчета.</span><span class="sxs-lookup"><span data-stu-id="94949-187">The following table lists the information provided in the Peer-to-Peer Session Detail Report for each diagnostic report.</span></span>

### <a name="metrics-for-diagnostic-reports"></a><span data-ttu-id="94949-188">Метрики для диагностических отчетов</span><span class="sxs-lookup"><span data-stu-id="94949-188">Metrics for Diagnostic Reports</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="94949-189">Имя</span><span class="sxs-lookup"><span data-stu-id="94949-189">Name</span></span></th>
<th><span data-ttu-id="94949-190">Поддержка сортировки</span><span class="sxs-lookup"><span data-stu-id="94949-190">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="94949-191">Описание</span><span class="sxs-lookup"><span data-stu-id="94949-191">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="94949-192"><strong>Подробности</strong></span><span class="sxs-lookup"><span data-stu-id="94949-192"><strong>Detail</strong></span></span></p></td>
<td><p><span data-ttu-id="94949-193">Нет</span><span class="sxs-lookup"><span data-stu-id="94949-193">No</span></span></p></td>
<td><p><span data-ttu-id="94949-194">При нажатии этой метрики отображается диагностический отчет для данного сеанса.</span><span class="sxs-lookup"><span data-stu-id="94949-194">When you click this item, the report shows the Diagnostic Report for the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94949-195"><strong>Reported time (Время создания отчета)</strong></span><span class="sxs-lookup"><span data-stu-id="94949-195"><strong>Report time</strong></span></span></p></td>
<td><p><span data-ttu-id="94949-196">Нет</span><span class="sxs-lookup"><span data-stu-id="94949-196">No</span></span></p></td>
<td><p><span data-ttu-id="94949-197">Дата и время создания отчета.</span><span class="sxs-lookup"><span data-stu-id="94949-197">Date and time the report was recorded.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94949-198"><strong>Запрос</strong></span><span class="sxs-lookup"><span data-stu-id="94949-198"><strong>Request</strong></span></span></p></td>
<td><p><span data-ttu-id="94949-199">Нет</span><span class="sxs-lookup"><span data-stu-id="94949-199">No</span></span></p></td>
<td><p><span data-ttu-id="94949-p109">SIP-тип запроса. Например, INVITE или BYE.</span><span class="sxs-lookup"><span data-stu-id="94949-p109">SIP request type. For example, INVITE or BYE.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94949-202"><strong>Diagnostic ID (ИД диагностики)</strong></span><span class="sxs-lookup"><span data-stu-id="94949-202"><strong>Diagnostic ID</strong></span></span></p></td>
<td><p><span data-ttu-id="94949-203">Нет</span><span class="sxs-lookup"><span data-stu-id="94949-203">No</span></span></p></td>
<td><p><span data-ttu-id="94949-204">Прикрепленный к SIP-сообщению уникальный идентификатор (в форме заголовка ms-diagnostics), который часто содержит информацию, полезную при поиске и устранении ошибок.</span><span class="sxs-lookup"><span data-stu-id="94949-204">Unique identifier (in the form of an ms-diagnostics header) attached to a SIP message that often provides information useful in troubleshooting errors.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94949-205"><strong>Тип содержимого</strong></span><span class="sxs-lookup"><span data-stu-id="94949-205"><strong>Content type</strong></span></span></p></td>
<td><p><span data-ttu-id="94949-206">Нет</span><span class="sxs-lookup"><span data-stu-id="94949-206">No</span></span></p></td>
<td><p><span data-ttu-id="94949-p110">Тип контента мультимедиа, использовавшегося в конференции. Например, распространенным типом контента является Application/sdp. Протокол SDP – это стандартный Интернет-протокол, используемый для объявления о сеансе, приглашения принять участие в сеансе и других форм инициации сеанса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="94949-p110">Type of media content used in the conference. For example, a common content type is Application/sdp. Session Description Protocol (SDP) is a standard Internet protocol used for session announcements, session invitations, and other forms of multimedia session initiation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94949-210"><strong>Reported by (Сообщил)</strong></span><span class="sxs-lookup"><span data-stu-id="94949-210"><strong>Reported by</strong></span></span></p></td>
<td><p><span data-ttu-id="94949-211">Нет</span><span class="sxs-lookup"><span data-stu-id="94949-211">No</span></span></p></td>
<td><p><span data-ttu-id="94949-212">Компьютер (клиент или сервер), который сообщил о проблеме.</span><span class="sxs-lookup"><span data-stu-id="94949-212">Computer (that is, client or server) that reported the problem.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="94949-213">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="94949-213">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

