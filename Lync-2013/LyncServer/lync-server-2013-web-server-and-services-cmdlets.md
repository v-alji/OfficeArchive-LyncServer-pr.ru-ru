---
title: 'Lync Server 2013: командлеты веб-сервера и служб'
description: 'Lync Server 2013: командлеты веб-сервера и служб.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Web server and services cmdlets
ms:assetid: 07ce7fd4-4068-4957-9cb9-fd121b43858c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg415631(v=OCS.15)
ms:contentKeyID: 48183326
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a5a4aca9d9859a070459b07d731271142d04b603
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398647"
---
# <a name="web-server-and-services-cmdlets-in-lync-server-2013"></a><span data-ttu-id="87d80-103">Командлеты веб-сервера и служб в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="87d80-103">Web server and services cmdlets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="87d80-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="87d80-104">

<span> </span></span></span>

<span data-ttu-id="87d80-105">_**Тема последнего изменения:** 2013-02-18_</span><span class="sxs-lookup"><span data-stu-id="87d80-105">_**Topic Last Modified:** 2013-02-18_</span></span>

<span data-ttu-id="87d80-106">Многие компоненты Microsoft Lync Server 2013 — это веб-компоненты, которые используются для выполнения своих задач, а также веб-службами.</span><span class="sxs-lookup"><span data-stu-id="87d80-106">Many Microsoft Lync Server 2013 components are web-based: these components either use Web Services or webpages to carry out their tasks.</span></span> <span data-ttu-id="87d80-107">С помощью командлетов веб-сервера и веб-служб можно настраивать параметры веб-сервера и управлять простыми URL-адресами.</span><span class="sxs-lookup"><span data-stu-id="87d80-107">The Web Server and Web services cmdlets enable you to do such things as configure Web Server settings and to manage simple URLs.</span></span> <span data-ttu-id="87d80-108">Простые URL-адреса упрощают присоединение к собраниям и конференциям и упрощение входа пользователей на панель управления Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="87d80-108">Simple URLs make it easier for users to join meetings and conferences, and make it easier for Administrators to log on to the Lync Server 2013 Control Panel.</span></span>

<div>

## <a name="web-server-and-web-services-cmdlets"></a><span data-ttu-id="87d80-109">Командлеты веб-сервера и веб-служб</span><span class="sxs-lookup"><span data-stu-id="87d80-109">Web Server and Web Services Cmdlets</span></span>

<span data-ttu-id="87d80-110">Ниже приведен список командлетов, которые непосредственно относятся к управлению веб-серверами и веб-службам.</span><span class="sxs-lookup"><span data-stu-id="87d80-110">The following is a list of cmdlets that relate directly to managing Web Servers and Web Services:</span></span>

