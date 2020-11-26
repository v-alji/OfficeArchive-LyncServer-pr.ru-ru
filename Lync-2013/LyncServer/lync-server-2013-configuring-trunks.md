---
title: 'Lync Server 2013: конфигурация магистралей'
description: 'Lync Server 2013: Настройка каналов.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring trunks
ms:assetid: 0c339511-a185-484e-94f0-dbe918b7e48a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398170(v=OCS.15)
ms:contentKeyID: 48183389
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 07d9503cd38419a7145796a6edf8484a14cdeb53
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432466"
---
# <a name="configuring-trunks-in-lync-server-2013"></a><span data-ttu-id="d7383-103">Конфигурация магистралей в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d7383-103">Configuring trunks in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d7383-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d7383-104">

<span> </span></span></span>

<span data-ttu-id="d7383-105">_**Тема последнего изменения:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="d7383-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="d7383-106">В рамках развертывания Enterprise Voice вы можете настроить магистраль между сервером-посредником и одним или несколькими из указанных ниже одноранговых сетей для предоставления подключения по коммутируемой телефонной сети (PSTN) для корпоративных клиентов и мобильных устройств в Организации.</span><span class="sxs-lookup"><span data-stu-id="d7383-106">As part of Enterprise Voice deployment, you can configure a trunk between a Mediation Server and one or more of the following peers to provide public switched telephone network (PSTN) connectivity for Enterprise Voice clients and devices in your organization:</span></span>

  - <span data-ttu-id="d7383-107">Подключение магистрали SIP к поставщику услуг Интернет-телефонии</span><span class="sxs-lookup"><span data-stu-id="d7383-107">SIP trunk connection to an Internet telephony service provider (ITSP)</span></span>

  - <span data-ttu-id="d7383-108">Шлюз ТСОП</span><span class="sxs-lookup"><span data-stu-id="d7383-108">PSTN gateway</span></span>

  - <span data-ttu-id="d7383-109">УАТС</span><span class="sxs-lookup"><span data-stu-id="d7383-109">Private branch exchange (PBX)</span></span>

