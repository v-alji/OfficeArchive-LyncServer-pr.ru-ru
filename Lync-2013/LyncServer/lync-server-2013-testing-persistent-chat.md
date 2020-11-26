---
title: 'Lync Server 2013: Проверка сохраняемого чата'
description: 'Lync Server 2013: Проверка сохраняемого чата.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing persistent chat
ms:assetid: d351b6f2-bc31-42e0-9e8d-c347713d6b4a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn727313(v=OCS.15)
ms:contentKeyID: 63969651
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a8b1dc4eef1870f1287dacdc1852ab1e24edd169
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440999"
---
# <a name="testing-persistent-chat-in-lync-server-2013"></a><span data-ttu-id="cc7ae-103">Проверка сохраняемого чата в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cc7ae-103">Testing persistent chat in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cc7ae-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cc7ae-104">

<span> </span></span></span>

<span data-ttu-id="cc7ae-105">_**Тема последнего изменения:** 2014-11-03_</span><span class="sxs-lookup"><span data-stu-id="cc7ae-105">_**Topic Last Modified:** 2014-11-03_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cc7ae-106">Расписание проверки</span><span class="sxs-lookup"><span data-stu-id="cc7ae-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="cc7ae-107">Ежедневно</span><span class="sxs-lookup"><span data-stu-id="cc7ae-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc7ae-108">Средство тестирования</span><span class="sxs-lookup"><span data-stu-id="cc7ae-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="cc7ae-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="cc7ae-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc7ae-110">Требуемые разрешения</span><span class="sxs-lookup"><span data-stu-id="cc7ae-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="cc7ae-111">При локальном запуске с помощью командной консоли Lync Server пользователи должны быть членами группы безопасности RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="cc7ae-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="cc7ae-112">При запуске с помощью удаленного экземпляра Windows PowerShell пользователям должна быть назначена роль RBAC, имеющая разрешение на запуск командлета <strong>Test-CsPersistentChatMessage</strong> .</span><span class="sxs-lookup"><span data-stu-id="cc7ae-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the <strong>Test-CsPersistentChatMessage</strong> cmdlet.</span></span> <span data-ttu-id="cc7ae-113">Чтобы просмотреть список всех ролей RBAC, которые могут использовать этот командлет, выполните в командной строке Windows PowerShell следующую команду:</span><span class="sxs-lookup"><span data-stu-id="cc7ae-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsPersistentChatMessage&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="cc7ae-114">Описание</span><span class="sxs-lookup"><span data-stu-id="cc7ae-114">Description</span></span>

<span data-ttu-id="cc7ae-115">Командлет **Test-CsPersistentChatMessage** удостоверяется в том, что с помощью службы сохраняемого чата пользователи могут обмениваться сообщениями с другими тестами.</span><span class="sxs-lookup"><span data-stu-id="cc7ae-115">The **Test-CsPersistentChatMessage** cmdlet verifies that a pair of test users can exchange messages using the Persistent Chat service.</span></span> <span data-ttu-id="cc7ae-116">Для этого командлет заносит двух пользователей на Lync Server 2013, подключает пользователей к сохраняемой комнате чата, обменивается сообщениями, а затем выходит из комнаты чата и завершает работу двух пользователей.</span><span class="sxs-lookup"><span data-stu-id="cc7ae-116">To do this, the cmdlet logs the two users on to Lync Server 2013, connects the users to a persistent Chat room, exchanges a pair of messages, then exits the chat room and logs off the two users.</span></span> <span data-ttu-id="cc7ae-117">Обратите внимание на то, что если вы не создали комнаты чата или если у двух тестовых учетных записей не назначена политика сохраняемого чата, которая предоставляет им доступ к службе сохраняемого чата, следует отметить, что вызов этого командлета завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="cc7ae-117">Note that calls to this cmdlet will fail if you have not created any chat rooms or if the two test user accounts are not assigned a Persistent Chat policy that gives them access to the Persistent Chat service.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="cc7ae-118">Выполнение теста</span><span class="sxs-lookup"><span data-stu-id="cc7ae-118">Running the test</span></span>

