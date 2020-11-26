---
title: Пример сбора требований к контролю за допуском звонков
description: Пример сбора требований к контролю за допуском звонков.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Example of gathering your requirements for call admission control
ms:assetid: 3363ac53-b7c4-4a59-aea1-b2f3ee016ae1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425827(v=OCS.15)
ms:contentKeyID: 48183820
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 25c0b450070bda62c2610d98cfff8c8cd16ad2af
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428500"
---
# <a name="example-gathering-your-requirements-for-call-admission-control-in-lync-server-2013"></a><span data-ttu-id="89d85-103">Пример: сбор требований к управлению допуском звонков в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="89d85-103">Example: Gathering your requirements for call admission control in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="89d85-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="89d85-104">

<span> </span></span></span>

<span data-ttu-id="89d85-105">_**Тема последнего изменения:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="89d85-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="89d85-p101">В этом примере показано, как спланировать и реализовать контроль допуска звонков (CAC). На высоком уровне этот процесс включает в себя следующие действия.</span><span class="sxs-lookup"><span data-stu-id="89d85-p101">This example shows you how to plan for and implement call admission control (CAC). At a high level, this consists of the following activities:</span></span>

1.  <span data-ttu-id="89d85-108">Распознавание всех сетевых концентраторов и магистралей (называемых *областями сети*).</span><span class="sxs-lookup"><span data-stu-id="89d85-108">Identify all of your network hubs and backbones (known as *network regions*).</span></span>

2.  <span data-ttu-id="89d85-109">Определите центральный сайт Lync Server, который будет управлять CAC для каждого сетевого региона.</span><span class="sxs-lookup"><span data-stu-id="89d85-109">Identify the Lync Server central site that will manage CAC for each network region.</span></span>

3.  <span data-ttu-id="89d85-110">Распознавание и задание *сетевых сайтов*, подключенных к каждой области сети.</span><span class="sxs-lookup"><span data-stu-id="89d85-110">Identify and define the *network sites* that are connected to each network region.</span></span>

4.  <span data-ttu-id="89d85-111">Для каждого сетевого сайта, подключенного к глобальной сети, необходимо указать пропускную способность подключения к глобальной сети и ограничения пропускной способности, настроенные для сетевого трафика Lync Server, если это применимо.</span><span class="sxs-lookup"><span data-stu-id="89d85-111">For each network site whose connection to the WAN is bandwidth-constrained, describe the bandwidth capacity of the WAN connection and the bandwidth limits that to the network administrator has set for Lync Server media traffic, if applicable.</span></span> <span data-ttu-id="89d85-112">Вам не требуется включать сайты, для которых подключения к глобальной сети не ограничены по пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="89d85-112">You do not need to include sites whose connection to the WAN is not bandwidth-constrained.</span></span>

5.  <span data-ttu-id="89d85-113">Свяжите каждую подсеть в сети с сетевым сайтом.</span><span class="sxs-lookup"><span data-stu-id="89d85-113">Associate each subnet in your network with a network site.</span></span>

6.  <span data-ttu-id="89d85-114">Сопоставьте каналы между областями сети.</span><span class="sxs-lookup"><span data-stu-id="89d85-114">Map the links between the network regions.</span></span> <span data-ttu-id="89d85-115">Для каждой ссылки Опишите ее пропускную способность и любые ограничения, помещаемые администратором сети на трафик мультимедиа Lync Server.</span><span class="sxs-lookup"><span data-stu-id="89d85-115">For each link, describe its bandwidth capacity and any limits that the network administrator has placed on Lync Server media traffic.</span></span>

7.  <span data-ttu-id="89d85-116">Определите маршрут между каждой парой областей сети.</span><span class="sxs-lookup"><span data-stu-id="89d85-116">Define a route between every pair of network regions.</span></span>

<div>

## <a name="gather-the-required-information"></a><span data-ttu-id="89d85-117">Сбор необходимой информации</span><span class="sxs-lookup"><span data-stu-id="89d85-117">Gather the Required Information</span></span>

<span data-ttu-id="89d85-118">Чтобы подготовиться к реализации контроля допуска вызовов, соберите информацию, описанную далее.</span><span class="sxs-lookup"><span data-stu-id="89d85-118">To prepare for call admission control, gather the information described in the following steps:</span></span>

1.  <span data-ttu-id="89d85-p104">Определите области сети, которые представляют сетевую магистраль или сетевой концентратор.</span><span class="sxs-lookup"><span data-stu-id="89d85-p104">Identify your network regions. A network region represents a network backbone or a network hub.</span></span>
    
    <span data-ttu-id="89d85-p105">Магистраль или концентратор сети является частью инфраструктуры компьютерной сети, которая соединяет различные части сети, предоставляя путь для обмена информацией между различными локальными сетями или подсетями. Магистраль может объединять различные сети: от небольших локальных сетей до крупномасштабных сетей. Мощность магистрали обычно больше, чем у сетей, подключенных к ней.</span><span class="sxs-lookup"><span data-stu-id="89d85-p105">A network backbone or a network hub is a part of computer network infrastructure that interconnects various pieces of network, providing a path for the exchange of information between different LANs or subnets. A backbone can tie together diverse networks, from a small location to a wide geographic area. The backbone's capacity is typically greater than that of the networks connected to it.</span></span>
    
    <span data-ttu-id="89d85-p106">Пример топологии сети содержит три области: Северная Америка, EMEA (Европа, Ближний Восток и Африка) и APAC (Азиатско-Тихоокеанский регион). Область сети содержит коллекцию сетевых сайтов. Определите области сети вашего предприятия вместе с сетевым администратором.</span><span class="sxs-lookup"><span data-stu-id="89d85-p106">Our example topology has three network regions: North America, EMEA, and APAC. A network region contains a collection of network sites. Work with your network administrator to define the network regions for your enterprise.</span></span>

