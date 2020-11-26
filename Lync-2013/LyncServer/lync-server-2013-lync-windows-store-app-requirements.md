---
title: 'Lync Server 2013: требования к приложению в магазине Lync из Магазина Windows'
description: 'Lync Server 2013: требования к приложению в магазине Lync из Магазина Windows.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Lync Windows Store app requirements
ms:assetid: 5f2e0a40-8450-4f61-b6f6-913fc1906020
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ823129(v=OCS.15)
ms:contentKeyID: 50120200
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 17e8705a55625bcf0ad099ead1000a82c994d867
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426169"
---
# <a name="lync-windows-store-app-requirements-for-lync-server-2013"></a>Требования к приложению Lync из Магазина Windows для Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2013-12-03_

Организации с локальным развертыванием сервера Lync Server должны соответствовать следующим требованиям для поддержки приложения Lync из Магазина Windows.

<div>


> [!NOTE]  
> Для Lync Server 2010 Запустите накопительное обновление для Lync Server 2010: Февраль 2012 (доступно по адресу <A class=uri href="https://go.microsoft.com/fwlink/?linkid=3052%26kbid=2670352"> https://go.microsoft.com/fwlink/?linkid=3052&amp ; kbid = 2670352</A>) или более поздней версии на всех серверах. Чтобы разрешить пользователям присоединяться к собраниям, запустите накопительное обновление для Lync Server 2010: Октябрь 2012 (доступно по адресу <A class=uri href="https://go.microsoft.com/fwlink/?linkid=3052%26kbid=2737915"> https://go.microsoft.com/fwlink/?linkid=3052&amp ; kbid = 2737915</A>) на серверах.



</div>

  - Включите функцию автообнаружения, Lync Web App и службы веб-билета на сервере.

  - Включите проверку подлинности на сертификате на сервере переднего плана или в пуле внешних интерфейсов. (Процесс регистрации пользователей на сервере переднего плана или в пуле переднего плана часто называется регистратором). Подробности можно найти [в разделе Создание параметров конфигурации регистратора в Lync Server 2013](lync-server-2013-create-registrar-configuration-settings.md).

  - Опубликуйте записи ресурсов псевдонимов DNS (CNAME) для службы автообнаружения.

  - Больше не требуется, чтобы точка распространения списка отзыва сертификатов (CDP) для сертификатов, выданных в Lync Server, указывала на ресурс HTTP, а не на ресурс LDAP. Тем не менее убедитесь, что на клиентских компьютерах установлены последние обновления Windows.

  - Настройте прокси-серверы HTTP в корпоративной сети, чтобы разрешить трафик HTTP, связанный с Lync Server.  При необходимости добавьте исключения для служб автообнаружения, Lync Web App и веб-билета.

  - На клиентских компьютерах установите Windows 8,1 и последнюю версию приложения Lync из Магазина Windows, чтобы устранить проблему с входом, которая обычно происходит при использовании нескольких доменов (например, если URI SIP — **userA@domainZ.com** , но пограничный сервер — **SIP.domainX.com**).

Если ваша организация подписалась на Lync Online или Microsoft 365, а вы используете свое собственное доменное имя, вы должны выполнить дополнительные действия, чтобы настроить сеть для автоопределения серверов Lync. Требования к конфигурации сети одинаковы для приложения Lync из Магазина Windows и Lync на мобильных устройствах.

<div>

## <a name="see-also"></a>См. также


[Развертывание приложения Lync из Магазина Windows в Lync Server 2013](lync-server-2013-deploying-lync-windows-store-app.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>
