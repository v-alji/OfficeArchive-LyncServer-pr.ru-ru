---
title: 'Lync Server 2013: Просмотр сведений о маршрутах для сетевого региона'
description: 'Lync Server 2013: Просмотр сведений о маршрутах для сетевого региона.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Viewing network region route information
ms:assetid: 34dd9fa3-e695-4680-b244-3019298b5009
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688021(v=OCS.15)
ms:contentKeyID: 49733611
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3eca6348ecb13cd0b0b28950d57c741c056c1bd7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446200"
---
# <a name="viewing-network-region-route-information-in-lync-server-2013"></a><span data-ttu-id="0beb4-103">Просмотр сведений о маршруте в сетевом регионе в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0beb4-103">Viewing network region route information in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0beb4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0beb4-104">

<span> </span></span></span>

<span data-ttu-id="0beb4-105">_**Тема последнего изменения:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="0beb4-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="0beb4-106">Каждый регион в конфигурации управления допуском звонков (CAC) должен иметь какой-либо способ получить доступ ко всем остальным регионам.</span><span class="sxs-lookup"><span data-stu-id="0beb4-106">Every region within a call admission control (CAC) configuration must have some way to access every other region.</span></span> <span data-ttu-id="0beb4-107">Несмотря на то, что ссылки на области устанавливают ограничения пропускной способности для подключений между регионами и представляют собой физические ссылки, маршрут определяет связанный путь, который будет проходить соединение между двумя областями.</span><span class="sxs-lookup"><span data-stu-id="0beb4-107">While region links set bandwidth limitations on the connections between regions and also represent the physical links, a route determines which linked path the connection will traverse from one region to another.</span></span> <span data-ttu-id="0beb4-108">Воспользуйтесь приведенными ниже инструкциями, чтобы просмотреть существующие маршруты к сетевым областям в Lync Server 2013 панели управления или в командной консоли Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0beb4-108">Use the following procedures to view existing network region routes in Lync Server 2013 Control Panel or Lync Server 2013 Management Shell.</span></span> <span data-ttu-id="0beb4-109">Дополнительные сведения о создании и изменении маршрутов сетевого региона можно найти [в разделе Создание и изменение маршрутов сетевого региона в Lync Server 2013](lync-server-2013-creating-or-modifying-network-region-routes.md).</span><span class="sxs-lookup"><span data-stu-id="0beb4-109">For details about creating or modifying network region routes, see [Creating or modifying network region routes in Lync Server 2013](lync-server-2013-creating-or-modifying-network-region-routes.md).</span></span>

<div>

## <a name="to-view-network-region-route-information-in-lync-server-control-panel"></a><span data-ttu-id="0beb4-110">Просмотр сведений о маршруте сетевого региона на панели управления Lync Server</span><span class="sxs-lookup"><span data-stu-id="0beb4-110">To view network region route information in Lync Server Control Panel</span></span>

1.  <span data-ttu-id="0beb4-111">Войдите на любой компьютер, находящийся во внутреннем развертывании, с использованием учетной записи, входящей в группу RTCUniversalServerAdmins (или имеющей равнозначные права пользователя) либо назначенной роли CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="0beb4-111">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="0beb4-112">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="0beb4-112">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="0beb4-113">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="0beb4-113">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="0beb4-114">На панели навигации слева выберите пункт **Настройка сети** , а затем — пункт **путь к региону**.</span><span class="sxs-lookup"><span data-stu-id="0beb4-114">In the left navigation bar, click **Network Configuration** and then click **Region Route**.</span></span>

4.  <span data-ttu-id="0beb4-115">На странице " **регион** " щелкните маршрут области, который вы хотите просмотреть.</span><span class="sxs-lookup"><span data-stu-id="0beb4-115">On the **Region Route** page, click the region route that you want to view.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="0beb4-116">Вы можете просматривать только один маршрут области за раз.</span><span class="sxs-lookup"><span data-stu-id="0beb4-116">You can only view one region route at a time.</span></span>

    
    </div>

5.  <span data-ttu-id="0beb4-117">В меню **Правка** щелкните **Подробнее**.</span><span class="sxs-lookup"><span data-stu-id="0beb4-117">On the **Edit** menu, click **Show details**.</span></span>

</div>

<div>

## <a name="viewing-network-region-route-information-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="0beb4-118">Просмотр сведений о маршруте сетевого региона с помощью командлетов Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="0beb4-118">Viewing Network Region Route Information by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="0beb4-119">Сведения о маршруте сетевого региона можно просмотреть с помощью Windows PowerShell и командлета Get-CsNetworkInterRegionRoute.</span><span class="sxs-lookup"><span data-stu-id="0beb4-119">Network region route information can be viewed by using Windows PowerShell and the Get-CsNetworkInterRegionRoute cmdlet.</span></span> <span data-ttu-id="0beb4-120">Этот командлет можно выполнить либо из управляющей оболочки Lync Server 2013, либо из удаленного сеанса Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0beb4-120">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="0beb4-121">Подробнее об использовании удаленной оболочки Windows PowerShell для подключения к серверу Lync Server можно найти в статье "Краткое руководство по работе с Microsoft Lync Server 2010 с помощью удаленной оболочки PowerShell" на веб-сервере Lync Server Windows PowerShell [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="0beb4-121">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-view-network-region-route-information"></a><span data-ttu-id="0beb4-122">Просмотр сведений о маршруте сетевого региона</span><span class="sxs-lookup"><span data-stu-id="0beb4-122">To view network region route information</span></span>

  - <span data-ttu-id="0beb4-123">Чтобы просмотреть сведения о всех маршрутах сетевого региона, введите в командной консоли Lync Server следующую команду и нажмите клавишу ВВОД.</span><span class="sxs-lookup"><span data-stu-id="0beb4-123">To view information about all your network region routes, type the following command in the Lync Server Management Shell and then press ENTER:</span></span>
    
        Get-CsNetworkInterRegionRoute
    
    <span data-ttu-id="0beb4-124">Команда возвращает примерно следующую информацию:</span><span class="sxs-lookup"><span data-stu-id="0beb4-124">That will return information similar to this:</span></span>
    
        Identity                  : TransAmericaRoute
        NetworkRegionLinks        : {NorthwestToNortheast}
        InterNetworkRegionRouteID : TransAmericaRoute
        NetworkRegionID1          : Pacific Northwest
        NetworkRegionID2          : Northeast

</div>

<span data-ttu-id="0beb4-125">Дополнительные сведения можно найти в разделе справки по командлету [Get-CsNetworkInterRegionRoute](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkInterRegionRoute) .</span><span class="sxs-lookup"><span data-stu-id="0beb4-125">For more information, see the help topic for the [Get-CsNetworkInterRegionRoute](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkInterRegionRoute) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="0beb4-126">См. также</span><span class="sxs-lookup"><span data-stu-id="0beb4-126">See Also</span></span>


[<span data-ttu-id="0beb4-127">Создание и изменение маршрутов сетевого региона в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0beb4-127">Creating or modifying network region routes in Lync Server 2013</span></span>](lync-server-2013-creating-or-modifying-network-region-routes.md)  
[<span data-ttu-id="0beb4-128">Удаление существующих маршрутов сетевого региона в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0beb4-128">Deleting existing network region routes in Lync Server 2013</span></span>](lync-server-2013-deleting-existing-network-region-routes.md)  
  

<span data-ttu-id="0beb4-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0beb4-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

