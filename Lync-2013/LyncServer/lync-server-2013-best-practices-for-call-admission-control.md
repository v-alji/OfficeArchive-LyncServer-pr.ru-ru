---
title: 'Lync Server 2013: рекомендации по контролю допуска звонков'
description: 'Lync Server 2013: советы и рекомендации по контролю за допуском звонков.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Best practices for call admission control
ms:assetid: 97173cca-8175-4ae2-a247-eb7ef809da93
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398770(v=OCS.15)
ms:contentKeyID: 48184913
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 17c32af904dc7fb48a1a5d1903bd6ed1f81f4cb3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436071"
---
# <a name="best-practices-for-call-admission-control-in-lync-server-2013"></a>Рекомендации по контролю допуска звонков в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-09-22_

Чтобы улучшить производительность и упростить развертывание, руководствуйтесь следующими рекомендациями при развертывании контроля допуска звонков.

  - Убедитесь, что глобальные сети соответствующим образом подготовлены для текущего и прогнозируемого трафика мультимедиа.
    
    <div>
    

    > [!NOTE]  
    > Мы рекомендуем учесть в ограничениях пропускной способности буфер. Существуют сценарии, такие как состояние гонки, которые затрагивают общую пропускную способность и могут привести к превышению предела пропускной способности. Например, при попытке запуска двух звонков в условиях приближения к пределу пропускной способности один из них может быть отклонен, так как другому удалось запуститься первым.

    
    </div>

  - Отслеживайте использование сети и записи регистрации вызовов, чтобы вы могли выбрать оптимальные параметры контроля допуска звонков и обновлять их по мере изменения использования сети.

  - Используйте политики пропускной способности контроля допуска звонков для настройки параметров качества обслуживания.

  - Если вы хотите перенаправлять заблокированные звонки в ТСОП, убедитесь в функциональных возможностях и обрабатывающих способностях ТСОП. Подробнее смотрите в разделе [Планирование исходящей маршрутизации голосовой связи в Lync Server 2013](lync-server-2013-planning-outbound-voice-routing.md).
    
    <div>
    

    > [!NOTE]  
    > Под емкостью понимается количество портов, которые требуется открыть для обеспечения поддержки потенциального объема перенаправлений в ТСОП.

    
    </div>

</div>

<span> </span>

</div>

</div>

</div>

