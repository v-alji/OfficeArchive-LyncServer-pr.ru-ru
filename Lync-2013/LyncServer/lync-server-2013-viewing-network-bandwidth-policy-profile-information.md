---
title: 'Lync Server 2013: Просмотр данных профиля политики пропускной способности сети'
description: 'Lync Server 2013: Просмотр данных профиля политики пропускной способности сети.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Viewing network bandwidth policy profile information
ms:assetid: eed453fc-04e9-4971-959c-6fad54bf1c96
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721931(v=OCS.15)
ms:contentKeyID: 49733866
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c72a3533ae6f49f91db91b2c3b515c0b5153ec27
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398932"
---
# <a name="viewing-network-bandwidth-policy-profile-information-in-lync-server-2013"></a><span data-ttu-id="2e7b9-103">Просмотр данных профиля политики пропускной способности сети в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2e7b9-103">Viewing network bandwidth policy profile information in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2e7b9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2e7b9-104">

<span> </span></span></span>

<span data-ttu-id="2e7b9-105">_**Тема последнего изменения:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="2e7b9-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="2e7b9-106">В рамках управления допуском звонков (CAC) для определения ограничений пропускной способности для некоторых модальностей используется политика пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="2e7b9-106">As part of call admission control (CAC), a bandwidth policy is used to define bandwidth limitations for certain modalities.</span></span> <span data-ttu-id="2e7b9-107">В Microsoft Lync Server 2013 можно назначать ограничения пропускной способности только для модальностей аудио и видео.</span><span class="sxs-lookup"><span data-stu-id="2e7b9-107">In Microsoft Lync Server 2013, only audio and video modalities can be assigned bandwidth limitations.</span></span> <span data-ttu-id="2e7b9-108">Вы можете настроить общие ограничения пропускной способности и ограничения сеанса.</span><span class="sxs-lookup"><span data-stu-id="2e7b9-108">You can set overall bandwidth limitations and session limitations.</span></span> <span data-ttu-id="2e7b9-109">С помощью панели управления Lync Server вы можете создавать, изменять и удалять профили контейнеров для этих политик.</span><span class="sxs-lookup"><span data-stu-id="2e7b9-109">You can use the Lync Server Control Panel to create, modify, or delete a container profile for these policies.</span></span> <span data-ttu-id="2e7b9-110">Каждый профиль политики пропускной способности может быть связан с одним или несколькими сетевыми сайтами.</span><span class="sxs-lookup"><span data-stu-id="2e7b9-110">Each bandwidth policy profile can be associated with one or more network sites.</span></span> <span data-ttu-id="2e7b9-111">Чтобы просмотреть профиль политики пропускной способности, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="2e7b9-111">Use the following procedures to view a bandwidth policy profile.</span></span> <span data-ttu-id="2e7b9-112">Чтобы создать или изменить профиль политики пропускной способности, ознакомьтесь с разразделами [Создание и изменение профилей политики пропускной способности в Lync Server 2013](lync-server-2013-creating-or-modifying-bandwidth-policy-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="2e7b9-112">To create or modify a bandwidth policy profile, see [Creating or modifying bandwidth policy profiles in Lync Server 2013](lync-server-2013-creating-or-modifying-bandwidth-policy-profiles.md).</span></span>

<div>

## <a name="to-view-a-bandwidth-policy-profile"></a><span data-ttu-id="2e7b9-113">Просмотр профиля политики пропускной способности</span><span class="sxs-lookup"><span data-stu-id="2e7b9-113">To view a bandwidth policy profile</span></span>

1.  <span data-ttu-id="2e7b9-114">Войдите на любой компьютер, находящийся во внутреннем развертывании, с использованием учетной записи, входящей в группу RTCUniversalServerAdmins (или имеющей равнозначные права пользователя) либо назначенной роли CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="2e7b9-114">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="2e7b9-115">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="2e7b9-115">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="2e7b9-116">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="2e7b9-116">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="2e7b9-117">На панели навигации слева выберите пункт **Настройка сети** , а затем — **политика пропускной способности**.</span><span class="sxs-lookup"><span data-stu-id="2e7b9-117">In the left navigation bar, click **Network Configuration** and then click **Bandwidth Policy**.</span></span>

