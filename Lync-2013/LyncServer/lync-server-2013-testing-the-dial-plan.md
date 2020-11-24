---
title: 'Lync Server 2013: Проверка абонентской группы'
description: 'Lync Server 2013: Проверка абонентской группы.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing the dial plan
ms:assetid: 70eec03c-aca3-4106-86a7-77ae96b53779
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn690130(v=OCS.15)
ms:contentKeyID: 63969616
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a0ef2e3fce9d1fbbb0186b1b7aef608834145d3e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49400171"
---
# <a name="testing-the-dial-plan-in-lync-server-2013"></a><span data-ttu-id="83c7f-103">Проверка абонентской группы в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="83c7f-103">Testing the dial plan in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="83c7f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="83c7f-104">

<span> </span></span></span>

<span data-ttu-id="83c7f-105">_**Тема последнего изменения:** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="83c7f-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="83c7f-106">Расписание проверки</span><span class="sxs-lookup"><span data-stu-id="83c7f-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="83c7f-107">Ежедневно</span><span class="sxs-lookup"><span data-stu-id="83c7f-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83c7f-108">Средство тестирования</span><span class="sxs-lookup"><span data-stu-id="83c7f-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="83c7f-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="83c7f-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83c7f-110">Требуемые разрешения</span><span class="sxs-lookup"><span data-stu-id="83c7f-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="83c7f-111">При локальном запуске с помощью командной консоли Lync Server пользователи должны быть членами группы безопасности RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="83c7f-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="83c7f-112">При запуске с помощью удаленного экземпляра Windows PowerShell пользователям должна быть назначена роль RBAC, имеющая разрешение на запуск командлета Test-CsDialPlan.</span><span class="sxs-lookup"><span data-stu-id="83c7f-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsDialPlan cmdlet.</span></span> <span data-ttu-id="83c7f-113">Чтобы просмотреть список всех ролей RBAC, которые могут использовать этот командлет, выполните в командной строке Windows PowerShell следующую команду:</span><span class="sxs-lookup"><span data-stu-id="83c7f-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsDialPlan&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="83c7f-114">Описание</span><span class="sxs-lookup"><span data-stu-id="83c7f-114">Description</span></span>

<span data-ttu-id="83c7f-115">Командлет Test-CsDialPlan позволяет видеть результаты применения абонентской группы к определенному номеру телефона.</span><span class="sxs-lookup"><span data-stu-id="83c7f-115">The Test-CsDialPlan cmdlet enables you to see the results of applying a dial plan to a given telephone number.</span></span> <span data-ttu-id="83c7f-116">Абонентские группы предоставляют сведения, например, как применяются правила нормализации, необходимые для того, чтобы пользователи корпоративной голосовой связи были звонить по телефону.</span><span class="sxs-lookup"><span data-stu-id="83c7f-116">Dial plans provide information, such as how normalization rules are applied, required to enable Enterprise Voice users to make telephone calls.</span></span> <span data-ttu-id="83c7f-117">При наборе номера и абонентской группы этот командлет проверит, какое правило нормализации в абонентской группе будет применено, и что будет переведенный номер.</span><span class="sxs-lookup"><span data-stu-id="83c7f-117">Given a dialed number and a dial plan, this cmdlet will verify which normalization rule within the dial plan will be applied and what the translated number will be.</span></span>

<span data-ttu-id="83c7f-118">Вы можете использовать этот командлет для устранения проблем с преобразованиями чисел или для проверки того, как применять правила к определенным числам.</span><span class="sxs-lookup"><span data-stu-id="83c7f-118">You can use this cmdlet for troubleshooting issues with number translations, or for verifying how to apply rules against certain numbers.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="83c7f-119">Выполнение теста</span><span class="sxs-lookup"><span data-stu-id="83c7f-119">Running the test</span></span>

