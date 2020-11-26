---
title: 'Lync Server 2013: настройка маршрутизации на основе расположения'
description: 'Lync Server 2013: Настройка маршрутизации Location-Based.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Location-Based Routing
ms:assetid: 63cdc474-e80f-43b1-a237-9d9ed673300a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994036(v=OCS.15)
ms:contentKeyID: 51803946
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 080c2a3a82a8714fc35ce882b0c6cb1630552f27
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433046"
---
# <a name="configuring-location-based-routing-in-lync-server-2013"></a><span data-ttu-id="2d46d-103">Настройка маршрутизации на основе расположения в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2d46d-103">Configuring Location-Based Routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2d46d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2d46d-104">

<span> </span></span></span>

<span data-ttu-id="2d46d-105">_**Тема последнего изменения:** 2013-03-12_</span><span class="sxs-lookup"><span data-stu-id="2d46d-105">_**Topic Last Modified:** 2013-03-12_</span></span>

<span data-ttu-id="2d46d-106">Lync Server 2013 CU1, Location-Based маршрутизация — это функция корпоративной голосовой связи.</span><span class="sxs-lookup"><span data-stu-id="2d46d-106">Lync Server 2013 CU1, Location-Based Routing is a feature of Enterprise Voice.</span></span> <span data-ttu-id="2d46d-107">Location-Based маршрутизация — это функция управления звонками, определяющая способ маршрутизации звонков Lync Server 2013 CU1.</span><span class="sxs-lookup"><span data-stu-id="2d46d-107">Location-Based Routing is a call management feature that controls how calls are routed by Lync Server 2013 CU1.</span></span> <span data-ttu-id="2d46d-108">Она обеспечивает ограничения на то, могут ли звонки перенаправляться в адреса для АТС или PSTN, основываясь на расположении вызывающего абонента Lync.</span><span class="sxs-lookup"><span data-stu-id="2d46d-108">It enforces restrictions on whether calls can be routed to PBX or PSTN destinations based on the Lync caller’s location.</span></span> <span data-ttu-id="2d46d-109">Location-Based маршрутизация применяет правила авторизации вызовов к КОММУТИРУЕМым звонкам на основе сетевого расположения вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="2d46d-109">Location-Based Routing applies call authorization rules to PSTN calls based on the caller’s network location.</span></span> <span data-ttu-id="2d46d-110">Расположение вызывающего абонента определяется на основе сетевого сайта, связанного с сетевой подсетью, в которой подключен вызывающий абонент.</span><span class="sxs-lookup"><span data-stu-id="2d46d-110">The caller’s location is determined based on the network site associated with the network subnet the caller is connected on.</span></span> <span data-ttu-id="2d46d-111">Для настройки маршрутизации Location-Based сначала необходимо развернуть корпоративный голос, а затем настроить регионы сети, сайты и подсети.</span><span class="sxs-lookup"><span data-stu-id="2d46d-111">Configuring Location-Based Routing requires first deploying Enterprise Voice, then configuring network regions, sites and subnets.</span></span> <span data-ttu-id="2d46d-112">Таким образом, вы задаете основу для включения Location-Based маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="2d46d-112">This sets up the foundation for enabling Location-Based Routing.</span></span>

<span data-ttu-id="2d46d-113">Прежде чем развертывать Location-Based маршрут, необходимо сначала развернуть корпоративный голос и настроить регионы сети, сайты и связать сетевые подсети с сетевыми сайтами.</span><span class="sxs-lookup"><span data-stu-id="2d46d-113">Before deploying Location-Based Routing, you must first deploy Enterprise Voice, and configure network regions, sites, and associate network subnets to your network sites.</span></span> <span data-ttu-id="2d46d-114">После завершения настройки можно настроить маршрутизацию Location-Based.</span><span class="sxs-lookup"><span data-stu-id="2d46d-114">Once completed, you can configure Location-Based Routing.</span></span> <span data-ttu-id="2d46d-115">Инструкции по настройке регионов сети, сайтов и подсетей можно найти [в статье развертывание расширенных функций голосовой связи для предприятий в Lync Server 2013](lync-server-2013-deploying-advanced-enterprise-voice-features.md)</span><span class="sxs-lookup"><span data-stu-id="2d46d-115">For steps on how to configure network regions, sites and subnets, see [Deploying advanced Enterprise Voice features in Lync Server 2013](lync-server-2013-deploying-advanced-enterprise-voice-features.md)</span></span>

<span data-ttu-id="2d46d-116">В этом разделе рассказывается о настройке маршрутизации Location-Based с помощью приведенного ниже примера.</span><span class="sxs-lookup"><span data-stu-id="2d46d-116">This section guides you through the configuration of Location-Based Routing using the following example as illustration.</span></span>

