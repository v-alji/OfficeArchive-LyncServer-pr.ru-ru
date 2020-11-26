---
title: 'Lync Server 2013: Проверка разрешений администратора'
description: 'Lync Server 2013: Проверка разрешений администратора.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test admin permissions
ms:assetid: 5dda3efd-0f84-4848-819e-87b1551066b1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn767945(v=OCS.15)
ms:contentKeyID: 63969607
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 07e15be288ed31afe9303d91ce3e623d19822428
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444317"
---
# <a name="test-admin-permissions-in-lync-server-2013"></a><span data-ttu-id="f3e2a-103">Проверка разрешений администратора в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f3e2a-103">Test admin permissions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f3e2a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f3e2a-104">

<span> </span></span></span>

<span data-ttu-id="f3e2a-105">_**Тема последнего изменения:** 2014-08-18_</span><span class="sxs-lookup"><span data-stu-id="f3e2a-105">_**Topic Last Modified:** 2014-08-18_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f3e2a-106">Расписание проверки</span><span class="sxs-lookup"><span data-stu-id="f3e2a-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="f3e2a-107">После первоначального развертывания Lync Server.</span><span class="sxs-lookup"><span data-stu-id="f3e2a-107">After initial Lync Server deployment.</span></span> <span data-ttu-id="f3e2a-108">По мере необходимости, если возникают проблемы, связанные с разрешениями.</span><span class="sxs-lookup"><span data-stu-id="f3e2a-108">As needed if permission-related issues arise.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f3e2a-109">Средство тестирования</span><span class="sxs-lookup"><span data-stu-id="f3e2a-109">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="f3e2a-110">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="f3e2a-110">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f3e2a-111">Требуемые разрешения</span><span class="sxs-lookup"><span data-stu-id="f3e2a-111">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="f3e2a-112">При локальном запуске с помощью командной консоли Lync Server пользователи должны быть членами группы безопасности RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="f3e2a-112">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="f3e2a-113">При запуске с помощью удаленного экземпляра Windows PowerShell пользователям должна быть назначена роль RBAC, имеющая разрешение на запуск командлета Test-CsOUPermission.</span><span class="sxs-lookup"><span data-stu-id="f3e2a-113">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsOUPermission cmdlet.</span></span> <span data-ttu-id="f3e2a-114">Чтобы просмотреть список всех ролей RBAC, которые могут использовать этот командлет, выполните в командной строке Windows PowerShell следующую команду:</span><span class="sxs-lookup"><span data-stu-id="f3e2a-114">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsOUPermission&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="f3e2a-115">Описание</span><span class="sxs-lookup"><span data-stu-id="f3e2a-115">Description</span></span>

<span data-ttu-id="f3e2a-116">При установке Lync Server 2013 1 для задач, выполненных программой установки, группе RTCUniversalUserAdmins предоставляются разрешения Active Directory, необходимые для управления пользователями, компьютерами, контактами, контактами приложения и InetOrg лицами.</span><span class="sxs-lookup"><span data-stu-id="f3e2a-116">When you install Lync Server 2013 one of the tasks that were performed by the Setup program gives the RTCUniversalUserAdmins group the Active Directory permissions that are needed to manage users, computers, contacts, application contacts, and InetOrg persons.</span></span> <span data-ttu-id="f3e2a-117">Если вы отключили наследование разрешений в службе каталогов Active Directory, вам не удастся назначить эти разрешения.</span><span class="sxs-lookup"><span data-stu-id="f3e2a-117">If you have disabled permission inheritance in Active Directory setup won't be able to assign those permissions.</span></span> <span data-ttu-id="f3e2a-118">В результате участники группы RTCUniversalUserAdmins не смогут управлять сущностями Lync Server.</span><span class="sxs-lookup"><span data-stu-id="f3e2a-118">As a result, members of the RTCUniversalUserAdmins group won't be able to manage Lync Server entities.</span></span> <span data-ttu-id="f3e2a-119">Эти права на управление будут доступны только администраторам домена.</span><span class="sxs-lookup"><span data-stu-id="f3e2a-119">Those management privileges will only be available to domain administrators.</span></span>

<span data-ttu-id="f3e2a-120">Командлет Test-CsOUPermission проверяет, что необходимые разрешения, необходимые для управления пользователями, компьютерами и другими объектами, задаются в контейнере Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f3e2a-120">The Test-CsOUPermission cmdlet verifies that the required permissions that are needed to manage users, computers, and other objects are set on an Active Directory container.</span></span> <span data-ttu-id="f3e2a-121">Если эти разрешения не заданы, вы можете устранить эту проблему, выполнив командлет [Grant-CsOUPermission](https://docs.microsoft.com/powershell/module/skype/Grant-CsOUPermission) .</span><span class="sxs-lookup"><span data-stu-id="f3e2a-121">If those permissions are not set, you can resolve this problem by running the [Grant-CsOUPermission](https://docs.microsoft.com/powershell/module/skype/Grant-CsOUPermission) cmdlet.</span></span>

