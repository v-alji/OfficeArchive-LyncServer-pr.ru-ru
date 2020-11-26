---
title: 'Lync Server 2013: таблица Registration'
description: 'Lync Server 2013: таблица регистрации.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Registration table
ms:assetid: 05ff9dd3-1aaa-4af0-bd69-8789fb8eaeb3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398114(v=OCS.15)
ms:contentKeyID: 48183298
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 806e1a4e944c9bc04ebdd167c41c80a57fde3f29
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436568"
---
# <a name="registration-table-in-lync-server-2013"></a><span data-ttu-id="32e36-103">Таблица Registration в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="32e36-103">Registration table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="32e36-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="32e36-104">

<span> </span></span></span>

<span data-ttu-id="32e36-105">_**Тема последнего изменения:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="32e36-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="32e36-106">Каждая запись представляет одно событие регистрации пользователя.</span><span class="sxs-lookup"><span data-stu-id="32e36-106">Each record represents one user registration event.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="32e36-107">Столбец</span><span class="sxs-lookup"><span data-stu-id="32e36-107">Column</span></span></th>
<th><span data-ttu-id="32e36-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="32e36-108">Data Type</span></span></th>
<th><span data-ttu-id="32e36-109">Ключ/индекс</span><span class="sxs-lookup"><span data-stu-id="32e36-109">Key/Index</span></span></th>
<th><span data-ttu-id="32e36-110">Сведения</span><span class="sxs-lookup"><span data-stu-id="32e36-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="32e36-111"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="32e36-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="32e36-112">datetime</span><span class="sxs-lookup"><span data-stu-id="32e36-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="32e36-113">Основной, внешний</span><span class="sxs-lookup"><span data-stu-id="32e36-113">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="32e36-114">Время запроса сеанса.</span><span class="sxs-lookup"><span data-stu-id="32e36-114">Time of session request.</span></span> <span data-ttu-id="32e36-115">Используется в сочетании с <strong>SessionIdSeq</strong> для уникальной идентификации сеанса.</span><span class="sxs-lookup"><span data-stu-id="32e36-115">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="32e36-116">Дополнительные сведения приведены <a href="lync-server-2013-dialogs-table.md">в таблице диалоговые окна Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="32e36-116">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32e36-117"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="32e36-117"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="32e36-118">целое</span><span class="sxs-lookup"><span data-stu-id="32e36-118">int</span></span></p></td>
<td><p><span data-ttu-id="32e36-119">Основной, внешний</span><span class="sxs-lookup"><span data-stu-id="32e36-119">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="32e36-120">ИДЕНТИФИКАЦИОНный номер для идентификации сеанса.</span><span class="sxs-lookup"><span data-stu-id="32e36-120">ID number to identify the session.</span></span> <span data-ttu-id="32e36-121">Используется в сочетании с <strong>SessionIdTime</strong> для уникальной идентификации сеанса.</span><span class="sxs-lookup"><span data-stu-id="32e36-121">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.</span></span> <span data-ttu-id="32e36-122">Дополнительные сведения приведены <a href="lync-server-2013-dialogs-table.md">в таблице диалоговые окна Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="32e36-122">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32e36-123"><strong>Идентификатора пользователя</strong></span><span class="sxs-lookup"><span data-stu-id="32e36-123"><strong>UserId</strong></span></span></p></td>
<td><p><span data-ttu-id="32e36-124">целое</span><span class="sxs-lookup"><span data-stu-id="32e36-124">int</span></span></p></td>
<td><p><span data-ttu-id="32e36-125">Другом</span><span class="sxs-lookup"><span data-stu-id="32e36-125">Foreign</span></span></p></td>
<td><p><span data-ttu-id="32e36-126">Идентификатор пользователя.</span><span class="sxs-lookup"><span data-stu-id="32e36-126">The user ID.</span></span> <span data-ttu-id="32e36-127">Дополнительные сведения <a href="lync-server-2013-users-table.md">можно найти в таблице Users (пользователи) в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="32e36-127">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32e36-128"><strong>EndpointId</strong></span><span class="sxs-lookup"><span data-stu-id="32e36-128"><strong>EndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="32e36-129">идентификатора</span><span class="sxs-lookup"><span data-stu-id="32e36-129">uniqueidentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="32e36-130">GUID для идентификации конечной точки регистрации.</span><span class="sxs-lookup"><span data-stu-id="32e36-130">A GUID to identify a registration endpoint.</span></span> <span data-ttu-id="32e36-131">Обычно событие Register на том же компьютере того же пользователя будет иметь тот же идентификатор конечной точки.</span><span class="sxs-lookup"><span data-stu-id="32e36-131">Usually the register event from the same computer of the same user will have the same endpoint ID.</span></span> <span data-ttu-id="32e36-132">У разных компьютеров другой идентификатор конечной точки.</span><span class="sxs-lookup"><span data-stu-id="32e36-132">Different machines have a different endpoint ID.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32e36-133"><strong>EndpointEra</strong></span><span class="sxs-lookup"><span data-stu-id="32e36-133"><strong>EndpointEra</strong></span></span></p></td>
<td><p><span data-ttu-id="32e36-134">Идентификатора</span><span class="sxs-lookup"><span data-stu-id="32e36-134">uniqueIdentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="32e36-135">Идентификатор, который используется для различения регистраций, включающих одного и того же пользователя и ту же конечную точку.</span><span class="sxs-lookup"><span data-stu-id="32e36-135">ID used to differentiate registrations that involve the same user and the same endpoint.</span></span></p>
<p><span data-ttu-id="32e36-136">Это поле было введено в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="32e36-136">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32e36-137"><strong>ClientVersionId</strong></span><span class="sxs-lookup"><span data-stu-id="32e36-137"><strong>ClientVersionId</strong></span></span></p></td>
<td><p><span data-ttu-id="32e36-138">целое</span><span class="sxs-lookup"><span data-stu-id="32e36-138">int</span></span></p></td>
<td><p><span data-ttu-id="32e36-139">Другом</span><span class="sxs-lookup"><span data-stu-id="32e36-139">Foreign</span></span></p></td>
<td><p><span data-ttu-id="32e36-140">Клиентская версия текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="32e36-140">Client version of current user.</span></span> <span data-ttu-id="32e36-141">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-clientversions-table.md">таблицей ClientVersions в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="32e36-141">See the <a href="lync-server-2013-clientversions-table.md">ClientVersions table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32e36-142"><strong>RegistrarId</strong></span><span class="sxs-lookup"><span data-stu-id="32e36-142"><strong>RegistrarId</strong></span></span></p></td>
<td><p><span data-ttu-id="32e36-143">целое</span><span class="sxs-lookup"><span data-stu-id="32e36-143">int</span></span></p></td>
<td><p><span data-ttu-id="32e36-144">Другом</span><span class="sxs-lookup"><span data-stu-id="32e36-144">Foreign</span></span></p></td>
<td><p><span data-ttu-id="32e36-145">Идентификатор сервера регистратора, используемого для регистрации.</span><span class="sxs-lookup"><span data-stu-id="32e36-145">ID of the Registrar Server used for registration.</span></span> <span data-ttu-id="32e36-146">Более подробную информацию вы видите <a href="lync-server-2013-servers-table.md">в таблице Servers (серверы) в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="32e36-146">See the <a href="lync-server-2013-servers-table.md">Servers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32e36-147"><strong>PoolId</strong></span><span class="sxs-lookup"><span data-stu-id="32e36-147"><strong>PoolId</strong></span></span></p></td>
<td><p><span data-ttu-id="32e36-148">целое</span><span class="sxs-lookup"><span data-stu-id="32e36-148">int</span></span></p></td>
<td><p><span data-ttu-id="32e36-149">Другом</span><span class="sxs-lookup"><span data-stu-id="32e36-149">Foreign</span></span></p></td>
<td><p><span data-ttu-id="32e36-150">Идентификатор пула, в котором был собран сеанс.</span><span class="sxs-lookup"><span data-stu-id="32e36-150">ID of the pool in which the session was captured.</span></span> <span data-ttu-id="32e36-151">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-pools-table.md">таблицей пулы в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="32e36-151">See the <a href="lync-server-2013-pools-table.md">Pools table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32e36-152"><strong>EdgeServerId</strong></span><span class="sxs-lookup"><span data-stu-id="32e36-152"><strong>EdgeServerId</strong></span></span></p></td>
<td><p><span data-ttu-id="32e36-153">целое</span><span class="sxs-lookup"><span data-stu-id="32e36-153">int</span></span></p></td>
<td><p><span data-ttu-id="32e36-154">Другом</span><span class="sxs-lookup"><span data-stu-id="32e36-154">Foreign</span></span></p></td>
<td><p><span data-ttu-id="32e36-155">Пограничный сервер, на котором проходит регистрация.</span><span class="sxs-lookup"><span data-stu-id="32e36-155">Edge Server the registration is going through.</span></span> <span data-ttu-id="32e36-156">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-edgeservers-table.md">таблицей EdgeServers в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="32e36-156">See the <a href="lync-server-2013-edgeservers-table.md">EdgeServers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32e36-157"><strong>Internal (внутренний)</strong></span><span class="sxs-lookup"><span data-stu-id="32e36-157"><strong>IsInternal</strong></span></span></p></td>
<td><p><span data-ttu-id="32e36-158">Разрядная версия</span><span class="sxs-lookup"><span data-stu-id="32e36-158">Bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="32e36-159">Вход пользователя из внутреннего режима или нет.</span><span class="sxs-lookup"><span data-stu-id="32e36-159">Whether the user is logged on from internal or not.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32e36-160"><strong>IsUserServiceAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="32e36-160"><strong>IsUserServiceAvailable</strong></span></span></p></td>
<td><p><span data-ttu-id="32e36-161">бит</span><span class="sxs-lookup"><span data-stu-id="32e36-161">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="32e36-162">Доступен ли UserService или нет.</span><span class="sxs-lookup"><span data-stu-id="32e36-162">Whether the UserService is available or not.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32e36-163"><strong>IsPrimaryRegistrar</strong></span><span class="sxs-lookup"><span data-stu-id="32e36-163"><strong>IsPrimaryRegistrar</strong></span></span></p></td>
<td><p><span data-ttu-id="32e36-164">бит</span><span class="sxs-lookup"><span data-stu-id="32e36-164">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="32e36-165">Регистрация для основного регистратора или нет.</span><span class="sxs-lookup"><span data-stu-id="32e36-165">Whether register to the primary Registrar or not.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32e36-166"><strong>IsPrimaryRegistrarCentral</strong></span><span class="sxs-lookup"><span data-stu-id="32e36-166"><strong>IsPrimaryRegistrarCentral</strong></span></span></p></td>
<td><p><span data-ttu-id="32e36-167">бит</span><span class="sxs-lookup"><span data-stu-id="32e36-167">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="32e36-168">Указывает, зарегистрирован ли пользователь в работающем устройстве филиала.</span><span class="sxs-lookup"><span data-stu-id="32e36-168">Indicates whether or not the user is registered with a survivable branch appliance.</span></span></p>
<p><span data-ttu-id="32e36-169">Это поле было введено в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="32e36-169">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32e36-170"><strong>RegisterTime</strong></span><span class="sxs-lookup"><span data-stu-id="32e36-170"><strong>RegisterTime</strong></span></span></p></td>
<td><p><span data-ttu-id="32e36-171">datetime</span><span class="sxs-lookup"><span data-stu-id="32e36-171">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="32e36-172">Время регистрации.</span><span class="sxs-lookup"><span data-stu-id="32e36-172">Registration time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32e36-173"><strong>DeRegisterTime</strong></span><span class="sxs-lookup"><span data-stu-id="32e36-173"><strong>DeRegisterTime</strong></span></span></p></td>
<td><p><span data-ttu-id="32e36-174">datetime</span><span class="sxs-lookup"><span data-stu-id="32e36-174">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="32e36-175">De-Registration Time (время).</span><span class="sxs-lookup"><span data-stu-id="32e36-175">De-Registration time.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32e36-176"><strong>ResponseCode</strong></span><span class="sxs-lookup"><span data-stu-id="32e36-176"><strong>ResponseCode</strong></span></span></p></td>
<td><p><span data-ttu-id="32e36-177">целое</span><span class="sxs-lookup"><span data-stu-id="32e36-177">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="32e36-178">Код ответа на запрос на регистрацию.</span><span class="sxs-lookup"><span data-stu-id="32e36-178">Response code of the register request.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32e36-179"><strong>DiagnosticId</strong></span><span class="sxs-lookup"><span data-stu-id="32e36-179"><strong>DiagnosticId</strong></span></span></p></td>
<td><p><span data-ttu-id="32e36-180">целое</span><span class="sxs-lookup"><span data-stu-id="32e36-180">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="32e36-181">Идентификатор диагностики запроса на регистрацию.</span><span class="sxs-lookup"><span data-stu-id="32e36-181">Diagnostic ID of the register request.</span></span> <span data-ttu-id="32e36-182">Это означает, что тип данных диагностики.</span><span class="sxs-lookup"><span data-stu-id="32e36-182">This indicates that diagnostic information type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32e36-183"><strong>Устройства</strong></span><span class="sxs-lookup"><span data-stu-id="32e36-183"><strong>DeviceId</strong></span></span></p></td>
<td><p><span data-ttu-id="32e36-184">целое</span><span class="sxs-lookup"><span data-stu-id="32e36-184">int</span></span></p></td>
<td><p><span data-ttu-id="32e36-185">Другом</span><span class="sxs-lookup"><span data-stu-id="32e36-185">Foreign</span></span></p></td>
<td><p><span data-ttu-id="32e36-186">Устройство, от которого поступил запрос на регистрацию.</span><span class="sxs-lookup"><span data-stu-id="32e36-186">The device that the register request is coming from.</span></span> <span data-ttu-id="32e36-187">Более подробную информацию вы видите в <a href="lync-server-2013-devices-table.md">таблице "устройства" в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="32e36-187">See the <a href="lync-server-2013-devices-table.md">Devices table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32e36-188"><strong>DeRegisterTypeId</strong></span><span class="sxs-lookup"><span data-stu-id="32e36-188"><strong>DeRegisterTypeId</strong></span></span></p></td>
<td><p><span data-ttu-id="32e36-189">tinyint</span><span class="sxs-lookup"><span data-stu-id="32e36-189">tinyint</span></span></p></td>
<td><p><span data-ttu-id="32e36-190">Другом</span><span class="sxs-lookup"><span data-stu-id="32e36-190">Foreign</span></span></p></td>
<td><p><span data-ttu-id="32e36-191">Причина отмены регистрации, например "пользователь инициировал", "регистрация просрочена", "клиент не проходит" и многое другое.</span><span class="sxs-lookup"><span data-stu-id="32e36-191">The reason of de-register, such as ‘user initiated’, ‘registration expired’, ‘client fail’, and more.</span></span> <span data-ttu-id="32e36-192">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-deregistertype-table.md">таблицей DeRegisterType в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="32e36-192">See the <a href="lync-server-2013-deregistertype-table.md">DeRegisterType table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32e36-193"><strong>IPAddress</strong></span><span class="sxs-lookup"><span data-stu-id="32e36-193"><strong>IPAddress</strong></span></span></p></td>
<td><p><span data-ttu-id="32e36-194">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="32e36-194">nvarchar(256)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="32e36-195">IP-адрес конечной точки, зарегистрированной пользователем.</span><span class="sxs-lookup"><span data-stu-id="32e36-195">IP address of the endpoint the user registered with.</span></span> <span data-ttu-id="32e36-196">Это может быть адрес IPv4 или IPv6.</span><span class="sxs-lookup"><span data-stu-id="32e36-196">This can be an IPv4 address or an IPv6 address.</span></span></p>
<p><span data-ttu-id="32e36-197">Это поле было введено в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="32e36-197">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="32e36-198">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="32e36-198">


</div>

<span> </span>

</div>

</div>

</span></span></div>

