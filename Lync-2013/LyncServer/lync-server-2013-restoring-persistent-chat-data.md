---
title: 'Lync Server 2013: восстановление сохраняемых данных чата'
description: 'Lync Server 2013: восстановление сохраняемых данных чата.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Restoring Persistent Chat data
ms:assetid: c251a7fa-50da-434b-b39a-17f5978ce736
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945649(v=OCS.15)
ms:contentKeyID: 51541516
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7c75683e151daaadab8374ed5b41886da9a3aea3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442511"
---
# <a name="restoring-persistent-chat-data-in-lync-server-2013"></a>Восстановление данных из сохраняемого чата в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2013-02-18_

Сохраняемый контент комнаты чата хранится в базе данных сохраняемого чата (MGC. mdf). Необходимо регулярно создавать резервные копии этих критически важных для бизнеса данных. В дополнение к содержимому комнаты чата, участникам (например, пользователям и группам), а также ролям и Access, которые им нужно общаться с комнатами и разговаривать с содержимым комнаты чата, в базе данных сохраняемого чата.

Способ восстановления сохраняемых данных чата зависит от того, какой метод вы использовали для архивации.

  - Если были использованы процедуры резервного копирования SQL Server, необходимо использовать процедуры восстановления SQL Server.

  - Если вы использовали командлет **Export-CsPersistentChatData** для резервного копирования сохраненных данных чата, необходимо использовать командлет **Import-CsPersistentChatData** для восстановления данных.

</div>

<span> </span>

</div>

</div>

</div>

