---
title: 'Lync Server 2013: аудио-и видеограничные серверы (A/V)'
description: 'Lync Server 2013: аудио-и видеограничные серверы (A/V).'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Audio/Video (A/V) Edge Servers
ms:assetid: b0cc538b-77eb-47fb-be82-5ab0631c6219
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721852(v=OCS.15)
ms:contentKeyID: 49733785
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d5aefd4516540485b84ba0eb80f1a809d89eba0e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438241"
---
# <a name="audiovideo-av-edge-servers-in-lync-server-2013"></a>Пограничные серверы для аудио-и видеоустройств (A/V) в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-11-01_

Служба "A/V Edge" обеспечивает способ предоставления внутренних пользователей (пользователей, вошедших в вашу организационную сеть) для совместного использования звуковых и видеофайлов с внешними пользователями (пользователям, которые не вошли в свою организационную сеть). Помимо звуковых и видеофайлов, служба Edge/V также обеспечивает поддержку общего и обмена данными с рабочим столом.

Служба EDGE (A/V) главным образом управляется с помощью конфигурации Edge/V. Эти параметры позволяют управлять максимальной пропускной способностью, выделенной для каждого порта и пользователем, а также время, в течение которого маркер проверки подлинности может быть использован до того, как он должен быть обновлен. Параметры конфигурации EDGE можно применять к сайтам и отдельным пограничным серверам (/V). Когда вы определяете, какой набор параметров имеет приоритет, используйте следующее руководство:

  - Параметры, настроенные для области службы (то есть на отдельном сервере), имеют приоритет над всеми.

  - Параметры, настроенные в области сайта, имеют приоритет над параметрами, настроенными в глобальной области. Однако параметры области служб также будут заменять параметры области сайта.

  - Параметры в глобальной области будут использоваться только в том случае, если на отдельном сервере не настроены параметры службы и для сайта, на котором находится этот сервер, отсутствуют параметры сайта.

Служба EDGE (A/V) может управляться только с помощью Lync Server PowerShell и командлетов CsAVEdgeConfiguration.

<div>

## <a name="in-this-section"></a>Содержание

  - [Возврат сведений о конфигурации пограничного сервера в Lync Server 2013](lync-server-2013-return-a-v-edge-server-configuration-information.md)

  - [Создание и изменение коллекции параметров конфигурации пограничного сервера в Lync Server 2013](lync-server-2013-create-or-modify-a-collection-of-a-v-edge-server-configuration-settings.md)

  - [Удаление существующей коллекции параметров конфигурации пограничного сервера в Lync Server 2013](lync-server-2013-delete-an-existing-collection-of-a-v-edge-server-configuration-settings.md)

</div>

</div>

<span> </span>

</div>

</div>

</div>

