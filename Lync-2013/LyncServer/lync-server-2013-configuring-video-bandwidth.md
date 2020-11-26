---
title: 'Lync Server 2013: Настройка пропускной способности видео'
description: 'Lync Server 2013: Настройка пропускной способности видео.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring video bandwidth in Lync Server
ms:assetid: 446bed91-b26f-4ab2-b2f5-36e6810b405b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204842(v=OCS.15)
ms:contentKeyID: 48183984
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 85fedbe2fb856696236e79c3bbcece34d5af4a34
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432417"
---
# <a name="configuring-video-bandwidth-in-lync-server-2013"></a><span data-ttu-id="3302d-103">Настройка пропускной способности видео в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3302d-103">Configuring video bandwidth in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3302d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3302d-104">

<span> </span></span></span>

<span data-ttu-id="3302d-105">_**Тема последнего изменения:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="3302d-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="3302d-106">Lync Server 2013 содержит несколько параметров для управления видеосвязью с участием двух сторон и многосторонних конференций.</span><span class="sxs-lookup"><span data-stu-id="3302d-106">Lync Server 2013 includes several settings for managing video for two-party calls and multiparty conferences.</span></span> <span data-ttu-id="3302d-107">При развертывании Lync Server 2013 необходимо оценить, подходят ли для вашей организации параметры по умолчанию, и при необходимости изменить их.</span><span class="sxs-lookup"><span data-stu-id="3302d-107">When you deploy Lync Server 2013, you should evaluate whether the default settings are appropriate for your organization, and modify them as necessary.</span></span>

<span data-ttu-id="3302d-108">Параметры, описанные в этом разделе, относятся к обоим звонкам и конференц-связи с несколькими участниками.</span><span class="sxs-lookup"><span data-stu-id="3302d-108">The parameters described in this section apply to both two-party calls and multiparty conferencing.</span></span> <span data-ttu-id="3302d-109">Чтобы просмотреть или изменить эти параметры, воспользуйтесь одним из следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="3302d-109">View or modify these settings by using one of the following cmdlets:</span></span>

  - <span data-ttu-id="3302d-110">**Get-CsConferencingPolicy**</span><span class="sxs-lookup"><span data-stu-id="3302d-110">**Get-CsConferencingPolicy**</span></span>

  - <span data-ttu-id="3302d-111">**Set-CsConferencingPolicy**</span><span class="sxs-lookup"><span data-stu-id="3302d-111">**Set-CsConferencingPolicy**</span></span>

  - <span data-ttu-id="3302d-112">**New-CsConferencingPolicy**</span><span class="sxs-lookup"><span data-stu-id="3302d-112">**New-CsConferencingPolicy**</span></span>

