---
title: 'Lync Server 2013: Проверка подключения пользователя к UM Exchange'
description: 'Lync Server 2013: Проверка подключения пользователя к UM Exchange.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing user connection to Exchange UM
ms:assetid: 0b83fbf4-e124-4efd-a0a9-202eb849af82
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn727300(v=OCS.15)
ms:contentKeyID: 63969573
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ea6f7d446fe3fd98db67bab4ffee9cc976202689
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440936"
---
# <a name="testing-user-connection-to-exchange-um-in-lync-server-2013"></a><span data-ttu-id="2b1e2-103">Проверка подключения пользователя к UM Exchange в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2b1e2-103">Testing user connection to Exchange UM in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2b1e2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2b1e2-104">

<span> </span></span></span>

<span data-ttu-id="2b1e2-105">_**Тема последнего изменения:** 2014-11-01_</span><span class="sxs-lookup"><span data-stu-id="2b1e2-105">_**Topic Last Modified:** 2014-11-01_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2b1e2-106">Расписание проверки</span><span class="sxs-lookup"><span data-stu-id="2b1e2-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="2b1e2-107">Ежедневно</span><span class="sxs-lookup"><span data-stu-id="2b1e2-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b1e2-108">Средство тестирования</span><span class="sxs-lookup"><span data-stu-id="2b1e2-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="2b1e2-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="2b1e2-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b1e2-110">Требуемые разрешения</span><span class="sxs-lookup"><span data-stu-id="2b1e2-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="2b1e2-111">При локальном запуске с помощью командной консоли Lync Server пользователи должны быть членами группы безопасности RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="2b1e2-112">При запуске с помощью удаленного экземпляра Windows PowerShell пользователям должна быть назначена роль RBAC, имеющая разрешение на запуск командлета <strong>Test-CsExUMConnectivity</strong> .</span><span class="sxs-lookup"><span data-stu-id="2b1e2-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the <strong>Test-CsExUMConnectivity</strong> cmdlet.</span></span> <span data-ttu-id="2b1e2-113">Чтобы просмотреть список всех ролей RBAC, которые могут использовать этот командлет, выполните в командной строке Windows PowerShell следующую команду:</span><span class="sxs-lookup"><span data-stu-id="2b1e2-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsExUMConnectivity&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="2b1e2-114">Описание</span><span class="sxs-lookup"><span data-stu-id="2b1e2-114">Description</span></span>

