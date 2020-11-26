---
title: 'Lync Server 2013: размещение данных и файла журнала SQL Server'
description: 'Lync Server 2013: расположение данных и файлов журнала SQL Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: SQL Server data and log file placement
ms:assetid: 67aa525b-8aa3-474f-827e-8e1d4697f30f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398479(v=OCS.15)
ms:contentKeyID: 48184395
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a127254fec41a734136df9b63fc6cc8929745df7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444597"
---
# <a name="sql-server-data-and-log-file-placement-for-lync-server-2013"></a>Размещение данных и файла журнала SQL Server для Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2013-02-21_

При планировании и развертывании Microsoft SQL Server 2012 или Microsoft SQL Server 2008 R2 SP1 для пула Lync Server 2013, важно помнить, что при работе с данными и файлами журнала на физических жестких дисках будет размещаться файл данных и журнал. Рекомендуемая конфигурация диска — это реализация 1 + 0 RAID-массива с использованием шести дисков. Если вы размещаете все файлы баз данных и журналов, которые используются интерфейсным пулом и связанными ролями и службами сервера (то есть сервер архивации и мониторинга, служба группы ответа на Lync Server, служба обслуживания звонков в Lync Server), на диск RAID с помощью мастера развертывания Lync Server вы сможете настроить конфигурацию, которая была протестирована на хорошую производительность. Файлы базы данных и их ответственные описаны в таблице ниже.

<div>


> [!NOTE]  
> Если ваши политики и конфигурации SQL Server требуют более специализированной установки, файлы базы данных и журнала можно установить в любое предопределенное расположение с помощью командной консоли Lync Server Management Shell. Дополнительные сведения о том, как <A href="lync-server-2013-database-installation-using-lync-server-management-shell.md">установить базу данных с помощью командной консоли Lync Server Management Shell, вы увидите в Lync server 2013</A> .



</div>

### <a name="data-and-log-files-for-central-management-store"></a>Файлы данных и журналов для централизованного управления хранилищем

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Файлы баз данных централизованного управления хранилищем</th>
<th>Файл данных или назначение журнала</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>XDS. ldf</p></td>
<td><p>Файл журнала транзакций для хранилища центрального управления</p></td>
</tr>
<tr class="even">
<td><p>XDS. mdf</p></td>
<td><p>Сохраняет конфигурацию текущей топологии Lync Server 2013, определенную и опубликованную с помощью построителя топологии.</p></td>
</tr>
<tr class="odd">
<td><p>LIS. mdf</p></td>
<td><p>Файл данных службы сведений о расположении</p></td>
</tr>
<tr class="even">
<td><p>LIS. ldf</p></td>
<td><p>Журнал транзакций для файла данных службы сведений о расположении</p></td>
</tr>
</tbody>
</table>


### <a name="data-and-log-files-for-user-conferencing-and-address-book"></a>Файлы данных и журналов для пользователей, конференций и адресной книги

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Файлы базы данных основного Lync Server 2013</th>
<th>Файл данных или назначение журнала</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>RTC. mdf</p></td>
<td><p>Постоянные данные пользователя (например, списки управления доступом (ACL), контакты, запланированные конференции)</p></td>
</tr>
<tr class="even">
<td><p>RTC. ldf</p></td>
<td><p>Журнал транзакций для данных RTC</p></td>
</tr>
<tr class="odd">
<td><p>RTCDyn. mdf</p></td>
<td><p>Поддерживает временные пользовательские данные (данные среды выполнения присутствия)</p></td>
</tr>
<tr class="even">
<td><p>RTCDyn. ldf</p></td>
<td><p>Журнал транзакций для данных RTCDyn</p></td>
</tr>
<tr class="odd">
<td><p>Rtcab. mdf</p></td>
<td><p>База данных адресной книги в реальном времени (RTC) — это репозиторий SQL Server, в котором хранятся сведения о службе адресной книги</p></td>
</tr>
<tr class="even">
<td><p>Rtcab. ldf</p></td>
<td><p>Журнал транзакций для службы «адресная книга»</p></td>
</tr>
<tr class="odd">
<td><p>Rtclocal. mdb</p></td>
<td><p>Размещение каталога конференций</p></td>
</tr>
<tr class="even">
<td><p>Rtcxds. mdf</p></td>
<td><p>Сохранение резервной копии данных пользователя</p></td>
</tr>
<tr class="odd">
<td><p>Rtcxds. ldf</p></td>
<td><p>Журнал транзакций для данных Rtcxds</p></td>
</tr>
</tbody>
</table>


