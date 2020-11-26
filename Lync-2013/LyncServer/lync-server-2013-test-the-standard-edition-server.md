---
title: 'Lync Server 2013: тестирование сервера Standard Edition'
description: 'Lync Server 2013: Проверка сервера Standard Edition.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test the Standard Edition server
ms:assetid: b6ef67bb-9665-43e4-b8b3-eac8898eebf6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412890(v=OCS.15)
ms:contentKeyID: 48185220
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 35dc13fc01979cc8b293d0647a7886b7d65d7669
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441181"
---
# <a name="test-the-standard-edition-server-in-lync-server-2013"></a><span data-ttu-id="8a4c4-103">Тестирование сервера Standard Edition в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8a4c4-103">Test the Standard Edition server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8a4c4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8a4c4-104">

<span> </span></span></span>

<span data-ttu-id="8a4c4-105">_**Тема последнего изменения:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="8a4c4-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="8a4c4-106">Ниже описана процедура проверки развертывания сервера Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="8a4c4-106">The following procedure describes how to test the deployment of a Standard Edition server.</span></span>

<div>

## <a name="to-test-the-deployment-of-a-standard-edition-server"></a><span data-ttu-id="8a4c4-107">Тестирование развертывания стандартного сервера выпуска</span><span class="sxs-lookup"><span data-stu-id="8a4c4-107">To test the deployment of a Standard Edition Server</span></span>

1.  <span data-ttu-id="8a4c4-108">С помощью оснасток "пользователи и компьютеры Active Directory" можно добавить объект "пользователи Active Directory" роли "Администратор" для развертывания Lync Server 2013 (на котором установлена панель управления Lync Server) в группу **CSAdministrator** .</span><span class="sxs-lookup"><span data-stu-id="8a4c4-108">Use Active Directory Computers and Users to add the Active Directory user object of the administrator role for the Lync Server 2013 deployment (on which Lync Server Control Panel is installed) to the **CSAdministrator** group.</span></span>

2.  <span data-ttu-id="8a4c4-109">Если объект-пользователь уже выполнил вход в систему, выйдите из системы, а затем повторите вход, чтобы зарегистрировать назначение новой группы.</span><span class="sxs-lookup"><span data-stu-id="8a4c4-109">If the user object is currently logged on, log off and then log on again to register the new group assignment.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="8a4c4-110">Учетная запись пользователя не может быть локальным администратором сервера, на котором установлен Lync Server 2013, Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="8a4c4-110">The user account cannot be the local administrator of the server running Lync Server 2013, Standard Edition.</span></span> <span data-ttu-id="8a4c4-111">Если вы не добавите соответствующих пользователей и группы в группу CsAdministors, то при открытии панели управления Lync Server 2013 появляется сообщение об ошибке, в котором говорится о том, что отказано в доступе из-за сбоя авторизации управления доступом на основе ролей (RBAC).</span><span class="sxs-lookup"><span data-stu-id="8a4c4-111">If you do not add the appropriate users and groups to the CsAdministors group, you will receive an error when opening Lync Server 2013 Control Panel, which states that “Unauthorized: Access is denied due to a role-based access control (RBAC) authorization failure.”</span></span>

    
    </div>

3.  <span data-ttu-id="8a4c4-112">Войдите в систему с помощью учетной записи администратора на компьютере, на котором установлена панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="8a4c4-112">Use the administrative account to log on to the computer where Lync Server Control Panel is installed.</span></span>

4.  <span data-ttu-id="8a4c4-113">Откройте панель управления Lync Server и укажите учетные данные при появлении соответствующего запроса.</span><span class="sxs-lookup"><span data-stu-id="8a4c4-113">Start Lync Server Control Panel and provide credentials, if prompted.</span></span> <span data-ttu-id="8a4c4-114">На панели управления Lync Server 2013 отображаются сведения о развертывании.</span><span class="sxs-lookup"><span data-stu-id="8a4c4-114">Lync Server 2013 Control Panel displays deployment information.</span></span>

5.  <span data-ttu-id="8a4c4-115">На левой панели навигации щелкните **топология**, а затем убедитесь, что состояние службы — значок компьютера с зеленой стрелкой, и рядом с каждой ролью сервера Lync Server, которая была развернута и переведена в сеть, есть зеленая галочка.</span><span class="sxs-lookup"><span data-stu-id="8a4c4-115">In the left navigation bar, click **Topology**, and then confirm that the service status is a computer icon with a green arrow and there is a green check mark next to each Lync Server server role that has been deployed and brought online.</span></span>

6.  <span data-ttu-id="8a4c4-116">На панели навигации слева выберите пункт **Пользователи**, а затем включите два пользователя для Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="8a4c4-116">In the left navigation bar, click **Users**, and then enable the two users for Lync Server 2013.</span></span>

7.  <span data-ttu-id="8a4c4-117">Зарегистрируйте одного пользователя на компьютере, подключенном к домену, и на другой пользователь в домене.</span><span class="sxs-lookup"><span data-stu-id="8a4c4-117">Log one user on to a computer that is joined to the domain, and the other user on to another computer in the domain.</span></span>

8.  <span data-ttu-id="8a4c4-118">Установите Lync Server 2013 на каждом из двух клиентских компьютеров, а затем убедитесь, что оба пользователя могут входить в Lync Server 2013 и обмениваться мгновенными сообщениями друг с другом.</span><span class="sxs-lookup"><span data-stu-id="8a4c4-118">Install Lync Server 2013 on each of the two client computers, and then verify that both users can sign in to Lync Server 2013 and can send instant messages to each other.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="8a4c4-119">См. также</span><span class="sxs-lookup"><span data-stu-id="8a4c4-119">See Also</span></span>


[<span data-ttu-id="8a4c4-120">Развертывание клиентов и устройств в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8a4c4-120">Deploying clients and devices in Lync Server 2013</span></span>](lync-server-2013-deploying-clients-and-devices.md)  
  

<span data-ttu-id="8a4c4-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8a4c4-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

