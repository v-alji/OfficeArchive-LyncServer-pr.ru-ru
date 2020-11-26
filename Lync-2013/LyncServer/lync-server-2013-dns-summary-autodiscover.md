---
title: 'Lync Server 2013: сводка DNS — автообнаружение'
description: 'Lync Server 2013: сводка DNS — автообнаружения.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS summary - Autodiscover
ms:assetid: b336a2ae-0e58-4b74-b606-aedbbd411587
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945644(v=OCS.15)
ms:contentKeyID: 51541504
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: eef9bd6a2489561145718c7bbf2f710ab0b1f248
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429044"
---
# <a name="dns-summary---autodiscover-in-lync-server-2013"></a><span data-ttu-id="b3af0-103">Сводка DNS: обнаружение автообнаружения в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b3af0-103">DNS summary - Autodiscover in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b3af0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b3af0-104">

<span> </span></span></span>

<span data-ttu-id="b3af0-105">_**Тема последнего изменения:** 2013-02-13_</span><span class="sxs-lookup"><span data-stu-id="b3af0-105">_**Topic Last Modified:** 2013-02-13_</span></span>

<span data-ttu-id="b3af0-106">Автообнаружение — это гибкая служба, в которой она будет поддерживать связь по протоколу HTTP или HTTPS.</span><span class="sxs-lookup"><span data-stu-id="b3af0-106">Autodiscover is a flexible service in that it will accept communication over HTTP or HTTPS.</span></span> <span data-ttu-id="b3af0-107">Для этого необходимо правильно настроить систему доменных имен (DNS) и сертификаты, используемые серверами, на которых размещается служба автообнаружения.</span><span class="sxs-lookup"><span data-stu-id="b3af0-107">To accomplish this, the domain name system (DNS) and the certificates used by servers that host the Autodiscover service must be configured correctly.</span></span> <span data-ttu-id="b3af0-108">Требования к сертификатам описаны в статье [сведения о сертификате: обнаружение автообнаружения в Lync Server 2013](lync-server-2013-certificate-summary-autodiscover.md).</span><span class="sxs-lookup"><span data-stu-id="b3af0-108">Certificate requirements are covered in [Certificate summary - Autodiscover in Lync Server 2013](lync-server-2013-certificate-summary-autodiscover.md).</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="b3af0-109">Логика поиска DNS для клиентов Lync Server использует определенную последовательность разрешения.</span><span class="sxs-lookup"><span data-stu-id="b3af0-109">DNS lookup logic for the Lync Server clients uses a specific order of resolution.</span></span> <span data-ttu-id="b3af0-110">Всегда следует включать и lyncdiscoverinternal. &lt; Domain &gt; и lyncdiscover. &lt; домен &gt; в DNS.</span><span class="sxs-lookup"><span data-stu-id="b3af0-110">You should always include both the lyncdiscoverinternal.&lt;domain&gt; and the lyncdiscover.&lt;domain&gt; in your DNS.</span></span> <span data-ttu-id="b3af0-111">Исключение lyncdiscoverinternal. &lt; &gt; запись домена приведет к тому, что внутренние клиенты не смогут подключиться к нужным службам или получить неправильный ответ автообнаружения.</span><span class="sxs-lookup"><span data-stu-id="b3af0-111">Excluding the lyncdiscoverinternal.&lt;domain&gt; record will cause internal clients to fail to connect to the intended services or receive the incorrect Autodiscover response.</span></span>



</div>

