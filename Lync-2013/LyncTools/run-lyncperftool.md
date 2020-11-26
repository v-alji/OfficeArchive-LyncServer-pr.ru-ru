---
title: Запуск LyncPerfTool
description: Запустите LyncPerfTool.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Run LyncPerfTool
ms:assetid: f2fd1940-d744-47b5-b299-04a914039182
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945612(v=OCS.15)
ms:contentKeyID: 51541437
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3278754c9154f47602c5c4f1fa95cdc4b465b228
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446408"
---
# <a name="run-lyncperftool"></a>Запуск LyncPerfTool

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2013-02-24_

Перед запуском средства нагрузки и производительности Lync Server 2013 (LyncPerfTool.exe) необходимо создать пользователей, контакты и сценарии. Дополнительные сведения об использовании этих действий можно найти в статье [Создание пользователей и контактов](create-users-and-contacts.md) и [Настройка профиля пользователя](configure-user-profile.md). При запуске этих средств также создается файл, который будет работать LyncPerfTool.exe как часть пакетного файла, в котором будут включены необходимые параметры.

<div>

## <a name="running-the-lync-server-2013-stress-and-performance-tool"></a>Работа с инструментом «нагрузочное тестирование и производительность» для Lync Server 2013

Средство UserProfileGenerator.exe создает пакетный файл, который позволяет запускать LyncPerfTool.exe путем регистрации счетчиков производительности LyncPerfTool и загрузки XML-файла конфигурации. Пакетный файл запускает один экземпляр LyncPerfTool.exe для каждого файла конфигурации. Чтобы запустить пакетный файл, выполните указанные ниже действия.

1.  Скопируйте папку, содержащую папки конфигурации и файлы, в каталог, содержащий LyncStressTool.exe на каждом клиентском компьютере. (Например, если вы создали файлы конфигурации в папке с именем 1,28 \_ 13.16.16, скопируйте ее в папку, содержащую LyncPerfTool.exe на каждом клиенте.)

2.  Перейдите к соответствующей клиентской папке и запустите пакетный сценарий RunClient. Вы можете дважды щелкнуть пакетный файл в проводнике, и он будет выполнять все файлы конфигурации для этого номера клиента. Вы также можете запустить сценарий из соответствующей клиентской папки, используя следующий синтаксис:

    ```Batch
        RunClient0.bat "C:\Program Files\Microsoft Lync Server 2013\LyncStressAndPerfTool\LyncStress" 
    ```
Чтобы запустить LyncPerfTool.exe напрямую, откройте командную строку и введите в командной строке следующую команду (при первом выполнении этой команды обязательно Зарегистрируйте счетчики производительности regsvr32/i/n/s LyncPerfToolPerf.dll, как показано в заметке далее в этом разделе) :LyncPerfTool.exe/file:\<configXML\>
```Powershell
    LyncPerfTool.exe /file:IM_client0.xml
```
Чтобы средство отображало значения в файле конфигурации, включите параметр/displayfile в предыдущую команду, как показано ниже.
```Powershell
    LyncPerfTool.exe /file:IM_client0.xml /displayfile
```
Чтобы завершить процесс, нажмите клавиши CTRL + C.

<div>


> [!NOTE]  
> Перед запуском LyncPerfTool напрямую необходимо зарегистрировать счетчики производительности. Чтобы зарегистрировать счетчики производительности, введите следующую команду:



</div>

```Powershell
    regsvr32 /i /n /s LyncPerfToolPerf.dll
```
<div>


> [!NOTE]  
> Каждый экземпляр LyncPerfTool.exe, который вы запускаете, сразу же начнет входить в свою учетную запись, как правило, на частоте одного пользователя в секунду. Пиковая частота входов пользователей для пула составляет около 12 в секунду. Это означает, что вы не должны запускать более 12 экземпляров LyncPerfTool, пока пользователи все еще работают. 1000. для полного входа пользователей потребуется около 20 минут (за секунду).



</div>

</div>

<div>

## <a name="see-also"></a>См. также


[Создание пользователей и контактов](create-users-and-contacts.md)  
[Настройка профиля пользователя](configure-user-profile.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

