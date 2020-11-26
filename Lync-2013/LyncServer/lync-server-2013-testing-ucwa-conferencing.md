---
title: 'Lync Server 2013: тестирование конференц-связи по UCWA'
description: 'Lync Server 2013: тестирование конференц-связи UCWA.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing UCWA conferencing
ms:assetid: 62b3866a-0759-4b1f-99ec-5a68d6a74f00
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn727306(v=OCS.15)
ms:contentKeyID: 63969610
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 37f88a683abb67d55211422fc4dcf45fc1d5c966
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439739"
---
# <a name="testing-ucwa-conferencing-in-lync-server-2013"></a><span data-ttu-id="5de07-103">Проверка конференц-связи UCWA в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5de07-103">Testing UCWA conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5de07-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5de07-104">

<span> </span></span></span>

<span data-ttu-id="5de07-105">_**Тема последнего изменения:** 2014-11-03_</span><span class="sxs-lookup"><span data-stu-id="5de07-105">_**Topic Last Modified:** 2014-11-03_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5de07-106">Расписание проверки</span><span class="sxs-lookup"><span data-stu-id="5de07-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="5de07-107">Ежедневно</span><span class="sxs-lookup"><span data-stu-id="5de07-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5de07-108">Средство тестирования</span><span class="sxs-lookup"><span data-stu-id="5de07-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="5de07-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="5de07-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5de07-110">Требуемые разрешения</span><span class="sxs-lookup"><span data-stu-id="5de07-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="5de07-111">При локальном запуске с помощью командной консоли Lync Server пользователи должны быть членами группы безопасности RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="5de07-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="5de07-112">При запуске с помощью удаленного экземпляра Windows PowerShell пользователям должна быть назначена роль RBAC, имеющая разрешение на запуск командлета <strong>Test-CsUcwaConference</strong> .</span><span class="sxs-lookup"><span data-stu-id="5de07-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the <strong>Test-CsUcwaConference</strong> cmdlet.</span></span> <span data-ttu-id="5de07-113">Чтобы просмотреть список всех ролей RBAC, которые могут использовать этот командлет, выполните в командной строке Windows PowerShell следующую команду:</span><span class="sxs-lookup"><span data-stu-id="5de07-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsUcwaConference&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="5de07-114">Описание</span><span class="sxs-lookup"><span data-stu-id="5de07-114">Description</span></span>

<span data-ttu-id="5de07-115">Командлет **Test-CsUcwaConference** удостоверяется в том, что с помощью веб-интерфейса единой системы обмена сообщениями (UCWA) пользователь может запланировать, присоединиться к Конференции и провести сетевую конференцию.</span><span class="sxs-lookup"><span data-stu-id="5de07-115">The **Test-CsUcwaConference** cmdlet verifies that a pair of test users can schedule, join, and then conduct an online conference using the Unified Communications Web API (UCWA).</span></span> <span data-ttu-id="5de07-116">Для этого командлет использует службу веб-билета Lync Server для проверки подлинности двух тестовых пользователей и их регистрации в Lync Server.</span><span class="sxs-lookup"><span data-stu-id="5de07-116">To do this, the cmdlet uses the Lync Server web ticket service to authenticate the two test users and register them with Lync Server.</span></span> <span data-ttu-id="5de07-117">Затем командлет начнет конференцию с использованием учетных данных организатора и приглашает участника присоединиться к собранию.</span><span class="sxs-lookup"><span data-stu-id="5de07-117">The cmdlet then starts a conference using the organizer credentials and invites the participant to join the meeting.</span></span> <span data-ttu-id="5de07-118">После присоединения к собранию командлет **Test-CsUcwaConference** удостоверяет, что пользователи могут выполнять такие действия, как обмен мгновенными сообщениями и объединением, а затем отключает конференцию и отменяет регистрацию двух тестовых пользователей.</span><span class="sxs-lookup"><span data-stu-id="5de07-118">After the meeting is joined, the **Test-CsUcwaConference** cmdlet verifies that the users can do such things as exchange instant message and conduct pools, then disconnects the conference and unregisters the two test users.</span></span> <span data-ttu-id="5de07-119">Запланированная Конференция также будет удалена после завершения теста.</span><span class="sxs-lookup"><span data-stu-id="5de07-119">The scheduled conference will also be deleted when the test is finished.</span></span>

