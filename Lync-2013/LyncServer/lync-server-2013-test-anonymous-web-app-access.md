---
title: 'Lync Server 2013: Проверка анонимного доступа к веб-приложению'
description: 'Lync Server 2013: Проверка анонимного доступа к веб-приложению.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test anonymous Web App access
ms:assetid: 92f691cd-e05e-4bab-beb5-251d4b837a19
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn767949(v=OCS.15)
ms:contentKeyID: 63969630
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 11c33840912fefcaeef069e14773cfefd0834a8b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441272"
---
# <a name="test-anonymous-web-app-access-in-lync-server-2013"></a><span data-ttu-id="5d6df-103">Проверка доступа анонимного веб-приложения в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5d6df-103">Test anonymous Web App access in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5d6df-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5d6df-104">

<span> </span></span></span>

<span data-ttu-id="5d6df-105">_**Тема последнего изменения:** 2014-06-07_</span><span class="sxs-lookup"><span data-stu-id="5d6df-105">_**Topic Last Modified:** 2014-06-07_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5d6df-106">Расписание проверки</span><span class="sxs-lookup"><span data-stu-id="5d6df-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="5d6df-107">Ежемесячно</span><span class="sxs-lookup"><span data-stu-id="5d6df-107">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d6df-108">Средство тестирования</span><span class="sxs-lookup"><span data-stu-id="5d6df-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="5d6df-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="5d6df-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d6df-110">Требуемые разрешения</span><span class="sxs-lookup"><span data-stu-id="5d6df-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="5d6df-111">При локальном запуске с помощью командной консоли Lync Server пользователи должны быть членами группы безопасности RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="5d6df-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="5d6df-112">При запуске с помощью удаленного экземпляра Windows PowerShell пользователям должна быть назначена роль RBAC, имеющая разрешение на запуск командлета Test-CsWebAppAnonymous.</span><span class="sxs-lookup"><span data-stu-id="5d6df-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsWebAppAnonymous cmdlet.</span></span> <span data-ttu-id="5d6df-113">Чтобы просмотреть список всех ролей RBAC, которые могут использовать этот командлет, выполните в командной строке Windows PowerShell следующую команду:</span><span class="sxs-lookup"><span data-stu-id="5d6df-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsWebAppAnonymous&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="5d6df-114">Описание</span><span class="sxs-lookup"><span data-stu-id="5d6df-114">Description</span></span>

<span data-ttu-id="5d6df-115">Командлет Test-CsWebAppAnonymous удостоверяется в том, что анонимный пользователь может присоединиться к конференциям Lync Server с помощью Lync Web App.</span><span class="sxs-lookup"><span data-stu-id="5d6df-115">The Test-CsWebAppAnonymous cmdlet verifies that an anonymous user can join Lync Server conferences by using the Lync Web App.</span></span> <span data-ttu-id="5d6df-116">Когда вы запускаете командлет, Test-CsWebAppAnonymous обращается к службе веб-билета для получения веб-билета для анонимного пользователя.</span><span class="sxs-lookup"><span data-stu-id="5d6df-116">When you run the cmdlet, Test-CsWebAppAnonymous contacts the Web Ticket service to obtain a web ticket for the anonymous user.</span></span> <span data-ttu-id="5d6df-117">Если командлету удалось получить этот билет, Test-CsWebAppAnonymous будет обращаться к Lync Server и попытаться установить отдельные конференции для обмена мгновенными сообщениями, общего обмена приложениями и совместной работы с данными.</span><span class="sxs-lookup"><span data-stu-id="5d6df-117">If the cmdlet succeeds in obtaining this ticket, Test-CsWebAppAnonymous will then contact Lync Server and attempt to establish separate conferences for instant messaging, application sharing, and data collaboration.</span></span>

<span data-ttu-id="5d6df-118">Обратите внимание, что Test-CsWebAppAnonymous только проверяет интерфейсы API и соединения, используемые для создания этих конференций.</span><span class="sxs-lookup"><span data-stu-id="5d6df-118">Note that Test-CsWebAppAnonymous only verifies the APIs and connections used to create these conferences.</span></span> <span data-ttu-id="5d6df-119">На самом деле командлеты не создают и не выполняют никакие Конференции.</span><span class="sxs-lookup"><span data-stu-id="5d6df-119">The cmdlet does not actually create and conduct any conferences.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="5d6df-120">Выполнение теста</span><span class="sxs-lookup"><span data-stu-id="5d6df-120">Running the test</span></span>