### <a name="internal-dns-records"></a><span data-ttu-id="b3af0-112">Внутренние DNS-записи</span><span class="sxs-lookup"><span data-stu-id="b3af0-112">Internal DNS Records</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b3af0-113">Тип записи</span><span class="sxs-lookup"><span data-stu-id="b3af0-113">Record type</span></span></th>
<th><span data-ttu-id="b3af0-114">Имя узла</span><span class="sxs-lookup"><span data-stu-id="b3af0-114">Host name</span></span></th>
<th><span data-ttu-id="b3af0-115">Разрешается в</span><span class="sxs-lookup"><span data-stu-id="b3af0-115">Resolves to</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b3af0-116">CNAME</span><span class="sxs-lookup"><span data-stu-id="b3af0-116">CNAME</span></span></p></td>
<td><p><span data-ttu-id="b3af0-117">Lyncdiscoverinternal. &lt; внутреннее доменное имя&gt;</span><span class="sxs-lookup"><span data-stu-id="b3af0-117">Lyncdiscoverinternal.&lt;internal domain name&gt;</span></span></p></td>
<td><p><span data-ttu-id="b3af0-118">Полное доменное имя веб-служб для пула, если у вас есть один из них или для пула переднего плана, если у вас нет директора.</span><span class="sxs-lookup"><span data-stu-id="b3af0-118">Internal Web Services FQDN for your Director pool, if you have one, or for your Front End pool if you do not have a Director.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3af0-119">A (узел, если IPv6, AAAA)</span><span class="sxs-lookup"><span data-stu-id="b3af0-119">A (host, if IPv6, AAAA)</span></span></p></td>
<td><p><span data-ttu-id="b3af0-120">lyncdiscoverinternal. &lt; внутреннее доменное имя&gt;</span><span class="sxs-lookup"><span data-stu-id="b3af0-120">lyncdiscoverinternal.&lt;internal domain name&gt;</span></span></p></td>
<td><p><span data-ttu-id="b3af0-121">Внутренний IP-адрес веб-служб (виртуальный IP-адрес), если вы используете подсистему балансировки нагрузки из вашего пула, если у вас нет директора.</span><span class="sxs-lookup"><span data-stu-id="b3af0-121">Internal Web Services IP address (virtual IP (VIP) address if you use a load balancer) of your Director pool, if you have one, or of your Front End pool if you do not have a Director.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b3af0-122">Вам необходимо создать одну из следующих внешних DNS-записей:</span><span class="sxs-lookup"><span data-stu-id="b3af0-122">You need to create one of the following external DNS records:</span></span>

