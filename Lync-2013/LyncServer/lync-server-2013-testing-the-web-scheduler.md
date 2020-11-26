---
title: 'Lync Server 2013: Проверка веб-планировщика'
description: 'Lync Server 2013: Проверка веб-планировщика.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing the Web scheduler
ms:assetid: 58e34058-1afa-42e3-9096-c4ea1954c237
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn727304(v=OCS.15)
ms:contentKeyID: 63969603
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6512bf074078005eac66d1e4f5cd3d8ba2dc4bc7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439725"
---
# <a name="testing-the-web-scheduler-in-lync-server-2013"></a><span data-ttu-id="894b8-103">Проверка веб-планировщика в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="894b8-103">Testing the Web scheduler in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="894b8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="894b8-104">

<span> </span></span></span>

<span data-ttu-id="894b8-105">_**Тема последнего изменения:** 2014-11-03_</span><span class="sxs-lookup"><span data-stu-id="894b8-105">_**Topic Last Modified:** 2014-11-03_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="894b8-106">Расписание проверки</span><span class="sxs-lookup"><span data-stu-id="894b8-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="894b8-107">Ежедневно</span><span class="sxs-lookup"><span data-stu-id="894b8-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="894b8-108">Средство тестирования</span><span class="sxs-lookup"><span data-stu-id="894b8-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="894b8-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="894b8-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="894b8-110">Требуемые разрешения</span><span class="sxs-lookup"><span data-stu-id="894b8-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="894b8-111">При локальном запуске с помощью командной консоли Lync Server пользователи должны быть членами группы безопасности RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="894b8-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="894b8-112">При запуске с помощью удаленного экземпляра Windows PowerShell пользователям должна быть назначена роль RBAC, имеющая разрешение на запуск командлета <strong>Test-CsWebScheduler</strong> .</span><span class="sxs-lookup"><span data-stu-id="894b8-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the <strong>Test-CsWebScheduler</strong> cmdlet.</span></span> <span data-ttu-id="894b8-113">Чтобы просмотреть список всех ролей RBAC, которые могут использовать этот командлет, выполните в командной строке Windows PowerShell следующую команду:</span><span class="sxs-lookup"><span data-stu-id="894b8-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsWebScheduler&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="894b8-114">Описание</span><span class="sxs-lookup"><span data-stu-id="894b8-114">Description</span></span>

<span data-ttu-id="894b8-115">Командлет **Test-CsWebScheduler** позволяет определить, может ли определенный пользователь запланировать собрание с помощью веб-планировщика.</span><span class="sxs-lookup"><span data-stu-id="894b8-115">The **Test-CsWebScheduler** cmdlet enables you to determine whether a specific user can schedule a meeting using the Web Scheduler.</span></span> <span data-ttu-id="894b8-116">Веб-планировщик позволяет пользователям, которые не запущены в Outlook, планировать собрания по сети.</span><span class="sxs-lookup"><span data-stu-id="894b8-116">The Web Scheduler enables users who are not running Outlook to schedule online meetings.</span></span> <span data-ttu-id="894b8-117">Помимо прочего, эта новая функция (которая включает в себя функцию, обнаруженную в средстве веб-планировщика, которая входит в состав набора Microsoft Lync Server 2010 Resource Kit), позволяет пользователям:</span><span class="sxs-lookup"><span data-stu-id="894b8-117">Among other things, this new feature (which incorporates the functionality found in the Web Scheduler tool that was included with the Microsoft Lync Server 2010 resource kit) enables users to:</span></span>

  - <span data-ttu-id="894b8-118">Планирование нового собрания по сети.</span><span class="sxs-lookup"><span data-stu-id="894b8-118">Schedule a new online meeting.</span></span>

  - <span data-ttu-id="894b8-119">Список всех собраний, для которых он запланирован.</span><span class="sxs-lookup"><span data-stu-id="894b8-119">List all meetings that he or she has scheduled.</span></span>

  - <span data-ttu-id="894b8-120">Просмотр и изменение существующего собрания.</span><span class="sxs-lookup"><span data-stu-id="894b8-120">View/modify an existing meeting.</span></span>

  - <span data-ttu-id="894b8-121">Удаление существующего собрания.</span><span class="sxs-lookup"><span data-stu-id="894b8-121">Delete an existing meeting.</span></span>

  - <span data-ttu-id="894b8-122">Отправьте приглашение по электронной почте участникам собрания с помощью предварительно настроенного почтового сервера SMTP.</span><span class="sxs-lookup"><span data-stu-id="894b8-122">Send an email invitation to meeting participants by using a preconfigured SMTP mail server.</span></span>

  - <span data-ttu-id="894b8-123">Присоединиться к существующей конференции.</span><span class="sxs-lookup"><span data-stu-id="894b8-123">Join an existing conference.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="894b8-124">Выполнение теста</span><span class="sxs-lookup"><span data-stu-id="894b8-124">Running the test</span></span>

