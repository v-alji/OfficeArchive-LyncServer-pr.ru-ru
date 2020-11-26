---
title: 'Lync Server 2013: компоненты и топологии для распределения каналов SIP'
description: 'Lync Server 2013: компоненты и топологии для магистрали SIP.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Components and topologies for SIP trunking
ms:assetid: 8ed9a9d0-517e-4f36-a131-22cdafa257fa
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398720(v=OCS.15)
ms:contentKeyID: 48184775
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f9d9c826539084a539d3efe7f143c335ec6d8f62
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434572"
---
# <a name="components-and-topologies-for-sip-trunking-in-lync-server-2013"></a><span data-ttu-id="2c809-103">Компоненты и топологии для распределения каналов SIP в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2c809-103">Components and topologies for SIP trunking in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2c809-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2c809-104">

<span> </span></span></span>

<span data-ttu-id="2c809-105">_**Тема последнего изменения:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="2c809-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="2c809-106">На приведенном ниже рисунке показана топология магистрали SIP в Lync Server.</span><span class="sxs-lookup"><span data-stu-id="2c809-106">The following figure depicts the SIP trunking topology in Lync Server.</span></span>

<span data-ttu-id="2c809-107">**Топология магистрали SIP**</span><span class="sxs-lookup"><span data-stu-id="2c809-107">**SIP trunking topology**</span></span>

<span data-ttu-id="2c809-108">![Топология распределения каналов SIP](images/Gg398720.669fb55d-7c81-4e21-9421-fabc43d6e064(OCS.15).jpg "Топология распределения каналов SIP")</span><span class="sxs-lookup"><span data-stu-id="2c809-108">![SIP Trunking Topology](images/Gg398720.669fb55d-7c81-4e21-9421-fabc43d6e064(OCS.15).jpg "SIP Trunking Topology")</span></span>

<span data-ttu-id="2c809-p101">Как показано на схеме, для подключений между корпоративной сетью и поставщиком услуг ТСОП используется виртуальная частная сеть VPN. Цель этой частной сети состоит в том, чтобы предоставить IP-подключение, повысить безопасность и (дополнительно) получить гарантированное качество обслуживания. В силу принципов работы VPN нет необходимости использовать протокол TLS для трафика передачи сигналов SIP или протокол SRTP для трафика мультимедиа. Таким образом, подключения между предприятием и поставщиком услуг представляют обычные TCP-соединения для SIP и обычные RTP-соединения (через UDP) для туннелирования мультимедиа через IP VPN. Убедитесь, что все брандмауэры между маршрутизаторами VPN имеют открытые порты, чтобы разрешить маршрутизаторам VPN взаимодействие, и что IP-адреса на внешних границах маршрутизаторов VPN маршрутизируемы общедоступным образом.</span><span class="sxs-lookup"><span data-stu-id="2c809-p101">As shown in the diagram, an IP virtual private network (VPN) is used for connectivity between the enterprise network and the public switched telephone network (PSTN) service provider. The purpose of this private network is to provide IP connectivity, enhance security, and (optionally) obtain Quality of Service (QoS) guarantees. Because of the nature of a VPN, you do not need to use Transport Layer Security (TLS) for SIP signaling traffic or secure real-time transport protocol (SRTP) for the media traffic. Connections between the enterprise and the service provider therefore consist of plain TCP connections for SIP and plain real-time transport protocol (RTP) (over UDP) for media tunneled through an IP VPN. Ensure that all firewalls between the VPN routers have ports open to allow the VPN routers to communicate, and that the IP addresses on the external edges of the VPN routers are publicly routable.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="2c809-114">Обратитесь к своему поставщику услуг, чтобы узнать, обеспечивает ли он поддержку высокой доступности, включая отработку отказа.</span><span class="sxs-lookup"><span data-stu-id="2c809-114">Contact your service provider to determine whether it provides support for high availability, including failover.</span></span> <span data-ttu-id="2c809-115">Если обеспечивает, то необходимо определить процедуры для ее настройки.</span><span class="sxs-lookup"><span data-stu-id="2c809-115">If so, you will need to determine the procedures for setting it up.</span></span> <span data-ttu-id="2c809-116">Например, нужно настроить только один IP-адрес и одну магистральную функцию SIP на каждом сервере-посреднике или настроить несколько магистральных каналов SIP на каждом сервере-посреднике?</span><span class="sxs-lookup"><span data-stu-id="2c809-116">For example, do you need to configure only one IP address and one SIP trunk on each Mediation Server, or do you need to configure multiple SIP trunks on each Mediation Server?</span></span><BR><span data-ttu-id="2c809-117">Если у вас есть несколько центральных сайтов, также Узнайте, есть ли у поставщика услуг возможность включения подключений и из другого центрального сайта.</span><span class="sxs-lookup"><span data-stu-id="2c809-117">If you have multiple central sites, also ask whether the service provider has the ability to enable connections to and from another central site.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="2c809-118">Для магистральной магистрали SIP настоятельно рекомендуется развертывать отдельные серверы-посредники.</span><span class="sxs-lookup"><span data-stu-id="2c809-118">For SIP trunking, we strongly recommend that you deploy stand-alone Mediation Servers.</span></span> <span data-ttu-id="2c809-119">Дополнительные сведения можно найти <A href="lync-server-2013-deploying-mediation-servers-and-defining-peers.md">в разделе Развертывание серверов обновлений и определение одноранговых узлов в Lync Server 2013</A> в документации по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="2c809-119">For details, see <A href="lync-server-2013-deploying-mediation-servers-and-defining-peers.md">Deploying Mediation Servers and defining peers in Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<div>

