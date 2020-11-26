---
title: 'Lync Server 2013: таблица Device'
description: 'Сервер Lync Server 2013: таблица устройств.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Device table
ms:assetid: d5a4f777-bc12-4ce8-bc0d-867d5e22b436
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398930(v=OCS.15)
ms:contentKeyID: 48185544
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 46de64a49eace52d62cbd6384fcae680b5c511b9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429414"
---
# <a name="device-table-in-lync-server-2013"></a><span data-ttu-id="b3f11-103">Таблица Device в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b3f11-103">Device table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b3f11-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b3f11-104">

<span> </span></span></span>

<span data-ttu-id="b3f11-105">_**Тема последнего изменения:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="b3f11-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="b3f11-106">Таблица Device является вспомогательной таблицей, в которой хранятся сведения о различных устройствах захвата или рендеринге.</span><span class="sxs-lookup"><span data-stu-id="b3f11-106">The Device table is a supporting table that stores information about the various capture or render devices.</span></span> <span data-ttu-id="b3f11-107">Каждая запись в таблице представляет одно устройство.</span><span class="sxs-lookup"><span data-stu-id="b3f11-107">Each record in the table represents one device.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b3f11-108"><strong>Столбец</strong></span><span class="sxs-lookup"><span data-stu-id="b3f11-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="b3f11-109"><strong>Тип данных</strong></span><span class="sxs-lookup"><span data-stu-id="b3f11-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="b3f11-110"><strong>Ключ/индекс</strong></span><span class="sxs-lookup"><span data-stu-id="b3f11-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="b3f11-111"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="b3f11-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b3f11-112"><strong>DeviceKey</strong></span><span class="sxs-lookup"><span data-stu-id="b3f11-112"><strong>DeviceKey</strong></span></span></p></td>
<td><p><span data-ttu-id="b3f11-113">целое</span><span class="sxs-lookup"><span data-stu-id="b3f11-113">int</span></span></p></td>
<td><p><span data-ttu-id="b3f11-114">Primary</span><span class="sxs-lookup"><span data-stu-id="b3f11-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="b3f11-115">Уникальный номер, идентифицирующий это устройство.</span><span class="sxs-lookup"><span data-stu-id="b3f11-115">Unique number identifying this device.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3f11-116"><strong>Водит</strong></span><span class="sxs-lookup"><span data-stu-id="b3f11-116"><strong>DeviceName</strong></span></span></p></td>
<td><p><span data-ttu-id="b3f11-117">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="b3f11-117">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="b3f11-118">Имя_устройства + DeviceType является уникальным</span><span class="sxs-lookup"><span data-stu-id="b3f11-118">DeviceName + DeviceType is unique</span></span></p></td>
<td><p><span data-ttu-id="b3f11-119">Имя устройства.</span><span class="sxs-lookup"><span data-stu-id="b3f11-119">Device name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3f11-120"><strong>DeviceType</strong></span><span class="sxs-lookup"><span data-stu-id="b3f11-120"><strong>DeviceType</strong></span></span></p></td>
<td><p><span data-ttu-id="b3f11-121">бит</span><span class="sxs-lookup"><span data-stu-id="b3f11-121">bit</span></span></p></td>
<td><p><span data-ttu-id="b3f11-122">Имя_устройства + DeviceType является уникальным</span><span class="sxs-lookup"><span data-stu-id="b3f11-122">DeviceName + DeviceType is unique</span></span></p></td>
<td><p><span data-ttu-id="b3f11-123">Тип устройства.</span><span class="sxs-lookup"><span data-stu-id="b3f11-123">Device type.</span></span> <span data-ttu-id="b3f11-124">1 — устройство захвата, 0 — устройство рендеринга.</span><span class="sxs-lookup"><span data-stu-id="b3f11-124">1 is a capture device, 0 is a render device.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="b3f11-125">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b3f11-125">


</div>

<span> </span>

</div>

</div>

</span></span></div>

