---
title: 'Lync Server 2013: ежедневные задачи'
description: 'Lync Server 2013: ежедневные задачи.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Daily tasks
ms:assetid: f7a5f99e-5d2b-445d-9ba1-cbfcfeff16ae
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720351(v=OCS.15)
ms:contentKeyID: 63969666
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d9e2d62eb29db2bafa23565637bb655ba932c7b6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431318"
---
# <a name="daily-tasks-in-lync-server-2013"></a><span data-ttu-id="2699b-103">Ежедневные задачи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2699b-103">Daily tasks in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2699b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2699b-104">

<span> </span></span></span>

<span data-ttu-id="2699b-105">_**Тема последнего изменения:** 2015-01-26_</span><span class="sxs-lookup"><span data-stu-id="2699b-105">_**Topic Last Modified:** 2015-01-26_</span></span>

<span data-ttu-id="2699b-106">Чтобы обеспечить доступность и надежность развертывания Lync Server 2013, вы должны быть частью повседневных повседневных задач мониторинга и тестирования, которые очень важны для работы системы, включая физическую платформу, операционную систему и все важные службы Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="2699b-106">To help ensure the availability and reliability of the Lync Server 2013 deployment, you should as part of daily routine monitor and test elements that are very important to the functioning of the system, which includes the physical platform, the operating system, and all important Lync Server 2013 services.</span></span> <span data-ttu-id="2699b-107">Профилактическое обслуживание и упреждающий мониторинг помогут выявить потенциальные ошибки и проблемы, которые могут отрицательно сказаться на развертывании Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="2699b-107">Preventive maintenance and proactive monitoring will help you identify potential errors and issues that may adversely affect the Lync Server 2013 deployment.</span></span>

<span data-ttu-id="2699b-108">Наблюдение за развертыванием Lync Server 2013 включает в себя поиск проблем с соединениями, службами, серверными ресурсами и системными ресурсами.</span><span class="sxs-lookup"><span data-stu-id="2699b-108">Monitoring the Lync Server 2013 deployment involves checking for issues with connections, services, server resources, and system resources.</span></span> <span data-ttu-id="2699b-109">Операционные системы Windows Server вместе с System Center Operations Manager и Lync Server предоставляют множество средств и служб мониторинга, которые помогают обеспечить бесперебойную работу Организации Lync Server.</span><span class="sxs-lookup"><span data-stu-id="2699b-109">Windows Server operating systems, together with System Center Operations Manager, and Lync Server give you many monitoring tools and services to help ensure that the Lync Server organization is running smoothly.</span></span> <span data-ttu-id="2699b-110">При совместной реализации данных технологий администраторы могут получать оповещения при или до возникновения проблем.</span><span class="sxs-lookup"><span data-stu-id="2699b-110">When these technologies are implemented together, administrators will be able to receive alerts when or before issues occur.</span></span>

<span data-ttu-id="2699b-111">Основные преимущества ежедневного мониторинга:</span><span class="sxs-lookup"><span data-stu-id="2699b-111">The key advantages to daily monitoring are as follows:</span></span>

  - <span data-ttu-id="2699b-112">Соответствие требованиям производительности и доступности, определенным в соглашениях об уровне обслуживания.</span><span class="sxs-lookup"><span data-stu-id="2699b-112">Meeting the performance and availability requirements of defined SLAs.</span></span>

  - <span data-ttu-id="2699b-113">Успешное выполнение определенных административных задач, таких как ежедневные операции резервного копирования и проверка работоспособности сервера.</span><span class="sxs-lookup"><span data-stu-id="2699b-113">Successfully completing specific administrative tasks, such as daily backup operations, and checking server health.</span></span>

  - <span data-ttu-id="2699b-114">Определение и решение проблем, таких как ограничения производительности сервера или необходимость в дополнительных ресурсах до того, как это окажет влияние на производительность.</span><span class="sxs-lookup"><span data-stu-id="2699b-114">Detecting and addressing issues, such as bottlenecks in the server performance, or need for additional resources before they affect productivity.</span></span>

<span data-ttu-id="2699b-115">Ежедневные задачи технического обслуживания помогут команде администраторов определить или установить критерий или базовые показатели для обычных операций системы в рамках организации, а также обнаруживать любую аномальную активность.</span><span class="sxs-lookup"><span data-stu-id="2699b-115">Daily maintenance tasks help the administrative team to define or establish a criteria or baseline for normal systems operations within the organization, and to detect any abnormal activity.</span></span> <span data-ttu-id="2699b-116">Важно реализовать эти ежедневные задачи обслуживания, чтобы участники группы разработчиков могли собирать и поддерживать данные о инфраструктуре Lync Server 2013, такие как уровни использования, возможные узкие места, а также административные изменения.</span><span class="sxs-lookup"><span data-stu-id="2699b-116">It is important to implement these daily maintenance tasks so that the administrative team can capture and maintain data about the Lync Server 2013 infrastructure, such as usage levels, possible performance bottlenecks, and administrative changes.</span></span>

<span data-ttu-id="2699b-117">Для помощи в организации производительности ежедневных задач используйте [контрольный список ежедневных задач](lync-server-2013-operations-checklists.md).</span><span class="sxs-lookup"><span data-stu-id="2699b-117">To help organize the performance of daily tasks, use the [Daily task checklist](lync-server-2013-operations-checklists.md).</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="2699b-118">См. также</span><span class="sxs-lookup"><span data-stu-id="2699b-118">See Also</span></span>


[<span data-ttu-id="2699b-119">Контрольный список ежедневных задач</span><span class="sxs-lookup"><span data-stu-id="2699b-119">Daily task checklist</span></span>](lync-server-2013-operations-checklists.md)  
  

<span data-ttu-id="2699b-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2699b-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

