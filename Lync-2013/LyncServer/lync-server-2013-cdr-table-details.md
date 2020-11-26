---
title: 'Lync Server 2013: сведения о таблице регистрации вызовов'
description: 'Lync Server 2013: сведения о таблицах CDR.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: CDR table details
ms:assetid: 896198f5-672b-48ea-852f-0211c0c90857
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398693(v=OCS.15)
ms:contentKeyID: 48184730
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 331a3dfd4ffccac2ac4a442eeb9ad9171defb41c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435483"
---
# <a name="cdr-table-details-in-lync-server-2013"></a><span data-ttu-id="fc8ac-103">Сведения о таблице регистрации вызовов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fc8ac-103">CDR table details in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fc8ac-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fc8ac-104">

<span> </span></span></span>

<span data-ttu-id="fc8ac-105">_**Тема последнего изменения:** 2012-10-18_</span><span class="sxs-lookup"><span data-stu-id="fc8ac-105">_**Topic Last Modified:** 2012-10-18_</span></span>

<span data-ttu-id="fc8ac-106">В следующих разделах описаны столбцы в каждой из таблиц схемы базы данных "сведения о звонке" (CDR).</span><span class="sxs-lookup"><span data-stu-id="fc8ac-106">The following topics detail the columns in each of the call detail records (CDR) database schema tables.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="fc8ac-107">Содержание</span><span class="sxs-lookup"><span data-stu-id="fc8ac-107">In This Section</span></span>

  - [<span data-ttu-id="fc8ac-108">Таблица Application в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fc8ac-108">Application table in Lync Server 2013</span></span>](lync-server-2013-application-table.md)

  - [<span data-ttu-id="fc8ac-109">Таблица SessionCorrelation в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fc8ac-109">CallPriorities table in Lync Server 2013</span></span>](lync-server-2013-callpriorities-table.md)

  - [<span data-ttu-id="fc8ac-110">Таблица CallType в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fc8ac-110">CallType table in Lync Server 2013</span></span>](lync-server-2013-calltype-table.md)

  - [<span data-ttu-id="fc8ac-111">Таблица ClientVersions в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fc8ac-111">ClientVersions table in Lync Server 2013</span></span>](lync-server-2013-clientversions-table.md)

  - [<span data-ttu-id="fc8ac-112">Таблица ConferenceJoinTimeThresholds в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fc8ac-112">ConferenceJoinTimeThresholds table in Lync Server 2013</span></span>](lync-server-2013-conferencejointimethresholds-table.md)

  - [<span data-ttu-id="fc8ac-113">Таблица ConferenceMessageCount в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fc8ac-113">ConferenceMessageCount table in Lync Server 2013</span></span>](lync-server-2013-conferencemessagecount-table.md)

  - [<span data-ttu-id="fc8ac-114">Таблица Conferences в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fc8ac-114">Conferences table in Lync Server 2013</span></span>](lync-server-2013-conferences-table.md)

  - [<span data-ttu-id="fc8ac-115">Таблица ConferenceSessionDetails в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fc8ac-115">ConferenceSessionDetails table in Lync Server 2013</span></span>](lync-server-2013-conferencesessiondetails-table.md)

  - [<span data-ttu-id="fc8ac-116">Таблица ConferenceUris в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fc8ac-116">ConferenceUris table in Lync Server 2013</span></span>](lync-server-2013-conferenceuris-table.md)

  - [<span data-ttu-id="fc8ac-117">Таблица ContentTypes в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fc8ac-117">ContentTypes table in Lync Server 2013</span></span>](lync-server-2013-contenttypes-table.md)

  - [<span data-ttu-id="fc8ac-118">Таблица DeRegisterType в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fc8ac-118">DeRegisterType table in Lync Server 2013</span></span>](lync-server-2013-deregistertype-table.md)

  - [<span data-ttu-id="fc8ac-119">Таблица Devices в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fc8ac-119">Devices table in Lync Server 2013</span></span>](lync-server-2013-devices-table.md)

  - [<span data-ttu-id="fc8ac-120">Таблица Dialogs в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fc8ac-120">Dialogs table in Lync Server 2013</span></span>](lync-server-2013-dialogs-table.md)

  - [<span data-ttu-id="fc8ac-121">Таблица EdgeServers в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fc8ac-121">EdgeServers table in Lync Server 2013</span></span>](lync-server-2013-edgeservers-table.md)

  - [<span data-ttu-id="fc8ac-122">Таблица ErrorCategory в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fc8ac-122">ErrorCategory table in Lync Server 2013</span></span>](lync-server-2013-errorcategory-table.md)

  - [<span data-ttu-id="fc8ac-123">Таблица ErrorDef в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fc8ac-123">ErrorDef table in Lync Server 2013</span></span>](lync-server-2013-errordef-table.md)

  - [<span data-ttu-id="fc8ac-124">Таблица ErrorReport в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fc8ac-124">ErrorReport table in Lync Server 2013</span></span>](lync-server-2013-errorreport-table.md)

  - [<span data-ttu-id="fc8ac-125">Таблица FileTransfers в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fc8ac-125">FileTransfers table in Lync Server 2013</span></span>](lync-server-2013-filetransfers-table.md)

  - [<span data-ttu-id="fc8ac-126">Таблица FocusJoinsAndLeaves в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fc8ac-126">FocusJoinsAndLeaves table in Lync Server 2013</span></span>](lync-server-2013-focusjoinsandleaves-table.md)

  - [<span data-ttu-id="fc8ac-127">Интерфейсная таблица в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fc8ac-127">FrontEnd table in Lync Server 2013</span></span>](lync-server-2013-frontend-table.md)

  - [<span data-ttu-id="fc8ac-128">Таблица Gateways в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fc8ac-128">Gateways table in Lync Server 2013</span></span>](lync-server-2013-gateways-table.md)

  - [<span data-ttu-id="fc8ac-129">Таблица HardwareVersions в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fc8ac-129">HardwareVersions table in Lync Server 2013</span></span>](lync-server-2013-hardwareversions-table.md)

  - [<span data-ttu-id="fc8ac-130">Таблица IMReportSummary в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fc8ac-130">IMReportSummary table in Lync Server 2013</span></span>](lync-server-2013-imreportsummary-table.md)

  - [<span data-ttu-id="fc8ac-131">Таблица Locations в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fc8ac-131">Locations table in Lync Server 2013</span></span>](lync-server-2013-locations-table.md)

  - [<span data-ttu-id="fc8ac-132">Таблица Manufacturers в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fc8ac-132">Manufacturers table in Lync Server 2013</span></span>](lync-server-2013-manufacturers-table.md)

  - [<span data-ttu-id="fc8ac-133">Таблица McuJoinsAndLeaves в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fc8ac-133">McuJoinsAndLeaves table in Lync Server 2013</span></span>](lync-server-2013-mcujoinsandleaves-table.md)

  - [<span data-ttu-id="fc8ac-134">Таблица Mcus в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fc8ac-134">Mcus table in Lync Server 2013</span></span>](lync-server-2013-mcus-table.md)

  - [<span data-ttu-id="fc8ac-135">Таблица Media в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fc8ac-135">Media table in Lync Server 2013</span></span>](lync-server-2013-media-table.md)

  - [<span data-ttu-id="fc8ac-136">Таблица MediaList в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fc8ac-136">MediaList table in Lync Server 2013</span></span>](lync-server-2013-medialist-table.md)

  - [<span data-ttu-id="fc8ac-137">Таблица MediationServers в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fc8ac-137">MediationServers table in Lync Server 2013</span></span>](lync-server-2013-mediationservers-table.md)

  - [<span data-ttu-id="fc8ac-138">Таблица MSMQProcessing в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fc8ac-138">MSMQProcessing table in Lync Server 2013</span></span>](lync-server-2013-msmqprocessing-table.md)

  - [<span data-ttu-id="fc8ac-139">Таблица Phones в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fc8ac-139">Phones table in Lync Server 2013</span></span>](lync-server-2013-phones-table.md)

  - [<span data-ttu-id="fc8ac-140">Таблица Pools в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fc8ac-140">Pools table in Lync Server 2013</span></span>](lync-server-2013-pools-table.md)

  - [<span data-ttu-id="fc8ac-141">Таблица ProgressReport в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fc8ac-141">ProgressReport table in Lync Server 2013</span></span>](lync-server-2013-progressreport-table.md)

  - [<span data-ttu-id="fc8ac-142">Таблица PurgeSettings в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fc8ac-142">PurgeSettings table in Lync Server 2013</span></span>](lync-server-2013-purgesettings-table.md)

  - [<span data-ttu-id="fc8ac-143">Таблица Registration в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fc8ac-143">Registration table in Lync Server 2013</span></span>](lync-server-2013-registration-table.md)

  - [<span data-ttu-id="fc8ac-144">Таблица Roles в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fc8ac-144">Roles table in Lync Server 2013</span></span>](lync-server-2013-roles-table.md)

  - [<span data-ttu-id="fc8ac-145">Таблица Servers в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fc8ac-145">Servers table in Lync Server 2013</span></span>](lync-server-2013-servers-table.md)

  - [<span data-ttu-id="fc8ac-146">Таблица SessionDetails в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fc8ac-146">SessionDetails table in Lync Server 2013</span></span>](lync-server-2013-sessiondetails-table.md)

  - [<span data-ttu-id="fc8ac-147">Таблица SIPResponseMetaData в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fc8ac-147">SIPResponseMetaData table in Lync Server 2013</span></span>](lync-server-2013-sipresponsemetadata-table.md)

  - [<span data-ttu-id="fc8ac-148">Таблица "синдикации" в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fc8ac-148">Syndicators table in Lync Server 2013</span></span>](lync-server-2013-syndicators-table.md)

  - [<span data-ttu-id="fc8ac-149">Таблица SyndicatorsTenantMap в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fc8ac-149">SyndicatorsTenantMap table in Lync Server 2013</span></span>](lync-server-2013-syndicatorstenantmap-table.md)

  - [<span data-ttu-id="fc8ac-150">Таблица задач в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fc8ac-150">Task table in Lync Server 2013</span></span>](lync-server-2013-task-table.md)

  - [<span data-ttu-id="fc8ac-151">Таблица Tenants в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fc8ac-151">Tenants table in Lync Server 2013</span></span>](lync-server-2013-tenants-table.md)

  - [<span data-ttu-id="fc8ac-152">Таблица UriTypes в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fc8ac-152">UriTypes table in Lync Server 2013</span></span>](lync-server-2013-uritypes-table.md)

  - [<span data-ttu-id="fc8ac-153">Таблица Users в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fc8ac-153">Users table in Lync Server 2013</span></span>](lync-server-2013-users-table.md)

  - [<span data-ttu-id="fc8ac-154">Таблица UserAgentDef в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fc8ac-154">UserAgentDef table in Lync Server 2013</span></span>](lync-server-2013-useragentdef-table.md)

  - [<span data-ttu-id="fc8ac-155">Таблица UserStatistics в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fc8ac-155">UserStatistics table in Lync Server 2013</span></span>](lync-server-2013-userstatistics-table.md)

  - [<span data-ttu-id="fc8ac-156">Таблица VoipDetails в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fc8ac-156">VoipDetails table in Lync Server 2013</span></span>](lync-server-2013-voipdetails-table.md)

<span data-ttu-id="fc8ac-157"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fc8ac-157"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

