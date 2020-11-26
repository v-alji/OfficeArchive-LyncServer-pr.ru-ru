---
title: 'Lync Server 2013: список таблиц регистрации звонков'
description: 'Lync Server 2013: список таблиц CDR.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: List of CDR tables
ms:assetid: 031843fd-c7ff-4534-9b02-8847aad70807
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398084(v=OCS.15)
ms:contentKeyID: 48183254
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 21d0f683ffeb0f5f1cbba5db4c45d248aa14e8e4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426615"
---
# <a name="list-of-cdr-tables-in-lync-server-2013"></a><span data-ttu-id="e7495-103">Список таблиц регистрации звонков в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e7495-103">List of CDR tables in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e7495-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e7495-104">

<span> </span></span></span>

<span data-ttu-id="e7495-105">_**Тема последнего изменения:** 2012-10-18_</span><span class="sxs-lookup"><span data-stu-id="e7495-105">_**Topic Last Modified:** 2012-10-18_</span></span>

<span data-ttu-id="e7495-106">Схема базы данных для записи сведений о звонке (CDR) состоит из следующих таблиц.</span><span class="sxs-lookup"><span data-stu-id="e7495-106">The call detail recording (CDR) database schema consists of the following tables.</span></span>

<div>

## <a name="static-tables"></a><span data-ttu-id="e7495-107">Статические таблицы</span><span class="sxs-lookup"><span data-stu-id="e7495-107">Static Tables</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e7495-108">Таблица</span><span class="sxs-lookup"><span data-stu-id="e7495-108">Table</span></span></th>
<th><span data-ttu-id="e7495-109">Описание</span><span class="sxs-lookup"><span data-stu-id="e7495-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e7495-110"><a href="lync-server-2013-callpriorities-table.md">Таблица SessionCorrelation в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="e7495-110"><a href="lync-server-2013-callpriorities-table.md">CallPriorities table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="e7495-111">Хранит список возможных приоритетов звонков, например, экстренных, срочных, обычных, несрочных и т. д.</span><span class="sxs-lookup"><span data-stu-id="e7495-111">Stores the list of possible call priorities, such as emergency, urgent, normal, non-urgent, and more.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7495-112"><a href="lync-server-2013-conferencejointimethresholds-table.md">Таблица ConferenceJoinTimeThresholds в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="e7495-112"><a href="lync-server-2013-conferencejointimethresholds-table.md">ConferenceJoinTimeThresholds table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="e7495-113">Хранит границы классификации, используемые в сводном отчете "время присоединения к Конференции".</span><span class="sxs-lookup"><span data-stu-id="e7495-113">Stores the classification boundaries used by the Conference Join Time Summary Report.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7495-114"><a href="lync-server-2013-deregistertype-table.md">Таблица DeRegisterType в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="e7495-114"><a href="lync-server-2013-deregistertype-table.md">DeRegisterType table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="e7495-115">Хранит список возможных причин, по которым пользователь может отменить регистрацию, например &quot; инициирование клиента, &quot; &quot; истек срок регистрации, &quot; &quot; сбой клиента &quot; и многое другое.</span><span class="sxs-lookup"><span data-stu-id="e7495-115">Stores the list of possible user de-register reasons, such as &quot;client initiated,&quot; &quot;registration expired,&quot; &quot;client crash,&quot; and more.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7495-116"><a href="lync-server-2013-medialist-table.md">Таблица MediaList в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="e7495-116"><a href="lync-server-2013-medialist-table.md">MediaList table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="e7495-117">Хранит список типов мультимедиа, которые могут создавать записи в базе данных (например, мгновенные сообщения, звук, видео и передачу файлов).</span><span class="sxs-lookup"><span data-stu-id="e7495-117">Stores the list of media types that can generate entries in the database (for example, IM, audio, video, and file transfer).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7495-118"><a href="lync-server-2013-purgesettings-table.md">Таблица PurgeSettings в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="e7495-118"><a href="lync-server-2013-purgesettings-table.md">PurgeSettings table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="e7495-119">Хранит сведения о том, будут ли (и когда) устаревшие записи о вызовах автоматически удалены из базы данных CDR.</span><span class="sxs-lookup"><span data-stu-id="e7495-119">Stores information that specifies if (and when) outdated call detail records will automatically be deleted from the CDR database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7495-120"><a href="lync-server-2013-roles-table.md">Таблица Roles в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="e7495-120"><a href="lync-server-2013-roles-table.md">Roles table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="e7495-121">Хранит список возможных ролей конференции (например, участника и выступающего).</span><span class="sxs-lookup"><span data-stu-id="e7495-121">Stores the list of possible conference roles (for example, attendee and presenter).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7495-122"><a href="lync-server-2013-sipresponsemetadata-table.md">Таблица SIPResponseMetaData в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="e7495-122"><a href="lync-server-2013-sipresponsemetadata-table.md">SIPResponseMetaData table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="e7495-123">Содержит список кодов ответов SIP и классификацию и определение каждого из этих кодов.</span><span class="sxs-lookup"><span data-stu-id="e7495-123">Stores a list of SIP response codes and the classification and definition of each of those codes.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="supporting-tables"></a><span data-ttu-id="e7495-124">Вспомогательные таблицы</span><span class="sxs-lookup"><span data-stu-id="e7495-124">Supporting Tables</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e7495-125">Таблица</span><span class="sxs-lookup"><span data-stu-id="e7495-125">Table</span></span></th>
<th><span data-ttu-id="e7495-126">Описание</span><span class="sxs-lookup"><span data-stu-id="e7495-126">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e7495-127"><a href="lync-server-2013-clientversions-table.md">Таблица ClientVersions в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="e7495-127"><a href="lync-server-2013-clientversions-table.md">ClientVersions table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="e7495-128">Хранит клиентов (тип клиента и номер версии) каждого клиента, участвующего в вызове, с данными, захваченными в этой базе данных.</span><span class="sxs-lookup"><span data-stu-id="e7495-128">Stores the clients (both client type and version number) of each client involved in a call with information captured in this database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7495-129"><a href="lync-server-2013-conferenceuris-table.md">Таблица ConferenceUris в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="e7495-129"><a href="lync-server-2013-conferenceuris-table.md">ConferenceUris table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="e7495-130">Хранит список ConferenceURIs, используемых в звонках, связанных с Конференцией.</span><span class="sxs-lookup"><span data-stu-id="e7495-130">Stores a list of ConferenceURIs that are used in conference related calls.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7495-131"><a href="lync-server-2013-contenttypes-table.md">Таблица ContentTypes в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="e7495-131"><a href="lync-server-2013-contenttypes-table.md">ContentTypes table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="e7495-132">Хранит список типов контента SIP, которые используются в одноранговых звонках и конференц-связи.</span><span class="sxs-lookup"><span data-stu-id="e7495-132">Stores a list of Session Initiation Protocol (SIP) content types that are used in both peer-to-peer calls and conference calls.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7495-133"><a href="lync-server-2013-devices-table.md">Таблица Devices в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="e7495-133"><a href="lync-server-2013-devices-table.md">Devices table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="e7495-134">Хранит список устройств, в том числе изготовителя, аппаратную версию и MAC-адрес.</span><span class="sxs-lookup"><span data-stu-id="e7495-134">Stores a list of devices, including their manufacturer, hardware version, and MAC address.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7495-135"><a href="lync-server-2013-dialogs-table.md">Таблица Dialogs в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="e7495-135"><a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="e7495-136">Хранит сведения о коде диалогового окна для каждого сеанса в базе данных.</span><span class="sxs-lookup"><span data-stu-id="e7495-136">Stores information about the Dialog ID for each session in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7495-137"><a href="lync-server-2013-edgeservers-table.md">Таблица EdgeServers в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="e7495-137"><a href="lync-server-2013-edgeservers-table.md">EdgeServers table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="e7495-138">Хранит список пограничных серверов, которые используются при внешних звонках.</span><span class="sxs-lookup"><span data-stu-id="e7495-138">Stores a list of Edge Servers that are used for external calls.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7495-139"><a href="lync-server-2013-gateways-table.md">Таблица Gateways в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="e7495-139"><a href="lync-server-2013-gateways-table.md">Gateways table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="e7495-140">Хранит список шлюзов, используемых для звонков по протоколу голосовой связи через Интернет (VoIP).</span><span class="sxs-lookup"><span data-stu-id="e7495-140">Stores a list of Gateways that are used for Voice over Internet Protocol (VoIP) calls.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7495-141"><a href="lync-server-2013-hardwareversions-table.md">Таблица HardwareVersions в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="e7495-141"><a href="lync-server-2013-hardwareversions-table.md">HardwareVersions table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="e7495-142">Хранит список аппаратных версий устройств (стационарных телефонов).</span><span class="sxs-lookup"><span data-stu-id="e7495-142">Stores a list of hardware versions of devices (desk phone).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7495-143"><a href="lync-server-2013-manufacturers-table.md">Таблица Manufacturers в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="e7495-143"><a href="lync-server-2013-manufacturers-table.md">Manufacturers table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="e7495-144">Хранит список изготовителей устройств (стационарный телефон).</span><span class="sxs-lookup"><span data-stu-id="e7495-144">Stores a list of manufacturers of devices (desk phone).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7495-145"><a href="lync-server-2013-mcus-table.md">Таблица Mcus в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="e7495-145"><a href="lync-server-2013-mcus-table.md">Mcus table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="e7495-146">В этой папке хранятся сведения о различных серверах конференций/V и их URI.</span><span class="sxs-lookup"><span data-stu-id="e7495-146">Stores information about the various A/V Conferencing Servers and their URIs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7495-147"><a href="lync-server-2013-mediationservers-table.md">Таблица MediationServers в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="e7495-147"><a href="lync-server-2013-mediationservers-table.md">MediationServers table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="e7495-148">Хранит список серверов-посредников, используемых для звонков по протоколу VoIP.</span><span class="sxs-lookup"><span data-stu-id="e7495-148">Stores a list of Mediation Servers that are used for VoIP calls.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7495-149"><a href="lync-server-2013-phones-table.md">Таблица Phones в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="e7495-149"><a href="lync-server-2013-phones-table.md">Phones table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="e7495-150">Хранит все телефонные номера, используемые для звонков по протоколу VoIP, которые были заархивированы или в которых были записаны сведения о звонках.</span><span class="sxs-lookup"><span data-stu-id="e7495-150">Stores all the phone numbers used in VoIP calls that were archived or whose call details were recorded.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7495-151"><a href="lync-server-2013-pools-table.md">Таблица Pools в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="e7495-151"><a href="lync-server-2013-pools-table.md">Pools table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="e7495-152">Хранит имена групп, в которых регистрируются МГНОВЕНные сообщения.</span><span class="sxs-lookup"><span data-stu-id="e7495-152">Stores the names of the pool on which IM messages are captured.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7495-153"><a href="lync-server-2013-servers-table.md">Таблица Servers в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="e7495-153"><a href="lync-server-2013-servers-table.md">Servers table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="e7495-154">Хранит имена серверов, участвующих в звонках.</span><span class="sxs-lookup"><span data-stu-id="e7495-154">Stores the name of servers involved in calls.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7495-155"><a href="lync-server-2013-tenants-table.md">Таблица Tenants в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="e7495-155"><a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="e7495-156">Хранит клиентов, которые поддерживаются текущим развертыванием.</span><span class="sxs-lookup"><span data-stu-id="e7495-156">Stores the tenants supported by current deployment.</span></span> <span data-ttu-id="e7495-157">Некоторые клиентские сборки для корпоративных пользователей, федеративного пользователя, общего пользователя подключения к обмену мгновенными сообщениями и анонимные пользователи.</span><span class="sxs-lookup"><span data-stu-id="e7495-157">There some build-in tenants for Enterprise user, Federated User, public IM connectivity user, and Anonymous users.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7495-158"><a href="lync-server-2013-useragentdef-table.md">Таблица UserAgentDef в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="e7495-158"><a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="e7495-159">Сопоставляет идентификаторы агента пользователя с описательными именами агента.</span><span class="sxs-lookup"><span data-stu-id="e7495-159">Maps user agent identifiers to the agent’s descriptive names.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7495-160"><a href="lync-server-2013-users-table.md">Таблица Users в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="e7495-160"><a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="e7495-161">Хранит идентификаторы URI пользователей, которые участвовали в сеансах, записанных или архивированных в этой базе данных.</span><span class="sxs-lookup"><span data-stu-id="e7495-161">Stores the user URIs of users who have participated in sessions recorded or archived in this database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7495-162"><a href="lync-server-2013-userstatistics-table.md">Таблица UserStatistics в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="e7495-162"><a href="lync-server-2013-userstatistics-table.md">UserStatistics table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="e7495-163">Хранит сведения об использовании системы конкретным пользователем.</span><span class="sxs-lookup"><span data-stu-id="e7495-163">Stores information about an individual user’s usage of the system.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="tables-specific-to-conference-cdr-records"></a><span data-ttu-id="e7495-164">Таблицы, связанные с записями CDR конференций</span><span class="sxs-lookup"><span data-stu-id="e7495-164">Tables Specific to Conference CDR Records</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e7495-165">Таблица</span><span class="sxs-lookup"><span data-stu-id="e7495-165">Table</span></span></th>
<th><span data-ttu-id="e7495-166">Описание</span><span class="sxs-lookup"><span data-stu-id="e7495-166">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e7495-167"><a href="lync-server-2013-conferences-table.md">Таблица Conferences в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="e7495-167"><a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="e7495-168">Хранит сведения обо всех конференциях, которые были архивированы, а также о том, какие данные были записаны, включая ConferenceURI, время начала и окончания.</span><span class="sxs-lookup"><span data-stu-id="e7495-168">Stores information about all conferences that were archived or whose details were recorded, including ConferenceURI, and start and end time.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7495-169"><a href="lync-server-2013-conferencesessiondetails-table.md">Таблица ConferenceSessionDetails в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="e7495-169"><a href="lync-server-2013-conferencesessiondetails-table.md">ConferenceSessionDetails table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="e7495-170">В этой папке хранятся сведения о каждом сеансе конференции на базе SIP, в том числе время начала и окончания, идентификатор пользователя, код ответа и идентификатор диагностики для каждого сеанса.</span><span class="sxs-lookup"><span data-stu-id="e7495-170">Stores information about every SIP-based conference session, including start and end time, user ID, response code, and diagnostic ID for each session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7495-171"><a href="lync-server-2013-focusjoinsandleaves-table.md">Таблица FocusJoinsAndLeaves в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="e7495-171"><a href="lync-server-2013-focusjoinsandleaves-table.md">FocusJoinsAndLeaves table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="e7495-172">Хранит сведения о присоединениях и листьях конференций, в том числе о роли пользователей и клиентской версии.</span><span class="sxs-lookup"><span data-stu-id="e7495-172">Stores information about conference joins and leaves, including users’ role and client version.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7495-173"><a href="lync-server-2013-mcujoinsandleaves-table.md">Таблица McuJoinsAndLeaves в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="e7495-173"><a href="lync-server-2013-mcujoinsandleaves-table.md">McuJoinsAndLeaves table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="e7495-174">Хранит сведения о серверах конференций (A/V), вовлеченных в конференцию, а также присоединения и выхода пользователей.</span><span class="sxs-lookup"><span data-stu-id="e7495-174">Stores information about the A/V Conferencing Servers that are involved in a conference and the user join and leave times.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="tables-for-messages-in-im-conferences"></a><span data-ttu-id="e7495-175">Таблицы для сообщений в конференциях по обмену мгновенными сообщениями</span><span class="sxs-lookup"><span data-stu-id="e7495-175">Tables for Messages in IM Conferences</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e7495-176">Таблица</span><span class="sxs-lookup"><span data-stu-id="e7495-176">Table</span></span></th>
<th><span data-ttu-id="e7495-177">Описание</span><span class="sxs-lookup"><span data-stu-id="e7495-177">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e7495-178"><a href="lync-server-2013-conferencemessagecount-table.md">Таблица ConferenceMessageCount в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="e7495-178"><a href="lync-server-2013-conferencemessagecount-table.md">ConferenceMessageCount table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="e7495-179">Для каждой конференции с мгновенными сообщениями хранится количество сообщений, отправленных каждым пользователем.</span><span class="sxs-lookup"><span data-stu-id="e7495-179">For each IM conference, stores the number of messages that were sent by each user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7495-180"><a href="lync-server-2013-imreportsummary-table.md">Таблица IMReportSummary в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="e7495-180"><a href="lync-server-2013-imreportsummary-table.md">IMReportSummary table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="e7495-181">Общие сведения о сеансах обмена мгновенными сообщениями, проводимых в Организации.</span><span class="sxs-lookup"><span data-stu-id="e7495-181">Provides an overall report on the instant messaging sessions held in an organization.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="tables-for-peer-to-peer-sessions"></a><span data-ttu-id="e7495-182">Таблицы для одноранговых сеансов</span><span class="sxs-lookup"><span data-stu-id="e7495-182">Tables for Peer-to-Peer Sessions</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e7495-183">Таблица</span><span class="sxs-lookup"><span data-stu-id="e7495-183">Table</span></span></th>
<th><span data-ttu-id="e7495-184">Описание</span><span class="sxs-lookup"><span data-stu-id="e7495-184">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e7495-185"><a href="lync-server-2013-sessiondetails-table.md">Таблица SessionDetails в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="e7495-185"><a href="lync-server-2013-sessiondetails-table.md">SessionDetails table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="e7495-186">Хранит сведения обо всех одноранговых сеансах, в том числе время начала и окончания, идентификатор пользователя, код ответа и количество сообщений для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="e7495-186">Stores information about every peer-to-peer session, including start and end time, user ID, response code, and message count for each user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7495-187"><a href="lync-server-2013-filetransfers-table.md">Таблица FileTransfers в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="e7495-187"><a href="lync-server-2013-filetransfers-table.md">FileTransfers table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="e7495-188">Хранит сведения о сеансах передачи файлов, включая имя файла и результат (разрешено, отклонено или отменено).</span><span class="sxs-lookup"><span data-stu-id="e7495-188">Stores information about file transfer sessions, including file name and result (accepted, rejected, or canceled).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7495-189"><a href="lync-server-2013-media-table.md">Таблица Media в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="e7495-189"><a href="lync-server-2013-media-table.md">Media table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="e7495-190">Хранит сведения о различных типах носителей, участвующих в одноранговых сеансах.</span><span class="sxs-lookup"><span data-stu-id="e7495-190">Stores information about the different media types involved in peer-to-peer sessions.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="table-for-voip-call-details"></a><span data-ttu-id="e7495-191">Таблица сведений о звонке VoIP</span><span class="sxs-lookup"><span data-stu-id="e7495-191">Table for VoIP Call Details</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e7495-192">Таблица</span><span class="sxs-lookup"><span data-stu-id="e7495-192">Table</span></span></th>
<th><span data-ttu-id="e7495-193">Описание</span><span class="sxs-lookup"><span data-stu-id="e7495-193">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e7495-194"><a href="lync-server-2013-voipdetails-table.md">Таблица VoipDetails в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="e7495-194"><a href="lync-server-2013-voipdetails-table.md">VoipDetails table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="e7495-195">Для каждого из двух сторон VoIP/КТСОП звоните сведения о звонке, например номер телефона телефона VoIP, используемый шлюз, и какая сторона отключилась.</span><span class="sxs-lookup"><span data-stu-id="e7495-195">For each two-party VoIP/PSTN call, stores information about the call, such as the phone ID of VoIP phone, gateway used, and which party disconnected.</span></span> <span data-ttu-id="e7495-196">Ссылка на <a href="lync-server-2013-sessiondetails-table.md">таблицу SessionDetails в Lync Server 2013</a> для значений "начало/окончание" и "код ответа" для вызова.</span><span class="sxs-lookup"><span data-stu-id="e7495-196">Refers to the <a href="lync-server-2013-sessiondetails-table.md">SessionDetails table in Lync Server 2013</a> for call start/end times and response code.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="e7495-197">Если один из участников звонка является пользователем VoIP или на него вовлечен сервер-посредник, в этой таблице будет создана запись.</span><span class="sxs-lookup"><span data-stu-id="e7495-197">If one party on a call is a VoIP user or if a Mediation Server was involved in the call, a record will be created in this table.</span></span> <span data-ttu-id="e7495-198">Сведения о вызовах VoIP и VoIP, не посвященных коммутируемой телефонной сети общего пользования (PSTN), записываются в <A href="lync-server-2013-sessiondetails-table.md">таблицу SessionDetails в Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="e7495-198">Information about VoIP/VoIP calls not involving a public switched telephone network (PSTN) phone is captured in the <A href="lync-server-2013-sessiondetails-table.md">SessionDetails table in Lync Server 2013</A>.</span></span>


