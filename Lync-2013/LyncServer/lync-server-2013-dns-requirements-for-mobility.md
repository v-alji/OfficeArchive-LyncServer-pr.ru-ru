---
title: 'Lync Server 2013: требования к DNS для мобильных устройств'
description: 'Lync Server 2013: требования к DNS для мобильных устройств.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS requirements for mobility
ms:assetid: df6962bc-2a16-440e-a333-022ebd14f957
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690040(v=OCS.15)
ms:contentKeyID: 48185624
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e2a8377dc7c856bb7250817cb3b8b66ed7789d3b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437807"
---
# <a name="dns-requirements-for-mobility-with-lync-server-2013"></a><span data-ttu-id="5f249-103">Требования к DNS для мобильных устройств с помощью Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5f249-103">DNS requirements for mobility with Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5f249-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5f249-104">

<span> </span></span></span>

<span data-ttu-id="5f249-105">_**Тема последнего изменения:** 2012-11-13_</span><span class="sxs-lookup"><span data-stu-id="5f249-105">_**Topic Last Modified:** 2012-11-13_</span></span>

<span data-ttu-id="5f249-106">При развертывании функции Lync Server 2013 Mobility Service вы можете использовать новые URL-адреса, доступные в службе автообнаружения Microsoft Lync Server 2013, или использовать существующие URL.</span><span class="sxs-lookup"><span data-stu-id="5f249-106">When you deploy the Lync Server 2013 mobility feature, you can use the new URLs that are available with the Microsoft Lync Server 2013 Autodiscover Service, or you can use your existing Web Services URLs.</span></span> <span data-ttu-id="5f249-107">Если вы используете существующие URL-адреса, пользователи должны вручную ввести URL-адреса в параметры мобильного устройства.</span><span class="sxs-lookup"><span data-stu-id="5f249-107">If you use your existing URLs, users need to manually enter the URLs in their mobile device settings.</span></span> <span data-ttu-id="5f249-108">Этот параметр обычно используется для устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="5f249-108">This option is typically used for troubleshooting.</span></span> <span data-ttu-id="5f249-109">При использовании новых URL-адресов мобильные клиенты могут автоматически определять ресурсы Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="5f249-109">When you use the new URLs, mobile clients can automatically discover Lync Server 2013 resources.</span></span> <span data-ttu-id="5f249-110">Если вы поддерживаете автоматическое обнаружение, вам нужно добавить новые записи DNS.</span><span class="sxs-lookup"><span data-stu-id="5f249-110">When you support automatic discovery, you need to add new Domain Name System (DNS) records.</span></span> <span data-ttu-id="5f249-111">В этом разделе описаны записи DNS, необходимые для автоматического обнаружения.</span><span class="sxs-lookup"><span data-stu-id="5f249-111">This section describes the DNS records that are required for automatic discovery.</span></span>

<span data-ttu-id="5f249-112">Для поддержки автоматического обнаружения необходимо создать следующие записи DNS для каждого домена SIP:</span><span class="sxs-lookup"><span data-stu-id="5f249-112">To support automatic discovery, you need to create the following DNS records for each SIP domain:</span></span>

  - <span data-ttu-id="5f249-113">Внутренняя запись DNS для поддержки мобильных пользователей, которые подключаются из сети Организации</span><span class="sxs-lookup"><span data-stu-id="5f249-113">An internal DNS record to support mobile users who connect from within your organization's network</span></span>

  - <span data-ttu-id="5f249-114">Внешняя (или общедоступная) запись DNS для поддержки мобильных пользователей, подключающихся из Интернета;</span><span class="sxs-lookup"><span data-stu-id="5f249-114">An external, or public, DNS record to support mobile users who connect from the Internet</span></span>

