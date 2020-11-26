---
title: 'Lync Server 2013: Проверка разрешений на активацию служб и групп'
description: 'Lync Server 2013: Проверка разрешений на активацию служб и групп.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing service activation and group permissions
ms:assetid: 2c59e603-ba85-40ba-91a7-51c6fd39472e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn743833(v=OCS.15)
ms:contentKeyID: 63969594
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 116cf939f3110616ce395eb14c7945890bdb89b7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440985"
---
# <a name="testing-service-activation-and-group-permissions-in-lync-server-2013"></a><span data-ttu-id="5b2f7-103">Проверка разрешений на активацию служб и групп в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5b2f7-103">Testing service activation and group permissions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5b2f7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5b2f7-104">

<span> </span></span></span>

<span data-ttu-id="5b2f7-105">_**Тема последнего изменения:** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="5b2f7-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5b2f7-106">Расписание проверки</span><span class="sxs-lookup"><span data-stu-id="5b2f7-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="5b2f7-107">Ежедневно</span><span class="sxs-lookup"><span data-stu-id="5b2f7-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5b2f7-108">Средство тестирования</span><span class="sxs-lookup"><span data-stu-id="5b2f7-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="5b2f7-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="5b2f7-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5b2f7-110">Требуемые разрешения</span><span class="sxs-lookup"><span data-stu-id="5b2f7-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="5b2f7-111">При локальном запуске с помощью командной консоли Lync Server пользователи должны быть членами группы безопасности RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="5b2f7-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="5b2f7-112">При запуске с помощью удаленного экземпляра Windows PowerShell пользователям должна быть назначена роль RBAC, имеющая разрешение на запуск командлета Test-CsTopology.</span><span class="sxs-lookup"><span data-stu-id="5b2f7-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsTopology cmdlet.</span></span> <span data-ttu-id="5b2f7-113">Чтобы просмотреть список всех ролей RBAC, которые могут использовать этот командлет, выполните в командной строке Windows PowerShell следующую команду:</span><span class="sxs-lookup"><span data-stu-id="5b2f7-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsTopology&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="5b2f7-114">Описание</span><span class="sxs-lookup"><span data-stu-id="5b2f7-114">Description</span></span>

<span data-ttu-id="5b2f7-115">Командлет Test-CsTopology позволяет проверить, правильно ли работает Lync Server 2013 в глобальной области.</span><span class="sxs-lookup"><span data-stu-id="5b2f7-115">The Test-CsTopology cmdlet enables you to verify that Lync Server 2013 is functioning correctly at a global scope.</span></span> <span data-ttu-id="5b2f7-116">По умолчанию командлет проверяет всю инфраструктуру Lync Server, убедившись в том, что необходимые службы запущены и установлены соответствующие разрешения для этих служб, а также для универсальных групп безопасности, которые создаются при установке Lync Server.</span><span class="sxs-lookup"><span data-stu-id="5b2f7-116">By default, the cmdlet checks your whole Lync Server infrastructure, verifying that the required services are running and that the appropriate permissions are set for these services and for the universal security groups that are created when you install Lync Server.</span></span>

<span data-ttu-id="5b2f7-117">Помимо проверки действительности установки Lync Server, Test-CsTopology также позволяет проверить правильность конкретной службы.</span><span class="sxs-lookup"><span data-stu-id="5b2f7-117">In addition to verifying the validity of the Lync Server installation, Test-CsTopology also lets you check the validity of a specific service.</span></span> <span data-ttu-id="5b2f7-118">Например, эта команда проверяет состояние сервера конференц-связи A/V в пуле atl-cs-001.litwareinc.com:</span><span class="sxs-lookup"><span data-stu-id="5b2f7-118">For example, this command checks the state of the A/V Conferencing Server on the pool atl-cs-001.litwareinc.com:</span></span>

    Test-CsTopology -Service "ConferencingServer:atl-cs-001.litwareinc.com"

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="5b2f7-119">Выполнение теста</span><span class="sxs-lookup"><span data-stu-id="5b2f7-119">Running the test</span></span>

<span data-ttu-id="5b2f7-120">По умолчанию в Test-CsTopology отображается очень маленький вывод на экран.</span><span class="sxs-lookup"><span data-stu-id="5b2f7-120">By default, Test-CsTopology displays very little output on-screen.</span></span> <span data-ttu-id="5b2f7-121">Вместо этого данные, возвращаемые командлетом, записываются в HTML-файл.</span><span class="sxs-lookup"><span data-stu-id="5b2f7-121">Instead, information returned by the cmdlet is written to an HTML file.</span></span> <span data-ttu-id="5b2f7-122">Параметр Report позволяет указать путь к файлу и имя файла для HTML-файла, созданного с помощью Test-CsTopology.</span><span class="sxs-lookup"><span data-stu-id="5b2f7-122">The Report parameter allows you to specify a file path and file name for the HTML file generated by Test-CsTopology.</span></span> <span data-ttu-id="5b2f7-123">Если параметр отчета не указан, HTML-файл будет автоматически сохранен в папке Users и будет выглядеть так: ce84964a-c4da-4622-ad34-c54ff3ed361f.html.</span><span class="sxs-lookup"><span data-stu-id="5b2f7-123">If you do not include the Report parameter the HTML file will automatically be saved to your Users folder and be given a name similar to this: ce84964a-c4da-4622-ad34-c54ff3ed361f.html.</span></span>

