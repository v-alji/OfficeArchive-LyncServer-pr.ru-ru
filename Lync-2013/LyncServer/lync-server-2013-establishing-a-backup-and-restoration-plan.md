---
title: 'Lync Server 2013: создание плана резервного копирования и восстановления'
description: 'Lync Server 2013: Установка плана резервного копирования и восстановления.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Establishing a backup and restoration plan
ms:assetid: 9f562ef1-3804-41e2-b3e4-d45b2e8c63c9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202183(v=OCS.15)
ms:contentKeyID: 51541499
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 06d93c713364bf6b5f230b255b68a2c1dfe1d04a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428463"
---
# <a name="establishing-a-backup-and-restoration-plan-for-lync-server-2013"></a><span data-ttu-id="5eeee-103">Установка плана резервного копирования и восстановления для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5eeee-103">Establishing a backup and restoration plan for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5eeee-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5eeee-104">

<span> </span></span></span>

<span data-ttu-id="5eeee-105">_**Тема последнего изменения:** 2013-02-17_</span><span class="sxs-lookup"><span data-stu-id="5eeee-105">_**Topic Last Modified:** 2013-02-17_</span></span>

<span data-ttu-id="5eeee-106">Создание резервной копии и плана восстановления включает следующие этапы:</span><span class="sxs-lookup"><span data-stu-id="5eeee-106">Creating a backup and restoration plan involves the following steps:</span></span>

  - <span data-ttu-id="5eeee-107">Разработка плана.</span><span class="sxs-lookup"><span data-stu-id="5eeee-107">Developing the plan.</span></span>

  - <span data-ttu-id="5eeee-108">Реализация плана.</span><span class="sxs-lookup"><span data-stu-id="5eeee-108">Implementing the plan.</span></span>

  - <span data-ttu-id="5eeee-109">Обслуживание плана.</span><span class="sxs-lookup"><span data-stu-id="5eeee-109">Maintaining the plan.</span></span>

<div>

## <a name="developing-a-backup-and-restoration-plan"></a><span data-ttu-id="5eeee-110">Разработка плана резервного копирования и восстановления</span><span class="sxs-lookup"><span data-stu-id="5eeee-110">Developing a Backup and Restoration Plan</span></span>

<span data-ttu-id="5eeee-111">После того как вы разрабатываете стратегию резервного копирования и восстановления для Lync Server, используйте ее для документирования подробного плана резервного копирования и восстановления.</span><span class="sxs-lookup"><span data-stu-id="5eeee-111">After you develop your backup and restoration strategy for Lync Server, use it to document a detailed backup and restoration plan.</span></span> <span data-ttu-id="5eeee-112">План должен явным образом передавать приоритеты и требования для резервного копирования данных и параметров.</span><span class="sxs-lookup"><span data-stu-id="5eeee-112">Your plan should clearly convey the priorities and requirements for backing up data and settings.</span></span> <span data-ttu-id="5eeee-113">Вы можете использовать информацию о том, [как создать стратегию резервного копирования и восстановления для Lync server 2013](lync-server-2013-establishing-a-backup-and-restoration-strategy.md) и листы на [листах резервного копирования и восстановления для Lync Server 2013](lync-server-2013-backup-and-restoration-worksheets.md) , чтобы облегчить документирование стратегии.</span><span class="sxs-lookup"><span data-stu-id="5eeee-113">You can use the information in [Establishing a backup and restoration strategy for Lync Server 2013](lync-server-2013-establishing-a-backup-and-restoration-strategy.md) and the worksheets in [Backup and restoration worksheets for Lync Server 2013](lync-server-2013-backup-and-restoration-worksheets.md) to facilitate the documentation of your strategy.</span></span> <span data-ttu-id="5eeee-114">План также должен содержать условия для выбора времени и способа восстановления служб.</span><span class="sxs-lookup"><span data-stu-id="5eeee-114">Your plan should also contain criteria for deciding when and how to restore service.</span></span>