<span data-ttu-id="f3e2a-122">Обратите внимание, что Grant-CsOUPermission может назначать разрешения только участникам группы RTCUniversalUserAdmins.</span><span class="sxs-lookup"><span data-stu-id="f3e2a-122">Note that Grant-CsOUPermission can only assign permissions to members of the RTCUniversalUserAdmins group.</span></span> <span data-ttu-id="f3e2a-123">Вы не можете использовать этот командлет, чтобы предоставить разрешения для произвольного пользователя или группы.</span><span class="sxs-lookup"><span data-stu-id="f3e2a-123">You can’t use this cmdlet to grant permissions to an arbitrary user or group.</span></span> <span data-ttu-id="f3e2a-124">Если вы хотите, чтобы другой пользователь или группа имели разрешения на управление пользователями, вы должны добавить этого пользователя (или группу) в группу RTCUniversalUserAdmins.</span><span class="sxs-lookup"><span data-stu-id="f3e2a-124">If you want a different user or group to have user management permissions, you should add that user (or group) to the RTCUniversalUserAdmins group.</span></span>

<span data-ttu-id="f3e2a-125">Дополнительные сведения о разрешениях для подразделений можно найти в статье [отключение наследования разрешений для пользователей и контейнеров inetOrgPerson в Lync Server 2013](lync-server-2013-permissions-inheritance-is-disabled-on-computers-users-or-inetorgperson-containers.md).</span><span class="sxs-lookup"><span data-stu-id="f3e2a-125">For more information on OU permissions, see the article [Permissions inheritance Is disabled on computers, users, or InetOrgPerson containers in Lync Server 2013](lync-server-2013-permissions-inheritance-is-disabled-on-computers-users-or-inetorgperson-containers.md).</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="f3e2a-126">Выполнение теста</span><span class="sxs-lookup"><span data-stu-id="f3e2a-126">Running the test</span></span>

<span data-ttu-id="f3e2a-127">Чтобы убедиться в том, что для контейнера заданы разрешения на управление, выполните командлет Test-CsOUPermission, а затем различающееся имя контейнера и тип проверяемых разрешений.</span><span class="sxs-lookup"><span data-stu-id="f3e2a-127">To verify that management permissions are set on a container, run the Test-CsOUPermission cmdlet followed by the distinguished name of the container and by the type of permissions that you are verifying.</span></span> <span data-ttu-id="f3e2a-128">Например, эта команда проверяет, заданы ли разрешения пользователей на подразделение OU = Redmond, DC = плана litwareinc, DC = com:</span><span class="sxs-lookup"><span data-stu-id="f3e2a-128">For example, this command checks whether user permissions are set on the OU ou=Redmond,dc=litwareinc,dc=com:</span></span>

    Test-CsOUPermission -OU "ou=Redmond,dc=litwareinc,dc=com" -ObjectType "user"

<span data-ttu-id="f3e2a-129">Для проверки нескольких разрешений с помощью одной команды заключите все типы разрешений в кавычки, а затем разделите их с помощью запятых.</span><span class="sxs-lookup"><span data-stu-id="f3e2a-129">To verify multiple permissions by using a single command, enclose each permission type enclosed in quotation marks, then separate those types by using commas.</span></span> <span data-ttu-id="f3e2a-130">Например, одна из этих команд проверяет разрешения пользователей, компьютеров и контактов.</span><span class="sxs-lookup"><span data-stu-id="f3e2a-130">For example, this one command verifies user, computer, and contact permissions:</span></span>

    Test-CsOUPermission -OU "ou=Redmond,dc=litwareinc,dc=com" -ObjectType "user", "computer", "contact"

