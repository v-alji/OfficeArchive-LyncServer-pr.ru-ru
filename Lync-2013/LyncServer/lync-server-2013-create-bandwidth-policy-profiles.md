---
title: 'Lync Server 2013: создание профилей политики пропускной способности'
description: 'Lync Server 2013: создание профилей политики пропускной способности.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create bandwidth policy profiles
ms:assetid: a71881ef-b04a-465e-9abb-0577bfd182f3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412785(v=OCS.15)
ms:contentKeyID: 48185086
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9646657c84806bff8caef3352774cdc5ddeab862
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431983"
---
# <a name="create-bandwidth-policy-profiles-in-lync-server-2013"></a><span data-ttu-id="9dbbc-103">Создание профилей политики пропускной способности в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9dbbc-103">Create bandwidth policy profiles in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9dbbc-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9dbbc-104">

<span> </span></span></span>

<span data-ttu-id="9dbbc-105">_**Тема последнего изменения:** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="9dbbc-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="9dbbc-p101">*Политики пропускной способности* определяют ограничения пропускной способности сети для режимов передачи звука и видеоизображения в реальном времени. Политики пропускной способности применяются к *профилям политики пропускной способности*, которые могут применяться к нескольким сетевым сайтам для контроля допуска звонков.</span><span class="sxs-lookup"><span data-stu-id="9dbbc-p101">*Bandwidth policies* define limitations on bandwidth usage for real-time audio and video modalities. Bandwidth policies are applied to *bandwidth policy profiles*, which can be applied to multiple network sites for call admission control.</span></span>

<span data-ttu-id="9dbbc-108">Рекомендации по выбору ограничений пропускной способности, которые следует настроить в развертывании CAC, описаны в разделе [Определение требований к управлению допуском звонков в Lync Server 2013](lync-server-2013-defining-your-requirements-for-call-admission-control.md) в документации по планированию.</span><span class="sxs-lookup"><span data-stu-id="9dbbc-108">For guidelines about what bandwidth limits you should set in your CAC deployment, see [Defining your requirements for call admission control in Lync Server 2013](lync-server-2013-defining-your-requirements-for-call-admission-control.md) in the Planning documentation.</span></span>

<span data-ttu-id="9dbbc-109">Дополнительные сведения о работе с политиками пропускной способности и профилями политики можно найти в документации по оболочке Lync Server Management Shell для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="9dbbc-109">For details about working with bandwidth policies and policy profiles, see the Lync Server Management Shell documentation for the following cmdlets:</span></span>

  - [<span data-ttu-id="9dbbc-110">New-CsNetworkBandwidthPolicyProfile</span><span class="sxs-lookup"><span data-stu-id="9dbbc-110">New-CsNetworkBandwidthPolicyProfile</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkBandwidthPolicyProfile)

  - [<span data-ttu-id="9dbbc-111">Get-CsNetworkBandwidthPolicyProfile</span><span class="sxs-lookup"><span data-stu-id="9dbbc-111">Get-CsNetworkBandwidthPolicyProfile</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkBandwidthPolicyProfile)

  - [<span data-ttu-id="9dbbc-112">Set-CsNetworkBandwidthPolicyProfile</span><span class="sxs-lookup"><span data-stu-id="9dbbc-112">Set-CsNetworkBandwidthPolicyProfile</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsNetworkBandwidthPolicyProfile)

  - [<span data-ttu-id="9dbbc-113">Remove-CsNetworkBandwidthPolicyProfile</span><span class="sxs-lookup"><span data-stu-id="9dbbc-113">Remove-CsNetworkBandwidthPolicyProfile</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsNetworkBandwidthPolicyProfile)

<span data-ttu-id="9dbbc-114">Примеры политик, созданных в следующей процедуре, задают ограничения для общего трафика аудиоданных, отдельных аудиосеансов, общего трафика видеоданных и отдельных видеосеансов.</span><span class="sxs-lookup"><span data-stu-id="9dbbc-114">The example policies created in the following procedure set limits for overall audio traffic, individual audio sessions, overall video traffic, and individual video sessions.</span></span> <span data-ttu-id="9dbbc-115">Например, в \_ профиле политики пропускной способности связи объемом 5 задаются указанные ниже ограничения.</span><span class="sxs-lookup"><span data-stu-id="9dbbc-115">For example, the 5Mb\_Link bandwidth policy profile sets the following limits:</span></span>

  - <span data-ttu-id="9dbbc-116">Аудиоданные: 2 000 кбит/с</span><span class="sxs-lookup"><span data-stu-id="9dbbc-116">Audio Limit: 2,000 kbps</span></span>

  - <span data-ttu-id="9dbbc-117">Аудиосеансы: 200 кбит/с</span><span class="sxs-lookup"><span data-stu-id="9dbbc-117">Audio Session Limit: 200 kbps</span></span>

  - <span data-ttu-id="9dbbc-118">Видеоданные: 1 400 кбит/с</span><span class="sxs-lookup"><span data-stu-id="9dbbc-118">Video Limit: 1,400 kbps</span></span>

  - <span data-ttu-id="9dbbc-119">Видеосеансы: 700 кбит/с</span><span class="sxs-lookup"><span data-stu-id="9dbbc-119">Video Session Limit: 700 kbps</span></span>

<div class=" ">


> [!NOTE]  
> <span data-ttu-id="9dbbc-p103">Минимальное значение для аудиосеанса 40 кбит/с. Минимальное значение для видеосеанса 100 кбит/с.</span><span class="sxs-lookup"><span data-stu-id="9dbbc-p103">The minimum Audio Session Limit value is 40 kbps. The minimum Video Session Limit value is 100 kbps.</span></span>



</div>

<div>

