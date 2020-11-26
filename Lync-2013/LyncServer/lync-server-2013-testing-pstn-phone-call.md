---
title: 'Lync Server 2013: Проверка КОММУТИРУЕМого телефонного звонка'
description: 'Lync Server 2013: Проверка КОММУТИРУЕМого телефонного звонка.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing PSTN phone call
ms:assetid: dc7d319d-a627-45b6-a978-6111901251e3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn690133(v=OCS.15)
ms:contentKeyID: 63969656
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b42ea6dd46145961a34386d704f8f44e9b7909ad
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439767"
---
# <a name="testing-pstn-phone-call-in-lync-server-2013"></a><span data-ttu-id="848b2-103">Проверка телефонной связи PSTN в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="848b2-103">Testing PSTN phone call in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="848b2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="848b2-104">

<span> </span></span></span>

<span data-ttu-id="848b2-105">_**Тема последнего изменения:** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="848b2-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="848b2-106">Расписание проверки</span><span class="sxs-lookup"><span data-stu-id="848b2-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="848b2-107">Ежедневно</span><span class="sxs-lookup"><span data-stu-id="848b2-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848b2-108">Средство тестирования</span><span class="sxs-lookup"><span data-stu-id="848b2-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="848b2-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="848b2-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848b2-110">Требуемые разрешения</span><span class="sxs-lookup"><span data-stu-id="848b2-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="848b2-111">При локальном запуске с помощью командной консоли Lync Server пользователи должны быть членами группы безопасности RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="848b2-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="848b2-112">При запуске с помощью удаленного экземпляра Windows PowerShell пользователям должна быть назначена роль RBAC, имеющая разрешение на запуск командлета Test-CsRegistration.</span><span class="sxs-lookup"><span data-stu-id="848b2-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsRegistration cmdlet.</span></span> <span data-ttu-id="848b2-113">Чтобы просмотреть список всех ролей RBAC, которые могут использовать этот командлет, выполните в командной строке Windows PowerShell следующую команду:</span><span class="sxs-lookup"><span data-stu-id="848b2-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsPstnOutboundCall&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="848b2-114">Описание</span><span class="sxs-lookup"><span data-stu-id="848b2-114">Description</span></span>

<span data-ttu-id="848b2-115">Командлет Test-CsPstnOutboundCall проверяет способность пользователя звонить на номер телефона, находящийся в КТСОП.</span><span class="sxs-lookup"><span data-stu-id="848b2-115">The Test-CsPstnOutboundCall cmdlet tests the ability of a user to make a call to a phone number located on the PSTN.</span></span> <span data-ttu-id="848b2-116">При запуске test-CsPstnOutboundCall командлет сначала пытается записать тестовый пользователь на сервер Lync Server.</span><span class="sxs-lookup"><span data-stu-id="848b2-116">When you run Test-CsPstnOutboundCall, the cmdlet first attempts to log the test user on to Lync Server.</span></span> <span data-ttu-id="848b2-117">Если вход будет выполнен успешно, командлет попытается выполнить телефонный звонок через шлюз PSTN.</span><span class="sxs-lookup"><span data-stu-id="848b2-117">If the logon succeeds, the cmdlet will then try to make a phone call across the PSTN gateway.</span></span> <span data-ttu-id="848b2-118">Этот телефонный звонок будет выполняться с использованием абонентской группы, политики голосовой связи и других политик и параметров, назначенных тестовой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="848b2-118">This phone call will be made using the dial plan, voice policy, and other policies and settings assigned to the test account.</span></span> <span data-ttu-id="848b2-119">При ответе на звонок командлет отправляет Многочастотные коды с несколькими частотами (DTMF) по сети для проверки подключения к носителю.</span><span class="sxs-lookup"><span data-stu-id="848b2-119">When the call is answered, the cmdlet sends dual-tone multi-frequency (DTMF) codes over the network to verify media connectivity.</span></span>

