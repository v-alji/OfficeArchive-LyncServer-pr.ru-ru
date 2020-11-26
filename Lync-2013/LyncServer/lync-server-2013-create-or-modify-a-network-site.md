---
title: 'Lync Server 2013: создание или изменение сетевого сайта'
description: 'Lync Server 2013: создание или изменение сайта сети.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or modify a network site
ms:assetid: 14e24856-9996-4da4-9f31-300940bdf5aa
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398218(v=OCS.15)
ms:contentKeyID: 48183488
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c4db9080f866becfcb94972787e099a69eac28c9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431794"
---
# <a name="create-or-modify-a-network-site-in-lync-server-2013"></a><span data-ttu-id="ca550-103">Создание или изменение сетевого сайта в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ca550-103">Create or modify a network site in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ca550-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ca550-104">

<span> </span></span></span>

<span data-ttu-id="ca550-105">_**Тема последнего изменения:** 2013-02-24_</span><span class="sxs-lookup"><span data-stu-id="ca550-105">_**Topic Last Modified:** 2013-02-24_</span></span>

<span data-ttu-id="ca550-106">Управление допуском звонков (CAC), E9-1-1, а для обхода мультимедийных развертываний используются *Сетевые сайты* , определенные внутри и всегда связанные с сетевым регионом.</span><span class="sxs-lookup"><span data-stu-id="ca550-106">Call admission control (CAC), E9-1-1, and media bypass deployments rely on the configuration of *network sites* which are defined within and always associated with a network region.</span></span> <span data-ttu-id="ca550-107">Сетевой сайт представляет местонахождение офиса подразделения, набор зданий или кампус.</span><span class="sxs-lookup"><span data-stu-id="ca550-107">A network site represents a branch office location, a set of buildings, or a campus.</span></span> <span data-ttu-id="ca550-108">Сетевые сайты представляют собой коллекции подсетей с одинаковой пропускной способностью.</span><span class="sxs-lookup"><span data-stu-id="ca550-108">Network sites represent collections of subnets with similar bandwidth.</span></span>

<span data-ttu-id="ca550-109">Чтобы создать или изменить сетевые сайты, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="ca550-109">Use the following procedures to create or modify network sites.</span></span> <span data-ttu-id="ca550-110">Например, если вы уже создали сетевые сайты для одной голосовой связи, вам не нужно создавать новые сетевые сайты; другие функции голосовой связи будут использовать те же сайты.</span><span class="sxs-lookup"><span data-stu-id="ca550-110">For example, if you have already created network sites for one Voice feature, you do not need to create new network sites; other Voice features will use those same sites.</span></span> <span data-ttu-id="ca550-111">You may, however, need to modify an existing network site definition to apply feature-specific settings.</span><span class="sxs-lookup"><span data-stu-id="ca550-111">You may, however, need to modify an existing network site definition to apply feature-specific settings.</span></span> <span data-ttu-id="ca550-112">For example, if you created a network site for E9-1-1, you need to modify the network site during deployment of call admission control to apply a bandwidth policy profile.</span><span class="sxs-lookup"><span data-stu-id="ca550-112">For example, if you created a network site for E9-1-1, you need to modify the network site during deployment of call admission control to apply a bandwidth policy profile.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="ca550-113">Там, где они есть, вы можете найти конкретные примеры и требования к сетевым сайтам, которые относятся к дополнительным функциям голосовой связи в документации по развертыванию для каждой из функций.</span><span class="sxs-lookup"><span data-stu-id="ca550-113">Where they exist, you can find specific examples and requirements for network sites as they pertain to an advanced Voice feature in the Deployment documentation for each feature:</span></span> 
> <UL>
> <LI>
> <P><span data-ttu-id="ca550-114"><A href="lync-server-2013-configure-network-sites-for-cac.md">Настройка сетевых сайтов для CAC в Lync Server 2013</A></span><span class="sxs-lookup"><span data-stu-id="ca550-114"><A href="lync-server-2013-configure-network-sites-for-cac.md">Configure network sites for CAC in Lync Server 2013</A></span></span></P></LI></UL>



