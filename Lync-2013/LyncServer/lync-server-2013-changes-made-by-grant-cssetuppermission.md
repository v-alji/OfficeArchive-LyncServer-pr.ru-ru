---
title: 'Lync Server 2013: изменения, внесенные Grant-CsSetupPermission'
description: 'Lync Server 2013: изменения, внесенные функцией Grant-CsSetupPermission.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Changes made by Grant-CsSetupPermission
ms:assetid: c5801f48-14e3-4fdd-8f14-d52e7af07a57
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205250(v=OCS.15)
ms:contentKeyID: 48185360
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d2a9156c977c993dd32e38fc6816bd08d3f65c1f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435070"
---
# <a name="changes-made-by-grant-cssetuppermission-in-lync-server-2013"></a><span data-ttu-id="508e7-103">Изменения, внесенные в Grant-CsSetupPermission в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="508e7-103">Changes made by Grant-CsSetupPermission in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="508e7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="508e7-104">

<span> </span></span></span>

<span data-ttu-id="508e7-105">_**Тема последнего изменения:** 2012-06-20_</span><span class="sxs-lookup"><span data-stu-id="508e7-105">_**Topic Last Modified:** 2012-06-20_</span></span>

<span data-ttu-id="508e7-106">Для делегирования настройки вы можете предоставить разрешения на доступ к универсальной группе RTCUniversalServerAdmins для определенного подразделения Active Directory (OU), включив в него членов группы RTCUniversalServerAdmins, чтобы установить Lync Server 2013 в указанный домен, не добавив в него пользователей, которые не входят в группу "Администраторы домена".</span><span class="sxs-lookup"><span data-stu-id="508e7-106">To delegate setup, you can grant permissions to the RTCUniversalServerAdmins universal group for a specific Active Directory organizational unit (OU), enabling members of the RTCUniversalServerAdmins group in that OU to install Lync Server 2013 in the specified domain without being members of the Domain Admins group.</span></span>

<span data-ttu-id="508e7-107">Командлет **Grant-CsSetupPermission** предоставляет разрешения на доступ к группе RTCUniversalServerAdmins на подразделение, как указано в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="508e7-107">The **Grant-CsSetupPermission** cmdlet grants the RTCUniversalServerAdmins group permissions on an OU, as specified in the following table:</span></span>

