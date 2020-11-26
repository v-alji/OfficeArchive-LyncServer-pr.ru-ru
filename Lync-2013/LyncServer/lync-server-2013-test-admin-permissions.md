---
title: 'Lync Server 2013: Проверка разрешений администратора'
description: 'Lync Server 2013: Проверка разрешений администратора.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test admin permissions
ms:assetid: 5dda3efd-0f84-4848-819e-87b1551066b1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn767945(v=OCS.15)
ms:contentKeyID: 63969607
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 07e15be288ed31afe9303d91ce3e623d19822428
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444317"
---
# <a name="test-admin-permissions-in-lync-server-2013"></a>Проверка разрешений администратора в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2014-08-18_


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Расписание проверки</p></td>
<td><p>После первоначального развертывания Lync Server. По мере необходимости, если возникают проблемы, связанные с разрешениями.</p></td>
</tr>
<tr class="even">
<td><p>Средство тестирования</p></td>
<td><p>Windows PowerShell</p></td>
</tr>
<tr class="odd">
<td><p>Требуемые разрешения</p></td>
<td><p>При локальном запуске с помощью командной консоли Lync Server пользователи должны быть членами группы безопасности RTCUniversalServerAdmins.</p>
<p>При запуске с помощью удаленного экземпляра Windows PowerShell пользователям должна быть назначена роль RBAC, имеющая разрешение на запуск командлета Test-CsOUPermission. Чтобы просмотреть список всех ролей RBAC, которые могут использовать этот командлет, выполните в командной строке Windows PowerShell следующую команду:</p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsOUPermission&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a>Описание

При установке Lync Server 2013 1 для задач, выполненных программой установки, группе RTCUniversalUserAdmins предоставляются разрешения Active Directory, необходимые для управления пользователями, компьютерами, контактами, контактами приложения и InetOrg лицами. Если вы отключили наследование разрешений в службе каталогов Active Directory, вам не удастся назначить эти разрешения. В результате участники группы RTCUniversalUserAdmins не смогут управлять сущностями Lync Server. Эти права на управление будут доступны только администраторам домена.

Командлет Test-CsOUPermission проверяет, что необходимые разрешения, необходимые для управления пользователями, компьютерами и другими объектами, задаются в контейнере Active Directory. Если эти разрешения не заданы, вы можете устранить эту проблему, выполнив командлет [Grant-CsOUPermission](https://docs.microsoft.com/powershell/module/skype/Grant-CsOUPermission) .

Обратите внимание, что Grant-CsOUPermission может назначать разрешения только участникам группы RTCUniversalUserAdmins. Вы не можете использовать этот командлет, чтобы предоставить разрешения для произвольного пользователя или группы. Если вы хотите, чтобы другой пользователь или группа имели разрешения на управление пользователями, вы должны добавить этого пользователя (или группу) в группу RTCUniversalUserAdmins.

Дополнительные сведения о разрешениях для подразделений можно найти в статье [отключение наследования разрешений для пользователей и контейнеров inetOrgPerson в Lync Server 2013](lync-server-2013-permissions-inheritance-is-disabled-on-computers-users-or-inetorgperson-containers.md).

</div>

<div>

## <a name="running-the-test"></a>Выполнение теста

Чтобы убедиться в том, что для контейнера заданы разрешения на управление, выполните командлет Test-CsOUPermission, а затем различающееся имя контейнера и тип проверяемых разрешений. Например, эта команда проверяет, заданы ли разрешения пользователей на подразделение OU = Redmond, DC = плана litwareinc, DC = com:

    Test-CsOUPermission -OU "ou=Redmond,dc=litwareinc,dc=com" -ObjectType "user"

Для проверки нескольких разрешений с помощью одной команды заключите все типы разрешений в кавычки, а затем разделите их с помощью запятых. Например, одна из этих команд проверяет разрешения пользователей, компьютеров и контактов.

    Test-CsOUPermission -OU "ou=Redmond,dc=litwareinc,dc=com" -ObjectType "user", "computer", "contact"

Дополнительные сведения можно найти в разделе справки по командлету [Test-CsOUPermission](https://docs.microsoft.com/powershell/module/skype/Test-CsOUPermission) .

</div>

<div>

## <a name="determining-success-or-failure"></a>Определение успеха или сбоя

Если необходимые разрешения уже установлены, Test-CsOUPermission будет возвращать ответ из одного слова:

Верно

Если необходимые разрешения не заданы, Test-CsOUPermission возвратит значение false. Может потребоваться найти это значение в течение некоторого времени. Как правило, он встраивается в несколько соответствующих предупреждений. Например:

Предупреждение: запись контроля доступа (ACE) ATL-CS-001 \\ RTCUniversalUserReadOnlyGroup; Allow; ReadProperty; ContainerInherit; Потомки; bf967aba-0de6-11d0-00aa003049e2; d819615a-3b9b-4738-b47e-f1bd8ee3aea4

Предупреждение: элементы управления доступом (ACE) для объекта "OU = NorthAmerica, DC = ATL-CS-001 DC = \\ плана litwareinc, DC = com" не готовы.

False

Предупреждение: обработка "Test-CsOUPermission" завершена с предупреждениями. во время этого запуска записано предупреждение "2".

Предупреждение: подробные результаты можно найти на странице "C: \\ Users \\ Admin \\ AppData \\ Local \\ temp \\Test-CsOUPermission-5d7a89af-f854-4a9c-87e3-69e37e58de.html".

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a>Причины, по которым может произойти сбой теста

Если Test-CsOUPermission не проходит, это обычно означает, что указанное разрешение не назначено группе RTCUniversalUserAdmins. Вы можете устранить эту проблему и назначить необходимые разрешения с помощью командлета Grant-CsOUPermission. Например, эта команда предоставляет разрешения на доступ к подразделению для пользователей, контактов и inetOrgPersons группе RTCUniversalUserAdmins:

    Grant-CsOUPermission -OU "ou=Redmond,dc=litwareinc,dc=com" -ObjectType "user", "contact", "inetOrgPerson"

Дополнительные сведения можно найти в разделе справки по командлету Grant-CsOUPermission.

</div>

</div>

<span> </span>

</div>

</div>

</div>

