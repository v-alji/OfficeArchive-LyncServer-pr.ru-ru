---
title: 'Lync Server 2013: Общие сведения о портах — общедоступная служба обмена мгновенными сообщениями'
description: 'Lync Server 2013: Общие сведения о портах — общедоступная служба обмена мгновенными сообщениями.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - Public instant messaging connectivity
ms:assetid: f46756ec-1401-4ca2-a4a4-5cd28bcfdc7f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ618376(v=OCS.15)
ms:contentKeyID: 49105663
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4137b5f92e043dc15dc9aa1f0b9593b4d9f7c2ca
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424277"
---
# <a name="port-summary---public-instant-messaging-connectivity-in-lync-server-2013"></a><span data-ttu-id="03e69-103">Общие сведения о портах — общедоступная служба обмена мгновенными сообщениями в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="03e69-103">Port summary - Public instant messaging connectivity in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="03e69-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="03e69-104">

<span> </span></span></span>

<span data-ttu-id="03e69-105">_**Тема последнего изменения:** 2013-02-16_</span><span class="sxs-lookup"><span data-stu-id="03e69-105">_**Topic Last Modified:** 2013-02-16_</span></span>

<span data-ttu-id="03e69-106">Чтобы настроить брандмауэр для порта и протоколов, необходимых для поддержки общедоступной службы обмена мгновенными сообщениями, сначала обратите внимание на то, что SIP/MTLS/TCP 5061 является двунаправленным, чтобы иметь возможность контактам в общедоступном поставщике обмена мгновенными сообщениями с контактами для связи с клиентами Lync или Lync для общения с</span><span class="sxs-lookup"><span data-stu-id="03e69-106">To configure your firewall for ports and protocols necessary to support public instant messaging connectivity, first note that SIP/MTLS/TCP 5061 is bidirectional to account for the ability of contacts in the public IM provider to contact Lync clients, or for Lync to contact public IM contacts.</span></span>

<span data-ttu-id="03e69-107">Windows Live Messenger может принимать участие в голосовой и видеосвязи с клиентами Lync.</span><span class="sxs-lookup"><span data-stu-id="03e69-107">Windows Live Messenger can participate in audio/video communications with Lync clients.</span></span> <span data-ttu-id="03e69-108">Эти учетные записи похожи на настройки порта и протокола брандмауэра, которые обычно используются в брандмауэре для поддержки клиентов Lync в качестве внешних пользователей.</span><span class="sxs-lookup"><span data-stu-id="03e69-108">This accounts for the very similar firewall port and protocol configuration that you would typically have on the firewall to support Lync clients as external users.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="03e69-109">В некоторых случаях Lync — это мощный инструмент для связи между организациями и людьми по всему миру.</span><span class="sxs-lookup"><span data-stu-id="03e69-109">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="03e69-110">Для интеграции с Windows Live Messenger не требуется дополнительных лицензий на пользователей и устройств, Кроме стандартной клиентской лицензии Lync (CAL).</span><span class="sxs-lookup"><span data-stu-id="03e69-110">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard Client Access License (CAL).</span></span> <span data-ttu-id="03e69-111">В этот список будет добавлена Федерация Skype, благодаря чему пользователи Lync смогут общаться с сотнями миллионов людей с помощью обмена мгновенными сообщениями и голосовой связью.</span><span class="sxs-lookup"><span data-stu-id="03e69-111">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people with IM and voice.</span></span><BR><span data-ttu-id="03e69-112">Интеграция с контактами клиентов Messenger официально заканчивается 15 марта 2013, за исключением mainland Китая.</span><span class="sxs-lookup"><span data-stu-id="03e69-112">Federation with Messenger client contacts will officially end on March 15, 2013, except for mainland China.</span></span> <span data-ttu-id="03e69-113">Skype станет клиентом Федерации федеративных пользователей, которые ранее использовали Messenger.</span><span class="sxs-lookup"><span data-stu-id="03e69-113">Skype will become the federation client for federated users who previously used Messenger.</span></span>



</div>

<div>

