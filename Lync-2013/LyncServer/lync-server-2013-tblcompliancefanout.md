---
title: 'Lync Server 2013: tblComplianceFanout'
description: 'Lync Server 2013: tblComplianceFanout.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblComplianceFanout
ms:assetid: f5d9f342-a7cb-4b54-baa6-e656256b75ad
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615050(v=OCS.15)
ms:contentKeyID: 48185828
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0cb94fff579c504598f027c8c68c7dde00a5a516
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423530"
---
# <a name="tblcompliancefanout-in-lync-server-2013"></a><span data-ttu-id="03972-103">tblComplianceFanout в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="03972-103">tblComplianceFanout in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="03972-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="03972-104">

<span> </span></span></span>

<span data-ttu-id="03972-105">_**Тема последнего изменения:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="03972-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="03972-106">tblComplianceFanout включает все серверы, которые обрабатывали событие соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="03972-106">tblComplianceFanout contains all servers that processed a compliance event.</span></span>

### <a name="columns"></a><span data-ttu-id="03972-107">Столбцов</span><span class="sxs-lookup"><span data-stu-id="03972-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="03972-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="03972-108">Column</span></span></th>
<th><span data-ttu-id="03972-109">Тип</span><span class="sxs-lookup"><span data-stu-id="03972-109">Type</span></span></th>
<th><span data-ttu-id="03972-110">Описание</span><span class="sxs-lookup"><span data-stu-id="03972-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="03972-111">fanoutEventID</span><span class="sxs-lookup"><span data-stu-id="03972-111">fanoutEventID</span></span></p></td>
<td><p><span data-ttu-id="03972-112">целое</span><span class="sxs-lookup"><span data-stu-id="03972-112">int</span></span></p></td>
<td><p><span data-ttu-id="03972-113">Код события.</span><span class="sxs-lookup"><span data-stu-id="03972-113">Event ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03972-114">fanoutServerID</span><span class="sxs-lookup"><span data-stu-id="03972-114">fanoutServerID</span></span></p></td>
<td><p><span data-ttu-id="03972-115">целое</span><span class="sxs-lookup"><span data-stu-id="03972-115">int</span></span></p></td>
<td><p><span data-ttu-id="03972-116">Идентификация сервера (соответствующая таблице tblServerIdentity. serverID).</span><span class="sxs-lookup"><span data-stu-id="03972-116">Server identity (corresponding to tblServerIdentity.serverID table).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="key"></a><span data-ttu-id="03972-117">Ключ</span><span class="sxs-lookup"><span data-stu-id="03972-117">Key</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="03972-118">Столбец</span><span class="sxs-lookup"><span data-stu-id="03972-118">Column</span></span></th>
<th><span data-ttu-id="03972-119">Описание</span><span class="sxs-lookup"><span data-stu-id="03972-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="03972-120">fanoutEventID</span><span class="sxs-lookup"><span data-stu-id="03972-120">fanoutEventID</span></span></p></td>
<td><p><span data-ttu-id="03972-121">Внешний ключ с подстановкой в таблице tblComplianceData. cmplEventID.</span><span class="sxs-lookup"><span data-stu-id="03972-121">Foreign key with lookup in tblComplianceData.cmplEventID table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="03972-122">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="03972-122">


</div>

<span> </span>

</div>

</div>

</span></span></div>

