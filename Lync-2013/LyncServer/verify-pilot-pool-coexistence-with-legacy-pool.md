---
title: Проверка возможности совместного использования пилотного и старого пула
description: Проверка сосуществования пилотного пула с помощью устаревшего пула.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Verify pilot pool coexistence with legacy pool
ms:assetid: fe7e14bb-c7eb-4719-b154-009e99360520
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205420(v=OCS.15)
ms:contentKeyID: 48185964
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b910939b59fdaed6df32ae504eb2719435a0161e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440182"
---
# <a name="verify-pilot-pool-coexistence-with-legacy-pool"></a><span data-ttu-id="62638-103">Проверка возможности совместного использования пилотного и старого пула</span><span class="sxs-lookup"><span data-stu-id="62638-103">Verify pilot pool coexistence with legacy pool</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="62638-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="62638-104">

<span> </span></span></span>

<span data-ttu-id="62638-105">_**Тема последнего изменения:** 2012-09-29_</span><span class="sxs-lookup"><span data-stu-id="62638-105">_**Topic Last Modified:** 2012-09-29_</span></span>

<span data-ttu-id="62638-106">После развертывания пилотного пула необходимо проверить сосуществование двух пулов с помощью средств администрирования для просмотра сведений о пуле.</span><span class="sxs-lookup"><span data-stu-id="62638-106">After you deploy the pilot pool, you need to verify the coexistence of the two pools by using the administrative tools to view the pool information.</span></span> <span data-ttu-id="62638-107">Для пулов и стандартных пулов Lync Server 2013 необходимо использовать инструменты панели управления и Topology Builder сервера Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="62638-107">For the Lync Server 2013 pools and legacy pools, you must use the Lync Server 2013 Control Panel and Topology Builder tools.</span></span>

<div>

## <a name="verify-that-lync-server-2013-services-have-started"></a><span data-ttu-id="62638-108">Проверка того, что службы Lync Server 2013 запущены</span><span class="sxs-lookup"><span data-stu-id="62638-108">Verify that Lync Server 2013 services have started</span></span>

1.  <span data-ttu-id="62638-109">На сервере Lync Server 2013 с интерфейсом front end перейдите к \\ апплету администрирование служб.</span><span class="sxs-lookup"><span data-stu-id="62638-109">From the Lync Server 2013 Front End Server, navigate to the Administrative Tools\\Services applet.</span></span>

2.  <span data-ttu-id="62638-110">Убедитесь в том, что на сервере переднего плана запущены следующие службы:</span><span class="sxs-lookup"><span data-stu-id="62638-110">Verify that the following services are running on the Front End Server:</span></span>

<span data-ttu-id="62638-111">**Lync Server 2013 Services**</span><span class="sxs-lookup"><span data-stu-id="62638-111">**Lync Server 2013 services**</span></span>

<span data-ttu-id="62638-112">![Список запущенных служб Lync Server](images/JJ205420.cfff9385-6bf6-461c-982c-e727c9f20b70(OCS.15).png "Список запущенных служб Lync Server")</span><span class="sxs-lookup"><span data-stu-id="62638-112">![List of Lync Server Services Started](images/JJ205420.cfff9385-6bf6-461c-982c-e727c9f20b70(OCS.15).png "List of Lync Server Services Started")</span></span>

</div>

<div>

## <a name="open-the-lync-server-2013-control-panel"></a><span data-ttu-id="62638-113">Открытие панели управления Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="62638-113">Open the Lync Server 2013 Control Panel</span></span>

<span data-ttu-id="62638-114">На сервере переднего плана в среде Lync Server 2013 откройте панель управления Lync Server 2013 и выберите пул Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="62638-114">From the Front End Server in your Lync Server 2013 deployment, open the Lync Server 2013 Control Panel and select the Lync Server 2010 pool.</span></span> <span data-ttu-id="62638-115">Повторите процедуру, чтобы открыть пул Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="62638-115">Repeat the procedure to open the Lync Server 2013 pool.</span></span>

