---
title: 'Lync Server 2013: развертывание регионов сети, сайтов и подсетей'
description: 'Lync Server 2013: развертывание регионов сети, сайтов и подсетей.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying network regions, sites, and subnets
ms:assetid: c4b75601-3538-4d07-8d23-1ad90459ae48
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994067(v=OCS.15)
ms:contentKeyID: 51803978
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f1c4c08cd9b78b1439000cdb4a7bbe3ffc2f99d8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429848"
---
# <a name="deploying-network-regions-sites-and-subnets-in-lync-server-2013"></a><span data-ttu-id="f5424-103">Развертывание регионов сети, сайтов и подсетей в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f5424-103">Deploying network regions, sites, and subnets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f5424-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f5424-104">

<span> </span></span></span>

<span data-ttu-id="f5424-105">_**Тема последнего изменения:** 2013-03-12_</span><span class="sxs-lookup"><span data-stu-id="f5424-105">_**Topic Last Modified:** 2013-03-12_</span></span>

<span data-ttu-id="f5424-106">После развертывания корпоративной голосовой связи необходимо настроить следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="f5424-106">Once Enterprise Voice is deployed, you need to configure:</span></span>

  - <span data-ttu-id="f5424-107">Регионы сети</span><span class="sxs-lookup"><span data-stu-id="f5424-107">Network regions</span></span>

  - <span data-ttu-id="f5424-108">Сетевые сайты</span><span class="sxs-lookup"><span data-stu-id="f5424-108">Network sites</span></span>

  - <span data-ttu-id="f5424-109">Сетевые подсети</span><span class="sxs-lookup"><span data-stu-id="f5424-109">Network subnets</span></span>

<div>

## <a name="define-network-regions"></a><span data-ttu-id="f5424-110">Определение регионов сети</span><span class="sxs-lookup"><span data-stu-id="f5424-110">Define Network Regions</span></span>

<span data-ttu-id="f5424-111">С помощью команды Lync Server Windows PowerShell, панели управления New-CsNetworkRegion или Lync Server можно определять регионы сети.</span><span class="sxs-lookup"><span data-stu-id="f5424-111">Use the Lync Server Windows PowerShell command, New-CsNetworkRegion, or Lync Server Control Panel to define network regions.</span></span>

    New-CsNetworkRegion -NetworkRegionID <region ID> -CentralSite <site ID>

<span data-ttu-id="f5424-112">Дополнительные сведения можно найти в разделе [New-CsNetworkRegion](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkRegion).</span><span class="sxs-lookup"><span data-stu-id="f5424-112">For more information, see [New-CsNetworkRegion](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkRegion).</span></span>

<span data-ttu-id="f5424-113">В этом примере Следующая команда Windows PowerShell иллюстрирует сетевую область, область 1 (Индия), определенную в этом сценарии.</span><span class="sxs-lookup"><span data-stu-id="f5424-113">For this example, the following Windows PowerShell command illustrates the network region, region 1 (India), defined in this scenario.</span></span>

    New-CsNetworkRegion -NetworkRegionID "India" -CentralSite "India Central Site"

<div>


</div>

</div>

<div>

## <a name="define-network-sites"></a><span data-ttu-id="f5424-114">Определение сетевых сайтов</span><span class="sxs-lookup"><span data-stu-id="f5424-114">Define Network Sites</span></span>

<span data-ttu-id="f5424-115">С помощью команды Lync Server Windows PowerShell, New-CsNetworkSite или панели управления Lync Server можно определять сетевые сайты.</span><span class="sxs-lookup"><span data-stu-id="f5424-115">Use the Lync Server Windows PowerShell command, New-CsNetworkSite, or the Lync Server Control Panel to define network sites.</span></span>

    New-CsNetworkSite -NetworkSiteID <site ID> -NetworkRegionID <region ID>

<span data-ttu-id="f5424-116">Дополнительные сведения можно найти в разделе [New-CsNetworkSite](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkSite).</span><span class="sxs-lookup"><span data-stu-id="f5424-116">For more information, see [New-CsNetworkSite](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkSite).</span></span>

<span data-ttu-id="f5424-117">В этом примере в приведенной ниже таблице и команде Windows PowerShell для Lync Server показаны сетевые сайты, определенные в этом сценарии.</span><span class="sxs-lookup"><span data-stu-id="f5424-117">For this example, the following table and Lync Server Windows PowerShell command illustrate the network sites defined in this scenario.</span></span> <span data-ttu-id="f5424-118">Только те параметры, которые относятся к Location-Based маршрутизации, включены в таблицу для целей иллюстрации.</span><span class="sxs-lookup"><span data-stu-id="f5424-118">Only settings that are specific to Location-Based Routing are included in the table for illustration purposes.</span></span>

    New-CsNetworkSite -NetworkSiteID "Delhi" -NetworkRegionID "India"
    New-CsNetworkSite -NetworkSiteID "Hyderabad" -NetworkRegionID "India"


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="f5424-119">Сайт 1 (Delhi)</span><span class="sxs-lookup"><span data-stu-id="f5424-119">Site 1 (Delhi)</span></span></th>
<th><span data-ttu-id="f5424-120">Сайт 2 (Hyderabad)</span><span class="sxs-lookup"><span data-stu-id="f5424-120">Site 2 (Hyderabad)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f5424-121">Идентификатор сайта</span><span class="sxs-lookup"><span data-stu-id="f5424-121">Site ID</span></span></p></td>
<td><p><span data-ttu-id="f5424-122">Сайт 1 (Delhi)</span><span class="sxs-lookup"><span data-stu-id="f5424-122">Site 1 (Delhi)</span></span></p></td>
<td><p><span data-ttu-id="f5424-123">Сайт 2 (Hyderabad)</span><span class="sxs-lookup"><span data-stu-id="f5424-123">Site 2 (Hyderabad)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5424-124">КОД региона</span><span class="sxs-lookup"><span data-stu-id="f5424-124">Region ID</span></span></p></td>
<td><p><span data-ttu-id="f5424-125">Регион 1 (Индия)</span><span class="sxs-lookup"><span data-stu-id="f5424-125">Region 1 (India)</span></span></p></td>
<td><p><span data-ttu-id="f5424-126">Регион 1 (Индия)</span><span class="sxs-lookup"><span data-stu-id="f5424-126">Region 1 (India)</span></span></p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="define-network-subnets"></a><span data-ttu-id="f5424-127">Определение подсетей сети</span><span class="sxs-lookup"><span data-stu-id="f5424-127">Define Network Subnets</span></span>

