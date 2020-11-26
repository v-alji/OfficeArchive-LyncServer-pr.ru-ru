---
title: 'Lync Server 2013: создание и изменение маршрутов сетевого региона'
description: 'Lync Server 2013: создание и изменение маршрутов сетевого региона.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Creating or modifying network region routes
ms:assetid: 76993daa-76c2-4cec-8363-de8aebef0145
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg521016(v=OCS.15)
ms:contentKeyID: 48184540
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 89106c905419778776ea16341f247027d49f1195
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431430"
---
# <a name="creating-or-modifying-network-region-routes-in-lync-server-2013"></a><span data-ttu-id="7cd77-103">Создание и изменение маршрутов сетевого региона в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7cd77-103">Creating or modifying network region routes in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7cd77-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7cd77-104">

<span> </span></span></span>

<span data-ttu-id="7cd77-105">_**Тема последнего изменения:** 2012-10-08_</span><span class="sxs-lookup"><span data-stu-id="7cd77-105">_**Topic Last Modified:** 2012-10-08_</span></span>

<span data-ttu-id="7cd77-106">Каждый регион в конфигурации управления допуском звонков (CAC) должен иметь какой-либо способ получить доступ ко всем остальным регионам.</span><span class="sxs-lookup"><span data-stu-id="7cd77-106">Every region within a call admission control (CAC) configuration must have some way to access every other region.</span></span> <span data-ttu-id="7cd77-107">Несмотря на то, что ссылки на области устанавливают ограничения пропускной способности для подключений между регионами и представляют собой физические ссылки, маршрут определяет связанный путь, который будет проходить соединение между двумя областями.</span><span class="sxs-lookup"><span data-stu-id="7cd77-107">While region links set bandwidth limitations on the connections between regions and also represent the physical links, a route determines which linked path the connection will traverse from one region to another.</span></span> <span data-ttu-id="7cd77-108">Вы можете настроить маршруты к сетевым регионам с помощью панели управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="7cd77-108">You can use Lync Server Control Panel to configure network region routes.</span></span> <span data-ttu-id="7cd77-109">С помощью панели управления Lync Server вы можете создавать, изменять и удалять маршруты сетевого региона.</span><span class="sxs-lookup"><span data-stu-id="7cd77-109">From Lync Server Control Panel, you can create, modify, or delete a network region route.</span></span> <span data-ttu-id="7cd77-110">Этот раздел используется для создания и изменения маршрута сетевого региона.</span><span class="sxs-lookup"><span data-stu-id="7cd77-110">Use this topic to create or modify a network region route.</span></span> <span data-ttu-id="7cd77-111">Дополнительные сведения об удалении существующих маршрутов сетевого региона можно найти [в разделе Удаление маршрутов сетевого региона в Lync Server 2013](lync-server-2013-deleting-existing-network-region-routes.md).</span><span class="sxs-lookup"><span data-stu-id="7cd77-111">For details about deleting an existing network region routes, see [Deleting existing network region routes in Lync Server 2013](lync-server-2013-deleting-existing-network-region-routes.md).</span></span>

<div>

## <a name="to-create-a-network-region-route"></a><span data-ttu-id="7cd77-112">Чтобы создать маршрут к сетевому региону</span><span class="sxs-lookup"><span data-stu-id="7cd77-112">To create a network region route</span></span>

1.  <span data-ttu-id="7cd77-113">Войдите на любой компьютер, находящийся во внутреннем развертывании, с использованием учетной записи, входящей в группу RTCUniversalServerAdmins (или имеющей равнозначные права пользователя) либо назначенной роли CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="7cd77-113">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="7cd77-114">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="7cd77-114">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="7cd77-115">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="7cd77-115">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="7cd77-116">На панели навигации слева выберите пункт **Настройка сети** , а затем — пункт **путь к региону**.</span><span class="sxs-lookup"><span data-stu-id="7cd77-116">In the left navigation bar, click **Network Configuration** and then click **Region Route**.</span></span>

4.  <span data-ttu-id="7cd77-117">На странице " **регион** " нажмите кнопку **создать**.</span><span class="sxs-lookup"><span data-stu-id="7cd77-117">On the **Region Route** page, click **New**.</span></span>

5.  <span data-ttu-id="7cd77-118">В разделе **Новый маршрут** введите значение в поле **имя** .</span><span class="sxs-lookup"><span data-stu-id="7cd77-118">In **New Region Route**, type a value in the **Name** field.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="7cd77-119">Это значение должно быть уникальным в рамках развертывания Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="7cd77-119">This value must be unique within your Microsoft Lync Server 2013 deployment.</span></span>

    
    </div>

