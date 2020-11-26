---
title: 'Lync Server 2013: определение требований к внешнему брандмауэру аудио- и видеосвязи и портам'
description: 'Lync Server 2013: Определите требования к внешнему брандмауэру и порту/V.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Determine external A/V firewall and port requirements
ms:assetid: 3b849dc7-175d-40d1-820d-80e6ade6d332
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425882(v=OCS.15)
ms:contentKeyID: 48183872
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 38c2a8c1e8e332a4a1e65adb87a1e962e82941c2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429518"
---
# <a name="determine-external-av-firewall-and-port-requirements-for-lync-server-2013"></a><span data-ttu-id="c8b90-103">Определение требований к внешнему брандмауэру аудио- и видеосвязи и портам для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c8b90-103">Determine external A/V firewall and port requirements for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c8b90-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c8b90-104">

<span> </span></span></span>

<span data-ttu-id="c8b90-105">_**Тема последнего изменения:** 2012-10-29_</span><span class="sxs-lookup"><span data-stu-id="c8b90-105">_**Topic Last Modified:** 2012-10-29_</span></span>

<span data-ttu-id="c8b90-106">Связь с аудио-и видеосигналами (A/V) может быть сложной.</span><span class="sxs-lookup"><span data-stu-id="c8b90-106">Audio/Video (A/V) communication can be a complex.</span></span> <span data-ttu-id="c8b90-107">Из-за природы протоколов, используемых в A/V, а также о том, как клиенты и серверы используют протоколы, для объяснения различий между версиями клиента и сервера требуется специальный раздел.</span><span class="sxs-lookup"><span data-stu-id="c8b90-107">Because of the nature of protocols used in A/V and how clients and servers use the protocols, a special section is warranted to explain the differences between client and server versions.</span></span>

<span data-ttu-id="c8b90-108">Для определения требований брандмауэра и портов для открытия используются следующие таблицы брандмауэров и портов.</span><span class="sxs-lookup"><span data-stu-id="c8b90-108">Use the following A/V Firewall and Port table to determine firewall requirements and which ports to open.</span></span> <span data-ttu-id="c8b90-109">Затем ознакомьтесь с терминологией преобразования сетевых адресов (NAT), поскольку NAT можно реализовать различными способами.</span><span class="sxs-lookup"><span data-stu-id="c8b90-109">Then, review the network address translation (NAT) terminology because NAT can be implemented in many different ways.</span></span> <span data-ttu-id="c8b90-110">Подробное описание параметров порта брандмауэра можно найти в разделе Архитектура ссылок в [сценариях для доступа внешних пользователей в Lync Server 2013](lync-server-2013-scenarios-for-external-user-access.md).</span><span class="sxs-lookup"><span data-stu-id="c8b90-110">For a detailed example of firewall port settings, see the reference architectures in [Scenarios for external user access in Lync Server 2013](lync-server-2013-scenarios-for-external-user-access.md).</span></span>