<span data-ttu-id="2d46d-117">![Пример маршрутизации на основе расположения голоса в корпоративной среде](images/JJ994036.b6ef5afc-36ac-406f-8ec2-a87532b20612(OCS.15).png "Пример маршрутизации на основе расположения голоса в корпоративной среде")</span><span class="sxs-lookup"><span data-stu-id="2d46d-117">![Enterprise Voice location-based routing example](images/JJ994036.b6ef5afc-36ac-406f-8ec2-a87532b20612(OCS.15).png "Enterprise Voice location-based routing example")</span></span>

  
<span data-ttu-id="2d46d-118">В следующей таблице представлены пользователи, определенные в этом примере.</span><span class="sxs-lookup"><span data-stu-id="2d46d-118">The following table represents the users defined in this example.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2d46d-119">Тип конечной точки</span><span class="sxs-lookup"><span data-stu-id="2d46d-119">Endpoint type</span></span></th>
<th><span data-ttu-id="2d46d-120">Местоположение</span><span class="sxs-lookup"><span data-stu-id="2d46d-120">Location</span></span></th>
<th><span data-ttu-id="2d46d-121">Пользователи</span><span class="sxs-lookup"><span data-stu-id="2d46d-121">Users</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2d46d-122">Lync</span><span class="sxs-lookup"><span data-stu-id="2d46d-122">Lync</span></span></p></td>
<td><p><span data-ttu-id="2d46d-123">Корпоративный офис Delhi</span><span class="sxs-lookup"><span data-stu-id="2d46d-123">Delhi corporate office</span></span></p></td>
<td><p><span data-ttu-id="2d46d-124">DEL — LYNC-1, DEL-LYNC-2, DEL-LYNC-3</span><span class="sxs-lookup"><span data-stu-id="2d46d-124">DEL-LYNC-1,DEL-LYNC-2,DEL-LYNC-3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d46d-125">Lync</span><span class="sxs-lookup"><span data-stu-id="2d46d-125">Lync</span></span></p></td>
<td><p><span data-ttu-id="2d46d-126">Корпоративный офис Hyderabad</span><span class="sxs-lookup"><span data-stu-id="2d46d-126">Hyderabad corporate office</span></span></p></td>
<td><p><span data-ttu-id="2d46d-127">HYD-LYNC-1, HYD-LYNC-2, HYD-LYNC-3</span><span class="sxs-lookup"><span data-stu-id="2d46d-127">HYD-LYNC-1, HYD-LYNC-2, HYD-LYNC-3</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d46d-128">Lync</span><span class="sxs-lookup"><span data-stu-id="2d46d-128">Lync</span></span></p></td>
<td><p><span data-ttu-id="2d46d-129">Неизвестно (например, Гостиницы)</span><span class="sxs-lookup"><span data-stu-id="2d46d-129">Unknown (i.e. hotel)</span></span></p></td>
<td><p><span data-ttu-id="2d46d-130">UNK-LYNC-1</span><span class="sxs-lookup"><span data-stu-id="2d46d-130">UNK-LYNC-1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d46d-131">АТС</span><span class="sxs-lookup"><span data-stu-id="2d46d-131">PBX</span></span></p></td>
<td><p><span data-ttu-id="2d46d-132">Корпоративный офис Delhi</span><span class="sxs-lookup"><span data-stu-id="2d46d-132">Delhi corporate office</span></span></p></td>
<td><p><span data-ttu-id="2d46d-133">DEL-УАТС-1, DEL-УАТС-2</span><span class="sxs-lookup"><span data-stu-id="2d46d-133">DEL-PBX-1, DEL-PBX-2</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d46d-134">АТС</span><span class="sxs-lookup"><span data-stu-id="2d46d-134">PBX</span></span></p></td>
<td><p><span data-ttu-id="2d46d-135">Корпоративный офис Hyderabad</span><span class="sxs-lookup"><span data-stu-id="2d46d-135">Hyderabad corporate office</span></span></p></td>
<td><p><span data-ttu-id="2d46d-136">HYD-УАТС-1, HYD-УАТС-2</span><span class="sxs-lookup"><span data-stu-id="2d46d-136">HYD-PBX-1, HYD-PBX-2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d46d-137">ТСОП</span><span class="sxs-lookup"><span data-stu-id="2d46d-137">PSTN</span></span></p></td>
<td><p><span data-ttu-id="2d46d-138">Неожиданно</span><span class="sxs-lookup"><span data-stu-id="2d46d-138">Unknown</span></span></p></td>
<td><p><span data-ttu-id="2d46d-139">PSTN-1, PSTN-2, КТСОП-3</span><span class="sxs-lookup"><span data-stu-id="2d46d-139">PSTN-1, PSTN-2, PSTN-3</span></span></p></td>
</tr>
</tbody>
</table>

  

