---
title: 'Lync Server 2013: изменения, внесенные Grant-CsOUPermission'
description: 'Lync Server 2013: изменения, внесенные функцией Grant-CsOUPermission.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Changes made by Grant-CsOUPermission
ms:assetid: d744d352-1ad9-4447-8e2b-28e768d2ed1b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205310(v=OCS.15)
ms:contentKeyID: 48185564
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 10d3db0e9dde380628690bc016e2b4bd2ec85b54
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435056"
---
# <a name="changes-made-by-grant-csoupermission-in-lync-server-2013"></a>Изменения, внесенные в Grant-CsOUPermission в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-06-20_

Чтобы делегировать администрирование Lync Server 2013, вы можете добавить разрешения для указанных организационных подразделений, чтобы участники универсальных групп RTC, созданные с помощью подготовки леса, могли получать доступ к подразделениям без участия в группе Администраторы домена.

Командлет **Grant-CsOuPermission** предоставляет разрешения на доступ к объектам в указанном подразделении, как указано в приведенных ниже таблицах.

<div>

## <a name="granting-permission-for-user-objects"></a>Предоставление разрешений для объектов пользователей

Когда вы запускаете командлет **Grant-CsOuPermission** для объектов пользователей в подразделении, группам предоставляются разрешения, как показано в приведенной ниже таблице.

### <a name="permissions-granted-for-user-objects"></a>Разрешения, предоставленные для объектов пользователя

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Сгруппирован</th>
<th>PermissionSet</th>
<th>Применимо к</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>RTCHSUniversalServices</p></td>
<td><p>Репликация изменений каталога</p></td>
<td><p>Только этот объект</p></td>
</tr>
<tr class="even">
<td><p>RTCUniversalServerReadOnlyGroup</p></td>
<td><p>Содержимое списка</p>
<p>Чтение всех свойств</p>
<p>Разрешения на чтение</p></td>
<td><p>Только этот объект</p></td>
</tr>
<tr class="odd">
<td><p>RTCUniversalUserReadOnlyGroup</p></td>
<td><p>Содержимое списка</p>
<p>Чтение всех свойств</p>
<p>Разрешения на чтение</p></td>
<td><p>Только этот объект</p></td>
</tr>
<tr class="even">
<td><p>RTCUniversalUserReadOnlyGroup</p></td>
<td><p>Прочитать RTCUserSearchPropertySet</p>
<p>Прочитать RTCUserProvisioningPropertySet</p>
<p>Прочитать RTCPropertySet</p>
<p>Чтение Public-Information</p>
<p>Чтение General-Information</p>
<p>Чтение ограничений для учетных записей пользователей</p></td>
<td><p>Дочерние объекты пользователей</p></td>
</tr>
<tr class="odd">
<td><p>RTCUniversalUserAdmins</p></td>
<td><p>Напишите RTCUserSearchPropertySet</p>
<p>Напишите msExchUCVoiceMailSettings</p>
<p>Напишите RTCUserProvisioningPropertySet</p>
<p>Напишите RTCPropertySet</p>
<p>Напишите proxyAddresses</p></td>
<td><p>Дочерние объекты пользователей</p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="granting-permission-for-computer-objects"></a>Предоставление разрешений на доступ к объектам компьютера

Когда вы запускаете командлет **Grant-CsOuPermission** для объектов компьютеров в подразделении, группам предоставляются разрешения, как показано в приведенной ниже таблице.