### <a name="general-protocol-usage-for-udp-and-tcp-in-audiovideo-and-media-traffic"></a><span data-ttu-id="c8b90-111">Общее использование протоколов для UDP и TCP для аудио-и видеофайлов и мультимедийных данных</span><span class="sxs-lookup"><span data-stu-id="c8b90-111">General Protocol Usage for UDP and TCP in Audio/Video and Media Traffic</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c8b90-112">Передача звука и видео</span><span class="sxs-lookup"><span data-stu-id="c8b90-112">Audio/Video Transport</span></span></th>
<th><span data-ttu-id="c8b90-113">Использование</span><span class="sxs-lookup"><span data-stu-id="c8b90-113">Usage</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c8b90-114">UDP</span><span class="sxs-lookup"><span data-stu-id="c8b90-114">UDP</span></span></p></td>
<td><p><span data-ttu-id="c8b90-115">Протокол предпочтительного транспортного уровня для звуковых и видеофайлов</span><span class="sxs-lookup"><span data-stu-id="c8b90-115">Preferred transport layer protocol for audio and video</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8b90-116">TCP</span><span class="sxs-lookup"><span data-stu-id="c8b90-116">TCP</span></span></p></td>
<td><p><span data-ttu-id="c8b90-117">Резервный протокол транспортного уровня для звуковых и видеофайлов</span><span class="sxs-lookup"><span data-stu-id="c8b90-117">Fallback transport layer protocol for audio and video</span></span></p>
<p><span data-ttu-id="c8b90-118">Протокол транспортного уровня, необходимый для совместного использования приложений, с Office Communications Server 2007 R2, Lync Server 2010 и Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c8b90-118">Required transport layer protocol for application sharing to Office Communications Server 2007 R2, Lync Server 2010 and Lync Server 2013</span></span></p>
<p><span data-ttu-id="c8b90-119">Обязательный протокол транспортного уровня для передачи файлов на Lync Server 2010 и Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c8b90-119">Required transport layer protocol for file transfer to Lync Server 2010 and Lync Server 2013</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="external-av-firewall-port-requirements-for-external-user-access"></a><span data-ttu-id="c8b90-120">Требования к портам внешней политики для внешних пользователей</span><span class="sxs-lookup"><span data-stu-id="c8b90-120">External A/V Firewall Port Requirements for External User Access</span></span>

<span data-ttu-id="c8b90-121">Требования к порту брандмауэра для внешних (и встроенных) интерфейсов SIP и конференций согласуются независимо от версии клиента или версии партнера Федерации.</span><span class="sxs-lookup"><span data-stu-id="c8b90-121">The firewall port requirements for external (and internal) SIP and conferencing interfaces are consistent, regardless of the version of your client or the version of the federation partner.</span></span>

<span data-ttu-id="c8b90-122">Это не относится к внешнему интерфейсу аудио/видео Edge.</span><span class="sxs-lookup"><span data-stu-id="c8b90-122">The same is not true for the Audio/Video Edge external interface.</span></span> <span data-ttu-id="c8b90-123">Для интеграции с Office Communications Server 2007 служба Edge/V требует, чтобы внешние правила брандмауэра разрешающие трафик RTP/TCP и RTP/UDP в диапазоне портов 50 000 – 59 999, чтобы поток был в обоих направлениях.</span><span class="sxs-lookup"><span data-stu-id="c8b90-123">For federation with Office Communications Server 2007, the A/V Edge service requires that external firewall rules allow RTP/TCP and RTP/UDP traffic in the 50,000 through 59,999 port range to flow in both directions.</span></span> <span data-ttu-id="c8b90-124">В предыдущей таблице предполагается, что Lync Server 2013 является основным партнером Федерации, и он настроен для связи с одним из указанных типов партнеров Федерации.</span><span class="sxs-lookup"><span data-stu-id="c8b90-124">The previous table assumes that Lync Server 2013 is the primary federation partner and it is being configured to communicate with one of the other federation partner types listed.</span></span>

<span data-ttu-id="c8b90-125">Настройка диапазона портов для аудио-и видеопортов 50000-59,999 должна учитывать, что диапазон портов будет содержать исходные порты для связи с партнерами Федерации.</span><span class="sxs-lookup"><span data-stu-id="c8b90-125">Configuring the Audio/Video port range of 50,000-59,999 must take into account that the port range will contain the source ports for communications to federation partners.</span></span> <span data-ttu-id="c8b90-126">В качестве подробностей следует рассмотреть вопрос о том, что связь инициируется партнером Федерации.</span><span class="sxs-lookup"><span data-stu-id="c8b90-126">In detail, consider that a communication is initiated from a federation partner.</span></span> <span data-ttu-id="c8b90-127">Связь между портами служб EDGE (A/V) в диапазоне 50000-59,999 будет подключаться к ожидаемому порту TCP 443 службы EDGE (A/V) партнера.</span><span class="sxs-lookup"><span data-stu-id="c8b90-127">The communication from the A/V Edge service ports in the 50,000-59,999 range will connect to the expected port TCP 443 of the partner’s A/V Edge service.</span></span> <span data-ttu-id="c8b90-128">И наоборот, входящий трафик для порта службы Edge/V TCP 443 будет иметь исходный порт в диапазоне 50000 — 59,999.</span><span class="sxs-lookup"><span data-stu-id="c8b90-128">Conversely, inbound traffic to your A/V Edge service port TCP 443 will have a source port in the range of 50,000-59,999.</span></span>

