---
title: Интерпретация результатов
description: Интерпретация результатов.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Interpreting the Results
ms:assetid: dd7f199f-7075-4d88-bb84-49a7e05eb593
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945608(v=OCS.15)
ms:contentKeyID: 51541433
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b8342a1ec1e15e42852fc5293f87342e98587a60
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443176"
---
# <a name="interpreting-the-results"></a><span data-ttu-id="45618-103">Интерпретация результатов</span><span class="sxs-lookup"><span data-stu-id="45618-103">Interpreting the Results</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="45618-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="45618-104">

<span> </span></span></span>

<span data-ttu-id="45618-105">_**Тема последнего изменения:** 2013-02-24_</span><span class="sxs-lookup"><span data-stu-id="45618-105">_**Topic Last Modified:** 2013-02-24_</span></span>

<span data-ttu-id="45618-106">Инструмент Lync Server 2013 (LyncPerfTool.exe) имеет множество счетчиков, которые можно использовать для понимания того, что делает клиент и при возникновении проблем.</span><span class="sxs-lookup"><span data-stu-id="45618-106">The Lync Server 2013 Stress and Performance Tool (LyncPerfTool.exe) has many counters that you can use to understand what the client is doing and whether it is encountering issues.</span></span>

<div>

## <a name="client-counters"></a><span data-ttu-id="45618-107">Счетчики клиента</span><span class="sxs-lookup"><span data-stu-id="45618-107">Client Counters</span></span>

<span data-ttu-id="45618-108">Каждый запущенный экземпляр LyncPerfTool.exe имеет отдельный экземпляр счетчиков.</span><span class="sxs-lookup"><span data-stu-id="45618-108">Each instance of LyncPerfTool.exe that is running has a separate instance of the counters.</span></span> <span data-ttu-id="45618-109">Каждый экземпляр именуется ИДЕНТИФИКАТОРом процесса.</span><span class="sxs-lookup"><span data-stu-id="45618-109">Each instance is named by its process ID.</span></span>

<span data-ttu-id="45618-110">Если клиенты перегружены, могут возникать проблемы.</span><span class="sxs-lookup"><span data-stu-id="45618-110">If the clients are overloaded, issues can occur.</span></span> <span data-ttu-id="45618-111">Чтобы предотвратить эти проблемы, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="45618-111">To prevent these issues, do the following:</span></span>

1.  <span data-ttu-id="45618-112">Отслеживайте ресурсы ЦП и использование памяти на клиентских компьютерах.</span><span class="sxs-lookup"><span data-stu-id="45618-112">Monitor the CPU and the memory usage on the client computers.</span></span> <span data-ttu-id="45618-113">Если ЦП постоянно превышает 90%, сократите количество пользователей.</span><span class="sxs-lookup"><span data-stu-id="45618-113">If the CPU is consistently above 90 percent, reduce the number of users.</span></span>

2.  <span data-ttu-id="45618-114">Если объем памяти велик, вы можете столкнуться с проблемами, если файл подкачки слишком мал.</span><span class="sxs-lookup"><span data-stu-id="45618-114">If the memory footprint is high, you could run into issues if the page file is not big enough.</span></span> <span data-ttu-id="45618-115">Убедитесь, что зарядка фиксации не достигнута на компьютере.</span><span class="sxs-lookup"><span data-stu-id="45618-115">Verify that the Commit Charge is not hitting the limit on the computer.</span></span> <span data-ttu-id="45618-116">Если вы используете ограничения памяти, рекомендуем увеличить размер файла подкачки или уменьшить количество пользователей.</span><span class="sxs-lookup"><span data-stu-id="45618-116">If you are running into memory limits, consider increasing the page file size or reducing the number of users</span></span>

<span data-ttu-id="45618-117">В приведенных ниже таблицах перечислены ключевые счетчики производительности LyncPerfTool.</span><span class="sxs-lookup"><span data-stu-id="45618-117">The following tables list the key LyncPerfTool performance counters.</span></span>

