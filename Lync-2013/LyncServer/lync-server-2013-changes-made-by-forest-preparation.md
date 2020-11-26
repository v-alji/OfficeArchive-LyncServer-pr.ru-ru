---
title: 'Lync Server 2013: изменения, внесенные с помощью подготовки леса'
description: 'Lync Server 2013: изменения, внесенные с помощью подготовки леса.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Changes made by forest preparation
ms:assetid: 2e12613e-59f2-4810-a32d-24a9789a4a6e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425791(v=OCS.15)
ms:contentKeyID: 48183734
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1c9bc40539c285e03610b2fc97166842473997fb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435077"
---
# <a name="changes-made-by-forest-preparation-in-lync-server-2013"></a><span data-ttu-id="b4912-103">Изменения, внесенные в процессе подготовки леса в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b4912-103">Changes made by forest preparation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b4912-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b4912-104">

<span> </span></span></span>

<span data-ttu-id="b4912-105">_**Тема последнего изменения:** 2012-10-30_</span><span class="sxs-lookup"><span data-stu-id="b4912-105">_**Topic Last Modified:** 2012-10-30_</span></span>

<span data-ttu-id="b4912-106">В этом разделе описаны глобальные параметры и объекты, а также универсальные службы и группы администрирования, созданные на этапе подготовки леса.</span><span class="sxs-lookup"><span data-stu-id="b4912-106">This section describes the global settings and objects, and the universal service and administration groups that are created by the forest preparation step.</span></span>

<div>

## <a name="active-directory-global-settings-and-objects"></a><span data-ttu-id="b4912-107">Глобальные параметры и объекты в службе каталогов Active Directory</span><span class="sxs-lookup"><span data-stu-id="b4912-107">Active Directory Global Settings and Objects</span></span>

<span data-ttu-id="b4912-108">Если вы сохраняете глобальные параметры в контейнере конфигурации (как в случае со всеми новыми развертываниями для Lync Server 2013), подготовка леса использует существующий контейнер служб и добавляет объект **службы RTC** в объект Configuration \\ Services.</span><span class="sxs-lookup"><span data-stu-id="b4912-108">If you store global settings in the Configuration container (as is the case for all new Lync Server 2013 deployments), forest preparation uses the existing Services container and adds an **RTC Service** object under the Configuration\\Services object.</span></span> <span data-ttu-id="b4912-109">В разделе объект службы RTC для подготовки леса добавляется **глобальный объект параметров** типа MsRTCSIP-GlobalContainer.</span><span class="sxs-lookup"><span data-stu-id="b4912-109">Under the RTC Service object, forest preparation adds a **Global Settings** object of type msRTCSIP-GlobalContainer.</span></span> <span data-ttu-id="b4912-110">Объект глобальных параметров содержит все параметры, которые применяются к развертыванию Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b4912-110">The global settings object holds all the settings that apply to the Lync Server deployment.</span></span> <span data-ttu-id="b4912-111">При хранении глобальных параметров в контейнере System для подготовки леса используется контейнер Microsoft из контейнера System корневого домена и объект службы RTC из системного \\ объекта Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b4912-111">If you store global settings in the System container, forest preparation uses a Microsoft container under the root domain System container and an RTC Service object under the System\\Microsoft object.</span></span>

<span data-ttu-id="b4912-112">Подготовка леса также добавляет новый объект **msRTCSIP-Domain** для корневого домена, в котором выполняется процедура.</span><span class="sxs-lookup"><span data-stu-id="b4912-112">Forest preparation also adds a new **msRTCSIP-Domain** object for the root domain in which the procedure is run.</span></span>

</div>

<div>

## <a name="active-directory-universal-service-and-administration-groups"></a><span data-ttu-id="b4912-113">Универсальные службы и группы администрирования Active Directory</span><span class="sxs-lookup"><span data-stu-id="b4912-113">Active Directory Universal Service and Administration Groups</span></span>

<span data-ttu-id="b4912-114">Подготовка леса создает универсальные группы на основе указанного домена и добавляет элементы управления доступом (ACE) для этих групп.</span><span class="sxs-lookup"><span data-stu-id="b4912-114">Forest preparation creates universal groups based on the domain that you specify and adds access control entries (ACEs) for these groups.</span></span> <span data-ttu-id="b4912-115">На этом этапе создаются универсальные группы в контейнерах пользователей указанного домена.</span><span class="sxs-lookup"><span data-stu-id="b4912-115">This step creates the universal groups in the User containers of the domain that you specify.</span></span>

