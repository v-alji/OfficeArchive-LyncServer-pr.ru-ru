---
title: 'Lync Server 2013: создание или изменение сетевого региона'
description: 'Lync Server 2013: создание или изменение сетевого региона.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or modify a network region
ms:assetid: bf7a3dc4-71a2-4559-a547-d90305d4f904
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412933(v=OCS.15)
ms:contentKeyID: 48185281
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a149a668f64df804d2631243d9bb63401bd8a284
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431808"
---
# <a name="create-or-modify-a-network-region-in-lync-server-2013"></a><span data-ttu-id="164f0-103">Создание или изменение сетевого региона в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="164f0-103">Create or modify a network region in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="164f0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="164f0-104">

<span> </span></span></span>

<span data-ttu-id="164f0-105">_**Тема последнего изменения:** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="164f0-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="164f0-106">*Регионы сетей* — это сетевые разветвители и одинарные кости, используемые в настройке управления допуском звонков, E9-1-1 и мультимедийными пропусками.</span><span class="sxs-lookup"><span data-stu-id="164f0-106">*Network regions* are the network hubs or backbones used in the configuration of call admission control, E9-1-1, and media bypass.</span></span> <span data-ttu-id="164f0-107">Для создания и изменения областей сети выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="164f0-107">Use the following procedures to create or modify network regions.</span></span> <span data-ttu-id="164f0-108">Например, если вы уже создали сетевые регионы для одной голосовой связи, вам не нужно создавать новые сетевые регионы; другие дополнительные функции для корпоративной голосовой связи будут использовать те же сетевые регионы.</span><span class="sxs-lookup"><span data-stu-id="164f0-108">For example, if you have already created network regions for one Voice feature, you do not need to create new network regions; other advanced Enterprise Voice features will use those same network regions.</span></span> <span data-ttu-id="164f0-109">Однако вам может потребоваться изменить существующее определение области сети для применения параметров, относящихся к функции.</span><span class="sxs-lookup"><span data-stu-id="164f0-109">You may, however, need to modify an existing network region definition to apply feature-specific settings.</span></span> <span data-ttu-id="164f0-110">Например, если вы создали области сети для службы E9-1-1, для которой не требуется связанный центральный сайт, и затем развернули службу контроля допуска звонков, вам потребуется изменить определения областей сети, чтобы указать центральный сайт.</span><span class="sxs-lookup"><span data-stu-id="164f0-110">For example, if you have created network regions for E9-1-1 (which do not require an associated central site) and you then deploy call admission control, you need to modify the network region definitions to specify a central site.</span></span> <span data-ttu-id="164f0-111">Подробности можно найти [в разделе Настройка регионов сети для CAC в Lync Server 2013](lync-server-2013-configure-network-regions-for-cac.md).</span><span class="sxs-lookup"><span data-stu-id="164f0-111">For details, see [Configure network regions for CAC in Lync Server 2013](lync-server-2013-configure-network-regions-for-cac.md).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="164f0-112">Любые особые требования к функциональным возможностям для определений сетевых областей описаны в разделе Развертывание для этой функции.</span><span class="sxs-lookup"><span data-stu-id="164f0-112">Any feature-specific requirements for network region definitions are documented in the Deployment topics for the feature.</span></span>



</div>

<span data-ttu-id="164f0-113">Дополнительные сведения о работе с сетевыми областями можно найти в документации по оболочке Lync Server Management Shell для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="164f0-113">For details about working with network regions, see the Lync Server Management Shell documentation for the following cmdlets:</span></span>

  - [<span data-ttu-id="164f0-114">New-CsNetworkRegion</span><span class="sxs-lookup"><span data-stu-id="164f0-114">New-CsNetworkRegion</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkRegion)

  - [<span data-ttu-id="164f0-115">Get-CsNetworkRegion</span><span class="sxs-lookup"><span data-stu-id="164f0-115">Get-CsNetworkRegion</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkRegionLink)

  - [<span data-ttu-id="164f0-116">Set-CsNetworkRegion</span><span class="sxs-lookup"><span data-stu-id="164f0-116">Set-CsNetworkRegion</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsNetworkRegion)

  - [<span data-ttu-id="164f0-117">Remove-CsNetworkRegion</span><span class="sxs-lookup"><span data-stu-id="164f0-117">Remove-CsNetworkRegion</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsNetworkRegion)

<div>

