---
title: 'Lync Server 2013: планирование подключения общедоступной службы обмена мгновенными сообщениями'
description: 'Lync Server 2013: планирование подключения общедоступной службы обмена мгновенными сообщениями.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for public instant messaging connectivity
ms:assetid: e75e8884-05c7-414a-8014-bc9aa8126fb7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205349(v=OCS.15)
ms:contentKeyID: 48185698
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9a020a291a39d78aea9271926c99b508a8cd9827
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49400216"
---
# <a name="planning-for-public-instant-messaging-connectivity-in-lync-server-2013"></a><span data-ttu-id="6aaf1-103">Планирование подключения общедоступной службы обмена мгновенными сообщениями в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6aaf1-103">Planning for public instant messaging connectivity in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6aaf1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6aaf1-104">

<span> </span></span></span>

<span data-ttu-id="6aaf1-105">_**Тема последнего изменения:** 2013-10-07_</span><span class="sxs-lookup"><span data-stu-id="6aaf1-105">_**Topic Last Modified:** 2013-10-07_</span></span>

<span data-ttu-id="6aaf1-106">Общедоступная служба обмена мгновенными сообщениями является классом Федерации и настроена на разрешение внутренних и внешних пользователей Lync Server 2013 для добавления контактов из указанных ниже вариантов.</span><span class="sxs-lookup"><span data-stu-id="6aaf1-106">Public Instant Messaging Connectivity is a class of federation, and is configured to allow your internal and external Lync Server 2013 users to add contacts from any of the following:</span></span>

  - <span data-ttu-id="6aaf1-107">Контакты Messenger</span><span class="sxs-lookup"><span data-stu-id="6aaf1-107">Messenger contacts</span></span>

  - <span data-ttu-id="6aaf1-108">Yahoo\!</span><span class="sxs-lookup"><span data-stu-id="6aaf1-108">Yahoo\!</span></span> <span data-ttu-id="6aaf1-109">контакты,</span><span class="sxs-lookup"><span data-stu-id="6aaf1-109">contacts</span></span>

  - <span data-ttu-id="6aaf1-110">Контакты из Skype Online (AOL)</span><span class="sxs-lookup"><span data-stu-id="6aaf1-110">America Online (AOL) contacts</span></span>

<div>


> [!IMPORTANT]  
> <UL>
> <LI>
> <P><span data-ttu-id="6aaf1-111">За Сентябрь 1 сентября 2012 г. Лицензия на подписку на общедоступные пользователи Microsoft Lync (PIC USL) больше не доступна для приобретения новых или обновленных договоров.</span><span class="sxs-lookup"><span data-stu-id="6aaf1-111">As of September 1st, 2012, the Microsoft Lync Public IM Connectivity User Subscription License (PIC USL) is no longer available for the purchase for new or renewing agreements.</span></span> <span data-ttu-id="6aaf1-112">Пользователи с активными лицензиями смогут продолжать использовать федерацию с помощью Yahoo!</span><span class="sxs-lookup"><span data-stu-id="6aaf1-112">Customers with active licenses will be able to continue to federate with Yahoo!</span></span> <span data-ttu-id="6aaf1-113">Messenger, пока не зайдет Дата завершения обслуживания.</span><span class="sxs-lookup"><span data-stu-id="6aaf1-113">Messenger until the service shutdown date.</span></span> <span data-ttu-id="6aaf1-114">Дата окончания жизненного цикла 2014 для AOL и Yahoo! в течение июня.</span><span class="sxs-lookup"><span data-stu-id="6aaf1-114">An end of life date of June 2014 for AOL and Yahoo!</span></span> <span data-ttu-id="6aaf1-115">было объявлено.</span><span class="sxs-lookup"><span data-stu-id="6aaf1-115">has been announced.</span></span> <span data-ttu-id="6aaf1-116">Подробности можно найти <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">в разделе Поддержка общедоступной службы обмена мгновенными сообщениями в Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="6aaf1-116">For details, see <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Support for public instant messenger connectivity in Lync Server 2013</A>.</span></span></P>
> <LI>
> <P><span data-ttu-id="6aaf1-117">USL PIC является лицензией на подписку "на пользователя", которая требуется для использования Lync Server или Office Communications Server для Федерации с помощью Yahoo!</span><span class="sxs-lookup"><span data-stu-id="6aaf1-117">The PIC USL is a per-user, per-month subscription license that is required for Lync Server or Office Communications Server to federate with Yahoo!</span></span> <span data-ttu-id="6aaf1-118">Messenger.</span><span class="sxs-lookup"><span data-stu-id="6aaf1-118">Messenger.</span></span> <span data-ttu-id="6aaf1-119">Возможность предоставления этой услуги корпорацией Майкрософт зависит от поддержки компании Yahoo!, основного соглашения, для которого она не будет продлена.</span><span class="sxs-lookup"><span data-stu-id="6aaf1-119">Microsoft’s ability to provide this service has been contingent upon support from Yahoo!, the underlying agreement for which will not be renewed.</span></span></P>
> <LI>
> <P><span data-ttu-id="6aaf1-120">В некоторых случаях Lync — это мощный инструмент для связи между организациями и людьми по всему миру.</span><span class="sxs-lookup"><span data-stu-id="6aaf1-120">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="6aaf1-121">Для интеграции с Windows Live Messenger не требуется дополнительных лицензий на пользователей и устройств за пределами стандартной клиентской лицензии Lync.</span><span class="sxs-lookup"><span data-stu-id="6aaf1-121">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard CAL.</span></span> <span data-ttu-id="6aaf1-122">В этот список будет добавлена Федерация Skype, благодаря чему пользователи Lync смогут получать сотни миллионов людей с помощью голосовой почты и голосовых сообщений.</span><span class="sxs-lookup"><span data-stu-id="6aaf1-122">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people through IM and voice.</span></span></P></LI></UL>



