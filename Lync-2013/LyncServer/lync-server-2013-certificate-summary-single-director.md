---
title: 'Lync Server 2013: сводка по сертификатам — единственный директор'
description: 'Lync Server 2013: сведения о сертификате — едином начальнике.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate summary - Single Director
ms:assetid: 1b769a76-cbf3-46e9-a955-f6cde5faff93
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204720(v=OCS.15)
ms:contentKeyID: 48183546
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4cf930a73d9989ec44f52f1d70ee9e0f900e4d6f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435196"
---
# <a name="certificate-summary---single-director-in-lync-server-2013"></a><span data-ttu-id="a2473-103">Сводка по сертификатам — единственный директор в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a2473-103">Certificate summary - Single Director in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a2473-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a2473-104">

<span> </span></span></span>

<span data-ttu-id="a2473-105">_**Тема последнего изменения:** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="a2473-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="a2473-106">Требования к сертификатам для единого директора состоят из сертификата по умолчанию, который содержит имя субъекта и другие имена тем для служб, которые может получать руководитель.</span><span class="sxs-lookup"><span data-stu-id="a2473-106">Certificate requirements for a single Director consist of a default certificate that has a subject name and subject alternative names for services that the Director can receive.</span></span> <span data-ttu-id="a2473-107">Кроме того, существует сертификат маркера OAuth для проверки подлинности сервера и сервера.</span><span class="sxs-lookup"><span data-stu-id="a2473-107">Additionally, there is an OAuth Token certificate for server to server authentication purposes.</span></span>

### <a name="certificates-for-director"></a><span data-ttu-id="a2473-108">Сертификаты для режиссера</span><span class="sxs-lookup"><span data-stu-id="a2473-108">Certificates for Director</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a2473-109">Компонент</span><span class="sxs-lookup"><span data-stu-id="a2473-109">Component</span></span></th>
<th><span data-ttu-id="a2473-110">Имя субъекта (SN)</span><span class="sxs-lookup"><span data-stu-id="a2473-110">Subject name (SN)</span></span></th>
<th><span data-ttu-id="a2473-111">Дополнительные имена субъектов (SAN)</span><span class="sxs-lookup"><span data-stu-id="a2473-111">Subject alternative names (SAN)</span></span></th>
<th><span data-ttu-id="a2473-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a2473-112">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a2473-113">"Default" (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a2473-113">Default</span></span></p></td>
<td><p><span data-ttu-id="a2473-114">dir01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="a2473-114">dir01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="a2473-115">dir01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="a2473-115">dir01.contoso.net</span></span></p>
<p><span data-ttu-id="a2473-116">dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="a2473-116">dialin.contoso.com</span></span></p>
<p><span data-ttu-id="a2473-117">meet.contoso.com</span><span class="sxs-lookup"><span data-stu-id="a2473-117">meet.contoso.com</span></span></p>
<p><span data-ttu-id="a2473-118">lyncdiscoverinternal.contoso.com</span><span class="sxs-lookup"><span data-stu-id="a2473-118">lyncdiscoverinternal.contoso.com</span></span></p>
<p><span data-ttu-id="a2473-119">lyncdiscover.contoso.com</span><span class="sxs-lookup"><span data-stu-id="a2473-119">lyncdiscover.contoso.com</span></span></p>
<p><span data-ttu-id="a2473-120">(Необязательно) \*. contoso.com</span><span class="sxs-lookup"><span data-stu-id="a2473-120">(Optionally) \*.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="a2473-121">Сертификаты в службе каталогов могут запрашиваться либо с помощью внутреннего управляемого центра сертификации (ЦС), либо из общедоступного центра сертификации.</span><span class="sxs-lookup"><span data-stu-id="a2473-121">Director certificates can be requested from either an internally managed certification authority (CA) or from a public CA.</span></span></p>
<p><span data-ttu-id="a2473-122">Режиссер отвечает на запросы на обратных прокси-серверах периметра или пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="a2473-122">The Director responds to requests from the reverse proxy in the perimeter or from the Edge Server.</span></span> <span data-ttu-id="a2473-123">Внутренние клиенты не будут использовать режиссер.</span><span class="sxs-lookup"><span data-stu-id="a2473-123">Internal clients will not use the Director.</span></span></p>
<p><span data-ttu-id="a2473-124">Или подстановочный знак для простых URL-адресов</span><span class="sxs-lookup"><span data-stu-id="a2473-124">Or, a wildcard entry for the simple URLs</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2473-125">OAuthTokenIssuer</span><span class="sxs-lookup"><span data-stu-id="a2473-125">OAuthTokenIssuer</span></span></p></td>
<td><p><span data-ttu-id="a2473-126">dir01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="a2473-126">dir01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="a2473-127">Нет записи</span><span class="sxs-lookup"><span data-stu-id="a2473-127">No Entry</span></span></p></td>
<td><div>

> [!IMPORTANT]  
> <span data-ttu-id="a2473-128">Обратите внимание, что минимальная длина ключа составляет 1024, но вы можете получить предупреждение о том, что минимальная рекомендуемая длина ключа составляет 2048 бит.</span><span class="sxs-lookup"><span data-stu-id="a2473-128">Note that the minimum key length is 1024, but you may receive a warning that the minimum recommended key length is 2048 bits.</span></span>


</div>
<p><span data-ttu-id="a2473-129">Сертификат OAuthTokenIssuer является однозначным сертификатом для серверов с проверкой подлинности в крупномасштабной среде и может запрашиваться из внутреннего или общедоступного ЦС.</span><span class="sxs-lookup"><span data-stu-id="a2473-129">The OAuthTokenIssuer certificate is a single-purpose certificate for the purpose of authenticating servers in a large-scale environment, and can be requested from an internal CA or from a public CA.</span></span> <span data-ttu-id="a2473-130">Требуется сертификат.</span><span class="sxs-lookup"><span data-stu-id="a2473-130">The certificate is required.</span></span></p><span data-ttu-id="a2473-131"></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a2473-131"></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span></span></div>

