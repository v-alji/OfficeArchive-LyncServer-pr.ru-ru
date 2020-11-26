---
title: 'Lync Server 2013: Настройка ссылок на сетевой регион'
description: 'Lync Server 2013: Настройка ссылок на сетевой регион.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring network region links
ms:assetid: 952bc93e-e6aa-4539-85c7-2b15f14eb382
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182551(v=OCS.15)
ms:contentKeyID: 48184829
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b92593f3b8fcd5fe3307a9c193ed7cddcf6dfce0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432928"
---
# <a name="configuring-network-region-links-in-lync-server-2013"></a><span data-ttu-id="88a9c-103">Настройка ссылок на сетевой регион в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="88a9c-103">Configuring network region links in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="88a9c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="88a9c-104">

<span> </span></span></span>

<span data-ttu-id="88a9c-105">_**Тема последнего изменения:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="88a9c-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="88a9c-106">Вы можете настроить связи между двумя сетевыми областями в рамках управления допуском звонков (CAC).</span><span class="sxs-lookup"><span data-stu-id="88a9c-106">You can configure links between two network regions as part of call admission control (CAC).</span></span> <span data-ttu-id="88a9c-107">Регионы в сети связаны по ГЛОБАЛЬным сетевым подключениям.</span><span class="sxs-lookup"><span data-stu-id="88a9c-107">Regions within a network are linked through physical wide area network (WAN) connectivity.</span></span> <span data-ttu-id="88a9c-108">С помощью панели управления Lync Server вы можете определить связь между двумя областями сети и задать ограничения пропускной способности для звуковых и видеоподключений между этими регионами.</span><span class="sxs-lookup"><span data-stu-id="88a9c-108">You can use the Lync Server Control Panel to define a link between two network regions and set the bandwidth limitations on audio and video connections between these regions.</span></span> <span data-ttu-id="88a9c-109">Подробнее об удалении ссылки на существующий сетевой регион можно узнать [в разделе Удаление ссылок на области сети в Lync Server 2013](lync-server-2013-deleting-network-region-links.md).</span><span class="sxs-lookup"><span data-stu-id="88a9c-109">For details about deleting an existing network region link, see [Deleting network region links in Lync Server 2013](lync-server-2013-deleting-network-region-links.md).</span></span>

<div>

## <a name="to-create-a-network-region-link"></a><span data-ttu-id="88a9c-110">Создание ссылки на сетевой регион</span><span class="sxs-lookup"><span data-stu-id="88a9c-110">To create a network region link</span></span>

1.  <span data-ttu-id="88a9c-111">Войдите на любой компьютер, находящийся во внутреннем развертывании, с использованием учетной записи, входящей в группу RTCUniversalServerAdmins (или имеющей равнозначные права пользователя) либо назначенной роли CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="88a9c-111">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="88a9c-112">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="88a9c-112">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="88a9c-113">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="88a9c-113">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="88a9c-114">На панели навигации слева выберите пункт **Настройка сети** , а затем щелкните **ссылку Region (регион**).</span><span class="sxs-lookup"><span data-stu-id="88a9c-114">In the left navigation bar, click **Network Configuration** and then click **Region Link**.</span></span>

4.  <span data-ttu-id="88a9c-115">На странице " **ссылка на регион** " нажмите кнопку **создать**.</span><span class="sxs-lookup"><span data-stu-id="88a9c-115">On the **Region Link** page, click **New**.</span></span>

5.  <span data-ttu-id="88a9c-116">В поле " **ссылка на новый регион**" введите значение из поля **имя** .</span><span class="sxs-lookup"><span data-stu-id="88a9c-116">In **New Region Link**, type a value in the **Name** field.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="88a9c-117">Это значение должно быть уникальным в рамках развертывания Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="88a9c-117">This value must be unique within your Lync Server 2013 deployment.</span></span>

    
    </div>

6.  <span data-ttu-id="88a9c-118">В раскрывающемся списке **сетевой регион \# 1** выберите один из двух областей, которые нужно связать.</span><span class="sxs-lookup"><span data-stu-id="88a9c-118">From the **Network region \#1** drop-down list, select one of the two regions to be linked.</span></span>

