---
title: 'Lync Server 2013: Проверка входных параметров Lync Phone Edition'
description: 'Lync Server 2013: Проверка входных данные Lync Phone Edition.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing Lync Phone Edition login
ms:assetid: 1ccde6bf-9a2d-4fcf-b81f-1bc9fee2cfbb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn690128(v=OCS.15)
ms:contentKeyID: 63969583
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d21d65676c4f5e0f867c7d9556cdea50419be69b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398938"
---
# <a name="testing-lync-phone-edition-login-in-lync-server-2013"></a>Проверка входа в Lync Phone Edition в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2014-06-05_


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Расписание проверки</p></td>
<td><p>Ежедневно</p></td>
</tr>
<tr class="even">
<td><p>Средство тестирования</p></td>
<td><p>Windows PowerShell</p></td>
</tr>
<tr class="odd">
<td><p>Требуемые разрешения</p></td>
<td><p>При локальном запуске с помощью командной консоли Lync Server пользователи должны быть членами группы безопасности RTCUniversalServerAdmins.</p>
<p>При запуске с помощью удаленного экземпляра Windows PowerShell пользователям должна быть назначена роль RBAC, имеющая разрешение на запуск командлета Test-CsPhoneBootstrap. Чтобы просмотреть список всех ролей RBAC, которые могут использовать этот командлет, выполните в командной строке Windows PowerShell следующую команду:</p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsPhoneBootstrap&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a>Описание

Командлет Test-CsPhoneBootstrap позволяет администраторам войти в систему с помощью устройства Lync 2013 Phone Edition, которое будет использоваться для подтверждения того, что пользователь использует номер телефона и ПИН-код, назначенный ему. (Для выполнения теста на самом деле не требуется никаких устройств.)

Чтобы Test-CsPhoneBootstrap выполнить проверку, пул регистратора, на котором размещается тестируемая учетная запись пользователя, должен быть обнаруживаемым с помощью DHCP. Чтобы определить, может ли регистратор быть обнаруживаемым таким образом, используйте командлет Get-CsRegistrarConfiguration и проверьте значение свойства EnableDHCPServer. Если для этого свойства задано значение false, необходимо использовать Set-CsRegistrarConfiguration для задания значения свойства true и сделать его обнаруживаемым с помощью DHCP. Это также можно сделать с помощью DHCP-сервера Enterprise и настройки параметров, относящихся к Lync Server.

</div>

<div>

## <a name="running-the-test"></a>Выполнение теста

Чтобы запустить командлет Test-CsPhoneBootstrap, необходимо, как минимум, указать номер телефона и персональный идентификационный номер клиента (ПИН-код) для допустимого пользователя Lync Server. Например, эта команда проверяет возможности входа для пользователя с номером телефона 12065551219 и ПИН-кодом 0712:

    Test-CsPhoneBootstrap -PhoneOrExt "+12065551219" -Pin "0712"

Для более полной проверки можно также указать адрес SIP пользователя. В этом случае номер телефона, ПИН-код клиента и адрес SIP должны быть действительны для успешной проверки.

    Test-CsPhoneBootstrap -PhoneOrExt "+12065551219" -Pin "0712" -UserSipAddress "sip:kenmyer@litwareinc.com"

Дополнительные сведения можно найти в справочной документации по командлету [Test-CsPhoneBootstrap](https://docs.microsoft.com/powershell/module/skype/Test-CsPhoneBootstrap) .

</div>

<div>

## <a name="determining-success-or-failure"></a>Определение успеха или сбоя

Если указанный пользователь смог подключиться к серверу Lync Server, вы получите вывод, как показано ниже, и свойство Result, помеченное как **успешно.**

TargetUri : https://atl-cs-001.litwareinc.com:443/CertProv/

CertProvisioningService. svc

TargetFqdn: atl-cs-001.litwareinc.com

Результат: успех

Задержка: 00:00:06.3981276

Ошибки

Диагностик

Если указанный пользователь не смог установить соединение, результат будет показан как сбой, а дополнительные сведения будут записаны в свойствах Error и диагноз.

TargetFqdn: atl-cs-001.litwareinc.com

Результат: сбой

Задержка: 00:00:04.1993845

Ошибка: ошибка — ответ на службу Web-Ticket не получен.

Диагностик

В предыдущем выводе говорится, что тест завершился сбоем, так как служба веб-билета не ответила. Это может быть вызвано проблемой с самой службой или из-за того, что адрес SIP, номер телефона или клиентский PIN-код передан в тест — CsPhoneBootstrap. Вы можете проверить SIP-адрес и номер телефона пользователя, выполнив следующую команду:

    Get-CsUser -Identity "sip:kenmyer@litwareinc.com" | Select-Object SipAddress, LineUri

Вы также можете убедиться, что у пользователя есть допустимый ПИН-код, выполнив команду, как описано ниже.

    Get-CsClientPinInfo -Identity "sip:kenmyer@litwareinc.com" 

Если Test-CsPhoneBootstrap не удается, возможно, потребуется повторно выполнить тест, на этот раз включая параметр подробно:

    Test-CsPhoneBootstrap -PhoneOrExt "+12065551219" -Pin "0712" -Verbose

После включения подробной информации Test-CsPhoneBootstrap будет возвращать пошаговые учетные записи каждого действия, которое он пытался войти на сервер Lync Server. Например, ниже приведена часть выходных данных для неудачного входа в сеанс, в котором был указан неверный ПИН-код:

Использование проверки подлинности PIN-кода с телефонным телефоном \\ : 12065551219 PIN: 0712

Не удалось получить веб-билет

ОПРЕДЕЛИТЬ

\- URL веб-службы является действительным, и веб-службы работают

\- Если \\ для проверки подлинности используется закрепление PhoneNo, убедитесь, что они соответствуют универсальному коду ресурса пользователя

\- При использовании \\ проверки подлинности NTLM Kerberos убедитесь, что вы указали действительные учетные данные.

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a>Причины, по которым может произойти сбой теста

Ниже приведены некоторые распространенные причины, по которым может произойти сбой Test-CsPhoneBootstrap.

  - Возможно, указан недопустимый адрес SIP. Вы можете проверить, правильно ли указан адрес SIP, используя одну из следующих команд:
    
        Get-CsUser -Identity "sip:kenmyer@litwareinc.com"

  - Возможно, указан недопустимый ПИН-код. Несмотря на то, что вы не можете получить PIN-код пользователя, вы можете убедиться, что у пользователя по крайней мере есть PIN-код, используя следующую команду:
    
        Get-CsClientPinInfo -Identity "sip:kenmyer@litwareinc.com"

  - Возможно, указан недопустимый номер телефона. Вы можете проверить телефон пользователя, выполнив команду, подобную следующей:
    
        Get-CsUser -Identity "sip:kenmyer@litwareinc.com" | Select-Object LineUri

  - Для пула регистраторов не включена служба DHCP. Чтобы определить, активирован ли пул регистратора для DHCP, выполните командлет Get-CsRegistrarConfiguration и проверьте значение свойства EnableDHCPServer. Например:
    
        Get-CsRegistrarConfiguration -Identity "global"

</div>

</div>

<span> </span>

</div>

</div>

</div>

