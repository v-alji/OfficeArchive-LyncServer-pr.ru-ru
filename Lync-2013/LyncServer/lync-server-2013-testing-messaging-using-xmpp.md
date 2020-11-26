---
title: 'Lync Server 2013: тестирование сообщений с помощью XMPP'
description: 'Lync Server 2013: тестирование сообщений с помощью XMPP.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing messaging using XMPP
ms:assetid: ae5305ba-e5fc-4ca0-a805-872b4ebaf981
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn727312(v=OCS.15)
ms:contentKeyID: 63969641
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 06faeae0a6104351f9102de31c76b2424a140deb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441006"
---
# <a name="testing-messaging-using-xmpp-in-lync-server-2013"></a><span data-ttu-id="4ce0e-103">Тестирование сообщений с помощью XMPP в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4ce0e-103">Testing messaging using XMPP in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4ce0e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4ce0e-104">

<span> </span></span></span>

<span data-ttu-id="4ce0e-105">_**Тема последнего изменения:** 2014-11-03_</span><span class="sxs-lookup"><span data-stu-id="4ce0e-105">_**Topic Last Modified:** 2014-11-03_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4ce0e-106">Расписание проверки</span><span class="sxs-lookup"><span data-stu-id="4ce0e-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="4ce0e-107">Ежедневно</span><span class="sxs-lookup"><span data-stu-id="4ce0e-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ce0e-108">Средство тестирования</span><span class="sxs-lookup"><span data-stu-id="4ce0e-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="4ce0e-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="4ce0e-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ce0e-110">Требуемые разрешения</span><span class="sxs-lookup"><span data-stu-id="4ce0e-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="4ce0e-111">При локальном запуске с помощью командной консоли Lync Server пользователи должны быть членами группы безопасности RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="4ce0e-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="4ce0e-112">При запуске с помощью удаленного экземпляра Windows PowerShell пользователям должна быть назначена роль RBAC, имеющая разрешение на запуск командлета <strong>Test-CsXmppIM</strong> .</span><span class="sxs-lookup"><span data-stu-id="4ce0e-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the <strong>Test-CsXmppIM</strong> cmdlet.</span></span> <span data-ttu-id="4ce0e-113">Чтобы просмотреть список всех ролей RBAC, которые могут использовать этот командлет, выполните в командной строке Windows PowerShell следующую команду:</span><span class="sxs-lookup"><span data-stu-id="4ce0e-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsXmppIM&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="4ce0e-114">Описание</span><span class="sxs-lookup"><span data-stu-id="4ce0e-114">Description</span></span>

<span data-ttu-id="4ce0e-115">Расширенный протокол обмена сообщениями (XMPP) является стандартным протоколом связи (на основе XML), который используется для отправки сообщений через Интернет.</span><span class="sxs-lookup"><span data-stu-id="4ce0e-115">The Extensible Messaging and Presence Protocol (XMPP) is a standard communications protocol (based on XML) used for sending messages across the Internet.</span></span> <span data-ttu-id="4ce0e-116">XMPP первоначально назывался Jabber и поддерживается несколькими приложениями для обмена сообщениями в Интернете и общения, например с помощью Google чата и Facebook.</span><span class="sxs-lookup"><span data-stu-id="4ce0e-116">XMPP was originally named Jabber, and is supported by several Internet messaging and communication applications, such as Google Talk and Facebook Chat.</span></span> <span data-ttu-id="4ce0e-117">Командлет **Test-CsXmppIM** подтверждает, что пользователь может обмениваться мгновенными сообщениями с пользователем в сети XMPP.</span><span class="sxs-lookup"><span data-stu-id="4ce0e-117">The **Test-CsXmppIM** cmdlet verifies that a user can exchange instant messages with a user on an XMPP network.</span></span> <span data-ttu-id="4ce0e-118">Обратите внимание, что для успешного завершения этого теста необходимо иметь действительный SIP-адрес для пользователя XMPP, и этот адрес SIP должен находиться в сети, которая была настроена как разрешенная XMPP партнер.</span><span class="sxs-lookup"><span data-stu-id="4ce0e-118">Note that, for this test to succeed, you must have a valid SIP address for the XMPP user, and that SIP address must be on a network that was configured as an allowed XMPP partner.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="4ce0e-119">Выполнение теста</span><span class="sxs-lookup"><span data-stu-id="4ce0e-119">Running the test</span></span>