<span data-ttu-id="b4912-116">Универсальные группы позволяют администраторам получать доступ к глобальным параметрам и службам и управлять ими.</span><span class="sxs-lookup"><span data-stu-id="b4912-116">Universal groups allow administrators to access and manage global settings and services.</span></span> <span data-ttu-id="b4912-117">Подготовка леса добавляет следующие типы универсальных групп:</span><span class="sxs-lookup"><span data-stu-id="b4912-117">Forest preparation adds the following types of universal groups:</span></span>

  - <span data-ttu-id="b4912-118">**Административные группы**   Эти группы определяют роли администратора в сети Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b4912-118">**Administrative groups**   These groups define administrator roles for a Lync Server network.</span></span>

  - <span data-ttu-id="b4912-119">**Группы инфраструктуры**   Эти группы предоставляют разрешения на доступ к определенным областям инфраструктуры Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b4912-119">**Infrastructure groups**   These groups provide permission to access specific areas of the Lync Server infrastructure.</span></span> <span data-ttu-id="b4912-120">Они будут работать как компоненты административных групп.</span><span class="sxs-lookup"><span data-stu-id="b4912-120">They function as components of administrative groups.</span></span> <span data-ttu-id="b4912-121">Не следует изменять эти группы и добавлять пользователей прямо в них.</span><span class="sxs-lookup"><span data-stu-id="b4912-121">You should not modify these groups or add users directly to them.</span></span>

  - <span data-ttu-id="b4912-122">**Группы служб**   Эти группы представляют собой учетные записи служб, необходимые для доступа к различным службам Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b4912-122">**Service groups**   These groups are service accounts that are required to access various Lync Server services.</span></span>

<span data-ttu-id="b4912-123">В приведенной ниже таблице описаны группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="b4912-123">The following table describes the administrative groups.</span></span>

### <a name="administrative-groups-created-during-forest-preparation"></a><span data-ttu-id="b4912-124">Административные группы, созданные во время подготовки леса</span><span class="sxs-lookup"><span data-stu-id="b4912-124">Administrative Groups Created During Forest Preparation</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b4912-125">Группа администраторов</span><span class="sxs-lookup"><span data-stu-id="b4912-125">Administrative group</span></span></th>
<th><span data-ttu-id="b4912-126">Описание</span><span class="sxs-lookup"><span data-stu-id="b4912-126">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b4912-127">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="b4912-127">RTCUniversalServerAdmins</span></span></p></td>
<td><p><span data-ttu-id="b4912-128">Позволяет пользователям управлять параметрами сервера и пула, включая все роли сервера, глобальные параметры и пользователей.</span><span class="sxs-lookup"><span data-stu-id="b4912-128">Allows members to manage server and pool settings, including all server roles, global settings, and users.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4912-129">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="b4912-129">RTCUniversalUserAdmins</span></span></p></td>
<td><p><span data-ttu-id="b4912-130">Позволяет пользователям управлять параметрами пользователей и перемещать пользователей из одного сервера или пула в другой.</span><span class="sxs-lookup"><span data-stu-id="b4912-130">Allows members to manage user settings and move users from one server or pool to another.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4912-131">RTCUniversalReadOnlyAdmins</span><span class="sxs-lookup"><span data-stu-id="b4912-131">RTCUniversalReadOnlyAdmins</span></span></p></td>
<td><p><span data-ttu-id="b4912-132">Позволяет участникам читать параметры сервера, пула и пользователей.</span><span class="sxs-lookup"><span data-stu-id="b4912-132">Allows members to read server, pool, and user settings.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b4912-133">В приведенной ниже таблице описаны группы инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="b4912-133">The following table describes the infrastructure groups.</span></span>