### <a name="permissions-granted-for-computer-objects"></a>Разрешения, предоставленные для объектов компьютера

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Сгруппирован</th>
<th>PermissionSet</th>
<th>Применимо к</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>RTCHSUniversalServices</p></td>
<td><p>Репликация изменений каталога</p></td>
<td><p>Только этот объект</p></td>
</tr>
<tr class="even">
<td><p>RTCUniversalServerReadOnlyGroup</p></td>
<td><p>Содержимое списка</p>
<p>Чтение всех свойств</p>
<p>Разрешения на чтение</p></td>
<td><p>Только этот объект</p></td>
</tr>
<tr class="odd">
<td><p>RTCUniversalUserReadOnlyGroup</p></td>
<td><p>Содержимое списка</p>
<p>Чтение всех свойств</p>
<p>Разрешения на чтение</p></td>
<td><p>Только этот объект</p></td>
</tr>
<tr class="even">
<td><p>RTCUniversalUserReadOnlyGroup</p></td>
<td><p>Чтение Public-Information</p>
<p>Проверка на прочтении DNS-Host-Name</p></td>
<td><p>Дочерние объекты компьютера</p></td>
</tr>
<tr class="odd">
<td><p>RTCUniversalUserAdmins</p></td>
<td><p>Чтение Public-Information</p>
<p>Проверка на прочтении DNS-Host-Name</p></td>
<td><p>Дочерние объекты компьютера</p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="granting-permission-for-contact-or-appcontact-objects"></a>Предоставление разрешений на доступ к объектам контакта или AppContact

При запуске командлета **Grant-CsOuPermission** для объектов контакта или объектов AppContact в подразделении группам предоставляются разрешения, описанные в приведенной ниже таблице.

### <a name="permissions-granted-for-contact-or-appcontact-objects"></a>Разрешения, предоставленные для контактных и AppContactных объектов

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Сгруппирован</th>
<th>PermissionSet</th>
<th>Применимо к</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>RTCHSUniversalServices</p></td>
<td><p>Репликация изменений каталога</p></td>
<td><p>Только этот объект</p></td>
</tr>
<tr class="even">
<td><p>RTCUniversalServerReadOnlyGroup</p></td>
<td><p>Содержимое списка</p>
<p>Чтение всех свойств</p>
<p>Разрешения на чтение</p></td>
<td><p>Только этот объект</p></td>
</tr>
<tr class="odd">
<td><p>RTCUniversalUserReadOnlyGroup</p></td>
<td><p>Содержимое списка</p>
<p>Чтение всех свойств</p>
<p>Разрешения на чтение</p></td>
<td><p>Только этот объект</p></td>
</tr>
<tr class="even">
<td><p>RTCUniversalUserReadOnlyGroup</p></td>
<td><p>Прочитать RTCUserSearchPropertySet</p>
<p>Прочитать RTCUserProvisioningPropertySet</p>
<p>Прочитать RTCPropertySet</p>
<p>Чтение Public-Information</p>
<p>Чтение General-Information</p>
<p>Чтение Personal-Information</p>
<p>Чтение ограничений для учетных записей пользователей</p></td>
<td><p>Дочерние объекты контактов</p></td>
</tr>
<tr class="odd">
<td><p>RTCUniversalUserAdmins</p></td>
<td><p>Напишите RTCUserSearchPropertySet</p>
<p>Напишите otherIpPhone</p>
<p>Запись отображаемого текста</p>
<p>Описание записи</p>
<p>Напишите telephoneNumber</p>
<p>Напишите msExchUCVoiceMailSettings</p>
<p>Напишите RTCUserProvisioningPropertySet</p>
<p>Напишите RTCPropertySet</p>
<p>Напишите proxyAddresses</p></td>
<td><p>Дочерние объекты контактов</p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="granting-permission-for-device-objects"></a>Предоставление разрешения на доступ к объектам устройства

Когда вы запускаете командлет **Grant-CsOuPermission** для объектов устройств в подразделении, группам предоставляются разрешения, как показано в приведенной ниже таблице.

