---
title: 'Lync Server 2013: Проверка одноранговых аудио-и видеозвонков'
description: 'Lync Server 2013: Проверка одноранговой голосовой и видеосвязи в одноранговых режимах.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing peer to peer audio/video call
ms:assetid: 95eb3693-b866-4652-bc45-9b75fdb40b49
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn743835(v=OCS.15)
ms:contentKeyID: 63969627
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 03bab69d926a99c091a510ce64b78dbf505d4cbc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439816"
---
# <a name="testing-peer-to-peer-audiovideo-call-in-lync-server-2013"></a><span data-ttu-id="f5525-103">Проверка одноранговых аудио-и видеозвонков в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f5525-103">Testing peer to peer audio/video call in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f5525-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f5525-104">

<span> </span></span></span>

<span data-ttu-id="f5525-105">_**Тема последнего изменения:** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="f5525-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f5525-106">Расписание проверки</span><span class="sxs-lookup"><span data-stu-id="f5525-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="f5525-107">Ежедневно</span><span class="sxs-lookup"><span data-stu-id="f5525-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5525-108">Средство тестирования</span><span class="sxs-lookup"><span data-stu-id="f5525-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="f5525-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="f5525-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5525-110">Требуемые разрешения</span><span class="sxs-lookup"><span data-stu-id="f5525-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="f5525-111">При локальном запуске с помощью командной консоли Lync Server пользователи должны быть членами группы безопасности RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="f5525-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="f5525-112">При запуске с помощью удаленного экземпляра Windows PowerShell пользователям должна быть назначена роль RBAC, имеющая разрешение на запуск командлета Test-CsP2PAV.</span><span class="sxs-lookup"><span data-stu-id="f5525-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsP2PAV cmdlet.</span></span> <span data-ttu-id="f5525-113">Чтобы просмотреть список всех ролей RBAC, которые могут использовать этот командлет, выполните в командной строке Windows PowerShell следующую команду:</span><span class="sxs-lookup"><span data-stu-id="f5525-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsP2PAV&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="f5525-114">Описание</span><span class="sxs-lookup"><span data-stu-id="f5525-114">Description</span></span>

<span data-ttu-id="f5525-115">Test-CsP2PAV используется, чтобы определить, могут ли пользователи, входящие в одноранговую беседу, использовать пару тестовых пользователей.</span><span class="sxs-lookup"><span data-stu-id="f5525-115">Test-CsP2PAV is used to determine whether a pair of test users can participate in a peer-to-peer A/V conversation.</span></span> <span data-ttu-id="f5525-116">Чтобы протестировать этот сценарий, командлет запускается путем записи двух пользователей на сервер Lync Server.</span><span class="sxs-lookup"><span data-stu-id="f5525-116">To test this scenario, the cmdlet starts off by logging on the two users to Lync Server.</span></span> <span data-ttu-id="f5525-117">Предполагается, что два входа выполняются успешно, первый пользователь затем приглашает второго пользователя присоединиться к вызову A/V.</span><span class="sxs-lookup"><span data-stu-id="f5525-117">Assuming that the two logons succeed, the first user then invites the second user to join an A/V call.</span></span> <span data-ttu-id="f5525-118">Второй пользователь принимает звонок, проверяет соединение между двумя пользователями, после чего звонок завершается, и тестовые пользователи вышли из системы.</span><span class="sxs-lookup"><span data-stu-id="f5525-118">The second user accepts the call, the connection between the two users is tested, and then the call is ended and the test users are logged off from the system.</span></span>

<span data-ttu-id="f5525-119">Test-CsP2PAV на самом деле вызов функции A/V не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f5525-119">Test-CsP2PAV does not actually conduct an A/V call.</span></span> <span data-ttu-id="f5525-120">Данные мультимедиа не передаются между тестовыми пользователями.</span><span class="sxs-lookup"><span data-stu-id="f5525-120">Multimedia information is not exchanged between the test users.</span></span> <span data-ttu-id="f5525-121">Вместо этого командлет проверяет, могут ли быть выполнены соответствующие подключения, и что эти пользователи могут выполнить такой вызов.</span><span class="sxs-lookup"><span data-stu-id="f5525-121">Instead, the cmdlet merely verifies that the appropriate connections can be made and that the two users can conduct such a call.</span></span>