## <a name="create-a-network-region"></a><span data-ttu-id="164f0-118">Создание сетевого региона</span><span class="sxs-lookup"><span data-stu-id="164f0-118">Create a Network Region</span></span>

<span data-ttu-id="164f0-119">Создание сетевого региона, который может использоваться для управления допуском звонков, E9-1-1 или мультимедийного обхода.</span><span class="sxs-lookup"><span data-stu-id="164f0-119">Create a network region that can be used by call admission control, E9-1-1, or media bypass.</span></span>

<div>

## <a name="to-create-a-network-region-using-lync-server-management-shell"></a><span data-ttu-id="164f0-120">Создание сетевого региона с помощью командной консоли Lync Server Management Shell</span><span class="sxs-lookup"><span data-stu-id="164f0-120">To create a network region using Lync Server Management Shell</span></span>

1.  <span data-ttu-id="164f0-121">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="164f0-121">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="164f0-122">Чтобы создать области сети, используйте командлет New-CsNetworkRegion.</span><span class="sxs-lookup"><span data-stu-id="164f0-122">Run the New-CsNetworkRegion cmdlet to create network regions:</span></span>
    
        New-CsNetworkRegion -Identity <String> -CentralSite <String>
    
    <span data-ttu-id="164f0-123">Например:</span><span class="sxs-lookup"><span data-stu-id="164f0-123">For example:</span></span>
    
        New-CsNetworkRegion -Identity NorthAmerica -CentralSite CHICAGO -Description "All North America Locations"
    
    <span data-ttu-id="164f0-124">В этом примере показано создание области сети "NorthAmerica", которая связана с центральным сайтом с ИД CHICAGO.</span><span class="sxs-lookup"><span data-stu-id="164f0-124">In this example, you created a network region called “NorthAmerica” that is associated with a central site with site ID CHICAGO.</span></span>

3.  <span data-ttu-id="164f0-125">Чтобы завершить создание областей сети для вашей топологии, повторите шаг 2, указав требуемые параметры для каждой области сети.</span><span class="sxs-lookup"><span data-stu-id="164f0-125">To finish creating network regions for your topology, repeat step 2 with settings for each network region.</span></span>

</div>

<div>

## <a name="to-create-a-network-region-using-lync-server-control-panel"></a><span data-ttu-id="164f0-126">Создание сетевого региона с помощью панели управления Lync Server</span><span class="sxs-lookup"><span data-stu-id="164f0-126">To create a network region using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="164f0-127">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="164f0-127">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="164f0-128">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="164f0-128">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

2.  <span data-ttu-id="164f0-129">В левой области навигации щелкните элемент **Конфигурация сети**.</span><span class="sxs-lookup"><span data-stu-id="164f0-129">In the left navigation bar, click **Network Configuration**.</span></span>

3.  <span data-ttu-id="164f0-130">Щелкните **Область**.</span><span class="sxs-lookup"><span data-stu-id="164f0-130">Click **Region**.</span></span>

4.  <span data-ttu-id="164f0-131">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="164f0-131">Click **New**.</span></span>

5.  <span data-ttu-id="164f0-132">На странице **Создание области** введите имя области сети в поле **Имя**.</span><span class="sxs-lookup"><span data-stu-id="164f0-132">On the **New Region** page, click **Name** and then type a name for the network region.</span></span>

6.  <span data-ttu-id="164f0-133">Щелкните **Центральный сайт**, затем выберите центральный сайт в списке.</span><span class="sxs-lookup"><span data-stu-id="164f0-133">Click **Central site**, and then click a central site in the list.</span></span>

7.  <span data-ttu-id="164f0-134">В поле **Описание** введите дополнительные сведения об области сети (необязательно).</span><span class="sxs-lookup"><span data-stu-id="164f0-134">Optionally, click **Description**, and then type additional information to describe this network site.</span></span>

8.  <span data-ttu-id="164f0-135">Нажмите **Исполнить**.</span><span class="sxs-lookup"><span data-stu-id="164f0-135">Click **Commit**.</span></span>

9.  <span data-ttu-id="164f0-136">Чтобы завершить создание областей сети для вашей топологии, повторите шаги с 4 по 8, указав требуемые параметры для остальных областей.</span><span class="sxs-lookup"><span data-stu-id="164f0-136">To finish creating network regions for your topology, repeat steps 4 through 8 with settings for other regions.</span></span>

</div>

</div>

<div>

