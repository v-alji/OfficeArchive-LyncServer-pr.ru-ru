---
title: 'Lync Server 2013: Проверка номера телефона на маршруте голосовой связи'
description: 'Lync Server 2013: Проверка номера телефона на маршруте голосовой связи.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test telephone number against a voice route
ms:assetid: 9a77ed6d-9394-4bef-9344-3d91b6959b97
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn725211(v=OCS.15)
ms:contentKeyID: 63969631
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 789f4a538a992a72abf61f4c1fbdb98370f2e643
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444240"
---
# <a name="test-telephone-number-against-a-voice-route-in-lync-server-2013"></a><span data-ttu-id="d69ed-103">Проверка номера телефона на маршруте голосовой связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d69ed-103">Test telephone number against a voice route in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d69ed-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d69ed-104">

<span> </span></span></span>

<span data-ttu-id="d69ed-105">_**Тема последнего изменения:** 2014-05-20_</span><span class="sxs-lookup"><span data-stu-id="d69ed-105">_**Topic Last Modified:** 2014-05-20_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d69ed-106">Расписание проверки</span><span class="sxs-lookup"><span data-stu-id="d69ed-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="d69ed-107">Ежемесячно</span><span class="sxs-lookup"><span data-stu-id="d69ed-107">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d69ed-108">Средство тестирования</span><span class="sxs-lookup"><span data-stu-id="d69ed-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="d69ed-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="d69ed-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d69ed-110">Требуемые разрешения</span><span class="sxs-lookup"><span data-stu-id="d69ed-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="d69ed-111">При локальном запуске с помощью командной консоли Lync Server пользователи должны быть членами группы безопасности RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="d69ed-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="d69ed-112">При запуске с помощью удаленного экземпляра Windows PowerShell пользователям должна быть назначена роль RBAC, имеющая разрешение на запуск командлета Test-CsVoiceRoute.</span><span class="sxs-lookup"><span data-stu-id="d69ed-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsVoiceRoute cmdlet.</span></span> <span data-ttu-id="d69ed-113">Чтобы просмотреть список всех ролей RBAC, которые могут использовать этот командлет, выполните в командной строке Windows PowerShell следующую команду:</span><span class="sxs-lookup"><span data-stu-id="d69ed-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<p><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsVoiceRoute&quot;}</code></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="d69ed-114">Описание</span><span class="sxs-lookup"><span data-stu-id="d69ed-114">Description</span></span>

<span data-ttu-id="d69ed-115">Голосовые маршруты работают вместе с голосовыми политиками, помогающие перенаправлять голосовые звонки в сеть PSTN.</span><span class="sxs-lookup"><span data-stu-id="d69ed-115">Voice routes work together with voice policies to help route Enterprise Voice calls to the PSTN network.</span></span> <span data-ttu-id="d69ed-116">Каждый маршрут голосовой связи содержит регулярное выражение (шаблон номера), который определяет номера телефонов, которые будут маршрутизироваться по данному голосовому маршруту. маршрут сможет обрабатывать любые телефонные номера, соответствующие этому регулярному выражению.</span><span class="sxs-lookup"><span data-stu-id="d69ed-116">Each voice route includes a regular expression (a number pattern) that identifies the phone numbers that will be routed through a given voice route: the route will be able to handle any phone numbers that match this regular expression.</span></span> <span data-ttu-id="d69ed-117">Например, голосовой маршрут может иметь регулярное выражение, которое позволяет ему обрабатывать любое 10-значное число.</span><span class="sxs-lookup"><span data-stu-id="d69ed-117">For example, a voice route might have a regular expression that enables it to handle any 10-digit number.</span></span> <span data-ttu-id="d69ed-118">Это означает, что маршрут сможет обработать номер телефона, например:</span><span class="sxs-lookup"><span data-stu-id="d69ed-118">That means the route would be able to handle a phone number such as this:</span></span>

  - <span data-ttu-id="d69ed-119">2065551219</span><span class="sxs-lookup"><span data-stu-id="d69ed-119">2065551219</span></span>