2.  <span data-ttu-id="89d85-127">Определите центральный сайт каждой области сети.</span><span class="sxs-lookup"><span data-stu-id="89d85-127">Identify each network region’s associated central site.</span></span> <span data-ttu-id="89d85-128">Центральный сайт содержит по крайней мере один сервер переднего плана и является развертыванием Lync Server, которое управляет CAC для всего трафика мультимедиа, который проходит через подключение к глобальной сети в сетевом регионе.</span><span class="sxs-lookup"><span data-stu-id="89d85-128">A central site contains at least one Front End Server and is the Lync Server deployment that will manage CAC for all media traffic that passes through the network region’s WAN connection.</span></span>
    
    <span data-ttu-id="89d85-129">**Пример корпоративной сети, разделенной на три области**</span><span class="sxs-lookup"><span data-stu-id="89d85-129">**An example enterprise network divided into three network regions**</span></span>
    
    <span data-ttu-id="89d85-130">![Пример топологии сети с 3 областями](images/Gg425827.08937347-250f-488f-ba5f-c256e6afcd8b(OCS.15).jpg "Пример топологии сети с 3 областями")</span><span class="sxs-lookup"><span data-stu-id="89d85-130">![Network Topology Example with 3 Network Regions](images/Gg425827.08937347-250f-488f-ba5f-c256e6afcd8b(OCS.15).jpg "Network Topology Example with 3 Network Regions")</span></span>  
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="89d85-131">Сеть MPLS следует представить как область сети, в которой каждому географическому расположению соответствует определенный сетевой сайт.</span><span class="sxs-lookup"><span data-stu-id="89d85-131">A Multiprotocol Label Switching (MPLS) network should be represented as a network region in which each geographic location has a corresponding network site.</span></span> <span data-ttu-id="89d85-132">Дополнительные сведения можно найти в разделе "<A href="lync-server-2013-call-admission-control-on-an-mpls-network.md">Управление допуском звонков в сети MPLS с помощью Lync Server 2013</A>" в документации по планированию.</span><span class="sxs-lookup"><span data-stu-id="89d85-132">For details, see the “<A href="lync-server-2013-call-admission-control-on-an-mpls-network.md">Call admission control on an MPLS network with Lync Server 2013</A>” topic in the Planning documentation.</span></span>

    
    </div>
    
    <span data-ttu-id="89d85-133">В приведенном выше примере топологии сети есть три сетевых региона, каждый из которых содержит центральный сайт Lync Server, управляющий CAC.</span><span class="sxs-lookup"><span data-stu-id="89d85-133">In the preceding example network topology, there are three network regions, each with a Lync Server central site that manages CAC.</span></span> <span data-ttu-id="89d85-134">Соответствующий центральный сайт для области сети выбирается на основе географической близости.</span><span class="sxs-lookup"><span data-stu-id="89d85-134">The appropriate central site for a network region is chosen by the geographic vicinity.</span></span> <span data-ttu-id="89d85-135">Так как трафик мультимедиа будет наиболее объемным в областях сети, определение владельца на основе близости позволяет сделать центральный сайт автономным и продолжать работу, даже если другие центральные сайты станут недоступными.</span><span class="sxs-lookup"><span data-stu-id="89d85-135">Because media traffic will be heaviest within network regions, the ownership by geographic vicinity makes it self-contained and will continue to be functional even if other central sites become unavailable.</span></span>
    
    <span data-ttu-id="89d85-136">В этом примере развертывание Lync Server с именем Чикаго — это центральный сайт для региона Северной Америки.</span><span class="sxs-lookup"><span data-stu-id="89d85-136">In this example, a Lync Server deployment named Chicago is the central site for the North America region.</span></span>
    
    <span data-ttu-id="89d85-137">Все пользователи Lync в Северной Америке размещаются на серверах в среде развертывания в Чикаго.</span><span class="sxs-lookup"><span data-stu-id="89d85-137">All Lync users in North America are homed on servers in the Chicago deployment.</span></span> <span data-ttu-id="89d85-138">В следующей таблице показаны центральные сайты для всех трех областей.</span><span class="sxs-lookup"><span data-stu-id="89d85-138">The following table shows central sites for all three network regions.</span></span>
    
    ### <a name="network-regions-and-their-associated-central-sites"></a><span data-ttu-id="89d85-139">Области сети и связанные с ними центральные сайты</span><span class="sxs-lookup"><span data-stu-id="89d85-139">Network Regions and their Associated Central Sites</span></span>
    
    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="89d85-140">Сетевой регион</span><span class="sxs-lookup"><span data-stu-id="89d85-140">Network Region</span></span></th>
    <th><span data-ttu-id="89d85-141">Центральный сайт</span><span class="sxs-lookup"><span data-stu-id="89d85-141">Central Site</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="89d85-142">Северная Америка</span><span class="sxs-lookup"><span data-stu-id="89d85-142">North America</span></span></p></td>
    <td><p><span data-ttu-id="89d85-143">Чикаго</span><span class="sxs-lookup"><span data-stu-id="89d85-143">Chicago</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="89d85-144">Европа, Ближний Восток и Африка</span><span class="sxs-lookup"><span data-stu-id="89d85-144">EMEA</span></span></p></td>
    <td><p><span data-ttu-id="89d85-145">Лондон</span><span class="sxs-lookup"><span data-stu-id="89d85-145">London</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="89d85-146">Азиатско-Тихоокеанский регион</span><span class="sxs-lookup"><span data-stu-id="89d85-146">APAC</span></span></p></td>
    <td><p><span data-ttu-id="89d85-147">Пекин</span><span class="sxs-lookup"><span data-stu-id="89d85-147">Beijing</span></span></p></td>
    </tr>
    </tbody>
    </table>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="89d85-148">В зависимости от топологии Lync Server один и тот же центральный сайт может быть назначен нескольким сетевым регионам.</span><span class="sxs-lookup"><span data-stu-id="89d85-148">Depending on your Lync Server topology, the same central site can be assigned to multiple network regions.</span></span>

    
    </div>

3.  <span data-ttu-id="89d85-p111">Для каждой области сети определите все сетевые сайты (офисы или расположения), для которых подключения к глобальной сети не ограничены по пропускной способности. Так как ограничений нет, к ним не требуется применять политики пропускной способности CAC.</span><span class="sxs-lookup"><span data-stu-id="89d85-p111">For each network region, identify all of the network sites (offices or locations) whose WAN connections are not bandwidth-constrained. Because these sites are not bandwidth constrained, you do not need to apply CAC bandwidth policies to them.</span></span>
    
    <span data-ttu-id="89d85-151">В примере в следующей таблице у сетевых сайтов нет каналов глобальной сети с ограниченной пропускной способностью: Нью-Йорк, Чикаго и Детройт.</span><span class="sxs-lookup"><span data-stu-id="89d85-151">In the example shown in the following table, three network sites do not have bandwidth-constrained WAN links: New York, Chicago, and Detroit.</span></span>
    
    ### <a name="network-sites-not-constrained-by-wan-bandwidth"></a><span data-ttu-id="89d85-152">Сетевые сайты без ограничений по пропускной способности глобальной сети</span><span class="sxs-lookup"><span data-stu-id="89d85-152">Network Sites not Constrained by WAN Bandwidth</span></span>
    
    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="89d85-153">Сетевой сайт</span><span class="sxs-lookup"><span data-stu-id="89d85-153">Network Site</span></span></th>
    <th><span data-ttu-id="89d85-154">Сетевой регион</span><span class="sxs-lookup"><span data-stu-id="89d85-154">Network Region</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="89d85-155">Нью-Йорк</span><span class="sxs-lookup"><span data-stu-id="89d85-155">New York</span></span></p></td>
    <td><p><span data-ttu-id="89d85-156">Северная Америка</span><span class="sxs-lookup"><span data-stu-id="89d85-156">North America</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="89d85-157">Чикаго</span><span class="sxs-lookup"><span data-stu-id="89d85-157">Chicago</span></span></p></td>
    <td><p><span data-ttu-id="89d85-158">Северная Америка</span><span class="sxs-lookup"><span data-stu-id="89d85-158">North America</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="89d85-159">Детройт</span><span class="sxs-lookup"><span data-stu-id="89d85-159">Detroit</span></span></p></td>
    <td><p><span data-ttu-id="89d85-160">Северная Америка</span><span class="sxs-lookup"><span data-stu-id="89d85-160">North America</span></span></p></td>
    </tr>
    </tbody>
    </table>