<span data-ttu-id="45618-118">**Общие сведения**</span><span class="sxs-lookup"><span data-stu-id="45618-118">**General Information**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="45618-119"><strong>Счетчик производительности</strong></span><span class="sxs-lookup"><span data-stu-id="45618-119"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="45618-120"><strong>Описание</strong></span><span class="sxs-lookup"><span data-stu-id="45618-120"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="45618-121">Время, потраченное на минуты</span><span class="sxs-lookup"><span data-stu-id="45618-121">Time Spent in Minutes</span></span></p></td>
<td><p><span data-ttu-id="45618-122">Время, потраченное с момента запуска процесса.</span><span class="sxs-lookup"><span data-stu-id="45618-122">Time spent since the process was started.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45618-123">Активные конечные точки</span><span class="sxs-lookup"><span data-stu-id="45618-123">Active Endpoints</span></span></p></td>
<td><p><span data-ttu-id="45618-124">Количество конечных точек, которые в настоящее время подключены к серверу.</span><span class="sxs-lookup"><span data-stu-id="45618-124">Number of endpoints currently connected to the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45618-125">Неудачные попытки входа</span><span class="sxs-lookup"><span data-stu-id="45618-125">Failed Logons</span></span></p></td>
<td><p><span data-ttu-id="45618-126">Общее количество ошибок входа в конечную точку.</span><span class="sxs-lookup"><span data-stu-id="45618-126">Total number of endpoint sign-in failures.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45618-127">Попытки входа</span><span class="sxs-lookup"><span data-stu-id="45618-127">Logon Attempts</span></span></p></td>
<td><p><span data-ttu-id="45618-128">Общее количество попыток входа в конечную точку.</span><span class="sxs-lookup"><span data-stu-id="45618-128">Total number of endpoint sign-in attempts.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45618-129">Конечные точки отключены</span><span class="sxs-lookup"><span data-stu-id="45618-129">Endpoints Disconnected</span></span></p></td>
<td><p><span data-ttu-id="45618-130">Общее количество отключенных конечных точек.</span><span class="sxs-lookup"><span data-stu-id="45618-130">Total number of endpoints that have been disconnected.</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="45618-131">**Сведения о присутствии**</span><span class="sxs-lookup"><span data-stu-id="45618-131">**Presence Information**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="45618-132"><strong>Счетчик производительности</strong></span><span class="sxs-lookup"><span data-stu-id="45618-132"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="45618-133"><strong>Описание</strong></span><span class="sxs-lookup"><span data-stu-id="45618-133"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="45618-134">Звонки SetPresence</span><span class="sxs-lookup"><span data-stu-id="45618-134">SetPresence Calls</span></span></p></td>
<td><p><span data-ttu-id="45618-135">Общее количество попыток изменения присутствия.</span><span class="sxs-lookup"><span data-stu-id="45618-135">Total number of presence change attempts.</span></span> <span data-ttu-id="45618-136">Сведения о различных типах изменений присутствия можно найти в разделе SetPresence (тип присутствия), который вызывает счетчик производительности.</span><span class="sxs-lookup"><span data-stu-id="45618-136">For different types of presence changes, see the SetPresence (Presence Type) Calls Performance Counter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45618-137">NNN ответов для SetPresence</span><span class="sxs-lookup"><span data-stu-id="45618-137">NNN Responses for SetPresence</span></span></p></td>
<td><p><span data-ttu-id="45618-138">Общее количество кодов ответов NNN, полученных с сервера.</span><span class="sxs-lookup"><span data-stu-id="45618-138">Total number of nnn response codes received from the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45618-139">Вызовы при присутствии</span><span class="sxs-lookup"><span data-stu-id="45618-139">GetPresence Calls</span></span></p></td>
<td><p><span data-ttu-id="45618-140">Общее количество попыток получения запросов на присутствие.</span><span class="sxs-lookup"><span data-stu-id="45618-140">Total number of get presence request attempts.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45618-141">NNN ответов для воздля присутствия</span><span class="sxs-lookup"><span data-stu-id="45618-141">NNN Responses for GetPresence</span></span></p></td>
<td><p><span data-ttu-id="45618-142">Общее количество кодов ответов NNN, полученных с сервера.</span><span class="sxs-lookup"><span data-stu-id="45618-142">Total number of nnn response codes received from the server.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="45618-143">**Сведения о службе адресной книги**</span><span class="sxs-lookup"><span data-stu-id="45618-143">**Address Book service Information**</span></span>