<span data-ttu-id="d69ed-120">Маршрут не может обрабатывать одно из следующих двух чисел, оба из которых содержат 10 цифр:</span><span class="sxs-lookup"><span data-stu-id="d69ed-120">The route would not be able to handle either of the following two numbers, neither of which has 10 digits:</span></span>

  - <span data-ttu-id="d69ed-121">5551219</span><span class="sxs-lookup"><span data-stu-id="d69ed-121">5551219</span></span>

  - <span data-ttu-id="d69ed-122">12065551219</span><span class="sxs-lookup"><span data-stu-id="d69ed-122">12065551219</span></span>

<span data-ttu-id="d69ed-123">Командлет Test-CsVoiceRoute проверяет, может ли указанный голосовой маршрут перенаправлять указанный номер телефона.</span><span class="sxs-lookup"><span data-stu-id="d69ed-123">The Test-CsVoiceRoute cmdlet verifies whether a given voice route can route a specified phone number.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="d69ed-124">Выполнение теста</span><span class="sxs-lookup"><span data-stu-id="d69ed-124">Running the test</span></span>

<span data-ttu-id="d69ed-125">Проверка возможности маршрута голоса к указанному номеру телефона состоит из двух этапов.</span><span class="sxs-lookup"><span data-stu-id="d69ed-125">Verifying the ability of a voice route to route a specified phone number is a two-step process.</span></span> <span data-ttu-id="d69ed-126">Прежде всего необходимо использовать командлет Get-CsVoiceRoute, чтобы возвращать экземпляр маршрута голосовой связи, а затем использовать командлет Test-CsVoiceRoute, чтобы проверить, может ли этот маршрут обрабатывать целевой номер телефона.</span><span class="sxs-lookup"><span data-stu-id="d69ed-126">First you have to use the Get-CsVoiceRoute cmdlet to return an instance of that voice route, and then you have to use the Test-CsVoiceRoute cmdlet to verify the ability of that route to handle the target phone number.</span></span> <span data-ttu-id="d69ed-127">Например, эта команда проверяет, может ли голосовой маршрут RedmondVoiceRoute перенаправлять номер телефона 2065551219:</span><span class="sxs-lookup"><span data-stu-id="d69ed-127">For example, this command verifies whether the RedmondVoiceRoute voice route can route the phone number 2065551219:</span></span>

`Get-CsVoiceRoute -Identity "RedmondVoiceRoute" | Test-CsVoiceRoute -TargetNumber "2065551219"`

<span data-ttu-id="d69ed-128">Обратите внимание на то, что номер телефона должен вводиться так, как ожидается, что пользователи будут набирать этот номер.</span><span class="sxs-lookup"><span data-stu-id="d69ed-128">Note that the phone number should be typed as you expect users to dial that number.</span></span> <span data-ttu-id="d69ed-129">Например, если вы не предполагаете, что пользователи должны включать код страны и города при наборе номера, используйте синтаксис, подобный приведенному ниже.</span><span class="sxs-lookup"><span data-stu-id="d69ed-129">For example, if you do not expect users to include the country code and area code when dialing, then use syntax similar to this:</span></span>

`-TargetNumber "5551219"`

<span data-ttu-id="d69ed-130">В этом случае целевой номер выходит из кода страны и кода города.</span><span class="sxs-lookup"><span data-stu-id="d69ed-130">In this case, the target number leaves out both the country code and the area code.</span></span>

<span data-ttu-id="d69ed-131">Чтобы использовать одну команду для проверки всех голосовых маршрутов по указанному целевому номеру, используйте следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="d69ed-131">To use a single command to test all the voice routes against a specified target number, use syntax such as the following:</span></span>

`Get-CsVoiceRoute | Test-CsVoiceRoute -TargetNumber "2065551219"`

<span data-ttu-id="d69ed-132">Дополнительные сведения можно найти в справочной документации по командлету Test-CsVoiceRoute.</span><span class="sxs-lookup"><span data-stu-id="d69ed-132">For more information, see the Help documentation for the Test-CsVoiceRoute cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="d69ed-133">Определение успеха или сбоя</span><span class="sxs-lookup"><span data-stu-id="d69ed-133">Determining success or failure</span></span>

<span data-ttu-id="d69ed-134">Если маршрут голосовой связи может перенаправлять целевой номер телефона, командлет Test-CsVoiceRoute просто возвращает значение true:</span><span class="sxs-lookup"><span data-stu-id="d69ed-134">If the voice route can route the target phone number the Test-CsVoiceRoute cmdlet just returns the value True:</span></span>

