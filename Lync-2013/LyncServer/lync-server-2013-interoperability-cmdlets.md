---
title: 'Lync Server 2013: командлеты взаимодействия'
description: 'Lync Server 2013: командлеты взаимодействия.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Interoperability cmdlets
ms:assetid: 18444a0b-7b66-4540-a262-775ea10b3b7d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204714(v=OCS.15)
ms:contentKeyID: 48183527
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 50a8bfca7621b76072cce8c68b15e5cc7e3468c4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426783"
---
# <a name="interoperability-cmdlets-in-lync-server-2013"></a><span data-ttu-id="ccc6e-103">Командлеты взаимодействия в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ccc6e-103">Interoperability cmdlets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ccc6e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ccc6e-104">

<span> </span></span></span>

<span data-ttu-id="ccc6e-105">_**Тема последнего изменения:** 2012-06-27_</span><span class="sxs-lookup"><span data-stu-id="ccc6e-105">_**Topic Last Modified:** 2012-06-27_</span></span>

<span data-ttu-id="ccc6e-106">Командлеты взаимодействия используются для настройки проверки подлинности серверов и авторизации сервера Microsoft Lync Server 2013 и других серверных продуктов, таких как Microsoft Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ccc6e-106">The interoperability cmdlets are used to configure server-to-server authentication and authorization between Microsoft Lync Server 2013 and other server products such as Microsoft Exchange Server 2013.</span></span> <span data-ttu-id="ccc6e-107">Проверка подлинности серверов и авторизация сервера позволяет этим серверам легко обмениваться данными и обмениваться ими.</span><span class="sxs-lookup"><span data-stu-id="ccc6e-107">Server-to-server authentication and authorization enables these servers to seamless exchange and share data.</span></span>

<div>

## <a name="interoperability-cmdlets"></a><span data-ttu-id="ccc6e-108">Командлеты взаимодействия</span><span class="sxs-lookup"><span data-stu-id="ccc6e-108">Interoperability Cmdlets</span></span>

<span data-ttu-id="ccc6e-109">Ниже приведен список командлетов, которые непосредственно связаны с настройкой и управлением взаимодействием между Microsoft Lync Server 2013 и другими серверными продуктами.</span><span class="sxs-lookup"><span data-stu-id="ccc6e-109">The following is a list of cmdlets that relate directly to configuring and managing interoperability between Microsoft Lync Server 2013 and other server products:</span></span>

<span data-ttu-id="ccc6e-110">**Командлеты взаимодействия**</span><span class="sxs-lookup"><span data-stu-id="ccc6e-110">**Interoperability Cmdlets**</span></span>

  - <span data-ttu-id="ccc6e-111">[Get-CsOAuthConfiguration](https://technet.microsoft.com/library/JJ205155(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="ccc6e-111">[Get-CsOAuthConfiguration](https://technet.microsoft.com/library/JJ205155(v=OCS.15))</span></span>

  - <span data-ttu-id="ccc6e-112">[Set-CsOAuthConfiguration](https://technet.microsoft.com/library/JJ204841(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="ccc6e-112">[Set-CsOAuthConfiguration](https://technet.microsoft.com/library/JJ204841(v=OCS.15))</span></span>

<!-- end list -->

  - <span data-ttu-id="ccc6e-113">[Get-CsOAuthServer](https://technet.microsoft.com/library/JJ205238(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="ccc6e-113">[Get-CsOAuthServer](https://technet.microsoft.com/library/JJ205238(v=OCS.15))</span></span>

  - <span data-ttu-id="ccc6e-114">[New-CsOAuthServer](https://technet.microsoft.com/library/JJ205206(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="ccc6e-114">[New-CsOAuthServer](https://technet.microsoft.com/library/JJ205206(v=OCS.15))</span></span>

  - <span data-ttu-id="ccc6e-115">[Remove-CsOAuthServer](https://technet.microsoft.com/library/JJ205408(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="ccc6e-115">[Remove-CsOAuthServer](https://technet.microsoft.com/library/JJ205408(v=OCS.15))</span></span>

  - <span data-ttu-id="ccc6e-116">[Set-CsOAuthServer](https://technet.microsoft.com/library/JJ204896(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="ccc6e-116">[Set-CsOAuthServer](https://technet.microsoft.com/library/JJ204896(v=OCS.15))</span></span>

<!-- end list -->

  - <span data-ttu-id="ccc6e-117">[Get-CsPartnerApplication](https://technet.microsoft.com/library/JJ205128(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="ccc6e-117">[Get-CsPartnerApplication](https://technet.microsoft.com/library/JJ205128(v=OCS.15))</span></span>

  - <span data-ttu-id="ccc6e-118">[New-CsPartnerApplication](https://technet.microsoft.com/library/JJ204628(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="ccc6e-118">[New-CsPartnerApplication](https://technet.microsoft.com/library/JJ204628(v=OCS.15))</span></span>

  - <span data-ttu-id="ccc6e-119">[Remove-CsPartnerApplication](https://technet.microsoft.com/library/JJ204820(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="ccc6e-119">[Remove-CsPartnerApplication](https://technet.microsoft.com/library/JJ204820(v=OCS.15))</span></span>

  - <span data-ttu-id="ccc6e-120">[Set-CsPartnerApplication](https://technet.microsoft.com/library/JJ204755(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="ccc6e-120">[Set-CsPartnerApplication](https://technet.microsoft.com/library/JJ204755(v=OCS.15))</span></span>

<span data-ttu-id="ccc6e-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ccc6e-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

