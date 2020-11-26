---
title: 'Lync Server 2013: таблица IMReportSummary'
description: 'Таблица Lync Server 2013: IMReportSummary.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: IMReportSummary table
ms:assetid: 27ff9453-53f2-4fae-b637-70a086c9df96
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204753(v=OCS.15)
ms:contentKeyID: 48183673
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dfafa81d1605845b29a3627321fcbc0f72ca7ac7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427315"
---
# <a name="imreportsummary-table-in-lync-server-2013"></a><span data-ttu-id="61d15-103">Таблица IMReportSummary в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="61d15-103">IMReportSummary table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="61d15-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="61d15-104">

<span> </span></span></span>

<span data-ttu-id="61d15-105">_**Тема последнего изменения:** 2012-08-20_</span><span class="sxs-lookup"><span data-stu-id="61d15-105">_**Topic Last Modified:** 2012-08-20_</span></span>

<span data-ttu-id="61d15-106">IMReportSummaryTable предоставляет общий отчет о сеансах обмена мгновенными сообщениями, которые хранятся в Организации.</span><span class="sxs-lookup"><span data-stu-id="61d15-106">The IMReportSummaryTable provides an overall report on the instant messaging sessions held in an organization.</span></span> <span data-ttu-id="61d15-107">Эта таблица введена в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="61d15-107">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="61d15-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="61d15-108">Column</span></span></th>
<th><span data-ttu-id="61d15-109">Тип данных</span><span class="sxs-lookup"><span data-stu-id="61d15-109">Data Type</span></span></th>
<th><span data-ttu-id="61d15-110">Ключ/индекс</span><span class="sxs-lookup"><span data-stu-id="61d15-110">Key/Index</span></span></th>
<th><span data-ttu-id="61d15-111">Сведения</span><span class="sxs-lookup"><span data-stu-id="61d15-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="61d15-112"><strong>StartTime</strong></span><span class="sxs-lookup"><span data-stu-id="61d15-112"><strong>StartTime</strong></span></span></p></td>
<td><p><span data-ttu-id="61d15-113">datetime</span><span class="sxs-lookup"><span data-stu-id="61d15-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="61d15-114">Primary</span><span class="sxs-lookup"><span data-stu-id="61d15-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="61d15-115">Дата и время начала сеанса обмена мгновенными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="61d15-115">Date and time that the instant messaging session began.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61d15-116"><strong>TimePeriod</strong></span><span class="sxs-lookup"><span data-stu-id="61d15-116"><strong>TimePeriod</strong></span></span></p></td>
<td><p><span data-ttu-id="61d15-117">char (1)</span><span class="sxs-lookup"><span data-stu-id="61d15-117">char(1)</span></span></p></td>
<td><p><span data-ttu-id="61d15-118">Primary</span><span class="sxs-lookup"><span data-stu-id="61d15-118">Primary</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61d15-119"><strong>PoolFQDN</strong></span><span class="sxs-lookup"><span data-stu-id="61d15-119"><strong>PoolFQDN</strong></span></span></p></td>
<td><p><span data-ttu-id="61d15-120">nvarchar (257)</span><span class="sxs-lookup"><span data-stu-id="61d15-120">nvarchar(257)</span></span></p></td>
<td><p><span data-ttu-id="61d15-121">Primary</span><span class="sxs-lookup"><span data-stu-id="61d15-121">Primary</span></span></p></td>
<td><p><span data-ttu-id="61d15-122">Полное доменное имя пула, на котором размещается сеанс.</span><span class="sxs-lookup"><span data-stu-id="61d15-122">Fully qualified domain name of the pool hosting the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61d15-123"><strong>AuthType</strong></span><span class="sxs-lookup"><span data-stu-id="61d15-123"><strong>AuthType</strong></span></span></p></td>
<td><p><span data-ttu-id="61d15-124">целое</span><span class="sxs-lookup"><span data-stu-id="61d15-124">int</span></span></p></td>
<td><p><span data-ttu-id="61d15-125">Primary</span><span class="sxs-lookup"><span data-stu-id="61d15-125">Primary</span></span></p></td>
<td><p><span data-ttu-id="61d15-126">Приоритет звонка (например, срочной или несрочный).</span><span class="sxs-lookup"><span data-stu-id="61d15-126">Priority (for example, urgent or non-urgent) of the call.</span></span> <span data-ttu-id="61d15-127">Сведения о приоритетах хранятся в <a href="lync-server-2013-callpriorities-table.md">таблице CallPriorities в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="61d15-127">Priority information is stored in the <a href="lync-server-2013-callpriorities-table.md">CallPriorities table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61d15-128"><strong>SessionCount</strong></span><span class="sxs-lookup"><span data-stu-id="61d15-128"><strong>SessionCount</strong></span></span></p></td>
<td><p><span data-ttu-id="61d15-129">bigint</span><span class="sxs-lookup"><span data-stu-id="61d15-129">bigint</span></span></p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61d15-130"><strong>MsgCount</strong></span><span class="sxs-lookup"><span data-stu-id="61d15-130"><strong>MsgCount</strong></span></span></p></td>
<td><p><span data-ttu-id="61d15-131">bigint</span><span class="sxs-lookup"><span data-stu-id="61d15-131">bigint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="61d15-132">Общее количество мгновенных сообщений, пересылаемых во время сеанса.</span><span class="sxs-lookup"><span data-stu-id="61d15-132">Total number of instant messages exchanged during the session.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="61d15-133">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="61d15-133">


</div>

<span> </span>

</div>

</div>

</span></span></div>

