---
title: 'Lync Server 2013: Проверка связи с клиентом Lync Online'
description: 'Lync Server 2013: Проверка связи с клиентом Lync Online.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Verify communications with a Lync Online customer
ms:assetid: c8287b15-e1bb-4b26-8354-0ec90b2fcfe7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202189(v=OCS.15)
ms:contentKeyID: 48185378
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 867b0f7ffffd563c869b9bcd5443a3cb91b156af
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399802"
---
# <a name="verify-communications-with-a-lync-online-customer-in-lync-server-2013"></a>Проверка связи с клиентом Lync Online в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-10-08_

Чтобы разрешить пользователям Lync в организации взаимодействовать с пользователями Microsoft Lync Online 2010, необходимо выполнить следующие действия.

  - Выполнены все необходимые условия. Сюда входит развертывание внутренних и пограничных серверов, включение поддержки федерации для Организации и Настройка учетных записей пользователей. Дополнительные сведения можно найти [в разделе Предварительные требования для Федерации с клиентом Lync Online в Lync Server 2013](lync-server-2013-prerequisites-for-federating-with-a-lync-online-customer.md).

  - Настройка поддержки доступа к доменам во внутренней среде. Сюда входит создание записи поставщика узла и Настройка развертывания для разрешения доступа из домена клиента Lync Online. Подробности можно найти [в разделе Настройка поддержки федерации для домена Lync Online в Lync Server 2013](lync-server-2013-configure-federation-support-for-a-lync-online-domain.md).

  - Настройка учетных записей пользователей для поддержки Федерации. Подробности можно найти [в разделе Настройка доступа пользователей к интеграции с клиентом Lync Online в Lync Server 2013](lync-server-2013-configure-user-access-for-federation-with-a-lync-online-customer.md).

После выполнения всех этих действий и администратором пользователя Lync Online 2010 завершается вся настройка интернет-служб для поддержки Федерации с вашей организацией, проверка связи путем проверки связи между внутренним пользователем в Организации и пользователем клиента Lync Online. Если связь не была успешной, для устранения проблемы используйте средство ведения журналов из пограничного сервера для захвата файлов журнала и трассировки. Подробнее об использовании средства ведения журнала можно найти в разделе [Открытие средства администрирования Lync Server 2013](lync-server-2013-open-lync-server-administrative-tools.md) в документации по эксплуатации. Подробные сведения о средстве ведения журнала можно найти в документации по средству ведения журнала Lync Server 2010 в библиотеке TechNet по адресу [https://go.microsoft.com/fwlink/p/?linkId=199265](https://go.microsoft.com/fwlink/p/?linkid=199265) .

</div>

<span> </span>

</div>

</div>

</div>

