---
title: 'Lync Server 2013: настройка среды для работы с веб-порталом администрирования системы комнат Lync'
description: 'Lync Server 2013: Настройка среды для веб-портала комнатной системы Lync.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring your environment for the Lync Room System Administrative Web Portal
ms:assetid: 1bf3cc55-cfa8-46ee-a8bc-6dab3bff76b2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn436325(v=OCS.15)
ms:contentKeyID: 56737623
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c942e1db799a7336a3eafb5571e82584694ddbf3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432305"
---
# <a name="configuring-your-lync-server-2013-environment-for-the-lync-room-system-administrative-web-portal"></a>Configuring your Lync Server 2013 environment for the Lync Room System Administrative Web Portal

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2014-05-22_

Чтобы использовать веб-портал для управления комнатой на Lync (LRS), необходимо установить или настроить следующие необходимые компоненты.

<div>


> [!IMPORTANT]  
> Если сервер настроен на проверку подлинности Kerberos и NTLM и LRS запущен на компьютере, который не подключен к домену, проверка подлинности Kerberos не будет выполнена, и пользователь не увидит состояние LRS на административном портале. Чтобы устранить эту проблему, настройте сервер для проверки подлинности NTLM либо проверки подлинности NTLM и TLS-DSK (без Kerberos) либо Присоедините компьютер LRS к домену.



</div>

1.  Установка накопительных обновлений для Lync Server 2013: Июль 2013 в топологии Lync Server.
    
    Чтобы получить обновление или просмотреть сведения о том, что входит в состав этого приложения, ознакомьтесь со статьей [Обновление для Lync Server 2013](https://go.microsoft.com/fwlink/p/?linkid=323959).

2.  Создайте учетную запись пользователя Active Directory с включенной поддержкой SIP.
    
    На веб-портале LRS администрирования эти учетные данные используются для запроса данных с сервера Lync Server. Рекомендуемое имя пользователя — LRSApp.

3.  Создайте группу безопасности Active Directory с именем LRSSupportAdminGroup.
    
    Создайте группу с глобальной областью действия и типом "Безопасность". Пользователи с включенной поддержкой SIP, добавляемые в эту группу, будут автоматически получать разрешения на просмотр списка комнат и выполнение определенных команд, таких как ведение журналов.

4.  Создайте группу безопасности Active Directory с именем LRSFullAccessAdminGroup. 
    
    Создание группы с областью группировки в качестве глобальных и группового типа как "безопасность". Пользователи, добавленные в эту группу, имеют разрешение на использование всех функций портала администрирования.
    
     
    
    ![Список групп администрирования с ролью группы безопасности](images/Dn436325.5d432819-a2e2-452c-bc2a-5d4ee79d8c33(OCS.15).png "Список групп администрирования с ролью группы безопасности")  
    
     

5.  Добавьте LRSFullAccessAdminGroup в качестве участника LRSSupportAdminGroup.
    
    ![Свойства LRSSupportAdminGroup, страница участников](images/Dn436325.91a4a28a-cacf-4ef6-aac1-915ec41c9648(OCS.15).png "Свойства LRSSupportAdminGroup, страница участников")  
    
     

6.  Создайте пользователя Active Directory с поддержкой возможностей SIP и именем LRSSupport. Добавьте его в группу LRSSupportAdminGroup.
    
    ![Свойства LRSSupportAdminGroup, страница участников](images/Dn436325.7638055d-22ac-4909-914d-1966f5623909(OCS.15).png "Свойства LRSSupportAdminGroup, страница участников")  
    
     

7.  Установите ASP.NET MVC 4 для Visual Studio 2010 с пакетом обновления 1 (SP1) и Visual Web Developer 2010 SP1, который можно найти в центре загрузки Майкрософт по адресу [https://go.microsoft.com/fwlink/p/?LinkId=323967](https://go.microsoft.com/fwlink/p/?linkid=323967) .

</div>

<span> </span>

</div>

</div>

</div>

