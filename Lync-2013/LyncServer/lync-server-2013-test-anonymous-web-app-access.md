---
title: 'Lync Server 2013: Проверка анонимного доступа к веб-приложению'
description: 'Lync Server 2013: Проверка анонимного доступа к веб-приложению.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test anonymous Web App access
ms:assetid: 92f691cd-e05e-4bab-beb5-251d4b837a19
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn767949(v=OCS.15)
ms:contentKeyID: 63969630
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 11c33840912fefcaeef069e14773cfefd0834a8b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441272"
---
# <a name="test-anonymous-web-app-access-in-lync-server-2013"></a>Проверка доступа анонимного веб-приложения в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2014-06-07_


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Расписание проверки</p></td>
<td><p>Ежемесячно</p></td>
</tr>
<tr class="even">
<td><p>Средство тестирования</p></td>
<td><p>Windows PowerShell</p></td>
</tr>
<tr class="odd">
<td><p>Требуемые разрешения</p></td>
<td><p>При локальном запуске с помощью командной консоли Lync Server пользователи должны быть членами группы безопасности RTCUniversalServerAdmins.</p>
<p>При запуске с помощью удаленного экземпляра Windows PowerShell пользователям должна быть назначена роль RBAC, имеющая разрешение на запуск командлета Test-CsWebAppAnonymous. Чтобы просмотреть список всех ролей RBAC, которые могут использовать этот командлет, выполните в командной строке Windows PowerShell следующую команду:</p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsWebAppAnonymous&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a>Описание

Командлет Test-CsWebAppAnonymous удостоверяется в том, что анонимный пользователь может присоединиться к конференциям Lync Server с помощью Lync Web App. Когда вы запускаете командлет, Test-CsWebAppAnonymous обращается к службе веб-билета для получения веб-билета для анонимного пользователя. Если командлету удалось получить этот билет, Test-CsWebAppAnonymous будет обращаться к Lync Server и попытаться установить отдельные конференции для обмена мгновенными сообщениями, общего обмена приложениями и совместной работы с данными.

Обратите внимание, что Test-CsWebAppAnonymous только проверяет интерфейсы API и соединения, используемые для создания этих конференций. На самом деле командлеты не создают и не выполняют никакие Конференции.

</div>

<div>

## <a name="running-the-test"></a>Выполнение теста

Командлет Test-CsWebAppAnonymous можно выполнить с помощью пары предварительно настроенных тестовых учетных записей или учетных записей двух пользователей, которые включены в Lync Server. Для выполнения этой проверки с помощью тестовых учетных записей нужно просто указать полное доменное имя для тестируемого пула сервера Lync Server. Например:

    Test-CsWebAppAnonymous -TargetFqdn atl-cs-001.litwareinc.com

Для выполнения этой проверки с использованием фактических учетных записей пользователей необходимо создать два объекта учетных данных командной консоли Lync Server (объекты, содержащие имя и пароль учетной записи) для каждой учетной записи. После вызова Test-CsWebAppAnonymous вы должны добавить эти объекты учетных данных и адреса SIP для двух учетных записей.

    $cred1 = Get-Credential "litwareinc\kenmyer"
    
    Test-CsWebApp -TargetFqdn atl-cs-001.litwareinc.com -UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $cred1

Дополнительные сведения можно найти в разделе справки по командлету Test-CsWebAppAnonymous. Обратите внимание, что Test-CsWebAppAnonymous не рекомендуется использовать в Lync Server 2013.

</div>

<div>

## <a name="determining-success-or-failure"></a>Определение успеха или сбоя

Если Test-CsWebAppAnonymous может присоединиться к своим собраниям для анонимного пользователя, командлет вернет результат теста "успешно".

Целевое полное доменное имя:

Результат: успех

Задержка: 00:00:00

Сообщение об ошибке:

Диагностик

Если анонимный пользователь не может присоединиться к необходимым конференциям, результат теста будет помечен как сбой. Обычно Test-CsWebAppAnonymous также сообщает о подробном сообщении об ошибке и диагностике:

Целевое полное доменное имя: atl-cs-001.litwareinc.com

Результат: сбой

Задержка: 00:00:05.9746266

Сообщение об ошибке: ни одного ответа не получено для службы Web-Ticket

Диагностика: запрос HTTP-запроса не разрешен клиентом

Схема проверки подлинности "NTLM". Проверка подлинности

заголовку, полученному от сервера, является "Negotiate, NTLM".

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a>Причины, по которым может произойти сбой теста

Ошибки Test-CsWebAppAnonymous обычно связаны с ошибками проверки подлинности пользователей: необходимо выполнить тест с помощью действительной учетной записи пользователя, несмотря на то, что командлет проверяет возможность подключения анонимного пользователя к Lync Server. Если Test-CsWebAppAnonymous не удается, необходимо проверить, является ли указанный пользователь действительной учетной записью пользователя Lync Server. Вы можете получить сведения об учетной записи Lync Server с помощью следующей команды:

    Get-CsUser -Identity "sip:kenmyer@litwareinc.com" | Select-Object Enabled

Если свойство Enabled не равно true или если команда не выполнена, это означает, что у пользователя нет действительной учетной записи Lync Server.

Кроме того, необходимо убедиться, что пароль, предоставленный при запуске командлета, является действительным паролем.

Проблемы с конфигурацией с помощью сервера Office Web Apps также могут привести к сбою Test-CsWebAppAnonymous; Это часто может возникнуть, если вы получаете следующую диагностику:

Запрос HTTP не разрешен в схеме проверки подлинности клиента "NTLM". Заголовок проверки подлинности, полученный от сервера, — "Negotiate, NTLM".

Дополнительные сведения о диагностике и устранении проблем с сервером Office Web Apps см. в блоге [сервер Office Web apps 2013 — компьютеры, на которых выводится сообщение о неработоспособности](http://www.wictorwilen.se/office-web-apps-server-2013---machines-are-always-reported-as-unhealthy).

</div>

</div>

<span> </span>

</div>

</div>

</div>

