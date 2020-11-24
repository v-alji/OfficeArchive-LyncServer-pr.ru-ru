---
title: 'Lync Server 2013: компоненты и топологии для локальной единой системы обмена сообщениями'
description: 'Lync Server 2013: компоненты и топологии для локальной единой системы обмена сообщениями.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Components and topologies for on-premises Unified Messaging
ms:assetid: 22fc87cf-a7e5-4c8c-bb9b-101e5380cdcf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425711(v=OCS.15)
ms:contentKeyID: 48183619
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8fe2ca16ec9fbd39e9245fd366e1f7046dd16d42
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398545"
---
# <a name="components-and-topologies-for-on-premises-unified-messaging-in-lync-server-2013"></a><span data-ttu-id="434a6-103">Компоненты и топологии для локальной единой системы обмена сообщениями в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="434a6-103">Components and topologies for on-premises Unified Messaging in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="434a6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="434a6-104">

<span> </span></span></span>

<span data-ttu-id="434a6-105">_**Тема последнего изменения:** 2012-09-25_</span><span class="sxs-lookup"><span data-stu-id="434a6-105">_**Topic Last Modified:** 2012-09-25_</span></span>

<span data-ttu-id="434a6-106">В этом разделе описаны компоненты Microsoft Exchange Server 2013, необходимые для обеспечения функций единой системы обмена сообщениями Exchange (UM) для развертывания Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="434a6-106">This topic describes the Microsoft Exchange Server 2013 components required to provide Exchange Unified Messaging (UM) features to Lync Server 2013 deployment.</span></span> <span data-ttu-id="434a6-107">Кроме того, здесь описаны поддерживаемые топологии для локальной интеграции единой системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="434a6-107">It also describes the supported topologies for on-premises Exchange UM integration.</span></span>

<div>

## <a name="exchange-server-components"></a><span data-ttu-id="434a6-108">Компоненты Exchange Server</span><span class="sxs-lookup"><span data-stu-id="434a6-108">Exchange Server Components</span></span>

<span data-ttu-id="434a6-109">Для предоставления функций и служб Exchange UM, описанных в [функциях интеграции единой системы обмена сообщениями и Lync Server 2013](lync-server-2013-features-of-integrated-unified-messaging.md) и корпоративной голосовой связи в Организации, необходимо развернуть сервер почтовых ящиков Microsoft Exchange и сервер клиентского доступа, на котором размещаются почтовые ящики пользователей и есть единое место для хранения электронной почты и голосовой почты.</span><span class="sxs-lookup"><span data-stu-id="434a6-109">To provide the Exchange UM features and services described in [Features of integrated Unified Messaging and Lync Server 2013](lync-server-2013-features-of-integrated-unified-messaging.md) to Enterprise Voice users in your organization, you must deploy an Microsoft Exchange Mailbox server and Client Access server, which hosts user mailboxes and provides a single storage location for email and voice mail.</span></span> <span data-ttu-id="434a6-110">UM Exchange работает как служба на почтовом ящике Exchange и серверах клиентского доступа.</span><span class="sxs-lookup"><span data-stu-id="434a6-110">Exchange UM runs as a service on Exchange Mailbox and Client Access servers.</span></span>

<span data-ttu-id="434a6-111">Дополнительные сведения о компонентах UM Exchange в Microsoft Exchange Server 2007 и Microsoft Exchange Server 2010 можно найти в разделе [развертывание локальной системы обмена сообщениями Exchange для предоставления голосовой почты Lync Server 2013](lync-server-2013-deploying-on-premises-exchange-um-to-provide-lync-server-2013-voice-mail.md) в документации по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="434a6-111">For details about Exchange UM components in Microsoft Exchange Server 2007 and Microsoft Exchange Server 2010, see [Deploying on-premises Exchange UM to provide Lync Server 2013 voice mail](lync-server-2013-deploying-on-premises-exchange-um-to-provide-lync-server-2013-voice-mail.md) in the Deployment documentation.</span></span>

</div>

<div>

## <a name="supported-topologies"></a><span data-ttu-id="434a6-112">Поддерживаемые топологии</span><span class="sxs-lookup"><span data-stu-id="434a6-112">Supported Topologies</span></span>

