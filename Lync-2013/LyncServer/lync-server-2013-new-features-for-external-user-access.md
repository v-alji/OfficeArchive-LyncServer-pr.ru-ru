---
title: 'Lync Server 2013: новые функции для доступа внешних пользователей'
description: 'Lync Server 2013: новые возможности для доступа внешних пользователей.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: New features for external user access
ms:assetid: 99da6bd5-ec14-4ad9-8f7d-37fbddf567dd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398794(v=OCS.15)
ms:contentKeyID: 48184884
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d9d960a469334a836c453e8ae3bbf51f1b66bb93
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445402"
---
# <a name="new-features-for-external-user-access-in-lync-server-2013"></a><span data-ttu-id="39d9a-103">Новые функции для доступа внешних пользователей в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="39d9a-103">New features for external user access in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="39d9a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="39d9a-104">

<span> </span></span></span>

<span data-ttu-id="39d9a-105">_**Тема последнего изменения:** 2012-10-17_</span><span class="sxs-lookup"><span data-stu-id="39d9a-105">_**Topic Last Modified:** 2012-10-17_</span></span>

<span data-ttu-id="39d9a-106">В Lync Server 2013 появились новые функции, расширяющие возможности и способы связи для пользователей.</span><span class="sxs-lookup"><span data-stu-id="39d9a-106">Lync Server 2013 introduces new features that extend the features and communications methods for your users.</span></span> <span data-ttu-id="39d9a-107">Кроме того, Lync Server 2013 предлагает изменения в существующих службах для лучшей интеграции и продления служб, доступных для вашей организации.</span><span class="sxs-lookup"><span data-stu-id="39d9a-107">Also, Lync Server 2013 introduces changes to existing services to better integrate and extend the services that are available to your organization.</span></span> <span data-ttu-id="39d9a-108">Ниже приведена сводка изменений, которые могут повлиять на планирование и развертывание служб сервера Lync Server 2013 Edge Server.</span><span class="sxs-lookup"><span data-stu-id="39d9a-108">Following is a summary of changes that may affect your planning and deployment of Lync Server 2013 Edge Server services.</span></span>

  - <span data-ttu-id="39d9a-109">**Поддержка адресации IPv6**   Lync Server 2013 поддерживает адресацию IPv6 для всех служб пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="39d9a-109">**Support for IPv6 addressing**   Lync Server 2013 supports IPv6 addressing for all Edge Server services.</span></span> <span data-ttu-id="39d9a-110">Если вы указали IPv6-адреса для интерфейсов с помощью конфигурации в Windows Server, вы можете использовать IPv6-адреса в конфигурации пограничного сервера с помощью конфигурации IP Address Builder в построителе топологии.</span><span class="sxs-lookup"><span data-stu-id="39d9a-110">If you have provided IPv6 addresses for the interfaces through configuration in Windows Server, you can use IPv6 addresses in your Edge Server configuration through the IP address configuration in Topology Builder.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="39d9a-111">Использование IPv6-адресов в Lync Server 2013 зависит от поддержки IPv6 в маршрутизаторах и брандмауэрах, а также о поддержке через поставщика услуг Интернета.</span><span class="sxs-lookup"><span data-stu-id="39d9a-111">Use of IPv6 addresses in Lync Server 2013 depends on support of IPv6 in routers and firewalls that your organization deploys, as well as support through your Internet service provider.</span></span>

    
    </div>

  - <span data-ttu-id="39d9a-112">**Расширяемый протокол передачи сообщений и присутствия (XMPP)**   Lync Server 2013 представляет полностью интегрированный прокси-сервер XMPP (развернутый на пограничном сервере) и шлюз XMPP, развернутый на серверах переднего плана.</span><span class="sxs-lookup"><span data-stu-id="39d9a-112">**Extensible Messaging and Presence Protocol (XMPP)**   Lync Server 2013 introduces a fully integrated XMPP proxy (deployed on the Edge Servers) and an XMPP gateway deployed on your Front End Servers.</span></span> <span data-ttu-id="39d9a-113">Вы можете развернуть XMPP Федерацию как дополнительный компонент.</span><span class="sxs-lookup"><span data-stu-id="39d9a-113">You can deploy XMPP federation as an optional component.</span></span> <span data-ttu-id="39d9a-114">Добавление и Настройка шлюза XMPP proxy и XMPP позволит пользователям Microsoft Lync 2013 добавлять контакты из партнеров на основе XMPP для обмена мгновенными сообщениями и их присутствия.</span><span class="sxs-lookup"><span data-stu-id="39d9a-114">Adding and configuring the XMPP proxy and XMPP gateway will allow your Microsoft Lync 2013 users to add contacts from XMPP-based partners for instant messaging (IM) and presence.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="39d9a-115">В настоящее время службы XMPP в Lync Server 2013 предоставляют мгновенные сообщения и сведения о присутствии между клиентами Lync и контактами на XMPP.</span><span class="sxs-lookup"><span data-stu-id="39d9a-115">Currently, the XMPP services in Lync Server 2013 only provide instant messaging and presence between Lync clients and XMPP-based contacts.</span></span>

    
    </div>

  - <span data-ttu-id="39d9a-116">**Услуги мобильной связи для мобильных клиентов**   В обновлении клиента для Lync Server 2010 службы Mobility Services в Lync Server 2013 позволяют клиентам Microsoft Lync Mobile на мобильных телефонах и планшетных устройствах с помощью поддерживаемых мобильных устройств Apple iOS, Android, Windows Phone или Nokia выполнять такие действия, как отправка и получение мгновенных сообщений, просмотр контактов и Просмотр сведений о присутствии.</span><span class="sxs-lookup"><span data-stu-id="39d9a-116">**Mobility services for Mobile clients**   Introduced in a customer update for Lync Server 2010, Mobility services in Lync Server 2013 allow Microsoft Lync Mobile clients on mobile phones and tablet devices using supported Apple iOS, Android, Windows Phone, or Nokia mobile devices to perform such activities as sending and receiving instant messages, viewing contacts, and viewing presence.</span></span> <span data-ttu-id="39d9a-117">Кроме того, мобильные устройства поддерживают некоторые корпоративные функции голосовой связи, например, для присоединения к Конференции, звонков по каналам связи с одним числом, а также голосовую почту и уведомление о пропущенных звонках.</span><span class="sxs-lookup"><span data-stu-id="39d9a-117">In addition, mobile devices support some Enterprise Voice features, such as click to join a conference, Call via Work, single number reach, voice mail, and missed call notification.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="39d9a-118">В службах Mobility Service используются обратные прокси-серверы и опубликованные службы, развернутые на серверах переднего плана.</span><span class="sxs-lookup"><span data-stu-id="39d9a-118">The mobility services use the reverse proxy and published services that are deployed on your Front End Servers.</span></span> <span data-ttu-id="39d9a-119">Пограничные серверы не требуют изменений.</span><span class="sxs-lookup"><span data-stu-id="39d9a-119">No changes are required to Edge Servers.</span></span>

    
    </div>

  - <span data-ttu-id="39d9a-120">**Режиссеры — это необязательная роль**   Роль директора сервера в топологии Lync Server 2013 не изменилась.</span><span class="sxs-lookup"><span data-stu-id="39d9a-120">**Directors are an optional role**   The role of the Director server in the Lync Server 2013 topology has not changed.</span></span> <span data-ttu-id="39d9a-121">Он по-прежнему содержит веб-службы, предварительную проверку подлинности входящих запросов пользователя и направляет внешних пользователей в свой личный пул.</span><span class="sxs-lookup"><span data-stu-id="39d9a-121">It still hosts web services, pre-authenticates incoming user requests, and directs external users to their home pool.</span></span> <span data-ttu-id="39d9a-122">Изменение режиссера с помощью рекомендованной роли на дополнительную роль не снижает ценность режиссера, но уменьшает число серверов и другие требования к оборудованию (например, подсистема балансировки нагрузки для этого директора) без нарушения функций и функциональности.</span><span class="sxs-lookup"><span data-stu-id="39d9a-122">Changing the Director from a recommended role to an optional role does not diminish the value of the Director, but emphasizes reducing server count and other hardware requirements (for example, hardware load balancers for the Director) requirements without compromising features and functionality.</span></span> <span data-ttu-id="39d9a-123">Поскольку сервер переднего плана может выполнять те же задачи, что и режиссер, но не влияет на предоставленные услуги, вы можете при желании развернуть их.</span><span class="sxs-lookup"><span data-stu-id="39d9a-123">Because the Front End Servers can do the same job as the Director with no impact to services provided, you can optionally deploy Directors if you choose to.</span></span> <span data-ttu-id="39d9a-124">Вы можете безопасно исключить режиссера, чтобы серверный интерфейс предоставил вам те же услуги на своем своем компьютере.</span><span class="sxs-lookup"><span data-stu-id="39d9a-124">You can safely exclude the Director with confidence that the Front End Servers will provide the same services in their place.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="39d9a-125">См. также</span><span class="sxs-lookup"><span data-stu-id="39d9a-125">See Also</span></span>


[<span data-ttu-id="39d9a-126">Планирование и настройка IPv6 в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="39d9a-126">Planning for and configuring IPv6 in Lync Server 2013</span></span>](lync-server-2013-planning-for-and-configuring-ipv6.md)  


[<span data-ttu-id="39d9a-127">Планирование доступа внешних пользователей в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="39d9a-127">Planning for external user access in Lync Server 2013</span></span>](lync-server-2013-planning-for-external-user-access.md)  
[<span data-ttu-id="39d9a-128">Планирование Федерации протоколов обмена сообщениями и присутствия в XMPP в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="39d9a-128">Planning for extensible messaging and presence protocol (XMPP) federation in Lync Server 2013</span></span>](lync-server-2013-planning-for-extensible-messaging-and-presence-protocol-xmpp-federation.md)  
  

<span data-ttu-id="39d9a-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="39d9a-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

