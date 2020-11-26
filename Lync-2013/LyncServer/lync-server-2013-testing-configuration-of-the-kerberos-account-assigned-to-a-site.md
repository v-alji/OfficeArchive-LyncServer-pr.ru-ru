---
title: Проверка конфигурации учетной записи Kerberos, назначенной сайту
description: Проверка конфигурации учетной записи Kerberos, назначенной сайту.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing configuration of the Kerberos account assigned to a site
ms:assetid: a087d77e-c59e-44f5-9caa-ccfd41be7276
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn743837(v=OCS.15)
ms:contentKeyID: 63969637
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0eab1618474a19753a4c6064d59aa4f8a856fceb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441069"
---
# <a name="testing-configuration-of-the-kerberos-account-assigned-to-a-site-in-lync-server-2013"></a>Проверка конфигурации учетной записи Kerberos, назначенной сайту, в Lync Server 2013

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
<p>При запуске с помощью удаленного экземпляра Windows PowerShell пользователям должна быть назначена роль RBAC, имеющая разрешение на запуск командлета Test-CsKerberosAccountAssignment. Чтобы просмотреть список всех ролей RBAC, которые могут использовать этот командлет, выполните в командной строке Windows PowerShell следующую команду:</p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsKerberosAccountAssignment&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a>Описание

Командлет Test-CsKerberosAccountAssignment позволяет удостовериться, что учетная запись Kerberos связана с указанным сайтом, что эта учетная запись настроена правильно, а учетная запись работает должным образом. Учетные записи Kerberos — это учетные записи компьютеров, которые могут служить субъектом проверки подлинности для всех компьютеров на сайте, на котором запущен сервер IIS. Поскольку эти учетные записи используют протокол проверки подлинности Kerberos, учетные записи известны как учетные записи Kerberos, а новый процесс проверки подлинности известен как веб-проверка подлинности Kerberos. Это позволяет управлять всеми серверами IIS с помощью одной учетной записи.

Дополнительные сведения можно найти в справочной документации по командлету [Test-CsKerberosAccountAssignment](https://technet.microsoft.com/library/Gg425938(v=OCS.15)) .

</div>

<div>

## <a name="running-the-test"></a>Выполнение теста

По умолчанию в Test-CsKerberosAccountAssignment отображается очень маленький вывод на экран. Вместо этого данные, возвращаемые командлетом, записываются в HTML-файл. По этой причине мы рекомендуем включать параметр подробных данных и параметр отчета каждый раз при запуске test-CsKerberosAccountAssignment. Параметр verbose обеспечивает немного более подробный вывод на экран во время выполнения командлета. Параметр Report позволяет указать путь к файлу и имя файла для HTML-файла, созданного с помощью Test-CsKerberosAccountAssignment. Если параметр отчета не указан, HTML-файл будет автоматически сохранен в папке Users и будет выглядеть так: ce84964a-c4da-4622-ad34-c54ff3ed361f.html.

Кроме того, необходимо указать удостоверение сайта при запуске test-CsKerberosAccountAssignment. Учетные записи Kerberos назначаются на уровне сайта.

Следующая команда запускает Test-CsKerberosAccountAssignment и сохраняет результат в файле с именем C: \\ Logs \\KerberosTest.html:

    Test-CsKerberosAccountAssignment -Identity "site:Redmond" -Report "C:\Logs\KerberosTest.html" -Verbose

Дополнительные сведения можно найти в справочной документации по командлету [Test-CsKerberosAccountAssignment](https://technet.microsoft.com/library/Gg425938(v=OCS.15)) .

</div>

<div>

## <a name="determining-success-or-failure"></a>Определение успеха или сбоя

Командлет Test-CsKerberosAccountAssignment не возвращает простой индикатор успеха или сбоя. Вместо этого вы должны просмотреть созданный HTML-файл с помощью Internet Explorer.

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a>Причины, по которым может произойти сбой теста

Ниже приведены некоторые распространенные причины, по которым может произойти сбой Test-CsKerberosAccountAssignment.

  - Возможно, вы указали неверный идентификатор сайта. Чтобы возвратить список допустимых идентификаторов сайта, используйте следующую команду:
    
        Get-CsSite | Select-Identity Identity
    
    Идентификатор сайта обычно выглядит следующим образом:
    
    сайт: Redmond

  - Возможно, для указанного сайта не назначена учетная запись Kerberos. Вы можете определить, назначена ли учетная запись Kerberos сайту, выполнив следующую команду:
    
        Get-CsKerberosAccountAssignment -Identity "site:Redmond"

  - Ваша учетная запись Kerberos может иметь Недействительный пароль. Если в отчете появляется следующее сообщение об ошибке, возможно, потребуется сбросить пароль учетной записи Kerberos.
    
    InvalidKerberosConfiguration: Недопустимая конфигурация Kerberos.
    
    InvalidKerberosConfiguration: Недопустимая конфигурация Kerberos на atl-cs001.litwareinc.com. Ожидаемой назначенной учетной записи является плана litwareinc \\ kerberostest. Убедитесь в том, что срок действия учетной записи не истек, и настроенный пароль для компьютера совпадает с паролем учетной записи Active Directory.
    
    Вы можете установить пароль с помощью командлета [Set-CsKerberosAccountPassword](https://technet.microsoft.com/library/Gg398659(v=OCS.15)) .

</div>

</div>

<span> </span>

</div>

</div>

</div>

