---
title: 'Lync Server 2013: поведение группы ответа при отказе пула'
description: Взаимодействие групп ответов Lync Server 2013 в случае сбоя пула.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Response group experience during pool failure
ms:assetid: 4e00fb38-64b1-4fd9-903d-7639177bc303
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204886(v=OCS.15)
ms:contentKeyID: 48184116
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7d8d5904bc6934d4c330202bafa66d6dd8a16ff5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436246"
---
# <a name="response-group-experience-in-lync-server-2013-during-pool-failure"></a><span data-ttu-id="2dd3a-103">Поведение группы ответа Lync Server 2013 при отказе пула</span><span class="sxs-lookup"><span data-stu-id="2dd3a-103">Response group experience in Lync Server 2013 during pool failure</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2dd3a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2dd3a-104">

<span> </span></span></span>

<span data-ttu-id="2dd3a-105">_**Тема последнего изменения:** 2012-10-30_</span><span class="sxs-lookup"><span data-stu-id="2dd3a-105">_**Topic Last Modified:** 2012-10-30_</span></span>

<span data-ttu-id="2dd3a-106">В этом разделе объясняется, как влияют действия группы ответа на следующие этапы:</span><span class="sxs-lookup"><span data-stu-id="2dd3a-106">This section describes in detail how response group activity is affected in the following stages:</span></span>

  - <span data-ttu-id="2dd3a-107">В основном пуле происходит отключение, но еще не инициирована отработка отказа.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-107">An outage occurs in the primary pool, but failover is not yet initiated.</span></span>

  - <span data-ttu-id="2dd3a-108">Ошибка при попытке выполнить обслуживание в пуле резервных копий.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-108">Service is failed over to the backup pool.</span></span>

  - <span data-ttu-id="2dd3a-109">Сбой при восстановлении службы в основной пул.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-109">Service is failed back to the primary pool.</span></span>

<div>

## <a name="user-experience-when-outage-occurs"></a><span data-ttu-id="2dd3a-110">Взаимодействие с пользователем при возникновении сбоя</span><span class="sxs-lookup"><span data-stu-id="2dd3a-110">User Experience When Outage Occurs</span></span>

<span data-ttu-id="2dd3a-111">При возникновении сбоя в работе пула или сайта, но администратор еще не инициировал отработку отказа, действия группы ответа обрабатываются в соответствии с приведенной ниже таблицей.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-111">When a pool or site outage occurs, but the administrator has not yet initiated failover, response group activity is handled as described in the following table.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="2dd3a-112">Во время аварийного восстановления звонки работают по-разному в зависимости от того, были ли группы ответов основного пула импортированы в пул резервного копирования во время восстановления.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-112">During disaster recovery, calls behave differently depending on whether the primary pool response groups were imported to the backup pool during recovery.</span></span> <span data-ttu-id="2dd3a-113">В приведенной ниже таблице ссылки на импортированные группы ответов означают, что группы ответов основного пула были импортированы в пул резервных копий в режиме восстановления после сбоя.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-113">In the following table, references to imported response groups mean that primary pool response groups were imported to the backup pool during disaster recovery mode.</span></span>



</div>