6.  <span data-ttu-id="7cd77-120">В раскрывающемся списке **сетевой регион \# 1** выберите один из двух областей, которые должны быть соединены этим маршрутом.</span><span class="sxs-lookup"><span data-stu-id="7cd77-120">From the **Network region \#1** drop-down list, select one of the two regions to be connected by this route.</span></span>

7.  <span data-ttu-id="7cd77-121">В раскрывающемся списке **сетевой регион \# 2** выберите другой регион для этого маршрута.</span><span class="sxs-lookup"><span data-stu-id="7cd77-121">From the **Network region \#2** drop-down list, select the other region for this route.</span></span> <span data-ttu-id="7cd77-122">Этот регион должен отличаться от региона, выбранного для сетевого региона \# 1.</span><span class="sxs-lookup"><span data-stu-id="7cd77-122">This region must be different from the region selected for Network region \#1.</span></span>

8.  <span data-ttu-id="7cd77-123">С помощью списка " **сетевой регион** " можно добавить в маршрут ссылки на регион.</span><span class="sxs-lookup"><span data-stu-id="7cd77-123">Use the **Network region links** list box to add region links to the route.</span></span> <span data-ttu-id="7cd77-124">Нажмите кнопку " **Добавить** ", чтобы открыть страницу **ссылки "регион** ".</span><span class="sxs-lookup"><span data-stu-id="7cd77-124">Click the **Add** button to display the **Region Link** page.</span></span> <span data-ttu-id="7cd77-125">Щелкните ссылку на регион, чтобы добавить в этот маршрут, и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="7cd77-125">Click a region link to add to this route, and then click **OK**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="7cd77-126">Нажмите кнопку <STRONG>Добавить</STRONG> , чтобы добавить ссылки, или выберите ссылку, а затем нажмите кнопку <STRONG>Удалить</STRONG> , чтобы удалить ссылку.</span><span class="sxs-lookup"><span data-stu-id="7cd77-126">Continue to click the <STRONG>Add</STRONG> button to add more links, or select a link and click <STRONG>Remove</STRONG> to remove a link.</span></span>

    
    </div>

9.  <span data-ttu-id="7cd77-127">Нажмите **Исполнить**.</span><span class="sxs-lookup"><span data-stu-id="7cd77-127">Click **Commit**.</span></span>

</div>

<div>

## <a name="to-modify-a-network-region-route"></a><span data-ttu-id="7cd77-128">Изменение маршрута сетевого региона</span><span class="sxs-lookup"><span data-stu-id="7cd77-128">To modify a network region route</span></span>

1.  <span data-ttu-id="7cd77-129">Войдите на любой компьютер, находящийся во внутреннем развертывании, с использованием учетной записи, входящей в группу RTCUniversalServerAdmins (или имеющей равнозначные права пользователя) либо назначенной роли CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="7cd77-129">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="7cd77-130">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="7cd77-130">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="7cd77-131">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="7cd77-131">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="7cd77-132">На панели навигации слева выберите пункт **Настройка сети** , а затем — пункт **путь к региону**.</span><span class="sxs-lookup"><span data-stu-id="7cd77-132">In the left navigation bar, click **Network Configuration** and then click **Region Route**.</span></span>

4.  <span data-ttu-id="7cd77-133">На странице " **регион** " щелкните маршрут региона, который вы хотите изменить.</span><span class="sxs-lookup"><span data-stu-id="7cd77-133">On the **Region Route** page, click the region route that you want to modify.</span></span>

5.  <span data-ttu-id="7cd77-134">В меню **Правка** щелкните **Подробнее**.</span><span class="sxs-lookup"><span data-stu-id="7cd77-134">On the **Edit** menu, click **Show details**.</span></span>

6.  <span data-ttu-id="7cd77-135">В окне " **изменить маршрут области**" можно изменить регионы, Соединенные этим маршрутом, и ссылки на области, связанные с этим маршрутом.</span><span class="sxs-lookup"><span data-stu-id="7cd77-135">In **Edit Region Route**, you can modify the regions joined by this route and the region links associated with the route.</span></span>

7.  <span data-ttu-id="7cd77-136">Нажмите **Исполнить**.</span><span class="sxs-lookup"><span data-stu-id="7cd77-136">Click **Commit**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="7cd77-137">См. также</span><span class="sxs-lookup"><span data-stu-id="7cd77-137">See Also</span></span>


[<span data-ttu-id="7cd77-138">Удаление существующих маршрутов сетевого региона в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7cd77-138">Deleting existing network region routes in Lync Server 2013</span></span>](lync-server-2013-deleting-existing-network-region-routes.md)  
  

<span data-ttu-id="7cd77-139"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7cd77-139"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

