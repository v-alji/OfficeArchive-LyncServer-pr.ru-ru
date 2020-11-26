---
title: 'Lync Server 2013: сводка по DNS — масштабируемый пул директоров, аппаратный балансировщик нагрузки'
description: 'Lync Server 2013: сводный пул DNS, масштабируемый с масштабированием, подсистема балансировки нагрузки для оборудования.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS summary - Scaled Director pool, hardware load balancer
ms:assetid: 08ba48e6-bfa1-4ab0-bc89-d58ddb9c20af
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204655(v=OCS.15)
ms:contentKeyID: 48183340
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7198e6a97feed8ce70cb16753ad1f21d58ef246c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428995"
---
# <a name="dns-summary---scaled-director-pool-hardware-load-balancer-in-lync-server-2013"></a><span data-ttu-id="a1c85-103">Сводка по DNS — масштабируемый пул директоров, аппаратный балансировщик нагрузки в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a1c85-103">DNS summary - Scaled Director pool, hardware load balancer in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a1c85-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a1c85-104">

<span> </span></span></span>

<span data-ttu-id="a1c85-105">_**Тема последнего изменения:** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="a1c85-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="a1c85-106">В таблице ниже приведены сведения о DNS-записях, которые необходимы для работы директора аппаратной балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a1c85-106">The following table contains a summary of the DNS records that are required to support the hardware load balanced Director.</span></span> <span data-ttu-id="a1c85-107">Роль режиссера требует наличия аналогичных записей DNS в качестве внешнего сервера.</span><span class="sxs-lookup"><span data-stu-id="a1c85-107">The role of the Director requires similar DNS records as the Front End Server.</span></span> <span data-ttu-id="a1c85-108">Количество необходимых записей отражается в альтернативных именах тем, необходимых для вашего сертификата в директории.</span><span class="sxs-lookup"><span data-stu-id="a1c85-108">The number of records needed is reflected in the subject alternative names required on the Director certificate.</span></span> <span data-ttu-id="a1c85-109">На сервере переднего плана не размещается учетные записи пользователей и не размещается служба Mobility Service.</span><span class="sxs-lookup"><span data-stu-id="a1c85-109">Different from the Front End Server, the Director pool does not host user accounts or host the Mobility Services.</span></span>

### <a name="dns-records-required-for-the-director-pool-using-a-hardware-load-balancer-and-dns-load-balancing"></a><span data-ttu-id="a1c85-110">DNS-записи, необходимые для пула режиссеров с помощью аппаратной подсистемы балансировки нагрузки и балансировки нагрузки DNS</span><span class="sxs-lookup"><span data-stu-id="a1c85-110">DNS Records Required for the Director pool using a Hardware Load Balancer and DNS Load Balancing</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a1c85-111">Расположение/тип/порт</span><span class="sxs-lookup"><span data-stu-id="a1c85-111">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="a1c85-112">Полное доменное имя/DNS-запись</span><span class="sxs-lookup"><span data-stu-id="a1c85-112">FQDN/DNS Record</span></span></th>
<th><span data-ttu-id="a1c85-113">IP-адрес или полное доменное имя</span><span class="sxs-lookup"><span data-stu-id="a1c85-113">IP Address/FQDN</span></span></th>
<th><span data-ttu-id="a1c85-114">Карты и примечания</span><span class="sxs-lookup"><span data-stu-id="a1c85-114">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a1c85-115">Внутренняя DNS/A</span><span class="sxs-lookup"><span data-stu-id="a1c85-115">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="a1c85-116">dir01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="a1c85-116">dir01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="a1c85-117">Директор</span><span class="sxs-lookup"><span data-stu-id="a1c85-117">Director</span></span></p></td>
<td><p><span data-ttu-id="a1c85-118">Запись узла директора, используемая для связи между репликацией и сервером</span><span class="sxs-lookup"><span data-stu-id="a1c85-118">Director host record used for replication and server to server communication</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1c85-119">Внутренняя DNS/A</span><span class="sxs-lookup"><span data-stu-id="a1c85-119">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="a1c85-120">dirpool01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="a1c85-120">dirpool01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="a1c85-121">Пул HLBных ВИРТУАЛЬНЫХ каталогов</span><span class="sxs-lookup"><span data-stu-id="a1c85-121">Director pool HLB VIP</span></span></p></td>
<td><p><span data-ttu-id="a1c85-122">Запись Host для пула пулов балансировки нагрузки DNS</span><span class="sxs-lookup"><span data-stu-id="a1c85-122">Host record for the DNS load balanced Director pool</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1c85-123">Внутренняя DNS/A</span><span class="sxs-lookup"><span data-stu-id="a1c85-123">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="a1c85-124">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="a1c85-124">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="a1c85-125">Пул HLBных ВИРТУАЛЬНЫХ каталогов</span><span class="sxs-lookup"><span data-stu-id="a1c85-125">Director pool HLB VIP</span></span></p></td>
<td><p><span data-ttu-id="a1c85-126">Протокол SIP, входящий в внутренний интерфейс пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="a1c85-126">Inbound session initiation protocol (SIP) from the internal interface of the Edge Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1c85-127">Внутренняя DNS/A</span><span class="sxs-lookup"><span data-stu-id="a1c85-127">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="a1c85-128">dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="a1c85-128">dialin.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="a1c85-129">Пул HLBных ВИРТУАЛЬНЫХ каталогов</span><span class="sxs-lookup"><span data-stu-id="a1c85-129">Director pool HLB VIP</span></span></p></td>
<td><p><span data-ttu-id="a1c85-130">Подходящими для аппаратной балансировки нагрузки веб-службы, опубликованные из обратного прокси</span><span class="sxs-lookup"><span data-stu-id="a1c85-130">Hardware load balanced published dialin web services from reverse proxy</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1c85-131">Внутренняя DNS/A</span><span class="sxs-lookup"><span data-stu-id="a1c85-131">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="a1c85-132">meet.contoso.com</span><span class="sxs-lookup"><span data-stu-id="a1c85-132">meet.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="a1c85-133">Пул HLBных ВИРТУАЛЬНЫХ каталогов</span><span class="sxs-lookup"><span data-stu-id="a1c85-133">Director pool HLB VIP</span></span></p></td>
<td><p><span data-ttu-id="a1c85-134">Служба балансировки нагрузки для оборудования, опубликованная в соответствии с обратной прокси-сервером</span><span class="sxs-lookup"><span data-stu-id="a1c85-134">Hardware load balanced published meet web services from reverse proxy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1c85-135">Внутренняя DNS/A</span><span class="sxs-lookup"><span data-stu-id="a1c85-135">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="a1c85-136">webdirexternal.contoso.com</span><span class="sxs-lookup"><span data-stu-id="a1c85-136">webdirexternal.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="a1c85-137">Пул HLBных ВИРТУАЛЬНЫХ каталогов</span><span class="sxs-lookup"><span data-stu-id="a1c85-137">Director pool HLB VIP</span></span></p></td>
<td><p><span data-ttu-id="a1c85-138">Балансировка нагрузки для оборудования, опубликованная и определяемая внешними веб-службами обратного прокси, для директора пула</span><span class="sxs-lookup"><span data-stu-id="a1c85-138">Hardware load balanced published and defined by the reverse proxy Web Ticket external web services for the Director pool</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="a1c85-139">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a1c85-139">


</div>

<span> </span>

</div>

</div>

</span></span></div>

