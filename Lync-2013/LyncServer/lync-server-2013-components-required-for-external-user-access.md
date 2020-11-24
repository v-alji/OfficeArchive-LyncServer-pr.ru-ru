---
title: 'Lync Server 2013: компоненты, необходимые для доступа внешних пользователей'
description: 'Lync Server 2013: компоненты, необходимые для доступа внешних пользователей.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Components required for external user access
ms:assetid: 2d0f9817-14e7-4109-95dc-62420e3c29e2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425779(v=OCS.15)
ms:contentKeyID: 48183711
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d75ef0c7f2000353a35acefa0b177c90bdcc879b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398530"
---
# <a name="components-required-for-external-user-access-in-lync-server-2013"></a><span data-ttu-id="85629-103">Компоненты, необходимые для доступа внешних пользователей в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="85629-103">Components required for external user access in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="85629-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="85629-104">

<span> </span></span></span>

<span data-ttu-id="85629-105">_**Тема последнего изменения:** 2014-05-29_</span><span class="sxs-lookup"><span data-stu-id="85629-105">_**Topic Last Modified:** 2014-05-29_</span></span>

<span data-ttu-id="85629-106">Большинство пограничных компонентов развертывается в сети периметра.</span><span class="sxs-lookup"><span data-stu-id="85629-106">Most Edge components are deployed in a perimeter network.</span></span> <span data-ttu-id="85629-107">Следующие компоненты составляют топологию пограничного периметра сети.</span><span class="sxs-lookup"><span data-stu-id="85629-107">The following components make up the edge topology of the perimeter network.</span></span> <span data-ttu-id="85629-108">За исключением случаев, когда отмечено иное, компоненты являются частью [сценариев доступа внешних пользователей в Lync Server 2013](lync-server-2013-scenarios-for-external-user-access.md) и находятся в сети периметра.</span><span class="sxs-lookup"><span data-stu-id="85629-108">Except where noted, the components are part of the [Scenarios for external user access in Lync Server 2013](lync-server-2013-scenarios-for-external-user-access.md) and are in the perimeter network.</span></span> <span data-ttu-id="85629-109">К пограничным компонентам относятся следующие:</span><span class="sxs-lookup"><span data-stu-id="85629-109">Edge components include the following:</span></span>

  - <span data-ttu-id="85629-110">Edge Servers</span><span class="sxs-lookup"><span data-stu-id="85629-110">Edge Servers</span></span>

  - <span data-ttu-id="85629-111">Reverse proxies</span><span class="sxs-lookup"><span data-stu-id="85629-111">Reverse proxies</span></span>

  - <span data-ttu-id="85629-112">Firewalls</span><span class="sxs-lookup"><span data-stu-id="85629-112">Firewalls</span></span>

  - <span data-ttu-id="85629-113">Директоры (не являются обязательными и логически расположены во внутренней сети);</span><span class="sxs-lookup"><span data-stu-id="85629-113">Directors (optional, and logically located on the internal network)</span></span>

  - <span data-ttu-id="85629-114">Балансировка нагрузки для масштабируемых пограничных топологий (балансировка нагрузки DNS или подсистема аппаратной балансировки нагрузки)</span><span class="sxs-lookup"><span data-stu-id="85629-114">Load balancing for Scaled Edge Topologies (either DNS load balancing or a hardware load balancer)</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="85629-p102">Использование в одном интерфейсе балансировки нагрузки через DNS, а в другом аппаратной балансировки нагрузки не поддерживается. Необходимо использовать либо ту, либо другую систему балансировки нагрузки для обоих интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="85629-p102">Using DNS load balancing on one interface and hardware load balancing on the other is not supported. You must use hardware load balancing for both interfaces or DNS load balancing for both.</span></span>

    
    </div>

<div>

## <a name="edge-servers"></a><span data-ttu-id="85629-117">пограничные серверы</span><span class="sxs-lookup"><span data-stu-id="85629-117">Edge Servers</span></span>

