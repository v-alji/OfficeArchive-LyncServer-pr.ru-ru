---
title: 'Lync Server 2013: Установка сертификата на узле-наблюдателе, расположенном за пределами сети периметра'
description: 'Lync Server 2013: Установка сертификата на узле-наблюдателе, расположенном за пределами сети периметра.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Installing a certificate on a watcher node located outside the perimeter network
ms:assetid: 825c9c02-1951-4d7a-a25e-a313a85333f8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688113(v=OCS.15)
ms:contentKeyID: 49733711
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 66f40886e9784b5bd4182a60b955745b5daf2034
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427070"
---
# <a name="installing-a-certificate-on-a-watcher-node-located-outside-the-perimeter-network-of-lync-server-2013"></a>Установка сертификата на узле-наблюдателе, расположенном вне сети периметра Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-10-22_

Агенты System Center Operations Manager, работающие в демилитаризованной зоне (например, на пограничном сервере Lync Server), вне Организации (например, на внешнем узле наблюдения за транзакциями) или на границе доверия доменных служб Active Directory, могут потребовать настройки сервера шлюза System Center Operations Manager. Эта роль сервера позволяет агентам, у которых нет отношения доверия с корневым сервером управления, создавать оповещения. Дополнительные сведения можно найти в разделе "Управление серверами шлюзов в Operations Manager 2007" в библиотеке TechNet System Center Operations Manager по адресу [https://go.microsoft.com/fwlink/p/?LinkId=268703](https://go.microsoft.com/fwlink/p/?linkid=268703) .

Если вы развертываете агент в одном из этих местоположений, вам также потребуется запросить и настроить сертификат, который позволит узлу-наблюдателю отправлять оповещения в System Center Operations Manager. Для упрощения этого процесса группа Operations Manager создала набор служебных программ, которые позволят вам запросить и установить правильный тип сертификата на компьютере с узлом-наблюдателем. Сведения о том, как скачать эти служебные программы, можно найти в статье "получение сертификатов для агентов, не присоединенных к домену, с помощью мастера создания сертификатов" на веб-странице блога [https://go.microsoft.com/fwlink/p/?LinkId=267421](https://go.microsoft.com/fwlink/p/?linkid=267421) .

</div>

<span> </span>

</div>

</div>

</div>

