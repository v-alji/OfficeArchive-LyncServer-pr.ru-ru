---
title: 'Lync Server 2013: изменения, внесенные Grant-CsOUPermission'
description: 'Lync Server 2013: изменения, внесенные функцией Grant-CsOUPermission.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Changes made by Grant-CsOUPermission
ms:assetid: d744d352-1ad9-4447-8e2b-28e768d2ed1b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205310(v=OCS.15)
ms:contentKeyID: 48185564
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 10d3db0e9dde380628690bc016e2b4bd2ec85b54
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435056"
---
# <a name="changes-made-by-grant-csoupermission-in-lync-server-2013"></a><span data-ttu-id="a777a-103">Изменения, внесенные в Grant-CsOUPermission в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a777a-103">Changes made by Grant-CsOUPermission in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a777a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a777a-104">

<span> </span></span></span>

<span data-ttu-id="a777a-105">_**Тема последнего изменения:** 2012-06-20_</span><span class="sxs-lookup"><span data-stu-id="a777a-105">_**Topic Last Modified:** 2012-06-20_</span></span>

<span data-ttu-id="a777a-106">Чтобы делегировать администрирование Lync Server 2013, вы можете добавить разрешения для указанных организационных подразделений, чтобы участники универсальных групп RTC, созданные с помощью подготовки леса, могли получать доступ к подразделениям без участия в группе Администраторы домена.</span><span class="sxs-lookup"><span data-stu-id="a777a-106">To delegate Lync Server 2013 administration, you can add permissions to specified organizational units (OUs) so that members of the RTC universal groups created by forest preparation can access the OUs without being members of the Domain Admins group.</span></span>

<span data-ttu-id="a777a-107">Командлет **Grant-CsOuPermission** предоставляет разрешения на доступ к объектам в указанном подразделении, как указано в приведенных ниже таблицах.</span><span class="sxs-lookup"><span data-stu-id="a777a-107">The **Grant-CsOuPermission** cmdlet grants permissions to objects in the specified OU as specified in the following tables.</span></span>

<div>

## <a name="granting-permission-for-user-objects"></a><span data-ttu-id="a777a-108">Предоставление разрешений для объектов пользователей</span><span class="sxs-lookup"><span data-stu-id="a777a-108">Granting Permission for User Objects</span></span>

<span data-ttu-id="a777a-109">Когда вы запускаете командлет **Grant-CsOuPermission** для объектов пользователей в подразделении, группам предоставляются разрешения, как показано в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="a777a-109">When you run the **Grant-CsOuPermission** cmdlet for User objects on an OU, groups are granted permissions as shown in the following table.</span></span>

