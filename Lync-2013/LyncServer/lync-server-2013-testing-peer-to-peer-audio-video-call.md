---
title: 'Lync Server 2013: Проверка одноранговых аудио-и видеозвонков'
description: 'Lync Server 2013: Проверка одноранговой голосовой и видеосвязи в одноранговых режимах.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing peer to peer audio/video call
ms:assetid: 95eb3693-b866-4652-bc45-9b75fdb40b49
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn743835(v=OCS.15)
ms:contentKeyID: 63969627
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 03bab69d926a99c091a510ce64b78dbf505d4cbc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439816"
---
# <a name="testing-peer-to-peer-audiovideo-call-in-lync-server-2013"></a>Проверка одноранговых аудио-и видеозвонков в Lync Server 2013

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
<p>При запуске с помощью удаленного экземпляра Windows PowerShell пользователям должна быть назначена роль RBAC, имеющая разрешение на запуск командлета Test-CsP2PAV. Чтобы просмотреть список всех ролей RBAC, которые могут использовать этот командлет, выполните в командной строке Windows PowerShell следующую команду:</p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsP2PAV&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a>Описание

Test-CsP2PAV используется, чтобы определить, могут ли пользователи, входящие в одноранговую беседу, использовать пару тестовых пользователей. Чтобы протестировать этот сценарий, командлет запускается путем записи двух пользователей на сервер Lync Server. Предполагается, что два входа выполняются успешно, первый пользователь затем приглашает второго пользователя присоединиться к вызову A/V. Второй пользователь принимает звонок, проверяет соединение между двумя пользователями, после чего звонок завершается, и тестовые пользователи вышли из системы.

Test-CsP2PAV на самом деле вызов функции A/V не выполняется. Данные мультимедиа не передаются между тестовыми пользователями. Вместо этого командлет проверяет, могут ли быть выполнены соответствующие подключения, и что эти пользователи могут выполнить такой вызов.

Дополнительные сведения можно найти в справочной документации по командлету [Test-CsP2PAV](https://docs.microsoft.com/powershell/module/skype/Test-CsP2PAV) .

</div>

<div>

## <a name="running-the-test"></a>Выполнение теста

Командлет Test-CsP2PAV можно выполнить с помощью пары предварительно настроенных тестовых учетных записей (см. раздел Настройка тестовых учетных записей для выполнения тестов Lync Server) или учетные записи любых двух пользователей, которые включены в Lync Server. Для выполнения этой проверки с помощью тестовых учетных записей нужно просто указать полное доменное имя для тестируемого пула Lync Server. Например:

    Test-CsP2PAV -TargetFqdn "atl-cs-001.litwareinc.com"

Для выполнения этой проверки с использованием фактических учетных записей пользователей необходимо создать два объекта учетных данных Lync Server (объекты, содержащие имя и пароль учетной записи) для каждой учетной записи. После вызова Test-CsP2PAV вы должны добавить эти объекты учетных данных и адреса SIP для двух учетных записей.

    $credential1 = Get-Credential "litwareinc\kenmyer"
    $credential2 = Get-Credential "litwareinc\davidlongmire"
    Test-CsP2PAV -TargetFqdn "atl-cs-001.litwareinc.com" -SenderSipAddress "sip:kenmyer@litwareinc.com" -SenderCredential $credential1 -ReceiverSipAddress "sip:davidlongmire@litwareinc.com" -ReceiverCredential $credential2

</div>

<div>

## <a name="determining-success-or-failure"></a>Определение успеха или сбоя

Если два тестовых пользователя могут выполнить одноранговый вызов A/V, вы получите вывод примерно так, чтобы свойство Result пометило **"успешно".**

TargetFqdn: atl-cs-001.litwareinc.com

Результат: успех

Задержка: 00:00:06.8630376

Ошибки

Диагностик

Если тестовые пользователи не могут завершить звонок, результат будет показан как сбой, а дополнительные сведения будут записаны в свойствах Error и диагноз.

TargetFqdn: atl-cs-001.litwareinc.com

Результат: сбой

Задержка: 00:00:00

Ошибка: 480, временно недоступна

Диагностика: ErrorCode = 15030, Source = ATL-CS-001. плана litwareinc. com, Reason = Failed

чтобы перенаправить на сервер Exchange Server

Microsoft. RTC. SignalR. DiagnosticHeader

Например, в предыдущем выводе говорится о том, что тест завершился сбоем, так как не удалось связаться с сервером Microsoft Exchange Server. Это сообщение об ошибке обычно указывает на проблему с настройкой единой системы обмена сообщениями Exchange.

Если Test-CsP2PAV не удается, возможно, потребуется повторно выполнить тест, на этот раз включая параметр подробно:

Test-CsP2PAV TargetFqdn "atl-cs-001.litwareinc.com" — подробный

После включения подробной информации Test-CsP2PAV будет возвращать пошаговые инструкции по выполнению всех действий, выполняемых указанным пользователем при входе на сервер Lync Server. Например, предположим, что тест завершился со следующей диагностикой.

ErrorCode = 6003, Source = ATL-CS-001. плана litwareinc. com, причина = не поддерживается запрос диалогового окна

Если вы снова запустите Test-CsP2PAV и включите параметр Verbose, вы получите вывод примерно так:

ПОДРОБНЫЕ сведения: начато действие "регистрация".

Отправка запроса на регистрацию:

Целевое полное доменное имя = atl-cs-011.litwareinc.com

SIP адрес пользователя = sip:kenmyer@litwareinc.com

Порт регистратора = 5062.

Выбран тип проверки подлинности "IWA".

Исключение "не удалось зарегистрировать конечную точку". Ознакомьтесь с ErrorCode по конкретной причине. произошла ошибка во время выполнения рабочего процесса Microsoft. RTC. SyntheticTransactions. Workflows. STP2PAVWorkflow.

Несмотря на то, что в результате проверки результатов может быть непросто, вы увидите, что указан неверный порт регистратора (порт 5062). В свою очередь, это привело к сбою теста.

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a>Причины, по которым может произойти сбой теста

Ниже приведены некоторые распространенные причины, по которым может произойти сбой Test-CsP2PAV.

  - Указана недействительная учетная запись пользователя. Для проверки существования учетной записи пользователя можно выполнить следующую команду:
    
    Get-CsUser "sip:kenmyer@litwareinc.com"

  - Учетная запись пользователя верна, но в настоящее время учетная запись не включена для Lync Server. Чтобы убедиться в том, что учетная запись пользователя включена для Lync Server, выполните команду, подобную следующей:
    
        Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object Enabled
    
    Если для свойства Enabled задано значение false, это означает, что пользователь в настоящее время не поддерживает Lync Server.

</div>

</div>

<span> </span>

</div>

</div>

</div>

