---
title: 'Lync Server 2013: Настройка канала с помощью мультимедийного обхода'
description: 'Lync Server 2013: Настройка магистрали с обходом мультимедиа.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure a trunk with media bypass
ms:assetid: 99d729ea-5a4c-4ff2-a4a3-93a24368da6d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398792(v=OCS.15)
ms:contentKeyID: 48184959
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 51bd58a685e1f4c222a863c21022b3c9dc7c70d6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434169"
---
# <a name="configure-a-trunk-with-media-bypass-in-lync-server-2013"></a><span data-ttu-id="759c6-103">Configure a trunk with media bypass in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="759c6-103">Configure a trunk with media bypass in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="759c6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="759c6-104">

<span> </span></span></span>

<span data-ttu-id="759c6-105">_**Тема последнего изменения:** 2014-02-07_</span><span class="sxs-lookup"><span data-stu-id="759c6-105">_**Topic Last Modified:** 2014-02-07_</span></span>

<span data-ttu-id="759c6-106">Выполните следующие действия, чтобы настроить магистраль с включенным режимом обхода сервера-посредника.</span><span class="sxs-lookup"><span data-stu-id="759c6-106">Follow these steps to configure a trunk with media bypass enabled.</span></span> <span data-ttu-id="759c6-107">Чтобы настроить магистраль с отключенным обходом мультимедиа, пропустите раздел [Настройка магистрали без обхода мультимедиа в Lync Server 2013](lync-server-2013-configure-a-trunk-without-media-bypass.md).</span><span class="sxs-lookup"><span data-stu-id="759c6-107">To configure a trunk with media bypass disabled, see [Configure a trunk without media bypass in Lync Server 2013](lync-server-2013-configure-a-trunk-without-media-bypass.md).</span></span> <span data-ttu-id="759c6-108">Обход мультимедиа полезен, если вы хотите минимизировать количество развернутых серверов исправлений.</span><span class="sxs-lookup"><span data-stu-id="759c6-108">Media bypass is useful when you want to minimize the number of Mediation Servers deployed.</span></span> <span data-ttu-id="759c6-109">Обычно пул серверов-посредников будет развернут на центральном сайте, и он будет управлять шлюзами на сайтах филиалов.</span><span class="sxs-lookup"><span data-stu-id="759c6-109">Typically, a Mediation Server pool will be deployed at a central site, and it will control gateways at branch sites.</span></span> <span data-ttu-id="759c6-110">Включение обхода сервера-посредника позволяет проходить мультимедиа для вызовов ТСОП от клиентов на сайтах филиалов непосредственно через шлюзы на этих сайтах.</span><span class="sxs-lookup"><span data-stu-id="759c6-110">Enabling media bypass allows media for public switched telephone network (PSTN) calls from clients at branch sites to flow directly through the gateways at those sites.</span></span> <span data-ttu-id="759c6-111">В Lync Server 2013 маршруты исходящих вызовов и политики корпоративной голосовой связи должны быть настроены правильно, так что звонки между клиентами на сайте филиала направляются на соответствующий шлюз.</span><span class="sxs-lookup"><span data-stu-id="759c6-111">Lync Server 2013 outbound call routes and Enterprise Voice policies must be properly configured so that PSTN calls from clients at a branch site are routed to the appropriate gateway.</span></span>

<span data-ttu-id="759c6-112">Мы настоятельно рекомендуем включить обход мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="759c6-112">We strongly recommend that you enable media bypass.</span></span> <span data-ttu-id="759c6-113">Тем не менее, перед включением поддержки мультимедиа на магистральной магистрали SIP убедитесь в том, что поставщик магистральной магистрали SIP поддерживает обход мультимедиа и может обеспечить соответствие требованиям, предъявляемым к успешному включению сценария.</span><span class="sxs-lookup"><span data-stu-id="759c6-113">However, before you enable media bypass on a SIP trunk, confirm that your qualified SIP trunk provider supports media bypass and is able to accommodate the requirements for successfully enabling the scenario.</span></span> <span data-ttu-id="759c6-114">В частности, поставщик должен иметь IP-адреса серверов в внутренней сети Организации.</span><span class="sxs-lookup"><span data-stu-id="759c6-114">Specifically, the provider must have the IP addresses of servers in your organization’s internal network.</span></span> <span data-ttu-id="759c6-115">Если поставщик не поддерживает этот сценарий, обход мультимедиа не будет успешным.</span><span class="sxs-lookup"><span data-stu-id="759c6-115">If the provider cannot support this scenario, media bypass will not succeed.</span></span> <span data-ttu-id="759c6-116">Подробности можно найти [в разделе Планирование обхода мультимедиа в Lync Server 2013](lync-server-2013-planning-for-media-bypass.md) в документации по планированию.</span><span class="sxs-lookup"><span data-stu-id="759c6-116">For details, see [Planning for media bypass in Lync Server 2013](lync-server-2013-planning-for-media-bypass.md) in the Planning documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="759c6-117">Обход мультимедиа не будет взаимодействовать с каждым шлюзом коммутируемой телефонной сети (PSTN), IP-УАТС и контроллером границ сеанса (SBC).</span><span class="sxs-lookup"><span data-stu-id="759c6-117">Media bypass will not interoperate with every public switched telephone network (PSTN) gateway, IP-PBX, and Session Border Controller (SBC).</span></span> <span data-ttu-id="759c6-118">Корпорация Microsoft протестировала набор шлюзов ТСОП и контроллеров SBC с сертифицированными партнерами и провела некоторые тесты для Cisco IP-PBX.</span><span class="sxs-lookup"><span data-stu-id="759c6-118">Microsoft has tested a set of PSTN gateways and SBCs with certified partners and has done some testing with Cisco IP-PBXs.</span></span> <span data-ttu-id="759c6-119">Обход мультимедиа поддерживается только в том случае, если у вас есть продукты и версии, которые указаны в едином приложении для совместной работы с общедоступной программой Lync <A href="https://go.microsoft.com/fwlink/p/?linkid=214406">https://go.microsoft.com/fwlink/p/?linkId=214406</A> Server:</span><span class="sxs-lookup"><span data-stu-id="759c6-119">Media bypass is supported only with products and versions that are listed on Unified Communications Open Interoperability Program – Lync Server at <A href="https://go.microsoft.com/fwlink/p/?linkid=214406">https://go.microsoft.com/fwlink/p/?linkId=214406</A>.</span></span>



