---
title: 'Lync Server 2013: таблица Locations'
description: 'Таблица "расположения" Lync Server 2013: местонахождения.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Locations table
ms:assetid: 78dc1b14-5394-4f8e-89d3-4ba593272a04
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398596(v=OCS.15)
ms:contentKeyID: 48184579
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9d07b6d3d3820f4efb3310adf0734a7e10c53e6d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399832"
---
# <a name="locations-table-in-lync-server-2013"></a><span data-ttu-id="71b5d-103">Таблица Locations в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="71b5d-103">Locations table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="71b5d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="71b5d-104">

<span> </span></span></span>

<span data-ttu-id="71b5d-105">_**Тема последнего изменения:** 2012-05-25_</span><span class="sxs-lookup"><span data-stu-id="71b5d-105">_**Topic Last Modified:** 2012-05-25_</span></span>

<span data-ttu-id="71b5d-106">Каждая запись представляет одну ссылку на расположение в экстренном звонке, например, в вызове E9-1-1.</span><span class="sxs-lookup"><span data-stu-id="71b5d-106">Each record represents one location reference in an emergency call, like an E9-1-1 call.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="71b5d-107">Столбец</span><span class="sxs-lookup"><span data-stu-id="71b5d-107">Column</span></span></th>
<th><span data-ttu-id="71b5d-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="71b5d-108">Data Type</span></span></th>
<th><span data-ttu-id="71b5d-109">Ключ/индекс</span><span class="sxs-lookup"><span data-stu-id="71b5d-109">Key/Index</span></span></th>
<th><span data-ttu-id="71b5d-110">Сведения</span><span class="sxs-lookup"><span data-stu-id="71b5d-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="71b5d-111"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="71b5d-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="71b5d-112">datetime</span><span class="sxs-lookup"><span data-stu-id="71b5d-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="71b5d-113">Основной, внешний</span><span class="sxs-lookup"><span data-stu-id="71b5d-113">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="71b5d-114">Время запроса сеанса.</span><span class="sxs-lookup"><span data-stu-id="71b5d-114">Time of session request.</span></span> <span data-ttu-id="71b5d-115">Используется в сочетании с <strong>SessionIdSeq</strong> для уникальной идентификации сеанса.</span><span class="sxs-lookup"><span data-stu-id="71b5d-115">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="71b5d-116">Дополнительные сведения приведены <a href="lync-server-2013-dialogs-table.md">в таблице диалоговые окна Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="71b5d-116">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71b5d-117"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="71b5d-117"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="71b5d-118">целое</span><span class="sxs-lookup"><span data-stu-id="71b5d-118">int</span></span></p></td>
<td><p><span data-ttu-id="71b5d-119">Основной, внешний</span><span class="sxs-lookup"><span data-stu-id="71b5d-119">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="71b5d-120">ИДЕНТИФИКАЦИОНный номер для идентификации сеанса.</span><span class="sxs-lookup"><span data-stu-id="71b5d-120">ID number to identify the session.</span></span> <span data-ttu-id="71b5d-121">Используется в сочетании с <strong>SessionIdTime</strong> для уникальной идентификации сеанса.</span><span class="sxs-lookup"><span data-stu-id="71b5d-121">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.</span></span> <span data-ttu-id="71b5d-122">Дополнительные сведения приведены <a href="lync-server-2013-dialogs-table.md">в таблице диалоговые окна Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="71b5d-122">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71b5d-123"><strong>Расположение</strong></span><span class="sxs-lookup"><span data-stu-id="71b5d-123"><strong>Location</strong></span></span></p></td>
<td><p><span data-ttu-id="71b5d-124">nvarchar (max)</span><span class="sxs-lookup"><span data-stu-id="71b5d-124">nvarchar(max)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="71b5d-125">Место вызова экстренной помощи.</span><span class="sxs-lookup"><span data-stu-id="71b5d-125">Location of emergency call.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="71b5d-126">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="71b5d-126">


</div>

<span> </span>

</div>

</div>

</span></span></div>

