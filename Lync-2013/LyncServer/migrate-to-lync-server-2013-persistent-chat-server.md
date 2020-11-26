---
title: Миграция с групповой беседы в Lync Server 2010 или Office Communications Server 2007 R2 на сервер сохраняемого сеанса беседы в Lync Server 2013
description: Миграция с Lync Server 2010, группового чата или Office Communications Server 2007 R2 Group Chat на Lync Server 2013 и на сервер сохраняемого чата.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Migration from Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat to Lync Server 2013, Persistent Chat Server
ms:assetid: 5b4d3db1-6eba-4932-b49c-f60bcf9488f9
ms:mtpsurl: https://technet.microsoft.com/library/Gg615442(v=OCS.15)
ms:contentKeyID: 48184240
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6090d5924a203a960444d9a10700fd178d038887
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446859"
---
# <a name="migration-from-lync-server-2010-group-chat-or-office-communications-server-2007-r2-group-chat-to-lync-server-2013-persistent-chat-server"></a><span data-ttu-id="fd9ac-103">Миграция с групповой беседы в Lync Server 2010 или Office Communications Server 2007 R2 на сервер сохраняемого сеанса беседы в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fd9ac-103">Migration from Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat to Lync Server 2013, Persistent Chat Server</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fd9ac-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fd9ac-104">

<span> </span></span></span>

<span data-ttu-id="fd9ac-105">_**Тема последнего изменения:** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="fd9ac-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="fd9ac-106">В этом разделе приведены инструкции по переносу сервера Lync Server 2010, группового чата или Office Communications Server 2007 R2 Group Chat на Lync Server 2013 и на сервер сохраняемого чата.</span><span class="sxs-lookup"><span data-stu-id="fd9ac-106">The topics in this section guide you through the process of migrating either Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat to Lync Server 2013, Persistent Chat Server.</span></span> <span data-ttu-id="fd9ac-107">Если вы планируете совместное развертывание сервера Lync Server 2013, то вы можете разговаривать с сервером Lync Server 2010, групповой чат или Office Communications Server 2007 R2 Group Chat, это руководство также содержит некоторые важные сведения для работы в этой смешанной среде.</span><span class="sxs-lookup"><span data-stu-id="fd9ac-107">If you intend for your Lync Server 2013, Persistent Chat Server deployment to coexist with a Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat deployment, this guide also includes some essential information for operating in this mixed environment.</span></span> <span data-ttu-id="fd9ac-108">Это руководство главным образом посвящено миграции данных на сохраняемом сервере чата.</span><span class="sxs-lookup"><span data-stu-id="fd9ac-108">This guide primarily focuses on data migration for Persistent Chat Server.</span></span> <span data-ttu-id="fd9ac-109">Для пользователей, которые переходят с устаревших версий Lync Server на Lync Server 2013, ознакомьтесь с разрешениями [Переход с Lync server 2010 на Lync server 2013](migration-from-lync-server-2010-to-lync-server-2013.md) и [Переход с Office Communications Server 2007 R2 на Lync Server 2013](migration-from-office-communications-server-2007-r2-to-lync-server-2013.md).</span><span class="sxs-lookup"><span data-stu-id="fd9ac-109">For users who are migrating from legacy versions of Lync Server to Lync Server 2013, see [Migration from Lync Server 2010 to Lync Server 2013](migration-from-lync-server-2010-to-lync-server-2013.md) and [Migration from Office Communications Server 2007 R2 to Lync Server 2013](migration-from-office-communications-server-2007-r2-to-lync-server-2013.md).</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="fd9ac-110">В этой статье предполагается, что вы уже установили Lync Server 2013 в сосуществовании с помощью Lync Server 2010 или Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="fd9ac-110">This topic assumes that you have already installed Lync Server 2013 in coexistence with Lync Server 2010 or Office Communications Server 2007 R2.</span></span>