<span data-ttu-id="5d6df-121">Командлет Test-CsWebAppAnonymous можно выполнить с помощью пары предварительно настроенных тестовых учетных записей или учетных записей двух пользователей, которые включены в Lync Server.</span><span class="sxs-lookup"><span data-stu-id="5d6df-121">The Test-CsWebAppAnonymous cmdlet can be run using either a pair of preconfigured test accounts or the accounts of any two users who are enabled for Lync Server.</span></span> <span data-ttu-id="5d6df-122">Для выполнения этой проверки с помощью тестовых учетных записей нужно просто указать полное доменное имя для тестируемого пула сервера Lync Server.</span><span class="sxs-lookup"><span data-stu-id="5d6df-122">To run this check using test accounts, you just have to specify the fully qualified domain name of the Lync Server pool being tested.</span></span> <span data-ttu-id="5d6df-123">Например:</span><span class="sxs-lookup"><span data-stu-id="5d6df-123">For example:</span></span>

    Test-CsWebAppAnonymous -TargetFqdn atl-cs-001.litwareinc.com

<span data-ttu-id="5d6df-124">Для выполнения этой проверки с использованием фактических учетных записей пользователей необходимо создать два объекта учетных данных командной консоли Lync Server (объекты, содержащие имя и пароль учетной записи) для каждой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="5d6df-124">To run this check using actual user accounts, you must create two Lync Server Management Shell credentials objects (objects that contain the account name and password) for each account.</span></span> <span data-ttu-id="5d6df-125">После вызова Test-CsWebAppAnonymous вы должны добавить эти объекты учетных данных и адреса SIP для двух учетных записей.</span><span class="sxs-lookup"><span data-stu-id="5d6df-125">You must then include those credentials objects and the SIP addresses of the two accounts when you call Test-CsWebAppAnonymous:</span></span>

    $cred1 = Get-Credential "litwareinc\kenmyer"
    
    Test-CsWebApp -TargetFqdn atl-cs-001.litwareinc.com -UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $cred1

<span data-ttu-id="5d6df-126">Дополнительные сведения можно найти в разделе справки по командлету Test-CsWebAppAnonymous.</span><span class="sxs-lookup"><span data-stu-id="5d6df-126">For more information, see the help topic for the Test-CsWebAppAnonymous cmdlet.</span></span> <span data-ttu-id="5d6df-127">Обратите внимание, что Test-CsWebAppAnonymous не рекомендуется использовать в Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="5d6df-127">Note that Test-CsWebAppAnonymous is deprecated for use on Lync Server 2013.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="5d6df-128">Определение успеха или сбоя</span><span class="sxs-lookup"><span data-stu-id="5d6df-128">Determining success or failure</span></span>

<span data-ttu-id="5d6df-129">Если Test-CsWebAppAnonymous может присоединиться к своим собраниям для анонимного пользователя, командлет вернет результат теста "успешно".</span><span class="sxs-lookup"><span data-stu-id="5d6df-129">If Test-CsWebAppAnonymous can join the anonymous user to his or her conferences, the cmdlet will return the test result Success:</span></span>

<span data-ttu-id="5d6df-130">Целевое полное доменное имя:</span><span class="sxs-lookup"><span data-stu-id="5d6df-130">Target Fqdn :</span></span>

<span data-ttu-id="5d6df-131">Результат: успех</span><span class="sxs-lookup"><span data-stu-id="5d6df-131">Result : Success</span></span>

<span data-ttu-id="5d6df-132">Задержка: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="5d6df-132">Latency : 00:00:00</span></span>

<span data-ttu-id="5d6df-133">Сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="5d6df-133">Error Message :</span></span>

<span data-ttu-id="5d6df-134">Диагностик</span><span class="sxs-lookup"><span data-stu-id="5d6df-134">Diagnosis :</span></span>

<span data-ttu-id="5d6df-135">Если анонимный пользователь не может присоединиться к необходимым конференциям, результат теста будет помечен как сбой.</span><span class="sxs-lookup"><span data-stu-id="5d6df-135">If the anonymous user can't join the necessary conferences then the test result will be marked as Failure.</span></span> <span data-ttu-id="5d6df-136">Обычно Test-CsWebAppAnonymous также сообщает о подробном сообщении об ошибке и диагностике:</span><span class="sxs-lookup"><span data-stu-id="5d6df-136">Typically Test-CsWebAppAnonymous will also report back a detailed error message and diagnosis:</span></span>

<span data-ttu-id="5d6df-137">Целевое полное доменное имя: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="5d6df-137">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="5d6df-138">Результат: сбой</span><span class="sxs-lookup"><span data-stu-id="5d6df-138">Result : Failure</span></span>

<span data-ttu-id="5d6df-139">Задержка: 00:00:05.9746266</span><span class="sxs-lookup"><span data-stu-id="5d6df-139">Latency : 00:00:05.9746266</span></span>

<span data-ttu-id="5d6df-140">Сообщение об ошибке: ни одного ответа не получено для службы Web-Ticket</span><span class="sxs-lookup"><span data-stu-id="5d6df-140">Error Message : No response received for Web-Ticket service</span></span>

