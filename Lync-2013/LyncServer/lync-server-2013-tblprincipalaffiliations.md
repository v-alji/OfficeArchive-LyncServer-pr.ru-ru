---
title: 'Lync Server 2013: tblPrincipalAffiliations'
description: 'Lync Server 2013: tblPrincipalAffiliations.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblPrincipalAffiliations
ms:assetid: 45fd8484-5837-44d2-85bb-45c83546607c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558642(v=OCS.15)
ms:contentKeyID: 48183993
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 01c373147a58300e64f22e60e989a777c59b2653
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441370"
---
# <a name="tblprincipalaffiliations-in-lync-server-2013"></a>tblPrincipalAffiliations в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-09-12_

tblPrincipalAffiliations содержит основные сведения о членстве в расположениях, в том числе о группах безопасности доменных служб Active Directory, в контейнерах Active Directory в доменах.

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
<td><p>principalID</p></td>
<td><p>int, NOT NULL</p></td>
<td><p>Идентификатор присоединенного участника.</p></td>
</tr>
<tr class="even">
<td><p>affiliationID</p></td>
<td><p>int, NOT NULL</p></td>
<td><p>Идентификатор участника, представляющего назначение. Каждый принципал (за исключением системных типов пользователей) также имеет свое Самоназначение.</p></td>
</tr>
<tr class="odd">
<td><p>индекса</p></td>
<td><p>int, NOT NULL</p></td>
<td><p>Индекса. Значение для самостоятельных принадлежностей —-1, а для других — для других — в пределах от 1 в каждом &lt; principalID, affiliationId &gt; сегмент.</p></td>
</tr>
<tr class="even">
<td><p>updatedBy</p></td>
<td><p>int, NOT NULL</p></td>
<td><p>Основной участник, который обновил Последнее обновление. Обычно это 1, что означает синхронизацию Active Directory.</p></td>
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
<th>Столбцов</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>&lt;principalID, index, affiliationID&gt;</p></td>
<td><p>Первичный ключ.</p></td>
</tr>
<tr class="even">
<td><p>principalID</p></td>
<td><p>Внешний ключ с подстановкой в таблице tblPrincipal. prinID.</p></td>
</tr>
<tr class="odd">
<td><p>affiliationID</p></td>
<td><p>Внешний ключ с подстановкой в таблице tblPrincipal. prinID.</p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

