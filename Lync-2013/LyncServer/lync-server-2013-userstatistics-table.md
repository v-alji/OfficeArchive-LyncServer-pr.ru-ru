---
title: 'Lync Server 2013: таблица UserStatistics'
description: 'Таблица Lync Server 2013: UserStatistics.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: UserStatistics table
ms:assetid: cfaf803b-1679-4169-92d3-533fad3e56ed
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721893(v=OCS.15)
ms:contentKeyID: 49733827
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 75b34fa3c34af4cc9cf2cacc6ae7feb4d217114c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436099"
---
# <a name="userstatistics-table-in-lync-server-2013"></a><span data-ttu-id="49c1c-103">Таблица UserStatistics в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="49c1c-103">UserStatistics table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="49c1c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="49c1c-104">

<span> </span></span></span>

<span data-ttu-id="49c1c-105">_**Тема последнего изменения:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="49c1c-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="49c1c-106">Таблица UserStatistics является вспомогательной таблицей.</span><span class="sxs-lookup"><span data-stu-id="49c1c-106">The UserStatistics table is a supporting table.</span></span> <span data-ttu-id="49c1c-107">Каждая запись в таблице содержит сведения об использовании системы конкретным пользователем.</span><span class="sxs-lookup"><span data-stu-id="49c1c-107">Each record in the table stores information about an individual user’s usage of the system.</span></span> <span data-ttu-id="49c1c-108">Эта таблица введена в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="49c1c-108">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="49c1c-109">Столбец</span><span class="sxs-lookup"><span data-stu-id="49c1c-109">Column</span></span></th>
<th><span data-ttu-id="49c1c-110">Тип данных</span><span class="sxs-lookup"><span data-stu-id="49c1c-110">Data Type</span></span></th>
<th><span data-ttu-id="49c1c-111">Ключ/индекс</span><span class="sxs-lookup"><span data-stu-id="49c1c-111">Key/Index</span></span></th>
<th><span data-ttu-id="49c1c-112">Сведения</span><span class="sxs-lookup"><span data-stu-id="49c1c-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49c1c-113"><strong>Идентификатора пользователя</strong></span><span class="sxs-lookup"><span data-stu-id="49c1c-113"><strong>UserId</strong></span></span></p></td>
<td><p><span data-ttu-id="49c1c-114">целое</span><span class="sxs-lookup"><span data-stu-id="49c1c-114">int</span></span></p></td>
<td><p><span data-ttu-id="49c1c-115">Primary</span><span class="sxs-lookup"><span data-stu-id="49c1c-115">Primary</span></span></p></td>
<td><p><span data-ttu-id="49c1c-116">Уникальный номер, идентифицирующий этого пользователя.</span><span class="sxs-lookup"><span data-stu-id="49c1c-116">Unique number identifying this user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49c1c-117"><strong>LastLogInTime</strong></span><span class="sxs-lookup"><span data-stu-id="49c1c-117"><strong>LastLogInTime</strong></span></span></p></td>
<td><p><span data-ttu-id="49c1c-118">datetime</span><span class="sxs-lookup"><span data-stu-id="49c1c-118">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="49c1c-119">Время последнего входа пользователя в систему.</span><span class="sxs-lookup"><span data-stu-id="49c1c-119">Last time the user logged in.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49c1c-120"><strong>LastConfOrganizedTime</strong></span><span class="sxs-lookup"><span data-stu-id="49c1c-120"><strong>LastConfOrganizedTime</strong></span></span></p></td>
<td><p><span data-ttu-id="49c1c-121">datetime</span><span class="sxs-lookup"><span data-stu-id="49c1c-121">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="49c1c-122">Последний раз, когда пользователь организует конференцию.</span><span class="sxs-lookup"><span data-stu-id="49c1c-122">Last time the user organized a conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49c1c-123"><strong>LastCallOrganizerCallFailureTime</strong></span><span class="sxs-lookup"><span data-stu-id="49c1c-123"><strong>LastCallOrganizerCallFailureTime</strong></span></span></p></td>
<td><p><span data-ttu-id="49c1c-124">datetime</span><span class="sxs-lookup"><span data-stu-id="49c1c-124">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="49c1c-125">Последнее время, когда пользователь попытался вызвать сбой звонка.</span><span class="sxs-lookup"><span data-stu-id="49c1c-125">Last time the user experienced a call failure.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49c1c-126"><strong>LastConfOrganizerCallFailureTime</strong></span><span class="sxs-lookup"><span data-stu-id="49c1c-126"><strong>LastConfOrganizerCallFailureTime</strong></span></span></p></td>
<td><p><span data-ttu-id="49c1c-127">datetime</span><span class="sxs-lookup"><span data-stu-id="49c1c-127">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="49c1c-128">Последний раз, когда пользователь попытался вызвать сбой в организаторе конференц-связи.</span><span class="sxs-lookup"><span data-stu-id="49c1c-128">Last time the user experienced a call failure as a conference organizer.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="49c1c-129">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="49c1c-129">


</div>

<span> </span>

</div>

</div>

</span></span></div>

