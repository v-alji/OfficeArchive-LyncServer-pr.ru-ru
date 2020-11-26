---
title: Подключение Survivable Branch Appliance к пулу переднего плана Lync Server 2013
description: Подключение устройства с бесперебойной подразделением к пуле внешних интерфейсов Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Connecting Survivable Branch Appliance to Lync Server 2013 Front End pool
ms:assetid: 3c7ca33f-5295-4d82-9152-41d8bc6f35cf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688026(v=OCS.15)
ms:contentKeyID: 49733616
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6ef917d3db6a1d653ac716d6c078e1df240fb31d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432263"
---
# <a name="connecting-survivable-branch-appliance-to-lync-server-2013-front-end-pool"></a>Подключение Survivable Branch Appliance к пулу переднего плана Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-10-05_

Каждое работающее устройство филиала (SBA) связано с пулом переднего плана, который выступает в качестве регистратора резервных копий для SBA. Когда пул переднего плана обновляется до Lync Server 2013, SBA должен быть связан с пулом переднего плана, пока пул переднего плана будет обновлен. После обновления пула переднего плана SBA можно связать с пулом переднего плана. Это связано с тем, что удаление SBA из топологии в построителе топологии и повторное добавление SBA для Topology Builder. Пользователи, размещенные на SBA, должны быть перемещены в другой пул переднего плана, прежде чем удалять SBA из топологии. После того как SBA снова добавится в топологию, эти пользователи могут быть возвращены в SBA.

Эти действия описаны ниже.

1.  Перемещение пользователей филиалов, размещенных на SBA, в другой пул переднего плана.

2.  Удалите SBA из топологии, чтобы разорвать существующий пул переднего плана в качестве регистратора резервных копий.

3.  Обновите пул переднего плана до Microsoft Lync Server 2013.

4.  Добавьте SBA обратно в топологию.

5.  Свяжите новый пул переднего плана с SBA в качестве регистратора резервных копий.

6.  Переместить пользователей филиалов обратно в SBA.

<div>

## <a name="in-this-section"></a>Содержание

  - [Добавление в топологию сайта филиала устройства для обеспечения связи в филиалах Lync Server 2013](lync-server-2013-add-lync-server-2013-survivable-branch-appliance-branch-site-to-your-topology.md)

  - [Добавление сайта филиала Lync Server 2010 Survivable Branch Appliance в топологию](lync-server-2013-add-lync-server-2010-survivable-branch-appliance-branch-site-to-your-topology.md)

</div>

</div>

<span> </span>

</div>

</div>

</div>

