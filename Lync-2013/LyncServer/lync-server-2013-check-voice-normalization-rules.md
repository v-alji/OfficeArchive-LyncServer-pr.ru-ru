---
title: 'Lync Server 2013: Проверка правил нормализации голосовых сообщений'
description: 'Lync Server 2013: Проверка правил нормализации голосовой связи.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Check voice normalization rules
ms:assetid: bf71a218-71cd-4b64-b8e8-b3a98b6e87a2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn725212(v=OCS.15)
ms:contentKeyID: 63969649
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f68bbde24a3dc7d8e8214dcfe506d4b8112fbbb3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435007"
---
# <a name="check-voice-normalization-rules-in-lync-server-2013"></a><span data-ttu-id="f93ed-103">Проверка правил нормализации голосовых сообщений в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f93ed-103">Check voice normalization rules in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f93ed-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f93ed-104">

<span> </span></span></span>

<span data-ttu-id="f93ed-105">_**Тема последнего изменения:** 2014-05-20_</span><span class="sxs-lookup"><span data-stu-id="f93ed-105">_**Topic Last Modified:** 2014-05-20_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f93ed-106">Расписание проверки</span><span class="sxs-lookup"><span data-stu-id="f93ed-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="f93ed-107">Ежемесячно</span><span class="sxs-lookup"><span data-stu-id="f93ed-107">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f93ed-108">Средство тестирования</span><span class="sxs-lookup"><span data-stu-id="f93ed-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="f93ed-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="f93ed-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f93ed-110">Требуемые разрешения</span><span class="sxs-lookup"><span data-stu-id="f93ed-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="f93ed-111">При локальном запуске с помощью командной консоли Lync Server пользователи должны быть членами группы безопасности RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="f93ed-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="f93ed-112">При запуске с помощью удаленного экземпляра Windows PowerShell пользователям должна быть назначена роль RBAC, имеющая разрешение на запуск командлета Test-CsVoiceNormalizationRule.</span><span class="sxs-lookup"><span data-stu-id="f93ed-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsVoiceNormalizationRule cmdlet.</span></span> <span data-ttu-id="f93ed-113">Чтобы просмотреть список всех ролей RBAC, которые могут использовать этот командлет, выполните в командной строке Windows PowerShell следующую команду:</span><span class="sxs-lookup"><span data-stu-id="f93ed-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<p><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsVoiceNormalizationRule&quot;}</code></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="f93ed-114">Описание</span><span class="sxs-lookup"><span data-stu-id="f93ed-114">Description</span></span>

<span data-ttu-id="f93ed-115">Правила нормализации голоса используются для преобразования номера телефона, набранного пользователем (например, 2065551219), в формат E. 164, который используется приложением Lync Server (+ 12065551219).</span><span class="sxs-lookup"><span data-stu-id="f93ed-115">Voice normalization rules are used to convert a phone number dialed by a user (for example, 2065551219) to the E.164 format that is used by Lync Server (+12065551219).</span></span> <span data-ttu-id="f93ed-116">Например, если пользователи находятся в привычке набрать номер телефона, не включая код страны или код города (например, 5551219), необходимо иметь правило нормализации голоса, которое может преобразовать этот номер в формат E. 164: + 12065551219.</span><span class="sxs-lookup"><span data-stu-id="f93ed-116">For example, if users are in the habit of dialing a phone number without including the country code or the area code (e.g., 5551219) then you must have a voice normalization rule that can convert that number to the E.164 format: +12065551219.</span></span> <span data-ttu-id="f93ed-117">Без такого правила пользователь не сможет позвонить в 555-1219.</span><span class="sxs-lookup"><span data-stu-id="f93ed-117">Without such a rule, the user won't be able to call 555-1219.</span></span>

<span data-ttu-id="f93ed-118">Командлет Test-CsVoiceNormalizationRule удостоверяется в том, что указанное правило нормализации голоса может успешно преобразовать указанный номер телефона.</span><span class="sxs-lookup"><span data-stu-id="f93ed-118">The Test-CsVoiceNormalizationRule cmdlet verifies that a specified voice normalization rule can successfully convert a specified phone number.</span></span> <span data-ttu-id="f93ed-119">Например, эта команда проверяет, может ли глобальная NoAreaCode правило нормализации нормализация и преобразование строки набора 5551219.</span><span class="sxs-lookup"><span data-stu-id="f93ed-119">For example, this command checks whether the global normalization rule NoAreaCode can normalize and convert the dial string 5551219.</span></span>

