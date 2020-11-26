---
title: Проверка федерации и удаленного доступа для внешних пользователей
description: Проверьте Федерацию и удаленный доступ для внешних пользователей.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Verify federation and remote access for external users
ms:assetid: a383fefb-c428-4462-93fd-15ba540fa867
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688163(v=OCS.15)
ms:contentKeyID: 49733768
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1ac36f2e1b6c5ddfd889810ba2a3ab4d82b7ae33
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446474"
---
# <a name="verify-federation-and-remote-access-for-external-users"></a>Проверка федерации и удаленного доступа для внешних пользователей

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-09-18_

После перевода маршрута Федерации на граничный сервер Lync Server 2013 необходимо выполнить несколько функциональных тестов, чтобы убедиться, что она работает должным образом. Для проверки внешнего доступа пользователей следует включить все типы внешних пользователей, которые поддерживаются вашей организацией, в том числе любые из указанных ниже элементов.

<div>

## <a name="test-connectivity-of-external-users-and-external-access"></a>Проверка подключения внешних пользователей и внешнего доступа

  - Пользователи, у которых есть хотя бы один федеративный домен, внутренний пользователь на Lync Server 2013 и пользователь на Lync Server 2010. Протестируйте обмен мгновенными сообщениями, присутствие, звук и видео (A/V) и общий доступ к рабочему столу.

  - Пользователи всех общедоступных служб обмена мгновенными сообщениями, которые поддерживаются вашей организацией (и для которых была выполнена подготовка) взаимодействия с пользователем в Lync Server 2013 и пользователем на Lync Server 2010.

  - Убедитесь в том, что анонимные пользователи смогут присоединиться к конференциям.

  - Пользователь, размещенный на Lync Server 2010 с удаленным доступом пользователей (вход в Lync Server 2010 из-за пределов интрасети, но не VPN) с пользователем на Lync Server 2013 и пользователем на Lync Server 2010. Проверка обмена мгновенными сообщениями, сведений о присутствии, а/V и совместном использовании рабочего стола.

  - Пользователь, размещенный на Lync Server 2013 с удаленным доступом пользователей (вход в Lync Server 2013 из-за пределов интрасети, но не VPN) с пользователем на Lync Server 2013 и пользователем на Lync Server 2010. Проверка обмена мгновенными сообщениями, сведений о присутствии, а/V и совместном использовании рабочего стола.

</div>

</div>

<span> </span>

</div>

</div>

</div>