</div></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="table-for-e9-1-1-call-auditing"></a><span data-ttu-id="e7495-199">Таблица для аудита звонков E9-1-1</span><span class="sxs-lookup"><span data-stu-id="e7495-199">Table for E9-1-1 Call Auditing</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e7495-200">Таблица</span><span class="sxs-lookup"><span data-stu-id="e7495-200">Table</span></span></th>
<th><span data-ttu-id="e7495-201">Описание</span><span class="sxs-lookup"><span data-stu-id="e7495-201">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e7495-202"><a href="lync-server-2013-locations-table.md">Таблица Locations в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="e7495-202"><a href="lync-server-2013-locations-table.md">Locations table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="e7495-203">Для каждого вызова экстренной помощи, например улучшенного звонка в 9-1-1 (E9-1-1), можно хранить сведения о его местонахождении.</span><span class="sxs-lookup"><span data-stu-id="e7495-203">For each emergency call, such as an Enhanced 9-1-1 (E9-1-1) call, stores location information about the call.</span></span> <span data-ttu-id="e7495-204">Ссылка на <a href="lync-server-2013-sessiondetails-table.md">таблицу SessionDetails в Lync Server 2013</a> для значений "начало/окончание" и "код ответа" для вызова.</span><span class="sxs-lookup"><span data-stu-id="e7495-204">Refers to the <a href="lync-server-2013-sessiondetails-table.md">SessionDetails table in Lync Server 2013</a> for call start/end times and response code.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="e7495-205">Эта таблица включает большой двоичный объект Location для вызова E9-1-1.</span><span class="sxs-lookup"><span data-stu-id="e7495-205">This table only contains the location blob for the E9-1-1 call.</span></span> <span data-ttu-id="e7495-206">Ссылка на таблицу SessionDetails для получения более подробной информации о звонке.</span><span class="sxs-lookup"><span data-stu-id="e7495-206">Refers to the SessionDetails table for other detailed information about the call.</span></span>


