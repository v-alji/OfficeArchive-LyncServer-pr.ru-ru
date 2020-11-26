---
title: 'Lync Server 2013: тестирование push-уведомлений на Интеллектуальные телефоны'
description: 'Lync Server 2013: тестирование push-уведомлений на Интеллектуальные телефоны.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test push notifications to smart phones
ms:assetid: 8f5ca7d1-1ccb-4cb0-b417-730559e79b6e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn767948(v=OCS.15)
ms:contentKeyID: 63969626
ms.date: 03/15/2017
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4b92ef444a5331c9a673fd2db506631554e96eea
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441230"
---
# <a name="test-push-notifications-to-smart-phones-in-lync-server-2013"></a>Тестирование push-уведомлений на смартфоны в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2017-03-15_


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
<p>При запуске с помощью удаленного экземпляра Windows PowerShell пользователям должна быть назначена роль RBAC, имеющая разрешение на запуск командлета Test-CsMcxPushNotification. Чтобы просмотреть список всех ролей RBAC, которые могут использовать этот командлет, выполните в командной строке Windows PowerShell следующую команду:</p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsMcxPushNotification&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a>Описание

Служба push-уведомлений Apple и Служба push-уведомлений Майкрософт может отправлять уведомления о событиях, например о новых мгновенных сообщениях или голосовой почте на мобильных устройствах, таких как iPhone и телефоны Windows, даже если клиент Lync на этих устройствах в настоящее время приостановлен или работает в фоновом режиме. Служба push-уведомлений — это облачная служба, выполняемая на серверах Microsoft. Чтобы воспользоваться преимуществами push-уведомлений, вы должны иметь возможность подключения и проверки подлинности с помощью службы push-уведомлений. Командлет Test-CsMcxPushNotification позволяет администраторам убедиться, что запросы push-уведомлений могут маршрутизироваться через пограничный сервер в расчетную палату push-уведомлений.

</div>

<div>

## <a name="running-the-test"></a>Выполнение теста

Чтобы протестировать службу push-уведомлений, вызовите командлет Test-CsMcxPushNotification. Убедитесь, что вы указали полное доменное имя пограничного сервера:

    Test-CsMcxPushNotification -AccessEdgeFqdn "atl-edge-001.litwareinc.com"

Дополнительные сведения можно найти в разделе справки по командлету [Test-CsMcxPushNotification](https://docs.microsoft.com/powershell/module/skype/Test-CsMcxPushNotification) .

</div>

<div>

## <a name="determining-success-or-failure"></a>Определение успеха или сбоя

Если Test-CsMcxPushNotification успешное выполнение командлета, будет возвращено результат теста:

TargetFqdn: atl-cs-001.litwareinc.com

Результат: успех

Задержка: 00:00:00

Ошибки

Диагностик

Если Test-CsMcxPushNotification не удается подключиться к расчетной палате push-уведомлений, этот командлет обычно не возвращает результат теста "сбой". Вместо этого, как правило, команда завершается сбоем. Например:

Test-CsMcxPushNotification: ответ 504 (время ожидания сервера), полученный от сети, не прошел операцию. Дополнительные сведения приведены в разделе сведения об исключении.

В строке: 1 символ: 27

\+Test-CsMcxPushNotification \< \< \< \< AccessEdgeFqdn lyncedge.mydomain.com

\+ CategoryInfo: OperationStopped: (:) \[ Test-CsMcxPushNotification \] , FailureResponseException

\+ FullyQualifiedErrorId: WorkflowNotCompleted, Microsoft. RTC. Management. SyntheticTransactions. TestMcxPushNotificationCmdlet

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a>Причины, по которым может произойти сбой теста

Если происходит сбой службы push-уведомлений, которая обычно указывает на наличие проблем с подключением пограничного сервера или проблем с подключением к клирингового отсоединению push-уведомлений. Если при выполнении теста-CsMcxPushNotification возникли проблемы, необходимо убедиться, что пограничный сервер работает правильно. Один из способов сделать это — использовать командлет Test-CsAVEdgeConnectivity:

    $credential = Get-Credential "litwareinc\kenmyer"
    
    Test-CsAVEdgeConnectivity -TargetFqdn "atl-cs-001.litwareinc.com" -UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential

Эта проверка удостоверяет, что указанный пользователь может подключаться к пограничного сервера.

Если пограничный сервер работает правильно, это часто означает, что вы не можете подключиться к расчетной палате push-уведомлений. В свою очередь, обычно это означает, что вы неправильно настроили URI расчетной палаты или не обладаете DNS SRV-записью, указывающей на этот URL-адрес. Вы можете проверить, правильно ли задано значение универсального кода ресурса (sip:push@push.lync.com), выполнив следующую команду:

    Get-CsMcxConfiguration

Если для свойства PushNotificationProxyUri задано значение, отличное от sip:push@push.lync.com, то эту проблему можно устранить с помощью командлета Set-McxConfiguration. Например, эта команда правильно задает универсальный код ресурса (URI) для всей Организации.

    Get-CsMcxConfiguration | Set-CsMcxConfiguration -PushNotificationProxyUri "sip:push@push.lync.com"

Дополнительные сведения можно найти в разделе справки по командлету [Set-CsMcxConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsMcxConfiguration) .

Если универсальный код ресурса (URI) настроен правильно, необходимо убедиться в том, что у вас есть DNS SRV-запись, которая разрешается для вашего домена SIP и пограничного сервера. Дополнительные сведения о том, как настроить эти записи, можно найти в разделе справки требования к DNS для мобильных устройств. Обратите внимание, что следующее сообщение об ошибке обычно указывает на проблему с DNS-записями.

Ответ 504 (время ожидания сервера), полученный от сети, не прошел операцию. Дополнительные сведения приведены в разделе сведения об исключении.

Возможно также, что Test-CsMcxConfiguration завершится сбоем с сообщением об ошибке:

Test-CsMcxPushNotification: запрос push-уведомления отклонен.

В строке: 1 символ: 27

\+ Test-CsMcxPushNotification \<\<\<\<

\+ CategoryInfo: OperationStopped: (:) \[ Test-CsMcxPushNotification \] , SyntheticTransactionException

\+ FullyQualifiedErrorId: WorkflowNotCompleted, Microsoft. RTC. Management. SyntheticTransactions. TestMcxPushNotificationCmdlet

Сообщение "запрос push-уведомлений отвергнуто" обычно происходит, если включена фильтрация URL-адресов и вы блокируете префиксы http: и HTTPS:. Вы можете определить, какие префиксы блокируются, с помощью команды, подобной приведенной ниже:

```PowerShell 
 (Get-CsImFilterConfiguration -Identity Global).Prefixes
```

Если в результатах отображаются протоколы HTTP: или HTTPS, необходимо удалить их из списка блокируемых префиксов для использования push-уведомлений. Это можно сделать с помощью команд, сходных с приведенными ниже.

    Set-CsImFilterConfiguration -Identity site:Redmond -Prefixes @{remove="http:"}
    Set-CsImFilterConfiguration -Identity site:Redmond -Prefixes @{remove="https:"}

Дополнительные сведения можно найти в разделе справки по командлету [Set-CsImFilterConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsImFilterConfiguration).

</div>

</div>

<span> </span>

</div>

</div>

</div>

