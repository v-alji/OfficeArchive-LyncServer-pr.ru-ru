---
title: 'Lync Server 2013: таблица AudioClientEvent'
description: 'Таблица Lync Server 2013: AudioClientEvent.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: AudioClientEvent table
ms:assetid: fef73d8f-7261-4e5b-9769-82435b007979
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413086(v=OCS.15)
ms:contentKeyID: 48185967
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2200cd9567bdd10ac4ad8f5c269062c2f5614dcb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438212"
---
# <a name="audioclientevent-table-in-lync-server-2013"></a>Таблица AudioClientEvent в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-10-17_

Каждая запись имеет событие клиента для одной конечной точки в голосовой видеозвонке. Обычно один звонок состоит из двух записей: одного для вызывающего и для вызываемого абонента.


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
<td><p><strong>FromCaller</strong></p></td>
<td><p>бит</p></td>
<td><p>Primary</p></td>
<td><p>0: данные вызывающего абонента</p>
<p>1: данные вызывающего абонента</p></td>
</tr>
<tr class="odd">
<td><p><strong>NetworkSendQualityEventRatio</strong></p></td>
<td><p>десятичное число (5; 2)</p></td>
<td><p> </p></td>
<td><p>Процент сеанса, когда событие NetworkSendQuality было инициировано для состояния "Bad".</p>
<p>Качество сети в условиях нарушения или потери пакетов является серьезным и повлияет на качество отправляемого звука.</p></td>
</tr>
<tr class="even">
<td><p><strong>NetworkReceiveQualityEventRatio</strong></p></td>
<td><p>десятичное число (5; 2)</p></td>
<td><p> </p></td>
<td><p>Процент сеанса, когда событие ReceiveSendQuality было инициировано для состояния "Bad".</p>
<p>Качество сети в условиях нарушения или потери пакетов является серьезным и повлияет на качество получаемого звука.</p></td>
</tr>
<tr class="odd">
<td><p><strong>NetworkDelayEventRatio</strong></p></td>
<td><p>десятичное число (5; 2)</p></td>
<td><p> </p></td>
<td><p>Процент сеанса. событие задержки было инициировано для состояния "Bad". Задержка сети является серьезной и повлияет на работу, предотвращая интерактивную связь</p></td>
</tr>
<tr class="even">
<td><p><strong>NetworkBandwidthLowEventRatio</strong></p></td>
<td><p>десятичное число (5; 2)</p></td>
<td><p> </p></td>
<td><p>Процент сеанса, когда событие LowBandwidth было инициировано для состояния "Bad". Доступная пропускная способность недостаточна для приемлемого голосового интерфейса.</p></td>
</tr>
<tr class="odd">
<td><p><strong>CPUInsufficientEventRatio</strong></p></td>
<td><p>десятичное число (5; 2)</p></td>
<td><p> </p></td>
<td><p>Процент пропускной ошибки ЦП, недостаточный для состояния "Bad". Недостаточно циклов ЦП для обработки с текущими модальностей и используемыми приложениями. Это приводит к искажениям канала звука.</p></td>
</tr>
<tr class="even">
<td><p><strong>DeviceHalfDuplexAECEventRatio</strong></p></td>
<td><p>десятичное число (5; 2)</p></td>
<td><p> </p></td>
<td><p>Процент сеанса, когда событие DeviceHalfDuplexAEC было инициировано для состояния "Bad". В целях предотвращения эхо-эха система вводит двухстороннюю двустороннюю печать.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DeviceRenderNotFunctioningEventRatio</strong></p></td>
<td><p>десятичное число (5; 2)</p></td>
<td><p> </p></td>
<td><p>Процент сеанса, когда событие DeviceRenderNotFunctioning было инициировано для состояния "Bad". Устройство рендеринга, используемое в данный момент для сеанса, работает неправильно. Это может привести к появлению односторонней голосовой проблемы.</p></td>
</tr>
<tr class="even">
<td><p><strong>DeviceCaptureNotFunctioningEventRatio</strong></p></td>
<td><p>десятичное число (5; 2)</p></td>
<td><p> </p></td>
<td><p>Процент сеанса, когда событие DeviceCaptureNotFunctioning было инициировано для состояния "Bad". Устройство захвата, используемое в сеансе, не работает должным образом. Это может привести к появлению односторонней голосовой проблемы.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DeviceGlitchesEventRatio</strong></p></td>
<td><p>десятичное число (5; 2)</p></td>
<td><p> </p></td>
<td><p>Процент сеанса, когда событие DeviceGlitches было инициировано для состояния "Bad". При отрисовке звука возникают серьезные проблемы, вызывающие искажения. Это может быть вызвано проблемами с драйверами, отложенными вызовами процедур (DPC) (Drivers) и высокой загрузкой ЦП.</p></td>
</tr>
<tr class="even">
<td><p><strong>DeviceLowSNREventRatio</strong></p></td>
<td><p>десятичное число (5; 2)</p></td>
<td><p> </p></td>
<td><p>Процент сеанса, когда событие DeviceLowSNR было инициировано для состояния "Bad". Качество захвата очень низкое, но очень шумный или пользовательский разговор слишком далеко от микрофона. Это вызовет искажения.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DeviceLowSpeechLevelEventRatio</strong></p></td>
<td><p>десятичное число (5; 2)</p></td>
<td><p> </p></td>
<td><p>Процент сеанса, когда событие DeviceLowSpeechLevel было инициировано для состояния "Bad". Слишком низкий уровень речи пользователя, система не может увеличить его. Это может вызвать либо искажение или восприятие в качестве односторонней голосовой.</p></td>
</tr>
<tr class="even">
<td><p><strong>DeviceClippingEventRatio</strong></p></td>
<td><p>Десятичное число (5; 2)</p></td>
<td><p> </p></td>
<td><p>Процент сеанса, когда событие DeviceClipping было инициировано для состояния "Bad".</p>
<p>При использовании близких между собой видеороликов микрофон прозвучит искажения из-за обрезки. Важно избегать вырезки близких микрофонов.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DeviceEchoEventRatio</strong></p></td>
<td><p>десятичное число (5; 2)</p></td>
<td><p> </p></td>
<td><p>Процент сеанса, когда событие DeviceEchoEvent было инициировано для состояния "Bad". Устройство или Настройка вызывают эхо за пределами способности системы компенсировать.</p></td>
</tr>
<tr class="even">
<td><p><strong>DeviceNearEndToEchoRatioEventRatio</strong></p></td>
<td><p>десятичное число (5; 2)</p></td>
<td><p> </p></td>
<td><p>Процент сеанса, когда событие DeviceNearEndToEchoRatio было инициировано для состояния "Bad". Голосовая речь пользователя слишком мала по сравнению с записанным эхо-эффектом, что влияет на работу пользователей, так как оно ограничивает возможности прерывания пользователя. Уменьшить громкость динамика, передвиньте микрофон ближе к разговору.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DeviceMultipleEndpointsEventCount</strong></p></td>
<td><p>целое</p></td>
<td></td>
<td><p>Количество ситуаций, в которых событие DeviceMultipleEndpoints было инициировано для состояния "Bad". Обнаружено несколько конечных точек звука в одном сеансе и компенсация системы была произведена с помощью уменьшения объема рендеринга.</p></td>
</tr>
<tr class="even">
<td><p><strong>DeviceHowlingEventCount</strong></p></td>
<td><p>целое</p></td>
<td><p> </p></td>
<td><p>Количество ситуаций, в которых событие DeviceHowlingEvent было инициировано для состояния "Bad". Обнаружен цикл обратной связи (это связано с тем, что несколько конечных точек совместно поддерживают звуковой путь).</p></td>
</tr>
<tr class="odd">
<td><p><strong>DeviceRenderZeroVolumeEventRatio</strong></p></td>
<td><p>десятичное число (5; 2)</p></td>
<td></td>
<td><p>Процент сеанса. событие DeviceRenderZeroVolume было инициировано в состоянии Bad. Для устройства обработки было установлено нулевое значение "Громкость".</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="even">
<td><p><strong>DeviceRenderMuteEventRatio</strong></p></td>
<td><p>десятичное число (5; 2)</p></td>
<td></td>
<td><p>Процент сеанса. событие DeviceRenderMute было инициировано в состоянии Bad. Устройство рендеринга отключено.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

