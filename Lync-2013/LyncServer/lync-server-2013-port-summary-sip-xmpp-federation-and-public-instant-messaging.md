---
title: 'Общие сведения о портах: SIP, Федерация XMPP и общедоступная служба обмена мгновенными сообщениями'
description: 'Общие сведения о портах: SIP, Федерация XMPP и общедоступная служба обмена мгновенными сообщениями.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - SIP, XMPP federation, and public instant messaging
ms:assetid: ab05bdd6-e9b0-4b1b-9dd9-29ab88e8befe
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ618373(v=OCS.15)
ms:contentKeyID: 49105660
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7c58dbf7bdd56b4678d56f96a11332219bb40c17
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398173"
---
# <a name="port-summary---sip-xmpp-federation-and-public-instant-messaging-in-lync-server-2013"></a><span data-ttu-id="308c1-103">Общие сведения о портах: SIP, Федерация XMPP и общедоступная служба обмена мгновенными сообщениями в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="308c1-103">Port summary - SIP, XMPP federation, and public instant messaging in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="308c1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="308c1-104">

<span> </span></span></span>

<span data-ttu-id="308c1-105">_**Тема последнего изменения:** 2013-03-15_</span><span class="sxs-lookup"><span data-stu-id="308c1-105">_**Topic Last Modified:** 2013-03-15_</span></span>

<span data-ttu-id="308c1-106">Требования к портам, протоколам и брандмауэрам для Федерации с Microsoft Lync Server 2013, Lync Server 2010 и Office Communications Server похожи на развернутый пограничный сервер.</span><span class="sxs-lookup"><span data-stu-id="308c1-106">Port, protocol and firewall requirements for federation with Microsoft Lync Server 2013, Lync Server 2010 and Office Communications Server are similar to those for the deployed Edge Server.</span></span> <span data-ttu-id="308c1-107">Клиенты инициируют связь с службой Edge Access через TLS/SIP/TCP 443.</span><span class="sxs-lookup"><span data-stu-id="308c1-107">Clients initiate communication with the Access Edge service over TLS/SIP/TCP 443.</span></span> <span data-ttu-id="308c1-108">Федеративные партнеры тем не менее, будут инициировать связь с службой Edge Access через MTLS/SIP/TCP 5061.</span><span class="sxs-lookup"><span data-stu-id="308c1-108">Federated partners however, will initiate communications to the Access Edge service over MTLS/SIP/TCP 5061.</span></span>

<span data-ttu-id="308c1-109">Чтобы настроить брандмауэр для порта и протоколов, необходимых для поддержки общедоступной службы обмена мгновенными сообщениями, сначала обратите внимание на то, что SIP/MTLS/TCP 5061 является двунаправленным, чтобы иметь возможность контактам в общедоступном поставщике обмена мгновенными сообщениями с контактами для связи с клиентами Lync или Lync для общения с</span><span class="sxs-lookup"><span data-stu-id="308c1-109">To configure your firewall for ports and protocols necessary to support public instant messaging connectivity, first note that SIP/MTLS/TCP 5061 is bidirectional to account for the ability of contacts in the public IM provider to contact Lync clients, or for Lync to contact public IM contacts.</span></span>

