---
title: 'Lync Server 2013: Системное администрирование'
description: 'Lync Server 2013: Администрирование системы.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: System administration
ms:assetid: 063eb962-b96a-4699-8579-bb7125112df4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720318(v=OCS.15)
ms:contentKeyID: 63969577
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b56271d8d90f1d83072af0577692be1ea0b5bc7e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49400006"
---
# <a name="system-administration-in-lync-server-2013"></a><span data-ttu-id="7f7bc-103">Администрирование системы в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7f7bc-103">System administration in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7f7bc-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7f7bc-104">

<span> </span></span></span>

<span data-ttu-id="7f7bc-105">_**Тема последнего изменения:** 2014-08-18_</span><span class="sxs-lookup"><span data-stu-id="7f7bc-105">_**Topic Last Modified:** 2014-08-18_</span></span>

<span data-ttu-id="7f7bc-106">Администрирование системы включает повседневные административные задачи, как запланированные, так и по запросу, необходимые для обеспечения бесперебойной работы системы.</span><span class="sxs-lookup"><span data-stu-id="7f7bc-106">System administration includes the day-to-day administrative tasks, both planned and on-demand, that are required to keep an IT system operating smoothly.</span></span> <span data-ttu-id="7f7bc-107">Обычно задачи по администрированию системы описаны в разделе написаны письменными процедурами.</span><span class="sxs-lookup"><span data-stu-id="7f7bc-107">Typically, system administration tasks are covered by written procedures.</span></span> <span data-ttu-id="7f7bc-108">Эти процедуры гарантируют, что одни и те же стандартные средства и методы используются всеми сотрудниками службы поддержки.</span><span class="sxs-lookup"><span data-stu-id="7f7bc-108">These procedures help ensure that the same standard tools and methods are used by all support staff.</span></span>

<span data-ttu-id="7f7bc-109">В среде Lync типичные задачи по администрированию системы включают резервное копирование и архивирование пулов, наблюдение за журналами, создание пользователей и управление ими, а также обновление антивирусных программ.</span><span class="sxs-lookup"><span data-stu-id="7f7bc-109">In a Lync environment, typical system administration tasks include backing up and archiving pools, monitoring logs, creating and managing users, and updating antivirus software.</span></span>

<div>

## <a name="system-troubleshooting"></a><span data-ttu-id="7f7bc-110">Устранение неполадок системы</span><span class="sxs-lookup"><span data-stu-id="7f7bc-110">System troubleshooting</span></span>

<span data-ttu-id="7f7bc-111">Организация должна быть готова к работе с непредвиденными проблемами и должна содержать процедуры для управления проблемами с того места, на котором они выводятся до их разрешения.</span><span class="sxs-lookup"><span data-stu-id="7f7bc-111">An organization must be prepared to deal with unexpected issues and should have a procedure to manage issues from the point at which they are reported until their resolution.</span></span> <span data-ttu-id="7f7bc-112">Сведения о том, как сотрудникам службы поддержки удалось выявить и использовать в будущем, чтобы избежать ненужной повторной выполненной работы.</span><span class="sxs-lookup"><span data-stu-id="7f7bc-112">Information about how support staff diagnosed an issue should be recorded and used in the future to avoid unnecessarily repeating completed work.</span></span>

</div>

<div>

## <a name="system-troubleshooting-process"></a><span data-ttu-id="7f7bc-113">Процесс устранения неполадок системы</span><span class="sxs-lookup"><span data-stu-id="7f7bc-113">System troubleshooting process</span></span>

<span data-ttu-id="7f7bc-114">На приведенной ниже схеме показан процесс устранения неполадок системы и взаимодействие с другими ролями операций.</span><span class="sxs-lookup"><span data-stu-id="7f7bc-114">The following diagram shows the system troubleshooting process and the interactions with other operations roles.</span></span>

<span data-ttu-id="7f7bc-115">**Блок-схема устранения неполадок системы**</span><span class="sxs-lookup"><span data-stu-id="7f7bc-115">**System troubleshooting flowchart**</span></span>