<span data-ttu-id="4ce0e-120">В следующем примере проверяются возможности обмена мгновенными сообщениями XMPP для atl-cs-001.litwareinc.com пула.</span><span class="sxs-lookup"><span data-stu-id="4ce0e-120">The following example verifies the XMPP instant messaging capabilities for the pool atl-cs-001.litwareinc.com.</span></span> <span data-ttu-id="4ce0e-121">Эта команда будет работать только в том случае, если тестовые пользователи определены для пула atl-cs-001.litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="4ce0e-121">This command will work only if test users are defined for the pool atl-cs-001.litwareinc.com.</span></span> <span data-ttu-id="4ce0e-122">Если это так, команда определит, может ли первый тестовый пользователь отправить мгновенное сообщение XMPP пользователю с адресом SIP adelaney@contoso.com.</span><span class="sxs-lookup"><span data-stu-id="4ce0e-122">If they have, then the command will determine whether the first test user can send an XMPP instant message to a user who has the SIP address adelaney@contoso.com.</span></span>

<span data-ttu-id="4ce0e-123">Если тестовые пользователи не заданы, команда завершится сбоем, так как не будет определять, какой пользователь должен войти в систему.</span><span class="sxs-lookup"><span data-stu-id="4ce0e-123">If test users are not defined, then the command will fail because it won't know which user to log on as.</span></span> <span data-ttu-id="4ce0e-124">Если вы не определили тестовых пользователей для пула, необходимо включить параметр UserSipAddress и учетные данные пользователя, который должна использовать команда при попытке входа в систему.</span><span class="sxs-lookup"><span data-stu-id="4ce0e-124">If you have not defined test users for a pool, then you must include the UserSipAddress parameter and the credentials of the user who the command should use when trying to log on.</span></span>

    Test-CsXmppIM -TargetFqdn "atl-cs-001.litwareinc.com" -Receiver "adelany@contoso.com"

<span data-ttu-id="4ce0e-125">Команды, показанные в следующем примере, проверяют возможность определенного пользователя (плана litwareinc \\ почтового) войти в систему для отправки XMPP мгновенного сообщения пользователю adelaney@contoso.com.</span><span class="sxs-lookup"><span data-stu-id="4ce0e-125">The commands shown in the next example test the ability of a specific user (litwareinc\\pilar) to log on to send an XMPP instant message to the user adelaney@contoso.com.</span></span> <span data-ttu-id="4ce0e-126">Для этого в первой команде примера используется командлет Get-Credential, чтобы создать объект учетных данных интерфейса командной строки Windows PowerShell, содержащий имя и пароль пользователя почтового Вронский.</span><span class="sxs-lookup"><span data-stu-id="4ce0e-126">To do this, the first command in the example uses the Get-Credential cmdlet to create a Windows PowerShell command-line interface credential object that contains the name and password of the user Pilar Ackerman.</span></span> <span data-ttu-id="4ce0e-127">(Поскольку имя для входа в плана litwareinc \\ почтового было включено в качестве параметра, в диалоговом окне Запрос учетных данных Windows PowerShell требуется, чтобы администратор введет пароль для учетной записи почтового Вронский). Полученный объект учетных данных затем сохраняется в переменной с именем $cred 1.</span><span class="sxs-lookup"><span data-stu-id="4ce0e-127">(Because the logon name litwareinc\\pilar was included as a parameter, the Windows PowerShell Credential Request dialog box only requires the administrator to enter the password for the Pilar Ackerman account.) The resulting credential object is then stored in a variable named $cred1.</span></span>

