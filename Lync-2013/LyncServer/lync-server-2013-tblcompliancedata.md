---
title: 'Lync Server 2013: tblComplianceData'
description: 'Lync Server 2013: tblComplianceData.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblComplianceData
ms:assetid: 05b28f9b-4aba-4b69-ba8d-2ceeb6cbfaac
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558606(v=OCS.15)
ms:contentKeyID: 48183308
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3c597d67054303de2753182b37419f68051d3af8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444478"
---
# <a name="tblcompliancedata-in-lync-server-2013"></a>tblComplianceData в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-09-12_

tblComplianceData содержит события соответствия требованиям, которые пока не обрабатывались адаптером соответствия требованиям.

### <a name="columns"></a>Столбцов

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Столбец</th>
<th>Тип</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>cmplEventID</p></td>
<td><p>bigint, NOT NULL</p></td>
<td><p>Код события.</p></td>
</tr>
<tr class="even">
<td><p>entryDate</p></td>
<td><p>smalldatetime, NOT NULL</p></td>
<td><p>Время вставки (может быть в будущем для cmplType = 9, так как в этом случае запись является заполнителем в этом случае).</p></td>
</tr>
<tr class="odd">
<td><p>cmplType</p></td>
<td><p>int, NOT NULL</p></td>
<td><p>Тип события соответствия:</p>
<ul>
<li><p>1: чат</p></li>
<li><p>2: чат</p></li>
<li><p>3: Загрузка файла</p></li>
<li><p>4: Отправка файлов</p></li>
<li><p>9: подготовка к передаче файлов</p></li>
<li><p>10: удаление чата (с заменой)</p></li>
<li><p>11: Очистка чата</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>cmplTime</p></td>
<td><p>bigint, NOT NULL</p></td>
<td><p>Метка времени для события.</p></td>
</tr>
<tr class="odd">
<td><p>cmplChannelUri</p></td>
<td><p>nvarchar (255), NOT NULL</p></td>
<td><p>Универсальный код ресурса (URI) канала.</p></td>
</tr>
<tr class="even">
<td><p>cmplChatID</p></td>
<td><p>bigint</p></td>
<td><p>ИДЕНТИФИКАТОР чата (соответствующая таблице tblChat. chatId).</p></td>
</tr>
<tr class="odd">
<td><p>cmplUserID</p></td>
<td><p>int, NOT NULL</p></td>
<td><p>Идентификатор участника афиши (соответствующий таблице tblPrincipal. prinID).</p></td>
</tr>
<tr class="even">
<td><p>cmplUserUri</p></td>
<td><p>nvarchar (255), NOT NULL</p></td>
<td><p>URI пользователя.</p></td>
</tr>
<tr class="odd">
<td><p>cmplMessage</p></td>
<td><p>nvarchar (max)</p></td>
<td><p>Сообщение (Кодировка зависит от cmplType).</p></td>
</tr>
</tbody>
</table>


### <a name="key"></a>Ключ

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Столбец</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>cmplEventID</p></td>
<td><p>Первичный ключ.</p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

