---
title: 'Lync Server 2013: таблица AppSharingMetricsThreshold'
description: 'Таблица Lync Server 2013: AppSharingMetricsThreshold.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: AppSharingMetricsThreshold table
ms:assetid: 782cfab9-01a6-4843-aea1-28f47b0b51f7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205018(v=OCS.15)
ms:contentKeyID: 48184556
ms.date: 12/09/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 092c7d08026e6b736b81043a71b4ecaabc4d5f1b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439874"
---
# <a name="appsharingmetricsthreshold-table-in-lync-server-2013"></a>Таблица AppSharingMetricsThreshold в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2015-12-08_

В таблице AppSharingMetricsThreshold содержатся оптимальные и приемлемые значения для показателей качества взаимодействия, используемых совместно с приложением. Эти пороговые значения используются, чтобы определить, следует ли классифицировать взаимодействие приложений как неудовлетворительные.

Эта таблица введена в Microsoft Lync Server 2013.


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
<td><p><strong>CallType</strong></p></td>
<td><p>целое</p></td>
<td><p>Primary</p></td>
<td><p>Тип размещенного звонка.</p></td>
</tr>
<tr class="even">
<td><p><strong>AppliedBandwidthLimitOptimal</strong></p></td>
<td><p>целое</p></td>
<td></td>
<td><p>Оптимальное ограничение пропускной способности для совместного использования приложений. Значение по умолчанию — 1000000.</p></td>
</tr>
<tr class="odd">
<td><p><strong>AppliedBandwidthLimitAcceptable</strong></p></td>
<td><p>целое</p></td>
<td></td>
<td><p>Допустимое ограничение пропускной способности для совместного использования приложений. Значение по умолчанию — 500000.</p></td>
</tr>
<tr class="even">
<td><p><strong>SpoiledTilePercentTotalOptimal</strong></p></td>
<td><p>десятичное число (5; 2)</p></td>
<td></td>
<td><p>Оптимальная процентная ставка для плиток "spoiled" для классификации качества общего использования приложения. Это значение — процент содержимого от общего доступа, которое не было доступно для просмотра. Содержимое может быть удалено (или spoiled), когда общий доступ отбрасывает плитки из источника графики, или ASMCU плитки отбрасывают плитки от общего доступа, соответственно. Значение по умолчанию составляет 11 процентов.</p></td>
</tr>
<tr class="odd">
<td><p><strong>SpoiledTilePercentTotalAcceptable</strong></p></td>
<td><p>десятичное число (5; 2)</p></td>
<td></td>
<td><p>cceptable процентная ставка для плиток "spoiled" для классификации качества общего использования приложения. Это значение — процент содержимого от общего доступа, которое не было доступно для просмотра. Содержимое может быть удалено (или spoiled), когда общий доступ отбрасывает плитки из источника графики, или ASMCU плитки отбрасывают плитки от общего доступа, соответственно. Значение по умолчанию составляет 36%.</p></td>
</tr>
<tr class="even">
<td><p><strong>JitterInterArrivalOptimal</strong></p></td>
<td><p>целое</p></td>
<td></td>
<td><p>Этот столбец не используется в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="odd">
<td><p><strong>JitterInterArrivalAcceptable</strong></p></td>
<td><p>целое</p></td>
<td></td>
<td><p>Этот столбец не используется в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="even">
<td><p><strong>RelativeOneWayBurstDensityOptimal</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Этот столбец не используется в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="odd">
<td><p><strong>RelativeOneWayBurstDensityAcceptable</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Этот столбец не используется в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="even">
<td><p><strong>RDPTileProcessingLatencyBurstDensityOptimal</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Этот столбец не используется в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="odd">
<td><p><strong>RDPTileProcessingLatencyBurstDensityAcceptable</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Этот столбец не используется в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="even">
<td><p><strong>RelativeOneWayAverageOptimal</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Оптимальное значение для относительной односторонней задержки между двумя конечными точками мультимедиа, задействованными в общем доступе к приложению. Это мера односкачковой задержки. Значение по умолчанию — 1,0 секунд.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="odd">
<td><p><strong>RelativeOneWayAverageAcceptable</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Оптимальное значение для относительной односторонней задержки между двумя конечными точками мультимедиа, задействованными в общем доступе к приложению. Это мера односкачковой задержки. Значение по умолчанию — 1,75 секунд.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="even">
<td><p><strong>RDPTileProcessingLatencyAverageOptimal</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Оптимальное значение средней задержки обработки плитки RDP на сервере конференций в течение сеанса просмотра. Задержка — это разница во времени между моментом, когда начальный кадр кодируется на сервере (в зависимости от сценария, или MCU, а также с помощью того же начального кадра декодируется в средстве просмотра).</p>
<p>Высокое среднее значение отражает более длительную задержку при просмотре. На перегруженном сервере конференц-связи могут происходить в среднем более длительные задержки. Значением по умолчанию является 200ms.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="odd">
<td><p><strong>RDPTileProcessingLatencyAverageAcceptable</strong></p></td>
<td><p>число с плавающей точкой</p></td>
<td></td>
<td><p>Допустимое значение средней задержки обработки плитки RDP на сервере конференций в течение сеанса просмотра. Задержка — это разница во времени между моментом, когда начальный кадр кодируется на сервере (в зависимости от сценария, или MCU, а также с помощью того же начального кадра декодируется в средстве просмотра).</p>
<p>Высокое среднее значение отражает более длительную задержку при просмотре. На перегруженном сервере конференц-связи могут происходить в среднем более длительные задержки. Значением по умолчанию является 200ms.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