<span data-ttu-id="cc7ae-119">Команды, показанные в приведенном ниже примере, проверяют возможность \\ \\ подключения к серверу Lync Server 2013 (плана litwareinc почтового и плана litwareinc kenmyer), а затем обмен сообщениями с помощью службы сохраняемого чата.</span><span class="sxs-lookup"><span data-stu-id="cc7ae-119">The commands shown in the following example test the ability of a pair of users (litwareinc\\pilar and litwareinc\\kenmyer) to log on to Lync Server 2013 and then exchange messages using the Persistent Chat service.</span></span> <span data-ttu-id="cc7ae-120">Для этого в первой команде примера используется командлет **Get-Credential** для создания объекта учетных данных интерфейса командной строки Windows PowerShell, содержащего имя и пароль пользователя почтового Вронский.</span><span class="sxs-lookup"><span data-stu-id="cc7ae-120">To do this, the first command in the example uses the **Get-Credential** cmdlet to create a Windows PowerShell command-line interface credential object that contains the name and password of the user Pilar Ackerman.</span></span> <span data-ttu-id="cc7ae-121">(Поскольку имя для входа, плана litwareinc \\ почтового, было включено в качестве параметра, в диалоговом окне Запрос учетных данных Windows PowerShell требуется, чтобы администратор введет пароль для учетной записи почтового Вронский.) Результирующий объект учетных данных сохраняется в переменной с именем $cred 1.</span><span class="sxs-lookup"><span data-stu-id="cc7ae-121">(Because the logon name, litwareinc\\pilar, was included as a parameter, the Windows PowerShell Credential Request dialog box only requires the administrator to enter the password for the Pilar Ackerman account.) The resulting credentials object is then stored in a variable named $cred1.</span></span> <span data-ttu-id="cc7ae-122">Вторая команда — это то же самое, что возвращает объект учетной записи Кен Myer.</span><span class="sxs-lookup"><span data-stu-id="cc7ae-122">The second command does the same thing, this time returning a credential object for the Ken Myer account.</span></span>

<span data-ttu-id="cc7ae-123">Если у вас есть объекты учетных данных, третья команда определяет, могут ли эти два пользователя входить на сервер Lync Server 2013 и обмениваться сообщениями с помощью сохраняемого чата.</span><span class="sxs-lookup"><span data-stu-id="cc7ae-123">With the credential objects in hand, the third command determines whether these two users can log on to Lync Server 2013 and exchange messages using Persistent Chat.</span></span> <span data-ttu-id="cc7ae-124">Для выполнения этой задачи командлет **Test-CsPersistentChatMessage** вызывается с помощью следующих параметров: TargetFqdn (полное доменное имя пула регистраторов). SenderSipAddress (адрес SIP для первого тестового пользователя); SenderCredential (объект Windows PowerShell, который включает в себя учетные данные для этого пользователя); ReceiverSipAddress (SIP-адрес для другого тестового пользователя); и ReceiverCredential (объект Windows PowerShell, который включает в себя учетные данные для другого тестового пользователя).</span><span class="sxs-lookup"><span data-stu-id="cc7ae-124">To perform this task, the **Test-CsPersistentChatMessage** cmdlet is called using the following parameters: TargetFqdn (the FQDN of the Registrar pool); SenderSipAddress (the SIP address for the first test user); SenderCredential (the Windows PowerShell object that contains the credentials for this same user); ReceiverSipAddress (the SIP address for the other test user); and ReceiverCredential (the Windows PowerShell object that contains the credentials for the other test user).</span></span>

    $cred1 = Get-Credential "litwareinc\pilar"
    $cred2 = Get-Credential "litwareinc\kenmyer"
    
    Test-CsPersistentChatMessage -TargetFqdn atl-persistentchat-001.litwareinc.com -SenderSipAddress "sip:pilar@litwareinc.com" -SenderCredential $cred1 -ReceiverSipAddress "sip:kenmyer@litwareinc.com" -ReceiverCredential $cred2

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="cc7ae-125">Определение успеха или сбоя</span><span class="sxs-lookup"><span data-stu-id="cc7ae-125">Determining success or failure</span></span>

