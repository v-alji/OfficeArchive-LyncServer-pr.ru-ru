---
title: 'Lync Server 2013: технические требования для сервера-посредника'
description: 'Lync Server 2013: технические требования для обхода мультимедиа.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Technical requirements for media bypass
ms:assetid: 6162a204-0e7c-460a-8eb2-e592c6590a8a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398435(v=OCS.15)
ms:contentKeyID: 48184321
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dee594139031966342fcec2bc1296a603055b4cc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423437"
---
# <a name="technical-requirements-for-media-bypass-in-lync-server-2013"></a>Технические требования для сервера-посредника в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-09-21_

Для каждого звонка в КТСОП сервер-посредник определяет, можно ли отправлять носители из конечной точки Lync непосредственно на сервер-посредника, не передавая его на сервер. Узлом партнера может являться шлюз ТСОП, УАТС или пограничный контроллер поставщика услуг интернет-телефонии (ITSP), связанного с магистральной линией между сервером-посредником, где маршрутизируется вызов.

Обход сервера-посредника можно использовать, если удовлетворены следующие требования:

  - Одноранговый сервер-посредник должен поддерживать необходимые возможности для пропуска мультимедиа, но важнее всего лишь возможность обработки нескольких разветвленных ответов (называемых ранними диалогами). Обратитесь к производителю шлюза или ITSP, чтобы получить значение максимального количества ранних диалогов, которые могут поддерживать шлюз, PBX или SBC.

  - Одноранговый сервер должен получать трафик мультимедиа прямо из конечных точек Lync. Многие ITSPs позволяют их SBC получать трафик только от сервера обновлений. Обратитесь к своему ITSPу, чтобы определить, принимает ли его SBC мультимедийный трафик прямо из конечных точек Lync.

  - Клиенты Lync и одноранговый сервер-посредник должны быть надежно подключены, то есть они размещаются в том же регионе сети или на сайтах сети, которые подключаются к региону по глобальным каналам связи, не имеющим ограничений на пропускную способность.

<div>

## <a name="see-also"></a>См. также


[Режимы обхода сервера-посредника в Lync Server 2013](lync-server-2013-media-bypass-modes.md)  
[Обход сервера-посредника и контроль допуска звонков в Lync Server 2013](lync-server-2013-media-bypass-and-call-admission-control.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