7.  <span data-ttu-id="88a9c-119">В раскрывающемся списке **сетевой регион \# 2** выберите другой регион, который нужно связать.</span><span class="sxs-lookup"><span data-stu-id="88a9c-119">From the **Network region \#2** drop-down list, select the other region to be linked.</span></span> <span data-ttu-id="88a9c-120">Этот регион должен отличаться от региона, выбранного для сетевого региона \# 1.</span><span class="sxs-lookup"><span data-stu-id="88a9c-120">This region must be different from the region selected for Network region \#1.</span></span>

8.  <span data-ttu-id="88a9c-121">Необязательно Если вы хотите помещать ограничения на пропускную способность для звуковых и видеозвонков в этих регионах, выберите профиль политики пропускной способности из раскрывающегося списка **политика пропускной способности** .</span><span class="sxs-lookup"><span data-stu-id="88a9c-121">(Optional) If you want to place bandwidth limitations on audio or video calls between these regions, select a bandwidth policy profile from the **Bandwidth policy** drop-down list.</span></span>

9.  <span data-ttu-id="88a9c-122">Нажмите **Исполнить**.</span><span class="sxs-lookup"><span data-stu-id="88a9c-122">Click **Commit**.</span></span>

</div>

<div>

## <a name="to-modify-a-network-region-link"></a><span data-ttu-id="88a9c-123">Изменение ссылки на сетевой регион</span><span class="sxs-lookup"><span data-stu-id="88a9c-123">To modify a network region link</span></span>

1.  <span data-ttu-id="88a9c-124">Войдите на любой компьютер, находящийся во внутреннем развертывании, с использованием учетной записи, входящей в группу RTCUniversalServerAdmins (или имеющей равнозначные права пользователя) либо назначенной роли CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="88a9c-124">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="88a9c-125">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="88a9c-125">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="88a9c-126">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="88a9c-126">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="88a9c-127">На панели навигации слева выберите пункт **Настройка сети** , а затем щелкните **ссылку Region (регион**).</span><span class="sxs-lookup"><span data-stu-id="88a9c-127">In the left navigation bar, click **Network Configuration** and then click **Region Link**.</span></span>

4.  <span data-ttu-id="88a9c-128">На странице " **ссылка на регион** " щелкните ссылку на область, которую вы хотите изменить.</span><span class="sxs-lookup"><span data-stu-id="88a9c-128">On the **Region Link** page, click the region link that you want to modify.</span></span>

5.  <span data-ttu-id="88a9c-129">В меню **Правка** щелкните **Подробнее**.</span><span class="sxs-lookup"><span data-stu-id="88a9c-129">On the **Edit** menu, click **Show details**.</span></span>

6.  <span data-ttu-id="88a9c-130">В **ссылке Изменить регион** можно изменить связанные с ней регионы или профиль политики пропускной способности для этой ссылки.</span><span class="sxs-lookup"><span data-stu-id="88a9c-130">In **Edit Region Link**, you can modify the regions that are linked or the bandwidth policy profile for this link.</span></span>

7.  <span data-ttu-id="88a9c-131">Нажмите **Исполнить**.</span><span class="sxs-lookup"><span data-stu-id="88a9c-131">Click **Commit**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="88a9c-132">См. также</span><span class="sxs-lookup"><span data-stu-id="88a9c-132">See Also</span></span>


[<span data-ttu-id="88a9c-133">Удаление ссылок на сетевой регион в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="88a9c-133">Deleting network region links in Lync Server 2013</span></span>](lync-server-2013-deleting-network-region-links.md)  


[<span data-ttu-id="88a9c-134">New-CsNetworkRegionLink</span><span class="sxs-lookup"><span data-stu-id="88a9c-134">New-CsNetworkRegionLink</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkRegionLink)  
[<span data-ttu-id="88a9c-135">Set-CsNetworkRegionLink</span><span class="sxs-lookup"><span data-stu-id="88a9c-135">Set-CsNetworkRegionLink</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsNetworkRegionLink)  
[<span data-ttu-id="88a9c-136">Remove-CsNetworkRegionLink</span><span class="sxs-lookup"><span data-stu-id="88a9c-136">Remove-CsNetworkRegionLink</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsNetworkRegionLink)  
[<span data-ttu-id="88a9c-137">Get-CsNetworkRegionLink</span><span class="sxs-lookup"><span data-stu-id="88a9c-137">Get-CsNetworkRegionLink</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkRegionLink)  
  

<span data-ttu-id="88a9c-138"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="88a9c-138"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>
