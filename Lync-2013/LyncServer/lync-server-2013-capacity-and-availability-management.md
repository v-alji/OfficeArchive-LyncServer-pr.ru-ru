---
title: 'Lync Server 2013: Управление емкостью и обеспечением доступности'
description: 'Lync Server 2013: Управление емкостью и обеспечением доступности.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Capacity and availability management
ms:assetid: 207a2997-f482-4bee-892d-d2b112294481
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720325(v=OCS.15)
ms:contentKeyID: 63969586
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d498649651f8cfbccc65f5b1b5f010025ac418e7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435602"
---
# <a name="capacity-and-availability-management-in-lync-server-2013"></a><span data-ttu-id="dfe43-103">Управление емкостью и доступностью в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dfe43-103">Capacity and availability management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="dfe43-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="dfe43-104">

<span> </span></span></span>

<span data-ttu-id="dfe43-105">_**Тема последнего изменения:** 2014-08-18_</span><span class="sxs-lookup"><span data-stu-id="dfe43-105">_**Topic Last Modified:** 2014-08-18_</span></span>

<span data-ttu-id="dfe43-106">Цель управления емкостью и обеспечением доступности — измерение и контроль производительности системы.</span><span class="sxs-lookup"><span data-stu-id="dfe43-106">The purpose of capacity management and availability management is to measure and control system performance.</span></span> <span data-ttu-id="dfe43-107">Мы рекомендуем реализовать процедуры управления емкостью и управления надежностью, чтобы можно было измерять и контролировать производительность системы.</span><span class="sxs-lookup"><span data-stu-id="dfe43-107">We recommend that you implement capacity management and availability management procedures so that you can measure and control system performance.</span></span> <span data-ttu-id="dfe43-108">Вам нужно знать, доступна ли система, и может обрабатывать текущие и прогнозируемые требования, задавая базовые показатели и контролируя систему для поиска тенденций.</span><span class="sxs-lookup"><span data-stu-id="dfe43-108">You have to know whether the system is available and if it can handle the current and the projected demands by setting baselines and monitoring the system to look for trends.</span></span>

<div>

## <a name="capacity-management"></a><span data-ttu-id="dfe43-109">Управление емкостью</span><span class="sxs-lookup"><span data-stu-id="dfe43-109">Capacity management</span></span>

<span data-ttu-id="dfe43-110">Управление производительностью включает в себя планирование, изменение размера и Управление емкостью служб, чтобы гарантировать превышение минимальных уровней производительности, указанных для вашего соглашения об уровне обслуживания.</span><span class="sxs-lookup"><span data-stu-id="dfe43-110">Capacity management involves planning, sizing, and controlling service capacity to help guarantee that the minimum performance levels specified in your SLA are exceeded.</span></span> <span data-ttu-id="dfe43-111">Эффективное Управление емкостью помогает обеспечить предоставление ИТ-услуг по разумным затратам и, тем не менее, отвечать на уровни производительности, определенные в рамках вашего соглашения об уровне обслуживания с помощью клиента.</span><span class="sxs-lookup"><span data-stu-id="dfe43-111">Good capacity management helps ensure that you can provide IT services at a reasonable cost and still meet the levels of performance defined in your SLAs with the client.</span></span> <span data-ttu-id="dfe43-112">Эти условия могут включать в себя следующее:</span><span class="sxs-lookup"><span data-stu-id="dfe43-112">These criteria can include the following:</span></span>

  - <span data-ttu-id="dfe43-113">**Время ответа системы**   Это измеряемое время, которое система предпринимает для выполнения типичных действий.</span><span class="sxs-lookup"><span data-stu-id="dfe43-113">**System Response Time**   This is the measured time that the system takes to do typical actions.</span></span> <span data-ttu-id="dfe43-114">В качестве примера можно привести время, необходимое для работы роли аудио-и видеофайла для обработки аудио-и видеопотока, время, необходимое для создания и присоединения к Конференции с помощью клиента, а также время, затраченное на обновление во всех клиентах наблюдателей.</span><span class="sxs-lookup"><span data-stu-id="dfe43-114">Examples include the time that is required for the audio/video server role to process audio/video traffic, the time that is required for a client to create and join a conference, or the time taken for presence to be updated in all watcher clients.</span></span>

  - <span data-ttu-id="dfe43-115">**Емкость хранилища**   Это емкость системы хранения, будь то база данных контента, устройство резервного копирования или локальный диск.</span><span class="sxs-lookup"><span data-stu-id="dfe43-115">**Storage Capacity**   This is the capacity of a storage system, whether it is a content database, a backup device, or a local drive.</span></span> <span data-ttu-id="dfe43-116">Пример: максимальный объем дискового пространства, который должен быть указан на сайте, и время, в которое необходимо сохранить резервные копии, прежде чем они будут перезаписаны.</span><span class="sxs-lookup"><span data-stu-id="dfe43-116">Examples include the maximum amount of storage space to be provided per site and the time that backups should be stored before they are overwritten.</span></span>