<span data-ttu-id="7f7bc-116">![Блок-схема устранения неполадок системы](images/Dn720318.869d0b89-6473-4b1f-9d90-59604b4b8e98(OCS.15).jpg "Блок-схема устранения неполадок системы")</span><span class="sxs-lookup"><span data-stu-id="7f7bc-116">![System Troubleshooting Flowchart](images/Dn720318.869d0b89-6473-4b1f-9d90-59604b4b8e98(OCS.15).jpg "System Troubleshooting Flowchart")</span></span>

  - <span data-ttu-id="7f7bc-117">**Классификация и определение приоритетов**   Эта задача обычно выполняется службой обслуживания.</span><span class="sxs-lookup"><span data-stu-id="7f7bc-117">**Classify and Prioritize**   This task is typically performed by the service desk.</span></span> <span data-ttu-id="7f7bc-118">Например, неполадка может быть сгруппирована как неполадка программного обеспечения или аппаратная ошибка.</span><span class="sxs-lookup"><span data-stu-id="7f7bc-118">For example, an issue may be grouped as a software issue or a hardware issue.</span></span> <span data-ttu-id="7f7bc-119">Затем эта неполадка перенаправляется в соответствующую службу поддержки.</span><span class="sxs-lookup"><span data-stu-id="7f7bc-119">The issue is then routed to the appropriate support team for investigation.</span></span> <span data-ttu-id="7f7bc-120">Правила определения приоритета проблемы, а также время реагирования и времени для разрешения, обычно определяются в соглашении об уровне обслуживания.</span><span class="sxs-lookup"><span data-stu-id="7f7bc-120">The rules for determining the priority of an issue, together with the time to respond and time to resolve, are typically defined in the SLA.</span></span>

  - <span data-ttu-id="7f7bc-121">**Исследование и диагностика**   Подходящая группа поддержки выявит проблему и предложит изменения, которые помогли устранить проблему.</span><span class="sxs-lookup"><span data-stu-id="7f7bc-121">**Investigate and Diagnose**   The appropriate support team diagnoses the issue and proposes changes to resolve the issue.</span></span> <span data-ttu-id="7f7bc-122">Если решение непростое и не требует управления изменениями, решение можно применить немедленно.</span><span class="sxs-lookup"><span data-stu-id="7f7bc-122">If the solution is simple and does not require change control, the solution can be applied immediately.</span></span> <span data-ttu-id="7f7bc-123">Если решение является непростым, должно быть инициировано требование на изменение, и предполагаемые трудозатраты должны управляться процессом управления изменениями, часто под процедурой быстрого отслеживания.</span><span class="sxs-lookup"><span data-stu-id="7f7bc-123">If the solution is not easy, a request for change should be raised and the proposed work should be managed by the change management process, frequently under a “fast-track” procedure.</span></span> <span data-ttu-id="7f7bc-124">Все внесенные изменения следует записать с помощью процесса управления конфигурацией.</span><span class="sxs-lookup"><span data-stu-id="7f7bc-124">Any changes that are made should be recorded using the configuration management process.</span></span>

  - <span data-ttu-id="7f7bc-125">**Закрыть и записать**   После проверки разрешения проблемы необходимо закрыть.</span><span class="sxs-lookup"><span data-stu-id="7f7bc-125">**Close and Record**   After testing the resolution, the issue should be closed.</span></span> <span data-ttu-id="7f7bc-126">Если у вас возникли уроки, которые следует изучить, нужно создать запись в базе знаний.</span><span class="sxs-lookup"><span data-stu-id="7f7bc-126">If there are lessons to be learned from the issue, an entry should be created in the knowledge base.</span></span>

  - <span data-ttu-id="7f7bc-127">**Просмотр и анализ тенденций**   Для выявления тенденций проблем должны быть выполнены периодический анализ недавних вопросов.</span><span class="sxs-lookup"><span data-stu-id="7f7bc-127">**Review and Trend Analysis**   Periodic reviews of recent issues should be performed to identify issue trends.</span></span> <span data-ttu-id="7f7bc-128">Например, если у пользователей часто возникают проблемы с медленным входом на сайты Lync, это может быть вызвано проблемами с пропускной способностью сети.</span><span class="sxs-lookup"><span data-stu-id="7f7bc-128">For example, if the users are experiencing frequent issues with slow logons to their Lync sites, network bandwidth issues may be the cause.</span></span> <span data-ttu-id="7f7bc-129">Разрешение вопросов и их влияние на уровень доступности системы должны проверяться и сравниваться с соглашением об уровне обслуживания.</span><span class="sxs-lookup"><span data-stu-id="7f7bc-129">Issue resolution times and the effect of any outages on system availability should be reviewed and compared with the SLA.</span></span> <span data-ttu-id="7f7bc-130">Человек, liaises с клиентом по вопросам обслуживания (например, диспетчером учетных записей), должен сообщить о каких – либо существенных проблемах.</span><span class="sxs-lookup"><span data-stu-id="7f7bc-130">The person who liaises with the customer on service issues, such as an account manager, should be informed of any significant issues.</span></span>

