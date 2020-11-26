---
title: 'Lync Server 2013: изменения схемы в Lync Server 2013'
description: 'Lync Server 2013: изменения схемы в Lync Server 2013.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Schema changes in Lync Server 2013
ms:assetid: d760cb93-77d4-4d64-adb7-416b808f36f8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398944(v=OCS.15)
ms:contentKeyID: 48185575
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9e914de48ace80fd2611f2d05b092894b11c534a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444926"
---
# <a name="schema-changes-in-lync-server-2013"></a><span data-ttu-id="eb234-103">Изменения схемы в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="eb234-103">Schema changes in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="eb234-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="eb234-104">

<span> </span></span></span>

<span data-ttu-id="eb234-105">_**Тема последнего изменения:** 2012-10-18_</span><span class="sxs-lookup"><span data-stu-id="eb234-105">_**Topic Last Modified:** 2012-10-18_</span></span>

<span data-ttu-id="eb234-106">Перед развертыванием и эксплуатацией Lync Server 2013 необходимо подготовить доменные службы Active Directory, расширив схему.</span><span class="sxs-lookup"><span data-stu-id="eb234-106">Before you deploy and operate Lync Server 2013, you must prepare Active Directory Domain Services by extending the schema.</span></span> <span data-ttu-id="eb234-107">Расширения схемы добавляют классы и атрибуты, необходимые для Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="eb234-107">The schema extensions add the classes and attributes that are required by Lync Server 2013.</span></span>

<span data-ttu-id="eb234-108">Lync Server 2013 требует нескольких новых классов и атрибутов и изменяет некоторые существующие классы и атрибуты.</span><span class="sxs-lookup"><span data-stu-id="eb234-108">Lync Server 2013 requires several new classes and attributes and modifies some existing classes and attributes.</span></span> <span data-ttu-id="eb234-109">Кроме того, многие сведения о конфигурации Lync Server 2013 хранятся в главном хранилище, а не в службах AD DS, как в предыдущих версиях.</span><span class="sxs-lookup"><span data-stu-id="eb234-109">In addition, much configuration information for Lync Server 2013 is stored in the Central Management store instead of in AD DS as in previous versions.</span></span> <span data-ttu-id="eb234-110">Следующая информация сохраняется в службах AD DS в Lync Server 2013:</span><span class="sxs-lookup"><span data-stu-id="eb234-110">The following information is still stored in AD DS in Lync Server 2013:</span></span>

  - <span data-ttu-id="eb234-111">**Расширения схемы**.</span><span class="sxs-lookup"><span data-stu-id="eb234-111">**Schema extensions**:</span></span>
    
      - <span data-ttu-id="eb234-112">Расширения объекта пользователя</span><span class="sxs-lookup"><span data-stu-id="eb234-112">User object extensions</span></span>
    
      - <span data-ttu-id="eb234-113">Расширения для классов Office Communications Server 2007 и Office Communications Server 2007 R2 обеспечивают обратную совместимость с предыдущими версиями</span><span class="sxs-lookup"><span data-stu-id="eb234-113">Extensions for Office Communications Server 2007 and Office Communications Server 2007 R2 classes to maintain backward compatibility with supported previous versions</span></span>

<!-- end list -->

  - <span data-ttu-id="eb234-114">**Данные** (хранящиеся в расширенной схеме Lync Server и существующих классах схем):</span><span class="sxs-lookup"><span data-stu-id="eb234-114">**Data** (stored in Lync Server extended schema and in existing schema classes):</span></span>
    
      - <span data-ttu-id="eb234-115">Универсальный код ресурса (URI) пользователя SIP и другие пользовательские параметры</span><span class="sxs-lookup"><span data-stu-id="eb234-115">User SIP Uniform Resource Identifier (URI) and other user settings</span></span>
    
      - <span data-ttu-id="eb234-116">Объекты контактов для таких приложений, как группа ответа и конференц-связь</span><span class="sxs-lookup"><span data-stu-id="eb234-116">Contact objects for applications such as Response Group and Conferencing Attendant</span></span>
    
      - <span data-ttu-id="eb234-117">Указатель на хранилище Центрального управления</span><span class="sxs-lookup"><span data-stu-id="eb234-117">A pointer to the Central Management store</span></span>
    
      - <span data-ttu-id="eb234-118">Учетная запись для проверки подлинности Kerberos (необязательный объект-компьютер)</span><span class="sxs-lookup"><span data-stu-id="eb234-118">Kerberos Authentication Account (an optional computer object)</span></span>

