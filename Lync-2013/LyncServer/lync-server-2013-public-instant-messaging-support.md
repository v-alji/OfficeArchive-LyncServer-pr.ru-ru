---
title: 'Lync Server 2013: поддержка общедоступных служб обмена мгновенными сообщениями'
description: 'Lync Server 2013: общедоступная поддержка обмена мгновенными сообщениями.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Public instant messaging support
ms:assetid: 1f45163b-52c6-4a78-b9c8-dfe3abe4e5eb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204732(v=OCS.15)
ms:contentKeyID: 48183582
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1e071e8b79be82d865a85a9488e48dd0a4264c7f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399079"
---
# <a name="public-instant-messaging-support-in-lync-server-2013"></a><span data-ttu-id="6d350-103">Поддержка общедоступных служб обмена мгновенными сообщениями в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6d350-103">Public instant messaging support in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6d350-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6d350-104">

<span> </span></span></span>

<span data-ttu-id="6d350-105">_**Тема последнего изменения:** 2013-10-07_</span><span class="sxs-lookup"><span data-stu-id="6d350-105">_**Topic Last Modified:** 2013-10-07_</span></span>

<span data-ttu-id="6d350-106">Lync Server 2013 поддерживает использование лицензированных общедоступных служб обмена мгновенными сообщениями, а также использование расширенных протоколов обмена сообщениями и присутствия (XMPP) для реализации специального типа Федерации, позволяющего серверу Lync доступ к настроенным партнерам домена XMPP с помощью клиента Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="6d350-106">Lync Server 2013 supports the use of licensed public instant messaging (IM) connectivity providers, as well as the use of eXtensible Messaging and Presence Protocol (XMPP) to implement a special type of federation that enables a Lync Server to access configured XMPP domain partners by using the Lync 2013 client.</span></span>

<div>

## <a name="public-im-connectivity-provider-support"></a><span data-ttu-id="6d350-107">Поддержка поставщика подключения к службе обмена мгновенными сообщениями</span><span class="sxs-lookup"><span data-stu-id="6d350-107">Public IM Connectivity Provider Support</span></span>

<span data-ttu-id="6d350-108">В настоящее время поддерживаются следующие партнеры по подключению к мгновенным сообщениям:</span><span class="sxs-lookup"><span data-stu-id="6d350-108">The currently supported public instant messaging connectivity partners are:</span></span>

  - <span data-ttu-id="6d350-109">America Online</span><span class="sxs-lookup"><span data-stu-id="6d350-109">America Online</span></span>

  - <span data-ttu-id="6d350-110">Windows Live</span><span class="sxs-lookup"><span data-stu-id="6d350-110">Windows Live</span></span>

  - <span data-ttu-id="6d350-111">Yahoo\!</span><span class="sxs-lookup"><span data-stu-id="6d350-111">Yahoo\!</span></span>

<span data-ttu-id="6d350-112">Для связи с пользователями Windows Live Lync Server 2013 поддерживает обмен мгновенными сообщениями, голосовые и видеозвонки в одноранговой сети.</span><span class="sxs-lookup"><span data-stu-id="6d350-112">For communications with Windows Live users, Lync Server 2013 supports peer-to-peer IM and audio and video calls.</span></span> <span data-ttu-id="6d350-113">Для связи с AOL и Yahoo в \! Lync Server 2013 поддерживается одноранговый обмен мгновенными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="6d350-113">For communications with AOL and Yahoo\!, Lync Server 2013 supports peer-to-peer IM.</span></span> <span data-ttu-id="6d350-114">Может потребоваться отдельная лицензия.</span><span class="sxs-lookup"><span data-stu-id="6d350-114">A separate license may be required.</span></span>

<div>


