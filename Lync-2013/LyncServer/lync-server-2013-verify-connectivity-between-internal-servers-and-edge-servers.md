---
title: Проверка подключения между внутренними и пограничными серверами
description: Проверка соединения между внутренними и пограничными серверами.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Verify connectivity between internal servers and Edge Servers
ms:assetid: 219f706e-2b8a-46c5-b394-c384240eef50
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398292(v=OCS.15)
ms:contentKeyID: 48183602
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f86f87428d7eaf91b8f70422cfee712584252fad
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399799"
---
# <a name="verify-connectivity-between-internal-servers-and-edge-servers-in-lync-server-2013"></a>Проверка подключения между внутренними и пограничными серверами в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-09-08_

В Lync Server 2013 имеется отдельный мастер проверки, помогающий проверить связь между пограничными серверами и внутренними серверами. В Lync Server 2013 проверка подключения выполняется автоматически при установке пограничного сервера.

Вы можете проверить репликацию сведений о конфигурации до края, запустив командлет Windows PowerShell **Get-CsManagementStoreReplicationStatus** на внутреннем компьютере, на котором расположено хранилище Центрального управления (или на любом компьютере, подключенном к домену, на котором установлен компонент Lync Server 2013 Core Components (OcsCore.msi). Начальные результаты могут содержать состояние "false", а не "истина" для репликации. Если это так, запустите командлет **Invoke-CsManagementStoreReplication** и разрешите время завершения репликации, прежде чем запускать командлет **Get-CsManagementStoreReplicationStatus** еще раз.

Вы можете проверить подключение внешних пользователей по отдельности, в том числе с помощью анализатора удаленных подключений Office Communications Server для проверки подключения удаленных пользователей. Дополнительные сведения можно найти [в разделе Проверка подключения внешних пользователей в Lync Server 2013](lync-server-2013-verify-connectivity-for-external-users.md).

</div>

<span> </span>

</div>

</div>

</div>

