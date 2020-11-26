---
title: Миграция с Office Communications Server 2007 R2 на Lync Server 2013
description: Переход с Office Communications Server 2007 R2 на Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Migration from Office Communications Server 2007 R2 to Lync Server 2013
ms:assetid: f3fa4f5f-e9a2-4fb7-a12d-20f04173e697
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205375(v=OCS.15)
ms:contentKeyID: 48185802
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d0afdc754ae691bc674c200addb9fb97c1eb4199
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446151"
---
# <a name="migration-from-office-communications-server-2007-r2-to-lync-server-2013"></a><span data-ttu-id="f4e1d-103">Миграция с Office Communications Server 2007 R2 на Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f4e1d-103">Migration from Office Communications Server 2007 R2 to Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f4e1d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f4e1d-104">

<span> </span></span></span>

<span data-ttu-id="f4e1d-105">_**Тема последнего изменения:** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="f4e1d-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="f4e1d-106">В этом разделе приведены инструкции по переходу с Office Communications Server 2007 R2 на Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f4e1d-106">The topics in this section guide you through the process of migrating from Office Communications Server 2007 R2 to Lync Server 2013</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="f4e1d-107">В этом документе описаны действия, которые обычно требуются для выполнения каждого этапа миграции.</span><span class="sxs-lookup"><span data-stu-id="f4e1d-107">This document describes the steps generally required to accomplish each phase of migration.</span></span> <span data-ttu-id="f4e1d-108">Она не будет обращаться к каждой возможной топологии устаревшего развертывания или к любому из возможных сценариев миграции.</span><span class="sxs-lookup"><span data-stu-id="f4e1d-108">It does not address every possible legacy deployment topology or every possible migration scenario.</span></span> <span data-ttu-id="f4e1d-109">Таким образом, вам может потребоваться выполнить все описанные выше действия или, возможно, потребуется выполнить дополнительные действия в зависимости от развертывания.</span><span class="sxs-lookup"><span data-stu-id="f4e1d-109">Therefore, you may not need to perform every step described, or you may need to perform additional steps, depending on your deployment.</span></span> <span data-ttu-id="f4e1d-110">В этом документе также приводятся примеры шагов проверки.</span><span class="sxs-lookup"><span data-stu-id="f4e1d-110">This document also provides examples of verification steps.</span></span> <span data-ttu-id="f4e1d-111">Эти шаги проверки предназначены для того, чтобы понять, что необходимо для того, чтобы убедиться в том, что каждый этап прошел успешно по ходу миграции.</span><span class="sxs-lookup"><span data-stu-id="f4e1d-111">These verification steps are provided to help you understand what you need to look for to ensure that each phase completes successfully as you progress through your migration.</span></span> <span data-ttu-id="f4e1d-112">Настройте эти шаги проверки в соответствии с конкретным процессом миграции.</span><span class="sxs-lookup"><span data-stu-id="f4e1d-112">Tailor these verification steps to your specific migration process.</span></span>



</div>

<span data-ttu-id="f4e1d-113">Это руководство содержит сведения, относящиеся к обновлению существующих развертываний.</span><span class="sxs-lookup"><span data-stu-id="f4e1d-113">This guide provides information specific to upgrading your existing deployment.</span></span> <span data-ttu-id="f4e1d-114">В этой статье объясняется, как изменить существующую топологию.</span><span class="sxs-lookup"><span data-stu-id="f4e1d-114">It does not explain how to change your existing topology.</span></span> <span data-ttu-id="f4e1d-115">В этом руководстве не рассматриваются реализации новых функций.</span><span class="sxs-lookup"><span data-stu-id="f4e1d-115">This guide does not cover the implementation of new features.</span></span> <span data-ttu-id="f4e1d-116">Подробное описание процедуры приведено в соответствующем руководстве документа или документа.</span><span class="sxs-lookup"><span data-stu-id="f4e1d-116">When a detailed procedure is documented elsewhere, this guide directs you to the appropriate document or document section.</span></span>

<span data-ttu-id="f4e1d-117">Этот документ определяет условия, указанные в приведенном ниже списке.</span><span class="sxs-lookup"><span data-stu-id="f4e1d-117">This document defines terms as specified in the following list.</span></span>

  - <span data-ttu-id="f4e1d-118">*Перемещение*</span><span class="sxs-lookup"><span data-stu-id="f4e1d-118">*migration*</span></span>  
    <span data-ttu-id="f4e1d-119">Перемещение рабочего развертывания из предыдущей версии Office Communications Server 2007 R2 на Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f4e1d-119">Moving your production deployment from a previous version of Office Communications Server 2007 R2 to Lync Server 2013.</span></span>

