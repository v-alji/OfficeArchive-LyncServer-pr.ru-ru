---
title: 'Lync Server 2013: Проверка служб Lync Server'
description: 'Lync Server 2013: Проверка служб Lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing Lync Server services
ms:assetid: b564b450-a746-4ec9-aabb-e076309ccd5f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn689119(v=OCS.15)
ms:contentKeyID: 63969644
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f04cf5e0c098c671b6fb126d4607f3cdba107712
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398935"
---
# <a name="testing-lync-server-services-in-lync-server-2013"></a>Тестирование служб Lync Server в Lync Server 2013

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
<p>При запуске с помощью удаленного экземпляра Windows PowerShell пользователям должна быть назначена роль RBAC, имеющая разрешение на запуск командлета Test-CsComputer. Чтобы просмотреть список всех ролей RBAC, которые могут использовать этот командлет, выполните в командной строке Windows PowerShell следующую команду:</p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsComputer&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a>Описание

Test-CsComputer проверяет состояние всех служб Lync Server 2013, запущенных на локальном компьютере. (Test-CsComputer можно выполнять только локально, и его невозможно запустить из удаленного экземпляра Windows PowerShell.) Командлет также проверяет, открыты ли на компьютере соответствующие порты брандмауэра, и определяет, были ли группы Active Directory, созданные при установке сервера Lync Server 2013, добавлены в соответствующие локальные группы. Например, Test-CsComputer будет проверять, добавлен ли RTCUniversalUserAdmins Group Active Directory в группу администраторов.

Дополнительные сведения можно найти в справочной документации по командлету [Test-CsComputer](https://docs.microsoft.com/powershell/module/skype/Test-CsComputer) .

</div>

<div>

## <a name="running-the-test"></a>Выполнение теста

Командлет Test-CsComputer можно запускать только на локальном компьютере, но вы не можете вызвать Test-CsComputer из удаленного экземпляра Windows PowerShell. По умолчанию Test-CsComputer отображает очень мало вывода на экран, а данные, возвращаемые командлетом, записываются в HTML-файл. По этой причине мы рекомендуем включать параметр подробных данных и параметр отчета каждый раз при запуске test-CsComputer. Параметр verbose обеспечивает немного более подробный вывод на экран во время выполнения командлета. Параметр Report позволяет указать путь к файлу и имя файла для HTML-файла, созданного с помощью Test-CsComputer. Если параметр отчета не указан, HTML-файл будет автоматически сохранен в папке Users и будет выглядеть так: ce84964a-c4da-4622-ad34-c54ff3ed361f.html.

В следующем образце команды выполняется Test-CsComputer и данные сохраняются в файле с именем C: \\ Logs \\ComputerTest.html:

    Test-CsComputer -Report "C:\Logs\ComputerTest.html" -Verbose

Дополнительные сведения можно найти в справочной документации по командлету [Test-CsComputer](https://docs.microsoft.com/powershell/module/skype/Test-CsComputer) .

</div>

<div>

## <a name="determining-success-or-failure"></a>Определение успеха или сбоя

Из-за количества выполняемых проверок Test-CsComputer не сообщает о том, что вы просто **Да, проверка прошла успешно** или **нет, тест завершился сбоем**. Вместо этого вам нужно будет просмотреть созданный HTML-файл с помощью Internet Explorer, чтобы определить успешность или сбой каждого теста.

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a>Причины, по которым может произойти сбой теста

Ниже приведены некоторые распространенные причины, по которым может произойти сбой Test-CsComputer.

  - Тестовый компьютер может быть недоступен для использования с сервером Lync Server. Это может произойти, если вы изменили серверные службы Lync или серверные роли на компьютере, а командлет Enable-CsComputer не был запущен. Чтобы устранить эту проблему, выполните следующую команду:
    
        Enable-CsComputer

  - Репликация может быть не актуальна на тестовом компьютере. Вы можете проверить текущее состояние репликации для компьютера, запустив командлет Get-CsManagementStoreReplicationStatus:
    
        Get-CsManagementStoreReplicationStatus -ReplicaFqdn "atl-cs-001.litwareinc.com"
    
    Если состояние репликации не устарело, вы можете вручную выполнить принудительную репликацию с помощью следующей команды:
    
        Invoke-CsManagementStoreReplication -ReplicaFqdn "atl-cs-001.litwareinc.com"

  - Возможно, требуется включить топологию. Если вы измените топологию Lync Server (изменения, которые могут повлиять на локальный компьютер), необходимо включить новую топологию. Вы можете включить топологию в любое время, выполнив следующую команду:
    
        Enable-CsTopology

</div>

</div>

<span> </span>

</div>

</div>

</div>

