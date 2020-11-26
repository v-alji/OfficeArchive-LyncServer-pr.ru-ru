---
title: 'Lync Server 2013: Проверка службы реплики'
description: 'Lync Server 2013: Проверка службы реплики.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing the replica service
ms:assetid: 4ff2cc91-0036-4c5a-9792-7bf43d8ce18d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn727303(v=OCS.15)
ms:contentKeyID: 63969600
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a61751b95115da3d6519f20f52262b7159ffcbfe
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440978"
---
# <a name="testing-the-replica-service-in-lync-server-2013"></a>Проверка службы реплики в Lync Server 2013

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
<p>При запуске с помощью удаленного экземпляра Windows PowerShell пользователям должна быть назначена роль RBAC, имеющая разрешение на запуск командлета <strong>Test-CsReplica</strong> . Чтобы просмотреть список всех ролей RBAC, которые могут использовать этот командлет, выполните в командной строке Windows PowerShell следующую команду:</p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsReplica&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a>Описание

Командлет **Test-CsReplica** проверяет, запущена ли служба реплики Lync Server 2013 на локальном компьютере. Командлет **Test-CsReplica** выполняет такие задачи, как:

  - Проверка состояния агента Replicator и службы агента централизованного ведения журнала

  - Проверка того, что нужные порты были открыты в брандмауэре Windows

  - Убедитесь в наличии необходимых групп безопасности Active Directory и локального компьютера.

Обратите внимание, что этот командлет должен выполняться локально. Это значит, что она должна быть запущена на том же компьютере, на котором запущена служба реплики. Для запуска командлета **Test-CsReplica** с удаленным сервером не существует параметров.

</div>

<div>

## <a name="running-the-test"></a>Выполнение теста

Команда, показанная в примере 1, проверяет службу реплики Lync Server 2013 на локальном компьютере. В этом примере параметр Verbose используется для того, чтобы гарантировать, что сведения о тесте — в том числе в конечном итоге отказа или успешности теста, а также расположение отчета, созданного тестом — отображается на экране.

    Test-CsReplica -Verbose

Пример 2 — это вариант команды, показанный в примере 1. В этом случае параметр отчета включает в себя путь к папке и имя для отчета, созданного с помощью теста. Если не указать путь к отчету, ему будет автоматически сгенерировано такое имя, как:

C: \\ Пользователи \\ администратор. плана litwareinc \\ AppData \\ Local \\ temp \\ 1 \\Test-Cs-Replica-3db40ee0-4b5d-4f58-8d3d-b1e61253129e.html

    Test-CsReplica -Verbose -Report C:\Logs\ReplicaTest.html

</div>

<div>

## <a name="determining-success-or-failure"></a>Определение успеха или сбоя

Вставить текст раздела здесь.

ПОДРОБНЫй: создание нового файла журнала "C: \\ Пользователи \\ тестирование \\ \\ локальной \\ папке AppData \\Test-CsReplica-3cb066b3-dd23-411a-8932-99f01c0f940c.xml".

ПОДРОБНЫй: создание нового файла журнала "C: \\ Пользователи \\ тестирование \\ \\ локальной \\ папке AppData \\Test-CsReplica-3cb066b3-dd23-411a-8932-99f01c0f940c.xml".

ПОДРОБНОе сообщение: обработка "Test-CsReplica" успешно завершена.

ПОДРОБНЫй: подробные результаты можно найти на странице "C: \\ Пользователи \\ тестирование" \\ AppData \\ Local \\ temp \\Test-CsReplica-3cb066b3-dd23-411a-8932-99f01c0f940c.xml ".

ПОДРОБНЫй: создание нового файла журнала

"C: \\ Пользователи \\ проверяют \\ \\ Каталог AppData Local \\ temp \\ 2 \\ Test-CsReplica-29fddb35-f56e-4e3c-8f4c-e

d3bd0e4a083.xml ".

ПОДРОБНЫй: создание нового файла журнала

"C: \\ Пользователи \\ проверяют \\ \\ Каталог AppData Local \\ temp \\ 2 \\ Test-CsReplica-29fddb35-f56e-4e3c-8f4c-e

d3bd0e4a083.html ".

Предупреждение: Test-CsReplica не удалось.

Предупреждение: подробные результаты можно найти по адресу

"C: \\ Пользователи \\ проверяют \\ \\ Каталог AppData Local \\ temp \\ 2 \\ Test-CsReplica-29fddb35-f56e-4e3c-8f4c-e

d3bd0e4a083.html ".

Test-CsReplica: не удалось выполнить команду: запрошенный доступ к реестру не

использоваться.

В строке: 1 символ: 1

\+ Test-CsReplica — подробный

\+ ~~~~~~~~~~~~~~~~~~~~~~~

\+ CategoryInfo: InvalidOperation: (:) \[ Test-CsReplica \] , безопасность

Ошибка

\+ FullyQualifiedErrorId: ProcessingFailed, Microsoft. RTC. Management. deploy

чения. TestReplicaCmdlet

PS C: \\ \\ Проверка пользователей\>

PS C: \\ Пользователи \\ тестирование \> Test-CsUcwaConference-TargetFqdn "LyncTest. SelfHost. Corp. M

icrosoft.com "

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

Ниже приведены некоторые распространенные причины, по которым может произойти сбой **Test-CsReplica** :

  - Возможно, возникла проблема с агентом тиражирования и службами агента централизованного ведения журнала

  - Возможно, требуемые порты не открыты в брандмауэре Windows

  - Возможно, не существует необходимая группа безопасности Active Directory и локального компьютера

</div>

</div>

<span> </span>

</div>

</div>

</div>

