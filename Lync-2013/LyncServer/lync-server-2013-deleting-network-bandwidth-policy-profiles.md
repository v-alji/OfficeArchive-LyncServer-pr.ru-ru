---
title: 'Lync Server 2013: удаление профилей политики пропускной способности сети'
description: 'Lync Server 2013: удаление профилей политики пропускной способности сети.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deleting network bandwidth policy profiles
ms:assetid: 4d6beda8-6aa5-4d5e-8a07-363598f0e0c8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688050(v=OCS.15)
ms:contentKeyID: 49733643
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 69f460d9620158d1857dae41e0033f6d36078868
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430303"
---
# <a name="deleting-network-bandwidth-policy-profiles-in-lync-server-2013"></a><span data-ttu-id="e1b79-103">Удаление профилей политики пропускной способности сети в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e1b79-103">Deleting network bandwidth policy profiles in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e1b79-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e1b79-104">

<span> </span></span></span>

<span data-ttu-id="e1b79-105">_**Тема последнего изменения:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="e1b79-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="e1b79-106">В рамках управления допуском звонков (CAC) для определения ограничений пропускной способности для некоторых модальностей используется политика пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="e1b79-106">As part of call admission control (CAC), a bandwidth policy is used to define bandwidth limitations for certain modalities.</span></span> <span data-ttu-id="e1b79-107">В Microsoft Lync Server 2013 можно назначать ограничения пропускной способности только для модальностей аудио и видео.</span><span class="sxs-lookup"><span data-stu-id="e1b79-107">In Microsoft Lync Server 2013, only audio and video modalities can be assigned bandwidth limitations.</span></span> <span data-ttu-id="e1b79-108">Вы можете настроить общие ограничения пропускной способности и ограничения сеанса.</span><span class="sxs-lookup"><span data-stu-id="e1b79-108">You can set overall bandwidth limitations and session limitations.</span></span> <span data-ttu-id="e1b79-109">С помощью панели управления Lync Server вы можете создавать, изменять и удалять профили контейнеров для этих политик.</span><span class="sxs-lookup"><span data-stu-id="e1b79-109">You can use the Lync Server Control Panel to create, modify, or delete a container profile for these policies.</span></span> <span data-ttu-id="e1b79-110">Для удаления профилей политики пропускной способности сети выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="e1b79-110">Use the following procedures to delete a network bandwidth policy profiles.</span></span> <span data-ttu-id="e1b79-111">Подробнее о создании или изменении профиля политики пропускной способности сети можно узнать [в разделе Создание и изменение профилей политики пропускной способности в Lync Server 2013](lync-server-2013-creating-or-modifying-bandwidth-policy-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="e1b79-111">For details on creating or modifying a network bandwidth policy profile, see [Creating or modifying bandwidth policy profiles in Lync Server 2013](lync-server-2013-creating-or-modifying-bandwidth-policy-profiles.md).</span></span>

<div>

## <a name="to-delete-a-bandwidth-policy-profile"></a><span data-ttu-id="e1b79-112">Удаление профиля политики пропускной способности</span><span class="sxs-lookup"><span data-stu-id="e1b79-112">To delete a bandwidth policy profile</span></span>

1.  <span data-ttu-id="e1b79-113">Войдите на любой компьютер, находящийся во внутреннем развертывании, с использованием учетной записи, входящей в группу RTCUniversalServerAdmins (или имеющей равнозначные права пользователя) либо назначенной роли CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="e1b79-113">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="e1b79-114">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="e1b79-114">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="e1b79-115">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="e1b79-115">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="e1b79-116">На панели навигации слева выберите пункт **Настройка сети** , а затем — **политика пропускной способности**.</span><span class="sxs-lookup"><span data-stu-id="e1b79-116">In the left navigation bar, click **Network Configuration** and then click **Bandwidth Policy**.</span></span>

4.  <span data-ttu-id="e1b79-117">На странице **политики пропускной способности** выберите профиль политики пропускной способности, который вы хотите удалить.</span><span class="sxs-lookup"><span data-stu-id="e1b79-117">On the **Bandwidth Policy** page, click the bandwidth policy profile that you want to delete.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="e1b79-118">За один раз можно удалить сразу несколько профилей.</span><span class="sxs-lookup"><span data-stu-id="e1b79-118">You can delete more than one profile at a time.</span></span> <span data-ttu-id="e1b79-119">Для этого нажмите клавишу CTRL и, удерживая нажатой клавишу CTRL, выберите несколько профилей.</span><span class="sxs-lookup"><span data-stu-id="e1b79-119">To do this, press CTRL and select multiple profiles while holding down the CTRL key.</span></span> <span data-ttu-id="e1b79-120">Кроме того, чтобы выбрать все профили, в меню <STRONG>Правка</STRONG> выберите команду <STRONG>выделить все</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="e1b79-120">Or, to select all profiles, click <STRONG>Select all</STRONG> on the <STRONG>Edit</STRONG> menu.</span></span>

    
    </div>

5.  <span data-ttu-id="e1b79-121">В меню **Правка** выберите команду **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="e1b79-121">On the **Edit** menu, click **Delete**.</span></span>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="e1b79-122">Вы не можете удалить профиль политики пропускной способности, связанный с сетевым сайтом.</span><span class="sxs-lookup"><span data-stu-id="e1b79-122">You cannot delete a bandwidth policy profile that is associated with a network site.</span></span> <span data-ttu-id="e1b79-123">Прежде чем удалять профиль, необходимо сначала удалить связь с сетевым сайтом.</span><span class="sxs-lookup"><span data-stu-id="e1b79-123">You must first remove the association with the network site before you can delete the profile.</span></span> <span data-ttu-id="e1b79-124">Сведения о том, как изменить сетевой сайт, можно найти <A href="lync-server-2013-creating-or-modifying-network-sites.md">в разделе Создание и изменение сетевых сайтов в Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="e1b79-124">For details about how to modify the network site, see <A href="lync-server-2013-creating-or-modifying-network-sites.md">Creating or modifying network sites in Lync Server 2013</A>.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="e1b79-125">См. также</span><span class="sxs-lookup"><span data-stu-id="e1b79-125">See Also</span></span>


[<span data-ttu-id="e1b79-126">Создание и изменение профилей политики пропускной способности в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e1b79-126">Creating or modifying bandwidth policy profiles in Lync Server 2013</span></span>](lync-server-2013-creating-or-modifying-bandwidth-policy-profiles.md)  
[<span data-ttu-id="e1b79-127">Просмотр данных профиля политики пропускной способности сети в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e1b79-127">Viewing network bandwidth policy profile information in Lync Server 2013</span></span>](lync-server-2013-viewing-network-bandwidth-policy-profile-information.md)  


[<span data-ttu-id="e1b79-128">Настройка управления допуском звонков в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e1b79-128">Configure call admission control in Lync Server 2013</span></span>](lync-server-2013-configure-call-admission-control.md)  
[<span data-ttu-id="e1b79-129">Remove-CsNetworkBandwidthPolicyProfile</span><span class="sxs-lookup"><span data-stu-id="e1b79-129">Remove-CsNetworkBandwidthPolicyProfile</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsNetworkBandwidthPolicyProfile)  
  

<span data-ttu-id="e1b79-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e1b79-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