<span data-ttu-id="4ce0e-128">Вторая команда проверяет, может ли пользователь войти в atl-cs-001.litwareinc.com пула и отправить мгновенное сообщение XMPP.</span><span class="sxs-lookup"><span data-stu-id="4ce0e-128">The second command then checks whether this user can log on to the pool atl-cs-001.litwareinc.com and send the XMPP instant message.</span></span> <span data-ttu-id="4ce0e-129">Для выполнения этой задачи вызывается командлет **Test-CsXmppIm** , вместе с четырьмя параметрами: TargetFqdn (полное доменное имя пула регистраторов). Получатель (адрес SIP пользователя, которому адресовано сообщение); UserCredential (объект Windows PowerShell, который включает в себя учетные данные пользователя для почтового Вронский); и UserSipAddress (SIP-адрес, соответствующий предоставленным учетным данным пользователя).</span><span class="sxs-lookup"><span data-stu-id="4ce0e-129">To run this task, the **Test-CsXmppIm** cmdlet is called, together with four parameters: TargetFqdn (the FQDN of the Registrar pool); Receiver (the SIP address of the user the message is being addressed to); UserCredential (the Windows PowerShell object that contains Pilar Ackerman’s user credentials); and UserSipAddress (the SIP address that corresponds to the supplied user credentials).</span></span>

    $credential = Get-Credential "litwareinc\kenmyer"
    
    Test-CsXmppIM -TargetFqdn "atl-cs-001.litwareinc.com" -Receiver "adelany@contoso.com" -UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="4ce0e-130">Определение успеха или сбоя</span><span class="sxs-lookup"><span data-stu-id="4ce0e-130">Determining success or failure</span></span>

<span data-ttu-id="4ce0e-131">Если XMPP обмен мгновенными сообщениями правильно настроен, вы получите вывод примерно так, чтобы свойство Result пометило **"успешно".**</span><span class="sxs-lookup"><span data-stu-id="4ce0e-131">If XMPP instant messaging is correctly configured, you'll receive output similar to this, with the Result property marked as **Success:**</span></span>

<span data-ttu-id="4ce0e-132">Целевое полное доменное имя: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="4ce0e-132">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="4ce0e-133">Результат: успех</span><span class="sxs-lookup"><span data-stu-id="4ce0e-133">Result : Success</span></span>

<span data-ttu-id="4ce0e-134">Задержка: 00:00:02.5361946</span><span class="sxs-lookup"><span data-stu-id="4ce0e-134">Latency : 00:00:02.5361946</span></span>

<span data-ttu-id="4ce0e-135">Сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="4ce0e-135">Error Message :</span></span>

<span data-ttu-id="4ce0e-136">Диагностик</span><span class="sxs-lookup"><span data-stu-id="4ce0e-136">Diagnosis :</span></span>

<span data-ttu-id="4ce0e-137">Если указанные пользователи не могут использовать XMPP обмен мгновенными сообщениями, результат будет показан как **сбой**, а дополнительные сведения будут записаны в свойствах Error и диагноз.</span><span class="sxs-lookup"><span data-stu-id="4ce0e-137">If the specified users can't use XMPP instant messaging, the Result will be shown as **Failure**, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="4ce0e-138">Предупреждение: не удалось прочитать номер порта регистратора для заданного полного имени</span><span class="sxs-lookup"><span data-stu-id="4ce0e-138">WARNING: Failed to read Registrar port number for the given fully qualified</span></span>

<span data-ttu-id="4ce0e-139">доменное имя (FQDN).</span><span class="sxs-lookup"><span data-stu-id="4ce0e-139">domain name (FQDN).</span></span> <span data-ttu-id="4ce0e-140">С помощью номера порта регистратора по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4ce0e-140">Using default Registrar port number.</span></span> <span data-ttu-id="4ce0e-141">Ошибка</span><span class="sxs-lookup"><span data-stu-id="4ce0e-141">Exception:</span></span>

<span data-ttu-id="4ce0e-142">System. InvalidOperationException: в топологии не обнаружены подходящие кластеры.</span><span class="sxs-lookup"><span data-stu-id="4ce0e-142">System.InvalidOperationException: No matching cluster found in topology.</span></span>

<span data-ttu-id="4ce0e-143">скорость</span><span class="sxs-lookup"><span data-stu-id="4ce0e-143">at</span></span>

<span data-ttu-id="4ce0e-144">Microsoft. RTC. Management. SyntheticTransactions. SipSyntheticTransaction. TryRetri</span><span class="sxs-lookup"><span data-stu-id="4ce0e-144">Microsoft.Rtc.Management.SyntheticTransactions.SipSyntheticTransaction.TryRetri</span></span>

<span data-ttu-id="4ce0e-145">eveRegistrarPortFromTopology (Int32& registrarPortNumber)</span><span class="sxs-lookup"><span data-stu-id="4ce0e-145">eveRegistrarPortFromTopology(Int32& registrarPortNumber)</span></span>

