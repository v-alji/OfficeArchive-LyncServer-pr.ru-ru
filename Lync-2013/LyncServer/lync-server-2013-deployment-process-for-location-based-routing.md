---
title: 'Lync Server 2013: процесс развертывания функции маршрутизации на основе местоположения'
description: 'Lync Server 2013: процесс развертывания для Location-Based маршрутизации.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment process for Location-Based Routing
ms:assetid: 9e923e72-83fc-4a4f-8937-28a55739ed3e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994055(v=OCS.15)
ms:contentKeyID: 51803966
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2c321d9b0eada6e9501b2ded69120feae36be171
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399568"
---
# <a name="deployment-process-for-location-based-routing-in-lync-server-2013"></a><span data-ttu-id="450bb-103">Процесс развертывания функции маршрутизации на основе местоположения в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="450bb-103">Deployment process for Location-Based Routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="450bb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="450bb-104">

<span> </span></span></span>

<span data-ttu-id="450bb-105">_**Тема последнего изменения:** 2013-03-09_</span><span class="sxs-lookup"><span data-stu-id="450bb-105">_**Topic Last Modified:** 2013-03-09_</span></span>

<span data-ttu-id="450bb-106">В этом разделе приводятся общие сведения о процессе настройки маршрутизации Location-Based.</span><span class="sxs-lookup"><span data-stu-id="450bb-106">This topic provides an overview of the process involved in configuring Location-Based Routing.</span></span> <span data-ttu-id="450bb-107">Перед настройкой маршрутизации Location-Based вы должны развернуть Lync Server Enterprise Edition или Standard Edition с корпоративной голосовой связью.</span><span class="sxs-lookup"><span data-stu-id="450bb-107">You must deploy Lync Server Enterprise Edition or Standard Edition with Enterprise Voice before you configure Location-Based Routing.</span></span> <span data-ttu-id="450bb-108">Компоненты, необходимые для маршрутизации Location-Based, уже установлены и включены при развертывании корпоративной голосовой связи.</span><span class="sxs-lookup"><span data-stu-id="450bb-108">The components required by Location-Based Routing are already installed and enabled when you deploy Enterprise Voice.</span></span>

