---
title: 'Lync Server 2013: таблица Dialogs'
description: 'Lync Server 2013: таблица диалогов.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Dialogs table
ms:assetid: 487a430b-af66-4ea6-b28e-4e33cfdb7f9e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425954(v=OCS.15)
ms:contentKeyID: 48184001
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8c2c9cf9ec59fc48f7f5ffc6232980e3f8aa68c1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429184"
---
# <a name="dialogs-table-in-lync-server-2013"></a><span data-ttu-id="5080f-103">Таблица Dialogs в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5080f-103">Dialogs table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5080f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5080f-104">

<span> </span></span></span>

<span data-ttu-id="5080f-105">_**Тема последнего изменения:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="5080f-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="5080f-106">Таблица диалогов — это вспомогательная таблица, в которой хранятся сведения о DialogIDs для одноранговых сеансов.</span><span class="sxs-lookup"><span data-stu-id="5080f-106">The Dialogs table is a supporting table that stores the information about DialogIDs for peer-to-peer sessions.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5080f-107">Столбец</span><span class="sxs-lookup"><span data-stu-id="5080f-107">Column</span></span></th>
<th><span data-ttu-id="5080f-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="5080f-108">Data Type</span></span></th>
<th><span data-ttu-id="5080f-109">Ключ/индекс</span><span class="sxs-lookup"><span data-stu-id="5080f-109">Key/Index</span></span></th>
<th><span data-ttu-id="5080f-110">Сведения</span><span class="sxs-lookup"><span data-stu-id="5080f-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5080f-111"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="5080f-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="5080f-112">datetime</span><span class="sxs-lookup"><span data-stu-id="5080f-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="5080f-113">Primary</span><span class="sxs-lookup"><span data-stu-id="5080f-113">Primary</span></span></p></td>
<td><p><span data-ttu-id="5080f-114">Время запроса сеанса; используется в сочетании с SessionIDSeq для уникальной идентификации сеанса.</span><span class="sxs-lookup"><span data-stu-id="5080f-114">Time of session request; used in conjunction with SessionIDSeq to uniquely identify a session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5080f-115"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="5080f-115"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="5080f-116">целое</span><span class="sxs-lookup"><span data-stu-id="5080f-116">int</span></span></p></td>
<td><p><span data-ttu-id="5080f-117">Primary</span><span class="sxs-lookup"><span data-stu-id="5080f-117">Primary</span></span></p></td>
<td><p><span data-ttu-id="5080f-118">ИДЕНТИФИКАЦИОНный номер для идентификации сеанса.</span><span class="sxs-lookup"><span data-stu-id="5080f-118">ID number to identify the session.</span></span> <span data-ttu-id="5080f-119">Используется в сочетании с SessionIDTime для уникальной идентификации сеанса.</span><span class="sxs-lookup"><span data-stu-id="5080f-119">Used in conjunction with SessionIDTime to uniquely identify a session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5080f-120"><strong>ExternalChecksum</strong></span><span class="sxs-lookup"><span data-stu-id="5080f-120"><strong>ExternalChecksum</strong></span></span></p></td>
<td><p><span data-ttu-id="5080f-121">целое</span><span class="sxs-lookup"><span data-stu-id="5080f-121">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="5080f-122">Контрольная сумма ExternalID.</span><span class="sxs-lookup"><span data-stu-id="5080f-122">Checksum of the ExternalID.</span></span> <span data-ttu-id="5080f-123">Это поле используется для увеличения скорости поиска в базе данных.</span><span class="sxs-lookup"><span data-stu-id="5080f-123">This field is used to increase the speed of database searches.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5080f-124"><strong>ExternalId</strong></span><span class="sxs-lookup"><span data-stu-id="5080f-124"><strong>ExternalId</strong></span></span></p></td>
<td><p><span data-ttu-id="5080f-125">varbinary (775)</span><span class="sxs-lookup"><span data-stu-id="5080f-125">varbinary(775)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="5080f-126">ИДЕНТИФИКАТОР диалогового окна SIP, сохраненный в виде двоичного файла.</span><span class="sxs-lookup"><span data-stu-id="5080f-126">SIP dialog ID, stored as a binary.</span></span> <span data-ttu-id="5080f-127">Двоичный формат:</span><span class="sxs-lookup"><span data-stu-id="5080f-127">The format of the binary is:</span></span></p>
<p><span data-ttu-id="5080f-128">диалоговое окно; тег "from-Tag"</span><span class="sxs-lookup"><span data-stu-id="5080f-128">dialog;from-tag;to-tag</span></span></p>
<p><span data-ttu-id="5080f-129">Эти данные можно преобразовать в текстовый формат, используя следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="5080f-129">This data can be converted to text format by using this syntax:</span></span></p>
<p><code>cast(cast(ExternalId as varbinary(max)) as varchar(max))</code></p></td>
</tr>
</tbody>
</table><span data-ttu-id="5080f-130">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5080f-130">


</div>

<span> </span>

</div>

</div>

</span></span></div>

