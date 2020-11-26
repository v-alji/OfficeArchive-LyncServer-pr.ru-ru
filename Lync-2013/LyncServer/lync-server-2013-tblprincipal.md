---
title: 'Lync Server 2013: tblPrincipal'
description: 'Lync Server 2013: tblPrincipal.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblPrincipal
ms:assetid: 79a24502-b4ce-41f0-8979-8caddf535338
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558667(v=OCS.15)
ms:contentKeyID: 48184571
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0f07b37ac4c8ceed5c044b5c263eeee6370adfdc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444415"
---
# <a name="tblprincipal-in-lync-server-2013"></a>tblPrincipal в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-09-12_

tblPrincipal содержит всех участников, в том числе пользователей, папок и групп.

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
<td><p>prinID</p></td>
<td><p>int, NOT NULL</p></td>
<td><p>Идентификатор участника.</p></td>
</tr>
<tr class="even">
<td><p>prinGuid</p></td>
<td><p>GUID, а не NULL</p></td>
<td><p>Идентификатор GUID участника. Это широко используется как альтернативный первичный ключ, так как его значение пересекается с пространством доменных служб Active Directory. (GUID для кэшированного участника равен GUID соответствующего объекта Active Directory.)</p></td>
</tr>
<tr class="odd">
<td><p>prinUri</p></td>
<td><p>nvarchar (256), NOT NULL</p></td>
<td><p>Универсальный код ресурса (URI) участника. Схема SIP используется для пользователей, а MA-GRP используется практически всеми остальными.</p></td>
</tr>
<tr class="even">
<td><p>prinName</p></td>
<td><p>nvarchar (256)</p></td>
<td><p>Обычное имя. Используется только для пользовательских типов.</p></td>
</tr>
<tr class="odd">
<td><p>prinDisplayName</p></td>
<td><p>Nvarchar (256)</p></td>
<td><p>Отображаемое имя. Используется только для пользовательских типов.</p></td>
</tr>
<tr class="even">
<td><p>prinCompanyName</p></td>
<td><p>nvarchar (256)</p></td>
<td><p>Название компании. Используется только для пользовательских типов.</p></td>
</tr>
<tr class="odd">
<td><p>prinEmail</p></td>
<td><p>nvarchar (256)</p></td>
<td><p>Отправить по электронной почте. Используется только для пользовательских типов.</p></td>
</tr>
<tr class="even">
<td><p>prinADPath</p></td>
<td><p>nvarchar (384)</p></td>
<td><p>Доменное имя объекта Active Directory, который является кэшированной версией участника. Может принимать значение NULL для типов, которые не являются объектами службы каталогов Active Directory (например, пользователи системы).</p></td>
</tr>
<tr class="odd">
<td><p>prinADUserPrincipalName</p></td>
<td><p>nvarchar (256)</p></td>
<td><p>Имя участника-пользователя (UPN) пользователя. Используется только обычными типами пользователей.</p></td>
</tr>
<tr class="even">
<td><p>prinDisabled</p></td>
<td><p>smallint, NOT NULL</p></td>
<td><ul>
<li><p>0: участник активен.</p></li>
<li><p>1: участник отключен, поскольку возможности SIP пользователя отключены.</p></li>
<li><p>2: участник удален, так как связанный объект рекламы удален.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>prinTypeID</p></td>
<td><p>smallint, NOT NULL</p></td>
<td><p>Тип участника (из таблицы tblPrincipalType).</p></td>
</tr>
<tr class="even">
<td><p>prinPoolID</p></td>
<td><p>Типом</p></td>
<td><p>Назначение пула Lync для участника.</p></td>
</tr>
<tr class="odd">
<td><p>prinPolicyID</p></td>
<td><p>Типом</p></td>
<td><p>Значение политики сервера сохраняемого чата для пользователя, если указана политика типа тега.</p></td>
</tr>
<tr class="even">
<td><p>prinAddedBy</p></td>
<td><p>целое</p></td>
<td><p>Идентификатор участника создателя.</p></td>
</tr>
<tr class="odd">
<td><p>prinAddedOn</p></td>
<td><p>bigint, NOT NULL</p></td>
<td><p>Метка времени для времени создания.</p></td>
</tr>
<tr class="even">
<td><p>prinUpdatedBy</p></td>
<td><p>целое</p></td>
<td><p>Идентификатор участника, который последним обновил это.</p></td>
</tr>
<tr class="odd">
<td><p>prinUpdatedOn</p></td>
<td><p>bigint, NOT NULL</p></td>
<td><p>Метка времени для последнего обновления.</p></td>
</tr>
<tr class="even">
<td><p>prinVerifiedOn</p></td>
<td><p>DateTime, NOT NULL</p></td>
<td><p>Дата и время последнего обновления службы синхронизации Active Directory для участника.</p></td>
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
<td><p>prinID</p></td>
<td><p>Первичный ключ.</p></td>
</tr>
<tr class="even">
<td><p>prinTypeID</p></td>
<td><p>Внешний ключ с подстановкой в таблице tblPrincipalType. ptypeID.</p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