<span data-ttu-id="5f249-115">Внутренний URL-адрес автоматического обнаружения не должен быть адресом за пределами вашей сети.</span><span class="sxs-lookup"><span data-stu-id="5f249-115">The internal automatic discovery URL should not be addressable from outside your network.</span></span> <span data-ttu-id="5f249-116">URL-адрес внешнего автоматического обнаружения не должен быть адресом в сети.</span><span class="sxs-lookup"><span data-stu-id="5f249-116">The external automatic discovery URL should not be addressable from within your network.</span></span> <span data-ttu-id="5f249-117">Тем не менее, если вы не можете выполнить это требование для внешнего URL-адреса, не следует повлиять на мобильный клиент.</span><span class="sxs-lookup"><span data-stu-id="5f249-117">However, if you cannot meet this requirement for the external URL, mobile client functionally should not be affected.</span></span>

<span data-ttu-id="5f249-118">DNS-записи могут быть либо записями CNAME, либо записями (ведущими).</span><span class="sxs-lookup"><span data-stu-id="5f249-118">The DNS records can be either CNAME records or A (host) records.</span></span>

<span data-ttu-id="5f249-119">**Внутренние DNS-записи**</span><span class="sxs-lookup"><span data-stu-id="5f249-119">**Internal DNS records**</span></span>

<span data-ttu-id="5f249-120">Вам нужно создать одну из следующих внутренних DNS-записей:</span><span class="sxs-lookup"><span data-stu-id="5f249-120">You need to create one of the following internal DNS records:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5f249-121">Тип записи</span><span class="sxs-lookup"><span data-stu-id="5f249-121">Record type</span></span></th>
<th><span data-ttu-id="5f249-122">Определение имени узла или SRV</span><span class="sxs-lookup"><span data-stu-id="5f249-122">Host name or SRV definition</span></span></th>
<th><span data-ttu-id="5f249-123">Разрешается в</span><span class="sxs-lookup"><span data-stu-id="5f249-123">Resolves to</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5f249-124">CNAME</span><span class="sxs-lookup"><span data-stu-id="5f249-124">CNAME</span></span></p></td>
<td><p><span data-ttu-id="5f249-125">lyncdiscoverinternal.&lt;sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="5f249-125">lyncdiscoverinternal.&lt;sipdomain&gt;</span></span></p></td>
<td><p><span data-ttu-id="5f249-126">Полное доменное имя (FQDN) внутренних веб-служб для пула, если у вас есть один из них или для пула переднего плана, если у вас нет директора</span><span class="sxs-lookup"><span data-stu-id="5f249-126">Internal Web Services fully qualified domain name (FQDN) for your Director pool, if you have one, or for your Front End pool if you do not have a Director</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f249-127">A (узел)</span><span class="sxs-lookup"><span data-stu-id="5f249-127">A (host)</span></span></p></td>
<td><p><span data-ttu-id="5f249-128">lyncdiscoverinternal.&lt;sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="5f249-128">lyncdiscoverinternal.&lt;sipdomain&gt;</span></span></p></td>
<td><p><span data-ttu-id="5f249-129">IP-адрес внутренних веб-служб (VIP) (виртуальный IP-адрес) Если вы используете подсистему балансировки нагрузки в вашем пуле, если у вас есть один из них или у вас нет интерфейса, если у вас нет директора</span><span class="sxs-lookup"><span data-stu-id="5f249-129">Internal Web Services IP address (virtual IP (VIP) address if you use a load balancer) of your Director pool, if you have one, or of your Front End pool if you do not have a Director</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5f249-130">**Внешние записи DNS**</span><span class="sxs-lookup"><span data-stu-id="5f249-130">**External DNS records**</span></span>