`Get-CsVoiceNormalizationRule -Identity "global/NoAreaCode" | Test-CsVoiceNormalizationRule -DialedNumber "5551219"`

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="f93ed-120">Выполнение теста</span><span class="sxs-lookup"><span data-stu-id="f93ed-120">Running the test</span></span>

<span data-ttu-id="f93ed-121">Чтобы запустить командлет Test-CsVoiceNormalizationRule, необходимо сначала использовать командлет Get-CsVoiceNormalizationRule, чтобы получить экземпляр тестируемого правила, а затем передать его в тест-CsVoiceNormalizationRule.</span><span class="sxs-lookup"><span data-stu-id="f93ed-121">To run the Test-CsVoiceNormalizationRule cmdlet, you must first use the Get-CsVoiceNormalizationRule cmdlet to retrieve an instance of the rule being tested, and then pipe that instance to Test-CsVoiceNormalizationRule.</span></span> <span data-ttu-id="f93ed-122">Синтаксис, похожий на этот, не подходит.</span><span class="sxs-lookup"><span data-stu-id="f93ed-122">Syntax similar to this won't work:</span></span>

<span data-ttu-id="f93ed-123">Test-CsVoiceNormalizationRule-DialedNumber "12065551219" – NormalizationRule "Global/prefix ALL"</span><span class="sxs-lookup"><span data-stu-id="f93ed-123">Test-CsVoiceNormalizationRule -DialedNumber "12065551219" –NormalizationRule "global/Prefix All"</span></span>

<span data-ttu-id="f93ed-124">Вместо этого используйте следующий синтаксис, объединяющий Get-CsVoiceNormalizationRuleные и командлеты Test-CsVoiceNormalizationRule.</span><span class="sxs-lookup"><span data-stu-id="f93ed-124">Instead, use syntax such as the following, which combines both the Get-CsVoiceNormalizationRule and the Test-CsVoiceNormalizationRule cmdlets:</span></span>

<span data-ttu-id="f93ed-125">Get-CsVoiceNormalizationRule-Identity "Global/prefix ALL" | Test-CsVoiceNormalizationRule DialedNumber "12065551219"</span><span class="sxs-lookup"><span data-stu-id="f93ed-125">Get-CsVoiceNormalizationRule -Identity "global/Prefix All" | Test-CsVoiceNormalizationRule -DialedNumber "12065551219"</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="f93ed-126">.</span><span class="sxs-lookup"><span data-stu-id="f93ed-126">.</span></span> <span data-ttu-id="f93ed-127">Кроме того, вы также можете использовать этот подход, чтобы получить экземпляр правила, а затем проверить правило по указанному номеру телефона.</span><span class="sxs-lookup"><span data-stu-id="f93ed-127">Or, you can also use this approach to retrieve an instance of a rule and then test that rule against a specified phone number:</span></span>



</div>

`$x = Get-CsVoiceNormalizationRule -Identity "global/Prefix All"`

`Test-CsVoiceNormalizationRule -DialedNumber "12065551219" -NormalizationRule $x`

<span data-ttu-id="f93ed-128">Введите значение параметра DialedNumber точно так же, как ожидается набор номера.</span><span class="sxs-lookup"><span data-stu-id="f93ed-128">Enter the value for the DialedNumber parameter exactly as you expect that number to be dialed.</span></span> <span data-ttu-id="f93ed-129">Например, если указанное правило нормализации голоса должно автоматически добавлять код страны (первый 1 в значении 12065551219), то вы должны выйти из кода страны.</span><span class="sxs-lookup"><span data-stu-id="f93ed-129">For example, if the specified voice normalization rule is supposed to automatically add the country code (the initial 1 in the value 12065551219) then you should leave off the country code:</span></span>

`-DialedNumber "2065551219"`

<span data-ttu-id="f93ed-130">Если правило настроено правильно, оно автоматически добавляет код страны при переводе номера в формат E. 164, который используется в Lync Server.</span><span class="sxs-lookup"><span data-stu-id="f93ed-130">If the rule is configured correctly, it will automatically add the country code when translating the number to the E.164 format that is used by Lync Server.</span></span>

<span data-ttu-id="f93ed-131">Дополнительные сведения можно найти в справочной документации по командлету Test-CsVoiceNormalizationRule.</span><span class="sxs-lookup"><span data-stu-id="f93ed-131">For more information, see the Help documentation for the Test-CsVoiceNormalizationRule cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="f93ed-132">Определение успеха или сбоя</span><span class="sxs-lookup"><span data-stu-id="f93ed-132">Determining success or failure</span></span>

