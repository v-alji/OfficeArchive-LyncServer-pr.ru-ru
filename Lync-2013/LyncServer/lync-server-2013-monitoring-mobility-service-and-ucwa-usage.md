---
title: 'Lync Server 2013: наблюдение за службой Mobility Service и использование UCWA'
description: 'Lync Server 2013: наблюдение за службой Mobility Service и использование UCWA.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Monitoring Mobility Service and UCWA usage
ms:assetid: 8389b37a-ca3e-4047-8b51-85bc07da87e8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690025(v=OCS.15)
ms:contentKeyID: 48184683
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6575941faf904e46cd1f66d7226a16c88e8cbaa3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425397"
---
# <a name="monitoring-mobility-service-and-ucwa-usage-in-lync-server-2013"></a><span data-ttu-id="1f9e4-103">Наблюдение за работой службы Mobility Service и использованием UCWA в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1f9e4-103">Monitoring Mobility Service and UCWA usage in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1f9e4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1f9e4-104">

<span> </span></span></span>

<span data-ttu-id="1f9e4-105">_**Тема последнего изменения:** 2013-02-14_</span><span class="sxs-lookup"><span data-stu-id="1f9e4-105">_**Topic Last Modified:** 2013-02-14_</span></span>

<span data-ttu-id="1f9e4-106">В настоящее время вы должны наблюдать за ЦП и памятью, используемой службой Lync Server Mobility Service (MCX), и веб-API единой системы обмена сообщениями (UCWA).</span><span class="sxs-lookup"><span data-stu-id="1f9e4-106">On an ongoing basis, you should monitor the CPU and memory that is used by the Lync Server Mobility Service (Mcx) and the Unified Communications Web API (UCWA).</span></span> <span data-ttu-id="1f9e4-107">Чтобы отслеживать использование, прибегите к одному из следующих способов:</span><span class="sxs-lookup"><span data-stu-id="1f9e4-107">To monitor usage, you can use the following:</span></span>

<span data-ttu-id="1f9e4-108">**Для веб-интерфейса API объединенных коммуникаций (UCWA):**</span><span class="sxs-lookup"><span data-stu-id="1f9e4-108">**For Unified Communications Web API (UCWA):**</span></span>

  - <span data-ttu-id="1f9e4-109">Рабочий процесс **LyncUcwa** в диспетчере информационных служб Интернета (IIS).</span><span class="sxs-lookup"><span data-stu-id="1f9e4-109">The **LyncUcwa** worker process in Internet Information Services (IIS) Manager.</span></span> <span data-ttu-id="1f9e4-110">На панели **Рабочие процессы** изучите столбцы **ЦП %** и **Частные байты (КБ)** (память).</span><span class="sxs-lookup"><span data-stu-id="1f9e4-110">In the **Worker Processes** pane, look at the **CPU %** and **Private Bytes (KB)** (memory) columns.</span></span>

  - <span data-ttu-id="1f9e4-111">Счетчики производительности **ЦП** и **Процессор**.</span><span class="sxs-lookup"><span data-stu-id="1f9e4-111">The **CPU** and **Processor** performance counters.</span></span>

<span data-ttu-id="1f9e4-112">В большинстве развертываний ресурсы ЦП, задействованные UCWA, не должны в среднем превышать 15 %.</span><span class="sxs-lookup"><span data-stu-id="1f9e4-112">For most deployments, UCWA CPU usage should be below 15 percent on average.</span></span> <span data-ttu-id="1f9e4-113">Использование памяти должно попадать в пределы, описанные в разделе [наблюдение за ограничениями объема памяти сервера в Lync server 2013](lync-server-2013-monitoring-for-server-memory-capacity-limits.md).</span><span class="sxs-lookup"><span data-stu-id="1f9e4-113">Memory usage should fall within the limits described in [Monitoring for server memory capacity limits in Lync Server 2013](lync-server-2013-monitoring-for-server-memory-capacity-limits.md).</span></span>

<span data-ttu-id="1f9e4-114">Помимо счетчиков использования ЦП и памяти можно использовать следующие счетчики производительности, которые позволят определить степень перегрузки сервера запросами:</span><span class="sxs-lookup"><span data-stu-id="1f9e4-114">In addition to CPU and memory usage counters, you can use the following performance counters to help determine when a server is overloaded with requests:</span></span>

  - <span data-ttu-id="1f9e4-115">**Лат: Интернет – регулирование и проверка подлинности \\ Интернет — общее количество запросов в обработке**, которое указывает число ожидающих веб-запросов на сервере.</span><span class="sxs-lookup"><span data-stu-id="1f9e4-115">**LS:WEB – Throttling and Authentication\\WEB – Total Requests in Processing**, which indicates the number of pending web requests on the server.</span></span> <span data-ttu-id="1f9e4-116">Если этот счетчик достигает 10 000, последующие запросы завершаются с ошибкой "503 — служба недоступна".</span><span class="sxs-lookup"><span data-stu-id="1f9e4-116">When this counter reaches 10,000, subsequent requests will fail, with the error message, "503 - Service Unavailable."</span></span>

  - <span data-ttu-id="1f9e4-117">**ASP.NET \\ Число запросов в очереди** (всегда должно быть равно нулю).</span><span class="sxs-lookup"><span data-stu-id="1f9e4-117">**ASP.NET\\Requests Queued** (should always be zero).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="1f9e4-118">Если вы отвечаете или превышают эти значения, вы должны повторно посещать и пересчитывать планирование мощностей для правильного размера ЦП, количества ядер и памяти для компьютеров, на которых размещается веб-службы.</span><span class="sxs-lookup"><span data-stu-id="1f9e4-118">If you meet or exceed these values, you should revisit and re-compute your capacity planning for the correct sizing of CPU, number of cores and memory for the computers hosting the Web services.</span></span>



