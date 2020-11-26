---
title: 'Lync Server 2013: Конфигурация узла контрольных значений'
description: 'Lync Server 2013: Конфигурация узла контрольных значений.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing watcher node configuration
ms:assetid: f9ecd85c-0ae9-4906-b786-6b002b5a77c6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn751537(v=OCS.15)
ms:contentKeyID: 63969667
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f1eeb141eee011d7e06f5dd49e483e026484d733
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440929"
---
# <a name="testing-watcher-node-configuration-in-lync-server-2013"></a><span data-ttu-id="c7ebf-103">Конфигурация узла контрольных значений в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c7ebf-103">Testing watcher node configuration in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c7ebf-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c7ebf-104">

<span> </span></span></span>

<span data-ttu-id="c7ebf-105">_**Тема последнего изменения:** 2014-11-03_</span><span class="sxs-lookup"><span data-stu-id="c7ebf-105">_**Topic Last Modified:** 2014-11-03_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c7ebf-106">Расписание проверки</span><span class="sxs-lookup"><span data-stu-id="c7ebf-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="c7ebf-107">Ежедневно</span><span class="sxs-lookup"><span data-stu-id="c7ebf-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebf-108">Средство тестирования</span><span class="sxs-lookup"><span data-stu-id="c7ebf-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="c7ebf-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="c7ebf-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebf-110">Требуемые разрешения</span><span class="sxs-lookup"><span data-stu-id="c7ebf-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="c7ebf-111">При локальном запуске с помощью командной консоли Lync Server пользователи должны быть членами группы безопасности RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="c7ebf-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="c7ebf-112">При запуске с помощью удаленного экземпляра Windows PowerShell пользователям должна быть назначена роль RBAC, имеющая разрешение на запуск командлета <strong>Test-CsWatcherNodeConfiguration</strong> .</span><span class="sxs-lookup"><span data-stu-id="c7ebf-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the <strong>Test-CsWatcherNodeConfiguration</strong> cmdlet.</span></span> <span data-ttu-id="c7ebf-113">Чтобы просмотреть список всех ролей RBAC, которые могут использовать этот командлет, выполните в командной строке Windows PowerShell следующую команду:</span><span class="sxs-lookup"><span data-stu-id="c7ebf-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot; Test-CsWatcherNodeConfiguration&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="c7ebf-114">Описание</span><span class="sxs-lookup"><span data-stu-id="c7ebf-114">Description</span></span>

<span data-ttu-id="c7ebf-115">Если вы используете Microsoft System Center Operations Manager для мониторинга сервера Lync Server 2013, у вас есть возможность настроить "узлы контрольных данных": компьютеры, периодически и автоматически выполняющие синтетические транзакции для проверки правильности работы сервера Lync Server.</span><span class="sxs-lookup"><span data-stu-id="c7ebf-115">If you are using Microsoft System Center Operations Manager to monitor Lync Server 2013 then you have the option of setting up "watcher nodes": computers that periodically, and automatically, run synthetic transactions to verify that Lync Server is working as expected.</span></span> <span data-ttu-id="c7ebf-116">Узлы наблюдателей назначаются пулам и управляются с помощью командлетов **CsWatcherNodeConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="c7ebf-116">Watcher nodes are assigned to pools, and are managed by using the **CsWatcherNodeConfiguration** cmdlets.</span></span> <span data-ttu-id="c7ebf-117">Обратите внимание, что при использовании System Center Operations Manager вам не нужно устанавливать узлы наблюдения.</span><span class="sxs-lookup"><span data-stu-id="c7ebf-117">Note that you do not need to install watcher nodes if you are using System Center Operations Manager.</span></span> <span data-ttu-id="c7ebf-118">Вы по-прежнему можете отслеживать систему без использования узлов-наблюдателей.</span><span class="sxs-lookup"><span data-stu-id="c7ebf-118">You can still monitor your system without using watcher nodes.</span></span> <span data-ttu-id="c7ebf-119">Единственная разница заключается в том, что все синтетические транзакции, которые необходимо выполнить, должны вызываться вручную, а не автоматически с помощью Operations Manager.</span><span class="sxs-lookup"><span data-stu-id="c7ebf-119">The only difference is that any synthetic transactions that you want to run must be invoked manually instead of automatically invoked by Operations Manager.</span></span>

<span data-ttu-id="c7ebf-120">Командлет **Test-CsWatcherNodeConfiguration** позволяет проверить, правильно ли настроен узел наблюдателя и назначен допустимым пулам Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c7ebf-120">The **Test-CsWatcherNodeConfiguration** cmdlet enables you to verify that a watcher node was configured correctly and is assigned to a valid Lync Server 2013 pool.</span></span> <span data-ttu-id="c7ebf-121">Обратите внимание на то, что командлет **Test-CsWatcherNodeConfiguration** должен выполняться на самом узле наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="c7ebf-121">Note that the **Test-CsWatcherNodeConfiguration** cmdlet must be run on the watcher node itself.</span></span> <span data-ttu-id="c7ebf-122">Командлет не может выполняться для удаленных компьютеров.</span><span class="sxs-lookup"><span data-stu-id="c7ebf-122">The cmdlet cannot be run against remote computers.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="c7ebf-123">Выполнение теста</span><span class="sxs-lookup"><span data-stu-id="c7ebf-123">Running the test</span></span>