### <a name="infrastructure-groups-created-during-forest-preparation"></a><span data-ttu-id="b4912-134">Группы инфраструктуры, созданные во время подготовки леса</span><span class="sxs-lookup"><span data-stu-id="b4912-134">Infrastructure Groups Created During Forest Preparation</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b4912-135">Группа инфраструктуры</span><span class="sxs-lookup"><span data-stu-id="b4912-135">Infrastructure group</span></span></th>
<th><span data-ttu-id="b4912-136">Описание</span><span class="sxs-lookup"><span data-stu-id="b4912-136">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b4912-137">RTCUniversalGlobalWriteGroup</span><span class="sxs-lookup"><span data-stu-id="b4912-137">RTCUniversalGlobalWriteGroup</span></span></p></td>
<td><p><span data-ttu-id="b4912-138">Предоставление доступа на запись к глобальным объектам параметров для Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b4912-138">Grants write access to global setting objects for Lync Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4912-139">RTCUniversalGlobalReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="b4912-139">RTCUniversalGlobalReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="b4912-140">Предоставляет доступ только для чтения к глобальным объектам параметров для Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b4912-140">Grants read-only access to global setting objects for Lync Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4912-141">RTCUniversalUserReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="b4912-141">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="b4912-142">Предоставляет доступ только для чтения к параметрам пользователя Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b4912-142">Grants read-only access to Lync Server user settings.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4912-143">RTCUniversalServerReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="b4912-143">RTCUniversalServerReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="b4912-144">Предоставляет доступ только для чтения к параметрам Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b4912-144">Grants read-only access to Lync Server settings.</span></span> <span data-ttu-id="b4912-145">У этой группы нет доступа к параметрам уровня группы, только к параметрам, относящимся к отдельному серверу.</span><span class="sxs-lookup"><span data-stu-id="b4912-145">This group does not have access to pool level settings, only to settings specific to an individual server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4912-146">RTCUniversalSBATechnicians</span><span class="sxs-lookup"><span data-stu-id="b4912-146">RTCUniversalSBATechnicians</span></span></p></td>
<td><p><span data-ttu-id="b4912-147">Предоставляет доступ только для чтения к конфигурации Lync Server и помещается в локальную группу администраторов для бесперебойных устройств филиала во время установки.</span><span class="sxs-lookup"><span data-stu-id="b4912-147">Grants read-only access to Lync Server configuration and are placed in the Local Administrators group of the survivable branch appliances during installation.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b4912-148">В приведенной ниже таблице описаны группы служб.</span><span class="sxs-lookup"><span data-stu-id="b4912-148">The following table describes the service groups.</span></span>