### <a name="location-based-routing-deployment-process"></a><span data-ttu-id="450bb-109">Процесс развертывания Location-Based маршрутизации</span><span class="sxs-lookup"><span data-stu-id="450bb-109">Location-Based Routing Deployment Process</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="450bb-110">Этап</span><span class="sxs-lookup"><span data-stu-id="450bb-110">Phase</span></span></th>
<th><span data-ttu-id="450bb-111">Шаги</span><span class="sxs-lookup"><span data-stu-id="450bb-111">Steps</span></span></th>
<th><span data-ttu-id="450bb-112">Необходимые группы и роли</span><span class="sxs-lookup"><span data-stu-id="450bb-112">Required groups and roles</span></span></th>
<th><span data-ttu-id="450bb-113">Документация по развертыванию</span><span class="sxs-lookup"><span data-stu-id="450bb-113">Deployment documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="450bb-114">Развертывание корпоративной голосовой связи</span><span class="sxs-lookup"><span data-stu-id="450bb-114">Deploy Enterprise Voice</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="450bb-115">Настройка каналов</span><span class="sxs-lookup"><span data-stu-id="450bb-115">Configure Trunks</span></span></p></li>
<li><p><span data-ttu-id="450bb-116">Создание политик голосовой связи</span><span class="sxs-lookup"><span data-stu-id="450bb-116">Create Voice Policies</span></span></p></li>
<li><p><span data-ttu-id="450bb-117">Определение маршрутов голосовой связи</span><span class="sxs-lookup"><span data-stu-id="450bb-117">Define Voice Routes</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="450bb-118">CSVoiceAdmins</span><span class="sxs-lookup"><span data-stu-id="450bb-118">CSVoiceAdmins</span></span><br />
<span data-ttu-id="450bb-119">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="450bb-119">CsAdministrator</span></span><br />
<span data-ttu-id="450bb-120">CsServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="450bb-120">CsServerAdministrator</span></span></p></td>
<td><p><span data-ttu-id="450bb-121">Развертывание корпоративной голосовой связи</span><span class="sxs-lookup"><span data-stu-id="450bb-121">Deploying Enterprise Voice</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="450bb-122">Проверка развертывания голосовой связи в корпоративной среде</span><span class="sxs-lookup"><span data-stu-id="450bb-122">Verify your Enterprise Voice deployment</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="450bb-123">CSVoiceAdmins</span><span class="sxs-lookup"><span data-stu-id="450bb-123">CSVoiceAdmins</span></span><br />
<span data-ttu-id="450bb-124">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="450bb-124">CsAdministrator</span></span><br />
<span data-ttu-id="450bb-125">CsServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="450bb-125">CsServerAdministrator</span></span></p></td>
<td> </td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="450bb-126">Настройка регионов, сайтов и подсетей сети</span><span class="sxs-lookup"><span data-stu-id="450bb-126">Configure network regions, sites, and subnets</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="450bb-127">Создание областей сети</span><span class="sxs-lookup"><span data-stu-id="450bb-127">Create network regions</span></span></p></li>
<li><p><span data-ttu-id="450bb-128">Создание сайтов сети</span><span class="sxs-lookup"><span data-stu-id="450bb-128">Create network sites</span></span></p></li>
<li><p><span data-ttu-id="450bb-129">Связывает подсети с сетевыми сайтами</span><span class="sxs-lookup"><span data-stu-id="450bb-129">Associates subnets with network sites</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="450bb-130">CSVoiceAdmins</span><span class="sxs-lookup"><span data-stu-id="450bb-130">CSVoiceAdmins</span></span><br />
<span data-ttu-id="450bb-131">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="450bb-131">CsAdministrator</span></span><br />
<span data-ttu-id="450bb-132">CsServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="450bb-132">CsServerAdministrator</span></span></p></td>
<td><p><span data-ttu-id="450bb-133">Сетевые регионы, сайты и подсети</span><span class="sxs-lookup"><span data-stu-id="450bb-133">About Network Regions, Sites, and Subnets</span></span><br />
<span data-ttu-id="450bb-134">Создание и изменение сетевого региона</span><span class="sxs-lookup"><span data-stu-id="450bb-134">Create or Modify a Network Region</span></span><br />
<span data-ttu-id="450bb-135">Создание или изменение сетевого сайта</span><span class="sxs-lookup"><span data-stu-id="450bb-135">Create or Modify a Network Site</span></span><br />
<span data-ttu-id="450bb-136">Связывание подсети с сетевым сайтом</span><span class="sxs-lookup"><span data-stu-id="450bb-136">Associate a Subnet with a Network Site</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="450bb-137">Настройка маршрутизации Location-Based</span><span class="sxs-lookup"><span data-stu-id="450bb-137">Configure Location-Based Routing</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="450bb-138">Создание политик голосовой маршрутизации</span><span class="sxs-lookup"><span data-stu-id="450bb-138">Create voice routing policies</span></span></p></li>
<li><p><span data-ttu-id="450bb-139">Определение отдельной конфигурации магистрали для каждой магистрали</span><span class="sxs-lookup"><span data-stu-id="450bb-139">Define separate trunk configuration per trunk</span></span></p></li>
<li><p><span data-ttu-id="450bb-140">Изменение политик голосовой связи</span><span class="sxs-lookup"><span data-stu-id="450bb-140">Modify voice policies</span></span></p></li>
<li><p><span data-ttu-id="450bb-141">Включение конфигурации маршрутизации Location-Based</span><span class="sxs-lookup"><span data-stu-id="450bb-141">Enable Location-Based Routing configuration</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="450bb-142">CSVoiceAdmins</span><span class="sxs-lookup"><span data-stu-id="450bb-142">CSVoiceAdmins</span></span><br />
<span data-ttu-id="450bb-143">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="450bb-143">CsAdministrator</span></span><br />
<span data-ttu-id="450bb-144">CsServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="450bb-144">CsServerAdministrator</span></span></p></td>
<td></td>
</tr>
</tbody>
</table>


<div>

## <a name="sample-deployment"></a><span data-ttu-id="450bb-145">Пример развертывания</span><span class="sxs-lookup"><span data-stu-id="450bb-145">Sample Deployment</span></span>

<span data-ttu-id="450bb-146">Для иллюстрации последующих механизмов, включенных Location-Based маршрутизации, используется следующее развертывание.</span><span class="sxs-lookup"><span data-stu-id="450bb-146">The following deployment is used to illustrate further the mechanisms enabled by Location-Based Routing.</span></span>

