---
title: 'Lync Server 2013: отработка отказа для пула'
description: 'Lync Server 2013: сбой обратной связи с пулом.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Failing back a pool
ms:assetid: 6232b644-ef57-4c9c-abec-14ff8ffc9fe7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204945(v=OCS.15)
ms:contentKeyID: 48184289
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1c1fc0ea4514d2f951dd936521590d47b809db38
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428330"
---
# <a name="failing-back-a-pool-in-lync-server-2013"></a>Отработка отказа для пула в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-11-01_

После того как пул, в котором произошел сбой, перейдет в оперативный режим (то есть Pool1 в этом примере), выполните указанные ниже действия, чтобы восстановить состояние развертывания для обычного рабочего состояния.

Обратите внимание, что процесс восстановления после сбоя занимает несколько минут.  Следует исходить из длительности 60 минут для пула, в котором работает 20 000 пользователей.

1.  Не изменяйте пользователей, которые изначально были размещены в Pool1, и произошел сбой при переходе на Pool2, введя следующий командлет:
    
        Invoke-CsPoolFailback -PoolFQDN <Pool1 FQDN> -Verbose

Никаких других действий не требуется. Если вы отошел сбой на центральном сервере управления, вы можете оставить его в Pool2.

</div>

<span> </span>

</div>

</div>

</div>

