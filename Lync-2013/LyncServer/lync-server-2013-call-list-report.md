---
title: 'Lync Server 2013: отчет о списке обзвона'
description: 'Lync Server 2013: отчет о списке обзвона.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Call List Report
ms:assetid: 9739f9f0-7a37-4844-91d5-f089d2011013
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615020(v=OCS.15)
ms:contentKeyID: 48184921
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5b08d4c5f3011facc9cd8d4f6b2800638f3cc896
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435756"
---
# <a name="call-list-report-in-lync-server-2013"></a><span data-ttu-id="06bba-103">Отчет "список обзвона" в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="06bba-103">Call List Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="06bba-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="06bba-104">

<span> </span></span></span>

<span data-ttu-id="06bba-105">_**Тема последнего изменения:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="06bba-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="06bba-106">Отчет по списку обзвона предоставляет параметры качества взаимодействия (QoE) для отдельных вызовов, выполненных и принятых сотрудниками организации.</span><span class="sxs-lookup"><span data-stu-id="06bba-106">The Call List Report provides Quality of Experience (QoE) metrics for individual calls made and received in your organization.</span></span> <span data-ttu-id="06bba-107">Обратите внимание, что действительные параметры, содержащиеся в отчете, зависят от способа доступа к отчету по списку обзвона.</span><span class="sxs-lookup"><span data-stu-id="06bba-107">Note that the actual metrics reported will depend on how you access the Call List report.</span></span> <span data-ttu-id="06bba-108">Например, если открыть отчет из [отчета на устройстве в Lync Server 2013, в](lync-server-2013-device-report.md)отчете об устройстве будут показаны такие метрики, как, например, метрики, указанные ниже.</span><span class="sxs-lookup"><span data-stu-id="06bba-108">For example, if you open the report from the [Device Report in Lync Server 2013](lync-server-2013-device-report.md), you'll see metrics such as the following, metrics that are also reported on the Device Report:</span></span>

  - <span data-ttu-id="06bba-109">Микрофон вызывающего абонента</span><span class="sxs-lookup"><span data-stu-id="06bba-109">Caller's microphone</span></span>

  - <span data-ttu-id="06bba-110">Динамик вызывающего абонента</span><span class="sxs-lookup"><span data-stu-id="06bba-110">Caller's speaker</span></span>

  - <span data-ttu-id="06bba-111">Микрофон вызываемого абонента</span><span class="sxs-lookup"><span data-stu-id="06bba-111">Callee's microphone</span></span>

  - <span data-ttu-id="06bba-112">Динамик вызываемого абонента</span><span class="sxs-lookup"><span data-stu-id="06bba-112">Callee's speaker</span></span>

  - <span data-ttu-id="06bba-113">Соотношение времени голосовой коммутации</span><span class="sxs-lookup"><span data-stu-id="06bba-113">Ratio of voice switch time</span></span>

<span data-ttu-id="06bba-114">Тем не менее, если открыть отчет "список обзвона" из [отчета о местоположении в Lync Server 2013](lync-server-2013-location-report.md), вы не увидите эти метрики; Вместо этого вы увидите метрики, подобные указанным ниже.</span><span class="sxs-lookup"><span data-stu-id="06bba-114">However, if you open the Call List Report from the [Location Report in Lync Server 2013](lync-server-2013-location-report.md), you won't see any of those metrics; instead, you'll see metrics like these:</span></span>

  - <span data-ttu-id="06bba-115">Круговой путь (мс)</span><span class="sxs-lookup"><span data-stu-id="06bba-115">Round trip (ms)</span></span>

  - <span data-ttu-id="06bba-116">Падение качества (средняя оценка)</span><span class="sxs-lookup"><span data-stu-id="06bba-116">Degradation (MOS)</span></span>

  - <span data-ttu-id="06bba-117">Потеря пакетов</span><span class="sxs-lookup"><span data-stu-id="06bba-117">Packet loss</span></span>

  - <span data-ttu-id="06bba-118">Дрожание (мс)</span><span class="sxs-lookup"><span data-stu-id="06bba-118">Jitter (ms)</span></span>

