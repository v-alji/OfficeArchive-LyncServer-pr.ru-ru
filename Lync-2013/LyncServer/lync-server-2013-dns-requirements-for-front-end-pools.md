---
title: 'Lync Server 2013: требования к DNS для пула переднего'
description: 'Lync Server 2013: требования к DNS для пула Front End.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS requirements for Front End pools
ms:assetid: ba28919c-fbbe-4c54-8bf9-2b0cd3fa39c7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412910(v=OCS.15)
ms:contentKeyID: 48185228
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8c0369e82bd8ed2ea63e2156728b41f9942b0148
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429072"
---
# <a name="dns-requirements-for-front-end-pools-in-lync-server-2013"></a><span data-ttu-id="d2e15-103">Требования к DNS для пула Front End в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d2e15-103">DNS requirements for Front End pools in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d2e15-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d2e15-104">

<span> </span></span></span>

<span data-ttu-id="d2e15-105">_**Тема последнего изменения:** 2012-11-07_</span><span class="sxs-lookup"><span data-stu-id="d2e15-105">_**Topic Last Modified:** 2012-11-07_</span></span>

<span data-ttu-id="d2e15-106">В этом разделе описаны записи службы доменных имен (DNS), необходимые для развертывания пулов переднего уровня.</span><span class="sxs-lookup"><span data-stu-id="d2e15-106">This section describes the Domain Name System (DNS) records that are required for deployment of Front End pools.</span></span>

<div>

## <a name="dns-records-for-front-end-pools"></a><span data-ttu-id="d2e15-107">Записи DNS для переднего пула</span><span class="sxs-lookup"><span data-stu-id="d2e15-107">DNS Records for Front End Pools</span></span>

<span data-ttu-id="d2e15-108">В следующей таблице указаны требования к DNS для развертывания переднего пула Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d2e15-108">The following table specifies DNS requirements for a Lync Server 2013 Front End pool deployment.</span></span>

### <a name="dns-requirements-for-a-front-end-pool"></a><span data-ttu-id="d2e15-109">Требования К DNS для переднего пула</span><span class="sxs-lookup"><span data-stu-id="d2e15-109">DNS Requirements for a Front End Pool</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d2e15-110">Сценарий развертывания</span><span class="sxs-lookup"><span data-stu-id="d2e15-110">Deployment scenario</span></span></th>
<th><span data-ttu-id="d2e15-111">Требование DNS</span><span class="sxs-lookup"><span data-stu-id="d2e15-111">DNS requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d2e15-112">Передней пул с несколькими серверами переднего уровня и аппаратным балансировчиком нагрузки (независимо от того, развернута ли в нем балансировка нагрузки DNS)</span><span class="sxs-lookup"><span data-stu-id="d2e15-112">Front End pool with multiple Front End Servers and a hardware load balancer (whether or not DNS load balancing is also deployed on that pool)</span></span></p></td>
<td><p><span data-ttu-id="d2e15-113">При использовании балансировки нагрузки DNS и балансировки нагрузки оборудования необходимо иметь записи host (A).</span><span class="sxs-lookup"><span data-stu-id="d2e15-113">When using both DNS load balancing and a hardware load balancer, you need to Host (A) records.</span></span> <span data-ttu-id="d2e15-114">Создайте внутреннюю запись A, которая разрешит полное доменное имя (FQDN) переднего пула для балансировки нагрузки DNS.</span><span class="sxs-lookup"><span data-stu-id="d2e15-114">Create an internal A record that resolves the fully qualified domain name (FQDN) of the Front End pool for DNS load balancing.</span></span> <span data-ttu-id="d2e15-115">Создайте внутреннюю запись (A) для внутренних веб-служб на виртуальный IP-адрес (VIP-адрес) балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="d2e15-115">Create an internal host (A) record for the internal Web services to the virtual IP (VIP) address of the load balancer.</span></span> <span data-ttu-id="d2e15-116">Необходимо использовать имя внутренней веб-службы, как определено в построитель топологии.</span><span class="sxs-lookup"><span data-stu-id="d2e15-116">You must use the internal Web services name as defined in Topology Builder.</span></span></p>
<p><span data-ttu-id="d2e15-117">Например, если вы используете как балансировку нагрузки DNS, так и балансировку нагрузки оборудования, у вас будет запись A для каждого переднего сервера в пуле для балансировки нагрузки DNS и запись A для внутренних веб-служб, указывающих на виртуальный IP-адрес балансировки нагрузки оборудования:</span><span class="sxs-lookup"><span data-stu-id="d2e15-117">For example, if you use both DNS load balancing and hardware load balancing, you would have an A record for each Front End Server in a pool for DNS load balancing, and an A record for the internal Web services pointing to the virtual IP of the hardware load balancer:</span></span></p>
<ul>
<li><p><span data-ttu-id="d2e15-118">Балансировка нагрузки DNS: Pool01.contoso.net IP-адрес пула 10.10.10.5</span><span class="sxs-lookup"><span data-stu-id="d2e15-118">DNS load balancing:   Pool01.contoso.net   IP Address of pool   10.10.10.5</span></span></p>
<div>