<span data-ttu-id="5f249-131">Вам необходимо создать одну из следующих внешних DNS-записей:</span><span class="sxs-lookup"><span data-stu-id="5f249-131">You need to create one of the following external DNS records:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5f249-132">Тип записи</span><span class="sxs-lookup"><span data-stu-id="5f249-132">Record type</span></span></th>
<th><span data-ttu-id="5f249-133">Имя узла</span><span class="sxs-lookup"><span data-stu-id="5f249-133">Host name</span></span></th>
<th><span data-ttu-id="5f249-134">Разрешается в</span><span class="sxs-lookup"><span data-stu-id="5f249-134">Resolves to</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5f249-135">CNAME</span><span class="sxs-lookup"><span data-stu-id="5f249-135">CNAME</span></span></p></td>
<td><p><span data-ttu-id="5f249-136">lyncdiscover.</span><span class="sxs-lookup"><span data-stu-id="5f249-136">lyncdiscover.</span></span> <span data-ttu-id="5f249-137">&lt;sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="5f249-137">&lt;sipdomain&gt;</span></span></p></td>
<td><p><span data-ttu-id="5f249-138">Внешнее полное доменное имя веб-служб для пула, если у вас есть один из них или для пула переднего плана, если у вас нет директора</span><span class="sxs-lookup"><span data-stu-id="5f249-138">External Web Services FQDN for your Director pool, if you have one, or for your Front End pool if you do not have a Director</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f249-139">A (узел)</span><span class="sxs-lookup"><span data-stu-id="5f249-139">A (host)</span></span></p></td>
<td><p><span data-ttu-id="5f249-140">lyncdiscover.</span><span class="sxs-lookup"><span data-stu-id="5f249-140">lyncdiscover.</span></span> <span data-ttu-id="5f249-141">&lt;sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="5f249-141">&lt;sipdomain&gt;</span></span></p></td>
<td><p><span data-ttu-id="5f249-142">Внешний или общий IP-адрес (VIP, если вы используете подсистему балансировки нагрузки) для обратного прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="5f249-142">External or public IP address (VIP address if you use a load balancer) of the reverse proxy</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f249-143">SRV</span><span class="sxs-lookup"><span data-stu-id="5f249-143">SRV</span></span></p></td>
<td><p><span data-ttu-id="5f249-144">_sipfederationtls._tcp.</span><span class="sxs-lookup"><span data-stu-id="5f249-144">_sipfederationtls._tcp.</span></span> <span data-ttu-id="5f249-145">&lt;sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="5f249-145">&lt;sipdomain&gt;</span></span></p>
<p><span data-ttu-id="5f249-146">Разрешение на запись узла (A или AAAA) для службы пограничного доступа</span><span class="sxs-lookup"><span data-stu-id="5f249-146">Resolves to host (A or AAAA) record for the Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="5f249-147">Для поддержки службы push-уведомлений и службы push-уведомлений Apple вы создаете одну запись SRV для каждого домена SIP с клиентами Microsoft Lync Mobile.</span><span class="sxs-lookup"><span data-stu-id="5f249-147">To support Push Notification Service and Apple Push Notification service, you create one SRV record for each SIP domain that has Microsoft Lync Mobile clients.</span></span></p>
<div>

> [!IMPORTANT]  
> <span data-ttu-id="5f249-148">Это требование относится только к клиентам Microsoft Lync Mobile на мобильных устройствах Apple и Microsoft.</span><span class="sxs-lookup"><span data-stu-id="5f249-148">This requirement applies only to Microsoft Lync Mobile clients on Apple or Microsoft based mobile devices.</span></span> <span data-ttu-id="5f249-149">Устройства Andriod и Nokia Symbian не используют push-уведомление.</span><span class="sxs-lookup"><span data-stu-id="5f249-149">Andriod and Nokia Symbian devices do not use push notification.</span></span>


</div></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="5f249-150">Lyncdiscover, также называемый автообнаружением, трафик проходит через обратный прокси-сервер.</span><span class="sxs-lookup"><span data-stu-id="5f249-150">Lyncdiscover, also known as autodiscover, traffic goes through the reverse proxy.</span></span> <span data-ttu-id="5f249-151">Запись SRV указывает на запись, которая разрешается службой Edge Access.</span><span class="sxs-lookup"><span data-stu-id="5f249-151">SRV record points to a record that resolves through the Access Edge service.</span></span>



<span data-ttu-id="5f249-152"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5f249-152"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

