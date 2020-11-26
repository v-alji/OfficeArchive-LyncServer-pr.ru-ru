---
title: Проверка сведений о топологии
description: Проверьте сведения о топологии.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Verify topology information
ms:assetid: aa4c424e-f87c-4be6-8df6-a0cd193b11fc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205151(v=OCS.15)
ms:contentKeyID: 48185046
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2ed41cd95fffdca629e710dcf443631d0c74c69e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440123"
---
# <a name="verify-topology-information"></a><span data-ttu-id="d0074-103">Проверка сведений о топологии</span><span class="sxs-lookup"><span data-stu-id="d0074-103">Verify topology information</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d0074-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d0074-104">

<span> </span></span></span>

<span data-ttu-id="d0074-105">_**Тема последнего изменения:** 2012-09-26_</span><span class="sxs-lookup"><span data-stu-id="d0074-105">_**Topic Last Modified:** 2012-09-26_</span></span>

<span data-ttu-id="d0074-106">Первый этап проверки успешности слияния — Просмотр сведений о топологии Office Communications Server 2007 R2, которые вы объединили с помощью Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d0074-106">The first step in verifying the merge completed successfully is to view the Office Communications Server 2007 R2 topology information that you merged with Lync Server 2013.</span></span> <span data-ttu-id="d0074-107">В построителе топологии в узле **BackCompatSite** отображается полное доменное имя (FQDN) для каждого пула и сервера Office Communications Server 2007 R2, который вы объединили.</span><span class="sxs-lookup"><span data-stu-id="d0074-107">In Topology Builder, the **BackCompatSite** node displays the fully qualified domain name (FQDN) of each Office Communications Server 2007 R2 pool and server that you merged.</span></span>

<div>

## <a name="to-view-backcompatsite-in-topology-builder"></a><span data-ttu-id="d0074-108">Просмотр BackCompatSite в построителе топологии</span><span class="sxs-lookup"><span data-stu-id="d0074-108">To view BackCompatSite in Topology Builder</span></span>

1.  <span data-ttu-id="d0074-109">В среде Office Communications Server 2007 R2 откройте средство администрирования Office Communications Server 2007 R2 и запомните полные доменные имена старых пулов и серверов.</span><span class="sxs-lookup"><span data-stu-id="d0074-109">In your Office Communications Server 2007 R2 environment, open the Office Communications Server 2007 R2 administrative tool and note the FQDNs of the legacy pools and servers.</span></span>

2.  <span data-ttu-id="d0074-110">В среде Lync Server 2013 откройте "Построитель топологии", а затем разверните узел **BackCompatSite** .</span><span class="sxs-lookup"><span data-stu-id="d0074-110">In your Lync Server 2013 environment, open Topology Builder and then expand the **BackCompatSite** node.</span></span>

3.  <span data-ttu-id="d0074-111">Убедитесь в том, что полные доменные имена для объединяемых пулов и серверов отображены.</span><span class="sxs-lookup"><span data-stu-id="d0074-111">Verify that the FQDNs for the pools and servers that you merge are displayed.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="d0074-112">В <STRONG>BackCompatSite</STRONG> не отображаются никакие данные для ролей сервера, размещенных на сервере переднего плана или стандартном сервере Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="d0074-112">You do not see any information in <STRONG>BackCompatSite</STRONG> for server roles that are collocated on a Front End Server or Standard Edition server.</span></span> <span data-ttu-id="d0074-113">Показаны только роли сервера, необходимые для взаимодействия между Office Communications Server 2007 R2 и Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d0074-113">Only server roles that are required for interoperability between Office Communications Server 2007 R2 and Lync Server 2013 are shown.</span></span>

    
    </div>

<span data-ttu-id="d0074-114">![Диалоговое окно "BackCompatSite Topology Builder"](images/JJ205243.62751c76-f018-4c6d-bb48-c61ef8974d31(OCS.15).jpg "Диалоговое окно "BackCompatSite Topology Builder"")</span><span class="sxs-lookup"><span data-stu-id="d0074-114">![Topology Builder BackCompatSite dialog box](images/JJ205243.62751c76-f018-4c6d-bb48-c61ef8974d31(OCS.15).jpg "Topology Builder BackCompatSite dialog box")</span></span>

<span data-ttu-id="d0074-115">Вы также можете использовать панель управления Lync Server 2013, чтобы просмотреть объединенную топологию.</span><span class="sxs-lookup"><span data-stu-id="d0074-115">You can also use Lync Server 2013 Control Panel to view your merged topology.</span></span> <span data-ttu-id="d0074-116">В панели управления Lync Server 2013 вы можете просмотреть полные доменные имена серверов, FQDN и имя пула для объединенной топологии.</span><span class="sxs-lookup"><span data-stu-id="d0074-116">In Lync Server 2013 Control Panel, you can see each server FQDN, pool FQDN, and site name for your merged topology.</span></span> <span data-ttu-id="d0074-117">У Объединенных серверов есть имя **сайта** **BackCompatSite**.</span><span class="sxs-lookup"><span data-stu-id="d0074-117">Merged servers have a **Site** name of **BackCompatSite**.</span></span>

