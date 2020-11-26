---
title: 'Lync Server 2013: сведения о сертификате-общедоступная служба обмена мгновенными сообщениями'
description: 'Lync Server 2013: сведения о сертификате — общедоступная служба обмена мгновенными сообщениями.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate summary - Public instant messaging connectivity
ms:assetid: 2b3687ee-50c2-4c1c-880e-8dcf8bd4f309
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ618370(v=OCS.15)
ms:contentKeyID: 49105657
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: abf5a01bdeb03da158e221c623417a1b42cc82f8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435294"
---
# <a name="certificate-summary---public-instant-messaging-connectivity-in-lync-server-2013"></a>Сведения о сертификате: общедоступная служба обмена мгновенными сообщениями в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2013-02-19_

Чтобы настроить сертификаты для подключения к общедоступной службе мгновенных сообщений, необходимо сначала обратить внимание на то, что ничего не отличается от других типов Федерации SIP или даже стандартных сертификатов пограничного сервера, за исключением того, что для America Online (AOL) требуется уникальная конфигурация сертификата. В дополнение к стандартному расширенному использованию серверного ключа (EKU) для Skype Online требуется, чтобы сертификат или сертификаты (в случае пограничного пула) также содержали клиентское EKU. Клиентское EKU является дополнением к сертификату и является частью внешнего общедоступного сертификата, назначенного пограничного сервера.

<div>

## <a name="certificate-summary--public-instant-messaging-connectivity"></a>Сведения о сертификате: общедоступная служба обмена мгновенными сообщениями


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
<td><p>Внешний край и доступ</p></td>
<td><p>sip.contoso.com</p></td>
<td><p>sip.contoso.com</p>
<p>webcon.contoso.com</p>
<p>sip.fabrikam.com</p></td>
<td><p>Сертификат должен находиться в общедоступном центре сертификации, а также в том случае, если вы разворачиваете общедоступную службу обмена мгновенными сообщениями с AOL, и у вас должен быть серверный EKU Сертификат назначается внешним интерфейсам пограничного сервера для следующих параметров:</p>
<ul>
<li><p>доступа</p></li>
<li><p>веб-конференций</p></li>
<li><p>передачи аудио- и видеоданных</p></li>
</ul>
<p>Обратите внимание, что сети SAN автоматически добавляются к сертификату на основе определений в построителе топологии. Вы добавляете записи SAN по мере необходимости для дополнительных доменов SIP и других элементов, которые необходимо поддерживать. Имя субъекта реплицируется в сети SAN и должно быть представлено для правильной работы.</p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a>См. также


[Сценарии доступа внешних пользователей в Lync Server 2013](lync-server-2013-scenarios-for-external-user-access.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

