---
title: 'Lync Server 2013: планирование доступа внешних пользователей'
description: 'Lync Server 2013: Планирование доступа внешних пользователей.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for external user access
ms:assetid: ea098933-eff5-461e-aba3-e7f128784dc2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399048(v=OCS.15)
ms:contentKeyID: 48185903
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b8f1854791ed837b963d4c80f3467e4e89555592
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49397891"
---
# <a name="planning-for-external-user-access-in-lync-server-2013"></a><span data-ttu-id="5481b-103">Планирование доступа внешних пользователей в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5481b-103">Planning for external user access in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5481b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5481b-104">

<span> </span></span></span>

<span data-ttu-id="5481b-105">_**Тема последнего изменения:** 2013-01-19_</span><span class="sxs-lookup"><span data-stu-id="5481b-105">_**Topic Last Modified:** 2013-01-19_</span></span>

<span data-ttu-id="5481b-106">Взаимодействие в большинстве организаций включает в себя службы и пользователей, которые не находятся в внутренней сети.</span><span class="sxs-lookup"><span data-stu-id="5481b-106">Communications in most organizations involve services and users that are not inside your internal network.</span></span> <span data-ttu-id="5481b-107">Эти службы и пользователи включают в себя сотрудников, которые временно или постоянно находятся за пределами Организации, сотрудников, использующих общедоступные службы обмена мгновенными сообщениями, и потенциальных клиентов, партнеров и анонимных пользователей, которые вы пригласили на собрания и презентации.</span><span class="sxs-lookup"><span data-stu-id="5481b-107">These services and users include employees who are temporarily or permanently offsite, employees of customer or partner organizations, people who use public instant messaging (IM) services, and potential customers, partners and anonymous users whom you invite to meetings and presentations.</span></span> <span data-ttu-id="5481b-108">В этой документации эти люди обозначаются как *внешние пользователи*.</span><span class="sxs-lookup"><span data-stu-id="5481b-108">In this documentation, these people are collectively referred to as *external users*.</span></span>

<span data-ttu-id="5481b-109">В Microsoft Lync Server 2013 пользователи в вашей организации могут использовать сообщения и сведения о присутствии для общения с внешними пользователями, а также могут принимать участие в конференциях и веб-конференциях с сотрудниками других организаций и других типов внешних пользователей.</span><span class="sxs-lookup"><span data-stu-id="5481b-109">With Microsoft Lync Server 2013, users in your organization can use IM and presence to communicate with external users, and they can participate in audio/video (A/V) conferencing and web conferencing with your offsite employees and other types of external users.</span></span> <span data-ttu-id="5481b-110">Вы также можете поддерживать внешний доступ с мобильных устройств и с помощью корпоративной голосовой связи.</span><span class="sxs-lookup"><span data-stu-id="5481b-110">You can also support external access from mobile devices and over Enterprise Voice.</span></span> <span data-ttu-id="5481b-111">Внешние пользователи, которые не являются сотрудниками вашей организации, могут принимать участие в собраниях Lync Server 2013, разрешая анонимным участникам.</span><span class="sxs-lookup"><span data-stu-id="5481b-111">External users who are not members of your organization can participate in Lync Server 2013 meetings, allowing anonymous attendees.</span></span>

<span data-ttu-id="5481b-112">Для поддержки обмена сообщениями через брандмауэр организации вы развертываете сервер Lync Server 2013 EDGE в сети периметра (также называемой демилитаризованной зоной, ДМЗ или экранированной подсетью).</span><span class="sxs-lookup"><span data-stu-id="5481b-112">To support communications across your organization’s firewall, you deploy Lync Server 2013 Edge Server in your perimeter network (also known as DMZ, demilitarized zone, and screened subnet).</span></span> <span data-ttu-id="5481b-113">Пограничный сервер управляет тем, как пользователи за пределами межсетевого экрана могут подключаться к внутренней среде Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="5481b-113">The Edge Server controls how users outside the firewall can connect to your internal Lync Server 2013 deployment.</span></span> <span data-ttu-id="5481b-114">Она также управляет связью с внешними пользователями, исходящие из брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="5481b-114">It also controls communications with external users that originate within the firewall.</span></span>

