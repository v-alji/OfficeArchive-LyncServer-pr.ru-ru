---
title: 'Lync Server 2013: Проверка службы реплики'
description: 'Lync Server 2013: Проверка службы реплики.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing the replica service
ms:assetid: 4ff2cc91-0036-4c5a-9792-7bf43d8ce18d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn727303(v=OCS.15)
ms:contentKeyID: 63969600
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a61751b95115da3d6519f20f52262b7159ffcbfe
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440978"
---
# <a name="testing-the-replica-service-in-lync-server-2013"></a><span data-ttu-id="bb975-103">Проверка службы реплики в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bb975-103">Testing the replica service in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bb975-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bb975-104">

<span> </span></span></span>

<span data-ttu-id="bb975-105">_**Тема последнего изменения:** 2014-11-03_</span><span class="sxs-lookup"><span data-stu-id="bb975-105">_**Topic Last Modified:** 2014-11-03_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bb975-106">Расписание проверки</span><span class="sxs-lookup"><span data-stu-id="bb975-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="bb975-107">Ежедневно</span><span class="sxs-lookup"><span data-stu-id="bb975-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb975-108">Средство тестирования</span><span class="sxs-lookup"><span data-stu-id="bb975-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="bb975-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="bb975-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb975-110">Требуемые разрешения</span><span class="sxs-lookup"><span data-stu-id="bb975-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="bb975-111">При локальном запуске с помощью командной консоли Lync Server пользователи должны быть членами группы безопасности RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="bb975-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="bb975-112">При запуске с помощью удаленного экземпляра Windows PowerShell пользователям должна быть назначена роль RBAC, имеющая разрешение на запуск командлета <strong>Test-CsReplica</strong> .</span><span class="sxs-lookup"><span data-stu-id="bb975-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the <strong>Test-CsReplica</strong> cmdlet.</span></span> <span data-ttu-id="bb975-113">Чтобы просмотреть список всех ролей RBAC, которые могут использовать этот командлет, выполните в командной строке Windows PowerShell следующую команду:</span><span class="sxs-lookup"><span data-stu-id="bb975-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsReplica&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="bb975-114">Описание</span><span class="sxs-lookup"><span data-stu-id="bb975-114">Description</span></span>

<span data-ttu-id="bb975-115">Командлет **Test-CsReplica** проверяет, запущена ли служба реплики Lync Server 2013 на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="bb975-115">The **Test-CsReplica** cmdlet verifies that the Lync Server 2013 replica service is running on the local computer.</span></span> <span data-ttu-id="bb975-116">Командлет **Test-CsReplica** выполняет такие задачи, как:</span><span class="sxs-lookup"><span data-stu-id="bb975-116">The **Test-CsReplica** cmdlet performs such tasks as:</span></span>

  - <span data-ttu-id="bb975-117">Проверка состояния агента Replicator и службы агента централизованного ведения журнала</span><span class="sxs-lookup"><span data-stu-id="bb975-117">checking the status of the Replicator Agent and Centralized Logging Agent services</span></span>

  - <span data-ttu-id="bb975-118">Проверка того, что нужные порты были открыты в брандмауэре Windows</span><span class="sxs-lookup"><span data-stu-id="bb975-118">verifying that the required ports were opened in the Windows Firewall</span></span>

  - <span data-ttu-id="bb975-119">Убедитесь в наличии необходимых групп безопасности Active Directory и локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="bb975-119">making sure that the necessary Active Directory and local computer security groups exist.</span></span>

<span data-ttu-id="bb975-120">Обратите внимание, что этот командлет должен выполняться локально.</span><span class="sxs-lookup"><span data-stu-id="bb975-120">Note that this cmdlet must be run locally.</span></span> <span data-ttu-id="bb975-121">Это значит, что она должна быть запущена на том же компьютере, на котором запущена служба реплики.</span><span class="sxs-lookup"><span data-stu-id="bb975-121">That is, it must be run on the same computer where the replica service is running.</span></span> <span data-ttu-id="bb975-122">Для запуска командлета **Test-CsReplica** с удаленным сервером не существует параметров.</span><span class="sxs-lookup"><span data-stu-id="bb975-122">There are no options for running the **Test-CsReplica** cmdlet against a remote server.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="bb975-123">Выполнение теста</span><span class="sxs-lookup"><span data-stu-id="bb975-123">Running the test</span></span>

