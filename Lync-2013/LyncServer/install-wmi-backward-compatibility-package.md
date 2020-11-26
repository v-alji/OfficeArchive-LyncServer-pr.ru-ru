---
title: Установка пакета обратной совместимости WMI
description: Установка пакета обратной совместимости WMI.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Install WMI Backward Compatibility package
ms:assetid: 38797fbd-06a0-4008-b099-158e7b5d7703
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204816(v=OCS.15)
ms:contentKeyID: 48183893
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9062e209981fd180b8772801960bd94d2256513a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439584"
---
# <a name="install-wmi-backward-compatibility-package"></a>Установка пакета обратной совместимости WMI

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-10-02_

Если вы попытаетесь запустить мастер слияния построителя топологии без установки пакета обратной совместимости WMI, появится следующее сообщение об ошибке:

![Сообщение об ошибке WMI](images/JJ204816.a007d2f2-fc85-430c-91eb-382b032469af(OCS.15).jpg "Сообщение об ошибке WMI")

При попытке выполнить командлет **Merge-CsLegacytopology** без установки пакета обратной совместимости WMI появляется следующее сообщение об ошибке:

![Ошибка поставщика Windows PowerShell WMI](images/JJ204816.c510824e-1807-4c7e-bb28-c6cfea2eac1d(OCS.15).jpg "Ошибка поставщика Windows PowerShell WMI")

Установка пакета обратной совместимости WMI

1.  С установочного носителя перейдите в раздел \\ настройка \\ \\OCSWMIBC.MSI установки amd64 \\ .

2.  Установите OCSWMIBC.MSI.
    
    <div>
    

    > [!IMPORTANT]  
    > OCSWMIBC.msi необходимо установить на компьютере, на котором запущен мастер объединения Topology Builder. Однако рекомендуется устанавливать OCSWMIBC.msi на всех серверах переднего плана в топологии.

    
    </div>
    
    <div>
    

    > [!IMPORTANT]  
    > OCSWMIBC.msi можно установить на любом компьютере домена, на котором установлены основные компоненты Lync Server 2013 и Командная консоль Lync Server 2013, и у него есть доступ к топологии Office Communications Server 2007 R2 (поставщик WMI для доменных служб Active Directory) и SQL Server.

    
    </div>

</div>

<span> </span>

</div>

</div>

</div>

