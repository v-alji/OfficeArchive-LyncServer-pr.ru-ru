---
title: 'Lync Server 2013: Добавление и удаление серверного переднего плана'
description: 'Lync Server 2013: Добавление и удаление серверного переднего плана.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Add or remove a Front End Server
ms:assetid: ab748733-6bad-4c93-8dda-db8d5271653d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205153(v=OCS.15)
ms:contentKeyID: 48185050
ms.date: 01/21/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 297bbf42dbba3d4f9926fd5ab9e0d7ed79349dc4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439277"
---
# <a name="add-or-remove-a-front-end-server-in-lync-server-2013"></a>Add or remove a Front End Server in Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2016-01-21_

Если вы добавите сервер переднего плана в пул или удалите сервер переднего плана из пула, необходимо перезапустить пул. Чтобы предотвратить прерывание обслуживания для пользователей, выполните описанные ниже действия при добавлении или удалении сервера переднего плана.

<div>


> [!NOTE]  
> При добавлении в пул новых серверов их уровень накопительного пакета обновления должен быть таким же, как у существующих серверов в пуле.



</div>

<div>

## <a name="to-add-or-remove-front-end-servers"></a>Добавление и удаление серверов переднего плана

1.  Если удаляются все серверы переднего плана, сначала необходимо остановить новые подключения к этим серверам. Для этого вы можете использовать следующий командлет:
    
        Stop-CsWindowsServices -Graceful

2.  Если удаляемые серверы не имеют текущих сеансов, остановите на них службы Lync Server.

3.  Откройте построитель топологии и добавьте или удалите необходимые серверы.

4.  Опубликуйте топологию.

5.  Если в пуле не было двух серверов переднего плана, более двух, или более двух серверов, необходимо ввести следующий командлет:
    
        Reset-CsPoolRegistrarState-ResetType FullReset -PoolFqdn <PoolFqdn>
    
    Если в пуле есть три или более серверов, при вводе этого командлета на компьютере должно быть запущено по крайней мере три сервера.

6.  Перезапустите все серверы переднего плана в пуле, по одному за один раз.

</div>

</div>

<span> </span>

</div>

</div>

</div>