</div></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="tables-for-troubleshooting"></a><span data-ttu-id="e7495-207">Таблицы для устранения неполадок</span><span class="sxs-lookup"><span data-stu-id="e7495-207">Tables for Troubleshooting</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e7495-208">Таблица</span><span class="sxs-lookup"><span data-stu-id="e7495-208">Table</span></span></th>
<th><span data-ttu-id="e7495-209">Описание</span><span class="sxs-lookup"><span data-stu-id="e7495-209">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e7495-210"><a href="lync-server-2013-application-table.md">Таблица Application в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="e7495-210"><a href="lync-server-2013-application-table.md">Application table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="e7495-211">В этой папке хранятся сведения о различных процессах в Lync Server 2013, которые используются в маршруте и соединениях.</span><span class="sxs-lookup"><span data-stu-id="e7495-211">Stores information about various processes within Lync Server 2013 that are involved in routing and connections.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7495-212"><a href="lync-server-2013-calltype-table.md">Таблица CallType в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="e7495-212"><a href="lync-server-2013-calltype-table.md">CallType table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="e7495-213">Хранит сведения о типах звонка, например "звук", "мгновенные сообщения", "звук и видео" и "общий доступ к приложениям".</span><span class="sxs-lookup"><span data-stu-id="e7495-213">Stores information about types of the call, such as, “audio”, “Instant Messaging”, “audio and video” and “application sharing”.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7495-214"><a href="lync-server-2013-errorcategory-table.md">Таблица ErrorCategory в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="e7495-214"><a href="lync-server-2013-errorcategory-table.md">ErrorCategory table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="e7495-215">Хранит понятное имя для каждого диагностического классификация Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e7495-215">Stores the friendly name for each Microsoft Lync Server 2013 diagnostic classification.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7495-216"><a href="lync-server-2013-errordef-table.md">Таблица ErrorDef в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="e7495-216"><a href="lync-server-2013-errordef-table.md">ErrorDef table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="e7495-217">Хранит сведения о типах ошибок и их определениях.</span><span class="sxs-lookup"><span data-stu-id="e7495-217">Stores information about types of errors and their definitions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7495-218"><a href="lync-server-2013-errorreport-table.md">Таблица ErrorReport в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="e7495-218"><a href="lync-server-2013-errorreport-table.md">ErrorReport table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="e7495-219">Хранит сведения о возникших ошибках.</span><span class="sxs-lookup"><span data-stu-id="e7495-219">Stores information about errors that have occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7495-220"><a href="lync-server-2013-progressreport-table.md">Таблица ProgressReport в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="e7495-220"><a href="lync-server-2013-progressreport-table.md">ProgressReport table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="e7495-221">Хранит сведения о ходе выполнения различных шагов, участвующих в процессах Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e7495-221">Stores information about the progress reports of various steps involved in Lync Server 2013 processes.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e7495-222">Таблицы, приведенные в следующем списке, используются для внутренних целей на сервере Lync Server.</span><span class="sxs-lookup"><span data-stu-id="e7495-222">The tables in the following list are used internally by Lync Server.</span></span> <span data-ttu-id="e7495-223">Эти сведения не описаны в настоящем документе.</span><span class="sxs-lookup"><span data-stu-id="e7495-223">Their details are not described in this document.</span></span>

