---
title: 'Lync Server 2013: Включение маршрутизации Location-Based'
description: 'Lync Server 2013: Включение маршрутизации Location-Based.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enabling Location-Based Routing
ms:assetid: 029ede7e-0c4e-4ad2-af99-909ae674d6fe
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994014(v=OCS.15)
ms:contentKeyID: 51803920
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7844af5792468cd5645b6b42c857c63b943c2df1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399286"
---
# <a name="enabling-location-based-routing-in-lync-server-2013"></a><span data-ttu-id="f16ec-103">Включение маршрутизации Location-Based в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f16ec-103">Enabling Location-Based Routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f16ec-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f16ec-104">

<span> </span></span></span>

<span data-ttu-id="f16ec-105">_**Тема последнего изменения:** 2013-04-26_</span><span class="sxs-lookup"><span data-stu-id="f16ec-105">_**Topic Last Modified:** 2013-04-26_</span></span>

<span data-ttu-id="f16ec-106">После развертывания корпоративной голосовой почты и регионов сети, сайтов и подсетей вы можете включить Location-Based маршрутизацию.</span><span class="sxs-lookup"><span data-stu-id="f16ec-106">Once Enterprise Voice is deployed and network regions, sites and subnets are defined, you can enable Location-Based Routing.</span></span> <span data-ttu-id="f16ec-107">Для следующих корпоративных элементов голосовой связи необходимо включить Location-Based маршрутизации:</span><span class="sxs-lookup"><span data-stu-id="f16ec-107">Location-Based Routing must be enabled for the following Enterprise Voice elements:</span></span>

  - <span data-ttu-id="f16ec-108">Сетевые сайты</span><span class="sxs-lookup"><span data-stu-id="f16ec-108">Network sites</span></span>

  - <span data-ttu-id="f16ec-109">Конфигурации магистрали</span><span class="sxs-lookup"><span data-stu-id="f16ec-109">Trunk configurations</span></span>

  - <span data-ttu-id="f16ec-110">Политики голосовой связи</span><span class="sxs-lookup"><span data-stu-id="f16ec-110">Voice policies</span></span>

  - <span data-ttu-id="f16ec-111">Настройка маршрутизации</span><span class="sxs-lookup"><span data-stu-id="f16ec-111">Routing configuration</span></span>

<div>

## <a name="enable-location-based-routing-to-network-sites"></a><span data-ttu-id="f16ec-112">Включение маршрутизации Location-Based на сайты сети</span><span class="sxs-lookup"><span data-stu-id="f16ec-112">Enable Location-Based Routing to Network Sites</span></span>

<span data-ttu-id="f16ec-113">После того как вы развернули корпоративный голос и настроили сетевые сайты, вы можете настроить маршрутизацию Location-Based.</span><span class="sxs-lookup"><span data-stu-id="f16ec-113">After you have deployed Enterprise Voice, and configured network sites, you are ready to configure Location-Based Routing.</span></span> <span data-ttu-id="f16ec-114">Сначала необходимо создать политику маршрутизации голосовой связи для связи сайта сети с соответствующими использованием PSTN.</span><span class="sxs-lookup"><span data-stu-id="f16ec-114">First, you create a voice routing policy to associate the network site with the appropriate PSTN usages.</span></span> <span data-ttu-id="f16ec-115">Когда вы назначаете использование PSTN для политики голосовой маршрутизации, убедитесь в том, что используются только использование PSTN, связанное с голосовыми маршрутами, которые используют локальный шлюз для сайта или шлюза PSTN, который находится в регионе, где не требуется Location-Based ограничения маршрутизации. С помощью команды Lync Server Windows PowerShell, панели управления New-CsVoiceRoutingPolicy или Lync Server можно создавать политики голосовой маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="f16ec-115">When assigning PSTN usages to a voice routing policy, make sure to only use PSTN usages that are associated to voice routes that use a PSTN gateway local to the site or a PSTN gateway that is located in a region where Location-Based Routing restrictions are not needed.Use the Lync Server Windows PowerShell command, New-CsVoiceRoutingPolicy, or Lync Server Control Panel to create voice routing policies.</span></span>

    New-CsVoiceRoutingPolicy -Identity <voice routing policy ID> -Name <voice routing policy name> -PstnUsages <usages>

