---
title: 'Lync Server 2013: проверка политики расположения'
description: 'Lync Server 2013: проверка политики расположения.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing location policy
ms:assetid: 23d06fd3-31ee-4480-ba1e-d179a55b8b14
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn690127(v=OCS.15)
ms:contentKeyID: 63969591
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4efc7ac6f3beef875ce1496b19b875ff252b145b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398956"
---
# <a name="testing-location-policy-in-lync-server-2013"></a>Проверка политики расположения в Lync Server 2013

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
<p>При запуске с помощью удаленного экземпляра Windows PowerShell пользователям должна быть назначена роль RBAC, имеющая разрешение на запуск командлета Test-CsLocationPolicy. Чтобы просмотреть список всех ролей RBAC, которые могут использовать этот командлет, выполните в командной строке Windows PowerShell следующую команду:</p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsLocationPolicy&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a>Описание

Командлет Test-CsLocationPolicy удостоверяет, что политика расположения назначена пользователю. Политика Location используется для применения параметров, которые связаны с функциональностью E9-1-1 и адресом клиента. Политика расположения определяет, разрешено ли пользователю E9-1-1, и, если вы ответили "Да", каково поведение вызова экстренной помощи. Например, вы можете использовать политику расположения, чтобы определить, какой номер является вызовом экстренной помощи (911 в США), следует ли автоматически уведомлять корпоративную безопасность, а также как перенаправлять этот звонок.

Вы можете проверить политики расположения для пользователей или подсетей сети. Если вы пропустили тест для подсети (указав значение параметра подсети), командлет попытается разрешить политику расположения для этой подсети. Если подсеть не назначена ни одной политики расположения, будет извлекаться политика расположения для настроенного пользователя. Если политика подсети получена успешно, выходные данные будут содержать значение LocationPolicyTagID, которое начинается с подсети TagId. Если политика расположения для подсети не найдена, LocationPolicyTagID будет начинаться с User-TagId.

</div>

<div>

## <a name="running-the-test"></a>Выполнение теста

Командлет Test-CsLocationPolicy можно выполнить с помощью предварительно настроенной тестовой учетной записи (см. раздел Настройка тестовых учетных записей для выполнения тестов Lync Server) или учетной записи пользователя, который включен для Lync Server. Для выполнения этой проверки с помощью тестовой учетной записи нужно просто указать полное доменное имя для тестируемого пула Lync Server. Например:

    Test-CsLocationPolicy -TargetFqdn "atl-cs-001.litwareinc.com"

Чтобы выполнить эту проверку с использованием реальной учетной записи пользователя, необходимо сначала создать объект учетных данных Windows PowerShell, содержащий имя учетной записи и пароль. Затем необходимо добавить этот объект учетных данных и адрес SIP, назначенный учетной записи, при вызове Test-CsLocationPolicy:

    $credential = Get-Credential "litwareinc\kenmyer"
    Test-CsLocationPolicy -TargetFqdn "atl-cs-001.litwareinc.com"-UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential

Дополнительные сведения можно найти в справочной документации по командлету [Test-CsLocationPolicy](https://docs.microsoft.com/powershell/module/skype/Test-CsLocationPolicy) .

</div>

<div>

## <a name="determining-success-or-failure"></a>Определение успеха или сбоя

Если указанный пользователь имеет действующую политику расположения, вы получите вывод, как показано ниже, и свойство Result, помеченное как **успешно.**

EnhancedEmergencyServicesEnabled: true

LocationPolicyTagID: User-TagId

TargetFqdn: atl-cs-001.litwareinc.com

Результат: успех

Задержка: 00:00:06.8630376

Ошибки

Диагностик

Если для указанного пользователя не удается найти действующую политику расположения, результат будет отображаться как сбой, а дополнительные сведения будут записаны в свойствах Error и диагноз.

TargetFqdn: atl-cs-001.litwareinc.com

Результат: сбой

Задержка: 00:00:00

Ошибка: 404, не найдена

Диагностика: ErrorCode = 4005, Source = ATL-CS-001.litwareinc.com,

Reason = универсальный код ресурса (URI) назначения не включен для SIP либо не

Существует.

Microsoft. RTC. SignalR. DiagnosticHeader

В предыдущем выводе говорится, что тест завершился сбоем, так как указан недопустимый пользователь: учетная запись не существует или пользователь не включен для Lync Server. Вы можете проверить правильность учетной записи и определить, включена ли эта учетная запись для NM-OCS-14-3, выполнив следующую команду:

    Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object SipAddress, Enabled

Если Test-CsLocationPolicy не удается, возможно, потребуется повторно выполнить тест, на этот раз включая параметр подробно:

    Test-CsLocationPolicy -TargetFqdn "atl-cs-001.litwareinc.com" -Verbose

После включения подробного параметра Test-CsLocationPolicy будет возвращать пошаговые учетные записи для каждого действия, которое он пытался проверить. Например, этот вывод указывает на то, что серверу Lync Server не удалось войти в тестовый пользователь, возможно, из-за того, что был введен недопустимый пароль.

Отправка запроса на регистрацию:

Целевое полное доменное имя = atl-cs-011.litwareinc.com

SIP адрес пользователя = sip:kenmyer@litwareinc.com

Порт регистратора = 5061

Выбран тип проверки подлинности "IWA".

Регистрация в соответствии с SIP/ATL-CS-001. плана litwareinc. com

Действие "регистрация" завершено в течение "0,0601795" сек.

Исключение "вход был отклонен". Убедитесь в том, что используются правильные учетные данные, а учетная запись активна. произошла ошибка рабочего процесса.

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a>Причины, по которым может произойти сбой теста

Ниже приведены некоторые распространенные причины, по которым может произойти сбой Test-CsLocationPolicy.

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

