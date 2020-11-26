---
title: Миграция сервера обновлений
description: Перенесите сервер исправлений.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migrate Mediation Server
ms:assetid: b0b77121-2c8f-413e-b276-dbf1038361d3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205173(v=OCS.15)
ms:contentKeyID: 48185117
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 31cc4c95f0e9c86b48594238218db22f3ec1a387
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446873"
---
# <a name="migrate-mediation-server"></a>Миграция сервера обновлений

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-09-28_

После запуска мастера слияния сервер, на котором работает ваш компьютер, будет объединен с пробной топологией Lync Server 2013. Однако настройка сервера обновлений Lync Server 2013 выполняется после миграции всех пользователей, так как пул Office Communications Server 2007 R2 не может взаимодействовать с сервером обновлений Lync Server 2013. В ходе параллельной миграции сервер Lync Server 2013 взаимодействует с сервером Office Communications Server 2007 R2.

При настройке сервера исправлений Lync Server 2013 Вы также должны обновить или заменить шлюзы Office Communications Server 2007 R2. Шлюзы Office Communications Server 2007 R2 не поддерживают сервер обновлений Lync Server 2013. Необходимо развернуть шлюзы, сертифицированные для Lync Server 2013, и связать их с сервером обновлений Lync Server 2013. Этот этап необходим для того, чтобы можно было полностью списать развертывание Office Communications Server 2007 R2.

В этом разделе описаны задачи настройки, которые необходимо выполнить после миграции сервера обновлений Lync Server 2013. Переход на размещенный сервер исправлений на отдельном сервере — это необязательная задача.

  - [Настройка сервера обновлений](configure-mediation-server.md)

  - [Изменение маршрутов голосовой связи для использования нового сервера исправлений Lync Server 2013](change-voice-routes-to-use-the-new-lync-server-2013-mediation-server.md)

  - [Переход размещенного сервера исправлений на отдельный сервер-посредник (необязательно)](transition-a-collocated-mediation-server-to-a-stand-alone-mediation-server-optional.md)

</div>

<span> </span>

</div>

</div>

</div>