<span data-ttu-id="cc7ae-126">Если указанный пользователь имеет действующую политику расположения, вы получите вывод, как показано ниже, и свойство Result, помеченное как **успешно**.</span><span class="sxs-lookup"><span data-stu-id="cc7ae-126">If the specified user has a valid location policy, then you'll receive output similar to this, with the Result property marked as **Success**:</span></span>

<span data-ttu-id="cc7ae-127">Целевое полное доменное имя: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="cc7ae-127">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="cc7ae-128">Результат: успех</span><span class="sxs-lookup"><span data-stu-id="cc7ae-128">Result : Success</span></span>

<span data-ttu-id="cc7ae-129">Задержка: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="cc7ae-129">Latency : 00:00:00</span></span>

<span data-ttu-id="cc7ae-130">Сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="cc7ae-130">Error Message :</span></span>

<span data-ttu-id="cc7ae-131">Диагностик</span><span class="sxs-lookup"><span data-stu-id="cc7ae-131">Diagnosis :</span></span>

<span data-ttu-id="cc7ae-132">Если указанные пользователи не могут обмениваться сообщениями с помощью службы "сохраняемый чат", результат будет отображаться как **сбой**, а дополнительные сведения будут записаны в свойствах Error и диагноз.</span><span class="sxs-lookup"><span data-stu-id="cc7ae-132">If the specified users can't exchange messages using the Persistent Chat service, the Result will be shown as **Failure**, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="cc7ae-133">Предупреждение: не удалось прочитать номер порта регистратора для заданного полного имени</span><span class="sxs-lookup"><span data-stu-id="cc7ae-133">WARNING: Failed to read Registrar port number for the given fully qualified</span></span>

<span data-ttu-id="cc7ae-134">доменное имя (FQDN).</span><span class="sxs-lookup"><span data-stu-id="cc7ae-134">domain name (FQDN).</span></span> <span data-ttu-id="cc7ae-135">С помощью номера порта регистратора по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cc7ae-135">Using default Registrar port number.</span></span> <span data-ttu-id="cc7ae-136">Ошибка</span><span class="sxs-lookup"><span data-stu-id="cc7ae-136">Exception:</span></span>

<span data-ttu-id="cc7ae-137">System. InvalidOperationException: в топологии не обнаружены подходящие кластеры.</span><span class="sxs-lookup"><span data-stu-id="cc7ae-137">System.InvalidOperationException: No matching cluster found in topology.</span></span>

<span data-ttu-id="cc7ae-138">скорость</span><span class="sxs-lookup"><span data-stu-id="cc7ae-138">at</span></span>

<span data-ttu-id="cc7ae-139">Microsoft. RTC. Management. SyntheticTransactions. SipSyntheticTransaction. TryRetri</span><span class="sxs-lookup"><span data-stu-id="cc7ae-139">Microsoft.Rtc.Management.SyntheticTransactions.SipSyntheticTransaction.TryRetri</span></span>

<span data-ttu-id="cc7ae-140">eveRegistrarPortFromTopology (Int32& registrarPortNumber)</span><span class="sxs-lookup"><span data-stu-id="cc7ae-140">eveRegistrarPortFromTopology(Int32& registrarPortNumber)</span></span>

<span data-ttu-id="cc7ae-141">Целевое полное доменное имя: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="cc7ae-141">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="cc7ae-142">Результат: сбой</span><span class="sxs-lookup"><span data-stu-id="cc7ae-142">Result : Failure</span></span>

<span data-ttu-id="cc7ae-143">Задержка: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="cc7ae-143">Latency : 00:00:00</span></span>

<span data-ttu-id="cc7ae-144">Сообщение об ошибке: 10060, не удалось установить соединение из-за того, что подключенная сторона</span><span class="sxs-lookup"><span data-stu-id="cc7ae-144">Error Message : 10060, A connection attempt failed because the connected party</span></span>

<span data-ttu-id="cc7ae-145">не отвечает на запросы в течение определенного периода времени или</span><span class="sxs-lookup"><span data-stu-id="cc7ae-145">did not properly respond after a period of time, or</span></span>

