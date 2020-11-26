---
title: 'Lync Server 2013: вопросы взаимодействия для видеоконференций'
description: 'Lync Server 2013: рекомендации по взаимодействию для видеоконференций.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Interoperability considerations for video conferencing
ms:assetid: 31ead3b5-ed95-42d4-96e2-7d9403d5c026
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204790(v=OCS.15)
ms:contentKeyID: 48183782
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 89675954ea4c4f188f50aab8fb2cb49494bcc247
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426790"
---
# <a name="interoperability-considerations-for-video-conferencing-in-lync-server-2013"></a>Рекомендации по взаимодействию при видеоконференциях в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-10-02_

В этом разделе описывается взаимодействие пользователей на этапе сосуществования миграции при взаимодействии между устаревшими клиентами и клиентами пула Lync Server 2013 или Lync Server 2013 и устаревшим пулом.

<div>

## <a name="lync-server-2013-pools"></a>Пулы Lync Server 2013

При использовании устаревшего клиента в пуле Lync Server 2013 пользователи могут столкнуться с приведенным ниже поведением.

  - При использовании двух абонентов разрешение экрана такое же, как и в устаревшем пуле.

  - Для многокомпонентных конференций разрешения на использование видео и видеоконференции одинаковы, как и в устаревшем пуле. Представление коллекции и высокое разрешение не поддерживаются.

</div>

<div>

## <a name="legacy-pools"></a>Устаревшие пулы

Если клиент Lync Server 2013 используется в устаревшем пуле, пользователи сталкиваются с описанным ниже поведением.

  - При использовании двух сторон Пользователи Lync Server 2013 могут использовать новые функции, как описано ниже.
    
      - Функция H. 264 доступна, если оба участника используют клиенты Lync Server 2013.
    
      - Клиент Lync Server 2013 использует значение по умолчанию для TotalReceiveVideoBitRateKb, так как старый сервер не отправляет эту информацию с помощью встроенного в стандартную подготовку.

  - Для многокомпонентных конференций разрешения на видео и видеоконференции — это то же, что и у устаревшего клиента в пуле устаревших элементов.

<div>


> [!NOTE]  
> Если на устаревшом сервере размещается клиент Lync Server 2013, можно настроить пропускную способность видеоконференций, чтобы все пользователи в пуле получали видео с низким разрешением, но отправлять видео с высоким разрешением. Например, если для MaxVideoRateAllowed задано значение CIF-250K в конфигурации мультимедиа, а VideoBitRateKb установлено значение 2000 кбит/с в политике конференц-связи. В этой ситуации это может привести к невозможности высокого разрешения для пользователей в пуле.<BR>Так как MaxVideoRateAllowed больше не используется для клиентов Lync Server 2013, он не может запретить клиентам Lync Server 2013 запрашивать видео с высоким разрешением. Вместо этого настройте VideoBitRateKb в политике конференц-связи для всех пользователей в пуле на то же значение, что и MaxVideoRateAllowed (то есть CIF имеет значение 250 кбит/с, или режим VGA — 600 кбит/с, а для параметра High — 1500 кбит/с).



</div>

</div>

</div>

<span> </span>

</div>

</div>

</div>

