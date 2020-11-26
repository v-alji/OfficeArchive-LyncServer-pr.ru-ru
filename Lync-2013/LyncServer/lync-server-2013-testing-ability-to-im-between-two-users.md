---
title: 'Lync Server 2013: Проверка возможности обмена мгновенными сообщениями между двумя пользователями'
description: 'Lync Server 2013: Проверка возможности обмена мгновенными сообщениями между двумя пользователями.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing ability to IM between two users
ms:assetid: a0f3f5c6-f115-4c3f-90ac-5fdc932b417e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn743838(v=OCS.15)
ms:contentKeyID: 63969635
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1409cfb58ed435a66dcf61db56660ca760e16422
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441097"
---
# <a name="testing-ability-to-im-between-two-users-in-lync-server-2013"></a><span data-ttu-id="3db1d-103">Возможность тестирования обмена мгновенными сообщениями между двумя пользователями в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3db1d-103">Testing ability to IM between two users in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3db1d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3db1d-104">

<span> </span></span></span>

<span data-ttu-id="3db1d-105">_**Тема последнего изменения:** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="3db1d-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3db1d-106">Расписание проверки</span><span class="sxs-lookup"><span data-stu-id="3db1d-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="3db1d-107">Ежедневно</span><span class="sxs-lookup"><span data-stu-id="3db1d-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3db1d-108">Средство тестирования</span><span class="sxs-lookup"><span data-stu-id="3db1d-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="3db1d-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="3db1d-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3db1d-110">Требуемые разрешения</span><span class="sxs-lookup"><span data-stu-id="3db1d-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="3db1d-111">При локальном запуске с помощью командной консоли Lync Server пользователи должны быть членами группы безопасности RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="3db1d-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="3db1d-112">При запуске с помощью удаленного экземпляра Windows PowerShell пользователям должна быть назначена роль RBAC, имеющая разрешение на запуск командлета Test-CsIM.</span><span class="sxs-lookup"><span data-stu-id="3db1d-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsIM cmdlet.</span></span> <span data-ttu-id="3db1d-113">Чтобы просмотреть список всех ролей RBAC, которые могут использовать этот командлет, выполните в командной строке Windows PowerShell следующую команду:</span><span class="sxs-lookup"><span data-stu-id="3db1d-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsIM&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="3db1d-114">Описание</span><span class="sxs-lookup"><span data-stu-id="3db1d-114">Description</span></span>

<span data-ttu-id="3db1d-115">Командлет Test-CsIM удостоверяется в том, что пользователь может обмениваться мгновенными сообщениями с помощью пары тестовых пользователей.</span><span class="sxs-lookup"><span data-stu-id="3db1d-115">The Test-CsIM cmdlet verifies that a pair of test users can exchange instant messages.</span></span> <span data-ttu-id="3db1d-116">При вызове командлет Test-CsIM запускается, пытаясь войти в систему с помощью пары тестовых пользователей на Lync Server.</span><span class="sxs-lookup"><span data-stu-id="3db1d-116">When called, the Test-CsIM cmdlet starts off by trying to log on a pair of test users to Lync Server.</span></span> <span data-ttu-id="3db1d-117">При условии, что два входа успешно выполняются, командлет запускает сеанс обмена мгновенными сообщениями между двумя тестовыми пользователями.</span><span class="sxs-lookup"><span data-stu-id="3db1d-117">Assuming the two logons are successful, the cmdlet then starts an IM session between the two test users.</span></span> <span data-ttu-id="3db1d-118">(Пользователь 1 приглашает пользователя 2 в сеанс обмена мгновенными сообщениями, а пользователь 2 принимает приглашение.) После того как вы убедитесь в том, что сообщения можно обменивать между двумя пользователями, Test-CsIM затем завершает сеанс обмена сообщениями и регистрирует обоих пользователей в системе.</span><span class="sxs-lookup"><span data-stu-id="3db1d-118">(User 1 invites User 2 to an IM session, and User 2 accepts the invitation.) After verifying that messages can be exchanged between the two users, Test-CsIM then ends the IM session and logs both users off the system.</span></span>

