---
title: 'Lync Server 2013: конфигурация маршрутизации на основе расположения для конференций'
description: 'Lync Server 2013: Настройка маршрутизации Location-Based для конференц-связи.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuration of Location-Based Routing for conferencing
ms:assetid: d8c708cc-a1b1-48b1-808c-a64df15f7701
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362846(v=OCS.15)
ms:contentKeyID: 56335088
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6a87f9c799e565f64b0dd30ce025a4e7a3174625
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399949"
---
# <a name="configuration-of-location-based-routing-for-conferencing-in-lync-server-2013"></a><span data-ttu-id="e313d-103">Конфигурация маршрутизации на основе расположения для конференций в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e313d-103">Configuration of Location-Based Routing for conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e313d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e313d-104">

<span> </span></span></span>

<span data-ttu-id="e313d-105">_**Тема последнего изменения:** 2013-09-11_</span><span class="sxs-lookup"><span data-stu-id="e313d-105">_**Topic Last Modified:** 2013-09-11_</span></span>

<span data-ttu-id="e313d-106">Приложение для конференц-связи Location-Based использует конфигурацию Lync Server 2013 Location-Based Routing.</span><span class="sxs-lookup"><span data-stu-id="e313d-106">The Location-Based Routing Conferencing application relies on the configuration of Lync Server 2013 Location-Based Routing.</span></span> <span data-ttu-id="e313d-107">Основные конфигурации следующие:</span><span class="sxs-lookup"><span data-stu-id="e313d-107">The main configurations are the following:</span></span>

  - <span data-ttu-id="e313d-108">Местоположение участников, присоединяющихся к собранию, определяется на основе их сетевого сайта.</span><span class="sxs-lookup"><span data-stu-id="e313d-108">The location of participants joining a meeting is determined based on their network site.</span></span> <span data-ttu-id="e313d-109">Чтобы обеспечить Location-Based маршрутизацию, необходимо определить сайт сети и связанные с ним подсети в Lync Server.</span><span class="sxs-lookup"><span data-stu-id="e313d-109">A network site and its associated network subnets must be defined in Lync Server in order to enforce Location-Based Routing.</span></span>

  - <span data-ttu-id="e313d-110">Для обеспечения Location-Based маршрутизации собраний участники Lync должны быть включены для Location-Based маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="e313d-110">To enforce Location-Based Routing of meetings, Lync participants must be enabled for Location-Based Routing.</span></span>

  - <span data-ttu-id="e313d-111">Чтобы обеспечить Location-Based маршрутизацию конечных точек PSTN, присоединяющихся к собраниям, необходимо настроить магистральную сеть SIP, используемую для подключения конечных точек PSTN, для Location-Based маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="e313d-111">To enforce Location-Based Routing of PSTN endpoints joining meetings, the SIP trunk used to connect the PSTN endpoints must be configured for Location-Based Routing.</span></span>

<span data-ttu-id="e313d-112">Дополнительные сведения о том, как развертывать и настраивать сервер Lync Server 2013 Location-Based Routing, можно найти в разделе Настройка [маршрутизации на основе местоположения](lync-server-2013-configuring-location-based-routing.md).</span><span class="sxs-lookup"><span data-stu-id="e313d-112">For additional information on deploying and configuring Lync Server 2013 Location-Based Routing, please refer Configuring [Location-Based Routing](lync-server-2013-configuring-location-based-routing.md).</span></span>

<div>

## <a name="enabling-the-location-based-routing-conferencing-application"></a><span data-ttu-id="e313d-113">Включение приложения для конференц-связи Location-Based</span><span class="sxs-lookup"><span data-stu-id="e313d-113">Enabling the Location-Based Routing Conferencing Application</span></span>

<span data-ttu-id="e313d-114">Приложение для конференц-связи по Location-Based отключено по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e313d-114">The Location-Based Routing Conferencing application is disabled by default.</span></span> <span data-ttu-id="e313d-115">Перед включением этого приложения необходимо определить и назначить для него правильное значение приоритета.</span><span class="sxs-lookup"><span data-stu-id="e313d-115">Before enabling this application, you need to determine the right priority to assign for the application.</span></span> <span data-ttu-id="e313d-116">Чтобы определить этот приоритет, выполните в командной консоли Lync Server следующий командлет:</span><span class="sxs-lookup"><span data-stu-id="e313d-116">To determine this priority, run the following cmdlet in Lync Server Management Shell:</span></span>

```powershell
Get-CsServerApplication -Identity Service:Registrar:<Pool FQDN>
```

<span data-ttu-id="e313d-117">В этом командлете \<Pool FQDN\> — это пул, в котором должно быть включено приложение для конференц-связи Location-Based.</span><span class="sxs-lookup"><span data-stu-id="e313d-117">In this cmdlet, \<Pool FQDN\> is the pool in which the Location-Based Routing Conferencing application is to be enabled.</span></span>

