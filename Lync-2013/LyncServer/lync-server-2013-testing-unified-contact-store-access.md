---
title: 'Lync Server 2013: тестирование доступа к единому хранилищу контактов'
description: 'Lync Server 2013: тестирование доступа к единому хранилищу контактов.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing Unified Contact Store access
ms:assetid: 761f46bd-2e14-4f40-82b9-afa1eaa816b0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn727309(v=OCS.15)
ms:contentKeyID: 63969621
ms.date: 05/16/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 58238685133c51130c414e0d7a8cd761d0233f5d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440943"
---
# <a name="testing-unified-contact-store-access-in-lync-server-2013"></a><span data-ttu-id="80ee6-103">Тестирование доступа к единому хранилищу контактов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="80ee6-103">Testing Unified Contact Store access in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="80ee6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="80ee6-104">

<span> </span></span></span>

<span data-ttu-id="80ee6-105">_**Тема последнего изменения:** 2015-05-15_</span><span class="sxs-lookup"><span data-stu-id="80ee6-105">_**Topic Last Modified:** 2015-05-15_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="80ee6-106">Расписание проверки</span><span class="sxs-lookup"><span data-stu-id="80ee6-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="80ee6-107">Ежедневно</span><span class="sxs-lookup"><span data-stu-id="80ee6-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80ee6-108">Средство тестирования</span><span class="sxs-lookup"><span data-stu-id="80ee6-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="80ee6-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="80ee6-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80ee6-110">Требуемые разрешения</span><span class="sxs-lookup"><span data-stu-id="80ee6-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="80ee6-111">При локальном запуске с помощью командной консоли Lync Server пользователи должны быть членами группы безопасности RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="80ee6-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="80ee6-112">При запуске с помощью удаленного экземпляра Windows PowerShell пользователям должна быть назначена роль RBAC, имеющая разрешение на запуск командлета <strong>Test-CsUnifiedContactStore</strong> .</span><span class="sxs-lookup"><span data-stu-id="80ee6-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the <strong>Test-CsUnifiedContactStore</strong> cmdlet.</span></span> <span data-ttu-id="80ee6-113">Чтобы просмотреть список всех ролей RBAC, которые могут использовать этот командлет, выполните в командной строке Windows PowerShell следующую команду:</span><span class="sxs-lookup"><span data-stu-id="80ee6-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsUnifiedContactStore&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="80ee6-114">Описание</span><span class="sxs-lookup"><span data-stu-id="80ee6-114">Description</span></span>

<span data-ttu-id="80ee6-115">Единое хранилище контактов, представленное в Lync Server 2013, дает администраторам возможность хранить контакты пользователя в Microsoft Exchange Server 2013, а не в Lync Server.</span><span class="sxs-lookup"><span data-stu-id="80ee6-115">The unified contact store introduced in Lync Server 2013 gives administrators the option of storing a user's contacts in Microsoft Exchange Server 2013 instead of in Lync Server.</span></span> <span data-ttu-id="80ee6-116">Это позволит пользователю получить доступ к тому же набору контактов в Outlook Web Access в дополнение к Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="80ee6-116">This allows the user to access the same set of contacts in Outlook Web Access in addition to Lync 2013.</span></span> <span data-ttu-id="80ee6-117">(Или вы можете продолжать хранить контакты в Lync Server.</span><span class="sxs-lookup"><span data-stu-id="80ee6-117">(Or, you can continue to store contacts in Lync Server.</span></span> <span data-ttu-id="80ee6-118">В этом случае пользователям придется поддерживать два отдельных набора контактов: один для использования с Outlook и Outlook Web Access, а второй — для использования в Lync 2013.)</span><span class="sxs-lookup"><span data-stu-id="80ee6-118">In that case, users will have to maintain two separate sets of contacts: one for use with Outlook and Outlook Web Access, and one for use with Lync 2013.)</span></span>

