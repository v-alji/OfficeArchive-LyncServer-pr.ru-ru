---
title: 'Lync Server 2013: tblLastChatId'
description: 'Lync Server 2013: tblLastChatId.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblLastChatId
ms:assetid: 17a4ffbe-cca9-4ec5-ae46-38a15274889a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558616(v=OCS.15)
ms:contentKeyID: 48183513
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 69e80a735e70c8a03441038f5e58eb93e0af1f82
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444429"
---
# <a name="tbllastchatid-in-lync-server-2013"></a><span data-ttu-id="cfcc4-103">tblLastChatId в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cfcc4-103">tblLastChatId in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cfcc4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cfcc4-104">

<span> </span></span></span>

<span data-ttu-id="cfcc4-105">_**Тема последнего изменения:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="cfcc4-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="cfcc4-106">tblLastChatId включает последний идентификатор чата, который был создан (и использован в таблице tblChat) для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="cfcc4-106">tblLastChatId contains the last chat ID that was generated (and used in the tblChat table) for each user.</span></span>

### <a name="columns"></a><span data-ttu-id="cfcc4-107">Столбцов</span><span class="sxs-lookup"><span data-stu-id="cfcc4-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cfcc4-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="cfcc4-108">Column</span></span></th>
<th><span data-ttu-id="cfcc4-109">Тип</span><span class="sxs-lookup"><span data-stu-id="cfcc4-109">Type</span></span></th>
<th><span data-ttu-id="cfcc4-110">Описание</span><span class="sxs-lookup"><span data-stu-id="cfcc4-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cfcc4-111">nodeID</span><span class="sxs-lookup"><span data-stu-id="cfcc4-111">nodeID</span></span></p></td>
<td><p><span data-ttu-id="cfcc4-112">int, NOT NULL</span><span class="sxs-lookup"><span data-stu-id="cfcc4-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="cfcc4-113">Идентификатор узла (комната чата — только тип).</span><span class="sxs-lookup"><span data-stu-id="cfcc4-113">Node ID (chat room-type only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cfcc4-114">lastChatID</span><span class="sxs-lookup"><span data-stu-id="cfcc4-114">lastChatID</span></span></p></td>
<td><p><span data-ttu-id="cfcc4-115">bigint, NOT NULL</span><span class="sxs-lookup"><span data-stu-id="cfcc4-115">bigint, not null</span></span></p></td>
<td><p><span data-ttu-id="cfcc4-116">НОМЕР последнего использованного чата.</span><span class="sxs-lookup"><span data-stu-id="cfcc4-116">Last used chat ID.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="cfcc4-117">Параметры</span><span class="sxs-lookup"><span data-stu-id="cfcc4-117">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cfcc4-118">Столбец</span><span class="sxs-lookup"><span data-stu-id="cfcc4-118">Column</span></span></th>
<th><span data-ttu-id="cfcc4-119">Описание</span><span class="sxs-lookup"><span data-stu-id="cfcc4-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cfcc4-120">&lt;nodeID, lastChatID&gt;</span><span class="sxs-lookup"><span data-stu-id="cfcc4-120">&lt;nodeID, lastChatID&gt;</span></span></p></td>
<td><p><span data-ttu-id="cfcc4-121">Первичный ключ (для обработки достаточно просто nodeID).</span><span class="sxs-lookup"><span data-stu-id="cfcc4-121">Primary key (just nodeID is sufficient for processing).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cfcc4-122">nodeID</span><span class="sxs-lookup"><span data-stu-id="cfcc4-122">nodeID</span></span></p></td>
<td><p><span data-ttu-id="cfcc4-123">Внешний ключ с подстановкой в таблице tblNode. nodeID.</span><span class="sxs-lookup"><span data-stu-id="cfcc4-123">Foreign key with lookup in tblNode.nodeID table.</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="see-also"></a><span data-ttu-id="cfcc4-124">См. также</span><span class="sxs-lookup"><span data-stu-id="cfcc4-124">See Also</span></span>


[<span data-ttu-id="cfcc4-125">tblChat в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cfcc4-125">tblChat in Lync Server 2013</span></span>](lync-server-2013-tblchat.md)  
  

<span data-ttu-id="cfcc4-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cfcc4-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

