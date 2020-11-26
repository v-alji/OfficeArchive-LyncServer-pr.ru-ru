---
title: 'Lync Server 2013: аварийное восстановление пограничного сервера'
description: 'Lync Server 2013: аварийное восстановление пограничного сервера.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Edge Server disaster recovery
ms:assetid: 05ec8d26-d167-4a6f-a966-a1f8873cf974
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687960(v=OCS.15)
ms:contentKeyID: 49733545
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: db084cae9b692ebc9d70660984275aa34096b7d3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437681"
---
# <a name="edge-server-disaster-recovery-in-lync-server-2013"></a><span data-ttu-id="2764a-103">Аварийное восстановление пограничного сервера в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2764a-103">Edge Server disaster recovery in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2764a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2764a-104">

<span> </span></span></span>

<span data-ttu-id="2764a-105">_**Тема последнего изменения:** 2014-03-12_</span><span class="sxs-lookup"><span data-stu-id="2764a-105">_**Topic Last Modified:** 2014-03-12_</span></span>

<span data-ttu-id="2764a-106">Как и в случае с другими ролями сервера, лучшим способом обеспечения высокой доступности серверов пограничного сервера является развертывание нескольких пограничных серверов в пулах на каждом сайте.</span><span class="sxs-lookup"><span data-stu-id="2764a-106">As with other server roles, the best way for you to provide high availability for your Edge Servers is to deploy multiple Edge servers in pools in each site.</span></span> <span data-ttu-id="2764a-107">Если один пограничный сервер отключается, другие серверы в пуле продолжат предоставлять услуги пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="2764a-107">If one Edge Server goes down, the other servers in the pool will continue to provide Edge services.</span></span>

<span data-ttu-id="2764a-108">Чтобы включить процедуры аварийного восстановления, на разных сайтах должны быть развернуты разные пулы пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="2764a-108">To enable disaster recovery procedures, you must have separate Edge Server pools deployed at separate sites.</span></span> <span data-ttu-id="2764a-109">Вам не нужно явным образом создавать пулы Edge вместе, как это происходит с пулами интерфейсных серверов, но при этом несколько пограничных пулов по-прежнему предоставляют сведения о доступности, которые необходимо выполнить, если один из них выходит из пула.</span><span class="sxs-lookup"><span data-stu-id="2764a-109">You do not need to explicitly pair Edge pools together as you do with Front End pools, but having multiple Edge pools still provides the availability to carry on if one entire Edge pool goes down.</span></span> <span data-ttu-id="2764a-110">В следующих разделах содержатся сведения об аварийном восстановлении различных функций пограничных серверов.</span><span class="sxs-lookup"><span data-stu-id="2764a-110">The following sections provide details on disaster recovery for the various functions of Edge Servers.</span></span>

<div>

## <a name="remote-access"></a><span data-ttu-id="2764a-111">Удаленный доступ</span><span class="sxs-lookup"><span data-stu-id="2764a-111">Remote Access</span></span>

<span data-ttu-id="2764a-112">Если у вас несколько сайтов, каждый из которых является пулом пограничных серверов и один из них завершается сбоем, службы удаленного доступа продолжат работать без вмешательства администратора.</span><span class="sxs-lookup"><span data-stu-id="2764a-112">If you have multiple sites, each with a pool of Edge servers, and one entire Edge pool fails, the remote access services will continue to function without needing administrator action.</span></span> <span data-ttu-id="2764a-113">При создании пулов EDGE на разных сайтах нельзя использовать одно полное доменное имя.</span><span class="sxs-lookup"><span data-stu-id="2764a-113">When creating Edge pools in different sites, you cannot use the same FQDN.</span></span> <span data-ttu-id="2764a-114">Каждый пул пограничного сервера должен иметь уникальные полные доменные имена (внутренние и внешние).</span><span class="sxs-lookup"><span data-stu-id="2764a-114">Each Edge pool must have unique FQDNs (internal and external).</span></span> <span data-ttu-id="2764a-115">В пулах EDGE не используются обратные правила прокси-публикации для общения с серверами переднего плана.</span><span class="sxs-lookup"><span data-stu-id="2764a-115">The Edge pools do not use reverse proxy publishing rules to talk to the Front End servers.</span></span> <span data-ttu-id="2764a-116">Автоматический переход на другой ресурс выполняется, когда клиент повторно отправляет записи DNS-службы удаленного доступа, а удаленные пользователи пересылаются на пограничные серверы другого сайта.</span><span class="sxs-lookup"><span data-stu-id="2764a-116">Automatic failover occurs when the client re-queries the remote access DNS service records, and remote users are routed to the Edge servers in another site.</span></span> <span data-ttu-id="2764a-117">Клиент попытается попытаться получить полное доменное имя внешнего края согласно приоритету DNS SRV-записей.</span><span class="sxs-lookup"><span data-stu-id="2764a-117">The client attempts each external Edge FQDN according to the priority of the DNS SRV records.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="2764a-118">Чтобы отработка отказа работала без проблем, убедитесь в том, что брандмауэр позволяет внешним серверам взаимодействовать со всеми пограничными серверами из всех пулов.</span><span class="sxs-lookup"><span data-stu-id="2764a-118">For failover to work smoothly, ensure that the firewall allows the Front End servers from every pool to communicate with all Edge servers.</span></span>



</div>

</div>

<div>

