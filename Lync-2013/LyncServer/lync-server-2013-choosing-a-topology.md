---
title: 'Lync Server 2013: выбор топологии'
description: 'Lync Server 2013: выбор топологии.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Choosing a topology
ms:assetid: 23f2aeb6-fed9-4349-8fba-dcbf18ee4b04
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425716(v=OCS.15)
ms:contentKeyID: 48183634
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 01ded739c3c5e4e0bd8c0f25f3f0fe8ff1f350b9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434910"
---
# <a name="choosing-a-topology-in-lync-server-2013"></a><span data-ttu-id="0157d-103">Выбор топологии в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0157d-103">Choosing a topology in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span data-ttu-id="0157d-104">_**Тема последнего изменения:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="0157d-104">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="0157d-105">При выборе топологии вы можете использовать один из указанных ниже вариантов топологии.</span><span class="sxs-lookup"><span data-stu-id="0157d-105">When you choose a topology, you can use one the following supported topology options:</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="0157d-106">Если не указано иное, если у вас есть опыт работы с Microsoft Lync Server 2010, здесь вы найдете рекомендации, описанные в этой статье в значительном неизменном виде.</span><span class="sxs-lookup"><span data-stu-id="0157d-106">Unless otherwise noted, if you have experience with Microsoft Lync Server 2010, you will find the guidance here is largely unchanged.</span></span>