<span data-ttu-id="450bb-147">![e1bd2230-44da-4784-b359-24572b6ce02d](images/JJ994055.e1bd2230-44da-4784-b359-24572b6ce02d(OCS.15).png "e1bd2230-44da-4784-b359-24572b6ce02d")</span><span class="sxs-lookup"><span data-stu-id="450bb-147">![e1bd2230-44da-4784-b359-24572b6ce02d](images/JJ994055.e1bd2230-44da-4784-b359-24572b6ce02d(OCS.15).png "e1bd2230-44da-4784-b359-24572b6ce02d")</span></span>

<div>

## <a name="incoming-pstn-calls"></a><span data-ttu-id="450bb-148">Входящие звонки PSTN</span><span class="sxs-lookup"><span data-stu-id="450bb-148">Incoming PSTN calls</span></span>

<span data-ttu-id="450bb-149">Администратор может включить магистраль, определенный для маршрутизации звонков на шлюз "сайт 1", для Location-Based маршрут и связать его с сайтом 1 с шлюзом сайта 1.</span><span class="sxs-lookup"><span data-stu-id="450bb-149">An administrator can enable the trunk defined to route calls to “Site 1 Gateway” for Location-Based Routing and associate the “Site 1 Gateway” to site 1.</span></span> <span data-ttu-id="450bb-150">После того как вы включите этот флажок, звонки, направляемые через шлюз "сайт 1", будут перенаправляться только тем пользователям, которые находятся на сайте 1.</span><span class="sxs-lookup"><span data-stu-id="450bb-150">Once enabled, calls that are routed through “Site 1 Gateway“ will only be routed to users that are located in site 1.</span></span> <span data-ttu-id="450bb-151">Все звонки, находящиеся на магистральном шлюзе "сайт 1", предназначенные для пользователей на другом сайте, например "сайт 2", будут заблокированы для предотвращения бесплатных звонков по сети PSTN.</span><span class="sxs-lookup"><span data-stu-id="450bb-151">All calls routed through the “Site 1 Gateway” trunk destined to users in a different site, such as site 2 will be blocked to prevent PSTN toll bypass.</span></span>

<span data-ttu-id="450bb-152">Все входящие звонки по коммутируемой телефонной связи через шлюз сайта 1 будут разрешены только для маршрутизации конечных точек, расположенных на сайте 1.</span><span class="sxs-lookup"><span data-stu-id="450bb-152">All incoming PSTN calls through “Site 1 Gateway” will only be allowed to route to endpoints located in site 1.</span></span> <span data-ttu-id="450bb-153">Например, когда "Lync User 1" перемещается на сайт 2, все входящие звонки PSTN через шлюз сайта 1 не будут перенаправлены в конечные точки "Lync User 1", расположенные на сайте 2.</span><span class="sxs-lookup"><span data-stu-id="450bb-153">For example, when “Lync user 1” travels to site 2, all incoming PSTN calls through “Site 1 Gateway” will not be routed to “Lync user 1” endpoints located in site 2.</span></span> <span data-ttu-id="450bb-154">Одно и то же правило маршрутизации применимо, если "пользователь Lync 1" перемещается на неизвестный сетевой сайт, на котором невозможно определить расположение пользователя.</span><span class="sxs-lookup"><span data-stu-id="450bb-154">The same routing rule applies if “Lync user 1” travels to an unknown network site where the user’s location can’t be determined.</span></span>

