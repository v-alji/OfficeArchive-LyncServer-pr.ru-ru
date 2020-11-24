---
title: 'Lync Server 2013: командлеты подключения PSTN'
description: 'Lync Server 2013: командлеты подключения PSTN.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: PSTN connectivity cmdlets
ms:assetid: b19ba43c-3987-410d-a704-aba0a4fb0498
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg415670(v=OCS.15)
ms:contentKeyID: 48185142
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b36311ea2f983bb65864d13929b5052d0a408c2c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399118"
---
# <a name="pstn-connectivity-cmdlets-in-lync-server-2013"></a><span data-ttu-id="0e627-103">Командлеты подключения PSTN в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0e627-103">PSTN connectivity cmdlets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0e627-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0e627-104">

<span> </span></span></span>

<span data-ttu-id="0e627-105">_**Тема последнего изменения:** 2012-10-09_</span><span class="sxs-lookup"><span data-stu-id="0e627-105">_**Topic Last Modified:** 2012-10-09_</span></span>

<span data-ttu-id="0e627-106">Корпоративная голосовая связь предоставляет параметры, позволяющие звонить через общедоступную телефонную сеть (PSTN), не отменяя качество обслуживания (QoS).</span><span class="sxs-lookup"><span data-stu-id="0e627-106">Enterprise Voice provides settings that allow for calls to and from the public switched telephone network (PSTN) without any decline in Quality of Service (QoS).</span></span> <span data-ttu-id="0e627-107">Эти параметры можно настроить с помощью командлетов, доступных в командной консоли Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="0e627-107">You can configure these settings through cmdlets available from the Lync Server Management Shell.</span></span>

<div>

## <a name="pstn-connectivity-cmdlets"></a><span data-ttu-id="0e627-108">Командлеты подключения PSTN</span><span class="sxs-lookup"><span data-stu-id="0e627-108">PSTN Connectivity Cmdlets</span></span>

<span data-ttu-id="0e627-109">Используйте указанные ниже командлеты, чтобы настроить различные аспекты подключения КТСОП.</span><span class="sxs-lookup"><span data-stu-id="0e627-109">Use the following cmdlets to configure various aspects of PSTN connectivity.</span></span>

