---
title: 'Lync Server 2013: Включение обхода сетевых мультимедийных файлов'
description: 'Lync Server 2013: Включение обхода сетевого мультимедиа.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enabling network media bypass
ms:assetid: 95c4fa06-49d3-41ac-acdc-7dcda66e5508
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182552(v=OCS.15)
ms:contentKeyID: 48184846
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1218376903aa42e1ea55205e3a9e8d16aade9a3a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399280"
---
# <a name="enabling-network-media-bypass-in-lync-server-2013"></a><span data-ttu-id="ba110-103">Включение обхода сетевых мультимедийных файлов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ba110-103">Enabling network media bypass in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ba110-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ba110-104">

<span> </span></span></span>

<span data-ttu-id="ba110-105">_**Тема последнего изменения:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="ba110-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="ba110-106">Параметры обхода мультимедиа применяются глобально в рамках развертывания Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ba110-106">Media bypass settings apply globally across a Microsoft Lync Server 2013 deployment.</span></span> <span data-ttu-id="ba110-107">Обойти функцию мультимедиа позволяет обходить сервер.</span><span class="sxs-lookup"><span data-stu-id="ba110-107">Media bypass allows calls to bypass the Mediation Server.</span></span> <span data-ttu-id="ba110-108">Сведения о том, когда следует использовать обход мультимедиа, приведены в статье [Планирование обхода мультимедиа в Lync Server 2013](lync-server-2013-planning-for-media-bypass.md) в разделе Планирование.</span><span class="sxs-lookup"><span data-stu-id="ba110-108">For details about when to use Media bypass, see [Planning for media bypass in Lync Server 2013](lync-server-2013-planning-for-media-bypass.md) in the Planning section.</span></span>

<span data-ttu-id="ba110-109">Вы можете включить и настроить обход мультимедиа с помощью панели управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ba110-109">You can enable and configure media bypass from the Lync Server Control Panel.</span></span>

<div>

## <a name="to-enable-and-configure-media-bypass"></a><span data-ttu-id="ba110-110">Включение и Настройка обхода мультимедиа</span><span class="sxs-lookup"><span data-stu-id="ba110-110">To enable and configure media bypass</span></span>

1.  <span data-ttu-id="ba110-111">Войдите на любой компьютер, находящийся во внутреннем развертывании, с использованием учетной записи, входящей в группу RTCUniversalServerAdmins (или имеющей равнозначные права пользователя) либо назначенной роли CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="ba110-111">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="ba110-112">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ba110-112">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="ba110-113">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="ba110-113">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="ba110-114">На панели навигации слева выберите пункт **Конфигурация сети** , а затем — **Глобальная**.</span><span class="sxs-lookup"><span data-stu-id="ba110-114">In the left navigation bar, click **Network Configuration** and then click **Global**.</span></span>

4.  <span data-ttu-id="ba110-115">На **глобальной** странице щелкните **глобальную** конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="ba110-115">On the **Global** page, click the **Global** configuration.</span></span> <span data-ttu-id="ba110-116">Всегда существует только одна конфигурация, и она всегда имеет имя Global.</span><span class="sxs-lookup"><span data-stu-id="ba110-116">There is always only one configuration, and it is always named Global.</span></span>

5.  <span data-ttu-id="ba110-117">В меню **Правка** выберите команду **Просмотреть сведения**.</span><span class="sxs-lookup"><span data-stu-id="ba110-117">On the **Edit** menu, click **View details**.</span></span>

6.  <span data-ttu-id="ba110-118">На странице " **изменение глобальных параметров** " установите флажок **включить обход мультимедиа** .</span><span class="sxs-lookup"><span data-stu-id="ba110-118">On the **Edit Global Setting** page, click the **Enable media bypass** check box.</span></span>