<span data-ttu-id="450bb-155">В таблице ниже приведено краткое руководство по работе пользователей Lync User 1 в этом контексте.</span><span class="sxs-lookup"><span data-stu-id="450bb-155">The following table outlines the user experience of “Lync user 1” in this context.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="450bb-156">Конечные точки пользователей Lync 1, размещенные на сетевом сайте 1</span><span class="sxs-lookup"><span data-stu-id="450bb-156">Lync user 1 endpoints located in network site 1</span></span></th>
<th><span data-ttu-id="450bb-157">Конечные точки пользователей Lync 1, расположенные на сайте сети 2</span><span class="sxs-lookup"><span data-stu-id="450bb-157">Lync user 1 endpoints located in network site 2</span></span></th>
<th><span data-ttu-id="450bb-158">Конечные точки пользователей Lync 1, расположенные на неизвестном сетевом сайте</span><span class="sxs-lookup"><span data-stu-id="450bb-158">Lync user 1 endpoints located in unknown network site</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="450bb-159">Входящие звонки PSTN в Lync User 1</span><span class="sxs-lookup"><span data-stu-id="450bb-159">Inbound PSTN calls to Lync user 1</span></span></p></td>
<td><p><span data-ttu-id="450bb-160">Звонки направляются в конечные точки в этом расположении</span><span class="sxs-lookup"><span data-stu-id="450bb-160">Calls are routed to endpoints in this location</span></span></p></td>
<td><p><span data-ttu-id="450bb-161">Звонки не передаются в конечные точки в этом расположении</span><span class="sxs-lookup"><span data-stu-id="450bb-161">Calls are not routed to endpoints in this location</span></span></p></td>
<td><p><span data-ttu-id="450bb-162">Звонки не передаются в конечные точки в этом расположении</span><span class="sxs-lookup"><span data-stu-id="450bb-162">Calls are not routed to endpoints in this location</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="outgoing-pstn-calls"></a><span data-ttu-id="450bb-163">Исходящие звонки PSTN</span><span class="sxs-lookup"><span data-stu-id="450bb-163">Outgoing PSTN calls</span></span>

<span data-ttu-id="450bb-164">На голосовые маршруты указываются и политики голосовой связи, назначенные пользователям, и политики маршрутизации голосовой связи, назначенные сетевым сайтам.</span><span class="sxs-lookup"><span data-stu-id="450bb-164">Voice routes are referenced in both Voice Policies assigned directly to users, and Voice Routing Policies assigned to network sites.</span></span> <span data-ttu-id="450bb-165">Обе политики содержат ссылки на маршруты, которые можно использовать для того, чтобы направлять звонок другим образом.</span><span class="sxs-lookup"><span data-stu-id="450bb-165">Both policies contain references to routes, which can be used to route a call differently.</span></span> <span data-ttu-id="450bb-166">Например, администратор может настроить политику маршрутизации голосовой связи для всех пользователей, расположенных на сайте сети 1, для маршрутизации всех исходящих вызовов через шлюз сайта 1, в то время как политика голосовой связи для некоторых пользователей определяет маршрут для всех исходящих звонков с помощью шлюза сайта 2.</span><span class="sxs-lookup"><span data-stu-id="450bb-166">For example, an administrator can define a Voice Routing Policy for all users located in network site 1 to route all outbound calls through the “Site 1 Gateway” while the Voice Policy of some users define a route for all outbound calls through the “Site 2 Gateway”.</span></span> <span data-ttu-id="450bb-167">Несмотря на то что эти пользователи находятся в сетевом сайте 1, исходящие звонки будут маршрутизироваться через шлюз сайта 1.</span><span class="sxs-lookup"><span data-stu-id="450bb-167">While these users are located in network site 1, their outbound calls will be routed through the “Site 1 Gateway”.</span></span>

<span data-ttu-id="450bb-168">Когда пользователь находится на сетевом сайте, настроенном для маршрутизации Location-Based, маршрут политики голосовой связи на сетевом сайте переопределяет маршрут политики голосовой связи пользователя.</span><span class="sxs-lookup"><span data-stu-id="450bb-168">When a user is located in a network site configured for Location-Based Routing, the network site’s Voice Routing Policy route overrides the user’s Voice Policy route.</span></span> <span data-ttu-id="450bb-169">Это правило особенно удобно для пользователей, которые временно перемещаются на другой сайт.</span><span class="sxs-lookup"><span data-stu-id="450bb-169">This rule is particularly useful for users that temporarily move to a different site.</span></span> <span data-ttu-id="450bb-170">В этом конкретном случае пользователь всегда будет использовать локальный шлюз для своего местоположения; Если "Lync User 3" находится на сайте 2, все его исходящие звонки будут маршрутизироваться через шлюз сайта 2, но если он перейдет на сайт 1, все входящие звонки, помещенные на сайт 1, будут маршрутизироваться через шлюз "сайт 1".</span><span class="sxs-lookup"><span data-stu-id="450bb-170">In this particular case a user will always use a gateway that is local to his location; if “Lync user 3” is located at “Site 2”, all his outbound calls will be routed via “Site 2 Gateway”, but if he travels to site 1, all his outbound calls placed while he’s at site 1 will be routed through “Site 1 Gateway”.</span></span>

