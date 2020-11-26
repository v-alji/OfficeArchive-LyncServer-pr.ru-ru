---
title: 'Lync Server 2013: Настройка корпоративной голосовой связи'
description: 'Lync Server 2013: Настройка корпоративной голосовой связи.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Enterprise Voice
ms:assetid: 7df179fa-d3a2-4b23-a433-b750aedf980b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994041(v=OCS.15)
ms:contentKeyID: 51803952
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 49a231b92bf7b04aa3466927a79258f0cbad4e3f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433124"
---
# <a name="configuring-enterprise-voice-in-lync-server-2013"></a><span data-ttu-id="aed59-103">Настройка корпоративной голосовой связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="aed59-103">Configuring Enterprise Voice in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="aed59-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="aed59-104">

<span> </span></span></span>

<span data-ttu-id="aed59-105">_**Тема последнего изменения:** 2013-03-12_</span><span class="sxs-lookup"><span data-stu-id="aed59-105">_**Topic Last Modified:** 2013-03-12_</span></span>

<span data-ttu-id="aed59-106">Для развертывания корпоративной голосовой связи необходимо настроить указанные ниже параметры.</span><span class="sxs-lookup"><span data-stu-id="aed59-106">To deploy Enterprise Voice, you’ll need to configure the following:</span></span>

  - <span data-ttu-id="aed59-107">Создание магистрали</span><span class="sxs-lookup"><span data-stu-id="aed59-107">Create a Trunk</span></span>

  - <span data-ttu-id="aed59-108">Определение политики голосовой связи</span><span class="sxs-lookup"><span data-stu-id="aed59-108">Define a Voice Policy</span></span>

  - <span data-ttu-id="aed59-109">Определение голосового маршрута</span><span class="sxs-lookup"><span data-stu-id="aed59-109">Define a Voice Route</span></span>

  - <span data-ttu-id="aed59-110">Enable Users for Enterprise Voice</span><span class="sxs-lookup"><span data-stu-id="aed59-110">Enable Users for Enterprise Voice</span></span>

<div>

## <a name="create-a-trunk"></a><span data-ttu-id="aed59-111">Создание магистрали</span><span class="sxs-lookup"><span data-stu-id="aed59-111">Create a Trunk</span></span>

<span data-ttu-id="aed59-112">Вы должны определить в развертывании своей корпоративной голосовой сети магистральные магистрали.</span><span class="sxs-lookup"><span data-stu-id="aed59-112">You must define trunks in your Enterprise Voice deployment.</span></span> <span data-ttu-id="aed59-113">Для маршрутизации Location-Based необходимо создать конфигурацию магистральной магистрали для каждой магистрали.</span><span class="sxs-lookup"><span data-stu-id="aed59-113">For Location-Based Routing, you must create a trunk configuration per trunk.</span></span> <span data-ttu-id="aed59-114">Используйте построитель топологии Lync Server для определения ваших каналов и используйте команду Lync Server Windows PowerShell New-CsTrunkConfiguration или панель управления Lync Server для определения соответствующих конфигураций магистрали.</span><span class="sxs-lookup"><span data-stu-id="aed59-114">Use the Lync Server Topology Builder to define your trunks, and use the Lync Server Windows PowerShell command, New-CsTrunkConfiguration, or the Lync Server Control Panel to define the corresponding trunk configurations.</span></span> <span data-ttu-id="aed59-115">Дополнительные сведения о том, как включить маршрутизацию Location-Based в конфигурациях с магистрали можно найти в разделе Включение Location-Based маршрутизации в магистральные маршруты, в разделе о том, как включить [Location-Based маршрутизацию в Lync Server 2013](lync-server-2013-enabling-location-based-routing.md).</span><span class="sxs-lookup"><span data-stu-id="aed59-115">More information on how to enable Location-Based Routing on trunk configurations can be found in the section, Enable Location-Based Routing to Trunks, in the topic, [Enabling Location-Based Routing in Lync Server 2013](lync-server-2013-enabling-location-based-routing.md).</span></span> <span data-ttu-id="aed59-116">В этом примере в следующей таблице показаны магистральные линии, используемые в этом сценарии.</span><span class="sxs-lookup"><span data-stu-id="aed59-116">For this example, the following table illustrates the trunks used in this scenario.</span></span>

