---
title: Перенос федерации XMPP
description: Миграция XMPP Федерации.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migrating XMPP federation
ms:assetid: b8d2b4b9-d0ed-4b48-820a-2c257fbdd2fb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721861(v=OCS.15)
ms:contentKeyID: 49733794
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e63c9f6fd3f1c1d45de77c27417987505678f74b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440362"
---
# <a name="migrating-xmpp-federation"></a>Перенос федерации XMPP

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-10-19_

Предыдущие версии Lync Server и Office Communications Server предоставили шлюз расширенных сообщений и протоколов доступа (XMPP), который можно развернуть как отдельную серверную роль, разрешающую Федерацию с помощью XMPPных развертываний. В Lync Server 2013 функциональность XMPP может быть развернута как функция. Функции XMPP устанавливаются в виде прокси-сервера XMPP, который работает на пограничном сервере Lync Server 2013 и шлюз XMPP, который работает на сервере переднего плана Lync Server 2013.

С точки зрения миграции учетная запись пользователя Lync Server может быть перемещена в пул Lync Server 2013 и продолжать использовать устаревший шлюз XMPP. Это возможно, только если для федеративного партнера XMPP не настроена платформа Lync Server 2013.

В сводке, если Lync Server 2010 был развернут с помощью шлюза Office Communications Server 2007 R2 XMPP Gateway и XMPP Federation для пользователей Lync Server 2010, чтобы перенести XMPPную Федерацию на Lync Server 2013, выполните указанные ниже действия.

1.  Развертывание пула Lync Server 2013.

2.  Разверните сервер Lync Server 2013 Edge.

3.  Перемещение всех пользователей в пул Lync Server 2013

4.  Создавайте политики доступа XMPP и сертификаты для пограничного сервера.

5.  Включите Федерацию XMPP в Lync Server 2013. 

6.  Обновите записи DNS, чтобы они указывали на сервер Lync Server 2013 XMPP Gateway.

</div>

<span> </span>

</div>

</div>

</div>

