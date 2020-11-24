---
title: Командлеты в Skype для бизнеса Online с использованием удостоверения поставщика конференц-связи
description: Командлеты в Skype для бизнеса Online, в которых используется удостоверение поставщика конференц-связи.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Cmdlets that use a conferencing provider identity
ms:assetid: be5621b6-ec11-4b12-83ec-075af269ca6a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362841(v=OCS.15)
ms:contentKeyID: 56558858
ms.date: 05/04/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 61ab4fb410878ca73314b73737948d9961462c87
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398572"
---
# <a name="cmdlets-in-skype-for-business-online-that-use-a-conferencing-provider-identity"></a><span data-ttu-id="243ba-103">Командлеты в Skype для бизнеса Online с использованием удостоверения поставщика конференц-связи</span><span class="sxs-lookup"><span data-stu-id="243ba-103">Cmdlets in Skype for Business Online that use a conferencing provider identity</span></span>

 


<span data-ttu-id="243ba-104">Чтобы получить сведения обо всех поставщиках голосовой конференц-связи, с которыми вы пропустили организацию, вы можете просто вызвать командлет [Get – CsAudioConferencingProvider](https://technet.microsoft.com/library/jj994030\(v=ocs.15\)) без каких-либо параметров:</span><span class="sxs-lookup"><span data-stu-id="243ba-104">To return information about all of the audio conferencing providers that your organization has contracted with, you can simply call the [Get-CsAudioConferencingProvider](https://technet.microsoft.com/library/jj994030\(v=ocs.15\)) cmdlet without any parameters:</span></span>

    Get-CsAudioConferencingProvider

<span data-ttu-id="243ba-105">Если вы хотите ограничить возвращаемые данные единственным поставщиком (в этом примере — службы голосовой связи Contoso поставщика), а затем использовать параметр Identity:</span><span class="sxs-lookup"><span data-stu-id="243ba-105">If you want to limit the returned data to a single provider (in this example, the provider Contoso Audio Services), then use the Identity parameter:</span></span>

    Get-CsAudioConferencingProvider -Identity "Contoso Audio Services"

<span data-ttu-id="243ba-106">Только один командлет Skype для бизнеса Online, принимающий идентификатор поставщика видеоконференций:</span><span class="sxs-lookup"><span data-stu-id="243ba-106">There is only one Skype for Business Online cmdlet that accepts an audio conferencing provider ID:</span></span>

  - <span data-ttu-id="243ba-107">[Get-CsAudioConferencingProvider](https://technet.microsoft.com/library/jj994030\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="243ba-107">[Get-CsAudioConferencingProvider](https://technet.microsoft.com/library/jj994030\(v=ocs.15\))</span></span>

## <a name="see-also"></a><span data-ttu-id="243ba-108">См. также</span><span class="sxs-lookup"><span data-stu-id="243ba-108">See Also</span></span>


[<span data-ttu-id="243ba-109">Удостоверения, области и клиенты в Skype для бизнеса Online</span><span class="sxs-lookup"><span data-stu-id="243ba-109">Identities, scopes, and tenants in Skype for Business Online</span></span>](identities-scopes-and-tenants-in-skype-for-business-online.md)  
<span data-ttu-id="243ba-110">[Командлеты Lync Online](https://technet.microsoft.com/library/dn362817\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="243ba-110">[The Skype for Business Online cmdlets](https://technet.microsoft.com/library/dn362817\(v=ocs.15\))</span></span>

