---
title: 'Lync Server 2013: восстановление правила обновления устройства'
description: 'Lync Server 2013: восстановление правила обновления устройства.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Restore a Device Update rule
ms:assetid: ac490baf-c7a0-48d9-8fd0-ba5729489341
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994061(v=OCS.15)
ms:contentKeyID: 51803972
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b3696bc7e074bfd7bea04b08246f07e107d4d0b9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442679"
---
# <a name="restore-a-device-update-rule-in-lync-server-2013"></a>Восстановление правила обновления устройства в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2013-02-23_

Чтобы удалить правило обновления устройства с устройств в развертывании, восстановите его. При восстановлении правила обновления для устройства удаляется и переустанавливается Предыдущая версия правила.

Вы можете восстановить правило обновления устройства с помощью панели управления Lync Server или Windows PowerShell.

<div>

## <a name="to-restore-device-update-rules-by-using-lync-server-control-panel"></a>Восстановление правил обновления устройства с помощью панели управления Lync Server

1.  Войдите на любой компьютер во внутреннем развертывании с использованием учетной записи пользователя, назначенной роли CsUserAdministrator или CsAdministrator.

2.  Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server. Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).

3.  На панели навигации слева выберите пункт **Клиенты** и нажмите кнопку Навигация по **обновлению устройства** .

4.  На странице **обновление устройства** выполните одно из указанных ниже действий.
    
      - Чтобы восстановить одно правило, выберите это правило.
    
      - Чтобы восстановить все правила, нажмите кнопку **изменить**, а затем выберите команду **выделить все**.

5.  Откройте меню **действия** , а затем выберите команду **восстановить**.

</div>

<div>

## <a name="restoring-device-update-rules-by-using-windows-powershell-cmdlets"></a>Восстановление правил обновления устройства с помощью командлетов Windows PowerShell

Кроме того, вы можете восстановить правила обновления устройства с помощью Windows PowerShell и командлета **RESTORE-CsDeviceUpdateRule** . Этот командлет можно выполнить либо из управляющей оболочки Lync Server 2013, либо из удаленного сеанса Windows PowerShell.

<div>


> [!NOTE]  
> Подробнее об использовании удаленной оболочки Windows PowerShell для подключения к серверу Lync Server можно найти в статье "Краткое руководство по работе с Microsoft Lync Server 2010 с помощью удаленной оболочки PowerShell" на веб-сервере Lync Server Windows PowerShell <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A> .



</div>

<div>

## <a name="to-restore-a-single-device-update-rule-on-a-server"></a>Восстановление отдельного правила обновления устройства на сервере

  - Следующая команда восстанавливает правило обновления устройства d5ce3c10-2588-420A-82ac-dc2d9b1222ff9 на веб-сервере atl-cs-001.litwareinc.com:
    
        Restore-CsDeviceUpdateRule -Identity "service:WebServer:atl-cs-001.litwareinc.com/d5ce3c10-2588-420a-82ac-dc2d9b1222ff9"

</div>

<div>

## <a name="to-restore-all-the-device-update-rules-on-a-server"></a>Восстановление всех правил обновления устройства на сервере

  - Эта команда восстанавливает все правила обновления устройств на веб-сервере atl-cs-001.litwareinc.com:
    
        Get-CsDeviceUpdateRule -Filter "service:WebServer:atl-cs-001.litwareinc.com*" | Restore-CsDeviceUpdateRule

</div>

Дополнительные сведения можно найти в разделе справки по командлету [RESTORE-CsDeviceUpdateRule](https://docs.microsoft.com/powershell/module/skype/Restore-CsDeviceUpdateRule) .

</div>

</div>

<span> </span>

</div>

</div>

</div>

