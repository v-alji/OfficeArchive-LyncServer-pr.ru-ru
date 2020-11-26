---
title: 'Lync Server 2013: таблица Users'
description: 'Таблица пользователей Lync Server 2013: Users.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Users table
ms:assetid: a8d71373-4b57-4245-9f02-f7fc0d9fcd3c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412791(v=OCS.15)
ms:contentKeyID: 48185032
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9b1418e162a04e46ee0dfeca082aa66b0665fc77
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436183"
---
# <a name="users-table-in-lync-server-2013"></a><span data-ttu-id="13a72-103">Таблица Users в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="13a72-103">Users table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="13a72-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="13a72-104">

<span> </span></span></span>

<span data-ttu-id="13a72-105">_**Тема последнего изменения:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="13a72-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="13a72-106">Таблица Users является вспомогательной таблицей.</span><span class="sxs-lookup"><span data-stu-id="13a72-106">The Users table is a supporting table.</span></span> <span data-ttu-id="13a72-107">В каждой записи в таблице хранятся сведения о пользователях, участвующих в звонках или сеансах с записями в базе данных.</span><span class="sxs-lookup"><span data-stu-id="13a72-107">Each record in the table stores information about one user involved in calls or sessions that have records in the database.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="13a72-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="13a72-108">Column</span></span></th>
<th><span data-ttu-id="13a72-109">Тип данных</span><span class="sxs-lookup"><span data-stu-id="13a72-109">Data Type</span></span></th>
<th><span data-ttu-id="13a72-110">Ключ/индекс</span><span class="sxs-lookup"><span data-stu-id="13a72-110">Key/Index</span></span></th>
<th><span data-ttu-id="13a72-111">Сведения</span><span class="sxs-lookup"><span data-stu-id="13a72-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="13a72-112"><strong>NextUpdateTS</strong></span><span class="sxs-lookup"><span data-stu-id="13a72-112"><strong>NextUpdateTS</strong></span></span></p></td>
<td><p><span data-ttu-id="13a72-113">datetime</span><span class="sxs-lookup"><span data-stu-id="13a72-113">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="13a72-114">Метка времени для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="13a72-114">Time stamp for internal use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13a72-115"><strong>Идентификатора пользователя</strong></span><span class="sxs-lookup"><span data-stu-id="13a72-115"><strong>UserId</strong></span></span></p></td>
<td><p><span data-ttu-id="13a72-116">целое</span><span class="sxs-lookup"><span data-stu-id="13a72-116">int</span></span></p></td>
<td><p><span data-ttu-id="13a72-117">Primary</span><span class="sxs-lookup"><span data-stu-id="13a72-117">Primary</span></span></p></td>
<td><p><span data-ttu-id="13a72-118">Уникальный номер, идентифицирующий этого пользователя.</span><span class="sxs-lookup"><span data-stu-id="13a72-118">Unique number identifying this user.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13a72-119"><strong>UserUri</strong></span><span class="sxs-lookup"><span data-stu-id="13a72-119"><strong>UserUri</strong></span></span></p></td>
<td><p><span data-ttu-id="13a72-120">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="13a72-120">nvarchar(450)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="13a72-121">URI пользователя.</span><span class="sxs-lookup"><span data-stu-id="13a72-121">User URI.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13a72-122"><strong>TenantId</strong></span><span class="sxs-lookup"><span data-stu-id="13a72-122"><strong>TenantId</strong></span></span></p></td>
<td><p><span data-ttu-id="13a72-123">целое</span><span class="sxs-lookup"><span data-stu-id="13a72-123">int</span></span></p></td>
<td><p><span data-ttu-id="13a72-124">Другом</span><span class="sxs-lookup"><span data-stu-id="13a72-124">Foreign</span></span></p></td>
<td><p><span data-ttu-id="13a72-125">Идентификатор клиента этого пользователя.</span><span class="sxs-lookup"><span data-stu-id="13a72-125">This user’s Tenant ID.</span></span> <span data-ttu-id="13a72-126">Дополнительные сведения приведены в <a href="lync-server-2013-tenants-table.md">таблице "клиенты" в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="13a72-126">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13a72-127"><strong>UriTypeId</strong></span><span class="sxs-lookup"><span data-stu-id="13a72-127"><strong>UriTypeId</strong></span></span></p></td>
<td><p><span data-ttu-id="13a72-128">целое</span><span class="sxs-lookup"><span data-stu-id="13a72-128">int</span></span></p></td>
<td><p><span data-ttu-id="13a72-129">Другом</span><span class="sxs-lookup"><span data-stu-id="13a72-129">Foreign</span></span></p></td>
<td><p><span data-ttu-id="13a72-130">Тип универсального кода ресурса (URI) этого пользователя.</span><span class="sxs-lookup"><span data-stu-id="13a72-130">This user’s URI type.</span></span> <span data-ttu-id="13a72-131">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-uritypes-table.md">таблицей UriTypes в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="13a72-131">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="13a72-132">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="13a72-132">


</div>

<span> </span>

</div>

</div>

</span></span></div>

