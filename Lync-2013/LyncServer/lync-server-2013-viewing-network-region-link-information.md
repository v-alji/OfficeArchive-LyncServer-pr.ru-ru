---
title: 'Lync Server 2013: Просмотр сведений о связи с сетевым регионом'
description: 'Lync Server 2013: Просмотр сведений о ссылке на сетевой регион.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Viewing network region link information
ms:assetid: 7b6b2ea2-83d8-4376-afb2-70e5d2cf6444
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688102(v=OCS.15)
ms:contentKeyID: 49733701
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0134ded9942ebda91050c1f7b0bbcfef018451a3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446207"
---
# <a name="viewing-network-region-link-information-in-lync-server-2013"></a><span data-ttu-id="70b06-103">Просмотр сведений о связи по сетевому региону в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="70b06-103">Viewing network region link information in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="70b06-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="70b06-104">

<span> </span></span></span>

<span data-ttu-id="70b06-105">_**Тема последнего изменения:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="70b06-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="70b06-106">Вы можете просматривать ссылки между двумя сетевыми областями в рамках управления допуском звонков (CAC).</span><span class="sxs-lookup"><span data-stu-id="70b06-106">You can view links between two network regions as part of call admission control (CAC).</span></span> <span data-ttu-id="70b06-107">Регионы в сети связаны по ГЛОБАЛЬным сетевым подключениям.</span><span class="sxs-lookup"><span data-stu-id="70b06-107">Regions within a network are linked through physical wide area network (WAN) connectivity.</span></span> <span data-ttu-id="70b06-108">Вы можете просмотреть существующую ссылку между двумя областями сети с помощью панели управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="70b06-108">You can use the Lync Server Control Panel to view an existing link between two network regions.</span></span> <span data-ttu-id="70b06-109">Дополнительные сведения о создании и изменении ссылки на сетевой регион можно найти [в разделе Настройка ссылок на сетевые регионы в Lync Server 2013](lync-server-2013-configuring-network-region-links.md).</span><span class="sxs-lookup"><span data-stu-id="70b06-109">For details about creating or modifying network region link, see [Configuring network region links in Lync Server 2013](lync-server-2013-configuring-network-region-links.md).</span></span>

<div>

## <a name="to-view-a-network-region-link-in-lync-server-control-panel"></a><span data-ttu-id="70b06-110">Просмотр ссылки на сетевой регион на панели управления Lync Server</span><span class="sxs-lookup"><span data-stu-id="70b06-110">To view a network region link in Lync Server Control Panel</span></span>

1.  <span data-ttu-id="70b06-111">Войдите на любой компьютер, находящийся во внутреннем развертывании, с использованием учетной записи, входящей в группу RTCUniversalServerAdmins (или имеющей равнозначные права пользователя) либо назначенной роли CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="70b06-111">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="70b06-112">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="70b06-112">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="70b06-113">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="70b06-113">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="70b06-114">На панели навигации слева выберите пункт **Настройка сети** , а затем щелкните **ссылку Region (регион**).</span><span class="sxs-lookup"><span data-stu-id="70b06-114">In the left navigation bar, click **Network Configuration** and then click **Region Link**.</span></span>

4.  <span data-ttu-id="70b06-115">На странице " **ссылка на регион** " щелкните ссылку "регион", которую вы хотите просмотреть.</span><span class="sxs-lookup"><span data-stu-id="70b06-115">On the **Region Link** page, click the region link that you want to view.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="70b06-116">Вы можете просматривать сведения только о одной ссылке на регион за один раз.</span><span class="sxs-lookup"><span data-stu-id="70b06-116">You can only view information about one region link at a time.</span></span>

    
    </div>

5.  <span data-ttu-id="70b06-117">В меню **Правка** выберите пункт **Показать подробности**.</span><span class="sxs-lookup"><span data-stu-id="70b06-117">From the **Edit** menu, select **Show details**.</span></span>

</div>

<div>

## <a name="viewing-network-region-link-information-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="70b06-118">Просмотр сведений о связи по сетевому региону с помощью командлетов Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="70b06-118">Viewing Network Region Link Information by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="70b06-119">Вы можете просматривать ссылки на сетевую область с помощью Windows PowerShell и командлета **Get-CsNetworkRegionLink** .</span><span class="sxs-lookup"><span data-stu-id="70b06-119">You can view network region links by using Windows PowerShell and the **Get-CsNetworkRegionLink** cmdlet.</span></span> <span data-ttu-id="70b06-120">Этот командлет можно выполнить из управляющей оболочки Lync Server 2013 или из удаленного сеанса Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="70b06-120">You can run this cmdlet from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="70b06-121">Подробнее об использовании удаленной оболочки Windows PowerShell для подключения к серверу Lync Server можно найти в статье "Краткое руководство по работе с Microsoft Lync Server 2010 с помощью удаленной оболочки PowerShell" на веб-сервере Lync Server Windows PowerShell [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="70b06-121">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-view-network-region-link-information"></a><span data-ttu-id="70b06-122">Просмотр сведений о связи по сетевому региону</span><span class="sxs-lookup"><span data-stu-id="70b06-122">To view network region link information</span></span>

  - <span data-ttu-id="70b06-123">Чтобы просмотреть сведения о ссылках на сетевой регион, введите следующую команду в командной консоли Lync Server Management Shell и нажмите клавишу ВВОД.</span><span class="sxs-lookup"><span data-stu-id="70b06-123">To view information about all your network region links, type the following command in the Lync Server Management Shell and then press ENTER:</span></span>
    
        Get-CsNetworkRegionLink
    
    <span data-ttu-id="70b06-124">Этой командой возвращается информация, аналогичная следующим сведениям:</span><span class="sxs-lookup"><span data-stu-id="70b06-124">This command returns information similar to the following:</span></span>
    
        Identity            : NorthwestToCalifornia
        BWPolicyProfileID   :
        NetworkRegionLinkID : NorthwestToCalifornia
        NetworkRegionID1    : Pacific Northwest
        NetworkRegionID2    : California

</div>

<span data-ttu-id="70b06-125">Подробности можно найти в [статьях Get-CsNetworkRegionLink](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkRegionLink).</span><span class="sxs-lookup"><span data-stu-id="70b06-125">For details, see [Get-CsNetworkRegionLink](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkRegionLink).</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="70b06-126">См. также</span><span class="sxs-lookup"><span data-stu-id="70b06-126">See Also</span></span>


[<span data-ttu-id="70b06-127">Настройка связей сайтов сети в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="70b06-127">Configuring network site links in Lync Server 2013</span></span>](lync-server-2013-configuring-network-site-links.md)  
  

<span data-ttu-id="70b06-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="70b06-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