<span data-ttu-id="3db1d-119">Дополнительные сведения можно найти в справочной документации по командлету [Test-CsIM](https://docs.microsoft.com/powershell/module/skype/Test-CsIM) .</span><span class="sxs-lookup"><span data-stu-id="3db1d-119">For more information, see the Help documentation for the [Test-CsIM](https://docs.microsoft.com/powershell/module/skype/Test-CsIM) cmdlet.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="3db1d-120">Выполнение теста</span><span class="sxs-lookup"><span data-stu-id="3db1d-120">Running the Test</span></span>

<span data-ttu-id="3db1d-121">Командлет Test-CsIM можно выполнить с помощью пары предварительно настроенных тестовых учетных записей (см. раздел Настройка тестовых учетных записей для выполнения тестов Lync Server) или учетные записи любых двух пользователей, которые включены в Lync Server.</span><span class="sxs-lookup"><span data-stu-id="3db1d-121">The Test-CsIM cmdlet can be run using either a pair of preconfigured test accounts (see Setting Up Test Accounts for Running Lync Server Tests) or the accounts of any two users who are enabled for Lync Server.</span></span> <span data-ttu-id="3db1d-122">Для выполнения этой проверки с помощью тестовых учетных записей нужно просто указать полное доменное имя для тестируемого пула Lync Server.</span><span class="sxs-lookup"><span data-stu-id="3db1d-122">To run this check using test accounts, you just have to specify the FQDN of the Lync Server pool being tested.</span></span> <span data-ttu-id="3db1d-123">Например:</span><span class="sxs-lookup"><span data-stu-id="3db1d-123">For example:</span></span>

    Test-CsIM -TargetFqdn "atl-cs-001.litwareinc.com"

<span data-ttu-id="3db1d-124">Для выполнения этой проверки с использованием фактических учетных записей пользователей необходимо создать два объекта учетных данных Windows PowerShell (объекты, содержащие имя и пароль учетной записи) для каждой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="3db1d-124">To run this check using actual user accounts, you must create two Windows PowerShell credentials objects (objects that contain the account name and password) for each account.</span></span> <span data-ttu-id="3db1d-125">После вызова Test-CsIM вы должны добавить эти объекты учетных данных и адреса SIP для двух учетных записей.</span><span class="sxs-lookup"><span data-stu-id="3db1d-125">You must then include those credentials objects and the SIP addresses of the two accounts when you call Test-CsIM:</span></span>

    $credential1 = Get-Credential "litwareinc\kenmyer"
    $credential2 = Get-Credential "litwareinc\davidlongmire"
    Test-CsIm -TargetFqdn "atl-cs-001.litwareinc.com" -SenderSipAddress "sip:kenmyer@litwareinc.com" -SenderCredential $credential1 -ReceiverSipAddress "sip:davidlongmire@litwareinc.com" -ReceiverCredential $credential2

<span data-ttu-id="3db1d-126">Дополнительные сведения можно найти в справочной документации по командлету [Test-CsIM](https://docs.microsoft.com/powershell/module/skype/Test-CsIM) .</span><span class="sxs-lookup"><span data-stu-id="3db1d-126">For more information, see the Help documentation for the [Test-CsIM](https://docs.microsoft.com/powershell/module/skype/Test-CsIM) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="3db1d-127">Определение успеха или сбоя</span><span class="sxs-lookup"><span data-stu-id="3db1d-127">Determining Success or Failure</span></span>

<span data-ttu-id="3db1d-128">Если два пользователя могут завершить сеанс обмена мгновенными сообщениями, вы получите вывод примерно так, чтобы свойство Result пометило **"успешно".**</span><span class="sxs-lookup"><span data-stu-id="3db1d-128">If the two users can complete an instant messaging session, you'll receive output similar to this, with the Result property marked as **Success:**</span></span>

<span data-ttu-id="3db1d-129">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="3db1d-129">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="3db1d-130">Результат: успех</span><span class="sxs-lookup"><span data-stu-id="3db1d-130">Result : Success</span></span>

<span data-ttu-id="3db1d-131">Задержка: 00:00:06.6630911</span><span class="sxs-lookup"><span data-stu-id="3db1d-131">Latency : 00:00:06.6630911</span></span>

<span data-ttu-id="3db1d-132">Ошибки</span><span class="sxs-lookup"><span data-stu-id="3db1d-132">Error :</span></span>

<span data-ttu-id="3db1d-133">Диагностик</span><span class="sxs-lookup"><span data-stu-id="3db1d-133">Diagnosis :</span></span>

<span data-ttu-id="3db1d-134">Если тестовые пользователи не могут завершить сеанс, результат будет показан как сбой, а дополнительные сведения будут записаны в свойствах Error и диагноз.</span><span class="sxs-lookup"><span data-stu-id="3db1d-134">If the test users can't complete the session, the Result will be shown as Failure, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="3db1d-135">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="3db1d-135">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="3db1d-136">Результат: сбой</span><span class="sxs-lookup"><span data-stu-id="3db1d-136">Result : Failure</span></span>

<span data-ttu-id="3db1d-137">Задержка: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="3db1d-137">Latency : 00:00:00</span></span>

<span data-ttu-id="3db1d-138">Ошибка: 504, время ожидания сервера</span><span class="sxs-lookup"><span data-stu-id="3db1d-138">Error : 504, Server time-out</span></span>

<span data-ttu-id="3db1d-139">Диагностика: ErrorCode = 2, источник = ATL-CS-001. плана litwareinc. com, Reason = см.</span><span class="sxs-lookup"><span data-stu-id="3db1d-139">Diagnosis : ErrorCode=2, Source=atl-cs-001.litwareinc.com,Reason=See</span></span>

<span data-ttu-id="3db1d-140">код ответа и фраза с основанием.</span><span class="sxs-lookup"><span data-stu-id="3db1d-140">response code and reason phrase.</span></span>

<span data-ttu-id="3db1d-141">Microsoft. RTC. SignalR. DiagnosticHeader</span><span class="sxs-lookup"><span data-stu-id="3db1d-141">Microsoft.Rtc.Signaling.DiagnosticHeader</span></span>

<span data-ttu-id="3db1d-142">Например, в предыдущем выводе говорится, что тест завершился сбоем, так как указанный пользователь не найден.</span><span class="sxs-lookup"><span data-stu-id="3db1d-142">For example, the previous output states that the test failed because the specified user couldn't be found.</span></span> <span data-ttu-id="3db1d-143">Вы можете определить, является ли адрес SIP допустимым (и назначен ли пользователю этот SIP-адрес для Lync Server), выполнив следующую команду:</span><span class="sxs-lookup"><span data-stu-id="3db1d-143">You can determine whether a SIP address is valid (and whether the user assigned that SIP address was enabled for Lync Server) by running this command:</span></span>

    Get-CsUser "Ken Myer" | Select-Object SipAddress, Enabled

<span data-ttu-id="3db1d-144">Если Test-CsIM не удается, возможно, потребуется повторно выполнить тест, на этот раз включая параметр подробно:</span><span class="sxs-lookup"><span data-stu-id="3db1d-144">If Test-CsIM fails, then you might want to rerun the test, this time including the Verbose parameter:</span></span>

    Test-CsIM -TargetFqdn "atl-cs-001.litwareinc.com" -Verbose

<span data-ttu-id="3db1d-145">После включения подробной информации Test-CsIM будет возвращать пошаговые учетные записи каждого действия, которое оно предпринимало, когда вы проверили возможности двух тестовых пользователей стать частью сеанса обмена мгновенными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="3db1d-145">When the Verbose parameter is included, Test-CsIM will return a step-by-step account of each action it tried when it checked the ability of the two test users to take part in an IM session.</span></span> <span data-ttu-id="3db1d-146">Например, в приведенном ниже примере показано, как выводится сообщение о неправильном наборе учетных данных пользователя (в данном случае — неверный пароль) для проверки-CsIM:</span><span class="sxs-lookup"><span data-stu-id="3db1d-146">For example, here’s sample output that occurs when an incorrect set of user credentials (in this case, an incorrect password) is supplied to Test-CsIM:</span></span>

<span data-ttu-id="3db1d-147">Отправка запроса на регистрацию:</span><span class="sxs-lookup"><span data-stu-id="3db1d-147">Sending Registration request :</span></span>

<span data-ttu-id="3db1d-148">Целевое полное доменное имя = atl-cs-011.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="3db1d-148">Target Fqdn = atl-cs-011.litwareinc.com</span></span>

<span data-ttu-id="3db1d-149">SIP адрес пользователя = sip:kenmyer@litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="3db1d-149">User Sip Address = sip:kenmyer@litwareinc.com</span></span>

<span data-ttu-id="3db1d-150">Порт регистратора = 5061</span><span class="sxs-lookup"><span data-stu-id="3db1d-150">Registrar Port = 5061</span></span>

<span data-ttu-id="3db1d-151">Выбран тип проверки подлинности "IWA".</span><span class="sxs-lookup"><span data-stu-id="3db1d-151">Auth Type 'IWA' is selected.</span></span>

<span data-ttu-id="3db1d-152">Регистрация в соответствии с SIP/ATL-CS-001. плана litwareinc. com</span><span class="sxs-lookup"><span data-stu-id="3db1d-152">Registration hit against sip/atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="3db1d-153">Действие "регистрация" завершено в течение "0,0601795" сек.</span><span class="sxs-lookup"><span data-stu-id="3db1d-153">'Register' activity completed in '0.0601795' secs.</span></span>

<span data-ttu-id="3db1d-154">Исключение "вход был отклонен".</span><span class="sxs-lookup"><span data-stu-id="3db1d-154">An exception 'The log on was denied.</span></span> <span data-ttu-id="3db1d-155">Убедитесь в том, что используются правильные учетные данные, а учетная запись активна.</span><span class="sxs-lookup"><span data-stu-id="3db1d-155">Check that the correct credentials are being used and the account is active.'</span></span> <span data-ttu-id="3db1d-156">произошла ошибка рабочего процесса.</span><span class="sxs-lookup"><span data-stu-id="3db1d-156">occurred during the Workflow.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="3db1d-157">Причины, по которым может произойти сбой теста</span><span class="sxs-lookup"><span data-stu-id="3db1d-157">Reasons Why the Test Might Have Failed</span></span>

<span data-ttu-id="3db1d-158">Ниже приведены некоторые распространенные причины, по которым может произойти сбой Test-CsIM.</span><span class="sxs-lookup"><span data-stu-id="3db1d-158">Here are some common reasons why Test-CsIM might fail:</span></span>

  - <span data-ttu-id="3db1d-159">Указана недействительная учетная запись пользователя.</span><span class="sxs-lookup"><span data-stu-id="3db1d-159">You specified a user account that is not valid.</span></span> <span data-ttu-id="3db1d-160">Для проверки существования учетной записи пользователя можно выполнить следующую команду:</span><span class="sxs-lookup"><span data-stu-id="3db1d-160">You can verify that a user account exists by running a command similar to this:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com"

  - <span data-ttu-id="3db1d-161">Учетная запись пользователя верна, но в настоящее время учетная запись не включена для Lync Server.</span><span class="sxs-lookup"><span data-stu-id="3db1d-161">The user account is valid, but the account is currently not enabled for Lync Server.</span></span> <span data-ttu-id="3db1d-162">Чтобы убедиться в том, что учетная запись пользователя включена для Lync Server, выполните команду, подобную следующей:</span><span class="sxs-lookup"><span data-stu-id="3db1d-162">To verify that a user account is enabled for Lync Server, run a command similar to the following:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object Enabled
    
    <span data-ttu-id="3db1d-163">Если для свойства Enabled задано значение false, это означает, что пользователь в настоящее время не поддерживает Lync Server.</span><span class="sxs-lookup"><span data-stu-id="3db1d-163">If the Enabled property is set to False that means that the user is currently not enabled for Lync Server.</span></span>

  - <span data-ttu-id="3db1d-164">Возможно, служба мгновенных сообщений недоступна.</span><span class="sxs-lookup"><span data-stu-id="3db1d-164">The instant messaging service might not be available.</span></span> <span data-ttu-id="3db1d-165">С помощью Lync Server вы можете настроить систему таким образом, чтобы мгновенное сообщение не помогло быть доступно, если база данных архивации недоступна.</span><span class="sxs-lookup"><span data-stu-id="3db1d-165">With Lync Server, you can configure the system so that IM is not available if the archiving database cannot be accessed.</span></span> <span data-ttu-id="3db1d-166">Это можно проверить, выполнив команду, подобную следующей:</span><span class="sxs-lookup"><span data-stu-id="3db1d-166">You can verify that by running a command similar to the following:</span></span>
    
        Get-CsArchivingConfiguration -Identity "atl-cs-001.litwareinc.com" | Select-Object BlockOnArchiveFailure
    
    <span data-ttu-id="3db1d-167">Если для BlockOnArchiveFailure задано значение "true", необходимо определить, доступна ли база данных архивации.</span><span class="sxs-lookup"><span data-stu-id="3db1d-167">If BlockOnArchiveFailure is set to True, then you should determine whether or not the archiving database is available.</span></span> <span data-ttu-id="3db1d-168">Вы можете вернуть расположение баз данных архивации с помощью следующей команды:</span><span class="sxs-lookup"><span data-stu-id="3db1d-168">You can return the locations of your archiving databases by using the following command:</span></span>
    
        Get-CsService -ArchivingDatabase

  - <span data-ttu-id="3db1d-169">Сервер архивации может быть недоступен.</span><span class="sxs-lookup"><span data-stu-id="3db1d-169">The Archiving server might not be available.</span></span> <span data-ttu-id="3db1d-170">Вы можете получить полное доменное имя серверов архивации с помощью этой команды:</span><span class="sxs-lookup"><span data-stu-id="3db1d-170">You can retrieve the FQDN of your Archiving servers by using this command:</span></span>
    
        Get-CsService -ArchivingServer
    
    <span data-ttu-id="3db1d-171">Затем вы можете обратиться к соответствующему серверу, чтобы убедиться, что он доступен.</span><span class="sxs-lookup"><span data-stu-id="3db1d-171">You can then ping the appropriate server to verify that it is available.</span></span> <span data-ttu-id="3db1d-172">Например:</span><span class="sxs-lookup"><span data-stu-id="3db1d-172">For example:</span></span>
    
        ping atl-archiving-001.litwareinc.com

<span data-ttu-id="3db1d-173"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3db1d-173"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

