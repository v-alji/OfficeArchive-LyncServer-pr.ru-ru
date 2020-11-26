---
title: 'Lync Server 2013: Проверка конфигурации голосовой связи'
description: 'Lync Server 2013: Проверка конфигурации голосовой связи.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test voice configuration
ms:assetid: 574794a3-cb30-4762-bb62-3a68574f05e9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn725208(v=OCS.15)
ms:contentKeyID: 63969605
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4cc05286e5f534b4d469ef561d9ce009367e15be
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444184"
---
# <a name="test-voice-configuration-in-lync-server-2013"></a><span data-ttu-id="0625d-103">Проверка конфигурации голосовой связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0625d-103">Test voice configuration in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0625d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0625d-104">

<span> </span></span></span>

<span data-ttu-id="0625d-105">_**Тема последнего изменения:** 2014-05-20_</span><span class="sxs-lookup"><span data-stu-id="0625d-105">_**Topic Last Modified:** 2014-05-20_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0625d-106">Расписание проверки</span><span class="sxs-lookup"><span data-stu-id="0625d-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="0625d-107">Ежемесячно</span><span class="sxs-lookup"><span data-stu-id="0625d-107">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0625d-108">Средство тестирования</span><span class="sxs-lookup"><span data-stu-id="0625d-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="0625d-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="0625d-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0625d-110">Требуемые разрешения</span><span class="sxs-lookup"><span data-stu-id="0625d-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="0625d-111">При локальном запуске с помощью командной консоли Lync Server пользователи должны быть членами группы безопасности RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="0625d-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="0625d-112">При запуске с помощью удаленного экземпляра Windows PowerShell пользователям должна быть назначена роль RBAC, имеющая разрешение на запуск командлета Test-CsVoiceTestConfiguration.</span><span class="sxs-lookup"><span data-stu-id="0625d-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsVoiceTestConfiguration cmdlet.</span></span> <span data-ttu-id="0625d-113">Чтобы просмотреть список всех ролей RBAC, которые могут использовать этот командлет, выполните в командной строке Windows PowerShell следующую команду:</span><span class="sxs-lookup"><span data-stu-id="0625d-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<p><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsVoiceTestConfiguration&quot;}</code></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="0625d-114">Описание</span><span class="sxs-lookup"><span data-stu-id="0625d-114">Description</span></span>

<span data-ttu-id="0625d-115">Lync Server включает несколько командлетов Windows PowerShell (например, Test-CsVoiceRoute и Test-CsVoicePolicy, Test-CsTrunkConfiguration), которые позволяют убедиться в том, что индивидуальные части инфраструктуры корпоративной голосовой связи – маршруты голосовой связи, политики голосовой связи, магистральные линии SIP — работают должным образом.</span><span class="sxs-lookup"><span data-stu-id="0625d-115">Lync Server includes several Windows PowerShell cmdlets (such as Test-CsVoiceRoute and Test-CsVoicePolicy, Test-CsTrunkConfiguration) that enable you to verify that the individual pieces of your Enterprise Voice infrastructure – voice routes, voice policies, SIP trunks – are working as expected.</span></span>