</div>

  - [<span data-ttu-id="0157d-107">Единая консолидированная пограничная топология с закрытыми IP-адресами и трансляцией сетевых адресов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0157d-107">Single consolidated edge with private IP addresses and NAT in Lync Server 2013</span></span>](lync-server-2013-single-consolidated-edge-with-private-ip-addresses-and-nat.md)

  - [<span data-ttu-id="0157d-108">Единая консолидированная пограничная топология с общедоступными IP-адресами в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0157d-108">Single consolidated edge with public IP addresses in Lync Server 2013</span></span>](lync-server-2013-single-consolidated-edge-with-public-ip-addresses.md)

  - [<span data-ttu-id="0157d-109">Масштабируемая консолидированная пограничная топология, балансировка нагрузки на DNS с закрытыми IP-адресами и трансляцией сетевых адресов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0157d-109">Scaled consolidated edge, DNS load balancing with private IP addresses using NAT in Lync Server 2013</span></span>](lync-server-2013-scaled-consolidated-edge-dns-load-balancing-with-private-ip-addresses-using-nat.md)

  - [<span data-ttu-id="0157d-110">Масштабируемая консолидированная пограничная топология, балансировка нагрузки на DNS с общедоступными IP-адресами в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0157d-110">Scaled consolidated edge, DNS load balancing with public IP addresses in Lync Server 2013</span></span>](lync-server-2013-scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses.md)

  - [<span data-ttu-id="0157d-111">Масштабируемая консолидированная пограничная топология с аппаратными балансировщиками нагрузки в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0157d-111">Scaled consolidated edge with hardware load balancers in Lync Server 2013</span></span>](lync-server-2013-scaled-consolidated-edge-with-hardware-load-balancers.md)

<div>


> [!IMPORTANT]
> <span data-ttu-id="0157d-112">Балансировка нагрузки на внутреннем и внешнем пограничным интерфейсах должна относиться к одному и тому же типу.</span><span class="sxs-lookup"><span data-stu-id="0157d-112">The internal Edge interface and external Edge interface must use the same type of load balancing.</span></span> <span data-ttu-id="0157d-113">Невозможно осуществлять балансировку нагрузки на одном пограничном интерфейсе средствами DNS, а на другом — аппаратными средствами.</span><span class="sxs-lookup"><span data-stu-id="0157d-113">You cannot use DNS load balancing on one Edge interface and hardware load balancing on the other Edge interface.</span></span>



</div>

<span data-ttu-id="0157d-114">В таблице ниже перечислены функции, доступные при использовании поддерживаемых топологий Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0157d-114">The following table summarizes the functionality available with the supported Microsoft Lync Server 2013 topologies.</span></span> <span data-ttu-id="0157d-115">Заголовки столбцов обозначают функциональные возможности, доступные для определенного параметра конфигурации Edge.</span><span class="sxs-lookup"><span data-stu-id="0157d-115">The column headings indicate the functionality available for a given Edge configuration option.</span></span> <span data-ttu-id="0157d-116">С помощью масштабируемого EDGE (Балансировка нагрузки DNS) в качестве примера вы видите, что он поддерживает высокий уровень доступности, может использовать частные IP-адреса без маршрутизации (с NAT) или маршрутизацию общедоступных IP-адресов, назначенных внешним интерфейсам периметра, и сокращает расходы, так как подсистема балансировки нагрузки аппаратных средств не требуется.</span><span class="sxs-lookup"><span data-stu-id="0157d-116">Using the Scaled Edge (DNS load balanced) option as an example, you can see that it supports high availability, can use non-routable private IP addresses (with NAT) or routable public IP addresses assigned to the Edge external interfaces, and reduces cost because a hardware load balancer is not required.</span></span>

<span data-ttu-id="0157d-117">Сценарии пограничного отработки отказа, поддерживаемые с помощью балансировки нагрузки DNS, являются сеансами "точка-точка" Lync-to-Lync, сеансами конференции Lync, семинарами Lync-to-Point, Office 365 и Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="0157d-117">Edge failover scenarios supported with DNS Load Balancing are Lync-to-Lync point-to-point sessions, Lync conferencing sessions, Lync-to-PSTN sessions, Office 365, and Microsoft 365.</span></span> <span data-ttu-id="0157d-118">Сценарии отработки отказа, которые не выигрывают от балансировки нагрузки DNS, отправляются для удаленной системы обмена сообщениями Exchange (до Exchange 2010 SP1), общедоступной службы обмена мгновенными сообщениями (IM) и Федерации с серверами с установленным пакетом Office Communications Server.</span><span class="sxs-lookup"><span data-stu-id="0157d-118">Edge failover scenarios that do not benefit from DNS Load Balancing are failover for remote user Exchange Unified Messaging (UM) (prior to Exchange 2010 SP1), public instant messaging (IM) connectivity, and federation with servers running Office Communications Server.</span></span>

### <a name="summary-of-edge-server-topology-options"></a><span data-ttu-id="0157d-119">Общие сведения о параметрах топологии пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="0157d-119">Summary of Edge Server Topology Options</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0157d-120">Топология</span><span class="sxs-lookup"><span data-stu-id="0157d-120">Topology</span></span></th>
<th><span data-ttu-id="0157d-121">Высокая доступность</span><span class="sxs-lookup"><span data-stu-id="0157d-121">High availability</span></span></th>
<th><span data-ttu-id="0157d-122">Дополнительные записи DNS A, необходимые для внешнего пограничного сервера в пуле Edge</span><span class="sxs-lookup"><span data-stu-id="0157d-122">Additional DNS A records required for external Edge Server in the Edge pool</span></span></th>
<th><span data-ttu-id="0157d-123">Отработка отказа для сеансов Lync-to-Lync</span><span class="sxs-lookup"><span data-stu-id="0157d-123">Edge Failover for Lync-to-Lync sessions</span></span></th>
<th><span data-ttu-id="0157d-124">Отработка отказа в сеансах интеграции Lync-to-Lync EUM/PIC/OCS</span><span class="sxs-lookup"><span data-stu-id="0157d-124">Edge Failover for Lync-to-Lync EUM/PIC/OCS Federation sessions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0157d-125">Один край с помощью NAT</span><span class="sxs-lookup"><span data-stu-id="0157d-125">Single Edge using NAT</span></span></p></td>
<td><p><span data-ttu-id="0157d-126">Нет</span><span class="sxs-lookup"><span data-stu-id="0157d-126">No</span></span></p></td>
<td><p><span data-ttu-id="0157d-127">Нет</span><span class="sxs-lookup"><span data-stu-id="0157d-127">No</span></span></p></td>
<td><p><span data-ttu-id="0157d-128">Нет</span><span class="sxs-lookup"><span data-stu-id="0157d-128">No</span></span></p></td>
<td><p><span data-ttu-id="0157d-129">Нет</span><span class="sxs-lookup"><span data-stu-id="0157d-129">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0157d-130">Один край с общедоступным IP-адресом</span><span class="sxs-lookup"><span data-stu-id="0157d-130">Single Edge using Public IP</span></span></p></td>
<td><p><span data-ttu-id="0157d-131">Нет</span><span class="sxs-lookup"><span data-stu-id="0157d-131">No</span></span></p></td>
<td><p><span data-ttu-id="0157d-132">Нет</span><span class="sxs-lookup"><span data-stu-id="0157d-132">No</span></span></p></td>
<td><p><span data-ttu-id="0157d-133">Нет</span><span class="sxs-lookup"><span data-stu-id="0157d-133">No</span></span></p></td>
<td><p><span data-ttu-id="0157d-134">Нет</span><span class="sxs-lookup"><span data-stu-id="0157d-134">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0157d-135">Масштабируемый край (Балансировка нагрузки DNS) с использованием NAT</span><span class="sxs-lookup"><span data-stu-id="0157d-135">Scaled Edge (DNS Load Balanced) using NAT</span></span></p></td>
<td><p><span data-ttu-id="0157d-136">Да</span><span class="sxs-lookup"><span data-stu-id="0157d-136">Yes</span></span></p></td>
<td><p><span data-ttu-id="0157d-137">Да</span><span class="sxs-lookup"><span data-stu-id="0157d-137">Yes</span></span></p></td>
<td><p><span data-ttu-id="0157d-138">Да</span><span class="sxs-lookup"><span data-stu-id="0157d-138">Yes</span></span></p></td>
<td><p>*</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0157d-139">Масштабируемый край (Балансировка нагрузки DNS) с использованием общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="0157d-139">Scaled Edge (DNS Load Balanced) using Public IP</span></span></p></td>
<td><p><span data-ttu-id="0157d-140">Да</span><span class="sxs-lookup"><span data-stu-id="0157d-140">Yes</span></span></p></td>
<td><p><span data-ttu-id="0157d-141">Да</span><span class="sxs-lookup"><span data-stu-id="0157d-141">Yes</span></span></p></td>
<td><p><span data-ttu-id="0157d-142">Да</span><span class="sxs-lookup"><span data-stu-id="0157d-142">Yes</span></span></p></td>
<td><p>*</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0157d-143">Балансировка нагрузки аппаратных средств с масштабированным краем</span><span class="sxs-lookup"><span data-stu-id="0157d-143">Scaled Edge Hardware load balanced)</span></span></p></td>
<td><p><span data-ttu-id="0157d-144">Да</span><span class="sxs-lookup"><span data-stu-id="0157d-144">Yes</span></span></p></td>
<td><p><span data-ttu-id="0157d-145">Нет (одна запись A DNS на каждый виртуальный IP-адрес)</span><span class="sxs-lookup"><span data-stu-id="0157d-145">No (one DNS A record per VIP)</span></span></p></td>
<td><p><span data-ttu-id="0157d-146">Да</span><span class="sxs-lookup"><span data-stu-id="0157d-146">Yes</span></span></p></td>
<td><p><span data-ttu-id="0157d-147">Да</span><span class="sxs-lookup"><span data-stu-id="0157d-147">Yes</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0157d-148">\**\** _ Отработка отказа для подключения к общедоступной службе обмена мгновенными сообщениями и интеграция с серверами с установленным пакетом Office Communications Server недоступна при балансировке нагрузки DNS.</span><span class="sxs-lookup"><span data-stu-id="0157d-148">\**\** _ Failover for public instant messaging (IM) connectivity, and federation with servers running Office Communications Server is not available with DNS load balancing.</span></span> <span data-ttu-id="0157d-149">Переключение на другой ресурс Exchange UM (удаленный пользователь) с помощью балансировки нагрузки DNS требует наличия Exchange Server 2010 SP1 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="0157d-149">Exchange UM (remote user) failover using DNS load balancing requires Exchange Server 2010 SP1 or newer.</span></span>



> [!NOTE]
> <span data-ttu-id="0157d-150">Топологии с одним краем и масштабированным краем (Балансировка нагрузки DNS) может использовать:</span><span class="sxs-lookup"><span data-stu-id="0157d-150">Single Edge and Scaled Edge (DNS load balanced) topologies can use:</span></span>
> <ul><li><p><span data-ttu-id="0157d-151">Маршрутизируемые общедоступные IP-адреса</span><span class="sxs-lookup"><span data-stu-id="0157d-151">Routable public IP addresses</span></span></p></li>
> <li><p><span data-ttu-id="0157d-152">Частный IP-адрес без маршрутизации при использовании симметричного преобразования сетевых адресов (NAT)</span><span class="sxs-lookup"><span data-stu-id="0157d-152">Non-routable private IP address if symmetric network address translation (NAT) is used</span></span></p></li>
>
> <ul><li> <span data-ttu-id="0157d-153">Если вы используете общедоступный IP-адрес или частный IP-адрес с помощью NAT, вы по-прежнему будете использовать одинаковое количество IP-адресов на основе выбора конфигурации в построителе топологии.</span><span class="sxs-lookup"><span data-stu-id="0157d-153">If you use public IP address or private IP address with NAT, you will still use the same number of IP addresses based on your configuration choice in Topology Builder.</span></span> <span data-ttu-id="0157d-154">Вы можете настроить пограничный сервер на использование одного IP-адреса с разными портами для каждой службы или использовать отдельные IP-адреса для каждой службы, но использовать один и тот же порт (по умолчанию — TCP 443).</span><span class="sxs-lookup"><span data-stu-id="0157d-154">You can configure the Edge Server to use a single IP address with distinct ports per service, or use distinct IP addresses per service, but use the same port (by default, TCP 443).</span></span></li></ul>>
> <span data-ttu-id="0157d-155">Если вы решили использовать для NAT частные IP-адреса без маршрутизации, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="0157d-155">If you decide to use non-routable private IP addresses with NAT:</span></span>
> <ul><li><p><span data-ttu-id="0157d-156">Для всех трех внешних интерфейсов необходимо использовать маршрутизируемый частный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="0157d-156">You must use routable private IP addresses on all three external interfaces</span></span></p></li>
> <li><p><span data-ttu-id="0157d-157">Необходимо настроить Симметричный NAT для входящего и исходящего трафика.</span><span class="sxs-lookup"><span data-stu-id="0157d-157">You must configure symmetric NAT for incoming and outgoing traffic</span></span></p></li></ul>>
> <span data-ttu-id="0157d-158">В топологии с масштабированным краем (Балансировка нагрузки оборудования) должны использоваться общедоступные IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="0157d-158">Scaled Edge (hardware load balanced) topology must use public IP addresses.</span></span>



<span data-ttu-id="0157d-159">Lync Server 2013 поддерживает размещение Access, веб-конференций и внешних интерфейсов, расположенных за маршрутизатором или брандмауэром, выполняющим преобразование сетевых адресов (NAT) для одномерной и масштабируемой топологии пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="0157d-159">Lync Server 2013 supports placing Access, Web Conferencing, and A/V Edge external interfaces behind a router or firewall that performs network address translation (NAT) for both single and scaled consolidated Edge Server topologies.</span></span>

<span data-ttu-id="0157d-160">Использование NAT для всех внешних интерфейсов пограничного сервера требует использования балансировки нагрузки DNS.</span><span class="sxs-lookup"><span data-stu-id="0157d-160">Using NAT for all Edge external interfaces requires the use of DNS load balancing.</span></span> <span data-ttu-id="0157d-161">При сравнении с использованием подсистем балансировки нагрузки для аппаратных средств, использующих NLB, вы можете сократить количество общедоступных IP-адресов на пограничном сервере в пуле EDGE, как описано в следующем списке.</span><span class="sxs-lookup"><span data-stu-id="0157d-161">When compared to using hardware load balancers, using DNS load balancing without NAT allows you to reduce the number of public IP address per Edge Server in an Edge pool as described in the following list:</span></span>

  - <span data-ttu-id="0157d-162">Для Lync Server 2013 с масштабированным консолидированным краем (Балансировка нагрузки DNS) требуется три общедоступных IP-адреса для каждого пограничного сервера в пуле Edge.</span><span class="sxs-lookup"><span data-stu-id="0157d-162">Lync Server 2013 Scaled Consolidated Edge (DNS load balanced) Requires three public IP addresses for each Edge Server in an Edge pool.</span></span>

  - <span data-ttu-id="0157d-163">Для Lync Server 2013 Scaleed EDGE (Балансировка нагрузки оборудования) для виртуальных IP-адресов подсистемы балансировки нагрузки требуется три общедоступных IP-адреса (требования, которые не помещаются в пул) плюс три общедоступных IP-адреса на пограничном сервере в пуле.</span><span class="sxs-lookup"><span data-stu-id="0157d-163">Lync Server 2013 Scaled Consolidated Edge (hardware load balanced) Requires three public IP address for load balancer virtual IP addresses (one time requirement that does not increment as more Edge Servers are added to the pool) plus three public IP addresses per Edge Server in a pool.</span></span>

### <a name="ip-address-requirements-for-scaled-consolidated-edge-ip-address-per-role"></a><span data-ttu-id="0157d-164">Требования к IP-адресу для масштабируемой консолидированной кромки (IP-адрес на роль)</span><span class="sxs-lookup"><span data-stu-id="0157d-164">IP Address Requirements for Scaled Consolidated Edge (IP Address per role)</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0157d-165">Число пограничных серверов в пуле</span><span class="sxs-lookup"><span data-stu-id="0157d-165">Number of Edge Servers per pool</span></span></th>
<th><span data-ttu-id="0157d-166">Число необходимых IP-адресов Lync Server 2013 (Балансировка нагрузки DNS)</span><span class="sxs-lookup"><span data-stu-id="0157d-166">Number of required IP addresses Lync Server 2013 (DNS load balanced)</span></span></th>
<th><span data-ttu-id="0157d-167">Число обязательных IP-адресов, Lync Server 2013 (Балансировка нагрузки оборудования)</span><span class="sxs-lookup"><span data-stu-id="0157d-167">Number of required IP addresses Lync Server 2013 (hardware load balanced)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0157d-168">2</span><span class="sxs-lookup"><span data-stu-id="0157d-168">2</span></span></p></td>
<td><p><span data-ttu-id="0157d-169">6</span><span class="sxs-lookup"><span data-stu-id="0157d-169">6</span></span></p></td>
<td><p><span data-ttu-id="0157d-170">3 (по 1 на виртуальный IP-адрес) + 6</span><span class="sxs-lookup"><span data-stu-id="0157d-170">3 (1 per VIP) + 6</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0157d-171">3</span><span class="sxs-lookup"><span data-stu-id="0157d-171">3</span></span></p></td>
<td><p><span data-ttu-id="0157d-172">@</span><span class="sxs-lookup"><span data-stu-id="0157d-172">9</span></span></p></td>
<td><p><span data-ttu-id="0157d-173">3 (по 1 на виртуальный IP-адрес) + 9</span><span class="sxs-lookup"><span data-stu-id="0157d-173">3 (1 per VIP) + 9</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0157d-174">4</span><span class="sxs-lookup"><span data-stu-id="0157d-174">4</span></span></p></td>
<td><p><span data-ttu-id="0157d-175">12</span><span class="sxs-lookup"><span data-stu-id="0157d-175">12</span></span></p></td>
<td><p><span data-ttu-id="0157d-176">3 (по 1 на виртуальный IP-адрес) + 12</span><span class="sxs-lookup"><span data-stu-id="0157d-176">3 (1 per VIP) + 12</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0157d-177">5</span><span class="sxs-lookup"><span data-stu-id="0157d-177">5</span></span></p></td>
<td><p><span data-ttu-id="0157d-178">10-15</span><span class="sxs-lookup"><span data-stu-id="0157d-178">15</span></span></p></td>
<td><p><span data-ttu-id="0157d-179">3 (1 на виртуальный IP-адрес) + 15</span><span class="sxs-lookup"><span data-stu-id="0157d-179">3 (1 per VIP) + 15</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="ip-address-requirements-for-scaled-consolidated-edge-single-ip-address-for-all-roles"></a><span data-ttu-id="0157d-180">Требования к IP-адресу для масштабируемой консолидированной кромки (один IP-адрес для всех ролей)</span><span class="sxs-lookup"><span data-stu-id="0157d-180">IP Address Requirements for Scaled Consolidated Edge (Single IP address for all roles)</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0157d-181">Число пограничных серверов в пуле</span><span class="sxs-lookup"><span data-stu-id="0157d-181">Number of Edge Servers per pool</span></span></th>
<th><span data-ttu-id="0157d-182">Число необходимых IP-адресов Lync Server 2013 (Балансировка нагрузки DNS)</span><span class="sxs-lookup"><span data-stu-id="0157d-182">Number of required IP addresses Lync Server 2013 (DNS load balanced)</span></span></th>
<th><span data-ttu-id="0157d-183">Число обязательных IP-адресов, Lync Server 2013 (Балансировка нагрузки оборудования)</span><span class="sxs-lookup"><span data-stu-id="0157d-183">Number of required IP addresses Lync Server 2013 (hardware load balanced)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0157d-184">2</span><span class="sxs-lookup"><span data-stu-id="0157d-184">2</span></span></p></td>
<td><p><span data-ttu-id="0157d-185">2</span><span class="sxs-lookup"><span data-stu-id="0157d-185">2</span></span></p></td>
<td><p><span data-ttu-id="0157d-186">1 (по 1 на виртуальный IP-адрес) + 2</span><span class="sxs-lookup"><span data-stu-id="0157d-186">1 (1 per VIP) + 2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0157d-187">3</span><span class="sxs-lookup"><span data-stu-id="0157d-187">3</span></span></p></td>
<td><p><span data-ttu-id="0157d-188">3</span><span class="sxs-lookup"><span data-stu-id="0157d-188">3</span></span></p></td>
<td><p><span data-ttu-id="0157d-189">1 (по 1 на виртуальный IP-адрес) + 3</span><span class="sxs-lookup"><span data-stu-id="0157d-189">1 (1 per VIP) + 3</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0157d-190">4</span><span class="sxs-lookup"><span data-stu-id="0157d-190">4</span></span></p></td>
<td><p><span data-ttu-id="0157d-191">4</span><span class="sxs-lookup"><span data-stu-id="0157d-191">4</span></span></p></td>
<td><p><span data-ttu-id="0157d-192">1 (по 1 на виртуальный IP-адрес) + 4</span><span class="sxs-lookup"><span data-stu-id="0157d-192">1 (1 per VIP) + 4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0157d-193">5</span><span class="sxs-lookup"><span data-stu-id="0157d-193">5</span></span></p></td>
<td><p><span data-ttu-id="0157d-194">5</span><span class="sxs-lookup"><span data-stu-id="0157d-194">5</span></span></p></td>
<td><p><span data-ttu-id="0157d-195">1 (по 1 на виртуальный IP-адрес) + 5</span><span class="sxs-lookup"><span data-stu-id="0157d-195">1 (1 per VIP) + 5</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0157d-196">Основные точки решения для выбора топологии — это высокая доступность и балансировка нагрузки.</span><span class="sxs-lookup"><span data-stu-id="0157d-196">The primary decision points for topology selection are high availability and load balancing.</span></span> <span data-ttu-id="0157d-197">Требование высокой доступности может повлиять на решение балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="0157d-197">The requirement for high availability can influence the load balancing decision.</span></span>

  - <span data-ttu-id="0157d-198">_ *Высокая доступность*\* если вам нужна высокая доступность, разверните по крайней мере два пограничных сервера в пуле.</span><span class="sxs-lookup"><span data-stu-id="0157d-198">_ *High availability*\*   If you need high availability, deploy at least two Edge Servers in a pool.</span></span> <span data-ttu-id="0157d-199">Один пул пограничного сервера обеспечивает поддержку до двенадцати пограничных серверов.</span><span class="sxs-lookup"><span data-stu-id="0157d-199">A single Edge pool will support up to twelve Edge Servers.</span></span> <span data-ttu-id="0157d-200">Если требуется дополнительная емкость, вы можете развернуть несколько пулов пограничных групп.</span><span class="sxs-lookup"><span data-stu-id="0157d-200">If more capacity is required, you can deploy multiple Edge pools.</span></span> <span data-ttu-id="0157d-201">Как правило, для 10% от данной базы пользователей потребуется внешний доступ.</span><span class="sxs-lookup"><span data-stu-id="0157d-201">As a general rule, 10% of a given user base will need external access.</span></span>
    
    <div>
    

    > [!IMPORTANT]
    > <span data-ttu-id="0157d-202">В построителе топологии вы можете настроить до двадцати пограничных серверов в одном пуле Edge.</span><span class="sxs-lookup"><span data-stu-id="0157d-202">Topology Builder will allow you to configure up to twenty Edge Servers in a single Edge pool.</span></span> <span data-ttu-id="0157d-203">Проверенное и поддерживаемое максимальное количество пограничных серверов в пуле — двенадцать, а построитель топологии — число больше двенадцати, которое не должно превышать двенадцать пограничных серверов в одном пуле пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="0157d-203">The tested and supported maximum number of Edge Servers in a pool is twelve and Topology Builder allowing for a number larger than twelve should not be construed as implied support for more than twelve Edge Servers in a single Edge pool.</span></span>

    
    </div>

  - <span data-ttu-id="0157d-204">**Балансировка нагрузки аппаратных средств**   Балансировка нагрузки оборудования поддерживается для балансировки нагрузки серверов Lync Server 2013 EDGE, если используется IP-адреса с общедоступной маршрутизацией для внешних интерфейсов Edge.</span><span class="sxs-lookup"><span data-stu-id="0157d-204">**Hardware load balancing**   Hardware load balancing is supported for load balancing Lync Server 2013 Edge Servers when using publicly routable IP addresses for the Edge external interfaces.</span></span> <span data-ttu-id="0157d-205">Например, этот подход следует использовать в ситуациях, когда для любого из следующих приложений требуется отработка отказа.</span><span class="sxs-lookup"><span data-stu-id="0157d-205">For example, you would use this approach in situations where failover is required for any of the following applications:</span></span>
    
      - <span data-ttu-id="0157d-206">Подключение к общедоступным системам обмена мгновенными сообщениями</span><span class="sxs-lookup"><span data-stu-id="0157d-206">Public IM connectivity</span></span>
    
      - <span data-ttu-id="0157d-207">Интеграция с компаниями, использующими Microsoft Office Communications Server 2007 или Microsoft Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="0157d-207">Federation with companies running Microsoft Office Communications Server 2007 or Microsoft Office Communications Server 2007 R2</span></span>
    
      - <span data-ttu-id="0157d-208">Внешний доступ к единой системе обмена сообщениями Exchange 2007 и Exchange 2010 (UM)</span><span class="sxs-lookup"><span data-stu-id="0157d-208">External access to Exchange 2007 Unified Messaging (UM) or Exchange 2010 UM</span></span>
        
        <div>
        

        > [!IMPORTANT]
        > <span data-ttu-id="0157d-209">Балансировка нагрузки DNS для Exchange 2010 с пакетом обновления 1 (SP1) и более поздних версий поддерживается для Exchange UM.</span><span class="sxs-lookup"><span data-stu-id="0157d-209">DNS load balancing for Exchange 2010 SP1 and newer is supported for Exchange UM.</span></span>

        
        </div>
    
    <span data-ttu-id="0157d-210">Эти три приложения продолжают работать, но они не поддерживают балансировку нагрузки DNS и будут подключены только к первому пограничного сервера в пуле.</span><span class="sxs-lookup"><span data-stu-id="0157d-210">These three applications will continue to operate, but they are not DNS load balancing aware and will only connect to the first Edge Server in the pool.</span></span> <span data-ttu-id="0157d-211">Если этот сервер недоступен, соединение закончится сбоем.</span><span class="sxs-lookup"><span data-stu-id="0157d-211">If that server is unavailable, the connection will fail.</span></span> <span data-ttu-id="0157d-212">Например, если в пуле развернуто несколько пограничных серверов для обработки загрузки федеративных данных, только один прокси-сервер доступа получает трафик, пока другие не простаивают.</span><span class="sxs-lookup"><span data-stu-id="0157d-212">For example, if multiple Edge Servers are deployed in a pool to handle the federated traffic load, only one access proxy actually receives traffic while the others are idle.</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="0157d-213">Использование балансировки нагрузки DNS рекомендуется, если вы собираетесь использовать в компании Lync Server 2010 и Office 365 или Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="0157d-213">Using DNS load balancing is recommended if you are federating with companies using Lync Server 2010 and Office 365 or Microsoft 365.</span></span> <span data-ttu-id="0157d-214">Имейте в виду, что в большинстве федеративных партнеров используется Office Communications Server 2007 или Office Communications Server 2007 R2, что влияет на производительность.</span><span class="sxs-lookup"><span data-stu-id="0157d-214">Be aware that there are significant performance impacts if most of your federated partners are using Office Communications Server 2007 or Office Communications Server 2007 R2.</span></span>



<span data-ttu-id="0157d-215"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0157d-215"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