<span data-ttu-id="eb234-119">В этой статье описаны изменения схемы Active Directory, необходимые для Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="eb234-119">This topic describes the Active Directory schema changes required by Lync Server 2013.</span></span> <span data-ttu-id="eb234-120">В нем не описаны изменения схемы, которые появились в предыдущих версиях Office Communications Server.</span><span class="sxs-lookup"><span data-stu-id="eb234-120">It does not describe schema changes that were introduced by previous versions of Office Communications Server.</span></span> <span data-ttu-id="eb234-121">Список классов и их описаний можно найти в разделе [классы и описания схемы в Lync Server 2013](lync-server-2013-schema-classes-and-descriptions.md).</span><span class="sxs-lookup"><span data-stu-id="eb234-121">For a list of classes and their descriptions, see [Schema classes and descriptions in Lync Server 2013](lync-server-2013-schema-classes-and-descriptions.md).</span></span> <span data-ttu-id="eb234-122">Список атрибутов и их описание можно найти [в разделе атрибуты и описания схемы в Lync Server 2013](lync-server-2013-schema-attributes-and-descriptions.md).</span><span class="sxs-lookup"><span data-stu-id="eb234-122">For a list of attributes and their descriptions, see [Schema attributes and descriptions in Lync Server 2013](lync-server-2013-schema-attributes-and-descriptions.md).</span></span> <span data-ttu-id="eb234-123">Список классов с атрибутами, которые они могут содержать, можно найти [в разделе атрибуты схемы по классу в Lync Server 2013](lync-server-2013-schema-attributes-by-class.md).</span><span class="sxs-lookup"><span data-stu-id="eb234-123">For a list of classes with the attributes they may contain, see [Schema attributes by class in Lync Server 2013](lync-server-2013-schema-attributes-by-class.md).</span></span>

<span data-ttu-id="eb234-124">Префикс msRTCSIP определяет классы и атрибуты, специфичные для сервера Lync Server.</span><span class="sxs-lookup"><span data-stu-id="eb234-124">The msRTCSIP prefix identifies classes and attributes that are specific to Lync Server.</span></span>

<div>

## <a name="new-active-directory-attributes"></a><span data-ttu-id="eb234-125">Новые атрибуты Active Directory</span><span class="sxs-lookup"><span data-stu-id="eb234-125">New Active Directory Attributes</span></span>

<span data-ttu-id="eb234-126">В таблице ниже описаны атрибуты Active Directory, добавленные в Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="eb234-126">The following table describes the Active Directory attributes that are added by Lync Server 2013.</span></span>

### <a name="attributes-added-by-lync-server-2013"></a><span data-ttu-id="eb234-127">Атрибуты, добавленные в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="eb234-127">Attributes Added by Lync Server 2013</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="eb234-128">Атрибут</span><span class="sxs-lookup"><span data-stu-id="eb234-128">Attribute</span></span></th>
<th><span data-ttu-id="eb234-129">Описание</span><span class="sxs-lookup"><span data-stu-id="eb234-129">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eb234-130">msExchUserHoldPolicies</span><span class="sxs-lookup"><span data-stu-id="eb234-130">msExchUserHoldPolicies</span></span></p></td>
<td><p><span data-ttu-id="eb234-131">Этот атрибут с несколькими значениями содержит идентификаторы для политик хранения, которые применяются к пользователю.</span><span class="sxs-lookup"><span data-stu-id="eb234-131">This multi-value attribute holds identifiers for hold policies that apply to the user.</span></span> <span data-ttu-id="eb234-132">Политики удержания сохраняют для пользователя элементы почтового ящика на время удержания.</span><span class="sxs-lookup"><span data-stu-id="eb234-132">Hold policies preserve mailbox items for the user for the duration of the hold.</span></span> <span data-ttu-id="eb234-133">Этот атрибут является общим для Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="eb234-133">This attribute is shared with Exchange 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb234-134">msRTCSIP-UserRoutingGroupId</span><span class="sxs-lookup"><span data-stu-id="eb234-134">msRTCSIP-UserRoutingGroupId</span></span></p></td>
<td><p><span data-ttu-id="eb234-135">Это идентификатор группы маршрутизации SIP.</span><span class="sxs-lookup"><span data-stu-id="eb234-135">This is the SIP routing group ID.</span></span> <span data-ttu-id="eb234-136">Пользователи в одной группе будут регистрироваться на одном и том же внешнем сервере.</span><span class="sxs-lookup"><span data-stu-id="eb234-136">Users in the same group will register to the same Front End Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb234-137">msRTCSIP-MirrorBackEndServer</span><span class="sxs-lookup"><span data-stu-id="eb234-137">msRTCSIP-MirrorBackEndServer</span></span></p></td>
<td><p><span data-ttu-id="eb234-138">Этот атрибут используется для хранения зеркальной серверной части SQL Server, используемой в пуле переднего плана.</span><span class="sxs-lookup"><span data-stu-id="eb234-138">This attribute is used to store the mirrored SQL Server backend used by the Front End pool.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="modified-active-directory-classes"></a><span data-ttu-id="eb234-139">Измененные классы Active Directory</span><span class="sxs-lookup"><span data-stu-id="eb234-139">Modified Active Directory Classes</span></span>

