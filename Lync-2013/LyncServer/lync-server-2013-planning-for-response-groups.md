---
title: 'Lync Server 2013: планирование групп ответа'
description: 'Lync Server 2013: планирование групп ответа.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for response groups
ms:assetid: 7c10ce08-0068-4b22-8ecc-33e94811c900
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398617(v=OCS.15)
ms:contentKeyID: 48184608
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a3e5abbcf3620a628f2929059b03ffc3588f5349
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49400204"
---
# <a name="planning-for-response-groups-in-lync-server-2013"></a><span data-ttu-id="854f9-103">Планирование групп ответа в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="854f9-103">Planning for response groups in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="854f9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="854f9-104">

<span> </span></span></span>

<span data-ttu-id="854f9-105">_**Тема последнего изменения:** 2012-06-19_</span><span class="sxs-lookup"><span data-stu-id="854f9-105">_**Topic Last Modified:** 2012-06-19_</span></span>

<span data-ttu-id="854f9-106">Если в вашей организации есть группы пользователей, которые отвечают и управляют определенными типами звонков, например для обслуживания клиентов, внутренней службы поддержки и поддержки по телефону для отдела, вы можете развернуть приложение группы ответа Lync Server для управления этими типами звонков.</span><span class="sxs-lookup"><span data-stu-id="854f9-106">If your organization has groups of people who answer and manage certain types of calls, such as for customer service, an internal help desk, or general telephone support for a department, you can deploy the Lync Server Response Group application to manage these types of calls.</span></span> <span data-ttu-id="854f9-107">Приложение "группа ответа" маршрутизирует и помещает входящие звонки определенным людям, которые называются агентами.</span><span class="sxs-lookup"><span data-stu-id="854f9-107">The Response Group application routes and queues incoming calls to designated persons, who are known as agents.</span></span> <span data-ttu-id="854f9-108">С помощью групп ответа можно увеличить степень использования телефонной службы поддержки и сократить расходы на работу этих служб.</span><span class="sxs-lookup"><span data-stu-id="854f9-108">You can increase the use of telephone support services and reduce the overhead of running these services by using response groups.</span></span> <span data-ttu-id="854f9-109">В этом разделе описаны вопросы планирования для группы ответа.</span><span class="sxs-lookup"><span data-stu-id="854f9-109">This section describes planning considerations for Response Group.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="854f9-110">Содержание</span><span class="sxs-lookup"><span data-stu-id="854f9-110">In This Section</span></span>

  - [<span data-ttu-id="854f9-111">Общие сведения о приложении "группа ответа" в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="854f9-111">Overview of the Response Group application in Lync Server 2013</span></span>](lync-server-2013-overview-of-the-response-group-application.md)

  - [<span data-ttu-id="854f9-112">Компоненты, используемые группой ответа в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="854f9-112">Components used by Response Group in Lync Server 2013</span></span>](lync-server-2013-components-used-by-response-group.md)

  - [<span data-ttu-id="854f9-113">Технические требования для групп ответа в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="854f9-113">Technical requirements for Response Group in Lync Server 2013</span></span>](lync-server-2013-technical-requirements-for-response-group.md)

  - [<span data-ttu-id="854f9-114">Клиенты, поддерживаемые для группы ответа в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="854f9-114">Clients supported for Response Group in Lync Server 2013</span></span>](lync-server-2013-clients-supported-for-response-group.md)

  - [<span data-ttu-id="854f9-115">Планирование емкости для группы ответа в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="854f9-115">Capacity planning for Response Group in Lync Server 2013</span></span>](lync-server-2013-capacity-planning-for-response-group.md)

  - [<span data-ttu-id="854f9-116">Процесс развертывания группы ответа в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="854f9-116">Deployment process for Response Group in Lync Server 2013</span></span>](lync-server-2013-deployment-process-for-response-group.md)

<span data-ttu-id="854f9-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="854f9-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

