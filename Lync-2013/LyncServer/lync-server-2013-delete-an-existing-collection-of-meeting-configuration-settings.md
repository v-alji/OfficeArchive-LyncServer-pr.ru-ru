---
title: Удаление существующей коллекции параметров конфигурации собрания
description: Удаление существующей коллекции параметров конфигурации собраний.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete an existing collection of meeting configuration settings
ms:assetid: 92ff8a91-05c5-4047-a533-5dff12f22299
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688136(v=OCS.15)
ms:contentKeyID: 49733736
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9fc0985023a1459130c7d589327535436145a0ac
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430534"
---
# <a name="delete-an-existing-collection-of-meeting-configuration-settings-in-lync-server-2013"></a>Удаление существующей коллекции параметров конфигурации собрания в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2013-02-23_

Вы можете удалить сайт или конфигурацию пользователя. Невозможно удалить глобальную конфигурацию. При удалении глобальной конфигурации она автоматически восстанавливает значения по умолчанию.

<div>

## <a name="to-delete-a-site-or-user-meeting-configuration"></a>Удаление конфигурации сайта или собрания пользователя

1.  Войдите на любой компьютер во внутреннем развертывании с использованием учетной записи пользователя, назначенной роли CsUserAdministrator или CsAdministrator.

2.  Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server. Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).

3.  На панели навигации слева выберите **Конференц** -связь, а затем — **Конфигурация собрания**.

4.  В списке конфигураций собрания выберите конфигурацию сайта или пула, щелкните **Изменить**, а затем **Удалить**.

</div>

<div>

## <a name="removing-meeting-configuration-settings-by-using-windows-powershell-cmdlets"></a>Удаление параметров конфигурации собраний с помощью командлетов Windows PowerShell

Параметры собрания можно удалить с помощью Windows PowerShell и командлета Remove-CsMeetingConfiguration. Этот командлет можно выполнить либо из управляющей оболочки Lync Server 2013, либо из удаленного сеанса Windows PowerShell. Подробнее об использовании удаленной оболочки Windows PowerShell для подключения к серверу Lync Server можно найти в статье "Краткое руководство по работе с Microsoft Lync Server 2010 с помощью удаленной оболочки PowerShell" на веб-сервере Lync Server Windows PowerShell [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .

<div>

## <a name="to-remove-a-specified-collection-of-meeting-configuration-settings"></a>Удаление заданной коллекции параметров конфигурации собрания

  - Эта команда удаляет параметры конфигурации собрания, примененные к сайту Redmond.
    
        Remove-CsMeetingConfiguration -Identity "site:Redmond"

</div>

<div>

## <a name="to-remove-all-the-meeting-configuration-settings-applied-to-the-site-scope"></a>Удаление всех параметров конфигурации собрания, примененных к области сайта

  - Эта команда удаляет все параметры конфигурации собрания, примененные к области сайта.
    
        Get-CsMeetingConfiguration -Filter "site:*" | Remove-CsMeetingConfiguration

</div>

<div>

## <a name="to-remove-all-the-meeting-configuration-settings-that-admit-anonymous-users-by-default"></a>Удаление всех параметров конфигурации собрания, которые по умолчанию применяют анонимные пользователи

  - И этот параметр удаляет все параметры, которые позволяют принимать анонимные пользователи по умолчанию.
    
        Get-CsMeetingConfiguration | Where-Object {$_.AdmitAnonymousUsersByDefault -eq $True} | Remove-CsMeetingConfiguration

</div>

Дополнительные сведения можно найти в разделе справки по командлету [Remove-CsMeetingConfiguration](https://technet.microsoft.com/library/Gg412775(v=OCS.15)) .

</div>

</div>

<span> </span>

</div>

</div>

</div>

