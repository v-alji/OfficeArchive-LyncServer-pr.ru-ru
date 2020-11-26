---
title: 'Lync Server 2013: предотвращение сеансов для служб'
description: 'Lync Server 2013: предотвращение сеансов для служб.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Prevent sessions for services
ms:assetid: 977dcc5c-2aac-48ef-86a1-a8d47b4d9e74
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182553(v=OCS.15)
ms:contentKeyID: 48184866
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 846a9da5330c3e64f61c27dfadd883f0c43a0ffa
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436904"
---
# <a name="prevent-sessions-for-services-in-lync-server-2013"></a>Предотвращение сеансов для служб в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-11-01_

Панель управления Lync Server можно использовать для предотвращения новых сеансов для всех служб Lync Server 2013, запущенных на определенном компьютере, или для предотвращения новых сеансов для конкретной службы Lync Server 2013.

<div>

## <a name="to-prevent-new-sessions-for-all-lync-server-services-on-a-computer"></a>Запрещение новых сеансов для всех служб Lync Server на компьютере

1.  Войдите в учетную запись пользователя, которая является членом группы RTCUniversalServerAdmins (или имеет эквивалентные права пользователей) или назначьте роль CsServerAdministrator или CsAdministrator, выполните вход на любой компьютер в сети, в которой вы развернули Lync Server 2013.

2.  Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server. Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).

3.  На панели навигации слева щелкните **топология** и выберите **состояние**.

4.  На странице " **состояние** " выполните сортировку или поиск по списку, если это необходимо, чтобы найти компьютер, на котором запущены службы, для которых вы хотите запретить новые сеансы, а затем щелкните его.

5.  Нажмите кнопку **действие**.

6.  Нажмите кнопку **запретить новые сеансы для всех служб**.

</div>

<div>

## <a name="to-prevent-new-sessions-for-a-specific-service"></a>Запрещение новых сеансов для конкретной службы

1.  Войдите в учетную запись пользователя, которая является членом группы RTCUniversalServerAdmins (или имеет эквивалентные права пользователей) или назначьте роль CsServerAdministrator или CsAdministrator, выполните вход на любой компьютер в сети, в которой вы развернули Lync Server 2013.

2.  Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server. Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).

3.  На панели навигации слева щелкните **топология** и выберите **состояние**.

4.  На странице " **состояние** " выполните сортировку и поиск по списку, если это необходимо, чтобы найти компьютер, на котором запущена служба, которую вы хотите запустить или остановить, а затем щелкните ее.

5.  Нажмите кнопку **Свойства**.

6.  При необходимости отсортируйте список служб и выберите службу, для которой вы хотите запретить новые сеансы.

7.  Нажмите кнопку **действие**.

8.  Выберите команду **запретить новые сеансы для службы**.

9.  Нажмите кнопку **Закрыть**.

</div>

<div>

## <a name="see-also"></a>См. также


[Управление топологией Lync Server 2013](lync-server-2013-managing-the-lync-server-topology.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

