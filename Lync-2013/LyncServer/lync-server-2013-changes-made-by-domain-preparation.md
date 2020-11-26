---
title: 'Lync Server 2013: изменения, внесенные с помощью подготовки домена'
description: 'Lync Server 2013: изменения, внесенные с помощью подготовки домена.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Changes made by domain preparation
ms:assetid: 9191221e-6166-4c2b-837e-fa73d90fdf80
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398742(v=OCS.15)
ms:contentKeyID: 48184845
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 26400bd1c72c6ae3b8dc1f2d2d8f6c6906b80595
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435119"
---
# <a name="changes-made-by-domain-preparation-in-lync-server-2013"></a><span data-ttu-id="a5bd4-103">Изменения, внесенные в ходе подготовки домена в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a5bd4-103">Changes made by domain preparation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a5bd4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a5bd4-104">

<span> </span></span></span>

<span data-ttu-id="a5bd4-105">_**Тема последнего изменения:** 2010-10-18_</span><span class="sxs-lookup"><span data-stu-id="a5bd4-105">_**Topic Last Modified:** 2010-10-18_</span></span>

<span data-ttu-id="a5bd4-106">В следующей таблице перечислены записи управления доступом (ACE), которые подготовка домена создает в корне домена.</span><span class="sxs-lookup"><span data-stu-id="a5bd4-106">The following table lists the access control entries (ACEs) that domain preparation creates on the domain root.</span></span> <span data-ttu-id="a5bd4-107">Все ACE наследуются, если не указано иное.</span><span class="sxs-lookup"><span data-stu-id="a5bd4-107">All ACEs are inherited unless otherwise noted.</span></span>

<div id="sectionSection0" class="section">

