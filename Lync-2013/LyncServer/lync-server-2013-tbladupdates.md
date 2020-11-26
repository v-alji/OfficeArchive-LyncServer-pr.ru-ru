---
title: 'Lync Server 2013: tblADUpdates'
description: 'Lync Server 2013: tblADUpdates.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblADUpdates
ms:assetid: ba19fa16-4d2d-4635-ac32-f93e09469546
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615033(v=OCS.15)
ms:contentKeyID: 48185227
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7ab4418a10eac283d0f39d09b1c1fe15a32b2e68
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444485"
---
# <a name="tbladupdates-in-lync-server-2013"></a>tblADUpdates в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-09-12_

tblADUpdates содержит изменения доменных служб Active Directory, которые еще не были обработаны с помощью последующих шагов синхронизации Active Directory.

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
<td><p>prinGuid</p></td>
<td><p>GUID, а не NULL</p></td>
<td><p>Идентификатор GUID участника измененного объекта.</p></td>
</tr>
<tr class="even">
<td><p>prinADPath</p></td>
<td><p>nvarchar (384), NOT NULL</p></td>
<td><p>Отличительное имя объекта.</p></td>
</tr>
<tr class="odd">
<td><p>prinAttributesChanged</p></td>
<td><p>bit, NOT NULL</p></td>
<td><p>Значение true, если по крайней мере один из атрибутов объекта изменился.</p></td>
</tr>
<tr class="even">
<td><p>prinMembersChanged</p></td>
<td><p>bit, NOT NULL</p></td>
<td><p>Значение true, если изменилось членство.</p></td>
</tr>
<tr class="odd">
<td><p>prinAffiliationsChanged</p></td>
<td><p>bit, NOT NULL</p></td>
<td><p>Не используется.</p></td>
</tr>
<tr class="even">
<td><p>prinDeleted</p></td>
<td><p>bit, NOT NULL</p></td>
<td><p>Значение true, если объект был удален.</p></td>
</tr>
<tr class="odd">
<td><p>lastUpdated</p></td>
<td><p>DateTime, NOT NULL</p></td>
<td><p>Метка времени вставки строки.</p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

