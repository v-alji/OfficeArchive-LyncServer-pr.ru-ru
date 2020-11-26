---
title: 'Lync Server 2013: технические требования для архивации'
description: 'Lync Server 2013: технические требования для архивации.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Technical requirements for Archiving
ms:assetid: 896d60e2-be4b-462d-8357-4cd307ab7304
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205059(v=OCS.15)
ms:contentKeyID: 48184732
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6100753ad2c62424eb68c8c258094ba51848170e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423388"
---
# <a name="technical-requirements-for-archiving-in-lync-server-2013"></a><span data-ttu-id="0445d-103">Технические требования для архивации в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0445d-103">Technical requirements for Archiving in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0445d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0445d-104">

<span> </span></span></span>

<span data-ttu-id="0445d-105">_**Тема последнего изменения:** 2012-10-09_</span><span class="sxs-lookup"><span data-stu-id="0445d-105">_**Topic Last Modified:** 2012-10-09_</span></span>

<span data-ttu-id="0445d-106">Технические требования для Lync Server 2013 включают следующее:</span><span class="sxs-lookup"><span data-stu-id="0445d-106">Lync Server 2013 technical requirements include the following:</span></span>

  - <span data-ttu-id="0445d-107">Требования к инфраструктуре.</span><span class="sxs-lookup"><span data-stu-id="0445d-107">Infrastructure requirements.</span></span>

  - <span data-ttu-id="0445d-108">Необходимое программное обеспечение, которое должно быть установлено для архивации.</span><span class="sxs-lookup"><span data-stu-id="0445d-108">Prerequisite software that must be installed for Archiving.</span></span>

  - <span data-ttu-id="0445d-109">Требования к хранилищу данных для архивации.</span><span class="sxs-lookup"><span data-stu-id="0445d-109">Data storage requirements for Archiving.</span></span>

  - <span data-ttu-id="0445d-110">Требования и рекомендации по масштабированию для развертывания архивов.</span><span class="sxs-lookup"><span data-stu-id="0445d-110">Scaling requirements and considerations for your Archiving deployment.</span></span>

  - <span data-ttu-id="0445d-111">Требования к производительности и рекомендации для баз данных архивации.</span><span class="sxs-lookup"><span data-stu-id="0445d-111">Performance requirements and considerations for your Archiving databases.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="0445d-112">Сведения о масштабировании и производительности недоступны в этом выпуске Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0445d-112">Scaling and performance information is not available in this Lync Server 2013 release.</span></span>



</div>

<div>

## <a name="infrastructure-requirements"></a><span data-ttu-id="0445d-113">Требования к инфраструктуре</span><span class="sxs-lookup"><span data-stu-id="0445d-113">Infrastructure Requirements</span></span>

<span data-ttu-id="0445d-114">В Lync Server 2013 для хранения требований к инфраструктуре используется то же самое, что и для развертывания Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0445d-114">Lync Server 2013 Archiving infrastructure requirements are the same as for deployment of Lync Server 2013.</span></span> <span data-ttu-id="0445d-115">Подробности можно найти в разделе [Определение требований инфраструктуры для Lync Server 2013](lync-server-2013-determining-your-infrastructure-requirements.md) в документации по планированию.</span><span class="sxs-lookup"><span data-stu-id="0445d-115">For details, see [Determining your infrastructure requirements for Lync Server 2013](lync-server-2013-determining-your-infrastructure-requirements.md) in the Planning documentation.</span></span>

</div>

<div>

## <a name="archiving-prerequisites"></a><span data-ttu-id="0445d-116">Предварительные требования для архивации</span><span class="sxs-lookup"><span data-stu-id="0445d-116">Archiving Prerequisites</span></span>