<span data-ttu-id="aed59-117">Дополнительные сведения можно найти [в разделе Определение дополнительных каналов в построителе топологии в Lync Server 2013](lync-server-2013-define-additional-trunks-in-topology-builder.md).</span><span class="sxs-lookup"><span data-stu-id="aed59-117">For more information, see [Define additional trunks in Topology Builder in Lync Server 2013](lync-server-2013-define-additional-trunks-in-topology-builder.md).</span></span>


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
<th><span data-ttu-id="aed59-118">Название магистрали</span><span class="sxs-lookup"><span data-stu-id="aed59-118">Trunk name</span></span></th>
<th><span data-ttu-id="aed59-119">Тип системы</span><span class="sxs-lookup"><span data-stu-id="aed59-119">System type</span></span></th>
<th><span data-ttu-id="aed59-120">Имя</span><span class="sxs-lookup"><span data-stu-id="aed59-120">Name</span></span></th>
<th><span data-ttu-id="aed59-121">Местоположение</span><span class="sxs-lookup"><span data-stu-id="aed59-121">Location</span></span></th>
<th><span data-ttu-id="aed59-122">Сервер-посредник</span><span class="sxs-lookup"><span data-stu-id="aed59-122">Mediation Server</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aed59-123">Магистраль 1 DEL-GW</span><span class="sxs-lookup"><span data-stu-id="aed59-123">Trunk 1 DEL-GW</span></span></p></td>
<td><p><span data-ttu-id="aed59-124">Шлюз ТСОП</span><span class="sxs-lookup"><span data-stu-id="aed59-124">PSTN gateway</span></span></p></td>
<td><p><span data-ttu-id="aed59-125">DEL-GW</span><span class="sxs-lookup"><span data-stu-id="aed59-125">DEL-GW</span></span></p></td>
<td><p><span data-ttu-id="aed59-126">Delhi</span><span class="sxs-lookup"><span data-stu-id="aed59-126">Delhi</span></span></p></td>
<td><p><span data-ttu-id="aed59-127">MS1</span><span class="sxs-lookup"><span data-stu-id="aed59-127">MS1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aed59-128">Магистраль 2 HYD-GW</span><span class="sxs-lookup"><span data-stu-id="aed59-128">Trunk 2 HYD-GW</span></span></p></td>
<td><p><span data-ttu-id="aed59-129">Шлюз ТСОП</span><span class="sxs-lookup"><span data-stu-id="aed59-129">PSTN gateway</span></span></p></td>
<td><p><span data-ttu-id="aed59-130">HYD-GW</span><span class="sxs-lookup"><span data-stu-id="aed59-130">HYD-GW</span></span></p></td>
<td><p><span data-ttu-id="aed59-131">Hyderabad</span><span class="sxs-lookup"><span data-stu-id="aed59-131">Hyderabad</span></span></p></td>
<td><p><span data-ttu-id="aed59-132">MS1</span><span class="sxs-lookup"><span data-stu-id="aed59-132">MS1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aed59-133">Магистрали 3, DEL и АТС</span><span class="sxs-lookup"><span data-stu-id="aed59-133">Trunk 3 DEL-PBX</span></span></p></td>
<td><p><span data-ttu-id="aed59-134">АТС</span><span class="sxs-lookup"><span data-stu-id="aed59-134">PBX</span></span></p></td>
<td><p><span data-ttu-id="aed59-135">DELETE-УАТС</span><span class="sxs-lookup"><span data-stu-id="aed59-135">DEL-PBX</span></span></p></td>
<td><p><span data-ttu-id="aed59-136">Delhi</span><span class="sxs-lookup"><span data-stu-id="aed59-136">Delhi</span></span></p></td>
<td><p><span data-ttu-id="aed59-137">MS1</span><span class="sxs-lookup"><span data-stu-id="aed59-137">MS1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aed59-138">Магистральная HYD 4-УАТС</span><span class="sxs-lookup"><span data-stu-id="aed59-138">Trunk 4 HYD-PBX</span></span></p></td>
<td><p><span data-ttu-id="aed59-139">АТС</span><span class="sxs-lookup"><span data-stu-id="aed59-139">PBX</span></span></p></td>
<td><p><span data-ttu-id="aed59-140">HYD-УАТС</span><span class="sxs-lookup"><span data-stu-id="aed59-140">HYD-PBX</span></span></p></td>
<td><p><span data-ttu-id="aed59-141">Hyderabad</span><span class="sxs-lookup"><span data-stu-id="aed59-141">Hyderabad</span></span></p></td>
<td><p><span data-ttu-id="aed59-142">MS1</span><span class="sxs-lookup"><span data-stu-id="aed59-142">MS1</span></span></p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="defines-voice-policies"></a><span data-ttu-id="aed59-143">Определяет политики голосовой связи</span><span class="sxs-lookup"><span data-stu-id="aed59-143">Defines Voice Policies</span></span>

