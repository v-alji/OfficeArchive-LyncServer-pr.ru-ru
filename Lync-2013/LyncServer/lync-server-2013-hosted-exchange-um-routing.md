---
title: 'Lync Server 2013: маршрутизация для размещенной единой системы обмена сообщениями'
description: 'Lync Server 2013: Маршрутизация размещенной единой системы обмена сообщениями в UM.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Hosted Exchange UM routing
ms:assetid: 6c90dc8b-6aef-4ce8-b483-37c7b5a553c2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398512(v=OCS.15)
ms:contentKeyID: 48184422
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 72fbdee5550ae53d5ff5e7513ea384cedad62c5a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427594"
---
# <a name="hosted-exchange-um-routing-in-lync-server-2013"></a><span data-ttu-id="882aa-103">Маршрутизация для размещенной единой системы обмена сообщениями в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="882aa-103">Hosted Exchange UM routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="882aa-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="882aa-104">

<span> </span></span></span>

<span data-ttu-id="882aa-105">_**Тема последнего изменения:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="882aa-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="882aa-106">Приложение маршрутизации UM Exchange запускается на сервере переднего плана для маршрутизации вызовов либо на развертывание локальной системы обмена сообщениями Microsoft Exchange Server (UM) или в размещенной службе Exchange UM.</span><span class="sxs-lookup"><span data-stu-id="882aa-106">The Exchange UM Routing application runs on the Front End Server to route calls, either to an on-premises Microsoft Exchange Server Unified Messaging (UM) deployment or to hosted Exchange UM service.</span></span>

<div>

## <a name="the-exum-routing-application"></a><span data-ttu-id="882aa-107">Приложение маршрутизации ExUM</span><span class="sxs-lookup"><span data-stu-id="882aa-107">The ExUM Routing Application</span></span>

<span data-ttu-id="882aa-108">Приложение Lync Server 2013 Exchange для маршрутизации UM использует данные из параметров учетной записи пользователя и из параметров политики размещенной голосовой почты, чтобы определить, как перенаправлять звонки на размещенные голосовые сообщения, как показано на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="882aa-108">The Lync Server 2013 Exchange UM Routing application uses information from user account settings and from hosted voice mail policy parameters to determine how to route calls for hosted voice messaging, as shown in the following diagram.</span></span>

<span data-ttu-id="882aa-109">**Пример маршрутизации единой системы обмена сообщениями Exchange для смешанного развертывания**</span><span class="sxs-lookup"><span data-stu-id="882aa-109">**Example of mixed deployment Exchange UM routing**</span></span>

<span data-ttu-id="882aa-110">![Развертывание локальной системы обмена сообщениями на сервере Lync Server](images/Gg398512.75258286-1f23-487b-bf46-d8538e7d540e(OCS.15).jpg "Развертывание локальной системы обмена сообщениями на сервере Lync Server")</span><span class="sxs-lookup"><span data-stu-id="882aa-110">![On-premises Lync Server Exchange UM deployment](images/Gg398512.75258286-1f23-487b-bf46-d8538e7d540e(OCS.15).jpg "On-premises Lync Server Exchange UM deployment")</span></span>

<span data-ttu-id="882aa-111">Маршрутизацию в UM-среде Exchange можно настроить так, чтобы она направляла звонки пользователям, которые поддерживают локальную систему обмена СООБЩЕНИЯми Exchange, пользователям, которые работают с размещенной единой системой обмена сообщениями, или сочетанием этих двух служб.</span><span class="sxs-lookup"><span data-stu-id="882aa-111">Exchange UM routing can be configured to route calls to users who are enabled for on-premises Exchange UM, to users who are enabled for hosted Exchange UM, or to a combination of the two.</span></span>

<span data-ttu-id="882aa-112">Например, предположим, что почтовый ящик Roy и служба Exchange UM размещены в локальной среде развертывания Exchange.</span><span class="sxs-lookup"><span data-stu-id="882aa-112">For example, suppose that Roy’s mailbox and Exchange UM service are homed in an on-premises Exchange deployment.</span></span>

  - <span data-ttu-id="882aa-113">Сведения об адресах прокси-сервера из учетной записи пользователя Roy предоставляют сведения, которые используются приложением Routing ExUM, чтобы перенаправлять свои звонки на локальный сервер единой системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="882aa-113">The proxy address information from Roy’s user account provides the information that the ExUM Routing application uses to route his calls to an on-premises Exchange UM server.</span></span>

