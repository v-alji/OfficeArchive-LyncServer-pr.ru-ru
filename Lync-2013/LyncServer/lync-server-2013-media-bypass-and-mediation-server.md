---
title: 'Lync Server 2013: сервер-посредник и обход сервера посредника'
description: 'Lync Server 2013: сервер обходит и исходящие мультимедиа.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Media bypass and Mediation Server
ms:assetid: 8ed35f95-05cd-4b5d-8470-442d2323df71
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398719(v=OCS.15)
ms:contentKeyID: 48184774
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ebb005d3d52fa9e5a38fdf56a65dfcbd73616d87
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425705"
---
# <a name="media-bypass-and-mediation-server-in-lync-server-2013"></a>Сервер-посредник и обход сервера посредника в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-09-21_

Обтекание мультимедиа — это возможность Lync Server, которая позволяет администратору настроить маршрутизацию звонков прямо между конечной точкой пользователя и шлюзом коммутируемой телефонной сети (PSTN) без обхода сервера-посредника. Обход мультимедиа улучшает качество связи, уменьшая задержку, ненужные переводы, вероятность потери пакетов и количество возможных точек сбоя. Если удаленный сайт без сервера-посредника подключен к центральному сайту по одной или нескольким ГЛОБАЛЬным каналам связи с ограниченной пропускной способностью, пропустите требования к пропускной способности, разрешив доступ к мультимедиа с клиента на удаленном сайте для непосредственного подключения к серверу-источнику и обратно. Это сокращение в обработке мультимедиа также дополняет возможности сервера-посредника для управления несколькими шлюзами.

Обход сервера-посредника и контроль допуска звонков являются взаимоисключающими функциями. Если для вызова применяется обход сервера-посредника, то для него не применяется контроль допуска звонков. Предполагается, что нет никакой связи с ограниченной пропускной способностью сторон, участвующих в вызове.

<div>

## <a name="see-also"></a>См. также


[Контроль допуска звонков и сервер-посредник в Lync Server 2013](lync-server-2013-call-admission-control-and-mediation-server.md)  


[Планирование обхода серверов-посредников в Lync Server 2013](lync-server-2013-planning-for-media-bypass.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

