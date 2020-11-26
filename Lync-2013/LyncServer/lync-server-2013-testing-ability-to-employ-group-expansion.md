---
title: 'Lync Server 2013: Проверка возможности развертывания групп'
description: 'Lync Server 2013: Проверка возможности развертывания групп.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing ability to employ group expansion
ms:assetid: 9b0fc954-6f9c-411a-ab32-94ebabc42de2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn743836(v=OCS.15)
ms:contentKeyID: 63969634
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6267bc2099fc420c5c57e1ef80f4bf4491334938
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441111"
---
# <a name="testing-ability-to-employ-group-expansion-in-lync-server-2013"></a>Тестирование возможности развертывания групп в Lync Server 2013

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
<p>При запуске с помощью удаленного экземпляра Windows PowerShell пользователям должна быть назначена роль RBAC, имеющая разрешение на запуск командлета Test-CsGroupExpansion. Чтобы просмотреть список всех ролей RBAC, которые могут использовать этот командлет, выполните в командной строке Windows PowerShell следующую команду:</p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsGroupExpansion&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a>Описание

Командлет Test-CsGroupExpansion позволяет определить, работает ли расширение групп в Организации. Если включено расширение группы, пользователи настраивают группы рассылки как контакты. Это означает, что пользователи смогут отправить одно и то же мгновенное сообщение всем участникам группы, направив сообщение группе, а не отдельным участникам этой группы. Расширение групп позволяет быстро и легко просмотреть всех участников группы и их текущее состояние.

С помощью командлета Test-CsGroupExpansion вы указываете группу рассылки Active Directory, используя адрес электронной почты группы. Test-CsGroupExpansion затем использует расширение группы для получения сведений о членстве в группах и сравнения извлеченного списка с членством в указанном адресе электронной почты группы. Если два списка соответствуют друг другу, то расширение группы работает правильно. Обратите внимание, что вы можете протестировать расширение группы двумя способами: Протестируйте саму службу или проверяя связанную веб-службу.

Дополнительные сведения можно найти в справочной документации по командлету [Test-CsGroupExpansion](https://docs.microsoft.com/powershell/module/skype/Test-CsGroupExpansion) .

</div>

<div>

## <a name="running-the-test"></a>Выполнение теста

Командлет Test-CsGroupExpansion можно выполнить с помощью предварительно настроенной тестовой учетной записи (см. раздел Настройка тестовых учетных записей для выполнения тестов Lync Server) или учетной записи пользователя, который был включен для Lync Server. Для выполнения этой проверки с помощью тестовой учетной записи необходимо указать полное доменное имя тестируемого пула сервера Lync и адрес электронной почты для действительной группы рассылки. Например:

    Test-CsGroupExpansion -TargetFqdn "atl-cs-001.litwareinc.com" -GroupEmailAddress "Sales@litwareinc.com"

Чтобы выполнить эту проверку с использованием реальной учетной записи пользователя, необходимо сначала создать объект учетных данных Lync Server, содержащий имя учетной записи и пароль. Затем необходимо добавить этот объект учетных данных и адрес SIP, назначенный учетной записи, когда система вызывает Test-CsGroupExpansion:

    $credential = Get-Credential "litwareinc\kenmyer"
    Test-CsGroupExpansion -TargetFqdn "atl-cs-001.litwareinc.com" -GroupEmailAddress "Sales@litwareinc.com" -UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential

Дополнительные сведения можно найти в справочной документации по командлету [Test-CsGroupExpansion](https://docs.microsoft.com/powershell/module/skype/Test-CsGroupExpansion) .

</div>

<div>

## <a name="determining-success-or-failure"></a>Определение успеха или сбоя

Если указанный пользователь может использовать расширение группы, вы будете получать выходные данные, аналогичные этим, с помощью свойства Result, помеченного как **успешно.**

TargetUri : https://atl-cs-001.litwareinc.com:443/groupexpansion/service.svc

TargetFqdn: atl-cs-001.litwareinc.com

Результат: успех

Задержка: 00:00:01.1234976

Ошибки

Диагностик

Если указанный пользователь не может использовать расширение группы, результат будет показан как сбой, а дополнительные сведения будут записаны в свойствах Error и диагноз.

TargetUri : https://atl-cs-001.litwareinc.com:443/groupexpansion/service.svc

TargetFqdn: atl-cs-001.litwareinc.com

Результат: сбой

Задержка: 00:00:00

Ошибки

Диагностик

Test-CsGroupExpansion: не удалось зарегистрировать конечную точку. Ознакомьтесь с ErrorCode по конкретной причине.

В предыдущем выводе говорится, что тест завершился сбоем, так как указанный пользователь не смог зарегистрироваться в Lync Server. Обычно это происходит, если учетная запись пользователя не существует или не включена в Lync Server. Вы можете проверить существование учетной записи и определить, включена ли учетная запись для NM-OCS-14-3, выполнив команду, подобную следующей:

    Get-CsUser -Identity "sip:kenmyer@litwareinc.com" | Select-Object SipAddress, Enabled

Если Test-CsGroupExpansion не удается, возможно, потребуется повторно выполнить тест, на этот раз включая параметр подробно:

    Test-CsGroupExpansion -TargetFqdn "atl-cs-001.litwareinc.com" -GroupEmailAddress "Sales@litwareinc.com" -Verbose

При включенном параметре подробных данных Test-CsGroupExpansion будет возвращать пошаговые учетные записи каждого действия, которое он пытался войти на сервер Lync Server. Например, эти выходные данные указывают на то, что не удалось найти указанную группу рассылки:

Попытка получить веб-билет.

URL веб-службы: https://atl-cs-001.litwareinc.com:443/WebTicket/WebTicketService.svc

Использование проверки подлинности NTLM/Kerb.

GetWebTicketActivity завершен.

Начато действие "VerifyDistributionList".

Состояние ответа веб-службы DLX: NotFound.

Действие "VerifyDistributionList" завершено в течение "0,2597923" сек.

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a>Причины, по которым может произойти сбой теста

Ниже приведены некоторые распространенные причины, по которым может произойти сбой Test-CsGroupExpansion.

  - Вы указали недопустимую учетную запись пользователя. Для проверки существования учетной записи пользователя можно выполнить следующую команду:
    
        Get-CsUser "sip:kenmyer@litwareinc.com"

  - Учетная запись пользователя верна, но в настоящее время учетная запись не включена для Lync Server. Чтобы убедиться в том, что учетная запись пользователя включена для Lync Server, выполните команду, подобную следующей:
    
        Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object Enabled
    
    Если для свойства Enabled задано значение false, это означает, что пользователь в настоящее время не поддерживает Lync Server.

  - Возможно, отключено расширение групп. Можно отключить развертывание групп. Если расширение группы было отключено, командлет Test-CsGroupExpansion завершится сбоем. Чтобы определить, включено ли расширение группы, выполните следующую команду:
    
        Get-CsWebServiceConfiguration | Select-Object Identity, EnableGroupExpansion

</div>

</div>

<span> </span>

</div>

</div>

</div>

