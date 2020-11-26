---
title: Подготовка топологии для загрузки
description: Выполняется подготовка топологии для загрузки.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Provisioning the Topology to Run Load
ms:assetid: 6fba03df-3914-4d2a-8208-e252ad993aff
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945598(v=OCS.15)
ms:contentKeyID: 51541424
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: da482fde949675acc1722305433b95b7a6a6b523
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446425"
---
# <a name="provisioning-the-topology-to-run-load"></a>Подготовка топологии для загрузки

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2013-02-04_

<div>

В зависимости от существующих настроек и конфигурации Lync Server 2013, возможно, потребуется внести в среду следующие изменения:

1.  Установите для политики выполнения Windows PowerShell неограниченный доступ. Чтобы проверить параметры политики выполнения, откройте командную консоль Lync Server Management Shell и выполните следующую команду:

    ``` powershell
        Get-ExecutionPolicy
    ```        

    Если эта команда не возвращает значение Unrestricted, выполните следующую команду:

    ``` powershell
        Set-ExecutionPolicy -Unrestricted
    ```

2.  Чтобы эффективно настроить Lync Server 2013, необходимо выполнить следующие действия.
    
      - Знакомство с топологией Lync Server 2013 (например, именами компьютеров, экземплярами служб, именами сайтов и политиками).
    
      - Назначьте пользователей, которые были созданы для групп, например группы слежения группы ответа (например, URI SIP).

3.  Чтобы запустить сценарий из командной строки, можно использовать:

    ``` powershell
        Powershell.exe -file <path to the file>
    ```
    
4.  Как правило, после выполнения одного из сценариев в этом пакете результаты трассировки из сценария будут храниться в файле, расположенном в том же пути, из которого был вызван сценарий, с именем \<scriptname\> $h $ m $s.txt. Например, выполнение ArchivingPolicy.ps1 в 12:15 P.M. создаст файл журнала, например ArchivingPolicy121500.txt.

5.  Наконец, обратите внимание на то, что, несмотря на то, что мы предоставили примеры для настройки сервера, вы несете ответственность за изменение или удаление конфигурации после завершения загрузки.

</div>

</div>

<span> </span>

</div>

</div>

</div>

