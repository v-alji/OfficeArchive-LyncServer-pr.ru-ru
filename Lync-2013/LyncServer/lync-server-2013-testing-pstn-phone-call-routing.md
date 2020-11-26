---
title: 'Lync Server 2013: Проверка маршрутизации звонков по телефонной сети PSTN'
description: 'Lync Server 2013: Проверка маршрутизации звонков по телефонной сети PSTN.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing PSTN phone call routing
ms:assetid: 301dd44d-03e9-41cd-9722-54e00365aa45
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn727302(v=OCS.15)
ms:contentKeyID: 63969598
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: da931b43176932a9b6781fa27318e83e6994548c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440992"
---
# <a name="testing-pstn-phone-call-routing-in-lync-server-2013"></a><span data-ttu-id="90c21-103">Проверка маршрутизации телефонных звонков PSTN в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="90c21-103">Testing PSTN phone call routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="90c21-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="90c21-104">

<span> </span></span></span>

<span data-ttu-id="90c21-105">_**Тема последнего изменения:** 2014-11-01_</span><span class="sxs-lookup"><span data-stu-id="90c21-105">_**Topic Last Modified:** 2014-11-01_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="90c21-106">Расписание проверки</span><span class="sxs-lookup"><span data-stu-id="90c21-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="90c21-107">Ежедневно</span><span class="sxs-lookup"><span data-stu-id="90c21-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90c21-108">Средство тестирования</span><span class="sxs-lookup"><span data-stu-id="90c21-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="90c21-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="90c21-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90c21-110">Требуемые разрешения</span><span class="sxs-lookup"><span data-stu-id="90c21-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="90c21-111">При локальном запуске с помощью командной консоли Lync Server пользователи должны быть членами группы безопасности RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="90c21-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="90c21-112">При запуске с помощью удаленного экземпляра Windows PowerShell пользователям должна быть назначена роль RBAC, имеющая разрешение на запуск командлета <strong>Test-CsInterTrunkRouting</strong> .</span><span class="sxs-lookup"><span data-stu-id="90c21-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the <strong>Test-CsInterTrunkRouting</strong> cmdlet.</span></span> <span data-ttu-id="90c21-113">Чтобы просмотреть список всех ролей RBAC, которые могут использовать этот командлет, выполните в командной строке Windows PowerShell следующую команду:</span><span class="sxs-lookup"><span data-stu-id="90c21-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsInterTrunkRouting&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="90c21-114">Описание</span><span class="sxs-lookup"><span data-stu-id="90c21-114">Description</span></span>

<span data-ttu-id="90c21-115">Командлет **Test-CsInterTrunkRouting** подтверждает, что звонки могут маршрутизироваться от одного SIP к другому.</span><span class="sxs-lookup"><span data-stu-id="90c21-115">The **Test-CsInterTrunkRouting** cmdlet verifies that calls can be routed from one SIP to another.</span></span> <span data-ttu-id="90c21-116">Для этого командлету задается номер телефона и конфигурация магистрали.</span><span class="sxs-lookup"><span data-stu-id="90c21-116">To do this, the cmdlet is given a phone number and a trunk configuration.</span></span> <span data-ttu-id="90c21-117">**Тест-CsInterTrunkRouting** будет указывать маршруты обратного сопоставления и использование PSTN для указанного номера.</span><span class="sxs-lookup"><span data-stu-id="90c21-117">**Test-CsInterTrunkRouting** will then report back matching routes and matching PSTN usages for the specified number.</span></span> <span data-ttu-id="90c21-118">Обратите внимание на то, что звонки между магистральами могут маршрутизироваться только в том случае, если в магистральных каналов есть шаблон номера, который соответствует указанному номеру телефона и только в том случае, если в магистральных каналов есть хотя бы одна PSTN.</span><span class="sxs-lookup"><span data-stu-id="90c21-118">Note that calls can be routed between trunks only if the trunks have a number pattern that matches the specified phone number and only if the trunks share at least one PSTN usage.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="90c21-119">Выполнение теста</span><span class="sxs-lookup"><span data-stu-id="90c21-119">Running the test</span></span>

<span data-ttu-id="90c21-120">Команды, показанные ниже, возвращают подходящие маршруты и соответствующие использование телефона, позволяющие пользователям звонить по номеру 1-206-555-1219 с помощью параметров конфигурации канала для сайта Redmond.</span><span class="sxs-lookup"><span data-stu-id="90c21-120">The commands shown below return the matching routes and matching phone usages that enable users to call the phone number 1-206-555-1219 using the trunk configuration settings for the Redmond site.</span></span>

    $trunk = Get-CsTrunkConfiguration -Identity "site:Redmond"
    
    Test-CsInterTrunkRouting -TargetNumber "tel:+12065551219" -TrunkConfiguration $trunk

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="90c21-121">Определение успеха или сбоя</span><span class="sxs-lookup"><span data-stu-id="90c21-121">Determining success or failure</span></span>

<span data-ttu-id="90c21-122">Если звонки могут маршрутизироваться от одного SIP к другому, вы получите вывод, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="90c21-122">If calls can be routed from one SIP to another, you'll receive output similar to this:</span></span>

