---
title: 'Lync Server 2013: атрибуты и описания схемы'
description: 'Lync Server 2013: атрибуты и описания схемы.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Schema attributes and descriptions
ms:assetid: b009df76-9c22-471d-b57a-bda009a98261
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412841(v=OCS.15)
ms:contentKeyID: 48185083
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 18888d20a772b3e84970e7d874bd6b6964affc75
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444961"
---
# <a name="schema-attributes-and-descriptions-in-lync-server-2013"></a><span data-ttu-id="52fc9-103">Атрибуты и описания схемы в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="52fc9-103">Schema attributes and descriptions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="52fc9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="52fc9-104">

<span> </span></span></span>

<span data-ttu-id="52fc9-105">_**Тема последнего изменения:** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="52fc9-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="52fc9-106">В этом разделе описаны все атрибуты схемы, которые используются в Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="52fc9-106">This section describes all the schema attributes used by Lync Server 2013.</span></span> <span data-ttu-id="52fc9-107">Классы, связанные с атрибутами, приведены [в разделе атрибуты схемы по классу в Lync Server 2013](lync-server-2013-schema-attributes-by-class.md).</span><span class="sxs-lookup"><span data-stu-id="52fc9-107">For the classes associated with attributes, see [Schema attributes by class in Lync Server 2013](lync-server-2013-schema-attributes-by-class.md).</span></span> <span data-ttu-id="52fc9-108">Список классов и атрибутов, новых в Lync Server 2013, можно найти [в разделе изменения схемы в Lync server 2013](lync-server-2013-schema-changes-in-lync-server-2013.md).</span><span class="sxs-lookup"><span data-stu-id="52fc9-108">For a list of classes and attributes that are new in Lync Server 2013, see [Schema changes in Lync Server 2013](lync-server-2013-schema-changes-in-lync-server-2013.md).</span></span>

<span data-ttu-id="52fc9-109">Атрибуты, которые являются связанными парами, задаются как пересылаемые ссылки или обратные ссылки.</span><span class="sxs-lookup"><span data-stu-id="52fc9-109">Attributes that are linked pairs are specified as forward links or back links.</span></span> <span data-ttu-id="52fc9-110">Атрибут, который ссылается на другой объект, является прямой ссылкой; атрибут другого объекта, который ссылается на первый объект, является обратной ссылкой.</span><span class="sxs-lookup"><span data-stu-id="52fc9-110">An attribute that refers to another object is a forward link; the attribute of the other object that refers back to the first object is a back link.</span></span> <span data-ttu-id="52fc9-111">Пересылка ссылок является обновляемой, а обратные ссылки — в режиме только для чтения.</span><span class="sxs-lookup"><span data-stu-id="52fc9-111">Forward links are updatable, while back links are read-only.</span></span>

<span data-ttu-id="52fc9-112">Некоторые атрибуты имеют значение битовой маски.</span><span class="sxs-lookup"><span data-stu-id="52fc9-112">Some attributes have a bit-mask value.</span></span> <span data-ttu-id="52fc9-113">Для этих атрибутов каждый параметр представляется битом, а отображаемое десятичное число — разрядное положение.</span><span class="sxs-lookup"><span data-stu-id="52fc9-113">For these attributes, each setting is represented by a bit, and the displayed decimal value represents the bit position.</span></span> <span data-ttu-id="52fc9-114">Битовые позиции начинаются с бита 0.</span><span class="sxs-lookup"><span data-stu-id="52fc9-114">Bit positions start with bit 0.</span></span> <span data-ttu-id="52fc9-115">Например, 1 (двоичный) является битом 0, а 10000 (двоичный) — бит 4 множества.</span><span class="sxs-lookup"><span data-stu-id="52fc9-115">For example, 1 (binary) is bit 0 set and 10000 (binary) is bit 4 set.</span></span> <span data-ttu-id="52fc9-116">Каждый бит представляет свойство.</span><span class="sxs-lookup"><span data-stu-id="52fc9-116">Each bit represents a property.</span></span> <span data-ttu-id="52fc9-117">Ниже приведено несколько примеров.</span><span class="sxs-lookup"><span data-stu-id="52fc9-117">The following are some examples:</span></span>

  - <span data-ttu-id="52fc9-118">10000 (двоичный) имеет десятичное значение 16 (то есть установлено значение bit 4).</span><span class="sxs-lookup"><span data-stu-id="52fc9-118">10000 (binary) has a decimal value of 16 (that is, bit 4 is set).</span></span>

  - <span data-ttu-id="52fc9-119">100000000 (двоичный) имеет десятичное значение 256 (то есть установлено значение bit 8).</span><span class="sxs-lookup"><span data-stu-id="52fc9-119">100000000 (binary) has a decimal value of 256 (that is, bit 8 is set).</span></span>

  - <span data-ttu-id="52fc9-120">1100 (двоичный) имеет десятичное значение 12 (это означает, что установлены биты 2 и 3; включены свойства, представленные обоими битами).</span><span class="sxs-lookup"><span data-stu-id="52fc9-120">1100 (binary) has a decimal value of 12 (that is, bits 2 and 3 are set; properties represented by both bits are enabled).</span></span>

  - <span data-ttu-id="52fc9-121">1111000001 (двоичный) имеет десятичное значение 961 (это значит, что заданы биты 0, 6, 7, 8 и 9), для каждого из этих битов включена поддержка свойств.</span><span class="sxs-lookup"><span data-stu-id="52fc9-121">1111000001 (binary) has a decimal value of 961 (that is, bits 0, 6, 7, 8, and 9 are set; properties for each of these bits are enabled).</span></span>

<div id="sectionSection0" class="section">