### <a name="permissions-granted-for-user-objects"></a><span data-ttu-id="a777a-110">Разрешения, предоставленные для объектов пользователя</span><span class="sxs-lookup"><span data-stu-id="a777a-110">Permissions Granted for User Objects</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a777a-111">Сгруппирован</span><span class="sxs-lookup"><span data-stu-id="a777a-111">Group</span></span></th>
<th><span data-ttu-id="a777a-112">PermissionSet</span><span class="sxs-lookup"><span data-stu-id="a777a-112">Permission</span></span></th>
<th><span data-ttu-id="a777a-113">Применимо к</span><span class="sxs-lookup"><span data-stu-id="a777a-113">Applies to</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a777a-114">RTCHSUniversalServices</span><span class="sxs-lookup"><span data-stu-id="a777a-114">RTCHSUniversalServices</span></span></p></td>
<td><p><span data-ttu-id="a777a-115">Репликация изменений каталога</span><span class="sxs-lookup"><span data-stu-id="a777a-115">Replicating directory changes</span></span></p></td>
<td><p><span data-ttu-id="a777a-116">Только этот объект</span><span class="sxs-lookup"><span data-stu-id="a777a-116">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a777a-117">RTCUniversalServerReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="a777a-117">RTCUniversalServerReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="a777a-118">Содержимое списка</span><span class="sxs-lookup"><span data-stu-id="a777a-118">List contents</span></span></p>
<p><span data-ttu-id="a777a-119">Чтение всех свойств</span><span class="sxs-lookup"><span data-stu-id="a777a-119">Read all properties</span></span></p>
<p><span data-ttu-id="a777a-120">Разрешения на чтение</span><span class="sxs-lookup"><span data-stu-id="a777a-120">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="a777a-121">Только этот объект</span><span class="sxs-lookup"><span data-stu-id="a777a-121">This object only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a777a-122">RTCUniversalUserReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="a777a-122">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="a777a-123">Содержимое списка</span><span class="sxs-lookup"><span data-stu-id="a777a-123">List contents</span></span></p>
<p><span data-ttu-id="a777a-124">Чтение всех свойств</span><span class="sxs-lookup"><span data-stu-id="a777a-124">Read all properties</span></span></p>
<p><span data-ttu-id="a777a-125">Разрешения на чтение</span><span class="sxs-lookup"><span data-stu-id="a777a-125">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="a777a-126">Только этот объект</span><span class="sxs-lookup"><span data-stu-id="a777a-126">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a777a-127">RTCUniversalUserReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="a777a-127">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="a777a-128">Прочитать RTCUserSearchPropertySet</span><span class="sxs-lookup"><span data-stu-id="a777a-128">Read RTCUserSearchPropertySet</span></span></p>
<p><span data-ttu-id="a777a-129">Прочитать RTCUserProvisioningPropertySet</span><span class="sxs-lookup"><span data-stu-id="a777a-129">Read RTCUserProvisioningPropertySet</span></span></p>
<p><span data-ttu-id="a777a-130">Прочитать RTCPropertySet</span><span class="sxs-lookup"><span data-stu-id="a777a-130">Read RTCPropertySet</span></span></p>
<p><span data-ttu-id="a777a-131">Чтение Public-Information</span><span class="sxs-lookup"><span data-stu-id="a777a-131">Read Public-Information</span></span></p>
<p><span data-ttu-id="a777a-132">Чтение General-Information</span><span class="sxs-lookup"><span data-stu-id="a777a-132">Read General-Information</span></span></p>
<p><span data-ttu-id="a777a-133">Чтение ограничений для учетных записей пользователей</span><span class="sxs-lookup"><span data-stu-id="a777a-133">Read User-Account-Restrictions</span></span></p></td>
<td><p><span data-ttu-id="a777a-134">Дочерние объекты пользователей</span><span class="sxs-lookup"><span data-stu-id="a777a-134">Descendant User objects</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a777a-135">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="a777a-135">RTCUniversalUserAdmins</span></span></p></td>
<td><p><span data-ttu-id="a777a-136">Напишите RTCUserSearchPropertySet</span><span class="sxs-lookup"><span data-stu-id="a777a-136">Write RTCUserSearchPropertySet</span></span></p>
<p><span data-ttu-id="a777a-137">Напишите msExchUCVoiceMailSettings</span><span class="sxs-lookup"><span data-stu-id="a777a-137">Write msExchUCVoiceMailSettings</span></span></p>
<p><span data-ttu-id="a777a-138">Напишите RTCUserProvisioningPropertySet</span><span class="sxs-lookup"><span data-stu-id="a777a-138">Write RTCUserProvisioningPropertySet</span></span></p>
<p><span data-ttu-id="a777a-139">Напишите RTCPropertySet</span><span class="sxs-lookup"><span data-stu-id="a777a-139">Write RTCPropertySet</span></span></p>
<p><span data-ttu-id="a777a-140">Напишите proxyAddresses</span><span class="sxs-lookup"><span data-stu-id="a777a-140">Write proxyAddresses</span></span></p></td>
<td><p><span data-ttu-id="a777a-141">Дочерние объекты пользователей</span><span class="sxs-lookup"><span data-stu-id="a777a-141">Descendant User objects</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="granting-permission-for-computer-objects"></a><span data-ttu-id="a777a-142">Предоставление разрешений на доступ к объектам компьютера</span><span class="sxs-lookup"><span data-stu-id="a777a-142">Granting Permission for Computer Objects</span></span>

<span data-ttu-id="a777a-143">Когда вы запускаете командлет **Grant-CsOuPermission** для объектов компьютеров в подразделении, группам предоставляются разрешения, как показано в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="a777a-143">When you run the **Grant-CsOuPermission** cmdlet for Computer objects on an OU, groups are granted permissions as shown in the following table.</span></span>

