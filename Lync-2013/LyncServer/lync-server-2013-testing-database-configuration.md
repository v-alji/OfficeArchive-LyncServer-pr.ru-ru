---
title: 'Lync Server 2013: Проверка конфигурации базы данных'
description: 'Lync Server 2013: Проверка конфигурации базы данных.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing database configuration
ms:assetid: 60f7fcd2-5efe-4791-b159-b0f9bf39a41b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn727307(v=OCS.15)
ms:contentKeyID: 63969606
ms.date: 07/07/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2b9f88eee99c4a2d523cc84df401dcc1d7b9fe59
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441041"
---
# <a name="testing-database-configuration-in-lync-server-2013"></a><span data-ttu-id="ec336-103">Проверка конфигурации базы данных в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ec336-103">Testing database configuration in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ec336-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ec336-104">

<span> </span></span></span>

<span data-ttu-id="ec336-105">_**Тема последнего изменения:** 2016-07-07_</span><span class="sxs-lookup"><span data-stu-id="ec336-105">_**Topic Last Modified:** 2016-07-07_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ec336-106">Расписание проверки</span><span class="sxs-lookup"><span data-stu-id="ec336-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="ec336-107">Ежедневно</span><span class="sxs-lookup"><span data-stu-id="ec336-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec336-108">Средство тестирования</span><span class="sxs-lookup"><span data-stu-id="ec336-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="ec336-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="ec336-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec336-110">Требуемые разрешения</span><span class="sxs-lookup"><span data-stu-id="ec336-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="ec336-111">При локальном запуске с помощью командной консоли Lync Server пользователи должны быть членами группы безопасности RTCUniversalServerAdmins и должны иметь права администратора на сервере SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ec336-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group, and need to have Administrator privileges on the SQL server.</span></span></p>
<p><span data-ttu-id="ec336-112">При запуске с помощью удаленного экземпляра Windows PowerShell пользователям должна быть назначена роль RBAC, имеющая разрешение на запуск командлета <strong>Test-CsDatabase</strong> .</span><span class="sxs-lookup"><span data-stu-id="ec336-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the <strong>Test-CsDatabase</strong> cmdlet.</span></span> <span data-ttu-id="ec336-113">Чтобы просмотреть список всех ролей RBAC, которые могут использовать этот командлет, выполните в командной строке Windows PowerShell следующую команду:</span><span class="sxs-lookup"><span data-stu-id="ec336-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsDatabase&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="ec336-114">Описание</span><span class="sxs-lookup"><span data-stu-id="ec336-114">Description</span></span>

<span data-ttu-id="ec336-115">Командлет **Test-CsDatabase** проверяет подключение к одной или нескольким базам данных Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ec336-115">The **Test-CsDatabase** cmdlet verifies connectivity to one or more Lync Server 2013 databases.</span></span> <span data-ttu-id="ec336-116">При запуске командлет **Test-CsDatabase** считывает топологию Lync Server, пытается подключиться к соответствующим базам данных, а затем сообщает об успешном завершении или сбое каждой попытки.</span><span class="sxs-lookup"><span data-stu-id="ec336-116">When run, the **Test-CsDatabase** cmdlet reads the Lync Server topology, attempts to connect to relevant databases, and then reports back the success or failure of each try.</span></span> <span data-ttu-id="ec336-117">Если подключение может быть установлено, командлет также сообщит такую информацию, как имя базы данных, сведения о версии SQL Server и расположение установленных зеркальных баз данных.</span><span class="sxs-lookup"><span data-stu-id="ec336-117">If a connection can be made, the cmdlet will also report back such information as the database name, SQL Server version information, and the location of any installed mirror databases.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="ec336-118">Выполнение теста</span><span class="sxs-lookup"><span data-stu-id="ec336-118">Running the test</span></span>

<span data-ttu-id="ec336-119">Команда, показанная в примере 1, проверяет конфигурацию базы данных Центрального управления.</span><span class="sxs-lookup"><span data-stu-id="ec336-119">The command shown in Example 1 verifies the configuration of the Central Management database.</span></span>

    Test-CsDatabase -CentralManagementDatabase

<span data-ttu-id="ec336-120">Пример 2: проверка всех баз данных Lync Server, установленных на компьютере atl-sql-001.litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="ec336-120">Example 2 verifies all the Lync Server databases installed on the computer atl-sql-001.litwareinc.com.</span></span>

    Test-CsDatabase -ConfiguredDatabases -SqlServerFqdn "atl-sql-001.litwareinc.com"

