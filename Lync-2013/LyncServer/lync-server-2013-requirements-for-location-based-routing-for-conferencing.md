---
title: 'Lync Server 2013: требования для маршрутизации Location-Based для конференц-связи'
description: 'Lync Server 2013: требования для маршрутизации Location-Based для конференц-связи.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Requirements for Location-Based Routing for conferencing
ms:assetid: 766d9286-2c34-4faf-bb3e-f0ca478a70cf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362806(v=OCS.15)
ms:contentKeyID: 56335085
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fbaa1af2690c3148d2ecfb173b13be288a21d80f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442665"
---
# <a name="requirements-for-location-based-routing-for-conferencing-in-lync-server-2013"></a><span data-ttu-id="c8ac8-103">Требования для маршрутизации Location-Based для конференц-связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c8ac8-103">Requirements for Location-Based Routing for conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c8ac8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c8ac8-104">

<span> </span></span></span>

<span data-ttu-id="c8ac8-105">_**Тема последнего изменения:** 2013-07-19_</span><span class="sxs-lookup"><span data-stu-id="c8ac8-105">_**Topic Last Modified:** 2013-07-19_</span></span>

<span data-ttu-id="c8ac8-106">Ниже приведены требования, необходимые для установки и настройки приложения для конференц-связи Location-Based.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-106">The following are the requirements needed for the installation and configuration of the Location-Based Routing Conferencing application:</span></span>

  - <span data-ttu-id="c8ac8-107">Для Lync Server 2013 накопительный пакет обновления 2 должен быть развернут на всех серверах или пулах в вашей топологии.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-107">Lync Server 2013 Cumulative Update 2 must be deployed on all servers or pools in your topology.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="c8ac8-108">Если на сервере Lync или в пуле в топологии не установлен Lync Server 2013 накопительный пакет обновления 2 или более новой версии, принудительное использование Location-Based маршрутизации собраний Lync не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-108">If a Lync server or pool in your topology does not have Lync Server 2013 Cumulative Update 2 or higher installed, then enforcement of Location-Based Routing of Lync meetings cannot be guaranteed.</span></span>



</div>

  - <span data-ttu-id="c8ac8-109">Lync Server 2013 Location-Based Routing является предварительным требованием для приложения для проведения конференций в Location-Based маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-109">Lync Server 2013 Location-Based Routing is a pre-requisite for Location-Based Routing Conferencing application.</span></span> <span data-ttu-id="c8ac8-110">Дополнительные сведения о настройке маршрутизации [Location-Based](lync-server-2013-configuring-location-based-routing.md)для Lync Server 2013 Location-Based см.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-110">For further information on configuring Lync Server 2013 Location-Based Routing, please refer to [Configuring Location-Based Routing](lync-server-2013-configuring-location-based-routing.md).</span></span>

  - <span data-ttu-id="c8ac8-111">Требования к приложению для конференц-связи Location-Based, такие же, как и в Lync Server 2013 Location-Based Routing.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-111">Requirements of Location-Based Routing Conferencing application are the same as the requirements for Lync Server 2013 Location-Based Routing.</span></span> <span data-ttu-id="c8ac8-112">Дополнительные сведения можно найти в разделе [планирование Location-Based маршрутизации](lync-server-2013-planning-for-location-based-routing.md).</span><span class="sxs-lookup"><span data-stu-id="c8ac8-112">For more information, please refer to [Planning for Location-Based Routing](lync-server-2013-planning-for-location-based-routing.md).</span></span>

<div>

## <a name="supported-servers"></a><span data-ttu-id="c8ac8-113">Поддерживаемые серверы</span><span class="sxs-lookup"><span data-stu-id="c8ac8-113">Supported Servers</span></span>

<span data-ttu-id="c8ac8-114">Для работы приложения для конференц-связи Location-Based требуется, чтобы Lync Server 2013 накопительный пакет обновления 2 развернут на всех пулах Front-End и серверах стандартных выпусков в вашей топологии.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-114">The Location-Based Routing Conferencing application requires that Lync Server 2013 Cumulative Update 2 is deployed on all Front-End pools and Standard Edition Servers in your topology.</span></span> <span data-ttu-id="c8ac8-115">Если на некоторых серверах Lync в вашей топологии не установлено приложение Lync Server 2013 Location-Based, то ограничения маршрутизации не могут быть полностью применены к собраниям Lync и consultative передаче звонков.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-115">If Lync Server 2013 Cumulative Update 2 is not installed on some Lync Servers in your topology, Location-Based Routing restrictions cannot be fully enforced on Lync meetings and consultative call transfers.</span></span>

