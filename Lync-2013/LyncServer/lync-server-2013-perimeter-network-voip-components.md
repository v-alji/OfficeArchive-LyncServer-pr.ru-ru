---
title: 'Lync Server 2013: компоненты VoIP для сети периметра'
description: 'Lync Server 2013: компоненты VoIP по периметру сети.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Perimeter network VoIP components
ms:assetid: 74230008-695d-436a-90b9-9cd060c70f7b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398559(v=OCS.15)
ms:contentKeyID: 48184514
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 20a416838b2ccec969e2990d492029486b6f2c72
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437142"
---
# <a name="perimeter-network-voip-components-for-lync-server-2013"></a>Компоненты VoIP для сети периметра для Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-09-21_

За пределами абонентов, использующих единые коммуникационные клиенты для индивидуальных и конференц-связи, на пограничном сервере подается пограничный голосовую связь с коллегами.

На пограничном сервере служба доступа Edge предоставляет сигналы SIP для звонков из пользователей Lync, которые находятся за пределами брандмауэра организации. Пограничная служба аудио- и видеоданных обеспечивает обход трансляторов сетевых адресов и брандмауэров. Вызывающий абонент, работающий с клиентом объединенных коммуникаций (UC) за пределами корпоративного брандмауэра, пользуется пограничной службой аудио- и видеоданных как для индивидуальных вызовов, так и для вызовов конференц-связи.

Служба проверки подлинности аудио и видео связана с пограничной службой аудио- и видеоданных и предоставляет услуги проверки подлинности. Внешним пользователям, которые пытаются подключиться к пограничной службе аудио- и видеоданных, требуется маркер проверки подлинности, предоставляемый службой проверки подлинности аудио и видео, для прохождения вызовов.

</div>

<span> </span>

</div>

</div>

</div>

