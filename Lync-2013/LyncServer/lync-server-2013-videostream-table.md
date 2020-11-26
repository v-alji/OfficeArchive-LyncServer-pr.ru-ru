---
title: 'Lync Server 2013: таблица VideoStream'
description: 'Таблица Lync Server 2013: VideoStream.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: VideoStream table
ms:assetid: 4275ede7-5467-4a97-b8c8-a4b00917bf32
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425928(v=OCS.15)
ms:contentKeyID: 48184014
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0d741478e1f6290685181bff471f143e41ce9ca1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444128"
---
# <a name="videostream-table-in-lync-server-2013"></a>Таблица VideoStream в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2013-12-13_

Каждая запись представляет один поток видео. Одна линия видеофайла обычно состоит из двух видеопотоков.


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Столбец</strong></th>
<th><strong>Тип данных</strong></th>
<th><strong>Ключ/индекс</strong></th>
<th><strong>Details</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>ConferenceDateTime</strong></p></td>
<td><p>datetime</p></td>
<td><p>Primary</p></td>
<td><p>На которую ссылается <a href="lync-server-2013-medialine-table.md">Таблица MediaLine в Lync Server 2013</a>.</p></td>
</tr>
<tr class="even">
<td><p><strong>SessionSeq</strong></p></td>
<td><p>целое</p></td>
<td><p>Primary</p></td>
<td><p>R, на который ссылается <a href="lync-server-2013-medialine-table.md">Таблица MediaLine в Lync Server 2013</a>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>MediaLineLabel</strong></p></td>
<td><p>tinyint</p></td>
<td><p>Primary</p></td>
<td><p>На которую ссылается <a href="lync-server-2013-medialine-table.md">Таблица MediaLine в Lync Server 2013</a>.</p></td>
</tr>
<tr class="even">
<td><p><strong>StreamID</strong></p></td>
<td><p>целое</p></td>
<td><p>Primary</p></td>
<td><p>Уникальный идентификатор в строке мультимедиа.</p></td>
</tr>
<tr class="odd">
<td><p><strong>VideoPayloadDescription</strong></p></td>
<td><p>smallint</p></td>
<td><p>Внешний, основной</p></td>
<td><p>Описание полезных данных. Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-payloaddescription-table.md">таблицей PayloadDescription в Lync Server 2013</a> .</p></td>
</tr>
<tr class="even">
<td><p><strong>JitterInterArrival</strong></p></td>
<td><p>целое</p></td>
<td><p> </p></td>
<td><p>Средняя колебание сети из статистики протокола управления временем в реальном времени (RTCP).</p></td>
</tr>
<tr class="odd">
<td><p><strong>JitterInterArrivalMax</strong></p></td>
<td><p>целое</p></td>
<td><p> </p></td>
<td><p>Максимальная колебание сети во время видеосеанса.</p></td>
</tr>
<tr class="even">
<td><p><strong>RoundTrip</strong></p></td>
<td><p>целое</p></td>
<td><p> </p></td>
<td><p>Время кругового приема из статистики RTCP.</p></td>
</tr>
<tr class="odd">
<td><p><strong>RoundTripMax</strong></p></td>
<td><p>целое</p></td>
<td><p> </p></td>
<td><p>Максимальное время кругового сеанса для видеопотока.</p></td>
</tr>
<tr class="even">
<td><p><strong>PacketLossRate</strong></p></td>
<td><p>десятичное число (5; 4)</p></td>
<td><p> </p></td>
<td><p>Средняя скорость потерь пакетов во время звонка.</p></td>
</tr>
<tr class="odd">
<td><p><strong>PacketLossRateMax</strong></p></td>
<td><p>десятичное число (5; 4)</p></td>
<td><p> </p></td>
<td><p>Максимальное количество потерь пакетов, замеченное во время звонка.</p></td>
</tr>
<tr class="even">
<td><p><strong>PacketUtilization</strong></p></td>
<td><p>целое</p></td>
<td><p> </p></td>
<td><p>Число пакетов для видеопотока (транспортный протокол в реальном времени).</p></td>
</tr>
<tr class="odd">
<td><p><strong>Самый пропускная способность</strong></p></td>
<td><p>целое</p></td>
<td><p> </p></td>
<td><p>Оценка пропускной способности для видеопотока.</p></td>
</tr>
<tr class="even">
<td><p><strong>VideoResolution</strong></p></td>
<td><p>char (9)</p></td>
<td><p> </p></td>
<td><p>Разрешение видео в пикселях, умноженное на высоту в пикселях. Отображается в виде строки.</p></td>
</tr>
<tr class="odd">
<td><p><strong>VideoBitRateAvg</strong></p></td>
<td><p>целое</p></td>
<td><p> </p></td>
<td><p>Средняя скорость потока видео.</p></td>
</tr>
<tr class="even">
<td><p><strong>InboundVideoFrameRateAvg</strong></p></td>
<td><p>десятичное число (9; 4)</p></td>
<td><p> </p></td>
<td><p>Полученная частота кадров видео.</p></td>
</tr>
<tr class="odd">
<td><p><strong>OutboundVideoFrameRateAvg</strong></p></td>
<td><p>десятичное число (9; 4)</p></td>
<td><p> </p></td>
<td><p>Частота отправки кадров видео.</p></td>
</tr>
<tr class="even">
<td><p><strong>VideoBitRateMax</strong></p></td>
<td><p>целое</p></td>
<td><p> </p></td>
<td><p>Максимальная скорость видеосигнала во время видеосеанса.</p></td>
</tr>
<tr class="odd">
<td><p><strong>VideoFrameLossRate</strong></p></td>
<td><p>десятичное число (9; 4)</p></td>
<td><p> </p></td>
<td><p>Процент от общего числа потерянных кадров видео.</p></td>
</tr>
<tr class="even">
<td><p><strong>VideoFEC</strong></p></td>
<td><p>бит</p></td>
<td><p> </p></td>
<td><p>Недоступно.</p></td>
</tr>
<tr class="odd">
<td><p><strong>VideoLocalFrameLossPercentageAvg</strong></p></td>
<td><p>десятичное число (9; 4)</p></td>
<td></td>
<td><p>Процент от общего числа потерянных кадров видео.</p></td>
</tr>
<tr class="even">
<td><p><strong>CIFQualityRatio</strong></p></td>
<td><p>tinyint</p></td>
<td></td>
<td><p>Процент звонка, находился в разрешении общего формата обмена (CIF).</p></td>
</tr>
<tr class="odd">
<td><p><strong>VGAQualityRatio</strong></p></td>
<td><p>tinyint</p></td>
<td></td>
<td><p>Процент звонка, находился в режиме разрешающей способности VGA.</p></td>
</tr>
<tr class="even">
<td><p><strong>HD720QualityRatio</strong></p></td>
<td><p>tinyint</p></td>
<td></td>
<td><p>Процентное соотношение вызова, которое было установлено по адресу HD720.</p></td>
</tr>
<tr class="odd">
<td><p><strong>NoneDropRatio</strong></p></td>
<td><p>tinyint</p></td>
<td></td>
<td><p>Процент продолжительности звонка без удаления кадров.</p></td>
</tr>
<tr class="even">
<td><p><strong>BDropRatio</strong></p></td>
<td><p>tinyint</p></td>
<td></td>
<td><p>Процент продолжительности звонка с помощью функции B Frame Drop.</p></td>
</tr>
<tr class="odd">
<td><p><strong>BPDropRatio</strong></p></td>
<td><p>tinyint</p></td>
<td></td>
<td><p>Процент продолжительности звонка с помощью перетаскивания рамки BP.</p></td>
</tr>
<tr class="even">
<td><p><strong>BPSPDropRatio</strong></p></td>
<td><p>tinyint</p></td>
<td></td>
<td><p>Процент продолжительности звонка с помощью BPSP Frame Drop.</p></td>
</tr>
<tr class="odd">
<td><p><strong>BPSPIDropRatio</strong></p></td>
<td><p>tinyint</p></td>
<td></td>
<td><p>Процент продолжительности звонка с помощью BPSPI Frame Drop.</p></td>
</tr>
<tr class="even">
<td><p><strong>443</strong></p></td>
<td><p>бит</p></td>
<td><p> </p></td>
<td><p>Получение потоковых данных на стороне получателя.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Исходящее</strong></p></td>
<td><p>бит</p></td>
<td><p> </p></td>
<td><p>Получение данных потока на стороне отправителя.</p></td>
</tr>
<tr class="even">
<td><p><strong>SenderIsCallerPAI</strong></p></td>
<td><p>бит</p></td>
<td><p> </p></td>
<td><p>1 — направление потока для вызываемого абонента.</p>
<p>0 — направление потока из вызываемого объекта вызывающему абоненту.</p></td>
</tr>
<tr class="odd">
<td><p><strong>LossCongestionPercent</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Указывает процент времени, в течение которого Звонок находился в состоянии перегрузки с потерей.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="even">
<td><p><strong>DelayCongestionPercent</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Указывает процент вызова, в течение которого перегрузка была вызвана отложенным поступлением сетевых пакетов.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="odd">
<td><p><strong>ContentionDetectedPercent</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Указывает процент времени, в течение которого Звонок конкурирует за ресурсы сети.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="even">
<td><p><strong>BandwidthEstMin</strong></p></td>
<td><p>целое</p></td>
<td></td>
<td><p>Минимальная сумма оценки пропускной способности, измеряемая во время звонка.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="odd">
<td><p><strong>BandwidthEstMax</strong></p></td>
<td><p>целое</p></td>
<td></td>
<td><p>Максимальная степень оценки пропускной способности, измеряемая во время звонка.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="even">
<td><p><strong>BandwidthEstStdDev</strong></p></td>
<td><p>целое</p></td>
<td></td>
<td><p>Стандартное отклонение оценки пропускной способности, измеряемой во время звонка.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="odd">
<td><p><strong>BandwidthEstAvge</strong></p></td>
<td><p>целое</p></td>
<td></td>
<td><p>Средняя сумма оценки пропускной способности, измеряемая во время звонка.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="even">
<td><p><strong>LowBandwidthForMultiview</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Процент звонка, когда конечная точка определила, что сетевое подключение не поддерживало функцию просмотра видео.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="odd">
<td><p><strong>RelativeOneWayTotal</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Общая сумма односторонней задержки. Относительная односторонняя задержка измеряет задержку между клиентом и сервером.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="even">
<td><p><strong>RelativeOneWayAverage</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Средняя величина односторонней задержки. Относительная односторонняя задержка измеряет задержку между клиентом и сервером.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="odd">
<td><p><strong>RelativeOneWayMax</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Максимальная сумма односторонняя задержка. Относительная односторонняя задержка измеряет задержку между клиентом и сервером.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="even">
<td><p><strong>RelativeOneWayBurstOccurrences</strong></p></td>
<td><p>целое</p></td>
<td></td>
<td><p>Общее количество односторонних вхождений. Одновременная передача данных — это передача, при которой данные передаются в непредсказуемые пакеты, а не в устойчивый поток. Этот показатель измеряет поток данных между клиентом и сервером.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="odd">
<td><p><strong>RelativeOneWayBurstDensity</strong></p></td>
<td><p>целое</p></td>
<td></td>
<td><p>Общая односторонняя плотность нагрузки. Одновременная передача данных — это передача, при которой данные передаются в непредсказуемые пакеты, а не в устойчивый поток. Этот показатель измеряет поток данных между клиентом и сервером.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="even">
<td><p><strong>RelativeOneWayBurstDuration</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Общая продолжительность односторонней длительности. Одновременная передача данных — это передача, при которой данные передаются в непредсказуемые пакеты, а не в устойчивый поток. Этот показатель измеряет поток данных между клиентом и сервером.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="odd">
<td><p><strong>RelativeOneWayGapOccurrences</strong></p></td>
<td><p>целое</p></td>
<td></td>
<td><p>Общее количество односторонних вхождений. Одновременная передача данных — это передача, при которой данные передаются в непредсказуемые пакеты, а не в устойчивый поток. зазоры указывают на задержку между этими пакетами. Этот показатель измеряет поток данных между клиентом и сервером.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="even">
<td><p><strong>RelativeOneWayGapDensity</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Общая плотность односторонних зазоров. Одновременная передача данных — это передача, при которой данные передаются в непредсказуемые пакеты, а не в устойчивый поток. зазоры указывают на задержку между этими пакетами. Этот показатель измеряет поток данных между клиентом и сервером.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="odd">
<td><p><strong>RelativeOneWayGapDuration</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Общая продолжительность односторонних промежутков. Одновременная передача данных — это передача, при которой данные передаются в непредсказуемые пакеты, а не в устойчивый поток. зазоры указывают на задержку между этими пакетами. Этот показатель измеряет поток данных между клиентом и сервером.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="even">
<td><p><strong>VideoPacketLossRate</strong></p></td>
<td><p>десятичное число (9; 4)</p></td>
<td></td>
<td><p>Частота потери видеопакетов.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="odd">
<td><p><strong>VideoAllocateBWAvg</strong></p></td>
<td><p>целое</p></td>
<td></td>
<td><p>Средний объем пропускной способности, выделенной для видео.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="even">
<td><p><strong>SendCodecTypes</strong></p></td>
<td><p>smallint</p></td>
<td><p>Другом</p></td>
<td><p>Тип видеокодеков, используемых отправителем. Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-codecdescription-table.md">таблицей CodecDescription в Lync Server 2013</a> .</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="odd">
<td><p><strong>SendResolutionWidth</strong></p></td>
<td><p>целое</p></td>
<td></td>
<td><p>Ширина разрешения, используемая отправителем.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="even">
<td><p><strong>SendResolutionHeight</strong></p></td>
<td><p>целое</p></td>
<td></td>
<td><p>Высота разрешения, используемая отправителем.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="odd">
<td><p><strong>SendFrameRateAverage</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Средняя скорость кадров видео, используемая отправителем.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="even">
<td><p><strong>SendBitRateMaximum</strong></p></td>
<td><p>целое</p></td>
<td></td>
<td><p>Максимальная скорость для отправителя.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="odd">
<td><p><strong>SendBitRateAverage</strong></p></td>
<td><p>целое</p></td>
<td></td>
<td><p>Средняя скорость в битах для отправителя.</p></td>
</tr>
<tr class="even">
<td><p><strong>SendVideoStreamsMax</strong></p></td>
<td><p>целое</p></td>
<td></td>
<td><p>Максимальное количество видеопотоков, используемых отправителем.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="odd">
<td><p><strong>RecvCodecTypes</strong></p></td>
<td><p>smallint</p></td>
<td><p>Другом</p></td>
<td><p>Видео коды, используемые получателем. Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-codecdescription-table.md">таблицей CodecDescription в Lync Server 2013</a> .</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="even">
<td><p><strong>RecvResolutionWidth</strong></p></td>
<td><p>целое</p></td>
<td></td>
<td><p>Ширина разрешения, используемая получателем.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="odd">
<td><p><strong>RecvResolutionHeight</strong></p></td>
<td><p>целое</p></td>
<td></td>
<td><p>Высота разрешения, используемая получателем.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="even">
<td><p><strong>RecvFrameRateAverage</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Средняя частота кадров видео, используемая получателем.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="odd">
<td><p><strong>RecvBitRateMaximum</strong></p></td>
<td><p>целое</p></td>
<td></td>
<td><p>Максимальная скорость потока для получателя.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="even">
<td><p><strong>RecvBitRateAverage</strong></p></td>
<td><p>целое</p></td>
<td></td>
<td><p>Средняя скорость потока для получателя.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="odd">
<td><p><strong>RecvVideoStreamsMax</strong></p></td>
<td><p>целое</p></td>
<td></td>
<td><p>Максимальное количество видеопотоков для получателя.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="even">
<td><p><strong>RecvVideoStreamsMin</strong></p></td>
<td><p>целое</p></td>
<td></td>
<td><p>Минимальный поток видеозаписи для получателя.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="odd">
<td><p><strong>RecvVideoStreamsMode</strong></p></td>
<td><p>целое</p></td>
<td></td>
<td><p>Режим видео (например, коллекция или один поток) получателя.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="even">
<td><p><strong>VideoPostFECPLR</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Применена ставка потери пакетов после исправления ошибки переадресации.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DynamicCapabilityPercent</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Процент времени, в течение которого был активен флаг динамической доступности.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="even">
<td><p><strong>ResolutionMin</strong></p></td>
<td><p>char (9)</p></td>
<td></td>
<td><p>Минимальное разрешение, измеряемое во время звонка.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="odd">
<td><p><strong>LowBitRateCallPercent</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Процент звонка ниже минимального порогового значения скорости (70 килобит в секунду).</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="even">
<td><p><strong>LowFrameRateCallPercent</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Процент звонка ниже нижнего порогового значения частоты кадров (количество кадров в 7,5 в секунду, входящее).</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="odd">
<td><p><strong>LowResolutionCallPercent</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Процент звонка, который выполнялся по низким разрешению.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="even">
<td><p><strong>DurationSeconds</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Продолжительность звонка в секундах.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="odd">
<td><p><strong>IsAggregatedData</strong></p></td>
<td><p>бит</p></td>
<td></td>
<td><p>Указывает, были ли данные объединены из нескольких вызовов.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

