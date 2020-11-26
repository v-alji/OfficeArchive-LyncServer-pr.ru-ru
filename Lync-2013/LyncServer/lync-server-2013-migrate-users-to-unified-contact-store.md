---
title: 'Lync Server 2013: перенос пользователей в единое хранилище контактов'
description: 'Lync Server 2013: перенос пользователей в единое хранилище контактов.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Migrate users to unified contact store
ms:assetid: 215a8ec1-d63e-4fdf-b73d-75aeb9dddb43
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204737(v=OCS.15)
ms:contentKeyID: 48183600
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9e9ee9850cc723ae132f15d7c0c6b3769e1240ba
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425593"
---
# <a name="migrate-users-to-unified-contact-store-in-lync-server-2013"></a>Перенос пользователей в единое хранилище контактов в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-10-15_

Пользовательские контакты автоматически переносятся на сервер Exchange 2013, когда пользователь:

  - Назначена политика пользовательских служб, у которой UcsAllowed установлено значение true.

  - Была настроена с помощью почтового ящика Exchange 2013 и один раз вошел в почтовый ящик.

  - Войдите в систему с помощью клиента Lync 2013 с богатыми возможностями.

Если пользователь входит в систему с помощью клиента Lync 2010 или более ранней версии или пользователь не подключен к серверу Exchange 2013, политика служб пользователей игнорируется, а контакты пользователя остаются в Lync Server.

Чтобы определить, перенесены ли контакты пользователя, используйте один из указанных ниже способов.

  - На клиентском компьютере проверьте следующий раздел реестра:
    
    Приложение hKey для \_ текущего \_ пользователя \\ \\ Microsoft \\ Office \\ 15,0 \\ Lync \\ \<SIP URL\> \\ UCS
    
    Если контакты пользователя хранятся в Exchange 2013, в этом разделе содержится значение InUCSMode со значением 2165.

  - Запустите командлет **Test-CsUnifiedContactStore** . В командной строке оболочки Lync Server Management Shell введите:
    
        Test-CsUnifiedContactStore -UserSipAddress "sip:kenmyer@litwareinc.com" -TargetFqdn "atl-cs-001.litwareinc.com"
    
    Если **тест-CsUnifiedContactStore** выполняется успешно, контакты пользователя были перенесены в единое хранилище контактов.

</div>

<span> </span>

</div>

</div>

</div>

