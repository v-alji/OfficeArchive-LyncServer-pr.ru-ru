---
title: 'Lync Server 2013: Афиша: Индикаторы работоспособности ключа'
description: 'Lync Server 2013: Афиша: Индикаторы работоспособности ключа.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: 'Poster: Key Health Indicators'
ms:assetid: 8367dccf-adaa-4a0b-a4ed-bc9570cc5e24
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn593599(v=OCS.15)
ms:contentKeyID: 61084873
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9962d1764d5d2c664bb8415261344d9b48c81149
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424241"
---
# <a name="key-health-indicators-in-lync-server-2013"></a><span data-ttu-id="2cb1b-103">Индикаторы работоспособности ключа в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2cb1b-103">Key Health Indicators in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2cb1b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2cb1b-104">

<span> </span></span></span>

<span data-ttu-id="2cb1b-105">_**Тема последнего изменения:** 2014-02-10_</span><span class="sxs-lookup"><span data-stu-id="2cb1b-105">_**Topic Last Modified:** 2014-02-10_</span></span>

<span data-ttu-id="2cb1b-106">Эта статья является дополнением к [основным индикаторам работоспособности: основанием для поддержки работоспособности](https://go.microsoft.com/fwlink/?linkid=391838) выводятся на рабочем фрагменте Lync Servers, которое можно скачать из центра загрузки.</span><span class="sxs-lookup"><span data-stu-id="2cb1b-106">This article is a companion to the [Key Health Indicators: The Foundation for Maintaining Healthy Lync Servers](https://go.microsoft.com/fwlink/?linkid=391838) poster, which you can download from the Download Center.</span></span>

<span data-ttu-id="2cb1b-107">![Афиша с описанием устранения неполадок с помощью данных KHI](images/Dn594589.b6fe82bd-d70f-4c1f-a812-b615ac5fa7d7(OCS.15).jpg "Афиша с описанием устранения неполадок с помощью данных KHI")</span><span class="sxs-lookup"><span data-stu-id="2cb1b-107">![Poster describing troubleshooting using KHI data](images/Dn594589.b6fe82bd-d70f-4c1f-a812-b615ac5fa7d7(OCS.15).jpg "Poster describing troubleshooting using KHI data")</span></span>

<span data-ttu-id="2cb1b-108">Вы можете использовать этот плакат, чтобы узнать о индикаторах работоспособности ключа (KHIs), о счетчиках производительности с пороговыми значениями, направленных на устранение проблем взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="2cb1b-108">You can use this poster to learn about Key Health Indicators (KHIs), performance counters with thresholds aimed at revealing user experience issues.</span></span> <span data-ttu-id="2cb1b-109">Сбор данных KHI обычно является первым этапом реализации методологии качества связи (CQM), что сосредоточено на обеспечении качества звука для пользователей Lync.</span><span class="sxs-lookup"><span data-stu-id="2cb1b-109">Gathering KHI data is usually the first step to implementing the Call Quality Methodology (CQM), which is focused on ensuring a quality audio experience for Lync users.</span></span>

<span data-ttu-id="2cb1b-110">Если у вас возникли вопросы о том, как использовать CQM, вы можете отправлять свои вопросы в cqmfeedback@microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="2cb1b-110">If you have questions about how to use CQM, you can submit your questions to cqmfeedback@microsoft.com.</span></span>

<span data-ttu-id="2cb1b-111">Афиша содержит сведения о следующих областях:</span><span class="sxs-lookup"><span data-stu-id="2cb1b-111">The poster explains the following areas:</span></span>

  - <span data-ttu-id="2cb1b-112">Что такое индикаторы работоспособности ключа?</span><span class="sxs-lookup"><span data-stu-id="2cb1b-112">What are Key Health Indicators?</span></span>

  - <span data-ttu-id="2cb1b-113">Сбор данных KHI</span><span class="sxs-lookup"><span data-stu-id="2cb1b-113">To Collect KHI Data</span></span>

  - <span data-ttu-id="2cb1b-114">Поток исправлений для всех ролей сервера</span><span class="sxs-lookup"><span data-stu-id="2cb1b-114">Remediation Flow for all Server Roles</span></span>

  - <span data-ttu-id="2cb1b-115">Глоссарий</span><span class="sxs-lookup"><span data-stu-id="2cb1b-115">Glossary</span></span>

  - <span data-ttu-id="2cb1b-116">Серверы переднего плана</span><span class="sxs-lookup"><span data-stu-id="2cb1b-116">Front-end Servers</span></span>

  - <span data-ttu-id="2cb1b-117">Внутренние серверы SQL Server</span><span class="sxs-lookup"><span data-stu-id="2cb1b-117">Backend SQL Servers</span></span>

  - <span data-ttu-id="2cb1b-118">Серверы-посредники</span><span class="sxs-lookup"><span data-stu-id="2cb1b-118">Mediation Servers</span></span>

  - <span data-ttu-id="2cb1b-119">пограничные серверы</span><span class="sxs-lookup"><span data-stu-id="2cb1b-119">Edge Servers</span></span>

<span id="WhatIs"></span>

<div>

## <a name="what-are-key-health-indicators"></a><span data-ttu-id="2cb1b-120">Что такое индикаторы работоспособности ключа?</span><span class="sxs-lookup"><span data-stu-id="2cb1b-120">What are Key Health Indicators?</span></span>

<span data-ttu-id="2cb1b-121">Ключевые показатели работоспособности — это счетчики производительности с пороговыми значениями, направленными на выявление проблем с производительностью пользователей.</span><span class="sxs-lookup"><span data-stu-id="2cb1b-121">Key Health Indicators are performance counters with thresholds aimed at revealing user experience issues.</span></span> <span data-ttu-id="2cb1b-122">Сбор данных KHI обычно является первым этапом реализации методологии качества связи (CQM), что сосредоточено на обеспечении качества звука для пользователей Lync.</span><span class="sxs-lookup"><span data-stu-id="2cb1b-122">Gathering KHI data is usually the first step to implementing the Call Quality Methodology (CQM), which is focused on ensuring a quality audio experience for Lync users.</span></span>

<span data-ttu-id="2cb1b-123">KHIs используются в дополнение к стандартным решениям для мониторинга Lync (например, System Center Operations Manager, Синтетическым транзакциям, сервер мониторинга), а не к этим решениям.</span><span class="sxs-lookup"><span data-stu-id="2cb1b-123">KHIs are used in addition to standard Lync Monitoring Solutions (e.g. System Center Operations Manager, Synthetic Transactions, Monitoring Server) and not instead of those solutions.</span></span>

<span data-ttu-id="2cb1b-124">Соберите данные о счетчиках производительности KHI и заполните электронную таблицу KHI, в которой находится руководство по сети, для создания системы показателей, которая поможет вам определить работоспособность развертывания Lync на сервере.</span><span class="sxs-lookup"><span data-stu-id="2cb1b-124">Collect the KHI performance counters and populate the KHI spreadsheet accompanying the Networking Guide to produce a scorecard that will help you determine the server health of a Lync deployment.</span></span> <span data-ttu-id="2cb1b-125">После заполнения она поможет вам восстановить среду и предоставит дополнительные советы другим заинтересованным сторонам.</span><span class="sxs-lookup"><span data-stu-id="2cb1b-125">Once populated, it guides you in repairing the environment and gives additional insight to other stakeholders.</span></span> <span data-ttu-id="2cb1b-126">Вычислите KHIs на ежемесячной основе и внедрите их в выполняющиеся рабочие процессы развертывания.</span><span class="sxs-lookup"><span data-stu-id="2cb1b-126">Evaluate KHIs on a monthly basis and incorporate them into any deployment’s ongoing operational processes.</span></span>

<span data-ttu-id="2cb1b-127">Загрузите [сетевое руководство по Lync Server](https://go.microsoft.com/fwlink/p/?linkid=390677) , чтобы просмотреть полный список KHIs и загрузить соответствующие электронные таблицы.</span><span class="sxs-lookup"><span data-stu-id="2cb1b-127">Download the [Lync Server Networking Guide](https://go.microsoft.com/fwlink/p/?linkid=390677) to see the full list of KHIs and to get the related spreadsheets.</span></span>

</div>

<span id="ToCollect"></span>

<div>

## <a name="to-collect-khi-data"></a><span data-ttu-id="2cb1b-128">Сбор данных KHI</span><span class="sxs-lookup"><span data-stu-id="2cb1b-128">To Collect KHI Data</span></span>

1.  <span data-ttu-id="2cb1b-129">Запустите сценарий KHI, который входит в руководство по сети Lync Server на каждом сервере Lync.</span><span class="sxs-lookup"><span data-stu-id="2cb1b-129">Run the KHI script included with the Lync Server Networking Guide on each Lync Server.</span></span> <span data-ttu-id="2cb1b-130">Это приведет к созданию сборщика данных в мониторе производительности и назовите его KHI.</span><span class="sxs-lookup"><span data-stu-id="2cb1b-130">This will create a Data Collector inside of Performance Monitor and name it KHI.</span></span> <span data-ttu-id="2cb1b-131">По умолчанию данные будут опрашиваться каждые 15 секунд.</span><span class="sxs-lookup"><span data-stu-id="2cb1b-131">By default, data will be polled every 15 seconds.</span></span>

2.  <span data-ttu-id="2cb1b-132">Перед началом рабочего дня компании перейдите на каждый сервер Lync и запустите сборщик данных KHI.</span><span class="sxs-lookup"><span data-stu-id="2cb1b-132">Before the start of your company's business day, go to each Lync Server and start the KHI Data Collector.</span></span>

3.  <span data-ttu-id="2cb1b-133">В конце этого дня остановите сборщик данных KHI и скопируйте данные в центральное расположение.</span><span class="sxs-lookup"><span data-stu-id="2cb1b-133">At the end of that day, stop the KHI Data Collector and copy the data to a central location.</span></span>

4.  <span data-ttu-id="2cb1b-134">После использования системного монитора для заполнения электронной таблицы KHI, включенной в загрузку сетевого руководства Lync Server, Сравните результаты с рекомендованными целями.</span><span class="sxs-lookup"><span data-stu-id="2cb1b-134">After using Performance Monitor to fill in the KHI spreadsheet included with the Lync Server Networking Guide download, compare the results to the recommended targets.</span></span>

</div>

<span id="Remidiation"></span>

<div>

## <a name="remediation-flow-for-all-server-roles"></a><span data-ttu-id="2cb1b-135">Поток исправлений для всех ролей сервера</span><span class="sxs-lookup"><span data-stu-id="2cb1b-135">Remediation Flow for all Server Roles</span></span>

<span data-ttu-id="2cb1b-136">Для каждого сервера в реализации Lync Начните с проверки работоспособности компонента сервера и производительности системы на нужном уровне.</span><span class="sxs-lookup"><span data-stu-id="2cb1b-136">For each server in your Lync implementation, begin by verifying that the server’s component health and system performance is at or above the desired level.</span></span> <span data-ttu-id="2cb1b-137">Только после этого вы должны ознакомиться с индикаторами, относящимися к роли сервера в общей реализации Lync.</span><span class="sxs-lookup"><span data-stu-id="2cb1b-137">Only after that should you look at the indicators relating to the server’s role in the overall Lync implementation.</span></span>

<span data-ttu-id="2cb1b-138">Начните с сбора данных о производительности KHI для всех серверов.</span><span class="sxs-lookup"><span data-stu-id="2cb1b-138">Begin by collecting KHI Performance Data for all servers.</span></span> <span data-ttu-id="2cb1b-139">Для каждой роли системы (сведения, обсуждаемые ниже в этом документе) определяют, соответствуют ли базовые системные компоненты рекомендуемым целям.</span><span class="sxs-lookup"><span data-stu-id="2cb1b-139">For each of the system roles (details discussed later in this document) determine whether the basic system components meet the recommended targets.</span></span> <span data-ttu-id="2cb1b-140">Если это не так, устраните производительность системы, а затем заново соберите данные KHI и обеспечьте работоспособность системы перед просмотром метрик, специфических для роли сервера в реализации Lync.</span><span class="sxs-lookup"><span data-stu-id="2cb1b-140">If they do not, remediate the system performance then re-collect KHI data and ensure system health before looking at the metrics specific to the server’s role in the Lync implementation.</span></span> <span data-ttu-id="2cb1b-141">Работоспособность компонента для всех ролей определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="2cb1b-141">Component health for all roles is defined as:</span></span>

  - <span data-ttu-id="2cb1b-142">Загрузка ЦП \< 80%</span><span class="sxs-lookup"><span data-stu-id="2cb1b-142">CPU Utilization \< 80%</span></span>

  - <span data-ttu-id="2cb1b-143">СР. объем записи на диск ( \< 10 мс)</span><span class="sxs-lookup"><span data-stu-id="2cb1b-143">Avg. Disk Write \< 10 ms</span></span>

  - <span data-ttu-id="2cb1b-144">СР. объем чтения на диске: \< 10 мс</span><span class="sxs-lookup"><span data-stu-id="2cb1b-144">Avg. Disk Read \< 10 ms</span></span>

  - <span data-ttu-id="2cb1b-145">Доступная память \> 20% всего системы (МБ)</span><span class="sxs-lookup"><span data-stu-id="2cb1b-145">Available memory \>20% System Total MB</span></span>

  - <span data-ttu-id="2cb1b-146">Сетевая очередь, длина \< 2</span><span class="sxs-lookup"><span data-stu-id="2cb1b-146">Network Queue Length \< 2</span></span>

  - <span data-ttu-id="2cb1b-147">Отброшенные пакеты (входящие и исходящие) = 0</span><span class="sxs-lookup"><span data-stu-id="2cb1b-147">Discarded Packets (in / out) = 0</span></span>

</div>

<span id="Glossary"></span>

<div>

## <a name="glossary"></a><span data-ttu-id="2cb1b-148">Глоссарий</span><span class="sxs-lookup"><span data-stu-id="2cb1b-148">Glossary</span></span>

<span data-ttu-id="2cb1b-149">В этом афише используются следующие термины и аббревиатуры.</span><span class="sxs-lookup"><span data-stu-id="2cb1b-149">The following terms and acronyms are used in this poster:</span></span>

<span data-ttu-id="2cb1b-150">КАК MCU = одноэлементный управляющий блок с общим доступом к приложениям</span><span class="sxs-lookup"><span data-stu-id="2cb1b-150">AS MCU = Application Sharing Multi-point Control Unit</span></span>

<span data-ttu-id="2cb1b-151">AV MCU = аудио/видео MCU</span><span class="sxs-lookup"><span data-stu-id="2cb1b-151">AV MCU = Audio/Video MCU</span></span>

<span data-ttu-id="2cb1b-152">МГНОВЕНные сообщения MCU = MCU мгновенных сообщений</span><span class="sxs-lookup"><span data-stu-id="2cb1b-152">IM MCU = Instant Messaging MCU</span></span>

<span data-ttu-id="2cb1b-153">UCWA = веб-API единой системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="2cb1b-153">UCWA = Unified Communications Web API</span></span>

<span data-ttu-id="2cb1b-154">AV Edge = прохождение аудио-или видеоизображения по краю</span><span class="sxs-lookup"><span data-stu-id="2cb1b-154">AV Edge = Traversal of audio/video via edge</span></span>

<span data-ttu-id="2cb1b-155">Проверка подлинности AV = аудио/видео</span><span class="sxs-lookup"><span data-stu-id="2cb1b-155">AV Auth = Audio/Video Authentication</span></span>

<span data-ttu-id="2cb1b-156">Стек SIP = включает основную реализацию SIP в Lync</span><span class="sxs-lookup"><span data-stu-id="2cb1b-156">SIP Stack = Contains Lync’s core SIP implementation</span></span>

<span data-ttu-id="2cb1b-157">Прокси-сервер данных = используется для проведения пограничного конференции</span><span class="sxs-lookup"><span data-stu-id="2cb1b-157">Data Proxy = Used for edge conferencing</span></span>

<span data-ttu-id="2cb1b-158">LySS = служба хранилища Lync</span><span class="sxs-lookup"><span data-stu-id="2cb1b-158">LySS = Lync Storage Service</span></span>

</div>

<span id="Front"></span>

<div>

## <a name="front-end-servers"></a><span data-ttu-id="2cb1b-159">Серверы переднего плана</span><span class="sxs-lookup"><span data-stu-id="2cb1b-159">Front-end Servers</span></span>

<span data-ttu-id="2cb1b-160">Ниже приведены рекомендуемые целевые объекты KHI, специфичные для серверов переднего плана в дополнение к основным компонентам работоспособности.</span><span class="sxs-lookup"><span data-stu-id="2cb1b-160">The following recommended KHI targets are specific to front-end servers in addition to basic component health:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2cb1b-161">Функциональная область</span><span class="sxs-lookup"><span data-stu-id="2cb1b-161">Functional area</span></span></th>
<th><span data-ttu-id="2cb1b-162">Целевые показатели</span><span class="sxs-lookup"><span data-stu-id="2cb1b-162">Target Metrics</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2cb1b-163">AS/AV/MCU ДЛЯ ОБМЕНА МГНОВЕННЫМИ СООБЩЕНИЯМИ</span><span class="sxs-lookup"><span data-stu-id="2cb1b-163">AS/AV/IM MCU</span></span></p></td>
<td><p><span data-ttu-id="2cb1b-164">Состояние работоспособности MCU &lt; 2</span><span class="sxs-lookup"><span data-stu-id="2cb1b-164">MCU Health State &lt;2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2cb1b-165">Веб-компоненты</span><span class="sxs-lookup"><span data-stu-id="2cb1b-165">Web Components</span></span></p></td>
<td><p><span data-ttu-id="2cb1b-166">Превышено время ожидания рекламы для расширения списка рассылки &lt; 0</span><span class="sxs-lookup"><span data-stu-id="2cb1b-166">Distribution List expansion AD timeouts &lt;0</span></span></p>
<p><span data-ttu-id="2cb1b-167">Ошибки ABWQ = 0</span><span class="sxs-lookup"><span data-stu-id="2cb1b-167">ABWQ failures = 0</span></span></p>
<p><span data-ttu-id="2cb1b-168">Ошибки LIS = 0</span><span class="sxs-lookup"><span data-stu-id="2cb1b-168">LIS failures = 0</span></span></p>
<p><span data-ttu-id="2cb1b-169">Ошибки проверки подлинности &lt; 1/с</span><span class="sxs-lookup"><span data-stu-id="2cb1b-169">Authentication Errors &lt; 1/sec</span></span></p>
<p><span data-ttu-id="2cb1b-170">Отвергнуто запросов ASP.NET V4 = 0</span><span class="sxs-lookup"><span data-stu-id="2cb1b-170">ASP.NET v4 Requests Rejected = 0</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2cb1b-171">Стек SIP</span><span class="sxs-lookup"><span data-stu-id="2cb1b-171">SIP Stack</span></span></p></td>
<td><p><span data-ttu-id="2cb1b-172">СР. обработка входящих сообщений &lt; 1 с</span><span class="sxs-lookup"><span data-stu-id="2cb1b-172">Avg. Incoming Message Processing &lt; 1 sec</span></span></p>
<p><span data-ttu-id="2cb1b-173">Отброшено входящих ответов &lt; 1 из-за отброшенных входящих запросов &lt; (1 за секунду)</span><span class="sxs-lookup"><span data-stu-id="2cb1b-173">Incoming Responses Dropped &lt; 1/sec Incoming Requests Dropped &lt; 1/sec</span></span></p>
<p><span data-ttu-id="2cb1b-174">Задержка очереди &lt; 100 мсек</span><span class="sxs-lookup"><span data-stu-id="2cb1b-174">Queue Latency &lt; 100 ms</span></span></p>
<p><span data-ttu-id="2cb1b-175">Sproc задержка &lt; 100 мсек</span><span class="sxs-lookup"><span data-stu-id="2cb1b-175">Sproc Latency &lt; 100 ms</span></span></p>
<p><span data-ttu-id="2cb1b-176">Регулируемые запросы = 0</span><span class="sxs-lookup"><span data-stu-id="2cb1b-176">Throttled Requests = 0</span></span></p>
<p><span data-ttu-id="2cb1b-177">Ошибки проверки подлинности &lt; 1/с</span><span class="sxs-lookup"><span data-stu-id="2cb1b-177">Authentication Errors &lt; 1/sec</span></span></p>
<p><span data-ttu-id="2cb1b-178">Превышение времени ожидания для входящих сообщений &lt; 2</span><span class="sxs-lookup"><span data-stu-id="2cb1b-178">Incoming Messages Timed Out &lt; 2</span></span></p>
<p><span data-ttu-id="2cb1b-179">Среднее входящее сообщение на хранение ( &lt; 1 с)</span><span class="sxs-lookup"><span data-stu-id="2cb1b-179">Avg. Incoming Message Hold &lt; 1 sec</span></span></p>
<p><span data-ttu-id="2cb1b-180">Соединения с управляемым потоком &lt; 2</span><span class="sxs-lookup"><span data-stu-id="2cb1b-180">Flow Controlled Connections &lt; 2</span></span></p>
<p><span data-ttu-id="2cb1b-181">Средняя задержка очереди исходящих сообщений &lt; 2 сек</span><span class="sxs-lookup"><span data-stu-id="2cb1b-181">Avg. Out Queue Delay &lt; 2 sec</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2cb1b-182">LySS</span><span class="sxs-lookup"><span data-stu-id="2cb1b-182">LySS</span></span></p></td>
<td><p><span data-ttu-id="2cb1b-183">% места, занятого базой данных службы хранилища &lt; 80</span><span class="sxs-lookup"><span data-stu-id="2cb1b-183">% of space used by Storage Service DB &lt; 80</span></span></p>
<p><span data-ttu-id="2cb1b-184"># ошибки репликации реплики = 0</span><span class="sxs-lookup"><span data-stu-id="2cb1b-184"># of replica replication failures = 0</span></span></p>
<p><span data-ttu-id="2cb1b-185"># событий потери данных = 0</span><span class="sxs-lookup"><span data-stu-id="2cb1b-185"># of data loss events = 0</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2cb1b-186">Microsoft</span><span class="sxs-lookup"><span data-stu-id="2cb1b-186">SQL</span></span></p></td>
<td><p><span data-ttu-id="2cb1b-187">Ожидаемый срок жизни страницы &gt; 300 сек.</span><span class="sxs-lookup"><span data-stu-id="2cb1b-187">Page life expectancy &gt; 300 Sec.</span></span></p>
<p><span data-ttu-id="2cb1b-188">Пакетных запросов в секунду &lt; 2500</span><span class="sxs-lookup"><span data-stu-id="2cb1b-188">Batch requests / sec &lt; 2500</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<span id="BackEnd"></span>

<div>

## <a name="backend-sql-servers"></a><span data-ttu-id="2cb1b-189">Внутренние серверы SQL Server</span><span class="sxs-lookup"><span data-stu-id="2cb1b-189">Backend SQL Servers</span></span>

<span data-ttu-id="2cb1b-190">Ниже приведены рекомендуемые целевые объекты KHI, специфичные для серверов SQL Server, в дополнение к основным компонентам работоспособности.</span><span class="sxs-lookup"><span data-stu-id="2cb1b-190">The following recommended KHI targets are specific to SQL servers in addition to basic component health:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2cb1b-191">Функциональная область</span><span class="sxs-lookup"><span data-stu-id="2cb1b-191">Functional area</span></span></th>
<th><span data-ttu-id="2cb1b-192">Целевые показатели</span><span class="sxs-lookup"><span data-stu-id="2cb1b-192">Target Metrics</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2cb1b-193">Microsoft</span><span class="sxs-lookup"><span data-stu-id="2cb1b-193">SQL</span></span></p></td>
<td><p><span data-ttu-id="2cb1b-194">Ожидаемый срок жизни страницы &gt; 300 сек.</span><span class="sxs-lookup"><span data-stu-id="2cb1b-194">Page life expectancy &gt; 300 Sec.</span></span></p>
<p><span data-ttu-id="2cb1b-195">Пакетных запросов в секунду &lt; 2500</span><span class="sxs-lookup"><span data-stu-id="2cb1b-195">Batch requests / sec &lt; 2500</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<span id="Mediation"></span>

<div>

## <a name="mediation-servers"></a><span data-ttu-id="2cb1b-196">Серверы-посредники</span><span class="sxs-lookup"><span data-stu-id="2cb1b-196">Mediation Servers</span></span>

<span data-ttu-id="2cb1b-197">Следующие целевые объекты KHI относятся к серверам для устранения проблем в дополнение к основным работоспособности компонентов:</span><span class="sxs-lookup"><span data-stu-id="2cb1b-197">The following recommended KHI targets are specific to mediation servers in addition to basic component health:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2cb1b-198">Функциональная область</span><span class="sxs-lookup"><span data-stu-id="2cb1b-198">Functional area</span></span></th>
<th><span data-ttu-id="2cb1b-199">Целевые показатели</span><span class="sxs-lookup"><span data-stu-id="2cb1b-199">Target Metrics</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2cb1b-200">Служба сервера обновлений</span><span class="sxs-lookup"><span data-stu-id="2cb1b-200">Mediation Server Service</span></span></p></td>
<td><p><span data-ttu-id="2cb1b-201">Индекс сбоя при загрузке = 0</span><span class="sxs-lookup"><span data-stu-id="2cb1b-201">Load Call Failure Index = 0</span></span></p>
<p><span data-ttu-id="2cb1b-202">Неудачные вызовы из-за прокси-сервера &lt; 10</span><span class="sxs-lookup"><span data-stu-id="2cb1b-202">Failed Calls due to Proxy &lt;10</span></span></p>
<p><span data-ttu-id="2cb1b-203">Неудачные звонки из-за шлюза &lt; 10</span><span class="sxs-lookup"><span data-stu-id="2cb1b-203">Failed Calls due to Gateway &lt;10</span></span></p>
<p><span data-ttu-id="2cb1b-204">Отвергнуто звонков (входящих и исходящим) = 0</span><span class="sxs-lookup"><span data-stu-id="2cb1b-204">Calls (in or out) rejected = 0</span></span></p>
<p><span data-ttu-id="2cb1b-205">Отсутствующие кандидаты на мультимедиа = 0</span><span class="sxs-lookup"><span data-stu-id="2cb1b-205">Media Candidates missing = 0</span></span></p>
<p><span data-ttu-id="2cb1b-206">Ошибки проверки подключения к мультимедиа = 0</span><span class="sxs-lookup"><span data-stu-id="2cb1b-206">Media Connectivity Check Failures = 0</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<span id="Edge"></span>

<div>

## <a name="edge-servers"></a><span data-ttu-id="2cb1b-207">пограничные серверы</span><span class="sxs-lookup"><span data-stu-id="2cb1b-207">Edge Servers</span></span>

<span data-ttu-id="2cb1b-208">Ниже приведены рекомендованные целевые объекты KHI, специфичные для пограничного сервера, помимо базовой работоспособности компонентов.</span><span class="sxs-lookup"><span data-stu-id="2cb1b-208">The following recommended KHI targets are specific to edge servers in addition to basic component health:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2cb1b-209">Функциональная область</span><span class="sxs-lookup"><span data-stu-id="2cb1b-209">Functional area</span></span></th>
<th><span data-ttu-id="2cb1b-210">Целевые показатели</span><span class="sxs-lookup"><span data-stu-id="2cb1b-210">Target Metrics</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2cb1b-211">Проверка подлинности AV</span><span class="sxs-lookup"><span data-stu-id="2cb1b-211">AV Auth</span></span></p></td>
<td><p><span data-ttu-id="2cb1b-212">Недопустимых запросов &lt; 20/сек</span><span class="sxs-lookup"><span data-stu-id="2cb1b-212">Bad Requests &lt; 20/sec</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2cb1b-213">Край AV</span><span class="sxs-lookup"><span data-stu-id="2cb1b-213">AV Edge</span></span></p></td>
<td><p><span data-ttu-id="2cb1b-214">Проверка подлинности: &lt; 20 за секунду</span><span class="sxs-lookup"><span data-stu-id="2cb1b-214">Auth. Failures &lt;20/sec</span></span></p>
<p><span data-ttu-id="2cb1b-215">Ошибок выделения &lt; 20/с</span><span class="sxs-lookup"><span data-stu-id="2cb1b-215">Allocation Failures &lt;20/sec</span></span></p>
<p><span data-ttu-id="2cb1b-216">Отброшено пакетов &lt; 300/сек</span><span class="sxs-lookup"><span data-stu-id="2cb1b-216">Packets Dropped &lt;300/sec</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2cb1b-217">Прокси-сервер данных</span><span class="sxs-lookup"><span data-stu-id="2cb1b-217">Data Proxy</span></span></p></td>
<td><p><span data-ttu-id="2cb1b-218">Отрегулированные соединения с сервером &lt; 3</span><span class="sxs-lookup"><span data-stu-id="2cb1b-218">Throttled Server connections &lt; 3</span></span></p>
<p><span data-ttu-id="2cb1b-219">Система регулирует &lt; 1</span><span class="sxs-lookup"><span data-stu-id="2cb1b-219">System is Throttling &lt;1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2cb1b-220">Стек SIP</span><span class="sxs-lookup"><span data-stu-id="2cb1b-220">SIP Stack</span></span></p></td>
<td><p><span data-ttu-id="2cb1b-221">Число подключений, отброшенных до &lt; 1</span><span class="sxs-lookup"><span data-stu-id="2cb1b-221">Connections over limit dropped &lt; 1</span></span></p>
<p><span data-ttu-id="2cb1b-222">Отправляет время ожидания в течение &lt; 10</span><span class="sxs-lookup"><span data-stu-id="2cb1b-222">Sends timed out &lt;10</span></span></p>
<p><span data-ttu-id="2cb1b-223">Подключения, управляемые потоком &lt; 100</span><span class="sxs-lookup"><span data-stu-id="2cb1b-223">Flow Controlled Connections &lt;100</span></span></p>
<p><span data-ttu-id="2cb1b-224">Отброшено входящих запросов &lt; (1 за секунду)</span><span class="sxs-lookup"><span data-stu-id="2cb1b-224">Incoming requests dropped &lt; 1/sec</span></span></p>
<p><span data-ttu-id="2cb1b-225">СР. Обработка сообщений &lt; 3 с</span><span class="sxs-lookup"><span data-stu-id="2cb1b-225">Avg. Message Processing &lt; 3 sec</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a><span data-ttu-id="2cb1b-226">См. также</span><span class="sxs-lookup"><span data-stu-id="2cb1b-226">See Also</span></span>


[<span data-ttu-id="2cb1b-227">Сетевое руководство по Lync Server</span><span class="sxs-lookup"><span data-stu-id="2cb1b-227">Lync Server Networking Guide</span></span>](https://go.microsoft.com/fwlink/p/?linkid=390677)  
[<span data-ttu-id="2cb1b-228">Индикаторы работоспособности ключа: основы обслуживания работоспособных серверов Lync</span><span class="sxs-lookup"><span data-stu-id="2cb1b-228">Key Health Indicators: The Foundation for Maintaining Healthy Lync Servers</span></span>](https://go.microsoft.com/fwlink/?linkid=391838)  
[<span data-ttu-id="2cb1b-229">Методология качества звонков Lync</span><span class="sxs-lookup"><span data-stu-id="2cb1b-229">Lync Call Quality Methodology</span></span>](https://go.microsoft.com/fwlink/?linkid=391841)  
  

<span data-ttu-id="2cb1b-230"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2cb1b-230"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

