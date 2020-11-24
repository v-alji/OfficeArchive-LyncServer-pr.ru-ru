---
title: Сводка по сертификатам — масштабированный пул директоров, аппаратный балансировщик нагрузки
description: Подсистема сертификата — масштабируемый режиссер, балансировщик аппаратной нагрузки.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate summary - Scaled Director pool, hardware load balancer
ms:assetid: 45940add-8027-418d-b79a-9033b494762f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204846(v=OCS.15)
ms:contentKeyID: 48183992
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 08abc37940cd41a29d6620cfc0a2a801de4a8e38
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399412"
---
# <a name="certificate-summary---scaled-director-pool-hardware-load-balancer-in-lync-server-2013"></a><span data-ttu-id="27067-103">Сводка по сертификатам — масштабированный пул директоров, аппаратный балансировщик нагрузки в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="27067-103">Certificate summary - Scaled Director pool, hardware load balancer in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="27067-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="27067-104">

<span> </span></span></span>

<span data-ttu-id="27067-105">_**Тема последнего изменения:** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="27067-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="27067-106">Требования к сертификатам для режиссера с помощью аппаратной подсистемы балансировки нагрузки будут использовать сертификат по умолчанию, который содержит имя субъекта и альтернативные имена субъектов для служб, которые может получать пул режиссера.</span><span class="sxs-lookup"><span data-stu-id="27067-106">Certificate requirements for a Director with a hardware load balancer will use a default certificate that has a subject name and subject alternative names for services that the Director pool can receive.</span></span> <span data-ttu-id="27067-107">Для каждого режиссера в пуле запрашивается сертификат.</span><span class="sxs-lookup"><span data-stu-id="27067-107">A certificate is requested for each Director in the pool.</span></span> <span data-ttu-id="27067-108">Кроме того, существует сертификат маркеров OAuth для проверки подлинности сервера и сервера, установленный на каждом сервере.</span><span class="sxs-lookup"><span data-stu-id="27067-108">Additionally there is an OAuth Token certificate for server to server authentication purposes that is installed on each server.</span></span>

### <a name="certificates-for-a-scaled-director-using-a-hardware-load-balancer"></a><span data-ttu-id="27067-109">Сертификаты для масштабированного директора с помощью аппаратной подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="27067-109">Certificates for a Scaled Director Using a Hardware Load Balancer</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="27067-110">Компонент</span><span class="sxs-lookup"><span data-stu-id="27067-110">Component</span></span></th>
<th><span data-ttu-id="27067-111">Имя субъекта (SN)</span><span class="sxs-lookup"><span data-stu-id="27067-111">Subject name (SN)</span></span></th>
<th><span data-ttu-id="27067-112">Дополнительные имена субъектов (SAN)</span><span class="sxs-lookup"><span data-stu-id="27067-112">Subject alternative names (SAN)</span></span></th>
<th><span data-ttu-id="27067-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="27067-113">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="27067-114">"Default" (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="27067-114">Default</span></span></p></td>
<td><p><span data-ttu-id="27067-115">dirpool01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="27067-115">dirpool01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="27067-116">dirpool01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="27067-116">dirpool01.contoso.net</span></span></p>
<p><span data-ttu-id="27067-117">dir01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="27067-117">dir01.contoso.net</span></span></p>
<p><span data-ttu-id="27067-118">dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="27067-118">dialin.contoso.com</span></span></p>
<p><span data-ttu-id="27067-119">meet.contoso.com</span><span class="sxs-lookup"><span data-stu-id="27067-119">meet.contoso.com</span></span></p>
<p><span data-ttu-id="27067-120">lyncdiscoverinternal.contoso.com</span><span class="sxs-lookup"><span data-stu-id="27067-120">lyncdiscoverinternal.contoso.com</span></span></p>
<p><span data-ttu-id="27067-121">lyncdiscover.contoso.com</span><span class="sxs-lookup"><span data-stu-id="27067-121">lyncdiscover.contoso.com</span></span></p>
<p><span data-ttu-id="27067-122">(Необязательно) \*. contoso.com</span><span class="sxs-lookup"><span data-stu-id="27067-122">(Optionally) \*.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="27067-123">Сертификаты в службе каталогов могут запрашиваться либо с помощью внутреннего управляемого центра сертификации (ЦС), либо из общедоступного центра сертификации.</span><span class="sxs-lookup"><span data-stu-id="27067-123">Director certificates can be requested from either an internally managed certification authority (CA) or from a public CA.</span></span></p>
<p><span data-ttu-id="27067-124">Режиссер отвечает на запросы на обратных прокси-серверах периметра или пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="27067-124">The Director responds to requests from the reverse proxy in the perimeter or from the Edge Server.</span></span></p>
<p><span data-ttu-id="27067-125">Или подстановочный знак для простых URL-адресов</span><span class="sxs-lookup"><span data-stu-id="27067-125">Or, a wildcard entry for the simple URLs</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27067-126">OAuthTokenIssuer</span><span class="sxs-lookup"><span data-stu-id="27067-126">OAuthTokenIssuer</span></span></p></td>
<td><p><span data-ttu-id="27067-127">dir01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="27067-127">dir01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="27067-128">Нет записи</span><span class="sxs-lookup"><span data-stu-id="27067-128">No Entry</span></span></p></td>
<td>


> [!IMPORTANT]
> <span data-ttu-id="27067-129">Обратите внимание, что минимальная длина ключа составляет 1024, но вы можете получить предупреждение о том, что минимальная рекомендуемая длина ключа составляет 2048 бит.</span><span class="sxs-lookup"><span data-stu-id="27067-129">Note that the minimum key length is 1024, but you may receive a warning that the minimum recommended key length is 2048 bits.</span></span>


<p><span data-ttu-id="27067-130">Сертификат OAuthTokenIssuer является однозначным сертификатом для серверов с проверкой подлинности в крупномасштабной среде и может запрашиваться из внутреннего или общедоступного ЦС.</span><span class="sxs-lookup"><span data-stu-id="27067-130">The OAuthTokenIssuer certificate is a single-purpose certificate for the purpose of authenticating servers in a large-scale environment, and can be requested from an internal CA or from a public CA.</span></span> <span data-ttu-id="27067-131">Требуется сертификат.</span><span class="sxs-lookup"><span data-stu-id="27067-131">The certificate is required.</span></span></p><span data-ttu-id="27067-132"></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="27067-132"></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span></span></div>

