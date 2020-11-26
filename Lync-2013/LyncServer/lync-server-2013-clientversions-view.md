---
title: 'Lync Server 2013: представление ClientVersions'
description: 'Lync Server 2013: ClientVersions View.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ClientVersions view
ms:assetid: caf7678f-83a0-46c8-83cc-fee4c3991f52
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721891(v=OCS.15)
ms:contentKeyID: 49733825
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 42ede7107a59db3162ac7f5344e47e81a80d57df
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434734"
---
# <a name="clientversions-view-in-lync-server-2013"></a>ClientVersions представления в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-10-01_

В представлении ClientVersions хранятся сведения о различных типах и версиях клиентов, которые принимали участие в сеансах, записанных в базе данных. Каждая запись в представлении представляет собой одну версию клиента. Это представление было представлено в Microsoft Lync Server 2013.

<div>


> [!NOTE]  
> Для некоторых столбцов может быть несколько записей.



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
<td><p><strong>VersionId</strong></p></td>
<td><p>целое</p></td>
<td><p>Уникальный номер, показывающий этот тип клиента и версию.</p></td>
</tr>
<tr class="even">
<td><p><strong>Версия</strong></p></td>
<td><p>nvarchar(256)</p></td>
<td><p>Представляет агент пользователя.</p></td>
</tr>
<tr class="odd">
<td><p><strong>ClientType</strong></p></td>
<td><p>целое</p></td>
<td><p>Тип клиента.</p></td>
</tr>
<tr class="even">
<td><p><strong>ClientCategory</strong></p></td>
<td><p>nvarchar (64)</p></td>
<td><p>Категория, к которой относится клиент. Например, клиент Conferencing_Attendant_1 .0 принадлежит ClientCategory CAA.</p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