<span data-ttu-id="848b2-120">При проведении проверки Test-CsPstnOutboundCall вызовет фактический телефонный звонок: конечный телефон будет звонить, и для успешного завершения теста должен быть дан ответ.</span><span class="sxs-lookup"><span data-stu-id="848b2-120">When conducting its test, Test-CsPstnOutboundCall will make an actual phone call: the target phone will ring and must be answered for the test to succeed.</span></span> <span data-ttu-id="848b2-121">Этот звонок также должен завершиться администратором вручную.</span><span class="sxs-lookup"><span data-stu-id="848b2-121">This call must also be manually ended by the administrator.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="848b2-122">Выполнение теста</span><span class="sxs-lookup"><span data-stu-id="848b2-122">Running the test</span></span>

<span data-ttu-id="848b2-123">Командлет Test-CsPstnOutboundCall можно выполнить с помощью предварительно настроенной тестовой учетной записи (см. раздел Настройка тестовых учетных записей для выполнения тестов Lync Server) или учетной записи пользователя, который включен для Lync Server.</span><span class="sxs-lookup"><span data-stu-id="848b2-123">The Test-CsPstnOutboundCall cmdlet can be run using either a preconfigured test account (see Setting Up Test Accounts for Running Lync Server Tests) or the account of any user who is enabled for Lync Server.</span></span> <span data-ttu-id="848b2-124">Для выполнения этой проверки с помощью тестовой учетной записи необходимо указать полное доменное имя тестируемого пула сервера Lync и телефонный номер PSTN.</span><span class="sxs-lookup"><span data-stu-id="848b2-124">To run this check using a test account, you just have to specify the FQDN of the Lync Server pool being tested and the PSTN phone number being called.</span></span> <span data-ttu-id="848b2-125">Например:</span><span class="sxs-lookup"><span data-stu-id="848b2-125">For example:</span></span>

    Test-CsPstnOutboundCall -TargetFqdn "atl-cs-001.litwareinc.com" -TargetPstnPhoneNumber "+12065551219"

<span data-ttu-id="848b2-126">Чтобы выполнить эту проверку с использованием реальной учетной записи пользователя, необходимо сначала создать объект учетных данных Windows PowerShell, содержащий имя учетной записи и пароль.</span><span class="sxs-lookup"><span data-stu-id="848b2-126">To run this check using an actual user account, you must first create a Windows PowerShell credentials object that contains the account name and password.</span></span> <span data-ttu-id="848b2-127">Затем необходимо добавить этот объект учетных данных и адрес SIP, назначенный учетной записи, при вызове Test-CsPstnOutboundCall:</span><span class="sxs-lookup"><span data-stu-id="848b2-127">You must then include that credentials object and the SIP address assigned to the account when you call Test-CsPstnOutboundCall:</span></span>

    $credential = Get-Credential "litwareinc\kenmyer"
    Test-CsPstnOutboundCall -TargetFqdn "atl-cs-001.litwareinc.com" -TargetPstnPhoneNumber "+12065551219" -UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential

