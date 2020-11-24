---
title: Замечания по сосуществованию
description: Рекомендации по сосуществованию.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Coexistence considerations
ms:assetid: 9d1a3c0f-492a-4e37-bc2f-63509e328785
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205131(v=OCS.15)
ms:contentKeyID: 48184990
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fd1f9525b37bdee3249e0e47352fdea1bc7f012f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399181"
---
# <a name="coexistence-considerations"></a>Замечания по сосуществованию

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-10-06_

После миграции будет существовать только сервер Lync Server 2013, пул серверов сохраняемого чата, и вы можете списать устаревшее развертывание.

Перед тем как вы завершите миграцию и до того, как вы полностью намерены списать текущее развертывание сервера группового чата, вы можете использовать любое из указанных ниже развертываний.

  - Сервер Lync Server 2013, пул серверов сохраняемого чата, который должен находиться в пуле Lync Server 2013.

  - Lync Server 2010, пул группового чата, который должен быть расположен в пуле Lync Server 2010.

  - Пул группового чата Office Communications Server 2007 R2, который должен быть расположен в пуле Office Communications Server 2007 R2.

Эти развертывания могут находиться рядом друг с другом. Однако категории, комнаты и надстройки в одном развертывании не взаимодействуют с теми, которые находятся в сопутствующем развертывании.

При использовании ручного конфигурирования для Office Communications Server 2007 R2, Lync Server 2010, группового чата или Lync Server 2013 вы можете подключаться к одному пулу за один из стандартных клиентов (клиент группового чата).

Lync 2013 (клиент) может взаимодействовать только с серверным пулом Lync Server 2013, сохраняемым чат, а не с пулами серверов группового чата. Для использования сохраняемого чата в Lync 2013 (клиент) пользователь должен быть расположен в Lync 2013 и включен в соответствии с политикой.

</div>

<span> </span>

</div>

</div>

</div>

