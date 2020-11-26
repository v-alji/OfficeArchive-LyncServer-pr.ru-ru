---
title: Совместимость Lync Server 2013 с устойчивостью главного сайта Lync Server 2010
description: Совместимость с Lync Server 2013 с помощью устойчивости сайта Lync Server 2010 для одногородной связи.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Lync Server 2010 metropolitan site resiliency
ms:assetid: 18673ff6-b664-4a57-a89b-cbda8b129e6a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204715(v=OCS.15)
ms:contentKeyID: 48183526
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ec72f261ac593b24bad13dcd400f495ba7ba0722
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434608"
---
# <a name="lync-server-2010-metropolitan-site-resiliency"></a><span data-ttu-id="c20c7-103">Устойчивость главного сайта Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="c20c7-103">Lync Server 2010 metropolitan site resiliency</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c20c7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c20c7-104">

<span> </span></span></span>

<span data-ttu-id="c20c7-105">_**Тема последнего изменения:** 2014-03-19_</span><span class="sxs-lookup"><span data-stu-id="c20c7-105">_**Topic Last Modified:** 2014-03-19_</span></span>

<span data-ttu-id="c20c7-106">Решение для обеспечения устойчивости сайтов, поддерживающее для Lync Server 2010, не поддерживается для Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c20c7-106">The metropolitan site resiliency solution supported for Lync Server 2010 is not supported for Lync Server 2013.</span></span> <span data-ttu-id="c20c7-107">Это решение вовлечено в объединение одного пула переднего плана в двух центрах обработки данных в одном регионе города.</span><span class="sxs-lookup"><span data-stu-id="c20c7-107">This solution involved spanning a single Front End pool across two data centers in the same metropolitan area.</span></span>

<span data-ttu-id="c20c7-108">Решение для обеспечения устойчивости сайтов с помощью этого типа разработано для восстановления после утраты полного центра обработки данных.</span><span class="sxs-lookup"><span data-stu-id="c20c7-108">The metropolitan site resiliency solution was designed to recover from the loss of a full datacenter.</span></span> <span data-ttu-id="c20c7-109">При охвате пула в двух центрах обработки данных обычно размещается половина переднего плана в одном центре обработки данных и вторая половина во втором центре обработки данных.</span><span class="sxs-lookup"><span data-stu-id="c20c7-109">When you span your pool across two datacenters, you typically put half of your front ends in one datacenter and the other half in the second datacenter.</span></span> <span data-ttu-id="c20c7-110">Если вы потеряли весь центр обработки данных, вы потеряли половину серверов переднего плана.</span><span class="sxs-lookup"><span data-stu-id="c20c7-110">If you lose an entire datacenter, you have lost half of your Front End Servers.</span></span> <span data-ttu-id="c20c7-111">Это может привести к возникновению проблем с новой моделью распределенной системы для пулов интерфейсов в Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c20c7-111">This can cause issues with the new distributed system model for Front End Pools in Lync Server 2013.</span></span> <span data-ttu-id="c20c7-112">Дополнительные сведения можно найти [в разделе топологии и компоненты для серверов переднего плана, обмена мгновенными сообщениями и присутствия в Lync Server 2013](lync-server-2013-topologies-and-components-for-front-end-servers-instant-messaging-and-presence.md).</span><span class="sxs-lookup"><span data-stu-id="c20c7-112">For more information, see [Topologies and components for Front End Servers, instant messaging, and presence in Lync Server 2013](lync-server-2013-topologies-and-components-for-front-end-servers-instant-messaging-and-presence.md).</span></span>

<span data-ttu-id="c20c7-113"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c20c7-113"></div>

<span> </span>

</div>

</div>

</span></span></div>