<span data-ttu-id="e313d-118">Этот командлет вернет список приложений, размещенных на сервере Lync Server, и значение приоритета для каждого из них.</span><span class="sxs-lookup"><span data-stu-id="e313d-118">This cmdlet will return the list of the applications hosted by Lync Server and the priority value for each of them.</span></span> <span data-ttu-id="e313d-119">Приложению для конференц-связи Location-Based необходимо назначить значение приоритета, большее, чем приложение "UdcAgent", и меньше, чем приложения "DefaultRouting", "ExumRouting" и "OutboundRouting".</span><span class="sxs-lookup"><span data-stu-id="e313d-119">The Location-Based Routing Conferencing application needs to be assigned a priority value larger than the “UdcAgent” application and smaller than the “DefaultRouting”, “ExumRouting” and “OutboundRouting” applications.</span></span> <span data-ttu-id="e313d-120">Мы рекомендуем назначить приложению для конференц-связи Location-Based значение приоритета, равное одной точке выше значения приоритета для приложения "UdcAgent".</span><span class="sxs-lookup"><span data-stu-id="e313d-120">We recommend that you assign the Location-Based Routing Conferencing application a priority value that is one point higher than the priority value of the “UdcAgent” application.</span></span>

<span data-ttu-id="e313d-121">Например, если для приложения "UdcAgent" задано значение приоритета "2", в приложении "DefaultRouting" задано значение приоритета "8", а для приложения "ExumRouting" задано значение приоритета "9", а в приложении "OutboundRouting" задано значение приоритета "10", необходимо назначить приложению для конференц-связи Location-Based значение приоритета "3".</span><span class="sxs-lookup"><span data-stu-id="e313d-121">For example, if the “UdcAgent” application has a priority value of “2”, the “DefaultRouting” application has a priority value of “8”, the “ExumRouting” application has a priority value of “9” and the “OutboundRouting” application has a priority value of “10” then you should assign the Location-Based Routing Conferencing application a priority value of “3”.</span></span> <span data-ttu-id="e313d-122">В этом случае приоритет приложений будет выстроен в следующем порядке: другие приложения (приоритеты: от 0 до 1), "UdcAgent" (приоритет: 2), приложение для конференций с маршрутизацией на основе расположения (приоритет: 3), другие приложения (приоритеты: от 4 до 8), "DefaultRouting" (приоритет: 9), "ExumRouting" (приоритет: 10) и "OutboundRouting" (приоритет: 11).</span><span class="sxs-lookup"><span data-stu-id="e313d-122">Doing so would place the priority of the applications in the following order: Other applications (Priorities: 0 to 1), “UdcAgent” (Priority: 2), Location-Based Routing Conferencing application (Priority: 3), other applications (Priorities: 4 to 8), “DefaultRouting” (Priority: 9), “ExumRouting” (Priority: 10) and “OutboundRouting” (Priority: 11).</span></span>

<span data-ttu-id="e313d-123">После того как вы найдете правильное значение приоритета для приложения для конференц-связи Location-Based, введите следующий командлет для каждого пула Front-End или сервера Standard Edition, для которого включены пользователи для маршрутизации Location-Based:</span><span class="sxs-lookup"><span data-stu-id="e313d-123">After you find the correct priority value for the Location-Based Routing Conferencing application, type the following cmdlet for each Front-End pool or Standard Edition Server that homes users enabled for Location-Based Routing:</span></span>

```powershell
New-CsServerApplication -Identity Service:Registrar:<Pool FQDN>/LBRouting -Priority <Application Priority> -Enabled $true -Critical $true -Uri http://www.microsoft.com/LCS/LBRouting
```

<span data-ttu-id="e313d-124">Например:</span><span class="sxs-lookup"><span data-stu-id="e313d-124">For example:</span></span>

```powershell
New-CsServerApplication -Identity Service:Registrar:LS2013CU2LBRPool.contoso.com/LBRouting -Priority 3 -Enabled $true -Critical $true -Uri http://www.microsoft.com/LCS/LBRouting
```

<span data-ttu-id="e313d-125">После использования этого командлета перезапустите все серверы переднего плана в пуле или на серверах стандартных выпусков, где разрешено приложение для конференц-связи Location-Based.</span><span class="sxs-lookup"><span data-stu-id="e313d-125">After using this cmdlet, restart all Front End servers in the pool or the Standard Edition Servers where the Location-Based Routing Conferencing application has been enabled.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="e313d-126">Location-Based принудительные маршруты к конференциям или consultative передач не будут применены, пока не будут перезапусканы все серверы переднего плана в соответствующих пулах или стандартные серверы выпуска.</span><span class="sxs-lookup"><span data-stu-id="e313d-126">Location-Based Routing enforcements to conferences or consultative transfers won’t be enforced until all the Front End Servers in the applicable pools or the Standard Edition Servers are restarted.</span></span>



</div>

<span data-ttu-id="e313d-127">После того как приложение для конференц-связи Location-Based успешно включено и все применимые серверы Lync будут перезапущены, все конференции пользователей Lync, включенные для Location-Based маршрутизации, отслеживаются в целях предотвращения бесплатных вызовов по коммутируемой телефонной связи.</span><span class="sxs-lookup"><span data-stu-id="e313d-127">Once the Location-Based Routing Conferencing application has been successfully enabled and all applicable Lync servers have been restarted, all conferences organized by Lync users enabled for Location-Based Routing will be monitored to prevent PSTN toll bypass</span></span>

<span data-ttu-id="e313d-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e313d-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

