---
title: 'Lync Server 2013: сервер компонента "исправления"'
description: 'Lync Server 2013: серверный компонент "исправления".'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Mediation Server component
ms:assetid: 5b19edef-4a54-43c9-aa12-5643b8108355
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398399(v=OCS.15)
ms:contentKeyID: 48184239
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 08c11bff3ee7077d991204cda5a9885787c50ec2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445977"
---
# <a name="mediation-server-component-in-lync-server-2013"></a><span data-ttu-id="e18cd-103">Компонент сервера «исправления» в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e18cd-103">Mediation Server component in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e18cd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e18cd-104">

<span> </span></span></span>

<span data-ttu-id="e18cd-105">_**Тема последнего изменения:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="e18cd-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="e18cd-106">При развертывании корпоративной голосовой связи необходимо развернуть сервер Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e18cd-106">You must deploy Lync Server 2013, Mediation Server if you deploy the Enterprise Voice workload.</span></span> <span data-ttu-id="e18cd-107">В этом разделе описаны основные функциональные возможности, зависимости, основные топологии и руководство по планированию.</span><span class="sxs-lookup"><span data-stu-id="e18cd-107">This section describes basic functionality, dependencies, basic topologies, and planning guidelines.</span></span>

<span data-ttu-id="e18cd-108">Сервер-посредник транслирует сигнализацию и, в некоторых случаях, носители между внутренней конфигурацией Lync Server 2013, корпоративной голосовой связью и шлюзом коммутируемой телефонной сети (PSTN) или магистральным протоколом SIP.</span><span class="sxs-lookup"><span data-stu-id="e18cd-108">The Mediation Server translates signaling and, in some configurations, media between your internal Lync Server 2013, Enterprise Voice infrastructure and a public switched telephone network (PSTN) gateway or a Session Initiation Protocol (SIP) trunk.</span></span> <span data-ttu-id="e18cd-109">На стороне Lync Server 2013 сервер исправлений прослушивает один транспортный адрес взаимного TLS (MTLS).</span><span class="sxs-lookup"><span data-stu-id="e18cd-109">On the Lync Server 2013 side, Mediation Server listens on a single mutual TLS (MTLS) transport address.</span></span> <span data-ttu-id="e18cd-110">На стороне шлюза сервер исправления прослушивает все связанные с портами прослушивания, связанные с магистральными соединениями, определенными в документе Topology.</span><span class="sxs-lookup"><span data-stu-id="e18cd-110">On the gateway side, Mediation Server listens on all associated listening ports associated with trunks defined in the Topology document.</span></span> <span data-ttu-id="e18cd-111">Все соответствующие шлюзы должны поддерживать TLS, но могут работать и через TCP.</span><span class="sxs-lookup"><span data-stu-id="e18cd-111">All qualified gateways must support TLS, but can enable TCP as well.</span></span> <span data-ttu-id="e18cd-112">TCP используется для шлюзов, которые не поддерживают TLS.</span><span class="sxs-lookup"><span data-stu-id="e18cd-112">TCP is supported for gateways that do not support TLS.</span></span>

<span data-ttu-id="e18cd-113">Если в вашей среде имеется существующий общедоступный обмен филиалами (УАТС), сервер-посредник обрабатывает вызовы между пользователями корпоративной голосовой связи и УАТС.</span><span class="sxs-lookup"><span data-stu-id="e18cd-113">If you also have an existing Public Branch Exchange (PBX) in your environment, Mediation Server handles calls between Enterprise Voice users and the PBX.</span></span> <span data-ttu-id="e18cd-114">Если УАТС является IP-УАТС, вы можете создать прямое соединение SIP между сервером УАТС и компьютером-посредником.</span><span class="sxs-lookup"><span data-stu-id="e18cd-114">If your PBX is an IP-PBX, you can create a direct SIP connection between the PBX and Mediation Server.</span></span> <span data-ttu-id="e18cd-115">Если ваша АТС является УАТС (TDM), необходимо также развернуть шлюз PSTN между сервером-посредником и УАТС.</span><span class="sxs-lookup"><span data-stu-id="e18cd-115">If your PBX is a Time Division Multiplex (TDM) PBX, you must also deploy a PSTN gateway between Mediation Server and the PBX.</span></span>

<span data-ttu-id="e18cd-116">Сервер обновлений по умолчанию выровнен с сервером переднего плана.</span><span class="sxs-lookup"><span data-stu-id="e18cd-116">The Mediation Server is collocated with the Front End Server by default.</span></span> <span data-ttu-id="e18cd-117">Сервер-посредник также может развертываться в отдельном пуле для повышения производительности или при развертывании магистральной магистрали SIP, в этом случае настоятельно рекомендуется использовать изолированный пул.</span><span class="sxs-lookup"><span data-stu-id="e18cd-117">The Mediation Server can also be deployed in a stand-alone pool for performance reasons, or if you deploy SIP trunking, in which case the stand-alone pool is strongly recommended.</span></span>

