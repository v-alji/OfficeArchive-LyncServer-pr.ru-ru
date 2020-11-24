---
title: 'Lync Server 2013: Настройка номеров групп для отправки звонков'
description: 'Lync Server 2013: Настройка номеров групп для отправки звонков.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure call pickup group numbers
ms:assetid: 5cc67f0b-d70d-446a-8db1-befda8671121
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945631(v=OCS.15)
ms:contentKeyID: 51541479
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5ddffae2e385ce6c3fd7a700a9b94a89b1b6679f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49397960"
---
# <a name="configure-call-pickup-group-numbers-in-lync-server-2013"></a>Настройка номеров групп для отправки звонков в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2013-01-30_

Отправка группового звонка осуществляется на основе заявления на приостановку звонков. При развертывании группового приема звонков настраивается таблица на приостановку соединения с диапазонами номеров телефонов, которые обозначены как номера групп для отправки звонков. These group numbers are the numbers that users dial to pick up calls that are ringing for another user.

Like call park orbit numbers, call pickup group numbers need to be virtual extensions that have no user or phone assigned to them. У каждого пула переднего плана, в котором вы развертываете раскладки группового звонка, может быть один или несколько диапазонов номеров групп для раскладки звонков. Диапазоны номеров групп должны быть глобально уникальными в рамках развертывания Lync Server.

<div>

## <a name="in-this-section"></a>Содержание

[Create or modify a Group Call Pickup number range in Lync Server 2013](lync-server-2013-create-or-modify-a-group-call-pickup-number-range.md)

</div>

</div>

<span> </span>

</div>

</div>

</div>

