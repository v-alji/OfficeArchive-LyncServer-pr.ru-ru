---
title: 'Lync Server 2013: поддержка маршрутизации на основе расположения клиентами и серверами'
description: 'Lync Server 2013: Поддержка клиента и сервера для маршрутизации Location-Based.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Client and server support for Location-Based Routing
ms:assetid: 26c2ca3d-026d-4dd7-94fa-15ebb4406953
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994024(v=OCS.15)
ms:contentKeyID: 51803933
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 20dca7444f58ee62dbc36edbb7d9e1c976a97807
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434902"
---
# <a name="client-and-server-support-for-location-based-routing-in-lync-server-2013"></a><span data-ttu-id="855c6-103">Поддержка маршрутизации на основе расположения клиентами и серверами в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="855c6-103">Client and server support for Location-Based Routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="855c6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="855c6-104">

<span> </span></span></span>

<span data-ttu-id="855c6-105">_**Тема последнего изменения:** 2013-06-18_</span><span class="sxs-lookup"><span data-stu-id="855c6-105">_**Topic Last Modified:** 2013-06-18_</span></span>

<span data-ttu-id="855c6-106">Location-Based маршрутизация обеспечивается приложением Lync Server.</span><span class="sxs-lookup"><span data-stu-id="855c6-106">Location-Based Routing is enforced by Lync Server.</span></span> <span data-ttu-id="855c6-107">Lync Server может определять сетевые сайты, в которых пользователи подключаются из корпоративной сети.</span><span class="sxs-lookup"><span data-stu-id="855c6-107">Lync Server can identify the network sites where users are connecting from within the corporate network.</span></span> <span data-ttu-id="855c6-108">Расположение удаленных пользователей считается неизвестным, поскольку они находятся вне корпоративной сети.</span><span class="sxs-lookup"><span data-stu-id="855c6-108">Since remote users are outside the corporate network, their location is considered to be unknown.</span></span>

<div>

## <a name="lync-server-support"></a><span data-ttu-id="855c6-109">Поддержка Lync Server</span><span class="sxs-lookup"><span data-stu-id="855c6-109">Lync Server Support</span></span>

<span data-ttu-id="855c6-110">Для маршрутизации Location-Based требуется, чтобы Lync Server 2013 CU1 развернут на всех пулах интерфейсных и стандартных серверах в заданной топологии.</span><span class="sxs-lookup"><span data-stu-id="855c6-110">Location-Based Routing requires that Lync Server 2013 CU1 is deployed on all Front End pools and Standard Edition servers in a given topology.</span></span> <span data-ttu-id="855c6-111">Если Lync Server 2013 CU1 не установлен в некоторых компонентах Lync в топологии, Location-Based ограничения маршрутизации не могут быть полностью применены.</span><span class="sxs-lookup"><span data-stu-id="855c6-111">If Lync Server 2013 CU1 is not installed on certain Lync components in the topology, Location-Based Routing restrictions cannot be fully enforced.</span></span>

