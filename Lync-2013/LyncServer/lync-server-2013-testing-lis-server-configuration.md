---
title: 'Lync Server 2013: Проверка конфигурации сервера LIS'
description: 'Lync Server 2013: Проверка конфигурации сервера LIS.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing LIS server configuration
ms:assetid: 6b06e7ab-522f-41a2-878b-e89cd4e3c6da
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn690129(v=OCS.15)
ms:contentKeyID: 63969614
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ba4d16d2ce48e3e5bb89e863f02902d05ce77bd7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398962"
---
# <a name="testing-lis-server-configuration-in-lync-server-2013"></a>Тестирование конфигурации сервера LIS в Lync Server 2013

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
<p>При запуске с помощью удаленного экземпляра Windows PowerShell пользователям должна быть назначена роль RBAC, имеющая разрешение на запуск командлета Test-CsLisConfiguration. Чтобы просмотреть список всех ролей RBAC, которые могут использовать этот командлет, выполните в командной строке Windows PowerShell следующую команду:</p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsLisConfiguration&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a>Описание

Командлет Test-CsLisConfiguration проверит, есть ли у вас возможность связаться с веб-службой LIS. Если вы можете связаться с веб-службой, проверка будет считаться успешной, независимо от того, можно ли найти определенные места.

</div>

<div>

## <a name="running-the-test"></a>Выполнение теста

Командлет Test-CsLisConfguration можно выполнить с помощью предварительно настроенной тестовой учетной записи (см. раздел Настройка тестовых учетных записей для выполнения тестов Lync Server) или учетной записи пользователя, который включен для Lync Server. Для выполнения этой проверки с помощью тестовой учетной записи нужно просто указать полное доменное имя для тестируемого пула Lync Server. Например:

    Test-CsLisConfiguration -TargetFqdn "atl-cs-001.litwareinc.com"

Чтобы выполнить эту проверку с использованием реальной учетной записи пользователя, необходимо сначала создать объект учетных данных Windows PowerShell, содержащий имя учетной записи и пароль. Затем необходимо добавить этот объект учетных данных и адрес SIP, назначенный учетной записи, при вызове Test-CsLisConfiguration:

    $credential = Get-Credential "litwareinc\kenmyer"
    Test-CsLisConfiguration -TargetFqdn "atl-cs-001.litwareinc.com"-UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential

Дополнительные сведения можно найти в справочной документации по командлету [Test-CsLisConfiguration](https://docs.microsoft.com/powershell/module/skype/Test-CsLisConfiguration) .

</div>

<div>

## <a name="determining-success-or-failure"></a>Определение успеха или сбоя

Если вы правильно настроили LIS, вы получите вывод примерно так, чтобы свойство Result пометило **"успешно".**

TargetUri : https://atl-cs-001.litwareinc.com:443/locationinformation/

liservice. svc

TargetFqdn: atl-cs-001.litwareinc.com

Результат: успех

Задержка: 00:00:06.1616913

Ошибки

Диагностик

Если указанному пользователю не удается войти в систему или выйти из нее, результат будет показан в виде ошибки, а дополнительные сведения будут записаны в свойствах Error и диагноз.

TargetUri :

TargetFqdn: atl-cs-001.litwareinc.com

Результат: сбой

Задержка: 00:00:00

Ошибка: 11004, запрошенное имя является действительным, но никаких данных запрошенного

Тип найден

Диагностик

Test-CsLisConfiguration: в топологии не найдено подходящих кластеров.

Например, в предыдущем выводе есть Примечание "в топологии не найдено подходящего кластера". Обычно это свидетельствует о проблеме с сервером граничного сервера: LIS с помощью пограничного сервера для подключения к поставщику услуг и проверки адресов.

Если Test-CsLisConfiguration не удается, возможно, потребуется повторно выполнить тест, на этот раз включая параметр подробно:

    Test-CsLisConfiguration -TargetFqdn "atl-cs-001.litwareinc.com" -Verbose

После включения подробной информации Test-CsLisConfiguration будет возвращать пошаговые учетные записи каждого действия, которое он пытался войти на сервер Lync Server. Например:

Вызов службы сведений о расположении.

Путь к службе = https://atl-cs-001.litwareinc.com:443/locationinformation/liservice.svc

Subnet =

BssId = 5

ChassisId =

PortId =

PortIdSubType = неопределенный тип

Mac

Не удалось выполнить запрос веб-службы сведений о расположении с кодом ответа Item400. произошла ошибка во время выполнения рабочего процесса Microsoft. RTC. SyntheticTrsnactions. Workflows. STLisConfigurationWorkflow.

Если вы проанализируете предыдущий вывод, вы увидите, что командлет завершился сбоем после того, как он попытался вызвать службу сведений о расположении. Один из параметров, которые использовались в этом вызове:

BssId = 5

Это значение не является допустимым для базового идентификатора Set службы (BssID). Вместо этого BssID должен выглядеть примерно так:

12-34-56-78-90 – AB

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a>Причины, по которым может произойти сбой теста

Ниже приведены некоторые распространенные причины, по которым может произойти сбой Test-CsLisConfiguration.

  - Предоставлено неправильное значение параметра. Как показано в предыдущем примере, необязательные параметры должны быть настроены правильно, или тест завершится сбоем. Повторите выполнение команды без дополнительных параметров и проверьте, выполняется ли это успешно.

</div>

</div>

<span> </span>

</div>

</div>

</div>

