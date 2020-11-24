---
title: 'Lync Server 2013: создание или изменение объекта контакта устройства конференц-связи'
description: 'Lync Server 2013: создание или изменение объекта контакта устройства конференц-связи.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or modify a conferencing device Contact object
ms:assetid: 62ed64be-379c-417d-9453-511881cf5604
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994035(v=OCS.15)
ms:contentKeyID: 51803945
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 853ee1c7dfda2fda99431b8cc1a5210a51f39a4e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398776"
---
# <a name="create-or-modify-a-conferencing-device-contact-object-in-lync-server-2013"></a>Создание или изменение объекта контакта устройства конференц-связи в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2013-10-02_

Чтобы создать объект комнаты конференц-связи, сначала создайте учетную запись пользователя Active Directory для представления устройства. Затем используйте командлет **Enable-CsMeetingRoom** , чтобы разрешить этой учетной записи работать в качестве устройства конференций. Если вам нужно изменить свойства существующего устройства конференц-связи, используйте командлет **Set – CsMeetingRoom** .

Эти командлеты можно запускать либо из командной консоли Lync Server 2013, либо из удаленного сеанса Windows PowerShell.

<div>


> [!NOTE]  
> Подробнее об использовании удаленной оболочки Windows PowerShell для подключения к серверу Lync Server можно найти в статье "Краткое руководство по работе с Microsoft Lync Server 2010 с помощью удаленной оболочки PowerShell" на веб-сервере Lync Server Windows PowerShell <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A> .



</div>

<div>


<div>

## <a name="creating-a-conferencing-device"></a>Создание устройства конференц-связи

  - После создания учетной записи пользователя Active Directory, которая представляет новое устройство для проведения конференций, включите ее с помощью командлета **Enable-CsMeetingRoom** . Убедитесь в том, что вы хотите добавить учетную запись, b) в пул регистраторов, в котором будет храниться счет комнаты и c) адрес SIP, назначаемый этой учетной записи. Например:
    
        Enable-CsMeetingRoom -Identity "Redmond Conferencing device" -RegistrarPool "atl-cs-001.litwareinc.com" -SipAddress "sip:RedmondMeetingRoom@litwareinc.com"

</div>

<div>

## <a name="modifying-a-conferencing-device"></a>Изменение устройства конференц-связи

  - Чтобы изменить значения свойств существующего устройства конференции, используйте командлет **Set-CsMeetingRoom** . Например, следующая команда обновляет номер телефона (LineUri), связанный с устройством конференц-связи:
    
        Set-CsMeetingRoom -Identity "Redmond Conferencing device" -LineUri "tel:+12065551219"

</div>

Подробные сведения можно найти в разделах справки по командлетам [Enable-CsMeetingRoom](https://docs.microsoft.com/powershell/module/skype/Enable-CsMeetingRoom) и командлету [Set-CsMeetingRoom](https://docs.microsoft.com/powershell/module/skype/Set-CsMeetingRoom) .

</div>

</div>

<span> </span>

</div>

</div>

</div>