</div>

<span data-ttu-id="ca550-115">Дополнительные сведения о работе с сетевыми сайтами можно найти в документации по оболочке Lync Server Management Shell для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="ca550-115">For details about working with network sites, see the Lync Server Management Shell documentation for the following cmdlets:</span></span>

  - [<span data-ttu-id="ca550-116">New-CsNetworkSite</span><span class="sxs-lookup"><span data-stu-id="ca550-116">New-CsNetworkSite</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkSite)

  - [<span data-ttu-id="ca550-117">Get-CsNetworkSite</span><span class="sxs-lookup"><span data-stu-id="ca550-117">Get-CsNetworkSite</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkSite)

  - [<span data-ttu-id="ca550-118">Set-CsNetworkSite</span><span class="sxs-lookup"><span data-stu-id="ca550-118">Set-CsNetworkSite</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsNetworkSite)

  - [<span data-ttu-id="ca550-119">Remove-CsNetworkSite</span><span class="sxs-lookup"><span data-stu-id="ca550-119">Remove-CsNetworkSite</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsNetworkSite)

<div>

## <a name="create-a-network-site"></a><span data-ttu-id="ca550-120">Создание сайта сети</span><span class="sxs-lookup"><span data-stu-id="ca550-120">Create a Network Site</span></span>

<span data-ttu-id="ca550-121">Создание сетевого региона, который может использоваться для управления допуском звонков, E9-1-1 или мультимедийного обхода.</span><span class="sxs-lookup"><span data-stu-id="ca550-121">Create a network region that can be used by call admission control, E9-1-1, or media bypass.</span></span>

<div>

## <a name="to-create-a-network-site-by-using-management-shell"></a><span data-ttu-id="ca550-122">Создание сетевого сайта с помощью командной консоли</span><span class="sxs-lookup"><span data-stu-id="ca550-122">To create a network site by using Management Shell</span></span>

1.  <span data-ttu-id="ca550-123">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="ca550-123">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="ca550-124">Выполните командлет New-CsNetworkSite для создания областей сети:</span><span class="sxs-lookup"><span data-stu-id="ca550-124">Run the New-CsNetworkSite cmdlet to create network sites:</span></span>
    
        New-CsNetworkSite -NetworkSiteID <string>
    
    <span data-ttu-id="ca550-125">Например:</span><span class="sxs-lookup"><span data-stu-id="ca550-125">For example:</span></span>
    
        New-CsNetworkSite -NetworkSiteID Chicago -Description "Corporate headquarters"-NetworkRegionID NorthAmerica
    
    <span data-ttu-id="ca550-126">В этом примере создается сетевой узел с именем "Chicago" в области сети "NorthAmerica".</span><span class="sxs-lookup"><span data-stu-id="ca550-126">In this example, you created a network site called “Chicago” that is in the “NorthAmerica” network region.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="ca550-127">Чтобы эта команда выполнилась успешно, область сети NorthAmerica должна уже быть создана.</span><span class="sxs-lookup"><span data-stu-id="ca550-127">The NorthAmerica network region must already exist for this command to run successfully.</span></span>

    
    </div>

3.  <span data-ttu-id="ca550-128">Чтобы закончить создание сетевых узлов для вашей топологии, повторите действие 2 с параметрами других узлов.</span><span class="sxs-lookup"><span data-stu-id="ca550-128">To finish creating network sites for your topology, repeat step 2 with settings for other sites.</span></span>

</div>

<div>

## <a name="to-create-a-network-site-by-using-lync-server-control-panel"></a><span data-ttu-id="ca550-129">Создание сайта сети с помощью панели управления Lync Server</span><span class="sxs-lookup"><span data-stu-id="ca550-129">To create a network site by using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="ca550-130">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ca550-130">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="ca550-131">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="ca550-131">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

2.  <span data-ttu-id="ca550-132">В левой области навигации щелкните элемент **Конфигурация сети**.</span><span class="sxs-lookup"><span data-stu-id="ca550-132">In the left navigation bar, click **Network Configuration**.</span></span>