<span data-ttu-id="5de07-120">Командлет **Test-CsUcwaConference** также можно использовать, чтобы определить, могут ли анонимные пользователи присоединиться к онлайн-конференциям.</span><span class="sxs-lookup"><span data-stu-id="5de07-120">The **Test-CsUcwaConference** cmdlet can also be used to determine whether anonymous users can join online conferences.</span></span>

<span data-ttu-id="5de07-121">Обратите внимание, что командлет **Test-CsUcwaConference** не следует запускать для пула Microsoft Lync Server 2010, если UCWA не установлен в этом пуле.</span><span class="sxs-lookup"><span data-stu-id="5de07-121">Note that the **Test-CsUcwaConference** cmdlet should not be run against a Microsoft Lync Server 2010 pool unless UCWA was installed on that pool.</span></span> <span data-ttu-id="5de07-122">Если UCWA не установлен, вызов командлета **Test-CsUcwaConference** завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="5de07-122">If UCWA has not been installed then the call to the **Test-CsUcwaConference** cmdlet will fail.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="5de07-123">Выполнение теста</span><span class="sxs-lookup"><span data-stu-id="5de07-123">Running the test</span></span>

<span data-ttu-id="5de07-124">Команда, показанная в примере 1, проверяет, может ли пользователь, который входит в состав Конференции UCWA в atl-cs-001.litwareinc.com пула, мог принимать участие в паре тестов.</span><span class="sxs-lookup"><span data-stu-id="5de07-124">The command shown in Example 1 verifies that a pair of test users can participate in an UCWA conference on the pool atl-cs-001.litwareinc.com.</span></span> <span data-ttu-id="5de07-125">Обратите внимание, что эта команда завершится сбоем, если вы не предatl-CS-001.litwareinc.com пару пользователей теста конфигурации мониторинга работоспособности для.</span><span class="sxs-lookup"><span data-stu-id="5de07-125">Note that this command will fail if you have not predefined a pair of health monitoring configuration test users for atl-cs-001.litwareinc.com.</span></span>

    Test-CsUcwaConference -TargetFqdn "atl-cs-001.litwareinc.com"

<span data-ttu-id="5de07-126">Команды, показанные в примере 2, проверяют возможности пары пользователей (плана litwareinc \\ почтового и плана litwareinc \\ kenmyer) для участия в UCWA Конференции.</span><span class="sxs-lookup"><span data-stu-id="5de07-126">The commands shown in Example 2 test the ability of a pair of users (litwareinc\\pilar and litwareinc\\kenmyer) to participate in an UCWA conference.</span></span> <span data-ttu-id="5de07-127">Для этого в первой команде примера используется командлет Get-Credential, чтобы создать объект учетных данных интерфейса командной строки Windows PowerShell, содержащий имя и пароль пользователя почтового Вронский.</span><span class="sxs-lookup"><span data-stu-id="5de07-127">To do this, the first command in the example uses the Get-Credential cmdlet to create a Windows PowerShell command-line interface credential object that contains the name and password of the user Pilar Ackerman.</span></span> <span data-ttu-id="5de07-128">(Поскольку имя для входа, плана litwareinc \\ почтового, было включено в качестве параметра, в диалоговом окне Запрос учетных данных Windows PowerShell требуется, чтобы администратор введет пароль для учетной записи почтового Вронский.) Результирующий объект учетных данных сохраняется в переменной с именем $cred 1.</span><span class="sxs-lookup"><span data-stu-id="5de07-128">(Because the logon name, litwareinc\\pilar, was included as a parameter, the Windows PowerShell Credential Request dialog box only requires the administrator to enter the password for the Pilar Ackerman account.) The resulting credentials object is then stored in a variable named $cred1.</span></span> <span data-ttu-id="5de07-129">Вторая команда — это то же самое, что возвращает объект учетной записи Кен Myer.</span><span class="sxs-lookup"><span data-stu-id="5de07-129">The second command does the same thing, this time returning a credential object for the Ken Myer account.</span></span>

