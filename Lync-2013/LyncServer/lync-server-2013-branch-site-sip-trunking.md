---
title: 'Lync Server 2013: магистральные магистрали SIP сайтов филиалов'
description: 'Lync Server 2013: магистральные магистрали SIP сайта филиала.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Branch site SIP trunking
ms:assetid: c4d9dfcd-8baa-41ea-9677-48b0e429429d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412974(v=OCS.15)
ms:contentKeyID: 48185350
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 33e408a462c21ffa6df6e6a2aee50d7b87dca1f7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435945"
---
# <a name="branch-site-sip-trunking-in-lync-server-2013"></a><span data-ttu-id="0e894-103">Branch site SIP trunking in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0e894-103">Branch site SIP trunking in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0e894-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0e894-104">

<span> </span></span></span>

<span data-ttu-id="0e894-105">_**Тема последнего изменения:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="0e894-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="0e894-106">В некоторых случаях может потребоваться реализация распределенной магистрали SIP на выбранных сайтах филиалов.</span><span class="sxs-lookup"><span data-stu-id="0e894-106">In some cases, you may need to implement distributed SIP trunking at selected branch sites.</span></span> <span data-ttu-id="0e894-107">Чтобы определить, нужна ли магистральная линия SIP для сайта филиала, ознакомьтесь со сведениями о [том, как реализовать магистральные линии SIP в Lync Server 2013?](lync-server-2013-how-do-i-implement-sip-trunking.md).</span><span class="sxs-lookup"><span data-stu-id="0e894-107">To determine whether a SIP trunk is needed for a branch site, review the information in [How do I implement SIP trunking in Lync Server 2013?](lync-server-2013-how-do-i-implement-sip-trunking.md).</span></span>

<span data-ttu-id="0e894-108">Дополнительные сведения о поддерживаемых параметрах топологии для развертывания магистральных каналов SIP на филиалах можно найти в статьях решения для обеспечения [устойчивости сайтов в Lync Server 2013](lync-server-2013-branch-site-resiliency-solutions.md).</span><span class="sxs-lookup"><span data-stu-id="0e894-108">For details about the supported topology options for deploying SIP trunks in branch sites, see [Branch-site resiliency solutions in Lync Server 2013](lync-server-2013-branch-site-resiliency-solutions.md).</span></span>

<div>

## <a name="example-branch-site-sip-trunk-requirements-analysis"></a><span data-ttu-id="0e894-109">Пример анализа требований к магистрали SIP для офиса филиала</span><span class="sxs-lookup"><span data-stu-id="0e894-109">Example Branch Site SIP Trunk Requirements Analysis</span></span>

<span data-ttu-id="0e894-110">При развертывании канала SIP на сайте филиала необходимо выполнить анализ затрат для определенного сайта.</span><span class="sxs-lookup"><span data-stu-id="0e894-110">When you decide to deploy a branch site SIP trunk, you need to perform a site-specific cost analysis.</span></span> <span data-ttu-id="0e894-111">Например, если в Нью-Йорке есть сайт, на котором установлен центральный сайт Redmond, Washington и филиал, необходимо выполнить анализ, чтобы определить, следует ли реализовать магистраль SIP из сайта Нью-Йорке для доступа к локальному поставщику услуг.</span><span class="sxs-lookup"><span data-stu-id="0e894-111">For example, an enterprise that has a central site in Redmond, Washington, and a branch site in New York, should do an analysis to determine whether to implement a SIP trunk from the New York site to a local service provider.</span></span>

<span data-ttu-id="0e894-112">Чтобы определить, является ли экономически выгодной распределенная магистральная сеть SIP в Нью-Йорке, определите, какие номера для прямого соединения с внутренними абонентами будет использовать магистраль SIP, и проанализируйте число звонков, совершаемых из офиса в Нью-Йорке в области, не включающие Рэдмонд (425).</span><span class="sxs-lookup"><span data-stu-id="0e894-112">To determine whether a distributed SIP trunk in New York is cost-effective, identify which Direct Inward Dialing (DID) numbers will use the SIP trunk, and analyze the number of calls New York makes to areas other than Redmond (425).</span></span> <span data-ttu-id="0e894-113">Вы можете присвоить прерывание для сайта филиала на центральном сайте.</span><span class="sxs-lookup"><span data-stu-id="0e894-113">You can have DID termination for the branch site at the central site.</span></span> <span data-ttu-id="0e894-114">Например, центр Redmond может размещать номера для сайта филиала Нью-Йорке.</span><span class="sxs-lookup"><span data-stu-id="0e894-114">For example, the Redmond central site can host DID numbers for the New York branch site.</span></span> <span data-ttu-id="0e894-115">Если стоимость реализации распределенной магистральной магистрали SIP меньше, чем стоимость этих звонков, рекомендуется реализовать магистраль SIP на сайте Нью-Йорка.</span><span class="sxs-lookup"><span data-stu-id="0e894-115">If the cost of implementing a distributed SIP trunk is less than the cost of those calls, consider implementing a SIP trunk at the New York branch site.</span></span>

</div>

<div>

## <a name="other-branch-site-sip-trunk-requirements"></a><span data-ttu-id="0e894-116">Другие требования к магистрали SIP для офиса филиала</span><span class="sxs-lookup"><span data-stu-id="0e894-116">Other Branch Site SIP Trunk Requirements</span></span>

<span data-ttu-id="0e894-117">Выбор между развертыванием магистрали SIP вместо шлюза основан на разнице тарифов за междугородные звонки в телефонной сети общего пользования в каждом из вариантов.</span><span class="sxs-lookup"><span data-stu-id="0e894-117">The choice between a deploying a SIP trunk instead of a gateway is based on the difference between the public switched telephone network (PSTN) long distance toll charges of each option.</span></span> <span data-ttu-id="0e894-118">При развертывании канала SIP на сайте филиала необходимо также определить требования к устойчивости и пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="0e894-118">If you deploy a branch site SIP trunk, you also need to determine your resiliency and bandwidth requirements.</span></span> <span data-ttu-id="0e894-119">Если связь между сайтом филиала и центральным сайтом является устойчивой и достаточным объемом пропускной способности, вы можете развернуть магистраль SIP или шлюз.</span><span class="sxs-lookup"><span data-stu-id="0e894-119">If the link between your branch site and central site is resilient and has sufficient bandwidth, you can deploy a SIP trunk or a gateway.</span></span> <span data-ttu-id="0e894-120">Вам не нужно развертывать бесперебойно работающее устройство филиала на сайте филиала.</span><span class="sxs-lookup"><span data-stu-id="0e894-120">You do not need to deploy a Survivable Branch Appliance at the branch site.</span></span> <span data-ttu-id="0e894-121">Если связь между сайтом ветви и центральным сайтом не является устойчивой, разверните бесперебойно работающее устройство филиала или разверните отказоустойчивый сервер филиала с шлюзом или магистральом SIP на сайте филиала.</span><span class="sxs-lookup"><span data-stu-id="0e894-121">If the link between your branch site and central site is not resilient, deploy a Survivable Branch Appliance, or deploy a Survivable Branch Server with either a gateway or SIP trunk at the branch site.</span></span>

<span data-ttu-id="0e894-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0e894-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