### <a name="service-groups-created-during-forest-preparation"></a><span data-ttu-id="b4912-149">Группы служб, созданные во время подготовки леса</span><span class="sxs-lookup"><span data-stu-id="b4912-149">Service Groups Created During Forest Preparation</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b4912-150">Группа "Сервис"</span><span class="sxs-lookup"><span data-stu-id="b4912-150">Service group</span></span></th>
<th><span data-ttu-id="b4912-151">Описание</span><span class="sxs-lookup"><span data-stu-id="b4912-151">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b4912-152">RTCHSUniversalServices</span><span class="sxs-lookup"><span data-stu-id="b4912-152">RTCHSUniversalServices</span></span></p></td>
<td><p><span data-ttu-id="b4912-153">Включает служебные учетные записи, используемые для запуска серверного сервера и сервера стандартных выпусков.</span><span class="sxs-lookup"><span data-stu-id="b4912-153">Includes service accounts used to run Front End Server and Standard Edition servers.</span></span> <span data-ttu-id="b4912-154">Эта группа позволяет серверам просматривать и записывать доступ к глобальным параметрам Lync Server и объектам пользователей Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b4912-154">This group allows servers read/write access to Lync Server global settings and Active Directory user objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4912-155">RTCComponentUniversalServices</span><span class="sxs-lookup"><span data-stu-id="b4912-155">RTCComponentUniversalServices</span></span></p></td>
<td><p><span data-ttu-id="b4912-156">Включает служебные учетные записи, которые используются для работы серверов конференц-связи, веб-служб, сервера исправлений, сервера архивирования и сервера мониторинга.</span><span class="sxs-lookup"><span data-stu-id="b4912-156">Includes service accounts used to run A/V Conferencing Servers, Web Services, Mediation Server, Archiving Server, and Monitoring Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4912-157">RTCProxyUniversalServices</span><span class="sxs-lookup"><span data-stu-id="b4912-157">RTCProxyUniversalServices</span></span></p></td>
<td><p><span data-ttu-id="b4912-158">Включает учетные записи служб, используемые для выполнения пограничных серверов Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b4912-158">Includes service accounts used to run Lync Server Edge Servers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4912-159">RTCUniversalConfigReplicator</span><span class="sxs-lookup"><span data-stu-id="b4912-159">RTCUniversalConfigReplicator</span></span></p></td>
<td><p><span data-ttu-id="b4912-160">Включает серверы, которые могут принимать участие в репликации в магазине Lync Server Central Management.</span><span class="sxs-lookup"><span data-stu-id="b4912-160">Includes servers that can participate in Lync Server Central Management store replication.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4912-161">RTCSBAUniversalServices</span><span class="sxs-lookup"><span data-stu-id="b4912-161">RTCSBAUniversalServices</span></span></p></td>
<td><p><span data-ttu-id="b4912-162">Предоставляет доступ только для чтения к параметрам Lync Server, но позволяет настроить конфигурацию для установления работающего сервера филиала и для бесперебойной конфигурации устройства филиала.</span><span class="sxs-lookup"><span data-stu-id="b4912-162">Grants read-only access to Lync Server settings, but allows for configuration for the installation of a survivable branch server and survivable branch appliance deployment.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b4912-163">После подготовки леса в соответствующие группы инфраструктуры добавляются группы служб и администрирования, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="b4912-163">Forest preparation then adds service and administration groups to the appropriate infrastructure groups, as follows:</span></span>

  - <span data-ttu-id="b4912-164">RTCUniversalServerAdmins добавляется в RTCUniversalGlobalReadOnlyGroup, RTCUniversalGlobalWriteGroup, RTCUniversalServerReadOnlyGroup и RTCUniversalUserReadOnlyGroup.</span><span class="sxs-lookup"><span data-stu-id="b4912-164">RTCUniversalServerAdmins is added to RTCUniversalGlobalReadOnlyGroup, RTCUniversalGlobalWriteGroup, RTCUniversalServerReadOnlyGroup, and RTCUniversalUserReadOnlyGroup.</span></span>

  - <span data-ttu-id="b4912-165">RTCUniversalUserAdmins добавляется как член из RTCUniversalGlobalReadOnlyGroup, RTCUniversalServerReadOnlyGroup и RTCUniversalUserReadOnlyGroup.</span><span class="sxs-lookup"><span data-stu-id="b4912-165">RTCUniversalUserAdmins is added as a member of RTCUniversalGlobalReadOnlyGroup, RTCUniversalServerReadOnlyGroup, and RTCUniversalUserReadOnlyGroup.</span></span>

  - <span data-ttu-id="b4912-166">RTCHSUniversalServices, RTCComponentUniversalServices и RTCUniversalReadOnlyAdmins добавляются как члены RTCUniversalGlobalReadOnlyGroup, RTCUniversalServerReadOnlyGroup и RTCUniversalUserReadOnlyGroup.</span><span class="sxs-lookup"><span data-stu-id="b4912-166">RTCHSUniversalServices, RTCComponentUniversalServices and RTCUniversalReadOnlyAdmins are added as members of RTCUniversalGlobalReadOnlyGroup, RTCUniversalServerReadOnlyGroup, and RTCUniversalUserReadOnlyGroup.</span></span>

