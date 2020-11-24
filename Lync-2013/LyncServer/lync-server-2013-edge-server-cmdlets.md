---
title: 'Lync Server 2013: командлеты пограничного сервера'
description: 'Lync Server 2013: командлеты пограничного сервера.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Edge Server cmdlets
ms:assetid: 1a5427f4-a0d1-4652-8135-91333158ffc8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg415635(v=OCS.15)
ms:contentKeyID: 48183534
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4b73172331ddcde76672cccda682669f71dd7262
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49397897"
---
# <a name="edge-server-cmdlets-in-lync-server-2013"></a><span data-ttu-id="92784-103">Командлеты пограничного сервера в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="92784-103">Edge Server cmdlets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="92784-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="92784-104">

<span> </span></span></span>

<span data-ttu-id="92784-105">_**Тема последнего изменения:** 2013-10-07_</span><span class="sxs-lookup"><span data-stu-id="92784-105">_**Topic Last Modified:** 2013-10-07_</span></span>

<span data-ttu-id="92784-106">Пограничные серверы предоставляют способ продления возможностей Microsoft Lync Server 2013 для пользователей, не вошедших в внутреннюю сеть.</span><span class="sxs-lookup"><span data-stu-id="92784-106">Edge Servers provide a way for you to extend the capabilities of Microsoft Lync Server 2013 to people who are not logged on to your internal network.</span></span> <span data-ttu-id="92784-107">Например, если у вас есть удаленные пользователи, прошедшие проверку подлинности, которые входят в состав сервера Lync Server 2013 через Интернет, а не через внутреннюю сеть, вам потребуется настроить пограничный сервер, на котором запущена служба Edge Access для доступа к Lync Server.</span><span class="sxs-lookup"><span data-stu-id="92784-107">For example, if you have remote users -- authenticated users who log on to Lync Server 2013 over the Internet rather than through the internal network -- you will need to set up an Edge Server that runs the Lync Server Access Edge service.</span></span> <span data-ttu-id="92784-108">Кроме того, пограничные серверы требуются, если вы хотите установить Федерацию с другой организацией или вы хотите предоставить пользователям право общаться с людьми, у которых есть учетные записи с помощью общедоступной службы обмена мгновенными сообщениями, например Yahoo \! , AOL или MSN.</span><span class="sxs-lookup"><span data-stu-id="92784-108">Additionally, Edge Servers are required if you want to establish federation with another organization or if you want to give your users the right to communicate with people who have accounts with a public instant messaging service such as Yahoo\!, AOL, or MSN.</span></span>

<div>