<span data-ttu-id="85629-118">Пограничные серверы отправляют и получают сетевой трафик для служб, предоставляемых внутренним развертыванием внешними пользователями.</span><span class="sxs-lookup"><span data-stu-id="85629-118">The Edge Servers send and receive network traffic for the services offered by internal deployment by external users.</span></span> <span data-ttu-id="85629-119">На пограничном сервере выполняются следующие службы:</span><span class="sxs-lookup"><span data-stu-id="85629-119">The Edge Server runs the following services:</span></span>

  - <span data-ttu-id="85629-120">**Служба пограничного доступа**   Служба пограничного доступа предоставляет единственную доверенную точку соединения для входящего и исходящего трафика протокола SIP.</span><span class="sxs-lookup"><span data-stu-id="85629-120">**Access Edge service**   The Access Edge service provides a single, trusted connection point for both outbound and inbound Session Initiation Protocol (SIP) traffic.</span></span>

  - <span data-ttu-id="85629-121">**Служба Edge для веб-конференций**   Служба веб-конференций EDGE позволяет внешним пользователям присоединяться к собраниям, размещенным во внутренней среде Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="85629-121">**Web Conferencing Edge service**   The Web Conferencing Edge service enables external users to join meetings that are hosted on your internal Lync Server 2013 deployment.</span></span>

  - <span data-ttu-id="85629-122">**Служба EDGE (/V**   )   Служба "A/V Edge" обеспечивает доступ к аудио-и видеофайлам, приложениям и передачам файлов внешним пользователям.</span><span class="sxs-lookup"><span data-stu-id="85629-122">**A/V Edge service**   The A/V Edge service makes audio, video, application sharing, and file transfer available to external users.</span></span> <span data-ttu-id="85629-123">Пользователи могут добавлять звуковые и видеозаписи для собраний, которые содержат внешних участников, и могут общаться с помощью аудио-и видеофайлов прямо с внешним пользователем в сеансах точка-точка.</span><span class="sxs-lookup"><span data-stu-id="85629-123">Your users can add audio and video to meetings that include external participants, and they can communicate using audio and/or video directly with an external user in point-to-point sessions.</span></span> <span data-ttu-id="85629-124">Служба Edge/V также поддерживает общий доступ к рабочему столу и передачу файлов.</span><span class="sxs-lookup"><span data-stu-id="85629-124">The A/V Edge service also provides support for desktop sharing and file transfer.</span></span>

  - <span data-ttu-id="85629-125">**Служба прокси XMPP**   Прокси-служба XMPP принимает и отправляет сообщения о протоколе передачи сообщений и протокола присутствия (XMPP) для настроенных XMPP федеративных партнеров.</span><span class="sxs-lookup"><span data-stu-id="85629-125">**XMPP Proxy service**   The XMPP Proxy service accepts and sends extensible messaging and presence protocol (XMPP) messages to and from configured XMPP Federated partners.</span></span>

<span data-ttu-id="85629-126">Авторизованные внешние пользователи могут получить доступ к пограничным серверам, чтобы подключиться к внутренней среде Lync Server 2013, но пограничные серверы не предоставляют никаких средств для другого доступа к внутренней сети.</span><span class="sxs-lookup"><span data-stu-id="85629-126">Authorized external users can access the Edge Servers in order to connect to your internal Lync Server 2013 deployment, but the Edge Servers do not provide a means for any other access to the internal network.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="85629-127">Пограничные серверы развертываются для предоставления подключений к включенным клиентам Lync и другим серверам Microsoft EDGE (как в сценариях Федерации).</span><span class="sxs-lookup"><span data-stu-id="85629-127">Edge servers are deployed to provide connections for enabled Lync clients and other Microsoft Edge servers (as in federation scenarios).</span></span> <span data-ttu-id="85629-128">Они не предназначены для разрешения подключений от других типов клиентов конечных точек или серверов.</span><span class="sxs-lookup"><span data-stu-id="85629-128">They are not designed to allow connections from other end point client or server types.</span></span> <span data-ttu-id="85629-129">Сервер шлюза XMPP можно развернуть, чтобы разрешить подключения с настроенными партнерами XMPP.</span><span class="sxs-lookup"><span data-stu-id="85629-129">The XMPP Gateway server can be deployed to allow connections with configured XMPP partners.</span></span> <span data-ttu-id="85629-130">Пограничный сервер и шлюз XMPP могут поддерживать только соединения конечных точек из этих клиентов и типов Федерации.</span><span class="sxs-lookup"><span data-stu-id="85629-130">The Edge server and XMPP Gateway can only support end point connections from these client and federation types.</span></span>



</div>

</div>

<div>

## <a name="reverse-proxy"></a><span data-ttu-id="85629-131">Обратный прокси-сервер</span><span class="sxs-lookup"><span data-stu-id="85629-131">Reverse Proxy</span></span>

