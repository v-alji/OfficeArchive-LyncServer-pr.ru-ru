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
# <a name="configuring-your-lync-server-2013-environment-for-the-lync-room-system-administrative-web-portal"></a><span data-ttu-id="71e3d-103">Configuring your Lync Server 2013 environment for the Lync Room System Administrative Web Portal</span><span class="sxs-lookup"><span data-stu-id="71e3d-103">Configuring your Lync Server 2013 environment for the Lync Room System Administrative Web Portal</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="71e3d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="71e3d-104">

<span> </span></span></span>

<span data-ttu-id="71e3d-105">_**Тема последнего изменения:** 2014-05-22_</span><span class="sxs-lookup"><span data-stu-id="71e3d-105">_**Topic Last Modified:** 2014-05-22_</span></span>

<span data-ttu-id="71e3d-106">Чтобы использовать веб-портал для управления комнатой на Lync (LRS), необходимо установить или настроить следующие необходимые компоненты.</span><span class="sxs-lookup"><span data-stu-id="71e3d-106">To use the Lync Room System (LRS) Administrative Web Portal, you will need to install or configure the following prerequisites.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="71e3d-107">Если сервер настроен на проверку подлинности Kerberos и NTLM и LRS запущен на компьютере, который не подключен к домену, проверка подлинности Kerberos не будет выполнена, и пользователь не увидит состояние LRS на административном портале.</span><span class="sxs-lookup"><span data-stu-id="71e3d-107">If the server is configured with both Kerberos and NTLM authentication, and LRS is running on a computer that is not joined to the domain, Kerberos authentication will fail and the user will not see the status of LRS in the administrative portal.</span></span> <span data-ttu-id="71e3d-108">Чтобы устранить эту проблему, настройте сервер для проверки подлинности NTLM либо проверки подлинности NTLM и TLS-DSK (без Kerberos) либо Присоедините компьютер LRS к домену.</span><span class="sxs-lookup"><span data-stu-id="71e3d-108">To resolve this issue, configure the server with NTLM authentication or both NTLM and TLS-DSK authentication (without Kerberos), or join the LRS computer to the domain.</span></span>



</div>

