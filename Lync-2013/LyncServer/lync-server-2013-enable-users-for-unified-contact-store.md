---
title: 'Lync Server 2013: включение для пользователей единого хранилища контактов'
description: 'Lync Server 2013: включение пользователей для единого хранилища контактов.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enable users for unified contact store
ms:assetid: 7b46a01f-beb5-4a33-adb0-35f0502b168d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205024(v=OCS.15)
ms:contentKeyID: 48184599
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2249249d314e13d840b276e46f1fe38ad271664a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428820"
---
# <a name="enable-users-for-unified-contact-store-in-lync-server-2013"></a>Включение для пользователей единого хранилища контактов в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-10-07_

При развертывании сервера Lync Server 2013 и публикации топологии единое хранилище контактов включается для всех пользователей по умолчанию. Вам не нужно предпринимать никаких дополнительных действий, чтобы активировать единое хранилище контактов после развертывания Lync Server 2013. Однако вы можете использовать командлет **Set-CsUserServicesPolicy** , чтобы настроить, какие пользователи будут доступны в едином хранилище контактов. Вы можете включить эту функцию глобально, по сайту, по клиенту или по отдельным пользователям или группам пользователей.

<div>

## <a name="to-enable-users-for-unified-contact-store"></a>Включение пользователей в едином хранилище контактов

1.  Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.

2.  Выполните одно из указанных ниже действий.
    
      - Чтобы включить единое хранилище контактов глобально для всех пользователей Lync Server, в командной строке введите:
        
            Set-CsUserServicesPolicy -Identity global -UcsAllowed $True
    
      - Чтобы включить единое хранилище контактов для пользователей на определенном сайте, в командной строке введите:
        
            New-CsUserServicesPolicy -Identity site:<site name> -UcsAllowed $True
        
        Например:
        
            New-CsUserServicesPolicy -Identity site:Redmond -UcsAllowed $True
    
      - Чтобы включить единое хранилище контактов по клиенту, в командной строке введите:
        
            Set-CsUserServicesPolicy -Tenant <tenantId> -UcsAllowed $True
        
        Например:
        
            Set-CsUserServicesPolicy -Tenant "38aad667-af54-4397-aaa7-e94c79ec2308" -UcsAllowed $True
    
      - Чтобы включить единое хранилище контактов для определенных пользователей, в командной строке введите:
        
            New-CsUserServicesPolicy -Identity "<policy name>" -UcsAllowed $True
            Grant-CsUserServicesPolicy -Identity "<user display name>" -PolicyName <"policy name">
        
        <div>
        

        > [!NOTE]  
        > Вы также можете использовать псевдонимы пользователя или URI SIP вместо отображаемого имени пользователя.

        
        </div>
        
        Например:
        
            New-CsUserServicesPolicy -Identity "UCS Enabled Users" -UcsAllowed $True
            Grant-CsUserServicesPolicy -Identity "Ken Myer" -PolicyName "UCS Enabled Users"
        
        <div>
        

        > [!NOTE]  
        > В предыдущем примере первая команда создает новую политику для пользователей с <EM>включенным управлением UCS</EM> , при этом для флага UcsAllowed задано значение true. Вторая команда назначает пользователю политику с отображаемым именем Кен Myer, что означает, что Кен Myer теперь включен для единого магазина контактов.

        
        </div>

</div>

</div>

<span> </span>

</div>

</div>

</div>

