---
title: 'Lync Server 2013: список таблиц сервера сохраняемого чата'
description: 'Lync Server 2013: список таблиц сервера для сохраняемого чата.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: List of Persistent Chat Server tables
ms:assetid: 26c9e271-3516-4d90-b930-70fec4e359ea
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558628(v=OCS.15)
ms:contentKeyID: 48183659
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 838e6d8f83b137923075851b29df4c602a487391
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426587"
---
# <a name="list-of-persistent-chat-server-tables-in-lync-server-2013"></a><span data-ttu-id="af94d-103">Список таблиц сервера сохраняемого чата в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="af94d-103">List of Persistent Chat Server tables in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="af94d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="af94d-104">

<span> </span></span></span>

<span data-ttu-id="af94d-105">_**Тема последнего изменения:** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="af94d-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="af94d-106">Схема базы данных сохраняемого чата состоит из следующих таблиц.</span><span class="sxs-lookup"><span data-stu-id="af94d-106">The Persistent Chat database schema consists of the following tables.</span></span>

<div>

## <a name="active-directory-sync"></a><span data-ttu-id="af94d-107">Синхронизация службы каталогов Active Directory</span><span class="sxs-lookup"><span data-stu-id="af94d-107">Active Directory Sync</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="af94d-108">Таблица</span><span class="sxs-lookup"><span data-stu-id="af94d-108">Table</span></span></th>
<th><span data-ttu-id="af94d-109">Описание</span><span class="sxs-lookup"><span data-stu-id="af94d-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="af94d-110"><a href="lync-server-2013-tbladcookie.md">tblADCookie в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="af94d-110"><a href="lync-server-2013-tbladcookie.md">tblADCookie in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="af94d-111">В этой папке содержатся файлы cookie для синхронизации протокола Lightweight Directory Access.</span><span class="sxs-lookup"><span data-stu-id="af94d-111">Contains the current Lightweight Directory Access Protocol (LDAP) Sync cookies.</span></span> <span data-ttu-id="af94d-112">Каждая строка соответствует домену доменных служб Active Directory, в котором активный сервер чата отслеживает изменения.</span><span class="sxs-lookup"><span data-stu-id="af94d-112">Each row corresponds to an Active Directory Domain Services domain that Persistent Chat Server is actively monitoring for changes.</span></span> <span data-ttu-id="af94d-113">(В этой таблице представлены только те домены службы каталогов Active Directory, которые относятся к серверу сохраняемого чата.)</span><span class="sxs-lookup"><span data-stu-id="af94d-113">(Only the Active Directory domains that are relevant for Persistent Chat Server are represented in this table.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="af94d-114"><a href="lync-server-2013-tblprincipalmemberdifference.md">tblPrincipalMemberDifference в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="af94d-114"><a href="lync-server-2013-tblprincipalmemberdifference.md">tblPrincipalMemberDifference in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="af94d-115">Содержит изменения членства в группах (добавленные и удаленные участники), которые еще не были обработаны с помощью последующих шагов синхронизации Active Directory и являются одной из временных таблиц (вместе с таблицей tblADUpdates), которая используется на первом этапе синхронизации Active Directory.</span><span class="sxs-lookup"><span data-stu-id="af94d-115">Contains group membership changes (both added and removed members) that have not yet been processed by the later Active Directory Sync steps and is one of the temporary tables (along with tblADUpdates table) that is used in the first step of Active Directory Sync.</span></span></p>
<p><span data-ttu-id="af94d-116">Изменения в членстве сохраняются, обрабатываются или отображаются только для групп, указанных в таблице tblPrincipal или уже содержащихся в них участников.</span><span class="sxs-lookup"><span data-stu-id="af94d-116">Membership changes are stored, processed, or both, only for groups that are listed in the tblPrincipal table or that already have members listed there.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="af94d-117"><a href="lync-server-2013-tbladupdates.md">tblADUpdates в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="af94d-117"><a href="lync-server-2013-tbladupdates.md">tblADUpdates in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="af94d-118">Содержит изменения доменных служб Active Directory, которые еще не были обработаны с помощью последующих шагов синхронизации Active Directory и являются одной из временных таблиц (вместе с таблицей tblPrincipalMemberDifference), которая используется на первом этапе синхронизации Active Directory.</span><span class="sxs-lookup"><span data-stu-id="af94d-118">Contains changes to Active Directory Domain Services that have not yet been processed by the later Active Directory Sync steps and is one of the temporary tables (along with the tblPrincipalMemberDifference table) that is used in the first step of Active Directory Sync.</span></span></p>
<p><span data-ttu-id="af94d-119">Изменения, вносимые в Active Directory, сохраняются, обрабатываются или обе будут только для участников, которые уже указаны в таблице tblPrincipal.</span><span class="sxs-lookup"><span data-stu-id="af94d-119">Changes to Active Directory are stored, processed, or both only for principals that are already listed in the tblPrincipal table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="af94d-120"><a href="lync-server-2013-tblprincipalmembers.md">tblPrincipalMembers в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="af94d-120"><a href="lync-server-2013-tblprincipalmembers.md">tblPrincipalMembers in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="af94d-121">Сведения о членстве участников.</span><span class="sxs-lookup"><span data-stu-id="af94d-121">Contains principal memberships.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="af94d-122"><a href="lync-server-2013-tblprincipalmeta.md">tblPrincipalMeta в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="af94d-122"><a href="lync-server-2013-tblprincipalmeta.md">tblPrincipalMeta in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="af94d-123">Содержит участников, которые необходимо обновлять из службы каталогов Active Directory.</span><span class="sxs-lookup"><span data-stu-id="af94d-123">Contains the principals that have to be refreshed from Active Directory.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="af94d-124"><a href="lync-server-2013-tblskippedaffiliations.md">tblSkippedAffiliations в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="af94d-124"><a href="lync-server-2013-tblskippedaffiliations.md">tblSkippedAffiliations in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="af94d-125">Содержат назначения, которые не удалось обновить по некоторым причинам, обычно из-за ошибок доступа в службе каталогов Active Directory.</span><span class="sxs-lookup"><span data-stu-id="af94d-125">Contains affiliations that could not be refreshed for some reason, usually due to Active Directory access errors.</span></span></p>
<p><span data-ttu-id="af94d-126">Эта таблица предназначена исключительно для информационных целей.</span><span class="sxs-lookup"><span data-stu-id="af94d-126">This table is for informational purposes only.</span></span> <span data-ttu-id="af94d-127">Его содержимое не используется.</span><span class="sxs-lookup"><span data-stu-id="af94d-127">Its content is not used.</span></span></p>
<p><span data-ttu-id="af94d-128">Участники с назначением, которые не удалось обновить надлежащим образом, хранятся в таблице tblPrincipalMeta и получают другой шанс на обновление.</span><span class="sxs-lookup"><span data-stu-id="af94d-128">The principals with affiliations that could not be refreshed properly are kept in the tblPrincipalMeta table and are given another chance to be refreshed.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="principals-affiliations-nodes-scopes-and-roles"></a><span data-ttu-id="af94d-129">Участники, принадлежности, узлы, области и роли</span><span class="sxs-lookup"><span data-stu-id="af94d-129">Principals, Affiliations, Nodes, Scopes, and Roles</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="af94d-130">Таблица</span><span class="sxs-lookup"><span data-stu-id="af94d-130">Table</span></span></th>
<th><span data-ttu-id="af94d-131">Описание</span><span class="sxs-lookup"><span data-stu-id="af94d-131">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="af94d-132"><a href="lync-server-2013-tblprincipaltype.md">tblPrincipalType в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="af94d-132"><a href="lync-server-2013-tblprincipaltype.md">tblPrincipalType in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="af94d-133">Содержит типы принципалов для классификации содержимого в таблице tblPrincipal.</span><span class="sxs-lookup"><span data-stu-id="af94d-133">Contains principal types to categorize what is in the tblPrincipal table.</span></span> <span data-ttu-id="af94d-134">Эта таблица является статичной.</span><span class="sxs-lookup"><span data-stu-id="af94d-134">This table is static.</span></span> <span data-ttu-id="af94d-135">Он настроен во время создания базы данных и не меняется.</span><span class="sxs-lookup"><span data-stu-id="af94d-135">It is set up during database creation and does not change.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="af94d-136"><a href="lync-server-2013-tblprincipal.md">tblPrincipal в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="af94d-136"><a href="lync-server-2013-tblprincipal.md">tblPrincipal in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="af94d-137">Содержат все участники (пользователи, папки, группы и т. д.).</span><span class="sxs-lookup"><span data-stu-id="af94d-137">Contains all principals (users, folders, groups, and so on).</span></span> <span data-ttu-id="af94d-138">Сервер сохраняемого чата обрабатывает его как плоский разнородный список.</span><span class="sxs-lookup"><span data-stu-id="af94d-138">Persistent Chat Server handles this as a flat heterogeneous list.</span></span> <span data-ttu-id="af94d-139">Различные столбцы основываются на типе каждого участника.</span><span class="sxs-lookup"><span data-stu-id="af94d-139">Various columns are based on the type of each principal.</span></span></p>
<p><span data-ttu-id="af94d-140">Большинство из этих участников кэшируют копии объектов, которые хранятся в Active Directory.</span><span class="sxs-lookup"><span data-stu-id="af94d-140">Most of these principals are cached copies of objects stored in Active Directory.</span></span> <span data-ttu-id="af94d-141">Создание кэшированной копии в основной таблице этих объектов Active Directory называется <em>Подготовка</em>.</span><span class="sxs-lookup"><span data-stu-id="af94d-141">Creating the cached copy in the Principal table of these Active Directory objects is referred as <em>provisioning</em>.</span></span></p>
<p><span data-ttu-id="af94d-142">Некоторые принципалы создаются более агрессивно, чем другие, а некоторые объекты Active Directory пропускаются полностью.</span><span class="sxs-lookup"><span data-stu-id="af94d-142">Some principals are created more aggressively than others, and some Active Directory objects are ignored altogether.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="af94d-143"><a href="lync-server-2013-tblprincipalaffiliations.md">tblPrincipalAffiliations в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="af94d-143"><a href="lync-server-2013-tblprincipalaffiliations.md">tblPrincipalAffiliations in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="af94d-144">Содержат основные принадлежности, описывающие участие в группах безопасности Active Directory, контейнерах Active Directory и т. д.</span><span class="sxs-lookup"><span data-stu-id="af94d-144">Contains principal affiliations that describe memberships in Active Directory security groups, Active Directory containers, and so on.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="af94d-145"><a href="lync-server-2013-tblnode.md">tblNode в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="af94d-145"><a href="lync-server-2013-tblnode.md">tblNode in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="af94d-146">Раздел "Категория", управляемый на панели управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="af94d-146">Contains the category node, as managed in Lync Server Control Panel.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="af94d-147"><a href="lync-server-2013-tblroletype.md">tblRoleType в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="af94d-147"><a href="lync-server-2013-tblroletype.md">tblRoleType in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="af94d-148">Содержат типы ролей и связанные с ними наборы разрешений.</span><span class="sxs-lookup"><span data-stu-id="af94d-148">Contains role types and their associated permission sets.</span></span> <span data-ttu-id="af94d-149">Эта таблица подстановки является статичной.</span><span class="sxs-lookup"><span data-stu-id="af94d-149">This lookup table is static.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="af94d-150"><a href="lync-server-2013-tblscopeprincipal.md">tblScopePrincipal в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="af94d-150"><a href="lync-server-2013-tblscopeprincipal.md">tblScopePrincipal in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="af94d-151">Содержат области, назначенные узлам.</span><span class="sxs-lookup"><span data-stu-id="af94d-151">Contains scopes assigned to nodes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="af94d-152"><a href="lync-server-2013-tblprincipalrole.md">tblPrincipalRole в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="af94d-152"><a href="lync-server-2013-tblprincipalrole.md">tblPrincipalRole in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="af94d-153">Содержат роли, назначенные узлам.</span><span class="sxs-lookup"><span data-stu-id="af94d-153">Contains roles assigned to nodes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="af94d-154"><a href="lync-server-2013-tblsiopwhitelist.md">tblSiopWhiteList в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="af94d-154"><a href="lync-server-2013-tblsiopwhitelist.md">tblSiopWhiteList in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="af94d-155">Содержат зарегистрированные надстройки, которые можно связать с узлами.</span><span class="sxs-lookup"><span data-stu-id="af94d-155">Contains the registered Add-ins that can be associated with nodes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="af94d-156"><a href="lync-server-2013-tblenumattribute.md">tblEnumAttribute в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="af94d-156"><a href="lync-server-2013-tblenumattribute.md">tblEnumAttribute in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="af94d-157">Содержат только закодированные &quot; &quot; атрибуты видимости и &quot; поведения &quot; , используемые в таблице tblNode.</span><span class="sxs-lookup"><span data-stu-id="af94d-157">Contains only the hardcoded &quot;Visibility&quot; and &quot;Behavior&quot; attributes that are used in the tblNode table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="af94d-158"><a href="lync-server-2013-tblenumvalue.md">tblEnumValue в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="af94d-158"><a href="lync-server-2013-tblenumvalue.md">tblEnumValue in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="af94d-159">Содержат значения &quot; атрибутов поведения "и", &quot; которые используются в таблице tblNode.</span><span class="sxs-lookup"><span data-stu-id="af94d-159">Contains the values of the hardcoded &quot;Visibility” and “Behavior&quot; attributes that are used in the tblNode table.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="invites-chats-and-other-client-support"></a><span data-ttu-id="af94d-160">Приглашения, разговоры и другие службы поддержки клиентов</span><span class="sxs-lookup"><span data-stu-id="af94d-160">Invites, Chats, and Other Client Support</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="af94d-161">Таблица</span><span class="sxs-lookup"><span data-stu-id="af94d-161">Table</span></span></th>
<th><span data-ttu-id="af94d-162">Описание</span><span class="sxs-lookup"><span data-stu-id="af94d-162">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="af94d-163"><a href="lync-server-2013-tblprincipalinvites.md">tblPrincipalInvites в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="af94d-163"><a href="lync-server-2013-tblprincipalinvites.md">tblPrincipalInvites in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="af94d-164">Содержат приглашения для всех подготовленных пользователей в системе для всех узлов с включенным параметром "автоматическое приглашение".</span><span class="sxs-lookup"><span data-stu-id="af94d-164">Contains invites for all provisioned users in the system for all nodes with Auto Invite enabled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="af94d-165"><a href="lync-server-2013-tblchat.md">tblChat в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="af94d-165"><a href="lync-server-2013-tblchat.md">tblChat in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="af94d-166">Содержат все сообщения чата.</span><span class="sxs-lookup"><span data-stu-id="af94d-166">Contains all chat messages.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="af94d-167"><a href="lync-server-2013-tbllastinviteid.md">tblLastInviteId в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="af94d-167"><a href="lync-server-2013-tbllastinviteid.md">tblLastInviteId in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="af94d-168">Содержащий идентификатор последнего приглашения, который был создан (и использован в таблице tblPrincipalInvites) для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="af94d-168">Contains the last invite ID that was generated (and used in the tblPrincipalInvites table) for each user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="af94d-169"><a href="lync-server-2013-tbllastchatid.md">tblLastChatId в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="af94d-169"><a href="lync-server-2013-tbllastchatid.md">tblLastChatId in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="af94d-170">Содержащий последний идентификатор чата, который был создан (и использован в таблице tblChat) для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="af94d-170">Contains the last chat ID that was generated (and used in the tblChat table) for each user.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="af94d-171"><a href="lync-server-2013-tblpreference.md">tblPreference в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="af94d-171"><a href="lync-server-2013-tblpreference.md">tblPreference in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="af94d-172">Содержат пользовательские настройки клиента (используется только устаревшими клиентами).</span><span class="sxs-lookup"><span data-stu-id="af94d-172">Contains user client preferences (used by legacy clients only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="af94d-173"><a href="lync-server-2013-tblfiletoken.md">tblFileToken в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="af94d-173"><a href="lync-server-2013-tblfiletoken.md">tblFileToken in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="af94d-174">Содержат временные маркеры для целей передачи файлов.</span><span class="sxs-lookup"><span data-stu-id="af94d-174">Contains temporary tokens for file transfer purposes.</span></span> <span data-ttu-id="af94d-175">Каждый раз, когда файл отправляется или загружается, служба сохраняемого чата создает маркер, который используется клиентом для доступа к хранилищу файлов веб-служб.</span><span class="sxs-lookup"><span data-stu-id="af94d-175">Each time a file is uploaded or downloaded, the Persistent Chat service generates a token that the client uses to access the Web service file store.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="server-support"></a><span data-ttu-id="af94d-176">Поддержка сервера</span><span class="sxs-lookup"><span data-stu-id="af94d-176">Server Support</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="af94d-177">Таблица</span><span class="sxs-lookup"><span data-stu-id="af94d-177">Table</span></span></th>
<th><span data-ttu-id="af94d-178">Описание</span><span class="sxs-lookup"><span data-stu-id="af94d-178">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="af94d-179"><a href="lync-server-2013-tblserveridentity.md">tblServerIdentity в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="af94d-179"><a href="lync-server-2013-tblserveridentity.md">tblServerIdentity in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="af94d-180">Включает активные серверы в пуле сервера сохраняемого чата.</span><span class="sxs-lookup"><span data-stu-id="af94d-180">Contains the active servers in the Persistent Chat Server pool.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="af94d-181"><a href="lync-server-2013-tbladminlock.md">tblAdminLock в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="af94d-181"><a href="lync-server-2013-tbladminlock.md">tblAdminLock in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="af94d-182">Включает блокировку администратора для выполнения некоторых команд администратора.</span><span class="sxs-lookup"><span data-stu-id="af94d-182">Contains the administrator lock to run some administrator commands.</span></span> <span data-ttu-id="af94d-183">При каждом выпуске блокировки в таблице tblSystemRevision увеличивается запись о редакции системы.</span><span class="sxs-lookup"><span data-stu-id="af94d-183">The system revision entry in the tblSystemRevision table is incremented after each release of the lock.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="af94d-184"><a href="lync-server-2013-tblsystemrevision.md">tblSystemRevision в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="af94d-184"><a href="lync-server-2013-tblsystemrevision.md">tblSystemRevision in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="af94d-185">Включает номер редакции (вместе с таблицей tblAdminLock) для достижения согласованности на нескольких серверах.</span><span class="sxs-lookup"><span data-stu-id="af94d-185">Contains the revision number entry used (along with the tblAdminLock table) for achieving consistency across multiple servers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="af94d-186"><a href="lync-server-2013-tblactivepeers.md">tblActivePeers в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="af94d-186"><a href="lync-server-2013-tblactivepeers.md">tblActivePeers in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="af94d-187">В этом поле содержатся текущие одноранговые соединения между службами сохраняемого чата.</span><span class="sxs-lookup"><span data-stu-id="af94d-187">Contains current peer-to-peer connections between Persistent Chat services.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="af94d-188"><a href="lync-server-2013-tblconfig.md">tblConfig в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="af94d-188"><a href="lync-server-2013-tblconfig.md">tblConfig in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="af94d-189">Неподдерживаемая конфигурация сервера сохраняемого чата.</span><span class="sxs-lookup"><span data-stu-id="af94d-189">Contains the Persistent Chat Server unsupported configuration.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="af94d-190">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="af94d-190">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

