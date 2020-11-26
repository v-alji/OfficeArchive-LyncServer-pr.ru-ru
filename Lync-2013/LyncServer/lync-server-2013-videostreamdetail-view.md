---
title: 'Lync Server 2013: представление VideoStreamDetail'
description: 'Lync Server 2013: VideoStreamDetail View.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: VideoStreamDetail view
ms:assetid: ec8c45e1-307d-40ec-a75e-6083306105f2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721928(v=OCS.15)
ms:contentKeyID: 49733863
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a3f420c292627d15fd0d54f2eba01c565a49a72d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443428"
---
# <a name="videostreamdetail-view-in-lync-server-2013"></a>VideoStreamDetail представления в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-10-03_

В представлении VideoStreamDetail хранятся сведения о каждом видеопотоке в базе данных. Это представление было представлено в Microsoft Lync Server 2013.


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
<th>Описание</th>
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
<td><p>MediaLineLabel</p></td>
<td><p>tinyint</p></td>
<td><p>На которую ссылается <a href="lync-server-2013-medialine-table.md">Таблица MediaLine в Lync Server 2013</a>.</p></td>
</tr>
<tr class="even">
<td><p>StreamId</p></td>
<td><p>целое</p></td>
<td><p>Уникальный идентификатор в строке мультимедиа.</p></td>
</tr>
<tr class="odd">
<td><p>StartTime</p></td>
<td><p>datetime</p></td>
<td><p>Время начала сеанса.</p></td>
</tr>
<tr class="even">
<td><p>EndTime</p></td>
<td><p>datetime</p></td>
<td><p>Время окончания сеанса.</p></td>
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
<td><p>Количество ядер ЦП конечной точки вызывающего абонента.</p></td>
</tr>
<tr class="odd">
<td><p>CalleeCPUNumberOfCores</p></td>
<td><p>smallint</p></td>
<td><p>Количество ядер ЦП конечной точки вызываемого абонента.</p></td>
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
<td><p>ConnectivityIce</p></td>
<td><p>tinyint</p></td>
<td><p>Сведения о пути к носителю, например прямая или ретранслируемая. Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-medialine-table.md">таблицей MediaLine в Lync Server 2013</a> .</p></td>
</tr>
<tr class="odd">
<td><p>CallerIceWarningFlags</p></td>
<td><p>целое</p></td>
<td><p>Сведения о процессе интерактивной установки подключения (ICE), описанные в разделе Флаги BITS для вызывающего абонента. Подробности можно найти в спецификации серверного протокола контроля качества обслуживания.</p></td>
</tr>
<tr class="even">
<td><p>CalleeIceWarningFlags</p></td>
<td><p>целое</p></td>
<td><p>Сведения о процессе установки интерактивной связи (ICE), описанные в флагах BITS для вызываемого абонента. Подробности можно найти в спецификации серверного протокола контроля качества обслуживания.</p></td>
</tr>
<tr class="odd">
<td><p>Transport</p></td>
<td><p>целое</p></td>
<td><p>Тип транспорта: 0 — UDP, 1 — TCP.</p></td>
</tr>
<tr class="even">
<td><p>CallerIPAddr</p></td>
<td><p>var (50)</p></td>
<td><p>IP-адрес вызывающего абонента. Это может быть либо IPv4, либо IPv6-адрес.</p></td>
</tr>
<tr class="odd">
<td><p>CallerPort</p></td>
<td><p>целое</p></td>
<td><p>Порт, используемый вызывающим абонентом.</p></td>
</tr>
<tr class="even">
<td><p>CallerInside</p></td>
<td><p>бит</p></td>
<td><p>Указывает, находится ли вызывающий абонент в сети Организации. 1 означает, что вызывающий абонент входит в корпоративную сеть, а 0 означает, что вызывающий абонент находится за пределами сети.</p></td>
</tr>
<tr class="odd">
<td><p>CalleeIPAddr</p></td>
<td><p>var (50)</p></td>
<td><p>IP-адрес вызываемого абонента. Это может быть либо IPv4, либо IPv6-адрес.</p></td>
</tr>
<tr class="even">
<td><p>CalleePort</p></td>
<td><p>целое</p></td>
<td><p>Порт, используемый вызываемым абонентом.</p></td>
</tr>
<tr class="odd">
<td><p>CalleeInside</p></td>
<td><p>бит</p></td>
<td><p>Указывает, входит ли вызывающий объект в сеть Организации. 1 означает вызываемый абонент в корпоративной сети, 0 означает, что вызываемый абонент находится за пределами сети.</p></td>
</tr>
<tr class="even">
<td><p>CallerUserSite</p></td>
<td><p>nvarchar(128</p></td>
<td><p>Имя сайта вызывающего абонента.</p></td>
</tr>
<tr class="odd">
<td><p>CallerRegion</p></td>
<td><p>nvarchar(128</p></td>
<td><p>Название страны или региона сайта вызывающего абонента.</p></td>
</tr>
<tr class="even">
<td><p>CalleeUserSite</p></td>
<td><p>nvarchar(128</p></td>
<td><p>Имя сайта вызываемого абонента.</p></td>
</tr>
<tr class="odd">
<td><p>CalleeRegion</p></td>
<td><p>nvarchar(128</p></td>
<td><p>Название страны или региона сайта вызываемого абонента.</p></td>
</tr>
<tr class="even">
<td><p>CallerRelayIPAddr</p></td>
<td><p>var (50)</p></td>
<td><p>IP-адрес службы EDGE (/V), используемой вызывающим абонентом. Дополнительные сведения приведены в <a href="lync-server-2013-ipaddress-table.md">таблице IP-адрес в Lync Server 2013</a> .</p></td>
</tr>
<tr class="odd">
<td><p>CallerRelayPort</p></td>
<td><p>целое</p></td>
<td><p>Порт для службы EDGE (A/V), используемой вызывающим абонентом.</p></td>
</tr>
<tr class="even">
<td><p>CalleeRelayIPAddr</p></td>
<td><p>var (50)</p></td>
<td><p>Ключ IP-адреса для службы EDGE (/V), используемой вызываемым абонентом. Дополнительные сведения приведены в <a href="lync-server-2013-ipaddress-table.md">таблице IP-адрес в Lync Server 2013</a> .</p></td>
</tr>
<tr class="odd">
<td><p>CalleeRelayPort</p></td>
<td><p>целое</p></td>
<td><p>Порт для службы EDGE (A/V), используемой вызываемым абонентом.</p></td>
</tr>
<tr class="even">
<td><p>CallerCaptureDev</p></td>
<td><p>varchar (256)</p></td>
<td><p>Имя устройства захвата вызывающего абонента.</p></td>
</tr>
<tr class="odd">
<td><p>CallerRenderDev</p></td>
<td><p>varchar (256)</p></td>
<td><p>Имя устройства отрисовки вызывающего абонента.</p></td>
</tr>
<tr class="even">
<td><p>CallerCaptureDevDriver</p></td>
<td><p>varchar (256)</p></td>
<td><p>Имя драйвера устройства захвата вызывающего абонента.</p></td>
</tr>
<tr class="odd">
<td><p>CallerRenderDevDriver</p></td>
<td><p>varchar (256)</p></td>
<td><p>Имя драйвера устройства отрисовки вызывающего абонента.</p></td>
</tr>
<tr class="even">
<td><p>CalleeCaptureDev</p></td>
<td><p>varchar (256)</p></td>
<td><p>Имя устройства захвата абонента.</p></td>
</tr>
<tr class="odd">
<td><p>CalleeRenderDev</p></td>
<td><p>varchar (256)</p></td>
<td><p>Имя устройства отрисовки вызываемого абонента.</p></td>
</tr>
<tr class="even">
<td><p>CalleCaptureDevDriver</p></td>
<td><p>varchar (256)</p></td>
<td><p>Имя драйвера устройства захвата абонента.</p></td>
</tr>
<tr class="odd">
<td><p>CalleeRenderDevDriver</p></td>
<td><p>varchar (256)</p></td>
<td><p>Имя драйвера устройства обработки вызываемого абонента.</p></td>
</tr>
<tr class="even">
<td><p>CallerNetworkConnectionType</p></td>
<td><p>tinyint</p></td>
<td><p>Тип сетевого подключения вызывающего абонента: 0 проводное соединение, 1 — Беспроводная связь.</p></td>
</tr>
<tr class="odd">
<td><p>CallerVPN</p></td>
<td><p>бит</p></td>
<td><p>Указывает, подключен ли вызывающий абонент к виртуальной частной сети. 1 — это виртуальная частная сеть (VPN), а 0 — не VPN.</p></td>
</tr>
<tr class="even">
<td><p>CallerLinkSpeed</p></td>
<td><p>десятичное число (18;)</p></td>
<td><p>Скорость сетевого соединения для конечной точки вызывающего абонента бит/с.</p></td>
</tr>
<tr class="odd">
<td><p>CalleeNetworkConnectionType</p></td>
<td><p>tinyint</p></td>
<td><p>Тип сетевого подключения абонента: 0 – проводное, 1 — Беспроводная связь.</p></td>
</tr>
<tr class="even">
<td><p>CalleeVPN</p></td>
<td><p>бит</p></td>
<td><p>Указывает, подсоединен ли вызывающий абонент к виртуальной частной сети. 1 — это виртуальная частная сеть (VPN), а 0 — не VPN.</p></td>
</tr>
<tr class="odd">
<td><p>CalleeLinkSpeed</p></td>
<td><p>десятичное число (18; 0)</p></td>
<td><p>Скорость сетевого соединения для конечной точки вызываемого абонента (бит/с).</p></td>
</tr>
<tr class="even">
<td><p>ConversationalMOS</p></td>
<td><p>десятичное число (3, 2)</p></td>
<td><p>Narrowband MOS из сеансов голосовой связи (на основе обоих звуковых потоков).</p></td>
</tr>
<tr class="odd">
<td><p>AppliedBandwidthLimit</p></td>
<td><p>целое</p></td>
<td><p>Реальная пропускная способность, примененная к потоку отправки данных в соответствии с различными параметрами политики (например, "повернуть", "API", SDP, сервер политики и т. д.). Это не следует путать с эффективной пропускной способностью, так как в зависимости от оценки пропускной способности может снизиться эффективная пропускная способность. Это является, по сути, максимальной пропускной способностью потока отправки, который может занимать ограничения пропускной способности.</p></td>
</tr>
<tr class="even">
<td><p>JitterInterArrival</p></td>
<td><p>целое</p></td>
<td><p>Средняя колебание сети из статистики протокола управления временем в реальном времени (RTCP).</p></td>
</tr>
<tr class="odd">
<td><p>JitterInterArrivalMax</p></td>
<td><p>целое</p></td>
<td><p>Максимальная колебание сети во время звонка.</p></td>
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
<td><p>PacketLossRate</p></td>
<td><p>десятичное число (5; 4)</p></td>
<td><p>Средняя скорость потерь пакетов во время звонка.</p></td>
</tr>
<tr class="odd">
<td><p>PacketLossRateMax</p></td>
<td><p>десятичное число (5; 4)</p></td>
<td><p>Максимальное количество потерь пакетов, замеченное во время звонка.</p></td>
</tr>
<tr class="even">
<td><p>PacketUtilization</p></td>
<td><p>целое</p></td>
<td><p>Число пакетов для видеопотока (транспортный протокол в реальном времени).</p></td>
</tr>
<tr class="odd">
<td><p>Самый пропускная способность</p></td>
<td><p>целое</p></td>
<td><p>Оценка пропускной способности для аудиопотока.</p></td>
</tr>
<tr class="even">
<td><p>PayloadDescription</p></td>
<td><p>целое</p></td>
<td><p>Аудиокодек, использованный для звонка, указан из <a href="lync-server-2013-payloaddescription-table.md">таблицы PayloadDescription в Lync Server 2013</a>.</p></td>
</tr>
<tr class="odd">
<td><p>VideoResolution</p></td>
<td><p>char (9)</p></td>
<td><p>Разрешение видео в пикселях, умноженное на высоту в пикселях. Отображается в виде строки.</p></td>
</tr>
<tr class="even">
<td><p>VideoBitRateAvg</p></td>
<td><p>целое</p></td>
<td><p>Средняя скорость потока видео.</p></td>
</tr>
<tr class="odd">
<td><p>InboundVideoFrameRateAvg</p></td>
<td><p>десятичное число (9; 4)</p></td>
<td><p>Частота кадров, полученных в видеоролике.</p></td>
</tr>
<tr class="even">
<td><p>OutboundVideoFrameRateAvg</p></td>
<td><p>десятичное число (9; 4)</p></td>
<td><p>Частота кадров, отправленных видео.</p></td>
</tr>
<tr class="odd">
<td><p>ViideoBitRateMax</p></td>
<td><p>целое</p></td>
<td><p>Максимальная скорость видеосигнала во время видеосеанса.</p></td>
</tr>
<tr class="even">
<td><p>VideoPacketLossRate</p></td>
<td><p>десятичное число (9; 4)</p></td>
<td><p>Частота потери видеопакетов.</p></td>
</tr>
<tr class="odd">
<td><p>VideoFrameLossRate</p></td>
<td><p>Decimal (9.4)</p></td>
<td><p>Процент от общего числа потерянных кадров видео.</p></td>
</tr>
<tr class="even">
<td><p>VideoFEC</p></td>
<td><p>бит</p></td>
<td><p>Не используется.</p></td>
</tr>
<tr class="odd">
<td><p>VideoAllocateBWAvg</p></td>
<td><p>целое</p></td>
<td><p>Средний объем пропускной способности, выделенной для видео.</p></td>
</tr>
<tr class="even">
<td><p>VideoLocalFrameLossPercentageAvg</p></td>
<td><p>Decimal (9.4)</p></td>
<td><p>Процент от общего количества кадров видео, которые были утрачены.</p></td>
</tr>
<tr class="odd">
<td><p>SenderIsCallerPAI</p></td>
<td><p>бит</p></td>
<td><p>Направление потока для идентификационной информации, утвержденной p. 1 — направление потока на вызываемый абонентом. 0 — направление потока из вызываемого объекта вызывающему абоненту.</p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

