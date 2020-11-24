---
title: 'Lync Server 2013: таблица UriTypes'
description: 'Таблица Lync Server 2013: UriTypes.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: UriTypes table
ms:assetid: 77c4dfae-1b29-4e81-ba05-609e61643998
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398587(v=OCS.15)
ms:contentKeyID: 48184553
ms.date: 06/16/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 97a63173b7ada258e7da22591b28a6a0410e666a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399445"
---
# <a name="uritypes-table-in-lync-server-2013"></a>Таблица UriTypes в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2015-06-16_

В таблице UriTypes содержатся различные типы URI (универсального идентификатора ресурса), отслеживаемые в Microsoft Lync Server 2013.


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Столбец</th>
<th>Тип данных</th>
<th>Ключ/индекс</th>
<th>Сведения</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>UriTypeId</strong></p></td>
<td><p>tinyint</p></td>
<td><p>Primary</p></td>
<td><p>Уникальный идентификатор, присвоенный типу URI.</p></td>
</tr>
<tr class="even">
<td><p><strong>UriType</strong></p></td>
<td><p>nvarchar(256)</p></td>
<td></td>
<td><p>Описание различных типов URI. Допустимые значения:</p>
<ul>
<li><p>1 – универсальный код ресурса (URI)</p></li>
<li><p>0 — URI пользователя</p></li>
</ul></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

