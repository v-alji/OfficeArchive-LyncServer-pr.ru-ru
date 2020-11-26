---
title: 'Lync Server 2013: Проверка доступа к веб-приложению'
description: 'Lync Server 2013: Проверка доступа к веб-приложению.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test Web App access
ms:assetid: 17d67ea3-f74d-4952-ac2b-92c0dacc8014
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn767944(v=OCS.15)
ms:contentKeyID: 63969584
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fc3bbc8008df4fe47fc5a39571356383fe5a6035
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441132"
---
# <a name="test-web-app-access-in-lync-server-2013"></a><span data-ttu-id="d1e17-103">Проверка доступа к веб-приложению в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d1e17-103">Test Web App access in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d1e17-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d1e17-104">

<span> </span></span></span>

<span data-ttu-id="d1e17-105">_**Тема последнего изменения:** 2014-06-07_</span><span class="sxs-lookup"><span data-stu-id="d1e17-105">_**Topic Last Modified:** 2014-06-07_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d1e17-106">Расписание проверки</span><span class="sxs-lookup"><span data-stu-id="d1e17-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="d1e17-107">Ежемесячно</span><span class="sxs-lookup"><span data-stu-id="d1e17-107">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1e17-108">Средство тестирования</span><span class="sxs-lookup"><span data-stu-id="d1e17-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="d1e17-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="d1e17-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d1e17-110">Требуемые разрешения</span><span class="sxs-lookup"><span data-stu-id="d1e17-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="d1e17-111">При локальном запуске с помощью командной консоли Lync Server пользователи должны быть членами группы безопасности RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="d1e17-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="d1e17-112">При запуске с помощью удаленного экземпляра Windows PowerShell пользователям должна быть назначена роль RBAC, имеющая разрешение на запуск командлета Test-CsWebApp.</span><span class="sxs-lookup"><span data-stu-id="d1e17-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsWebApp cmdlet.</span></span> <span data-ttu-id="d1e17-113">Чтобы просмотреть список всех ролей RBAC, которые могут использовать этот командлет, выполните в командной строке Windows PowerShell следующую команду:</span><span class="sxs-lookup"><span data-stu-id="d1e17-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsWebApp&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="d1e17-114">Описание</span><span class="sxs-lookup"><span data-stu-id="d1e17-114">Description</span></span>

<span data-ttu-id="d1e17-115">Командлет Test-CsWebApp удостоверяет, что пользователи, прошедшие проверку подлинности, могут присоединиться к конференциям Lync Server с помощью Lync Web App.</span><span class="sxs-lookup"><span data-stu-id="d1e17-115">The Test-CsWebApp cmdlet verifies that authenticated users can join Lync Server conferences by using the Lync Web App.</span></span> <span data-ttu-id="d1e17-116">Когда вы запускаете командлет, Test-CsWebApp обращается к службе веб-билета, чтобы получить веб-билеты для указанных пользователей.</span><span class="sxs-lookup"><span data-stu-id="d1e17-116">When you run the cmdlet, Test-CsWebApp contacts the Web Ticket service to obtain web tickets for the specified users.</span></span> <span data-ttu-id="d1e17-117">Эти билеты эффективно действуют в конференц-зале Lync Server с помощью билетов на допускную связь.</span><span class="sxs-lookup"><span data-stu-id="d1e17-117">These tickets effectively act as ‘admission tickets” to the Lync Server conference.</span></span> <span data-ttu-id="d1e17-118">Если вы можете получить билеты, и если пользователи могут проходить проверку подлинности, Test-CsWebApp будут обращаться к Lync Server и попытаться установить отдельные конференции для обмена мгновенными сообщениями, совместного использования приложений и совместной работы с данными.</span><span class="sxs-lookup"><span data-stu-id="d1e17-118">If the tickets can be retrieved, and if the users can be authenticated, Test-CsWebApp will then contact Lync Server and attempt to establish separate conferences for instant messaging, application sharing, and data collaboration.</span></span>

