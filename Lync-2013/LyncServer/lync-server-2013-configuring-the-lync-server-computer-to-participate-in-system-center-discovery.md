---
title: Настройка компьютера Lync Server для участия в обнаружении System Center
description: Настройка компьютера Lync Server для участия в обнаружении System Center.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring the Lync Server computer to participate in System Center discovery
ms:assetid: 2f9c9cb0-3120-4571-9cd2-657c2123fe21
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204776(v=OCS.15)
ms:contentKeyID: 48183731
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 44d25ba3de673084b2e64e17790a2776cbe57f07
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432564"
---
# <a name="configuring-the-lync-server-2013-computer-to-participate-in-system-center-discovery"></a>Настройка компьютера Lync Server 2013 для участия в обнаружении System Center

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-10-20_

Чтобы убедиться в том, что новый агент сервера Lync участвует в процессе обнаружения для System Center Operations Manager, необходимо выполнить описанные ниже действия для каждого компьютера, на котором установлена консоль System Center Operations Manager.

1.  На вкладке **Администрирование** выберите пункт **управляемая агентом**.

2.  Right-click the name of the computer, and then click **Properties**. В диалоговом окне **Свойства** на вкладке **Безопасность** выберите **Разрешить этому агенту выступать в качестве прокси-сервера и найдите управляемые объекты на других компьютерах**, а затем нажмите кнопку **ОК**.

После завершения действия 2 перезапустите службу агента работоспособности. (При перезагрузке служба будет "принудительно" обнаружение нового компьютера. Если вы не перезапускает службу, она может занять до 4 часов, прежде чем новый компьютер будет обнаружен с помощью System Center Operations Manager.). После перезагрузки службы убедитесь в том, что в журнале событий Operations Manager на этом компьютере не записываются события ошибок.

</div>

<span> </span>

</div>

</div>

</div>