<span data-ttu-id="f5525-122">Дополнительные сведения можно найти в справочной документации по командлету [Test-CsP2PAV](https://docs.microsoft.com/powershell/module/skype/Test-CsP2PAV) .</span><span class="sxs-lookup"><span data-stu-id="f5525-122">For more information, see the Help documentation for the [Test-CsP2PAV](https://docs.microsoft.com/powershell/module/skype/Test-CsP2PAV) cmdlet.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="f5525-123">Выполнение теста</span><span class="sxs-lookup"><span data-stu-id="f5525-123">Running the test</span></span>

<span data-ttu-id="f5525-124">Командлет Test-CsP2PAV можно выполнить с помощью пары предварительно настроенных тестовых учетных записей (см. раздел Настройка тестовых учетных записей для выполнения тестов Lync Server) или учетные записи любых двух пользователей, которые включены в Lync Server.</span><span class="sxs-lookup"><span data-stu-id="f5525-124">The Test-CsP2PAV cmdlet can be run using either a pair of preconfigured test accounts (see Setting Up Test Accounts for Running Lync Server Tests) or the accounts of any two users who are enabled for Lync Server.</span></span> <span data-ttu-id="f5525-125">Для выполнения этой проверки с помощью тестовых учетных записей нужно просто указать полное доменное имя для тестируемого пула Lync Server.</span><span class="sxs-lookup"><span data-stu-id="f5525-125">To run this check using test accounts, you just have to specify the FQDN of the Lync Server pool being tested.</span></span> <span data-ttu-id="f5525-126">Например:</span><span class="sxs-lookup"><span data-stu-id="f5525-126">For example:</span></span>

    Test-CsP2PAV -TargetFqdn "atl-cs-001.litwareinc.com"

<span data-ttu-id="f5525-127">Для выполнения этой проверки с использованием фактических учетных записей пользователей необходимо создать два объекта учетных данных Lync Server (объекты, содержащие имя и пароль учетной записи) для каждой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="f5525-127">To run this check using actual user accounts, you must create two Lync Server credentials objects (objects that contain the account name and password) for each account.</span></span> <span data-ttu-id="f5525-128">После вызова Test-CsP2PAV вы должны добавить эти объекты учетных данных и адреса SIP для двух учетных записей.</span><span class="sxs-lookup"><span data-stu-id="f5525-128">You must then include those credentials objects and the SIP addresses of the two accounts when you call Test-CsP2PAV:</span></span>

    $credential1 = Get-Credential "litwareinc\kenmyer"
    $credential2 = Get-Credential "litwareinc\davidlongmire"
    Test-CsP2PAV -TargetFqdn "atl-cs-001.litwareinc.com" -SenderSipAddress "sip:kenmyer@litwareinc.com" -SenderCredential $credential1 -ReceiverSipAddress "sip:davidlongmire@litwareinc.com" -ReceiverCredential $credential2

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="f5525-129">Определение успеха или сбоя</span><span class="sxs-lookup"><span data-stu-id="f5525-129">Determining success or failure</span></span>

<span data-ttu-id="f5525-130">Если два тестовых пользователя могут выполнить одноранговый вызов A/V, вы получите вывод примерно так, чтобы свойство Result пометило **"успешно".**</span><span class="sxs-lookup"><span data-stu-id="f5525-130">If the two test users can complete a peer-to-peer A/V call, then you'll receive output similar to this with the Result property marked as **Success:**</span></span>

<span data-ttu-id="f5525-131">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="f5525-131">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="f5525-132">Результат: успех</span><span class="sxs-lookup"><span data-stu-id="f5525-132">Result : Success</span></span>

<span data-ttu-id="f5525-133">Задержка: 00:00:06.8630376</span><span class="sxs-lookup"><span data-stu-id="f5525-133">Latency : 00:00:06.8630376</span></span>

<span data-ttu-id="f5525-134">Ошибки</span><span class="sxs-lookup"><span data-stu-id="f5525-134">Error :</span></span>

<span data-ttu-id="f5525-135">Диагностик</span><span class="sxs-lookup"><span data-stu-id="f5525-135">Diagnosis :</span></span>

<span data-ttu-id="f5525-136">Если тестовые пользователи не могут завершить звонок, результат будет показан как сбой, а дополнительные сведения будут записаны в свойствах Error и диагноз.</span><span class="sxs-lookup"><span data-stu-id="f5525-136">If the test users can't complete the call, then the Result will be shown as Failure, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="f5525-137">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="f5525-137">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="f5525-138">Результат: сбой</span><span class="sxs-lookup"><span data-stu-id="f5525-138">Result : Failure</span></span>

<span data-ttu-id="f5525-139">Задержка: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="f5525-139">Latency : 00:00:00</span></span>

<span data-ttu-id="f5525-140">Ошибка: 480, временно недоступна</span><span class="sxs-lookup"><span data-stu-id="f5525-140">Error : 480, Temporarily Unavailable</span></span>

<span data-ttu-id="f5525-141">Диагностика: ErrorCode = 15030, Source = ATL-CS-001. плана litwareinc. com, Reason = Failed</span><span class="sxs-lookup"><span data-stu-id="f5525-141">Diagnosis : ErrorCode=15030,Source=atl-cs-001.litwareinc.com,Reason=Failed</span></span>

<span data-ttu-id="f5525-142">чтобы перенаправить на сервер Exchange Server</span><span class="sxs-lookup"><span data-stu-id="f5525-142">to route to Exchange Server</span></span>

<span data-ttu-id="f5525-143">Microsoft. RTC. SignalR. DiagnosticHeader</span><span class="sxs-lookup"><span data-stu-id="f5525-143">Microsoft.Rtc.Signaling.DiagnosticHeader</span></span>

<span data-ttu-id="f5525-144">Например, в предыдущем выводе говорится о том, что тест завершился сбоем, так как не удалось связаться с сервером Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="f5525-144">For example, the previous output states that the test failed because the Microsoft Exchange Server couldn't be contacted.</span></span> <span data-ttu-id="f5525-145">Это сообщение об ошибке обычно указывает на проблему с настройкой единой системы обмена сообщениями Exchange.</span><span class="sxs-lookup"><span data-stu-id="f5525-145">This error message typically indicates a problem the configuration of Exchange Unified Messaging.</span></span>

<span data-ttu-id="f5525-146">Если Test-CsP2PAV не удается, возможно, потребуется повторно выполнить тест, на этот раз включая параметр подробно:</span><span class="sxs-lookup"><span data-stu-id="f5525-146">If Test-CsP2PAV fails then you might want to rerun the test, this time including the Verbose parameter:</span></span>

<span data-ttu-id="f5525-147">Test-CsP2PAV TargetFqdn "atl-cs-001.litwareinc.com" — подробный</span><span class="sxs-lookup"><span data-stu-id="f5525-147">Test-CsP2PAV -TargetFqdn "atl-cs-001.litwareinc.com" -Verbose</span></span>

<span data-ttu-id="f5525-148">После включения подробной информации Test-CsP2PAV будет возвращать пошаговые инструкции по выполнению всех действий, выполняемых указанным пользователем при входе на сервер Lync Server.</span><span class="sxs-lookup"><span data-stu-id="f5525-148">When the Verbose parameter is included, Test-CsP2PAV will return a step-by-step account of each action it tried as it checked the ability of the specified user to log on to Lync Server.</span></span> <span data-ttu-id="f5525-149">Например, предположим, что тест завершился со следующей диагностикой.</span><span class="sxs-lookup"><span data-stu-id="f5525-149">For example, suppose that your test failed with the following Diagnosis:</span></span>

<span data-ttu-id="f5525-150">ErrorCode = 6003, Source = ATL-CS-001. плана litwareinc. com, причина = не поддерживается запрос диалогового окна</span><span class="sxs-lookup"><span data-stu-id="f5525-150">ErrorCode=6003,Source=atl-cs-001.litwareinc.com,Reason=Unsupported out of dialog request</span></span>

<span data-ttu-id="f5525-151">Если вы снова запустите Test-CsP2PAV и включите параметр Verbose, вы получите вывод примерно так:</span><span class="sxs-lookup"><span data-stu-id="f5525-151">If you rerun Test-CsP2PAV and include the Verbose parameter, you'll get output similar to this:</span></span>

<span data-ttu-id="f5525-152">ПОДРОБНЫЕ сведения: начато действие "регистрация".</span><span class="sxs-lookup"><span data-stu-id="f5525-152">VERBOSE: 'Register' activity started.</span></span>

<span data-ttu-id="f5525-153">Отправка запроса на регистрацию:</span><span class="sxs-lookup"><span data-stu-id="f5525-153">Sending Registration request:</span></span>

<span data-ttu-id="f5525-154">Целевое полное доменное имя = atl-cs-011.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="f5525-154">Target Fqdn = atl-cs-011.litwareinc.com</span></span>

<span data-ttu-id="f5525-155">SIP адрес пользователя = sip:kenmyer@litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="f5525-155">User Sip Address = sip:kenmyer@litwareinc.com</span></span>

<span data-ttu-id="f5525-156">Порт регистратора = 5062.</span><span class="sxs-lookup"><span data-stu-id="f5525-156">Registrar Port = 5062.</span></span>

<span data-ttu-id="f5525-157">Выбран тип проверки подлинности "IWA".</span><span class="sxs-lookup"><span data-stu-id="f5525-157">Auth Type 'IWA' is selected.</span></span>

<span data-ttu-id="f5525-158">Исключение "не удалось зарегистрировать конечную точку".</span><span class="sxs-lookup"><span data-stu-id="f5525-158">An exception 'The endpoint was unable to register.</span></span> <span data-ttu-id="f5525-159">Ознакомьтесь с ErrorCode по конкретной причине.</span><span class="sxs-lookup"><span data-stu-id="f5525-159">See the ErrorCode for specific reason.'</span></span> <span data-ttu-id="f5525-160">произошла ошибка во время выполнения рабочего процесса Microsoft. RTC. SyntheticTransactions. Workflows. STP2PAVWorkflow.</span><span class="sxs-lookup"><span data-stu-id="f5525-160">occurred during workflow Microsoft.Rtc.SyntheticTransactions.Workflows.STP2PAVWorkflow execution.</span></span>

<span data-ttu-id="f5525-161">Несмотря на то, что в результате проверки результатов может быть непросто, вы увидите, что указан неверный порт регистратора (порт 5062).</span><span class="sxs-lookup"><span data-stu-id="f5525-161">Although it might not be immediately obvious, if you examine the output carefully you’ll see that an incorrect Registrar port (port 5062) was specified.</span></span> <span data-ttu-id="f5525-162">В свою очередь, это привело к сбою теста.</span><span class="sxs-lookup"><span data-stu-id="f5525-162">In turn, that caused the test to fail.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="f5525-163">Причины, по которым может произойти сбой теста</span><span class="sxs-lookup"><span data-stu-id="f5525-163">Reasons why the test might have failed</span></span>

<span data-ttu-id="f5525-164">Ниже приведены некоторые распространенные причины, по которым может произойти сбой Test-CsP2PAV.</span><span class="sxs-lookup"><span data-stu-id="f5525-164">Here are some common reasons why Test-CsP2PAV might fail:</span></span>

  - <span data-ttu-id="f5525-165">Указана недействительная учетная запись пользователя.</span><span class="sxs-lookup"><span data-stu-id="f5525-165">You specified a user account that is not valid.</span></span> <span data-ttu-id="f5525-166">Для проверки существования учетной записи пользователя можно выполнить следующую команду:</span><span class="sxs-lookup"><span data-stu-id="f5525-166">You can verify that a user account exists by running a command similar to this:</span></span>
    
    <span data-ttu-id="f5525-167">Get-CsUser "sip:kenmyer@litwareinc.com"</span><span class="sxs-lookup"><span data-stu-id="f5525-167">Get-CsUser "sip:kenmyer@litwareinc.com"</span></span>

  - <span data-ttu-id="f5525-168">Учетная запись пользователя верна, но в настоящее время учетная запись не включена для Lync Server.</span><span class="sxs-lookup"><span data-stu-id="f5525-168">The user account is valid, but the account is currently not enabled for Lync Server.</span></span> <span data-ttu-id="f5525-169">Чтобы убедиться в том, что учетная запись пользователя включена для Lync Server, выполните команду, подобную следующей:</span><span class="sxs-lookup"><span data-stu-id="f5525-169">To verify that a user account is enabled for Lync Server, run a command similar to the following:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object Enabled
    
    <span data-ttu-id="f5525-170">Если для свойства Enabled задано значение false, это означает, что пользователь в настоящее время не поддерживает Lync Server.</span><span class="sxs-lookup"><span data-stu-id="f5525-170">If the Enabled property is set to False, that means that the user is currently not enabled for Lync Server.</span></span>

<span data-ttu-id="f5525-171"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f5525-171"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

