---
title: 'Lync Server 2013: предоставление разрешений организационного подразделения'
description: 'Lync Server 2013: предоставление разрешений на доступ к организационному подразделению.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Granting organizational unit permissions
ms:assetid: 95ee5ffa-39b1-4d80-87a2-27bb364f7396
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398763(v=OCS.15)
ms:contentKeyID: 48184849
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 47ad862241e409190620afa7dbf4fa73adf339de
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427899"
---
# <a name="granting-organizational-unit-permissions-in-lync-server-2013"></a>Предоставление разрешений организационного подразделения в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-05-14_

Командлет **Grant-CsOuPermission** можно использовать, чтобы предоставить разрешения на доступ к объектам в указанных организационных подразделениях (OU) таким образом, чтобы пользователи универсальных групп RTC, созданные с помощью подготовки леса, могли получать к ним доступа, не прибегая к группе администраторов домена. Разрешения, добавленные в указанный ОРГАНИЗАЦИОНный элемент, являются теми же разрешениями, которые командлет **Enable-CsAdDomain** добавляет к контейнерам компьютеров и пользователей во время подготовки домена.

Используйте командлет **Test-CsOuPermission** для проверки разрешений, настроенных с помощью командлета **Grant-CsOuPermission** .

Командлет **REVOKE-CsOuPermission** можно использовать для удаления разрешений, предоставленных с помощью командлета **Grant-CsOuPermission** .

<div>

## <a name="to-grant-ou-permissions"></a>Предоставление разрешений на доступ к подразделению

1.  Войдите на компьютер, на котором работает Lync Server 2013, в домен, в котором вы хотите предоставить разрешения на доступ к подразделению. Используйте учетную запись, которая входит в группу "Администраторы домена" или "Администраторы предприятия", если подразделение находится в другом дочернем домене.

2.  Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.

3.  Выполните следующую команду:
    
        Grant-CsOuPermission -ObjectType <User | Computer | InetOrgPerson | Contact | AppContact | Device> -OU <DN of the OU> [-Domain <Domain FQDN>]
    
    Если параметр Domain не указан, значение по умолчанию — локальный домен.

</div>

<div>

## <a name="to-verify-ou-permissions"></a>Проверка разрешений на доступ к подразделению

1.  Войдите на компьютер, на котором работает Lync Server 2013, в домен, в котором вы хотите проверить разрешения на доступ к подразделению, предоставленные с помощью командлета **Grant-CsOuPermission** . Используйте учетную запись, которая входит в группу "Администраторы домена" или "Администраторы предприятия", если подразделение находится в другом дочернем домене.

2.  Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.

3.  Выполните следующую команду:
    
        Test-CsOuPermission -ObjectType <User | Computer | InetOrgPerson | Contact | AppContact | Device> -OU <DN of the OU> [-Domain <Domain FQDN>]
    
    Если параметр Domain не указан, значение по умолчанию — локальный домен.

</div>

<div>

## <a name="to-revoke-ou-permissions"></a>Отмена разрешений на доступ к подразделению

1.  Войдите на компьютер, на котором работает Lync Server 2013, в домен, в котором вы хотите отозвать разрешения на доступ к подразделению, предоставленные командлетом **Grant-CsOuPermission** . Используйте учетную запись, которая входит в группу "Администраторы домена" или "Администраторы предприятия", если подразделение находится в другом дочернем домене.

2.  Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.

3.  Выполните следующую команду:
    
        Revoke-CsOuPermission -ObjectType <User | Computer | InetOrgPerson | Contact | AppContact | Device> -OU <DN of the OU> [-Domain <Domain FQDN>]
    
    Если параметр Domain не указан, значение по умолчанию — локальный домен.

</div>

</div>

<span> </span>

</div>

</div>

</div>

