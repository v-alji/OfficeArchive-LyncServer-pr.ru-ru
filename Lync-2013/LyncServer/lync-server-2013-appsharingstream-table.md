---
title: 'Lync Server 2013: таблица AppSharingStream'
description: 'Таблица Lync Server 2013: AppSharingStream.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: AppSharingStream table
ms:assetid: 391490cb-d7b8-44ca-b4d1-429600da909c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204808(v=OCS.15)
ms:contentKeyID: 48183852
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b530af5b489e090e5d0d00fbb01b2b950bafbe5a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440558"
---
# <a name="appsharingstream-table-in-lync-server-2013"></a><span data-ttu-id="65afc-103">Таблица AppSharingStream в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="65afc-103">AppSharingStream table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="65afc-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="65afc-104">

<span> </span></span></span>

<span data-ttu-id="65afc-105">_**Тема последнего изменения:** 2014-02-21_</span><span class="sxs-lookup"><span data-stu-id="65afc-105">_**Topic Last Modified:** 2014-02-21_</span></span>

<span data-ttu-id="65afc-106">В таблице AppSharingStream содержатся показатели качества взаимодействия для сетевых потоков, используемых для совместного использования приложений.</span><span class="sxs-lookup"><span data-stu-id="65afc-106">The AppSharingStream table contains Quality of Experience metrics for the network streams used for application sharing.</span></span> <span data-ttu-id="65afc-107">Эта таблица введена в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="65afc-107">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="65afc-108"><strong>Столбец</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="65afc-109"><strong>Тип данных</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="65afc-110"><strong>Ключ/индекс</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="65afc-111"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="65afc-112"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-112"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-113">Датой</span><span class="sxs-lookup"><span data-stu-id="65afc-113">dateTime</span></span></p></td>
<td><p><span data-ttu-id="65afc-114">Основной, внешний</span><span class="sxs-lookup"><span data-stu-id="65afc-114">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="65afc-115">Дата и время начала сеанса.</span><span class="sxs-lookup"><span data-stu-id="65afc-115">Date and time that the session started.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65afc-116"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-116"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-117">целое</span><span class="sxs-lookup"><span data-stu-id="65afc-117">int</span></span></p></td>
<td><p><span data-ttu-id="65afc-118">Основной, внешний</span><span class="sxs-lookup"><span data-stu-id="65afc-118">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="65afc-119">Последовательный идентификатор, который используется для различения сеансов, запущенных в одну и ту же дату.</span><span class="sxs-lookup"><span data-stu-id="65afc-119">Sequential identifier used to distinguish between sessions that started on the same date and at the same time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65afc-120"><strong>MediaLineLabel</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-120"><strong>MediaLineLabel</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-121">tinyint</span><span class="sxs-lookup"><span data-stu-id="65afc-121">tinyint</span></span></p></td>
<td><p><span data-ttu-id="65afc-122">Основной, внешний</span><span class="sxs-lookup"><span data-stu-id="65afc-122">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="65afc-123">Представляет тип видеостроки, используемой в звонке.</span><span class="sxs-lookup"><span data-stu-id="65afc-123">Represents the type of video line used in the call.</span></span> <span data-ttu-id="65afc-124">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="65afc-124">Allowed values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="65afc-125">0 – звук</span><span class="sxs-lookup"><span data-stu-id="65afc-125">0 – Audio</span></span></p></li>
<li><p><span data-ttu-id="65afc-126">1 – видео</span><span class="sxs-lookup"><span data-stu-id="65afc-126">1 – Video</span></span></p></li>
<li><p><span data-ttu-id="65afc-127">2 — панорамное видео</span><span class="sxs-lookup"><span data-stu-id="65afc-127">2 – Panoramic video</span></span></p></li>
<li><p><span data-ttu-id="65afc-128">3 — общий доступ к приложениям и рабочим столам</span><span class="sxs-lookup"><span data-stu-id="65afc-128">3 –Application/Desktop Sharing</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65afc-129"><strong>StreamID</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-129"><strong>StreamID</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-130">целое</span><span class="sxs-lookup"><span data-stu-id="65afc-130">int</span></span></p></td>
<td><p><span data-ttu-id="65afc-131">Primary</span><span class="sxs-lookup"><span data-stu-id="65afc-131">Primary</span></span></p></td>
<td><p><span data-ttu-id="65afc-132">Уникальный идентификатор потока общего просмотра приложения.</span><span class="sxs-lookup"><span data-stu-id="65afc-132">Unique identifier of the application sharing stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65afc-133"><strong>JitterInterArrival</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-133"><strong>JitterInterArrival</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-134">целое</span><span class="sxs-lookup"><span data-stu-id="65afc-134">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-135">Среднее значение колебаний, зарегистрированных между прибытиями пакетов RTP.</span><span class="sxs-lookup"><span data-stu-id="65afc-135">Average jitter detected between RTP packet arrivals.</span></span> <span data-ttu-id="65afc-136">(Колебание — это мера &quot; shakiness &quot; звонка). Обычно значения с высокой степенью колебаний заключаются в результате перегруженности или перегруженного сервера мультимедиа, что приводит к искажению или потере звука.</span><span class="sxs-lookup"><span data-stu-id="65afc-136">(Jitter is a measure of the &quot;shakiness&quot; of a call.) High jitter values are typically caused by congestion or an overloaded media server, and result in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65afc-137"><strong>JitterInterArrivalMax</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-137"><strong>JitterInterArrivalMax</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-138">целое</span><span class="sxs-lookup"><span data-stu-id="65afc-138">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-139">Обнаружена максимальная колебание между поступлением пакетов RTP.</span><span class="sxs-lookup"><span data-stu-id="65afc-139">Maximum jitter detected between RTP packet arrivals.</span></span> <span data-ttu-id="65afc-140">(Колебание — это мера &quot; shakiness &quot; звонка). Обычно значения с высокой степенью колебаний заключаются в результате перегруженности или перегруженного сервера мультимедиа, что приводит к искажению или потере звука.</span><span class="sxs-lookup"><span data-stu-id="65afc-140">(Jitter is a measure of the &quot;shakiness&quot; of a call.) High jitter values are typically caused by congestion or an overloaded media server, and result in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65afc-141"><strong>RoundTrip</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-141"><strong>RoundTrip</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-142">целое</span><span class="sxs-lookup"><span data-stu-id="65afc-142">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-p105">Среднее время (в миллисекундах), необходимое для перемещения пакета Real-Time Transport Protocol в другую конечную точку и его возврата. Приемлемым считается время двусторонней передачи, равное 200 мс (или менее).</span><span class="sxs-lookup"><span data-stu-id="65afc-p105">Average amount of (in milliseconds) required for a Real-Time Transport Protocol packet to travel to another endpoint and then back. Round-trip times of 200 milliseconds or less are considered of acceptable quality.</span></span></p>
<p><span data-ttu-id="65afc-p106">Высокие значения времени двусторонней передачи могут быть обусловлены международной маршрутизацией вызовов, неправильной конфигурацией маршрутизации или перегрузкой сервера-посредника. Длительное время двусторонней передачи приводит к возникновению проблем при двусторонних аудиоразговорах в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="65afc-p106">High round-trip values can be caused by international call routing; a routing misconfiguration; or an overloaded media server. High round-trip times result in difficulties with two-way, real-time audio conversations.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65afc-147"><strong>RoundTripMax</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-147"><strong>RoundTripMax</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-148">целое</span><span class="sxs-lookup"><span data-stu-id="65afc-148">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-149">Максимальный объем (в миллисекундах), необходимый для перемещения пакета Real-Time транспортного протокола на другую конечную точку, а затем обратно.</span><span class="sxs-lookup"><span data-stu-id="65afc-149">Maximum amount of (in milliseconds) required for a Real-Time Transport Protocol packet to travel to another endpoint and then back.</span></span> <span data-ttu-id="65afc-150">Приемлемым считается время двусторонней передачи, равное 200 мс (или менее).</span><span class="sxs-lookup"><span data-stu-id="65afc-150">Round-trip times of 200 milliseconds or less are considered of acceptable quality.</span></span></p>
<p><span data-ttu-id="65afc-p108">Высокие значения времени двусторонней передачи могут быть обусловлены международной маршрутизацией вызовов, неправильной конфигурацией маршрутизации или перегрузкой сервера-посредника. Длительное время двусторонней передачи приводит к возникновению проблем при двусторонних аудиоразговорах в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="65afc-p108">High round-trip values can be caused by international call routing; a routing misconfiguration; or an overloaded media server. High round-trip times result in difficulties with two-way, real-time audio conversations.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65afc-153"><strong>PacketLossRate</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-153"><strong>PacketLossRate</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-154">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-154">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-p109">Средняя частота потери пакетов RTP. (Потеря пакетов происходит, когда пакеты RTP (Real-Time Transport Protocol — протокол, используемый для передачи аудио- и видеопакетов через Интернет) не достигают места назначения.) Высокие показатели потерь обычно вызваны перегрузкой, недостаточной полосой пропускания, помехами или перегрузкой беспроводной сети, а также перегрузкой сервера-посредника. Потеря пакетов обычно приводит к искажению звука или потере аудиосигналов.</span><span class="sxs-lookup"><span data-stu-id="65afc-p109">Average rate of Real-Time Transport Protocol (RTP) packet loss. (Packet loss occurs when RTP packets, a protocol used for transmitting audio and video across the Internet, failed to reach their destination.) High loss rates are generally caused by congestion; lack of bandwidth; wireless congestion or interference; or an overloaded media server. Packet loss typically results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65afc-158"><strong>PacketLossRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-158"><strong>PacketLossRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-159">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-159">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-160">Максимальная частота потери пакетов на транспортном протоколе Real-Time (RTP).</span><span class="sxs-lookup"><span data-stu-id="65afc-160">Maximum rate of Real-Time Transport Protocol (RTP) packet loss.</span></span> <span data-ttu-id="65afc-161">(Потеря пакетов происходит, когда пакеты RTP, протокол, используемый для передачи звука и видео через Интернет, не достигают места назначения.) Обычно тарифы на высокую степень потерь обусловлены перегрузкой; отсутствие пропускной способности; перегрузка беспроводной сети или помехи; или перегруженный сервер мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="65afc-161">(Packet loss occurs when RTP packets, a protocol used for transmitting audio and video across the Internet, failed to reach their destination.) High loss rates are generally caused by congestion; lack of bandwidth; wireless congestion or interference; or an overloaded media server.</span></span> <span data-ttu-id="65afc-162">Обычно это приводит к искажению или потере аудиосигнала.</span><span class="sxs-lookup"><span data-stu-id="65afc-162">Packet loss typically results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65afc-163"><strong>PacketUtilization</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-163"><strong>PacketUtilization</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-164">целое</span><span class="sxs-lookup"><span data-stu-id="65afc-164">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-165">Количество отправленных пакетов.</span><span class="sxs-lookup"><span data-stu-id="65afc-165">Number of packets sent.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65afc-166"><strong>Самый пропускная способность</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-166"><strong>BandwidthEst</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-167">целое</span><span class="sxs-lookup"><span data-stu-id="65afc-167">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-168">Предполагаемая односторонняя пропускная способность, доступная в конце сеанса.</span><span class="sxs-lookup"><span data-stu-id="65afc-168">Estimated one-way bandwidth available at the end of the session.</span></span> <span data-ttu-id="65afc-169">Указывается в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="65afc-169">Reported in bits per second.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65afc-170"><strong>AppSharingPayloadDescription</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-170"><strong>AppSharingPayloadDescription</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-171">целое</span><span class="sxs-lookup"><span data-stu-id="65afc-171">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-172">Описание полезных данных для общего использования приложений.</span><span class="sxs-lookup"><span data-stu-id="65afc-172">Description of the application sharing payload.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65afc-173"><strong>RelativeOneWayTotal</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-173"><strong>RelativeOneWayTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-174">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-174">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-175">Общая сумма односторонней задержки.</span><span class="sxs-lookup"><span data-stu-id="65afc-175">Total amount of one-way latency.</span></span> <span data-ttu-id="65afc-176">Относительная односторонняя задержка измеряет задержку между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="65afc-176">Relative one-way latency measures the delay between the client and the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65afc-177"><strong>RelativeOneWayAverage</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-177"><strong>RelativeOneWayAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-178">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-178">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-179">Средняя величина односторонней задержки.</span><span class="sxs-lookup"><span data-stu-id="65afc-179">Average amount of one-way latency.</span></span> <span data-ttu-id="65afc-180">Относительная односторонняя задержка измеряет задержку между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="65afc-180">Relative one-way latency measures the delay between the client and the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65afc-181"><strong>RelativeOneWayMax</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-181"><strong>RelativeOneWayMax</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-182">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-182">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-183">Максимальная сумма односторонняя задержка.</span><span class="sxs-lookup"><span data-stu-id="65afc-183">Maximum amount of one-way latency.</span></span> <span data-ttu-id="65afc-184">Относительная односторонняя задержка измеряет задержку между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="65afc-184">Relative one-way latency measures the delay between the client and the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65afc-185"><strong>RelativeOneWayBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-185"><strong>RelativeOneWayBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-186">целое</span><span class="sxs-lookup"><span data-stu-id="65afc-186">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-187">Общее количество односторонних вхождений.</span><span class="sxs-lookup"><span data-stu-id="65afc-187">Total one-way burst occurrences.</span></span> <span data-ttu-id="65afc-188">Одновременная передача данных — это передача, при которой данные передаются в непредсказуемые пакеты, а не в устойчивый поток.</span><span class="sxs-lookup"><span data-stu-id="65afc-188">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="65afc-189">Этот показатель измеряет поток данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="65afc-189">This metric measures data flow between the client and the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65afc-190"><strong>RelativeOneWayBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-190"><strong>RelativeOneWayBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-191">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-191">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-192">Общая односторонняя плотность нагрузки.</span><span class="sxs-lookup"><span data-stu-id="65afc-192">Total one-way burst density.</span></span> <span data-ttu-id="65afc-193">Одновременная передача данных — это передача, при которой данные передаются в непредсказуемые пакеты, а не в устойчивый поток.</span><span class="sxs-lookup"><span data-stu-id="65afc-193">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="65afc-194">Этот показатель измеряет поток данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="65afc-194">This metric measures data flow between the client and the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65afc-195"><strong>RelativeOneWayBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-195"><strong>RelativeOneWayBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-196">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-196">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-197">Общая продолжительность односторонней длительности.</span><span class="sxs-lookup"><span data-stu-id="65afc-197">Total one-way burst duration.</span></span> <span data-ttu-id="65afc-198">Одновременная передача данных — это передача, при которой данные передаются в непредсказуемые пакеты, а не в устойчивый поток.</span><span class="sxs-lookup"><span data-stu-id="65afc-198">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="65afc-199">Этот показатель измеряет поток данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="65afc-199">This metric measures data flow between the client and the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65afc-200"><strong>RelativeOneWayGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-200"><strong>RelativeOneWayGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-201">целое</span><span class="sxs-lookup"><span data-stu-id="65afc-201">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-202">Общее количество односторонних вхождений.</span><span class="sxs-lookup"><span data-stu-id="65afc-202">Total one-way gap occurrences.</span></span> <span data-ttu-id="65afc-203">Одновременная передача данных — это передача, при которой данные передаются в непредсказуемые пакеты, а не в устойчивый поток. зазоры указывают на задержку между этими пакетами.</span><span class="sxs-lookup"><span data-stu-id="65afc-203">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="65afc-204">Этот показатель измеряет поток данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="65afc-204">This metric measures data flow between the client and the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65afc-205"><strong>RelativeOneWayGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-205"><strong>RelativeOneWayGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-206">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-206">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-207">Общая плотность односторонних зазоров.</span><span class="sxs-lookup"><span data-stu-id="65afc-207">Total one-way gap density.</span></span> <span data-ttu-id="65afc-208">Одновременная передача данных — это передача, при которой данные передаются в непредсказуемые пакеты, а не в устойчивый поток. зазоры указывают на задержку между этими пакетами.</span><span class="sxs-lookup"><span data-stu-id="65afc-208">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="65afc-209">Этот показатель измеряет поток данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="65afc-209">This metric measures data flow between the client and the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65afc-210"><strong>RelativeOneWayGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-210"><strong>RelativeOneWayGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-211">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-211">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-212">Общая продолжительность односторонних промежутков.</span><span class="sxs-lookup"><span data-stu-id="65afc-212">Total one-way gap duration.</span></span> <span data-ttu-id="65afc-213">Одновременная передача данных — это передача, при которой данные передаются в непредсказуемые пакеты, а не в устойчивый поток. зазоры указывают на задержку между этими пакетами.</span><span class="sxs-lookup"><span data-stu-id="65afc-213">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="65afc-214">Этот показатель измеряет поток данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="65afc-214">This metric measures data flow between the client and the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65afc-215"><strong>ApplicationSharingType</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-215"><strong>ApplicationSharingType</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-216">varChar (256)</span><span class="sxs-lookup"><span data-stu-id="65afc-216">varChar(256)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-217">Роль приложения (общий доступ или средство просмотра) и тип контента.</span><span class="sxs-lookup"><span data-stu-id="65afc-217">Application role (Sharer or Viewer) and content type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65afc-218"><strong>RDPTileProcessingLatencyTotal</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-218"><strong>RDPTileProcessingLatencyTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-219">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-219">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-220">Общее время обработки плиток протокола удаленного рабочего стола (RDP).</span><span class="sxs-lookup"><span data-stu-id="65afc-220">Total processing time for remote desktop protocol (RDP) tiles.</span></span> <span data-ttu-id="65afc-221">Общая сумма равна более длительной задержке при просмотре.</span><span class="sxs-lookup"><span data-stu-id="65afc-221">A higher total equates to a longer delay in the viewing experience.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65afc-222"><strong>RDPTileProcessingLatencyAverage</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-222"><strong>RDPTileProcessingLatencyAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-223">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-223">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-224">Среднее время обработки плиток протокола удаленного рабочего стола (RDP).</span><span class="sxs-lookup"><span data-stu-id="65afc-224">Average processing time for remote desktop protocol (RDP) tiles.</span></span> <span data-ttu-id="65afc-225">Общая сумма равна более длительной задержке при просмотре.</span><span class="sxs-lookup"><span data-stu-id="65afc-225">A higher total equates to a longer delay in the viewing experience.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65afc-226"><strong>RDPTileProcessingLatencyMax</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-226"><strong>RDPTileProcessingLatencyMax</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-227">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-227">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-228">Максимальное время обработки плиток протокола удаленного рабочего стола (RDP).</span><span class="sxs-lookup"><span data-stu-id="65afc-228">Maximum processing time for remote desktop protocol (RDP) tiles.</span></span> <span data-ttu-id="65afc-229">Общая сумма равна более длительной задержке при просмотре.</span><span class="sxs-lookup"><span data-stu-id="65afc-229">A higher total equates to a longer delay in the viewing experience.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65afc-230"><strong>RDPTileProcessingLatencyBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-230"><strong>RDPTileProcessingLatencyBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-231">целое</span><span class="sxs-lookup"><span data-stu-id="65afc-231">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-232">Пакетное повторение на время обработки плиток протокола удаленного рабочего стола (RDP).</span><span class="sxs-lookup"><span data-stu-id="65afc-232">Burst occurrences in the processing time for remote desktop protocol (RDP) tiles.</span></span> <span data-ttu-id="65afc-233">Одновременная передача данных — это передача, при которой данные передаются в непредсказуемые пакеты, а не в устойчивый поток.</span><span class="sxs-lookup"><span data-stu-id="65afc-233">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65afc-234"><strong>RDPTileProcessingLatencyBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-234"><strong>RDPTileProcessingLatencyBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-235">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-235">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-236">Ускоренная плотность плиток протокола удаленного рабочего стола (RDP) на время обработки.</span><span class="sxs-lookup"><span data-stu-id="65afc-236">Burst density in the processing time for remote desktop protocol (RDP) tiles.</span></span> <span data-ttu-id="65afc-237">Одновременная передача данных — это передача, при которой данные передаются в непредсказуемые пакеты, а не в устойчивый поток.</span><span class="sxs-lookup"><span data-stu-id="65afc-237">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65afc-238"><strong>RDPTileProcessingLatencyBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-238"><strong>RDPTileProcessingLatencyBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-239">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-239">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-240">Продолжительность разбивки на время обработки плиток протокола удаленного рабочего стола (RDP).</span><span class="sxs-lookup"><span data-stu-id="65afc-240">Burst duration in the processing time for remote desktop protocol (RDP) tiles.</span></span> <span data-ttu-id="65afc-241">Одновременная передача данных — это передача, при которой данные передаются в непредсказуемые пакеты, а не в устойчивый поток.</span><span class="sxs-lookup"><span data-stu-id="65afc-241">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65afc-242"><strong>RDPTileProcessingLatencyGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-242"><strong>RDPTileProcessingLatencyGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-243">целое</span><span class="sxs-lookup"><span data-stu-id="65afc-243">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-244">Случаи пропуска на момент обработки плиток протокола удаленного рабочего стола (RDP).</span><span class="sxs-lookup"><span data-stu-id="65afc-244">Gap occurrences in the processing time for remote desktop protocol (RDP) tiles.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65afc-245"><strong>RDPTileProcessingLatencyGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-245"><strong>RDPTileProcessingLatencyGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-246">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-246">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-247">Плотность зазоров во время обработки плиток протокола удаленного рабочего стола (RDP).</span><span class="sxs-lookup"><span data-stu-id="65afc-247">Gap density in the processing time for remote desktop protocol (RDP) tiles.</span></span> <span data-ttu-id="65afc-248">Плотность неограниченного промежутка означает более качественный просмотр.</span><span class="sxs-lookup"><span data-stu-id="65afc-248">Low gap density equates to a better viewing experience.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65afc-249"><strong>RDPTileProcessingLatencyGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-249"><strong>RDPTileProcessingLatencyGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-250">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-250">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-251">Продолжительность пропуска для плиток протокола удаленного рабочего стола (RDP).</span><span class="sxs-lookup"><span data-stu-id="65afc-251">Gap duration in the processing time for remote desktop protocol (RDP) tiles.</span></span> <span data-ttu-id="65afc-252">Продолжительность коротких промежутков эквивалентна более качественному просмотру.</span><span class="sxs-lookup"><span data-stu-id="65afc-252">Short gap durations equate to a better viewing experience.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65afc-253"><strong>CaptureTileRateTotal</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-253"><strong>CaptureTileRateTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-254">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-254">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-255">Общая частота захваченных плиток (в плитках в секунду).</span><span class="sxs-lookup"><span data-stu-id="65afc-255">Total rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65afc-256"><strong>CaptureTileRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-256"><strong>CaptureTileRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-257">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-257">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-258">Средняя скорость захваченных плиток (в плитках в секунду).</span><span class="sxs-lookup"><span data-stu-id="65afc-258">Average rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65afc-259"><strong>CaptureTileRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-259"><strong>CaptureTileRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-260">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-260">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-261">Максимальная частота захваченных плиток (в плитках в секунду).</span><span class="sxs-lookup"><span data-stu-id="65afc-261">Maximum rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65afc-262"><strong>CaptureTileRateBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-262"><strong>CaptureTileRateBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-263">в t</span><span class="sxs-lookup"><span data-stu-id="65afc-263">in t</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-264">Пакетное повторение в частоте захваченных плиток (в плитках в секунду).</span><span class="sxs-lookup"><span data-stu-id="65afc-264">Burst occurrences in the rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65afc-265"><strong>CaptureTileRateBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-265"><strong>CaptureTileRateBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-266">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-266">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-267">Плотность разбивки на захваченные плитки (в плитках в секунду).</span><span class="sxs-lookup"><span data-stu-id="65afc-267">Burst density in the rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65afc-268"><strong>CaptureTileRateBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-268"><strong>CaptureTileRateBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-269">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-269">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-270">Продолжительность разбивки на собранные плитки (в плитках в секунду).</span><span class="sxs-lookup"><span data-stu-id="65afc-270">Burst duration in the rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65afc-271"><strong>CaptureTileRateGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-271"><strong>CaptureTileRateGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-272">целое</span><span class="sxs-lookup"><span data-stu-id="65afc-272">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-273">Количество повторений в частоте захваченных плиток (в плитках в секунду).</span><span class="sxs-lookup"><span data-stu-id="65afc-273">Gap occurrences in the rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65afc-274"><strong>CaptureTileRateGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-274"><strong>CaptureTileRateGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-275">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-275">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-276">Плотность зазоров в процентах захваченных плиток (в плитках в секунду).</span><span class="sxs-lookup"><span data-stu-id="65afc-276">Gap density in the rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65afc-277"><strong>CaptureTileRateGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-277"><strong>CaptureTileRateGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-278">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-278">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-279">Продолжительность зазора в процентах собранных плиток (в плитках в секунду).</span><span class="sxs-lookup"><span data-stu-id="65afc-279">Gap duration in the rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65afc-280"><strong>SpoiledTilePercentTotal</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-280"><strong>SpoiledTilePercentTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-281">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-281">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-282">Общий процент содержимого, которое не было получено средством просмотра, но было бы удалено и заменено новым содержимым.</span><span class="sxs-lookup"><span data-stu-id="65afc-282">Total percentage of the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65afc-283"><strong>SpoiledTilePercentAverage</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-283"><strong>SpoiledTilePercentAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-284">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-284">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-285">Средний процент содержимого, которое не достиго средства просмотра, но было удалено и заменено новым содержимым.</span><span class="sxs-lookup"><span data-stu-id="65afc-285">Average percentage of the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65afc-286"><strong>SpoiledTilePercentMax</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-286"><strong>SpoiledTilePercentMax</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-287">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-287">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-288">Максимальный процент содержимого, которое не было получено средством просмотра, но было бы удалено и заменено новым содержимым.</span><span class="sxs-lookup"><span data-stu-id="65afc-288">Maximum percentage of the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65afc-289"><strong>SpoiledTilePercentBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-289"><strong>SpoiledTilePercentBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-290">целое</span><span class="sxs-lookup"><span data-stu-id="65afc-290">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-291">Пакетное повторение для содержимого, которое не достиго средства просмотра, а было удалено и заменено новым содержимым.</span><span class="sxs-lookup"><span data-stu-id="65afc-291">Burst occurrences for the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65afc-292"><strong>SpoiledTilePercentBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-292"><strong>SpoiledTilePercentBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-293">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-293">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-294">Для содержимого, которое не достигают средства просмотра, оно было удалено и заменено новым содержимым.</span><span class="sxs-lookup"><span data-stu-id="65afc-294">Burst density for the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65afc-295"><strong>SpoiledTilePercentBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-295"><strong>SpoiledTilePercentBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-296">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-296">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-297">Продолжительность разбивки на содержимое, которое не было получено средством просмотра, но было бы удалено и заменено новым содержимым.</span><span class="sxs-lookup"><span data-stu-id="65afc-297">Burst duration for the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65afc-298"><strong>SpoiledTilePercentGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-298"><strong>SpoiledTilePercentGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-299">целое</span><span class="sxs-lookup"><span data-stu-id="65afc-299">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-300">Повторение для содержимого, которое не достиго средства просмотра, но было удалено и заменено новым содержимым.</span><span class="sxs-lookup"><span data-stu-id="65afc-300">Gap occurrences for the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65afc-301"><strong>SpoiledTilePercentGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-301"><strong>SpoiledTilePercentGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-302">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-302">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-303">Плотность зазоров для содержимого, которое не достиго средства просмотра, но было удалено и заменено новым содержимым.</span><span class="sxs-lookup"><span data-stu-id="65afc-303">Gap density for the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65afc-304"><strong>SpoiledTilePercentGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-304"><strong>SpoiledTilePercentGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-305">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-305">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-306">Продолжительность зазора для содержимого, которое не достиго средства просмотра, но было удалено и заменено новым содержимым.</span><span class="sxs-lookup"><span data-stu-id="65afc-306">Gap duration for the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65afc-307"><strong>ScrapingFrameRateTotal</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-307"><strong>ScrapingFrameRateTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-308">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-308">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-309">Общее количество кадров, набракованных из источника графики.</span><span class="sxs-lookup"><span data-stu-id="65afc-309">Total number of frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65afc-310"><strong>ScrapingFrameRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-310"><strong>ScrapingFrameRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-311">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-311">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-312">Среднее количество кадров, набракованных из источника графики.</span><span class="sxs-lookup"><span data-stu-id="65afc-312">Average number of frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65afc-313"><strong>ScrapingFrameRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-313"><strong>ScrapingFrameRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-314">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-314">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-315">Предельное число кадров, которые не побраковано от источника графики.</span><span class="sxs-lookup"><span data-stu-id="65afc-315">Maximum number of frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65afc-316"><strong>ScrapingFrameRateBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-316"><strong>ScrapingFrameRateBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-317">целое</span><span class="sxs-lookup"><span data-stu-id="65afc-317">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-318">Пакетное повторение в кадре побраковано от источника графики.</span><span class="sxs-lookup"><span data-stu-id="65afc-318">Burst occurrences in the frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65afc-319"><strong>ScrapingFrameRateBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-319"><strong>ScrapingFrameRateBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-320">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-320">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-321">Ускоренная плотность кадров в кадрах, побракованных из источника графики.</span><span class="sxs-lookup"><span data-stu-id="65afc-321">Burst density in the frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65afc-322"><strong>ScrapingFrameRateBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-322"><strong>ScrapingFrameRateBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-323">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-323">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-324">Продолжительность разбивки кадров в кадре, побракованная от источника графики.</span><span class="sxs-lookup"><span data-stu-id="65afc-324">Burst duration in the frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65afc-325"><strong>ScrapingFrameRateGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-325"><strong>ScrapingFrameRateGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-326">целое</span><span class="sxs-lookup"><span data-stu-id="65afc-326">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-327">Случаи разрывов в кадрах оббракованы из источника графики.</span><span class="sxs-lookup"><span data-stu-id="65afc-327">Gap occurrences in the frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65afc-328"><strong>ScrapingFrameRateGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-328"><strong>ScrapingFrameRateGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-329">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-329">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-330">Плотность зазоров в кадрах, побракованных из источника графики.</span><span class="sxs-lookup"><span data-stu-id="65afc-330">Gap density in the frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65afc-331"><strong>ScrapingFrameRateGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-331"><strong>ScrapingFrameRateGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-332">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-332">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-333">Продолжительность зазора в кадрах, побракованных из источника графики.</span><span class="sxs-lookup"><span data-stu-id="65afc-333">Gap duration in the frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65afc-334"><strong>IncomingTileRateTotal</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-334"><strong>IncomingTileRateTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-335">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-335">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-336">Общая частота входящих кадров, полученных средством просмотра.</span><span class="sxs-lookup"><span data-stu-id="65afc-336">Total incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65afc-337"><strong>IncomingTileRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-337"><strong>IncomingTileRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-338">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-338">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-339">Средняя частота входящих кадров, полученная средством просмотра.</span><span class="sxs-lookup"><span data-stu-id="65afc-339">Average incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65afc-340"><strong>IncomingTileRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-340"><strong>IncomingTileRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-341">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-341">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-342">Максимальное количество входящих частот плиток, полученных средством просмотра.</span><span class="sxs-lookup"><span data-stu-id="65afc-342">Maximum incoming tile rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65afc-343"><strong>IncomingTileRateBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-343"><strong>IncomingTileRateBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-344">целое</span><span class="sxs-lookup"><span data-stu-id="65afc-344">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-345">Пакетное повторение входящего, полученного средством просмотра частоты плиток.</span><span class="sxs-lookup"><span data-stu-id="65afc-345">Burst occurrences in the incoming tile rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65afc-346"><strong>IncomingTileRateBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-346"><strong>IncomingTileRateBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-347">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-347">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-348">Многоуровневая плотность во входящих частотах плиток, полученных средством просмотра.</span><span class="sxs-lookup"><span data-stu-id="65afc-348">Burst density in the incoming tile rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65afc-349"><strong>IncomingTileRateBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-349"><strong>IncomingTileRateBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-350">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-350">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-351">Продолжительность пакетной обработки на входящем частоте плиток, полученной средством просмотра.</span><span class="sxs-lookup"><span data-stu-id="65afc-351">Burst duration in the incoming tile rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65afc-352"><strong>IncomingTileRateGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-352"><strong>IncomingTileRateGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-353">целое</span><span class="sxs-lookup"><span data-stu-id="65afc-353">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-354">Количество вхождений во входящих частотах плиток, полученных средством просмотра.</span><span class="sxs-lookup"><span data-stu-id="65afc-354">Gap occurrences in the incoming tile rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65afc-355"><strong>IncomingTileRateGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-355"><strong>IncomingTileRateGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-356">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-356">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-357">Плотность просветов во входящих частотах плиток, полученных средством просмотра.</span><span class="sxs-lookup"><span data-stu-id="65afc-357">Gap density in the incoming tile rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65afc-358"><strong>IncomingTileRateGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-358"><strong>IncomingTileRateGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-359">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-359">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-360">Длительность пропуска во входящих частотах плиток, полученных средством просмотра.</span><span class="sxs-lookup"><span data-stu-id="65afc-360">Gap duration in the incoming tile rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65afc-361"><strong>IncomingFrameRateTotal</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-361"><strong>IncomingFrameRateTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-362">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-362">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-363">Общая частота входящих кадров, полученных средством просмотра.</span><span class="sxs-lookup"><span data-stu-id="65afc-363">Total incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65afc-364"><strong>IncomingFrameRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-364"><strong>IncomingFrameRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-365">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-365">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-366">Средняя частота входящих кадров, полученная средством просмотра.</span><span class="sxs-lookup"><span data-stu-id="65afc-366">Average incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65afc-367"><strong>IncomingFrameRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-367"><strong>IncomingFrameRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-368">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-368">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-369">Максимальная частота поступающих кадров, полученных средством просмотра.</span><span class="sxs-lookup"><span data-stu-id="65afc-369">Maximum incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65afc-370"><strong>IncomingFrameRateBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-370"><strong>IncomingFrameRateBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-371">целое</span><span class="sxs-lookup"><span data-stu-id="65afc-371">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-372">Пакетное повторение во входящих частотах кадров, полученных средством просмотра.</span><span class="sxs-lookup"><span data-stu-id="65afc-372">Burst occurrences in the incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65afc-373"><strong>IncomingFrameRateBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-373"><strong>IncomingFrameRateBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-374">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-374">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-375">Многоуровневая плотность во входящих частотах кадров, полученных средством просмотра.</span><span class="sxs-lookup"><span data-stu-id="65afc-375">Burst density in the incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65afc-376"><strong>IncomingFrameRateBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-376"><strong>IncomingFrameRateBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-377">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-377">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-378">Продолжительность многочастотной обработки кадров, полученная средством просмотра.</span><span class="sxs-lookup"><span data-stu-id="65afc-378">Burst duration in the incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65afc-379"><strong>IncomingFrameRateGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-379"><strong>IncomingFrameRateGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-380">целое</span><span class="sxs-lookup"><span data-stu-id="65afc-380">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-381">Пропуск вхождений во входной частоте кадров, полученной средством просмотра.</span><span class="sxs-lookup"><span data-stu-id="65afc-381">Gap occurrences in the incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65afc-382"><strong>IncomingFrameRateGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-382"><strong>IncomingFrameRateGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-383">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-383">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-384">Плотность зазоров во входящих частотах кадров, полученных средством просмотра.</span><span class="sxs-lookup"><span data-stu-id="65afc-384">Gap density in the incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65afc-385"><strong>IncomingFrameRateDuration</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-385"><strong>IncomingFrameRateDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-386">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-386">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-387">Длительность промежутка во входящих частотах кадров, полученных средством просмотра.</span><span class="sxs-lookup"><span data-stu-id="65afc-387">Gap duration in the incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65afc-388"><strong>OutgoingTileRateTotal</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-388"><strong>OutgoingTileRateTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-389">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-389">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-390">Общая частота исходящих плиток для отправителя.</span><span class="sxs-lookup"><span data-stu-id="65afc-390">Total outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65afc-391"><strong>OutgoingTileRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-391"><strong>OutgoingTileRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-392">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-392">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-393">Средняя исходящая частота плиток для отправителя.</span><span class="sxs-lookup"><span data-stu-id="65afc-393">Average outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65afc-394"><strong>OutgoingTileRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-394"><strong>OutgoingTileRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-395">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-395">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-396">Максимальная исходящая ставка плиток для отправителя.</span><span class="sxs-lookup"><span data-stu-id="65afc-396">Maximum outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65afc-397"><strong>OutgoingTileRateBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-397"><strong>OutgoingTileRateBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-398">целое</span><span class="sxs-lookup"><span data-stu-id="65afc-398">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-399">Пакетное повторение исходящих плиток для отправителя.</span><span class="sxs-lookup"><span data-stu-id="65afc-399">Burst occurrences in the outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65afc-400"><strong>OutgoingTileRateBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-400"><strong>OutgoingTileRateBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-401">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-401">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-402">Плотность разбивки на выходящую частоту плиток для отправителя.</span><span class="sxs-lookup"><span data-stu-id="65afc-402">Burst density in the outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65afc-403"><strong>OutgoingTileRateBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-403"><strong>OutgoingTileRateBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-404">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-404">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-405">Продолжительность разбивки на исходящую частоту плиток для отправителя.</span><span class="sxs-lookup"><span data-stu-id="65afc-405">Burst duration in the outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65afc-406"><strong>OutgoingTileRateGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-406"><strong>OutgoingTileRateGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-407">целое</span><span class="sxs-lookup"><span data-stu-id="65afc-407">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-408">Количество повторений в исходящих частотах плиток для отправителя.</span><span class="sxs-lookup"><span data-stu-id="65afc-408">Gap occurrences in the outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65afc-409"><strong>OutgoingTileRateGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-409"><strong>OutgoingTileRateGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-410">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-410">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-411">Плотность зазоров для отправителя за исходящую частоту плиток.</span><span class="sxs-lookup"><span data-stu-id="65afc-411">Gap density in the outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65afc-412"><strong>OutgoingTileRateGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-412"><strong>OutgoingTileRateGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-413">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-413">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-414">Продолжительность зазора для отправителя с исходящим рейтингом.</span><span class="sxs-lookup"><span data-stu-id="65afc-414">Gap duration in the outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65afc-415"><strong>OutgoingFrameRateTotal</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-415"><strong>OutgoingFrameRateTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-416">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-416">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-417">Общая частота исходящих кадров для отправителя.</span><span class="sxs-lookup"><span data-stu-id="65afc-417">Total outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65afc-418"><strong>OutgoingFrameRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-418"><strong>OutgoingFrameRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-419">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-419">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-420">средняя исходящая частота кадров для отправителя.</span><span class="sxs-lookup"><span data-stu-id="65afc-420">average outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65afc-421"><strong>OutgoingFrameRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-421"><strong>OutgoingFrameRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-422">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-422">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-423">Максимальная исходящая частота кадров для отправителя.</span><span class="sxs-lookup"><span data-stu-id="65afc-423">Maximum outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65afc-424"><strong>OutgoingFrameRateBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-424"><strong>OutgoingFrameRateBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-425">целое</span><span class="sxs-lookup"><span data-stu-id="65afc-425">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-426">Пакетное повторение в исходящих частотах кадров для отправителя.</span><span class="sxs-lookup"><span data-stu-id="65afc-426">Burst occurrences in the outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65afc-427"><strong>OutgoingFrameRateBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-427"><strong>OutgoingFrameRateBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-428">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-428">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-429">В исходящих частотах кадров для отправителя — это пакетная плотность.</span><span class="sxs-lookup"><span data-stu-id="65afc-429">Burst density in the outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65afc-430"><strong>OutgoingFrameRateBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-430"><strong>OutgoingFrameRateBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-431">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-431">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-432">Продолжительность разбивки кадров в исходящей частотной скорости для отправителя.</span><span class="sxs-lookup"><span data-stu-id="65afc-432">Burst duration in the outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65afc-433"><strong>OutgoingFrameRateGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-433"><strong>OutgoingFrameRateGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-434">целое</span><span class="sxs-lookup"><span data-stu-id="65afc-434">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-435">Количество повторений в исходящей частоте кадров для отправителя.</span><span class="sxs-lookup"><span data-stu-id="65afc-435">Gap occurrences in the outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65afc-436"><strong>OutgoingFrameRateGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-436"><strong>OutgoingFrameRateGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-437">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-437">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-438">Плотность зазоров в исходящих частотах кадров для отправителя.</span><span class="sxs-lookup"><span data-stu-id="65afc-438">Gap density in the outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65afc-439"><strong>OutgoingFrameRateGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-439"><strong>OutgoingFrameRateGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-440">число с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="65afc-440">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-441">Длительность промежутка в исходящих частотах кадров для отправителя.</span><span class="sxs-lookup"><span data-stu-id="65afc-441">Gap duration in the outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65afc-442"><strong>AverageRectangleHeight</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-442"><strong>AverageRectangleHeight</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-443">целое</span><span class="sxs-lookup"><span data-stu-id="65afc-443">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-444">Средняя высота разрешающей способности видео (в пикселях).</span><span class="sxs-lookup"><span data-stu-id="65afc-444">Average video resolution height, in pixels.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65afc-445"><strong>AverageRectangleWidth</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-445"><strong>AverageRectangleWidth</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-446">целое</span><span class="sxs-lookup"><span data-stu-id="65afc-446">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-447">Средняя ширина разрешающей способности видео в пикселях.</span><span class="sxs-lookup"><span data-stu-id="65afc-447">Average video resolution width, in pixels.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65afc-448"><strong>443</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-448"><strong>Inbound</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-449">бит</span><span class="sxs-lookup"><span data-stu-id="65afc-449">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-450">Средняя частота кадров (в кадрах в секунду) для входящих передач.</span><span class="sxs-lookup"><span data-stu-id="65afc-450">Average frame rate (in frames per second) for inbound transmissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65afc-451"><strong>Исходящее</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-451"><strong>Outbound</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-452">бит</span><span class="sxs-lookup"><span data-stu-id="65afc-452">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-453">Средняя частота кадров (в кадрах в секунду) для исходящих передач.</span><span class="sxs-lookup"><span data-stu-id="65afc-453">Average frame rate (in frames per second) for outbound transmissions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65afc-454"><strong>SenderIsCallerPAI</strong></span><span class="sxs-lookup"><span data-stu-id="65afc-454"><strong>SenderIsCallerPAI</strong></span></span></p></td>
<td><p><span data-ttu-id="65afc-455">бит</span><span class="sxs-lookup"><span data-stu-id="65afc-455">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65afc-456">1 — направление потока для вызываемого абонента.</span><span class="sxs-lookup"><span data-stu-id="65afc-456">1 means the stream direction is from the caller to callee.</span></span></p>
<p><span data-ttu-id="65afc-457">0 — направление потока из вызываемого объекта вызывающему абоненту.</span><span class="sxs-lookup"><span data-stu-id="65afc-457">0 means the stream direction is from the callee to the caller.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="65afc-458">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="65afc-458">


</div>

<span> </span>

</div>

</div>

</span></span></div>

