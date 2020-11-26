---
title: 'Lync Server 2013: сведения о сертификате — расширяемая Федерация протоколов обмена сообщениями и присутствия (XMPP)'
description: 'Lync Server 2013: сведения о сертификате — расширяемая Федерация протоколов обмена сообщениями и присутствия (XMPP).'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate summary - Extensible messaging and presence protocol (XMPP) federation
ms:assetid: b059a34e-99df-40af-91fe-fe2aa52841f6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ618374(v=OCS.15)
ms:contentKeyID: 49105661
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6e2bb593d909c2eec6032dc89c07cc5f5b1a72db
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435301"
---
# <a name="certificate-summary---extensible-messaging-and-presence-protocol-xmpp-federation-in-lync-server-2013"></a>Сведения о сертификате — расширяемая Федерация протоколов обмена сообщениями и присутствия (XMPP) в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-12-23_

Требования к сертификатам для включения и установления связи с партнерами по протоколу расширенного обмена сообщениями (XMPP) требуют дополнительной записи доменов XMPP. Запись, включенная в сертификат в качестве дополнительного имени субъекта (SAN), будет являться доменом, который может принимать участие в XMPP обмене сообщениями. Домен может быть доменом корневого уровня (например, contoso.com), если вы хотите включить XMPP для всего домена или выбрать его дочерние домены (например, corp.contoso.com, finance.contoso.com), если вы включаете XMPP для подмножества пользователей.

<div>

## <a name="certificate-summary-for-extensible-messaging-and-presence-protocol"></a>Сведения о сертификате для протокола расширенного обмена сообщениями и присутствия


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Компонент</th>
<th>Имя субъекта</th>
<th>Замещающий имена субъектов (SAN)/Order</th>
<th>Комментарии</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Назначение доступа к службе Edge пограничного сервера или пограничного пула</p></td>
<td><p>sip.contoso.com</p></td>
<td><p>webcon.contoso.com</p>
<p>sip.contoso.com</p>
<p>sip.fabrikam.com</p>
<p>contoso.com</p></td>
<td><p>Первые три элемента сети SAN — это стандартные записи в сети SAN для полного пограничного сервера. Contoso.com — это запись, необходимая для Федерации с партнером XMPP на уровне корневого домена. Эта запись позволит XMPP всем доменам с суффиксом contoso.com.</p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a>См. также


[Пример конфигурации XMPP в Lync Server 2013 — федерация XMPP с Google Talk](lync-server-2013-example-xmpp-configuration-–-xmpp-federation-with-google-talk.md)  


[Планирование сертификатов пограничного сервера в Lync Server 2013](lync-server-2013-plan-for-edge-server-certificates.md)  


[Настройка сертификатов пограничного сервера для Lync Server 2013](lync-server-2013-set-up-edge-certificates.md)  
[Request-CsCertificate](https://docs.microsoft.com/powershell/module/skype/Request-CsCertificate)  
[Set-CsCertificate](https://docs.microsoft.com/powershell/module/skype/Set-CsCertificate)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

