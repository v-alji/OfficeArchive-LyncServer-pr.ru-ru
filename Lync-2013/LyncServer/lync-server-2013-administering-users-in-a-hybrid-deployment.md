---
title: 'Lync Server 2013: Администрирование пользователей в гибридном развертывании'
description: 'Lync Server 2013: Администрирование пользователей в гибридном развертывании.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Administering users in a hybrid deployment
ms:assetid: 6924ed7b-30a9-4be7-b952-90655625f2c8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204967(v=OCS.15)
ms:contentKeyID: 48184381
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7f1d7684a9f56eb013574a985ded0313378621c2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398008"
---
# <a name="administering-users-in-a-hybrid-lync-server-2013-deployment"></a>Администрирование пользователей в гибридном развертывании Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2014-05-29_

Вы можете управлять параметрами пользователей и политиками для пользователей, перенесенных на Lync Online с помощью функций управления пользователями, которые доступны в центре администрирования Microsoft 365. Для выполнения задач администрирования необходимо войти по учетной записи администратора клиента.

<div>

## <a name="moving-users-back-to-on-premises"></a>Перемещение пользователей на локальный сервер

<div class="">


> [!IMPORTANT]  
> Этот раздел относится только к пользователям, которые были созданы и включены в локальной среде Lync, а затем перенесено из локального развертывания в Lync Online. Если вы хотите переместить пользователей, которые были созданы в Lync Online (и не включены для Lync в локальном развертывании), ознакомьтесь с разрешениями: <A href="lync-server-2013-moving-users-from-lync-online-to-lync-on-premises.md">Перемещение пользователей из Lync Online в локальное приложение Lync в Lync Server 2013</A>.



</div>

  - Чтобы переместить пользователя из Lync Online обратно в локальное Lync, выполните следующие командлеты:
    
       ```PowerShell
        $cred=Get-Credential
       ```
    
       ```PowerShell
        Move-CsUser -Identity username@contoso.com -Target localpool.contoso.com -Credential $cred -HostedMigrationOverrideUrl <URL>
       ```

В качестве параметра **HostedMigrationOverrideUrl** следует указать URL-адрес пула, где работает служба миграции с размещением, в следующем формате:

Https:// \<Pool FQDN\> /HostedMigration/hostedmigrationService.svc. Вы можете определить URL-адрес размещенной службы миграции, просмотрев URL-адрес панели управления Lync Online для своей учетной записи Microsoft 365 или Office 365.

**Определение URL-адреса размещенной службы миграции для организации Microsoft 365 или Office 365**

1.  Войдите в свою организацию в качестве администратора.

2.  Откройте **центр администрирования Lync**.

3.  В **центре администрирования Lync** выберите и скопируйте URL-адрес в адресной строке на **Lync.com**. Ниже показан возможны пример URL-адреса
    
    `https://webdir0a.online.lync.com/lscp/?language=en-US&tenantID=`

4.  После замены фрагмента **webdir** в URL-адресе фрагментом **admin** получается следующий результат:
    
    `https://admin0a.online.lync.com`

5.  Добавьте к URL-адресу следующую строку: **/HostedMigration/hostedmigrationservice.svc**.
    
    Итоговый URL-адрес, который служит значением параметра **HostedMigrationOverrideUrl**, должен выглядеть следующим образом:
    
    `https://admin0a.online.lync.com/HostedMigration/hostedmigrationservice.svc`

</div>

</div>

<span> </span>

</div>

</div>

</div>