</div>

<div>

## <a name="tables-for-internal-use-by-lync-server"></a><span data-ttu-id="e7495-224">Таблицы для внутреннего использования в Lync Server</span><span class="sxs-lookup"><span data-stu-id="e7495-224">Tables for Internal Use by Lync Server</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e7495-225">Таблица</span><span class="sxs-lookup"><span data-stu-id="e7495-225">Table</span></span></th>
<th><span data-ttu-id="e7495-226">Описание</span><span class="sxs-lookup"><span data-stu-id="e7495-226">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e7495-227"><strong>DbConfigDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="e7495-227"><strong>DbConfigDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="e7495-228">Только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="e7495-228">For internal use only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7495-229"><strong>DbConfigInt</strong></span><span class="sxs-lookup"><span data-stu-id="e7495-229"><strong>DbConfigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="e7495-230">Только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="e7495-230">For internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7495-231"><strong>DbErrorMessage</strong></span><span class="sxs-lookup"><span data-stu-id="e7495-231"><strong>DbErrorMessage</strong></span></span></p></td>
<td><p><span data-ttu-id="e7495-232">Только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="e7495-232">For internal use only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7495-233"><strong>Интерфейсная таблица</strong></span><span class="sxs-lookup"><span data-stu-id="e7495-233"><strong>FrontEnd Table</strong></span></span></p></td>
<td><p><span data-ttu-id="e7495-234">Только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="e7495-234">For internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7495-235"><strong>Таблица MSMQProcessing</strong></span><span class="sxs-lookup"><span data-stu-id="e7495-235"><strong>MSMQProcessing Table</strong></span></span></p></td>
<td><p><span data-ttu-id="e7495-236">Только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="e7495-236">For internal use only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7495-237"><strong>SummaryTableConfiguration</strong></span><span class="sxs-lookup"><span data-stu-id="e7495-237"><strong>SummaryTableConfiguration</strong></span></span></p></td>
<td><p><span data-ttu-id="e7495-238">Только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="e7495-238">For internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7495-239"><strong>Таблица "синдикации"</strong></span><span class="sxs-lookup"><span data-stu-id="e7495-239"><strong>Syndicators Table</strong></span></span></p></td>
<td><p><span data-ttu-id="e7495-240">Только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="e7495-240">For internal use only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7495-241"><strong>Таблица SyndicatorsTenantMap</strong></span><span class="sxs-lookup"><span data-stu-id="e7495-241"><strong>SyndicatorsTenantMap Table</strong></span></span></p></td>
<td><p><span data-ttu-id="e7495-242">Только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="e7495-242">For internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7495-243"><strong>Таблица задач</strong></span><span class="sxs-lookup"><span data-stu-id="e7495-243"><strong>Task Table</strong></span></span></p></td>
<td><p><span data-ttu-id="e7495-244">Только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="e7495-244">For internal use only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7495-245"><strong>UserStatistics</strong></span><span class="sxs-lookup"><span data-stu-id="e7495-245"><strong>UserStatistics</strong></span></span></p></td>
<td><p><span data-ttu-id="e7495-246">Только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="e7495-246">For internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7495-247"><strong>UsageSummary_UQ</strong></span><span class="sxs-lookup"><span data-stu-id="e7495-247"><strong>UsageSummary_UQ</strong></span></span></p></td>
<td><p><span data-ttu-id="e7495-248">Только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="e7495-248">For internal use only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7495-249"><strong>UsageSummary</strong></span><span class="sxs-lookup"><span data-stu-id="e7495-249"><strong>UsageSummary</strong></span></span></p></td>
<td><p><span data-ttu-id="e7495-250">Только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="e7495-250">For internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7495-251"><strong>DaylightSavingYears</strong></span><span class="sxs-lookup"><span data-stu-id="e7495-251"><strong>DaylightSavingYears</strong></span></span></p></td>
<td><p><span data-ttu-id="e7495-252">Только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="e7495-252">For internal use only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7495-253"><strong>TimeZoneConfiguration</strong></span><span class="sxs-lookup"><span data-stu-id="e7495-253"><strong>TimeZoneConfiguration</strong></span></span></p></td>
<td><p><span data-ttu-id="e7495-254">Только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="e7495-254">For internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7495-255"><strong>Часовых поясов</strong></span><span class="sxs-lookup"><span data-stu-id="e7495-255"><strong>TimeZones</strong></span></span></p></td>
<td><p><span data-ttu-id="e7495-256">Только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="e7495-256">For internal use only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7495-257"><strong>FailureSummary_UQ</strong></span><span class="sxs-lookup"><span data-stu-id="e7495-257"><strong>FailureSummary_UQ</strong></span></span></p></td>
<td><p><span data-ttu-id="e7495-258">Только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="e7495-258">For internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7495-259"><strong>FailureSummary</strong></span><span class="sxs-lookup"><span data-stu-id="e7495-259"><strong>FailureSummary</strong></span></span></p></td>
<td><p><span data-ttu-id="e7495-260">Только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="e7495-260">For internal use only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7495-261"><strong>ServerSummary</strong></span><span class="sxs-lookup"><span data-stu-id="e7495-261"><strong>ServerSummary</strong></span></span></p></td>
<td><p><span data-ttu-id="e7495-262">Только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="e7495-262">For internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7495-263"><strong>MsDiagMetaData</strong></span><span class="sxs-lookup"><span data-stu-id="e7495-263"><strong>MsDiagMetaData</strong></span></span></p></td>
<td><p><span data-ttu-id="e7495-264">Только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="e7495-264">For internal use only.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="e7495-265">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e7495-265">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

