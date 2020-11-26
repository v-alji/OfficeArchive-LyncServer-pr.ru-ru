---
title: 'Lync Server 2013: таблица использованием Traceroute'
description: 'Таблица Lync Server 2013: использованием Traceroute.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: TraceRoute table
ms:assetid: b9493cef-6ece-4f13-bf68-dbf132aab4f4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205205(v=OCS.15)
ms:contentKeyID: 48185242
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8af33e572065fbab1eaaaef684997e7f95edaed9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440838"
---
# <a name="traceroute-table-in-lync-server-2013"></a>Таблица использованием Traceroute в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2014-02-21_

В таблице использованием Traceroute содержатся сведения о маршрутизации из звонков. Эта таблица введена в Microsoft Lync Server 2013.


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
<td><p>Основной, внешний</p></td>
<td><p>Дата и время начала звонка.</p></td>
</tr>
<tr class="even">
<td><p><strong>SessionSeq</strong></p></td>
<td><p>целое</p></td>
<td><p>Основной, внешний</p></td>
<td><p>Уникальный идентификатор, который используется для различения нескольких звонков, которые могли приступили к одной и той же дате и в то же время.</p></td>
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
<td><p><strong>FromCaller</strong></p></td>
<td><p>бит</p></td>
<td><p>Primary</p></td>
<td><p>Конечная точка, в которой был помещен звонок.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Участк</strong></p></td>
<td><p>целое</p></td>
<td></td>
<td><p>Транзитный сетевой переход/</p></td>
</tr>
<tr class="even">
<td><p><strong>IPAddressKey</strong></p></td>
<td><p>целое</p></td>
<td><p>Другом</p></td>
<td><p>Уникальный идентификатор IP-адреса. Информация об IP-адресах хранится в <a href="lync-server-2013-ipaddress-table.md">таблице IPAddress в Lync Server 2013</a>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>ПЕРЕДАЧИ</strong></p></td>
<td><p>целое</p></td>
<td></td>
<td><p>Время обмена данными. Время для обмена данными измеряет время, затрачиваемое на передачу голосового пакета получателю, а затем отправляет уведомление о том, что оно получено.</p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