<span data-ttu-id="f5424-128">С помощью команды Lync Server Windows PowerShell, New-CsNetworkSubnet или панели управления Lync Server можно определять сетевые подсети и назначать их сетевым сайтам.</span><span class="sxs-lookup"><span data-stu-id="f5424-128">Use the Lync Server Windows PowerShell command, New-CsNetworkSubnet, or the Lync Server Control Panel to define network subnets and assign them to network sites.</span></span>

    New-CsNetworkSubnet -SubnetID <Subnet IP address> -MaskBits <Subnet bitmask> -NetworkSiteID <site ID>

<span data-ttu-id="f5424-129">Дополнительные сведения можно найти в разделе [New-CsNetworkSubnet](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkSubnet).</span><span class="sxs-lookup"><span data-stu-id="f5424-129">For more information, see [New-CsNetworkSubnet](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkSubnet).</span></span>

<span data-ttu-id="f5424-130">В этом примере приведенная ниже таблица и команды Windows PowerShell иллюстрируют Назначение сетевых подсетей сетевым сайтам, Delhi и Hyderabad, определенным в этом сценарии.</span><span class="sxs-lookup"><span data-stu-id="f5424-130">For this example, the following table and Windows PowerShell commands illustrate the assignment of network subnets to the network sites, Delhi and Hyderabad, defined in this scenario.</span></span> <span data-ttu-id="f5424-131">Только те параметры, которые относятся к Location-Based маршрутизации, включены в таблицу для целей иллюстрации.</span><span class="sxs-lookup"><span data-stu-id="f5424-131">Only settings that are specific to Location-Based Routing are included in the table for illustration purposes.</span></span>

    New-CsNetworkSubnet -SubnetID "192.168.0.0" -MaskBits "24" -NetworkSiteID "Delhi"
    New-CsNetworkSubnet -SubnetID "192.168.1.0" -MaskBits "24" -NetworkSiteID "Hyderabad"


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="f5424-132">Сайт 1 (Delhi)</span><span class="sxs-lookup"><span data-stu-id="f5424-132">Site 1 (Delhi)</span></span></th>
<th><span data-ttu-id="f5424-133">Сайт 2 (Hyderabad)</span><span class="sxs-lookup"><span data-stu-id="f5424-133">Site 2 (Hyderabad)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f5424-134">КОД подсети</span><span class="sxs-lookup"><span data-stu-id="f5424-134">Subnet ID</span></span></p></td>
<td><p><span data-ttu-id="f5424-135">172.16.0.0</span><span class="sxs-lookup"><span data-stu-id="f5424-135">192.168.0.0</span></span></p></td>
<td><p><span data-ttu-id="f5424-136">192.168.1.0</span><span class="sxs-lookup"><span data-stu-id="f5424-136">192.168.1.0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5424-137">Маски</span><span class="sxs-lookup"><span data-stu-id="f5424-137">Mask</span></span></p></td>
<td><p><span data-ttu-id="f5424-138">24</span><span class="sxs-lookup"><span data-stu-id="f5424-138">24</span></span></p></td>
<td><p><span data-ttu-id="f5424-139">24</span><span class="sxs-lookup"><span data-stu-id="f5424-139">24</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5424-140">Идентификатор сайта</span><span class="sxs-lookup"><span data-stu-id="f5424-140">Site ID</span></span></p></td>
<td><p><span data-ttu-id="f5424-141">Сайт 1 (Delhi)</span><span class="sxs-lookup"><span data-stu-id="f5424-141">Site 1 (Delhi)</span></span></p></td>
<td><p><span data-ttu-id="f5424-142">Сайт 2 (Hyderabad)</span><span class="sxs-lookup"><span data-stu-id="f5424-142">Site 2 (Hyderabad)</span></span></p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="f5424-143">См. также</span><span class="sxs-lookup"><span data-stu-id="f5424-143">See Also</span></span>


[<span data-ttu-id="f5424-144">Настройка маршрутизации на основе расположения в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f5424-144">Configuring Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-configuring-location-based-routing.md)  
  

<span data-ttu-id="f5424-145"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f5424-145"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

