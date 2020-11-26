---
title: 'Lync Server 2013: требования DNS для пулов переднего плана'
description: 'Lync Server 2013: требования DNS для пула переднего плана.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS requirements for Front End pool
ms:assetid: 02d2aa6b-9e01-437b-a2df-00590280150d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398082(v=OCS.15)
ms:contentKeyID: 48183249
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bfce90eccb8c8dff94d4122c96c4ca68ea9150f1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437828"
---
# <a name="dns-requirements-for-front-end-pool-in-lync-server-2013"></a><span data-ttu-id="00674-103">Требования DNS для пулов переднего плана в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="00674-103">DNS requirements for Front End pool in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="00674-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="00674-104">

<span> </span></span></span>

<span data-ttu-id="00674-105">_**Тема последнего изменения:** 2012-11-07_</span><span class="sxs-lookup"><span data-stu-id="00674-105">_**Topic Last Modified:** 2012-11-07_</span></span>

<span data-ttu-id="00674-106">Для успешного выполнения этой процедуры необходимо войти в систему на сервере или в домене в группу администраторов домена или в группу пользователей DnsAdmins.</span><span class="sxs-lookup"><span data-stu-id="00674-106">To successfully complete this procedure, you should be logged on to the server or domain minimally as a member of the Domain Admins group or a member of the DnsAdmins group.</span></span>

<span data-ttu-id="00674-107">Прежде чем публиковать топологию в построителе топологии, необходимо настроить нужные записи DNS (Domain Name System).</span><span class="sxs-lookup"><span data-stu-id="00674-107">You need to configure the required Domain Name System (DNS) records prior to publishing your topology in Topology Builder.</span></span> <span data-ttu-id="00674-108">Кроме того, некоторые полные доменные имена, используемые в конфигурации Lync Server 2013, являются логическими, а не физическими (FQDN), поэтому перед публикацией требуется дополнительная настройка DNS.</span><span class="sxs-lookup"><span data-stu-id="00674-108">Additionally, some of the fully qualified domain names (FQDNs) used in the configuration of a Lync Server 2013 deployment are logical and not physical server FQDNs, so additional DNS configuration is required prior to publishing.</span></span>

<div>