<span data-ttu-id="450bb-171">В таблице ниже показано, как пользователь Lync 1 помещает исходящий звонок на следующие сайты сети.</span><span class="sxs-lookup"><span data-stu-id="450bb-171">The following table illustrates the user experience of Lync user 1 placing an outbound call from the following network sites.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="450bb-172">Сетевой сайт 1</span><span class="sxs-lookup"><span data-stu-id="450bb-172">Network site 1</span></span></th>
<th><span data-ttu-id="450bb-173">Сетевой сайт 2</span><span class="sxs-lookup"><span data-stu-id="450bb-173">Network site 2</span></span></th>
<th><span data-ttu-id="450bb-174">Неизвестный сетевой сайт или недоступен для маршрутизации Location-Based</span><span class="sxs-lookup"><span data-stu-id="450bb-174">Unknown network site or not enabled for Location-Based Routing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="450bb-175">Авторизация исходящих звонков</span><span class="sxs-lookup"><span data-stu-id="450bb-175">Authorization of outbound calls</span></span></p></td>
<td><p><span data-ttu-id="450bb-176">Политика голосовой связи пользователя Lync 1</span><span class="sxs-lookup"><span data-stu-id="450bb-176">Lync user 1 voice policy</span></span></p></td>
<td><p><span data-ttu-id="450bb-177">Политика голосовой связи пользователя Lync 1</span><span class="sxs-lookup"><span data-stu-id="450bb-177">Lync user 1 voice policy</span></span></p></td>
<td><p><span data-ttu-id="450bb-178">Политика голосовой связи пользователя Lync 1</span><span class="sxs-lookup"><span data-stu-id="450bb-178">Lync user 1 voice policy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="450bb-179">Маршрутизация исходящих звонков</span><span class="sxs-lookup"><span data-stu-id="450bb-179">Routing of outbound calls</span></span></p></td>
<td><p><span data-ttu-id="450bb-180">Политика маршрутизации голосовой связи для сайта 1</span><span class="sxs-lookup"><span data-stu-id="450bb-180">Site 1 voice routing policy</span></span></p></td>
<td><p><span data-ttu-id="450bb-181">Политика маршрутизации голосовой связи на сайте 2</span><span class="sxs-lookup"><span data-stu-id="450bb-181">Site 2 voice routing policy</span></span></p></td>
<td><p><span data-ttu-id="450bb-182">Голосовая политика пользователя и только системы, не включенные для маршрутизации Location-Based</span><span class="sxs-lookup"><span data-stu-id="450bb-182">User’s voice policy and only to systems not enabled for Location-Based Routing</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="call-transfers-and-forwards"></a><span data-ttu-id="450bb-183">Передача и переадресация звонков</span><span class="sxs-lookup"><span data-stu-id="450bb-183">Call transfers and forwards</span></span>

<span data-ttu-id="450bb-184">При переносе или пересылке звонка на него влияет маршрутизация на звонки Location-Based.</span><span class="sxs-lookup"><span data-stu-id="450bb-184">When calls are transferred or forwarded, the routing of calls is affected by Location-Based Routing.</span></span>