<span data-ttu-id="c8ac8-116">В таблице ниже указаны роли сервера и версии, которые поддерживают маршрутизацию Location-Based.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-116">The following table identifies the combination of server roles and versions that support Location-Based Routing.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c8ac8-117">Версия внешнего пула</span><span class="sxs-lookup"><span data-stu-id="c8ac8-117">Front-End Pool version</span></span></p></td>
<td><p><span data-ttu-id="c8ac8-118">Версия cервера-посредника</span><span class="sxs-lookup"><span data-stu-id="c8ac8-118">Mediation Server version</span></span></p></td>
<td><p><span data-ttu-id="c8ac8-119">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="c8ac8-119">Supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8ac8-120">Накопительный пакет обновления 2 для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c8ac8-120">Lync Server 2013 Cumulative Update 2</span></span></p></td>
<td><p><span data-ttu-id="c8ac8-121">Накопительный пакет обновления 2 для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c8ac8-121">Lync Server 2013 Cumulative Update 2</span></span></p></td>
<td><p><span data-ttu-id="c8ac8-122">Да</span><span class="sxs-lookup"><span data-stu-id="c8ac8-122">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8ac8-123">Накопительный пакет обновления 2 для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c8ac8-123">Lync Server 2013 Cumulative Update 2</span></span></p></td>
<td><p><span data-ttu-id="c8ac8-124">Накопительный пакет обновления 1 для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c8ac8-124">Lync Server 2013 Cumulative Update 1</span></span></p></td>
<td><p><span data-ttu-id="c8ac8-125">Нет</span><span class="sxs-lookup"><span data-stu-id="c8ac8-125">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8ac8-126">Накопительный пакет обновления 2 для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c8ac8-126">Lync Server 2013 Cumulative Update 2</span></span></p></td>
<td><p><span data-ttu-id="c8ac8-127">Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="c8ac8-127">Lync Server 2010</span></span></p></td>
<td><p><span data-ttu-id="c8ac8-128">Нет</span><span class="sxs-lookup"><span data-stu-id="c8ac8-128">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8ac8-129">Накопительный пакет обновления 2 для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c8ac8-129">Lync Server 2013 Cumulative Update 2</span></span></p></td>
<td><p><span data-ttu-id="c8ac8-130">Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="c8ac8-130">Office Communications Server 2007 R2</span></span></p></td>
<td><p><span data-ttu-id="c8ac8-131">Нет</span><span class="sxs-lookup"><span data-stu-id="c8ac8-131">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8ac8-132">Накопительный пакет обновления 1 для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c8ac8-132">Lync Server 2013 Cumulative Update 1</span></span></p></td>
<td><p><span data-ttu-id="c8ac8-133">Любой</span><span class="sxs-lookup"><span data-stu-id="c8ac8-133">Any</span></span></p></td>
<td><p><span data-ttu-id="c8ac8-134">Нет</span><span class="sxs-lookup"><span data-stu-id="c8ac8-134">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8ac8-135">Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="c8ac8-135">Lync Server 2010</span></span></p></td>
<td><p><span data-ttu-id="c8ac8-136">Любой</span><span class="sxs-lookup"><span data-stu-id="c8ac8-136">Any</span></span></p></td>
<td><p><span data-ttu-id="c8ac8-137">Нет</span><span class="sxs-lookup"><span data-stu-id="c8ac8-137">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8ac8-138">Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="c8ac8-138">Office Communications Server 2007 R2</span></span></p></td>
<td><p><span data-ttu-id="c8ac8-139">Любой</span><span class="sxs-lookup"><span data-stu-id="c8ac8-139">Any</span></span></p></td>
<td><p><span data-ttu-id="c8ac8-140">Нет</span><span class="sxs-lookup"><span data-stu-id="c8ac8-140">No</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="supported-clients"></a><span data-ttu-id="c8ac8-141">Поддерживаемые клиенты</span><span class="sxs-lookup"><span data-stu-id="c8ac8-141">Supported Clients</span></span>

<span data-ttu-id="c8ac8-142">Клиенты Lync, поддерживающие Location-Basedную маршрутизацию собраний Lync, — это те же клиенты, которые поддерживают маршрутизацию Lync Server 2013 Location-Based.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-142">The Lync clients that support Location-Based Routing of Lync meetings are the same clients that support Lync Server 2013 Location-Based Routing.</span></span> <span data-ttu-id="c8ac8-143">Для получения дополнительных сведений обратитесь в [службу поддержки клиентов и серверов для маршрутизации Location-Based](lync-server-2013-client-and-server-support-for-location-based-routing.md).</span><span class="sxs-lookup"><span data-stu-id="c8ac8-143">For more information, please refer to [Client and Server Support for Location-Based Routing](lync-server-2013-client-and-server-support-for-location-based-routing.md).</span></span>