<span data-ttu-id="bb975-124">Команда, показанная в примере 1, проверяет службу реплики Lync Server 2013 на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="bb975-124">The command shown in Example 1 tests the Lync Server 2013 replica service on the local computer.</span></span> <span data-ttu-id="bb975-125">В этом примере параметр Verbose используется для того, чтобы гарантировать, что сведения о тесте — в том числе в конечном итоге отказа или успешности теста, а также расположение отчета, созданного тестом — отображается на экране.</span><span class="sxs-lookup"><span data-stu-id="bb975-125">In this example the Verbose parameter is used to guarantee that information about the test – including the eventual failure or success of the test and the location of the report generated by the test – is displayed on screen.</span></span>

    Test-CsReplica -Verbose

<span data-ttu-id="bb975-126">Пример 2 — это вариант команды, показанный в примере 1.</span><span class="sxs-lookup"><span data-stu-id="bb975-126">Example 2 is a variation of the command shown in Example 1.</span></span> <span data-ttu-id="bb975-127">В этом случае параметр отчета включает в себя путь к папке и имя для отчета, созданного с помощью теста.</span><span class="sxs-lookup"><span data-stu-id="bb975-127">In this case, the Report parameter is included to specify a folder path and name for the report generated by the test.</span></span> <span data-ttu-id="bb975-128">Если не указать путь к отчету, ему будет автоматически сгенерировано такое имя, как:</span><span class="sxs-lookup"><span data-stu-id="bb975-128">If you do not specify a report path the report will be given an auto-generated name similar to this:</span></span>

<span data-ttu-id="bb975-129">C: \\ Пользователи \\ администратор. плана litwareinc \\ AppData \\ Local \\ temp \\ 1 \\Test-Cs-Replica-3db40ee0-4b5d-4f58-8d3d-b1e61253129e.html</span><span class="sxs-lookup"><span data-stu-id="bb975-129">C:\\Users\\Administrator.Litwareinc\\AppData\\Local\\Temp\\1\\Test-Cs-Replica-3db40ee0-4b5d-4f58-8d3d-b1e61253129e.html</span></span>

    Test-CsReplica -Verbose -Report C:\Logs\ReplicaTest.html

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="bb975-130">Определение успеха или сбоя</span><span class="sxs-lookup"><span data-stu-id="bb975-130">Determining success or failure</span></span>

<span data-ttu-id="bb975-131">Вставить текст раздела здесь.</span><span class="sxs-lookup"><span data-stu-id="bb975-131">Insert section body here.</span></span>

<span data-ttu-id="bb975-132">ПОДРОБНЫй: создание нового файла журнала "C: \\ Пользователи \\ тестирование \\ \\ локальной \\ папке AppData \\Test-CsReplica-3cb066b3-dd23-411a-8932-99f01c0f940c.xml".</span><span class="sxs-lookup"><span data-stu-id="bb975-132">VERBOSE: Creating new log file "C:\\Users\\Testing\\AppData\\Local\\Temp\\Test-CsReplica-3cb066b3-dd23-411a-8932-99f01c0f940c.xml".</span></span>

<span data-ttu-id="bb975-133">ПОДРОБНЫй: создание нового файла журнала "C: \\ Пользователи \\ тестирование \\ \\ локальной \\ папке AppData \\Test-CsReplica-3cb066b3-dd23-411a-8932-99f01c0f940c.xml".</span><span class="sxs-lookup"><span data-stu-id="bb975-133">VERBOSE: Creating new log file "C:\\Users\\Testing\\AppData\\Local\\Temp\\Test-CsReplica-3cb066b3-dd23-411a-8932-99f01c0f940c.xml".</span></span>

