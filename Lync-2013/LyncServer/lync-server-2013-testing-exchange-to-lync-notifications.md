---
title: 'Lync Server 2013: проверка Exchange на уведомления Lync'
description: 'Lync Server 2013: проверка Exchange на уведомления Lync.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing Exchange to Lync notifications
ms:assetid: ed2d6325-3cf5-4450-9951-03092bcb0a7c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn727315(v=OCS.15)
ms:contentKeyID: 63969665
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bdf453bfdaab7e7b6bdaae8b67ac7759c0d55af4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398971"
---
# <a name="testing-exchange-to-lync-notifications-in-lync-server-2013"></a><span data-ttu-id="ee2d0-103">Проверка Exchange для уведомлений Lync в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ee2d0-103">Testing Exchange to Lync notifications in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ee2d0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ee2d0-104">

<span> </span></span></span>

<span data-ttu-id="ee2d0-105">_**Тема последнего изменения:** 2014-11-01_</span><span class="sxs-lookup"><span data-stu-id="ee2d0-105">_**Topic Last Modified:** 2014-11-01_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ee2d0-106">Расписание проверки</span><span class="sxs-lookup"><span data-stu-id="ee2d0-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="ee2d0-107">Ежедневно</span><span class="sxs-lookup"><span data-stu-id="ee2d0-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee2d0-108">Средство тестирования</span><span class="sxs-lookup"><span data-stu-id="ee2d0-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="ee2d0-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="ee2d0-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee2d0-110">Требуемые разрешения</span><span class="sxs-lookup"><span data-stu-id="ee2d0-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="ee2d0-111">При локальном запуске с помощью командной консоли Lync Server пользователи должны быть членами группы безопасности RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="ee2d0-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="ee2d0-112">При запуске с помощью удаленного экземпляра Windows PowerShell пользователям должна быть назначена роль RBAC, имеющая разрешение на запуск командлета <strong>Test-CsExStorageNotification</strong> .</span><span class="sxs-lookup"><span data-stu-id="ee2d0-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the <strong>Test-CsExStorageNotification</strong> cmdlet.</span></span> <span data-ttu-id="ee2d0-113">Чтобы просмотреть список всех ролей RBAC, которые могут использовать этот командлет, выполните в командной строке Windows PowerShell следующую команду:</span><span class="sxs-lookup"><span data-stu-id="ee2d0-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsExStorageNotification&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="ee2d0-114">Описание</span><span class="sxs-lookup"><span data-stu-id="ee2d0-114">Description</span></span>

<span data-ttu-id="ee2d0-115">Командлет **Test-CsExStorageNotification** используется для подтверждения того, что служба уведомлений сервера Microsoft Exchange Server 2013 может уведомлять Lync Server 2013 о внесении обновлений в список контактов пользователя.</span><span class="sxs-lookup"><span data-stu-id="ee2d0-115">The **Test-CsExStorageNotification** cmdlet is used to verify that the Microsoft Exchange Server 2013 notification service can notify Lync Server 2013 any time updates are made to a user's Contact List.</span></span> <span data-ttu-id="ee2d0-116">Этот командлет действует только в том случае, если вы используете единое хранилище контактов.</span><span class="sxs-lookup"><span data-stu-id="ee2d0-116">This cmdlet is valid only if you are using the unified contact store.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="ee2d0-117">Выполнение теста</span><span class="sxs-lookup"><span data-stu-id="ee2d0-117">Running the test</span></span>

<span data-ttu-id="ee2d0-118">Команда, показанная в примере 1, проверяет, может ли служба хранилища Lync Server подключиться к службе уведомлений почтового ящика сервера Microsoft Exchange Server для пользователя sip:kenmyer@litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="ee2d0-118">The command shown in Example 1 tests to see whether the Lync Server Storage Service can connect to the Microsoft Exchange Server mailbox notification service for the user sip:kenmyer@litwareinc.com.</span></span> <span data-ttu-id="ee2d0-119">В этом примере NetNamedPipe используется в качестве привязки WCF.</span><span class="sxs-lookup"><span data-stu-id="ee2d0-119">In this example, NetNamedPipe is used as the WCF binding.</span></span>

    Test-CsExStorageNotification -SipUri "sip:kenmyer@litwareinc.com" -Binding "NetNamedPipe"

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="ee2d0-120">Определение успеха или сбоя</span><span class="sxs-lookup"><span data-stu-id="ee2d0-120">Determining success or failure</span></span>

<span data-ttu-id="ee2d0-121">Если интеграция с Exchange настроена правильно, вы получите вывод примерно так, чтобы свойство Result пометило " **успешно**".</span><span class="sxs-lookup"><span data-stu-id="ee2d0-121">If Exchange integration is configured correctly , you'll receive output similar to this, with the Result property marked as **Success**:</span></span>

<span data-ttu-id="ee2d0-122">Целевое полное доменное имя: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="ee2d0-122">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="ee2d0-123">Результат: успех</span><span class="sxs-lookup"><span data-stu-id="ee2d0-123">Result : Success</span></span>