</div>

<div>

## <a name="mediation-server-requirements-for-consultative-call-transfers"></a><span data-ttu-id="c8ac8-144">Требования к серверу исправлений для передачи вызовов consultative</span><span class="sxs-lookup"><span data-stu-id="c8ac8-144">Mediation Server Requirements for Consultative Call Transfers</span></span>

<span data-ttu-id="c8ac8-145">Приложение для конференц-связи Location-Based необходимо развертывать изолированные серверы, чтобы применить ограничения Location-Based маршрутизации для передачи вызовов consultative.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-145">The Location-Based Routing Conferencing application requires deploying stand-alone Mediation Servers in order to enforce Location-Based Routing restrictions on consultative call transfers.</span></span>

<span data-ttu-id="c8ac8-146">Чтобы обеспечить Location-Based маршрутизации передачи вызовов consultative, сервер-посредник должен быть связан только с одним одноранговым узлом сервера-посредником (например, УАТС, шлюзом SIP и т. д.) в сетевых регионах, где требуется Location-Based маршрутизация.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-146">To enforce Location-Based Routing of consultative call transfers, the Mediation Server must be associated with only one Mediation Server peer (i.e. PBX, SIP gateway, etc) in network regions where Location-Based Routing is required.</span></span> <span data-ttu-id="c8ac8-147">Если в одном и том же регионе развернуты одноранговые узлы сервера-посредника, то узел сервера-посредника должен быть связан с другим сервером-посредником.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-147">If additional Mediation Server peers are deployed in the same network region, the Mediation Server peer must be associated with a different Mediation Server .</span></span> <span data-ttu-id="c8ac8-148">Это требование подробно описано ниже.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-148">This Requirement is detailed as follows:</span></span>

  - <span data-ttu-id="c8ac8-149">Одноранговый сервер для одного сервера-посредника, когда передача вызова consultative перенаправляется на одноранговый сервер с несколькими магистральными серверами SIP на несколько одноранговых узлов (например, АТС и шлюзы) передача вызова consultative блокируется, чтобы предотвратить бесплатный звонок, если передача вызова consultative разрешена через некоторые магистральные магистрали SIP, но это запрещено посредством других магистральных каналов SIP.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-149">Single Mediation Server per multiple Mediation Server peers When a consultative call transfer is routed to a Mediation Server peer through a Mediation Server that’s configured with multiple SIP trunks to multiple peers (i.e. PBXs and gateways), the consultative call transfer is blocked to prevent PSTN toll bypass if the consultative call transfer is permitted through some SIP trunks but disallowed through other SIP trunks.</span></span>
    
    <span data-ttu-id="c8ac8-150">Например, в случае одного сервера-посредника, обслуживающего одноранговый сервер шлюза КТСОП и одноранговый сервер обнаружения АТС, будет проблюдаться описанное ниже поведение.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-150">For example, in the case of a single Mediation Server servicing a PSTN Gateway Mediation Server Peer and a PBX Mediation Server Peer, the following behavior will be observed:</span></span>
    
      - <span data-ttu-id="c8ac8-151">Если пользователь Lync с определенного сайта (например, сайт 1) пытается передать Звонок в конечную точку PSTN пользователю Lync из другого сайта (например, сайта 2) через consultative Transfer, Звонок будет запрещен для предотвращения бесплатных звонков по сети PSTN.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-151">When a Lync user from a given site (i.e. site 1) attempts to transfer a call with a PSTN endpoint to a Lync user from a different site (i.e. site 2) via consultative transfer, the call will be disallowed to prevent PSTN toll bypass.</span></span>
    
      - <span data-ttu-id="c8ac8-152">Если пользователь Lync с определенного сайта (например, сайт 1) пытается передать Звонок в конечную точку УАТС в том же сайте (например, на сайте 1) для пользователя Lync с другого сайта (то есть для сайта 2) через consultative Transfer, Звонок будет запрещен, даже если он не повлечет за собой потенциального бесплатного звонка.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-152">When a Lync user from a given site (i.e. site 1) attempts to transfer a call with a PBX endpoint in the same site (site 1) to a Lync user from a different site (i.e. site 2) via consultative transfer, the call will be disallowed even if it doesn’t incur in potential PSTN toll bypassing.</span></span>

  - <span data-ttu-id="c8ac8-153">Отдельные серверы исправлений для одного из серверов исправлений</span><span class="sxs-lookup"><span data-stu-id="c8ac8-153">Separate Mediation Servers per Mediation Server peer</span></span>
    
    <span data-ttu-id="c8ac8-154">Когда consultative передача предназначена для однорангового сервера-посредника, пересылка consultative будет оцениваться относительно однорангового сервера единого обслуживания, обслуживаемого сервером-посредником.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-154">When a consultative transfer is targeted at a Mediation Server Peer, the consultative transfer will be evaluated against the single Mediation Server Peer serviced by the Mediation Server.</span></span> <span data-ttu-id="c8ac8-155">Этот звонок не будет разрешен или разрешен в соответствии со своими возможностями, которые могут повлечь за собой бесплатные звонки по бесплатной сети, независимо от того, на каком сервере они обходились, по мере их обслуживания разными серверами-посредниками.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-155">The call will be disallowed or allowed based in its potential to incur in PSTN toll bypass regardless of all other Mediations Server Peers in the site as they’re serviced by separate Mediation Servers.</span></span>
    
    <span data-ttu-id="c8ac8-156">Например, в случае отдельного сервера-посредника, обслуживающего одноранговый сервер шлюза КТСОП и одноранговый сервер обнаружения АТС, будут наблюдаться указанные ниже правила.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-156">For example, in the case of a separate Mediation Servers servicing a PSTN Gateway Mediation Server Peer and a PBX Mediation Server Peer, the following behavior will be observed:</span></span>
    
      - <span data-ttu-id="c8ac8-157">Если пользователь Lync с определенного сайта (например, сайт 1) пытается передать Звонок в конечную точку PSTN пользователю Lync из другого сайта (например, сайта 2) через consultative Transfer, Звонок будет запрещен для предотвращения бесплатных звонков по сети PSTN.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-157">When a Lync user from a given site (i.e. site 1) attempts to transfer a call with a PSTN endpoint to a Lync user from a different site (i.e. site 2) via consultative transfer, the call will be disallowed to prevent PSTN toll bypass.</span></span>
    
      - <span data-ttu-id="c8ac8-158">Если пользователь Lync с определенного сайта (например, сайт 1) пытается передать Звонок в конечную точку УАТС в том же сайте (например, на сайте 1) для пользователя Lync с другого сайта (то есть для сайта 2) через consultative Transfer, Звонок будет разрешен, так как он не повлечет за собой потенциальную бесплатный звонок.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-158">When a Lync user from a given site (i.e. site 1) attempts to transfer a call with a PBX endpoint in the same site (site 1) to a Lync user from a different site (i.e. site 2) via consultative transfer, the call will be allowed as it doesn’t incur in potential PSTN toll bypassing.</span></span>

