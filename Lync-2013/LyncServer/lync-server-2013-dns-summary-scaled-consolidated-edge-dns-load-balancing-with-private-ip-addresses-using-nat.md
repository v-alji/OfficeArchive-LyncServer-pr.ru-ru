---
title: 'Lync Server 2013: сводка по DNS — масштабируемая консолидированная пограничная топология, балансировка нагрузки на DNS с закрытыми IP-адресами и трансляцией сетевых адресов'
description: 'Lync Server 2013: масштабируемая статистическая подложка, балансировка нагрузки DNS с частными IP-адресами, использующая NAT.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS summary - Scaled consolidated edge, DNS load balancing with private IP addresses using NAT
ms:assetid: 11bc7b84-91cf-48f9-ad0e-06ad30b46a2e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398201(v=OCS.15)
ms:contentKeyID: 48183447
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2eef3029323c1c2f798fddc721df832a932524c8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437709"
---
# <a name="dns-summary---scaled-consolidated-edge-dns-load-balancing-with-private-ip-addresses-using-nat-in-lync-server-2013"></a><span data-ttu-id="eb99a-103">Сводка по DNS — масштабируемая консолидированная пограничная топология, балансировка нагрузки на DNS с закрытыми IP-адресами и трансляцией сетевых адресов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="eb99a-103">DNS summary - Scaled consolidated edge, DNS load balancing with private IP addresses using NAT in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="eb99a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="eb99a-104">

<span> </span></span></span>

<span data-ttu-id="eb99a-105">_**Тема последнего изменения:** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="eb99a-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="eb99a-106">Требования к записям DNS для удаленного доступа к Lync Server 2013 довольно просты в сравнении с сертификатами и портами.</span><span class="sxs-lookup"><span data-stu-id="eb99a-106">DNS record requirements for remote access to Lync Server 2013 are fairly straightforward compared to those for certificates and ports.</span></span> <span data-ttu-id="eb99a-107">Кроме того, в зависимости от того, как вы настраиваете клиентов под управлением Lync 2013 и включена ли интеграция, многие записи не являются обязательными.</span><span class="sxs-lookup"><span data-stu-id="eb99a-107">Also, many records are optional, depending on how you configure clients running Lync 2013 and whether you enable federation.</span></span>

