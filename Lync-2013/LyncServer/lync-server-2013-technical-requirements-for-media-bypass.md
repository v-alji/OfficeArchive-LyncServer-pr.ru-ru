---
title: 'Lync Server 2013: технические требования для сервера-посредника'
description: 'Lync Server 2013: технические требования для обхода мультимедиа.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Technical requirements for media bypass
ms:assetid: 6162a204-0e7c-460a-8eb2-e592c6590a8a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398435(v=OCS.15)
ms:contentKeyID: 48184321
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dee594139031966342fcec2bc1296a603055b4cc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423437"
---
# <a name="technical-requirements-for-media-bypass-in-lync-server-2013"></a><span data-ttu-id="851fa-103">Технические требования для сервера-посредника в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="851fa-103">Technical requirements for media bypass in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="851fa-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="851fa-104">

<span> </span></span></span>

<span data-ttu-id="851fa-105">_**Тема последнего изменения:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="851fa-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="851fa-106">Для каждого звонка в КТСОП сервер-посредник определяет, можно ли отправлять носители из конечной точки Lync непосредственно на сервер-посредника, не передавая его на сервер.</span><span class="sxs-lookup"><span data-stu-id="851fa-106">For each call to the PSTN, the Mediation Server determines whether media from the Lync endpoint of origin can be sent directly to a Mediation Server peer without traversing the Mediation Server.</span></span> <span data-ttu-id="851fa-107">Узлом партнера может являться шлюз ТСОП, УАТС или пограничный контроллер поставщика услуг интернет-телефонии (ITSP), связанного с магистральной линией между сервером-посредником, где маршрутизируется вызов.</span><span class="sxs-lookup"><span data-stu-id="851fa-107">The peer can be a PSTN gateway, IP-PBX, or Session Border Controller (SBC) at an Internet telephony service provider (ITSP) that is associated with the trunk between the Mediation Server where the call is routed.</span></span>

<span data-ttu-id="851fa-108">Обход сервера-посредника можно использовать, если удовлетворены следующие требования:</span><span class="sxs-lookup"><span data-stu-id="851fa-108">Media bypass can be employed when the following requirements are met:</span></span>

  - <span data-ttu-id="851fa-109">Одноранговый сервер-посредник должен поддерживать необходимые возможности для пропуска мультимедиа, но важнее всего лишь возможность обработки нескольких разветвленных ответов (называемых ранними диалогами).</span><span class="sxs-lookup"><span data-stu-id="851fa-109">A Mediation Server peer must support the necessary capabilities for media bypass, the most important being the ability to handle multiple forked responses (known as “early dialogs”).</span></span> <span data-ttu-id="851fa-110">Обратитесь к производителю шлюза или ITSP, чтобы получить значение максимального количества ранних диалогов, которые могут поддерживать шлюз, PBX или SBC.</span><span class="sxs-lookup"><span data-stu-id="851fa-110">Contact the manufacturer of your gateway or PBX, or your ITSP, to obtain the value for the maximum number of early dialogs that the gateway, PBX, or SBC can accept.</span></span>

  - <span data-ttu-id="851fa-111">Одноранговый сервер должен получать трафик мультимедиа прямо из конечных точек Lync.</span><span class="sxs-lookup"><span data-stu-id="851fa-111">The Mediation Server peer must accept media traffic directly from Lync endpoints.</span></span> <span data-ttu-id="851fa-112">Многие ITSPs позволяют их SBC получать трафик только от сервера обновлений.</span><span class="sxs-lookup"><span data-stu-id="851fa-112">Many ITSPs allow their SBC to receive traffic only from the Mediation Server.</span></span> <span data-ttu-id="851fa-113">Обратитесь к своему ITSPу, чтобы определить, принимает ли его SBC мультимедийный трафик прямо из конечных точек Lync.</span><span class="sxs-lookup"><span data-stu-id="851fa-113">Contact your ITSP to determine whether its SBC accepts media traffic directly from Lync endpoints.</span></span>

  - <span data-ttu-id="851fa-114">Клиенты Lync и одноранговый сервер-посредник должны быть надежно подключены, то есть они размещаются в том же регионе сети или на сайтах сети, которые подключаются к региону по глобальным каналам связи, не имеющим ограничений на пропускную способность.</span><span class="sxs-lookup"><span data-stu-id="851fa-114">Lync clients and a Mediation Server peer must be well connected, meaning that they are either located in the same network region or at network sites that connect to the region over WAN links that have no bandwidth constraints</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="851fa-115">См. также</span><span class="sxs-lookup"><span data-stu-id="851fa-115">See Also</span></span>


[<span data-ttu-id="851fa-116">Режимы обхода сервера-посредника в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="851fa-116">Media bypass modes in Lync Server 2013</span></span>](lync-server-2013-media-bypass-modes.md)  
[<span data-ttu-id="851fa-117">Обход сервера-посредника и контроль допуска звонков в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="851fa-117">Media bypass and call admission control in Lync Server 2013</span></span>](lync-server-2013-media-bypass-and-call-admission-control.md)  
  

<span data-ttu-id="851fa-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="851fa-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