<span data-ttu-id="855c6-112">В следующей таблице указаны комбинации ролей сервера и версий, которые поддерживаются для маршрутизации Location-Based.</span><span class="sxs-lookup"><span data-stu-id="855c6-112">The following table identifies the combination of server roles and versions that is supported for Location-Based Routing.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="855c6-113">Версия пула</span><span class="sxs-lookup"><span data-stu-id="855c6-113">Pool version</span></span></th>
<th><span data-ttu-id="855c6-114">Версия cервера-посредника</span><span class="sxs-lookup"><span data-stu-id="855c6-114">Mediation Server version</span></span></th>
<th><span data-ttu-id="855c6-115">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="855c6-115">Supported</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="855c6-116">Накопительное обновление для Lync Server 2013 за Февраль 2013</span><span class="sxs-lookup"><span data-stu-id="855c6-116">Lync Server 2013 February 2013 Cumulative Update</span></span></p></td>
<td><p><span data-ttu-id="855c6-117">Накопительное обновление для Lync Server 2013 за Февраль 2013</span><span class="sxs-lookup"><span data-stu-id="855c6-117">Lync Server 2013 February 2013 Cumulative Update</span></span></p></td>
<td><p><span data-ttu-id="855c6-118">Да</span><span class="sxs-lookup"><span data-stu-id="855c6-118">yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="855c6-119">Накопительное обновление для Lync Server 2013 за Февраль 2013</span><span class="sxs-lookup"><span data-stu-id="855c6-119">Lync Server 2013 February 2013 Cumulative Update</span></span></p></td>
<td><p><span data-ttu-id="855c6-120">Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="855c6-120">Lync Server 2013</span></span></p></td>
<td><p><span data-ttu-id="855c6-121">нет</span><span class="sxs-lookup"><span data-stu-id="855c6-121">no</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="855c6-122">Накопительное обновление для Lync Server 2013 за Февраль 2013</span><span class="sxs-lookup"><span data-stu-id="855c6-122">Lync Server 2013 February 2013 Cumulative Update</span></span></p></td>
<td><p><span data-ttu-id="855c6-123">Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="855c6-123">Lync Server 2010</span></span></p></td>
<td><p><span data-ttu-id="855c6-124">нет</span><span class="sxs-lookup"><span data-stu-id="855c6-124">no</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="855c6-125">Накопительное обновление для Lync Server 2013 за Февраль 2013</span><span class="sxs-lookup"><span data-stu-id="855c6-125">Lync Server 2013 February 2013 Cumulative Update</span></span></p></td>
<td><p><span data-ttu-id="855c6-126">Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="855c6-126">Office Communications Server 2007 R2</span></span></p></td>
<td><p><span data-ttu-id="855c6-127">нет</span><span class="sxs-lookup"><span data-stu-id="855c6-127">no</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="855c6-128">Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="855c6-128">Lync Server 2013</span></span></p></td>
<td><p><span data-ttu-id="855c6-129">любая</span><span class="sxs-lookup"><span data-stu-id="855c6-129">any</span></span></p></td>
<td><p><span data-ttu-id="855c6-130">нет</span><span class="sxs-lookup"><span data-stu-id="855c6-130">no</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="855c6-131">Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="855c6-131">Lync Server 2010</span></span></p></td>
<td><p><span data-ttu-id="855c6-132">любая</span><span class="sxs-lookup"><span data-stu-id="855c6-132">any</span></span></p></td>
<td><p><span data-ttu-id="855c6-133">нет</span><span class="sxs-lookup"><span data-stu-id="855c6-133">no</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="855c6-134">Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="855c6-134">Office Communications Server 2007 R2</span></span></p></td>
<td><p><span data-ttu-id="855c6-135">любая</span><span class="sxs-lookup"><span data-stu-id="855c6-135">any</span></span></p></td>
<td><p><span data-ttu-id="855c6-136">нет</span><span class="sxs-lookup"><span data-stu-id="855c6-136">no</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="lync-client-support"></a><span data-ttu-id="855c6-137">Поддержка клиента Lync</span><span class="sxs-lookup"><span data-stu-id="855c6-137">Lync Client Support</span></span>

