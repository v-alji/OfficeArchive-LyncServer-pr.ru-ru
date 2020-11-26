---
title: 'Lync Server 2013: Удаление политики ПИН-кода'
description: 'Lync Server 2013: Удаление политики ПИН-кода.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete a PIN policy
ms:assetid: 7c378927-2e41-418e-9721-327021bd2e45
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg521020(v=OCS.15)
ms:contentKeyID: 48184609
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 03e0f1d9c22e367693f846a31b1ad2232f048965
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430702"
---
# <a name="delete-a-pin-policy-in-lync-server-2013"></a>Удаление политики ПИН-кода в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2013-02-23_

Чтобы удалить политику персональных идентификационных номеров (политику ПИН-кодов), выполните следующие действия.

<div>


> [!NOTE]  
> Глобальную политику ПИН-кодов удалить нельзя.



</div>

<div>

## <a name="to-delete-a-pin-policy-in-lync-server-2013-control-panel"></a>Удаление политики ПИН-кода в Lync Server 2013 панели управления

1.  Войдите в учетную запись пользователя, которая является членом группы RTCUniversalServerAdmins (или имеет эквивалентные права пользователей) или назначьте роль CsServerAdministrator или CsAdministrator, выполните вход на любой компьютер в сети, в которой вы развернули Lync Server 2013.

2.  Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server. Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).

3.  В левой панели навигации последовательно выберите пункты **Безопасность** и **Политика ПИН-кода**.

4.  На странице **Политика ПИН-кода** в поле поиска полностью или частично введите имя политики, которую требуется удалить.

5.  В списке политик выберите необходимую политику, щелкните **Правка**, затем выберите **Удалить**.

6.  Нажмите **ОК**.

</div>

<div>

## <a name="removing-pin-policies-by-using-windows-powershell-cmdlets"></a>Удаление политик закрепления с помощью командлетов Windows PowerShell

Вы можете удалять политики закрепления с помощью Windows PowerShell и командлета Remove-CsPinPolicy. Этот командлет можно выполнить либо из управляющей оболочки Lync Server 2013, либо из удаленного сеанса Windows PowerShell. Подробнее об использовании удаленной оболочки Windows PowerShell для подключения к серверу Lync Server можно найти в статье "Краткое руководство по работе с Microsoft Lync Server 2010 с помощью удаленной оболочки PowerShell" на веб-сервере Lync Server Windows PowerShell [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .

<div>

## <a name="to-remove-a-specific-pin-policy"></a>Удаление определенной политики ПИН-кода

  - Эта команда удаляет политику ПИН-кода с идентификатором RedmondPinPolicy:
    
        Remove-CsPinPolicy -Identity "RedmondPinPolicy"

</div>

<div>

## <a name="to-remove-all-the-pin-policies-applied-to-the-site-scope"></a>Порядок применения всех политик ПИН-кода, применяемых на уровне сайта

  - Эта команда удаляет все политики ПИН-кода, настроенные в области действия сайта:
    
        Get-CsPinPolicy -Filter "site:*" | Remove-CsPinPolicy

</div>

<div>

## <a name="to-remove-all-the-pin-policies-that-allow-the-use-of-common-patterns"></a>Удаление всех политик ПИН-кодов, позволяющих использовать общие шаблоны

  - А эта команда удаляет все политики ПИН-кодов, допускающие использование общих шаблонов:
    
        et-CsPinPolicy | Where-Object {$_.AllowCommonPatterns -eq $True} | Remove-CsPinPolicy

</div>

Дополнительные сведения можно найти в разделе справки по командлету [Remove-CsPinPolicy](https://docs.microsoft.com/powershell/module/skype/Remove-CsPinPolicy) .

</div>

</div>

<span> </span>

</div>

</div>

</div>