<span data-ttu-id="5d6df-141">Диагностика: запрос HTTP-запроса не разрешен клиентом</span><span class="sxs-lookup"><span data-stu-id="5d6df-141">Diagnosis : The HTTP request is unauthorized with client</span></span>

<span data-ttu-id="5d6df-142">Схема проверки подлинности "NTLM".</span><span class="sxs-lookup"><span data-stu-id="5d6df-142">authentication scheme 'Ntlm'.</span></span> <span data-ttu-id="5d6df-143">Проверка подлинности</span><span class="sxs-lookup"><span data-stu-id="5d6df-143">The authentication</span></span>

<span data-ttu-id="5d6df-144">заголовку, полученному от сервера, является "Negotiate, NTLM".</span><span class="sxs-lookup"><span data-stu-id="5d6df-144">header received from the server was 'Negotiate,NTLM'.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="5d6df-145">Причины, по которым может произойти сбой теста</span><span class="sxs-lookup"><span data-stu-id="5d6df-145">Reasons why the test might have failed</span></span>

<span data-ttu-id="5d6df-146">Ошибки Test-CsWebAppAnonymous обычно связаны с ошибками проверки подлинности пользователей: необходимо выполнить тест с помощью действительной учетной записи пользователя, несмотря на то, что командлет проверяет возможность подключения анонимного пользователя к Lync Server.</span><span class="sxs-lookup"><span data-stu-id="5d6df-146">Test-CsWebAppAnonymous failures usually revolve around user authentication errors: you must run the test using a valid user account even though the cmdlet is checking the ability of an anonymous user to connect to Lync Server.</span></span> <span data-ttu-id="5d6df-147">Если Test-CsWebAppAnonymous не удается, необходимо проверить, является ли указанный пользователь действительной учетной записью пользователя Lync Server.</span><span class="sxs-lookup"><span data-stu-id="5d6df-147">If Test-CsWebAppAnonymous fails, you should verify that the specified user has valid a Lync Server user account.</span></span> <span data-ttu-id="5d6df-148">Вы можете получить сведения об учетной записи Lync Server с помощью следующей команды:</span><span class="sxs-lookup"><span data-stu-id="5d6df-148">You can retrieve Lync Server account information by using a command similar to this:</span></span>

    Get-CsUser -Identity "sip:kenmyer@litwareinc.com" | Select-Object Enabled

<span data-ttu-id="5d6df-149">Если свойство Enabled не равно true или если команда не выполнена, это означает, что у пользователя нет действительной учетной записи Lync Server.</span><span class="sxs-lookup"><span data-stu-id="5d6df-149">If the Enabled property is not equal to True or if the command fails, that means that the user does not have a valid Lync Server account.</span></span>

<span data-ttu-id="5d6df-150">Кроме того, необходимо убедиться, что пароль, предоставленный при запуске командлета, является действительным паролем.</span><span class="sxs-lookup"><span data-stu-id="5d6df-150">You should also verify that the password that you supplied when you run the cmdlet is a valid password.</span></span>

<span data-ttu-id="5d6df-151">Проблемы с конфигурацией с помощью сервера Office Web Apps также могут привести к сбою Test-CsWebAppAnonymous; Это часто может возникнуть, если вы получаете следующую диагностику:</span><span class="sxs-lookup"><span data-stu-id="5d6df-151">Configuration problems with Office Web Apps Server can also cause Test-CsWebAppAnonymous to fail; that will often be the case if you receive the following diagnosis:</span></span>

<span data-ttu-id="5d6df-152">Запрос HTTP не разрешен в схеме проверки подлинности клиента "NTLM".</span><span class="sxs-lookup"><span data-stu-id="5d6df-152">The HTTP request is unauthorized with client authentication scheme 'Ntlm'.</span></span> <span data-ttu-id="5d6df-153">Заголовок проверки подлинности, полученный от сервера, — "Negotiate, NTLM".</span><span class="sxs-lookup"><span data-stu-id="5d6df-153">The authentication header received from the server was 'Negotiate,NTLM'.</span></span>

<span data-ttu-id="5d6df-154">Дополнительные сведения о диагностике и устранении проблем с сервером Office Web Apps см. в блоге [сервер Office Web apps 2013 — компьютеры, на которых выводится сообщение о неработоспособности](http://www.wictorwilen.se/office-web-apps-server-2013---machines-are-always-reported-as-unhealthy).</span><span class="sxs-lookup"><span data-stu-id="5d6df-154">For more information on diagnosing and resolving Office Web Apps Server problems see the blog post [Office Web Apps Server 2013 - machines are always reported as Unhealthy](http://www.wictorwilen.se/office-web-apps-server-2013---machines-are-always-reported-as-unhealthy).</span></span>

<span data-ttu-id="5d6df-155"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5d6df-155"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

