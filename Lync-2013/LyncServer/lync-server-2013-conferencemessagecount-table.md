---
title: 'Lync Server 2013: таблица ConferenceMessageCount'
description: 'Таблица Lync Server 2013: ConferenceMessageCount.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ConferenceMessageCount table
ms:assetid: 78569dbf-5217-42fa-ba1a-4380f56e2a3d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398590(v=OCS.15)
ms:contentKeyID: 48184570
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 271b654c09ab1aef194eb613e660de208aea1534
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434454"
---
# <a name="conferencemessagecount-table-in-lync-server-2013"></a><span data-ttu-id="5bfbf-103">Таблица ConferenceMessageCount в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5bfbf-103">ConferenceMessageCount table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5bfbf-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5bfbf-104">

<span> </span></span></span>

<span data-ttu-id="5bfbf-105">_**Тема последнего изменения:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="5bfbf-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="5bfbf-106">Каждая запись в этой таблице представляет одного пользователя в одной конференции для обмена мгновенными сообщениями и включает количество сообщений, отправленных этим пользователем.</span><span class="sxs-lookup"><span data-stu-id="5bfbf-106">Each record in this table represents one user in one IM conference and includes the number of messages sent by that user.</span></span> <span data-ttu-id="5bfbf-107">Каждая конференция представлена в этой таблице несколькими записями; одна запись для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="5bfbf-107">Each conference is represented by multiple records in this table; one record for each user.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5bfbf-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="5bfbf-108">Column</span></span></th>
<th><span data-ttu-id="5bfbf-109">Тип данных</span><span class="sxs-lookup"><span data-stu-id="5bfbf-109">Data Type</span></span></th>
<th><span data-ttu-id="5bfbf-110">Ключ/индекс</span><span class="sxs-lookup"><span data-stu-id="5bfbf-110">Key/Index</span></span></th>
<th><span data-ttu-id="5bfbf-111">Сведения</span><span class="sxs-lookup"><span data-stu-id="5bfbf-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5bfbf-112"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="5bfbf-112"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="5bfbf-113">datetime</span><span class="sxs-lookup"><span data-stu-id="5bfbf-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="5bfbf-114">Основной, внешний</span><span class="sxs-lookup"><span data-stu-id="5bfbf-114">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="5bfbf-115">Время экземпляра Конференции.</span><span class="sxs-lookup"><span data-stu-id="5bfbf-115">Time of conference instance.</span></span> <span data-ttu-id="5bfbf-116">Используется в сочетании с <strong>SessionIdSeq</strong> для уникальной идентификации экземпляра Конференции.</span><span class="sxs-lookup"><span data-stu-id="5bfbf-116">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a conference instance.</span></span> <span data-ttu-id="5bfbf-117">Дополнительные сведения приведены <a href="lync-server-2013-conferences-table.md">в таблице конференции для Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="5bfbf-117">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5bfbf-118"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="5bfbf-118"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="5bfbf-119">целое</span><span class="sxs-lookup"><span data-stu-id="5bfbf-119">int</span></span></p></td>
<td><p><span data-ttu-id="5bfbf-120">Основной, внешний</span><span class="sxs-lookup"><span data-stu-id="5bfbf-120">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="5bfbf-121">ИДЕНТИФИКАЦИОНный номер для идентификации экземпляра Конференции.</span><span class="sxs-lookup"><span data-stu-id="5bfbf-121">ID number to identify the conference instance.</span></span> <span data-ttu-id="5bfbf-122">Используется в сочетании с <strong>SessionIdTime</strong> для уникальной идентификации экземпляра Конференции.</span><span class="sxs-lookup"><span data-stu-id="5bfbf-122">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a conference instance.</span></span> <span data-ttu-id="5bfbf-123">Дополнительные сведения приведены <a href="lync-server-2013-conferences-table.md">в таблице конференции для Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="5bfbf-123">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5bfbf-124"><strong>Идентификатора пользователя</strong></span><span class="sxs-lookup"><span data-stu-id="5bfbf-124"><strong>UserId</strong></span></span></p></td>
<td><p><span data-ttu-id="5bfbf-125">целое</span><span class="sxs-lookup"><span data-stu-id="5bfbf-125">int</span></span></p></td>
<td><p><span data-ttu-id="5bfbf-126">Другом</span><span class="sxs-lookup"><span data-stu-id="5bfbf-126">Foreign</span></span></p></td>
<td><p><span data-ttu-id="5bfbf-127">Уникальный номер, идентифицирующий этого пользователя, на который ссылается <a href="lync-server-2013-users-table.md">Таблица "Пользователи" в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="5bfbf-127">Unique number identifying this user, referenced from the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5bfbf-128"><strong>MessageCount</strong></span><span class="sxs-lookup"><span data-stu-id="5bfbf-128"><strong>MessageCount</strong></span></span></p></td>
<td><p><span data-ttu-id="5bfbf-129">smallint</span><span class="sxs-lookup"><span data-stu-id="5bfbf-129">smallint</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="5bfbf-130">Количество сообщений, отправленных этим пользователем во время данной Конференции.</span><span class="sxs-lookup"><span data-stu-id="5bfbf-130">The number of messages sent by this user during this conference.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="5bfbf-131">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5bfbf-131">


</div>

<span> </span>

</div>

</div>

</span></span></div>

