---
title: 'Lync Server 2013: командлеты регистратора и режиссер'
description: 'Lync Server 2013: регистраторы и режиссер командлетов.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Registrar and Director cmdlets
ms:assetid: 327c08ab-7e1e-47c0-b280-a001722c116f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg415641(v=OCS.15)
ms:contentKeyID: 48183813
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7a0cd1775e2fc4e83e3507cbbea588b57550b8cb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436547"
---
# <a name="registrar-and-director-cmdlets-in-lync-server-2013"></a><span data-ttu-id="13015-103">Командлеты регистраторов и режиссеры в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="13015-103">Registrar and Director cmdlets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="13015-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="13015-104">

<span> </span></span></span>

<span data-ttu-id="13015-105">_**Тема последнего изменения:** 2012-10-09_</span><span class="sxs-lookup"><span data-stu-id="13015-105">_**Topic Last Modified:** 2012-10-09_</span></span>

<span data-ttu-id="13015-106">Регистраторы и режиссеры используются для проверки подлинности запросов на вход и для хранения сведений о состоянии пользователей и доступности.</span><span class="sxs-lookup"><span data-stu-id="13015-106">Registrars and Directors are used to authenticate logon requests and to maintain information about user status and availability.</span></span> <span data-ttu-id="13015-107">Командлеты регистраторов и режиссер позволяют управлять параметрами конфигурации для этих серверов.</span><span class="sxs-lookup"><span data-stu-id="13015-107">The Registrar and Director cmdlets enable you to manage configuration settings for these servers.</span></span>

<div>

## <a name="registrar-and-director-cmdlets"></a><span data-ttu-id="13015-108">Командлеты регистратора и режиссера</span><span class="sxs-lookup"><span data-stu-id="13015-108">Registrar and Director Cmdlets</span></span>

<span data-ttu-id="13015-109">Ниже приведен список командлетов, непосредственно связанных с управлением регистраторами и режиссерами.</span><span class="sxs-lookup"><span data-stu-id="13015-109">The following is a list of cmdlets that relate directly to managing Registrars and Directors:</span></span>

<span data-ttu-id="13015-110">**Регистраторы и режиссеры**</span><span class="sxs-lookup"><span data-stu-id="13015-110">**Registrars and Directors**</span></span>

  - <span></span>  
    <span data-ttu-id="13015-111">[Set-CsDirector](https://technet.microsoft.com/library/Gg398565(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="13015-111">[Set-CsDirector](https://technet.microsoft.com/library/Gg398565(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="13015-112">[Reset-CsPoolRegistrarState](https://technet.microsoft.com/library/JJ619172(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="13015-112">[Reset-CsPoolRegistrarState](https://technet.microsoft.com/library/JJ619172(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="13015-113">[Set-CsRegistrar](https://technet.microsoft.com/library/Gg398993(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="13015-113">[Set-CsRegistrar](https://technet.microsoft.com/library/Gg398993(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="13015-114">[Get-CsRegistrarConfiguration](https://technet.microsoft.com/library/Gg398483(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="13015-114">[Get-CsRegistrarConfiguration](https://technet.microsoft.com/library/Gg398483(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="13015-115">[New-CsRegistrarConfiguration](https://technet.microsoft.com/library/Gg425893(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="13015-115">[New-CsRegistrarConfiguration](https://technet.microsoft.com/library/Gg425893(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="13015-116">[Remove-CsRegistrarConfiguration](https://technet.microsoft.com/library/Gg398482(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="13015-116">[Remove-CsRegistrarConfiguration](https://technet.microsoft.com/library/Gg398482(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="13015-117">[Set-CsRegistrarConfiguration](https://technet.microsoft.com/library/Gg398764(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="13015-117">[Set-CsRegistrarConfiguration](https://technet.microsoft.com/library/Gg398764(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="13015-118">[Test-CsRegistration](https://technet.microsoft.com/library/Gg412737(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="13015-118">[Test-CsRegistration](https://technet.microsoft.com/library/Gg412737(v=OCS.15))</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="13015-119">См. также</span><span class="sxs-lookup"><span data-stu-id="13015-119">See Also</span></span>


[<span data-ttu-id="13015-120">Блог Lync Server PowerShell</span><span class="sxs-lookup"><span data-stu-id="13015-120">Lync Server PowerShell Blog</span></span>](https://go.microsoft.com/fwlink/p/?linkid=203150)  
  

<span data-ttu-id="13015-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="13015-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

