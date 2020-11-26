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
# <a name="appsharingstream-table-in-lync-server-2013"></a>Таблица AppSharingStream в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2014-02-21_

В таблице AppSharingStream содержатся показатели качества взаимодействия для сетевых потоков, используемых для совместного использования приложений. Эта таблица введена в Microsoft Lync Server 2013.


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
<td><p>Датой</p></td>
<td><p>Основной, внешний</p></td>
<td><p>Дата и время начала сеанса.</p></td>
</tr>
<tr class="even">
<td><p><strong>SessionSeq</strong></p></td>
<td><p>целое</p></td>
<td><p>Основной, внешний</p></td>
<td><p>Последовательный идентификатор, который используется для различения сеансов, запущенных в одну и ту же дату.</p></td>
</tr>
<tr class="odd">
<td><p><strong>MediaLineLabel</strong></p></td>
<td><p>tinyint</p></td>
<td><p>Основной, внешний</p></td>
<td><p>Представляет тип видеостроки, используемой в звонке. Допустимые значения:</p>
<ul>
<li><p>0 – звук</p></li>
<li><p>1 – видео</p></li>
<li><p>2 — панорамное видео</p></li>
<li><p>3 — общий доступ к приложениям и рабочим столам</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><strong>StreamID</strong></p></td>
<td><p>целое</p></td>
<td><p>Primary</p></td>
<td><p>Уникальный идентификатор потока общего просмотра приложения.</p></td>
</tr>
<tr class="odd">
<td><p><strong>JitterInterArrival</strong></p></td>
<td><p>целое</p></td>
<td></td>
<td><p>Среднее значение колебаний, зарегистрированных между прибытиями пакетов RTP. (Колебание — это мера &quot; shakiness &quot; звонка). Обычно значения с высокой степенью колебаний заключаются в результате перегруженности или перегруженного сервера мультимедиа, что приводит к искажению или потере звука.</p></td>
</tr>
<tr class="even">
<td><p><strong>JitterInterArrivalMax</strong></p></td>
<td><p>целое</p></td>
<td></td>
<td><p>Обнаружена максимальная колебание между поступлением пакетов RTP. (Колебание — это мера &quot; shakiness &quot; звонка). Обычно значения с высокой степенью колебаний заключаются в результате перегруженности или перегруженного сервера мультимедиа, что приводит к искажению или потере звука.</p></td>
</tr>
<tr class="odd">
<td><p><strong>RoundTrip</strong></p></td>
<td><p>целое</p></td>
<td></td>
<td><p>Среднее время (в миллисекундах), необходимое для перемещения пакета Real-Time Transport Protocol в другую конечную точку и его возврата. Приемлемым считается время двусторонней передачи, равное 200 мс (или менее).</p>
<p>Высокие значения времени двусторонней передачи могут быть обусловлены международной маршрутизацией вызовов, неправильной конфигурацией маршрутизации или перегрузкой сервера-посредника. Длительное время двусторонней передачи приводит к возникновению проблем при двусторонних аудиоразговорах в режиме реального времени.</p></td>
</tr>
<tr class="even">
<td><p><strong>RoundTripMax</strong></p></td>
<td><p>целое</p></td>
<td></td>
<td><p>Максимальный объем (в миллисекундах), необходимый для перемещения пакета Real-Time транспортного протокола на другую конечную точку, а затем обратно. Приемлемым считается время двусторонней передачи, равное 200 мс (или менее).</p>
<p>Высокие значения времени двусторонней передачи могут быть обусловлены международной маршрутизацией вызовов, неправильной конфигурацией маршрутизации или перегрузкой сервера-посредника. Длительное время двусторонней передачи приводит к возникновению проблем при двусторонних аудиоразговорах в режиме реального времени.</p></td>
</tr>
<tr class="odd">
<td><p><strong>PacketLossRate</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Средняя частота потери пакетов RTP. (Потеря пакетов происходит, когда пакеты RTP (Real-Time Transport Protocol — протокол, используемый для передачи аудио- и видеопакетов через Интернет) не достигают места назначения.) Высокие показатели потерь обычно вызваны перегрузкой, недостаточной полосой пропускания, помехами или перегрузкой беспроводной сети, а также перегрузкой сервера-посредника. Потеря пакетов обычно приводит к искажению звука или потере аудиосигналов.</p></td>
</tr>
<tr class="even">
<td><p><strong>PacketLossRateMax</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Максимальная частота потери пакетов на транспортном протоколе Real-Time (RTP). (Потеря пакетов происходит, когда пакеты RTP, протокол, используемый для передачи звука и видео через Интернет, не достигают места назначения.) Обычно тарифы на высокую степень потерь обусловлены перегрузкой; отсутствие пропускной способности; перегрузка беспроводной сети или помехи; или перегруженный сервер мультимедиа. Обычно это приводит к искажению или потере аудиосигнала.</p></td>
</tr>
<tr class="odd">
<td><p><strong>PacketUtilization</strong></p></td>
<td><p>целое</p></td>
<td></td>
<td><p>Количество отправленных пакетов.</p></td>
</tr>
<tr class="even">
<td><p><strong>Самый пропускная способность</strong></p></td>
<td><p>целое</p></td>
<td></td>
<td><p>Предполагаемая односторонняя пропускная способность, доступная в конце сеанса. Указывается в битах в секунду.</p></td>
</tr>
<tr class="odd">
<td><p><strong>AppSharingPayloadDescription</strong></p></td>
<td><p>целое</p></td>
<td></td>
<td><p>Описание полезных данных для общего использования приложений.</p></td>
</tr>
<tr class="even">
<td><p><strong>RelativeOneWayTotal</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Общая сумма односторонней задержки. Относительная односторонняя задержка измеряет задержку между клиентом и сервером.</p></td>
</tr>
<tr class="odd">
<td><p><strong>RelativeOneWayAverage</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Средняя величина односторонней задержки. Относительная односторонняя задержка измеряет задержку между клиентом и сервером.</p></td>
</tr>
<tr class="even">
<td><p><strong>RelativeOneWayMax</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Максимальная сумма односторонняя задержка. Относительная односторонняя задержка измеряет задержку между клиентом и сервером.</p></td>
</tr>
<tr class="odd">
<td><p><strong>RelativeOneWayBurstOccurrences</strong></p></td>
<td><p>целое</p></td>
<td></td>
<td><p>Общее количество односторонних вхождений. Одновременная передача данных — это передача, при которой данные передаются в непредсказуемые пакеты, а не в устойчивый поток. Этот показатель измеряет поток данных между клиентом и сервером.</p></td>
</tr>
<tr class="even">
<td><p><strong>RelativeOneWayBurstDensity</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Общая односторонняя плотность нагрузки. Одновременная передача данных — это передача, при которой данные передаются в непредсказуемые пакеты, а не в устойчивый поток. Этот показатель измеряет поток данных между клиентом и сервером.</p></td>
</tr>
<tr class="odd">
<td><p><strong>RelativeOneWayBurstDuration</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Общая продолжительность односторонней длительности. Одновременная передача данных — это передача, при которой данные передаются в непредсказуемые пакеты, а не в устойчивый поток. Этот показатель измеряет поток данных между клиентом и сервером.</p></td>
</tr>
<tr class="even">
<td><p><strong>RelativeOneWayGapOccurrences</strong></p></td>
<td><p>целое</p></td>
<td></td>
<td><p>Общее количество односторонних вхождений. Одновременная передача данных — это передача, при которой данные передаются в непредсказуемые пакеты, а не в устойчивый поток. зазоры указывают на задержку между этими пакетами. Этот показатель измеряет поток данных между клиентом и сервером.</p></td>
</tr>
<tr class="odd">
<td><p><strong>RelativeOneWayGapDensity</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Общая плотность односторонних зазоров. Одновременная передача данных — это передача, при которой данные передаются в непредсказуемые пакеты, а не в устойчивый поток. зазоры указывают на задержку между этими пакетами. Этот показатель измеряет поток данных между клиентом и сервером.</p></td>
</tr>
<tr class="even">
<td><p><strong>RelativeOneWayGapDuration</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Общая продолжительность односторонних промежутков. Одновременная передача данных — это передача, при которой данные передаются в непредсказуемые пакеты, а не в устойчивый поток. зазоры указывают на задержку между этими пакетами. Этот показатель измеряет поток данных между клиентом и сервером.</p></td>
</tr>
<tr class="odd">
<td><p><strong>ApplicationSharingType</strong></p></td>
<td><p>varChar (256)</p></td>
<td></td>
<td><p>Роль приложения (общий доступ или средство просмотра) и тип контента.</p></td>
</tr>
<tr class="even">
<td><p><strong>RDPTileProcessingLatencyTotal</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Общее время обработки плиток протокола удаленного рабочего стола (RDP). Общая сумма равна более длительной задержке при просмотре.</p></td>
</tr>
<tr class="odd">
<td><p><strong>RDPTileProcessingLatencyAverage</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Среднее время обработки плиток протокола удаленного рабочего стола (RDP). Общая сумма равна более длительной задержке при просмотре.</p></td>
</tr>
<tr class="even">
<td><p><strong>RDPTileProcessingLatencyMax</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Максимальное время обработки плиток протокола удаленного рабочего стола (RDP). Общая сумма равна более длительной задержке при просмотре.</p></td>
</tr>
<tr class="odd">
<td><p><strong>RDPTileProcessingLatencyBurstOccurrences</strong></p></td>
<td><p>целое</p></td>
<td></td>
<td><p>Пакетное повторение на время обработки плиток протокола удаленного рабочего стола (RDP). Одновременная передача данных — это передача, при которой данные передаются в непредсказуемые пакеты, а не в устойчивый поток.</p></td>
</tr>
<tr class="even">
<td><p><strong>RDPTileProcessingLatencyBurstDensity</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Ускоренная плотность плиток протокола удаленного рабочего стола (RDP) на время обработки. Одновременная передача данных — это передача, при которой данные передаются в непредсказуемые пакеты, а не в устойчивый поток.</p></td>
</tr>
<tr class="odd">
<td><p><strong>RDPTileProcessingLatencyBurstDuration</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Продолжительность разбивки на время обработки плиток протокола удаленного рабочего стола (RDP). Одновременная передача данных — это передача, при которой данные передаются в непредсказуемые пакеты, а не в устойчивый поток.</p></td>
</tr>
<tr class="even">
<td><p><strong>RDPTileProcessingLatencyGapOccurrences</strong></p></td>
<td><p>целое</p></td>
<td></td>
<td><p>Случаи пропуска на момент обработки плиток протокола удаленного рабочего стола (RDP).</p></td>
</tr>
<tr class="odd">
<td><p><strong>RDPTileProcessingLatencyGapDensity</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Плотность зазоров во время обработки плиток протокола удаленного рабочего стола (RDP). Плотность неограниченного промежутка означает более качественный просмотр.</p></td>
</tr>
<tr class="even">
<td><p><strong>RDPTileProcessingLatencyGapDuration</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Продолжительность пропуска для плиток протокола удаленного рабочего стола (RDP). Продолжительность коротких промежутков эквивалентна более качественному просмотру.</p></td>
</tr>
<tr class="odd">
<td><p><strong>CaptureTileRateTotal</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Общая частота захваченных плиток (в плитках в секунду).</p></td>
</tr>
<tr class="even">
<td><p><strong>CaptureTileRateAverage</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Средняя скорость захваченных плиток (в плитках в секунду).</p></td>
</tr>
<tr class="odd">
<td><p><strong>CaptureTileRateMax</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Максимальная частота захваченных плиток (в плитках в секунду).</p></td>
</tr>
<tr class="even">
<td><p><strong>CaptureTileRateBurstOccurrences</strong></p></td>
<td><p>в t</p></td>
<td></td>
<td><p>Пакетное повторение в частоте захваченных плиток (в плитках в секунду).</p></td>
</tr>
<tr class="odd">
<td><p><strong>CaptureTileRateBurstDensity</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Плотность разбивки на захваченные плитки (в плитках в секунду).</p></td>
</tr>
<tr class="even">
<td><p><strong>CaptureTileRateBurstDuration</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Продолжительность разбивки на собранные плитки (в плитках в секунду).</p></td>
</tr>
<tr class="odd">
<td><p><strong>CaptureTileRateGapOccurrences</strong></p></td>
<td><p>целое</p></td>
<td></td>
<td><p>Количество повторений в частоте захваченных плиток (в плитках в секунду).</p></td>
</tr>
<tr class="even">
<td><p><strong>CaptureTileRateGapDensity</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Плотность зазоров в процентах захваченных плиток (в плитках в секунду).</p></td>
</tr>
<tr class="odd">
<td><p><strong>CaptureTileRateGapDuration</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Продолжительность зазора в процентах собранных плиток (в плитках в секунду).</p></td>
</tr>
<tr class="even">
<td><p><strong>SpoiledTilePercentTotal</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Общий процент содержимого, которое не было получено средством просмотра, но было бы удалено и заменено новым содержимым.</p></td>
</tr>
<tr class="odd">
<td><p><strong>SpoiledTilePercentAverage</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Средний процент содержимого, которое не достиго средства просмотра, но было удалено и заменено новым содержимым.</p></td>
</tr>
<tr class="even">
<td><p><strong>SpoiledTilePercentMax</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Максимальный процент содержимого, которое не было получено средством просмотра, но было бы удалено и заменено новым содержимым.</p></td>
</tr>
<tr class="odd">
<td><p><strong>SpoiledTilePercentBurstOccurrences</strong></p></td>
<td><p>целое</p></td>
<td></td>
<td><p>Пакетное повторение для содержимого, которое не достиго средства просмотра, а было удалено и заменено новым содержимым.</p></td>
</tr>
<tr class="even">
<td><p><strong>SpoiledTilePercentBurstDensity</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Для содержимого, которое не достигают средства просмотра, оно было удалено и заменено новым содержимым.</p></td>
</tr>
<tr class="odd">
<td><p><strong>SpoiledTilePercentBurstDuration</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Продолжительность разбивки на содержимое, которое не было получено средством просмотра, но было бы удалено и заменено новым содержимым.</p></td>
</tr>
<tr class="even">
<td><p><strong>SpoiledTilePercentGapOccurrences</strong></p></td>
<td><p>целое</p></td>
<td></td>
<td><p>Повторение для содержимого, которое не достиго средства просмотра, но было удалено и заменено новым содержимым.</p></td>
</tr>
<tr class="odd">
<td><p><strong>SpoiledTilePercentGapDensity</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Плотность зазоров для содержимого, которое не достиго средства просмотра, но было удалено и заменено новым содержимым.</p></td>
</tr>
<tr class="even">
<td><p><strong>SpoiledTilePercentGapDuration</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Продолжительность зазора для содержимого, которое не достиго средства просмотра, но было удалено и заменено новым содержимым.</p></td>
</tr>
<tr class="odd">
<td><p><strong>ScrapingFrameRateTotal</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Общее количество кадров, набракованных из источника графики.</p></td>
</tr>
<tr class="even">
<td><p><strong>ScrapingFrameRateAverage</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Среднее количество кадров, набракованных из источника графики.</p></td>
</tr>
<tr class="odd">
<td><p><strong>ScrapingFrameRateMax</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Предельное число кадров, которые не побраковано от источника графики.</p></td>
</tr>
<tr class="even">
<td><p><strong>ScrapingFrameRateBurstOccurrences</strong></p></td>
<td><p>целое</p></td>
<td></td>
<td><p>Пакетное повторение в кадре побраковано от источника графики.</p></td>
</tr>
<tr class="odd">
<td><p><strong>ScrapingFrameRateBurstDensity</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Ускоренная плотность кадров в кадрах, побракованных из источника графики.</p></td>
</tr>
<tr class="even">
<td><p><strong>ScrapingFrameRateBurstDuration</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Продолжительность разбивки кадров в кадре, побракованная от источника графики.</p></td>
</tr>
<tr class="odd">
<td><p><strong>ScrapingFrameRateGapOccurrences</strong></p></td>
<td><p>целое</p></td>
<td></td>
<td><p>Случаи разрывов в кадрах оббракованы из источника графики.</p></td>
</tr>
<tr class="even">
<td><p><strong>ScrapingFrameRateGapDensity</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Плотность зазоров в кадрах, побракованных из источника графики.</p></td>
</tr>
<tr class="odd">
<td><p><strong>ScrapingFrameRateGapDuration</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Продолжительность зазора в кадрах, побракованных из источника графики.</p></td>
</tr>
<tr class="even">
<td><p><strong>IncomingTileRateTotal</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Общая частота входящих кадров, полученных средством просмотра.</p></td>
</tr>
<tr class="odd">
<td><p><strong>IncomingTileRateAverage</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Средняя частота входящих кадров, полученная средством просмотра.</p></td>
</tr>
<tr class="even">
<td><p><strong>IncomingTileRateMax</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Максимальное количество входящих частот плиток, полученных средством просмотра.</p></td>
</tr>
<tr class="odd">
<td><p><strong>IncomingTileRateBurstOccurrences</strong></p></td>
<td><p>целое</p></td>
<td></td>
<td><p>Пакетное повторение входящего, полученного средством просмотра частоты плиток.</p></td>
</tr>
<tr class="even">
<td><p><strong>IncomingTileRateBurstDensity</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Многоуровневая плотность во входящих частотах плиток, полученных средством просмотра.</p></td>
</tr>
<tr class="odd">
<td><p><strong>IncomingTileRateBurstDuration</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Продолжительность пакетной обработки на входящем частоте плиток, полученной средством просмотра.</p></td>
</tr>
<tr class="even">
<td><p><strong>IncomingTileRateGapOccurrences</strong></p></td>
<td><p>целое</p></td>
<td></td>
<td><p>Количество вхождений во входящих частотах плиток, полученных средством просмотра.</p></td>
</tr>
<tr class="odd">
<td><p><strong>IncomingTileRateGapDensity</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Плотность просветов во входящих частотах плиток, полученных средством просмотра.</p></td>
</tr>
<tr class="even">
<td><p><strong>IncomingTileRateGapDuration</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Длительность пропуска во входящих частотах плиток, полученных средством просмотра.</p></td>
</tr>
<tr class="odd">
<td><p><strong>IncomingFrameRateTotal</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Общая частота входящих кадров, полученных средством просмотра.</p></td>
</tr>
<tr class="even">
<td><p><strong>IncomingFrameRateAverage</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Средняя частота входящих кадров, полученная средством просмотра.</p></td>
</tr>
<tr class="odd">
<td><p><strong>IncomingFrameRateMax</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Максимальная частота поступающих кадров, полученных средством просмотра.</p></td>
</tr>
<tr class="even">
<td><p><strong>IncomingFrameRateBurstOccurrences</strong></p></td>
<td><p>целое</p></td>
<td></td>
<td><p>Пакетное повторение во входящих частотах кадров, полученных средством просмотра.</p></td>
</tr>
<tr class="odd">
<td><p><strong>IncomingFrameRateBurstDensity</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Многоуровневая плотность во входящих частотах кадров, полученных средством просмотра.</p></td>
</tr>
<tr class="even">
<td><p><strong>IncomingFrameRateBurstDuration</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Продолжительность многочастотной обработки кадров, полученная средством просмотра.</p></td>
</tr>
<tr class="odd">
<td><p><strong>IncomingFrameRateGapOccurrences</strong></p></td>
<td><p>целое</p></td>
<td></td>
<td><p>Пропуск вхождений во входной частоте кадров, полученной средством просмотра.</p></td>
</tr>
<tr class="even">
<td><p><strong>IncomingFrameRateGapDensity</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Плотность зазоров во входящих частотах кадров, полученных средством просмотра.</p></td>
</tr>
<tr class="odd">
<td><p><strong>IncomingFrameRateDuration</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Длительность промежутка во входящих частотах кадров, полученных средством просмотра.</p></td>
</tr>
<tr class="even">
<td><p><strong>OutgoingTileRateTotal</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Общая частота исходящих плиток для отправителя.</p></td>
</tr>
<tr class="odd">
<td><p><strong>OutgoingTileRateAverage</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Средняя исходящая частота плиток для отправителя.</p></td>
</tr>
<tr class="even">
<td><p><strong>OutgoingTileRateMax</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Максимальная исходящая ставка плиток для отправителя.</p></td>
</tr>
<tr class="odd">
<td><p><strong>OutgoingTileRateBurstOccurrences</strong></p></td>
<td><p>целое</p></td>
<td></td>
<td><p>Пакетное повторение исходящих плиток для отправителя.</p></td>
</tr>
<tr class="even">
<td><p><strong>OutgoingTileRateBurstDensity</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Плотность разбивки на выходящую частоту плиток для отправителя.</p></td>
</tr>
<tr class="odd">
<td><p><strong>OutgoingTileRateBurstDuration</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Продолжительность разбивки на исходящую частоту плиток для отправителя.</p></td>
</tr>
<tr class="even">
<td><p><strong>OutgoingTileRateGapOccurrences</strong></p></td>
<td><p>целое</p></td>
<td></td>
<td><p>Количество повторений в исходящих частотах плиток для отправителя.</p></td>
</tr>
<tr class="odd">
<td><p><strong>OutgoingTileRateGapDensity</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Плотность зазоров для отправителя за исходящую частоту плиток.</p></td>
</tr>
<tr class="even">
<td><p><strong>OutgoingTileRateGapDuration</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Продолжительность зазора для отправителя с исходящим рейтингом.</p></td>
</tr>
<tr class="odd">
<td><p><strong>OutgoingFrameRateTotal</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Общая частота исходящих кадров для отправителя.</p></td>
</tr>
<tr class="even">
<td><p><strong>OutgoingFrameRateAverage</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>средняя исходящая частота кадров для отправителя.</p></td>
</tr>
<tr class="odd">
<td><p><strong>OutgoingFrameRateMax</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Максимальная исходящая частота кадров для отправителя.</p></td>
</tr>
<tr class="even">
<td><p><strong>OutgoingFrameRateBurstOccurrences</strong></p></td>
<td><p>целое</p></td>
<td></td>
<td><p>Пакетное повторение в исходящих частотах кадров для отправителя.</p></td>
</tr>
<tr class="odd">
<td><p><strong>OutgoingFrameRateBurstDensity</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>В исходящих частотах кадров для отправителя — это пакетная плотность.</p></td>
</tr>
<tr class="even">
<td><p><strong>OutgoingFrameRateBurstDuration</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Продолжительность разбивки кадров в исходящей частотной скорости для отправителя.</p></td>
</tr>
<tr class="odd">
<td><p><strong>OutgoingFrameRateGapOccurrences</strong></p></td>
<td><p>целое</p></td>
<td></td>
<td><p>Количество повторений в исходящей частоте кадров для отправителя.</p></td>
</tr>
<tr class="even">
<td><p><strong>OutgoingFrameRateGapDensity</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Плотность зазоров в исходящих частотах кадров для отправителя.</p></td>
</tr>
<tr class="odd">
<td><p><strong>OutgoingFrameRateGapDuration</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Длительность промежутка в исходящих частотах кадров для отправителя.</p></td>
</tr>
<tr class="even">
<td><p><strong>AverageRectangleHeight</strong></p></td>
<td><p>целое</p></td>
<td></td>
<td><p>Средняя высота разрешающей способности видео (в пикселях).</p></td>
</tr>
<tr class="odd">
<td><p><strong>AverageRectangleWidth</strong></p></td>
<td><p>целое</p></td>
<td></td>
<td><p>Средняя ширина разрешающей способности видео в пикселях.</p></td>
</tr>
<tr class="even">
<td><p><strong>443</strong></p></td>
<td><p>бит</p></td>
<td></td>
<td><p>Средняя частота кадров (в кадрах в секунду) для входящих передач.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Исходящее</strong></p></td>
<td><p>бит</p></td>
<td></td>
<td><p>Средняя частота кадров (в кадрах в секунду) для исходящих передач.</p></td>
</tr>
<tr class="even">
<td><p><strong>SenderIsCallerPAI</strong></p></td>
<td><p>бит</p></td>
<td></td>
<td><p>1 — направление потока для вызываемого абонента.</p>
<p>0 — направление потока из вызываемого объекта вызывающему абоненту.</p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