4.  <span data-ttu-id="89d85-161">Для каждой области сети определите все сетевые сайты, подключающиеся к области по каналам глобальной сети с ограниченной пропускной способностью.</span><span class="sxs-lookup"><span data-stu-id="89d85-161">For each network region, identify all of the network sites that connect to the network region through bandwidth-constrained WAN links.</span></span>
    
    <span data-ttu-id="89d85-162">Чтобы помочь обеспечить высокое качество звука и видео, рекомендуется на этих сайтах с ограниченной пропускной способностью отслеживать глобальные сети и использовать политики пропускной способности CAC, которые ограничивают трафик мультимедиа (голосовой или видео) для данной области сети.</span><span class="sxs-lookup"><span data-stu-id="89d85-162">To help ensure audio and video quality, we recommend that these bandwidth-constrained network sites have their WANs monitored and CAC bandwidth policies that limit media (voice or video) traffic flow to and from the network region.</span></span>
    
    <span data-ttu-id="89d85-163">В примере из следующей таблицы показаны три сетевых сайта с ограниченной пропускной способностью глобальной сети: Портленд, Рино и и Альбукерке.</span><span class="sxs-lookup"><span data-stu-id="89d85-163">In the example shown in the following table, there are three network sites that are constrained by WAN bandwidth: Portland, Reno and Albuquerque.</span></span>
    
    ### <a name="network-sites-constrained-by-wan-bandwidth"></a><span data-ttu-id="89d85-164">Сетевые сайты с ограниченной пропускной способностью глобальной сети</span><span class="sxs-lookup"><span data-stu-id="89d85-164">Network Sites Constrained by WAN Bandwidth</span></span>
    
    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="89d85-165">Сетевой сайт</span><span class="sxs-lookup"><span data-stu-id="89d85-165">Network Site</span></span></th>
    <th><span data-ttu-id="89d85-166">Сетевой регион</span><span class="sxs-lookup"><span data-stu-id="89d85-166">Network Region</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="89d85-167">Альбукерке</span><span class="sxs-lookup"><span data-stu-id="89d85-167">Albuquerque</span></span></p></td>
    <td><p><span data-ttu-id="89d85-168">Северная Америка</span><span class="sxs-lookup"><span data-stu-id="89d85-168">North America</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="89d85-169">Рено</span><span class="sxs-lookup"><span data-stu-id="89d85-169">Reno</span></span></p></td>
    <td><p><span data-ttu-id="89d85-170">Северная Америка</span><span class="sxs-lookup"><span data-stu-id="89d85-170">North America</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="89d85-171">Портленд</span><span class="sxs-lookup"><span data-stu-id="89d85-171">Portland</span></span></p></td>
    <td><p><span data-ttu-id="89d85-172">Северная Америка</span><span class="sxs-lookup"><span data-stu-id="89d85-172">North America</span></span></p></td>
    </tr>
    </tbody>
    </table>
    
    <span data-ttu-id="89d85-173">**Область сети CAC Северная Америка с тремя сетевыми узлами без ограничений по пропускной способности (Чикаго, Нью-Йорк и Детройт) и тремя сетевыми узлами с ограниченной пропускной способностью глобальной сети (Портленд, Рино и Альбукерке)**</span><span class="sxs-lookup"><span data-stu-id="89d85-173">**CAC network region North America with three network sites that are unconstrained by bandwidth (Chicago, New York, and Detroit) and three network sites that are constrained by WAN bandwidth (Portland, Reno, and Albuquerque)**</span></span>
    
    <span data-ttu-id="89d85-174">![Пример сетевых узлов, ограниченных пропускной способностью глобальной сети](images/Gg425827.d9d1f231-db4d-4dd7-8fbc-eb0b6d1e705d(OCS.15).jpg "Пример сетевых узлов, ограниченных пропускной способностью глобальной сети")</span><span class="sxs-lookup"><span data-stu-id="89d85-174">![Example network sites constrained by WAN bandwidth](images/Gg425827.d9d1f231-db4d-4dd7-8fbc-eb0b6d1e705d(OCS.15).jpg "Example network sites constrained by WAN bandwidth")</span></span>  

5.  <span data-ttu-id="89d85-175">Для каждого канала глобальной сети с ограниченной пропускной способностью определите следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="89d85-175">For each bandwidth-constrained WAN link, determine the following:</span></span>
    
      - <span data-ttu-id="89d85-176">Общее ограничение пропускной способности, которое необходимо задать для всех параллельных аудиосеансов.</span><span class="sxs-lookup"><span data-stu-id="89d85-176">Overall bandwidth limit that you want to set for all concurrent audio sessions.</span></span> <span data-ttu-id="89d85-177">Если это ограничение будет превышено, приложение Lync Server не разрешается запускать сеанс.</span><span class="sxs-lookup"><span data-stu-id="89d85-177">If a new audio session will cause this limit to be exceeded, Lync Server does not allow the session to start.</span></span>
    
      - <span data-ttu-id="89d85-p113">Ограничение пропускной способности, которое необходимо задать для каждого отдельного аудиосеанса. По умолчанию это ограничение CAC равно 175 кбит/с, но его может изменить администратор.</span><span class="sxs-lookup"><span data-stu-id="89d85-p113">Bandwidth limit that you want to set for each individual audio session. The default CAC bandwidth limit is 175 kbps, but it can be modified by the administrator.</span></span>
    
      - <span data-ttu-id="89d85-180">Общее ограничение пропускной способности, которое необходимо задать для всех параллельных видеосеансов.</span><span class="sxs-lookup"><span data-stu-id="89d85-180">Overall bandwidth limit that you want to set for all concurrent video sessions.</span></span> <span data-ttu-id="89d85-181">Если в новом видеосеансе это ограничение будет превышено, Lync Server не разрешает запуск сеанса.</span><span class="sxs-lookup"><span data-stu-id="89d85-181">If a new video session will cause this limit to be exceeded, Lync Server does not allow the session to start.</span></span>
    
      - <span data-ttu-id="89d85-p115">Ограничение пропускной способности, которое необходимо задать для каждого отдельного видеосеанса. По умолчанию это ограничение CAC равно 700 кбит/с, но его может изменить администратор.</span><span class="sxs-lookup"><span data-stu-id="89d85-p115">Bandwidth limit that you want to set for each individual video session. The default CAC bandwidth limit is 700 kbps, but it can be modified by the administrator.</span></span>
    
    ### <a name="network-sites-with-wan-bandwidth-constraint-information-bandwidth-in-kbps"></a><span data-ttu-id="89d85-184">Сведения о сетевых сайтах с ограниченной пропускной способностью глобальной сети (пропускная способность в кбит/с)</span><span class="sxs-lookup"><span data-stu-id="89d85-184">Network Sites with WAN Bandwidth Constraint Information (Bandwidth in kbps)</span></span>
    
    <table style="width:100%;">
    <colgroup>
    <col style="width: 14%" />
    <col style="width: 14%" />
    <col style="width: 14%" />
    <col style="width: 14%" />
    <col style="width: 14%" />
    <col style="width: 14%" />
    <col style="width: 14%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="89d85-185">Сетевой сайт</span><span class="sxs-lookup"><span data-stu-id="89d85-185">Network Site</span></span></th>
    <th><span data-ttu-id="89d85-186">Сетевой регион</span><span class="sxs-lookup"><span data-stu-id="89d85-186">Network Region</span></span></th>
    <th><span data-ttu-id="89d85-187">Ограничение пропускной способности</span><span class="sxs-lookup"><span data-stu-id="89d85-187">BW Limit</span></span></th>
    <th><span data-ttu-id="89d85-188">Ограничение для аудио</span><span class="sxs-lookup"><span data-stu-id="89d85-188">Audio Limit</span></span></th>
    <th><span data-ttu-id="89d85-189">Ограничение аудиосеансов</span><span class="sxs-lookup"><span data-stu-id="89d85-189">Audio Session Limit</span></span></th>
    <th><span data-ttu-id="89d85-190">Ограничение для видео</span><span class="sxs-lookup"><span data-stu-id="89d85-190">Video Limit</span></span></th>
    <th><span data-ttu-id="89d85-191">Ограничение видеосеансов</span><span class="sxs-lookup"><span data-stu-id="89d85-191">Video Session Limit</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="89d85-192">Альбукерке</span><span class="sxs-lookup"><span data-stu-id="89d85-192">Albuquerque</span></span></p></td>
    <td><p><span data-ttu-id="89d85-193">Северная Америка</span><span class="sxs-lookup"><span data-stu-id="89d85-193">North America</span></span></p></td>
    <td><p><span data-ttu-id="89d85-194">5 000</span><span class="sxs-lookup"><span data-stu-id="89d85-194">5,000</span></span></p></td>
    <td><p><span data-ttu-id="89d85-195">2 000</span><span class="sxs-lookup"><span data-stu-id="89d85-195">2,000</span></span></p></td>
    <td><p><span data-ttu-id="89d85-196">175</span><span class="sxs-lookup"><span data-stu-id="89d85-196">175</span></span></p></td>
    <td><p><span data-ttu-id="89d85-197">1 400</span><span class="sxs-lookup"><span data-stu-id="89d85-197">1,400</span></span></p></td>
    <td><p><span data-ttu-id="89d85-198">700</span><span class="sxs-lookup"><span data-stu-id="89d85-198">700</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="89d85-199">Рено</span><span class="sxs-lookup"><span data-stu-id="89d85-199">Reno</span></span></p></td>
    <td><p><span data-ttu-id="89d85-200">Северная Америка</span><span class="sxs-lookup"><span data-stu-id="89d85-200">North America</span></span></p></td>
    <td><p><span data-ttu-id="89d85-201">10 000</span><span class="sxs-lookup"><span data-stu-id="89d85-201">10,000</span></span></p></td>
    <td><p><span data-ttu-id="89d85-202">4 000</span><span class="sxs-lookup"><span data-stu-id="89d85-202">4,000</span></span></p></td>
    <td><p><span data-ttu-id="89d85-203">175</span><span class="sxs-lookup"><span data-stu-id="89d85-203">175</span></span></p></td>
    <td><p><span data-ttu-id="89d85-204">2 800</span><span class="sxs-lookup"><span data-stu-id="89d85-204">2,800</span></span></p></td>
    <td><p><span data-ttu-id="89d85-205">700</span><span class="sxs-lookup"><span data-stu-id="89d85-205">700</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="89d85-206">Портленд</span><span class="sxs-lookup"><span data-stu-id="89d85-206">Portland</span></span></p></td>
    <td><p><span data-ttu-id="89d85-207">Северная Америка</span><span class="sxs-lookup"><span data-stu-id="89d85-207">North America</span></span></p></td>
    <td><p><span data-ttu-id="89d85-208">5 000</span><span class="sxs-lookup"><span data-stu-id="89d85-208">5,000</span></span></p></td>
    <td><p><span data-ttu-id="89d85-209">4 000</span><span class="sxs-lookup"><span data-stu-id="89d85-209">4,000</span></span></p></td>
    <td><p><span data-ttu-id="89d85-210">175</span><span class="sxs-lookup"><span data-stu-id="89d85-210">175</span></span></p></td>
    <td><p><span data-ttu-id="89d85-211">2 800</span><span class="sxs-lookup"><span data-stu-id="89d85-211">2,800</span></span></p></td>
    <td><p><span data-ttu-id="89d85-212">700</span><span class="sxs-lookup"><span data-stu-id="89d85-212">700</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="89d85-213">Нью-Йорк</span><span class="sxs-lookup"><span data-stu-id="89d85-213">New York</span></span></p></td>
    <td><p><span data-ttu-id="89d85-214">Северная Америка</span><span class="sxs-lookup"><span data-stu-id="89d85-214">North America</span></span></p></td>
    <td><p><span data-ttu-id="89d85-215">(без ограничений)</span><span class="sxs-lookup"><span data-stu-id="89d85-215">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="89d85-216">(без ограничений)</span><span class="sxs-lookup"><span data-stu-id="89d85-216">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="89d85-217">(без ограничений)</span><span class="sxs-lookup"><span data-stu-id="89d85-217">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="89d85-218">(без ограничений)</span><span class="sxs-lookup"><span data-stu-id="89d85-218">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="89d85-219">(без ограничений)</span><span class="sxs-lookup"><span data-stu-id="89d85-219">(no limit)</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="89d85-220">Чикаго</span><span class="sxs-lookup"><span data-stu-id="89d85-220">Chicago</span></span></p></td>
    <td><p><span data-ttu-id="89d85-221">Северная Америка</span><span class="sxs-lookup"><span data-stu-id="89d85-221">North America</span></span></p></td>
    <td><p><span data-ttu-id="89d85-222">(без ограничений)</span><span class="sxs-lookup"><span data-stu-id="89d85-222">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="89d85-223">(без ограничений)</span><span class="sxs-lookup"><span data-stu-id="89d85-223">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="89d85-224">(без ограничений)</span><span class="sxs-lookup"><span data-stu-id="89d85-224">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="89d85-225">(без ограничений)</span><span class="sxs-lookup"><span data-stu-id="89d85-225">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="89d85-226">(без ограничений)</span><span class="sxs-lookup"><span data-stu-id="89d85-226">(no limit)</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="89d85-227">Детройт</span><span class="sxs-lookup"><span data-stu-id="89d85-227">Detroit</span></span></p></td>
    <td><p><span data-ttu-id="89d85-228">Северная Америка</span><span class="sxs-lookup"><span data-stu-id="89d85-228">North America</span></span></p></td>
    <td><p><span data-ttu-id="89d85-229">(без ограничений)</span><span class="sxs-lookup"><span data-stu-id="89d85-229">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="89d85-230">(без ограничений)</span><span class="sxs-lookup"><span data-stu-id="89d85-230">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="89d85-231">(без ограничений)</span><span class="sxs-lookup"><span data-stu-id="89d85-231">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="89d85-232">(без ограничений)</span><span class="sxs-lookup"><span data-stu-id="89d85-232">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="89d85-233">(без ограничений)</span><span class="sxs-lookup"><span data-stu-id="89d85-233">(no limit)</span></span></p></td>
    </tr>
    </tbody>
    </table>