<span data-ttu-id="d1e17-119">Обратите внимание, что Test-CsWebApp просто проверяет интерфейсы API и соединения, используемые для создания этих конференций.</span><span class="sxs-lookup"><span data-stu-id="d1e17-119">Note that Test-CsWebApp just verifies the APIs and connections used to create these conferences.</span></span> <span data-ttu-id="d1e17-120">Этот командлет предназначен для проверки того, что приложение Lync Web App можно использовать для создания и присоединения к конференциям.</span><span class="sxs-lookup"><span data-stu-id="d1e17-120">The cmdlet is designed to verify that Lync Web App could be used to create and join conferences.</span></span> <span data-ttu-id="d1e17-121">Тем не менее, в действительности она не создает и не проводит конференции.</span><span class="sxs-lookup"><span data-stu-id="d1e17-121">However,, it does not actually create and conduct a conference.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="d1e17-122">Выполнение теста</span><span class="sxs-lookup"><span data-stu-id="d1e17-122">Running the test</span></span>

<span data-ttu-id="d1e17-123">Командлет Test-CsWebApp можно выполнить с помощью пары предварительно настроенных тестовых учетных записей или учетных записей двух пользователей, которые включены в Lync Server.</span><span class="sxs-lookup"><span data-stu-id="d1e17-123">The Test-CsWebApp cmdlet can be run using either a pair of preconfigured test accounts or the accounts of any two users who are enabled for Lync Server.</span></span> <span data-ttu-id="d1e17-124">Для выполнения этой проверки с помощью тестовых учетных записей нужно просто указать полное доменное имя для тестируемого пула сервера Lync Server.</span><span class="sxs-lookup"><span data-stu-id="d1e17-124">To run this check using test accounts, you just have to specify the fully qualified domain name of the Lync Server pool being tested.</span></span> <span data-ttu-id="d1e17-125">Например:</span><span class="sxs-lookup"><span data-stu-id="d1e17-125">For example:</span></span>

    Test-CsWebApp -TargetFqdn "atl-cs-001.litwareinc.com"

<span data-ttu-id="d1e17-126">Для выполнения этой проверки с использованием фактических учетных записей пользователей необходимо создать два объекта учетных данных Windows PowerShell (объекты, содержащие имя и пароль учетной записи) для каждой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="d1e17-126">To run this check using actual user accounts, you must create two Windows PowerShell credentials objects (objects that contain the account name and password) for each account.</span></span> <span data-ttu-id="d1e17-127">После вызова Test-CsWebApp вы должны добавить эти объекты учетных данных и адреса SIP для двух учетных записей.</span><span class="sxs-lookup"><span data-stu-id="d1e17-127">You must then include those credentials objects and the SIP addresses of the two accounts when you call Test-CsWebApp:</span></span>

    $cred1 = Get-Credential "litwareinc\kenmyer"
    $cred2 = Get-Credential "litwareinc\pilar"
    
    Test-CsWebApp -TargetFqdn atl-cs-001.litwareinc.com -UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $cred1 -User2SipAddress "sip:pilar@litwareinc.com" -User2Credential $cred2