<span data-ttu-id="c8b90-129">Для использования разных брандмауэров и политик для администрирования брандмауэра может потребоваться настроить только правила назначения или настроить оба источника и назначение.</span><span class="sxs-lookup"><span data-stu-id="c8b90-129">Different firewalls and policies for firewall administration may require only destination rules to be configured, or they may require both source and destination to be configured.</span></span> <span data-ttu-id="c8b90-130">Если требования предназначены только для конечных портов, требования к аудио-и видеозаписи:</span><span class="sxs-lookup"><span data-stu-id="c8b90-130">If your requirements are for destination ports only, the Audio/Video requirements are:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c8b90-131">Исходный IP-адрес</span><span class="sxs-lookup"><span data-stu-id="c8b90-131">Source IP</span></span></th>
<th><span data-ttu-id="c8b90-132">Конечный IP-адрес</span><span class="sxs-lookup"><span data-stu-id="c8b90-132">Destination IP</span></span></th>
<th><span data-ttu-id="c8b90-133">Конечный порт</span><span class="sxs-lookup"><span data-stu-id="c8b90-133">Destination Port</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c8b90-134">Интерфейс службы Edge</span><span class="sxs-lookup"><span data-stu-id="c8b90-134">A/V Edge service interface</span></span></p></td>
<td><p><span data-ttu-id="c8b90-135">Любой</span><span class="sxs-lookup"><span data-stu-id="c8b90-135">Any</span></span></p></td>
<td><p><span data-ttu-id="c8b90-136">TCP 443</span><span class="sxs-lookup"><span data-stu-id="c8b90-136">TCP 443</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8b90-137">Интерфейс службы Edge</span><span class="sxs-lookup"><span data-stu-id="c8b90-137">A/V Edge service interface</span></span></p></td>
<td><p><span data-ttu-id="c8b90-138">Любой</span><span class="sxs-lookup"><span data-stu-id="c8b90-138">Any</span></span></p></td>
<td><p><span data-ttu-id="c8b90-139">UDP 3478</span><span class="sxs-lookup"><span data-stu-id="c8b90-139">UDP 3478</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8b90-140">Любой</span><span class="sxs-lookup"><span data-stu-id="c8b90-140">Any</span></span></p></td>
<td><p><span data-ttu-id="c8b90-141">Интерфейс службы Edge</span><span class="sxs-lookup"><span data-stu-id="c8b90-141">A/V Edge service interface</span></span></p></td>
<td><p><span data-ttu-id="c8b90-142">TCP 443</span><span class="sxs-lookup"><span data-stu-id="c8b90-142">TCP 443</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8b90-143">Любой</span><span class="sxs-lookup"><span data-stu-id="c8b90-143">Any</span></span></p></td>
<td><p><span data-ttu-id="c8b90-144">Интерфейс службы Edge</span><span class="sxs-lookup"><span data-stu-id="c8b90-144">A/V Edge service interface</span></span></p></td>
<td><p><span data-ttu-id="c8b90-145">UDP 3478</span><span class="sxs-lookup"><span data-stu-id="c8b90-145">UDP 3478</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c8b90-146">Если политики требуют для входящих и исходящих определений правил брандмауэра, необходимо использовать требования к аудио-и видеозаписи:</span><span class="sxs-lookup"><span data-stu-id="c8b90-146">If your policies require both inbound and outbound firewall rule definitions, the Audio/Video requirements are:</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c8b90-147">Исходный IP-адрес</span><span class="sxs-lookup"><span data-stu-id="c8b90-147">Source IP</span></span></th>
<th><span data-ttu-id="c8b90-148">Конечный IP-адрес</span><span class="sxs-lookup"><span data-stu-id="c8b90-148">Destination IP</span></span></th>
<th><span data-ttu-id="c8b90-149">Исходный порт</span><span class="sxs-lookup"><span data-stu-id="c8b90-149">Source Port</span></span></th>
<th><span data-ttu-id="c8b90-150">Конечный порт</span><span class="sxs-lookup"><span data-stu-id="c8b90-150">Destination Port</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c8b90-151">Интерфейс службы Edge</span><span class="sxs-lookup"><span data-stu-id="c8b90-151">A/V Edge service interface</span></span></p></td>
<td><p><span data-ttu-id="c8b90-152">Любой</span><span class="sxs-lookup"><span data-stu-id="c8b90-152">Any</span></span></p></td>
<td><p><span data-ttu-id="c8b90-153">TCP 50 000-59 999</span><span class="sxs-lookup"><span data-stu-id="c8b90-153">TCP 50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="c8b90-154">TCP 443</span><span class="sxs-lookup"><span data-stu-id="c8b90-154">TCP 443</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8b90-155">Интерфейс службы Edge</span><span class="sxs-lookup"><span data-stu-id="c8b90-155">A/V Edge service interface</span></span></p></td>
<td><p><span data-ttu-id="c8b90-156">Любой</span><span class="sxs-lookup"><span data-stu-id="c8b90-156">Any</span></span></p></td>
<td><p><span data-ttu-id="c8b90-157">UDP 3478</span><span class="sxs-lookup"><span data-stu-id="c8b90-157">UDP 3478</span></span></p></td>
<td><p><span data-ttu-id="c8b90-158">UDP 3478</span><span class="sxs-lookup"><span data-stu-id="c8b90-158">UDP 3478</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8b90-159">Любой</span><span class="sxs-lookup"><span data-stu-id="c8b90-159">Any</span></span></p></td>
<td><p><span data-ttu-id="c8b90-160">Интерфейс службы Edge</span><span class="sxs-lookup"><span data-stu-id="c8b90-160">A/V Edge service interface</span></span></p></td>
<td><p><span data-ttu-id="c8b90-161">Любой</span><span class="sxs-lookup"><span data-stu-id="c8b90-161">Any</span></span></p></td>
<td><p><span data-ttu-id="c8b90-162">TCP 443</span><span class="sxs-lookup"><span data-stu-id="c8b90-162">TCP 443</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8b90-163">Любой</span><span class="sxs-lookup"><span data-stu-id="c8b90-163">Any</span></span></p></td>
<td><p><span data-ttu-id="c8b90-164">Интерфейс службы Edge</span><span class="sxs-lookup"><span data-stu-id="c8b90-164">A/V Edge service interface</span></span></p></td>
<td><p><span data-ttu-id="c8b90-165">Любой</span><span class="sxs-lookup"><span data-stu-id="c8b90-165">Any</span></span></p></td>
<td><p><span data-ttu-id="c8b90-166">UDP 3478</span><span class="sxs-lookup"><span data-stu-id="c8b90-166">UDP 3478</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!IMPORTANT]  
> <span data-ttu-id="c8b90-167">Для Microsoft Office Communications Server 2007 требуется немного другая настройка.</span><span class="sxs-lookup"><span data-stu-id="c8b90-167">Microsoft Office Communications Server 2007 requires a slightly different configuration.</span></span> <span data-ttu-id="c8b90-168">Диапазон портов TCP и UDP, 50 000 – 59,999, должен быть открытым для входящих и исходящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="c8b90-168">The TCP and UDP port range of 50,000-59,999 must be open inbound and outbound.</span></span> <span data-ttu-id="c8b90-169">Это требование относится только к Office Communicator 2007.</span><span class="sxs-lookup"><span data-stu-id="c8b90-169">This requirement is only for Office Communicator 2007.</span></span> <span data-ttu-id="c8b90-170">Office Communications Server 2007 R2, Lync Server 2010 и Lync Server 2013 требуется только диапазон TCP 50000-59,999 Open Outbound.</span><span class="sxs-lookup"><span data-stu-id="c8b90-170">Office Communications Server 2007 R2, Lync Server 2010 and Lync Server 2013 only require TCP range 50,000-59,999 open outbound.</span></span>



