---
title: Перенос нескольких сайтов и пулов
description: Перенос нескольких сайтов и групп.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migrating multiple sites and pools
ms:assetid: a6d726d2-564d-4b39-a97c-5656a673292a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205165(v=OCS.15)
ms:contentKeyID: 48185079
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7efaa6f038286ff9138e631f23da88bb445e20f1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440376"
---
# <a name="migrating-multiple-sites-and-pools"></a><span data-ttu-id="c2dc4-103">Перенос нескольких сайтов и пулов</span><span class="sxs-lookup"><span data-stu-id="c2dc4-103">Migrating multiple sites and pools</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c2dc4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c2dc4-104">

<span> </span></span></span>

<span data-ttu-id="c2dc4-105">_**Тема последнего изменения:** 2012-09-17_</span><span class="sxs-lookup"><span data-stu-id="c2dc4-105">_**Topic Last Modified:** 2012-09-17_</span></span>

<span data-ttu-id="c2dc4-106">Lync Server 2013 поддерживает развертывание с несколькими сайтами и несколькими пулами.</span><span class="sxs-lookup"><span data-stu-id="c2dc4-106">Lync Server 2013 supports multi-site and multi-pool deployments.</span></span> <span data-ttu-id="c2dc4-107">Процесс миграции нескольких пулов с Lync Server 2010 на Lync Server 2013 требует указанных ниже факторов.</span><span class="sxs-lookup"><span data-stu-id="c2dc4-107">The process of migrating multiple pools from Lync Server 2010 to Lync Server 2013 requires the following considerations:</span></span>

1.  <span data-ttu-id="c2dc4-108">После развертывания пула Lync Server 2013 Pilot вы должны определить подмножество пользователей пилотной версии, которые будут перенесены в пул Lync Server 2013, и методологию для проверки функциональных возможностей пользователей.</span><span class="sxs-lookup"><span data-stu-id="c2dc4-108">After deploying a Lync Server 2013 pilot pool, you need to define a subset of pilot users that will be moved to the Lync Server 2013 pool, and a methodology for validating the functionality of the users.</span></span> <span data-ttu-id="c2dc4-109">Например, после перемещения пользователя в пилотный пул убедитесь, что политика конференции пользователя перешла на Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c2dc4-109">For example, after moving a user to the pilot pool, verify the user’s conference policy has moved to Lync Server 2013.</span></span>

2.  <span data-ttu-id="c2dc4-110">После развертывания пограничного сервера в пилотном пуле необходимо проверить, могут и внешние пользователи взаимодействовать с пулом Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c2dc4-110">After deploying an Edge Server in the pilot pool, you need to validate that external users can communicate with the Lync Server 2013 pool.</span></span>

3.  <span data-ttu-id="c2dc4-111">После перевода федеративных маршрутов с сервера Lync Server 2010 EDGE на пробную подложку Lync Server 2013 Edges необходимо проверить, что Федеративные пользователи смогут взаимодействовать с пулом Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c2dc4-111">After transitioning the federated routes from Lync Server 2010 Edge Servers to the pilot Lync Server 2013 Edge Servers, you need to validate that federated users can communicate with the Lync Server 2013 pool.</span></span>

4.  <span data-ttu-id="c2dc4-112">После перемещения всех пользователей и объектов контактных лиц, не являющихся пользователями, необходимо проверить, что пул Lync Server 2010 пуст.</span><span class="sxs-lookup"><span data-stu-id="c2dc4-112">After moving all the users and non-user contact objects, you need to validate that the Lync Server 2010 pool is empty.</span></span>

5.  <span data-ttu-id="c2dc4-113">После того как вы убедитесь в том, что пул Lync Server 2010 пуст, вы можете деактивировать пул.</span><span class="sxs-lookup"><span data-stu-id="c2dc4-113">After verifying that the Lync Server 2010 pool is empty, you can then deactivate the pool.</span></span>
    
    <span data-ttu-id="c2dc4-114">Подробнее об отключении устаревшего пула и серверов Lync Server 2010 вы можете найти в разделе [Этап 8: списание стандартных пулов](phase-8-decommission-legacy-pools.md).</span><span class="sxs-lookup"><span data-stu-id="c2dc4-114">For details about how to deactivate the legacy Lync Server 2010 pool and servers, see [Phase 8: Decommission legacy pools](phase-8-decommission-legacy-pools.md).</span></span>

<span data-ttu-id="c2dc4-115"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c2dc4-115"></div>

<span> </span>

</div>

</div>

</span></span></div>