<span data-ttu-id="06bba-p102">Это показатели, содержащиеся в отчете о местоположении. Однако вы всегда можете щелкнуть «Подробные показатели» в отчете по списку обзвона, чтобы получить полную информацию QoE для любого вызова.</span><span class="sxs-lookup"><span data-stu-id="06bba-p102">Those are the metrics reported on the Location Report. However, from the Call List Report you can always click the Detail metric to provide complete QoE information for any call.</span></span>

<div>

## <a name="accessing-the-call-list-report"></a><span data-ttu-id="06bba-121">Доступ к отчету по списку обзвона</span><span class="sxs-lookup"><span data-stu-id="06bba-121">Accessing the Call List Report</span></span>

<span data-ttu-id="06bba-122">Доступ к отчету по списку обзвона можно получить из любого из следующих отчетов:</span><span class="sxs-lookup"><span data-stu-id="06bba-122">The Call List Report can be accessed from any of the following reports:</span></span>

  - <span data-ttu-id="06bba-123">[Отчет о расположении в Lync Server 2013](lync-server-2013-location-report.md) (щелчок на громкость звонка или процент неудовлетворительного звонка)</span><span class="sxs-lookup"><span data-stu-id="06bba-123">The [Location Report in Lync Server 2013](lync-server-2013-location-report.md) (by clicking the Call volume or Poor call percentage metric)</span></span>

  - <span data-ttu-id="06bba-124">[Отчет об устройстве в Lync Server 2013](lync-server-2013-device-report.md) (щелчок на громкость звонка или процент неудовлетворительного звонка)</span><span class="sxs-lookup"><span data-stu-id="06bba-124">The [Device Report in Lync Server 2013](lync-server-2013-device-report.md) (by clicking the Call volume or Poor call percentage metric)</span></span>

  - <span data-ttu-id="06bba-125">[Сводный отчет о качестве качества мультимедиа в Lync Server 2013](lync-server-2013-media-quality-summary-report.md) (щелчок на громкость звонка или процент неудовлетворительного звонка)</span><span class="sxs-lookup"><span data-stu-id="06bba-125">The [Media Quality Summary Report in Lync Server 2013](lync-server-2013-media-quality-summary-report.md) (by clicking the Call volume or Poor call percentage metric)</span></span>

  - <span data-ttu-id="06bba-126">[Отчет о производительности сервера в Lync server 2013](lync-server-2013-server-performance-report.md) (с помощью кнопки "позвонить" или "неудовлетворительный процент звонка")</span><span class="sxs-lookup"><span data-stu-id="06bba-126">The [Server Performance Report in Lync Server 2013](lync-server-2013-server-performance-report.md) (by clicking the Call volume or Poor call percentage metric)</span></span>

<span data-ttu-id="06bba-127">В отчете список обзвона вы можете получить доступ к [подробным сведениям о звонке в Lync Server 2013](lync-server-2013-call-detail-report.md) , щелкнув соответствующую детальную метрику.</span><span class="sxs-lookup"><span data-stu-id="06bba-127">From within the Call List Report you can access the [Call Detail Report in Lync Server 2013](lync-server-2013-call-detail-report.md) by clicking the Detail metric.</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-call-list-report"></a><span data-ttu-id="06bba-128">Эффективное использование отчета по списку обзвона</span><span class="sxs-lookup"><span data-stu-id="06bba-128">Making the Best Use of the Call List Report</span></span>