<span data-ttu-id="5eeee-115">По мере разработки плана необходимо учитывать следующие требования:</span><span class="sxs-lookup"><span data-stu-id="5eeee-115">As you develop your plan, you need to consider, and account for, the following:</span></span>

  - <span data-ttu-id="5eeee-116">Как вы будете восстанавливать серверы на новом оборудовании.</span><span class="sxs-lookup"><span data-stu-id="5eeee-116">How you will recover servers on new hardware.</span></span>

  - <span data-ttu-id="5eeee-117">Способ восстановления служб, требующих действия, в составе нескольких бизнес-областей или отделов.</span><span class="sxs-lookup"><span data-stu-id="5eeee-117">How you will recover services that require action on the part of multiple business areas or departments.</span></span>

  - <span data-ttu-id="5eeee-118">Как можно быстро получить резервные серверы.</span><span class="sxs-lookup"><span data-stu-id="5eeee-118">How you can acquire spare servers quickly.</span></span>

  - <span data-ttu-id="5eeee-119">Время, необходимое для восстановления с помощью стратегии.</span><span class="sxs-lookup"><span data-stu-id="5eeee-119">The time it takes to recover by using your strategy.</span></span> <span data-ttu-id="5eeee-120">Рассматривайте требования, предъявляемые в вашей организации, к целевому показателю времени восстановления (RTO).</span><span class="sxs-lookup"><span data-stu-id="5eeee-120">Consider your organization’s requirements for recovery time objective (RTO).</span></span>

<span data-ttu-id="5eeee-121">Измените процедуры резервного копирования и восстановления, описанные в этой статье, чтобы отразить серверы и компоненты в развертывании, добавляя и удаляя необходимые процедуры.</span><span class="sxs-lookup"><span data-stu-id="5eeee-121">Modify the backup and restoration procedures in this topic, adding and deleting procedures as appropriate, to reflect the servers and components in your deployment.</span></span> <span data-ttu-id="5eeee-122">Вы также можете добавить нужные сведения, например расписание резервного копирования, в соответствующие процедуры, чтобы убедиться, что эти сведения не проходили.</span><span class="sxs-lookup"><span data-stu-id="5eeee-122">You can also add appropriate details, such as the backup schedule, to the appropriate procedures to make sure that the information is not overlooked.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="5eeee-123">Рекомендуется создавать сценарии для максимально возможного количества действий, чтобы обеспечить качество и Reproducibility процедур.</span><span class="sxs-lookup"><span data-stu-id="5eeee-123">It is good practice to create scripts for as many steps as possible, to help ensure the quality and reproducibility of procedures.</span></span>



</div>

<span data-ttu-id="5eeee-124">В своем плане укажите, кто является ответственным за просмотр плана, кто отвечает за тестирование и проверку каких – либо новых процедур или средств, а также кто должен утвердить изменения плана и связанных процедур.</span><span class="sxs-lookup"><span data-stu-id="5eeee-124">In your plan, specify who is responsible for reviewing the plan, who is responsible for testing and validating any new procedures or tools, and who must approve any changes to the plan and related procedures.</span></span>

<span data-ttu-id="5eeee-125">Чтобы убедиться в том, что план резервного копирования и восстановления полностью отвечает всем установленным целям и приоритетам, прежде чем приступить к реализации плана, получите утверждение соответствующих ответственных бизнес-решений и ответственных за принятие технических решений в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="5eeee-125">To make sure that your backup and restoration plan fully meets all established goals and priorities, get the approval of the appropriate business decision makers and technical decision makers in your organization before you implement the plan.</span></span>

</div>

<div>

## <a name="implementing-the-backup-and-restoration-plan"></a><span data-ttu-id="5eeee-126">Реализация плана резервного копирования и восстановления</span><span class="sxs-lookup"><span data-stu-id="5eeee-126">Implementing the Backup and Restoration Plan</span></span>

<span data-ttu-id="5eeee-127">Для реализации плана резервного копирования и восстановления необходимо выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="5eeee-127">Implementing a backup and restoration plan requires the following steps:</span></span>

  - <span data-ttu-id="5eeee-128">Тестирование плана и его проверка.</span><span class="sxs-lookup"><span data-stu-id="5eeee-128">Testing and validating the plan.</span></span>

  - <span data-ttu-id="5eeee-129">Связь с планом.</span><span class="sxs-lookup"><span data-stu-id="5eeee-129">Communicating the plan.</span></span>

  - <span data-ttu-id="5eeee-130">Проверка операций резервного копирования и восстановления.</span><span class="sxs-lookup"><span data-stu-id="5eeee-130">Validating backup and restoration operations.</span></span>

