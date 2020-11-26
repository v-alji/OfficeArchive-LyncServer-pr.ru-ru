---
title: Перенос существующих собраний и содержимого собраний
description: Перенос существующих собраний и содержимого собраний.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migrate existing meetings and meeting content
ms:assetid: 30516731-2ae1-4a6d-a7e1-d3f05778c954
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688011(v=OCS.15)
ms:contentKeyID: 49733599
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d94dd35063a121a057a218c27fdb36e42a155b77
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443806"
---
# <a name="migrate-existing-meetings-and-meeting-content"></a>Перенос существующих собраний и содержимого собраний

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2013-02-22_

При перемещении учетной записи пользователя из Lync Server 2010 на сервер Lync Server 2013 переносятся следующие данные с учетной записью пользователя:

  - **Собрания, уже запланированные пользователем**. Сюда входит перемещение каталогов конференций и данных конференций.

  - **Персональный идентификационный номер пользователя (ПИН-код)**. Текущий ПИН-код пользователя продолжает работать, пока не истечет срок действия или пользователь запросит новый ПИН-код.

Указанные ниже сведения об учетной записи пользователя не перемещаются на новый сервер.

  - **Содержимое собрания**. Чтобы переместить содержимое, совместно используемое во время собрания, например PowerPoint, доска, вложения или данные опроса, используйте параметр **-MoveConferenceData** в составе командлета **Move-CsUser** .

</div>

<span> </span>

</div>

</div>

</div>