<span data-ttu-id="894b8-125">В следующем примере показана проверка веб-планировщика для пула atl-cs-001.litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="894b8-125">The following example verifies the Web Scheduler for the pool atl-cs-001.litwareinc.com.</span></span> <span data-ttu-id="894b8-126">Эта команда будет работать только в том случае, если тестовые пользователи определены для пула atl-cs-001.litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="894b8-126">This command will work only if test users are defined for the pool atl-cs-001.litwareinc.com.</span></span> <span data-ttu-id="894b8-127">Если это так, команда определит, может ли первый тестовый пользователь запланировать собрание по сети с помощью веб-планировщика.</span><span class="sxs-lookup"><span data-stu-id="894b8-127">If they have, then the command will determine whether the first test user can schedule an online meeting using the Web Scheduler.</span></span>

<span data-ttu-id="894b8-128">Если тестовые пользователи не заданы, команда завершится сбоем, так как не будет определять, какой пользователь должен войти в систему.</span><span class="sxs-lookup"><span data-stu-id="894b8-128">If test users are not defined, then the command will fail because it won't know which user to log on as.</span></span> <span data-ttu-id="894b8-129">Если вы не определили тестовых пользователей для пула, необходимо включить параметр UserSipAddress и учетные данные пользователя, который должна использовать команда при попытке входа в систему.</span><span class="sxs-lookup"><span data-stu-id="894b8-129">If you have not defined test users for a pool, then you must include the UserSipAddress parameter and the credentials of the user the command should use when trying to log on.</span></span>

    Test-CsWebScheduler -TargetFqdn "atl-cs-001.litwareinc.com"

<span data-ttu-id="894b8-130">Команды, показанные в следующем примере, проверяют возможность определенного пользователя (плана litwareinc \\ kenmeyer), чтобы запланировать собрание по сети с помощью веб-планировщика.</span><span class="sxs-lookup"><span data-stu-id="894b8-130">The commands shown in the next example test the ability of a specific user (litwareinc\\kenmeyer) to schedule an online meeting using the Web scheduler.</span></span> <span data-ttu-id="894b8-131">Для этого в первой команде примера используется командлет **Get-Credential** для создания объекта учетных данных интерфейса командной строки Windows PowerShell, который содержит имя и пароль пользователя Кен Meyer.</span><span class="sxs-lookup"><span data-stu-id="894b8-131">To do this, the first command in the example uses the **Get-Credential** cmdlet to create a Windows PowerShell command-line interface credential object that contains the name and password of the user Ken Meyer.</span></span> <span data-ttu-id="894b8-132">(Поскольку имя для входа плана litwareinc \\ kenmeyer входит в качестве параметра, в диалоговом окне Запрос учетных данных Windows PowerShell требуется, чтобы администратор введет пароль для учетной записи Кен Meyer.) Полученный объект учетных данных затем сохраняется в переменной с именем $cred 1.</span><span class="sxs-lookup"><span data-stu-id="894b8-132">(Because the logon name litwareinc\\kenmeyer is included as a parameter, the Windows PowerShell Credential Request dialog box only requires the administrator to enter the password for the Ken Meyer account.) The resulting credential object is then stored in a variable named $cred1.</span></span>

