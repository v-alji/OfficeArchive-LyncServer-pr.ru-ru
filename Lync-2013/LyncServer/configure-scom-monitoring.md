---
title: Настройка мониторинга SCOM
description: Настройте мониторинг SCOM.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Configure SCOM monitoring
ms:assetid: 4003d225-2a33-448c-abd9-571750661140
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688033(v=OCS.15)
ms:contentKeyID: 49733624
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c93e10c705a1a1e08972d7534e00a33c472d23a3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398371"
---
# <a name="configure-scom-monitoring"></a><span data-ttu-id="61d52-103">Настройка мониторинга SCOM</span><span class="sxs-lookup"><span data-stu-id="61d52-103">Configure SCOM monitoring</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="61d52-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="61d52-104">

<span> </span></span></span>

<span data-ttu-id="61d52-105">_**Тема последнего изменения:** 2012-10-04_</span><span class="sxs-lookup"><span data-stu-id="61d52-105">_**Topic Last Modified:** 2012-10-04_</span></span>

<span data-ttu-id="61d52-106">После перехода на Microsoft Lync Server 2013 необходимо выполнить несколько задач, чтобы настроить Lync Server 2013 для работы с System Center Operations Manager.</span><span class="sxs-lookup"><span data-stu-id="61d52-106">After migrating to Microsoft Lync Server 2013, you must complete a few tasks to configure Lync Server 2013 to work with System Center Operations Manager.</span></span>

  - <span data-ttu-id="61d52-107">Примените к серверу Lync Server 2010 обновлений, выбранных для управления логикой центрального обнаружения.</span><span class="sxs-lookup"><span data-stu-id="61d52-107">Apply Lync Server 2010 updates to a server elected to manage the central discovery logic.</span></span>

  - <span data-ttu-id="61d52-108">Обновите раздел реестра для основного сервера поиска кандидатов.</span><span class="sxs-lookup"><span data-stu-id="61d52-108">Update the central discovery candidate server registry key.</span></span>

  - <span data-ttu-id="61d52-109">Настройка основного сервера System Center Operations Manager для переопределения узла центра обнаружения кандидатов.</span><span class="sxs-lookup"><span data-stu-id="61d52-109">Configure your primary System Center Operations Manager management server to override the candidate central discovery node.</span></span>

<span data-ttu-id="61d52-110">Ниже приведены инструкции по переносу каждой из этих задач.</span><span class="sxs-lookup"><span data-stu-id="61d52-110">Instructions for carrying out each of these tasks are provided below.</span></span>

<span data-ttu-id="61d52-111">**Примените к серверу Lync Server 2010 обновлений, выбранных для управления логикой центрального обнаружения.**</span><span class="sxs-lookup"><span data-stu-id="61d52-111">**Apply Lync Server 2010 updates to a server elected to manage the central discovery logic.**</span></span>

1.  <span data-ttu-id="61d52-112">Выровняйте сервер, на котором установлены файлы агента System Center Operations Manager и настроен как узел обнаружения кандидатов.</span><span class="sxs-lookup"><span data-stu-id="61d52-112">Elect a server that has the System Center Operations Manager agent files installed and is configured as a candidate discovery node.</span></span>

2.  <span data-ttu-id="61d52-113">Примените к этому серверу обновления Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="61d52-113">Apply Lync Server 2010 updates to this server.</span></span> <span data-ttu-id="61d52-114">Ознакомьтесь с разделом [применение обновлений Lync Server 2010](apply-lync-server-2010-updates.md).</span><span class="sxs-lookup"><span data-stu-id="61d52-114">See the topic [Apply Lync Server 2010 updates](apply-lync-server-2010-updates.md).</span></span>

<span data-ttu-id="61d52-115">**Обновите раздел реестра для основного сервера поиска кандидатов.**</span><span class="sxs-lookup"><span data-stu-id="61d52-115">**Update the central discovery candidate server registry key.**</span></span>

1.  <span data-ttu-id="61d52-116">На сервере, выбранном для управления логикой центрального обнаружения, Откройте командное окно Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="61d52-116">On the server elected to manage the central discovery logic, open a Windows PowerShell command window.</span></span>

2.  <span data-ttu-id="61d52-117">В командной строке введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="61d52-117">At the command line, type the following:</span></span>
    
       ```PowerShell
        New-Item -Path "HKLM:\Software\Microsoft\Real-Time Communications\Health"
       ```
    
       ```PowerShell
        New-Item -Path "HKLM:\Software\Microsoft\Real-Time Communications\Health\CentralDiscoveryCandidate"
       ```
    
    <div class="">
    

    > [!NOTE]  
    > <span data-ttu-id="61d52-118">При внесении изменений в реестр может возникнуть сообщение о том, что команда завершилась сбоем, если раздел реестра уже существует.</span><span class="sxs-lookup"><span data-stu-id="61d52-118">Whenever you edit the registry, you may experience an error that the command failed if the registry key already exists.</span></span> <span data-ttu-id="61d52-119">Если вы столкнетесь с этим, вы можете спокойно проигнорировать ошибку.</span><span class="sxs-lookup"><span data-stu-id="61d52-119">If you experience this, you can safely ignore the error.</span></span>

    
    </div>

<span data-ttu-id="61d52-120">**Настройка основного сервера System Center Operations Manager для переопределения узла наблюдения за центральным обнаружением.**</span><span class="sxs-lookup"><span data-stu-id="61d52-120">**Configure your primary System Center Operations Manager management server to override the candidate central discovery watcher node.**</span></span>

1.  <span data-ttu-id="61d52-121">На компьютере с установленной консолью System Center Operations Manager разверните **объект пакета управления** , а затем выберите пункт **Обнаружение объектов**.</span><span class="sxs-lookup"><span data-stu-id="61d52-121">On a computer where the System Center Operations Manager console has been installed, expand **Management Pack Objects** and then select **Object Discoveries**.</span></span>

2.  <span data-ttu-id="61d52-122">Выберите команду **изменить область...**</span><span class="sxs-lookup"><span data-stu-id="61d52-122">Click **Change Scope...**</span></span>

3.  <span data-ttu-id="61d52-123">На странице " **объекты пакета управления областью** " выберите **кандидат на обнаружение Ls**.</span><span class="sxs-lookup"><span data-stu-id="61d52-123">From the **Scope Management Pack Objects** page, select **LS Discovery Candidate**.</span></span>

4.  <span data-ttu-id="61d52-124">Переопределение **действующего значения-кандидата на обнаружение Ls** на имя сервера-кандидата, выбранное в предыдущей процедуре.</span><span class="sxs-lookup"><span data-stu-id="61d52-124">Override the **LS Discovery Candidate Effective Value** to the name of the candidate server elected in the earlier procedure.</span></span>

<span data-ttu-id="61d52-125">Наконец, чтобы завершить изменения, перезапустите службу работоспособности на корневом сервере управления System Center Operations Manager.</span><span class="sxs-lookup"><span data-stu-id="61d52-125">Lastly, to finalize your changes, restart the health service on the System Center Operations Manager Root Management Server.</span></span>

<span data-ttu-id="61d52-126"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="61d52-126"></div>

<span> </span>

</div>

</div>

</span></span></div>

