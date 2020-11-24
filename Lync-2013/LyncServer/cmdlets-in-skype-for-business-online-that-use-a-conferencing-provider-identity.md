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
# <a name="cmdlets-in-skype-for-business-online-that-use-a-conferencing-provider-identity"></a>Командлеты в Skype для бизнеса Online с использованием удостоверения поставщика конференц-связи

 


Чтобы получить сведения обо всех поставщиках голосовой конференц-связи, с которыми вы пропустили организацию, вы можете просто вызвать командлет [Get – CsAudioConferencingProvider](https://technet.microsoft.com/library/jj994030\(v=ocs.15\)) без каких-либо параметров:

    Get-CsAudioConferencingProvider

Если вы хотите ограничить возвращаемые данные единственным поставщиком (в этом примере — службы голосовой связи Contoso поставщика), а затем использовать параметр Identity:

    Get-CsAudioConferencingProvider -Identity "Contoso Audio Services"

Только один командлет Skype для бизнеса Online, принимающий идентификатор поставщика видеоконференций:

  - [Get-CsAudioConferencingProvider](https://technet.microsoft.com/library/jj994030\(v=ocs.15\))

## <a name="see-also"></a>См. также


[Удостоверения, области и клиенты в Skype для бизнеса Online](identities-scopes-and-tenants-in-skype-for-business-online.md)  
[Командлеты Lync Online](https://technet.microsoft.com/library/dn362817\(v=ocs.15\))

