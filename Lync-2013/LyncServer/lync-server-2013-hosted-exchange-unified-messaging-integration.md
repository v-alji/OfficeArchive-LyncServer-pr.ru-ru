---
title: 'Lync Server 2013: интеграция с размещенной единой системой обмена сообщениями Exchange'
description: 'Lync Server 2013: размещена интеграция единой системы обмена сообщениями Exchange.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Hosted Exchange Unified Messaging integration
ms:assetid: f4de0165-da3b-499e-98fc-28ddd0db02d5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413027(v=OCS.15)
ms:contentKeyID: 48185829
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 980c0bc47258e9fae94ff623559342ca36eea145
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427532"
---
# <a name="hosted-exchange-unified-messaging-integration-in-lync-server-2013"></a><span data-ttu-id="27ab5-103">Интеграция с размещенной единой системой обмена сообщениями Exchange в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="27ab5-103">Hosted Exchange Unified Messaging integration in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="27ab5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="27ab5-104">

<span> </span></span></span>

<span data-ttu-id="27ab5-105">_**Тема последнего изменения:** 2012-09-20_</span><span class="sxs-lookup"><span data-stu-id="27ab5-105">_**Topic Last Modified:** 2012-09-20_</span></span>

<span data-ttu-id="27ab5-106">Помимо поддержки предыдущих выпусков Lync Server 2013 для интеграции с *локальными* развертываниями единой системы обмена сообщениями Exchange (UM), Lync Server 2013 обеспечивает поддержку интеграции с *размещенной* UM-средой Exchange.</span><span class="sxs-lookup"><span data-stu-id="27ab5-106">In addition to the support that previous Lync Server 2013 releases have provided for integration with *on-premises* deployments of Exchange Unified Messaging (UM), Lync Server 2013 introduces support for integration with *hosted* Exchange UM.</span></span> <span data-ttu-id="27ab5-107">Размещенная UM-служба Exchange позволяет Lync Server 2013 предоставлять пользователям голосовую почту, если вы переносите их на размещенный поставщик услуг Exchange, например Microsoft Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="27ab5-107">Hosted Exchange UM enables Lync Server 2013 to provide voice messaging to your users if you transfer some or all of them to a hosted Exchange service provider such as Microsoft Exchange Online.</span></span>

<span data-ttu-id="27ab5-108">Lync Server 2013 Enterprise Voice использует инфраструктуру UM Exchange для обеспечения ответа на звонки, уведомления о звонках, доступа к голосовой почте (в том числе голосовой почты) и служб автоматического ассистента.</span><span class="sxs-lookup"><span data-stu-id="27ab5-108">Lync Server 2013 Enterprise Voice uses the Exchange UM infrastructure to provide call answering, call notification, voice access (including voice mail), and auto attendant services.</span></span> <span data-ttu-id="27ab5-109">Подробные сведения можно найти в разделе [функции интегрированной единой системы обмена сообщениями и Lync Server 2013](lync-server-2013-features-of-integrated-unified-messaging.md).</span><span class="sxs-lookup"><span data-stu-id="27ab5-109">For details, see [Features of integrated Unified Messaging and Lync Server 2013](lync-server-2013-features-of-integrated-unified-messaging.md).</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="27ab5-110">Содержание</span><span class="sxs-lookup"><span data-stu-id="27ab5-110">In This Section</span></span>

  - [<span data-ttu-id="27ab5-111">Архитектура и маршрутизация для размещенной единой системы обмена сообщениями Exchange в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="27ab5-111">Hosted Exchange UM architecture and routing in Lync Server 2013</span></span>](lync-server-2013-hosted-exchange-um-architecture-and-routing.md)

  - [<span data-ttu-id="27ab5-112">Политики размещенной голосовой почты в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="27ab5-112">Hosted voice mail policies in Lync Server 2013</span></span>](lync-server-2013-hosted-voice-mail-policies.md)

  - [<span data-ttu-id="27ab5-113">Управление пользователями размещенной системы Exchange в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="27ab5-113">Hosted Exchange user management in Lync Server 2013</span></span>](lync-server-2013-hosted-exchange-user-management.md)

  - [<span data-ttu-id="27ab5-114">Управление объектом Contact в размещенной системе Exchange в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="27ab5-114">Hosted Exchange Contact object management in Lync Server 2013</span></span>](lync-server-2013-hosted-exchange-contact-object-management.md)

  - [<span data-ttu-id="27ab5-115">Процесс развертывания для интеграции размещенной единой системы обмена сообщениями Exchange с Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="27ab5-115">Deployment process for integrating hosted Exchange UM with Lync Server 2013</span></span>](lync-server-2013-deployment-process-for-integrating-hosted-exchange-um.md)

<span data-ttu-id="27ab5-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="27ab5-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