### <a name="outage-occurs"></a><span data-ttu-id="2dd3a-114">Возникает отключение</span><span class="sxs-lookup"><span data-stu-id="2dd3a-114">Outage Occurs</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2dd3a-115">Тип звонка или действия пользователя</span><span class="sxs-lookup"><span data-stu-id="2dd3a-115">Type of call or user action</span></span></th>
<th><span data-ttu-id="2dd3a-116">Во время отключения</span><span class="sxs-lookup"><span data-stu-id="2dd3a-116">During outage</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2dd3a-117">Звонки, подключенные к агенту</span><span class="sxs-lookup"><span data-stu-id="2dd3a-117">Calls connected to an agent</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="2dd3a-118">Обычные звонки остаются подключенными.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-118">Regular calls remain connected.</span></span></p></li>
<li><p><span data-ttu-id="2dd3a-119">Анонимные звонки будут разорваны.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-119">Anonymous calls are disconnected.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2dd3a-120">Звонки, которые пока не подключены к агенту</span><span class="sxs-lookup"><span data-stu-id="2dd3a-120">In progress calls not yet connected to an agent</span></span></p></td>
<td><p><span data-ttu-id="2dd3a-121">Звонки будут разорваны.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-121">Calls are disconnected.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2dd3a-122">Новые звонки</span><span class="sxs-lookup"><span data-stu-id="2dd3a-122">New calls</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="2dd3a-123">Звонки будут разорваны.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-123">Calls are disconnected.</span></span></p></li>
<li><p><span data-ttu-id="2dd3a-124">Если группы ответа импортированы, вызовы подключаются к пулу резервных копий, но агенты, расположенные в основном пуле, недостижимы.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-124">If response groups were imported, calls connect to backup pool, but agents homed in primary pool are unreachable.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2dd3a-125">Вызов агента от имени группы ответа</span><span class="sxs-lookup"><span data-stu-id="2dd3a-125">Agent calls on behalf of response group</span></span></p></td>
<td><p><span data-ttu-id="2dd3a-126">Функция отключена на этом этапе.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-126">Feature is disabled during this stage.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2dd3a-127">Вход агента и информация агента</span><span class="sxs-lookup"><span data-stu-id="2dd3a-127">Agent sign-in and agent information</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="2dd3a-128">Группы агентов, принадлежащие основному пулу, можно просматривать на консоли агента, но агенты не могут войти в систему.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-128">Agent groups owned by the primary pool can be viewed on agent console but agents cannot sign in.</span></span></p></li>
<li><p><span data-ttu-id="2dd3a-129">Группы агентов, владельцами которых является пул резервных копий, можно просмотреть на консоли агента, а агенты могут войти в нее.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-129">Agent groups owned by the backup pool can be viewed on agent console and agents can sign in.</span></span></p></li>
<li><p><span data-ttu-id="2dd3a-130">Импортированные группы агентов не отображаются на консоли агента.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-130">Imported agent groups are not displayed on agent console.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2dd3a-131">Настройка группы ответа</span><span class="sxs-lookup"><span data-stu-id="2dd3a-131">Response group configuration</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="2dd3a-132">Группы ответа, принадлежащие основному пулу, можно просмотреть в зависимости от доступности серверной базы данных основного пула, но не для ее изменения.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-132">Response groups owned by the primary pool can be viewed, depending on the availability of the primary pool’s back-end database, but cannot be modified.</span></span></p></li>
<li><p><span data-ttu-id="2dd3a-133">Группы ответа, принадлежащие пулу резервных копий, можно просмотреть и изменить.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-133">Response groups owned by the backup pool can be viewed and modified.</span></span></p></li>
<li><p><span data-ttu-id="2dd3a-134">Импортированные группы ответа нельзя просматривать с помощью панели управления Lync Server или средства настройки группы ответа, но их можно настроить в командлетах командной консоли Lync Server.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-134">Imported response groups cannot be viewed with Lync Server Control Panel or the Response Group Configuration Tool, but can be configured by using Lync Server Management Shell cmdlets.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="user-experience-during-failover"></a><span data-ttu-id="2dd3a-135">Взаимодействие с пользователем во время перехода на другой ресурс</span><span class="sxs-lookup"><span data-stu-id="2dd3a-135">User Experience During Failover</span></span>

<span data-ttu-id="2dd3a-136">Когда администратор выполняет отработку отказа для резервного пула, действия группы ответа обрабатываются во время и после перехода на другой ресурс, как описано в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-136">When an administrator invokes failover to a backup pool, response group activity is handled during and after the failover as described in the following table.</span></span> <span data-ttu-id="2dd3a-137">Первый столбец описывает тип действия, которое может происходить.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-137">The first column describes the type of activity that might be taking place.</span></span> <span data-ttu-id="2dd3a-138">Средний столбец показывает, как обрабатываются все действия в течение короткого времени, при переходе на резервный пул.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-138">The middle column describes how each activity is handled during the brief time that it takes to fail over to the backup pool.</span></span> <span data-ttu-id="2dd3a-139">В последнем столбце показано, как обрабатываются действия в течение длительного времени после завершения процесса отработки отказа и резервного пула для основного пула.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-139">The last column describes how the activity is handled for the duration, after the failover process is complete and the backup pool is standing in for the primary pool.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="2dd3a-140">Во время аварийного восстановления звонки работают по-разному в зависимости от того, были ли группы ответов основного пула импортированы в пул резервного копирования во время восстановления.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-140">During disaster recovery, calls behave differently depending on whether the primary pool response groups were imported to the backup pool during recovery.</span></span> <span data-ttu-id="2dd3a-141">В приведенной ниже таблице ссылки на импортированные группы ответов означают, что группы ответов основного пула были импортированы в пул резервных копий в режиме восстановления после сбоя.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-141">In the following table, references to imported response groups mean that primary pool response groups were imported to the backup pool during disaster recovery mode.</span></span>



