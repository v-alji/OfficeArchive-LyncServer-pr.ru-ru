---
title: 'Lync Server 2013: реализация распределения каналов SIP'
description: 'Lync Server 2013: как внедрить магистральные линии SIP?.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: How do I implement SIP trunking?
ms:assetid: 273a22b1-8a4c-4187-acf8-c57d5c6598ce
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425743(v=OCS.15)
ms:contentKeyID: 48183666
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 10882adc0bff573868dcd07268ed0446385d895c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427448"
---
# <a name="how-do-i-implement-sip-trunking-in-lync-server-2013"></a><span data-ttu-id="24934-103">Реализация распределения каналов SIP в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="24934-103">How do I implement SIP trunking in Lync Server 2013?</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="24934-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="24934-104">

<span> </span></span></span>

<span data-ttu-id="24934-105">_**Тема последнего изменения:** 2013-03-18_</span><span class="sxs-lookup"><span data-stu-id="24934-105">_**Topic Last Modified:** 2013-03-18_</span></span>

<span data-ttu-id="24934-106">Для реализации магистрали SIP необходимо перенаправлять подключение на сервер-посредник, который выступает в качестве прокси для сеансов связи между клиентами Lync Server 2013 и поставщиком услуг, и при необходимости перекодировать носитель.</span><span class="sxs-lookup"><span data-stu-id="24934-106">To implement SIP trunking, you must route the connection through a Mediation Server, which acts as a proxy for communications sessions between Lync Server 2013 clients and the service provider and transcodes media, when necessary.</span></span>

<span data-ttu-id="24934-107">У каждого сервера исправлений есть внутренний сетевой интерфейс и внешний сетевой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="24934-107">Each Mediation Server has an internal network interface and an external network interface.</span></span> <span data-ttu-id="24934-108">Внутренний интерфейс подключается к серверам переднего плана.</span><span class="sxs-lookup"><span data-stu-id="24934-108">The internal interface connects to the Front End Servers.</span></span> <span data-ttu-id="24934-109">Внешний интерфейс обычно называется интерфейсом шлюза, так как он обычно используется для подключения сервера-посредника к шлюзу КОММУТИРУЕМой телефонной сети, поддерживающей коммутируемую связь, или IP-УАТС.</span><span class="sxs-lookup"><span data-stu-id="24934-109">The external interface is commonly called the gateway interface because it has traditionally been used to connect the Mediation Server to a public switched telephone network (PSTN) gateway or an IP-PBX.</span></span> <span data-ttu-id="24934-110">Для реализации магистральной магистрали SIP вы подключаете внешний интерфейс сервера-посредника к внешнему компоненту EDGE в ITSP.</span><span class="sxs-lookup"><span data-stu-id="24934-110">To implement a SIP trunk, you connect the external interface of the Mediation Server to the external edge component of the ITSP.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="24934-111">Внешний пограничный компонент ITSP может быть пограничным контроллером сеансов (SBC), маршрутизатором или шлюзом.</span><span class="sxs-lookup"><span data-stu-id="24934-111">The external edge component of the ITSP could be a Session Border Controller (SBC), a router, or a gateway.</span></span>



</div>

<span data-ttu-id="24934-112">Подробнее об этих серверах можно найти [в разделе Сервер исправлений в Lync Server 2013](lync-server-2013-mediation-server-component.md).</span><span class="sxs-lookup"><span data-stu-id="24934-112">For details about Mediation Servers, see [Mediation Server component in Lync Server 2013](lync-server-2013-mediation-server-component.md).</span></span>

<div>

## <a name="centralized-vs-distributed-sip-trunking"></a><span data-ttu-id="24934-113">Централизованные и распределенные магистрали SIP</span><span class="sxs-lookup"><span data-stu-id="24934-113">Centralized vs. Distributed SIP Trunking</span></span>

<span data-ttu-id="24934-114">*Централизованная* С помощью магистрали SIP можно передавать трафик по протоколу голосовой почты через Интернет (VoIP), включая трафик сайтов филиалов, посредством центрального сайта.</span><span class="sxs-lookup"><span data-stu-id="24934-114">*Centralized* SIP trunking routes all Voice over Internet Protocol (VoIP) traffic, including branch site traffic, through your central site.</span></span> <span data-ttu-id="24934-115">Централизованная модель развертывания – это простой и экономичный подход, который обычно является рекомендуемым способом реализации каналов SIP с помощью Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="24934-115">The centralized deployment model is simple, cost-effective, and is generally the recommended approach for implementing SIP trunks with Lync Server 2013.</span></span>