### <a name="aces-added-to-domain-root"></a><span data-ttu-id="a5bd4-108">ACE, добавленные в корень домена</span><span class="sxs-lookup"><span data-stu-id="a5bd4-108">ACEs Added to Domain Root</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a5bd4-109">РЕЗУЛЬТИРУЮЩ</span><span class="sxs-lookup"><span data-stu-id="a5bd4-109">ACE</span></span></th>
<th><span data-ttu-id="a5bd4-110">RTCUniversal — UserReadOnly-Group</span><span class="sxs-lookup"><span data-stu-id="a5bd4-110">RTCUniversal-UserReadOnly-Group</span></span></th>
<th><span data-ttu-id="a5bd4-111">RTCUniversal — ServerReadOnly-Group</span><span class="sxs-lookup"><span data-stu-id="a5bd4-111">RTCUniversal-ServerReadOnly-Group</span></span></th>
<th><span data-ttu-id="a5bd4-112">RTCUniversal-UserAdmins</span><span class="sxs-lookup"><span data-stu-id="a5bd4-112">RTCUniversal-UserAdmins</span></span></th>
<th><span data-ttu-id="a5bd4-113">RTCHSUniversal-Services</span><span class="sxs-lookup"><span data-stu-id="a5bd4-113">RTCHSUniversal-Services</span></span></th>
<th><span data-ttu-id="a5bd4-114">Authenticated-Users</span><span class="sxs-lookup"><span data-stu-id="a5bd4-114">Authenticated-Users</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a5bd4-115">Прочитать контейнер (не наследуется)</span><span class="sxs-lookup"><span data-stu-id="a5bd4-115">Read Container (not inherited)</span></span></p></td>
<td><p><span data-ttu-id="a5bd4-116"><strong>Да</strong></span><span class="sxs-lookup"><span data-stu-id="a5bd4-116"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="a5bd4-117"><strong>Да</strong></span><span class="sxs-lookup"><span data-stu-id="a5bd4-117"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="a5bd4-118">Нет</span><span class="sxs-lookup"><span data-stu-id="a5bd4-118">No</span></span></p></td>
<td><p><span data-ttu-id="a5bd4-119">Нет</span><span class="sxs-lookup"><span data-stu-id="a5bd4-119">No</span></span></p></td>
<td><p><span data-ttu-id="a5bd4-120">Нет</span><span class="sxs-lookup"><span data-stu-id="a5bd4-120">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a5bd4-121">Чтение пользовательских свойств в пользовательском интерфейсе — ограничения для учетных записей</span><span class="sxs-lookup"><span data-stu-id="a5bd4-121">Read User PropertySet User-Account-Restrictions</span></span></p></td>
<td><p><span data-ttu-id="a5bd4-122"><strong>Да</strong></span><span class="sxs-lookup"><span data-stu-id="a5bd4-122"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="a5bd4-123">Нет</span><span class="sxs-lookup"><span data-stu-id="a5bd4-123">No</span></span></p></td>
<td><p><span data-ttu-id="a5bd4-124">Нет</span><span class="sxs-lookup"><span data-stu-id="a5bd4-124">No</span></span></p></td>
<td><p><span data-ttu-id="a5bd4-125">Нет</span><span class="sxs-lookup"><span data-stu-id="a5bd4-125">No</span></span></p></td>
<td><p><span data-ttu-id="a5bd4-126">Нет</span><span class="sxs-lookup"><span data-stu-id="a5bd4-126">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a5bd4-127">Чтение Personal-Information свойств пользователя</span><span class="sxs-lookup"><span data-stu-id="a5bd4-127">Read User PropertySet Personal-Information</span></span></p></td>
<td><p><span data-ttu-id="a5bd4-128"><strong>Да</strong></span><span class="sxs-lookup"><span data-stu-id="a5bd4-128"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="a5bd4-129">Нет</span><span class="sxs-lookup"><span data-stu-id="a5bd4-129">No</span></span></p></td>
<td><p><span data-ttu-id="a5bd4-130">Нет</span><span class="sxs-lookup"><span data-stu-id="a5bd4-130">No</span></span></p></td>
<td><p><span data-ttu-id="a5bd4-131">Нет</span><span class="sxs-lookup"><span data-stu-id="a5bd4-131">No</span></span></p></td>
<td><p><span data-ttu-id="a5bd4-132">Нет</span><span class="sxs-lookup"><span data-stu-id="a5bd4-132">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a5bd4-133">Чтение General-Information свойств пользователя</span><span class="sxs-lookup"><span data-stu-id="a5bd4-133">Read User PropertySet General-Information</span></span></p></td>
<td><p><span data-ttu-id="a5bd4-134"><strong>Да</strong></span><span class="sxs-lookup"><span data-stu-id="a5bd4-134"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="a5bd4-135">Нет</span><span class="sxs-lookup"><span data-stu-id="a5bd4-135">No</span></span></p></td>
<td><p><span data-ttu-id="a5bd4-136">Нет</span><span class="sxs-lookup"><span data-stu-id="a5bd4-136">No</span></span></p></td>
<td><p><span data-ttu-id="a5bd4-137">Нет</span><span class="sxs-lookup"><span data-stu-id="a5bd4-137">No</span></span></p></td>
<td><p><span data-ttu-id="a5bd4-138">Нет</span><span class="sxs-lookup"><span data-stu-id="a5bd4-138">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a5bd4-139">Чтение Public-Information свойств пользователя</span><span class="sxs-lookup"><span data-stu-id="a5bd4-139">Read User PropertySet Public-Information</span></span></p></td>
<td><p><span data-ttu-id="a5bd4-140"><strong>Да</strong></span><span class="sxs-lookup"><span data-stu-id="a5bd4-140"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="a5bd4-141">Нет</span><span class="sxs-lookup"><span data-stu-id="a5bd4-141">No</span></span></p></td>
<td><p><span data-ttu-id="a5bd4-142">Нет</span><span class="sxs-lookup"><span data-stu-id="a5bd4-142">No</span></span></p></td>
<td><p><span data-ttu-id="a5bd4-143">Нет</span><span class="sxs-lookup"><span data-stu-id="a5bd4-143">No</span></span></p></td>
<td><p><span data-ttu-id="a5bd4-144">Нет</span><span class="sxs-lookup"><span data-stu-id="a5bd4-144">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a5bd4-145">Чтение RTCUserSearchProperty-Set свойств пользователя</span><span class="sxs-lookup"><span data-stu-id="a5bd4-145">Read User PropertySet RTCUserSearchProperty-Set</span></span></p></td>
<td><p><span data-ttu-id="a5bd4-146"><strong>Да</strong></span><span class="sxs-lookup"><span data-stu-id="a5bd4-146"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="a5bd4-147">Нет</span><span class="sxs-lookup"><span data-stu-id="a5bd4-147">No</span></span></p></td>
<td><p><span data-ttu-id="a5bd4-148">Нет</span><span class="sxs-lookup"><span data-stu-id="a5bd4-148">No</span></span></p></td>
<td><p><span data-ttu-id="a5bd4-149">Нет</span><span class="sxs-lookup"><span data-stu-id="a5bd4-149">No</span></span></p></td>
<td><p><span data-ttu-id="a5bd4-150"><strong>Да</strong></span><span class="sxs-lookup"><span data-stu-id="a5bd4-150"><strong>Yes</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a5bd4-151">Чтение RTCPropertySet свойств пользователя</span><span class="sxs-lookup"><span data-stu-id="a5bd4-151">Read User PropertySet RTCPropertySet</span></span></p></td>
<td><p><span data-ttu-id="a5bd4-152"><strong>Да</strong></span><span class="sxs-lookup"><span data-stu-id="a5bd4-152"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="a5bd4-153">Нет</span><span class="sxs-lookup"><span data-stu-id="a5bd4-153">No</span></span></p></td>
<td><p><span data-ttu-id="a5bd4-154">Нет</span><span class="sxs-lookup"><span data-stu-id="a5bd4-154">No</span></span></p></td>
<td><p><span data-ttu-id="a5bd4-155">Нет</span><span class="sxs-lookup"><span data-stu-id="a5bd4-155">No</span></span></p></td>
<td><p><span data-ttu-id="a5bd4-156">Нет</span><span class="sxs-lookup"><span data-stu-id="a5bd4-156">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a5bd4-157">Запись Proxy-Addresses свойств пользователя</span><span class="sxs-lookup"><span data-stu-id="a5bd4-157">Write User Property Proxy-Addresses</span></span></p></td>
<td><p><span data-ttu-id="a5bd4-158">Нет</span><span class="sxs-lookup"><span data-stu-id="a5bd4-158">No</span></span></p></td>
<td><p><span data-ttu-id="a5bd4-159">Нет</span><span class="sxs-lookup"><span data-stu-id="a5bd4-159">No</span></span></p></td>
<td><p><span data-ttu-id="a5bd4-160"><strong>Да</strong></span><span class="sxs-lookup"><span data-stu-id="a5bd4-160"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="a5bd4-161">Нет</span><span class="sxs-lookup"><span data-stu-id="a5bd4-161">No</span></span></p></td>
<td><p><span data-ttu-id="a5bd4-162">Нет</span><span class="sxs-lookup"><span data-stu-id="a5bd4-162">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a5bd4-163">Написание RTCUserSearchProperty-Set свойств пользователя</span><span class="sxs-lookup"><span data-stu-id="a5bd4-163">Write User PropertySet RTCUserSearchProperty-Set</span></span></p></td>
<td><p><span data-ttu-id="a5bd4-164">Нет</span><span class="sxs-lookup"><span data-stu-id="a5bd4-164">No</span></span></p></td>
<td><p><span data-ttu-id="a5bd4-165">Нет</span><span class="sxs-lookup"><span data-stu-id="a5bd4-165">No</span></span></p></td>
<td><p><span data-ttu-id="a5bd4-166"><strong>Да</strong></span><span class="sxs-lookup"><span data-stu-id="a5bd4-166"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="a5bd4-167">Нет</span><span class="sxs-lookup"><span data-stu-id="a5bd4-167">No</span></span></p></td>
<td><p><span data-ttu-id="a5bd4-168">Нет</span><span class="sxs-lookup"><span data-stu-id="a5bd4-168">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a5bd4-169">Написание пользовательского свойства RTCPropertySet</span><span class="sxs-lookup"><span data-stu-id="a5bd4-169">Write User PropertySet RTCPropertySet</span></span></p></td>
<td><p><span data-ttu-id="a5bd4-170">Нет</span><span class="sxs-lookup"><span data-stu-id="a5bd4-170">No</span></span></p></td>
<td><p><span data-ttu-id="a5bd4-171">Нет</span><span class="sxs-lookup"><span data-stu-id="a5bd4-171">No</span></span></p></td>
<td><p><span data-ttu-id="a5bd4-172"><strong>Да</strong></span><span class="sxs-lookup"><span data-stu-id="a5bd4-172"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="a5bd4-173">Нет</span><span class="sxs-lookup"><span data-stu-id="a5bd4-173">No</span></span></p></td>
<td><p><span data-ttu-id="a5bd4-174">Нет</span><span class="sxs-lookup"><span data-stu-id="a5bd4-174">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a5bd4-175">Чтение набора свойств DS-репликация — получение изменений для всех объектов Active Directory</span><span class="sxs-lookup"><span data-stu-id="a5bd4-175">Read PropertySet DS-Replication-Get-Changes of all Active Directory objects</span></span></p></td>
<td><p><span data-ttu-id="a5bd4-176">Нет</span><span class="sxs-lookup"><span data-stu-id="a5bd4-176">No</span></span></p></td>
<td><p><span data-ttu-id="a5bd4-177">Нет</span><span class="sxs-lookup"><span data-stu-id="a5bd4-177">No</span></span></p></td>
<td><p><span data-ttu-id="a5bd4-178">Нет</span><span class="sxs-lookup"><span data-stu-id="a5bd4-178">No</span></span></p></td>
<td><p><span data-ttu-id="a5bd4-179"><strong>Да</strong></span><span class="sxs-lookup"><span data-stu-id="a5bd4-179"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="a5bd4-180">Нет</span><span class="sxs-lookup"><span data-stu-id="a5bd4-180">No</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a5bd4-181">В следующей таблице перечислены записи ACE, которые подготовка домена создает в трех встроенных контейнерах: пользователи, компьютеры и контроллеры домена.</span><span class="sxs-lookup"><span data-stu-id="a5bd4-181">The following table lists the ACEs that domain preparation creates in the three built-in containers: Users, Computers, and Domain Controllers.</span></span> <span data-ttu-id="a5bd4-182">Все ACE наследуются, если не указано иное.</span><span class="sxs-lookup"><span data-stu-id="a5bd4-182">All ACEs are inherited unless otherwise noted.</span></span>

