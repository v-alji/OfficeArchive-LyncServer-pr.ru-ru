---
title: 'Lync Server 2013: настройка маршрута отработки отказа'
description: 'Lync Server 2013: Настройка маршрута для перемещения при сбое.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring a failover route
ms:assetid: 76e48df4-3b78-4fb7-b1f7-c1e604b81bad
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398581(v=OCS.15)
ms:contentKeyID: 48184542
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e7cfc45276931685a2d42103b1b7f1d5015dcd7e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433523"
---
# <a name="configuring-a-failover-route-in-lync-server-2013"></a><span data-ttu-id="fc078-103">Настройка маршрута отработки отказа в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fc078-103">Configuring a failover route in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fc078-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fc078-104">

<span> </span></span></span>

<span data-ttu-id="fc078-105">_**Тема последнего изменения:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="fc078-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="fc078-p101">В следующем примере показано, как администратор может определить маршрут отработки отказа на тот случай, если шлюз Dallas-GW1 отключается для проведения технического обслуживания или недоступен по иным причинам. В таблице ниже показаны изменения, которые нужно внести в конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="fc078-p101">The following example shows how an administrator can define a failover route for use if the Dallas-GW1 is down for maintenance or is otherwise unavailable. The following tables illustrate the required configuration change.</span></span>

