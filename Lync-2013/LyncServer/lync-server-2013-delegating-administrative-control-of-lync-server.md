---
title: 'Lync Server 2013: делегирование административного управления Lync Server'
description: 'Lync Server 2013: делегирование административного управления Lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delegating administrative control of Lync Server 2013
ms:assetid: 0f378eff-8ef4-4c60-9fd2-67d7ee259ef8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520951(v=OCS.15)
ms:contentKeyID: 48183418
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a8d3710af2d194a5aa4ebdd7291be2ee58176507
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430765"
---
# <a name="delegating-administrative-control-of-lync-server-2013"></a>Делегирование административного управления Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2013-02-22_

В Lync Server 2013 задачи администрирования делегируются пользователям с помощью новой функции управления доступом на основе ролей (RBAC). При установке сервера Lync Server создаются несколько ролей RBAC. These roles correspond to universal security groups in Active Directory Domain Services. Например, роль RBAC CsHelpDesk соответствует группе CsHelpDesk, которая находится в контейнере Users доменных служб Active Directory. Кроме того, каждая роль RBAC связана с набором командлетов Windows PowerShell для Lync Server. Эти командлеты представляют задачи, которые могут быть выполнены пользователями, которым назначена данная роль RBAC. Например, роль CsHelpDesk назначила командлеты Lock-CsClientPin и UnlockCsClientPin. Это означает, что пользователи, которым назначена роль CsHelpDesk, могут блокировать и разблокирование PIN-кодов пользователей. Однако роль CsHelpDesk не назначила командлету New-CsVoicePolicy. Это означает, что пользователи, которым назначена роль CsHelpDesk, не могут создавать новые политики голосовой связи.

<div>

## <a name="viewing-information-about-rbac-roles"></a>Просмотр сведений о ролях RBAC

Вы можете получить основные сведения о ролях RBAC, выполнив в командной консоли Lync Server следующую команду:

    Get-CsAdminRole

Имейте в виду, что идентификатор роли RBAC (например, CsVoiceAdministrator) имеет прямое сопоставление с группой безопасности, обнаруженной в контейнере Users доменных служб Active Directory.

Чтобы просмотреть список командлетов, назначенных для роли, используйте следующую команду:

    Get-CsAdminRole -Identity "CsHelpDesk" | Select-Object -ExpandProperty Cmdlets

</div>

<div>

## <a name="assigning-an-rbac-role-to-a-user"></a>Назначение роли RBAC пользователю

Чтобы назначить пользователю роль RBAC, необходимо добавить этого пользователя в соответствующую группу безопасности Active Directory. Например, чтобы назначить пользователю роль CsLocationAdministrator, необходимо добавить этого пользователя в группу CsLocationAdministrator. Это можно сделать, выполнив описанные ниже действия.

**Назначение пользователя группе безопасности**

1.  Используя учетную запись, которая имеет разрешение на изменение членства группы Active Directory, войдите в систему на компьютере, на котором установлен компонент "пользователи и компьютеры Active Directory".

2.  Нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Администрирование**, а затем — **Пользователи и компьютеры Active Directory**.

3.  В окне "пользователи и компьютеры Active Directory" разверните имя своего домена и щелкните контейнер " **Пользователи** ".

4.  Щелкните правой кнопкой мыши группу безопасности **CsLocationAdministrator** и выберите пункт **свойства**.

5.  В диалоговом окне **Свойства** на вкладке **члены** нажмите кнопку **добавить**.

6.  В диалоговом окне **Выбор пользователей, компьютеров, контактов или групп** введите имя пользователя или отображаемое имя пользователя, которого нужно добавить в группу (например, **Кен Myer**) в поле **Введите имена объектов, которые нужно выделить** , и нажмите кнопку **ОК**.

7.  В диалоговом окне " **Свойства** " нажмите кнопку **ОК**.

Чтобы убедиться в том, что роль RBAC назначена, используйте командлет [Get-CsAdminRoleAssignment](https://docs.microsoft.com/powershell/module/skype/Get-CsAdminRoleAssignment) , передав командлету значение SAMAccountName (имя для входа в службу каталогов Active Directory) для пользователя. Например, выполните эту команду в командной консоли Lync Server Management Shell:

    Get-CsAdminRoleAssignment  -Identity "kenmyer"

</div>

</div>

<span> </span>

</div>

</div>

</div>

