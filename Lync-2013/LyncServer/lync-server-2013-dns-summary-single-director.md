---
title: 'Lync Server 2013: сводка по DNS — единственный директор'
description: 'Lync Server 2013: Общие сведения о DNS — единый режиссер.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS summary - Single Director
ms:assetid: 790ecb56-92cd-41f4-baf6-c290a707aa4d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205021(v=OCS.15)
ms:contentKeyID: 48184568
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 78ef19383df45644ad951ca5da69ef893b231980
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49397939"
---
# <a name="dns-summary---single-director-in-lync-server-2013"></a><span data-ttu-id="1d574-103">Сводка по DNS — единственный директор в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1d574-103">DNS summary - Single Director in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1d574-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1d574-104">

<span> </span></span></span>

<span data-ttu-id="1d574-105">_**Тема последнего изменения:** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="1d574-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="1d574-106">В таблице ниже приведены основные сведения о DNS-записях, которые необходимы для поддержки единого директора.</span><span class="sxs-lookup"><span data-stu-id="1d574-106">The following table contains a summary of the DNS records that are required to support the single Director.</span></span> <span data-ttu-id="1d574-107">Роль режиссера требует наличия аналогичных записей DNS в качестве внешнего сервера.</span><span class="sxs-lookup"><span data-stu-id="1d574-107">The role of the Director requires similar DNS records as the Front End Server.</span></span> <span data-ttu-id="1d574-108">Количество необходимых записей отражается в альтернативных именах тем, необходимых для вашего сертификата в директории.</span><span class="sxs-lookup"><span data-stu-id="1d574-108">The number of records needed is reflected in the subject alternative names required on the Director certificate.</span></span> <span data-ttu-id="1d574-109">На сервере переднего плана не размещается учетные записи пользователей и не размещается служба Mobility Service.</span><span class="sxs-lookup"><span data-stu-id="1d574-109">Different from the Front End Server, the Director does not host user accounts or host the Mobility Services.</span></span>

### <a name="dns-records-required-for-the-director"></a><span data-ttu-id="1d574-110">DNS-записи, необходимые для режиссера</span><span class="sxs-lookup"><span data-stu-id="1d574-110">DNS Records Required for the Director</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1d574-111">Расположение/тип/порт</span><span class="sxs-lookup"><span data-stu-id="1d574-111">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="1d574-112">Полное доменное имя/DNS-запись</span><span class="sxs-lookup"><span data-stu-id="1d574-112">FQDN/DNS Record</span></span></th>
<th><span data-ttu-id="1d574-113">IP-адрес или полное доменное имя</span><span class="sxs-lookup"><span data-stu-id="1d574-113">IP Address/FQDN</span></span></th>
<th><span data-ttu-id="1d574-114">Карты и примечания</span><span class="sxs-lookup"><span data-stu-id="1d574-114">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1d574-115">Внутренняя DNS/A</span><span class="sxs-lookup"><span data-stu-id="1d574-115">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="1d574-116">dir01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="1d574-116">dir01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="1d574-117">Директор</span><span class="sxs-lookup"><span data-stu-id="1d574-117">Director</span></span></p></td>
<td><p><span data-ttu-id="1d574-118">Запись узла директора, используемая для репликации и сервера на сервер</span><span class="sxs-lookup"><span data-stu-id="1d574-118">Director host record used for replication and server to server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d574-119">Внутренняя DNS/A</span><span class="sxs-lookup"><span data-stu-id="1d574-119">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="1d574-120">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="1d574-120">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="1d574-121">Директор</span><span class="sxs-lookup"><span data-stu-id="1d574-121">Director</span></span></p></td>
<td><p><span data-ttu-id="1d574-122">Протокол SIP из внутреннего интерфейса Edge-сервера</span><span class="sxs-lookup"><span data-stu-id="1d574-122">Inbound session initiation protocol (SIP) from the internal Edge interface of the Edge Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d574-123">Внутренняя DNS/A</span><span class="sxs-lookup"><span data-stu-id="1d574-123">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="1d574-124">dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="1d574-124">dialin.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="1d574-125">Директор</span><span class="sxs-lookup"><span data-stu-id="1d574-125">Director</span></span></p></td>
<td><p><span data-ttu-id="1d574-126">Опубликованные веб-службы телефонной связи из обратного прокси</span><span class="sxs-lookup"><span data-stu-id="1d574-126">Published dialin web services from reverse proxy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d574-127">Внутренняя DNS/A</span><span class="sxs-lookup"><span data-stu-id="1d574-127">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="1d574-128">meet.contoso.com</span><span class="sxs-lookup"><span data-stu-id="1d574-128">meet.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="1d574-129">Директор</span><span class="sxs-lookup"><span data-stu-id="1d574-129">Director</span></span></p></td>
<td><p><span data-ttu-id="1d574-130">Опубликованные веб-службы в обратном прокси</span><span class="sxs-lookup"><span data-stu-id="1d574-130">Published meet web services from reverse proxy</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d574-131">Внутренняя DNS/A</span><span class="sxs-lookup"><span data-stu-id="1d574-131">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="1d574-132">webdirexternal.contoso.com</span><span class="sxs-lookup"><span data-stu-id="1d574-132">webdirexternal.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="1d574-133">Директор</span><span class="sxs-lookup"><span data-stu-id="1d574-133">Director</span></span></p></td>
<td><p><span data-ttu-id="1d574-134">Опубликовано и определено в обратном веб-службах External Web Ticket для режиссера.</span><span class="sxs-lookup"><span data-stu-id="1d574-134">Published and defined by the reverse proxy Web Ticket external web services for the Director</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="1d574-135">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1d574-135">


</div>

<span> </span>

</div>

</div>

</span></span></div>