<span data-ttu-id="bb975-134">ПОДРОБНОе сообщение: обработка "Test-CsReplica" успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="bb975-134">VERBOSE: "Test-CsReplica" processing has completed successfully.</span></span>

<span data-ttu-id="bb975-135">ПОДРОБНЫй: подробные результаты можно найти на странице "C: \\ Пользователи \\ тестирование" \\ AppData \\ Local \\ temp \\Test-CsReplica-3cb066b3-dd23-411a-8932-99f01c0f940c.xml ".</span><span class="sxs-lookup"><span data-stu-id="bb975-135">VERBOSE: Detailed results can be found at "C:\\Users\\Testing\\AppData\\Local\\Temp\\Test-CsReplica-3cb066b3-dd23-411a-8932-99f01c0f940c.xml".</span></span>

<span data-ttu-id="bb975-136">ПОДРОБНЫй: создание нового файла журнала</span><span class="sxs-lookup"><span data-stu-id="bb975-136">VERBOSE: Creating new log file</span></span>

<span data-ttu-id="bb975-137">"C: \\ Пользователи \\ проверяют \\ \\ Каталог AppData Local \\ temp \\ 2 \\ Test-CsReplica-29fddb35-f56e-4e3c-8f4c-e</span><span class="sxs-lookup"><span data-stu-id="bb975-137">"C:\\Users\\Testing\\AppData\\Local\\Temp\\2\\Test-CsReplica-29fddb35-f56e-4e3c-8f4c-e</span></span>

<span data-ttu-id="bb975-138">d3bd0e4a083.xml ".</span><span class="sxs-lookup"><span data-stu-id="bb975-138">d3bd0e4a083.xml".</span></span>

<span data-ttu-id="bb975-139">ПОДРОБНЫй: создание нового файла журнала</span><span class="sxs-lookup"><span data-stu-id="bb975-139">VERBOSE: Creating new log file</span></span>

<span data-ttu-id="bb975-140">"C: \\ Пользователи \\ проверяют \\ \\ Каталог AppData Local \\ temp \\ 2 \\ Test-CsReplica-29fddb35-f56e-4e3c-8f4c-e</span><span class="sxs-lookup"><span data-stu-id="bb975-140">"C:\\Users\\Testing\\AppData\\Local\\Temp\\2\\Test-CsReplica-29fddb35-f56e-4e3c-8f4c-e</span></span>

<span data-ttu-id="bb975-141">d3bd0e4a083.html ".</span><span class="sxs-lookup"><span data-stu-id="bb975-141">d3bd0e4a083.html".</span></span>

<span data-ttu-id="bb975-142">Предупреждение: Test-CsReplica не удалось.</span><span class="sxs-lookup"><span data-stu-id="bb975-142">WARNING: Test-CsReplica failed.</span></span>

<span data-ttu-id="bb975-143">Предупреждение: подробные результаты можно найти по адресу</span><span class="sxs-lookup"><span data-stu-id="bb975-143">WARNING: Detailed results can be found at</span></span>

<span data-ttu-id="bb975-144">"C: \\ Пользователи \\ проверяют \\ \\ Каталог AppData Local \\ temp \\ 2 \\ Test-CsReplica-29fddb35-f56e-4e3c-8f4c-e</span><span class="sxs-lookup"><span data-stu-id="bb975-144">"C:\\Users\\Testing\\AppData\\Local\\Temp\\2\\Test-CsReplica-29fddb35-f56e-4e3c-8f4c-e</span></span>

<span data-ttu-id="bb975-145">d3bd0e4a083.html ".</span><span class="sxs-lookup"><span data-stu-id="bb975-145">d3bd0e4a083.html".</span></span>

<span data-ttu-id="bb975-146">Test-CsReplica: не удалось выполнить команду: запрошенный доступ к реестру не</span><span class="sxs-lookup"><span data-stu-id="bb975-146">Test-CsReplica : Command execution failed: Requested registry access is not</span></span>

