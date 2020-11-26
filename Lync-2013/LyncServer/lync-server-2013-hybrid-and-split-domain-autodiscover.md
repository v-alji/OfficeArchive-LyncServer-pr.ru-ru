---
title: 'Lync Server 2013: гибридный и разделяемый домен — автообнаружения'
description: 'Lync Server 2013: гибридные и разделяемые доменные возможности автообнаружения.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Hybrid and split-domain - Autodiscover
ms:assetid: c855bcc5-b656-4d2d-92d6-f016f2797d3a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945652(v=OCS.15)
ms:contentKeyID: 51541520
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 972233fd10d2b68a002d2d3a203f61bb0bd29574
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427441"
---
# <a name="hybrid-and-split-domain---autodiscover-in-lync-server-2013"></a><span data-ttu-id="6574c-103">Гибридная и Разделяемая доменные возможности автообнаружения в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6574c-103">Hybrid and split-domain - Autodiscover in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6574c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6574c-104">

<span> </span></span></span>

<span data-ttu-id="6574c-105">_**Тема последнего изменения:** 2013-02-14_</span><span class="sxs-lookup"><span data-stu-id="6574c-105">_**Topic Last Modified:** 2013-02-14_</span></span>

<span data-ttu-id="6574c-106">Общее адресное пространство SIP, также называемое развертыванием с *разделением доменов* или *гибридным* развертыванием, — это конфигурация, в которой пользователи развертываются в рамках локального развертывания и из Интернета.</span><span class="sxs-lookup"><span data-stu-id="6574c-106">A shared SIP address space, also known as a *split-domain* deployment, or a *hybrid* deployment, is a configuration where users are deployed across an on-premise deployment and an online environment.</span></span> <span data-ttu-id="6574c-107">Желаемый результат состоит в том, что пользователь вне зависимости от того, где расположен домашний сервер (локально или в сети), подключается к развертыванию и перенаправляется на место своего домашнего сервера.</span><span class="sxs-lookup"><span data-stu-id="6574c-107">The desired outcome is to have a user, regardless of where their home server is located (on-premise or online), log into the deployment and be redirected to their home server location.</span></span> <span data-ttu-id="6574c-108">Для этого функция автообнаружения в Lync Server 2013 используется для перенаправления пользователя Online в сетевую топологию.</span><span class="sxs-lookup"><span data-stu-id="6574c-108">To accomplish this, the Autodiscover feature of Lync Server 2013 is used to redirect the online user to the online topology.</span></span> <span data-ttu-id="6574c-109">Это можно сделать, настроив указатель URL-адреса автообнаружения с помощью командной консоли Lync Server Management Shell, командлета **Get-CsHostingProvider** и командлета **Set-CsHostingProvider** .</span><span class="sxs-lookup"><span data-stu-id="6574c-109">You can do this by configuring the Autodiscover uniform resource locator (URL) by using the Lync Server Management Shell, the **Get-CsHostingProvider** cmdlet, and the **Set-CsHostingProvider** cmdlet.</span></span>

<div>

## <a name="mobility-for-the-split-domain-deployment"></a><span data-ttu-id="6574c-110">Мобильность для раздельного развертывания доменов</span><span class="sxs-lookup"><span data-stu-id="6574c-110">Mobility for the Split Domain Deployment</span></span>

<span data-ttu-id="6574c-111">Вам потребуется собрать и записать следующие развернутые атрибуты:</span><span class="sxs-lookup"><span data-stu-id="6574c-111">You will need to collect and record the following deployed attributes:</span></span>

  - <span data-ttu-id="6574c-112">В командной консоли Lync Server введите</span><span class="sxs-lookup"><span data-stu-id="6574c-112">From the Lync Server Management Shell, type</span></span>
    
        Get-CsHostingProvider

  - <span data-ttu-id="6574c-113">В результатах найдите Интернет-провайдер с атрибутом **ProxyFQDN**.</span><span class="sxs-lookup"><span data-stu-id="6574c-113">In the results, find the online provider with the attribute **ProxyFQDN**.</span></span> <span data-ttu-id="6574c-114">Например, sipfed.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="6574c-114">For example, sipfed.online.lync.com.</span></span>

  - <span data-ttu-id="6574c-115">Запишите значение параметра ProxyFQDN.</span><span class="sxs-lookup"><span data-stu-id="6574c-115">Record the value of the ProxyFQDN.</span></span>

  - <span data-ttu-id="6574c-116">Включите Федерацию в локальной панели управления Lync Server и разрешите Федерацию с помощью веб-поставщика.</span><span class="sxs-lookup"><span data-stu-id="6574c-116">Enable federation in the on-premise Lync Server Control Panel, allowing federation with the online provider.</span></span>

  - <span data-ttu-id="6574c-117">Включите Федерацию для поставщика услуг Интернета.</span><span class="sxs-lookup"><span data-stu-id="6574c-117">Enable federation for the online provider.</span></span> <span data-ttu-id="6574c-118">По умолчанию все пользователи в сети включены в доменную Федерацию и могут взаимодействовать со всеми доменами.</span><span class="sxs-lookup"><span data-stu-id="6574c-118">By default, all online users are enabled for domain federation and can communicate with all domains.</span></span>

  - <span data-ttu-id="6574c-119">Если вы определяете блокируемые и разрешенные домены, определите домены, которые будут явно разрешены или явным образом заблокированы.</span><span class="sxs-lookup"><span data-stu-id="6574c-119">If you will define blocked and allowed domains, determine the domains that you will explicitly allow or explicitly block.</span></span>

  - <span data-ttu-id="6574c-120">Для службы интеграции с Интернетом необходимо планировать исключения брандмауэра, сертификаты и узел DNS (A или AAAA, если используется IPv6).</span><span class="sxs-lookup"><span data-stu-id="6574c-120">For online federation, you must plan for firewall exceptions, certificates, and DNS host (A or AAAA, if using IPv6) records.</span></span> <span data-ttu-id="6574c-121">Кроме того, необходимо настроить политики Федерации.</span><span class="sxs-lookup"><span data-stu-id="6574c-121">Additionally, you must configure federation policies.</span></span> <span data-ttu-id="6574c-122">Подробные сведения можно найти в разделе [планирование для Lync server 2013 и Office Communications Server Federation](lync-server-2013-planning-for-lync-server-and-office-communications-server-federation.md).</span><span class="sxs-lookup"><span data-stu-id="6574c-122">For details, see [Planning for Lync Server 2013 and Office Communications Server federation](lync-server-2013-planning-for-lync-server-and-office-communications-server-federation.md).</span></span>

<span data-ttu-id="6574c-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6574c-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