<span data-ttu-id="0625d-116">Несмотря на то, что в корпоративной голосовой связи все индивидуальные компоненты работают, вы можете использовать допустимый голосовой маршрут, действительную голосовую политику и действительную магистраль SIP, но при этом пользователи не смогут совершать и принимать телефонные звонки.</span><span class="sxs-lookup"><span data-stu-id="0625d-116">While it’s important with Enterprise Voice that all the individual pieces work: it’s possible to have a valid voice route, a valid voice policy, and a valid SIP trunk, but still have users unable to make or receive phone calls.</span></span> <span data-ttu-id="0625d-117">По этой причине Lync Server также предоставляет возможность создавать конфигурации тестовых тестов.</span><span class="sxs-lookup"><span data-stu-id="0625d-117">Because of that, Lync Server also provides the ability to create voice test configurations.</span></span> <span data-ttu-id="0625d-118">Конфигурации тестовых тестов — это распространенные сценарии для корпоративных клиентов: вы можете указать такие параметры, как голосовая связь, политика голосовой связи и абонентская группа, а затем убедиться, что эти индивидуальные элементы смогут работать вместе для предоставления услуг телефонной связи.</span><span class="sxs-lookup"><span data-stu-id="0625d-118">Voice test configurations represent common Enterprise Voice scenarios: you can specify such things as a voice route, a voice policy, and a dial plan, and then verify that those individual items are work able to work together to provide phone service.</span></span> <span data-ttu-id="0625d-119">Кроме того, вы можете проверить свои ожидания в указанном сценарии.</span><span class="sxs-lookup"><span data-stu-id="0625d-119">In addition, you can validate your expectations in a given scenario.</span></span> <span data-ttu-id="0625d-120">Например, предположим, что сочетание абонентов и политик голосовой связи "B" привело бы к переадресации звонков по голосовой маршруту C. Вы можете ввести голосовой маршрут C в качестве ExpectedRoute.</span><span class="sxs-lookup"><span data-stu-id="0625d-120">For example, suppose that you expect that the combination of dial plan A and voice policy B would result in calls being routed over voice route C. You can enter voice route C as the ExpectedRoute.</span></span> <span data-ttu-id="0625d-121">Если при выполнении теста маршрут "C" не установлен, проверка будет помечена как невыполненная.</span><span class="sxs-lookup"><span data-stu-id="0625d-121">When you run the test, if voice route C is not employed then the test will be marked as having failed.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="0625d-122">Выполнение теста</span><span class="sxs-lookup"><span data-stu-id="0625d-122">Running the test</span></span>

<span data-ttu-id="0625d-123">Перед тестированием коллекций голосовой конфигурации с помощью Windows PowerShell необходимо сначала использовать командлет Get-CsVoiceTestConfiguration, чтобы получить экземпляр этих параметров конфигурации.</span><span class="sxs-lookup"><span data-stu-id="0625d-123">Before testing Voice configuration collections using Windows PowerShell, you must first use the Get-CsVoiceTestConfiguration cmdlet to retrieve an instance of these configuration settings.</span></span> <span data-ttu-id="0625d-124">Затем этот экземпляр должен быть передан в тест-CsVoiceTestConfiguration.</span><span class="sxs-lookup"><span data-stu-id="0625d-124">That instance must then be piped to the Test-CsVoiceTestConfiguration.</span></span> <span data-ttu-id="0625d-125">Например:</span><span class="sxs-lookup"><span data-stu-id="0625d-125">For example:</span></span>

`Get-CsVoiceTestConfiguration -Identity "RedmondVoiceTestConfiguration" | Test-CsVoiceTestConfiguration`

<span data-ttu-id="0625d-126">Для одновременной проверки всех параметров конфигурации голосового теста используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="0625d-126">To validate all the voice test configuration settings at the same time, use this command instead:</span></span>

`Get-CsVoiceTestConfiguration | Test-CsVoiceTestConfiguration`

<span data-ttu-id="0625d-127">Дополнительные сведения можно найти в справочной документации по командлету Test-CsVoiceTestConfiguration.</span><span class="sxs-lookup"><span data-stu-id="0625d-127">For more information, see the Help documentation for the Test-CsVoiceTestConfiguration cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="0625d-128">Определение успеха или сбоя</span><span class="sxs-lookup"><span data-stu-id="0625d-128">Determining success or failure</span></span>

<span data-ttu-id="0625d-129">Командлет Test-CsVoiceTestConfiguration сообщает об ошибке теста или его успешности, а также предоставляет дополнительные сведения о каждом успешном прохождении теста, такие как правила трансляции, Голосовые маршруты и использование PSTN, используемое для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="0625d-129">The Test-CsVoiceTestConfiguration cmdlet reports whether a test failed or succeeded, and provides additional information about each successful test, such as the translation rule, voice route, and PSTN usage used to complete the task:</span></span>

