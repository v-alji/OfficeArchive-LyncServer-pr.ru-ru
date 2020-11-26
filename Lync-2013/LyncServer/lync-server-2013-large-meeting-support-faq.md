---
title: 'Lync Server 2013: вопросы и ответы по поддержке большого количества собраний'
description: 'Lync Server 2013: вопросы и ответы по поддержке большого количества собраний.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Lync Server large meeting support FAQ
ms:assetid: 34b4fb6a-e35c-47e8-8ab1-f8331741fed2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204804(v=OCS.15)
ms:contentKeyID: 48183837
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c8d206400b46fc32a3af7b21ad7d50663e85d069
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426692"
---
# <a name="large-meeting-support-faq-for-lync-server-2013"></a><span data-ttu-id="c524a-103">Дополнительные вопросы и ответы о поддержке собраний для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c524a-103">Large meeting support FAQ for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c524a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c524a-104">

<span> </span></span></span>

<span data-ttu-id="c524a-105">_**Тема последнего изменения:** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="c524a-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="c524a-106">В следующих разделах приведены ответы на часто задаваемые вопросы о создании и выполнении крупных собраний.</span><span class="sxs-lookup"><span data-stu-id="c524a-106">The following sections provide answers to common questions for creating and running large meetings.</span></span>

<div>

## <a name="q-how-many-users-can-participate-in-a-large-meeting"></a><span data-ttu-id="c524a-107">Вопрос: сколько пользователей может участвовать в большом собрании?</span><span class="sxs-lookup"><span data-stu-id="c524a-107">Q: How many users can participate in a large meeting?</span></span>

<span data-ttu-id="c524a-108">Пользовательская модель Lync Server определяет количество пользователей 250 в общем пуле или 1000 пользователей в пуле, предназначенных для крупных собраний, но эти числа представляют только число тестируемых пользователей и только для определенного набора оборудования, которое мы использовали в нашем тестировании.</span><span class="sxs-lookup"><span data-stu-id="c524a-108">The Lync Server user model specifies limits of 250 users in a shared pool or 1000 users in a pool dedicated to large meetings, but these numbers only represent the number of users we tested and only for the specific set of hardware that we used in our testing.</span></span> <span data-ttu-id="c524a-109">В соответствии с нашим тестированием мы рекомендуем использовать эти ограничения для максимального размера.</span><span class="sxs-lookup"><span data-stu-id="c524a-109">Based on our testing, we recommend those limits for maximum sizes.</span></span> <span data-ttu-id="c524a-110">Тем не менее, вы можете управлять реальным количеством участников, разрешенных на собраниях в вашей организации, настроив одну или несколько политик конференц-связи (которые вы конфигурируете с помощью командлетов Windows PowerShell в командной консоли Lync Server Management Shell или с помощью панели управления Lync Server).</span><span class="sxs-lookup"><span data-stu-id="c524a-110">However, you control the actual number of participants allowed in meetings in your organization by configuring one or more conferencing policies (which you configure using Windows PowerShell cmdlets in the Lync Server Management Shell or using the Lync Server Control Panel).</span></span> <span data-ttu-id="c524a-111">Число, указанное в политике конференц-связи, может быть любым 32-битным целым числом от 1 до 4 294 967 295, но рекомендуемый размер — от 2 до 250 участников, включительно; значение по умолчанию — 250.</span><span class="sxs-lookup"><span data-stu-id="c524a-111">The number that you specify in a conferencing policy can be any 32-bit whole number between 1 and 4,294,967,295, but the recommended size is between 2 and 250 participants, inclusive; and the default value is 250.</span></span>

</div>

<div>

## <a name="q-how-many-meetings-or-other-workloads-can-i-have-in-a-pool-that-is-dedicated-to-large-meetings"></a><span data-ttu-id="c524a-112">Вопрос: сколько собраний или других рабочих нагрузок можно найти в пуле, предназначенном для крупных собраний?</span><span class="sxs-lookup"><span data-stu-id="c524a-112">Q: How many meetings or other workloads can I have in a pool that is dedicated to large meetings?</span></span>

<span data-ttu-id="c524a-113">Для обеспечения оптимального взаимодействия с пользователями в крупных собраниях до 1000 участников рекомендуется размещать в пуле только одно большое собрание, предназначенное для крупных собраний.</span><span class="sxs-lookup"><span data-stu-id="c524a-113">To ensure the best user experience in large meetings of up to 1000 participants, we recommend hosting only a single large meeting at a time on a pool that is dedicated to large meetings.</span></span> <span data-ttu-id="c524a-114">Кроме того, мы рекомендуем не разрешать выполнение каких – либо других рабочих нагрузок в пуле при выполнении большого собрания.</span><span class="sxs-lookup"><span data-stu-id="c524a-114">We also recommend not allowing any other workloads to run on that pool when the large meeting is in progress.</span></span>

</div>

<div>

## <a name="q-should-the-organizers-of-large-meeting-be-homed-on-the-dedicated-pool"></a><span data-ttu-id="c524a-115">Вопрос: должна ли организаторовка большого собрания быть размещена в выделенном пуле?</span><span class="sxs-lookup"><span data-stu-id="c524a-115">Q: Should the organizers of large meeting be homed on the dedicated pool?</span></span>