### <a name="permissions-granted-for-device-objects"></a>Разрешения, предоставленные для объектов устройства

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Сгруппирован</th>
<th>PermissionSet</th>
<th>Применимо к</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>RTCHSUniversalServices</p></td>
<td><p>Репликация изменений каталога</p></td>
<td><p>Только этот объект</p></td>
</tr>
<tr class="even">
<td><p>RTCUniversalServerReadOnlyGroup</p></td>
<td><p>Содержимое списка</p>
<p>Чтение всех свойств</p>
<p>Разрешения на чтение</p></td>
<td><p>Только этот объект</p></td>
</tr>
<tr class="odd">
<td><p>RTCUniversalUserReadOnlyGroup</p></td>
<td><p>Содержимое списка</p>
<p>Чтение всех свойств</p>
<p>Разрешения на чтение</p></td>
<td><p>Только этот объект</p></td>
</tr>
<tr class="even">
<td><p>RTCUniversalUserReadOnlyGroup</p></td>
<td><p>Прочитать RTCUserSearchPropertySet</p>
<p>Прочитать RTCUserProvisioningPropertySet</p>
<p>Прочитать RTCPropertySet</p>
<p>Чтение Public-Information</p>
<p>Чтение Personal-Information</p>
<p>Чтение General-Information</p>
<p>Чтение ограничений для учетных записей пользователей</p></td>
<td><p>Дочерние объекты контактов</p></td>
</tr>
<tr class="odd">
<td><p>RTCUniversalUserAdmins</p></td>
<td><p>Создание дочернего элемента</p>
<p>Удалить дочерний элемент</p>
<p>Удалить дерево</p></td>
<td><p>Службу</p></td>
</tr>
<tr class="even">
<td><p>RTCUniversalUserAdmins</p></td>
<td><p>Запись отображаемого текста</p>
<p>Описание записи</p>
<p>Напишите telephoneNumber</p></td>
<td><p>Дочерние объекты пользователей</p></td>
</tr>
<tr class="odd">
<td><p>RTCUniversalUserAdmins</p></td>
<td><p>Напишите RTCUserSearchPropertySet</p>
<p>Напишите otherIpPhone</p>
<p>Запись отображаемого текста</p>
<p>Описание записи</p>
<p>Напишите telephoneNumber</p>
<p>Напишите msExchUCVoiceMailSettings</p>
<p>Напишите RTCUserProvisioningPropertySet</p>
<p>Напишите RTCPropertySet</p>
<p>Напишите proxyAddresses</p></td>
<td><p>Дочерние объекты контактов</p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="granting-permission-for-inetorgperson-objects"></a>Предоставление разрешения для объектов InetOrgPerson

При запуске командлета **Grant-CsOuPermission** для объектов inetOrgPerson в подразделении группам предоставляются разрешения, описанные в приведенной ниже таблице.

### <a name="permissions-granted-for-inetorgperson-objects"></a>Разрешения, предоставленные для объектов InetOrgPerson

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Сгруппирован</th>
<th>PermissionSet</th>
<th>Применимо к</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>RTCHSUniversalServices</p></td>
<td><p>Репликация изменений каталога</p></td>
<td><p>Только этот объект</p></td>
</tr>
<tr class="even">
<td><p>RTCUniversalServerReadOnlyGroup</p></td>
<td><p>Содержимое списка</p>
<p>Чтение всех свойств</p>
<p>Разрешения на чтение</p></td>
<td><p>Только этот объект</p></td>
</tr>
<tr class="odd">
<td><p>RTCUniversalUserReadOnlyGroup</p></td>
<td><p>Содержимое списка</p>
<p>Чтение всех свойств</p>
<p>Разрешения на чтение</p></td>
<td><p>Только этот объект</p></td>
</tr>
<tr class="even">
<td><p>RTCUniversalUserReadOnlyGroup</p></td>
<td><p>Прочитать RTCUserSearchPropertySet</p>
<p>Прочитать RTCUserProvisioningPropertySet</p>
<p>Прочитать RTCPropertySet</p>
<p>Чтение Personal-Information</p>
<p>Чтение Public-Information</p>
<p>Чтение General-Information</p>
<p>Чтение ограничений для учетных записей пользователей</p></td>
<td><p>Дочерние объекты inetOrgPerson</p></td>
</tr>
<tr class="odd">
<td><p>RTCUniversalUserAdmins</p></td>
<td><p>Напишите RTCUserSearchPropertySet</p>
<p>Напишите RTCUserProvisioningPropertySet</p>
<p>Напишите RTCPropertySet</p>
<p>Напишите proxyAddresses</p></td>
<td><p>Дочерние объекты inetOrgPerson</p></td>
</tr>
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</div>

