---
title: 'Lync Server 2013: таблица Region'
description: 'Таблица Lync Server 2013: Region.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Region table
ms:assetid: 1751a6aa-a6e8-4f16-8eb7-ae731c2e3ee3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398235(v=OCS.15)
ms:contentKeyID: 48183518
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 544827434808a0277438984c420fcc39cd1b02a8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436561"
---
# <a name="region-table-in-lync-server-2013"></a>Таблица Region в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2010-11-09_

Таблица Region является вспомогательной таблицей. Каждая запись представляет одну страну/регион, определенные в параметрах конфигурации сети.


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
<td><p><strong>RegionKey</strong></p></td>
<td><p>целое</p></td>
<td><p>Primary</p></td>
<td><p>Уникальный номер, идентифицирующий страну или регион.</p></td>
</tr>
<tr class="even">
<td><p><strong>RegionName</strong></p></td>
<td><p>nvarchar(128</p></td>
<td><p>Повторя</p></td>
<td><p>Название страны/региона.</p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

