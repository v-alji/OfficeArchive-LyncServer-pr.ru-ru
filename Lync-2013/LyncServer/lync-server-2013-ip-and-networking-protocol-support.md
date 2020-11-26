---
title: 'Lync Server 2013: поддержка IP и сетевого протокола'
description: 'Lync Server 2013: поддержка IP и сетевых протоколов.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: IP and networking protocol support
ms:assetid: b0cffb10-3478-445c-89c7-8cb8b5027424
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412848(v=OCS.15)
ms:contentKeyID: 48185128
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dbd8022dd7197524334e0c70ea0ad875a30446de
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426748"
---
# <a name="ip-and-networking-protocol-support-in-lync-server-2013"></a><span data-ttu-id="00119-103">Поддержка IP и сетевого протокола в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="00119-103">IP and networking protocol support in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="00119-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="00119-104">

<span> </span></span></span>

<span data-ttu-id="00119-105">_**Тема последнего изменения:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="00119-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="00119-106">Lync Server 2013 поддерживает следующие протоколы IP и сети:</span><span class="sxs-lookup"><span data-stu-id="00119-106">Lync Server 2013 supports the following IP and networking protocols:</span></span>

  - <span data-ttu-id="00119-107">**IP-протоколы.**</span><span class="sxs-lookup"><span data-stu-id="00119-107">**IP Protocols.**</span></span>   <span data-ttu-id="00119-108">Lync Server 2013 поддерживает IP-версии 4 (IPv4) или IP версии 6 (IPv6) для серверной сети.</span><span class="sxs-lookup"><span data-stu-id="00119-108">Lync Server 2013 supports either IP version 4 (IPv4) or IP version 6 (IPv6) for the server network.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="00119-109">Lync Server 2013 может работать в сети с поддержкой двух стеков IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="00119-109">Lync Server 2013 can function in a network with dual IP stack enabled.</span></span>

    
    </div>

  - <span data-ttu-id="00119-110">**Транспортные протоколы SIP.**</span><span class="sxs-lookup"><span data-stu-id="00119-110">**SIP Transport Protocols.**</span></span>   <span data-ttu-id="00119-111">В общем случае SIP может использовать по крайней мере три типа транспорта: протокол UDP и протокол управления передачей (TCP), а также TLS-защиту.</span><span class="sxs-lookup"><span data-stu-id="00119-111">Generically, SIP can use at least three transport types: User Datagram Protocol (UDP), Transmission Control Protocol (TCP), and Transport Layer Security (TLS).</span></span> <span data-ttu-id="00119-112">В конфигурации транспорта SIP по умолчанию TLS выполняется по протоколу TCP.</span><span class="sxs-lookup"><span data-stu-id="00119-112">In the default SIP transport configuration, TLS runs over TCP.</span></span> <span data-ttu-id="00119-113">Протокол TLS используется в сети Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="00119-113">TLS is used within the Lync Server 2013 network.</span></span> <span data-ttu-id="00119-114">На краю сети Lync Server 2013 может взаимодействовать по протоколу TCP.</span><span class="sxs-lookup"><span data-stu-id="00119-114">At the edge of the network, Lync Server 2013 can interoperate over TCP.</span></span> <span data-ttu-id="00119-115">Lync Server 2013 не поддерживает транспортный протокол UDP для SIP, так как он не соответствует минимальным стандартам безопасности, надежности и масштабируемости для корпоративной связи.</span><span class="sxs-lookup"><span data-stu-id="00119-115">Lync Server 2013 does not support UDP for SIP transport because it doesn’t meet the minimum standards for enterprise communications security, reliability, and scalability.</span></span> <span data-ttu-id="00119-116">Подробные сведения можно найти в статье блога для NextHop: "для UDP, а не в UDP, вопрос которой —" по адресу " [https://go.microsoft.com/fwlink/p/?linkId=185369](https://go.microsoft.com/fwlink/p/?linkid=185369) .</span><span class="sxs-lookup"><span data-stu-id="00119-116">For details, see the NextHop blog article, "To UDP, or not to UDP, that is the question," at [https://go.microsoft.com/fwlink/p/?linkId=185369](https://go.microsoft.com/fwlink/p/?linkid=185369).</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="00119-117">Содержимое всех блогов и их URL-адреса могут быть изменены без уведомления.</span><span class="sxs-lookup"><span data-stu-id="00119-117">The content of each blog and its URL are subject to change without notice.</span></span>

    
    <span data-ttu-id="00119-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="00119-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

