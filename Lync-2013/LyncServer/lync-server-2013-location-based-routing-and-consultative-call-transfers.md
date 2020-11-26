---
title: 'Lync Server 2013: Location-Based Маршрутизация и consultativeные передачи звонков'
description: 'Lync Server 2013: Location-Based маршрутизации и передачи звонков consultative.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Location-Based Routing and consultative call transfers
ms:assetid: b12460c2-36c8-481f-b867-fe10dc1c0bdf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362836(v=OCS.15)
ms:contentKeyID: 56335089
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0d07cf6a33ff4d6ad57f8913a798fac3bc393a00
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426558"
---
# <a name="location-based-routing-and-consultative-call-transfers-in-lync-server-2013"></a><span data-ttu-id="f86e7-103">Location-Based маршрутизации и consultative передачи звонков в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f86e7-103">Location-Based Routing and consultative call transfers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f86e7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f86e7-104">

<span> </span></span></span>

<span data-ttu-id="f86e7-105">_**Тема последнего изменения:** 2013-07-31_</span><span class="sxs-lookup"><span data-stu-id="f86e7-105">_**Topic Last Modified:** 2013-07-31_</span></span>

<span data-ttu-id="f86e7-106">Помимо принудительного направления Location-Based в собрания Lync, приложение для конференц-связи Location-Based обеспечивает Location-Based ограничения маршрутизации для передачи вызовов consultative, которые исполняют конечные точки PSTN.</span><span class="sxs-lookup"><span data-stu-id="f86e7-106">In addition to enforcing Location-Based Routing to Lync meetings, the Location-Based Routing Conferencing application enforces Location-Based Routing restrictions on consultative call transfers that egress to PSTN endpoints.</span></span> <span data-ttu-id="f86e7-107">Переключение консультативного вызова — это вызов, установленный между двумя абонентами, в котором один из абонентов передает вызов новому абоненту.</span><span class="sxs-lookup"><span data-stu-id="f86e7-107">A consultative call transfer is a call established between two parties where one of the parties transfers the call to a new user.</span></span> <span data-ttu-id="f86e7-108">Например, конечная точка PSTN вызывает пользователя A (вызываемый Lync).</span><span class="sxs-lookup"><span data-stu-id="f86e7-108">For example, a PSTN endpoint calls user A (Lync callee).</span></span> <span data-ttu-id="f86e7-109">Пользователь а определяет, следует ли перенаправлять пользователя PSTN на пользователя B (пользователь Lync).</span><span class="sxs-lookup"><span data-stu-id="f86e7-109">User A determines the PSTN user should be forwarded to user B (Lync user).</span></span> <span data-ttu-id="f86e7-110">Абонент A переводит вызов пользователя ТСОП в режим ожидания и вызывает абонента B. Абонент B подтверждает согласие на разговор с пользователем ТСОП.</span><span class="sxs-lookup"><span data-stu-id="f86e7-110">User A places the call with the PSTN user on hold, and calls user B. User B agrees to talk to the PSTN user.</span></span> <span data-ttu-id="f86e7-111">Абонент A переключает вызов, находящийся в режиме ожидания, на абонента B.</span><span class="sxs-lookup"><span data-stu-id="f86e7-111">User A transfers the call on-hold to user B.</span></span>

<span data-ttu-id="f86e7-112">**Потоки вызовов при переключении консультативных вызовов**</span><span class="sxs-lookup"><span data-stu-id="f86e7-112">**Consultative call transfer call flow**</span></span>

<span data-ttu-id="f86e7-113">![Схема маршрутизации на основе местоположения для конференц-связи](images/Dn362836.e4d43d6f-23d2-49c9-b12b-15248a743f92(OCS.15).jpg "Схема маршрутизации на основе местоположения для конференц-связи")</span><span class="sxs-lookup"><span data-stu-id="f86e7-113">![Location-based routing for conferencing diagram](images/Dn362836.e4d43d6f-23d2-49c9-b12b-15248a743f92(OCS.15).jpg "Location-based routing for conferencing diagram")</span></span>

