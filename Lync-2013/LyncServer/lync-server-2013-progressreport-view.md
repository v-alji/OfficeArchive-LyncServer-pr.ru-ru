---
title: 'Lync Server 2013: представление ProgressReport'
description: 'Lync Server 2013: ProgressReport View.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ProgressReport view
ms:assetid: b49f3fc7-0e2f-498f-8505-aaaf54e435f9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721857(v=OCS.15)
ms:contentKeyID: 49733790
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b95086012f254499644e778e43cafdf70ffc8f9c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436855"
---
# <a name="progressreport-view-in-lync-server-2013"></a>ProgressReport представления в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-10-01_

В представлении ProgressReport хранятся сведения о завершенных сеансах. Отчеты о ходе выполнения будут записываться только для звонков и сеансов, которые определяет Lync Server 2013, может быть полезен в целях диагностики. Это представление было представлено в Microsoft Lync Server 2013.

<div>


> [!NOTE]  
> Поля ErrorTime, ErrorReportSeq и ProgressReportSeq не обязательно ссылаются на ошибки, а также на сообщения, указывающие на состояние вызовов или сообщений.



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
<td><p><strong>ErrorTime</strong></p></td>
<td><p>datetime</p></td>
<td><p>Время возникновения ошибки. Используется в сочетании с ErrorReportSeq для уникальной идентификации ошибки.</p></td>
</tr>
<tr class="even">
<td><p><strong>ErrorReportSeq</strong></p></td>
<td><p>целое</p></td>
<td><p>ИДЕНТИФИКАЦИОНный номер для идентификации ошибки. Используется в сочетании с ErrorTime для уникальной идентификации ошибки.</p></td>
</tr>
<tr class="odd">
<td><p><strong>ProgressReportSeq</strong></p></td>
<td><p>целое</p></td>
<td><p>Идентификатор для идентификации отчета о ходе выполнения. Используется, чтобы отличать отчеты о ходе выполнения одного отчета об ошибках.</p></td>
</tr>
<tr class="even">
<td><p><strong>MsDiagId</strong></p></td>
<td><p>целое</p></td>
<td><p>Идентификатор диагностики для отчета об ошибке.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Источник</strong></p></td>
<td><p>nvarchar(256)</p></td>
<td><p>Имя сервера, отправившего ошибку (при отправке отчета из серверного компонента).</p></td>
</tr>
<tr class="even">
<td><p><strong>Приложение</strong></p></td>
<td><p>nvarchar(256)</p></td>
<td><p>Имя приложения, которое поступило об ошибке (при отправке отчета из серверного компонента).</p></td>
</tr>
<tr class="odd">
<td><p><strong>TelemetryId</strong></p></td>
<td><p>идентификатора</p></td>
<td><p>Уникальный идентификатор, соответствующий сведениям о времени соединения для различных компонентов, участвующих в Конференции.</p></td>
</tr>
<tr class="even">
<td><p><strong>SessionSetupTime</strong></p></td>
<td><p>целое</p></td>
<td><p>Время (в миллисекундах), требуемое конкретным компонентом для присоединения к Конференции.</p></td>
</tr>
<tr class="odd">
<td><p><strong>MsDiagHeader</strong></p></td>
<td><p>varchar (max)</p></td>
<td><p>Дополнительные сведения об ошибке.</p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

