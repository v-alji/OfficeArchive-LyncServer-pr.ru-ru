---
title: 'Lync Server 2013: tblEnumValue'
description: 'Lync Server 2013: tblEnumValue.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblEnumValue
ms:assetid: a33df20c-d19d-4f5c-b012-29dab8fb9200
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615025(v=OCS.15)
ms:contentKeyID: 48185040
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 159f90bb96c367fcb3e11725a582a9993080d3fd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444450"
---
# <a name="tblenumvalue-in-lync-server-2013"></a>tblEnumValue в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-06-28_

tblEnumValue — это жесткая таблица, содержащая значения видимости и поведения атрибутов, используемых в таблице node.

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
<td><p>valueID</p></td>
<td><p>smallint, NOT NULL</p></td>
<td><p>Идентификатор значения.</p></td>
</tr>
<tr class="even">
<td><p>attributeID</p></td>
<td><p>smallint, NOT NULL</p></td>
<td><p>Идентификатор атрибута.</p></td>
</tr>
<tr class="odd">
<td><p>attributeValue</p></td>
<td><p>nvarchar (256), NOT NULL</p></td>
<td><p>Имя значения.</p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a>Параметры

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
<td><p>valueID</p></td>
<td><p>Первичный ключ.</p></td>
</tr>
<tr class="even">
<td><p>attributeID</p></td>
<td><p>Внешний ключ с подстановкой в таблице tblEnumAttribute. attributeID.</p></td>
</tr>
</tbody>
</table>


### <a name="table-values"></a>Значения таблицы

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>valueID</th>
<th>attributeID</th>
<th>attributeValue</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>2</p></td>
<td><p>1</p></td>
<td><p>закрытые</p></td>
</tr>
<tr class="even">
<td><p>3</p></td>
<td><p>1</p></td>
<td><p>област</p></td>
</tr>
<tr class="odd">
<td><p>4</p></td>
<td><p>2</p></td>
<td><p>нормальный</p></td>
</tr>
<tr class="even">
<td><p>5</p></td>
<td><p>2</p></td>
<td><p>auditorium</p></td>
</tr>
<tr class="odd">
<td><p>6</p></td>
<td><p>1</p></td>
<td><p>запуска</p></td>
</tr>
</tbody>
</table>


<div>

## <a name="see-also"></a>См. также


[tblNode в Lync Server 2013](lync-server-2013-tblnode.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

