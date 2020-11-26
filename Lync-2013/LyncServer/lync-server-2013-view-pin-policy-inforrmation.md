---
title: 'Lync Server 2013: Просмотр политики ПИН inforrmation'
description: 'Lync Server 2013: Просмотр политики ПИН inforrmation.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View PIN policy inforrmation
ms:assetid: 1d48b060-d77f-44ee-b70f-3ce128aedac4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687985(v=OCS.15)
ms:contentKeyID: 49733575
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d60125663bed2b79921de62663865c56b6a27786
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444100"
---
# <a name="view-pin-policy-inforrmation-in-lync-server-2013"></a>Просмотр политики ПИН-кода inforrmation в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2013-02-23_

С помощью вкладки " **политика закрепления** " можно просмотреть персональный идентификационный номер (ПИН-код) пользователей, которые подключаются к Lync 2013 с IP-телефонами. Чтобы использовать проверку подлинности по ПИН-коду, необходимо установить флажок **Разрешить проверку подлинности на основе ПИН-кода** в настройках веб-службы. Дополнительные сведения можно найти [в разделе изменение существующих параметров конфигурации веб-службы в Lync Server 2013](lync-server-2013-modify-existing-web-service-configuration-settings.md).

Выполните следующие действия, чтобы изменить политику ПИН-кода на уровне пользователя или узла.

<div>

## <a name="to-view-information-about-a-pin-policy-in-lync-server-control-panel"></a>Просмотр сведений о политике закрепления на панели управления Lync Server

1.  Войдите в учетную запись пользователя, которая является членом группы RTCUniversalServerAdmins (или имеет эквивалентные права пользователей) или назначьте роль CsServerAdministrator или CsAdministrator, выполните вход на любой компьютер в сети, в которой вы развернули Lync Server 2013.

2.  Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server. Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).

3.  В левой панели навигации последовательно выберите пункты **Безопасность** и **Политика ПИН-кода**.

4.  На странице **Политика ПИН-кода** выберите политику, нажмите кнопку **Правка**, а затем щелкните **Подробнее**.

</div>

<div>

## <a name="viewing-pin-policies-by-using-windows-powershell-cmdlets"></a>Просмотр политик ПИН-кода с помощью командлетов Windows PowerShell

Вы также можете просмотреть политики ПИН-кода с помощью Windows PowerShell и командлета Get-CsPinPolicy. Этот командлет можно выполнить либо из управляющей оболочки Lync Server 2013, либо из удаленного сеанса Windows PowerShell. Подробнее об использовании удаленной оболочки Windows PowerShell для подключения к серверу Lync Server можно найти в статье "Краткое руководство по работе с Microsoft Lync Server 2010 с помощью удаленной оболочки PowerShell" на веб-сервере Lync Server Windows PowerShell [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .

<div>

## <a name="to-view-pin-policies"></a>Просмотр политик ПИН-кодов

  - Чтобы просмотреть сведения обо всех политиках для ПИН-кода, введите в командной консоли Lync Server следующую команду и нажмите клавишу ВВОД.
    
        Get-CsPinPolicy
    
    Команда возвращает примерно следующую информацию:
    
        Identity             : Global
        Description          :
        MinPasswordLength    : 5
        PINHistoryCount      : 0
        AllowCommonPatterns  : False
        PINLifetime          : 0
        MaximumLogonAttempts :

</div>

Дополнительные сведения можно найти в разделе справки по командлету [Get-CsPinPolicy](https://docs.microsoft.com/powershell/module/skype/Get-CsPinPolicy) .

</div>

<div>

## <a name="see-also"></a>См. также


[Изменение существующих параметров конфигурации веб-службы в Lync Server 2013](lync-server-2013-modify-existing-web-service-configuration-settings.md)  
[Создание новой политики ПИН-кода в Lync Server 2013](lync-server-2013-create-a-new-pin-policy.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