<span data-ttu-id="308c1-110">Windows Live Messenger может принимать участие в голосовой и видеосвязи с клиентами Lync.</span><span class="sxs-lookup"><span data-stu-id="308c1-110">Windows Live Messenger can participate in audio/video communications with Lync clients.</span></span> <span data-ttu-id="308c1-111">Эти учетные записи похожи на настройки порта и протокола брандмауэра, которые обычно используются в брандмауэре для поддержки клиентов Lync в качестве внешних пользователей.</span><span class="sxs-lookup"><span data-stu-id="308c1-111">This accounts for the very similar firewall port and protocol configuration that you would typically have on the firewall to support Lync clients as external users.</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="308c1-112">В некоторых случаях Lync — это мощный инструмент для связи между организациями и людьми по всему миру.</span><span class="sxs-lookup"><span data-stu-id="308c1-112">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="308c1-113">Для интеграции с Windows Live Messenger не требуется дополнительных лицензий на пользователей и устройств, Кроме стандартной клиентской лицензии Lync (CAL).</span><span class="sxs-lookup"><span data-stu-id="308c1-113">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard Client Access License (CAL).</span></span> <span data-ttu-id="308c1-114">В этот список будет добавлена Федерация Skype, благодаря чему пользователи Lync смогут общаться с сотнями миллионов людей с помощью обмена мгновенными сообщениями и голосовой связью.</span><span class="sxs-lookup"><span data-stu-id="308c1-114">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people with IM and voice.</span></span><BR><span data-ttu-id="308c1-115">Интеграция с контактами клиентов Messenger официально заканчивается 15 марта 2013, за исключением mainland Китая.</span><span class="sxs-lookup"><span data-stu-id="308c1-115">Federation with Messenger client contacts will officially end on March 15, 2013, except for mainland China.</span></span> <span data-ttu-id="308c1-116">Skype станет клиентом Федерации федеративных пользователей, которые ранее использовали Messenger.</span><span class="sxs-lookup"><span data-stu-id="308c1-116">Skype will become the federation client for federated users who previously used Messenger.</span></span>



</div>

<span data-ttu-id="308c1-117">Порты и протоколы, определенные для прокси-сервера расширяемых сообщений и протоколов XMPP, развернутых на пограничном сервере, разрешают обмен данными между сервером пограничного сервера XMPP и допускает передачу данных с пограничного сервера на сервер федеративного партнера XMPP.</span><span class="sxs-lookup"><span data-stu-id="308c1-117">The ports and protocols defined for the extensible messaging and presence protocol (XMPP) proxy deployed on the Edge Server allow communications from the XMPP federated partner to the Edge Server, and also allows communication from your Edge Server to the XMPP federated partner.</span></span> <span data-ttu-id="308c1-118">Правило также определяется во внутреннем брандмауэре, доступном на сервере переднего плана или на пограничном пуле, к внешнему и внешнему интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="308c1-118">A rule is also defined on the internal-facing firewall from the Front End Server or Front End pool to the Edge Server or Edge pool.</span></span>

<div>