3.  <span data-ttu-id="ca550-133">Нажмите кнопку навигации **Сайт**.</span><span class="sxs-lookup"><span data-stu-id="ca550-133">Click the **Site** navigation button.</span></span>

4.  <span data-ttu-id="ca550-134">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="ca550-134">Click **New**.</span></span>

5.  <span data-ttu-id="ca550-135">На странице **Создать сайт** выберите поле **Имя** и введите имя для сетевого сайта.</span><span class="sxs-lookup"><span data-stu-id="ca550-135">On the **New Site** page, click **Name** and then type a name for the network site.</span></span>

6.  <span data-ttu-id="ca550-136">Нажмите пункт **Область** и выберите в списке нужную область.</span><span class="sxs-lookup"><span data-stu-id="ca550-136">Click **Region**, and then click a region in the list.</span></span>

7.  <span data-ttu-id="ca550-137">Дополнительно можно выбрать пункт **Политика пропускной способности** и выбрать нужную политику в списке.</span><span class="sxs-lookup"><span data-stu-id="ca550-137">Optionally, click **Bandwidth policy**, and then click a bandwidth policy in the list.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="ca550-138">Политика пропускной способности требуется только в том случае, если в узле разворачивается контроль допуска звонков.</span><span class="sxs-lookup"><span data-stu-id="ca550-138">Bandwidth policy is required only if you deploy call admission control at the site.</span></span>

    
    </div>

8.  <span data-ttu-id="ca550-139">Дополнительно можно выбрать пункт **Политика местонахождения** и выбрать нужную политику местонахождения в списке.</span><span class="sxs-lookup"><span data-stu-id="ca550-139">Optionally, click **Location policy**, and then click a location policy in the list.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="ca550-140">Политика местонахождения требуется только в том случае, если в узле разворачивается служба E9-1-1.</span><span class="sxs-lookup"><span data-stu-id="ca550-140">Location policy is required only if you deploy E9-1-1 at the site.</span></span>

    
    </div>

9.  <span data-ttu-id="ca550-141">В поле **Описание** введите дополнительные сведения об области сети (необязательно).</span><span class="sxs-lookup"><span data-stu-id="ca550-141">Optionally, click **Description**, and then type additional information to describe this network site.</span></span>

10. <span data-ttu-id="ca550-142">Нажмите **Исполнить**.</span><span class="sxs-lookup"><span data-stu-id="ca550-142">Click **Commit**.</span></span>

11. <span data-ttu-id="ca550-143">Чтобы завершить создание сетевых узлов для вашей топологии, повторите действия с 4 по 10 с параметрами для других узлов.</span><span class="sxs-lookup"><span data-stu-id="ca550-143">To finish creating network sites for your topology, repeat steps 4 through 10 with settings for other sites.</span></span>

</div>

</div>

<div>

## <a name="modify-a-network-site"></a><span data-ttu-id="ca550-144">Изменение сетевого сайта</span><span class="sxs-lookup"><span data-stu-id="ca550-144">Modify a Network Site</span></span>

<span data-ttu-id="ca550-145">Изменение сетевого региона, который может использоваться для управления допуском звонков, E9-1-1 или мультимедийного обхода.</span><span class="sxs-lookup"><span data-stu-id="ca550-145">Modify a network region that can be used by call admission control, E9-1-1, or media bypass.</span></span>

<div>

## <a name="to-modify-a-network-site"></a><span data-ttu-id="ca550-146">Изменение сетевого сайта</span><span class="sxs-lookup"><span data-stu-id="ca550-146">To modify a network site</span></span>

