---
title: 'Lync Server 2013: счетчики производительности мобильных устройств'
description: 'Lync Server 2013: счетчики производительности мобильных устройств.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Mobility performance counters
ms:assetid: d18ed85a-673d-4695-aa3f-ac83a38ab90a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690046(v=OCS.15)
ms:contentKeyID: 48185441
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 922288f6c026f088d651dc61afdcb6ba04fed30a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425558"
---
# <a name="mobility-performance-counters-in-lync-server-2013"></a><span data-ttu-id="6c190-103">Счетчики производительности мобильных устройств в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6c190-103">Mobility performance counters in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6c190-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6c190-104">

<span> </span></span></span>

<span data-ttu-id="6c190-105">_**Тема последнего изменения:** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="6c190-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="6c190-106">В следующих таблицах перечислены имена и описания счетчиков производительности, которые можно использовать для мониторинга серверов, использующих веб-API единой системы обмена сообщениями (UCWA) и службы Lync Server 2013 MCX Mobility Service.</span><span class="sxs-lookup"><span data-stu-id="6c190-106">The following tables list the names and descriptions of performance counters that you can use to monitor servers running the Unified Communications Web API (UCWA) and the Lync Server 2013 Mcx Mobility Service.</span></span>

<span data-ttu-id="6c190-107">Имя категории для счетчиков в таблице UCWA — **LS:WEB — UCWA**.</span><span class="sxs-lookup"><span data-stu-id="6c190-107">The category name for the counters in the UCWA table is **LS:WEB – UCWA**.</span></span>

<span data-ttu-id="6c190-108">Имя категории для счетчиков в таблице службы Mcx Mobility Service — **LS:WEB — Mobile Communication Service**.</span><span class="sxs-lookup"><span data-stu-id="6c190-108">The category name for the counters in the Mcx Mobility Service table is **LS:WEB - Mobile Communication Service**.</span></span>

<div>