### <a name="permissions-granted-to-objects-in-the-ou"></a><span data-ttu-id="508e7-108">Разрешения, предоставленные объектам в подразделении</span><span class="sxs-lookup"><span data-stu-id="508e7-108">Permissions granted to Objects in the OU</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="508e7-109">Разрешения применяются к:</span><span class="sxs-lookup"><span data-stu-id="508e7-109">Permissions apply to:</span></span></th>
<th><span data-ttu-id="508e7-110">Предоставлены следующие разрешения:</span><span class="sxs-lookup"><span data-stu-id="508e7-110">Permissions granted are:</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="508e7-111">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="508e7-111">RTCUniversalServerAdmins</span></span></p></td>
<td><p><span data-ttu-id="508e7-112">Специальный доступ:</span><span class="sxs-lookup"><span data-stu-id="508e7-112">Special access:</span></span></p>
<ul>
<li><p><span data-ttu-id="508e7-113">Чтение передаваемые по себе</span><span class="sxs-lookup"><span data-stu-id="508e7-113">Read servicePrincipalName</span></span></p></li>
<li><p><span data-ttu-id="508e7-114">Вводный текст</span><span class="sxs-lookup"><span data-stu-id="508e7-114">Write servicePrincipalName</span></span></p></li>
<li><p><span data-ttu-id="508e7-115">Удалить дерево</span><span class="sxs-lookup"><span data-stu-id="508e7-115">Delete tree</span></span></p></li>
<li><p><span data-ttu-id="508e7-116">Репликация изменений каталога</span><span class="sxs-lookup"><span data-stu-id="508e7-116">Replicating directory changes</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="508e7-117">Дочерние объекты serviceConnectionPoint</span><span class="sxs-lookup"><span data-stu-id="508e7-117">Descendant serviceConnectionPoint objects</span></span></p></td>
<td><p><span data-ttu-id="508e7-118">Специальный доступ:</span><span class="sxs-lookup"><span data-stu-id="508e7-118">Special access:</span></span></p>
<ul>
<li><p><span data-ttu-id="508e7-119">Разрешения на чтение</span><span class="sxs-lookup"><span data-stu-id="508e7-119">Read permissions</span></span></p></li>
<li><p><span data-ttu-id="508e7-120">Разрешения на запись</span><span class="sxs-lookup"><span data-stu-id="508e7-120">Write permissions</span></span></p></li>
<li><p><span data-ttu-id="508e7-121">Создание дочернего элемента</span><span class="sxs-lookup"><span data-stu-id="508e7-121">Create child</span></span></p></li>
<li><p><span data-ttu-id="508e7-122">Удалить дочерний элемент</span><span class="sxs-lookup"><span data-stu-id="508e7-122">Delete child</span></span></p></li>
<li><p><span data-ttu-id="508e7-123">Содержимое списка</span><span class="sxs-lookup"><span data-stu-id="508e7-123">List contents</span></span></p></li>
<li><p><span data-ttu-id="508e7-124">Запись свойства</span><span class="sxs-lookup"><span data-stu-id="508e7-124">Write property</span></span></p></li>
<li><p><span data-ttu-id="508e7-125">Чтение свойства</span><span class="sxs-lookup"><span data-stu-id="508e7-125">Read property</span></span></p></li>
<li><p><span data-ttu-id="508e7-126">Удалить дерево</span><span class="sxs-lookup"><span data-stu-id="508e7-126">Delete tree</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="508e7-127">Дочерние объекты msRTCSIP-Server</span><span class="sxs-lookup"><span data-stu-id="508e7-127">Descendant msRTCSIP-Server objects</span></span></p></td>
<td><p><span data-ttu-id="508e7-128">Специальный доступ:</span><span class="sxs-lookup"><span data-stu-id="508e7-128">Special access:</span></span></p>
<ul>
<li><p><span data-ttu-id="508e7-129">Запись свойства</span><span class="sxs-lookup"><span data-stu-id="508e7-129">Write property</span></span></p></li>
<li><p><span data-ttu-id="508e7-130">Чтение свойства</span><span class="sxs-lookup"><span data-stu-id="508e7-130">Read property</span></span></p></li>
<li><p><span data-ttu-id="508e7-131">Удалить дерево</span><span class="sxs-lookup"><span data-stu-id="508e7-131">Delete tree</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="508e7-132">Дочерние msRTCSIP — объекты-компоненты</span><span class="sxs-lookup"><span data-stu-id="508e7-132">Descendant msRTCSIP-WebComponents objects</span></span></p></td>
<td><p><span data-ttu-id="508e7-133">Специальный доступ:</span><span class="sxs-lookup"><span data-stu-id="508e7-133">Special access:</span></span></p>
<ul>
<li><p><span data-ttu-id="508e7-134">Запись свойства</span><span class="sxs-lookup"><span data-stu-id="508e7-134">Write property</span></span></p></li>
<li><p><span data-ttu-id="508e7-135">Чтение свойства</span><span class="sxs-lookup"><span data-stu-id="508e7-135">Read property</span></span></p></li>
<li><p><span data-ttu-id="508e7-136">Удалить дерево</span><span class="sxs-lookup"><span data-stu-id="508e7-136">Delete tree</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="508e7-137">Дочерние объекты msRTCSIP-MCU</span><span class="sxs-lookup"><span data-stu-id="508e7-137">Descendant msRTCSIP-MCU objects</span></span></p></td>
<td><p><span data-ttu-id="508e7-138">Специальный доступ:</span><span class="sxs-lookup"><span data-stu-id="508e7-138">Special access:</span></span></p>
<ul>
<li><p><span data-ttu-id="508e7-139">Запись свойства</span><span class="sxs-lookup"><span data-stu-id="508e7-139">Write property</span></span></p></li>
<li><p><span data-ttu-id="508e7-140">Чтение свойства</span><span class="sxs-lookup"><span data-stu-id="508e7-140">Read property</span></span></p></li>
<li><p><span data-ttu-id="508e7-141">Удалить дерево</span><span class="sxs-lookup"><span data-stu-id="508e7-141">Delete tree</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="508e7-142">Дочерние объекты msRTCSIP-MediationServer</span><span class="sxs-lookup"><span data-stu-id="508e7-142">Descendant msRTCSIP-MediationServer objects</span></span></p></td>
<td><p><span data-ttu-id="508e7-143">Специальный доступ:</span><span class="sxs-lookup"><span data-stu-id="508e7-143">Special access:</span></span></p>
<ul>
<li><p><span data-ttu-id="508e7-144">Запись свойства</span><span class="sxs-lookup"><span data-stu-id="508e7-144">Write property</span></span></p></li>
<li><p><span data-ttu-id="508e7-145">Чтение свойства</span><span class="sxs-lookup"><span data-stu-id="508e7-145">Read property</span></span></p></li>
<li><p><span data-ttu-id="508e7-146">Удалить дерево</span><span class="sxs-lookup"><span data-stu-id="508e7-146">Delete tree</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="508e7-147">Дочерние объекты msRTCSIP-ApplicationServer</span><span class="sxs-lookup"><span data-stu-id="508e7-147">Descendant msRTCSIP-ApplicationServer objects</span></span></p></td>
<td><p><span data-ttu-id="508e7-148">Специальный доступ:</span><span class="sxs-lookup"><span data-stu-id="508e7-148">Special access:</span></span></p>
<ul>
<li><p><span data-ttu-id="508e7-149">Запись свойства</span><span class="sxs-lookup"><span data-stu-id="508e7-149">Write property</span></span></p></li>
<li><p><span data-ttu-id="508e7-150">Чтение свойства</span><span class="sxs-lookup"><span data-stu-id="508e7-150">Read property</span></span></p></li>
<li><p><span data-ttu-id="508e7-151">Удалить дерево</span><span class="sxs-lookup"><span data-stu-id="508e7-151">Delete tree</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="508e7-152">Дочерние объекты msRTCSIP-ConnectionPoint</span><span class="sxs-lookup"><span data-stu-id="508e7-152">Descendant msRTCSIP-ConnectionPoint objects</span></span></p></td>
<td><p><span data-ttu-id="508e7-153">Специальный доступ:</span><span class="sxs-lookup"><span data-stu-id="508e7-153">Special access:</span></span></p>
<ul>
<li><p><span data-ttu-id="508e7-154">Запись свойства</span><span class="sxs-lookup"><span data-stu-id="508e7-154">Write property</span></span></p></li>
<li><p><span data-ttu-id="508e7-155">Чтение свойства</span><span class="sxs-lookup"><span data-stu-id="508e7-155">Read property</span></span></p></li>
<li><p><span data-ttu-id="508e7-156">Удалить дерево</span><span class="sxs-lookup"><span data-stu-id="508e7-156">Delete tree</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="508e7-157">Дочерние объекты компьютера</span><span class="sxs-lookup"><span data-stu-id="508e7-157">Descendant Computer objects</span></span></p></td>
<td><p><span data-ttu-id="508e7-158">Специальный доступ для serviceConnectionPoint:</span><span class="sxs-lookup"><span data-stu-id="508e7-158">Special access for serviceConnectionPoint:</span></span></p>
<ul>
<li><p><span data-ttu-id="508e7-159">Создание дочерних объектов</span><span class="sxs-lookup"><span data-stu-id="508e7-159">Create child objects</span></span></p></li>
<li><p><span data-ttu-id="508e7-160">Удаление дочерних объектов</span><span class="sxs-lookup"><span data-stu-id="508e7-160">Delete child objects</span></span></p></li>
<li><p><span data-ttu-id="508e7-161">Удалить дерево</span><span class="sxs-lookup"><span data-stu-id="508e7-161">Delete tree</span></span></p></li>
</ul>
<p><span data-ttu-id="508e7-162">Специальный доступ к общедоступным сведениям:</span><span class="sxs-lookup"><span data-stu-id="508e7-162">Special access for public information:</span></span></p>
<ul>
<li><p><span data-ttu-id="508e7-163">Чтение свойства</span><span class="sxs-lookup"><span data-stu-id="508e7-163">Read property</span></span></p></li>
</ul>
<p><span data-ttu-id="508e7-164">Особый доступ для DNS-имени узла:</span><span class="sxs-lookup"><span data-stu-id="508e7-164">Special access for DNS host name:</span></span></p>
<ul>
<li><p><span data-ttu-id="508e7-165">Чтение свойства</span><span class="sxs-lookup"><span data-stu-id="508e7-165">Read property</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table><span data-ttu-id="508e7-166">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="508e7-166">


</div>

<span> </span>

</div>

</div>

</span></span></div>

