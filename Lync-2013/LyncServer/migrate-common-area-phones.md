---
title: Миграция телефонов общего пользования
description: Перенесите общие Телефоны на телефонную сеть.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migrate Common Area Phones
ms:assetid: 31bd26fc-861b-45c6-8221-18df16e575de
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688015(v=OCS.15)
ms:contentKeyID: 49733604
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1b8df4d94a3db3274df7e4e82ed2185c3626de12
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443827"
---
# <a name="migrate-common-area-phones"></a>Миграция телефонов общего пользования

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-09-29_

Обычные телефоны — это IP-телефоны, которые чаще всего находятся в общей рабочей области или в общей области, например в зале ожидания, кухни или фабрики. Для обеспечения функций UC для Lync Server не нужно подключаться к компьютеру с помощью обычных телефонов. После миграции развертывания Lync Server 2010 на Lync Server 2013 необходимо также перенести объекты контактов, связанные с устаревшим стандартным телефоном. С помощью командной консоли Lync Server вы сначала получите все объекты контактов, связанные с Lync Server 2010 Common Area Phone, а затем переместите эти объекты в пул Lync Server 2013.

**Миграция телефонов общего пользования**

1.  На сервере переднего плана Lync Server 2013 откройте консоль управления Lync Server.

2.  В командной строке введите следующую команду:
    
        Get-CsCommonAreaPhone -Filter {RegistrarPool -eq "pool01.contoso.net"} | Move-CsCommonAreaPhone -Target pool02.contoso.net

3.  Чтобы убедиться в том, что все объекты контакта были перемещены в пул Lync Server 2013, в командной консоли Lync Server Management Shell введите следующую команду:
    
        Get-CsCommonAreaPhone -Filter {RegistrarPool -eq "pool02.contoso.net"}
    
    Убедитесь, что все объекты контакта теперь связаны с пулом Lync Server 2013.

</div>

<span> </span>

</div>

</div>

</div>