</div>

</div>

<div>

## <a name="nat-requirements-for-the-edge-service"></a><span data-ttu-id="c8b90-171">Требования к NAT для услуги пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="c8b90-171">NAT requirements for the Edge service</span></span>

<span data-ttu-id="c8b90-172">Если вы решите настроить для службы Edge частные IP-адреса без маршрутизации, применяются следующие требования NAT:</span><span class="sxs-lookup"><span data-stu-id="c8b90-172">The following NAT requirements apply if you choose to configure non-routable private IP addresses for the Edge service:</span></span>

  - <span data-ttu-id="c8b90-173">Преобразование сетевых адресов (NAT) можно использовать только для балансировки нагрузки DNS.</span><span class="sxs-lookup"><span data-stu-id="c8b90-173">NAT can only be used with DNS load-balancing.</span></span> <span data-ttu-id="c8b90-174">NAT не поддерживается для топологии Edge аппаратной балансировки нагрузки (HLB).</span><span class="sxs-lookup"><span data-stu-id="c8b90-174">NAT is not supported with a hardware load balancing (HLB) Edge topology.</span></span>

  - <span data-ttu-id="c8b90-175">NAT можно использовать только во внешнем интерфейсе Edge.</span><span class="sxs-lookup"><span data-stu-id="c8b90-175">NAT can only be used on the external Edge interface.</span></span> <span data-ttu-id="c8b90-176">NAT не поддерживается внутренним интерфейсом Edge.</span><span class="sxs-lookup"><span data-stu-id="c8b90-176">NAT is not supported on the internal Edge interface.</span></span>

  - <span data-ttu-id="c8b90-177">Трафик NAT должен быть симметричным для входящего и исходящего трафика.</span><span class="sxs-lookup"><span data-stu-id="c8b90-177">NAT must be symmetric for incoming and outgoing traffic.</span></span>
    
  - <span data-ttu-id="c8b90-178">Для трафика из Интернета необходимо изменить IP-адрес назначения с общедоступного IP-адреса, поддерживающего NAT, на внешний IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="c8b90-178">For traffic from the Internet, NAT must change the destination IP address from the NAT-enabled public IP address of the A/V Edge service to its external IP address.</span></span> <span data-ttu-id="c8b90-179">IP-адрес источника должен оставаться неизменным, чтобы служба Edge может найти оптимальный путь к носителю.</span><span class="sxs-lookup"><span data-stu-id="c8b90-179">The source IP address must remain intact, so that the A/V Edge service can find the optimal media path.</span></span>
  
  <span data-ttu-id="c8b90-180">Например, в направлении, указанном на рисунке ниже, общедоступный IP-адрес 131.107.155.30 был изменен на внешний (частный) IP-адрес 10.45.16.10.</span><span class="sxs-lookup"><span data-stu-id="c8b90-180">For example, in the inbound direction in the figure below, the public IP address 131.107.155.30 was changed to the external (private) IP address 10.45.16.10.</span></span> <span data-ttu-id="c8b90-181">IP-адрес источника остался неизменным.</span><span class="sxs-lookup"><span data-stu-id="c8b90-181">The source IP address remained unchanged.</span></span>
  
  - <span data-ttu-id="c8b90-182">Для трафика из службы EDGE (A/V) к Интернету необходимо изменить исходный IP-адрес с внешнего IP-адреса службы EDGE на общедоступный IP-адрес, поддерживающий NAT.</span><span class="sxs-lookup"><span data-stu-id="c8b90-182">For traffic from the A/V Edge service to the Internet, NAT must change the source IP address from the external IP address of the A/V Edge service to the NAT-enabled public IP address.</span></span>

