---
title: 'Lync Server 2013: тестирование развертывания пула'
description: 'Lync Server 2013: Проверьте развертывание пула.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test the pool deployment
ms:assetid: ffd80617-155a-4041-bbeb-74503e7938dd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413092(v=OCS.15)
ms:contentKeyID: 48185976
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 28101a252eda5048ded9f1eaf76c092c5cb7f986
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444233"
---
# <a name="test-the-pool-deployment-in-lync-server-2013"></a><span data-ttu-id="3378f-103">Тестирование развертывания пула в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3378f-103">Test the pool deployment in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3378f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3378f-104">

<span> </span></span></span>

<span data-ttu-id="3378f-105">_**Тема последнего изменения:** 2013-09-25_</span><span class="sxs-lookup"><span data-stu-id="3378f-105">_**Topic Last Modified:** 2013-09-25_</span></span>

<span data-ttu-id="3378f-106">Ниже описана процедура проверки развертывания пула переднего плана.</span><span class="sxs-lookup"><span data-stu-id="3378f-106">The following procedure describes how to test the deployment of the Front End pool.</span></span>

<div>

## <a name="to-test-the-pool-deployment"></a><span data-ttu-id="3378f-107">Проверка развертывания пула</span><span class="sxs-lookup"><span data-stu-id="3378f-107">To test the pool deployment</span></span>

1.  <span data-ttu-id="3378f-108">С помощью оснасток "пользователи и компьютеры Active Directory" можно добавить объект "пользователи Active Directory" роли "Администратор" для развертывания Lync Server 2013 (на котором установлена панель управления Lync Server 2013) в группу **CSAdministrator** .</span><span class="sxs-lookup"><span data-stu-id="3378f-108">Use Active Directory Computers and Users to add the Active Directory user object of the administrator role for the Lync Server 2013 deployment (on which Lync Server 2013 Control Panel is installed) to the **CSAdministrator** group.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="3378f-109">Если вы не добавите соответствующих пользователей и группы в группу CsAdministors, то при открытии панели управления Lync Server появляется сообщение об ошибке, в котором говорится о том, что отказано в доступе из-за сбоя авторизации управления доступом на основе ролей (RBAC).</span><span class="sxs-lookup"><span data-stu-id="3378f-109">If you do not add the appropriate users and groups to the CsAdministors group, you will receive an error when opening Lync Server Control Panel, which states that “Unauthorized: Access is denied due to a role-based access control (RBAC) authorization failure.”</span></span>

    
    </div>

2.  <span data-ttu-id="3378f-110">Если объект-пользователь уже выполнил вход в систему, выйдите из системы, а затем повторите вход, чтобы зарегистрировать назначение новой группы.</span><span class="sxs-lookup"><span data-stu-id="3378f-110">If the user object is currently logged on, log off and then log on again to register the new group assignment.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="3378f-111">Учетная запись пользователя не может быть локальным администратором любого сервера, на котором работает Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3378f-111">The user account cannot be the local administrator of any server running Lync Server 2013.</span></span>

    
    </div>

3.  <span data-ttu-id="3378f-112">Войдите в систему с помощью учетной записи администратора на компьютере, на котором установлена панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="3378f-112">Use the administrative account to log on to the computer where Lync Server Control Panel is installed.</span></span>

4.  <span data-ttu-id="3378f-113">Откройте панель управления Lync Server и укажите учетные данные при появлении соответствующего запроса.</span><span class="sxs-lookup"><span data-stu-id="3378f-113">Start Lync Server Control Panel, and then provide credentials, if prompted.</span></span> <span data-ttu-id="3378f-114">На панели управления сервера Lync Server выводятся сведения о развертывании.</span><span class="sxs-lookup"><span data-stu-id="3378f-114">Lync Server Control Panel displays deployment information.</span></span>

5.  <span data-ttu-id="3378f-115">На панели навигации слева выберите пункт **топология** и убедитесь, что состояние службы отображается на компьютере с зеленой стрелкой и рядом с каждой ролью сервера Lync Server, которая была развернута и переведена в сеть, находится зеленая галочка для состояния репликации.</span><span class="sxs-lookup"><span data-stu-id="3378f-115">In the left navigation bar, click **Topology**, and then confirm that the service status shows a computer with a green arrow and that a green check mark for replication status is next to each Lync Server server role that has been deployed and brought online.</span></span>

6.  <span data-ttu-id="3378f-116">В левой панели навигации щелкните элемент **Пользователи**, а затем **Включить пользователей**.</span><span class="sxs-lookup"><span data-stu-id="3378f-116">In the left navigation bar, click **Users**, and then click **Enable users**.</span></span>

7.  <span data-ttu-id="3378f-117">На странице **Новый пользователь Lync Server** нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="3378f-117">On the **New Lync Server User** page, click **Add**.</span></span>

8.  <span data-ttu-id="3378f-118">Чтобы определить параметры поиска для объектов, на странице **Выбор из Active Directory** можно щелкнуть меню **Поиск** и выбрать пункт **Добавить фильтр** (необязательно).</span><span class="sxs-lookup"><span data-stu-id="3378f-118">To define search parameters for the objects you want to find, on the **Select from Active Directory** page, you can select **Search**, and then optionally click **Add Filter**.</span></span> <span data-ttu-id="3378f-119">Можно также выбрать команду **Поиск LDAP** и ввести выражение LDAP для фильтрации или ограничения числа возвращаемых объектов.</span><span class="sxs-lookup"><span data-stu-id="3378f-119">You can also select **LDAP search** and enter an LDAP expression to filter or limit the objects that will be returned.</span></span> <span data-ttu-id="3378f-120">Определив параметры поиска, Clink **найти**.</span><span class="sxs-lookup"><span data-stu-id="3378f-120">After you have decided on your Search options, clink **Find**.</span></span>

