---
title: 'Lync Server 2013: Включение и отключение устройства для конференц-связи'
description: 'Lync Server 2013: Включение и отключение устройства для конференц-связи.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enable or disable a conferencing device
ms:assetid: d5140e38-d015-4706-9bde-cf2fa748c36b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994070(v=OCS.15)
ms:contentKeyID: 51803981
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 761bc19536c889cced68ff586753f6800df0da59
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437576"
---
# <a name="enable-or-disable-a-conferencing-device-in-lync-server-2013"></a><span data-ttu-id="8a122-103">Включение и отключение устройства конференц-связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8a122-103">Enable or disable a conferencing device in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8a122-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8a122-104">

<span> </span></span></span>

<span data-ttu-id="8a122-105">_**Тема последнего изменения:** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="8a122-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="8a122-106">Включать и отключать устройства конференц-связи с помощью командлета **Enable – CsMeetingRoom** и командлета **Disable-CsMeetingRoom** .</span><span class="sxs-lookup"><span data-stu-id="8a122-106">Enable and disable a conferencing device by using the **Enable-CsMeetingRoom** cmdlet and the **Disable-CsMeetingRoom** cmdlet.</span></span> <span data-ttu-id="8a122-107">Эти командлеты можно запускать либо из командной консоли Lync Server 2013, либо из удаленного сеанса Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8a122-107">These cmdlets can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="8a122-108">Подробнее об использовании удаленной оболочки Windows PowerShell для подключения к серверу Lync Server можно найти в статье "Краткое руководство по работе с Microsoft Lync Server 2010 с помощью удаленной оболочки PowerShell" на веб-сервере Lync Server Windows PowerShell <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A> .</span><span class="sxs-lookup"><span data-stu-id="8a122-108">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A>.</span></span>



</div>

<div>


<div>

## <a name="enabling-a-conferencing-device"></a><span data-ttu-id="8a122-109">Включение устройства для конференц-связи</span><span class="sxs-lookup"><span data-stu-id="8a122-109">Enabling a Conferencing Device</span></span>

  - <span data-ttu-id="8a122-110">Чтобы включить устройство для проведения конференций, используйте командлет **Enable-CsMeetingRoom** .</span><span class="sxs-lookup"><span data-stu-id="8a122-110">To enable a conferencing device, use the **Enable-CsMeetingRoom** cmdlet.</span></span> <span data-ttu-id="8a122-111">При включении устройства для конференц-связи необходимо включить в него удостоверение устройства конференц-связи, b) пула регистраторов, в котором будет храниться учетная запись комнаты, и c) адрес SIP, назначаемый этой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="8a122-111">When enabling a conferencing device, you must include a) the conferencing device identity, b) the Registrar pool where the room account will be homed, and c) the SIP address to be assigned to that account.</span></span>
    
        Enable-CsMeetingRoom -Identity "Redmond Conferencing device" -RegistrarPool "atl-cs-001.litwareinc.com" -SipAddress "sip:RedmondMeetingRoom@litwareinc.com"

</div>

<div>

## <a name="disabling-a-conferencing-device"></a><span data-ttu-id="8a122-112">Отключение устройства конференц-связи</span><span class="sxs-lookup"><span data-stu-id="8a122-112">Disabling a Conferencing Device</span></span>

  - <span data-ttu-id="8a122-113">Чтобы отключить устройство для проведения конференций, используйте командлет **Disable-CsMeetingRoom** .</span><span class="sxs-lookup"><span data-stu-id="8a122-113">To disable a conferencing device, use the **Disable-CsMeetingRoom** cmdlet.</span></span> <span data-ttu-id="8a122-114">Убедитесь в том, что вы указали, что устройство конференц-связи будет отключено:</span><span class="sxs-lookup"><span data-stu-id="8a122-114">Make sure that you specify the identity of the conferencing device to be disabled:</span></span>
    
        Disable-CsMeetingRoom -Identity "sip:RedmondMeetingRoom@litwareinc.com"

</div>

<span data-ttu-id="8a122-115">Подробные сведения можно найти в разделах справки по командлетам [Enable-CsMeetingRoom](https://docs.microsoft.com/powershell/module/skype/Enable-CsMeetingRoom) и командлету [Disable-CsMeetingRoom](https://docs.microsoft.com/powershell/module/skype/Disable-CsMeetingRoom) .</span><span class="sxs-lookup"><span data-stu-id="8a122-115">For details, see the Help topics for the [Enable-CsMeetingRoom](https://docs.microsoft.com/powershell/module/skype/Enable-CsMeetingRoom) cmdlet and the [Disable-CsMeetingRoom](https://docs.microsoft.com/powershell/module/skype/Disable-CsMeetingRoom) cmdlet.</span></span>

<span data-ttu-id="8a122-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8a122-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

