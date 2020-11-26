---
title: 'Lync Server 2013: командлеты Active Directory'
description: 'Lync Server 2013: командлеты Active Directory.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Active Directory cmdlets
ms:assetid: 313d73cb-f3db-4bc4-8708-de4da1d719c1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg415640(v=OCS.15)
ms:contentKeyID: 48183769
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8c5e87cda24d5517b9c4501523fd06804ea20020
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439473"
---
# <a name="active-directory-cmdlets-in-lync-server-2013"></a><span data-ttu-id="ab07b-103">Командлеты Active Directory в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ab07b-103">Active Directory cmdlets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ab07b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ab07b-104">

<span> </span></span></span>

<span data-ttu-id="ab07b-105">_**Тема последнего изменения:** 2012-06-20_</span><span class="sxs-lookup"><span data-stu-id="ab07b-105">_**Topic Last Modified:** 2012-06-20_</span></span>

<span data-ttu-id="ab07b-106">Командлеты Active Directory обычно используются программой установки и редко вызываются администратором напрямую.</span><span class="sxs-lookup"><span data-stu-id="ab07b-106">The Active Directory cmdlets are typically used by Setup, and will rarely be called directly by an administrator.</span></span> <span data-ttu-id="ab07b-107">Однако администраторы могут использовать эти командлеты для подготовки (или разподготовки) домена или леса для Microsoft Lync Server 2013, а также для установки необходимых файлов схемы Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ab07b-107">However, administrators can use these cmdlets to prepare (or unprepare) a domain or forest for Microsoft Lync Server 2013, and to install the required Active Directory schema files.</span></span>

<div>

## <a name="active-directory-cmdlets"></a><span data-ttu-id="ab07b-108">Командлеты Active Directory</span><span class="sxs-lookup"><span data-stu-id="ab07b-108">Active Directory Cmdlets</span></span>

<span data-ttu-id="ab07b-109">Ниже приведен список командлетов, которые непосредственно связаны с управлением параметрами Active Directory Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ab07b-109">The following is a list of cmdlets that relate directly to managing Lync Server 2013 Active Directory settings:</span></span>

<span data-ttu-id="ab07b-110">**Active Directory**</span><span class="sxs-lookup"><span data-stu-id="ab07b-110">**Active Directory**</span></span>

  - <span></span>  
    <span data-ttu-id="ab07b-111">[Disable-CsAdDomain](https://technet.microsoft.com/library/Gg398785(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="ab07b-111">[Disable-CsAdDomain](https://technet.microsoft.com/library/Gg398785(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="ab07b-112">[Enable-CsAdDomain](https://technet.microsoft.com/library/Gg412764(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="ab07b-112">[Enable-CsAdDomain](https://technet.microsoft.com/library/Gg412764(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="ab07b-113">[Get-CsAdDomain](https://technet.microsoft.com/library/Gg398453(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="ab07b-113">[Get-CsAdDomain](https://technet.microsoft.com/library/Gg398453(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="ab07b-114">[Disable-CsAdForest](https://technet.microsoft.com/library/Gg398122(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="ab07b-114">[Disable-CsAdForest](https://technet.microsoft.com/library/Gg398122(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="ab07b-115">[Enable-CsAdForest](https://technet.microsoft.com/library/Gg425713(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="ab07b-115">[Enable-CsAdForest](https://technet.microsoft.com/library/Gg425713(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="ab07b-116">[Get-CsAdForest](https://technet.microsoft.com/library/Gg412995(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="ab07b-116">[Get-CsAdForest](https://technet.microsoft.com/library/Gg412995(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="ab07b-117">[Get-CsAdServerSchema](https://technet.microsoft.com/library/Gg413070(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="ab07b-117">[Get-CsAdServerSchema](https://technet.microsoft.com/library/Gg413070(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="ab07b-118">[Install-CsAdServerSchema](https://technet.microsoft.com/library/Gg398681(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="ab07b-118">[Install-CsAdServerSchema](https://technet.microsoft.com/library/Gg398681(v=OCS.15))</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="ab07b-119">См. также</span><span class="sxs-lookup"><span data-stu-id="ab07b-119">See Also</span></span>


[<span data-ttu-id="ab07b-120">Блог Lync Server PowerShell</span><span class="sxs-lookup"><span data-stu-id="ab07b-120">Lync Server PowerShell Blog</span></span>](https://go.microsoft.com/fwlink/p/?linkid=203150)  
  

<span data-ttu-id="ab07b-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ab07b-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

