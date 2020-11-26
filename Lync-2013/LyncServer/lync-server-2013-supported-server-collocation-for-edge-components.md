---
title: 'Lync Server 2013: поддерживаемое выровненное размещение серверов для пограничных компонентов'
description: 'Lync Server 2013: Поддерживаемые расвыровнения серверов для компонентов Edge.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Supported server collocation for edge components
ms:assetid: 435c4dd8-36af-4b71-9b88-3ffcf0fc5c65
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425934(v=OCS.15)
ms:contentKeyID: 48183978
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7bf253e5210e077ca62b3d00f7f130d54d8392a5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423640"
---
# <a name="supported-server-collocation-for-edge-components-in-lync-server-2013"></a>Поддерживаемое выровненное размещение серверов для пограничных компонентов в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-09-08_

Служба пограничного доступа, служба Edge для веб-конференций, служба EDGE и служба XMPP proxy размещаются на пограничных серверах. Следующие серверы предоставляют функции, необходимые для доступа внешних пользователей, и должны развертываться как выделенные серверы:

  - Пограничный сервер

  - Режиссер (необязательно)

  - Сертификат обратного прокси-сервера

<div>


> [!IMPORTANT]  
> Обратный прокси-сервер не требуется специально для обслуживания только сервера Lync Server 2013. Например, вы можете предоставить услуги для публикации веб-служб Lync Server и одновременно предоставить опубликованный веб-сайт для другого веб-сайта, на котором не установлено Lync Server. Если у вас уже есть обратный прокси-сервер в демилитаризованной зоне для поддержки других служб, вы можете использовать его для Lync Server 2013.



</div>

</div>

<span> </span>

</div>

</div>

</div>

