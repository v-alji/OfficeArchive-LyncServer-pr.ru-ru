---
title: 'Lync Server 2013: сведения о просмотре QoE'
description: 'Lync Server 2013: QoE View Details.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: QoE view details
ms:assetid: 6a658318-a317-4546-a44c-a9c473d8e86a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688081(v=OCS.15)
ms:contentKeyID: 49733677
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b20eb083295a5f3d3ecb5be7a8c96d9c4b7cfab2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398992"
---
# <a name="qoe-view-details-in-lync-server-2013"></a>QoE просмотра данных в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-10-03_

В представлениях рассматриваются наиболее распространенные сценарии возврата данных из базы данных SQL QoE. Рекомендуется использовать представления для создания настраиваемых отчетов вместо прямого доступа к таблицам базы данных; Это связано с тем, что представления более удобны для обеспечения обратной совместимости с будущими выпусками.


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Имя представления</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="lync-server-2013-audiostreamdetail-view.md">AudioStreamDetail представления в Lync Server 2013</a></p></td>
<td><p>Хранит сведения о каждом звуковом потоке в базе данных.</p></td>
</tr>
<tr class="even">
<td><p><a href="lync-server-2013-medialine-view.md">MediaLine представления в Lync Server 2013</a></p></td>
<td><p>Хранит сведения о каждой строке мультимедиа в базе данных. Один звуковой сеанс обычно состоит из одной линии звукового файла. Один из звуковых и видеофайлов (A/V) обычно состоит из одной линии звукового файла и одной линии видеоклипа; Тем не менее, в этом сеансе могут содержаться две строки видеофайла, если используется устройство конференц-связи или если используется представление коллекции.</p></td>
</tr>
<tr class="odd">
<td><p><a href="lync-server-2013-networkconfigurationsettings-view.md">NetworkConfigurationSettings представления в Lync Server 2013</a></p></td>
<td><p>Хранит сведения о конфигурации сети.</p></td>
</tr>
<tr class="even">
<td><p><a href="lync-server-2013-session-view.md">Представление сеанса в Lync Server 2013</a></p></td>
<td><p>Хранит сведения о сеансах с записями в базе данных.</p></td>
</tr>
<tr class="odd">
<td><p><a href="lync-server-2013-useragent-view.md">Представление "UserAgent" в Lync Server 2013</a></p></td>
<td><p>Хранит сведения об агентах пользователей, вовлеченных в сеансы с записями в базе данных.</p></td>
</tr>
<tr class="even">
<td><p><a href="lync-server-2013-videostreamdetail-view.md">VideoStreamDetail представления в Lync Server 2013</a></p></td>
<td><p>Хранит сведения о каждом видеопотоке в базе данных.</p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

