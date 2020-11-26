---
title: 'Lync Server 2013: поддержка прямых SIP-подключений'
description: Поддержка прямых подключений SIP для Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Direct SIP connections support
ms:assetid: 2107b5b1-b619-4c10-a7db-81d0b9c7f8bf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398289(v=OCS.15)
ms:contentKeyID: 48183611
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 32461cbfd5b1e6371fee3fc92467c8430227f48c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429149"
---
# <a name="direct-sip-connections-support-in-lync-server-2013"></a><span data-ttu-id="566cf-103">Поддержка прямых SIP-подключений в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="566cf-103">Direct SIP connections support in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="566cf-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="566cf-104">

<span> </span></span></span>

<span data-ttu-id="566cf-105">_**Тема последнего изменения:** 2012-06-29_</span><span class="sxs-lookup"><span data-stu-id="566cf-105">_**Topic Last Modified:** 2012-06-29_</span></span>

<span data-ttu-id="566cf-106">Lync Server 2013 поддерживает использование прямых подключений SIP для подключения к серверу Lync Server 2013 одним из следующих способов:</span><span class="sxs-lookup"><span data-stu-id="566cf-106">Lync Server 2013 supports the use of direct SIP connections to connect Lync Server 2013 to either of the following:</span></span>

  - <span data-ttu-id="566cf-107">IP-УАТС;</span><span class="sxs-lookup"><span data-stu-id="566cf-107">An IP-PBX</span></span>

  - <span data-ttu-id="566cf-108">шлюз ТСОП.</span><span class="sxs-lookup"><span data-stu-id="566cf-108">A PSTN gateway</span></span>

<span data-ttu-id="566cf-109">Серверы-посредники в пуле Lync Server 2013 могут управлять несколькими шлюзами, контроллерами границ сеансов (SBCs), предоставленными поставщиками услуг телефонной связи, или некоторыми сочетаниями.</span><span class="sxs-lookup"><span data-stu-id="566cf-109">The Mediation Servers in a Lync Server 2013 pool can control multiple gateways, Session Border Controllers (SBCs) provided by telephony service providers, or some combination thereof.</span></span> <span data-ttu-id="566cf-110">Кроме того, несколько серверов-исправлений в пуле могут взаимодействовать с одним шлюзом.</span><span class="sxs-lookup"><span data-stu-id="566cf-110">Additionally, multiple Mediation Servers in the pool can interact with a single gateway.</span></span>

<span data-ttu-id="566cf-111">Для поиска квалифицированных шлюзов, протоколов IP-АТС и магистральных каналов SIP вы можете использовать открытую программу взаимодействия Microsoft Unified Communications для инфраструктуры корпоративной телефонии.</span><span class="sxs-lookup"><span data-stu-id="566cf-111">You can use the Microsoft Unified Communications Open Interoperability Program for enterprise telephony infrastructure to find qualified PSTN gateways, IP-PBXs, and SIP trunking services.</span></span> <span data-ttu-id="566cf-112">Дополнительные сведения можно найти на веб-сайте Microsoft Unified Communications Open для программы взаимодействия [https://go.microsoft.com/fwlink/p/?linkId=203309](https://go.microsoft.com/fwlink/p/?linkid=203309) .</span><span class="sxs-lookup"><span data-stu-id="566cf-112">For details, see the Microsoft Unified Communications Open Interoperability Program website at [https://go.microsoft.com/fwlink/p/?linkId=203309](https://go.microsoft.com/fwlink/p/?linkid=203309).</span></span>

<span data-ttu-id="566cf-113">Подробнее о топологии и параметрах развертывания для прямых подключений по протоколу SIP можно найти в документации по планированию: [прямые подключения по протоколу SIP в Lync Server 2013](lync-server-2013-direct-sip-connections.md) .</span><span class="sxs-lookup"><span data-stu-id="566cf-113">For details about the topology and deployment options for direct SIP connections, see [Direct SIP connections in Lync Server 2013](lync-server-2013-direct-sip-connections.md) in the Planning documentation.</span></span>

<span data-ttu-id="566cf-114"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="566cf-114"></div>

<span> </span>

</div>

</div>

</span></span></div>