</div>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="fd9ac-111">В этом руководстве описаны действия, которые обычно требуются для выполнения каждого этапа миграции.</span><span class="sxs-lookup"><span data-stu-id="fd9ac-111">This guide describes the steps generally required to accomplish each phase of migration.</span></span> <span data-ttu-id="fd9ac-112">Она не будет обращаться к каждой возможной топологии устаревшего развертывания или к любому из возможных сценариев миграции.</span><span class="sxs-lookup"><span data-stu-id="fd9ac-112">It does not address every possible legacy deployment topology or every possible migration scenario.</span></span> <span data-ttu-id="fd9ac-113">Таким образом, вам может потребоваться выполнить все описанные выше шаги или, возможно, потребуется выполнить дополнительные действия в зависимости от развертывания.</span><span class="sxs-lookup"><span data-stu-id="fd9ac-113">Therefore, you may not need to perform every step that is described, or you may need to perform additional steps, depending on your deployment.</span></span> <span data-ttu-id="fd9ac-114">В руководстве также приводятся примеры шагов проверки.</span><span class="sxs-lookup"><span data-stu-id="fd9ac-114">The guide also provides examples of verification steps.</span></span> <span data-ttu-id="fd9ac-115">Эти шаги проверки предназначены для того, чтобы понять, что нужно сделать, чтобы убедиться в том, что каждый этап завершается успешно по ходу миграции.</span><span class="sxs-lookup"><span data-stu-id="fd9ac-115">These verification steps are provided to help you understand what you need to look for to be sure that each phase completes successfully as you progress through your migration.</span></span> <span data-ttu-id="fd9ac-116">Вы можете изменить эти шаги проверки в процессе миграции.</span><span class="sxs-lookup"><span data-stu-id="fd9ac-116">You can modify these verification steps to your specific migration process.</span></span>



</div>

<span data-ttu-id="fd9ac-117">Это руководство содержит сведения, относящиеся к обновлению существующих развертываний.</span><span class="sxs-lookup"><span data-stu-id="fd9ac-117">This guide provides information specific to upgrading your existing deployment.</span></span> <span data-ttu-id="fd9ac-118">В этой статье объясняется, как изменить существующую топологию.</span><span class="sxs-lookup"><span data-stu-id="fd9ac-118">It does not explain how to change your existing topology.</span></span> <span data-ttu-id="fd9ac-119">В этом руководстве не рассматриваются реализации новых функций.</span><span class="sxs-lookup"><span data-stu-id="fd9ac-119">This guide does not cover the implementation of new features.</span></span> <span data-ttu-id="fd9ac-120">Подробное описание процедуры приведено в соответствующем руководстве документа или документа.</span><span class="sxs-lookup"><span data-stu-id="fd9ac-120">When a detailed procedure is documented elsewhere, this guide directs you to the appropriate document or document section.</span></span>

<span data-ttu-id="fd9ac-121">Этот документ определяет условия, указанные в приведенном ниже списке.</span><span class="sxs-lookup"><span data-stu-id="fd9ac-121">This document defines terms as specified in the following list.</span></span>

  - <span data-ttu-id="fd9ac-122">*Перемещение*</span><span class="sxs-lookup"><span data-stu-id="fd9ac-122">*migration*</span></span>  
    <span data-ttu-id="fd9ac-123">Перемещение развертывания из предыдущей версии сервера сохраняемого чата, прежнее название — сервер группового чата, в Lync Server 2013, сервер сохраняемого чата.</span><span class="sxs-lookup"><span data-stu-id="fd9ac-123">Moving your deployment from a previous version of Persistent Chat Server, formerly known as Group Chat Server, to Lync Server 2013, Persistent Chat Server.</span></span>

<!-- end list -->

  - <span data-ttu-id="fd9ac-124">*Обновление*</span><span class="sxs-lookup"><span data-stu-id="fd9ac-124">*upgrade*</span></span>  
    <span data-ttu-id="fd9ac-125">Установка более новой версии программного обеспечения на сервере или клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="fd9ac-125">Installing a newer version of software on a server or client computer.</span></span>

<!-- end list -->

  - <span data-ttu-id="fd9ac-126">*сосуществование*</span><span class="sxs-lookup"><span data-stu-id="fd9ac-126">*coexistence*</span></span>  
    <span data-ttu-id="fd9ac-127">Временная среда, существующая во время миграции, когда некоторые функции были перенесены на Lync Server 2013, сервер сохраняемого чата и другие функции по-прежнему остаются в предыдущей версии сервера группового чата.</span><span class="sxs-lookup"><span data-stu-id="fd9ac-127">The temporary environment that exists during migration, when some functionality has been migrated to Lync Server 2013, Persistent Chat Server, and other functionality still remains on a prior version of Group Chat Server.</span></span>

