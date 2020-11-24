---
title: 'Lync Server 2013: планирование емкости для парковки вызовов'
description: 'Lync Server 2013: планирование мощностей для приостановки звонков.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Capacity planning for Call Park
ms:assetid: 75520310-760a-4b1b-bcc1-4d724d13f87a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg416493(v=OCS.15)
ms:contentKeyID: 48184529
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 053a6dabad9d10540e84e9e4f43de09057c295f5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399952"
---
# <a name="capacity-planning-for-call-park-in-lync-server-2013"></a><span data-ttu-id="54137-103">Планирование емкости для парковки вызовов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="54137-103">Capacity planning for Call Park in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="54137-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="54137-104">

<span> </span></span></span>

<span data-ttu-id="54137-105">_**Тема последнего изменения:** 2012-09-13_</span><span class="sxs-lookup"><span data-stu-id="54137-105">_**Topic Last Modified:** 2012-09-13_</span></span>

<div id="sectionSection0" class="section">

<span data-ttu-id="54137-106">В приведенной ниже таблице описана пользовательская модель парковки звонков, которую можно использовать в качестве основы для планирования производственных мощностей.</span><span class="sxs-lookup"><span data-stu-id="54137-106">The following table describes the Call Park user model that you can use as the basis for capacity planning requirements.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="54137-107">Имейте в виду, что при планировании производительности аварийного восстановления каждый пул из сопряженного пула может обрабатывать рабочие нагрузки для служб приостановки звонков в обоих пулах.</span><span class="sxs-lookup"><span data-stu-id="54137-107">Keep in mind that, for disaster recovery capacity planning, each pool of a paired pool should be able to handle the workloads for Call Park services in both pools.</span></span>



</div>

### <a name="call-park-user-model"></a><span data-ttu-id="54137-108">Пользовательская модель парковки вызовов</span><span class="sxs-lookup"><span data-stu-id="54137-108">Call Park User Model</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="54137-109">Показатель</span><span class="sxs-lookup"><span data-stu-id="54137-109">Metric</span></span></th>
<th><span data-ttu-id="54137-110">На пул переднего плана (с 8 серверами переднего плана)</span><span class="sxs-lookup"><span data-stu-id="54137-110">Per Front End pool (with 8 Front End Servers)</span></span></th>
<th><span data-ttu-id="54137-111">Для каждого сервера Standard Edition</span><span class="sxs-lookup"><span data-stu-id="54137-111">Per Standard Edition server</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="54137-112">Скорость парковки</span><span class="sxs-lookup"><span data-stu-id="54137-112">Park rate</span></span></p></td>
<td><p><span data-ttu-id="54137-113">8 вызов в минуту</span><span class="sxs-lookup"><span data-stu-id="54137-113">8 per minute</span></span></p></td>
<td><p><span data-ttu-id="54137-114">1 вызов в минуту</span><span class="sxs-lookup"><span data-stu-id="54137-114">1 per minute</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54137-115">Скорость извлечения приостановленных вызовов</span><span class="sxs-lookup"><span data-stu-id="54137-115">Retrieve parked call rate</span></span></p></td>
<td><p><span data-ttu-id="54137-116">8 вызов в минуту</span><span class="sxs-lookup"><span data-stu-id="54137-116">8 per minute</span></span></p></td>
<td><p><span data-ttu-id="54137-117">1 вызов в минуту</span><span class="sxs-lookup"><span data-stu-id="54137-117">1 per minute</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54137-118">Среднее время парковки</span><span class="sxs-lookup"><span data-stu-id="54137-118">Average park duration</span></span></p></td>
<td><p><span data-ttu-id="54137-119">60 с</span><span class="sxs-lookup"><span data-stu-id="54137-119">60 seconds</span></span></p></td>
<td><p><span data-ttu-id="54137-120">60 с</span><span class="sxs-lookup"><span data-stu-id="54137-120">60 seconds</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="54137-121">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="54137-121">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