</div>

<div>

## <a name="issue-management-tools"></a><span data-ttu-id="7f7bc-131">Средства управления проблемами</span><span class="sxs-lookup"><span data-stu-id="7f7bc-131">Issue management tools</span></span>

<span data-ttu-id="7f7bc-132">Средства службы поддержки позволяют сотрудникам записывать, классифицировать и назначать приоритеты для новых проблем.</span><span class="sxs-lookup"><span data-stu-id="7f7bc-132">Service desk tools enable staff to record, classify, and prioritize new issues.</span></span> <span data-ttu-id="7f7bc-133">После этого инструменты рабочего процесса смогут управлять запросом на обслуживание проблем с помощью исследования и диагностики, часто с помощью более одной команды поддержки.</span><span class="sxs-lookup"><span data-stu-id="7f7bc-133">Tools will then provide the workflow processes to manage the issue service request through investigation and diagnosis, often by more than one support team.</span></span> <span data-ttu-id="7f7bc-134">Средства, которые часто предоставляют отчеты о времени разрешения и исторических тенденциях, также могут включать базу данных Knowledge Base, которая может использоваться для поиска в прошлых проблемах.</span><span class="sxs-lookup"><span data-stu-id="7f7bc-134">Tools, which will frequently provide reports about resolution times and historical trends, may also include a knowledge base database, which can be used to search through past issues.</span></span>

