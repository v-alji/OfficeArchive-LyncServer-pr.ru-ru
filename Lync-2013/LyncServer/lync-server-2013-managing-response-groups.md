---
title: 'Lync Server 2013: Управление группами ответа'
description: 'Lync Server 2013: Управление группами ответа.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing response groups
ms:assetid: 5a804d7d-3c1a-4647-a0e0-d5c4c8c23b73
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520996(v=OCS.15)
ms:contentKeyID: 48184222
ms.date: 02/01/2018
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 138ece386d55895893402e5a1fdead58790504f5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437212"
---
# <a name="managing-response-groups-in-lync-server-2013"></a><span data-ttu-id="691e2-103">Управление группами ответов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="691e2-103">Managing response groups in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="691e2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="691e2-104">

<span> </span></span></span>

<span data-ttu-id="691e2-105">_**Тема последнего изменения:** 2018-02-01_</span><span class="sxs-lookup"><span data-stu-id="691e2-105">_**Topic Last Modified:** 2018-02-01_</span></span>

<span data-ttu-id="691e2-106">Группы ответа — это функция управления звонками, которая позволяет ставить в очередь звонки, которые выполняются в определенной области, например в службу поддержки, а затем перенаправлять звонки в определенную группу пользователей, которые называются *агентами*.</span><span class="sxs-lookup"><span data-stu-id="691e2-106">Response groups are a call management feature that enables you to queue calls that are made to a specific area, such as a Help Desk, and then route the calls to a designated group of people, called *agents*.</span></span>

<span data-ttu-id="691e2-107">Для управления группами ответа настраиваются группы агента, очереди и рабочие процессы, которые определяют, что произойдет с вызовом с момента его появления, пока агент не ответит.</span><span class="sxs-lookup"><span data-stu-id="691e2-107">To manage response groups, you configure agent groups, queues, and workflows, which define what happens to a call from the time it is placed until an agent answers it.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="691e2-108">Если у вас более 300 рабочих процессов в одном пуле в развертывании группы ответа, лучше использовать командлеты командной консоли Lync Server для создания рабочих процессов.</span><span class="sxs-lookup"><span data-stu-id="691e2-108">If you have more than 300 workflows in a single pool in your Response Group deployment, it is better to use Lync Server Management Shell cmdlets to create the workflows.</span></span> <span data-ttu-id="691e2-109">Если вы используете средство настройки группы ответа для создания рабочих процессов для пула с более чем 300 рабочими процессами, веб-страница занимает много времени.</span><span class="sxs-lookup"><span data-stu-id="691e2-109">If you use the Response Group Configuration Tool to create workflows for a pool that has more than 300 workflows, the webpage takes a long time to load.</span></span> <span data-ttu-id="691e2-110">Количество агентов, косвенно связанных с рабочими процессами, в очереди также имеет пропорциональный эффект для загрузки страницы.</span><span class="sxs-lookup"><span data-stu-id="691e2-110">The number of agents that are indirectly associated with workflows through the queues also has a proportional effect on page loading.</span></span>



</div>

<span data-ttu-id="691e2-111">В этой статье приведены пошаговые инструкции для задач, которые можно выполнять для настройки и обслуживания приложения группы ответа в развертывании.</span><span class="sxs-lookup"><span data-stu-id="691e2-111">Topics in this section provide step-by-step procedures for tasks that you can perform to customize and maintain the Response Group application in your deployment</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="691e2-112">Содержание</span><span class="sxs-lookup"><span data-stu-id="691e2-112">In This Section</span></span>

  - [<span data-ttu-id="691e2-113">Управление группами агентов группы ответа в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="691e2-113">Managing Response Group agent groups in Lync Server 2013</span></span>](lync-server-2013-managing-response-group-agent-groups.md)

  - [<span data-ttu-id="691e2-114">Управление очередями групп ответов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="691e2-114">Managing Response Group queues in Lync Server 2013</span></span>](lync-server-2013-managing-response-group-queues.md)

  - [<span data-ttu-id="691e2-115">Управление рабочими процессами групп ответов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="691e2-115">Managing Response Group workflows in Lync Server 2013</span></span>](lync-server-2013-managing-response-group-workflows.md)

  - [<span data-ttu-id="691e2-116">Управление параметрами группы ответа уровня приложения в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="691e2-116">Managing application-level Response Group settings in Lync Server 2013</span></span>](lync-server-2013-managing-application-level-response-group-settings.md)

  - [<span data-ttu-id="691e2-117">Перемещение групп ответа в новый пул в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="691e2-117">Moving response groups to a new pool in Lync Server 2013</span></span>](lync-server-2013-moving-response-groups-to-a-new-pool.md)

  - [<span data-ttu-id="691e2-118">Управление группами ответов в Lync Server 2013 в аварийном режиме</span><span class="sxs-lookup"><span data-stu-id="691e2-118">Managing response groups in Lync Server 2013 during a disaster</span></span>](lync-server-2013-managing-response-groups-during-a-disaster.md)

<span data-ttu-id="691e2-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="691e2-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

