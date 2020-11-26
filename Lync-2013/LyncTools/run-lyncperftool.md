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
# <a name="run-lyncperftool"></a><span data-ttu-id="f697d-103">Запуск LyncPerfTool</span><span class="sxs-lookup"><span data-stu-id="f697d-103">Run LyncPerfTool</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f697d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f697d-104">

<span> </span></span></span>

<span data-ttu-id="f697d-105">_**Тема последнего изменения:** 2013-02-24_</span><span class="sxs-lookup"><span data-stu-id="f697d-105">_**Topic Last Modified:** 2013-02-24_</span></span>

<span data-ttu-id="f697d-106">Перед запуском средства нагрузки и производительности Lync Server 2013 (LyncPerfTool.exe) необходимо создать пользователей, контакты и сценарии.</span><span class="sxs-lookup"><span data-stu-id="f697d-106">Before running the Lync Server 2013 Stress and Performance Tool (LyncPerfTool.exe), you must create users, contacts, and scenarios.</span></span> <span data-ttu-id="f697d-107">Дополнительные сведения об использовании этих действий можно найти в статье [Создание пользователей и контактов](create-users-and-contacts.md) и [Настройка профиля пользователя](configure-user-profile.md).</span><span class="sxs-lookup"><span data-stu-id="f697d-107">For details about using the tools to perform these actions, see [Create Users and Contacts](create-users-and-contacts.md) and [Configure User Profile](configure-user-profile.md).</span></span> <span data-ttu-id="f697d-108">При запуске этих средств также создается файл, который будет работать LyncPerfTool.exe как часть пакетного файла, в котором будут включены необходимые параметры.</span><span class="sxs-lookup"><span data-stu-id="f697d-108">Running these tools will also generate a file that will run LyncPerfTool.exe as part of a batch file with the required parameters included.</span></span>

<div>

## <a name="running-the-lync-server-2013-stress-and-performance-tool"></a><span data-ttu-id="f697d-109">Работа с инструментом «нагрузочное тестирование и производительность» для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f697d-109">Running the Lync Server 2013 Stress and Performance Tool</span></span>

<span data-ttu-id="f697d-110">Средство UserProfileGenerator.exe создает пакетный файл, который позволяет запускать LyncPerfTool.exe путем регистрации счетчиков производительности LyncPerfTool и загрузки XML-файла конфигурации.</span><span class="sxs-lookup"><span data-stu-id="f697d-110">The UserProfileGenerator.exe tool creates a batch file that enables you to run LyncPerfTool.exe by registering the LyncPerfTool performance counters and loading the XML configuration file.</span></span> <span data-ttu-id="f697d-111">Пакетный файл запускает один экземпляр LyncPerfTool.exe для каждого файла конфигурации.</span><span class="sxs-lookup"><span data-stu-id="f697d-111">The batch file runs one instance of LyncPerfTool.exe per configuration file.</span></span> <span data-ttu-id="f697d-112">Чтобы запустить пакетный файл, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="f697d-112">To run the batch file, do the following:</span></span>

1.  <span data-ttu-id="f697d-113">Скопируйте папку, содержащую папки конфигурации и файлы, в каталог, содержащий LyncStressTool.exe на каждом клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="f697d-113">Copy the folder that contains the configuration folders and files to the directory that contains LyncStressTool.exe on each client computer.</span></span> <span data-ttu-id="f697d-114">(Например, если вы создали файлы конфигурации в папке с именем 1,28 \_ 13.16.16, скопируйте ее в папку, содержащую LyncPerfTool.exe на каждом клиенте.)</span><span class="sxs-lookup"><span data-stu-id="f697d-114">(For example, if you generated the configuration files in the folder named 1.28\_13.16.16, copy that folder to the folder that contains LyncPerfTool.exe on each client.)</span></span>

2.  <span data-ttu-id="f697d-115">Перейдите к соответствующей клиентской папке и запустите пакетный сценарий RunClient.</span><span class="sxs-lookup"><span data-stu-id="f697d-115">Navigate to the appropriately numbered client folder and run the RunClient batch script.</span></span> <span data-ttu-id="f697d-116">Вы можете дважды щелкнуть пакетный файл в проводнике, и он будет выполнять все файлы конфигурации для этого номера клиента.</span><span class="sxs-lookup"><span data-stu-id="f697d-116">You can simply double-click the batch file in Windows Explorer and it will run all of the configuration files for that client number.</span></span> <span data-ttu-id="f697d-117">Вы также можете запустить сценарий из соответствующей клиентской папки, используя следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="f697d-117">You can also run the script from the appropriate client folder by using the following syntax:</span></span>

    ```Batch
        RunClient0.bat "C:\Program Files\Microsoft Lync Server 2013\LyncStressAndPerfTool\LyncStress" 
    ```
