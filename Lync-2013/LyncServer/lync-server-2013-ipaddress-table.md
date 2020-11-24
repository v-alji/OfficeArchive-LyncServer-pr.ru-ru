---
title: 'Таблица в Lync Server 2013: IP-адрес'
description: 'Таблица Lync Server 2013: IPAddress.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: IPAddress table
ms:assetid: 8ec018b9-158e-4bbe-ad46-869e60315555
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205077(v=OCS.15)
ms:contentKeyID: 48184771
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6d987281fc310a3a179fa99f2aae51b0764349dd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399250"
---
# <a name="ipaddress-table-in-lync-server-2013"></a><span data-ttu-id="6da7c-103">Таблица IP-адреса в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6da7c-103">IPAddress table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6da7c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6da7c-104">

<span> </span></span></span>

<span data-ttu-id="6da7c-105">_**Тема последнего изменения:** 2012-10-17_</span><span class="sxs-lookup"><span data-stu-id="6da7c-105">_**Topic Last Modified:** 2012-10-17_</span></span>

<span data-ttu-id="6da7c-106">В таблице IPAddress IP-адреса сопоставляются с уникальными идентификаторами IP-адресов, которые используются в базе данных качества обслуживания.</span><span class="sxs-lookup"><span data-stu-id="6da7c-106">The IPAddress table maps IP addresses to the unique IP address identifiers used elsewhere in the Quality of Experience database.</span></span> <span data-ttu-id="6da7c-107">Эта таблица введена в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6da7c-107">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6da7c-108"><strong>Столбец</strong></span><span class="sxs-lookup"><span data-stu-id="6da7c-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="6da7c-109"><strong>Тип данных</strong></span><span class="sxs-lookup"><span data-stu-id="6da7c-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="6da7c-110"><strong>Ключ/индекс</strong></span><span class="sxs-lookup"><span data-stu-id="6da7c-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="6da7c-111"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="6da7c-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6da7c-112"><strong>IPAddressKey</strong></span><span class="sxs-lookup"><span data-stu-id="6da7c-112"><strong>IPAddressKey</strong></span></span></p></td>
<td><p><span data-ttu-id="6da7c-113">целое</span><span class="sxs-lookup"><span data-stu-id="6da7c-113">int</span></span></p></td>
<td><p><span data-ttu-id="6da7c-114">Primary</span><span class="sxs-lookup"><span data-stu-id="6da7c-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="6da7c-115">Уникальный идентификатор указанного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="6da7c-115">Unique identifier for the specified IP address.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6da7c-116"><strong>IPAddress</strong></span><span class="sxs-lookup"><span data-stu-id="6da7c-116"><strong>IPAddress</strong></span></span></p></td>
<td><p><span data-ttu-id="6da7c-117">varchar(50)</span><span class="sxs-lookup"><span data-stu-id="6da7c-117">varchar(50)</span></span></p></td>
<td><p><span data-ttu-id="6da7c-118">Повторя</span><span class="sxs-lookup"><span data-stu-id="6da7c-118">Unique</span></span></p></td>
<td><p><span data-ttu-id="6da7c-119">Уникальный IP-адрес (например, 189.168.1.1), сопоставляемый с IpAddressKey.</span><span class="sxs-lookup"><span data-stu-id="6da7c-119">Unique IP address (for example, 189.168.1.1) that maps to the IpAddressKey.</span></span> <span data-ttu-id="6da7c-120">Это может быть либо IPv4, либо IPv6-адрес.</span><span class="sxs-lookup"><span data-stu-id="6da7c-120">This may be either an IPv4 or an IPv6 address.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="6da7c-121">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6da7c-121">


</div>

<span> </span>

</div>

</div>

</span></span></div>

