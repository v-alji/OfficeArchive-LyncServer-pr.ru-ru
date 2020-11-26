---
title: 'Lync Server 2013: Remove-CsWebServiceConfiguration для управления адресными книгами'
description: 'Lync Server 2013: Remove-CsWebServiceConfiguration для управления адресными книгами.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Remove-CsWebServiceConfiguration for Address Book management
ms:assetid: 91947cad-5cdd-41b9-83e1-650703c55879
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429713(v=OCS.15)
ms:contentKeyID: 48184848
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 145cb1cb98bcb4c988a8fdaea74a4eae86d5fc4f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436428"
---
# <a name="remove-cswebserviceconfiguration-for-address-book-management-in-lync-server-2013"></a><span data-ttu-id="9a79e-103">Remove-CsWebServiceConfiguration для управления адресной книгой в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9a79e-103">Remove-CsWebServiceConfiguration for Address Book management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9a79e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9a79e-104">

<span> </span></span></span>

<span data-ttu-id="9a79e-105">_**Тема последнего изменения:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="9a79e-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="9a79e-106">Кто может запустить этот командлет: по умолчанию членам следующих групп разрешено выполнять командлет Remove-CsWebServiceConfiguration локально: RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="9a79e-106">Who can run this cmdlet: By default, members of the following groups are authorized to run the Remove-CsWebServiceConfiguration cmdlet locally: RTCUniversalServerAdmins.</span></span> <span data-ttu-id="9a79e-107">Чтобы возвратить список всех ролей управления доступом на основе ролей (RBAC), которые назначены этому командлету (включая любые пользовательские роли RBAC, созданные пользователем), выполните в командной строке Windows PowerShell следующую команду:</span><span class="sxs-lookup"><span data-stu-id="9a79e-107">To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:</span></span>

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Remove-CsWebServiceConfiguration"}

<span data-ttu-id="9a79e-108">Командлет Remove-CsWebServiceConfiguration позволяет администратору удалить ранее созданную конфигурацию веб-служб.</span><span class="sxs-lookup"><span data-stu-id="9a79e-108">The Remove-CsWebServiceConfiguration cmdlet allows an administrator to remove a previously created Web Services configuration.</span></span> <span data-ttu-id="9a79e-109">Командлет не может удалить глобальную конфигурацию веб-служб.</span><span class="sxs-lookup"><span data-stu-id="9a79e-109">The cmdlet cannot remove the global Web Services configuration.</span></span>

<span data-ttu-id="9a79e-110">Например:</span><span class="sxs-lookup"><span data-stu-id="9a79e-110">For example:</span></span>

    Remove-CsWebServiceConfiguration -Identity site:Redmond

<div>

## <a name="see-also"></a><span data-ttu-id="9a79e-111">См. также</span><span class="sxs-lookup"><span data-stu-id="9a79e-111">See Also</span></span>


[<span data-ttu-id="9a79e-112">Remove-CsWebServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="9a79e-112">Remove-CsWebServiceConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsWebServiceConfiguration)  
  

<span data-ttu-id="9a79e-113"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9a79e-113"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