</div>

<span data-ttu-id="759c6-p104">Описанная ниже конфигурация магистрали содержит набор параметров, применяемых к магистралям, которым она назначается. Отдельная конфигурация магистрали может действовать в глобальной области (для всех магистралей, которым не назначена более конкретная конфигурация сайта или пула), в области сайта или в области пула. Конфигурация магистрали уровня пула используется для назначения отдельной магистрали.</span><span class="sxs-lookup"><span data-stu-id="759c6-p104">A trunk configuration as described below groups a set of parameters that are applied to trunks assigned this trunk configuration. A particular trunk configuration can be scoped globally (to all trunks that do not have more specific site or pool configuration), or to a site, or to a pool. The pool-level trunk configuration is used to scope a specific trunk configuration to a single trunk.</span></span>

<span id="BKMK_ConfigTrunkMediaBypassSteps"></span>

<div>

## <a name="to-configure-a-trunk-with-media-bypass"></a><span data-ttu-id="759c6-123">Настройка магистрали с обходом сервера-посредника</span><span class="sxs-lookup"><span data-stu-id="759c6-123">To configure a trunk with media bypass</span></span>

1.  <span data-ttu-id="759c6-124">Войдите на компьютер как член группы RTCUniversalServerAdmins или роли CsVoiceAdministrator, CsServerAdministrator или CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="759c6-124">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the CsVoiceAdministrator, CsServerAdministrator, or CsAdministrator role.</span></span> <span data-ttu-id="759c6-125">Дополнительные сведения можно найти [в разделе Делегирование разрешений на настройку в Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="759c6-125">For details, see [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="759c6-126">Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="759c6-126">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="759c6-127">Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="759c6-127">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="759c6-128">На левой панели навигации щелкните **Маршрутизация голосовой связи** и **Настройка магистрали**.</span><span class="sxs-lookup"><span data-stu-id="759c6-128">In the left navigation bar, click **Voice Routing**, and then click **Trunk Configuration**.</span></span>

4.  <span data-ttu-id="759c6-129">На странице **Настройка магистрали** воспользуйтесь одним из описанных ниже методов.</span><span class="sxs-lookup"><span data-stu-id="759c6-129">On the **Trunk Configuration** page, use one of the following methods to configure a trunk:</span></span>
    
      - <span data-ttu-id="759c6-130">Дважды щелкните имеющуюся магистраль (например, **Глобальную**), чтобы открыть окно **Изменение настройки магистрали**.</span><span class="sxs-lookup"><span data-stu-id="759c6-130">Double-click an existing trunk (for example, the **Global** trunk) to display the **Edit Trunk Configuration** dialog box.</span></span>
    
      - <span data-ttu-id="759c6-131">Нажмите **Создать** и выберите область для новой конфигурации магистрали:</span><span class="sxs-lookup"><span data-stu-id="759c6-131">Click **New**, and then select a scope for the new trunk configuration:</span></span>
        
          - <span data-ttu-id="759c6-132">**Магистраль сайта:** Выберите сайт для этой конфигурации канала и **выберите сайт**, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="759c6-132">**Site trunk:** Choose the site for this trunk configuration from **Select a Site**, and then click **OK**.</span></span> <span data-ttu-id="759c6-133">Обратите внимание, что сайты, для которых уже создана конфигурация магистрали, не отображаются в разделе **Выбор сайта**.</span><span class="sxs-lookup"><span data-stu-id="759c6-133">Note that if a trunk configuration has already been created for a site, the site does not appear in **Select a Site**.</span></span> <span data-ttu-id="759c6-134">Эта конфигурация будет применяться ко всем магистралям на сайте.</span><span class="sxs-lookup"><span data-stu-id="759c6-134">This trunk configuration will be applied to all trunks in the site.</span></span>
        
          - <span data-ttu-id="759c6-135">**Магистраль пула:** Выберите имя канала, к которому будет применена эта конфигурация магистрали.</span><span class="sxs-lookup"><span data-stu-id="759c6-135">**Pool trunk:** Choose the name of the trunk that this trunk configuration applies to.</span></span> <span data-ttu-id="759c6-136">Этот магистраль может быть корневым магистральом или любыми дополнительными магистральными магистрали, определенными в построителе топологии.</span><span class="sxs-lookup"><span data-stu-id="759c6-136">This trunk can be the root trunk or any additional trunks defined in Topology Builder.</span></span> <span data-ttu-id="759c6-137">В разделе **Выбор службы** нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="759c6-137">From **Select a Service**, click **OK**.</span></span> <span data-ttu-id="759c6-138">Обратите внимание, что магистрали, для которых уже создана конфигурация, не отображаются в разделе **Выбор службы**.</span><span class="sxs-lookup"><span data-stu-id="759c6-138">Note that if a trunk configuration has already been created for a specific trunk, the trunk does not appear in **Select a Service**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="759c6-139">Выбранную область конфигурации магистрали нельзя изменить.</span><span class="sxs-lookup"><span data-stu-id="759c6-139">After you select the scope of the trunk configuration, it cannot be changed.</span></span><BR><span data-ttu-id="759c6-140">Поле <STRONG>Название</STRONG> заполняется названием связанного с конфигурацией магистрали сайта или службы. Изменить его нельзя.</span><span class="sxs-lookup"><span data-stu-id="759c6-140">The <STRONG>Name</STRONG> field is prepopulated with the name of the trunk configuration’s associated site or service and cannot be changed.</span></span>

    
    </div>

5.  <span data-ttu-id="759c6-p109">Укажите значение в поле **Максимальное количество поддерживаемых предварительных диалогов**. Это максимальное число разветвленных ответов, которые может получить ТСОП-шлюз, IP-УАТС или пограничный контроллер сеансов ITSP (SBC) на запрос INVITE, отправленный серверу-посреднику. Значение по умолчанию: 20.</span><span class="sxs-lookup"><span data-stu-id="759c6-p109">Specify a value in **Maximum early dialogs supported**. This is the maximum number of forked responses a public switched telephone network (PSTN) gateway, IP-PBX, or ITSP Session Border Controller (SBC) can receive to an INVITE that it sent to the Mediation Server. The default value is 20.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="759c6-144">Перед сменой данного значения, проконсультируйтесь со своим поставщиком или производителем оборудования насчет информации о возможностях своей системы.</span><span class="sxs-lookup"><span data-stu-id="759c6-144">Before you change this value, consult your service provider or equipment manufacturer for details about the capabilities of your system.</span></span>

    
    </div>

6.  <span data-ttu-id="759c6-145">Выберите один из описанных ниже вариантов для **Уровня поддержки шифрования**.</span><span class="sxs-lookup"><span data-stu-id="759c6-145">Select one of the following **Encryption support level** options:</span></span>
    
      - <span data-ttu-id="759c6-146">**Обязательно:** Шифрование с помощью протокола передачи данных в режиме реального времени (SRTP) должно использоваться для защиты трафика между сервером-посредником и шлюзом или частным обменом филиалов (УАТС).</span><span class="sxs-lookup"><span data-stu-id="759c6-146">**Required:** Secure real-time transport protocol (SRTP) encryption must be used to help protect traffic between the Mediation Server and the gateway or private branch exchange (PBX).</span></span>
    
      - <span data-ttu-id="759c6-147">**Необязательно:** SRTP шифрование используется, если поставщик услуг или оборудования его поддерживает.</span><span class="sxs-lookup"><span data-stu-id="759c6-147">**Optional:** SRTP encryption will be used if the service provider or equipment manufacturer supports it.</span></span>
    
      - <span data-ttu-id="759c6-148">**Не поддерживается:** SRTP шифрование не поддерживается поставщиком услуг или производителем оборудования, поэтому оно не будет использоваться.</span><span class="sxs-lookup"><span data-stu-id="759c6-148">**Not Supported:** SRTP encryption is not supported by the service provider or equipment manufacturer and therefore will not be used.</span></span>

7.  <span data-ttu-id="759c6-149">Установите флажок **Включить режим обхода сервера-посредника**, если нужно, чтобы одноранговые узлы магистрали обходили сервер-посредник при передаче медиаданных.</span><span class="sxs-lookup"><span data-stu-id="759c6-149">Select the **Enable media bypass** check box if you want media to bypass the Mediation Server for processing by the trunk peer.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="759c6-150">Для успешной работы данного режима ТСОП-шлюз, IP-УАТС или пограничный контроллер сеансов ITSP должны иметь определенные возможности.</span><span class="sxs-lookup"><span data-stu-id="759c6-150">For media bypass to work successfully, the PSTN gateway, IP-PBX, or ITSP Session Border Controller must support certain capabilities.</span></span> <span data-ttu-id="759c6-151">Подробности можно найти <A href="lync-server-2013-planning-for-media-bypass.md">в разделе Планирование обхода мультимедиа в Lync Server 2013</A> в документации по планированию.</span><span class="sxs-lookup"><span data-stu-id="759c6-151">For details, see <A href="lync-server-2013-planning-for-media-bypass.md">Planning for media bypass in Lync Server 2013</A> in the Planning documentation.</span></span>

    
    </div>

8.  <span data-ttu-id="759c6-p111">Установите флажок **Централизованная обработка медиаданных**, если имеется хорошо известная конечная точка для медиаданных (например, ТСОП-шлюз, где завершение медиаданных имеет тот же IP что и завершение сигнала). Сбросьте данный флажок, если у магистрали нет такой точки.</span><span class="sxs-lookup"><span data-stu-id="759c6-p111">Select the **Centralized media processing** check box if there is a well-known media termination point (for example, a PSTN gateway where the media termination has the same IP as the signaling termination). Clear this check box if the trunk does not have a well-known media termination point.</span></span>

9.  <span data-ttu-id="759c6-154">Если магистральный одноранговый элемент поддерживает получение запросов на использование SIP от сервера обновлений, установите флажок **Разрешить отправку ссылку на шлюз** .</span><span class="sxs-lookup"><span data-stu-id="759c6-154">If the trunk peer supports receiving SIP REFER requests from the Mediation Server, select the **Enable sending refer to the gateway** check box.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="759c6-155">Если отключить данную опцию при установленной <STRONG>Включить режим обхода медиаданных</STRONG> потребуется указание дополнительных параметров.</span><span class="sxs-lookup"><span data-stu-id="759c6-155">If you disable this option while the <STRONG>Enable media bypass</STRONG> option is selected, additional settings are required.</span></span> <span data-ttu-id="759c6-156">Если узел магистрали не поддерживает получение запросов SIP REFER от сервера-посредника и включен режим обхода, необходимо также запустить командлет <STRONG>Set-CsTrunkConfiguration</STRONG>, чтобы отключить RTCP для активных и удерживаемых звонков и обеспечить нужные условия для обхода.</span><span class="sxs-lookup"><span data-stu-id="759c6-156">If the trunk peer does not support receiving SIP REFER requests from the Mediation Server and media bypass is enabled, you must also run the <STRONG>Set-CsTrunkConfiguration</STRONG> cmdlet to disable RTCP for active and held calls in order to support proper conditions for media bypass.</span></span> <span data-ttu-id="759c6-157">Подробные сведения можно найти в руководстве по <A href="lync-server-2013-lync-server-management-shell.md">среде управления Lync Server 2013</A> .</span><span class="sxs-lookup"><span data-stu-id="759c6-157">For details, see the <A href="lync-server-2013-lync-server-management-shell.md">Lync Server 2013 Management Shell</A> documentation.</span></span><BR><span data-ttu-id="759c6-158">Если необходимо, чтобы переключенные звонки обходили медиаданные и шлюз не поддерживал запросы SIP REFER, выберите <STRONG>Разрешить ссылку с использованием стороннего контроля вызовов</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="759c6-158">Alternatively, you can select <STRONG>Enable refer using third-party-call control</STRONG> if you want transferred calls to be media bypassed, and the gateway does not support SIP REFER requests.</span></span>

    
    </div>

10. <span data-ttu-id="759c6-159">(Необязательно) Чтобы включить маршрутизацию между магистральными линиями связи, сопоставьте и настройте записи режима работы с ТСОП для этой конфигурации магистральной линии связи.</span><span class="sxs-lookup"><span data-stu-id="759c6-159">(Optional) To enable inter-trunk routing, associate and configure PSTN usage records to this trunk configuration.</span></span> <span data-ttu-id="759c6-160">Использование PSTN, связанное с этой конфигурацией канала, будет применяться ко всем входящим звонкам через магистраль, не исходящий из конечной точки Lync.</span><span class="sxs-lookup"><span data-stu-id="759c6-160">The PSTN usages associated to this trunk configuration will be applied for all incoming calls through the trunk that is not originating from a Lync endpoint.</span></span> <span data-ttu-id="759c6-161">Чтобы управлять записями режима работы с ТСОП, связанными с конфигурацией магистральной линии связи, используйте один из приведенных ниже методов.</span><span class="sxs-lookup"><span data-stu-id="759c6-161">To manage PSTN usage records associated to a trunk configuration, use one of the following methods:</span></span>
    
      - <span data-ttu-id="759c6-162">Чтобы выбрать одну или несколько записей из списка всех записей использования PSTN, доступных в вашем корпоративном развертывании, нажмите кнопку **выбрать**.</span><span class="sxs-lookup"><span data-stu-id="759c6-162">To select one or more records from a list of all PSTN usage records available in your Enterprise Voice deployment, click **Select**.</span></span> <span data-ttu-id="759c6-163">Выделите записи, которые следует связать с этой конфигурацией магистральной линии связи, и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="759c6-163">Highlight the records you want to associate with this trunk configuration and then click **OK**.</span></span>
    
      - <span data-ttu-id="759c6-164">Чтобы удалить запись режима работы с ТСОП из этой конфигурации магистральной линии связи, выберите эту запись и щелкните **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="759c6-164">To remove a PSTN usage record from this trunk configuration, select the record and click **Remove**.</span></span>
    
      - <span data-ttu-id="759c6-165">Чтобы определить новую запись режима работы с ТСОП и сопоставить ее с этой конфигурацией магистральной линии связи, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="759c6-165">To define a new PSTN usage record and associate it with this trunk configuration, do the following:</span></span>
        
        1.  <span data-ttu-id="759c6-166">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="759c6-166">Click **New**.</span></span>
        
        2.  <span data-ttu-id="759c6-167">В поле **Имя** укажите уникальное описательное имя для записи.</span><span class="sxs-lookup"><span data-stu-id="759c6-167">In the **Name** field, specify a descriptive name for the record that is unique.</span></span>
            
            <div>
            

            > [!NOTE]  
            > <span data-ttu-id="759c6-p115">Имя записи о режиме работы с ТСОП не должно повторяться в пределах развертывания корпоративной голосовой связи. После сохранения записи поле <STRONG>Имя</STRONG> не доступно для редактирования.</span><span class="sxs-lookup"><span data-stu-id="759c6-p115">The PSTN usage record name must be unique within the Enterprise Voice deployment. After the record is saved, the <STRONG>Name</STRONG> field cannot be edited.</span></span>

            
            </div>
        
        3.  <span data-ttu-id="759c6-170">Используйте один из следующих методов для сопоставления и настройки маршрутов для этой записи режима работы с ТСОП:</span><span class="sxs-lookup"><span data-stu-id="759c6-170">Use one of the following methods to associate and configure routes for this PSTN usage record:</span></span>
            
              - <span data-ttu-id="759c6-171">Чтобы выбрать один или несколько маршрутов из списка всех доступных маршрутов в вашем корпоративном развертывании, нажмите кнопку **выбрать**.</span><span class="sxs-lookup"><span data-stu-id="759c6-171">To select one or more routes from the list of all available routes in your Enterprise Voice deployment, click **Select**.</span></span> <span data-ttu-id="759c6-172">Выделите маршруты, которые требуется сопоставить с этой записью режима работы с ТСОП, и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="759c6-172">Highlight the routes you want to associate with this PSTN usage record, and click **OK**.</span></span>
            
              - <span data-ttu-id="759c6-173">Чтобы удалить маршрут из записи режима работы с ТСОП, выберите этот маршрут и щелкните **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="759c6-173">To remove a route from the PSTN usage record, select the route, and click **Remove**.</span></span>
            
              - <span data-ttu-id="759c6-174">Чтобы определить новый маршрут и сопоставить его с этой записью режима работы с ТСОП, щелкните **Создать**.</span><span class="sxs-lookup"><span data-stu-id="759c6-174">To define a new route and associate it to this PSTN usage record, click **New**.</span></span> <span data-ttu-id="759c6-175">Дополнительные сведения можно найти [в разделе Создание голосовых маршрутов в Lync Server 2013](lync-server-2013-create-a-voice-route.md).</span><span class="sxs-lookup"><span data-stu-id="759c6-175">For details, see [Create a voice route in Lync Server 2013](lync-server-2013-create-a-voice-route.md).</span></span>
            
              - <span data-ttu-id="759c6-176">Чтобы изменить маршрут, сопоставленный с этой записью режима работы с ТСОП, выберите данный маршрут и щелкните **Подробнее**.</span><span class="sxs-lookup"><span data-stu-id="759c6-176">To edit a route that is associated with this PSTN usage record, select the route, and click **Show details**.</span></span> <span data-ttu-id="759c6-177">Подробности можно найти [в разделе Изменение голосового маршрута в Lync Server 2013](lync-server-2013-modify-a-voice-route.md).</span><span class="sxs-lookup"><span data-stu-id="759c6-177">For details, see [Modify a voice route in Lync Server 2013](lync-server-2013-modify-a-voice-route.md).</span></span>
        
        4.  <span data-ttu-id="759c6-178">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="759c6-178">Click **OK**.</span></span>
    
      - <span data-ttu-id="759c6-179">Чтобы изменить запись режима работы с ТСОП, уже сопоставленную с этой настройкой магистральной линии связи, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="759c6-179">To edit a PSTN usage record that is already associated with this trunk configuration, do the following:</span></span>
        
        1.  <span data-ttu-id="759c6-180">Выберите запись режима работы с ТСОП, которую требуется изменить, и щелкните **Подробнее**.</span><span class="sxs-lookup"><span data-stu-id="759c6-180">Select the PSTN usage record you want to edit, and click **Show details**.</span></span>
        
        2.  <span data-ttu-id="759c6-181">Используйте один из следующих методов для сопоставления и настройки маршрутов для этой записи режима работы с ТСОП:</span><span class="sxs-lookup"><span data-stu-id="759c6-181">Use one of the following methods to associate and configure routes for this PSTN usage record:</span></span>
            
              - <span data-ttu-id="759c6-182">Чтобы выбрать один или несколько маршрутов из списка всех доступных маршрутов в вашем корпоративном развертывании, нажмите кнопку **выбрать**.</span><span class="sxs-lookup"><span data-stu-id="759c6-182">To select one or more routes from the list of all available routes in your Enterprise Voice deployment, click **Select**.</span></span> <span data-ttu-id="759c6-183">Выделите маршруты, которые требуется сопоставить с этой записью режима работы с ТСОП, и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="759c6-183">Highlight the routes you want to associate with this PSTN usage record, and click **OK**.</span></span>
            
              - <span data-ttu-id="759c6-184">Чтобы удалить маршрут из записи режима работы с ТСОП, выберите этот маршрут и щелкните **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="759c6-184">To remove a route from the PSTN usage record, select the route, and click **Remove**.</span></span>
            
              - <span data-ttu-id="759c6-185">Чтобы определить новый маршрут и сопоставить его с этой записью режима работы с ТСОП, щелкните **Создать**.</span><span class="sxs-lookup"><span data-stu-id="759c6-185">To define a new route and associate it to this PSTN usage record, click **New**.</span></span> <span data-ttu-id="759c6-186">Дополнительные сведения можно найти [в разделе Создание голосовых маршрутов в Lync Server 2013](lync-server-2013-create-a-voice-route.md).</span><span class="sxs-lookup"><span data-stu-id="759c6-186">For details, see [Create a voice route in Lync Server 2013](lync-server-2013-create-a-voice-route.md).</span></span>
            
              - <span data-ttu-id="759c6-187">Чтобы изменить маршрут, сопоставленный с этой записью режима работы с ТСОП, выберите данный маршрут и щелкните **Подробнее**.</span><span class="sxs-lookup"><span data-stu-id="759c6-187">To edit a route that is associated with this PSTN usage record, select the route, and click **Show details**.</span></span> <span data-ttu-id="759c6-188">Подробности можно найти [в разделе Изменение голосового маршрута в Lync Server 2013](lync-server-2013-modify-a-voice-route.md).</span><span class="sxs-lookup"><span data-stu-id="759c6-188">For details, see [Modify a voice route in Lync Server 2013](lync-server-2013-modify-a-voice-route.md).</span></span>
        
        3.  <span data-ttu-id="759c6-189">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="759c6-189">Click **OK**.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="759c6-190">Важно связывать записи об использовании PSTN в соответствии с одноранговым элементом сервера, связанным с настройкой магистрали.</span><span class="sxs-lookup"><span data-stu-id="759c6-190">It important to associate PSTN usage records according to the Mediation Server peer that is associated to the trunk being configured.</span></span> <span data-ttu-id="759c6-191">Если узел сервера-партнера является шлюзом PSTN или контроллером границ сеанса (SBC), настоятельно рекомендуется, чтобы конфигурация магистрали не сопоставлена с записью использования PSTN, которая направляет маршруты в назначение PSTN или другие нижестоящие системы, подключенные через Lync Server.</span><span class="sxs-lookup"><span data-stu-id="759c6-191">If the Mediation Server peer is a PSTN gateway or a Session Border Controller (SBC), it is strongly recommended that the trunk configuration is not associated to a PSTN usage record that routes to a PSTN destination or any other downstream systems connected via Lync Server.</span></span>

    
    </div>

11. <span data-ttu-id="759c6-p123">Измените расположение записей режима работы с ТСОП, чтобы обеспечить оптимальную производительность. Чтобы изменить расположение записи в списке, выберите соответствующую запись режима работы с ТСОП и щелкните стрелку вверх или стрелку вниз.</span><span class="sxs-lookup"><span data-stu-id="759c6-p123">Arrange the PSTN usage records for optimum performance. To change a record’s position in the list, select the PSTN usage record, and click the up or down arrows.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="759c6-194">Порядок расположения записей режима работы с ТСОП в списке является важным.</span><span class="sxs-lookup"><span data-stu-id="759c6-194">The order in which PSTN usage records are listed in the trunk configuration is significant.</span></span> <span data-ttu-id="759c6-195">Lync Server обходит список сверху вниз.</span><span class="sxs-lookup"><span data-stu-id="759c6-195">Lync Server traverses the list from top to down.</span></span>

    
    </div>

12. <span data-ttu-id="759c6-196">Чтобы включить обход медиаданных для клиентов, защищенных системой преобразования сетевых адресов (NAT) или брандмауэром и SBC с поддержкой блокировки, выберите **Разрешить блокирование RTP**.</span><span class="sxs-lookup"><span data-stu-id="759c6-196">**Enable RTP Latching** should be selected to enable bypass media for clients behind a network address translation (NAT) or firewall and an SBC that supports latching.</span></span>

13. <span data-ttu-id="759c6-197">**Включите функцию "включить переадресацию звонков** ", чтобы разрешить отправку сведений из журнала звонков на узел шлюза на сервере обновлений.</span><span class="sxs-lookup"><span data-stu-id="759c6-197">**Enable forward call history** should be selected to enable sending of call history information to the gateway peer of the Mediation Server.</span></span>

14. <span data-ttu-id="759c6-198">**Включите функцию переадресации с Поутвержденными данными об удостоверениях** , чтобы включить в нее сведения о выдаче сигнала p-Assert (PAI), которые нужно перенаправить на сторону сервера-посредника и на сторону шлюза (и наоборот) (и наоборот).</span><span class="sxs-lookup"><span data-stu-id="759c6-198">**Enable forward P-Asserted-Identity data** should be selected to enable the P-Asserted-Identity (PAI) call originator information to be forwarded between the Mediation Server side and gateway side (and vice versa), when present.</span></span>

15. <span data-ttu-id="759c6-199">Чтобы включить быструю отработку отказа, выберите **Включить таймер отработки отказа внешней маршрутизации**.</span><span class="sxs-lookup"><span data-stu-id="759c6-199">**Enable outbound routing failover timer** should be selected to enable fast failover.</span></span> <span data-ttu-id="759c6-200">Шлюз, связанный с данной магистралью, может отправить уведомление об обработке исходящего вызова в течение 10 секунд.</span><span class="sxs-lookup"><span data-stu-id="759c6-200">The gateway associated with this trunk can give notification within 10 seconds that it is processing an outbound call.</span></span> <span data-ttu-id="759c6-201">Перенаправление на другую магистраль произойдет, если это уведомление не получено от сервера обновлений.</span><span class="sxs-lookup"><span data-stu-id="759c6-201">Rerouting to another trunk will occur if this notification is not received by the Mediation Server.</span></span> <span data-ttu-id="759c6-202">Для сетей с высокой задержкой, которая может увеличить время ответа, или для шлюзов, время отклика которых превышает 10 секунд, быстрая отработка отказа должна быть отключена.</span><span class="sxs-lookup"><span data-stu-id="759c6-202">On networks where latency may delay the response time or the gateway takes longer than 10 seconds to respond, the fast failover should be disabled.</span></span>

16. <span data-ttu-id="759c6-203">(Необязательно) Сопоставьте и настройте **правила трансляции вызывающего номера** для магистральной линии связи.</span><span class="sxs-lookup"><span data-stu-id="759c6-203">(Optional) Associate and configure **calling number translation rules** for the trunk.</span></span> <span data-ttu-id="759c6-204">Эти правила применяются к вызывающим номерам для исходящих вызовов</span><span class="sxs-lookup"><span data-stu-id="759c6-204">These translation rules apply to the calling number for outbound calls</span></span>
    
      - <span data-ttu-id="759c6-205">Чтобы выбрать одно или несколько правил из списка всех правил трансляции, доступных в вашем корпоративном развертывании, нажмите кнопку **выбрать**.</span><span class="sxs-lookup"><span data-stu-id="759c6-205">To choose one or more rules from a list of all translation rules that are available in your Enterprise Voice deployment, click **Select**.</span></span> <span data-ttu-id="759c6-206">В окне **Выбор правил трансляции** выберите правила, которые требуется сопоставить с магистральной линией связи, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="759c6-206">In **Select Translation Rules**, click the rules that you want to associate with the trunk, and then click **OK**.</span></span>
    
      - <span data-ttu-id="759c6-207">Чтобы определить новое правило преобразования и сопоставить его с магистральной линией связи, щелкните **Создать**.</span><span class="sxs-lookup"><span data-stu-id="759c6-207">To define a new translation rule and associate it with the trunk, click **New**.</span></span> <span data-ttu-id="759c6-208">Подробные сведения о том, как определить новое правило, приведены в разделе [Определение правил перевода в Lync Server 2013](lync-server-2013-defining-translation-rules.md) в документации по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="759c6-208">For details about defining a new rule, see [Defining translation rules in Lync Server 2013](lync-server-2013-defining-translation-rules.md) in the Deployment documentation.</span></span>
    
      - <span data-ttu-id="759c6-209">Чтобы изменить правило преобразования, уже сопоставленное с магистральной линией связи, щелкните имя правила, а затем выберите **Подробнее**.</span><span class="sxs-lookup"><span data-stu-id="759c6-209">To edit a translation rule that is already associated with the trunk, click the rule name, and then click **Show details**.</span></span> <span data-ttu-id="759c6-210">Подробности можно найти [в разделе Определение правил перевода в Lync Server 2013](lync-server-2013-defining-translation-rules.md) в документации по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="759c6-210">For details, see [Defining translation rules in Lync Server 2013](lync-server-2013-defining-translation-rules.md) in the Deployment documentation.</span></span>
    
      - <span data-ttu-id="759c6-211">Чтобы скопировать существующее правило преобразования и использовать его в качестве отправной точки для определения нового правила, щелкните имя этого правила, щелкните **Копировать** и **Вставить**.</span><span class="sxs-lookup"><span data-stu-id="759c6-211">To copy an existing translation rule to use as a starting point for defining a new rule, click the rule name and click **Copy**, and then click **Paste**.</span></span> <span data-ttu-id="759c6-212">Подробности можно найти [в разделе Определение правил перевода в Lync Server 2013](lync-server-2013-defining-translation-rules.md).</span><span class="sxs-lookup"><span data-stu-id="759c6-212">For details, see [Defining translation rules in Lync Server 2013](lync-server-2013-defining-translation-rules.md).</span></span>
    
      - <span data-ttu-id="759c6-213">Чтобы удалить правило преобразования из магистральной линии связи, выделите имя этого правила, а затем щелкните **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="759c6-213">To remove a translation rule from the trunk, highlight the rule name and click **Remove**.</span></span>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="759c6-214">Не сопоставляйте правила преобразования с магистральной линией связи, если вы уже настроили их для связанной одноранговой магистральной линии связи, поскольку эти два правила могут конфликтовать друг с другом.</span><span class="sxs-lookup"><span data-stu-id="759c6-214">Do not associate translation rules with a trunk if you have configured translation rules on the associated trunk peer, because the two rules might conflict.</span></span>

    
    </div>

17. <span data-ttu-id="759c6-p131">(Необязательно) Сопоставьте и настройте **правила трансляции набранного номера** для магистральной линии связи. Эти правила применяются к вызываемым номерам для исходящих вызовов.</span><span class="sxs-lookup"><span data-stu-id="759c6-p131">(Optional) Associate and configure **called number translation rules** for the trunk. The translation rules apply to the called number in an outbound call.</span></span>
    
      - <span data-ttu-id="759c6-217">Чтобы выбрать одно или несколько правил из списка всех правил трансляции, доступных в вашем корпоративном развертывании, нажмите кнопку **выбрать**.</span><span class="sxs-lookup"><span data-stu-id="759c6-217">To choose one or more rules from a list of all translation rules that are available in your Enterprise Voice deployment, click **Select**.</span></span> <span data-ttu-id="759c6-218">В окне **Выбор правил трансляции** выберите правила, которые требуется сопоставить с магистральной линией связи, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="759c6-218">In **Select Translation Rules**, click the rules that you want to associate with the trunk, and then click **OK**.</span></span>
    
      - <span data-ttu-id="759c6-219">Чтобы определить новое правило преобразования и сопоставить его с магистральной линией связи, щелкните **Создать**.</span><span class="sxs-lookup"><span data-stu-id="759c6-219">To define a new translation rule and associate it with the trunk, click **New**.</span></span> <span data-ttu-id="759c6-220">Подробные сведения о том, как определить новое правило, приведены в разделе [Определение правил перевода в Lync Server 2013](lync-server-2013-defining-translation-rules.md) в документации по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="759c6-220">For details about defining a new rule, see [Defining translation rules in Lync Server 2013](lync-server-2013-defining-translation-rules.md) in the Deployment documentation.</span></span>
    
      - <span data-ttu-id="759c6-221">Чтобы изменить правило преобразования, уже сопоставленное с магистральной линией связи, щелкните имя правила, а затем выберите **Подробнее**.</span><span class="sxs-lookup"><span data-stu-id="759c6-221">To edit a translation rule that is already associated with the trunk, click the rule name, and then click **Show details**.</span></span> <span data-ttu-id="759c6-222">Подробности можно найти [в разделе Определение правил перевода в Lync Server 2013](lync-server-2013-defining-translation-rules.md) в документации по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="759c6-222">For details, see [Defining translation rules in Lync Server 2013](lync-server-2013-defining-translation-rules.md) in the Deployment documentation.</span></span>
    
      - <span data-ttu-id="759c6-223">Чтобы скопировать существующее правило преобразования и использовать его в качестве отправной точки для определения нового правила, щелкните имя этого правила, щелкните **Копировать** и **Вставить**.</span><span class="sxs-lookup"><span data-stu-id="759c6-223">To copy an existing translation rule to use as a starting point for defining a new rule, click the rule name and click **Copy**, and then click **Paste**.</span></span> <span data-ttu-id="759c6-224">Подробности можно найти [в разделе Определение правил перевода в Lync Server 2013](lync-server-2013-defining-translation-rules.md).</span><span class="sxs-lookup"><span data-stu-id="759c6-224">For details, see [Defining translation rules in Lync Server 2013](lync-server-2013-defining-translation-rules.md).</span></span>
    
      - <span data-ttu-id="759c6-225">Чтобы удалить правило преобразования из магистральной линии связи, выделите имя этого правила, а затем щелкните **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="759c6-225">To remove a translation rule from the trunk, highlight the rule name and click **Remove**.</span></span>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="759c6-226">Не сопоставляйте правила преобразования с магистральной линией связи, если вы уже настроили их для связанной одноранговой магистральной линии связи, поскольку эти два правила могут конфликтовать друг с другом.</span><span class="sxs-lookup"><span data-stu-id="759c6-226">Do not associate translation rules with a trunk if you have configured translation rules on the associated trunk peer, because the two rules might conflict.</span></span>

    
    </div>

18. <span data-ttu-id="759c6-p136">Правила трансляции линии связи должны быть выстроены в правильном порядке. Для изменения позиции правила, выделите его в списке и нажмите кнопку со стрелкой вверх или вниз.</span><span class="sxs-lookup"><span data-stu-id="759c6-p136">Make sure that the trunk’s translation rules are arranged in the correct order. To change a rule’s position in the list, highlight the rule name and then click the up or down arrow.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="759c6-229">Lync Server 2013 обходит список правил перевода сверху вниз и использует первое правило, которое соответствует номеру набора.</span><span class="sxs-lookup"><span data-stu-id="759c6-229">Lync Server 2013 traverses the translation rule list from the top down and uses the first rule that matches the dialed number.</span></span> <span data-ttu-id="759c6-230">Если магистраль настроена так, что набранный номер может соответствовать нескольким правилам, то более строгие правила должны предшествовать менее строгим.</span><span class="sxs-lookup"><span data-stu-id="759c6-230">If you configure a trunk so that a dialed number can match more than one translation rule, be sure that the more restrictive rules are sorted above the less restrictive rules.</span></span> <span data-ttu-id="759c6-231">Например, если вы добавили правило трансляции, совпадающее с любым 11-значным номером и правило, совпадающее с 11-значным номером, начинающимся на +1425, то первое правило должно располагаться <EM>ниже</EM> второго, более строгого правила.</span><span class="sxs-lookup"><span data-stu-id="759c6-231">For example, if you have included a translation rule that matches any 11-digit number and a translation rule that matches only 11-digit numbers that start with +1425, be sure that the rule that matches any 11-digit number is sorted <EM>below</EM> the more restrictive rule.</span></span>

    
    </div>

19. <span data-ttu-id="759c6-232">После завершения настройки магистрали нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="759c6-232">When you are finished configuring the trunk, click **OK**.</span></span>

20. <span data-ttu-id="759c6-233">На странице **Настройка магистрали** нажмите **Фиксировать** и затем **Фиксировать все**.</span><span class="sxs-lookup"><span data-stu-id="759c6-233">On the **Trunk Configuration** page, click **Commit**, and then click **Commit all**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="759c6-234">После создания или изменения конфигурации магистрали следует выполнить команду <STRONG>Сохранить все</STRONG>, чтобы опубликовать изменения конфигурации.</span><span class="sxs-lookup"><span data-stu-id="759c6-234">Whenever you create or modify a trunk configuration, you must run the <STRONG>Commit all</STRONG> command to publish the configuration change.</span></span> <span data-ttu-id="759c6-235">Дополнительные сведения можно найти в разделе <A href="lync-server-2013-publish-pending-changes-to-the-voice-routing-configuration.md">Публикация ожидающих изменений в конфигурации голосовой маршрутизации в Lync Server 2013</A> в документации по эксплуатации.</span><span class="sxs-lookup"><span data-stu-id="759c6-235">For details, see <A href="lync-server-2013-publish-pending-changes-to-the-voice-routing-configuration.md">Publish pending changes to the voice routing configuration in Lync Server 2013</A> in the Operations documentation.</span></span>

    
    </div>

<span data-ttu-id="759c6-236">После настройки магистральной магистрали Продолжайте настраивать режим обхода мультимедиа, выбирая между глобальными параметрами обхода мультимедиа, как описано в разделе [Общие параметры обхода мультимедиа в Lync Server 2013](lync-server-2013-global-media-bypass-options.md) в документации по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="759c6-236">After you have configured the trunk, continue configuring media bypass by choosing between global media bypass options, as described in [Global media bypass options in Lync Server 2013](lync-server-2013-global-media-bypass-options.md) in the Deployment documentation.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="759c6-237">См. также</span><span class="sxs-lookup"><span data-stu-id="759c6-237">See Also</span></span>


[<span data-ttu-id="759c6-238">Настройка магистрали без обхода мультимедиа в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="759c6-238">Configure a trunk without media bypass in Lync Server 2013</span></span>](lync-server-2013-configure-a-trunk-without-media-bypass.md)  


[<span data-ttu-id="759c6-239">Настройка обхода сервера-посредника в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="759c6-239">Configure media bypass in Lync Server 2013</span></span>](lync-server-2013-configure-media-bypass.md)  
[<span data-ttu-id="759c6-240">Глобальные параметры обхода мультимедиа в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="759c6-240">Global media bypass options in Lync Server 2013</span></span>](lync-server-2013-global-media-bypass-options.md)  


[<span data-ttu-id="759c6-241">Определение правил преобразования в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="759c6-241">Defining translation rules in Lync Server 2013</span></span>](lync-server-2013-defining-translation-rules.md)  
  

<span data-ttu-id="759c6-242"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="759c6-242"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