<span data-ttu-id="80ee6-119">Вы можете определить, перенесены ли контакты пользователя в единое хранилище контактов, запустив командлет **Test-CsUnifiedContactStore** .</span><span class="sxs-lookup"><span data-stu-id="80ee6-119">You can determine whether or not a user's contacts were moved to the unified contact store by running the **Test-CsUnifiedContactStore** cmdlet.</span></span> <span data-ttu-id="80ee6-120">Командлет **Test-CsUnifiedContactStore** займет указанную учетную запись пользователя, подключаться к единому хранилищу контактов и пытаться получить контакт для пользователя.</span><span class="sxs-lookup"><span data-stu-id="80ee6-120">The **Test-CsUnifiedContactStore** cmdlet will take the specified user account, connect to the unified contact store, and attempt to retrieve a contact for the user.</span></span> <span data-ttu-id="80ee6-121">Если ни одного контакта не удается получить, команда завершится сбоем вместе с сообщением "не получено ни одного контакта для пользователя".</span><span class="sxs-lookup"><span data-stu-id="80ee6-121">If no contacts can be retrieved then the command will fail together with the message "No contacts were received for the user.</span></span> <span data-ttu-id="80ee6-122">Убедитесь, что у пользователя есть контакты. "</span><span class="sxs-lookup"><span data-stu-id="80ee6-122">Verify that contacts exist for the user."</span></span>

<span data-ttu-id="80ee6-123">Обратите внимание, что командлет **Test-CsUnifiedContactStore** завершает работу со сбоем, если пользователь успешно прошел миграцию в едином банке контактов, но у него нет контактов в своем списке контактов.</span><span class="sxs-lookup"><span data-stu-id="80ee6-123">Note that the **Test-CsUnifiedContactStore** cmdlet will fail if the user has successfully migrated to the unified contact store but has no contacts on his or her Contacts list.</span></span> <span data-ttu-id="80ee6-124">Для успешного завершения командлета **Test-CsUnifiedContactStore** указанному пользователю должен быть хотя бы один контакт.</span><span class="sxs-lookup"><span data-stu-id="80ee6-124">The specified user must have at least one contact for the **Test-CsUnifiedContactStore** cmdlet to complete successfully.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="80ee6-125">Выполнение теста</span><span class="sxs-lookup"><span data-stu-id="80ee6-125">Running the test</span></span>

<span data-ttu-id="80ee6-126">Команды, показанные в приведенном ниже примере, определяют, могут ли контакты пользователя плана litwareinc \\ kenmyer быть обнаружены в едином банке контактов.</span><span class="sxs-lookup"><span data-stu-id="80ee6-126">The commands shown in the following example determine whether contacts for the user litwareinc\\kenmyer can be found in the unified contact store.</span></span> <span data-ttu-id="80ee6-127">Для этого в первой команде примера используется командлет **Get-Credential** для создания объекта учетных данных интерфейса командной строки Windows PowerShell для пользователя плана litwareinc \\ kenmyer.</span><span class="sxs-lookup"><span data-stu-id="80ee6-127">To do this, the first command in the example uses the **Get-Credential** cmdlet to create a Windows PowerShell command-line interface credentials object for the user litwareinc\\kenmyer.</span></span> <span data-ttu-id="80ee6-128">Обратите внимание, что для этой учетной записи необходимо указать пароль, чтобы создать допустимый объект учетных данных и убедиться, что командлет **Test-CsUnifiedContactStore** может выполнить его проверку.</span><span class="sxs-lookup"><span data-stu-id="80ee6-128">Note that you must supply the password for this account to create a valid credentials object and to make sure that the **Test-CsUnifiedContactStore** cmdlet can run its check.</span></span>

<span data-ttu-id="80ee6-129">Во второй команде в примере используется предоставленный объект учетных данных ($x) и адрес SIP пользователя плана litwareinc kenmyer, \\ чтобы определить, можно ли найти контакты в едином банке контактов.</span><span class="sxs-lookup"><span data-stu-id="80ee6-129">The second command in the example uses the supplied credentials object ($x) and the SIP address of the user litwareinc\\kenmyer to determine whether his contacts can be found in the unified contact store.</span></span>

    $credential = Get-Credential "litwareinc\kenmyer"
    
    Test-CsUnifiedContactStore -TargetFqdn "atl-cs-001.litwareinc.com" -UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="80ee6-130">Определение успеха или сбоя</span><span class="sxs-lookup"><span data-stu-id="80ee6-130">Determining success or failure</span></span>

