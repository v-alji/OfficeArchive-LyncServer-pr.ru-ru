---
title: 'Lync Server 2013: Настройка службы Mobility Service для высокой производительности'
description: 'Lync Server 2013: Настройка службы Mobility Service для обеспечения высокой производительности.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Mobility Service for high performance
ms:assetid: c2b8aadb-cffb-49f0-ba7a-e8541a1ff475
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690042(v=OCS.15)
ms:contentKeyID: 48185332
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4732d9f6a92c383a105a6f0d7162c9b6c798de24
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432886"
---
# <a name="configuring-mobility-service-for-high-performance-in-lync-server-2013"></a>Настройка службы Mobility Service для высокой производительности в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2013-02-17_

<div>


> [!IMPORTANT]  
> Этот раздел относится только к службе мобильной связи Lync Server 2013 (MCX) и не применяется к веб-API единой системы обмена сообщениями (UCWA), как в накопительных обновлениях для Lync Server 2013: Февраль 2013.



</div>

При установке службы Mobility Service (MCX) в службах IIS 7,5 программа установки службы Mobility Service настраивает некоторые параметры быстродействия на сервере переднего плана. We recommend that you use IIS 7.5 for mobility. The settings affect the maximum number of concurrent user requests and the maximum number of threads that are allowed for the Mobility Service.

Далее представлены параметры производительности:

<div>

## <a name="settings-for-mcx-on-iis-75"></a>Параметры для Mcx в службе IIS 7.5

1.  **maxConcurrentThreadsPerCPU** имеет значение нуля (0).

2.  **maxConcurrentRequestsPerCPU** имеет значение нуля (0).

3.  Процессная модель ASP.NET имеет значение AutoConfig (только для IIS 7.5).

4.  Предел очереди HTTP.sys имеет значение 1000 (по умолчанию).

</div>

</div>

<span> </span>

</div>

</div>

</div>