<span data-ttu-id="aed59-144">Вы должны определить политики голосовой связи для своего корпоративного развертывания.</span><span class="sxs-lookup"><span data-stu-id="aed59-144">You must define voice policies for your Enterprise Voice deployment.</span></span> <span data-ttu-id="aed59-145">Определение политики голосовой связи для обеспечения ограничений Location-Based ограничения маршрутизации для подмножества пользователей, если только их подмножество требуется для использования Location-Based маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="aed59-145">Define a Voice Policy to enforce Location-Based Routing restrictions to a subset of users if only a subset of them is required to use Location-Based Routing.</span></span> <span data-ttu-id="aed59-146">В этом примере в следующей таблице показаны политики голосовой связи, используемые в этом сценарии.</span><span class="sxs-lookup"><span data-stu-id="aed59-146">For this example, the following table illustrates the voice policies used in this scenario.</span></span> <span data-ttu-id="aed59-147">Только те параметры, которые относятся к Location-Based маршрутизации, включены в таблицу для целей иллюстрации.</span><span class="sxs-lookup"><span data-stu-id="aed59-147">Only settings that are specific to Location-Based Routing are included in the table for illustration purposes.</span></span>

<span data-ttu-id="aed59-148">Дополнительные сведения можно найти в разделе [Настройка политик голосовой связи и использование PSTN для авторизации функций и привилегий для звонков в Lync Server 2013](lync-server-2013-configuring-voice-policies-and-pstn-usage-records-to-authorize-calling-features-and-privileges.md).</span><span class="sxs-lookup"><span data-stu-id="aed59-148">For more information, see [Configuring voice policies and PSTN usage records to authorize calling features and privileges in Lync Server 2013](lync-server-2013-configuring-voice-policies-and-pstn-usage-records-to-authorize-calling-features-and-privileges.md).</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="aed59-149">Политика голосовой связи 1</span><span class="sxs-lookup"><span data-stu-id="aed59-149">Voice policy 1</span></span></th>
<th><span data-ttu-id="aed59-150">Политика голосовой связи 2</span><span class="sxs-lookup"><span data-stu-id="aed59-150">Voice policy 2</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aed59-151">Идентификатор политики голосовой связи</span><span class="sxs-lookup"><span data-stu-id="aed59-151">Voice policy ID</span></span></p></td>
<td><p><span data-ttu-id="aed59-152">Политика голосовой связи Delhi</span><span class="sxs-lookup"><span data-stu-id="aed59-152">Delhi voice policy</span></span></p></td>
<td><p><span data-ttu-id="aed59-153">Политика голосовой связи Hyderabad</span><span class="sxs-lookup"><span data-stu-id="aed59-153">Hyderabad voice policy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aed59-154">Использование PSTN</span><span class="sxs-lookup"><span data-stu-id="aed59-154">PSTN usages</span></span></p></td>
<td><p><span data-ttu-id="aed59-155">Использование Delhi, использование АТС DELETE, использование Hyd УАТС</span><span class="sxs-lookup"><span data-stu-id="aed59-155">Delhi usage, PBX Del usage, PBX Hyd usage</span></span></p></td>
<td><p><span data-ttu-id="aed59-156">Использование Hyderabad, Hyd УАТС, использование АТС Delete</span><span class="sxs-lookup"><span data-stu-id="aed59-156">Hyderabad usage, PBX Hyd usage, PBX Del usage</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aed59-157">PreventPSTNTollBypass</span><span class="sxs-lookup"><span data-stu-id="aed59-157">PreventPSTNTollBypass</span></span></p></td>
<td><p><span data-ttu-id="aed59-158">False</span><span class="sxs-lookup"><span data-stu-id="aed59-158">False</span></span></p></td>
<td><p><span data-ttu-id="aed59-159">False</span><span class="sxs-lookup"><span data-stu-id="aed59-159">False</span></span></p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="define-voice-routes"></a><span data-ttu-id="aed59-160">Определение маршрутов голосовой связи</span><span class="sxs-lookup"><span data-stu-id="aed59-160">Define Voice Routes</span></span>