<span data-ttu-id="3302d-113">Убедитесь в том, что в политике конференц-связи указаны следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="3302d-113">Verify the following settings in your conferencing policy:</span></span>

  - <span data-ttu-id="3302d-114">**VideoBitRateKb**   Этот параметр указывает максимальную скорость видеосвязи в килобитах в секунду (кбит/с), используемую для видео, отправленных пользователем.</span><span class="sxs-lookup"><span data-stu-id="3302d-114">**VideoBitRateKb**   This setting specifies the maximum video bit rate in kilobits per second (kbps) used for video sent by a user.</span></span> <span data-ttu-id="3302d-115">Значение по умолчанию — 50000 кбит/с.</span><span class="sxs-lookup"><span data-stu-id="3302d-115">The default value is 50000 kbps.</span></span> <span data-ttu-id="3302d-116">Допустимые значения: от 0 до 50000.</span><span class="sxs-lookup"><span data-stu-id="3302d-116">Valid values are 0 to 50000.</span></span>
    
    <span data-ttu-id="3302d-117">Этот параметр действует отдельно для основного видео и панорамного видео.</span><span class="sxs-lookup"><span data-stu-id="3302d-117">This setting applies separately to main video and panoramic video.</span></span>
    
    <span data-ttu-id="3302d-118">Пример: Если вы укажете 2000 кбит/с, то сервер Lync Server сможет отправлять 2000 кбит/с для основного видеопотока и 2000 кбит/с для видеопотока панорамного видео.</span><span class="sxs-lookup"><span data-stu-id="3302d-118">Example: if you specify 2000 kbps, then Lync Server can send 2000 kbps for the main video stream and 2000 kbps for the panoramic video stream.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="3302d-119">Максимальная пропускная способность сетевого видео для конечной точки Lync 2013 составляет 8000 кбит/с для основного видео и 2500 кбит/с для панорамного видео.</span><span class="sxs-lookup"><span data-stu-id="3302d-119">The maximum video network bandwidth for a Lync 2013 endpoint is 8000 kbps for the main video and 2500 kbps for panoramic video.</span></span> <span data-ttu-id="3302d-120">Эти максимальные значения достигаются только при получении или отправке нескольких видеороликов.</span><span class="sxs-lookup"><span data-stu-id="3302d-120">These maximum values are reached only if multiple videos are received or sent.</span></span> <span data-ttu-id="3302d-121">Дополнительные сведения можно найти в разделе "использование сетевого трафика мультимедиа" в <A href="lync-server-2013-network-bandwidth-requirements-for-media-traffic.md">требованиях к пропускной способности сети для мультимедийного трафика в Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="3302d-121">For details, see the "Media Traffic Network Usage" section in <A href="lync-server-2013-network-bandwidth-requirements-for-media-traffic.md">Network bandwidth requirements for media traffic in Lync Server 2013</A>.</span></span> <span data-ttu-id="3302d-122">В этом разделе приведена максимальная и Типичная пропускная способность потока видео для всех поддерживаемых разрешений.</span><span class="sxs-lookup"><span data-stu-id="3302d-122">This section lists the maximum and typical video stream bandwidth for all supported resolutions.</span></span>

    
    </div>

  - <span data-ttu-id="3302d-123">**TotalReceiveVideoBitRateKb**   Этот параметр, который является новым в Lync Server 2013, указывает максимально допустимую скорость (в килобитах в секунду) для всех потоков видео, полученных клиентом.</span><span class="sxs-lookup"><span data-stu-id="3302d-123">**TotalReceiveVideoBitRateKb**   This setting, which is new in Lync Server 2013, specifies the maximum allowed bitrate (in kilobits per second) for all the video streams received by a client.</span></span> <span data-ttu-id="3302d-124">Это означает, что он указывает совокупный итог для всех видеопотоков, за исключением потоковых видеороликов, которые может получать клиент.</span><span class="sxs-lookup"><span data-stu-id="3302d-124">That is, it specifies the combined total for all the video streams, except for panoramic video streams, that a client can receive.</span></span> <span data-ttu-id="3302d-125">Например, если вы укажете 1500 кбит/с, клиент может получить до 1500 кбит/с для видео, которое может состоять из нескольких видеопотоков или одного видеопотока.</span><span class="sxs-lookup"><span data-stu-id="3302d-125">For example, if you specify 1500 kbps, then a client can receive up to 1500 kbps of video, which may consist of multiple video streams or a single video stream.</span></span> <span data-ttu-id="3302d-126">Этот параметр применяется только к клиентам Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3302d-126">This setting applies only to Lync Server 2013 clients.</span></span>
    
    <span data-ttu-id="3302d-127">Значением по умолчанию для **TotalReceiveVideoBitRateKb** является 50000 кбит/с.</span><span class="sxs-lookup"><span data-stu-id="3302d-127">The default value for **TotalReceiveVideoBitRateKb** is 50000 kbps.</span></span> <span data-ttu-id="3302d-128">Если для параметра **EnableMultiviewJoin** в представлении коллекции задано значение "истина", **TotalReceiveVideoBitRateKb** не должно быть задано ниже 420 кбит/с.</span><span class="sxs-lookup"><span data-stu-id="3302d-128">If the **EnableMultiviewJoin** setting for Gallery View is set to True, **TotalReceiveVideoBitRateKb** must not be set below 420 kbps.</span></span> <span data-ttu-id="3302d-129">Если для параметра **EnableMultiviewJoin** в представлении коллекции задано значение "ложь", **TotalReceiveVideoBitRateKb** не должно быть задано ниже 100 Кбит/с.</span><span class="sxs-lookup"><span data-stu-id="3302d-129">If the **EnableMultiviewJoin** setting for Gallery View is set to False, **TotalReceiveVideoBitRateKb** must not be set below 100 kbps.</span></span> <span data-ttu-id="3302d-130">Если для **EnableMultiviewJoin** задано значение "true", а для значения ниже 420 кбит/с, то по умолчанию будет использоваться пороговое значение.</span><span class="sxs-lookup"><span data-stu-id="3302d-130">If **EnableMultiviewJoin** is set to True and you set the value below 420 kbps, the values will default to the threshold value.</span></span> <span data-ttu-id="3302d-131">Это пороговое значение помогает избежать случайной неправильной конфигурации, которая может привести к плохому взаимодействию с пользователем.</span><span class="sxs-lookup"><span data-stu-id="3302d-131">This threshold helps prevent accidental misconfiguration that might result in poor user experience.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="3302d-132">Дополнительные сведения о параметре <STRONG>EnableMultiviewJoin</STRONG> : <A href="lync-server-2013-configuring-gallery-view.md">Настройка представления галереи в Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="3302d-132">For details about the <STRONG>EnableMultiviewJoin</STRONG> setting, see <A href="lync-server-2013-configuring-gallery-view.md">Configuring Gallery View in Lync Server 2013</A>.</span></span>

    
    </div>

  - <span data-ttu-id="3302d-133">**MaxVideoConferencingResolution**   Этот параметр больше не используется для клиентов Lync Server 2013 в конференциях Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3302d-133">**MaxVideoConferencingResolution**   This parameter is no longer used for Lync Server 2013 clients in Lync Server 2013 conferences.</span></span> <span data-ttu-id="3302d-134">Конференции Lync Server 2013 используют элементы управления скоростью потока, описанные ранее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="3302d-134">Lync Server 2013 conferences use the bit rate controls described earlier in this section.</span></span> <span data-ttu-id="3302d-135">Этот параметр по-прежнему используется для устаревших клиентов, присоединяющихся к конференции Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3302d-135">This setting is still used for legacy clients joining a Lync Server 2013 conference.</span></span> <span data-ttu-id="3302d-136">Этот параметр определяет максимально допустимое разрешение для устаревших клиентов в конференциях, организованных пользователями, которые размещены на Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3302d-136">This parameter determines the maximum resolution allowed for legacy clients in conferences organized by users who are homed on Lync Server 2013.</span></span> <span data-ttu-id="3302d-137">Это значит, что устаревшие клиенты обрабатываются так же, как в предыдущих версиях Lync Server или Office Communications Server.</span><span class="sxs-lookup"><span data-stu-id="3302d-137">That is, legacy clients are treated the same as they were in previous versions of Lync Server or Office Communications Server.</span></span>

