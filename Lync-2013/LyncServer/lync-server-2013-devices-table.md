---
title: 'Lync Server 2013: таблица Devices'
description: 'Таблица "устройства" Lync Server 2013: Devices.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Devices table
ms:assetid: 532e2280-4bbc-4a6c-93da-45d9f80a30a0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398351(v=OCS.15)
ms:contentKeyID: 48184169
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 763e1788e2874f9f9831c089ffe8fa077621b030
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429341"
---
# <a name="devices-table-in-lync-server-2013"></a><span data-ttu-id="5dd3e-103">Таблица Devices в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5dd3e-103">Devices table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5dd3e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5dd3e-104">

<span> </span></span></span>

<span data-ttu-id="5dd3e-105">_**Тема последнего изменения:** 2012-05-25_</span><span class="sxs-lookup"><span data-stu-id="5dd3e-105">_**Topic Last Modified:** 2012-05-25_</span></span>

<span data-ttu-id="5dd3e-106">Таблица "устройства" является вспомогательной таблицей.</span><span class="sxs-lookup"><span data-stu-id="5dd3e-106">The Devices table is a supporting table.</span></span> <span data-ttu-id="5dd3e-107">Каждая запись хранит информацию об одном устройстве (стационарном телефоне).</span><span class="sxs-lookup"><span data-stu-id="5dd3e-107">Each record stores information about one device (desk phone).</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5dd3e-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="5dd3e-108">Column</span></span></th>
<th><span data-ttu-id="5dd3e-109">Тип данных</span><span class="sxs-lookup"><span data-stu-id="5dd3e-109">Data Type</span></span></th>
<th><span data-ttu-id="5dd3e-110">Ключ/индекс</span><span class="sxs-lookup"><span data-stu-id="5dd3e-110">Key/Index</span></span></th>
<th><span data-ttu-id="5dd3e-111">Сведения</span><span class="sxs-lookup"><span data-stu-id="5dd3e-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5dd3e-112"><strong>Устройства</strong></span><span class="sxs-lookup"><span data-stu-id="5dd3e-112"><strong>DeviceId</strong></span></span></p></td>
<td><p><span data-ttu-id="5dd3e-113">целое</span><span class="sxs-lookup"><span data-stu-id="5dd3e-113">int</span></span></p></td>
<td><p><span data-ttu-id="5dd3e-114">Primary</span><span class="sxs-lookup"><span data-stu-id="5dd3e-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="5dd3e-115">Уникальный номер, идентифицирующий эту аппаратную версию.</span><span class="sxs-lookup"><span data-stu-id="5dd3e-115">Unique number identifying this hardware version.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dd3e-116"><strong>ManufacturerId</strong></span><span class="sxs-lookup"><span data-stu-id="5dd3e-116"><strong>ManufacturerId</strong></span></span></p></td>
<td><p><span data-ttu-id="5dd3e-117">целое</span><span class="sxs-lookup"><span data-stu-id="5dd3e-117">int</span></span></p></td>
<td><p><span data-ttu-id="5dd3e-118">Другом</span><span class="sxs-lookup"><span data-stu-id="5dd3e-118">Foreign</span></span></p></td>
<td><p><span data-ttu-id="5dd3e-119">Производитель этого устройства.</span><span class="sxs-lookup"><span data-stu-id="5dd3e-119">Manufacturer of this device.</span></span> <span data-ttu-id="5dd3e-120">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-manufacturers-table.md">таблицей изготовителей в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="5dd3e-120">See the <a href="lync-server-2013-manufacturers-table.md">Manufacturers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dd3e-121"><strong>HardwareVersionId</strong></span><span class="sxs-lookup"><span data-stu-id="5dd3e-121"><strong>HardwareVersionId</strong></span></span></p></td>
<td><p><span data-ttu-id="5dd3e-122">целое</span><span class="sxs-lookup"><span data-stu-id="5dd3e-122">int</span></span></p></td>
<td><p><span data-ttu-id="5dd3e-123">Другом</span><span class="sxs-lookup"><span data-stu-id="5dd3e-123">Foreign</span></span></p></td>
<td><p><span data-ttu-id="5dd3e-124">Аппаратная версия этого устройства.</span><span class="sxs-lookup"><span data-stu-id="5dd3e-124">Hardware version of this device.</span></span> <span data-ttu-id="5dd3e-125">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-hardwareversions-table.md">таблицей HardwareVersions в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="5dd3e-125">See the <a href="lync-server-2013-hardwareversions-table.md">HardwareVersions table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dd3e-126"><strong>MacAddress</strong></span><span class="sxs-lookup"><span data-stu-id="5dd3e-126"><strong>MacAddress</strong></span></span></p></td>
<td><p><span data-ttu-id="5dd3e-127">bigint</span><span class="sxs-lookup"><span data-stu-id="5dd3e-127">bigint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="5dd3e-128">MAC-адрес</span><span class="sxs-lookup"><span data-stu-id="5dd3e-128">MAC Address</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="5dd3e-129">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5dd3e-129">


</div>

<span> </span>

</div>

</div>

</span></span></div>