<span data-ttu-id="f16ec-116">Дополнительные сведения см. в разделе [New-CsVoiceRoutingPolicy](https://docs.microsoft.com/powershell/module/skype/New-CsVoiceRoutingPolicy).</span><span class="sxs-lookup"><span data-stu-id="f16ec-116">For more information, see [New-CsVoiceRoutingPolicy](https://docs.microsoft.com/powershell/module/skype/New-CsVoiceRoutingPolicy).</span></span>

<span data-ttu-id="f16ec-117">В этом примере приведенная ниже таблица и команды Windows PowerShell иллюстрируют две политики маршрутизации голосовой связи и использование PSTN, описанных в этом сценарии.</span><span class="sxs-lookup"><span data-stu-id="f16ec-117">For this example, the following table and Windows PowerShell commands illustrate two voice routing policies and their associated PSTN usages defined in this scenario.</span></span> <span data-ttu-id="f16ec-118">Только те параметры, которые относятся к Location-Based маршрутизации, включены в таблицу для целей иллюстрации.</span><span class="sxs-lookup"><span data-stu-id="f16ec-118">Only settings that are specific to Location-Based Routing are included in the table for illustration purposes.</span></span>

    New-CsVoiceRoutingPolicy -Identity "DelhiVoiceRoutingPolicy" -Name "Delhi voice routing policy" -PstnUsages @{add="Delhi usage", "PBX Del usage", "PBX Hyd usage"}
    New-CsVoiceRoutingPolicy -Identity "HyderabadVoiceRoutingPolicy" -Name " Hyderabad voice routing policy" -PstnUsages @{add="Hyderabad usage", "PBX Del usage", "PBX Hyd usage"}


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="f16ec-119">Политика маршрутизации голосовой связи 1</span><span class="sxs-lookup"><span data-stu-id="f16ec-119">Voice routing policy 1</span></span></th>
<th><span data-ttu-id="f16ec-120">Политика маршрутизации голосовой связи 2</span><span class="sxs-lookup"><span data-stu-id="f16ec-120">Voice routing policy 2</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f16ec-121">Идентификатор политики голосовой связи</span><span class="sxs-lookup"><span data-stu-id="f16ec-121">Voice policy ID</span></span></p></td>
<td><p><span data-ttu-id="f16ec-122">Политика маршрутизации голосовой связи Delhi</span><span class="sxs-lookup"><span data-stu-id="f16ec-122">Delhi voice routing policy</span></span></p></td>
<td><p><span data-ttu-id="f16ec-123">Политика маршрутизации голосовой связи Hyderabad</span><span class="sxs-lookup"><span data-stu-id="f16ec-123">Hyderabad voice routing policy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f16ec-124">Использование PSTN</span><span class="sxs-lookup"><span data-stu-id="f16ec-124">PSTN usages</span></span></p></td>
<td><p><span data-ttu-id="f16ec-125">Использование Delhi, использование АТС DELETE, использование Hyd УАТС</span><span class="sxs-lookup"><span data-stu-id="f16ec-125">Delhi usage, PBX Del usage, PBX Hyd usage</span></span></p></td>
<td><p><span data-ttu-id="f16ec-126">Использование Hyderabad, Hyd УАТС, использование АТС Delete</span><span class="sxs-lookup"><span data-stu-id="f16ec-126">Hyderabad usage, PBX Hyd usage, PBX Del usage</span></span></p></td>
</tr>
</tbody>
</table>

  

<span data-ttu-id="f16ec-127">Затем настройте маршрутизацию Location-Based для соответствующих сайтов сети и свяжите с ними политики маршрутизации голосовой связи.</span><span class="sxs-lookup"><span data-stu-id="f16ec-127">Next, configure Location-Based Routing for the applicable network sites and associate your voice routing policies to them.</span></span> <span data-ttu-id="f16ec-128">Используйте команду Lync Server Windows PowerShell New-CsNetworkSite, чтобы включить Location-Based маршрутизацию и сопоставить политики маршрутизации голосовой связи с сетевыми сайтами, которые должны применять ограничения маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="f16ec-128">Use the Lync Server Windows PowerShell command, New-CsNetworkSite, to enable Location-Based Routing and associate voice routing policies to your network sites that must enforce routing restrictions.</span></span>

    Set-CsNetworkSite -Identity <site ID> -EnableLocationBasedRouting <$true|$false> -VoiceRoutingPolicy <voice routing policy ID>

<span data-ttu-id="f16ec-129">В приведенной ниже таблице показано, Location-Based маршрутизацию для двух различных сайтов сети Delhi и Hyderabad, определенных в этом сценарии, с помощью Lync Server Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f16ec-129">In this example, the following table illustrates Location-Based Routing for two different network sites, Delhi and Hyderabad, defined in this scenario using the Lync Server Windows PowerShell.</span></span> <span data-ttu-id="f16ec-130">Только те параметры, которые относятся к Location-Based маршрутизации, включены в таблицу для целей иллюстрации.</span><span class="sxs-lookup"><span data-stu-id="f16ec-130">Only settings that are specific to Location-Based Routing are included in the table for illustration purposes.</span></span>

    Set-CsNetworkSite -Identity "Delhi" -EnableLocationBasedRouting $true -VoiceRoutingPolicy "DelhiVoiceRoutingPolicy"
    Set-CsNetworkSite -Identity "Hyderabad" -EnableLocationBasedRouting $true -VoiceRoutingPolicy "HyderabadVoiceRoutingPolicy"


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="f16ec-131">Сайт 1 (Delhi)</span><span class="sxs-lookup"><span data-stu-id="f16ec-131">Site 1 (Delhi)</span></span></th>
<th><span data-ttu-id="f16ec-132">Сайт 2 (Hyderabad)</span><span class="sxs-lookup"><span data-stu-id="f16ec-132">Site 2 (Hyderabad)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f16ec-133">Имя сайта</span><span class="sxs-lookup"><span data-stu-id="f16ec-133">Site Name</span></span></p></td>
<td><p><span data-ttu-id="f16ec-134">Сайт 1 (Delhi)</span><span class="sxs-lookup"><span data-stu-id="f16ec-134">Site 1 (Delhi)</span></span></p></td>
<td><p><span data-ttu-id="f16ec-135">Сайт 2 (Hyderabad)</span><span class="sxs-lookup"><span data-stu-id="f16ec-135">Site 2 (Hyderabad)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f16ec-136">EnableLocationBasedRouting</span><span class="sxs-lookup"><span data-stu-id="f16ec-136">EnableLocationBasedRouting</span></span></p></td>
<td><p><span data-ttu-id="f16ec-137">Верно</span><span class="sxs-lookup"><span data-stu-id="f16ec-137">True</span></span></p></td>
<td><p><span data-ttu-id="f16ec-138">Верно</span><span class="sxs-lookup"><span data-stu-id="f16ec-138">True</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f16ec-139">Политика маршрутизации голосовой связи</span><span class="sxs-lookup"><span data-stu-id="f16ec-139">Voice routing policy</span></span></p></td>
<td><p><span data-ttu-id="f16ec-140">Политика маршрутизации голосовой связи Delhi</span><span class="sxs-lookup"><span data-stu-id="f16ec-140">Delhi voice routing policy</span></span></p></td>
<td><p><span data-ttu-id="f16ec-141">Политика маршрутизации голосовой связи Hyderabad</span><span class="sxs-lookup"><span data-stu-id="f16ec-141">Hyderabad voice routing policy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f16ec-142">Подсети</span><span class="sxs-lookup"><span data-stu-id="f16ec-142">Subnets</span></span></p></td>
<td><p><span data-ttu-id="f16ec-143">Подсеть 1 (Delhi)</span><span class="sxs-lookup"><span data-stu-id="f16ec-143">Subnet 1 (Delhi)</span></span></p></td>
<td><p><span data-ttu-id="f16ec-144">Подсеть 2 (Hyderabad)</span><span class="sxs-lookup"><span data-stu-id="f16ec-144">Subnet 2 (Hyderabad)</span></span></p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="enable-location-based-routing-to-trunks"></a><span data-ttu-id="f16ec-145">Включение маршрутизации Location-Based в магистральные магистрали</span><span class="sxs-lookup"><span data-stu-id="f16ec-145">Enable Location-Based Routing to Trunks</span></span>

<span data-ttu-id="f16ec-146">Прежде чем можно будет включить конфигурацию магистрали для маршрутизации Location-Based, необходимо создать конфигурацию магистрали для каждой магистрали или каждого из сайтов сети.</span><span class="sxs-lookup"><span data-stu-id="f16ec-146">Before a trunk configuration can be enabled for Location-Based Routing, you need to create a trunk configuration for each trunk or each network site.</span></span> <span data-ttu-id="f16ec-147">Используйте команду Lync Server Windows PowerShell New-CsTrunkConfiguration для создания конфигурации канала магистрали.</span><span class="sxs-lookup"><span data-stu-id="f16ec-147">Use the Lync Server Windows PowerShell command, New-CsTrunkConfiguration, to create a trunk configuration.</span></span> <span data-ttu-id="f16ec-148">Если несколько магистральных каналов связаны с определенной системой (например, Gateway или УАТС), каждую из них нужно изменить, чтобы включить Location-Based ограничения маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="f16ec-148">If multiple trunks are associated with a given system (i.e. Gateway or PBX), each trunk configuration must be modified to enable Location-Based Routing restrictions.</span></span>

    New-CsTrunkConfiguration -Identity < trunk configuration ID>

<span data-ttu-id="f16ec-149">Дополнительные сведения можно найти в разделе [New-CsTrunkConfiguration](https://docs.microsoft.com/powershell/module/skype/New-CsTrunkConfiguration).</span><span class="sxs-lookup"><span data-stu-id="f16ec-149">For more information, see [New-CsTrunkConfiguration](https://docs.microsoft.com/powershell/module/skype/New-CsTrunkConfiguration).</span></span>

<span data-ttu-id="f16ec-150">В этом примере следующие команды Windows PowerShell иллюстрируют создание одной конфигурации магистрали для каждой магистрали в развертывании, определенном в этом сценарии.</span><span class="sxs-lookup"><span data-stu-id="f16ec-150">For this example, the following Windows PowerShell commands illustrate creating one trunk configuration for each trunk in the deployment defined in this scenario.</span></span>

    New-CsTrunkConfiguration -Identity Service:PstnGateway:"<Trunk 1 DEL-GW>"
    New-CsTrunkConfiguration -Identity Service:PstnGateway:"<Trunk 2 HYD-GW>"
    New-CsTrunkConfiguration -Identity Service:PstnGateway:"<Trunk 3 DEL-PBX>"
    New-CsTrunkConfiguration -Identity Service:PstnGateway:"<Trunk 4 HYD-PBX>"

<span data-ttu-id="f16ec-151">После настройки магистральной конфигурации для каждой магистрали вы можете использовать команду Lync Server Windows PowerShell Set-CsTrunkConfiguration, чтобы включить Location-Based маршрутизацию на магистральные системы, которые должны применять ограничения маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="f16ec-151">Once a trunk configuration is configured per trunk, you can use the Lync Server Windows PowerShell command, Set-CsTrunkConfiguration, to enable Location-Based Routing to your trunks that must enforce routing restrictions.</span></span> <span data-ttu-id="f16ec-152">Включите Location-Based маршрутизацию на магистральы, которые направляют звонки на шлюзы PSTN, которые перенаправляют звонки в КТСОП и связывают сетевой сайт, на котором расположен шлюз.</span><span class="sxs-lookup"><span data-stu-id="f16ec-152">Enable Location-Based Routing to trunks that route calls to PSTN gateways that route calls to the PSTN, and associate the network site where the gateway is located.</span></span>

    Set-CsTrunkConfiguration -Identity <trunk configuration ID> -EnableLocationRestriction $true -NetworkSiteID <site ID>

<span data-ttu-id="f16ec-153">Дополнительные сведения можно найти в разделе [New-CsTrunkConfiguration](https://docs.microsoft.com/powershell/module/skype/New-CsTrunkConfiguration).</span><span class="sxs-lookup"><span data-stu-id="f16ec-153">For more information, see [New-CsTrunkConfiguration](https://docs.microsoft.com/powershell/module/skype/New-CsTrunkConfiguration).</span></span>

<span data-ttu-id="f16ec-154">В этом примере Location-Based маршрутизация включена для каждой магистрали, связанной с шлюзами PSTN в Delhi и Hyderabad:</span><span class="sxs-lookup"><span data-stu-id="f16ec-154">In this example, Location-Based Routing is enabled for each trunk that is associated to PSTN gateways in Delhi and Hyderabad:</span></span>

    Set-CsTrunkConfiguration -Identity Service:PstnGateway:Trunk 1 DEL-GW -EnableLocationRestriction $true -NetworkSiteID "Delhi"
    Set-CsTrunkConfiguration -Identity Service:PstnGateway:Trunk 2 HYD-GW -EnableLocationRestriction $true -NetworkSiteID "Hyderabad"

  

<span data-ttu-id="f16ec-155">Не включайте Location-Based маршрутизацию для каналов, которые не направляют звонки в КТСОП. Однако вы по-прежнему обязаны привязать магистраль к сетевому сайту, на котором находится система, так как Location-Based ограничения маршрутизации, которые необходимо применять для звонков по протоколу PSTN, подключенных к конечным точкам с помощью этой магистрали.</span><span class="sxs-lookup"><span data-stu-id="f16ec-155">Do not enable Location-Based Routing for trunks that do not route calls to the PSTN; however, you must still associate the trunk to the network site where the system is located as Location-Based Routing restrictions need to be enforced for PSTN calls reaching endpoints connected via this trunk.</span></span> <span data-ttu-id="f16ec-156">В этом примере Location-Based маршрутизация не включена для каждой магистрали, связанной с системами УАТС в Delhi и Hyderabad:</span><span class="sxs-lookup"><span data-stu-id="f16ec-156">For this example, Location-Based Routing is not enabled for each trunk that is associated to PBX systems in Delhi and Hyderabad:</span></span>

    Set-CsTrunkConfiguration -Identity Service:PstnGateway:Trunk 3 DEL-PBX -EnableLocationRestriction $false -NetworkSiteID "Delhi"
    Set-CsTrunkConfiguration -Identity Service:PstnGateway:Trunk 4 HYD-PBX -EnableLocationRestriction $false -NetworkSiteID "Hyderabad"

  
<span data-ttu-id="f16ec-157">Конечные точки, которые подключены к системам, не накладываемым на протокол PSTN (например, УАТС), имеют аналогичные ограничения в качестве конечных точек Lync для пользователей, которые включены для Location-Based маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="f16ec-157">Endpoints that are connected to systems that do not route calls to the PSTN (i.e. a PBX) will have similar restrictions as Lync endpoints of users enabled for Location-Based Routing.</span></span> <span data-ttu-id="f16ec-158">Это означает, что эти пользователи смогут размещать и принимать звонки на пользователей Lync, независимо от местонахождения пользователя.</span><span class="sxs-lookup"><span data-stu-id="f16ec-158">This means that these users will be able to place and receive calls to and from Lync user regardless of the user’s location.</span></span> <span data-ttu-id="f16ec-159">Кроме того, они смогут принимать звонки в другие системы и из них, которые не направляют звонки в сеть PSTN (например, конечную точку, подключенную к другой УАТС) независимо от того, с какой сетевой страницы связана система.</span><span class="sxs-lookup"><span data-stu-id="f16ec-159">They will also be able to place an receive calls to and from other systems that do not route calls to the PSTN network (i.e. an endpoint connected to a different PBX) regardless of the network site to which the system is associated.</span></span> <span data-ttu-id="f16ec-160">Все входящие звонки, звонки, передача звонков и переадресация звонков с использованием конечных точек PSTN будут Location-Based принудительной маршрутизацией.</span><span class="sxs-lookup"><span data-stu-id="f16ec-160">All inbound calls, outbound calls, call transfers and call forwarding involving PSTN endpoints will be subject to Location-Based Routing enforcements.</span></span> <span data-ttu-id="f16ec-161">Такие звонки должны использовать только шлюзы PSTN, определенные как локальные для таких систем.</span><span class="sxs-lookup"><span data-stu-id="f16ec-161">Such calls must use only PSTN gateways that are defined as local to such systems.</span></span>

<span data-ttu-id="f16ec-162">В приведенной ниже таблице показана конфигурация магистрали с четырьмя магистральами на двух разных сетевых сайтах: два соединения с шлюзами PSTN и двумя подключенными к системам АТС.</span><span class="sxs-lookup"><span data-stu-id="f16ec-162">The following table illustrates the trunk configuration of four trunks in two different network sites: two connected to PSTN gateways and two connected to PBX systems.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f16ec-163">Имя</span><span class="sxs-lookup"><span data-stu-id="f16ec-163">Name</span></span></th>
<th><span data-ttu-id="f16ec-164">EnableLocationRestriction</span><span class="sxs-lookup"><span data-stu-id="f16ec-164">EnableLocationRestriction</span></span></th>
<th><span data-ttu-id="f16ec-165">NetworkSiteID</span><span class="sxs-lookup"><span data-stu-id="f16ec-165">NetworkSiteID</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f16ec-166">PstnGateway: магистраль 1 DEL-GW</span><span class="sxs-lookup"><span data-stu-id="f16ec-166">PstnGateway:Trunk 1 DEL-GW</span></span></p></td>
<td><p><span data-ttu-id="f16ec-167">Верно</span><span class="sxs-lookup"><span data-stu-id="f16ec-167">True</span></span></p></td>
<td><p><span data-ttu-id="f16ec-168">Сайт 1 (Delhi)</span><span class="sxs-lookup"><span data-stu-id="f16ec-168">Site 1 (Delhi)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f16ec-169">PstnGateway: магистраль 2 HYD-GW</span><span class="sxs-lookup"><span data-stu-id="f16ec-169">PstnGateway:Trunk 2 HYD-GW</span></span></p></td>
<td><p><span data-ttu-id="f16ec-170">Верно</span><span class="sxs-lookup"><span data-stu-id="f16ec-170">True</span></span></p></td>
<td><p><span data-ttu-id="f16ec-171">Сайт 2 (Hyderabad)</span><span class="sxs-lookup"><span data-stu-id="f16ec-171">Site 2 (Hyderabad)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f16ec-172">PstnGateway: магистраль 3 DEL-УАТС</span><span class="sxs-lookup"><span data-stu-id="f16ec-172">PstnGateway:Trunk 3 DEL-PBX</span></span></p></td>
<td><p><span data-ttu-id="f16ec-173">False</span><span class="sxs-lookup"><span data-stu-id="f16ec-173">False</span></span></p></td>
<td><p><span data-ttu-id="f16ec-174">Сайт 1 (Delhi)</span><span class="sxs-lookup"><span data-stu-id="f16ec-174">Site 1 (Delhi)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f16ec-175">PstnGateway: HYD-УАТС (магистральная линия 4)</span><span class="sxs-lookup"><span data-stu-id="f16ec-175">PstnGateway:Trunk 4 HYD-PBX</span></span></p></td>
<td><p><span data-ttu-id="f16ec-176">False</span><span class="sxs-lookup"><span data-stu-id="f16ec-176">False</span></span></p></td>
<td><p><span data-ttu-id="f16ec-177">Сайт 2 (Hyderabad)</span><span class="sxs-lookup"><span data-stu-id="f16ec-177">Site 2 (Hyderabad)</span></span></p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="enable-location-based-routing-to-voice-policies"></a><span data-ttu-id="f16ec-178">Включение Location-Based маршрутизации к политикам голосовой связи</span><span class="sxs-lookup"><span data-stu-id="f16ec-178">Enable Location-Based Routing to Voice Policies</span></span>

<span data-ttu-id="f16ec-179">Чтобы включить Location-Based маршрутизацию для определенных пользователей, настройте политику голосовой связи пользователей, чтобы отключить бесплатный звонок.</span><span class="sxs-lookup"><span data-stu-id="f16ec-179">To enforce Location-Based Routing to specific users, configure those users’ voice policy to prevent PSTN toll bypass.</span></span> <span data-ttu-id="f16ec-180">Используйте команду Lync Server Windows PowerShell New-CsVoicePolicy, чтобы создать новую политику голосовой связи или Set-CsVoicePolicy, при использовании существующей политики для включения Location-Based маршрутизации, запретив бесплатный звонок по протоколу КТСОП.</span><span class="sxs-lookup"><span data-stu-id="f16ec-180">Use the Lync Server Windows PowerShell command, New-CsVoicePolicy, to create a new voice policy or Set-CsVoicePolicy, if using an existing policy, to enable Location-Based Routing by preventing PSTN toll bypass.</span></span>

    Set-CsVoicePolicy -Identity <voice policy ID> -PreventPSTNTollBypass <$true|$false>

<span data-ttu-id="f16ec-181">Дополнительные сведения можно найти в разделе [New-CsVoicePolicy](https://docs.microsoft.com/powershell/module/skype/New-CsVoicePolicy).</span><span class="sxs-lookup"><span data-stu-id="f16ec-181">For more information, see [New-CsVoicePolicy](https://docs.microsoft.com/powershell/module/skype/New-CsVoicePolicy).</span></span>

<span data-ttu-id="f16ec-182">В этом примере приведенная ниже таблица и команды Windows PowerShell иллюстрируют использование политик голосовой связи по Delhi и Hyderabad, описанных в этом сценарии, в целях предотвращения бесплатной поддержки PSTN.</span><span class="sxs-lookup"><span data-stu-id="f16ec-182">For this example, the following table and Windows PowerShell commands illustrate enabling the prevention of PSTN toll bypass to the Delhi and Hyderabad voice policies defined in this scenario.</span></span> <span data-ttu-id="f16ec-183">Только те параметры, которые относятся к Location-Based маршрутизации, включены в таблицу для целей иллюстрации.</span><span class="sxs-lookup"><span data-stu-id="f16ec-183">Only settings that are specific to Location-Based Routing are included in the table for illustration purposes.</span></span>

    Set-CsVoicePolicy -Identity "Delhi voice policy" -PreventPSTNTollBypass $true
    Set-CsVoicePolicy -Identity "Hyderabad voice policy" -PreventPSTNTollBypass $true


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="f16ec-184">Политика голосовой связи 1</span><span class="sxs-lookup"><span data-stu-id="f16ec-184">Voice policy 1</span></span></th>
<th><span data-ttu-id="f16ec-185">Политика голосовой связи 2</span><span class="sxs-lookup"><span data-stu-id="f16ec-185">Voice policy 2</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f16ec-186">Идентификатор политики голосовой связи</span><span class="sxs-lookup"><span data-stu-id="f16ec-186">Voice policy ID</span></span></p></td>
<td><p><span data-ttu-id="f16ec-187">Политика голосовой связи Delhi</span><span class="sxs-lookup"><span data-stu-id="f16ec-187">Delhi voice policy</span></span></p></td>
<td><p><span data-ttu-id="f16ec-188">Политика голосовой связи Hyderabad</span><span class="sxs-lookup"><span data-stu-id="f16ec-188">Hyderabad voice policy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f16ec-189">Использование PSTN</span><span class="sxs-lookup"><span data-stu-id="f16ec-189">PSTN usages</span></span></p></td>
<td><p><span data-ttu-id="f16ec-190">Использование Delhi, использование АТС DELETE, использование Hyd УАТС</span><span class="sxs-lookup"><span data-stu-id="f16ec-190">Delhi usage, PBX Del usage, PBX Hyd usage</span></span></p></td>
<td><p><span data-ttu-id="f16ec-191">Использование Hyderabad, Hyd УАТС, использование АТС Delete</span><span class="sxs-lookup"><span data-stu-id="f16ec-191">Hyderabad usage, PBX Hyd usage, PBX Del usage</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f16ec-192">PreventPSTNTollBypass</span><span class="sxs-lookup"><span data-stu-id="f16ec-192">PreventPSTNTollBypass</span></span></p></td>
<td><p><span data-ttu-id="f16ec-193">Верно</span><span class="sxs-lookup"><span data-stu-id="f16ec-193">True</span></span></p></td>
<td><p><span data-ttu-id="f16ec-194">Верно</span><span class="sxs-lookup"><span data-stu-id="f16ec-194">True</span></span></p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="enable-location-based-routing-in-the-routing-configuration"></a><span data-ttu-id="f16ec-195">Включение маршрутизации Location-Based в конфигурации маршрутизации</span><span class="sxs-lookup"><span data-stu-id="f16ec-195">Enable Location-Based Routing in the routing configuration</span></span>

<span data-ttu-id="f16ec-196">Наконец, разрешите Location-Based маршрутизацию в конфигурацию маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="f16ec-196">Finally, globally enable Location-Based Routing to your routing configuration.</span></span> <span data-ttu-id="f16ec-197">Используйте команду Lync Server Windows PowerShell New-CsRoutingConfiguration, чтобы включить маршрутизацию Location-Based.</span><span class="sxs-lookup"><span data-stu-id="f16ec-197">Use the Lync Server Windows PowerShell command, New-CsRoutingConfiguration, to enable Location-Based Routing.</span></span>

    Set-CsRoutingConfiguration -EnableLocationBasedRouting $true

<span data-ttu-id="f16ec-198">Дополнительные сведения можно найти в разделе [Set-CsRoutingConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsRoutingConfiguration).</span><span class="sxs-lookup"><span data-stu-id="f16ec-198">For more information, see [Set-CsRoutingConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsRoutingConfiguration).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="f16ec-199">Несмотря на то, что в глобальной конфигурации должна быть включена Location-Based маршрутизация, набор применяемых правил будет применяться только для сайтов, пользователей и магистральов, для которых она настроена, как указано в этой документации.</span><span class="sxs-lookup"><span data-stu-id="f16ec-199">while Location-Based Routing must be enabled via a global configuration, the set of rules to be applied will only be enforced for the sites, users and trunks for which it has been configured as specified in this documentation.</span></span>



</div>

<div>


</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="f16ec-200">См. также</span><span class="sxs-lookup"><span data-stu-id="f16ec-200">See Also</span></span>


[<span data-ttu-id="f16ec-201">Настройка маршрутизации на основе расположения в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f16ec-201">Configuring Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-configuring-location-based-routing.md)  
  

<span data-ttu-id="f16ec-202"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f16ec-202"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