<span data-ttu-id="894b8-133">Вторая команда проверяет, может ли пользователь войти в пул atl-cs-001.litwareinc.com и запланировать собрание по сети.</span><span class="sxs-lookup"><span data-stu-id="894b8-133">The second command then checks whether this user can log on to the pool atl-cs-001.litwareinc.com and schedule an online meeting.</span></span> <span data-ttu-id="894b8-134">Для выполнения этой задачи вызывается командлет **Test-CsWebScheduler** , вместе с тремя параметрами: TargetFqdn (полное доменное имя пула регистраторов). UserCredential (объект Windows PowerShell, который включает в себя учетные данные пользователя для почтового Вронский); и UserSipAddress (SIP-адрес, соответствующий предоставленным учетным данным пользователя).</span><span class="sxs-lookup"><span data-stu-id="894b8-134">To run this task, the **Test-CsWebScheduler** cmdlet is called, together with three parameters: TargetFqdn (the FQDN of the Registrar pool); UserCredential (the Windows PowerShell object that contains Pilar Ackerman’s user credentials); and UserSipAddress (the SIP address that corresponds to the supplied user credentials).</span></span>

    $credential = Get-Credential "litwareinc\kenmyer"
    
    Test-CsWebScheduler -TargetFqdn "atl-cs-001.litwareinc.com" -UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="894b8-135">Определение успеха или сбоя</span><span class="sxs-lookup"><span data-stu-id="894b8-135">Determining success or failure</span></span>

<span data-ttu-id="894b8-136">Если веб-планировщик настроен правильно, вы получите вывод, аналогичный приведенному ниже, и свойство Result помечается как **успешно**.</span><span class="sxs-lookup"><span data-stu-id="894b8-136">If the web scheduler is configured correctly , you'll receive output similar to this, with the Result property marked as **Success**:</span></span>

<span data-ttu-id="894b8-137">Целевое полное доменное имя: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="894b8-137">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="894b8-138">Конечный URI: https://atl-cs-001.litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="894b8-138">Target Uri : https:// atl-cs-001.litwareinc.com.</span></span>

<span data-ttu-id="894b8-139">litwareinc.com:443/Scheduler</span><span class="sxs-lookup"><span data-stu-id="894b8-139">litwareinc.com:443/Scheduler</span></span>

<span data-ttu-id="894b8-140">Результат: успех</span><span class="sxs-lookup"><span data-stu-id="894b8-140">Result : Success</span></span>

<span data-ttu-id="894b8-141">Задержка: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="894b8-141">Latency : 00:00:00</span></span>

<span data-ttu-id="894b8-142">Сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="894b8-142">Error Message :</span></span>

<span data-ttu-id="894b8-143">Диагностик</span><span class="sxs-lookup"><span data-stu-id="894b8-143">Diagnosis :</span></span>

<span data-ttu-id="894b8-144">Если веб-планировщик настроен неправильно, результат будет отображаться как **сбой**, а дополнительные сведения будут записаны в свойствах Error и диагноз.</span><span class="sxs-lookup"><span data-stu-id="894b8-144">If the web scheduler is not configured correctly, the Result will be shown as **Failure**, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="894b8-145">Предупреждение: не удалось прочитать номер порта регистратора для заданного полного имени</span><span class="sxs-lookup"><span data-stu-id="894b8-145">WARNING: Failed to read Registrar port number for the given fully qualified</span></span>

<span data-ttu-id="894b8-146">доменное имя (FQDN).</span><span class="sxs-lookup"><span data-stu-id="894b8-146">domain name (FQDN).</span></span> <span data-ttu-id="894b8-147">С помощью номера порта регистратора по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="894b8-147">Using default Registrar port number.</span></span> <span data-ttu-id="894b8-148">Ошибка</span><span class="sxs-lookup"><span data-stu-id="894b8-148">Exception:</span></span>

