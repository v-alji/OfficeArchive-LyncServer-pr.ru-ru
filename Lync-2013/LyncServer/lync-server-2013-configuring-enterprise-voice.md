---
title: 'Lync Server 2013: Настройка корпоративной голосовой связи'
description: 'Lync Server 2013: Настройка корпоративной голосовой связи.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Enterprise Voice
ms:assetid: 7df179fa-d3a2-4b23-a433-b750aedf980b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994041(v=OCS.15)
ms:contentKeyID: 51803952
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 49a231b92bf7b04aa3466927a79258f0cbad4e3f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433124"
---
# <a name="configuring-enterprise-voice-in-lync-server-2013"></a>Настройка корпоративной голосовой связи в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2013-03-12_

Для развертывания корпоративной голосовой связи необходимо настроить указанные ниже параметры.

  - Создание магистрали

  - Определение политики голосовой связи

  - Определение голосового маршрута

  - Enable Users for Enterprise Voice

<div>

## <a name="create-a-trunk"></a>Создание магистрали

Вы должны определить в развертывании своей корпоративной голосовой сети магистральные магистрали. Для маршрутизации Location-Based необходимо создать конфигурацию магистральной магистрали для каждой магистрали. Используйте построитель топологии Lync Server для определения ваших каналов и используйте команду Lync Server Windows PowerShell New-CsTrunkConfiguration или панель управления Lync Server для определения соответствующих конфигураций магистрали. Дополнительные сведения о том, как включить маршрутизацию Location-Based в конфигурациях с магистрали можно найти в разделе Включение Location-Based маршрутизации в магистральные маршруты, в разделе о том, как включить [Location-Based маршрутизацию в Lync Server 2013](lync-server-2013-enabling-location-based-routing.md). В этом примере в следующей таблице показаны магистральные линии, используемые в этом сценарии.

Дополнительные сведения можно найти [в разделе Определение дополнительных каналов в построителе топологии в Lync Server 2013](lync-server-2013-define-additional-trunks-in-topology-builder.md).


<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th>Название магистрали</th>
<th>Тип системы</th>
<th>Имя</th>
<th>Местоположение</th>
<th>Сервер-посредник</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Магистраль 1 DEL-GW</p></td>
<td><p>Шлюз ТСОП</p></td>
<td><p>DEL-GW</p></td>
<td><p>Delhi</p></td>
<td><p>MS1</p></td>
</tr>
<tr class="even">
<td><p>Магистраль 2 HYD-GW</p></td>
<td><p>Шлюз ТСОП</p></td>
<td><p>HYD-GW</p></td>
<td><p>Hyderabad</p></td>
<td><p>MS1</p></td>
</tr>
<tr class="odd">
<td><p>Магистрали 3, DEL и АТС</p></td>
<td><p>АТС</p></td>
<td><p>DELETE-УАТС</p></td>
<td><p>Delhi</p></td>
<td><p>MS1</p></td>
</tr>
<tr class="even">
<td><p>Магистральная HYD 4-УАТС</p></td>
<td><p>АТС</p></td>
<td><p>HYD-УАТС</p></td>
<td><p>Hyderabad</p></td>
<td><p>MS1</p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="defines-voice-policies"></a>Определяет политики голосовой связи

Вы должны определить политики голосовой связи для своего корпоративного развертывания. Определение политики голосовой связи для обеспечения ограничений Location-Based ограничения маршрутизации для подмножества пользователей, если только их подмножество требуется для использования Location-Based маршрутизации. В этом примере в следующей таблице показаны политики голосовой связи, используемые в этом сценарии. Только те параметры, которые относятся к Location-Based маршрутизации, включены в таблицу для целей иллюстрации.

Дополнительные сведения можно найти в разделе [Настройка политик голосовой связи и использование PSTN для авторизации функций и привилегий для звонков в Lync Server 2013](lync-server-2013-configuring-voice-policies-and-pstn-usage-records-to-authorize-calling-features-and-privileges.md).


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th>Политика голосовой связи 1</th>
<th>Политика голосовой связи 2</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Идентификатор политики голосовой связи</p></td>
<td><p>Политика голосовой связи Delhi</p></td>
<td><p>Политика голосовой связи Hyderabad</p></td>
</tr>
<tr class="even">
<td><p>Использование PSTN</p></td>
<td><p>Использование Delhi, использование АТС DELETE, использование Hyd УАТС</p></td>
<td><p>Использование Hyderabad, Hyd УАТС, использование АТС Delete</p></td>
</tr>
<tr class="odd">
<td><p>PreventPSTNTollBypass</p></td>
<td><p>False</p></td>
<td><p>False</p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="define-voice-routes"></a>Определение маршрутов голосовой связи

Вы должны определить Голосовые маршруты для своего корпоративного развертывания. В этом примере в приведенной ниже таблице показаны маршруты голосовой связи, используемые в этом сценарии. Только те параметры, которые относятся к Location-Based маршрутизации, включены в таблицу для целей иллюстрации.

Дополнительные сведения можно найти [в разделе Настройка голосовых маршрутов для исходящих звонков в Lync Server 2013](lync-server-2013-configuring-voice-routes-for-outbound-calls.md).


<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th>Маршрут к голосовой связи 1</th>
<th>Маршрут к голосовой связи 2</th>
<th>Маршрут голоса 3</th>
<th>Маршрут голосовой связи 4</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Имя</p></td>
<td><p>Маршрут Delhi</p></td>
<td><p>Маршрут Hyderabad</p></td>
<td><p>Маршрут для УАТС Delete</p></td>
<td><p>Маршрут Hyd УАТС</p></td>
</tr>
<tr class="even">
<td><p>Использование PSTN</p></td>
<td><p>Использование Delhi</p></td>
<td><p>Использование Hyderabad</p></td>
<td><p>Использование DELETE для АТС</p></td>
<td><p>Использование Hyd УАТС</p></td>
</tr>
<tr class="odd">
<td><p>Линия связи</p></td>
<td><p>Магистраль 1 DEL-GW</p></td>
<td><p>Магистраль 2 HYD-GW</p></td>
<td><p>Магистрали 3, DEL и АТС</p></td>
<td><p>Магистральная HYD 4-УАТС</p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="enable-users-for-enterprise-voice"></a>Enable Users for Enterprise Voice

Включите пользователей для корпоративного голоса и назначьте им политику голосовой связи, которую вы определили ранее. В этом примере в приведенной ниже таблице показано назначение, используемое в этом сценарии. Только те параметры, которые относятся к Location-Based маршрутизации, включены в таблицу для целей иллюстрации.

Дополнительные сведения можно найти [в разделе Включение пользователей для корпоративной голосовой связи в Lync Server 2013](lync-server-2013-enable-users-for-enterprise-voice.md).


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th>Пользователи, находящиеся в Delhi</th>
<th>Пользователи, находящиеся в Hyderabad</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Соответствующая политика голосовой связи</p></td>
<td><p>Политика голосовой связи Delhi</p></td>
<td><p>Политика голосовой связи Hyderabad</p></td>
</tr>
<tr class="even">
<td><p>Примеры пользователей</p></td>
<td><p>DEL — LYNC-1, DEL-LYNC-2, DEL-LYNC-3</p></td>
<td><p>HYD-LYNC-1, HYD-LYNC-2, HYD-LYNC-3</p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="see-also"></a>См. также


[Настройка маршрутизации на основе расположения в Lync Server 2013](lync-server-2013-configuring-location-based-routing.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