<span data-ttu-id="24934-116">*Распространяется* Магистраль SIP — это модель развертывания, в которой вы реализуете локальную магистральную сеть SIP для одного или нескольких сайтов филиалов.</span><span class="sxs-lookup"><span data-stu-id="24934-116">*Distributed* SIP trunking is a deployment model in which you implement a local SIP trunk at one or more branch sites.</span></span> <span data-ttu-id="24934-117">Затем трафик VoIP перенаправляется от сайта филиала непосредственно поставщику услуг, не проходясь между центральным сайтом.</span><span class="sxs-lookup"><span data-stu-id="24934-117">VoIP traffic is then routed from the branch site directly to a service provider without going through the central site.</span></span>

<span data-ttu-id="24934-118">Распределенные магистрали SIP требуются только в следующих случаях.</span><span class="sxs-lookup"><span data-stu-id="24934-118">Distributed SIP trunking is required only in the following cases:</span></span>

  - <span data-ttu-id="24934-119">Для сайта филиала требуется бесперебойная телефонная связь (например, при отключении глобальной сети).</span><span class="sxs-lookup"><span data-stu-id="24934-119">The branch site requires survivable phone connectivity (for example, if the WAN goes down).</span></span> <span data-ttu-id="24934-120">Это требование необходимо проанализировать для каждого сайта ветви; для некоторых ветвей может потребоваться резервирование и переход на другой ресурс, в то время как другие могут.</span><span class="sxs-lookup"><span data-stu-id="24934-120">This requirement should be analyzed for each branch site; some of your branches may require redundancy and failover, whereas others may not.</span></span>

  - <span data-ttu-id="24934-121">Для двух центральных сайтов требуется устойчивость.</span><span class="sxs-lookup"><span data-stu-id="24934-121">Resiliency is required between two central sites.</span></span> <span data-ttu-id="24934-122">Необходимо убедиться, что на каждом центральном сайте завершается магистральная сеть SIP.</span><span class="sxs-lookup"><span data-stu-id="24934-122">You need to make sure that a SIP trunk terminates at each central site.</span></span> <span data-ttu-id="24934-123">Например, если у вас есть центральные сайты Дублин и Tukwila, и оба они используют только один сайт SIP, то при переходе на другую сеть пользователи не смогут звонить по протоколу PSTN.</span><span class="sxs-lookup"><span data-stu-id="24934-123">For example, if you have Dublin and Tukwila central sites and both use only one site’s SIP trunk, if the trunk goes down, the other site’s users cannot make PSTN calls.</span></span>

  - <span data-ttu-id="24934-124">Сайт ответвления и центральный сайт находятся в разных странах или регионах.</span><span class="sxs-lookup"><span data-stu-id="24934-124">The branch site and central site are in different countries/regions.</span></span> <span data-ttu-id="24934-125">По причинам обеспечения совместимости, а также по причинам правового характера требуется по крайней мере одна магистраль SIP на страну или регион.</span><span class="sxs-lookup"><span data-stu-id="24934-125">For compatibility and legal reasons, you need at least one SIP trunk per country/region.</span></span> <span data-ttu-id="24934-126">Например, в Евросоюзе коммуникации не могут покинуть страну или регион, не завершившись локально в централизованной точке.</span><span class="sxs-lookup"><span data-stu-id="24934-126">For example, in the European Union, communications cannot leave a country/region without terminating locally at a centralized point.</span></span>

