---
title: 'Lync Server 2013: Проверка правил голосовой связи, маршрутов и политик'
description: 'Lync Server 2013: проверьте правила голосовой связи, маршруты и политики.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test voice rules, routes, and policies
ms:assetid: ebb9c3fa-6950-4311-87ca-e1ecd9280a43
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn725213(v=OCS.15)
ms:contentKeyID: 63969661
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: cf205ac2585298dfc5347d93e382e8bbda9f3ff4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398062"
---
# <a name="test-voice-rules-routes-and-policies-in-lync-server-2013"></a><span data-ttu-id="0e28b-103">Проверка правил, маршрутов и политик голосовой связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0e28b-103">Test voice rules, routes, and policies in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0e28b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0e28b-104">

<span> </span></span></span>

<span data-ttu-id="0e28b-105">_**Тема последнего изменения:** 2014-05-20_</span><span class="sxs-lookup"><span data-stu-id="0e28b-105">_**Topic Last Modified:** 2014-05-20_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0e28b-106">Расписание проверки</span><span class="sxs-lookup"><span data-stu-id="0e28b-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="0e28b-107">Ежемесячно</span><span class="sxs-lookup"><span data-stu-id="0e28b-107">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e28b-108">Средство тестирования</span><span class="sxs-lookup"><span data-stu-id="0e28b-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="0e28b-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="0e28b-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e28b-110">Требуемые разрешения</span><span class="sxs-lookup"><span data-stu-id="0e28b-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="0e28b-111">При локальном запуске с помощью командной консоли Lync Server пользователи должны быть членами группы безопасности RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="0e28b-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="0e28b-112">При запуске с помощью удаленного экземпляра Windows PowerShell пользователям должна быть назначена роль RBAC, имеющая разрешение на запуск командлета Test-CsVoiceUser.</span><span class="sxs-lookup"><span data-stu-id="0e28b-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsVoiceUser cmdlet.</span></span> <span data-ttu-id="0e28b-113">Чтобы просмотреть список всех ролей RBAC, которые могут использовать этот командлет, выполните в командной строке Windows PowerShell следующую команду:</span><span class="sxs-lookup"><span data-stu-id="0e28b-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<p><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsVoiceUser&quot;}</code></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="0e28b-114">Описание</span><span class="sxs-lookup"><span data-stu-id="0e28b-114">Description</span></span>

<span data-ttu-id="0e28b-115">Когда пользователь выполняет телефонный звонок, маршрут, по которому выполняется звонок, зависит от политик и абонентских тарифов, назначенных этому пользователю.</span><span class="sxs-lookup"><span data-stu-id="0e28b-115">When a user makes a phone call, the route the call takes to reach its destination depends on both the policies and dial plans assigned to that user.</span></span> <span data-ttu-id="0e28b-116">Если у пользователя есть SIP-адрес и номер телефона, командлет Test-CsVoiceUser проверяет, может ли пользователь выполнить Звонок на этот номер.</span><span class="sxs-lookup"><span data-stu-id="0e28b-116">Given a user’s SIP address and a phone number, the Test-CsVoiceUser cmdlet verifies whether the user in question can complete a call to that number.</span></span> <span data-ttu-id="0e28b-117">Если проверка выполнена успешно, Test-CsVoiceUser возвращает следующее:</span><span class="sxs-lookup"><span data-stu-id="0e28b-117">If the test succeeds, Test-CsVoiceUser returns the following:</span></span>

  - <span data-ttu-id="0e28b-118">Число преобразовано в формат E. 164 (в соответствии с абонентской панелью пользователя).</span><span class="sxs-lookup"><span data-stu-id="0e28b-118">The number translated to E.164 format (based on the user’s dial plan)</span></span>

  - <span data-ttu-id="0e28b-119">Правило нормализации, которое предоставляет этот перевод</span><span class="sxs-lookup"><span data-stu-id="0e28b-119">The normalization rule that supplied that translation</span></span>

  - <span data-ttu-id="0e28b-120">Используемый маршрут голоса (на основе приоритета маршрута);</span><span class="sxs-lookup"><span data-stu-id="0e28b-120">The voice route used (based on route priority);</span></span>

  - <span data-ttu-id="0e28b-121">Использование телефона, связанного с политикой голосовой связи пользователя, с голосовым маршрутом.</span><span class="sxs-lookup"><span data-stu-id="0e28b-121">The phone usage that linked the user’s voice policy to the voice route.</span></span>

