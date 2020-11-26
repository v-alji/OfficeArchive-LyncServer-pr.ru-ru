---
title: Распределение нагрузки для конференции Lync Server 2013
description: Распределение загрузки для конференции Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Conferencing load distribution
ms:assetid: 5901a076-1b6f-4720-8837-95fc7f3c37f3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204922(v=OCS.15)
ms:contentKeyID: 48184233
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 28897b26d7351bf0ea577e2678d916aec6d15647
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434328"
---
# <a name="conferencing-load-distribution-in-lync-server-2013"></a><span data-ttu-id="0cde0-103">Распределение нагрузки для конференц-связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0cde0-103">Conferencing load distribution in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0cde0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0cde0-104">

<span> </span></span></span>

<span data-ttu-id="0cde0-105">_**Тема последнего изменения:** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="0cde0-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="0cde0-106">В отличие от некоторых других выделенных решений для конференций архитектура Lync Server — это модель общего оборудования.</span><span class="sxs-lookup"><span data-stu-id="0cde0-106">Unlike some other dedicated conferencing solutions, Lync Server architecture is a shared-hardware model.</span></span> <span data-ttu-id="0cde0-107">Это означает, что одно и то же оборудование является общим для многих программных компонентов, каждый из которых поддерживает различные коммуникации в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="0cde0-107">This means that the same hardware is shared by many software components, each of which supports different real-time communications.</span></span> <span data-ttu-id="0cde0-108">Каждый тип загрузок в режиме реального времени, определенных на серверах.</span><span class="sxs-lookup"><span data-stu-id="0cde0-108">Each type of real-time communications places specific loads on the servers.</span></span> <span data-ttu-id="0cde0-109">Например, сервер переднего плана может выполнять компоненты маршрутизации SIP, веб-приложения (например, поиск в адресных книгах), службу веб-конференций, службу Конференции, а также корпоративные приложения (например, приложение для проведения конференций и приложение группы ответа) и сервер исправлений.</span><span class="sxs-lookup"><span data-stu-id="0cde0-109">For example, the Front End Server can run the Session Initiation Protocol (SIP) routing components, web applications (such as Address Book search), Web Conferencing service, A/V Conferencing service, Enterprise Voice applications (for example, Conferencing Attendant application and Response Group application), and Mediation Server.</span></span> <span data-ttu-id="0cde0-110">Набор баз данных на сервере переднего плана также обеспечивает хранение и обработку для пользователей, контактов, присутствия, конференций и данных голосовой маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="0cde0-110">A set of databases on the Front End Server also provide storage and processing for user, contact, presence, conferencing, and voice routing data.</span></span> <span data-ttu-id="0cde0-111">Благодаря такому оборудованию, компоненты, службы и процессы конкурирует за ресурсы ЦП и памяти, поэтому рабочие нагрузки, не связанные с Конференцией, непосредственным образом влияют на масштабирование сервера.</span><span class="sxs-lookup"><span data-stu-id="0cde0-111">With this hardware sharing, components, services, and processes compete for CPU and memory resources, so non-conferencing workloads have a direct impact on server scaling.</span></span>

<span data-ttu-id="0cde0-112">По сравнению с другими решениями для Конференции на основе аппаратного порта, архитектура конференции Lync Server — это модель без резервирования.</span><span class="sxs-lookup"><span data-stu-id="0cde0-112">Compared to other hardware port-based conferencing solutions, Lync Server conferencing architecture is a no-reservation model.</span></span> <span data-ttu-id="0cde0-113">Когда пользователь планирует собрание, Lync Server создает запись в базе данных конференций, в которой хранятся данные конференций, но не резервирует ресурсы оборудования для запланированного собрания заранее.</span><span class="sxs-lookup"><span data-stu-id="0cde0-113">When a user schedules a meeting, Lync Server creates a record in the conferencing database, which stores conferencing data, but does not reserve any hardware resources for the scheduled meeting ahead of time.</span></span> <span data-ttu-id="0cde0-114">Вместо этого Lync Server имеет встроенную логику балансировки нагрузки для динамического выделения ресурсов конференций на серверах переднего плана таким образом, чтобы они были распределены между всеми серверами переднего плана в пуле.</span><span class="sxs-lookup"><span data-stu-id="0cde0-114">Instead, Lync Server has built-in load balancing logic to dynamically allocate conferencing resources on Front End Servers in a way that distributes loads equally across all Front End Servers in the pool.</span></span> <span data-ttu-id="0cde0-115">Это эффективно подготавливает и использует аппаратные ресурсы, но затрудняет поддержку очень крупных собраний (особенно без соответствующего планирования).</span><span class="sxs-lookup"><span data-stu-id="0cde0-115">This effectively provisions and utilizes hardware resources, but makes it challenging to support very large meetings (especially without appropriate planning).</span></span> <span data-ttu-id="0cde0-116">Например, когда сервер Lync Server 2013 работает ближе к наибольшей емкости, каждый сервер переднего плана может размещаться около 125 среднего размера собраний.</span><span class="sxs-lookup"><span data-stu-id="0cde0-116">For example, when a Lync Server 2013 pool is running close to its top capacity, each Front End Server might host approximately 125 average-size meetings.</span></span> <span data-ttu-id="0cde0-117">При этом можно без затруднений добавить еще одно небольшое собрание, но добавление собрания для 1000 пользователей может привести к неполадкам, так как серверы переднего плана, вероятно, не смогут поддерживать такое большое собрание и одновременно еще 125 собраний.</span><span class="sxs-lookup"><span data-stu-id="0cde0-117">Adding another small meeting would not be a problem, but adding a meeting for 1000 users would be a problem because the Front End Servers would probably not be able to support such a large meeting at the same time as the other 125 meetings.</span></span>

<span data-ttu-id="0cde0-118"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0cde0-118"></div>

<span> </span>

</div>

</div>

</span></span></div>

