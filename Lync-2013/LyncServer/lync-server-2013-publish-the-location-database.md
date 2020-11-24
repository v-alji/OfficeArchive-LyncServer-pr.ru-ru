---
title: 'Lync Server 2013: публикация базы данных расположения'
description: 'Lync Server 2013: опубликуйте базу данных местоположений.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Publish the location database
ms:assetid: dd032b5b-df0e-4017-ac46-e17570c1ab1e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398974(v=OCS.15)
ms:contentKeyID: 48185598
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 26892429c7bf5fd9cbfebd0d7ac62482767a541e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399055"
---
# <a name="publish-the-location-database-from-lync-server-2013"></a>Публикация базы данных местоположений из Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-10-30_

Новые расположения, добавленные вами в базу данных местоположений, останутся недоступны клиенту, пока не будут опубликованы.

Подробности можно найти в документации по оболочке управления Lync Server для следующего командлета:

  - **Publish-CsLisConfiguration**

Если вы используете шлюзы ELIN, необходимо также загрузить номера ELIN в базу данных автоматического определения расположения (ALI) сети ТСОП. Оператор ТСОП может потребовать использования определенного формата для записей ELIN. Обратитесь к оператору ТСОП для получения более подробных сведений. Вы можете экспортировать записи из базы данных службы сведений о расположении и отформатировать их в соответствии с требованиями.

<div>

## <a name="to-publish-the-location-database"></a>Публикация базы данных местоположений

  - Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.

  - Чтобы опубликовать базу данных местоположений, выполните следующий командлет.
    
        Publish-CsLisConfiguration

</div>

</div>

<span> </span>

</div>

</div>

</div>