<span data-ttu-id="0445d-117">Lync Server 2013 оптимизирует предварительные требования для архивации из-за указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="0445d-117">Lync Server 2013 streamlines prerequisites for Archiving because of the following:</span></span>

  - <span data-ttu-id="0445d-118">Сервер архивации больше не является ролью сервера.</span><span class="sxs-lookup"><span data-stu-id="0445d-118">Archiving Server is no longer a server role.</span></span> <span data-ttu-id="0445d-119">Вместо этого агенты Объединенного сбора данных выполняются на серверах переднего плана и серверах стандартных выпусков, чтобы захватывать данные для архивации, чтобы не настраивать отдельные системные платформы для архивации.</span><span class="sxs-lookup"><span data-stu-id="0445d-119">Instead, Unified Data Collection Agents run on the Front End Servers in a pool and Standard Edition servers to capture data for Archiving, so you do not set up separate system platforms for Archiving.</span></span>

  - <span data-ttu-id="0445d-120">При архивации используется хранилище файлов Lync Server 2013 для временного хранения файлов содержимого собрания, поэтому вы не настраиваете отдельное хранилище файлов для архивации.</span><span class="sxs-lookup"><span data-stu-id="0445d-120">Archiving uses the Lync Server 2013 file storage for temporary storage of meeting content files, so you do not set up a separate file store for archiving.</span></span>

  - <span data-ttu-id="0445d-121">В Lync Server 2013 очередь сообщений не требуется.</span><span class="sxs-lookup"><span data-stu-id="0445d-121">In Lync Server 2013, Message Queuing is not required.</span></span>

</div>

<div>

## <a name="data-storage-requirements-for-archiving"></a><span data-ttu-id="0445d-122">Требования к хранилищу данных для архивации</span><span class="sxs-lookup"><span data-stu-id="0445d-122">Data Storage Requirements for Archiving</span></span>

