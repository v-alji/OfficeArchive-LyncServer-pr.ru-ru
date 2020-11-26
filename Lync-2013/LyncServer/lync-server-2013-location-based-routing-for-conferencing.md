---
title: 'Lync Server 2013: Location-Based маршрутизацию для конференц-связи'
description: 'Lync Server 2013: Location-Based маршрутизацию для конференц-связи.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Location-Based Routing for conferencing
ms:assetid: e1acb1ba-0ed2-4abf-8a7b-1ca3049e95e3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362849(v=OCS.15)
ms:contentKeyID: 56335087
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 979c835e03bbf87c9a9bf86b030cb9a8f4e138e0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426545"
---
# <a name="location-based-routing-for-conferencing-in-lync-server-2013"></a><span data-ttu-id="cf718-103">Location-Based маршрутизации для конференций в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cf718-103">Location-Based Routing for conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cf718-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cf718-104">

<span> </span></span></span>

<span data-ttu-id="cf718-105">_**Тема последнего изменения:** 2013-07-31_</span><span class="sxs-lookup"><span data-stu-id="cf718-105">_**Topic Last Modified:** 2013-07-31_</span></span>

<span data-ttu-id="cf718-106">Маршрутизация Location-Based позволяет ограничить маршрутизацию звонков между конечными точками VoIP и КОММУТИРУЕМыми конечными точками, основываясь на местоположении сторон в звонке.</span><span class="sxs-lookup"><span data-stu-id="cf718-106">Location-Based Routing makes it possible to restrict the routing of calls between VoIP endpoints and PSTN endpoints based on the location of the parties in the call.</span></span> <span data-ttu-id="cf718-107">Благодаря накопительному обновлению 2 для Lync Server 2013 Location-Based правила маршрутизации можно применять к собраниям Lync (например, конференции), чтобы предотвратить бесплатный звонок.</span><span class="sxs-lookup"><span data-stu-id="cf718-107">With Cumulative Update 2 of Lync Server 2013, Location-Based Routing rules can be enforced on Lync meetings (i.e. conferences) to prevent PSTN toll bypass.</span></span> <span data-ttu-id="cf718-108">Приложение отслеживает активную конференцию и применяет Location-Based ограничениям маршрутизации в зависимости от того, где они участвуют.</span><span class="sxs-lookup"><span data-stu-id="cf718-108">The application monitors an active conference and enforces Location-Based Routing restrictions based on the location of users participating.</span></span> <span data-ttu-id="cf718-109">Кроме того, приложение для конференц-связи с Location-Based позволяет принудительно применять Location-Based ограничения маршрутизации к consultative передачам, содержащим конечные точки PSTN.</span><span class="sxs-lookup"><span data-stu-id="cf718-109">The Location-Based Routing Conferencing application additionally enables the enforcement of Location-Based Routing restrictions to consultative transfers involving PSTN endpoints.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="cf718-110">Содержание</span><span class="sxs-lookup"><span data-stu-id="cf718-110">In This Section</span></span>

  - [<span data-ttu-id="cf718-111">Общие сведения о маршрутизации Location-Based для конференц-связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cf718-111">Overview of Location-Based Routing for conferencing in Lync Server 2013</span></span>](lync-server-2013-overview-of-location-based-routing-for-conferencing.md)

  - [<span data-ttu-id="cf718-112">Маршрутизация на основе местоположения и передача звонков consultative в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cf718-112">Location-Based Routing and consultative call transfers in Lync Server 2013</span></span>](lync-server-2013-location-based-routing-and-consultative-call-transfers.md)

  - [<span data-ttu-id="cf718-113">Требования для маршрутизации Location-Based для конференц-связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cf718-113">Requirements for Location-Based Routing for conferencing in Lync Server 2013</span></span>](lync-server-2013-requirements-for-location-based-routing-for-conferencing.md)

  - [<span data-ttu-id="cf718-114">Конфигурация маршрутизации на основе расположения для конференций в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cf718-114">Configuration of Location-Based Routing for conferencing in Lync Server 2013</span></span>](lync-server-2013-configuration-of-location-based-routing-for-conferencing.md)

<span data-ttu-id="cf718-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cf718-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