<span data-ttu-id="f697d-118">Чтобы запустить LyncPerfTool.exe напрямую, откройте командную строку и введите в командной строке следующую команду (при первом выполнении этой команды обязательно Зарегистрируйте счетчики производительности regsvr32/i/n/s LyncPerfToolPerf.dll, как показано в заметке далее в этом разделе) :LyncPerfTool.exe/file:\<configXML\></span><span class="sxs-lookup"><span data-stu-id="f697d-118">To run LyncPerfTool.exe directly, open a command prompt, and then type the following command at the command line (when doing this for the first time, be sure to register the performance counters regsvr32 /i /n /s LyncPerfToolPerf.dll, as show in the note later in this topic):LyncPerfTool.exe /file:\<configXML\></span></span>
```Powershell
    LyncPerfTool.exe /file:IM_client0.xml
```
<span data-ttu-id="f697d-119">Чтобы средство отображало значения в файле конфигурации, включите параметр/displayfile в предыдущую команду, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="f697d-119">To have the tool display the values in the configuration file, include the /displayfile parameter on the preceding command, like this:</span></span>
```Powershell
    LyncPerfTool.exe /file:IM_client0.xml /displayfile
```
<span data-ttu-id="f697d-120">Чтобы завершить процесс, нажмите клавиши CTRL + C.</span><span class="sxs-lookup"><span data-stu-id="f697d-120">To end the process, press Ctrl+C.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="f697d-121">Перед запуском LyncPerfTool напрямую необходимо зарегистрировать счетчики производительности.</span><span class="sxs-lookup"><span data-stu-id="f697d-121">Before running LyncPerfTool directly, you must register the performance counters.</span></span> <span data-ttu-id="f697d-122">Чтобы зарегистрировать счетчики производительности, введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="f697d-122">Enter the following command to register performance counters:</span></span>



</div>

```Powershell
    regsvr32 /i /n /s LyncPerfToolPerf.dll
```
<div>


> [!NOTE]  
> <span data-ttu-id="f697d-123">Каждый экземпляр LyncPerfTool.exe, который вы запускаете, сразу же начнет входить в свою учетную запись, как правило, на частоте одного пользователя в секунду.</span><span class="sxs-lookup"><span data-stu-id="f697d-123">Every instance of LyncPerfTool.exe that you start will immediately start signing in users, usually at a rate of one user per second.</span></span> <span data-ttu-id="f697d-124">Пиковая частота входов пользователей для пула составляет около 12 в секунду.</span><span class="sxs-lookup"><span data-stu-id="f697d-124">The peak user sign-in rate for the pool is about 12 per second.</span></span> <span data-ttu-id="f697d-125">Это означает, что вы не должны запускать более 12 экземпляров LyncPerfTool, пока пользователи все еще работают.</span><span class="sxs-lookup"><span data-stu-id="f697d-125">This means that you should not start more than 12 LyncPerfTool instances at the same time, while the users are still signing in.</span></span> <span data-ttu-id="f697d-126">1000. для полного входа пользователей потребуется около 20 минут (за секунду).</span><span class="sxs-lookup"><span data-stu-id="f697d-126">1000 users will take about 20 minutes to fully sign in, at one per second.</span></span>



</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="f697d-127">См. также</span><span class="sxs-lookup"><span data-stu-id="f697d-127">See Also</span></span>


[<span data-ttu-id="f697d-128">Создание пользователей и контактов</span><span class="sxs-lookup"><span data-stu-id="f697d-128">Create Users and Contacts</span></span>](create-users-and-contacts.md)  
[<span data-ttu-id="f697d-129">Настройка профиля пользователя</span><span class="sxs-lookup"><span data-stu-id="f697d-129">Configure User Profile</span></span>](configure-user-profile.md)  
  

<span data-ttu-id="f697d-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f697d-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

