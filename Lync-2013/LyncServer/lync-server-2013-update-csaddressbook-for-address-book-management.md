---
title: 'Lync Server 2013: Update-CsAddressBook для управления адресными книгами'
description: 'Lync Server 2013: Update-CsAddressBook для управления адресными книгами.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Update-CsAddressBook for Address Book management
ms:assetid: 0ffd2ef8-201c-44aa-8c64-1c7b0eaa7d48
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429695(v=OCS.15)
ms:contentKeyID: 48183428
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4adc7f94e2f31f64f6517b8cdf9bbcb0649f6c8b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399478"
---
# <a name="update-csaddressbook-for-address-book-management-in-lync-server-2013"></a>Update-CsAddressBook для управления адресной книгой в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-11-01_

Кто может запустить этот командлет: по умолчанию членам следующих групп разрешено выполнять командлет Update-CsAddressBook локально: RTCUniversalUserAdmins, RTCUniversalServerAdmins. Чтобы возвратить список всех ролей управления доступом на основе ролей (RBAC), которые назначены этому командлету (включая любые пользовательские роли RBAC, созданные пользователем), выполните в командной строке Windows PowerShell следующую команду:

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Update-CsAddressBook"}

Командлет Update-CsAddressBook заменяет команду **abserver.exe – syncNow** из Office Communications Server. Цель командлета состоит в том, чтобы начать синхронизацию немедленно, вместо того чтобы ждать запланированного времени. Первый пример команды обновляет все адресные книги в Организации. Вторая обновляет только адресную книгу, связанную с определенным сервером.

<div>


> [!NOTE]  
> В Lync Server 2013 служба репликатора пользователей Lync Server выберет изменения из Active Directory и обновит базу данных пользователей Lync Server на основе заданного интервала. Служба репликации пользователей Lync Server также будет автоматически распространять изменения базы данных RTCab, не требуя администратора запускать Update-CSAddressBook. Администраторам потребуется выполнить Update-CSAddressBook только в том случае, если разрешена загрузка файла адресной книги.



</div>

Например:

   ```PowerShell
    Update-CsAddressBook
   ```

   ```PowerShell
    Update-CsAddressBook -Fqdn atl-abs-001.contoso.com
   ```

<div>

## <a name="see-also"></a>См. также


[Update-CsAddressBook](https://docs.microsoft.com/powershell/module/skype/Update-CsAddressBook)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

