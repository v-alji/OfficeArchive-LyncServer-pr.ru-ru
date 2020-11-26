---
title: 'Lync Server 2013: tblLastInviteId'
description: 'Lync Server 2013: tblLastInviteId.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblLastInviteId
ms:assetid: 222b3508-5963-4ddc-b4f3-e8412767e61b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558625(v=OCS.15)
ms:contentKeyID: 48183608
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e5a13cfc7edc29ea20c95f7f4d587b0cfb84eb73
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444422"
---
# <a name="tbllastinviteid-in-lync-server-2013"></a>tblLastInviteId в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-09-12_

tblLastInviteId — это последний идентификатор приглашения, созданный (и использованный в таблице tblPrincipalInvites) для каждого пользователя.

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
<td><p>lastInviteID</p></td>
<td><p>int, NOT NULL</p></td>
<td><p>Идентификатор приглашения последнего использован.</p></td>
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
<td><p>prinID</p></td>
<td><p>Внешний ключ с подстановкой в таблице tblPrincipal. prinID.</p></td>
</tr>
</tbody>
</table>


<div>

## <a name="see-also"></a>См. также


[tblPrincipalInvites в Lync Server 2013](lync-server-2013-tblprincipalinvites.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

