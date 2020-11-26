---
title: 'Lync Server 2013: Проверка конфигурации голосовой связи'
description: 'Lync Server 2013: Проверка конфигурации голосовой связи.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test voice configuration
ms:assetid: 574794a3-cb30-4762-bb62-3a68574f05e9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn725208(v=OCS.15)
ms:contentKeyID: 63969605
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4cc05286e5f534b4d469ef561d9ce009367e15be
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444184"
---
# <a name="test-voice-configuration-in-lync-server-2013"></a>Проверка конфигурации голосовой связи в Lync Server 2013

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
<p>При запуске с помощью удаленного экземпляра Windows PowerShell пользователям должна быть назначена роль RBAC, имеющая разрешение на запуск командлета Test-CsVoiceTestConfiguration. Чтобы просмотреть список всех ролей RBAC, которые могут использовать этот командлет, выполните в командной строке Windows PowerShell следующую команду:</p>
<p><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsVoiceTestConfiguration&quot;}</code></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a>Описание

Lync Server включает несколько командлетов Windows PowerShell (например, Test-CsVoiceRoute и Test-CsVoicePolicy, Test-CsTrunkConfiguration), которые позволяют убедиться в том, что индивидуальные части инфраструктуры корпоративной голосовой связи – маршруты голосовой связи, политики голосовой связи, магистральные линии SIP — работают должным образом.

Несмотря на то, что в корпоративной голосовой связи все индивидуальные компоненты работают, вы можете использовать допустимый голосовой маршрут, действительную голосовую политику и действительную магистраль SIP, но при этом пользователи не смогут совершать и принимать телефонные звонки. По этой причине Lync Server также предоставляет возможность создавать конфигурации тестовых тестов. Конфигурации тестовых тестов — это распространенные сценарии для корпоративных клиентов: вы можете указать такие параметры, как голосовая связь, политика голосовой связи и абонентская группа, а затем убедиться, что эти индивидуальные элементы смогут работать вместе для предоставления услуг телефонной связи. Кроме того, вы можете проверить свои ожидания в указанном сценарии. Например, предположим, что сочетание абонентов и политик голосовой связи "B" привело бы к переадресации звонков по голосовой маршруту C. Вы можете ввести голосовой маршрут C в качестве ExpectedRoute. Если при выполнении теста маршрут "C" не установлен, проверка будет помечена как невыполненная.

</div>

<div>

## <a name="running-the-test"></a>Выполнение теста

Перед тестированием коллекций голосовой конфигурации с помощью Windows PowerShell необходимо сначала использовать командлет Get-CsVoiceTestConfiguration, чтобы получить экземпляр этих параметров конфигурации. Затем этот экземпляр должен быть передан в тест-CsVoiceTestConfiguration. Например:

`Get-CsVoiceTestConfiguration -Identity "RedmondVoiceTestConfiguration" | Test-CsVoiceTestConfiguration`

Для одновременной проверки всех параметров конфигурации голосового теста используйте следующую команду:

`Get-CsVoiceTestConfiguration | Test-CsVoiceTestConfiguration`

Дополнительные сведения можно найти в справочной документации по командлету Test-CsVoiceTestConfiguration.

</div>

<div>

## <a name="determining-success-or-failure"></a>Определение успеха или сбоя

Командлет Test-CsVoiceTestConfiguration сообщает об ошибке теста или его успешности, а также предоставляет дополнительные сведения о каждом успешном прохождении теста, такие как правила трансляции, Голосовые маршруты и использование PSTN, используемое для выполнения задачи.

Результат: успех

TranslatedNumber: + 15551234

MatchingRule: описание =; Шаблон = ^ ( \\ d {4} ) $; Преобразование = + 1 \\ d; Name = Test; IsInternalExtension = false

FirstMatchingRoute: сайт: Redmond

MatchingUsage: local

Если тест не удалось выполнить, результат будет указан как ошибка.

Результат: Failed

TranslatedNumber:   

FirstMatchingRoute:

MatchingUsage:      

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a>Причины, по которым может произойти сбой теста

Поскольку тестирование конфигурации для проверки правописания проверяет несколько различных элементов, в том числе политики голосовой связи, абонентские группы, маршруты голосовой почты и т. д., это может привести к неудачному тесту. Если тест завершается сбоем, первым шагом необходимо проверить параметры конфигурации с помощью командлета Get-CsVoiceTestConfiguration:

`Get-CsVoiceTestConfiguration -Identity "RedmondVoiceTestConfiguration"`

Если параметры настроены правильно, повторно выполните тест, включив параметр Verbose.

`Get-CsVoiceTestConfiguration -Identity "RedmondVoiceTestConfiguration" | Test-CsVoiceTestConfiguration`

Параметр подробных данных предоставит пошаговые инструкции для каждого действия, выполненного Test-CsVoiceTestConfiguration, как показано в следующем примере:

ПОДРОБНЫй: Загрузка абонентской группы: "Global"

ПОДРОБНЫй: Загрузка политики голосовой связи: "RedmondDialPlan"

Эта пошаговая учетная запись может быть полезна в том случае, если тест действительно завершился сбоем. В противном случае вы можете использовать другие командлеты Windows PowerShell (например, Test-CsVoicePolicy) и methodically Begin для проверки отдельных компонентов, которые включены в параметры конфигурации голосового теста.

Кроме того, обратите внимание на то, что тест может перенаправлять вызов, но все еще не помечается как сбой. Это может произойти, если вы ввели значения для ExpectedRoute, ExpectedTranslatedNumber и ExpectedUsage, и любые из этих ожиданий не будут удовлетворены. Например, предположим, что вы ввели голосовую переадресацию в качестве ожидаемого голоса, но проверка завершит звонок с помощью голосового маршрута г. В этом случае тест будет помечен как сбой, так как ожидаемый маршрут голосовой связи не использовался. Если тест завершается сбоем, вы можете удалить значения для ExpectedRoute, ExpectedTranslatedNumber и ExpectedUsage, а затем повторно выполнить тест. Это поможет вам определить, завершился ли сбой из-за того, что не удалось выполнить звонок или вы ожидаете одного и фактического получения другого.

</div>

<div>

## <a name="see-also"></a>См. также


[Test-CsVoiceTestConfiguration](https://docs.microsoft.com/powershell/module/skype/Test-CsVoiceTestConfiguration)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

