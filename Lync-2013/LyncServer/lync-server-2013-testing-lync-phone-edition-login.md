---
title: 'Lync Server 2013: Проверка входных параметров Lync Phone Edition'
description: 'Lync Server 2013: Проверка входных данные Lync Phone Edition.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing Lync Phone Edition login
ms:assetid: 1ccde6bf-9a2d-4fcf-b81f-1bc9fee2cfbb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn690128(v=OCS.15)
ms:contentKeyID: 63969583
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d21d65676c4f5e0f867c7d9556cdea50419be69b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398938"
---
# <a name="testing-lync-phone-edition-login-in-lync-server-2013"></a><span data-ttu-id="38d4e-103">Проверка входа в Lync Phone Edition в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="38d4e-103">Testing Lync Phone Edition login in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="38d4e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="38d4e-104">

<span> </span></span></span>

<span data-ttu-id="38d4e-105">_**Тема последнего изменения:** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="38d4e-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="38d4e-106">Расписание проверки</span><span class="sxs-lookup"><span data-stu-id="38d4e-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="38d4e-107">Ежедневно</span><span class="sxs-lookup"><span data-stu-id="38d4e-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38d4e-108">Средство тестирования</span><span class="sxs-lookup"><span data-stu-id="38d4e-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="38d4e-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="38d4e-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38d4e-110">Требуемые разрешения</span><span class="sxs-lookup"><span data-stu-id="38d4e-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="38d4e-111">При локальном запуске с помощью командной консоли Lync Server пользователи должны быть членами группы безопасности RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="38d4e-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="38d4e-112">При запуске с помощью удаленного экземпляра Windows PowerShell пользователям должна быть назначена роль RBAC, имеющая разрешение на запуск командлета Test-CsPhoneBootstrap.</span><span class="sxs-lookup"><span data-stu-id="38d4e-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsPhoneBootstrap cmdlet.</span></span> <span data-ttu-id="38d4e-113">Чтобы просмотреть список всех ролей RBAC, которые могут использовать этот командлет, выполните в командной строке Windows PowerShell следующую команду:</span><span class="sxs-lookup"><span data-stu-id="38d4e-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsPhoneBootstrap&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="38d4e-114">Описание</span><span class="sxs-lookup"><span data-stu-id="38d4e-114">Description</span></span>

<span data-ttu-id="38d4e-115">Командлет Test-CsPhoneBootstrap позволяет администраторам войти в систему с помощью устройства Lync 2013 Phone Edition, которое будет использоваться для подтверждения того, что пользователь использует номер телефона и ПИН-код, назначенный ему.</span><span class="sxs-lookup"><span data-stu-id="38d4e-115">The Test-CsPhoneBootstrap cmdlet enables administrators to verify that a given user—using the phone number and PIN assigned to him or her—can log on to the system from a Lync 2013 Phone Edition-compatible device.</span></span> <span data-ttu-id="38d4e-116">(Для выполнения теста на самом деле не требуется никаких устройств.)</span><span class="sxs-lookup"><span data-stu-id="38d4e-116">(No device is actually needed to run the test.)</span></span>

<span data-ttu-id="38d4e-117">Чтобы Test-CsPhoneBootstrap выполнить проверку, пул регистратора, на котором размещается тестируемая учетная запись пользователя, должен быть обнаруживаемым с помощью DHCP.</span><span class="sxs-lookup"><span data-stu-id="38d4e-117">In order for Test-CsPhoneBootstrap to make its check, the Registrar pool that hosts the user account being tested must be discoverable using DHCP.</span></span> <span data-ttu-id="38d4e-118">Чтобы определить, может ли регистратор быть обнаруживаемым таким образом, используйте командлет Get-CsRegistrarConfiguration и проверьте значение свойства EnableDHCPServer.</span><span class="sxs-lookup"><span data-stu-id="38d4e-118">To determine whether a Registrar is discoverable in this manner, use the cmdlet Get-CsRegistrarConfiguration and check the value of the EnableDHCPServer property.</span></span> <span data-ttu-id="38d4e-119">Если для этого свойства задано значение false, необходимо использовать Set-CsRegistrarConfiguration для задания значения свойства true и сделать его обнаруживаемым с помощью DHCP.</span><span class="sxs-lookup"><span data-stu-id="38d4e-119">If this property is set to False, you must use Set-CsRegistrarConfiguration to set the property value to True and make the Registrar discoverable using DHCP.</span></span> <span data-ttu-id="38d4e-120">Это также можно сделать с помощью DHCP-сервера Enterprise и настройки параметров, относящихся к Lync Server.</span><span class="sxs-lookup"><span data-stu-id="38d4e-120">This can also be done by using Enterprise DHCP Server and configuring the Lync Server-specific options.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="38d4e-121">Выполнение теста</span><span class="sxs-lookup"><span data-stu-id="38d4e-121">Running the test</span></span>

