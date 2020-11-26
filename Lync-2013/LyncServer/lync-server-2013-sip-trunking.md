---
title: 'Lync Server 2013: магистральные линии SIP'
description: 'Lync Server 2013: магистраль SIP.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: SIP trunking
ms:assetid: 7c586401-d0e5-4017-b3e1-fe5e7f8fc6db
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398619(v=OCS.15)
ms:contentKeyID: 48184615
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 60b68d9d0400c87de2832d7fe7bdabe4057ec47a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423808"
---
# <a name="sip-trunking-in-lync-server-2013"></a><span data-ttu-id="d0f7a-103">Магистральные линии SIP в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d0f7a-103">SIP trunking in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d0f7a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d0f7a-104">

<span> </span></span></span>

<span data-ttu-id="d0f7a-105">_**Тема последнего изменения:** 2012-08-13_</span><span class="sxs-lookup"><span data-stu-id="d0f7a-105">_**Topic Last Modified:** 2012-08-13_</span></span>

<span data-ttu-id="d0f7a-p101">С помощью протокола инициирования сеансов (SIP) сеансы связи инициируются и управляются по протоколу VoIP для основной телефонной службы и для таких дополнительных коммуникационных услуг в режиме реального времени, как обмен мгновенными сообщениями, конференц-связь, обнаружение присутствия и мультимедиа. В этом разделе представлены сведения по планированию для реализации *магистралей SIP*, типы подключений SIP, которые распространяется за пределы локальной сети.</span><span class="sxs-lookup"><span data-stu-id="d0f7a-p101">Session Initiation Protocol (SIP) is used to initiate and manage Voice over IP (VoIP) communications sessions for basic telephone service and for additional real-time communication services, such as instant messaging, conferencing, presence detection, and multimedia. This section provides planning information for implementing *SIP trunks*, a type of SIP connection that extends beyond the boundary of your local network.</span></span>

<div>

## <a name="what-is-sip-trunking"></a><span data-ttu-id="d0f7a-108">Что такое транкинг SIP?</span><span class="sxs-lookup"><span data-stu-id="d0f7a-108">What is SIP Trunking?</span></span>

<span data-ttu-id="d0f7a-p102">Транкинг SIP — это IP-подключение, которое устанавливает коммуникационную связь SIP между вашей организацией и поставщиком услуг интернет-телефонии (ITSP) за пределами брандмауэра организации. Обычно магистраль SIP используется для подключения центрального сайта организации к ITSP. В некоторых случаях вы также можете выбрать транкинг SIP для подключения сайта филиала к ITSP.</span><span class="sxs-lookup"><span data-stu-id="d0f7a-p102">A SIP trunk is an IP connection that establishes a SIP communications link between your organization and an Internet telephony service provider (ITSP) beyond your firewall. Typically, a SIP trunk is used to connect your organization’s central site to an ITSP. In some cases, you may also opt to use SIP trunking to connect your branch site to an ITSP.</span></span>

<div>

## <a name="sip-trunks-vs-direct-sip-connections"></a><span data-ttu-id="d0f7a-112">Сравнение магистралей SIP с прямыми SIP-подключениями</span><span class="sxs-lookup"><span data-stu-id="d0f7a-112">SIP Trunks vs. Direct SIP Connections</span></span>

<span data-ttu-id="d0f7a-113">Термин *магистраль* происходит технологии коммутируемых каналов.</span><span class="sxs-lookup"><span data-stu-id="d0f7a-113">The term *trunk* is derived from circuit-switched technology.</span></span> <span data-ttu-id="d0f7a-114">Он относится к выделенной физической линии, соединяющей телефонное коммутационное оборудование.</span><span class="sxs-lookup"><span data-stu-id="d0f7a-114">It refers to a dedicated physical line that connects telephone switching equipment.</span></span> <span data-ttu-id="d0f7a-115">Как и в случае с их предшественниками, мультиплексированием деления времени (TDM), магистральные магистрали SIP — это соединения между двумя отдельными сетями SIP — Lync Server 2013 Enterprise и ITSP.</span><span class="sxs-lookup"><span data-stu-id="d0f7a-115">Like their predecessor, time division multiplexing (TDM) trunks, SIP trunks are connections between two separate SIP networks—the Lync Server 2013 enterprise and the ITSP.</span></span> <span data-ttu-id="d0f7a-116">В отличие от коммутируемых каналов, магистрали SIP являются виртуальными подключениями, которые могут быть установлены в любых поддерживаемых типах подключений транкинга SIP.</span><span class="sxs-lookup"><span data-stu-id="d0f7a-116">Unlike circuit-switched trunks, SIP trunks are virtual connections that can be established over any of the supported SIP trunking connection types.</span></span> <span data-ttu-id="d0f7a-117">Подробнее о поддерживаемых типах подключений вы узнаете, [как реализовать магистральные линии SIP в Lync Server 2013?](lync-server-2013-how-do-i-implement-sip-trunking.md).</span><span class="sxs-lookup"><span data-stu-id="d0f7a-117">For details about the supported connection types, see [How do I implement SIP trunking in Lync Server 2013?](lync-server-2013-how-do-i-implement-sip-trunking.md).</span></span>

<span data-ttu-id="d0f7a-118">С другой стороны, прямые SIP-подключения — это подключения, которые не пересекают границ локальной сети (т.е. они подключаются к шлюзу ТСОП или УАТС во внутренней сети).</span><span class="sxs-lookup"><span data-stu-id="d0f7a-118">Direct SIP connections, on the other hand, are SIP connections that do not cross the local network boundary (that is, they connect to a public switched telephone network (PSTN) gateway or private branch exchange (PBX) within your internal network).</span></span> <span data-ttu-id="d0f7a-119">Подробнее о том, как использовать прямые подключения по протоколу SIP с Lync Server 2013, можно найти [в разделе прямые подключения SIP в Lync server 2013](lync-server-2013-direct-sip-connections.md).</span><span class="sxs-lookup"><span data-stu-id="d0f7a-119">For details about how you can use direct SIP connections with Lync Server 2013, see [Direct SIP connections in Lync Server 2013](lync-server-2013-direct-sip-connections.md).</span></span>

</div>

</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="d0f7a-120">Содержание</span><span class="sxs-lookup"><span data-stu-id="d0f7a-120">In This Section</span></span>

  - [<span data-ttu-id="d0f7a-121">Обзор распределения каналов SIP в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d0f7a-121">Overview of SIP trunking in Lync Server 2013</span></span>](lync-server-2013-overview-of-sip-trunking.md)

  - [<span data-ttu-id="d0f7a-122">Реализация распределения каналов SIP в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d0f7a-122">How do I implement SIP trunking in Lync Server 2013?</span></span>](lync-server-2013-how-do-i-implement-sip-trunking.md)

  - [<span data-ttu-id="d0f7a-123">Компоненты и топологии для распределения каналов SIP в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d0f7a-123">Components and topologies for SIP trunking in Lync Server 2013</span></span>](lync-server-2013-components-and-topologies-for-sip-trunking.md)

  - [<span data-ttu-id="d0f7a-124">Branch site SIP trunking in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d0f7a-124">Branch site SIP trunking in Lync Server 2013</span></span>](lync-server-2013-branch-site-sip-trunking.md)

  - [<span data-ttu-id="d0f7a-125">Контрольный список развертывания для каналов SIP для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d0f7a-125">SIP trunk deployment checklist for Lync Server 2013</span></span>](lync-server-2013-sip-trunk-deployment-checklist.md)

<span data-ttu-id="d0f7a-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d0f7a-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

