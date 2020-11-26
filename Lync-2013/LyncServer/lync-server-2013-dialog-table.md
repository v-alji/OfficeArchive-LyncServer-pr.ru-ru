---
title: 'Lync Server 2013: таблица Dialog'
description: 'Lync Server 2013: таблица диалоговых окон.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Dialog table
ms:assetid: 4d93424f-9072-43f5-83c2-3d539e3e9ca6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398313(v=OCS.15)
ms:contentKeyID: 48184068
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7ae93b8ca9f1146b7dc164803f27cbeeadc66777
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429205"
---
# <a name="dialog-table-in-lync-server-2013"></a><span data-ttu-id="8ae4a-103">Таблица Dialog в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8ae4a-103">Dialog table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8ae4a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8ae4a-104">

<span> </span></span></span>

<span data-ttu-id="8ae4a-105">_**Тема последнего изменения:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="8ae4a-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="8ae4a-106">Диалоговая таблица — это вспомогательная таблица; Каждая запись отображает диалоговое окно протокола SIP.</span><span class="sxs-lookup"><span data-stu-id="8ae4a-106">The Dialog table is a supporting table; each record represents one Session Initiation Protocol (SIP) dialog.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8ae4a-107"><strong>Столбец</strong></span><span class="sxs-lookup"><span data-stu-id="8ae4a-107"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="8ae4a-108"><strong>Тип данных</strong></span><span class="sxs-lookup"><span data-stu-id="8ae4a-108"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="8ae4a-109"><strong>Ключ/индекс</strong></span><span class="sxs-lookup"><span data-stu-id="8ae4a-109"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="8ae4a-110"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="8ae4a-110"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8ae4a-111"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="8ae4a-111"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="8ae4a-112">datetime</span><span class="sxs-lookup"><span data-stu-id="8ae4a-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="8ae4a-113">Primary</span><span class="sxs-lookup"><span data-stu-id="8ae4a-113">Primary</span></span></p></td>
<td><p><span data-ttu-id="8ae4a-114">Время, когда агент качества (QoE) получает первый отчет от вызывающего или вызываемого абонента.</span><span class="sxs-lookup"><span data-stu-id="8ae4a-114">Time when the Quality of Excellence (QoE) agent receives the first report from either caller or callee.</span></span> <span data-ttu-id="8ae4a-115">Используется в сочетании с SessionSeq для уникальной идентификации сеанса.</span><span class="sxs-lookup"><span data-stu-id="8ae4a-115">Used in conjunction with SessionSeq to uniquely identify a session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ae4a-116"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="8ae4a-116"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="8ae4a-117">целое</span><span class="sxs-lookup"><span data-stu-id="8ae4a-117">int</span></span></p></td>
<td><p><span data-ttu-id="8ae4a-118">Primary</span><span class="sxs-lookup"><span data-stu-id="8ae4a-118">Primary</span></span></p></td>
<td><p><span data-ttu-id="8ae4a-119">Порядковый номер, чтобы отличать сеансы связи с одинаковым ConferenceDateTime.</span><span class="sxs-lookup"><span data-stu-id="8ae4a-119">Sequence number to differentiate sessions when they have the same ConferenceDateTime.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ae4a-120"><strong>DialogID</strong></span><span class="sxs-lookup"><span data-stu-id="8ae4a-120"><strong>DialogID</strong></span></span></p></td>
<td><p><span data-ttu-id="8ae4a-121">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="8ae4a-121">varchar(256)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="8ae4a-122">ИДЕНТИФИКАТОР диалогового окна, который является глобально уникальным.</span><span class="sxs-lookup"><span data-stu-id="8ae4a-122">Dialog ID which is globally unique.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ae4a-123"><strong>DialogIDChecksum</strong></span><span class="sxs-lookup"><span data-stu-id="8ae4a-123"><strong>DialogIDChecksum</strong></span></span></p></td>
<td><p><span data-ttu-id="8ae4a-124">целое</span><span class="sxs-lookup"><span data-stu-id="8ae4a-124">int</span></span></p></td>
<td><p><span data-ttu-id="8ae4a-125">индекса</span><span class="sxs-lookup"><span data-stu-id="8ae4a-125">index</span></span></p></td>
<td><p><span data-ttu-id="8ae4a-126">Контрольная сумма идентификатора диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="8ae4a-126">Checksum of the Dialog ID.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="8ae4a-127">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8ae4a-127">


</div>

<span> </span>

</div>

</div>

</span></span></div>