</div>

### <a name="failover-is-initiated"></a><span data-ttu-id="2dd3a-142">Отработка отказа инициируется</span><span class="sxs-lookup"><span data-stu-id="2dd3a-142">Failover Is Initiated</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2dd3a-143">Тип звонка или действия пользователя</span><span class="sxs-lookup"><span data-stu-id="2dd3a-143">Type of call or user action</span></span></th>
<th><span data-ttu-id="2dd3a-144">При переходе на другой ресурс</span><span class="sxs-lookup"><span data-stu-id="2dd3a-144">During Failover</span></span></th>
<th><span data-ttu-id="2dd3a-145">После завершения отработки отказа</span><span class="sxs-lookup"><span data-stu-id="2dd3a-145">After Failover Completes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2dd3a-146">Звонки, подключенные к агенту</span><span class="sxs-lookup"><span data-stu-id="2dd3a-146">Calls connected to an agent</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="2dd3a-147">Обычные звонки остаются подключенными.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-147">Regular calls remain connected.</span></span></p></li>
<li><p><span data-ttu-id="2dd3a-148">Анонимные звонки будут разорваны.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-148">Anonymous calls are disconnected.</span></span></p></li>
</ul></td>
<td><ul>
<li><p><span data-ttu-id="2dd3a-149">Обычные звонки остаются подключенными.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-149">Regular calls remain connected.</span></span></p></li>
<li><p><span data-ttu-id="2dd3a-150">Для импортированных групп ответа анонимные звонки, достигнутые пулом резервных копий, остаются подключенными.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-150">For imported response groups, anonymous calls that have reached the backup pool remain connected.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2dd3a-151">Звонки, которые пока не подключены к агенту</span><span class="sxs-lookup"><span data-stu-id="2dd3a-151">In progress calls not yet connected to an agent</span></span></p></td>
<td><p><span data-ttu-id="2dd3a-152">Звонки будут разорваны.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-152">Calls are disconnected.</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="2dd3a-153">Если группы ответа не были импортированы, ни одно из них не находится в этом состоянии.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-153">If response groups were not imported, no calls are in this status.</span></span></p></li>
<li><p><span data-ttu-id="2dd3a-154">Для импортированных групп ответа звонки, достигнутые в пуле резервных копий, остаются подключенными.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-154">For imported response groups, calls that have reached the backup pool remain connected.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2dd3a-155">Новые звонки</span><span class="sxs-lookup"><span data-stu-id="2dd3a-155">New calls</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="2dd3a-156">Звонки будут разорваны.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-156">Calls are disconnected.</span></span></p></li>
<li><p><span data-ttu-id="2dd3a-157">Для импортированных групп ответа звонки подключаются к резервному пулу, но агенты, расположенные в основном пуле, недостижимы.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-157">For imported response groups, calls connect to the backup pool, but agents homed in the primary pool are unreachable.</span></span></p></li>
</ul></td>
<td><ul>
<li><p><span data-ttu-id="2dd3a-158">Если группы ответа не были импортированы, звонки будут разорваны.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-158">If response groups were not imported, calls are disconnected.</span></span></p></li>
<li><p><span data-ttu-id="2dd3a-159">Для импортированных групп ответа вызовы подключаются к резервному пулу.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-159">For imported response groups, calls connect to the backup pool.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2dd3a-160">Вызов агента от имени группы ответа</span><span class="sxs-lookup"><span data-stu-id="2dd3a-160">Agent calls on behalf of response group</span></span></p></td>
<td><p><span data-ttu-id="2dd3a-161">Функция отключена на этом этапе</span><span class="sxs-lookup"><span data-stu-id="2dd3a-161">Feature is disabled during this stage</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="2dd3a-162">Если группы ответа не были импортированы, вызов завершается сбоем.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-162">If response groups were not imported, calls fail.</span></span></p></li>
<li><p><span data-ttu-id="2dd3a-163">Для импортированных групп ответа звонки выполняются успешно.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-163">For imported response groups, calls succeed.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2dd3a-164">Вход агента и информация агента</span><span class="sxs-lookup"><span data-stu-id="2dd3a-164">Agent sign-in and agent information</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="2dd3a-165">Группы агентов, принадлежащие основному пулу, можно просматривать на консоли агента, но агенты не могут войти в систему.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-165">Agent groups owned by the primary pool can be viewed on agent console but agents cannot sign in.</span></span></p></li>
<li><p><span data-ttu-id="2dd3a-166">Группы агентов, владельцами которых является пул резервных копий, можно просмотреть на консоли агента, а агенты могут войти в нее.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-166">Agent groups owned by the backup pool can be viewed on agent console and agents can sign in.</span></span></p></li>
<li><p><span data-ttu-id="2dd3a-167">Импортированные группы агентов отображаются на консоли агента, и агенты могут входить в систему.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-167">Imported agent groups are displayed on agent console and agents can sign in.</span></span></p></li>
</ul></td>
<td><ul>
<li><p><span data-ttu-id="2dd3a-168">Группы агентов, принадлежащие основному пулу, можно просматривать на консоли агента, но агенты не могут войти в систему.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-168">Agent groups owned by the primary pool can be viewed on agent console but agents cannot sign in.</span></span></p></li>
<li><p><span data-ttu-id="2dd3a-169">Группы агентов, владельцами которых является пул резервных копий, можно просмотреть на консоли агента, а агенты могут войти в нее.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-169">Agent groups owned by the backup pool can be viewed on agent console and agents can sign in.</span></span></p></li>
<li><p><span data-ttu-id="2dd3a-170">Импортированные группы агентов отображаются на консоли агента, и агенты могут входить в систему.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-170">Imported agent groups are displayed on agent console and agents can sign in.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2dd3a-171">Настройка группы ответа</span><span class="sxs-lookup"><span data-stu-id="2dd3a-171">Response group configuration</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="2dd3a-172">Группы ответа, принадлежащие основному пулу, можно просмотреть в зависимости от доступности серверной базы данных основного пула, но не для ее изменения.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-172">Response groups owned by the primary pool can be viewed, depending on the availability of the primary pool’s back-end database, but cannot be modified.</span></span></p></li>
<li><p><span data-ttu-id="2dd3a-173">Группы ответа, принадлежащие пулу резервных копий, можно просмотреть и изменить.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-173">Response groups owned by the backup pool can be viewed and modified.</span></span></p></li>
<li><p><span data-ttu-id="2dd3a-174">Импортированные группы ответа нельзя просматривать с помощью панели управления Lync Server или средства настройки группы ответа, но их можно настроить в командлетах командной консоли Lync Server.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-174">Imported response groups cannot be viewed with Lync Server Control Panel or the Response Group Configuration Tool, but can be configured by using Lync Server Management Shell cmdlets.</span></span></p></li>
</ul></td>
<td><ul>
<li><p><span data-ttu-id="2dd3a-175">Группы ответа, принадлежащие основному пулу, можно просмотреть в зависимости от доступности базы данных, но не могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-175">Response groups owned by the primary pool can be viewed, depending on the availability of the back end database, but cannot be modified.</span></span></p></li>
<li><p><span data-ttu-id="2dd3a-176">Группы ответа, принадлежащие пулу резервных копий, можно просмотреть и изменить.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-176">Response groups owned by the backup pool can be viewed and modified.</span></span></p></li>
<li><p><span data-ttu-id="2dd3a-177">Импортированные группы ответа нельзя просматривать с помощью панели управления Lync Server или средства настройки группы ответа, но их можно настроить в командлетах командной консоли Lync Server.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-177">Imported response groups cannot be viewed with Lync Server Control Panel or the Response Group Configuration Tool, but can be configured by using Lync Server Management Shell cmdlets.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="user-experience-during-failback"></a><span data-ttu-id="2dd3a-178">Взаимодействие с пользователем при восстановлении из восстановления</span><span class="sxs-lookup"><span data-stu-id="2dd3a-178">User Experience During Failback</span></span>