<span data-ttu-id="e18cd-118">Если вы разворачиваете прямые подключения по протоколу SIP к квалифицированному шлюзу PSTN, поддерживающему обход ресурсов мультимедиа и балансировку нагрузки DNS, то не нужно использовать изолированный пул серверов для исправления.</span><span class="sxs-lookup"><span data-stu-id="e18cd-118">If you deploy Direct SIP connections to a qualified PSTN gateway that supports media bypass and DNS load balancing, a stand-alone Mediation Server pool is not necessary.</span></span> <span data-ttu-id="e18cd-119">Пул серверов автономных исправлений не нужен, так как квалифицированные шлюзы могут выполнять балансировку нагрузки DNS для пула серверов-посредников, и они могут принимать трафик от любого сервера обновлений в пуле.</span><span class="sxs-lookup"><span data-stu-id="e18cd-119">A stand-alone Mediation Server pool is not necessary because qualified gateways are capable of DNS load balancing to a pool of Mediation Servers and they can receive traffic from any Mediation Server in a pool.</span></span>

<span data-ttu-id="e18cd-120">Кроме того, рекомендуется разгруппировать сервер-посредник в пуле переднего плана, если вы развернули IP-PBXs или подключаться к контроллеру границ сеанса поставщика услуг Интернет-телефонии (SBC), если выполняются следующие условия:</span><span class="sxs-lookup"><span data-stu-id="e18cd-120">We also recommend that you collocate the Mediation Server on a Front End pool when you have deployed IP-PBXs or connect to an Internet Telephony Server Provider’s Session Border Controller (SBC), as long as any of the following conditions are met:</span></span>

  - <span data-ttu-id="e18cd-121">IP-УАТС или SBC настроен для приема трафика от любого сервера-посредника в пуле и может маршрутизировать трафик одинаково для всех серверов-посредников в пуле.</span><span class="sxs-lookup"><span data-stu-id="e18cd-121">The IP-PBX or SBC is configured to receive traffic from any Mediation Server in the pool and can route traffic uniformly to all Mediation Servers in the pool.</span></span>

  - <span data-ttu-id="e18cd-122">IP-УАТС не поддерживает обход мультимедиа, но интерфейсный пул, на котором размещен сервер-посредник, может обрабатывать передачу голосовой почты для звонков, к которым не применяется обход мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="e18cd-122">The IP-PBX does not support media bypass, but the Front End pool that is hosting the Mediation Server can handle voice transcoding for calls to which media bypass does not apply.</span></span>

<span data-ttu-id="e18cd-123">Вы можете воспользоваться средством Microsoft Lync Server 2013, планированием, чтобы определить, может ли пул переднего плана, где должен быть размещен сервер обновлений, обрабатывать загрузку.</span><span class="sxs-lookup"><span data-stu-id="e18cd-123">You can use the Microsoft Lync Server 2013, Planning Tool to evaluate whether the Front End pool where you want to collocate the Mediation Server can handle the load.</span></span> <span data-ttu-id="e18cd-124">Если среда не отвечает этим требованиям, необходимо развернуть пул серверов изолированных исправлений.</span><span class="sxs-lookup"><span data-stu-id="e18cd-124">If your environment cannot meet these requirements, then you must deploy a stand-alone Mediation Server pool.</span></span>

