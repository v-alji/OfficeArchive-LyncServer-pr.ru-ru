---
title: 'Lync Server 2013: Проверка возможности развертывания групп'
description: 'Lync Server 2013: Проверка возможности развертывания групп.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing ability to employ group expansion
ms:assetid: 9b0fc954-6f9c-411a-ab32-94ebabc42de2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn743836(v=OCS.15)
ms:contentKeyID: 63969634
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6267bc2099fc420c5c57e1ef80f4bf4491334938
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441111"
---
# <a name="testing-ability-to-employ-group-expansion-in-lync-server-2013"></a><span data-ttu-id="cd59d-103">Тестирование возможности развертывания групп в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cd59d-103">Testing ability to employ group expansion in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cd59d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cd59d-104">

<span> </span></span></span>

<span data-ttu-id="cd59d-105">_**Тема последнего изменения:** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="cd59d-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cd59d-106">Расписание проверки</span><span class="sxs-lookup"><span data-stu-id="cd59d-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="cd59d-107">Ежедневно</span><span class="sxs-lookup"><span data-stu-id="cd59d-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd59d-108">Средство тестирования</span><span class="sxs-lookup"><span data-stu-id="cd59d-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="cd59d-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="cd59d-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd59d-110">Требуемые разрешения</span><span class="sxs-lookup"><span data-stu-id="cd59d-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="cd59d-111">При локальном запуске с помощью командной консоли Lync Server пользователи должны быть членами группы безопасности RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="cd59d-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="cd59d-112">При запуске с помощью удаленного экземпляра Windows PowerShell пользователям должна быть назначена роль RBAC, имеющая разрешение на запуск командлета Test-CsGroupExpansion.</span><span class="sxs-lookup"><span data-stu-id="cd59d-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsGroupExpansion cmdlet.</span></span> <span data-ttu-id="cd59d-113">Чтобы просмотреть список всех ролей RBAC, которые могут использовать этот командлет, выполните в командной строке Windows PowerShell следующую команду:</span><span class="sxs-lookup"><span data-stu-id="cd59d-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsGroupExpansion&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="cd59d-114">Описание</span><span class="sxs-lookup"><span data-stu-id="cd59d-114">Description</span></span>

<span data-ttu-id="cd59d-115">Командлет Test-CsGroupExpansion позволяет определить, работает ли расширение групп в Организации.</span><span class="sxs-lookup"><span data-stu-id="cd59d-115">The Test-CsGroupExpansion cmdlet lets you determine whether group expansion is working within your organization.</span></span> <span data-ttu-id="cd59d-116">Если включено расширение группы, пользователи настраивают группы рассылки как контакты.</span><span class="sxs-lookup"><span data-stu-id="cd59d-116">When group expansion is enabled, users configure distribution groups as a contact.</span></span> <span data-ttu-id="cd59d-117">Это означает, что пользователи смогут отправить одно и то же мгновенное сообщение всем участникам группы, направив сообщение группе, а не отдельным участникам этой группы.</span><span class="sxs-lookup"><span data-stu-id="cd59d-117">That means that those users can then send the same instant message to all the group members by addressing the message to the group instead of to individual members of that group.</span></span> <span data-ttu-id="cd59d-118">Расширение групп позволяет быстро и легко просмотреть всех участников группы и их текущее состояние.</span><span class="sxs-lookup"><span data-stu-id="cd59d-118">Group expansion enables you to quickly and easily view all the group members and their current status.</span></span>

<span data-ttu-id="cd59d-119">С помощью командлета Test-CsGroupExpansion вы указываете группу рассылки Active Directory, используя адрес электронной почты группы.</span><span class="sxs-lookup"><span data-stu-id="cd59d-119">With the Test-CsGroupExpansion cmdlet, you specify an Active Directory distribution group by using the group’s email address.</span></span> <span data-ttu-id="cd59d-120">Test-CsGroupExpansion затем использует расширение группы для получения сведений о членстве в группах и сравнения извлеченного списка с членством в указанном адресе электронной почты группы.</span><span class="sxs-lookup"><span data-stu-id="cd59d-120">Test-CsGroupExpansion then uses group expansion to retrieve the group membership and compare the retrieved list to the membership of the group email address that you supplied.</span></span> <span data-ttu-id="cd59d-121">Если два списка соответствуют друг другу, то расширение группы работает правильно.</span><span class="sxs-lookup"><span data-stu-id="cd59d-121">If the two lists match, then group expansion is working correctly.</span></span> <span data-ttu-id="cd59d-122">Обратите внимание, что вы можете протестировать расширение группы двумя способами: Протестируйте саму службу или проверяя связанную веб-службу.</span><span class="sxs-lookup"><span data-stu-id="cd59d-122">Note that you can test group expansion in two ways: by testing the service itself or by testing the associated web service.</span></span>

