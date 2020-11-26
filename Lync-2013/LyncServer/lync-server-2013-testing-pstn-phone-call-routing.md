---
title: 'Lync Server 2013: Проверка маршрутизации звонков по телефонной сети PSTN'
description: 'Lync Server 2013: Проверка маршрутизации звонков по телефонной сети PSTN.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing PSTN phone call routing
ms:assetid: 301dd44d-03e9-41cd-9722-54e00365aa45
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn727302(v=OCS.15)
ms:contentKeyID: 63969598
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: da931b43176932a9b6781fa27318e83e6994548c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440992"
---
# <a name="testing-pstn-phone-call-routing-in-lync-server-2013"></a>Проверка маршрутизации телефонных звонков PSTN в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2014-11-01_


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
<p>При запуске с помощью удаленного экземпляра Windows PowerShell пользователям должна быть назначена роль RBAC, имеющая разрешение на запуск командлета <strong>Test-CsInterTrunkRouting</strong> . Чтобы просмотреть список всех ролей RBAC, которые могут использовать этот командлет, выполните в командной строке Windows PowerShell следующую команду:</p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsInterTrunkRouting&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a>Описание

Командлет **Test-CsInterTrunkRouting** подтверждает, что звонки могут маршрутизироваться от одного SIP к другому. Для этого командлету задается номер телефона и конфигурация магистрали. **Тест-CsInterTrunkRouting** будет указывать маршруты обратного сопоставления и использование PSTN для указанного номера. Обратите внимание на то, что звонки между магистральами могут маршрутизироваться только в том случае, если в магистральных каналов есть шаблон номера, который соответствует указанному номеру телефона и только в том случае, если в магистральных каналов есть хотя бы одна PSTN.

</div>

<div>

## <a name="running-the-test"></a>Выполнение теста

Команды, показанные ниже, возвращают подходящие маршруты и соответствующие использование телефона, позволяющие пользователям звонить по номеру 1-206-555-1219 с помощью параметров конфигурации канала для сайта Redmond.

    $trunk = Get-CsTrunkConfiguration -Identity "site:Redmond"
    
    Test-CsInterTrunkRouting -TargetNumber "tel:+12065551219" -TrunkConfiguration $trunk

</div>

<div>

## <a name="determining-success-or-failure"></a>Определение успеха или сбоя

Если звонки могут маршрутизироваться от одного SIP к другому, вы получите вывод, как показано ниже.

FirstMatchingRoute MatchingUsage MatchingRoutes

\------------------ ------------- --------------

RedmondRoute LocalUsage {RedmondRoute}

Если проверка завершилась сбоем, вы получите вывод примерно так:

Test-CsInterTrunkRouting: не удается обработать Преобразование аргументов для параметра

'TrunkConfiguration'. Недопустимый TrunkConfigurationsetting (параметр). Укажите

допустимый параметр (параметр) и повторите попытку.

В строке: 1 символ: 79

\+ Test-CsInterTrunkRouting TargetNumber "Tel: + 12065551219"

\-TrunkConfiguration $t...

\+

~~

\+ CategoryInfo: InvalidData: (:) \[ Test-CsInterTrunkRouting \] , номинал

ameterBindingArgumentTransformationException

\+ FullyQualifiedErrorId: ParameterArgumentTransformationError, Microsoft. R

традиционно. Management. Voice. командлеты. TestOcsInterTrunkRoutingCmdlet

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a>Причины, по которым может произойти сбой теста

Ниже приведены некоторые распространенные причины, по которым может произойти сбой **Test-CsInterTrunkRouting** :

  - Указаны недопустимые параметры. Возможно, вы еще не настроили магистраль, а указанный конечный номер может быть неверным или недействительным.

</div>

<div>

## <a name="see-also"></a>См. также


[Get-CsTrunk](https://docs.microsoft.com/powershell/module/skype/Get-CsTrunk)  
[Get-CsTrunkConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsTrunkConfiguration)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