<span data-ttu-id="c8b90-183">Например, в направлении выхода на рисунке ниже внешний IP-адрес 10.45.16.10 был изменен на общедоступный IP-адрес 131.107.155.30.</span><span class="sxs-lookup"><span data-stu-id="c8b90-183">For example, in the outbound direction in the figure below, the external (private) IP address 10.45.16.10 was changed to the public IP address 131.107.155.30.</span></span>

<span data-ttu-id="c8b90-184">**На рисунке ниже показано, как NAT изменяет IP-адрес назначения для входящего трафика и IP-адрес источника для исходящего трафика.**</span><span class="sxs-lookup"><span data-stu-id="c8b90-184">**The figure below shows how NAT changes the destination IP address for inbound traffic and the source IP Address for outbound traffic.**</span></span>

<span data-ttu-id="c8b90-185">![Изменение исходных IP-адресов и IP-адресов назначения](images/Gg425882.0fee7ec5-4cb8-4aff-9164-e7fbab73336d(OCS.15).jpg "Изменение исходных IP-адресов и IP-адресов назначения")</span><span class="sxs-lookup"><span data-stu-id="c8b90-185">![Changing destination/source IP addresses](images/Gg425882.0fee7ec5-4cb8-4aff-9164-e7fbab73336d(OCS.15).jpg "Changing destination/source IP addresses")</span></span>

