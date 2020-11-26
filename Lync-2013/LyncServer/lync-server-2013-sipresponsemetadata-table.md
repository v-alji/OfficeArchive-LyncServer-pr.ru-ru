---
title: 'Lync Server 2013: таблица SIPResponseMetaData'
description: 'Таблица Lync Server 2013: SIPResponseMetaData.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: SIPResponseMetaData table
ms:assetid: cf723737-4a75-4352-829b-f4954aa59716
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205294(v=OCS.15)
ms:contentKeyID: 48185510
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 402cff331f81a9b46028d76de69deeaace8d5ae1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444625"
---
# <a name="sipresponsemetadata-table-in-lync-server-2013"></a><span data-ttu-id="0d9ab-103">Таблица SIPResponseMetaData в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0d9ab-103">SIPResponseMetaData table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0d9ab-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0d9ab-104">

<span> </span></span></span>

<span data-ttu-id="0d9ab-105">_**Тема последнего изменения:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="0d9ab-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="0d9ab-106">В SIPResponseMetaDataTable содержится список кодов ответов SIP, а также классификация и определение каждого из этих кодов.</span><span class="sxs-lookup"><span data-stu-id="0d9ab-106">The SIPResponseMetaDataTable contains a list of SIP response codes and the classification and definition of each of those codes.</span></span> <span data-ttu-id="0d9ab-107">Эти коды генерируются в ответ на события, влияющие на устройства SIP и сеансы связи SIP; Например, код ответа 403 генерируется, когда устройство SIP делает запрос, но сервер отклоняет этот запрос.</span><span class="sxs-lookup"><span data-stu-id="0d9ab-107">These codes are generated in response to events affecting SIP devices and SIP communication sessions; for example, the response code 403 is generated when a SIP device makes a request, but the server declines to honor that request.</span></span>

<span data-ttu-id="0d9ab-108">Эта таблица введена в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0d9ab-108">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0d9ab-109">Столбец</span><span class="sxs-lookup"><span data-stu-id="0d9ab-109">Column</span></span></th>
<th><span data-ttu-id="0d9ab-110">Тип данных</span><span class="sxs-lookup"><span data-stu-id="0d9ab-110">Data Type</span></span></th>
<th><span data-ttu-id="0d9ab-111">Ключ/индекс</span><span class="sxs-lookup"><span data-stu-id="0d9ab-111">Key/Index</span></span></th>
<th><span data-ttu-id="0d9ab-112">Сведения</span><span class="sxs-lookup"><span data-stu-id="0d9ab-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0d9ab-113"><strong>ResponseCode</strong></span><span class="sxs-lookup"><span data-stu-id="0d9ab-113"><strong>ResponseCode</strong></span></span></p></td>
<td><p><span data-ttu-id="0d9ab-114">целое</span><span class="sxs-lookup"><span data-stu-id="0d9ab-114">int</span></span></p></td>
<td><p><span data-ttu-id="0d9ab-115">Primary</span><span class="sxs-lookup"><span data-stu-id="0d9ab-115">Primary</span></span></p></td>
<td><p><span data-ttu-id="0d9ab-116">Числовое значение, представляющее код ответа SIP.</span><span class="sxs-lookup"><span data-stu-id="0d9ab-116">Numeric value that represents the SIP response code.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d9ab-117"><strong>Классов</strong></span><span class="sxs-lookup"><span data-stu-id="0d9ab-117"><strong>Class</strong></span></span></p></td>
<td><p><span data-ttu-id="0d9ab-118">целое</span><span class="sxs-lookup"><span data-stu-id="0d9ab-118">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0d9ab-119">Общая классификация для кода ответа.</span><span class="sxs-lookup"><span data-stu-id="0d9ab-119">General classification for the response code.</span></span> <span data-ttu-id="0d9ab-120">Существуют следующие классификации:</span><span class="sxs-lookup"><span data-stu-id="0d9ab-120">Classifications include:</span></span></p>
<ul>
<li><p><span data-ttu-id="0d9ab-121">1 — Информационные ответы</span><span class="sxs-lookup"><span data-stu-id="0d9ab-121">1 – Informational Responses</span></span></p></li>
<li><p><span data-ttu-id="0d9ab-122">2 – успешные ответы</span><span class="sxs-lookup"><span data-stu-id="0d9ab-122">2 – Successful Responses</span></span></p></li>
<li><p><span data-ttu-id="0d9ab-123">3 – Ответы на перенаправление</span><span class="sxs-lookup"><span data-stu-id="0d9ab-123">3 – Redirection Responses</span></span></p></li>
<li><p><span data-ttu-id="0d9ab-124">4 – Ответы на ошибки клиента</span><span class="sxs-lookup"><span data-stu-id="0d9ab-124">4 – Client Failure Responses</span></span></p></li>
<li><p><span data-ttu-id="0d9ab-125">5-Ответы на ошибки сервера</span><span class="sxs-lookup"><span data-stu-id="0d9ab-125">5 -- Server Failure Responses</span></span></p></li>
<li><p><span data-ttu-id="0d9ab-126">6 – Глобальный ответ на сбой</span><span class="sxs-lookup"><span data-stu-id="0d9ab-126">6 – Global Failure Response</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0d9ab-127"><strong>Описание</strong></span><span class="sxs-lookup"><span data-stu-id="0d9ab-127"><strong>Description</strong></span></span></p></td>
<td><p><span data-ttu-id="0d9ab-128">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="0d9ab-128">nvarchar(256)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0d9ab-129">Описание кода ответа SIP.</span><span class="sxs-lookup"><span data-stu-id="0d9ab-129">Description of the SIP response code.</span></span> <span data-ttu-id="0d9ab-130">Например, код ответа 181 имеет следующее описание:</span><span class="sxs-lookup"><span data-stu-id="0d9ab-130">For example, response code 181 has the following description:</span></span></p>
<p><span data-ttu-id="0d9ab-131">Переадресация звонка</span><span class="sxs-lookup"><span data-stu-id="0d9ab-131">Call Is Being Forwarded</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="0d9ab-132">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0d9ab-132">


</div>

<span> </span>

</div>

</div>

</span></span></div>