<span data-ttu-id="dfe43-117">Настройка емкости зачастую является единственным вариантом обеспечения доступности достаточных физических ресурсов, таких как место на диске и пропускная способность сети.</span><span class="sxs-lookup"><span data-stu-id="dfe43-117">Adjusting capacity is frequently a case of making sure that enough physical resources are available, such as disk space and network bandwidth.</span></span> <span data-ttu-id="dfe43-118">В приведенной ниже таблице перечислены типичные решения проблем, связанных с производительностью.</span><span class="sxs-lookup"><span data-stu-id="dfe43-118">The following table lists typical resolutions for capacity-related issues.</span></span>

### <a name="typical-resolutions-for-capacity-related-issues"></a><span data-ttu-id="dfe43-119">Типичные решения проблем, связанных с производительностью</span><span class="sxs-lookup"><span data-stu-id="dfe43-119">Typical resolutions for capacity-related issues</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="dfe43-120">Ошибка</span><span class="sxs-lookup"><span data-stu-id="dfe43-120">Issue</span></span></th>
<th><span data-ttu-id="dfe43-121">Возможное решение</span><span class="sxs-lookup"><span data-stu-id="dfe43-121">Possible resolution</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dfe43-122">Неудовлетворительные качество звука и видео удаленных пользователей</span><span class="sxs-lookup"><span data-stu-id="dfe43-122">Remote users having poor audio/video performance</span></span></p></td>
<td><p><span data-ttu-id="dfe43-123">Проверьте, доступна ли подходящая пропускная способность для WAN Links, а также в том случае, если качество обслуживания включено и настроено надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="dfe43-123">Check to see whether appropriate bandwidth is available on the WAN links and if QoS is enabled and appropriately configured.</span></span> <span data-ttu-id="dfe43-124">Проверьте данные QoE.</span><span class="sxs-lookup"><span data-stu-id="dfe43-124">Check QoE data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dfe43-125">Общий ответ среды Lync очень медленный.</span><span class="sxs-lookup"><span data-stu-id="dfe43-125">Overall response of the Lync environment is slow.</span></span></p></td>
<td><p><span data-ttu-id="dfe43-126">Выполнение тестов для проверки того, что существующие серверы переднего плана могут работать с загрузкой.</span><span class="sxs-lookup"><span data-stu-id="dfe43-126">Run tests to check that the existing front-end servers can deal with the load.</span></span> <span data-ttu-id="dfe43-127">Представьте новый сервер переднего плана, если это необходимо. Проверьте значения времени ответа на базу данных SQL и исправьте причины возникновения задержек (например, улучшения дискового ввода-вывода).</span><span class="sxs-lookup"><span data-stu-id="dfe43-127">Introduce a new front-end server if it is needed.Check SQL database response times and fix the causes for the delays (for example, improve disk I/O).</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="dfe43-128">Более подробные сведения об устранении неполадок описаны в руководстве по сети Lync Server.</span><span class="sxs-lookup"><span data-stu-id="dfe43-128">Troubleshooting in greater detail is covered in the Lync Server Networking Guide.</span></span>

<span data-ttu-id="dfe43-129">На производительность влияет настройка системы, и они зависят от физических ресурсов, таких как пропускная способность сети.</span><span class="sxs-lookup"><span data-stu-id="dfe43-129">Capacity is affected by system configuration and depends on physical resources such as network bandwidth.</span></span> <span data-ttu-id="dfe43-130">Например, если среда Lync настроена для ежедневного выполнения полного резервного копирования, необходимо соблюдать осторожность, чтобы гарантировать, что эффект на интерактивной производительности, доступ к которой происходил для конечных пользователей, будет минимизирован.</span><span class="sxs-lookup"><span data-stu-id="dfe43-130">For example, if a Lync environment is configured to perform a full backup nightly, care must be taken to help guarantee that the effect on the interactive performance experienced by end-users is minimized.</span></span>