</div>

<span data-ttu-id="1f9e4-119">**Для службы Mobility Service (Mcx):**</span><span class="sxs-lookup"><span data-stu-id="1f9e4-119">**For the Mobility Service (Mcx):**</span></span>

  - <span data-ttu-id="1f9e4-120">Рабочие процессы **CSIntMcxAppPool** и **CSExtMcxAppPool** в диспетчере информационных служб Интернета (IIS).</span><span class="sxs-lookup"><span data-stu-id="1f9e4-120">The **CSIntMcxAppPool** and **CSExtMcxAppPool** worker processes in Internet Information Services (IIS) Manager.</span></span> <span data-ttu-id="1f9e4-121">На панели **Рабочие процессы** изучите столбцы **ЦП %** и **Частные байты (КБ)** (память).</span><span class="sxs-lookup"><span data-stu-id="1f9e4-121">In the **Worker Processes** pane, look at the **CPU %** and **Private Bytes (KB)** (memory) columns.</span></span>

  - <span data-ttu-id="1f9e4-122">Счетчики производительности **ЦП** и **Процессор**.</span><span class="sxs-lookup"><span data-stu-id="1f9e4-122">The **CPU** and **Processor** performance counters.</span></span>

<span data-ttu-id="1f9e4-123">В большинстве развертываний ресурсы ЦП, задействованные службой Mobility Service, не должны в среднем превышать 15 %.</span><span class="sxs-lookup"><span data-stu-id="1f9e4-123">For most deployments, Mobility Service CPU usage should be below 15 percent, on average.</span></span> <span data-ttu-id="1f9e4-124">Использование памяти должно попадать в пределы, описанные в разделе [наблюдение за ограничениями объема памяти сервера в Lync server 2013](lync-server-2013-monitoring-for-server-memory-capacity-limits.md).</span><span class="sxs-lookup"><span data-stu-id="1f9e4-124">Memory usage should fall within the limits described in [Monitoring for server memory capacity limits in Lync Server 2013](lync-server-2013-monitoring-for-server-memory-capacity-limits.md).</span></span>

<span data-ttu-id="1f9e4-125">Помимо счетчиков производительности ЦП и памяти можно использовать следующие счетчики производительности ASP.NET, которые позволят определить степень перегрузки сервера запросами.</span><span class="sxs-lookup"><span data-stu-id="1f9e4-125">In addition to CPU and memory usage counters, you can use the following ASP.NET performance counters to help determine when a server is overloaded with requests:</span></span>

  - <span data-ttu-id="1f9e4-126">**ASP.NET v 2.0.50727 \\ Текущие запросы**, обозначающие количество ожидающих веб-запросов на сервере.</span><span class="sxs-lookup"><span data-stu-id="1f9e4-126">**ASP.NET v2.0.50727\\Requests Current**, which indicates the number of pending web requests on the server.</span></span> <span data-ttu-id="1f9e4-127">Если этот счетчик достигает 5 000, последующие запросы завершаются с ошибкой "503 — служба недоступна".</span><span class="sxs-lookup"><span data-stu-id="1f9e4-127">When this counter reaches 5,000, subsequent requests will fail with the error message, "503 - Service Unavailable."</span></span>

  - <span data-ttu-id="1f9e4-128">**ASP.NET \\ Число запросов в очереди** (всегда должно быть равно нулю).</span><span class="sxs-lookup"><span data-stu-id="1f9e4-128">**ASP.NET\\Requests Queued** (should always be zero).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="1f9e4-129">Если вы отвечаете или превышают эти значения, вы должны повторно посещать и повторно вычислять планирование производительности для правильного размера ЦП, количества ядер и памяти для компьютеров, на которых размещается веб-службы.</span><span class="sxs-lookup"><span data-stu-id="1f9e4-129">If you meet or exceed these values, you should revisit and recompute your capacity planning for the correct sizing of CPU, number of cores, and memory for the computers hosting the Web services.</span></span>



</div>

<div>

## <a name="see-also"></a><span data-ttu-id="1f9e4-130">См. также</span><span class="sxs-lookup"><span data-stu-id="1f9e4-130">See Also</span></span>


[<span data-ttu-id="1f9e4-131">Наблюдение за пределами объема памяти сервера в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1f9e4-131">Monitoring for server memory capacity limits in Lync Server 2013</span></span>](lync-server-2013-monitoring-for-server-memory-capacity-limits.md)  
  

<span data-ttu-id="1f9e4-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1f9e4-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