<span data-ttu-id="ec336-121">В примере 3 Проверка выполняется только для архивной базы данных, установленной на компьютере atl-sql-001.litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="ec336-121">In Example 3, verification is performed only for the Archiving database installed on the computer atl-sql-001.litwareinc.com.</span></span> <span data-ttu-id="ec336-122">Обратите внимание, что параметр SqlInstanceName включает экземпляр SQL Server (Archinst), в котором находится база данных архивации.</span><span class="sxs-lookup"><span data-stu-id="ec336-122">Note that the SqlInstanceName parameter is included to specify the SQL Server instance (Archinst) where the Archiving database is located.</span></span>

    Test-CsDatabase -DatabaseType "Archiving" -SqlServerFqdn "atl-sql-001.litwareinc.com" -SqlInstanceName "archinst"

<span data-ttu-id="ec336-123">Команда, показанная в примере 4, проверяет базы данных, установленные на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="ec336-123">The command shown in Example 4 verifies the databases installed on the local computer.</span></span>

    Test-CsDatabase -LocalService

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="ec336-124">Определение успеха или сбоя</span><span class="sxs-lookup"><span data-stu-id="ec336-124">Determining success or failure</span></span>

<span data-ttu-id="ec336-125">Если подключение к базам данных настроено должным образом, вы получите такие данные, как, например, свойство успешно, помеченное как **Истина**:</span><span class="sxs-lookup"><span data-stu-id="ec336-125">If database connectivity is configured correctly, you'll receive output similar to this, with the Succeed property marked as **True**:</span></span>

<span data-ttu-id="ec336-126">SqlServerFqdn: atl-sql-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="ec336-126">SqlServerFqdn : atl-sql-001.litwareinc.com</span></span>

<span data-ttu-id="ec336-127">SqlInstanceName: RTC</span><span class="sxs-lookup"><span data-stu-id="ec336-127">SqlInstanceName : rtc</span></span>

<span data-ttu-id="ec336-128">MirrorSqlServerFqdn :</span><span class="sxs-lookup"><span data-stu-id="ec336-128">MirrorSqlServerFqdn :</span></span>

<span data-ttu-id="ec336-129">MirrorSqlInstanceName :</span><span class="sxs-lookup"><span data-stu-id="ec336-129">MirrorSqlInstanceName :</span></span>

<span data-ttu-id="ec336-130">DatabaseName: XDS</span><span class="sxs-lookup"><span data-stu-id="ec336-130">DatabaseName : xds</span></span>

<span data-ttu-id="ec336-131">Источников</span><span class="sxs-lookup"><span data-stu-id="ec336-131">DataSource :</span></span>

<span data-ttu-id="ec336-132">SQLServerVersion :</span><span class="sxs-lookup"><span data-stu-id="ec336-132">SQLServerVersion :</span></span>

<span data-ttu-id="ec336-133">ExpectedVersion : 10.13.2</span><span class="sxs-lookup"><span data-stu-id="ec336-133">ExpectedVersion : 10.13.2</span></span>

<span data-ttu-id="ec336-134">InstalledVersion :</span><span class="sxs-lookup"><span data-stu-id="ec336-134">InstalledVersion :</span></span>

<span data-ttu-id="ec336-135">Успешно: истина</span><span class="sxs-lookup"><span data-stu-id="ec336-135">Succeed : True</span></span>

<span data-ttu-id="ec336-136">SqlServerFqdn: atl-sql-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="ec336-136">SqlServerFqdn : atl-sql-001.litwareinc.com</span></span>

<span data-ttu-id="ec336-137">SqlInstanceName: RTC</span><span class="sxs-lookup"><span data-stu-id="ec336-137">SqlInstanceName : rtc</span></span>

<span data-ttu-id="ec336-138">MirrorSqlServerFqdn :</span><span class="sxs-lookup"><span data-stu-id="ec336-138">MirrorSqlServerFqdn :</span></span>

<span data-ttu-id="ec336-139">MirrorSqlInstanceName :</span><span class="sxs-lookup"><span data-stu-id="ec336-139">MirrorSqlInstanceName :</span></span>

<span data-ttu-id="ec336-140">Имя базы: LIS</span><span class="sxs-lookup"><span data-stu-id="ec336-140">DatabaseName : lis</span></span>