<span data-ttu-id="83c7f-120">Для командлета Test-CsDialPlan необходимо выполнить два действия.</span><span class="sxs-lookup"><span data-stu-id="83c7f-120">The Test-CsDialPlan cmdlet requires you to do two things.</span></span> <span data-ttu-id="83c7f-121">Сначала необходимо получить экземпляр тестируемой абонентской группы; Это можно сделать с помощью командлета Get-CsDialPlan.</span><span class="sxs-lookup"><span data-stu-id="83c7f-121">First, you must obtain an instance of the dial plan being tested; that can be done by using the Get-CsDialPlan cmdlet.</span></span> <span data-ttu-id="83c7f-122">Во вторых, необходимо указать телефонный номер, который должен быть нормализован.</span><span class="sxs-lookup"><span data-stu-id="83c7f-122">Second, you must specify the phone number that has to be normalized.</span></span> <span data-ttu-id="83c7f-123">Формат, используемый для номера телефона, должен совпадать с номером, набранным и введенным пользователем.</span><span class="sxs-lookup"><span data-stu-id="83c7f-123">The format that is used for the phone number should match the number as dialed/entered by a user.</span></span> <span data-ttu-id="83c7f-124">Например, эта команда извлекает экземпляр абонентской группы RedmondDialPlan и проверяет, можно ли использовать номер телефона 12065551219.</span><span class="sxs-lookup"><span data-stu-id="83c7f-124">For example, this command retrieves an instance of the dial plan, RedmondDialPlan, and checks whether the phone number 12065551219 can be normalized:</span></span>

    Get-CsDialPlan -Identity "RedmondDialPlan" | Test-CsDialPlan -DialedNumber "12065551219" | Format-List

<span data-ttu-id="83c7f-125">Если у вас есть правило нормализации, которое автоматически добавляет код страны (в этом примере, 1) и код города (206), вам может потребоваться проверить номер телефона 5551219, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="83c7f-125">If you have a normalization rule that automatically adds the country code (in this example, 1) and the area code (206), then you might want to check the phone number 5551219, as follows:</span></span>

    Get-CsDialPlan -Identity "RedmondDialPlan" | Test-CsDialPlan -DialedNumber "5551219" | Format-List

