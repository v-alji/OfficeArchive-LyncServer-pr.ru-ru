---
title: 'Lync Server 2013: Просмотр сведений о политике расположения'
description: 'Lync Server 2013: Просмотр сведений о политике местоположений.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Viewing location policy information
ms:assetid: 14e41bcb-ea0a-49c2-99b3-1f61fc34416d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520954(v=OCS.15)
ms:contentKeyID: 48183489
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2fecc5de5fb71014a1641038e9e09afba0e90cdb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443960"
---
# <a name="viewing-location-policy-information-in-lync-server-2013"></a><span data-ttu-id="bd8a5-103">Просмотр сведений о политике местоположений в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bd8a5-103">Viewing location policy information in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bd8a5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bd8a5-104">

<span> </span></span></span>

<span data-ttu-id="bd8a5-105">_**Тема последнего изменения:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="bd8a5-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="bd8a5-106">В Lync Server 2013 вы можете использовать политику расположения для применения параметров, которые относятся к расширенным функциям 9-1-1 (E9-1-1), а также к параметрам расположения для пользователей и контактов.</span><span class="sxs-lookup"><span data-stu-id="bd8a5-106">In Lync Server 2013, you can use the location policy to apply settings that relate to Enhanced 9-1-1 (E9-1-1) functionality and to location settings for users or contacts.</span></span> <span data-ttu-id="bd8a5-107">Политика расположения определяет, разрешено ли пользователю E9-1-1, и в каких случаях может происходить вызов экстренной помощи.</span><span class="sxs-lookup"><span data-stu-id="bd8a5-107">The location policy determines whether a user is enabled for E9-1-1, and if so what the behavior is of an emergency call.</span></span> <span data-ttu-id="bd8a5-108">Например, вы можете использовать политику расположения, чтобы определить, какой номер является вызовом экстренной помощи (например, 911 в США), следует ли автоматически уведомлять корпоративную безопасность, а также как перенаправлять этот звонок.</span><span class="sxs-lookup"><span data-stu-id="bd8a5-108">For example, you can use the location policy to define what number constitutes an emergency call (for example, 911 in the United States), whether corporate security should be automatically notified, and how the call should be routed.</span></span>

<span data-ttu-id="bd8a5-109">Политики местоположений можно настроить в группе **Конфигурация сети** в Lync Server 2013 панели управления.</span><span class="sxs-lookup"><span data-stu-id="bd8a5-109">You can configure location policies from the **Network Configuration** group in Lync Server 2013 Control Panel.</span></span> <span data-ttu-id="bd8a5-110">На панели управления Lync Server вы можете просматривать, создавать, изменять и удалять политики расположения.</span><span class="sxs-lookup"><span data-stu-id="bd8a5-110">From Lync Server Control Panel you can view, create, modify, or delete location policies.</span></span> <span data-ttu-id="bd8a5-111">Чтобы просмотреть сведения о политиках расположения, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="bd8a5-111">Use the following procedure to view information about location policies.</span></span> <span data-ttu-id="bd8a5-112">Дополнительные сведения о создании и изменении политик расположения можно найти [в разделе Создание и изменение политики расположения в Lync Server 2013](lync-server-2013-creating-or-modifying-a-location-policy.md).</span><span class="sxs-lookup"><span data-stu-id="bd8a5-112">For details on creating or modifying location policies, see [Creating or modifying a location policy in Lync Server 2013](lync-server-2013-creating-or-modifying-a-location-policy.md).</span></span>

<div>

## <a name="to-view-information-about-a-location-policy"></a><span data-ttu-id="bd8a5-113">Просмотр сведений о политике расположения</span><span class="sxs-lookup"><span data-stu-id="bd8a5-113">To view information about a location policy</span></span>