<span data-ttu-id="dfe43-131">Управление производительностью — это процесс сохранения мощности системы в пределах приемлемых уровней и устранения указанных ниже проблем.</span><span class="sxs-lookup"><span data-stu-id="dfe43-131">Capacity management is the process of keeping the capacity of a system within acceptable levels and addresses the following issues:</span></span>

  - <span data-ttu-id="dfe43-132">**Реагирование на изменения в требованиях**   Требования к мощности должны быть скорректированы для учета изменений в системе или в Организации.</span><span class="sxs-lookup"><span data-stu-id="dfe43-132">**Reacting to changes in requirements**   Capacity requirements have to be adjusted to account for changes in the system or the organization.</span></span> <span data-ttu-id="dfe43-133">Например, если в вашей среде требуется реализовать корпоративную голосовую почту, будет очень важнее количество и расположение серверов-посредников и шлюзов для коммутируемой телефонной сети.</span><span class="sxs-lookup"><span data-stu-id="dfe43-133">For example, if your environment decides to implement Enterprise Voice, the number and placement of Mediation Servers and public switched telephone network (PSTN) gateways will be very important.</span></span> <span data-ttu-id="dfe43-134">Если вы собираетесь звонить по протоколу SIP или Direct SIP, Общая схема будет значительно изменяться для обеспечения оптимальной производительности при работе с корпоративной голосовой связью.</span><span class="sxs-lookup"><span data-stu-id="dfe43-134">If you'll be doing Session Initiation Protocol (SIP) trunking or direct SIP, the overall design will be significantly changed to provide the best Enterprise Voice performance.</span></span>

  - <span data-ttu-id="dfe43-135">**Прогнозирование будущих требований**   Некоторые требования к мощности изменяются предсказуемым образом с течением времени.</span><span class="sxs-lookup"><span data-stu-id="dfe43-135">**Predicting future requirements**   Some capacity requirements change predictably over time.</span></span> <span data-ttu-id="dfe43-136">Отслеживая тенденции, вы можете предварительно планировать обновления.</span><span class="sxs-lookup"><span data-stu-id="dfe43-136">By tracking trends you can plan upgrades in advance.</span></span> <span data-ttu-id="dfe43-137">Например, для создания базового плана необходимо отслеживать доступную пропускную способность между различными сайтами Lync.</span><span class="sxs-lookup"><span data-stu-id="dfe43-137">For example, available bandwidth between various Lync sites must be monitored to create a baseline.</span></span> <span data-ttu-id="dfe43-138">Этот базовый план позволит вам предсказать, когда необходимо добавить дополнительную пропускную способность для этих ссылок, так как количество пользователей на этих сайтах увеличится с учетом времени.</span><span class="sxs-lookup"><span data-stu-id="dfe43-138">This baseline will allow you to predict when you have to add more bandwidth to these links as user count in these remote sites increases with time.</span></span>

</div>

<div>

## <a name="availability-management"></a><span data-ttu-id="dfe43-139">Управление обеспечением доступности</span><span class="sxs-lookup"><span data-stu-id="dfe43-139">Availability management</span></span>

<span data-ttu-id="dfe43-140">Управление обеспечением доступности — это процесс, который гарантирует своевременную и экономичную работу любых ИТ – служб, необходимых для клиента.</span><span class="sxs-lookup"><span data-stu-id="dfe43-140">Availability management is the process of making sure that any IT service consistently and cost effectively delivers the level of consistent, reliable service that is required by the customer.</span></span> <span data-ttu-id="dfe43-141">Управление обеспечением доступности — это минимизация потерь на обслуживание и обеспечение выполнения соответствующего действия при потере обслуживания.</span><span class="sxs-lookup"><span data-stu-id="dfe43-141">Availability management deals with minimizing loss of service and with making sure that appropriate action is taken if service is lost.</span></span> <span data-ttu-id="dfe43-142">В среде Lync может возникнуть вопрос того, доступна ли корпоративная голосовая служба, могут ли пользователи присоединяться к запланированным конференциям и т. д.</span><span class="sxs-lookup"><span data-stu-id="dfe43-142">In a Lync environment, you may be concerned about whether the Enterprise Voice service is available, whether users can join scheduled conferences, and so on.</span></span> <span data-ttu-id="dfe43-143">Соглашение об уровне обслуживания определяет приемлемую частоту и продолжительность перерывов, а также позволяет получить определенные периоды, когда система будет недоступна для запланированного обслуживания.</span><span class="sxs-lookup"><span data-stu-id="dfe43-143">An SLA defines an acceptable frequency and length of outages and allows for certain periods when the system is unavailable for planned maintenance.</span></span>

