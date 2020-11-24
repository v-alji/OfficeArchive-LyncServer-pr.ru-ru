---
title: 'Lync Server 2013: таблица VoipDetails'
description: 'Таблица Lync Server 2013: VoipDetails.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: VoipDetails table
ms:assetid: 74ffbb71-569b-4018-be1f-4db2bbafcf36
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398566(v=OCS.15)
ms:contentKeyID: 48184522
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f23d991c1d577a15717de2572d744e1b65ba6bab
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49397888"
---
# <a name="voipdetails-table-in-lync-server-2013"></a><span data-ttu-id="3810e-103">Таблица VoipDetails в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3810e-103">VoipDetails table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3810e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3810e-104">

<span> </span></span></span>

<span data-ttu-id="3810e-105">_**Тема последнего изменения:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="3810e-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="3810e-106">Каждая запись представляет вызов на стороне 1 2, в котором как минимум один пользователь является пользователем VoIP.</span><span class="sxs-lookup"><span data-stu-id="3810e-106">Each record represents one two-party call in which at least one user is a VoIP user.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3810e-107">Столбец</span><span class="sxs-lookup"><span data-stu-id="3810e-107">Column</span></span></th>
<th><span data-ttu-id="3810e-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="3810e-108">Data Type</span></span></th>
<th><span data-ttu-id="3810e-109">Ключ/индекс</span><span class="sxs-lookup"><span data-stu-id="3810e-109">Key/Index</span></span></th>
<th><span data-ttu-id="3810e-110">Сведения</span><span class="sxs-lookup"><span data-stu-id="3810e-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3810e-111"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="3810e-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="3810e-112">datetime</span><span class="sxs-lookup"><span data-stu-id="3810e-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="3810e-113">Primary</span><span class="sxs-lookup"><span data-stu-id="3810e-113">Primary</span></span></p></td>
<td><p><span data-ttu-id="3810e-114">Время запроса сеанса.</span><span class="sxs-lookup"><span data-stu-id="3810e-114">Time of session request.</span></span> <span data-ttu-id="3810e-115">Используется в сочетании с <strong>SessionIdSeq</strong> для уникальной идентификации сеанса.</span><span class="sxs-lookup"><span data-stu-id="3810e-115">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="3810e-116">Дополнительные сведения приведены <a href="lync-server-2013-dialogs-table.md">в таблице диалоговые окна Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="3810e-116">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3810e-117"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="3810e-117"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="3810e-118">целое</span><span class="sxs-lookup"><span data-stu-id="3810e-118">int</span></span></p></td>
<td><p><span data-ttu-id="3810e-119">Primary</span><span class="sxs-lookup"><span data-stu-id="3810e-119">Primary</span></span></p></td>
<td><p><span data-ttu-id="3810e-120">ИДЕНТИФИКАЦИОНный номер для идентификации сеанса.</span><span class="sxs-lookup"><span data-stu-id="3810e-120">ID number to identify the session.</span></span> <span data-ttu-id="3810e-121">Используется в сочетании с <strong>SessionIdTime</strong> для уникальной идентификации сеанса.</span><span class="sxs-lookup"><span data-stu-id="3810e-121">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.</span></span> <span data-ttu-id="3810e-122">Дополнительные сведения приведены <a href="lync-server-2013-dialogs-table.md">в таблице диалоговые окна Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="3810e-122">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3810e-123"><strong>FromNumberId</strong></span><span class="sxs-lookup"><span data-stu-id="3810e-123"><strong>FromNumberId</strong></span></span></p></td>
<td><p><span data-ttu-id="3810e-124">целое</span><span class="sxs-lookup"><span data-stu-id="3810e-124">int</span></span></p></td>
<td><p><span data-ttu-id="3810e-125">Другом</span><span class="sxs-lookup"><span data-stu-id="3810e-125">Foreign</span></span></p></td>
<td><p><span data-ttu-id="3810e-126"><strong>PhoneId</strong> вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="3810e-126"><strong>PhoneId</strong> of the caller.</span></span> <span data-ttu-id="3810e-127">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-phones-table.md">таблицей "телефоны" в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="3810e-127">See the <a href="lync-server-2013-phones-table.md">Phones table in Lync Server 2013</a> for more information.</span></span> <span data-ttu-id="3810e-128">Если NOT NULL и <strong>FromGatewayId</strong> не NULL, вызывающий абонент являлся пользователем КТСОП.</span><span class="sxs-lookup"><span data-stu-id="3810e-128">If not NULL and <strong>FromGatewayId</strong> is not NULL, then the caller was a PSTN user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3810e-129"><strong>ConnectedNumberId</strong></span><span class="sxs-lookup"><span data-stu-id="3810e-129"><strong>ConnectedNumberId</strong></span></span></p></td>
<td><p><span data-ttu-id="3810e-130">целое</span><span class="sxs-lookup"><span data-stu-id="3810e-130">int</span></span></p></td>
<td><p><span data-ttu-id="3810e-131">Другом</span><span class="sxs-lookup"><span data-stu-id="3810e-131">Foreign</span></span></p></td>
<td><p><span data-ttu-id="3810e-132"><strong>PhoneId</strong> получателя звонка.</span><span class="sxs-lookup"><span data-stu-id="3810e-132"><strong>PhoneId</strong> of the call receiver.</span></span> <span data-ttu-id="3810e-133">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-phones-table.md">таблицей "телефоны" в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="3810e-133">See the <a href="lync-server-2013-phones-table.md">Phones table in Lync Server 2013</a> for more information.</span></span> <span data-ttu-id="3810e-134">Если NOT NULL и <strong>ToGatewayId</strong> не NULL, получатель звонка был пользователем КТСОП.</span><span class="sxs-lookup"><span data-stu-id="3810e-134">If not NULL and <strong>ToGatewayId</strong> is not NULL, then the call receiver was a PSTN user.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3810e-135"><strong>FromMediationServerId</strong></span><span class="sxs-lookup"><span data-stu-id="3810e-135"><strong>FromMediationServerId</strong></span></span></p></td>
<td><p><span data-ttu-id="3810e-136">целое</span><span class="sxs-lookup"><span data-stu-id="3810e-136">int</span></span></p></td>
<td><p><span data-ttu-id="3810e-137">Другом</span><span class="sxs-lookup"><span data-stu-id="3810e-137">Foreign</span></span></p></td>
<td><p><span data-ttu-id="3810e-138">Сервер, на котором поступил звонок.</span><span class="sxs-lookup"><span data-stu-id="3810e-138">The Mediation Server the call is coming from.</span></span> <span data-ttu-id="3810e-139">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-mediationservers-table.md">таблицей MediationServers в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="3810e-139">See the <a href="lync-server-2013-mediationservers-table.md">MediationServers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3810e-140"><strong>ToMediationServerId</strong></span><span class="sxs-lookup"><span data-stu-id="3810e-140"><strong>ToMediationServerId</strong></span></span></p></td>
<td><p><span data-ttu-id="3810e-141">целое</span><span class="sxs-lookup"><span data-stu-id="3810e-141">int</span></span></p></td>
<td><p><span data-ttu-id="3810e-142">Другом</span><span class="sxs-lookup"><span data-stu-id="3810e-142">Foreign</span></span></p></td>
<td><p><span data-ttu-id="3810e-143">Будет вызываем сервер для устранения проблем.</span><span class="sxs-lookup"><span data-stu-id="3810e-143">The Mediation Server called is going to.</span></span> <span data-ttu-id="3810e-144">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-mediationservers-table.md">таблицей MediationServers в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="3810e-144">See the <a href="lync-server-2013-mediationservers-table.md">MediationServers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3810e-145"><strong>FromGatewayId</strong></span><span class="sxs-lookup"><span data-stu-id="3810e-145"><strong>FromGatewayId</strong></span></span></p></td>
<td><p><span data-ttu-id="3810e-146">целое</span><span class="sxs-lookup"><span data-stu-id="3810e-146">int</span></span></p></td>
<td><p><span data-ttu-id="3810e-147">Другом</span><span class="sxs-lookup"><span data-stu-id="3810e-147">Foreign</span></span></p></td>
<td><p><span data-ttu-id="3810e-148">Шлюз, из которого поступил звонок.</span><span class="sxs-lookup"><span data-stu-id="3810e-148">Gateway the call is coming from.</span></span> <span data-ttu-id="3810e-149">Более подробную информацию вы увидите <a href="lync-server-2013-gateways-table.md">в таблице шлюзов в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="3810e-149">See the <a href="lync-server-2013-gateways-table.md">Gateways table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3810e-150"><strong>ToGatewayId</strong></span><span class="sxs-lookup"><span data-stu-id="3810e-150"><strong>ToGatewayId</strong></span></span></p></td>
<td><p><span data-ttu-id="3810e-151">целое</span><span class="sxs-lookup"><span data-stu-id="3810e-151">int</span></span></p></td>
<td><p><span data-ttu-id="3810e-152">Другом</span><span class="sxs-lookup"><span data-stu-id="3810e-152">Foreign</span></span></p></td>
<td><p><span data-ttu-id="3810e-153">Шлюз, на который проходит звонок.</span><span class="sxs-lookup"><span data-stu-id="3810e-153">Gateway the call is going to.</span></span> <span data-ttu-id="3810e-154">Более подробную информацию вы увидите <a href="lync-server-2013-gateways-table.md">в таблице шлюзов в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="3810e-154">See the <a href="lync-server-2013-gateways-table.md">Gateways table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3810e-155"><strong>DisconnectedbyURIId</strong></span><span class="sxs-lookup"><span data-stu-id="3810e-155"><strong>DisconnectedbyURIId</strong></span></span></p></td>
<td><p><span data-ttu-id="3810e-156">целое</span><span class="sxs-lookup"><span data-stu-id="3810e-156">int</span></span></p></td>
<td><p><span data-ttu-id="3810e-157">Другом</span><span class="sxs-lookup"><span data-stu-id="3810e-157">Foreign</span></span></p></td>
<td><p><span data-ttu-id="3810e-158">Универсальный код ресурса (URI) пользователя, который отключил звонок, если пользователь имеет URI.</span><span class="sxs-lookup"><span data-stu-id="3810e-158">URI of the user who disconnected the call, if the user has a URI.</span></span> <span data-ttu-id="3810e-159">Дополнительные сведения <a href="lync-server-2013-users-table.md">можно найти в таблице Users (пользователи) в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="3810e-159">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3810e-160"><strong>DisconnectedbyPhoneId</strong></span><span class="sxs-lookup"><span data-stu-id="3810e-160"><strong>DisconnectedbyPhoneId</strong></span></span></p></td>
<td><p><span data-ttu-id="3810e-161">целое</span><span class="sxs-lookup"><span data-stu-id="3810e-161">int</span></span></p></td>
<td><p><span data-ttu-id="3810e-162">Другом</span><span class="sxs-lookup"><span data-stu-id="3810e-162">Foreign</span></span></p></td>
<td><p><span data-ttu-id="3810e-163">Идентификационный номер телефона, который отключил звонок, был отключен от телефона.</span><span class="sxs-lookup"><span data-stu-id="3810e-163">ID of the phone that disconnected the call was disconnected from a phone.</span></span> <span data-ttu-id="3810e-164">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-phones-table.md">таблицей "телефоны" в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="3810e-164">See the <a href="lync-server-2013-phones-table.md">Phones table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="3810e-165">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3810e-165">


</div>

<span> </span>

</div>

</div>

</span></span></div>

