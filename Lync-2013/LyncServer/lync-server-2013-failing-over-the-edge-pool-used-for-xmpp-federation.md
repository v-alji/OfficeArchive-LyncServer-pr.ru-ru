---
title: 'Lync Server 2013: отработка отказа для пограничного пула, используемого для федерации XMPP'
description: 'Lync Server 2013: сбой в пуле EDGE, используемом для XMPP Федерации.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Failing over the Edge pool used for XMPP federation
ms:assetid: 587e7829-a26b-46f8-8aad-b78a7b325b55
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688065(v=OCS.15)
ms:contentKeyID: 49733659
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ccdfe119258b4d09ddedefb22d0272d72003bf04
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428253"
---
# <a name="failing-over-the-edge-pool-used-for-xmpp-federation-in-lync-server-2013"></a>Отработка отказа для пограничного пула, используемого для федерации XMPP в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-10-19_

В вашей организации используется один пул краев, назначенный пулом для XMPP Федерации. Если этот пул отключается, необходимо отдать отказ на XMPP Федерацию для использования другого пула Edge перед тем, как XMPP Федерация сможет снова работать.

После установки пулов EDGE и включения XMPP Федерации вы можете упростить процесс аварийного восстановления, настроив внешние записи DNS SRV для всех пулов Edge для XMPP Федерации, а не только для одной из них. Для каждой из этих записей SRV должен быть установлен другой приоритет. Весь трафик Федерации XMPP проходит через пул с записью SRV с самым высоким приоритетом. Дополнительные сведения о том, как включить и настроить федерацию XMPP, можно найти [в разделе Настройка XMPP Федерации в Lync Server 2013](lync-server-2013-setting-up-xmpp-federation.md).

В описанной ниже процедуре EdgePool1 — пул, изначально размещенный XMPP Federation, и EdgePool2 — пул, который теперь будет размещен XMPP Федерации.

<div>

## <a name="failing-over-the-edge-pool-used-for-xmpp-federation"></a>Сбой в пуле EDGE, используемом для Федерации XMPP

1.  Если вы еще не развернули другой пул пограничных кромок (Кроме того, который в данный момент не работает), разверните этот пул. Подробные сведения можно найти [в разделе Развертывание внешних пользователей Access в Lync Server 2013](lync-server-2013-deploying-external-user-access.md).

2.  На каждом пограничном сервере в новом пограничном пуле, на котором будет размещена XMPP Федерация (EdgePool2), запустите следующий командлет:
    
        Stop-CsWindowsService

3.  Чтобы перенаправить маршрут Федерации XMPP на EdgePool2, выполните следующий командлет:
    
        Set-CsSite Site2 -XmppExternalFederationRoute EdgeServer2.contoso.com
    
    В этом примере Site2 — сайт с пулом EDGE, который теперь будет размещаться на маршруте Федерации XMPP, а EdgeServer2.contoso.com — это полное доменное имя пограничного сервера в этом пуле.

4.  На внешнем DNS-сервере измените запись DNS A для Федерации XMPP, чтобы она указывала на EdgeServer2.contoso.com.

5.  Если у вас еще нет DNS-записи SRV для Федерации XMPP, которая разрешается в пул EDGE, который теперь будет размещаться в XMPP Федерации, необходимо добавить его, как показано в следующем примере. Для этой записи SRV должно быть задано значение Port 5269.
    
        _xmpp-server._tcp.contoso.com

6.  Убедитесь, что в пуле EDGE, на котором будет размещена XMPP Федерация, есть порт 5269, Открытый извне.

7.  Запустите службы на всех пограничных серверах в пограничном пуле, где будет размещаться Федерация XMPP:
    
        Start-CsWindowsService

</div>

</div>

<span> </span>

</div>

</div>

</div>