<span data-ttu-id="38d4e-122">Чтобы запустить командлет Test-CsPhoneBootstrap, необходимо, как минимум, указать номер телефона и персональный идентификационный номер клиента (ПИН-код) для допустимого пользователя Lync Server.</span><span class="sxs-lookup"><span data-stu-id="38d4e-122">To run the Test-CsPhoneBootstrap cmdlet, you must, at a minimum, supply the phone number and client personal identification number (PIN) for a valid Lync Server user.</span></span> <span data-ttu-id="38d4e-123">Например, эта команда проверяет возможности входа для пользователя с номером телефона 12065551219 и ПИН-кодом 0712:</span><span class="sxs-lookup"><span data-stu-id="38d4e-123">For example, this command tests the logon ability for the user who has the phone number 12065551219 and the PIN 0712:</span></span>

    Test-CsPhoneBootstrap -PhoneOrExt "+12065551219" -Pin "0712"

<span data-ttu-id="38d4e-124">Для более полной проверки можно также указать адрес SIP пользователя.</span><span class="sxs-lookup"><span data-stu-id="38d4e-124">For a more comprehensive check, you can also include the user’s SIP address.</span></span> <span data-ttu-id="38d4e-125">В этом случае номер телефона, ПИН-код клиента и адрес SIP должны быть действительны для успешной проверки.</span><span class="sxs-lookup"><span data-stu-id="38d4e-125">In that case, the phone number, client PIN, and SIP address must all be valid for the test to succeed:</span></span>

    Test-CsPhoneBootstrap -PhoneOrExt "+12065551219" -Pin "0712" -UserSipAddress "sip:kenmyer@litwareinc.com"