<span data-ttu-id="0e28b-122">Test-CsVoiceUser позволяет определить, нужно ли перенаправлять и перевести конкретный номер телефона, и это поможет устранить проблемы, связанные с вызовами, которые могут возникнуть у отдельных пользователей.</span><span class="sxs-lookup"><span data-stu-id="0e28b-122">Test-CsVoiceUser enables you to determine whether a specific phone number will route and translate as expected, and can help troubleshoot call-related problems that are experienced by individual users.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="0e28b-123">Выполнение теста</span><span class="sxs-lookup"><span data-stu-id="0e28b-123">Running the test</span></span>

<span data-ttu-id="0e28b-124">При запуске командлета Test-CsVoiceUser необходимо указать два фрагмента данных: номер набора номера (DialedNumber) и идентификация проверяемой учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="0e28b-124">When running the Test-CsVoiceUser cmdlet you must supply two pieces of information: the number being dialed (DialedNumber) and the Identity of the user account being tested.</span></span> <span data-ttu-id="0e28b-125">Например, эта команда проверяет возможность пользователя, у которого есть SIP-адрес sip:kenmyer@litwareinc.com, звонить на номер телефона + 1206555-1219:</span><span class="sxs-lookup"><span data-stu-id="0e28b-125">For example, this command tests the ability of the user who has the SIP address sip:kenmyer@litwareinc.com to make a call to the phone number +1206555-1219:</span></span>

`Test-CsVoiceUser -DialedNumber "12065551219" -SipUri "sip:kenmyer@litwareinc.com"`

<span data-ttu-id="0e28b-126">Номер телефона должен быть отформатирован так, как вы планируете набрать его.</span><span class="sxs-lookup"><span data-stu-id="0e28b-126">The phone number should be formatted in the way that you expect it to be dialed.</span></span> <span data-ttu-id="0e28b-127">Например, если пользователи, как правило, не набирает номер 1 перед тем, как звонить по междугородней связи, следует использовать следующий формат:</span><span class="sxs-lookup"><span data-stu-id="0e28b-127">For example, if users typically do not dial the 1 before placing a long distance call then you should use this format:</span></span>

`-DialedNumber "2065551219"`

<span data-ttu-id="0e28b-128">Разумеется, в этом случае тест завершится ошибкой, если у вас нет правила нормализации, позволяющего правильно перевести число 2065551219 в формат телефона E. 164, который используется в Lync Server.</span><span class="sxs-lookup"><span data-stu-id="0e28b-128">Of course, in that case, the test will fail if you do not have a normalization rule that can correctly translate the number 2065551219 into the E.164 telephone format that is used by Lync Server.</span></span> <span data-ttu-id="0e28b-129">Дополнительные сведения можно найти в разделе справки New-CsVoiceNormalizationRule командлет.</span><span class="sxs-lookup"><span data-stu-id="0e28b-129">For more information, see the help topic New-CsVoiceNormalizationRule cmdlet.</span></span>

<span data-ttu-id="0e28b-130">Если вы хотите выполнить этот же тест для каждой учетной записи пользователя, вы можете использовать команду, подобную следующей:</span><span class="sxs-lookup"><span data-stu-id="0e28b-130">If you want to run this same test against each of your user accounts, you can use a command similar to the following:</span></span>

`Get-CsUser | ForEach-Object {$_.DisplayName; Test-CsVoiceUser -DialedNumber "+12065551219" -SipUri $_.SipAddress} | Format-List`

<span data-ttu-id="0e28b-131">Дополнительные сведения можно найти в справочной документации по командлету Test-CsVoiceUser.</span><span class="sxs-lookup"><span data-stu-id="0e28b-131">For more information, see the Help documentation for the Test-CsVoiceUser cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="0e28b-132">Определение успеха или сбоя</span><span class="sxs-lookup"><span data-stu-id="0e28b-132">Determining success or failure</span></span>

<span data-ttu-id="0e28b-133">Если проверка выполнена успешно (то есть, если пользователь может выполнить телефонный звонок на указанный номер), на выходе будут показаны такие данные, как переведенный номер телефона, а также соответствующее правило нормализации и голосовой маршрут.</span><span class="sxs-lookup"><span data-stu-id="0e28b-133">If the test is completed successfully (that is, if the user can make a phone call to the specified number), the output will show information like the translated phone number and the matching normalization rule and voice route:</span></span>