## <a name="firewall-summary---sip-federation"></a><span data-ttu-id="308c1-119">Сводка по межсетевому экрану — Федерация SIP</span><span class="sxs-lookup"><span data-stu-id="308c1-119">Firewall Summary - SIP Federation</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="308c1-120">Role/Protocol/TCP/UDP/порт</span><span class="sxs-lookup"><span data-stu-id="308c1-120">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="308c1-121">IP-адрес источника</span><span class="sxs-lookup"><span data-stu-id="308c1-121">Source IP address</span></span></th>
<th><span data-ttu-id="308c1-122">IP-адрес назначения</span><span class="sxs-lookup"><span data-stu-id="308c1-122">Destination IP address</span></span></th>
<th><span data-ttu-id="308c1-123">Примечания.</span><span class="sxs-lookup"><span data-stu-id="308c1-123">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="308c1-124">Access/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="308c1-124">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="308c1-125">Общедоступный IP-адрес службы пограничного доступа</span><span class="sxs-lookup"><span data-stu-id="308c1-125">Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="308c1-126">Любой</span><span class="sxs-lookup"><span data-stu-id="308c1-126">Any</span></span></p></td>
<td><p><span data-ttu-id="308c1-127">Для Федеративной и общедоступной службы обмена мгновенными сообщениями с помощью SIP</span><span class="sxs-lookup"><span data-stu-id="308c1-127">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary--public-instant-messaging-connectivity"></a><span data-ttu-id="308c1-128">Сводка по брандмауэрам: общедоступная служба обмена мгновенными сообщениями</span><span class="sxs-lookup"><span data-stu-id="308c1-128">Firewall Summary – Public Instant Messaging Connectivity</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="308c1-129">Role/Protocol/TCP/UDP/порт</span><span class="sxs-lookup"><span data-stu-id="308c1-129">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="308c1-130">IP-адрес источника</span><span class="sxs-lookup"><span data-stu-id="308c1-130">Source IP address</span></span></th>
<th><span data-ttu-id="308c1-131">IP-адрес назначения</span><span class="sxs-lookup"><span data-stu-id="308c1-131">Destination IP address</span></span></th>
<th><span data-ttu-id="308c1-132">Примечания.</span><span class="sxs-lookup"><span data-stu-id="308c1-132">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="308c1-133">Access/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="308c1-133">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="308c1-134">Партнеры по подключению общедоступных мгновенных сообщений</span><span class="sxs-lookup"><span data-stu-id="308c1-134">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="308c1-135">Интерфейс доступа пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="308c1-135">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="308c1-136">Для Федеративной и общедоступной службы обмена мгновенными сообщениями, использующих SIP.</span><span class="sxs-lookup"><span data-stu-id="308c1-136">For federated and public IM connectivity that use SIP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="308c1-137">Access/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="308c1-137">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="308c1-138">Интерфейс доступа пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="308c1-138">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="308c1-139">Партнеры по подключению общедоступных мгновенных сообщений</span><span class="sxs-lookup"><span data-stu-id="308c1-139">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="308c1-140">Для Федеративной и общедоступной службы обмена мгновенными сообщениями, использующих SIP.</span><span class="sxs-lookup"><span data-stu-id="308c1-140">For federated and public IM connectivity that use SIP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="308c1-141">Access/SIP (TLS)/TCP/443</span><span class="sxs-lookup"><span data-stu-id="308c1-141">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="308c1-142">Клиенты</span><span class="sxs-lookup"><span data-stu-id="308c1-142">Clients</span></span></p></td>
<td><p><span data-ttu-id="308c1-143">Интерфейс доступа пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="308c1-143">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="308c1-144">Трафик SIP от клиента к серверу для доступа внешних пользователей.</span><span class="sxs-lookup"><span data-stu-id="308c1-144">Client-to-server SIP traffic for external user access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="308c1-145">A/V/RTP/TCP/50000-59,999</span><span class="sxs-lookup"><span data-stu-id="308c1-145">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="308c1-146">Интерфейс доступа пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="308c1-146">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="308c1-147">Клиенты Live Messenger</span><span class="sxs-lookup"><span data-stu-id="308c1-147">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="308c1-148">Используется для сеансов обмена мгновенными сообщениями с помощью Windows Live Messenger, если настроена служба общего доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="308c1-148">Used for A/V sessions with Windows Live Messenger if public IM connectivity is configured.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="308c1-149">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="308c1-149">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="308c1-150">Интерфейс доступа пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="308c1-150">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="308c1-151">Клиенты Live Messenger</span><span class="sxs-lookup"><span data-stu-id="308c1-151">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="308c1-152">Требуется для общедоступной службы обмена мгновенными сообщениями с Windows Live Messenger.</span><span class="sxs-lookup"><span data-stu-id="308c1-152">Required for public IM connectivity with Windows Live Messenger.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="308c1-153">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="308c1-153">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="308c1-154">Клиенты Live Messenger</span><span class="sxs-lookup"><span data-stu-id="308c1-154">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="308c1-155">Интерфейс доступа пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="308c1-155">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="308c1-156">Требуется для общедоступной службы обмена мгновенными сообщениями с Windows Live Messenger.</span><span class="sxs-lookup"><span data-stu-id="308c1-156">Required for public IM connectivity with Windows Live Messenger.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary---extensible-messaging-and-presence-protocol-xmpp"></a><span data-ttu-id="308c1-157">Сводка по межсетевому экрану — расширяемый протокол для обмена сообщениями и присутствия (XMPP)</span><span class="sxs-lookup"><span data-stu-id="308c1-157">Firewall Summary - Extensible Messaging and Presence Protocol (XMPP)</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="308c1-158">Протокол/TCP или UDP/порт</span><span class="sxs-lookup"><span data-stu-id="308c1-158">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="308c1-159">Источник (IP-адрес)</span><span class="sxs-lookup"><span data-stu-id="308c1-159">Source (IP address)</span></span></th>
<th><span data-ttu-id="308c1-160">Назначение (IP-адрес)</span><span class="sxs-lookup"><span data-stu-id="308c1-160">Destination (IP address)</span></span></th>
<th><span data-ttu-id="308c1-161">Комментарии</span><span class="sxs-lookup"><span data-stu-id="308c1-161">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="308c1-162">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="308c1-162">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="308c1-163">Любой</span><span class="sxs-lookup"><span data-stu-id="308c1-163">Any</span></span></p></td>
<td><p><span data-ttu-id="308c1-164">IP-адрес интерфейса службы Edge Access</span><span class="sxs-lookup"><span data-stu-id="308c1-164">Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="308c1-165">Стандартный коммуникационный порт "сервер-сервер" для XMPP.</span><span class="sxs-lookup"><span data-stu-id="308c1-165">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="308c1-166">Разрешает связь с прокси-сервером пограничного сервера XMPP от федеративных XMPP партнеров</span><span class="sxs-lookup"><span data-stu-id="308c1-166">Allows communication to the Edge Server XMPP proxy from federated XMPP partners</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="308c1-167">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="308c1-167">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="308c1-168">IP-адрес интерфейса службы Edge Access</span><span class="sxs-lookup"><span data-stu-id="308c1-168">Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="308c1-169">Любой</span><span class="sxs-lookup"><span data-stu-id="308c1-169">Any</span></span></p></td>
<td><p><span data-ttu-id="308c1-170">Стандартный коммуникационный порт "сервер-сервер" для XMPP.</span><span class="sxs-lookup"><span data-stu-id="308c1-170">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="308c1-171">Разрешает взаимодействие с XMPP прокси-сервером для федеративных XMPP партнеров</span><span class="sxs-lookup"><span data-stu-id="308c1-171">Allows communication from the Edge Server XMPP proxy to federated XMPP partners</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="308c1-172">XMPP/MTLS/23456</span><span class="sxs-lookup"><span data-stu-id="308c1-172">XMPP/MTLS/23456</span></span></p></td>
<td><p><span data-ttu-id="308c1-173">Любой</span><span class="sxs-lookup"><span data-stu-id="308c1-173">Any</span></span></p></td>
<td><p><span data-ttu-id="308c1-174">IP-адрес внутреннего интерфейса пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="308c1-174">Internal Edge Server Interface IP</span></span></p></td>
<td><p><span data-ttu-id="308c1-175">Внутренний XMPP трафик из шлюза XMPP на сервере переднего плана или в пуле переднего плана на пограничный сервер</span><span class="sxs-lookup"><span data-stu-id="308c1-175">Internal XMPP traffic from the XMPP Gateway on the Front End Server or Front End pool to the Edge Server</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a><span data-ttu-id="308c1-176">См. также</span><span class="sxs-lookup"><span data-stu-id="308c1-176">See Also</span></span>


[<span data-ttu-id="308c1-177">Сценарии доступа внешних пользователей в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="308c1-177">Scenarios for external user access in Lync Server 2013</span></span>](lync-server-2013-scenarios-for-external-user-access.md)  
[<span data-ttu-id="308c1-178">Определение требований к внешнему брандмауэру аудио- и видеосвязи и портам для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="308c1-178">Determine external A/V firewall and port requirements for Lync Server 2013</span></span>](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md)  


[<span data-ttu-id="308c1-179">Управление федеративными XMPP-партнерами в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="308c1-179">Manage XMPP federated partners in Lync Server 2013</span></span>](lync-server-2013-manage-xmpp-federated-partners-for-your-organization.md)  
  

<span data-ttu-id="308c1-180"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="308c1-180"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

