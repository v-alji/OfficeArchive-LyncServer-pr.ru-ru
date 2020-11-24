---
title: 'Lync Server 2013: командлеты для прав пользователей и разрешений'
description: 'Lync Server 2013: командлеты для доступа пользователей и разрешения.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: User rights and permissions cmdlets
ms:assetid: b53aae4c-651f-4cbc-a762-ba818d63897e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg415672(v=OCS.15)
ms:contentKeyID: 48185178
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ec14442e6cdd5c398da9e9291109d8ba128dbd9a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398656"
---
# <a name="user-rights-and-permissions-cmdlets-in-lync-server-2013"></a><span data-ttu-id="42dbf-103">Командлеты для доступа пользователей и разрешения в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="42dbf-103">User rights and permissions cmdlets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="42dbf-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="42dbf-104">

<span> </span></span></span>

<span data-ttu-id="42dbf-105">_**Тема последнего изменения:** 2012-06-26_</span><span class="sxs-lookup"><span data-stu-id="42dbf-105">_**Topic Last Modified:** 2012-06-26_</span></span>

<span data-ttu-id="42dbf-106">Командлеты разрешений пользователей главным образом используются для управления доступом на основе ролей (RBAC), а также новыми технологиями для делегирования административного управления Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="42dbf-106">The user permission cmdlets are primarily used to manage role-based access control (RBAC), the new technology for delegating administrative control of Microsoft Lync Server 2013.</span></span>

<div>

## <a name="user-permission-cmdlets"></a><span data-ttu-id="42dbf-107">Командлеты разрешений пользователей</span><span class="sxs-lookup"><span data-stu-id="42dbf-107">User Permission Cmdlets</span></span>

<span data-ttu-id="42dbf-108">Ниже приведен список командлетов, непосредственно связанных с управлением разрешениями пользователей.</span><span class="sxs-lookup"><span data-stu-id="42dbf-108">The following is a list of cmdlets that relate directly to managing user permissions:</span></span>

<span data-ttu-id="42dbf-109">**Разрешения пользователей**</span><span class="sxs-lookup"><span data-stu-id="42dbf-109">**User Permissions**</span></span>

  - <span></span>  
    <span data-ttu-id="42dbf-110">[Get-CsAdminRole](https://technet.microsoft.com/library/Gg399050(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="42dbf-110">[Get-CsAdminRole](https://technet.microsoft.com/library/Gg399050(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="42dbf-111">[New-CsAdminRole](https://technet.microsoft.com/library/Gg398271(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="42dbf-111">[New-CsAdminRole](https://technet.microsoft.com/library/Gg398271(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="42dbf-112">[Remove-CsAdminRole](https://technet.microsoft.com/library/Gg413036(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="42dbf-112">[Remove-CsAdminRole](https://technet.microsoft.com/library/Gg413036(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="42dbf-113">[Set-CsAdminRole](https://technet.microsoft.com/library/Gg399066(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="42dbf-113">[Set-CsAdminRole](https://technet.microsoft.com/library/Gg399066(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="42dbf-114">[Update-CsAdminRole](https://technet.microsoft.com/library/JJ204851(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="42dbf-114">[Update-CsAdminRole](https://technet.microsoft.com/library/JJ204851(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="42dbf-115">[Get-CsAdminRoleAssignment](https://technet.microsoft.com/library/Gg398434(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="42dbf-115">[Get-CsAdminRoleAssignment](https://technet.microsoft.com/library/Gg398434(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="42dbf-116">[Grant-CsOUPermission](https://technet.microsoft.com/library/Gg425739(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="42dbf-116">[Grant-CsOUPermission](https://technet.microsoft.com/library/Gg425739(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="42dbf-117">[Revoke-CsOUPermission](https://technet.microsoft.com/library/Gg398977(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="42dbf-117">[Revoke-CsOUPermission](https://technet.microsoft.com/library/Gg398977(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="42dbf-118">[Test-CsOUPermission](https://technet.microsoft.com/library/Gg398787(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="42dbf-118">[Test-CsOUPermission](https://technet.microsoft.com/library/Gg398787(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="42dbf-119">[Grant-CsSetupPermission](https://technet.microsoft.com/library/Gg398569(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="42dbf-119">[Grant-CsSetupPermission](https://technet.microsoft.com/library/Gg398569(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="42dbf-120">[Revoke-CsSetupPermission](https://technet.microsoft.com/library/Gg425834(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="42dbf-120">[Revoke-CsSetupPermission](https://technet.microsoft.com/library/Gg425834(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="42dbf-121">[Test-CsSetupPermission](https://technet.microsoft.com/library/Gg398428(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="42dbf-121">[Test-CsSetupPermission](https://technet.microsoft.com/library/Gg398428(v=OCS.15))</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="42dbf-122">См. также</span><span class="sxs-lookup"><span data-stu-id="42dbf-122">See Also</span></span>


[<span data-ttu-id="42dbf-123">Блог Lync Server PowerShell</span><span class="sxs-lookup"><span data-stu-id="42dbf-123">Lync Server PowerShell Blog</span></span>](https://go.microsoft.com/fwlink/p/?linkid=203150)  
  

<span data-ttu-id="42dbf-124"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="42dbf-124"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