<span data-ttu-id="0e28b-134">TranslatedNumber MatchingRule FirstMatchingRoute MatchingUsage</span><span class="sxs-lookup"><span data-stu-id="0e28b-134">TranslatedNumber    MatchingRule    FirstMatchingRoute    MatchingUsage</span></span>

<span data-ttu-id="0e28b-135">\----------------    ------------    ------------------    -------------</span><span class="sxs-lookup"><span data-stu-id="0e28b-135">\----------------    ------------    ------------------    -------------</span></span>

<span data-ttu-id="0e28b-136">\+12065551219 Descripti...    Локальный LocalRoute</span><span class="sxs-lookup"><span data-stu-id="0e28b-136">\+12065551219        Descripti...    LocalRoute            Local</span></span>

<span data-ttu-id="0e28b-137">Из-за ограничений на экран Windows PowerShell по крайней мере некоторые возвращенные сведения (особенно важно, полное описание соответствующего правила нормализации) могут не отображаться на экране.</span><span class="sxs-lookup"><span data-stu-id="0e28b-137">Because of the limitations of the Windows PowerShell screen, at least some returned information (most notably the full description of the matching normalization rule) might not appear on-screen.</span></span> <span data-ttu-id="0e28b-138">Если вы заинтересованы в успешном или неуспешном выполнении теста, это может быть неважно.</span><span class="sxs-lookup"><span data-stu-id="0e28b-138">If you are only interested in the success or failure of the test, then this might not matter.</span></span> <span data-ttu-id="0e28b-139">Если вы хотите просмотреть полные сведения о возвращенных данных, переводите выходные данные в командлет Format-List при выполнении теста.</span><span class="sxs-lookup"><span data-stu-id="0e28b-139">If you would prefer to see the full details of the returned data then pipe the output to the Format-List cmdlet when running the test:</span></span>

`Test-CsVoiceUser -DialedNumber "+12065551219" -SipUri "sip:kenmyer@litwareinc.com" -Verbose | Format-List`

<span data-ttu-id="0e28b-140">Это приведет к отображению выходных данных в более удобном формате для чтения:</span><span class="sxs-lookup"><span data-stu-id="0e28b-140">That will display the output in a more reader-friendly format:</span></span>

<span data-ttu-id="0e28b-141">TranslatedNumber: + 12065551219</span><span class="sxs-lookup"><span data-stu-id="0e28b-141">TranslatedNumber : +12065551219</span></span>

<span data-ttu-id="0e28b-142">MatchingRule: описание =; Шаблон = ^ ( \\ d {11} ) $; Перевод = + $1;</span><span class="sxs-lookup"><span data-stu-id="0e28b-142">MatchingRule : Description=;Pattern=^(\\d{11})$;Translation=+$1;</span></span>

<span data-ttu-id="0e28b-143">Name = prefix ALL; IsInternalExtension = false</span><span class="sxs-lookup"><span data-stu-id="0e28b-143">Name=Prefix All;IsInternalExtension=False</span></span>

<span data-ttu-id="0e28b-144">FirsMatchingRoute : LocalRoute</span><span class="sxs-lookup"><span data-stu-id="0e28b-144">FirsMatchingRoute : LocalRoute</span></span>

<span data-ttu-id="0e28b-145">MatchingUsage: local</span><span class="sxs-lookup"><span data-stu-id="0e28b-145">MatchingUsage : Local</span></span>

<span data-ttu-id="0e28b-146">В случае сбоя теста Test-CsVoiceUser будет возвращать пустой набор значений свойств.</span><span class="sxs-lookup"><span data-stu-id="0e28b-146">If the test fails, Test-CsVoiceUser will return an empty set of property values:</span></span>

<span data-ttu-id="0e28b-147">TranslatedNumber MatchingRule FirstMatchingRoute MatchingUsage</span><span class="sxs-lookup"><span data-stu-id="0e28b-147">TranslatedNumber MatchingRule FirstMatchingRoute MatchingUsage</span></span>

