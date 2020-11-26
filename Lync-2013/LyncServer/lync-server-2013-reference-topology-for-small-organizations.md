---
title: Эталонная топология Lync Server 2013 для малых организаций
description: Эталонная топология Lync Server 2013 для малых организаций.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Reference topology for small organizations
ms:assetid: 0453aeee-c41f-44e6-a6e0-aaace526ca08
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398095(v=OCS.15)
ms:contentKeyID: 48183272
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7f2f23a963543c303e54f8f2773d499e8317a63a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436609"
---
# <a name="reference-topology-for-lync-server-2013-in-small-organizations"></a><span data-ttu-id="fb2fa-103">Топология ссылок для Lync Server 2013 в небольших организациях</span><span class="sxs-lookup"><span data-stu-id="fb2fa-103">Reference topology for Lync Server 2013 in small organizations</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fb2fa-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fb2fa-104">

<span> </span></span></span>

<span data-ttu-id="fb2fa-105">_**Тема последнего изменения:** 2013-10-07_</span><span class="sxs-lookup"><span data-stu-id="fb2fa-105">_**Topic Last Modified:** 2013-10-07_</span></span>

<span data-ttu-id="fb2fa-106">Топология ссылок в малых организациях показывает, как развернуть надежное решение с высокой степенью доступности, развертывая только три сервера с Lync Server.</span><span class="sxs-lookup"><span data-stu-id="fb2fa-106">The reference topology for small organizations shows how you can deploy a robust, highly available solution by deploying only three servers running Lync Server.</span></span>

<span data-ttu-id="fb2fa-107">**Эталонная топология для небольших организаций**</span><span class="sxs-lookup"><span data-stu-id="fb2fa-107">**Reference topology for small organizations**</span></span>

