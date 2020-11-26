---
title: 'Lync Server 2013: создание и изменение подсетей сети'
description: 'Lync Server 2013: создание и изменение подсетей сети.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or modify network subnets
ms:assetid: 1ba8c4e3-fbc7-4758-88ac-d651fef17bed
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520957(v=OCS.15)
ms:contentKeyID: 48183548
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 37695707bf39b10c351a4990b132c9799406f9c4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431654"
---
# <a name="create-or-modify-network-subnets-in-lync-server-2013"></a><span data-ttu-id="6524c-103">Создание и изменение подсетей сети в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6524c-103">Create or modify network subnets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6524c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6524c-104">

<span> </span></span></span>

<span data-ttu-id="6524c-105">_**Тема последнего изменения:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="6524c-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="6524c-106">Сетевая подсеть должна быть связана с сетевым сайтом в целях определения географического расположения узла, принадлежащего данной подсети.</span><span class="sxs-lookup"><span data-stu-id="6524c-106">A network subnet must be associated with a network site for the purposes of determining the geographic location of the host belonging to this subnet.</span></span> <span data-ttu-id="6524c-107">Вы можете настроить подсети с помощью панели управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="6524c-107">You can use Lync Server Control Panel to configure subnets.</span></span> <span data-ttu-id="6524c-108">С помощью панели управления Lync Server вы можете создавать, изменять и удалять сетевые подсети.</span><span class="sxs-lookup"><span data-stu-id="6524c-108">From the Lync Server Control Panel, you can create, modify, or delete a network subnet.</span></span> <span data-ttu-id="6524c-109">Подробнее об удалении подсетей сети можно узнать в разделе Удаление подсетей сети [в Lync Server 2013](lync-server-2013-deleting-network-subnets.md).</span><span class="sxs-lookup"><span data-stu-id="6524c-109">For details about deleting network subnets, see [Deleting network subnets in Lync Server 2013](lync-server-2013-deleting-network-subnets.md).</span></span>

<span data-ttu-id="6524c-110">В большинстве развертываний Microsoft Lync Server 2013 там, где реализовано управление допуском звонков (CAC), обычно это большое количество подсетей.</span><span class="sxs-lookup"><span data-stu-id="6524c-110">In most deployments of Microsoft Lync Server 2013 where call admission control (CAC) is implemented, there will typically be a large number of subnets.</span></span> <span data-ttu-id="6524c-111">По этой причине лучше всего настроить подсети из командной консоли Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="6524c-111">Because of this, it is often best to configure subnets from the Lync Server Management Shell.</span></span> <span data-ttu-id="6524c-112">Из него вы можете вызвать **New-CsNetworkSubnet** в сочетании с командлетом Windows PowerShell **Import-CSV**.</span><span class="sxs-lookup"><span data-stu-id="6524c-112">From there you can call **New-CsNetworkSubnet** in conjunction with the Windows PowerShell cmdlet **Import-CSV**.</span></span> <span data-ttu-id="6524c-113">Используя эти командлеты вместе, вы можете прочитать параметры подсети из CSV-файла и одновременно создать несколько подсетей.</span><span class="sxs-lookup"><span data-stu-id="6524c-113">By using these cmdlets together, you can read in subnet settings from a comma-separated values (.csv) file and create multiple subnets at the same time.</span></span> <span data-ttu-id="6524c-114">Примеры создания подсетей из CSV-файла можно найти в разделе [New-CsNetworkSubnet](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkSubnet).</span><span class="sxs-lookup"><span data-stu-id="6524c-114">For examples of how to create subnets from a .csv file, see [New-CsNetworkSubnet](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkSubnet).</span></span>

<div>

## <a name="to-create-a-network-subnet"></a><span data-ttu-id="6524c-115">Создание сетевой подсети</span><span class="sxs-lookup"><span data-stu-id="6524c-115">To create a network subnet</span></span>

1.  <span data-ttu-id="6524c-116">Войдите на любой компьютер, находящийся во внутреннем развертывании, с использованием учетной записи, входящей в группу RTCUniversalServerAdmins (или имеющей равнозначные права пользователя) либо назначенной роли CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="6524c-116">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="6524c-117">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="6524c-117">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="6524c-118">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="6524c-118">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="6524c-119">На панели навигации слева выберите пункт **Настройка сети** , а затем — **подсеть**.</span><span class="sxs-lookup"><span data-stu-id="6524c-119">In the left navigation bar, click **Network Configuration** and then click **Subnet**.</span></span>

4.  <span data-ttu-id="6524c-120">На странице " **подсеть** " нажмите кнопку " **создать**".</span><span class="sxs-lookup"><span data-stu-id="6524c-120">On the **Subnet** page, click **New**.</span></span>

5.  <span data-ttu-id="6524c-121">В разделе **Новая подсеть** введите значение в поле **код подсети** .</span><span class="sxs-lookup"><span data-stu-id="6524c-121">In **New Subnet**, enter a value in the **Subnet ID** field.</span></span> <span data-ttu-id="6524c-122">Это должен быть IP-адрес (например, 174.11.12.0), и он должен быть первым адресом в диапазоне IP-адресов, определенном подсетью.</span><span class="sxs-lookup"><span data-stu-id="6524c-122">This must be an IP address (for example, 174.11.12.0), and it must be the first address in the IP address range defined by the subnet.</span></span>

