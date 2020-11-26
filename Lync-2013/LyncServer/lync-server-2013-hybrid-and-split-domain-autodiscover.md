---
title: 'Lync Server 2013: гибридный и разделяемый домен — автообнаружения'
description: 'Lync Server 2013: гибридные и разделяемые доменные возможности автообнаружения.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Hybrid and split-domain - Autodiscover
ms:assetid: c855bcc5-b656-4d2d-92d6-f016f2797d3a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945652(v=OCS.15)
ms:contentKeyID: 51541520
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 972233fd10d2b68a002d2d3a203f61bb0bd29574
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427441"
---
# <a name="hybrid-and-split-domain---autodiscover-in-lync-server-2013"></a>Гибридная и Разделяемая доменные возможности автообнаружения в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2013-02-14_

Общее адресное пространство SIP, также называемое развертыванием с *разделением доменов* или *гибридным* развертыванием, — это конфигурация, в которой пользователи развертываются в рамках локального развертывания и из Интернета. Желаемый результат состоит в том, что пользователь вне зависимости от того, где расположен домашний сервер (локально или в сети), подключается к развертыванию и перенаправляется на место своего домашнего сервера. Для этого функция автообнаружения в Lync Server 2013 используется для перенаправления пользователя Online в сетевую топологию. Это можно сделать, настроив указатель URL-адреса автообнаружения с помощью командной консоли Lync Server Management Shell, командлета **Get-CsHostingProvider** и командлета **Set-CsHostingProvider** .

<div>

## <a name="mobility-for-the-split-domain-deployment"></a>Мобильность для раздельного развертывания доменов

Вам потребуется собрать и записать следующие развернутые атрибуты:

  - В командной консоли Lync Server введите
    
        Get-CsHostingProvider

  - В результатах найдите Интернет-провайдер с атрибутом **ProxyFQDN**. Например, sipfed.online.lync.com.

  - Запишите значение параметра ProxyFQDN.

  - Включите Федерацию в локальной панели управления Lync Server и разрешите Федерацию с помощью веб-поставщика.

  - Включите Федерацию для поставщика услуг Интернета. По умолчанию все пользователи в сети включены в доменную Федерацию и могут взаимодействовать со всеми доменами.

  - Если вы определяете блокируемые и разрешенные домены, определите домены, которые будут явно разрешены или явным образом заблокированы.

  - Для службы интеграции с Интернетом необходимо планировать исключения брандмауэра, сертификаты и узел DNS (A или AAAA, если используется IPv6). Кроме того, необходимо настроить политики Федерации. Подробные сведения можно найти в разделе [планирование для Lync server 2013 и Office Communications Server Federation](lync-server-2013-planning-for-lync-server-and-office-communications-server-federation.md).

</div>

</div>

<span> </span>

</div>

</div>

</div>