<span data-ttu-id="06bba-129">Если вы не помните, для чего именно используются некоторые показатели отчета по списку обзвона (например, «Соотношение времени голосовой коммутации»), наведите указатель мыши на метку показателя; отобразится всплывающая подсказка, содержащая краткое описание показателя.</span><span class="sxs-lookup"><span data-stu-id="06bba-129">If you can't remember what some of the Call List Report metrics (such as Ratio voice switch time) actually measure, hold your mouse over the metric label; a tool tip will then appear giving you a brief description of the metric.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="06bba-130">Фильтры</span><span class="sxs-lookup"><span data-stu-id="06bba-130">Filters</span></span>

<span data-ttu-id="06bba-p103">Нет. Фильтрация отчета по списку обзвона невозможна.</span><span class="sxs-lookup"><span data-stu-id="06bba-p103">None. You cannot filter the Call List Report.</span></span>

</div>

<div>

## <a name="metrics"></a><span data-ttu-id="06bba-133">Показатели</span><span class="sxs-lookup"><span data-stu-id="06bba-133">Metrics</span></span>

<span data-ttu-id="06bba-134">В следующей таблице представлен список данных, которые приводятся в отчете по списку обзвона для каждого вызова.</span><span class="sxs-lookup"><span data-stu-id="06bba-134">The following table lists the information provided in the Call List Report for each call.</span></span>