<span data-ttu-id="24934-127">В зависимости от географического расположения сайтов и того, какой объем трафика вы планируете использовать в вашем предприятии, вам может не потребоваться перенаправлять всех пользователей через центральную магистральную телефонную сеть или перенаправлять некоторых пользователей через магистраль SIP на своем сайте филиала.</span><span class="sxs-lookup"><span data-stu-id="24934-127">Depending on the geographical location of sites and how much traffic you anticipate within your enterprise, you may not want to route all users through the central SIP trunk, or you may opt to route some users through a SIP trunk at their branch site.</span></span> <span data-ttu-id="24934-128">Для анализа своих потребностей, ответьте на следующие вопросы.</span><span class="sxs-lookup"><span data-stu-id="24934-128">To analyze your needs, answer the following questions:</span></span>

  - <span data-ttu-id="24934-129">Каковы все сайты (то есть сколько пользователей разрешено для корпоративной голосовой связи)?</span><span class="sxs-lookup"><span data-stu-id="24934-129">How big is each site (that is, how many users are enabled for Enterprise Voice)?</span></span>

  - <span data-ttu-id="24934-130">Сколько номеров прямого входного набора на каждом участке получает больше всего телефонных звонков?</span><span class="sxs-lookup"><span data-stu-id="24934-130">Which direct inward dialing (DID) numbers at each site get the most phone calls?</span></span>

<span data-ttu-id="24934-131">Принятие решения о развертывании централизованных или распределенных магистралей SIP требует проведения функционально-стоимостного анализа.</span><span class="sxs-lookup"><span data-stu-id="24934-131">The decision whether to deploy centralized or distributed SIP trunking requires a cost-benefit analysis.</span></span> <span data-ttu-id="24934-132">В некоторых случаях лучше выбрать распределенную модель развертывания, даже если этого не требуется.</span><span class="sxs-lookup"><span data-stu-id="24934-132">In some cases, it may be advantageous to opt for the distributed deployment model even if it is not required.</span></span> <span data-ttu-id="24934-133">В полностью централизованном развертывании трафик сайтов филиалов маршрутизируется по ссылкам WAN.</span><span class="sxs-lookup"><span data-stu-id="24934-133">In a completely centralized deployment, all branch site traffic is routed over WAN links.</span></span> <span data-ttu-id="24934-134">Вместо того, чтобы платить за полосу пропускания, необходимую для связи с WAN-каналами, возможно, вы предпочтете использование распределенных магистралей SIP.</span><span class="sxs-lookup"><span data-stu-id="24934-134">Instead of paying for the bandwidth required for WAN linking, you may want to use distributed SIP trunking.</span></span> <span data-ttu-id="24934-135">Например, вам может потребоваться развертывание стандартного сервера выпуска на сайте филиала с интеграцией на центральном сайте или развертывание бесперебойно работающего устройства филиала или работающего сервера подразделения с небольшим шлюзом.</span><span class="sxs-lookup"><span data-stu-id="24934-135">For example, you may want to deploy a Standard Edition server at a branch site with federation to the central site, or you may want to deploy a Survivable Branch Appliance or a Survivable Branch Server with a small gateway.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="24934-136">Подробнее об использовании распределенных магистральных каналов SIP можно узнать в статьях <A href="lync-server-2013-branch-site-sip-trunking.md">магистральные МАГИСТРАЛИ SIP сайтов филиалов в Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="24934-136">For details about distributed SIP trunking, see <A href="lync-server-2013-branch-site-sip-trunking.md">Branch site SIP trunking in Lync Server 2013</A>.</span></span>



</div>

</div>

<div>

## <a name="supported-sip-trunking-connection-types"></a><span data-ttu-id="24934-137">Поддерживаемые типы подключений для магистралей SIP</span><span class="sxs-lookup"><span data-stu-id="24934-137">Supported SIP Trunking Connection Types</span></span>

