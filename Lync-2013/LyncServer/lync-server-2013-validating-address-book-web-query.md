---
title: 'Lync Server 2013: Проверка веб-запроса адресной книги'
description: 'Lync Server 2013: Проверка веб-запроса на адресную книгу.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Validating address book web query
ms:assetid: e6ae0a5a-e131-4cfe-9a33-6e611831072d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720925(v=OCS.15)
ms:contentKeyID: 63969662
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e73c39fc33f8d1851fc89d277333a94aaa137790
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438906"
---
# <a name="validating-address-book-web-query-in-lync-server-2013"></a>Проверка веб-запроса адресной книги в Lync Server 2013

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
<p>При запуске с помощью удаленного экземпляра Windows PowerShell пользователям должна быть назначена роль RBAC, имеющая разрешение на запуск командлета Test-CsAddressBookWebQuery. Чтобы просмотреть список всех ролей RBAC, которые могут использовать этот командлет, выполните в командной строке Windows PowerShell следующую команду:</p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsAddressBookWebQuery&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a>Описание

Командлет Test-CsAddressBookWebQuery позволяет администраторам удостовериться в том, что пользователи могут использовать службу веб-запросов адресной книги для поиска определенного контакта. Когда вы запускаете командлет, Test-CsAddressBookWebQuery сначала подключается к службе веб-билета для проверки подлинности. Если проверка подлинности прошла успешно, командлет подключится к службе веб-запросов адресной книги и проведет поиск по указанному контакту. Если этот контакт будет найден, командлет попытается вернуть эти данные на локальный компьютер. Тест помечается успешно, только если все эти действия можно выполнить.

Дополнительные сведения можно найти в справочной документации по командлету [Test-CsAddressBookWebQuery](https://docs.microsoft.com/powershell/module/skype/Test-CsAddressBookWebQuery) .

</div>

<div>

## <a name="running-the-test"></a>Выполнение теста

Командлет Test-CsAddressBookWebQuery можно выполнить с помощью предварительно настроенной тестовой учетной записи (см. раздел Настройка тестовых учетных записей для выполнения тестов Lync Server) или учетной записи пользователя, который включен для Lync Server. Для выполнения этой проверки с помощью тестовой учетной записи необходимо указать полное доменное имя пула сервера Lync Server и адрес SIP пользователя, который действует как цель поиска. Например:

    Test-CsAddressBookWebQuery -TargetFqdn "atl-cs-001.litwareinc.com" -TargetSipAddress "sip:davidlongmire@litwareinc.com"

Для выполнения этой проверки с использованием реальной учетной записи пользователя необходимо создать объект учетных данных Windows PowerShell, содержащий действительное имя пользователя и пароль. Затем необходимо добавить этот объект учетных данных и адрес SIP, назначенный учетной записи, когда код вызывает Test-CsAddressBookWebQuery:

    $credential = Get-Credential "litwareinc\kenmyer"
    Test-CsAddressBookWebQuery -TargetFqdn "atl-cs-001.litwareinc.com" -TargetSipAddress "sip:davidlongmire@litwareinc.com" -UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential

Дополнительные сведения можно найти в справочной документации по командлету [Test-CsAddressBookWebQuery](https://docs.microsoft.com/powershell/module/skype/Test-CsAddressBookWebQuery) .

</div>

<div>

## <a name="determining-success-or-failure"></a>Определение успеха или сбоя

Если указанный пользователь может подключаться к службе адресной книги и извлекать конечный адрес пользователя, вы вернете вывод, аналогичный этому, с помощью свойства Result, помеченного как успешно.

TargetUri : https://atl-cs-001.litwareinc.com:443/groupexpansion/service.svc

TargetFqdn: atl-cs-001.litwareinc.com

Результат: успех

Задержка: 00:00:06.2611356

Ошибки

Диагностик

Если указанному пользователю не удается подключиться или не удается получить целевой адрес пользователя, результат будет показан в виде ошибки, а дополнительные сведения будут записаны в свойствах Error и диагноз.

TargetUri : https://atl-cs-001.litwareinc.com:443/groupexpansion/service.svc

TargetFqdn: atl-cs-001.litwareinc.com

Результат: сбой

Задержка: 00:00:00

Ошибка: не удалось выполнить запрос веб-службы адресной книги с кодом ответа

NoEntryFound.

Диагностик

В предыдущем выводе говорится, что тест завершился сбоем, так как целевой пользователь не найден. Вы можете определить, был ли допустимый адрес SIP передан Test-CsAddressBookWebQuery, выполнив команду, подобную следующей:

    Get-CsUser | Where-Object {$_.SipAddress -eq "sip:davidlongmire@litwareinc.com"

Если Test-CsAddressBookWebQuery не удается, возможно, потребуется повторно выполнить тест, на этот раз включая параметр подробно:

    Test-CsAddressBookWebQuery -TargetFqdn "atl-cs-001.litwareinc.com" -TargetSipAddress "sip:davidlongmire@litwareinc.com" -Verbose

После включения подробной информации Test-CsAddressBookWebQuery будет возвращать пошаговые учетные записи каждого действия, которое он пытался выполнить, при проверке возможности указанного пользователя войти на сервер Lync Server. Например, эти выходные данные указывают на то, что Test-CsAddressBookWebQuery удалось подключиться к службе адресной книги, но ей не удалось найти адрес SIP, указанный ниже.

Начато действие "QueryAddressBookWebService".

Служба веб-запросов из адресной книги телефонной связи. URL-АДРЕС ABWS =

https://atl-cs-001.litwareinc.com:443/groupexpansion/service.svc

Исключение запроса в адресную книгу: запрос веб-службы адресной книги не удался с кодом ответа NoEntryFound.

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a>Причины, по которым может произойти сбой теста

Ниже приведены некоторые распространенные причины, по которым может произойти сбой Test-CsAddressBookWebQuery.

  - Вы указали недопустимую учетную запись пользователя. Для проверки существования учетной записи пользователя можно выполнить следующую команду:
    
        Get-CsUser "sip:kenmyer@litwareinc.com"

  - Учетная запись пользователя верна, но в настоящее время эта учетная запись не включена для Lync Server. Чтобы убедиться в том, что учетная запись пользователя включена для Lync Server, выполните команду, подобную следующей:
    
        Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object Enabled
    
    Если для свойства Enabled задано значение false, это означает, что пользователь в данный момент не включен для Lync Server.

  - Конечный пользователь может отсутствовать в адресной книге.

  - Возможно, адресная книга не полностью обновлена и не была реплицирована. Вы можете принудительно обновить все серверы адресной книги в вашей организации, выполнив следующую команду:
    
        Update-CsAddressBook

</div>

</div>

<span> </span>

</div>

</div>

</div>

