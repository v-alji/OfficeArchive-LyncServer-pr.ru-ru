---
title: 'Lync Server 2013: таблица Phones'
description: 'Таблица Lync Server 2013: phones.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Phones table
ms:assetid: 41cb356d-9cc8-42b6-ac23-98a61b25aadc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425923(v=OCS.15)
ms:contentKeyID: 48183996
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9c62fffecd2442b79aefde77eb037dca4bffc9d4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437114"
---
# <a name="phones-table-in-lync-server-2013"></a><span data-ttu-id="cac99-103">Таблица Phones в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cac99-103">Phones table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cac99-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cac99-104">

<span> </span></span></span>

<span data-ttu-id="cac99-105">_**Тема последнего изменения:** 2012-08-20_</span><span class="sxs-lookup"><span data-stu-id="cac99-105">_**Topic Last Modified:** 2012-08-20_</span></span>

<span data-ttu-id="cac99-106">Таблица phones является вспомогательной таблицей.</span><span class="sxs-lookup"><span data-stu-id="cac99-106">The Phones table is a supporting table.</span></span> <span data-ttu-id="cac99-107">Каждая запись в таблице хранит информацию об одном номере телефона, который участвует в звонках по протоколу VoIP с записями в базе данных.</span><span class="sxs-lookup"><span data-stu-id="cac99-107">Each record in the table stores information about one phone number involved in VoIP calls that have records in the database.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cac99-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="cac99-108">Column</span></span></th>
<th><span data-ttu-id="cac99-109">Тип данных</span><span class="sxs-lookup"><span data-stu-id="cac99-109">Data Type</span></span></th>
<th><span data-ttu-id="cac99-110">Ключ/индекс</span><span class="sxs-lookup"><span data-stu-id="cac99-110">Key/Index</span></span></th>
<th><span data-ttu-id="cac99-111">Сведения</span><span class="sxs-lookup"><span data-stu-id="cac99-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cac99-112"><strong>PhoneId</strong></span><span class="sxs-lookup"><span data-stu-id="cac99-112"><strong>PhoneId</strong></span></span></p></td>
<td><p><span data-ttu-id="cac99-113">целое</span><span class="sxs-lookup"><span data-stu-id="cac99-113">int</span></span></p></td>
<td><p><span data-ttu-id="cac99-114">Primary</span><span class="sxs-lookup"><span data-stu-id="cac99-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="cac99-115">Уникальный номер, идентифицирующий этот телефон.</span><span class="sxs-lookup"><span data-stu-id="cac99-115">Unique number identifying this phone.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cac99-116"><strong>PhoneUri</strong></span><span class="sxs-lookup"><span data-stu-id="cac99-116"><strong>PhoneUri</strong></span></span></p></td>
<td><p><span data-ttu-id="cac99-117">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="cac99-117">nvarchar(450)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="cac99-118">Номер телефона.</span><span class="sxs-lookup"><span data-stu-id="cac99-118">Phone number.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cac99-119"><strong>NextUpdateTS</strong></span><span class="sxs-lookup"><span data-stu-id="cac99-119"><strong>NextUpdateTS</strong></span></span></p></td>
<td><p><span data-ttu-id="cac99-120">Датой</span><span class="sxs-lookup"><span data-stu-id="cac99-120">dateTime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="cac99-121">Метка времени (только для внутреннего использования).</span><span class="sxs-lookup"><span data-stu-id="cac99-121">Time stamp (for internal use only).</span></span></p>
<p><span data-ttu-id="cac99-122">Это поле было введено в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="cac99-122">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="cac99-123">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cac99-123">


</div>

<span> </span>

</div>

</div>

</span></span></div>

