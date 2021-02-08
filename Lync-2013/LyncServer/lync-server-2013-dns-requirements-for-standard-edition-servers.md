---
title: 'Lync Server 2013: требования к DNS для серверов Standard Edition'
description: 'Lync Server 2013: требования к DNS для серверов Standard Edition.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS requirements for Standard Edition servers
ms:assetid: 3d6bbe65-e7ce-491b-a0bd-d2f7197f240d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425900(v=OCS.15)
ms:contentKeyID: 48183920
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: cc93549e07fb82304ad76b051730eab972530764
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398185"
---
# <a name="dns-requirements-for-standard-edition-servers-in-lync-server-2013"></a>Требования к DNS для серверов Standard Edition в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-06-19_

В этом разделе описаны записи службы доменных имен (DNS), необходимые для развертывания серверов Standard Edition.

<div>

## <a name="dns-records-for-standard-edition-servers"></a>DNS Records for Standard Edition Servers

В следующей таблице указаны требования к DNS для развертывания сервера Lync Server 2013 Standard Edition.

### <a name="dns-requirements-for-a-standard-edition-server"></a>Требования К DNS для сервера Standard Edition Server

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Сценарий развертывания</th>
<th>Требование DNS</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Standard Edition</p></td>
<td><p>Внутренняя запись A, разрешающая полное доменное имя сервера в IP-адрес.</p></td>
</tr>
<tr class="even">
<td><p>Автоматический вход в клиент</p></td>
<td><p>Для каждого поддерживаемых домена SIP записи SRV для _sipinternaltls._tcp. &lt; домен через порт 5061, который сопопишется с FQDN сервера Standard Edition, который аутентификация и перенаправляет запросы клиентов на &gt; вход. Подробные сведения см. в требованиях К DNS для автоматического входов <a href="lync-server-2013-dns-requirements-for-automatic-client-sign-in.md">клиентов в Lync Server 2013.</a></p></td>
</tr>
<tr class="odd">
<td><p>Обнаружение веб-службы обновления устройств на устройствах единой коммуникации</p></td>
<td><p>Внутренняя запись A с именем ucupdates-r2. &lt; Домен SIP, который передается на IP-адрес веб-службы обновления устройства standard Edition на сервере Standard &gt; Edition. В ситуации, когда устройство UC включено, но пользователь никогда не вошел в систему, запись A позволяет устройству найти веб-службу обновления устройства на сервере и получить обновления. В противном случае устройство получает сведения о сервере посредством автоматической подготовки при первом входе пользователя.</p></td>
</tr>
<tr class="even">
<td><p>Обратный прокси-сервер для поддержки HTTP-трафика</p></td>
<td><p>Внешняя запись A, которая устраняет FQDN внешней веб-фермы с внешним IP-адресом обратного прокси-сервера. Клиенты и устройства UC используют эту запись для подключения к обратному прокси-серверу. Подробные сведения см. в документации по планированию определения <a href="lync-server-2013-determine-dns-requirements.md">требований К DNS для Lync Server 2013.</a></p></td>
</tr>
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</div>