<span data-ttu-id="f93ed-133">Если указанное правило нормализации голоса может перевести предоставленный номер, на экране будет отображаться переведенный номер.</span><span class="sxs-lookup"><span data-stu-id="f93ed-133">If the specified voice normalization rule can translate the supplied number then the translated number will be displayed on-screen:</span></span>

<span data-ttu-id="f93ed-134">TranslatedNumber</span><span class="sxs-lookup"><span data-stu-id="f93ed-134">TranslatedNumber</span></span>

\----------------

<span data-ttu-id="f93ed-135">\+12065551219</span><span class="sxs-lookup"><span data-stu-id="f93ed-135">\+12065551219</span></span>

<span data-ttu-id="f93ed-136">Если проверка завершится ошибкой, будет возвращено пустое переведенное число.</span><span class="sxs-lookup"><span data-stu-id="f93ed-136">If the test fails then a blank translated number will be returned:</span></span>

<span data-ttu-id="f93ed-137">TranslatedNumber</span><span class="sxs-lookup"><span data-stu-id="f93ed-137">TranslatedNumber</span></span>

\----------------

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="f93ed-138">Причины, по которым может произойти сбой теста</span><span class="sxs-lookup"><span data-stu-id="f93ed-138">Reasons why the test might have failed</span></span>

<span data-ttu-id="f93ed-139">Если Test-CsVoiceNormalizationRule возвращает переведенное число, которое означает, что указанное правило нормализации голоса не смогло перевести предоставленный телефонный номер в формат E. 164, который используется в Lync Server.</span><span class="sxs-lookup"><span data-stu-id="f93ed-139">If the Test-CsVoiceNormalizationRule does return a translated number that means that the specified voice normalization rule was unable to translate the supplied telephone number into the E.164 format that is used by Lync Server.</span></span> <span data-ttu-id="f93ed-140">Чтобы убедиться в том, что вы ввели правильный номер телефона, убедитесь в том, что он правильно введен.</span><span class="sxs-lookup"><span data-stu-id="f93ed-140">To verify that, first make sure that you typed the telephone number in correctly.</span></span> <span data-ttu-id="f93ed-141">Например, вы ожидаете, что правило нормализации голоса будет иметь проблемы при преобразовании числа, похожего на следующее:</span><span class="sxs-lookup"><span data-stu-id="f93ed-141">For example, you would expect your voice normalization rule to have problems translating a number similar to this:</span></span>

`-DialedNumber "1"`

<span data-ttu-id="f93ed-142">Если номер введен правильно, необходимо убедиться в том, что указанное правило нормализации предназначено для обработки этого номера телефона.</span><span class="sxs-lookup"><span data-stu-id="f93ed-142">Assuming the number was entered correctly, your next step should be to verify that the specified normalization rule is designed to handle that phone number.</span></span> <span data-ttu-id="f93ed-143">Например, одно правило нормализации может быть спроектировано для обработки формата 12065551219, но второе правило может быть спроектировано для обработки числа 2065551219.</span><span class="sxs-lookup"><span data-stu-id="f93ed-143">For example, one normalization rule might be designed to handle the format 12065551219, but a second rule might be designed to handle the number 2065551219.</span></span> <span data-ttu-id="f93ed-144">(Это тот же самый и тот же номер телефона, но и код страны 1 в самом начале.) Чтобы получить подробные сведения о правиле нормализации голосовой связи, выполните команду, подобную следующей:</span><span class="sxs-lookup"><span data-stu-id="f93ed-144">(That’s the same phone number, minus the country code 1 at the very beginning.) To return detailed information about a voice normalization rule, run a command similar to this:</span></span>

`Get-CsVoiceNormalizationRule -Identity "global/Prefix All" | Format-List`

<span data-ttu-id="f93ed-145">Чтобы получить подробные сведения о всех правилах нормализации голоса, выполните эту команду:</span><span class="sxs-lookup"><span data-stu-id="f93ed-145">To return detailed information about all the voice normalization rules, run this command instead:</span></span>

`Get-CsVoiceNormalizationRule | Format-List`

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="f93ed-146">См. также</span><span class="sxs-lookup"><span data-stu-id="f93ed-146">See Also</span></span>


[<span data-ttu-id="f93ed-147">Test-CsVoiceNormalizationRule</span><span class="sxs-lookup"><span data-stu-id="f93ed-147">Test-CsVoiceNormalizationRule</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsVoiceNormalizationRule)  
  

<span data-ttu-id="f93ed-148"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f93ed-148"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

