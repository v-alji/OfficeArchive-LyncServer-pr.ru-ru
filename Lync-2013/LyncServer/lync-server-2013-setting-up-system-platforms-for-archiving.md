---
title: 'Lync Server 2013: Настройка системных платформ для архивации'
description: 'Lync Server 2013: Настройка системных платформ для архивации.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up system platforms for Archiving
ms:assetid: 2df40fdf-0e32-46d4-9fb2-1ce1d7bfa328
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204768(v=OCS.15)
ms:contentKeyID: 48183716
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2f210083451ae8fcb87c53e52b5512de6f1f18d0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441678"
---
# <a name="setting-up-system-platforms-for-archiving-in-lync-server-2013"></a><span data-ttu-id="aeba1-103">Настройка системных платформ для архивации в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="aeba1-103">Setting up system platforms for Archiving in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="aeba1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="aeba1-104">

<span> </span></span></span>

<span data-ttu-id="aeba1-105">_**Тема последнего изменения:** 2012-10-09_</span><span class="sxs-lookup"><span data-stu-id="aeba1-105">_**Topic Last Modified:** 2012-10-09_</span></span>

<span data-ttu-id="aeba1-106">Прежде чем приступать к развертыванию архива, необходимо установить требуемую операционную систему и любое другое необходимое программное обеспечение на оборудовании, удовлетворяющем требованиям к системе.</span><span class="sxs-lookup"><span data-stu-id="aeba1-106">Before starting the deployment of Archiving, you must install the required operating system and any other prerequisite software on hardware that meets system requirements:</span></span>

  - <span data-ttu-id="aeba1-107">**Платформа Lync Server 2013**   У развертываний Lync Server 2013 нет серверов архивации.</span><span class="sxs-lookup"><span data-stu-id="aeba1-107">**Lync Server 2013 platform**   Lync Server 2013 deployments do not have Archiving Servers.</span></span> <span data-ttu-id="aeba1-108">Вместо этого агенты сбора данных Объединенные данные выполняются на серверах переднего плана и серверах стандартных выпусков для сбора данных для архивации, поэтому для размещения архивации не требуется отдельная системная платформа.</span><span class="sxs-lookup"><span data-stu-id="aeba1-108">Instead, Unified Data Collection Agents run on Front End Servers and Standard Edition servers to capture data for archiving, so no separate system platform is required to host Archiving.</span></span>

  - <span data-ttu-id="aeba1-109">**Платформа для хранения данных**   В Lync Server 2013 вы можете хранить данные с помощью одного из указанных ниже вариантов.</span><span class="sxs-lookup"><span data-stu-id="aeba1-109">**Data storage platform**   In Lync Server 2013, you can store data by using either of the following:</span></span>
    
      - <span data-ttu-id="aeba1-110">**Интеграция с Microsoft Exchange**   Если вы хотите сохранить данные архивации в Lync Server 2013 с помощью развертывания Exchange 2013, вместо или в дополнение к настройке отдельной базы данных для хранения данных архивации, необходимо, чтобы в среде развертывания Exchange была установлена версия Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="aeba1-110">**Microsoft Exchange integration**   If you want to store Lync Server 2013 Archiving data by using your Exchange 2013 deployment, instead of or in addition to setting up a separate database for storage of Archiving data, your Exchange deployment must be running Exchange 2013.</span></span> <span data-ttu-id="aeba1-111">Подробные сведения о настройке системных платформ для Exchange 2013 можно найти в документации по продукту Exchange.</span><span class="sxs-lookup"><span data-stu-id="aeba1-111">For details about setting up system platforms for Exchange 2013, see the Exchange product documentation.</span></span>
    
      - <span data-ttu-id="aeba1-112">**Сервер SQL Server**   Если вы хотите использовать отдельную базу данных SQL Server для хранения данных для архивации, вместо или помимо использования интеграции с Microsoft Exchange необходимо настроить платформу системы для базы данных перед развертыванием архивации.</span><span class="sxs-lookup"><span data-stu-id="aeba1-112">**SQL Server**   If you want to use a separate SQL Server database for storage of archiving data, instead of or in addition to using Microsoft Exchange integration, you must set up the system platform for the database prior to deployment of Archiving.</span></span> <span data-ttu-id="aeba1-113">Конкретные требования к системной платформе зависят от того, используете ли вы Microsoft SQL Server 2008 R2 или Microsoft SQL Server 2012 для базы данных архивирования.</span><span class="sxs-lookup"><span data-stu-id="aeba1-113">The specific system platform requirements depend on whether you use Microsoft SQL Server 2008 R2 or Microsoft SQL Server 2012 for the Archiving database.</span></span> <span data-ttu-id="aeba1-114">Подробные сведения о настройке системных платформ для этих баз данных можно найти в документации по продукту Microsoft SQL Server 2008 R2 и Microsoft SQL Server 2012.</span><span class="sxs-lookup"><span data-stu-id="aeba1-114">For details about setting up system platforms for these databases, see the Microsoft SQL Server 2008 R2 and Microsoft SQL Server 2012 product documentation.</span></span>

  - <span data-ttu-id="aeba1-115">**Платформа файлового сервера**   Lync Server 2013 хранит архивные файлы Lync Server в том же расположении, которое вы указали для хранения файлов при настройке серверов переднего плана или стандартных серверов выпусков.</span><span class="sxs-lookup"><span data-stu-id="aeba1-115">**File server platform**   Lync Server 2013 stores Lync Server archiving files in the same location that you specify for file storage when you set up your Front End Servers or Standard Edition servers.</span></span> <span data-ttu-id="aeba1-116">Вы не можете указать отдельное расположение для хранения файлов, поэтому для архивации файлов не требуется отдельная системная платформа.</span><span class="sxs-lookup"><span data-stu-id="aeba1-116">You cannot specify a separate location for archiving file storage, so no separate system platform is required for Archiving file storage.</span></span> <span data-ttu-id="aeba1-117">Если вы используете Microsoft Exchange Integration, Exchange 2013 файлы для архивации данных Lync хранятся на серверах Exchange 2013 для пользователей, использующих эти серверы Exchange.</span><span class="sxs-lookup"><span data-stu-id="aeba1-117">If you use Microsoft Exchange integration, Exchange 2013 the files for archived Lync communications are stored on Exchange 2013 servers for users homed on those Exchange servers.</span></span>

<span data-ttu-id="aeba1-118"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="aeba1-118"></div>

<span> </span>

</div>

</div>

</span></span></div>