<span data-ttu-id="dfe43-144">Если вам нужно предоставлять отчеты для управления сведениями о доступности систем или при наличии финансовых или других санкций, связанных с отсутствующими целевыми объектами доступности, необходимо записать данные о доступности.</span><span class="sxs-lookup"><span data-stu-id="dfe43-144">If you have to provide reports to your management about the availability of systems, or if you have financial or other penalties associated with missing availability targets, you must record availability data.</span></span> <span data-ttu-id="dfe43-145">Даже если у вас нет подобных формальных требований, рекомендуется по крайней мере знать, как часто система завершилась сбоем за определенный период времени.</span><span class="sxs-lookup"><span data-stu-id="dfe43-145">Even if you do not have such formal requirements, it is a good idea to at least know how frequently a system has failed in a certain time period.</span></span> <span data-ttu-id="dfe43-146">Например, доступность системы за последние 12 месяцев и время, затраченное на восстановление после каждой ошибки.</span><span class="sxs-lookup"><span data-stu-id="dfe43-146">For example, system availability in the last 12 months and how long it took to recover from each failure.</span></span> <span data-ttu-id="dfe43-147">Эта информация поможет вам измерять и улучшать эффективность работы группы в ответ на сбой системы.</span><span class="sxs-lookup"><span data-stu-id="dfe43-147">This information will help you measure and improve your team’s effectiveness in responding to a system failure.</span></span> <span data-ttu-id="dfe43-148">Кроме того, он может предоставить вам полезные сведения, если у вас есть спорный вопрос.</span><span class="sxs-lookup"><span data-stu-id="dfe43-148">It can also give you useful information if there is a dispute.</span></span>

<span data-ttu-id="dfe43-149">Меры, связанные с обеспечением доступности, описаны ниже.</span><span class="sxs-lookup"><span data-stu-id="dfe43-149">Measures related to availability are as follows:</span></span>

  - <span data-ttu-id="dfe43-150">**Доступность**   Обычно оно выражается в том случае, если вы хотите получить доступ к системе или службе по сравнению со временем, когда она не работает.</span><span class="sxs-lookup"><span data-stu-id="dfe43-150">**Availability**   This is typically expressed as the time that a system or service can be accessed compared to the time that it is down.</span></span> <span data-ttu-id="dfe43-151">Обычно оно выражается в процентах.</span><span class="sxs-lookup"><span data-stu-id="dfe43-151">It is typically expressed as a percentage.</span></span> <span data-ttu-id="dfe43-152">(Могут отображаться ссылки на три девяти или пять девяти).</span><span class="sxs-lookup"><span data-stu-id="dfe43-152">(You may see references to “three nines” or “five nines”.</span></span> <span data-ttu-id="dfe43-153">Они ссылаются на 99,9% и 99,999 процента доступности.)</span><span class="sxs-lookup"><span data-stu-id="dfe43-153">These refer to 99.9 percent or 99.999 percent availability.)</span></span>

  - <span data-ttu-id="dfe43-154">**Надежность**   Это мера времени между сбоями системы и иногда выражается в среднем (или среднего) времени между сбоями (MTBF).</span><span class="sxs-lookup"><span data-stu-id="dfe43-154">**Reliability**   This is a measure of the time between failures of a system and is sometimes expressed as mean (or average) time between failures (MTBF).</span></span>

  - <span data-ttu-id="dfe43-155">**Время восстановления**   Это время, затраченное на восстановление службы после возникновения сбоя, которое часто выражается как среднее время восстановления (MTTR).</span><span class="sxs-lookup"><span data-stu-id="dfe43-155">**Time to Repair**   This is the time taken to recover a service after a failure has occurred and is often expressed as mean (meaning average) time to repair (MTTR).</span></span>

<span data-ttu-id="dfe43-156">Доступность, надежность и время восстановления связаны следующим образом:</span><span class="sxs-lookup"><span data-stu-id="dfe43-156">Availability, reliability, and time to repair are related as follows:</span></span>

