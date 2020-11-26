---
title: 'Lync Server 2013: представление мультимедиа'
description: 'Lync Server 2013: представление "мультимедиа".'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Media view
ms:assetid: 1a7b2e59-082e-4188-98ae-48ae9bd3494a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687981(v=OCS.15)
ms:contentKeyID: 49733570
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 74643986b12a30b1055a46a37febf90eeb70c514
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446039"
---
# <a name="media-view-in-lync-server-2013"></a><span data-ttu-id="554e6-103">Представление мультимедиа в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="554e6-103">Media view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="554e6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="554e6-104">

<span> </span></span></span>

<span data-ttu-id="554e6-105">_**Тема последнего изменения:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="554e6-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="554e6-106">В представлении мультимедиа хранятся сведения о одном типе мультимедиа, используемом в одноранговых сеансах.</span><span class="sxs-lookup"><span data-stu-id="554e6-106">The Media view stores information about one media type used in a peer-to-peer session.</span></span> <span data-ttu-id="554e6-107">Один сеанс будет представлен в таблице несколькими записями, если используется более одного типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="554e6-107">One session would be represented by multiple records in the table, if more than one media type is used.</span></span> <span data-ttu-id="554e6-108">Это представление было представлено в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="554e6-108">This view was introduced in Microsoft Lync Server 2013.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="554e6-109">Представление мультимедиа не следует использовать для расчета длительности мультимедиа для сеанса.</span><span class="sxs-lookup"><span data-stu-id="554e6-109">The Media view should not be used to calculate the media duration for a session.</span></span> <span data-ttu-id="554e6-110">В этом представлении содержатся сведения о сигналах обмена мультимедийными данными в сеансе.</span><span class="sxs-lookup"><span data-stu-id="554e6-110">This view contains the signaling details of media exchange in a session.</span></span> <span data-ttu-id="554e6-111">Обмен мультимедийными данными выполняется запросом приглашения, а StartTime указывает время отправки приглашения. Время приглашения не обязательно означает время начала воспроизведения мультимедиа, так как средство мультимедиа запускается только после принятия сеанса.</span><span class="sxs-lookup"><span data-stu-id="554e6-111">Media exchange is done by the INVITE request, and StartTime indicates the time that the INVITE was sent out. The invite time does not necessarily mean the media start time, because media starts only after the session is accepted.</span></span>



</div>

<span data-ttu-id="554e6-112">В представлении мультимедиа содержатся все столбцы в [представлении SessionDetails в Lync Server 2013](lync-server-2013-sessiondetails-view.md) в дополнение к указанным ниже.</span><span class="sxs-lookup"><span data-stu-id="554e6-112">The Media view contains all of the columns in the [SessionDetails view in Lync Server 2013](lync-server-2013-sessiondetails-view.md) in addition the ones listed below.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="554e6-113">Столбец</span><span class="sxs-lookup"><span data-stu-id="554e6-113">Column</span></span></th>
<th><span data-ttu-id="554e6-114">Тип данных</span><span class="sxs-lookup"><span data-stu-id="554e6-114">Data Type</span></span></th>
<th><span data-ttu-id="554e6-115">Подробности</span><span class="sxs-lookup"><span data-stu-id="554e6-115">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="554e6-116"><strong>Media</strong></span><span class="sxs-lookup"><span data-stu-id="554e6-116"><strong>Media</strong></span></span></p></td>
<td><p><span data-ttu-id="554e6-117">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="554e6-117">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="554e6-118">Тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="554e6-118">Media type.</span></span> <span data-ttu-id="554e6-119">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-medialist-table.md">таблицей MediaList в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="554e6-119">See the <a href="lync-server-2013-medialist-table.md">MediaList table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="554e6-120"><strong>MediaStartTime</strong></span><span class="sxs-lookup"><span data-stu-id="554e6-120"><strong>MediaStartTime</strong></span></span></p></td>
<td><p><span data-ttu-id="554e6-121">datetime</span><span class="sxs-lookup"><span data-stu-id="554e6-121">datetime</span></span></p></td>
<td><p><span data-ttu-id="554e6-122">Время отправки запроса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="554e6-122">Time that a media request was sent out.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="554e6-123"><strong>MediaEndTime</strong></span><span class="sxs-lookup"><span data-stu-id="554e6-123"><strong>MediaEndTime</strong></span></span></p></td>
<td><p><span data-ttu-id="554e6-124">datetime</span><span class="sxs-lookup"><span data-stu-id="554e6-124">datetime</span></span></p></td>
<td><p><span data-ttu-id="554e6-125">Время окончания сеанса.</span><span class="sxs-lookup"><span data-stu-id="554e6-125">End time of the session.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="554e6-126">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="554e6-126">


</div>

<span> </span>

</div>

</div>

</span></span></div>

