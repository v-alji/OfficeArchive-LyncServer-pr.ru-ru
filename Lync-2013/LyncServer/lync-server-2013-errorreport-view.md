---
title: 'Lync Server 2013: представление ErrorReport'
description: 'Lync Server 2013: ErrorReport View.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ErrorReport view
ms:assetid: ca873f7e-b18b-4eaf-8db0-5f9d5a9b60a1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721887(v=OCS.15)
ms:contentKeyID: 49733821
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 50fb0a362c71d8dfb5873157e7b1ed3d3eb680ae
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428526"
---
# <a name="errorreport-view-in-lync-server-2013"></a>ErrorReport представления в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2013-01-22_

В представлении ErrorReport хранятся сведения об ошибках, о которых сообщается. Каждая запись содержит один экземпляр ошибки. Эти ошибки регистрируются агентом CDR, который запущен на сервере переднего плана или отправлен клиентом. Это представление было представлено в Microsoft Lync Server 2013.


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
<td><p><strong>MsDiagId</strong></p></td>
<td><p>целое</p></td>
<td><p>Идентификатор диагностики для отчета об ошибке.</p></td>
</tr>
<tr class="even">
<td><p><strong>FromUri</strong></p></td>
<td><p>nvarchar (450)</p></td>
<td><p>URI пользователя, который поступил с ошибкой.</p></td>
</tr>
<tr class="odd">
<td><p><strong>FromUriType</strong></p></td>
<td><p>nvarchar(256)</p></td>
<td><p>Тип URI пользователя, который поступил на ошибку. Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-uritypes-table.md">таблицей UriTypes в Lync Server 2013</a> .</p></td>
</tr>
<tr class="even">
<td><p><strong>FromTenant</strong></p></td>
<td><p>nvarchar(256)</p></td>
<td><p>Клиент пользователя, который поступил с ошибкой. Дополнительные сведения приведены в <a href="lync-server-2013-tenants-table.md">таблице "клиенты" в Lync Server 2013</a> .</p></td>
</tr>
<tr class="odd">
<td><p><strong>ToUri</strong></p></td>
<td><p>nvarchar (450)</p></td>
<td><p>Универсальный код ресурса (URI) пользователя, который является целью отчета об ошибке.</p></td>
</tr>
<tr class="even">
<td><p><strong>ToUriType</strong></p></td>
<td><p>nvarchar(256)</p></td>
<td><p>Тип URI пользователя, который является конечным лицом отчета об ошибке. Для получения дополнительных сведений ознакомьтесь с таблицей UriTypes.</p></td>
</tr>
<tr class="odd">
<td><p><strong>ToTenant</strong></p></td>
<td><p>nvarchar(256)</p></td>
<td><p>Клиент пользователя, который является конечным лицом отчета об ошибке. Дополнительные сведения приведены в <a href="lync-server-2013-tenants-table.md">таблице "клиенты" в Lync Server 2013</a> .</p></td>
</tr>
<tr class="even">
<td><p><strong>ConferenceUri</strong></p></td>
<td><p>nvarchar (450)</p></td>
<td><p>Универсальный код ресурса (URI) Конференции, которая была целью отчета об ошибке.</p></td>
</tr>
<tr class="odd">
<td><p><strong>ConferenceUriType</strong></p></td>
<td><p>nvarchar(256)</p></td>
<td><p>Тип URI конференции, которая была целью отчета об ошибке. Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-uritypes-table.md">таблицей UriTypes в Lync Server 2013</a> .</p></td>
</tr>
<tr class="even">
<td><p><strong>SessionIdTime</strong></p></td>
<td><p>datetime</p></td>
<td><p>Время запроса сеанса, в котором был создан отчет об ошибке. Используется в сочетании с SessionIdSeq для уникальной идентификации сеанса. Дополнительные сведения приведены <a href="lync-server-2013-dialogs-table.md">в таблице диалоговые окна Lync Server 2013</a> .</p></td>
</tr>
<tr class="odd">
<td><p><strong>SessionIdSeq</strong></p></td>
<td><p>целое</p></td>
<td><p>ИДЕНТИФИКАЦИОНный номер для идентификации запроса на сеанс, который является источником отчета об ошибке. Используется в сочетании с SessionIdTime для уникальной идентификации сеанса. Дополнительные сведения приведены <a href="lync-server-2013-dialogs-table.md">в таблице диалоговые окна Lync Server 2013</a> .</p></td>
</tr>
<tr class="even">
<td><p><strong>DialogId</strong></p></td>
<td><p>varstring (775)</p></td>
<td><p>ИДЕНТИФИКАТОР диалогового окна SIP сеанса, на который поступила ошибка. Формат:</p>
<p>диалоговое окно; тег "from-Tag"</p>
<p>Эти данные можно преобразовать в текстовый формат, используя следующий синтаксис:</p>
<p>Cast (CAST (ExternalId AS varbinary (max)) AS varchar (max))</p></td>
</tr>
<tr class="odd">
<td><p><strong>ClientVersion</strong></p></td>
<td><p>nvarchar(256)</p></td>
<td><p>Версия клиента, используемая пользователем, который поступил с ошибкой.</p></td>
</tr>
<tr class="even">
<td><p><strong>ClientType</strong></p></td>
<td><p>целое</p></td>
<td><p>Клиент, использованный пользователем, который поступил с ошибкой. Дополнительные сведения вы увидите <a href="lync-server-2013-useragentdef-table.md">в таблице UserAgentDef в Lync Server 2013</a> .</p></td>
</tr>
<tr class="odd">
<td><p><strong>ClientCategory</strong></p></td>
<td><p>nvarchar (64)</p></td>
<td><p>Имя категории клиента, используемой пользователем, который поступил с ошибкой.</p></td>
</tr>
<tr class="even">
<td><p><strong>Источник</strong></p></td>
<td><p>nvarchar(256)</p></td>
<td><p>Имя сервера, отправившего ошибку (при отправке отчета из серверного компонента).</p></td>
</tr>
<tr class="odd">
<td><p><strong>Приложение</strong></p></td>
<td><p>nvarchar(256)</p></td>
<td><p>Имя приложения, которое поступило об ошибке (при отправке отчета из серверного компонента).</p></td>
</tr>
<tr class="even">
<td><p><strong>ResponseCode</strong></p></td>
<td><p>целое</p></td>
<td><p>Код ответа SIP в сеанс сообщения SIP с отчетом об ошибке.</p></td>
</tr>
<tr class="odd">
<td><p><strong>RequestType</strong></p></td>
<td><p>varchar (max)</p></td>
<td><p>Тип запроса, который завершился сбоем.</p></td>
</tr>
<tr class="even">
<td><p><strong>Контента</strong></p></td>
<td><p>varchar (max)</p></td>
<td><p>Тип контента запроса, который завершился сбоем.</p></td>
</tr>
<tr class="odd">
<td><p><strong>CallType</strong></p></td>
<td><p>nvarchar(256)</p></td>
<td><p>Тип сеанса. Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-calltype-table.md">таблицей CallType в Lync Server 2013</a> .</p></td>
</tr>
<tr class="even">
<td><p><strong>TelemetryId</strong></p></td>
<td><p>идентификатора</p></td>
<td><p>Уникальный идентификатор, соответствующий сведениям о времени соединения для различных компонентов, участвующих в Конференции.</p></td>
</tr>
<tr class="odd">
<td><p><strong>SetupTime</strong></p></td>
<td><p>целое</p></td>
<td><p>Время (в миллисекундах), требуемое конкретным компонентом для присоединения к Конференции.</p></td>
</tr>
<tr class="even">
<td><p><strong>IsCapturedByServer</strong></p></td>
<td><p>бит</p></td>
<td><p>Указывает, был ли отчет об ошибке записан агентом CDR, запущенным на сервере переднего плана или отправлен клиентом.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Пометка</strong></p></td>
<td><p>smallint</p></td>
<td><p>Зарезервировано для будущего использования.</p></td>
</tr>
<tr class="even">
<td><p><strong>MsDiagHeader</strong></p></td>
<td><p>varchar (max)</p></td>
<td><p>Дополнительные сведения об ошибке.</p></td>
</tr>
<tr class="odd">
<td><p><strong>FrontEnd</strong></p></td>
<td><p>nvarchar</p></td>
<td><p>Полное доменное имя сервера переднего плана, отправившего отчет.</p></td>
</tr>
<tr class="even">
<td><p><strong>Pool</strong></p></td>
<td><p>nvarchar</p></td>
<td><p>Полное доменное имя пула, содержащего сервер переднего плана, отправивший отчет.</p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