### <a name="call-list-report-metrics"></a><span data-ttu-id="06bba-135">Показатели в отчете по списку обзвона</span><span class="sxs-lookup"><span data-stu-id="06bba-135">Call List Report Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="06bba-136">Имя</span><span class="sxs-lookup"><span data-stu-id="06bba-136">Name</span></span></th>
<th><span data-ttu-id="06bba-137">Поддержка сортировки</span><span class="sxs-lookup"><span data-stu-id="06bba-137">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="06bba-138">Описание</span><span class="sxs-lookup"><span data-stu-id="06bba-138">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="06bba-139"><strong>Сведения</strong></span><span class="sxs-lookup"><span data-stu-id="06bba-139"><strong>Details</strong></span></span></p></td>
<td><p><span data-ttu-id="06bba-140">Нет</span><span class="sxs-lookup"><span data-stu-id="06bba-140">No</span></span></p></td>
<td><p><span data-ttu-id="06bba-141">Если щелкнуть этот элемент, в отчете отображается дополнительная информация о вызове.</span><span class="sxs-lookup"><span data-stu-id="06bba-141">When you click this item, the report shows additional information on the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06bba-142"><strong>Вызывающая сторона</strong></span><span class="sxs-lookup"><span data-stu-id="06bba-142"><strong>Caller</strong></span></span></p></td>
<td><p><span data-ttu-id="06bba-143">Да</span><span class="sxs-lookup"><span data-stu-id="06bba-143">Yes</span></span></p></td>
<td><p><span data-ttu-id="06bba-144">SIP-адрес пользователя, инициировавшего вызов.</span><span class="sxs-lookup"><span data-stu-id="06bba-144">SIP address of the person who initiated the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06bba-145"><strong>Вызываемая сторона</strong></span><span class="sxs-lookup"><span data-stu-id="06bba-145"><strong>Callee</strong></span></span></p></td>
<td><p><span data-ttu-id="06bba-146">Да</span><span class="sxs-lookup"><span data-stu-id="06bba-146">Yes</span></span></p></td>
<td><p><span data-ttu-id="06bba-147">SIP-адрес пользователя, который принял вызов.</span><span class="sxs-lookup"><span data-stu-id="06bba-147">SIP address of the person who was called.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06bba-148"><strong>Время начала</strong></span><span class="sxs-lookup"><span data-stu-id="06bba-148"><strong>Start time</strong></span></span></p></td>
<td><p><span data-ttu-id="06bba-149">Да</span><span class="sxs-lookup"><span data-stu-id="06bba-149">Yes</span></span></p></td>
<td><p><span data-ttu-id="06bba-150">Дата и время начала звонка.</span><span class="sxs-lookup"><span data-stu-id="06bba-150">Date and time that the call started.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06bba-151"><strong>Время окончания</strong></span><span class="sxs-lookup"><span data-stu-id="06bba-151"><strong>End time</strong></span></span></p></td>
<td><p><span data-ttu-id="06bba-152">Да</span><span class="sxs-lookup"><span data-stu-id="06bba-152">Yes</span></span></p></td>
<td><p><span data-ttu-id="06bba-153">Дата и время окончания звонка.</span><span class="sxs-lookup"><span data-stu-id="06bba-153">Date and time that the call ended.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06bba-154"><strong>Агент вызывающего пользователя</strong></span><span class="sxs-lookup"><span data-stu-id="06bba-154"><strong>Caller user agent</strong></span></span></p></td>
<td><p><span data-ttu-id="06bba-155">Да</span><span class="sxs-lookup"><span data-stu-id="06bba-155">Yes</span></span></p></td>
<td><p><span data-ttu-id="06bba-156">Программное обеспечение, используемое конечной точкой пользователя, который инициировал вызов.</span><span class="sxs-lookup"><span data-stu-id="06bba-156">Software used by the endpoint of the person who initiated the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06bba-157"><strong>Агент вызываемого пользователя</strong></span><span class="sxs-lookup"><span data-stu-id="06bba-157"><strong>Callee user agent</strong></span></span></p></td>
<td><p><span data-ttu-id="06bba-158">Да</span><span class="sxs-lookup"><span data-stu-id="06bba-158">Yes</span></span></p></td>
<td><p><span data-ttu-id="06bba-159">Программное обеспечение, используемое конечной точкой пользователя, который принял вызов.</span><span class="sxs-lookup"><span data-stu-id="06bba-159">Software used by the endpoint of the person who was called.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06bba-160"><strong>Круговой путь (мс)</strong></span><span class="sxs-lookup"><span data-stu-id="06bba-160"><strong>Round trip (ms)</strong></span></span></p></td>
<td><p><span data-ttu-id="06bba-161">Да</span><span class="sxs-lookup"><span data-stu-id="06bba-161">Yes</span></span></p></td>
<td><p><span data-ttu-id="06bba-p104">Среднее время (в миллисекунда) требуемое для передачи пакета протокола транспорта реального времени (RTP) в другую конечную точку и обратно. Круговой путь в 100 и меньше миллисекунд считается допустимым.</span><span class="sxs-lookup"><span data-stu-id="06bba-p104">Average amount of (in milliseconds) required for a real-time transport protocol (RTP) packet to travel to another endpoint and then back. Round-trip times of 100 milliseconds or less are considered of acceptable quality.</span></span></p>
<p><span data-ttu-id="06bba-p105">Высокие значения прохождения кругового пути могут быть вызваны маршрутизацией международных звонков, неправильной настройкой маршрутизацией или перегрузкой сервера-посредника. Большое время кругового пути приводит к трудностям при обслуживании двунаправленных аудиоразговоров.</span><span class="sxs-lookup"><span data-stu-id="06bba-p105">High round-trip values can be caused by international call routing, a routing misconfiguration, or an overloaded media server. High round-trip times result in difficulties with two-way, real-time audio conversations.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06bba-166"><strong>Падение качества (средняя оценка)</strong></span><span class="sxs-lookup"><span data-stu-id="06bba-166"><strong>Degradation (MOS)</strong></span></span></p></td>
<td><p><span data-ttu-id="06bba-167">Да</span><span class="sxs-lookup"><span data-stu-id="06bba-167">Yes</span></span></p></td>
<td><p><span data-ttu-id="06bba-168">Средняя экспертная оценка падения качества связи во время звонка.</span><span class="sxs-lookup"><span data-stu-id="06bba-168">Average amount of mean opinion score (MOS) degradation experienced during a call.</span></span> <span data-ttu-id="06bba-169">Значения лежат в диапазоне от 0,0 до 5,0.</span><span class="sxs-lookup"><span data-stu-id="06bba-169">Degradation values can range from a low of 0.0 to a high of 5.0.</span></span> <span data-ttu-id="06bba-170">Значение 0,5 или меньшее обозначает допустимое падение качества.</span><span class="sxs-lookup"><span data-stu-id="06bba-170">A value of 0.5 or less represents acceptable degradation.</span></span> <span data-ttu-id="06bba-171">Изначально средние оценки рассчитывались на основе оценок, даваемых звонкам пользователями по шкале от 1 до 5.</span><span class="sxs-lookup"><span data-stu-id="06bba-171">Historically, mean options scores were calculated by having users rate the quality of a call on a scale of 1-to-5.</span></span> <span data-ttu-id="06bba-172">В Lync Server Lync Server использует набор алгоритмов для прогнозирования того, как пользователи будут оценены при звонке.</span><span class="sxs-lookup"><span data-stu-id="06bba-172">In Lync Server, Lync Server uses a set of algorithms to predict how users would have rated a call.</span></span></p>
<p><span data-ttu-id="06bba-p107">Большие оценки падения качества могут быть вызваны перегрузкой сети, недостатком пропускной способности, помехами в беспроводной среде, перегрузкой на сервере-посреднике или конечной точке. Падение качества приводит к искажению или потере аудиосигнала.</span><span class="sxs-lookup"><span data-stu-id="06bba-p107">High degradation values can be caused by congestion, lack of bandwidth, wireless congestion or interference, or an overloaded media server or endpoint. High degradation results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06bba-175"><strong>Потеря пакетов</strong></span><span class="sxs-lookup"><span data-stu-id="06bba-175"><strong>Packet loss</strong></span></span></p></td>
<td><p><span data-ttu-id="06bba-176">Да</span><span class="sxs-lookup"><span data-stu-id="06bba-176">Yes</span></span></p></td>
<td><p><span data-ttu-id="06bba-p108">Среднее значение потери RTP-пакетов. (Пакет считается потерянным, если он не дошел до назначения). Большие значения потери пакетов могут быть вызваны перегрузкой сети, недостатком пропускной способности, помехами в беспроводной среде, перегрузкой на сервере-посреднике. Обычно это приводит к искажению или потере аудиосигнала.</span><span class="sxs-lookup"><span data-stu-id="06bba-p108">Average rate of RTP packet loss. (Packet loss occurs when RTP packets, a protocol used for transmitting audio and video across the Internet, failed to reach their destination.) High loss rates are generally caused by congestion, lack of bandwidth, wireless congestion or interference, or an overloaded media server. Packet loss typically results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06bba-180"><strong>Искажение</strong></span><span class="sxs-lookup"><span data-stu-id="06bba-180"><strong>Jitter</strong></span></span></p></td>
<td><p><span data-ttu-id="06bba-181">Да</span><span class="sxs-lookup"><span data-stu-id="06bba-181">Yes</span></span></p></td>
<td><p><span data-ttu-id="06bba-182">Среднее значение колебаний, зарегистрированных между прибытиями пакетов RTP.</span><span class="sxs-lookup"><span data-stu-id="06bba-182">Average jitter detected between RTP packet arrivals.</span></span> <span data-ttu-id="06bba-183">(Колебание — это мера &quot; shakiness &quot; звонка). Обычно значения с высокой степенью колебаний заключаются в результате перегруженности или перегруженного сервера мультимедиа, что приводит к искажению или потере звука.</span><span class="sxs-lookup"><span data-stu-id="06bba-183">(Jitter is a measure of the &quot;shakiness&quot; of a call.) High jitter values are typically caused by congestion or an overloaded media server, and result in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06bba-184"><strong>Степень маскированных аудиообразцов</strong></span><span class="sxs-lookup"><span data-stu-id="06bba-184"><strong>Healer concealed ratio</strong></span></span></p></td>
<td><p><span data-ttu-id="06bba-185">Да</span><span class="sxs-lookup"><span data-stu-id="06bba-185">Yes</span></span></p></td>
<td><p><span data-ttu-id="06bba-p110">Средняя степень маскированных аудиообразцов по отношению к общему числу образцов. (Маскирование аудио - это методика, которая применяется для сглаживания оборванной передачи, которая обычно происходит при потери сетевых пакетов). Большие значения обозначают частое применение данной методики, вызванной из-за потери пакетов или искажений сигнала.</span><span class="sxs-lookup"><span data-stu-id="06bba-p110">Average ratio of concealed audio samples to the total to the total number of samples. (A concealed audio sample is a technique used to smooth out the abrupt transition that would usually be caused by dropped network packets.) High values indicate significant levels of loss concealment applied caused by packet loss or jitter, and results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06bba-188"><strong>Степень растянутых образцов</strong></span><span class="sxs-lookup"><span data-stu-id="06bba-188"><strong>Healer stretched ratio</strong></span></span></p></td>
<td><p><span data-ttu-id="06bba-189">Да</span><span class="sxs-lookup"><span data-stu-id="06bba-189">Yes</span></span></p></td>
<td><p><span data-ttu-id="06bba-p111">Средняя степень растянутых аудиообразцов по отношению к общему числу образцов. (Растягивание аудиопакета - это методика, которая применяется для поддержания качества звонка при обнаружении потери сетевого пакета). Большие значения обозначают частое применение данной методики, вызванное большими искажениями – аудиосигнал звучит как роботизированный.</span><span class="sxs-lookup"><span data-stu-id="06bba-p111">Average ratio of stretched audio samples to the total to the total number of samples. (Stretched audio is audio that has been expanded to help maintain call quality when a dropped network packet has been detected.) High values indicate significant levels of sample stretching caused by jitter, and result in audio sounding robotic or distorted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06bba-192"><strong>Степень сжатых аудиообразцов</strong></span><span class="sxs-lookup"><span data-stu-id="06bba-192"><strong>Healer compressed ratio</strong></span></span></p></td>
<td><p><span data-ttu-id="06bba-193">Да</span><span class="sxs-lookup"><span data-stu-id="06bba-193">Yes</span></span></p></td>
<td><p><span data-ttu-id="06bba-p112">Средняя степень растянутых аудиообразцов по отношению к общему числу образцов. (Сжатие аудиопакета - это методика, которая применяется для поддержания качества звонка при обнаружении потери сетевого пакета). Большие значения обозначают частое применение данной методики, вызванное большими искажениями – аудиосигнал звучит как ускоренный или искаженный.</span><span class="sxs-lookup"><span data-stu-id="06bba-p112">Average ratio of compressed audio samples to the total number of samples. (Compressed audio is audio that has been compressed to help maintain call quality when a dropped network packet has been detected.) High values indicate significant levels of sample compression caused by jitter, and result in audio sounding accelerated or distorted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06bba-196"><strong>Подключение</strong></span><span class="sxs-lookup"><span data-stu-id="06bba-196"><strong>Connectivity</strong></span></span></p></td>
<td><p><span data-ttu-id="06bba-197">Да</span><span class="sxs-lookup"><span data-stu-id="06bba-197">Yes</span></span></p></td>
<td><p><span data-ttu-id="06bba-p113">Типа канала беспроводной связи. Как правило, используется один из следующих каналов:</span><span class="sxs-lookup"><span data-stu-id="06bba-p113">Type of wireless communication link. Typically, this is one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="06bba-200">Ретрансляция</span><span class="sxs-lookup"><span data-stu-id="06bba-200">Relay</span></span></p></li>
<li><p><span data-ttu-id="06bba-201">Прямое подключение</span><span class="sxs-lookup"><span data-stu-id="06bba-201">Direct</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table><span data-ttu-id="06bba-202">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="06bba-202">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

