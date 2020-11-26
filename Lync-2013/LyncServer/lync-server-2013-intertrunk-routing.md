---
title: 'Lync Server 2013: маршрутизация между каналами'
description: 'Lync Server 2013: межмагистральный маршрут.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Intertrunk routing
ms:assetid: d3a33b4a-8bf4-4a8c-a371-8ef79e740780
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205272(v=OCS.15)
ms:contentKeyID: 48185442
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 30c838ee94a2df0807195c172d7e2a3a393523af
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426775"
---
# <a name="intertrunk-routing-in-lync-server-2013"></a>Маршрутизация между каналами в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-10-20_

Lync Server 2013 может использовать IP-УАТС с шлюзом коммутируемой телефонной сети (PSTN), чтобы звонки с телефонной АТС могли перенаправляться на телефон, входящий в протокол PSTN. Аналогичным образом Lync Server 2013 может использоваться для объединения двух или более систем УАТС IP и обмена звонками между телефонами УАТС из различных систем IP-УАТС.

Эту функцию маршрутизации по межмагистрали можно настроить с помощью командлета командной консоли Lync Server, **Set-CsTrunkConfiguration** с новым параметром PstnUsages. Этот параметр указывает набор записей использования КТСОП для использования. Магистраль использует это использование PSTN для определения маршрута и для маршрутизации всех входящих вызовов соответственно.

    Set-CsTrunkConfiguration -Identity <TrunkId> -PstnUsages @{add="<UsageString>"}

На следующей схеме показана интеграция сервера Lync Server 2013, обеспечивающая взаимодействие между шлюзом PSTN и IP-УАТС.

**Межмагистральная маршрутизация между шлюзом и IP-УАТС**

![Схема подключения Lync Server к ТСОП-шлюзу/IP-УАТС](images/JJ721940.cc3858ca-2ee3-4d51-8a51-db078366b50b(OCS.15).jpg "Схема подключения Lync Server к ТСОП-шлюзу/IP-УАТС")

На следующей схеме показана платформа Lync Server 2013, соединяющая две системы IP-УАТС.

**Межмагистральная маршрутизация между двумя IP-АТС**

![Схема соединений между системами IP-УАТС с помощью Lync Server](images/JJ721940.6ba18ec9-df70-498a-9cf7-7fc41e5ec432(OCS.15).jpg "Схема соединений между системами IP-УАТС с помощью Lync Server")

</div>

<span> </span>

</div>

</div>

</div>