<span data-ttu-id="c7ebf-124">Следующая команда проверяет параметры конфигурации для каждого узла-наблюдателя, который используется в Организации.</span><span class="sxs-lookup"><span data-stu-id="c7ebf-124">The following command verifies the configuration settings for each watcher node that is being used in the organization.</span></span>

    Test-CsWatcherNodeConfiguration

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="c7ebf-125">Определение успеха или сбоя</span><span class="sxs-lookup"><span data-stu-id="c7ebf-125">Determining success or failure</span></span>

<span data-ttu-id="c7ebf-126">Приведенный ниже успешный пример показывает систему с четырьмя пограничными серверами.</span><span class="sxs-lookup"><span data-stu-id="c7ebf-126">The following successful sample output shows a system with four edge servers.</span></span>

<span data-ttu-id="c7ebf-127">Проверка целевого пула atl-cs-001.litwareinc.com в соответствии с топологией.</span><span class="sxs-lookup"><span data-stu-id="c7ebf-127">Validating target pool atl-cs-001.litwareinc.com against topology.</span></span>

<span data-ttu-id="c7ebf-128">Успех: конечный пул atl-cs-001.litwareinc.com существует в топологии.</span><span class="sxs-lookup"><span data-stu-id="c7ebf-128">Success: Target pool atl-cs-001.litwareinc.com exists in topology.</span></span>

<span data-ttu-id="c7ebf-129">Успех: на целевом пуле atl-cs-001.litwareinc.com установлена роль регистратора.</span><span class="sxs-lookup"><span data-stu-id="c7ebf-129">Success: Target pool atl-cs-001.litwareinc.com has Registrar role installed.</span></span>

<span data-ttu-id="c7ebf-130">Успех: atl-cs-001.litwareinc.com пула поддерживает версию.</span><span class="sxs-lookup"><span data-stu-id="c7ebf-130">Success: Target pool atl-cs-001.litwareinc.com is supported version.</span></span>

<span data-ttu-id="c7ebf-131">Успех: номер порта для целевого atl-cs-001.litwareinc.com пула 5061 является правильным.</span><span class="sxs-lookup"><span data-stu-id="c7ebf-131">Success: Port number for 5061 Target pool atl-cs-001.litwareinc.com is correct.</span></span>

<span data-ttu-id="c7ebf-132">Проверка наличия отсутствующих пулов в конфигурации узла-наблюдателя начинается.</span><span class="sxs-lookup"><span data-stu-id="c7ebf-132">Checking for missing pools in watcher node configuration is started.</span></span> <span data-ttu-id="c7ebf-133">Если обнаружена какая – либо ошибка, она будет распечатана.</span><span class="sxs-lookup"><span data-stu-id="c7ebf-133">If any error is detected, it will be printed.</span></span>

<span data-ttu-id="c7ebf-134">Проверка наличия отсутствующих пулов в конфигурации узла-наблюдателя завершена.</span><span class="sxs-lookup"><span data-stu-id="c7ebf-134">Checking for missing pools in watcher node configuration is finished.</span></span>

<span data-ttu-id="c7ebf-135">Начата проверка разделов реестра узла-наблюдателя, созданных при установке узла-наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="c7ebf-135">Checking for watcher node registry keys created by watcher node installation, is started.</span></span> <span data-ttu-id="c7ebf-136">Если обнаружена какая – либо ошибка, она будет распечатана.</span><span class="sxs-lookup"><span data-stu-id="c7ebf-136">If any error is detected, it will be printed.</span></span>

<span data-ttu-id="c7ebf-137">Проверка наличия разделов реестра узла-наблюдателя, созданных при установке узла-наблюдателя, завершено.</span><span class="sxs-lookup"><span data-stu-id="c7ebf-137">Checking for watcher node registry keys created by watcher node installation, is finished.</span></span> <span data-ttu-id="c7ebf-138">Обнаруженный тип проверки подлинности — Negotiate.</span><span class="sxs-lookup"><span data-stu-id="c7ebf-138">Detected authentication type is Negotiate.</span></span>

<span data-ttu-id="c7ebf-139">Успешная проверка существования учетных данных тестового пользователя: user1@ atl-cs-001.litwareinc.com в хранилище управления учетными данными.</span><span class="sxs-lookup"><span data-stu-id="c7ebf-139">Successfully validated existence of test user’s credential sip:user1@ atl-cs-001.litwareinc.com in credential management store.</span></span>

