---
title: 'Lync Server 2013: определение требований для серверов переднего плана, обмена мгновенными сообщениями и сведениями о присутствии'
description: 'Lync Server 2013: определение требований к серверам переднего плана, мгновенным сообщениям и сведениям о присутствии.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Defining your requirements for Front End Servers, instant messaging, and presence
ms:assetid: c21198bc-520c-4d17-8b84-7ff1475b9b0a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412956(v=OCS.15)
ms:contentKeyID: 48185319
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 923132b32d5aef80191b19a7b85c3f17276e5946
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430814"
---
# <a name="defining-your-requirements-for-front-end-servers-instant-messaging-and-presence-in-lync-server-2013"></a><span data-ttu-id="16706-103">Определение требований для серверов переднего плана, обмена мгновенными сообщениями и сведениями о присутствии в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="16706-103">Defining your requirements for Front End Servers, instant messaging, and presence in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="16706-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="16706-104">

<span> </span></span></span>

<span data-ttu-id="16706-105">_**Тема последнего изменения:** 2013-10-07_</span><span class="sxs-lookup"><span data-stu-id="16706-105">_**Topic Last Modified:** 2013-10-07_</span></span>

<span data-ttu-id="16706-106">Главная задача планирования обмена мгновенными сообщениями и присутствия состоит в том, что у вас достаточно серверов переднего плана для пользователей.</span><span class="sxs-lookup"><span data-stu-id="16706-106">The main task of planning for instant messaging (IM) and presence is ensuring that you have enough Front End Servers for your users.</span></span>

<div>

## <a name="enabling-communication-with-external-users"></a><span data-ttu-id="16706-107">Включение связи с внешними пользователями</span><span class="sxs-lookup"><span data-stu-id="16706-107">Enabling Communication with External Users</span></span>

<span data-ttu-id="16706-108">Вы можете значительно повысить эффективность ваших капиталовложений в Lync Server, разрешив пользователям общаться с внешними пользователями.</span><span class="sxs-lookup"><span data-stu-id="16706-108">You can greatly increase the benefits of your investment in Lync Server by enabling your users to communicate with external users.</span></span> <span data-ttu-id="16706-109">К внешним пользователям относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="16706-109">External users can include:</span></span>

  - <span data-ttu-id="16706-110">**Удаленные пользователи**   Собственные пользователи организации, работающие за пределами брандмауэров и использующие Ноутбуки и другие серверные устройства Lync.</span><span class="sxs-lookup"><span data-stu-id="16706-110">**Remote users**   Your organization’s own users, when they are working outside your firewalls and are using their laptops or other Lync Server devices.</span></span>

  - <span data-ttu-id="16706-111">**Федеративные пользователи**   Пользователи из компаний, которым вы работаете, и которые работают с Lync Server.</span><span class="sxs-lookup"><span data-stu-id="16706-111">**Federated users**   Users from companies you work with who also run Lync Server.</span></span> <span data-ttu-id="16706-112">С этими компаниями создаются отношения федерации, что упрощает взаимодействие сотрудников организации с такими пользователями.</span><span class="sxs-lookup"><span data-stu-id="16706-112">To enable your users to easily contact these users, you create federated relationships with these companies.</span></span>

  - <span data-ttu-id="16706-113">**Общедоступные пользователи**   Пользователи общедоступных служб обмена мгновенными сообщениями, такие как службы обмена мгновенными сообщениями, предоставленные в сети Интернет-служб, Yahoo \! и AOL, а также пользователи поставщиков и серверов, использующих протокол расширенного обмена сообщениями (XMPP), например Google поговорить.</span><span class="sxs-lookup"><span data-stu-id="16706-113">**Public users**   Users of public IM services, such as IM services provided by the Windows Live network of Internet services, Yahoo\!, and AOL, and users of providers and servers that use Extensible Messaging and Presence Protocol (XMPP), such as Google Talk.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="16706-114">Обратите внимание, что для общедоступной службы обмена мгновенными сообщениями с Windows Live, AOL и Yahoo! может потребоваться отдельная лицензия.</span><span class="sxs-lookup"><span data-stu-id="16706-114">Note that a separate license might be required for public IM connectivity with Windows Live, AOL, and Yahoo!</span></span>

    
    </div>
    
    <div>
    

    > [!IMPORTANT]  
    > <UL>
    > <LI>
    > <P><span data-ttu-id="16706-115">По состоянию на 1 сентября 2012, лицензия на подписку на общедоступные службы обмена мгновенными сообщениями в Microsoft Lync ("PIC USL") больше недоступна для приобретения новых или обновленных договоров.</span><span class="sxs-lookup"><span data-stu-id="16706-115">As of September 1st, 2012, the Microsoft Lync Public IM Connectivity User Subscription License (“PIC USL”) is no longer available for purchase for new or renewing agreements.</span></span> <span data-ttu-id="16706-116">Пользователи с активными лицензиями смогут продолжать использовать федерацию с помощью Yahoo!</span><span class="sxs-lookup"><span data-stu-id="16706-116">Customers with active licenses will be able to continue to federate with Yahoo!</span></span> <span data-ttu-id="16706-117">Messenger, пока служба не отключается.</span><span class="sxs-lookup"><span data-stu-id="16706-117">Messenger until the service shut down date.</span></span> <span data-ttu-id="16706-118">Дата окончания жизненного цикла 2014 для AOL и Yahoo! в течение июня.</span><span class="sxs-lookup"><span data-stu-id="16706-118">An end of life date of June 2014 for AOL and Yahoo!</span></span> <span data-ttu-id="16706-119">было объявлено.</span><span class="sxs-lookup"><span data-stu-id="16706-119">has been announced.</span></span> <span data-ttu-id="16706-120">Подробности можно найти <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">в разделе Поддержка общедоступной службы обмена мгновенными сообщениями в Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="16706-120">For details, see <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Support for public instant messenger connectivity in Lync Server 2013</A>.</span></span></P>
    > <LI>
    > <P><span data-ttu-id="16706-121">USL PIC является лицензией на ежемесячную подписку для пользователей Lync Server или Office Communications Server, которая требуется для Федерации с помощью Yahoo!.</span><span class="sxs-lookup"><span data-stu-id="16706-121">The PIC USL is a per-user per-month subscription license that is required for Lync Server or Office Communications Server to federate with Yahoo!</span></span> <span data-ttu-id="16706-122">Messenger.</span><span class="sxs-lookup"><span data-stu-id="16706-122">Messenger.</span></span> <span data-ttu-id="16706-123">Возможность предоставления этой услуги корпорацией Майкрософт зависит от поддержки компании Yahoo!, основного соглашения, для которого выполняется обмотка.</span><span class="sxs-lookup"><span data-stu-id="16706-123">Microsoft’s ability to provide this service has been contingent upon support from Yahoo!, the underlying agreement for which is winding down.</span></span></P>
    > <LI>
    > <P><span data-ttu-id="16706-124">В некоторых случаях Lync — это мощный инструмент для связи между организациями и людьми по всему миру.</span><span class="sxs-lookup"><span data-stu-id="16706-124">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="16706-125">Для интеграции с Windows Live Messenger не требуется дополнительных лицензий на пользователей и устройств за пределами стандартной клиентской лицензии Lync.</span><span class="sxs-lookup"><span data-stu-id="16706-125">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard CAL.</span></span> <span data-ttu-id="16706-126">В этот список будет добавлена Федерация Skype, благодаря чему пользователи Lync смогут общаться с сотнями миллионов людей с помощью обмена мгновенными сообщениями и голосовой связью.</span><span class="sxs-lookup"><span data-stu-id="16706-126">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people with IM and voice.</span></span></P></LI></UL>

    
    </div>

