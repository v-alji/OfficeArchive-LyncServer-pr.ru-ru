---
title: 'Lync Server 2013: таблица AudioStream'
description: 'Таблица Lync Server 2013: AudioStream.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: AudioStream table
ms:assetid: 49ccbbc3-2f73-45fc-80a6-e612535cbc10
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425961(v=OCS.15)
ms:contentKeyID: 48184077
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8af2e622e14c54fa4f9a6313e1b0dae8f2483132
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438178"
---
# <a name="audiostream-table-in-lync-server-2013"></a>Таблица AudioStream в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-10-02_

Каждая запись представляет собой один звуковой поток. Одна линейка звуковых файлов обычно состоит из двух звуковых потоков.


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
<td><p>На которую ссылается <a href="lync-server-2013-medialine-table.md">Таблица MediaLine в Lync Server 2013</a>.</p></td>
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
<td><p><strong>JitterInterArrival</strong></p></td>
<td><p>целое</p></td>
<td><p> </p></td>
<td><p>Средняя колебание сети из статистики протокола управления временем в реальном времени (RTCP).</p></td>
</tr>
<tr class="even">
<td><p><strong>JitterInterArrivalMax</strong></p></td>
<td><p>целое</p></td>
<td><p> </p></td>
<td><p>Максимальная колебание сети во время звонка.</p></td>
</tr>
<tr class="odd">
<td><p><strong>PacketLossRate</strong></p></td>
<td><p>десятичное число (5; 4)</p></td>
<td><p> </p></td>
<td><p>Средняя скорость потерь пакетов во время звонка.</p></td>
</tr>
<tr class="even">
<td><p><strong>PacketLossRateMax</strong></p></td>
<td><p>десятичное число (5; 4)</p></td>
<td><p> </p></td>
<td><p>Максимальное количество потерь пакетов, замеченное во время звонка.</p></td>
</tr>
<tr class="odd">
<td><p><strong>BurstDensity</strong></p></td>
<td><p>десятичное число (9; 4)</p></td>
<td><p> </p></td>
<td><p>Средняя плотность потери пакетов во время звонка.</p></td>
</tr>
<tr class="even">
<td><p><strong>BurstDuration</strong></p></td>
<td><p>целое</p></td>
<td><p> </p></td>
<td><p>Средняя продолжительность потери пакетов в течение заданных потерь во время звонка.</p></td>
</tr>
<tr class="odd">
<td><p><strong>BurstGapDensity</strong></p></td>
<td><p>десятичное число (9; 4)</p></td>
<td><p> </p></td>
<td><p>Средняя плотность потери пакетов при пропуске между пакетами потери данных.</p></td>
</tr>
<tr class="even">
<td><p><strong>BurstGapDuration</strong></p></td>
<td><p>целое</p></td>
<td><p> </p></td>
<td><p>Средняя продолжительность промежутков между пакетами потери данных.</p></td>
</tr>
<tr class="odd">
<td><p><strong>PacketUtilization</strong></p></td>
<td><p>Типом</p></td>
<td><p> </p></td>
<td><p>Число пакетов для аудиопотока.</p></td>
</tr>
<tr class="even">
<td><p><strong>Самый пропускная способность</strong></p></td>
<td><p>Типом</p></td>
<td><p> </p></td>
<td><p>Оценка пропускной способности для аудиопотока.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DegradationAvg</strong></p></td>
<td><p>десятичное число (3, 2)</p></td>
<td><p> </p></td>
<td><p>Сетевое MOS падение на весь звонок. Диапазон от 0,0 до 5,0. Этот показатель показывает объем сетевого MOS уменьшился из-за колебаний и потери пакетов. Для приемлемого качества оно должно быть менее 0,5.</p></td>
</tr>
<tr class="even">
<td><p><strong>DegradationMax</strong></p></td>
<td><p>десятичное число (3, 2)</p></td>
<td><p> </p></td>
<td><p>Максимальная длина сетевого MOS во время звонка.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DegradationJitterAvg</strong></p></td>
<td><p>десятичное число (3, 2)</p></td>
<td><p> </p></td>
<td><p>Снижение производительности сети MOS из – за колебаний.</p></td>
</tr>
<tr class="even">
<td><p><strong>DegradationPacketLossAvg</strong></p></td>
<td><p>десятичное число (3, 2)</p></td>
<td><p> </p></td>
<td><p>Снижение производительности сети MOS из – за потери пакетов.</p></td>
</tr>
<tr class="odd">
<td><p><strong>AudioPayloadDescription</strong></p></td>
<td><p>целое</p></td>
<td><p>Другом</p></td>
<td><p>Аудиокодек, использованный для вызова, на который ссылается таблица PayloadDescription.</p></td>
</tr>
<tr class="even">
<td><p><strong>AudioSampleRate</strong></p></td>
<td><p>целое</p></td>
<td><p> </p></td>
<td><p>Частота дискретизации для аудиопотока.</p></td>
</tr>
<tr class="odd">
<td><p><strong>RoundTrip</strong></p></td>
<td><p>целое</p></td>
<td><p> </p></td>
<td><p>Время кругового приема из статистики RTCP. Для приемлемого качества оно должно быть меньше 100ms.</p></td>
</tr>
<tr class="even">
<td><p><strong>RoundTripMax</strong></p></td>
<td><p>целое</p></td>
<td><p> </p></td>
<td><p>Максимальное время кругового приема для звукового потока.</p></td>
</tr>
<tr class="odd">
<td><p><strong>OverallAvgNetworkMOS</strong></p></td>
<td><p>десятичное число (3, 2)</p></td>
<td><p> </p></td>
<td><p>Средняя сетевая MOS широкополосному для звонка. Эта метрика зависит от потерь пакетов, колебаний и используемого кодека. Диапазон: [1,0 – 5,0].</p></td>
</tr>
<tr class="even">
<td><p><strong>OverallMinNetworkMOS</strong></p></td>
<td><p>десятичное число (3, 2)</p></td>
<td><p> </p></td>
<td><p>Минимальная широкополосному сеть MOS для звонка.</p></td>
</tr>
<tr class="odd">
<td><p><strong>SendListenMOS</strong></p></td>
<td><p>десятичное число (3, 2)</p></td>
<td><p> </p></td>
<td><p>Средний прогнозируемый широкополосному прослушивания MOS для звукового сигнала, в том числе уровней речи, уровней шума и характеристик устройства захвата.</p></td>
</tr>
<tr class="even">
<td><p><strong>SendListenMOSMin</strong></p></td>
<td><p>десятичное число (3, 2)</p></td>
<td><p> </p></td>
<td><p>Минимальная SendListenMOS для звонка.</p></td>
</tr>
<tr class="odd">
<td><p><strong>RecvListenMOS</strong></p></td>
<td><p>десятичное число (3, 2)</p></td>
<td><p> </p></td>
<td><p>Средний прогнозируемый широкополосному прослушивания MOS для звукового сигнала, получаемого из сети, включая уровень речи, уровень шума, кодек, условия сети и характеристики устройства захвата.</p></td>
</tr>
<tr class="even">
<td><p><strong>RecvListenMOSMin</strong></p></td>
<td><p>десятичное число (3, 2)</p></td>
<td><p> </p></td>
<td><p>Минимальная RecvListenMOS для звонка.</p></td>
</tr>
<tr class="odd">
<td><p><strong>AudioFECUsed</strong></p></td>
<td><p>бит</p></td>
<td></td>
<td><p>Флаг, указывающий, использовался ли для звонка звуковой FEC.</p></td>
</tr>
<tr class="even">
<td><p><strong>RatioConcealedSamplesAvg</strong></p></td>
<td><p>десятичное число (5; 2)</p></td>
<td></td>
<td><p>Среднее отношение количества преобразованных образцов, созданных при воспроизведении звука, на обычные выборки.</p></td>
</tr>
<tr class="odd">
<td><p><strong>RatioStretchedSamplesAvg</strong></p></td>
<td><p>десятичное число (5; 2)</p></td>
<td></td>
<td><p>Среднее отношение растянутых образцов, созданных при воспроизведении звука, на обычные выборки.</p></td>
</tr>
<tr class="even">
<td><p><strong>RatioCompressedSamplesAvg</strong></p></td>
<td><p>десятичное число (5; 2)</p></td>
<td></td>
<td><p>Среднее отношение количества сжатых образцов, созданных при восстановлении звука, на обычные образцы.</p></td>
</tr>
<tr class="odd">
<td><p><strong>443</strong></p></td>
<td><p>бит</p></td>
<td><p> </p></td>
<td><p>Получение потоковых данных на стороне получателя.</p></td>
</tr>
<tr class="even">
<td><p><strong>Исходящее</strong></p></td>
<td><p>бит</p></td>
<td><p> </p></td>
<td><p>Получение данных потока на стороне отправителя.</p></td>
</tr>
<tr class="odd">
<td><p><strong>SenderIsCallerPAI</strong></p></td>
<td><p>бит</p></td>
<td><p> </p></td>
<td><p>1 — направление потока на вызываемый абонентом.</p>
<p>0 — направление потока из вызываемого объекта вызывающему абоненту.</p></td>
</tr>
<tr class="even">
<td><p><strong>JitterInterArrivalSD</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Стандартное отклонение для наступления интервала ожидания.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="odd">
<td><p><strong>ConcealRatioMax</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Максимальное соотношение пакетов, которые скрываются с помощью восстанавливаемого экземпляра.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="even">
<td><p><strong>ConcealRatioSD</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Стандартное отклонение для соотношения пакетов, которые скрываются с помощью восстанавливаемого экземпляра.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="odd">
<td><p><strong>HealerPacketDropRatio</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Доля пакетов, отброшенных с помощью восстанавливаемого экземпляра по сравнению с общим количеством полученных пакетов.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="even">
<td><p><strong>HealerFECPacketUsedRatio</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Отношение использованных пакетов исправлений ошибок переадресации к общему количеству полученных пакетов.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="odd">
<td><p><strong>MaxCompressedSamples</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Максимальное количество звуковых пакетов, сжатых с помощью восстанавливаемого архива.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="even">
<td><p><strong>LossCongestionPercent</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Указывает процент времени, в течение которого Звонок находился в состоянии перегрузки с потерей.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DelayCongestionPercent</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Указывает процент вызова, в течение которого перегрузка была вызвана отложенным поступлением сетевых пакетов.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="even">
<td><p><strong>ContentionDetectedPercent</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Указывает процент времени, в течение которого Звонок конкурирует за ресурсы сети.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="odd">
<td><p><strong>BandwidthEstMin</strong></p></td>
<td><p>целое</p></td>
<td></td>
<td><p>Минимальная сумма оценки пропускной способности, измеряемая во время звонка.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="even">
<td><p><strong>BandwidthEstMax</strong></p></td>
<td><p>целое</p></td>
<td></td>
<td><p>Максимальная степень оценки пропускной способности, измеряемая во время звонка.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="odd">
<td><p><strong>BandwidthEstStdDev</strong></p></td>
<td><p>целое</p></td>
<td></td>
<td><p>Стандартное отклонение оценки пропускной способности, измеряемой во время звонка.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="even">
<td><p><strong>BandwidthEstAvge</strong></p></td>
<td><p>целое</p></td>
<td></td>
<td><p>Средняя сумма оценки пропускной способности, измеряемая во время звонка.</p>
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
<td><p>число с плавающей точкой</p></td>
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
<td><p><strong>DecodeStereoPercent</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Процент звонка, декодированный как стерео.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="odd">
<td><p><strong>AecRenderStereoPercent</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Процент звонка, выводимого в качестве стерео, с помощью отдавления акустического эха.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="even">
<td><p><strong>AudioPostFECPLR</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Применена ставка потери пакетов после исправления ошибки переадресации.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="odd">
<td><p><strong>EncodeStereoPercent</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Процент звонка, закодированный как стерео.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="even">
<td><p><strong>AecCaptureStereoPercent</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Процент звонка, захваченного как стерео, с помощью функции отмены акустического эха.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

