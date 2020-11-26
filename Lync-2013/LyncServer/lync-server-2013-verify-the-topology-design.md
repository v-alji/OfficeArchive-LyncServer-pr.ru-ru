---
title: 'Lync Server 2013: проверка структуры топологии'
description: 'Lync Server 2013: Проверьте структуру топологии.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Verify the topology design
ms:assetid: c1b61814-239e-4101-aab0-de3db1d8793c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412951(v=OCS.15)
ms:contentKeyID: 48185311
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: cb1e65343aacddbc11d3b909dfdff715503cab93
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438913"
---
# <a name="verify-the-topology-design-in-lync-server-2013"></a>Проверка структуры топологии в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-01-02_

Построитель топологии автоматически проверяет топологию. Любая ошибка топологии определяется как ошибка проверки, указанная значком ошибки проверки рядом с ролью сервера. Важно также убедиться, что топология правильно представляет топологию для развертывания.

<div>

## <a name="to-verify-the-topology-prior-to-publication"></a>Проверка топологии перед публикацией

1.  Проверьте, что все простые URL-адреса настроены правильно.

2.  Проверьте, что сервер на основе SQL Server включен и доступен компьютеру, на котором установлен построитель топологий, включая все необходимые правила брандмауэра.

3.  Убедитесь в том, что общий доступ к файлам доступен, и у него есть соответствующие разрешения.

4.  Проверьте, что в топологии заданы правильные роли сервера, удовлетворяющие требованиям развертывания.

5.  Убедитесь в том, что серверы находятся в доменных службах Active Directory. Это происходит автоматически, если вы присоединили серверы к домену.

Когда топология проверена и ошибки проверки отсутствуют, все должно быть готово к публикации топологии. Если обнаружены ошибки проверки, необходимо исправить эти значения, прежде чем можно будет опубликовать топологию. Подробнее о публикации топологии можно найти в разделе [Публикация топологии в Lync Server 2013](lync-server-2013-publish-the-topology.md).

</div>

</div>

<span> </span>

</div>

</div>

</div>