9.  <span data-ttu-id="3378f-121">В области результаты поиска выберите все объекты для этого сеанса поиска, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="3378f-121">In the Search results pane, select all the objects for this search session, and then click **OK**.</span></span>

10. <span data-ttu-id="3378f-122">На странице **нового пользователя Lync Server** выделенные объекты отображаются в окне **Пользователи** .</span><span class="sxs-lookup"><span data-stu-id="3378f-122">On the **New Lync Server User** page, the object or objects you selected are in the **Users** display.</span></span> <span data-ttu-id="3378f-123">В списке **Назначение пользователей группе** выберите сервер, на котором должны быть размещены объекты.</span><span class="sxs-lookup"><span data-stu-id="3378f-123">In the **Assign users to a pool** list, select the server where the objects should be homed.</span></span>
    
    <span data-ttu-id="3378f-124">Ниже приведены некоторые параметры для настройки объектов.</span><span class="sxs-lookup"><span data-stu-id="3378f-124">Following are a number of options for configuring the objects.</span></span>
    
      - <span data-ttu-id="3378f-125">**Создать пользовательский URI для SIP**,</span><span class="sxs-lookup"><span data-stu-id="3378f-125">**Generate user’s SIP URI**</span></span>
    
      - <span data-ttu-id="3378f-126">**Телефония**</span><span class="sxs-lookup"><span data-stu-id="3378f-126">**Telephony**</span></span>
    
      - <span data-ttu-id="3378f-127">**Line URI (URI линии)**,</span><span class="sxs-lookup"><span data-stu-id="3378f-127">**Line URI**</span></span>
    
      - <span data-ttu-id="3378f-128">**Политика конференц-связи**,</span><span class="sxs-lookup"><span data-stu-id="3378f-128">**Conferencing policy**</span></span>
    
      - <span data-ttu-id="3378f-129">**Политика версий клиентов**,</span><span class="sxs-lookup"><span data-stu-id="3378f-129">**Client version policy**</span></span>
    
      - <span data-ttu-id="3378f-130">**Политика ПИН-кода**,</span><span class="sxs-lookup"><span data-stu-id="3378f-130">**PIN policy**</span></span>
    
      - <span data-ttu-id="3378f-131">**Политика внешнего доступа**,</span><span class="sxs-lookup"><span data-stu-id="3378f-131">**External access policy**</span></span>
    
      - <span data-ttu-id="3378f-132">**Политика архивации**,</span><span class="sxs-lookup"><span data-stu-id="3378f-132">**Archiving policy**</span></span>
    
      - <span data-ttu-id="3378f-133">**Политика расположения**,</span><span class="sxs-lookup"><span data-stu-id="3378f-133">**Location policy**</span></span>
    
      - <span data-ttu-id="3378f-134">**Политика клиента**.</span><span class="sxs-lookup"><span data-stu-id="3378f-134">**Client policy**</span></span>
    
    <span data-ttu-id="3378f-135">Для целей тестирования основных функций выберите предпочтительный параметр для **URI-адресу для пользовательского** интерфейса (другие параметры в конфигурации будут использовать параметры по умолчанию), а затем нажмите кнопку **включить**.</span><span class="sxs-lookup"><span data-stu-id="3378f-135">For the purposes of testing the basic functionality, select the option you prefer for the **Generate user’s SIP URI** setting (the other options in the configuration will use default settings), and then click **Enable**.</span></span>

11. <span data-ttu-id="3378f-136">Откроется страница со сводкой, на которой показан флажок в столбце **Enabled** , указывающий на то, что объекты теперь готовы к использованию.</span><span class="sxs-lookup"><span data-stu-id="3378f-136">A summary page is displayed that shows a check mark in the **Enabled** column to indicate that the objects are now ready for use.</span></span> <span data-ttu-id="3378f-137">В столбце **SIP-адрес** будет отображаться адрес, который требуется для настройки входа пользователя.</span><span class="sxs-lookup"><span data-stu-id="3378f-137">The **SIP address** column displays the address you need for the user sign-in configuration.</span></span>

12. <span data-ttu-id="3378f-138">Зарегистрируйте одного пользователя на компьютере, который присоединен к домену, а также на другом компьютере домена.</span><span class="sxs-lookup"><span data-stu-id="3378f-138">Log one user on to a computer that is joined to the domain, and another user on to another computer in the domain.</span></span>

13. <span data-ttu-id="3378f-139">Установите Lync 2013 на каждом из двух клиентских компьютеров, а затем убедитесь, что оба пользователя могут входить в Lync Server 2013 и обмениваться мгновенными сообщениями друг с другом.</span><span class="sxs-lookup"><span data-stu-id="3378f-139">Install Lync 2013 on each of the two client computers, and then verify that both users can sign in to Lync Server 2013 and can send instant messages to each other.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="3378f-140">См. также</span><span class="sxs-lookup"><span data-stu-id="3378f-140">See Also</span></span>


[<span data-ttu-id="3378f-141">Развертывание клиентов и устройств в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3378f-141">Deploying clients and devices in Lync Server 2013</span></span>](lync-server-2013-deploying-clients-and-devices.md)  
  

<span data-ttu-id="3378f-142"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3378f-142"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

