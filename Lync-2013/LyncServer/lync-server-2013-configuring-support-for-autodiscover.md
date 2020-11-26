---
title: 'Lync Server 2013: Настройка поддержки автообнаружения'
description: 'Lync Server 2013: Настройка поддержки автообнаружения.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring support for Autodiscover
ms:assetid: 3a266456-69a0-4539-ba99-d388b83799a8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945622(v=OCS.15)
ms:contentKeyID: 51541463
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 23991f2f9467035f4ba461ff1b6a84fa8ed1a11d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432613"
---
# <a name="configuring-support-for-autodiscover-in-lync-server-2013"></a><span data-ttu-id="934a2-103">Настройка поддержки автообнаружения в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="934a2-103">Configuring support for Autodiscover in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="934a2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="934a2-104">

<span> </span></span></span>

<span data-ttu-id="934a2-105">_**Тема последнего изменения:** 2013-01-21_</span><span class="sxs-lookup"><span data-stu-id="934a2-105">_**Topic Last Modified:** 2013-01-21_</span></span>

<span data-ttu-id="934a2-106">**Служба автообнаружения** веб-служб Lync Server впервые появилась в накопительном обновлении lync Server 2010: Ноябрь 2011.</span><span class="sxs-lookup"><span data-stu-id="934a2-106">The Lync Server web services **Autodiscover service** first appeared in the Lync Server 2010 Cumulative Update: November 2011.</span></span> <span data-ttu-id="934a2-107">Это обновление сопровождается первоначальным выпуском мобильных клиентов Lync.</span><span class="sxs-lookup"><span data-stu-id="934a2-107">This update was accompanied by the initial release of Lync Mobile clients.</span></span> <span data-ttu-id="934a2-108">Служба автообнаружения предоставляет службы Mobility Services, называемые службой MCX.</span><span class="sxs-lookup"><span data-stu-id="934a2-108">The autodiscover service exposed the mobility services, known as the Mcx service.</span></span>

<span data-ttu-id="934a2-109">Служба автообнаружения действует как единое место для всех клиентов, которые запрашивают сведения о доступных службах и функциях, а также о том, как связаться с sevices — либо полным доменным именем, либо ссылкой на указатель URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="934a2-109">The autodiscover service acts as a single location for all clients to request information on what services and features are available, and how to contact the sevices – either by a fully qualified domain name or a web uniform resource locator reference.</span></span> <span data-ttu-id="934a2-110">Функция автообнаружения предоставляет ряд функций, и каждый клиент будет выполнять запросы на основании функций, которые может использовать клиент.</span><span class="sxs-lookup"><span data-stu-id="934a2-110">Autodiscover exposes a number of features, and each client will make requests based on the features that the client can use.</span></span> <span data-ttu-id="934a2-111">Например, классическое приложение Lync 2013 будет использовать autodiscvoer для определения внешней веб-службы, но не будет использовать службы Mobility (MCX).</span><span class="sxs-lookup"><span data-stu-id="934a2-111">For example, a desktop Lync 2013 client will use autodiscvoer to determine the external web services, but will not use the mobility (Mcx) services.</span></span> <span data-ttu-id="934a2-112">Чтобы правильно определить и позволить клиентам использовать доступные для них функции, необходимо определить сценарии, позволяющие клиенту эффективно находить и использовать записи автообнаружения.</span><span class="sxs-lookup"><span data-stu-id="934a2-112">To properly define and enable your clients to use the features available to them, the scenarios that allow a client to effectively find and use autodiscover entries should be defined.</span></span> <span data-ttu-id="934a2-113">Для использования autodoscover необходимо, чтобы на обратном прокси публикуются веб-службы Lync Server, что записи DNS настроены для разрешения запросов DNS для службы автообнаружения сервера Lync Server и веб-служб Lync Server, а также для того, чтобы службы сертификации правильно настроились для вашего конкретного сценария.</span><span class="sxs-lookup"><span data-stu-id="934a2-113">To use autodoscover, your deployment requires that a reverse proxy publishes the Lync Server web services, that DNS records are configured to resolve DNS queries for the Lync Server autodiscover service and Lync Server web services, and that certificate services are properly configured for your specific scenario.</span></span>

<div>


> [!TIP]  
> <span data-ttu-id="934a2-114">Технические сведения о том, какие элементы содержатся в запросе и ответе автообнаружения, приведены <A href="lync-server-2013-understanding-autodiscover.md">в разделе Общие сведения о автообнаружения в Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="934a2-114">For technical details on what the elements within the autodiscover request/response do, see <A href="lync-server-2013-understanding-autodiscover.md">Understanding Autodiscover in Lync Server 2013</A>.</span></span>



</div>

<span data-ttu-id="934a2-115">Следующие данные и таблицы определяют, какие конфигурации (если таковые имеются) необходимо реализовать для обеспечения полного и эффективного использования службы автообнаружения.</span><span class="sxs-lookup"><span data-stu-id="934a2-115">The following information and tables define, per scenario, what configurations (if any) you need to implement to provide the full and effective use of the autodiscover service.</span></span> <span data-ttu-id="934a2-116">Сведения в указанных ниже разделах относятся к Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="934a2-116">The information in the following topics is specific to Microsoft Lync Server 2013.</span></span> <span data-ttu-id="934a2-117">Если вы ищете руководство по планированию мобильных устройств для Lync Server 2010, ознакомьтесь с разрешениями [https://go.microsoft.com/fwlink/?LinkId=275113](https://go.microsoft.com/fwlink/?linkid=275113) .</span><span class="sxs-lookup"><span data-stu-id="934a2-117">If you are looking for guidance on how to plan Mobility for Lync Server 2010, see [https://go.microsoft.com/fwlink/?LinkId=275113](https://go.microsoft.com/fwlink/?linkid=275113).</span></span> <span data-ttu-id="934a2-118">Развертывание мобильных устройств для Lync Server 2010 можно найти в разделе [https://go.microsoft.com/fwlink/?LinkId=275114](https://go.microsoft.com/fwlink/?linkid=275114)</span><span class="sxs-lookup"><span data-stu-id="934a2-118">To deploy Mobility for Lync Server 2010, see [https://go.microsoft.com/fwlink/?LinkId=275114](https://go.microsoft.com/fwlink/?linkid=275114)</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="934a2-119">Содержание</span><span class="sxs-lookup"><span data-stu-id="934a2-119">In This Section</span></span>

  - [<span data-ttu-id="934a2-120">Настройка DNS для автообнаружения в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="934a2-120">Configuring DNS for Autodiscover in Lync Server 2013</span></span>](lync-server-2013-configuring-dns-for-autodiscover.md)

  - [<span data-ttu-id="934a2-121">Настройка сертификатов для автообнаружения в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="934a2-121">Configuring certificates for Autodiscover in Lync Server 2013</span></span>](lync-server-2013-configuring-certificates-for-autodiscover.md)

  - [<span data-ttu-id="934a2-122">Настройка обратного прокси-сервера для автообнаружения в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="934a2-122">Configuring a reverse proxy for Autodiscover in Lync Server 2013</span></span>](lync-server-2013-configuring-a-reverse-proxy-for-autodiscover.md)

  - [<span data-ttu-id="934a2-123">Настройка автообнаружения в Lync Server 2013 для гибридных развертываний</span><span class="sxs-lookup"><span data-stu-id="934a2-123">Configuring Autodiscover in Lync Server 2013 for hybrid deployments</span></span>](lync-server-2013-configuring-autodiscover-for-hybrid-deployments.md)

<span data-ttu-id="934a2-124"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="934a2-124"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