<span data-ttu-id="85629-132">Обратный прокси-сервер требуется для указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="85629-132">The reverse proxy is required for the following:</span></span>

  - <span data-ttu-id="85629-133">Разрешение пользователям подключаться к собраниям или конференц-связи с телефонным подключением с помощью простого URL-адреса</span><span class="sxs-lookup"><span data-stu-id="85629-133">To allow users to connect to meetings or dial-in conferences using simple URLs</span></span>

  - <span data-ttu-id="85629-134">Чтобы разрешить внешним пользователям загружать содержимое собрания</span><span class="sxs-lookup"><span data-stu-id="85629-134">To enable external users to download meeting content</span></span>

  - <span data-ttu-id="85629-135">Предоставление внешним пользователям разрешения на развертывание групп рассылки</span><span class="sxs-lookup"><span data-stu-id="85629-135">To enable external users to expand distribution groups</span></span>

  - <span data-ttu-id="85629-136">Предоставление пользователю разрешения на получение сертификата для проверки подлинности на основе сертификата клиента</span><span class="sxs-lookup"><span data-stu-id="85629-136">To allow the user to obtain a user-based certificate for client certificate based authentication</span></span>

  - <span data-ttu-id="85629-137">Как разрешить удаленным пользователям загружать файлы с сервера адресной книги или отправлять запросы в службу веб-запросов к адресной книге.</span><span class="sxs-lookup"><span data-stu-id="85629-137">To enable remote users to download files from the Address Book Server or to submit queries to the Address Book Web Query service</span></span>

  - <span data-ttu-id="85629-138">Разрешение удаленным пользователям получать обновления программного обеспечения клиента и устройства</span><span class="sxs-lookup"><span data-stu-id="85629-138">To enable remote users to obtain updates to client and device software</span></span>

  - <span data-ttu-id="85629-139">Использование мобильных устройств для автоматического доступа к серверам переднего плана, на котором предлагаются службы Mobility Service</span><span class="sxs-lookup"><span data-stu-id="85629-139">To enable mobile devices to automatically discover Front End Servers offering mobility services</span></span>

  - <span data-ttu-id="85629-140">Включение push-уведомлений для мобильных устройств из служб Microsoft 365, Office 365 и push-уведомлений Apple</span><span class="sxs-lookup"><span data-stu-id="85629-140">To enable push notifications to mobile devices from the Microsoft 365, Office 365, or Apple push notification services</span></span>

<span data-ttu-id="85629-141">Дополнительные сведения об обратном прокси и требованиях, которым должны соответствовать обратные прокси-серверы, приведены в разделе [требования к конфигурации для обратного прокси в Lync Server 2013](lync-server-2013-configuration-requirements-for-reverse-proxy.md).</span><span class="sxs-lookup"><span data-stu-id="85629-141">For additional information related to reverse proxies and the requirements that reverse proxies must meet, see the details in [Configuration requirements for reverse proxy in Lync Server 2013](lync-server-2013-configuration-requirements-for-reverse-proxy.md).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="85629-142">Внешние пользователи не нуждаются в подключении к вашей организации через виртуальную частную сеть (VPN) для участия в обмене данными с помощью Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="85629-142">External users do not need a virtual private network (VPN) connection to your organization in order to participate in communications using Lync Server 2013.</span></span> <span data-ttu-id="85629-143">Если в вашей организации реализована технология VPN и пользователи используют VPN для Lync, трафик мультимедиа (например, видеоконференции) может негативно сказаться на нем.</span><span class="sxs-lookup"><span data-stu-id="85629-143">If you have implemented VPN technology in your organization and your users use the VPN for Lync, media traffic (such as video conferencing) can be adversely affected.</span></span> <span data-ttu-id="85629-144">Рекомендуется предоставлять трафик мультимедиа для подключения к службе AV EDGE и минуя VPN.</span><span class="sxs-lookup"><span data-stu-id="85629-144">You should consider providing a means for media traffic to connect to the AV Edge service directly and bypass the VPN.</span></span> <span data-ttu-id="85629-145">Дополнительные сведения можно найти в статье блога на NextHop, в разделе Включение туннеля VPN в Lync Media <A href="https://go.microsoft.com/fwlink/p/?linkid=256532">https://go.microsoft.com/fwlink/p/?LinkId=256532</A></span><span class="sxs-lookup"><span data-stu-id="85629-145">For details, see the NextHop Blog article, “Enabling Lync Media to Bypass a VPN Tunnel,” at <A href="https://go.microsoft.com/fwlink/p/?linkid=256532">https://go.microsoft.com/fwlink/p/?LinkId=256532</A>.</span></span>



