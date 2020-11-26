---
title: Проверка репликации параметров конфигурации
description: Проверка репликации параметров конфигурации.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Validate replication of configuration settings
ms:assetid: 81a3c21d-b28a-4287-adac-11791e8db56d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205042(v=OCS.15)
ms:contentKeyID: 48184663
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 26d8e9326da8b865f4e2ca3181975fb899300636
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446537"
---
# <a name="validate-replication-of-configuration-settings"></a>Проверка репликации параметров конфигурации

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-10-19_

Вы можете проверить репликацию сведений о конфигурации на пограничном сервере, запустив командлет Lync Server 2013 **Get-CsManagementStoreReplicationStatus** на внутреннем компьютере, на котором находится корневой центр управления, или на любом компьютере, подключенном к домену, на котором установлен компонент lync Server 2013.

Начальные результаты могут содержать состояние "false", а не "истина" для репликации. Если это так, выполните командлет **Invoke-CsManagementStoreReplication** и разрешите время завершения репликации, прежде чем запускать командлет **Get-CsManagementStoreReplicationStatus** еще раз.

</div>

<span> </span>

</div>

</div>

</div>