<span data-ttu-id="855c6-138">В следующей таблице указаны клиенты, которые Location-Based поддерживаются службой маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="855c6-138">The following table identifies the clients that Location-Based Routing supports.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="855c6-139">Тип клиента</span><span class="sxs-lookup"><span data-stu-id="855c6-139">Client type</span></span></th>
<th><span data-ttu-id="855c6-140">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="855c6-140">Supported</span></span></th>
<th><span data-ttu-id="855c6-141">Сведения</span><span class="sxs-lookup"><span data-stu-id="855c6-141">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="855c6-142">Lync 2013</span><span class="sxs-lookup"><span data-stu-id="855c6-142">Lync 2013</span></span></p></td>
<td><p><span data-ttu-id="855c6-143">Да</span><span class="sxs-lookup"><span data-stu-id="855c6-143">yes</span></span></p></td>
<td><p><span data-ttu-id="855c6-144">В том числе накопительное обновление для Lync 2013 за Февраль 2013</span><span class="sxs-lookup"><span data-stu-id="855c6-144">Including Lync 2013 February 2013 Cumulative Update</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="855c6-145">Lync 2010</span><span class="sxs-lookup"><span data-stu-id="855c6-145">Lync 2010</span></span></p></td>
<td><p><span data-ttu-id="855c6-146">Да</span><span class="sxs-lookup"><span data-stu-id="855c6-146">yes</span></span></p></td>
<td> </td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="855c6-147">Office Communicator 2007 R2</span><span class="sxs-lookup"><span data-stu-id="855c6-147">Office Communicator 2007 R2</span></span></p></td>
<td><p><span data-ttu-id="855c6-148">нет</span><span class="sxs-lookup"><span data-stu-id="855c6-148">no</span></span></p></td>
<td> </td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="855c6-149">Lync Phone Edition</span><span class="sxs-lookup"><span data-stu-id="855c6-149">Lync Phone Edition</span></span></p></td>
<td><p><span data-ttu-id="855c6-150">Да</span><span class="sxs-lookup"><span data-stu-id="855c6-150">yes</span></span></p></td>
<td> </td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="855c6-151">Lync Attendant</span><span class="sxs-lookup"><span data-stu-id="855c6-151">Lync Attendant</span></span></p></td>
<td><p><span data-ttu-id="855c6-152">Да</span><span class="sxs-lookup"><span data-stu-id="855c6-152">yes</span></span></p></td>
<td> </td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="855c6-153">Lync для Windows 8</span><span class="sxs-lookup"><span data-stu-id="855c6-153">Lync for Windows 8</span></span></p></td>
<td><p><span data-ttu-id="855c6-154">нет</span><span class="sxs-lookup"><span data-stu-id="855c6-154">no</span></span></p></td>
<td> </td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="855c6-155">Lync Mobile 2013</span><span class="sxs-lookup"><span data-stu-id="855c6-155">Lync Mobile 2013</span></span></p></td>
<td><p><span data-ttu-id="855c6-156">нет</span><span class="sxs-lookup"><span data-stu-id="855c6-156">no</span></span></p></td>
<td><p><span data-ttu-id="855c6-157">Для клиентов Lync Mobile 2013 необходимо отключить VoIP, если они используются пользователями, в которых включена маршрутизация Location-Based.</span><span class="sxs-lookup"><span data-stu-id="855c6-157">VoIP must be disabled for Lync Mobile 2013 clients if used by users with Location-Based Routing enabled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="855c6-158">Lync Mobile 2010</span><span class="sxs-lookup"><span data-stu-id="855c6-158">Lync Mobile 2010</span></span></p></td>
<td><p><span data-ttu-id="855c6-159">Да</span><span class="sxs-lookup"><span data-stu-id="855c6-159">yes</span></span></p></td>
<td> </td>
</tr>
</tbody>
</table>

  

<div>


> [!NOTE]  
> <span data-ttu-id="855c6-160">Чтобы отключить VoIP для клиентов Lync Mobile 2013, назначьте политику мобильности с параметром, IP аудио-и видеофайлы, отключенными для всех пользователей, для которых включена маршрутизация на основе местоположения.</span><span class="sxs-lookup"><span data-stu-id="855c6-160">To disable VoIP for Lync Mobile 2013 clients, assign a mobility policy with the setting, IP Audio/Video, disabled for all users enabled for Location Based Routing.</span></span> <span data-ttu-id="855c6-161">Более подробно о политике мобильности см. в разделе <A href="https://docs.microsoft.com/powershell/module/skype/New-CsMobilityPolicy">New-CsMobilityPolicy</A>.</span><span class="sxs-lookup"><span data-stu-id="855c6-161">For more details about mobility policy, see <A href="https://docs.microsoft.com/powershell/module/skype/New-CsMobilityPolicy">New-CsMobilityPolicy</A>.</span></span>



</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="855c6-162">См. также</span><span class="sxs-lookup"><span data-stu-id="855c6-162">See Also</span></span>


[<span data-ttu-id="855c6-163">Планирование маршрутизации на основе местоположения в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="855c6-163">Planning for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-planning-for-location-based-routing.md)  
  

<span data-ttu-id="855c6-164"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="855c6-164"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

