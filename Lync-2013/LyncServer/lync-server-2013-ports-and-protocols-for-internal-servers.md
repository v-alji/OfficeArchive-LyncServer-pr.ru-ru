---
title: 'Lync Server 2013: порты и протоколы для внутренних серверов'
description: 'Lync Server 2013: порты и протоколы для внутренних серверов.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Ports and protocols for internal servers
ms:assetid: c94063f1-e802-4a61-be90-022fc185335e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398833(v=OCS.15)
ms:contentKeyID: 48185402
ms.date: 04/06/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d7d8f12c78c5dec5caacaeb1156f4d228b7cd591
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424249"
---
# <a name="ports-and-protocols-for-internal-servers-in-lync-server-2013"></a><span data-ttu-id="b4419-103">Порты и протоколы для внутренних серверов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b4419-103">Ports and protocols for internal servers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b4419-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b4419-104">

<span> </span></span></span>

<span data-ttu-id="b4419-105">_**Тема последнего изменения:** 2016-04-06_</span><span class="sxs-lookup"><span data-stu-id="b4419-105">_**Topic Last Modified:** 2016-04-06_</span></span>

<span data-ttu-id="b4419-106">В этом разделе приведены общие сведения о портах и протоколах, используемых серверами, подсистемами балансировки нагрузки и клиентами в развертывании Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b4419-106">This section summarizes the ports and protocols used by servers, load balancers, and clients in a Lync Server deployment.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="b4419-107">Клиенты Lync и Communicator, вовлеченные в одну и ту же связь, часто называют одноранговой.</span><span class="sxs-lookup"><span data-stu-id="b4419-107">Lync and Communicator clients when involved in a one to one communication, is often referred to as peer-to-peer.</span></span> <span data-ttu-id="b4419-108">Технически, эти два клиента взаимодействуют между собой в одном сеансе, с помощью управляющего блока обмена мгновенными сообщениями (IMMCU) в центре.</span><span class="sxs-lookup"><span data-stu-id="b4419-108">Technically, the two clients are communicating in a one to one conversation, with the Instant Messaging multipoint control unit (IMMCU) in the middle.</span></span> <span data-ttu-id="b4419-109">IMMCU является компонентом сервера переднего плана.</span><span class="sxs-lookup"><span data-stu-id="b4419-109">The IMMCU is a component of Front End Server.</span></span> <span data-ttu-id="b4419-110">Размещение IMMCU в требуемом рабочем канале связи позволяет записывать сведения о вызове и другие возможности, которые сервер переднего плана включит.</span><span class="sxs-lookup"><span data-stu-id="b4419-110">Placing the IMMCU in the required communication workflow allows call detail recording and other features that the Front End Server enables.</span></span> <span data-ttu-id="b4419-111">Взаимодействие осуществляется из динамического исходного порта на клиенте на серверный порт TLS/TCP/5061 (предполагается использование рекомендуемой безопасности транспортного уровня).</span><span class="sxs-lookup"><span data-stu-id="b4419-111">Communication is from a dynamic source port on the client to the Front End Server port TLS/TCP/5061 (assuming the use of the recommended transport layer security).</span></span> <span data-ttu-id="b4419-112">Связь между одноранговым и одноранговой связью (а также многосторонним СООБЩЕНИЕм) возможна только в том случае, если Lync Server и IMMCU активны и доступны.</span><span class="sxs-lookup"><span data-stu-id="b4419-112">By design, peer-to-peer communication (as well as multi-party IM) is possible only when Lync Server and the IMMCU is active and available.</span></span>



</div>

<div>

## <a name="port-and-protocol-details"></a><span data-ttu-id="b4419-113">Сведения о портах и протоколах</span><span class="sxs-lookup"><span data-stu-id="b4419-113">Port and Protocol Details</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="b4419-114">Перед запуском служб Lync Server на сервере необходимо запустить брандмауэр Windows, так как это происходит в том случае, если Lync Server открывает нужные порты в брандмауэре.</span><span class="sxs-lookup"><span data-stu-id="b4419-114">Windows Firewall must be running before you start the Lync Server services on a server, because that is when Lync Server opens the required ports in the firewall.</span></span>



</div>