<span data-ttu-id="cd59d-123">Дополнительные сведения можно найти в справочной документации по командлету [Test-CsGroupExpansion](https://docs.microsoft.com/powershell/module/skype/Test-CsGroupExpansion) .</span><span class="sxs-lookup"><span data-stu-id="cd59d-123">For more information, see the Help documentation for the [Test-CsGroupExpansion](https://docs.microsoft.com/powershell/module/skype/Test-CsGroupExpansion) cmdlet.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="cd59d-124">Выполнение теста</span><span class="sxs-lookup"><span data-stu-id="cd59d-124">Running the test</span></span>

<span data-ttu-id="cd59d-125">Командлет Test-CsGroupExpansion можно выполнить с помощью предварительно настроенной тестовой учетной записи (см. раздел Настройка тестовых учетных записей для выполнения тестов Lync Server) или учетной записи пользователя, который был включен для Lync Server.</span><span class="sxs-lookup"><span data-stu-id="cd59d-125">The Test-CsGroupExpansion cmdlet can be run using either a preconfigured test account (see Setting Up Test Accounts for Running Lync Server Tests) or the account of any user who was enabled for Lync Server.</span></span> <span data-ttu-id="cd59d-126">Для выполнения этой проверки с помощью тестовой учетной записи необходимо указать полное доменное имя тестируемого пула сервера Lync и адрес электронной почты для действительной группы рассылки.</span><span class="sxs-lookup"><span data-stu-id="cd59d-126">To run this check using a test account, you just have to specify the FQDN of the Lync Server pool being tested and the email address for a valid distribution group.</span></span> <span data-ttu-id="cd59d-127">Например:</span><span class="sxs-lookup"><span data-stu-id="cd59d-127">For example:</span></span>

    Test-CsGroupExpansion -TargetFqdn "atl-cs-001.litwareinc.com" -GroupEmailAddress "Sales@litwareinc.com"

<span data-ttu-id="cd59d-128">Чтобы выполнить эту проверку с использованием реальной учетной записи пользователя, необходимо сначала создать объект учетных данных Lync Server, содержащий имя учетной записи и пароль.</span><span class="sxs-lookup"><span data-stu-id="cd59d-128">To run this check using an actual user account, you must first create a Lync Server credentials object that contains the account name and password.</span></span> <span data-ttu-id="cd59d-129">Затем необходимо добавить этот объект учетных данных и адрес SIP, назначенный учетной записи, когда система вызывает Test-CsGroupExpansion:</span><span class="sxs-lookup"><span data-stu-id="cd59d-129">You must then include that credentials object and the SIP address assigned to the account when the system calls Test-CsGroupExpansion:</span></span>

    $credential = Get-Credential "litwareinc\kenmyer"
    Test-CsGroupExpansion -TargetFqdn "atl-cs-001.litwareinc.com" -GroupEmailAddress "Sales@litwareinc.com" -UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential

<span data-ttu-id="cd59d-130">Дополнительные сведения можно найти в справочной документации по командлету [Test-CsGroupExpansion](https://docs.microsoft.com/powershell/module/skype/Test-CsGroupExpansion) .</span><span class="sxs-lookup"><span data-stu-id="cd59d-130">For more information, see the Help documentation for the [Test-CsGroupExpansion](https://docs.microsoft.com/powershell/module/skype/Test-CsGroupExpansion) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="cd59d-131">Определение успеха или сбоя</span><span class="sxs-lookup"><span data-stu-id="cd59d-131">Determining success or failure</span></span>

<span data-ttu-id="cd59d-132">Если указанный пользователь может использовать расширение группы, вы будете получать выходные данные, аналогичные этим, с помощью свойства Result, помеченного как **успешно.**</span><span class="sxs-lookup"><span data-stu-id="cd59d-132">If the specified user can use group expansion, you'll receive output similar to this with the Result property marked as **Success:**</span></span>

<span data-ttu-id="cd59d-133">TargetUri : https://atl-cs-001.litwareinc.com:443/groupexpansion/service.svc</span><span class="sxs-lookup"><span data-stu-id="cd59d-133">TargetUri : https://atl-cs-001.litwareinc.com:443/groupexpansion/service.svc</span></span>

<span data-ttu-id="cd59d-134">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="cd59d-134">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="cd59d-135">Результат: успех</span><span class="sxs-lookup"><span data-stu-id="cd59d-135">Result : Success</span></span>

<span data-ttu-id="cd59d-136">Задержка: 00:00:01.1234976</span><span class="sxs-lookup"><span data-stu-id="cd59d-136">Latency : 00:00:01.1234976</span></span>

<span data-ttu-id="cd59d-137">Ошибки</span><span class="sxs-lookup"><span data-stu-id="cd59d-137">Error :</span></span>

<span data-ttu-id="cd59d-138">Диагностик</span><span class="sxs-lookup"><span data-stu-id="cd59d-138">Diagnosis :</span></span>

<span data-ttu-id="cd59d-139">Если указанный пользователь не может использовать расширение группы, результат будет показан как сбой, а дополнительные сведения будут записаны в свойствах Error и диагноз.</span><span class="sxs-lookup"><span data-stu-id="cd59d-139">If the specified user can't use group expansion, then the Result will be shown as Failure and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="cd59d-140">TargetUri : https://atl-cs-001.litwareinc.com:443/groupexpansion/service.svc</span><span class="sxs-lookup"><span data-stu-id="cd59d-140">TargetUri : https://atl-cs-001.litwareinc.com:443/groupexpansion/service.svc</span></span>

<span data-ttu-id="cd59d-141">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="cd59d-141">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="cd59d-142">Результат: сбой</span><span class="sxs-lookup"><span data-stu-id="cd59d-142">Result : Failure</span></span>

<span data-ttu-id="cd59d-143">Задержка: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="cd59d-143">Latency : 00:00:00</span></span>

<span data-ttu-id="cd59d-144">Ошибки</span><span class="sxs-lookup"><span data-stu-id="cd59d-144">Error :</span></span>

<span data-ttu-id="cd59d-145">Диагностик</span><span class="sxs-lookup"><span data-stu-id="cd59d-145">Diagnosis :</span></span>

<span data-ttu-id="cd59d-146">Test-CsGroupExpansion: не удалось зарегистрировать конечную точку.</span><span class="sxs-lookup"><span data-stu-id="cd59d-146">Test-CsGroupExpansion : The endpoint was unable to register.</span></span> <span data-ttu-id="cd59d-147">Ознакомьтесь с ErrorCode по конкретной причине.</span><span class="sxs-lookup"><span data-stu-id="cd59d-147">See the ErrorCode for specific reason.</span></span>

<span data-ttu-id="cd59d-148">В предыдущем выводе говорится, что тест завершился сбоем, так как указанный пользователь не смог зарегистрироваться в Lync Server.</span><span class="sxs-lookup"><span data-stu-id="cd59d-148">The previous output states that the test failed because the specified user was unable to register with Lync Server.</span></span> <span data-ttu-id="cd59d-149">Обычно это происходит, если учетная запись пользователя не существует или не включена в Lync Server.</span><span class="sxs-lookup"><span data-stu-id="cd59d-149">This will typically occur if the test account does not exist or has not enabled for Lync Server.</span></span> <span data-ttu-id="cd59d-150">Вы можете проверить существование учетной записи и определить, включена ли учетная запись для NM-OCS-14-3, выполнив команду, подобную следующей:</span><span class="sxs-lookup"><span data-stu-id="cd59d-150">You can verify that the account exists, and determine whether or not the account has been enabled for nm-ocs-14-3rd by running a command similar to the following:</span></span>

    Get-CsUser -Identity "sip:kenmyer@litwareinc.com" | Select-Object SipAddress, Enabled

<span data-ttu-id="cd59d-151">Если Test-CsGroupExpansion не удается, возможно, потребуется повторно выполнить тест, на этот раз включая параметр подробно:</span><span class="sxs-lookup"><span data-stu-id="cd59d-151">If Test-CsGroupExpansion fails, then you might want to rerun the test, this time including the Verbose parameter:</span></span>

    Test-CsGroupExpansion -TargetFqdn "atl-cs-001.litwareinc.com" -GroupEmailAddress "Sales@litwareinc.com" -Verbose

<span data-ttu-id="cd59d-152">При включенном параметре подробных данных Test-CsGroupExpansion будет возвращать пошаговые учетные записи каждого действия, которое он пытался войти на сервер Lync Server.</span><span class="sxs-lookup"><span data-stu-id="cd59d-152">When the Verbose parameter is included Test-CsGroupExpansion will return a step-by-step account of each action it tried when it checked the ability of the specified user to log on to Lync Server.</span></span> <span data-ttu-id="cd59d-153">Например, эти выходные данные указывают на то, что не удалось найти указанную группу рассылки:</span><span class="sxs-lookup"><span data-stu-id="cd59d-153">For example, this output indicates that the specified distribution group couldn't be found:</span></span>

<span data-ttu-id="cd59d-154">Попытка получить веб-билет.</span><span class="sxs-lookup"><span data-stu-id="cd59d-154">Trying to get web ticket.</span></span>

<span data-ttu-id="cd59d-155">URL веб-службы: https://atl-cs-001.litwareinc.com:443/WebTicket/WebTicketService.svc</span><span class="sxs-lookup"><span data-stu-id="cd59d-155">Web Service url : https://atl-cs-001.litwareinc.com:443/WebTicket/WebTicketService.svc</span></span>

<span data-ttu-id="cd59d-156">Использование проверки подлинности NTLM/Kerb.</span><span class="sxs-lookup"><span data-stu-id="cd59d-156">Using NTLM/Kerb auth.</span></span>

<span data-ttu-id="cd59d-157">GetWebTicketActivity завершен.</span><span class="sxs-lookup"><span data-stu-id="cd59d-157">GetWebTicketActivity completed.</span></span>

<span data-ttu-id="cd59d-158">Начато действие "VerifyDistributionList".</span><span class="sxs-lookup"><span data-stu-id="cd59d-158">'VerifyDistributionList' activity started.</span></span>

<span data-ttu-id="cd59d-159">Состояние ответа веб-службы DLX: NotFound.</span><span class="sxs-lookup"><span data-stu-id="cd59d-159">DLX Web Service Response Status is: NotFound.</span></span>

<span data-ttu-id="cd59d-160">Действие "VerifyDistributionList" завершено в течение "0,2597923" сек.</span><span class="sxs-lookup"><span data-stu-id="cd59d-160">'VerifyDistributionList' activity completed in '0.2597923' secs.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="cd59d-161">Причины, по которым может произойти сбой теста</span><span class="sxs-lookup"><span data-stu-id="cd59d-161">Reasons why the test might have failed</span></span>

<span data-ttu-id="cd59d-162">Ниже приведены некоторые распространенные причины, по которым может произойти сбой Test-CsGroupExpansion.</span><span class="sxs-lookup"><span data-stu-id="cd59d-162">Here are some common reasons why Test-CsGroupExpansion might fail:</span></span>

  - <span data-ttu-id="cd59d-163">Вы указали недопустимую учетную запись пользователя.</span><span class="sxs-lookup"><span data-stu-id="cd59d-163">You specified an invalid user account.</span></span> <span data-ttu-id="cd59d-164">Для проверки существования учетной записи пользователя можно выполнить следующую команду:</span><span class="sxs-lookup"><span data-stu-id="cd59d-164">You can verify that a user account exists by running a command similar to this:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com"

  - <span data-ttu-id="cd59d-165">Учетная запись пользователя верна, но в настоящее время учетная запись не включена для Lync Server.</span><span class="sxs-lookup"><span data-stu-id="cd59d-165">The user account is valid, but the account is currently not enabled for Lync Server.</span></span> <span data-ttu-id="cd59d-166">Чтобы убедиться в том, что учетная запись пользователя включена для Lync Server, выполните команду, подобную следующей:</span><span class="sxs-lookup"><span data-stu-id="cd59d-166">To verify that a user account was enabled for Lync Server, run a command similar to the following:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object Enabled
    
    <span data-ttu-id="cd59d-167">Если для свойства Enabled задано значение false, это означает, что пользователь в настоящее время не поддерживает Lync Server.</span><span class="sxs-lookup"><span data-stu-id="cd59d-167">If the Enabled property is set to False, that means that the user is currently not enabled for Lync Server.</span></span>

  - <span data-ttu-id="cd59d-168">Возможно, отключено расширение групп.</span><span class="sxs-lookup"><span data-stu-id="cd59d-168">Group expansion might be disabled.</span></span> <span data-ttu-id="cd59d-169">Можно отключить развертывание групп.</span><span class="sxs-lookup"><span data-stu-id="cd59d-169">It is possible to turn off group expansion.</span></span> <span data-ttu-id="cd59d-170">Если расширение группы было отключено, командлет Test-CsGroupExpansion завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="cd59d-170">If group expansion was disabled then the Test-CsGroupExpansion cmdlet will fail.</span></span> <span data-ttu-id="cd59d-171">Чтобы определить, включено ли расширение группы, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="cd59d-171">To determine whether group expansion is enabled, use a command similar to this:</span></span>
    
        Get-CsWebServiceConfiguration | Select-Object Identity, EnableGroupExpansion

<span data-ttu-id="cd59d-172"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cd59d-172"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