### <a name="aces-added-to-built-in-containers"></a><span data-ttu-id="a5bd4-183">ACE, добавленные в встроенные контейнеры</span><span class="sxs-lookup"><span data-stu-id="a5bd4-183">ACEs Added to Built-in Containers</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a5bd4-184">РЕЗУЛЬТИРУЮЩ</span><span class="sxs-lookup"><span data-stu-id="a5bd4-184">ACE</span></span></th>
<th><span data-ttu-id="a5bd4-185">RTCUniversal — UserReadOnly-Group</span><span class="sxs-lookup"><span data-stu-id="a5bd4-185">RTCUniversal-UserReadOnly-Group</span></span></th>
<th><span data-ttu-id="a5bd4-186">RTCUniversal — ServerReadOnly-Group</span><span class="sxs-lookup"><span data-stu-id="a5bd4-186">RTCUniversal-ServerReadOnly-Group</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a5bd4-187">Прочитать контейнер (не наследуется)</span><span class="sxs-lookup"><span data-stu-id="a5bd4-187">Read Container (not inherited)</span></span></p></td>
<td><p><span data-ttu-id="a5bd4-188"><strong>Да</strong></span><span class="sxs-lookup"><span data-stu-id="a5bd4-188"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="a5bd4-189"><strong>Да</strong></span><span class="sxs-lookup"><span data-stu-id="a5bd4-189"><strong>Yes</strong></span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="a5bd4-190">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a5bd4-190">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