6.  <span data-ttu-id="6524c-123">В поле " **Маска** " введите числовое значение от 1 до 32.</span><span class="sxs-lookup"><span data-stu-id="6524c-123">In the **Mask** field, enter a numeric value from 1 through 32.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="6524c-124">Это значение — битовая маска, применяемая к создаваемой подсети.</span><span class="sxs-lookup"><span data-stu-id="6524c-124">This value is the bitmask that is to be applied to the subnet being created.</span></span>

    
    </div>

7.  <span data-ttu-id="6524c-125">В поле " **код сайта сети**" выберите сайт, к которому относится эта подсеть.</span><span class="sxs-lookup"><span data-stu-id="6524c-125">In **Network site ID**, select the site to which this subnet belongs.</span></span>

8.  <span data-ttu-id="6524c-126">Необязательно Введите значение в поле **Описание** , чтобы получить дополнительные сведения о подсети, которые нельзя выразить только именем.</span><span class="sxs-lookup"><span data-stu-id="6524c-126">(Optional) Type a value in the **Description** field to provide more information about this subnet that cannot be expressed by the name alone.</span></span>

9.  <span data-ttu-id="6524c-127">Нажмите **Исполнить**.</span><span class="sxs-lookup"><span data-stu-id="6524c-127">Click **Commit**.</span></span>

</div>

<div>

## <a name="to-modify-a-network-subnet"></a><span data-ttu-id="6524c-128">Изменение подсети сети</span><span class="sxs-lookup"><span data-stu-id="6524c-128">To modify a network subnet</span></span>

1.  <span data-ttu-id="6524c-129">Войдите на любой компьютер, находящийся во внутреннем развертывании, с использованием учетной записи, входящей в группу RTCUniversalServerAdmins (или имеющей равнозначные права пользователя) либо назначенной роли CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="6524c-129">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="6524c-130">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="6524c-130">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="6524c-131">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="6524c-131">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="6524c-132">На панели навигации слева выберите пункт **Настройка сети** , а затем — **подсеть**.</span><span class="sxs-lookup"><span data-stu-id="6524c-132">In the left navigation bar, click **Network Configuration** and then click **Subnet**.</span></span>

4.  <span data-ttu-id="6524c-133">На странице **Subnet (подсеть** ) выберите подсеть, которую вы хотите изменить.</span><span class="sxs-lookup"><span data-stu-id="6524c-133">On the **Subnet** page, click the subnet that you want to modify.</span></span>

5.  <span data-ttu-id="6524c-134">В меню **Правка** щелкните **Подробнее**.</span><span class="sxs-lookup"><span data-stu-id="6524c-134">On the **Edit** menu, click **Show details**.</span></span>

6.  <span data-ttu-id="6524c-135">На странице **Изменение подсети** вы можете изменить битовую маску, связанный сетевой сайт или описание.</span><span class="sxs-lookup"><span data-stu-id="6524c-135">On the **Edit Subnet** page, you can modify the bitmask, associated network site, or description.</span></span> <span data-ttu-id="6524c-136">Если вы измените битовую маску, имейте в виду, что идентификатор подсети по-прежнему должен быть первым в диапазоне IP-адресов, определенном подсетью.</span><span class="sxs-lookup"><span data-stu-id="6524c-136">If you modify the bitmask, keep in mind that the Subnet ID must still be the first address in the IP address range defined by the subnet.</span></span>

7.  <span data-ttu-id="6524c-137">Нажмите **Исполнить**.</span><span class="sxs-lookup"><span data-stu-id="6524c-137">Click **Commit**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="6524c-138">См. также</span><span class="sxs-lookup"><span data-stu-id="6524c-138">See Also</span></span>


[<span data-ttu-id="6524c-139">Удаление подсетей сети в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6524c-139">Deleting network subnets in Lync Server 2013</span></span>](lync-server-2013-deleting-network-subnets.md)  


[<span data-ttu-id="6524c-140">О сетевых областях, сайтах и подсетях в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6524c-140">About network regions, sites, and subnets in Lync Server 2013</span></span>](lync-server-2013-about-network-regions-sites-and-subnets.md)  


[<span data-ttu-id="6524c-141">New-CsNetworkSubnet</span><span class="sxs-lookup"><span data-stu-id="6524c-141">New-CsNetworkSubnet</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkSubnet)  
[<span data-ttu-id="6524c-142">Set-CsNetworkSubnet</span><span class="sxs-lookup"><span data-stu-id="6524c-142">Set-CsNetworkSubnet</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsNetworkSubnet)  
[<span data-ttu-id="6524c-143">Remove-CsNetworkSubnet</span><span class="sxs-lookup"><span data-stu-id="6524c-143">Remove-CsNetworkSubnet</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsNetworkSubnet)  
[<span data-ttu-id="6524c-144">Get-CsNetworkSubnet</span><span class="sxs-lookup"><span data-stu-id="6524c-144">Get-CsNetworkSubnet</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkSubnet)  
  

<span data-ttu-id="6524c-145"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6524c-145"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