<span data-ttu-id="c8b90-186">Ключевые моменты:</span><span class="sxs-lookup"><span data-stu-id="c8b90-186">The key points are:</span></span>

  - <span data-ttu-id="c8b90-187">Трафик, входящий на сервер, на котором работает служба Edge/V, IP-адрес источника не меняется, но IP-адрес назначения меняется с 131.107.155.30 на переведенный IP-адрес 10.45.16.10.</span><span class="sxs-lookup"><span data-stu-id="c8b90-187">Traffic that is inbound to the server running the A/V Edge service, the source IP address does not change but the destination IP address changes from 131.107.155.30 to the translated IP address of 10.45.16.10.</span></span>

  - <span data-ttu-id="c8b90-188">Трафик, исходящий от сервера, на котором запущена служба EDGE (A/V), исходный IP-адрес изменится с общедоступного IP-адреса сервера на общедоступный IP-адрес сервера, на котором работает служба Edge-V.</span><span class="sxs-lookup"><span data-stu-id="c8b90-188">Traffic that is outbound from the server running the A/V Edge service back to the workstation, the source IP address changes from the server’s public IP address to the public IP address of the server running the A/V Edge service.</span></span> <span data-ttu-id="c8b90-189">Конечный IP-адрес остается на общедоступной рабочей станции.</span><span class="sxs-lookup"><span data-stu-id="c8b90-189">The destination IP remains the workstation’s public IP address.</span></span> <span data-ttu-id="c8b90-190">После того как пакет выходит из первого исходящего устройства NAT, правило на устройстве NAT изменит исходный IP-адрес сервера, на котором размещается IP-адрес внешнего интерфейса службы EDGE (10.45.16.10), на его общедоступный IP-адрес (131.107.155.30).</span><span class="sxs-lookup"><span data-stu-id="c8b90-190">After the packet leaves the first NAT device outbound, the rule on the NAT device changes the source IP address of the server running the A/V Edge service external interface IP address (10.45.16.10) to its public IP address (131.107.155.30).</span></span>

<span data-ttu-id="c8b90-191"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c8b90-191"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

