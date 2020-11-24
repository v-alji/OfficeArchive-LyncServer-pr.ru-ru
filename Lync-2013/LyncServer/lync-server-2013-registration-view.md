---
title: 'Lync Server 2013: представление регистрации'
description: 'Lync Server 2013: представление регистрации.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Registration view
ms:assetid: 8a42bc7d-3d4f-43c1-9e15-89b2ee419ade
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688120(v=OCS.15)
ms:contentKeyID: 49733718
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: be169cafc324f89cacedda154ca49a8ff1ff39aa
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398731"
---
# <a name="registration-view-in-lync-server-2013"></a><span data-ttu-id="ee50a-103">Представление регистрации в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ee50a-103">Registration view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ee50a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ee50a-104">

<span> </span></span></span>

<span data-ttu-id="ee50a-105">_**Тема последнего изменения:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="ee50a-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="ee50a-106">В представлении регистрация хранятся сведения о регистрации пользователей.</span><span class="sxs-lookup"><span data-stu-id="ee50a-106">The Registration view stores information about user registration.</span></span> <span data-ttu-id="ee50a-107">Это представление было представлено в Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ee50a-107">This view was introduced in Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ee50a-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="ee50a-108">Column</span></span></th>
<th><span data-ttu-id="ee50a-109">Тип данных</span><span class="sxs-lookup"><span data-stu-id="ee50a-109">Data Type</span></span></th>
<th><span data-ttu-id="ee50a-110">Подробности</span><span class="sxs-lookup"><span data-stu-id="ee50a-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ee50a-111"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="ee50a-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="ee50a-112">datetime</span><span class="sxs-lookup"><span data-stu-id="ee50a-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="ee50a-113">Время запроса сеанса.</span><span class="sxs-lookup"><span data-stu-id="ee50a-113">Time of session request.</span></span> <span data-ttu-id="ee50a-114">Используется в сочетании с SessionIdSeq для уникальной идентификации сеанса.</span><span class="sxs-lookup"><span data-stu-id="ee50a-114">Used in conjunction with SessionIdSeq to uniquely identify a session.</span></span> <span data-ttu-id="ee50a-115">Дополнительные сведения приведены <a href="lync-server-2013-dialogs-table.md">в таблице диалоговые окна Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="ee50a-115">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee50a-116"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="ee50a-116"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="ee50a-117">целое</span><span class="sxs-lookup"><span data-stu-id="ee50a-117">int</span></span></p></td>
<td><p><span data-ttu-id="ee50a-118">ИДЕНТИФИКАЦИОНный номер для идентификации сеанса.</span><span class="sxs-lookup"><span data-stu-id="ee50a-118">ID number to identify the session.</span></span> <span data-ttu-id="ee50a-119">Используется в сочетании с SessionIdTime для уникальной идентификации сеанса.</span><span class="sxs-lookup"><span data-stu-id="ee50a-119">Used in conjunction with SessionIdTime to uniquely identify a session.</span></span> <span data-ttu-id="ee50a-120">Дополнительные сведения приведены <a href="lync-server-2013-dialogs-table.md">в таблице диалоговые окна Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="ee50a-120">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee50a-121"><strong>RegisterTime</strong></span><span class="sxs-lookup"><span data-stu-id="ee50a-121"><strong>RegisterTime</strong></span></span></p></td>
<td><p><span data-ttu-id="ee50a-122">datetime</span><span class="sxs-lookup"><span data-stu-id="ee50a-122">datetime</span></span></p></td>
<td><p><span data-ttu-id="ee50a-123">Время, когда была выполнена регистрация.</span><span class="sxs-lookup"><span data-stu-id="ee50a-123">Time at which registration occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee50a-124"><strong>UserUri</strong></span><span class="sxs-lookup"><span data-stu-id="ee50a-124"><strong>UserUri</strong></span></span></p></td>
<td><p><span data-ttu-id="ee50a-125">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="ee50a-125">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="ee50a-126">URI пользователя, который зарегистрировался.</span><span class="sxs-lookup"><span data-stu-id="ee50a-126">URI of the user who registered.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee50a-127"><strong>UserUriType</strong></span><span class="sxs-lookup"><span data-stu-id="ee50a-127"><strong>UserUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="ee50a-128">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="ee50a-128">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="ee50a-129">Тип URI пользователя, который зарегистрировался.</span><span class="sxs-lookup"><span data-stu-id="ee50a-129">Type of URI of the user who registered.</span></span> <span data-ttu-id="ee50a-130">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-uritypes-table.md">таблицей UriTypes в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="ee50a-130">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee50a-131"><strong>UserTenant</strong></span><span class="sxs-lookup"><span data-stu-id="ee50a-131"><strong>UserTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="ee50a-132">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="ee50a-132">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="ee50a-133">Клиент пользователя, который зарегистрировался.</span><span class="sxs-lookup"><span data-stu-id="ee50a-133">Tenant of the user who registered.</span></span> <span data-ttu-id="ee50a-134">Дополнительные сведения приведены в <a href="lync-server-2013-tenants-table.md">таблице "клиенты" в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="ee50a-134">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee50a-135"><strong>EndpointId</strong></span><span class="sxs-lookup"><span data-stu-id="ee50a-135"><strong>EndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="ee50a-136">идентификатора</span><span class="sxs-lookup"><span data-stu-id="ee50a-136">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="ee50a-137">Уникальный идентификатор конечной точки пользователя, зарегистрированного в.</span><span class="sxs-lookup"><span data-stu-id="ee50a-137">Unique identifier of the endpoint of the user registered with.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee50a-138"><strong>EndpointEra</strong></span><span class="sxs-lookup"><span data-stu-id="ee50a-138"><strong>EndpointEra</strong></span></span></p></td>
<td><p><span data-ttu-id="ee50a-139">идентификатора</span><span class="sxs-lookup"><span data-stu-id="ee50a-139">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="ee50a-140">Уникальный идентификатор, который используется для различения регистраций, включающих одного и того же пользователя и ту же конечную точку.</span><span class="sxs-lookup"><span data-stu-id="ee50a-140">Unique identifier used to differentiate registrations that involve the same user and the same endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee50a-141"><strong>DeRegisterType</strong></span><span class="sxs-lookup"><span data-stu-id="ee50a-141"><strong>DeRegisterType</strong></span></span></p></td>
<td><p><span data-ttu-id="ee50a-142">datetime</span><span class="sxs-lookup"><span data-stu-id="ee50a-142">datetime</span></span></p></td>
<td><p><span data-ttu-id="ee50a-143">Время, когда была произведена отмена регистрации.</span><span class="sxs-lookup"><span data-stu-id="ee50a-143">Time at which deregistration occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee50a-144"><strong>DeRegisterReason</strong></span><span class="sxs-lookup"><span data-stu-id="ee50a-144"><strong>DeRegisterReason</strong></span></span></p></td>
<td><p><span data-ttu-id="ee50a-145">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="ee50a-145">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="ee50a-146">Причина отмены регистрации.</span><span class="sxs-lookup"><span data-stu-id="ee50a-146">Reason for deregistration.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee50a-147"><strong>ClientVersion</strong></span><span class="sxs-lookup"><span data-stu-id="ee50a-147"><strong>ClientVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="ee50a-148">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="ee50a-148">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="ee50a-149">Версия клиента, используемая пользователем, который зарегистрировался.</span><span class="sxs-lookup"><span data-stu-id="ee50a-149">Version of client used by the user who registered.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee50a-150"><strong>ClientType</strong></span><span class="sxs-lookup"><span data-stu-id="ee50a-150"><strong>ClientType</strong></span></span></p></td>
<td><p><span data-ttu-id="ee50a-151">целое</span><span class="sxs-lookup"><span data-stu-id="ee50a-151">int</span></span></p></td>
<td><p><span data-ttu-id="ee50a-152">Клиент, используемый зарегистрированным пользователем.</span><span class="sxs-lookup"><span data-stu-id="ee50a-152">Client used by the user who registered.</span></span> <span data-ttu-id="ee50a-153">Дополнительные сведения вы увидите <a href="lync-server-2013-useragentdef-table.md">в таблице UserAgentDef в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="ee50a-153">See the <a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a> for more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee50a-154"><strong>ClientCategory</strong></span><span class="sxs-lookup"><span data-stu-id="ee50a-154"><strong>ClientCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="ee50a-155">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="ee50a-155">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="ee50a-156">Категория клиента, используемая пользователем, который зарегистрировался.</span><span class="sxs-lookup"><span data-stu-id="ee50a-156">Category of the client used by the user who registered.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee50a-157"><strong>Следующий</strong></span><span class="sxs-lookup"><span data-stu-id="ee50a-157"><strong>IpAddress</strong></span></span></p></td>
<td><p><span data-ttu-id="ee50a-158">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="ee50a-158">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="ee50a-159">IP-адрес, с которым пользователь зарегистрировался.</span><span class="sxs-lookup"><span data-stu-id="ee50a-159">IP Address the user registered with.</span></span> <span data-ttu-id="ee50a-160">Это может быть адрес IPv4 или IPv6.</span><span class="sxs-lookup"><span data-stu-id="ee50a-160">This may be an IPv4 or IPv6 address.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee50a-161"><strong>DialogId</strong></span><span class="sxs-lookup"><span data-stu-id="ee50a-161"><strong>DialogId</strong></span></span></p></td>
<td><p><span data-ttu-id="ee50a-162">varstring (775)</span><span class="sxs-lookup"><span data-stu-id="ee50a-162">varstring(775)</span></span></p></td>
<td><p><span data-ttu-id="ee50a-163">ИДЕНТИФИКАТОР диалогового окна SIP.</span><span class="sxs-lookup"><span data-stu-id="ee50a-163">SIP dialog ID.</span></span> <span data-ttu-id="ee50a-164">Формат:</span><span class="sxs-lookup"><span data-stu-id="ee50a-164">The format of the is:</span></span></p>
<p><span data-ttu-id="ee50a-165">диалоговое окно; тег "from-Tag"</span><span class="sxs-lookup"><span data-stu-id="ee50a-165">dialog;from-tag;to-tag</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee50a-166"><strong>ResponseCode</strong></span><span class="sxs-lookup"><span data-stu-id="ee50a-166"><strong>ResponseCode</strong></span></span></p></td>
<td><p><span data-ttu-id="ee50a-167">целое</span><span class="sxs-lookup"><span data-stu-id="ee50a-167">int</span></span></p></td>
<td><p><span data-ttu-id="ee50a-168">Код ответа SIP на приглашение на сеанс.</span><span class="sxs-lookup"><span data-stu-id="ee50a-168">SIP response code to the session invitation.</span></span> <span data-ttu-id="ee50a-169">Это поле обычно заполняется данными, созданными на основе исходного сообщения INVITE в сеансе.</span><span class="sxs-lookup"><span data-stu-id="ee50a-169">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="ee50a-170">Если сообщение приглашения отсутствует, поле заполняется датой и временем первого соответствующего сообщения SIP (пока, CANCEL, MESSAGE или INFO).</span><span class="sxs-lookup"><span data-stu-id="ee50a-170">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee50a-171"><strong>DiagnosticId</strong></span><span class="sxs-lookup"><span data-stu-id="ee50a-171"><strong>DiagnosticId</strong></span></span></p></td>
<td><p><span data-ttu-id="ee50a-172">целое</span><span class="sxs-lookup"><span data-stu-id="ee50a-172">int</span></span></p></td>
<td><p><span data-ttu-id="ee50a-173">Идентификатор диагностики, полученный в заголовке SIP.</span><span class="sxs-lookup"><span data-stu-id="ee50a-173">Diagnostic ID captured from SIP header.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee50a-174"><strong>регистратор</strong></span><span class="sxs-lookup"><span data-stu-id="ee50a-174"><strong>Registrar</strong></span></span></p></td>
<td><p><span data-ttu-id="ee50a-175">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="ee50a-175">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="ee50a-176">Полное доменное имя регистратора.</span><span class="sxs-lookup"><span data-stu-id="ee50a-176">FQDN of the Registrar.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee50a-177"><strong>Pool</strong></span><span class="sxs-lookup"><span data-stu-id="ee50a-177"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="ee50a-178">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="ee50a-178">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="ee50a-179">Полное доменное имя пула, который захватывает данные для сеанса.</span><span class="sxs-lookup"><span data-stu-id="ee50a-179">FQDN of the pool that captured the data for the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee50a-180"><strong>Пограничный сервер</strong></span><span class="sxs-lookup"><span data-stu-id="ee50a-180"><strong>EdgeServer</strong></span></span></p></td>
<td><p><span data-ttu-id="ee50a-181">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="ee50a-181">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="ee50a-182">Полное доменное имя пограничного сервера, используемое пользователем, который зарегистрировался.</span><span class="sxs-lookup"><span data-stu-id="ee50a-182">FQDN of the Edge Server used by the user who registered.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee50a-183"><strong>Internal (внутренний)</strong></span><span class="sxs-lookup"><span data-stu-id="ee50a-183"><strong>IsInternal</strong></span></span></p></td>
<td><p><span data-ttu-id="ee50a-184">бит</span><span class="sxs-lookup"><span data-stu-id="ee50a-184">bit</span></span></p></td>
<td><p><span data-ttu-id="ee50a-185">Указывает, вошел ли пользователь из внутренней сети.</span><span class="sxs-lookup"><span data-stu-id="ee50a-185">Indicates whether the user logged on from the internal network.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee50a-186"><strong>IsUserServiceAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="ee50a-186"><strong>IsUserServiceAvailable</strong></span></span></p></td>
<td><p><span data-ttu-id="ee50a-187">бит</span><span class="sxs-lookup"><span data-stu-id="ee50a-187">bit</span></span></p></td>
<td><p><span data-ttu-id="ee50a-188">Указывает, был ли UserService доступен на момент регистрации.</span><span class="sxs-lookup"><span data-stu-id="ee50a-188">Indicates whether the UserService was available at registration time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee50a-189"><strong>IsPrimaryRegistrar</strong></span><span class="sxs-lookup"><span data-stu-id="ee50a-189"><strong>IsPrimaryRegistrar</strong></span></span></p></td>
<td><p><span data-ttu-id="ee50a-190">бит</span><span class="sxs-lookup"><span data-stu-id="ee50a-190">bit</span></span></p></td>
<td><p><span data-ttu-id="ee50a-191">Указывает, была ли регистрация основным регистратором.</span><span class="sxs-lookup"><span data-stu-id="ee50a-191">Indicates whether registration was with the primary Registrar.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee50a-192"><strong>DeviceMacAddress</strong></span><span class="sxs-lookup"><span data-stu-id="ee50a-192"><strong>DeviceMacAddress</strong></span></span></p></td>
<td><p><span data-ttu-id="ee50a-193">bigint</span><span class="sxs-lookup"><span data-stu-id="ee50a-193">bigint</span></span></p></td>
<td><p><span data-ttu-id="ee50a-194">MAC-адрес устройства зарегистрирован.</span><span class="sxs-lookup"><span data-stu-id="ee50a-194">MAC Address of device registered.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee50a-195"><strong>DeviceManufacturer</strong></span><span class="sxs-lookup"><span data-stu-id="ee50a-195"><strong>DeviceManufacturer</strong></span></span></p></td>
<td><p><span data-ttu-id="ee50a-196">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="ee50a-196">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="ee50a-197">Производитель зарегистрированного устройства.</span><span class="sxs-lookup"><span data-stu-id="ee50a-197">Manufacturer of the device registered.</span></span> <span data-ttu-id="ee50a-198">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-manufacturers-table.md">таблицей изготовителей в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="ee50a-198">See the <a href="lync-server-2013-manufacturers-table.md">Manufacturers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee50a-199"><strong>DeviceHardwareVersion</strong></span><span class="sxs-lookup"><span data-stu-id="ee50a-199"><strong>DeviceHardwareVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="ee50a-200">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="ee50a-200">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="ee50a-201">Аппаратная версия зарегистрированного устройства.</span><span class="sxs-lookup"><span data-stu-id="ee50a-201">Hardware version of the device registered.</span></span> <span data-ttu-id="ee50a-202">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-hardwareversions-table.md">таблицей HardwareVersions в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="ee50a-202">See the <a href="lync-server-2013-hardwareversions-table.md">HardwareVersions table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="ee50a-203">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ee50a-203">


</div>

<span> </span>

</div>

</div>

</span></span></div>