<span data-ttu-id="cc7ae-146">не удалось установить соединение, так как подключенный узел имеет</span><span class="sxs-lookup"><span data-stu-id="cc7ae-146">established connection failed because connected host has</span></span>

<span data-ttu-id="cc7ae-147">не удалось ответить на \[ 2001:4898: E8: f39e: 5c9a: ad83:81b3:9944: \] 5061</span><span class="sxs-lookup"><span data-stu-id="cc7ae-147">failed to respond \[2001:4898:e8:f39e:5c9a:ad83:81b3:9944\]:5061</span></span>

<span data-ttu-id="cc7ae-148">Внутреннее исключение: сбой при попытке подключения из-за того, что</span><span class="sxs-lookup"><span data-stu-id="cc7ae-148">Inner Exception:A connection attempt failed because the</span></span>

<span data-ttu-id="cc7ae-149">связь с абонентом завершилась неправильно после определенного периода</span><span class="sxs-lookup"><span data-stu-id="cc7ae-149">connected party did not properly respond after a period of</span></span>

<span data-ttu-id="cc7ae-150">время или соединение не удалось установить, так как подключенный узел</span><span class="sxs-lookup"><span data-stu-id="cc7ae-150">time, or established connection failed because connected host</span></span>

<span data-ttu-id="cc7ae-151">не отвечает</span><span class="sxs-lookup"><span data-stu-id="cc7ae-151">has failed to respond</span></span>

<span data-ttu-id="cc7ae-152">\[2001:4898: E8: f39e: 5c9a: ad83:81b3:9944 \] : 5061</span><span class="sxs-lookup"><span data-stu-id="cc7ae-152">\[2001:4898:e8:f39e:5c9a:ad83:81b3:9944\]:5061</span></span>

<span data-ttu-id="cc7ae-153">Диагностик</span><span class="sxs-lookup"><span data-stu-id="cc7ae-153">Diagnosis :</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="cc7ae-154">Причины, по которым может произойти сбой теста</span><span class="sxs-lookup"><span data-stu-id="cc7ae-154">Reasons why the test might have failed</span></span>

<span data-ttu-id="cc7ae-155">Ниже приведены некоторые распространенные причины, по которым может произойти сбой **Test-CsPersistentChatMessage** :</span><span class="sxs-lookup"><span data-stu-id="cc7ae-155">Here are some common reasons why **Test-CsPersistentChatMessage** might fail:</span></span>

  - <span data-ttu-id="cc7ae-156">Предоставлено неправильное значение параметра.</span><span class="sxs-lookup"><span data-stu-id="cc7ae-156">An incorrect parameter value was supplied.</span></span> <span data-ttu-id="cc7ae-157">Возможно, необходимые проверочные учетные записи не существуют или созданы неправильно.</span><span class="sxs-lookup"><span data-stu-id="cc7ae-157">The required test accounts may not exist or have been correctly created.</span></span>

  - <span data-ttu-id="cc7ae-158">Возможно, возникла проблема с сетью, вызывающая непредвиденную задержку, из-за которой истекло время выполнения теста.</span><span class="sxs-lookup"><span data-stu-id="cc7ae-158">There may have been a network issue causing an unexpected delay which timed out the test.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="cc7ae-159">См. также</span><span class="sxs-lookup"><span data-stu-id="cc7ae-159">See Also</span></span>


[<span data-ttu-id="cc7ae-160">Grant-CsPersistentChatPolicy</span><span class="sxs-lookup"><span data-stu-id="cc7ae-160">Grant-CsPersistentChatPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Grant-CsPersistentChatPolicy)  
[<span data-ttu-id="cc7ae-161">New-CsPersistentChatPolicy</span><span class="sxs-lookup"><span data-stu-id="cc7ae-161">New-CsPersistentChatPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsPersistentChatPolicy)  
[<span data-ttu-id="cc7ae-162">Set-CsPersistentChatPolicy</span><span class="sxs-lookup"><span data-stu-id="cc7ae-162">Set-CsPersistentChatPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsPersistentChatPolicy)  
  

<span data-ttu-id="cc7ae-163"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cc7ae-163"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

