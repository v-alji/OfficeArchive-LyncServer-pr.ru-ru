---
title: 'Lync Server 2013: Проверка аудио-и видеоконференций'
description: 'Lync Server 2013: Проверка аудио-и видеоконференций.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Validating audio/video conferences
ms:assetid: 6c8c422a-d501-42cb-820b-b002f9b2250b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720915(v=OCS.15)
ms:contentKeyID: 63969615
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ad12611e928a64b934252ec21c18b98366e0912b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443491"
---
# <a name="validating-audiovideo-conferences-in-lync-server-2013"></a><span data-ttu-id="981c2-103">Проверка аудио-и видеоконференций в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="981c2-103">Validating audio/video conferences in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="981c2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="981c2-104">

<span> </span></span></span>

<span data-ttu-id="981c2-105">_**Тема последнего изменения:** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="981c2-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="981c2-106">Расписание проверки</span><span class="sxs-lookup"><span data-stu-id="981c2-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="981c2-107">Ежедневно</span><span class="sxs-lookup"><span data-stu-id="981c2-107">Daily</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="981c2-108">Средство тестирования</span><span class="sxs-lookup"><span data-stu-id="981c2-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="981c2-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="981c2-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="981c2-110">Требуемые разрешения</span><span class="sxs-lookup"><span data-stu-id="981c2-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="981c2-111">При локальном запуске с помощью командной консоли Lync Server пользователи должны быть членами группы безопасности RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="981c2-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="981c2-112">При запуске с помощью удаленного экземпляра Windows PowerShell пользователям должна быть назначена роль RBAC, имеющая разрешение на запуск командлета Test-CsAVConference.</span><span class="sxs-lookup"><span data-stu-id="981c2-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsAVConference cmdlet.</span></span> <span data-ttu-id="981c2-113">Чтобы просмотреть список всех ролей RBAC, которые могут использовать этот командлет, выполните в командной строке Windows PowerShell следующую команду:</span><span class="sxs-lookup"><span data-stu-id="981c2-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsAVConference&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="981c2-114">Описание</span><span class="sxs-lookup"><span data-stu-id="981c2-114">Description</span></span>

<span data-ttu-id="981c2-115">Командлет Test-CsAVConference проверяет, могут ли два тестовых пользователя участвовать в аудио-или видеоконференции (A/V).</span><span class="sxs-lookup"><span data-stu-id="981c2-115">The Test-CsAVConference cmdlet checks whether two test users can participate in an audio/video (A/V) conference.</span></span> <span data-ttu-id="981c2-116">При запуске командлета два пользователя вошли в систему.</span><span class="sxs-lookup"><span data-stu-id="981c2-116">When the cmdlet runs, the two users are logged on to the system.</span></span> <span data-ttu-id="981c2-117">После того как они будут успешно вошли в систему, первый пользователь создаст Конференц-связь, а затем ждет, пока второй пользователь присоединится к этой Конференции.</span><span class="sxs-lookup"><span data-stu-id="981c2-117">After they face successfully logged on, the first user creates an A/V conference, and then waits for the second user to join that conference.</span></span> <span data-ttu-id="981c2-118">После краткого обмена данными Конференция удаляется, а два теста пользователя выводятся из сеанса.</span><span class="sxs-lookup"><span data-stu-id="981c2-118">After a brief exchange of data, the conference is deleted and the two tests users are logged off.</span></span>

<span data-ttu-id="981c2-119">Обратите внимание, что Test-CsAVConference не выполняет фактическую конференцию/V-связь между двумя тестовыми пользователями.</span><span class="sxs-lookup"><span data-stu-id="981c2-119">Note that Test-CsAVConference does not conduct an actual A/V conference between the two test users.</span></span> <span data-ttu-id="981c2-120">Вместо этого командлет проверяет, что два пользователя могут выполнять все необходимые подключения для проведения такой конференции.</span><span class="sxs-lookup"><span data-stu-id="981c2-120">Instead, the cmdlet verifies that the two users can make all the connections necessary to conduct such a conference.</span></span>

