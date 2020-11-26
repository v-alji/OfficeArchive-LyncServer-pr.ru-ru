---
title: 'Lync Server 2013: сводка по сертификатам — балансировка нагрузки на DNS и аппаратная балансировка нагрузки'
description: 'Lync Server 2013: сведения о сертификате — DNS и HLB балансировка нагрузки.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate summary - DNS and HLB load balanced
ms:assetid: 8318a1a4-b423-47b7-95e6-9541adfad391
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205047(v=OCS.15)
ms:contentKeyID: 48184676
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 97a89975af16b6e39625677f787d3726f00c76c1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435322"
---
# <a name="certificate-summary---dns-and-hlb-load-balanced-in-lync-server-2013"></a><span data-ttu-id="9ee7d-103">Сводка по сертификатам — балансировка нагрузки на DNS и аппаратная балансировка нагрузки в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9ee7d-103">Certificate summary - DNS and HLB load balanced in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9ee7d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9ee7d-104">

<span> </span></span></span>

<span data-ttu-id="9ee7d-105">_**Тема последнего изменения:** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="9ee7d-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="9ee7d-106">Требования к сертификатам для режиссера с балансировкой нагрузки DNS и аппаратной подсистемой балансировки нагрузки будут использовать сертификат по умолчанию с именем субъекта и дополнительными именами для служб, которые может получать руководитель.</span><span class="sxs-lookup"><span data-stu-id="9ee7d-106">Certificate requirements for a Director with DNS load balancing and a hardware load balancer will use a default certificate that has a subject name and subject alternative names for services that the Director can receive.</span></span> <span data-ttu-id="9ee7d-107">Для каждого режиссера в пуле запрашивается сертификат.</span><span class="sxs-lookup"><span data-stu-id="9ee7d-107">A certificate is requested for each Director in the pool.</span></span> <span data-ttu-id="9ee7d-108">Важно помнить, что подсистема балансировки нагрузки аппаратных средств обеспечивает балансировку нагрузки только трафик из обратного прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="9ee7d-108">It is important to remember that the hardware load balancer is load balancing only the traffic from the reverse proxy.</span></span> <span data-ttu-id="9ee7d-109">Кроме того, существует сертификат маркеров OAuth для проверки подлинности сервера и сервера, установленный на каждом сервере.</span><span class="sxs-lookup"><span data-stu-id="9ee7d-109">Additionally, there is an OAuth Token certificate for server to server authentication purposes that is installed on each server.</span></span>

### <a name="certificates-for-director"></a><span data-ttu-id="9ee7d-110">Сертификаты для режиссера</span><span class="sxs-lookup"><span data-stu-id="9ee7d-110">Certificates for Director</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9ee7d-111">Компонент</span><span class="sxs-lookup"><span data-stu-id="9ee7d-111">Component</span></span></th>
<th><span data-ttu-id="9ee7d-112">Имя субъекта (SN)</span><span class="sxs-lookup"><span data-stu-id="9ee7d-112">Subject name (SN)</span></span></th>
<th><span data-ttu-id="9ee7d-113">Дополнительные имена субъектов (SAN)</span><span class="sxs-lookup"><span data-stu-id="9ee7d-113">Subject alternative names (SAN)</span></span></th>
<th><span data-ttu-id="9ee7d-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9ee7d-114">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9ee7d-115">"Default" (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9ee7d-115">Default</span></span></p></td>
<td><p><span data-ttu-id="9ee7d-116">dirpool01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="9ee7d-116">dirpool01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="9ee7d-117">dirpool01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="9ee7d-117">dirpool01.contoso.net</span></span></p>
<p><span data-ttu-id="9ee7d-118">dir01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="9ee7d-118">dir01.contoso.net</span></span></p>
<p><span data-ttu-id="9ee7d-119">dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="9ee7d-119">dialin.contoso.com</span></span></p>
<p><span data-ttu-id="9ee7d-120">meet.contoso.com</span><span class="sxs-lookup"><span data-stu-id="9ee7d-120">meet.contoso.com</span></span></p>
<p><span data-ttu-id="9ee7d-121">lyncdiscoverinternal.contoso.com</span><span class="sxs-lookup"><span data-stu-id="9ee7d-121">lyncdiscoverinternal.contoso.com</span></span></p>
<p><span data-ttu-id="9ee7d-122">lyncdiscover.contoso.com</span><span class="sxs-lookup"><span data-stu-id="9ee7d-122">lyncdiscover.contoso.com</span></span></p>
<p><span data-ttu-id="9ee7d-123">(Необязательно) \*. contoso.com</span><span class="sxs-lookup"><span data-stu-id="9ee7d-123">(Optionally) \*.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="9ee7d-124">Сертификаты в службе каталогов могут запрашиваться либо с помощью внутреннего управляемого центра сертификации (ЦС), либо из общедоступного центра сертификации.</span><span class="sxs-lookup"><span data-stu-id="9ee7d-124">Director certificates can be requested from either an internally managed certification authority (CA) or from a public CA.</span></span></p>
<p><span data-ttu-id="9ee7d-125">Режиссер отвечает на запросы на обратных прокси-серверах периметра или пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="9ee7d-125">The Director responds to requests from the reverse proxy in the perimeter or from the Edge Server.</span></span> <span data-ttu-id="9ee7d-126">Внутренние клиенты не будут использовать режиссер.</span><span class="sxs-lookup"><span data-stu-id="9ee7d-126">Internal clients will not use the Director.</span></span></p>
<p><span data-ttu-id="9ee7d-127">Или подстановочный знак для простых URL-адресов</span><span class="sxs-lookup"><span data-stu-id="9ee7d-127">Or, a wildcard entry for the simple URLs</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ee7d-128">OAuthTokenIssuer</span><span class="sxs-lookup"><span data-stu-id="9ee7d-128">OAuthTokenIssuer</span></span></p></td>
<td><p><span data-ttu-id="9ee7d-129">dir01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="9ee7d-129">dir01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="9ee7d-130">Нет записи</span><span class="sxs-lookup"><span data-stu-id="9ee7d-130">No Entry</span></span></p></td>
<td><div>

> [!IMPORTANT]  
> <span data-ttu-id="9ee7d-131">Обратите внимание, что минимальная длина ключа составляет 1024, но вы можете получить предупреждение о том, что минимальная рекомендуемая длина ключа составляет 2048 бит.</span><span class="sxs-lookup"><span data-stu-id="9ee7d-131">Note that the minimum key length is 1024, but you may receive a warning that the minimum recommended key length is 2048 bits.</span></span>


</div>
<p><span data-ttu-id="9ee7d-132">Сертификат OAuthTokenIssuer является однозначным сертификатом для серверов с проверкой подлинности в крупномасштабной среде и может запрашиваться из внутреннего или общедоступного ЦС.</span><span class="sxs-lookup"><span data-stu-id="9ee7d-132">The OAuthTokenIssuer certificate is a single-purpose certificate for the purpose of authenticating servers in a large-scale environment, and can be requested from an internal CA or from a public CA.</span></span> <span data-ttu-id="9ee7d-133">Требуется сертификат.</span><span class="sxs-lookup"><span data-stu-id="9ee7d-133">The certificate is required.</span></span></p><span data-ttu-id="9ee7d-134"></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9ee7d-134"></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span></span></div>

