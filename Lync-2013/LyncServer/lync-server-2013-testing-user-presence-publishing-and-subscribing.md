---
title: 'Lync Server 2013: Проверка публикации и подписки на присутствие пользователей'
description: 'Lync Server 2013: Проверка публикации и подписки на присутствие пользователей.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing user presence publishing and subscribing
ms:assetid: 27694c71-8e63-4aa4-b49f-fa06ccb81949
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn743832(v=OCS.15)
ms:contentKeyID: 63969587
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 90913f270fbd034ca4d2ea7cf3b93c255fc95c66
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439716"
---
# <a name="testing-user-presence-publishing-and-subscribing-in-lync-server-2013"></a><span data-ttu-id="e4d91-103">Проверка публикации и подписки на присутствие пользователей в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e4d91-103">Testing user presence publishing and subscribing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e4d91-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e4d91-104">

<span> </span></span></span>

<span data-ttu-id="e4d91-105">_**Тема последнего изменения:** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="e4d91-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e4d91-106">Расписание проверки</span><span class="sxs-lookup"><span data-stu-id="e4d91-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="e4d91-107">Ежедневно</span><span class="sxs-lookup"><span data-stu-id="e4d91-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4d91-108">Средство тестирования</span><span class="sxs-lookup"><span data-stu-id="e4d91-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="e4d91-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="e4d91-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4d91-110">Требуемые разрешения</span><span class="sxs-lookup"><span data-stu-id="e4d91-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="e4d91-111">При локальном запуске с помощью командной консоли Lync Server пользователи должны быть членами группы безопасности RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="e4d91-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="e4d91-112">При запуске с помощью удаленного экземпляра Windows PowerShell пользователям должна быть назначена роль RBAC, имеющая разрешение на запуск командлета Test-CsPresence.</span><span class="sxs-lookup"><span data-stu-id="e4d91-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsPresence cmdlet.</span></span> <span data-ttu-id="e4d91-113">Чтобы просмотреть список всех ролей RBAC, которые могут использовать этот командлет, выполните в командной строке Windows PowerShell следующую команду:</span><span class="sxs-lookup"><span data-stu-id="e4d91-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsPresence&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="e4d91-114">Описание</span><span class="sxs-lookup"><span data-stu-id="e4d91-114">Description</span></span>

<span data-ttu-id="e4d91-115">Test-CsPresence используется, чтобы определить, может ли пользовательская учетная запись входить на сервер Lync, а затем обмениваться сведениями о присутствии.</span><span class="sxs-lookup"><span data-stu-id="e4d91-115">Test-CsPresence is used to determine whether a pair of test users can log on to Lync Server and then exchange presence information.</span></span> <span data-ttu-id="e4d91-116">Для этого командлет сначала заносит в нее двух пользователей в систему.</span><span class="sxs-lookup"><span data-stu-id="e4d91-116">To do this, the cmdlet first logs the two users on to the system.</span></span> <span data-ttu-id="e4d91-117">Если оба входа выполняются успешно, первый тестовый пользователь запрашивает получение сведений о присутствии от второго пользователя.</span><span class="sxs-lookup"><span data-stu-id="e4d91-117">If both logons succeed, the first test user then asks to receive presence information from the second user.</span></span> <span data-ttu-id="e4d91-118">Второй пользователь публикует эту информацию и Test-CsPresence удостоверяет, что данные были успешно переданы первому пользователю.</span><span class="sxs-lookup"><span data-stu-id="e4d91-118">The second user publishes this information, and Test-CsPresence verifies that the information was successfully transmitted to the first user.</span></span> <span data-ttu-id="e4d91-119">После получения сведений о присутствии два тестовых пользователя затем выключаются из Lync Server.</span><span class="sxs-lookup"><span data-stu-id="e4d91-119">After the exchange of presence information, the two test users are then logged off from Lync Server.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="e4d91-120">Выполнение теста</span><span class="sxs-lookup"><span data-stu-id="e4d91-120">Running the test</span></span>