<span data-ttu-id="eb99a-108">Дополнительные сведения о требованиях к службе DNS для Lync 2013: [Определение требований к DNS для Lync Server 2013](lync-server-2013-determine-dns-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="eb99a-108">For details about Lync 2013 DNS requirements, see [Determine DNS requirements for Lync Server 2013](lync-server-2013-determine-dns-requirements.md).</span></span>

<span data-ttu-id="eb99a-109">Дополнительные сведения о настройке автоматической конфигурации клиентов Lync 2013, если DNS с разделением не настроена, приведены в статье [Определение требований к DNS для Lync Server 2013](lync-server-2013-determine-dns-requirements.md)в разделе Автоматическая настройка без разделения DNS-мозгового обобщения.</span><span class="sxs-lookup"><span data-stu-id="eb99a-109">For details about configuring automatic configuration of Lync 2013 clients if split-brain DNS is not configured, see the "Automatic Configuration without Split Brain DNS" section in [Determine DNS requirements for Lync Server 2013](lync-server-2013-determine-dns-requirements.md).</span></span>

<span data-ttu-id="eb99a-110">В таблице ниже приведены сведения о DNS-записях, которые должны поддерживать единую объединенную топологию пограничного объекта, которая показана на рисунке одномерной топологии.</span><span class="sxs-lookup"><span data-stu-id="eb99a-110">The following table contains a summary of the DNS records that are required to support the single consolidated edge topology shown in the Single Consolidated Edge Topology figure.</span></span> <span data-ttu-id="eb99a-111">Обратите внимание, что определенные записи DNS требуются только для автоматической настройки клиентов Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="eb99a-111">Note that certain DNS records are required only for automatic configuration of Lync 2013 clients.</span></span> <span data-ttu-id="eb99a-112">Если вы планируете использовать объекты групповой политики (GPO) для настройки клиентов Lync, связанные записи не нужны.</span><span class="sxs-lookup"><span data-stu-id="eb99a-112">If you plan to use group policy objects (GPOs) to configure Lync clients, the associated records are not necessary.</span></span>

<div>

## <a name="important-edge-server-network-adapter-requirements"></a><span data-ttu-id="eb99a-113">ВНИМАНИЕ! требования к сетевому адаптеру пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="eb99a-113">IMPORTANT: Edge Server Network Adapter Requirements</span></span>

<span data-ttu-id="eb99a-114">Чтобы избежать проблем с маршрутизацией, убедитесь в том, что на пограничных серверах есть по крайней мере два сетевых адаптера, и что шлюз по умолчанию задан только на сетевом адаптере, связанном с внешним интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="eb99a-114">To avoid routing issues, verify that there are at least two network adapters in your Edge Servers and that the default gateway is set only on the network adapter associated with the external interface.</span></span> <span data-ttu-id="eb99a-115">Например, как показано в описании масштабируемой подложки в масштабе [, в Lync Server 2013 шлюзом балансировки нагрузки DNS с частными IP-адресами](lync-server-2013-scaled-consolidated-edge-dns-load-balancing-with-private-ip-addresses-using-nat.md), используемым по умолчанию, указывает на внешний брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="eb99a-115">For example, as shown in the Scaled Consolidated Edge Scenario figure in [Scaled consolidated edge, DNS load balancing with private IP addresses using NAT in Lync Server 2013](lync-server-2013-scaled-consolidated-edge-dns-load-balancing-with-private-ip-addresses-using-nat.md), the default gateway would point to the external firewall.</span></span>

<span data-ttu-id="eb99a-116">Вы можете настроить два сетевых адаптера для каждого пограничного сервера, выполнив указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="eb99a-116">You can configure two network adapters in each of your Edge Server as follows:</span></span>

  - <span data-ttu-id="eb99a-117">**Сетевой адаптер 1-узел 1 (внутренний интерфейс)**</span><span class="sxs-lookup"><span data-stu-id="eb99a-117">**Network adapter 1 - Node 1 (Internal Interface)**</span></span>
    
    <span data-ttu-id="eb99a-118">Внутренний интерфейс с назначенным 172.25.33.10.</span><span class="sxs-lookup"><span data-stu-id="eb99a-118">Internal interface with 172.25.33.10 assigned.</span></span>
    
    <span data-ttu-id="eb99a-119">Шлюз по умолчанию не определен.</span><span class="sxs-lookup"><span data-stu-id="eb99a-119">No default gateway is defined.</span></span>
    
    <span data-ttu-id="eb99a-120">Убедитесь в том, что в сети есть маршрут, содержащий внутренний интерфейс EDGE, для всех сетей, содержащих серверы с установленными клиентами Lync Server 2013 или Lync Server 2013 (например, с 172.25.33.0 на 192.168.10.0).</span><span class="sxs-lookup"><span data-stu-id="eb99a-120">Ensure that there is a route from the network containing the Edge internal interface to any networks that contain servers running Lync Server 2013 or Lync Server 2013 clients (for example, from 172.25.33.0 to 192.168.10.0).</span></span>

  - <span data-ttu-id="eb99a-121">**Сетевой адаптер 1-node 2 (внутренний интерфейс)**</span><span class="sxs-lookup"><span data-stu-id="eb99a-121">**Network adapter 1 - Node 2 (Internal Interface)**</span></span>
    
    <span data-ttu-id="eb99a-122">Внутренний интерфейс с назначенным 172.25.33.11.</span><span class="sxs-lookup"><span data-stu-id="eb99a-122">Internal interface with 172.25.33.11 assigned.</span></span>
    
    <span data-ttu-id="eb99a-123">Шлюз по умолчанию не определен.</span><span class="sxs-lookup"><span data-stu-id="eb99a-123">No default gateway is defined.</span></span>
    
    <span data-ttu-id="eb99a-124">Убедитесь в том, что в сети есть маршрут, содержащий внутренний интерфейс EDGE, для всех сетей, содержащих серверы с установленными клиентами Lync Server 2013 или Lync Server 2013 (например, с 172.25.33.0 на 192.168.10.0).</span><span class="sxs-lookup"><span data-stu-id="eb99a-124">Ensure that there is a route from the network containing the Edge internal interface to any networks that contain servers running Lync Server 2013 or Lync Server 2013 clients (for example, from 172.25.33.0 to 192.168.10.0).</span></span>

  - <span data-ttu-id="eb99a-125">**Сетевой адаптер 2, узел 1 (внешний интерфейс)**</span><span class="sxs-lookup"><span data-stu-id="eb99a-125">**Network adapter 2 Node 1 (External Interface)**</span></span>
    
    <span data-ttu-id="eb99a-126">Этому сетевому адаптеру назначаются три частных IP-адреса, например 10.45.16.10 для доступа к краю, 10.45.16.20 для веб-конференций EDGE, 10.45.16.30 для AV Edge.</span><span class="sxs-lookup"><span data-stu-id="eb99a-126">Three private IP addresses are assigned to this network adapter, for example 10.45.16.10 for Access Edge, 10.45.16.20 for Web Conferencing Edge, 10.45.16.30 for AV Edge.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="eb99a-127">Возможно, хотя и не рекомендуется использовать один IP-адрес для всех трех интерфейсов служб Edge.</span><span class="sxs-lookup"><span data-stu-id="eb99a-127">It is possible, though not recommended, to use a single IP address for all three Edge service interfaces.</span></span> <span data-ttu-id="eb99a-128">Несмотря на то, что это сохранит IP-адреса, для каждой службы требуется указать разные номера портов.</span><span class="sxs-lookup"><span data-stu-id="eb99a-128">Though this does save IP addresses, it requires different port numbers for each service.</span></span> <span data-ttu-id="eb99a-129">Номер порта по умолчанию: 443/TCP, что позволяет большинству удаленных брандмауэров допустить трафик.</span><span class="sxs-lookup"><span data-stu-id="eb99a-129">The default port number is 443/TCP, which ensures that most remote firewalls will allow the traffic.</span></span> <span data-ttu-id="eb99a-130">Изменение значений порта (например,) 5061/TCP для Edge доступа, 444/TCP для веб-конференций EDGE и 443/TCP для теплосвязи может привести к проблемам с удаленными пользователями, в которых брандмауэр не разрешает трафик через 5061/TCP и 444/TCP.</span><span class="sxs-lookup"><span data-stu-id="eb99a-130">Changing the port values to (for example) 5061/TCP for the Access Edge, 444/TCP for the Web Conferencing Edge and 443/TCP for the AV Edge might cause problems for remote users where a firewall that they are behind does not allow the traffic over 5061/TCP and 444/TCP.</span></span> <span data-ttu-id="eb99a-131">Кроме того, три отдельных IP-адреса упрощают устранение неполадок, так как они позволяют фильтровать по IP-адресу.</span><span class="sxs-lookup"><span data-stu-id="eb99a-131">Additionally, three distinct IP addresses makes troubleshooting easier due to being able to filter on IP address.</span></span>

    
    </div>
    
    <span data-ttu-id="eb99a-132">Общедоступный IP-адрес Edge для доступа является основным шлюзом по умолчанию, установленным на интегрированный маршрутизатор (10.45.16.1).</span><span class="sxs-lookup"><span data-stu-id="eb99a-132">The Access Edge public IP address is primary with default gateway set to the integrated router (10.45.16.1).</span></span>
    
    <span data-ttu-id="eb99a-133">Веб-конференции и частные IP-адреса Edge — это дополнительные IP-адреса в разделе " **Дополнительно** " свойств IP- **протоколов версии 4 (TCP/IPv4)** и IP- **протоколов версии 6 (TCP/IPv6)** для **подключений по локальной** сети в Windows Server.</span><span class="sxs-lookup"><span data-stu-id="eb99a-133">Web conferencing and A/V Edge private IP addresses are additional IP addresses in the **Advanced** section of the properties of **Internet Protocol Version 4 (TCP/IPv4)** and **Internet Protocol Version 6 (TCP/IPv6)** of the **Local Area Connection Properties** in Windows Server.</span></span>

  - <span data-ttu-id="eb99a-134">**Сетевой адаптер 2, узел 2 (внешний интерфейс)**</span><span class="sxs-lookup"><span data-stu-id="eb99a-134">**Network adapter 2 Node 2 (External Interface)**</span></span>
    
    <span data-ttu-id="eb99a-135">Этому сетевому адаптеру назначаются три частных IP-адреса, например 10.45.16.11 для доступа к краю, 10.45.16.21 для веб-конференций EDGE, 10.45.16.31 для AV Edge.</span><span class="sxs-lookup"><span data-stu-id="eb99a-135">Three private IP addresses are assigned to this network adapter, for example 10.45.16.11 for Access Edge, 10.45.16.21 for Web Conferencing Edge, 10.45.16.31 for AV Edge.</span></span>
    
    <span data-ttu-id="eb99a-136">Общедоступный IP-адрес Edge для доступа является основным шлюзом по умолчанию, установленным на интегрированный маршрутизатор (10.45.16.1).</span><span class="sxs-lookup"><span data-stu-id="eb99a-136">The Access Edge public IP address is primary with default gateway set to the integrated router (10.45.16.1).</span></span>
    
    <span data-ttu-id="eb99a-137">Веб-конференции и частные IP-адреса Edge — это дополнительные IP-адреса в разделе " **Дополнительно** " свойств IP- **протоколов версии 4 (TCP/IPv4)** и IP- **протоколов версии 6 (TCP/IPv6)** для **подключений по локальной** сети в Windows Server.</span><span class="sxs-lookup"><span data-stu-id="eb99a-137">Web conferencing and A/V Edge private IP addresses are additional IP addresses in the **Advanced** section of the properties of **Internet Protocol Version 4 (TCP/IPv4)** and **Internet Protocol Version 6 (TCP/IPv6)** of the **Local Area Connection Properties** in Windows Server.</span></span>

<div>


> [!TIP]  
> <span data-ttu-id="eb99a-138">Настройка пограничного сервера двумя сетевыми адаптерами — один из двух вариантов.</span><span class="sxs-lookup"><span data-stu-id="eb99a-138">Configuring the Edge Server with two network adapters is one of two options.</span></span> <span data-ttu-id="eb99a-139">Другим вариантом является использование одного сетевого адаптера для внутренних и трех сетевых адаптеров на внешней стороне пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="eb99a-139">The other option is to use one network adapter for the internal side and three network adapters for the external side of the Edge Server.</span></span> <span data-ttu-id="eb99a-140">Основным преимуществом этого параметра является отдельный сетевой адаптер для службы пограничного сервера и, возможно, более краткая коллекция данных, если требуется устранение неполадок</span><span class="sxs-lookup"><span data-stu-id="eb99a-140">The main benefit of this option is a distinct network adapter per Edge Server service, and potentially more concise data collection when troubleshooting is necessary</span></span>



</div>

### <a name="dns-records-required-for-scaled-consolidated-edge-dns-load-balancing-with-private-ip-addresses-using-nat-example"></a><span data-ttu-id="eb99a-141">DNS-записи, необходимые для масштабируемой консолидированной кромки, балансировки нагрузки DNS с частными IP-адресами с использованием NAT (пример)</span><span class="sxs-lookup"><span data-stu-id="eb99a-141">DNS Records Required for Scaled Consolidated Edge, DNS Load Balancing with Private IP Addresses Using NAT (Example)</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="eb99a-142">Расположение/тип/порт</span><span class="sxs-lookup"><span data-stu-id="eb99a-142">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="eb99a-143">Полное доменное имя/DNS-запись</span><span class="sxs-lookup"><span data-stu-id="eb99a-143">FQDN/DNS Record</span></span></th>
<th><span data-ttu-id="eb99a-144">IP-адрес или полное доменное имя</span><span class="sxs-lookup"><span data-stu-id="eb99a-144">IP Address/FQDN</span></span></th>
<th><span data-ttu-id="eb99a-145">Карты и примечания</span><span class="sxs-lookup"><span data-stu-id="eb99a-145">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eb99a-146">Внешние DNS/A</span><span class="sxs-lookup"><span data-stu-id="eb99a-146">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="eb99a-147">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="eb99a-147">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="eb99a-148">131.107.155.10 и 131.107.155.11</span><span class="sxs-lookup"><span data-stu-id="eb99a-148">131.107.155.10 and 131.107.155.11</span></span></p></td>
<td><p><span data-ttu-id="eb99a-149">Внешний интерфейс Access Edge (Contoso) повторяется по мере необходимости для всех доменов SIP с пользователями, поддерживающими Lync.</span><span class="sxs-lookup"><span data-stu-id="eb99a-149">Access Edge external interface (Contoso) Repeat as necessary for all SIP domains with Lync enabled users</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb99a-150">Внешние DNS/A</span><span class="sxs-lookup"><span data-stu-id="eb99a-150">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="eb99a-151">webcon.contoso.com</span><span class="sxs-lookup"><span data-stu-id="eb99a-151">webcon.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="eb99a-152">131.107.155.20 и 131.107.155.21</span><span class="sxs-lookup"><span data-stu-id="eb99a-152">131.107.155.20 and 131.107.155.21</span></span></p></td>
<td><p><span data-ttu-id="eb99a-153">Внешний интерфейс для веб-конференций Edge</span><span class="sxs-lookup"><span data-stu-id="eb99a-153">Web Conferencing Edge external interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb99a-154">Внешние DNS/A</span><span class="sxs-lookup"><span data-stu-id="eb99a-154">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="eb99a-155">av.contoso.com</span><span class="sxs-lookup"><span data-stu-id="eb99a-155">av.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="eb99a-156">131.107.155.30 и 131.107.155.31</span><span class="sxs-lookup"><span data-stu-id="eb99a-156">131.107.155.30 and 131.107.155.31</span></span></p></td>
<td><p><span data-ttu-id="eb99a-157">Внешний интерфейс "на/V" Edge</span><span class="sxs-lookup"><span data-stu-id="eb99a-157">A/V Edge external interface</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb99a-158">Внешние DNS/SRV/443</span><span class="sxs-lookup"><span data-stu-id="eb99a-158">External DNS/SRV/443</span></span></p></td>
<td><p><span data-ttu-id="eb99a-159">_sip._tls.contoso.com</span><span class="sxs-lookup"><span data-stu-id="eb99a-159">_sip._tls.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="eb99a-160">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="eb99a-160">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="eb99a-161">Внешний интерфейс пограничного доступа.</span><span class="sxs-lookup"><span data-stu-id="eb99a-161">Access Edge external interface.</span></span> <span data-ttu-id="eb99a-162">Требуется для автоматической настройки клиентов Lync 2013 и Lync 2010 для работы с внешними сотрудниками.</span><span class="sxs-lookup"><span data-stu-id="eb99a-162">Required for automatic configuration of Lync 2013 and Lync 2010 clients to work externally.</span></span> <span data-ttu-id="eb99a-163">При необходимости повторите эти действия для всех доменов SIP с пользователями, поддерживающими Lync.</span><span class="sxs-lookup"><span data-stu-id="eb99a-163">Repeat as necessary for all SIP domains with Lync enabled users.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb99a-164">Внешние DNS/SRV/5061</span><span class="sxs-lookup"><span data-stu-id="eb99a-164">External DNS/SRV/5061</span></span></p></td>
<td><p><span data-ttu-id="eb99a-165">_sipfederationtls._tcp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="eb99a-165">_sipfederationtls._tcp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="eb99a-166">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="eb99a-166">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="eb99a-167">Внешний интерфейс пограничного доступа SIP.</span><span class="sxs-lookup"><span data-stu-id="eb99a-167">SIP Access Edge external interface.</span></span> <span data-ttu-id="eb99a-168">Требуется для автоматического обнаружения DNS федеративных партнеров, известного как "разрешенный домен SIP" (в предыдущих версиях — Улучшенная Федерация).</span><span class="sxs-lookup"><span data-stu-id="eb99a-168">Required for automatic DNS discovery of federated partners known as “Allowed SIP Domain” (called enhanced federation in previous releases).</span></span> <span data-ttu-id="eb99a-169">При необходимости повторите эти действия для всех доменов SIP с пользователями, поддерживающими Lync.</span><span class="sxs-lookup"><span data-stu-id="eb99a-169">Repeat as necessary for all SIP domains with Lync enabled users</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb99a-170">Внутренняя DNS/A</span><span class="sxs-lookup"><span data-stu-id="eb99a-170">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="eb99a-171">lsedge.contoso.net</span><span class="sxs-lookup"><span data-stu-id="eb99a-171">lsedge.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="eb99a-172">172.25.33.10 и 172.25.33.11</span><span class="sxs-lookup"><span data-stu-id="eb99a-172">172.25.33.10 and 172.25.33.11</span></span></p></td>
<td><p><span data-ttu-id="eb99a-173">Внутренний интерфейс "консолидированный Edge"</span><span class="sxs-lookup"><span data-stu-id="eb99a-173">Consolidated Edge internal interface</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="records-required-for-federation"></a><span data-ttu-id="eb99a-174">Записи, необходимые для Федерации</span><span class="sxs-lookup"><span data-stu-id="eb99a-174">Records Required for Federation</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="eb99a-175">Расположение/тип/порт</span><span class="sxs-lookup"><span data-stu-id="eb99a-175">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="eb99a-176">Полное доменное имя</span><span class="sxs-lookup"><span data-stu-id="eb99a-176">FQDN</span></span></th>
<th><span data-ttu-id="eb99a-177">IP-адрес или полное доменное имя записи узла</span><span class="sxs-lookup"><span data-stu-id="eb99a-177">IP address/FQDN host record</span></span></th>
<th><span data-ttu-id="eb99a-178">Карты и примечания</span><span class="sxs-lookup"><span data-stu-id="eb99a-178">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eb99a-179">Внешние DNS/SRV/5061</span><span class="sxs-lookup"><span data-stu-id="eb99a-179">External DNS/SRV/5061</span></span></p></td>
<td><p><span data-ttu-id="eb99a-180">_sipfederationtls._tcp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="eb99a-180">_sipfederationtls._tcp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="eb99a-181">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="eb99a-181">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="eb99a-182">Внешний интерфейс внешнего доступа SIP, необходимый для автоматического обнаружения DNS для Федерации с другими потенциальными партнерами Федерации и известный как "разрешенные домены SIP" (с названием "Улучшенная Федерация в предыдущих версиях)". При необходимости повторите эти действия для всех доменов SIP с пользователями, поддерживающими Lync.</span><span class="sxs-lookup"><span data-stu-id="eb99a-182">SIP Access Edge external interface Required for automatic DNS discovery of your federation to other potential federation partners, and is known as “Allowed SIP Domains” (called enhanced federation in previous releases).Repeat as necessary for all SIP domains with Lync enabled users</span></span></p>
<div>

> [!IMPORTANT]  
> <span data-ttu-id="eb99a-183">Эта запись SRV требуется для мобильных устройств и для очищенных push-уведомлений</span><span class="sxs-lookup"><span data-stu-id="eb99a-183">This SRV record is required for mobility and the push notification clearing house</span></span>


</div></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="dns-summary--public-instant-messaging-connectivity"></a><span data-ttu-id="eb99a-184">Общие сведения о DNS — общедоступная служба обмена мгновенными сообщениями</span><span class="sxs-lookup"><span data-stu-id="eb99a-184">DNS Summary – Public Instant Messaging Connectivity</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="eb99a-185">Расположение/тип/порт</span><span class="sxs-lookup"><span data-stu-id="eb99a-185">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="eb99a-186">Полное доменное имя/DNS-запись</span><span class="sxs-lookup"><span data-stu-id="eb99a-186">FQDN/DNS Record</span></span></th>
<th><span data-ttu-id="eb99a-187">IP-адрес или полное доменное имя</span><span class="sxs-lookup"><span data-stu-id="eb99a-187">IP Address/FQDN</span></span></th>
<th><span data-ttu-id="eb99a-188">Карты и примечания</span><span class="sxs-lookup"><span data-stu-id="eb99a-188">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eb99a-189">Внешние DNS/A</span><span class="sxs-lookup"><span data-stu-id="eb99a-189">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="eb99a-190">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="eb99a-190">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="eb99a-191">Интерфейс пограничной службы доступа</span><span class="sxs-lookup"><span data-stu-id="eb99a-191">Access Edge service interface</span></span></p></td>
<td><p><span data-ttu-id="eb99a-192">Внешний интерфейс Access Edge (Contoso) повторяется по мере необходимости для всех доменов SIP с пользователями, поддерживающими Lync.</span><span class="sxs-lookup"><span data-stu-id="eb99a-192">Access Edge external interface (Contoso)Repeat as necessary for all SIP domains with Lync enabled users</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="dns-summary-for-extensible-messaging-and-presence-protocol"></a><span data-ttu-id="eb99a-193">Сводка DNS по расширенному протоколу обмена сообщениями и присутствием</span><span class="sxs-lookup"><span data-stu-id="eb99a-193">DNS Summary for Extensible Messaging and Presence Protocol</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="eb99a-194">Расположение/тип/порт</span><span class="sxs-lookup"><span data-stu-id="eb99a-194">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="eb99a-195">Полное доменное имя</span><span class="sxs-lookup"><span data-stu-id="eb99a-195">FQDN</span></span></th>
<th><span data-ttu-id="eb99a-196">IP-адрес или полное доменное имя записи узла</span><span class="sxs-lookup"><span data-stu-id="eb99a-196">IP address/FQDN host record</span></span></th>
<th><span data-ttu-id="eb99a-197">Карты и примечания</span><span class="sxs-lookup"><span data-stu-id="eb99a-197">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eb99a-198">Внешние DNS/SRV/5269</span><span class="sxs-lookup"><span data-stu-id="eb99a-198">External DNS/SRV/5269</span></span></p></td>
<td><p><span data-ttu-id="eb99a-199">_xmpp-server._tcp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="eb99a-199">_xmpp-server._tcp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="eb99a-200">xmpp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="eb99a-200">xmpp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="eb99a-201">Внешний интерфейс XMPP прокси-сервера в службе пограничного доступа или пуле Edge. При необходимости повторите эти действия для всех внутренних доменов SIP, в которых пользователи Lync поддерживают доступ к контактам с контактами XMPP с помощью глобальной политики, политики сайта, в которой находится пользователь, или политики пользователя, примененной к пользователю с поддержкой Lync.</span><span class="sxs-lookup"><span data-stu-id="eb99a-201">XMPP proxy external interface on the Access Edge service or Edge pool.Repeat as necessary for all internal SIP domains with Lync enabled users where contact with XMPP contacts is allowed through the configuration of the External Access Policy through a global policy, site policy where the user is located, or user policy applied to the Lync-enabled user.</span></span> <span data-ttu-id="eb99a-202">Разрешенный домен XMPP также должен быть настроен в политике федеративных партнеров XMPP.</span><span class="sxs-lookup"><span data-stu-id="eb99a-202">An allowed XMPP domain must also be configured in the XMPP Federated Partners policy.</span></span> <span data-ttu-id="eb99a-203">Дополнительные сведения <strong>можно</strong> найти в разделах.</span><span class="sxs-lookup"><span data-stu-id="eb99a-203">See topics in <strong>See Also</strong> for additional details</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb99a-204">Внешние DNS/A</span><span class="sxs-lookup"><span data-stu-id="eb99a-204">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="eb99a-205">xmpp.contoso.com (например)</span><span class="sxs-lookup"><span data-stu-id="eb99a-205">xmpp.contoso.com (for example)</span></span></p></td>
<td><p><span data-ttu-id="eb99a-206">IP-адрес службы пограничного доступа на пограничном сервере или в пограничном пуле, где размещен прокси-сервер XMPP</span><span class="sxs-lookup"><span data-stu-id="eb99a-206">IP address of Access Edge service on your Edge Server or Edge pool hosting XMPP proxy</span></span></p></td>
<td><p><span data-ttu-id="eb99a-207">Указывает на службу пограничного доступа или пул EDGE, на котором размещена служба прокси XMPP.</span><span class="sxs-lookup"><span data-stu-id="eb99a-207">Points to the Access Edge service or Edge pool that hosts the XMPP proxy service.</span></span> <span data-ttu-id="eb99a-208">Как правило, создаваемая SRV-запись будет указывать на эту запись узла (A или AAAA).</span><span class="sxs-lookup"><span data-stu-id="eb99a-208">Typically, the SRV record that you create will point to this host (A or AAAA) record</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="eb99a-209">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="eb99a-209">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

