---
title: 'Lync Server 2013: таблица ErrorDef'
description: 'Таблица Lync Server 2013: ErrorDef.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ErrorDef table
ms:assetid: 6acf3b86-da61-4923-9812-300db6f66dec
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398503(v=OCS.15)
ms:contentKeyID: 48184403
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e58980a671b54007012bbbf6780e24c162aebe00
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428540"
---
# <a name="errordef-table-in-lync-server-2013"></a>Таблица ErrorDef в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-05-25_

В таблице ErrorDef хранятся сведения о каждом типе ошибки, которые могут возникать. Каждая запись имеет один тип ошибки.


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
<td><p><strong>ErrorId</strong></p></td>
<td><p>целое</p></td>
<td><p>Primary</p></td>
<td><p>Уникальный ИДЕНТИФИКАЦИОНный номер, показывающий этот тип ошибки.</p></td>
</tr>
<tr class="even">
<td><p><strong>ResponseCode</strong></p></td>
<td><p>целое</p></td>
<td><p> </p></td>
<td><p>Стандартный код ответа SIP, связанный с этой ошибкой.</p></td>
</tr>
<tr class="odd">
<td><p><strong>MsDiagId</strong></p></td>
<td><p>целое</p></td>
<td><p> </p></td>
<td><p>Идентификатор диагностики (Майкрософт).</p></td>
</tr>
<tr class="even">
<td><p><strong>CallTypeId</strong></p></td>
<td><p>Типом</p></td>
<td><p>Другом</p></td>
<td><p>Тип звонка. Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-calltype-table.md">таблицей CallType в Lync Server 2013</a> .</p></td>
</tr>
<tr class="odd">
<td><p><strong>RequestType</strong></p></td>
<td><p>varbinary (33)</p></td>
<td><p> </p></td>
<td><p>Тип запроса, который завершился сбоем.</p>
<p>Эти данные можно преобразовать в текстовый формат, используя следующий синтаксис:</p>
<p><code>cast(cast(RequestType as varbinary(max)) as varchar(max))</code></p></td>
</tr>
<tr class="even">
<td><p><strong>Контента</strong></p></td>
<td><p>varbinary (257)</p></td>
<td><p> </p></td>
<td><p>Тип контента запроса, который завершился сбоем.</p>
<p>Эти данные можно преобразовать в текстовый формат с помощью синтаксиса:</p>
<p><code>cast(cast(ContentType as varbinary(max)) as varchar(max))</code></p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