<span data-ttu-id="c7ebf-140">Успешная проверка существования учетных данных тестового пользователя: user2@ atl-cs-001.litwareinc.com в хранилище управления учетными данными.</span><span class="sxs-lookup"><span data-stu-id="c7ebf-140">Successfully validated existence of test user’s credential sip:user2@ atl-cs-001.litwareinc.com in credential management store.</span></span>

<span data-ttu-id="c7ebf-141">Проверка наличия отсутствующих пулов в конфигурации узла-наблюдателя начинается.</span><span class="sxs-lookup"><span data-stu-id="c7ebf-141">Checking for missing pools in watcher node configuration is started.</span></span> <span data-ttu-id="c7ebf-142">Если обнаружена какая – либо ошибка, она будет распечатана.</span><span class="sxs-lookup"><span data-stu-id="c7ebf-142">If any error is detected, it will be printed.</span></span>

<span data-ttu-id="c7ebf-143">Предупреждение: atl-cs-001.litwareinc.com пула имеет регистратор</span><span class="sxs-lookup"><span data-stu-id="c7ebf-143">WARNING: Pool atl-cs-001.litwareinc.com has Registrar</span></span>

<span data-ttu-id="c7ebf-144">роль установлена, но для нее не заданы тестовые пользователи.</span><span class="sxs-lookup"><span data-stu-id="c7ebf-144">role installed, but there are no test users configured for it.</span></span>

<span data-ttu-id="c7ebf-145">Проверка наличия отсутствующих пулов в конфигурации узла-наблюдателя завершена.</span><span class="sxs-lookup"><span data-stu-id="c7ebf-145">Checking for missing pools in watcher node configuration is finished.</span></span>

<span data-ttu-id="c7ebf-146">Проверка наличия разделов реестра для узла-наблюдателя, созданных при установке узла-наблюдателя, —</span><span class="sxs-lookup"><span data-stu-id="c7ebf-146">Checking for watcher node registry keys created by watcher node installation, is</span></span>

<span data-ttu-id="c7ebf-147">загружен.</span><span class="sxs-lookup"><span data-stu-id="c7ebf-147">started.</span></span> <span data-ttu-id="c7ebf-148">Если обнаружена какая – либо ошибка, она будет распечатана.</span><span class="sxs-lookup"><span data-stu-id="c7ebf-148">If any error is detected, it will be printed.</span></span>

<span data-ttu-id="c7ebf-149">Test-CsWatcherNodeConfiguration: не удается найти раздел реестра Health в</span><span class="sxs-lookup"><span data-stu-id="c7ebf-149">Test-CsWatcherNodeConfiguration : Cannot find Health registry key in</span></span>

<span data-ttu-id="c7ebf-150">Программное обеспечение \\ Microsoft для \\ обмена данными в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="c7ebf-150">Software\\Microsoft\\Real-Time Communications.</span></span> <span data-ttu-id="c7ebf-151">Убедитесь в том, что узел наблюдателя. MSI является</span><span class="sxs-lookup"><span data-stu-id="c7ebf-151">Make sure watcher node .msi is</span></span>

<span data-ttu-id="c7ebf-152">установлено правильно.</span><span class="sxs-lookup"><span data-stu-id="c7ebf-152">installed properly.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="c7ebf-153">Причины, по которым может произойти сбой теста</span><span class="sxs-lookup"><span data-stu-id="c7ebf-153">Reasons why the test might have failed</span></span>

<span data-ttu-id="c7ebf-154">Ниже приведены некоторые распространенные причины, по которым может произойти сбой **Test-CsWatcherNodeConfiguration** :</span><span class="sxs-lookup"><span data-stu-id="c7ebf-154">Here are some common reasons why **Test-CsWatcherNodeConfiguration** might fail:</span></span>

  - <span data-ttu-id="c7ebf-155">Узел-наблюдатель установлен неправильно.</span><span class="sxs-lookup"><span data-stu-id="c7ebf-155">Watcher node is not correctly installed.</span></span>

  - <span data-ttu-id="c7ebf-156">Тестовые пользователи не настроены.</span><span class="sxs-lookup"><span data-stu-id="c7ebf-156">No test users are configured.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="c7ebf-157">См. также</span><span class="sxs-lookup"><span data-stu-id="c7ebf-157">See Also</span></span>


[<span data-ttu-id="c7ebf-158">Get-CsWatcherNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="c7ebf-158">Get-CsWatcherNodeConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsWatcherNodeConfiguration)  
[<span data-ttu-id="c7ebf-159">New-CsWatcherNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="c7ebf-159">New-CsWatcherNodeConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsWatcherNodeConfiguration)  
[<span data-ttu-id="c7ebf-160">Remove-CsWatcherNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="c7ebf-160">Remove-CsWatcherNodeConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsWatcherNodeConfiguration)  
[<span data-ttu-id="c7ebf-161">Set-CsWatcherNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="c7ebf-161">Set-CsWatcherNodeConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsWatcherNodeConfiguration)  
  

<span data-ttu-id="c7ebf-162"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c7ebf-162"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