> [!IMPORTANT]
> <UL>
> <LI>
> <P><span data-ttu-id="92784-109">По состоянию на 1 сентября 2012, лицензия на подписку на общедоступные службы обмена мгновенными сообщениями в Microsoft Lync ("PIC USL") больше недоступна для приобретения новых или обновленных договоров.</span><span class="sxs-lookup"><span data-stu-id="92784-109">As of September 1st, 2012, the Microsoft Lync Public IM Connectivity User Subscription License (“PIC USL”) is no longer available for purchase for new or renewing agreements.</span></span> <span data-ttu-id="92784-110">Пользователи с активными лицензиями смогут продолжать использовать федерацию с помощью Yahoo!</span><span class="sxs-lookup"><span data-stu-id="92784-110">Customers with active licenses will be able to continue to federate with Yahoo!</span></span> <span data-ttu-id="92784-111">Messenger, пока служба не отключается.</span><span class="sxs-lookup"><span data-stu-id="92784-111">Messenger until the service shut down date.</span></span> <span data-ttu-id="92784-112">Дата окончания жизненного цикла 2014 для AOL и Yahoo! в течение июня.</span><span class="sxs-lookup"><span data-stu-id="92784-112">An end of life date of June 2014 for AOL and Yahoo!</span></span> <span data-ttu-id="92784-113">было объявлено.</span><span class="sxs-lookup"><span data-stu-id="92784-113">has been announced.</span></span> <span data-ttu-id="92784-114">Подробности можно найти <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">в разделе Поддержка общедоступной службы обмена мгновенными сообщениями в Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="92784-114">For details, see <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Support for public instant messenger connectivity in Lync Server 2013</A>.</span></span></P>
> <LI>
> <P><span data-ttu-id="92784-115">USL PIC является лицензией на ежемесячную подписку для пользователей Lync Server или Office Communications Server, которая требуется для Федерации с помощью Yahoo!.</span><span class="sxs-lookup"><span data-stu-id="92784-115">The PIC USL is a per-user per-month subscription license that is required for Lync Server or Office Communications Server to federate with Yahoo!</span></span> <span data-ttu-id="92784-116">Messenger.</span><span class="sxs-lookup"><span data-stu-id="92784-116">Messenger.</span></span> <span data-ttu-id="92784-117">Возможность предоставления этой услуги корпорацией Майкрософт зависит от поддержки компании Yahoo!, основного соглашения, для которого выполняется обмотка.</span><span class="sxs-lookup"><span data-stu-id="92784-117">Microsoft’s ability to provide this service has been contingent upon support from Yahoo!, the underlying agreement for which is winding down.</span></span></P>
> <LI>
> <P><span data-ttu-id="92784-118">В некоторых случаях Lync — это мощный инструмент для связи между организациями и людьми по всему миру.</span><span class="sxs-lookup"><span data-stu-id="92784-118">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="92784-119">Для интеграции с Windows Live Messenger не требуется дополнительных лицензий на пользователей и устройств за пределами стандартной клиентской лицензии Lync.</span><span class="sxs-lookup"><span data-stu-id="92784-119">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard CAL.</span></span> <span data-ttu-id="92784-120">В этот список будет добавлена Федерация Skype, благодаря чему пользователи Lync смогут общаться с сотнями миллионов людей с помощью обмена мгновенными сообщениями и голосовой связью.</span><span class="sxs-lookup"><span data-stu-id="92784-120">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people with IM and voice.</span></span></P></LI></UL>



</div>

<div>

## <a name="edge-server-cmdlets"></a><span data-ttu-id="92784-121">Командлеты пограничного сервера</span><span class="sxs-lookup"><span data-stu-id="92784-121">Edge Server Cmdlets</span></span>

<span data-ttu-id="92784-122">Ниже приведен список командлетов, которые непосредственно относятся к управлению пограничными серверами.</span><span class="sxs-lookup"><span data-stu-id="92784-122">The following is a list of cmdlets that relate directly to managing Edge Servers:</span></span>

<span data-ttu-id="92784-123">**Пограничный сервер**</span><span class="sxs-lookup"><span data-stu-id="92784-123">**Edge Server**</span></span>

  - <span></span>  
    <span data-ttu-id="92784-124">[Get-CsAccessEdgeConfiguration](https://technet.microsoft.com/library/Gg398574(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="92784-124">[Get-CsAccessEdgeConfiguration](https://technet.microsoft.com/library/Gg398574(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="92784-125">[Set-CsAccessEdgeConfiguration](https://technet.microsoft.com/library/Gg413017(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="92784-125">[Set-CsAccessEdgeConfiguration](https://technet.microsoft.com/library/Gg413017(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="92784-126">[Get-CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg413008(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="92784-126">[Get-CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg413008(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="92784-127">[New-CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg412884(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="92784-127">[New-CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg412884(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="92784-128">[Remove-CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg398786(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="92784-128">[Remove-CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg398786(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="92784-129">[Set-CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg412869(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="92784-129">[Set-CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg412869(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="92784-130">[Test-CsAVEdgeConnectivity](https://technet.microsoft.com/library/JJ205138(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="92784-130">[Test-CsAVEdgeConnectivity](https://technet.microsoft.com/library/JJ205138(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="92784-131">[Set-CsEdgeServer](https://technet.microsoft.com/library/Gg398859(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="92784-131">[Set-CsEdgeServer](https://technet.microsoft.com/library/Gg398859(v=OCS.15))</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="92784-132">См. также</span><span class="sxs-lookup"><span data-stu-id="92784-132">See Also</span></span>


[<span data-ttu-id="92784-133">Блог Lync Server PowerShell</span><span class="sxs-lookup"><span data-stu-id="92784-133">Lync Server PowerShell Blog</span></span>](https://go.microsoft.com/fwlink/p/?linkid=203150)  
  

<span data-ttu-id="92784-134"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="92784-134"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