</div>

</div>

<div>

## <a name="firewall"></a><span data-ttu-id="85629-146">Брандмауэр</span><span class="sxs-lookup"><span data-stu-id="85629-146">Firewall</span></span>

<span data-ttu-id="85629-147">Вы можете развернуть топологию пограничного сервера только с помощью внешнего брандмауэра или внешних и внутренних брандмауэров.</span><span class="sxs-lookup"><span data-stu-id="85629-147">You can deploy your edge topology with only an external firewall or both external and internal firewalls.</span></span> <span data-ttu-id="85629-148">Архитектурные сценарии включают два брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="85629-148">The scenario architectures include two firewalls.</span></span> <span data-ttu-id="85629-149">Использование двух брандмауэров является рекомендуемым подходом, так как он обеспечивает строгую маршрутизацию из одной сети на другую и защищает внутреннее развертывание за счет двух уровней брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="85629-149">Using two firewalls is the recommended approach because it ensures strict routing from one network edge to the other, and it protects your internal deployment behind two levels of firewall.</span></span>

</div>

<div>

## <a name="director"></a><span data-ttu-id="85629-150">Директор</span><span class="sxs-lookup"><span data-stu-id="85629-150">Director</span></span>

<span data-ttu-id="85629-151">Режиссер — это отдельная необязательная роль сервера в Lync Server 2013, которая не является домашней учетной записью пользователя, а также предоставление служб присутствия или конференций.</span><span class="sxs-lookup"><span data-stu-id="85629-151">A Director is a separate, optional server role in Lync Server 2013 that does not home user accounts, or provide presence or conferencing services.</span></span> <span data-ttu-id="85629-152">Она служит внутренним сервером следующего прыжка, на который пограничный сервер маршрутизирует входящий трафик SIP, предназначенный для внутренних серверов.</span><span class="sxs-lookup"><span data-stu-id="85629-152">It serves as an internal next hop server to which an Edge Server routes inbound SIP traffic destined for internal servers.</span></span> <span data-ttu-id="85629-153">Режиссер выполняет предварительную проверку подлинности входящих запросов и перенаправляет их в домашнюю группу пользователя или на сервер.</span><span class="sxs-lookup"><span data-stu-id="85629-153">The Director preauthenticates inbound requests and redirects them to the user’s home pool or server.</span></span> <span data-ttu-id="85629-154">С помощью предварительной проверки подлинности в режиссере можно удалять запросы из учетных записей пользователей, неизвестных для развертывания.</span><span class="sxs-lookup"><span data-stu-id="85629-154">By preauthenticating at the Director, you can drop requests from user accounts that are unknown to the deployment.</span></span>

<span data-ttu-id="85629-155">Режиссер помогает разрушить стандартные серверы выпусков и серверы переднего плана в пулах переднего плана Enterprise Edition из вредоносных данных, таких как атаки типа "отказ от обслуживания" (DoS).</span><span class="sxs-lookup"><span data-stu-id="85629-155">A Director helps insulate Standard Edition servers and Front End Servers in Enterprise Edition Front End pools from malicious traffic such as denial-of-service (DoS) attacks.</span></span> <span data-ttu-id="85629-156">Если при такой атаке сеть перегружается с недопустимым внешним трафиком, трафик завершается на режиссере.</span><span class="sxs-lookup"><span data-stu-id="85629-156">If the network is flooded with invalid external traffic in such an attack, the traffic ends at the Director.</span></span> <span data-ttu-id="85629-157">Подробнее об использовании режиссеров можно узнать в разделе [сценарии для режиссера в Lync Server 2013](lync-server-2013-scenarios-for-the-director.md).</span><span class="sxs-lookup"><span data-stu-id="85629-157">For details about the use of Directors, see [Scenarios for the Director in Lync Server 2013](lync-server-2013-scenarios-for-the-director.md).</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="85629-158">См. также</span><span class="sxs-lookup"><span data-stu-id="85629-158">See Also</span></span>


[<span data-ttu-id="85629-159">Требования к подсистеме балансировки нагрузки оборудования для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="85629-159">Hardware load balancer requirements for Lync Server 2013</span></span>](lync-server-2013-hardware-load-balancer-requirements.md)  
  

<span data-ttu-id="85629-160"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="85629-160"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