6.  <span data-ttu-id="89d85-234">Для каждой подсети в вашей сети укажите связанный с ними сетевой сайт.</span><span class="sxs-lookup"><span data-stu-id="89d85-234">For every subnet in your network, specify its associated network site.</span></span>
    
    <div>
    

    > [!IMPORTANT]
    > <span data-ttu-id="89d85-p116">Каждая подсеть необходимо связать с сетевым сайтом, даже если он не ограничен по пропускной способности. Это связано с тем, что контроль допуска вызовов использует информацию о подсети, чтобы определить, на каком сетевом сайте расположена конечная точка. Когда расположение обеих сторон сеанса определено, контроль допуска вызовов может определить, достаточно ли пропускной способности для осуществления вызова. Когда сеанс инициируется по каналу без ограничения по пропускной способности, создается предупреждение.</span><span class="sxs-lookup"><span data-stu-id="89d85-p116">Every subnet in your network must be associated with a network site, even if the network site is not bandwidth constrained. This is because call admission control uses subnet information to determine at which network site an endpoint is located. When the locations of both parties in the session are determined, call admission control can determine if there is sufficient bandwidth to establish a call. When a session is established over a link that has no bandwidth limits, an alert is generated.</span></span><BR><span data-ttu-id="89d85-239">При развертывании пограничных серверов аудио- и видеоданных общедоступные IP-адреса каждого пограничного сервера должны быть связаны с тем сетевым сайтом, на котором он развертывается.</span><span class="sxs-lookup"><span data-stu-id="89d85-239">If you deploy Audio/Video Edge Servers, the public IP addresses of each Edge Server must be associated with the network site where the Edge Server is deployed.</span></span> <span data-ttu-id="89d85-240">Каждый общедоступный IP-адрес пограничного сервера аудио- и видеоданных необходимо добавить в разделе параметров конфигурации сети в качестве подсети с маской 32.</span><span class="sxs-lookup"><span data-stu-id="89d85-240">Each public IP address of the A/V Edge Server must be added to your network configuration settings as a subnet with a subnet mask of 32.</span></span> <span data-ttu-id="89d85-241">Например, при развертывании пограничных серверов аудио- и видеоданных в Чикаго следует создать для каждого внешнего IP-адреса этих серверов подсеть с маской 32 и связать сетевой сайт Чикаго с этими подсетями.</span><span class="sxs-lookup"><span data-stu-id="89d85-241">For example, if you deploy A/V Edge Servers in Chicago, then for each external IP address of those servers create a subnet with a subnet mask of 32 and associate network site Chicago with those subnets.</span></span> <span data-ttu-id="89d85-242">Дополнительные сведения об общедоступных IP-адресах можно найти в статьях <A href="lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md">Определение внешних параметров брандмауэра/V и портов для Lync Server 2013</A> в документации по планированию.</span><span class="sxs-lookup"><span data-stu-id="89d85-242">For details about public IP addresses, see <A href="lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md">Determine external A/V firewall and port requirements for Lync Server 2013</A> in the Planning documentation.</span></span>

    
    </div>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="89d85-p118">Формируется предупреждение ключевого индикатора работоспособности (KHI) со списком списка IP-адресов, которые существуют в сети, но которые либо не связаны с подсетью или связаны с подсетью, включающей IP-адреса, не связанные с сетевым сайтом. Данное предупреждение не формируется более одного раза в течение 8 часов. Далее представлены сведения о предупреждении и пример.</span><span class="sxs-lookup"><span data-stu-id="89d85-p118">A Key Health Indicator (KHI) alert is raised, specifying a list of IP addresses that are present in your network but are either not associated with a subnet, or the subnet that includes the IP addresses is not associated with a network site. This alert will not be raised more than once within an 8 hour period. The relevant alert information and an example are as follows:</span></span><BR><span data-ttu-id="89d85-246"><STRONG>Источник:</STRONG> Служба политики пропускной способности CS (ядро)</span><span class="sxs-lookup"><span data-stu-id="89d85-246"><STRONG>Source:</STRONG> CS Bandwidth Policy Service (Core)</span></span><BR><span data-ttu-id="89d85-247"><STRONG>Номер события:</STRONG> 36034</span><span class="sxs-lookup"><span data-stu-id="89d85-247"><STRONG>Event number:</STRONG> 36034</span></span><BR><span data-ttu-id="89d85-248"><STRONG>Уровень:</STRONG> 2</span><span class="sxs-lookup"><span data-stu-id="89d85-248"><STRONG>Level:</STRONG> 2</span></span><BR><span data-ttu-id="89d85-249"><STRONG>Описание:</STRONG> Подсети для указанных ниже IP-адресов: &lt; список IP-адресов &gt; либо не настроен, либо подсети не связаны с сетевым сайтом.</span><span class="sxs-lookup"><span data-stu-id="89d85-249"><STRONG>Description:</STRONG> The subnets for the following IP Addresses: &lt;List of IP Addresses&gt; are either not configured or the subnets are not associated to a network site.</span></span><BR><span data-ttu-id="89d85-250"><STRONG>Причина:</STRONG> В параметрах сетевой конфигурации отсутствуют подсети для соответствующих IP-адресов, или подсети не связаны с сетевым сайтом.</span><span class="sxs-lookup"><span data-stu-id="89d85-250"><STRONG>Cause:</STRONG> The subnets for the corresponding IP addresses are missing from the network configuration settings or the subnets are not associated to a network site.</span></span><BR><span data-ttu-id="89d85-251"><STRONG>Решение:</STRONG> Добавьте подсети, соответствующие предыдущему списку IP-адресов, в параметры конфигурации сети и свяжите каждую подсеть с сайтом сети.</span><span class="sxs-lookup"><span data-stu-id="89d85-251"><STRONG>Resolution:</STRONG> Add subnets corresponding to the preceding list of IP addresses into the network configuration settings and associate every subnet to a network site.</span></span><BR><span data-ttu-id="89d85-p119">Например, если список IP-адресов в предупреждении содержит адреса 10.121.248.226 и 10.121.249.20, эти IP-адреса не связаны с подсетью или же подсеть, с которой они связаны, не принадлежит сетевому сайту. Если 10.121.248.0/24 и 10.121.249.0/24 являются соответствующими подсетями для этих адресов, эту проблему можно решить следующим образом.</span><span class="sxs-lookup"><span data-stu-id="89d85-p119">For example, if the IP address list in the alert specifies 10.121.248.226 and 10.121.249.20, either these IP addresses are not associated with a subnet, or the subnet that they are associated with does not belong to a network site. If 10.121.248.0/24 and 10.121.249.0/24 are the corresponding subnets for these addresses, you can resolve this issue as follows:</span></span> 
    > <OL>
    > <LI>
    > <P><span data-ttu-id="89d85-254">Убедитесь в том, что IP-адрес 10.121.248.226 связан с подсетью 10.121.248.0/24, а IP-адрес 10.121.249.20 — с подсетью 10.121.249.0/24.</span><span class="sxs-lookup"><span data-stu-id="89d85-254">Be sure that IP address 10.121.248.226 is associated with the 10.121.248.0/24 subnet and IP address 10.121.249.20 is associated with the 10.121.249.0/24 subnet.</span></span></P>
    > <LI>
    > <P><span data-ttu-id="89d85-255">Убедитесь, в том что обе подсети 10.121.248.0/24 и 10.121.249.0/24 связаны с сетевым сайтом.</span><span class="sxs-lookup"><span data-stu-id="89d85-255">Be sure that the 10.121.248.0/24 and 10.121.249.0/24 subnets are each associated with a network site.</span></span></P></LI></OL>

    
    </div>
    
    ### <a name="network-sites-and-associated-subnets-bandwidth-in-kbps"></a><span data-ttu-id="89d85-256">Сетевые сайты и связанные подсети (пропускная способность в кбит/с)</span><span class="sxs-lookup"><span data-stu-id="89d85-256">Network Sites and Associated Subnets (Bandwidth in kbps)</span></span>
    
    <table>
    <colgroup>
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="89d85-257">Сетевой сайт</span><span class="sxs-lookup"><span data-stu-id="89d85-257">Network Site</span></span></th>
    <th><span data-ttu-id="89d85-258">Сетевой регион</span><span class="sxs-lookup"><span data-stu-id="89d85-258">Network Region</span></span></th>
    <th><span data-ttu-id="89d85-259">Ограничение пропускной способности</span><span class="sxs-lookup"><span data-stu-id="89d85-259">BW Limit</span></span></th>
    <th><span data-ttu-id="89d85-260">Ограничение для аудио</span><span class="sxs-lookup"><span data-stu-id="89d85-260">Audio Limit</span></span></th>
    <th><span data-ttu-id="89d85-261">Ограничение аудиосеансов</span><span class="sxs-lookup"><span data-stu-id="89d85-261">Audio Session Limit</span></span></th>
    <th><span data-ttu-id="89d85-262">Ограничение для видео</span><span class="sxs-lookup"><span data-stu-id="89d85-262">Video Limit</span></span></th>
    <th><span data-ttu-id="89d85-263">Ограничение видеосеансов</span><span class="sxs-lookup"><span data-stu-id="89d85-263">Video Session Limit</span></span></th>
    <th><span data-ttu-id="89d85-264">Подсети</span><span class="sxs-lookup"><span data-stu-id="89d85-264">Subnets</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="89d85-265">Альбукерке</span><span class="sxs-lookup"><span data-stu-id="89d85-265">Albuquerque</span></span></p></td>
    <td><p><span data-ttu-id="89d85-266">Северная Америка</span><span class="sxs-lookup"><span data-stu-id="89d85-266">North America</span></span></p></td>
    <td><p><span data-ttu-id="89d85-267">5 000</span><span class="sxs-lookup"><span data-stu-id="89d85-267">5,000</span></span></p></td>
    <td><p><span data-ttu-id="89d85-268">2 000</span><span class="sxs-lookup"><span data-stu-id="89d85-268">2,000</span></span></p></td>
    <td><p><span data-ttu-id="89d85-269">175</span><span class="sxs-lookup"><span data-stu-id="89d85-269">175</span></span></p></td>
    <td><p><span data-ttu-id="89d85-270">1 400</span><span class="sxs-lookup"><span data-stu-id="89d85-270">1,400</span></span></p></td>
    <td><p><span data-ttu-id="89d85-271">700</span><span class="sxs-lookup"><span data-stu-id="89d85-271">700</span></span></p></td>
    <td><p><span data-ttu-id="89d85-272">172.29.79.0/23, 157.57.215.0/25, 172.29.90.0/23, 172.29.80.0/24</span><span class="sxs-lookup"><span data-stu-id="89d85-272">172.29.79.0/23, 157.57.215.0/25, 172.29.90.0/23, 172.29.80.0/24</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="89d85-273">Рено</span><span class="sxs-lookup"><span data-stu-id="89d85-273">Reno</span></span></p></td>
    <td><p><span data-ttu-id="89d85-274">Северная Америка</span><span class="sxs-lookup"><span data-stu-id="89d85-274">North America</span></span></p></td>
    <td><p><span data-ttu-id="89d85-275">10 000</span><span class="sxs-lookup"><span data-stu-id="89d85-275">10,000</span></span></p></td>
    <td><p><span data-ttu-id="89d85-276">4 000</span><span class="sxs-lookup"><span data-stu-id="89d85-276">4,000</span></span></p></td>
    <td><p><span data-ttu-id="89d85-277">175</span><span class="sxs-lookup"><span data-stu-id="89d85-277">175</span></span></p></td>
    <td><p><span data-ttu-id="89d85-278">2 800</span><span class="sxs-lookup"><span data-stu-id="89d85-278">2,800</span></span></p></td>
    <td><p><span data-ttu-id="89d85-279">700</span><span class="sxs-lookup"><span data-stu-id="89d85-279">700</span></span></p></td>
    <td><p><span data-ttu-id="89d85-280">157.57.210.0/23, 172.28.151.128/25</span><span class="sxs-lookup"><span data-stu-id="89d85-280">157.57.210.0/23, 172.28.151.128/25</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="89d85-281">Портленд</span><span class="sxs-lookup"><span data-stu-id="89d85-281">Portland</span></span></p></td>
    <td><p><span data-ttu-id="89d85-282">Северная Америка</span><span class="sxs-lookup"><span data-stu-id="89d85-282">North America</span></span></p></td>
    <td><p><span data-ttu-id="89d85-283">5 000</span><span class="sxs-lookup"><span data-stu-id="89d85-283">5,000</span></span></p></td>
    <td><p><span data-ttu-id="89d85-284">4 000</span><span class="sxs-lookup"><span data-stu-id="89d85-284">4,000</span></span></p></td>
    <td><p><span data-ttu-id="89d85-285">175</span><span class="sxs-lookup"><span data-stu-id="89d85-285">175</span></span></p></td>
    <td><p><span data-ttu-id="89d85-286">2 800</span><span class="sxs-lookup"><span data-stu-id="89d85-286">2,800</span></span></p></td>
    <td><p><span data-ttu-id="89d85-287">700</span><span class="sxs-lookup"><span data-stu-id="89d85-287">700</span></span></p></td>
    <td><p><span data-ttu-id="89d85-288">172.29.77.0/24 10.71.108.0/24, 157.57.208.0/23</span><span class="sxs-lookup"><span data-stu-id="89d85-288">172.29.77.0/24 10.71.108.0/24, 157.57.208.0/23</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="89d85-289">Нью-Йорк</span><span class="sxs-lookup"><span data-stu-id="89d85-289">New York</span></span></p></td>
    <td><p><span data-ttu-id="89d85-290">Северная Америка</span><span class="sxs-lookup"><span data-stu-id="89d85-290">North America</span></span></p></td>
    <td><p><span data-ttu-id="89d85-291">(без ограничений)</span><span class="sxs-lookup"><span data-stu-id="89d85-291">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="89d85-292">(без ограничений)</span><span class="sxs-lookup"><span data-stu-id="89d85-292">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="89d85-293">(без ограничений)</span><span class="sxs-lookup"><span data-stu-id="89d85-293">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="89d85-294">(без ограничений)</span><span class="sxs-lookup"><span data-stu-id="89d85-294">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="89d85-295">(без ограничений)</span><span class="sxs-lookup"><span data-stu-id="89d85-295">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="89d85-296">172.29.80.0/23, 157.57.216.0/25, 172.29.91.0/23, 172.29.81.0/24</span><span class="sxs-lookup"><span data-stu-id="89d85-296">172.29.80.0/23, 157.57.216.0/25, 172.29.91.0/23, 172.29.81.0/24</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="89d85-297">Чикаго</span><span class="sxs-lookup"><span data-stu-id="89d85-297">Chicago</span></span></p></td>
    <td><p><span data-ttu-id="89d85-298">Северная Америка</span><span class="sxs-lookup"><span data-stu-id="89d85-298">North America</span></span></p></td>
    <td><p><span data-ttu-id="89d85-299">(без ограничений)</span><span class="sxs-lookup"><span data-stu-id="89d85-299">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="89d85-300">(без ограничений)</span><span class="sxs-lookup"><span data-stu-id="89d85-300">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="89d85-301">(без ограничений)</span><span class="sxs-lookup"><span data-stu-id="89d85-301">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="89d85-302">(без ограничений)</span><span class="sxs-lookup"><span data-stu-id="89d85-302">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="89d85-303">(без ограничений)</span><span class="sxs-lookup"><span data-stu-id="89d85-303">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="89d85-304">157.57.211.0/23, 172.28.152.128/25</span><span class="sxs-lookup"><span data-stu-id="89d85-304">157.57.211.0/23, 172.28.152.128/25</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="89d85-305">Детройт</span><span class="sxs-lookup"><span data-stu-id="89d85-305">Detroit</span></span></p></td>
    <td><p><span data-ttu-id="89d85-306">Северная Америка</span><span class="sxs-lookup"><span data-stu-id="89d85-306">North America</span></span></p></td>
    <td><p><span data-ttu-id="89d85-307">(без ограничений)</span><span class="sxs-lookup"><span data-stu-id="89d85-307">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="89d85-308">(без ограничений)</span><span class="sxs-lookup"><span data-stu-id="89d85-308">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="89d85-309">(без ограничений)</span><span class="sxs-lookup"><span data-stu-id="89d85-309">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="89d85-310">(без ограничений)</span><span class="sxs-lookup"><span data-stu-id="89d85-310">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="89d85-311">(без ограничений)</span><span class="sxs-lookup"><span data-stu-id="89d85-311">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="89d85-312">172.29.78.0/24 10.71.109.0/24, 157.57.209.0/23</span><span class="sxs-lookup"><span data-stu-id="89d85-312">172.29.78.0/24 10.71.109.0/24, 157.57.209.0/23</span></span></p></td>
    </tr>
    </tbody>
    </table>


