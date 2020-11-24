---
title: 'Lync Server 2013: Общие сведения о маршрутизации Location-Based'
description: 'Lync Server 2013: Общие сведения о маршрутизации Location-Based.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Overview of Location-Based Routing
ms:assetid: 4aa494bd-0d66-4335-b9e8-f758d44a7202
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994032(v=OCS.15)
ms:contentKeyID: 51803941
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0b1e026791a8562629231b91b58d7e7eff569ffa
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399679"
---
# <a name="overview-of-location-based-routing-in-lync-server-2013"></a>Общие сведения о маршрутизации Location-Based в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2013-02-21_

Маршрутизация на основе расположения вводит новый набор правил, который изменяет маршрутизацию местных и международных звонков на номер ТСОП для предотвращения обхода платных звонков. Маршрутизация на основе расположения предоставляет гибкость для анализа этих правил в пределах определенных областей, шлюзов или только наборов пользователей.

В следующих сценариях показаны основные типы ограничений, которые Location-Based маршрутизации может принудительно применять:

  - Входящие звонки – Location-Based маршрутизация может принудительно применять исходящие вызовы для выхода с шлюза PSTN, который находится в той же области, что и вызывающий объект, чтобы предотвратить бесплатный звонок, что предотвращает звонки с шлюза PSTN, находящегося в другом регионе, в качестве вызывающего абонента.

  - Входные звонки – Location-Based маршрутизация может препятствовать входящим звонкам КТСОП для звонков в конечные точки Lync, если маршрутизация шлюза PSTN не находится в том же регионе, что и у вызываемого пользователя Lync.

  - Неизвестные регионы: Location-Based маршрутизация ограничивает входящие и исходящие звонки по протоколу PSTN между пользователями, которые находятся в неопределенном расположении (например, удаленные пользователи, подключающиеся из Интернета или расположенные в неизвестных регионах).

  - Международные регионы: Маршрутизация Location-Based принудительно обеспечивает маршрутизацию исходящих звонков через международные шлюзы PSTN, если не удается найти шлюз, локальный для которого нужно указать расположение пользователя.

<div>

## <a name="see-also"></a>См. также


[Планирование маршрутизации на основе местоположения в Lync Server 2013](lync-server-2013-planning-for-location-based-routing.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