<span data-ttu-id="3302d-138">Помимо параметров политики конференций, применяемых к пользователям, оцените параметры конфигурации мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="3302d-138">In addition to conferencing policy settings that apply to users, evaluate media configuration settings.</span></span> <span data-ttu-id="3302d-139">Чтобы просмотреть или изменить эти параметры, воспользуйтесь одним из следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="3302d-139">View or modify these settings by using one of the following cmdlets:</span></span>

  - <span data-ttu-id="3302d-140">**Get-CsMediaConfiguration**</span><span class="sxs-lookup"><span data-stu-id="3302d-140">**Get-CsMediaConfiguration**</span></span>

  - <span data-ttu-id="3302d-141">**Set-CsMediaConfiguration**</span><span class="sxs-lookup"><span data-stu-id="3302d-141">**Set- CsMediaConfiguration**</span></span>

  - <span data-ttu-id="3302d-142">**New-CsMediaConfiguration**</span><span class="sxs-lookup"><span data-stu-id="3302d-142">**New- CsMediaConfiguration**</span></span>

<span data-ttu-id="3302d-143">Проверьте указанные ниже параметры.</span><span class="sxs-lookup"><span data-stu-id="3302d-143">Verify the following setting:</span></span>

  - <span data-ttu-id="3302d-144">**MaxVideoRateAllowed**   Этот параметр для каждого пула определяет максимальную скорость, с которой видеосигналы будут передаваться из конечных точек клиента.</span><span class="sxs-lookup"><span data-stu-id="3302d-144">**MaxVideoRateAllowed**   This per-pool setting specifies the maximum rate at which video signals will be transferred at the client endpoints.</span></span> <span data-ttu-id="3302d-145">Она применяется только к предыдущим версиям клиентов Lync Server.</span><span class="sxs-lookup"><span data-stu-id="3302d-145">It applies only to previous versions of Lync Server clients.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="3302d-146">Пользователи Lync Server 2013 не пропускают этот параметр и используют параметр TotalReceiveVideoBitRateKb в разделе "политика конференц-связи".</span><span class="sxs-lookup"><span data-stu-id="3302d-146">Lync Server 2013 clients ignore this setting and use the TotalReceiveVideoBitRateKb setting in conferencing policy instead.</span></span>

    
    </div>
    
    <span data-ttu-id="3302d-147">Значением по умолчанию является HD720P.</span><span class="sxs-lookup"><span data-stu-id="3302d-147">The default value is HD720P.</span></span> <span data-ttu-id="3302d-148">Допустимые значения: HD720p15M, VGA600K и CIF250K.</span><span class="sxs-lookup"><span data-stu-id="3302d-148">Valid values are HD720p15M, VGA600K, and CIF250K.</span></span>
    
    <span data-ttu-id="3302d-149">Пример: Если вы укажете 1500 кбит/с, то все устаревшие клиенты в пуле смогут получать до 1500 кбит/с для видео в двух или многосторонних конференциях.</span><span class="sxs-lookup"><span data-stu-id="3302d-149">Example: If you specify 1500 kbps, then all the legacy clients in the pool can receive up to 1500 kbps of video in two-party or multiparty conferences.</span></span>