1.  <span data-ttu-id="ca550-147">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="ca550-147">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="ca550-148">Чтобы изменить сетевые узлы, выполните командлет Set-CsNetworkSite:</span><span class="sxs-lookup"><span data-stu-id="ca550-148">Run the Set-CsNetworkSite cmdlet to modify network sites:</span></span>
    
        Set-CsNetworkSite -Identity <string>
    
    <span data-ttu-id="ca550-149">Например:</span><span class="sxs-lookup"><span data-stu-id="ca550-149">For example:</span></span>
    
        Set-CsNetworkSite -Identity Albuquerque -NetworkRegionID NorthAmerica
    
    <span data-ttu-id="ca550-p104">В данном примере узел с именем "Albuquerque" перемещается в область сети "NorthAmerica". Чтобы изменить конфигурацию этого сетевого узла для развертывания контроля допуска звонков, E9-1-1 или обхода сервера-посредника, измените параметры сетевого узла, выполнив командлет Set-CsNetworkSite с параметром BWPolicyProfileID или LocationPolicy соответственно.</span><span class="sxs-lookup"><span data-stu-id="ca550-p104">In this example, the site called “Albuquerque” is moved to the “NorthAmerica” network region. To modify the network site configuration to deploy call admission control, E9-1-1, or media bypass, modify the network site settings by running the Set-CsNetworkSite cmdlet with the BWPolicyProfileID or LocationPolicy parameter, respectively.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="ca550-p105">Хотя для обхода сервера-посредника существует параметр BypassID, настоятельно рекомендуется не переопределять автоматически созданные идентификаторы обхода. Чтобы настроить сетевой узел для обхода сервера-посредника, указывать дополнительные параметры не требуется.</span><span class="sxs-lookup"><span data-stu-id="ca550-p105">Although the BypassID parameter exists for media bypass, we strongly recommend that you do not override automatically generated bypass IDs. You do not need to specify additional parameters to configure a network site for media bypass.</span></span>

    
    </div>

3.  <span data-ttu-id="ca550-154">Чтобы закончить изменение сетевых узлов для вашей топологии, повторите действие 2 с параметрами других узлов.</span><span class="sxs-lookup"><span data-stu-id="ca550-154">To finish modifying network sites for your topology, repeat step 2 with settings for other sites.</span></span>

</div>

<div>

## <a name="to-modify-a-network-site-by-using-lync-server-control-panel"></a><span data-ttu-id="ca550-155">Изменение сетевого сайта с помощью панели управления Lync Server</span><span class="sxs-lookup"><span data-stu-id="ca550-155">To modify a network site by using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="ca550-156">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ca550-156">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="ca550-157">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="ca550-157">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

2.  <span data-ttu-id="ca550-158">В левой области навигации щелкните элемент **Конфигурация сети**.</span><span class="sxs-lookup"><span data-stu-id="ca550-158">In the left navigation bar, click **Network Configuration**.</span></span>

3.  <span data-ttu-id="ca550-159">Нажмите кнопку навигации **Сайт**.</span><span class="sxs-lookup"><span data-stu-id="ca550-159">Click the **Site** navigation button.</span></span>

4.  <span data-ttu-id="ca550-160">Выберите в таблице сетевой узел, который требуется изменить.</span><span class="sxs-lookup"><span data-stu-id="ca550-160">In the table, click the network site that you want to modify.</span></span>

5.  <span data-ttu-id="ca550-161">Щелкните **Изменить**, затем щелкните **Подробнее**.</span><span class="sxs-lookup"><span data-stu-id="ca550-161">Click **Edit**, and then click **Show details…**.</span></span>

6.  <span data-ttu-id="ca550-162">На странице **Изменение сайта** соответствующим образом измените значения параметров для этого сетевого узла.</span><span class="sxs-lookup"><span data-stu-id="ca550-162">On the **Edit Site** page, change the values for this network site’s settings as appropriate.</span></span>

7.  <span data-ttu-id="ca550-163">Нажмите **Исполнить**.</span><span class="sxs-lookup"><span data-stu-id="ca550-163">Click **Commit**.</span></span>

8.  <span data-ttu-id="ca550-164">Чтобы завершить изменение сетевых узлов, повторите действия с 4 по 7 с параметрами для других узлов.</span><span class="sxs-lookup"><span data-stu-id="ca550-164">To finish modify network sites, repeat steps 4 through 7 with settings for other sites.</span></span>

<span data-ttu-id="ca550-165"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ca550-165"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

