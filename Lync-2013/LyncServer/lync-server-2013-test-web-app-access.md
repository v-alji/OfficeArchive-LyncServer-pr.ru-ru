---
title: 'Lync Server 2013: Проверка доступа к веб-приложению'
description: 'Lync Server 2013: Проверка доступа к веб-приложению.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test Web App access
ms:assetid: 17d67ea3-f74d-4952-ac2b-92c0dacc8014
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn767944(v=OCS.15)
ms:contentKeyID: 63969584
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fc3bbc8008df4fe47fc5a39571356383fe5a6035
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441132"
---
# <a name="test-web-app-access-in-lync-server-2013"></a>Проверка доступа к веб-приложению в Lync Server 2013

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
<p>При запуске с помощью удаленного экземпляра Windows PowerShell пользователям должна быть назначена роль RBAC, имеющая разрешение на запуск командлета Test-CsWebApp. Чтобы просмотреть список всех ролей RBAC, которые могут использовать этот командлет, выполните в командной строке Windows PowerShell следующую команду:</p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsWebApp&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a>Описание

Командлет Test-CsWebApp удостоверяет, что пользователи, прошедшие проверку подлинности, могут присоединиться к конференциям Lync Server с помощью Lync Web App. Когда вы запускаете командлет, Test-CsWebApp обращается к службе веб-билета, чтобы получить веб-билеты для указанных пользователей. Эти билеты эффективно действуют в конференц-зале Lync Server с помощью билетов на допускную связь. Если вы можете получить билеты, и если пользователи могут проходить проверку подлинности, Test-CsWebApp будут обращаться к Lync Server и попытаться установить отдельные конференции для обмена мгновенными сообщениями, совместного использования приложений и совместной работы с данными.

Обратите внимание, что Test-CsWebApp просто проверяет интерфейсы API и соединения, используемые для создания этих конференций. Этот командлет предназначен для проверки того, что приложение Lync Web App можно использовать для создания и присоединения к конференциям. Тем не менее, в действительности она не создает и не проводит конференции.

</div>

<div>

## <a name="running-the-test"></a>Выполнение теста

Командлет Test-CsWebApp можно выполнить с помощью пары предварительно настроенных тестовых учетных записей или учетных записей двух пользователей, которые включены в Lync Server. Для выполнения этой проверки с помощью тестовых учетных записей нужно просто указать полное доменное имя для тестируемого пула сервера Lync Server. Например:

    Test-CsWebApp -TargetFqdn "atl-cs-001.litwareinc.com"

Для выполнения этой проверки с использованием фактических учетных записей пользователей необходимо создать два объекта учетных данных Windows PowerShell (объекты, содержащие имя и пароль учетной записи) для каждой учетной записи. После вызова Test-CsWebApp вы должны добавить эти объекты учетных данных и адреса SIP для двух учетных записей.

    $cred1 = Get-Credential "litwareinc\kenmyer"
    $cred2 = Get-Credential "litwareinc\pilar"
    
    Test-CsWebApp -TargetFqdn atl-cs-001.litwareinc.com -UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $cred1 -User2SipAddress "sip:pilar@litwareinc.com" -User2Credential $cred2

Дополнительные сведения можно найти в разделе справки по командлету [Test-CsWebApp](https://docs.microsoft.com/powershell/module/skype/Test-CsWebApp) . Обратите внимание, что Test-CsWebApp не рекомендуется использовать в Lync Server 2013.

</div>

<div>

## <a name="determining-success-or-failure"></a>Определение успеха или сбоя

Если Test-CsWebApp можете присоединиться к своим конференциям, командлет вернет результат теста "успешно".

Целевое полное доменное имя:

Результат: успех

Задержка: 00:00:00

Сообщение об ошибке:

Диагностик

Если пользователи не могут присоединиться к необходимым конференциям, результат теста будет помечен как сбой. Обычно Test-CsWebApp также сообщает о подробном сообщении об ошибке и диагностике:

Целевое полное доменное имя: atl-cs-001.litwareinc.com

Результат: сбой

Задержка: 00:00:00

Сообщение об ошибке: ни одного ответа не получено для службы Web-Ticket

Диагностика: запрос HTTP-запроса не разрешен клиентом

Схема проверки подлинности "NTLM". Проверка подлинности

заголовку, полученному от сервера, является "Negotiate, NTLM".

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a>Причины, по которым может произойти сбой теста

Обычно ошибки, связанные с проверкой подлинности пользователей, Test-CsWebApp. Если Test-CsWebApp не удается, сначала убедитесь в том, что у указанных пользователей есть действительные учетные записи пользователей и они включены для Lync Server. Вы можете получить сведения об учетной записи с помощью следующей команды:

    Get-CsUser -Identity "sip:kenmyer@litwareinc.com" | Select-Object Enabled

Если свойство Enabled не равно true или если команда не выполнена, это означает, что у пользователя нет действительной учетной записи Lync Server. Кроме того, необходимо убедиться, что указанные в командлете пароли действительны.

</div>

</div>

<span> </span>

</div>

</div>

</div>

