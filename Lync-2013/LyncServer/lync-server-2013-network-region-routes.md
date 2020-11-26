---
title: 'Lync Server 2013: Маршруты сетевого региона'
description: 'Lync Server 2013: Маршруты сетевого региона.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Network region routes
ms:assetid: 32da29aa-7612-48fa-a983-72a821651aa3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688018(v=OCS.15)
ms:contentKeyID: 49733608
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 740b517f1dab80b028b319d220dfcb01af08ef25
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425180"
---
# <a name="network-region-routes-in-lync-server-2013"></a><span data-ttu-id="034f8-103">Маршруты к сетевым регионам в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="034f8-103">Network region routes in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="034f8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="034f8-104">

<span> </span></span></span>

<span data-ttu-id="034f8-105">_**Тема последнего изменения:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="034f8-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="034f8-106">*Маршрут к сетевому региону* определяет маршрут между парой областей сети.</span><span class="sxs-lookup"><span data-stu-id="034f8-106">A *network region route* defines the route between a pair of network regions.</span></span> <span data-ttu-id="034f8-107">Для каждой пары областей сети в развертывании средства управления допуском звонков требуется маршрут к сетевому региону.</span><span class="sxs-lookup"><span data-stu-id="034f8-107">Each pair of network regions in your call admission control deployment requires a network region route.</span></span> <span data-ttu-id="034f8-108">Это позволяет каждому региону сети в рамках развертывания осуществлять доступ к любому другому региону.</span><span class="sxs-lookup"><span data-stu-id="034f8-108">This enables every network region within the deployment to access every other region.</span></span> <span data-ttu-id="034f8-109">В этом разделе описаны процедуры для просмотра, создания, изменения и удаления маршрутов сетевого региона.</span><span class="sxs-lookup"><span data-stu-id="034f8-109">Use the procedures in this section to view, create, modify, or delete network region routes.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="034f8-110">Содержание</span><span class="sxs-lookup"><span data-stu-id="034f8-110">In This Section</span></span>

  - [<span data-ttu-id="034f8-111">Создание и изменение областей сети в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="034f8-111">Creating or modifying network regions in Lync Server 2013</span></span>](lync-server-2013-creating-or-modifying-network-regions.md)

  - [<span data-ttu-id="034f8-112">Просмотр сведений о маршруте в сетевом регионе в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="034f8-112">Viewing network region route information in Lync Server 2013</span></span>](lync-server-2013-viewing-network-region-route-information.md)

  - [<span data-ttu-id="034f8-113">Удаление существующих маршрутов сетевого региона в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="034f8-113">Deleting existing network region routes in Lync Server 2013</span></span>](lync-server-2013-deleting-existing-network-region-routes.md)

</div>

<div>

## <a name="reference"></a><span data-ttu-id="034f8-114">Справка</span><span class="sxs-lookup"><span data-stu-id="034f8-114">Reference</span></span>

[<span data-ttu-id="034f8-115">Развертывание улучшенных функций голосовой связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="034f8-115">Deploying advanced Enterprise Voice features in Lync Server 2013</span></span>](lync-server-2013-deploying-advanced-enterprise-voice-features.md)

<span data-ttu-id="034f8-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="034f8-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