## <a name="modify-a-network-region"></a><span data-ttu-id="164f0-137">Изменение сетевого региона</span><span class="sxs-lookup"><span data-stu-id="164f0-137">Modify a Network Region</span></span>

<span data-ttu-id="164f0-138">Измените параметры существующего сетевого региона, чтобы внести изменения в основные сведения о регионе или изменения, необходимые для новой функции.</span><span class="sxs-lookup"><span data-stu-id="164f0-138">Modify settings for an existing network region to accommodate changes to the basic region information or changes required by a new feature.</span></span>

<div>

## <a name="to-modify-a-network-region-using-lync-server-management-shell"></a><span data-ttu-id="164f0-139">Изменение сетевого региона с помощью командной консоли Lync Server Management Shell</span><span class="sxs-lookup"><span data-stu-id="164f0-139">To modify a network region using Lync Server Management Shell</span></span>

1.  <span data-ttu-id="164f0-140">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="164f0-140">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="164f0-141">Чтобы изменить существующую область сети, выполните командлет Set-CsNetworkRegion.</span><span class="sxs-lookup"><span data-stu-id="164f0-141">Run the Set-CsNetworkRegion cmdlet to modify an existing network region:</span></span>
    
        Set-CsNetworkRegion -Identity <String> -CentralSite <String>
    
    <span data-ttu-id="164f0-142">Например:</span><span class="sxs-lookup"><span data-stu-id="164f0-142">For example:</span></span>
    
        Set-CsNetworkRegion -Identity NorthAmerica -CentralSite CHICAGO -Description "North American Region"
    
    <span data-ttu-id="164f0-p103">В этом примере показано изменение описания области сети "NorthAmerica", созданной ранее. Если для области "NorthAmerica" описание уже задано, оно будет перезаписано; в противном случае описание будет задано.</span><span class="sxs-lookup"><span data-stu-id="164f0-p103">In this example, you modified an existing network region called “NorthAmerica” (created using the procedures earlier in this topic) by changing the description. If a description existed for the “NorthAmerica” region, this command overwrites it with this value; if no description had been set, then this command sets it.</span></span>

3.  <span data-ttu-id="164f0-145">Чтобы изменить остальные области сети, повторите шаг 2, указав параметры для остальных областей.</span><span class="sxs-lookup"><span data-stu-id="164f0-145">To modify other network regions, repeat step 2 with settings for other regions.</span></span>

</div>

<div>

## <a name="to-modify-a-network-region-using-lync-server-control-panel"></a><span data-ttu-id="164f0-146">Изменение сетевого региона с помощью панели управления Lync Server</span><span class="sxs-lookup"><span data-stu-id="164f0-146">To modify a network region using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="164f0-147">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="164f0-147">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="164f0-148">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="164f0-148">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

2.  <span data-ttu-id="164f0-149">В левой области навигации щелкните элемент **Конфигурация сети**.</span><span class="sxs-lookup"><span data-stu-id="164f0-149">In the left navigation bar, click **Network Configuration**.</span></span>

3.  <span data-ttu-id="164f0-150">Нажмите кнопку навигации **Область**.</span><span class="sxs-lookup"><span data-stu-id="164f0-150">Click the **Region** navigation button.</span></span>

4.  <span data-ttu-id="164f0-151">В таблице щелкните область сети, которую требуется изменить.</span><span class="sxs-lookup"><span data-stu-id="164f0-151">In the table, click the network region that you want to modify.</span></span>

5.  <span data-ttu-id="164f0-152">Щелкните **Изменить**, затем щелкните **Подробнее**.</span><span class="sxs-lookup"><span data-stu-id="164f0-152">Click **Edit**, and then click **Show details…**.</span></span>

6.  <span data-ttu-id="164f0-153">На странице **Изменение области** измените требуемые параметры области сети.</span><span class="sxs-lookup"><span data-stu-id="164f0-153">On the **Edit Region** page, change the values for this network region’s settings as appropriate.</span></span>

7.  <span data-ttu-id="164f0-154">Нажмите **Исполнить**.</span><span class="sxs-lookup"><span data-stu-id="164f0-154">Click **Commit**.</span></span>

8.  <span data-ttu-id="164f0-155">Чтобы завершить изменение областей сети, повторите шаги 4–7, используя параметры для других областей.</span><span class="sxs-lookup"><span data-stu-id="164f0-155">To finish modify network regions, repeat steps 4 through 7 with settings for other regions.</span></span>

<span data-ttu-id="164f0-156"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="164f0-156"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

