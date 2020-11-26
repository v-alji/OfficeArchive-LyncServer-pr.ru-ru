---
title: 'Lync Server 2013: настройка маршрутизации на основе расположения'
description: 'Lync Server 2013: Настройка маршрутизации Location-Based.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Location-Based Routing
ms:assetid: 63cdc474-e80f-43b1-a237-9d9ed673300a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994036(v=OCS.15)
ms:contentKeyID: 51803946
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 080c2a3a82a8714fc35ce882b0c6cb1630552f27
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433046"
---
# <a name="configuring-location-based-routing-in-lync-server-2013"></a>Настройка маршрутизации на основе расположения в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2013-03-12_

Lync Server 2013 CU1, Location-Based маршрутизация — это функция корпоративной голосовой связи. Location-Based маршрутизация — это функция управления звонками, определяющая способ маршрутизации звонков Lync Server 2013 CU1. Она обеспечивает ограничения на то, могут ли звонки перенаправляться в адреса для АТС или PSTN, основываясь на расположении вызывающего абонента Lync. Location-Based маршрутизация применяет правила авторизации вызовов к КОММУТИРУЕМым звонкам на основе сетевого расположения вызывающего абонента. Расположение вызывающего абонента определяется на основе сетевого сайта, связанного с сетевой подсетью, в которой подключен вызывающий абонент. Для настройки маршрутизации Location-Based сначала необходимо развернуть корпоративный голос, а затем настроить регионы сети, сайты и подсети. Таким образом, вы задаете основу для включения Location-Based маршрутизации.

Прежде чем развертывать Location-Based маршрут, необходимо сначала развернуть корпоративный голос и настроить регионы сети, сайты и связать сетевые подсети с сетевыми сайтами. После завершения настройки можно настроить маршрутизацию Location-Based. Инструкции по настройке регионов сети, сайтов и подсетей можно найти [в статье развертывание расширенных функций голосовой связи для предприятий в Lync Server 2013](lync-server-2013-deploying-advanced-enterprise-voice-features.md)

В этом разделе рассказывается о настройке маршрутизации Location-Based с помощью приведенного ниже примера.

![Пример маршрутизации на основе расположения голоса в корпоративной среде](images/JJ994036.b6ef5afc-36ac-406f-8ec2-a87532b20612(OCS.15).png "Пример маршрутизации на основе расположения голоса в корпоративной среде")

  
В следующей таблице представлены пользователи, определенные в этом примере.


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Тип конечной точки</th>
<th>Местоположение</th>
<th>Пользователи</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Lync</p></td>
<td><p>Корпоративный офис Delhi</p></td>
<td><p>DEL — LYNC-1, DEL-LYNC-2, DEL-LYNC-3</p></td>
</tr>
<tr class="even">
<td><p>Lync</p></td>
<td><p>Корпоративный офис Hyderabad</p></td>
<td><p>HYD-LYNC-1, HYD-LYNC-2, HYD-LYNC-3</p></td>
</tr>
<tr class="odd">
<td><p>Lync</p></td>
<td><p>Неизвестно (например, Гостиницы)</p></td>
<td><p>UNK-LYNC-1</p></td>
</tr>
<tr class="even">
<td><p>АТС</p></td>
<td><p>Корпоративный офис Delhi</p></td>
<td><p>DEL-УАТС-1, DEL-УАТС-2</p></td>
</tr>
<tr class="odd">
<td><p>АТС</p></td>
<td><p>Корпоративный офис Hyderabad</p></td>
<td><p>HYD-УАТС-1, HYD-УАТС-2</p></td>
</tr>
<tr class="even">
<td><p>ТСОП</p></td>
<td><p>Неожиданно</p></td>
<td><p>PSTN-1, PSTN-2, КТСОП-3</p></td>
</tr>
</tbody>
</table>

  

В следующей таблице представлены системы, показанные в этом примере среды.


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Администратор</th>
<th>Местоположение</th>
<th>Имя</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Пул Lync Server 2013 CU1</p></td>
<td><p>любой</p></td>
<td><p>LS-PL1</p></td>
</tr>
<tr class="even">
<td><p>Lync Server 2013 CU1, сервер для устранения проблем</p></td>
<td><p>любой</p></td>
<td><p>MS-PL1</p></td>
</tr>
<tr class="odd">
<td><p>Шлюз PSTN 1</p></td>
<td><p>Delhi</p></td>
<td><p>DEL-GW</p></td>
</tr>
<tr class="even">
<td><p>Шлюз PSTN 2</p></td>
<td><p>Hyderabad</p></td>
<td><p>HYD-GW</p></td>
</tr>
<tr class="odd">
<td><p>АТС 1</p></td>
<td><p>Delhi</p></td>
<td><p>DELETE-УАТС</p></td>
</tr>
<tr class="even">
<td><p>АТС 2</p></td>
<td><p>Hyderabad</p></td>
<td><p>КРАСНАЯ-УАТС</p></td>
</tr>
</tbody>
</table>


<div>

## <a name="in-this-section"></a>Содержание

  - [Настройка корпоративной голосовой связи в Lync Server 2013](lync-server-2013-configuring-enterprise-voice.md)

  - [Развертывание регионов сети, сайтов и подсетей в Lync Server 2013](lync-server-2013-deploying-network-regions-sites-and-subnets.md)

  - [Включение маршрутизации Location-Based в Lync Server 2013](lync-server-2013-enabling-location-based-routing.md)

</div>

<div>

## <a name="see-also"></a>См. также


[Развертывание улучшенных функций голосовой связи в Lync Server 2013](lync-server-2013-deploying-advanced-enterprise-voice-features.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