### <a name="data-and-log-files-for-call-park-and-response-group"></a>Файлы данных и журналов для парковки звонков и группы ответа

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>данных приложения</th>
<th>Файл данных или назначение журнала</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Cpsdyn. mdf</p></td>
<td><p>Динамическая информационная база данных для приложения парковки звонков</p></td>
</tr>
<tr class="even">
<td><p>Cpsdyn. ldf</p></td>
<td><p>Журнал транзакций для файла данных приложения с приостановкой звонков</p></td>
</tr>
<tr class="odd">
<td><p>Rgsconfig. mdf</p></td>
<td><p>Файл данных службы группы ответа Lync Server для настройки служб</p></td>
</tr>
<tr class="even">
<td><p>Rgsconfig. ldf</p></td>
<td><p>Файл журнала транзакций для конфигурации приложения группы ответа</p></td>
</tr>
<tr class="odd">
<td><p>Rgsdyn. mdf</p></td>
<td><p>Файл данных службы группы ответа для операций среды выполнения</p></td>
</tr>
<tr class="even">
<td><p>Rgsdyn. ldf</p></td>
<td><p>Журнал транзакций для файла данных среды выполнения службы группы ответа</p></td>
</tr>
</tbody>
</table>


### <a name="data-and-log-files-for-archiving-and-monitoring-server"></a>Файлы данных и журналов для архивации и мониторинга сервера

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Архивирование и мониторинг файлов базы данных</th>
<th>Файл данных или назначение журнала</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>LcsCdr. mdf</p></td>
<td><p>Хранилище данных для процесса записи сведений о звонке (CDR) на сервере мониторинга</p></td>
</tr>
<tr class="even">
<td><p>LcsCdr. ldf</p></td>
<td><p>Журнал транзакций для данных записи сведений о звонке (CDR)</p></td>
</tr>
<tr class="odd">
<td><p>QoEMetrics. mdf</p></td>
<td><p>Файл данных качества взаимодействия, хранящийся на сервере мониторинга</p></td>
</tr>
<tr class="even">
<td><p>QoEMetrics. ldf</p></td>
<td><p>Журнал транзакций для наблюдения за данными</p></td>
</tr>
<tr class="odd">
<td><p>Lcslog. mdf</p></td>
<td><p>Файл данных для хранения данных о мгновенных сообщениях и конференц-связи на сервере архивации</p></td>
</tr>
<tr class="even">
<td><p>Lcslog. ldf</p></td>
<td><p>Журнал транзакций для архивации данных</p></td>
</tr>
</tbody>
</table>


В этом разделе приведены ссылки на диск и на наборы RAID. Обратите внимание, что в конфигурации ресурсов SQL Server обращение к диску означает, что это одно аппаратное устройство. Жесткий диск с двумя разделами, один из которых хранит файлы журнала и другой раздел, содержащий файлы данных, отличается от двух дисков, каждый из которых предназначен для файлов журнала или данных.

В ссылках на массивы RAID существуют различные технологии RAID различных производителей. И с ростом числа сетей хранения данных (SAN) наборы RAID, выделенные для одной системы, rarer. Вы должны обратиться к поставщику RAID или сети хранения данных, чтобы определить оптимальную конфигурацию для вашего макета диска при настройке производительности SQL Server с помощью Lync Server 2013.

Кроме того, обратите внимание на то, что не все диски создаются одинаково. Некоторые действия выполняются лучше, чем другие. Даже диски одного и того же производителя могут варьироваться в зависимости от скорости вращения, размера кэша оборудования и других факторов.

</div>

<span> </span>

</div>

</div>

</div>

