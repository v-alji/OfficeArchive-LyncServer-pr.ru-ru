---
title: 'Lync Server 2013: связывание подсетей с сетевыми сайтами для обхода мультимедиа'
description: 'Lync Server 2013: сопоставьте подсети с сетевыми сайтами для обхода мультимедиа.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Associate subnets with network sites for media bypass
ms:assetid: 5bc632b7-1446-470f-b332-48ea0ca4d1fd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398401(v=OCS.15)
ms:contentKeyID: 48184244
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ee03b51d29a88ff634cb87385c5889c35acd8884
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399955"
---
# <a name="associate-subnets-with-network-sites-for-media-bypass-in-lync-server-2013"></a>Связывание подсетей с сетевыми сайтами для обхода мультимедиа в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-09-12_

<div>


> [!NOTE]  
> В этой статье предполагается, что вы настроили обход глобальных параметров в мультимедиа и что вы настроили сетевой регион и сетевые сайты для обхода мультимедиа.



</div>

Каждая подсеть в сети должна быть связана с определенным сетевым сайтом. Это связано с тем, что сведения о подсети используются для определения сетевого сайта, на котором находится конечная точка. Если в сеансе известны расположение обеих сторон сеанса, обход мультимедиа может определять, куда отправлять мультимедиа для обработки.

В пропуске мультимедиа отсутствуют особые требования для сопоставления подсетей с сетевыми сайтами. Чтобы создать связь между подсетями и сетевыми сайтами в вашей топологии, выполните действия, описанные в разделе [связывание подсети с сетевым сайтом в Lync Server 2013](lync-server-2013-associate-a-subnet-with-a-network-site.md).

<div>

## <a name="next-steps-create-bandwidth-policy-profiles"></a>Дальнейшие действия: создание профилей политики пропускной способности

После связывания подсетей с сетевыми сайтами для обхода мультимедиа необходимо создать один или несколько профилей политики пропускной способности, которые будут разбивать подсети на разделы с хорошим подключением и без них, в целях обхода мультимедиа. Все подсети в сетевом регионе с сетевыми сайтами, не имеющими ограничений пропускной способности, имеют хорошее соединение и, следовательно, такие подсети могут использовать обход мультимедиа.

Инструкции по настройке профилей политики пропускной способности описаны [в разделе Создание профилей политики пропускной способности в Lync Server 2013](lync-server-2013-create-bandwidth-policy-profiles.md).

</div>

</div>

<span> </span>

</div>

</div>

</div>