<span data-ttu-id="83c7f-126">Дополнительные сведения можно найти в справочной документации по командлету [Test-CsDialPlan](https://docs.microsoft.com/powershell/module/skype/Test-CsDialPlan) .</span><span class="sxs-lookup"><span data-stu-id="83c7f-126">For more information, see the Help documentation for the [Test-CsDialPlan](https://docs.microsoft.com/powershell/module/skype/Test-CsDialPlan) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="83c7f-127">Определение успеха или сбоя</span><span class="sxs-lookup"><span data-stu-id="83c7f-127">Determining success or failure</span></span>

<span data-ttu-id="83c7f-128">Test-CsDialPlan отличается от многих командлетов тестирования Lync Server, так как он не только косвенно указывает, успешно ли прошел тестирование или завершилось сбоем.</span><span class="sxs-lookup"><span data-stu-id="83c7f-128">Test-CsDialPlan differs from many of the Lync Server test cmdlets because it only indirectly indicates whether a test succeeded or failed.</span></span> <span data-ttu-id="83c7f-129">При использовании Test-CsDialPlan не получается вывод результатов, похожий на результат:</span><span class="sxs-lookup"><span data-stu-id="83c7f-129">When using Test-CsDialPlan you do not receive back output similar to this with the Result clearly labeled:</span></span>

<span data-ttu-id="83c7f-130">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="83c7f-130">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="83c7f-131">Результат: успех</span><span class="sxs-lookup"><span data-stu-id="83c7f-131">Result : Success</span></span>

<span data-ttu-id="83c7f-132">Задержка: 00:00:06.8630376</span><span class="sxs-lookup"><span data-stu-id="83c7f-132">Latency : 00:00:06.8630376</span></span>

<span data-ttu-id="83c7f-133">Ошибки</span><span class="sxs-lookup"><span data-stu-id="83c7f-133">Error :</span></span>

<span data-ttu-id="83c7f-134">Диагностик</span><span class="sxs-lookup"><span data-stu-id="83c7f-134">Diagnosis :</span></span>

<span data-ttu-id="83c7f-135">Вместо этого, если Test-CsDialPlan выполняется успешно, вы получите сведения о правиле нормализации, которое могло бы успешно перевести и использовать указанный номер телефона:</span><span class="sxs-lookup"><span data-stu-id="83c7f-135">Instead, if Test-CsDialPlan succeeds, then you'll receive information about the normalization rule that was able to successfully translate and use the specified phone number:</span></span>

<span data-ttu-id="83c7f-136">TranslatedNumber: + 12065551219</span><span class="sxs-lookup"><span data-stu-id="83c7f-136">TranslatedNumber : +12065551219</span></span>

<span data-ttu-id="83c7f-137">MatchingRule: описание =; Шаблон = ^ ( \\ d (11)) $; Перевод = + $1;</span><span class="sxs-lookup"><span data-stu-id="83c7f-137">MatchingRule : Description=;Pattern=^(\\d(11))$;Translation=+$1;</span></span>

<span data-ttu-id="83c7f-138">Name = prefix (префикс); IsInternalExtension = false</span><span class="sxs-lookup"><span data-stu-id="83c7f-138">Name=Prefix All; IsInternalExtension=False</span></span>

<span data-ttu-id="83c7f-139">Если Test-CsDialPlan не удалось (то есть, если абонентская группа не имеет правила нормализации, которое может перевести указанный номер телефона), вы получите «пустой» вывод, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="83c7f-139">If Test-CsDialPlan fails (that is, if the dial plan does not have a normalization rule that can translate the specified phone number), you'll just receive “empty” output as follows:</span></span>

<span data-ttu-id="83c7f-140">TranslatedNumber :</span><span class="sxs-lookup"><span data-stu-id="83c7f-140">TranslatedNumber :</span></span>

<span data-ttu-id="83c7f-141">MatchingRule :</span><span class="sxs-lookup"><span data-stu-id="83c7f-141">MatchingRule :</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="83c7f-142">Причины, по которым может произойти сбой теста</span><span class="sxs-lookup"><span data-stu-id="83c7f-142">Reasons why the test might have failed</span></span>

<span data-ttu-id="83c7f-143">Ниже приведены некоторые распространенные причины, по которым может произойти сбой Test-CsDialPlan.</span><span class="sxs-lookup"><span data-stu-id="83c7f-143">Here are some common reasons why Test-CsDialPlan might fail:</span></span>

  - <span data-ttu-id="83c7f-144">Возможно, вы использовали неверный формат при указании номера телефона.</span><span class="sxs-lookup"><span data-stu-id="83c7f-144">You might have used an incorrect format when specifying the phone number.</span></span> <span data-ttu-id="83c7f-145">Абонентские планы включают правила нормализации, позволяющие серверу Lync Server переводить телефонные номера, набранные или введенные пользователем.</span><span class="sxs-lookup"><span data-stu-id="83c7f-145">Dial plans include normalization rules that enable Lync Server to translate the phone numbers dialed or entered by a user.</span></span> <span data-ttu-id="83c7f-146">Поэтому абонентская группа должна иметь правила нормализации, соответствующие числам, которые пользователи могут набрать.</span><span class="sxs-lookup"><span data-stu-id="83c7f-146">Therefore, your dial plan should have normalization rules that match the numbers users are likely to dial.</span></span> <span data-ttu-id="83c7f-147">Например, если пользователь может набрать код страны, код города, а затем сам номер телефона, это означает, что абонентская группа должна иметь правило нормализации для обработки телефонных номеров, например:</span><span class="sxs-lookup"><span data-stu-id="83c7f-147">For example, if users might dial the country code, area code, and then the phone number itself, that means that your dial plan should have a normalization rule to handle phone numbers such as this:</span></span>
    
    <span data-ttu-id="83c7f-148">12065551219</span><span class="sxs-lookup"><span data-stu-id="83c7f-148">12065551219</span></span>
    
    <span data-ttu-id="83c7f-149">Тем не менее, если ввести неправильный телефонный номер (например, выход из последней цифры), Test-CsDialPlan завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="83c7f-149">However, if you enter an incorrect phone number (for example, leaving off the final digit), then Test-CsDialPlan will fail.</span></span> <span data-ttu-id="83c7f-150">Это не значит, что абонентская группа является неисправной, но из-за того, что вы ввели номер телефона, который не удается интерпретировать.</span><span class="sxs-lookup"><span data-stu-id="83c7f-150">That’s not because the dial plan is faulty but because you have entered a phone number than can’t be interpreted.</span></span>

<span data-ttu-id="83c7f-151"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="83c7f-151"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