<span data-ttu-id="d7383-110">Подробнее смотрите в разделе [Планирование подключений PSTN в Lync Server 2013](lync-server-2013-planning-for-pstn-connectivity.md) в документации по планированию.</span><span class="sxs-lookup"><span data-stu-id="d7383-110">For details, see [Planning for PSTN connectivity in Lync Server 2013](lync-server-2013-planning-for-pstn-connectivity.md) in the Planning documentation.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="d7383-111">Перед началом настройки магистрали убедитесь в том, что топология создана и что сервер исправлений и его одноранговые элементы настроены и связаны друг с другом.</span><span class="sxs-lookup"><span data-stu-id="d7383-111">Before you begin trunk configuration, verify that the topology has been created and that the Mediation Server and its peer have been configured and associated with one another.</span></span> <span data-ttu-id="d7383-112">Подробности можно найти <A href="lync-server-2013-define-a-gateway-in-topology-builder.md">в разделе определение шлюза в построителе топологии в Lync Server 2013</A> в документации по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="d7383-112">For details, see <A href="lync-server-2013-define-a-gateway-in-topology-builder.md">Define a gateway in Topology Builder in Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="d7383-113">В рамках настройки магистрали вы можете включить функцию обхода мультимедиа Lync Server 2013, которая позволяет мультимедиа обходить сервер-посредник.</span><span class="sxs-lookup"><span data-stu-id="d7383-113">As a part of trunk configuration, you can enable the Lync Server 2013 media bypass feature, which enables media to bypass the Mediation Server.</span></span> <span data-ttu-id="d7383-114">Магистральные магистрали можно настраивать с включенным параметром "обойти" или без него, но настоятельно рекомендуем включить его.</span><span class="sxs-lookup"><span data-stu-id="d7383-114">Trunks can be configured either with or without media bypass enabled, but we strongly recommend that you enable it.</span></span> <span data-ttu-id="d7383-115">Подробности можно найти <A href="lync-server-2013-planning-for-media-bypass.md">в разделе Планирование обхода мультимедиа в Lync Server 2013</A> в документации по планированию.</span><span class="sxs-lookup"><span data-stu-id="d7383-115">For details, see <A href="lync-server-2013-planning-for-media-bypass.md">Planning for media bypass in Lync Server 2013</A> in the Planning documentation.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="d7383-116">Содержание</span><span class="sxs-lookup"><span data-stu-id="d7383-116">In This Section</span></span>

  - [<span data-ttu-id="d7383-117">Поддержка нескольких каналов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d7383-117">Multiple trunk support in Lync Server 2013</span></span>](lync-server-2013-multiple-trunk-support.md)

  - [<span data-ttu-id="d7383-118">Маршрутизация с межмагистральными организациями в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d7383-118">Inter-trunk routing in Lync Server 2013</span></span>](lync-server-2013-inter-trunk-routing.md)

  - [<span data-ttu-id="d7383-119">Просмотр сведений о магистральной конфигурации в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d7383-119">View trunk configuration information in Lync Server 2013</span></span>](lync-server-2013-view-trunk-configuration-information.md)

  - [<span data-ttu-id="d7383-120">Configure a trunk with media bypass in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d7383-120">Configure a trunk with media bypass in Lync Server 2013</span></span>](lync-server-2013-configure-a-trunk-with-media-bypass.md)

  - [<span data-ttu-id="d7383-121">Настройка магистрали без обхода мультимедиа в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d7383-121">Configure a trunk without media bypass in Lync Server 2013</span></span>](lync-server-2013-configure-a-trunk-without-media-bypass.md)

  - [<span data-ttu-id="d7383-122">Создание нового набора параметров конфигурации магистрали в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d7383-122">Create a new collection of trunk configuration settings in Lync Server 2013</span></span>](lync-server-2013-create-a-new-collection-of-trunk-configuration-settings.md)

  - [<span data-ttu-id="d7383-123">Удаление существующей коллекции параметров конфигурации магистральной магистрали SIP в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d7383-123">Delete an existing collection of SIP trunk configuration settings in Lync Server 2013</span></span>](lync-server-2013-delete-an-existing-collection-of-sip-trunk-configuration-settings.md)

  - [<span data-ttu-id="d7383-124">Изменение параметров конфигурации магистральной магистрали SIP в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d7383-124">Modify SIP trunk configuration settings in Lync Server 2013</span></span>](lync-server-2013-modify-sip-trunk-configuration-settings.md)

  - [<span data-ttu-id="d7383-125">Проверка параметров конфигурации магистральной магистрали SIP в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d7383-125">Test SIP trunk configuration settings in Lync Server 2013</span></span>](lync-server-2013-test-sip-trunk-configuration-settings.md)

  - [<span data-ttu-id="d7383-126">Просмотр сведений об отдельных магистральах SIP в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d7383-126">View information about individual SIP trunks in Lync Server 2013</span></span>](lync-server-2013-view-information-about-individual-sip-trunks.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="d7383-127">См. также</span><span class="sxs-lookup"><span data-stu-id="d7383-127">See Also</span></span>


[<span data-ttu-id="d7383-128">Определение шлюза в построителе топологии в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d7383-128">Define a gateway in Topology Builder in Lync Server 2013</span></span>](lync-server-2013-define-a-gateway-in-topology-builder.md)  


[<span data-ttu-id="d7383-129">Планирование подключений PSTN в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d7383-129">Planning for PSTN connectivity in Lync Server 2013</span></span>](lync-server-2013-planning-for-pstn-connectivity.md)  
[<span data-ttu-id="d7383-130">Планирование обхода серверов-посредников в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d7383-130">Planning for media bypass in Lync Server 2013</span></span>](lync-server-2013-planning-for-media-bypass.md)  
  

<span data-ttu-id="d7383-131"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d7383-131"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