7.  <span data-ttu-id="89d85-313">В элементе управления допуском звонков в Lync Server соединения между сетевыми областями называются *связями "регион*".</span><span class="sxs-lookup"><span data-stu-id="89d85-313">In Lync Server call admission control, the connections between network regions are called *region links*.</span></span> <span data-ttu-id="89d85-314">Для каждой связи области определите следующие параметры (как и для сетевых сайтов).</span><span class="sxs-lookup"><span data-stu-id="89d85-314">For each region link, determine the following, just as you did for the network sites:</span></span>
    
      - <span data-ttu-id="89d85-315">Общее ограничение пропускной способности, которое необходимо задать для всех параллельных аудиосеансов.</span><span class="sxs-lookup"><span data-stu-id="89d85-315">Overall bandwidth limit that you want to set for all concurrent audio sessions.</span></span> <span data-ttu-id="89d85-316">Если это ограничение будет превышено, приложение Lync Server не разрешается запускать сеанс.</span><span class="sxs-lookup"><span data-stu-id="89d85-316">If a new audio session will cause this limit to be exceeded, Lync Server does not allow the session to start.</span></span>
    
      - <span data-ttu-id="89d85-p122">Ограничение пропускной способности, которое необходимо задать для каждого отдельного аудиосеанса. По умолчанию это ограничение CAC равно 175 кбит/с, но его может изменить администратор.</span><span class="sxs-lookup"><span data-stu-id="89d85-p122">Bandwidth limit that you want to set for each individual audio session. The default CAC bandwidth limit is 175 kbps, but it can be modified by the administrator.</span></span>
    
      - <span data-ttu-id="89d85-319">Общее ограничение пропускной способности, которое необходимо задать для всех параллельных видеосеансов.</span><span class="sxs-lookup"><span data-stu-id="89d85-319">Overall bandwidth limit that you want to set for all concurrent video sessions.</span></span> <span data-ttu-id="89d85-320">Если в новом видеосеансе это ограничение будет превышено, Lync Server не разрешает запуск сеанса.</span><span class="sxs-lookup"><span data-stu-id="89d85-320">If a new video session will cause this limit to be exceeded, Lync Server does not allow the session to start.</span></span>
    
      - <span data-ttu-id="89d85-p124">Ограничение пропускной способности, которое необходимо задать для каждого отдельного видеосеанса. По умолчанию это ограничение CAC равно 700 кбит/с, но его может изменить администратор.</span><span class="sxs-lookup"><span data-stu-id="89d85-p124">Bandwidth limit that you want to set for each individual video session. The default CAC bandwidth limit is 700 kbps, but it can be modified by the administrator.</span></span>
    
    <span data-ttu-id="89d85-323">**Связи областей сети с соответствующими ограничениями пропускной способности**</span><span class="sxs-lookup"><span data-stu-id="89d85-323">**Network Region links with associated bandwidth limits**</span></span>
    
    <span data-ttu-id="89d85-324">![Пример ограничений между 3 областями](images/Gg425827.25259afa-ee7c-4d26-bc41-92ba9cb56dec(OCS.15).jpg "Пример ограничений между 3 областями")</span><span class="sxs-lookup"><span data-stu-id="89d85-324">![Example of Limitations between 3 Regions](images/Gg425827.25259afa-ee7c-4d26-bc41-92ba9cb56dec(OCS.15).jpg "Example of Limitations between 3 Regions")</span></span>  
    
    ### <a name="region-link-bandwidth-information-bandwidth-in-kbps"></a><span data-ttu-id="89d85-325">Сведения о пропускной способности связи области (пропускная способность в кбит/с)</span><span class="sxs-lookup"><span data-stu-id="89d85-325">Region Link Bandwidth Information (Bandwidth in kbps)</span></span>
    
    <table>
    <colgroup>
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="89d85-326">Имя связи области</span><span class="sxs-lookup"><span data-stu-id="89d85-326">Region Link Name</span></span></th>
    <th><span data-ttu-id="89d85-327">Первая область</span><span class="sxs-lookup"><span data-stu-id="89d85-327">First Region</span></span></th>
    <th><span data-ttu-id="89d85-328">Вторая область</span><span class="sxs-lookup"><span data-stu-id="89d85-328">Second Region</span></span></th>
    <th><span data-ttu-id="89d85-329">Ограничение пропускной способности</span><span class="sxs-lookup"><span data-stu-id="89d85-329">BW Limit</span></span></th>
    <th><span data-ttu-id="89d85-330">Ограничение для аудио</span><span class="sxs-lookup"><span data-stu-id="89d85-330">Audio Limit</span></span></th>
    <th><span data-ttu-id="89d85-331">Ограничение аудиосеансов</span><span class="sxs-lookup"><span data-stu-id="89d85-331">Audio Session Limit</span></span></th>
    <th><span data-ttu-id="89d85-332">Ограничение для видео</span><span class="sxs-lookup"><span data-stu-id="89d85-332">Video Limit</span></span></th>
    <th><span data-ttu-id="89d85-333">Ограничение видеосеансов</span><span class="sxs-lookup"><span data-stu-id="89d85-333">Video Session Limit</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="89d85-334">NA-EMEA-LINK</span><span class="sxs-lookup"><span data-stu-id="89d85-334">NA-EMEA-LINK</span></span></p></td>
    <td><p><span data-ttu-id="89d85-335">Северная Америка</span><span class="sxs-lookup"><span data-stu-id="89d85-335">North America</span></span></p></td>
    <td><p><span data-ttu-id="89d85-336">Европа, Ближний Восток и Африка</span><span class="sxs-lookup"><span data-stu-id="89d85-336">EMEA</span></span></p></td>
    <td><p><span data-ttu-id="89d85-337">50 000</span><span class="sxs-lookup"><span data-stu-id="89d85-337">50,000</span></span></p></td>
    <td><p><span data-ttu-id="89d85-338">20 000</span><span class="sxs-lookup"><span data-stu-id="89d85-338">20,000</span></span></p></td>
    <td><p><span data-ttu-id="89d85-339">175</span><span class="sxs-lookup"><span data-stu-id="89d85-339">175</span></span></p></td>
    <td><p><span data-ttu-id="89d85-340">14 000</span><span class="sxs-lookup"><span data-stu-id="89d85-340">14,000</span></span></p></td>
    <td><p><span data-ttu-id="89d85-341">700</span><span class="sxs-lookup"><span data-stu-id="89d85-341">700</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="89d85-342">EMEA-APAC-LINK</span><span class="sxs-lookup"><span data-stu-id="89d85-342">EMEA-APAC-LINK</span></span></p></td>
    <td><p><span data-ttu-id="89d85-343">Европа, Ближний Восток и Африка</span><span class="sxs-lookup"><span data-stu-id="89d85-343">EMEA</span></span></p></td>
    <td><p><span data-ttu-id="89d85-344">Азиатско-Тихоокеанский регион</span><span class="sxs-lookup"><span data-stu-id="89d85-344">APAC</span></span></p></td>
    <td><p><span data-ttu-id="89d85-345">25 000</span><span class="sxs-lookup"><span data-stu-id="89d85-345">25,000</span></span></p></td>
    <td><p><span data-ttu-id="89d85-346">10 000</span><span class="sxs-lookup"><span data-stu-id="89d85-346">10,000</span></span></p></td>
    <td><p><span data-ttu-id="89d85-347">175</span><span class="sxs-lookup"><span data-stu-id="89d85-347">175</span></span></p></td>
    <td><p><span data-ttu-id="89d85-348">7 000</span><span class="sxs-lookup"><span data-stu-id="89d85-348">7,000</span></span></p></td>
    <td><p><span data-ttu-id="89d85-349">700</span><span class="sxs-lookup"><span data-stu-id="89d85-349">700</span></span></p></td>
    </tr>
    </tbody>
    </table>