<span data-ttu-id="0625d-130">Результат: успех</span><span class="sxs-lookup"><span data-stu-id="0625d-130">Result:             Success</span></span>

<span data-ttu-id="0625d-131">TranslatedNumber: + 15551234</span><span class="sxs-lookup"><span data-stu-id="0625d-131">TranslatedNumber:   +15551234</span></span>

<span data-ttu-id="0625d-132">MatchingRule: описание =; Шаблон = ^ ( \\ d {4} ) $; Преобразование = + 1 \\ d; Name = Test; IsInternalExtension = false</span><span class="sxs-lookup"><span data-stu-id="0625d-132">MatchingRule:       Description=;Pattern=^(\\d{4})$;Translation=+1\\d;Name=Test;IsInternalExtension=False</span></span>

<span data-ttu-id="0625d-133">FirstMatchingRoute: сайт: Redmond</span><span class="sxs-lookup"><span data-stu-id="0625d-133">FirstMatchingRoute: site:Redmond</span></span>

<span data-ttu-id="0625d-134">MatchingUsage: local</span><span class="sxs-lookup"><span data-stu-id="0625d-134">MatchingUsage:      Local</span></span>

<span data-ttu-id="0625d-135">Если тест не удалось выполнить, результат будет указан как ошибка.</span><span class="sxs-lookup"><span data-stu-id="0625d-135">If the test fails then the result is reported as Fail:</span></span>

<span data-ttu-id="0625d-136">Результат: Failed</span><span class="sxs-lookup"><span data-stu-id="0625d-136">Result:             Fail</span></span>

<span data-ttu-id="0625d-137">TranslatedNumber:</span><span class="sxs-lookup"><span data-stu-id="0625d-137">TranslatedNumber:</span></span>   

<span data-ttu-id="0625d-138">FirstMatchingRoute:</span><span class="sxs-lookup"><span data-stu-id="0625d-138">FirstMatchingRoute:</span></span>

<span data-ttu-id="0625d-139">MatchingUsage:</span><span class="sxs-lookup"><span data-stu-id="0625d-139">MatchingUsage:</span></span>      

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="0625d-140">Причины, по которым может произойти сбой теста</span><span class="sxs-lookup"><span data-stu-id="0625d-140">Reasons why the test might have failed</span></span>

<span data-ttu-id="0625d-141">Поскольку тестирование конфигурации для проверки правописания проверяет несколько различных элементов, в том числе политики голосовой связи, абонентские группы, маршруты голосовой почты и т. д., это может привести к неудачному тесту.</span><span class="sxs-lookup"><span data-stu-id="0625d-141">Because voice test configuration testing tests several different items – including voice policies, dial plans, voice routes, and so on – there are several different factors that could result in a failed test.</span></span> <span data-ttu-id="0625d-142">Если тест завершается сбоем, первым шагом необходимо проверить параметры конфигурации с помощью командлета Get-CsVoiceTestConfiguration:</span><span class="sxs-lookup"><span data-stu-id="0625d-142">If a test fails, your first step should be to review the configuration settings themselves by using the Get-CsVoiceTestConfiguration cmdlet:</span></span>

`Get-CsVoiceTestConfiguration -Identity "RedmondVoiceTestConfiguration"`

<span data-ttu-id="0625d-143">Если параметры настроены правильно, повторно выполните тест, включив параметр Verbose.</span><span class="sxs-lookup"><span data-stu-id="0625d-143">If the settings seem to be configured correctly, re-run the test while including the Verbose parameter:</span></span>

`Get-CsVoiceTestConfiguration -Identity "RedmondVoiceTestConfiguration" | Test-CsVoiceTestConfiguration`

