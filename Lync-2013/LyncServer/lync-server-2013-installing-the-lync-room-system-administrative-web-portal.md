---
title: 'Lync Server 2013: Установка системы управления комнатой на Lync Web портал'
description: 'Lync Server 2013: Установка системы управления комнатой на Lync Web портал.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Installing the Lync Room System Administrative Web Portal
ms:assetid: dd19e368-c338-4e21-a40d-6439d46a9748
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn436326(v=OCS.15)
ms:contentKeyID: 56737622
ms.date: 04/09/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0fba239346d75142bb4009c58e0ac67e8e1f3bcb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427007"
---
# <a name="installing-the-lync-room-system-administrative-web-portal-in-lync-server-2013"></a>Installing the Lync Room System Administrative Web Portal in Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2015-04-09_

Вы можете скачать веб-портал для Microsoft Lync Room System из центра загрузки Майкрософт по адресу [https://go.microsoft.com/fwlink/p/?LinkId=324044](https://go.microsoft.com/fwlink/p/?linkid=324044) .

Чтобы установить веб-портал для управления комнатой на Lync, выполните указанные ниже действия.

1.  Настройте порт доверенного приложения, выполнив следующий командлет в командной консоли Lync Server.
    
        Set-CsWebServer -Identity POOLFQDN -MeetingRoomAdminPortalInternalListeningPort 4456 -MeetingRoomAdminPortalExternalListeningPort 4457

2.  Чтобы установить портал комнаты для собраний, скачайте **LyncRoomAdminPortal.exe** и запустите его в качестве администратора.

3.  Откройте файл Web.config в следующей папке:
    
    % Program Files% \\ Microsoft Lync Server 2013 \\ веб-компоненты для \\ собраний портал комнаты \\ \\\\

4.  В файле Web.Config измените PortalUserName на имя пользователя, созданное на этапе 2, в разделе "Настройка предварительных требований для портала администрирования системы комнат в Lync" (рекомендуемое имя на этапе — LRSApp):
    
        <add key="PortalUserName" value="sip:LRSApp@domain.com" />

5.  Поскольку портал администрирования LRS является надежным приложением, вам не нужно указывать пароль в конфигурации портала. Если этот пользователь использует регистратор, отличный от локального, необходимо указать регистратор, добавив в файл Web.Config следующую строку:
    
        <add key="PortalUserRegistrarFQDN" value="pool-xxxx.domain.com" />

6.  Если используется порт, отличный от 5061, добавьте в файл Web.Config следующую строку: 
    
        <add key="PortalUserRegistrarPort" value="5061" />

<div>

## <a name="verifying-installation-of-the-lync-room-system-administrative-web-portal"></a>Проверка установки системы управления комнатой Lync Web портал

Чтобы проверить, установлен ли веб-портал для управления комнатой на Lync, выполните указанные ниже действия.


1.  Откройте следующий URL-адрес на сервере переднего плана:
    
    https:// \<fe-server\> /LRS
    
    При этом не должно выводиться никаких сообщений об ошибках, как на следующем рисунке:
    
    ![Экран входа в портал администрирования системы комнат Lync](images/Dn436326.050bcf70-2f3b-46b2-9b96-ebd12679b713(OCS.15).png "Экран входа в портал администрирования системы комнат Lync")

2.  Если никаких сообщений при этом не выводится, попробуйте перейти по следующему URL-адресу с любого другого компьютера в топологии:
    
    https:// \<fe-server\> /LRS
    
    Для доступа к странице вам потребуется добавить записи DNS, как описано в разделе "необходимые записи DNS для автоматического входа в клиент" [https://go.microsoft.com/fwlink/p/?LinkId=318056](https://go.microsoft.com/fwlink/p/?linkid=318056) .

</div>

</div>

<span> </span>

</div>

</div>

</div>