<span data-ttu-id="f86e7-114">Если пользователь, использующий Location-Basedную маршрутизацию, инициирует передачу вызова consultative для конечной точки PSTN (как показано на предыдущем рисунке), при этом создаются два активных звонка: один звонок между пользователем КТСОП и пользователем Lync A, а другой пользователь Lync A и Lync User B. следующие поведения принудительно применяются приложением для конференц-связи Location-Based.</span><span class="sxs-lookup"><span data-stu-id="f86e7-114">When a user enabled for Location-Based Routing initiates a consultative call transfer of a PSTN endpoint (as shown in the preceding figure), this creates two active calls, one call between the PSTN user and Lync user A, and the other between Lync user A and Lync user B. the following behavior is enforced by the Location-Based Routing Conferencing application:</span></span>

  - <span data-ttu-id="f86e7-115">Если магистральная маршрутизация SIP, на которую звонит звонок по протоколу PSTN, может перенаправить звонок на сетевой сайт, на котором находится пользователь B (например, объект передачи), будет разрешено его передача. в противном случае передача вызова consultative будет заблокирована.</span><span class="sxs-lookup"><span data-stu-id="f86e7-115">If the SIP trunk routing the PSTN call is authorized to re-route the PSTN call to the network site where Lync user B (i.e. transfer target) is located,, then the call transfer will be allowed; otherwise, the consultative call transfer will be blocked.</span></span> <span data-ttu-id="f86e7-116">Это разрешение предоставляется при условии, что расположение передаваемого абонента находится в пределах той же сети, что и магистраль SIP, по которой активный вызов направляется в конечную точку ТСОП.</span><span class="sxs-lookup"><span data-stu-id="f86e7-116">This authorization is performed based on the transferred party’s location being in the same network site as the SIP trunk that is routing the active call to the PSTN endpoint.</span></span>

  - <span data-ttu-id="f86e7-117">Если магистральная маршрутизация SIP не авторизована для маршрутизации звонков на сетевой сайт, на котором находится полученный абонент (Lync User B) или если он находится на неизвестном сетевом сайте, то передача вызова consultative в конечную точку КТСОП (например, цель передачи звонков) будет заблокирована.</span><span class="sxs-lookup"><span data-stu-id="f86e7-117">If the SIP trunk routing the inbound PSTN call is not authorized to route calls to the network site where the transferred party (Lync user B) is located or the transferred party is located in an unknown network site, then the consultative call transfer to the PSTN endpoint (i.e. call transfer target) will be blocked.</span></span>

