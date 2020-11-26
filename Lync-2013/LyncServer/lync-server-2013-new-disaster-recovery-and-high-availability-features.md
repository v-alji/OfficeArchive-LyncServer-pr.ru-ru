---
title: 'Lync Server 2013: новые возможности высокой доступности и аварийного восстановления'
description: 'Lync Server 2013: новые возможности аварийного восстановления и обеспечения высокой доступности.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: New disaster recovery and high availability features
ms:assetid: 4fa7cd0f-784b-4d3f-b839-432c2ecaf7c1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204892(v=OCS.15)
ms:contentKeyID: 48184130
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 92816f61b66d9eed76c16286aaa6c7392dca7708
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425116"
---
# <a name="new-disaster-recovery-and-high-availability-features-in-lync-server-2013"></a>Новые возможности высокой доступности и аварийного восстановления в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-09-20_

Как и в Lync Server 2010, основная схема высокой доступности для Lync Server 2013 основывается на избыточности сервера посредством группировки. При сбое сервера с определенными ролями остальные серверы в пуле с такими же ролями берут на себя нагрузку этого сервера. Это касается серверов переднего плана, пограничных серверов, серверов-посредников и Директоров.

Lync Server 2013 добавляет новые показатели аварийного восстановления, позволяя связывать пулы интерфейсов, расположенные в двух центрах обработки данных. Если один из сопоставленных пулов выходит из строя, администратор может перенести пользователей из этого пула в другой пул в паре для предоставления возможности продолжения обслуживания. Эта функция не требует дорогостоящих сетевых и аппаратных решений, таких как сети хранения данных или общие диски.

Lync Server 2013 также добавляет полную доступность сервера для серверной части. Это необязательная топология, в которой развертывается два серверных сервера для пула переднего плана, а также синхронное зеркальное отображение SQL для всех баз данных Lync, запущенных на серверном сервере. Вы можете выбрать, нужно ли развертывать следящий сервер для зеркала.

<div>

## <a name="see-also"></a>См. также


[Планирование высокой доступности и аварийного восстановления в Lync Server 2013](lync-server-2013-planning-for-high-availability-and-disaster-recovery.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

