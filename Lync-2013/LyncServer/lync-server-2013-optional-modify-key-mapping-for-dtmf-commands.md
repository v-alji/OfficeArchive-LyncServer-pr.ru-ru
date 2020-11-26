---
title: 'Lync Server 2013: изменение назначенных клавиш для команд DTMF (необязательно)'
description: 'Lync Server 2013: (необязательно) измените сопоставление ключей для команд DTMF.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: (Optional) Modify key mapping for DTMF commands
ms:assetid: d753b78d-400c-4df2-957f-e7576b2019c2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398943(v=OCS.15)
ms:contentKeyID: 48185563
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7581001c31d929163962378a8734435f6d07c6c8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424893"
---
# <a name="optional-modify-key-mapping-for-dtmf-commands-in-lync-server-2013"></a>Изменение назначенных клавиш для команд DTMF в Lync Server 2013 (необязательно)

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-09-30_

Пользователи конференц-связи с телефонным подключением могут использовать клавиши на клавиатуре телефона для выполнения команд DTMF. Команды DTMF позволяют пользователям, подключающимся к конференции по телефону, управлять параметрами конференции (например, включением и отключением звука микрофона или блокированием и снятием блокировки конференции) с помощью клавиатуры телефона. Вы можете использовать командлеты для изменения ключей, используемых для команд DTMF. Этот шаг является необязательным.

<div>


> [!NOTE]  
> Подробнее об этих командлетах и возможных параметрах DTMF можно найти в разделе Документация оболочки управления Lync Server или командной консоли Lync Server Management Shell.



</div>

<div>

## <a name="to-modify-the-key-mapping-of-dtmf-commands"></a>Изменение сопоставления клавиш для команд DTMF

1.  Войдите в систему под учетной записью члена группы **RTCUniversalServerAdmins** или члена роли **CS-ServerAdministrator** или **CsAdministrator** .

2.  Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.

3.  Выполните следующую команду в командной строке:
    
        Get-CsDialinConferencingDtmfConfiguration
    
    Этот командлет возвращает параметры DTMF, используемые для конференц-связи с телефонным подключением.

4.  Выполните следующий командлет и укажите клавишу, которую нужно нажимать для каждого параметра, который вы хотите изменить.
    
        Set-CsDialinConferencingDtmfConfiguration [-Identity <global or site collection to be changed>]
        [-AdmitAll <default key is 8>] [-AudienceMuteCommand <default key is 4>]
        [-CommandCharacter <* (default) | #>] [-EnableDisableAnnouncementsCommand <default key is 9>]
        [-HelpCommand <default key is 1>] [-LockUnlockConferenceCommand <default key is 7>]
        [-MuteUnmuteCommand <default key is 6>] [-PrivateRollCallCommand <default key is 3>]
    
    Этот командлет изменяет параметры DTMF, используемые для конференц-связи с телефонным подключением.
    
    Например:
    
        Set-CsDialinConferencingDtmfConfiguration -EnableDisableAnnouncementsCommand 4 -AudienceMuteCommand 9
    
    В этом примере заменяется клавиша, нажатная для включения или отключения объявлений, и нажатие клавиши, позволяющей отключить Микрофоны всех участников. Поскольку удостоверение не задано, эти изменения применяются к глобальным параметрам DTMF.

5.  (Дополнительно). Чтобы создать дополнительные наборы команд DTMF для конкретных сайтов, используйте командлет **New-CsDialinConferencingDtmfConfiguration**, указав идентификатор сайта. При создании новых параметров DTMF для сайтов эти параметры сайтов имеют приоритет перед глобальными параметрами. Дополнительные сведения можно найти в разделе Документация оболочки управления Lync Server или командной строки оболочки Lync Server Management Shell.

</div>

</div>

<span> </span>

</div>

</div>

</div>

