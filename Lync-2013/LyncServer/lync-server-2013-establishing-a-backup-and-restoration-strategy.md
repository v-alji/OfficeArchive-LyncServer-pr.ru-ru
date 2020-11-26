---
title: 'Lync Server 2013: Установка стратегии резервного копирования и восстановления'
description: 'Lync Server 2013: Установка стратегии резервного копирования и восстановления.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Establishing a backup and restoration strategy
ms:assetid: f545a75f-bbc4-4968-b510-8f6f3920112b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202195(v=OCS.15)
ms:contentKeyID: 51541532
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f4fdefed873d1fd69d82f8ecebceeb92f06f65f7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428470"
---
# <a name="establishing-a-backup-and-restoration-strategy-for-lync-server-2013"></a><span data-ttu-id="529fa-103">Установка стратегии резервного копирования и восстановления для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="529fa-103">Establishing a backup and restoration strategy for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="529fa-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="529fa-104">

<span> </span></span></span>

<span data-ttu-id="529fa-105">_**Тема последнего изменения:** 2013-03-26_</span><span class="sxs-lookup"><span data-stu-id="529fa-105">_**Topic Last Modified:** 2013-03-26_</span></span>

<span data-ttu-id="529fa-106">Прежде чем вы сможете разработать план резервного копирования и восстановления для Lync Server, вам нужно разработать стратегию, которая подходит для целей Организации.</span><span class="sxs-lookup"><span data-stu-id="529fa-106">Before you can develop a backup and restoration plan for Lync Server, you need to develop a strategy that fits with your organization's goals.</span></span> <span data-ttu-id="529fa-107">Чтобы разработать эффективную стратегию резервного копирования и восстановления, вам понадобятся следующие возможности:</span><span class="sxs-lookup"><span data-stu-id="529fa-107">To develop an effective backup and restoration strategy, you will need to:</span></span>

  - <span data-ttu-id="529fa-108">Определите бизнес-приоритеты.</span><span class="sxs-lookup"><span data-stu-id="529fa-108">Establish business priorities.</span></span>

  - <span data-ttu-id="529fa-109">Определите требования к резервному копированию и восстановлению.</span><span class="sxs-lookup"><span data-stu-id="529fa-109">Identify backup and restoration requirements.</span></span>

<div>

## <a name="establishing-business-priorities"></a><span data-ttu-id="529fa-110">Установка бизнес-приоритетов</span><span class="sxs-lookup"><span data-stu-id="529fa-110">Establishing Business Priorities</span></span>

<span data-ttu-id="529fa-111">Оцените бизнес-приоритеты своей организации.</span><span class="sxs-lookup"><span data-stu-id="529fa-111">Evaluate the business priorities of your organization.</span></span> <span data-ttu-id="529fa-112">Обычно основные бизнес-приоритеты, влияющие на стратегию резервного копирования и восстановления, описаны ниже.</span><span class="sxs-lookup"><span data-stu-id="529fa-112">Typically, the primary business priorities that affect your backup and restoration strategy are the following:</span></span>

  - <span data-ttu-id="529fa-113">Требования к бесперебойной работе компании</span><span class="sxs-lookup"><span data-stu-id="529fa-113">Business continuity requirements</span></span>

  - <span data-ttu-id="529fa-114">Полнота данных</span><span class="sxs-lookup"><span data-stu-id="529fa-114">Data completeness</span></span>

  - <span data-ttu-id="529fa-115">Критические данные</span><span class="sxs-lookup"><span data-stu-id="529fa-115">Data criticality</span></span>

  - <span data-ttu-id="529fa-116">Требования к переносимости</span><span class="sxs-lookup"><span data-stu-id="529fa-116">Portability requirements</span></span>

  - <span data-ttu-id="529fa-117">Ограничения затрат</span><span class="sxs-lookup"><span data-stu-id="529fa-117">Cost constraints</span></span>