<span data-ttu-id="b4419-115">Подробнее о настройке брандмауэра для компонентов EDGE можно узнать в статьях [Определение внешних параметров брандмауэра/V и требований к портам для Lync Server 2013](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b4419-115">For details about firewall configuration for edge components, see [Determine external A/V firewall and port requirements for Lync Server 2013](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md).</span></span>

<span data-ttu-id="b4419-116">В следующей таблице приводится список портов, которые должны быть открыты для каждой роли внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="b4419-116">The following table lists the ports that need to be open on each internal server role.</span></span>

### <a name="required-server-ports-by-server-role"></a><span data-ttu-id="b4419-117">Необходимые порты сервера (по ролям сервера)</span><span class="sxs-lookup"><span data-stu-id="b4419-117">Required Server Ports (by Server Role)</span></span>

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
<th><span data-ttu-id="b4419-118">Роль сервера</span><span class="sxs-lookup"><span data-stu-id="b4419-118">Server role</span></span></th>
<th><span data-ttu-id="b4419-119">Имя службы</span><span class="sxs-lookup"><span data-stu-id="b4419-119">Service name</span></span></th>
<th><span data-ttu-id="b4419-120">Порт</span><span class="sxs-lookup"><span data-stu-id="b4419-120">Port</span></span></th>
<th><span data-ttu-id="b4419-121">Протокол</span><span class="sxs-lookup"><span data-stu-id="b4419-121">Protocol</span></span></th>
<th><span data-ttu-id="b4419-122">Notes</span><span class="sxs-lookup"><span data-stu-id="b4419-122">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b4419-123">Все серверы</span><span class="sxs-lookup"><span data-stu-id="b4419-123">All Servers</span></span></p></td>
<td><p><span data-ttu-id="b4419-124">Браузер SQL</span><span class="sxs-lookup"><span data-stu-id="b4419-124">SQL Browser</span></span></p></td>
<td><p><span data-ttu-id="b4419-125">1434</span><span class="sxs-lookup"><span data-stu-id="b4419-125">1434</span></span></p></td>
<td><p><span data-ttu-id="b4419-126">UDP</span><span class="sxs-lookup"><span data-stu-id="b4419-126">UDP</span></span></p></td>
<td><p><span data-ttu-id="b4419-127">Браузер SQL для локальной реплицированной копии базы данных центрального хранилища управления.</span><span class="sxs-lookup"><span data-stu-id="b4419-127">SQL Browser for the local replicated copy of the Central Management Store database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4419-128">Серверы переднего плана</span><span class="sxs-lookup"><span data-stu-id="b4419-128">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b4419-129">Служба Lync Server Front-End Service</span><span class="sxs-lookup"><span data-stu-id="b4419-129">Lync Server Front-End service</span></span></p></td>
<td><p><span data-ttu-id="b4419-130">5060</span><span class="sxs-lookup"><span data-stu-id="b4419-130">5060</span></span></p></td>
<td><p><span data-ttu-id="b4419-131">TCP</span><span class="sxs-lookup"><span data-stu-id="b4419-131">TCP</span></span></p></td>
<td><p><span data-ttu-id="b4419-132">При необходимости используется для статических маршрутов к доверенным службам серверами Standard Edition и серверами переднего плана, например серверами удаленного управления звонками.</span><span class="sxs-lookup"><span data-stu-id="b4419-132">Optionally used by Standard Edition servers and Front End Servers for static routes to trusted services, such as remote call control servers.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4419-133">Серверы переднего плана</span><span class="sxs-lookup"><span data-stu-id="b4419-133">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b4419-134">Служба Lync Server Front-End Service</span><span class="sxs-lookup"><span data-stu-id="b4419-134">Lync Server Front-End service</span></span></p></td>
<td><p><span data-ttu-id="b4419-135">5061</span><span class="sxs-lookup"><span data-stu-id="b4419-135">5061</span></span></p></td>
<td><p><span data-ttu-id="b4419-136">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="b4419-136">TCP (TLS)</span></span></p></td>
<td><p><span data-ttu-id="b4419-137">Используется серверами Standard Edition и серверами переднего плана для всех внутренних SIP-соединений между серверами (MTLS), для SIP-соединений между сервером и клиентом (TLS) и для SIP-соединений между серверами переднего плана и серверами-посредниками (MTLS).</span><span class="sxs-lookup"><span data-stu-id="b4419-137">Used by Standard Edition servers and Front End pools for all internal SIP communications between servers (MTLS), for SIP communications between Server and Client (TLS) and for SIP communications between Front End Servers and Mediation Servers (MTLS).</span></span> <span data-ttu-id="b4419-138">Также используется для связи с сервером мониторинга.</span><span class="sxs-lookup"><span data-stu-id="b4419-138">Also used for communications with Monitoring Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4419-139">Серверы переднего плана</span><span class="sxs-lookup"><span data-stu-id="b4419-139">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b4419-140">Служба Lync Server Front-End Service</span><span class="sxs-lookup"><span data-stu-id="b4419-140">Lync Server Front-End service</span></span></p></td>
<td><p><span data-ttu-id="b4419-141">444</span><span class="sxs-lookup"><span data-stu-id="b4419-141">444</span></span></p></td>
<td><p><span data-ttu-id="b4419-142">HTTPS</span><span class="sxs-lookup"><span data-stu-id="b4419-142">HTTPS</span></span></p>
<p><span data-ttu-id="b4419-143">TCP</span><span class="sxs-lookup"><span data-stu-id="b4419-143">TCP</span></span></p></td>
<td><p><span data-ttu-id="b4419-144">Используется для взаимодействия по протоколу HTTPS между фокусом (компонент Lync Server, управляющий состоянием конференции) и отдельными серверами.</span><span class="sxs-lookup"><span data-stu-id="b4419-144">Used for HTTPS communication between the Focus (the Lync Server component that manages conference state) and the individual servers.</span></span></p>
<p><span data-ttu-id="b4419-145">Этот порт также используется для TCP-соединений между устройствами для обеспечения связи в филиалах и серверами переднего плана.</span><span class="sxs-lookup"><span data-stu-id="b4419-145">This port is also used for TCP communication between Survivable Branch Appliances and Front End Servers.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4419-146">Серверы переднего плана</span><span class="sxs-lookup"><span data-stu-id="b4419-146">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b4419-147">Служба Lync Server Front-End Service</span><span class="sxs-lookup"><span data-stu-id="b4419-147">Lync Server Front-End service</span></span></p></td>
<td><p><span data-ttu-id="b4419-148">135</span><span class="sxs-lookup"><span data-stu-id="b4419-148">135</span></span></p></td>
<td><p><span data-ttu-id="b4419-149">DCOM и удаленный вызов процедур (RPC)</span><span class="sxs-lookup"><span data-stu-id="b4419-149">DCOM and remote procedure call (RPC)</span></span></p></td>
<td><p><span data-ttu-id="b4419-150">Используется для операций на базе DCOM, таких как перемещение пользователей, синхронизация репликаторов пользовательских данных и адресных книг.</span><span class="sxs-lookup"><span data-stu-id="b4419-150">Used for DCOM based operations such as Moving Users, User Replicator Synchronization, and Address Book Synchronization.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4419-151">Серверы переднего плана</span><span class="sxs-lookup"><span data-stu-id="b4419-151">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b4419-152">Служба конференц-связи Lync Server для обмена мгновенными сообщениями</span><span class="sxs-lookup"><span data-stu-id="b4419-152">Lync Server IM Conferencing service</span></span></p></td>
<td><p><span data-ttu-id="b4419-153">5062</span><span class="sxs-lookup"><span data-stu-id="b4419-153">5062</span></span></p></td>
<td><p><span data-ttu-id="b4419-154">TCP</span><span class="sxs-lookup"><span data-stu-id="b4419-154">TCP</span></span></p></td>
<td><p><span data-ttu-id="b4419-155">Используется для входящих SIP-запросов в конференц-связи с использованием обмена мгновенными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="b4419-155">Used for incoming SIP requests for instant messaging (IM) conferencing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4419-156">Серверы переднего плана</span><span class="sxs-lookup"><span data-stu-id="b4419-156">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b4419-157">Служба веб-конференций Lync Server</span><span class="sxs-lookup"><span data-stu-id="b4419-157">Lync Server Web Conferencing service</span></span></p></td>
<td><p><span data-ttu-id="b4419-158">8057</span><span class="sxs-lookup"><span data-stu-id="b4419-158">8057</span></span></p></td>
<td><p><span data-ttu-id="b4419-159">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="b4419-159">TCP (TLS)</span></span></p></td>
<td><p><span data-ttu-id="b4419-160">Используется для прослушивания подключений по протоколу PSOM от клиента.</span><span class="sxs-lookup"><span data-stu-id="b4419-160">Used to listen for Persistent Shared Object Model (PSOM) connections from client.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4419-161">Серверы переднего плана</span><span class="sxs-lookup"><span data-stu-id="b4419-161">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b4419-162">Служба совместимости веб-конференций Lync Server</span><span class="sxs-lookup"><span data-stu-id="b4419-162">Lync Server Web Conferencing Compatibility service</span></span></p></td>
<td><p><span data-ttu-id="b4419-163">8058</span><span class="sxs-lookup"><span data-stu-id="b4419-163">8058</span></span></p></td>
<td><p><span data-ttu-id="b4419-164">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="b4419-164">TCP (TLS)</span></span></p></td>
<td><p><span data-ttu-id="b4419-165">Используется для прослушивания подключений к постоянной общей объектной модели (PSOM) из клиента Live Meeting и предыдущих версий Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b4419-165">Used to listen for Persistent Shared Object Model (PSOM) connections from the Live Meeting client and previous versions of Lync Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4419-166">Серверы переднего плана</span><span class="sxs-lookup"><span data-stu-id="b4419-166">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b4419-167">Служба голосовой и видеоконференций Lync Server</span><span class="sxs-lookup"><span data-stu-id="b4419-167">Lync Server Audio/Video Conferencing service</span></span></p></td>
<td><p><span data-ttu-id="b4419-168">5063</span><span class="sxs-lookup"><span data-stu-id="b4419-168">5063</span></span></p></td>
<td><p><span data-ttu-id="b4419-169">TCP</span><span class="sxs-lookup"><span data-stu-id="b4419-169">TCP</span></span></p></td>
<td><p><span data-ttu-id="b4419-170">Используется для входящих SIP-запросов на аудио- и видеоконференции.</span><span class="sxs-lookup"><span data-stu-id="b4419-170">Used for incoming SIP requests for audio/video (A/V) conferencing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4419-171">Серверы переднего плана</span><span class="sxs-lookup"><span data-stu-id="b4419-171">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b4419-172">Служба голосовой и видеоконференций Lync Server</span><span class="sxs-lookup"><span data-stu-id="b4419-172">Lync Server Audio/Video Conferencing service</span></span></p></td>
<td><p><span data-ttu-id="b4419-173">57501-65535</span><span class="sxs-lookup"><span data-stu-id="b4419-173">57501-65535</span></span></p></td>
<td><p><span data-ttu-id="b4419-174">TCP/UDP</span><span class="sxs-lookup"><span data-stu-id="b4419-174">TCP/UDP</span></span></p></td>
<td><p><span data-ttu-id="b4419-175">Диапазон портов, используемых для видеоконференций.</span><span class="sxs-lookup"><span data-stu-id="b4419-175">Media port range used for video conferencing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4419-176">Серверы переднего плана</span><span class="sxs-lookup"><span data-stu-id="b4419-176">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b4419-177">Служба веб-совместимости Lync Server</span><span class="sxs-lookup"><span data-stu-id="b4419-177">Lync Server Web Compatibility service</span></span></p></td>
<td><p><span data-ttu-id="b4419-178">80</span><span class="sxs-lookup"><span data-stu-id="b4419-178">80</span></span></p></td>
<td><p><span data-ttu-id="b4419-179">HTTP</span><span class="sxs-lookup"><span data-stu-id="b4419-179">HTTP</span></span></p></td>
<td><p><span data-ttu-id="b4419-180">Используется для подключений от серверов переднего плана к полным доменным именам в веб-ферме (URL-адреса используются по веб-компонентам IIS), когда не используется HTTPS.</span><span class="sxs-lookup"><span data-stu-id="b4419-180">Used for communication from Front End Servers to the web farm FQDNs (the URLs used by IIS web components) when HTTPS is not used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4419-181">Серверы переднего плана</span><span class="sxs-lookup"><span data-stu-id="b4419-181">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b4419-182">Служба веб-совместимости Lync Server</span><span class="sxs-lookup"><span data-stu-id="b4419-182">Lync Server Web Compatibility service</span></span></p></td>
<td><p><span data-ttu-id="b4419-183">443</span><span class="sxs-lookup"><span data-stu-id="b4419-183">443</span></span></p></td>
<td><p><span data-ttu-id="b4419-184">HTTPS</span><span class="sxs-lookup"><span data-stu-id="b4419-184">HTTPS</span></span></p></td>
<td><p><span data-ttu-id="b4419-185">Используется для подключений от серверов переднего плана к полным доменным именам в веб-ферме (URL-адреса используются по веб-компонентам IIS).</span><span class="sxs-lookup"><span data-stu-id="b4419-185">Used for communication from Front End Servers to the web farm FQDNs (the URLs used by IIS web components).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4419-186">Серверы переднего плана</span><span class="sxs-lookup"><span data-stu-id="b4419-186">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b4419-187">Служба веб-совместимости Lync Server</span><span class="sxs-lookup"><span data-stu-id="b4419-187">Lync Server Web Compatibility service</span></span></p></td>
<td><p><span data-ttu-id="b4419-188">8080</span><span class="sxs-lookup"><span data-stu-id="b4419-188">8080</span></span></p></td>
<td><p><span data-ttu-id="b4419-189">TCP и HTTP</span><span class="sxs-lookup"><span data-stu-id="b4419-189">TCP and HTTP</span></span></p></td>
<td><p><span data-ttu-id="b4419-190">Используется веб-компонентами для внешнего доступа.</span><span class="sxs-lookup"><span data-stu-id="b4419-190">Used by web components for external access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4419-191">Серверы переднего плана</span><span class="sxs-lookup"><span data-stu-id="b4419-191">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b4419-192">Компонент веб-сервера</span><span class="sxs-lookup"><span data-stu-id="b4419-192">Web server component</span></span></p></td>
<td><p><span data-ttu-id="b4419-193">4443</span><span class="sxs-lookup"><span data-stu-id="b4419-193">4443</span></span></p></td>
<td><p><span data-ttu-id="b4419-194">HTTPS</span><span class="sxs-lookup"><span data-stu-id="b4419-194">HTTPS</span></span></p></td>
<td><p><span data-ttu-id="b4419-195">Связь по протоколу HTTPS (от обратного прокси-сервера) и по протоколу HTTPS между пулами переднего плана для автообнаружения входа.</span><span class="sxs-lookup"><span data-stu-id="b4419-195">HTTPS (from Reverse Proxy) and HTTPS Front End inter-pool communications for Autodiscover sign-in.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4419-196">Серверы переднего плана</span><span class="sxs-lookup"><span data-stu-id="b4419-196">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b4419-197">Компонент веб-сервера</span><span class="sxs-lookup"><span data-stu-id="b4419-197">Web server component</span></span></p></td>
<td><p><span data-ttu-id="b4419-198">8060</span><span class="sxs-lookup"><span data-stu-id="b4419-198">8060</span></span></p></td>
<td><p><span data-ttu-id="b4419-199">TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="b4419-199">TCP (MTLS)</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4419-200">Серверы переднего плана</span><span class="sxs-lookup"><span data-stu-id="b4419-200">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b4419-201">Компонент веб-сервера</span><span class="sxs-lookup"><span data-stu-id="b4419-201">Web server component</span></span></p></td>
<td><p><span data-ttu-id="b4419-202">8061</span><span class="sxs-lookup"><span data-stu-id="b4419-202">8061</span></span></p></td>
<td><p><span data-ttu-id="b4419-203">TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="b4419-203">TCP (MTLS)</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4419-204">Серверы переднего плана</span><span class="sxs-lookup"><span data-stu-id="b4419-204">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b4419-205">Компонент служб Mobility Services</span><span class="sxs-lookup"><span data-stu-id="b4419-205">Mobility Services component</span></span></p></td>
<td><p><span data-ttu-id="b4419-206">5086</span><span class="sxs-lookup"><span data-stu-id="b4419-206">5086</span></span></p></td>
<td><p><span data-ttu-id="b4419-207">TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="b4419-207">TCP (MTLS)</span></span></p></td>
<td><p><span data-ttu-id="b4419-208">SIP-порт, используемый внутренними процессами служб Mobility Services.</span><span class="sxs-lookup"><span data-stu-id="b4419-208">SIP port used by Mobility Services internal processes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4419-209">Серверы переднего плана</span><span class="sxs-lookup"><span data-stu-id="b4419-209">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b4419-210">Компонент служб Mobility Services</span><span class="sxs-lookup"><span data-stu-id="b4419-210">Mobility Services component</span></span></p></td>
<td><p><span data-ttu-id="b4419-211">5087</span><span class="sxs-lookup"><span data-stu-id="b4419-211">5087</span></span></p></td>
<td><p><span data-ttu-id="b4419-212">TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="b4419-212">TCP (MTLS)</span></span></p></td>
<td><p><span data-ttu-id="b4419-213">SIP-порт, используемый внутренними процессами служб Mobility Services.</span><span class="sxs-lookup"><span data-stu-id="b4419-213">SIP port used by Mobility Services internal processes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4419-214">Серверы переднего плана</span><span class="sxs-lookup"><span data-stu-id="b4419-214">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b4419-215">Компонент служб Mobility Services</span><span class="sxs-lookup"><span data-stu-id="b4419-215">Mobility Services component</span></span></p></td>
<td><p><span data-ttu-id="b4419-216">443</span><span class="sxs-lookup"><span data-stu-id="b4419-216">443</span></span></p></td>
<td><p><span data-ttu-id="b4419-217">HTTPS</span><span class="sxs-lookup"><span data-stu-id="b4419-217">HTTPS</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4419-218">Серверы переднего плана</span><span class="sxs-lookup"><span data-stu-id="b4419-218">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b4419-219">Служба помощника по конференциям Lync Server (Конференц-связь с телефонным подключением)</span><span class="sxs-lookup"><span data-stu-id="b4419-219">Lync Server Conferencing Attendant service (dial-in conferencing)</span></span></p></td>
<td><p><span data-ttu-id="b4419-220">5064</span><span class="sxs-lookup"><span data-stu-id="b4419-220">5064</span></span></p></td>
<td><p><span data-ttu-id="b4419-221">TCP</span><span class="sxs-lookup"><span data-stu-id="b4419-221">TCP</span></span></p></td>
<td><p><span data-ttu-id="b4419-222">Используется для входящих SIP-запросов для конференц-связи с телефонным подключением.</span><span class="sxs-lookup"><span data-stu-id="b4419-222">Used for incoming SIP requests for dial-in conferencing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4419-223">Серверы переднего плана</span><span class="sxs-lookup"><span data-stu-id="b4419-223">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b4419-224">Служба помощника по конференциям Lync Server (Конференц-связь с телефонным подключением)</span><span class="sxs-lookup"><span data-stu-id="b4419-224">Lync Server Conferencing Attendant service (dial-in conferencing)</span></span></p></td>
<td><p><span data-ttu-id="b4419-225">5072</span><span class="sxs-lookup"><span data-stu-id="b4419-225">5072</span></span></p></td>
<td><p><span data-ttu-id="b4419-226">TCP</span><span class="sxs-lookup"><span data-stu-id="b4419-226">TCP</span></span></p></td>
<td><p><span data-ttu-id="b4419-227">Используется для входящих SIP-запросов для помощника по конференц-связи" (с телефонным подключением).</span><span class="sxs-lookup"><span data-stu-id="b4419-227">Used for incoming SIP requests for Attendant (dial in conferencing).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4419-228">Серверы переднего плана, на которых также работает совмещенный сервер-посредник</span><span class="sxs-lookup"><span data-stu-id="b4419-228">Front End Servers that also run a Collocated Mediation Server</span></span></p></td>
<td><p><span data-ttu-id="b4419-229">Служба "серверное исправление Lync"</span><span class="sxs-lookup"><span data-stu-id="b4419-229">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="b4419-230">5070</span><span class="sxs-lookup"><span data-stu-id="b4419-230">5070</span></span></p></td>
<td><p><span data-ttu-id="b4419-231">TCP</span><span class="sxs-lookup"><span data-stu-id="b4419-231">TCP</span></span></p></td>
<td><p><span data-ttu-id="b4419-232">Используется сервером-посредником для входящих запросов от сервера переднего плана к серверу посреднику.</span><span class="sxs-lookup"><span data-stu-id="b4419-232">Used by the Mediation Server for incoming requests from the Front End Server to the Mediation Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4419-233">Серверы переднего плана, на которых также работает соотнесенный сервер-посредник</span><span class="sxs-lookup"><span data-stu-id="b4419-233">Front End Servers that also run a Collocated Mediation Server</span></span></p></td>
<td><p><span data-ttu-id="b4419-234">Служба "серверное исправление Lync"</span><span class="sxs-lookup"><span data-stu-id="b4419-234">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="b4419-235">5067</span><span class="sxs-lookup"><span data-stu-id="b4419-235">5067</span></span></p></td>
<td><p><span data-ttu-id="b4419-236">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="b4419-236">TCP (TLS)</span></span></p></td>
<td><p><span data-ttu-id="b4419-237">Используется для входящих SIP-запросов от шлюза ТСОП к серверу-посреднику.</span><span class="sxs-lookup"><span data-stu-id="b4419-237">Used for incoming SIP requests from the PSTN gateway to the Mediation Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4419-238">Серверы переднего плана, на которых также работает соотнесенный сервер-посредник</span><span class="sxs-lookup"><span data-stu-id="b4419-238">Front End Servers that also run a Collocated Mediation Server</span></span></p></td>
<td><p><span data-ttu-id="b4419-239">Служба "серверное исправление Lync"</span><span class="sxs-lookup"><span data-stu-id="b4419-239">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="b4419-240">5068</span><span class="sxs-lookup"><span data-stu-id="b4419-240">5068</span></span></p></td>
<td><p><span data-ttu-id="b4419-241">TCP</span><span class="sxs-lookup"><span data-stu-id="b4419-241">TCP</span></span></p></td>
<td><p><span data-ttu-id="b4419-242">Используется для входящих SIP-запросов от шлюза ТСОП к серверу-посреднику.</span><span class="sxs-lookup"><span data-stu-id="b4419-242">Used for incoming SIP requests from the PSTN gateway to the Mediation Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4419-243">Серверы переднего плана, на которых также работает соотнесенный сервер-посредник</span><span class="sxs-lookup"><span data-stu-id="b4419-243">Front End Servers that also run a Collocated Mediation Server</span></span></p></td>
<td><p><span data-ttu-id="b4419-244">Служба "серверное исправление Lync"</span><span class="sxs-lookup"><span data-stu-id="b4419-244">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="b4419-245">5081</span><span class="sxs-lookup"><span data-stu-id="b4419-245">5081</span></span></p></td>
<td><p><span data-ttu-id="b4419-246">TCP</span><span class="sxs-lookup"><span data-stu-id="b4419-246">TCP</span></span></p></td>
<td><p><span data-ttu-id="b4419-247">Используется для исходящих SIP-запросов от сервера-посредника к шлюзу ТСОП.</span><span class="sxs-lookup"><span data-stu-id="b4419-247">Used for outgoing SIP requests from the Mediation Server to the PSTN gateway.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4419-248">Серверы переднего плана, на которых также работает соотнесенный сервер-посредник</span><span class="sxs-lookup"><span data-stu-id="b4419-248">Front End Servers that also run a Collocated Mediation Server</span></span></p></td>
<td><p><span data-ttu-id="b4419-249">Служба "серверное исправление Lync"</span><span class="sxs-lookup"><span data-stu-id="b4419-249">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="b4419-250">5082</span><span class="sxs-lookup"><span data-stu-id="b4419-250">5082</span></span></p></td>
<td><p><span data-ttu-id="b4419-251">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="b4419-251">TCP (TLS)</span></span></p></td>
<td><p><span data-ttu-id="b4419-252">Используется для исходящих SIP-запросов от сервера-посредника к шлюзу ТСОП.</span><span class="sxs-lookup"><span data-stu-id="b4419-252">Used for outgoing SIP requests from the Mediation Server to the PSTN gateway.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4419-253">Серверы переднего плана</span><span class="sxs-lookup"><span data-stu-id="b4419-253">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b4419-254">Служба общего обмена приложениями в Lync Server</span><span class="sxs-lookup"><span data-stu-id="b4419-254">Lync Server Application Sharing service</span></span></p></td>
<td><p><span data-ttu-id="b4419-255">5065</span><span class="sxs-lookup"><span data-stu-id="b4419-255">5065</span></span></p></td>
<td><p><span data-ttu-id="b4419-256">TCP</span><span class="sxs-lookup"><span data-stu-id="b4419-256">TCP</span></span></p></td>
<td><p><span data-ttu-id="b4419-257">Используется для входящих SIP-запросов на прослушивание для общего доступа к приложению.</span><span class="sxs-lookup"><span data-stu-id="b4419-257">Used for incoming SIP listening requests for application sharing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4419-258">Серверы переднего плана</span><span class="sxs-lookup"><span data-stu-id="b4419-258">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b4419-259">Служба общего обмена приложениями в Lync Server</span><span class="sxs-lookup"><span data-stu-id="b4419-259">Lync Server Application Sharing service</span></span></p></td>
<td><p><span data-ttu-id="b4419-260">49152-65535</span><span class="sxs-lookup"><span data-stu-id="b4419-260">49152-65535</span></span></p></td>
<td><p><span data-ttu-id="b4419-261">TCP</span><span class="sxs-lookup"><span data-stu-id="b4419-261">TCP</span></span></p></td>
<td><p><span data-ttu-id="b4419-262">Диапазон портов, используемых для общего доступа к приложению.</span><span class="sxs-lookup"><span data-stu-id="b4419-262">Media port range used for application sharing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4419-263">Серверы переднего плана</span><span class="sxs-lookup"><span data-stu-id="b4419-263">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b4419-264">Служба объявлений Lync Server конференций</span><span class="sxs-lookup"><span data-stu-id="b4419-264">Lync Server Conferencing Announcement service</span></span></p></td>
<td><p><span data-ttu-id="b4419-265">5073</span><span class="sxs-lookup"><span data-stu-id="b4419-265">5073</span></span></p></td>
<td><p><span data-ttu-id="b4419-266">TCP</span><span class="sxs-lookup"><span data-stu-id="b4419-266">TCP</span></span></p></td>
<td><p><span data-ttu-id="b4419-267">Используется для входящих запросов SIP для службы объявления конференций Lync Server (то есть для конференц-связи с телефонным подключением).</span><span class="sxs-lookup"><span data-stu-id="b4419-267">Used for incoming SIP requests for the Lync Server Conferencing Announcement service (that is, for dial-in conferencing).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4419-268">Серверы переднего плана</span><span class="sxs-lookup"><span data-stu-id="b4419-268">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b4419-269">приостановки вызовов Lync Server</span><span class="sxs-lookup"><span data-stu-id="b4419-269">Lync Server Call Park service</span></span></p></td>
<td><p><span data-ttu-id="b4419-270">5075</span><span class="sxs-lookup"><span data-stu-id="b4419-270">5075</span></span></p></td>
<td><p><span data-ttu-id="b4419-271">TCP</span><span class="sxs-lookup"><span data-stu-id="b4419-271">TCP</span></span></p></td>
<td><p><span data-ttu-id="b4419-272">Используется для входящих SIP-запросов для приложения парковки вызовов.</span><span class="sxs-lookup"><span data-stu-id="b4419-272">Used for incoming SIP requests for the Call Park application.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4419-273">Серверы переднего плана</span><span class="sxs-lookup"><span data-stu-id="b4419-273">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b4419-274">Служба проверки звука в Lync Server</span><span class="sxs-lookup"><span data-stu-id="b4419-274">Lync Server Audio Test service</span></span></p></td>
<td><p><span data-ttu-id="b4419-275">5076</span><span class="sxs-lookup"><span data-stu-id="b4419-275">5076</span></span></p></td>
<td><p><span data-ttu-id="b4419-276">TCP</span><span class="sxs-lookup"><span data-stu-id="b4419-276">TCP</span></span></p></td>
<td><p><span data-ttu-id="b4419-277">Используется для входящих SIP-запросов для службы проверки аудиосвязи.</span><span class="sxs-lookup"><span data-stu-id="b4419-277">Used for incoming SIP requests for the Audio Test service.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4419-278">Серверы переднего плана</span><span class="sxs-lookup"><span data-stu-id="b4419-278">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b4419-279">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="b4419-279">Not applicable</span></span></p></td>
<td><p><span data-ttu-id="b4419-280">5066</span><span class="sxs-lookup"><span data-stu-id="b4419-280">5066</span></span></p></td>
<td><p><span data-ttu-id="b4419-281">TCP</span><span class="sxs-lookup"><span data-stu-id="b4419-281">TCP</span></span></p></td>
<td><p><span data-ttu-id="b4419-282">Используется для исходящего трафика в шлюзе службы Enhanced 9-1-1 (E9-1-1).</span><span class="sxs-lookup"><span data-stu-id="b4419-282">Used for outbound Enhanced 9-1-1 (E9-1-1) gateway.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4419-283">Серверы переднего плана</span><span class="sxs-lookup"><span data-stu-id="b4419-283">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b4419-284">группы ответа Lync Server</span><span class="sxs-lookup"><span data-stu-id="b4419-284">Lync Server Response Group service</span></span></p></td>
<td><p><span data-ttu-id="b4419-285">5071</span><span class="sxs-lookup"><span data-stu-id="b4419-285">5071</span></span></p></td>
<td><p><span data-ttu-id="b4419-286">TCP</span><span class="sxs-lookup"><span data-stu-id="b4419-286">TCP</span></span></p></td>
<td><p><span data-ttu-id="b4419-287">Используется для входящих SIP-запросов для приложения группы ответа.</span><span class="sxs-lookup"><span data-stu-id="b4419-287">Used for incoming SIP requests for the Response Group application.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4419-288">Серверы переднего плана</span><span class="sxs-lookup"><span data-stu-id="b4419-288">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b4419-289">группы ответа Lync Server</span><span class="sxs-lookup"><span data-stu-id="b4419-289">Lync Server Response Group service</span></span></p></td>
<td><p><span data-ttu-id="b4419-290">8404</span><span class="sxs-lookup"><span data-stu-id="b4419-290">8404</span></span></p></td>
<td><p><span data-ttu-id="b4419-291">TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="b4419-291">TCP (MTLS)</span></span></p></td>
<td><p><span data-ttu-id="b4419-292">Используется для входящих SIP-запросов для приложения группы ответа.</span><span class="sxs-lookup"><span data-stu-id="b4419-292">Used for incoming SIP requests for the Response Group application.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4419-293">Серверы переднего плана</span><span class="sxs-lookup"><span data-stu-id="b4419-293">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b4419-294">Служба политики пропускной способности Lync Server</span><span class="sxs-lookup"><span data-stu-id="b4419-294">Lync Server Bandwidth Policy Service</span></span></p></td>
<td><p><span data-ttu-id="b4419-295">5080</span><span class="sxs-lookup"><span data-stu-id="b4419-295">5080</span></span></p></td>
<td><p><span data-ttu-id="b4419-296">TCP</span><span class="sxs-lookup"><span data-stu-id="b4419-296">TCP</span></span></p></td>
<td><p><span data-ttu-id="b4419-297">Используется для контроля допуска звонков, осуществляемого службой политики пропускной способности в отношении пограничного аудио-/видео-трафика "TURN".</span><span class="sxs-lookup"><span data-stu-id="b4419-297">Used for call admission control by the Bandwidth Policy service for A/V Edge TURN traffic.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4419-298">Серверы переднего плана</span><span class="sxs-lookup"><span data-stu-id="b4419-298">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b4419-299">Служба политики пропускной способности Lync Server</span><span class="sxs-lookup"><span data-stu-id="b4419-299">Lync Server Bandwidth Policy Service</span></span></p></td>
<td><p><span data-ttu-id="b4419-300">448</span><span class="sxs-lookup"><span data-stu-id="b4419-300">448</span></span></p></td>
<td><p><span data-ttu-id="b4419-301">TCP</span><span class="sxs-lookup"><span data-stu-id="b4419-301">TCP</span></span></p></td>
<td><p><span data-ttu-id="b4419-302">Используется службой политики пропускной способности Lync Server для управления допуском звонков.</span><span class="sxs-lookup"><span data-stu-id="b4419-302">Used for call admission control by the Lync Server Bandwidth Policy Service.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4419-303">Серверы переднего плана, на которых находится центральное хранилище управления</span><span class="sxs-lookup"><span data-stu-id="b4419-303">Front End Servers where the Central Management store resides</span></span></p></td>
<td><p><span data-ttu-id="b4419-304">Служба агента репликатора главной реплики Lync Server</span><span class="sxs-lookup"><span data-stu-id="b4419-304">Lync Server Master Replicator Agent service</span></span></p></td>
<td><p><span data-ttu-id="b4419-305">445</span><span class="sxs-lookup"><span data-stu-id="b4419-305">445</span></span></p></td>
<td><p><span data-ttu-id="b4419-306">TCP</span><span class="sxs-lookup"><span data-stu-id="b4419-306">TCP</span></span></p></td>
<td><p><span data-ttu-id="b4419-307">Используется для принудительной отправки данных конфигурации из хранилища центрального управления на серверы Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b4419-307">Used to push configuration data from the Central Management store to servers running Lync Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4419-308">Все серверы</span><span class="sxs-lookup"><span data-stu-id="b4419-308">All Servers</span></span></p></td>
<td><p><span data-ttu-id="b4419-309">Браузер SQL</span><span class="sxs-lookup"><span data-stu-id="b4419-309">SQL Browser</span></span></p></td>
<td><p><span data-ttu-id="b4419-310">1434</span><span class="sxs-lookup"><span data-stu-id="b4419-310">1434</span></span></p></td>
<td><p><span data-ttu-id="b4419-311">UDP</span><span class="sxs-lookup"><span data-stu-id="b4419-311">UDP</span></span></p></td>
<td><p><span data-ttu-id="b4419-312">Браузер SQL для локальной реплицированной копии данных сервера центрального хранилища управления в локальном экземпляре SQL Server</span><span class="sxs-lookup"><span data-stu-id="b4419-312">SQL Browser for local replicated copy of Central Management store data in local SQL Server instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4419-313">Все внутренние серверы</span><span class="sxs-lookup"><span data-stu-id="b4419-313">All internal servers</span></span></p></td>
<td><p><span data-ttu-id="b4419-314">Разное</span><span class="sxs-lookup"><span data-stu-id="b4419-314">Various</span></span></p></td>
<td><p><span data-ttu-id="b4419-315">49152-57500</span><span class="sxs-lookup"><span data-stu-id="b4419-315">49152-57500</span></span></p></td>
<td><p><span data-ttu-id="b4419-316">TCP/UDP</span><span class="sxs-lookup"><span data-stu-id="b4419-316">TCP/UDP</span></span></p></td>
<td><p><span data-ttu-id="b4419-317">Диапазон портов, используемых для аудиоконференций на всех внутренних серверах.</span><span class="sxs-lookup"><span data-stu-id="b4419-317">Media port range used for audio conferencing on all internal servers.</span></span> <span data-ttu-id="b4419-318">Используется всеми серверами, которые применяют звуковое сопровождение: серверы переднего плана (служба помощника по конференциям Lync Server, служба объявления конференций Lync Server) и сервер исправлений.</span><span class="sxs-lookup"><span data-stu-id="b4419-318">Used by all servers that terminate audio: Front End Servers (for Lync Server Conferencing Attendant service, Lync Server Conferencing Announcement service, and Lync Server Audio/Video Conferencing service), and Mediation Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4419-319">Серверы Office Web Apps</span><span class="sxs-lookup"><span data-stu-id="b4419-319">Office Web Apps Servers</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b4419-320">443</span><span class="sxs-lookup"><span data-stu-id="b4419-320">443</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b4419-321">Используется в Lync Server 2013 для подключения к серверу Office Web Apps.</span><span class="sxs-lookup"><span data-stu-id="b4419-321">Used by Lync Server 2013 to connect to Office Web Apps Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4419-322">Директоры</span><span class="sxs-lookup"><span data-stu-id="b4419-322">Directors</span></span></p></td>
<td><p><span data-ttu-id="b4419-323">Служба Lync Server Front-End Service</span><span class="sxs-lookup"><span data-stu-id="b4419-323">Lync Server Front-End service</span></span></p></td>
<td><p><span data-ttu-id="b4419-324">5060</span><span class="sxs-lookup"><span data-stu-id="b4419-324">5060</span></span></p></td>
<td><p><span data-ttu-id="b4419-325">TCP</span><span class="sxs-lookup"><span data-stu-id="b4419-325">TCP</span></span></p></td>
<td><p><span data-ttu-id="b4419-326">При необходимости используется для статических маршрутов к доверенным службам, таким как серверы удаленного управления звонками.</span><span class="sxs-lookup"><span data-stu-id="b4419-326">Optionally used for static routes to trusted services, such as remote call control servers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4419-327">Директоры</span><span class="sxs-lookup"><span data-stu-id="b4419-327">Directors</span></span></p></td>
<td><p><span data-ttu-id="b4419-328">Служба Lync Server Front-End Service</span><span class="sxs-lookup"><span data-stu-id="b4419-328">Lync Server Front-End service</span></span></p></td>
<td><p><span data-ttu-id="b4419-329">444</span><span class="sxs-lookup"><span data-stu-id="b4419-329">444</span></span></p></td>
<td><p><span data-ttu-id="b4419-330">HTTPS</span><span class="sxs-lookup"><span data-stu-id="b4419-330">HTTPS</span></span></p>
<p><span data-ttu-id="b4419-331">TCP</span><span class="sxs-lookup"><span data-stu-id="b4419-331">TCP</span></span></p></td>
<td><p><span data-ttu-id="b4419-332">Обмен данными между сервером переднего плана и сервером директора.</span><span class="sxs-lookup"><span data-stu-id="b4419-332">Inter-server communication between Front End and Director.</span></span> <span data-ttu-id="b4419-333">Также публикация клиентских сертификатов (на серверах переднего плана) и их проверка, если они уже опубликованы.</span><span class="sxs-lookup"><span data-stu-id="b4419-333">Additionally, client certificate publish (to Front End Servers) or validate if the client certificate has already been published.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4419-334">Директоры</span><span class="sxs-lookup"><span data-stu-id="b4419-334">Directors</span></span></p></td>
<td><p><span data-ttu-id="b4419-335">Служба веб-совместимости Lync Server</span><span class="sxs-lookup"><span data-stu-id="b4419-335">Lync Server Web Compatibility service</span></span></p></td>
<td><p><span data-ttu-id="b4419-336">80</span><span class="sxs-lookup"><span data-stu-id="b4419-336">80</span></span></p></td>
<td><p><span data-ttu-id="b4419-337">TCP</span><span class="sxs-lookup"><span data-stu-id="b4419-337">TCP</span></span></p></td>
<td><p><span data-ttu-id="b4419-p105">Используется для исходного подключения от директоров к полным доменным именам в веб-ферме (URL-адреса используются по веб-компонентам IIS). При обычной работе происходит переключение на трафик HTTPS с использованием порта 443 и протокола TCP.</span><span class="sxs-lookup"><span data-stu-id="b4419-p105">Used for initial communication from Directors to the web farm FQDNs (the URLs used by IIS web components). In normal operation, will switch to HTTPS traffic, using port 443 and protocol type TCP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4419-340">Директоры</span><span class="sxs-lookup"><span data-stu-id="b4419-340">Directors</span></span></p></td>
<td><p><span data-ttu-id="b4419-341">Служба веб-совместимости Lync Server</span><span class="sxs-lookup"><span data-stu-id="b4419-341">Lync Server Web Compatibility service</span></span></p></td>
<td><p><span data-ttu-id="b4419-342">443</span><span class="sxs-lookup"><span data-stu-id="b4419-342">443</span></span></p></td>
<td><p><span data-ttu-id="b4419-343">HTTPS</span><span class="sxs-lookup"><span data-stu-id="b4419-343">HTTPS</span></span></p></td>
<td><p><span data-ttu-id="b4419-344">Используется для подключения от директоров к полным доменным именам в веб-ферме (URL-адреса используются по веб-компонентам IIS).</span><span class="sxs-lookup"><span data-stu-id="b4419-344">Used for communication from Directors to the web farm FQDNs (the URLs used by IIS web components).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4419-345">Директоры</span><span class="sxs-lookup"><span data-stu-id="b4419-345">Directors</span></span></p></td>
<td><p><span data-ttu-id="b4419-346">Служба Lync Server Front-End Service</span><span class="sxs-lookup"><span data-stu-id="b4419-346">Lync Server Front-End service</span></span></p></td>
<td><p><span data-ttu-id="b4419-347">5061</span><span class="sxs-lookup"><span data-stu-id="b4419-347">5061</span></span></p></td>
<td><p><span data-ttu-id="b4419-348">TCP</span><span class="sxs-lookup"><span data-stu-id="b4419-348">TCP</span></span></p></td>
<td><p><span data-ttu-id="b4419-349">Используется для внутренних подключений между серверами и для клиентских подключений.</span><span class="sxs-lookup"><span data-stu-id="b4419-349">Used for internal communications between servers and for client connections.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4419-350">Серверы-посредники</span><span class="sxs-lookup"><span data-stu-id="b4419-350">Mediation Servers</span></span></p></td>
<td><p><span data-ttu-id="b4419-351">Служба "серверное исправление Lync"</span><span class="sxs-lookup"><span data-stu-id="b4419-351">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="b4419-352">5070</span><span class="sxs-lookup"><span data-stu-id="b4419-352">5070</span></span></p></td>
<td><p><span data-ttu-id="b4419-353">TCP</span><span class="sxs-lookup"><span data-stu-id="b4419-353">TCP</span></span></p></td>
<td><p><span data-ttu-id="b4419-354">Используется сервером-посредником для входящих запросов от сервера переднего плана.</span><span class="sxs-lookup"><span data-stu-id="b4419-354">Used by the Mediation Server for incoming requests from the Front End Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4419-355">Серверы-посредники</span><span class="sxs-lookup"><span data-stu-id="b4419-355">Mediation Servers</span></span></p></td>
<td><p><span data-ttu-id="b4419-356">Служба "серверное исправление Lync"</span><span class="sxs-lookup"><span data-stu-id="b4419-356">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="b4419-357">5067</span><span class="sxs-lookup"><span data-stu-id="b4419-357">5067</span></span></p></td>
<td><p><span data-ttu-id="b4419-358">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="b4419-358">TCP (TLS)</span></span></p></td>
<td><p><span data-ttu-id="b4419-359">Используется для входящих SIP-запросов от шлюза ТСОП.</span><span class="sxs-lookup"><span data-stu-id="b4419-359">Used for incoming SIP requests from the PSTN gateway.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4419-360">Серверы-посредники</span><span class="sxs-lookup"><span data-stu-id="b4419-360">Mediation Servers</span></span></p></td>
<td><p><span data-ttu-id="b4419-361">Служба "серверное исправление Lync"</span><span class="sxs-lookup"><span data-stu-id="b4419-361">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="b4419-362">5068</span><span class="sxs-lookup"><span data-stu-id="b4419-362">5068</span></span></p></td>
<td><p><span data-ttu-id="b4419-363">TCP</span><span class="sxs-lookup"><span data-stu-id="b4419-363">TCP</span></span></p></td>
<td><p><span data-ttu-id="b4419-364">Используется для входящих SIP-запросов от шлюза ТСОП.</span><span class="sxs-lookup"><span data-stu-id="b4419-364">Used for incoming SIP requests from the PSTN gateway.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4419-365">Серверы-посредники</span><span class="sxs-lookup"><span data-stu-id="b4419-365">Mediation Servers</span></span></p></td>
<td><p><span data-ttu-id="b4419-366">Служба "серверное исправление Lync"</span><span class="sxs-lookup"><span data-stu-id="b4419-366">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="b4419-367">5070</span><span class="sxs-lookup"><span data-stu-id="b4419-367">5070</span></span></p></td>
<td><p><span data-ttu-id="b4419-368">TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="b4419-368">TCP (MTLS)</span></span></p></td>
<td><p><span data-ttu-id="b4419-369">Используется для SIP-запросов от серверов переднего плана.</span><span class="sxs-lookup"><span data-stu-id="b4419-369">Used for SIP requests from the Front End Servers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4419-370">Сервер переднего плана сохраняемого чата</span><span class="sxs-lookup"><span data-stu-id="b4419-370">Persistent Chat Front End Server</span></span></p></td>
<td><p><span data-ttu-id="b4419-371">SIP-запрос сохраняемого чата</span><span class="sxs-lookup"><span data-stu-id="b4419-371">Persistent Chat SIP</span></span></p></td>
<td><p><span data-ttu-id="b4419-372">5041</span><span class="sxs-lookup"><span data-stu-id="b4419-372">5041</span></span></p></td>
<td><p><span data-ttu-id="b4419-373">TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="b4419-373">TCP (MTLS)</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4419-374">Сервер переднего плана сохраняемого чата</span><span class="sxs-lookup"><span data-stu-id="b4419-374">Persistent Chat Front End Server</span></span></p></td>
<td><p><span data-ttu-id="b4419-375">Платформа Windows Communication Foundation (WCF) для сохраняемого чата</span><span class="sxs-lookup"><span data-stu-id="b4419-375">Persistent Chat Windows Communication Foundation (WCF)</span></span></p></td>
<td><p><span data-ttu-id="b4419-376">881</span><span class="sxs-lookup"><span data-stu-id="b4419-376">881</span></span></p></td>
<td><p><span data-ttu-id="b4419-377">TCP (TLS) и TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="b4419-377">TCP (TLS) and TCP (MTLS)</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4419-378">Сервер переднего плана сохраняемого чата</span><span class="sxs-lookup"><span data-stu-id="b4419-378">Persistent Chat Front End Server</span></span></p></td>
<td><p><span data-ttu-id="b4419-379">Служба передачи файлов для сохраняемого чата</span><span class="sxs-lookup"><span data-stu-id="b4419-379">Persistent Chat File Transfer Service</span></span></p></td>
<td><p><span data-ttu-id="b4419-380">443</span><span class="sxs-lookup"><span data-stu-id="b4419-380">443</span></span></p></td>
<td><p><span data-ttu-id="b4419-381">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="b4419-381">TCP (TLS)</span></span></p></td>
<td></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="b4419-382">Для некоторых сценариев с удаленным управлением звонками требуется TCP-соединение между сервером переднего плана или директором и УАТС.</span><span class="sxs-lookup"><span data-stu-id="b4419-382">Some remote call control scenarios require a TCP connection between the Front End Server or Director and the PBX.</span></span> <span data-ttu-id="b4419-383">Несмотря на то, что Lync Server больше не использует TCP-порт 5060, при развертывании удаленного управления звонками вы создаете конфигурацию доверенного сервера, которая связывает полное доменное имя сервера для подключений по протоколу RCC с портом TCP, который будет использоваться интерфейсом Front End Server для подключения к системе УАТС.</span><span class="sxs-lookup"><span data-stu-id="b4419-383">Although Lync Server no longer uses TCP port 5060, during remote call control deployment you create a trusted server configuration, which associates the RCC Line Server FQDN with the TCP port that the Front End Server or Director will use to connect to the PBX system.</span></span> <span data-ttu-id="b4419-384">Дополнительные сведения можно найти в командлете <STRONG>CsTrustedApplicationComputer</STRONG> в документации по среде управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b4419-384">For details, see the <STRONG>CsTrustedApplicationComputer</STRONG> cmdlet in the Lync Server Management Shell documentation.</span></span>



</div>

<span data-ttu-id="b4419-385">Для пулов, использующих только аппаратную балансировку нагрузки (без балансировки нагрузки на DNS), в следующей таблице представлены порты, которые должны быть открыты на аппаратных балансировщиках нагрузки.</span><span class="sxs-lookup"><span data-stu-id="b4419-385">For your pools that use only hardware load balancing (not DNS load balancing), the following table shows the ports that need to open the hardware load balancers.</span></span>

### <a name="hardware-load-balancer-ports-if-using-only-hardware-load-balancing"></a><span data-ttu-id="b4419-386">Порты аппаратного балансировщика нагрузки при использовании только аппаратной балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="b4419-386">Hardware Load Balancer Ports if Using Only Hardware Load Balancing</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b4419-387">Балансировщик нагрузки</span><span class="sxs-lookup"><span data-stu-id="b4419-387">Load Balancer</span></span></th>
<th><span data-ttu-id="b4419-388">Порт</span><span class="sxs-lookup"><span data-stu-id="b4419-388">Port</span></span></th>
<th><span data-ttu-id="b4419-389">Протокол</span><span class="sxs-lookup"><span data-stu-id="b4419-389">Protocol</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b4419-390">Балансировщик нагрузки сервера переднего плана</span><span class="sxs-lookup"><span data-stu-id="b4419-390">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="b4419-391">5061</span><span class="sxs-lookup"><span data-stu-id="b4419-391">5061</span></span></p></td>
<td><p><span data-ttu-id="b4419-392">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="b4419-392">TCP (TLS)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4419-393">Балансировщик нагрузки сервера переднего плана</span><span class="sxs-lookup"><span data-stu-id="b4419-393">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="b4419-394">444</span><span class="sxs-lookup"><span data-stu-id="b4419-394">444</span></span></p></td>
<td><p><span data-ttu-id="b4419-395">HTTPS</span><span class="sxs-lookup"><span data-stu-id="b4419-395">HTTPS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4419-396">Балансировщик нагрузки сервера переднего плана</span><span class="sxs-lookup"><span data-stu-id="b4419-396">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="b4419-397">135</span><span class="sxs-lookup"><span data-stu-id="b4419-397">135</span></span></p></td>
<td><p><span data-ttu-id="b4419-398">DCOM и удаленный вызов процедур (RPC)</span><span class="sxs-lookup"><span data-stu-id="b4419-398">DCOM and remote procedure call (RPC)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4419-399">Балансировщик нагрузки сервера переднего плана</span><span class="sxs-lookup"><span data-stu-id="b4419-399">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="b4419-400">80</span><span class="sxs-lookup"><span data-stu-id="b4419-400">80</span></span></p></td>
<td><p><span data-ttu-id="b4419-401">HTTP</span><span class="sxs-lookup"><span data-stu-id="b4419-401">HTTP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4419-402">Балансировщик нагрузки сервера переднего плана</span><span class="sxs-lookup"><span data-stu-id="b4419-402">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="b4419-403">8080</span><span class="sxs-lookup"><span data-stu-id="b4419-403">8080</span></span></p></td>
<td><p><span data-ttu-id="b4419-404">TCP-клиенты и устройства, подлинность которых проверяется с помощью NTLM на сервере переднего плана и на устройствах.</span><span class="sxs-lookup"><span data-stu-id="b4419-404">TCP - Client and device retrieval of root certificate from Front End Server – clients and devices authenticated by NTLM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4419-405">Балансировщик нагрузки сервера переднего плана</span><span class="sxs-lookup"><span data-stu-id="b4419-405">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="b4419-406">443</span><span class="sxs-lookup"><span data-stu-id="b4419-406">443</span></span></p></td>
<td><p><span data-ttu-id="b4419-407">HTTPS</span><span class="sxs-lookup"><span data-stu-id="b4419-407">HTTPS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4419-408">Балансировщик нагрузки сервера переднего плана</span><span class="sxs-lookup"><span data-stu-id="b4419-408">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="b4419-409">4443</span><span class="sxs-lookup"><span data-stu-id="b4419-409">4443</span></span></p></td>
<td><p><span data-ttu-id="b4419-410">HTTPS (от обратного прокси-сервера)</span><span class="sxs-lookup"><span data-stu-id="b4419-410">HTTPS (from reverse proxy)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4419-411">Балансировщик нагрузки сервера переднего плана</span><span class="sxs-lookup"><span data-stu-id="b4419-411">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="b4419-412">5072</span><span class="sxs-lookup"><span data-stu-id="b4419-412">5072</span></span></p></td>
<td><p><span data-ttu-id="b4419-413">TCP</span><span class="sxs-lookup"><span data-stu-id="b4419-413">TCP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4419-414">Балансировщик нагрузки сервера переднего плана</span><span class="sxs-lookup"><span data-stu-id="b4419-414">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="b4419-415">5073</span><span class="sxs-lookup"><span data-stu-id="b4419-415">5073</span></span></p></td>
<td><p><span data-ttu-id="b4419-416">TCP</span><span class="sxs-lookup"><span data-stu-id="b4419-416">TCP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4419-417">Балансировщик нагрузки сервера переднего плана</span><span class="sxs-lookup"><span data-stu-id="b4419-417">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="b4419-418">5075</span><span class="sxs-lookup"><span data-stu-id="b4419-418">5075</span></span></p></td>
<td><p><span data-ttu-id="b4419-419">TCP</span><span class="sxs-lookup"><span data-stu-id="b4419-419">TCP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4419-420">Балансировщик нагрузки сервера переднего плана</span><span class="sxs-lookup"><span data-stu-id="b4419-420">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="b4419-421">5076</span><span class="sxs-lookup"><span data-stu-id="b4419-421">5076</span></span></p></td>
<td><p><span data-ttu-id="b4419-422">TCP</span><span class="sxs-lookup"><span data-stu-id="b4419-422">TCP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4419-423">Балансировщик нагрузки сервера переднего плана</span><span class="sxs-lookup"><span data-stu-id="b4419-423">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="b4419-424">5071</span><span class="sxs-lookup"><span data-stu-id="b4419-424">5071</span></span></p></td>
<td><p><span data-ttu-id="b4419-425">TCP</span><span class="sxs-lookup"><span data-stu-id="b4419-425">TCP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4419-426">Балансировщик нагрузки сервера переднего плана</span><span class="sxs-lookup"><span data-stu-id="b4419-426">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="b4419-427">5080</span><span class="sxs-lookup"><span data-stu-id="b4419-427">5080</span></span></p></td>
<td><p><span data-ttu-id="b4419-428">TCP</span><span class="sxs-lookup"><span data-stu-id="b4419-428">TCP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4419-429">Балансировщик нагрузки сервера переднего плана</span><span class="sxs-lookup"><span data-stu-id="b4419-429">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="b4419-430">448</span><span class="sxs-lookup"><span data-stu-id="b4419-430">448</span></span></p></td>
<td><p><span data-ttu-id="b4419-431">TCP</span><span class="sxs-lookup"><span data-stu-id="b4419-431">TCP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4419-432">Балансировщик нагрузки сервера-посредника</span><span class="sxs-lookup"><span data-stu-id="b4419-432">Mediation Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="b4419-433">5070</span><span class="sxs-lookup"><span data-stu-id="b4419-433">5070</span></span></p></td>
<td><p><span data-ttu-id="b4419-434">TCP</span><span class="sxs-lookup"><span data-stu-id="b4419-434">TCP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4419-435">Балансировщик нагрузки на сервере переднего плана (если в пуле также работает сервер-посредник)</span><span class="sxs-lookup"><span data-stu-id="b4419-435">Front End Server load balancer (if the pool also runs Mediation Server)</span></span></p></td>
<td><p><span data-ttu-id="b4419-436">5070</span><span class="sxs-lookup"><span data-stu-id="b4419-436">5070</span></span></p></td>
<td><p><span data-ttu-id="b4419-437">TCP</span><span class="sxs-lookup"><span data-stu-id="b4419-437">TCP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4419-438">Балансировщик нагрузки директора</span><span class="sxs-lookup"><span data-stu-id="b4419-438">Director load balancer</span></span></p></td>
<td><p><span data-ttu-id="b4419-439">443</span><span class="sxs-lookup"><span data-stu-id="b4419-439">443</span></span></p></td>
<td><p><span data-ttu-id="b4419-440">HTTPS</span><span class="sxs-lookup"><span data-stu-id="b4419-440">HTTPS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4419-441">Балансировщик нагрузки директора</span><span class="sxs-lookup"><span data-stu-id="b4419-441">Director load balancer</span></span></p></td>
<td><p><span data-ttu-id="b4419-442">444</span><span class="sxs-lookup"><span data-stu-id="b4419-442">444</span></span></p></td>
<td><p><span data-ttu-id="b4419-443">HTTPS</span><span class="sxs-lookup"><span data-stu-id="b4419-443">HTTPS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4419-444">Балансировщик нагрузки директора</span><span class="sxs-lookup"><span data-stu-id="b4419-444">Director load balancer</span></span></p></td>
<td><p><span data-ttu-id="b4419-445">5061</span><span class="sxs-lookup"><span data-stu-id="b4419-445">5061</span></span></p></td>
<td><p><span data-ttu-id="b4419-446">TCP</span><span class="sxs-lookup"><span data-stu-id="b4419-446">TCP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4419-447">Балансировщик нагрузки директора</span><span class="sxs-lookup"><span data-stu-id="b4419-447">Director load balancer</span></span></p></td>
<td><p><span data-ttu-id="b4419-448">4443</span><span class="sxs-lookup"><span data-stu-id="b4419-448">4443</span></span></p></td>
<td><p><span data-ttu-id="b4419-449">HTTPS (от обратного прокси-сервера)</span><span class="sxs-lookup"><span data-stu-id="b4419-449">HTTPS (from reverse proxy)</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b4419-450">В пулах переднего плана и пулах директоров, использующих балансировку нагрузки на DNS, также должны быть развернуты аппаратные балансировщики нагрузки.</span><span class="sxs-lookup"><span data-stu-id="b4419-450">Your Front End pools and Director pools that use DNS load balancing also must have a hardware load balancer deployed.</span></span> <span data-ttu-id="b4419-451">В следующей таблице показаны порты, которые должны быть открыты на этих аппаратных балансировщиках нагрузки.</span><span class="sxs-lookup"><span data-stu-id="b4419-451">The following table shows the ports that need to be open on these hardware load balancers.</span></span>

### <a name="hardware-load-balancer-ports-if-using-dns-load-balancing"></a><span data-ttu-id="b4419-452">Порты аппаратного балансировщика нагрузки при использовании балансировки нагрузки на DNS</span><span class="sxs-lookup"><span data-stu-id="b4419-452">Hardware Load Balancer Ports if Using DNS Load Balancing</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b4419-453">Балансировщик нагрузки</span><span class="sxs-lookup"><span data-stu-id="b4419-453">Load Balancer</span></span></th>
<th><span data-ttu-id="b4419-454">Порт</span><span class="sxs-lookup"><span data-stu-id="b4419-454">Port</span></span></th>
<th><span data-ttu-id="b4419-455">Протокол</span><span class="sxs-lookup"><span data-stu-id="b4419-455">Protocol</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b4419-456">Балансировщик нагрузки сервера переднего плана</span><span class="sxs-lookup"><span data-stu-id="b4419-456">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="b4419-457">80</span><span class="sxs-lookup"><span data-stu-id="b4419-457">80</span></span></p></td>
<td><p><span data-ttu-id="b4419-458">HTTP</span><span class="sxs-lookup"><span data-stu-id="b4419-458">HTTP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4419-459">Балансировщик нагрузки сервера переднего плана</span><span class="sxs-lookup"><span data-stu-id="b4419-459">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="b4419-460">443</span><span class="sxs-lookup"><span data-stu-id="b4419-460">443</span></span></p></td>
<td><p><span data-ttu-id="b4419-461">HTTPS</span><span class="sxs-lookup"><span data-stu-id="b4419-461">HTTPS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4419-462">Балансировщик нагрузки сервера переднего плана</span><span class="sxs-lookup"><span data-stu-id="b4419-462">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="b4419-463">8080</span><span class="sxs-lookup"><span data-stu-id="b4419-463">8080</span></span></p></td>
<td><p><span data-ttu-id="b4419-464">TCP-клиенты и устройства, подлинность которых проверяется с помощью NTLM на сервере переднего плана и на устройствах.</span><span class="sxs-lookup"><span data-stu-id="b4419-464">TCP - Client and device retrieval of root certificate from Front End Server – clients and devices authenticated by NTLM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4419-465">Балансировщик нагрузки сервера переднего плана</span><span class="sxs-lookup"><span data-stu-id="b4419-465">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="b4419-466">4443</span><span class="sxs-lookup"><span data-stu-id="b4419-466">4443</span></span></p></td>
<td><p><span data-ttu-id="b4419-467">HTTPS (от обратного прокси-сервера)</span><span class="sxs-lookup"><span data-stu-id="b4419-467">HTTPS (from reverse proxy)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4419-468">Балансировщик нагрузки директора</span><span class="sxs-lookup"><span data-stu-id="b4419-468">Director load balancer</span></span></p></td>
<td><p><span data-ttu-id="b4419-469">443</span><span class="sxs-lookup"><span data-stu-id="b4419-469">443</span></span></p></td>
<td><p><span data-ttu-id="b4419-470">HTTPS</span><span class="sxs-lookup"><span data-stu-id="b4419-470">HTTPS</span></span></p></td>
</tr>
<tr class="even">
<td> </td>
<td> </td>
<td> </td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4419-471">Балансировщик нагрузки директора</span><span class="sxs-lookup"><span data-stu-id="b4419-471">Director load balancer</span></span></p></td>
<td><p><span data-ttu-id="b4419-472">4443</span><span class="sxs-lookup"><span data-stu-id="b4419-472">4443</span></span></p></td>
<td><p><span data-ttu-id="b4419-473">HTTPS (от обратного прокси-сервера)</span><span class="sxs-lookup"><span data-stu-id="b4419-473">HTTPS (from reverse proxy)</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="required-client-ports"></a><span data-ttu-id="b4419-474">Необходимые порты клиента</span><span class="sxs-lookup"><span data-stu-id="b4419-474">Required Client Ports</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b4419-475">Компонент</span><span class="sxs-lookup"><span data-stu-id="b4419-475">Component</span></span></th>
<th><span data-ttu-id="b4419-476">Порт</span><span class="sxs-lookup"><span data-stu-id="b4419-476">Port</span></span></th>
<th><span data-ttu-id="b4419-477">Протокол</span><span class="sxs-lookup"><span data-stu-id="b4419-477">Protocol</span></span></th>
<th><span data-ttu-id="b4419-478">Notes</span><span class="sxs-lookup"><span data-stu-id="b4419-478">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b4419-479">Клиенты</span><span class="sxs-lookup"><span data-stu-id="b4419-479">Clients</span></span></p></td>
<td><p><span data-ttu-id="b4419-480">67/68</span><span class="sxs-lookup"><span data-stu-id="b4419-480">67/68</span></span></p></td>
<td><p><span data-ttu-id="b4419-481">DHCP</span><span class="sxs-lookup"><span data-stu-id="b4419-481">DHCP</span></span></p></td>
<td><p><span data-ttu-id="b4419-482">Используется приложением Lync Server для поиска полного доменного имени регистратора (то есть в случае сбоя DNS SRV и ненастроенных параметров вручную).</span><span class="sxs-lookup"><span data-stu-id="b4419-482">Used by Lync Server to find the Registrar FQDN (that is, if DNS SRV fails and manual settings are not configured).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4419-483">Клиенты</span><span class="sxs-lookup"><span data-stu-id="b4419-483">Clients</span></span></p></td>
<td><p><span data-ttu-id="b4419-484">443</span><span class="sxs-lookup"><span data-stu-id="b4419-484">443</span></span></p></td>
<td><p><span data-ttu-id="b4419-485">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="b4419-485">TCP (TLS)</span></span></p></td>
<td><p><span data-ttu-id="b4419-486">Используется для SIP-трафика от клиента к серверу для доступа внешних пользователей.</span><span class="sxs-lookup"><span data-stu-id="b4419-486">Used for client-to-server SIP traffic for external user access.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4419-487">Клиенты</span><span class="sxs-lookup"><span data-stu-id="b4419-487">Clients</span></span></p></td>
<td><p><span data-ttu-id="b4419-488">443</span><span class="sxs-lookup"><span data-stu-id="b4419-488">443</span></span></p></td>
<td><p><span data-ttu-id="b4419-489">TCP (PSOM/TLS)</span><span class="sxs-lookup"><span data-stu-id="b4419-489">TCP (PSOM/TLS)</span></span></p></td>
<td><p><span data-ttu-id="b4419-490">Используется для доступа внешних пользователей к сеансам веб-конференций.</span><span class="sxs-lookup"><span data-stu-id="b4419-490">Used for external user access to web conferencing sessions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4419-491">Клиенты</span><span class="sxs-lookup"><span data-stu-id="b4419-491">Clients</span></span></p></td>
<td><p><span data-ttu-id="b4419-492">443</span><span class="sxs-lookup"><span data-stu-id="b4419-492">443</span></span></p></td>
<td><p><span data-ttu-id="b4419-493">TCP (STUN/MSTURN)</span><span class="sxs-lookup"><span data-stu-id="b4419-493">TCP (STUN/MSTURN)</span></span></p></td>
<td><p><span data-ttu-id="b4419-494">Используется для доступа внешних пользователей к аудио- и видеосеансам и сеансам мультимедиа (TCP)</span><span class="sxs-lookup"><span data-stu-id="b4419-494">Used for external user access to A/V sessions and media (TCP)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4419-495">Клиенты</span><span class="sxs-lookup"><span data-stu-id="b4419-495">Clients</span></span></p></td>
<td><p><span data-ttu-id="b4419-496">3478</span><span class="sxs-lookup"><span data-stu-id="b4419-496">3478</span></span></p></td>
<td><p><span data-ttu-id="b4419-497">UDP (STUN/MSTURN)</span><span class="sxs-lookup"><span data-stu-id="b4419-497">UDP (STUN/MSTURN)</span></span></p></td>
<td><p><span data-ttu-id="b4419-498">Используется для доступа внешних пользователей к аудио- и видеосеансам и сеансам мультимедиа (UDP)</span><span class="sxs-lookup"><span data-stu-id="b4419-498">Used for external user access to A/V sessions and media (UDP)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4419-499">Клиенты</span><span class="sxs-lookup"><span data-stu-id="b4419-499">Clients</span></span></p></td>
<td><p><span data-ttu-id="b4419-500">5061</span><span class="sxs-lookup"><span data-stu-id="b4419-500">5061</span></span></p></td>
<td><p><span data-ttu-id="b4419-501">TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="b4419-501">TCP (MTLS)</span></span></p></td>
<td><p><span data-ttu-id="b4419-502">Используется для SIP-трафика от клиента к серверу для доступа внешних пользователей.</span><span class="sxs-lookup"><span data-stu-id="b4419-502">Used for client-to-server SIP traffic for external user access.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4419-503">Клиенты</span><span class="sxs-lookup"><span data-stu-id="b4419-503">Clients</span></span></p></td>
<td><p><span data-ttu-id="b4419-504">6891–6901</span><span class="sxs-lookup"><span data-stu-id="b4419-504">6891-6901</span></span></p></td>
<td><p><span data-ttu-id="b4419-505">TCP</span><span class="sxs-lookup"><span data-stu-id="b4419-505">TCP</span></span></p></td>
<td><p><span data-ttu-id="b4419-506">Используется для передачи файлов между клиентами Lync и предыдущими клиентами (клиенты из Microsoft Office Communications Server 2007 R2, Microsoft Office Communications Server 2007 и Live Communications Server 2005).</span><span class="sxs-lookup"><span data-stu-id="b4419-506">Used for file transfer between Lync clients and previous clients (clients of Microsoft Office Communications Server 2007 R2, Microsoft Office Communications Server 2007, and Live Communications Server 2005).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4419-507">Клиенты</span><span class="sxs-lookup"><span data-stu-id="b4419-507">Clients</span></span></p></td>
<td><p><span data-ttu-id="b4419-508">1024-65535 \*</span><span class="sxs-lookup"><span data-stu-id="b4419-508">1024-65535 \*</span></span></p></td>
<td><p><span data-ttu-id="b4419-509">TCP/UDP</span><span class="sxs-lookup"><span data-stu-id="b4419-509">TCP/UDP</span></span></p></td>
<td><p><span data-ttu-id="b4419-510">Диапазон портов для передачи аудио (требуется минимум 20 портов).</span><span class="sxs-lookup"><span data-stu-id="b4419-510">Audio port range (minimum of 20 ports required)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4419-511">Клиенты</span><span class="sxs-lookup"><span data-stu-id="b4419-511">Clients</span></span></p></td>
<td><p><span data-ttu-id="b4419-512">1024-65535 \*</span><span class="sxs-lookup"><span data-stu-id="b4419-512">1024-65535 \*</span></span></p></td>
<td><p><span data-ttu-id="b4419-513">TCP/UDP</span><span class="sxs-lookup"><span data-stu-id="b4419-513">TCP/UDP</span></span></p></td>
<td><p><span data-ttu-id="b4419-514">Диапазон портов для передачи видео (требуется минимум 20 портов).</span><span class="sxs-lookup"><span data-stu-id="b4419-514">Video port range (minimum of 20 ports required).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4419-515">Клиенты</span><span class="sxs-lookup"><span data-stu-id="b4419-515">Clients</span></span></p></td>
<td><p><span data-ttu-id="b4419-516">1024-65535 \*</span><span class="sxs-lookup"><span data-stu-id="b4419-516">1024-65535 \*</span></span></p></td>
<td><p><span data-ttu-id="b4419-517">TCP</span><span class="sxs-lookup"><span data-stu-id="b4419-517">TCP</span></span></p></td>
<td><p><span data-ttu-id="b4419-518">Одноранговая передача файлов (для передачи файлов во время конференций клиенты используют протокол PSOM).</span><span class="sxs-lookup"><span data-stu-id="b4419-518">Peer-to-peer file transfer (for conferencing file transfer, clients use PSOM).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4419-519">Клиенты</span><span class="sxs-lookup"><span data-stu-id="b4419-519">Clients</span></span></p></td>
<td><p><span data-ttu-id="b4419-520">1024-65535 \*</span><span class="sxs-lookup"><span data-stu-id="b4419-520">1024-65535 \*</span></span></p></td>
<td><p><span data-ttu-id="b4419-521">TCP</span><span class="sxs-lookup"><span data-stu-id="b4419-521">TCP</span></span></p></td>
<td><p><span data-ttu-id="b4419-522">Общий доступ к приложениям.</span><span class="sxs-lookup"><span data-stu-id="b4419-522">Application sharing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4419-523">Телефон общего пользования Aastra 6721ip</span><span class="sxs-lookup"><span data-stu-id="b4419-523">Aastra 6721ip common area phone</span></span></p>
<p><span data-ttu-id="b4419-524">Стационарный телефон Aastra 6725ip</span><span class="sxs-lookup"><span data-stu-id="b4419-524">Aastra 6725ip desk phone</span></span></p>
<p><span data-ttu-id="b4419-525">IP-телефон HP 4110 (телефон общего пользования)</span><span class="sxs-lookup"><span data-stu-id="b4419-525">HP 4110 IP Phone (common area phone)</span></span></p>
<p><span data-ttu-id="b4419-526">IP-телефон HP 4120 (стационарный телефон)</span><span class="sxs-lookup"><span data-stu-id="b4419-526">HP 4120 IP Phone (desk phone)</span></span></p>
<p><span data-ttu-id="b4419-527">IP-телефон общего доступа Polycom CX500</span><span class="sxs-lookup"><span data-stu-id="b4419-527">Polycom CX500 IP common area phone</span></span></p>
<p><span data-ttu-id="b4419-528">Стационарный IP-телефон Polycom CX600</span><span class="sxs-lookup"><span data-stu-id="b4419-528">Polycom CX600 IP desk phone</span></span></p>
<p><span data-ttu-id="b4419-529">Стационарный IP-телефон Polycom CX700</span><span class="sxs-lookup"><span data-stu-id="b4419-529">Polycom CX700 IP desk phone</span></span></p>
<p><span data-ttu-id="b4419-530">Телефон для IP-конференций Polycom CX3000</span><span class="sxs-lookup"><span data-stu-id="b4419-530">Polycom CX3000 IP conference phone</span></span></p></td>
<td><p><span data-ttu-id="b4419-531">67/68</span><span class="sxs-lookup"><span data-stu-id="b4419-531">67/68</span></span></p></td>
<td><p><span data-ttu-id="b4419-532">DHCP</span><span class="sxs-lookup"><span data-stu-id="b4419-532">DHCP</span></span></p></td>
<td><p><span data-ttu-id="b4419-533">Используется в списке устройств для поиска сертификата сервера Lync, подготовки полного доменного имени и полного доменного имени регистратора.</span><span class="sxs-lookup"><span data-stu-id="b4419-533">Used by the listed devices to find the Lync Server certificate, provisioning FQDN, and Registrar FQDN.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b4419-534">**\*** Чтобы настроить определенные порты для этих типов мультимедиа, используйте командлет CsConferencingConfiguration (ClientMediaPortRangeEnabled, ClientMediaPort и ClientMediaPortRange).</span><span class="sxs-lookup"><span data-stu-id="b4419-534">**\*** To configure specific ports for these media types, use the CsConferencingConfiguration cmdlet (ClientMediaPortRangeEnabled, ClientMediaPort, and ClientMediaPortRange parameters).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="b4419-535">Программа Set для клиентов Lync автоматически создает необходимые исключения брандмауэра операционной системы на клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="b4419-535">The set programs for Lync clients automatically create the required operating-system firewall exceptions on the client computer.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="b4419-536">Порты, используемые для внешнего доступа пользователей, необходимы для любого сценария, в котором клиент должен пройти межсетевой экран Организации (например, любые внешние коммуникации или собрания, размещенные в других организациях).</span><span class="sxs-lookup"><span data-stu-id="b4419-536">The ports that are used for external user access are required for any scenario in which the client must traverse the organization’s firewall (for example, any external communications or meetings hosted by other organizations).</span></span>



<span data-ttu-id="b4419-537"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b4419-537"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