<span data-ttu-id="aed59-161">Вы должны определить Голосовые маршруты для своего корпоративного развертывания.</span><span class="sxs-lookup"><span data-stu-id="aed59-161">You must define voice routes for your Enterprise Voice deployment.</span></span> <span data-ttu-id="aed59-162">В этом примере в приведенной ниже таблице показаны маршруты голосовой связи, используемые в этом сценарии.</span><span class="sxs-lookup"><span data-stu-id="aed59-162">For this example, the following table illustrates the voice routes used in this scenario.</span></span> <span data-ttu-id="aed59-163">Только те параметры, которые относятся к Location-Based маршрутизации, включены в таблицу для целей иллюстрации.</span><span class="sxs-lookup"><span data-stu-id="aed59-163">Only settings that are specific to Location-Based Routing are included in the table for illustration purposes.</span></span>

<span data-ttu-id="aed59-164">Дополнительные сведения можно найти [в разделе Настройка голосовых маршрутов для исходящих звонков в Lync Server 2013](lync-server-2013-configuring-voice-routes-for-outbound-calls.md).</span><span class="sxs-lookup"><span data-stu-id="aed59-164">For more information, see [Configuring voice routes for outbound calls in Lync Server 2013](lync-server-2013-configuring-voice-routes-for-outbound-calls.md).</span></span>


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
<th></th>
<th><span data-ttu-id="aed59-165">Маршрут к голосовой связи 1</span><span class="sxs-lookup"><span data-stu-id="aed59-165">Voice route 1</span></span></th>
<th><span data-ttu-id="aed59-166">Маршрут к голосовой связи 2</span><span class="sxs-lookup"><span data-stu-id="aed59-166">Voice route 2</span></span></th>
<th><span data-ttu-id="aed59-167">Маршрут голоса 3</span><span class="sxs-lookup"><span data-stu-id="aed59-167">Voice route 3</span></span></th>
<th><span data-ttu-id="aed59-168">Маршрут голосовой связи 4</span><span class="sxs-lookup"><span data-stu-id="aed59-168">Voice route 4</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aed59-169">Имя</span><span class="sxs-lookup"><span data-stu-id="aed59-169">Name</span></span></p></td>
<td><p><span data-ttu-id="aed59-170">Маршрут Delhi</span><span class="sxs-lookup"><span data-stu-id="aed59-170">Delhi route</span></span></p></td>
<td><p><span data-ttu-id="aed59-171">Маршрут Hyderabad</span><span class="sxs-lookup"><span data-stu-id="aed59-171">Hyderabad route</span></span></p></td>
<td><p><span data-ttu-id="aed59-172">Маршрут для УАТС Delete</span><span class="sxs-lookup"><span data-stu-id="aed59-172">PBX Del route</span></span></p></td>
<td><p><span data-ttu-id="aed59-173">Маршрут Hyd УАТС</span><span class="sxs-lookup"><span data-stu-id="aed59-173">PBX Hyd route</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aed59-174">Использование PSTN</span><span class="sxs-lookup"><span data-stu-id="aed59-174">PSTN usages</span></span></p></td>
<td><p><span data-ttu-id="aed59-175">Использование Delhi</span><span class="sxs-lookup"><span data-stu-id="aed59-175">Delhi usage</span></span></p></td>
<td><p><span data-ttu-id="aed59-176">Использование Hyderabad</span><span class="sxs-lookup"><span data-stu-id="aed59-176">Hyderabad usage</span></span></p></td>
<td><p><span data-ttu-id="aed59-177">Использование DELETE для АТС</span><span class="sxs-lookup"><span data-stu-id="aed59-177">PBX Del usage</span></span></p></td>
<td><p><span data-ttu-id="aed59-178">Использование Hyd УАТС</span><span class="sxs-lookup"><span data-stu-id="aed59-178">PBX Hyd usage</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aed59-179">Линия связи</span><span class="sxs-lookup"><span data-stu-id="aed59-179">Trunk</span></span></p></td>
<td><p><span data-ttu-id="aed59-180">Магистраль 1 DEL-GW</span><span class="sxs-lookup"><span data-stu-id="aed59-180">Trunk 1 DEL-GW</span></span></p></td>
<td><p><span data-ttu-id="aed59-181">Магистраль 2 HYD-GW</span><span class="sxs-lookup"><span data-stu-id="aed59-181">Trunk 2 HYD-GW</span></span></p></td>
<td><p><span data-ttu-id="aed59-182">Магистрали 3, DEL и АТС</span><span class="sxs-lookup"><span data-stu-id="aed59-182">Trunk 3 DEL-PBX</span></span></p></td>
<td><p><span data-ttu-id="aed59-183">Магистральная HYD 4-УАТС</span><span class="sxs-lookup"><span data-stu-id="aed59-183">Trunk 4 HYD-PBX</span></span></p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="enable-users-for-enterprise-voice"></a><span data-ttu-id="aed59-184">Enable Users for Enterprise Voice</span><span class="sxs-lookup"><span data-stu-id="aed59-184">Enable Users for Enterprise Voice</span></span>