> [!IMPORTANT]  
> <UL>
> <LI>
> <P><span data-ttu-id="6d350-115">По состоянию на 1 сентября 2012, лицензия на подписку на общедоступные службы обмена мгновенными сообщениями в Microsoft Lync ("PIC USL") больше недоступна для приобретения новых или обновленных договоров.</span><span class="sxs-lookup"><span data-stu-id="6d350-115">As of September 1st, 2012, the Microsoft Lync Public IM Connectivity User Subscription License (“PIC USL”) is no longer available for purchase for new or renewing agreements.</span></span> <span data-ttu-id="6d350-116">Пользователи с активными лицензиями смогут продолжать использовать федерацию с помощью Yahoo!</span><span class="sxs-lookup"><span data-stu-id="6d350-116">Customers with active licenses will be able to continue to federate with Yahoo!</span></span> <span data-ttu-id="6d350-117">Messenger, пока служба не отключается.</span><span class="sxs-lookup"><span data-stu-id="6d350-117">Messenger until the service shut down date.</span></span> <span data-ttu-id="6d350-118">Дата окончания жизненного цикла 2014 для AOL и Yahoo! в течение июня.</span><span class="sxs-lookup"><span data-stu-id="6d350-118">An end of life date of June 2014 for AOL and Yahoo!</span></span> <span data-ttu-id="6d350-119">было объявлено.</span><span class="sxs-lookup"><span data-stu-id="6d350-119">has been announced.</span></span> <span data-ttu-id="6d350-120">Подробности можно найти <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">в разделе Поддержка общедоступной службы обмена мгновенными сообщениями в Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="6d350-120">For details, see <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Support for public instant messenger connectivity in Lync Server 2013</A>.</span></span></P>
> <LI>
> <P><span data-ttu-id="6d350-121">USL PIC является лицензией на ежемесячную подписку для пользователей Lync Server или Office Communications Server, которая требуется для Федерации с помощью Yahoo!.</span><span class="sxs-lookup"><span data-stu-id="6d350-121">The PIC USL is a per-user per-month subscription license that is required for Lync Server or Office Communications Server to federate with Yahoo!</span></span> <span data-ttu-id="6d350-122">Messenger.</span><span class="sxs-lookup"><span data-stu-id="6d350-122">Messenger.</span></span> <span data-ttu-id="6d350-123">Возможность предоставления этой услуги корпорацией Майкрософт зависит от поддержки компании Yahoo!, основного соглашения, для которого выполняется обмотка.</span><span class="sxs-lookup"><span data-stu-id="6d350-123">Microsoft’s ability to provide this service has been contingent upon support from Yahoo!, the underlying agreement for which is winding down.</span></span></P>
> <LI>
> <P><span data-ttu-id="6d350-124">В некоторых случаях Lync — это мощный инструмент для связи между организациями и людьми по всему миру.</span><span class="sxs-lookup"><span data-stu-id="6d350-124">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="6d350-125">Для интеграции с Windows Live Messenger не требуется дополнительных лицензий на пользователей и устройств за пределами стандартной клиентской лицензии Lync.</span><span class="sxs-lookup"><span data-stu-id="6d350-125">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard CAL.</span></span> <span data-ttu-id="6d350-126">В этот список будет добавлена Федерация Skype, благодаря чему пользователи Lync смогут общаться с сотнями миллионов людей с помощью обмена мгновенными сообщениями и голосовой связью.</span><span class="sxs-lookup"><span data-stu-id="6d350-126">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people with IM and voice.</span></span></P></LI></UL>



</div>

</div>

<div>

## <a name="xmpp-federation-support"></a><span data-ttu-id="6d350-127">Поддержка Федерации XMPP</span><span class="sxs-lookup"><span data-stu-id="6d350-127">XMPP Federation Support</span></span>

<span data-ttu-id="6d350-128">XMPP Федерация поддерживает взаимодействие пользователей Lync с настроенными пользователями домена XMPP, которые используют общедоступный поставщик, например GTalk.</span><span class="sxs-lookup"><span data-stu-id="6d350-128">XMPP federation supports Lync users communication with configured XMPP domain users who use a public provider, such as GTalk.</span></span> <span data-ttu-id="6d350-129">Связь с этими пользователями может включать в себя следующее:</span><span class="sxs-lookup"><span data-stu-id="6d350-129">Communications with these users can include the following:</span></span>

  - <span data-ttu-id="6d350-130">Обмен мгновенными сообщениями и присутствием одноранговой сети</span><span class="sxs-lookup"><span data-stu-id="6d350-130">Peer-to-peer IM and presence</span></span>

  - <span data-ttu-id="6d350-131">Создание федеративных контактов XMPP в клиенте Lync</span><span class="sxs-lookup"><span data-stu-id="6d350-131">Creation of XMPP federated contacts in the Lync client</span></span>

<span data-ttu-id="6d350-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6d350-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

