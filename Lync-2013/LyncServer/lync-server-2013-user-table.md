---
title: 'Lync Server 2013: таблица User'
description: 'Lync Server 2013: пользовательская таблица.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: User table
ms:assetid: 6b52047e-286d-47ab-b7bc-a9b266f62d82
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398505(v=OCS.15)
ms:contentKeyID: 48184437
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 15d1ac08a229f4afea35a2727ef1105a5f24b826
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444170"
---
# <a name="user-table-in-lync-server-2013"></a>Таблица User в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-10-02_

Таблица user — это вспомогательная таблица, в которой хранится список различных пользователей, которые участвовали в сеансах, записанных в базе данных. Каждая запись в таблице представляет одного пользователя.


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
<td><p><strong>UserKey</strong></p></td>
<td><p>целое</p></td>
<td><p>Primary</p></td>
<td><p>Уникальный номер, идентифицирующий этого пользователя.</p></td>
</tr>
<tr class="even">
<td><p><strong>КОД</strong></p></td>
<td><p>nvarchar (450)</p></td>
<td><p>Повторя</p></td>
<td><p>Строка URI.</p></td>
</tr>
<tr class="odd">
<td><p><strong>URIType</strong></p></td>
<td><p>целое</p></td>
<td></td>
<td><p>1 — неизвестный тип URI.</p>
<p>2 — это универсальный код ресурса пользователя.</p>
<p>4 — универсальный код ресурса Конференции.</p>
<p>8 — это универсальный код ресурса (URI) телефона.</p></td>
</tr>
<tr class="even">
<td><p><strong>TenantKey</strong></p></td>
<td><p>целое</p></td>
<td><p>Другом</p></td>
<td><p>Клиент для пользователя, на который ссылается таблица "клиент".</p></td>
</tr>
<tr class="odd">
<td><p><strong>LastPoorCallTime</strong></p></td>
<td><p>datetime</p></td>
<td></td>
<td><p>Самая поздняя метка времени, когда пользователь приходил к вызову неудовлетворительного звука.</p></td>
</tr>
<tr class="even">
<td><p><strong>NextUpdateTS</strong></p></td>
<td><p>datetime</p></td>
<td></td>
<td><p>Только для внутреннего использования.</p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

