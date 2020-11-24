---
title: 'Lync Server 2013: компоненты, необходимые для директора'
description: 'Lync Server 2013: компоненты, необходимые для режиссера.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Components required for the Director
ms:assetid: 15c7c8d4-b93f-4386-b2d1-d76dab8f801e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398228(v=OCS.15)
ms:contentKeyID: 48183502
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 57f717b9ddb9557f212321cdab075713a4b85c2d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398239"
---
# <a name="components-required-for-the-director-in-lync-server-2013"></a>Компоненты, необходимые для директора в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-09-08_

Единственный компонент, необходимый для создания и настройки режиссера, — это развертывание роли "Режиссерный сервер". Это можно сделать, воспользовавшись построителем топологии и определив один или несколько пулов компьютеров в узле режиссера пула. Определив пул режиссеров или режиссера, запустите мастер развертывания Lync Server на компьютере, который будет режиссером. В случае с режиссером пула вы запускаете мастер развертывания Lync Server на каждом сервере, который будет входить в пул.

<div>

## <a name="topologies"></a>Топологий

Вы можете внедрить один и тот же Режиссерный сервер или пул. Режиссер всегда является отдельным сервером или пулом, но не может быть размещен с другой ролью сервера в Lync Server 2013.

<div>


> [!NOTE]  
> Если вы не развертываете режиссеров, роль директора будет возлагаться на сервер переднего плана или пул внешних интерфейсов.



</div>

Пул директоров должен быть сбалансированно загружен. Вы можете выполнить одно из указанных ниже действий.

  - Создайте топологию, использующую аппаратную подсистему балансировки нагрузки для веб-служб и балансировки нагрузки DNS для других типов трафика.
    
    [Масштабируемый пул директоров — балансировка нагрузки на DNS и аппаратный балансировщик нагрузки в Lync Server 2013](lync-server-2013-scaled-director-pool-dns-load-balancing-and-hardware-load-balancer.md)

  - Создание топологии, использующей аппаратный балансировщик нагрузки для балансировки нагрузки, необходимый для пула ресурсов.
    
    [Масштабируемый пул директоров — аппаратный балансировщик нагрузки в Lync Server 2013](lync-server-2013-scaled-director-pool-hardware-load-balancer.md)

</div>

</div>

<span> </span>

</div>

</div>

</div>

