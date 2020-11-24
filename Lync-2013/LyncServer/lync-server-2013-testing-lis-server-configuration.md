---
title: 'Lync Server 2013: Проверка конфигурации сервера LIS'
description: 'Lync Server 2013: Проверка конфигурации сервера LIS.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing LIS server configuration
ms:assetid: 6b06e7ab-522f-41a2-878b-e89cd4e3c6da
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn690129(v=OCS.15)
ms:contentKeyID: 63969614
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ba4d16d2ce48e3e5bb89e863f02902d05ce77bd7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398962"
---
# <a name="testing-lis-server-configuration-in-lync-server-2013"></a><span data-ttu-id="ba4eb-103">Тестирование конфигурации сервера LIS в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ba4eb-103">Testing LIS server configuration in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ba4eb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ba4eb-104">

<span> </span></span></span>

<span data-ttu-id="ba4eb-105">_**Тема последнего изменения:** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="ba4eb-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ba4eb-106">Расписание проверки</span><span class="sxs-lookup"><span data-stu-id="ba4eb-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="ba4eb-107">Ежедневно</span><span class="sxs-lookup"><span data-stu-id="ba4eb-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba4eb-108">Средство тестирования</span><span class="sxs-lookup"><span data-stu-id="ba4eb-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="ba4eb-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="ba4eb-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba4eb-110">Требуемые разрешения</span><span class="sxs-lookup"><span data-stu-id="ba4eb-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="ba4eb-111">При локальном запуске с помощью командной консоли Lync Server пользователи должны быть членами группы безопасности RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="ba4eb-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="ba4eb-112">При запуске с помощью удаленного экземпляра Windows PowerShell пользователям должна быть назначена роль RBAC, имеющая разрешение на запуск командлета Test-CsLisConfiguration.</span><span class="sxs-lookup"><span data-stu-id="ba4eb-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsLisConfiguration cmdlet.</span></span> <span data-ttu-id="ba4eb-113">Чтобы просмотреть список всех ролей RBAC, которые могут использовать этот командлет, выполните в командной строке Windows PowerShell следующую команду:</span><span class="sxs-lookup"><span data-stu-id="ba4eb-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsLisConfiguration&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="ba4eb-114">Описание</span><span class="sxs-lookup"><span data-stu-id="ba4eb-114">Description</span></span>

<span data-ttu-id="ba4eb-115">Командлет Test-CsLisConfiguration проверит, есть ли у вас возможность связаться с веб-службой LIS.</span><span class="sxs-lookup"><span data-stu-id="ba4eb-115">The Test-CsLisConfiguration cmdlet verifies your ability to contact the LIS web service.</span></span> <span data-ttu-id="ba4eb-116">Если вы можете связаться с веб-службой, проверка будет считаться успешной, независимо от того, можно ли найти определенные места.</span><span class="sxs-lookup"><span data-stu-id="ba4eb-116">If the web service can be contacted, then the test will be considered a success, regardless of whether any specific locations can be found.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="ba4eb-117">Выполнение теста</span><span class="sxs-lookup"><span data-stu-id="ba4eb-117">Running the test</span></span>

<span data-ttu-id="ba4eb-118">Командлет Test-CsLisConfguration можно выполнить с помощью предварительно настроенной тестовой учетной записи (см. раздел Настройка тестовых учетных записей для выполнения тестов Lync Server) или учетной записи пользователя, который включен для Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ba4eb-118">The Test-CsLisConfguration cmdlet can be run using either a preconfigured test account (see Setting Up Test Accounts for Running Lync Server Tests) or the account of any user who is enabled for Lync Server.</span></span> <span data-ttu-id="ba4eb-119">Для выполнения этой проверки с помощью тестовой учетной записи нужно просто указать полное доменное имя для тестируемого пула Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ba4eb-119">To run this check using a test account, you just have to specify the FQDN of the Lync Server pool being tested.</span></span> <span data-ttu-id="ba4eb-120">Например:</span><span class="sxs-lookup"><span data-stu-id="ba4eb-120">For example:</span></span>

    Test-CsLisConfiguration -TargetFqdn "atl-cs-001.litwareinc.com"