<span data-ttu-id="ec336-141">Источников</span><span class="sxs-lookup"><span data-stu-id="ec336-141">DataSource :</span></span>

<span data-ttu-id="ec336-142">SQLServerVersion :</span><span class="sxs-lookup"><span data-stu-id="ec336-142">SQLServerVersion :</span></span>

<span data-ttu-id="ec336-143">ExpectedVersion : 3.1.1</span><span class="sxs-lookup"><span data-stu-id="ec336-143">ExpectedVersion : 3.1.1</span></span>

<span data-ttu-id="ec336-144">InstalledVersion :</span><span class="sxs-lookup"><span data-stu-id="ec336-144">InstalledVersion :</span></span>

<span data-ttu-id="ec336-145">Успешно: истина</span><span class="sxs-lookup"><span data-stu-id="ec336-145">Succeed : True</span></span>

<span data-ttu-id="ec336-146">Если база данных настроена правильно, но по-прежнему доступна, поле "успешно" будет отображаться как " **ложь**", а также будут указаны дополнительные предупреждения и сведения.</span><span class="sxs-lookup"><span data-stu-id="ec336-146">If the database is configured correctly but still available, the Succeed field will be shown as **False**, and additional warnings and information will be provided:</span></span>

<span data-ttu-id="ec336-147">SqlServerFqdn: atl-sql-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="ec336-147">SqlServerFqdn : atl-sql-001.litwareinc.com</span></span>

<span data-ttu-id="ec336-148">SqlInstanceName: RTC</span><span class="sxs-lookup"><span data-stu-id="ec336-148">SqlInstanceName : rtc</span></span>

<span data-ttu-id="ec336-149">MirrorSqlServerFqdn :</span><span class="sxs-lookup"><span data-stu-id="ec336-149">MirrorSqlServerFqdn :</span></span>

<span data-ttu-id="ec336-150">MirrorSqlInstanceName :</span><span class="sxs-lookup"><span data-stu-id="ec336-150">MirrorSqlInstanceName :</span></span>

<span data-ttu-id="ec336-151">DatabaseName: XDS</span><span class="sxs-lookup"><span data-stu-id="ec336-151">DatabaseName : xds</span></span>

<span data-ttu-id="ec336-152">Источников</span><span class="sxs-lookup"><span data-stu-id="ec336-152">DataSource :</span></span>

<span data-ttu-id="ec336-153">SQLServerVersion :</span><span class="sxs-lookup"><span data-stu-id="ec336-153">SQLServerVersion :</span></span>

<span data-ttu-id="ec336-154">ExpectedVersion : 10.13.2</span><span class="sxs-lookup"><span data-stu-id="ec336-154">ExpectedVersion : 10.13.2</span></span>

<span data-ttu-id="ec336-155">InstalledVersion :</span><span class="sxs-lookup"><span data-stu-id="ec336-155">InstalledVersion :</span></span>

<span data-ttu-id="ec336-156">Успешно: ложь</span><span class="sxs-lookup"><span data-stu-id="ec336-156">Succeed : False</span></span>

<span data-ttu-id="ec336-157">SqlServerFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="ec336-157">SqlServerFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="ec336-158">SqlInstanceName: RTC</span><span class="sxs-lookup"><span data-stu-id="ec336-158">SqlInstanceName : rtc</span></span>

<span data-ttu-id="ec336-159">MirrorSqlServerFqdn :</span><span class="sxs-lookup"><span data-stu-id="ec336-159">MirrorSqlServerFqdn :</span></span>

<span data-ttu-id="ec336-160">MirrorSqlInstanceName :</span><span class="sxs-lookup"><span data-stu-id="ec336-160">MirrorSqlInstanceName :</span></span>

<span data-ttu-id="ec336-161">Имя базы: LIS</span><span class="sxs-lookup"><span data-stu-id="ec336-161">DatabaseName : lis</span></span>

<span data-ttu-id="ec336-162">Источников</span><span class="sxs-lookup"><span data-stu-id="ec336-162">DataSource :</span></span>

<span data-ttu-id="ec336-163">SQLServerVersion :</span><span class="sxs-lookup"><span data-stu-id="ec336-163">SQLServerVersion :</span></span>

<span data-ttu-id="ec336-164">ExpectedVersion : 3.1.1</span><span class="sxs-lookup"><span data-stu-id="ec336-164">ExpectedVersion : 3.1.1</span></span>