### <a name="permissions-granted-for-computer-objects"></a><span data-ttu-id="a777a-144">Разрешения, предоставленные для объектов компьютера</span><span class="sxs-lookup"><span data-stu-id="a777a-144">Permissions Granted for Computer Objects</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a777a-145">Сгруппирован</span><span class="sxs-lookup"><span data-stu-id="a777a-145">Group</span></span></th>
<th><span data-ttu-id="a777a-146">PermissionSet</span><span class="sxs-lookup"><span data-stu-id="a777a-146">Permission</span></span></th>
<th><span data-ttu-id="a777a-147">Применимо к</span><span class="sxs-lookup"><span data-stu-id="a777a-147">Applies to</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a777a-148">RTCHSUniversalServices</span><span class="sxs-lookup"><span data-stu-id="a777a-148">RTCHSUniversalServices</span></span></p></td>
<td><p><span data-ttu-id="a777a-149">Репликация изменений каталога</span><span class="sxs-lookup"><span data-stu-id="a777a-149">Replicating directory changes</span></span></p></td>
<td><p><span data-ttu-id="a777a-150">Только этот объект</span><span class="sxs-lookup"><span data-stu-id="a777a-150">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a777a-151">RTCUniversalServerReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="a777a-151">RTCUniversalServerReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="a777a-152">Содержимое списка</span><span class="sxs-lookup"><span data-stu-id="a777a-152">List contents</span></span></p>
<p><span data-ttu-id="a777a-153">Чтение всех свойств</span><span class="sxs-lookup"><span data-stu-id="a777a-153">Read all properties</span></span></p>
<p><span data-ttu-id="a777a-154">Разрешения на чтение</span><span class="sxs-lookup"><span data-stu-id="a777a-154">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="a777a-155">Только этот объект</span><span class="sxs-lookup"><span data-stu-id="a777a-155">This object only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a777a-156">RTCUniversalUserReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="a777a-156">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="a777a-157">Содержимое списка</span><span class="sxs-lookup"><span data-stu-id="a777a-157">List contents</span></span></p>
<p><span data-ttu-id="a777a-158">Чтение всех свойств</span><span class="sxs-lookup"><span data-stu-id="a777a-158">Read all properties</span></span></p>
<p><span data-ttu-id="a777a-159">Разрешения на чтение</span><span class="sxs-lookup"><span data-stu-id="a777a-159">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="a777a-160">Только этот объект</span><span class="sxs-lookup"><span data-stu-id="a777a-160">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a777a-161">RTCUniversalUserReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="a777a-161">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="a777a-162">Чтение Public-Information</span><span class="sxs-lookup"><span data-stu-id="a777a-162">Read Public-Information</span></span></p>
<p><span data-ttu-id="a777a-163">Проверка на прочтении DNS-Host-Name</span><span class="sxs-lookup"><span data-stu-id="a777a-163">Read Validated-DNS-Host-Name</span></span></p></td>
<td><p><span data-ttu-id="a777a-164">Дочерние объекты компьютера</span><span class="sxs-lookup"><span data-stu-id="a777a-164">Descendant Computer objects</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a777a-165">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="a777a-165">RTCUniversalUserAdmins</span></span></p></td>
<td><p><span data-ttu-id="a777a-166">Чтение Public-Information</span><span class="sxs-lookup"><span data-stu-id="a777a-166">Read Public-Information</span></span></p>
<p><span data-ttu-id="a777a-167">Проверка на прочтении DNS-Host-Name</span><span class="sxs-lookup"><span data-stu-id="a777a-167">Read Validated-DNS-Host-Name</span></span></p></td>
<td><p><span data-ttu-id="a777a-168">Дочерние объекты компьютера</span><span class="sxs-lookup"><span data-stu-id="a777a-168">Descendant Computer objects</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="granting-permission-for-contact-or-appcontact-objects"></a><span data-ttu-id="a777a-169">Предоставление разрешений на доступ к объектам контакта или AppContact</span><span class="sxs-lookup"><span data-stu-id="a777a-169">Granting Permission for Contact or AppContact Objects</span></span>