<span data-ttu-id="ba4eb-121">Чтобы выполнить эту проверку с использованием реальной учетной записи пользователя, необходимо сначала создать объект учетных данных Windows PowerShell, содержащий имя учетной записи и пароль.</span><span class="sxs-lookup"><span data-stu-id="ba4eb-121">To run this check using an actual user account, you must first create a Windows PowerShell credentials object that contains the account name and password.</span></span> <span data-ttu-id="ba4eb-122">Затем необходимо добавить этот объект учетных данных и адрес SIP, назначенный учетной записи, при вызове Test-CsLisConfiguration:</span><span class="sxs-lookup"><span data-stu-id="ba4eb-122">You must then include that credentials object and the SIP address assigned to the account when you call Test-CsLisConfiguration:</span></span>

    $credential = Get-Credential "litwareinc\kenmyer"
    Test-CsLisConfiguration -TargetFqdn "atl-cs-001.litwareinc.com"-UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential

<span data-ttu-id="ba4eb-123">Дополнительные сведения можно найти в справочной документации по командлету [Test-CsLisConfiguration](https://docs.microsoft.com/powershell/module/skype/Test-CsLisConfiguration) .</span><span class="sxs-lookup"><span data-stu-id="ba4eb-123">For more information, see the Help documentation for the [Test-CsLisConfiguration](https://docs.microsoft.com/powershell/module/skype/Test-CsLisConfiguration) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="ba4eb-124">Определение успеха или сбоя</span><span class="sxs-lookup"><span data-stu-id="ba4eb-124">Determining success or failure</span></span>

<span data-ttu-id="ba4eb-125">Если вы правильно настроили LIS, вы получите вывод примерно так, чтобы свойство Result пометило **"успешно".**</span><span class="sxs-lookup"><span data-stu-id="ba4eb-125">If the LIS is correctly configured, you'll receive output similar to this, with the Result property marked as **Success:**</span></span>

<span data-ttu-id="ba4eb-126">TargetUri : https://atl-cs-001.litwareinc.com:443/locationinformation/</span><span class="sxs-lookup"><span data-stu-id="ba4eb-126">TargetUri : https://atl-cs-001.litwareinc.com:443/locationinformation/</span></span>

<span data-ttu-id="ba4eb-127">liservice. svc</span><span class="sxs-lookup"><span data-stu-id="ba4eb-127">liservice.svc</span></span>

<span data-ttu-id="ba4eb-128">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="ba4eb-128">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="ba4eb-129">Результат: успех</span><span class="sxs-lookup"><span data-stu-id="ba4eb-129">Result : Success</span></span>

<span data-ttu-id="ba4eb-130">Задержка: 00:00:06.1616913</span><span class="sxs-lookup"><span data-stu-id="ba4eb-130">Latency : 00:00:06.1616913</span></span>

<span data-ttu-id="ba4eb-131">Ошибки</span><span class="sxs-lookup"><span data-stu-id="ba4eb-131">Error :</span></span>

<span data-ttu-id="ba4eb-132">Диагностик</span><span class="sxs-lookup"><span data-stu-id="ba4eb-132">Diagnosis :</span></span>

<span data-ttu-id="ba4eb-133">Если указанному пользователю не удается войти в систему или выйти из нее, результат будет показан в виде ошибки, а дополнительные сведения будут записаны в свойствах Error и диагноз.</span><span class="sxs-lookup"><span data-stu-id="ba4eb-133">If the specified user can't log on or log off, the Result will be shown as Failure, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="ba4eb-134">TargetUri :</span><span class="sxs-lookup"><span data-stu-id="ba4eb-134">TargetUri :</span></span>

<span data-ttu-id="ba4eb-135">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="ba4eb-135">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="ba4eb-136">Результат: сбой</span><span class="sxs-lookup"><span data-stu-id="ba4eb-136">Result : Failure</span></span>

<span data-ttu-id="ba4eb-137">Задержка: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="ba4eb-137">Latency : 00:00:00</span></span>

<span data-ttu-id="ba4eb-138">Ошибка: 11004, запрошенное имя является действительным, но никаких данных запрошенного</span><span class="sxs-lookup"><span data-stu-id="ba4eb-138">Error : 11004, The requested name is valid but no data of the requested</span></span>

<span data-ttu-id="ba4eb-139">Тип найден</span><span class="sxs-lookup"><span data-stu-id="ba4eb-139">type was found</span></span>

<span data-ttu-id="ba4eb-140">Диагностик</span><span class="sxs-lookup"><span data-stu-id="ba4eb-140">Diagnosis :</span></span>

<span data-ttu-id="ba4eb-141">Test-CsLisConfiguration: в топологии не найдено подходящих кластеров.</span><span class="sxs-lookup"><span data-stu-id="ba4eb-141">Test-CsLisConfiguration : No matching cluster found in topology.</span></span>

<span data-ttu-id="ba4eb-142">Например, в предыдущем выводе есть Примечание "в топологии не найдено подходящего кластера".</span><span class="sxs-lookup"><span data-stu-id="ba4eb-142">For example, the previous output includes the note “No matching cluster found in topology.”</span></span> <span data-ttu-id="ba4eb-143">Обычно это свидетельствует о проблеме с сервером граничного сервера: LIS с помощью пограничного сервера для подключения к поставщику услуг и проверки адресов.</span><span class="sxs-lookup"><span data-stu-id="ba4eb-143">That typically indicates a problem with the Edge Server: the LIS using the Edge Server to connect to the service provider and validate addresses.</span></span>

<span data-ttu-id="ba4eb-144">Если Test-CsLisConfiguration не удается, возможно, потребуется повторно выполнить тест, на этот раз включая параметр подробно:</span><span class="sxs-lookup"><span data-stu-id="ba4eb-144">If Test-CsLisConfiguration fails then you might want to rerun the test, this time including the Verbose parameter:</span></span>

    Test-CsLisConfiguration -TargetFqdn "atl-cs-001.litwareinc.com" -Verbose

<span data-ttu-id="ba4eb-145">После включения подробной информации Test-CsLisConfiguration будет возвращать пошаговые учетные записи каждого действия, которое он пытался войти на сервер Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ba4eb-145">When the Verbose parameter is included, Test-CsLisConfiguration will return a step-by-step account of each action it tried when it checked the ability of the specified user to log on to Lync Server.</span></span> <span data-ttu-id="ba4eb-146">Например:</span><span class="sxs-lookup"><span data-stu-id="ba4eb-146">For example:</span></span>

<span data-ttu-id="ba4eb-147">Вызов службы сведений о расположении.</span><span class="sxs-lookup"><span data-stu-id="ba4eb-147">Calling Location Information Service.</span></span>

<span data-ttu-id="ba4eb-148">Путь к службе = https://atl-cs-001.litwareinc.com:443/locationinformation/liservice.svc</span><span class="sxs-lookup"><span data-stu-id="ba4eb-148">Service Path = https://atl-cs-001.litwareinc.com:443/locationinformation/liservice.svc</span></span>

<span data-ttu-id="ba4eb-149">Subnet =</span><span class="sxs-lookup"><span data-stu-id="ba4eb-149">Subnet =</span></span>

<span data-ttu-id="ba4eb-150">BssId = 5</span><span class="sxs-lookup"><span data-stu-id="ba4eb-150">BssId = 5</span></span>

<span data-ttu-id="ba4eb-151">ChassisId =</span><span class="sxs-lookup"><span data-stu-id="ba4eb-151">ChassisId =</span></span>

<span data-ttu-id="ba4eb-152">PortId =</span><span class="sxs-lookup"><span data-stu-id="ba4eb-152">PortId =</span></span>

<span data-ttu-id="ba4eb-153">PortIdSubType = неопределенный тип</span><span class="sxs-lookup"><span data-stu-id="ba4eb-153">PortIdSubType = Undefined Type</span></span>

<span data-ttu-id="ba4eb-154">Mac</span><span class="sxs-lookup"><span data-stu-id="ba4eb-154">Mac</span></span>

<span data-ttu-id="ba4eb-155">Не удалось выполнить запрос веб-службы сведений о расположении с кодом ответа Item400.</span><span class="sxs-lookup"><span data-stu-id="ba4eb-155">An exception 'Location Information Web Service request has failed with a response code Item400.'</span></span> <span data-ttu-id="ba4eb-156">произошла ошибка во время выполнения рабочего процесса Microsoft. RTC. SyntheticTrsnactions. Workflows. STLisConfigurationWorkflow.</span><span class="sxs-lookup"><span data-stu-id="ba4eb-156">occurred during Workflow Microsoft.Rtc.SyntheticTrsnactions.Workflows.STLisConfigurationWorkflow execution.</span></span>

<span data-ttu-id="ba4eb-157">Если вы проанализируете предыдущий вывод, вы увидите, что командлет завершился сбоем после того, как он попытался вызвать службу сведений о расположении.</span><span class="sxs-lookup"><span data-stu-id="ba4eb-157">If you examine the previous output closely, you’ll see that the cmdlet failed after it tried to call the Location Information Service.</span></span> <span data-ttu-id="ba4eb-158">Один из параметров, которые использовались в этом вызове:</span><span class="sxs-lookup"><span data-stu-id="ba4eb-158">One of the parameters that were used in that call was this:</span></span>

<span data-ttu-id="ba4eb-159">BssId = 5</span><span class="sxs-lookup"><span data-stu-id="ba4eb-159">BssId = 5</span></span>

<span data-ttu-id="ba4eb-160">Это значение не является допустимым для базового идентификатора Set службы (BssID).</span><span class="sxs-lookup"><span data-stu-id="ba4eb-160">That’s not a valid value for the Basic Service Set Identifier (BssID).</span></span> <span data-ttu-id="ba4eb-161">Вместо этого BssID должен выглядеть примерно так:</span><span class="sxs-lookup"><span data-stu-id="ba4eb-161">Instead, a BssID should resemble this:</span></span>

<span data-ttu-id="ba4eb-162">12-34-56-78-90 – AB</span><span class="sxs-lookup"><span data-stu-id="ba4eb-162">12-34-56-78-90-ab</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="ba4eb-163">Причины, по которым может произойти сбой теста</span><span class="sxs-lookup"><span data-stu-id="ba4eb-163">Reasons why the test might have failed</span></span>

<span data-ttu-id="ba4eb-164">Ниже приведены некоторые распространенные причины, по которым может произойти сбой Test-CsLisConfiguration.</span><span class="sxs-lookup"><span data-stu-id="ba4eb-164">Here are some common reasons why Test-CsLisConfiguration might fail:</span></span>

  - <span data-ttu-id="ba4eb-165">Предоставлено неправильное значение параметра.</span><span class="sxs-lookup"><span data-stu-id="ba4eb-165">An incorrect parameter value was supplied.</span></span> <span data-ttu-id="ba4eb-166">Как показано в предыдущем примере, необязательные параметры должны быть настроены правильно, или тест завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="ba4eb-166">As shown in the previous example, the optional parameters must be configured correctly or the test will fail.</span></span> <span data-ttu-id="ba4eb-167">Повторите выполнение команды без дополнительных параметров и проверьте, выполняется ли это успешно.</span><span class="sxs-lookup"><span data-stu-id="ba4eb-167">Rerun the command without the optional parameters and see whether that succeeds.</span></span>

<span data-ttu-id="ba4eb-168"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ba4eb-168"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