<span data-ttu-id="90c21-123">FirstMatchingRoute MatchingUsage MatchingRoutes</span><span class="sxs-lookup"><span data-stu-id="90c21-123">FirstMatchingRoute MatchingUsage MatchingRoutes</span></span>

<span data-ttu-id="90c21-124">\------------------ ------------- --------------</span><span class="sxs-lookup"><span data-stu-id="90c21-124">\------------------ ------------- --------------</span></span>

<span data-ttu-id="90c21-125">RedmondRoute LocalUsage {RedmondRoute}</span><span class="sxs-lookup"><span data-stu-id="90c21-125">RedmondRoute LocalUsage {RedmondRoute}</span></span>

<span data-ttu-id="90c21-126">Если проверка завершилась сбоем, вы получите вывод примерно так:</span><span class="sxs-lookup"><span data-stu-id="90c21-126">If the test did not succeed, you'll receive output similar to this:</span></span>

<span data-ttu-id="90c21-127">Test-CsInterTrunkRouting: не удается обработать Преобразование аргументов для параметра</span><span class="sxs-lookup"><span data-stu-id="90c21-127">Test-CsInterTrunkRouting : Cannot process argument transformation on parameter</span></span>

<span data-ttu-id="90c21-128">'TrunkConfiguration'.</span><span class="sxs-lookup"><span data-stu-id="90c21-128">'TrunkConfiguration'.</span></span> <span data-ttu-id="90c21-129">Недопустимый TrunkConfigurationsetting (параметр).</span><span class="sxs-lookup"><span data-stu-id="90c21-129">Invalid TrunkConfigurationsetting (parameter).</span></span> <span data-ttu-id="90c21-130">Укажите</span><span class="sxs-lookup"><span data-stu-id="90c21-130">Specify a</span></span>

<span data-ttu-id="90c21-131">допустимый параметр (параметр) и повторите попытку.</span><span class="sxs-lookup"><span data-stu-id="90c21-131">valid setting (parameter) and then try again.</span></span>

<span data-ttu-id="90c21-132">В строке: 1 символ: 79</span><span class="sxs-lookup"><span data-stu-id="90c21-132">At line:1 char:79</span></span>

<span data-ttu-id="90c21-133">\+ Test-CsInterTrunkRouting TargetNumber "Tel: + 12065551219"</span><span class="sxs-lookup"><span data-stu-id="90c21-133">\+ Test-CsInterTrunkRouting -TargetNumber "tel:+12065551219"</span></span>

<span data-ttu-id="90c21-134">\-TrunkConfiguration $t...</span><span class="sxs-lookup"><span data-stu-id="90c21-134">\-TrunkConfiguration $t ...</span></span>

\+

~~

<span data-ttu-id="90c21-135">\+ CategoryInfo: InvalidData: (:) \[ Test-CsInterTrunkRouting \] , номинал</span><span class="sxs-lookup"><span data-stu-id="90c21-135">\+ CategoryInfo : InvalidData: (:) \[Test-CsInterTrunkRouting\], Par</span></span>

<span data-ttu-id="90c21-136">ameterBindingArgumentTransformationException</span><span class="sxs-lookup"><span data-stu-id="90c21-136">ameterBindingArgumentTransformationException</span></span>

<span data-ttu-id="90c21-137">\+ FullyQualifiedErrorId: ParameterArgumentTransformationError, Microsoft. R</span><span class="sxs-lookup"><span data-stu-id="90c21-137">\+ FullyQualifiedErrorId : ParameterArgumentTransformationError,Microsoft.R</span></span>

<span data-ttu-id="90c21-138">традиционно. Management. Voice. командлеты. TestOcsInterTrunkRoutingCmdlet</span><span class="sxs-lookup"><span data-stu-id="90c21-138">tc.Management.Voice.Cmdlets.TestOcsInterTrunkRoutingCmdlet</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="90c21-139">Причины, по которым может произойти сбой теста</span><span class="sxs-lookup"><span data-stu-id="90c21-139">Reasons why the test might have failed</span></span>

<span data-ttu-id="90c21-140">Ниже приведены некоторые распространенные причины, по которым может произойти сбой **Test-CsInterTrunkRouting** :</span><span class="sxs-lookup"><span data-stu-id="90c21-140">Here are some common reasons why **Test-CsInterTrunkRouting** might fail:</span></span>

  - <span data-ttu-id="90c21-141">Указаны недопустимые параметры.</span><span class="sxs-lookup"><span data-stu-id="90c21-141">You specified invalid parameters.</span></span> <span data-ttu-id="90c21-142">Возможно, вы еще не настроили магистраль, а указанный конечный номер может быть неверным или недействительным.</span><span class="sxs-lookup"><span data-stu-id="90c21-142">The trunk might not yet be correctly configured and the specified target number might be incorrect or invalid.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="90c21-143">См. также</span><span class="sxs-lookup"><span data-stu-id="90c21-143">See Also</span></span>


[<span data-ttu-id="90c21-144">Get-CsTrunk</span><span class="sxs-lookup"><span data-stu-id="90c21-144">Get-CsTrunk</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsTrunk)  
[<span data-ttu-id="90c21-145">Get-CsTrunkConfiguration</span><span class="sxs-lookup"><span data-stu-id="90c21-145">Get-CsTrunkConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsTrunkConfiguration)  
  

<span data-ttu-id="90c21-146"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="90c21-146"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

