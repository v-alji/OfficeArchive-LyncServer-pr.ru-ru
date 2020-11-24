---
title: 'Lync Server 2013: tblRoleType'
description: 'Lync Server 2013: tblRoleType.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblRoleType
ms:assetid: 1eac3a54-656a-40ac-b771-edfc64d6e34b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558623(v=OCS.15)
ms:contentKeyID: 48183577
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f458259acaee7821d5f6a7339b993c70fe65f595
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398077"
---
# <a name="tblroletype-in-lync-server-2013"></a><span data-ttu-id="a5500-103">tblRoleType в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a5500-103">tblRoleType in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a5500-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a5500-104">

<span> </span></span></span>

<span data-ttu-id="a5500-105">_**Тема последнего изменения:** 2012-06-25_</span><span class="sxs-lookup"><span data-stu-id="a5500-105">_**Topic Last Modified:** 2012-06-25_</span></span>

<span data-ttu-id="a5500-106">tblRoleType — это статическая таблица подстановки с типами ролей и связанными с ними наборами разрешений.</span><span class="sxs-lookup"><span data-stu-id="a5500-106">tblRoleType is a static lookup table with role types and their associated permission sets.</span></span>

### <a name="columns"></a><span data-ttu-id="a5500-107">Столбцов</span><span class="sxs-lookup"><span data-stu-id="a5500-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a5500-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="a5500-108">Column</span></span></th>
<th><span data-ttu-id="a5500-109">Тип</span><span class="sxs-lookup"><span data-stu-id="a5500-109">Type</span></span></th>
<th><span data-ttu-id="a5500-110">Описание</span><span class="sxs-lookup"><span data-stu-id="a5500-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a5500-111">rtypeID</span><span class="sxs-lookup"><span data-stu-id="a5500-111">rtypeID</span></span></p></td>
<td><p><span data-ttu-id="a5500-112">int, NOT NULL</span><span class="sxs-lookup"><span data-stu-id="a5500-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="a5500-113">Идентификатор типа роли.</span><span class="sxs-lookup"><span data-stu-id="a5500-113">Role type ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a5500-114">rtypeDesc</span><span class="sxs-lookup"><span data-stu-id="a5500-114">rtypeDesc</span></span></p></td>
<td><p><span data-ttu-id="a5500-115">nvarchar (256), NOT NULL</span><span class="sxs-lookup"><span data-stu-id="a5500-115">nvarchar (256), not null</span></span></p></td>
<td><p><span data-ttu-id="a5500-116">Описание типа роли.</span><span class="sxs-lookup"><span data-stu-id="a5500-116">Role type description.</span></span> <span data-ttu-id="a5500-117">Доступно четыре роли:</span><span class="sxs-lookup"><span data-stu-id="a5500-117">There are four available roles:</span></span></p>
<ul>
<li><p><span data-ttu-id="a5500-118">Член: участник комнаты чата</span><span class="sxs-lookup"><span data-stu-id="a5500-118">Member: Chat room member</span></span></p></li>
<li><p><span data-ttu-id="a5500-119">Руководитель: руководитель комнаты чата</span><span class="sxs-lookup"><span data-stu-id="a5500-119">Manager: Chat room manager</span></span></p></li>
<li><p><span data-ttu-id="a5500-120">Выставлено сообщение: выступающий для комнаты чата Auditorium</span><span class="sxs-lookup"><span data-stu-id="a5500-120">Voiced: Presenter for an auditorium chat room</span></span></p></li>
<li><p><span data-ttu-id="a5500-121">Создатель: может создавать комнаты чата</span><span class="sxs-lookup"><span data-stu-id="a5500-121">Creator: Can create chat rooms</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a5500-122">rtypeAllowedPermSet</span><span class="sxs-lookup"><span data-stu-id="a5500-122">rtypeAllowedPermSet</span></span></p></td>
<td><p><span data-ttu-id="a5500-123">bigint, NOT NULL</span><span class="sxs-lookup"><span data-stu-id="a5500-123">bigint, not null</span></span></p></td>
<td><p><span data-ttu-id="a5500-124">Наборы разрешений для роли.</span><span class="sxs-lookup"><span data-stu-id="a5500-124">Permission set for the role.</span></span> <span data-ttu-id="a5500-125">Используются следующие биты:</span><span class="sxs-lookup"><span data-stu-id="a5500-125">The used bits are:</span></span></p>
<ul>
<li><p><span data-ttu-id="a5500-126">2: значение true, если роль может управлять узлами.</span><span class="sxs-lookup"><span data-stu-id="a5500-126">2: True if the role can manage nodes.</span></span></p></li>
<li><p><span data-ttu-id="a5500-127">4: значение true, если роль может создавать дочерние узлы.</span><span class="sxs-lookup"><span data-stu-id="a5500-127">4: True if the role can create children nodes.</span></span></p></li>
<li><p><span data-ttu-id="a5500-128">7: значение true, если роль может присоединиться к комнате чата (или дочерним комнатам чатов для категории).</span><span class="sxs-lookup"><span data-stu-id="a5500-128">7: True if the role can join a chat room (or children chat rooms of a category).</span></span></p></li>
<li><p><span data-ttu-id="a5500-129">8: true, если роль может общаться в комнате чата (или в дочерних комнатах чата).</span><span class="sxs-lookup"><span data-stu-id="a5500-129">8: True if the role can chat in a chat room (or in children chat rooms of a category).</span></span></p></li>
<li><p><span data-ttu-id="a5500-130">10: true, если роль может читать историю чата, даже если она не присоединяется к комнате чата.</span><span class="sxs-lookup"><span data-stu-id="a5500-130">10: True if the role can read chat history even when not joined to a chat room.</span></span></p></li>
<li><p><span data-ttu-id="a5500-131">11: true, если роль может видеть комнату чата.</span><span class="sxs-lookup"><span data-stu-id="a5500-131">11: True if the role can see the chat room.</span></span> <span data-ttu-id="a5500-132">(Это улучшено с помощью таких факторов, как область видимости и видимость.)</span><span class="sxs-lookup"><span data-stu-id="a5500-132">(This is further refined by factors such as scope and visibility.)</span></span></p></li>
<li><p><span data-ttu-id="a5500-133">12: true, если роль может общаться в комнате чата Auditorium.</span><span class="sxs-lookup"><span data-stu-id="a5500-133">12: True if the role can chat in an auditorium chat room.</span></span></p></li>
<li><p><span data-ttu-id="a5500-134">13: true, если роль может обойти правила видимости при просмотре узлов.</span><span class="sxs-lookup"><span data-stu-id="a5500-134">13: True if the role can bypass visibility rules when viewing nodes.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


### <a name="key"></a><span data-ttu-id="a5500-135">Ключ</span><span class="sxs-lookup"><span data-stu-id="a5500-135">Key</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a5500-136">Столбец</span><span class="sxs-lookup"><span data-stu-id="a5500-136">Column</span></span></th>
<th><span data-ttu-id="a5500-137">Описание</span><span class="sxs-lookup"><span data-stu-id="a5500-137">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a5500-138">rtypeID</span><span class="sxs-lookup"><span data-stu-id="a5500-138">rtypeID</span></span></p></td>
<td><p><span data-ttu-id="a5500-139">Первичный ключ.</span><span class="sxs-lookup"><span data-stu-id="a5500-139">Primary key.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="a5500-140">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a5500-140">


</div>

<span> </span>

</div>

</div>

</span></span></div>

