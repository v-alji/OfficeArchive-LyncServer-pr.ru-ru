---
title: 'Lync Server 2013: удаление файлов обновлений устройств, не связанных с устройством'
description: 'Lync Server 2013: удаление файлов обновлений устройств, не связанных с устройством.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Remove Device Update files not associated with a device
ms:assetid: ecebbf73-b456-4990-a91d-308b84d39404
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994084(v=OCS.15)
ms:contentKeyID: 51803996
ms.date: 12/12/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8338f7274d1d27e2290d822324986238f4856fe4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436407"
---
# <a name="remove-device-update-files-not-associated-with-a-device-in-lync-server-2013"></a>Удаление файлов обновления устройства, не связанных с устройством в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2013-02-20_

Каждый раз, когда новые обновления устройства загружаются в систему, создается соответствующее правило обновления устройства. По умолчанию новые правила обновления устройства назначаются в состояние ожидания. Это означает, что правила можно загрузить и установить на тестовые устройства, но не на производственные устройства, что позволит вам тестировать обновления перед их предоставлением пользователям. На основании тестов вы принимаете и разворачиваете или отклоняете и удаляете обновление. Когда вы отклоняете обновление, обновление устройства не связано с его правилом обновления устройства.

<div>


Файлы обновления устройства, которые больше не связаны с устройством, можно удалить с помощью Windows PowerShell и командлета **clear-CsDeviceUpdateFile** . Этот командлет можно выполнить либо из управляющей оболочки Lync Server 2013, либо из удаленного сеанса Windows PowerShell.

<div>


> [!NOTE]  
> Подробнее об использовании удаленной оболочки Windows PowerShell для подключения к серверу Lync Server можно найти в статье "Краткое руководство по работе с Microsoft Lync Server 2010 с помощью удаленной оболочки PowerShell" на веб-сервере Lync Server Windows PowerShell <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A> .



</div>

<div>


  - Например, следующая команда удаляет все правила обновления устройства на веб-сервере atl-cs-001.litwareinc.com, которые больше не связаны с устройством.
    
        Clear-CsDeviceUpdateFile -Identity "service:WebServer:atl-cs-001.litwareinc.com"

</div>

Дополнительные сведения можно найти в разделе справки по командлету [clear-CsDeviceUpdateFile](https://docs.microsoft.com/powershell/module/skype/Clear-CsDeviceUpdateFile) .

</div>

</div>

<span> </span>

</div>

</div>

</div>

