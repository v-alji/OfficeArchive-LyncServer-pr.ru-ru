---
title: Перенос серверов архивирования и мониторинга
description: Перенос серверов архивации и мониторинга.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migrating Archiving and Monitoring servers
ms:assetid: 77831579-df45-4697-b8c5-207b74a07a40
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205015(v=OCS.15)
ms:contentKeyID: 48184550
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2dabd16fd38dbf463a4bc608fe77368e781571fd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443750"
---
# <a name="migrating-archiving-and-monitoring-servers"></a><span data-ttu-id="3ed3b-103">Перенос серверов архивирования и мониторинга</span><span class="sxs-lookup"><span data-stu-id="3ed3b-103">Migrating Archiving and Monitoring servers</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3ed3b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3ed3b-104">

<span> </span></span></span>

<span data-ttu-id="3ed3b-105">_**Тема последнего изменения:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="3ed3b-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="3ed3b-106">Если вы развернули сервер архивации и сервер мониторинга в среде Lync Server 2010, вы можете развернуть эти серверы в среде Lync Server 2013 после миграции пулов переднего плана.</span><span class="sxs-lookup"><span data-stu-id="3ed3b-106">If you deployed Archiving Server and Monitoring Server in your Lync Server 2010 environment, you can deploy these servers in your Lync Server 2013 environment after you migrate your Front End pools.</span></span> <span data-ttu-id="3ed3b-107">Тем не менее, если функции архивации и мониторинга критически важны для вашей организации, необходимо добавить архивацию и мониторинг в пул Lync Server 2013 Pilot, прежде чем вы сможете выполнить миграцию, чтобы они были доступны в процессе миграции.</span><span class="sxs-lookup"><span data-stu-id="3ed3b-107">If archiving and monitoring functionality are critical to your organization, however, you should add archiving and monitoring to your Lync Server 2013 pilot pool before you migrate so that the functionality is available during the migration process.</span></span>

<span data-ttu-id="3ed3b-108">Если вы хотите использовать функции архивации и наблюдения в процессе миграции, имейте в виду следующие моменты.</span><span class="sxs-lookup"><span data-stu-id="3ed3b-108">If you want archiving and monitoring functionality during the migration process, keep the following considerations in mind:</span></span>

  - <span data-ttu-id="3ed3b-109">Архивирование данных и данных мониторинга не переносятся в развертывание Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3ed3b-109">Archiving data and monitoring data are not moved to the Lync Server 2013 deployment.</span></span> <span data-ttu-id="3ed3b-110">Данные, которые вы заархивированы перед списанием устаревшей среды, будут журналом действий в среде Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="3ed3b-110">The data you back up prior to decommissioning the legacy environment will be your history of activity in the Lync Server 2010 environment.</span></span>

  - <span data-ttu-id="3ed3b-111">Версия Lync Server 2010 для архивации сервера и сервера мониторинга может быть связана только с интерфейсом front end сервера Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="3ed3b-111">The Lync Server 2010 version of Archiving Server and Monitoring Server can be associated only with a Lync Server 2010 Front End pool.</span></span> <span data-ttu-id="3ed3b-112">В Lync Server 2013 возможности архивации и мониторинга больше не являются серверными ролями, но службы, интегрированные в пул переднего плана Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3ed3b-112">In Lync Server 2013, Archiving and Monitoring are no longer server roles, but services integrated into the Lync Server 2013 Front End pool.</span></span>

  - <span data-ttu-id="3ed3b-113">В течение времени существования устаревших развертываний и сред Lync Server 2013 версия сервера архивации и мониторинга сервера Lync Server 2010 собирает данные для пользователей, размещенных в пулах Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="3ed3b-113">During the time that your legacy and Lync Server 2013 deployments coexist, the Lync Server 2010 version of Archiving Server and Monitoring Server gather data for users homed on Lync Server 2010 pools.</span></span> <span data-ttu-id="3ed3b-114">Архивация и мониторинг в Lync Server 2013 сбор данных для пользователей, размещенных в пулах Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3ed3b-114">Archiving and Monitoring in Lync Server 2013 gather data for users homed on Lync Server 2013 pools.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="3ed3b-115">На этапе миграции при использовании устаревшего пограничного сервера с новым пулом Lync Server 2013 Pilot версия сервера архивирования для Lync Server 2010 продолжает собирать данные для пользователей, размещенных на Lync Server 2010 пулов и архивации в Lync Server 2013 собирает данные для пользователей, размещенных на пулах Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3ed3b-115">During the phase of migration when you are still using your legacy Edge server with the new Lync Server 2013 pilot pool, the Lync Server 2010 version of Archiving Server continues to gather data for users homed on Lync Server 2010 pools and Archiving in Lync Server 2013 gathers data for users homed on Lync Server 2013 pools.</span></span>

    
    </div>

  - <span data-ttu-id="3ed3b-116">Если вы используете сторонние решения для архивации и мониторинга в сочетании с архивацией и мониторингом в Lync Server 2013, обратитесь к своему поставщику о том, когда и как следует интегрировать сторонние решения с Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3ed3b-116">If you use a third-party archiving and monitoring solution in conjunction with Archiving and Monitoring in Lync Server 2013, consult with your vendor about when and how you need to integrate the third-party solution with Lync Server 2013.</span></span>

<span data-ttu-id="3ed3b-117"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3ed3b-117"></div>

<span> </span>

</div>

</div>

</span></span></div>

