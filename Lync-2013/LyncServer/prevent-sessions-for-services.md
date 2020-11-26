---
title: Запрет сеансов для служб
description: Предотвращение сеансов для служб.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Prevent sessions for services
ms:assetid: 4b541c72-cdc1-4f86-a5a8-c43c24f41d8b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688049(v=OCS.15)
ms:contentKeyID: 49733642
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a452f8091716daa0a15967e2a278e82c5bc8c4f3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438465"
---
# <a name="prevent-sessions-for-services"></a>Запрет сеансов для служб

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-10-04_

С помощью панели управления Microsoft Lync Server 2010 можно запретить новые сеансы для всех служб Lync Server 2010, запущенных на определенном компьютере, или запретить новые сеансы для конкретной службы Lync Server 2010.

<div>

## <a name="to-prevent-new-sessions-for-all-lync-server-services-on-a-computer"></a>Запрещение новых сеансов для всех служб Lync Server на компьютере

1.  Войдите в учетную запись пользователя, которая является членом группы RTCUniversalServerAdmins (или имеет эквивалентные права пользователей) или назначьте роль CsServerAdministrator или CsAdministrator, выполните вход на любой компьютер в сети, в которой вы развернули Lync Server 2013.

2.  Откройте Панель управления Lync Server.

3.  На панели навигации слева щелкните **топология** и выберите **состояние**.

4.  На странице " **состояние** " выполните сортировку или поиск по списку, если это необходимо, чтобы найти компьютер, на котором запущены службы, для которых вы хотите запретить новые сеансы, а затем щелкните его.

5.  Нажмите кнопку **действие**.

6.  Нажмите кнопку **запретить новые сеансы для всех служб**.

</div>

<div>

## <a name="to-prevent-new-sessions-for-a-specific-service"></a>Запрещение новых сеансов для конкретной службы

1.  Войдите в учетную запись пользователя, которая является членом группы RTCUniversalServerAdmins (или имеет эквивалентные права пользователей) или назначьте роль CsServerAdministrator или CsAdministrator, выполните вход на любой компьютер в сети, в которой вы развернули Lync Server 2013.

2.  Откройте Панель управления Lync Server.

3.  На панели навигации слева щелкните **топология** и выберите **состояние**.

4.  На странице " **состояние** " выполните сортировку и поиск по списку, если это необходимо, чтобы найти компьютер, на котором запущена служба, которую вы хотите запустить или остановить, а затем щелкните ее.

5.  Нажмите кнопку **Свойства**.

6.  При необходимости отсортируйте список служб и выберите службу, для которой вы хотите запретить новые сеансы.

7.  Нажмите кнопку **действие**.

8.  Выберите команду **запретить новые сеансы для службы**.

9.  Нажмите кнопку **Закрыть**.

</div>

</div>

<span> </span>

</div>

</div>

</div>