## <a name="securing-the-mediation-server-for-sip-trunking"></a><span data-ttu-id="2c809-120">Защита сервера-посредника для транкинга SIP</span><span class="sxs-lookup"><span data-stu-id="2c809-120">Securing the Mediation Server for SIP Trunking</span></span>

<span data-ttu-id="2c809-p104">В целях безопасности необходимо настроить виртуальную локальную сеть (VLAN) для каждого соединения между двумя маршрутизаторами VPN. Фактический процесс настройки VLAN зависит от производителя маршрутизатора. Подробные сведения следует запросить у вашего поставщика маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="2c809-p104">For security purposes, you should set up a virtual LAN (VLAN) for each connection between the two VPN routers. The actual process for setting up a VLAN varies from one router manufacturer to another. For details, contact your router vendor.</span></span>

<span data-ttu-id="2c809-124">Рекомендуется придерживаться следующих правил.</span><span class="sxs-lookup"><span data-stu-id="2c809-124">We recommend that you follow these guidelines:</span></span>

  - <span data-ttu-id="2c809-125">Настройте виртуальную локальную сеть (VLAN) между сервером-посредником и маршрутизатором VPN в демилитаризованной зоне (также называемой демилитаризованной зоной, ДМЗ или экранированной подсетью).</span><span class="sxs-lookup"><span data-stu-id="2c809-125">Set up a virtual LAN (VLAN) between the Mediation Server and the VPN router in the perimeter network (also known as DMZ, demilitarized zone, and screened subnet).</span></span>

  - <span data-ttu-id="2c809-126">Не разрешать передачу широковещательных или многоадресных пакетов от маршрутизатора в VLAN.</span><span class="sxs-lookup"><span data-stu-id="2c809-126">Do not allow broadcast or multicast packets to be transferred from the router to the VLAN.</span></span>

  - <span data-ttu-id="2c809-127">Заблокируйте любые правила маршрутизации, которые перенаправляют трафик с маршрутизатора в любое место, но не на сервер обновлений.</span><span class="sxs-lookup"><span data-stu-id="2c809-127">Block any routing rules that route traffic from the router to anywhere but the Mediation Server.</span></span>

<span data-ttu-id="2c809-128">Если используется VPN-сервер, рекомендуется придерживаться следующих правил.</span><span class="sxs-lookup"><span data-stu-id="2c809-128">If you use a VPN server, we recommend that you follow these guidelines:</span></span>

  - <span data-ttu-id="2c809-129">Настройте виртуальную ЛС между VPN-сервером и сервером-посредником.</span><span class="sxs-lookup"><span data-stu-id="2c809-129">Set up a VLAN between the VPN server and the Mediation Server.</span></span>

  - <span data-ttu-id="2c809-130">Не разрешать передачу широковещательных или многоадресных пакетов от VPN-сервера в VLAN.</span><span class="sxs-lookup"><span data-stu-id="2c809-130">Do not allow broadcast or multicast packets to be transmitted from the VPN server to the VLAN.</span></span>

  - <span data-ttu-id="2c809-131">Заблокируйте любые правила маршрутизации, которые направляют трафик VPN-сервера в любое место, но не на сервер-посредника.</span><span class="sxs-lookup"><span data-stu-id="2c809-131">Block any routing rule that routes VPN server traffic to anywhere but the Mediation Server.</span></span>

  - <span data-ttu-id="2c809-132">Шифровать данные в VPN с помощью протокола GRE (Generic Routing Encapsulation).</span><span class="sxs-lookup"><span data-stu-id="2c809-132">Encrypt data on the VPN by using generic routing encapsulation (GRE).</span></span>

<span data-ttu-id="2c809-133"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2c809-133"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