<span data-ttu-id="dfe43-157">**Доступность = (MTBF – MTTR)/MTBF**   Например, если в течение шести месяцев сервер не проходит два часа и недоступен в среднем в течение 20 минут, MTBF составляет три месяца или 90 дня, а MTTR — 20 минут.</span><span class="sxs-lookup"><span data-stu-id="dfe43-157">**Availability = (MTBF – MTTR) / MTBF**   For example, if a server fails two times over a six-month period and is unavailable for an average of 20 minutes, the MTBF is three months or 90 days and the MTTR is 20 minutes.</span></span> <span data-ttu-id="dfe43-158">Таким образом, доступность = (90 дней – 20 минут)/90 дней = 99,985%.</span><span class="sxs-lookup"><span data-stu-id="dfe43-158">Therefore, Availability = (90 days – 20 minutes) / 90 days = 99.985 percent.</span></span>

<span data-ttu-id="dfe43-159">Управление обеспечением доступности — это процесс, который гарантирует, что доступность развернута и сохраняется в параметрах, определенных в SLA.</span><span class="sxs-lookup"><span data-stu-id="dfe43-159">Availability management is the process of making sure that availability is maximized and kept within the parameters that are defined in SLAs.</span></span> <span data-ttu-id="dfe43-160">Управление обеспечением доступности включает следующие процессы:</span><span class="sxs-lookup"><span data-stu-id="dfe43-160">Availability management includes the following processes:</span></span>

  - <span data-ttu-id="dfe43-161">**Мониторинг**    Проверка времени и количества недоступности служб.</span><span class="sxs-lookup"><span data-stu-id="dfe43-161">**Monitoring**    Examining when and for how long services are unavailable.</span></span>

  - <span data-ttu-id="dfe43-162">**Создание отчетов**   Данные о доступности должны регулярно предоставляться для управления, пользователей и групп операций.</span><span class="sxs-lookup"><span data-stu-id="dfe43-162">**Reporting**   Availability figures should be regularly provided to management, users, and operations teams.</span></span> <span data-ttu-id="dfe43-163">Эти отчеты должны выявлять тенденции и определять области, которые прекрасно работают, и области, требующие внимания.</span><span class="sxs-lookup"><span data-stu-id="dfe43-163">These reports should highlight trends and identify areas that are doing well and areas that require attention.</span></span> <span data-ttu-id="dfe43-164">Отчет должен суммировать соответствие требованиям с целями, заданными в SLA.</span><span class="sxs-lookup"><span data-stu-id="dfe43-164">The report should summarize compliance with targets set in the SLAs.</span></span>

  - <span data-ttu-id="dfe43-165">**Улучшение**   Если доступность не соответствует конечным объектам, определенным в SLA, или тенденция к снижению доступности, процесс управления сведениями о доступности должен планировать шаги.</span><span class="sxs-lookup"><span data-stu-id="dfe43-165">**Improvement**   If availability does not meet targets that are defined in the SLAs or where the trend is toward reduced availability, the availability management process should plan remedial steps.</span></span> <span data-ttu-id="dfe43-166">Это должно включать работу с другими ответственными группами, чтобы вычислить причины нарушения и спланировать повторяющиеся действия, чтобы не допустить повторения перерывов.</span><span class="sxs-lookup"><span data-stu-id="dfe43-166">This should include working with other responsible teams to highlight reasons for outages and to plan remedial actions to prevent a recurrence of the outages.</span></span>

<span data-ttu-id="dfe43-167">Измерения емкости и доступности — это повторяющиеся задачи, которые лучше всего подходят для автоматизированных средств и сценариев, таких как Microsoft System Center Operations Manager (прежнее название — Microsoft Operations Manager), которое рассматривается ниже в этом документе.</span><span class="sxs-lookup"><span data-stu-id="dfe43-167">Capacity and availability measurements are repetitive tasks that are ideally suited to automated tools and scripts such as Microsoft System Center Operations Manager (formerly Microsoft Operations Manager), which is discussed later in this document.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="dfe43-168">См. также</span><span class="sxs-lookup"><span data-stu-id="dfe43-168">See Also</span></span>


[<span data-ttu-id="dfe43-169">Мониторинг сервера Lync Server 2013 с помощью System Center Operations Manager</span><span class="sxs-lookup"><span data-stu-id="dfe43-169">Monitoring Lync Server 2013 with System Center Operations Manager</span></span>](lync-server-2013-monitoring-lync-server-with-system-center-operations-manager.md)  
  

<span data-ttu-id="dfe43-170"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="dfe43-170"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