<span data-ttu-id="4ce0e-146">Целевое полное доменное имя: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="4ce0e-146">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="4ce0e-147">Результат: сбой</span><span class="sxs-lookup"><span data-stu-id="4ce0e-147">Result : Failure</span></span>

<span data-ttu-id="4ce0e-148">Задержка: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="4ce0e-148">Latency : 00:00:00</span></span>

<span data-ttu-id="4ce0e-149">Сообщение об ошибке: 10060, не удалось установить соединение из-за того, что подключенная сторона</span><span class="sxs-lookup"><span data-stu-id="4ce0e-149">Error Message : 10060, A connection attempt failed because the connected party</span></span>

<span data-ttu-id="4ce0e-150">не отвечает на запросы в течение определенного периода времени или</span><span class="sxs-lookup"><span data-stu-id="4ce0e-150">did not properly respond after a period of time, or</span></span>

<span data-ttu-id="4ce0e-151">не удалось установить соединение, так как подключенный узел имеет</span><span class="sxs-lookup"><span data-stu-id="4ce0e-151">established connection failed because connected host has</span></span>

<span data-ttu-id="4ce0e-152">не удалось ответить на 10.188.116.96:5061</span><span class="sxs-lookup"><span data-stu-id="4ce0e-152">failed to respond 10.188.116.96:5061</span></span>

<span data-ttu-id="4ce0e-153">Внутреннее исключение: сбой при попытке подключения из-за того, что</span><span class="sxs-lookup"><span data-stu-id="4ce0e-153">Inner Exception:A connection attempt failed because the</span></span>

<span data-ttu-id="4ce0e-154">связь с абонентом завершилась неправильно после определенного периода</span><span class="sxs-lookup"><span data-stu-id="4ce0e-154">connected party did not properly respond after a period of</span></span>

<span data-ttu-id="4ce0e-155">время или соединение не удалось установить, так как подключенный узел</span><span class="sxs-lookup"><span data-stu-id="4ce0e-155">time, or established connection failed because connected host</span></span>

<span data-ttu-id="4ce0e-156">не удалось ответить 10.188.116.96:5061</span><span class="sxs-lookup"><span data-stu-id="4ce0e-156">has failed to respond 10.188.116.96:5061</span></span>

<span data-ttu-id="4ce0e-157">Диагностик</span><span class="sxs-lookup"><span data-stu-id="4ce0e-157">Diagnosis :</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="4ce0e-158">Причины, по которым может произойти сбой теста</span><span class="sxs-lookup"><span data-stu-id="4ce0e-158">Reasons why the test might have failed</span></span>

<span data-ttu-id="4ce0e-159">Ниже приведены некоторые распространенные причины, по которым может произойти сбой **Test-CsXmppIM** :</span><span class="sxs-lookup"><span data-stu-id="4ce0e-159">Here are some common reasons why **Test-CsXmppIM** might fail:</span></span>

  - <span data-ttu-id="4ce0e-160">Предоставлено неправильное значение параметра.</span><span class="sxs-lookup"><span data-stu-id="4ce0e-160">An incorrect parameter value was supplied.</span></span> <span data-ttu-id="4ce0e-161">Если используется, необязательные параметры необходимо настроить правильно, или тест завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="4ce0e-161">If used, the optional parameters must be configured correctly or the test will fail.</span></span> <span data-ttu-id="4ce0e-162">Повторите выполнение команды без дополнительных параметров и проверьте, выполняется ли это успешно.</span><span class="sxs-lookup"><span data-stu-id="4ce0e-162">Rerun the command without the optional parameters and see whether that succeeds.</span></span>

  - <span data-ttu-id="4ce0e-163">Эта команда завершится сбоем, если конфигурация шлюза XMPP неправильно настроена или еще не развернута.</span><span class="sxs-lookup"><span data-stu-id="4ce0e-163">This command will fail if XMPP gateway configuration is misconfigured or not yet deployed.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="4ce0e-164">См. также</span><span class="sxs-lookup"><span data-stu-id="4ce0e-164">See Also</span></span>


[<span data-ttu-id="4ce0e-165">Set-CsXmppGatewayConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ce0e-165">Set-CsXmppGatewayConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsXmppGatewayConfiguration)  
  

<span data-ttu-id="4ce0e-166"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4ce0e-166"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

