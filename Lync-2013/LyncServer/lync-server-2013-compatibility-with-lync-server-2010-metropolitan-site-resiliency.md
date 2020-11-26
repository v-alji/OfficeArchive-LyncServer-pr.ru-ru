---
title: Совместимость Lync Server 2013 с устойчивостью главного сайта Lync Server 2010
description: Совместимость с Lync Server 2013 с помощью устойчивости сайта Lync Server 2010 для одногородной связи.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Lync Server 2010 metropolitan site resiliency
ms:assetid: 18673ff6-b664-4a57-a89b-cbda8b129e6a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204715(v=OCS.15)
ms:contentKeyID: 48183526
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ec72f261ac593b24bad13dcd400f495ba7ba0722
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434608"
---
# <a name="lync-server-2010-metropolitan-site-resiliency"></a>Устойчивость главного сайта Lync Server 2010

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2014-03-19_

Решение для обеспечения устойчивости сайтов, поддерживающее для Lync Server 2010, не поддерживается для Lync Server 2013. Это решение вовлечено в объединение одного пула переднего плана в двух центрах обработки данных в одном регионе города.

Решение для обеспечения устойчивости сайтов с помощью этого типа разработано для восстановления после утраты полного центра обработки данных. При охвате пула в двух центрах обработки данных обычно размещается половина переднего плана в одном центре обработки данных и вторая половина во втором центре обработки данных. Если вы потеряли весь центр обработки данных, вы потеряли половину серверов переднего плана. Это может привести к возникновению проблем с новой моделью распределенной системы для пулов интерфейсов в Lync Server 2013. Дополнительные сведения можно найти [в разделе топологии и компоненты для серверов переднего плана, обмена мгновенными сообщениями и присутствия в Lync Server 2013](lync-server-2013-topologies-and-components-for-front-end-servers-instant-messaging-and-presence.md).

</div>

<span> </span>

</div>

</div>

</div>