<span data-ttu-id="c524a-116">Нет.</span><span class="sxs-lookup"><span data-stu-id="c524a-116">No.</span></span> <span data-ttu-id="c524a-117">Мы рекомендуем не разкрывайте пользователей, кроме выделенных сотрудников, которые управляют планированием крупных собраний в выделенном пуле.</span><span class="sxs-lookup"><span data-stu-id="c524a-117">We recommend not homing any users other than the dedicated staff that manages scheduling of large meetings on the dedicated pool.</span></span> <span data-ttu-id="c524a-118">Это предотвращает возникновение проблем с большим количеством собраний, размещенных в пуле, в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="c524a-118">This prevents other real-time communications traffic from causing problems with large meetings that are hosted in the pool.</span></span> <span data-ttu-id="c524a-119">Вы должны планировать большие собрания в выделенном пуле, используя учетную запись большого сотрудника для планирования собраний.</span><span class="sxs-lookup"><span data-stu-id="c524a-119">You should schedule large meetings on the dedicated pool using a user account of the large meeting scheduling staff.</span></span> <span data-ttu-id="c524a-120">Вы должны добавить учетную запись пользователя организатора собрания (пользователя, который запрашивает большое собрание) в качестве выступающего для большого собрания.</span><span class="sxs-lookup"><span data-stu-id="c524a-120">You should add the user account of the meeting organizer (the user who requests a large meeting) as a presenter for the large meeting.</span></span>

</div>

<div>

## <a name="q-what-media-modalities-can-i-use-in-a-large-meeting"></a><span data-ttu-id="c524a-121">Вопрос: какие носители мультимедиа модальностей можно использовать в большом собрании?</span><span class="sxs-lookup"><span data-stu-id="c524a-121">Q: What media modalities can I use in a large meeting?</span></span>

<span data-ttu-id="c524a-122">Большое количество собраний с до 1000 пользователей может включать в себя звук, видео, общий доступ к PowerPoint, доски и опрос присутствия.</span><span class="sxs-lookup"><span data-stu-id="c524a-122">Large meetings with up to 1000 users can include audio, video, PowerPoint sharing, whiteboards, and presence polling.</span></span>

</div>

<div>

## <a name="q-can-i-use-group-instant-messaging-im-in-large-meetings"></a><span data-ttu-id="c524a-123">Вопрос: можно ли использовать групповую обмен мгновенными сообщениями (IM) в крупных собраниях?</span><span class="sxs-lookup"><span data-stu-id="c524a-123">Q: Can I use group instant messaging (IM) in large meetings?</span></span>

<span data-ttu-id="c524a-124">Да.</span><span class="sxs-lookup"><span data-stu-id="c524a-124">Yes.</span></span> <span data-ttu-id="c524a-125">Однако большое количество мгновенных сообщений, особенно при отправке большого количества участников собрания, может повлиять на взаимодействие с пользователем из-за проблем с быстрой прокруткой текста в окне мгновенного обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="c524a-125">However, large numbers of instant messages, especially when sent by a large number of meeting participants, can affect the user experience due to problems with fast text scrolling in the IM window.</span></span> <span data-ttu-id="c524a-126">Доставка большого количества мгновенных сообщений до 1000 пользователей также может привести к значительным загрузкам сервера, что может повлиять на производительность.</span><span class="sxs-lookup"><span data-stu-id="c524a-126">Delivering a large amount of instant messages to up to 1000 users can also introduce significant server loads, which can affect performance.</span></span> <span data-ttu-id="c524a-127">Обычно обмен мгновенными сообщениями требуется только для вопросов и ответов (Q \& as).</span><span class="sxs-lookup"><span data-stu-id="c524a-127">Generally, IM is only required for questions and answers (Q\&As).</span></span>

</div>

<div>

## <a name="can-users-join-large-meetings-by-dialing-in-from-a-phone"></a><span data-ttu-id="c524a-128">Могут ли пользователи присоединяться к большим собраниям с помощью телефонного подключения?</span><span class="sxs-lookup"><span data-stu-id="c524a-128">Can users join large meetings by dialing in from a phone?</span></span>

<span data-ttu-id="c524a-129">Да.</span><span class="sxs-lookup"><span data-stu-id="c524a-129">Yes.</span></span> <span data-ttu-id="c524a-130">Если пул Lync Server 2013 правильно развернут и включен для конференц-связи с телефонным подключением, пользователи смогут присоединиться к большим собраниям с помощью набора номера.</span><span class="sxs-lookup"><span data-stu-id="c524a-130">If the Lync Server 2013 pool is properly deployed and enabled for dial-in conferencing, users will be able to join the large meetings by dialing in.</span></span> <span data-ttu-id="c524a-131">Наше тестирование показало, что до 15% пользователей 1000 может присоединиться к большому собранию в течение 10 минут.</span><span class="sxs-lookup"><span data-stu-id="c524a-131">Our testing has shown that up to 15% of the 1000 users can join the large meeting over a 10 minute period.</span></span>

</div>

<div>

## <a name="q-can-i-host-large-meetings-in-a-virtual-topology"></a><span data-ttu-id="c524a-132">Вопрос: можно ли размещать большие собрания в виртуальной топологии?</span><span class="sxs-lookup"><span data-stu-id="c524a-132">Q: Can I host large meetings in a virtual topology?</span></span>

<span data-ttu-id="c524a-133">Мы не проверяли в виртуальной топологии большое количество собраний, поэтому мы не поддерживаем использование виртуальных машин для размещения выделенного пула для крупных собраний.</span><span class="sxs-lookup"><span data-stu-id="c524a-133">We have not tested large meetings in a virtual topology, so we do not support the use of virtual machines to host a dedicated pool for large meetings.</span></span>

<span data-ttu-id="c524a-134"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c524a-134"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