> [!WARNING]  
> <span data-ttu-id="00674-109">Lync Server 2013 не поддерживает домены, помеченные как единые.</span><span class="sxs-lookup"><span data-stu-id="00674-109">Lync Server 2013 does not support single-labeled domains.</span></span> <span data-ttu-id="00674-110">Например, лес с корневым доменом с именем <STRONG>contoso. local</STRONG> поддерживается, но корневой домен с именем <STRONG>Local</STRONG> не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="00674-110">For example, a forest with a root domain named <STRONG>contoso.local</STRONG> is supported, but a root domain named <STRONG>local</STRONG> is not supported.</span></span> <span data-ttu-id="00674-111">Подробные сведения о том, как настроить Windows для доменов с DNS-именами, сопоставленными с одной меткой, можно найти в статье 300684 (at <A class=uri href="https://go.microsoft.com/fwlink/p/?linkid=3052%26kbid=300684"> https://go.microsoft.com/fwlink/p/?linkid=3052&amp ; kbid = 300684</A>.</span><span class="sxs-lookup"><span data-stu-id="00674-111">For details, see Microsoft Knowledge Base article 300684, “Information about configuring Windows for domains with single-label DNS names,” at <A class=uri href="https://go.microsoft.com/fwlink/p/?linkid=3052%26kbid=300684">https://go.microsoft.com/fwlink/p/?linkid=3052&amp;kbid=300684</A>.</span></span>



</div>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="00674-112">Указанное имя должно быть идентично имени компьютера, настроенному на сервере.</span><span class="sxs-lookup"><span data-stu-id="00674-112">The name you specify must be identical to the computer name configured on the server.</span></span> <span data-ttu-id="00674-113">По умолчанию имя компьютера, не подключенного к домену, является коротким именем, а не FQDN.</span><span class="sxs-lookup"><span data-stu-id="00674-113">By default the computer name of a computer that is not joined to a domain is a short name, not an FQDN.</span></span> <span data-ttu-id="00674-114">Построитель топологии использует полные доменные имена, а не короткие имена.</span><span class="sxs-lookup"><span data-stu-id="00674-114">Topology Builder uses FQDNs, not short names.</span></span> <span data-ttu-id="00674-115">При назначении полных доменных имен серверам Lync Server, пограничным серверам и пулам <STRONG>Используйте только стандартные символы</STRONG> (включая A-z, a-z, 0 – 9 и дефисы).</span><span class="sxs-lookup"><span data-stu-id="00674-115"><STRONG>Use only standard characters</STRONG> (including A–Z, a–z, 0–9, and hyphens) when assigning FQDNs of your servers running Lync Server, Edge Servers, and pools.</span></span> <span data-ttu-id="00674-116">Не используйте символы Unicode или подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="00674-116">Do not use Unicode characters or underscores.</span></span> <span data-ttu-id="00674-117">Нестандартные символы в полном доменном имени часто не поддерживаются внешними DNS-и общедоступными центрами сертификации (ЦС) (когда полное доменное имя должно быть назначено для SN в сертификате).</span><span class="sxs-lookup"><span data-stu-id="00674-117">Nonstandard characters in an FQDN are often not supported by external DNS and public certification authorities (CAs) (when the FQDN must be assigned to the SN in the certificate).</span></span>



</div>

<span data-ttu-id="00674-118">Перед тем как приступать к работе с топологией после ее развертывания, убедитесь в том, что созданы указанные ниже записи Active Directory и DNS (в зависимости от того, что требуется для определенных функций):</span><span class="sxs-lookup"><span data-stu-id="00674-118">Prior to operating the topology after it has been deployed, ensure that the following Active Directory and DNS records are created (as your needs for specific features dictate):</span></span>

  - <span data-ttu-id="00674-119">Все роли сервера, которые будут существовать в топологии, публикуются как объект Active Directory (это можно сделать с помощью присоединения компьютера к домену).</span><span class="sxs-lookup"><span data-stu-id="00674-119">Each server role that will exist in the topology is published as an Active Directory object (joining the computer to the domain will accomplish this).</span></span>

  - <span data-ttu-id="00674-120">Для каждого сервера существует запись DNS A.</span><span class="sxs-lookup"><span data-stu-id="00674-120">A DNS A Record exists for each server.</span></span>

  - <span data-ttu-id="00674-121">DNS SRV-запись для каждого домена SIP используется, если вы планируете использовать автоматический вход в систему для клиентов в форме \_ sipinternaltls \_ TCP. \<SIP domain\> .</span><span class="sxs-lookup"><span data-stu-id="00674-121">A DNS SRV Record exists for each SIP domain if you plan to use automatic logon for clients in the form of \_sipinternaltls\_tcp.\<SIP domain\>.</span></span> <span data-ttu-id="00674-122">Если вы будете использовать ручную настройку для клиентов, эта запись не требуется.</span><span class="sxs-lookup"><span data-stu-id="00674-122">If you will use manual configuration for clients, this record is not necessary.</span></span>

  - <span data-ttu-id="00674-123">Запись DNS A для каждого настроенного простого URL-адреса, который обычно состоит из четырех: "Встреча", "Входящие", "LWA" и "Планировщик".</span><span class="sxs-lookup"><span data-stu-id="00674-123">A DNS A Record for each configured simple URL, of which there are typically four: meet, dialin, lwa, and scheduler.</span></span> <span data-ttu-id="00674-124">Кроме того, существует простой URL-адрес администратора, который является специальным URL-адресом для доступа к панели управления Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="00674-124">Additionally, there is the admin simple URL which is a special URL for access to the Lync Server 2013 Control Panel.</span></span>

  - <span data-ttu-id="00674-125">Сервер, на котором работает SQL Server, должен быть присоединен к домену и доступен на компьютере, с которого построитель топологии выполняет публикацию.</span><span class="sxs-lookup"><span data-stu-id="00674-125">The server running SQL Server must be joined to the domain, and reachable by the computer that Topology Builder is publishing from.</span></span>

<span data-ttu-id="00674-126">В таблице ниже приведены справочные архитектуры, представленные в разделе Планирование.</span><span class="sxs-lookup"><span data-stu-id="00674-126">The table follows the reference architectures presented in the Planning section.</span></span> <span data-ttu-id="00674-127">Дополнительные сведения можно найти [в разделе сценарии доступа внешних пользователей в Lync Server 2013](lync-server-2013-scenarios-for-external-user-access.md) в документации по планированию.</span><span class="sxs-lookup"><span data-stu-id="00674-127">For details, see [Scenarios for external user access in Lync Server 2013](lync-server-2013-scenarios-for-external-user-access.md) in the Planning documentation.</span></span>

<div id="sectionSection0" class="section">

### <a name="dns-records-required-for-the-front-end-pool"></a><span data-ttu-id="00674-128">DNS-записи, необходимые для пула переднего плана</span><span class="sxs-lookup"><span data-stu-id="00674-128">DNS Records Required for the Front End pool</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="00674-129">Расположение</span><span class="sxs-lookup"><span data-stu-id="00674-129">Location</span></span></th>
<th><span data-ttu-id="00674-130">Тип</span><span class="sxs-lookup"><span data-stu-id="00674-130">Type</span></span></th>
<th><span data-ttu-id="00674-131">Полное доменное имя</span><span class="sxs-lookup"><span data-stu-id="00674-131">FQDN</span></span></th>
<th><span data-ttu-id="00674-132">Карты и примечания</span><span class="sxs-lookup"><span data-stu-id="00674-132">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="00674-133">Внутренняя DNS</span><span class="sxs-lookup"><span data-stu-id="00674-133">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="00674-134">А</span><span class="sxs-lookup"><span data-stu-id="00674-134">A</span></span></p></td>
<td><p><span data-ttu-id="00674-135">pool01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="00674-135">pool01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="00674-136">Pool01 (Балансировка нагрузки DNS).</span><span class="sxs-lookup"><span data-stu-id="00674-136">Pool01 (DNS load balancing).</span></span> <span data-ttu-id="00674-137">Требуется запись DNS A для IP-адреса каждого сервера переднего плана в пуле, сопоставленная с полным доменным именем пула.</span><span class="sxs-lookup"><span data-stu-id="00674-137">Requires a DNS A record for the IP address of each Front End Server within the pool, mapping to the pool FQDN.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="00674-138">Внутренняя DNS</span><span class="sxs-lookup"><span data-stu-id="00674-138">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="00674-139">А</span><span class="sxs-lookup"><span data-stu-id="00674-139">A</span></span></p></td>
<td><p><span data-ttu-id="00674-140">pool01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="00674-140">pool01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="00674-141">Pool01 (виртуальный IP-адрес (VIP) балансировщика аппаратной балансировки нагрузки).</span><span class="sxs-lookup"><span data-stu-id="00674-141">Pool01 (virtual IP (VIP) of hardware load balancer).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="00674-142">Внутренняя DNS</span><span class="sxs-lookup"><span data-stu-id="00674-142">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="00674-143">А</span><span class="sxs-lookup"><span data-stu-id="00674-143">A</span></span></p></td>
<td><p><span data-ttu-id="00674-144">fe01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="00674-144">fe01.contoso.net</span></span></p>
<p><span data-ttu-id="00674-145">fe02.contoso.net</span><span class="sxs-lookup"><span data-stu-id="00674-145">fe02.contoso.net</span></span></p>
<p><span data-ttu-id="00674-146">fe03.contoso.net</span><span class="sxs-lookup"><span data-stu-id="00674-146">fe03.contoso.net</span></span></p>
<p><span data-ttu-id="00674-147">…</span><span class="sxs-lookup"><span data-stu-id="00674-147">…</span></span></p></td>
<td><p><span data-ttu-id="00674-148">Сервер Pool01 переднего плана (узел 1).</span><span class="sxs-lookup"><span data-stu-id="00674-148">Pool01 Front End Server (NODE 1).</span></span></p>
<p><span data-ttu-id="00674-149">Сервер Pool01 переднего плана (узел 2).</span><span class="sxs-lookup"><span data-stu-id="00674-149">Pool01 Front End Server (NODE 2).</span></span></p>
<p><span data-ttu-id="00674-150">Сервер Pool01 переднего плана (узел 3).</span><span class="sxs-lookup"><span data-stu-id="00674-150">Pool01 Front End Server (NODE 3).</span></span></p>
<p><span data-ttu-id="00674-151">…</span><span class="sxs-lookup"><span data-stu-id="00674-151">…</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="00674-152">Внутренняя DNS</span><span class="sxs-lookup"><span data-stu-id="00674-152">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="00674-153">А</span><span class="sxs-lookup"><span data-stu-id="00674-153">A</span></span></p></td>
<td><p><span data-ttu-id="00674-154">fe02.contoso.net</span><span class="sxs-lookup"><span data-stu-id="00674-154">fe02.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="00674-155">Сервер Pool01 переднего плана (узел 2).</span><span class="sxs-lookup"><span data-stu-id="00674-155">Pool01 Front End Server (NODE 2).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="00674-156">Внутренняя DNS</span><span class="sxs-lookup"><span data-stu-id="00674-156">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="00674-157">А</span><span class="sxs-lookup"><span data-stu-id="00674-157">A</span></span></p></td>
<td><p><span data-ttu-id="00674-158">lsweb.contoso.net</span><span class="sxs-lookup"><span data-stu-id="00674-158">lsweb.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="00674-159">Pool01 (VIP) для веб-трафика между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="00674-159">Pool01 (VIP) for client-to-server web traffic.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="00674-160">Внутренняя DNS</span><span class="sxs-lookup"><span data-stu-id="00674-160">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="00674-161">А</span><span class="sxs-lookup"><span data-stu-id="00674-161">A</span></span></p></td>
<td><p><span data-ttu-id="00674-162">sqlbe.contoso.net</span><span class="sxs-lookup"><span data-stu-id="00674-162">sqlbe.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="00674-163">Сервер Pool01 Server, на котором запущен SQL Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="00674-163">Pool01 Back End Server running SQL Server 2008 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="00674-164">Внутренняя DNS</span><span class="sxs-lookup"><span data-stu-id="00674-164">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="00674-165">А</span><span class="sxs-lookup"><span data-stu-id="00674-165">A</span></span></p></td>
<td><p><span data-ttu-id="00674-166">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="00674-166">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="00674-167">Требуется для Lync Phone Edition или для автоматического входа в систему клиентов без DNS SRV-записей и для строгого сопоставления доменов.</span><span class="sxs-lookup"><span data-stu-id="00674-167">Required for Lync Phone Edition, or automatic logon of clients without DNS SRV records, and for strict domain matching.</span></span> <span data-ttu-id="00674-168">Не является обязательным для всех случаев.</span><span class="sxs-lookup"><span data-stu-id="00674-168">Not required in all cases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="00674-169">Внутренняя DNS</span><span class="sxs-lookup"><span data-stu-id="00674-169">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="00674-170">А</span><span class="sxs-lookup"><span data-stu-id="00674-170">A</span></span></p></td>
<td><p><span data-ttu-id="00674-171">sip.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="00674-171">sip.fabrikam.com</span></span></p></td>
<td><p><span data-ttu-id="00674-172">Предполагается наличие второго домена SIP.</span><span class="sxs-lookup"><span data-stu-id="00674-172">Assumes a second SIP domain.</span></span> <span data-ttu-id="00674-173">Требуется для Lync Phone Edition, автоматического входа в систему клиентов без DNS SRV-записей и для строгого сопоставления доменов.</span><span class="sxs-lookup"><span data-stu-id="00674-173">Required for Lync Phone Edition, automatic logon of clients without DNS SRV records, and for strict domain matching.</span></span> <span data-ttu-id="00674-174">Не является обязательным для всех случаев.</span><span class="sxs-lookup"><span data-stu-id="00674-174">Not required in all cases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="00674-175">Внутренняя DNS</span><span class="sxs-lookup"><span data-stu-id="00674-175">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="00674-176">А</span><span class="sxs-lookup"><span data-stu-id="00674-176">A</span></span></p></td>
<td><p><span data-ttu-id="00674-177">dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="00674-177">dialin.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="00674-178">Простой URL-адрес для конференц-связи с телефонным подключением, опубликованный внутренне — сервер переднего плана (или режиссер, если он установлен) отвечает на простые URL-запросы.</span><span class="sxs-lookup"><span data-stu-id="00674-178">Simple URL for dial-in conferencing published internally – Front End Server (or Director, if installed) responds to simple URL queries.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="00674-179">Внутренняя DNS</span><span class="sxs-lookup"><span data-stu-id="00674-179">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="00674-180">А</span><span class="sxs-lookup"><span data-stu-id="00674-180">A</span></span></p></td>
<td><p><span data-ttu-id="00674-181">meet.contoso.com</span><span class="sxs-lookup"><span data-stu-id="00674-181">meet.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="00674-182">Простой URL-адрес для конференций, опубликованный внутренне — сервер переднего плана (или режиссер, если он установлен) отвечает на простые URL-запросы.</span><span class="sxs-lookup"><span data-stu-id="00674-182">Simple URL for conferences published internally – Front End Server (or Director, if installed) responds to simple URL queries.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="00674-183">Внутренняя DNS</span><span class="sxs-lookup"><span data-stu-id="00674-183">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="00674-184">А</span><span class="sxs-lookup"><span data-stu-id="00674-184">A</span></span></p></td>
<td><p><span data-ttu-id="00674-185">admin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="00674-185">admin.contoso.com</span></span></p>
<p><span data-ttu-id="00674-186">RAS</span><span class="sxs-lookup"><span data-stu-id="00674-186">admin</span></span></p></td>
<td><p><span data-ttu-id="00674-187">Необязательная запись, простой URL-адрес для панели управления Lync Server 2013, опубликованный внутренним образом сервер переднего плана (или режиссер, если он установлен) отвечает на простые URL-запросы.</span><span class="sxs-lookup"><span data-stu-id="00674-187">Optional record, simple URL for Lync Server 2013 Control Panel published internally - Front End Server (or Director, if installed) responds to simple URL queries.</span></span> <span data-ttu-id="00674-188">Рекомендуется только имя узла (имя домена не поддерживается).</span><span class="sxs-lookup"><span data-stu-id="00674-188">Host name only (no domain name) is recommended.</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="00674-189">VIP = виртуальный IP-адрес для подсистемы балансировки нагрузки для оборудования</span><span class="sxs-lookup"><span data-stu-id="00674-189">VIP = Virtual IP address for hardware load balancer</span></span>



</div>

</div>

<div>

## <a name="dns-srv-records-for-the-front-end-pool"></a><span data-ttu-id="00674-190">Записи DNS SRV для пула переднего плана</span><span class="sxs-lookup"><span data-stu-id="00674-190">DNS SRV Records for the Front End pool</span></span>


<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="00674-191">Расположение</span><span class="sxs-lookup"><span data-stu-id="00674-191">Location</span></span></th>
<th><span data-ttu-id="00674-192">Тип</span><span class="sxs-lookup"><span data-stu-id="00674-192">Type</span></span></th>
<th><span data-ttu-id="00674-193">Полное доменное имя</span><span class="sxs-lookup"><span data-stu-id="00674-193">FQDN</span></span></th>
<th><span data-ttu-id="00674-194">Целевое полное доменное имя</span><span class="sxs-lookup"><span data-stu-id="00674-194">Target FQDN</span></span></th>
<th><span data-ttu-id="00674-195">Порт</span><span class="sxs-lookup"><span data-stu-id="00674-195">Port</span></span></th>
<th><span data-ttu-id="00674-196">Карты и примечания</span><span class="sxs-lookup"><span data-stu-id="00674-196">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="00674-197">Внутренняя DNS</span><span class="sxs-lookup"><span data-stu-id="00674-197">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="00674-198">SRV</span><span class="sxs-lookup"><span data-stu-id="00674-198">SRV</span></span></p></td>
<td><p><span data-ttu-id="00674-199">_sipinternaltls _sipinternaltls._tcp. contoso. com</span><span class="sxs-lookup"><span data-stu-id="00674-199">_sipinternaltls._tcp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="00674-200">pool01.contoso.com</span><span class="sxs-lookup"><span data-stu-id="00674-200">pool01.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="00674-201">5061</span><span class="sxs-lookup"><span data-stu-id="00674-201">5061</span></span></p></td>
<td><p><span data-ttu-id="00674-202">Требуется для автоматической настройки клиентов Lync 2013 для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="00674-202">Required for automatic configuration of Lync 2013 clients to work internally.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="00674-203">Внутренняя DNS</span><span class="sxs-lookup"><span data-stu-id="00674-203">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="00674-204">SRV</span><span class="sxs-lookup"><span data-stu-id="00674-204">SRV</span></span></p></td>
<td><p><span data-ttu-id="00674-205">_sipinternaltls _sipinternaltls._tcp. fabrikam. com</span><span class="sxs-lookup"><span data-stu-id="00674-205">_sipinternaltls._tcp.fabrikam.com</span></span></p></td>
<td><p><span data-ttu-id="00674-206">pool01.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="00674-206">pool01.fabrikam.com</span></span></p></td>
<td><p><span data-ttu-id="00674-207">5061</span><span class="sxs-lookup"><span data-stu-id="00674-207">5061</span></span></p></td>
<td><p><span data-ttu-id="00674-208">Требуется для автоматической настройки клиентов Lync 2013 для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="00674-208">Required for automatic configuration of Lync 2013 clients to work internally.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="00674-209">Внутренняя DNS</span><span class="sxs-lookup"><span data-stu-id="00674-209">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="00674-210">SRV</span><span class="sxs-lookup"><span data-stu-id="00674-210">SRV</span></span></p></td>
<td><p><span data-ttu-id="00674-211">_ntp _ntp._udp. contoso. com</span><span class="sxs-lookup"><span data-stu-id="00674-211">_ntp._udp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="00674-212">dc01.contoso.com</span><span class="sxs-lookup"><span data-stu-id="00674-212">dc01.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="00674-213">123</span><span class="sxs-lookup"><span data-stu-id="00674-213">123</span></span></p></td>
<td><p><span data-ttu-id="00674-214">Для устройств с Lync Phone Edition требуется источник сетевого времени (NTP).</span><span class="sxs-lookup"><span data-stu-id="00674-214">Network Time Protocol (NTP) source required for devices running Lync Phone Edition.</span></span> <span data-ttu-id="00674-215">На внутреннем уровне это значение должно указывать на контроллер домена.</span><span class="sxs-lookup"><span data-stu-id="00674-215">Internally, this should point to the domain controller.</span></span> <span data-ttu-id="00674-216">Если контроллер домена не определен, он попытается использовать сервер NTP time.windows.com.</span><span class="sxs-lookup"><span data-stu-id="00674-216">If the domain controller is not defined, it will try to use the NTP server time.windows.com.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="00674-217">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="00674-217">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