<span data-ttu-id="80ee6-131">Если доступ к хранилищу контактов настроен правильно, вы получите вывод примерно так, чтобы свойство Result пометило **"успешно".**</span><span class="sxs-lookup"><span data-stu-id="80ee6-131">If access to the contact store is configured correctly, you'll receive output similar to this, with the Result property marked as **Success:**</span></span>

<span data-ttu-id="80ee6-132">Целевое полное доменное имя: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="80ee6-132">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="80ee6-133">Результат: успех</span><span class="sxs-lookup"><span data-stu-id="80ee6-133">Result : Success</span></span>

<span data-ttu-id="80ee6-134">Задержка: 00:00:14.9862716</span><span class="sxs-lookup"><span data-stu-id="80ee6-134">Latency : 00:00:14.9862716</span></span>

<span data-ttu-id="80ee6-135">Сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="80ee6-135">Error Message :</span></span>

<span data-ttu-id="80ee6-136">Диагностик</span><span class="sxs-lookup"><span data-stu-id="80ee6-136">Diagnosis :</span></span>

<span data-ttu-id="80ee6-137">Если доступ к хранилищу контактов настроен неправильно, результат будет показан в виде **ошибки**, а дополнительные сведения будут записаны в свойствах Error и диагноз.</span><span class="sxs-lookup"><span data-stu-id="80ee6-137">If access to the contact store is not configured correctly, the Result will be shown as **Failure**, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="80ee6-138">Предупреждение: не удалось прочитать номер порта регистратора для заданного полного имени</span><span class="sxs-lookup"><span data-stu-id="80ee6-138">WARNING: Failed to read Registrar port number for the given fully qualified</span></span>

<span data-ttu-id="80ee6-139">доменное имя (FQDN).</span><span class="sxs-lookup"><span data-stu-id="80ee6-139">domain name (FQDN).</span></span> <span data-ttu-id="80ee6-140">С помощью номера порта регистратора по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="80ee6-140">Using default Registrar port number.</span></span> <span data-ttu-id="80ee6-141">Ошибка</span><span class="sxs-lookup"><span data-stu-id="80ee6-141">Exception:</span></span>

<span data-ttu-id="80ee6-142">System. InvalidOperationException: в топологии не обнаружены подходящие кластеры.</span><span class="sxs-lookup"><span data-stu-id="80ee6-142">System.InvalidOperationException: No matching cluster found in topology.</span></span>

<span data-ttu-id="80ee6-143">скорость</span><span class="sxs-lookup"><span data-stu-id="80ee6-143">at</span></span>

<span data-ttu-id="80ee6-144">Microsoft. RTC. Management. SyntheticTransactions. SipSyntheticTransaction. TryRetri</span><span class="sxs-lookup"><span data-stu-id="80ee6-144">Microsoft.Rtc.Management.SyntheticTransactions.SipSyntheticTransaction.TryRetri</span></span>

<span data-ttu-id="80ee6-145">eveRegistrarPortFromTopology (Int32& registrarPortNumber)</span><span class="sxs-lookup"><span data-stu-id="80ee6-145">eveRegistrarPortFromTopology(Int32& registrarPortNumber)</span></span>

<span data-ttu-id="80ee6-146">Целевое полное доменное имя: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="80ee6-146">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="80ee6-147">Результат: сбой</span><span class="sxs-lookup"><span data-stu-id="80ee6-147">Result : Failure</span></span>

<span data-ttu-id="80ee6-148">Задержка: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="80ee6-148">Latency : 00:00:00</span></span>

<span data-ttu-id="80ee6-149">Сообщение об ошибке: 10060, не удалось установить соединение из-за того, что подключенная сторона</span><span class="sxs-lookup"><span data-stu-id="80ee6-149">Error Message : 10060, A connection attempt failed because the connected party</span></span>

