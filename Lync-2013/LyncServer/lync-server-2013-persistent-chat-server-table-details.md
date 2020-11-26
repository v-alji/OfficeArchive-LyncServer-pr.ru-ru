---
title: 'Lync Server 2013: данные таблицы сервера сохраняемого чата'
description: 'Lync Server 2013: сведения о таблице сохраняемого сервера чата.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Persistent Chat Server table details
ms:assetid: c22d4a76-da50-49de-9038-e0ed7b8e1b58
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615034(v=OCS.15)
ms:contentKeyID: 48185323
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6a27feaaccf861d537127f06920cf903be5ae000
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443085"
---
# <a name="persistent-chat-server-table-details-in-lync-server-2013"></a><span data-ttu-id="c43a2-103">Данные таблицы сервера сохраняемого чата в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c43a2-103">Persistent Chat Server table details in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c43a2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c43a2-104">

<span> </span></span></span>

<span data-ttu-id="c43a2-105">_**Тема последнего изменения:** 2012-06-25_</span><span class="sxs-lookup"><span data-stu-id="c43a2-105">_**Topic Last Modified:** 2012-06-25_</span></span>

<span data-ttu-id="c43a2-106">В следующих разделах приведены сведения о столбцах в каждой из таблиц схемы базы данных "сохраняемый чат".</span><span class="sxs-lookup"><span data-stu-id="c43a2-106">The following topics detail the columns in each of the Persistent Chat database schema tables.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="c43a2-107">Содержание</span><span class="sxs-lookup"><span data-stu-id="c43a2-107">In This Section</span></span>

  - [<span data-ttu-id="c43a2-108">tblADCookie в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c43a2-108">tblADCookie in Lync Server 2013</span></span>](lync-server-2013-tbladcookie.md)

  - [<span data-ttu-id="c43a2-109">tblPrincipalMemberDifference в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c43a2-109">tblPrincipalMemberDifference in Lync Server 2013</span></span>](lync-server-2013-tblprincipalmemberdifference.md)

  - [<span data-ttu-id="c43a2-110">tblADUpdates в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c43a2-110">tblADUpdates in Lync Server 2013</span></span>](lync-server-2013-tbladupdates.md)

  - [<span data-ttu-id="c43a2-111">tblPrincipalMembers в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c43a2-111">tblPrincipalMembers in Lync Server 2013</span></span>](lync-server-2013-tblprincipalmembers.md)

  - [<span data-ttu-id="c43a2-112">tblPrincipalMeta в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c43a2-112">tblPrincipalMeta in Lync Server 2013</span></span>](lync-server-2013-tblprincipalmeta.md)

  - [<span data-ttu-id="c43a2-113">tblSkippedAffiliations в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c43a2-113">tblSkippedAffiliations in Lync Server 2013</span></span>](lync-server-2013-tblskippedaffiliations.md)

  - [<span data-ttu-id="c43a2-114">tblPrincipalType в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c43a2-114">tblPrincipalType in Lync Server 2013</span></span>](lync-server-2013-tblprincipaltype.md)

  - [<span data-ttu-id="c43a2-115">tblPrincipal в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c43a2-115">tblPrincipal in Lync Server 2013</span></span>](lync-server-2013-tblprincipal.md)

  - [<span data-ttu-id="c43a2-116">tblPrincipalAffiliations в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c43a2-116">tblPrincipalAffiliations in Lync Server 2013</span></span>](lync-server-2013-tblprincipalaffiliations.md)

  - [<span data-ttu-id="c43a2-117">tblNode в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c43a2-117">tblNode in Lync Server 2013</span></span>](lync-server-2013-tblnode.md)

  - [<span data-ttu-id="c43a2-118">tblRoleType в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c43a2-118">tblRoleType in Lync Server 2013</span></span>](lync-server-2013-tblroletype.md)

  - [<span data-ttu-id="c43a2-119">tblScopePrincipal в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c43a2-119">tblScopePrincipal in Lync Server 2013</span></span>](lync-server-2013-tblscopeprincipal.md)

  - [<span data-ttu-id="c43a2-120">tblPrincipalRole в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c43a2-120">tblPrincipalRole in Lync Server 2013</span></span>](lync-server-2013-tblprincipalrole.md)

  - [<span data-ttu-id="c43a2-121">tblSiopWhiteList в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c43a2-121">tblSiopWhiteList in Lync Server 2013</span></span>](lync-server-2013-tblsiopwhitelist.md)

  - [<span data-ttu-id="c43a2-122">tblEnumAttribute в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c43a2-122">tblEnumAttribute in Lync Server 2013</span></span>](lync-server-2013-tblenumattribute.md)

  - [<span data-ttu-id="c43a2-123">tblEnumValue в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c43a2-123">tblEnumValue in Lync Server 2013</span></span>](lync-server-2013-tblenumvalue.md)

  - [<span data-ttu-id="c43a2-124">tblPrincipalInvites в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c43a2-124">tblPrincipalInvites in Lync Server 2013</span></span>](lync-server-2013-tblprincipalinvites.md)

  - [<span data-ttu-id="c43a2-125">tblChat в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c43a2-125">tblChat in Lync Server 2013</span></span>](lync-server-2013-tblchat.md)

  - [<span data-ttu-id="c43a2-126">tblLastInviteId в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c43a2-126">tblLastInviteId in Lync Server 2013</span></span>](lync-server-2013-tbllastinviteid.md)

  - [<span data-ttu-id="c43a2-127">tblLastChatId в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c43a2-127">tblLastChatId in Lync Server 2013</span></span>](lync-server-2013-tbllastchatid.md)

  - [<span data-ttu-id="c43a2-128">tblPreference в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c43a2-128">tblPreference in Lync Server 2013</span></span>](lync-server-2013-tblpreference.md)

  - [<span data-ttu-id="c43a2-129">tblFileToken в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c43a2-129">tblFileToken in Lync Server 2013</span></span>](lync-server-2013-tblfiletoken.md)

  - [<span data-ttu-id="c43a2-130">tblServerIdentity в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c43a2-130">tblServerIdentity in Lync Server 2013</span></span>](lync-server-2013-tblserveridentity.md)

  - [<span data-ttu-id="c43a2-131">tblAdminLock в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c43a2-131">tblAdminLock in Lync Server 2013</span></span>](lync-server-2013-tbladminlock.md)

  - [<span data-ttu-id="c43a2-132">tblSystemRevision в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c43a2-132">tblSystemRevision in Lync Server 2013</span></span>](lync-server-2013-tblsystemrevision.md)

  - [<span data-ttu-id="c43a2-133">tblActivePeers в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c43a2-133">tblActivePeers in Lync Server 2013</span></span>](lync-server-2013-tblactivepeers.md)

  - [<span data-ttu-id="c43a2-134">tblConfig в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c43a2-134">tblConfig in Lync Server 2013</span></span>](lync-server-2013-tblconfig.md)

  - [<span data-ttu-id="c43a2-135">tblComplianceData в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c43a2-135">tblComplianceData in Lync Server 2013</span></span>](lync-server-2013-tblcompliancedata.md)

  - [<span data-ttu-id="c43a2-136">tblComplianceFanout в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c43a2-136">tblComplianceFanout in Lync Server 2013</span></span>](lync-server-2013-tblcompliancefanout.md)

  - [<span data-ttu-id="c43a2-137">tblComplianceParticipant в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c43a2-137">tblComplianceParticipant in Lync Server 2013</span></span>](lync-server-2013-tblcomplianceparticipant.md)

  - [<span data-ttu-id="c43a2-138">tblComplianceState в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c43a2-138">tblComplianceState in Lync Server 2013</span></span>](lync-server-2013-tblcompliancestate.md)

<span data-ttu-id="c43a2-139"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c43a2-139"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

