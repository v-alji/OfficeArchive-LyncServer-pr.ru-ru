---
title: Сводка по порту — расширяемая Федерация протоколов обмена сообщениями и присутствия (XMPP)
description: Сводка по порту — расширяемая Федерация протоколов обмена сообщениями и присутствия (XMPP).
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary -  Extensible messaging and presence protocol (XMPP) federation
ms:assetid: 62e98fab-7add-4983-a3fa-dbe74e1c3849
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ618371(v=OCS.15)
ms:contentKeyID: 49105658
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9508bc8b9fbcca6fb6a37478def258a9fa52c373
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442805"
---
# <a name="port-summary---extensible-messaging-and-presence-protocol-xmpp-federation-in-lync-server-2013"></a>Сводка по порту — расширяемая Федерация протоколов обмена сообщениями и присутствия (XMPP) в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-10-20_

Порты и протоколы, определенные для прокси-сервера расширяемых сообщений и протоколов XMPP, развернутых на пограничном сервере, разрешают обмен данными между сервером пограничного сервера XMPP и допускает передачу данных с пограничного сервера на сервер федеративного партнера XMPP. Правило также определяется во внутреннем брандмауэре, доступном на сервере переднего плана или на пограничном пуле, к внешнему и внешнему интерфейсу.

<div>

## <a name="firewall-summary-for-extensible-messaging-and-presence-protocol"></a>Сводка брандмауэра по протоколу расширенного обмена сообщениями и присутствия


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Протокол/TCP или UDP/порт</th>
<th>Источник (IP-адрес)</th>
<th>Назначение (IP-адрес)</th>
<th>Комментарии</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>XMPP/TCP/5269</p></td>
<td><p>Любой</p></td>
<td><p>IP-адрес интерфейса службы Edge Access</p></td>
<td><p>Стандартный коммуникационный порт "сервер-сервер" для XMPP. Разрешает связь с прокси-сервером пограничного сервера XMPP от федеративных XMPP партнеров</p></td>
</tr>
<tr class="even">
<td><p>XMPP/TCP/5269</p></td>
<td><p>IP-адрес интерфейса службы Edge Access</p></td>
<td><p>Любой</p></td>
<td><p>Стандартный коммуникационный порт "сервер-сервер" для XMPP. Разрешает взаимодействие с XMPP прокси-сервером для федеративных XMPP партнеров</p></td>
</tr>
<tr class="odd">
<td><p>XMPP/MTLS/23456</p></td>
<td><p>Любой</p></td>
<td><p>IP-адрес внутреннего интерфейса пограничного сервера</p></td>
<td><p>Внутренний XMPP трафик из шлюза XMPP на сервере переднего плана или в пуле переднего плана на пограничный сервер</p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a>См. также


[Пример конфигурации XMPP в Lync Server 2013 — федерация XMPP с Google Talk](lync-server-2013-example-xmpp-configuration-–-xmpp-federation-with-google-talk.md)  


[Управление федеративными XMPP-партнерами в Lync Server 2013](lync-server-2013-manage-xmpp-federated-partners-for-your-organization.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