</div>

<div>

## <a name="to-view-the-merged-topology-in-lync-server-2013-control-panel"></a><span data-ttu-id="d0074-118">Просмотр объединенной топологии в Lync Server 2013 панели управления</span><span class="sxs-lookup"><span data-stu-id="d0074-118">To view the merged topology in Lync Server 2013 Control Panel</span></span>

1.  <span data-ttu-id="d0074-119">Откройте панель управления Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d0074-119">Open Lync Server 2013 Control Panel.</span></span>

2.  <span data-ttu-id="d0074-120">Нажмите **топология**.</span><span class="sxs-lookup"><span data-stu-id="d0074-120">Click **Topology**.</span></span>

3.  <span data-ttu-id="d0074-121">На вкладке **Status (состояние** ) убедитесь в том, что Объединенные серверы и пулы отображаются по столбцу " **сайт** ", выполнив поиск **BackCompatSite** .</span><span class="sxs-lookup"><span data-stu-id="d0074-121">On the **Status** tab, verify that servers and pools you merged appear by looking for **BackCompatSite** in the **Site** column.</span></span>

<span data-ttu-id="d0074-122">![Объединенная топология на панели управления сервера Lync Server](images/JJ205151.f986ddd4-2040-454d-9389-7f6154b59cc9(OCS.15).jpg "Объединенная топология на панели управления сервера Lync Server")</span><span class="sxs-lookup"><span data-stu-id="d0074-122">![Lync Server Control Panel showing merged topology](images/JJ205151.f986ddd4-2040-454d-9389-7f6154b59cc9(OCS.15).jpg "Lync Server Control Panel showing merged topology")</span></span>

<span data-ttu-id="d0074-123">Чтобы просмотреть дополнительные сведения о объединенном пуле, используйте командлет **Get-CsPool** .</span><span class="sxs-lookup"><span data-stu-id="d0074-123">To see more detail about a merged pool, use the **Get-CsPool** cmdlet.</span></span> <span data-ttu-id="d0074-124">В дополнение к сведениям, доступным в построителе топологии и панели управления Lync Server 2013, в этом командлете выводятся службы, которые выполняются в пуле Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d0074-124">In addition to the information that is available in Topology Builder and Lync Server 2013 Control Panel, this cmdlet displays the services that run on the Lync Server 2013 pool.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="d0074-125">После публикации топологии после запуска мастера слияния в построителе топологии каталоги конференций объединяются в Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d0074-125">When you publish the topology after running the Merge wizard in Topology Builder, conference directories are merged to Lync Server 2013.</span></span> <span data-ttu-id="d0074-126">Каталоги конференций можно проверить, запустив командлет <STRONG>Get-CsConferenceDirectory</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="d0074-126">Conference directories can be verified by running the <STRONG>Get-CsConferenceDirectory</STRONG> cmdlet.</span></span>



</div>

</div>

<div>

## <a name="to-view-services-on-a-merged-pool"></a><span data-ttu-id="d0074-127">Просмотр служб в Объединенном пуле</span><span class="sxs-lookup"><span data-stu-id="d0074-127">To view services on a merged pool</span></span>

1.  <span data-ttu-id="d0074-128">Откройте консоль управления Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d0074-128">Open the Lync Server 2013 Management Shell.</span></span>

2.  <span data-ttu-id="d0074-129">В командной строке введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="d0074-129">At the command line, type the following:</span></span>
    
        Get-CsPool [-Identity <FQDN of the pool>]
    
    <span data-ttu-id="d0074-130">Например:</span><span class="sxs-lookup"><span data-stu-id="d0074-130">For example:</span></span>
    
        Get-CsPool -Identity pool02.contoso.net

</div>

<div>

## <a name="to-verify-conference-directories-merged"></a><span data-ttu-id="d0074-131">Проверка Объединенных каталогов конференций</span><span class="sxs-lookup"><span data-stu-id="d0074-131">To verify conference directories merged</span></span>

1.  <span data-ttu-id="d0074-132">Откройте консоль управления Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d0074-132">Open the Lync Server 2013 Management Shell.</span></span>

2.  <span data-ttu-id="d0074-133">В командной строке введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="d0074-133">At the command line, type the following:</span></span>
    
        Get-CsConferenceDirectory

3.  <span data-ttu-id="d0074-134">Убедитесь в том, что все каталоги конференций для пула или сервера, который вы собираетесь объединять, теперь находятся в Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d0074-134">Verify that all the conference directories for the pool or server you are merging are now in Lync Server 2013.</span></span>

<span data-ttu-id="d0074-135"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d0074-135"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

