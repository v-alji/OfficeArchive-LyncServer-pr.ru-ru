---
title: 'Lync Server 2013: представление VoIPDetails'
description: 'Lync Server 2013: VoIPDetails View.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: VoIPDetails view
ms:assetid: 14c44736-71ba-4fc5-82c7-1df65bf6261c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687973(v=OCS.15)
ms:contentKeyID: 49733561
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5ecd34be0c8568eef29d773f088e8503a8065743
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446186"
---
# <a name="voipdetails-view-in-lync-server-2013"></a><span data-ttu-id="20263-103">VoIPDetails представления в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="20263-103">VoIPDetails view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="20263-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="20263-104">

<span> </span></span></span>

<span data-ttu-id="20263-105">_**Тема последнего изменения:** 2012-10-18_</span><span class="sxs-lookup"><span data-stu-id="20263-105">_**Topic Last Modified:** 2012-10-18_</span></span>

<span data-ttu-id="20263-106">В представлении VoIPDetails хранятся сведения о одноранговых сеансах, где по крайней мере один пользователь является пользователем VoIP.</span><span class="sxs-lookup"><span data-stu-id="20263-106">The VoIPDetails view stores information about peer-to-peer sessions, where at least one user is a VoIP user.</span></span> <span data-ttu-id="20263-107">Это представление было представлено в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="20263-107">This view was introduced in Microsoft Lync Server 2013.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="20263-108">В представлении VoIPDetails содержатся все столбцы в <A href="lync-server-2013-sessiondetails-view.md">представлении SessionDetails в Lync Server 2013</A> в дополнение к столбцам, перечисленным ниже.</span><span class="sxs-lookup"><span data-stu-id="20263-108">The VoIPDetails view contains all of the columns in the <A href="lync-server-2013-sessiondetails-view.md">SessionDetails view in Lync Server 2013</A> in addition the columns listed below.</span></span>



</div>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="20263-109">Столбец</span><span class="sxs-lookup"><span data-stu-id="20263-109">Column</span></span></th>
<th><span data-ttu-id="20263-110">Тип данных</span><span class="sxs-lookup"><span data-stu-id="20263-110">Data Type</span></span></th>
<th><span data-ttu-id="20263-111">Подробности</span><span class="sxs-lookup"><span data-stu-id="20263-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="20263-112"><strong>FromPhone</strong></span><span class="sxs-lookup"><span data-stu-id="20263-112"><strong>FromPhone</strong></span></span></p></td>
<td><p><span data-ttu-id="20263-113">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="20263-113">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="20263-114">URI телефона пользователя, запустившего сеанс.</span><span class="sxs-lookup"><span data-stu-id="20263-114">Phone URI of the user who started the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20263-115"><strong>ToPhone</strong></span><span class="sxs-lookup"><span data-stu-id="20263-115"><strong>ToPhone</strong></span></span></p></td>
<td><p><span data-ttu-id="20263-116">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="20263-116">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="20263-117">Универсальный код ресурса (URI) пользователя, который присоединился к сеансу.</span><span class="sxs-lookup"><span data-stu-id="20263-117">Phone URI of the user who joined the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20263-118"><strong>DisconnectedByUri</strong></span><span class="sxs-lookup"><span data-stu-id="20263-118"><strong>DisconnectedByUri</strong></span></span></p></td>
<td><p><span data-ttu-id="20263-119">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="20263-119">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="20263-120">Универсальный код ресурса (URI) пользователя, который отключил сеанс.</span><span class="sxs-lookup"><span data-stu-id="20263-120">URI of the user who disconnected the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20263-121"><strong>DisconnectedByUriType</strong></span><span class="sxs-lookup"><span data-stu-id="20263-121"><strong>DisconnectedByUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="20263-122">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="20263-122">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="20263-123">Тип URI пользователя, который отключил сеанс.</span><span class="sxs-lookup"><span data-stu-id="20263-123">Type of URI of the user who disconnected the session.</span></span> <span data-ttu-id="20263-124">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-uritypes-table.md">таблицей UriTypes в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="20263-124">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20263-125"><strong>DisconnectedByTenant</strong></span><span class="sxs-lookup"><span data-stu-id="20263-125"><strong>DisconnectedByTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="20263-126">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="20263-126">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="20263-127">Клиент пользователя, который отключил сеанс.</span><span class="sxs-lookup"><span data-stu-id="20263-127">Tenant of the user who disconnected the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20263-128"><strong>DisconnectedByPhone</strong></span><span class="sxs-lookup"><span data-stu-id="20263-128"><strong>DisconnectedByPhone</strong></span></span></p></td>
<td><p><span data-ttu-id="20263-129">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="20263-129">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="20263-130">Универсальный код ресурса (URI) пользователя, который отключил сеанс.</span><span class="sxs-lookup"><span data-stu-id="20263-130">Phone URI of the user who disconnected the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20263-131"><strong>FromMediationServer</strong></span><span class="sxs-lookup"><span data-stu-id="20263-131"><strong>FromMediationServer</strong></span></span></p></td>
<td><p><span data-ttu-id="20263-132">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="20263-132">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="20263-133">Сервер исправлений, используемый пользователем, который запустил сеанс.</span><span class="sxs-lookup"><span data-stu-id="20263-133">Mediation Server used by the user who started the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20263-134"><strong>ToMediationServer</strong></span><span class="sxs-lookup"><span data-stu-id="20263-134"><strong>ToMediationServer</strong></span></span></p></td>
<td><p><span data-ttu-id="20263-135">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="20263-135">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="20263-136">Сервер исправлений, используемый пользователем, который присоединил сеанс.</span><span class="sxs-lookup"><span data-stu-id="20263-136">Mediation Server used by the user who joined the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20263-137"><strong>FromGateway</strong></span><span class="sxs-lookup"><span data-stu-id="20263-137"><strong>FromGateway</strong></span></span></p></td>
<td><p><span data-ttu-id="20263-138">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="20263-138">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="20263-139">Шлюз, используемый пользователем, который запустил сеанс.</span><span class="sxs-lookup"><span data-stu-id="20263-139">Gateway used by the user who started the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20263-140"><strong>ToGateway</strong></span><span class="sxs-lookup"><span data-stu-id="20263-140"><strong>ToGateway</strong></span></span></p></td>
<td><p><span data-ttu-id="20263-141">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="20263-141">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="20263-142">Шлюз, используемый пользователем, который присоединился к сеансу.</span><span class="sxs-lookup"><span data-stu-id="20263-142">Gateway used by the user who joined the session.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="20263-143">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="20263-143">


</div>

<span> </span>

</div>

</div>

</span></span></div>