<span data-ttu-id="5de07-130">Если у вас есть два объекта учетных данных, третья команда в примере определяет, могут ли два пользователя принимать участие в конференц-связи UCWA.</span><span class="sxs-lookup"><span data-stu-id="5de07-130">With the two credential objects in hand, the third command in the example determines whether the two users can participate in an UCWA conference.</span></span> <span data-ttu-id="5de07-131">Для выполнения этой задачи вызывается командлет **Test-CsUcwaConference** , вместе со следующими параметрами: TargetFqdn (полное доменное имя пула регистраторов). OrganizerSipAddress (SIP-адрес организатора собрания); OrganizerCredential (объект Windows PowerShell, который включает в себя учетные данные для этого пользователя); ParticipantSipAddress (SIP-адрес для другого тестового пользователя); и ParticipantCredential (объект интерфейса командной строки Windows PowerShell, который включает в себя учетные данные для другого пользователя).</span><span class="sxs-lookup"><span data-stu-id="5de07-131">To run this task, the **Test-CsUcwaConference** cmdlet is called, together with the following parameters: TargetFqdn (the FQDN of the Registrar pool); OrganizerSipAddress (the SIP address for the meeting organizer); OrganizerCredential (the Windows PowerShell object that contains the credentials for this same user); ParticipantSipAddress (the SIP address for the other test user); and ParticipantCredential (the Windows PowerShell command-line interface object that contains the credentials for the other user).</span></span>

    $cred1 = Get-Credential "litwareinc\pilar"
    $cred2 = Get-Credential "litwareinc\kenmyer"
    Test-CsUcwaConference -TargetFqdn atl-cs-001.litwareinc.com -OrganizerSipAddress "sip:pilar@litwareinc.com" -OrganizerCredential $cred1 -ParticipantSipAddress "sip:kenmyer@litwareinc.com" -ParticipantCredential $cred2

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="5de07-132">Определение успеха или сбоя</span><span class="sxs-lookup"><span data-stu-id="5de07-132">Determining success or failure</span></span>

<span data-ttu-id="5de07-133">Если вы правильно настраиваете Конференц-связь, вы получите вывод примерно так, чтобы свойство Result пометило **"успешно".**</span><span class="sxs-lookup"><span data-stu-id="5de07-133">If conferencing is correctly configured, you'll receive output similar to this, with the Result property marked as **Success:**</span></span>

<span data-ttu-id="5de07-134">Целевое полное доменное имя: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="5de07-134">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="5de07-135">Конечный URI: https://LyncTest-SE. LyncTest. SelfHost. Corp.</span><span class="sxs-lookup"><span data-stu-id="5de07-135">Target Uri : https:// LyncTest-SE.LyncTest.SelfHost.Corp.</span></span>

<span data-ttu-id="5de07-136">Microsoft.com:443/CertProv/CertProvisiongService.svc</span><span class="sxs-lookup"><span data-stu-id="5de07-136">Microsoft.com:443/CertProv/CertProvisiongService.svc</span></span>

<span data-ttu-id="5de07-137">Результат: успех</span><span class="sxs-lookup"><span data-stu-id="5de07-137">Result : Success</span></span>

<span data-ttu-id="5de07-138">Задержка: 00:00:14.9862716</span><span class="sxs-lookup"><span data-stu-id="5de07-138">Latency : 00:00:14.9862716</span></span>