<span data-ttu-id="2d46d-140">В следующей таблице представлены системы, показанные в этом примере среды.</span><span class="sxs-lookup"><span data-stu-id="2d46d-140">The following table represents the systems illustrated in this example environment.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2d46d-141">Администратор</span><span class="sxs-lookup"><span data-stu-id="2d46d-141">System</span></span></th>
<th><span data-ttu-id="2d46d-142">Местоположение</span><span class="sxs-lookup"><span data-stu-id="2d46d-142">Location</span></span></th>
<th><span data-ttu-id="2d46d-143">Имя</span><span class="sxs-lookup"><span data-stu-id="2d46d-143">Name</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2d46d-144">Пул Lync Server 2013 CU1</span><span class="sxs-lookup"><span data-stu-id="2d46d-144">Lync Server 2013 CU1 pool</span></span></p></td>
<td><p><span data-ttu-id="2d46d-145">любой</span><span class="sxs-lookup"><span data-stu-id="2d46d-145">any</span></span></p></td>
<td><p><span data-ttu-id="2d46d-146">LS-PL1</span><span class="sxs-lookup"><span data-stu-id="2d46d-146">LS-PL1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d46d-147">Lync Server 2013 CU1, сервер для устранения проблем</span><span class="sxs-lookup"><span data-stu-id="2d46d-147">Lync Server 2013 CU1, Mediation Server</span></span></p></td>
<td><p><span data-ttu-id="2d46d-148">любой</span><span class="sxs-lookup"><span data-stu-id="2d46d-148">any</span></span></p></td>
<td><p><span data-ttu-id="2d46d-149">MS-PL1</span><span class="sxs-lookup"><span data-stu-id="2d46d-149">MS-PL1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d46d-150">Шлюз PSTN 1</span><span class="sxs-lookup"><span data-stu-id="2d46d-150">PSTN gateway 1</span></span></p></td>
<td><p><span data-ttu-id="2d46d-151">Delhi</span><span class="sxs-lookup"><span data-stu-id="2d46d-151">Delhi</span></span></p></td>
<td><p><span data-ttu-id="2d46d-152">DEL-GW</span><span class="sxs-lookup"><span data-stu-id="2d46d-152">DEL-GW</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d46d-153">Шлюз PSTN 2</span><span class="sxs-lookup"><span data-stu-id="2d46d-153">PSTN gateway 2</span></span></p></td>
<td><p><span data-ttu-id="2d46d-154">Hyderabad</span><span class="sxs-lookup"><span data-stu-id="2d46d-154">Hyderabad</span></span></p></td>
<td><p><span data-ttu-id="2d46d-155">HYD-GW</span><span class="sxs-lookup"><span data-stu-id="2d46d-155">HYD-GW</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d46d-156">АТС 1</span><span class="sxs-lookup"><span data-stu-id="2d46d-156">PBX 1</span></span></p></td>
<td><p><span data-ttu-id="2d46d-157">Delhi</span><span class="sxs-lookup"><span data-stu-id="2d46d-157">Delhi</span></span></p></td>
<td><p><span data-ttu-id="2d46d-158">DELETE-УАТС</span><span class="sxs-lookup"><span data-stu-id="2d46d-158">DEL-PBX</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d46d-159">АТС 2</span><span class="sxs-lookup"><span data-stu-id="2d46d-159">PBX 2</span></span></p></td>
<td><p><span data-ttu-id="2d46d-160">Hyderabad</span><span class="sxs-lookup"><span data-stu-id="2d46d-160">Hyderabad</span></span></p></td>
<td><p><span data-ttu-id="2d46d-161">КРАСНАЯ-УАТС</span><span class="sxs-lookup"><span data-stu-id="2d46d-161">RED-PBX</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="in-this-section"></a><span data-ttu-id="2d46d-162">Содержание</span><span class="sxs-lookup"><span data-stu-id="2d46d-162">In This Section</span></span>

  - [<span data-ttu-id="2d46d-163">Настройка корпоративной голосовой связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2d46d-163">Configuring Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-configuring-enterprise-voice.md)

  - [<span data-ttu-id="2d46d-164">Развертывание регионов сети, сайтов и подсетей в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2d46d-164">Deploying network regions, sites, and subnets in Lync Server 2013</span></span>](lync-server-2013-deploying-network-regions-sites-and-subnets.md)

  - [<span data-ttu-id="2d46d-165">Включение маршрутизации Location-Based в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2d46d-165">Enabling Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-enabling-location-based-routing.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="2d46d-166">См. также</span><span class="sxs-lookup"><span data-stu-id="2d46d-166">See Also</span></span>


[<span data-ttu-id="2d46d-167">Развертывание улучшенных функций голосовой связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2d46d-167">Deploying advanced Enterprise Voice features in Lync Server 2013</span></span>](lync-server-2013-deploying-advanced-enterprise-voice-features.md)  
  

<span data-ttu-id="2d46d-168"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2d46d-168"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

