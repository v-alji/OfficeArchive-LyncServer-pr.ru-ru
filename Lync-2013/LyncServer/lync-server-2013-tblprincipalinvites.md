---
title: 'Lync Server 2013: tblPrincipalInvites'
description: 'Lync Server 2013: tblPrincipalInvites.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblPrincipalInvites
ms:assetid: 548ec156-4d1a-469d-a804-62cff226e5c2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558650(v=OCS.15)
ms:contentKeyID: 48184141
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d30d741864ed2a3cfbec8329215be33c21b3b262
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423507"
---
# <a name="tblprincipalinvites-in-lync-server-2013"></a><span data-ttu-id="72a55-103">tblPrincipalInvites в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="72a55-103">tblPrincipalInvites in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="72a55-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="72a55-104">

<span> </span></span></span>

<span data-ttu-id="72a55-105">_**Тема последнего изменения:** 2012-06-25_</span><span class="sxs-lookup"><span data-stu-id="72a55-105">_**Topic Last Modified:** 2012-06-25_</span></span>

<span data-ttu-id="72a55-106">tblPrincipalInvites включает приглашения для всех подготовленных пользователей для всех узлов с автоматическим приглашением.</span><span class="sxs-lookup"><span data-stu-id="72a55-106">tblPrincipalInvites contains invitations for all provisioned users for all nodes with auto-invite on.</span></span>

### <a name="columns"></a><span data-ttu-id="72a55-107">Столбцов</span><span class="sxs-lookup"><span data-stu-id="72a55-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="72a55-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="72a55-108">Column</span></span></th>
<th><span data-ttu-id="72a55-109">Тип</span><span class="sxs-lookup"><span data-stu-id="72a55-109">Type</span></span></th>
<th><span data-ttu-id="72a55-110">Описание</span><span class="sxs-lookup"><span data-stu-id="72a55-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="72a55-111">prinID</span><span class="sxs-lookup"><span data-stu-id="72a55-111">prinID</span></span></p></td>
<td><p><span data-ttu-id="72a55-112">int, NOT NULL</span><span class="sxs-lookup"><span data-stu-id="72a55-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="72a55-113">Идентификатор участника.</span><span class="sxs-lookup"><span data-stu-id="72a55-113">Principal ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72a55-114">invID</span><span class="sxs-lookup"><span data-stu-id="72a55-114">invID</span></span></p></td>
<td><p><span data-ttu-id="72a55-115">int, NOT NULL</span><span class="sxs-lookup"><span data-stu-id="72a55-115">int, not null</span></span></p></td>
<td><p><span data-ttu-id="72a55-116">Уникальный последовательный номер (для идентификатора участника), сформированный из таблицы tblLastInviteId.</span><span class="sxs-lookup"><span data-stu-id="72a55-116">Unique sequential number (per principal ID) generated from tblLastInviteId table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72a55-117">nodeID</span><span class="sxs-lookup"><span data-stu-id="72a55-117">nodeID</span></span></p></td>
<td><p><span data-ttu-id="72a55-118">int, NOT NULL</span><span class="sxs-lookup"><span data-stu-id="72a55-118">int, not null</span></span></p></td>
<td><p><span data-ttu-id="72a55-119">Идентификатор узла (только для комнаты чата).</span><span class="sxs-lookup"><span data-stu-id="72a55-119">Node ID (chat room only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72a55-120">createdOn</span><span class="sxs-lookup"><span data-stu-id="72a55-120">createdOn</span></span></p></td>
<td><p><span data-ttu-id="72a55-121">DateTime, NOT NULL</span><span class="sxs-lookup"><span data-stu-id="72a55-121">datetime, not null</span></span></p></td>
<td><p><span data-ttu-id="72a55-122">Время создания.</span><span class="sxs-lookup"><span data-stu-id="72a55-122">Time of creation.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="72a55-123">Параметры</span><span class="sxs-lookup"><span data-stu-id="72a55-123">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="72a55-124">Столбец</span><span class="sxs-lookup"><span data-stu-id="72a55-124">Column</span></span></th>
<th><span data-ttu-id="72a55-125">Описание</span><span class="sxs-lookup"><span data-stu-id="72a55-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="72a55-126">&lt;prinID, nodeID&gt;</span><span class="sxs-lookup"><span data-stu-id="72a55-126">&lt;prinID, nodeID&gt;</span></span></p></td>
<td><p><span data-ttu-id="72a55-127">Первичный ключ.</span><span class="sxs-lookup"><span data-stu-id="72a55-127">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72a55-128">prinID</span><span class="sxs-lookup"><span data-stu-id="72a55-128">prinID</span></span></p></td>
<td><p><span data-ttu-id="72a55-129">Внешний ключ с подстановкой в таблице tblPrincipal. prinID.</span><span class="sxs-lookup"><span data-stu-id="72a55-129">Foreign key with lookup in tblPrincipal.prinID table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72a55-130">nodeID</span><span class="sxs-lookup"><span data-stu-id="72a55-130">nodeID</span></span></p></td>
<td><p><span data-ttu-id="72a55-131">Внешний ключ с подстановкой в таблице tblNode. nodeID.</span><span class="sxs-lookup"><span data-stu-id="72a55-131">Foreign key with lookup in tblNode.nodeID table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="72a55-132">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="72a55-132">


</div>

<span> </span>

</div>

</div>

</span></span></div>