<span data-ttu-id="434a6-113">Вы можете развернуть Lync Server 2013 и единую систему обмена сообщениями Exchange (UM) в одном лесе или нескольких лесах.</span><span class="sxs-lookup"><span data-stu-id="434a6-113">You can deploy Lync Server 2013 and Exchange Unified Messaging (UM) in the same forest or multiple forests.</span></span> <span data-ttu-id="434a6-114">Если развертывание охватывает несколько лесов, необходимо выполнить шаги интеграции Exchange для каждого леса UM Exchange.</span><span class="sxs-lookup"><span data-stu-id="434a6-114">If the deployment spans multiple forests, you must perform the Exchange integration steps for each Exchange UM forest.</span></span> <span data-ttu-id="434a6-115">Кроме того, необходимо настроить каждый лес Microsoft Exchange для доверительных отношений с лесом Lync Server 2013 и лесом сервера Lync Server 2013 для доверительных отношений между каждым лесом Exchange UM.</span><span class="sxs-lookup"><span data-stu-id="434a6-115">Furthermore, you must configure each Microsoft Exchange forest to trust the Lync Server 2013 forest and the Lync Server 2013 forest to trust each Exchange UM forest.</span></span> <span data-ttu-id="434a6-116">В дополнение к этому доверию лесов параметры Exchange UM для всех пользователей должны быть установлены на объектах пользователей в лесу Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="434a6-116">In addition to this forest trust, the Exchange UM settings for all users must be set on the user objects in the Lync Server 2013 forest.</span></span>

<span data-ttu-id="434a6-117">Lync Server 2013 поддерживает следующие топологии интеграции Exchange UM.</span><span class="sxs-lookup"><span data-stu-id="434a6-117">Lync Server 2013 supports the following topologies for Exchange UM integration:</span></span>

  - <span data-ttu-id="434a6-118">Один лес</span><span class="sxs-lookup"><span data-stu-id="434a6-118">Single forest</span></span>

  - <span data-ttu-id="434a6-119">Один домен (то есть один лес с одним доменом).</span><span class="sxs-lookup"><span data-stu-id="434a6-119">Single domain (that is, a single forest with a single domain).</span></span> <span data-ttu-id="434a6-120">Lync Server 2013, Microsoft Exchange и пользователи находятся в одном домене.</span><span class="sxs-lookup"><span data-stu-id="434a6-120">Lync Server 2013, Microsoft Exchange, and users all reside in the same domain.</span></span>

  - <span data-ttu-id="434a6-121">Multiple domain (that is, a root domain with one or more child domains).</span><span class="sxs-lookup"><span data-stu-id="434a6-121">Multiple domain (that is, a root domain with one or more child domains).</span></span> <span data-ttu-id="434a6-122">Сервер Lync Server 2013 и серверы Microsoft Exchange развертываются в разных доменах из домена, где создаются пользователи.</span><span class="sxs-lookup"><span data-stu-id="434a6-122">Lync Server 2013, and Microsoft Exchange servers are deployed in different domains from the domain where you create users.</span></span> <span data-ttu-id="434a6-123">Серверы Exchange UM можно разворачивать в разных доменах из пула Lync Server 2013, который они поддерживают.</span><span class="sxs-lookup"><span data-stu-id="434a6-123">Exchange UM servers can be deployed in different domains from the Lync Server 2013 pool they support.</span></span>

  - <span data-ttu-id="434a6-124">Несколько лесов (то есть лес ресурсов).</span><span class="sxs-lookup"><span data-stu-id="434a6-124">Multiple forest (that is, resource forest).</span></span> <span data-ttu-id="434a6-125">Lync Server 2013 развернут в одном лесе, и пользователи распределены по нескольким лесам.</span><span class="sxs-lookup"><span data-stu-id="434a6-125">Lync Server 2013 is deployed in a single forest, and then users are distributed across multiple forests.</span></span> <span data-ttu-id="434a6-126">Атрибуты среды обмена UM для пользователей должны быть реплицированы в лес 2013 для Lync Server.</span><span class="sxs-lookup"><span data-stu-id="434a6-126">The users’ Exchange UM attributes must be replicated over to the Lync Server 2013 forest.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="434a6-127">Exchange can be deployed in multiple forests.</span><span class="sxs-lookup"><span data-stu-id="434a6-127">Exchange can be deployed in multiple forests.</span></span> <span data-ttu-id="434a6-128">Каждая организация Exchange может предоставлять своим пользователям обмен UM, а Exchange UM может быть развернут в том же лесе, что и Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="434a6-128">Each Exchange organization can provide Exchange UM to its users, or Exchange UM can be deployed in the same forest as Lync Server 2013.</span></span>

    
    <span data-ttu-id="434a6-129"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="434a6-129"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