<span data-ttu-id="45618-144">В этой категории содержатся счетчики, которые используются для отслеживания файлов и запросов службы веб-книги (ABS) и запроса на обслуживание адресной книги.</span><span class="sxs-lookup"><span data-stu-id="45618-144">This category includes counters used to monitor Address Book service (ABS) file downloads and Address Book Web Query service requests.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="45618-145"><strong>Счетчик производительности</strong></span><span class="sxs-lookup"><span data-stu-id="45618-145"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="45618-146"><strong>Описание</strong></span><span class="sxs-lookup"><span data-stu-id="45618-146"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="45618-147">Попытка скачивания файлов с полными и дельта-файлами (ABS)</span><span class="sxs-lookup"><span data-stu-id="45618-147">ABS Full/Delta File Downloads Attempted</span></span></p></td>
<td><p><span data-ttu-id="45618-148">Общее количество попыток полных или Дельта запросов на скачивание файлов.</span><span class="sxs-lookup"><span data-stu-id="45618-148">Total number of full or delta file download requests attempted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45618-149">Успешное скачивание полных и дельта-файлов в формате ABS</span><span class="sxs-lookup"><span data-stu-id="45618-149">ABS Full/Delta File Downloads Succeeded</span></span></p></td>
<td><p><span data-ttu-id="45618-150">Общее количество попыток полных или Дельта запросов на скачивание файлов.</span><span class="sxs-lookup"><span data-stu-id="45618-150">Total number of full or delta file download requests attempted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45618-151">Счетчики, связанные со службами веб-запросов в адресной книге</span><span class="sxs-lookup"><span data-stu-id="45618-151">Address Book Web Query service related counters</span></span></p></td>
<td><p><span data-ttu-id="45618-152">Счетчики, связанные с загрузкой файлов в адресной книге.</span><span class="sxs-lookup"><span data-stu-id="45618-152">Address book file download related counters.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45618-153">Попытка обращения к службе ABS</span><span class="sxs-lookup"><span data-stu-id="45618-153">ABS WS Calls attempted</span></span></p></td>
<td><p><span data-ttu-id="45618-154">Общее количество попыток запросов службы веб-запросов в адресную книгу.</span><span class="sxs-lookup"><span data-stu-id="45618-154">Total number of Address Book Web Query service requests attempted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45618-155">Успешные вызовы ABS WS</span><span class="sxs-lookup"><span data-stu-id="45618-155">ABS WS Calls Succeeded</span></span></p></td>
<td><p><span data-ttu-id="45618-156">Общее количество запросов на веб-службу адресной книги, которые возвращали успешный код ответа.</span><span class="sxs-lookup"><span data-stu-id="45618-156">Total number of Address Book Web Query service requests that returned a successful response code.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45618-157">Сбой вызовов ABS WS</span><span class="sxs-lookup"><span data-stu-id="45618-157">ABS WS Calls Failed</span></span></p></td>
<td><p><span data-ttu-id="45618-158">Общее количество запросов на веб-службу адресной книги, которые возвращали код ответа об ошибке.</span><span class="sxs-lookup"><span data-stu-id="45618-158">Total number of Address Book Web Query service requests that returned an error response code.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="45618-159">**Сведения о списке рассылки (DL)**</span><span class="sxs-lookup"><span data-stu-id="45618-159">**Distribution List (DL) Information**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="45618-160"><strong>Счетчик производительности</strong></span><span class="sxs-lookup"><span data-stu-id="45618-160"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="45618-161"><strong>Описание</strong></span><span class="sxs-lookup"><span data-stu-id="45618-161"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="45618-162">Попытки звонков</span><span class="sxs-lookup"><span data-stu-id="45618-162">Calls Attempted</span></span></p></td>
<td><p><span data-ttu-id="45618-163">Общее количество предпроизведенных запросов на веб-службу расширения списка рассылки (DLX).</span><span class="sxs-lookup"><span data-stu-id="45618-163">Total number of distribution list expansion (DLX) web service requests attempted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45618-164">Успешные звонки</span><span class="sxs-lookup"><span data-stu-id="45618-164">Calls Succeeded</span></span></p></td>
<td><p><span data-ttu-id="45618-165">Общее количество запросов веб-службы DLX, которые возвращали успешный код ответа.</span><span class="sxs-lookup"><span data-stu-id="45618-165">Total number of DLX web service requests that returned a successful response code.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45618-166">Не удалось выполнить звонки</span><span class="sxs-lookup"><span data-stu-id="45618-166">Calls Failed</span></span></p></td>
<td><p><span data-ttu-id="45618-167">Общее количество запросов веб-службы DLX, которые возвращали код ответа об ошибке.</span><span class="sxs-lookup"><span data-stu-id="45618-167">Total number of DLX web service requests that returned an error response code.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="45618-168">**Основные сведения о VoIP**</span><span class="sxs-lookup"><span data-stu-id="45618-168">**VoIP Basic Information**</span></span>