<span data-ttu-id="87d80-111">**Веб-серверы и службы**</span><span class="sxs-lookup"><span data-stu-id="87d80-111">**Web Servers and Services**</span></span>

  - <span></span>  
    <span data-ttu-id="87d80-112">[New-CsSimpleUrl](https://technet.microsoft.com/library/Gg398180(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="87d80-112">[New-CsSimpleUrl](https://technet.microsoft.com/library/Gg398180(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="87d80-113">[Get-CsSimpleUrlConfiguration](https://technet.microsoft.com/library/Gg398392(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="87d80-113">[Get-CsSimpleUrlConfiguration](https://technet.microsoft.com/library/Gg398392(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="87d80-114">[New-CsSimpleUrlConfiguration](https://technet.microsoft.com/library/Gg425813(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="87d80-114">[New-CsSimpleUrlConfiguration](https://technet.microsoft.com/library/Gg425813(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="87d80-115">[Remove-CsSimpleUrlConfiguration](https://technet.microsoft.com/library/Gg398515(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="87d80-115">[Remove-CsSimpleUrlConfiguration](https://technet.microsoft.com/library/Gg398515(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="87d80-116">[Set-CsSimpleUrlConfiguration](https://technet.microsoft.com/library/Gg412991(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="87d80-116">[Set-CsSimpleUrlConfiguration](https://technet.microsoft.com/library/Gg412991(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="87d80-117">[New-CsSimpleUrlEntry](https://technet.microsoft.com/library/Gg425902(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="87d80-117">[New-CsSimpleUrlEntry](https://technet.microsoft.com/library/Gg425902(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="87d80-118">[New-CsWebOrigin](https://technet.microsoft.com/library/JJ950236(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="87d80-118">[New-CsWebOrigin](https://technet.microsoft.com/library/JJ950236(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="87d80-119">[Set-CsWebServer](https://technet.microsoft.com/library/Gg398759(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="87d80-119">[Set-CsWebServer](https://technet.microsoft.com/library/Gg398759(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="87d80-120">[Get-CsWebServiceConfiguration](https://technet.microsoft.com/library/Gg425751(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="87d80-120">[Get-CsWebServiceConfiguration](https://technet.microsoft.com/library/Gg425751(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="87d80-121">[New-CsWebServiceConfiguration](https://technet.microsoft.com/library/Gg398440(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="87d80-121">[New-CsWebServiceConfiguration](https://technet.microsoft.com/library/Gg398440(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="87d80-122">[Remove-CsWebServiceConfiguration](https://technet.microsoft.com/library/Gg398266(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="87d80-122">[Remove-CsWebServiceConfiguration](https://technet.microsoft.com/library/Gg398266(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="87d80-123">[Set-CsWebServiceConfiguration](https://technet.microsoft.com/library/Gg398396(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="87d80-123">[Set-CsWebServiceConfiguration](https://technet.microsoft.com/library/Gg398396(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="87d80-124">[New-CsWebTrustedCACertificate](https://technet.microsoft.com/library/Gg412746(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="87d80-124">[New-CsWebTrustedCACertificate](https://technet.microsoft.com/library/Gg412746(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="87d80-125">[New-CsKerberosAccount](https://technet.microsoft.com/library/Gg398485(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="87d80-125">[New-CsKerberosAccount](https://technet.microsoft.com/library/Gg398485(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="87d80-126">[Get-CsKerberosAccountAssignment](https://technet.microsoft.com/library/Gg398526(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="87d80-126">[Get-CsKerberosAccountAssignment](https://technet.microsoft.com/library/Gg398526(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="87d80-127">[New-CsKerberosAccountAssignment](https://technet.microsoft.com/library/Gg398074(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="87d80-127">[New-CsKerberosAccountAssignment](https://technet.microsoft.com/library/Gg398074(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="87d80-128">[Remove-CsKerberosAccountAssignment](https://technet.microsoft.com/library/Gg413052(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="87d80-128">[Remove-CsKerberosAccountAssignment](https://technet.microsoft.com/library/Gg413052(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="87d80-129">[Set-CsKerberosAccountAssignment](https://technet.microsoft.com/library/Gg398232(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="87d80-129">[Set-CsKerberosAccountAssignment](https://technet.microsoft.com/library/Gg398232(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="87d80-130">[Test-CsKerberosAccountAssignment](https://technet.microsoft.com/library/Gg425938(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="87d80-130">[Test-CsKerberosAccountAssignment](https://technet.microsoft.com/library/Gg425938(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="87d80-131">[Set-CsKerberosAccountPassword](https://technet.microsoft.com/library/Gg398659(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="87d80-131">[Set-CsKerberosAccountPassword](https://technet.microsoft.com/library/Gg398659(v=OCS.15))</span></span>

<!-- end list -->

  - <span data-ttu-id="87d80-132">[Test-CsWebApp](https://technet.microsoft.com/library/Hh689989(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="87d80-132">[Test-CsWebApp](https://technet.microsoft.com/library/Hh689989(v=OCS.15))</span></span>

  - <span data-ttu-id="87d80-133">[Test-CsWebAppAnonymous](https://technet.microsoft.com/library/Hh690041(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="87d80-133">[Test-CsWebAppAnonymous](https://technet.microsoft.com/library/Hh690041(v=OCS.15))</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="87d80-134">См. также</span><span class="sxs-lookup"><span data-stu-id="87d80-134">See Also</span></span>


[<span data-ttu-id="87d80-135">Блог Lync Server PowerShell</span><span class="sxs-lookup"><span data-stu-id="87d80-135">Lync Server PowerShell Blog</span></span>](https://go.microsoft.com/fwlink/p/?linkid=203150)  
  

<span data-ttu-id="87d80-136"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="87d80-136"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

