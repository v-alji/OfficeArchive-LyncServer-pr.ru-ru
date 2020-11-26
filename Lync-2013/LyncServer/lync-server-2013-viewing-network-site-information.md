---
title: 'Lync Server 2013: Просмотр сведений о сетевом сайте'
description: 'Lync Server 2013: Просмотр сведений о сетевом сайте.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Viewing network site information
ms:assetid: 24a97d98-b168-4016-81bf-c2c478092b87
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687996(v=OCS.15)
ms:contentKeyID: 49733586
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b46dc91510cb5ff737977871470033374573ba8c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440404"
---
# <a name="viewing-network-site-information-in-lync-server-2013"></a><span data-ttu-id="e14d8-103">Просмотр сведений о сетевом сайте в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e14d8-103">Viewing network site information in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e14d8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e14d8-104">

<span> </span></span></span>

<span data-ttu-id="e14d8-105">_**Тема последнего изменения:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="e14d8-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="e14d8-106">Сетевые сайты — это офисы или места, настроенные в каждом регионе управления допуском звонков (CAC) или Улучшенное развертывание 9-1-1.</span><span class="sxs-lookup"><span data-stu-id="e14d8-106">Network sites are the offices or locations configured within each region of a call admission control (CAC) or Enhanced 9-1-1 deployment.</span></span> <span data-ttu-id="e14d8-107">Вы можете просматривать сведения о сетевом сайте либо на панели управления Lync Server 2013, либо в командной консоли Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="e14d8-107">You can view network site information in either Lync Server 2013 Control Panel or Lync Server Management Shell .</span></span> <span data-ttu-id="e14d8-108">Дополнительные сведения о создании и изменении сайтов сети можно найти [в разделе Создание или изменение сетевых сайтов в Lync Server 2013](lync-server-2013-creating-or-modifying-network-sites.md).</span><span class="sxs-lookup"><span data-stu-id="e14d8-108">For details about creating or modifying network sites, see [Creating or modifying network sites in Lync Server 2013](lync-server-2013-creating-or-modifying-network-sites.md).</span></span>

<div>

## <a name="to-view-network-site-information-in-lync-server-control-panel"></a><span data-ttu-id="e14d8-109">Просмотр сведений о сетевом сайте на панели управления Lync Server</span><span class="sxs-lookup"><span data-stu-id="e14d8-109">To view network site information in Lync Server Control Panel</span></span>

1.  <span data-ttu-id="e14d8-110">Войдите на любой компьютер, находящийся во внутреннем развертывании, с использованием учетной записи, входящей в группу RTCUniversalServerAdmins (или имеющей равнозначные права пользователя) либо назначенной роли CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="e14d8-110">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="e14d8-111">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="e14d8-111">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="e14d8-112">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="e14d8-112">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="e14d8-113">На панели навигации слева выберите пункт **Настройка сети** , а затем — **сайт**.</span><span class="sxs-lookup"><span data-stu-id="e14d8-113">In the left navigation bar, click **Network Configuration** and then click **Site**.</span></span>

4.  <span data-ttu-id="e14d8-114">На странице **сайта** выберите сайт, который вы хотите просмотреть.</span><span class="sxs-lookup"><span data-stu-id="e14d8-114">On the **Site** page, click the site that you want to view.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="e14d8-115">Вы можете просматривать сведения только для одного сайта одновременно.</span><span class="sxs-lookup"><span data-stu-id="e14d8-115">You can only view information for one site at a time.</span></span>

    
    </div>

5.  <span data-ttu-id="e14d8-116">В меню **Правка** щелкните **Подробнее**.</span><span class="sxs-lookup"><span data-stu-id="e14d8-116">On the **Edit** menu, click **Show details**.</span></span>

</div>

<div>

## <a name="viewing-network-site-information-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="e14d8-117">Просмотр сведений о сетевом сайте с помощью командлетов Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="e14d8-117">Viewing Network Site Information by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="e14d8-118">Вы можете просматривать сведения о сетевом сайте с помощью Windows PowerShell и командлета Get-CsNetworkSite.</span><span class="sxs-lookup"><span data-stu-id="e14d8-118">You can view network site information by using Windows PowerShell and the Get-CsNetworkSite cmdlet.</span></span> <span data-ttu-id="e14d8-119">Этот командлет можно выполнить либо из управляющей оболочки Lync Server 2013, либо из удаленного сеанса Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e14d8-119">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="e14d8-120">Подробнее об использовании удаленной оболочки Windows PowerShell для подключения к серверу Lync Server можно найти в статье "Краткое руководство по работе с Microsoft Lync Server 2010 с помощью удаленной оболочки PowerShell" на веб-сервере Lync Server Windows PowerShell [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="e14d8-120">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-view-network-site-information"></a><span data-ttu-id="e14d8-121">Просмотр сведений о сетевом сайте</span><span class="sxs-lookup"><span data-stu-id="e14d8-121">To view network site information</span></span>

  - <span data-ttu-id="e14d8-122">Чтобы просмотреть сведения о всех сетевых сайтах, введите в командной консоли Lync Server указанную ниже команду и нажмите клавишу ВВОД.</span><span class="sxs-lookup"><span data-stu-id="e14d8-122">To view information about all your network sites, type the following command in the Lync Server Management Shell and then press ENTER:</span></span>
    
        Get-CsNetworkSite
    
    <span data-ttu-id="e14d8-123">Команда возвращает примерно следующую информацию:</span><span class="sxs-lookup"><span data-stu-id="e14d8-123">That will return information similar to this:</span></span>
    
        Identity          : Redmond
        NetworkSiteID     : Redmond
        Description       :
        NetworkRegionID   : Pacific Northwest
        BypassID          : 3b232b84-2c1d-4da2-8181-e9330bafebe9
        BWPolicyProfileID :
        LocationPolicy    :

</div>

<span data-ttu-id="e14d8-124">Дополнительные сведения можно найти в разделе справки по командлету [Get-CsNetworkSite](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkSite) .</span><span class="sxs-lookup"><span data-stu-id="e14d8-124">For more information, see the help topic for the [Get-CsNetworkSite](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkSite) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="e14d8-125">См. также</span><span class="sxs-lookup"><span data-stu-id="e14d8-125">See Also</span></span>


[<span data-ttu-id="e14d8-126">Создание и изменение сетевых сайтов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e14d8-126">Creating or modifying network sites in Lync Server 2013</span></span>](lync-server-2013-creating-or-modifying-network-sites.md)  
[<span data-ttu-id="e14d8-127">Удаление существующего сетевого сайта в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e14d8-127">Deleting an existing network site in Lync Server 2013</span></span>](lync-server-2013-deleting-an-existing-network-site.md)  
  

<span data-ttu-id="e14d8-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e14d8-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

