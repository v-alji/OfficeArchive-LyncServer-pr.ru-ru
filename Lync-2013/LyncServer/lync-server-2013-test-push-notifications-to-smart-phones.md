---
title: 'Lync Server 2013: тестирование push-уведомлений на Интеллектуальные телефоны'
description: 'Lync Server 2013: тестирование push-уведомлений на Интеллектуальные телефоны.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test push notifications to smart phones
ms:assetid: 8f5ca7d1-1ccb-4cb0-b417-730559e79b6e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn767948(v=OCS.15)
ms:contentKeyID: 63969626
ms.date: 03/15/2017
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4b92ef444a5331c9a673fd2db506631554e96eea
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441230"
---
# <a name="test-push-notifications-to-smart-phones-in-lync-server-2013"></a><span data-ttu-id="adcf3-103">Тестирование push-уведомлений на смартфоны в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="adcf3-103">Test push notifications to smart phones in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="adcf3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="adcf3-104">

<span> </span></span></span>

<span data-ttu-id="adcf3-105">_**Тема последнего изменения:** 2017-03-15_</span><span class="sxs-lookup"><span data-stu-id="adcf3-105">_**Topic Last Modified:** 2017-03-15_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="adcf3-106">Расписание проверки</span><span class="sxs-lookup"><span data-stu-id="adcf3-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="adcf3-107">Ежемесячно</span><span class="sxs-lookup"><span data-stu-id="adcf3-107">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adcf3-108">Средство тестирования</span><span class="sxs-lookup"><span data-stu-id="adcf3-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="adcf3-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="adcf3-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adcf3-110">Требуемые разрешения</span><span class="sxs-lookup"><span data-stu-id="adcf3-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="adcf3-111">При локальном запуске с помощью командной консоли Lync Server пользователи должны быть членами группы безопасности RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="adcf3-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="adcf3-112">При запуске с помощью удаленного экземпляра Windows PowerShell пользователям должна быть назначена роль RBAC, имеющая разрешение на запуск командлета Test-CsMcxPushNotification.</span><span class="sxs-lookup"><span data-stu-id="adcf3-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsMcxPushNotification cmdlet.</span></span> <span data-ttu-id="adcf3-113">Чтобы просмотреть список всех ролей RBAC, которые могут использовать этот командлет, выполните в командной строке Windows PowerShell следующую команду:</span><span class="sxs-lookup"><span data-stu-id="adcf3-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsMcxPushNotification&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="adcf3-114">Описание</span><span class="sxs-lookup"><span data-stu-id="adcf3-114">Description</span></span>

<span data-ttu-id="adcf3-115">Служба push-уведомлений Apple и Служба push-уведомлений Майкрософт может отправлять уведомления о событиях, например о новых мгновенных сообщениях или голосовой почте на мобильных устройствах, таких как iPhone и телефоны Windows, даже если клиент Lync на этих устройствах в настоящее время приостановлен или работает в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="adcf3-115">The push notification service (Apple Push Notification Service and Microsoft Push Notification Service) can send notifications about events such as new instant messages or new voice mail to mobile devices such as iPhones and Windows Phones, even if the Lync client on those devices is currently suspended or running in the background.</span></span> <span data-ttu-id="adcf3-116">Служба push-уведомлений — это облачная служба, выполняемая на серверах Microsoft.</span><span class="sxs-lookup"><span data-stu-id="adcf3-116">The push notification service is a cloud-based service that is running on Microsoft servers.</span></span> <span data-ttu-id="adcf3-117">Чтобы воспользоваться преимуществами push-уведомлений, вы должны иметь возможность подключения и проверки подлинности с помощью службы push-уведомлений.</span><span class="sxs-lookup"><span data-stu-id="adcf3-117">In order to take advantage of push notifications, you must be able to connect to, and be authenticated by, the push notification clearinghouse.</span></span> <span data-ttu-id="adcf3-118">Командлет Test-CsMcxPushNotification позволяет администраторам убедиться, что запросы push-уведомлений могут маршрутизироваться через пограничный сервер в расчетную палату push-уведомлений.</span><span class="sxs-lookup"><span data-stu-id="adcf3-118">The Test-CsMcxPushNotification cmdlet enables administrators to verify that push notification requests can be routed through your Edge server to the push notification clearinghouse.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="adcf3-119">Выполнение теста</span><span class="sxs-lookup"><span data-stu-id="adcf3-119">Running the test</span></span>

