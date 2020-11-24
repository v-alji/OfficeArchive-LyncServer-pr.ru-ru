---
title: Командлеты в Skype для бизнеса Online, не использующие область или удостоверение
description: Командлеты в Skype для бизнеса Online, не использующие область или удостоверение.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Cmdlets that do not use a scope or an identity
ms:assetid: 9c50c732-3c64-4b6a-96fd-8f528eb739ce
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362824(v=OCS.15)
ms:contentKeyID: 56558839
ms.date: 05/04/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e7d893c4cf9203c8657dfbdfd7fb2bf46dbdfe4e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398578"
---
# <a name="cmdlets-in-skype-for-business-online-that-do-not-use-a-scope-or-an-identity"></a><span data-ttu-id="c1dd0-103">Командлеты в Skype для бизнеса Online, не использующие область или удостоверение</span><span class="sxs-lookup"><span data-stu-id="c1dd0-103">Cmdlets in Skype for Business Online that do not use a scope or an identity</span></span>

 


<span data-ttu-id="c1dd0-104">Командлеты, используемые при изменении списков разрешенных и заблокированных списков (списки, которые определяют, какие внешние организации могут взаимодействовать с ними) не используют ни область, ни удостоверение.</span><span class="sxs-lookup"><span data-stu-id="c1dd0-104">The cmdlets used when modifying the allowed lists and blocked lists (lists that determine which outside organizations your users are allowed to communicate with) do not use either a scope or an Identity.</span></span> <span data-ttu-id="c1dd0-105">На самом деле командлет **New-CsEdgeAllowAllKnownDomains** не имеет никаких каких-либо параметров.</span><span class="sxs-lookup"><span data-stu-id="c1dd0-105">In fact, the **New-CsEdgeAllowAllKnownDomains** cmdlet does not have any parameters whatsoever.</span></span> <span data-ttu-id="c1dd0-106">Ниже указаны командлеты, которые не используют ни область, ни удостоверение.</span><span class="sxs-lookup"><span data-stu-id="c1dd0-106">The cmdlets that do not use either a scope or an Identity are:</span></span>

  - <span data-ttu-id="c1dd0-107">[New-CsEdgeAllowAllKnownDomains](https://technet.microsoft.com/library/jj994088\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="c1dd0-107">[New-CsEdgeAllowAllKnownDomains](https://technet.microsoft.com/library/jj994088\(v=ocs.15\))</span></span>

  - <span data-ttu-id="c1dd0-108">[New-CsEdgeAllowList](https://technet.microsoft.com/library/jj994023\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="c1dd0-108">[New-CsEdgeAllowList](https://technet.microsoft.com/library/jj994023\(v=ocs.15\))</span></span>

  - <span data-ttu-id="c1dd0-109">[New-CsEdgeDomainPattern](https://technet.microsoft.com/library/jj994040\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="c1dd0-109">[New-CsEdgeDomainPattern](https://technet.microsoft.com/library/jj994040\(v=ocs.15\))</span></span>

<span data-ttu-id="c1dd0-110">Обратите внимание, что вместе с командлетом New **-CsEdgeAllowList** и командлетом **New-CsEdgeDomainPattern** необходимо добавить параметр Domain.</span><span class="sxs-lookup"><span data-stu-id="c1dd0-110">Note that, with both the **New-CsEdgeAllowList** cmdlet and the **New-CsEdgeDomainPattern** cmdlet, you must include the Domain parameter.</span></span> <span data-ttu-id="c1dd0-111">Например:</span><span class="sxs-lookup"><span data-stu-id="c1dd0-111">For example:</span></span>

    $x = New-CsEdgeDomainPattern -Domain "fabrikam.com"

## <a name="see-also"></a><span data-ttu-id="c1dd0-112">См. также</span><span class="sxs-lookup"><span data-stu-id="c1dd0-112">See Also</span></span>


[<span data-ttu-id="c1dd0-113">Удостоверения, области и клиенты в Skype для бизнеса Online</span><span class="sxs-lookup"><span data-stu-id="c1dd0-113">Identities, scopes, and tenants in Skype for Business Online</span></span>](identities-scopes-and-tenants-in-skype-for-business-online.md)  
<span data-ttu-id="c1dd0-114">[Командлеты Lync Online](https://technet.microsoft.com/library/dn362817\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="c1dd0-114">[The Skype for Business Online cmdlets](https://technet.microsoft.com/library/dn362817\(v=ocs.15\))</span></span>