<span data-ttu-id="0e28b-148">\---------------- ------------ ------------------ -------------</span><span class="sxs-lookup"><span data-stu-id="0e28b-148">\---------------- ------------ ------------------ -------------</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="0e28b-149">Причины, по которым может произойти сбой теста</span><span class="sxs-lookup"><span data-stu-id="0e28b-149">Reasons why the test might have failed</span></span>

<span data-ttu-id="0e28b-150">Существует несколько причин, по которым может произойти сбой командлета Test-CsVoiceUser: возможно, правило нормализации, которое может перевести указанный номер телефона, не существует.</span><span class="sxs-lookup"><span data-stu-id="0e28b-150">There are any number of reasons why the Test-CsVoiceUser cmdlet might fail: there might not be a normalization rule that can translate the provided phone number.</span></span> <span data-ttu-id="0e28b-151">Возможно, возникли проблемы с голосовым маршрутом.</span><span class="sxs-lookup"><span data-stu-id="0e28b-151">There could be problems with the voice route.</span></span> <span data-ttu-id="0e28b-152">Возможно, у вас возникла ошибка конфигурации для абонентской группы, назначенной пользователю.</span><span class="sxs-lookup"><span data-stu-id="0e28b-152">There could be a configuration issue with the dial plan assigned to the user in question.</span></span> <span data-ttu-id="0e28b-153">По этой причине при запуске командлета Test-CsVoiceUser может потребоваться включить параметр Verbose.</span><span class="sxs-lookup"><span data-stu-id="0e28b-153">Because of that, you might want to include the Verbose parameter when you are running the Test-CsVoiceUser cmdlet:</span></span>

`Test-CsVoiceUser -DialedNumber "+12065551219" -SipUri "sip:kenmyer@litwareinc.com" -Verbose`

<span data-ttu-id="0e28b-154">Когда вы включаете подробный командлет, Test-CsVoiceUser выдает подробные сведения о всех действиях, выполняемых при проведении проверок.</span><span class="sxs-lookup"><span data-stu-id="0e28b-154">When the Verbose cmdlet is included, Test-CsVoiceUser will issue a detailed account of all the steps in takes when conducting its checks.</span></span> <span data-ttu-id="0e28b-155">Например, вы можете увидеть шаги, аналогичные указанным ниже.</span><span class="sxs-lookup"><span data-stu-id="0e28b-155">For example, you might see steps similar to these:</span></span> 

<span data-ttu-id="0e28b-156">VERBOSE: Поиск пользователей с удостоверением "sip:kenmyer@litwareinc.com"</span><span class="sxs-lookup"><span data-stu-id="0e28b-156">VERBOSE: Locating user with identity "sip:kenmyer@litwareinc.com"</span></span>

<span data-ttu-id="0e28b-157">VERBOSE: Загрузка абонентской группы: "RedmondDialPlan"</span><span class="sxs-lookup"><span data-stu-id="0e28b-157">VERBOSE: Loading dial plan: "RedmondDialPlan"</span></span>

<span data-ttu-id="0e28b-158">Дополнительные сведения можно найти в разделе действия, которые можно выполнить для выявления причины сбоя.</span><span class="sxs-lookup"><span data-stu-id="0e28b-158">This additional information can provide hints as to the steps that you can take to pinpoint the cause of the failure.</span></span> <span data-ttu-id="0e28b-159">Например, подробный вывод показывает, что тестируемому пользователю назначена абонентская группа RedmondDialPlan.</span><span class="sxs-lookup"><span data-stu-id="0e28b-159">For example, the verbose output shown here tells us that the user being tested was assigned the dial plan RedmondDialPlan.</span></span> <span data-ttu-id="0e28b-160">Если тест завершился сбоем, следующим логическим шагом будет проверка того, что RedmondDialPlan может перевести предоставленный телефонный номер.</span><span class="sxs-lookup"><span data-stu-id="0e28b-160">If the test has failed, one logical next step would be to verify that RedmondDialPlan can translate the supplied phone number.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="0e28b-161">См. также</span><span class="sxs-lookup"><span data-stu-id="0e28b-161">See Also</span></span>


[<span data-ttu-id="0e28b-162">Test-CsVoiceUser</span><span class="sxs-lookup"><span data-stu-id="0e28b-162">Test-CsVoiceUser</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsVoiceUser)  
  

<span data-ttu-id="0e28b-163"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0e28b-163"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

