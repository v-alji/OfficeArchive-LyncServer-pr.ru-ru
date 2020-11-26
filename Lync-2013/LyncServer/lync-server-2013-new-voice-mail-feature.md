---
title: 'Lync Server 2013: новая функция голосовой почты'
description: 'Lync Server 2013: новая функция голосовой почты.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: New voice mail feature
ms:assetid: 84d13238-67ef-42cc-801a-2d8147ba3b7f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688117(v=OCS.15)
ms:contentKeyID: 49733715
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: aa4d963d3cdcb50f6195184218c07dfd98032b33
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445318"
---
# <a name="new-voice-mail-feature-in-lync-server-2013"></a><span data-ttu-id="3e061-103">Новая функция голосовой почты в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3e061-103">New voice mail feature in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3e061-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3e061-104">

<span> </span></span></span>

<span data-ttu-id="3e061-105">_**Тема последнего изменения:** 2012-10-05_</span><span class="sxs-lookup"><span data-stu-id="3e061-105">_**Topic Last Modified:** 2012-10-05_</span></span>

<span data-ttu-id="3e061-106">Lync Server 2013 представляет голосовую почту, а именно улучшенные возможности управления голосовой почтой.</span><span class="sxs-lookup"><span data-stu-id="3e061-106">Lync Server 2013 introduces Voice mail Escape, an enhancement for managing voice mail.</span></span> <span data-ttu-id="3e061-107">Эта новая функция может определять, когда звонок направляется на голосовую почту, и предотвращает немедленное перенаправление звонка на голосовую почту пользователя, не предоставляя пользователю возможность ответить на звонок.</span><span class="sxs-lookup"><span data-stu-id="3e061-107">This new feature can detect when a call has been routed to voice mail, and prevent the call from being immediately routed to the user’s mobile phone voice mail without giving the user the opportunity to answer the call.</span></span> <span data-ttu-id="3e061-108">Это происходит, когда пользователь включает Одновременный звонок на мобильный телефон, а его мобильный телефон выключен, выходит за пределы батареи или выходит за пределы диапазона.</span><span class="sxs-lookup"><span data-stu-id="3e061-108">This scenario occurs when the user enables simultaneous ringing to their mobile phone, and their mobile phone is turned off, out of battery, or out of range.</span></span> <span data-ttu-id="3e061-109">Управляющая Голосовая почта обнаруживает, что звонок немедленно отвечал на голосовую почту пользователя, и отсоединяет Звонок на голосовую почту мобильного телефона.</span><span class="sxs-lookup"><span data-stu-id="3e061-109">Voicemail Escape detects that the call was immediately answered by the user’s mobile phone voice mail, and disconnects the call to the mobile phone voice mail.</span></span> <span data-ttu-id="3e061-110">Звонок продолжает звонить по другим конечным точкам пользователя, предоставляя пользователю возможность ответить на звонок.</span><span class="sxs-lookup"><span data-stu-id="3e061-110">The call continues to ring on the user’s other endpoints giving the user the opportunity to answer the call.</span></span> <span data-ttu-id="3e061-111">Если пользователь не отвечает на звонок, Звонок направляется в корпоративную голосовую почту.</span><span class="sxs-lookup"><span data-stu-id="3e061-111">If the user does not answer the call, then the call is routed to the corporate voice mail.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="3e061-112">См. также</span><span class="sxs-lookup"><span data-stu-id="3e061-112">See Also</span></span>


[<span data-ttu-id="3e061-113">Настройка escape-последовательности голосовой почты в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3e061-113">Configuring voice mail escape in Lync Server 2013</span></span>](lync-server-2013-configuring-voice-mail-escape.md)  


[<span data-ttu-id="3e061-114">Новые возможности корпоративной голосовой связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3e061-114">New Enterprise Voice features in Lync Server 2013</span></span>](lync-server-2013-new-enterprise-voice-features.md)  
  

<span data-ttu-id="3e061-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3e061-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