<span data-ttu-id="5481b-115">В зависимости от ваших требований вы можете развернуть один или несколько пограничных серверов в одном или нескольких расположениях.</span><span class="sxs-lookup"><span data-stu-id="5481b-115">Depending on your requirements, you can deploy one or more Edge Servers in one or more locations.</span></span> <span data-ttu-id="5481b-116">В этом разделе описаны сценарии для внешних пользователей Access в Lync Server 2013, а также объясняется, как спланировать пограничный и обратную топологию прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="5481b-116">This section describes scenarios for external user access in Lync Server 2013, and it explains how to plan your edge and reverse proxy topology.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="5481b-117">Несмотря на то что вам нужен пограничный сервер для поддержки корпоративного голосовой связи и доступа внешних пользователей, в этом разделе рассматриваются вопросы поддержки обмена мгновенными сообщениями, присутствия, интеграции, веб-конференций и Lync Mobile.</span><span class="sxs-lookup"><span data-stu-id="5481b-117">Although you need an Edge Server to support Enterprise Voice and external user access, this section focuses on support for IM, presence, A/V conferencing, federation, web conferencing, and Lync Mobile.</span></span> <span data-ttu-id="5481b-118">Подробные сведения о поддержке корпоративной голосовой связи можно найти <A href="lync-server-2013-planning-for-enterprise-voice.md">в разделе Планирование корпоративной голосовой связи в Lync Server 2013</A> в документации по планированию.</span><span class="sxs-lookup"><span data-stu-id="5481b-118">For details about support for Enterprise Voice, see <A href="lync-server-2013-planning-for-enterprise-voice.md">Planning for Enterprise Voice in Lync Server 2013</A> in the Planning documentation.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="5481b-119">Содержание</span><span class="sxs-lookup"><span data-stu-id="5481b-119">In This Section</span></span>

  - [<span data-ttu-id="5481b-120">Изменения Lync Server 2013, затрагивающие планирование пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="5481b-120">Changes in Lync Server 2013 that affect Edge Server planning</span></span>](lync-server-2013-changes-in-lync-server-that-affect-edge-server-planning.md)

  - [<span data-ttu-id="5481b-121">Системные требования для компонентов доступа внешних пользователей для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5481b-121">System requirements for external user access components for Lync Server 2013</span></span>](lync-server-2013-system-requirements-for-external-user-access-components.md)

  - [<span data-ttu-id="5481b-122">Обзор доступа внешних пользователей в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5481b-122">Overview of external user access in Lync Server 2013</span></span>](lync-server-2013-overview-of-external-user-access.md)

  - [<span data-ttu-id="5481b-123">Общие сведения о автообнаружения в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5481b-123">Understanding Autodiscover in Lync Server 2013</span></span>](lync-server-2013-understanding-autodiscover.md)

  - [<span data-ttu-id="5481b-124">Выбор топологии в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5481b-124">Choosing a topology in Lync Server 2013</span></span>](lync-server-2013-choosing-a-topology.md)

  - [<span data-ttu-id="5481b-125">Сбор данных в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5481b-125">Data collection in Lync Server 2013</span></span>](lync-server-2013-data-collection.md)

  - [<span data-ttu-id="5481b-126">Определение требований DNS для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5481b-126">Determine DNS requirements for Lync Server 2013</span></span>](lync-server-2013-determine-dns-requirements.md)

  - [<span data-ttu-id="5481b-127">Определение требований к внешнему брандмауэру аудио- и видеосвязи и портам для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5481b-127">Determine external A/V firewall and port requirements for Lync Server 2013</span></span>](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md)

  - [<span data-ttu-id="5481b-128">Планирование сертификатов пограничного сервера в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5481b-128">Plan for Edge Server certificates in Lync Server 2013</span></span>](lync-server-2013-plan-for-edge-server-certificates.md)

  - [<span data-ttu-id="5481b-129">Сценарии доступа внешних пользователей в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5481b-129">Scenarios for external user access in Lync Server 2013</span></span>](lync-server-2013-scenarios-for-external-user-access.md)

<span data-ttu-id="5481b-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5481b-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