<span data-ttu-id="bb975-147">использоваться.</span><span class="sxs-lookup"><span data-stu-id="bb975-147">allowed.</span></span>

<span data-ttu-id="bb975-148">В строке: 1 символ: 1</span><span class="sxs-lookup"><span data-stu-id="bb975-148">At line:1 char:1</span></span>

<span data-ttu-id="bb975-149">\+ Test-CsReplica — подробный</span><span class="sxs-lookup"><span data-stu-id="bb975-149">\+ Test-CsReplica -Verbose</span></span>

\+ ~~~~~~~~~~~~~~~~~~~~~~~

<span data-ttu-id="bb975-150">\+ CategoryInfo: InvalidOperation: (:) \[ Test-CsReplica \] , безопасность</span><span class="sxs-lookup"><span data-stu-id="bb975-150">\+ CategoryInfo : InvalidOperation: (:) \[Test-CsReplica\], Security</span></span>

<span data-ttu-id="bb975-151">Ошибка</span><span class="sxs-lookup"><span data-stu-id="bb975-151">Exception</span></span>

<span data-ttu-id="bb975-152">\+ FullyQualifiedErrorId: ProcessingFailed, Microsoft. RTC. Management. deploy</span><span class="sxs-lookup"><span data-stu-id="bb975-152">\+ FullyQualifiedErrorId : ProcessingFailed,Microsoft.Rtc.Management.Deploy</span></span>

<span data-ttu-id="bb975-153">чения. TestReplicaCmdlet</span><span class="sxs-lookup"><span data-stu-id="bb975-153">ment.TestReplicaCmdlet</span></span>

<span data-ttu-id="bb975-154">PS C: \\ \\ Проверка пользователей\></span><span class="sxs-lookup"><span data-stu-id="bb975-154">PS C:\\Users\\Testing\></span></span>

<span data-ttu-id="bb975-155">PS C: \\ Пользователи \\ тестирование \> Test-CsUcwaConference-TargetFqdn "LyncTest. SelfHost. Corp. M</span><span class="sxs-lookup"><span data-stu-id="bb975-155">PS C:\\Users\\Testing\> Test-CsUcwaConference -TargetFqdn "LyncTest.SelfHost.Corp.M</span></span>

<span data-ttu-id="bb975-156">icrosoft.com "</span><span class="sxs-lookup"><span data-stu-id="bb975-156">icrosoft.com"</span></span>

<span data-ttu-id="bb975-157">Предупреждение: не удалось прочитать номер порта регистратора для заданного полного имени</span><span class="sxs-lookup"><span data-stu-id="bb975-157">WARNING: Failed to read Registrar port number for the given fully qualified</span></span>

<span data-ttu-id="bb975-158">доменное имя (FQDN).</span><span class="sxs-lookup"><span data-stu-id="bb975-158">domain name (FQDN).</span></span> <span data-ttu-id="bb975-159">С помощью номера порта регистратора по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bb975-159">Using default Registrar port number.</span></span> <span data-ttu-id="bb975-160">Ошибка</span><span class="sxs-lookup"><span data-stu-id="bb975-160">Exception:</span></span>

<span data-ttu-id="bb975-161">System. InvalidOperationException: в топологии не обнаружены подходящие кластеры.</span><span class="sxs-lookup"><span data-stu-id="bb975-161">System.InvalidOperationException: No matching cluster found in topology.</span></span>

<span data-ttu-id="bb975-162">скорость</span><span class="sxs-lookup"><span data-stu-id="bb975-162">at</span></span>

<span data-ttu-id="bb975-163">Microsoft. RTC. Management. SyntheticTransactions. SipSyntheticTransaction. TryRetri</span><span class="sxs-lookup"><span data-stu-id="bb975-163">Microsoft.Rtc.Management.SyntheticTransactions.SipSyntheticTransaction.TryRetri</span></span>

