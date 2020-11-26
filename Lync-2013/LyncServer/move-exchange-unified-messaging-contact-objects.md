---
title: Перемещение объектов контактов единой системы обмена сообщениями Exchange
description: Перемещение объектов контактов для единой системы обмена сообщениями Exchange.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Move Exchange Unified Messaging Contact objects
ms:assetid: 35c7e987-41b5-4798-b617-3303f20e52e3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688022(v=OCS.15)
ms:contentKeyID: 49733612
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e3353427f407523a8778585d27201355714a3085
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438449"
---
# <a name="move-exchange-unified-messaging-contact-objects"></a>Перемещение объектов контактов единой системы обмена сообщениями Exchange

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-10-19_

Для миграции объектов контактов для автосекретаря (AA) и доступа к подписчикам (SA) на новый сервер Lync Server 2013 сначала нужно переместить объекты из устаревшего развертывания Office Communications Server 2007 R2 на новое развертывание Lync Server 2013 с помощью командлетов **Get-CsExUmContact** и **Move-CsExUmContact** . На сервере Exchange Server вы можете запустить сценарий Windows PowerShell **ExchUCUtil** , чтобы сделать следующее для вновь развернутого пула Lync:

  - Добавьте его в IP-шлюз единой системы обмена сообщениями.

  - Добавьте его в группу слежения единой системы обмена сообщениями.

<div>


> [!NOTE]  
> Чтобы использовать командлеты <STRONG>Get-CsExUmContact</STRONG> и <STRONG>Move-CsExUmContact</STRONG> , вы должны быть участником группы RTCUNIVERSALUSERADMINS и иметь разрешение OU на подразделение, в котором хранятся объекты контактов. Разрешение OU можно предоставить с помощью командлета <STRONG>Grant-OUPermission</STRONG> .



</div>

<div>

## <a name="to-move-contact-objects-by-using-the-lync-server-management-shell"></a>Перемещение объектов контакта с помощью командной консоли Lync Server Management Shell

1.  Откройте командную консоль Lync Server Management Shell.

2.  Для каждого пула, зарегистрированного в единой системе обмена сообщениями Exchange (где pool1.contoso.net — это пул из конфигурации Office Communications Server 2007 R2 и pool2.contoso.net — это пул из развертывания Lync Server 2013), введите следующую команду:
    
        Get-CsExUmContact -Filter {RegistrarPool -eq "pool01.contoso.net"} | Move-CsExUmContact -Target pool02.contoso.net
    
    Чтобы убедиться в том, что объекты контакта перемещены, выполните командлет **Get-CsExumContact** и убедитесь, что в **RegistrarPool** указывает на новый пул.

</div>

<div>

## <a name="to-run-the-exchucutil-windows-powershell-script"></a>Выполнение сценария Windows PowerShell ExchUCUtil

1.  Войдите на сервер Exchange UM как пользователь с правами администратора организации Exchange.

2.  Перейдите на ExchUCUtil сценарий Windows PowerShell.
    
    В Exchange 2007 ExchUCUtil.ps1 расположен по адресу: **% Program Files \\ % \\ сценариев Microsoft Exchange Server \\ \\ExchUCUtil.ps1**
    
    В Exchange 2010 ExchUCUtil.ps1 расположен по адресу: **% Program Files \\ % \\ \\ V14 \\ Scripts \\ for Microsoft Exchange ServerExchUCUtil.ps1**

3.  Если Exchange развернут в одном лесе, введите:
    
        exchucutil.ps1
    
    Если Exchange развернут в нескольких лесах, введите:
    
        exchucutil.ps1 -Forest:" <forest FQDN>"
    
    где полное доменное имя леса определяет лес, в котором развернут Lync Server 2013.
    
    <div>
    

    > [!IMPORTANT]  
    > Не забудьте перезапустить службу <STRONG>переднего плана Lync Server</STRONG> (rtcsrv.exe) <EM>после</EM> запуска exchucutil.ps1. В противном случае Lync Server 2013 не будет определять единую систему обмена сообщениями в топологии.

    
    </div>

</div>

</div>

<span> </span>

</div>

</div>

</div>