<span data-ttu-id="aed59-185">Включите пользователей для корпоративного голоса и назначьте им политику голосовой связи, которую вы определили ранее.</span><span class="sxs-lookup"><span data-stu-id="aed59-185">Enable users for Enterprise Voice and assign them a voice policy you’ve previously defined.</span></span> <span data-ttu-id="aed59-186">В этом примере в приведенной ниже таблице показано назначение, используемое в этом сценарии.</span><span class="sxs-lookup"><span data-stu-id="aed59-186">For this example, the following table illustrates the assignment used in this scenario.</span></span> <span data-ttu-id="aed59-187">Только те параметры, которые относятся к Location-Based маршрутизации, включены в таблицу для целей иллюстрации.</span><span class="sxs-lookup"><span data-stu-id="aed59-187">Only settings that are specific to Location-Based Routing are included in the table for illustration purposes.</span></span>

<span data-ttu-id="aed59-188">Дополнительные сведения можно найти [в разделе Включение пользователей для корпоративной голосовой связи в Lync Server 2013](lync-server-2013-enable-users-for-enterprise-voice.md).</span><span class="sxs-lookup"><span data-stu-id="aed59-188">For more information, see [Enable users for Enterprise Voice in Lync Server 2013](lync-server-2013-enable-users-for-enterprise-voice.md).</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="aed59-189">Пользователи, находящиеся в Delhi</span><span class="sxs-lookup"><span data-stu-id="aed59-189">Users located in Delhi</span></span></th>
<th><span data-ttu-id="aed59-190">Пользователи, находящиеся в Hyderabad</span><span class="sxs-lookup"><span data-stu-id="aed59-190">Users located in Hyderabad</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aed59-191">Соответствующая политика голосовой связи</span><span class="sxs-lookup"><span data-stu-id="aed59-191">Associated voice policy</span></span></p></td>
<td><p><span data-ttu-id="aed59-192">Политика голосовой связи Delhi</span><span class="sxs-lookup"><span data-stu-id="aed59-192">Delhi voice policy</span></span></p></td>
<td><p><span data-ttu-id="aed59-193">Политика голосовой связи Hyderabad</span><span class="sxs-lookup"><span data-stu-id="aed59-193">Hyderabad voice policy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aed59-194">Примеры пользователей</span><span class="sxs-lookup"><span data-stu-id="aed59-194">Sample users</span></span></p></td>
<td><p><span data-ttu-id="aed59-195">DEL — LYNC-1, DEL-LYNC-2, DEL-LYNC-3</span><span class="sxs-lookup"><span data-stu-id="aed59-195">DEL-LYNC-1,DEL-LYNC-2,DEL-LYNC-3</span></span></p></td>
<td><p><span data-ttu-id="aed59-196">HYD-LYNC-1, HYD-LYNC-2, HYD-LYNC-3</span><span class="sxs-lookup"><span data-stu-id="aed59-196">HYD-LYNC-1, HYD-LYNC-2, HYD-LYNC-3</span></span></p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="aed59-197">См. также</span><span class="sxs-lookup"><span data-stu-id="aed59-197">See Also</span></span>


[<span data-ttu-id="aed59-198">Настройка маршрутизации на основе расположения в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="aed59-198">Configuring Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-configuring-location-based-routing.md)  
  

<span data-ttu-id="aed59-199"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="aed59-199"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

