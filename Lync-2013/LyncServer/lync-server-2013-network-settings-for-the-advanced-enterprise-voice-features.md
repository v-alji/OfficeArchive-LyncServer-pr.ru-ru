---
title: 'Lync Server 2013: сетевые параметры для расширенных корпоративных функций голосовой связи'
description: 'Lync Server 2013: сетевые параметры расширенных функций голосовой связи для предприятий.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Network settings for the advanced Enterprise Voice features
ms:assetid: 7f6de9e4-c8a4-44e4-8d14-21fe8c45283a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398637(v=OCS.15)
ms:contentKeyID: 48184632
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 42f04ba78a4cd2114e6ecffb5b92a7a54facb0df
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445549"
---
# <a name="network-settings-for-the-advanced-enterprise-voice-features-in-lync-server-2013"></a><span data-ttu-id="2b1e2-103">Network settings for the advanced Enterprise Voice features in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2b1e2-103">Network settings for the advanced Enterprise Voice features in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2b1e2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2b1e2-104">

<span> </span></span></span>

<span data-ttu-id="2b1e2-105">_**Тема последнего изменения:** 2012-10-10_</span><span class="sxs-lookup"><span data-stu-id="2b1e2-105">_**Topic Last Modified:** 2012-10-10_</span></span>

<span data-ttu-id="2b1e2-106">На сервере Lync Server есть три опытных услуги голосовой связи: управление допуском звонков (CAC), службы экстренной помощи (E9-1) и обход мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-106">Lync Server has three advanced Enterprise Voice features: call admission control (CAC), emergency services (E9-1-1), and media bypass.</span></span> <span data-ttu-id="2b1e2-107">Эти функции используются для предоставления определенных требований к конфигурации для сетевых регионов, сетевых сайтов и связей каждой подсети в топологии сервера Lync с сетевым сайтом.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-107">These features share certain configuration requirements for network regions, network sites, and association of each subnet in the Lync Server topology with a network site.</span></span> <span data-ttu-id="2b1e2-108">Подробные сведения о планировании развертывания этих функций можно найти в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="2b1e2-108">For details about planning for deployment of these features, see:</span></span>

  - [<span data-ttu-id="2b1e2-109">Планирование контроля допуска звонков в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2b1e2-109">Planning for call admission control in Lync Server 2013</span></span>](lync-server-2013-planning-for-call-admission-control.md)

  - [<span data-ttu-id="2b1e2-110">Планирование чрезвычайных служб (E9-1-1) в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2b1e2-110">Planning for emergency services (E9-1-1) in Lync Server 2013</span></span>](lync-server-2013-planning-for-emergency-services-e9-1-1.md)

  - [<span data-ttu-id="2b1e2-111">Планирование обхода серверов-посредников в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2b1e2-111">Planning for media bypass in Lync Server 2013</span></span>](lync-server-2013-planning-for-media-bypass.md)

<span data-ttu-id="2b1e2-112">Подробнее о том, как развертывать каждую из этих функций, можно найти [в разделе Развертывание дополнительных функций голосовой связи в Lync Server 2013](lync-server-2013-deploying-advanced-enterprise-voice-features.md) в документации по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-112">For details about deploying each of these features, see [Deploying advanced Enterprise Voice features in Lync Server 2013](lync-server-2013-deploying-advanced-enterprise-voice-features.md) in the Deployment documentation.</span></span>

<span data-ttu-id="2b1e2-113">В этом разделе приводятся общие сведения о требованиях к конфигурации, которые являются общими для всех трех улучшенных корпоративных голосовых функций.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-113">This topic provides an overview of the configuration requirements that are common to all three advanced Enterprise Voice features.</span></span>

<div>

## <a name="network-regions"></a><span data-ttu-id="2b1e2-114">Сетевые регионы</span><span class="sxs-lookup"><span data-stu-id="2b1e2-114">Network Regions</span></span>

<span data-ttu-id="2b1e2-115">Сетевой регион — это сетевой концентратор или сетевая магистраль, которые используются только в конфигурации контроля допуска звонков (CAC), служб экстренной помощи и обхода сервера-посредника.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-115">A network region is a network hub or network backbone used only in the configuration of call admission control (CAC), E9-1-1, and media bypass.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="2b1e2-116">Регионы сети не совпадают с областями конференц-связи с телефонным подключением Lync Server, которые необходимы для сопоставления номеров доступа для конференц-связи с телефонным подключением с помощью одной или нескольких абонентов Lync Server.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-116">Network regions are not the same as Lync Server dial-in conferencing regions, which are required to associate dial-in conferencing access numbers with one or more Lync Server dial plans.</span></span> <span data-ttu-id="2b1e2-117">Подробнее об областях конференц-связи с телефонным подключением можно найти <A href="lync-server-2013-dial-in-conferencing-requirements.md">в разделе Требования к конференциям с телефонным подключением в Lync Server 2013</A> в документации по планированию.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-117">For details about dial-in conferencing regions, see <A href="lync-server-2013-dial-in-conferencing-requirements.md">Dial-in conferencing requirements in Lync Server 2013</A> in the Planning documentation.</span></span>



</div>

<span data-ttu-id="2b1e2-118">Для использования CAC требуется, чтобы у каждого сетевого региона был связанный центральный сайт Lync Server, который управляет трафиком мультимедиа в регионе (то есть принимают решения на основе настроенных политик, в зависимости от того, можно ли установить звуковой или видеосеанс в реальном времени).</span><span class="sxs-lookup"><span data-stu-id="2b1e2-118">CAC requires that every network region have an associated Lync Server central site, which manages media traffic within the region (that is, it makes decisions based on policies that you have configured, regarding whether or not a real-time audio or video session can be established).</span></span> <span data-ttu-id="2b1e2-119">Центральные сайты Lync Server не представляют географические расположения, а логические группы серверов, которые настроены как пул или набор пулов.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-119">Lync Server central sites do not represent geographical locations, but rather logical groups of servers that are configured as a pool or a set of pools.</span></span> <span data-ttu-id="2b1e2-120">Подробнее об основных сайтах можно найти [в разделе топологии ссылок в Lync Server 2013](lync-server-2013-reference-topologies.md) в документации по планированию.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-120">For details about central sites, see [Reference topologies in Lync Server 2013](lync-server-2013-reference-topologies.md) in the Planning documentation.</span></span> <span data-ttu-id="2b1e2-121">[Поддерживаемые топологии в Lync Server 2013](lync-server-2013-supported-topologies.md) можно найти в документации по поддержке.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-121">Also see [Supported topologies in Lync Server 2013](lync-server-2013-supported-topologies.md) in the Supportability documentation.</span></span>

<span data-ttu-id="2b1e2-122">Чтобы настроить сетевой регион, вы можете воспользоваться вкладкой **регионы** в разделе **Сетевая конфигурация** на панели управления Lync Server или выполнить командлеты **New-CsNetworkRegion** или **Set-CsNetworkRegion** Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-122">To configure a network region, you can either use the **Regions** tab on the **Network Configuration** section of Lync Server Control Panel, or run the **New-CsNetworkRegion** or **Set-CsNetworkRegion** Lync Server Management Shell cmdlets.</span></span> <span data-ttu-id="2b1e2-123">Инструкции читайте в статье [Создание или изменение сетевого региона в Lync Server 2013](lync-server-2013-create-or-modify-a-network-region.md) в документации по развертыванию или ссылка на документацию по консоли управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-123">For instructions, see [Create or modify a network region in Lync Server 2013](lync-server-2013-create-or-modify-a-network-region.md) in the Deployment documentation, or refer to the Lync Server Management Shell documentation.</span></span>

<span data-ttu-id="2b1e2-124">Одни и те же определения сетевого региона совместно используются всеми тремя расширенными корпоративными голосовыми функциями.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-124">The same network region definitions are shared by all three advanced Enterprise Voice features.</span></span> <span data-ttu-id="2b1e2-125">Если сетевые регионы уже были созданы для одной функции, то для остальных функций не требуется создание новых сетевых регионов.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-125">If you have already created network regions for one feature, you do not need to create new network regions for the other features.</span></span> <span data-ttu-id="2b1e2-126">Но может потребоваться изменить существующее определение сетевых регионов, чтобы применить параметры для определенной функции.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-126">You may, however, need to modify an existing network region definition to apply feature-specific settings.</span></span> <span data-ttu-id="2b1e2-127">Например, если созданы сетевые регионы для служб экстренной помощи (E9-1-1) (которым не требуется связанный центральный сайт), а затем разворачивается контроль допуска звонков, то необходимо изменить каждое определение сетевого региона, чтобы указать центральный сайт.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-127">For example, if you have created network regions for E9-1-1 (which do not require an associated central site) and, later, you deploy call admission control, you must modify each of the network region definitions to specify a central site.</span></span>

<span data-ttu-id="2b1e2-128">Чтобы связать центральный сайт Lync Server с сетевым регионом, укажите имя центрального сайта: с помощью раздела " **Настройка сети** " панели управления Lync Server или с помощью командлетов **New-CsNetworkRegion** или **Set-CsNetworkRegion** Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-128">To associate a Lync Server central site with a network region, you specify the central site name, either by using the **Network Configuration** section of Lync Server Control Panel, or by running the **New-CsNetworkRegion** or **Set-CsNetworkRegion** Lync Server Management Shell cmdlets.</span></span> <span data-ttu-id="2b1e2-129">Инструкции читайте в статье [Создание или изменение сетевого региона в Lync Server 2013](lync-server-2013-create-or-modify-a-network-region.md) в документации по развертыванию или ссылка на документацию по консоли управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-129">For instructions, see [Create or modify a network region in Lync Server 2013](lync-server-2013-create-or-modify-a-network-region.md) in the Deployment documentation, or refer to the Lync Server Management Shell documentation.</span></span>

</div>

<div>

## <a name="network-sites"></a><span data-ttu-id="2b1e2-130">Сетевые сайты</span><span class="sxs-lookup"><span data-stu-id="2b1e2-130">Network Sites</span></span>

<span data-ttu-id="2b1e2-p107">Сетевой сайт представляет географическое расположение, такое как филиал, региональное отделение или главный офис. Каждый сетевой сайт должен быть связан с конкретным сетевым регионом.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-p107">A network site represents a geographical location, such as a branch office, a regional office, or a main office. Each network site must be associated with a specific network region.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="2b1e2-133">Сетевые сайты используются только расширенными корпоративными голосовыми функциями.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-133">Network sites are used only by the advanced Enterprise Voice features.</span></span> <span data-ttu-id="2b1e2-134">Они не совпадают с сайтами филиалов, которые настроены в топологии сервера Lync.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-134">They are not the same as the branch sites that you configure in your Lync Server topology.</span></span> <span data-ttu-id="2b1e2-135">Дополнительные сведения о сайтах филиалов можно найти <A href="lync-server-2013-reference-topologies.md">в разделе топологии ссылок в Lync Server 2013</A> в документации по планированию.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-135">For details about branch sites, see <A href="lync-server-2013-reference-topologies.md">Reference topologies in Lync Server 2013</A> in the Planning documentation.</span></span> <span data-ttu-id="2b1e2-136"><A href="lync-server-2013-supported-topologies.md">Поддерживаемые топологии в Lync Server 2013</A> можно найти в документации по поддержке.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-136">Also see <A href="lync-server-2013-supported-topologies.md">Supported topologies in Lync Server 2013</A> in the Supportability documentation.</span></span>



</div>

<span data-ttu-id="2b1e2-137">Чтобы настроить сайт сети и связать его с сетевым регионом, вы можете либо использовать раздел " **Настройка сети** " на панели управления Lync Server, либо запустить командлеты **New-CsNetworkSite** или **Set-CsNetworkSite** на Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-137">To configure a network site and associate it with a network region, you can either use the **Network Configuration** section of Lync Server Control Panel, or run the Lync Server Management Shell **New-CsNetworkSite** or **Set-CsNetworkSite** cmdlets.</span></span> <span data-ttu-id="2b1e2-138">Подробнее читайте в статье [Создание или изменение сетевого сайта в Lync Server 2013](lync-server-2013-create-or-modify-a-network-site.md) в документации по развертыванию или ссылка на документацию по консоли управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-138">For details, see [Create or modify a network site in Lync Server 2013](lync-server-2013-create-or-modify-a-network-site.md) in the Deployment documentation, or refer to the Lync Server Management Shell documentation.</span></span>

</div>

<div>

## <a name="identify-ip-subnets"></a><span data-ttu-id="2b1e2-139">Определение IP-подсетей</span><span class="sxs-lookup"><span data-stu-id="2b1e2-139">Identify IP Subnets</span></span>

<span data-ttu-id="2b1e2-p110">Для каждого сетевого сайта потребуется совместно с администратором сети определить, какая IP-подсеть назначена этому сетевому сайту. Если ваш администратор сети уже организовал IP-подсети в сетевые регионы и сетевые сайты, ваша работа значительно облегчается.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-p110">For each network site, you will need to work with your network administrator to determine which IP subnets are assigned to each network site. If your network administrator has already organized the IP subnets into network regions and network sites, then your work is significantly simplified.</span></span>

<span data-ttu-id="2b1e2-p111">В нашем примере сайту "Нью-Йорк" в регионе "Северная Америка" назначены следующие IP-подсети: 172.29.80.0/23, 157.57.216.0/25, 172.29.91.0/23, 172.29.81.0/24. Когда Боб, который обычно работает в Детройте, приезжает в офис в Нью-Йорке для прохождения обучения, он включает свой компьютер и подключается к сети, его компьютер получает IP-адрес в одном из четырех диапазонов, выделенных для Нью-Йорка, например 172.29.80.103.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-p111">For example, the New York site in the North America region can be assigned the following IP subnets: 172.29.80.0/23, 157.57.216.0/25, 172.29.91.0/23, 172.29.81.0/24. If Bob, who usually works in Detroit, travels to the New York office for training, turns on his computer and connects to the network, his computer will get an IP address in one of the four ranges that are allocated for New York—for example, 172.29.80.103.</span></span>

<div>


> [!WARNING]  
> <span data-ttu-id="2b1e2-144">IP-подсети, заданные во время конфигурации сети на сервере, должны соответствовать формату, предоставленному клиентскими компьютерами, чтобы они использовались соответствующим образом для обхода сервера-посредника.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-144">The IP subnets specified during network configuration on the server must match the format that is provided by client computers in order to be properly used for media bypass.</span></span> <span data-ttu-id="2b1e2-145">Клиент Lync принимает свой локальный IP-адрес и маскирует IP-адрес с помощью соответствующей маски подсети.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-145">A Lync client takes its local IP address and masks the IP address with the associated subnet mask.</span></span> <span data-ttu-id="2b1e2-146">При определении идентификатора обхода, связанного с каждым клиентом, регистратор будет сравнивать список IP-подсетей, связанных с каждым сетевым сайтом, с подсетью, предоставленной клиентом, и искать точное совпадение.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-146">When determining the bypass ID associated with each client, the Registrar will compare the list of IP subnets associated with each network site against the subnet that is provided by the client for an exact match.</span></span> <span data-ttu-id="2b1e2-147">По этой причине важно, чтобы подсети, указанные при конфигурации сети на сервере, были не виртуальными, а реальными подсетями.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-147">For this reason, it is important that subnets entered during network configuration on the server are actual subnets instead of virtual subnets.</span></span> <span data-ttu-id="2b1e2-148">(Если разворачивается контроль допуска звонков, а не обход сервера-посредника, то контроль допуска звонков будет работать должным образом даже при настройке виртуальных подсетей.)</span><span class="sxs-lookup"><span data-stu-id="2b1e2-148">(If you deploy call admission control, but not media bypass, call admission control will function properly even if you configure virtual subnets.)</span></span><BR><span data-ttu-id="2b1e2-149">Например, если клиент Lync выполняет вход на компьютере с IP-адресом 172.29.81.57 с маской подсети IP 255.255.255.0, он запрашивает идентификатор обхода, связанный с подсетью 172.29.81.0.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-149">For example, if a Lync client signs in on a computer with an IP address of 172.29.81.57 with an IP subnet mask of 255.255.255.0, it will request the bypass ID that is associated with subnet 172.29.81.0.</span></span> <span data-ttu-id="2b1e2-150">Если подсеть определена как 172.29.0.0/16, то хотя клиент принадлежит к этой виртуальной подсети, регистратор не будет считать это соответствием, поскольку точно ищет подсеть 172.29.81.0.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-150">If the subnet is defined as 172.29.0.0/16, although the client belongs to the virtual subnet, the Registrar will not consider this a match because the Registrar is specifically looking for subnet 172.29.81.0.</span></span> <span data-ttu-id="2b1e2-151">Таким образом, важно, чтобы администратор ввел подсети точно так же, как и в клиентах Lync (которые доставляются с подсетями в процессе настройки сети, статически или по протоколу DHCP).</span><span class="sxs-lookup"><span data-stu-id="2b1e2-151">Therefore, it is important that the administrator enters subnets exactly as provided by Lync clients (which are provisioned with subnets during network configuration, either statically or by Dynamic Host Configuration Protocol (DHCP).)</span></span>



</div>

</div>

<div>

## <a name="associating-subnets-with-network-sites"></a><span data-ttu-id="2b1e2-152">Сопоставление подсетей с сетевыми сайтами</span><span class="sxs-lookup"><span data-stu-id="2b1e2-152">Associating Subnets with Network Sites</span></span>

<span data-ttu-id="2b1e2-153">Каждая подсеть в корпоративной сети должна быть связана с сетевым сайтом (т.е. каждая подсеть должна быть связана с географическим расположением).</span><span class="sxs-lookup"><span data-stu-id="2b1e2-153">Every subnet in the enterprise network must be associated with a network site (that is, every subnet needs to be associated with a geographic location).</span></span> <span data-ttu-id="2b1e2-154">Такая ассоциация подсетей позволяет дополнительно находить конечные точки в графических элементах предприятия.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-154">This association of subnets enables the advanced Enterprise Voice features to locate the endpoints geographically.</span></span> <span data-ttu-id="2b1e2-155">Например, обнаружение конечных точек позволяет функции контроля допуска звонков регулировать поток аудио- и видео данных в режиме реального времени, приходящий на этот сетевой сайт и исходящий из него.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-155">For example, locating the endpoints enables CAC to regulate the flow of real-time audio and video data going to and from the network site.</span></span>

<span data-ttu-id="2b1e2-156">Чтобы связать подсети с сетевыми сайтами, вы можете использовать раздел " **Настройка сети** " на панели управления Lync Server или консоль управления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-156">To associate subnets with network sites, you can either use the **Network Configuration** section of Lync Server Control Panel, or you can use the Lync Server Management Shell.</span></span> <span data-ttu-id="2b1e2-157">Инструкции можно найти в разделе [Сопоставление подсети с сетевым сайтом в Lync Server 2013](lync-server-2013-associate-a-subnet-with-a-network-site.md) в документации по развертыванию или ознакомьтесь с документацией по командной консоли Lync Server.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-157">For instructions, see [Associate a subnet with a network site in Lync Server 2013](lync-server-2013-associate-a-subnet-with-a-network-site.md) in the Deployment documentation, or refer to the Lync Server Management Shell documentation.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="2b1e2-158">См. также</span><span class="sxs-lookup"><span data-stu-id="2b1e2-158">See Also</span></span>


[<span data-ttu-id="2b1e2-159">Планирование контроля допуска звонков в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2b1e2-159">Planning for call admission control in Lync Server 2013</span></span>](lync-server-2013-planning-for-call-admission-control.md)  
[<span data-ttu-id="2b1e2-160">Планирование чрезвычайных служб (E9-1-1) в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2b1e2-160">Planning for emergency services (E9-1-1) in Lync Server 2013</span></span>](lync-server-2013-planning-for-emergency-services-e9-1-1.md)  
[<span data-ttu-id="2b1e2-161">Планирование обхода серверов-посредников в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2b1e2-161">Planning for media bypass in Lync Server 2013</span></span>](lync-server-2013-planning-for-media-bypass.md)  
  

<span data-ttu-id="2b1e2-162"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2b1e2-162"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