### <a name="external-dns-records"></a><span data-ttu-id="b3af0-123">Внешние записи DNS</span><span class="sxs-lookup"><span data-stu-id="b3af0-123">External DNS Records</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b3af0-124">Тип записи</span><span class="sxs-lookup"><span data-stu-id="b3af0-124">Record type</span></span></th>
<th><span data-ttu-id="b3af0-125">Имя узла</span><span class="sxs-lookup"><span data-stu-id="b3af0-125">Host name</span></span></th>
<th><span data-ttu-id="b3af0-126">Разрешается в</span><span class="sxs-lookup"><span data-stu-id="b3af0-126">Resolves to</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b3af0-127">CNAME</span><span class="sxs-lookup"><span data-stu-id="b3af0-127">CNAME</span></span></p></td>
<td><p><span data-ttu-id="b3af0-128">lyncdiscover.&lt;sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="b3af0-128">lyncdiscover.&lt;sipdomain&gt;</span></span></p></td>
<td><p><span data-ttu-id="b3af0-129">Внешнее полное доменное имя веб-служб для пула, если у вас есть один из них или для пула переднего плана, если у вас нет директора.</span><span class="sxs-lookup"><span data-stu-id="b3af0-129">External Web Services FQDN for your Director pool, if you have one, or for your Front End pool if you do not have a Director.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3af0-130">A (узел, если IPv6, AAAA)</span><span class="sxs-lookup"><span data-stu-id="b3af0-130">A (host, if IPv6, AAAA)</span></span></p></td>
<td><p><span data-ttu-id="b3af0-131">lyncdiscover.&lt;sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="b3af0-131">lyncdiscover.&lt;sipdomain&gt;</span></span></p></td>
<td><p><span data-ttu-id="b3af0-132">Внешний или общий IP-адрес обратного прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="b3af0-132">External or public IP address of the reverse proxy.</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="b3af0-133">Внешний трафик проходит через обратный прокси-сервер.</span><span class="sxs-lookup"><span data-stu-id="b3af0-133">External traffic goes through the reverse proxy.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="b3af0-134">Клиенты мобильных устройств не поддерживают несколько сертификатов SSL (Secure Sockets Layer) из разных доменов.</span><span class="sxs-lookup"><span data-stu-id="b3af0-134">Mobile device clients do not support multiple Secure Sockets Layer (SSL) certificates from different domains.</span></span> <span data-ttu-id="b3af0-135">Таким образом, перенаправление CNAME на разные домены не поддерживается по протоколу HTTPS.</span><span class="sxs-lookup"><span data-stu-id="b3af0-135">Therefore, CNAME redirection to different domains is not supported over HTTPS.</span></span> <span data-ttu-id="b3af0-136">Например, запись DNS CNAME для lyncdiscover.contoso.com, которая перенаправляет адрес director.contoso.net, не поддерживается по протоколу HTTPS.</span><span class="sxs-lookup"><span data-stu-id="b3af0-136">For example, a DNS CNAME record for lyncdiscover.contoso.com that redirects to an address of director.contoso.net is not supported over HTTPS.</span></span> <span data-ttu-id="b3af0-137">В такой топологии клиенту на мобильном устройстве необходимо использовать HTTP для первого запроса, чтобы перенаправление CNAME было разрешено через HTTP.</span><span class="sxs-lookup"><span data-stu-id="b3af0-137">In such a topology, a mobile device client needs to use HTTP for the first request, so that the CNAME redirection is resolved over HTTP.</span></span> <span data-ttu-id="b3af0-138">Затем последующие запросы используют протокол HTTPS.</span><span class="sxs-lookup"><span data-stu-id="b3af0-138">Subsequent requests then use HTTPS.</span></span> <span data-ttu-id="b3af0-139">Для поддержки этого сценария необходимо настроить обратный прокси с помощью правила веб-публикации для порта 80 (HTTP).</span><span class="sxs-lookup"><span data-stu-id="b3af0-139">To support this scenario, you need to configure your reverse proxy with a web publishing rule for port 80 (HTTP).</span></span> <span data-ttu-id="b3af0-140">Дополнительные сведения можно найти в разделе "Создание правила веб-публикации для порта 80" при <A href="lync-server-2013-configuring-the-reverse-proxy-for-mobility.md">настройке обратного прокси-сервера для мобильных устройств в Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="b3af0-140">For details, see "To create a web publishing rule for port 80" in <A href="lync-server-2013-configuring-the-reverse-proxy-for-mobility.md">Configuring the reverse proxy for mobility in Lync Server 2013</A>.</span></span> <span data-ttu-id="b3af0-141">Перенаправление CNAME на тот же домен поддерживается по протоколу HTTPS.</span><span class="sxs-lookup"><span data-stu-id="b3af0-141">CNAME redirection to the same domain is supported over HTTPS.</span></span> <span data-ttu-id="b3af0-142">В этом случае сертификат конечного домена охватывает исходный домен.</span><span class="sxs-lookup"><span data-stu-id="b3af0-142">In this case, the destination domain's certificate covers the originating domain.</span></span>



</div>

<div>

## <a name="see-also"></a><span data-ttu-id="b3af0-143">См. также</span><span class="sxs-lookup"><span data-stu-id="b3af0-143">See Also</span></span>


[<span data-ttu-id="b3af0-144">Настройка обратного прокси-сервера для мобильной работы в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b3af0-144">Configuring the reverse proxy for mobility in Lync Server 2013</span></span>](lync-server-2013-configuring-the-reverse-proxy-for-mobility.md)  


[<span data-ttu-id="b3af0-145">Сведения о сертификате: обнаружение автообнаружения в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b3af0-145">Certificate summary - Autodiscover in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-autodiscover.md)  
  

<span data-ttu-id="b3af0-146"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b3af0-146"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

