---
title: 'Lync Server 2013: представление AudioStreamDetail'
description: 'Lync Server 2013: AudioStreamDetail View.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: AudioStreamDetail view
ms:assetid: b6a435b3-103c-41c4-96ed-33c3784534c0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721859(v=OCS.15)
ms:contentKeyID: 49733792
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 92c4c9bbb4f126e242e28d835222f6ba2af89d8b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438164"
---
# <a name="audiostreamdetail-view-in-lync-server-2013"></a>AudioStreamDetail представления в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-10-03_

В представлении AudioStreamDetail хранятся сведения о каждом звуковом потоке в базе данных. Это представление было представлено в Microsoft Lync Server 2013.


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Столбец</th>
<th>Тип данных</th>
<th>Подробности</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>SessionTime</p></td>
<td><p>datetime</p></td>
<td><p>На которую ссылается <a href="lync-server-2013-medialine-table.md">Таблица MediaLine в Lync Server 2013</a>.</p></td>
</tr>
<tr class="even">
<td><p>SessionSeq</p></td>
<td><p>целое</p></td>
<td><p>На которую ссылается <a href="lync-server-2013-medialine-table.md">Таблица MediaLine в Lync Server 2013</a>.</p></td>
</tr>
<tr class="odd">
<td><p>StreamId</p></td>
<td><p>целое</p></td>
<td><p>Уникальный идентификатор в строке мультимедиа.</p></td>
</tr>
<tr class="even">
<td><p>StartTime</p></td>
<td><p>datetime</p></td>
<td><p>Время начала сеанса.</p></td>
</tr>
<tr class="odd">
<td><p>EndTime</p></td>
<td><p>datetime</p></td>
<td><p>Время окончания сеанса.</p></td>
</tr>
<tr class="even">
<td><p>DialogCategory</p></td>
<td><p>бит</p></td>
<td><p>Категория диалоговых окон: 0 — сервер Lync Server — серверное средство для устранения проблем; 1 — это сервер, на котором выдается посредник для шлюза PSTN.</p></td>
</tr>
<tr class="odd">
<td><p>MediationServerBypassFlag</p></td>
<td><p>бит</p></td>
<td><p>Флаг, указывающий, обходит ли звонок.</p></td>
</tr>
<tr class="even">
<td><p>MediaBypassWarningFlag</p></td>
<td><p>целое</p></td>
<td><p>Если указано, указывает, почему звонок не обходится, даже если идентификаторы обхода не совпадают. Определено только одно значение:</p>
<p>0x0001 — Неизвестный идентификатор обхода для сетевого адаптера по умолчанию.</p></td>
</tr>
<tr class="odd">
<td><p>CallPriority</p></td>
<td><p>целое</p></td>
<td><p>Приоритет звонка.</p></td>
</tr>
<tr class="even">
<td><p>CallerPool</p></td>
<td><p>nvarchar(256)</p></td>
<td><p>Полное доменное имя пула вызывающего абонента.</p></td>
</tr>
<tr class="odd">
<td><p>CalleePool</p></td>
<td><p>nvarchar(256)</p></td>
<td><p>Полное доменное имя пула вызываемых абонентов.</p></td>
</tr>
<tr class="even">
<td><p>Вызывающая сторона</p></td>
<td><p>nvarchar (450)</p></td>
<td><p>URI вызывающего абонента.</p></td>
</tr>
<tr class="odd">
<td><p>Вызываемая сторона</p></td>
<td><p>nvarchar (450)</p></td>
<td><p>Универсальный код ресурса (URI) вызываемого абонента.</p></td>
</tr>
<tr class="even">
<td><p>CallerUserAgent</p></td>
<td><p>nvarchar(256)</p></td>
<td><p>Строка агента пользователя вызывающего абонента.</p></td>
</tr>
<tr class="odd">
<td><p>CallerUserAgentType</p></td>
<td><p>smallint</p></td>
<td><p>Тип агента пользователя вызывающего абонента. Дополнительные сведения: <a href="lync-server-2013-useragent-table.md">Таблица UserAgent в Lync Server 2013</a> .</p></td>
</tr>
<tr class="even">
<td><p>CallerUserAgentCategory</p></td>
<td><p>nvarchar (64)</p></td>
<td><p>Категория агента пользователя вызывающего абонента. Дополнительные сведения <a href="lync-server-2013-useragentdef-table-qoe.md">UserAgentDef в таблице "QoE" в Lync Server 2013</a> .</p></td>
</tr>
<tr class="odd">
<td><p>CalleeUserAgent</p></td>
<td><p>nvarchar(256)</p></td>
<td><p>Строка агента пользователя вызываемого абонента.</p></td>
</tr>
<tr class="even">
<td><p>CalleeUserAgentType</p></td>
<td><p>smallint</p></td>
<td><p>Тип агента пользователя, вызываемого абонентом. Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-useragent-table.md">таблицей UserAgent в Lync Server 2013</a> .</p></td>
</tr>
<tr class="odd">
<td><p>CalleeUserAgentCategory</p></td>
<td><p>nvarchar (64)</p></td>
<td><p>Категория агента пользователя вызываемого абонента. Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-useragentdef-table-qoe.md">таблицей UserAgentDef (QoE) в Lync Server 2013</a> .</p></td>
</tr>
<tr class="even">
<td><p>CallerEndpoint</p></td>
<td><p>nvarchar(256)</p></td>
<td><p>Имя конечной точки вызывающего абонента.</p></td>
</tr>
<tr class="odd">
<td><p>CalleeEndpoint</p></td>
<td><p>nvarchar(256)</p></td>
<td><p>Имя конечной точки вызываемого абонента.</p></td>
</tr>
<tr class="even">
<td><p>CallerOS</p></td>
<td><p>nvarchar(128</p></td>
<td><p>Операционная система (ОС) конечной точки вызывающего абонента.</p></td>
</tr>
<tr class="odd">
<td><p>CalleeOS</p></td>
<td><p>nvarchar(128</p></td>
<td><p>Операционная система (ОС) конечной точки вызываемого абонента.</p></td>
</tr>
<tr class="even">
<td><p>CallerCPUName</p></td>
<td><p>nvarchar(128</p></td>
<td><p>Имя ЦП конечной точки вызывающего абонента.</p></td>
</tr>
<tr class="odd">
<td><p>CalleeCPUName</p></td>
<td><p>nvarchar(128</p></td>
<td><p>Имя ЦП конечной точки вызываемого абонента.</p></td>
</tr>
<tr class="even">
<td><p>CallerCPUNumberOfCores</p></td>
<td><p>smallint</p></td>
<td><p>Количество ядер ЦП в конечной точке вызывающего абонента.</p></td>
</tr>
<tr class="odd">
<td><p>CalleeCPUNumberOfCores</p></td>
<td><p>smallint</p></td>
<td><p>Количество ядер ЦП в конечной точке вызываемого абонента.</p></td>
</tr>
<tr class="even">
<td><p>CallerCPUProcessorSpeed</p></td>
<td><p>целое</p></td>
<td><p>Частота процессора конечной точки вызывающего абонента.</p></td>
</tr>
<tr class="odd">
<td><p>CalleeCPUProcessorSpeed</p></td>
<td><p>целое</p></td>
<td><p>Тактовая частота процессора на конечной точке вызываемого абонента.</p></td>
</tr>
<tr class="even">
<td><p>CallerVirtualizationFlag</p></td>
<td><p>tinyint</p></td>
<td><p>Указывает, работает ли система вызывающего абонента в виртуализованной среде. Дополнительные сведения приведены <a href="lync-server-2013-endpoint-table.md">в таблице конечная точка в Lync Server 2013</a> .</p></td>
</tr>
<tr class="odd">
<td><p>CalleeVirtualizationFlag</p></td>
<td><p>tinyint</p></td>
<td><p>Указывает, работает ли система вызываемого абонента в виртуализованной среде. Дополнительные сведения приведены <a href="lync-server-2013-endpoint-table.md">в таблице конечная точка в Lync Server 2013</a> .</p></td>
</tr>
<tr class="even">
<td><p>CorrelationKey</p></td>
<td></td>
<td><p>Ключ корреляции. На которую ссылается <a href="lync-server-2013-sessioncorrelation-table.md">Таблица SessionCorrelation в Lync Server 2013</a>.</p></td>
</tr>
<tr class="odd">
<td><p>ConnectivityIce</p></td>
<td><p>tinyint</p></td>
<td><p>Информация о пути к носителю, например прямая или ретранслируемая. Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-medialine-table.md">таблицей MediaLine в Lync Server 2013</a> .</p></td>
</tr>
<tr class="even">
<td><p>CallerIceWarningFlags</p></td>
<td><p>целое</p></td>
<td><p>Сведения о процессе интерактивной установки подключения (ICE), описанные в разделе Флаги BITS для вызывающего абонента. Подробности можно найти в спецификации серверного протокола контроля качества обслуживания.</p></td>
</tr>
<tr class="odd">
<td><p>CalleeIceWarningFlags</p></td>
<td><p>целое</p></td>
<td><p>Сведения о процессе установки интерактивной связи (ICE), описанные в флагах BITS для вызываемого абонента. Подробности можно найти в спецификации серверного протокола контроля качества обслуживания.</p></td>
</tr>
<tr class="even">
<td><p>Transport</p></td>
<td><p>tinyint</p></td>
<td><p>Тип транспорта: 0 — UDP, 1 — TCP.</p></td>
</tr>
<tr class="odd">
<td><p>CallerIPAddr</p></td>
<td><p>var (50)</p></td>
<td><p>IP-адрес вызывающего абонента. Это может быть либо IPv4, либо IPv6-адрес.</p></td>
</tr>
<tr class="even">
<td><p>CallerPort</p></td>
<td><p>целое</p></td>
<td><p>Порт, используемый вызывающим абонентом.</p></td>
</tr>
<tr class="odd">
<td><p>CallerInside</p></td>
<td><p>бит</p></td>
<td><p>Указывает, находится ли вызывающий объект в сети Interval: 1 означает, что вызывающий абонент входит в корпоративную сеть, а 0 означает, что вызывающий абонент находится за пределами сети.</p></td>
</tr>
<tr class="even">
<td><p>CalleeIPAddr</p></td>
<td><p>var (50)</p></td>
<td><p>IP-адрес вызываемого абонента. Это может быть либо IPv4, либо IPv6-адрес.</p></td>
</tr>
<tr class="odd">
<td><p>CalleePort</p></td>
<td><p>целое</p></td>
<td><p>Порт, используемый вызываемым абонентом.</p></td>
</tr>
<tr class="even">
<td><p>CalleeInside</p></td>
<td><p>бит</p></td>
<td><p>Указывает, находится ли вызывающий объект в сети Interval: 1 означает, что вызываемый абонент входит в корпоративную сеть, а 0 означает, что вызываемый объект находится за пределами сети.</p></td>
</tr>
<tr class="odd">
<td><p>CallerUserSite</p></td>
<td><p>nvarchar(128</p></td>
<td><p>Имя сайта вызывающего абонента.</p></td>
</tr>
<tr class="even">
<td><p>CallerRegion</p></td>
<td><p>nvarchar(128</p></td>
<td><p>Название страны или региона сайта вызывающего абонента.</p></td>
</tr>
<tr class="odd">
<td><p>CalleeUserSite</p></td>
<td><p>nvarchar(128</p></td>
<td><p>Имя сайта вызываемого абонента.</p></td>
</tr>
<tr class="even">
<td><p>CalleeRegion</p></td>
<td><p>nvarchar(128</p></td>
<td><p>Название страны или региона сайта вызываемого абонента.</p></td>
</tr>
<tr class="odd">
<td><p>CallerRelayIPAddr</p></td>
<td><p>var (50)</p></td>
<td><p>IP-адрес службы EDGE (/V), используемой вызывающим абонентом. Дополнительные сведения приведены в <a href="lync-server-2013-ipaddress-table.md">таблице IP-адрес в Lync Server 2013</a> .</p></td>
</tr>
<tr class="even">
<td><p>CallerRelayPort</p></td>
<td><p>целое</p></td>
<td><p>Порт, используемый в службе EDGE (A/V), используемой вызывающим абонентом.</p></td>
</tr>
<tr class="odd">
<td><p>CalleeRelayIPAddr</p></td>
<td><p>var (50)</p></td>
<td><p>Ключ IP-адреса для службы EDGE (/V), используемой вызываемым абонентом. Дополнительные сведения приведены в <a href="lync-server-2013-ipaddress-table.md">таблице IP-адрес в Lync Server 2013</a> .</p></td>
</tr>
<tr class="even">
<td><p>CalleeRelayPort</p></td>
<td><p>целое</p></td>
<td><p>Порт, используемый в службе EDGE (A/V), используемой вызываемым абонентом.</p></td>
</tr>
<tr class="odd">
<td><p>CallerCaptureDev</p></td>
<td><p>varchar (256)</p></td>
<td><p>Имя устройства захвата вызывающего абонента.</p></td>
</tr>
<tr class="even">
<td><p>CallerRenderDev</p></td>
<td><p>varchar (256)</p></td>
<td><p>Имя устройства отрисовки вызывающего абонента.</p></td>
</tr>
<tr class="odd">
<td><p>CallerCaptureDevDriver</p></td>
<td><p>varchar (256)</p></td>
<td><p>Имя драйвера устройства захвата вызывающего абонента.</p></td>
</tr>
<tr class="even">
<td><p>CallerRenderDriver</p></td>
<td><p>varchar (256)</p></td>
<td><p>Имя драйвера устройства отрисовки вызывающего абонента.</p></td>
</tr>
<tr class="odd">
<td><p>CalleeCaptureDev</p></td>
<td><p>varchar (256)</p></td>
<td><p>Имя устройства захвата абонента.</p></td>
</tr>
<tr class="even">
<td><p>CalleeRenderDev</p></td>
<td><p>varchar (256)</p></td>
<td><p>Имя устройства отрисовки вызываемого абонента.</p></td>
</tr>
<tr class="odd">
<td><p>CalleeCaptureDevDriver</p></td>
<td><p>varchar (256)</p></td>
<td><p>Имя драйвера устройства захвата абонента.</p></td>
</tr>
<tr class="even">
<td><p>CalleeRenderDevDriver</p></td>
<td><p>varchar (256)</p></td>
<td><p>Имя драйвера устройства обработки вызываемого абонента.</p></td>
</tr>
<tr class="odd">
<td><p>CallerNetworkConnectionType</p></td>
<td><p>tinyint</p></td>
<td><p>Тип сетевого подключения вызывающего абонента: 0 проводное соединение, 1 — Беспроводная связь.</p></td>
</tr>
<tr class="even">
<td><p>CallerVPN</p></td>
<td><p>бит</p></td>
<td><p>Указывает, подключен ли вызывающий абонент к виртуальной частной сети: 1 — виртуальная частная сеть (VPN), 0 — не VPN.</p></td>
</tr>
<tr class="odd">
<td><p>CallerLinkSpeed</p></td>
<td><p>десятичное число (18; 0)</p></td>
<td><p>Скорость сетевого соединения для конечной точки вызывающего абонента бит/с.</p></td>
</tr>
<tr class="even">
<td><p>CalleeNetworkConnectionType</p></td>
<td><p>tinyint</p></td>
<td><p>Тип сетевого подключения абонента: 0 – проводное, 1 — Беспроводная связь.</p></td>
</tr>
<tr class="odd">
<td><p>CalleeVPN</p></td>
<td><p>бит</p></td>
<td><p>Указывает, подключен ли вызывающий абонент к виртуальной частной сети: 1 — виртуальная частная сеть (VPN), 0 — не VPN.</p></td>
</tr>
<tr class="even">
<td><p>CalleeLinkSpeed</p></td>
<td><p>десятичное число (18; 0)</p></td>
<td><p>Скорость сетевого соединения для конечной точки вызываемого абонента бит/с.</p></td>
</tr>
<tr class="odd">
<td><p>ConversationalMOS</p></td>
<td><p>десятичное число (3, 2)</p></td>
<td><p>Narrowband MOS из сеансов голосовой связи (на основе обоих звуковых потоков).</p></td>
</tr>
<tr class="even">
<td><p>AppliedBandwidthLimit</p></td>
<td><p>целое</p></td>
<td><p>Реальная пропускная способность, примененная к потоку отправки данных в соответствии с различными параметрами политики (например, "повернуть", "API", SDP, сервер политики и т. д.). Это не следует путать с эффективной пропускной способностью, так как в зависимости от оценки пропускной способности может снизиться эффективная пропускная способность. Это является, по сути, максимальной пропускной способностью потока отправки, который может занимать ограничения пропускной способности, наложенные на эту оценку.</p></td>
</tr>
<tr class="odd">
<td><p>JitterInterArrival</p></td>
<td><p>целое</p></td>
<td><p>Средняя колебание сети из статистики протокола управления временем в реальном времени (RTCP).</p></td>
</tr>
<tr class="even">
<td><p>JitterInterArrivalMax</p></td>
<td><p>целое</p></td>
<td><p>Максимальная колебание сети во время звонка.</p></td>
</tr>
<tr class="odd">
<td><p>PacketLossRate</p></td>
<td><p>десятичное число (5; 4)</p></td>
<td><p>Средняя скорость потерь пакетов во время звонка.</p></td>
</tr>
<tr class="even">
<td><p>PacketLossRateMax</p></td>
<td><p>десятичное число (5; 4)</p></td>
<td><p>Максимальное количество потерь пакетов, замеченное во время звонка.</p></td>
</tr>
<tr class="odd">
<td><p>BurstDensity</p></td>
<td><p>десятичное число (9; 4)</p></td>
<td><p>Средняя плотность потери пакетов во время звонка.</p></td>
</tr>
<tr class="even">
<td><p>BurstDuration</p></td>
<td><p>целое</p></td>
<td><p>Средняя продолжительность потери пакетов в течение заданных потерь во время звонка.</p></td>
</tr>
<tr class="odd">
<td><p>BurstGapDensity</p></td>
<td><p>десятичное число (9; 4)</p></td>
<td><p>Средняя плотность потери пакетов при пропуске между пакетами потери данных.</p></td>
</tr>
<tr class="even">
<td><p>BurstGapDuration</p></td>
<td><p>целое</p></td>
<td><p>Средняя продолжительность промежутков между пакетами потери данных.</p></td>
</tr>
<tr class="odd">
<td><p>PacketUtilization</p></td>
<td><p>целое</p></td>
<td><p>Число пакетов для аудиопотока.</p></td>
</tr>
<tr class="even">
<td><p>Самый пропускная способность</p></td>
<td><p>целое</p></td>
<td><p>Оценка пропускной способности для аудиопотока.</p></td>
</tr>
<tr class="odd">
<td><p>DegradationAvg</p></td>
<td><p>десятичное число (3, 2)</p></td>
<td><p>Сетевое MOS падение на весь звонок. Диапазон от 0,0 до 5,0. Этот показатель показывает объем сетевого MOS уменьшился из-за колебаний и потери пакетов. Для приемлемого качества оно должно быть менее 0,5.</p></td>
</tr>
<tr class="even">
<td><p>DegradationMax</p></td>
<td><p>десятичное число (3, 2)</p></td>
<td><p>Максимальная длина сетевого MOS во время звонка.</p></td>
</tr>
<tr class="odd">
<td><p>DegradationJitterAvg</p></td>
<td><p>десятичное число (3, 2)</p></td>
<td><p>Снижение производительности сети MOS из – за колебаний.</p></td>
</tr>
<tr class="even">
<td><p>DegradationPacketLossAvg</p></td>
<td><p>десятичное число (3, 2)</p></td>
<td><p>Снижение производительности сети MOS из – за потери пакетов.</p></td>
</tr>
<tr class="odd">
<td><p>PayloadDescription</p></td>
<td><p>целое</p></td>
<td><p>Аудиокодек, использованный для вызова, на который ссылается <a href="lync-server-2013-payloaddescription-table.md">Таблица PayloadDescription в Lync Server 2013</a>.</p></td>
</tr>
<tr class="even">
<td><p>AudioSampleRate</p></td>
<td><p>целое</p></td>
<td><p>Частота дискретизации для аудиопотока.</p></td>
</tr>
<tr class="odd">
<td><p>CallerSendSignalLevel</p></td>
<td><p>целое</p></td>
<td><p>Уровень звукового сигнала, выступающем после аналогового усиления, для звука, отправленного вызывающим абонентом. Единицей измерения для этой метрики является dBmo. Для приемлемого качества оно должно быть не менее 30 dBmo. Этот показатель не передается сервером Конференции и IP-телефонами по протоколу A/V.</p></td>
</tr>
<tr class="even">
<td><p>CallerRecvSignalLevel</p></td>
<td><p>целое</p></td>
<td><p>Уровень звукового сигнала для звука, полученного вызывающим абонентом. Единицей измерения для этой метрики является dBmo. Для приемлемого качества оно должно быть не менее 30 dBmo. Этот показатель не передается сервером Конференции и IP-телефонами по протоколу A/V.</p></td>
</tr>
<tr class="odd">
<td><p>CallerSendNoiseLevel</p></td>
<td><p>целое</p></td>
<td><p>После аналогового усиления контрольного шума для звука, который отправляет вызывающий абонент. Единицей измерения для этой метрики является dBmo. Для приемлемого качества оно должно быть менее 35 dBmo. Этот показатель не передается сервером Конференции и IP-телефонами по протоколу A/V.</p></td>
</tr>
<tr class="even">
<td><p>CallerRecvNoiseLevel</p></td>
<td><p>целое</p></td>
<td><p>Звуковой шум по контролю звукового сопровождения для звукового сигнала, полученного вызывающим абонентом. Единицей измерения для этой метрики является dBmo. Для приемлемого качества оно должно быть менее 35 dBmo. Этот показатель не передается сервером Конференции и IP-телефонами по протоколу A/V.</p></td>
</tr>
<tr class="odd">
<td><p>CallerEchoReturn</p></td>
<td><p>целое</p></td>
<td><p>Для вызывающего абонента возводится расширение возвращающего эха. Единицей измерения для этой метрики является dB. Более низкие значения представляют менее эхо. Этот показатель не передается сервером Конференции и IP-телефонами по протоколу A/V.</p></td>
</tr>
<tr class="even">
<td><p>CallerSpeakerGlitchRate</p></td>
<td><p>целое</p></td>
<td><p>Среднее число сбоев в течение пяти минут для отрисовки динамик вызывающего абонента. Для хорошего качества это должно быть меньше, чем один за пять минут. Не сообщается серверам конференц-связи, серверам или IP-телефонам.</p></td>
</tr>
<tr class="odd">
<td><p>CallerMicGlitchRate</p></td>
<td><p>целое</p></td>
<td><p>Среднее число сбоев в течение пяти минут для захвата микрофона вызывающего абонента. Для хорошего качества это должно быть менее чем на одну 5 минут. Не сообщается серверам конференц-связи, серверам или IP-телефонам.</p></td>
</tr>
<tr class="even">
<td><p>CallerTimestampDriftRateMic</p></td>
<td><p>десятичное число (9, 2)</p></td>
<td><p>Частота отсчета часов микрофона вызывающего устройства, относящихся к тактовой частоте процессора.</p></td>
</tr>
<tr class="odd">
<td><p>CallerTimestampDriftRateSpk</p></td>
<td><p>десятичное число (9, 2)</p></td>
<td><p>Частота отсчета сигналов для динамиков устройства выступающего в сторону от времени ЦП.</p></td>
</tr>
<tr class="even">
<td><p>CallerTimestampErrorMicMs</p></td>
<td><p>десятичное число (9, 2)</p></td>
<td><p>Средняя пометка времени потока захвата микрофона в миллисекундах за последние 20 секунд звонка.</p></td>
</tr>
<tr class="odd">
<td><p>CallerTimestampErrorSpkMs</p></td>
<td><p>десятичное число (9, 2)</p></td>
<td><p>Среднее значение ошибки метки времени линейного отображения динамика вызывающего абонента в миллисекундах за последние 20 секунд звонка.</p></td>
</tr>
<tr class="even">
<td><p>CallerVsEntryCauses</p></td>
<td><p>smallint</p></td>
<td><p>Голосовая связь — это режим двусторонней печати с ограниченными возможностями перерывов. Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-medialine-table.md">таблицей MediaLine в Lync Server 2013</a> .</p></td>
</tr>
<tr class="odd">
<td><p>CallerEchoEventCauses</p></td>
<td><p>tinyint</p></td>
<td><p>Причины возникновения события echo для вызывающего абонента. Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-medialine-table.md">таблицей MediaLine в Lync Server 2013</a> .</p></td>
</tr>
<tr class="even">
<td><p>CallerEchoPercentMicIn</p></td>
<td><p>десятичное число (5; 2)</p></td>
<td><p>Процент времени, в течение которого обнаружено эхо в потоке захвата микрофона вызывающего абонента. Если используется гарнитура, значение должно быть низким.</p></td>
</tr>
<tr class="odd">
<td><p>CallerEchoPercentSend</p></td>
<td><p>десятичное число (5; 2)</p></td>
<td><p>Процент времени, в течение которого обнаружено эхо в потоке, отправленном вызывающим абонентом. Высокий процент эха в потоках отправки указывает на наличие утечки эха.</p></td>
</tr>
<tr class="even">
<td><p>CallerRxAGCSignalLevel</p></td>
<td><p>целое</p></td>
<td><p>Уровень сигнала на сервере-источнике сообщений от шлюза к звуку вызывающего абонента; Это относится только к серверу обновлений. Единица измерения этой метрики — dBoV. Для хорошего качества допустимый диапазон должен составлять от-30 до-18 dBoV.</p></td>
</tr>
<tr class="odd">
<td><p>CallerRxAGCNoiseLevel</p></td>
<td><p>целое</p></td>
<td><p>Уровень сигнала на сервере-источнике от шлюза для звука вызывающего абонента. Это относится только к серверу обновлений. Единица измерения этой метрики — dBoV. Для хорошего качества допустимый диапазон должен быть меньше, чем-50 dBoV.</p></td>
</tr>
<tr class="even">
<td><p>CallerRxAGCGain</p></td>
<td><p>целое</p></td>
<td><p>Автоматический контроль усиления (AGC) на стороне сервера-посредника, примененной к звуковому каналу вызывающего абонента.</p></td>
</tr>
<tr class="odd">
<td><p>CallerInitialSignalLevelRMS</p></td>
<td><p>число с плавающей точкой</p></td>
<td><p>Среднее значение среднего квадрата входящего сигнала для вызывающего абонента до первых 30 секунд звонка.</p></td>
</tr>
<tr class="even">
<td><p>CalleeSendSignalLevel</p></td>
<td><p>целое</p></td>
<td><p>Представляет уровень звукового сигнала после аналогового усиления для звука, отправленного вызываемым абонентом. Единицей измерения для этой метрики является dBmo. Для приемлемого качества оно должно быть не менее 30 dBmo. Этот показатель не передается сервером Конференции и IP-телефонами по протоколу A/V.</p></td>
</tr>
<tr class="odd">
<td><p>CalleeRecvSignalLevel</p></td>
<td><p>целое</p></td>
<td><p>Уровень звукового сигнала для звука, полученного вызываемым абонентом. Единицей измерения для этой метрики является dBmo. Для приемлемого качества оно должно быть не менее 30 dBmo. Этот показатель не передается сервером Конференции и IP-телефонами по протоколу A/V.</p></td>
</tr>
<tr class="even">
<td><p>CalleeSendNoiseLevel</p></td>
<td><p>целое</p></td>
<td><p>После аналогового усиления контрольного шума для звука, отправленного вызываемым абонентом. Единицей измерения для этой метрики является dBmo. Для приемлемого качества оно должно быть менее 35 dBmo. Этот показатель не передается сервером Конференции и IP-телефонами по протоколу A/V.</p></td>
</tr>
<tr class="odd">
<td><p>CalleeRecvNoiseLevel</p></td>
<td><p>целое</p></td>
<td><p>После аналогового усиления контрольного шума для звука, полученного вызывающим абонентом, на уровне звука. Единицей измерения для этой метрики является dBmo. Для приемлемого качества оно должно быть менее 35 dBmo. Этот показатель не передается сервером Конференции и IP-телефонами по протоколу A/V.</p></td>
</tr>
<tr class="even">
<td><p>CalleeEchoReturn</p></td>
<td><p>целое</p></td>
<td><p>Для вызываемого функции возвращаются улучшения с потерей эха. Единицей измерения для этой метрики является dB. Более низкие значения представляют менее эхо. Этот показатель не передается сервером Конференции и IP-телефонами по протоколу A/V.</p></td>
</tr>
<tr class="odd">
<td><p>CalleeSpeakerGlitchRate</p></td>
<td><p>целое</p></td>
<td><p>Среднее число сбоев в течение пяти минут для отрисовки динамик вызываемого абонента. Для хорошего качества это должно быть меньше, чем один за пять минут. Не сообщается серверам конференц-связи, серверам или IP-телефонам.</p></td>
</tr>
<tr class="even">
<td><p>CalleeMicGlitchRate</p></td>
<td><p>целое</p></td>
<td><p>Среднее число сбоев в течение пяти минут для захвата микрофона вызывающего абонента. Для хорошего качества это должно быть менее чем на одну 5 минут. Не сообщается серверам конференц-связи, серверам или IP-телефонам.</p></td>
</tr>
<tr class="odd">
<td><p>CalleeTimestampDriftRateMic</p></td>
<td><p>десятичное число (9, 2)</p></td>
<td><p>Частота отсчета часов микрофона для вызываемого абонента в соответствии с тактовой частотой процессора.</p></td>
</tr>
<tr class="even">
<td><p>CalleeTimestampDriftRateSpk</p></td>
<td><p>десятичное число (9, 2)</p></td>
<td><p>Частота отсчета звукового сигнала устройства вызываемого абонента в соответствии с тактовой частотой процессора.</p></td>
</tr>
<tr class="odd">
<td><p>CalleeTimestampErrorMicMs</p></td>
<td><p>десятичное число (9, 2)</p></td>
<td><p>Средняя пометка времени потока захвата микрофона в миллисекундах за последние 20 секунд звонка.</p></td>
</tr>
<tr class="even">
<td><p>CalleeTimestampErrorSpkMs</p></td>
<td><p>десятичное число (9, 2)</p></td>
<td><p>Среднее сообщение об ошибке пометки времени линейного отображения динамика в миллисекундах за последние 20 секунд звонка.</p></td>
</tr>
<tr class="odd">
<td><p>CalleeVsEntryCauses</p></td>
<td><p>smallint</p></td>
<td><p>Голосовая связь — это режим двусторонней печати с ограниченными возможностями перерывов. Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-medialine-table.md">таблицей MediaLine в Lync Server 2013</a> .</p></td>
</tr>
<tr class="even">
<td><p>CalleeEchoEventCauses</p></td>
<td><p>tinyint</p></td>
<td><p>Причины возникновения события echo для вызываемого объекта. Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-medialine-table.md">таблицей MediaLine в Lync Server 2013</a> .</p></td>
</tr>
<tr class="odd">
<td><p>CalleeEchoPercentMicIn</p></td>
<td><p>десятичное число (5; 2)</p></td>
<td><p>Процент времени, когда в потоке захвата микрофона вызываемого абонента будет обнаружено эхо. Если используется гарнитура, значение должно быть низким.</p></td>
</tr>
<tr class="even">
<td><p>CalleeEchoPercentSend</p></td>
<td><p>десятичное число (5; 2)</p></td>
<td><p>Процент времени, в течение которого обнаружено эхо в потоке, отправленном вызываемым абонентом. Высокий процент эха в потоках отправки указывает на наличие утечки эха.</p></td>
</tr>
<tr class="odd">
<td><p>CalleeRxAGCSignalLevel</p></td>
<td><p>целое</p></td>
<td><p>Уровень сигнала на сервере-посреднике от шлюза для звука вызываемого абонента; Это относится только к серверу обновлений. Единица измерения этой метрики — dBoV. Для хорошего качества допустимый диапазон должен составлять от [-30 до-18] dBoV.</p></td>
</tr>
<tr class="even">
<td><p>CalleeRxAGCNoiseLevel</p></td>
<td><p>целое</p></td>
<td><p>Уровень сигнала на сервере-посреднике от шлюза к звуковому каналу вызываемого абонента. Это относится только к серверу обновлений. Единица измерения этой метрики — dBoV. Для хорошего качества допустимый диапазон должен быть меньше, чем-50 dBoV.</p></td>
</tr>
<tr class="odd">
<td><p>CalleeRxAGCGain</p></td>
<td><p>целое</p></td>
<td><p>Функция автоматического усиления доступа (AGC) на стороне сервера-посредника, примененная к звуковому каналу вызываемого абонента.</p></td>
</tr>
<tr class="even">
<td><p>CalleeInitialSignalLevelRMS</p></td>
<td><p>число с плавающей точкой</p></td>
<td><p>Среднее значение среднего квадрата (RMS) входящего сигнала для вызываемого абонента до первых 30 секунд звонка.</p></td>
</tr>
<tr class="odd">
<td><p>RatioConcealedSamplesAvg</p></td>
<td><p>десятичное число (5; 2)</p></td>
<td><p>Среднее отношение количества преобразованных образцов, созданных при воспроизведении звука, на обычные выборки.</p></td>
</tr>
<tr class="even">
<td><p>RatioStretchedSamplesAvg</p></td>
<td><p>десятичное число (5; 2)</p></td>
<td><p>Среднее отношение растянутых образцов, созданных при воспроизведении звука, на обычные выборки.</p></td>
</tr>
<tr class="odd">
<td><p>RatioCompressedSamplesAvg</p></td>
<td><p>десятичное число (5; 2)</p></td>
<td><p>Среднее отношение количества сжатых образцов, созданных при восстановлении звука, на обычные образцы.</p></td>
</tr>
<tr class="even">
<td><p>RoundTrip</p></td>
<td><p>целое</p></td>
<td><p>Время кругового приема из статистики RTCP.</p></td>
</tr>
<tr class="odd">
<td><p>RoundTripMax</p></td>
<td><p>целое</p></td>
<td><p>Максимальное время кругового приема для звукового потока.</p></td>
</tr>
<tr class="even">
<td><p>OverallAvgNetworkMOS</p></td>
<td><p>десятичное число (3, 2)</p></td>
<td><p>Средняя сетевая MOS широкополосному для звонка. Эта метрика зависит от потерь пакетов, колебаний и используемого кодека. Диапазон от 1,0 до 5,0.</p></td>
</tr>
<tr class="odd">
<td><p>OverallMinNetworkMOS</p></td>
<td><p>десятичное число (3, 2)</p></td>
<td><p>Минимальная широкополосному сети MOS для звонка.</p></td>
</tr>
<tr class="even">
<td><p>SendListenMOS</p></td>
<td><p>десятичное число (3, 2)</p></td>
<td><p>Средняя прогнозируемая широкополосному прослушивания MOS для звукового сигнала, в том числе уровней речи, шума и характеристик устройства захвата.</p></td>
</tr>
<tr class="odd">
<td><p>SendListenMOSMin</p></td>
<td><p>десятичное число (3, 2)</p></td>
<td><p>Минимальная SendListenMOS для звонка.</p></td>
</tr>
<tr class="even">
<td><p>RecvListenMOS</p></td>
<td><p>десятичное число (3, 2)</p></td>
<td><p>Средняя прогнозируемая широкополосному прослушивания MOS для звуковых сообщений, полученных из сети, включая уровень речи, уровень шума, кодек, условия сети и характеристики устройства захвата.</p></td>
</tr>
<tr class="odd">
<td><p>RecvListenMOSMin</p></td>
<td><p>десятичное число (3, 2)</p></td>
<td><p>Минимальная RecvListenMOS для звонка.</p></td>
</tr>
<tr class="even">
<td><p>AudioFECUsed</p></td>
<td><p>бит</p></td>
<td><p>Указывает, был ли использован голосовой FEC для звонка.</p></td>
</tr>
<tr class="odd">
<td><p>SenderIsCallerPAI</p></td>
<td><p>бит</p></td>
<td><p>Указывает направление, в котором определяются p-утвержденные сведения; 1 — направление потока на вызываемый абонентом. 0 — направление потока из вызываемого объекта вызывающему абоненту.</p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