8.  <span data-ttu-id="89d85-350">Определите маршрут между каждой парой областей сети.</span><span class="sxs-lookup"><span data-stu-id="89d85-350">Define a route between every pair of network regions.</span></span>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="89d85-351">Две связи необходимы для маршрута между Северной Америкой и Азиатско-Тихоокеанской областью, поскольку отсутствует связь, которая напрямую связывает их.</span><span class="sxs-lookup"><span data-stu-id="89d85-351">Two links are required for the route between the North America and APAC regions because there is no region link that directly connects them.</span></span>

    
    </div>
    
    ### <a name="region-routes"></a><span data-ttu-id="89d85-352">Маршруты области</span><span class="sxs-lookup"><span data-stu-id="89d85-352">Region Routes</span></span>
    
    <table>
    <colgroup>
    <col style="width: 25%" />
    <col style="width: 25%" />
    <col style="width: 25%" />
    <col style="width: 25%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="89d85-353">Имя маршрута области</span><span class="sxs-lookup"><span data-stu-id="89d85-353">Region Route Name</span></span></th>
    <th><span data-ttu-id="89d85-354">Первая область</span><span class="sxs-lookup"><span data-stu-id="89d85-354">First Region</span></span></th>
    <th><span data-ttu-id="89d85-355">Вторая область</span><span class="sxs-lookup"><span data-stu-id="89d85-355">Second Region</span></span></th>
    <th><span data-ttu-id="89d85-356">Связи области</span><span class="sxs-lookup"><span data-stu-id="89d85-356">Region Links</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="89d85-357">NA-EMEA-ROUTE</span><span class="sxs-lookup"><span data-stu-id="89d85-357">NA-EMEA-ROUTE</span></span></p></td>
    <td><p><span data-ttu-id="89d85-358">Северная Америка</span><span class="sxs-lookup"><span data-stu-id="89d85-358">North America</span></span></p></td>
    <td><p><span data-ttu-id="89d85-359">Европа, Ближний Восток и Африка</span><span class="sxs-lookup"><span data-stu-id="89d85-359">EMEA</span></span></p></td>
    <td><p><span data-ttu-id="89d85-360">NA-EMEA-LINK</span><span class="sxs-lookup"><span data-stu-id="89d85-360">NA-EMEA-LINK</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="89d85-361">EMEA-APAC-ROUTE</span><span class="sxs-lookup"><span data-stu-id="89d85-361">EMEA-APAC-ROUTE</span></span></p></td>
    <td><p><span data-ttu-id="89d85-362">Европа, Ближний Восток и Африка</span><span class="sxs-lookup"><span data-stu-id="89d85-362">EMEA</span></span></p></td>
    <td><p><span data-ttu-id="89d85-363">Азиатско-Тихоокеанский регион</span><span class="sxs-lookup"><span data-stu-id="89d85-363">APAC</span></span></p></td>
    <td><p><span data-ttu-id="89d85-364">EMEA-APAC-LINK</span><span class="sxs-lookup"><span data-stu-id="89d85-364">EMEA-APAC-LINK</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="89d85-365">NA-APAC-ROUTE</span><span class="sxs-lookup"><span data-stu-id="89d85-365">NA-APAC-ROUTE</span></span></p></td>
    <td><p><span data-ttu-id="89d85-366">Северная Америка</span><span class="sxs-lookup"><span data-stu-id="89d85-366">North America</span></span></p></td>
    <td><p><span data-ttu-id="89d85-367">Азиатско-Тихоокеанский регион</span><span class="sxs-lookup"><span data-stu-id="89d85-367">APAC</span></span></p></td>
    <td><p><span data-ttu-id="89d85-368">NA-EMEA-LINK, EMEA-APAC-LINK</span><span class="sxs-lookup"><span data-stu-id="89d85-368">NA-EMEA-LINK, EMEA-APAC-LINK</span></span></p></td>
    </tr>
    </tbody>
    </table>


