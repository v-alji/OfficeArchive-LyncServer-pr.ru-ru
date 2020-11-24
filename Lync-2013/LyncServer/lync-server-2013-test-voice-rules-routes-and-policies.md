---
title: 'Lync Server 2013: Проверка правил голосовой связи, маршрутов и политик'
description: 'Lync Server 2013: проверьте правила голосовой связи, маршруты и политики.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test voice rules, routes, and policies
ms:assetid: ebb9c3fa-6950-4311-87ca-e1ecd9280a43
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn725213(v=OCS.15)
ms:contentKeyID: 63969661
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: cf205ac2585298dfc5347d93e382e8bbda9f3ff4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398062"
---
# <a name="test-voice-rules-routes-and-policies-in-lync-server-2013"></a>Проверка правил, маршрутов и политик голосовой связи в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2014-05-20_


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
<p>При запуске с помощью удаленного экземпляра Windows PowerShell пользователям должна быть назначена роль RBAC, имеющая разрешение на запуск командлета Test-CsVoiceUser. Чтобы просмотреть список всех ролей RBAC, которые могут использовать этот командлет, выполните в командной строке Windows PowerShell следующую команду:</p>
<p><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsVoiceUser&quot;}</code></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a>Описание

Когда пользователь выполняет телефонный звонок, маршрут, по которому выполняется звонок, зависит от политик и абонентских тарифов, назначенных этому пользователю. Если у пользователя есть SIP-адрес и номер телефона, командлет Test-CsVoiceUser проверяет, может ли пользователь выполнить Звонок на этот номер. Если проверка выполнена успешно, Test-CsVoiceUser возвращает следующее:

  - Число преобразовано в формат E. 164 (в соответствии с абонентской панелью пользователя).

  - Правило нормализации, которое предоставляет этот перевод

  - Используемый маршрут голоса (на основе приоритета маршрута);

  - Использование телефона, связанного с политикой голосовой связи пользователя, с голосовым маршрутом.

Test-CsVoiceUser позволяет определить, нужно ли перенаправлять и перевести конкретный номер телефона, и это поможет устранить проблемы, связанные с вызовами, которые могут возникнуть у отдельных пользователей.

</div>

<div>

## <a name="running-the-test"></a>Выполнение теста

При запуске командлета Test-CsVoiceUser необходимо указать два фрагмента данных: номер набора номера (DialedNumber) и идентификация проверяемой учетной записи пользователя. Например, эта команда проверяет возможность пользователя, у которого есть SIP-адрес sip:kenmyer@litwareinc.com, звонить на номер телефона + 1206555-1219:

`Test-CsVoiceUser -DialedNumber "12065551219" -SipUri "sip:kenmyer@litwareinc.com"`

Номер телефона должен быть отформатирован так, как вы планируете набрать его. Например, если пользователи, как правило, не набирает номер 1 перед тем, как звонить по междугородней связи, следует использовать следующий формат:

`-DialedNumber "2065551219"`

Разумеется, в этом случае тест завершится ошибкой, если у вас нет правила нормализации, позволяющего правильно перевести число 2065551219 в формат телефона E. 164, который используется в Lync Server. Дополнительные сведения можно найти в разделе справки New-CsVoiceNormalizationRule командлет.

Если вы хотите выполнить этот же тест для каждой учетной записи пользователя, вы можете использовать команду, подобную следующей:

`Get-CsUser | ForEach-Object {$_.DisplayName; Test-CsVoiceUser -DialedNumber "+12065551219" -SipUri $_.SipAddress} | Format-List`

Дополнительные сведения можно найти в справочной документации по командлету Test-CsVoiceUser.

</div>

<div>

## <a name="determining-success-or-failure"></a>Определение успеха или сбоя

Если проверка выполнена успешно (то есть, если пользователь может выполнить телефонный звонок на указанный номер), на выходе будут показаны такие данные, как переведенный номер телефона, а также соответствующее правило нормализации и голосовой маршрут.

TranslatedNumber MatchingRule FirstMatchingRoute MatchingUsage

\----------------    ------------    ------------------    -------------

\+12065551219 Descripti...    Локальный LocalRoute

Из-за ограничений на экран Windows PowerShell по крайней мере некоторые возвращенные сведения (особенно важно, полное описание соответствующего правила нормализации) могут не отображаться на экране. Если вы заинтересованы в успешном или неуспешном выполнении теста, это может быть неважно. Если вы хотите просмотреть полные сведения о возвращенных данных, переводите выходные данные в командлет Format-List при выполнении теста.

`Test-CsVoiceUser -DialedNumber "+12065551219" -SipUri "sip:kenmyer@litwareinc.com" -Verbose | Format-List`

Это приведет к отображению выходных данных в более удобном формате для чтения:

TranslatedNumber: + 12065551219

MatchingRule: описание =; Шаблон = ^ ( \\ d {11} ) $; Перевод = + $1;

Name = prefix ALL; IsInternalExtension = false

FirsMatchingRoute : LocalRoute

MatchingUsage: local

В случае сбоя теста Test-CsVoiceUser будет возвращать пустой набор значений свойств.

TranslatedNumber MatchingRule FirstMatchingRoute MatchingUsage

\---------------- ------------ ------------------ -------------

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a>Причины, по которым может произойти сбой теста

Существует несколько причин, по которым может произойти сбой командлета Test-CsVoiceUser: возможно, правило нормализации, которое может перевести указанный номер телефона, не существует. Возможно, возникли проблемы с голосовым маршрутом. Возможно, у вас возникла ошибка конфигурации для абонентской группы, назначенной пользователю. По этой причине при запуске командлета Test-CsVoiceUser может потребоваться включить параметр Verbose.

`Test-CsVoiceUser -DialedNumber "+12065551219" -SipUri "sip:kenmyer@litwareinc.com" -Verbose`

Когда вы включаете подробный командлет, Test-CsVoiceUser выдает подробные сведения о всех действиях, выполняемых при проведении проверок. Например, вы можете увидеть шаги, аналогичные указанным ниже. 

VERBOSE: Поиск пользователей с удостоверением "sip:kenmyer@litwareinc.com"

VERBOSE: Загрузка абонентской группы: "RedmondDialPlan"

Дополнительные сведения можно найти в разделе действия, которые можно выполнить для выявления причины сбоя. Например, подробный вывод показывает, что тестируемому пользователю назначена абонентская группа RedmondDialPlan. Если тест завершился сбоем, следующим логическим шагом будет проверка того, что RedmondDialPlan может перевести предоставленный телефонный номер.

</div>

<div>

## <a name="see-also"></a>См. также


[Test-CsVoiceUser](https://docs.microsoft.com/powershell/module/skype/Test-CsVoiceUser)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

