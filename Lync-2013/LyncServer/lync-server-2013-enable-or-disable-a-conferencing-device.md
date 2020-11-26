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
# <a name="enable-or-disable-a-conferencing-device-in-lync-server-2013"></a>Включение и отключение устройства конференц-связи в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2013-02-20_

Включать и отключать устройства конференц-связи с помощью командлета **Enable – CsMeetingRoom** и командлета **Disable-CsMeetingRoom** . Эти командлеты можно запускать либо из командной консоли Lync Server 2013, либо из удаленного сеанса Windows PowerShell.

<div>


> [!NOTE]  
> Подробнее об использовании удаленной оболочки Windows PowerShell для подключения к серверу Lync Server можно найти в статье "Краткое руководство по работе с Microsoft Lync Server 2010 с помощью удаленной оболочки PowerShell" на веб-сервере Lync Server Windows PowerShell <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A> .



</div>

<div>


<div>

## <a name="enabling-a-conferencing-device"></a>Включение устройства для конференц-связи

  - Чтобы включить устройство для проведения конференций, используйте командлет **Enable-CsMeetingRoom** . При включении устройства для конференц-связи необходимо включить в него удостоверение устройства конференц-связи, b) пула регистраторов, в котором будет храниться учетная запись комнаты, и c) адрес SIP, назначаемый этой учетной записи.
    
        Enable-CsMeetingRoom -Identity "Redmond Conferencing device" -RegistrarPool "atl-cs-001.litwareinc.com" -SipAddress "sip:RedmondMeetingRoom@litwareinc.com"

</div>

<div>

## <a name="disabling-a-conferencing-device"></a>Отключение устройства конференц-связи

  - Чтобы отключить устройство для проведения конференций, используйте командлет **Disable-CsMeetingRoom** . Убедитесь в том, что вы указали, что устройство конференц-связи будет отключено:
    
        Disable-CsMeetingRoom -Identity "sip:RedmondMeetingRoom@litwareinc.com"

</div>

Подробные сведения можно найти в разделах справки по командлетам [Enable-CsMeetingRoom](https://docs.microsoft.com/powershell/module/skype/Enable-CsMeetingRoom) и командлету [Disable-CsMeetingRoom](https://docs.microsoft.com/powershell/module/skype/Disable-CsMeetingRoom) .

</div>

</div>

<span> </span>

</div>

</div>

</div>

