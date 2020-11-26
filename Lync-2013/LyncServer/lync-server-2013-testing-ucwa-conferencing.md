---
title: 'Lync Server 2013: тестирование конференц-связи по UCWA'
description: 'Lync Server 2013: тестирование конференц-связи UCWA.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing UCWA conferencing
ms:assetid: 62b3866a-0759-4b1f-99ec-5a68d6a74f00
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn727306(v=OCS.15)
ms:contentKeyID: 63969610
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 37f88a683abb67d55211422fc4dcf45fc1d5c966
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439739"
---
# <a name="testing-ucwa-conferencing-in-lync-server-2013"></a>Проверка конференц-связи UCWA в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2014-11-03_


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
<p>При запуске с помощью удаленного экземпляра Windows PowerShell пользователям должна быть назначена роль RBAC, имеющая разрешение на запуск командлета <strong>Test-CsUcwaConference</strong> . Чтобы просмотреть список всех ролей RBAC, которые могут использовать этот командлет, выполните в командной строке Windows PowerShell следующую команду:</p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsUcwaConference&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a>Описание

Командлет **Test-CsUcwaConference** удостоверяется в том, что с помощью веб-интерфейса единой системы обмена сообщениями (UCWA) пользователь может запланировать, присоединиться к Конференции и провести сетевую конференцию. Для этого командлет использует службу веб-билета Lync Server для проверки подлинности двух тестовых пользователей и их регистрации в Lync Server. Затем командлет начнет конференцию с использованием учетных данных организатора и приглашает участника присоединиться к собранию. После присоединения к собранию командлет **Test-CsUcwaConference** удостоверяет, что пользователи могут выполнять такие действия, как обмен мгновенными сообщениями и объединением, а затем отключает конференцию и отменяет регистрацию двух тестовых пользователей. Запланированная Конференция также будет удалена после завершения теста.

Командлет **Test-CsUcwaConference** также можно использовать, чтобы определить, могут ли анонимные пользователи присоединиться к онлайн-конференциям.

Обратите внимание, что командлет **Test-CsUcwaConference** не следует запускать для пула Microsoft Lync Server 2010, если UCWA не установлен в этом пуле. Если UCWA не установлен, вызов командлета **Test-CsUcwaConference** завершится сбоем.

</div>

<div>

## <a name="running-the-test"></a>Выполнение теста

Команда, показанная в примере 1, проверяет, может ли пользователь, который входит в состав Конференции UCWA в atl-cs-001.litwareinc.com пула, мог принимать участие в паре тестов. Обратите внимание, что эта команда завершится сбоем, если вы не предatl-CS-001.litwareinc.com пару пользователей теста конфигурации мониторинга работоспособности для.

    Test-CsUcwaConference -TargetFqdn "atl-cs-001.litwareinc.com"

Команды, показанные в примере 2, проверяют возможности пары пользователей (плана litwareinc \\ почтового и плана litwareinc \\ kenmyer) для участия в UCWA Конференции. Для этого в первой команде примера используется командлет Get-Credential, чтобы создать объект учетных данных интерфейса командной строки Windows PowerShell, содержащий имя и пароль пользователя почтового Вронский. (Поскольку имя для входа, плана litwareinc \\ почтового, было включено в качестве параметра, в диалоговом окне Запрос учетных данных Windows PowerShell требуется, чтобы администратор введет пароль для учетной записи почтового Вронский.) Результирующий объект учетных данных сохраняется в переменной с именем $cred 1. Вторая команда — это то же самое, что возвращает объект учетной записи Кен Myer.

Если у вас есть два объекта учетных данных, третья команда в примере определяет, могут ли два пользователя принимать участие в конференц-связи UCWA. Для выполнения этой задачи вызывается командлет **Test-CsUcwaConference** , вместе со следующими параметрами: TargetFqdn (полное доменное имя пула регистраторов). OrganizerSipAddress (SIP-адрес организатора собрания); OrganizerCredential (объект Windows PowerShell, который включает в себя учетные данные для этого пользователя); ParticipantSipAddress (SIP-адрес для другого тестового пользователя); и ParticipantCredential (объект интерфейса командной строки Windows PowerShell, который включает в себя учетные данные для другого пользователя).

    $cred1 = Get-Credential "litwareinc\pilar"
    $cred2 = Get-Credential "litwareinc\kenmyer"
    Test-CsUcwaConference -TargetFqdn atl-cs-001.litwareinc.com -OrganizerSipAddress "sip:pilar@litwareinc.com" -OrganizerCredential $cred1 -ParticipantSipAddress "sip:kenmyer@litwareinc.com" -ParticipantCredential $cred2

</div>

<div>

## <a name="determining-success-or-failure"></a>Определение успеха или сбоя

Если вы правильно настраиваете Конференц-связь, вы получите вывод примерно так, чтобы свойство Result пометило **"успешно".**

Целевое полное доменное имя: atl-cs-001.litwareinc.com

Конечный URI: https://LyncTest-SE. LyncTest. SelfHost. Corp.

Microsoft.com:443/CertProv/CertProvisiongService.svc

Результат: успех

Задержка: 00:00:14.9862716

Сообщение об ошибке:

Диагностик

Если указанные пользователи не могут использовать конференц-связь, результат будет отображаться как **сбой**, а дополнительные сведения будут записаны в свойствах Error и диагноз.

Предупреждение: не удалось прочитать номер порта регистратора для заданного полного имени

доменное имя (FQDN). С помощью номера порта регистратора по умолчанию. Ошибка

System. InvalidOperationException: в топологии не обнаружены подходящие кластеры.

скорость

Microsoft. RTC. Management. SyntheticTransactions. SipSyntheticTransaction. TryRetri

eveRegistrarPortFromTopology (Int32& registrarPortNumber)

Test-CsUcwaConference: нет тестового пользователя, назначенного для

\[LyncTest.SelfHost.Corp.Microsoft.com \] . Проверка конфигурации тестового пользователя.

В строке: 1 символ: 1

\+ Test-CsUcwaConference TargetFqdn "LyncTest.SelfHost.Corp.Microsoft.com"

\+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

\+ CategoryInfo: ResourceUnavailable: (:) \[ Test-CsUcwaConference\]

, InvalidOperationException

\+ FullyQualifiedErrorId: NotFoundTestUsers, Microsoft. RTC. Management. синтезатор

eticTransactions.TestUcwaConferenceCmdlet

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a>Причины, по которым может произойти сбой теста

Ниже приведены некоторые распространенные причины, по которым может произойти сбой **Test-CsUcwaConference** :

  - Предоставлено неправильное значение параметра. Если используется, необязательные параметры необходимо настроить правильно, или тест завершится сбоем. Повторите выполнение команды без дополнительных параметров и проверьте, выполняется ли это успешно.

  - Возможность проведения Конференции зависит от политики конференц-связи, назначенной пользователю, который организовал конференцию (в случае командлета **Test — CsUcwaConference** , который является отправителем). Если организатор не может включать мероприятия для совместной работы на своем собрании (например, если у его политики Конференции задано значение false), командлет **Test-CsUcwaConference** завершится сбоем.

  - Эта команда завершается сбоем, если граничный сервер неправильно настроен или еще не развернут.

</div>

<div>

## <a name="see-also"></a>См. также


[Test-CsASConference](https://docs.microsoft.com/powershell/module/skype/Test-CsASConference)  
[Test-CsDataConference](https://docs.microsoft.com/powershell/module/skype/Test-CsDataConference)  
[Test-CsAVConference](https://docs.microsoft.com/powershell/module/skype/Test-CsAVConference)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

