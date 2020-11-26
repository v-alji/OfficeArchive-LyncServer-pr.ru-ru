---
title: 'Lync Server 2013: развертывание серверов-посредников и определение одноранговых узлов'
description: 'Lync Server 2013: развертывание серверов обновлений и определение одноранговых узлов.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying Mediation Servers and defining peers
ms:assetid: a684f1da-6671-4011-adf6-2db49e2528e2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412780(v=OCS.15)
ms:contentKeyID: 48185077
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fc3afce038371920beea1cc52549d8d027429e08
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429897"
---
# <a name="deploying-mediation-servers-and-defining-peers-in-lync-server-2013"></a><span data-ttu-id="2fa16-103">Развертывание серверов-посредников и определение одноранговых узлов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2fa16-103">Deploying Mediation Servers and defining peers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2fa16-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2fa16-104">

<span> </span></span></span>

<span data-ttu-id="2fa16-105">_**Тема последнего изменения:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="2fa16-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="2fa16-106">Корпоративная рабочая нагрузка, Конференц-связь с телефонным подключением и сложные приложения для корпоративной голосовой связи (приложение группы ответа, приложение для допуска звонков (CAC) и т. д.) можно использовать в пулах интерфейсного сервера.</span><span class="sxs-lookup"><span data-stu-id="2fa16-106">The Enterprise Voice workload, dial-in conferencing, and advanced Enterprise Voice applications (Response Group application, Call Park application, call admission control (CAC), and so on), are available in Front End pools.</span></span> <span data-ttu-id="2fa16-107">При использовании Lync Server 2013 функциональность сервера обновлений встроена в сервер переднего плана.</span><span class="sxs-lookup"><span data-stu-id="2fa16-107">With Lync Server 2013, the functionality of the Mediation Server is built into the Front End Server.</span></span> <span data-ttu-id="2fa16-108">На отдельном изолированном сервере обновлений больше нет необходимости.</span><span class="sxs-lookup"><span data-stu-id="2fa16-108">A separate stand-alone Mediation Server is no longer necessary.</span></span> <span data-ttu-id="2fa16-109">Пулы переднего плана могут взаимодействовать непосредственно с поддерживаемыми шлюзами (коммутируемые коммутируемые телефонные сети (PSTN) или IP-УАТС), устраняя необходимость в использовании сервера-посредника для использования в качестве посредника.</span><span class="sxs-lookup"><span data-stu-id="2fa16-109">Front End pools can communicate directly with supported gateways (a public switched telephone network (PSTN) gateway or an IP-PBX), removing the need for a Mediation Server to serve as an intermediary.</span></span>

<span data-ttu-id="2fa16-110">Единственным исключением является настройка магистральной магистрали SIP для подключения к контроллеру границ сеанса для поставщика услуг телефонной связи через Интернет.</span><span class="sxs-lookup"><span data-stu-id="2fa16-110">The only exception is if you configure a SIP trunk to connect to a Session Border Controller for an Internet Telephony Service Provider.</span></span> <span data-ttu-id="2fa16-111">Чтобы подключить корпоративную инфраструктуру голосовой связи к провайдеру магистральной магистрали SIP, необходимо развернуть отдельный сервер-посредник.</span><span class="sxs-lookup"><span data-stu-id="2fa16-111">To connect your Enterprise Voice infrastructure to your SIP trunk provider, a separate Mediation Server must be deployed.</span></span>

<span data-ttu-id="2fa16-112">Соединение между Lync Server (компонент сервера-посредника в пуле переднего плана или отдельного сервера-посредника) и шлюз определено как логическая связь, называемая *магистральной*.</span><span class="sxs-lookup"><span data-stu-id="2fa16-112">The connection between Lync Server (the Mediation Server component on a Front End pool or stand-alone Mediation Server) and a gateway is defined as a logical association called a *trunk*.</span></span> <span data-ttu-id="2fa16-113">В этом разделе объясняется, как определить магистраль и как развернуть отдельный сервер-посредник, если вы подключаетесь к магистрали SIP.</span><span class="sxs-lookup"><span data-stu-id="2fa16-113">The topics in this section describe how to define a trunk and how to deploy a stand-alone Mediation Server, if you connect to a SIP trunk.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="2fa16-114">Содержание</span><span class="sxs-lookup"><span data-stu-id="2fa16-114">In This Section</span></span>

  - [<span data-ttu-id="2fa16-115">Определение сервера-посредника в построителе топологии в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2fa16-115">Define a Mediation Server in Topology Builder in Lync Server 2013</span></span>](lync-server-2013-define-a-mediation-server-in-topology-builder.md)

  - [<span data-ttu-id="2fa16-116">Определение шлюза в построителе топологии в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2fa16-116">Define a gateway in Topology Builder in Lync Server 2013</span></span>](lync-server-2013-define-a-gateway-in-topology-builder.md)

  - [<span data-ttu-id="2fa16-117">Установка сервера исправлений в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2fa16-117">Install the files for Mediation Server in Lync Server 2013</span></span>](lync-server-2013-install-the-files-for-mediation-server.md)

  - [<span data-ttu-id="2fa16-118">Определение дополнительных каналов в построителе топологии в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2fa16-118">Define additional trunks in Topology Builder in Lync Server 2013</span></span>](lync-server-2013-define-additional-trunks-in-topology-builder.md)

</div>

<div>

## <a name="related-sections"></a><span data-ttu-id="2fa16-119">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="2fa16-119">Related Sections</span></span>

[<span data-ttu-id="2fa16-120">Настройка конференц-связи с телефонным подключением в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2fa16-120">Configuring dial-in conferencing in Lync Server 2013</span></span>](lync-server-2013-configuring-dial-in-conferencing.md)

<span data-ttu-id="2fa16-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2fa16-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

