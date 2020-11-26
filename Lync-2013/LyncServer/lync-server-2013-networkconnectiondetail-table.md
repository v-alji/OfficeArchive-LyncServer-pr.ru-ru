---
title: 'Lync Server 2013: таблица NetworkConnectionDetail'
description: 'Таблица Lync Server 2013: NetworkConnectionDetail.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: NetworkConnectionDetail table
ms:assetid: b48cc9a6-5232-48b5-bd20-53b68229336b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205185(v=OCS.15)
ms:contentKeyID: 48185170
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dcd0f429999b6629826a9f9369d154afe3c1af2f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445493"
---
# <a name="networkconnectiondetail-table-in-lync-server-2013"></a><span data-ttu-id="f7d91-103">Таблица NetworkConnectionDetail в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f7d91-103">NetworkConnectionDetail table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f7d91-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f7d91-104">

<span> </span></span></span>

<span data-ttu-id="f7d91-105">_**Тема последнего изменения:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="f7d91-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="f7d91-106">Таблица NetworkConnectionDetail сопоставляет типы сетевых подключений с идентификаторами сетевых подключений, используемыми в базе данных качества обслуживания.</span><span class="sxs-lookup"><span data-stu-id="f7d91-106">The NetworkConnectionDetail table maps network connection types to the network connection identifiers used elsewhere in the Quality of Experience database.</span></span> <span data-ttu-id="f7d91-107">Эта таблица введена в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f7d91-107">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f7d91-108"><strong>Столбец</strong></span><span class="sxs-lookup"><span data-stu-id="f7d91-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="f7d91-109"><strong>Тип данных</strong></span><span class="sxs-lookup"><span data-stu-id="f7d91-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="f7d91-110"><strong>Ключ/индекс</strong></span><span class="sxs-lookup"><span data-stu-id="f7d91-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="f7d91-111"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="f7d91-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f7d91-112"><strong>NetworkConnectionDetailKey</strong></span><span class="sxs-lookup"><span data-stu-id="f7d91-112"><strong>NetworkConnectionDetailKey</strong></span></span></p></td>
<td><p><span data-ttu-id="f7d91-113">tinyint</span><span class="sxs-lookup"><span data-stu-id="f7d91-113">tinyint</span></span></p></td>
<td><p><span data-ttu-id="f7d91-114">Primary</span><span class="sxs-lookup"><span data-stu-id="f7d91-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="f7d91-115">Уникальный идентификатор типа сетевого подключения.</span><span class="sxs-lookup"><span data-stu-id="f7d91-115">Unique identifier for the network connection type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f7d91-116"><strong>NetworkConnectionDetail</strong></span><span class="sxs-lookup"><span data-stu-id="f7d91-116"><strong>NetworkConnectionDetail</strong></span></span></p></td>
<td><p><span data-ttu-id="f7d91-117">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="f7d91-117">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="f7d91-118">Повторя</span><span class="sxs-lookup"><span data-stu-id="f7d91-118">Unique</span></span></p></td>
<td><p><span data-ttu-id="f7d91-119">Тип сетевого подключения, соответствующий NetworkConnectionDetailKey.</span><span class="sxs-lookup"><span data-stu-id="f7d91-119">Network connection type that corresponds to the NetworkConnectionDetailKey.</span></span> <span data-ttu-id="f7d91-120">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="f7d91-120">Allowed values are:</span></span></p>
<ol>
<li><p><span data-ttu-id="f7d91-121">0--проводное подключение</span><span class="sxs-lookup"><span data-stu-id="f7d91-121">0 -- Wired</span></span></p></li>
<li><p><span data-ttu-id="f7d91-122">1--WiFi</span><span class="sxs-lookup"><span data-stu-id="f7d91-122">1 -- WiFi</span></span></p></li>
<li><p><span data-ttu-id="f7d91-123">2--Ethernet</span><span class="sxs-lookup"><span data-stu-id="f7d91-123">2 -- Ethernet</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table><span data-ttu-id="f7d91-124">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f7d91-124">


</div>

<span> </span>

</div>

</div>

</span></span></div>

