---
title: Масштабируемый пул директоров — балансировка нагрузки на DNS и аппаратный балансировщик нагрузки
description: Масштабируемый пул режиссеров — балансировка нагрузки DNS и балансировщик нагрузки оборудования.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Scaled Director pool - DNS load balancing and hardware load balancer
ms:assetid: a1f6ffc0-9e6e-4217-a923-025c9679e154
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205142(v=OCS.15)
ms:contentKeyID: 48185023
ms.date: 03/29/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b30dfcc3515420ffb34343e4653e9518b1b9c3ed
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442060"
---
# <a name="scaled-director-pool---dns-load-balancing-and-hardware-load-balancer-in-lync-server-2013"></a>Масштабируемый пул директоров — балансировка нагрузки на DNS и аппаратный балансировщик нагрузки в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-10-22_

Масштабируемый пул режиссеров, на котором развернуты более одного режиссера для обработки дополнительной емкости и обеспечения высокой доступности, требуется балансировка нагрузки для распространения взаимодействия между клиентом и сервером со всеми участниками пула. В режиссере веб-службы размещаются очень похоже на внешний интерфейс пула. Для обеспечения балансировки нагрузки вы можете использовать аппаратную балансировку нагрузки или балансировку нагрузки DNS и аппаратную балансировку нагрузки. Для веб-служб требуется балансировка нагрузки на оборудовании, а для балансировки нагрузки DNS — только возможности, необходимые для веб-служб.

В следующих разделах описаны вопросы планирования для развертывания пула с помощью балансировки нагрузки DNS в сочетании с аппаратным обеспечением балансировки нагрузки. Если вы планируете использовать аппаратную балансировку нагрузки, но не балансировку нагрузки DNS для группового пула, ознакомьтесь с разделом [масштабированный пул пулов — подсистема подсистемы балансировки нагрузки оборудования в Lync Server 2013, в](lync-server-2013-scaled-director-pool-hardware-load-balancer.md) которой описаны требования к планированию для этой топологии.

![Масштабируемый пул режиссеров](images/JJ205142.35a78a7a-b781-4c8f-951e-168451ba6a65(OCS.15).jpg "Масштабируемый пул режиссеров")

<div>

## <a name="in-this-section"></a>Содержание

  - [Сводка по сертификатам — балансировка нагрузки на DNS и аппаратная балансировка нагрузки в Lync Server 2013](lync-server-2013-certificate-summary-dns-and-hlb-load-balanced.md)

  - [Сводка по портам — балансировка нагрузки на DNS и аппаратная балансировка нагрузки в Lync Server 2013](lync-server-2013-port-summary-dns-and-hlb-load-balanced.md)

  - [Сводка по DNS — балансировка нагрузки на DNS и аппаратная балансировка нагрузки в Lync Server 2013](lync-server-2013-dns-summary-dns-and-hlb-load-balanced.md)

</div>

</div>

<span> </span>

</div>

</div>

</div>

