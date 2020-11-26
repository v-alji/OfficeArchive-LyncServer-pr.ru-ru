---
title: 'Lync Server 2013: создание или изменение рабочего процесса'
description: 'Lync Server 2013: создание или изменение рабочего процесса.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or modify a workflow
ms:assetid: 5ac1c0f3-e82f-40ca-b972-91950e38c05b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520997(v=OCS.15)
ms:contentKeyID: 48184225
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 053b80e313e497313e613a5f8b16bd5beeabf7ac
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431731"
---
# <a name="create-or-modify-a-workflow-in-lync-server-2013"></a><span data-ttu-id="0ba17-103">Создание или изменение рабочего процесса в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0ba17-103">Create or modify a workflow in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0ba17-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0ba17-104">

<span> </span></span></span>

<span data-ttu-id="0ba17-105">_**Тема последнего изменения:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="0ba17-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="0ba17-106">Lync Server 2013 поддерживает два типа рабочих процессов: группу слежения и интерактивный голосовой ответ (интерактивный автоответчик).</span><span class="sxs-lookup"><span data-stu-id="0ba17-106">Lync Server 2013 supports two types of workflows: hunt group and interactive voice response (IVR).</span></span> <span data-ttu-id="0ba17-107">Когда вы создаете рабочий процесс, вы можете указать используемую очередь и другие параметры, такие как приветственное сообщение, музыка на удержании, рабочие часы и вопросы о том, что приложение группы ответа запрашивает вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="0ba17-107">When you create a workflow, you use the Response Group Configuration Tool to specify the queue to use and other settings, such as a welcome message, music on hold, business hours, and questions that the Response Group application asks the caller.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="0ba17-108">Вам следует создать группы агентов и очереди до создания рабочего процесса, который их использует.</span><span class="sxs-lookup"><span data-stu-id="0ba17-108">You must create agent groups and queues before you create a workflow that uses them.</span></span> <span data-ttu-id="0ba17-109">Если вы хотите создать стандартные рабочие часы и праздничные дни, которые можно использовать для нескольких рабочих процессов, необходимо также определить эти часы и праздничные дни перед созданием рабочего процесса, в котором они используются.</span><span class="sxs-lookup"><span data-stu-id="0ba17-109">If you want to create predefined business hours and holidays that you can use for multiple workflows, you must also define these hours and holidays before you create a workflow that uses them.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="0ba17-110">Содержание</span><span class="sxs-lookup"><span data-stu-id="0ba17-110">In This Section</span></span>

  - [<span data-ttu-id="0ba17-111">Создание или изменение рабочего процесса группы слежения в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0ba17-111">Create or modify a hunt group workflow in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-hunt-group-workflow.md)

  - [<span data-ttu-id="0ba17-112">Создание или изменение интерактивного рабочего процесса в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0ba17-112">Create or modify an interactive workflow in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-an-interactive-workflow.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="0ba17-113">См. также</span><span class="sxs-lookup"><span data-stu-id="0ba17-113">See Also</span></span>


[<span data-ttu-id="0ba17-114">Создание или изменение группы агента в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0ba17-114">Create or modify an agent group in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-an-agent-group.md)  
[<span data-ttu-id="0ba17-115">Создание и изменение очереди в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0ba17-115">Create or modify a queue in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-queue.md)  
[<span data-ttu-id="0ba17-116">Необязательно Определение наборов праздников группы ответа в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0ba17-116">(Optional) Define Response Group holiday sets in Lync Server 2013</span></span>](lync-server-2013-optional-define-response-group-holiday-sets.md)  


[<span data-ttu-id="0ba17-117">Необязательно Определение группы ответа в рабочее время в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0ba17-117">(Optional) Define Response Group business hours in Lync Server 2013</span></span>](lync-server-2013-optional-define-response-group-business-hours.md)  
  

<span data-ttu-id="0ba17-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0ba17-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