<span data-ttu-id="45618-169">Счетчики производительности, указанные ниже, указаны в разделе "номера отчетов" для всех звонков по протоколу голосовой связи (VoIP), в том числе для звонков на сервер-посредник, сервер конференции, пограничный сервер, приложение группы ответа и автосекретарь конференции, если эти сценарии включены.</span><span class="sxs-lookup"><span data-stu-id="45618-169">The performance counters listed below report numbers for all Voice over IP (VoIP) calls, including calls to Mediation Server, A/V Conferencing Server, Edge Server, Response Group application, and Conference Auto Attendant, when these scenarios are enabled.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="45618-170"><strong>Счетчик производительности</strong></span><span class="sxs-lookup"><span data-stu-id="45618-170"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="45618-171"><strong>Описание</strong></span><span class="sxs-lookup"><span data-stu-id="45618-171"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="45618-172">Активных звонков</span><span class="sxs-lookup"><span data-stu-id="45618-172">Calls Active</span></span></p></td>
<td><p><span data-ttu-id="45618-173">Общее количество текущих и входящих и исходящих голосовых вызовов.</span><span class="sxs-lookup"><span data-stu-id="45618-173">Total number of incoming/outgoing voice calls ongoing currently.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45618-174">Прерванные звонки</span><span class="sxs-lookup"><span data-stu-id="45618-174">Calls Terminated</span></span></p></td>
<td><p><span data-ttu-id="45618-175">Общее количество входящих и исходящих голосовых вызовов, которые уже были прерваны.</span><span class="sxs-lookup"><span data-stu-id="45618-175">Total number of incoming/outgoing voice calls already terminated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45618-176">Отклоненные звонки</span><span class="sxs-lookup"><span data-stu-id="45618-176">Calls Declined</span></span></p></td>
<td><p><span data-ttu-id="45618-177">Общее количество отклоненных входящих голосовых вызовов.</span><span class="sxs-lookup"><span data-stu-id="45618-177">Total number of incoming voice calls declined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45618-178">Попыток входящих и исходящих звонков</span><span class="sxs-lookup"><span data-stu-id="45618-178">Incoming/Outgoing Calls Attempted</span></span></p></td>
<td><p><span data-ttu-id="45618-179">Общее количество попыток входящих и исходящих голосовых вызовов.</span><span class="sxs-lookup"><span data-stu-id="45618-179">Total number of incoming/outgoing voice calls attempted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45618-180">Входящие и исходящие вызовы установлены</span><span class="sxs-lookup"><span data-stu-id="45618-180">Incoming/Outgoing Calls Established</span></span></p></td>
<td><p><span data-ttu-id="45618-181">Общее количество установленных входящих и исходящих голосовых вызовов.</span><span class="sxs-lookup"><span data-stu-id="45618-181">Total number of incoming/outgoing voice calls established.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45618-182">Получено звонков NNN</span><span class="sxs-lookup"><span data-stu-id="45618-182">Calls Received NNN</span></span></p></td>
<td><p><span data-ttu-id="45618-183">Общее количество кодов ответов NNN, полученных с сервера.</span><span class="sxs-lookup"><span data-stu-id="45618-183">Total number of nnn response codes received from the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45618-184">Доля успешных похождения в VoIP (%)</span><span class="sxs-lookup"><span data-stu-id="45618-184">VoIP Pass Rate (%)</span></span></p></td>
<td><p><span data-ttu-id="45618-185">Общее количество попыток установленного/общего количества звонков.</span><span class="sxs-lookup"><span data-stu-id="45618-185">Total calls established/Total calls attempted.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="45618-186">**Сведения о вызове службы группы ответа**</span><span class="sxs-lookup"><span data-stu-id="45618-186">**Response Group service Call Information**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="45618-187"><strong>Счетчик производительности</strong></span><span class="sxs-lookup"><span data-stu-id="45618-187"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="45618-188"><strong>Описание</strong></span><span class="sxs-lookup"><span data-stu-id="45618-188"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="45618-189">Активных звонков</span><span class="sxs-lookup"><span data-stu-id="45618-189">Calls Active</span></span></p></td>
<td><p><span data-ttu-id="45618-190">Общее количество активных звонков в приложение группы ответа.</span><span class="sxs-lookup"><span data-stu-id="45618-190">Total number of active calls to the Response Group application.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45618-191">Попытки звонков</span><span class="sxs-lookup"><span data-stu-id="45618-191">Calls Attempted</span></span></p></td>
<td><p><span data-ttu-id="45618-192">Общее количество попыток звонков.</span><span class="sxs-lookup"><span data-stu-id="45618-192">Total number of calls attempted.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="45618-193">**Информация о звонках в мгновенных сообщениях**</span><span class="sxs-lookup"><span data-stu-id="45618-193">**Instant Messaging (IM) Call Information**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="45618-194"><strong>Счетчик производительности</strong></span><span class="sxs-lookup"><span data-stu-id="45618-194"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="45618-195"><strong>Описание</strong></span><span class="sxs-lookup"><span data-stu-id="45618-195"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="45618-196">Активных звонков</span><span class="sxs-lookup"><span data-stu-id="45618-196">Calls Active</span></span></p></td>
<td><p><span data-ttu-id="45618-197">Общее количество текущих входящих и исходящих звонков с мгновенными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="45618-197">Total number of ongoing incoming/outgoing instant messaging calls.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45618-198">Прерванные звонки</span><span class="sxs-lookup"><span data-stu-id="45618-198">Calls Terminated</span></span></p></td>
<td><p><span data-ttu-id="45618-199">Общее количество уже прерванных входящих и исходящих вызовов мгновенных сообщений.</span><span class="sxs-lookup"><span data-stu-id="45618-199">Total number of incoming/outgoing instant messaging calls already terminated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45618-200">Получено звонков NNN</span><span class="sxs-lookup"><span data-stu-id="45618-200">Calls Received NNN</span></span></p></td>
<td><p><span data-ttu-id="45618-201">Общее количество кодов ответов NNN, полученных с сервера.</span><span class="sxs-lookup"><span data-stu-id="45618-201">Total number of nnn response codes received from the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45618-202">Полученные и отправленные МГНОВЕНные сообщения</span><span class="sxs-lookup"><span data-stu-id="45618-202">IM Messages Received/Sent</span></span></p></td>
<td><p><span data-ttu-id="45618-203">Общее количество сообщений, полученных или отправленных для всех сеансов.</span><span class="sxs-lookup"><span data-stu-id="45618-203">Total number of messages received or sent for all sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45618-204">Попыток входящих и исходящих звонков</span><span class="sxs-lookup"><span data-stu-id="45618-204">Incoming/Outgoing Calls Attempted</span></span></p></td>
<td><p><span data-ttu-id="45618-205">Общее количество попыток входящих и исходящих вызовов мгновенных сообщений.</span><span class="sxs-lookup"><span data-stu-id="45618-205">Total number of incoming/outgoing instant messaging calls attempted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45618-206">Входящие и исходящие вызовы установлены</span><span class="sxs-lookup"><span data-stu-id="45618-206">Incoming/Outgoing Calls Established</span></span></p></td>
<td><p><span data-ttu-id="45618-207">Общее количество установленных звонков для входящих и исходящих мгновенных сообщений.</span><span class="sxs-lookup"><span data-stu-id="45618-207">Total number of incoming/outgoing instant message calls established.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="45618-208">**Сведения о вызовах для общего использования приложений**</span><span class="sxs-lookup"><span data-stu-id="45618-208">**App Sharing Call Information**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="45618-209"><strong>Счетчик производительности</strong></span><span class="sxs-lookup"><span data-stu-id="45618-209"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="45618-210"><strong>Описание</strong></span><span class="sxs-lookup"><span data-stu-id="45618-210"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="45618-211">Активных звонков</span><span class="sxs-lookup"><span data-stu-id="45618-211">Calls Active</span></span></p></td>
<td><p><span data-ttu-id="45618-212">Общее количество текущих входящих и исходящих вызовов для общего использования приложений.</span><span class="sxs-lookup"><span data-stu-id="45618-212">Total number of ongoing incoming/outgoing application sharing calls.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45618-213">Прерванные звонки</span><span class="sxs-lookup"><span data-stu-id="45618-213">Calls Terminated</span></span></p></td>
<td><p><span data-ttu-id="45618-214">Общее количество входящих и исходящих вызовов для общего использования приложений, которые уже завершены.</span><span class="sxs-lookup"><span data-stu-id="45618-214">Total number of incoming/outgoing application sharing calls already terminated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45618-215">Получено звонков NNN</span><span class="sxs-lookup"><span data-stu-id="45618-215">Calls Received NNN</span></span></p></td>
<td><p><span data-ttu-id="45618-216">Общее количество кодов ответов NNN, полученных с сервера.</span><span class="sxs-lookup"><span data-stu-id="45618-216">Total number of nnn response codes received from the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45618-217">Попыток входящих и исходящих звонков</span><span class="sxs-lookup"><span data-stu-id="45618-217">Incoming/Outgoing Calls Attempted</span></span></p></td>
<td><p><span data-ttu-id="45618-218">Общее количество попыток входящих и исходящих вызовов для общего использования приложений.</span><span class="sxs-lookup"><span data-stu-id="45618-218">Total number of incoming/outgoing application sharing calls attempted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45618-219">Входящие и исходящие вызовы установлены</span><span class="sxs-lookup"><span data-stu-id="45618-219">Incoming/Outgoing Calls Established</span></span></p></td>
<td><p><span data-ttu-id="45618-220">Общее количество установленных звонков входящих и исходящих приложений.</span><span class="sxs-lookup"><span data-stu-id="45618-220">Total number of incoming/outgoing application sharing calls established.</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="45618-221">**Информация о звонке CAA**</span><span class="sxs-lookup"><span data-stu-id="45618-221">**CAA Call Information**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="45618-222"><strong>Счетчик производительности</strong></span><span class="sxs-lookup"><span data-stu-id="45618-222"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="45618-223"><strong>Описание</strong></span><span class="sxs-lookup"><span data-stu-id="45618-223"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="45618-224">Активных звонков</span><span class="sxs-lookup"><span data-stu-id="45618-224">Calls Active</span></span></p></td>
<td><p><span data-ttu-id="45618-225">Общее количество входящих и исходящих телефонных сетей с открытым коммутируемым подключением (PSTN), в настоящее время используемых вами звонков.</span><span class="sxs-lookup"><span data-stu-id="45618-225">Total number of incoming/outgoing public switched telephone network (PSTN) calls ongoing currently.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45618-226">Прерванные звонки</span><span class="sxs-lookup"><span data-stu-id="45618-226">Calls Terminated</span></span></p></td>
<td><p><span data-ttu-id="45618-227">Общее количество входящих и исходящих вызовов КТСОП, которые уже были прерваны.</span><span class="sxs-lookup"><span data-stu-id="45618-227">Total number of incoming/outgoing PSTN calls already terminated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45618-228">Попыток входящих и исходящих звонков</span><span class="sxs-lookup"><span data-stu-id="45618-228">Incoming/Outgoing Calls Attempted</span></span></p></td>
<td><p><span data-ttu-id="45618-229">Общее количество попыток входящих и исходящих звонков по КТСОП.</span><span class="sxs-lookup"><span data-stu-id="45618-229">Total number of incoming/outgoing PSTN calls attempted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45618-230">Входящие и исходящие вызовы установлены</span><span class="sxs-lookup"><span data-stu-id="45618-230">Incoming/Outgoing Calls Established</span></span></p></td>
<td><p><span data-ttu-id="45618-231">Общее количество установленных входящих и исходящих звонков по КТСОП.</span><span class="sxs-lookup"><span data-stu-id="45618-231">Total number of incoming/outgoing PSTN calls established.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="45618-232">**Сведения о Конференции**</span><span class="sxs-lookup"><span data-stu-id="45618-232">**Conference Information**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="45618-233"><strong>Счетчик производительности</strong></span><span class="sxs-lookup"><span data-stu-id="45618-233"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="45618-234"><strong>Описание</strong></span><span class="sxs-lookup"><span data-stu-id="45618-234"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="45618-235">Активные конференции для обмена мгновенными сообщениями</span><span class="sxs-lookup"><span data-stu-id="45618-235">Active Instant Messaging Conferences</span></span></p></td>
<td><p><span data-ttu-id="45618-236">Общее количество текущих конференций с обменом мгновенными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="45618-236">Total number of ongoing instant messaging conferences.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45618-237">Активные аудио-и видеоконференции</span><span class="sxs-lookup"><span data-stu-id="45618-237">Active Audio/Video Conferences</span></span></p></td>
<td><p><span data-ttu-id="45618-238">Общее количество текущих голосовых и видеоконференций (A/V).</span><span class="sxs-lookup"><span data-stu-id="45618-238">Total number of ongoing audio/video (A/V) conferences.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45618-239">Активные конференции для совместного использования приложений</span><span class="sxs-lookup"><span data-stu-id="45618-239">Active Application Sharing Conferences</span></span></p></td>
<td><p><span data-ttu-id="45618-240">Общее количество текущих конференций общего обмена приложениями.</span><span class="sxs-lookup"><span data-stu-id="45618-240">Total number of ongoing application sharing conferences.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45618-241">Количество участников</span><span class="sxs-lookup"><span data-stu-id="45618-241">Number of Participants</span></span></p></td>
<td><p><span data-ttu-id="45618-242">Общее количество участников, которые в настоящее время подключены к конференциям.</span><span class="sxs-lookup"><span data-stu-id="45618-242">Total number of participants currently connected to conferences.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45618-243">Сбой расписания Конференции</span><span class="sxs-lookup"><span data-stu-id="45618-243">Conference Schedule Failure</span></span></p></td>
<td><p><span data-ttu-id="45618-244">Общее количество сбоев при попытке запланировать конференцию.</span><span class="sxs-lookup"><span data-stu-id="45618-244">Total number of failures while trying to schedule a conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45618-245">Присоединиться к Конференции с ошибкой</span><span class="sxs-lookup"><span data-stu-id="45618-245">Join Conference Failure</span></span></p></td>
<td><p><span data-ttu-id="45618-246">Общее количество сбоев при попытке подключиться к Конференции.</span><span class="sxs-lookup"><span data-stu-id="45618-246">Total number of failures while trying to connect to a conference.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="45618-247">**Счетчики клиента UCWA**</span><span class="sxs-lookup"><span data-stu-id="45618-247">**UCWA Client Counters**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="45618-248"><strong>Счетчик производительности</strong></span><span class="sxs-lookup"><span data-stu-id="45618-248"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="45618-249"><strong>Описание</strong></span><span class="sxs-lookup"><span data-stu-id="45618-249"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="45618-250">Общее количество успешных объединений IMMCU</span><span class="sxs-lookup"><span data-stu-id="45618-250">Total Number of IMMCU Joins Succeeded</span></span></p></td>
<td><p><span data-ttu-id="45618-251">Общее количество Объединенных конференций с мгновенными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="45618-251">Total number of instant messaging conferences joined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45618-252">Общее количество успешных объединений DMCU</span><span class="sxs-lookup"><span data-stu-id="45618-252">Total Number of DMCU Joins Succeeded</span></span></p></td>
<td><p><span data-ttu-id="45618-253">Общее количество Объединенных конференций/V.</span><span class="sxs-lookup"><span data-stu-id="45618-253">Total number of A/V conferences joined.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="45618-254">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="45618-254">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

