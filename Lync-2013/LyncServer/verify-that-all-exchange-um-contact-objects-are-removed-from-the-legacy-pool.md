---
title: Проверка того, что все объекты контактов Exchange UM удалены из устаревшего пула
description: Убедитесь, что все объекты контакта Exchange UM удалены из устаревшего пула.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Verify that all Exchange UM Contact objects are removed from the legacy pool
ms:assetid: 5a813169-0ed7-4f84-a242-ed2cd4ea5c43
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688068(v=OCS.15)
ms:contentKeyID: 49733664
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8af5dea6cf746c55d8fecf074e132f721c380de1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440138"
---
# <a name="verify-that-all-exchange-um-contact-objects-are-removed-from-the-legacy-pool"></a>Проверка того, что все объекты контактов Exchange UM удалены из устаревшего пула

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-09-26_

С помощью средства **OCSUmUtil** или командлета **Get-CsExumContact** убедитесь в том, что объекты контактов Exchange UM были удалены из устаревшего пула Office Communications Server 2007 R2. **OCSUmUtil** находится в следующей папке:

% Программных файлов% \\ распространенных файлов \\ Lync Server 2013 \\ support \\OcsUMUtil.exe

**OCSUmUtil** необходимо запускать из учетной записи пользователя:

  - Членство в группе RTCUniversalServerAdmins и RTCUniversalUserAdmins (которая включает права на чтение параметров единой системы обмена сообщениями Exchange Server)

  - Права домена на создание объектов контакта в указанном контейнере подразделения

Дополнительные сведения об использовании командлета **Get-CsExumContact** можно найти в документации [Get-CsExumContact](https://docs.microsoft.com/powershell/module/skype/Get-CsExUmContact) в командной консоли Lync Server Management Shell.

</div>

<span> </span>

</div>

</div>

</div>