<span data-ttu-id="b4912-167">При подготовке леса также создаются следующие группы управления доступом на основе ролей (RBAC).</span><span class="sxs-lookup"><span data-stu-id="b4912-167">Forest preparation also creates the following role-based access control (RBAC) groups:</span></span>

  - <span data-ttu-id="b4912-168">CSAdministrator</span><span class="sxs-lookup"><span data-stu-id="b4912-168">CSAdministrator</span></span>

  - <span data-ttu-id="b4912-169">CSArchivingAdministrator</span><span class="sxs-lookup"><span data-stu-id="b4912-169">CSArchivingAdministrator</span></span>

  - <span data-ttu-id="b4912-170">CSHelpDesk</span><span class="sxs-lookup"><span data-stu-id="b4912-170">CSHelpDesk</span></span>

  - <span data-ttu-id="b4912-171">CSLocationAdministrator</span><span class="sxs-lookup"><span data-stu-id="b4912-171">CSLocationAdministrator</span></span>

  - <span data-ttu-id="b4912-172">CSResponseGroupAdministrator</span><span class="sxs-lookup"><span data-stu-id="b4912-172">CSResponseGroupAdministrator</span></span>

  - <span data-ttu-id="b4912-173">CSServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="b4912-173">CSServerAdministrator</span></span>

  - <span data-ttu-id="b4912-174">CSUserAdministrator</span><span class="sxs-lookup"><span data-stu-id="b4912-174">CSUserAdministrator</span></span>

  - <span data-ttu-id="b4912-175">CSViewOnlyAdministrator</span><span class="sxs-lookup"><span data-stu-id="b4912-175">CSViewOnlyAdministrator</span></span>

  - <span data-ttu-id="b4912-176">CSVoiceAdministrator</span><span class="sxs-lookup"><span data-stu-id="b4912-176">CSVoiceAdministrator</span></span>

  - <span data-ttu-id="b4912-177">CsPersistentChatAdministator</span><span class="sxs-lookup"><span data-stu-id="b4912-177">CsPersistentChatAdministator</span></span>

  - <span data-ttu-id="b4912-178">CsResponseGroupManager</span><span class="sxs-lookup"><span data-stu-id="b4912-178">CsResponseGroupManager</span></span>

<span data-ttu-id="b4912-179">Подробные сведения о ролях RBAC и допустимых задачах можно найти [в разделе Планирование управления доступом на основе ролей в Lync Server 2013](lync-server-2013-planning-for-role-based-access-control.md) в документации по планированию.</span><span class="sxs-lookup"><span data-stu-id="b4912-179">For details about RBAC roles and the tasks allowed for each, see [Planning for role-based access control in Lync Server 2013](lync-server-2013-planning-for-role-based-access-control.md) in the Planning documentation.</span></span>

<span data-ttu-id="b4912-180">Подготовка леса создает как закрытые, так и общедоступные элементы управления доступом.</span><span class="sxs-lookup"><span data-stu-id="b4912-180">Forest preparation creates both private and public ACEs.</span></span> <span data-ttu-id="b4912-181">Он создает закрытые записи ACE в контейнере глобальных параметров, используемом в Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b4912-181">It creates private ACEs on the global settings container used by Lync Server.</span></span> <span data-ttu-id="b4912-182">Этот контейнер используется только приложением Lync Server и находится в контейнере Configuration или контейнере System в корневом домене в зависимости от того, где хранятся глобальные параметры.</span><span class="sxs-lookup"><span data-stu-id="b4912-182">This container is used only by Lync Server and is located either in the Configuration container or the System container in the root domain, depending on where you store global settings.</span></span> <span data-ttu-id="b4912-183">Общедоступные ACE, созданные с помощью подготовки леса, перечислены в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="b4912-183">The public ACEs created by forest preparation are listed in the following table.</span></span>

### <a name="public-aces-created-by-forest-preparation"></a><span data-ttu-id="b4912-184">Общедоступные ACE, созданные с помощью подготовки леса</span><span class="sxs-lookup"><span data-stu-id="b4912-184">Public ACEs created by Forest Preparation</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b4912-185">РЕЗУЛЬТИРУЮЩ</span><span class="sxs-lookup"><span data-stu-id="b4912-185">ACE</span></span></th>
<th><span data-ttu-id="b4912-186">RTCUniversalGlobalReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="b4912-186">RTCUniversalGlobalReadOnlyGroup</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b4912-187">Чтение контейнера корневого домена системы (не наследуется)<strong>\*</strong></span><span class="sxs-lookup"><span data-stu-id="b4912-187">Read root domain System Container (not inherited)<strong>\*</strong></span></span></p></td>
<td><p><span data-ttu-id="b4912-188">X</span><span class="sxs-lookup"><span data-stu-id="b4912-188">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4912-189">DisplaySpecifiers контейнер конфигурации чтения (не унаследовано)</span><span class="sxs-lookup"><span data-stu-id="b4912-189">Read Configuration’s DisplaySpecifiers container (not inherited)</span></span></p></td>
<td><p><span data-ttu-id="b4912-190">X</span><span class="sxs-lookup"><span data-stu-id="b4912-190">X</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="b4912-191"><STRONG>\*</STRONG>ACE, не унаследованные, не предоставляют доступ к дочерним объектам в этих контейнерах.</span><span class="sxs-lookup"><span data-stu-id="b4912-191"><STRONG>\*</STRONG>ACEs that are not inherited do not grant access to child objects under these containers.</span></span> <span data-ttu-id="b4912-192">ACE, наследуемые предоставлением разрешения на доступ к дочерним объектам в этих контейнерах.</span><span class="sxs-lookup"><span data-stu-id="b4912-192">ACEs that are inherited grant access to child objects under these containers.</span></span>