<span data-ttu-id="e18cd-125">Ниже приведены основные функции сервера обновлений.</span><span class="sxs-lookup"><span data-stu-id="e18cd-125">The main functions of the Mediation Server are as follows:</span></span>

  - <span data-ttu-id="e18cd-126">Шифрование и расшифровка SRTP на стороне Lync Server</span><span class="sxs-lookup"><span data-stu-id="e18cd-126">Encrypting and decrypting SRTP on the Lync Server side</span></span>

  - <span data-ttu-id="e18cd-127">Перевод SIP по протоколу TCP (для шлюзов, не поддерживающих TLS) в SIP по обоюдному протоколу TLS</span><span class="sxs-lookup"><span data-stu-id="e18cd-127">Translating SIP over TCP (for gateways that do not support TLS) to SIP over mutual TLS</span></span>

  - <span data-ttu-id="e18cd-128">Преобразование потоков мультимедиа между Lync Server и одноранговым элементом шлюза на сервере обновлений</span><span class="sxs-lookup"><span data-stu-id="e18cd-128">Translating media streams between Lync Server and the gateway peer of the Mediation Server</span></span>

  - <span data-ttu-id="e18cd-129">Подключение клиентов, находящихся за пределами сети, к внутренним компонентам ICE, которые позволяют прослеживать мультимедийные компоненты NAT и брандмауэры.</span><span class="sxs-lookup"><span data-stu-id="e18cd-129">Connecting clients that are outside the network to internal ICE components, which enable media traversal of NAT and firewalls</span></span>

  - <span data-ttu-id="e18cd-130">Выступающий в качестве посредника для потоков звонков, которые не поддерживаются шлюзом (например, звонки от удаленных сотрудников в корпоративном клиенте голосовой связи).</span><span class="sxs-lookup"><span data-stu-id="e18cd-130">Acting as an intermediary for call flows that a gateway does not support, such as calls from remote workers on an Enterprise Voice client</span></span>

  - <span data-ttu-id="e18cd-131">В развертываниях, включающих в себя магистраль SIP, работа с поставщиком услуг по магистрали SIP для обеспечения поддержки PSTN, что устраняет необходимость в шлюзе PSTN.</span><span class="sxs-lookup"><span data-stu-id="e18cd-131">In deployments that include SIP trunking, working with the SIP trunking service provider to provide PSTN support, which eliminates the need for a PSTN gateway</span></span>

<span data-ttu-id="e18cd-132">На рисунке ниже показана передача сигналов и протоколов мультимедиа, которые используются сервером-посредником при общении с основным шлюзом PSTN и корпоративной инфраструктурой голосовой связи.</span><span class="sxs-lookup"><span data-stu-id="e18cd-132">The following figure shows the signaling and media protocols that are used by the Mediation Server when communicating with a basic PSTN gateway and the Enterprise Voice infrastructure.</span></span>

<span data-ttu-id="e18cd-133">**Протоколы передачи сигналов и мультимедиа, используемые сервером-посредником**</span><span class="sxs-lookup"><span data-stu-id="e18cd-133">**Signaling and media protocols used by the Mediation Server**</span></span>

<span data-ttu-id="e18cd-134">![Протоколы сервера-посредника (схема)](images/Gg398399.c3d39ba0-e323-4a58-8f07-4e80d3278af2(OCS.15).jpg "Протоколы сервера-посредника (схема)")</span><span class="sxs-lookup"><span data-stu-id="e18cd-134">![Mediation Server Protocols diagram](images/Gg398399.c3d39ba0-e323-4a58-8f07-4e80d3278af2(OCS.15).jpg "Mediation Server Protocols diagram")</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="e18cd-135">Если вы используете протокол TCP или RTP/RTCP (вместо SRTP или SRTCP) в сети между шлюзом PSTN и сервером-посредником, мы рекомендуем использовать меры для обеспечения безопасности и конфиденциальности сети.</span><span class="sxs-lookup"><span data-stu-id="e18cd-135">If you are using TCP or RTP/RTCP (instead of SRTP or SRTCP) on the network between the PSTN gateway and the Mediation Server, we recommend that you take measures to help ensure the security and privacy of the network.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="e18cd-136">Содержание</span><span class="sxs-lookup"><span data-stu-id="e18cd-136">In This Section</span></span>

  - [<span data-ttu-id="e18cd-137">M:N магистраль в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e18cd-137">M:N trunk in Lync Server 2013</span></span>](lync-server-2013-m-n-trunk.md)

  - [<span data-ttu-id="e18cd-138">Контроль допуска звонков и сервер-посредник в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e18cd-138">Call admission control and Mediation Server in Lync Server 2013</span></span>](lync-server-2013-call-admission-control-and-mediation-server.md)

  - [<span data-ttu-id="e18cd-139">Enhanced 9-1-1 (E9-1-1) и сервер-посредник в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e18cd-139">Enhanced 9-1-1 (E9-1-1) and Mediation Server in Lync Server 2013</span></span>](lync-server-2013-enhanced-9-1-1-e9-1-1-and-mediation-server.md)

  - [<span data-ttu-id="e18cd-140">Сервер-посредник и обход сервера посредника в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e18cd-140">Media bypass and Mediation Server in Lync Server 2013</span></span>](lync-server-2013-media-bypass-and-mediation-server.md)

  - [<span data-ttu-id="e18cd-141">Компоненты и топологии для сервера-посредника в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e18cd-141">Components and topologies for Mediation Server in Lync Server 2013</span></span>](lync-server-2013-components-and-topologies-for-mediation-server.md)

  - [<span data-ttu-id="e18cd-142">Рекомендации по развертыванию сервера обновлений в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e18cd-142">Deployment guidelines for Mediation Server in Lync Server 2013</span></span>](lync-server-2013-deployment-guidelines-for-mediation-server.md)

<span data-ttu-id="e18cd-143"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e18cd-143"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

