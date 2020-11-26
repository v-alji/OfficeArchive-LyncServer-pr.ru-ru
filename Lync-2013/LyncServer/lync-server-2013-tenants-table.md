---
title: 'Lync Server 2013: таблица Tenants'
description: 'Таблица клиентов Lync Server 2013: клиент.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Tenants table
ms:assetid: c1b070c1-2c59-4ca9-910b-43f673f97fda
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412950(v=OCS.15)
ms:contentKeyID: 48185309
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 96025dfd9fb42a6083f7f3daca98e243f01a8516
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441286"
---
# <a name="tenants-table-in-lync-server-2013"></a>Таблица Tenants в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-09-28_

Таблица "клиенты" — это вспомогательная таблица, в которой хранится список различных клиентов. Каждая запись в таблице представляет собой один клиент.

<div>


> [!NOTE]  
> В локальной среде CDR использует идентификатор клиента сборки для указания другого типа проверки подлинности, например общедоступной службы обмена мгновенными сообщениями, федеративного и анонимного.



</div>


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
<td><p><strong>TenantId</strong></p></td>
<td><p>целое</p></td>
<td><p>Primary</p></td>
<td><p>Уникальный номер, идентифицирующий этот идентификатор клиента.</p></td>
</tr>
<tr class="even">
<td><p><strong>TenantKey</strong></p></td>
<td><p>nvarchar(256)</p></td>
<td></td>
<td><p>Допустимые значения:</p>
<ul>
<li><p>00000000-0000-0000-0000-000000000000 – предприятие</p></li>
<li><p>00000000-0000-0000-0000-000000000001 – Федеративные</p></li>
<li><p>00000000-0000-0000-0000-000000000002 – анонимный</p></li>
<li><p>00000000-0000-0000-0000-000000000003 – общедоступная служба обмена мгновенными сообщениями</p></li>
</ul></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

