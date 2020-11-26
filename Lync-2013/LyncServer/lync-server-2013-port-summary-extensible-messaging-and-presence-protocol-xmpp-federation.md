---
title: Сводка по порту — расширяемая Федерация протоколов обмена сообщениями и присутствия (XMPP)
description: Сводка по порту — расширяемая Федерация протоколов обмена сообщениями и присутствия (XMPP).
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary -  Extensible messaging and presence protocol (XMPP) federation
ms:assetid: 62e98fab-7add-4983-a3fa-dbe74e1c3849
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ618371(v=OCS.15)
ms:contentKeyID: 49105658
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9508bc8b9fbcca6fb6a37478def258a9fa52c373
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442805"
---
# <a name="port-summary---extensible-messaging-and-presence-protocol-xmpp-federation-in-lync-server-2013"></a><span data-ttu-id="2ca64-103">Сводка по порту — расширяемая Федерация протоколов обмена сообщениями и присутствия (XMPP) в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2ca64-103">Port summary - Extensible messaging and presence protocol (XMPP) federation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2ca64-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2ca64-104">

<span> </span></span></span>

<span data-ttu-id="2ca64-105">_**Тема последнего изменения:** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="2ca64-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="2ca64-106">Порты и протоколы, определенные для прокси-сервера расширяемых сообщений и протоколов XMPP, развернутых на пограничном сервере, разрешают обмен данными между сервером пограничного сервера XMPP и допускает передачу данных с пограничного сервера на сервер федеративного партнера XMPP.</span><span class="sxs-lookup"><span data-stu-id="2ca64-106">The ports and protocols defined for the extensible messaging and presence protocol (XMPP) proxy deployed on the Edge Server allow communications from the XMPP federated partner to the Edge Server, and also allows communication from your Edge Server to the XMPP federated partner.</span></span> <span data-ttu-id="2ca64-107">Правило также определяется во внутреннем брандмауэре, доступном на сервере переднего плана или на пограничном пуле, к внешнему и внешнему интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="2ca64-107">A rule is also defined on the internal-facing firewall from the Front End Server or Front End pool to the Edge Server or Edge pool.</span></span>

<div>

## <a name="firewall-summary-for-extensible-messaging-and-presence-protocol"></a><span data-ttu-id="2ca64-108">Сводка брандмауэра по протоколу расширенного обмена сообщениями и присутствия</span><span class="sxs-lookup"><span data-stu-id="2ca64-108">Firewall Summary for Extensible Messaging and Presence Protocol</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2ca64-109">Протокол/TCP или UDP/порт</span><span class="sxs-lookup"><span data-stu-id="2ca64-109">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="2ca64-110">Источник (IP-адрес)</span><span class="sxs-lookup"><span data-stu-id="2ca64-110">Source (IP address)</span></span></th>
<th><span data-ttu-id="2ca64-111">Назначение (IP-адрес)</span><span class="sxs-lookup"><span data-stu-id="2ca64-111">Destination (IP address)</span></span></th>
<th><span data-ttu-id="2ca64-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2ca64-112">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2ca64-113">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="2ca64-113">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="2ca64-114">Любой</span><span class="sxs-lookup"><span data-stu-id="2ca64-114">Any</span></span></p></td>
<td><p><span data-ttu-id="2ca64-115">IP-адрес интерфейса службы Edge Access</span><span class="sxs-lookup"><span data-stu-id="2ca64-115">Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="2ca64-116">Стандартный коммуникационный порт "сервер-сервер" для XMPP.</span><span class="sxs-lookup"><span data-stu-id="2ca64-116">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="2ca64-117">Разрешает связь с прокси-сервером пограничного сервера XMPP от федеративных XMPP партнеров</span><span class="sxs-lookup"><span data-stu-id="2ca64-117">Allows communication to the Edge Server XMPP proxy from federated XMPP partners</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2ca64-118">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="2ca64-118">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="2ca64-119">IP-адрес интерфейса службы Edge Access</span><span class="sxs-lookup"><span data-stu-id="2ca64-119">Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="2ca64-120">Любой</span><span class="sxs-lookup"><span data-stu-id="2ca64-120">Any</span></span></p></td>
<td><p><span data-ttu-id="2ca64-121">Стандартный коммуникационный порт "сервер-сервер" для XMPP.</span><span class="sxs-lookup"><span data-stu-id="2ca64-121">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="2ca64-122">Разрешает взаимодействие с XMPP прокси-сервером для федеративных XMPP партнеров</span><span class="sxs-lookup"><span data-stu-id="2ca64-122">Allows communication from the Edge Server XMPP proxy to federated XMPP partners</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2ca64-123">XMPP/MTLS/23456</span><span class="sxs-lookup"><span data-stu-id="2ca64-123">XMPP/MTLS/23456</span></span></p></td>
<td><p><span data-ttu-id="2ca64-124">Любой</span><span class="sxs-lookup"><span data-stu-id="2ca64-124">Any</span></span></p></td>
<td><p><span data-ttu-id="2ca64-125">IP-адрес внутреннего интерфейса пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="2ca64-125">Internal Edge Server Interface IP</span></span></p></td>
<td><p><span data-ttu-id="2ca64-126">Внутренний XMPP трафик из шлюза XMPP на сервере переднего плана или в пуле переднего плана на пограничный сервер</span><span class="sxs-lookup"><span data-stu-id="2ca64-126">Internal XMPP traffic from the XMPP Gateway on the Front End Server or Front End pool to the Edge Server</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a><span data-ttu-id="2ca64-127">См. также</span><span class="sxs-lookup"><span data-stu-id="2ca64-127">See Also</span></span>


[<span data-ttu-id="2ca64-128">Пример конфигурации XMPP в Lync Server 2013 — федерация XMPP с Google Talk</span><span class="sxs-lookup"><span data-stu-id="2ca64-128">Example XMPP configuration in Lync Server 2013 – XMPP federation with Google Talk</span></span>](lync-server-2013-example-xmpp-configuration-–-xmpp-federation-with-google-talk.md)  


[<span data-ttu-id="2ca64-129">Управление федеративными XMPP-партнерами в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2ca64-129">Manage XMPP federated partners in Lync Server 2013</span></span>](lync-server-2013-manage-xmpp-federated-partners-for-your-organization.md)  
  

<span data-ttu-id="2ca64-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2ca64-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

