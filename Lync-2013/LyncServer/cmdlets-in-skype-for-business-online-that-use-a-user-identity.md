---
title: Командлеты в Skype для бизнеса Online, использующие удостоверение пользователя
description: Командлеты в Skype для бизнеса Online, в которых используется удостоверение пользователя.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Cmdlets that use a user identity
ms:assetid: be87409f-6372-4c70-91ac-6ef13dfbe65a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362842(v=OCS.15)
ms:contentKeyID: 56558859
ms.date: 05/04/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 29f838317f8b2779de862eb2df82ae1b348871e4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398563"
---
# <a name="cmdlets-in-skype-for-business-online-that-use-a-user-identity"></a><span data-ttu-id="e48a5-103">Командлеты в Skype для бизнеса Online, использующие удостоверение пользователя</span><span class="sxs-lookup"><span data-stu-id="e48a5-103">Cmdlets in Skype for Business Online that use a user identity</span></span>

 


<span data-ttu-id="e48a5-104">В Skype для бизнеса Online есть несколько способов ссылки на индивидуальные удостоверения пользователей.</span><span class="sxs-lookup"><span data-stu-id="e48a5-104">In Skype for Business Online, there are a number of different ways to reference an individual user Identity:</span></span>

  - <span data-ttu-id="e48a5-105">Введите отображаемое имя пользователя доменных служб Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e48a5-105">Use the user’s Active Directory Domain Services display name.</span></span> <span data-ttu-id="e48a5-106">Например:</span><span class="sxs-lookup"><span data-stu-id="e48a5-106">For example:</span></span>
    
        -Identity "Ken Myer"

  - <span data-ttu-id="e48a5-107">Используйте SIP-адрес пользователя.</span><span class="sxs-lookup"><span data-stu-id="e48a5-107">Use the user’s SIP address.</span></span> <span data-ttu-id="e48a5-108">Например:</span><span class="sxs-lookup"><span data-stu-id="e48a5-108">For example:</span></span>
    
        -Identity "sip:kenmyer@litwareinc.com"

  - <span data-ttu-id="e48a5-109">Используйте имя участника-пользователя.</span><span class="sxs-lookup"><span data-stu-id="e48a5-109">Use the user’s UPN.</span></span> <span data-ttu-id="e48a5-110">Например:</span><span class="sxs-lookup"><span data-stu-id="e48a5-110">For example:</span></span>
    
        -Identity " kenmyer@litwareinc.com"

  - <span data-ttu-id="e48a5-111">Используйте различающееся имя доменных служб Active Directory пользователя.</span><span class="sxs-lookup"><span data-stu-id="e48a5-111">Use the user’s Active Directory Domain Services distinguished name.</span></span> <span data-ttu-id="e48a5-112">Например:</span><span class="sxs-lookup"><span data-stu-id="e48a5-112">For example:</span></span>
    
        -Identity "CN=48ebd1ba-95d4-460c-b751-811ebf0c4611,OU=fa8226f5-14fa-46da-8 236-039b25bc7a27,OU=Lync Online Tenants,DC=litwareinc,DC=com"