> [!WARNING]  
> <span data-ttu-id="d2e15-119">У каждого переднего сервера также будет отдельная запись A:</span><span class="sxs-lookup"><span data-stu-id="d2e15-119">Each Front End Server will also have a distinct A record:</span></span>


</div>
<ol>
<li><p><span data-ttu-id="d2e15-120">FE01.contoso.net 10.10.10.1</span><span class="sxs-lookup"><span data-stu-id="d2e15-120">FE01.contoso.net    10.10.10.1</span></span></p></li>
<li><p><span data-ttu-id="d2e15-121">FE02.contoso.net 10.10.10.2</span><span class="sxs-lookup"><span data-stu-id="d2e15-121">FE02.contoso.net    10.10.10.2</span></span></p></li>
<li><p><span data-ttu-id="d2e15-122">FE03.contoso.net 10.10.10.3</span><span class="sxs-lookup"><span data-stu-id="d2e15-122">FE03.contoso.net    10.10.10.3</span></span></p></li>
<li><p><span data-ttu-id="d2e15-123">FE04.contoso.net 10.10.10.4</span><span class="sxs-lookup"><span data-stu-id="d2e15-123">FE04.contoso.net    10.10.10.4</span></span></p></li>
</ol></li>
<li><p><span data-ttu-id="d2e15-124">Балансировка нагрузки оборудования: WebInternal.contoso.net IP-адреса VIP 192.168.10.5 HLB</span><span class="sxs-lookup"><span data-stu-id="d2e15-124">Hardware load balancing:   WebInternal.contoso.net   IP Address of HLB VIP   192.168.10.5</span></span></p></li>
</ul>
<p><span data-ttu-id="d2e15-125">Все трафик, за исключением трафика HTTP или HTTPS, будет использовать Pool01.contoso.net записи.</span><span class="sxs-lookup"><span data-stu-id="d2e15-125">All traffic except for HTTP/HTTPS traffic will use the Pool01.contoso.net record.</span></span> <span data-ttu-id="d2e15-126">Трафик HTTP или HTTPS будет использовать определенный адрес внутренних веб-служб 192.168.10.5</span><span class="sxs-lookup"><span data-stu-id="d2e15-126">HTTP/HTTPS traffic will use the defined internal Web services address of 192.168.10.5</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2e15-127">Передний пул с развернутой балансировой нагрузки DNS</span><span class="sxs-lookup"><span data-stu-id="d2e15-127">Front End pool with DNS load balancing deployed</span></span></p></td>
<td><p><span data-ttu-id="d2e15-128">Набор внутренних записей A, которые решают FQDN пула с IP-адресами каждого сервера в пуле.</span><span class="sxs-lookup"><span data-stu-id="d2e15-128">A set of internal A records that resolve the FQDN of the pool to the IP address of each server in the pool.</span></span> <span data-ttu-id="d2e15-129">Для каждого сервера в пуле должна быть одна запись A.</span><span class="sxs-lookup"><span data-stu-id="d2e15-129">There must one A record for each server in the pool.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2e15-130">Передний пул с развернутой балансировой нагрузки DNS</span><span class="sxs-lookup"><span data-stu-id="d2e15-130">Front End pool with DNS load balancing deployed</span></span></p></td>
<td><p><span data-ttu-id="d2e15-131">Набор внутренних записей A, которые по IP-адресу этого сервера устанавливают FQDN каждого сервера в пуле.</span><span class="sxs-lookup"><span data-stu-id="d2e15-131">A set of internal A records that resolve the FQDN of each server in the pool to the IP address of that server.</span></span> <span data-ttu-id="d2e15-132">Подробные сведения см. в документации по планированию для балансировки нагрузки DNS в <a href="lync-server-2013-dns-load-balancing.md">Lync Server 2013.</a></span><span class="sxs-lookup"><span data-stu-id="d2e15-132">For details, see <a href="lync-server-2013-dns-load-balancing.md">DNS load balancing in Lync Server 2013</a> in the Planning documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2e15-133">Front End pool with a single Front End Server and a dedicated back-end database but no load balancer</span><span class="sxs-lookup"><span data-stu-id="d2e15-133">Front End pool with a single Front End Server and a dedicated back-end database but no load balancer</span></span></p></td>
<td><p><span data-ttu-id="d2e15-134">Внутренняя запись A, которая устраняет FQDN переднего пула с IP-адресом одного переднего сервера Enterprise Edition.</span><span class="sxs-lookup"><span data-stu-id="d2e15-134">An internal A record that resolves the FQDN of the Front End pool to the IP address of the single Enterprise Edition Front End Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2e15-135">Автоматический вход в клиент</span><span class="sxs-lookup"><span data-stu-id="d2e15-135">Automatic client sign-in</span></span></p></td>
<td><p><span data-ttu-id="d2e15-136">Для каждого поддерживаемых домена SIP записи SRV для _sipinternaltls._tcp. &lt; домен &gt; через порт 5061, который сопоканирует FQDN переднего пула, который аутентификация и перенаправляет запросы клиентов на вход.</span><span class="sxs-lookup"><span data-stu-id="d2e15-136">For each supported SIP domain, an SRV record for _sipinternaltls._tcp.&lt;domain&gt; over port 5061 that maps to the FQDN of the Front End pool that authenticates and redirects client requests for sign-in.</span></span> <span data-ttu-id="d2e15-137">Подробные сведения см. в требованиях К DNS для автоматического входов <a href="lync-server-2013-dns-requirements-for-automatic-client-sign-in.md">клиентов в Lync Server 2013.</a></span><span class="sxs-lookup"><span data-stu-id="d2e15-137">For details, see <a href="lync-server-2013-dns-requirements-for-automatic-client-sign-in.md">DNS requirements for automatic client sign-in in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2e15-138">Обнаружение веб-службы обновления устройств на устройствах единой коммуникации</span><span class="sxs-lookup"><span data-stu-id="d2e15-138">Device Update Web service discovery by unified communications (UC) devices</span></span></p></td>
<td><p><span data-ttu-id="d2e15-139">Внутренняя запись A с именем ucupdates-r2. &lt; Домен SIP, который передается на IP-адрес переднего пула, на котором размещена &gt; веб-служба обновления устройств.</span><span class="sxs-lookup"><span data-stu-id="d2e15-139">An internal A record with the name ucupdates-r2.&lt;SIP domain&gt; that resolves to the IP address of the Front End pool that hosts the Device Update Web service.</span></span> <span data-ttu-id="d2e15-140">В ситуации, когда устройство UC включено, но пользователь никогда не вошел в систему, запись A позволяет устройству обнаружить интерфейсную службу обновления пула, в которой размещено устройство, и получить обновления.</span><span class="sxs-lookup"><span data-stu-id="d2e15-140">In the situation where a UC device is turned on, but a user has never logged into the device, the A record allows the device to discover the Front End pool hosting Device Update Web service and obtain updates.</span></span> <span data-ttu-id="d2e15-141">В противном случае устройства получают эти сведения, хотя при первом входе пользователя они получают доступ к интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="d2e15-141">Otherwise, devices obtain this information though in-band provisioning the first time a user logs in.</span></span></p>
<div>