<div>

## <a name="testing-and-validating-the-plan"></a><span data-ttu-id="5eeee-131">Тестирование и проверка плана</span><span class="sxs-lookup"><span data-stu-id="5eeee-131">Testing and Validating the Plan</span></span>

<span data-ttu-id="5eeee-132">Описанные здесь процедуры были протестированы и проверены в лабораторной среде.</span><span class="sxs-lookup"><span data-stu-id="5eeee-132">The procedures described here have been tested and validated in a lab environment.</span></span> <span data-ttu-id="5eeee-133">Чтобы убедиться в том, что эти и другие процедуры работают в вашей среде, необходимо проверить и протестировать каждую процедуру, которую вы планируете реализовать.</span><span class="sxs-lookup"><span data-stu-id="5eeee-133">To make sure that these or any other procedures work in your environment, you should test and validate each procedure you intend to implement.</span></span> <span data-ttu-id="5eeee-134">Перед отправкой плана для финального утверждения прополните тестирование и проверку.</span><span class="sxs-lookup"><span data-stu-id="5eeee-134">Complete the testing and the validation before you submit your plan for final approval.</span></span>

</div>

<div>

## <a name="communicating-the-plan"></a><span data-ttu-id="5eeee-135">Связь с планом</span><span class="sxs-lookup"><span data-stu-id="5eeee-135">Communicating the Plan</span></span>

<span data-ttu-id="5eeee-136">В плане резервного копирования и восстановления нужно четко описать, кто реализует процедуры, и пошаговые инструкции по выполнению процедур.</span><span class="sxs-lookup"><span data-stu-id="5eeee-136">Your backup and restoration plan should clearly describe who implements procedures and step-by-step instructions for carrying out the procedures.</span></span> <span data-ttu-id="5eeee-137">Необходимо убедиться, что все, кто несет ответственность за любой аспект резервного копирования и восстановления, понимает план, как его реализация и назначение роли.</span><span class="sxs-lookup"><span data-stu-id="5eeee-137">You should make sure that everyone responsible for any aspect of backup and restoration understands the plan, how it is to be implemented, and what their role is.</span></span> <span data-ttu-id="5eeee-138">Сюда входят все требования к реализации, указанные ниже.</span><span class="sxs-lookup"><span data-stu-id="5eeee-138">This includes all implementation requirements for the following:</span></span>

  - <span data-ttu-id="5eeee-139">Резервное копирование пула и сервера.</span><span class="sxs-lookup"><span data-stu-id="5eeee-139">Pool and server backup.</span></span>

  - <span data-ttu-id="5eeee-140">Восстановление службы.</span><span class="sxs-lookup"><span data-stu-id="5eeee-140">Restoration of service.</span></span>

<span data-ttu-id="5eeee-141">**Резервное копирование пула и сервера**</span><span class="sxs-lookup"><span data-stu-id="5eeee-141">**Pool and server backup**</span></span>