<span data-ttu-id="e48a5-113">Следующие командлеты допускают удостоверение пользователя:</span><span class="sxs-lookup"><span data-stu-id="e48a5-113">The following cmdlets accept a user Identity:</span></span>

  - <span data-ttu-id="e48a5-114">[Disable-CsMeetingRoom](https://technet.microsoft.com/library/jj204723\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="e48a5-114">[Disable-CsMeetingRoom](https://technet.microsoft.com/library/jj204723\(v=ocs.15\))</span></span>

  - <span data-ttu-id="e48a5-115">[Enable-CsMeetingRoom](https://technet.microsoft.com/library/jj205062\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="e48a5-115">[Enable-CsMeetingRoom](https://technet.microsoft.com/library/jj205062\(v=ocs.15\))</span></span>

  - <span data-ttu-id="e48a5-116">[Get-CsExUmContact](https://technet.microsoft.com/library/gg412725\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="e48a5-116">[Get-CsExUmContact](https://technet.microsoft.com/library/gg412725\(v=ocs.15\))</span></span>

  - <span data-ttu-id="e48a5-117">[Get-CsMeetingRoom](https://technet.microsoft.com/library/jj205277\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="e48a5-117">[Get-CsMeetingRoom](https://technet.microsoft.com/library/jj205277\(v=ocs.15\))</span></span>

  - <span data-ttu-id="e48a5-118">[Get-CsOnlineUser](https://technet.microsoft.com/library/jj994026\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="e48a5-118">[Get-CsOnlineUser](https://technet.microsoft.com/library/jj994026\(v=ocs.15\))</span></span>

  - <span data-ttu-id="e48a5-119">[Get-CsUserAcp](https://technet.microsoft.com/library/gg398978\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="e48a5-119">[Get-CsUserAcp](https://technet.microsoft.com/library/gg398978\(v=ocs.15\))</span></span>

  - <span data-ttu-id="e48a5-120">[New-CsExUmContact](https://technet.microsoft.com/library/gg398139\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="e48a5-120">[New-CsExUmContact](https://technet.microsoft.com/library/gg398139\(v=ocs.15\))</span></span>

  - <span data-ttu-id="e48a5-121">[Remove-CsExUmContact](https://technet.microsoft.com/library/gg398946\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="e48a5-121">[Remove-CsExUmContact](https://technet.microsoft.com/library/gg398946\(v=ocs.15\))</span></span>

  - <span data-ttu-id="e48a5-122">[Remove-CsUserAcp](https://technet.microsoft.com/library/gg398982\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="e48a5-122">[Remove-CsUserAcp](https://technet.microsoft.com/library/gg398982\(v=ocs.15\))</span></span>

  - <span data-ttu-id="e48a5-123">[Set-CsExUmContact](https://technet.microsoft.com/library/gg412944\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="e48a5-123">[Set-CsExUmContact](https://technet.microsoft.com/library/gg412944\(v=ocs.15\))</span></span>

  - <span data-ttu-id="e48a5-124">[Set-CsMeetingRoom](https://technet.microsoft.com/library/jj204831\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="e48a5-124">[Set-CsMeetingRoom](https://technet.microsoft.com/library/jj204831\(v=ocs.15\))</span></span>

  - <span data-ttu-id="e48a5-125">[Set-CsUserAcp](https://technet.microsoft.com/library/gg413018\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="e48a5-125">[Set-CsUserAcp](https://technet.microsoft.com/library/gg413018\(v=ocs.15\))</span></span>

<span data-ttu-id="e48a5-126">Обратите внимание, что при вызове одного из командлетов **Get-CS** вам не нужно указывать удостоверение пользователя.</span><span class="sxs-lookup"><span data-stu-id="e48a5-126">Note that you do not need to specify a user Identity when calling one of the **Get-Cs** cmdlets.</span></span> <span data-ttu-id="e48a5-127">В этом случае командлеты возвращают все экземпляры указанного элемента.</span><span class="sxs-lookup"><span data-stu-id="e48a5-127">In this case, the cmdlets return all the instances of the specified item.</span></span> <span data-ttu-id="e48a5-128">Например, эта команда возвращает сведения обо всех пользователях, которые были включены в Skype для бизнеса Online:</span><span class="sxs-lookup"><span data-stu-id="e48a5-128">For example, this command returns information about all the users who have been enabled for Skype for Business Online:</span></span>

    Get-CsOnlineUser

<span data-ttu-id="e48a5-129">Параметр Identity является обязательным только в том случае, если вы хотите вернуть сведения для определенного пользователя:</span><span class="sxs-lookup"><span data-stu-id="e48a5-129">The Identity parameter is required only if you want to return information for a specific user:</span></span>

    Get-CsOnlineUser -Identity "Ken Myer"

## <a name="see-also"></a><span data-ttu-id="e48a5-130">См. также</span><span class="sxs-lookup"><span data-stu-id="e48a5-130">See Also</span></span>


[<span data-ttu-id="e48a5-131">Удостоверения, области и клиенты в Skype для бизнеса Online</span><span class="sxs-lookup"><span data-stu-id="e48a5-131">Identities, scopes, and tenants in Skype for Business Online</span></span>](identities-scopes-and-tenants-in-skype-for-business-online.md)  
<span data-ttu-id="e48a5-132">[Командлеты Lync Online](https://technet.microsoft.com/library/dn362817\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="e48a5-132">[The Skype for Business Online cmdlets](https://technet.microsoft.com/library/dn362817\(v=ocs.15\))</span></span>