<span data-ttu-id="16706-127">Чтобы включить любые из этих сценариев, вам нужно развернуть пограничный сервер, чтобы обеспечить безопасную связь между развертыванием Lync Server и внешними пользователями.</span><span class="sxs-lookup"><span data-stu-id="16706-127">To enable any or all of these scenarios, you need to deploy an Edge Server to help enable secure communications between your Lync Server deployment and external users.</span></span> <span data-ttu-id="16706-128">Удаленные пользователи вашей организации и пользователи в федеративных организациях смогут видеть сведения о присутствии друг друга и общаться с помощью мгновенных сообщений.</span><span class="sxs-lookup"><span data-stu-id="16706-128">Your organization’s remote users and users at federated organizations will be able to see each other’s presence and communicate using IM.</span></span> <span data-ttu-id="16706-129">Подробнее о том, как включить связь с внешними пользователями, можно узнать в разделе [Планирование доступа внешних пользователей в Lync Server 2013](lync-server-2013-planning-for-external-user-access.md) в документации по планированию.</span><span class="sxs-lookup"><span data-stu-id="16706-129">For details about enabling communication with external users, see [Planning for external user access in Lync Server 2013](lync-server-2013-planning-for-external-user-access.md) in the Planning documentation.</span></span>

</div>

<div>

## <a name="archiving-im-content"></a><span data-ttu-id="16706-130">Сохранение содержимого для обмена мгновенными сообщениями</span><span class="sxs-lookup"><span data-stu-id="16706-130">Archiving IM Content</span></span>

<span data-ttu-id="16706-131">Lync Server предоставляет возможности, которые можно использовать, если в вашей организации должны следовать правила соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="16706-131">Lync Server provides features you can use if your organization must follow compliance regulations.</span></span> <span data-ttu-id="16706-132">С помощью службы архивации можно архивировать содержимое мгновенных сообщений для всех пользователей в организации или только для некоторых указанных пользователей.</span><span class="sxs-lookup"><span data-stu-id="16706-132">You can use Archiving to archive the content of IM messages for all users in your organization or for only certain users that you specify.</span></span> <span data-ttu-id="16706-133">Подробности можно найти [в разделе Планирование архивации в Lync Server 2013](lync-server-2013-planning-for-archiving.md) в документации по планированию.</span><span class="sxs-lookup"><span data-stu-id="16706-133">For details, see [Planning for Archiving in Lync Server 2013](lync-server-2013-planning-for-archiving.md) in the Planning documentation.</span></span>

<span data-ttu-id="16706-134">Если вы также развернули Microsoft Exchange Server 2013, вы можете интегрировать архивирование данных Exchange с архивацией данных сервера Lync и использовать один инструмент для поиска обоих типов архивных данных.</span><span class="sxs-lookup"><span data-stu-id="16706-134">If you also have Microsoft Exchange Server 2013 deployed, you can integrate the archiving of Exchange data with the archiving of Lync Server data, and use a single tool to search both types of archived data.</span></span> <span data-ttu-id="16706-135">Дополнительные сведения можно найти [в разделе Настройка Microsoft Lync server 2013 для использования архивации Microsoft Exchange server 2013](configuring-lync-server-2013-to-use-microsoft-exchange-server-2013-archiving.md).</span><span class="sxs-lookup"><span data-stu-id="16706-135">For more information, see [Configuring Microsoft Lync Server 2013 to use Microsoft Exchange Server 2013 archiving](configuring-lync-server-2013-to-use-microsoft-exchange-server-2013-archiving.md).</span></span>

<span data-ttu-id="16706-136"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="16706-136"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

