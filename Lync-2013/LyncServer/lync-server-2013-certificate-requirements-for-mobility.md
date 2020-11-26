---
title: 'Lync Server 2013: требования к сертификатам для организации мобильной работы'
description: 'Lync Server 2013: требования к сертификату для мобильных устройств.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate requirements for mobility
ms:assetid: bb0e97af-cf60-4271-a0ab-654429d884ea
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690044(v=OCS.15)
ms:contentKeyID: 48185251
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 51af74b3efc1ffcb4fe38d7431e315f9b55af943
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435364"
---
# <a name="certificate-requirements-for-mobility-in-lync-server-2013"></a><span data-ttu-id="e87f8-103">Требования к сертификатам для организации мобильной работы в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e87f8-103">Certificate requirements for mobility in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e87f8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e87f8-104">

<span> </span></span></span>

<span data-ttu-id="e87f8-105">_**Тема последнего изменения:** 2012-06-24_</span><span class="sxs-lookup"><span data-stu-id="e87f8-105">_**Topic Last Modified:** 2012-06-24_</span></span>

<span data-ttu-id="e87f8-106">Если вы разворачиваете мобильное устройство и поддерживаете автоматическое обнаружение для мобильных клиентов, необходимо включить некоторые записи альтернативных имен для субъектов в сертификаты для обеспечения защищенных подключений из мобильных клиентов.</span><span class="sxs-lookup"><span data-stu-id="e87f8-106">If you deploy the mobility feature and support automatic discovery for mobile clients, you need to include certain subject alternative name entries on certificates to support secure connections from the mobile clients.</span></span>

<span data-ttu-id="e87f8-107">Необходимо включить записи альтернативных имен для субъектов для автоматического обнаружения в следующих сертификатах:</span><span class="sxs-lookup"><span data-stu-id="e87f8-107">You need to include subject alternative name entries for automatic discovery on the following certificates:</span></span>

  - <span data-ttu-id="e87f8-108">Пул директоров</span><span class="sxs-lookup"><span data-stu-id="e87f8-108">Director pool</span></span>

  - <span data-ttu-id="e87f8-109">Пул переднего плана</span><span class="sxs-lookup"><span data-stu-id="e87f8-109">Front End pool</span></span>

  - <span data-ttu-id="e87f8-110">Сертификат обратного прокси-сервера</span><span class="sxs-lookup"><span data-stu-id="e87f8-110">Reverse proxy</span></span>