<span data-ttu-id="981c2-121">Дополнительные примеры для этой команды можно найти на странице [Test-CsAVConference](https://docs.microsoft.com/powershell/module/skype/Test-CsAVConference).</span><span class="sxs-lookup"><span data-stu-id="981c2-121">Further examples for this command can be found at [Test-CsAVConference](https://docs.microsoft.com/powershell/module/skype/Test-CsAVConference).</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="981c2-122">Выполнение теста</span><span class="sxs-lookup"><span data-stu-id="981c2-122">Running the test</span></span>

<span data-ttu-id="981c2-123">Командлет Test-CsAVConference можно выполнить с помощью пары предварительно настроенных тестовых учетных записей (см. раздел Настройка тестовых учетных записей для выполнения тестов Lync Server) или учетные записи любых двух пользователей, которые включены в Lync Server.</span><span class="sxs-lookup"><span data-stu-id="981c2-123">The Test-CsAVConference cmdlet can be run using either a pair of preconfigured test accounts (see Setting Up Test Accounts for Running Lync Server Tests) or the accounts of any two users who are enabled for Lync Server.</span></span> <span data-ttu-id="981c2-124">Для выполнения этой проверки с помощью тестовых учетных записей нужно просто указать полное доменное имя для тестируемого пула Lync Server.</span><span class="sxs-lookup"><span data-stu-id="981c2-124">To run this check using test accounts, you just have to specify the FQDN of the Lync Server pool being tested.</span></span> <span data-ttu-id="981c2-125">Например:</span><span class="sxs-lookup"><span data-stu-id="981c2-125">For example:</span></span>

    Test-CsAVConference -TargetFqdn "atl-cs-001.litwareinc.com"

<span data-ttu-id="981c2-126">Для выполнения этой проверки с использованием фактических учетных записей пользователей необходимо создать два объекта учетных данных Windows PowerShell (объекты, содержащие имя и пароль учетной записи) для каждой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="981c2-126">To run this check using actual user accounts, you must create two Windows PowerShell credentials objects (objects that contain the account name and password) for each account.</span></span> <span data-ttu-id="981c2-127">После этого вы должны добавить эти объекты учетных данных и адреса SIP для двух учетных записей при вызове Test-CsAVConference:</span><span class="sxs-lookup"><span data-stu-id="981c2-127">You must then include those credentials objects and the SIP addresses of the two accounts when they call Test-CsAVConference:</span></span>

    $credential1 = Get-Credential "litwareinc\kenmyer"
    $credential2 = Get-Credential "litwareinc\davidlongmire"
    Test-CsAVConference -TargetFqdn "atl-cs-001.litwareinc.com" -SenderSipAddress "sip:kenmyer@litwareinc.com" -SenderCredential $credential1 -ReceiverSipAddress "sip:davidlongmire@litwareinc.com" -ReceiverCredential $credential2

<span data-ttu-id="981c2-128">Дополнительные сведения можно найти в справочной документации по командлету [Test-CsAVConference](https://docs.microsoft.com/powershell/module/skype/Test-CsAVConference) .</span><span class="sxs-lookup"><span data-stu-id="981c2-128">For more information, see the Help documentation for the [Test-CsAVConference](https://docs.microsoft.com/powershell/module/skype/Test-CsAVConference) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="981c2-129">Определение успеха или сбоя</span><span class="sxs-lookup"><span data-stu-id="981c2-129">Determining Success or Failure</span></span>

<span data-ttu-id="981c2-130">Если указанные пользователи могут успешно выполнить Конференц-связь между собой, вы получите вывод примерно так, чтобы свойство Result пометило **"успешно".**</span><span class="sxs-lookup"><span data-stu-id="981c2-130">If the specified users can successfully complete an A/V conference, you'll receive output similar to this, with the Result property marked as **Success:**</span></span>

<span data-ttu-id="981c2-131">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="981c2-131">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="981c2-132">Результат: успех</span><span class="sxs-lookup"><span data-stu-id="981c2-132">Result : Success</span></span>

<span data-ttu-id="981c2-133">Задержка: 00:00:02.6841765</span><span class="sxs-lookup"><span data-stu-id="981c2-133">Latency : 00:00:02.6841765</span></span>

<span data-ttu-id="981c2-134">Ошибки</span><span class="sxs-lookup"><span data-stu-id="981c2-134">Error :</span></span>

<span data-ttu-id="981c2-135">Диагностик</span><span class="sxs-lookup"><span data-stu-id="981c2-135">Diagnosis :</span></span>

<span data-ttu-id="981c2-136">Если пользователи не могут выполнить конференцию, результат будет отображаться как сбой, а дополнительные сведения будут записаны в свойствах Error и диагноз.</span><span class="sxs-lookup"><span data-stu-id="981c2-136">If the users can not complete the conference, then the Result will be shown as Failure, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="981c2-137">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="981c2-137">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="981c2-138">Результат: сбой</span><span class="sxs-lookup"><span data-stu-id="981c2-138">Result : Failure</span></span>

<span data-ttu-id="981c2-139">Задержка: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="981c2-139">Latency : 00:00:00</span></span>

<span data-ttu-id="981c2-140">Ошибка: 404, не найдена</span><span class="sxs-lookup"><span data-stu-id="981c2-140">Error : 404, Not Found</span></span>

<span data-ttu-id="981c2-141">Диагностика: ErrorCode = 4005, Source = ATL-CS-001.litwareinc.com,</span><span class="sxs-lookup"><span data-stu-id="981c2-141">Diagnosis : ErrorCode=4005,Source=atl-cs-001.litwareinc.com,</span></span>

<span data-ttu-id="981c2-142">Reason = универсальный код ресурса (URI) назначения не включен для SIP либо не</span><span class="sxs-lookup"><span data-stu-id="981c2-142">Reason=Destination URI either not enabled for SIP or does not</span></span>

<span data-ttu-id="981c2-143">Существует.</span><span class="sxs-lookup"><span data-stu-id="981c2-143">exist.</span></span>

<span data-ttu-id="981c2-144">Microsoft. RTC. SignalR. DiagnosticHeader</span><span class="sxs-lookup"><span data-stu-id="981c2-144">Microsoft.Rtc.Signaling.DiagnosticHeader</span></span>

<span data-ttu-id="981c2-145">Например, предыдущее выходное состояние не прошло проверку, так как по крайней мере одна из двух учетных записей пользователей была недействительной из-за того, что учетная запись не существует или учетная запись не включена для Lync Server.</span><span class="sxs-lookup"><span data-stu-id="981c2-145">For example, the previous output states that the test failed because at least one of the two user accounts was not valid, either because the account does not exist or because the account has not been enabled for Lync Server.</span></span> <span data-ttu-id="981c2-146">Для проверки существования двух тестовых учетных записей и того, включены ли они в Lync Server, можно выполнить следующую команду:</span><span class="sxs-lookup"><span data-stu-id="981c2-146">You can verify the existence of the two test accounts, and whether they were enabled for Lync Server, by running a command similar to the following:</span></span>

    "sip:kenmyer@litwareinc.com","sip:davidlongmire@litwareinc.com" | Get-CsUser | Select-Object SipAddress, enabled

<span data-ttu-id="981c2-147">Если Test-CsAVConference не удается, возможно, потребуется повторно выполнить тест, на этот раз включая параметр подробно:</span><span class="sxs-lookup"><span data-stu-id="981c2-147">If Test-CsAVConference fails, then you might want to rerun the test, this time including the Verbose parameter:</span></span>

    Test-CsAVConference -TargetFqdn "atl-cs-001.litwareinc.com" -Verbose

<span data-ttu-id="981c2-148">При включенном параметре подробных данных Test-CsAVConference будет возвращать пошаговые учетные записи для каждого действия, которое оно предпринимало, когда вы проверили возможность участия указанных пользователей на Конференции AV.</span><span class="sxs-lookup"><span data-stu-id="981c2-148">When the Verbose parameter is included Test-CsAVConference will return a step-by-step account of each action it tried when it checked the ability of the specified users to participate in an AV conference.</span></span> <span data-ttu-id="981c2-149">Например, предположим, что тест завершается сбоем и вы получаете следующую диагностику.</span><span class="sxs-lookup"><span data-stu-id="981c2-149">For example, suppose that your test fails and you receive the following Diagnosis:</span></span>

<span data-ttu-id="981c2-150">ErrorCode = 1008, Source = accessproxy. плана litwareinc. com, причина — не удалось разрешить DNS-запись SRV</span><span class="sxs-lookup"><span data-stu-id="981c2-150">ErrorCode=1008,Source=accessproxy.litwareinc.com,Reason=Unable to resolve DNS SRV record</span></span>

<span data-ttu-id="981c2-151">При повторном выполнении теста с помощью параметра подробных данных пошаговые инструкции будут возвращены следующим образом:</span><span class="sxs-lookup"><span data-stu-id="981c2-151">If you rerun the test using the Verbose parameter, the step-by-step information returned will include output similar to this:</span></span>

<span data-ttu-id="981c2-152">ПОДРОБНЫЕ сведения: начато действие "регистрация".</span><span class="sxs-lookup"><span data-stu-id="981c2-152">VERBOSE: 'Register' activity started.</span></span>

<span data-ttu-id="981c2-153">Отправка запроса на регистрацию:</span><span class="sxs-lookup"><span data-stu-id="981c2-153">Sending Registration request:</span></span>

<span data-ttu-id="981c2-154">Целевое полное доменное имя = atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="981c2-154">Target Fqdn = atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="981c2-155">SIP адрес пользователя = sip:davidlongmire@litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="981c2-155">User Sip Address = sip:davidlongmire@litwareinc.com</span></span>

<span data-ttu-id="981c2-156">Порт регистратора = 5061.</span><span class="sxs-lookup"><span data-stu-id="981c2-156">Registrar Port = 5061.</span></span>

<span data-ttu-id="981c2-157">Выбран тип проверки подлинности "Trusted".</span><span class="sxs-lookup"><span data-stu-id="981c2-157">Auth Type 'Trusted' is selected.</span></span>

<span data-ttu-id="981c2-158">Начато действие "регистрация".</span><span class="sxs-lookup"><span data-stu-id="981c2-158">'Register' activity started.</span></span>

<span data-ttu-id="981c2-159">Отправка запроса на регистрацию:</span><span class="sxs-lookup"><span data-stu-id="981c2-159">Sending Registration request:</span></span>

<span data-ttu-id="981c2-160">Целевое полное доменное имя = atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="981c2-160">Target Fqdn = atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="981c2-161">SIP адрес пользователя = sip:kenmyer@litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="981c2-161">User Sip Address = sip:kenmyer@litwareinc.com</span></span>

<span data-ttu-id="981c2-162">Порт регистратора = 5061.</span><span class="sxs-lookup"><span data-stu-id="981c2-162">Registrar Port = 5061.</span></span>

<span data-ttu-id="981c2-163">Выбран тип проверки подлинности "Trusted".</span><span class="sxs-lookup"><span data-stu-id="981c2-163">Auth Type 'Trusted' is selected.</span></span>

<span data-ttu-id="981c2-164">Исключение "не удалось зарегистрировать конечную точку".</span><span class="sxs-lookup"><span data-stu-id="981c2-164">An exception 'The endpoint was unable to register.</span></span> <span data-ttu-id="981c2-165">Ознакомьтесь с ErrorCode по конкретной причине.</span><span class="sxs-lookup"><span data-stu-id="981c2-165">See the ErrorCode for specific reason.'</span></span> <span data-ttu-id="981c2-166">произошла ошибка в рабочем процессе</span><span class="sxs-lookup"><span data-stu-id="981c2-166">occurred during Workflow</span></span>

<span data-ttu-id="981c2-167">Последняя строка в этом выходных данных указывает на то, что пользователь sip:kenmyer@litwareinc.com не смог зарегистрироваться в Lync Server.</span><span class="sxs-lookup"><span data-stu-id="981c2-167">The last line in that output indicates that the user sip:kenmyer@litwareinc.com was unable to register with Lync Server.</span></span> <span data-ttu-id="981c2-168">Это означает, что необходимо убедиться в том, что адрес SIP sip:kenmyer@litwareinc.com действителен и что связанный пользователь включен для Lync Server.</span><span class="sxs-lookup"><span data-stu-id="981c2-168">That means that you should verify that the SIP address sip:kenmyer@litwareinc.com is valid, and that the associated user is enabled for Lync Server.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="981c2-169">Причины, по которым может произойти сбой теста</span><span class="sxs-lookup"><span data-stu-id="981c2-169">Reasons why the test might have failed</span></span>

<span data-ttu-id="981c2-170">Ниже приведены некоторые распространенные причины, по которым может произойти сбой Test-CsAVConference.</span><span class="sxs-lookup"><span data-stu-id="981c2-170">Here are some common reasons why Test-CsAVConference might fail:</span></span>

  - <span data-ttu-id="981c2-171">Указана недействительная учетная запись пользователя.</span><span class="sxs-lookup"><span data-stu-id="981c2-171">You specified a user account that is not valid.</span></span> <span data-ttu-id="981c2-172">Для проверки существования учетной записи пользователя можно выполнить следующую команду:</span><span class="sxs-lookup"><span data-stu-id="981c2-172">You can verify that a user account exists by running a command similar to this:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com"

  - <span data-ttu-id="981c2-173">Учетная запись пользователя верна, но в настоящее время учетная запись не включена для Lync Server.</span><span class="sxs-lookup"><span data-stu-id="981c2-173">The user account is valid, but the account is currently not enabled for Lync Server.</span></span> <span data-ttu-id="981c2-174">Чтобы убедиться в том, что учетная запись пользователя включена для Lync Server, выполните команду, подобную следующей:</span><span class="sxs-lookup"><span data-stu-id="981c2-174">To verify that a user account is enabled for Lync Server, run a command similar to the following:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object Enabled
    
    <span data-ttu-id="981c2-175">Если для свойства Enabled задано значение false, это означает, что пользователь в настоящее время не поддерживает Lync Server.</span><span class="sxs-lookup"><span data-stu-id="981c2-175">If the Enabled property is set to False that means that the user is currently not enabled for Lync Server.</span></span>

<span data-ttu-id="981c2-176"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="981c2-176"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