<span data-ttu-id="e4d91-121">Командлет Test-CsPresence можно выполнить с помощью пары предварительно настроенных тестовых учетных записей (см. раздел Настройка тестовых учетных записей для выполнения тестов Lync Server) или учетные записи любых двух пользователей, которые включены в Lync Server.</span><span class="sxs-lookup"><span data-stu-id="e4d91-121">The Test-CsPresence cmdlet can be run using either a pair of preconfigured test accounts (see Setting Up Test Accounts for Running Lync Server Tests) or the accounts of any two users who are enabled for Lync Server.</span></span> <span data-ttu-id="e4d91-122">Для выполнения этой проверки с помощью тестовых учетных записей нужно просто указать полное доменное имя для тестируемого пула Lync Server.</span><span class="sxs-lookup"><span data-stu-id="e4d91-122">To run this check using test accounts, you just have to specify the FQDN of the Lync Server pool being tested.</span></span> <span data-ttu-id="e4d91-123">Например:</span><span class="sxs-lookup"><span data-stu-id="e4d91-123">For example:</span></span>

    Test-CsPresence -TargetFqdn "atl-cs-001.litwareinc.com"

<span data-ttu-id="e4d91-124">Для выполнения этой проверки с использованием фактических учетных записей пользователей необходимо создать два объекта учетных данных Windows PowerShell (объекты, содержащие имя и пароль учетной записи) для каждой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="e4d91-124">To run this check using actual user accounts, you must create two Windows PowerShell credentials objects (objects that contain the account name and password) for each account.</span></span> <span data-ttu-id="e4d91-125">После вызова Test-CsPresence вы должны добавить эти объекты учетных данных и адреса SIP для двух учетных записей.</span><span class="sxs-lookup"><span data-stu-id="e4d91-125">You must then include those credentials objects and the SIP addresses of the two accounts when you call Test-CsPresence:</span></span>

    $credential1 = Get-Credential "litwareinc\kenmyer"
    $credential2 = Get-Credential "litwareinc\davidlongmire"
    Test-CsPresence -TargetFqdn "atl-cs-001.litwareinc.com" -PublisherSipAddress "sip:kenmyer@litwareinc.com" -PublisherCredential $credential1 -SubscriberSipAddress "sip:davidlongmire@litwareinc.com" -SubscriberCredential $credential2