<span data-ttu-id="7f7bc-135">Microsoft Knowledge Base — это полезная запись проблем поддержки, обнаруженных корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="7f7bc-135">The Microsoft Knowledge Base is a useful record of support issues that were encountered by Microsoft.</span></span> <span data-ttu-id="7f7bc-136">Дополнительные сведения можно найти на веб-сайте службы поддержки Майкрософт ( <https://go.microsoft.com/fwlink/?linkid=14898> ).</span><span class="sxs-lookup"><span data-stu-id="7f7bc-136">For more information, see the Microsoft Support website (<https://go.microsoft.com/fwlink/?linkid=14898>).</span></span>

<span data-ttu-id="7f7bc-137">Стороннее программное обеспечение обычно требует настройки в соответствии с потребностями Организации, такими как Организация групп, требования к отчетности и меры, необходимые для SLA.</span><span class="sxs-lookup"><span data-stu-id="7f7bc-137">Third-party software typically requires customization to suit the organization’s needs, such as the organization of teams, reporting requirements, and measures required by the SLA.</span></span>

</div>

<div>

## <a name="centralized-vs-decentralized-administration"></a><span data-ttu-id="7f7bc-138">Централизованное или децентрализованное администрирование</span><span class="sxs-lookup"><span data-stu-id="7f7bc-138">Centralized vs. decentralized administration</span></span>

<span data-ttu-id="7f7bc-139">Роли и обязанности по выполнению задач системного администрирования зависят от того, следует ли организациям придерживаться централизованной модели, децентрализованной модели или их комбинации.</span><span class="sxs-lookup"><span data-stu-id="7f7bc-139">Roles and responsibilities for performing system administration tasks depend on whether the organization follows a centralized model, a decentralized model, or a combination of both.</span></span>

  - <span data-ttu-id="7f7bc-140">**Централизованная модель**   В централизованной модели для одной или нескольких административных групп поддерживается полный контроль над всей средой Lync Server.</span><span class="sxs-lookup"><span data-stu-id="7f7bc-140">**Centralized Model**   In a centralized model, one or several administrative groups maintain complete control of the whole Lync Server environment.</span></span> <span data-ttu-id="7f7bc-141">Эта модель администрирования напоминает центр обработки данных, в котором все задачи администрирования выполняются одной группой информационных технологий.</span><span class="sxs-lookup"><span data-stu-id="7f7bc-141">This administrative model resembles a data center where all administration tasks are performed by a single information technology group.</span></span> <span data-ttu-id="7f7bc-142">Роли и обязанности в команде должны определяться в соответствии с опытом и опытом.</span><span class="sxs-lookup"><span data-stu-id="7f7bc-142">Roles and responsibilities within the team should be defined according to experience and expertise.</span></span>

  - <span data-ttu-id="7f7bc-143">**Децентрализованная модель**   Децентрализованные организации размещаются в нескольких географических расположениях и работают с серверами Lync Server и Teams в разных расположениях.</span><span class="sxs-lookup"><span data-stu-id="7f7bc-143">**Decentralized Model**   Decentralized organizations are located in several geographic locations and have functioning Lync Server servers and teams of administrators in different locations.</span></span> <span data-ttu-id="7f7bc-144">Например, для каждой страны или региона может быть локальный сотрудник для администрирования и один или несколько серверов с Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="7f7bc-144">For example, there may be local administration staff and one or more servers that are running Lync Server 2013 for each country/region.</span></span> <span data-ttu-id="7f7bc-145">Возможно также, что у вас есть пул серверов с Lync Server 2013 и административная группа для Северной Америки и One для Европы.</span><span class="sxs-lookup"><span data-stu-id="7f7bc-145">Or, there may be a pool of servers that are running Lync Server 2013 and an administrative team for North America and one for Europe.</span></span> <span data-ttu-id="7f7bc-146">Иногда вам может потребоваться, чтобы администраторы были ответственными только для своей географической зоны и ограничивают разрешения на администрирование ресурсов в других областях.</span><span class="sxs-lookup"><span data-stu-id="7f7bc-146">Sometimes, you may want administrators to be responsible only for their own geographical area and restrict permissions to administer resources in other areas.</span></span>

<span data-ttu-id="7f7bc-147">Кроме того, Lync Server позволяет делегировать конкретные задачи администрирования определенным пользователям или группам с помощью управления доступом на основе ролей (RBAC).</span><span class="sxs-lookup"><span data-stu-id="7f7bc-147">Lync Server also allows you to delegate specific administrative tasks to specific people or groups by using role-based access control (RBAC).</span></span> <span data-ttu-id="7f7bc-148">RBAC позволяет администраторам делегировать определенные права и разрешения пользователей другим администраторам для выполнения подмножества возможных задач администрирования.</span><span class="sxs-lookup"><span data-stu-id="7f7bc-148">RBAC allows administrators to delegate specific user rights and permissions to other administrators to perform a subset of the administrative tasks possible.</span></span> <span data-ttu-id="7f7bc-149">С помощью RBAC пользователи могут выполнять определенные задачи администрирования, зависящие от ролей RBAC, назначенных пользователю.</span><span class="sxs-lookup"><span data-stu-id="7f7bc-149">By using RBAC, the user’s ability to perform specific administrative tasks depends on the RBAC roles that are assigned to the user.</span></span> <span data-ttu-id="7f7bc-150">RBAC предоставляет список командлетов, которые пользователь может запускать на основе ролей RBAC, членом которых является пользователь.</span><span class="sxs-lookup"><span data-stu-id="7f7bc-150">RBAC provides a list of cmdlets that the user can run based on the RBAC roles that the user is a member of.</span></span>

<span data-ttu-id="7f7bc-151"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7f7bc-151"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