</div>

<span data-ttu-id="6aaf1-123">Для этого класса Федерации требуются следующие вопросы планирования:</span><span class="sxs-lookup"><span data-stu-id="6aaf1-123">This class of federation requires the following planning considerations:</span></span>

  - <span data-ttu-id="6aaf1-124">Пользователи Windows Live Messenger могут иметь доступ к одноранговой голосовой и видеосвязи с пользователями Lync Server 2013, а также обмениваться мгновенными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="6aaf1-124">Windows Live Messenger users can have peer-to-peer audio/visual communication with Lync Server 2013 users, in addition to instant messaging.</span></span> <span data-ttu-id="6aaf1-125">Пограничные серверы должны соответствовать конкретным требованиям к порту и протоколу.</span><span class="sxs-lookup"><span data-stu-id="6aaf1-125">Your Edge Servers must meet specific port and protocol requirements.</span></span> <span data-ttu-id="6aaf1-126">Подробности можно найти [в разделе Определение внешних параметров брандмауэра/V и требований к портам для Lync Server 2013](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="6aaf1-126">For details, see [Determine external A/V firewall and port requirements for Lync Server 2013](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md).</span></span>

  - <span data-ttu-id="6aaf1-127">В обмене сообщениями Yahoo нет уникальных требований, кроме тех, которые обычно используются при планировании и развертывании типичного пограничного сервера, предоставляющего Федерацию.</span><span class="sxs-lookup"><span data-stu-id="6aaf1-127">Yahoo instant messaging has no unique requirements, other than those typically used in the planning and deployment of the typical Edge Server that is providing federation.</span></span>

  - <span data-ttu-id="6aaf1-128">Для использования Skype Online требуется, чтобы сертификат пограничного сервера, назначенный службе EDGE, использовал улучшенное использование ключа (EKU).</span><span class="sxs-lookup"><span data-stu-id="6aaf1-128">America Online requires that your Edge Server certificate assigned to the Access Edge service has a client enhanced key usage (EKU).</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="6aaf1-129">Содержание</span><span class="sxs-lookup"><span data-stu-id="6aaf1-129">In This Section</span></span>

  - [<span data-ttu-id="6aaf1-130">Сведения о сертификате: общедоступная служба обмена мгновенными сообщениями в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6aaf1-130">Certificate summary - Public instant messaging connectivity in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-public-instant-messaging-connectivity.md)

  - [<span data-ttu-id="6aaf1-131">Общие сведения о портах — общедоступная служба обмена мгновенными сообщениями в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6aaf1-131">Port summary - Public instant messaging connectivity in Lync Server 2013</span></span>](lync-server-2013-port-summary-public-instant-messaging-connectivity.md)

  - <span data-ttu-id="6aaf1-132">[Сводка DNS: подключение общедоступной службы обмена мгновенными сообщениями в Lync Server 2013](https://technet.microsoft.com/library/jj618375\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="6aaf1-132">[DNS summary - Public instant messaging connectivity in Lync Server 2013](https://technet.microsoft.com/library/jj618375\(v=ocs.15\))</span></span>

<span data-ttu-id="6aaf1-133"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6aaf1-133"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