<span data-ttu-id="24934-138">Lync Server поддерживает следующие типы подключений для магистральной магистрали SIP:</span><span class="sxs-lookup"><span data-stu-id="24934-138">Lync Server supports the following connection types for SIP trunking:</span></span>

  - <span data-ttu-id="24934-p109">Технология мультипротокольной коммутации по меткам (MPLS) — это частная сеть, которая переносит и направляет данные из одного сетевого сайта на следующий. Полоса пропускания MPLS-сети разделяется с другими подписчиками, и каждому пакету данных назначается метка для различения данных одного подписчика от других пакетов. Для данного типа подключения виртуальная частная сеть (VPN) не требуется. Потенциальный недостаток — большое количество IP-трафика может сказаться на работе протокола VoIP, если последнему не дан приоритет.</span><span class="sxs-lookup"><span data-stu-id="24934-p109">Multiprotocol Label Switching (MPLS) is a private network that directs and carries data from one network node to the next. The bandwidth in an MPLS network is shared with other subscribers, and each data packet is assigned a label to distinguish one subscriber’s data from another’s. This connection type does not require a virtual private network (VPN). A potential drawback is that excessive IP traffic can interfere with VoIP operation unless VoIP traffic is given priority.</span></span>

  - <span data-ttu-id="24934-p110">Частное подключение без другого трафика, например арендованное оптоволоконное подключение или линия T1, обычно является наиболее надежным и безопасным методом подключения. Данный тип обеспечивает самую высокую способность выдерживать нагрузку, но и является самым дорогим. VPN-сеть не требуется. Частные подключения подходят для организаций с большим объемом звонков или строгими требованиями к безопасности и доступности.</span><span class="sxs-lookup"><span data-stu-id="24934-p110">A private connection with no other traffic—for example, a leased fiber-optic connection or T1 line—is typically the most reliable and secure connection type. This connection type provides the highest call-carrying capacity, but it is typically the most expensive. VPN is not required. Private connections are appropriate for organizations with high call volumes or stringent security and availability requirements.</span></span>

  - <span data-ttu-id="24934-147">Интернет — это наименее дорогой тип подключения, но и самый ненадежный.</span><span class="sxs-lookup"><span data-stu-id="24934-147">The Internet is the least expensive connection type, but it is also the least reliable.</span></span> <span data-ttu-id="24934-148">Подключение к Интернету — это единственный тип подключения к магистрали SIP сервера Lync Server, для которого требуется VPN.</span><span class="sxs-lookup"><span data-stu-id="24934-148">Internet connection is the only Lync Server SIP trunking connection type that requires VPN.</span></span>

<div>

## <a name="selecting-a-connection-type"></a><span data-ttu-id="24934-149">Выбор типа подключения</span><span class="sxs-lookup"><span data-stu-id="24934-149">Selecting a Connection Type</span></span>

<span data-ttu-id="24934-150">Наиболее подходящий для вашей организации тип подключения зависит от ваших потребностей и бюджета.</span><span class="sxs-lookup"><span data-stu-id="24934-150">The most appropriate SIP trunking connection type for your enterprise depends on your needs and your budget.</span></span>

  - <span data-ttu-id="24934-p112">Для средних и больших предприятий MPLS-сеть обычно подходит лучше всего. Она обеспечивает необходимую полосу пропускания по меньшей цене, чем специализированная частная сеть.</span><span class="sxs-lookup"><span data-stu-id="24934-p112">For a mid-size or larger enterprise, an MPLS network usually provides the greatest value. It can provide the necessary bandwidth at a cheaper rate than a specialized private network.</span></span>

  - <span data-ttu-id="24934-153">Для больших предприятий может потребовать отдельный оптоволоконный канал, линия T1, T3 или более высокого класса (E1, E3 или выше в Евросоюзе).</span><span class="sxs-lookup"><span data-stu-id="24934-153">Large enterprises may require a private fiber-optic, T1, T3 or higher connection (E1, E3 or higher in the European Union).</span></span>

  - <span data-ttu-id="24934-154">Для небольших организаций или сайтов филиалов с низким уровнем громкости звонка для этого лучше использовать функцию выбора SIP через Интернет.</span><span class="sxs-lookup"><span data-stu-id="24934-154">For a small enterprise or branch site with low call volume, SIP trunking through the Internet may be the best choice.</span></span> <span data-ttu-id="24934-155">Данный тип подключения не рекомендуется для сайтов среднего и большого размера.</span><span class="sxs-lookup"><span data-stu-id="24934-155">This connection type is not recommended for mid-size or larger sites.</span></span>

</div>

</div>

<div>

## <a name="bandwidth-requirements"></a><span data-ttu-id="24934-156">Требования к полосе пропускания</span><span class="sxs-lookup"><span data-stu-id="24934-156">Bandwidth Requirements</span></span>

<span data-ttu-id="24934-p114">Требуемая полоса пропускания зависит от количества одновременных звонков, которая система должна быть способна обрабатывать. Следует учитывать доступность полосы для реализации максимальной пропускной способности, за которую вы платите. Используйте следующую формулу для расчета требований к максимальной пропускной способности для магистрали SIP.</span><span class="sxs-lookup"><span data-stu-id="24934-p114">The amount of bandwidth your implementation requires depends on call capacity (the number of concurrent calls you must be able to support). You need to consider bandwidth availability, so that you can take full advantage of the peak capacity that you have paid for. Use the following formula to calculate SIP trunk peak bandwidth requirement:</span></span>