1.  <span data-ttu-id="71e3d-109">Установка накопительных обновлений для Lync Server 2013: Июль 2013 в топологии Lync Server.</span><span class="sxs-lookup"><span data-stu-id="71e3d-109">Install Lync Server 2013 Cumulative Updates: July 2013 in the Lync Server topology.</span></span>
    
    <span data-ttu-id="71e3d-110">Чтобы получить обновление или просмотреть сведения о том, что входит в состав этого приложения, ознакомьтесь со статьей [Обновление для Lync Server 2013](https://go.microsoft.com/fwlink/p/?linkid=323959).</span><span class="sxs-lookup"><span data-stu-id="71e3d-110">To get the update or see what’s included with it, see [Updates for Lync Server 2013](https://go.microsoft.com/fwlink/p/?linkid=323959).</span></span>

2.  <span data-ttu-id="71e3d-111">Создайте учетную запись пользователя Active Directory с включенной поддержкой SIP.</span><span class="sxs-lookup"><span data-stu-id="71e3d-111">Create a SIP-enabled Active Directory user.</span></span>
    
    <span data-ttu-id="71e3d-112">На веб-портале LRS администрирования эти учетные данные используются для запроса данных с сервера Lync Server.</span><span class="sxs-lookup"><span data-stu-id="71e3d-112">The LRS Administrative Web Portal uses these credentials to query information from Lync Server.</span></span> <span data-ttu-id="71e3d-113">Рекомендуемое имя пользователя — LRSApp.</span><span class="sxs-lookup"><span data-stu-id="71e3d-113">The recommended username is LRSApp.</span></span>

3.  <span data-ttu-id="71e3d-114">Создайте группу безопасности Active Directory с именем LRSSupportAdminGroup.</span><span class="sxs-lookup"><span data-stu-id="71e3d-114">Create an Active Directory security group with name LRSSupportAdminGroup.</span></span>
    
    <span data-ttu-id="71e3d-p103">Создайте группу с глобальной областью действия и типом "Безопасность". Пользователи с включенной поддержкой SIP, добавляемые в эту группу, будут автоматически получать разрешения на просмотр списка комнат и выполнение определенных команд, таких как ведение журналов.</span><span class="sxs-lookup"><span data-stu-id="71e3d-p103">Create the group with Group Scope as Global and Group Type as Security. SIP enabled users who are added to this group will be authorized to see the list of rooms and execute certain commands, such as collecting logs.</span></span>

4.  <span data-ttu-id="71e3d-117">Создайте группу безопасности Active Directory с именем LRSFullAccessAdminGroup. </span><span class="sxs-lookup"><span data-stu-id="71e3d-117">Create an Active Directory security group with name LRSFullAccessAdminGroup.</span></span>
    
    <span data-ttu-id="71e3d-118">Создание группы с областью группировки в качестве глобальных и группового типа как "безопасность". Пользователи, добавленные в эту группу, имеют разрешение на использование всех функций портала администрирования.</span><span class="sxs-lookup"><span data-stu-id="71e3d-118">Create the group with Group Scope as Global and Group Type as Security.SIP enabled users who are added to this group are authorized to use all admin portal functionality.</span></span>
    
     
    
    <span data-ttu-id="71e3d-119">![Список групп администрирования с ролью группы безопасности](images/Dn436325.5d432819-a2e2-452c-bc2a-5d4ee79d8c33(OCS.15).png "Список групп администрирования с ролью группы безопасности")</span><span class="sxs-lookup"><span data-stu-id="71e3d-119">![List of Admin Groups with security group role](images/Dn436325.5d432819-a2e2-452c-bc2a-5d4ee79d8c33(OCS.15).png "List of Admin Groups with security group role")</span></span>  
    
     

5.  <span data-ttu-id="71e3d-120">Добавьте LRSFullAccessAdminGroup в качестве участника LRSSupportAdminGroup.</span><span class="sxs-lookup"><span data-stu-id="71e3d-120">Add LRSFullAccessAdminGroup as a member of LRSSupportAdminGroup.</span></span>
    
    <span data-ttu-id="71e3d-121">![Свойства LRSSupportAdminGroup, страница участников](images/Dn436325.91a4a28a-cacf-4ef6-aac1-915ec41c9648(OCS.15).png "Свойства LRSSupportAdminGroup, страница участников")</span><span class="sxs-lookup"><span data-stu-id="71e3d-121">![LRSSupportAdminGroup Properties Members page](images/Dn436325.91a4a28a-cacf-4ef6-aac1-915ec41c9648(OCS.15).png "LRSSupportAdminGroup Properties Members page")</span></span>  
    
     

6.  <span data-ttu-id="71e3d-122">Создайте пользователя Active Directory с поддержкой возможностей SIP и именем LRSSupport.</span><span class="sxs-lookup"><span data-stu-id="71e3d-122">Create a SIP enabled Active Directory user with name LRSSupport.</span></span> <span data-ttu-id="71e3d-123">Добавьте его в группу LRSSupportAdminGroup.</span><span class="sxs-lookup"><span data-stu-id="71e3d-123">Add this user to LRSSupportAdminGroup.</span></span>
    
    <span data-ttu-id="71e3d-124">![Свойства LRSSupportAdminGroup, страница участников](images/Dn436325.7638055d-22ac-4909-914d-1966f5623909(OCS.15).png "Свойства LRSSupportAdminGroup, страница участников")</span><span class="sxs-lookup"><span data-stu-id="71e3d-124">![LRSSupportAdminGroup Properties Members page](images/Dn436325.7638055d-22ac-4909-914d-1966f5623909(OCS.15).png "LRSSupportAdminGroup Properties Members page")</span></span>  
    
     

7.  <span data-ttu-id="71e3d-125">Установите ASP.NET MVC 4 для Visual Studio 2010 с пакетом обновления 1 (SP1) и Visual Web Developer 2010 SP1, который можно найти в центре загрузки Майкрософт по адресу [https://go.microsoft.com/fwlink/p/?LinkId=323967](https://go.microsoft.com/fwlink/p/?linkid=323967) .</span><span class="sxs-lookup"><span data-stu-id="71e3d-125">Install ASP.NET MVC 4 for Visual Studio 2010 SP1 and Visual Web Developer 2010 SP1, available in the Microsoft Download Center at [https://go.microsoft.com/fwlink/p/?LinkId=323967](https://go.microsoft.com/fwlink/p/?linkid=323967).</span></span>

<span data-ttu-id="71e3d-126"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="71e3d-126"></div>

<span> </span>

</div>

</div>

</span></span></div>