### <a name="schema-attributes-for-lync-server-2013"></a><span data-ttu-id="52fc9-122">Атрибуты схемы для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="52fc9-122">Schema Attributes for Lync Server 2013</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="52fc9-123">Атрибут</span><span class="sxs-lookup"><span data-stu-id="52fc9-123">Attribute</span></span></th>
<th><span data-ttu-id="52fc9-124">Описание</span><span class="sxs-lookup"><span data-stu-id="52fc9-124">Description</span></span></th>
<th><span data-ttu-id="52fc9-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="52fc9-125">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-126">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="52fc9-126">dnsHostName</span></span></p></td>
<td><p><span data-ttu-id="52fc9-127">Существующий атрибут в доменных службах Active Directory, который теперь связан с классами <strong>msRTCSIP-Pool</strong> и <strong>msRTCSIP-MonitoringServer</strong> .</span><span class="sxs-lookup"><span data-stu-id="52fc9-127">An existing attribute in Active Directory Domain Services that is now associated with the <strong>msRTCSIP-Pool</strong> and <strong>msRTCSIP-MonitoringServer</strong> classes.</span></span> <span data-ttu-id="52fc9-128">Этот атрибут указывает полное доменное имя (FQDN) для пула или сервера мониторинга.</span><span class="sxs-lookup"><span data-stu-id="52fc9-128">This attribute specifies the fully qualified domain name (FQDN) of a pool or Monitoring Server.</span></span></p>
<p><span data-ttu-id="52fc9-129">Допустимые значения для каждого сегмента — 63 символов; допустимое значение полного доменного имени — 255 символов.</span><span class="sxs-lookup"><span data-stu-id="52fc9-129">A valid value for each segment is 63 characters; a valid value for the entire FQDN is 255 characters.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-130">Новые возможности Microsoft Office Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="52fc9-130">New in Microsoft Office Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-131">msDS-SourceObjectDN</span><span class="sxs-lookup"><span data-stu-id="52fc9-131">msDS-SourceObjectDN</span></span></p></td>
<td><p><span data-ttu-id="52fc9-132">Этот атрибут представляет строковое представление различающегося имени (DN) объекта в другом лесе, которое соответствует этому объекту.</span><span class="sxs-lookup"><span data-stu-id="52fc9-132">This attribute contains the string representation of the distinguished name (DN) of the object in another forest that corresponds to this object.</span></span> <span data-ttu-id="52fc9-133">Этот атрибут используется для расширения группы рассылки и автоматического посещения.</span><span class="sxs-lookup"><span data-stu-id="52fc9-133">This attribute is used for distribution group expansion and auto attendance.</span></span> <span data-ttu-id="52fc9-134">Этот атрибут определен в схеме Active Directory, используемой по умолчанию, для Windows Server 2003 R2.</span><span class="sxs-lookup"><span data-stu-id="52fc9-134">This attribute is defined in the default Active Directory schema for Windows Server 2003 R2.</span></span></p>
<p><span data-ttu-id="52fc9-135">Чтобы не допустить необходимости обновления AD DS до Windows Server 2003 R2, подготовка схемы Active Directory расширяет схему Windows Server 2003 с помощью этого определения атрибута.</span><span class="sxs-lookup"><span data-stu-id="52fc9-135">To avoid requiring an upgrade of AD DS to Windows Server 2003 R2, Active Directory schema preparation extends the Windows Server 2003 schema with this attribute definition.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-136">Новые возможности Microsoft Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="52fc9-136">New in Microsoft Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-137">msExchUCVoiceMailSettings</span><span class="sxs-lookup"><span data-stu-id="52fc9-137">msExchUCVoiceMailSettings</span></span></p></td>
<td><p><span data-ttu-id="52fc9-138">Этот атрибут с несколькими значениями хранит параметры голосовой почты.</span><span class="sxs-lookup"><span data-stu-id="52fc9-138">This multi-valued attribute holds voice mail settings.</span></span> <span data-ttu-id="52fc9-139">Этот атрибут является общим для единой системы обмена сообщениями Exchange.</span><span class="sxs-lookup"><span data-stu-id="52fc9-139">This attribute is shared with Exchange Unified Messaging (UM).</span></span></p></td>
<td><p><span data-ttu-id="52fc9-140">Новые возможности Microsoft Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="52fc9-140">New in Microsoft Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-141">msExchUserHoldPolicies</span><span class="sxs-lookup"><span data-stu-id="52fc9-141">msExchUserHoldPolicies</span></span></p></td>
<td><p><span data-ttu-id="52fc9-142">Этот атрибут с несколькими значениями содержит идентификаторы для политик хранения, которые применяются к пользователю.</span><span class="sxs-lookup"><span data-stu-id="52fc9-142">This multi-value attribute holds identifiers for hold policies that apply to the user.</span></span> <span data-ttu-id="52fc9-143">Политики удержания сохраняют для пользователя элементы почтового ящика на время удержания.</span><span class="sxs-lookup"><span data-stu-id="52fc9-143">Hold policies preserve mailbox items for the user for the duration of the hold.</span></span> <span data-ttu-id="52fc9-144">Этот атрибут является общим для Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="52fc9-144">This attribute is shared with Exchange 2013.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-145">Новые возможности Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="52fc9-145">New in Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-146">msRTCSIP-AcpInfo</span><span class="sxs-lookup"><span data-stu-id="52fc9-146">msRTCSIP-AcpInfo</span></span></p></td>
<td><p><span data-ttu-id="52fc9-147">Этот атрибут хранит сведения о поставщике голосовой конференции для пользователя.</span><span class="sxs-lookup"><span data-stu-id="52fc9-147">This attribute stores audio conferencing provider information for a user.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-148">Новые возможности Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="52fc9-148">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-149">msRTCSIP-ApplicationDestination</span><span class="sxs-lookup"><span data-stu-id="52fc9-149">msRTCSIP-ApplicationDestination</span></span></p></td>
<td><p><span data-ttu-id="52fc9-150">Этот атрибут указывает на запись доверенной службы для контакта приложения.</span><span class="sxs-lookup"><span data-stu-id="52fc9-150">This attribute points to the trusted service entry for the application contact.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-151">Новые возможности Microsoft Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="52fc9-151">New in Microsoft Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-152">msRTCSIP-ApplicationList</span><span class="sxs-lookup"><span data-stu-id="52fc9-152">msRTCSIP-ApplicationList</span></span></p></td>
<td><p><span data-ttu-id="52fc9-153">Этот атрибут включает список размещенных приложений на сервере приложений.</span><span class="sxs-lookup"><span data-stu-id="52fc9-153">This attribute contains a list of hosted applications on the application server.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-154">Новые возможности Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="52fc9-154">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-155">msRTCSIP-ApplicationOptions</span><span class="sxs-lookup"><span data-stu-id="52fc9-155">msRTCSIP-ApplicationOptions</span></span></p></td>
<td><p><span data-ttu-id="52fc9-156">Этот атрибут определяет параметры для контакта приложения.</span><span class="sxs-lookup"><span data-stu-id="52fc9-156">This attribute specifies the options for the application contact.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-157">Новые возможности Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="52fc9-157">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-158">msRTCSIP-ApplicationPrimaryLanguage</span><span class="sxs-lookup"><span data-stu-id="52fc9-158">msRTCSIP-ApplicationPrimaryLanguage</span></span></p></td>
<td><p><span data-ttu-id="52fc9-159">Этот атрибут включает основной язык для контакта приложения.</span><span class="sxs-lookup"><span data-stu-id="52fc9-159">This attribute contains the primary language for the application contact.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-160">Новые возможности Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="52fc9-160">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-161">msRTCSIP-ApplicationSecondaryLanguages</span><span class="sxs-lookup"><span data-stu-id="52fc9-161">msRTCSIP-ApplicationSecondaryLanguages</span></span></p></td>
<td><p><span data-ttu-id="52fc9-162">Этот многозначный атрибут имеет дополнительные языки для контакта приложения.</span><span class="sxs-lookup"><span data-stu-id="52fc9-162">This multiple value attribute contains the secondary languages for the application contact.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-163">Новые возможности Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="52fc9-163">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-164">msRTCSIP-ApplicationServerBL</span><span class="sxs-lookup"><span data-stu-id="52fc9-164">msRTCSIP-ApplicationServerBL</span></span></p></td>
<td><p><span data-ttu-id="52fc9-165">Этот атрибут включает список серверов приложений, входящих в этот пул.</span><span class="sxs-lookup"><span data-stu-id="52fc9-165">This attribute contains a list of application servers that belong to this pool.</span></span> <span data-ttu-id="52fc9-166">Соответствующая ссылка для перехода на этот атрибут обратной ссылки — <strong>msRTCSIP-ApplicationServerPoolLink</strong>.</span><span class="sxs-lookup"><span data-stu-id="52fc9-166">The corresponding forward link to this back link attribute is <strong>msRTCSIP-ApplicationServerPoolLink</strong>.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-167">Новые возможности Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="52fc9-167">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-168">msRTCSIP-ApplicationServerPoolLink</span><span class="sxs-lookup"><span data-stu-id="52fc9-168">msRTCSIP-ApplicationServerPoolLink</span></span></p></td>
<td><p><span data-ttu-id="52fc9-169">Этот атрибут указывает на пул, к которому относится этот сервер приложений.</span><span class="sxs-lookup"><span data-stu-id="52fc9-169">This attribute points to the pool to which this application server belongs.</span></span> <span data-ttu-id="52fc9-170">Это пересылка ссылки.</span><span class="sxs-lookup"><span data-stu-id="52fc9-170">This is the forward link.</span></span> <span data-ttu-id="52fc9-171">Соответствующая обратная ссылка — <strong>msRTCSIP-ApplicationServerBL</strong>.</span><span class="sxs-lookup"><span data-stu-id="52fc9-171">The corresponding backward link is <strong>msRTCSIP-ApplicationServerBL</strong>.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-172">Новые возможности Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="52fc9-172">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-173">msRTCSIP-ArchiveDefault (устарело)</span><span class="sxs-lookup"><span data-stu-id="52fc9-173">msRTCSIP-ArchiveDefault (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="52fc9-174">Новые возможности Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="52fc9-174">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="52fc9-175">Устаревшие в Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="52fc9-175">Obsolete in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-176">msRTCSIP-ArchiveDefaultFlags (устарело)</span><span class="sxs-lookup"><span data-stu-id="52fc9-176">msRTCSIP-ArchiveDefaultFlags (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="52fc9-177">Этот атрибут определяет глобальное значение по умолчанию в пределах границы леса для архивации всех пользовательских сообщений.</span><span class="sxs-lookup"><span data-stu-id="52fc9-177">This attribute specifies the global default within the forest boundary for archiving all user communications.</span></span> <span data-ttu-id="52fc9-178">Это действие обеспечивается уровнем агента архивации.</span><span class="sxs-lookup"><span data-stu-id="52fc9-178">This is enforced by the archiving agent layer.</span></span> <span data-ttu-id="52fc9-179">Диапазон значений для этого атрибута выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="52fc9-179">The range of values for this attribute is as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="52fc9-180"><strong>Истина</strong>: архивация всех пользователей</span><span class="sxs-lookup"><span data-stu-id="52fc9-180"><strong>TRUE</strong>: Archive all users</span></span></p></li>
<li><p><span data-ttu-id="52fc9-181"><strong>False</strong>: не архивировать всех пользователей</span><span class="sxs-lookup"><span data-stu-id="52fc9-181"><strong>FALSE</strong>: Do not archive all users</span></span></p></li>
</ul>
<p><span data-ttu-id="52fc9-182">Этот атрибут глобально Controls в пределах границы леса, в котором архивируются сведения о взаимодействии пользователей во внутренней сети.</span><span class="sxs-lookup"><span data-stu-id="52fc9-182">This attribute globally controls, within the forest boundary, how user communications within an internal network are archived.</span></span></p>
<p><span data-ttu-id="52fc9-183"><strong>Поведение сервера Live Communications Server 2005 (теперь оно устарело)</strong></span><span class="sxs-lookup"><span data-stu-id="52fc9-183"><strong>Live Communications Server 2005 behavior (now retired)</strong></span></span></p>
<p><span data-ttu-id="52fc9-184">Диапазон значений для этого атрибута выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="52fc9-184">The range of values for this attribute is as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="52fc9-185">0: Архивация текста сообщения [бит 0]</span><span class="sxs-lookup"><span data-stu-id="52fc9-185">0: Archive the message body [bit 0]</span></span></p></li>
<li><p><span data-ttu-id="52fc9-186">1: не архивируйте текст сообщения [бит 0]</span><span class="sxs-lookup"><span data-stu-id="52fc9-186">1: Do not archive the message body [bit 0]</span></span></p></li>
</ul>
<p><span data-ttu-id="52fc9-187"><strong>Поведение сервера Office Communications Server 2007</strong></span><span class="sxs-lookup"><span data-stu-id="52fc9-187"><strong>Office Communications Server 2007 behavior</strong></span></span></p>
<p><span data-ttu-id="52fc9-188">Диапазон значений для этого атрибута выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="52fc9-188">The range of values for this attribute is as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="52fc9-189">0: ArchiveFederationDefaultWithoutBody (устарело)</span><span class="sxs-lookup"><span data-stu-id="52fc9-189">0: ArchiveFederationDefaultWithoutBody (retired)</span></span></p></li>
<li><p><span data-ttu-id="52fc9-190">1-2: ArchiveInternalCommunications</span><span class="sxs-lookup"><span data-stu-id="52fc9-190">1-2: ArchiveInternalCommunications</span></span></p></li>
<li><p><span data-ttu-id="52fc9-191">3-4: ArchiveFederatedCommunications</span><span class="sxs-lookup"><span data-stu-id="52fc9-191">3-4: ArchiveFederatedCommunications</span></span></p></li>
<li><p><span data-ttu-id="52fc9-192">5: RecordPresenceRegistrations</span><span class="sxs-lookup"><span data-stu-id="52fc9-192">5: RecordPresenceRegistrations</span></span></p></li>
<li><p><span data-ttu-id="52fc9-193">6: RecordIMCallDetails</span><span class="sxs-lookup"><span data-stu-id="52fc9-193">6: RecordIMCallDetails</span></span></p></li>
<li><p><span data-ttu-id="52fc9-194">7: RecordGroupIMCallDetails</span><span class="sxs-lookup"><span data-stu-id="52fc9-194">7: RecordGroupIMCallDetails</span></span></p></li>
<li><p><span data-ttu-id="52fc9-195">8: RecordFileTransferInstances</span><span class="sxs-lookup"><span data-stu-id="52fc9-195">8: RecordFileTransferInstances</span></span></p></li>
<li><p><span data-ttu-id="52fc9-196">9: RecordAudioCallDetails</span><span class="sxs-lookup"><span data-stu-id="52fc9-196">9: RecordAudioCallDetails</span></span></p></li>
<li><p><span data-ttu-id="52fc9-197">10: RecordVideoCallDetails</span><span class="sxs-lookup"><span data-stu-id="52fc9-197">10: RecordVideoCallDetails</span></span></p></li>
<li><p><span data-ttu-id="52fc9-198">11: RecordRemoteAssistanceCallDetails</span><span class="sxs-lookup"><span data-stu-id="52fc9-198">11: RecordRemoteAssistanceCallDetails</span></span></p></li>
<li><p><span data-ttu-id="52fc9-199">12: RecordApplicationSharingDetails</span><span class="sxs-lookup"><span data-stu-id="52fc9-199">12: RecordApplicationSharingDetails</span></span></p></li>
<li><p><span data-ttu-id="52fc9-200">13: RecordMeetingInstantiations</span><span class="sxs-lookup"><span data-stu-id="52fc9-200">13: RecordMeetingInstantiations</span></span></p></li>
<li><p><span data-ttu-id="52fc9-201">14: RecordMeetingJoins</span><span class="sxs-lookup"><span data-stu-id="52fc9-201">14: RecordMeetingJoins</span></span></p></li>
<li><p><span data-ttu-id="52fc9-202">15: RecordDataJoins</span><span class="sxs-lookup"><span data-stu-id="52fc9-202">15: RecordDataJoins</span></span></p></li>
<li><p><span data-ttu-id="52fc9-203">16: RecordAVJoins</span><span class="sxs-lookup"><span data-stu-id="52fc9-203">16: RecordAVJoins</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="52fc9-204">Новые возможности Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="52fc9-204">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="52fc9-205">Устаревшие в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="52fc9-205">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-206">msRTCSIP-ArchiveFederationDefault (устарело)</span><span class="sxs-lookup"><span data-stu-id="52fc9-206">msRTCSIP-ArchiveFederationDefault (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="52fc9-207">Новые возможности Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="52fc9-207">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="52fc9-208">Устаревшие в Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="52fc9-208">Obsolete in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-209">msRTCSIP-ArchiveFederationDefaultFlags (устарело)</span><span class="sxs-lookup"><span data-stu-id="52fc9-209">msRTCSIP-ArchiveFederationDefaultFlags (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="52fc9-210">Новые возможности Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="52fc9-210">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="52fc9-211">Устаревшие в Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="52fc9-211">Obsolete in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-212">msRTCSIP-ArchivingEnabled</span><span class="sxs-lookup"><span data-stu-id="52fc9-212">msRTCSIP-ArchivingEnabled</span></span></p></td>
<td><p><span data-ttu-id="52fc9-213">Этот атрибут является целым числом, используемым в качестве битового поля, чтобы указать, нужно ли архивировать связь отдельного пользователя.</span><span class="sxs-lookup"><span data-stu-id="52fc9-213">This attribute is an integer used as a bit field to control whether a single user’s communications are to be archived.</span></span> <span data-ttu-id="52fc9-214">Этот элемент управления принудительно применяется уровнем агента архивации.</span><span class="sxs-lookup"><span data-stu-id="52fc9-214">This control is enforced by the archiving agent layer.</span></span> <span data-ttu-id="52fc9-215">Оно помечено для репликации глобального каталога.</span><span class="sxs-lookup"><span data-stu-id="52fc9-215">It is marked for global catalog replication.</span></span></p>
<p><span data-ttu-id="52fc9-216">Область действия этого атрибута зависит от одного пользователя или контакта.</span><span class="sxs-lookup"><span data-stu-id="52fc9-216">The scope of this attribute is specific to a single user or contact.</span></span> <span data-ttu-id="52fc9-217">Допустимые значения (и связанные с ними битовые позиции) в Lync Server описаны ниже.</span><span class="sxs-lookup"><span data-stu-id="52fc9-217">The valid values (and associated bit positions) in Lync Server are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="52fc9-218">0: не архивировать (не установлен бит)</span><span class="sxs-lookup"><span data-stu-id="52fc9-218">0: Do not archive (no bit set)</span></span></p></li>
<li><p><span data-ttu-id="52fc9-219">1: устарело (разрядное расположение 0)</span><span class="sxs-lookup"><span data-stu-id="52fc9-219">1: Retired (bit position 0)</span></span></p></li>
<li><p><span data-ttu-id="52fc9-220">2: устарело (разрядное расположение 1)</span><span class="sxs-lookup"><span data-stu-id="52fc9-220">2: Retired (bit position 1)</span></span></p></li>
<li><p><span data-ttu-id="52fc9-221">4: Архивация внутренних сообщений (разрядность 2)</span><span class="sxs-lookup"><span data-stu-id="52fc9-221">4: Archive internal communications (bit position 2)</span></span></p></li>
<li><p><span data-ttu-id="52fc9-222">8: Архивация федеративных коммуникаций (разрядное расположение 3)</span><span class="sxs-lookup"><span data-stu-id="52fc9-222">8: Archive federated communications (bit position 3)</span></span></p></li>
</ul>
<p><span data-ttu-id="52fc9-223">Ранее действительные значения в режиме Live Communications Server 2005 описаны ниже.</span><span class="sxs-lookup"><span data-stu-id="52fc9-223">Previously valid values in Live Communications Server 2005 are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="52fc9-224">0: используйте значение по умолчанию, определяемое <strong>msRTCSIP-ArchiveDefault</strong> и <strong>msRTCSIP-ArchiveFederation</strong> в следующем порядке приоритета:</span><span class="sxs-lookup"><span data-stu-id="52fc9-224">0:Use the default value defined by <strong>msRTCSIP-ArchiveDefault</strong> and <strong>msRTCSIP-ArchiveFederation</strong> in this order of precedence:</span></span></p>
<ul>
<li><p><span data-ttu-id="52fc9-225">1: Архив</span><span class="sxs-lookup"><span data-stu-id="52fc9-225">1: Archive</span></span></p></li>
<li><p><span data-ttu-id="52fc9-226">2: не архивировать</span><span class="sxs-lookup"><span data-stu-id="52fc9-226">2: Do not archive</span></span></p></li>
<li><p><span data-ttu-id="52fc9-227">3: Архивация без текста сообщения</span><span class="sxs-lookup"><span data-stu-id="52fc9-227">3: Archive without the message body</span></span></p></li>
</ul></li>
</ul></td>
<td><p><span data-ttu-id="52fc9-228">Новые возможности Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="52fc9-228">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-229">msRTCSIP-ArchivingServerData (устарело)</span><span class="sxs-lookup"><span data-stu-id="52fc9-229">msRTCSIP-ArchivingServerData (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="52fc9-230">Этот атрибут зарезервирован для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="52fc9-230">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-231">Устаревшие в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="52fc9-231">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-232">msRTCSIP-ArchivingServerVersion (устарело)</span><span class="sxs-lookup"><span data-stu-id="52fc9-232">msRTCSIP-ArchivingServerVersion (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="52fc9-233">Этот атрибут определяет версию службы архивации.</span><span class="sxs-lookup"><span data-stu-id="52fc9-233">This attribute defines the version of the Archiving service.</span></span> <span data-ttu-id="52fc9-234">Этот атрибут является monotonously увеличивающимся целочисленным типом, увеличивающимся до каждого официального выпуска продукта.</span><span class="sxs-lookup"><span data-stu-id="52fc9-234">This attribute is a monotonously increasing integer type that increments with each official product release.</span></span> <span data-ttu-id="52fc9-235">Возможные допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="52fc9-235">The possible valid values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="52fc9-236">Не определено: сервер Live Communications Server 2003</span><span class="sxs-lookup"><span data-stu-id="52fc9-236">Undefined: Live Communications Server 2003</span></span></p>
<p>                 <span data-ttu-id="52fc9-237">Live Communications Server 2005</span><span class="sxs-lookup"><span data-stu-id="52fc9-237">Live Communications Server 2005</span></span></p>
<p>                 <span data-ttu-id="52fc9-238">Live Communications Server 2005 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="52fc9-238">Live Communications Server 2005 with SP1</span></span></p></li>
<li><p><span data-ttu-id="52fc9-239">3: Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="52fc9-239">3: Office Communications Server 2007</span></span></p></li>
<li><p><span data-ttu-id="52fc9-240">4: Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="52fc9-240">4: Office Communications Server 2007 R2</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="52fc9-241">Новые возможности Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="52fc9-241">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="52fc9-242">Устаревшие в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="52fc9-242">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-243">msRTCSIP-BackEndServer</span><span class="sxs-lookup"><span data-stu-id="52fc9-243">msRTCSIP-BackEndServer</span></span></p></td>
<td><p><span data-ttu-id="52fc9-244">Этот атрибут указывает полное доменное имя сервера, на котором находится пул.</span><span class="sxs-lookup"><span data-stu-id="52fc9-244">This attribute specifies the FQDN of the Back End Server of the pool.</span></span> <span data-ttu-id="52fc9-245">Так как в каждом пуле может быть только один сервер, это является атрибутом с одним значением.</span><span class="sxs-lookup"><span data-stu-id="52fc9-245">Because there can only be a single Back End Server per pool, this is a single-valued attribute.</span></span></p>
<p><span data-ttu-id="52fc9-246">Допустимые значения для каждого сегмента — 63 символов; допустимое значение полного доменного имени — 255 символов.</span><span class="sxs-lookup"><span data-stu-id="52fc9-246">The valid value for each segment is 63 characters; the valid value for the entire FQDN is 255 characters.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-247">Новые возможности Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="52fc9-247">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-248">msRTCSIP-ConferenceDirectoryHomePool</span><span class="sxs-lookup"><span data-stu-id="52fc9-248">msRTCSIP-ConferenceDirectoryHomePool</span></span></p></td>
<td><p><span data-ttu-id="52fc9-249">Этот атрибут содержит идентификатор пула, на котором размещен каталог конференций.</span><span class="sxs-lookup"><span data-stu-id="52fc9-249">This attribute contains the identifier of the pool that hosts the conference directory.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-250">Новые возможности Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="52fc9-250">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-251">msRTCSIP-ConferenceDirectoryId</span><span class="sxs-lookup"><span data-stu-id="52fc9-251">msRTCSIP-ConferenceDirectoryId</span></span></p></td>
<td><p><span data-ttu-id="52fc9-252">Этот атрибут включает идентификатор каталога конференций.</span><span class="sxs-lookup"><span data-stu-id="52fc9-252">This attribute contains the identifier of a conference directory.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-253">Новые возможности Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="52fc9-253">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-254">msRTCSIP-ConferenceDirectoryTargetPool</span><span class="sxs-lookup"><span data-stu-id="52fc9-254">msRTCSIP-ConferenceDirectoryTargetPool</span></span></p></td>
<td><p><span data-ttu-id="52fc9-255">Этот атрибут содержит идентификатор пула, в который перемещается Каталог конференций.</span><span class="sxs-lookup"><span data-stu-id="52fc9-255">This attribute contains the identifier of the pool to which the conference directory is being moved.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-256">Новые возможности Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="52fc9-256">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-257">msRTCSIP — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="52fc9-257">msRTCSIP-Default</span></span></p></td>
<td><p><span data-ttu-id="52fc9-258">Этот логический атрибут определяет, используется ли по умолчанию использование телефона.</span><span class="sxs-lookup"><span data-stu-id="52fc9-258">This Boolean attribute defines whether the phone usage is a default usage.</span></span> <span data-ttu-id="52fc9-259">Если для этого атрибута установлено <strong>значение true</strong>, использование телефона является использованием по умолчанию и не может быть удалено администратором.</span><span class="sxs-lookup"><span data-stu-id="52fc9-259">If this attribute is set to <strong>TRUE</strong>, the phone usage is a default usage and cannot be deleted by the administrator.</span></span> <span data-ttu-id="52fc9-260">Если для атрибута задано значение <strong>false</strong>, использование может быть удалено.</span><span class="sxs-lookup"><span data-stu-id="52fc9-260">If this attribute is set to <strong>FALSE</strong>, the usage can be deleted.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-261">Новые возможности Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="52fc9-261">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-262">msRTCSIP-DefaultCWAExternalURL</span><span class="sxs-lookup"><span data-stu-id="52fc9-262">msRTCSIP-DefaultCWAExternalURL</span></span></p></td>
<td><p><span data-ttu-id="52fc9-263">Этот атрибут определяет URL-адрес Communicator Web Access для пользователей, которые находятся за пределами Организации.</span><span class="sxs-lookup"><span data-stu-id="52fc9-263">This attribute identifies the Communicator Web Access URL for users who are outside the organization.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-264">Новые возможности Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="52fc9-264">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-265">msRTCSIP-DefaultCWAInternalURL</span><span class="sxs-lookup"><span data-stu-id="52fc9-265">msRTCSIP-DefaultCWAInternalURL</span></span></p></td>
<td><p><span data-ttu-id="52fc9-266">Этот атрибут определяет URL-адрес Communicator Web Access для пользователей в Организации.</span><span class="sxs-lookup"><span data-stu-id="52fc9-266">This attribute identifies the Communicator Web Access URL for users who are inside the organization.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-267">Новые возможности Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="52fc9-267">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-268">msRTCSIP-DefaultLocationProfileLink (устарело)</span><span class="sxs-lookup"><span data-stu-id="52fc9-268">msRTCSIP-DefaultLocationProfileLink (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="52fc9-269">Этот атрибут с одним значением включает различающееся имя (DN) объекта класса профиля расположения, присвоенного ему.</span><span class="sxs-lookup"><span data-stu-id="52fc9-269">This single-valued attribute contains the distinguished name (DN) of a location profile class object assigned to it.</span></span></p>
<p><span data-ttu-id="52fc9-270">Ссылка "вперед": <strong>ИД ссылки 11036</strong></span><span class="sxs-lookup"><span data-stu-id="52fc9-270">Forward link: <strong>Link ID 11036</strong></span></span></p>
<p><span data-ttu-id="52fc9-271">Соответствующая обратная ссылка — <strong>msRTCSIP-ServerReferenceBL</strong>.</span><span class="sxs-lookup"><span data-stu-id="52fc9-271">The corresponding backward link is <strong>msRTCSIP-ServerReferenceBL</strong>.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-272">Устаревшие в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="52fc9-272">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-273">msRTCSIP-DefaultPolicy (устарело)</span><span class="sxs-lookup"><span data-stu-id="52fc9-273">msRTCSIP-DefaultPolicy (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="52fc9-274">Этот логический атрибут указывает, является ли политика политикой по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="52fc9-274">This Boolean attribute specifies whether the policy is a default policy.</span></span> <span data-ttu-id="52fc9-275">Политика — это политика по умолчанию, для которой установлено <strong>значение true</strong>.</span><span class="sxs-lookup"><span data-stu-id="52fc9-275">The policy is a default policy when set to <strong>TRUE</strong>.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-276">Новые возможности Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="52fc9-276">New in Office Communications Server 2007</span></span></p>
<p><span data-ttu-id="52fc9-277">Устаревшие в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="52fc9-277">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-278">msRTCSIP-DefaultRouteToEdgeProxy (устарело)</span><span class="sxs-lookup"><span data-stu-id="52fc9-278">msRTCSIP-DefaultRouteToEdgeProxy (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="52fc9-279">Этот атрибут указывает полное доменное имя либо для пограничного сервера, на котором запущена служба Edge Access, если к нему есть прямой доступ, либо из подсистемы балансировки нагрузки для пула серверов, на котором запущена служба пограничного доступа.</span><span class="sxs-lookup"><span data-stu-id="52fc9-279">This attribute specifies the FQDN of either the Edge Server running the Access Edge service, if it can be accessed directly, or of the hardware load balancer for a pool of servers running Access Edge service.</span></span> <span data-ttu-id="52fc9-280">Если доступ к службам пограничного сервера Access возможен только через одного или нескольких режиссеров, этот атрибут указывает полное доменное имя и, при необходимости, номер порта режиссера или аппаратного балансировщика подсистемы балансировки нагрузки, обслуживающего каталог пула.</span><span class="sxs-lookup"><span data-stu-id="52fc9-280">If the servers running Access Edge service can be accessed only through one or more Directors, this attribute specifies the FQDN and, optionally, the port number of the Director or of the hardware load balancer serving a Director pool.</span></span></p>
<p><span data-ttu-id="52fc9-281">Допустимые значения для каждого сегмента — 63 символов; допустимое значение полного доменного имени — 255 символов.</span><span class="sxs-lookup"><span data-stu-id="52fc9-281">The valid value for each segment is 63 characters; the valid value for the entire FQDN is 255 characters.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-282">Новые возможности Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="52fc9-282">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="52fc9-283">Устаревшие в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="52fc9-283">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-284">msRTCSIP-DefaultRouteToEdgeProxyPort (устарело)</span><span class="sxs-lookup"><span data-stu-id="52fc9-284">msRTCSIP-DefaultRouteToEdgeProxyPort (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="52fc9-285">Этот атрибут представляет номер порта, который должен использоваться для подключения к серверу, на котором запущена служба пограничного доступа.</span><span class="sxs-lookup"><span data-stu-id="52fc9-285">This attribute represents the port number that should be used to connect to the server running Access Edge service.</span></span></p>
<p><span data-ttu-id="52fc9-286">Допустимое значение — это целое число, задающее используемый порт.</span><span class="sxs-lookup"><span data-stu-id="52fc9-286">The valid value is an integer value specifying the port to be used.</span></span> <span data-ttu-id="52fc9-287">Значение по умолчанию — 5061.</span><span class="sxs-lookup"><span data-stu-id="52fc9-287">The default value is 5061.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-288">Новые возможности Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="52fc9-288">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="52fc9-289">Устаревшие в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="52fc9-289">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-290">msRTCSIP-DefPresenceSubscriptionTimeout (устарело)</span><span class="sxs-lookup"><span data-stu-id="52fc9-290">msRTCSIP-DefPresenceSubscriptionTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="52fc9-291">Этот атрибут представляет период ожидания подписки на присутствие по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="52fc9-291">This attribute represents the default presence subscription time-out period.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-292">Устаревшие в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="52fc9-292">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-293">msRTCSIP-DefRegistrationTimeout (устарело)</span><span class="sxs-lookup"><span data-stu-id="52fc9-293">msRTCSIP-DefRegistrationTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="52fc9-294">Этот атрибут представляет окно времени ожидания регистрации по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="52fc9-294">This attribute represents the default registration time-out window.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-295">Устаревшие в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="52fc9-295">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-296">msRTCSIP-DefRoamingDataSubscriptionTimeout (устарело)</span><span class="sxs-lookup"><span data-stu-id="52fc9-296">msRTCSIP-DefRoamingDataSubscriptionTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="52fc9-297">Этот атрибут представляет окно времени ожидания для подписки на перемещаемые данные по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="52fc9-297">This attribute represents the default roaming data subscription time-out window.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-298">Устаревшие в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="52fc9-298">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-299">msRTCSIP-DeploymentLocator</span><span class="sxs-lookup"><span data-stu-id="52fc9-299">msRTCSIP-DeploymentLocator</span></span></p></td>
<td><p><span data-ttu-id="52fc9-300">Этот атрибут используется в топологии разделения доменов и содержит полное доменное имя (FQDN).</span><span class="sxs-lookup"><span data-stu-id="52fc9-300">This attribute is used in a split domain topology and contains a fully qualified domain name (FQDN).</span></span></p></td>
<td><p><span data-ttu-id="52fc9-301">Новые возможности Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="52fc9-301">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-302">msRTCSIP — описание (устарело)</span><span class="sxs-lookup"><span data-stu-id="52fc9-302">msRTCSIP-Description (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="52fc9-303">Этот однозначный строковый атрибут Юникода включает понятное описание этого маршрута или правила нормализации.</span><span class="sxs-lookup"><span data-stu-id="52fc9-303">This single-valued UNICODE string attribute contains a friendly description of this phone route or normalization rule.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-304">Новые возможности Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="52fc9-304">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="52fc9-305">Устаревшие в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="52fc9-305">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-306">msRTCSIP-DomainData</span><span class="sxs-lookup"><span data-stu-id="52fc9-306">msRTCSIP-DomainData</span></span></p></td>
<td><p><span data-ttu-id="52fc9-307">Этот атрибут зарезервирован для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="52fc9-307">This attribute is reserved for future use.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-308">msRTCSIP-имя_домена</span><span class="sxs-lookup"><span data-stu-id="52fc9-308">msRTCSIP-DomainName</span></span></p></td>
<td><p><span data-ttu-id="52fc9-309">Этот атрибут представляет домен, настроенный для регистратора.</span><span class="sxs-lookup"><span data-stu-id="52fc9-309">This attribute represents a domain configured for the Registrar.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-310">msRTCSIP-EdgeProxyData</span><span class="sxs-lookup"><span data-stu-id="52fc9-310">msRTCSIP-EdgeProxyData</span></span></p></td>
<td><p><span data-ttu-id="52fc9-311">Этот атрибут зарезервирован для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="52fc9-311">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-312">Новые возможности Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="52fc9-312">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-313">msRTCSIP-EdgeProxyFQDN</span><span class="sxs-lookup"><span data-stu-id="52fc9-313">msRTCSIP-EdgeProxyFQDN</span></span></p></td>
<td><p><span data-ttu-id="52fc9-314">Этот атрибут указывает полное доменное имя сервера, на котором запущена служба пограничного доступа.</span><span class="sxs-lookup"><span data-stu-id="52fc9-314">This attribute specifies the FQDN of the server running Access Edge service.</span></span></p>
<p><span data-ttu-id="52fc9-315">Допустимые значения для каждого сегмента — 63 символов; допустимое значение полного доменного имени — 255 символов.</span><span class="sxs-lookup"><span data-stu-id="52fc9-315">The valid value for each segment is 63 characters; the valid value for the entire FQDN is 255 characters.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-316">Новые возможности Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="52fc9-316">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-317">msRTCSIP-EnableBestEffortNotify (устарело)</span><span class="sxs-lookup"><span data-stu-id="52fc9-317">msRTCSIP-EnableBestEffortNotify (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="52fc9-318">Этот атрибут определяет, будет ли сервер создавать запрос уведомления о неэффективном выполнении (уведомления), а не запрос уведомления в ответ на запрос подписки от клиента.</span><span class="sxs-lookup"><span data-stu-id="52fc9-318">This attribute controls whether a server generates a Best Effort NOTIFY (BENOTIFY) request, instead of a NOTIFY request, in response to a SUBSCRIBE request from a client.</span></span> <span data-ttu-id="52fc9-319">УВЕДОМЛЕНИЕ — это расширение с повышенной производительностью для подтверждения подписки на подписку, в котором сервер генерирует запросы уведомлений, а не обычные уведомления.</span><span class="sxs-lookup"><span data-stu-id="52fc9-319">BENOTIFY is a performance-enhancing extension to the subscribe notification handshake where the server generates BENOTIFY requests, instead of regular NOTIFY requests.</span></span> <span data-ttu-id="52fc9-320">Преимущество в производительности заключается в том, что запрос на уведомление не требует ответа на 200 ОК от клиента в ответ на запрос уведомления.</span><span class="sxs-lookup"><span data-stu-id="52fc9-320">The performance benefit is that a BENOTIFY request does not require a 200 OK response from the client as the NOTIFY request does.</span></span></p>
<p><span data-ttu-id="52fc9-321">Допустимые значения: <strong>true</strong> или <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="52fc9-321">The valid values are <strong>TRUE</strong> or <strong>FALSE</strong>.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="52fc9-322">Сервер Live Communications Server 2003 не поддерживает уведомления запросов.</span><span class="sxs-lookup"><span data-stu-id="52fc9-322">Live Communications Server 2003 does not support BENOTIFY requests.</span></span> <span data-ttu-id="52fc9-323">Для взаимодействия с серверными приложениями, написанными с помощью API сервера Live Communications Server 2003, работающего на сервере Live Communications Server 2005 и сторонних серверах, запросы уведомления можно отключить, задавая для них значение <STRONG>false</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="52fc9-323">To interoperate with server applications written with the Live Communications Server 2003 server API running on Live Communications Server 2005 and third-party servers, BENOTIFY requests can be disabled by setting its value to <STRONG>FALSE</STRONG>.</span></span> <span data-ttu-id="52fc9-324">В настоящее время уведомления не входят в стандарт IETF (задачи по проектированию Интернета), процесс стандартизации SIP.</span><span class="sxs-lookup"><span data-stu-id="52fc9-324">BENOTIFY is not currently part of the IETF (Internet Engineering Task Force) SIP standardization process.</span></span>


</div></td>
<td><p><span data-ttu-id="52fc9-325">Новые возможности Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="52fc9-325">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="52fc9-326">Устаревшие в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="52fc9-326">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-327">msRTCSIP-EnableFederation (устарело)</span><span class="sxs-lookup"><span data-stu-id="52fc9-327">msRTCSIP-EnableFederation (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="52fc9-328">Этот атрибут является глобальным переключателем, с помощью которого администраторы могут настроить, разрешено ли пользователям взаимодействовать с пользователями из других организаций.</span><span class="sxs-lookup"><span data-stu-id="52fc9-328">This attribute is a global switch that IT administrators use to configure whether users are allowed to communicate with users from other organizations.</span></span> <span data-ttu-id="52fc9-329">Он позволяет администратору перезаписать атрибут <strong>FederationEnabled</strong> отдельного пользователя.</span><span class="sxs-lookup"><span data-stu-id="52fc9-329">It enables an administrator to overwrite an individual user’s <strong>FederationEnabled</strong> attribute.</span></span> <span data-ttu-id="52fc9-330">Этот атрибут полезен для защиты внутренней сети от атак из Интернета, которые могут быть вызваны червем, вирусами или целевыми атаками в компании.</span><span class="sxs-lookup"><span data-stu-id="52fc9-330">This attribute can be useful to help protect the internal network from Internet attacks that may be caused by worms, viruses, or targeted attacks on the company.</span></span></p>
<p><span data-ttu-id="52fc9-331">Допустимые значения (и связанные с ними битовые положения) приведены ниже.</span><span class="sxs-lookup"><span data-stu-id="52fc9-331">The valid values (and associated bit positions) are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="52fc9-332">1: включено для общедоступной службы обмена мгновенными сообщениями (разрядное расположение 0)</span><span class="sxs-lookup"><span data-stu-id="52fc9-332">1: Enabled for public IM connectivity (bit position 0)</span></span></p></li>
<li><p><span data-ttu-id="52fc9-333">2: зарезервировано (разрядное расположение 1)</span><span class="sxs-lookup"><span data-stu-id="52fc9-333">2: Reserved (bit position 1)</span></span></p></li>
<li><p><span data-ttu-id="52fc9-334">4: зарезервировано (разрядное расположение 2)</span><span class="sxs-lookup"><span data-stu-id="52fc9-334">4: Reserved (bit position 2)</span></span></p></li>
<li><p><span data-ttu-id="52fc9-335">8: зарезервировано (разрядное расположение 3)</span><span class="sxs-lookup"><span data-stu-id="52fc9-335">8: Reserved (bit position 3)</span></span></p></li>
<li><p><span data-ttu-id="52fc9-336">16: удаленное управление звонками включено [телефония] (разрядность 4)</span><span class="sxs-lookup"><span data-stu-id="52fc9-336">16: Remote call control Enabled [Telephony] (bit position 4)</span></span></p></li>
<li><p><span data-ttu-id="52fc9-337">64: AllowOrganizeMeetingWithAnonymousParticipants (разрешите пользователям приглашать анонимных пользователей к собраниям (разрядное расположение 6)</span><span class="sxs-lookup"><span data-stu-id="52fc9-337">64: AllowOrganizeMeetingWithAnonymousParticipants (allow users to invite anonymous users to meetings (bit position 6)</span></span></p></li>
<li><p><span data-ttu-id="52fc9-338">128: UCEnabled (включение пользователей для единой системы обмена сообщениями) (разрядность 7)</span><span class="sxs-lookup"><span data-stu-id="52fc9-338">128: UCEnabled (enable users for unified communications) (bit position 7)</span></span></p></li>
<li><p><span data-ttu-id="52fc9-339">256: EnabledForEnhancedPresence (включение пользователей для общедоступной службы обмена мгновенными сообщениями) (разрядное расположение 8)</span><span class="sxs-lookup"><span data-stu-id="52fc9-339">256: EnabledForEnhancedPresence (enable user for public IM connectivity) (bit position 8)</span></span></p></li>
<li><p><span data-ttu-id="52fc9-340">512: RemoteCallControlDualMode (разрядность 9)</span><span class="sxs-lookup"><span data-stu-id="52fc9-340">512: RemoteCallControlDualMode (bit position 9)</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="52fc9-341">Новые возможности Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="52fc9-341">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="52fc9-342">Устаревшие в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="52fc9-342">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-343">msRTCSIP-EnterpriseServices</span><span class="sxs-lookup"><span data-stu-id="52fc9-343">msRTCSIP-EnterpriseServices</span></span></p></td>
<td><p><span data-ttu-id="52fc9-344">Этот атрибут указывает, загружены ли корпоративные службы на данном сервере.</span><span class="sxs-lookup"><span data-stu-id="52fc9-344">This attribute indicates whether the Enterprise Services are loaded on the given server.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-345">msRTCSIP-ExtensionData</span><span class="sxs-lookup"><span data-stu-id="52fc9-345">msRTCSIP-ExtensionData</span></span></p></td>
<td><p><span data-ttu-id="52fc9-346">Этот атрибут зарезервирован для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="52fc9-346">This attribute is reserved for future use.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-347">msRTCSIP-ExternalAccessCode</span><span class="sxs-lookup"><span data-stu-id="52fc9-347">msRTCSIP-ExternalAccessCode</span></span></p></td>
<td><p><span data-ttu-id="52fc9-348">Этот атрибут включает код набора номера для внешнего доступа.</span><span class="sxs-lookup"><span data-stu-id="52fc9-348">This attribute contains the dial code for external access.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-349">Новые возможности Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="52fc9-349">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-350">msRTCSIP-FederationEnabled</span><span class="sxs-lookup"><span data-stu-id="52fc9-350">msRTCSIP-FederationEnabled</span></span></p></td>
<td><p><span data-ttu-id="52fc9-351">Этот атрибут определяет, включена ли Федерация для одного пользователя.</span><span class="sxs-lookup"><span data-stu-id="52fc9-351">This attribute controls whether a single user is enabled for federation.</span></span> <span data-ttu-id="52fc9-352">Она принудительно применена уровнем корпоративных служб.</span><span class="sxs-lookup"><span data-stu-id="52fc9-352">It is enforced by the Enterprise Services layer.</span></span> <span data-ttu-id="52fc9-353">Оно помечено для репликации глобального каталога.</span><span class="sxs-lookup"><span data-stu-id="52fc9-353">It is marked for global catalog replication.</span></span></p>
<p><span data-ttu-id="52fc9-354">Допустимые значения: <strong>true</strong> или <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="52fc9-354">The valid values are <strong>TRUE</strong> or <strong>FALSE</strong>.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-355">Новые возможности Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="52fc9-355">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-356">msRTCSIP-FrontEndServers</span><span class="sxs-lookup"><span data-stu-id="52fc9-356">msRTCSIP-FrontEndServers</span></span></p></td>
<td><p><span data-ttu-id="52fc9-357">Этот атрибут — Многозначный список доменных имен всех серверов Enterprise Edition, связанных с пулом.</span><span class="sxs-lookup"><span data-stu-id="52fc9-357">This attribute is a multi-valued list of the domain names of all Enterprise Edition servers associated with a pool.</span></span></p>
<p><span data-ttu-id="52fc9-358">Обратная ссылка: <strong>идентификатор ссылки 11023</strong></span><span class="sxs-lookup"><span data-stu-id="52fc9-358">Back link: <strong>Link ID 11023</strong></span></span></p>
<p><span data-ttu-id="52fc9-359">Соответствующая ссылка "вперед" на эту ссылку <strong>msRTCSIP-PoolAddress</strong>.</span><span class="sxs-lookup"><span data-stu-id="52fc9-359">The corresponding forward link to this back link is <strong>msRTCSIP-PoolAddress</strong>.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-360">Новые возможности Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="52fc9-360">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-361">msRTCSIP — Gateways (устарело)</span><span class="sxs-lookup"><span data-stu-id="52fc9-361">msRTCSIP-Gateways (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="52fc9-362">Этот многозначный атрибут строки включает список шлюзов и портов (для шлюза).</span><span class="sxs-lookup"><span data-stu-id="52fc9-362">This multi-valued string attribute contains a list of gateways and ports (per gateway).</span></span></p></td>
<td><p><span data-ttu-id="52fc9-363">Устаревшие в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="52fc9-363">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-364">msRTCSIP-GlobalSettingsData (устарело)</span><span class="sxs-lookup"><span data-stu-id="52fc9-364">msRTCSIP-GlobalSettingsData (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="52fc9-365">Этот атрибут хранит пары имя: значение.</span><span class="sxs-lookup"><span data-stu-id="52fc9-365">This attribute stores name:value pairs.</span></span> <span data-ttu-id="52fc9-366">В параметре " <strong>Разрешить опрос для проверки присутствия</strong> " указана уже определенная пара имя: значение.</span><span class="sxs-lookup"><span data-stu-id="52fc9-366">The already-defined name:value pair is for the <strong>allow polling for presence</strong> setting.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-367">Устаревшие в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="52fc9-367">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-368">msRTCSIP-GroupingID</span><span class="sxs-lookup"><span data-stu-id="52fc9-368">msRTCSIP-GroupingID</span></span></p></td>
<td><p><span data-ttu-id="52fc9-369">Этот атрибут является уникальным идентификатором группы, которая используется для группировки записей в адресной книге.</span><span class="sxs-lookup"><span data-stu-id="52fc9-369">This attribute is a unique identifier of a group that is used to group address book entries.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-370">Новые возможности Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="52fc9-370">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-371">msRTCSIP-HomeServer (устарело)</span><span class="sxs-lookup"><span data-stu-id="52fc9-371">msRTCSIP-HomeServer (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="52fc9-372">Новые возможности Live Communications Server 2003 (не используется).</span><span class="sxs-lookup"><span data-stu-id="52fc9-372">New in Live Communications Server 2003 (not used).</span></span></p>
<p><span data-ttu-id="52fc9-373">Устаревшие возможности для сервера Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="52fc9-373">Obsolete in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-374">msRTCSIP-HomeServerString (устарело)</span><span class="sxs-lookup"><span data-stu-id="52fc9-374">msRTCSIP-HomeServerString (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="52fc9-375">Новые возможности Live Communications Server 2003.</span><span class="sxs-lookup"><span data-stu-id="52fc9-375">New in Live Communications Server 2003.</span></span></p>
<p><span data-ttu-id="52fc9-376">Устаревшие возможности для сервера Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="52fc9-376">Obsolete in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-377">msRTCSIP-HomeUsers (устарело)</span><span class="sxs-lookup"><span data-stu-id="52fc9-377">msRTCSIP-HomeUsers (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="52fc9-378">Новые возможности Live Communications Server 2003 (не используется).</span><span class="sxs-lookup"><span data-stu-id="52fc9-378">New in Live Communications Server 2003 (not used).</span></span></p>
<p><span data-ttu-id="52fc9-379">Устаревшие возможности для сервера Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="52fc9-379">Obsolete in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-380">msRTCSIP-InternetAccessEnabled</span><span class="sxs-lookup"><span data-stu-id="52fc9-380">msRTCSIP-InternetAccessEnabled</span></span></p></td>
<td><p><span data-ttu-id="52fc9-381">Этот атрибут определяет, разрешено ли для одного пользователя доступ за пределы внешних пользователей.</span><span class="sxs-lookup"><span data-stu-id="52fc9-381">This attribute controls whether a single user is enabled for outside user access.</span></span> <span data-ttu-id="52fc9-382">Она принудительно применена уровнем корпоративных служб.</span><span class="sxs-lookup"><span data-stu-id="52fc9-382">It is enforced by the Enterprise Services layer.</span></span> <span data-ttu-id="52fc9-383">Оно помечено для репликации глобального каталога.</span><span class="sxs-lookup"><span data-stu-id="52fc9-383">It is marked for global catalog replication.</span></span></p>
<p><span data-ttu-id="52fc9-384">Допустимые значения: <strong>true</strong> или <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="52fc9-384">The valid values are <strong>TRUE</strong> or <strong>FALSE</strong>.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-385">Новые возможности Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="52fc9-385">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-386">msRTCSIP-Master (устарело)</span><span class="sxs-lookup"><span data-stu-id="52fc9-386">msRTCSIP-IsMaster (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="52fc9-387">Новые возможности Live Communications Server 2003</span><span class="sxs-lookup"><span data-stu-id="52fc9-387">New in Live Communications Server 2003</span></span></p>
<p><span data-ttu-id="52fc9-388">Устаревшие возможности для сервера Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="52fc9-388">Obsolete in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-389">msRTCSIP (линия)</span><span class="sxs-lookup"><span data-stu-id="52fc9-389">msRTCSIP-Line</span></span></p></td>
<td><p><span data-ttu-id="52fc9-390">Этот атрибут с одним значением включает идентификатор устройства (URI SIP или URI TEL телефона, который используются в Lync для телефонной связи).</span><span class="sxs-lookup"><span data-stu-id="52fc9-390">This single-valued attribute contains the device ID (either the SIP URI or the TEL URI of the phone the user controls) used by Lync for telephony.</span></span> <span data-ttu-id="52fc9-391">Этот атрибут помечен для репликации глобального каталога и является индексированным.</span><span class="sxs-lookup"><span data-stu-id="52fc9-391">This attribute is marked for Global Catalog replication and is indexed.</span></span> <span data-ttu-id="52fc9-392">Если для пользователя разрешена Корпоративная голосовая связь, этот атрибут сохраняет нормализованную версию E. 164 для номера телефона пользователя.</span><span class="sxs-lookup"><span data-stu-id="52fc9-392">If a user is enabled for Enterprise Voice, this attribute stores the E.164 normalized version of the user’s phone number.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-393">Новые возможности Microsoft Office Live Communications Server 2005 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="52fc9-393">New in Microsoft Office Live Communications Server 2005 with SP1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-394">msRTCSIP-LineServer</span><span class="sxs-lookup"><span data-stu-id="52fc9-394">msRTCSIP-LineServer</span></span></p></td>
<td><p><span data-ttu-id="52fc9-395">Этот атрибут с одним значением включает URI SIP сервера шлюза CSTA-SIP.</span><span class="sxs-lookup"><span data-stu-id="52fc9-395">This single-valued attribute contains the SIP URI of the CSTA-SIP gateway server.</span></span> <span data-ttu-id="52fc9-396">Этот атрибут помечен для репликации глобального каталога, но не индексирован.</span><span class="sxs-lookup"><span data-stu-id="52fc9-396">This attribute is marked for Global Catalog replication but is not indexed.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-397">Новые возможности Microsoft Office Live Communications Server 2005 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="52fc9-397">New in Microsoft Office Live Communications Server 2005 with SP1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-398">msRTCSIP-LocalNormalizationData (устарело)</span><span class="sxs-lookup"><span data-stu-id="52fc9-398">msRTCSIP-LocalNormalizationData (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="52fc9-399">Этот атрибут зарезервирован для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="52fc9-399">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-400">Новые возможности Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="52fc9-400">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="52fc9-401">Устаревшие в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="52fc9-401">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-402">msRTCSIP-LocalNormalizationLinks (устарело)</span><span class="sxs-lookup"><span data-stu-id="52fc9-402">msRTCSIP-LocalNormalizationLinks (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="52fc9-403">Этот многозначный атрибут включает список локальных имен, различающих нормализацию (DN), связанных с этим профилем расположения.</span><span class="sxs-lookup"><span data-stu-id="52fc9-403">This multi-valued attribute contains a list of local normalization distinguished names (DN) associated with this location profile.</span></span> <span data-ttu-id="52fc9-404">Тип этого атрибута — двоичный DN.</span><span class="sxs-lookup"><span data-stu-id="52fc9-404">The type of this attribute is a DN binary.</span></span> <span data-ttu-id="52fc9-405">Существует связь "один ко многим" между профилем места и локальными правилами нормализации.</span><span class="sxs-lookup"><span data-stu-id="52fc9-405">There is a one-to-many relationship between location profile and local normalization rules.</span></span> <span data-ttu-id="52fc9-406">Упорядочение списка локальных DNs-имен для нормализации должно поддерживаться в соответствии с порядком, указанным администратором.</span><span class="sxs-lookup"><span data-stu-id="52fc9-406">The ordering of the list of local normalization DNs must be maintained in the order specified by the administrator.</span></span> <span data-ttu-id="52fc9-407">Сохранение порядка поддерживается двоичной частью РАЗЛИЧАЮЩЕГОСЯ двоичного кода, указывающей индекс порядка.</span><span class="sxs-lookup"><span data-stu-id="52fc9-407">The preservation of order is maintained by the binary portion of the DN binary, which specifies the order index.</span></span></p>
<p><span data-ttu-id="52fc9-408">Ссылка "вперед": <strong>ИД ссылки 11034</strong></span><span class="sxs-lookup"><span data-stu-id="52fc9-408">Forward link: <strong>Link ID 11034</strong></span></span></p>
<p><span data-ttu-id="52fc9-409">Для обратной ссылки на этот атрибут прямой ссылки будет задано значение <strong>msRTCSIP-LocationProfileBL</strong>.</span><span class="sxs-lookup"><span data-stu-id="52fc9-409">The corresponding back link to this forward link attribute is <strong>msRTCSIP-LocationProfileBL</strong>.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-410">Новые возможности Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="52fc9-410">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="52fc9-411">Устаревшие в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="52fc9-411">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-412">msRTCSIP-LocalNormalizationOptions</span><span class="sxs-lookup"><span data-stu-id="52fc9-412">msRTCSIP-LocalNormalizationOptions</span></span></p></td>
<td><p><span data-ttu-id="52fc9-413">Этот атрибут включает список параметров для правила нормализации.</span><span class="sxs-lookup"><span data-stu-id="52fc9-413">This attribute contains a list of options for the normalization rule.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-414">Новые возможности Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="52fc9-414">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-415">msRTCSIP-LocationName (устарело)</span><span class="sxs-lookup"><span data-stu-id="52fc9-415">msRTCSIP-LocationName (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="52fc9-416">Этот атрибут с одним значением содержит понятное имя для профиля расположения, показывающее, какое расположение представляет этот профиль.</span><span class="sxs-lookup"><span data-stu-id="52fc9-416">This single-valued attribute contains a friendly name for the location profile that indicates which location this profile represents.</span></span> <span data-ttu-id="52fc9-417">Так как может быть несколько профилей местоположения, администратору нужно способ отличать различные профили.</span><span class="sxs-lookup"><span data-stu-id="52fc9-417">Because there can be multiple location profiles, the administrator needs a way to distinguish between different profiles.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-418">Новые возможности Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="52fc9-418">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="52fc9-419">Устаревшие в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="52fc9-419">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-420">msRTCSIP-locationProfileBL (устарело)</span><span class="sxs-lookup"><span data-stu-id="52fc9-420">msRTCSIP-locationProfileBL (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="52fc9-421">Этот атрибут с несколькими значениями включает список различающихся имен для профиля расположения.</span><span class="sxs-lookup"><span data-stu-id="52fc9-421">This multi-valued attribute contains a list of location profile distinguished names.</span></span> <span data-ttu-id="52fc9-422">Этот атрибут определяет обратную ссылку на один или несколько профилей местоположений.</span><span class="sxs-lookup"><span data-stu-id="52fc9-422">This attribute specifies the back link to one or more location profiles.</span></span></p>
<p><span data-ttu-id="52fc9-423">Обратная ссылка: <strong>идентификатор ссылки 11035</strong></span><span class="sxs-lookup"><span data-stu-id="52fc9-423">Back link: <strong>Link ID 11035</strong></span></span></p>
<p><span data-ttu-id="52fc9-424">Этот атрибут соответствует ссылке "вперед" <strong>msRTCSIP-LocalNormalizationLinks</strong>.</span><span class="sxs-lookup"><span data-stu-id="52fc9-424">This attribute corresponds to the forward link <strong>msRTCSIP-LocalNormalizationLinks</strong>.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-425">Новые возможности Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="52fc9-425">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="52fc9-426">Устаревшие в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="52fc9-426">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-427">msRTCSIP-LocationProfileData (устарело)</span><span class="sxs-lookup"><span data-stu-id="52fc9-427">msRTCSIP-LocationProfileData (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="52fc9-428">Этот атрибут зарезервирован для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="52fc9-428">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-429">Новые возможности Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="52fc9-429">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="52fc9-430">Устаревшие в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="52fc9-430">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-431">msRTCSIP-LocationProfileOptions</span><span class="sxs-lookup"><span data-stu-id="52fc9-431">msRTCSIP-LocationProfileOptions</span></span></p></td>
<td><p><span data-ttu-id="52fc9-432">Этот атрибут включает параметры для профиля расположения.</span><span class="sxs-lookup"><span data-stu-id="52fc9-432">This attribute contains the options for the location profile.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-433">Новые возможности Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="52fc9-433">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-434">msRTCSIP-MappingContact</span><span class="sxs-lookup"><span data-stu-id="52fc9-434">msRTCSIP-MappingContact</span></span></p></td>
<td><p><span data-ttu-id="52fc9-435">Этот атрибут с несколькими значениями содержит список контактов приложения.</span><span class="sxs-lookup"><span data-stu-id="52fc9-435">This multiple-value attribute holds a list of application contacts.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-436">Новые возможности Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="52fc9-436">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-437">msRTCSIP-MappingLocation</span><span class="sxs-lookup"><span data-stu-id="52fc9-437">msRTCSIP-MappingLocation</span></span></p></td>
<td><p><span data-ttu-id="52fc9-438">Этот атрибут с несколькими значениями содержит список профилей местоположения.</span><span class="sxs-lookup"><span data-stu-id="52fc9-438">This multiple-value attribute holds a list of location profiles.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-439">Новые возможности Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="52fc9-439">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-440">msRTCSIP-MaxNumOutstandingSearchPerServer (устарело)</span><span class="sxs-lookup"><span data-stu-id="52fc9-440">msRTCSIP-MaxNumOutstandingSearchPerServer (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="52fc9-441">Этот атрибут представляет максимальное количество ожидающих запросов на поиск на одном сервере.</span><span class="sxs-lookup"><span data-stu-id="52fc9-441">This attribute represents the maximum number of outstanding search requests per server.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-442">Устаревшие в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="52fc9-442">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-443">msRTCSIP-MaxNumSubscriptionsPerUser (устарело)</span><span class="sxs-lookup"><span data-stu-id="52fc9-443">msRTCSIP-MaxNumSubscriptionsPerUser (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="52fc9-444">Атрибут представляет максимальное число подписок на одного пользователя.</span><span class="sxs-lookup"><span data-stu-id="52fc9-444">The attribute represents the maximum number of subscriptions per user.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-445">Устаревшие в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="52fc9-445">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-446">msRTCSIP-MaxPresenceSubscriptionTimeout (устарело)</span><span class="sxs-lookup"><span data-stu-id="52fc9-446">msRTCSIP-MaxPresenceSubscriptionTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="52fc9-447">Этот атрибут представляет окно максимального времени ожидания подписки.</span><span class="sxs-lookup"><span data-stu-id="52fc9-447">This attribute represents the maximum subscription time-out window.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-448">Устаревшие в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="52fc9-448">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-449">msRTCSIP-MaxRegistrationsTimeout (устарело)</span><span class="sxs-lookup"><span data-stu-id="52fc9-449">msRTCSIP-MaxRegistrationsTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="52fc9-450">Этот атрибут представляет окно "максимальное время ожидания регистрации".</span><span class="sxs-lookup"><span data-stu-id="52fc9-450">This attribute represents the maximum registrations time-out window.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-451">Устаревшие в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="52fc9-451">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-452">msRTCSIP-MaxRoamingDataSubscriptionTimeout (устарело)</span><span class="sxs-lookup"><span data-stu-id="52fc9-452">msRTCSIP-MaxRoamingDataSubscriptionTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="52fc9-453">Этот атрибут представляет максимальное время ожидания подписки на подписку данных в роуминге.</span><span class="sxs-lookup"><span data-stu-id="52fc9-453">This attribute represents the maximum roaming data subscriptions time-out window.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-454">Устаревшие в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="52fc9-454">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-455">msRTCSIP-MCUData</span><span class="sxs-lookup"><span data-stu-id="52fc9-455">msRTCSIP-MCUData</span></span></p></td>
<td><p><span data-ttu-id="52fc9-456">Этот атрибут зарезервирован для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="52fc9-456">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-457">Новые возможности Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="52fc9-457">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-458">msRTCSIP-MCUFactoryAddress</span><span class="sxs-lookup"><span data-stu-id="52fc9-458">msRTCSIP-MCUFactoryAddress</span></span></p></td>
<td><p><span data-ttu-id="52fc9-459">Этот атрибут является атрибутом точки управления службой в классе компьютера, который указывает ссылку на фабрику элементов управления MultiPoint (MCU), к которой она относится.</span><span class="sxs-lookup"><span data-stu-id="52fc9-459">This attribute is a service control point attribute under the computer class that specifies a link back to the multipoint control unit (MCU) Factory to which it belongs.</span></span> <span data-ttu-id="52fc9-460">Эта точка управления службой и атрибут создаются для каждого приложения Microsoft MCU.</span><span class="sxs-lookup"><span data-stu-id="52fc9-460">This service control point and attribute is created for every Microsoft MCU.</span></span> <span data-ttu-id="52fc9-461">Каждый из Microsoft MCU должен найти сервер пула, к которому он принадлежит, чтобы получить из него параметры уровня пула.</span><span class="sxs-lookup"><span data-stu-id="52fc9-461">Each Microsoft MCU must find the Back End Server of the pool to which it belongs, in order to retrieve pool-level settings from it.</span></span></p>
<p><span data-ttu-id="52fc9-462">Значение этого атрибута — различающееся имя (DN) фабрики MCU.</span><span class="sxs-lookup"><span data-stu-id="52fc9-462">The value of this attribute is the distinguished name (DN) of the MCU Factory.</span></span> <span data-ttu-id="52fc9-463">Это атрибут с одним значением и помеченный для репликации глобального каталога.</span><span class="sxs-lookup"><span data-stu-id="52fc9-463">This is a single-valued attribute and marked for global catalog replication.</span></span></p>
<p><span data-ttu-id="52fc9-464">Ссылка "вперед": <strong>ИД ссылки 11026</strong></span><span class="sxs-lookup"><span data-stu-id="52fc9-464">Forward link: <strong>Link ID 11026</strong></span></span></p>
<p><span data-ttu-id="52fc9-465">Для обратной ссылки на этот атрибут прямой ссылки будет задано значение <strong>msRTCSIP-MCUServers</strong>.</span><span class="sxs-lookup"><span data-stu-id="52fc9-465">The corresponding back link to this forward link attribute is <strong>msRTCSIP-MCUServers</strong>.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-466">Новые возможности Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="52fc9-466">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-467">msRTCSIP-MCUFactoryData</span><span class="sxs-lookup"><span data-stu-id="52fc9-467">msRTCSIP-MCUFactoryData</span></span></p></td>
<td><p><span data-ttu-id="52fc9-468">Это многострочный атрибут, зарезервированный.</span><span class="sxs-lookup"><span data-stu-id="52fc9-468">This is a multi-string reserved attribute.</span></span> <span data-ttu-id="52fc9-469">Параметры, хранящиеся в этом атрибуте, представлены в виде пар "имя = значение".</span><span class="sxs-lookup"><span data-stu-id="52fc9-469">Settings stored in this attribute are represented as name=value pairs.</span></span> <span data-ttu-id="52fc9-470">В настоящее время определены следующие пары name = value:</span><span class="sxs-lookup"><span data-stu-id="52fc9-470">Currently defined name=value pairs are:</span></span></p>
<ul>
<li><p><span data-ttu-id="52fc9-471">FactoryURL = &lt; URL-адрес&gt;</span><span class="sxs-lookup"><span data-stu-id="52fc9-471">FactoryURL = &lt;URL&gt;</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="52fc9-472">Новые возможности Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="52fc9-472">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-473">msRTCSIP-MCUFactoryPath</span><span class="sxs-lookup"><span data-stu-id="52fc9-473">msRTCSIP-MCUFactoryPath</span></span></p></td>
<td><p><span data-ttu-id="52fc9-474">Это однозначный атрибут, который содержит различающееся имя (DN) одной фабрики MCU, связанной с пулом.</span><span class="sxs-lookup"><span data-stu-id="52fc9-474">This is a single-valued attribute that contains the distinguished name (DN) of a single MCU factory associated with a pool.</span></span></p>
<p><span data-ttu-id="52fc9-475">Ссылка "вперед": <strong>ИД ссылки 11024</strong></span><span class="sxs-lookup"><span data-stu-id="52fc9-475">Forward link: <strong>Link ID 11024</strong></span></span></p>
<p><span data-ttu-id="52fc9-476">Для обратной ссылки на этот атрибут прямой ссылки будет задано значение <strong>msRTCSIP-PoolAddresses</strong>.</span><span class="sxs-lookup"><span data-stu-id="52fc9-476">The corresponding back link to this forward link attribute is <strong>msRTCSIP-PoolAddresses</strong>.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-477">Новые возможности Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="52fc9-477">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-478">msRTCSIP-MCUFactoryProviderID</span><span class="sxs-lookup"><span data-stu-id="52fc9-478">msRTCSIP-MCUFactoryProviderID</span></span></p></td>
<td><p><span data-ttu-id="52fc9-479">Этот атрибут является однозначной строкой, которая определяет GUID поставщика фабрики MCU.</span><span class="sxs-lookup"><span data-stu-id="52fc9-479">This attribute is a single-valued string that specifies the GUID of the MCU factory provider.</span></span> <span data-ttu-id="52fc9-480">На основе значения GUID процесс фабрики MCU определяет, нужно ли обслуживать этот тип MCU.</span><span class="sxs-lookup"><span data-stu-id="52fc9-480">Based on the GUID value, the MCU factory process determines whether to service this MCU type.</span></span> <span data-ttu-id="52fc9-481">Если значение GUID — <strong>{F0810510-424F-46ef-84FE-6CC720DF1791}</strong>, процесс фабрики MCU (доступен по умолчанию в Lync Server) будет обрабатываться.</span><span class="sxs-lookup"><span data-stu-id="52fc9-481">If the GUID value is <strong>{F0810510-424F-46ef-84FE-6CC720DF1791}</strong>, then the MCU factory process (available by default in Lync Server) will process it.</span></span> <span data-ttu-id="52fc9-482">Для любого другого значения GUID процесс фабрики MCU не будет обслуживать тип MCU.</span><span class="sxs-lookup"><span data-stu-id="52fc9-482">For any other GUID value, the MCU factory process will not service the MCU type.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-483">Новые возможности Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="52fc9-483">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-484">msRTCSIP-MCUServers</span><span class="sxs-lookup"><span data-stu-id="52fc9-484">msRTCSIP-MCUServers</span></span></p></td>
<td><p><span data-ttu-id="52fc9-485">Этот атрибут представляет собой список различающихся имен (DN) с несколькими значениями.</span><span class="sxs-lookup"><span data-stu-id="52fc9-485">This attribute is a multi-valued list of distinguished names (DN).</span></span> <span data-ttu-id="52fc9-486">Этот атрибут представляет список всех серверов MCU одного и того же типа и поставщика, связанных с этой фабрикой MCU.</span><span class="sxs-lookup"><span data-stu-id="52fc9-486">This attribute contains a list of all MCU servers of the same type and vendor associated with this MCU factory.</span></span> <span data-ttu-id="52fc9-487">Допустимые значения для каждого сегмента — 63 символов; допустимое значение полного доменного имени — 255 символов.</span><span class="sxs-lookup"><span data-stu-id="52fc9-487">The valid value for each segment is 63 characters; the valid value for the entire FQDN is 255 characters.</span></span></p>
<p><span data-ttu-id="52fc9-488">Обратная ссылка: идентификатор ссылки 11027</span><span class="sxs-lookup"><span data-stu-id="52fc9-488">Back link: Link ID 11027</span></span></p>
<p><span data-ttu-id="52fc9-489">Соответствующая ссылка "вперед" на эту ссылку <strong>msRTCSIP-MCUFactoryAddress</strong>.</span><span class="sxs-lookup"><span data-stu-id="52fc9-489">The corresponding forward link to this back link is <strong>msRTCSIP-MCUFactoryAddress</strong>.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-490">Новые возможности Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="52fc9-490">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-491">msRTCSIP-MCUType</span><span class="sxs-lookup"><span data-stu-id="52fc9-491">msRTCSIP-MCUType</span></span></p></td>
<td><p><span data-ttu-id="52fc9-492">Этот атрибут является однозначной строкой, указывающей на то, что MCU может обрабатываться.</span><span class="sxs-lookup"><span data-stu-id="52fc9-492">This attribute is a single-valued string that specifies the medium the MCU can handle.</span></span></p>
<p><span data-ttu-id="52fc9-493">Поддерживаются следующие допустимые типы:</span><span class="sxs-lookup"><span data-stu-id="52fc9-493">Supported valid types are:</span></span></p>
<ul>
<li><p><span data-ttu-id="52fc9-494">зала</span><span class="sxs-lookup"><span data-stu-id="52fc9-494">meeting</span></span></p></li>
<li><p><span data-ttu-id="52fc9-495">аудио-видео</span><span class="sxs-lookup"><span data-stu-id="52fc9-495">audio-video</span></span></p></li>
<li><p><span data-ttu-id="52fc9-496">сеанс</span><span class="sxs-lookup"><span data-stu-id="52fc9-496">chat</span></span></p></li>
<li><p><span data-ttu-id="52fc9-497">Phone-CONF</span><span class="sxs-lookup"><span data-stu-id="52fc9-497">phone-conf</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="52fc9-498">Новые возможности Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="52fc9-498">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-499">msRTCSIP-MCUVendor</span><span class="sxs-lookup"><span data-stu-id="52fc9-499">msRTCSIP-MCUVendor</span></span></p></td>
<td><p><span data-ttu-id="52fc9-500">Этот атрибут является однозначной строкой, указывающей имя поставщика MCU.</span><span class="sxs-lookup"><span data-stu-id="52fc9-500">This attribute is a single-valued string that specifies an MCU vendor’s name.</span></span> <span data-ttu-id="52fc9-501">В Microsoft MCUs этот атрибут будет указан в <strong>Microsoft Corporation</strong>.</span><span class="sxs-lookup"><span data-stu-id="52fc9-501">All Microsoft MCUs will specify this attribute to be <strong>Microsoft Corporation</strong>.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-502">Новые возможности Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="52fc9-502">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-503">msRTCSIP-MeetingFlags (устарело)</span><span class="sxs-lookup"><span data-stu-id="52fc9-503">msRTCSIP-MeetingFlags (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="52fc9-504">Этот атрибут определяет различные параметры собрания, которые включаются глобально для всех пользователей или объектов контактов.</span><span class="sxs-lookup"><span data-stu-id="52fc9-504">This attribute defines different meeting options that are enabled globally for all users or contact objects.</span></span> <span data-ttu-id="52fc9-505">Этот атрибут является значением битовой маски целочисленного типа.</span><span class="sxs-lookup"><span data-stu-id="52fc9-505">This attribute is a bit-mask value of integer type.</span></span></p>
<p><span data-ttu-id="52fc9-506">Допустимые значения (и связанные с ними битовые положения) приведены ниже.</span><span class="sxs-lookup"><span data-stu-id="52fc9-506">The valid values (and associated bit positions) are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="52fc9-507">0: AllowOrganizeMeetingWithAnonymousParticipants имеет значение None (не разрешать пользователям приглашать анонимных пользователей для собраний) (никакие биты не установлены).</span><span class="sxs-lookup"><span data-stu-id="52fc9-507">0: AllowOrganizeMeetingWithAnonymousParticipants is None (do not allow users to invite anonymous users to meetings) (no bits set)</span></span></p></li>
<li><p><span data-ttu-id="52fc9-508">4: AllowOrganizeMeetingWithAnonymousParticipants — все пользователи (разрешающие собрания анонимных пользователей) (разрядное расположение 2)</span><span class="sxs-lookup"><span data-stu-id="52fc9-508">4: AllowOrganizeMeetingWithAnonymousParticipants is Everyone (allow all users to invite anonymous users to meetings) (bit position 2)</span></span></p></li>
<li><p><span data-ttu-id="52fc9-509">8: AllowOrganizeMeetingWithAnonymousParticipants — UsePerUserSetting (разрешите пользователям приглашать анонимных пользователей для собраний на основе параметров пользователя) (разрядное положение 3).</span><span class="sxs-lookup"><span data-stu-id="52fc9-509">8: AllowOrganizeMeetingWithAnonymousParticipants is UsePerUserSetting (allow users to invite anonymous users to meetings based on per user setting) (bit position 3)</span></span></p></li>
<li><p><span data-ttu-id="52fc9-510">16: UserPerUserMeetingPolicy (определена политика собраний для пользователей) (битовая разряда 4)</span><span class="sxs-lookup"><span data-stu-id="52fc9-510">16: UserPerUserMeetingPolicy (meeting policy is defined per user) (bit position 4)</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="52fc9-511">Новые возможности Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="52fc9-511">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="52fc9-512">Устаревшие в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="52fc9-512">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-513">msRTCSIP-MeetingPolicy (устарело)</span><span class="sxs-lookup"><span data-stu-id="52fc9-513">msRTCSIP-MeetingPolicy (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="52fc9-514">Этот атрибут указывает различающееся имя (DN) политики, назначенной администратором для этого пользователя в качестве атрибута с одним значением.</span><span class="sxs-lookup"><span data-stu-id="52fc9-514">This attribute specifies the distinguished name (DN) of the policy the administrator has assigned for this user as a single-valued attribute.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-515">Новые возможности Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="52fc9-515">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="52fc9-516">Устаревшие в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="52fc9-516">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-517">msRTCSIP-MinPresenceSubscriptionTimeout (устарело)</span><span class="sxs-lookup"><span data-stu-id="52fc9-517">msRTCSIP-MinPresenceSubscriptionTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="52fc9-518">Этот атрибут представляет окно минимального времени ожидания подписки на присутствие.</span><span class="sxs-lookup"><span data-stu-id="52fc9-518">This attribute represents the minimum presence subscription time-out window.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-519">Устаревшие в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="52fc9-519">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-520">msRTCSIP-MinRegistrationTimeout (устарело)</span><span class="sxs-lookup"><span data-stu-id="52fc9-520">msRTCSIP-MinRegistrationTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="52fc9-521">Этот атрибут представляет окно минимального времени ожидания регистрации.</span><span class="sxs-lookup"><span data-stu-id="52fc9-521">This attribute represents the minimum registration time-out window.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-522">Новые возможности Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="52fc9-522">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="52fc9-523">Устаревшие в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="52fc9-523">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-524">msRTCSIP-MinRoamingDataSubscriptionTimeout (устарело)</span><span class="sxs-lookup"><span data-stu-id="52fc9-524">msRTCSIP-MinRoamingDataSubscriptionTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="52fc9-525">Этот атрибут представляет временное время ожидания подписки на подписку данных в роуминге.</span><span class="sxs-lookup"><span data-stu-id="52fc9-525">This attribute represents the minimum roaming data subscription time-out window.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-526">Новые возможности Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="52fc9-526">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="52fc9-527">Устаревшие в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="52fc9-527">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-528">msRTCSIP-MirrorBackEndServer</span><span class="sxs-lookup"><span data-stu-id="52fc9-528">msRTCSIP-MirrorBackEndServer</span></span></p></td>
<td><p><span data-ttu-id="52fc9-529">Этот атрибут используется для хранения зеркальной серверной части SQL Server, используемой в пуле переднего плана.</span><span class="sxs-lookup"><span data-stu-id="52fc9-529">This attribute is used to store the mirrored SQL Server backend used by the Front End pool.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-530">Новые возможности Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="52fc9-530">New in Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-531">msRTCSIP-MobilityFlags</span><span class="sxs-lookup"><span data-stu-id="52fc9-531">msRTCSIP-MobilityFlags</span></span></p></td>
<td><p><span data-ttu-id="52fc9-532">Этот атрибут включает параметры и флаги, определяющие параметры мобильности.</span><span class="sxs-lookup"><span data-stu-id="52fc9-532">This attribute contains options and flags that define mobility settings.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-533">Новые возможности Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="52fc9-533">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-534">msRTCSIP-MobilityPolicy</span><span class="sxs-lookup"><span data-stu-id="52fc9-534">msRTCSIP-MobilityPolicy</span></span></p></td>
<td><p><span data-ttu-id="52fc9-535">Этот атрибут включает DN для объекта политики мобильности.</span><span class="sxs-lookup"><span data-stu-id="52fc9-535">This attribute contains the DN for a mobility policy object.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-536">Новые возможности Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="52fc9-536">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-537">msRTCSIP-NumDevicesPerUser (устарело)</span><span class="sxs-lookup"><span data-stu-id="52fc9-537">msRTCSIP-NumDevicesPerUser (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="52fc9-538">Этот атрибут представляет допустимое количество устройств, на которые пользователь может зарегистрироваться для связи с SIP, и оформить подписку на состояние присутствия.</span><span class="sxs-lookup"><span data-stu-id="52fc9-538">This attribute represents the allowed number of devices on which a user can register for SIP communications and subscribe to presence.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-539">Новые возможности Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="52fc9-539">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="52fc9-540">Устаревшие в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="52fc9-540">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-541">msRTCSIP-OptionFlags</span><span class="sxs-lookup"><span data-stu-id="52fc9-541">msRTCSIP-OptionFlags</span></span></p></td>
<td><p><span data-ttu-id="52fc9-542">Этот атрибут определяет параметры, доступные для объекта пользователя или контакта.</span><span class="sxs-lookup"><span data-stu-id="52fc9-542">This attribute specifies the options that are enabled for the user or contact object.</span></span> <span data-ttu-id="52fc9-543">Этот атрибут является значением битовой маски типа Integer.</span><span class="sxs-lookup"><span data-stu-id="52fc9-543">This attribute is a bit-mask value of type integer.</span></span> <span data-ttu-id="52fc9-544">Каждый параметр представлен битом.</span><span class="sxs-lookup"><span data-stu-id="52fc9-544">Each option is represented by a bit.</span></span> <span data-ttu-id="52fc9-545">Этот атрибут помечен для репликации глобального каталога.</span><span class="sxs-lookup"><span data-stu-id="52fc9-545">This attribute is marked for global catalog replication.</span></span></p>
<p><span data-ttu-id="52fc9-546">Допустимые значения (и связанные с ними битовые положения) приведены ниже.</span><span class="sxs-lookup"><span data-stu-id="52fc9-546">The valid values (and associated bit positions) are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="52fc9-547">1: включено для общедоступной службы обмена мгновенными сообщениями (с битовой позицией 0)</span><span class="sxs-lookup"><span data-stu-id="52fc9-547">1: Enabled for public instant messaging (IM) connectivity (bit position 0)</span></span></p></li>
<li><p><span data-ttu-id="52fc9-548">2: зарезервировано (разрядное расположение 1)</span><span class="sxs-lookup"><span data-stu-id="52fc9-548">2: Reserved (bit position 1)</span></span></p></li>
<li><p><span data-ttu-id="52fc9-549">4: зарезервировано (разрядное расположение 2)</span><span class="sxs-lookup"><span data-stu-id="52fc9-549">4: Reserved (bit position 2)</span></span></p></li>
<li><p><span data-ttu-id="52fc9-550">8: зарезервировано (разрядное расположение 3)</span><span class="sxs-lookup"><span data-stu-id="52fc9-550">8: Reserved (bit position 3)</span></span></p></li>
<li><p><span data-ttu-id="52fc9-551">16: удаленное управление звонками включено [телефония] (разрядность 4)</span><span class="sxs-lookup"><span data-stu-id="52fc9-551">16: Remote call control Enabled [Telephony] (bit position 4)</span></span></p></li>
<li><p><span data-ttu-id="52fc9-552">64: AllowOrganizeMeetingWithAnonymousParticipants (разрешите пользователям приглашать анонимных пользователей к собраниям (разрядное расположение 6)</span><span class="sxs-lookup"><span data-stu-id="52fc9-552">64: AllowOrganizeMeetingWithAnonymousParticipants (allow users to invite anonymous users to meetings (bit position 6)</span></span></p></li>
<li><p><span data-ttu-id="52fc9-553">128: UCEnabled (разрешение пользователей на UC) (разрядность 7)</span><span class="sxs-lookup"><span data-stu-id="52fc9-553">128: UCEnabled (enable users for UC) (bit position 7)</span></span></p></li>
<li><p><span data-ttu-id="52fc9-554">256: EnabledForEnhancedPresence (включение пользователей для общедоступной службы обмена мгновенными сообщениями) (разрядное расположение 8)</span><span class="sxs-lookup"><span data-stu-id="52fc9-554">256: EnabledForEnhancedPresence (enable user for public IM connectivity) (bit position 8)</span></span></p></li>
<li><p><span data-ttu-id="52fc9-555">512: RemoteCallControlDualMode (разрядность 9)</span><span class="sxs-lookup"><span data-stu-id="52fc9-555">512: RemoteCallControlDualMode (bit position 9)</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="52fc9-556">Новые возможности Live Communications Server 2005 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="52fc9-556">New in Live Communications Server 2005 with SP1.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-557">msRTCSIP-OriginatorSID</span><span class="sxs-lookup"><span data-stu-id="52fc9-557">msRTCSIP-OriginatorSID</span></span></p></td>
<td><p><span data-ttu-id="52fc9-558">Этот атрибут используется в топологиях ресурсов и центральных лесах для включения единого входа, если пользователь ObjectSID из учетной записи участника Windows NT Server копируется в этот атрибут соответствующего объекта пользователя или контакта в ресурсе или центральном лесе.</span><span class="sxs-lookup"><span data-stu-id="52fc9-558">This attribute is used in resource and central forest topologies to enable single sign-on when a user’s ObjectSID from the Windows NT Server principal account is copied into this attribute of the corresponding user or contact object in the resource or central forest.</span></span> <span data-ttu-id="52fc9-559">Служба Communicator Web Access осуществляет поиск пользователя в доменных СЛУЖБах Active Directory с помощью этого атрибута или ObjectSID пользователя.</span><span class="sxs-lookup"><span data-stu-id="52fc9-559">Communicator Web Access searches for a user in AD DS using this attribute or the user’s ObjectSID.</span></span> <span data-ttu-id="52fc9-560">Этот атрибут помечен для репликации глобального каталога.</span><span class="sxs-lookup"><span data-stu-id="52fc9-560">This attribute is marked for global catalog replication.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-561">msRTCSIP-OwnerUrn</span><span class="sxs-lookup"><span data-stu-id="52fc9-561">msRTCSIP-OwnerUrn</span></span></p></td>
<td><p><span data-ttu-id="52fc9-562">Этот атрибут представляет собой унифицированное имя ресурса (URN) владельца для контакта приложения.</span><span class="sxs-lookup"><span data-stu-id="52fc9-562">This attribute is the Uniform Resource Name (URN) of the owner for an application contact.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-563">Новые возможности Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="52fc9-563">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-564">Шаблон msRTCSIP (устаревший)</span><span class="sxs-lookup"><span data-stu-id="52fc9-564">msRTCSIP-Pattern (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="52fc9-565">Этот однозначный атрибут String включает шаблон, используемый для сопоставления номеров набора с форматом E. 164.</span><span class="sxs-lookup"><span data-stu-id="52fc9-565">This single-valued string attribute contains a pattern used for matching dial numbers into E.164 format.</span></span> <span data-ttu-id="52fc9-566">Если номер набора номера соответствует этому шаблону, для набора номера применяется перевод.</span><span class="sxs-lookup"><span data-stu-id="52fc9-566">If the dial number matches this pattern, the translation is applied to the dialed number.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-567">Новые возможности Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="52fc9-567">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="52fc9-568">Устаревшие в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="52fc9-568">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-569">msRTCSIP-PhoneRouteBL (устарело)</span><span class="sxs-lookup"><span data-stu-id="52fc9-569">msRTCSIP-PhoneRouteBL (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="52fc9-570">Этот атрибут с несколькими значениями имеет список различающихся имен для маршрутных маршрутов (DN).</span><span class="sxs-lookup"><span data-stu-id="52fc9-570">This multi-valued attribute contains a list of phone route distinguished names (DN).</span></span> <span data-ttu-id="52fc9-571">Этот атрибут определяет обратную ссылку на один или несколько телефонных маршрутов.</span><span class="sxs-lookup"><span data-stu-id="52fc9-571">This attribute specifies the back link to one or more phone routes.</span></span></p>
<p><span data-ttu-id="52fc9-572">Обратная ссылка: <strong>идентификатор ссылки 11033</strong></span><span class="sxs-lookup"><span data-stu-id="52fc9-572">Back link: <strong>Link ID 11033</strong></span></span></p>
<p><span data-ttu-id="52fc9-573">Этот атрибут соответствует ссылке "вперед" <strong>msRTCSIP-RouteUsageLinks</strong>.</span><span class="sxs-lookup"><span data-stu-id="52fc9-573">This attribute corresponds to the forward link <strong>msRTCSIP-RouteUsageLinks</strong>.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-574">Новые возможности Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="52fc9-574">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="52fc9-575">Устаревшие в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="52fc9-575">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-576">msRTCSIP-PhoneRouteData (устарело)</span><span class="sxs-lookup"><span data-stu-id="52fc9-576">msRTCSIP-PhoneRouteData (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="52fc9-577">Этот атрибут зарезервирован для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="52fc9-577">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-578">Устаревшие в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="52fc9-578">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-579">msRTCSIP-PhoneRouteName (устарело)</span><span class="sxs-lookup"><span data-stu-id="52fc9-579">msRTCSIP-PhoneRouteName (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="52fc9-580">Этот однозначный строковый атрибут Юникода определяет понятное имя маршрута, поэтому на него может легко ссылаться администратор.</span><span class="sxs-lookup"><span data-stu-id="52fc9-580">This single valued UNICODE string attribute specifies the friendly name of the phone route, so it can easily be referenced by the administrator.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-581">Устаревшие в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="52fc9-581">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-582">msRTCSIP-PhoneUsageData (устарело)</span><span class="sxs-lookup"><span data-stu-id="52fc9-582">msRTCSIP-PhoneUsageData (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="52fc9-583">Этот атрибут зарезервирован для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="52fc9-583">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-584">Новые возможности Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="52fc9-584">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="52fc9-585">Устаревшие в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="52fc9-585">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-586">msRTCSIP-PolicyContent (устарело)</span><span class="sxs-lookup"><span data-stu-id="52fc9-586">msRTCSIP-PolicyContent (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="52fc9-587">Этот атрибут является строкой Юникода с одним значением.</span><span class="sxs-lookup"><span data-stu-id="52fc9-587">This attribute is a single-valued Unicode string.</span></span> <span data-ttu-id="52fc9-588">Этот атрибут String включает определение политики в формате XML.</span><span class="sxs-lookup"><span data-stu-id="52fc9-588">This string attribute contains the policy definition in XML format.</span></span> <span data-ttu-id="52fc9-589">Определение схемы XML является общим для разных типов политик, но для каждого типа политики различаются только параметры.</span><span class="sxs-lookup"><span data-stu-id="52fc9-589">The XML schema definition is common across different policy types, only the settings are different for each policy type.</span></span></p>
<p><span data-ttu-id="52fc9-590">Определение схемы XML (XSD) определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="52fc9-590">The XML schema definition (XSD) is defined as follows:</span></span></p>
<pre><code>&lt;?xml version=&quot;1.0&quot; encoding=&quot;utf-8&quot;?&gt;
&lt;xs:schema id=&quot;instance&quot; xmlns=&quot;&quot; xmlns:xs=&quot;http://www.w3.org/2001/XMLSchema&quot; xmlns:msdata=&quot;urn:schemas-microsoft-com:xml-msdata&quot;&gt;
  &lt;xs:element name=&quot;instance&quot; msdata:IsDataSet=&quot;true&quot;&gt;
    &lt;xs:complexType&gt;
      &lt;xs:choice maxOccurs=&quot;unbounded&quot;&gt;
        &lt;xs:element name=&quot;property&quot; nillable=&quot;true&quot;&gt;
          &lt;xs:complexType&gt;
            &lt;xs:simpleContent msdata:ColumnName=&quot;property_Text&quot; msdata:Ordinal=&quot;1&quot;&gt;
              &lt;xs:extension base=&quot;xs:string&quot;&gt;
                &lt;xs:attribute name=&quot;name&quot; type=&quot;xs:string&quot; /&gt;
              &lt;/xs:extension&gt;
            &lt;/xs:simpleContent&gt;
          &lt;/xs:complexType&gt;
        &lt;/xs:element&gt;
      &lt;/xs:choice&gt;
    &lt;/xs:complexType&gt;
  &lt;/xs:element&gt;
&lt;/xs:schema&gt;</code></pre></td>
<td><p><span data-ttu-id="52fc9-591">Новые возможности Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="52fc9-591">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="52fc9-592">Устаревшие в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="52fc9-592">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-593">msRTCSIP-PolicyData (устарело)</span><span class="sxs-lookup"><span data-stu-id="52fc9-593">msRTCSIP-PolicyData (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="52fc9-594">Этот атрибут зарезервирован для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="52fc9-594">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-595">Новые возможности Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="52fc9-595">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="52fc9-596">Устаревшие в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="52fc9-596">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-597">msRTCSIP-PolicyType (устарело)</span><span class="sxs-lookup"><span data-stu-id="52fc9-597">msRTCSIP-PolicyType (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="52fc9-598">Этот однозначный атрибут строки Юникод включает тип политики.</span><span class="sxs-lookup"><span data-stu-id="52fc9-598">This single-valued Unicode string attribute contains the policy type.</span></span> <span data-ttu-id="52fc9-599">Ниже указаны допустимые типы политик.</span><span class="sxs-lookup"><span data-stu-id="52fc9-599">Valid policy types are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="52fc9-600">зала</span><span class="sxs-lookup"><span data-stu-id="52fc9-600">meeting</span></span></p></li>
<li><p><span data-ttu-id="52fc9-601">телефонии</span><span class="sxs-lookup"><span data-stu-id="52fc9-601">telephony</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="52fc9-602">Новые возможности Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="52fc9-602">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="52fc9-603">Устаревшие в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="52fc9-603">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-604">msRTCSIP-PoolAddress</span><span class="sxs-lookup"><span data-stu-id="52fc9-604">msRTCSIP-PoolAddress</span></span></p></td>
<td><p><span data-ttu-id="52fc9-605">Этот атрибут указывает ссылку обратно в пул, к которому принадлежит компьютер.</span><span class="sxs-lookup"><span data-stu-id="52fc9-605">This attribute specifies a link back to the pool to which a computer belongs.</span></span> <span data-ttu-id="52fc9-606">Этот атрибут задается независимо от того, работает ли на компьютере выпуск Standard Edition или выпуск Enterprise Edition для Lync Server.</span><span class="sxs-lookup"><span data-stu-id="52fc9-606">This attribute is set regardless of whether the computer is running the Standard Edition or the Enterprise Edition of Lync Server.</span></span> <span data-ttu-id="52fc9-607">Этот атрибут помечен для репликации глобального каталога.</span><span class="sxs-lookup"><span data-stu-id="52fc9-607">This attribute is marked for global catalog replication.</span></span></p>
<p><span data-ttu-id="52fc9-608">Допустимым значением является доменное имя пула.</span><span class="sxs-lookup"><span data-stu-id="52fc9-608">The valid value is the domain name of the pool.</span></span></p>
<p><span data-ttu-id="52fc9-609">Ссылка "вперед": <strong>ИД ссылки 11022</strong></span><span class="sxs-lookup"><span data-stu-id="52fc9-609">Forward link: <strong>Link ID 11022</strong></span></span></p>
<p><span data-ttu-id="52fc9-610">Для обратной ссылки на этот атрибут прямой ссылки будет задано значение <strong>msRTCSIP-FrontEndServers</strong>.</span><span class="sxs-lookup"><span data-stu-id="52fc9-610">The corresponding back link to this forward link attribute is <strong>msRTCSIP-FrontEndServers</strong>.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-611">Новые возможности Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="52fc9-611">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-612">msRTCSIP-PoolAddresses</span><span class="sxs-lookup"><span data-stu-id="52fc9-612">msRTCSIP-PoolAddresses</span></span></p></td>
<td><p><span data-ttu-id="52fc9-613">Это многозначный атрибут, содержащий список различающихся имен (DN) пулов, с которым связана фабрика MCU.</span><span class="sxs-lookup"><span data-stu-id="52fc9-613">This is a multi-valued attribute that contains a list of the distinguished names (DN) of pools with which the MCU factory is associated.</span></span></p>
<p><span data-ttu-id="52fc9-614">Обратная ссылка: <strong>идентификатор ссылки 11025</strong></span><span class="sxs-lookup"><span data-stu-id="52fc9-614">Back link: <strong>Link ID 11025</strong></span></span></p>
<p><span data-ttu-id="52fc9-615">Соответствующая ссылка "вперед" на эту ссылку <strong>msRTCSIP-MCUFactoryPath</strong>.</span><span class="sxs-lookup"><span data-stu-id="52fc9-615">The corresponding forward link to this back link is <strong>msRTCSIP-MCUFactoryPath</strong>.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-616">Новые возможности Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="52fc9-616">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-617">msRTCSIP-PoolData</span><span class="sxs-lookup"><span data-stu-id="52fc9-617">msRTCSIP-PoolData</span></span></p></td>
<td><p><span data-ttu-id="52fc9-618">Этот атрибут зарезервирован для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="52fc9-618">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-619">Новые возможности Live Communications Server 2005 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="52fc9-619">New in Live Communications Server 2005 with SP1.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-620">msRTCSIP-PoolDisplayName</span><span class="sxs-lookup"><span data-stu-id="52fc9-620">msRTCSIP-PoolDisplayName</span></span></p></td>
<td><p><span data-ttu-id="52fc9-621">Этот атрибут указывает произвольное имя для пула, отображаемого на консоли управления.</span><span class="sxs-lookup"><span data-stu-id="52fc9-621">This attribute specifies an arbitrary name for a pool that is displayed by the management console.</span></span> <span data-ttu-id="52fc9-622">Это имя может быть изменено администратором.</span><span class="sxs-lookup"><span data-stu-id="52fc9-622">This name can be changed by the administrator.</span></span></p>
<p><span data-ttu-id="52fc9-623">Допустимым значением является строка, представляющая имя пула.</span><span class="sxs-lookup"><span data-stu-id="52fc9-623">The valid value is a string representing the name of a pool.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-624">Новые возможности Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="52fc9-624">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-625">msRTCSIP-PoolDomainFQDN</span><span class="sxs-lookup"><span data-stu-id="52fc9-625">msRTCSIP-PoolDomainFQDN</span></span></p></td>
<td><p><span data-ttu-id="52fc9-626">Этот атрибут представляет собой строковое значение с одним значением.</span><span class="sxs-lookup"><span data-stu-id="52fc9-626">This attribute is a single-valued string value.</span></span> <span data-ttu-id="52fc9-627">Значение этого атрибута, если оно указано, представляет доменное имя домена пула, если администратор хочет создать пул переднего плана с полным доменным именем, не соответствующим структуре домена Active Directory, для которой создается пул переднего плана (например, пространство имен SIP, которое не было присвоено из пространства имен службы доменных имен).</span><span class="sxs-lookup"><span data-stu-id="52fc9-627">The value of this attribute, when present, represents the pool’s domain FQDN if the administrator wants to create a Front End pool with an FQDN that does not conform to the Active Directory domain structure in which the Front End pool is created (for example, a SIP namespace disjoined from Domain Name System (DNS) namespace).</span></span></p>
<p><span data-ttu-id="52fc9-628">Мы рекомендуем сопоставить полное доменное имя домена пула с именем домена в качестве домена Active Directory, в котором находится пул.</span><span class="sxs-lookup"><span data-stu-id="52fc9-628">We recommend that you map the Front End pool domain FQDN to the domain name portion as the Active Directory domain in which the pool resides.</span></span> <span data-ttu-id="52fc9-629">Таким образом, если в этом атрибуте значение не указано, то ДОМЕНное имя пула переднего плана по умолчанию будет представлять собой структуру доменных имен Active Directory, как указано в атрибуте <strong>dnsHostName</strong> .</span><span class="sxs-lookup"><span data-stu-id="52fc9-629">Therefore, when no value is present in this attribute, the Front End pool FQDN will default to the Active Directory domain name structure, as denoted by the <strong>dnsHostName</strong> attribute.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-630">Новые возможности Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="52fc9-630">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-631">msRTCSIP-PoolFunctionality</span><span class="sxs-lookup"><span data-stu-id="52fc9-631">msRTCSIP-PoolFunctionality</span></span></p></td>
<td><p><span data-ttu-id="52fc9-632">Многозначный список доменных имен всех серверов Lync Server, связанных с пулом.</span><span class="sxs-lookup"><span data-stu-id="52fc9-632">A multi-valued list of the domain names of all Lync Server, Enterprise Edition servers associated with a pool.</span></span> <span data-ttu-id="52fc9-633">Этот атрибут типа Integer определяет, может ли пул обмениваться мгновенными сообщениями и сведениями о присутствии и собраниях.</span><span class="sxs-lookup"><span data-stu-id="52fc9-633">This attribute of type integer defines whether the pool is capable of instant messaging (IM) and presence, and meetings.</span></span></p>
<p><span data-ttu-id="52fc9-634">Возможны следующие допустимые типы значений:</span><span class="sxs-lookup"><span data-stu-id="52fc9-634">The possible valid value types are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="52fc9-635">Не определено: служба обмена мгновенными сообщениями и сведениями о присутствии (сервер Live Communications Server 2005 и 2003)</span><span class="sxs-lookup"><span data-stu-id="52fc9-635">Undefined: IM and Presence Service (Live Communications Server 2005 and 2003)</span></span></p></li>
<li><p><span data-ttu-id="52fc9-636">1: служба мгновенных сообщений и присутствие (Lync Server)</span><span class="sxs-lookup"><span data-stu-id="52fc9-636">1: IM and Presence Service (Lync Server)</span></span></p></li>
<li><p><span data-ttu-id="52fc9-637">2: обмен мгновенными сообщениями и служба сведений о присутствии и собраниях (Lync Server)</span><span class="sxs-lookup"><span data-stu-id="52fc9-637">2: IM and Presence and Meeting Service (Lync Server)</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="52fc9-638">Новые возможности Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="52fc9-638">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-639">msRTCSIP-PoolType</span><span class="sxs-lookup"><span data-stu-id="52fc9-639">msRTCSIP-PoolType</span></span></p></td>
<td><p><span data-ttu-id="52fc9-640">Этот атрибут указывает, работает ли серверный пул на сервере Standard Edition Server или Enterprise Edition Server.</span><span class="sxs-lookup"><span data-stu-id="52fc9-640">This attribute specifies whether a server pool is running Standard Edition server or Enterprise Edition server.</span></span> <span data-ttu-id="52fc9-641">Этот атрибут является значением битовой маски типа Integer.</span><span class="sxs-lookup"><span data-stu-id="52fc9-641">This attribute is a bit-mask value of type integer.</span></span> <span data-ttu-id="52fc9-642">Каждый параметр представлен битом.</span><span class="sxs-lookup"><span data-stu-id="52fc9-642">Each option is represented by a bit.</span></span></p>
<p><span data-ttu-id="52fc9-643">Допустимые значения (и связанные с ними битовые положения) приведены ниже.</span><span class="sxs-lookup"><span data-stu-id="52fc9-643">The valid values (and associated bit positions) are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="52fc9-644">1: сервер Standard Edition, пользователи hosts (разрядное расположение 0)</span><span class="sxs-lookup"><span data-stu-id="52fc9-644">1: Standard Edition server, hosts users (bit position 0)</span></span></p></li>
<li><p><span data-ttu-id="52fc9-645">2: выпуск Enterprise Edition, пользователи hosts (разрядное расположение 1)</span><span class="sxs-lookup"><span data-stu-id="52fc9-645">2: Enterprise Edition server, hosts users (bit position 1)</span></span></p></li>
<li><p><span data-ttu-id="52fc9-646">4: сервер Standard Edition, приложения hosts (разрядное расположение 2)</span><span class="sxs-lookup"><span data-stu-id="52fc9-646">4: Standard Edition server, hosts applications (bit position 2)</span></span></p></li>
<li><p><span data-ttu-id="52fc9-647">8: сервер Enterprise Edition, приложения hosts (разрядное расположение 3)</span><span class="sxs-lookup"><span data-stu-id="52fc9-647">8: Enterprise Edition server, hosts applications (bit position 3)</span></span></p></li>
</ul>
<p><span data-ttu-id="52fc9-648">Поскольку Lync Server не поддерживает пулы, в которых размещаются только приложения, допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="52fc9-648">Because Lync Server does not support pools that host only applications, the only valid values are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="52fc9-649">5: Standard Edition Server, узлы пользователей и приложения (битовые позиции 0 и 2)</span><span class="sxs-lookup"><span data-stu-id="52fc9-649">5: Standard Edition server, hosts users and applications (bit positions 0 and 2)</span></span></p></li>
<li><p><span data-ttu-id="52fc9-650">10: Enterprise Edition Server, узлы пользователей и приложения (битовые позиции 1 и 3)</span><span class="sxs-lookup"><span data-stu-id="52fc9-650">10: Enterprise Edition server, hosts users and applications (bit positions 1 and 3)</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="52fc9-651">Новые возможности Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="52fc9-651">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-652">msRTCSIP-PoolVersion</span><span class="sxs-lookup"><span data-stu-id="52fc9-652">msRTCSIP-PoolVersion</span></span></p></td>
<td><p><span data-ttu-id="52fc9-653">Этот атрибут определяет версию пула.</span><span class="sxs-lookup"><span data-stu-id="52fc9-653">This attribute defines the pool version.</span></span> <span data-ttu-id="52fc9-654">Это целочисленный тип, который увеличивается при использовании каждого основного выпуска продукта.</span><span class="sxs-lookup"><span data-stu-id="52fc9-654">It is an integer type that is incremented with each major product release.</span></span></p>
<p><span data-ttu-id="52fc9-655">Возможны следующие допустимые типы значений:</span><span class="sxs-lookup"><span data-stu-id="52fc9-655">The possible valid value types are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="52fc9-656">0: сервер Live Communications Server 2003</span><span class="sxs-lookup"><span data-stu-id="52fc9-656">0: Live Communications Server 2003</span></span></p></li>
<li><p><span data-ttu-id="52fc9-657">1: сервер Live Communications Server 2005</span><span class="sxs-lookup"><span data-stu-id="52fc9-657">1: Live Communications Server 2005</span></span></p></li>
<li><p><span data-ttu-id="52fc9-658">2: сервер Live Communications Server 2005 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="52fc9-658">2: Live Communications Server 2005 with SP1</span></span></p></li>
<li><p><span data-ttu-id="52fc9-659">3: Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="52fc9-659">3: Office Communications Server 2007</span></span></p></li>
<li><p><span data-ttu-id="52fc9-660">4: Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="52fc9-660">4: Office Communications Server 2007 R2</span></span></p></li>
<li><p><span data-ttu-id="52fc9-661">5: Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="52fc9-661">5: Lync Server 2010</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="52fc9-662">Сервер Live Communications Server 2005 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="52fc9-662">Live Communications Server 2005 with SP1.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-663">msRTCSIP-PresenceFlags</span><span class="sxs-lookup"><span data-stu-id="52fc9-663">msRTCSIP-PresenceFlags</span></span></p></td>
<td><p><span data-ttu-id="52fc9-664">Этот атрибут включает параметры и флаги, определяющие параметры присутствия.</span><span class="sxs-lookup"><span data-stu-id="52fc9-664">This attribute contains options and flags that define presence settings.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-665">Новые возможности Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="52fc9-665">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-666">msRTCSIP-PresencePolicy</span><span class="sxs-lookup"><span data-stu-id="52fc9-666">msRTCSIP-PresencePolicy</span></span></p></td>
<td><p><span data-ttu-id="52fc9-667">Этот атрибут включает DN для объекта политики присутствия.</span><span class="sxs-lookup"><span data-stu-id="52fc9-667">This attribute contains the DN for a presence policy object.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-668">Новые возможности Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="52fc9-668">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-669">msRTCSIP-PrimaryHomeServer</span><span class="sxs-lookup"><span data-stu-id="52fc9-669">msRTCSIP-PrimaryHomeServer</span></span></p></td>
<td><p><span data-ttu-id="52fc9-670">Этот атрибут позволяет пользователю или контакту для обмена сообщениями SIP.</span><span class="sxs-lookup"><span data-stu-id="52fc9-670">This attribute enables a user or contact for SIP messaging.</span></span> <span data-ttu-id="52fc9-671">Он добавляется в класс Contact, так как в топологии центрального леса, объекты контактов, а не пользовательские объекты — включена поддержка SIP.</span><span class="sxs-lookup"><span data-stu-id="52fc9-671">It is added to the contact class because in the central forest topology, contact objects, not user objects, are SIP enabled.</span></span></p>
<p><span data-ttu-id="52fc9-672">Допустимым значением является различающееся имя пула переднего плана сервера Standard Edition или корпоративного выпуска Enterprise Edition, где находится пользователь.</span><span class="sxs-lookup"><span data-stu-id="52fc9-672">The valid value is the DN of the Standard Edition server or Enterprise Edition Front End pool where a user is homed.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-673">Новые возможности Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="52fc9-673">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-674">msRTCSIP-PrimaryUserAddress</span><span class="sxs-lookup"><span data-stu-id="52fc9-674">msRTCSIP-PrimaryUserAddress</span></span></p></td>
<td><p><span data-ttu-id="52fc9-675">Этот атрибут включает адрес SIP определенного пользователя.</span><span class="sxs-lookup"><span data-stu-id="52fc9-675">This attribute contains the SIP address of a given user.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-676">msRTCSIP-PrivateLine</span><span class="sxs-lookup"><span data-stu-id="52fc9-676">msRTCSIP-PrivateLine</span></span></p></td>
<td><p><span data-ttu-id="52fc9-677">Этот атрибут представляет идентификатор устройства для частной линии устройства.</span><span class="sxs-lookup"><span data-stu-id="52fc9-677">This attribute contains the device ID of the private line device.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-678">Новые возможности Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="52fc9-678">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-679">msRTCSIP с маршрутизацией</span><span class="sxs-lookup"><span data-stu-id="52fc9-679">msRTCSIP-Routable</span></span></p></td>
<td><p><span data-ttu-id="52fc9-680">Этот атрибут является логическим атрибутом, используемым для определения того, авторизован ли Lync Server для маршрутизации к этой службе с помощью ее адреса GRUU.</span><span class="sxs-lookup"><span data-stu-id="52fc9-680">This attribute is a Boolean attribute used to determine whether Lync Server is authorized to route to this service using its GRUU address.</span></span> <span data-ttu-id="52fc9-681">Если для этого параметра установлено значение <strong>true</strong>, Lync Server авторизован для маршрутизации к этой службе.</span><span class="sxs-lookup"><span data-stu-id="52fc9-681">If this value is set to <strong>TRUE</strong>, Lync Server is authorized to route to this service.</span></span> <span data-ttu-id="52fc9-682">Если для этого параметра задано значение <strong>false</strong>, Lync Server не уполномочен для маршрутизации к этой службе.</span><span class="sxs-lookup"><span data-stu-id="52fc9-682">If this value is set to <strong>FALSE</strong>, Lync Server is not authorized to route to this service.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-683">Новые возможности Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="52fc9-683">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-684">msRTCSIP-RouteUsageAttribute (устарело)</span><span class="sxs-lookup"><span data-stu-id="52fc9-684">msRTCSIP-RouteUsageAttribute (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="52fc9-685">Этот однозначный атрибут String Юникода определяет атрибут, который позволяет определять использование для телефонного маршрута.</span><span class="sxs-lookup"><span data-stu-id="52fc9-685">This single-valued UNICODE string attribute defines an attribute that qualifies the usage for a phone route.</span></span> <span data-ttu-id="52fc9-686">Выбор номера телефона определяется на основе двух элементов: атрибута использования, назначенного для телефонного маршрута, и атрибутов использования, разрешенных вызывающим участником.</span><span class="sxs-lookup"><span data-stu-id="52fc9-686">Selection of a phone route is determined based on two elements: the usage attribute assigned to the phone route and the caller’s allowed policy usage attributes.</span></span> <span data-ttu-id="52fc9-687">Первый телефонный маршрут с атрибутом использования, соответствующим разрешенному использованию вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="52fc9-687">The first phone route with a usage attribute that matches the caller’s allowed usage is selected.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-688">Новые возможности Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="52fc9-688">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="52fc9-689">Устаревшие в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="52fc9-689">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-690">msRTCSIP-RouteUsageLinks (устарело)</span><span class="sxs-lookup"><span data-stu-id="52fc9-690">msRTCSIP-RouteUsageLinks (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="52fc9-691">Этот атрибут различающегося многозначного имени (DN) включает список различающихся имен, используемых маршрутами.</span><span class="sxs-lookup"><span data-stu-id="52fc9-691">This multi-valued distinguished name (DN) attribute contains a list of route usage distinguished names.</span></span></p>
<p><span data-ttu-id="52fc9-692">Ссылка "вперед": <strong>ИД ссылки 11032</strong></span><span class="sxs-lookup"><span data-stu-id="52fc9-692">Forward link: <strong>Link ID 11032</strong></span></span></p>
<p><span data-ttu-id="52fc9-693">Этот атрибут является прямой ссылкой на соответствующую обратную ссылку <strong>msRTCSIP-PhoneRouteBL</strong>.</span><span class="sxs-lookup"><span data-stu-id="52fc9-693">This attribute is a forward link to the corresponding back link <strong>msRTCSIP-PhoneRouteBL</strong>.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-694">Устаревшие в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="52fc9-694">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-695">msRTCSIP-RoutingPoolDN</span><span class="sxs-lookup"><span data-stu-id="52fc9-695">msRTCSIP-RoutingPoolDN</span></span></p></td>
<td><p><span data-ttu-id="52fc9-696">Этот атрибут включает DN, указывающий на пул, который должен пройти весь трафик SIP, адресованный данной MCU или доверенной службе.</span><span class="sxs-lookup"><span data-stu-id="52fc9-696">This attribute contains the DN that points to the pool that all SIP traffic addressed to this MCU or Trusted Service must go through.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-697">Новые возможности Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="52fc9-697">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-698">msRTCSIP-RuleName (устарело)</span><span class="sxs-lookup"><span data-stu-id="52fc9-698">msRTCSIP-RuleName (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="52fc9-699">Этот однозначный строковый атрибут Юникода задает понятное имя правила нормализации, поэтому на него может легко ссылаться администратор.</span><span class="sxs-lookup"><span data-stu-id="52fc9-699">This single-valued UNICODE string attribute specifies the friendly name of the normalization rule, so it can easily be referenced by an administrator.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-700">Новые возможности Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="52fc9-700">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="52fc9-701">Устаревшие в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="52fc9-701">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-702">msRTCSIP-SchemaVersion</span><span class="sxs-lookup"><span data-stu-id="52fc9-702">msRTCSIP-SchemaVersion</span></span></p></td>
<td><p><span data-ttu-id="52fc9-703">Этот атрибут представляет версию схемы, которая в данный момент развернута в Организации.</span><span class="sxs-lookup"><span data-stu-id="52fc9-703">This attribute represents the schema version currently deployed in the organization.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-704">msRTCSIP-SearchMaxRequests (устарело)</span><span class="sxs-lookup"><span data-stu-id="52fc9-704">msRTCSIP-SearchMaxRequests (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="52fc9-705">Этот атрибут ограничивает число результатов поиска, возвращаемое при поиске в каталоге, когда пользователь осуществляет поиск контакта с помощью Communicator.</span><span class="sxs-lookup"><span data-stu-id="52fc9-705">This attribute limits the number of search results to be returned from a directory search when a user searches for a contact using Communicator.</span></span> <span data-ttu-id="52fc9-706">Этот атрибут будет переопределять значение, указанное клиентом.</span><span class="sxs-lookup"><span data-stu-id="52fc9-706">This attribute will override the value provided by the client.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-707">Устаревшие в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="52fc9-707">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-708">msRTCSIP-SearchMaxResults (устарело)</span><span class="sxs-lookup"><span data-stu-id="52fc9-708">msRTCSIP-SearchMaxResults (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="52fc9-709">Этот атрибут ограничивает количество возвращаемых запросов поиска.</span><span class="sxs-lookup"><span data-stu-id="52fc9-709">This attribute limits the number of search requests returned.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-710">Устаревшие в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="52fc9-710">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-711">msRTCSIP-ServerBL</span><span class="sxs-lookup"><span data-stu-id="52fc9-711">msRTCSIP-ServerBL</span></span></p></td>
<td><p><span data-ttu-id="52fc9-712">Этот атрибут с несколькими значениями является обратной ссылкой, которая содержит список различающихся имен (DN).</span><span class="sxs-lookup"><span data-stu-id="52fc9-712">This multi-valued attribute is a back link that contains a list of distinguished names (DN).</span></span> <span data-ttu-id="52fc9-713">Эти точки DNs для пула или объекта <strong>TrustedService</strong> .</span><span class="sxs-lookup"><span data-stu-id="52fc9-713">These DNs point to a pool or <strong>TrustedService</strong> object.</span></span></p>
<p><span data-ttu-id="52fc9-714">Этот атрибут соответствует ссылке "вперед" <strong>msRTCSIP-TrustedServiceLinks</strong>.</span><span class="sxs-lookup"><span data-stu-id="52fc9-714">This attribute corresponds to the forward link <strong>msRTCSIP-TrustedServiceLinks</strong>.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-715">Новые возможности Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="52fc9-715">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-716">msRTCSIP-ServerData</span><span class="sxs-lookup"><span data-stu-id="52fc9-716">msRTCSIP-ServerData</span></span></p></td>
<td><p><span data-ttu-id="52fc9-717">Этот атрибут зарезервирован для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="52fc9-717">This attribute is reserved for future use.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-718">msRTCSIP-ServerReferenceBL (устарело)</span><span class="sxs-lookup"><span data-stu-id="52fc9-718">msRTCSIP-ServerReferenceBL (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="52fc9-719">Этот атрибут с несколькими значениями включает список различающихся имен.</span><span class="sxs-lookup"><span data-stu-id="52fc9-719">This multi-valued attribute contains a list of distinguished names.</span></span> <span data-ttu-id="52fc9-720">Эти отличительные имена представляют собой обратные ссылки, которые ссылаются на другие объекты сервера, которые можно назначить профилю расположения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="52fc9-720">These distinguished names are back links that reference other server objects that can be assigned a default location profile.</span></span></p>
<p><span data-ttu-id="52fc9-721">Обратная ссылка: <strong>идентификатор ссылки 11037</strong></span><span class="sxs-lookup"><span data-stu-id="52fc9-721">Back link: <strong>Link ID 11037</strong></span></span></p>
<p><span data-ttu-id="52fc9-722">Соответствующая ссылка "вперед" на эту ссылку <strong>msRTCSIP-DefaultLocationProfileLink</strong>.</span><span class="sxs-lookup"><span data-stu-id="52fc9-722">The corresponding forward link to this back link is <strong>msRTCSIP-DefaultLocationProfileLink</strong>.</span></span></p>
<p><span data-ttu-id="52fc9-723">Этот атрибут обратной связи указывает только на пулы и серверы исправлений.</span><span class="sxs-lookup"><span data-stu-id="52fc9-723">This back link attribute references pools and Mediation Servers only.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-724">Новые возможности Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="52fc9-724">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="52fc9-725">Устаревшие в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="52fc9-725">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-726">msRTCSIP-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="52fc9-726">msRTCSIP-ServerVersion</span></span></p></td>
<td><p><span data-ttu-id="52fc9-727">Этот атрибут определяет сведения о версии сервера.</span><span class="sxs-lookup"><span data-stu-id="52fc9-727">This attribute defines the version information of the server.</span></span> <span data-ttu-id="52fc9-728">Этот номер версии действует для всех ролей сервера.</span><span class="sxs-lookup"><span data-stu-id="52fc9-728">This version number applies to all server roles.</span></span> <span data-ttu-id="52fc9-729">Это monotonously увеличивает целое число, которое увеличивается при использовании каждого официального выпуска продукта.</span><span class="sxs-lookup"><span data-stu-id="52fc9-729">It is a monotonously increasing integer that increments with each official product release.</span></span></p>
<p><span data-ttu-id="52fc9-730">Возможны следующие допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="52fc9-730">The possible valid values are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="52fc9-731">Не определено: сервер Live Communications Server 2003</span><span class="sxs-lookup"><span data-stu-id="52fc9-731">Undefined: Live Communications Server 2003</span></span></p>
<p>                 <span data-ttu-id="52fc9-732">Live Communications Server 2005</span><span class="sxs-lookup"><span data-stu-id="52fc9-732">Live Communications Server 2005</span></span></p>
<p>                 <span data-ttu-id="52fc9-733">Live Communications Server 2005 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="52fc9-733">Live Communications Server 2005 with SP1</span></span></p></li>
<li><p><span data-ttu-id="52fc9-734">3: Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="52fc9-734">3: Office Communications Server 2007</span></span></p></li>
<li><p><span data-ttu-id="52fc9-735">4: Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="52fc9-735">4: Office Communications Server 2007 R2</span></span></p></li>
<li><p><span data-ttu-id="52fc9-736">5: Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="52fc9-736">5: Lync Server 2010</span></span></p></li>
<li><p><span data-ttu-id="52fc9-737">6: Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="52fc9-737">6: Lync Server 2013</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="52fc9-738">Новые возможности Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="52fc9-738">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-739">msRTCSIP-SourceObjectType</span><span class="sxs-lookup"><span data-stu-id="52fc9-739">msRTCSIP-SourceObjectType</span></span></p></td>
<td><p><span data-ttu-id="52fc9-740">Этот атрибут с одним значением целочисленного типа задает тип объекта, на который указывает <strong>msDS-SourceObjectDN</strong> , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="52fc9-740">This single-valued attribute of integer type specifies the type of object the <strong>msDS-SourceObjectDN</strong> points to, as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="52fc9-741">NULL | 0x00000001: предоставляет объект пользователя-участника Windows NT Server из другого леса.</span><span class="sxs-lookup"><span data-stu-id="52fc9-741">null | 0x00000001: Represents a Windows NT Server principal user object from a different forest</span></span></p></li>
<li><p><span data-ttu-id="52fc9-742">Следующие атрибуты представляют типы групп из другого леса для развертывания групп рассылки.</span><span class="sxs-lookup"><span data-stu-id="52fc9-742">The following attributes represent a group type from a different forest for distribution group expansion:</span></span></p>
<ul>
<li><p><span data-ttu-id="52fc9-743">0x00000002: ADS_GROUP_TYPE_GLOBAL_GROUP</span><span class="sxs-lookup"><span data-stu-id="52fc9-743">0x00000002: ADS_GROUP_TYPE_GLOBAL_GROUP</span></span></p></li>
<li><p><span data-ttu-id="52fc9-744">0x00000004: ADS_GROUP_TYPE_DOMAIN_LOCAL_GROUP</span><span class="sxs-lookup"><span data-stu-id="52fc9-744">0x00000004: ADS_GROUP_TYPE_DOMAIN_LOCAL_GROUP</span></span></p></li>
<li><p><span data-ttu-id="52fc9-745">0x00000004: ADS_GROUP_TYPE_LOCAL_GROUP</span><span class="sxs-lookup"><span data-stu-id="52fc9-745">0x00000004: ADS_GROUP_TYPE_LOCAL_GROUP</span></span></p></li>
<li><p><span data-ttu-id="52fc9-746">0x00000008: ADS_GROUP_TYPE_UNIVERSAL_GROUP</span><span class="sxs-lookup"><span data-stu-id="52fc9-746">0x00000008: ADS_GROUP_TYPE_UNIVERSAL_GROUP</span></span></p></li>
<li><p><span data-ttu-id="52fc9-747">0x80000000: ADS_GROUP_TYPE_SECURITY_ENABLED</span><span class="sxs-lookup"><span data-stu-id="52fc9-747">0x80000000: ADS_GROUP_TYPE_SECURITY_ENABLED</span></span></p></li>
<li><p><span data-ttu-id="52fc9-748">0x90000000: представляет объект автоматического ассистента или абонентского доступа из того же леса или другого леса.</span><span class="sxs-lookup"><span data-stu-id="52fc9-748">0x90000000: Represents an Auto-Attendant or subscriber access object from the same forest or a different forest</span></span></p></li>
</ul></li>
</ul></td>
<td><p><span data-ttu-id="52fc9-749">Новые возможности Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="52fc9-749">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-750">msRTCSIP-SubscriptionAuthRequired (устарело)</span><span class="sxs-lookup"><span data-stu-id="52fc9-750">msRTCSIP-SubscriptionAuthRequired (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="52fc9-751">Новые возможности Live Communications Server 2003.</span><span class="sxs-lookup"><span data-stu-id="52fc9-751">New in Live Communications Server 2003.</span></span></p>
<p><span data-ttu-id="52fc9-752">Устаревшие возможности для сервера Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="52fc9-752">Obsolete in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-753">msRTCSIP-TargetHomeServer</span><span class="sxs-lookup"><span data-stu-id="52fc9-753">msRTCSIP-TargetHomeServer</span></span></p></td>
<td><p><span data-ttu-id="52fc9-754">Этот атрибут позволяет переместить пользователя или объект контакта из одного пула сервера Lync Server в другой.</span><span class="sxs-lookup"><span data-stu-id="52fc9-754">This attribute enables you to move a user or contact object from one Lync Server pool to another.</span></span> <span data-ttu-id="52fc9-755">Этот атрибут добавляется в класс Contact, так как в топологии центрального леса, объекты контактов, а не объекты пользователя, включены модули SIP.</span><span class="sxs-lookup"><span data-stu-id="52fc9-755">This attribute is added to the contact class, because in the central forest topology, contact objects, not user objects, are SIP enabled.</span></span></p>
<p><span data-ttu-id="52fc9-756">Допустимым значением является DN сервера назначения Standard Edition или переднего плана, в который нужно переместить пользователя.</span><span class="sxs-lookup"><span data-stu-id="52fc9-756">The valid value is the DN of the destination Standard Edition server or Front End pool to which a user is to be moved.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-757">Новые возможности Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="52fc9-757">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-758">msRTCSIP-TargetPhoneNumber (устарело)</span><span class="sxs-lookup"><span data-stu-id="52fc9-758">msRTCSIP-TargetPhoneNumber (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="52fc9-759">Этот однозначный атрибут String включает шаблон номера телефона или диапазон, который направляется на указанные шлюзы, определенные в <strong>msRTCSIP-Gateway</strong>.</span><span class="sxs-lookup"><span data-stu-id="52fc9-759">This single-valued string attribute contains a phone number pattern or range to route to the specified gateways defined in <strong>msRTCSIP-Gateways</strong>.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-760">Устаревшие в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="52fc9-760">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-761">msRTCSIP-TargetUserPolicies</span><span class="sxs-lookup"><span data-stu-id="52fc9-761">msRTCSIP-TargetUserPolicies</span></span></p></td>
<td><p><span data-ttu-id="52fc9-762">Этот атрибут хранит пары "имя-значение" для конечных политик пользователей Lync Server.</span><span class="sxs-lookup"><span data-stu-id="52fc9-762">This attribute stores name-value pairs for target policies for Lync Server users.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-763">Новые возможности Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="52fc9-763">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-764">msRTCSIP-TenantId</span><span class="sxs-lookup"><span data-stu-id="52fc9-764">msRTCSIP-TenantId</span></span></p></td>
<td><p><span data-ttu-id="52fc9-765">Этот атрибут хранит уникальный идентификатор клиента.</span><span class="sxs-lookup"><span data-stu-id="52fc9-765">This attribute stores the unique identifier for a tenant.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-766">Новые возможности Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="52fc9-766">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-767">msRTCSIP-трансляция (устаревшая)</span><span class="sxs-lookup"><span data-stu-id="52fc9-767">msRTCSIP-Translation (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="52fc9-768">Этот атрибут используется функцией голосовой связи в Lync Server и содержит строку перевода, применяемую при наборе номера, если найдено соответствие.</span><span class="sxs-lookup"><span data-stu-id="52fc9-768">This attribute is used by the voice feature of Lync Server and contains the translation string to apply on the dialed number, if a match is found.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-769">Новые возможности Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="52fc9-769">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="52fc9-770">Устаревшие в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="52fc9-770">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-771">msRTCSIP-TrustedMCUData</span><span class="sxs-lookup"><span data-stu-id="52fc9-771">msRTCSIP-TrustedMCUData</span></span></p></td>
<td><p><span data-ttu-id="52fc9-772">Этот атрибут зарезервирован для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="52fc9-772">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-773">Новые возможности Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="52fc9-773">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-774">msRTCSIP-TrustedMCUFQDN</span><span class="sxs-lookup"><span data-stu-id="52fc9-774">msRTCSIP-TrustedMCUFQDN</span></span></p></td>
<td><p><span data-ttu-id="52fc9-775">Этот атрибут представляет собой строковое значение, содержащее полное доменное имя MCU.</span><span class="sxs-lookup"><span data-stu-id="52fc9-775">This attribute is a string value that contains the FQDN of the MCU.</span></span> <span data-ttu-id="52fc9-776">Это атрибут с одним значением.</span><span class="sxs-lookup"><span data-stu-id="52fc9-776">This is a single-valued attribute.</span></span> <span data-ttu-id="52fc9-777">Допустимые значения для каждого сегмента — 63 символов; допустимое значение полного доменного имени — 255 символов.</span><span class="sxs-lookup"><span data-stu-id="52fc9-777">The valid value for each segment is 63 characters; the valid value for the entire FQDN is 255 characters.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-778">Новые возможности Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="52fc9-778">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-779">msRTCSIP-TrustedProxyData</span><span class="sxs-lookup"><span data-stu-id="52fc9-779">msRTCSIP-TrustedProxyData</span></span></p></td>
<td><p><span data-ttu-id="52fc9-780">Этот атрибут зарезервирован для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="52fc9-780">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-781">Новые возможности Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="52fc9-781">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-782">msRTCSIP-TrustedProxyFQDN</span><span class="sxs-lookup"><span data-stu-id="52fc9-782">msRTCSIP-TrustedProxyFQDN</span></span></p></td>
<td><p><span data-ttu-id="52fc9-783">Этот атрибут представляет собой строковое значение, содержащее полное доменное имя сервера, на котором запущен прокси-сервер.</span><span class="sxs-lookup"><span data-stu-id="52fc9-783">This attribute is a string value that contains the FQDN of the server running Proxy Server.</span></span> <span data-ttu-id="52fc9-784">Этот атрибут является однозначным.</span><span class="sxs-lookup"><span data-stu-id="52fc9-784">This attribute is single-valued.</span></span> <span data-ttu-id="52fc9-785">Допустимые значения для каждого сегмента — 63 символов; допустимое значение полного доменного имени — 255 символов.</span><span class="sxs-lookup"><span data-stu-id="52fc9-785">The valid value for each segment is 63 characters; the valid value for the entire FQDN is 255 characters.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-786">Новые возможности Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="52fc9-786">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-787">msRTCSIP-TrustedServerData</span><span class="sxs-lookup"><span data-stu-id="52fc9-787">msRTCSIP-TrustedServerData</span></span></p></td>
<td><p><span data-ttu-id="52fc9-788">Этот атрибут зарезервирован для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="52fc9-788">This attribute is reserved for future use.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-789">msRTCSIP-TrustedServerFQDN</span><span class="sxs-lookup"><span data-stu-id="52fc9-789">msRTCSIP-TrustedServerFQDN</span></span></p></td>
<td><p><span data-ttu-id="52fc9-790">Этот атрибут является атрибутом с одним значением, представляющим полное доменное имя доверенного сервера.</span><span class="sxs-lookup"><span data-stu-id="52fc9-790">This attribute is a single-valued attribute that represents the FQDN of a trusted server.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-791">Новые возможности Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="52fc9-791">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-792">msRTCSIP-TrustedServerVersion</span><span class="sxs-lookup"><span data-stu-id="52fc9-792">msRTCSIP-TrustedServerVersion</span></span></p></td>
<td><p><span data-ttu-id="52fc9-793">Этот атрибут указывает номер версии сервера в списке надежных серверов.</span><span class="sxs-lookup"><span data-stu-id="52fc9-793">This attribute specifies the version number of a server in the trusted server list.</span></span></p>
<p><span data-ttu-id="52fc9-794">Возможны следующие допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="52fc9-794">The possible valid values are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="52fc9-795">NULL: сервер Live Communications Server 2003</span><span class="sxs-lookup"><span data-stu-id="52fc9-795">NULL: Live Communications Server 2003</span></span></p></li>
<li><p><span data-ttu-id="52fc9-796">2: сервер Live Communications Server 2005</span><span class="sxs-lookup"><span data-stu-id="52fc9-796">2: Live Communications Server 2005</span></span></p></li>
<li><p><span data-ttu-id="52fc9-797">3: Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="52fc9-797">3: Office Communications Server 2007</span></span></p></li>
<li><p><span data-ttu-id="52fc9-798">4: Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="52fc9-798">4: Office Communications Server 2007 R2</span></span></p></li>
<li><p><span data-ttu-id="52fc9-799">5: Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="52fc9-799">5: Lync Server 2010</span></span></p></li>
<li><p><span data-ttu-id="52fc9-800">6: Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="52fc9-800">6: Lync Server 2013</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="52fc9-801">Новые возможности Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="52fc9-801">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-802">msRTCSIP-TrustedServiceFlags</span><span class="sxs-lookup"><span data-stu-id="52fc9-802">msRTCSIP-TrustedServiceFlags</span></span></p></td>
<td><p><span data-ttu-id="52fc9-803">Этот атрибут определяет параметры, включенные для доверенной службы.</span><span class="sxs-lookup"><span data-stu-id="52fc9-803">This attribute defines the options that are enabled for the trusted service.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-804">Новые возможности Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="52fc9-804">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-805">msRTCSIP-TrustedServiceLinks</span><span class="sxs-lookup"><span data-stu-id="52fc9-805">msRTCSIP-TrustedServiceLinks</span></span></p></td>
<td><p><span data-ttu-id="52fc9-806">Этот атрибут с несколькими значениями включает список отличительных имен (DN), которые ссылаются на доверенный объект службы, например службу проверки подлинности мультимедиа-ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="52fc9-806">This multi-valued attribute contains a list of distinguished names (DN) that reference a trusted service object, such as a Media Relay Authentication Service.</span></span> <span data-ttu-id="52fc9-807">Служба проверки подлинности мультимедиа-ретрансляции (которая физически размещена на пограничном сервере, выполняющем службу конференц-связи) должна быть связана с пулом, чтобы поддерживать звуковые сценарии для удаленных пользователей.</span><span class="sxs-lookup"><span data-stu-id="52fc9-807">A Media Relay Authentication Service (physically collocated on the Edge Server running the A/V Conferencing service) must be associated with a pool to support audio scenarios for remote users.</span></span></p>
<p><span data-ttu-id="52fc9-808">Для обратной ссылки на этот атрибут прямой ссылки будет задано значение <strong>msRTCSIP-ServerBL</strong>.</span><span class="sxs-lookup"><span data-stu-id="52fc9-808">The corresponding back link to this forward link attribute is <strong>msRTCSIP-ServerBL</strong>.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-809">ПЛАТФОРМЫ</span><span class="sxs-lookup"><span data-stu-id="52fc9-809">UC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-810">msRTCSIP-TrustedServicePort</span><span class="sxs-lookup"><span data-stu-id="52fc9-810">msRTCSIP-TrustedServicePort</span></span></p></td>
<td><p><span data-ttu-id="52fc9-811">Этот атрибут является целым числом, определяющим номер порта, который используется для подключения к этой службе GRUU.</span><span class="sxs-lookup"><span data-stu-id="52fc9-811">This attribute is an integer that defines the port number used to connect to this GRUU service.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-812">Новые возможности Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="52fc9-812">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-813">msRTCSIP-TrustedServiceType</span><span class="sxs-lookup"><span data-stu-id="52fc9-813">msRTCSIP-TrustedServiceType</span></span></p></td>
<td><p><span data-ttu-id="52fc9-814">Этот атрибут представляет собой строковое значение, определяющее тип GRUU службы.</span><span class="sxs-lookup"><span data-stu-id="52fc9-814">This attribute is a string value that defines the type of GRUU service it represents.</span></span></p>
<p><span data-ttu-id="52fc9-815">Допустимые типы служб GRUU описаны ниже.</span><span class="sxs-lookup"><span data-stu-id="52fc9-815">The valid GRUU service types are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="52fc9-816">MediationServer</span><span class="sxs-lookup"><span data-stu-id="52fc9-816">MediationServer</span></span></p></li>
<li><p><span data-ttu-id="52fc9-817">Шлюз</span><span class="sxs-lookup"><span data-stu-id="52fc9-817">Gateway</span></span></p></li>
<li><p><span data-ttu-id="52fc9-818">Служба проверки подлинности мультимедиа-ретрансляции (MRAS)</span><span class="sxs-lookup"><span data-stu-id="52fc9-818">Media Relay Authentication Service (MRAS)</span></span></p></li>
<li><p><span data-ttu-id="52fc9-819">QoSM</span><span class="sxs-lookup"><span data-stu-id="52fc9-819">QoSM</span></span></p></li>
<li><p><span data-ttu-id="52fc9-820">msRTCSIP — UserExtension CWA</span><span class="sxs-lookup"><span data-stu-id="52fc9-820">msRTCSIP-UserExtension CWA</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="52fc9-821">Новые возможности Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="52fc9-821">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-822">msRTCSIP-TrustedWebComponentsServerData</span><span class="sxs-lookup"><span data-stu-id="52fc9-822">msRTCSIP-TrustedWebComponentsServerData</span></span></p></td>
<td><p><span data-ttu-id="52fc9-823">Этот атрибут зарезервирован для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="52fc9-823">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-824">Новые возможности Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="52fc9-824">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-825">msRTCSIP-TrustedWebComponentsServerFQDN</span><span class="sxs-lookup"><span data-stu-id="52fc9-825">msRTCSIP-TrustedWebComponentsServerFQDN</span></span></p></td>
<td><p><span data-ttu-id="52fc9-826">Этот атрибут представляет собой строковое значение, содержащее полные доменные имена для IIS, на котором выполняются веб-службы Lync Server.</span><span class="sxs-lookup"><span data-stu-id="52fc9-826">This attribute is a string value that contains the FQDN of the IIS running Lync Server Web Services.</span></span> <span data-ttu-id="52fc9-827">Это атрибут с одним значением.</span><span class="sxs-lookup"><span data-stu-id="52fc9-827">This is a single-valued attribute.</span></span> <span data-ttu-id="52fc9-828">Допустимые значения для каждого сегмента — 63 символов; допустимое значение полного доменного имени — 255 символов.</span><span class="sxs-lookup"><span data-stu-id="52fc9-828">The valid value for each segment is 63 characters; the valid value for the entire FQDN is 255 characters.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-829">Новые возможности Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="52fc9-829">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-830">msRTCSIP-UCFlags (устарело)</span><span class="sxs-lookup"><span data-stu-id="52fc9-830">msRTCSIP-UCFlags (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="52fc9-831">Этот атрибут определяет различные параметры UC, которые включаются глобально для всех пользователей и объектов контактов.</span><span class="sxs-lookup"><span data-stu-id="52fc9-831">This attribute defines different UC options that are enabled globally to all user or contact objects.</span></span> <span data-ttu-id="52fc9-832">Этот атрибут является значением битовой маски целочисленного типа.</span><span class="sxs-lookup"><span data-stu-id="52fc9-832">This attribute is a bit-mask value of integer type.</span></span> <span data-ttu-id="52fc9-833">Каждый вариант представляется наличием бита.</span><span class="sxs-lookup"><span data-stu-id="52fc9-833">Each option is represented by the presence of a bit.</span></span></p>
<p><span data-ttu-id="52fc9-834">Возможны следующие допустимые значения (и связанное расположение битов).</span><span class="sxs-lookup"><span data-stu-id="52fc9-834">The possible valid value (and associated bit position) are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="52fc9-835">4: UsePerUserUCPolicy (разрядное расположение 2)</span><span class="sxs-lookup"><span data-stu-id="52fc9-835">4: UsePerUserUCPolicy (bit position 2)</span></span></p></li>
</ul>
<p><span data-ttu-id="52fc9-836">Если задан этот бит, политика UC определена для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="52fc9-836">When this bit is set, the UC policy is defined per user.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-837">Устаревшие в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="52fc9-837">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-838">msRTCSIP-UCPolicy (устарело)</span><span class="sxs-lookup"><span data-stu-id="52fc9-838">msRTCSIP-UCPolicy (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="52fc9-839">Этот атрибут с одним значением содержит различающееся имя (DN) политики UC, которой назначен администратор для этого пользователя.</span><span class="sxs-lookup"><span data-stu-id="52fc9-839">This single-valued attribute contains the distinguished name (DN) of the UC policy that the administrator has assigned for this user.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-840">Устаревшие в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="52fc9-840">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-841">msRTCSIP-UserDomainList (устарело)</span><span class="sxs-lookup"><span data-stu-id="52fc9-841">msRTCSIP-UserDomainList (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="52fc9-842">Этот атрибут предоставляет список всех доменов в лесу, которые размещает пользователей с поддержкой SIP.</span><span class="sxs-lookup"><span data-stu-id="52fc9-842">This attribute provides a list of all the domains in a forest that host SIP-enabled users.</span></span> <span data-ttu-id="52fc9-843">По умолчанию это пустой список, указывающий на то, что все домены в лесу включены с поддержкой SIP.</span><span class="sxs-lookup"><span data-stu-id="52fc9-843">The default is an empty list, indicating that all domains in the forest are SIP-enabled.</span></span></p>
<p><span data-ttu-id="52fc9-844">Допустимые значения — это несколько строк, представляющих доменные имена отдельных доменов.</span><span class="sxs-lookup"><span data-stu-id="52fc9-844">Valid values are multiple strings representing the domain names of individual domains.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-845">Новые возможности Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="52fc9-845">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="52fc9-846">Устаревшие в Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="52fc9-846">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-847">msRTCSIP-UserEnabled</span><span class="sxs-lookup"><span data-stu-id="52fc9-847">msRTCSIP-UserEnabled</span></span></p></td>
<td><p><span data-ttu-id="52fc9-848">Этот атрибут определяет, разрешено ли в данный момент пользователь Lync Server.</span><span class="sxs-lookup"><span data-stu-id="52fc9-848">This attribute determines whether the user is currently enabled for Lync Server.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-849">msRTCSIP-UserExtension</span><span class="sxs-lookup"><span data-stu-id="52fc9-849">msRTCSIP-UserExtension</span></span></p></td>
<td><p><span data-ttu-id="52fc9-850">Этот атрибут с несколькими значениями включает список пар "имя-значение" в формате &quot; name = value. &quot; Этот атрибут помечен для репликации глобального каталога.</span><span class="sxs-lookup"><span data-stu-id="52fc9-850">This multi-valued attribute contains a list of name-value pairs in the format of &quot;name=value.&quot; This attribute is marked for global catalog replication.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-851">Новые возможности Live Communications Server 2005 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="52fc9-851">New in Live Communications Server 2005 with SP1.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-852">msRTCSIP-UserLocationProfile</span><span class="sxs-lookup"><span data-stu-id="52fc9-852">msRTCSIP-UserLocationProfile</span></span></p></td>
<td><p><span data-ttu-id="52fc9-853">Этот атрибут включает различающееся имя (DN), которое указывает на объект профиля расположения.</span><span class="sxs-lookup"><span data-stu-id="52fc9-853">This attribute contains the distinguished name (DN) that points to a location profile object.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-854">Новые возможности Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="52fc9-854">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-855">msRTCSIP-UserPolicies</span><span class="sxs-lookup"><span data-stu-id="52fc9-855">msRTCSIP-UserPolicies</span></span></p></td>
<td><p><span data-ttu-id="52fc9-856">Этот атрибут хранит пары "имя-значение" для политик пользователей.</span><span class="sxs-lookup"><span data-stu-id="52fc9-856">This attribute stores name-value pairs for user policies.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-857">Новые возможности Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="52fc9-857">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-858">msRTCSIP-UserPolicy</span><span class="sxs-lookup"><span data-stu-id="52fc9-858">msRTCSIP-UserPolicy</span></span></p></td>
<td><p><span data-ttu-id="52fc9-859">Это многозначный атрибут, содержащий список различающихся имен с двоичными (DN_WITH_BINARY), указывающими на глобальные политики пользователей различных типов.</span><span class="sxs-lookup"><span data-stu-id="52fc9-859">This is a multi-valued attribute containing a list of distinguished names with binary (DN_WITH_BINARY) pointing to global user policies of different types.</span></span> <span data-ttu-id="52fc9-860">Двоичная часть указывает тип политики, на которую указывает область DN.</span><span class="sxs-lookup"><span data-stu-id="52fc9-860">The binary part indicates the type of policy to which the DN portion points.</span></span></p>
<p><span data-ttu-id="52fc9-861">Допустимы следующие двоичные значения:</span><span class="sxs-lookup"><span data-stu-id="52fc9-861">The valid binary values are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="52fc9-862">0x00000001: политика собраний</span><span class="sxs-lookup"><span data-stu-id="52fc9-862">0x00000001: Meeting policy</span></span></p></li>
<li><p><span data-ttu-id="52fc9-863">0x00000002: политика UC</span><span class="sxs-lookup"><span data-stu-id="52fc9-863">0x00000002: UC policy</span></span></p></li>
<li><p><span data-ttu-id="52fc9-864">0x00000005: политика присутствия</span><span class="sxs-lookup"><span data-stu-id="52fc9-864">0x00000005: Presence policy</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="52fc9-865">Новые возможности Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="52fc9-865">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-866">msRTCSIP-UserRoutingGroupId</span><span class="sxs-lookup"><span data-stu-id="52fc9-866">msRTCSIP-UserRoutingGroupId</span></span></p></td>
<td><p><span data-ttu-id="52fc9-867">Это идентификатор группы маршрутизации SIP.</span><span class="sxs-lookup"><span data-stu-id="52fc9-867">This is the SIP routing group ID.</span></span> <span data-ttu-id="52fc9-868">Пользователи в одной группе будут регистрироваться на одном и том же внешнем сервере.</span><span class="sxs-lookup"><span data-stu-id="52fc9-868">Users in the same group will register to the same Front End Server.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-869">Новые возможности Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="52fc9-869">New in Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-870">msRTCSIP-WebComponentsData</span><span class="sxs-lookup"><span data-stu-id="52fc9-870">msRTCSIP-WebComponentsData</span></span></p></td>
<td><p><span data-ttu-id="52fc9-871">Это атрибут с несколькими значениями.</span><span class="sxs-lookup"><span data-stu-id="52fc9-871">This is a multi-valued attribute.</span></span> <span data-ttu-id="52fc9-872">Этот атрибут зарезервирован для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="52fc9-872">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-873">Новые возможности Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="52fc9-873">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-874">msRTCSIP-WebComponentsPoolAddress</span><span class="sxs-lookup"><span data-stu-id="52fc9-874">msRTCSIP-WebComponentsPoolAddress</span></span></p></td>
<td><p><span data-ttu-id="52fc9-875">Этот атрибут с одним значением указывает на сервер пула или стандартный выпуск, к которому относятся веб-компоненты.</span><span class="sxs-lookup"><span data-stu-id="52fc9-875">This single-valued attribute points to the pool or Standard Edition server to which the web components belong.</span></span></p>
<p><span data-ttu-id="52fc9-876">Ссылка "вперед": <strong>ИД ссылки 11028</strong></span><span class="sxs-lookup"><span data-stu-id="52fc9-876">Forward link: <strong>Link ID 11028</strong></span></span></p>
<p><span data-ttu-id="52fc9-877">Для обратной ссылки на этот атрибут прямой ссылки будет задано значение <strong>msRTCSIP-WebComponentsServers</strong>.</span><span class="sxs-lookup"><span data-stu-id="52fc9-877">The corresponding back link to this forward link attribute is <strong>msRTCSIP-WebComponentsServers</strong>.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-878">Новые возможности Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="52fc9-878">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-879">msRTCSIP-WebComponentsServers</span><span class="sxs-lookup"><span data-stu-id="52fc9-879">msRTCSIP-WebComponentsServers</span></span></p></td>
<td><p><span data-ttu-id="52fc9-880">Этот атрибут представляет собой список различающихся имен, одновременно допускающего несколько значений.</span><span class="sxs-lookup"><span data-stu-id="52fc9-880">This attribute is a multi-valued list of distinguished names.</span></span> <span data-ttu-id="52fc9-881">Этот атрибут включает список всех веб-серверов, связанных с этим пулом.</span><span class="sxs-lookup"><span data-stu-id="52fc9-881">This attribute contains a list of all Web servers associated with this pool.</span></span></p>
<p><span data-ttu-id="52fc9-882">Обратная ссылка: <strong>идентификатор ссылки 11029</strong></span><span class="sxs-lookup"><span data-stu-id="52fc9-882">Back link: <strong>Link ID 11029</strong></span></span></p>
<p><span data-ttu-id="52fc9-883">Соответствующая ссылка "вперед" на эту ссылку <strong>msRTCSIP-WebComponentsPoolAddress</strong>.</span><span class="sxs-lookup"><span data-stu-id="52fc9-883">The corresponding forward link to this back link is <strong>msRTCSIP-WebComponentsPoolAddress</strong>.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-884">Новые возможности Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="52fc9-884">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-885">msRTCSIP-WMIInstanceId (устарело)</span><span class="sxs-lookup"><span data-stu-id="52fc9-885">msRTCSIP-WMIInstanceId (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="52fc9-886">Новые возможности Live Communications Server 2003.</span><span class="sxs-lookup"><span data-stu-id="52fc9-886">New in Live Communications Server 2003.</span></span></p>
<p><span data-ttu-id="52fc9-887">Устаревшие возможности для сервера Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="52fc9-887">Obsolete in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-888">OtherIPPhone</span><span class="sxs-lookup"><span data-stu-id="52fc9-888">OtherIPPhone</span></span></p></td>
<td><p><span data-ttu-id="52fc9-889">Этот существующий атрибут Active Directory используется телефонией для указания списка альтернативных TCP/IP-адресов для телефона.</span><span class="sxs-lookup"><span data-stu-id="52fc9-889">This existing Active Directory attribute is used by telephony to specify the list of alternate TCP/IP addresses for a phone.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-890">Новые возможности операционной системы Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="52fc9-890">New in Windows Server 2008 operating system.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-891">PhoneOfficeOther</span><span class="sxs-lookup"><span data-stu-id="52fc9-891">PhoneOfficeOther</span></span></p></td>
<td><p><span data-ttu-id="52fc9-892">Этот существующий атрибут Active Directory используется в Lync Server для доступа к объектам контакта только в целях маршрутизации обращений к функциям автоматического ассистента единой системы обмена сообщениями и номерам абонентов.</span><span class="sxs-lookup"><span data-stu-id="52fc9-892">This existing Active Directory attribute is used by the voice components in Lync Server, for contact objects only, for the purpose of routing calls to the unified messaging auto-attendant and subscriber access numbers.</span></span> <span data-ttu-id="52fc9-893">Адрес для переадресации неусловного звонка сохраняется в атрибуте с несколькими значениями.</span><span class="sxs-lookup"><span data-stu-id="52fc9-893">The unconditional call forwarding address is stored in this multi-valued attribute.</span></span> <span data-ttu-id="52fc9-894">Эта учетная запись создается для определенной цели автоматического ассистента и абонентского доступа.</span><span class="sxs-lookup"><span data-stu-id="52fc9-894">This account is created for the specific purpose of auto-attendant and subscriber access.</span></span> <span data-ttu-id="52fc9-895">Атрибуты этой учетной записи не должны изменяться администраторами.</span><span class="sxs-lookup"><span data-stu-id="52fc9-895">This account’s attributes should not be modified by administrators.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-896">Новые возможности в операционной системе Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="52fc9-896">New in Windows 2000 operating system.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52fc9-897">ProxyAddresses</span><span class="sxs-lookup"><span data-stu-id="52fc9-897">ProxyAddresses</span></span></p></td>
<td><p><span data-ttu-id="52fc9-898">Этот существующий многозначный атрибут Active Directory является частью базовой схемы Active Directory, представленной в Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="52fc9-898">This existing Active Directory multi-valued attribute is part of the base Active Directory schema introduced in Windows 2000.</span></span> <span data-ttu-id="52fc9-899">Этот атрибут включает различные адреса X400, X500 и SMTP для электронной почты пользователя.</span><span class="sxs-lookup"><span data-stu-id="52fc9-899">This attribute contains the various X400, X500, and SMTP addresses of the user’s email.</span></span> <span data-ttu-id="52fc9-900">В реальном Communications Server 2003 и более поздних версиях URI пользователя SIP добавляется в этот список с помощью &quot; тега SIP: &quot; .</span><span class="sxs-lookup"><span data-stu-id="52fc9-900">In Live Communications Server 2003 and later, the user’s SIP URI is added to this list, using the &quot;sip:&quot; tag.</span></span></p>
<p><span data-ttu-id="52fc9-901">Следующие приложения выполняйте поиск URI пользователя SIP из этого атрибута:</span><span class="sxs-lookup"><span data-stu-id="52fc9-901">The following applications search the user’s SIP URI from this attribute:</span></span></p>
<ul>
<li><p><span data-ttu-id="52fc9-902">Клиент обмена сообщениями и совместной работы в Microsoft Office Outlook 2003</span><span class="sxs-lookup"><span data-stu-id="52fc9-902">Microsoft Office Outlook 2003 messaging and collaboration client</span></span></p></li>
<li><p><span data-ttu-id="52fc9-903">Microsoft Office SharePoint Server 2007</span><span class="sxs-lookup"><span data-stu-id="52fc9-903">Microsoft Office SharePoint Server 2007</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="52fc9-904">Новые возможности в операционной системе Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="52fc9-904">New in Windows 2000 operating system.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52fc9-905">TelephoneNumber</span><span class="sxs-lookup"><span data-stu-id="52fc9-905">TelephoneNumber</span></span></p></td>
<td><p><span data-ttu-id="52fc9-906">Этот существующий атрибут Active Directory включает номер телефона пользователя.</span><span class="sxs-lookup"><span data-stu-id="52fc9-906">This existing Active Directory attribute contains the telephone number for the user.</span></span></p></td>
<td><p><span data-ttu-id="52fc9-907">Новые возможности в операционной системе Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="52fc9-907">New in Windows 2000 operating system.</span></span></p></td>
</tr><span data-ttu-id="52fc9-908">
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="52fc9-908">
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

