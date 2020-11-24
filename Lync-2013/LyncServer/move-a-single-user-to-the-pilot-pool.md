---
title: Перемещение отдельного пользователя в пилотный пул
description: Переместить отдельного пользователя в проект пилотного пула.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Move a single user to the pilot pool
ms:assetid: e9de81a8-40dd-4446-81e7-a2b810eaea50
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205401(v=OCS.15)
ms:contentKeyID: 48185905
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f5f7396ed2d92c7015f01ff6cd6e90fd3998219d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398638"
---
# <a name="move-a-single-user-to-the-pilot-pool"></a>Перемещение отдельного пользователя в пилотный пул

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-09-26_

Вы можете переместить пользователя из пула Lync Server 2010 на сервер Lync Server 2013 для пилотного пула с помощью панели управления Lync Server 2013 или консоли управления Lync Server 2013. В приведенном ниже примере в столбце пула регистратора **pool01.contoso.NET** используется пул Lync Server 2010, а в этот пул будут подключены все шесть пользователей. Используйте описанные ниже процедуры для перемещения пользователя в пул Lync Server 2013 с помощью панели управления Lync Server 2013 и командной консоли Lync Server Management Shell.

<div>

## <a name="to-move-a-user-by-using-the-lync-server-2013-control-panel"></a>Перемещение пользователя с помощью панели управления Lync Server 2013

**Список пользователей на панели управления Lync Server 2013**

![Панель управления Lync Server, диалоговое окно перемещения пользователя](images/JJ721870.a2bce284-0392-4db3-9bb2-9f12699738e7(OCS.15).jpg "Панель управления Lync Server, диалоговое окно перемещения пользователя")

1.  Войдите на сервер переднего плана с помощью учетной записи, являющейся членом группы RTCUniversalServerAdmins или членом административной роли CsAdministrator или CsUserAdministrator.

2.  Откройте **Панель управления Lync Server**.

3.  Нажмите **Пользователи**, затем "Поиск" и **Найти**.

4.  Выберите пользователя, которого вы хотите переместить в пул Lync Server 2013. В данном примере мы будем перемещать пользователя Sara Davis.

5.  В меню **Макрокоманда** выберите **Переместить выбранных пользователей в пул**.

6.  В раскрывающемся списке выберите пул Lync Server 2013.

7.  Нажмите **Макрокоманда** и затем **Переместить выбранных пользователей в пул**. Нажмите **OK**.
    
    ![Перемещение пользователей, диалоговое окно «пул конечных регистраторов»](images/JJ205401.8a375003-dc00-4541-b578-4d88f2010601(OCS.15).png "Перемещение пользователей, диалоговое окно «пул конечных регистраторов»")  

8.  Убедитесь в том, что столбец **пула регистратора** для пользователя теперь содержит пул Lync Server 2013, указывающий на то, что пользователь успешно перемещен.

</div>

<div>

## <a name="to-move-a-user-by-using-the-lync-server-2013-management-shell"></a>Перемещение пользователя с помощью управляющей оболочки Lync Server 2013

1.  Откройте командную консоль Lync Server Management Shell.

2.  В командной строке введите следующую команду:
    
        Move-CsUser -Identity "David Pelton" -Target "pool02.contoso.net"

3.  Затем в командной строке введите следующую команду:
    
        Get-CsUser -Identity "David Pelton"

4.  Идентификатор **RegistrarPool** теперь указывает на пул Lync Server 2013. Присутствие этого удостоверения подтверждает, что пользователь успешно переместился.
    
    ![Вывод из командлета Get-CsUser с фильтром идентификаторов](images/JJ205401.bc5d4672-8068-4475-b882-dbd305c801a9(OCS.15).jpg "Вывод из командлета Get-CsUser с фильтром идентификаторов")  
    
    <div>
    

    > [!NOTE]  
    > Дополнительные сведения о командлете <STRONG>Get-CsUser</STRONG> : <STRONG>Get-Help Get-CsUser-Detailed</STRONG>

    
    </div>

</div>

</div>

<span> </span>

</div>

</div>

</div>