<span data-ttu-id="894b8-149">System. InvalidOperationException: в топологии не обнаружены подходящие кластеры.</span><span class="sxs-lookup"><span data-stu-id="894b8-149">System.InvalidOperationException: No matching cluster found in topology.</span></span>

<span data-ttu-id="894b8-150">скорость</span><span class="sxs-lookup"><span data-stu-id="894b8-150">at</span></span>

<span data-ttu-id="894b8-151">Microsoft. RTC. Management. SyntheticTransactions. SipSyntheticTransaction. TryRetri</span><span class="sxs-lookup"><span data-stu-id="894b8-151">Microsoft.Rtc.Management.SyntheticTransactions.SipSyntheticTransaction.TryRetri</span></span>

<span data-ttu-id="894b8-152">eveRegistrarPortFromTopology (Int32& registrarPortNumber)</span><span class="sxs-lookup"><span data-stu-id="894b8-152">eveRegistrarPortFromTopology(Int32& registrarPortNumber)</span></span>

<span data-ttu-id="894b8-153">Целевое полное доменное имя: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="894b8-153">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="894b8-154">Конечный URI:</span><span class="sxs-lookup"><span data-stu-id="894b8-154">Target Uri :</span></span>

<span data-ttu-id="894b8-155">Результат: сбой</span><span class="sxs-lookup"><span data-stu-id="894b8-155">Result : Failure</span></span>

<span data-ttu-id="894b8-156">Задержка: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="894b8-156">Latency : 00:00:00</span></span>

<span data-ttu-id="894b8-157">Сообщение об ошибке: подходящие кластеры не найдены в топологии.</span><span class="sxs-lookup"><span data-stu-id="894b8-157">Error Message : No matching cluster found in topology.</span></span>

<span data-ttu-id="894b8-158">Диагностик</span><span class="sxs-lookup"><span data-stu-id="894b8-158">Diagnosis :</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="894b8-159">Причины, по которым может произойти сбой теста</span><span class="sxs-lookup"><span data-stu-id="894b8-159">Reasons why the test might have failed</span></span>

<span data-ttu-id="894b8-160">Ниже приведены некоторые распространенные причины, по которым может произойти сбой **Test-CsWebScheduler** :</span><span class="sxs-lookup"><span data-stu-id="894b8-160">Here are some common reasons why **Test-CsWebScheduler** might fail:</span></span>

  - <span data-ttu-id="894b8-161">Предоставлено неправильное значение параметра.</span><span class="sxs-lookup"><span data-stu-id="894b8-161">An incorrect parameter value was supplied.</span></span> <span data-ttu-id="894b8-162">Если используется, необязательные параметры необходимо настроить правильно, или тест завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="894b8-162">If used, the optional parameters must be configured correctly or the test will fail.</span></span> <span data-ttu-id="894b8-163">Повторите выполнение команды без дополнительных параметров и проверьте, выполняется ли это успешно.</span><span class="sxs-lookup"><span data-stu-id="894b8-163">Rerun the command without the optional parameters and see whether that succeeds.</span></span>

  - <span data-ttu-id="894b8-164">Эта команда завершится сбоем, если веб-планировщик неправильно настроен или еще не развернут.</span><span class="sxs-lookup"><span data-stu-id="894b8-164">This command will fail if the Web Scheduler is misconfigured or not yet deployed.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="894b8-165">См. также</span><span class="sxs-lookup"><span data-stu-id="894b8-165">See Also</span></span>


[<span data-ttu-id="894b8-166">Set-CsWebServer</span><span class="sxs-lookup"><span data-stu-id="894b8-166">Set-CsWebServer</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsWebServer)  
  

<span data-ttu-id="894b8-167"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="894b8-167"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