<span data-ttu-id="0e627-110">**[Командлеты PSTN Gateway в Lync Server 2013](lync-server-2013-pstn-gateways-cmdlets.md)**</span><span class="sxs-lookup"><span data-stu-id="0e627-110">**[PSTN gateways cmdlets in Lync Server 2013](lync-server-2013-pstn-gateways-cmdlets.md)**</span></span>

  - <span></span>  
    <span data-ttu-id="0e627-111">[Set-CsPstnGateway](https://technet.microsoft.com/library/Gg398408(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="0e627-111">[Set-CsPstnGateway](https://technet.microsoft.com/library/Gg398408(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="0e627-112">[Test-CsPstnOutboundCall](https://technet.microsoft.com/library/Gg398207(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="0e627-112">[Test-CsPstnOutboundCall](https://technet.microsoft.com/library/Gg398207(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="0e627-113">[Test-CsPstnPeerToPeerCall](https://technet.microsoft.com/library/Gg398662(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="0e627-113">[Test-CsPstnPeerToPeerCall](https://technet.microsoft.com/library/Gg398662(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="0e627-114">[Set-CsMediationServer](https://technet.microsoft.com/library/Gg398213(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="0e627-114">[Set-CsMediationServer](https://technet.microsoft.com/library/Gg398213(v=OCS.15))</span></span>

<span data-ttu-id="0e627-115">**[Командлеты статической маршрутизации в Lync Server 2013](lync-server-2013-static-routing-cmdlets.md)**</span><span class="sxs-lookup"><span data-stu-id="0e627-115">**[Static routing cmdlets in Lync Server 2013](lync-server-2013-static-routing-cmdlets.md)**</span></span>

  - <span></span>  
    <span data-ttu-id="0e627-116">[Get-CsSipResponseCodeTranslationRule](https://technet.microsoft.com/library/Gg398130(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="0e627-116">[Get-CsSipResponseCodeTranslationRule](https://technet.microsoft.com/library/Gg398130(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="0e627-117">[New-CsSipResponseCodeTranslationRule](https://technet.microsoft.com/library/Gg413041(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="0e627-117">[New-CsSipResponseCodeTranslationRule](https://technet.microsoft.com/library/Gg413041(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="0e627-118">[Remove-CsSipResponseCodeTranslationRule](https://technet.microsoft.com/library/Gg412932(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="0e627-118">[Remove-CsSipResponseCodeTranslationRule](https://technet.microsoft.com/library/Gg412932(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="0e627-119">[Set-CsSipResponseCodeTranslationRule](https://technet.microsoft.com/library/Gg425895(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="0e627-119">[Set-CsSipResponseCodeTranslationRule](https://technet.microsoft.com/library/Gg425895(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="0e627-120">[New-CsStaticRoute](https://technet.microsoft.com/library/Gg398265(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="0e627-120">[New-CsStaticRoute](https://technet.microsoft.com/library/Gg398265(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="0e627-121">[Get-CsStaticRoutingConfiguration](https://technet.microsoft.com/library/Gg398754(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="0e627-121">[Get-CsStaticRoutingConfiguration](https://technet.microsoft.com/library/Gg398754(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="0e627-122">[New-CsStaticRoutingConfiguration](https://technet.microsoft.com/library/Gg425811(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="0e627-122">[New-CsStaticRoutingConfiguration](https://technet.microsoft.com/library/Gg425811(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="0e627-123">[Remove-CsStaticRoutingConfiguration](https://technet.microsoft.com/library/Gg398668(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="0e627-123">[Remove-CsStaticRoutingConfiguration](https://technet.microsoft.com/library/Gg398668(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="0e627-124">[Set-CsStaticRoutingConfiguration](https://technet.microsoft.com/library/Gg398724(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="0e627-124">[Set-CsStaticRoutingConfiguration](https://technet.microsoft.com/library/Gg398724(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="0e627-125">[New-CsSipProxyCustom](https://technet.microsoft.com/library/Gg425904(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="0e627-125">[New-CsSipProxyCustom](https://technet.microsoft.com/library/Gg425904(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="0e627-126">[New-CsSipProxyRealm](https://technet.microsoft.com/library/Gg413084(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="0e627-126">[New-CsSipProxyRealm](https://technet.microsoft.com/library/Gg413084(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="0e627-127">[New-CsSipProxyTCP](https://technet.microsoft.com/library/Gg425745(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="0e627-127">[New-CsSipProxyTCP](https://technet.microsoft.com/library/Gg425745(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="0e627-128">[New-CsSipProxyTLS](https://technet.microsoft.com/library/Gg398629(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="0e627-128">[New-CsSipProxyTLS](https://technet.microsoft.com/library/Gg398629(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="0e627-129">[New-CsSipProxyTransport](https://technet.microsoft.com/library/Gg398489(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="0e627-129">[New-CsSipProxyTransport](https://technet.microsoft.com/library/Gg398489(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="0e627-130">[New-CsSipProxyUseDefault](https://technet.microsoft.com/library/Gg398274(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="0e627-130">[New-CsSipProxyUseDefault](https://technet.microsoft.com/library/Gg398274(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="0e627-131">[New-CsSipProxyUseDefaultCert](https://technet.microsoft.com/library/Gg425858(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="0e627-131">[New-CsSipProxyUseDefaultCert](https://technet.microsoft.com/library/Gg425858(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="0e627-132">[New-CsIssuedCertId](https://technet.microsoft.com/library/Gg425814(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="0e627-132">[New-CsIssuedCertId](https://technet.microsoft.com/library/Gg425814(v=OCS.15))</span></span>

<span data-ttu-id="0e627-133">**[Командлеты конфигурации для магистрали в Lync Server 2013](lync-server-2013-trunking-configuration-cmdlets.md)**</span><span class="sxs-lookup"><span data-stu-id="0e627-133">**[Trunking configuration cmdlets in Lync Server 2013](lync-server-2013-trunking-configuration-cmdlets.md)**</span></span>

  - <span data-ttu-id="0e627-134">[Test-CsInterTrunkRouting](https://technet.microsoft.com/library/JJ204741(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="0e627-134">[Test-CsInterTrunkRouting](https://technet.microsoft.com/library/JJ204741(v=OCS.15))</span></span>

<!-- end list -->

  - <span data-ttu-id="0e627-135">[Get-CsOutboundCallingNumberTranslationRule](https://technet.microsoft.com/library/JJ204962(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="0e627-135">[Get-CsOutboundCallingNumberTranslationRule](https://technet.microsoft.com/library/JJ204962(v=OCS.15))</span></span>

  - <span data-ttu-id="0e627-136">[New-CsOutboundCallingNumberTranslationRule](https://technet.microsoft.com/library/JJ205097(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="0e627-136">[New-CsOutboundCallingNumberTranslationRule](https://technet.microsoft.com/library/JJ205097(v=OCS.15))</span></span>

  - <span data-ttu-id="0e627-137">[Remove-CsOutboundCallingNumberTranslationRule](https://technet.microsoft.com/library/JJ204836(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="0e627-137">[Remove-CsOutboundCallingNumberTranslationRule](https://technet.microsoft.com/library/JJ204836(v=OCS.15))</span></span>

  - <span data-ttu-id="0e627-138">[Set-CsOutboundCallingNumberTranslationRule](https://technet.microsoft.com/library/JJ205400(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="0e627-138">[Set-CsOutboundCallingNumberTranslationRule](https://technet.microsoft.com/library/JJ205400(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="0e627-139">[Get-CsOutboundTranslationRule](https://technet.microsoft.com/library/Gg398104(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="0e627-139">[Get-CsOutboundTranslationRule](https://technet.microsoft.com/library/Gg398104(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="0e627-140">[New-CsOutboundTranslationRule](https://technet.microsoft.com/library/Gg412803(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="0e627-140">[New-CsOutboundTranslationRule](https://technet.microsoft.com/library/Gg412803(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="0e627-141">[Remove-CsOutboundTranslationRule](https://technet.microsoft.com/library/Gg398556(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="0e627-141">[Remove-CsOutboundTranslationRule](https://technet.microsoft.com/library/Gg398556(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="0e627-142">[Set-CsOutboundTranslationRule](https://technet.microsoft.com/library/Gg413073(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="0e627-142">[Set-CsOutboundTranslationRule](https://technet.microsoft.com/library/Gg413073(v=OCS.15))</span></span>

<!-- end list -->

  - <span data-ttu-id="0e627-143">[Get-CsTrunk](https://technet.microsoft.com/library/JJ205244(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="0e627-143">[Get-CsTrunk](https://technet.microsoft.com/library/JJ205244(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="0e627-144">[Get-CsTrunkConfiguration](https://technet.microsoft.com/library/Gg398224(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="0e627-144">[Get-CsTrunkConfiguration](https://technet.microsoft.com/library/Gg398224(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="0e627-145">[New-CsTrunkConfiguration](https://technet.microsoft.com/library/Gg413021(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="0e627-145">[New-CsTrunkConfiguration](https://technet.microsoft.com/library/Gg413021(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="0e627-146">[Remove-CsTrunkConfiguration](https://technet.microsoft.com/library/Gg425943(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="0e627-146">[Remove-CsTrunkConfiguration](https://technet.microsoft.com/library/Gg425943(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="0e627-147">[Set-CsTrunkConfiguration](https://technet.microsoft.com/library/Gg398238(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="0e627-147">[Set-CsTrunkConfiguration](https://technet.microsoft.com/library/Gg398238(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="0e627-148">[Test-CsTrunkConfiguration](https://technet.microsoft.com/library/Gg398137(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="0e627-148">[Test-CsTrunkConfiguration](https://technet.microsoft.com/library/Gg398137(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="0e627-149">[New-CsVoiceRegex](https://technet.microsoft.com/library/Gg412751(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="0e627-149">[New-CsVoiceRegex](https://technet.microsoft.com/library/Gg412751(v=OCS.15))</span></span>

<span data-ttu-id="0e627-150">**[Командлеты голосовой маршрутизации в Lync Server 2013](lync-server-2013-voice-routing-cmdlets.md)**</span><span class="sxs-lookup"><span data-stu-id="0e627-150">**[Voice routing cmdlets in Lync Server 2013](lync-server-2013-voice-routing-cmdlets.md)**</span></span>

  - <span></span>  
    <span data-ttu-id="0e627-151">[Get-CsRoutingConfiguration](https://technet.microsoft.com/library/Gg425851(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="0e627-151">[Get-CsRoutingConfiguration](https://technet.microsoft.com/library/Gg425851(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="0e627-152">[New-CsRoutingConfiguration](https://technet.microsoft.com/library/Gg399056(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="0e627-152">[New-CsRoutingConfiguration](https://technet.microsoft.com/library/Gg399056(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="0e627-153">[Remove-CsRoutingConfiguration](https://technet.microsoft.com/library/Gg398643(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="0e627-153">[Remove-CsRoutingConfiguration](https://technet.microsoft.com/library/Gg398643(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="0e627-154">[Set-CsRoutingConfiguration](https://technet.microsoft.com/library/Gg412811(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="0e627-154">[Set-CsRoutingConfiguration](https://technet.microsoft.com/library/Gg412811(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="0e627-155">[Get-CsVoiceRoute](https://technet.microsoft.com/library/Gg425926(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="0e627-155">[Get-CsVoiceRoute](https://technet.microsoft.com/library/Gg425926(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="0e627-156">[New-CsVoiceRoute](https://technet.microsoft.com/library/Gg398197(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="0e627-156">[New-CsVoiceRoute](https://technet.microsoft.com/library/Gg398197(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="0e627-157">[Remove-CsVoiceRoute](https://technet.microsoft.com/library/Gg398468(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="0e627-157">[Remove-CsVoiceRoute](https://technet.microsoft.com/library/Gg398468(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="0e627-158">[Set-CsVoiceRoute](https://technet.microsoft.com/library/Gg412893(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="0e627-158">[Set-CsVoiceRoute](https://technet.microsoft.com/library/Gg412893(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="0e627-159">[Test-CsVoiceRoute](https://technet.microsoft.com/library/Gg425873(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="0e627-159">[Test-CsVoiceRoute](https://technet.microsoft.com/library/Gg425873(v=OCS.15))</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="0e627-160">См. также</span><span class="sxs-lookup"><span data-stu-id="0e627-160">See Also</span></span>


[<span data-ttu-id="0e627-161">Блог Lync Server PowerShell</span><span class="sxs-lookup"><span data-stu-id="0e627-161">Lync Server PowerShell Blog</span></span>](https://go.microsoft.com/fwlink/p/?linkid=203150)  
  

<span data-ttu-id="0e627-162"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0e627-162"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

