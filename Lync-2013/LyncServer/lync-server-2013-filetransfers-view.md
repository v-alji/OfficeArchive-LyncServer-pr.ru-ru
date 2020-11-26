---
title: 'Lync Server 2013: представление FileTransfers'
description: 'Lync Server 2013: FileTransfers View.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: FileTransfers view
ms:assetid: e52c3ad0-152e-4a18-af1c-1aff0d205151
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721914(v=OCS.15)
ms:contentKeyID: 49733848
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dd2b084274a4d5daa093f2269617214f703ac03e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428155"
---
# <a name="filetransfers-view-in-lync-server-2013"></a>FileTransfers представления в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-10-01_

В представлении FileTransfer хранятся сведения о одноранговых сеансах передачи файлов. Это представление было представлено в Microsoft Lync Server 2013.

<div>


> [!NOTE]  
> В представлении FileTransfers содержатся все столбцы в <A href="lync-server-2013-sessiondetails-view.md">представлении SessionDetails в Lync Server 2013</A> в дополнение к столбцам, перечисленным ниже.



</div>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Столбец</th>
<th>Тип данных</th>
<th>Подробности</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>FileName</strong></p></td>
<td><p>nvarchar(256)</p></td>
<td><p>Имя перенесенного файла.</p></td>
</tr>
<tr class="even">
<td><p><strong>Файлах</strong></p></td>
<td><p>nvarchar(128</p></td>
<td><p>Используется для идентификации каждого сообщения к исполнению, связанного с этим сообщением.</p></td>
</tr>
<tr class="odd">
<td><p><strong>FileIdentity</strong></p></td>
<td><p>идентификатора</p></td>
<td><p>Уникальный идентификатор, позволяющий отличать передачу файлов с одним и тем же именем файла.</p></td>
</tr>
<tr class="even">
<td><p><strong>Отвечать</strong></p></td>
<td><p>бит</p></td>
<td><p>Может иметь значение истина или NULL. Если значение равно TRUE, то значение "отклонить" и "Отмена" будет равно NULL.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Отклонил</strong></p></td>
<td><p>бит</p></td>
<td><p>Может иметь значение истина или NULL. Если значение равно TRUE, то "принимать" и "Отмена" будут иметь значение NULL.</p></td>
</tr>
<tr class="even">
<td><p><strong>Отмена</strong>.</p></td>
<td><p>бит</p></td>
<td><p>Может иметь значение истина или NULL. Если значение равно TRUE, то принять и отклонить будет значение NULL.</p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

