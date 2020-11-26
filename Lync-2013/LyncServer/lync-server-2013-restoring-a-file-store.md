---
title: 'Lync Server 2013: восстановление хранилища файлов'
description: 'Lync Server 2013: восстановление хранилища файлов.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Restoring a file store
ms:assetid: 89916fc6-31d3-4c7f-9eaf-c02584761ef4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202180(v=OCS.15)
ms:contentKeyID: 51541491
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 201c4b20f224fa3a25e931689e564410c60143e6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436253"
---
# <a name="restoring-a-file-store-in-lync-server-2013"></a>Восстановление хранилища файлов в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2013-02-18_

Хранилища файлов для выпуска Standard Edition обычно находятся на сервере Standard Edition. Хранилища файлов Enterprise Edition обычно находятся на файловом сервере или кластере. Ниже описана процедура восстановления хранилища файлов.

<div>

## <a name="to-restore-a-file-store"></a>Восстановление хранилища файлов

1.  Если хранилище файлов не удается, скопируйте соответствующее хранилище файлов из $Backup \\ в хранилище файлов на файловом сервере или стандартном сервере выпуске, а затем предоставьте к ней общий доступ.
    
    <div>
    

    > [!IMPORTANT]  
    > Путь и имя файла для восстановленного хранилища файлов должны совпадать с заархивированным хранилищем файлов, чтобы компоненты, использующие эти файлы, могли получать к ним доступ.

    
    </div>

2.  При необходимости задайте списки управления доступом (ACL) для хранилища файлов. В командной строке выполните следующую команду:
    
        Enable-CsTopology
    
    <div>
    

    > [!NOTE]  
    > Этот шаг необходимо выполнить только в том случае, если в процессе восстановления не выполнялась построитель топологии.

    
    </div>

</div>

</div>

<span> </span>

</div>

</div>

</div>