<span data-ttu-id="38d4e-126">Дополнительные сведения можно найти в справочной документации по командлету [Test-CsPhoneBootstrap](https://docs.microsoft.com/powershell/module/skype/Test-CsPhoneBootstrap) .</span><span class="sxs-lookup"><span data-stu-id="38d4e-126">For more information, see the Help documentation for the [Test-CsPhoneBootstrap](https://docs.microsoft.com/powershell/module/skype/Test-CsPhoneBootstrap) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="38d4e-127">Определение успеха или сбоя</span><span class="sxs-lookup"><span data-stu-id="38d4e-127">Determining success or failure</span></span>

<span data-ttu-id="38d4e-128">Если указанный пользователь смог подключиться к серверу Lync Server, вы получите вывод, как показано ниже, и свойство Result, помеченное как **успешно.**</span><span class="sxs-lookup"><span data-stu-id="38d4e-128">If the specified user was able to connect to Lync Server, you'll receive output similar to this, with the Result property marked as **Success:**</span></span>

<span data-ttu-id="38d4e-129">TargetUri : https://atl-cs-001.litwareinc.com:443/CertProv/</span><span class="sxs-lookup"><span data-stu-id="38d4e-129">TargetUri : https://atl-cs-001.litwareinc.com:443/CertProv/</span></span>

<span data-ttu-id="38d4e-130">CertProvisioningService. svc</span><span class="sxs-lookup"><span data-stu-id="38d4e-130">CertProvisioningService.svc</span></span>

<span data-ttu-id="38d4e-131">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="38d4e-131">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="38d4e-132">Результат: успех</span><span class="sxs-lookup"><span data-stu-id="38d4e-132">Result : Success</span></span>

<span data-ttu-id="38d4e-133">Задержка: 00:00:06.3981276</span><span class="sxs-lookup"><span data-stu-id="38d4e-133">Latency : 00:00:06.3981276</span></span>

<span data-ttu-id="38d4e-134">Ошибки</span><span class="sxs-lookup"><span data-stu-id="38d4e-134">Error :</span></span>

<span data-ttu-id="38d4e-135">Диагностик</span><span class="sxs-lookup"><span data-stu-id="38d4e-135">Diagnosis :</span></span>

<span data-ttu-id="38d4e-136">Если указанный пользователь не смог установить соединение, результат будет показан как сбой, а дополнительные сведения будут записаны в свойствах Error и диагноз.</span><span class="sxs-lookup"><span data-stu-id="38d4e-136">If the specified user was not able to make a connection, then the Result will be shown as Failure, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="38d4e-137">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="38d4e-137">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="38d4e-138">Результат: сбой</span><span class="sxs-lookup"><span data-stu-id="38d4e-138">Result : Failure</span></span>

<span data-ttu-id="38d4e-139">Задержка: 00:00:04.1993845</span><span class="sxs-lookup"><span data-stu-id="38d4e-139">Latency : 00:00:04.1993845</span></span>

<span data-ttu-id="38d4e-140">Ошибка: ошибка — ответ на службу Web-Ticket не получен.</span><span class="sxs-lookup"><span data-stu-id="38d4e-140">Error : ERROR - No response received for Web-Ticket service.</span></span>

<span data-ttu-id="38d4e-141">Диагностик</span><span class="sxs-lookup"><span data-stu-id="38d4e-141">Diagnosis :</span></span>

<span data-ttu-id="38d4e-142">В предыдущем выводе говорится, что тест завершился сбоем, так как служба веб-билета не ответила.</span><span class="sxs-lookup"><span data-stu-id="38d4e-142">The previous output states that the test failed because the Web Ticket service did not respond.</span></span> <span data-ttu-id="38d4e-143">Это может быть вызвано проблемой с самой службой или из-за того, что адрес SIP, номер телефона или клиентский PIN-код передан в тест — CsPhoneBootstrap.</span><span class="sxs-lookup"><span data-stu-id="38d4e-143">This could be due to a problem with the service itself, or it might be due to the SIP address, phone number, or client PIN passed to Test-CsPhoneBootstrap.</span></span> <span data-ttu-id="38d4e-144">Вы можете проверить SIP-адрес и номер телефона пользователя, выполнив следующую команду:</span><span class="sxs-lookup"><span data-stu-id="38d4e-144">You can verify the user’s SIP address and phone number by using a command similar to this one:</span></span>

    Get-CsUser -Identity "sip:kenmyer@litwareinc.com" | Select-Object SipAddress, LineUri

<span data-ttu-id="38d4e-145">Вы также можете убедиться, что у пользователя есть допустимый ПИН-код, выполнив команду, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="38d4e-145">And you can verify that the user has a valid PIN by using a command as follows:</span></span>

    Get-CsClientPinInfo -Identity "sip:kenmyer@litwareinc.com" 

<span data-ttu-id="38d4e-146">Если Test-CsPhoneBootstrap не удается, возможно, потребуется повторно выполнить тест, на этот раз включая параметр подробно:</span><span class="sxs-lookup"><span data-stu-id="38d4e-146">If Test-CsPhoneBootstrap fails, then you might want to rerun the test, this time including the Verbose parameter:</span></span>

    Test-CsPhoneBootstrap -PhoneOrExt "+12065551219" -Pin "0712" -Verbose

<span data-ttu-id="38d4e-147">После включения подробной информации Test-CsPhoneBootstrap будет возвращать пошаговые учетные записи каждого действия, которое он пытался войти на сервер Lync Server.</span><span class="sxs-lookup"><span data-stu-id="38d4e-147">When the Verbose parameter is included, Test-CsPhoneBootstrap will return a step-by-step account of each action it tried when it checked the ability of the specified user to log on to Lync Server.</span></span> <span data-ttu-id="38d4e-148">Например, ниже приведена часть выходных данных для неудачного входа в сеанс, в котором был указан неверный ПИН-код:</span><span class="sxs-lookup"><span data-stu-id="38d4e-148">For example, here is a portion of the output for an unsuccessful logon, a session in which an incorrect PIN was included:</span></span>

<span data-ttu-id="38d4e-149">Использование проверки подлинности PIN-кода с телефонным телефоном \\ : 12065551219 PIN: 0712</span><span class="sxs-lookup"><span data-stu-id="38d4e-149">Using PIN auth with Phone\\Ext : 12065551219 Pin : 0712</span></span>

<span data-ttu-id="38d4e-150">Не удалось получить веб-билет</span><span class="sxs-lookup"><span data-stu-id="38d4e-150">Could not get web ticket</span></span>

<span data-ttu-id="38d4e-151">ОПРЕДЕЛИТЬ</span><span class="sxs-lookup"><span data-stu-id="38d4e-151">CHECK :</span></span>

<span data-ttu-id="38d4e-152">\- URL веб-службы является действительным, и веб-службы работают</span><span class="sxs-lookup"><span data-stu-id="38d4e-152">\- Web service url is valid and the web services are functional</span></span>

<span data-ttu-id="38d4e-153">\- Если \\ для проверки подлинности используется закрепление PhoneNo, убедитесь, что они соответствуют универсальному коду ресурса пользователя</span><span class="sxs-lookup"><span data-stu-id="38d4e-153">\- If using PhoneNo\\PIN to authenticate, make sure they match the user uri</span></span>

<span data-ttu-id="38d4e-154">\- При использовании \\ проверки подлинности NTLM Kerberos убедитесь, что вы указали действительные учетные данные.</span><span class="sxs-lookup"><span data-stu-id="38d4e-154">\- If using NTLM\\Kerberos auth, make sure you provided valid credentials</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="38d4e-155">Причины, по которым может произойти сбой теста</span><span class="sxs-lookup"><span data-stu-id="38d4e-155">Reasons why the test might have failed</span></span>

<span data-ttu-id="38d4e-156">Ниже приведены некоторые распространенные причины, по которым может произойти сбой Test-CsPhoneBootstrap.</span><span class="sxs-lookup"><span data-stu-id="38d4e-156">Here are some common reasons why Test-CsPhoneBootstrap might fail:</span></span>

  - <span data-ttu-id="38d4e-157">Возможно, указан недопустимый адрес SIP.</span><span class="sxs-lookup"><span data-stu-id="38d4e-157">You might have specified a SIP address that is not valid.</span></span> <span data-ttu-id="38d4e-158">Вы можете проверить, правильно ли указан адрес SIP, используя одну из следующих команд:</span><span class="sxs-lookup"><span data-stu-id="38d4e-158">You can verify that a SIP address is correct by using a command such as this one:</span></span>
    
        Get-CsUser -Identity "sip:kenmyer@litwareinc.com"

  - <span data-ttu-id="38d4e-159">Возможно, указан недопустимый ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="38d4e-159">You might have specified a PIN that is not valid.</span></span> <span data-ttu-id="38d4e-160">Несмотря на то, что вы не можете получить PIN-код пользователя, вы можете убедиться, что у пользователя по крайней мере есть PIN-код, используя следующую команду:</span><span class="sxs-lookup"><span data-stu-id="38d4e-160">Although you can't retrieve the user’s PIN number, you can verify that the user at least has a PIN number by using a command similar to this:</span></span>
    
        Get-CsClientPinInfo -Identity "sip:kenmyer@litwareinc.com"

  - <span data-ttu-id="38d4e-161">Возможно, указан недопустимый номер телефона.</span><span class="sxs-lookup"><span data-stu-id="38d4e-161">You might have specified a phone number that is not valid.</span></span> <span data-ttu-id="38d4e-162">Вы можете проверить телефон пользователя, выполнив команду, подобную следующей:</span><span class="sxs-lookup"><span data-stu-id="38d4e-162">You can verify a user’s phone by using a command similar to the following:</span></span>
    
        Get-CsUser -Identity "sip:kenmyer@litwareinc.com" | Select-Object LineUri

  - <span data-ttu-id="38d4e-163">Для пула регистраторов не включена служба DHCP.</span><span class="sxs-lookup"><span data-stu-id="38d4e-163">The Registrar pool is not DHCP-enabled.</span></span> <span data-ttu-id="38d4e-164">Чтобы определить, активирован ли пул регистратора для DHCP, выполните командлет Get-CsRegistrarConfiguration и проверьте значение свойства EnableDHCPServer.</span><span class="sxs-lookup"><span data-stu-id="38d4e-164">To determine whether your Registrar pool is enabled for DHCP, run the Get-CsRegistrarConfiguration cmdlet and check the value of the EnableDHCPServer property.</span></span> <span data-ttu-id="38d4e-165">Например:</span><span class="sxs-lookup"><span data-stu-id="38d4e-165">For example:</span></span>
    
        Get-CsRegistrarConfiguration -Identity "global"

<span data-ttu-id="38d4e-166"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="38d4e-166"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