<span data-ttu-id="a777a-170">При запуске командлета **Grant-CsOuPermission** для объектов контакта или объектов AppContact в подразделении группам предоставляются разрешения, описанные в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="a777a-170">When you run the **Grant-CsOuPermission** cmdlet for Contact objects or AppContact objects on an OU, groups are granted permissions as shown in the following table.</span></span>

### <a name="permissions-granted-for-contact-or-appcontact-objects"></a><span data-ttu-id="a777a-171">Разрешения, предоставленные для контактных и AppContactных объектов</span><span class="sxs-lookup"><span data-stu-id="a777a-171">Permissions Granted for Contact or AppContact Objects</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a777a-172">Сгруппирован</span><span class="sxs-lookup"><span data-stu-id="a777a-172">Group</span></span></th>
<th><span data-ttu-id="a777a-173">PermissionSet</span><span class="sxs-lookup"><span data-stu-id="a777a-173">Permission</span></span></th>
<th><span data-ttu-id="a777a-174">Применимо к</span><span class="sxs-lookup"><span data-stu-id="a777a-174">Applies to</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a777a-175">RTCHSUniversalServices</span><span class="sxs-lookup"><span data-stu-id="a777a-175">RTCHSUniversalServices</span></span></p></td>
<td><p><span data-ttu-id="a777a-176">Репликация изменений каталога</span><span class="sxs-lookup"><span data-stu-id="a777a-176">Replicating directory changes</span></span></p></td>
<td><p><span data-ttu-id="a777a-177">Только этот объект</span><span class="sxs-lookup"><span data-stu-id="a777a-177">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a777a-178">RTCUniversalServerReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="a777a-178">RTCUniversalServerReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="a777a-179">Содержимое списка</span><span class="sxs-lookup"><span data-stu-id="a777a-179">List contents</span></span></p>
<p><span data-ttu-id="a777a-180">Чтение всех свойств</span><span class="sxs-lookup"><span data-stu-id="a777a-180">Read all properties</span></span></p>
<p><span data-ttu-id="a777a-181">Разрешения на чтение</span><span class="sxs-lookup"><span data-stu-id="a777a-181">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="a777a-182">Только этот объект</span><span class="sxs-lookup"><span data-stu-id="a777a-182">This object only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a777a-183">RTCUniversalUserReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="a777a-183">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="a777a-184">Содержимое списка</span><span class="sxs-lookup"><span data-stu-id="a777a-184">List contents</span></span></p>
<p><span data-ttu-id="a777a-185">Чтение всех свойств</span><span class="sxs-lookup"><span data-stu-id="a777a-185">Read all properties</span></span></p>
<p><span data-ttu-id="a777a-186">Разрешения на чтение</span><span class="sxs-lookup"><span data-stu-id="a777a-186">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="a777a-187">Только этот объект</span><span class="sxs-lookup"><span data-stu-id="a777a-187">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a777a-188">RTCUniversalUserReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="a777a-188">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="a777a-189">Прочитать RTCUserSearchPropertySet</span><span class="sxs-lookup"><span data-stu-id="a777a-189">Read RTCUserSearchPropertySet</span></span></p>
<p><span data-ttu-id="a777a-190">Прочитать RTCUserProvisioningPropertySet</span><span class="sxs-lookup"><span data-stu-id="a777a-190">Read RTCUserProvisioningPropertySet</span></span></p>
<p><span data-ttu-id="a777a-191">Прочитать RTCPropertySet</span><span class="sxs-lookup"><span data-stu-id="a777a-191">Read RTCPropertySet</span></span></p>
<p><span data-ttu-id="a777a-192">Чтение Public-Information</span><span class="sxs-lookup"><span data-stu-id="a777a-192">Read Public-Information</span></span></p>
<p><span data-ttu-id="a777a-193">Чтение General-Information</span><span class="sxs-lookup"><span data-stu-id="a777a-193">Read General-Information</span></span></p>
<p><span data-ttu-id="a777a-194">Чтение Personal-Information</span><span class="sxs-lookup"><span data-stu-id="a777a-194">Read Personal-Information</span></span></p>
<p><span data-ttu-id="a777a-195">Чтение ограничений для учетных записей пользователей</span><span class="sxs-lookup"><span data-stu-id="a777a-195">Read User-Account-Restrictions</span></span></p></td>
<td><p><span data-ttu-id="a777a-196">Дочерние объекты контактов</span><span class="sxs-lookup"><span data-stu-id="a777a-196">Descendant Contact objects</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a777a-197">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="a777a-197">RTCUniversalUserAdmins</span></span></p></td>
<td><p><span data-ttu-id="a777a-198">Напишите RTCUserSearchPropertySet</span><span class="sxs-lookup"><span data-stu-id="a777a-198">Write RTCUserSearchPropertySet</span></span></p>
<p><span data-ttu-id="a777a-199">Напишите otherIpPhone</span><span class="sxs-lookup"><span data-stu-id="a777a-199">Write otherIpPhone</span></span></p>
<p><span data-ttu-id="a777a-200">Запись отображаемого текста</span><span class="sxs-lookup"><span data-stu-id="a777a-200">Write displayName</span></span></p>
<p><span data-ttu-id="a777a-201">Описание записи</span><span class="sxs-lookup"><span data-stu-id="a777a-201">Write description</span></span></p>
<p><span data-ttu-id="a777a-202">Напишите telephoneNumber</span><span class="sxs-lookup"><span data-stu-id="a777a-202">Write telephoneNumber</span></span></p>
<p><span data-ttu-id="a777a-203">Напишите msExchUCVoiceMailSettings</span><span class="sxs-lookup"><span data-stu-id="a777a-203">Write msExchUCVoiceMailSettings</span></span></p>
<p><span data-ttu-id="a777a-204">Напишите RTCUserProvisioningPropertySet</span><span class="sxs-lookup"><span data-stu-id="a777a-204">Write RTCUserProvisioningPropertySet</span></span></p>
<p><span data-ttu-id="a777a-205">Напишите RTCPropertySet</span><span class="sxs-lookup"><span data-stu-id="a777a-205">Write RTCPropertySet</span></span></p>
<p><span data-ttu-id="a777a-206">Напишите proxyAddresses</span><span class="sxs-lookup"><span data-stu-id="a777a-206">Write proxyAddresses</span></span></p></td>
<td><p><span data-ttu-id="a777a-207">Дочерние объекты контактов</span><span class="sxs-lookup"><span data-stu-id="a777a-207">Descendant Contact objects</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="granting-permission-for-device-objects"></a><span data-ttu-id="a777a-208">Предоставление разрешения на доступ к объектам устройства</span><span class="sxs-lookup"><span data-stu-id="a777a-208">Granting Permission for Device Objects</span></span>

