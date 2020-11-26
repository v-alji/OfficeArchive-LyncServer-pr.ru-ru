---
title: Повторная активация сервера после закрытия портов в IIS мастером настройки безопасности
description: После того как мастер настройки безопасности закроет порт в службах IIS, повторно активируйте сервер.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Re-activate server after Security Configuration Wizard closes ports in IIS
ms:assetid: cb8e17cf-f8c1-4099-b63b-c242d656c26a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398851(v=OCS.15)
ms:contentKeyID: 48185644
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d824845a7f89c28087a7b5d180a6ed017cb47ade
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436722"
---
# <a name="re-activate-server-after-security-configuration-wizard-closes-ports-in-iis"></a>Повторная активация сервера после закрытия портов в IIS мастером настройки безопасности

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-10-01_

Некоторые роли Lync Server 2013 работают на веб-службах на порте служб IIS 4443. При запуске мастера развертывания Lync Server, Bootstrapper.exe или с помощью командлета **Enable-CsComputer** создается в брандмауэре исключение и открывается порт. Если вы запустите мастер настройки безопасности Windows Server 2008 R2 (или другие сценарии защиты), порт 4443 будет заблокирован, а внешние клиенты не смогут обращаться к веб-службам. Чтобы снова открыть порт, вы можете либо изменить исключение межсетевого экрана напрямую, либо повторно активировать сервер.

<div>

## <a name="to-re-activate-the-server-by-using-the-deployment-wizard"></a>Повторная активация сервера с помощью мастера развертывания

1.  На странице мастера развертывания Lync Server нажмите кнопку **выполнить** рядом с **шагом 2: Настройка или удаление компонентов Lync Server**.

2.  На странице **настройки серверных компонентов Lync** нажмите кнопку **Далее**.

3.  На странице **выполнение команд** после того, как состояние задачи отображается как завершенное, нажмите кнопку **Готово**.
    
    <div>
    

    > [!NOTE]
    > Вы также можете повторно активировать сервер с помощью bootstrapper.exe или <STRONG>Enable-CsComputer</STRONG> .

    
    </div>

</div>

</div>

<span> </span>

</div>

</div>

</div>