7.  <span data-ttu-id="ba110-119">Выберите один из следующих вариантов:</span><span class="sxs-lookup"><span data-stu-id="ba110-119">Select one of the following options:</span></span>
    
      - <span data-ttu-id="ba110-120">**Всегда обходить**   Выберите этот параметр, чтобы попытаться пропускать мультимедиа во всех звонках.</span><span class="sxs-lookup"><span data-stu-id="ba110-120">**Always bypass**   Select this option to attempt media bypass on all calls.</span></span> <span data-ttu-id="ba110-121">Этот параметр будет недоступен, если включен элемент управления допуском звонков (CAC).</span><span class="sxs-lookup"><span data-stu-id="ba110-121">This option will be unavailable if call admission control (CAC) is enabled.</span></span> <span data-ttu-id="ba110-122">Если функция CAC не включена, выберите этот параметр в указанных ниже случаях.</span><span class="sxs-lookup"><span data-stu-id="ba110-122">If CAC is not enabled, select this option in the following situations:</span></span>
        
          - <span data-ttu-id="ba110-123">Контроль за пропускной способностью не требуется.</span><span class="sxs-lookup"><span data-stu-id="ba110-123">There is no need for bandwidth control.</span></span>
        
          - <span data-ttu-id="ba110-124">Не нужно детально настраивать конфигурацию, чтобы определить, когда должно происходить обход.</span><span class="sxs-lookup"><span data-stu-id="ba110-124">There is no need for fine-grained configuration to determine when bypass should happen.</span></span>
        
          - <span data-ttu-id="ba110-125">Существует полная связь между шлюзами и клиентами.</span><span class="sxs-lookup"><span data-stu-id="ba110-125">There is full connectivity between gateways and clients.</span></span>
    
      - <span data-ttu-id="ba110-126">**Использование сайтов и конфигурации областей**   Если включена функция CAC, этот параметр установлен по умолчанию и не может быть изменен.</span><span class="sxs-lookup"><span data-stu-id="ba110-126">**Use sites and region configuration**   If CAC is enabled, this option is selected by default and cannot be changed.</span></span> <span data-ttu-id="ba110-127">Если выбран этот параметр, сайты и регионы настройки сети будут использоваться для определения способа обхода мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="ba110-127">When this option is selected, network configuration sites and regions will be used to determine when media bypass is possible.</span></span> <span data-ttu-id="ba110-128">Если выбрать этот параметр, вы можете включить обход для несопоставленных сайтов.</span><span class="sxs-lookup"><span data-stu-id="ba110-128">If you select this option, you can choose to enable bypass for sites that are not mapped.</span></span> <span data-ttu-id="ba110-129">Установите флажок **Разрешить игнорировать для несопоставленных сайтов** только в том случае, если у вас есть один или несколько крупных сайтов, связанных с тем же регионом, но не пропускаемых ограничений (например, для крупного центрального сайта), а также есть некоторые сайты филиалов, связанные с тем же регионом, в котором есть ограничения пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="ba110-129">Click the **Enable bypass for non-mapped sites** check box only if you have one or more large sites associated with the same region that do not have bandwidth constraints (for example, a large central site) and you also have some branch sites associated with the same region that do have bandwidth constraints.</span></span> <span data-ttu-id="ba110-130">При включении обхода для несопоставленных сайтов Настройка оптимизируется, так как вы указываете только подсети, связанные с сайтами филиалов, а не необходимость указывать все подсети, связанные со всеми сайтами.</span><span class="sxs-lookup"><span data-stu-id="ba110-130">When you enable bypass for non-mapped sites, configuration is streamlined because you specify only the subnets associated with the branch sites rather than needing to specify all subnets associated with all sites.</span></span> <span data-ttu-id="ba110-131">Мы рекомендуем не устанавливать флажок **включить обход для несопоставленных сайтов** , если включен параметр CAC.</span><span class="sxs-lookup"><span data-stu-id="ba110-131">We recommend that you do not select the **Enable bypass for non-mapped sites** check box if CAC is enabled.</span></span>

8.  <span data-ttu-id="ba110-132">Нажмите **кнопку Сохранить,** чтобы сохранить изменения.</span><span class="sxs-lookup"><span data-stu-id="ba110-132">Click **Commit** to save your changes.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="ba110-133">См. также</span><span class="sxs-lookup"><span data-stu-id="ba110-133">See Also</span></span>


[<span data-ttu-id="ba110-134">Отключение обхода сетевых мультимедийных файлов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ba110-134">Disabling network media bypass in Lync Server 2013</span></span>](lync-server-2013-disabling-network-media-bypass.md)  


[<span data-ttu-id="ba110-135">Глобальные параметры обхода мультимедиа в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ba110-135">Global media bypass options in Lync Server 2013</span></span>](lync-server-2013-global-media-bypass-options.md)  


[<span data-ttu-id="ba110-136">Планирование обхода серверов-посредников в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ba110-136">Planning for media bypass in Lync Server 2013</span></span>](lync-server-2013-planning-for-media-bypass.md)  
  

<span data-ttu-id="ba110-137"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ba110-137"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