## <a name="performance-counters-for-ucwa"></a><span data-ttu-id="6c190-109">Счетчики производительности для UCWA</span><span class="sxs-lookup"><span data-stu-id="6c190-109">Performance Counters for UCWA</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6c190-110">Счетчик</span><span class="sxs-lookup"><span data-stu-id="6c190-110">Counter</span></span></th>
<th><span data-ttu-id="6c190-111">Описание</span><span class="sxs-lookup"><span data-stu-id="6c190-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c190-112">Active Application Count (Число активных приложений)</span><span class="sxs-lookup"><span data-stu-id="6c190-112">Active Application Count</span></span></p></td>
<td><p><span data-ttu-id="6c190-113">Текущее число приложений</span><span class="sxs-lookup"><span data-stu-id="6c190-113">The current number of applications</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c190-114">Active Application Sharing Modality Count (Число активных модальностей общего доступа к приложениям)</span><span class="sxs-lookup"><span data-stu-id="6c190-114">Active Application Sharing Modality Count</span></span></p></td>
<td><p><span data-ttu-id="6c190-115">Текущее число модальностей общего доступа к приложениям</span><span class="sxs-lookup"><span data-stu-id="6c190-115">The current number of Application Sharing modality</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c190-116">Active Audio Modality Count (Число активных модальностей звука)</span><span class="sxs-lookup"><span data-stu-id="6c190-116">Active Audio Modality Count</span></span></p></td>
<td><p><span data-ttu-id="6c190-117">Текущее число модальностей звука</span><span class="sxs-lookup"><span data-stu-id="6c190-117">The current number of Audio modality</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c190-118">Active Data Collaboration Modality Count (Число активных модальностей совместной работы с данными)</span><span class="sxs-lookup"><span data-stu-id="6c190-118">Active Data Collaboration Modality Count</span></span></p></td>
<td><p><span data-ttu-id="6c190-119">Текущее число модальностей совместной работы с данными</span><span class="sxs-lookup"><span data-stu-id="6c190-119">The current number of Data Collaboration modality</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c190-120">Active Directory Photo Get Latency (ms) (Задержка получения фотографий из Active Directory (мс))</span><span class="sxs-lookup"><span data-stu-id="6c190-120">Active Directory Photo Get Latency (ms)</span></span></p></td>
<td><p><span data-ttu-id="6c190-121">Этот счетчик показывает среднее время (в миллисекундах), необходимое для получения фотографии из каталога Аctive Directory.</span><span class="sxs-lookup"><span data-stu-id="6c190-121">This counter shows the average time (in milliseconds) to retrieve a photo from active directory</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c190-122">Active Messaging Modality Count (Число активных модальностей обмена сообщениями)</span><span class="sxs-lookup"><span data-stu-id="6c190-122">Active Messaging Modality Count</span></span></p></td>
<td><p><span data-ttu-id="6c190-123">Текущее число модальностей обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="6c190-123">The current number of Messaging modality</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c190-124">Active Panoramic Video Modality Count (Число активных модальностей панорамного видео)</span><span class="sxs-lookup"><span data-stu-id="6c190-124">Active Panoramic Video Modality Count</span></span></p></td>
<td><p><span data-ttu-id="6c190-125">Текущее число модальностей панорамного видео</span><span class="sxs-lookup"><span data-stu-id="6c190-125">The current number of Panoramic Video modality</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c190-126">Active Pending Get Count (Число активных операций ожидания получения)</span><span class="sxs-lookup"><span data-stu-id="6c190-126">Active Pending Get Count</span></span></p></td>
<td><p><span data-ttu-id="6c190-127">Число активных операций ожидания получения; долгосрочные подключения к серверу</span><span class="sxs-lookup"><span data-stu-id="6c190-127">The number of currently active pending gets; long-held connections to the server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c190-128">Active Session Count (Число активных сеансов)</span><span class="sxs-lookup"><span data-stu-id="6c190-128">Active Session Count</span></span></p></td>
<td><p><span data-ttu-id="6c190-129">Текущее число конечных точек, зарегистрированных в интерфейсе UCWA, на приложение и общее число</span><span class="sxs-lookup"><span data-stu-id="6c190-129">The current number of endpoints registered in UCWA per application and total</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c190-130">Active User Instance Count (Число активных экземпляров пользователей)</span><span class="sxs-lookup"><span data-stu-id="6c190-130">Active User Instance Count</span></span></p></td>
<td><p><span data-ttu-id="6c190-131">Текущее число экземпляров пользователей</span><span class="sxs-lookup"><span data-stu-id="6c190-131">The current number of user instances</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c190-132">Active User Instances without Application (Активные экземпляры пользователей без приложения)</span><span class="sxs-lookup"><span data-stu-id="6c190-132">Active User Instances without Application</span></span></p></td>
<td><p><span data-ttu-id="6c190-133">Текущее число экземпляров пользователей без приложения</span><span class="sxs-lookup"><span data-stu-id="6c190-133">The current number of user instances without application</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c190-134">Active Video Modality Count (Число активных модальностей видео)</span><span class="sxs-lookup"><span data-stu-id="6c190-134">Active Video Modality Count</span></span></p></td>
<td><p><span data-ttu-id="6c190-135">Текущее число модальностей видео</span><span class="sxs-lookup"><span data-stu-id="6c190-135">The current number of Video modality</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c190-136">Application Creation Requests Received/Second (Получено запросов на создание приложения/с)</span><span class="sxs-lookup"><span data-stu-id="6c190-136">Application Creation Requests Received/Second</span></span></p></td>
<td><p><span data-ttu-id="6c190-137">Частота полученных запросов (в секунду) на создание приложения</span><span class="sxs-lookup"><span data-stu-id="6c190-137">The per second rate of received application creation requests</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c190-138">AS MCU Join Failures (Сбои присоединения MCU AS)</span><span class="sxs-lookup"><span data-stu-id="6c190-138">AS MCU Join Failures</span></span></p></td>
<td><p><span data-ttu-id="6c190-139">Число неудачных попыток присоединения блоков MCU AS</span><span class="sxs-lookup"><span data-stu-id="6c190-139">The number of AS MCU Join Failures</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c190-140">AV MCU Join Failures (Сбои присоединения MCU AV)</span><span class="sxs-lookup"><span data-stu-id="6c190-140">AV MCU Join Failures</span></span></p></td>
<td><p><span data-ttu-id="6c190-141">Число неудачных попыток присоединения блоков MCU (AV)</span><span class="sxs-lookup"><span data-stu-id="6c190-141">The number of AV MCU Join Failures</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c190-142">Average Application Startup Time (ms) (Среднее время загрузки приложения (мс))</span><span class="sxs-lookup"><span data-stu-id="6c190-142">Average Application Startup Time (ms)</span></span></p></td>
<td><p><span data-ttu-id="6c190-143">Среднее время загрузки приложения в миллисекундах</span><span class="sxs-lookup"><span data-stu-id="6c190-143">The average application startup time in Milliseconds</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c190-144">Average Lifetime for Session (ms) (Среднее время существования сеанса (мс))</span><span class="sxs-lookup"><span data-stu-id="6c190-144">Average Lifetime for Session (ms)</span></span></p></td>
<td><p><span data-ttu-id="6c190-145">Среднее время существования сеанса в миллисекундах (мс)</span><span class="sxs-lookup"><span data-stu-id="6c190-145">The average lifetime for a session in milliseconds</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c190-146">Data MCU Join Failures (Сбои присоединения MCU данных)</span><span class="sxs-lookup"><span data-stu-id="6c190-146">Data MCU Join Failures</span></span></p></td>
<td><p><span data-ttu-id="6c190-147">Число неудачных попыток присоединения блоков MCU данных</span><span class="sxs-lookup"><span data-stu-id="6c190-147">The number of Data MCU Join Failures</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c190-148">Exchange Contact Search Latency (ms) (Задержка поиска контакта в Exchange (мс))</span><span class="sxs-lookup"><span data-stu-id="6c190-148">Exchange Contact Search Latency (ms)</span></span></p></td>
<td><p><span data-ttu-id="6c190-149">Этот счетчик показывает среднее время (в миллисекундах), затрачиваемое на поиск контакта Exchange.</span><span class="sxs-lookup"><span data-stu-id="6c190-149">This counter shows the average time (in milliseconds) to search contact in Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c190-150">Задержка получения фотографий в формате HD из Exchange (мс)</span><span class="sxs-lookup"><span data-stu-id="6c190-150">Exchange HD Photo Get Latency (ms)</span></span></p></td>
<td><p><span data-ttu-id="6c190-151">Этот счетчик показывает среднее время (в миллисекундах), затрачиваемое на получение фотографии с сервера Exchange.</span><span class="sxs-lookup"><span data-stu-id="6c190-151">This counter shows the average time (in milliseconds) to retrieve a photo from Exchange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c190-152">Ответов HTTP 4xx/с</span><span class="sxs-lookup"><span data-stu-id="6c190-152">HTTP 4xx Responses/Second</span></span></p></td>
<td><p><span data-ttu-id="6c190-153">Частота ответов с кодом HTTP 4xx (в секунду)</span><span class="sxs-lookup"><span data-stu-id="6c190-153">The per second rate of responses with HTTP 4xx code</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c190-154">Ответов HTTP 5xx/с</span><span class="sxs-lookup"><span data-stu-id="6c190-154">HTTP 5xx Responses/Second</span></span></p></td>
<td><p><span data-ttu-id="6c190-155">Частота ответов с кодом HTTP 5xx (в секунду)</span><span class="sxs-lookup"><span data-stu-id="6c190-155">The per second rate of responses with HTTP 5xx code</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c190-156">IM MCU Join Failures (Сбои присоединения MCU IM)</span><span class="sxs-lookup"><span data-stu-id="6c190-156">IM MCU Join Failures</span></span></p></td>
<td><p><span data-ttu-id="6c190-157">Число неудачных попыток присоединения блоков MCU IM</span><span class="sxs-lookup"><span data-stu-id="6c190-157">The number of IM MCU Join Failures</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c190-158">Number of Active Directory Photo Get Failures (Число сбоев получения фотографий из Active Directory)</span><span class="sxs-lookup"><span data-stu-id="6c190-158">Number of Active Directory Photo Get Failures</span></span></p></td>
<td><p><span data-ttu-id="6c190-159">Общее число неудачных попыток получения фотографий из Active Directory</span><span class="sxs-lookup"><span data-stu-id="6c190-159">The total number of failures to retrieve photos from Active Directory</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c190-160">Number of Contact Search failures (Число сбоев поиска контактов)</span><span class="sxs-lookup"><span data-stu-id="6c190-160">Number of Contact Search failures</span></span></p></td>
<td><p><span data-ttu-id="6c190-161">Общее число неудачных попыток поиска контактов в Exchange</span><span class="sxs-lookup"><span data-stu-id="6c190-161">The total number of failures to search contacts in Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c190-162">Number of Deserialization Failures (Число сбоев десериализации)</span><span class="sxs-lookup"><span data-stu-id="6c190-162">Number of Deserialization Failures</span></span></p></td>
<td><p><span data-ttu-id="6c190-163">Общее число неудачных попыток десериализации</span><span class="sxs-lookup"><span data-stu-id="6c190-163">The total number of deserialization failures</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c190-164">Количество сбоев при получении фотографий HD</span><span class="sxs-lookup"><span data-stu-id="6c190-164">Number of HD Photo Get Failures</span></span></p></td>
<td><p><span data-ttu-id="6c190-165">Общее число неудачных попыток получения фотографий в формате HD с сервера Exchange</span><span class="sxs-lookup"><span data-stu-id="6c190-165">The total number of failures to retrieve HD photos from Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c190-166">Over The Maximum Subscriptions Per Application (Превышение максимального числа подписок на приложение)</span><span class="sxs-lookup"><span data-stu-id="6c190-166">Over The Maximum Subscriptions Per Application</span></span></p></td>
<td><p><span data-ttu-id="6c190-167">Число запросов на подписку, превышающих максимальное значение для приложения</span><span class="sxs-lookup"><span data-stu-id="6c190-167">The number of Subscription requests over the maximum allowed per application</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c190-168">Over The Maximum Subscriptions Per Batch (Превышение максимального числа подписок на пакет)</span><span class="sxs-lookup"><span data-stu-id="6c190-168">Over The Maximum Subscriptions Per Batch</span></span></p></td>
<td><p><span data-ttu-id="6c190-169">Число запросов на подписку, превышающих максимальное значение для пакета</span><span class="sxs-lookup"><span data-stu-id="6c190-169">The number of Subscription requests over the maximum allowed per batch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c190-170">Presence Subscription Failures (Сбои подписок отслеживания присутствия)</span><span class="sxs-lookup"><span data-stu-id="6c190-170">Presence Subscription Failures</span></span></p></td>
<td><p><span data-ttu-id="6c190-171">Число неудачных попыток подписаться на сведения о присутствии</span><span class="sxs-lookup"><span data-stu-id="6c190-171">The number of failures to subscribe presence</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c190-172">Registering Endpoint Failures (Сбои регистрации конечных точек)</span><span class="sxs-lookup"><span data-stu-id="6c190-172">Registering Endpoint Failures</span></span></p></td>
<td><p><span data-ttu-id="6c190-173">Число сбоев регистрации конечных точек</span><span class="sxs-lookup"><span data-stu-id="6c190-173">The number of failures to register endpoints</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c190-174">Requests Received/Second (Полученных запросов/с)</span><span class="sxs-lookup"><span data-stu-id="6c190-174">Requests Received/Second</span></span></p></td>
<td><p><span data-ttu-id="6c190-175">Частота полученных запросов (в секунду)</span><span class="sxs-lookup"><span data-stu-id="6c190-175">The per second rate of received requests</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c190-176">Requests Succeeded/Second (Успешных запросов/с)</span><span class="sxs-lookup"><span data-stu-id="6c190-176">Requests Succeeded/Second</span></span></p></td>
<td><p><span data-ttu-id="6c190-177">Частота успешных запросов (в секунду) (коды ответов HTTP 2xx/3xx)</span><span class="sxs-lookup"><span data-stu-id="6c190-177">The per second rate of successful requests (HTTP 2xx/3xx response codes)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c190-178">Succeeded Create Application Requests/Second (Успешных запросов на создание приложений/с)</span><span class="sxs-lookup"><span data-stu-id="6c190-178">Succeeded Create Application Requests/Second</span></span></p></td>
<td><p><span data-ttu-id="6c190-179">Частота успешных запросов (в секунду) на создание приложения</span><span class="sxs-lookup"><span data-stu-id="6c190-179">The per second rate of successful application creation requests</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c190-180">Timed Out Pending Get Count (Число ожидающих операций получения с истекшим временем ожидания)</span><span class="sxs-lookup"><span data-stu-id="6c190-180">Timed Out Pending Get Count</span></span></p></td>
<td><p><span data-ttu-id="6c190-181">Число ожидающих операций получения с истекшим временем ожидания</span><span class="sxs-lookup"><span data-stu-id="6c190-181">The number of pending gets that timed out</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c190-182">Total Application Creation Requests Received (Всего полученных запросов на создание приложений)</span><span class="sxs-lookup"><span data-stu-id="6c190-182">Total Application Creation Requests Received</span></span></p></td>
<td><p><span data-ttu-id="6c190-183">Общее число запросов на создание приложений, полученных с момента запуска службы</span><span class="sxs-lookup"><span data-stu-id="6c190-183">The total number of application creation requests received since the service was started</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c190-184">Всего ответов HTTP 4xx</span><span class="sxs-lookup"><span data-stu-id="6c190-184">Total HTTP 4xx Responses</span></span></p></td>
<td><p><span data-ttu-id="6c190-185">Общее число ответов HTTP 4xx</span><span class="sxs-lookup"><span data-stu-id="6c190-185">The total number of HTTP 4xx responses</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c190-186">Всего отчетов HTTP 5xx</span><span class="sxs-lookup"><span data-stu-id="6c190-186">Total HTTP 5xx Responses</span></span></p></td>
<td><p><span data-ttu-id="6c190-187">Общее число ответов HTTP 5xx</span><span class="sxs-lookup"><span data-stu-id="6c190-187">The total number of HTTP 5xx responses</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c190-188">Total Requests received on the Command Channel (Всего запросов, полученных по каналу управления)</span><span class="sxs-lookup"><span data-stu-id="6c190-188">Total Requests Received on the Command Channel</span></span></p></td>
<td><p><span data-ttu-id="6c190-189">Общее число запросов, полученных по каналу управления</span><span class="sxs-lookup"><span data-stu-id="6c190-189">The total number of requests received on the command channel</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c190-190">Total Requests Succeeded (Всего успешных запросов)</span><span class="sxs-lookup"><span data-stu-id="6c190-190">Total Requests Succeeded</span></span></p></td>
<td><p><span data-ttu-id="6c190-191">Общее число успешных запросов</span><span class="sxs-lookup"><span data-stu-id="6c190-191">The total number of requests that succeeded</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c190-192">Total Sessions Initiated (Всего запущенных сеансов)</span><span class="sxs-lookup"><span data-stu-id="6c190-192">Total Sessions Initiated</span></span></p></td>
<td><p><span data-ttu-id="6c190-193">Общее число сеансов, запущенных с момента запуска службы</span><span class="sxs-lookup"><span data-stu-id="6c190-193">The total number of sessions that were initiated since the service was started</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c190-194">Total Sessions Terminated Because of User Idle Timeout (Всего сеансов, завершенных из-за таймаута бездействия)</span><span class="sxs-lookup"><span data-stu-id="6c190-194">Total Sessions Terminated Because of Idle Timeout</span></span></p></td>
<td><p><span data-ttu-id="6c190-195">Общее число сеансов, которые были завершены из-за истечения времени ожидания в режиме бездействия пользователя</span><span class="sxs-lookup"><span data-stu-id="6c190-195">The total number of sessions that were terminated because of user idle timeout</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c190-196">Total Throttled Applications (Всего приложений, к которым применяется регулирование)</span><span class="sxs-lookup"><span data-stu-id="6c190-196">Total Throttled Applications</span></span></p></td>
<td><p><span data-ttu-id="6c190-197">Число приложений, к которым применяется регулирование</span><span class="sxs-lookup"><span data-stu-id="6c190-197">The number of throttled applications</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div id="sectionSection1" class="section">