<span data-ttu-id="3302d-150">Ниже описаны действия, которые можно использовать для изменения параметров, описанных в этом разделе, в командной консоли Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="3302d-150">The following procedures are examples of using Lync Server Management Shell to modify the settings described in this section.</span></span>

<div>

## <a name="to-modify-conferencing-policy-for-video-settings"></a><span data-ttu-id="3302d-151">Изменение политики конференции для настройки видео</span><span class="sxs-lookup"><span data-stu-id="3302d-151">To modify conferencing policy for video settings</span></span>

1.  <span data-ttu-id="3302d-152">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="3302d-152">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="3302d-153">Чтобы изменить политику конференц-связи, в командной строке выполните следующий командлет:</span><span class="sxs-lookup"><span data-stu-id="3302d-153">At the command line, run the following cmdlet to edit conferencing policy:</span></span>
    
        Set-CsConferencingPolicy -Identity Pool01ConferencingPolicy -VideoBitRateKb 2000 -TotalReceiveVideoBitRateKb 2000 

</div>

<div>

## <a name="to-modify-media-configuration-for-legacy-clients"></a><span data-ttu-id="3302d-154">Изменение конфигурации мультимедиа для устаревших клиентов</span><span class="sxs-lookup"><span data-stu-id="3302d-154">To modify media configuration for legacy clients</span></span>

1.  <span data-ttu-id="3302d-155">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="3302d-155">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="3302d-156">Чтобы изменить конфигурацию мультимедиа, в командной строке выполните следующий командлет:</span><span class="sxs-lookup"><span data-stu-id="3302d-156">At the command line, run the following cmdlet to edit the media configuration:</span></span>
    
        Set-CsMediaConfiguration -Identity site:Redmond01 -MaxVideoRateAllowed CIF250K

<span data-ttu-id="3302d-157"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3302d-157"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

