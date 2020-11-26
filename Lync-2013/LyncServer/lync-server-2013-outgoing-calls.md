---
title: 'Lync Server 2013: исходящие звонки'
description: 'Lync Server 2013: исходящие вызовы.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Outgoing calls
ms:assetid: 885ffe6f-cd51-4f21-8d4f-a1ff8d818858
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994049(v=OCS.15)
ms:contentKeyID: 51803960
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e14f19dec35a6da47a2ddd62657d5d087a854f16
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424837"
---
# <a name="outgoing-calls-in-lync-server-2013"></a>Исходящие звонки в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2013-03-09_

Маршрутизация исходящих вызовов пользователей, для которых разрешена Location-Based маршрутизация, зависит от расположения в сети для конечной точки пользователя. В следующей таблице показано, как маршрутизация Location-Based влияет на маршрутизацию исходящих вызовов в зависимости от расположения конечной точки вызывающего абонента.

### <a name="caller-placing-an-outbound-call-to-the-pstn"></a>Абонент размещает исходящий звонок ТСОП

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th>Конечная точка пользователя расположена на сетевом сайте, для которого включена маршрутизация на основе расположения</th>
<th>Конечная точка пользователя расположена на неизвестном сетевом сайте или на сайте, для которого не включена маршрутизация на основе расположения</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Авторизация исходящих звонков</p></td>
<td><p>Звонок авторизован на основе политики голосовой связи пользователя</p></td>
<td><p>Звонок авторизован на основе политики голосовой связи пользователя</p></td>
</tr>
<tr class="even">
<td><p>Маршрутизация исходящего звонка</p></td>
<td><p>Звонок маршрутизируется в соответствии с политикой маршрутизации голосовой связи для данного сетевого сайта</p></td>
<td><p>Звонок маршрутизируется в соответствии с политикой голосовой связи пользователя и только через магистрали, для которых не включена маршрутизация на основе расположения (если они доступны)</p></td>
</tr>
</tbody>
</table>


<div>

## <a name="see-also"></a>См. также


[Сценарии маршрутизации на основе местоположения в Lync Server 2013](lync-server-2013-scenarios-for-location-based-routing.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