<span data-ttu-id="f86e7-118">В следующей таблице описано, как Location-Based ограничения маршрутизации, применяемые приложением для проведения конференций Location-Based для передачи вызовов consultative.</span><span class="sxs-lookup"><span data-stu-id="f86e7-118">The following table describes how Location-Based Routing restrictions are applied by the Location-Based Routing Conferencing application for consultative call transfers.</span></span> <span data-ttu-id="f86e7-119">Хотя конечные точки УАТС не связаны напрямую с сетевым сайтом, магистрали SIP, к которой подключена УАТС, можно назначить сетевой сайт.</span><span class="sxs-lookup"><span data-stu-id="f86e7-119">Although PBX endpoints are not directly associated with a network site, the SIP trunk the PBX is connected to can be assigned a network site.</span></span> <span data-ttu-id="f86e7-120">Таким образом, конечную точку УАТС можно косвенно связать с сетевым сайтом.</span><span class="sxs-lookup"><span data-stu-id="f86e7-120">Therefore, the PBX endpoint can be indirectly associated with a network site.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f86e7-121">Сетевой сайт стороны, передавшей вызов</span><span class="sxs-lookup"><span data-stu-id="f86e7-121">Network site of call transferred party</span></span></p></td>
<td><p><span data-ttu-id="f86e7-122">Сетевой сайт целевого объекта переключения вызова</span><span class="sxs-lookup"><span data-stu-id="f86e7-122">Network site of call transfer target</span></span></p></td>
<td><p><span data-ttu-id="f86e7-123">Поведение</span><span class="sxs-lookup"><span data-stu-id="f86e7-123">Behavior</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f86e7-124">Конечная точка ТСОП</span><span class="sxs-lookup"><span data-stu-id="f86e7-124">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="f86e7-125">Пользователь Lync на сайте сети (например, 1)</span><span class="sxs-lookup"><span data-stu-id="f86e7-125">Lync user in the same network site (i.e. site 1)</span></span></p></td>
<td><p><span data-ttu-id="f86e7-126">Переключение консультативного вызова после консультации будет разрешено</span><span class="sxs-lookup"><span data-stu-id="f86e7-126">Consultative transfer will be allowed</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f86e7-127">Конечная точка ТСОП</span><span class="sxs-lookup"><span data-stu-id="f86e7-127">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="f86e7-128">Пользователь Lync на разных сетевых сайтах (то есть на сайте 2)</span><span class="sxs-lookup"><span data-stu-id="f86e7-128">Lync user in different network sites (i.e. site 2)</span></span></p></td>
<td><p><span data-ttu-id="f86e7-129">Переключение консультативного вызова после консультации будет заблокировано</span><span class="sxs-lookup"><span data-stu-id="f86e7-129">Consultative transfer will be disallowed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f86e7-130">Конечная точка ТСОП</span><span class="sxs-lookup"><span data-stu-id="f86e7-130">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="f86e7-131">Пользователь Lync на неизвестном сетевом сайте</span><span class="sxs-lookup"><span data-stu-id="f86e7-131">Lync user in an unknown network site</span></span></p></td>
<td><p><span data-ttu-id="f86e7-132">Переключение консультативного вызова после консультации будет заблокировано</span><span class="sxs-lookup"><span data-stu-id="f86e7-132">Consultative transfer will be disallowed</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f86e7-133">Конечная точка ТСОП</span><span class="sxs-lookup"><span data-stu-id="f86e7-133">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="f86e7-134">Федеративный пользователь Lync</span><span class="sxs-lookup"><span data-stu-id="f86e7-134">Federated Lync user</span></span></p></td>
<td><p><span data-ttu-id="f86e7-135">Переключение консультативного вызова после консультации будет заблокировано</span><span class="sxs-lookup"><span data-stu-id="f86e7-135">Consultative transfer will be disallowed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f86e7-136">Конечная точка ТСОП</span><span class="sxs-lookup"><span data-stu-id="f86e7-136">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="f86e7-137">Конечная точка УАТС на том же сайте (т. е. на сайте 1)</span><span class="sxs-lookup"><span data-stu-id="f86e7-137">PBX endpoint in the same site (i.e. site 1)</span></span></p></td>
<td><p><span data-ttu-id="f86e7-138">Переключение консультативного вызова после консультации будет разрешено</span><span class="sxs-lookup"><span data-stu-id="f86e7-138">Consultative transfer will be allowed</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f86e7-139">Конечная точка ТСОП</span><span class="sxs-lookup"><span data-stu-id="f86e7-139">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="f86e7-140">Конечная точка УАТС на других сайтах (т. е. на сайте 2)</span><span class="sxs-lookup"><span data-stu-id="f86e7-140">PBX endpoint in a different sites (i.e. site 2)</span></span></p></td>
<td><p><span data-ttu-id="f86e7-141">Переключение консультативного вызова после консультации будет заблокировано</span><span class="sxs-lookup"><span data-stu-id="f86e7-141">Consultative transfer will be disallowed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f86e7-142">Конечная точка УАТС на том же сайте (т. е. на сайте 1)</span><span class="sxs-lookup"><span data-stu-id="f86e7-142">PBX endpoint in the same site (i.e. site 1)</span></span></p></td>
<td><p><span data-ttu-id="f86e7-143">Конечная точка ТСОП</span><span class="sxs-lookup"><span data-stu-id="f86e7-143">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="f86e7-144">Переключение консультативного вызова после консультации будет разрешено</span><span class="sxs-lookup"><span data-stu-id="f86e7-144">Consultative transfer will be allowed</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f86e7-145">Конечная точка УАТС на другом сайте (т. е. на сайте 2)</span><span class="sxs-lookup"><span data-stu-id="f86e7-145">PBX endpoint in a different site (i.e. site 2)</span></span></p></td>
<td><p><span data-ttu-id="f86e7-146">Конечная точка ТСОП</span><span class="sxs-lookup"><span data-stu-id="f86e7-146">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="f86e7-147">Переключение консультативного вызова после консультации будет заблокировано</span><span class="sxs-lookup"><span data-stu-id="f86e7-147">Consultative transfer will be disallowed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f86e7-148">Конечная точка УАТС на любом сайте</span><span class="sxs-lookup"><span data-stu-id="f86e7-148">PBX endpoint in any site</span></span></p></td>
<td><p><span data-ttu-id="f86e7-149">Пользователь Lync на сайте сети (например, 1)</span><span class="sxs-lookup"><span data-stu-id="f86e7-149">Lync user in the same network site (i.e. site 1)</span></span></p></td>
<td><p><span data-ttu-id="f86e7-150">Переключение консультативного вызова после консультации будет разрешено</span><span class="sxs-lookup"><span data-stu-id="f86e7-150">Consultative transfer will be allowed</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f86e7-151">Конечная точка УАТС на любом сайте</span><span class="sxs-lookup"><span data-stu-id="f86e7-151">PBX endpoint in any site</span></span></p></td>
<td><p><span data-ttu-id="f86e7-152">Пользователь Lync на разных сетевых сайтах (то есть на сайте 2)</span><span class="sxs-lookup"><span data-stu-id="f86e7-152">Lync user in different network sites (i.e. site 2)</span></span></p></td>
<td><p><span data-ttu-id="f86e7-153">Переключение консультативного вызова после консультации будет разрешено</span><span class="sxs-lookup"><span data-stu-id="f86e7-153">Consultative transfer will be allowed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f86e7-154">Конечная точка УАТС на любом сайте</span><span class="sxs-lookup"><span data-stu-id="f86e7-154">PBX endpoint in any site</span></span></p></td>
<td><p><span data-ttu-id="f86e7-155">Пользователь Lync на неизвестном сетевом сайте</span><span class="sxs-lookup"><span data-stu-id="f86e7-155">Lync user in an unknown network site</span></span></p></td>
<td><p><span data-ttu-id="f86e7-156">Переключение консультативного вызова после консультации будет разрешено</span><span class="sxs-lookup"><span data-stu-id="f86e7-156">Consultative transfer will be allowed</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f86e7-157">Конечная точка УАТС на любом сайте</span><span class="sxs-lookup"><span data-stu-id="f86e7-157">PBX endpoint in any site</span></span></p></td>
<td><p><span data-ttu-id="f86e7-158">Федеративный пользователь Lync</span><span class="sxs-lookup"><span data-stu-id="f86e7-158">Federated Lync user</span></span></p></td>
<td><p><span data-ttu-id="f86e7-159">Переключение консультативного вызова после консультации будет разрешено</span><span class="sxs-lookup"><span data-stu-id="f86e7-159">Consultative transfer will be allowed</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="f86e7-160">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f86e7-160">


</div>

<span> </span>

</div>

</div>

</span></span></div>