<span data-ttu-id="e4d91-126">Дополнительные сведения можно найти в справочной документации по командлету [Test-CsPresence](https://docs.microsoft.com/powershell/module/skype/Test-CsPresence) .</span><span class="sxs-lookup"><span data-stu-id="e4d91-126">For more information, see the Help documentation for the [Test-CsPresence](https://docs.microsoft.com/powershell/module/skype/Test-CsPresence) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="e4d91-127">Определение успеха или сбоя</span><span class="sxs-lookup"><span data-stu-id="e4d91-127">Determining success or failure</span></span>

<span data-ttu-id="e4d91-128">Если указанные пользователи могут обмениваться сведениями о присутствии, вы получите вывод, как показано ниже, и свойство результата помечено как **успешно.**</span><span class="sxs-lookup"><span data-stu-id="e4d91-128">If the specified users can exchange presence information, then you'll receive output similar to this, with the Result property marked as **Success:**</span></span>

<span data-ttu-id="e4d91-129">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="e4d91-129">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="e4d91-130">Результат: успех</span><span class="sxs-lookup"><span data-stu-id="e4d91-130">Result : Success</span></span>

<span data-ttu-id="e4d91-131">Задержка: 00:00:06.3280315</span><span class="sxs-lookup"><span data-stu-id="e4d91-131">Latency : 00:00:06.3280315</span></span>

<span data-ttu-id="e4d91-132">Ошибки</span><span class="sxs-lookup"><span data-stu-id="e4d91-132">Error :</span></span>

<span data-ttu-id="e4d91-133">Диагностик</span><span class="sxs-lookup"><span data-stu-id="e4d91-133">Diagnosis :</span></span>

<span data-ttu-id="e4d91-134">Если два пользователя не могут обмениваться сведениями о присутствии, результат будет показан в виде ошибки, а дополнительные сведения будут записаны в свойствах Error и диагноз.</span><span class="sxs-lookup"><span data-stu-id="e4d91-134">If the two users can't exchange presence information, then the Result will be shown as Failure, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="e4d91-135">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="e4d91-135">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="e4d91-136">Результат: сбой</span><span class="sxs-lookup"><span data-stu-id="e4d91-136">Result : Failure</span></span>

<span data-ttu-id="e4d91-137">Задержка: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="e4d91-137">Latency : 00:00:00</span></span>

<span data-ttu-id="e4d91-138">Ошибка: 404, не найдена</span><span class="sxs-lookup"><span data-stu-id="e4d91-138">Error : 404, Not Found</span></span>

<span data-ttu-id="e4d91-139">Диагностика: ErrorCode = 4005, Source = ATL-CS-001.litwareinc.com,</span><span class="sxs-lookup"><span data-stu-id="e4d91-139">Diagnosis : ErrorCode=4005,Source=atl-cs-001.litwareinc.com,</span></span>

<span data-ttu-id="e4d91-140">Reason = универсальный код ресурса (URI) назначения не включен для SIP либо не</span><span class="sxs-lookup"><span data-stu-id="e4d91-140">Reason=Destination URI either not enabled for SIP or does not</span></span>

<span data-ttu-id="e4d91-141">Существует.</span><span class="sxs-lookup"><span data-stu-id="e4d91-141">exist.</span></span>

<span data-ttu-id="e4d91-142">Microsoft. RTC. SignalR. DiagnosticHeader</span><span class="sxs-lookup"><span data-stu-id="e4d91-142">Microsoft.Rtc.Signaling.DiagnosticHeader</span></span>

<span data-ttu-id="e4d91-143">Например, предыдущее выходное состояние не прошло проверку, так как по крайней мере одна из двух учетных записей пользователей недействительна: либо учетная запись не существует, либо она не включена для Lync Server.</span><span class="sxs-lookup"><span data-stu-id="e4d91-143">For example, the previous output states that the test failed because at least one of the two user accounts is not valid: either the account does not exist or it has not been enabled for Lync Server.</span></span> <span data-ttu-id="e4d91-144">Вы можете убедиться, что учетные записи существуют, и определить, включены ли они для Lync Server, выполнив следующую команду:</span><span class="sxs-lookup"><span data-stu-id="e4d91-144">You can verify that the accounts exist, and determine whether they are enabled for Lync Server, by running a command similar to this:</span></span>

    "sip:kenmyer@litwareinc.com", "sip:davidlongmire@litwareinc.com" | Get-CsUser | Select-Object SipAddress, Enabled

<span data-ttu-id="e4d91-145">Если Test-CsPresence не удается, возможно, потребуется повторно выполнить тест, на этот раз включая параметр подробно:</span><span class="sxs-lookup"><span data-stu-id="e4d91-145">If Test-CsPresence fails, then you might want to rerun the test, this time including the Verbose parameter:</span></span>

    Test-CsPresence -TargetFqdn "atl-cs-001.litwareinc.com" -Verbose

<span data-ttu-id="e4d91-146">После включения подробной информации Test-CsPresence будет возвращать пошаговые учетные записи каждого действия, которое он пытался войти на сервер Lync Server.</span><span class="sxs-lookup"><span data-stu-id="e4d91-146">When the Verbose parameter is included, Test-CsPresence will return a step-by-step account of each action it tried when it checked the ability of the specified user to log on to Lync Server.</span></span> <span data-ttu-id="e4d91-147">Например:</span><span class="sxs-lookup"><span data-stu-id="e4d91-147">For example:</span></span>

<span data-ttu-id="e4d91-148">Попадание в запрос на регистрацию для неизвестного</span><span class="sxs-lookup"><span data-stu-id="e4d91-148">Registration Request hit against Unknown</span></span>

<span data-ttu-id="e4d91-149">Действие "регистрация" завершено в течение "0,0345791" сек.</span><span class="sxs-lookup"><span data-stu-id="e4d91-149">'Register' activity completed in '0.0345791' secs.</span></span>

<span data-ttu-id="e4d91-150">Начато действие "SelfSubscribeActivity".</span><span class="sxs-lookup"><span data-stu-id="e4d91-150">'SelfSubscribeActivity' activity started.</span></span>

<span data-ttu-id="e4d91-151">Действие "SelfSubscribeActivity" завершено в течение "0,0041174" сек.</span><span class="sxs-lookup"><span data-stu-id="e4d91-151">'SelfSubscribeActivity' activity completed in '0.0041174' secs.</span></span>

<span data-ttu-id="e4d91-152">Начато действие "SubscribePresence".</span><span class="sxs-lookup"><span data-stu-id="e4d91-152">'SubscribePresence' activity started.</span></span>

<span data-ttu-id="e4d91-153">Действие "SubscribePresence" завершено в течение "0,0038764" сек.</span><span class="sxs-lookup"><span data-stu-id="e4d91-153">'SubscribePresence' activity completed in '0.0038764' secs.</span></span>

<span data-ttu-id="e4d91-154">Начато действие "PublishPresence".</span><span class="sxs-lookup"><span data-stu-id="e4d91-154">'PublishPresence' activity started.</span></span>

<span data-ttu-id="e4d91-155">Уведомление о присутствии исключения не получено в течение 25 сек.</span><span class="sxs-lookup"><span data-stu-id="e4d91-155">An exception 'Presence notification is not received within 25 secs.'</span></span> <span data-ttu-id="e4d91-156">произошла ошибка ruing рабочего процесса Microsoft. RTC. SyntheticTransactions. Workflow. STPresenceWorkflow.</span><span class="sxs-lookup"><span data-stu-id="e4d91-156">occurred ruing Workflow Microsoft.Rtc.SyntheticTransactions.Workflows.STPresenceWorkflow execution.</span></span>

<span data-ttu-id="e4d91-157">Тот факт, что уведомление о присутствии не было получено в течение 25 секунд, может указывать на проблемы с сетью, препятствующие обмену данными.</span><span class="sxs-lookup"><span data-stu-id="e4d91-157">The fact that the presence notification was not received within 25 seconds might indicate that network issues are preventing information from being exchanged.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="e4d91-158">Причины, по которым может произойти сбой теста</span><span class="sxs-lookup"><span data-stu-id="e4d91-158">Reasons why the test might have failed</span></span>

<span data-ttu-id="e4d91-159">Ниже приведены некоторые распространенные причины, по которым может произойти сбой Test-CsPresence.</span><span class="sxs-lookup"><span data-stu-id="e4d91-159">Here are some common reasons why Test-CsPresence might fail:</span></span>

  - <span data-ttu-id="e4d91-160">Вы указали неверную учетную запись пользователя.</span><span class="sxs-lookup"><span data-stu-id="e4d91-160">You specified an incorrect user account.</span></span> <span data-ttu-id="e4d91-161">Для проверки существования учетной записи пользователя можно выполнить следующую команду:</span><span class="sxs-lookup"><span data-stu-id="e4d91-161">You can verify that a user account exists by running a command similar to this:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com"

  - <span data-ttu-id="e4d91-162">Учетная запись пользователя верна, но в настоящее время учетная запись не включена для Lync Server.</span><span class="sxs-lookup"><span data-stu-id="e4d91-162">The user account is valid, but the account is currently not enabled for Lync Server.</span></span> <span data-ttu-id="e4d91-163">Чтобы убедиться в том, что учетная запись пользователя включена для Lync Server, выполните команду, подобную следующей:</span><span class="sxs-lookup"><span data-stu-id="e4d91-163">To verify that a user account is enabled for Lync Server, run a command similar to the following:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object Enabled
    
    <span data-ttu-id="e4d91-164">Если для свойства Enabled задано значение false, это означает, что пользователь в настоящее время не поддерживает Lync Server.</span><span class="sxs-lookup"><span data-stu-id="e4d91-164">If the Enabled property is set to False that means that the user is currently not enabled for Lync Server.</span></span>

<span data-ttu-id="e4d91-165"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e4d91-165"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