<span data-ttu-id="5eeee-142">План резервного копирования и восстановления должен включать все данные, необходимые для выполнения процедур резервного копирования на постоянной основе.</span><span class="sxs-lookup"><span data-stu-id="5eeee-142">The backup and restoration plan should include all information required to complete backup procedures on an ongoing basis.</span></span> <span data-ttu-id="5eeee-143">К основным сведениям, которые должны быть переданы ответственным участникам группы, относятся следующие:</span><span class="sxs-lookup"><span data-stu-id="5eeee-143">The primary information to be communicated to responsible team members includes the following:</span></span>

  - <span data-ttu-id="5eeee-144">Группа или человек (заданные как индивидуальные пользователи или роли), ответственные за резервное копирование каждого сервера.</span><span class="sxs-lookup"><span data-stu-id="5eeee-144">Team or person (specified as an individual or role) responsible for backing up each server.</span></span>

  - <span data-ttu-id="5eeee-145">Определенные расписания резервного копирования каждого сервера.</span><span class="sxs-lookup"><span data-stu-id="5eeee-145">Specific schedules for backing up each server.</span></span>

  - <span data-ttu-id="5eeee-146">Расположение резервных копий для каждого типа данных (параметры, база данных и файловые ресурсы).</span><span class="sxs-lookup"><span data-stu-id="5eeee-146">Backup locations for each type of data (settings, database, and file shares).</span></span>

  - <span data-ttu-id="5eeee-147">Процедуры резервного копирования, которые необходимо использовать, в том числе инструменты, необходимые для выполнения каждой процедуры.</span><span class="sxs-lookup"><span data-stu-id="5eeee-147">Backup procedures to be used, including the tools required to complete each procedure.</span></span>

  - <span data-ttu-id="5eeee-148">Сведения, необходимые для создания резервных копий, как описано в [книге резервного копирования и восстановления для Lync Server 2013](lync-server-2013-backup-and-restoration-worksheets.md).</span><span class="sxs-lookup"><span data-stu-id="5eeee-148">Information required to complete backups, as covered in [Backup and restoration worksheets for Lync Server 2013](lync-server-2013-backup-and-restoration-worksheets.md).</span></span>

  - <span data-ttu-id="5eeee-149">Методы проверки, которые должны использоваться для обеспечения надлежащей архивации данных и параметров, а также для восстановления, которые могут включать периодические проверки и тестирование восстановлений.</span><span class="sxs-lookup"><span data-stu-id="5eeee-149">Validation methods to be used to help ensure that data and settings are appropriately backed up and available for restoration, which can include periodic audits and test restorations.</span></span>

<span data-ttu-id="5eeee-150">**Восстановление службы**</span><span class="sxs-lookup"><span data-stu-id="5eeee-150">**Restoration of service**</span></span>

<span data-ttu-id="5eeee-151">План резервного копирования и восстановления должен включать все данные, необходимые для восстановления службы, на случай, если один или несколько серверов испытывают убытки, которые делают обслуживание недоступным.</span><span class="sxs-lookup"><span data-stu-id="5eeee-151">The backup and restoration plan should include all information required to restore service, in case one or more servers experience a loss that makes service unavailable.</span></span> <span data-ttu-id="5eeee-152">К основным сведениям, которые должны быть переданы ответственным участникам группы, относятся следующие:</span><span class="sxs-lookup"><span data-stu-id="5eeee-152">The primary information to be communicated to responsible team members includes the following:</span></span>

  - <span data-ttu-id="5eeee-153">Группа или человек (заданные в виде отдельного пользователя или роли), ответственные за определение того, что требуется восстановление службы, и процедуры, которые должны использоваться для восстановления служб, а также группы или сотрудника, ответственные за реализацию процедур для каждого сценария восстановления.</span><span class="sxs-lookup"><span data-stu-id="5eeee-153">Team or person (specified as an individual or a role) that is responsible for determining when restoration of service is required and the procedures to be used to restore service, and also the team or person responsible for implementing procedures for each restoration scenario.</span></span>

  - <span data-ttu-id="5eeee-154">Условия для определения того, какие процедуры восстановления наиболее подходящие для конкретной ситуации.</span><span class="sxs-lookup"><span data-stu-id="5eeee-154">Criteria for determining which restoration procedures are most appropriate for a specific situation.</span></span>

  - <span data-ttu-id="5eeee-155">Оценка времени для восстановления обслуживания и времени восстановления (RTO) в каждом сценарии восстановления.</span><span class="sxs-lookup"><span data-stu-id="5eeee-155">Time estimates for restoration of service and recovery time objective (RTO) in each restoration scenario.</span></span>

  - <span data-ttu-id="5eeee-156">Процедуры восстановления, которые необходимо использовать, в том числе инструменты, необходимые для выполнения каждой процедуры.</span><span class="sxs-lookup"><span data-stu-id="5eeee-156">Restoration procedures to be used, including the tools required to complete each procedure.</span></span>

  - <span data-ttu-id="5eeee-157">Данные, необходимые для восстановления данных и параметров.</span><span class="sxs-lookup"><span data-stu-id="5eeee-157">Information required to restore data and settings.</span></span> <span data-ttu-id="5eeee-158">На [листах резервного копирования и восстановления для Lync Server 2013](lync-server-2013-backup-and-restoration-worksheets.md)доступны листы.</span><span class="sxs-lookup"><span data-stu-id="5eeee-158">Worksheets are provided in [Backup and restoration worksheets for Lync Server 2013](lync-server-2013-backup-and-restoration-worksheets.md).</span></span>