> [!IMPORTANT]  
> <span data-ttu-id="d2e15-142">Если у вас уже развернута веб-служба обновления устройств в Lync Server 2010, вы уже создали внутреннюю запись A с именем, которое не работает. &lt; Домен &gt; SIP.</span><span class="sxs-lookup"><span data-stu-id="d2e15-142">If you have an existing deployment of Device Update Web service in Lync Server 2010, you have already created an internal A record with the name ucupdates.&lt;SIP domain&gt;.</span></span> <span data-ttu-id="d2e15-143">Для Microsoft Office Communications Server 2007 R2 необходимо создать дополнительную запись DNS A с именем ucupdates-r2. &lt; Домен &gt; SIP.</span><span class="sxs-lookup"><span data-stu-id="d2e15-143">For Microsoft Office Communications Server 2007 R2, you must create an additional DNS A record with the name ucupdates-r2.&lt;SIP domain&gt;.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2e15-144">Обратный прокси-сервер для поддержки HTTP-трафика</span><span class="sxs-lookup"><span data-stu-id="d2e15-144">A reverse proxy to support HTTP traffic</span></span></p></td>
<td><p><span data-ttu-id="d2e15-145">Внешняя запись A, которая устраняет FQDN внешней веб-фермы с внешним IP-адресом обратного прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="d2e15-145">An external A record that resolves the external web farm FQDN to the external IP address of the reverse proxy.</span></span> <span data-ttu-id="d2e15-146">Клиенты и устройства UC используют эту запись для подключения к обратному прокси-серверу.</span><span class="sxs-lookup"><span data-stu-id="d2e15-146">Clients and UC devices use this record to connect to the reverse proxy.</span></span> <span data-ttu-id="d2e15-147">Подробные сведения см. в документации по планированию определения требований К DNS для <a href="lync-server-2013-determine-dns-requirements.md">Lync Server 2013.</a></span><span class="sxs-lookup"><span data-stu-id="d2e15-147">For details, see <a href="lync-server-2013-determine-dns-requirements.md">Determine DNS requirements for Lync Server 2013</a> in the Planning documentation.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d2e15-148">В таблице ниже показан пример записей DNS, необходимых для FQDN внутренней веб-фермы.</span><span class="sxs-lookup"><span data-stu-id="d2e15-148">The following table shows an example of the DNS records required for the internal web farm FQDN.</span></span>