## <a name="to-create-bandwidth-policy-profiles-by-using-management-shell"></a><span data-ttu-id="9dbbc-122">Создание профилей политики пропускной способности с помощью командной консоли</span><span class="sxs-lookup"><span data-stu-id="9dbbc-122">To create bandwidth policy profiles by using Management Shell</span></span>

1.  <span data-ttu-id="9dbbc-123">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="9dbbc-123">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="9dbbc-124">Выполните командлет New-CsNetworkBandwidthPolicyProfile для каждого создаваемого профиля политики пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="9dbbc-124">For each bandwidth policy profile that you want to create, run the New-CsNetworkBandwidthPolicyProfile cmdlet.</span></span> <span data-ttu-id="9dbbc-125">Пример:</span><span class="sxs-lookup"><span data-stu-id="9dbbc-125">For example, run:</span></span>
    
       ```powershell
        New-CsNetworkBandwidthPolicyProfile -Identity 5Mb_Link -Description "BW profile for 5Mb links" -AudioBWLimit 2000 -AudioBWSessionLimit 200 -VideoBWLimit 1400  -VideoBWSessionLimit 700
       ```
    
       ```powershell
        New-CsNetworkBandwidthPolicyProfile -Identity 10Mb_Link -Description "BW profile for 10Mb links" -AudioBWLimit 4000 -AudioBWSessionLimit 200 -VideoBWLimit 2800 -VideoBWSessionLimit 700
       ```
    
       ```powershell
        New-CsNetworkBandwidthPolicyProfile -Identity 50Mb_Link -Description "BW profile for 50Mb links" -AudioBWLimit 20000 -AudioBWSessionLimit 200 -VideoBWLimit 14000 -VideoBWSessionLimit 700
       ```
    
       ```powershell
        New-CsNetworkBandwidthPolicyProfile -Identity 25Mb_Link -Description "BW profile for 25Mb links" -AudioBWLimit 10000 -AudioBWSessionLimit 200 -VideoBWLimit 7000 -VideoBWSessionLimit 700
       ```

</div>

<div>

## <a name="to-create-bandwidth-policy-profiles-by-using-lync-server-control-panel"></a><span data-ttu-id="9dbbc-126">Создание профилей политики пропускной способности с помощью панели управления Lync Server</span><span class="sxs-lookup"><span data-stu-id="9dbbc-126">To create bandwidth policy profiles by using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="9dbbc-127">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="9dbbc-127">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="9dbbc-128">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="9dbbc-128">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

2.  <span data-ttu-id="9dbbc-129">В левой области навигации щелкните **Конфигурация сети**.</span><span class="sxs-lookup"><span data-stu-id="9dbbc-129">In the left navigation bar, click **Network Configuration**.</span></span>

3.  <span data-ttu-id="9dbbc-130">Нажмите кнопку навигации **Профиль политики**.</span><span class="sxs-lookup"><span data-stu-id="9dbbc-130">Click the **Policy Profile** navigation button.</span></span>

4.  <span data-ttu-id="9dbbc-131">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="9dbbc-131">Click **New**.</span></span>

5.  <span data-ttu-id="9dbbc-132">На странице **создания профиля политики** в поле щелкните **Имя**, затем введите имя профиля политики пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="9dbbc-132">On the **New Policy Profile** page, click **Name** and then type a name for the bandwidth policy profile.</span></span>

6.  <span data-ttu-id="9dbbc-133">Щелкните **Ограничение для звукового сеанса**, затем введите максимальную скорость в кбит/с, общую для всех сеансов звуковой связи.</span><span class="sxs-lookup"><span data-stu-id="9dbbc-133">Click **Audio limit**, and then type in the maximum number of kbps to allow for all audio sessions combined.</span></span>

7.  <span data-ttu-id="9dbbc-134">Щелкните **Ограничение для видео**, затем введите максимальную скорость в кбит/с для отдельного сеанса звуковой связи.</span><span class="sxs-lookup"><span data-stu-id="9dbbc-134">Click **Audio session limit**, and then type in the maximum number of kbps to allow for each individual audio session.</span></span>

8.  <span data-ttu-id="9dbbc-135">Щелкните **Ограничение для видео**, затем введите максимальную скорость в кбит/с, общую для всех сеансов видеосвязи.</span><span class="sxs-lookup"><span data-stu-id="9dbbc-135">Click **Video limit**, and then type in the maximum number of kbps to allow for all video sessions combined.</span></span>

9.  <span data-ttu-id="9dbbc-136">Щелкните **Ограничение для видеосеанса**, затем введите максимальную скорость в кбит/с для отдельного сеанса видеосвязи.</span><span class="sxs-lookup"><span data-stu-id="9dbbc-136">Click **Video session limit**, and then type in the maximum number of kbps to allow for each individual video session.</span></span>

10. <span data-ttu-id="9dbbc-137">Щелкните **Описание** и введите дополнительные сведения о профиле политики пропускной способности (не обязательно).</span><span class="sxs-lookup"><span data-stu-id="9dbbc-137">Optionally, click **Description**, and then type additional information to describe this bandwidth policy profile.</span></span>

11. <span data-ttu-id="9dbbc-138">Нажмите **Исполнить**.</span><span class="sxs-lookup"><span data-stu-id="9dbbc-138">Click **Commit**.</span></span>

12. <span data-ttu-id="9dbbc-139">Чтобы завершить создание профилей политики пропускной способности для топологии, повторите шаги с 4 по 11 для остальных профилей политики пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="9dbbc-139">To finish creating bandwidth policy profiles for your topology, repeat steps 4 through 11 with settings for other bandwidth policy profiles.</span></span>

<span data-ttu-id="9dbbc-140"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9dbbc-140"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