<span data-ttu-id="5b2f7-124">В следующем образце команды выполняется Test-CsTopology и данные сохраняются в файле с именем C: \\ Logs \\ComputerTest.html:</span><span class="sxs-lookup"><span data-stu-id="5b2f7-124">The following sample command runs Test-CsTopology and saves the output to a file that is named C:\\Logs\\ComputerTest.html:</span></span>

    Test-CsTopology -Report "C:\Logs\ComputerTest.html" -Verbose

<span data-ttu-id="5b2f7-125">Дополнительные сведения можно найти в справочной документации по командлету [Test-CsTopology](https://docs.microsoft.com/powershell/module/skype/Test-CsTopology) .</span><span class="sxs-lookup"><span data-stu-id="5b2f7-125">For more information, see the Help documentation for the [Test-CsTopology](https://docs.microsoft.com/powershell/module/skype/Test-CsTopology) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="5b2f7-126">Определение успеха или сбоя</span><span class="sxs-lookup"><span data-stu-id="5b2f7-126">Determining success or failure</span></span>

<span data-ttu-id="5b2f7-127">В отличие от большинства командлетов теста, Test-CsTopology сообщает об успешном завершении или сбое.</span><span class="sxs-lookup"><span data-stu-id="5b2f7-127">Unlike most of the test cmdlets, Test-CsTopology does report back Success or Failure.</span></span> <span data-ttu-id="5b2f7-128">Частично, это связано с большим количеством проверок, которое командлет должен выполнять каждый раз при запуске.</span><span class="sxs-lookup"><span data-stu-id="5b2f7-128">In part, that’s due to the large number of verification checks that the cmdlet must make every time that it runs.</span></span> <span data-ttu-id="5b2f7-129">Вместо этого данные сохраняются в отчете в формате HTML, который затем можно просматривать с помощью Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="5b2f7-129">Instead, data is saved to an HTML report that can then be viewed by using Internet Explorer.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="5b2f7-130">Причины, по которым может произойти сбой теста</span><span class="sxs-lookup"><span data-stu-id="5b2f7-130">Reasons why the test might have failed</span></span>

<span data-ttu-id="5b2f7-131">Ниже приведены некоторые распространенные причины, по которым может произойти сбой Test-CsTopology.</span><span class="sxs-lookup"><span data-stu-id="5b2f7-131">Here are some common reasons why Test-CsTopology might fail:</span></span>

  - <span data-ttu-id="5b2f7-132">Репликация может быть неактуальной на тестовом компьютере.</span><span class="sxs-lookup"><span data-stu-id="5b2f7-132">Replication might not be up-to-date on the test computer.</span></span> <span data-ttu-id="5b2f7-133">Вы можете проверить текущее состояние репликации для компьютера, запустив командлет Get-CsManagementStoreReplicationStatus:</span><span class="sxs-lookup"><span data-stu-id="5b2f7-133">You can check the current replication status for a computer by running the Get-CsManagementStoreReplicationStatus cmdlet:</span></span>
    
        Get-CsManagementStoreReplicationStatus -ReplicaFqdn "atl-cs-001.litwareinc.com"
    
    <span data-ttu-id="5b2f7-134">Если состояние репликации не устарело, вы можете вручную выполнить принудительную репликацию с помощью следующей команды:</span><span class="sxs-lookup"><span data-stu-id="5b2f7-134">If the replication status is not up-to-date, you can manually force replication to occur by using a command similar to this:</span></span>
    
        Invoke-CsManagementStoreReplication -ReplicaFqdn "atl-cs-001.litwareinc.com"

  - <span data-ttu-id="5b2f7-135">Возможно, требуется включить топологию.</span><span class="sxs-lookup"><span data-stu-id="5b2f7-135">The topology might have to be enabled.</span></span> <span data-ttu-id="5b2f7-136">Если вы измените топологию Lync Server (изменения, которые могут повлиять на локальный компьютер), необходимо включить новую топологию.</span><span class="sxs-lookup"><span data-stu-id="5b2f7-136">If you change the Lync Server topology (changes that might affect the local computer), then you must enable the new topology.</span></span> <span data-ttu-id="5b2f7-137">Вы можете включить топологию в любое время, выполнив следующую команду:</span><span class="sxs-lookup"><span data-stu-id="5b2f7-137">You can enable the topology at any time by running this command:</span></span>
    
        Enable-CsTopology

<span data-ttu-id="5b2f7-138"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5b2f7-138"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