<span data-ttu-id="450bb-185">В приведенной ниже таблице показано, как пользователь Lync 1 передает или перенаправляет Звонок на другой пользователь Lync.</span><span class="sxs-lookup"><span data-stu-id="450bb-185">The following table depicts Lync user 1 transferring or forwarding a PSTN call to another Lync user.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="450bb-186">Передача или пересылка звонка пользователем</span><span class="sxs-lookup"><span data-stu-id="450bb-186">User initiating call transfer or forward</span></span></th>
<th><span data-ttu-id="450bb-187">Пользователь Lync 2</span><span class="sxs-lookup"><span data-stu-id="450bb-187">Lync user 2</span></span></th>
<th><span data-ttu-id="450bb-188">Пользователь Lync 4</span><span class="sxs-lookup"><span data-stu-id="450bb-188">Lync user 4</span></span></th>
<th><span data-ttu-id="450bb-189">Пользователь Lync на сетевом сайте не включен для маршрутизации Location-Based</span><span class="sxs-lookup"><span data-stu-id="450bb-189">Lync user in network site not enabled for Location-Based Routing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="450bb-190">Пользователь Lync 1</span><span class="sxs-lookup"><span data-stu-id="450bb-190">Lync user 1</span></span></p></td>
<td><p><span data-ttu-id="450bb-191">Переключение или переадресация звонка разрешены</span><span class="sxs-lookup"><span data-stu-id="450bb-191">Call forward or transfer is allowed</span></span></p></td>
<td><p><span data-ttu-id="450bb-192">Переключение или переадресация звонка не разрешены</span><span class="sxs-lookup"><span data-stu-id="450bb-192">Call forward or transfer is not allowed</span></span></p></td>
<td><p><span data-ttu-id="450bb-193">Переключение или переадресация звонка не разрешены</span><span class="sxs-lookup"><span data-stu-id="450bb-193">Call forward or transfer is not allowed</span></span></p></td>
</tr>
</tbody>
</table>

  
<span data-ttu-id="450bb-194">В следующей таблице показано, как маршрутизация Location-Based влияет на маршрутизацию звонка в зависимости от расположения перемещаемого пользователя Lync (Lync User 2, Lync User 4 и т. д.) в конечную точку PSTN</span><span class="sxs-lookup"><span data-stu-id="450bb-194">The following table illustrates how Location-Based Routing affects how the call is routed based on the location of the Lync user being transferred (Lync user 2, Lync user 4, etc) to a PSTN endpoint</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="450bb-195">Конечная точка, в которую передается или пересылается Звонок</span><span class="sxs-lookup"><span data-stu-id="450bb-195">Endpoint where call is transferred or forwarded to</span></span></th>
<th><span data-ttu-id="450bb-196">Пользователь Lync 2</span><span class="sxs-lookup"><span data-stu-id="450bb-196">Lync user 2</span></span></th>
<th><span data-ttu-id="450bb-197">Пользователь Lync 4</span><span class="sxs-lookup"><span data-stu-id="450bb-197">Lync user 4</span></span></th>
<th><span data-ttu-id="450bb-198">Пользователь Lync на сетевом сайте не включен для маршрутизации Location-Based</span><span class="sxs-lookup"><span data-stu-id="450bb-198">Lync user in network site not enabled for Location-Based Routing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="450bb-199">Конечная точка ТСОП</span><span class="sxs-lookup"><span data-stu-id="450bb-199">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="450bb-200">Переадресация и пересылка звонков осуществляется с помощью политики маршрутизации голосовой связи сайта 1 и выхода через шлюз сайта 1</span><span class="sxs-lookup"><span data-stu-id="450bb-200">Call forward or transfer is routed through site 1 voice routing policy and egress via Site 1 Gateway</span></span></p></td>
<td><p><span data-ttu-id="450bb-201">Переадресация и пересылка звонков осуществляется с помощью политики маршрутизации голосовой связи сайта 2 и выхода через шлюз сайта 2</span><span class="sxs-lookup"><span data-stu-id="450bb-201">Call forward or transfer is routed through site 2 voice routing policy and egress via Site 2 Gateway</span></span></p></td>
<td><p><span data-ttu-id="450bb-202">Переадресация звонков или передача данных осуществляется посредством политики голосовой связи пользователя Lync и выхода через шлюз, не включенный для маршрутизации на основе местоположения (если она доступна).</span><span class="sxs-lookup"><span data-stu-id="450bb-202">Call forward or transfer is routed through the Lync user voice policy and egress via a gateway not enabled for location-based routing (if available)</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="simultaneous-ringing"></a><span data-ttu-id="450bb-203">Одновременный звонок</span><span class="sxs-lookup"><span data-stu-id="450bb-203">Simultaneous ringing</span></span>

<span data-ttu-id="450bb-204">После настройки маршрутизации на основе местоположения в образце топологии применяются следующие взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="450bb-204">Once location-based routing is configured in the sample topology, the following interactions are enforced.</span></span>

