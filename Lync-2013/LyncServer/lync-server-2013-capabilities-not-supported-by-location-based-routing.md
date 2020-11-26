---
title: 'Lync Server 2013: функции, не поддерживаемые маршрутизацией на основе расположения'
description: 'Lync Server 2013: возможности, не поддерживаемые службой маршрутизации Location-Based.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Capabilities not supported by Location-Based Routing
ms:assetid: c3d54953-a7d6-4465-a6c3-ae411b2d8ea9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994071(v=OCS.15)
ms:contentKeyID: 51803982
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bf9cd03a8cbdd50e136605c4f172598b2ad3f523
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435609"
---
# <a name="capabilities-not-supported-by-location-based-routing-in-lync-server-2013"></a>Функции, не поддерживаемые маршрутизацией на основе расположения в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2014-03-12_

Location-Based маршрутизация не применяется к следующим типам взаимодействий. Если конечные точки Lync взаимодействуют с конечными точками PSTN с помощью этих возможностей, маршрутизация Location-Based не выполняется принудительно.

  - Конференции с телефонным подключением

  - Входящие и исходящие вызовы ТСОП через группу ответов

  - Парковка вызовов или преобразование вызовов ТСОП с помощью функции парковки вызовов

  - Входящие вызовы ТСОП в службу оповещений

  - Входящие вызовы ТСОП, преобразованные через групповой ответ на вызовы

Чтобы применить правила маршрутизации Location-Based к типам взаимодействия в следующем списке, необходимо включить Location-Based маршрутизацию для конференц-связи.

  - Исходящие вызовы по ТСОП из конференций

  - Эскалации из сеансов одноранговой голосовой связи к сеансам конференций с привлечением конечных точек ТСОП

  - Передачи после консультации с привлечением конечных точек ТСОП

Чтобы включить Location-Basedную маршрутизацию для конференц-связи, ознакомьтесь со сведениями [о маршрутизации на основе местоположения для конференций в Lync Server 2013](lync-server-2013-location-based-routing-for-conferencing.md).

<div>

## <a name="see-also"></a>См. также


[Планирование маршрутизации на основе местоположения в Lync Server 2013](lync-server-2013-planning-for-location-based-routing.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