### <a name="example-dns-records-for-internal-web-farm-fqdn"></a><span data-ttu-id="d2e15-149">Примеры DNS-записей для FQDN внутренней веб-фермы</span><span class="sxs-lookup"><span data-stu-id="d2e15-149">Example DNS Records for Internal Web Farm FQDN</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d2e15-150">FQDN внутренней веб-фермы</span><span class="sxs-lookup"><span data-stu-id="d2e15-150">Internal web farm FQDN</span></span></th>
<th><span data-ttu-id="d2e15-151">Полное доменное имя пула</span><span class="sxs-lookup"><span data-stu-id="d2e15-151">Pool FQDN</span></span></th>
<th><span data-ttu-id="d2e15-152">Записи DNS A</span><span class="sxs-lookup"><span data-stu-id="d2e15-152">DNS A record(s)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d2e15-153">webcon.contoso.com</span><span class="sxs-lookup"><span data-stu-id="d2e15-153">webcon.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="d2e15-154">ee-pool.contoso.com</span><span class="sxs-lookup"><span data-stu-id="d2e15-154">ee-pool.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="d2e15-155">DNS A-запись для ee-pool.contoso.com, которая передается на VIP-адрес балансира нагрузки, используемого серверами переднего сервера.</span><span class="sxs-lookup"><span data-stu-id="d2e15-155">DNS A record for the ee-pool.contoso.com that resolves to the VIP address of the load balancer used by the Front End Servers.</span></span></p>
<p><span data-ttu-id="d2e15-156">DNS A-запись для webcon.contoso.com, которая передается на VIP-адрес балансира нагрузки, используемого серверами переднего сервера.</span><span class="sxs-lookup"><span data-stu-id="d2e15-156">DNS A record for webcon.contoso.com that resolves to the VIP address of the load balancer used by the Front End Servers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2e15-157">ee-pool.contoso.com</span><span class="sxs-lookup"><span data-stu-id="d2e15-157">ee-pool.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="d2e15-158">ee-pool.contoso.com</span><span class="sxs-lookup"><span data-stu-id="d2e15-158">ee-pool.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="d2e15-159">DNS A-запись для ee-pool.contoso.com, которая передается на виртуальный IP-адрес (VIP) балансира нагрузки, используемого серверами Front End Server Enterprise Edition в переднем пуле.</span><span class="sxs-lookup"><span data-stu-id="d2e15-159">DNS A record for ee-pool.contoso.com that resolves to the virtual IP (VIP) address of the load balancer used by the Enterprise Edition Front End Servers in the Front End pool.</span></span></p>
<p><span data-ttu-id="d2e15-160">Обратите внимание: если в этом пуле используется балансировка нагрузки DNS, у вашего переднего и внутреннего веб-фермы не может быть одного и того же FQDN.</span><span class="sxs-lookup"><span data-stu-id="d2e15-160">Note that if you are using DNS load balancing on this pool, your Front End pool and internal web farm cannot have the same FQDN.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="d2e15-161">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d2e15-161">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

