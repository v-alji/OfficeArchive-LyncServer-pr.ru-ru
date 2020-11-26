---
title: 'Lync Server 2013: Проверка КОММУТИРУЕМого телефонного звонка'
description: 'Lync Server 2013: Проверка КОММУТИРУЕМого телефонного звонка.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing PSTN phone call
ms:assetid: dc7d319d-a627-45b6-a978-6111901251e3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn690133(v=OCS.15)
ms:contentKeyID: 63969656
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b42ea6dd46145961a34386d704f8f44e9b7909ad
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439767"
---
# <a name="testing-pstn-phone-call-in-lync-server-2013"></a>Проверка телефонной связи PSTN в Lync Server 2013

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
<p>При запуске с помощью удаленного экземпляра Windows PowerShell пользователям должна быть назначена роль RBAC, имеющая разрешение на запуск командлета Test-CsRegistration. Чтобы просмотреть список всех ролей RBAC, которые могут использовать этот командлет, выполните в командной строке Windows PowerShell следующую команду:</p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsPstnOutboundCall&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a>Описание

Командлет Test-CsPstnOutboundCall проверяет способность пользователя звонить на номер телефона, находящийся в КТСОП. При запуске test-CsPstnOutboundCall командлет сначала пытается записать тестовый пользователь на сервер Lync Server. Если вход будет выполнен успешно, командлет попытается выполнить телефонный звонок через шлюз PSTN. Этот телефонный звонок будет выполняться с использованием абонентской группы, политики голосовой связи и других политик и параметров, назначенных тестовой учетной записи. При ответе на звонок командлет отправляет Многочастотные коды с несколькими частотами (DTMF) по сети для проверки подключения к носителю.

При проведении проверки Test-CsPstnOutboundCall вызовет фактический телефонный звонок: конечный телефон будет звонить, и для успешного завершения теста должен быть дан ответ. Этот звонок также должен завершиться администратором вручную.

</div>

<div>

## <a name="running-the-test"></a>Выполнение теста

Командлет Test-CsPstnOutboundCall можно выполнить с помощью предварительно настроенной тестовой учетной записи (см. раздел Настройка тестовых учетных записей для выполнения тестов Lync Server) или учетной записи пользователя, который включен для Lync Server. Для выполнения этой проверки с помощью тестовой учетной записи необходимо указать полное доменное имя тестируемого пула сервера Lync и телефонный номер PSTN. Например:

    Test-CsPstnOutboundCall -TargetFqdn "atl-cs-001.litwareinc.com" -TargetPstnPhoneNumber "+12065551219"

Чтобы выполнить эту проверку с использованием реальной учетной записи пользователя, необходимо сначала создать объект учетных данных Windows PowerShell, содержащий имя учетной записи и пароль. Затем необходимо добавить этот объект учетных данных и адрес SIP, назначенный учетной записи, при вызове Test-CsPstnOutboundCall:

    $credential = Get-Credential "litwareinc\kenmyer"
    Test-CsPstnOutboundCall -TargetFqdn "atl-cs-001.litwareinc.com" -TargetPstnPhoneNumber "+12065551219" -UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential

Дополнительные сведения можно найти в справочной документации по командлету [Test-CsPstnOutboundCall](https://docs.microsoft.com/powershell/module/skype/Test-CsPstnOutboundCall) .

</div>

<div>

## <a name="determining-success-or-failure"></a>Определение успеха или сбоя

Если заданный пользователь может позвонить, и при ответе на него будет получено сообщение о том, что свойство результата помечено как **успешное:**

TargetFqdn: atl-cs-001.litwareinc.com

Результат: успех

Задержка: 00:00:06.8630376

Ошибки

Диагностик

Если указанный пользователь не может позвонить или звонок не отвечает, результат будет показан как сбой, а дополнительные сведения будут записаны в свойствах Error и диагноз.

TargetFqdn: atl-cs-001.litwareinc.com

Результат: сбой

Задержка: 00:00:0987365

Ошибка: 403, запрещено

Диагностика: ErrorCode = 12001, Source = ATL-CS-001. плана litwareinc. com, Reason = User

Политика не содержит использование маршрутных номеров

В предыдущем выводе говорится, что тест завершился сбоем, так как политика голосовой связи, назначенная указанному пользователю, не содержит использование телефона. (Использование телефона применяет политики голосовой связи для голосовых маршрутов. Без политики голосовой связи и соответствующего голосового маршрута вы не можете звонить по протоколу PSTN.

Если Test-CsPstnOutboundCall не удается, возможно, потребуется повторно выполнить тест, на этот раз включая параметр подробно:

    Test-CsPstnOutboundCall -TargetFqdn "atl-cs-001.litwareinc.com" -TargetPstnPhoneNumber "+12065551219" -Verbose

После включения подробной информации Test-CsPstnOutboundCall будет возвращать пошаговые учетные записи каждого действия, которое он пытался войти на сервер Lync Server. Например, эти выходные данные указывают на то, что неполадки в сети не препятствуют подключению к КТСОП.

Установка голосового видеозвонка на "SIP: + 12065551219@litwareinc. com; user = Phone".

В сети получено исключение "404 (не найдено), и операция завершилась сбоем.

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a>Причины, по которым может произойти сбой теста

Ниже приведены некоторые распространенные причины, по которым может произойти сбой Test-CsPstnOutboundCall.

  - Вы указали недопустимую учетную запись пользователя. Для проверки существования учетной записи пользователя можно выполнить следующую команду:
    
        Get-CsUser "sip:kenmyer@litwareinc.com"

  - Учетная запись пользователя верна, но в настоящее время учетная запись не включена для Lync Server. Чтобы убедиться в том, что учетная запись пользователя включена для Lync Server, выполните команду, подобную следующей:
    
        Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object Enabled
    
    Если для свойства Enabled задано значение false, это означает, что пользователь в настоящее время не поддерживает Lync Server.

  - Политика голосовой связи, назначенная указанному пользователю, не может использоваться в качестве использования КТСОП. Вы можете определить политику голосовой связи, назначенную для пользователя, с помощью следующей команды:
    
        Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object VoicePolicy
    
    Затем вы можете определить использование PSTN (если таковые есть), назначенные этой политике, используя следующую команду, которая извлекает сведения о политике голосовой связи для пользователя RedmondVoicePolicy:
    
        Get-CsVoicePolicy -Identity "RedmondVoicePolicy"

</div>

</div>

<span> </span>

</div>

</div>

</div>

