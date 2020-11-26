---
title: 'Lync Server 2013: наблюдение за производительностью мобильных устройств'
description: 'Lync Server 2013: отслеживание мобильных устройств для повышения производительности.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Monitoring mobility for performance
ms:assetid: 9c831c63-9a7d-48ec-9118-f8a7e80ddd04
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690033(v=OCS.15)
ms:contentKeyID: 48184908
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d6c366542e88406df043ba1a782ee12cd64bd804
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425404"
---
# <a name="monitoring-mobility-for-performance-in-lync-server-2013"></a><span data-ttu-id="e23a1-103">Мониторинг мобильных устройств для повышения производительности в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e23a1-103">Monitoring mobility for performance in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e23a1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e23a1-104">

<span> </span></span></span>

<span data-ttu-id="e23a1-105">_**Тема последнего изменения:** 2013-02-14_</span><span class="sxs-lookup"><span data-stu-id="e23a1-105">_**Topic Last Modified:** 2013-02-14_</span></span>

<span data-ttu-id="e23a1-106">Служба мобильной связи Lync Server (MCX) и веб-интерфейс единой системы обмена сообщениями (UCWA) увеличивают нагрузку на сервер переднего плана и пулы интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="e23a1-106">The Lync Server Mobility Service (Mcx) and the Unified Communications Web API (UCWA) increase the load on Front End Servers and Front End pools.</span></span> <span data-ttu-id="e23a1-107">Мобильные устройства, поддерживающие подключение к серверу даже в том случае, если мобильное приложение свернуто, например устройства с Android и Nokia, на которых работает Lync 2010 Mobile, а также устройства Android и Apple, работающие под управлением Lync 2013 на мобильном устройстве, выпускают больше нагрузки, чем устройства, которые завершают соединение с сервером, когда оно свернуто.</span><span class="sxs-lookup"><span data-stu-id="e23a1-107">Mobile devices that maintain a connection to the server even when the mobile application is minimized, such as Android and Nokia devices running Lync 2010 Mobile, as well as Android and Apple devices running Lync 2013 Mobile, impose a greater load than devices that terminate their connection to the server when the mobile application is minimized.</span></span> <span data-ttu-id="e23a1-108">As your mobility usage increases, you must monitor mobility performance to determine when you need to increase your capacity.</span><span class="sxs-lookup"><span data-stu-id="e23a1-108">As your mobility usage increases, you must monitor mobility performance to determine when you need to increase your capacity.</span></span>

<span data-ttu-id="e23a1-109">Некоторые ограничения, влияющие на производительность мобильности:</span><span class="sxs-lookup"><span data-stu-id="e23a1-109">Several limits influence mobility performance:</span></span>

  - <span data-ttu-id="e23a1-110">доступная память;</span><span class="sxs-lookup"><span data-stu-id="e23a1-110">Available memory</span></span>

  - <span data-ttu-id="e23a1-111">ограничение очереди запросов;</span><span class="sxs-lookup"><span data-stu-id="e23a1-111">Request queue limit</span></span>

  - <span data-ttu-id="e23a1-112">одновременные подключения;</span><span class="sxs-lookup"><span data-stu-id="e23a1-112">Concurrent connections</span></span>

  - <span data-ttu-id="e23a1-113">длина очереди IIS.</span><span class="sxs-lookup"><span data-stu-id="e23a1-113">IIS queue length</span></span>

<span data-ttu-id="e23a1-114">Другие ограничения на серверах, которые могут повлиять на производительность мобильных устройств, задаются максимум двенадцать одновременных входов, проверок подлинности, продления сеансов и прекращений.</span><span class="sxs-lookup"><span data-stu-id="e23a1-114">Other limits on servers that can influence mobility performance are a maximum of twelve concurrent sign-ins, authentications, session renewals, and terminations.</span></span> <span data-ttu-id="e23a1-115">В большинстве развертываний эти максимальные значения не нуждаются в изменении.</span><span class="sxs-lookup"><span data-stu-id="e23a1-115">These maximums do not need to be modified for most deployments.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="e23a1-116">Содержание</span><span class="sxs-lookup"><span data-stu-id="e23a1-116">In This Section</span></span>

  - [<span data-ttu-id="e23a1-117">Наблюдение за пределами объема памяти сервера в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e23a1-117">Monitoring for server memory capacity limits in Lync Server 2013</span></span>](lync-server-2013-monitoring-for-server-memory-capacity-limits.md)

  - [<span data-ttu-id="e23a1-118">Наблюдение за работой службы Mobility Service и использованием UCWA в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e23a1-118">Monitoring Mobility Service and UCWA usage in Lync Server 2013</span></span>](lync-server-2013-monitoring-mobility-service-and-ucwa-usage.md)

  - [<span data-ttu-id="e23a1-119">Настройка службы Mobility Service для высокой производительности в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e23a1-119">Configuring Mobility Service for high performance in Lync Server 2013</span></span>](lync-server-2013-configuring-mobility-service-for-high-performance.md)

  - [<span data-ttu-id="e23a1-120">Мониторинг файлов журнала трассировки запросов IIS в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e23a1-120">Monitoring IIS request tracing log files in Lync Server 2013</span></span>](lync-server-2013-monitoring-iis-request-tracing-log-files.md)

  - [<span data-ttu-id="e23a1-121">Счетчики производительности мобильных устройств в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e23a1-121">Mobility performance counters in Lync Server 2013</span></span>](lync-server-2013-mobility-performance-counters.md)

<span data-ttu-id="e23a1-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e23a1-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

