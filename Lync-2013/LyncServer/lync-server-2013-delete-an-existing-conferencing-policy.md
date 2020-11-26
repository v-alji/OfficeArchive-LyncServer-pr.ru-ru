---
title: 'Lync Server 2013: удаление существующей политики конференц-связи'
description: 'Lync Server 2013: удаление существующей политики конференц-связи.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete an existing conferencing policy
ms:assetid: 709ed771-790f-4bf1-a4de-b37ca5168688
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688089(v=OCS.15)
ms:contentKeyID: 49733688
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0b64e51acc6e6dc91b938244da28057b01957069
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430506"
---
# <a name="delete-an-existing-conferencing-policy-in-lync-server-2013"></a>Удаление существующей политики конференц-связи в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2013-02-23_

Выполните эти действия, чтобы удалить политику конференц-связи на уровне пользователя или сайта.

<div>


> [!NOTE]  
> Вы не можете удалить глобальную политику конференций.



</div>

<div>

## <a name="to-delete-a-site-or-user-conferencing-policy"></a>Удаление политики сайта или конференц-связи пользователей

1.  Войдите на любой компьютер во внутреннем развертывании с использованием учетной записи пользователя, назначенной роли CsUserAdministrator или CsAdministrator.

2.  Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server. Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).

3.  На панели навигации слева выберите **Конференц** -связь, а затем — **Политика Конференц**-связи.

4.  В списке политик конференц-связи выберите политику узла или пользователя для удаления и щелкните **Изменить**, затем **Удалить**.

</div>

<div>

## <a name="removing-conferencing-policies-by-using-windows-powershell-cmdlets"></a>Удаление политик конференц-связи с помощью командлетов Windows PowerShell

Вы можете удалять политики конференций с помощью командной консоли Lync Server Management Shell и командлета **Remove-CsConferencingPolicy** . Этот командлет можно выполнить из управляющей оболочки Lync Server 2013 или из удаленного сеанса Windows PowerShell. Подробнее об использовании удаленной оболочки Windows PowerShell для подключения к серверу Lync Server можно найти в статье "Краткое руководство по работе с Microsoft Lync Server 2010 с помощью удаленной оболочки PowerShell" на веб-сервере Lync Server Windows PowerShell [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .

<div>

## <a name="to-remove-a-specified-conferencing-policy"></a>Удаление указанной политики конференц-связи

  - Следующая команда удаляет политику конференц-связи с идентификатором RedmondConferencingPolicy:
    
        Remove-CsConferencingPolicy -Identity "RedmondConferencingPolicy"

</div>

<div>

## <a name="to-remove-all-of-the-conferencing-policies-applied-to-the-per-user-scope"></a>Удаление всех политик конференц-связи, примененных к области "на пользователя"

  - Следующая команда удаляет все политики конференций, настроенные в области "на пользователя".
    
        Get-CsConferencingPolicy -Filter "tag:*" | Remove-CsConferencingPolicy

</div>

<div>

## <a name="to-remove-all-of-the-conferencing-polices-that-allow-recording-by-external-users"></a>Удаление всех политик конференц-связи, разрешающих запись внешними пользователями

  - Следующая команда удаляет все политики конференц-связи, позволяющие внешним пользователям записывать конференцию.
    
        Get-CsConferencingPolicy | Where-Object {$_.AllowExternalUsersToRecordMeetings -eq $True} | Remove-CsConferencingPolicy

</div>

Подробности можно найти в разделе [Remove-CsConferencingPolicy](https://docs.microsoft.com/powershell/module/skype/Remove-CsConferencingPolicy).

</div>

</div>

<span> </span>

</div>

</div>

</div>