<span data-ttu-id="e87f8-111">В этом разделе описаны записи альтернативных имен субъектов, необходимые для сертификатов для автоматического обнаружения.</span><span class="sxs-lookup"><span data-stu-id="e87f8-111">This section describes the subject alternative name entries that are required on your certificates for automatic discovery.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="e87f8-112">Повторное выдача сертификатов с помощью внутреннего центра сертификации обычно является простым процессом, но добавление нескольких записей альтернативных имен субъектов в общедоступные сертификаты, используемые обратным прокси, может быть дорогостоящим.</span><span class="sxs-lookup"><span data-stu-id="e87f8-112">Reissuing certificates by using an internal certificate authority is typically a simple process, but adding multiple subject alternative name entries to public certificates used by the reverse proxy can be expensive.</span></span> <span data-ttu-id="e87f8-113">Если у вас много доменов SIP, что значительно затрудняет Добавление альтернативных имен субъектов, вы можете настроить обратный прокси так, чтобы он использовал HTTP для первоначального запроса на обслуживание автообнаружения, вместо использования HTTPS (конфигурация по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="e87f8-113">If you have many SIP domains, making the addition of subject alternative names very expensive, you can configure the reverse proxy to use HTTP for the initial Autodiscover Service request, instead of using HTTPS (the default configuration).</span></span> <span data-ttu-id="e87f8-114">Подробности можно найти <A href="lync-server-2013-technical-requirements-for-mobility.md">в разделе Технические требования для мобильных устройств на Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="e87f8-114">For details, see <A href="lync-server-2013-technical-requirements-for-mobility.md">Technical requirements for mobility in Lync Server 2013</A>.</span></span>



</div>

### <a name="director-pool-certificate-requirements"></a><span data-ttu-id="e87f8-115">Требования к сертификатам пула директоров</span><span class="sxs-lookup"><span data-stu-id="e87f8-115">Director Pool Certificate Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e87f8-116">Описание</span><span class="sxs-lookup"><span data-stu-id="e87f8-116">Description</span></span></th>
<th><span data-ttu-id="e87f8-117">Запись альтернативного имени субъекта</span><span class="sxs-lookup"><span data-stu-id="e87f8-117">Subject alternative name entry</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e87f8-118">URL-адрес внутренней службы автообнаружения</span><span class="sxs-lookup"><span data-stu-id="e87f8-118">Internal Autodiscover Service URL</span></span></p></td>
<td><p><span data-ttu-id="e87f8-119">SAN=lyncdiscoverinternal.&lt;домен_SIP&gt;</span><span class="sxs-lookup"><span data-stu-id="e87f8-119">SAN=lyncdiscoverinternal.&lt;sipdomain&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e87f8-120">Внешний URL-адрес службы автообнаружения</span><span class="sxs-lookup"><span data-stu-id="e87f8-120">External Autodiscover Service URL</span></span></p></td>
<td><p><span data-ttu-id="e87f8-121">SAN=lyncdiscover.&lt;домен_SIP&gt;</span><span class="sxs-lookup"><span data-stu-id="e87f8-121">SAN=lyncdiscover.&lt;sipdomain&gt;</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="e87f8-122">Кроме того, вы можете использовать сеть SAN = \*. &lt; sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="e87f8-122">Alternatively, you can use SAN=\*.&lt;sipdomain&gt;</span></span>



</div>

### <a name="front-end-pool-certificate-requirements"></a><span data-ttu-id="e87f8-123">Требования к сертификату пула переднего плана</span><span class="sxs-lookup"><span data-stu-id="e87f8-123">Front End Pool Certificate Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e87f8-124">Описание</span><span class="sxs-lookup"><span data-stu-id="e87f8-124">Description</span></span></th>
<th><span data-ttu-id="e87f8-125">Запись альтернативного имени субъекта</span><span class="sxs-lookup"><span data-stu-id="e87f8-125">Subject alternative name entry</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e87f8-126">URL-адрес внутренней службы автообнаружения</span><span class="sxs-lookup"><span data-stu-id="e87f8-126">Internal Autodiscover Service URL</span></span></p></td>
<td><p><span data-ttu-id="e87f8-127">SAN=lyncdiscoverinternal.&lt;домен_SIP&gt;</span><span class="sxs-lookup"><span data-stu-id="e87f8-127">SAN=lyncdiscoverinternal.&lt;sipdomain&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e87f8-128">Внешний URL-адрес службы автообнаружения</span><span class="sxs-lookup"><span data-stu-id="e87f8-128">External Autodiscover Service URL</span></span></p></td>
<td><p><span data-ttu-id="e87f8-129">SAN=lyncdiscover.&lt;домен_SIP&gt;</span><span class="sxs-lookup"><span data-stu-id="e87f8-129">SAN=lyncdiscover.&lt;sipdomain&gt;</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="e87f8-130">Кроме того, вы можете использовать сеть SAN = \*. &lt; sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="e87f8-130">Alternatively, you can use SAN=\*.&lt;sipdomain&gt;</span></span>



</div>

### <a name="reverse-proxy-public-ca-certificate-requirements"></a><span data-ttu-id="e87f8-131">Требования сертификата по обратному прокси (общедоступному центру сертификации)</span><span class="sxs-lookup"><span data-stu-id="e87f8-131">Reverse Proxy (Public CA) Certificate Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e87f8-132">Описание</span><span class="sxs-lookup"><span data-stu-id="e87f8-132">Description</span></span></th>
<th><span data-ttu-id="e87f8-133">Запись альтернативного имени субъекта</span><span class="sxs-lookup"><span data-stu-id="e87f8-133">Subject alternative name entry</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e87f8-134">Внешний URL-адрес службы автообнаружения</span><span class="sxs-lookup"><span data-stu-id="e87f8-134">External Autodiscover Service URL</span></span></p></td>
<td><p><span data-ttu-id="e87f8-135">SAN=lyncdiscover.&lt;домен_SIP&gt;</span><span class="sxs-lookup"><span data-stu-id="e87f8-135">SAN=lyncdiscover.&lt;sipdomain&gt;</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="e87f8-136">Вы назначаете эту сеть SAN сертификату, назначенному прослушивателю SSL на обратном прокси-сервере.</span><span class="sxs-lookup"><span data-stu-id="e87f8-136">You assign this SAN to the certificate assigned to the SSL Listener on the reverse proxy.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="e87f8-137">В обратном прослушивателе прокси-сервера будут указаны альтернативные имена для URL-адресов внешних веб-служб (например, SAN = lyncwebextpool01. contoso. com и dirwebexternal.contoso.com, если вы развернули дополнительный режиссер).</span><span class="sxs-lookup"><span data-stu-id="e87f8-137">Your reverse proxy listener will have subject alternative names for your external Web Services URL(s) (for example, SAN=lyncwebextpool01.contoso.com, and dirwebexternal.contoso.com if you have deployed the optional Director).</span></span>



<span data-ttu-id="e87f8-138"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e87f8-138"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

