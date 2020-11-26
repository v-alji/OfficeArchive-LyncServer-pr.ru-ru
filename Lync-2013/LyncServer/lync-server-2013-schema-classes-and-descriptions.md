---
title: 'Lync Server 2013: классы и описания схемы'
description: 'Lync Server 2013: классы и описания схемы.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Schema classes and descriptions
ms:assetid: 7d43b920-ac37-40cc-adfe-be289bda6e9e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398625(v=OCS.15)
ms:contentKeyID: 48184612
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ec27c2e00a7f969dbc13c91b06313c8045894a9e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441972"
---
# <a name="schema-classes-and-descriptions-in-lync-server-2013"></a><span data-ttu-id="c97f3-103">Классы схем и описания в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c97f3-103">Schema classes and descriptions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c97f3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c97f3-104">

<span> </span></span></span>

<span data-ttu-id="c97f3-105">_**Тема последнего изменения:** 2012-10-30_</span><span class="sxs-lookup"><span data-stu-id="c97f3-105">_**Topic Last Modified:** 2012-10-30_</span></span>

<span data-ttu-id="c97f3-106">В этом разделе описаны все классы схем, используемые в Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c97f3-106">This section describes all the schema classes used by Lync Server 2013.</span></span>

<div>

## <a name="schema-classes-and-descriptions"></a><span data-ttu-id="c97f3-107">Классы и описания схемы</span><span class="sxs-lookup"><span data-stu-id="c97f3-107">Schema Classes and Descriptions</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c97f3-108">Классов</span><span class="sxs-lookup"><span data-stu-id="c97f3-108">Class</span></span></th>
<th><span data-ttu-id="c97f3-109">Описание</span><span class="sxs-lookup"><span data-stu-id="c97f3-109">Description</span></span></th>
<th><span data-ttu-id="c97f3-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c97f3-110">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c97f3-111">Mail-Recipient</span><span class="sxs-lookup"><span data-stu-id="c97f3-111">Mail-Recipient</span></span></p></td>
<td><p><span data-ttu-id="c97f3-112">Сообщение электронной почты в единой системе обмена сообщениями Exchange (UM).</span><span class="sxs-lookup"><span data-stu-id="c97f3-112">Exchange Unified Messaging (UM) email recipient.</span></span></p></td>
<td><p><span data-ttu-id="c97f3-113">Этот вспомогательный класс предоставляется в единой системе обмена сообщениями Exchange.</span><span class="sxs-lookup"><span data-stu-id="c97f3-113">This auxiliary class is shared with Exchange UM.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c97f3-114">msRTCSIP-ApplicationContacts</span><span class="sxs-lookup"><span data-stu-id="c97f3-114">msRTCSIP-ApplicationContacts</span></span></p></td>
<td><p><span data-ttu-id="c97f3-115">Этот класс является контейнером для нескольких контактов приложения и не содержит самих атрибутов.</span><span class="sxs-lookup"><span data-stu-id="c97f3-115">This class is a container for multiple application contacts and does not contain any attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="c97f3-116">Новые возможности Microsoft Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="c97f3-116">New in Microsoft Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c97f3-117">msRTCSIP-ApplicationServer</span><span class="sxs-lookup"><span data-stu-id="c97f3-117">msRTCSIP-ApplicationServer</span></span></p></td>
<td><p><span data-ttu-id="c97f3-118">Этот класс содержит запись для точки управления службой для экземпляра служб единой системы обмена сообщениями (UCAS).</span><span class="sxs-lookup"><span data-stu-id="c97f3-118">This class holds the entry for the service control point for an instance of Unified Communications Application Services (UCAS).</span></span></p></td>
<td><p><span data-ttu-id="c97f3-119">Новые возможности Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="c97f3-119">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c97f3-120">msRTCSIP-ApplicationServerService</span><span class="sxs-lookup"><span data-stu-id="c97f3-120">msRTCSIP-ApplicationServerService</span></span></p></td>
<td><p><span data-ttu-id="c97f3-121">Этот класс предоставляет ассоциацию от определенного пула к его службе приложения.</span><span class="sxs-lookup"><span data-stu-id="c97f3-121">This class provides an association from a specific pool to its Application service.</span></span></p></td>
<td><p><span data-ttu-id="c97f3-122">Новые возможности коммуникационного сервера 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="c97f3-122">New in Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c97f3-123">msRTCSIP-ApplicationServerSettings</span><span class="sxs-lookup"><span data-stu-id="c97f3-123">msRTCSIP-ApplicationServerSettings</span></span></p></td>
<td><p><span data-ttu-id="c97f3-124">Этот вспомогательный класс для msRTCSIP-ApplicationServer содержит атрибуты, представляющие параметры для экземпляров службы приложения.</span><span class="sxs-lookup"><span data-stu-id="c97f3-124">This auxiliary class to msRTCSIP-ApplicationServer holds attributes representing settings for instances of the Application service.</span></span></p></td>
<td><p><span data-ttu-id="c97f3-125">Новые возможности коммуникационного сервера 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="c97f3-125">New in Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c97f3-126">msRTCSIP — Архив (устарело)</span><span class="sxs-lookup"><span data-stu-id="c97f3-126">msRTCSIP-Archive (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="c97f3-127">Этот вспомогательный класс в msRTCSIP-GlobalContainer содержит все параметры, связанные с архивацией.</span><span class="sxs-lookup"><span data-stu-id="c97f3-127">This auxiliary class to msRTCSIP-GlobalContainer holds all settings related to archiving.</span></span></p></td>
<td><p><span data-ttu-id="c97f3-128">Устаревшие в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="c97f3-128">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c97f3-129">msRTCSIP-ArchivingServer (устарело)</span><span class="sxs-lookup"><span data-stu-id="c97f3-129">msRTCSIP-ArchivingServer (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="c97f3-130">Этот класс представляет собой один сервер архивирования для обмена мгновенными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="c97f3-130">This class represents a single instant messaging Archiving Server.</span></span> <span data-ttu-id="c97f3-131">Экземпляр этого класса создается, когда компьютер активируется в качестве сервера архивации мгновенных сообщений, например с компьютера, на котором установлена служба архивации мгновенных сообщений.</span><span class="sxs-lookup"><span data-stu-id="c97f3-131">An instance of this class is created when a computer is activated as an instant messaging Archiving Server, such as a computer with the Instant Messaging Archiving service installed.</span></span></p></td>
<td><p><span data-ttu-id="c97f3-132">Устаревшие в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="c97f3-132">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c97f3-133">msRTCSIP-ConferenceDirectories</span><span class="sxs-lookup"><span data-stu-id="c97f3-133">msRTCSIP-ConferenceDirectories</span></span></p></td>
<td><p><span data-ttu-id="c97f3-134">Этот класс является контейнером для нескольких экземпляров каталогов конференций и не содержит самих атрибутов.</span><span class="sxs-lookup"><span data-stu-id="c97f3-134">This class is a container for multiple instances of conference directories and does not contain any attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="c97f3-135">Новые возможности коммуникационного сервера 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="c97f3-135">New in Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c97f3-136">msRTCSIP-ConferenceDirectory</span><span class="sxs-lookup"><span data-stu-id="c97f3-136">msRTCSIP-ConferenceDirectory</span></span></p></td>
<td><p><span data-ttu-id="c97f3-137">Этот класс содержит атрибуты, представляющие параметры для определенного каталога конференций.</span><span class="sxs-lookup"><span data-stu-id="c97f3-137">This class holds attributes representing settings for a specific conference directory.</span></span></p></td>
<td><p><span data-ttu-id="c97f3-138">Новые возможности коммуникационного сервера 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="c97f3-138">New in Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c97f3-139">msRTCSIP-ConnectionPoint</span><span class="sxs-lookup"><span data-stu-id="c97f3-139">msRTCSIP-ConnectionPoint</span></span></p></td>
<td><p><span data-ttu-id="c97f3-140">Общая точка управления службой (SCP) для указания компьютера в качестве сервера, на котором работает Lync Server.</span><span class="sxs-lookup"><span data-stu-id="c97f3-140">Generic service control point (SCP) to specify the computer as a server running Lync Server.</span></span></p></td>
<td><p><span data-ttu-id="c97f3-141">Новые возможности в Lync 2010.</span><span class="sxs-lookup"><span data-stu-id="c97f3-141">New in Lync 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c97f3-142">msRTCSIP-DefaultCWABank</span><span class="sxs-lookup"><span data-stu-id="c97f3-142">msRTCSIP-DefaultCWABank</span></span></p></td>
<td><p><span data-ttu-id="c97f3-143">Этот вспомогательный класс содержит параметры банка Microsoft Lync Web App.</span><span class="sxs-lookup"><span data-stu-id="c97f3-143">This auxiliary class holds the settings for a Microsoft Lync Web App bank.</span></span></p></td>
<td><p><span data-ttu-id="c97f3-144">Новые возможности коммуникационного сервера 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="c97f3-144">New in Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c97f3-145">msRTCSIP-Domain (домен)</span><span class="sxs-lookup"><span data-stu-id="c97f3-145">msRTCSIP-Domain</span></span></p></td>
<td><p><span data-ttu-id="c97f3-146">Этот класс содержит атрибуты, определяющие настроенные домены регистратора SIP.</span><span class="sxs-lookup"><span data-stu-id="c97f3-146">This class holds attributes that define the configured domains of the SIP Registrar.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c97f3-147">msRTCSIP-EdgeProxy</span><span class="sxs-lookup"><span data-stu-id="c97f3-147">msRTCSIP-EdgeProxy</span></span></p></td>
<td><p><span data-ttu-id="c97f3-148">Этот контейнер класса представляет одну службу пограничного доступа.</span><span class="sxs-lookup"><span data-stu-id="c97f3-148">This class container represents a single Access Edge service.</span></span> <span data-ttu-id="c97f3-149">Поскольку служба Edge Access развернута в демилитаризованной зоне, а пользователи обычно не разрешают доступ доменных служб Active Directory из сети периметра, то экземпляры службы Edge Access не присоединяются к сети Active Directory в интрасети.</span><span class="sxs-lookup"><span data-stu-id="c97f3-149">Because an Access Edge service is deployed in the perimeter network and customers usually do not allow Active Directory Domain Services access from the perimeter network, instances of Access Edge service are not joined to the intranet’s Active Directory network.</span></span> <span data-ttu-id="c97f3-150">Таким образом, прокси-серверы доступа не регистрируются автоматически в доменных СЛУЖБах Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c97f3-150">Therefore, Access Proxies are not automatically registered in AD DS.</span></span> <span data-ttu-id="c97f3-151">Администратор должен вручную настроить существование каждого экземпляра службы пограничного доступа в AD DS.</span><span class="sxs-lookup"><span data-stu-id="c97f3-151">The administrator must manually configure the existence of each instance of Access Edge service in AD DS.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c97f3-152">msRTCSIP-EnterpriseMCUSettings</span><span class="sxs-lookup"><span data-stu-id="c97f3-152">msRTCSIP-EnterpriseMCUSettings</span></span></p></td>
<td><p><span data-ttu-id="c97f3-153">Этот вспомогательный класс для msRTCSIP-MCU содержит атрибуты, представляющие параметры серверов конференций.</span><span class="sxs-lookup"><span data-stu-id="c97f3-153">This auxiliary class to msRTCSIP-MCU holds attributes representing settings for Conferencing servers.</span></span></p></td>
<td><p><span data-ttu-id="c97f3-154">Новые возможности Microsoft Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="c97f3-154">New in Microsoft Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c97f3-155">msRTCSIP-EnterpriseMediationServerSettings</span><span class="sxs-lookup"><span data-stu-id="c97f3-155">msRTCSIP-EnterpriseMediationServerSettings</span></span></p></td>
<td><p><span data-ttu-id="c97f3-156">Этот вспомогательный класс для msRTCSIP-MediationServer содержит атрибуты, представляющие параметры серверов-исправлений.</span><span class="sxs-lookup"><span data-stu-id="c97f3-156">This auxiliary class to msRTCSIP-MediationServer holds attributes representing settings for Mediation Servers.</span></span></p></td>
<td><p><span data-ttu-id="c97f3-157">Новые возможности Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="c97f3-157">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c97f3-158">msRTCSIP-EnterpriseServerSettings</span><span class="sxs-lookup"><span data-stu-id="c97f3-158">msRTCSIP-EnterpriseServerSettings</span></span></p></td>
<td><p><span data-ttu-id="c97f3-159">Этот вспомогательный класс для msRTCSIP-Server содержит атрибуты, представляющие параметры для серверов SIP.</span><span class="sxs-lookup"><span data-stu-id="c97f3-159">This auxiliary class to msRTCSIP-Server holds attributes representing settings for SIP servers.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c97f3-160">msRTCSIP-Federation</span><span class="sxs-lookup"><span data-stu-id="c97f3-160">msRTCSIP-Federation</span></span></p></td>
<td><p><span data-ttu-id="c97f3-161">Этот вспомогательный класс для msRTCSIP-GlobalContainer содержит все параметры, связанные с интеграцией.</span><span class="sxs-lookup"><span data-stu-id="c97f3-161">This auxiliary class to msRTCSIP-GlobalContainer holds all settings related to federation.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c97f3-162">msRTCSIP-GlobalContainer</span><span class="sxs-lookup"><span data-stu-id="c97f3-162">msRTCSIP-GlobalContainer</span></span></p></td>
<td><p><span data-ttu-id="c97f3-163">Этот класс содержит все параметры, которые применяются во время развертывания Lync Server.</span><span class="sxs-lookup"><span data-stu-id="c97f3-163">This class holds all settings that apply throughout a Lync Server deployment.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c97f3-164">msRTCSIP-GlobalUserPolicy (устарело)</span><span class="sxs-lookup"><span data-stu-id="c97f3-164">msRTCSIP-GlobalUserPolicy (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="c97f3-165">Этот класс представляет одну политику собраний Office Communications Server.</span><span class="sxs-lookup"><span data-stu-id="c97f3-165">This class represents a single Office Communications Server meeting policy.</span></span></p></td>
<td><p><span data-ttu-id="c97f3-166">Устаревшие в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="c97f3-166">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c97f3-167">msRTCSIP-GlobalTopologySetting</span><span class="sxs-lookup"><span data-stu-id="c97f3-167">msRTCSIP-GlobalTopologySetting</span></span></p></td>
<td><p><span data-ttu-id="c97f3-168">Объект локального глобального параметра топологии.</span><span class="sxs-lookup"><span data-stu-id="c97f3-168">The local global topology setting object.</span></span></p></td>
<td><p><span data-ttu-id="c97f3-169">Новые возможности Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="c97f3-169">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c97f3-170">msRTCSIP-GlobalTopologySettings</span><span class="sxs-lookup"><span data-stu-id="c97f3-170">msRTCSIP-GlobalTopologySettings</span></span></p></td>
<td><p><span data-ttu-id="c97f3-171">Контейнер для размещения глобальных объектов параметров топологии.</span><span class="sxs-lookup"><span data-stu-id="c97f3-171">Container to hold global topology setting objects.</span></span></p></td>
<td><p><span data-ttu-id="c97f3-172">Новые возможности Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="c97f3-172">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c97f3-173">msRTCSIP-LocalNormalization</span><span class="sxs-lookup"><span data-stu-id="c97f3-173">msRTCSIP-LocalNormalization</span></span></p></td>
<td><p><span data-ttu-id="c97f3-174">Этот класс является контейнером, представляющим экземпляр правила нормализации расположения.</span><span class="sxs-lookup"><span data-stu-id="c97f3-174">This class is a container that represents an instance of a location normalization rule.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c97f3-175">msRTCSIP-LocationContactMapping</span><span class="sxs-lookup"><span data-stu-id="c97f3-175">msRTCSIP-LocationContactMapping</span></span></p></td>
<td><p><span data-ttu-id="c97f3-176">Этот класс создается приложением для проведения конференций и содержит атрибуты, которые используются для классификации телефонных номеров конференций по регионам.</span><span class="sxs-lookup"><span data-stu-id="c97f3-176">This class is created by the Conferencing Attendant application and holds attributes used to categorize conference telephone numbers by region.</span></span></p></td>
<td><p><span data-ttu-id="c97f3-177">Новые возможности коммуникационного сервера 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="c97f3-177">New in Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c97f3-178">msRTCSIP-LocationContactMappings</span><span class="sxs-lookup"><span data-stu-id="c97f3-178">msRTCSIP-LocationContactMappings</span></span></p></td>
<td><p><span data-ttu-id="c97f3-179">Этот класс является контейнером для нескольких экземпляров сопоставлений контактов местоположения и не содержит самих атрибутов.</span><span class="sxs-lookup"><span data-stu-id="c97f3-179">This class is a container for multiple instances of location contact mappings and does not contain any attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="c97f3-180">Новые возможности коммуникационного сервера 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="c97f3-180">New in Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c97f3-181">msRTCSIP-LocationProfile</span><span class="sxs-lookup"><span data-stu-id="c97f3-181">msRTCSIP-LocationProfile</span></span></p></td>
<td><p><span data-ttu-id="c97f3-182">Этот класс является контейнером, представляющим определенный профиль расположения.</span><span class="sxs-lookup"><span data-stu-id="c97f3-182">This class is a container that represents a specific location profile.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c97f3-183">msRTCSIP-LocationProfiles (устарело)</span><span class="sxs-lookup"><span data-stu-id="c97f3-183">msRTCSIP-LocationProfiles (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="c97f3-184">Этот класс является контейнером для нескольких профилей местоположения и не содержит самих атрибутов.</span><span class="sxs-lookup"><span data-stu-id="c97f3-184">This class is a container for multiple location profiles and does not contain any attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="c97f3-185">Устаревшие в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="c97f3-185">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c97f3-186">msRTCSIP-LocalNormalizations (устарело)</span><span class="sxs-lookup"><span data-stu-id="c97f3-186">msRTCSIP-LocalNormalizations (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="c97f3-187">Этот класс является контейнером для нескольких локальных правил нормализации и не содержит самих атрибутов.</span><span class="sxs-lookup"><span data-stu-id="c97f3-187">This class is a container for multiple local normalization rules and does not contain any attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="c97f3-188">Устаревшие в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="c97f3-188">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c97f3-189">msRTCSIP-MCU</span><span class="sxs-lookup"><span data-stu-id="c97f3-189">msRTCSIP-MCU</span></span></p></td>
<td><p><span data-ttu-id="c97f3-190">Этот класс представляет один сервер конференц-связи.</span><span class="sxs-lookup"><span data-stu-id="c97f3-190">This class represents a single Conferencing server.</span></span></p></td>
<td><p><span data-ttu-id="c97f3-191">Новые возможности коммуникационного сервера 2007.</span><span class="sxs-lookup"><span data-stu-id="c97f3-191">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c97f3-192">msRTCSIP-MCUFactories</span><span class="sxs-lookup"><span data-stu-id="c97f3-192">msRTCSIP-MCUFactories</span></span></p></td>
<td><p><span data-ttu-id="c97f3-193">Этот класс содержит несколько классов msRTCSIP-MCUFactory и не имеет самих атрибутов.</span><span class="sxs-lookup"><span data-stu-id="c97f3-193">This class holds multiple msRTCSIP-MCUFactory classes and does not have attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="c97f3-194">Новые возможности коммуникационного сервера 2007.</span><span class="sxs-lookup"><span data-stu-id="c97f3-194">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c97f3-195">msRTCSIP-MCUFactory</span><span class="sxs-lookup"><span data-stu-id="c97f3-195">msRTCSIP-MCUFactory</span></span></p></td>
<td><p><span data-ttu-id="c97f3-196">Этот класс является контейнером, представляющим фабрику серверов конференций для одного типа носителя.</span><span class="sxs-lookup"><span data-stu-id="c97f3-196">This class is a container representing a Conferencing Server Factory for a single medium type.</span></span> <span data-ttu-id="c97f3-197">Экземпляр этого класса создается при активации первого сервера конференций для этого конкретного типа и поставщика.</span><span class="sxs-lookup"><span data-stu-id="c97f3-197">An instance of this class is created when the first Conferencing server for this particular type and vendor is activated.</span></span></p></td>
<td><p><span data-ttu-id="c97f3-198">Новые возможности коммуникационного сервера 2007.</span><span class="sxs-lookup"><span data-stu-id="c97f3-198">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c97f3-199">msRTCSIP-MCUFactoryService</span><span class="sxs-lookup"><span data-stu-id="c97f3-199">msRTCSIP-MCUFactoryService</span></span></p></td>
<td><p><span data-ttu-id="c97f3-200">Этот класс обеспечивает связь определенного пула с его фабрикой серверов конференций.</span><span class="sxs-lookup"><span data-stu-id="c97f3-200">This class provides an association from a specific pool to its Conferencing Server Factory.</span></span></p></td>
<td><p><span data-ttu-id="c97f3-201">Новые возможности коммуникационного сервера 2007.</span><span class="sxs-lookup"><span data-stu-id="c97f3-201">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c97f3-202">msRTCSIP-MediationServer</span><span class="sxs-lookup"><span data-stu-id="c97f3-202">msRTCSIP-MediationServer</span></span></p></td>
<td><p><span data-ttu-id="c97f3-203">Этот класс содержит запись для точки управления службой для сервера-посредника.</span><span class="sxs-lookup"><span data-stu-id="c97f3-203">This class holds the entry for the service control point for a Mediation Server.</span></span></p></td>
<td><p><span data-ttu-id="c97f3-204">Новые возможности коммуникационного сервера 2007.</span><span class="sxs-lookup"><span data-stu-id="c97f3-204">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c97f3-205">msRTCSIP — собрание (устарело)</span><span class="sxs-lookup"><span data-stu-id="c97f3-205">msRTCSIP-Meeting (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="c97f3-206">Этот вспомогательный класс для msRTCSIP-GlobalContainer содержит атрибуты, которые представляют настраиваемые параметры собрания.</span><span class="sxs-lookup"><span data-stu-id="c97f3-206">This auxiliary class to msRTCSIP-GlobalContainer holds attributes representing configurable meeting settings.</span></span></p></td>
<td><p><span data-ttu-id="c97f3-207">Устаревшие в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="c97f3-207">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c97f3-208">msRTCSIP — мобильность</span><span class="sxs-lookup"><span data-stu-id="c97f3-208">msRTCSIP-Mobility</span></span></p></td>
<td><p><span data-ttu-id="c97f3-209">Контейнер, в котором хранятся глобальные параметры мобильности.</span><span class="sxs-lookup"><span data-stu-id="c97f3-209">Container that stores the global mobility settings.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c97f3-210">msRTCSIP-MonitoringServer</span><span class="sxs-lookup"><span data-stu-id="c97f3-210">msRTCSIP-MonitoringServer</span></span></p></td>
<td><p><span data-ttu-id="c97f3-211">Этот класс содержит атрибуты, представляющие параметры для одного сервера мониторинга.</span><span class="sxs-lookup"><span data-stu-id="c97f3-211">This class holds attributes that represent settings for a single Monitoring Server.</span></span></p></td>
<td><p><span data-ttu-id="c97f3-212">Новые возможности коммуникационного сервера 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="c97f3-212">New in Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c97f3-213">msRTCSIP-PhoneRoute (устарело)</span><span class="sxs-lookup"><span data-stu-id="c97f3-213">msRTCSIP-PhoneRoute (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="c97f3-214">Этот класс является контейнером, представляющим собой экземпляр наименее затратный маршрут к шлюзу или набору шлюзов.</span><span class="sxs-lookup"><span data-stu-id="c97f3-214">This class is a container representing an instance of a least cost route to a gateway or set of gateways.</span></span> <span data-ttu-id="c97f3-215">Эти сведения используются всеми корпоративными пулами или серверами Standard Edition для маршрутизации исходящих звонков в коммутируемую телефонную сеть общего пользования (PSTN) в наиболее экономичном виде.</span><span class="sxs-lookup"><span data-stu-id="c97f3-215">This information is used by all Enterprise pools or servers running Standard Edition to route outgoing calls to the public switched telephone network (PSTN) in the most cost effective way.</span></span></p></td>
<td><p><span data-ttu-id="c97f3-216">Устаревшие в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="c97f3-216">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c97f3-217">msRTCSIP-PhoneRoutes (устарело)</span><span class="sxs-lookup"><span data-stu-id="c97f3-217">msRTCSIP-PhoneRoutes (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="c97f3-218">Этот класс является контейнером для нескольких маршрутов с наименьшей стоимостью и не содержит самих атрибутов.</span><span class="sxs-lookup"><span data-stu-id="c97f3-218">This class is a container for multiple, least cost routes and does not contain any attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="c97f3-219">Устаревшие в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="c97f3-219">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c97f3-220">msRTCSIP — стратегии (устаревшие)</span><span class="sxs-lookup"><span data-stu-id="c97f3-220">msRTCSIP-Policies (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="c97f3-221">Этот класс содержит несколько классов политики Lync Server и не имеет самих атрибутов.</span><span class="sxs-lookup"><span data-stu-id="c97f3-221">This class holds multiple Lync Server policy classes and does not have any attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="c97f3-222">Устаревшие в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="c97f3-222">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c97f3-223">msRTCSIP — пул</span><span class="sxs-lookup"><span data-stu-id="c97f3-223">msRTCSIP-Pool</span></span></p></td>
<td><p><span data-ttu-id="c97f3-224">Этот класс представляет один пул сервера Lync Server.</span><span class="sxs-lookup"><span data-stu-id="c97f3-224">This class represents a single Lync Server pool.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c97f3-225">msRTCSIP (пулы)</span><span class="sxs-lookup"><span data-stu-id="c97f3-225">msRTCSIP-Pools</span></span></p></td>
<td><p><span data-ttu-id="c97f3-226">Этот класс содержит несколько пулов серверов Lync и не имеет самих атрибутов.</span><span class="sxs-lookup"><span data-stu-id="c97f3-226">This class holds multiple Lync Server pools and does not have any attributes itself.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c97f3-227">msRTCSIP-PoolService</span><span class="sxs-lookup"><span data-stu-id="c97f3-227">msRTCSIP-PoolService</span></span></p></td>
<td><p><span data-ttu-id="c97f3-228">Этот класс представляет контрольную точку элемента управления pointservice для пула.</span><span class="sxs-lookup"><span data-stu-id="c97f3-228">This class represents the service control pointservice control point of a pool.</span></span> <span data-ttu-id="c97f3-229">Пользователи, размещенные в пуле, имеют в качестве точки атрибута msRTCSIP-PrimaryHomeServer экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="c97f3-229">Users hosted on a pool have their msRTCSIP-PrimaryHomeServer attribute point to an instance of this class.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c97f3-230">msRTCSIP — присутствие</span><span class="sxs-lookup"><span data-stu-id="c97f3-230">msRTCSIP-Presence</span></span></p></td>
<td><p><span data-ttu-id="c97f3-231">Контейнер, в котором хранятся глобальные параметры присутствия.</span><span class="sxs-lookup"><span data-stu-id="c97f3-231">Container that stores the global presence settings.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c97f3-232">msRTCSIP-регистратор</span><span class="sxs-lookup"><span data-stu-id="c97f3-232">msRTCSIP-Registrar</span></span></p></td>
<td><p><span data-ttu-id="c97f3-233">Этот вспомогательный класс для msRTCSIP-GlobalContainer содержит атрибуты, представляющие параметры пользователя, поддерживаемые серверами регистратора SIP.</span><span class="sxs-lookup"><span data-stu-id="c97f3-233">This auxiliary class to msRTCSIP-GlobalContainer holds attributes representing user settings maintained by the SIP Registrar servers.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c97f3-234">msRTCSIP-RouteUsage (устарело)</span><span class="sxs-lookup"><span data-stu-id="c97f3-234">msRTCSIP-RouteUsage (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="c97f3-235">Этот класс является контейнером, представляющим экземпляр использования телефонной маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="c97f3-235">This class is a container representing an instance of a phone route usage.</span></span> <span data-ttu-id="c97f3-236">Класс использования для телефонных маршрутов состоит из поля атрибута и поля Описание.</span><span class="sxs-lookup"><span data-stu-id="c97f3-236">A phone route usage class consists of an attribute field and a description field.</span></span> <span data-ttu-id="c97f3-237">Поле атрибута определяет тип использования.</span><span class="sxs-lookup"><span data-stu-id="c97f3-237">The attribute field defines a usage type.</span></span> <span data-ttu-id="c97f3-238">Поле «Описание» позволяет администраторам описать использование этого атрибута в телефонном маршруте.</span><span class="sxs-lookup"><span data-stu-id="c97f3-238">The description field allows administrators to describe the usage for this attribute in the phone route.</span></span></p></td>
<td><p><span data-ttu-id="c97f3-239">Устаревшие в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="c97f3-239">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c97f3-240">msRTCSIP-RouteUsages (устарело)</span><span class="sxs-lookup"><span data-stu-id="c97f3-240">msRTCSIP-RouteUsages (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="c97f3-241">Этот класс содержит несколько экземпляров класса msRTCSIP-RouteUsage и не содержит самих атрибутов.</span><span class="sxs-lookup"><span data-stu-id="c97f3-241">This class holds multiple instances of the msRTCSIP-RouteUsage class and does not have any attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="c97f3-242">Устаревшие в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="c97f3-242">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c97f3-243">msRTCSIP-Поиск</span><span class="sxs-lookup"><span data-stu-id="c97f3-243">msRTCSIP-Search</span></span></p></td>
<td><p><span data-ttu-id="c97f3-244">Этот вспомогательный класс для msRTCSIP-GlobalContainer содержит атрибуты, которые ограничивают область результатов поиска и управляют ей.</span><span class="sxs-lookup"><span data-stu-id="c97f3-244">This auxiliary class to msRTCSIP-GlobalContainer holds attributes that limit and control the scope of search results.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c97f3-245">msRTCSIP-Server (сервер)</span><span class="sxs-lookup"><span data-stu-id="c97f3-245">msRTCSIP-Server</span></span></p></td>
<td><p><span data-ttu-id="c97f3-246">Этот класс представляет один сервер, на котором работает Lync Server.</span><span class="sxs-lookup"><span data-stu-id="c97f3-246">This class represents a single server running Lync Server.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c97f3-247">msRTCSIP-Service</span><span class="sxs-lookup"><span data-stu-id="c97f3-247">msRTCSIP-Service</span></span></p></td>
<td><p><span data-ttu-id="c97f3-248">Этот класс содержит контейнер глобальных параметров и объект msRTCSIP-domain.</span><span class="sxs-lookup"><span data-stu-id="c97f3-248">This class holds the global settings container and msRTCSIP-Domain objects.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c97f3-249">msRTCSIP-TrustedMCU</span><span class="sxs-lookup"><span data-stu-id="c97f3-249">msRTCSIP-TrustedMCU</span></span></p></td>
<td><p><span data-ttu-id="c97f3-250">Этот класс содержит атрибуты, представляющие параметры для надежного сервера конференц-связи.</span><span class="sxs-lookup"><span data-stu-id="c97f3-250">This class holds attributes that represent settings for a trusted Conferencing server.</span></span></p></td>
<td><p><span data-ttu-id="c97f3-251">Новые возможности коммуникационного сервера 2007.</span><span class="sxs-lookup"><span data-stu-id="c97f3-251">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c97f3-252">msRTCSIP-TrustedMCUs</span><span class="sxs-lookup"><span data-stu-id="c97f3-252">msRTCSIP-TrustedMCUs</span></span></p></td>
<td><p><span data-ttu-id="c97f3-253">Этот класс содержит несколько экземпляров класса msRTCSIP-TrustedMCU и не содержит самих атрибутов.</span><span class="sxs-lookup"><span data-stu-id="c97f3-253">This class holds multiple instances of the msRTCSIP-TrustedMCU class and does not have any attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="c97f3-254">Новые возможности коммуникационного сервера 2007.</span><span class="sxs-lookup"><span data-stu-id="c97f3-254">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c97f3-255">msRTCSIP-TrustedProxies</span><span class="sxs-lookup"><span data-stu-id="c97f3-255">msRTCSIP-TrustedProxies</span></span></p></td>
<td><p><span data-ttu-id="c97f3-256">Этот класс содержит несколько классов msRTCSIP-TrustedProxy и не содержит самих атрибутов.</span><span class="sxs-lookup"><span data-stu-id="c97f3-256">This class holds multiple msRTCSIP-TrustedProxy classes and does not contain any attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="c97f3-257">Новые возможности коммуникационного сервера 2007.</span><span class="sxs-lookup"><span data-stu-id="c97f3-257">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c97f3-258">msRTCSIP-TrustedProxy</span><span class="sxs-lookup"><span data-stu-id="c97f3-258">msRTCSIP-TrustedProxy</span></span></p></td>
<td><p><span data-ttu-id="c97f3-259">Этот класс является контейнером, представляющим сервер, на котором запущен прокси-сервер.</span><span class="sxs-lookup"><span data-stu-id="c97f3-259">This class is a container representing a server running Proxy Server.</span></span> <span data-ttu-id="c97f3-260">Экземпляр этого класса создается при активации нового прокси-сервера на компьютере, Соединенном с AD DS.</span><span class="sxs-lookup"><span data-stu-id="c97f3-260">An instance of this class is created when activating a new Proxy Server on a computer joined to AD DS.</span></span></p></td>
<td><p><span data-ttu-id="c97f3-261">Новые возможности коммуникационного сервера 2007.</span><span class="sxs-lookup"><span data-stu-id="c97f3-261">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c97f3-262">msRTCSIP-TrustedServer</span><span class="sxs-lookup"><span data-stu-id="c97f3-262">msRTCSIP-TrustedServer</span></span></p></td>
<td><p><span data-ttu-id="c97f3-263">Этот класс содержит атрибуты, представляющие параметры для доверенного сервера.</span><span class="sxs-lookup"><span data-stu-id="c97f3-263">This class holds attributes that represent settings for a trusted server.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c97f3-264">msRTCSIP-TrustedService</span><span class="sxs-lookup"><span data-stu-id="c97f3-264">msRTCSIP-TrustedService</span></span></p></td>
<td><p><span data-ttu-id="c97f3-265">Этот класс является контейнером, представляющим доверенную службу, которая поддерживает маршрутизацию с помощью глобально маршрутизируемой URL-адреса агента пользователя (GRUU).</span><span class="sxs-lookup"><span data-stu-id="c97f3-265">This class is a container representing a trusted service that is routable using a Globally Routable User Agent URI (GRUU) address.</span></span> <span data-ttu-id="c97f3-266">Экземпляр этого класса создается, когда активируется новый сервер, являющийся надежным для сервера Lync Server.</span><span class="sxs-lookup"><span data-stu-id="c97f3-266">An instance of this class is created when a new server that is trusted by Lync Server is activated.</span></span> <span data-ttu-id="c97f3-267">Этот доверенный сервер должен быть присоединен к домену Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c97f3-267">This trusted server must be joined to an Active Directory domain.</span></span></p></td>
<td><p><span data-ttu-id="c97f3-268">Новые возможности коммуникационного сервера 2007.</span><span class="sxs-lookup"><span data-stu-id="c97f3-268">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c97f3-269">msRTCSIP-TrustedServices</span><span class="sxs-lookup"><span data-stu-id="c97f3-269">msRTCSIP-TrustedServices</span></span></p></td>
<td><p><span data-ttu-id="c97f3-270">Этот класс является контейнером для нескольких серверов GRUU и не содержит самих атрибутов.</span><span class="sxs-lookup"><span data-stu-id="c97f3-270">This class is a container for multiple GRUU servers and does not contain any attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="c97f3-271">Новые возможности коммуникационного сервера 2007.</span><span class="sxs-lookup"><span data-stu-id="c97f3-271">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c97f3-272">msRTCSIP-TrustedWebComponentsServer</span><span class="sxs-lookup"><span data-stu-id="c97f3-272">msRTCSIP-TrustedWebComponentsServer</span></span></p></td>
<td><p><span data-ttu-id="c97f3-273">Этот класс содержит атрибуты, представляющие параметры надежного веб-компонента.</span><span class="sxs-lookup"><span data-stu-id="c97f3-273">This class holds attributes that represent the settings for a trusted web component.</span></span></p></td>
<td><p><span data-ttu-id="c97f3-274">Новые возможности коммуникационного сервера 2007.</span><span class="sxs-lookup"><span data-stu-id="c97f3-274">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c97f3-275">msRTCSIP-TrustedWebComponentsServers</span><span class="sxs-lookup"><span data-stu-id="c97f3-275">msRTCSIP-TrustedWebComponentsServers</span></span></p></td>
<td><p><span data-ttu-id="c97f3-276">Этот класс содержит несколько экземпляров класса msRTCSIP-TrustedWebComponentServer и не содержит самих атрибутов.</span><span class="sxs-lookup"><span data-stu-id="c97f3-276">This class holds multiple instances of the msRTCSIP-TrustedWebComponentServer class and does not have any attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="c97f3-277">Новые возможности коммуникационного сервера 2007.</span><span class="sxs-lookup"><span data-stu-id="c97f3-277">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c97f3-278">msRTCSIP-UnifiedCommunications (устарело)</span><span class="sxs-lookup"><span data-stu-id="c97f3-278">msRTCSIP-UnifiedCommunications (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="c97f3-279">Этот вспомогательный класс для msRTCSIP-GlobalContainer содержит атрибуты, связанные с единым обменом данными.</span><span class="sxs-lookup"><span data-stu-id="c97f3-279">This auxiliary class to msRTCSIP-GlobalContainer holds attributes related to unified communications.</span></span></p></td>
<td><p><span data-ttu-id="c97f3-280">Устаревшие в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="c97f3-280">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c97f3-281">msRTCSIP — компоненты</span><span class="sxs-lookup"><span data-stu-id="c97f3-281">msRTCSIP-WebComponents</span></span></p></td>
<td><p><span data-ttu-id="c97f3-282">Этот класс содержит контрольную точку управления службой pointservice для сервера IIS.</span><span class="sxs-lookup"><span data-stu-id="c97f3-282">This class holds the service control pointservice control point for Internet Information Server (IIS).</span></span> <span data-ttu-id="c97f3-283">Он определяет сервер как сервер веб-компонентов.</span><span class="sxs-lookup"><span data-stu-id="c97f3-283">It identifies a server as a web components server.</span></span></p></td>
<td><p><span data-ttu-id="c97f3-284">Новые возможности коммуникационного сервера 2007.</span><span class="sxs-lookup"><span data-stu-id="c97f3-284">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c97f3-285">msRTCSIP-WebComponentsService</span><span class="sxs-lookup"><span data-stu-id="c97f3-285">msRTCSIP-WebComponentsService</span></span></p></td>
<td><p><span data-ttu-id="c97f3-286">Этот класс предоставляет ассоциацию из определенного пула к веб-компонентам, которые будут использоваться пулом.</span><span class="sxs-lookup"><span data-stu-id="c97f3-286">This class provides an association from a specific pool to the web components that the pool will use.</span></span></p></td>
<td><p><span data-ttu-id="c97f3-287">Новые возможности коммуникационного сервера 2007.</span><span class="sxs-lookup"><span data-stu-id="c97f3-287">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c97f3-288">msRTCSIP-WebComponentSettings</span><span class="sxs-lookup"><span data-stu-id="c97f3-288">msRTCSIP-WebComponentSettings</span></span></p></td>
<td><p><span data-ttu-id="c97f3-289">Этот вспомогательный класс для msRTCSIP-компонентов содержит атрибуты, представляющие параметры для веб-компонентов.</span><span class="sxs-lookup"><span data-stu-id="c97f3-289">This auxiliary class to msRTCSIP-WebComponents holds attributes representing settings for web components.</span></span></p></td>
<td><p><span data-ttu-id="c97f3-290">Новые возможности коммуникационного сервера 2007.</span><span class="sxs-lookup"><span data-stu-id="c97f3-290">New in Communications Server 2007.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="c97f3-291">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c97f3-291">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

