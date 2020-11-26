---
title: 'Lync Server 2013: представление "Конференции"'
description: 'Lync Server 2013: представление "Конференции".'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Conferences view
ms:assetid: c0e5c4db-c135-401f-9296-e9a49f6499a1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721871(v=OCS.15)
ms:contentKeyID: 49733803
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dee7fbb7c839c351fc9c81716a5800a678980549
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434426"
---
# <a name="conferences-view-in-lync-server-2013"></a><span data-ttu-id="2f2b4-103">Представление "Конференции" в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2f2b4-103">Conferences view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2f2b4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2f2b4-104">

<span> </span></span></span>

<span data-ttu-id="2f2b4-105">_**Тема последнего изменения:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="2f2b4-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="2f2b4-106">В представлении "Конференции" хранятся сведения о конференциях.</span><span class="sxs-lookup"><span data-stu-id="2f2b4-106">The Conferences View stores information about the conferences.</span></span> <span data-ttu-id="2f2b4-107">Это представление было представлено в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="2f2b4-107">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2f2b4-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="2f2b4-108">Column</span></span></th>
<th><span data-ttu-id="2f2b4-109">Тип данных</span><span class="sxs-lookup"><span data-stu-id="2f2b4-109">Data Type</span></span></th>
<th><span data-ttu-id="2f2b4-110">Подробности</span><span class="sxs-lookup"><span data-stu-id="2f2b4-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2f2b4-111"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="2f2b4-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="2f2b4-112">datetime</span><span class="sxs-lookup"><span data-stu-id="2f2b4-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="2f2b4-113">Время запроса сеанса.</span><span class="sxs-lookup"><span data-stu-id="2f2b4-113">Time of session request.</span></span> <span data-ttu-id="2f2b4-114">Используется в сочетании с SessionIdSeq для уникальной идентификации сеанса.</span><span class="sxs-lookup"><span data-stu-id="2f2b4-114">Used in conjunction with SessionIdSeq to uniquely identify a session.</span></span> <span data-ttu-id="2f2b4-115">Дополнительные сведения приведены <a href="lync-server-2013-dialogs-table.md">в таблице диалоговые окна Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="2f2b4-115">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f2b4-116"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="2f2b4-116"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="2f2b4-117">целое</span><span class="sxs-lookup"><span data-stu-id="2f2b4-117">int</span></span></p></td>
<td><p><span data-ttu-id="2f2b4-118">ИДЕНТИФИКАЦИОНный номер для идентификации сеанса.</span><span class="sxs-lookup"><span data-stu-id="2f2b4-118">ID number to identify the session.</span></span> <span data-ttu-id="2f2b4-119">Используется в сочетании с SessionIdTime для уникальной идентификации сеанса.</span><span class="sxs-lookup"><span data-stu-id="2f2b4-119">Used in conjunction with SessionIdTime to uniquely identify a session.</span></span> <span data-ttu-id="2f2b4-120">Дополнительные сведения приведены <a href="lync-server-2013-dialogs-table.md">в таблице диалоговые окна Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="2f2b4-120">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f2b4-121"><strong>ConferenceUri</strong></span><span class="sxs-lookup"><span data-stu-id="2f2b4-121"><strong>ConferenceUri</strong></span></span></p></td>
<td><p><span data-ttu-id="2f2b4-122">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="2f2b4-122">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="2f2b4-123">Универсальный код ресурса (URI) для Конференции.</span><span class="sxs-lookup"><span data-stu-id="2f2b4-123">URI for the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f2b4-124"><strong>ConferenceUriType</strong></span><span class="sxs-lookup"><span data-stu-id="2f2b4-124"><strong>ConferenceUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="2f2b4-125">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="2f2b4-125">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="2f2b4-126">Тип URI конференции.</span><span class="sxs-lookup"><span data-stu-id="2f2b4-126">Type of the conference URI.</span></span> <span data-ttu-id="2f2b4-127">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-uritypes-table.md">таблицей UriTypes в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="2f2b4-127">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f2b4-128"><strong>ConfInstance</strong></span><span class="sxs-lookup"><span data-stu-id="2f2b4-128"><strong>ConfInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="2f2b4-129">идентификатора</span><span class="sxs-lookup"><span data-stu-id="2f2b4-129">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="2f2b4-130">Используется для повторяющихся конференций.</span><span class="sxs-lookup"><span data-stu-id="2f2b4-130">Used for recurring conferences.</span></span> <span data-ttu-id="2f2b4-131">Каждый экземпляр повторяющейся Конференции имеет один и тот же ConferenceUri, но другой ConfInstance.</span><span class="sxs-lookup"><span data-stu-id="2f2b4-131">Each instance of a recurring conference has the same ConferenceUri but a different ConfInstance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f2b4-132"><strong>ConferenceStartTime</strong></span><span class="sxs-lookup"><span data-stu-id="2f2b4-132"><strong>ConferenceStartTime</strong></span></span></p></td>
<td><p><span data-ttu-id="2f2b4-133">datetime</span><span class="sxs-lookup"><span data-stu-id="2f2b4-133">datetime</span></span></p></td>
<td><p><span data-ttu-id="2f2b4-134">Время начала Конференции.</span><span class="sxs-lookup"><span data-stu-id="2f2b4-134">Starting time for the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f2b4-135"><strong>ConferenceEndTime</strong></span><span class="sxs-lookup"><span data-stu-id="2f2b4-135"><strong>ConferenceEndTime</strong></span></span></p></td>
<td><p><span data-ttu-id="2f2b4-136">datetime</span><span class="sxs-lookup"><span data-stu-id="2f2b4-136">datetime</span></span></p></td>
<td><p><span data-ttu-id="2f2b4-137">Время окончания Конференции.</span><span class="sxs-lookup"><span data-stu-id="2f2b4-137">Ending time for the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f2b4-138"><strong>OrganizerUri</strong></span><span class="sxs-lookup"><span data-stu-id="2f2b4-138"><strong>OrganizerUri</strong></span></span></p></td>
<td><p><span data-ttu-id="2f2b4-139">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="2f2b4-139">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="2f2b4-140">Универсальный код ресурса (URI) пользователя, который организовал конференцию.</span><span class="sxs-lookup"><span data-stu-id="2f2b4-140">URI of the user who organized the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f2b4-141"><strong>OrganizerType</strong></span><span class="sxs-lookup"><span data-stu-id="2f2b4-141"><strong>OrganizerType</strong></span></span></p></td>
<td><p><span data-ttu-id="2f2b4-142">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="2f2b4-142">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="2f2b4-143">Тип URI пользователя, который организовал конференцию.</span><span class="sxs-lookup"><span data-stu-id="2f2b4-143">Type of URI of the user who organized the conference.</span></span> <span data-ttu-id="2f2b4-144">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-uritypes-table.md">таблицей UriTypes в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="2f2b4-144">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f2b4-145"><strong>OrganizerTenant</strong></span><span class="sxs-lookup"><span data-stu-id="2f2b4-145"><strong>OrganizerTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="2f2b4-146">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="2f2b4-146">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="2f2b4-147">Клиент пользователя, который организовал конференцию.</span><span class="sxs-lookup"><span data-stu-id="2f2b4-147">Tenant of the user who organized the conference.</span></span> <span data-ttu-id="2f2b4-148">Дополнительные сведения приведены в <a href="lync-server-2013-tenants-table.md">таблице "клиенты" в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="2f2b4-148">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f2b4-149"><strong>Pool</strong></span><span class="sxs-lookup"><span data-stu-id="2f2b4-149"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="2f2b4-150">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="2f2b4-150">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="2f2b4-151">Полное доменное имя пула, на котором размещается конференция.</span><span class="sxs-lookup"><span data-stu-id="2f2b4-151">Fully qualified domain name of the pool that hosted the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f2b4-152"><strong>Пометка</strong></span><span class="sxs-lookup"><span data-stu-id="2f2b4-152"><strong>Flag</strong></span></span></p></td>
<td><p><span data-ttu-id="2f2b4-153">smallint</span><span class="sxs-lookup"><span data-stu-id="2f2b4-153">smallint</span></span></p></td>
<td><p><span data-ttu-id="2f2b4-154">Битовая маска, которая включает атрибуты Конференции.</span><span class="sxs-lookup"><span data-stu-id="2f2b4-154">Bit mask that contains Conference Attributes.</span></span> <span data-ttu-id="2f2b4-155">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="2f2b4-155">Possible values are:</span></span></p>
<p><span data-ttu-id="2f2b4-156">0X01 — искусственная транзакция</span><span class="sxs-lookup"><span data-stu-id="2f2b4-156">0X01 – Synthetic Transaction</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="2f2b4-157">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2f2b4-157">


</div>

<span> </span>

</div>

</div>

</span></span></div>