<span data-ttu-id="450bb-205">В следующей таблице показано, поддерживает ли маршрутизацию Location-Based одновременные звонки для разных пользователей Lync (например, пользователи Lync 2, Lync User и т. д.).</span><span class="sxs-lookup"><span data-stu-id="450bb-205">The following table illustrates whether Location-Based Routing allows simultaneous ringing for different Lync users (i.e. Lync user 2, Lync user 4, etc).</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="450bb-206">Нацеливание на входящий звонок по КОММУТИРУЕМой сети</span><span class="sxs-lookup"><span data-stu-id="450bb-206">Incoming PSTN call target</span></span></th>
<th><span data-ttu-id="450bb-207">Пользователь Lync 2</span><span class="sxs-lookup"><span data-stu-id="450bb-207">Lync user 2</span></span></th>
<th><span data-ttu-id="450bb-208">Пользователь Lync 4</span><span class="sxs-lookup"><span data-stu-id="450bb-208">Lync user 4</span></span></th>
<th><span data-ttu-id="450bb-209">Пользователь Lync на сетевом сайте не включен для маршрутизации Location-Based</span><span class="sxs-lookup"><span data-stu-id="450bb-209">Lync user in network site not enabled for Location-Based Routing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="450bb-210">Пользователь Lync 1</span><span class="sxs-lookup"><span data-stu-id="450bb-210">Lync user 1</span></span></p></td>
<td><p><span data-ttu-id="450bb-211">Одновременный звонок разрешен</span><span class="sxs-lookup"><span data-stu-id="450bb-211">Simultaneous ring is allowed</span></span></p></td>
<td><p><span data-ttu-id="450bb-212">Одновременный звонок не разрешен</span><span class="sxs-lookup"><span data-stu-id="450bb-212">Simultaneous ring is not allowed</span></span></p></td>
<td><p><span data-ttu-id="450bb-213">Одновременный звонок не разрешен</span><span class="sxs-lookup"><span data-stu-id="450bb-213">Simultaneous ring is not allowed</span></span></p></td>
</tr>
</tbody>
</table>

  
<span data-ttu-id="450bb-214">В следующей таблице показано, разрешено ли Location-Based маршрутизации Одновременный звонок в конечную точку PSTN из различных пользователей Lync (например, пользователи Lync 2, Lync User 4 и т. д.).</span><span class="sxs-lookup"><span data-stu-id="450bb-214">The following table illustrates whether Location-Based Routing allows simultaneous ringing to a PSTN endpoint from different Lync users (i.e. Lync user 2, Lync user 4, etc).</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="450bb-215">Цель одновременного вызова</span><span class="sxs-lookup"><span data-stu-id="450bb-215">Simultaneous ring target</span></span></th>
<th><span data-ttu-id="450bb-216">Пользователь Lync 2</span><span class="sxs-lookup"><span data-stu-id="450bb-216">Lync user 2</span></span></th>
<th><span data-ttu-id="450bb-217">Пользователь Lync 4</span><span class="sxs-lookup"><span data-stu-id="450bb-217">Lync user 4</span></span></th>
<th><span data-ttu-id="450bb-218">Пользователь Lync на сетевом сайте не включен для маршрутизации Location-Based</span><span class="sxs-lookup"><span data-stu-id="450bb-218">Lync user in network site not enabled for Location-Based Routing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="450bb-219">Мобильный телефон пользователя Lync 1 (конечная точка PSTN)</span><span class="sxs-lookup"><span data-stu-id="450bb-219">Lync user 1 mobile phone (PSTN endpoint)</span></span></p></td>
<td><p><span data-ttu-id="450bb-220">Вызов, направляемый по политике голосовой маршрутизации на сетевом сайте 1 и выходному каналу через шлюз сайта 1</span><span class="sxs-lookup"><span data-stu-id="450bb-220">Call routed through network site 1’s voice routing policy and egress via site 1 gateway</span></span></p></td>
<td><p><span data-ttu-id="450bb-221">Вызов, направляемый по политике голосовой маршрутизации на сетевом сайте 2 и выходному каналу через шлюз сайта 2</span><span class="sxs-lookup"><span data-stu-id="450bb-221">Call routed through network site 2’s voice routing policy and egress via site 2 gateway</span></span></p></td>
<td><p><span data-ttu-id="450bb-222">Вызов, направляемый через голосовую политику вызывающего абонента, будет исключаться через шлюз PSTN, не включенный для маршрутизации Location-Based</span><span class="sxs-lookup"><span data-stu-id="450bb-222">Call routed through the caller voice policy and will egress via a PSTN gateway not enabled for Location-Based Routing</span></span></p></td>
</tr>
</tbody>
</table>


</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="450bb-223">См. также</span><span class="sxs-lookup"><span data-stu-id="450bb-223">See Also</span></span>


[<span data-ttu-id="450bb-224">Планирование маршрутизации на основе местоположения в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="450bb-224">Planning for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-planning-for-location-based-routing.md)  
  

<span data-ttu-id="450bb-225"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="450bb-225"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

