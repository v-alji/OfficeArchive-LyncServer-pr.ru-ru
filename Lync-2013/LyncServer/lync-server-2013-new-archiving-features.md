---
title: 'Lync Server 2013: новые функции архивации'
description: 'Lync Server 2013: новые возможности архивации.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: New Archiving features
ms:assetid: c002e367-41ad-498d-9d23-8b117ac435b2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205225(v=OCS.15)
ms:contentKeyID: 48185288
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b5b69c90e62914284f178ae328375c6e350f5b3e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425165"
---
# <a name="new-archiving-features-in-lync-server-2013"></a><span data-ttu-id="f488c-103">Новые функции архивации в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f488c-103">New Archiving features in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f488c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f488c-104">

<span> </span></span></span>

<span data-ttu-id="f488c-105">_**Тема последнего изменения:** 2012-10-09_</span><span class="sxs-lookup"><span data-stu-id="f488c-105">_**Topic Last Modified:** 2012-10-09_</span></span>

<span data-ttu-id="f488c-106">Архивация в Lync Server 2013 может архивировать данные следующих типов:</span><span class="sxs-lookup"><span data-stu-id="f488c-106">Archiving in Lync Server 2013 can archive the following types of content:</span></span>

  - <span data-ttu-id="f488c-107">одноранговые мгновенные сообщения;</span><span class="sxs-lookup"><span data-stu-id="f488c-107">Peer-to-peer instant messages</span></span>

  - <span data-ttu-id="f488c-108">Конференции (собрания), которые являются мгновенными сообщениями с несколькими участниками</span><span class="sxs-lookup"><span data-stu-id="f488c-108">Conferences (meetings) that are multi-party instant messages</span></span>

  - <span data-ttu-id="f488c-109">содержимое конференций, включая загруженное содержимого (например, раздаточные материалы), и связанное с событиями содержание (например, сведения о присоединении, выходе, загрузке, общем доступе и изменениях видимости);</span><span class="sxs-lookup"><span data-stu-id="f488c-109">Conference content, including uploaded content (for example, handouts) and event-related content (for example, joining, leaving, uploading sharing, and changes in visibility)</span></span>