<span data-ttu-id="ee2d0-124">Задержка: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="ee2d0-124">Latency : 00:00:00</span></span>

<span data-ttu-id="ee2d0-125">Сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="ee2d0-125">Error Message :</span></span>

<span data-ttu-id="ee2d0-126">Диагностик</span><span class="sxs-lookup"><span data-stu-id="ee2d0-126">Diagnosis :</span></span>

<span data-ttu-id="ee2d0-127">Если указанный пользователь не может получать уведомления, результат будет отображаться как сбой, а дополнительные сведения будут записаны в свойствах Error и диагноз.</span><span class="sxs-lookup"><span data-stu-id="ee2d0-127">If the specified user can't receive notifications, the Result will be shown as Failure, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="ee2d0-128">Целевое полное доменное имя: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="ee2d0-128">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="ee2d0-129">Результат: сбой</span><span class="sxs-lookup"><span data-stu-id="ee2d0-129">Result : Failure</span></span>

<span data-ttu-id="ee2d0-130">Задержка: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="ee2d0-130">Latency : 00:00:00</span></span>

<span data-ttu-id="ee2d0-131">Сообщение об ошибке: 10060, не удалось установить соединение из-за того, что подключенная сторона</span><span class="sxs-lookup"><span data-stu-id="ee2d0-131">Error Message : 10060, A connection attempt failed because the connected party</span></span>

<span data-ttu-id="ee2d0-132">не отвечает на запросы в течение определенного периода времени или</span><span class="sxs-lookup"><span data-stu-id="ee2d0-132">did not properly respond after a period of time, or</span></span>

<span data-ttu-id="ee2d0-133">не удалось установить соединение, так как подключенный узел имеет</span><span class="sxs-lookup"><span data-stu-id="ee2d0-133">established connection failed because connected host has</span></span>

<span data-ttu-id="ee2d0-134">не удалось ответить на 10.188.116.96:5061</span><span class="sxs-lookup"><span data-stu-id="ee2d0-134">failed to respond 10.188.116.96:5061</span></span>

<span data-ttu-id="ee2d0-135">Внутреннее исключение: сбой при попытке подключения из-за того, что</span><span class="sxs-lookup"><span data-stu-id="ee2d0-135">Inner Exception:A connection attempt failed because the</span></span>

<span data-ttu-id="ee2d0-136">связь с абонентом завершилась неправильно после определенного периода</span><span class="sxs-lookup"><span data-stu-id="ee2d0-136">connected party did not properly respond after a period of</span></span>

<span data-ttu-id="ee2d0-137">время или соединение не удалось установить, так как подключенный узел</span><span class="sxs-lookup"><span data-stu-id="ee2d0-137">time, or established connection failed because connected host</span></span>

<span data-ttu-id="ee2d0-138">не удалось ответить 10.188.116.96:5061</span><span class="sxs-lookup"><span data-stu-id="ee2d0-138">has failed to respond 10.188.116.96:5061</span></span>

<span data-ttu-id="ee2d0-139">Диагностик</span><span class="sxs-lookup"><span data-stu-id="ee2d0-139">Diagnosis :</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="ee2d0-140">Причины, по которым может произойти сбой теста</span><span class="sxs-lookup"><span data-stu-id="ee2d0-140">Reasons why the test might have failed</span></span>

<span data-ttu-id="ee2d0-141">Ниже приведены некоторые распространенные причины, по которым может произойти сбой **Test-CsExStorageNotification** :</span><span class="sxs-lookup"><span data-stu-id="ee2d0-141">Here are some common reasons why **Test-CsExStorageNotification** might fail:</span></span>

  - <span data-ttu-id="ee2d0-142">Предоставлено неправильное значение параметра.</span><span class="sxs-lookup"><span data-stu-id="ee2d0-142">An incorrect parameter value was supplied.</span></span> <span data-ttu-id="ee2d0-143">Если используется, необязательные параметры необходимо настроить правильно, или тест завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="ee2d0-143">If used, the optional parameters must be configured correctly or the test will fail.</span></span> <span data-ttu-id="ee2d0-144">Повторите выполнение команды без дополнительных параметров и проверьте, выполняется ли это успешно.</span><span class="sxs-lookup"><span data-stu-id="ee2d0-144">Rerun the command without the optional parameters and see whether that succeeds.</span></span>

  - <span data-ttu-id="ee2d0-145">Эта команда завершится сбоем, если сервер Microsoft Exchange неправильно настроен или еще не развернут.</span><span class="sxs-lookup"><span data-stu-id="ee2d0-145">This command will fail if the Microsoft Exchange Server is misconfigured or not yet deployed.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="ee2d0-146">См. также</span><span class="sxs-lookup"><span data-stu-id="ee2d0-146">See Also</span></span>


[<span data-ttu-id="ee2d0-147">Test-CsExStorageConnectivity</span><span class="sxs-lookup"><span data-stu-id="ee2d0-147">Test-CsExStorageConnectivity</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsExStorageConnectivity)  
  

<span data-ttu-id="ee2d0-148"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ee2d0-148"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