### <a name="performance-counters-for-mcx-mobility-service"></a><span data-ttu-id="6c190-198">Счетчики производительности для службы Mcx Mobility Service</span><span class="sxs-lookup"><span data-stu-id="6c190-198">Performance Counters for Mcx Mobility Service</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6c190-199">Счетчик</span><span class="sxs-lookup"><span data-stu-id="6c190-199">Counter</span></span></th>
<th><span data-ttu-id="6c190-200">Описание</span><span class="sxs-lookup"><span data-stu-id="6c190-200">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c190-201">Average Lifetime for a Session in Milliseconds (Среднее время существования сеанса в миллисекундах)</span><span class="sxs-lookup"><span data-stu-id="6c190-201">Average Lifetime for a Session in Milliseconds</span></span></p></td>
<td><p><span data-ttu-id="6c190-202">Среднее время существования сеанса в миллисекундах (мс)</span><span class="sxs-lookup"><span data-stu-id="6c190-202">The average lifetime for a session in milliseconds</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c190-203">Current Push Notification Subscriptions (Текущие подписки на push-уведомления)</span><span class="sxs-lookup"><span data-stu-id="6c190-203">Current Push Notification Subscriptions</span></span></p></td>
<td><p><span data-ttu-id="6c190-p101">Текущее число подписок на push-уведомления. Это число вместе с счетчиком текущих активных сеансов представляет подмножество текущих активных сеансов, зарегистрированных для устройств Windows Mobile или iPhone.</span><span class="sxs-lookup"><span data-stu-id="6c190-p101">The current number of push notification subscriptions. This number, in conjunction with Currently Active Session Count, represents the subset of currently active sessions that are registered for Windows Mobile or iPhone devices.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c190-206">Currently Active Network Timeout Poll Count (Число текущих активных опросов времени ожидания сети)</span><span class="sxs-lookup"><span data-stu-id="6c190-206">Currently Active Network Timeout Poll Count</span></span></p></td>
<td><p><span data-ttu-id="6c190-207">Число опросов сети с истекшим временем ожидания</span><span class="sxs-lookup"><span data-stu-id="6c190-207">The number of network polls that timed out</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c190-208">Currently Active Poll Count (Число активных опросов)</span><span class="sxs-lookup"><span data-stu-id="6c190-208">Currently Active Poll Count</span></span></p></td>
<td><p><span data-ttu-id="6c190-209">Число активных опросов (долгосрочные подключения к серверу)</span><span class="sxs-lookup"><span data-stu-id="6c190-209">The number of currently active polls (long-held connections to the server)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c190-210">Currently Active Session Count (Число текущих активных сеансов)</span><span class="sxs-lookup"><span data-stu-id="6c190-210">Currently Active Session Count</span></span></p></td>
<td><p><span data-ttu-id="6c190-211">Текущее число конечных точек, зарегистрированных в службе Mobility Service</span><span class="sxs-lookup"><span data-stu-id="6c190-211">Current number of endpoints registered in the Mobility Service</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c190-212">Currently Active Session Count with Active Presence Subscriptions (Число текущих активных сеансов с активными подписками на сведения о присутствии)</span><span class="sxs-lookup"><span data-stu-id="6c190-212">Currently Active Session Count with Active Presence Subscriptions</span></span></p></td>
<td><p><span data-ttu-id="6c190-213">Число текущих активных сеансов с активными подписками на сведения о присутствии</span><span class="sxs-lookup"><span data-stu-id="6c190-213">The number of currently active sessions with active presence subscriptions</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c190-214">Push Notification Requests Failed/Second (Неудачных запросов на push-уведомления/с)</span><span class="sxs-lookup"><span data-stu-id="6c190-214">Push Notification Requests Failed/Second</span></span></p></td>
<td><p><span data-ttu-id="6c190-215">Частота push-уведомлений, завершившихся сбоем (в секунду)</span><span class="sxs-lookup"><span data-stu-id="6c190-215">The per second rate of failed push notifications</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c190-216">Push Notification Requests Succeeded/Second (Успешных запросов на push-уведомления/с)</span><span class="sxs-lookup"><span data-stu-id="6c190-216">Push Notification Requests Succeeded/Second</span></span></p></td>
<td><p><span data-ttu-id="6c190-217">Частота успешно выполненных push-уведомлений (в секунду)</span><span class="sxs-lookup"><span data-stu-id="6c190-217">The per second rate of successful push notifications</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c190-218">Push Notification Requests Throttled/Second (Регулируемых запросов на push-уведомления/с)</span><span class="sxs-lookup"><span data-stu-id="6c190-218">Push Notification Requests Throttled/Second</span></span></p></td>
<td><p><span data-ttu-id="6c190-219">Частота регулируемых push-уведомлений (в секунду)</span><span class="sxs-lookup"><span data-stu-id="6c190-219">The per second rate of throttled push notifications</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c190-220">Push Notification Requests/Second (Запросов push-уведомлений/с)</span><span class="sxs-lookup"><span data-stu-id="6c190-220">Push Notification Requests/Second</span></span></p></td>
<td><p><span data-ttu-id="6c190-221">Частота отправленных push-уведомлений (в секунду)</span><span class="sxs-lookup"><span data-stu-id="6c190-221">The per second rate of sent push notifications</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c190-222">Requests Failed/Second (Неудачных запросов/с)</span><span class="sxs-lookup"><span data-stu-id="6c190-222">Requests Failed/Second</span></span></p></td>
<td><p><span data-ttu-id="6c190-223">Частота запросов, завершившихся ошибками (в секунду)</span><span class="sxs-lookup"><span data-stu-id="6c190-223">The per second rate of failed requests</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c190-224">Requests Received/Second (Полученных запросов/с)</span><span class="sxs-lookup"><span data-stu-id="6c190-224">Requests Received/Second</span></span></p></td>
<td><p><span data-ttu-id="6c190-225">Частота полученных запросов (в секунду)</span><span class="sxs-lookup"><span data-stu-id="6c190-225">The per second rate of received requests</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c190-226">Requests Rejected/Second (Отклоненных запросов/с)</span><span class="sxs-lookup"><span data-stu-id="6c190-226">Requests Rejected/Second</span></span></p></td>
<td><p><span data-ttu-id="6c190-227">Частота отклоненных запросов (в секунду)</span><span class="sxs-lookup"><span data-stu-id="6c190-227">The per second rate of rejected requests</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c190-228">Requests Succeeded/Second (Успешных запросов/с)</span><span class="sxs-lookup"><span data-stu-id="6c190-228">Requests Succeeded/Second</span></span></p></td>
<td><p><span data-ttu-id="6c190-229">Частота успешных запросов (в секунду)</span><span class="sxs-lookup"><span data-stu-id="6c190-229">The per second rate of successful requests</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c190-230">Succeeded Initiate Session Requests/Second (Успешных запросов на запуск сеанса/с)</span><span class="sxs-lookup"><span data-stu-id="6c190-230">Succeeded Initiate Session Requests/Second</span></span></p></td>
<td><p><span data-ttu-id="6c190-p102">Частота успешных запросов на получение расположения (в секунду). Запросы на запуск сеанса потребляют больше всего ресурсов ЦП на сервере. Поддерживаемая пиковая нагрузка составляет 12 сеансов в секунду. Устойчивость зависит от других нагрузок на сервере. Запуск сеанса, как правило, означает вход пользователя, с момента выхода которого из сеанса прошло довольно много времени.</span><span class="sxs-lookup"><span data-stu-id="6c190-p102">The per second rate of successful Get Location requests. Requests to initiate a session consume the most CPU on the server. Peak supported load is 12/second. Sustainability depends on other loads on the server. Initiate a session typically means a sign-in for a user that has been signed out for an extended period of time.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c190-236">Total Declined Inbound Voice Calls (Всего отклоненных входящих голосовых звонков)</span><span class="sxs-lookup"><span data-stu-id="6c190-236">Total Declined Inbound Voice Calls</span></span></p></td>
<td><p><span data-ttu-id="6c190-237">Общее число отклоненных входящих голосовых звонков</span><span class="sxs-lookup"><span data-stu-id="6c190-237">The total number of inbound voice calls that were declined</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c190-238">Total Failed Inbound Voice Calls (Всего неудачных входящих голосовых звонков)</span><span class="sxs-lookup"><span data-stu-id="6c190-238">Total Failed Inbound Voice Calls</span></span></p></td>
<td><p><span data-ttu-id="6c190-239">Общее число входящих голосовых звонков, завершившихся сбоем</span><span class="sxs-lookup"><span data-stu-id="6c190-239">The total number of inbound voice calls that failed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c190-240">Total Failed Outbound Voice Calls (Всего неудачных исходящих вызовов)</span><span class="sxs-lookup"><span data-stu-id="6c190-240">Total Failed Outbound Voice Calls</span></span></p></td>
<td><p><span data-ttu-id="6c190-241">Общее число исходящих голосовых вызовов, завершившихся сбоем</span><span class="sxs-lookup"><span data-stu-id="6c190-241">The total number of outbound voice calls that failed</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c190-242">Total number of sessions terminated by user (Общее число сеансов, завершенных пользователем)</span><span class="sxs-lookup"><span data-stu-id="6c190-242">Total number of sessions terminated by user</span></span></p></td>
<td><p><span data-ttu-id="6c190-243">Общее число сеансов, завершенных пользователями</span><span class="sxs-lookup"><span data-stu-id="6c190-243">The total number of sessions terminated by users</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c190-244">Total Push Notification Requests (Всего запросов на push-уведомления)</span><span class="sxs-lookup"><span data-stu-id="6c190-244">Total Push Notification Requests</span></span></p></td>
<td><p><span data-ttu-id="6c190-245">Общее число запросов на push-уведомления</span><span class="sxs-lookup"><span data-stu-id="6c190-245">The total number of push notification requests</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c190-246">Total Push Notification Requests Failed (Всего неудачных запросов на push-уведомления)</span><span class="sxs-lookup"><span data-stu-id="6c190-246">Total Push Notification Requests Failed</span></span></p></td>
<td><p><span data-ttu-id="6c190-247">Общее число запросов на push-уведомления, завершившихся сбоем</span><span class="sxs-lookup"><span data-stu-id="6c190-247">The total number of push notification requests that failed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c190-248">Total Push Notification Requests Succeeded (Всего успешных запросов на push-уведомления)</span><span class="sxs-lookup"><span data-stu-id="6c190-248">Total Push Notification Requests Succeeded</span></span></p></td>
<td><p><span data-ttu-id="6c190-249">Общее число успешно выполненных запросов на push-уведомления</span><span class="sxs-lookup"><span data-stu-id="6c190-249">The total number of push notification requests that were successful</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c190-250">Total Push Notification Requests Throttled (Всего ограниченных запросов на push-уведомления)</span><span class="sxs-lookup"><span data-stu-id="6c190-250">Total Push Notification Requests Throttled</span></span></p></td>
<td><p><span data-ttu-id="6c190-251">Общее число запросов на push-уведомления, которые были ограничены</span><span class="sxs-lookup"><span data-stu-id="6c190-251">The total number of push notification requests that were throttled</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c190-252">Total Requests Failed (Всего неудачных запросов)</span><span class="sxs-lookup"><span data-stu-id="6c190-252">Total Requests Failed</span></span></p></td>
<td><p><span data-ttu-id="6c190-253">Общее число запросов, завершившихся сбоем</span><span class="sxs-lookup"><span data-stu-id="6c190-253">The total number of requests that failed</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c190-254">Total Requests received on the Command Channel (Всего запросов, полученных по каналу управления)</span><span class="sxs-lookup"><span data-stu-id="6c190-254">Total Requests received on the Command Channel</span></span></p></td>
<td><p><span data-ttu-id="6c190-255">Общее число запросов, полученных по каналу управления</span><span class="sxs-lookup"><span data-stu-id="6c190-255">The total number of requests received on the command channel</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c190-256">Total Requests Rejected (Всего отклоненных запросов)</span><span class="sxs-lookup"><span data-stu-id="6c190-256">Total Requests Rejected</span></span></p></td>
<td><p><span data-ttu-id="6c190-257">Общее число отклоненных запросов</span><span class="sxs-lookup"><span data-stu-id="6c190-257">The total number of requests that were rejected</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c190-258">Total Requests Succeeded (Всего успешных запросов)</span><span class="sxs-lookup"><span data-stu-id="6c190-258">Total Requests Succeeded</span></span></p></td>
<td><p><span data-ttu-id="6c190-259">Общее число запросов, поступивших в службу Mobility Service, которые были успешно выполнены</span><span class="sxs-lookup"><span data-stu-id="6c190-259">The total number of requests made to the Mobility Service that succeeded</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c190-260">Total Session Initiated Count (Всего запущенных сеансов)</span><span class="sxs-lookup"><span data-stu-id="6c190-260">Total Session Initiated Count</span></span></p></td>
<td><p><span data-ttu-id="6c190-261">Общее число сеансов, запущенных с момента запуска службы Mobility Service</span><span class="sxs-lookup"><span data-stu-id="6c190-261">The total number of sessions that were initiated since the Mobility Service was started</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c190-262">Total Sessions Terminated Because of User Idle Timeout (Всего сеансов, завершенных из-за таймаута бездействия пользователя)</span><span class="sxs-lookup"><span data-stu-id="6c190-262">Total Sessions Terminated Because of User Idle Timeout</span></span></p></td>
<td><p><span data-ttu-id="6c190-263">Общее число сеансов, которые были завершены из-за истечения времени ожидания в режиме бездействия пользователя</span><span class="sxs-lookup"><span data-stu-id="6c190-263">The total number of sessions that were terminated because of user idle timeout</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c190-264">Total Successful Inbound Voice Calls (Всего успешных входящих голосовых вызовов)</span><span class="sxs-lookup"><span data-stu-id="6c190-264">Total Successful Inbound Voice Calls</span></span></p></td>
<td><p><span data-ttu-id="6c190-265">Общее число успешных входящих голосовых вызовов</span><span class="sxs-lookup"><span data-stu-id="6c190-265">The total number of inbound voice calls that were successful</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c190-266">Total Successful Outbound Voice Calls (Всего успешных исходящих голосовых вызовов)</span><span class="sxs-lookup"><span data-stu-id="6c190-266">Total Successful Outbound Voice Calls</span></span></p></td>
<td><p><span data-ttu-id="6c190-267">Общее число успешных исходящих голосовых вызовов</span><span class="sxs-lookup"><span data-stu-id="6c190-267">The total number of outbound voice calls that were successful</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="6c190-268">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6c190-268">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

