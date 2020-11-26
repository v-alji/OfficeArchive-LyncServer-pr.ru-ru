---
title: 'Lync Server 2013: получение сведений о местоположении'
description: 'Lync Server 2013: получение расположения.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Acquiring a location
ms:assetid: 9bf069aa-d240-4d95-be3a-e795537f8e70
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205110(v=OCS.15)
ms:contentKeyID: 48184903
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 25aa907b5373cadd9eb8ffe9e32a7531afa01deb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439493"
---
# <a name="acquiring-a-location-in-lync-server-2013"></a>Получение сведений о местоположении в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-06-06_

В среде Lync Server 2013 E9-1-1 — Каждый внутренний подключаемый клиент Lync или Lync Phone Edition активно получает свое собственное расположение. После регистрации SIP клиент помещает все сведения о сетевом подключении, которые ему знают, в запрос расположения службе сведений о расположении, которая является веб-службой с помощью реплицированной базы данных SQL Server. У каждого центрального пула сайтов есть служба сведений о расположении, которая использует сведения о сети для запроса записей для соответствующего местоположения. В случае соответствия служба сведений о расположении возвращает расположение клиенту. If there is not a match, the user may be prompted to enter a location manually (depending on location policy settings). The location data are transmitted back to the client in an Internet Engineering Task Force (IETF) standardized XML format called Presence Information Data Format Location Object (PIDF-LO).

Клиент Lync Server включает данные из PIDF в процессе вызова экстренной помощи, и эти данные используются поставщиком услуг E9-1-1, чтобы определить соответствующие PSAP и перенаправить вызов на этот PSAP вместе с правильным ESQK, что позволяет диспетчеру PSAP получить расположение вызывающего абонента.

На приведенной ниже схеме показано, как клиент Lync Server получает расположение (за исключением метода расположения, основанного на сторонних MAC-адресах сторонних клиентов).

![Получение расположения клиентом (схема)](images/JJ205110.4438f5fc-f1b2-444b-8565-09035363ed43(OCS.15).jpg "Получение расположения клиентом (схема)")

Чтобы клиент мог получить местоположение, необходимо выполнить следующие действия.

1.  Администратор заполнит базу данных службы сведений о расположении, указав сетевые Wiremap (таблицы, которые сопоставляют различные типы сетевых адресов с соответствующими расположениями в службе аварийного реагирования (ERLs)).

2.  Если используется поставщик службы E9-1-1 с магистралью SIP, администратор проверяет физические адреса в ERL по базе данных основного справочника адресов (MSAG), поддерживаемой поставщиком службы E9-1-1. Если используется шлюз ELIN, администратор проверяет, что оператор ТСОП отправляет данные ELIN в базу данных автоматического определения местоположения (ALI).

3.  Во время регистрации или при каждом изменении сети внутренний подключаемый клиент отправляет запрос на расположение, содержащий обнаруженные сетевые адреса клиента, в службу сведений о расположении.

4.  Служба сведений о расположении запрашивает опубликованные записи для местоположения и, если оно найдено, возвращает ERL клиенту в формате PIDF.

</div>

<span> </span>

</div>

</div>

</div>

