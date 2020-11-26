---
title: 'Lync Server 2013: Настройка параметров рисунка по умолчанию'
description: 'Lync Server 2013: Настройка параметров рисунка по умолчанию.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring default picture options
ms:assetid: b1c986f0-6400-447a-9e36-78c1c3a4f793
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn205074(v=OCS.15)
ms:contentKeyID: 56280893
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6261aca82b4c71eb8e0573e8d2adbfc008e743fc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433215"
---
# <a name="configuring-default-picture-options-in-lync-server-2013"></a>Настройка параметров рисунка по умолчанию в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2013-03-22_

По умолчанию рисунки пользователей отображаются автоматически. Если пользователи хотят скрыть свои рисунки, они смогут выбрать параметр **скрыть мою фотографию** в клиенте Lync. Тем не менее этот параметр игнорируется некоторыми другими приложениями Office.

Если возможность отображения рисунков даже при выключенном пользователе является проблемой, вы можете изменить параметры отображения рисунков Lync глобально или для сайта или службы таким образом, чтобы изображения пользователей не отображались по умолчанию. Используйте следующий командлет командной консоли Lync Server, чтобы изображения пользователя не отображались, пока не будет явно указан параметр " **Показывать мои рисунки** " в клиенте:

    Set-CsPrivacyConfiguration -DisplayPublishedPhotoDefault $False

Дополнительные сведения об этом командлете можно найти в документации [Set-CsPrivacyConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsPrivacyConfiguration) в командной консоли Lync Server Management Shell.

</div>

<span> </span>

</div>

</div>

</div>

