---
title: 'Lync Server 2013: настройка автоматического входа клиента для использования директора'
description: 'Lync Server 2013: Настройка автоматических клиентских Sign-In для использования режиссера.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure Automatic Client Sign-In to use the Director
ms:assetid: 85369ffc-53ae-43be-8a23-84a094faecff
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398678(v=OCS.15)
ms:contentKeyID: 48184703
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b9c45a1a677d3a30704d8dca1771ef865cef29ec
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399619"
---
# <a name="configure-automatic-client-sign-in-to-use-the-director-in-lync-server-2013"></a>Настройка автоматического входа клиента для использования директора в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-09-08_

При развертывании Lync Server 2013, Director или пула директоров рекомендуется использовать функцию автоматического клиентского Sign-In. Дополнительные сведения о том, как настроить DNS-серверы для автоматического входа в клиент, приведены в разделе [требования к DNS для автоматического входа в службу в Lync Server 2013](lync-server-2013-dns-requirements-for-automatic-client-sign-in.md) в документации по планированию.

Если вы уже развернули функцию автоматического входа в систему, ознакомьтесь со следующими разделами, чтобы настроить ее для вашего режиссера (-ов).

<div>

## <a name="single-director-instance"></a>Один экземпляр режиссера

Если вы уже развернули клиентские Sign-In с автоматическим подключением и указываете на сервер переднего плана или пул переднего плана, вам нужно изменить DNS-запись SRV, чтобы она указывала на режиссер.

</div>

<div>

## <a name="director-pool"></a>Пул режиссеров

Если вы уже развернули автоматически клиентские Sign-In и указываете на сервер переднего плана или пул переднего плана, вам нужно изменить DNS-запись SRV, чтобы она указывала на этот пул.

</div>

</div>

<span> </span>

</div>

</div>

</div>