<span data-ttu-id="5de07-139">Сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="5de07-139">Error Message :</span></span>

<span data-ttu-id="5de07-140">Диагностик</span><span class="sxs-lookup"><span data-stu-id="5de07-140">Diagnosis :</span></span>

<span data-ttu-id="5de07-141">Если указанные пользователи не могут использовать конференц-связь, результат будет отображаться как **сбой**, а дополнительные сведения будут записаны в свойствах Error и диагноз.</span><span class="sxs-lookup"><span data-stu-id="5de07-141">If the specified users can't use conferencing, the Result will be shown as **Failure**, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="5de07-142">Предупреждение: не удалось прочитать номер порта регистратора для заданного полного имени</span><span class="sxs-lookup"><span data-stu-id="5de07-142">WARNING: Failed to read Registrar port number for the given fully qualified</span></span>

<span data-ttu-id="5de07-143">доменное имя (FQDN).</span><span class="sxs-lookup"><span data-stu-id="5de07-143">domain name (FQDN).</span></span> <span data-ttu-id="5de07-144">С помощью номера порта регистратора по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5de07-144">Using default Registrar port number.</span></span> <span data-ttu-id="5de07-145">Ошибка</span><span class="sxs-lookup"><span data-stu-id="5de07-145">Exception:</span></span>

<span data-ttu-id="5de07-146">System. InvalidOperationException: в топологии не обнаружены подходящие кластеры.</span><span class="sxs-lookup"><span data-stu-id="5de07-146">System.InvalidOperationException: No matching cluster found in topology.</span></span>

<span data-ttu-id="5de07-147">скорость</span><span class="sxs-lookup"><span data-stu-id="5de07-147">at</span></span>

<span data-ttu-id="5de07-148">Microsoft. RTC. Management. SyntheticTransactions. SipSyntheticTransaction. TryRetri</span><span class="sxs-lookup"><span data-stu-id="5de07-148">Microsoft.Rtc.Management.SyntheticTransactions.SipSyntheticTransaction.TryRetri</span></span>

<span data-ttu-id="5de07-149">eveRegistrarPortFromTopology (Int32& registrarPortNumber)</span><span class="sxs-lookup"><span data-stu-id="5de07-149">eveRegistrarPortFromTopology(Int32& registrarPortNumber)</span></span>

<span data-ttu-id="5de07-150">Test-CsUcwaConference: нет тестового пользователя, назначенного для</span><span class="sxs-lookup"><span data-stu-id="5de07-150">Test-CsUcwaConference : There is no test user assigned for</span></span>

<span data-ttu-id="5de07-151">\[LyncTest.SelfHost.Corp.Microsoft.com \] .</span><span class="sxs-lookup"><span data-stu-id="5de07-151">\[LyncTest.SelfHost.Corp.Microsoft.com\].</span></span> <span data-ttu-id="5de07-152">Проверка конфигурации тестового пользователя.</span><span class="sxs-lookup"><span data-stu-id="5de07-152">Verify test user configuration.</span></span>

<span data-ttu-id="5de07-153">В строке: 1 символ: 1</span><span class="sxs-lookup"><span data-stu-id="5de07-153">At line:1 char:1</span></span>

<span data-ttu-id="5de07-154">\+ Test-CsUcwaConference TargetFqdn "LyncTest.SelfHost.Corp.Microsoft.com"</span><span class="sxs-lookup"><span data-stu-id="5de07-154">\+ Test-CsUcwaConference -TargetFqdn "LyncTest.SelfHost.Corp.Microsoft.com"</span></span>

\+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

<span data-ttu-id="5de07-155">\+ CategoryInfo: ResourceUnavailable: (:) \[ Test-CsUcwaConference\]</span><span class="sxs-lookup"><span data-stu-id="5de07-155">\+ CategoryInfo : ResourceUnavailable: (:) \[Test-CsUcwaConference\]</span></span>