<span data-ttu-id="adcf3-120">Чтобы протестировать службу push-уведомлений, вызовите командлет Test-CsMcxPushNotification.</span><span class="sxs-lookup"><span data-stu-id="adcf3-120">To test the push notification service, call the Test-CsMcxPushNotification cmdlet.</span></span> <span data-ttu-id="adcf3-121">Убедитесь, что вы указали полное доменное имя пограничного сервера:</span><span class="sxs-lookup"><span data-stu-id="adcf3-121">Make sure that you specify the fully qualified domain name of your Edge server:</span></span>

    Test-CsMcxPushNotification -AccessEdgeFqdn "atl-edge-001.litwareinc.com"

<span data-ttu-id="adcf3-122">Дополнительные сведения можно найти в разделе справки по командлету [Test-CsMcxPushNotification](https://docs.microsoft.com/powershell/module/skype/Test-CsMcxPushNotification) .</span><span class="sxs-lookup"><span data-stu-id="adcf3-122">For more information, see the help topic for the [Test-CsMcxPushNotification](https://docs.microsoft.com/powershell/module/skype/Test-CsMcxPushNotification) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="adcf3-123">Определение успеха или сбоя</span><span class="sxs-lookup"><span data-stu-id="adcf3-123">Determining success or failure</span></span>

<span data-ttu-id="adcf3-124">Если Test-CsMcxPushNotification успешное выполнение командлета, будет возвращено результат теста:</span><span class="sxs-lookup"><span data-stu-id="adcf3-124">If Test-CsMcxPushNotification succeeds the cmdlet will return the test result Success:</span></span>

<span data-ttu-id="adcf3-125">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="adcf3-125">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="adcf3-126">Результат: успех</span><span class="sxs-lookup"><span data-stu-id="adcf3-126">Result : Success</span></span>

<span data-ttu-id="adcf3-127">Задержка: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="adcf3-127">Latency : 00:00:00</span></span>

<span data-ttu-id="adcf3-128">Ошибки</span><span class="sxs-lookup"><span data-stu-id="adcf3-128">Error :</span></span>

<span data-ttu-id="adcf3-129">Диагностик</span><span class="sxs-lookup"><span data-stu-id="adcf3-129">Diagnosis :</span></span>

<span data-ttu-id="adcf3-130">Если Test-CsMcxPushNotification не удается подключиться к расчетной палате push-уведомлений, этот командлет обычно не возвращает результат теста "сбой".</span><span class="sxs-lookup"><span data-stu-id="adcf3-130">If Test-CsMcxPushNotification is unable to connect to the push notification clearinghouse the cmdlet will typically not return a test result of Failure.</span></span> <span data-ttu-id="adcf3-131">Вместо этого, как правило, команда завершается сбоем.</span><span class="sxs-lookup"><span data-stu-id="adcf3-131">Instead the command will usually fail completely.</span></span> <span data-ttu-id="adcf3-132">Например:</span><span class="sxs-lookup"><span data-stu-id="adcf3-132">For example:</span></span>

<span data-ttu-id="adcf3-133">Test-CsMcxPushNotification: ответ 504 (время ожидания сервера), полученный от сети, не прошел операцию.</span><span class="sxs-lookup"><span data-stu-id="adcf3-133">Test-CsMcxPushNotification : A 504 (Server time-out) response was received from the network and the operation failed.</span></span> <span data-ttu-id="adcf3-134">Дополнительные сведения приведены в разделе сведения об исключении.</span><span class="sxs-lookup"><span data-stu-id="adcf3-134">See the exception details for more information.</span></span>

<span data-ttu-id="adcf3-135">В строке: 1 символ: 27</span><span class="sxs-lookup"><span data-stu-id="adcf3-135">At line:1 char:27</span></span>

<span data-ttu-id="adcf3-136">\+Test-CsMcxPushNotification \< \< \< \< AccessEdgeFqdn lyncedge.mydomain.com</span><span class="sxs-lookup"><span data-stu-id="adcf3-136">\+ Test-CsMcxPushNotification \<\<\<\< -AccessEdgeFqdn lyncedge.mydomain.com</span></span>

<span data-ttu-id="adcf3-137">\+ CategoryInfo: OperationStopped: (:) \[ Test-CsMcxPushNotification \] , FailureResponseException</span><span class="sxs-lookup"><span data-stu-id="adcf3-137">\+ CategoryInfo : OperationStopped: (:) \[Test-CsMcxPushNotification\], FailureResponseException</span></span>

<span data-ttu-id="adcf3-138">\+ FullyQualifiedErrorId: WorkflowNotCompleted, Microsoft. RTC. Management. SyntheticTransactions. TestMcxPushNotificationCmdlet</span><span class="sxs-lookup"><span data-stu-id="adcf3-138">\+ FullyQualifiedErrorId : WorkflowNotCompleted,Microsoft.Rtc.Management.SyntheticTransactions.TestMcxPushNotificationCmdlet</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="adcf3-139">Причины, по которым может произойти сбой теста</span><span class="sxs-lookup"><span data-stu-id="adcf3-139">Reasons why the test might have failed</span></span>

<span data-ttu-id="adcf3-140">Если происходит сбой службы push-уведомлений, которая обычно указывает на наличие проблем с подключением пограничного сервера или проблем с подключением к клирингового отсоединению push-уведомлений.</span><span class="sxs-lookup"><span data-stu-id="adcf3-140">If the push notification service fails that usually indicates either problems communicating with your Edge server, or problems communicating with the Push Notification Clearing House.</span></span> <span data-ttu-id="adcf3-141">Если при выполнении теста-CsMcxPushNotification возникли проблемы, необходимо убедиться, что пограничный сервер работает правильно.</span><span class="sxs-lookup"><span data-stu-id="adcf3-141">If you encounter problems when you run Test-CsMcxPushNotification, the first thing that you should do is verify that your Edge server is working correctly.</span></span> <span data-ttu-id="adcf3-142">Один из способов сделать это — использовать командлет Test-CsAVEdgeConnectivity:</span><span class="sxs-lookup"><span data-stu-id="adcf3-142">One way to do that is to use the Test-CsAVEdgeConnectivity cmdlet:</span></span>

    $credential = Get-Credential "litwareinc\kenmyer"
    
    Test-CsAVEdgeConnectivity -TargetFqdn "atl-cs-001.litwareinc.com" -UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential

<span data-ttu-id="adcf3-143">Эта проверка удостоверяет, что указанный пользователь может подключаться к пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="adcf3-143">This check verifies that a specified user can connect to the Edge server.</span></span>

<span data-ttu-id="adcf3-144">Если пограничный сервер работает правильно, это часто означает, что вы не можете подключиться к расчетной палате push-уведомлений.</span><span class="sxs-lookup"><span data-stu-id="adcf3-144">If the Edge server seems to be working correctly, that often means that you are unable to connect to the push notification clearinghouse.</span></span> <span data-ttu-id="adcf3-145">В свою очередь, обычно это означает, что вы неправильно настроили URI расчетной палаты или не обладаете DNS SRV-записью, указывающей на этот URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="adcf3-145">In turn, that typically means that you either have not configured the clearinghouse URI correctly or that you do not have a DNS SRV record that points to this URL.</span></span> <span data-ttu-id="adcf3-146">Вы можете проверить, правильно ли задано значение универсального кода ресурса (sip:push@push.lync.com), выполнив следующую команду:</span><span class="sxs-lookup"><span data-stu-id="adcf3-146">You can verify that the URI is set to the correct value (sip:push@push.lync.com) by running this command:</span></span>

    Get-CsMcxConfiguration

<span data-ttu-id="adcf3-147">Если для свойства PushNotificationProxyUri задано значение, отличное от sip:push@push.lync.com, то эту проблему можно устранить с помощью командлета Set-McxConfiguration.</span><span class="sxs-lookup"><span data-stu-id="adcf3-147">If the PushNotificationProxyUri property is set to anything other than sip:push@push.lync.com then you can correct that problem by using the Set-McxConfiguration cmdlet.</span></span> <span data-ttu-id="adcf3-148">Например, эта команда правильно задает универсальный код ресурса (URI) для всей Организации.</span><span class="sxs-lookup"><span data-stu-id="adcf3-148">For example, this command correctly sets the URI throughout your organization:</span></span>

    Get-CsMcxConfiguration | Set-CsMcxConfiguration -PushNotificationProxyUri "sip:push@push.lync.com"

<span data-ttu-id="adcf3-149">Дополнительные сведения можно найти в разделе справки по командлету [Set-CsMcxConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsMcxConfiguration) .</span><span class="sxs-lookup"><span data-stu-id="adcf3-149">For more information, see the help topic for the [Set-CsMcxConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsMcxConfiguration) cmdlet.</span></span>

<span data-ttu-id="adcf3-150">Если универсальный код ресурса (URI) настроен правильно, необходимо убедиться в том, что у вас есть DNS SRV-запись, которая разрешается для вашего домена SIP и пограничного сервера.</span><span class="sxs-lookup"><span data-stu-id="adcf3-150">If the URI is configured correctly, your next step should be to verify that you have a DNS SRV record that resolves to your SIP domain and your Edge server.</span></span> <span data-ttu-id="adcf3-151">Дополнительные сведения о том, как настроить эти записи, можно найти в разделе справки требования к DNS для мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="adcf3-151">For more information about how to configure these records, see the help topic DNS Requirements for Mobility.</span></span> <span data-ttu-id="adcf3-152">Обратите внимание, что следующее сообщение об ошибке обычно указывает на проблему с DNS-записями.</span><span class="sxs-lookup"><span data-stu-id="adcf3-152">Note that the following error message usually indicates a problem with DNS records:</span></span>

<span data-ttu-id="adcf3-153">Ответ 504 (время ожидания сервера), полученный от сети, не прошел операцию.</span><span class="sxs-lookup"><span data-stu-id="adcf3-153">A 504 (Server time-out) response was received from the network and the operation failed.</span></span> <span data-ttu-id="adcf3-154">Дополнительные сведения приведены в разделе сведения об исключении.</span><span class="sxs-lookup"><span data-stu-id="adcf3-154">See the exception details for more information.</span></span>

<span data-ttu-id="adcf3-155">Возможно также, что Test-CsMcxConfiguration завершится сбоем с сообщением об ошибке:</span><span class="sxs-lookup"><span data-stu-id="adcf3-155">It’s also possible that Test-CsMcxConfiguration will fail with this error message:</span></span>

<span data-ttu-id="adcf3-156">Test-CsMcxPushNotification: запрос push-уведомления отклонен.</span><span class="sxs-lookup"><span data-stu-id="adcf3-156">Test-CsMcxPushNotification : Push Notification request was rejected.</span></span>

<span data-ttu-id="adcf3-157">В строке: 1 символ: 27</span><span class="sxs-lookup"><span data-stu-id="adcf3-157">At line:1 char:27</span></span>

<span data-ttu-id="adcf3-158">\+ Test-CsMcxPushNotification \<\<\<\<</span><span class="sxs-lookup"><span data-stu-id="adcf3-158">\+ Test-CsMcxPushNotification \<\<\<\<</span></span>

<span data-ttu-id="adcf3-159">\+ CategoryInfo: OperationStopped: (:) \[ Test-CsMcxPushNotification \] , SyntheticTransactionException</span><span class="sxs-lookup"><span data-stu-id="adcf3-159">\+ CategoryInfo : OperationStopped: (:) \[Test-CsMcxPushNotification\], SyntheticTransactionException</span></span>

<span data-ttu-id="adcf3-160">\+ FullyQualifiedErrorId: WorkflowNotCompleted, Microsoft. RTC. Management. SyntheticTransactions. TestMcxPushNotificationCmdlet</span><span class="sxs-lookup"><span data-stu-id="adcf3-160">\+ FullyQualifiedErrorId : WorkflowNotCompleted,Microsoft.Rtc.Management.SyntheticTransactions.TestMcxPushNotificationCmdlet</span></span>

<span data-ttu-id="adcf3-161">Сообщение "запрос push-уведомлений отвергнуто" обычно происходит, если включена фильтрация URL-адресов и вы блокируете префиксы http: и HTTPS:.</span><span class="sxs-lookup"><span data-stu-id="adcf3-161">The “Push notification request was rejected” message typically occurs if you have enabled URL filtering and are blocking the http: and https: prefixes.</span></span> <span data-ttu-id="adcf3-162">Вы можете определить, какие префиксы блокируются, с помощью команды, подобной приведенной ниже:</span><span class="sxs-lookup"><span data-stu-id="adcf3-162">You can determine which prefixes are being blocked by using a command similar to the following:</span></span>

```PowerShell 
 (Get-CsImFilterConfiguration -Identity Global).Prefixes
```

<span data-ttu-id="adcf3-163">Если в результатах отображаются протоколы HTTP: или HTTPS, необходимо удалить их из списка блокируемых префиксов для использования push-уведомлений.</span><span class="sxs-lookup"><span data-stu-id="adcf3-163">If http: or https: appear in the results, you must remove them from the blocked prefix list for push notifications to work.</span></span> <span data-ttu-id="adcf3-164">Это можно сделать с помощью команд, сходных с приведенными ниже.</span><span class="sxs-lookup"><span data-stu-id="adcf3-164">That can be done by using commands similar to these:</span></span>

    Set-CsImFilterConfiguration -Identity site:Redmond -Prefixes @{remove="http:"}
    Set-CsImFilterConfiguration -Identity site:Redmond -Prefixes @{remove="https:"}

<span data-ttu-id="adcf3-165">Дополнительные сведения можно найти в разделе справки по командлету [Set-CsImFilterConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsImFilterConfiguration).</span><span class="sxs-lookup"><span data-stu-id="adcf3-165">For more information, see the help topic for the [Set-CsImFilterConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsImFilterConfiguration)cmdlet.</span></span>

<span data-ttu-id="adcf3-166"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="adcf3-166"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