<span data-ttu-id="fb2fa-108">![Схема эталонной топологии с развертыванием трех серверов](images/Gg398095.25196d0d-dd07-451b-83ba-94c0ddf59030(OCS.15).jpg "Схема эталонной топологии с развертыванием трех серверов")</span><span class="sxs-lookup"><span data-stu-id="fb2fa-108">![Reference topology deploying three servers diagram](images/Gg398095.25196d0d-dd07-451b-83ba-94c0ddf59030(OCS.15).jpg "Reference topology deploying three servers diagram")</span></span>

  - <span data-ttu-id="fb2fa-109">**Пара развернутых серверов стандартных выпусков**    У этой организации есть 4 000 пользователей на своем центральном сайте.</span><span class="sxs-lookup"><span data-stu-id="fb2fa-109">**Pair of Standard Edition Servers Deployed**    This organization has 4,000 users at their central site.</span></span> <span data-ttu-id="fb2fa-110">Для обеспечения высокого уровня доступности и аварийного восстановления Организация развернула два сервера стандартных выпусков Standard и пару их вместе.</span><span class="sxs-lookup"><span data-stu-id="fb2fa-110">The organization has deployed two Standard Edition servers and paired them together to enable high availability and disaster recovery.</span></span> <span data-ttu-id="fb2fa-111">Each server homes 2,000 users, but information about all users is synchronized between the two servers.</span><span class="sxs-lookup"><span data-stu-id="fb2fa-111">Each server homes 2,000 users, but information about all users is synchronized between the two servers.</span></span> <span data-ttu-id="fb2fa-112">If one goes down, an administrator can fail over those users to be served by the other server, with a minimum of disruption to users.</span><span class="sxs-lookup"><span data-stu-id="fb2fa-112">If one goes down, an administrator can fail over those users to be served by the other server, with a minimum of disruption to users.</span></span> <span data-ttu-id="fb2fa-113">Дополнительные сведения о возможностях высокой доступности и аварийного восстановления в Lync Server 2013 можно найти [в разделе Планирование обеспечения высокой доступности и аварийного восстановления в Lync server 2013](lync-server-2013-planning-for-high-availability-and-disaster-recovery.md).</span><span class="sxs-lookup"><span data-stu-id="fb2fa-113">For more information about high availability and disaster recovery features in Lync Server 2013, see [Planning for high availability and disaster recovery in Lync Server 2013](lync-server-2013-planning-for-high-availability-and-disaster-recovery.md).</span></span>

  - <span data-ttu-id="fb2fa-114">**Рекомендуется использовать развертывание с пограничным сервером.**</span><span class="sxs-lookup"><span data-stu-id="fb2fa-114">**Edge Server deployment is recommended.**</span></span>   <span data-ttu-id="fb2fa-115">Хотя развертывание пограничного сервера не является обязательным, для внутреннего обмена мгновенными сообщениями, предоставления сведений о присутствии и конференций мы рекомендуем сделать это даже для развертываний малого размера.</span><span class="sxs-lookup"><span data-stu-id="fb2fa-115">Although deploying an Edge Server is not required for internal IM, presence and conferencing, we recommend it even for small deployments.</span></span> <span data-ttu-id="fb2fa-116">Вы можете максимально увеличить инвестиции на Lync Server, развертывая пограничный сервер, чтобы обеспечить обслуживание пользователей, находящихся за пределами брандмауэров вашей организации.</span><span class="sxs-lookup"><span data-stu-id="fb2fa-116">You can maximize your Lync Server investment by deploying an Edge Server to provide service to users currently outside your organization’s firewalls.</span></span> <span data-ttu-id="fb2fa-117">Вам будут доступны следующие преимущества:</span><span class="sxs-lookup"><span data-stu-id="fb2fa-117">The benefits include the following:</span></span>
    
      - <span data-ttu-id="fb2fa-118">Пользователи вашей организации могут использовать возможности Lync Server, если они работают дома или находятся в пути.</span><span class="sxs-lookup"><span data-stu-id="fb2fa-118">Your organization’s own users can use Lync Server functionality, if they are working from home or are out on the road.</span></span>
    
      - <span data-ttu-id="fb2fa-119">Ваши пользователи смогут приглашать внешних пользователей для участия в собраниях.</span><span class="sxs-lookup"><span data-stu-id="fb2fa-119">Your users can invite outside users to participate in meetings.</span></span>
    
      - <span data-ttu-id="fb2fa-120">Если у вас есть партнер, поставщик или организация клиента, который также использует Lync Server, вы можете сформировать *федеративное отношение* с этой организацией.</span><span class="sxs-lookup"><span data-stu-id="fb2fa-120">If you have a partner, vendor or customer organization that also uses Lync Server, you can form a *federated relationship* with that organization.</span></span> <span data-ttu-id="fb2fa-121">После этого развертывание Lync Server сможет распознать пользователей из этой федеративной организации, что лучше для совместной работы.</span><span class="sxs-lookup"><span data-stu-id="fb2fa-121">Your Lync Server deployment would then recognize users from that federated organization, leading to better collaboration.</span></span>
    
      - <span data-ttu-id="fb2fa-122">Пользователи могут обмениваться мгновенными сообщениями с пользователями общедоступных служб обмена мгновенными сообщениями, в том числе любые или все из указанных ниже вариантов: Windows Live, AOL, Yahoo \! и Google.</span><span class="sxs-lookup"><span data-stu-id="fb2fa-122">Your users can exchange instant messages with users of public IM services, including any or all of the following: Windows Live, AOL, Yahoo\!, and Google Talk.</span></span> <span data-ttu-id="fb2fa-123">Для общедоступной службы обмена мгновенными сообщениями с этими службами может потребоваться отдельная лицензия.</span><span class="sxs-lookup"><span data-stu-id="fb2fa-123">A separate license might be required for public IM connectivity with these services.</span></span>
        
        <div>
        

        > [!IMPORTANT]  
        > <UL>
        > <LI>
        > <P><span data-ttu-id="fb2fa-124">По состоянию на 1 сентября 2012, лицензия на подписку на общедоступные службы обмена мгновенными сообщениями в Microsoft Lync ("PIC USL") больше недоступна для приобретения новых или обновленных договоров.</span><span class="sxs-lookup"><span data-stu-id="fb2fa-124">As of September 1st, 2012, the Microsoft Lync Public IM Connectivity User Subscription License (“PIC USL”) is no longer available for purchase for new or renewing agreements.</span></span> <span data-ttu-id="fb2fa-125">Пользователи с активными лицензиями смогут продолжать использовать федерацию с помощью Yahoo!</span><span class="sxs-lookup"><span data-stu-id="fb2fa-125">Customers with active licenses will be able to continue to federate with Yahoo!</span></span> <span data-ttu-id="fb2fa-126">Messenger, пока служба не отключается.</span><span class="sxs-lookup"><span data-stu-id="fb2fa-126">Messenger until the service shut down date.</span></span> <span data-ttu-id="fb2fa-127">Дата окончания жизненного цикла 2014 для AOL и Yahoo! в течение июня.</span><span class="sxs-lookup"><span data-stu-id="fb2fa-127">An end of life date of June 2014 for AOL and Yahoo!</span></span> <span data-ttu-id="fb2fa-128">было объявлено.</span><span class="sxs-lookup"><span data-stu-id="fb2fa-128">has been announced.</span></span> <span data-ttu-id="fb2fa-129">Подробности можно найти <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">в разделе Поддержка общедоступной службы обмена мгновенными сообщениями в Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="fb2fa-129">For details, see <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Support for public instant messenger connectivity in Lync Server 2013</A>.</span></span></P>
        > <LI>
        > <P><span data-ttu-id="fb2fa-130">USL PIC является лицензией на ежемесячную подписку для пользователей Lync Server или Office Communications Server, которая требуется для Федерации с помощью Yahoo!.</span><span class="sxs-lookup"><span data-stu-id="fb2fa-130">The PIC USL is a per-user per-month subscription license that is required for Lync Server or Office Communications Server to federate with Yahoo!</span></span> <span data-ttu-id="fb2fa-131">Messenger.</span><span class="sxs-lookup"><span data-stu-id="fb2fa-131">Messenger.</span></span> <span data-ttu-id="fb2fa-132">Возможность предоставления этой услуги корпорацией Майкрософт зависит от поддержки компании Yahoo!, основного соглашения, для которого выполняется обмотка.</span><span class="sxs-lookup"><span data-stu-id="fb2fa-132">Microsoft’s ability to provide this service has been contingent upon support from Yahoo!, the underlying agreement for which is winding down.</span></span></P>
        > <LI>
        > <P><span data-ttu-id="fb2fa-133">В некоторых случаях Lync — это мощный инструмент для связи между организациями и людьми по всему миру.</span><span class="sxs-lookup"><span data-stu-id="fb2fa-133">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="fb2fa-134">Для интеграции с Windows Live Messenger не требуется дополнительных лицензий на пользователей и устройств за пределами стандартной клиентской лицензии Lync.</span><span class="sxs-lookup"><span data-stu-id="fb2fa-134">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard CAL.</span></span> <span data-ttu-id="fb2fa-135">В этот список будет добавлена Федерация Skype, благодаря чему пользователи Lync смогут общаться с сотнями миллионов людей с помощью обмена мгновенными сообщениями и голосовой связью.</span><span class="sxs-lookup"><span data-stu-id="fb2fa-135">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people with IM and voice.</span></span></P></LI></UL>

        
        </div>

  - <span data-ttu-id="fb2fa-136">**Устойчивость работы сайта филиала.**</span><span class="sxs-lookup"><span data-stu-id="fb2fa-136">**Branch site survivability.**</span></span>   <span data-ttu-id="fb2fa-137">В этой организации запущен пилотный проект функции "Корпоративная голосовая связь" на Lync Server.</span><span class="sxs-lookup"><span data-stu-id="fb2fa-137">This organization is running a pilot program of the Enterprise Voice feature of Lync Server.</span></span> <span data-ttu-id="fb2fa-138">Некоторые пользователи используют Lync Server в качестве единственного голосового решения.</span><span class="sxs-lookup"><span data-stu-id="fb2fa-138">Some users are using Lync Server as their sole voice solution.</span></span> <span data-ttu-id="fb2fa-139">Некоторые из этих пользователей пилотного проекта находятся на сайте филиала.</span><span class="sxs-lookup"><span data-stu-id="fb2fa-139">Some of these Voice pilot users are located at the branch site.</span></span> <span data-ttu-id="fb2fa-140">Сайт филиала не имеет надежной ссылки на глобальную сеть (WAN) на центральный сайт, поэтому там будет развернуто работающее устройство для филиалов.</span><span class="sxs-lookup"><span data-stu-id="fb2fa-140">The branch site does not have a reliable wide area network (WAN) link to the central site, so a Survivable Branch Appliance is deployed there.</span></span> <span data-ttu-id="fb2fa-141">При сбое связи по глобальной сети эта система позволяет пользователям на сайте филиала принимать и посылать вызовы (внутри организации и по ТСОП), пользоваться возможностями голосовой почты и обмениваться двусторонними мгновенными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="fb2fa-141">With this deployed, if the WAN link goes down, users at the branch site can still make and receive calls (both calls within the organization and PSTN calls), have voice mail functionality, and communicate with two-party instant messaging (IM).</span></span> <span data-ttu-id="fb2fa-142">Кроме того, при нарушении связи по глобальной сети возможна проверка подлинности пользователей.</span><span class="sxs-lookup"><span data-stu-id="fb2fa-142">Users can also be authenticated when the WAN link is unavailable as well.</span></span>

  - <span data-ttu-id="fb2fa-143">**Развертывание единой системы обмена сообщениями Exchange.**</span><span class="sxs-lookup"><span data-stu-id="fb2fa-143">**Exchange UM deployment.**</span></span> <span data-ttu-id="fb2fa-144">Эта топология ссылок включает сервер единой системы обмена сообщениями Exchange (UM), на котором запущен Microsoft Exchange Server, а не Lync Server.</span><span class="sxs-lookup"><span data-stu-id="fb2fa-144">This reference topology includes an Exchange Unified Messaging (UM) Server, which runs Microsoft Exchange Server, not Lync Server.</span></span>
    
    <span data-ttu-id="fb2fa-145">Подробнее об обмене мгновенными сообщениями в Exchange можно узнать в разделе [Планирование интеграции единой системы обмена сообщениями Exchange в Lync server 2013](lync-server-2013-planning-for-exchange-unified-messaging-integration.md) и [интеграции единой системы обмена сообщениями Exchange в среде Lync Server 2013](lync-server-2013-hosted-exchange-unified-messaging-integration.md) в документации по планированию.</span><span class="sxs-lookup"><span data-stu-id="fb2fa-145">For details about Exchange UM, see [Planning for Exchange Unified Messaging integration in Lync Server 2013](lync-server-2013-planning-for-exchange-unified-messaging-integration.md) and [Hosted Exchange Unified Messaging integration in Lync Server 2013](lync-server-2013-hosted-exchange-unified-messaging-integration.md) in the Planning documentation.</span></span>

  - <span data-ttu-id="fb2fa-146">**Сервер Office Web Apps.**</span><span class="sxs-lookup"><span data-stu-id="fb2fa-146">**Office Web Apps Server.**</span></span> <span data-ttu-id="fb2fa-147">В каждой организации, где проводятся веб-конференции, рекомендуется развернуть сервер Office Web Apps или ферму таких серверов.</span><span class="sxs-lookup"><span data-stu-id="fb2fa-147">We recommend deploying an Office Web Apps Server or Office Web Apps Server farm in every organization that uses web conferencing.</span></span> <span data-ttu-id="fb2fa-148">Сервер Office Web Apps обеспечивает возможность представления слайдов PowerPoint на веб-конференциях.</span><span class="sxs-lookup"><span data-stu-id="fb2fa-148">Office Web Apps Server makes it possible for PowerPoint slides to be presented in web conferences.</span></span> <span data-ttu-id="fb2fa-149">Дополнительные сведения можно найти [в разделе Настройка интеграции с Office Web Apps Server и Lync Server 2013](lync-server-2013-enabling-office-web-apps-server-and-lync-server-2013.md).</span><span class="sxs-lookup"><span data-stu-id="fb2fa-149">For more information, see [Configuring integration with Office Web Apps Server and Lync Server 2013](lync-server-2013-enabling-office-web-apps-server-and-lync-server-2013.md).</span></span>

<span data-ttu-id="fb2fa-150"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fb2fa-150"></div>

<span> </span>

</div>

</div>

</span></span></div>