<span data-ttu-id="0445d-123">Кроме того, необходимо настроить инфраструктуру хранения архивов.</span><span class="sxs-lookup"><span data-stu-id="0445d-123">Additionally, you need to set up the infrastructure for Archiving storage.</span></span> <span data-ttu-id="0445d-124">Сюда относятся один или оба следующих варианта:</span><span class="sxs-lookup"><span data-stu-id="0445d-124">This includes one or both of the following:</span></span>

  - <span data-ttu-id="0445d-125">**Хранилище Microsoft Exchange**.</span><span class="sxs-lookup"><span data-stu-id="0445d-125">**Microsoft Exchange storage**.</span></span> <span data-ttu-id="0445d-126">Файлы содержимого собраний, например презентации PowerPoint, архивируются как вложения.</span><span class="sxs-lookup"><span data-stu-id="0445d-126">Meeting content files, such as PowerPoint presentations, are archived as attachments.</span></span> <span data-ttu-id="0445d-127">Если вы хотите использовать интеграцию с Microsoft Exchange, чтобы данные архива Lync хранились с данными о соответствиях Exchange, необходимо использовать Exchange 2013 для развертывания Exchange и убедиться в том, что максимальный размер хранилища поддерживает хранение файлов содержимого собраний.</span><span class="sxs-lookup"><span data-stu-id="0445d-127">If you want to use Microsoft Exchange integration so that Lync archive data is stored with Exchange compliance data, you must use Exchange 2013 for your Exchange deployment and ensure that the maximum storage size supports storage of the meeting content files.</span></span> <span data-ttu-id="0445d-128">Если вы разворачиваете архивацию с помощью параметра интеграции Microsoft Exchange, архивные данные Lync сохраняются с данными соответствия требованиям Exchange 2013 только для пользователей, которые размещены на серверах Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="0445d-128">If you deploy Archiving using the Microsoft Exchange integration option, Lync archive data is stored with Exchange 2013 compliance data only for the users who are homed on your Exchange 2013 servers.</span></span> <span data-ttu-id="0445d-129">Перед развертыванием и включением архивации с помощью параметра интеграции Microsoft Exchange необходимо развернуть Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="0445d-129">You must deploy Exchange 2013 prior to deploying and enabling Archiving using the Microsoft Exchange integration option.</span></span> <span data-ttu-id="0445d-130">Если вы решили использовать хранилище Exchange 2013, вам не нужно развертывать отдельные базы данных SQL Server для архивации, если только у вас нет пользователей Lync на серверах Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="0445d-130">If you choose to use Exchange 2013 storage, you do not need to deploy separate SQL Server databases for Archiving, unless you have Lync users who are not homed on your Exchange 2013 servers.</span></span>

  - <span data-ttu-id="0445d-131">**Хранилище базы данных SQL Server для архивации**.</span><span class="sxs-lookup"><span data-stu-id="0445d-131">**SQL Server database storage for Archiving**.</span></span> <span data-ttu-id="0445d-132">Для поддержки пользователей, не использующих серверы Exchange 2013, или если вы не хотите использовать параметр интеграции Microsoft Exchange, необходимо развернуть хранилище архивации с помощью базы данных SQL Server.</span><span class="sxs-lookup"><span data-stu-id="0445d-132">To support users who are not homed on Exchange 2013 servers, or if you do not want to use the Microsoft Exchange integration option, you must deploy Archiving storage using a SQL Server database.</span></span> <span data-ttu-id="0445d-133">Lync Server 2013 поддерживает следующие 64-разрядные версии SQL Server:</span><span class="sxs-lookup"><span data-stu-id="0445d-133">Lync Server 2013 supports the following 64-bit versions of SQL Server:</span></span>
    
      - <span data-ttu-id="0445d-134">Microsoft SQL Server 2008 R2 Enterprise</span><span class="sxs-lookup"><span data-stu-id="0445d-134">Microsoft SQL Server 2008 R2 Enterprise</span></span>
    
      - <span data-ttu-id="0445d-135">Microsoft SQL Server 2008 R2 Standard</span><span class="sxs-lookup"><span data-stu-id="0445d-135">Microsoft SQL Server 2008 R2 Standard</span></span>
    
      - <span data-ttu-id="0445d-136">Microsoft SQL Server 2012 корпоративный</span><span class="sxs-lookup"><span data-stu-id="0445d-136">Microsoft SQL Server 2012 Enterprise</span></span>
    
      - <span data-ttu-id="0445d-137">Microsoft SQL Server 2012 Standard</span><span class="sxs-lookup"><span data-stu-id="0445d-137">Microsoft SQL Server 2012 Standard</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="0445d-138">Microsoft SQL Server 2008 R2 Express и Microsoft SQL Server 2012 Express не поддерживают архивацию.</span><span class="sxs-lookup"><span data-stu-id="0445d-138">Microsoft SQL Server 2008 R2 Express and Microsoft SQL Server 2012 Express are not supported for Archiving.</span></span> <span data-ttu-id="0445d-139">32-разрядные версии SQL Server не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="0445d-139">32-bit versions of SQL Server are not supported.</span></span> <span data-ttu-id="0445d-140">Дополнительные требования и ограничения SQL Server можно найти в разделе <A href="lync-server-2013-database-software-support.md">Поддержка программного обеспечения баз данных в Lync Server 2013</A> в документации по планированию или в документации по поддержке.</span><span class="sxs-lookup"><span data-stu-id="0445d-140">For additional SQL Server requirements and restrictions, see <A href="lync-server-2013-database-software-support.md">Database software support in Lync Server 2013</A> in the Planning documentation or in the Supportability documentation.</span></span>

    
    </div>
    
    <span data-ttu-id="0445d-141">Перед развертыванием и включением архивации необходимо настроить платформы SQL Server.</span><span class="sxs-lookup"><span data-stu-id="0445d-141">You must set up the SQL Server platforms prior to deploying and enabling Archiving.</span></span> <span data-ttu-id="0445d-142">Если учетная запись, которую планируется использовать для публикации топологии, имеет соответствующие права и разрешения администратора, базу данных архивации (LcsLog) можно создать при публикации топологии.</span><span class="sxs-lookup"><span data-stu-id="0445d-142">If the account to be used to publish the topology has the appropriate administrator rights and permissions, you can create the Archiving database (LcsLog) when you publish your topology.</span></span> <span data-ttu-id="0445d-143">Кроме того, вы можете создать базу данных позже, в том числе в ходе процедуры установки.</span><span class="sxs-lookup"><span data-stu-id="0445d-143">You can also create the database later, including as part of the installation procedure.</span></span> <span data-ttu-id="0445d-144">Подробные сведения о SQL Server можно найти в центре SQL Server TechCenter по адресу [https://go.microsoft.com/fwlink/p/?linkID=129045](https://go.microsoft.com/fwlink/p/?linkid=129045) .</span><span class="sxs-lookup"><span data-stu-id="0445d-144">For details about SQL Server, see the SQL Server TechCenter at [https://go.microsoft.com/fwlink/p/?linkID=129045](https://go.microsoft.com/fwlink/p/?linkid=129045).</span></span>

<span data-ttu-id="0445d-145"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0445d-145"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

