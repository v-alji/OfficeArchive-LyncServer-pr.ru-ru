---
title: 'Lync Server 2013: New-CsWebServiceConfiguration для управления адресными книгами'
description: 'Lync Server 2013: New-CsWebServiceConfiguration для управления адресными книгами.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: New-CsWebServiceConfiguration for Address Book management
ms:assetid: 49e4ecc5-aa3e-4dd4-a32c-b0dea3758fab
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429703(v=OCS.15)
ms:contentKeyID: 48184067
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8972f1b4fe71554e6a8925ddebea6303e2f074a6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445437"
---
# <a name="new-cswebserviceconfiguration-for-address-book-management-in-lync-server-2013"></a><span data-ttu-id="04bd2-103">New-CsWebServiceConfiguration для управления адресной книгой в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="04bd2-103">New-CsWebServiceConfiguration for Address Book management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="04bd2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="04bd2-104">

<span> </span></span></span>

<span data-ttu-id="04bd2-105">_**Тема последнего изменения:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="04bd2-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="04bd2-106">Кто может запустить этот командлет: по умолчанию членам следующих групп разрешено выполнять командлет New-CsWebServiceConfiguration локально: RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="04bd2-106">Who can run this cmdlet: By default, members of the following groups are authorized to run the New-CsWebServiceConfiguration cmdlet locally: RTCUniversalServerAdmins.</span></span> <span data-ttu-id="04bd2-107">Чтобы возвратить список всех ролей управления доступом на основе ролей (RBAC), которые назначены этому командлету (включая любые пользовательские роли RBAC, созданные пользователем), выполните в командной строке Windows PowerShell следующую команду:</span><span class="sxs-lookup"><span data-stu-id="04bd2-107">To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:</span></span>

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "New-CsWebServiceConfiguration"}

<span data-ttu-id="04bd2-108">New-CsWebServiceConfiguration командлета определяет новую конфигурацию веб-служб в Организации.</span><span class="sxs-lookup"><span data-stu-id="04bd2-108">The cmdlet New-CsWebServiceConfiguration defines a new configuration for Web Services in your organization.</span></span> <span data-ttu-id="04bd2-109">Область конфигурации веб-служб может находиться только на уровне сайта или службы.</span><span class="sxs-lookup"><span data-stu-id="04bd2-109">The scope for the Web Services configuration can only be at the site or service level.</span></span> <span data-ttu-id="04bd2-110">Создать новую конфигурацию веб-служб на глобальном уровне нельзя.</span><span class="sxs-lookup"><span data-stu-id="04bd2-110">It cannot create a new Web Services configuration at the global level.</span></span> <span data-ttu-id="04bd2-111">В адресную книгу, в частности, интересует атрибут EnableGroupExansion.</span><span class="sxs-lookup"><span data-stu-id="04bd2-111">Specifically of interest to the Address Book is the EnableGroupExansion attribute.</span></span> <span data-ttu-id="04bd2-112">Если установлено значение true, веб-службы могут отвечать на запросы на развертывание групп.</span><span class="sxs-lookup"><span data-stu-id="04bd2-112">If set to True, the Web Services can respond to requests for group expansion.</span></span>

<span data-ttu-id="04bd2-113">Например:</span><span class="sxs-lookup"><span data-stu-id="04bd2-113">For example:</span></span>

    New-CsWebServiceConfiguration -Identity site:Redmond -EnableGroupExpansion $False -UseCertificateAuth $True

<div>

## <a name="see-also"></a><span data-ttu-id="04bd2-114">См. также</span><span class="sxs-lookup"><span data-stu-id="04bd2-114">See Also</span></span>


[<span data-ttu-id="04bd2-115">New-CsWebServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="04bd2-115">New-CsWebServiceConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsWebServiceConfiguration)  
  

<span data-ttu-id="04bd2-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="04bd2-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