</div>

<div>

## <a name="validating-backup-and-restoration-operations"></a><span data-ttu-id="5eeee-159">Проверка операций резервного копирования и восстановления</span><span class="sxs-lookup"><span data-stu-id="5eeee-159">Validating Backup and Restoration Operations</span></span>

<span data-ttu-id="5eeee-160">После выполнения начальной архивации в производственной среде и через определенные интервалы (в соответствии с планом резервного копирования и восстановления) необходимо проверить следующее:</span><span class="sxs-lookup"><span data-stu-id="5eeee-160">After completing initial backup efforts in your production environment and at specified intervals (as covered in your backup and restoration plan), you should verify the following:</span></span>

  - <span data-ttu-id="5eeee-161">Резервные копии происходят по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="5eeee-161">Backups are occurring as required.</span></span>

  - <span data-ttu-id="5eeee-162">Заархивированные данные и параметры доступны для всех.</span><span class="sxs-lookup"><span data-stu-id="5eeee-162">Backed-up data and settings are accessible.</span></span>

  - <span data-ttu-id="5eeee-163">Процедуры восстановления могут выполняться в рамках целевого значения времени восстановления (RTO), указанного в плане резервного копирования и восстановления, и результаты соответствуют всем бизнес-требованиям.</span><span class="sxs-lookup"><span data-stu-id="5eeee-163">Restoration procedures can be performed within the recovery time objective (RTO) times specified in the backup and restoration plan, and the results meet all business requirements.</span></span>

  - <span data-ttu-id="5eeee-164">Резервные листы загружаются и проверяются и хранятся в безопасном месте.</span><span class="sxs-lookup"><span data-stu-id="5eeee-164">Backup worksheets have been completed and verified, and they are stored in a secure location.</span></span> <span data-ttu-id="5eeee-165">Эти листы содержатся в [книге резервного копирования и восстановления для Lync Server 2013](lync-server-2013-backup-and-restoration-worksheets.md).</span><span class="sxs-lookup"><span data-stu-id="5eeee-165">These worksheets are provided in [Backup and restoration worksheets for Lync Server 2013](lync-server-2013-backup-and-restoration-worksheets.md).</span></span>

  - <span data-ttu-id="5eeee-166">Процедуры восстановления были проверены и проверены на предмет ожидаемых действий, как указано в плане резервного копирования и восстановления.</span><span class="sxs-lookup"><span data-stu-id="5eeee-166">Restoration procedures have been tested and verified to work as expected, as specified in your backup and restoration plan.</span></span>

</div>

</div>

<div>

## <a name="maintaining-the-backup-and-restoration-plan"></a><span data-ttu-id="5eeee-167">Сохранение плана резервного копирования и восстановления</span><span class="sxs-lookup"><span data-stu-id="5eeee-167">Maintaining the Backup and Restoration Plan</span></span>

<span data-ttu-id="5eeee-168">Топология сервера Lync Server — это динамическая среда, которая изменяется в Организации.</span><span class="sxs-lookup"><span data-stu-id="5eeee-168">A Lync Server topology is a dynamic environment that changes with your organization.</span></span> <span data-ttu-id="5eeee-169">Изучите план резервного копирования и восстановления по мере изменения своей организации и периодически проверяйте его, чтобы убедиться, что он продолжает отвечать потребностям вашего бизнеса.</span><span class="sxs-lookup"><span data-stu-id="5eeee-169">Reassess your backup and restoration plan as your organization changes, and review it periodically to make sure that it continues to meet the needs of your business.</span></span>

<span data-ttu-id="5eeee-170"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5eeee-170"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

