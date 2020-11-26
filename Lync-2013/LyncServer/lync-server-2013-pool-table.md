---
title: 'Lync Server 2013: таблица Pool'
description: 'Таблица пула Lync Server 2013: пул.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Pool table
ms:assetid: 92ded8fd-d0ad-4f8a-9e6f-2e8a690fda3a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398746(v=OCS.15)
ms:contentKeyID: 48184803
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 559244d37580070e7930a163eaddcc748eb2172c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442861"
---
# <a name="pool-table-in-lync-server-2013"></a><span data-ttu-id="1120d-103">Таблица Pool в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1120d-103">Pool table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1120d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1120d-104">

<span> </span></span></span>

<span data-ttu-id="1120d-105">_**Тема последнего изменения:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="1120d-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="1120d-106">Таблица Pool — это вспомогательная таблица, в которой хранятся сведения о различных пулах интерфейсов переднего плана.</span><span class="sxs-lookup"><span data-stu-id="1120d-106">The Pool table is a supporting table that stores information about the various Front End pools.</span></span> <span data-ttu-id="1120d-107">Каждая запись в таблице представляет один пул.</span><span class="sxs-lookup"><span data-stu-id="1120d-107">Each record in the table represents one pool.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1120d-108"><strong>Столбец</strong></span><span class="sxs-lookup"><span data-stu-id="1120d-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="1120d-109"><strong>Тип данных</strong></span><span class="sxs-lookup"><span data-stu-id="1120d-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="1120d-110"><strong>Ключ/индекс</strong></span><span class="sxs-lookup"><span data-stu-id="1120d-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="1120d-111"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="1120d-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1120d-112"><strong>PoolKey</strong></span><span class="sxs-lookup"><span data-stu-id="1120d-112"><strong>PoolKey</strong></span></span></p></td>
<td><p><span data-ttu-id="1120d-113">целое</span><span class="sxs-lookup"><span data-stu-id="1120d-113">int</span></span></p></td>
<td><p><span data-ttu-id="1120d-114">Primary</span><span class="sxs-lookup"><span data-stu-id="1120d-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="1120d-115">Уникальный номер, идентифицирующий этот пул.</span><span class="sxs-lookup"><span data-stu-id="1120d-115">Unique number identifying this pool.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1120d-116"><strong>PoolName</strong></span><span class="sxs-lookup"><span data-stu-id="1120d-116"><strong>PoolName</strong></span></span></p></td>
<td><p><span data-ttu-id="1120d-117">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="1120d-117">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="1120d-118">Повторя</span><span class="sxs-lookup"><span data-stu-id="1120d-118">Unique</span></span> </p></td>
<td><p><span data-ttu-id="1120d-119">Полное доменное имя пула.</span><span class="sxs-lookup"><span data-stu-id="1120d-119">Pool FQDN.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="1120d-120">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1120d-120">


</div>

<span> </span>

</div>

</div>

</span></span></div>

