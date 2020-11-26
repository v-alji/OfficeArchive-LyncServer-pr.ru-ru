---
title: Импорт политик и параметров
description: Импорт политик и параметров.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Import policies and settings
ms:assetid: b25decee-2ee5-4836-b370-454411d39252
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205178(v=OCS.15)
ms:contentKeyID: 48185147
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e014b7e8f0498742104118eec9eb313394ae6a94
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439606"
---
# <a name="import-policies-and-settings"></a>Импорт политик и параметров

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-09-28_

После того как вы объедините информацию о топологии Office Communications Server 2007 R2 с помощью административного пула Lync Server 2013, вам необходимо запустить командлет командной консоли Lync Server 2013, чтобы перенести политики и параметры конфигурации Office Communications Server 2007 R2 в пул Lync Server 2013 для пилотного пула.

Командлет **Import-CsLegacyConfiguration** импортирует политики, маршруты голосовой связи, абонентские группы, URL-адреса Communicator Web Access и номера доступа для телефонного подключения в Lync Server 2013.

<div>

## <a name="to-migrate-policies-and-settings"></a>Миграция политик и параметров

1.  На сервере переднего плана Lync Server 2013 запустите командную консоль Lync Server Management Shell.

2.  В командной строке введите следующую команду:
    
        Import-CsLegacyConfiguration
    
    После импорта политик воспользуйтесь приведенными ниже инструкциями, чтобы просмотреть импортированные политики на панели управления Lync Server.

</div>

<div>

## <a name="to-view-imported-policies"></a>Просмотр импортированных политик

1.  Откройте панель управления Lync Server 2013.

2.  Нажмите кнопку **Маршрутизация голоса** и просмотрите импортированные политики.

3.  Выберите **Конференц** -связь и просмотрите импортированные политики.

4.  Выберите пункт **Федерация и внешний доступ** и просмотрите импортированные политики.

5.  Нажмите кнопку **мониторинг и архивация** и просмотрите импортированные политики.

</div>

</div>

<span> </span>

</div>

</div>

</div>

