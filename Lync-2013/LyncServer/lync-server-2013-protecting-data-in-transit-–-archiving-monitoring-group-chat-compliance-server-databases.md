---
title: 'Lync Server 2013: защита данных при передаче — архивирование, мониторинг, группирование баз данных сервера совместимости чатов'
description: 'Lync Server 2013: защита данных в пути — архивирование, отслеживание, группировка баз данных сервера соответствия требованиям группового чата.'
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
manager: serdars
audience: admin
f1.keywords:
- NOCSH
TOCTitle: Protecting data in transit – archiving, monitoring, group chat compliance server databases in Lync Server 2013
ms:assetid: ea219705-1015-43a7-890b-e7e67b451e7c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn518336(v=OCS.15)
ms:contentKeyID: 62625494
ms.date: 07/23/2014
mtps_version: v=OCS.15
ms.openlocfilehash: d4d4127bb0404bca376da450d0b0c58cf3b76560
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436848"
---
# <a name="protecting-data-in-transit--archiving-monitoring-group-chat-compliance-server-databases-in-lync-server-2013"></a>Защита данных при передаче — архивирование, мониторинг, группирование баз данных сервера совместимости чатов в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2013-12-05_

Microsoft Lync Server 2013 Архивирование сервера и сервера мониторинга используют как служба очереди сообщений (также называемая MSMQ) для сбора и надежного перемещения сообщений данных из коллекции на серверы репозитория. Служба соответствия собирает данные вместе с сервером группового чата, который также использует очередь сообщений.

В Lync Server 2013 отсутствует внутренняя защита для данных по каналу связи. Тем не менее, если требуется защитить этот трафик, служба очереди сообщений может обеспечивать шифрование на уровне сообщений в очереди отправки сообщений. Это делается с помощью сертификатов, управляемых доменными службами Active Directory. Подробные сведения можно найти в статье приложение г: очередь сообщений и связь через Интернет в Windows Server 2008 в [https://go.microsoft.com/fwlink/p/?LinkId=145238](https://go.microsoft.com/fwlink/p/?linkid=145238) или приложении I: очередь сообщений и Интернет-связь в Windows server 2008 R2 [https://go.microsoft.com/fwlink/p/?LinkId=211883](https://go.microsoft.com/fwlink/p/?linkid=211883) для windows Server 2008 R2.

</div>

<span> </span>

</div>

</div>

</div>