9.  <span data-ttu-id="89d85-369">Для каждой пары сетевых сайтов, которые соединены напрямую одной связью (которую называют *межсайтовой* связью), определите следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="89d85-369">For every pair of network sites that are directly connected by a single link (called an *inter-site* link), determine the following:</span></span>
    
      - <span data-ttu-id="89d85-370">Общее ограничение пропускной способности, которое необходимо задать для всех параллельных аудиосеансов.</span><span class="sxs-lookup"><span data-stu-id="89d85-370">Overall bandwidth limit that you want to set for all concurrent audio sessions.</span></span> <span data-ttu-id="89d85-371">Если это ограничение будет превышено, приложение Lync Server не разрешается запускать сеанс.</span><span class="sxs-lookup"><span data-stu-id="89d85-371">If a new audio session will cause this limit to be exceeded, Lync Server does not allow the session to start.</span></span>
    
      - <span data-ttu-id="89d85-p126">Ограничение пропускной способности, которое необходимо задать для каждого отдельного аудиосеанса. По умолчанию это ограничение CAC равно 175 кбит/с, но его может изменить администратор.</span><span class="sxs-lookup"><span data-stu-id="89d85-p126">Bandwidth limit that you want to set for each individual audio session. The default CAC bandwidth limit is 175 kbps, but it can be modified by the administrator.</span></span>
    
      - <span data-ttu-id="89d85-374">Общее ограничение пропускной способности, которое необходимо задать для всех параллельных видеосеансов.</span><span class="sxs-lookup"><span data-stu-id="89d85-374">Overall bandwidth limit that you want to set for all concurrent video sessions.</span></span> <span data-ttu-id="89d85-375">Если в новом видеосеансе это ограничение будет превышено, Lync Server не разрешает запуск сеанса.</span><span class="sxs-lookup"><span data-stu-id="89d85-375">If a new video session will cause this limit to be exceeded, Lync Server does not allow the session to start.</span></span>
    
      - <span data-ttu-id="89d85-p128">Ограничение пропускной способности, которое необходимо задать для каждого отдельного видеосеанса. По умолчанию это ограничение CAC равно 700 кбит/с, но его может изменить администратор.</span><span class="sxs-lookup"><span data-stu-id="89d85-p128">Bandwidth limit that you want to set for each individual video session. The default CAC bandwidth limit is 700 kbps, but it can be modified by the administrator.</span></span>
    
    <span data-ttu-id="89d85-378">**Область сети CAC Северная Америка с отображением пропускной способности и ограничений пропускной способности для межсайтовой связи между Рино и Альбукерке**</span><span class="sxs-lookup"><span data-stu-id="89d85-378">**CAC network region North America showing the bandwidth capacities and bandwidth limits for the inter-site link between Reno and Albuquerque**</span></span>
    
    <span data-ttu-id="89d85-379">![Пример сетевых узлов, ограниченных пропускной способностью глобальной сети](images/Gg425827.063e5e1d-b6c8-4e8c-98db-c227c78f671d(OCS.15).jpg "Пример сетевых узлов, ограниченных пропускной способностью глобальной сети")</span><span class="sxs-lookup"><span data-stu-id="89d85-379">![Network Sites Constrained by WAN Bandwidth example](images/Gg425827.063e5e1d-b6c8-4e8c-98db-c227c78f671d(OCS.15).jpg "Network Sites Constrained by WAN Bandwidth example")</span></span>  
    
    ### <a name="bandwidth-information-for-an-inter-site-link-between-two-network-sites-bandwidth-in-kbps"></a><span data-ttu-id="89d85-380">Сведения о пропускной способности межсайтовой связи между двумя сетевыми сайтами (пропускная способность в кбит/с)</span><span class="sxs-lookup"><span data-stu-id="89d85-380">Bandwidth Information for an Inter-Site Link between Two Network Sites (Bandwidth in kbps)</span></span>
    
    <table>
    <colgroup>
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="89d85-381">Имя межсайтовой связи</span><span class="sxs-lookup"><span data-stu-id="89d85-381">Inter-Site Link Name</span></span></th>
    <th><span data-ttu-id="89d85-382">Первый узел</span><span class="sxs-lookup"><span data-stu-id="89d85-382">First Site</span></span></th>
    <th><span data-ttu-id="89d85-383">Второй узел</span><span class="sxs-lookup"><span data-stu-id="89d85-383">Second Site</span></span></th>
    <th><span data-ttu-id="89d85-384">Ограничение пропускной способности</span><span class="sxs-lookup"><span data-stu-id="89d85-384">BW Limit</span></span></th>
    <th><span data-ttu-id="89d85-385">Ограничение для аудио</span><span class="sxs-lookup"><span data-stu-id="89d85-385">Audio Limit</span></span></th>
    <th><span data-ttu-id="89d85-386">Ограничение аудиосеансов</span><span class="sxs-lookup"><span data-stu-id="89d85-386">Audio Session Limit</span></span></th>
    <th><span data-ttu-id="89d85-387">Ограничение для видео</span><span class="sxs-lookup"><span data-stu-id="89d85-387">Video Limit</span></span></th>
    <th><span data-ttu-id="89d85-388">Ограничение видеосеансов</span><span class="sxs-lookup"><span data-stu-id="89d85-388">Video Session Limit</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="89d85-389">Reno-Albu-Intersite-Link</span><span class="sxs-lookup"><span data-stu-id="89d85-389">Reno-Albu-Intersite-Link</span></span></p></td>
    <td><p><span data-ttu-id="89d85-390">Рено</span><span class="sxs-lookup"><span data-stu-id="89d85-390">Reno</span></span></p></td>
    <td><p><span data-ttu-id="89d85-391">Альбукерке</span><span class="sxs-lookup"><span data-stu-id="89d85-391">Albuquerque</span></span></p></td>
    <td><p><span data-ttu-id="89d85-392">20 000</span><span class="sxs-lookup"><span data-stu-id="89d85-392">20,000</span></span></p></td>
    <td><p><span data-ttu-id="89d85-393">12 000</span><span class="sxs-lookup"><span data-stu-id="89d85-393">12,000</span></span></p></td>
    <td><p><span data-ttu-id="89d85-394">175</span><span class="sxs-lookup"><span data-stu-id="89d85-394">175</span></span></p></td>
    <td><p><span data-ttu-id="89d85-395">5 000</span><span class="sxs-lookup"><span data-stu-id="89d85-395">5,000</span></span></p></td>
    <td><p><span data-ttu-id="89d85-396">700</span><span class="sxs-lookup"><span data-stu-id="89d85-396">700</span></span></p></td>
    </tr>
    </tbody>
    </table>


