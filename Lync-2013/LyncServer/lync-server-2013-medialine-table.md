---
title: 'Lync Server 2013: таблица MediaLine'
description: 'Таблица Lync Server 2013: MediaLine.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: MediaLine table
ms:assetid: 414b1d63-ae97-4c27-bac0-c9ad0f808ff0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425920(v=OCS.15)
ms:contentKeyID: 48183956
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2acea8e14ba0608d9ebf72a48f888bfc4501fae3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425621"
---
# <a name="medialine-table-in-lync-server-2013"></a>Таблица MediaLine в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2014-02-21_

Каждая запись представляет одну сеть мультимедиа. (Один звуковой сеанс обычно состоит из одной линии звукового файла. Один из звуковых и видеофайлов (A/V) обычно содержит одну строку звукового файла и одну строку видеофайла, хотя в этом сеансе может быть две видеоустройства, если используется устройство конференц-связи или режим галереи.


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
<td><p>Ссылка из <a href="lync-server-2013-session-table.md">таблицы Sessions в Lync Server 2013</a>.</p></td>
</tr>
<tr class="even">
<td><p><strong>SessionSeq</strong></p></td>
<td><p>целое</p></td>
<td><p>Primary</p></td>
<td><p>Ссылка из <a href="lync-server-2013-session-table.md">таблицы Sessions в Lync Server 2013</a>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>MediaLineLabel</strong></p></td>
<td><p>tinyint</p></td>
<td><p>Primary</p></td>
<td><p>0 — основной звук, 1 — основной видеофайл, а 2 — панорамный видеоролик, а 3 — общий доступ к приложениям и рабочему столу. Эта метка должна быть уникальной в пределах одного сеанса.</p></td>
</tr>
<tr class="even">
<td><p><strong>ConnectivityIce</strong></p></td>
<td><p>tinyint</p></td>
<td><p> </p></td>
<td><p>Этот столбец присутствует в Microsoft Lync Server 2013, но не используется. Сведения о подключении, используемом для линии мультимедиа, записываются в столбцах CallerConnectivityICE и CalleeConnectivityICE.</p></td>
</tr>
<tr class="odd">
<td><p><strong>CallerIceWarningFlags</strong></p></td>
<td><p>целое</p></td>
<td><p> </p></td>
<td><p>Сведения о процессе установки интерактивной связи (ICE), описанные в разделе Флаги BITS. Подробные сведения можно найти в <em>спецификации протоколов сервера контроля качества обслуживания</em>, которую можно загрузить.</p></td>
</tr>
<tr class="even">
<td><p><strong>CalleeIceWarningFlags</strong></p></td>
<td><p>целое</p></td>
<td><p> </p></td>
<td><p>То же, что и CallerIceWarningFlags, но на стороне вызываемого абонента. Подробные сведения можно найти в <em>спецификации протоколов сервера контроля качества обслуживания</em>, которую можно загрузить.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Безопасность</strong></p></td>
<td><p>tinyint</p></td>
<td><p> </p></td>
<td><p>Используемый профиль безопасности. 0 — NONE, 1 — SRTP, 2 — v1.</p></td>
</tr>
<tr class="even">
<td><p><strong>Transport</strong></p></td>
<td><p>tinyint</p></td>
<td><p> </p></td>
<td><p>0 — это UDP, а 1 — TCP.</p></td>
</tr>
<tr class="odd">
<td><p><strong>CallerIPAddr</strong></p></td>
<td><p>целое</p></td>
<td><p>Другом</p></td>
<td><p>IP-адрес вызывающего абонента. Дополнительные сведения приведены в <a href="lync-server-2013-ipaddress-table.md">таблице IP-адрес в Lync Server 2013</a> .</p></td>
</tr>
<tr class="even">
<td><p><strong>CallerPort</strong></p></td>
<td><p>целое</p></td>
<td><p> </p></td>
<td><p>Порт, используемый вызывающим абонентом.</p></td>
</tr>
<tr class="odd">
<td><p><strong>CallerSubnet</strong></p></td>
<td><p>целое</p></td>
<td><p> Другом</p></td>
<td><p>Подсеть вызывающего абонента. Дополнительные сведения приведены в <a href="lync-server-2013-ipaddress-table.md">таблице IP-адрес в Lync Server 2013</a> .</p></td>
</tr>
<tr class="even">
<td><p><strong>CallerInside</strong></p></td>
<td><p>бит</p></td>
<td><p> </p></td>
<td><p>1 означает, что вызывающий абонент входит в корпоративную сеть, а 0 означает, что вызывающий абонент находится за пределами сети.</p></td>
</tr>
<tr class="odd">
<td><p><strong>CallerMacAddress</strong></p></td>
<td><p>целое</p></td>
<td><p>Другом</p></td>
<td><p>Mac-адрес вызывающего абонента, на который ссылается <a href="lync-server-2013-macaddress-table.md">Таблица MacAddress в Lync Server 2013</a>.</p></td>
</tr>
<tr class="even">
<td><p><strong>CallerRelayIPAddr</strong></p></td>
<td><p>целое</p></td>
<td><p>Другом</p></td>
<td><p>IP-адрес службы Edge сервера Lync/V, используемой вызывающим абонентом. Дополнительные сведения приведены в <a href="lync-server-2013-ipaddress-table.md">таблице IP-адрес в Lync Server 2013</a> .</p></td>
</tr>
<tr class="odd">
<td><p><strong>CallerRelayPort</strong></p></td>
<td><p>целое</p></td>
<td><p> </p></td>
<td><p>Порт, используемый вызывающим абонентом для службы Edge A/V.</p></td>
</tr>
<tr class="even">
<td><p><strong>CallerCaptureDev</strong></p></td>
<td><p>целое</p></td>
<td><p>Другом</p></td>
<td><p>Устройство захвата, используемое вызывающим абонентом. Ссылка из <a href="lync-server-2013-device-table.md">таблицы устройств в Lync Server 2013</a>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>CallerRenderDev</strong></p></td>
<td><p>целое</p></td>
<td><p>Другом</p></td>
<td><p>Устройство обработки, используемое вызывающим абонентом. Ссылка из <a href="lync-server-2013-device-table.md">таблицы устройств в Lync Server 2013</a>.</p></td>
</tr>
<tr class="even">
<td><p><strong>CallerCaptureDevDriver</strong></p></td>
<td><p>целое</p></td>
<td><p>Другом</p></td>
<td><p>Драйвер устройства захвата вызывающего абонента, на который ссылается <a href="lync-server-2013-devicedriver-table.md">Таблица DeviceDriver в Lync Server 2013</a>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>CallerRenderDevDriver</strong></p></td>
<td><p>целое</p></td>
<td><p>Другом</p></td>
<td><p>Драйвер для устройства отрисовки вызывающего абонента, на который ссылается <a href="lync-server-2013-devicedriver-table.md">Таблица DeviceDriver в Lync Server 2013</a>.</p></td>
</tr>
<tr class="even">
<td><p><strong>CallerNetworkConnectionType</strong></p></td>
<td><p>tinyint</p></td>
<td><p>Другом</p></td>
<td><p>Показывает, как вызывающий абонент подключился к сети. Значения извлекаются из <a href="lync-server-2013-networkconnectiondetail-table.md">таблицы NetworkConnectionDetail в Lync Server 2013</a>. Типичные значения: 0 для проводного подключения 1 для подключения WiFi; и 3 для подключения Ethernet.</p></td>
</tr>
<tr class="odd">
<td><p><strong>CallerBssid</strong></p></td>
<td><p>целое</p></td>
<td><p>Другом</p></td>
<td><p>BSSID для вызывающего абонента, если используется беспроводная связь. Ссылка из <a href="lync-server-2013-macaddress-table.md">таблицы MacAddress в Lync Server 2013</a>.</p></td>
</tr>
<tr class="even">
<td><p><strong>CallerVPN</strong></p></td>
<td><p>бит</p></td>
<td></td>
<td><p>Ссылка вызывающего абонента. 1 — это виртуальная частная сеть (VPN), а 0 — не VPN.</p></td>
</tr>
<tr class="odd">
<td><p><strong>CallerLinkSpeed</strong></p></td>
<td><p>десятичное число (18; 0)</p></td>
<td></td>
<td><p>Скорость сетевого соединения (в бит/с) для конечной точки вызывающего объекта.</p></td>
</tr>
<tr class="even">
<td><p><strong>CalleeIPAddr</strong></p></td>
<td><p>целое</p></td>
<td><p>Другом</p></td>
<td><p>IP-адрес получателя звонка. Дополнительные сведения приведены в <a href="lync-server-2013-ipaddress-table.md">таблице IP-адрес в Lync Server 2013</a> .</p></td>
</tr>
<tr class="odd">
<td><p><strong>CalleePort</strong></p></td>
<td><p>бит</p></td>
<td></td>
<td><p>Порт, используемый получателем звонка.</p></td>
</tr>
<tr class="even">
<td><p><strong>CalleeSubnet</strong></p></td>
<td><p>целое</p></td>
<td><p>Другом</p></td>
<td><p>Подсеть вызываемого абонента. Дополнительные сведения приведены в <a href="lync-server-2013-ipaddress-table.md">таблице IP-адрес в Lync Server 2013</a> .</p></td>
</tr>
<tr class="odd">
<td><p><strong>CalleeInside</strong></p></td>
<td><p>бит</p></td>
<td><p> </p></td>
<td><p>1 — Получатель звонка входит в корпоративную сеть, а 0 означает, что получатель звонка находится за пределами сети.</p></td>
</tr>
<tr class="even">
<td><p><strong>CalleeMacAddress</strong></p></td>
<td><p>целое</p></td>
<td><p>Другом</p></td>
<td><p>Абонентский Mac-адрес. Ссылка на <a href="lync-server-2013-macaddress-table.md">таблицу MacAddress в Lync Server 2013</a>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>CalleeRelayIPAddr</strong></p></td>
<td><p>целое</p></td>
<td><p>Другом</p></td>
<td><p>IP-адрес службы EDGE (/V), используемой приемником вызова. Дополнительные сведения приведены в <a href="lync-server-2013-ipaddress-table.md">таблице IP-адрес в Lync Server 2013</a> .</p></td>
</tr>
<tr class="even">
<td><p><strong>CalleeRelayPort</strong></p></td>
<td><p>целое</p></td>
<td><p> </p></td>
<td><p>Порт, используемый приемником вызова для службы Edge/V.</p></td>
</tr>
<tr class="odd">
<td><p><strong>CalleeCaptureDev</strong></p></td>
<td><p>целое</p></td>
<td><p>другом</p></td>
<td><p>Устройство захвата, используемое получателем звонка. Ссылка из <a href="lync-server-2013-device-table.md">таблицы устройств в Lync Server 2013</a>.</p></td>
</tr>
<tr class="even">
<td><p><strong>CalleeRenderDev</strong></p></td>
<td><p>целое</p></td>
<td><p>Другом</p></td>
<td><p>Устройство обработки, используемое получателем звонка. Ссылка из <a href="lync-server-2013-device-table.md">таблицы устройств в Lync Server 2013</a>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>CalleeCaptureDevDriver</strong></p></td>
<td><p>целое</p></td>
<td><p>Другом</p></td>
<td><p>Драйвер устройства захвата приемника звонков. Ссылка из <a href="lync-server-2013-devicedriver-table.md">таблицы DeviceDriver в Lync Server 2013</a>.</p></td>
</tr>
<tr class="even">
<td><p><strong>CalleeRenderDevDriver</strong></p></td>
<td><p>varchar (256)</p></td>
<td><p>Другом</p></td>
<td><p>Драйвер устройства отрисовки приемника звонков. Ссылка из <a href="lync-server-2013-devicedriver-table.md">таблицы DeviceDriver в Lync Server 2013</a>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>CalleeNetworkConnectionType</strong></p></td>
<td><p>tinyint</p></td>
<td><p>Другом</p></td>
<td><p>Показывает, как вызывающий абонент подключился к сети. Значения извлекаются из <a href="lync-server-2013-networkconnectiondetail-table.md">таблицы NetworkConnectionDetail в Lync Server 2013</a>. Типичные значения: 0 для проводного подключения 1 для подключения WiFi; и 3 для подключения Ethernet.</p></td>
</tr>
<tr class="even">
<td><p><strong>CalleeBssid</strong></p></td>
<td><p>целое</p></td>
<td><p>Другом</p></td>
<td><p>Если используется беспроводная связь, вызовите BSSID. Ссылка из <a href="lync-server-2013-macaddress-table.md">таблицы MacAddress в Lync Server 2013</a>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>CalleeVPN</strong></p></td>
<td><p>бит</p></td>
<td><p> </p></td>
<td><p>Ссылка на приемник звонка; 1 — это виртуальная частная сеть (VPN), а 0 — не VPN.</p></td>
</tr>
<tr class="even">
<td><p><strong>CalleeLinkSpeed</strong></p></td>
<td><p>десятичное число (18; 0)</p></td>
<td><p> </p></td>
<td><p>Скорость сетевого соединения (в бит/с) для конечной точки получателя звонка.</p></td>
</tr>
<tr class="odd">
<td><p><strong>ConversationalMOS</strong></p></td>
<td><p>десятичное число (3, 2)</p></td>
<td><p> </p></td>
<td><p>Narrowband MOS из сеансов голосовой связи (на основе обоих звуковых потоков).</p></td>
</tr>
<tr class="even">
<td><p><strong>AppliedBandwidthLimit</strong></p></td>
<td><p>целое</p></td>
<td></td>
<td><p>Это фактическая пропускная способность, примененная к данному потоку отправки на стороне, для которой заданы различные параметры политики (повернуть, API, SDP, сервер политики и т. д.). Это не следует путать с эффективной пропускной способностью, так как в зависимости от оценки пропускной способности может снизиться эффективная пропускная способность. Это является, по сути, максимальной пропускной способностью потока отправки, который может занимать ограничения пропускной способности.</p></td>
</tr>
<tr class="odd">
<td><p><strong>AppliedBandwidthSourceKey</strong></p></td>
<td><p>smallint</p></td>
<td></td>
<td><p>Это источник установленного места для пропускной способности. Она описывает, откуда поступают ограничения пропускной способности ("сервер политики", "превратить сервер", "модальность" и т. д.). На которую ссылается <a href="lync-server-2013-appliedbandwidthsource-table.md">Таблица AppliedBandwidthSource в Lync Server 2013</a>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Вызывающая сторона</strong></p></td>
<td><p>бит</p></td>
<td><p> </p></td>
<td><p>Указывает, получены ли метрики от вызывающего абонента; 1 — это "Да", значение null — "нет".</p></td>
</tr>
<tr class="odd">
<td><p><strong>Вызываемая сторона</strong></p></td>
<td><p>бит</p></td>
<td><p> </p></td>
<td><p>Указывает, получены ли метрики от приемника вызова; 1 — это "Да", значение null — "нет".</p></td>
</tr>
<tr class="even">
<td><p><strong>MidCallReport</strong></p></td>
<td><p>бит</p></td>
<td></td>
<td><p>Указывает, является ли отчет частью сеанса или для полного сеанса.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="odd">
<td><p><strong>ClassifiedPoorCall</strong></p></td>
<td><p>бит</p></td>
<td></td>
<td><p>Указывает, был ли звонок классифицирован как неудовлетворительный (значение 1) или как хороший звонок (0).</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="even">
<td><p><strong>CallerConnectivityICE</strong></p></td>
<td><p>tinyInt</p></td>
<td></td>
<td><p>Указывает, подключен ли вызывающий абонент к сети с помощью протокола ICE (установление подключения к Интернету).</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="odd">
<td><p><strong>CalleeConnectivityICE</strong></p></td>
<td><p>tinyint</p></td>
<td></td>
<td><p>Указывает, подключен ли вызывающий абонент к сети с помощью протокола ICE (установление подключения к Интернету).</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="even">
<td><p><strong>CallerReflexiveLocalIPAddr</strong></p></td>
<td><p>целое</p></td>
<td><p>Другом</p></td>
<td><p>IP-адрес пользователя, который поместил звонок. В организациях, использующих NAT (преобразование сетевых адресов), можно использовать IP-адрес прокси-сервера.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="odd">
<td><p><strong>CallerWiFiDriverDevicesDesc</strong></p></td>
<td><p>целое</p></td>
<td><p>Другом</p></td>
<td><p>Описание устройства для драйвера Wi-Fi, задействованного пользовательским абонентом.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="even">
<td><p><strong>CallerWiFiDriverVersion</strong></p></td>
<td><p>целое</p></td>
<td><p>Другом</p></td>
<td><p>Номер версии для драйвера Wi-Fi, используемый пользователем, который присоединил звонок.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="odd">
<td><p><strong>CalleReflexiveLocalIPAddr</strong></p></td>
<td><p>целое</p></td>
<td><p>Другом</p></td>
<td><p>IP-адрес пользователя, который получил звонок. В организациях, использующих NAT (преобразование сетевых адресов), можно использовать IP-адрес прокси-сервера.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="even">
<td><p><strong>CalleeWiFiDriverDevicesDesc</strong></p></td>
<td><p>целое</p></td>
<td><p>Другом</p></td>
<td><p>Описание устройства для драйвера Wi-Fi, применяемого пользователем, который получил звонок.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
<tr class="odd">
<td><p><strong>CalleeWiFiDriverVersion</strong></p></td>
<td><p>целое</p></td>
<td><p>Другом</p></td>
<td><p>Номер версии для драйвера Wi-Fi, используемый пользователем, который получил звонок.</p>
<p>Этот столбец появился в Microsoft Lync Server 2013.</p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