<span data-ttu-id="eb234-140">В таблице ниже описаны классы Active Directory, измененные в Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="eb234-140">The following table describes the Active Directory classes that are modified by Lync Server 2013.</span></span>

### <a name="classes-modified-by-lync-server-2013"></a><span data-ttu-id="eb234-141">Классы, измененные в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="eb234-141">Classes Modified by Lync Server 2013</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="eb234-142">Классов</span><span class="sxs-lookup"><span data-stu-id="eb234-142">Class</span></span></th>
<th><span data-ttu-id="eb234-143">Изменение</span><span class="sxs-lookup"><span data-stu-id="eb234-143">Change</span></span></th>
<th><span data-ttu-id="eb234-144">Класс или атрибут</span><span class="sxs-lookup"><span data-stu-id="eb234-144">Class or Attribute</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eb234-145">Пользователь</span><span class="sxs-lookup"><span data-stu-id="eb234-145">User</span></span></p></td>
<td><p><span data-ttu-id="eb234-146">Add (Добавить): mayContain</span><span class="sxs-lookup"><span data-stu-id="eb234-146">add: mayContain</span></span></p>
<p><span data-ttu-id="eb234-147">Add (Добавить): mayContain</span><span class="sxs-lookup"><span data-stu-id="eb234-147">add: mayContain</span></span></p></td>
<td><p><span data-ttu-id="eb234-148">ProxyAddresses</span><span class="sxs-lookup"><span data-stu-id="eb234-148">ProxyAddresses</span></span></p>
<p><span data-ttu-id="eb234-149">msRTCSIP-UserRoutingGroupId</span><span class="sxs-lookup"><span data-stu-id="eb234-149">msRTCSIP-UserRoutingGroupId</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb234-150">Службу</span><span class="sxs-lookup"><span data-stu-id="eb234-150">Contact</span></span></p></td>
<td><p><span data-ttu-id="eb234-151">Add (Добавить): mayContain</span><span class="sxs-lookup"><span data-stu-id="eb234-151">add: mayContain</span></span></p>
<p><span data-ttu-id="eb234-152">Add (Добавить): mayContain</span><span class="sxs-lookup"><span data-stu-id="eb234-152">add: mayContain</span></span></p></td>
<td><p><span data-ttu-id="eb234-153">ProxyAddresses</span><span class="sxs-lookup"><span data-stu-id="eb234-153">ProxyAddresses</span></span></p>
<p><span data-ttu-id="eb234-154">msRTCSIP-UserRoutingGroupId</span><span class="sxs-lookup"><span data-stu-id="eb234-154">msRTCSIP-UserRoutingGroupId</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb234-155">Mail-Recipient</span><span class="sxs-lookup"><span data-stu-id="eb234-155">Mail-Recipient</span></span></p></td>
<td><p><span data-ttu-id="eb234-156">Add (Добавить): mayContain</span><span class="sxs-lookup"><span data-stu-id="eb234-156">add: mayContain</span></span></p></td>
<td><p><span data-ttu-id="eb234-157">msExchUserHoldPolicies</span><span class="sxs-lookup"><span data-stu-id="eb234-157">msExchUserHoldPolicies</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb234-158">msRTCSIP-GlobalTopologySetting</span><span class="sxs-lookup"><span data-stu-id="eb234-158">msRTCSIP-GlobalTopologySetting</span></span></p></td>
<td><p><span data-ttu-id="eb234-159">Add (Добавить): mayContain</span><span class="sxs-lookup"><span data-stu-id="eb234-159">add: mayContain</span></span></p></td>
<td><p><span data-ttu-id="eb234-160">msRTCSIP-MirrorBackEndServer</span><span class="sxs-lookup"><span data-stu-id="eb234-160">msRTCSIP-MirrorBackEndServer</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="eb234-161">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="eb234-161">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