<span data-ttu-id="bb975-164">eveRegistrarPortFromTopology (Int32& registrarPortNumber)</span><span class="sxs-lookup"><span data-stu-id="bb975-164">eveRegistrarPortFromTopology(Int32& registrarPortNumber)</span></span>

<span data-ttu-id="bb975-165">Test-CsUcwaConference: нет тестового пользователя, назначенного для</span><span class="sxs-lookup"><span data-stu-id="bb975-165">Test-CsUcwaConference : There is no test user assigned for</span></span>

<span data-ttu-id="bb975-166">\[LyncTest.SelfHost.Corp.Microsoft.com \] .</span><span class="sxs-lookup"><span data-stu-id="bb975-166">\[LyncTest.SelfHost.Corp.Microsoft.com\].</span></span> <span data-ttu-id="bb975-167">Проверка конфигурации тестового пользователя.</span><span class="sxs-lookup"><span data-stu-id="bb975-167">Verify test user configuration.</span></span>

<span data-ttu-id="bb975-168">В строке: 1 символ: 1</span><span class="sxs-lookup"><span data-stu-id="bb975-168">At line:1 char:1</span></span>

<span data-ttu-id="bb975-169">\+ Test-CsUcwaConference TargetFqdn "LyncTest.SelfHost.Corp.Microsoft.com"</span><span class="sxs-lookup"><span data-stu-id="bb975-169">\+ Test-CsUcwaConference -TargetFqdn "LyncTest.SelfHost.Corp.Microsoft.com"</span></span>

\+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

<span data-ttu-id="bb975-170">\+ CategoryInfo: ResourceUnavailable: (:) \[ Test-CsUcwaConference\]</span><span class="sxs-lookup"><span data-stu-id="bb975-170">\+ CategoryInfo : ResourceUnavailable: (:) \[Test-CsUcwaConference\]</span></span>

<span data-ttu-id="bb975-171">, InvalidOperationException</span><span class="sxs-lookup"><span data-stu-id="bb975-171">, InvalidOperationException</span></span>

<span data-ttu-id="bb975-172">\+ FullyQualifiedErrorId: NotFoundTestUsers, Microsoft. RTC. Management. синтезатор</span><span class="sxs-lookup"><span data-stu-id="bb975-172">\+ FullyQualifiedErrorId : NotFoundTestUsers,Microsoft.Rtc.Management.Synth</span></span>

<span data-ttu-id="bb975-173">eticTransactions.TestUcwaConferenceCmdlet</span><span class="sxs-lookup"><span data-stu-id="bb975-173">eticTransactions.TestUcwaConferenceCmdlet</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="bb975-174">Причины, по которым может произойти сбой теста</span><span class="sxs-lookup"><span data-stu-id="bb975-174">Reasons why the test might have failed</span></span>

<span data-ttu-id="bb975-175">Ниже приведены некоторые распространенные причины, по которым может произойти сбой **Test-CsReplica** :</span><span class="sxs-lookup"><span data-stu-id="bb975-175">Here are some common reasons why **Test-CsReplica** might fail:</span></span>

  - <span data-ttu-id="bb975-176">Возможно, возникла проблема с агентом тиражирования и службами агента централизованного ведения журнала</span><span class="sxs-lookup"><span data-stu-id="bb975-176">There may be a larger problem with the Replicator Agent and Centralized Logging Agent services</span></span>

  - <span data-ttu-id="bb975-177">Возможно, требуемые порты не открыты в брандмауэре Windows</span><span class="sxs-lookup"><span data-stu-id="bb975-177">The required ports may not be open in the Windows Firewall</span></span>

  - <span data-ttu-id="bb975-178">Возможно, не существует необходимая группа безопасности Active Directory и локального компьютера</span><span class="sxs-lookup"><span data-stu-id="bb975-178">The necessary Active Directory and local computer security groups may not exist</span></span>

<span data-ttu-id="bb975-179"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bb975-179"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