<span data-ttu-id="fd9ac-128">Сервер сохраняемого чата является расширением инфраструктуры Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="fd9ac-128">Persistent Chat Server is an extension of the Lync Server 2013 infrastructure.</span></span> <span data-ttu-id="fd9ac-129">В зависимости от вашей топологии вы можете перенести Lync Server 2010, групповой чат или Office Communications Server 2007 R2 Group Chat на сервер Lync Server 2013 для сохраняемого сервера чата.</span><span class="sxs-lookup"><span data-stu-id="fd9ac-129">Depending on your topology, you can migrate Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat to Lync Server 2013 Persistent Chat Server.</span></span> <span data-ttu-id="fd9ac-130">Подробные сведения о доступных топологиях, требования к техническим и программному обеспечению для миграции сервера группового чата, приведены в разделе [планирование сохраняемого сервера чата в Lync server 2013](lync-server-2013-planning-for-persistent-chat-server.md) в документации по планированию.</span><span class="sxs-lookup"><span data-stu-id="fd9ac-130">For details about available topologies and the technical and software requirements for migrating Group Chat Server, see [Planning for Persistent Chat Server in Lync Server 2013](lync-server-2013-planning-for-persistent-chat-server.md) in the Planning documentation.</span></span>

<span data-ttu-id="fd9ac-131">Если ваша организация требует поддержки соответствия требованиям, она будет автоматически устанавливаться вместе с каждым сервером в каждом из этих сохраненных чатов.</span><span class="sxs-lookup"><span data-stu-id="fd9ac-131">If your organization requires compliance support, it is now automatically installed with each Persistent Chat Server.</span></span> <span data-ttu-id="fd9ac-132">Отдельный сервер больше не нужен для соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="fd9ac-132">A separate server is no longer needed for compliance.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="fd9ac-133">Для обеспечения безопасности файловой системы необходимо установить сохраняемый сервер чата в файловой системе NTFS.</span><span class="sxs-lookup"><span data-stu-id="fd9ac-133">Persistent Chat Server must be installed on an NTFS file system to help enforce file system security.</span></span> <span data-ttu-id="fd9ac-134">Файловая система FAT32 не поддерживается для сервера сохраняемого чата.</span><span class="sxs-lookup"><span data-stu-id="fd9ac-134">FAT32 is not a supported file system for Persistent Chat Server.</span></span><BR><span data-ttu-id="fd9ac-135">Если ваша организация требует поддержки соответствия требованиям, она будет автоматически устанавливаться вместе с каждым сервером в каждом из этих сохраненных чатов.</span><span class="sxs-lookup"><span data-stu-id="fd9ac-135">If your organization requires compliance support, it is now automatically installed with each Persistent Chat Server.</span></span> <span data-ttu-id="fd9ac-136">Отдельный сервер больше не нужен для соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="fd9ac-136">A separate server is no longer needed for compliance.</span></span> <span data-ttu-id="fd9ac-137">Дополнительные сведения об изменениях, внесенных в Lync Server 2013 &nbsp; , можно найти в разделе <A href="lync-server-2013-new-persistent-chat-server-features.md">новые функции сервера сохраняемого чата в lync Server 2013</A> в документации "Приступая к работе".</span><span class="sxs-lookup"><span data-stu-id="fd9ac-137">For more details about changes in Lync Server 2013&nbsp;Persistent Chat Server, see <A href="lync-server-2013-new-persistent-chat-server-features.md">New Persistent Chat Server features in Lync Server 2013</A> in the Getting Started documentation.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="fd9ac-138">Содержание</span><span class="sxs-lookup"><span data-stu-id="fd9ac-138">In This Section</span></span>

  - [<span data-ttu-id="fd9ac-139">Стандартный сценарий миграции — высокоуровневый</span><span class="sxs-lookup"><span data-stu-id="fd9ac-139">Standard migration scenario - high-level</span></span>](standard-migration-scenario-high-level.md)

  - [<span data-ttu-id="fd9ac-140">Процесс миграции — сведения</span><span class="sxs-lookup"><span data-stu-id="fd9ac-140">Migration process - details</span></span>](migration-process-details.md)

  - [<span data-ttu-id="fd9ac-141">Замечания по сосуществованию</span><span class="sxs-lookup"><span data-stu-id="fd9ac-141">Coexistence considerations</span></span>](coexistence-considerations.md)

<span data-ttu-id="fd9ac-142"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fd9ac-142"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