<span data-ttu-id="882aa-114">Почтовый ящик Алисы и служба Exchange UM находятся в центре обработки данных размещенного поставщика услуг Exchange.</span><span class="sxs-lookup"><span data-stu-id="882aa-114">Alice’s mailbox and Exchange UM service are located at a hosted Exchange service provider’s data center.</span></span> <span data-ttu-id="882aa-115">Маршрутизация для входящих звонков UM происходит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="882aa-115">Routing for her Exchange UM calls is configured as follows:</span></span>

  - <span data-ttu-id="882aa-116">Значения, заданные в атрибуте msExchUCVoiceMailSettings учетной записи Алисы, говорят приложению Routing ExUM о необходимости поиска подробных сведений о маршрутизации в политике размещенной голосовой почты.</span><span class="sxs-lookup"><span data-stu-id="882aa-116">The values set in the msExchUCVoiceMailSettings attribute of Alice’s user account tell the ExUM Routing application to check for routing details in a hosted voice mail policy.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="882aa-117">Значение атрибута msExchUCVoiceMailSettings может быть задано поставщиком услуг Exchange или администратором Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="882aa-117">The value of the msExchUCVoiceMailSettings attribute can be set by either the Exchange service provider or the Lync Server 2013 administrator.</span></span> <span data-ttu-id="882aa-118">В примере, показанном на предыдущей схеме, значение (CsHostedVoiceMail = 1) было установлено администратором Lync Server 2013 для включения размещенной голосовой почты для Алисы.</span><span class="sxs-lookup"><span data-stu-id="882aa-118">In the example shown in the preceding diagram, the value (CsHostedVoiceMail=1) was set by the Lync Server 2013 administrator to enable hosted voice mail for Alice.</span></span> <span data-ttu-id="882aa-119">Подробнее об этом атрибуте можно узнать <A href="lync-server-2013-hosted-exchange-user-management.md">в разделе Управление пользователями Exchange в Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="882aa-119">For details about this attribute, see <A href="lync-server-2013-hosted-exchange-user-management.md">Hosted Exchange user management in Lync Server 2013</A>.</span></span>

    
    </div>

  - <span data-ttu-id="882aa-120">Политика размещенной голосовой почты, назначенная учетной записи пользователя Алисы, предоставляет сведения о маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="882aa-120">The hosted voice mail policy that is assigned to Alice’s user account provides routing details:</span></span>
    
      - <span data-ttu-id="882aa-121">Destination — это размещенный поставщик служб обмена почтовыми сообщениями (лат. ExUm. \<hostedExchangeServer\> . com в этом примере).</span><span class="sxs-lookup"><span data-stu-id="882aa-121">Destination is the hosted Exchange UM service provider (ls.ExUm.\<hostedExchangeServer\>.com in this example).</span></span>
    
      - <span data-ttu-id="882aa-122">Организации определяются с помощью идентификаторов клиентов, которые представляют собой полные доменные имена для сообщений SIP для клиентов Exchange Server, размещенных на Ls. ExUm. \<hostedExchangeServer\> . com (в этом примере — corp.contoso.com и corp.litwareinc.com).</span><span class="sxs-lookup"><span data-stu-id="882aa-122">Organizations are identified by the tenant IDs, which are the routing FQDNs for SIP messages for Exchange Server tenants that are located on ls.ExUm.\<hostedExchangeServer\>.com (corp.contoso.com and corp.litwareinc.com in this example).</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="882aa-123">Полное доменное имя Exchange Online — exap.um.outlook.com.</span><span class="sxs-lookup"><span data-stu-id="882aa-123">The FQDN for Exchange Online is exap.um.outlook.com.</span></span>

        
        </div>
        
        <span data-ttu-id="882aa-124">Подробнее смотрите в разделе [политики размещенной голосовой почты в Lync Server 2013](lync-server-2013-hosted-voice-mail-policies.md).</span><span class="sxs-lookup"><span data-stu-id="882aa-124">For details, see [Hosted voice mail policies in Lync Server 2013](lync-server-2013-hosted-voice-mail-policies.md).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="882aa-125">Если в учетной записи пользователя есть атрибут msExchUCVoiceMailSettings и параметры прокси-сервера UM, атрибут msExchUCVoiceMailSettings имеет приоритет.</span><span class="sxs-lookup"><span data-stu-id="882aa-125">If both the msExchUCVoiceMailSettings attribute and the UM proxy address settings are present in a user account, the msExchUCVoiceMailSettings attribute takes precedence.</span></span>



<span data-ttu-id="882aa-126"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="882aa-126"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

