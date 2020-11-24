---
title: 'Lync Server 2013: таблица Conferences'
description: 'Lync Server 2013: Конференции с Конференцией.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Conferences table
ms:assetid: c3da6271-b3c6-4898-894f-10456ec794d0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412964(v=OCS.15)
ms:contentKeyID: 48185340
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1e0d8c61e795dc0c8f9843b871d7e4efd1bec571
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399382"
---
# <a name="conferences-table-in-lync-server-2013"></a><span data-ttu-id="8e337-103">Таблица Conferences в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8e337-103">Conferences table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8e337-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8e337-104">

<span> </span></span></span>

<span data-ttu-id="8e337-105">_**Тема последнего изменения:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="8e337-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="8e337-106">Каждая запись в этой таблице включает сведения о звонках для одной конференции.</span><span class="sxs-lookup"><span data-stu-id="8e337-106">Each record in this table contains call details about one conference.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8e337-107">Столбец</span><span class="sxs-lookup"><span data-stu-id="8e337-107">Column</span></span></th>
<th><span data-ttu-id="8e337-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="8e337-108">Data Type</span></span></th>
<th><span data-ttu-id="8e337-109">Ключ/индекс</span><span class="sxs-lookup"><span data-stu-id="8e337-109">Key/Index</span></span></th>
<th><span data-ttu-id="8e337-110">Сведения</span><span class="sxs-lookup"><span data-stu-id="8e337-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8e337-111"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="8e337-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="8e337-112">datetime</span><span class="sxs-lookup"><span data-stu-id="8e337-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="8e337-113">Primary</span><span class="sxs-lookup"><span data-stu-id="8e337-113">Primary</span></span></p></td>
<td><p><span data-ttu-id="8e337-114">Время, в течение которого запрос на конференцию был собран агентом CDR.</span><span class="sxs-lookup"><span data-stu-id="8e337-114">Time that the conference request was captured by the CDR agent.</span></span> <span data-ttu-id="8e337-115">Используется только в качестве первичного ключа для уникальной идентификации экземпляра Конференции.</span><span class="sxs-lookup"><span data-stu-id="8e337-115">Used only as a primary key to uniquely identify a conference instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e337-116"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="8e337-116"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="8e337-117">целое</span><span class="sxs-lookup"><span data-stu-id="8e337-117">int</span></span></p></td>
<td><p><span data-ttu-id="8e337-118">Primary</span><span class="sxs-lookup"><span data-stu-id="8e337-118">Primary</span></span></p></td>
<td><p><span data-ttu-id="8e337-119">ИДЕНТИФИКАЦИОНный номер для идентификации сеанса.</span><span class="sxs-lookup"><span data-stu-id="8e337-119">ID number to identify the session.</span></span> <span data-ttu-id="8e337-120">Используется в сочетании с <strong>SessionIdTime</strong> для уникальной идентификации экземпляра Конференции.</span><span class="sxs-lookup"><span data-stu-id="8e337-120">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a conference instance.</span></span> *</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e337-121"><strong>ConferenceUriId</strong></span><span class="sxs-lookup"><span data-stu-id="8e337-121"><strong>ConferenceUriId</strong></span></span></p></td>
<td><p><span data-ttu-id="8e337-122">целое</span><span class="sxs-lookup"><span data-stu-id="8e337-122">int</span></span></p></td>
<td><p><span data-ttu-id="8e337-123">Другом</span><span class="sxs-lookup"><span data-stu-id="8e337-123">Foreign</span></span></p></td>
<td><p><span data-ttu-id="8e337-124">Универсальный код ресурса (URI) Конференции.</span><span class="sxs-lookup"><span data-stu-id="8e337-124">Conference URI.</span></span> <span data-ttu-id="8e337-125">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-conferenceuris-table.md">таблицей ConferenceUris в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="8e337-125">See the <a href="lync-server-2013-conferenceuris-table.md">ConferenceUris table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e337-126"><strong>ConfInstance</strong></span><span class="sxs-lookup"><span data-stu-id="8e337-126"><strong>ConfInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="8e337-127">идентификатора</span><span class="sxs-lookup"><span data-stu-id="8e337-127">uniqueidentifier</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="8e337-128">Полезен для повторяющихся конференций; Каждый экземпляр повторяющейся Конференции имеет один и тот же <strong>ConferenceUri</strong>, но у него будет другой <strong>ConfInstance</strong>.</span><span class="sxs-lookup"><span data-stu-id="8e337-128">Useful for recurring conferences; each instance of a recurring conference has the same <strong>ConferenceUri</strong>, but will have a different <strong>ConfInstance</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e337-129"><strong>ConferenceStartTime</strong></span><span class="sxs-lookup"><span data-stu-id="8e337-129"><strong>ConferenceStartTime</strong></span></span></p></td>
<td><p><span data-ttu-id="8e337-130">datetime</span><span class="sxs-lookup"><span data-stu-id="8e337-130">datetime</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="8e337-131">Время начала Конференции.</span><span class="sxs-lookup"><span data-stu-id="8e337-131">Conference start time.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e337-132"><strong>ConferenceEndTime</strong></span><span class="sxs-lookup"><span data-stu-id="8e337-132"><strong>ConferenceEndTime</strong></span></span></p></td>
<td><p><span data-ttu-id="8e337-133">datetime</span><span class="sxs-lookup"><span data-stu-id="8e337-133">datetime</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="8e337-134">Время начала Конференции.</span><span class="sxs-lookup"><span data-stu-id="8e337-134">Conference start time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e337-135"><strong>PoolId</strong></span><span class="sxs-lookup"><span data-stu-id="8e337-135"><strong>PoolId</strong></span></span></p></td>
<td><p><span data-ttu-id="8e337-136">целое</span><span class="sxs-lookup"><span data-stu-id="8e337-136">int</span></span></p></td>
<td><p><span data-ttu-id="8e337-137">Другом</span><span class="sxs-lookup"><span data-stu-id="8e337-137">Foreign</span></span></p></td>
<td><p><span data-ttu-id="8e337-138">ИДЕНТИФИКАЦИОНный номер для идентификации пула, в котором собрана конференция.</span><span class="sxs-lookup"><span data-stu-id="8e337-138">ID number to identify the pool in which the conference was captured.</span></span> <span data-ttu-id="8e337-139">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-pools-table.md">таблицей пулы в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="8e337-139">See the <a href="lync-server-2013-pools-table.md">Pools table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e337-140"><strong>OrganizerId</strong></span><span class="sxs-lookup"><span data-stu-id="8e337-140"><strong>OrganizerId</strong></span></span></p></td>
<td><p><span data-ttu-id="8e337-141">Типом</span><span class="sxs-lookup"><span data-stu-id="8e337-141">Int</span></span></p></td>
<td><p><span data-ttu-id="8e337-142">Другом</span><span class="sxs-lookup"><span data-stu-id="8e337-142">Foreign</span></span></p></td>
<td><p><span data-ttu-id="8e337-143">ИДЕНТИФИКАЦИОНный номер для идентификации универсального кода ресурса (URI) организатора данной Конференции.</span><span class="sxs-lookup"><span data-stu-id="8e337-143">ID number to identify the organizer URI of this conference.</span></span> <span data-ttu-id="8e337-144">Дополнительные сведения <a href="lync-server-2013-users-table.md">можно найти в таблице Users (пользователи) в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="8e337-144">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e337-145"><strong>Пометка</strong></span><span class="sxs-lookup"><span data-stu-id="8e337-145"><strong>Flag</strong></span></span></p></td>
<td><p><span data-ttu-id="8e337-146">smallint</span><span class="sxs-lookup"><span data-stu-id="8e337-146">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="8e337-147">Битовая маска, которая включает атрибуты Конференции.</span><span class="sxs-lookup"><span data-stu-id="8e337-147">A bit mask that contains Conference Attributes.</span></span> <span data-ttu-id="8e337-148">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="8e337-148">Possible values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="8e337-149">0X01</span><span class="sxs-lookup"><span data-stu-id="8e337-149">0X01</span></span></p></li>
<li><p><span data-ttu-id="8e337-150">Накопител</span><span class="sxs-lookup"><span data-stu-id="8e337-150">Synthetic</span></span></p></li>
<li><p><span data-ttu-id="8e337-151">Транзакции</span><span class="sxs-lookup"><span data-stu-id="8e337-151">Transaction</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e337-152"><strong>Обработка</strong></span><span class="sxs-lookup"><span data-stu-id="8e337-152"><strong>Processed</strong></span></span></p></td>
<td><p><span data-ttu-id="8e337-153">бит</span><span class="sxs-lookup"><span data-stu-id="8e337-153">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="8e337-154">Внутреннее поле, используемое службой мониторинга.</span><span class="sxs-lookup"><span data-stu-id="8e337-154">Internal field used by the Monitoring service.</span></span></p>
<p><span data-ttu-id="8e337-155">Это поле было введено в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="8e337-155">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8e337-156">\* Для большинства сеансов для SessionIdSeq будет задано значение 1.</span><span class="sxs-lookup"><span data-stu-id="8e337-156">\* For most sessions, SessionIdSeq will have the value of 1.</span></span> <span data-ttu-id="8e337-157">Если два сеанса начинаются в одно и то же время, SessionIdSeq для одного из них будет равен 1, а для другого — 2 и т. д.</span><span class="sxs-lookup"><span data-stu-id="8e337-157">If two sessions start at exactly the same time, the SessionIdSeq for one will be 1, and for the other will be 2, and so on.</span></span>

<span data-ttu-id="8e337-158"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8e337-158"></div>

<span> </span>

</div>

</div>

</span></span></div>

