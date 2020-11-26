---
title: 'Lync Server 2013: удаление существующего сетевого сайта'
description: 'Lync Server 2013: удаление существующего сайта сети.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deleting an existing network site
ms:assetid: 2762149b-3572-4513-b838-beda7fa9e81e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688001(v=OCS.15)
ms:contentKeyID: 49733589
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7cef4774ee71aaf6851757d5b88d30138fc34997
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430359"
---
# <a name="deleting-an-existing-network-site-in-lync-server-2013"></a><span data-ttu-id="c226f-103">Удаление существующего сетевого сайта в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c226f-103">Deleting an existing network site in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c226f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c226f-104">

<span> </span></span></span>

<span data-ttu-id="c226f-105">_**Тема последнего изменения:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="c226f-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="c226f-106">Сетевые сайты — это офисы или места, настроенные в каждом регионе управления допуском звонков (CAC) или Улучшенное развертывание 9-1-1.</span><span class="sxs-lookup"><span data-stu-id="c226f-106">Network sites are the offices or locations configured within each region of a call admission control (CAC) or Enhanced 9-1-1 deployment.</span></span> <span data-ttu-id="c226f-107">Вы можете настроить сайты и связать их с областями с помощью панели управления Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c226f-107">You can use the Lync Server 2013 Control Panel to configure sites and associate them with regions.</span></span> <span data-ttu-id="c226f-108">Например, сетевой регион для Северной Америки может быть связан с сайтами сети, например в Чикаго, Redmond и Vancouver.</span><span class="sxs-lookup"><span data-stu-id="c226f-108">For example, a network region for North America might be associated with networks sites such as Chicago, Redmond, and Vancouver.</span></span> <span data-ttu-id="c226f-109">Сайт сети CAC должен создаваться для каждого сайта в Организации, даже если на нем нет ограничений по пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="c226f-109">A CAC network site must be created for every site within an organization, even if that site has no bandwidth limitations.</span></span> <span data-ttu-id="c226f-110">На панели управления Lync Server вы можете создавать, изменять и удалять сетевые сайты.</span><span class="sxs-lookup"><span data-stu-id="c226f-110">From the Lync Server Control Panel you can create, modify, and delete network sites.</span></span> <span data-ttu-id="c226f-111">Чтобы удалить существующий сайт сети, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="c226f-111">Use the following procedure to delete an existing network site.</span></span> <span data-ttu-id="c226f-112">Сведения о создании и изменении сайтов сети можно найти [в разделе Создание или изменение сетевых сайтов в Lync Server 2013](lync-server-2013-creating-or-modifying-network-sites.md)</span><span class="sxs-lookup"><span data-stu-id="c226f-112">For details about creating or modifying network sites, see [Creating or modifying network sites in Lync Server 2013](lync-server-2013-creating-or-modifying-network-sites.md)</span></span>

<div>

## <a name="to-delete-a-network-site"></a><span data-ttu-id="c226f-113">Удаление сайта сети</span><span class="sxs-lookup"><span data-stu-id="c226f-113">To delete a network site</span></span>

1.  <span data-ttu-id="c226f-114">Войдите на любой компьютер, находящийся во внутреннем развертывании, с использованием учетной записи, входящей в группу RTCUniversalServerAdmins (или имеющей равнозначные права пользователя) либо назначенной роли CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="c226f-114">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="c226f-115">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="c226f-115">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="c226f-116">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="c226f-116">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="c226f-117">На панели навигации слева выберите пункт **Настройка сети** , а затем — **сайт**.</span><span class="sxs-lookup"><span data-stu-id="c226f-117">In the left navigation bar, click **Network Configuration** and then click **Site**.</span></span>

4.  <span data-ttu-id="c226f-118">На странице **сайта** выберите сайт, который вы хотите удалить.</span><span class="sxs-lookup"><span data-stu-id="c226f-118">On the **Site** page, click the site that you want to delete.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="c226f-119">За один раз можно удалить сразу несколько сайтов.</span><span class="sxs-lookup"><span data-stu-id="c226f-119">You can delete more than one site at a time.</span></span> <span data-ttu-id="c226f-120">Для этого нажмите клавишу CTRL и, удерживая нажатой клавишу CTRL, щелкните несколько сайтов.</span><span class="sxs-lookup"><span data-stu-id="c226f-120">To do this, press CTRL and select multiple sites while holding down the CTRL key.</span></span> <span data-ttu-id="c226f-121">Кроме того, чтобы выбрать все сайты, в меню <STRONG>Правка</STRONG> выберите команду <STRONG>выделить все</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="c226f-121">Or, to select all sites, click <STRONG>Select all</STRONG> on the <STRONG>Edit</STRONG> menu.</span></span>

    
    </div>

5.  <span data-ttu-id="c226f-122">В меню **Правка** выберите команду **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="c226f-122">On the **Edit** menu, click **Delete**.</span></span>

6.  <span data-ttu-id="c226f-123">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="c226f-123">Click **OK**.</span></span>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="c226f-124">Вы не можете удалить сайт сети, если он связан с сетевой подсетью.</span><span class="sxs-lookup"><span data-stu-id="c226f-124">You cannot remove a network site if it is associated with a network subnet.</span></span> <span data-ttu-id="c226f-125">При попытке удалить сайт, связанный с подсетью, появится сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="c226f-125">If you attempt to remove a site associated with a subnet you will receive an error message.</span></span> <span data-ttu-id="c226f-126">Чтобы проверить, связан ли сайт с подсетями, щелкните его, а затем в меню <STRONG>Правка</STRONG> выберите команду <STRONG>Показать подробности</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="c226f-126">To see if a site is associated with any subnets, click the site and then click <STRONG>Show details</STRONG> on the <STRONG>Edit</STRONG> menu.</span></span>

    
    <span data-ttu-id="c226f-127"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c226f-127"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

