---
title: Проверка среды Office Communications Server 2007 R2
description: Проверка среды Office Communications Server 2007 R2.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Verify Office Communications Server 2007 R2 environment
ms:assetid: e051bdd5-e7ef-4754-8705-900b2c57f37c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721906(v=OCS.15)
ms:contentKeyID: 49733840
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: eb200941b3a35ece2b587bcfc89be743c9960d1f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443644"
---
# <a name="verify-office-communications-server-2007-r2-environment"></a><span data-ttu-id="74fc9-103">Проверка среды Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="74fc9-103">Verify Office Communications Server 2007 R2 environment</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="74fc9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="74fc9-104">

<span> </span></span></span>

<span data-ttu-id="74fc9-105">_**Тема последнего изменения:** 2012-10-16_</span><span class="sxs-lookup"><span data-stu-id="74fc9-105">_**Topic Last Modified:** 2012-10-16_</span></span>

<span data-ttu-id="74fc9-106">Перед развертыванием Lync Server 2013 в состоянии сосуществования с помощью Office Communications Server 2007 R2 необходимо убедиться, что службы Office Communications Server 2007 R2 настроены и запущены.</span><span class="sxs-lookup"><span data-stu-id="74fc9-106">Prior to deploying Lync Server 2013 in a coexistence state with Office Communications Server 2007 R2, you need to verify the Office Communications Server 2007 R2 services are configured and started.</span></span>

<span data-ttu-id="74fc9-107">**Проверка того, что пул запущен с помощью средства администрирования Office Communications Server 2007 R2**</span><span class="sxs-lookup"><span data-stu-id="74fc9-107">**Verify the Pool is started using the Office Communications Server 2007 R2 Administrative Tool**</span></span>

1.  <span data-ttu-id="74fc9-108">Откройте средство администрирования Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="74fc9-108">Open the Office Communications Server 2007 R2 administrative tool.</span></span>

2.  <span data-ttu-id="74fc9-109">Разверните узел **леса** , разверните узел **Стандартные серверы выпуска** или **Пулы предприятий** , а затем разверните имя пула или сервера.</span><span class="sxs-lookup"><span data-stu-id="74fc9-109">Expand the **Forest** node, expand the **Standard Edition Servers** or **Enterprise pools** node, and then expand the pool or server name.</span></span>

3.  <span data-ttu-id="74fc9-110">Убедитесь, что службы запущены на сервере Standard Edition или корпоративном пуле.</span><span class="sxs-lookup"><span data-stu-id="74fc9-110">Ensure that the services are running on the Standard Edition server or Enterprise pool.</span></span>
    
    <span data-ttu-id="74fc9-111">![Консоль администрирования Office Communications Server 2007 R2](images/JJ721906.76897b6d-f433-47d2-930d-0816fc30a3c2(OCS.15).jpg "Консоль администрирования Office Communications Server 2007 R2")</span><span class="sxs-lookup"><span data-stu-id="74fc9-111">![Office Communications Server 2007 R2 Admin Console](images/JJ721906.76897b6d-f433-47d2-930d-0816fc30a3c2(OCS.15).jpg "Office Communications Server 2007 R2 Admin Console")</span></span>

<span data-ttu-id="74fc9-112">**Просмотр пользователей, настроенных для Office Communications Server 2007 R2**</span><span class="sxs-lookup"><span data-stu-id="74fc9-112">**Review Users configured for Office Communications Server 2007 R2**</span></span>

1.  <span data-ttu-id="74fc9-113">Откройте средство администрирования Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="74fc9-113">Open the Office Communications Server 2007 R2 administrative tool.</span></span>

2.  <span data-ttu-id="74fc9-114">Разверните узел **леса** , разверните узел **Стандартные серверы выпуска** или **Пулы предприятий** , а затем разверните имя пула или сервера.</span><span class="sxs-lookup"><span data-stu-id="74fc9-114">Expand the **Forest** node, expand the **Standard Edition Servers** or **Enterprise pools** node, and then expand the pool or server name.</span></span>

3.  <span data-ttu-id="74fc9-115">Нажмите кнопку **Пользователи**.</span><span class="sxs-lookup"><span data-stu-id="74fc9-115">Click **Users**.</span></span>

4.  <span data-ttu-id="74fc9-116">Проверьте список пользователей Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="74fc9-116">Verify the list of Office Communications Server 2007 R2 users.</span></span>
    
    <span data-ttu-id="74fc9-117">![Список пользователей в средстве администрирования OCS](images/JJ721906.f6bb7c4f-cbed-4389-8d0a-69a28577f17a(OCS.15).jpg "Список пользователей в средстве администрирования OCS")</span><span class="sxs-lookup"><span data-stu-id="74fc9-117">![List fo users in OCS Admin tool](images/JJ721906.f6bb7c4f-cbed-4389-8d0a-69a28577f17a(OCS.15).jpg "List fo users in OCS Admin tool")</span></span>

<span data-ttu-id="74fc9-118">**Проверка конфигурации устаревшего XMPP федеративного партнера**</span><span class="sxs-lookup"><span data-stu-id="74fc9-118">**Verify legacy XMPP Federated Partner Configuration**</span></span>

1.  <span data-ttu-id="74fc9-119">Из устаревшего сервера XMPP перейдите на вкладку Администрирование \\ служб.</span><span class="sxs-lookup"><span data-stu-id="74fc9-119">From the legacy XMPP server, navigate to the Administrative Tools\\Services applet.</span></span>

2.  <span data-ttu-id="74fc9-120">Убедитесь, что служба шлюза Office Communications Server XMPP запущена.</span><span class="sxs-lookup"><span data-stu-id="74fc9-120">Verify that the Office Communications Server XMPP Gateway service is started.</span></span>
    
    <span data-ttu-id="74fc9-121">![Служба шлюза Office Communications Server XMPP](images/JJ721906.23223724-3c4b-4cb9-ace2-1cab2c3c91c3(OCS.15).jpg "Служба шлюза Office Communications Server XMPP")</span><span class="sxs-lookup"><span data-stu-id="74fc9-121">![Office Communications Server XMPP Gateway Service](images/JJ721906.23223724-3c4b-4cb9-ace2-1cab2c3c91c3(OCS.15).jpg "Office Communications Server XMPP Gateway Service")</span></span>

<span data-ttu-id="74fc9-122"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="74fc9-122"></div>

<span> </span>

</div>

</div>

</span></span></div>