<span data-ttu-id="24934-160">Максимальная пропускная способность магистрали SIP = Макс. кол-во одновременных звонков x (64 кбит + размер заголовка)</span><span class="sxs-lookup"><span data-stu-id="24934-160">SIP Trunk Peak Bandwidth = Max Simultaneous Calls x (64 kbps + header size)</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="24934-161">Размер заголовка максимум 20 байт</span><span class="sxs-lookup"><span data-stu-id="24934-161">Header size is 20 bytes maximum.</span></span>



</div>

</div>

<div>

## <a name="codec-support"></a><span data-ttu-id="24934-162">Поддерживаемые кодеки</span><span class="sxs-lookup"><span data-stu-id="24934-162">Codec Support</span></span>

<span data-ttu-id="24934-163">Lync Server 2013 поддерживает только следующие кодеки:</span><span class="sxs-lookup"><span data-stu-id="24934-163">Lync Server 2013 supports only the following codecs:</span></span>

  - <span data-ttu-id="24934-164">G.711 a-law (в основном используется за пределами Северной Америки)</span><span class="sxs-lookup"><span data-stu-id="24934-164">G.711 a-law (used primarily outside North America)</span></span>

  - <span data-ttu-id="24934-165">G.711 µ-law (используется в Северной Америке)</span><span class="sxs-lookup"><span data-stu-id="24934-165">G.711 µ-law (used in North America)</span></span>

</div>

<div>

## <a name="internet-telephony-service-provider"></a><span data-ttu-id="24934-166">Поставщик услуг интернет-телефонии</span><span class="sxs-lookup"><span data-stu-id="24934-166">Internet Telephony Service Provider</span></span>

<span data-ttu-id="24934-167">Реализация подключения магистрали SIP к стороне поставщика услуг зависит от того или иного поставщика услуг интернет-телефонии (ITSP).</span><span class="sxs-lookup"><span data-stu-id="24934-167">How you implement the service provider side of a SIP trunk connection varies from one ITSP to another.</span></span> <span data-ttu-id="24934-168">Для получения сведений о развертывании свяжитесь со своим поставщиком услуг.</span><span class="sxs-lookup"><span data-stu-id="24934-168">For deployment information, contact your service provider.</span></span> <span data-ttu-id="24934-169">Список сертифицированных поставщиков услуг магистральной магистрали SIP можно найти на [веб-сайте унифицированной программы взаимодействия Microsoft Open Communications](https://go.microsoft.com/fwlink/?linkid=287029).</span><span class="sxs-lookup"><span data-stu-id="24934-169">For a list of certified SIP trunking service providers, see [Microsoft Unified Communications Open Interoperability Program website](https://go.microsoft.com/fwlink/?linkid=287029).</span></span>

<span data-ttu-id="24934-170">Дополнительные сведения о сертифицированных корпорацией Майкрософт поставщиках транкинга SIP можно получить, связавшись с вашим представителем Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="24934-170">For details about Microsoft certified SIP trunking providers, contact your Microsoft representative.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="24934-p116">Вам следует работать с сертифицированным корпорацией Майкрософт поставщиком услуг, чтобы ваш ITSP обеспечил весь функционал магистрали SIP (например, должны поддерживаться функции настройки и управления сеансами и все расширенные службы VoIP). Техническая поддержка Майкрософт не распространяется на конфигурации, в которых используются услуги несертифицированных поставщиков услуг. Если в данный момент вы пользуетесь услугами поставщика интернет-телефонии, не сертифицированного для магистралей SIP, можно оставить его в качестве интернет-оператора и перейти к использованию услуг поставщика транкинга SIP, сертифицированного корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="24934-p116">You must use a Microsoft certified service provider to ensure that your ITSP supports all of the functionality that traverses the SIP trunk (for example, setting up and managing sessions and supporting all of the extended VoIP services). Microsoft technical support does not extend to configurations that use noncertified providers. If you currently use an Internet service provider that is not certified for SIP trunking, you can opt to continue using that provider as your ISP and use a provider certified by Microsoft for SIP trunking.</span></span>



<span data-ttu-id="24934-174"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="24934-174"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

