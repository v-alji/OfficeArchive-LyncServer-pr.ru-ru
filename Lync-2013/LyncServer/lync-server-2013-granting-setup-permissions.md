---
title: 'Lync Server 2013: предоставление разрешений на установку'
description: 'Lync Server 2013: предоставление разрешений на настройку.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Granting setup permissions
ms:assetid: 15982bfe-6844-44f6-815a-72dcaf0e4d21
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398225(v=OCS.15)
ms:contentKeyID: 48183491
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5523494219d07907caeefc1bd139c41856effa54
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427902"
---
# <a name="granting-setup-permissions-in-lync-server-2013"></a>Предоставление разрешений на установку в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-08-27_

Вы можете использовать командлет **Grant-CsSetupPermission** , чтобы добавить разрешения на чтение, запись, ReadSPN и WriteSPN для группы RTCUniversalServerAdmins для указанного организационного подразделения Active Directory (OU). Затем члены группы RTCUniversalServerAdmins в этом подразделении могут устанавливать серверы, на которых запущен Lync Server 2013 в указанном домене, и не входить в группу администраторов домена.

Используйте командлет **Test-CsSetupPermission** для проверки разрешений, настроенных с помощью командлета **Grant-CsSetupPermission** .

Командлет **REVOKE-CsSetupPermission** можно использовать для удаления разрешений, предоставленных с помощью командлета **Grant-CsSetupPermission** .

<div>

## <a name="to-grant-setup-permissions"></a>Предоставление разрешений на настройку

1.  Войдите на компьютер, на котором работает Lync Server 2013, в домен, в котором вы хотите предоставить разрешения на установку. Используйте учетную запись, которая входит в группу "Администраторы домена" или "Администраторы предприятия", если подразделение находится в другом дочернем домене.

2.  Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.

3.  Выполните следующую команду:
    
        Grant-CsSetupPermission -ComputerOu <DN of the OU or container where the computer objects that will run Lync Server reside > [-Domain <Domain FQDN>]
    
    Параметр ComputerOu можно задать относительно контекста именования по умолчанию для указанного домена (например, CN = Computers). Кроме того, вы можете указать этот параметр в качестве полного различающегося имени OU (DN), например "CN = Computers, DC = contoso, DC = com"). В последнем случае необходимо указать различающееся имя OU, соответствующее указанному домену.
    
    Если параметр Domain не указан, значение по умолчанию — локальный домен.

</div>

<div>

## <a name="to-verify-setup-permissions"></a>Проверка разрешений на установку

1.  Войдите на компьютер, на котором работает Lync Server 2013, в домен, в котором вы хотите проверить разрешения на установку, предоставленные с помощью командлета **Grant-CsSetupPermission** . Используйте учетную запись, которая входит в группу "Администраторы домена" или "Администраторы предприятия", если подразделение находится в другом дочернем домене.

2.  Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.

3.  Выполните следующую команду:
    
        Test-CsSetupPermission -ComputerOu <DN of the OU or container where the computer objects that will run Lync Server reside> [-Domain <Domain FQDN>]
    
    Параметр ComputerOu можно задать относительно контекста именования по умолчанию для указанного домена (например, CN = Computers). Кроме того, вы можете указать этот параметр в качестве полного различающегося имени OU (DN), например "CN = Computers, DC = contoso, DC = com"). В последнем случае необходимо указать различающееся имя OU, соответствующее указанному домену.
    
    Если параметр Domain не указан, значение по умолчанию — локальный домен.

</div>

<div>

## <a name="to-revoke-setup-permissions"></a>Отмена разрешений на установку

1.  Войдите на компьютер, на котором работает Lync Server 2013, в домен, для которого вы хотите отозвать разрешения на установку, предоставленные командлетом **Grant-CsSetupPermission** . Используйте учетную запись, которая входит в группу "Администраторы домена" или "Администраторы предприятия", если подразделение находится в другом дочернем домене.

2.  Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.

3.  Выполните следующую команду:
    
        Revoke-CsSetupPermission -ComputerOu <DN of the OU or container where the computer objects that will run Lync Server reside > [-Domain <Domain FQDN>]
    
    Параметр ComputerOu можно задать относительно контекста именования по умолчанию для указанного домена (например, CN = Computers). Кроме того, вы можете указать этот параметр в качестве полного различающегося имени OU (DN), например "CN = Computers, DC = contoso, DC = com"). В последнем случае необходимо указать различающееся имя OU, соответствующее указанному домену.
    
    Если параметр Domain не указан, значение по умолчанию — локальный домен.

</div>

</div>

<span> </span>

</div>

</div>

</div>

