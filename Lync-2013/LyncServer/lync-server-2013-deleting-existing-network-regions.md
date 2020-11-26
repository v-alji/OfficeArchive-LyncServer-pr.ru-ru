---
title: 'Lync Server 2013: удаление существующих областей сети'
description: 'Lync Server 2013: удаление существующих областей сети.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deleting existing network regions
ms:assetid: c7293a2f-2b49-4c4a-903f-f7edcea2bc5f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721882(v=OCS.15)
ms:contentKeyID: 49733815
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b148f0bd92ad398ab7057a5a291bf3245df3e47e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430324"
---
# <a name="deleting-existing-network-regions-in-lync-server-2013"></a><span data-ttu-id="b472c-103">Удаление существующих областей сети в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b472c-103">Deleting existing network regions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b472c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b472c-104">

<span> </span></span></span>

<span data-ttu-id="b472c-105">_**Тема последнего изменения:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="b472c-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="b472c-106">Сетевой регион соединяет различные части сети в нескольких географических регионах.</span><span class="sxs-lookup"><span data-stu-id="b472c-106">A network region interconnects various parts of a network across multiple geographic areas.</span></span> <span data-ttu-id="b472c-107">Каждый сетевой регион должен быть связан с центральным сайтом.</span><span class="sxs-lookup"><span data-stu-id="b472c-107">Every network region must be associated with a central site.</span></span> <span data-ttu-id="b472c-108">Центральный сайт — это сайт центра обработки данных, на котором запущена служба политики "Управление допуском звонков" (CAC).</span><span class="sxs-lookup"><span data-stu-id="b472c-108">The central site is the data center site on which the call admission control (CAC) bandwidth policy service is running.</span></span> <span data-ttu-id="b472c-109">Вы можете настроить регионы сети с помощью панели управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b472c-109">You can use Lync Server Control Panel to configure network regions.</span></span> <span data-ttu-id="b472c-110">Сетевые регионы включают параметры, определяющие, разрешены ли для аудио-и видеоподключений альтернативные пути через Интернет.</span><span class="sxs-lookup"><span data-stu-id="b472c-110">Network regions include settings that determine whether alternate paths through the Internet are allowed for audio and video connections.</span></span> <span data-ttu-id="b472c-111">С помощью панели управления Lync Server вы можете создавать, изменять и удалять сетевые регионы.</span><span class="sxs-lookup"><span data-stu-id="b472c-111">From the Lync Server Control Panel, you can create, modify, or delete a network region.</span></span> <span data-ttu-id="b472c-112">Используйте этот раздел для удаления существующих областей сети.</span><span class="sxs-lookup"><span data-stu-id="b472c-112">Use this topic to delete existing network regions.</span></span> <span data-ttu-id="b472c-113">Дополнительные сведения о создании и изменении существующих областей сети можно найти [в разделе Создание или изменение областей сети в Lync Server 2013](lync-server-2013-creating-or-modifying-network-regions.md).</span><span class="sxs-lookup"><span data-stu-id="b472c-113">For details about creating or modifying existing network regions, see [Creating or modifying network regions in Lync Server 2013](lync-server-2013-creating-or-modifying-network-regions.md).</span></span>

<div>

## <a name="to-delete-a-network-region"></a><span data-ttu-id="b472c-114">Удаление сетевого региона</span><span class="sxs-lookup"><span data-stu-id="b472c-114">To delete a network region</span></span>

1.  <span data-ttu-id="b472c-115">Войдите на любой компьютер, находящийся во внутреннем развертывании, с использованием учетной записи, входящей в группу RTCUniversalServerAdmins (или имеющей равнозначные права пользователя) либо назначенной роли CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="b472c-115">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="b472c-116">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b472c-116">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="b472c-117">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="b472c-117">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="b472c-118">На панели навигации слева выберите пункт **Настройка сети** , а затем — **регион**.</span><span class="sxs-lookup"><span data-stu-id="b472c-118">In the left navigation bar, click **Network Configuration** and then click **Region**.</span></span>

4.  <span data-ttu-id="b472c-119">На странице **регион** выберите область, которую вы хотите удалить.</span><span class="sxs-lookup"><span data-stu-id="b472c-119">On the **Region** page, click the region you want to delete.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="b472c-120">За один раз можно удалить несколько областей.</span><span class="sxs-lookup"><span data-stu-id="b472c-120">You can delete more than one region at a time.</span></span> <span data-ttu-id="b472c-121">Для этого нажмите клавишу CTRL и, удерживая нажатой клавишу CTRL, щелкните несколько областей.</span><span class="sxs-lookup"><span data-stu-id="b472c-121">To do this, press CTRL and select multiple regions while holding down the CTRL key.</span></span> <span data-ttu-id="b472c-122">Кроме того, чтобы выделить все области, в меню <STRONG>Правка</STRONG> выберите команду <STRONG>выделить все</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="b472c-122">Or, to select all regions, click <STRONG>Select all</STRONG> on the <STRONG>Edit</STRONG> menu.</span></span>

    
    </div>

5.  <span data-ttu-id="b472c-123">В меню **Правка** выберите команду **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="b472c-123">On the **Edit** menu, click **Delete**.</span></span>

6.  <span data-ttu-id="b472c-124">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b472c-124">Click **OK**.</span></span>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="b472c-125">Сетевая область не может быть удалена, если она связана с сетевым сайтом.</span><span class="sxs-lookup"><span data-stu-id="b472c-125">A network region cannot be removed if it is associated with a network site.</span></span> <span data-ttu-id="b472c-126">При попытке удалить регион, связанный с сайтом, появится сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="b472c-126">If you attempt to remove a region associated with a site you will receive an error message.</span></span> <span data-ttu-id="b472c-127">Чтобы узнать, связана ли область с любыми сайтами, выберите ее, а затем в меню <STRONG>Правка</STRONG> выберите команду <STRONG>Показать подробности</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="b472c-127">To see if a region is associated with any sites, select the region and then click <STRONG>Show details</STRONG> on the <STRONG>Edit</STRONG> menu.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="b472c-128">См. также</span><span class="sxs-lookup"><span data-stu-id="b472c-128">See Also</span></span>


[<span data-ttu-id="b472c-129">Создание и изменение областей сети в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b472c-129">Creating or modifying network regions in Lync Server 2013</span></span>](lync-server-2013-creating-or-modifying-network-regions.md)  
  

<span data-ttu-id="b472c-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b472c-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