<span data-ttu-id="2dd3a-179">Когда администратор выполняет восстановление по восстановлению для основного пула, действия группы ответа обрабатываются во время и после восстановления размещения, как описано в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-179">When an administrator invokes failback to the primary pool, response group activity is handled during and after the failback as described in the following table.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="2dd3a-180">Во время аварийного восстановления звонки работают по-разному в зависимости от того, были ли группы ответов основного пула импортированы в пул резервного копирования во время восстановления.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-180">During disaster recovery, calls behave differently depending on whether the primary pool response groups were imported to the backup pool during recovery.</span></span> <span data-ttu-id="2dd3a-181">В приведенной ниже таблице ссылки на импортированные группы ответов означают, что группы ответов основного пула были импортированы в пул резервных копий в режиме восстановления после сбоя.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-181">In the following table, references to imported response groups mean that primary pool response groups were imported to the backup pool during disaster recovery mode.</span></span>



</div>

### <a name="call-handling-in-failback"></a><span data-ttu-id="2dd3a-182">Обработка звонков в отказовозвращение</span><span class="sxs-lookup"><span data-stu-id="2dd3a-182">Call Handling in Failback</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2dd3a-183">Тип звонка или действия пользователя</span><span class="sxs-lookup"><span data-stu-id="2dd3a-183">Type of call or user action</span></span></th>
<th><span data-ttu-id="2dd3a-184">Во время восстановления размещения</span><span class="sxs-lookup"><span data-stu-id="2dd3a-184">During Failback</span></span></th>
<th><span data-ttu-id="2dd3a-185">После завершения восстановления</span><span class="sxs-lookup"><span data-stu-id="2dd3a-185">After Failback Completes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2dd3a-186">Звонки, подключенные к агенту</span><span class="sxs-lookup"><span data-stu-id="2dd3a-186">Calls connected to an agent</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="2dd3a-187">Обычные звонки остаются подключенными.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-187">Regular calls remain connected.</span></span></p></li>
<li><p><span data-ttu-id="2dd3a-188">Если группы ответа не были импортированы, анонимные звонки не будут находиться в этом состоянии.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-188">If response groups were not imported, no anonymous calls are in this status.</span></span></p></li>
<li><p><span data-ttu-id="2dd3a-189">Для импортированных групп ответа анонимные звонки остаются подключенными.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-189">For imported response groups, anonymous calls remain connected.</span></span></p></li>
</ul></td>
<td><ul>
<li><p><span data-ttu-id="2dd3a-190">Обычные звонки остаются подключенными.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-190">Regular calls remain connected.</span></span></p></li>
<li><p><span data-ttu-id="2dd3a-191">Если группы ответа не были импортированы, анонимные звонки не будут находиться в этом состоянии.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-191">If response groups were not imported, no anonymous calls are in this status.</span></span></p></li>
<li><p><span data-ttu-id="2dd3a-192">Для импортированных групп ответа анонимные звонки остаются подключенными.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-192">For imported response groups, anonymous calls remain connected.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2dd3a-193">Звонки, которые пока не подключены к агенту</span><span class="sxs-lookup"><span data-stu-id="2dd3a-193">In progress calls not yet connected to an agent</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="2dd3a-194">Если группы ответа не были импортированы, ни одно из них не находится в этом состоянии.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-194">If response groups were not imported, no calls are in this status.</span></span></p></li>
<li><p><span data-ttu-id="2dd3a-195">Для импортированных групп ответа звонки будут разорваны.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-195">For imported response groups, calls will be disconnected.</span></span></p></li>
</ul></td>
<td><ul>
<li><p><span data-ttu-id="2dd3a-196">Если группы ответа не были импортированы, ни одно из них не находится в этом состоянии.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-196">If response groups were not imported, no calls are in this status.</span></span></p></li>
<li><p><span data-ttu-id="2dd3a-197">Для импортированных групп ответа звонки будут разорваны.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-197">For imported response groups, calls will be disconnected.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2dd3a-198">Новые звонки</span><span class="sxs-lookup"><span data-stu-id="2dd3a-198">New calls</span></span></p></td>
<td><p><span data-ttu-id="2dd3a-199">Вызовы подключаются к основному пулу, но агенты, расположенные в основном пуле, недостижимы.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-199">Calls connect to the primary pool, but agents homed in the primary pool are unreachable.</span></span></p></td>
<td><p><span data-ttu-id="2dd3a-200">Звонки подключаются к основному пулу.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-200">Calls connect to the primary pool.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2dd3a-201">Вызов агента от имени группы ответа</span><span class="sxs-lookup"><span data-stu-id="2dd3a-201">Agent calls on behalf of response group</span></span></p></td>
<td><p><span data-ttu-id="2dd3a-202">Функция отключена на этом этапе.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-202">Feature is disabled during this stage.</span></span></p></td>
<td><p><span data-ttu-id="2dd3a-203">Успешные звонки.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-203">Calls succeed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2dd3a-204">Вход агента и информация агента</span><span class="sxs-lookup"><span data-stu-id="2dd3a-204">Agent sign-in and agent information</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="2dd3a-205">Группы агентов, принадлежащие основному пулу, можно просматривать на консоли агента, но агенты не могут войти в систему.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-205">Agent groups owned by the primary pool can be viewed on agent console but agents cannot sign in.</span></span></p></li>
<li><p><span data-ttu-id="2dd3a-206">Группы агентов, владельцами которых является пул резервных копий, можно просмотреть на консоли агента, а агенты могут войти в нее.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-206">Agent groups owned by the backup pool can be viewed on agent console and agents can sign in.</span></span></p></li>
<li><p><span data-ttu-id="2dd3a-207">Импортированные группы агентов отображаются на консоли агента, и агенты могут входить в систему.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-207">Imported agent groups are displayed on agent console and agents can sign in.</span></span></p></li>
</ul></td>
<td><ul>
<li><p><span data-ttu-id="2dd3a-208">Группы агентов, владельцами которых является основной пул, можно просматривать на консоли агента, а агенты — на входе.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-208">Agent groups owned by the primary pool can be viewed on agent console and agents can sign in.</span></span></p></li>
<li><p><span data-ttu-id="2dd3a-209">Группы агентов, владельцами которых является пул резервных копий, можно просмотреть на консоли агента, а агенты могут войти в нее.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-209">Agent groups owned by the backup pool can be viewed on agent console and agents can sign in.</span></span></p></li>
<li><p><span data-ttu-id="2dd3a-210">Импортированные группы агентов не отображаются на консоли агента.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-210">Imported agent groups are not displayed on agent console.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2dd3a-211">Настройка группы ответа</span><span class="sxs-lookup"><span data-stu-id="2dd3a-211">Response group configuration</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="2dd3a-212">Группы ответа, принадлежащие основному пулу, можно просмотреть в зависимости от доступности серверной базы данных основного пула, но не для ее изменения.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-212">Response groups owned by the primary pool can be viewed, depending on the availability of the primary pool’s back-end database, but cannot be modified.</span></span></p></li>
<li><p><span data-ttu-id="2dd3a-213">Группы ответа, принадлежащие пулу резервных копий, можно просмотреть и изменить.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-213">Response groups owned by the backup pool can be viewed and modified.</span></span></p></li>
<li><p><span data-ttu-id="2dd3a-214">Импортированные группы ответа нельзя просматривать с помощью панели управления Lync Server или средства настройки группы ответа, но их можно настроить в командлетах командной консоли Lync Server.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-214">Imported response groups cannot be viewed with Lync Server Control Panel or the Response Group Configuration Tool, but can be configured by using Lync Server Management Shell cmdlets.</span></span></p></li>
</ul></td>
<td><ul>
<li><p><span data-ttu-id="2dd3a-215">Группы ответа, принадлежащие основным пулам, можно просмотреть и изменить.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-215">Response groups owned by the primary pool can be viewed and modified.</span></span></p></li>
<li><p><span data-ttu-id="2dd3a-216">Группы ответа, принадлежащие пулу резервных копий, можно просмотреть и изменить.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-216">Response groups owned by the backup pool can be viewed and modified.</span></span></p></li>
<li><p><span data-ttu-id="2dd3a-217">Импортированные группы ответа нельзя просматривать с помощью панели управления Lync Server или средства настройки группы ответа, но их можно настроить в командлетах командной консоли Lync Server.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-217">Imported response groups cannot be viewed with Lync Server Control Panel or the Response Group Configuration Tool, but can be configured by using Lync Server Management Shell cmdlets.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table><span data-ttu-id="2dd3a-218">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2dd3a-218">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