### <a name="table-1-user-policy"></a><span data-ttu-id="fc078-p102">Таблица 1. Политика пользователя</span><span class="sxs-lookup"><span data-stu-id="fc078-p102">Table 1. User Policy</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fc078-110">Политика пользователя</span><span class="sxs-lookup"><span data-stu-id="fc078-110">User policy</span></span></th>
<th><span data-ttu-id="fc078-111">Использование телефонов</span><span class="sxs-lookup"><span data-stu-id="fc078-111">Phone usage</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fc078-112">Политика звонков по умолчанию</span><span class="sxs-lookup"><span data-stu-id="fc078-112">Default Calling Policy</span></span></p></td>
<td><p><span data-ttu-id="fc078-113">Local</span><span class="sxs-lookup"><span data-stu-id="fc078-113">Local</span></span></p>
<p><span data-ttu-id="fc078-114">GlobalPSTNHopoff</span><span class="sxs-lookup"><span data-stu-id="fc078-114">GlobalPSTNHopoff</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc078-115">Локальная политика в Редмонде</span><span class="sxs-lookup"><span data-stu-id="fc078-115">Redmond Local Policy</span></span></p></td>
<td><p><span data-ttu-id="fc078-116">RedmondLocal</span><span class="sxs-lookup"><span data-stu-id="fc078-116">RedmondLocal</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc078-117">Политика звонков в Далласе</span><span class="sxs-lookup"><span data-stu-id="fc078-117">Dallas Calling Policy</span></span></p></td>
<td><p><span data-ttu-id="fc078-118">DallasUsers</span><span class="sxs-lookup"><span data-stu-id="fc078-118">DallasUsers</span></span></p>
<p><span data-ttu-id="fc078-119">GlobalPSTNHopoff</span><span class="sxs-lookup"><span data-stu-id="fc078-119">GlobalPSTNHopoff</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="table-2-routes"></a><span data-ttu-id="fc078-p103">Таблица 2. Маршруты</span><span class="sxs-lookup"><span data-stu-id="fc078-p103">Table 2. Routes</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fc078-122">Название маршрута</span><span class="sxs-lookup"><span data-stu-id="fc078-122">Route name</span></span></th>
<th><span data-ttu-id="fc078-123">Шаблон номера</span><span class="sxs-lookup"><span data-stu-id="fc078-123">Number pattern</span></span></th>
<th><span data-ttu-id="fc078-124">Использование телефонов</span><span class="sxs-lookup"><span data-stu-id="fc078-124">Phone usage</span></span></th>
<th><span data-ttu-id="fc078-125">Линия связи</span><span class="sxs-lookup"><span data-stu-id="fc078-125">Trunk</span></span></th>
<th><span data-ttu-id="fc078-126">Шлюз</span><span class="sxs-lookup"><span data-stu-id="fc078-126">Gateway</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fc078-127">Локальный маршрут в Редмонде</span><span class="sxs-lookup"><span data-stu-id="fc078-127">Redmond Local Route</span></span></p></td>
<td><p><span data-ttu-id="fc078-128">^\+1 (425 | 206 | 253) (\d {7} ) $</span><span class="sxs-lookup"><span data-stu-id="fc078-128">^\+1(425|206|253)(\d{7})$</span></span></p></td>
<td><p><span data-ttu-id="fc078-129">Local</span><span class="sxs-lookup"><span data-stu-id="fc078-129">Local</span></span></p>
<p><span data-ttu-id="fc078-130">RedmondLocal</span><span class="sxs-lookup"><span data-stu-id="fc078-130">RedmondLocal</span></span></p></td>
<td><p><span data-ttu-id="fc078-131">Trunk1</span><span class="sxs-lookup"><span data-stu-id="fc078-131">Trunk1</span></span></p>
<p><span data-ttu-id="fc078-132">Trunk2</span><span class="sxs-lookup"><span data-stu-id="fc078-132">Trunk2</span></span></p></td>
<td><p><span data-ttu-id="fc078-133">Red-GW1</span><span class="sxs-lookup"><span data-stu-id="fc078-133">Red-GW1</span></span></p>
<p><span data-ttu-id="fc078-134">Red-GW2</span><span class="sxs-lookup"><span data-stu-id="fc078-134">Red-GW2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc078-135">Локальный маршрут в Далласе</span><span class="sxs-lookup"><span data-stu-id="fc078-135">Dallas Local Route</span></span></p></td>
<td><p><span data-ttu-id="fc078-136">^\+1 (972 | 214 | 469) (\d {7} ) $</span><span class="sxs-lookup"><span data-stu-id="fc078-136">^\+1(972|214|469)(\d{7})$</span></span></p></td>
<td><p><span data-ttu-id="fc078-137">Local</span><span class="sxs-lookup"><span data-stu-id="fc078-137">Local</span></span></p></td>
<td><p><span data-ttu-id="fc078-138">Trunk3</span><span class="sxs-lookup"><span data-stu-id="fc078-138">Trunk3</span></span></p></td>
<td><p><span data-ttu-id="fc078-139">Dallas-GW1</span><span class="sxs-lookup"><span data-stu-id="fc078-139">Dallas-GW1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc078-140">Универсальный маршрут</span><span class="sxs-lookup"><span data-stu-id="fc078-140">Universal Route</span></span></p></td>
<td><p><span data-ttu-id="fc078-141">^\+? (\d \*) $</span><span class="sxs-lookup"><span data-stu-id="fc078-141">^\+?(\d\*)$</span></span></p></td>
<td><p><span data-ttu-id="fc078-142">GlobalPSTNHopoff</span><span class="sxs-lookup"><span data-stu-id="fc078-142">GlobalPSTNHopoff</span></span></p></td>
<td><p><span data-ttu-id="fc078-143">Trunk1</span><span class="sxs-lookup"><span data-stu-id="fc078-143">Trunk1</span></span></p>
<p><span data-ttu-id="fc078-144">Trunk2</span><span class="sxs-lookup"><span data-stu-id="fc078-144">Trunk2</span></span></p>
<p><span data-ttu-id="fc078-145">Trunk3</span><span class="sxs-lookup"><span data-stu-id="fc078-145">Trunk3</span></span></p></td>
<td><p><span data-ttu-id="fc078-146">Red-GW1</span><span class="sxs-lookup"><span data-stu-id="fc078-146">Red-GW1</span></span></p>
<p><span data-ttu-id="fc078-147">Red-GW2</span><span class="sxs-lookup"><span data-stu-id="fc078-147">Red-GW2</span></span></p>
<p><span data-ttu-id="fc078-148">Dallas-GW1</span><span class="sxs-lookup"><span data-stu-id="fc078-148">Dallas-GW1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc078-149">Маршрут для пользователей в Далласе</span><span class="sxs-lookup"><span data-stu-id="fc078-149">Dallas Users Route</span></span></p></td>
<td><p><span data-ttu-id="fc078-150">^\+? (\d \*) $</span><span class="sxs-lookup"><span data-stu-id="fc078-150">^\+?(\d\*)$</span></span></p></td>
<td><p><span data-ttu-id="fc078-151">DallasUsers</span><span class="sxs-lookup"><span data-stu-id="fc078-151">DallasUsers</span></span></p></td>
<td><p><span data-ttu-id="fc078-152">Trunk3</span><span class="sxs-lookup"><span data-stu-id="fc078-152">Trunk3</span></span></p></td>
<td><p><span data-ttu-id="fc078-153">Dallas-GW1</span><span class="sxs-lookup"><span data-stu-id="fc078-153">Dallas-GW1</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fc078-p104">В таблице 1 использование телефона GlobalPSTNHopoff добавлено после использования телефона DallasUsers в политике звонков в Далласе. Это позволяет использовать для звонков, к которым применяется политика звонков в Далласе, маршруты, настроенные для использования телефонов GlobalPSTNHopoff, если маршрут, заданный для использования телефонов DallasUsers, недоступен.</span><span class="sxs-lookup"><span data-stu-id="fc078-p104">In Table 1, a phone usage of GlobalPSTNHopoff is added after the DallasUsers phone usage in the Dallas Calling Policy. This enables calls with the Dallas Calling policy to use routes that are configured for the GlobalPSTNHopoff phone usage if a route for the DallasUsers phone usage is unavailable.</span></span>

<span data-ttu-id="fc078-156"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fc078-156"></div>

<span> </span>

</div>

</div>

</span></span></div>

