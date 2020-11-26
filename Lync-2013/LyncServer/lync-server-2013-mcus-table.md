---
title: 'Lync Server 2013: таблица Mcus'
description: 'Таблица Lync Server 2013: MCUs.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Mcus table
ms:assetid: 271b7963-8fd8-4d92-a701-1a62aaf895ee
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425742(v=OCS.15)
ms:contentKeyID: 48183674
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b0b5d0bcbebb5efc1d767776b4581b18d9f2ed18
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425747"
---
# <a name="mcus-table-in-lync-server-2013"></a><span data-ttu-id="db0bc-103">Таблица Mcus в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="db0bc-103">Mcus table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="db0bc-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="db0bc-104">

<span> </span></span></span>

<span data-ttu-id="db0bc-105">_**Тема последнего изменения:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="db0bc-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="db0bc-106">Таблица MCUs является вспомогательной таблицей.</span><span class="sxs-lookup"><span data-stu-id="db0bc-106">The Mcus table is a supporting table.</span></span> <span data-ttu-id="db0bc-107">Каждая запись содержит сведения о одной службе конференц-связи.</span><span class="sxs-lookup"><span data-stu-id="db0bc-107">Each record stores information about one conferencing service.</span></span> <span data-ttu-id="db0bc-108">К ним относятся служба конференций обмена мгновенными сообщениями и служба конференц-связи с телефонным подключением (которая запускается как процессы на серверах переднего плана), а также службы "веб-конференции" и "Конференция".</span><span class="sxs-lookup"><span data-stu-id="db0bc-108">These can include the IM Conferencing service and the Telephony Conferencing service (which run as processes on front-end servers), and the Web Conferencing service and A/V Conferencing service.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="db0bc-109">Столбец</span><span class="sxs-lookup"><span data-stu-id="db0bc-109">Column</span></span></th>
<th><span data-ttu-id="db0bc-110">Тип данных</span><span class="sxs-lookup"><span data-stu-id="db0bc-110">Data Type</span></span></th>
<th><span data-ttu-id="db0bc-111">Ключ/индекс</span><span class="sxs-lookup"><span data-stu-id="db0bc-111">Key/Index</span></span></th>
<th><span data-ttu-id="db0bc-112">Сведения</span><span class="sxs-lookup"><span data-stu-id="db0bc-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="db0bc-113"><strong>McuId</strong></span><span class="sxs-lookup"><span data-stu-id="db0bc-113"><strong>McuId</strong></span></span></p></td>
<td><p><span data-ttu-id="db0bc-114">целое</span><span class="sxs-lookup"><span data-stu-id="db0bc-114">int</span></span></p></td>
<td><p><span data-ttu-id="db0bc-115">Primary</span><span class="sxs-lookup"><span data-stu-id="db0bc-115">Primary</span></span></p></td>
<td><p><span data-ttu-id="db0bc-116">Уникальный номер, идентифицирующий этот сервер конференц-связи.</span><span class="sxs-lookup"><span data-stu-id="db0bc-116">Unique number identifying this conferencing server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db0bc-117"><strong>McuUri</strong></span><span class="sxs-lookup"><span data-stu-id="db0bc-117"><strong>McuUri</strong></span></span></p></td>
<td><p><span data-ttu-id="db0bc-118">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="db0bc-118">nvarchar(450)</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db0bc-119"><strong>McuTypeId</strong></span><span class="sxs-lookup"><span data-stu-id="db0bc-119"><strong>McuTypeId</strong></span></span></p></td>
<td><p><span data-ttu-id="db0bc-120">inyint</span><span class="sxs-lookup"><span data-stu-id="db0bc-120">inyint</span></span></p></td>
<td><p> <span data-ttu-id="db0bc-121">Другом</span><span class="sxs-lookup"><span data-stu-id="db0bc-121">Foreign</span></span></p></td>
<td><p><span data-ttu-id="db0bc-122">Тип сервера конференций, например conf: Chat (для мгновенных сообщений) или conf: аудио-видео.</span><span class="sxs-lookup"><span data-stu-id="db0bc-122">Conferencing server type, such as conf:chat (for IMs) or conf:audio-video.</span></span> <span data-ttu-id="db0bc-123">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-uritypes-table.md">таблицей UriTypes в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="db0bc-123">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="db0bc-124">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="db0bc-124">


</div>

<span> </span>

</div>

</div>

</span></span></div>