<span data-ttu-id="80ee6-150">не отвечает на запросы в течение определенного периода времени или</span><span class="sxs-lookup"><span data-stu-id="80ee6-150">did not properly respond after a period of time, or</span></span>

<span data-ttu-id="80ee6-151">не удалось установить соединение, так как подключенный узел имеет</span><span class="sxs-lookup"><span data-stu-id="80ee6-151">established connection failed because connected host has</span></span>

<span data-ttu-id="80ee6-152">не удалось ответить на 10.188.116.96:5061</span><span class="sxs-lookup"><span data-stu-id="80ee6-152">failed to respond 10.188.116.96:5061</span></span>

<span data-ttu-id="80ee6-153">Внутреннее исключение: сбой при попытке подключения из-за того, что</span><span class="sxs-lookup"><span data-stu-id="80ee6-153">Inner Exception:A connection attempt failed because the</span></span>

<span data-ttu-id="80ee6-154">связь с абонентом завершилась неправильно после определенного периода</span><span class="sxs-lookup"><span data-stu-id="80ee6-154">connected party did not properly respond after a period of</span></span>

<span data-ttu-id="80ee6-155">время или соединение не удалось установить, так как подключенный узел</span><span class="sxs-lookup"><span data-stu-id="80ee6-155">time, or established connection failed because connected host</span></span>

<span data-ttu-id="80ee6-156">не удалось ответить 10.188.116.96:5061</span><span class="sxs-lookup"><span data-stu-id="80ee6-156">has failed to respond 10.188.116.96:5061</span></span>

<span data-ttu-id="80ee6-157">Диагностик</span><span class="sxs-lookup"><span data-stu-id="80ee6-157">Diagnosis :</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="80ee6-158">Причины, по которым может произойти сбой теста</span><span class="sxs-lookup"><span data-stu-id="80ee6-158">Reasons why the test might have failed</span></span>

<span data-ttu-id="80ee6-159">Ниже приведены некоторые распространенные причины, по которым может произойти сбой **Test-CsUnifiedContactStore** :</span><span class="sxs-lookup"><span data-stu-id="80ee6-159">Here are some common reasons why **Test-CsUnifiedContactStore** might fail:</span></span>

  - <span data-ttu-id="80ee6-160">Предоставлено неправильное значение параметра.</span><span class="sxs-lookup"><span data-stu-id="80ee6-160">An incorrect parameter value was supplied.</span></span> <span data-ttu-id="80ee6-161">Если используется, необязательные параметры необходимо настроить правильно, или тест завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="80ee6-161">If used, the optional parameters must be configured correctly or the test will fail.</span></span> <span data-ttu-id="80ee6-162">Повторите выполнение команды без дополнительных параметров и проверьте, выполняется ли это успешно.</span><span class="sxs-lookup"><span data-stu-id="80ee6-162">Rerun the command without the optional parameters and see whether that succeeds.</span></span>

  - <span data-ttu-id="80ee6-163">Не удалось подключиться к единому хранилищу контактов, и попытка получить контакт для пользователя невозможна.</span><span class="sxs-lookup"><span data-stu-id="80ee6-163">Connect to the unified contact store failed, and the attempt to retrieve a contact for the user was not possible.</span></span> <span data-ttu-id="80ee6-164">Возможно, возникли проблемы с подключением к сети.</span><span class="sxs-lookup"><span data-stu-id="80ee6-164">There may be network connectivity issues.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="80ee6-165">См. также</span><span class="sxs-lookup"><span data-stu-id="80ee6-165">See Also</span></span>


[<span data-ttu-id="80ee6-166">New-CsUserServicesPolicy</span><span class="sxs-lookup"><span data-stu-id="80ee6-166">New-CsUserServicesPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsUserServicesPolicy)  
[<span data-ttu-id="80ee6-167">Set-CsUserServicesPolicy</span><span class="sxs-lookup"><span data-stu-id="80ee6-167">Set-CsUserServicesPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsUserServicesPolicy)  
  

<span data-ttu-id="80ee6-168"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="80ee6-168"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