<span data-ttu-id="d69ed-135">MatchesPattern</span><span class="sxs-lookup"><span data-stu-id="d69ed-135">MatchesPattern</span></span>

\--------------

<span data-ttu-id="d69ed-136">Верно</span><span class="sxs-lookup"><span data-stu-id="d69ed-136">True</span></span>

<span data-ttu-id="d69ed-137">Это означает, что маршрут может обрабатывать номера, аналогичные целевому номеру.</span><span class="sxs-lookup"><span data-stu-id="d69ed-137">That means that route can handle numbers similar to the target number.</span></span> <span data-ttu-id="d69ed-138">Если голосовой маршрут не может обработать целевой номер, Test-CsVoiceRoute возвращает значение ложь.</span><span class="sxs-lookup"><span data-stu-id="d69ed-138">If the voice route is can't handle the target number then Test-CsVoiceRoute returns the value False:</span></span>

<span data-ttu-id="d69ed-139">MatchesPattern</span><span class="sxs-lookup"><span data-stu-id="d69ed-139">MatchesPattern</span></span>

\--------------

<span data-ttu-id="d69ed-140">False</span><span class="sxs-lookup"><span data-stu-id="d69ed-140">False</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="d69ed-141">Причины, по которым может произойти сбой теста</span><span class="sxs-lookup"><span data-stu-id="d69ed-141">Reasons why the test might have failed</span></span>

<span data-ttu-id="d69ed-142">При тестировании голосовых маршрутов "сбой" — это относительный термин.</span><span class="sxs-lookup"><span data-stu-id="d69ed-142">When testing voice routes, “failure” is a relative term.</span></span> <span data-ttu-id="d69ed-143">В этом случае это не означает, что маршрут является "разорванным"; вместо этого он просто означает, что маршрут не может обработать целевой номер.</span><span class="sxs-lookup"><span data-stu-id="d69ed-143">In this case, it doesn’t mean that the route is somehow “broken;” instead, it just means that the route can't handle the target number.</span></span> <span data-ttu-id="d69ed-144">Это может быть вызвано неправильным настройкам голосового маршрута.</span><span class="sxs-lookup"><span data-stu-id="d69ed-144">That could be because the voice route was configured incorrectly.</span></span> <span data-ttu-id="d69ed-145">Это также может означать, что маршрут не предназначался для обработки чисел с помощью этого шаблона.</span><span class="sxs-lookup"><span data-stu-id="d69ed-145">It could also mean that the route was never intended to handle numbers using this pattern.</span></span> <span data-ttu-id="d69ed-146">Например, если вы не хотите перенаправлять звонки в другие страны по определенному маршруту, этот маршрут можно настроить таким образом, чтобы он отклонил все номера телефонов, включающие код страны.</span><span class="sxs-lookup"><span data-stu-id="d69ed-146">For example, if you do not want to route calls to other countries over a given route that route might be configured to reject all phone numbers that include a country code.</span></span> <span data-ttu-id="d69ed-147">Если Test-CsVoiceRoute возвращает значение ложь, если предполагается, что оно возвращает значение истина, убедитесь, что конечный номер введен правильно.</span><span class="sxs-lookup"><span data-stu-id="d69ed-147">If Test-CsVoiceRoute returns False when you expected it to return True, verify that you typed the target number in correctly.</span></span> <span data-ttu-id="d69ed-148">Если вы сделали это, для просмотра NumberPattern, настроенного для маршрута, используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="d69ed-148">If you did, then use a command similar to this one to view the NumberPattern configured for the route:</span></span>

`Get-CsVoiceRoute -Identity "RedmondVoiceRoute" | Select-Object NumberPattern`

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="d69ed-149">См. также</span><span class="sxs-lookup"><span data-stu-id="d69ed-149">See Also</span></span>


[<span data-ttu-id="d69ed-150">Test-CsVoiceRoute</span><span class="sxs-lookup"><span data-stu-id="d69ed-150">Test-CsVoiceRoute</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsVoiceRoute)  
  

<span data-ttu-id="d69ed-151"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d69ed-151"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