4.  <span data-ttu-id="2e7b9-118">На странице **политики пропускной способности** выберите профиль политики пропускной способности, который вы хотите просмотреть.</span><span class="sxs-lookup"><span data-stu-id="2e7b9-118">On the **Bandwidth Policy** page, click the bandwidth policy profile that you want to view.</span></span>

5.  <span data-ttu-id="2e7b9-119">В меню **Правка** щелкните **Подробнее**.</span><span class="sxs-lookup"><span data-stu-id="2e7b9-119">On the **Edit** menu, click **Show details**.</span></span>

</div>

<div>

## <a name="viewing-network-bandwidth-policy-profile-information-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="2e7b9-120">Просмотр данных профиля политики пропускной способности сети с помощью командлетов Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="2e7b9-120">Viewing Network Bandwidth Policy Profile Information by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="2e7b9-121">Профили пропускной способности сети можно просматривать с помощью Windows PowerShell и командлета Get-CsNetworkBandwidthPolicyProfile.</span><span class="sxs-lookup"><span data-stu-id="2e7b9-121">Network bandwidth profiles can be viewed by using Windows PowerShell and the Get-CsNetworkBandwidthPolicyProfile cmdlet.</span></span> <span data-ttu-id="2e7b9-122">Этот командлет можно выполнить либо из управляющей оболочки Lync Server 2013, либо из удаленного сеанса Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2e7b9-122">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="2e7b9-123">Подробнее об использовании удаленной оболочки Windows PowerShell для подключения к серверу Lync Server можно найти в статье "Краткое руководство по работе с Microsoft Lync Server 2010 с помощью удаленной оболочки PowerShell" на веб-сервере Lync Server Windows PowerShell [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="2e7b9-123">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-view-network-bandwidth-policy-profile-information"></a><span data-ttu-id="2e7b9-124">Просмотр данных профиля политики пропускной способности сети</span><span class="sxs-lookup"><span data-stu-id="2e7b9-124">To view network bandwidth policy profile information</span></span>

  - <span data-ttu-id="2e7b9-125">Чтобы просмотреть сведения о профиле политики пропускной способности сети, введите следующую команду в командной консоли Lync Server Management Shell и нажмите клавишу ВВОД.</span><span class="sxs-lookup"><span data-stu-id="2e7b9-125">To view information about all your network bandwidth policy profiles, type the following command in the Lync Server Management Shell and then press ENTER:</span></span>
    
        Get-CsNetworkBandwidthPolicyProfile
    
    <span data-ttu-id="2e7b9-126">Команда возвращает примерно следующую информацию:</span><span class="sxs-lookup"><span data-stu-id="2e7b9-126">That will return information similar to this:</span></span>
    
        Identity          : RedmondBandwidthPolicy
        BWPolicy          : {BWLimit=200;BWSessionLimit=200;
                            BWPolicyModality=Audio, 
                            BWLimit=1400;BWSessionLimit=500;
                            BWPolicyModality=Video}
        BWPolicyProfileID : RedmondBandwidthPolicy
        Description       :

</div>

<span data-ttu-id="2e7b9-127">Дополнительные сведения можно найти в разделе справки по командлету [Get-CsNetworkBandwidthPolicyProfile](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkBandwidthPolicyProfile) .</span><span class="sxs-lookup"><span data-stu-id="2e7b9-127">For more information, see the help topic for the [Get-CsNetworkBandwidthPolicyProfile](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkBandwidthPolicyProfile) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="2e7b9-128">См. также</span><span class="sxs-lookup"><span data-stu-id="2e7b9-128">See Also</span></span>


[<span data-ttu-id="2e7b9-129">Создание и изменение профилей политики пропускной способности в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2e7b9-129">Creating or modifying bandwidth policy profiles in Lync Server 2013</span></span>](lync-server-2013-creating-or-modifying-bandwidth-policy-profiles.md)  
[<span data-ttu-id="2e7b9-130">Удаление профилей политики пропускной способности сети в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2e7b9-130">Deleting network bandwidth policy profiles in Lync Server 2013</span></span>](lync-server-2013-deleting-network-bandwidth-policy-profiles.md)  


[<span data-ttu-id="2e7b9-131">Настройка управления допуском звонков в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2e7b9-131">Configure call admission control in Lync Server 2013</span></span>](lync-server-2013-configure-call-admission-control.md)  
  

<span data-ttu-id="2e7b9-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2e7b9-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

