---
title: 'Lync Server 2013: настройка сертификатов для обратного прокси-сервера'
description: 'Lync Server 2013: Настройка сертификатов для обратного прокси-сервера.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Set up certificates for the reverse proxy
ms:assetid: c03a08ec-a67b-4f11-b0d7-6677461beaaa
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412938(v=OCS.15)
ms:contentKeyID: 48185291
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f4b84241775bb3594840b68551048c01ff5faba2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441748"
---
# <a name="set-up-certificates-for-the-reverse-proxy-in-lync-server-2013"></a>Настройка сертификатов для обратного прокси-сервера в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-09-08_

Каждый обратный прокси-сервер требует наличия сертификата веб-сервера для использования службой прослушивания. Сертификат веб-сервера должен быть выдан общедоступным центром сертификации (ЦС).

Подробнее об этих и других требованиях к сертификатам можно узнать в статьях [требования к сертификатам для доступа внешних пользователей в Lync Server 2013](lync-server-2013-certificate-requirements-for-external-user-access.md).

<div>

## <a name="to-set-up-a-web-services-certificate-for-the-reverse-proxy"></a>Настройка сертификата веб-службы для обратного прокси

  - Вы должны уже настроить обратный прокси-сервер, в том числе настроить сертификат веб-служб. Если вы не сделали этого, прежде чем приступать к развертыванию пограничных серверов, выполните действия, описанные в разделе [Настройка обратного прокси-сервера для Lync Server 2013](lync-server-2013-setting-up-reverse-proxy-servers.md) для создания запроса и установки сертификата веб-служб, а затем создайте каждое правило веб-публикации и настройте его для использования сертификата.

</div>

</div>

<span> </span>

</div>

</div>

</div>