<span data-ttu-id="2b1e2-115">Командлет **Test-CsExUMConnectivity** подтверждает, что указанный пользователь может подключиться к службе единой системы обмена сообщениями Microsoft Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-115">The **Test-CsExUMConnectivity** cmdlet verifies that the specified user can connect to the Microsoft Exchange Server 2013 unified messaging service.</span></span> <span data-ttu-id="2b1e2-116">Обратите внимание, что этот командлет проверяет только то, что подключение может быть выполнено для службы.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-116">Note that this cmdlet only verifies that a connection can be made to the service.</span></span> <span data-ttu-id="2b1e2-117">Сама служба не проверяется.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-117">It does not test the service itself.</span></span> <span data-ttu-id="2b1e2-118">Чтобы протестировать службу единой системы обмена сообщениями (с помощью командлета синтетической транзакции, который действительно оставляет сообщение голосовой почты в почтовом ящике пользователя), используйте командлет Test-CsExUMVoiceMail.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-118">To test the unified messaging service (by running a synthetic transaction cmdlet that actually leaves a voice mail message in a user's mailbox) use the Test-CsExUMVoiceMail cmdlet.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="2b1e2-119">Выполнение теста</span><span class="sxs-lookup"><span data-stu-id="2b1e2-119">Running the test</span></span>

<span data-ttu-id="2b1e2-120">В следующем примере показано, как проверить подключение к единой системе обмена сообщениями Exchange для пула atl-cs-001.litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-120">The following example tests Exchange Unified Messaging connectivity for the pool atl-cs-001.litwareinc.com.</span></span> <span data-ttu-id="2b1e2-121">Эта команда будет работать только в том случае, если тестовые пользователи были определены для пула atl-cs-001.litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-121">This command will work only if test users were defined for the pool atl-cs-001.litwareinc.com.</span></span> <span data-ttu-id="2b1e2-122">Если это так, команда определит, может ли первый тестовый пользователь подключаться к единой системе обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-122">If they have, then the command will determine whether the first test user can connect to Unified Messaging.</span></span> <span data-ttu-id="2b1e2-123">Если тестовые пользователи не были настроены для пула, команда завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-123">If test users were not configured for the pool then the command will fail.</span></span>

    Test-CsExUMConnectivity -TargetFqdn "atl-cs-001.litwareinc.com" 

<span data-ttu-id="2b1e2-124">Команды, показанные в следующем примере, проверяют подключение к единой системе обмена сообщениями Exchange для пользователя плана litwareinc \\ kenmyer.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-124">The commands shown in the following example test Exchange Unified Messaging connectivity for the user litwareinc\\kenmyer.</span></span> <span data-ttu-id="2b1e2-125">Для этого в первой команде примера используется командлет **Get-Credential** для создания объекта учетных данных интерфейса командной строки Windows PowerShell для пользователя плана litwareinc \\ kenmyer.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-125">To do this, the first command in the example uses the **Get-Credential** cmdlet to create a Windows PowerShell command-line interface credentials object for the user litwareinc\\kenmyer.</span></span> <span data-ttu-id="2b1e2-126">Обратите внимание, что для этой учетной записи необходимо указать пароль, чтобы создать допустимый объект учетных данных и убедиться, что командлет **Test-CsExUMConnectivity** может выполнить свою проверку.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-126">Note that you must supply the password for this account to create a valid credentials object and to ensure that the **Test-CsExUMConnectivity** cmdlet can run its check.</span></span>

<span data-ttu-id="2b1e2-127">Во второй команде в примере используется предоставленный объект учетных данных ($x) и адрес SIP пользователя плана litwareinc kenmyer, \\ чтобы определить, может ли этот пользователь подключиться к единой системе обмена сообщениями Exchange.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-127">The second command in the example uses the supplied credentials object ($x) and the SIP address of the user litwareinc\\kenmyer to determine whether or this user can connect to Exchange Unified Messaging.</span></span>

    $credential = Get-Credential "litwareinc\kenmyer" 
    Test-CsExUMConnectivity -TargetFqdn "atl-cs-001.litwareinc.com" -UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential

<span data-ttu-id="2b1e2-128">Команда, показанная в следующем примере, является вариантом только что показанной команды.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-128">The command shown in the next example is a variation of the command just shown.</span></span> <span data-ttu-id="2b1e2-129">В этом случае параметр OutLoggerVariable включается для создания подробного журнала каждого шага, выполненного с помощью **Test-CsExUMConnectivity** , cmdletand успешное выполнение или сбой каждого из этих действий.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-129">In this case, the OutLoggerVariable parameter is included to generate a detailed log of every step done by the **Test-CsExUMConnectivity** cmdletand the success or failure of each of those steps.</span></span> <span data-ttu-id="2b1e2-130">Для этого параметр OutLoggerVariable добавляется вместе со значением параметра ExumText; Это приводит к тому, что подробные данные журнала хранятся в переменной с именем $ExumTest.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-130">To do this, the OutLoggerVariable parameter is added together with the parameter value ExumText; that causes detailed logging information to be stored in a variable named $ExumTest.</span></span> <span data-ttu-id="2b1e2-131">В последней команде в примере метод ToXML () используется для преобразования данных журнала в формат XML.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-131">In the final command in the example, the ToXML() method is used to convert the log information to XML format.</span></span> <span data-ttu-id="2b1e2-132">Эти данные XML затем записываются в файл с именем C: \\ журналы \\ExumTest.xml с помощью командлета Out-File.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-132">That XML data is then written to a file that is named C:\\Logs\\ExumTest.xml by using the Out-File cmdlet.</span></span>

    $credential = Get-Credential "litwareinc\kenmyer" 
    Test-CsExUMConnectivity -TargetFqdn "atl-cs-001.litwareinc.com" -UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential -OutLoggerVariable ExumTest 
    $ExumTest.ToXML() | Out-File C:\Logs\ExumTest.xml 

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="2b1e2-133">Определение успеха или сбоя</span><span class="sxs-lookup"><span data-stu-id="2b1e2-133">Determining success or failure</span></span>

<span data-ttu-id="2b1e2-134">Если интеграция с Exchange настроена правильно, вы получите вывод, аналогичный этому, и свойство Result помечается как **успешно**.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-134">If Exchange integration is correctly configured, you'll receive output similar to this, with the Result property marked as **Success**:</span></span>

<span data-ttu-id="2b1e2-135">Целевое полное доменное имя: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="2b1e2-135">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="2b1e2-136">Результат: успех</span><span class="sxs-lookup"><span data-stu-id="2b1e2-136">Result : Success</span></span>

<span data-ttu-id="2b1e2-137">Задержка: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="2b1e2-137">Latency : 00:00:00</span></span>

<span data-ttu-id="2b1e2-138">Сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="2b1e2-138">Error Message :</span></span>

<span data-ttu-id="2b1e2-139">Диагностик</span><span class="sxs-lookup"><span data-stu-id="2b1e2-139">Diagnosis :</span></span>

<span data-ttu-id="2b1e2-140">Если указанный пользователь не может получать уведомления, результат будет отображаться как **сбой**, а дополнительные сведения будут записаны в свойствах Error и диагноз.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-140">If the specified user can't receive notifications, the Result will be shown as **Failure**, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="2b1e2-141">Целевое полное доменное имя: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="2b1e2-141">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="2b1e2-142">Результат: сбой</span><span class="sxs-lookup"><span data-stu-id="2b1e2-142">Result : Failure</span></span>

<span data-ttu-id="2b1e2-143">Задержка: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="2b1e2-143">Latency : 00:00:00</span></span>

<span data-ttu-id="2b1e2-144">Сообщение об ошибке: 10060, не удалось установить соединение из-за того, что подключенная сторона</span><span class="sxs-lookup"><span data-stu-id="2b1e2-144">Error Message : 10060, A connection attempt failed because the connected party</span></span>

<span data-ttu-id="2b1e2-145">не отвечает на запросы в течение определенного периода времени или</span><span class="sxs-lookup"><span data-stu-id="2b1e2-145">did not properly respond after a period of time, or</span></span>

<span data-ttu-id="2b1e2-146">не удалось установить соединение, так как подключенный узел имеет</span><span class="sxs-lookup"><span data-stu-id="2b1e2-146">established connection failed because connected host has</span></span>

<span data-ttu-id="2b1e2-147">не удалось ответить на 10.188.116.96:5061</span><span class="sxs-lookup"><span data-stu-id="2b1e2-147">failed to respond 10.188.116.96:5061</span></span>

<span data-ttu-id="2b1e2-148">Внутреннее исключение: сбой при попытке подключения из-за того, что</span><span class="sxs-lookup"><span data-stu-id="2b1e2-148">Inner Exception:A connection attempt failed because the</span></span>

<span data-ttu-id="2b1e2-149">связь с абонентом завершилась неправильно после определенного периода</span><span class="sxs-lookup"><span data-stu-id="2b1e2-149">connected party did not properly respond after a period of</span></span>

<span data-ttu-id="2b1e2-150">время или соединение не удалось установить, так как подключенный узел</span><span class="sxs-lookup"><span data-stu-id="2b1e2-150">time, or established connection failed because connected host</span></span>

<span data-ttu-id="2b1e2-151">не удалось ответить 10.188.116.96:5061</span><span class="sxs-lookup"><span data-stu-id="2b1e2-151">has failed to respond 10.188.116.96:5061</span></span>

<span data-ttu-id="2b1e2-152">Диагностик</span><span class="sxs-lookup"><span data-stu-id="2b1e2-152">Diagnosis :</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="2b1e2-153">Причины, по которым может произойти сбой теста</span><span class="sxs-lookup"><span data-stu-id="2b1e2-153">Reasons why the test might have failed</span></span>

<span data-ttu-id="2b1e2-154">Ниже приведены некоторые распространенные причины, по которым может произойти сбой **Test-CsExUMConnectivity** :</span><span class="sxs-lookup"><span data-stu-id="2b1e2-154">Here are some common reasons why **Test-CsExUMConnectivity** might fail:</span></span>

  - <span data-ttu-id="2b1e2-155">Предоставлено неправильное значение параметра.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-155">An incorrect parameter value was supplied.</span></span> <span data-ttu-id="2b1e2-156">Если используется, необязательные параметры необходимо настроить правильно, или тест завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-156">If used, the optional parameters must be configured correctly or the test will fail.</span></span> <span data-ttu-id="2b1e2-157">Повторите выполнение команды без дополнительных параметров и проверьте, выполняется ли это успешно.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-157">Rerun the command without the optional parameters and see whether that succeeds.</span></span>

  - <span data-ttu-id="2b1e2-158">Эта команда завершается сбоем, если сервер Exchange неправильно настроен или еще не развернут.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-158">This command will fail if the Exchange Server is misconfigured or not yet deployed.</span></span>

  - <span data-ttu-id="2b1e2-159">Эта команда завершится сбоем, если сервер Exchange недоступен по сети.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-159">This command will fail if the Exchange Server is not reachable over your network.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="2b1e2-160">См. также</span><span class="sxs-lookup"><span data-stu-id="2b1e2-160">See Also</span></span>


[<span data-ttu-id="2b1e2-161">Test-CsExUMVoiceMail</span><span class="sxs-lookup"><span data-stu-id="2b1e2-161">Test-CsExUMVoiceMail</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsExUMVoiceMail)  
  

<span data-ttu-id="2b1e2-162"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2b1e2-162"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

