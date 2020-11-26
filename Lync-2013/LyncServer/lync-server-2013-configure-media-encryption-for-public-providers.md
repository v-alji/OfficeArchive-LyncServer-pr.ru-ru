---
title: 'Lync Server 2013: настройка шифрования мультимедиа для общедоступных поставщиков'
description: 'Lync Server 2013: Настройка шифрования мультимедиа для общедоступных поставщиков.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure media encryption for public providers
ms:assetid: a95814cf-c5a9-4652-8ffc-c469a2653153
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205149(v=OCS.15)
ms:contentKeyID: 48185036
ms.date: 12/13/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 177c19f151b67d741c7e26506f7ebc98b3ce831a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433887"
---
# <a name="configure-media-encryption-for-public-providers-in-lync-server-2013"></a>Настройка шифрования мультимедиа для общедоступных поставщиков в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2014-12-12_

Если вы реализуете Федерацию аудио-и видеосвязи (A/V) с Windows Live Messenger, необходимо изменить два параметра: уровень шифрования Lync Server и политика EnablePublicCloudAccess. По умолчанию задано значение "обязательный уровень шифрования". Этот параметр необходимо изменить на "поддерживается". Если для политики EnablePublicCloudAccess задано значение false, необходимо установить **значение true**. Это можно сделать в командной консоли Lync Server Management Shell.

<div>

## <a name="configure-federation-for-windows-live"></a>Настройка Федерации для Windows Live

1.  Запустите командную консоль Lync Server на сервере переднего плана: нажмите кнопку **Пуск**, выберите пункт **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.

2.  В командной строке введите следующие команды:
    
       ```powershell
        Set-CsMediaConfiguration -EncryptionLevel SupportEncryption
       ```
    
       ```powershell
        Set-CsExternalAccessPolicy Global -EnablePublicCloudAccess $true -EnablePublicCloudAudioVideoAccess $true
       ```
    
    <div class=" ">
    

    > [!NOTE]  
    > Это действие является обязательным, так как в Windows Live Messenger не поддерживается шифрование аудио-и видеофайлов. В команде для глобальной политики задано значение параметра шифрование поддержки, а не необходимость шифрования аудио-и видеоданных. Клиенты, которые поддерживают шифрование, по-прежнему будут использовать шифрование, например Lync 2013.

    
    </div>

</div>

</div>

<span> </span>

</div>

</div>

</div>

