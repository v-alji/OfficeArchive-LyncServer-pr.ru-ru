---
title: 'Lync Server 2013: командлеты приложения для приостановки вызова'
description: 'Lync Server 2013: командлеты приложения для приостановки вызова.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Call Park application cmdlets
ms:assetid: 30cc001f-b29e-4d44-bad7-65e1133e67b1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg415639(v=OCS.15)
ms:contentKeyID: 48183764
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 25d37e8cfad022e9e8478e68f158e1838bdcca5b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435721"
---
# <a name="call-park-application-cmdlets-in-lync-server-2013"></a><span data-ttu-id="30715-103">Командлеты приложения для приостановки звонков в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="30715-103">Call Park application cmdlets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="30715-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="30715-104">

<span> </span></span></span>

<span data-ttu-id="30715-105">_**Тема последнего изменения:** 2012-03-21_</span><span class="sxs-lookup"><span data-stu-id="30715-105">_**Topic Last Modified:** 2012-03-21_</span></span>

<span data-ttu-id="30715-106">Приложение "Приостановка звонка" позволяет пользователю помещать Звонок на удержание и получать этот звонок с другого телефона.</span><span class="sxs-lookup"><span data-stu-id="30715-106">Call Park application allows a user to place a call on hold, then retrieve that call from a different phone.</span></span> <span data-ttu-id="30715-107">Используйте эти командлеты, чтобы настроить параметры для орбиты и приложения для приостановки звонков.</span><span class="sxs-lookup"><span data-stu-id="30715-107">Use these cmdlets to configure settings for call park orbits and the Call Park application.</span></span>

<div>

## <a name="call-park-application-cmdlets"></a><span data-ttu-id="30715-108">Командлеты приложения для приостановки звонков</span><span class="sxs-lookup"><span data-stu-id="30715-108">Call Park Application Cmdlets</span></span>

<span data-ttu-id="30715-109">Для управления приложением на приостановке звонков можно использовать следующие командлеты.</span><span class="sxs-lookup"><span data-stu-id="30715-109">The following cmdlets can be used to manage Call Park application.</span></span>

<span data-ttu-id="30715-110">**Приложение для приостановки звонков**</span><span class="sxs-lookup"><span data-stu-id="30715-110">**Call Park Application**</span></span>

  - <span></span>  
    <span data-ttu-id="30715-111">[Get-CsCallParkOrbit](https://technet.microsoft.com/library/Gg398554(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="30715-111">[Get-CsCallParkOrbit](https://technet.microsoft.com/library/Gg398554(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="30715-112">[New-CsCallParkOrbit](https://technet.microsoft.com/library/Gg398936(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="30715-112">[New-CsCallParkOrbit](https://technet.microsoft.com/library/Gg398936(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="30715-113">[Remove-CsCallParkOrbit](https://technet.microsoft.com/library/Gg412901(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="30715-113">[Remove-CsCallParkOrbit](https://technet.microsoft.com/library/Gg412901(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="30715-114">[Set-CsCallParkOrbit](https://technet.microsoft.com/library/Gg398796(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="30715-114">[Set-CsCallParkOrbit](https://technet.microsoft.com/library/Gg398796(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="30715-115">[Set-CsCallParkServiceMusicOnHoldFile](https://technet.microsoft.com/library/Gg412836(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="30715-115">[Set-CsCallParkServiceMusicOnHoldFile](https://technet.microsoft.com/library/Gg412836(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="30715-116">[Get-CsCpsConfiguration](https://technet.microsoft.com/library/Gg398948(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="30715-116">[Get-CsCpsConfiguration](https://technet.microsoft.com/library/Gg398948(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="30715-117">[New-CsCpsConfiguration](https://technet.microsoft.com/library/Gg412919(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="30715-117">[New-CsCpsConfiguration](https://technet.microsoft.com/library/Gg412919(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="30715-118">[Remove-CsCpsConfiguration](https://technet.microsoft.com/library/Gg398358(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="30715-118">[Remove-CsCpsConfiguration](https://technet.microsoft.com/library/Gg398358(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="30715-119">[Set-CsCpsConfiguration](https://technet.microsoft.com/library/Gg412721(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="30715-119">[Set-CsCpsConfiguration](https://technet.microsoft.com/library/Gg412721(v=OCS.15))</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="30715-120">См. также</span><span class="sxs-lookup"><span data-stu-id="30715-120">See Also</span></span>


[<span data-ttu-id="30715-121">Блог Lync Server PowerShell</span><span class="sxs-lookup"><span data-stu-id="30715-121">Lync Server PowerShell Blog</span></span>](https://go.microsoft.com/fwlink/p/?linkid=203150)  
  

<span data-ttu-id="30715-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="30715-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

