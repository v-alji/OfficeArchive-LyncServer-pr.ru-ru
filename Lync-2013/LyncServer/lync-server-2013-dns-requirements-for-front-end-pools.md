---
title: 'Lync Server 2013: требования к DNS для пула переднего'
description: 'Lync Server 2013: требования к DNS для пула Front End.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS requirements for Front End pools
ms:assetid: ba28919c-fbbe-4c54-8bf9-2b0cd3fa39c7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412910(v=OCS.15)
ms:contentKeyID: 48185228
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8c0369e82bd8ed2ea63e2156728b41f9942b0148
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429072"
---
# <a name="dns-requirements-for-front-end-pools-in-lync-server-2013"></a>Требования к DNS для пула Front End в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-11-07_

В этом разделе описаны записи службы доменных имен (DNS), необходимые для развертывания пулов переднего уровня.

<div>

## <a name="dns-records-for-front-end-pools"></a>Записи DNS для переднего пула

В следующей таблице указаны требования к DNS для развертывания переднего пула Lync Server 2013.

### <a name="dns-requirements-for-a-front-end-pool"></a>Требования К DNS для переднего пула

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
<td><p>Передней пул с несколькими серверами переднего уровня и аппаратным балансировчиком нагрузки (независимо от того, развернута ли в нем балансировка нагрузки DNS)</p></td>
<td><p>При использовании балансировки нагрузки DNS и балансировки нагрузки оборудования необходимо иметь записи host (A). Создайте внутреннюю запись A, которая разрешит полное доменное имя (FQDN) переднего пула для балансировки нагрузки DNS. Создайте внутреннюю запись (A) для внутренних веб-служб на виртуальный IP-адрес (VIP-адрес) балансиров нагрузки. Необходимо использовать имя внутренней веб-службы, как определено в построитель топологии.</p>
<p>Например, если вы используете как балансировку нагрузки DNS, так и балансировку нагрузки оборудования, у вас будет запись A для каждого переднего сервера в пуле для балансировки нагрузки DNS и запись A для внутренних веб-служб, указывающих на виртуальный IP-адрес балансировки нагрузки оборудования:</p>
<ul>
<li><p>Балансировка нагрузки DNS: Pool01.contoso.net IP-адрес пула 10.10.10.5</p>
<div>

> [!WARNING]  
> У каждого переднего сервера также будет отдельная запись A:


</div>
<ol>
<li><p>FE01.contoso.net 10.10.10.1</p></li>
<li><p>FE02.contoso.net 10.10.10.2</p></li>
<li><p>FE03.contoso.net 10.10.10.3</p></li>
<li><p>FE04.contoso.net 10.10.10.4</p></li>
</ol></li>
<li><p>Балансировка нагрузки оборудования: WebInternal.contoso.net IP-адреса VIP 192.168.10.5 HLB</p></li>
</ul>
<p>Все трафик, за исключением трафика HTTP или HTTPS, будет использовать Pool01.contoso.net записи. Трафик HTTP или HTTPS будет использовать определенный адрес внутренних веб-служб 192.168.10.5</p></td>
</tr>
<tr class="even">
<td><p>Передний пул с развернутой балансировой нагрузки DNS</p></td>
<td><p>Набор внутренних записей A, которые решают FQDN пула с IP-адресами каждого сервера в пуле. Для каждого сервера в пуле должна быть одна запись A.</p></td>
</tr>
<tr class="odd">
<td><p>Передний пул с развернутой балансировой нагрузки DNS</p></td>
<td><p>Набор внутренних записей A, которые по IP-адресу этого сервера устанавливают FQDN каждого сервера в пуле. Подробные сведения см. в документации по планированию для балансировки нагрузки DNS в <a href="lync-server-2013-dns-load-balancing.md">Lync Server 2013.</a></p></td>
</tr>
<tr class="even">
<td><p>Front End pool with a single Front End Server and a dedicated back-end database but no load balancer</p></td>
<td><p>Внутренняя запись A, которая устраняет FQDN переднего пула с IP-адресом одного переднего сервера Enterprise Edition.</p></td>
</tr>
<tr class="odd">
<td><p>Автоматический вход в клиент</p></td>
<td><p>Для каждого поддерживаемых домена SIP записи SRV для _sipinternaltls._tcp. &lt; домен &gt; через порт 5061, который сопоканирует FQDN переднего пула, который аутентификация и перенаправляет запросы клиентов на вход. Подробные сведения см. в требованиях К DNS для автоматического входов <a href="lync-server-2013-dns-requirements-for-automatic-client-sign-in.md">клиентов в Lync Server 2013.</a></p></td>
</tr>
<tr class="even">
<td><p>Обнаружение веб-службы обновления устройств на устройствах единой коммуникации</p></td>
<td><p>Внутренняя запись A с именем ucupdates-r2. &lt; Домен SIP, который передается на IP-адрес переднего пула, на котором размещена &gt; веб-служба обновления устройств. В ситуации, когда устройство UC включено, но пользователь никогда не вошел в систему, запись A позволяет устройству обнаружить интерфейсную службу обновления пула, в которой размещено устройство, и получить обновления. В противном случае устройства получают эти сведения, хотя при первом входе пользователя они получают доступ к интерфейсу.</p>
<div>

> [!IMPORTANT]  
> Если у вас уже развернута веб-служба обновления устройств в Lync Server 2010, вы уже создали внутреннюю запись A с именем, которое не работает. &lt; Домен &gt; SIP. Для Microsoft Office Communications Server 2007 R2 необходимо создать дополнительную запись DNS A с именем ucupdates-r2. &lt; Домен &gt; SIP.


</div></td>
</tr>
<tr class="odd">
<td><p>Обратный прокси-сервер для поддержки HTTP-трафика</p></td>
<td><p>Внешняя запись A, которая устраняет FQDN внешней веб-фермы с внешним IP-адресом обратного прокси-сервера. Клиенты и устройства UC используют эту запись для подключения к обратному прокси-серверу. Подробные сведения см. в документации по планированию определения требований К DNS для <a href="lync-server-2013-determine-dns-requirements.md">Lync Server 2013.</a></p></td>
</tr>
</tbody>
</table>


В таблице ниже показан пример записей DNS, необходимых для FQDN внутренней веб-фермы.

### <a name="example-dns-records-for-internal-web-farm-fqdn"></a>Примеры DNS-записей для FQDN внутренней веб-фермы

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>FQDN внутренней веб-фермы</th>
<th>Полное доменное имя пула</th>
<th>Записи DNS A</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>webcon.contoso.com</p></td>
<td><p>ee-pool.contoso.com</p></td>
<td><p>DNS A-запись для ee-pool.contoso.com, которая передается на VIP-адрес балансира нагрузки, используемого серверами переднего сервера.</p>
<p>DNS A-запись для webcon.contoso.com, которая передается на VIP-адрес балансира нагрузки, используемого серверами переднего сервера.</p></td>
</tr>
<tr class="even">
<td><p>ee-pool.contoso.com</p></td>
<td><p>ee-pool.contoso.com</p></td>
<td><p>DNS A-запись для ee-pool.contoso.com, которая передается на виртуальный IP-адрес (VIP) балансира нагрузки, используемого серверами Front End Server Enterprise Edition в переднем пуле.</p>
<p>Обратите внимание: если в этом пуле используется балансировка нагрузки DNS, у вашего переднего и внутреннего веб-фермы не может быть одного и того же FQDN.</p></td>
</tr>
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</div>

