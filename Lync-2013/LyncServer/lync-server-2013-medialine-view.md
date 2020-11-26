---
title: 'Lync Server 2013: представление MediaLine'
description: 'Lync Server 2013: MediaLine View.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: MediaLine view
ms:assetid: 132eca13-8913-4218-9eff-4960ced8c3dc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687972(v=OCS.15)
ms:contentKeyID: 49733560
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4c61fcc15b46958622e6cddd66427255a6def154
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445948"
---
# <a name="medialine-view-in-lync-server-2013"></a>MediaLine представления в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-10-03_

В представлении MediaLine хранятся сведения о каждой строке мультимедиа в базе данных. Один звуковой сеанс обычно состоит из одной линии звукового файла. Один из звуковых и видеофайлов (A/V) обычно состоит из одной линии звукового файла и одной линии видеоклипа; Тем не менее, в этом сеансе могут содержаться две строки видеофайла, если используется устройство конференц-связи или если используется представление коллекции. Это представление было представлено в Microsoft Lync Server 2013.


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
<th>сведения</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>ConferenceDateTime</p></td>
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
<td><p>Безопасность</p></td>
<td><p>tinyint</p></td>
<td><p>Профиль безопасности используется. 0 — NONE, 1 — SRTP, 2 — v1.</p></td>
</tr>
<tr class="odd">
<td><p>Transport</p></td>
<td><p>tinyint</p></td>
<td><p>Тип транспорта. 0 — это UDP, а 1 — TCP.</p></td>
</tr>
<tr class="even">
<td><p>CallerIPAddr</p></td>
<td><p>var (50)</p></td>
<td><p>IP-адрес вызывающего абонента. Это может быть либо адрес IPv4, либо IPv6.</p></td>
</tr>
<tr class="odd">
<td><p>CallerPort</p></td>
<td><p>целое</p></td>
<td><p>Порт, используемый вызывающим абонентом.</p></td>
</tr>
<tr class="even">
<td><p>CallerInside</p></td>
<td><p>бит</p></td>
<td><p>Указывает, находится ли вызывающий абонент в сети Организации. 1 означает, что вызывающий абонент входит в корпоративную сеть. 0 означает, что вызывающий абонент находится за пределами сети.</p></td>
</tr>
<tr class="odd">
<td><p>CallerMacAddress</p></td>
<td><p>varchar (256)</p></td>
<td><p>MAC-адрес сетевого интерфейса, используемого вызывающим абонентом.</p></td>
</tr>
<tr class="even">
<td><p>CallerRelayIPAddr</p></td>
<td><p>var (50)</p></td>
<td><p>IP-адрес службы EDGE (/V), используемой вызывающим абонентом. Дополнительные сведения приведены в <a href="lync-server-2013-ipaddress-table.md">таблице IP-адрес в Lync Server 2013</a> .</p></td>
</tr>
<tr class="odd">
<td><p>CalleeRelayPort</p></td>
<td><p>целое</p></td>
<td><p>Порт, используемый в службе EDGE (A/V), используемой вызывающим абонентом.</p></td>
</tr>
<tr class="even">
<td><p>CallerReflexiveIPAddr</p></td>
<td><p>var (50)</p></td>
<td><p>IP-адрес вызывающего абонента, предоставленный службой EDGE (A/V). Этот адрес может отличаться от CallerIPAddr, если клиент находится за пределами NAT, например.</p></td>
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
<td><p>CallerRenderDevDriver</p></td>
<td><p>varchar (256)</p></td>
<td><p>Имя драйвера устройства отрисовки вызывающего абонента.</p></td>
</tr>
<tr class="odd">
<td><p>CallerWifiDriverDeviceDesc</p></td>
<td><p>varchar (256</p></td>
<td><p>Описание драйвера Wi-Fi вызывающего абонента.</p></td>
</tr>
<tr class="even">
<td><p>CallerWifiDriverVersion</p></td>
<td><p>varchar (256)</p></td>
<td><p>Версия драйвера Wi-Fi вызывающего абонента.</p></td>
</tr>
<tr class="odd">
<td><p>CalleeNetworkConnectionDetail</p></td>
<td><p>varchar (256)</p></td>
<td><p>Сведения о сетевом подключении вызывающего абонента. Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-networkconnectiondetail-table.md">таблицей NetworkConnectionDetail в Lync Server 2013</a> .</p></td>
</tr>
<tr class="even">
<td><p>CallerBssid</p></td>
<td><p>varchar (256)</p></td>
<td><p>Основной идентификатор набора служб, используемый вызывающими абонентами WiFi-связи.</p></td>
</tr>
<tr class="odd">
<td><p>CallerVPN</p></td>
<td><p>бит</p></td>
<td><p>Указывает, подключен ли вызывающий абонент к виртуальной частной сети. 1 — это виртуальная частная сеть (VPN), а 0 — не VPN.</p></td>
</tr>
<tr class="even">
<td><p>CalleeIPAddr</p></td>
<td><p>var (50)</p></td>
<td><p>IP-адрес вызываемого абонента. Это может быть либо адрес IPv4, либо IPv6.</p></td>
</tr>
<tr class="odd">
<td><p>CalleePort</p></td>
<td><p>целое</p></td>
<td><p>Порт, используемый вызываемым абонентом.</p></td>
</tr>
<tr class="even">
<td><p>CalleeInside</p></td>
<td><p>бит</p></td>
<td><p>Указывает, входит ли вызывающий объект в корпоративную сеть. 1 означает, что вызываемый абонент входит в корпоративную сеть, а 0 означает, что вызываемый объект находится за пределами сети.</p></td>
</tr>
<tr class="odd">
<td><p>CalleeMacAddress</p></td>
<td><p>varchar (256)</p></td>
<td><p>MAC-адрес сетевого интерфейса, используемого вызываемым абонентом.</p></td>
</tr>
<tr class="even">
<td><p>CalleeRelayIPAddr</p></td>
<td><p>var (50)</p></td>
<td><p>IP-адрес службы EDGE (/V), используемой вызываемым абонентом. Дополнительные сведения приведены в <a href="lync-server-2013-ipaddress-table.md">таблице IP-адрес в Lync Server 2013</a> .</p></td>
</tr>
<tr class="odd">
<td><p>CalleeRelayPort</p></td>
<td><p>целое</p></td>
<td><p>Порт, используемый в службе EDGE (A/V), используемой вызываемым абонентом.</p></td>
</tr>
<tr class="even">
<td><p>CalleeReflexiveIPAddr</p></td>
<td><p>var (50)</p></td>
<td><p>IP-адрес вызываемого абонента, предоставленный службой Edge/V. Этот адрес может отличаться от CalleeIPAddr, если клиент находится за пределами NAT, например.</p></td>
</tr>
<tr class="odd">
<td><p>CalleeCaptureDev</p></td>
<td><p>var (50)</p></td>
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
<td><p>CalleeWifiDriverDeviceDesc</p></td>
<td><p>varchar (256)</p></td>
<td><p>Описание драйвера WiFi вызываемого абонента.</p></td>
</tr>
<tr class="even">
<td><p>CalleeWifiDriverVersion</p></td>
<td><p>varchar (256</p></td>
<td><p>Версия драйвера Wi-Fi для вызываемого абонента.</p></td>
</tr>
<tr class="odd">
<td><p>CalleeNetworkConnectionDetail</p></td>
<td><p>varchar (256)</p></td>
<td><p>Сведения о сетевом подключении для вызываемого абонента. Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-networkconnectiondetail-table.md">таблицей NetworkConnectionDetail в Lync Server 2013</a> .</p></td>
</tr>
<tr class="even">
<td><p>CalleeBssid</p></td>
<td><p>varchar (256)</p></td>
<td><p>Основной идентификатор набора служб, используемый для подключений WiFi.</p></td>
</tr>
<tr class="odd">
<td><p>CalleeVPN</p></td>
<td><p>бит</p></td>
<td><p>Указывает, подсоединен ли вызывающий объект к виртуальной частной сети. 1 — это виртуальная частная сеть (VPN), а 0 — не VPN.</p></td>
</tr>
<tr class="even">
<td><p>ConversationalMOS</p></td>
<td><p>десятичное число (3, 2)</p></td>
<td><p>Narrowband MOS из сеансов голосовой связи (на основе обоих звуковых потоков).</p></td>
</tr>
<tr class="odd">
<td><p>AppliedBandwidthLimit</p></td>
<td><p>целое</p></td>
<td><p>Это фактическая пропускная способность, примененная к потоку отправки на стороне, для которой заданы различные параметры политики (TURN, API, SDP, сервер политики и т. д.). Это не следует путать с эффективной пропускной способностью, так как в зависимости от оценки пропускной способности может снизиться эффективная пропускная способность. Это является, по сути, максимальной пропускной способностью потока отправки, который может занимать ограничения пропускной способности.</p></td>
</tr>
<tr class="even">
<td><p>AppliedBandwidthSource</p></td>
<td><p>varchar (256)</p></td>
<td><p>Источник ограничения пропускной способности. Она описывает, откуда поступают ограничения пропускной способности (например, "сервер политики", "превратить сервер" или "модальность").</p></td>
</tr>
<tr class="odd">
<td><p>Вызывающая сторона</p></td>
<td><p>бит</p></td>
<td><p>Указывает, получены ли метрики от вызывающего абонента; 1 — Да, 0 — нет.</p></td>
</tr>
<tr class="even">
<td><p>Вызываемая сторона</p></td>
<td><p>бит</p></td>
<td><p>Указывает, получены ли метрики от приемника вызова; 1 — Да, 0 — нет.</p></td>
</tr>
<tr class="odd">
<td><p>MidCallReport</p></td>
<td><p>бит</p></td>
<td><p>Указывает, является ли отчет частью звонка или полным звонком.</p></td>
</tr>
<tr class="even">
<td><p>ClassifiedPoorCall</p></td>
<td><p>бит</p></td>
<td><p>Указывает, был ли звонок классифицирован как некачественный звонок (1) или как хороший звонок (0).</p></td>
</tr>
<tr class="odd">
<td><p>CallerConnectivityICE</p></td>
<td><p>tinyint</p></td>
<td><p>Указывает, подключен ли вызывающий абонент к сети с помощью протокола ICE (установление подключения к Интернету).</p></td>
</tr>
<tr class="even">
<td><p>CalleeConnectivityICE</p></td>
<td><p>tinyint</p></td>
<td><p>Указывает, вызывает ли пользователь подключение к сети с помощью протокола ICE (установление подключения к Интернету).</p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

