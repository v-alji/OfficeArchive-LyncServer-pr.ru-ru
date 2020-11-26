---
title: 'Lync Server 2013: командлеты правил нормализации голосовой связи'
description: 'Lync Server 2013: командлеты правил нормализации голосовой связи.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Voice normalization rules cmdlets
ms:assetid: 8d500ccb-318b-4bb3-87fe-63bff4d8d436
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg415662(v=OCS.15)
ms:contentKeyID: 48184758
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8a130c9dd7bca7969237292c9fc8017e59995a19
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440390"
---
# <a name="voice-normalization-rules-cmdlets-in-lync-server-2013"></a><span data-ttu-id="30f8d-103">Командлеты правил нормализации голосовой связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="30f8d-103">Voice normalization rules cmdlets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="30f8d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="30f8d-104">

<span> </span></span></span>

<span data-ttu-id="30f8d-105">_**Тема последнего изменения:** 2012-06-20_</span><span class="sxs-lookup"><span data-stu-id="30f8d-105">_**Topic Last Modified:** 2012-06-20_</span></span>

<span data-ttu-id="30f8d-106">Правила нормализации голоса используются для преобразования требования набора номера (например, набора номера 9 для доступа к внешней линии) на формат телефонного номера E. 164, используемого Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="30f8d-106">Voice normalization rules are used to convert a telephone dialing requirement (for example, dialing 9 to access an outside line) to the E.164 phone number format used by Microsoft Lync Server 2013.</span></span>

<div>

## <a name="voice-normalization-rules-cmdlets"></a><span data-ttu-id="30f8d-107">Командлеты правил нормализации голосовых сообщений</span><span class="sxs-lookup"><span data-stu-id="30f8d-107">Voice Normalization Rules Cmdlets</span></span>

<span data-ttu-id="30f8d-108">Для управления правилами нормализации голосовой связи можно использовать следующие командлеты.</span><span class="sxs-lookup"><span data-stu-id="30f8d-108">The following cmdlets can be used to manage voice normalization rules.</span></span>

<span data-ttu-id="30f8d-109">**Правила нормализации голосовых сообщений**</span><span class="sxs-lookup"><span data-stu-id="30f8d-109">**Voice Normalization Rules**</span></span>

  - <span></span>  
    <span data-ttu-id="30f8d-110">[Get-CsVoiceNormalizationRule](https://technet.microsoft.com/library/Gg398393(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="30f8d-110">[Get-CsVoiceNormalizationRule](https://technet.microsoft.com/library/Gg398393(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="30f8d-111">[New-CsVoiceNormalizationRule](https://technet.microsoft.com/library/Gg398240(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="30f8d-111">[New-CsVoiceNormalizationRule](https://technet.microsoft.com/library/Gg398240(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="30f8d-112">[Remove-CsVoiceNormalizationRule](https://technet.microsoft.com/library/Gg398501(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="30f8d-112">[Remove-CsVoiceNormalizationRule](https://technet.microsoft.com/library/Gg398501(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="30f8d-113">[Set-CsVoiceNormalizationRule](https://technet.microsoft.com/library/Gg398491(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="30f8d-113">[Set-CsVoiceNormalizationRule](https://technet.microsoft.com/library/Gg398491(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="30f8d-114">[Test-CsVoiceNormalizationRule](https://technet.microsoft.com/library/Gg399003(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="30f8d-114">[Test-CsVoiceNormalizationRule](https://technet.microsoft.com/library/Gg399003(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="30f8d-115">[New-CsVoiceRegex](https://technet.microsoft.com/library/Gg412751(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="30f8d-115">[New-CsVoiceRegex](https://technet.microsoft.com/library/Gg412751(v=OCS.15))</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="30f8d-116">См. также</span><span class="sxs-lookup"><span data-stu-id="30f8d-116">See Also</span></span>


[<span data-ttu-id="30f8d-117">Командлеты для корпоративных голосовых команд в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="30f8d-117">Enterprise Voice cmdlets in Lync Server 2013</span></span>](lync-server-2013-enterprise-voice-cmdlets.md)  


[<span data-ttu-id="30f8d-118">Блог Lync Server PowerShell</span><span class="sxs-lookup"><span data-stu-id="30f8d-118">Lync Server PowerShell Blog</span></span>](https://go.microsoft.com/fwlink/p/?linkid=203150)  
  

<span data-ttu-id="30f8d-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="30f8d-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