<span data-ttu-id="848b2-128">Дополнительные сведения можно найти в справочной документации по командлету [Test-CsPstnOutboundCall](https://docs.microsoft.com/powershell/module/skype/Test-CsPstnOutboundCall) .</span><span class="sxs-lookup"><span data-stu-id="848b2-128">For more information, see the Help documentation for the [Test-CsPstnOutboundCall](https://docs.microsoft.com/powershell/module/skype/Test-CsPstnOutboundCall) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="848b2-129">Определение успеха или сбоя</span><span class="sxs-lookup"><span data-stu-id="848b2-129">Determining success or failure</span></span>

<span data-ttu-id="848b2-130">Если заданный пользователь может позвонить, и при ответе на него будет получено сообщение о том, что свойство результата помечено как **успешное:**</span><span class="sxs-lookup"><span data-stu-id="848b2-130">If the specified user can make the call, and if the call is answered, you'll receive output similar to this, with the Result property marked as **Success:**</span></span>

<span data-ttu-id="848b2-131">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="848b2-131">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="848b2-132">Результат: успех</span><span class="sxs-lookup"><span data-stu-id="848b2-132">Result : Success</span></span>

<span data-ttu-id="848b2-133">Задержка: 00:00:06.8630376</span><span class="sxs-lookup"><span data-stu-id="848b2-133">Latency : 00:00:06.8630376</span></span>

<span data-ttu-id="848b2-134">Ошибки</span><span class="sxs-lookup"><span data-stu-id="848b2-134">Error :</span></span>

<span data-ttu-id="848b2-135">Диагностик</span><span class="sxs-lookup"><span data-stu-id="848b2-135">Diagnosis :</span></span>

<span data-ttu-id="848b2-136">Если указанный пользователь не может позвонить или звонок не отвечает, результат будет показан как сбой, а дополнительные сведения будут записаны в свойствах Error и диагноз.</span><span class="sxs-lookup"><span data-stu-id="848b2-136">If the specified user can't make the call or if the call is not answered, then the Result will be shown as Failure, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="848b2-137">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="848b2-137">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="848b2-138">Результат: сбой</span><span class="sxs-lookup"><span data-stu-id="848b2-138">Result : Failure</span></span>

<span data-ttu-id="848b2-139">Задержка: 00:00:0987365</span><span class="sxs-lookup"><span data-stu-id="848b2-139">Latency : 00:00:0987365</span></span>

<span data-ttu-id="848b2-140">Ошибка: 403, запрещено</span><span class="sxs-lookup"><span data-stu-id="848b2-140">Error : 403, Forbidden</span></span>

<span data-ttu-id="848b2-141">Диагностика: ErrorCode = 12001, Source = ATL-CS-001. плана litwareinc. com, Reason = User</span><span class="sxs-lookup"><span data-stu-id="848b2-141">Diagnosis : ErrorCode=12001,Source=atl-cs-001.litwareinc.com,Reason=User</span></span>

<span data-ttu-id="848b2-142">Политика не содержит использование маршрутных номеров</span><span class="sxs-lookup"><span data-stu-id="848b2-142">Policy does not contain phone route usage</span></span>

<span data-ttu-id="848b2-143">В предыдущем выводе говорится, что тест завершился сбоем, так как политика голосовой связи, назначенная указанному пользователю, не содержит использование телефона.</span><span class="sxs-lookup"><span data-stu-id="848b2-143">The previous output states that the test failed because the voice policy assigned to the specified user does not include a phone usage.</span></span> <span data-ttu-id="848b2-144">(Использование телефона применяет политики голосовой связи для голосовых маршрутов.</span><span class="sxs-lookup"><span data-stu-id="848b2-144">(Phone usages tie voice policies to voice routes.</span></span> <span data-ttu-id="848b2-145">Без политики голосовой связи и соответствующего голосового маршрута вы не можете звонить по протоколу PSTN.</span><span class="sxs-lookup"><span data-stu-id="848b2-145">Without both a voice policy and a corresponding voice route you can't make calls over the PSTN.)</span></span>

<span data-ttu-id="848b2-146">Если Test-CsPstnOutboundCall не удается, возможно, потребуется повторно выполнить тест, на этот раз включая параметр подробно:</span><span class="sxs-lookup"><span data-stu-id="848b2-146">If Test-CsPstnOutboundCall fails then you might want to rerun the test, this time including the Verbose parameter:</span></span>

    Test-CsPstnOutboundCall -TargetFqdn "atl-cs-001.litwareinc.com" -TargetPstnPhoneNumber "+12065551219" -Verbose

<span data-ttu-id="848b2-147">После включения подробной информации Test-CsPstnOutboundCall будет возвращать пошаговые учетные записи каждого действия, которое он пытался войти на сервер Lync Server.</span><span class="sxs-lookup"><span data-stu-id="848b2-147">When the Verbose parameter is included, Test-CsPstnOutboundCall will return a step-by-step account of each action it tried when it checked the ability of the specified user to log on to Lync Server.</span></span> <span data-ttu-id="848b2-148">Например, эти выходные данные указывают на то, что неполадки в сети не препятствуют подключению к КТСОП.</span><span class="sxs-lookup"><span data-stu-id="848b2-148">For example, this output indicates that network problems are preventing a connection with the PSTN:</span></span>

<span data-ttu-id="848b2-149">Установка голосового видеозвонка на "SIP: + 12065551219@litwareinc. com; user = Phone".</span><span class="sxs-lookup"><span data-stu-id="848b2-149">Establishing Audio Video call to 'sip:+12065551219@litwareinc.com;user=phone'.</span></span>

<span data-ttu-id="848b2-150">В сети получено исключение "404 (не найдено), и операция завершилась сбоем.</span><span class="sxs-lookup"><span data-stu-id="848b2-150">An exception 'A 404 (Not Found) response was received from the network and the operation failed.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="848b2-151">Причины, по которым может произойти сбой теста</span><span class="sxs-lookup"><span data-stu-id="848b2-151">Reasons why the test might have failed</span></span>

<span data-ttu-id="848b2-152">Ниже приведены некоторые распространенные причины, по которым может произойти сбой Test-CsPstnOutboundCall.</span><span class="sxs-lookup"><span data-stu-id="848b2-152">Here are some common reasons why Test-CsPstnOutboundCall might fail:</span></span>

  - <span data-ttu-id="848b2-153">Вы указали недопустимую учетную запись пользователя.</span><span class="sxs-lookup"><span data-stu-id="848b2-153">You specified an invalid user account.</span></span> <span data-ttu-id="848b2-154">Для проверки существования учетной записи пользователя можно выполнить следующую команду:</span><span class="sxs-lookup"><span data-stu-id="848b2-154">You can verify that a user account exists by running a command similar to this:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com"

  - <span data-ttu-id="848b2-155">Учетная запись пользователя верна, но в настоящее время учетная запись не включена для Lync Server.</span><span class="sxs-lookup"><span data-stu-id="848b2-155">The user account is valid, but the account is currently not enabled for Lync Server.</span></span> <span data-ttu-id="848b2-156">Чтобы убедиться в том, что учетная запись пользователя включена для Lync Server, выполните команду, подобную следующей:</span><span class="sxs-lookup"><span data-stu-id="848b2-156">To verify that a user account is enabled for Lync Server, run a command similar to the following:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object Enabled
    
    <span data-ttu-id="848b2-157">Если для свойства Enabled задано значение false, это означает, что пользователь в настоящее время не поддерживает Lync Server.</span><span class="sxs-lookup"><span data-stu-id="848b2-157">If the Enabled property is set to False that means that the user is currently not enabled for Lync Server.</span></span>

  - <span data-ttu-id="848b2-158">Политика голосовой связи, назначенная указанному пользователю, не может использоваться в качестве использования КТСОП.</span><span class="sxs-lookup"><span data-stu-id="848b2-158">The voice policy assigned to the specified user does not have a valid PSTN usage.</span></span> <span data-ttu-id="848b2-159">Вы можете определить политику голосовой связи, назначенную для пользователя, с помощью следующей команды:</span><span class="sxs-lookup"><span data-stu-id="848b2-159">You can determine the voice policy that is assigned to a user by using a command similar to this:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object VoicePolicy
    
    <span data-ttu-id="848b2-160">Затем вы можете определить использование PSTN (если таковые есть), назначенные этой политике, используя следующую команду, которая извлекает сведения о политике голосовой связи для пользователя RedmondVoicePolicy:</span><span class="sxs-lookup"><span data-stu-id="848b2-160">And then you can determine the PSTN usages (if any) that are assigned to that policy by using a command similar to the following, which retrieves information about the per-user voice policy RedmondVoicePolicy:</span></span>
    
        Get-CsVoicePolicy -Identity "RedmondVoicePolicy"

<span data-ttu-id="848b2-161"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="848b2-161"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

