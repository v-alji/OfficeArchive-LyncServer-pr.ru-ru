---
title: 'Lync Server 2013: Test-CsAddressBookService для управления адресными книгами'
description: 'Lync Server 2013: Test-CsAddressBookService для управления адресными книгами.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test-CsAddressBookService for Address Book management
ms:assetid: b88cea74-41fd-4c0e-9284-7135bff27a27
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429720(v=OCS.15)
ms:contentKeyID: 48185206
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 345886c68c814534fcbfd4debfd3be8562fae5a2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444282"
---
# <a name="test-csaddressbookservice-for-address-book-management-in-lync-server-2013"></a>Test-CsAddressBookService для управления адресной книгой в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-11-01_

Кто может запустить этот командлет: по умолчанию членам указанных ниже групп разрешено выполнять командлет Test-CsAddressBookService: RTCUniversalServerAdmins. Чтобы возвратить список всех ролей управления доступом на основе ролей (RBAC), которые назначены этому командлету (включая любые пользовательские роли RBAC, созданные пользователем), выполните в командной строке Windows PowerShell следующую команду:

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Test-CsAddressBookService"}

Lync Server 2013 содержит несколько командлетов, инициирующих искусственные команды для подтверждения того, что определенная функция или функция работает правильно. Test-CsAddressBookService подтверждает, что определенный пользователь может подключаться к локальным файлам веб-службы адресной книги и запрашивать у него локальные файлы.

Например:

    Test-CsAddressBookService -TargetFqdn atl-cs-001.contoso.com -UserCredential contoso\bob -UserSipAddress "sip:bob@contoso.com"

<div>

## <a name="see-also"></a>См. также


[Test-CsAddressBookService](https://docs.microsoft.com/powershell/module/skype/Test-CsAddressBookService)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