<span data-ttu-id="0625d-144">Параметр подробных данных предоставит пошаговые инструкции для каждого действия, выполненного Test-CsVoiceTestConfiguration, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="0625d-144">The Verbose parameter will provide a step-by-step account of each action taken by Test-CsVoiceTestConfiguration as shown in this example:</span></span>

<span data-ttu-id="0625d-145">ПОДРОБНЫй: Загрузка абонентской группы: "Global"</span><span class="sxs-lookup"><span data-stu-id="0625d-145">VERBOSE: Loading dial plan: "Global"</span></span>

<span data-ttu-id="0625d-146">ПОДРОБНЫй: Загрузка политики голосовой связи: "RedmondDialPlan"</span><span class="sxs-lookup"><span data-stu-id="0625d-146">VERBOSE: Loading voice policy: "RedmondDialPlan"</span></span>

<span data-ttu-id="0625d-147">Эта пошаговая учетная запись может быть полезна в том случае, если тест действительно завершился сбоем.</span><span class="sxs-lookup"><span data-stu-id="0625d-147">This step-by-step account might provide a useful clue as to where the test actually failed.</span></span> <span data-ttu-id="0625d-148">В противном случае вы можете использовать другие командлеты Windows PowerShell (например, Test-CsVoicePolicy) и methodically Begin для проверки отдельных компонентов, которые включены в параметры конфигурации голосового теста.</span><span class="sxs-lookup"><span data-stu-id="0625d-148">If not, you can then use other Windows PowerShell cmdlets (such as Test-CsVoicePolicy) and methodically begin to verify the individual components that are included in the voice test configuration settings.</span></span>

<span data-ttu-id="0625d-149">Кроме того, обратите внимание на то, что тест может перенаправлять вызов, но все еще не помечается как сбой. Это может произойти, если вы ввели значения для ExpectedRoute, ExpectedTranslatedNumber и ExpectedUsage, и любые из этих ожиданий не будут удовлетворены.</span><span class="sxs-lookup"><span data-stu-id="0625d-149">In addition to that, be aware that it’s possible for a test to be able to route a call and yet still be marked as a failure; that can occur if you enter values for ExpectedRoute, ExpectedTranslatedNumber, and ExpectedUsage, and any of those expectations are not met.</span></span> <span data-ttu-id="0625d-150">Например, предположим, что вы ввели голосовую переадресацию в качестве ожидаемого голоса, но проверка завершит звонок с помощью голосового маршрута г. В этом случае тест будет помечен как сбой, так как ожидаемый маршрут голосовой связи не использовался.</span><span class="sxs-lookup"><span data-stu-id="0625d-150">For example, suppose that you enter voice route C as your expected voice route, but the test actually completes the call using voice route D. In that case the test will be marked as Failed because the expected voice route was not used.</span></span> <span data-ttu-id="0625d-151">Если тест завершается сбоем, вы можете удалить значения для ExpectedRoute, ExpectedTranslatedNumber и ExpectedUsage, а затем повторно выполнить тест.</span><span class="sxs-lookup"><span data-stu-id="0625d-151">If a test fails, you might remove the values for ExpectedRoute, ExpectedTranslatedNumber, and ExpectedUsage and then re-run the test.</span></span> <span data-ttu-id="0625d-152">Это поможет вам определить, завершился ли сбой из-за того, что не удалось выполнить звонок или вы ожидаете одного и фактического получения другого.</span><span class="sxs-lookup"><span data-stu-id="0625d-152">That will help you determine whether the failure was because the call couldn't be completed, or because you expect one thing and actually received another.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="0625d-153">См. также</span><span class="sxs-lookup"><span data-stu-id="0625d-153">See Also</span></span>


[<span data-ttu-id="0625d-154">Test-CsVoiceTestConfiguration</span><span class="sxs-lookup"><span data-stu-id="0625d-154">Test-CsVoiceTestConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsVoiceTestConfiguration)  
  

<span data-ttu-id="0625d-155"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0625d-155"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