</div>

<div>

## <a name="capabilities-not-supported-by-the-location-based-routing-conferencing-application"></a><span data-ttu-id="c8ac8-159">Возможности, не поддерживаемые приложением для конференц-связи Location-Based</span><span class="sxs-lookup"><span data-stu-id="c8ac8-159">Capabilities Not Supported by the Location-Based Routing Conferencing Application</span></span>

<span data-ttu-id="c8ac8-160">Следующие возможности не поддерживаются приложением для конференц-связи Location-Based.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-160">The following capabilities are not supported by the Location-Based Routing Conferencing application:</span></span>

  - <span data-ttu-id="c8ac8-161">Конференц-связь с телефонным подключением.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-161">Dial-in conferencing.</span></span> <span data-ttu-id="c8ac8-162">Для конференц-связи с телефонным подключением не может быть применена Location-Based маршрутизация.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-162">Location-Based Routing cannot be enforced for Dial-in conferencing.</span></span> <span data-ttu-id="c8ac8-163">Любой запрос на подключение к данной Конференции не ограничивается Location-Based маршрутом, даже если организатором конференции является пользователь Lync, на котором разрешена Location-Based маршрутизация.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-163">Any dial-in request to a given conference will not be restricted by Location-Based Routing even if the conference organizer is a Lync user enabled for Location-Based Routing.</span></span>

  - <span data-ttu-id="c8ac8-164">Не рекомендуется подготавливать номера доступа к конференциям в регионах, где должны быть принудительно Location-Based ограничения маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-164">It’s recommended not to provision conferencing access numbers in regions where Location-Based Routing restrictions need to be enforced.</span></span>

<span data-ttu-id="c8ac8-165"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c8ac8-165"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