<span data-ttu-id="62638-116">**Открытие панели управления Lync Server 2013**</span><span class="sxs-lookup"><span data-stu-id="62638-116">**Open Lync Server 2013 Control Panel**</span></span>

<span data-ttu-id="62638-117">![Диалоговое окно "Выбор URL-адреса"](images/JJ205420.b1f8e650-9c3c-4563-a403-5069f198342f(OCS.15).png "Диалоговое окно "Выбор URL-адреса"")</span><span class="sxs-lookup"><span data-stu-id="62638-117">![Select URL dialog box](images/JJ205420.b1f8e650-9c3c-4563-a403-5069f198342f(OCS.15).png "Select URL dialog box")</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="62638-118">На Lync Server 2013 необходимо обновить Silverlight до Silverlight версии 5, прежде чем использовать панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="62638-118">On Lync Server 2013, you must upgrade Silverlight to Silverlight version 5 prior to using the Lync Server Control Panel.</span></span>



</div>

<span data-ttu-id="62638-119">Теперь эта топология включает в себя серверные роли Lync Server 2010 и Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="62638-119">This topology now includes Lync Server 2010 and Lync Server 2013 server roles.</span></span>

<span data-ttu-id="62638-120">**Страница топологии панели управления Lync Server 2013**</span><span class="sxs-lookup"><span data-stu-id="62638-120">**Lync Server 2013 Control Panel Topology page**</span></span>

<span data-ttu-id="62638-121">![Страница топологии на панели управления сервера Lync Server](images/JJ205420.4ed1cc7a-cb3e-42f6-82e2-6d4d71d19352(OCS.15).jpg "Страница топологии на панели управления сервера Lync Server")</span><span class="sxs-lookup"><span data-stu-id="62638-121">![Lync Server Control Panel - Topology page](images/JJ205420.4ed1cc7a-cb3e-42f6-82e2-6d4d71d19352(OCS.15).jpg "Lync Server Control Panel - Topology page")</span></span>

</div>

<div>

## <a name="dont-attempt-to-open-the-topology-in-lync-server-2010-topology-builder"></a><span data-ttu-id="62638-122">Не пытайтесь открыть топологию в Lync Server 2010 Topology Builder</span><span class="sxs-lookup"><span data-stu-id="62638-122">Don’t attempt to open the topology in Lync Server 2010 Topology Builder</span></span>

<span data-ttu-id="62638-123">Если вы попытаетесь открыть топологию с помощью Lync Server 2010 Topology Builder, вам появятся описанные ниже ошибки.</span><span class="sxs-lookup"><span data-stu-id="62638-123">If you attempt to open the topology using Lync Server 2010 Topology Builder, you will encounter the error below.</span></span> <span data-ttu-id="62638-124">Топологию можно просмотреть только с помощью построителя Lync Server 2013 Topology.</span><span class="sxs-lookup"><span data-stu-id="62638-124">The topology can only be viewed using Lync Server 2013 Topology Builder.</span></span> <span data-ttu-id="62638-125">Для создания пулов как для Lync Server 2013, так и для Lync Server 2010 необходимо использовать строитель топологии Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="62638-125">The Lync Server 2013 Topology Builder must be used to create pools for both Lync Server 2013 and Lync Server 2010.</span></span>

<span data-ttu-id="62638-126">**Сообщение об ошибке в Lync Server 2010 Topology Builder**</span><span class="sxs-lookup"><span data-stu-id="62638-126">**Lync Server 2010 Topology Builder error message**</span></span>

<span data-ttu-id="62638-127">![Ошибка привязки консоли управления "Построитель топологии Lync Server"](images/JJ205420.f6666343-c348-4d81-ae0e-6ba5a44e16c4(OCS.15).png "Ошибка привязки консоли управления "Построитель топологии Lync Server"")</span><span class="sxs-lookup"><span data-stu-id="62638-127">![Lync Server Topology Builder MMC Snap Error](images/JJ205420.f6666343-c348-4d81-ae0e-6ba5a44e16c4(OCS.15).png "Lync Server Topology Builder MMC Snap Error")</span></span>

<span data-ttu-id="62638-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="62638-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

