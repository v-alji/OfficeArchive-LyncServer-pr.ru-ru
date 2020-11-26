---
title: 'Lync Server 2013: делегирование'
description: 'Lync Server 2013: делегирование.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delegation
ms:assetid: 89e76e5c-3cfb-4504-8d0d-7509c8ba9815
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994045(v=OCS.15)
ms:contentKeyID: 51803956
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6dc25d0ea3dfd64ee1b71677e6bac55c1cb1ca32
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430744"
---
# <a name="delegation-in-lync-server-2013"></a>Делегирование в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2013-03-09_

Возможности делегирования в Lync влияют на Location-Based маршрутизации следующим образом:

  - Если представитель, включенный для Location-Based маршрутизации, помещает звонок от имени руководителя, для авторизации звонка используется политика голосовой связи представителя, а для направления звонка используется политика маршрутизации голосовой связи на сайте.

  - Что касается исходящих звонков ТСОП диспетчеру, действуют те же правила, регламентирующие переадресацию звонков и порядок обработки одновременных звонков, что и в соответствующих разделах.

  - Когда делегат устанавливает конечную точку ТСОП в качестве точки назначения одновременных звонков для входящих звонков в адрес диспетчера, для маршрутизации звонка на конечную точку ТСОП делегата используется политика маршрутизации голосовых звонков сетевого сайта, связанного с входящей магистралью.

  - Для целей делегирования, как правило, рекомендуется, чтобы диспетчер и связанные с ним делегаты находились на одном сетевом сайте.

<div>

## <a name="see-also"></a>См. также


[Сценарии маршрутизации на основе местоположения в Lync Server 2013](lync-server-2013-scenarios-for-location-based-routing.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