<!-- end list -->

  - <span data-ttu-id="f4e1d-120">*Обновление*</span><span class="sxs-lookup"><span data-stu-id="f4e1d-120">*upgrade*</span></span>  
    <span data-ttu-id="f4e1d-121">Установка более новой версии программного обеспечения на сервере или клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="f4e1d-121">Installing a newer version of software on a server or client computer.</span></span>

<!-- end list -->

  - <span data-ttu-id="f4e1d-122">*сосуществование*</span><span class="sxs-lookup"><span data-stu-id="f4e1d-122">*coexistence*</span></span>  
    <span data-ttu-id="f4e1d-123">Временная среда, существующая во время миграции, если некоторые функции были перенесены на Lync Server 2013, а другие функции по-прежнему остаются на ранней версии Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="f4e1d-123">The temporary environment that exists during migration when some functionality has been migrated to Lync Server 2013 and other functionality still remains on a prior version of Office Communications Server 2007 R2.</span></span>

<!-- end list -->

  - <span data-ttu-id="f4e1d-124">*взаимодействия*</span><span class="sxs-lookup"><span data-stu-id="f4e1d-124">*interoperability*</span></span>  
    <span data-ttu-id="f4e1d-125">Развертывание может успешно выполняться в течение периода сосуществования.</span><span class="sxs-lookup"><span data-stu-id="f4e1d-125">The ability of your deployment to operate successfully during the period of coexistence.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="f4e1d-126">Содержание</span><span class="sxs-lookup"><span data-stu-id="f4e1d-126">In This Section</span></span>

  - [<span data-ttu-id="f4e1d-127">Перед началом миграции</span><span class="sxs-lookup"><span data-stu-id="f4e1d-127">Before you begin the migration</span></span>](before-you-begin-the-migration.md)

  - [<span data-ttu-id="f4e1d-128">Этапы миграции</span><span class="sxs-lookup"><span data-stu-id="f4e1d-128">Migration phases</span></span>](migration-phases.md)

  - [<span data-ttu-id="f4e1d-129">Этап 1: планирование перехода с Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="f4e1d-129">Phase 1: Plan your migration from Office Communications Server 2007 R2</span></span>](phase-1-plan-your-migration-from-office-communications-server-2007-r2.md)

  - [<span data-ttu-id="f4e1d-130">Этап 2: подготовка к миграции</span><span class="sxs-lookup"><span data-stu-id="f4e1d-130">Phase 2: Prepare for migration</span></span>](phase-2-prepare-for-migration.md)

  - [<span data-ttu-id="f4e1d-131">Этап 3: развертывание пула Lync Server 2013 Pilot</span><span class="sxs-lookup"><span data-stu-id="f4e1d-131">Phase 3: Deploy Lync Server 2013 pilot pool</span></span>](phase-3-deploy-lync-server-2013-pilot-pool.md)

  - [<span data-ttu-id="f4e1d-132">Этап 4: объединение топологий</span><span class="sxs-lookup"><span data-stu-id="f4e1d-132">Phase 4: Merge topologies</span></span>](phase-4-merge-topologies.md)

  - [<span data-ttu-id="f4e1d-133">Этап 5: Настройка пилотного пула</span><span class="sxs-lookup"><span data-stu-id="f4e1d-133">Phase 5: Configure the pilot pool</span></span>](phase-5-configure-the-pilot-pool.md)

  - [<span data-ttu-id="f4e1d-134">Этап 6: перемещение пользователей в пилотный пул</span><span class="sxs-lookup"><span data-stu-id="f4e1d-134">Phase 6: Move users to the pilot pool</span></span>](phase-6-move-users-to-the-pilot-pool.md)

  - [<span data-ttu-id="f4e1d-135">Этап 7: Добавление сервера Lync Server 2013 EDGE на пилотный пул</span><span class="sxs-lookup"><span data-stu-id="f4e1d-135">Phase 7: Add Lync Server 2013 Edge Server to pilot pool</span></span>](phase-7-add-lync-server-2013-edge-server-to-pilot-pool.md)

  - [<span data-ttu-id="f4e1d-136">Этап 8: переход с пилотного развертывания на рабочий</span><span class="sxs-lookup"><span data-stu-id="f4e1d-136">Phase 8: Move from pilot deployment into production</span></span>](phase-8-move-from-pilot-deployment-into-production.md)

  - [<span data-ttu-id="f4e1d-137">Этап 9: завершение задач после миграции</span><span class="sxs-lookup"><span data-stu-id="f4e1d-137">Phase 9: Complete post-migration tasks</span></span>](phase-9-complete-post-migration-tasks.md)

  - [<span data-ttu-id="f4e1d-138">Этап 10: списание устаревшего сайта</span><span class="sxs-lookup"><span data-stu-id="f4e1d-138">Phase 10: Decommission legacy site</span></span>](phase-10-decommission-legacy-site.md)

<span data-ttu-id="f4e1d-139"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f4e1d-139"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