<span data-ttu-id="d1e17-128">Дополнительные сведения можно найти в разделе справки по командлету [Test-CsWebApp](https://docs.microsoft.com/powershell/module/skype/Test-CsWebApp) .</span><span class="sxs-lookup"><span data-stu-id="d1e17-128">For more information, see the help topic for the [Test-CsWebApp](https://docs.microsoft.com/powershell/module/skype/Test-CsWebApp) cmdlet.</span></span> <span data-ttu-id="d1e17-129">Обратите внимание, что Test-CsWebApp не рекомендуется использовать в Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d1e17-129">Note that Test-CsWebApp was deprecated for use on Lync Server 2013.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="d1e17-130">Определение успеха или сбоя</span><span class="sxs-lookup"><span data-stu-id="d1e17-130">Determining success or failure</span></span>

<span data-ttu-id="d1e17-131">Если Test-CsWebApp можете присоединиться к своим конференциям, командлет вернет результат теста "успешно".</span><span class="sxs-lookup"><span data-stu-id="d1e17-131">If Test-CsWebApp can join the users to their conferences, the cmdlet will return the test result Success:</span></span>

<span data-ttu-id="d1e17-132">Целевое полное доменное имя:</span><span class="sxs-lookup"><span data-stu-id="d1e17-132">Target Fqdn :</span></span>

<span data-ttu-id="d1e17-133">Результат: успех</span><span class="sxs-lookup"><span data-stu-id="d1e17-133">Result : Success</span></span>

<span data-ttu-id="d1e17-134">Задержка: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="d1e17-134">Latency : 00:00:00</span></span>

<span data-ttu-id="d1e17-135">Сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="d1e17-135">Error Message :</span></span>

<span data-ttu-id="d1e17-136">Диагностик</span><span class="sxs-lookup"><span data-stu-id="d1e17-136">Diagnosis :</span></span>

<span data-ttu-id="d1e17-137">Если пользователи не могут присоединиться к необходимым конференциям, результат теста будет помечен как сбой.</span><span class="sxs-lookup"><span data-stu-id="d1e17-137">If the users cannot join the necessary conferences then the test result will be marked as Failure.</span></span> <span data-ttu-id="d1e17-138">Обычно Test-CsWebApp также сообщает о подробном сообщении об ошибке и диагностике:</span><span class="sxs-lookup"><span data-stu-id="d1e17-138">Typically Test-CsWebApp will also report back a detailed error message and diagnosis:</span></span>

<span data-ttu-id="d1e17-139">Целевое полное доменное имя: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="d1e17-139">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="d1e17-140">Результат: сбой</span><span class="sxs-lookup"><span data-stu-id="d1e17-140">Result : Failure</span></span>

<span data-ttu-id="d1e17-141">Задержка: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="d1e17-141">Latency : 00:00:00</span></span>

<span data-ttu-id="d1e17-142">Сообщение об ошибке: ни одного ответа не получено для службы Web-Ticket</span><span class="sxs-lookup"><span data-stu-id="d1e17-142">Error Message : No response received for Web-Ticket service</span></span>

<span data-ttu-id="d1e17-143">Диагностика: запрос HTTP-запроса не разрешен клиентом</span><span class="sxs-lookup"><span data-stu-id="d1e17-143">Diagnosis : The HTTP request is unauthorized with client</span></span>

<span data-ttu-id="d1e17-144">Схема проверки подлинности "NTLM".</span><span class="sxs-lookup"><span data-stu-id="d1e17-144">authentication scheme 'Ntlm'.</span></span> <span data-ttu-id="d1e17-145">Проверка подлинности</span><span class="sxs-lookup"><span data-stu-id="d1e17-145">The authentication</span></span>

<span data-ttu-id="d1e17-146">заголовку, полученному от сервера, является "Negotiate, NTLM".</span><span class="sxs-lookup"><span data-stu-id="d1e17-146">header received from the server was 'Negotiate,NTLM'.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="d1e17-147">Причины, по которым может произойти сбой теста</span><span class="sxs-lookup"><span data-stu-id="d1e17-147">Reasons why the test might have failed</span></span>

<span data-ttu-id="d1e17-148">Обычно ошибки, связанные с проверкой подлинности пользователей, Test-CsWebApp.</span><span class="sxs-lookup"><span data-stu-id="d1e17-148">Test-CsWebApp failures typically involve user authentication errors.</span></span> <span data-ttu-id="d1e17-149">Если Test-CsWebApp не удается, сначала убедитесь в том, что у указанных пользователей есть действительные учетные записи пользователей и они включены для Lync Server.</span><span class="sxs-lookup"><span data-stu-id="d1e17-149">If Test-CsWebApp fails, you should first verify that the specified users have valid user accounts and are enabled for Lync Server.</span></span> <span data-ttu-id="d1e17-150">Вы можете получить сведения об учетной записи с помощью следующей команды:</span><span class="sxs-lookup"><span data-stu-id="d1e17-150">You can retrieve account information by using a command similar to this:</span></span>

    Get-CsUser -Identity "sip:kenmyer@litwareinc.com" | Select-Object Enabled

<span data-ttu-id="d1e17-151">Если свойство Enabled не равно true или если команда не выполнена, это означает, что у пользователя нет действительной учетной записи Lync Server. Кроме того, необходимо убедиться, что указанные в командлете пароли действительны.</span><span class="sxs-lookup"><span data-stu-id="d1e17-151">If the Enabled property is not equal to True or if the command fails, that means that the user does not have a valid Lync Server account.You should also verify that the passwords that you supplied to the cmdlet are valid.</span></span>

<span data-ttu-id="d1e17-152"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d1e17-152"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