<span data-ttu-id="529fa-118">Бизнес-потребности, такие как эти сведения помогут вам определить соглашения об уровне обслуживания, разработанные для клиентов.</span><span class="sxs-lookup"><span data-stu-id="529fa-118">Business needs such as these help to determine the service level agreements (SLAs) that you develop with your customers.</span></span> <span data-ttu-id="529fa-119">Соглашение об уровне обслуживания сильно влияет на стратегию резервного копирования и восстановления.</span><span class="sxs-lookup"><span data-stu-id="529fa-119">Service level agreements greatly influence your backup and recovery strategy.</span></span>

</div>

<div>

## <a name="identifying-backup-and-restoration-requirements"></a><span data-ttu-id="529fa-120">Определение требований к резервному копированию и восстановлению</span><span class="sxs-lookup"><span data-stu-id="529fa-120">Identifying Backup and Restoration Requirements</span></span>

<span data-ttu-id="529fa-121">Ваши бизнес-приоритеты и соглашения об уровне обслуживания определяют требования Организации к резервному и восстановлению сервера Lync Server.</span><span class="sxs-lookup"><span data-stu-id="529fa-121">Your business priorities and service level agreements act in determining your organizations' requirements for backing up and restoring Lync Server.</span></span> <span data-ttu-id="529fa-122">Определите и Задокументируйте требования, указанные ниже.</span><span class="sxs-lookup"><span data-stu-id="529fa-122">Identify and document your requirements for the following:</span></span>

  - <span data-ttu-id="529fa-123">**Периодичность архивации**   Подробные сведения о том, как ознакомиться с периодичностью резервного копирования, приведены в разделе рекомендации [по резервному копированию и восстановлению для Lync Server 2013](lync-server-2013-best-practices-for-backup-and-restoration.md).</span><span class="sxs-lookup"><span data-stu-id="529fa-123">**Frequency of backups**   For details about best practices for backup frequency, see [Best practices for backup and restoration for Lync Server 2013](lync-server-2013-best-practices-for-backup-and-restoration.md).</span></span>

  - <span data-ttu-id="529fa-124">**Средства резервного копирования и восстановления**   Включите пользователей, которые должны использовать инструменты, и укажите, какие компьютеры.</span><span class="sxs-lookup"><span data-stu-id="529fa-124">**Backup and restoration tools**   Include who is to use the tools, and on which computers.</span></span> <span data-ttu-id="529fa-125">Сведения о средствах и разрешениях, описанных в этом разделе, и необходимые разрешения описаны в статье [требования к резервному копированию и восстановлению в Lync Server 2013: инструменты и разрешения](lync-server-2013-backup-and-restoration-requirements-tools-and-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="529fa-125">For details about the tools discussed in this topic and necessary permissions, see [Backup and restoration requirements in Lync Server 2013: tools and permissions](lync-server-2013-backup-and-restoration-requirements-tools-and-permissions.md).</span></span>

  - <span data-ttu-id="529fa-126">**Расположение резервной копии**   Определение того, хранятся ли резервные копии локально или удаленно, с учетом безопасности и специальных возможностей.</span><span class="sxs-lookup"><span data-stu-id="529fa-126">**Backup location**   Identify whether the backups are kept locally or remotely, taking security and accessibility into consideration.</span></span> <span data-ttu-id="529fa-127">Укажите носитель, который будет использоваться для резервных копий.</span><span class="sxs-lookup"><span data-stu-id="529fa-127">Specify the media to be used for the backups.</span></span>

  - <span data-ttu-id="529fa-128">**Требования к оборудованию и программному обеспечению**   Определите и задокументируйте особые требования к оборудованию и программному обеспечению, включая оборудование для резервного хранения и восстановление конкретных компонентов, а также любые программы и сетевые подключения, необходимые для поддержки резервного копирования и восстановления.</span><span class="sxs-lookup"><span data-stu-id="529fa-128">**Hardware and software requirements**   Identify and document your specific hardware and software requirements, including the hardware for backup storage and restoration of specific components and any software and network connectivity required to support backup and restoration.</span></span> <span data-ttu-id="529fa-129">По мере разработки требований к оборудованию и программному обеспечению следует помнить о различных сценариях восстановления, которые следуют за этим.</span><span class="sxs-lookup"><span data-stu-id="529fa-129">As you develop your hardware and software requirements, keep in mind the various restoration scenarios that follow.</span></span>

  - <span data-ttu-id="529fa-130">**Сценарии восстановления**   Ниже приведены процедуры восстановления для следующих сценариев:</span><span class="sxs-lookup"><span data-stu-id="529fa-130">**Restoration scenarios**   Here are the restoration processes for the following scenarios:</span></span>
    
      - <span data-ttu-id="529fa-131">Пул Lync Server завершает работу со сбоем.</span><span class="sxs-lookup"><span data-stu-id="529fa-131">A Lync Server pool fails.</span></span> <span data-ttu-id="529fa-132">Для этого сценария необходимо перестраивать каждый сервер в пуле.</span><span class="sxs-lookup"><span data-stu-id="529fa-132">This scenario requires rebuilding each server in the pool.</span></span>
    
      - <span data-ttu-id="529fa-133">Сервер Standard Edition завершается сбоем.</span><span class="sxs-lookup"><span data-stu-id="529fa-133">A Standard Edition server fails.</span></span> <span data-ttu-id="529fa-134">Этот сценарий требует перестройки сервера на новом или очистке компьютера и восстановлении баз данных.</span><span class="sxs-lookup"><span data-stu-id="529fa-134">This scenario requires rebuilding the server on a new or clean computer and restoring databases.</span></span>
    
      - <span data-ttu-id="529fa-135">Потеря хранилища центрального управления.</span><span class="sxs-lookup"><span data-stu-id="529fa-135">Loss of the Central Management store.</span></span> <span data-ttu-id="529fa-136">Как минимум, этот сценарий требует восстановления и публикации хранилища центрального управления.</span><span class="sxs-lookup"><span data-stu-id="529fa-136">At a minimum, this scenario requires restoring and publishing the Central Management store.</span></span>
    
      - <span data-ttu-id="529fa-137">Потеря обратного сервера, когда хранилище Центрального управления продолжает работать нормально.</span><span class="sxs-lookup"><span data-stu-id="529fa-137">Loss of a Back End Server when the Central Management store is still functioning normally.</span></span> <span data-ttu-id="529fa-138">Этот сценарий требует перестройки сервера на новом или очистке компьютера и восстановлении баз данных.</span><span class="sxs-lookup"><span data-stu-id="529fa-138">This scenario requires rebuilding the server on a new or clean computer and restoring databases.</span></span>
    
      - <span data-ttu-id="529fa-139">Сервер, который входит в состав пула Lync Server, завершает работу со сбоем.</span><span class="sxs-lookup"><span data-stu-id="529fa-139">A server that is a member of a Lync Server pool fails.</span></span> <span data-ttu-id="529fa-140">Для этого сценария требуется перестроение сервера на новом или пустом компьютере.</span><span class="sxs-lookup"><span data-stu-id="529fa-140">This scenario requires rebuilding the server on a new or clean computer.</span></span>
    
      - <span data-ttu-id="529fa-141">Не удается сохранить файл.</span><span class="sxs-lookup"><span data-stu-id="529fa-141">A File Store fails.</span></span> <span data-ttu-id="529fa-142">Для этого сценария требуется восстановление файлового сервера или кластера файлов.</span><span class="sxs-lookup"><span data-stu-id="529fa-142">This scenario requires restoring the file server or file cluster.</span></span>
    
      - <span data-ttu-id="529fa-143">Не удается выполнить архивацию, мониторинг или сохраняемость базы данных чата.</span><span class="sxs-lookup"><span data-stu-id="529fa-143">An Archiving, Monitoring, or Persistent Chat database fails.</span></span> <span data-ttu-id="529fa-144">Этот сценарий требует повторного создания баз данных и, если данные важны для Организации, — для восстановления данных.</span><span class="sxs-lookup"><span data-stu-id="529fa-144">This scenario requires recreating the databases, and, if the data is critical to your organization, restoring the data.</span></span> <span data-ttu-id="529fa-145">Архивация, мониторинг и сохраняемые данные чата не требуются для того, чтобы получить доступ к серверу Lync Server и запустить его.</span><span class="sxs-lookup"><span data-stu-id="529fa-145">Archiving, Monitoring, and Persistent Chat data is not required to get Lync Server back up and running.</span></span>

<span data-ttu-id="529fa-146"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="529fa-146"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