<div>

## <a name="next-steps"></a><span data-ttu-id="89d85-397">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="89d85-397">Next Steps</span></span>

<span data-ttu-id="89d85-398">После того как вы собрали необходимые данные, вы можете выполнить развертывание CAC с помощью командной консоли Lync Server Management Shell или панели управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="89d85-398">After you have gathered the required information, you can perform CAC deployment either by using the Lync Server Management Shell or Lync Server Control Panel.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="89d85-399">Несмотря на то, что вы можете выполнять большинство задач по настройке сети с помощью панели управления Lync Server, для создания подсетей и межсайтовых ссылок необходимо использовать командную консоль Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="89d85-399">Although you can perform most network configuration tasks by using Lync Server Control Panel, to create subnets and intersite links, you must use Lync Server Management Shell.</span></span> <span data-ttu-id="89d85-400">Дополнительные сведения можно найти в документации оболочки управления Lync Server для командлетов <STRONG>New-CsNetworkSubnet</STRONG> и командлета <STRONG>New-CsNetworkIntersitePolicy</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="89d85-400">For details, see the Lync Server Management Shell documentation for the <STRONG>New-CsNetworkSubnet</STRONG> cmdlet and the <STRONG>New-CsNetworkIntersitePolicy</STRONG> cmdlet.</span></span>



<span data-ttu-id="89d85-401"></div>

</div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="89d85-401"></div>

</div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