<span data-ttu-id="a777a-209">Когда вы запускаете командлет **Grant-CsOuPermission** для объектов устройств в подразделении, группам предоставляются разрешения, как показано в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="a777a-209">When you run the **Grant-CsOuPermission** cmdlet for Device objects on an OU, groups are granted permissions as shown in the following table.</span></span>

### <a name="permissions-granted-for-device-objects"></a><span data-ttu-id="a777a-210">Разрешения, предоставленные для объектов устройства</span><span class="sxs-lookup"><span data-stu-id="a777a-210">Permissions Granted for Device Objects</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a777a-211">Сгруппирован</span><span class="sxs-lookup"><span data-stu-id="a777a-211">Group</span></span></th>
<th><span data-ttu-id="a777a-212">PermissionSet</span><span class="sxs-lookup"><span data-stu-id="a777a-212">Permission</span></span></th>
<th><span data-ttu-id="a777a-213">Применимо к</span><span class="sxs-lookup"><span data-stu-id="a777a-213">Applies to</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a777a-214">RTCHSUniversalServices</span><span class="sxs-lookup"><span data-stu-id="a777a-214">RTCHSUniversalServices</span></span></p></td>
<td><p><span data-ttu-id="a777a-215">Репликация изменений каталога</span><span class="sxs-lookup"><span data-stu-id="a777a-215">Replicating directory changes</span></span></p></td>
<td><p><span data-ttu-id="a777a-216">Только этот объект</span><span class="sxs-lookup"><span data-stu-id="a777a-216">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a777a-217">RTCUniversalServerReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="a777a-217">RTCUniversalServerReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="a777a-218">Содержимое списка</span><span class="sxs-lookup"><span data-stu-id="a777a-218">List contents</span></span></p>
<p><span data-ttu-id="a777a-219">Чтение всех свойств</span><span class="sxs-lookup"><span data-stu-id="a777a-219">Read all properties</span></span></p>
<p><span data-ttu-id="a777a-220">Разрешения на чтение</span><span class="sxs-lookup"><span data-stu-id="a777a-220">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="a777a-221">Только этот объект</span><span class="sxs-lookup"><span data-stu-id="a777a-221">This object only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a777a-222">RTCUniversalUserReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="a777a-222">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="a777a-223">Содержимое списка</span><span class="sxs-lookup"><span data-stu-id="a777a-223">List contents</span></span></p>
<p><span data-ttu-id="a777a-224">Чтение всех свойств</span><span class="sxs-lookup"><span data-stu-id="a777a-224">Read all properties</span></span></p>
<p><span data-ttu-id="a777a-225">Разрешения на чтение</span><span class="sxs-lookup"><span data-stu-id="a777a-225">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="a777a-226">Только этот объект</span><span class="sxs-lookup"><span data-stu-id="a777a-226">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a777a-227">RTCUniversalUserReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="a777a-227">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="a777a-228">Прочитать RTCUserSearchPropertySet</span><span class="sxs-lookup"><span data-stu-id="a777a-228">Read RTCUserSearchPropertySet</span></span></p>
<p><span data-ttu-id="a777a-229">Прочитать RTCUserProvisioningPropertySet</span><span class="sxs-lookup"><span data-stu-id="a777a-229">Read RTCUserProvisioningPropertySet</span></span></p>
<p><span data-ttu-id="a777a-230">Прочитать RTCPropertySet</span><span class="sxs-lookup"><span data-stu-id="a777a-230">Read RTCPropertySet</span></span></p>
<p><span data-ttu-id="a777a-231">Чтение Public-Information</span><span class="sxs-lookup"><span data-stu-id="a777a-231">Read Public-Information</span></span></p>
<p><span data-ttu-id="a777a-232">Чтение Personal-Information</span><span class="sxs-lookup"><span data-stu-id="a777a-232">Read Personal-Information</span></span></p>
<p><span data-ttu-id="a777a-233">Чтение General-Information</span><span class="sxs-lookup"><span data-stu-id="a777a-233">Read General-Information</span></span></p>
<p><span data-ttu-id="a777a-234">Чтение ограничений для учетных записей пользователей</span><span class="sxs-lookup"><span data-stu-id="a777a-234">Read User-Account-Restrictions</span></span></p></td>
<td><p><span data-ttu-id="a777a-235">Дочерние объекты контактов</span><span class="sxs-lookup"><span data-stu-id="a777a-235">Descendant Contact objects</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a777a-236">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="a777a-236">RTCUniversalUserAdmins</span></span></p></td>
<td><p><span data-ttu-id="a777a-237">Создание дочернего элемента</span><span class="sxs-lookup"><span data-stu-id="a777a-237">Create child</span></span></p>
<p><span data-ttu-id="a777a-238">Удалить дочерний элемент</span><span class="sxs-lookup"><span data-stu-id="a777a-238">Delete child</span></span></p>
<p><span data-ttu-id="a777a-239">Удалить дерево</span><span class="sxs-lookup"><span data-stu-id="a777a-239">Delete tree</span></span></p></td>
<td><p><span data-ttu-id="a777a-240">Службу</span><span class="sxs-lookup"><span data-stu-id="a777a-240">Contact</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a777a-241">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="a777a-241">RTCUniversalUserAdmins</span></span></p></td>
<td><p><span data-ttu-id="a777a-242">Запись отображаемого текста</span><span class="sxs-lookup"><span data-stu-id="a777a-242">Write displayName</span></span></p>
<p><span data-ttu-id="a777a-243">Описание записи</span><span class="sxs-lookup"><span data-stu-id="a777a-243">Write description</span></span></p>
<p><span data-ttu-id="a777a-244">Напишите telephoneNumber</span><span class="sxs-lookup"><span data-stu-id="a777a-244">Write telephoneNumber</span></span></p></td>
<td><p><span data-ttu-id="a777a-245">Дочерние объекты пользователей</span><span class="sxs-lookup"><span data-stu-id="a777a-245">Descendant User objects</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a777a-246">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="a777a-246">RTCUniversalUserAdmins</span></span></p></td>
<td><p><span data-ttu-id="a777a-247">Напишите RTCUserSearchPropertySet</span><span class="sxs-lookup"><span data-stu-id="a777a-247">Write RTCUserSearchPropertySet</span></span></p>
<p><span data-ttu-id="a777a-248">Напишите otherIpPhone</span><span class="sxs-lookup"><span data-stu-id="a777a-248">Write otherIpPhone</span></span></p>
<p><span data-ttu-id="a777a-249">Запись отображаемого текста</span><span class="sxs-lookup"><span data-stu-id="a777a-249">Write displayName</span></span></p>
<p><span data-ttu-id="a777a-250">Описание записи</span><span class="sxs-lookup"><span data-stu-id="a777a-250">Write description</span></span></p>
<p><span data-ttu-id="a777a-251">Напишите telephoneNumber</span><span class="sxs-lookup"><span data-stu-id="a777a-251">Write telephoneNumber</span></span></p>
<p><span data-ttu-id="a777a-252">Напишите msExchUCVoiceMailSettings</span><span class="sxs-lookup"><span data-stu-id="a777a-252">Write msExchUCVoiceMailSettings</span></span></p>
<p><span data-ttu-id="a777a-253">Напишите RTCUserProvisioningPropertySet</span><span class="sxs-lookup"><span data-stu-id="a777a-253">Write RTCUserProvisioningPropertySet</span></span></p>
<p><span data-ttu-id="a777a-254">Напишите RTCPropertySet</span><span class="sxs-lookup"><span data-stu-id="a777a-254">Write RTCPropertySet</span></span></p>
<p><span data-ttu-id="a777a-255">Напишите proxyAddresses</span><span class="sxs-lookup"><span data-stu-id="a777a-255">Write proxyAddresses</span></span></p></td>
<td><p><span data-ttu-id="a777a-256">Дочерние объекты контактов</span><span class="sxs-lookup"><span data-stu-id="a777a-256">Descendant Contact objects</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="granting-permission-for-inetorgperson-objects"></a><span data-ttu-id="a777a-257">Предоставление разрешения для объектов InetOrgPerson</span><span class="sxs-lookup"><span data-stu-id="a777a-257">Granting Permission for InetOrgPerson Objects</span></span>