<span data-ttu-id="f488c-110">Кроме того, архивация в Lync Server 2013 предоставляет новые функции, повышающие эффективность развертывания и операций.</span><span class="sxs-lookup"><span data-stu-id="f488c-110">Additionally, Archiving in Lync Server 2013 provides new features that improve deployment and operations efficiency.</span></span> <span data-ttu-id="f488c-111">Эти новые функции состоят из следующих компонентов:</span><span class="sxs-lookup"><span data-stu-id="f488c-111">These new features consist of:</span></span>

  - <span data-ttu-id="f488c-112">**Размещение архивов на серверах переднего плана.**</span><span class="sxs-lookup"><span data-stu-id="f488c-112">**Collocation of Archiving on Front End Servers.**</span></span>   <span data-ttu-id="f488c-113">В Lync Server 2013 отсутствует отдельная роль сервера архивации.</span><span class="sxs-lookup"><span data-stu-id="f488c-113">Lync Server 2013 does not have a separate Archiving Server role.</span></span> <span data-ttu-id="f488c-114">Архивация — это необязательная функция, доступная на всех серверах переднего плана в развертывании Enterprise Edition и на серверах Standard Edition, которые можно реализовать для пула или сайта.</span><span class="sxs-lookup"><span data-stu-id="f488c-114">Archiving is an optional feature available on all Front End Servers in an Enterprise Edition deployment, and on Standard Edition servers, that can be implemented configured for a pool or a site.</span></span>

  - <span data-ttu-id="f488c-115">**Интеграция с Microsoft Exchange.**</span><span class="sxs-lookup"><span data-stu-id="f488c-115">**Microsoft Exchange integration.**</span></span>   <span data-ttu-id="f488c-116">При развертывании архива вы можете интегрировать хранилище данных для архивации с существующим хранилищем Exchange 2013 для всех пользователей, размещенных на сервере Exchange 2013 и почтовых ящиков, которые помещаются на In-Place удержание, поэтому вам не нужно развертывать отдельные базы данных SQL Server для архивации данных Lync.</span><span class="sxs-lookup"><span data-stu-id="f488c-116">When you deploy Archiving, you can integrate data storage for Archiving with your existing Exchange 2013 storage for all users who are homed on Exchange 2013 and have their mailboxes put on In-Place Hold, so you don’t need to deploy separate SQL Server databases to archive Lync data.</span></span> <span data-ttu-id="f488c-117">Если у вас нет развертывания Exchange 2013 или вы предпочитаете не интегрироваться с ним, а если у вас есть пользователи Lync 2013, не размещенные в Exchange 2013 с почтовыми ящиками в In-Place удержание, вы можете развернуть отдельные архивные базы данных с помощью сервера SQL Server, чтобы хранить архивированные данные из Lync Communications.</span><span class="sxs-lookup"><span data-stu-id="f488c-117">If you do not have an Exchange 2013 deployment, or if you prefer not to integrate with it, or if you have any Lync 2013 users who are not homed on Exchange 2013 with their mailboxes put on In-Place Hold, you can deploy separate Archiving databases by using SQL Server to store archived data from Lync communications.</span></span> <span data-ttu-id="f488c-118">Базы данных Microsoft Exchange Integration и Lync Server 2013 можно использовать, если вы хотите использовать интеграцию с Microsoft Exchange для некоторых пользователей в развертывании.</span><span class="sxs-lookup"><span data-stu-id="f488c-118">You can use both Microsoft Exchange integration and Lync Server 2013 Archiving databases if you want to use Microsoft Exchange integration for some but not all users in your deployment.</span></span> <span data-ttu-id="f488c-119">Подробнее о In-Place удержании можно найти в разделе "хранение на месте" [https://go.microsoft.com/fwlink/p/?LinkId=267500](https://go.microsoft.com/fwlink/p/?linkid=267500) .</span><span class="sxs-lookup"><span data-stu-id="f488c-119">For details about In-Place Hold, see “In-Place Hold” at [https://go.microsoft.com/fwlink/p/?LinkId=267500](https://go.microsoft.com/fwlink/p/?linkid=267500).</span></span>

  - <span data-ttu-id="f488c-120">**Зеркальное отображение хранилища SQL.**</span><span class="sxs-lookup"><span data-stu-id="f488c-120">**SQL Store Mirroring.**</span></span>   <span data-ttu-id="f488c-121">При развертывании архивации можно включить зеркальное отображение базы данных SQL Server для базы данных архивации.</span><span class="sxs-lookup"><span data-stu-id="f488c-121">When you deploy Archiving, you can enable SQL Server database mirroring for your Archiving database.</span></span>

  - <span data-ttu-id="f488c-122">**Архивирование досок и опросов.**</span><span class="sxs-lookup"><span data-stu-id="f488c-122">**Archiving of Whiteboards and Polls.**</span></span>   <span data-ttu-id="f488c-123">Архивированное содержимое конференции теперь включает в себя доски и опросы, которые совместно используются во время собрания.</span><span class="sxs-lookup"><span data-stu-id="f488c-123">Archived conference content now includes whiteboards and polls that are shared during the meeting.</span></span>

<span data-ttu-id="f488c-124">Не архивируются следующие типы контента:</span><span class="sxs-lookup"><span data-stu-id="f488c-124">The following types of content are not archived:</span></span>

  - <span data-ttu-id="f488c-125">одноранговые передачи файлов;</span><span class="sxs-lookup"><span data-stu-id="f488c-125">Peer-to-peer file transfers</span></span>

  - <span data-ttu-id="f488c-126">аудио/видео для одноранговых мгновенных сообщений и конференций;</span><span class="sxs-lookup"><span data-stu-id="f488c-126">Audio/video for peer-to-peer instant messages and conferences</span></span>

  - <span data-ttu-id="f488c-127">Общий доступ к приложениям для обмена мгновенными сообщениями и конференц-связи в одноранговой сети</span><span class="sxs-lookup"><span data-stu-id="f488c-127">Application sharing for peer-to-peer instant messages and conferences</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="f488c-128">См. также</span><span class="sxs-lookup"><span data-stu-id="f488c-128">See Also</span></span>


[<span data-ttu-id="f488c-129">Планирование архивации в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f488c-129">Planning for Archiving in Lync Server 2013</span></span>](lync-server-2013-planning-for-archiving.md)  
  

<span data-ttu-id="f488c-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f488c-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