1.  <span data-ttu-id="bd8a5-114">Войдите на любой компьютер, находящийся во внутреннем развертывании, с использованием учетной записи, входящей в группу RTCUniversalServerAdmins (или имеющей равнозначные права пользователя) либо назначенной роли CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="bd8a5-114">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="bd8a5-115">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="bd8a5-115">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="bd8a5-116">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="bd8a5-116">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="bd8a5-117">На панели навигации слева выберите пункт **Настройка сети** , а затем — **Политика расположения**.</span><span class="sxs-lookup"><span data-stu-id="bd8a5-117">In the left navigation bar, click **Network Configuration** and then click **Location Policy**.</span></span>

4.  <span data-ttu-id="bd8a5-118">На странице " **Политика расположения** " выберите политику расположения, которую вы хотите изменить.</span><span class="sxs-lookup"><span data-stu-id="bd8a5-118">On the **Location Policy** page, select the location policy that you want to modify.</span></span>

5.  <span data-ttu-id="bd8a5-119">В меню **Правка** щелкните **Подробнее**.</span><span class="sxs-lookup"><span data-stu-id="bd8a5-119">On the **Edit** menu, click **Show details**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="bd8a5-120">Вы можете только просматривать сведения о одной политике размещения.</span><span class="sxs-lookup"><span data-stu-id="bd8a5-120">You can only view information about one location policy at a time.</span></span>

    
    </div>

<span data-ttu-id="bd8a5-121">Отдельная политика, называемая Global, существует по умолчанию и не может быть удалена или переименована.</span><span class="sxs-lookup"><span data-stu-id="bd8a5-121">A single policy, called Global, exists by default and cannot be deleted or renamed.</span></span> <span data-ttu-id="bd8a5-122">Однако вы можете изменить глобальную политику.</span><span class="sxs-lookup"><span data-stu-id="bd8a5-122">However, you can modify the Global policy.</span></span> <span data-ttu-id="bd8a5-123">Эта политика будет применяться ко всем пользователям и контактам, если только вы не создаете политики сайта или политики для пользователей.</span><span class="sxs-lookup"><span data-stu-id="bd8a5-123">This policy will apply to all users and contacts, unless you create site policies or per-user policies.</span></span> <span data-ttu-id="bd8a5-124">Политики для пользователей должны применяться к определенным пользователям.</span><span class="sxs-lookup"><span data-stu-id="bd8a5-124">Per-user policies must be applied to specific users.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="bd8a5-125">См. также</span><span class="sxs-lookup"><span data-stu-id="bd8a5-125">See Also</span></span>


[<span data-ttu-id="bd8a5-126">Создание и изменение политики расположения в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bd8a5-126">Creating or modifying a location policy in Lync Server 2013</span></span>](lync-server-2013-creating-or-modifying-a-location-policy.md)  
[<span data-ttu-id="bd8a5-127">Создание политик местоположений в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bd8a5-127">Create location policies in Lync Server 2013</span></span>](lync-server-2013-create-location-policies.md)  
[<span data-ttu-id="bd8a5-128">Создание или изменение сетевого сайта в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bd8a5-128">Create or modify a network site in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-network-site.md)  


[<span data-ttu-id="bd8a5-129">New-CsLocationPolicy</span><span class="sxs-lookup"><span data-stu-id="bd8a5-129">New-CsLocationPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsLocationPolicy)  
[<span data-ttu-id="bd8a5-130">Set-CsLocationPolicy</span><span class="sxs-lookup"><span data-stu-id="bd8a5-130">Set-CsLocationPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsLocationPolicy)  
[<span data-ttu-id="bd8a5-131">Remove-CsLocationPolicy</span><span class="sxs-lookup"><span data-stu-id="bd8a5-131">Remove-CsLocationPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsLocationPolicy)  
[<span data-ttu-id="bd8a5-132">Get-CsLocationPolicy</span><span class="sxs-lookup"><span data-stu-id="bd8a5-132">Get-CsLocationPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsLocationPolicy)  
  

<span data-ttu-id="bd8a5-133"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bd8a5-133"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