</div>

<span data-ttu-id="b4912-193">В контейнере конфигурации в разделе контекст именования конфигурации для подготовки леса выполняются следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="b4912-193">On the Configuration container, under the Configuration naming context, forest preparation performs the following tasks:</span></span>

  - <span data-ttu-id="b4912-194">Добавляет запись **{AB255F23-2DBD-4bb6-891D-38754AC280EF}** для страницы **Свойства RTC** в соответствии с атрибутами adminContextMenu и adminPropertyPages в описателе языка для пользователей, контактов и INETORGPERSONS (например, CN = User-Display, CN = 409, CN = DisplaySpecifiers).</span><span class="sxs-lookup"><span data-stu-id="b4912-194">Adds an entry **{AB255F23-2DBD-4bb6-891D-38754AC280EF}** for the **RTC property** page under the adminContextMenu and adminPropertyPages attributes of the language display specifier for users, contacts, and InetOrgPersons (for example, CN=user-Display,CN=409,CN=DisplaySpecifiers).</span></span>

  - <span data-ttu-id="b4912-195">Добавляет объект **RTCPropertySet** типа **ControlAccessRight** в разделе **Extended-Rights** , который относится к классу пользователя и контакту.</span><span class="sxs-lookup"><span data-stu-id="b4912-195">Adds an **RTCPropertySet** object of type **controlAccessRight** under **Extended-Rights** that applies to the User and Contact classes.</span></span>

  - <span data-ttu-id="b4912-196">Добавляет объект **RTCUserSearchPropertySet** типа **ControlAccessRight** в разделе **Расширенные права** , применимые к классам пользователь, контакт, OU и DomainDNS.</span><span class="sxs-lookup"><span data-stu-id="b4912-196">Adds an **RTCUserSearchPropertySet** object of type **controlAccessRight** under **Extended-Rights** that applies to User, Contact, OU, and DomainDNS classes.</span></span>

  - <span data-ttu-id="b4912-197">Добавляет **msRTCSIP-PrimaryUserAddress** в атрибуте **extraColumns** для описателя отображения каждого из языков (например, CN = ORGANIZATIONALUNIT-Display, CN = 409, CN = DisplaySpecifiers) и копирует значения атрибута **extraColumns** дисплея по умолчанию (например, CN = Default-Display, CN = 409, CN = DisplaySpecifiers).</span><span class="sxs-lookup"><span data-stu-id="b4912-197">Adds **msRTCSIP-PrimaryUserAddress** under the **extraColumns** attribute of each language organizational unit (OU) display specifier (for example, CN=organizationalUnit-Display,CN=409,CN=DisplaySpecifiers) and copies the values of the **extraColumns** attribute of the default display (for example, CN=default-Display, CN=409,CN=DisplaySpecifiers).</span></span>

  - <span data-ttu-id="b4912-198">Добавляются атрибуты фильтрации **msRTCSIP-PrimaryUserAddress**, **msRTCSIP-PrimaryHomeServer** и **msRTCSIP-UserEnabled** в атрибуте **AttributeDisplayNames** каждого спецификатора отображения языка для пользователей, контактов и объектов INETORGPERSON (например, на английском языке: CN = User-Display, CN = 409, CN = DisplaySpecifiers).</span><span class="sxs-lookup"><span data-stu-id="b4912-198">Adds **msRTCSIP-PrimaryUserAddress**, **msRTCSIP-PrimaryHomeServer**, and **msRTCSIP-UserEnabled** filtering attributes under the **attributeDisplayNames** attribute of each language display specifier for Users, Contacts, and InetOrgPerson objects (for example, in English: CN=user-Display,CN=409,CN=DisplaySpecifiers).</span></span>

<span data-ttu-id="b4912-199"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b4912-199"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