<span data-ttu-id="a777a-258">При запуске командлета **Grant-CsOuPermission** для объектов inetOrgPerson в подразделении группам предоставляются разрешения, описанные в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="a777a-258">When you run the **Grant-CsOuPermission** cmdlet for InetOrgPerson objects on an OU, groups are granted permissions as shown in the following table.</span></span>

### <a name="permissions-granted-for-inetorgperson-objects"></a><span data-ttu-id="a777a-259">Разрешения, предоставленные для объектов InetOrgPerson</span><span class="sxs-lookup"><span data-stu-id="a777a-259">Permissions Granted for InetOrgPerson Objects</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a777a-260">Сгруппирован</span><span class="sxs-lookup"><span data-stu-id="a777a-260">Group</span></span></th>
<th><span data-ttu-id="a777a-261">PermissionSet</span><span class="sxs-lookup"><span data-stu-id="a777a-261">Permission</span></span></th>
<th><span data-ttu-id="a777a-262">Применимо к</span><span class="sxs-lookup"><span data-stu-id="a777a-262">Applies to</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a777a-263">RTCHSUniversalServices</span><span class="sxs-lookup"><span data-stu-id="a777a-263">RTCHSUniversalServices</span></span></p></td>
<td><p><span data-ttu-id="a777a-264">Репликация изменений каталога</span><span class="sxs-lookup"><span data-stu-id="a777a-264">Replicating directory changes</span></span></p></td>
<td><p><span data-ttu-id="a777a-265">Только этот объект</span><span class="sxs-lookup"><span data-stu-id="a777a-265">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a777a-266">RTCUniversalServerReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="a777a-266">RTCUniversalServerReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="a777a-267">Содержимое списка</span><span class="sxs-lookup"><span data-stu-id="a777a-267">List contents</span></span></p>
<p><span data-ttu-id="a777a-268">Чтение всех свойств</span><span class="sxs-lookup"><span data-stu-id="a777a-268">Read all properties</span></span></p>
<p><span data-ttu-id="a777a-269">Разрешения на чтение</span><span class="sxs-lookup"><span data-stu-id="a777a-269">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="a777a-270">Только этот объект</span><span class="sxs-lookup"><span data-stu-id="a777a-270">This object only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a777a-271">RTCUniversalUserReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="a777a-271">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="a777a-272">Содержимое списка</span><span class="sxs-lookup"><span data-stu-id="a777a-272">List contents</span></span></p>
<p><span data-ttu-id="a777a-273">Чтение всех свойств</span><span class="sxs-lookup"><span data-stu-id="a777a-273">Read all properties</span></span></p>
<p><span data-ttu-id="a777a-274">Разрешения на чтение</span><span class="sxs-lookup"><span data-stu-id="a777a-274">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="a777a-275">Только этот объект</span><span class="sxs-lookup"><span data-stu-id="a777a-275">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a777a-276">RTCUniversalUserReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="a777a-276">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="a777a-277">Прочитать RTCUserSearchPropertySet</span><span class="sxs-lookup"><span data-stu-id="a777a-277">Read RTCUserSearchPropertySet</span></span></p>
<p><span data-ttu-id="a777a-278">Прочитать RTCUserProvisioningPropertySet</span><span class="sxs-lookup"><span data-stu-id="a777a-278">Read RTCUserProvisioningPropertySet</span></span></p>
<p><span data-ttu-id="a777a-279">Прочитать RTCPropertySet</span><span class="sxs-lookup"><span data-stu-id="a777a-279">Read RTCPropertySet</span></span></p>
<p><span data-ttu-id="a777a-280">Чтение Personal-Information</span><span class="sxs-lookup"><span data-stu-id="a777a-280">Read Personal-Information</span></span></p>
<p><span data-ttu-id="a777a-281">Чтение Public-Information</span><span class="sxs-lookup"><span data-stu-id="a777a-281">Read Public-Information</span></span></p>
<p><span data-ttu-id="a777a-282">Чтение General-Information</span><span class="sxs-lookup"><span data-stu-id="a777a-282">Read General-Information</span></span></p>
<p><span data-ttu-id="a777a-283">Чтение ограничений для учетных записей пользователей</span><span class="sxs-lookup"><span data-stu-id="a777a-283">Read User-Account-Restrictions</span></span></p></td>
<td><p><span data-ttu-id="a777a-284">Дочерние объекты inetOrgPerson</span><span class="sxs-lookup"><span data-stu-id="a777a-284">Descendant inetOrgPerson objects</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a777a-285">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="a777a-285">RTCUniversalUserAdmins</span></span></p></td>
<td><p><span data-ttu-id="a777a-286">Напишите RTCUserSearchPropertySet</span><span class="sxs-lookup"><span data-stu-id="a777a-286">Write RTCUserSearchPropertySet</span></span></p>
<p><span data-ttu-id="a777a-287">Напишите RTCUserProvisioningPropertySet</span><span class="sxs-lookup"><span data-stu-id="a777a-287">Write RTCUserProvisioningPropertySet</span></span></p>
<p><span data-ttu-id="a777a-288">Напишите RTCPropertySet</span><span class="sxs-lookup"><span data-stu-id="a777a-288">Write RTCPropertySet</span></span></p>
<p><span data-ttu-id="a777a-289">Напишите proxyAddresses</span><span class="sxs-lookup"><span data-stu-id="a777a-289">Write proxyAddresses</span></span></p></td>
<td><p><span data-ttu-id="a777a-290">Дочерние объекты inetOrgPerson</span><span class="sxs-lookup"><span data-stu-id="a777a-290">Descendant inetOrgPerson objects</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="a777a-291">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a777a-291">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