<span data-ttu-id="f3e2a-131">Дополнительные сведения можно найти в разделе справки по командлету [Test-CsOUPermission](https://docs.microsoft.com/powershell/module/skype/Test-CsOUPermission) .</span><span class="sxs-lookup"><span data-stu-id="f3e2a-131">For more information, see the help topic for the [Test-CsOUPermission](https://docs.microsoft.com/powershell/module/skype/Test-CsOUPermission) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="f3e2a-132">Определение успеха или сбоя</span><span class="sxs-lookup"><span data-stu-id="f3e2a-132">Determining success or failure</span></span>

<span data-ttu-id="f3e2a-133">Если необходимые разрешения уже установлены, Test-CsOUPermission будет возвращать ответ из одного слова:</span><span class="sxs-lookup"><span data-stu-id="f3e2a-133">If the required permissions have already been set then Test-CsOUPermission will return a one-word response:</span></span>

<span data-ttu-id="f3e2a-134">Верно</span><span class="sxs-lookup"><span data-stu-id="f3e2a-134">True</span></span>

<span data-ttu-id="f3e2a-135">Если необходимые разрешения не заданы, Test-CsOUPermission возвратит значение false.</span><span class="sxs-lookup"><span data-stu-id="f3e2a-135">If the required permissions are not set then Test-CsOUPermission will return the value False.</span></span> <span data-ttu-id="f3e2a-136">Может потребоваться найти это значение в течение некоторого времени.</span><span class="sxs-lookup"><span data-stu-id="f3e2a-136">You might have to search for a moment to find this value.</span></span> <span data-ttu-id="f3e2a-137">Как правило, он встраивается в несколько соответствующих предупреждений.</span><span class="sxs-lookup"><span data-stu-id="f3e2a-137">It will typically be embedded inside several accompanying warnings.</span></span> <span data-ttu-id="f3e2a-138">Например:</span><span class="sxs-lookup"><span data-stu-id="f3e2a-138">For example:</span></span>

<span data-ttu-id="f3e2a-139">Предупреждение: запись контроля доступа (ACE) ATL-CS-001 \\ RTCUniversalUserReadOnlyGroup; Allow; ReadProperty; ContainerInherit; Потомки; bf967aba-0de6-11d0-00aa003049e2; d819615a-3b9b-4738-b47e-f1bd8ee3aea4</span><span class="sxs-lookup"><span data-stu-id="f3e2a-139">WARNING: access control entry (ACE) atl-cs-001\\RTCUniversalUserReadOnlyGroup; allow; ReadProperty; ContainerInherit; Descendents; bf967aba-0de6-11d0-00aa003049e2; d819615a-3b9b-4738-b47e-f1bd8ee3aea4</span></span>

<span data-ttu-id="f3e2a-140">Предупреждение: элементы управления доступом (ACE) для объекта "OU = NorthAmerica, DC = ATL-CS-001 DC = \\ плана litwareinc, DC = com" не готовы.</span><span class="sxs-lookup"><span data-stu-id="f3e2a-140">WARNING: The access control entries (ACEs) on the object "OU=NorthAmerica,DC=atl-cs-001\\DC=litwareinc,DC=com" are not ready.</span></span>

<span data-ttu-id="f3e2a-141">False</span><span class="sxs-lookup"><span data-stu-id="f3e2a-141">False</span></span>

<span data-ttu-id="f3e2a-142">Предупреждение: обработка "Test-CsOUPermission" завершена с предупреждениями.</span><span class="sxs-lookup"><span data-stu-id="f3e2a-142">WARNING: "Test-CsOUPermission" processing has completed with warnings.</span></span> <span data-ttu-id="f3e2a-143">во время этого запуска записано предупреждение "2".</span><span class="sxs-lookup"><span data-stu-id="f3e2a-143">"2" warnings were recorded during this run.</span></span>

<span data-ttu-id="f3e2a-144">Предупреждение: подробные результаты можно найти на странице "C: \\ Users \\ Admin \\ AppData \\ Local \\ temp \\Test-CsOUPermission-5d7a89af-f854-4a9c-87e3-69e37e58de.html".</span><span class="sxs-lookup"><span data-stu-id="f3e2a-144">WARNING: Detailed results can be found at "C:\\Users\\Admin\\AppData\\Local\\Temp\\Test-CsOUPermission-5d7a89af-f854-4a9c-87e3-69e37e58de.html".</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="f3e2a-145">Причины, по которым может произойти сбой теста</span><span class="sxs-lookup"><span data-stu-id="f3e2a-145">Reasons why the test might have failed</span></span>

<span data-ttu-id="f3e2a-146">Если Test-CsOUPermission не проходит, это обычно означает, что указанное разрешение не назначено группе RTCUniversalUserAdmins.</span><span class="sxs-lookup"><span data-stu-id="f3e2a-146">If Test-CsOUPermission fails that will usually mean that the specified permission has not been assign to the RTCUniversalUserAdmins group.</span></span> <span data-ttu-id="f3e2a-147">Вы можете устранить эту проблему и назначить необходимые разрешения с помощью командлета Grant-CsOUPermission.</span><span class="sxs-lookup"><span data-stu-id="f3e2a-147">You can resolve this problem, and assign the required permissions, by using the Grant-CsOUPermission cmdlet.</span></span> <span data-ttu-id="f3e2a-148">Например, эта команда предоставляет разрешения на доступ к подразделению для пользователей, контактов и inetOrgPersons группе RTCUniversalUserAdmins:</span><span class="sxs-lookup"><span data-stu-id="f3e2a-148">For example, this command gives OU permissions for users, contacts, and inetOrgPersons to the RTCUniversalUserAdmins group:</span></span>

    Grant-CsOUPermission -OU "ou=Redmond,dc=litwareinc,dc=com" -ObjectType "user", "contact", "inetOrgPerson"

<span data-ttu-id="f3e2a-149">Дополнительные сведения можно найти в разделе справки по командлету Grant-CsOUPermission.</span><span class="sxs-lookup"><span data-stu-id="f3e2a-149">For more information, see the help topic for the Grant-CsOUPermission cmdlet.</span></span>

<span data-ttu-id="f3e2a-150"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f3e2a-150"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