<span data-ttu-id="5de07-156">, InvalidOperationException</span><span class="sxs-lookup"><span data-stu-id="5de07-156">, InvalidOperationException</span></span>

<span data-ttu-id="5de07-157">\+ FullyQualifiedErrorId: NotFoundTestUsers, Microsoft. RTC. Management. синтезатор</span><span class="sxs-lookup"><span data-stu-id="5de07-157">\+ FullyQualifiedErrorId : NotFoundTestUsers,Microsoft.Rtc.Management.Synth</span></span>

<span data-ttu-id="5de07-158">eticTransactions.TestUcwaConferenceCmdlet</span><span class="sxs-lookup"><span data-stu-id="5de07-158">eticTransactions.TestUcwaConferenceCmdlet</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="5de07-159">Причины, по которым может произойти сбой теста</span><span class="sxs-lookup"><span data-stu-id="5de07-159">Reasons why the test might have failed</span></span>

<span data-ttu-id="5de07-160">Ниже приведены некоторые распространенные причины, по которым может произойти сбой **Test-CsUcwaConference** :</span><span class="sxs-lookup"><span data-stu-id="5de07-160">Here are some common reasons why **Test-CsUcwaConference** might fail:</span></span>

  - <span data-ttu-id="5de07-161">Предоставлено неправильное значение параметра.</span><span class="sxs-lookup"><span data-stu-id="5de07-161">An incorrect parameter value was supplied.</span></span> <span data-ttu-id="5de07-162">Если используется, необязательные параметры необходимо настроить правильно, или тест завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="5de07-162">If used, the optional parameters must be configured correctly or the test will fail.</span></span> <span data-ttu-id="5de07-163">Повторите выполнение команды без дополнительных параметров и проверьте, выполняется ли это успешно.</span><span class="sxs-lookup"><span data-stu-id="5de07-163">Rerun the command without the optional parameters and see whether that succeeds.</span></span>

  - <span data-ttu-id="5de07-164">Возможность проведения Конференции зависит от политики конференц-связи, назначенной пользователю, который организовал конференцию (в случае командлета **Test — CsUcwaConference** , который является отправителем).</span><span class="sxs-lookup"><span data-stu-id="5de07-164">The ability to conduct a conference depends on the conferencing policy that has been assigned to the user who organized the conference (in the case of the **Test-CsUcwaConference** cmdlet, that is the "sender").</span></span> <span data-ttu-id="5de07-165">Если организатор не может включать мероприятия для совместной работы на своем собрании (например, если у его политики Конференции задано значение false), командлет **Test-CsUcwaConference** завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="5de07-165">If the organizer is not allowed to include collaborative activities in his or her meeting (for example, if his or her conferencing policy has the EnableDataCollaboration property set to False) then the **Test-CsUcwaConference** cmdlet will fail.</span></span>

  - <span data-ttu-id="5de07-166">Эта команда завершается сбоем, если граничный сервер неправильно настроен или еще не развернут.</span><span class="sxs-lookup"><span data-stu-id="5de07-166">This command will fail if the Edge Server is misconfigured or not yet deployed.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="5de07-167">См. также</span><span class="sxs-lookup"><span data-stu-id="5de07-167">See Also</span></span>


[<span data-ttu-id="5de07-168">Test-CsASConference</span><span class="sxs-lookup"><span data-stu-id="5de07-168">Test-CsASConference</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsASConference)  
[<span data-ttu-id="5de07-169">Test-CsDataConference</span><span class="sxs-lookup"><span data-stu-id="5de07-169">Test-CsDataConference</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsDataConference)  
[<span data-ttu-id="5de07-170">Test-CsAVConference</span><span class="sxs-lookup"><span data-stu-id="5de07-170">Test-CsAVConference</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsAVConference)  
  

<span data-ttu-id="5de07-171"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5de07-171"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

