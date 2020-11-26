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
# <a name="provisioning-the-topology-to-run-load"></a><span data-ttu-id="6627b-103">Подготовка топологии для загрузки</span><span class="sxs-lookup"><span data-stu-id="6627b-103">Provisioning the Topology to Run Load</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6627b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6627b-104">

<span> </span></span></span>

<span data-ttu-id="6627b-105">_**Тема последнего изменения:** 2013-02-04_</span><span class="sxs-lookup"><span data-stu-id="6627b-105">_**Topic Last Modified:** 2013-02-04_</span></span>

<div>

<span data-ttu-id="6627b-106">В зависимости от существующих настроек и конфигурации Lync Server 2013, возможно, потребуется внести в среду следующие изменения:</span><span class="sxs-lookup"><span data-stu-id="6627b-106">Depending on your existing settings and configuration of Lync Server 2013, you may need to make the following changes in your environment:</span></span>

1.  <span data-ttu-id="6627b-107">Установите для политики выполнения Windows PowerShell неограниченный доступ.</span><span class="sxs-lookup"><span data-stu-id="6627b-107">Set the Windows PowerShell execution policy to Unrestricted.</span></span> <span data-ttu-id="6627b-108">Чтобы проверить параметры политики выполнения, откройте командную консоль Lync Server Management Shell и выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="6627b-108">To check your execution policy settings, open the Lync Server Management Shell and run the following command:</span></span>

    ``` powershell
        Get-ExecutionPolicy
    ```        

    <span data-ttu-id="6627b-109">Если эта команда не возвращает значение Unrestricted, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="6627b-109">If this command does not return the value Unrestricted, run this command:</span></span>

    ``` powershell
        Set-ExecutionPolicy -Unrestricted
    ```

2.  <span data-ttu-id="6627b-110">Чтобы эффективно настроить Lync Server 2013, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="6627b-110">To effectively configure Lync Server 2013, you will need to:</span></span>
    
      - <span data-ttu-id="6627b-111">Знакомство с топологией Lync Server 2013 (например, именами компьютеров, экземплярами служб, именами сайтов и политиками).</span><span class="sxs-lookup"><span data-stu-id="6627b-111">Be familiar with Lync Server 2013 topology (for example, computer names, service instances, site names, and policies).</span></span>
    
      - <span data-ttu-id="6627b-112">Назначьте пользователей, которые были созданы для групп, например группы слежения группы ответа (например, URI SIP).</span><span class="sxs-lookup"><span data-stu-id="6627b-112">Assign some of the users that were created to groups, such as Response Group hunt groups (for example, SIP URIs).</span></span>

3.  <span data-ttu-id="6627b-113">Чтобы запустить сценарий из командной строки, можно использовать:</span><span class="sxs-lookup"><span data-stu-id="6627b-113">To run the script from the command line, you may use:</span></span>

    ``` powershell
        Powershell.exe -file <path to the file>
    ```
    
4.  <span data-ttu-id="6627b-114">Как правило, после выполнения одного из сценариев в этом пакете результаты трассировки из сценария будут храниться в файле, расположенном в том же пути, из которого был вызван сценарий, с именем \<scriptname\> $h $ m $s.txt.</span><span class="sxs-lookup"><span data-stu-id="6627b-114">Typically, after one of the scripts in this package runs, the resulting traces from the script will be stored in a file in the same path from which the script was invoked, named \<scriptname\>$h$m$s.txt.</span></span> <span data-ttu-id="6627b-115">Например, выполнение ArchivingPolicy.ps1 в 12:15 P.M.</span><span class="sxs-lookup"><span data-stu-id="6627b-115">For example, running ArchivingPolicy.ps1 at 12:15 P.M.</span></span> <span data-ttu-id="6627b-116">создаст файл журнала, например ArchivingPolicy121500.txt.</span><span class="sxs-lookup"><span data-stu-id="6627b-116">will generate a log file such as ArchivingPolicy121500.txt.</span></span>

5.  <span data-ttu-id="6627b-117">Наконец, обратите внимание на то, что, несмотря на то, что мы предоставили примеры для настройки сервера, вы несете ответственность за изменение или удаление конфигурации после завершения загрузки.</span><span class="sxs-lookup"><span data-stu-id="6627b-117">Finally, note that although we have provided examples to configure the server, you are responsible for modifying or deleting the configuration after you have finished running the load.</span></span>

<span data-ttu-id="6627b-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6627b-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