## <a name="federation"></a><span data-ttu-id="2764a-119">Федерация</span><span class="sxs-lookup"><span data-stu-id="2764a-119">Federation</span></span>

<span data-ttu-id="2764a-120">Для связей между федерациями с другими организациями, работающими в Lync Server, входящие запросы Федерации продолжат работать, если у вас есть решения, такие как геодоменные GTM.</span><span class="sxs-lookup"><span data-stu-id="2764a-120">For federation relationships with other organizations running Lync Server, inbound federation requests will continue to work as long as you have solutions like Geo-DNS GTM.</span></span> <span data-ttu-id="2764a-121">Важно понимать, что отработка отказа Федерации не обеспечивает отработку отказа с приоритетом в SRV-записях.</span><span class="sxs-lookup"><span data-stu-id="2764a-121">It’s important to understand that federation failover does not provide failover with priority in SRV records.</span></span> <span data-ttu-id="2764a-122">Приведенное выше решение поможет вам обеспечить возможности аварийного восстановления для входящей интеграции.</span><span class="sxs-lookup"><span data-stu-id="2764a-122">A solution provided earlier can help you provide disaster recovery capabilities for inbound federation.</span></span>

<span data-ttu-id="2764a-123">Исходящая Федерация всегда настраивается с помощью одного пула пограничных серверов или пограничного сервера в Организации.</span><span class="sxs-lookup"><span data-stu-id="2764a-123">Outbound federation is always set up through one published Edge pool or Edge Server in the organization.</span></span> <span data-ttu-id="2764a-124">Если в этом пуле пограничного сервера возникли неполадки, необходимо использовать Topology Builder, чтобы изменить исходящий маршрут Федерации для использования пула пограничного сервера, который еще выполняется.</span><span class="sxs-lookup"><span data-stu-id="2764a-124">If this Edge pool has gone down, you must use Topology Builder to change the outbound federation route to use an Edge pool which is still running.</span></span> <span data-ttu-id="2764a-125">Дополнительные сведения можно найти [в разделе отказ в пуле EDGE, который используется для интеграции Lync Server в Lync server 2013](lync-server-2013-failing-over-the-edge-pool-used-for-lync-server-federation.md)</span><span class="sxs-lookup"><span data-stu-id="2764a-125">For details, see [Failing over the Edge pool used for Lync Server federation in Lync Server 2013](lync-server-2013-failing-over-the-edge-pool-used-for-lync-server-federation.md)</span></span>

</div>

<div>

## <a name="xmpp-federation"></a><span data-ttu-id="2764a-126">XMPP Федерация</span><span class="sxs-lookup"><span data-stu-id="2764a-126">XMPP Federation</span></span>

<span data-ttu-id="2764a-127">В случае XMPP Федерации исходящий и входящий трафик завершатся сбоем, если пул пограничного пула, назначенный как шлюз XMPP Federation Gateway, не проходит.</span><span class="sxs-lookup"><span data-stu-id="2764a-127">For XMPP federation, both outbound and inbound traffic will fail if the Edge pool which is designated as the XMPP federation gateway goes down.</span></span> <span data-ttu-id="2764a-128">Чтобы XMPP Федерация еще раз, необходимо изменить XMPP Федерации на использование другого пула пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="2764a-128">To make XMPP federation work again, you must change XMPP federation to use a different Edge pool.</span></span> <span data-ttu-id="2764a-129">Дополнительные сведения можно найти [в разделе отказ в пуле EDGE, который используется для Федерации XMPP в Lync Server 2013](lync-server-2013-failing-over-the-edge-pool-used-for-xmpp-federation.md).</span><span class="sxs-lookup"><span data-stu-id="2764a-129">For details, see [Failing over the Edge pool used for XMPP federation in Lync Server 2013](lync-server-2013-failing-over-the-edge-pool-used-for-xmpp-federation.md).</span></span>

</div>

<div>

## <a name="edge-pool-fails-but-front-end-pool-is-still-running"></a><span data-ttu-id="2764a-130">Пул пограничного сервера завершает работу со сбоем, но пул переднего плана по-прежнему работает</span><span class="sxs-lookup"><span data-stu-id="2764a-130">Edge Pool Fails But Front End Pool Is Still Running</span></span>

<span data-ttu-id="2764a-131">Если при пограничного пула на сайте происходит сбой, но пул переднего плана на этом сайте по-прежнему работает, вам нужно будет изменить пул переднего плана так, чтобы он использовал другой пул EDGE на другом сайте, пока пул первого пограничного пула не будет остановлен.</span><span class="sxs-lookup"><span data-stu-id="2764a-131">If an Edge pool fails at a site, but the Front End pool at that site is still running, you will need to change the Front End pool to use a different Edge pool at a different site while that first Edge pool is down.</span></span> <span data-ttu-id="2764a-132">Дополнительные сведения можно найти [в разделе Изменение пула EDGE, связанного с пулом переднего плана в Lync Server 2013](lync-server-2013-changing-the-edge-pool-associated-with-a-front-end-pool.md).</span><span class="sxs-lookup"><span data-stu-id="2764a-132">For more information, see [Changing the Edge pool associated with a Front End pool in Lync Server 2013](lync-server-2013-changing-the-edge-pool-associated-with-a-front-end-pool.md).</span></span>

<span data-ttu-id="2764a-133"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2764a-133"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

