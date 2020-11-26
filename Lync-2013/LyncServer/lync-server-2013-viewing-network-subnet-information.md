---
title: 'Lync Server 2013: Просмотр сведений о сетевой подсети'
description: 'Lync Server 2013: Просмотр сведений о сетевой подсети.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Viewing network subnet information
ms:assetid: 46f165f2-efe3-4cc1-9fee-a78b7f2ed41e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688044(v=OCS.15)
ms:contentKeyID: 49733636
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 313135c43318817391d54f2fa3e73dd318f7a11f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438857"
---
# <a name="viewing-network-subnet-information-in-lync-server-2013"></a><span data-ttu-id="3779f-103">Просмотр сведений о сетевой подсети в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3779f-103">Viewing network subnet information in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3779f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3779f-104">

<span> </span></span></span>

<span data-ttu-id="3779f-105">_**Тема последнего изменения:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="3779f-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="3779f-106">Вы можете использовать описанную ниже процедуру для просмотра сетевой подсети.</span><span class="sxs-lookup"><span data-stu-id="3779f-106">You can use the following procedure to view a network subnet.</span></span> <span data-ttu-id="3779f-107">С помощью панели управления Lync Server вы можете создавать, изменять и удалять сетевые подсети.</span><span class="sxs-lookup"><span data-stu-id="3779f-107">From the Lync Server Control Panel, you can create, modify, or delete a network subnet.</span></span> <span data-ttu-id="3779f-108">Дополнительные сведения о создании и изменении подсетей сети можно найти [в разделе Создание или изменение подсетей сети в Lync Server 2013](lync-server-2013-create-or-modify-network-subnets.md).</span><span class="sxs-lookup"><span data-stu-id="3779f-108">For details about creating or modifying network subnets, see [Create or modify network subnets in Lync Server 2013](lync-server-2013-create-or-modify-network-subnets.md).</span></span>

<div>

## <a name="to-view-a-network-subnet"></a><span data-ttu-id="3779f-109">Просмотр сетевой подсети</span><span class="sxs-lookup"><span data-stu-id="3779f-109">To view a network subnet</span></span>

1.  <span data-ttu-id="3779f-110">Войдите на любой компьютер, находящийся во внутреннем развертывании, с использованием учетной записи, входящей в группу RTCUniversalServerAdmins (или имеющей равнозначные права пользователя) либо назначенной роли CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="3779f-110">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="3779f-111">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="3779f-111">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="3779f-112">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="3779f-112">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="3779f-113">На панели навигации слева выберите пункт **Настройка сети** , а затем — **подсеть**.</span><span class="sxs-lookup"><span data-stu-id="3779f-113">In the left navigation bar, click **Network Configuration** and then click **Subnet**.</span></span>

4.  <span data-ttu-id="3779f-114">На странице **Subnet (подсеть** ) выберите подсеть, которую вы хотите просмотреть.</span><span class="sxs-lookup"><span data-stu-id="3779f-114">On the **Subnet** page, click the subnet that you want to view.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="3779f-115">Вы можете просматривать только одну подсеть за один раз.</span><span class="sxs-lookup"><span data-stu-id="3779f-115">You can only view one subnet at a time.</span></span>

    
    </div>

5.  <span data-ttu-id="3779f-116">В меню **Правка** выберите пункт **Показать подробности..**..</span><span class="sxs-lookup"><span data-stu-id="3779f-116">On the **Edit** menu, click **Show details…**.</span></span>

</div>

<div>

## <a name="viewing-network-subnet-configuration-information-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="3779f-117">Просмотр сведений о конфигурации сетевой подсети с помощью командлетов Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="3779f-117">Viewing Network Subnet Configuration Information by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="3779f-118">Сведения о сетевой подсети можно просмотреть с помощью Windows PowerShell и командлета Get-CsNetworkSubnet.</span><span class="sxs-lookup"><span data-stu-id="3779f-118">Network subnet information can be viewed by using Windows PowerShell and the Get-CsNetworkSubnet cmdlet.</span></span> <span data-ttu-id="3779f-119">Этот командлет можно выполнить либо из управляющей оболочки Lync Server 2013, либо из удаленного сеанса Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3779f-119">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="3779f-120">Подробнее об использовании удаленной оболочки Windows PowerShell для подключения к серверу Lync Server можно найти в статье "Краткое руководство по работе с Microsoft Lync Server 2010 с помощью удаленной оболочки PowerShell" на веб-сервере Lync Server Windows PowerShell [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="3779f-120">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-view-network-subnet-information"></a><span data-ttu-id="3779f-121">Просмотр сведений о сетевой подсети</span><span class="sxs-lookup"><span data-stu-id="3779f-121">To view network subnet information</span></span>

  - <span data-ttu-id="3779f-122">Чтобы просмотреть сведения о всех подсетях, введите в командной консоли Lync Server следующую команду и нажмите клавишу ВВОД.</span><span class="sxs-lookup"><span data-stu-id="3779f-122">To view information about all your network subnets, type the following command in the Lync Server Management Shell and then press ENTER:</span></span>
    
        Get-CsNetworkSubnet
    
    <span data-ttu-id="3779f-123">Команда возвращает примерно следующую информацию:</span><span class="sxs-lookup"><span data-stu-id="3779f-123">That will return information similar to this:</span></span>
    
        Identity      : 172.11.15.0
        MaskBits      : 28
        Description   :
        NetworkSiteID : Redmond
        SubnetID      : 172.11.15.0

</div>

<span data-ttu-id="3779f-124">Дополнительные сведения можно найти в разделе справки по командлету [Get-CsNetworkSubnet](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkSubnet) .</span><span class="sxs-lookup"><span data-stu-id="3779f-124">For more information, see the help topic for the [Get-CsNetworkSubnet](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkSubnet) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="3779f-125">См. также</span><span class="sxs-lookup"><span data-stu-id="3779f-125">See Also</span></span>


[<span data-ttu-id="3779f-126">Создание и изменение подсетей сети в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3779f-126">Create or modify network subnets in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-network-subnets.md)  
[<span data-ttu-id="3779f-127">Удаление подсетей сети в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3779f-127">Deleting network subnets in Lync Server 2013</span></span>](lync-server-2013-deleting-network-subnets.md)  
  

<span data-ttu-id="3779f-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3779f-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

