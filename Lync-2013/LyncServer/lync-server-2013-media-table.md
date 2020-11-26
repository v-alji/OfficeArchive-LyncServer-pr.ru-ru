---
title: 'Lync Server 2013: таблица Media'
description: 'Таблица медиа сервера Lync Server 2013: Media.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Media table
ms:assetid: 1e1b427f-59b5-4564-bde5-1002a80439ee
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398268(v=OCS.15)
ms:contentKeyID: 48183568
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 31e30d1f91c59b8e3aa7915fc0d513618d0f709f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425677"
---
# <a name="media-table-in-lync-server-2013"></a><span data-ttu-id="8b2fe-103">Таблица Media в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8b2fe-103">Media table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8b2fe-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8b2fe-104">

<span> </span></span></span>

<span data-ttu-id="8b2fe-105">_**Тема последнего изменения:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="8b2fe-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="8b2fe-106">Каждая запись представляет один тип мультимедиа, используемый в одноранговых сеансах.</span><span class="sxs-lookup"><span data-stu-id="8b2fe-106">Each record represents one media type used in a peer-to-peer session.</span></span> <span data-ttu-id="8b2fe-107">Один сеанс будет представлен в таблице несколькими записями, если используется более одного типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="8b2fe-107">One session would be represented by multiple records in the table, if more than one media type is used.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="8b2fe-108">Таблицу мультимедиа нельзя использовать для расчета длительности мультимедиа для сеанса.</span><span class="sxs-lookup"><span data-stu-id="8b2fe-108">The Media table should not be used to calculate the media duration for a session.</span></span> <span data-ttu-id="8b2fe-109">В этой таблице содержатся сведения о сигнализации обмена мультимедийными данными в сеансе.</span><span class="sxs-lookup"><span data-stu-id="8b2fe-109">This table contains the signaling details of media exchange in a session.</span></span> <span data-ttu-id="8b2fe-110">Обмен мультимедийными данными выполняется запросом приглашения, а StartTime указывает время отправки приглашения. Время приглашения не обязательно означает время запуска мультимедиа, так как Media запускается только после того, как сеанс принял сеанс.</span><span class="sxs-lookup"><span data-stu-id="8b2fe-110">Media exchange is done by the INVITE request, and StartTime indicates the time that the INVITE was sent out. The invite time does not necessarily mean the media start time, because media starts only after the sessionee accepts the session.</span></span> <span data-ttu-id="8b2fe-111">Значение EndTime обычно означает время окончания этого сеанса.</span><span class="sxs-lookup"><span data-stu-id="8b2fe-111">The EndTime usually means the end time of this session.</span></span>



</div>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8b2fe-112">Столбец</span><span class="sxs-lookup"><span data-stu-id="8b2fe-112">Column</span></span></th>
<th><span data-ttu-id="8b2fe-113">Тип данных</span><span class="sxs-lookup"><span data-stu-id="8b2fe-113">Data Type</span></span></th>
<th><span data-ttu-id="8b2fe-114">Ключ/индекс</span><span class="sxs-lookup"><span data-stu-id="8b2fe-114">Key/Index</span></span></th>
<th><span data-ttu-id="8b2fe-115">Сведения</span><span class="sxs-lookup"><span data-stu-id="8b2fe-115">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8b2fe-116"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="8b2fe-116"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="8b2fe-117">datetime</span><span class="sxs-lookup"><span data-stu-id="8b2fe-117">datetime</span></span></p></td>
<td><p><span data-ttu-id="8b2fe-118">Основной, внешний</span><span class="sxs-lookup"><span data-stu-id="8b2fe-118">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="8b2fe-119">Время запроса сеанса.</span><span class="sxs-lookup"><span data-stu-id="8b2fe-119">Time of session request.</span></span> <span data-ttu-id="8b2fe-120">Используется в сочетании с <strong>SessionIdSeq</strong> для уникальной идентификации сеанса.</span><span class="sxs-lookup"><span data-stu-id="8b2fe-120">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="8b2fe-121">Дополнительные сведения приведены <a href="lync-server-2013-dialogs-table.md">в таблице диалоговые окна Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="8b2fe-121">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b2fe-122"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="8b2fe-122"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="8b2fe-123">целое</span><span class="sxs-lookup"><span data-stu-id="8b2fe-123">int</span></span></p></td>
<td><p><span data-ttu-id="8b2fe-124">Основной, внешний</span><span class="sxs-lookup"><span data-stu-id="8b2fe-124">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="8b2fe-125">ИДЕНТИФИКАЦИОНный номер для идентификации сеанса.</span><span class="sxs-lookup"><span data-stu-id="8b2fe-125">ID number to identify the session.</span></span> <span data-ttu-id="8b2fe-126">Используется в сочетании с <strong>SessionIdTime</strong> для уникальной идентификации сеанса.</span><span class="sxs-lookup"><span data-stu-id="8b2fe-126">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.</span></span> <span data-ttu-id="8b2fe-127">Дополнительные сведения приведены <a href="lync-server-2013-dialogs-table.md">в таблице диалоговые окна Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="8b2fe-127">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b2fe-128"><strong>MediaId</strong></span><span class="sxs-lookup"><span data-stu-id="8b2fe-128"><strong>MediaId</strong></span></span></p></td>
<td><p><span data-ttu-id="8b2fe-129">tinyint</span><span class="sxs-lookup"><span data-stu-id="8b2fe-129">tinyint</span></span></p></td>
<td><p><span data-ttu-id="8b2fe-130">Основной, внешний</span><span class="sxs-lookup"><span data-stu-id="8b2fe-130">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="8b2fe-131">Уникальный номер, идентифицирующий этот тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="8b2fe-131">Unique number identifying this media type.</span></span> <span data-ttu-id="8b2fe-132">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-medialist-table.md">таблицей MediaList в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="8b2fe-132">See the <a href="lync-server-2013-medialist-table.md">MediaList table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b2fe-133"><strong>StartTime</strong></span><span class="sxs-lookup"><span data-stu-id="8b2fe-133"><strong>StartTime</strong></span></span></p></td>
<td><p><span data-ttu-id="8b2fe-134">datetime</span><span class="sxs-lookup"><span data-stu-id="8b2fe-134">datetime</span></span></p></td>
<td><p><span data-ttu-id="8b2fe-135">Primary</span><span class="sxs-lookup"><span data-stu-id="8b2fe-135">Primary</span></span></p></td>
<td><p><span data-ttu-id="8b2fe-136">Это время отправки запроса мультимедиа, а не фактического времени запуска мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="8b2fe-136">This is the time that a media request was sent out, not the real media start time.</span></span> <span data-ttu-id="8b2fe-137">Параметр <strong>StartTime</strong> включает время настройки сеанса.</span><span class="sxs-lookup"><span data-stu-id="8b2fe-137"><strong>StartTime</strong> includes the session setup time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b2fe-138"><strong>EndTime</strong></span><span class="sxs-lookup"><span data-stu-id="8b2fe-138"><strong>EndTime</strong></span></span></p></td>
<td><p><span data-ttu-id="8b2fe-139">datetime</span><span class="sxs-lookup"><span data-stu-id="8b2fe-139">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="8b2fe-140">Это время окончания сеанса.</span><span class="sxs-lookup"><span data-stu-id="8b2fe-140">This is the end time of the session.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="8b2fe-141">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8b2fe-141">


</div>

<span> </span>

</div>

</div>

</span></span></div>