## <a name="firewall-summary--public-instant-messaging-connectivity"></a><span data-ttu-id="03e69-114">Сводка по брандмауэрам: общедоступная служба обмена мгновенными сообщениями</span><span class="sxs-lookup"><span data-stu-id="03e69-114">Firewall Summary – Public Instant Messaging Connectivity</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="03e69-115">Role/Protocol/TCP/UDP/порт</span><span class="sxs-lookup"><span data-stu-id="03e69-115">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="03e69-116">IP-адрес источника</span><span class="sxs-lookup"><span data-stu-id="03e69-116">Source IP address</span></span></th>
<th><span data-ttu-id="03e69-117">IP-адрес назначения</span><span class="sxs-lookup"><span data-stu-id="03e69-117">Destination IP address</span></span></th>
<th><span data-ttu-id="03e69-118">Примечания.</span><span class="sxs-lookup"><span data-stu-id="03e69-118">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="03e69-119">Access/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="03e69-119">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="03e69-120">Партнеры по подключению общедоступных мгновенных сообщений</span><span class="sxs-lookup"><span data-stu-id="03e69-120">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="03e69-121">Интерфейс доступа пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="03e69-121">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="03e69-122">Для Федеративной и общедоступной службы обмена мгновенными сообщениями, использующих SIP.</span><span class="sxs-lookup"><span data-stu-id="03e69-122">For federated and public IM connectivity that use SIP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03e69-123">Access/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="03e69-123">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="03e69-124">Интерфейс доступа пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="03e69-124">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="03e69-125">Партнеры по подключению общедоступных мгновенных сообщений</span><span class="sxs-lookup"><span data-stu-id="03e69-125">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="03e69-126">Для Федеративной и общедоступной службы обмена мгновенными сообщениями, использующих SIP.</span><span class="sxs-lookup"><span data-stu-id="03e69-126">For federated and public IM connectivity that use SIP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03e69-127">Access/SIP (TLS)/TCP/443</span><span class="sxs-lookup"><span data-stu-id="03e69-127">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="03e69-128">Клиенты</span><span class="sxs-lookup"><span data-stu-id="03e69-128">Clients</span></span></p></td>
<td><p><span data-ttu-id="03e69-129">Интерфейс доступа пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="03e69-129">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="03e69-130">Трафик SIP от клиента к серверу для доступа внешних пользователей.</span><span class="sxs-lookup"><span data-stu-id="03e69-130">Client-to-server SIP traffic for external user access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03e69-131">A/V/RTP/TCP/50000-59,999</span><span class="sxs-lookup"><span data-stu-id="03e69-131">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="03e69-132">Интерфейс доступа пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="03e69-132">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="03e69-133">Клиенты Live Messenger</span><span class="sxs-lookup"><span data-stu-id="03e69-133">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="03e69-134">Используется для сеансов обмена мгновенными сообщениями с помощью Windows Live Messenger, если настроена служба общего доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="03e69-134">Used for A/V sessions with Windows Live Messenger if public IM connectivity is configured.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03e69-135">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="03e69-135">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="03e69-136">Интерфейс доступа пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="03e69-136">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="03e69-137">Клиенты Live Messenger</span><span class="sxs-lookup"><span data-stu-id="03e69-137">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="03e69-138">Требуется для общедоступной службы обмена мгновенными сообщениями с Windows Live Messenger.</span><span class="sxs-lookup"><span data-stu-id="03e69-138">Required for public IM connectivity with Windows Live Messenger.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03e69-139">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="03e69-139">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="03e69-140">Клиенты Live Messenger</span><span class="sxs-lookup"><span data-stu-id="03e69-140">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="03e69-141">Интерфейс доступа пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="03e69-141">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="03e69-142">Требуется для общедоступной службы обмена мгновенными сообщениями с Windows Live Messenger.</span><span class="sxs-lookup"><span data-stu-id="03e69-142">Required for public IM connectivity with Windows Live Messenger.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a><span data-ttu-id="03e69-143">См. также</span><span class="sxs-lookup"><span data-stu-id="03e69-143">See Also</span></span>


[<span data-ttu-id="03e69-144">Сценарии доступа внешних пользователей в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="03e69-144">Scenarios for external user access in Lync Server 2013</span></span>](lync-server-2013-scenarios-for-external-user-access.md)  
[<span data-ttu-id="03e69-145">Определение требований к внешнему брандмауэру аудио- и видеосвязи и портам для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="03e69-145">Determine external A/V firewall and port requirements for Lync Server 2013</span></span>](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md)  
  

<span data-ttu-id="03e69-146"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="03e69-146"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