<span data-ttu-id="ec336-165">InstalledVersion :</span><span class="sxs-lookup"><span data-stu-id="ec336-165">InstalledVersion :</span></span>

<span data-ttu-id="ec336-166">Успешно: ложь</span><span class="sxs-lookup"><span data-stu-id="ec336-166">Succeed : False</span></span>

<span data-ttu-id="ec336-167">Предупреждение: в Test-CsDatabase обнаружены ошибки.</span><span class="sxs-lookup"><span data-stu-id="ec336-167">WARNING: Test-CsDatabase encountered errors.</span></span> <span data-ttu-id="ec336-168">Просмотрите файл журнала для</span><span class="sxs-lookup"><span data-stu-id="ec336-168">Consult the log file for a</span></span>

<span data-ttu-id="ec336-169">подробный анализ и проверка того, что все ошибки (2) и предупреждения (0) рассмотрены.</span><span class="sxs-lookup"><span data-stu-id="ec336-169">detailed analysis, and to make sure that all errors (2) and warnings (0) are addressed</span></span>

<span data-ttu-id="ec336-170">перед продолжением.</span><span class="sxs-lookup"><span data-stu-id="ec336-170">before continuing.</span></span>

<span data-ttu-id="ec336-171">Предупреждение: подробные результаты можно найти по адресу</span><span class="sxs-lookup"><span data-stu-id="ec336-171">WARNING: Detailed results can be found at</span></span>

<span data-ttu-id="ec336-172">"C: \\ Пользователи \\ проверяют \\ \\ Каталог AppData Local \\ temp \\ 2 \\ Test-CsDatabase-b18d488a-8044-4679-bbf2-</span><span class="sxs-lookup"><span data-stu-id="ec336-172">"C:\\Users\\Testing\\AppData\\Local\\Temp\\2\\Test-CsDatabase-b18d488a-8044-4679-bbf2-</span></span>

<span data-ttu-id="ec336-173">04d593cce8e6.html ".</span><span class="sxs-lookup"><span data-stu-id="ec336-173">04d593cce8e6.html".</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="ec336-174">Причины, по которым может произойти сбой теста</span><span class="sxs-lookup"><span data-stu-id="ec336-174">Reasons why the test might have failed</span></span>

<span data-ttu-id="ec336-175">Ниже приведены некоторые распространенные причины, по которым может произойти сбой **Test-CsDatabase** :</span><span class="sxs-lookup"><span data-stu-id="ec336-175">Here are some common reasons why **Test-CsDatabase** might fail:</span></span>

  - <span data-ttu-id="ec336-176">Предоставлено неправильное значение параметра.</span><span class="sxs-lookup"><span data-stu-id="ec336-176">An incorrect parameter value was supplied.</span></span> <span data-ttu-id="ec336-177">Если используется, необязательные параметры необходимо настроить правильно, или тест завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="ec336-177">If used, the optional parameters must be configured correctly or the test will fail.</span></span> <span data-ttu-id="ec336-178">Повторите выполнение команды без дополнительных параметров и проверьте, выполняется ли это успешно.</span><span class="sxs-lookup"><span data-stu-id="ec336-178">Rerun the command without the optional parameters and see whether that succeeds.</span></span>

  - <span data-ttu-id="ec336-179">Эта команда завершается сбоем, если база данных неправильно настроена или еще не развернута.</span><span class="sxs-lookup"><span data-stu-id="ec336-179">This command will fail if the database is misconfigured or not yet deployed.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="ec336-180">См. также</span><span class="sxs-lookup"><span data-stu-id="ec336-180">See Also</span></span>


[<span data-ttu-id="ec336-181">Get-CsDatabaseMirrorState</span><span class="sxs-lookup"><span data-stu-id="ec336-181">Get-CsDatabaseMirrorState</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsDatabaseMirrorState)  
[<span data-ttu-id="ec336-182">Get-CsService</span><span class="sxs-lookup"><span data-stu-id="ec336-182">Get-CsService</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsService)  
[<span data-ttu-id="ec336-183">Get-CsUserDatabaseState</span><span class="sxs-lookup"><span data-stu-id="ec336-183">Get-CsUserDatabaseState</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsUserDatabaseState)  
  

<span data-ttu-id="ec336-184"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ec336-184"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

