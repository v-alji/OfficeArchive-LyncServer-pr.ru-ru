---
title: Пользовательская модель конференц-связи Lync Server 2013
description: Пользовательская модель конференции Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: The conferencing user model
ms:assetid: ba4bbba9-f2e3-4cab-8eba-b51f12133cab
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205199(v=OCS.15)
ms:contentKeyID: 48185229
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 699f41303b82f4d8fd2864cbf1b29a1c601b826e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434281"
---
# <a name="the-conferencing-user-model-in-lync-server-2013"></a><span data-ttu-id="057f7-103">Пользовательская модель конференц-связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="057f7-103">The conferencing user model in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="057f7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="057f7-104">

<span> </span></span></span>

<span data-ttu-id="057f7-105">_**Тема последнего изменения:** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="057f7-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="057f7-106">Важной частью пользовательской модели конференц-связи с Lync Server является размер собрания.</span><span class="sxs-lookup"><span data-stu-id="057f7-106">A critical part of the Lync Server conferencing user model is meeting size.</span></span> <span data-ttu-id="057f7-107">После сбора данных из нескольких точек данных (как описано в предыдущем разделе) мы определили следующее:</span><span class="sxs-lookup"><span data-stu-id="057f7-107">After collecting data from the multiple data points (as described in the previous section), we determined the following:</span></span>

  - <span data-ttu-id="057f7-108">Большинство собраний — это небольшие собрания для совместной работы с участием не более 4 – 6 человек.</span><span class="sxs-lookup"><span data-stu-id="057f7-108">Most meetings are actually small collaborative meetings with an average of four to six participants</span></span>

  - <span data-ttu-id="057f7-109">Около 80% собраний менее 20 участников.</span><span class="sxs-lookup"><span data-stu-id="057f7-109">Approximately 80 percent of meetings have fewer than 20 participants.</span></span>

  - <span data-ttu-id="057f7-110">99,98 процентов собраний менее 100 участников.</span><span class="sxs-lookup"><span data-stu-id="057f7-110">99.98 percent of meetings have fewer than 100 participants.</span></span>

<span data-ttu-id="057f7-111">Кроме размера собрания, пользовательская модель конференций также учитывает различные факторы, например:</span><span class="sxs-lookup"><span data-stu-id="057f7-111">In addition to meeting size, the conferencing user model also takes into account a variety of factors, such as:</span></span>

  - <span data-ttu-id="057f7-112">**Одновременные собрания**   Сколько пользователей должны одновременно находиться в собраниях?</span><span class="sxs-lookup"><span data-stu-id="057f7-112">**Concurrent meetings**   How many users are expected to be in meetings at the same time?</span></span>

  - <span data-ttu-id="057f7-113">**Набор мультимедиа**   Какие типы мультимедиа доступны и должны использоваться пользователями в собраниях?</span><span class="sxs-lookup"><span data-stu-id="057f7-113">**Media mix**   What types of media are available and expected to be used by users in meetings?</span></span>

  - <span data-ttu-id="057f7-114">**Пользовательские типы**   Пользователи — внутренние пользователи, удаленные пользователи, Федеративные пользователи или анонимные пользователи?</span><span class="sxs-lookup"><span data-stu-id="057f7-114">**User types**   Are users internal users, remote users, federated users, or anonymous users?</span></span>

  - <span data-ttu-id="057f7-115">**Время увеличения собрания**   Как долго все пользователи собрания смогут присоединиться к собранию?</span><span class="sxs-lookup"><span data-stu-id="057f7-115">**Meeting ramp up time**   How long does it take for all users of a meeting to join a meeting?</span></span>

<span data-ttu-id="057f7-116">Подробные сведения о пользовательской модели можно найти в статьях [пользовательские модели в Lync Server 2013](lync-server-2013-user-models.md).</span><span class="sxs-lookup"><span data-stu-id="057f7-116">For details about the user model, see [User models in Lync Server 2013](lync-server-2013-user-models.md).</span></span>

<span data-ttu-id="057f7-117">Для определения количества собраний и пользователей, используемых для тестирования, мы сделали следующее:</span><span class="sxs-lookup"><span data-stu-id="057f7-117">To determine the number of meetings and users to use for testing, we did the following:</span></span>

  - <span data-ttu-id="057f7-118">Затратил общее количество пользователей в Организации (например, 80 000 пользователей) и умножая их на параллельный тариф (например, 5% от всех пользователей), чтобы определить общее количество пользователей, которые должны одновременно находиться в собраниях (в этом примере — 4000 пользователей).</span><span class="sxs-lookup"><span data-stu-id="057f7-118">Took the total number of users in an organization (for example, 80,000 users) and multiplied it by the meeting concurrency rate (for example, 5% of all users) to determine the total number of users expected to be in meetings at the same time (in this example, 4000 users).</span></span>

  - <span data-ttu-id="057f7-119">В этом примере общее количество пользователей на сервере Lync Server 2013, сервере переднего плана в развертывании (например, 8 серверов) используется для определения предполагаемого количества участников собрания для каждого сервера переднего плана (в данном случае — 500 пользователей на сервере переднего плана).</span><span class="sxs-lookup"><span data-stu-id="057f7-119">Divided the total number of users by the number of Lync Server 2013, Front End Servers in the deployment (for example, 8 servers) to determine the estimated number of meeting participants per Front End Server (in this example, 500 users per Front End Server).</span></span>

  - <span data-ttu-id="057f7-120">Разделить количество пользователей на сервере переднего плана по среднему размеру собрания (например, 4 пользователям), чтобы определить предполагаемое среднее количество собраний на сервер переднего плана (в этом примере — собрание 125 на сервере переднего плана).</span><span class="sxs-lookup"><span data-stu-id="057f7-120">Divided the number of users per Front End Server by the average meeting size (for example, 4 users) to determine the estimated average number of meetings per Front End Server (in this example, 125 meetings per Front End Server).</span></span>

  - <span data-ttu-id="057f7-121">Для получения каждой нагрузки на каждый сервер переднего плана мы оценили набор мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="057f7-121">To get the per media load on each Front End Server, we estimated the media mix.</span></span> <span data-ttu-id="057f7-122">Например, при условии, что в 75% для собраний требуется больше, чем просто поддержка звука, а 50% — общий доступ к приложениям, то есть общее число 47 и 188 пользователей подключаются параллельно к каждому серверу переднего плана для общего доступа к приложениям.</span><span class="sxs-lookup"><span data-stu-id="057f7-122">For example, assuming that 75% of the meetings require more than just audio support and 50% of those meetings require application sharing, an average of 47 meetings and 188 users connect concurrently to each Front End Server for application sharing.</span></span>

  - <span data-ttu-id="057f7-123">Вы проверили различные размеры собрания (на основе нашей пользовательской модели 250 для пользователей в общем пуле), чтобы обеспечить масштабируемость сервера.</span><span class="sxs-lookup"><span data-stu-id="057f7-123">Tested a variety of meeting sizes (based our user model of up to 250 users in a shared pool) to ensure server scalability.</span></span>

<span data-ttu-id="057f7-124"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="057f7-124"></div>

<span> </span>

</div>

</div>

</span></span></div>

