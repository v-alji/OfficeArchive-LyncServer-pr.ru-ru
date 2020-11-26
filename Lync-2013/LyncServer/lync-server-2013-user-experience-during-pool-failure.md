---
title: Пользовательский интерфейс Lync Server 2013 в случае сбоя пула
description: Пользовательский интерфейс Lync Server 2013 в случае сбоя пула.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: User experience during pool failure
ms:assetid: b224b0d0-87e3-4cac-ae87-f45f54fabb49
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205184(v=OCS.15)
ms:contentKeyID: 48185166
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a0483a01b643d8195e7f8f6259c11ab6fc3561f2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440782"
---
# <a name="user-experience-during-pool-failure-in-lync-server-2013"></a><span data-ttu-id="bb671-103">Взаимодействие с пользователем во время сбоя пула в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bb671-103">User experience during pool failure in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bb671-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bb671-104">

<span> </span></span></span>

<span data-ttu-id="bb671-105">_**Тема последнего изменения:** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="bb671-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="bb671-106">Если вы перейдете из-за сбоя пула, все пользователи этого пула будут вынуждены выйти из нее, а затем войти в пул резервной копии.</span><span class="sxs-lookup"><span data-stu-id="bb671-106">If a pool is failed over, all users of the affected pool are forced to sign out and then sign into the backup pool.</span></span> <span data-ttu-id="bb671-107">В течение непродолжительного периода времени пользователи, вошедшие в резервный пул, могут находиться в режиме устойчивости.</span><span class="sxs-lookup"><span data-stu-id="bb671-107">For a brief period users who sign into the backup pool may be in resiliency mode.</span></span> <span data-ttu-id="bb671-108">В режиме устойчивости пользователи не могут выполнять задачи, которые приводили к сохранению изменений на сервере Lync Server, например добавление контакта.</span><span class="sxs-lookup"><span data-stu-id="bb671-108">In Resiliency mode, users are unable to perform tasks that would cause a persistent change on Lync Server, such as adding a contact.</span></span> <span data-ttu-id="bb671-109">По завершении отработки отказа возможно полное обслуживание всех пользователей из резервного пула.</span><span class="sxs-lookup"><span data-stu-id="bb671-109">After the failover is complete, all users can get all services from the backup pool.</span></span>

<span data-ttu-id="bb671-110">Любые сеансы, которые пользователь может вызвать, когда происходит сбой пула, и пользователь должен повторно установить эти сеансы после перемещения, чтобы продолжить.</span><span class="sxs-lookup"><span data-stu-id="bb671-110">Any sessions a user has when the pool fails are disrupted, and the user must re-establish those sessions after failover to continue.</span></span>

<span data-ttu-id="bb671-111">При отработке отказа или переключении на основной ресурс пользователи не перемещаются.</span><span class="sxs-lookup"><span data-stu-id="bb671-111">Users are not rehomed during failover or failback.</span></span> <span data-ttu-id="bb671-112">Пользователи, размещенные в сбойном пуле, временно обслуживаются из резервного пула.</span><span class="sxs-lookup"><span data-stu-id="bb671-112">Users who are homed on a pool that fails will be temporarily serviced by the backup pool.</span></span> <span data-ttu-id="bb671-113">После восстановления пула домашних компьютеров администратор может не отменять эти пользователи на обслуживание первоначального пула домашних компьютеров.</span><span class="sxs-lookup"><span data-stu-id="bb671-113">When the home pool is restored, the administrator can fail back these users to be serviced by their original home pool.</span></span>

<span data-ttu-id="bb671-114">Обратите внимание, что в Lync 2013 база данных сервера сведений о расположениях не реплицируется в пул резервных копий.</span><span class="sxs-lookup"><span data-stu-id="bb671-114">Note in Lync 2013, the Location Information Server database is not replicated to the backup pool.</span></span> <span data-ttu-id="bb671-115">Администратору рекомендуется регулярно создавать резервные копии базы данных сервера информирования о местонахождении и после отработки отказа восстанавливать базу данных этого сервера из последней резервную копии в резервном пуле.</span><span class="sxs-lookup"><span data-stu-id="bb671-115">For best practice, the administrator should regularly back up the LIS database and use the latest backup copy to restore the LIS database in the backup pool after the failover.</span></span>

<div>

## <a name="user-experience-during-failover"></a><span data-ttu-id="bb671-116">Взаимодействие с пользователем во время перехода на другой ресурс</span><span class="sxs-lookup"><span data-stu-id="bb671-116">User Experience During Failover</span></span>

<span data-ttu-id="bb671-117">Если пользователь в пуле не проходит, пользователь выходит из него. Любые одноранговые сеансы, в которых участвует пользователь, прекращаются, как и конференции, упорядоченные этим пользователем.</span><span class="sxs-lookup"><span data-stu-id="bb671-117">When a user is in a pool that fails, the user is logged out. Any peer-to-peer session the user was participating in is terminated, as are conferences organized by that user.</span></span> <span data-ttu-id="bb671-118">Пользователь может войти снова только после срабатывания таймера регистрации устойчивости или запуска процедуры отработки отказа администратором в зависимости от того, что произойдет раньше.</span><span class="sxs-lookup"><span data-stu-id="bb671-118">The user cannot log back in until either the registrar resiliency timer expires or the administrator initiates failover procedures, whichever comes first.</span></span> <span data-ttu-id="bb671-119">Следующий вход пользователя осуществляется в резервный пул.</span><span class="sxs-lookup"><span data-stu-id="bb671-119">When the user logs back in, they will log in to the backup pool.</span></span> <span data-ttu-id="bb671-120">Пользователь, вошедший во время отработки отказа или ранее, до ее завершения находится в режиме устойчивости.</span><span class="sxs-lookup"><span data-stu-id="bb671-120">If they log in before the failover has completed, they will be in Resiliency mode until failover is complete.</span></span> <span data-ttu-id="bb671-121">Только после этого пользователь сможет устанавливать новые сеансы или повторно устанавливать предыдущие сеансы.</span><span class="sxs-lookup"><span data-stu-id="bb671-121">Only then the user is able to establish new sessions or re-establish previous sessions.</span></span>

</div>

<div>

## <a name="user-experience-during-failback"></a><span data-ttu-id="bb671-122">Взаимодействие с пользователем при восстановлении из восстановления</span><span class="sxs-lookup"><span data-stu-id="bb671-122">User Experience During Failback</span></span>

<span data-ttu-id="bb671-123">Переключение на основной ресурс может произойти во время сеанса работы пользователя в резервном пуле; во время переключения на основной ресурс этот сеанс продолжается.</span><span class="sxs-lookup"><span data-stu-id="bb671-123">Pool failback can happen while an affected user is logged on to the backup pool, and the user remains logged on and working during the failback.</span></span> <span data-ttu-id="bb671-124">Обратите внимание, что процесс восстановления после сбоя занимает несколько минут.</span><span class="sxs-lookup"><span data-stu-id="bb671-124">Note that the failback process takes several minute to complete.</span></span>  <span data-ttu-id="bb671-125">Следует исходить из длительности 60 минут для пула, в котором работает 20 000 пользователей.</span><span class="sxs-lookup"><span data-stu-id="bb671-125">For reference, it is expected to take up to 60 minutes for a pool of 20,000 users.</span></span>

<span data-ttu-id="bb671-126">В приведенных ниже таблицах приведены дополнительные сведения о том, как повлияет пользователь, работающий с клиентом Lync 2013 или Microsoft Lync 2010, в процессе и после восстановления, а также о том, как пользователи в других пулах видят и работают с пользователем в пуле, который не прошел обратно.</span><span class="sxs-lookup"><span data-stu-id="bb671-126">The following tables show more details about how a user with a Lync 2013 client or a Microsoft Lync 2010 client is affected during and after failback, and also how users in other pools see and interact with a user in a pool who is being failed back.</span></span> <span data-ttu-id="bb671-127">Пользователи с помощью Microsoft Office Communicator 2007 R2 не могут войти в систему, пока не будет полностью восстановлен пул переднего плана.)</span><span class="sxs-lookup"><span data-stu-id="bb671-127">Users with Microsoft Office Communicator 2007 R2 clients cannot sign in until the Front End pool is completely failed back.)</span></span>

<span data-ttu-id="bb671-128">Термином *затронутый пользователь* обозначается любой пользователь, вышедший из исходного пула в ходе отработки отказа и обслуживаемый из резервного пула.</span><span class="sxs-lookup"><span data-stu-id="bb671-128">The term *affected user* refers to any user who was failed over from the home pool and is being serviced by the backup pool.</span></span> <span data-ttu-id="bb671-129">По определению, пользователи, первоначально размещенные в пуле резервных копий, не подвержены уязвимости.</span><span class="sxs-lookup"><span data-stu-id="bb671-129">By definition, any user originally homed on the backup pool is not an affected user.</span></span>

### <a name="user-experience-for-an-affected-user-in-a-pool-in-failback"></a><span data-ttu-id="bb671-130">Взаимодействие с затронутым пользователем пула в ходе восстановления размещения</span><span class="sxs-lookup"><span data-stu-id="bb671-130">User Experience for an Affected User in a Pool in Failback</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bb671-131">Состояние пользователя или задача</span><span class="sxs-lookup"><span data-stu-id="bb671-131">User state or task</span></span></th>
<th><span data-ttu-id="bb671-132">Во время восстановления размещения</span><span class="sxs-lookup"><span data-stu-id="bb671-132">During failback</span></span></th>
<th><span data-ttu-id="bb671-133">После завершения восстановления размещения</span><span class="sxs-lookup"><span data-stu-id="bb671-133">After failback completion</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bb671-134">Состояние пользователя, который уже выполнил вход</span><span class="sxs-lookup"><span data-stu-id="bb671-134">User state of user already logged in</span></span></p></td>
<td><p><span data-ttu-id="bb671-p108">Пользователь остается подключенным к резервному пулу. В определенный момент времени пользователь выйдет из системы и затем снова выполнит вход на исходном пуле в режиме устойчивости.</span><span class="sxs-lookup"><span data-stu-id="bb671-p108">User stays signed in and connected to backup pool. At some point user will be signed out and sign back in to the original home pool, in Resiliency mode.</span></span></p></td>
<td><p><span data-ttu-id="bb671-137">Состояние входа пользователя не изменяется, и он переходит в обычный режим.</span><span class="sxs-lookup"><span data-stu-id="bb671-137">User remains signed in and goes into regular mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb671-138">Вход нового пользователя</span><span class="sxs-lookup"><span data-stu-id="bb671-138">New user logging in</span></span></p></td>
<td><p><span data-ttu-id="bb671-139">Пользователь может выполнить вход в пул в режиме устойчивости.</span><span class="sxs-lookup"><span data-stu-id="bb671-139">User can sign in to the home pool in Resiliency mode.</span></span></p></td>
<td><p><span data-ttu-id="bb671-140">Пользователь может выполнить вход в исходный пул в обычном режиме.</span><span class="sxs-lookup"><span data-stu-id="bb671-140">User can sign in to the original home pool in regular mode.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb671-141">Текущие конференции, созданные затронутым пользователем</span><span class="sxs-lookup"><span data-stu-id="bb671-141">Ongoing conferences organized by affected user</span></span></p></td>
<td><p><span data-ttu-id="bb671-p109">Все модальности конференции приостанавливаются. Кнопка "Повторно присоединиться" будет отображаться, но ни один пользователь не сможет присоединиться повторно, если затронутый пользователь находится в режиме устойчивости.</span><span class="sxs-lookup"><span data-stu-id="bb671-p109">All modalities of conference are terminated. Rejoin button will appear, but no users can rejoin while the affected user is in Resiliency mode.</span></span></p></td>
<td><p><span data-ttu-id="bb671-p110">Все модальности работают. Для повторного присоединения к конференции участникам требуется нажать кнопку "Повторно присоединиться".</span><span class="sxs-lookup"><span data-stu-id="bb671-p110">All modalities now work. Every participant needs to click to rejoin the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb671-146">Текущие конференции, созданные незатронутым пользователем</span><span class="sxs-lookup"><span data-stu-id="bb671-146">Ongoing conferences organized by unaffected user</span></span></p></td>
<td><p><span data-ttu-id="bb671-p111">Конференция будет продолжена, и затронутый пользователь останется подключенным к конференции. Возможности затронутого пользователя в режиме устойчивости ограничены.</span><span class="sxs-lookup"><span data-stu-id="bb671-p111">Conference continues and affected user can stay in the conference. Affected user is restricted to what he/she can do in Resiliency mode.</span></span></p></td>
<td><p><span data-ttu-id="bb671-149">Конференция будет продолжена, затронутый пользователь останется подключенным к конференции, а все модальности начнут работу после выхода из режима устойчивости.</span><span class="sxs-lookup"><span data-stu-id="bb671-149">Conference continues, and affected user can stay in the conference and all modalities work after user exits Resiliency mode.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb671-150">Создание расписания и изменение запланированных собраний, создание запланированных конференций</span><span class="sxs-lookup"><span data-stu-id="bb671-150">Scheduling or modifying scheduled meetings, creating ad-hoc conferences</span></span></p></td>
<td><p><span data-ttu-id="bb671-151">Невозможно в режиме устойчивости.</span><span class="sxs-lookup"><span data-stu-id="bb671-151">Not possible while user is in Resiliency mode.</span></span></p></td>
<td><p><span data-ttu-id="bb671-152">Доступно для всех модальностей.</span><span class="sxs-lookup"><span data-stu-id="bb671-152">Available for all modalities.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb671-153">Сведения о присутствии, отображаемые остальным пользователям того же пула</span><span class="sxs-lookup"><span data-stu-id="bb671-153">Presence as seen by other users in the same pool</span></span></p></td>
<td><p><span data-ttu-id="bb671-154">Сведения о присутствии отсутствуют, если пользователь выполнил вход в резервный пул в режиме устойчивости.</span><span class="sxs-lookup"><span data-stu-id="bb671-154">Presence unknown while user is signed into backup pool during Resiliency mode.</span></span></p></td>
<td><p><span data-ttu-id="bb671-155">Отображается последнее состояние присутствия, заданное пользователем, при этом изменения состояния присутствия не отображаются.</span><span class="sxs-lookup"><span data-stu-id="bb671-155">Shows the last presence state set by the user, and presence changes will now be reflected.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb671-156">Доступность списка контактов и службы адресной книги</span><span class="sxs-lookup"><span data-stu-id="bb671-156">Contacts list and Address Book Service availability</span></span></p></td>
<td><p><span data-ttu-id="bb671-157">Недоступно</span><span class="sxs-lookup"><span data-stu-id="bb671-157">Not available</span></span></p></td>
<td><p><span data-ttu-id="bb671-158">Доступно</span><span class="sxs-lookup"><span data-stu-id="bb671-158">Available</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb671-159">Все одноранговые сеансы и модальности</span><span class="sxs-lookup"><span data-stu-id="bb671-159">All peer-to-peer sessions and modalities</span></span></p></td>
<td><p><span data-ttu-id="bb671-160">Доступно</span><span class="sxs-lookup"><span data-stu-id="bb671-160">Available</span></span></p></td>
<td><p><span data-ttu-id="bb671-161">Доступно</span><span class="sxs-lookup"><span data-stu-id="bb671-161">Available</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="user-experience-for-a-user-homed-in-an-unaffected-pool-during-failback-of-another-pool"></a><span data-ttu-id="bb671-162">Взаимодействие с пользователями, размещенными в незатронутом пуле, в ходе восстановления размещения другого пула</span><span class="sxs-lookup"><span data-stu-id="bb671-162">User Experience for a User Homed in an Unaffected Pool During Failback of Another Pool</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bb671-163">Задача пользователя</span><span class="sxs-lookup"><span data-stu-id="bb671-163">User task</span></span></th>
<th><span data-ttu-id="bb671-164">Во время восстановления размещения</span><span class="sxs-lookup"><span data-stu-id="bb671-164">During failback</span></span></th>
<th><span data-ttu-id="bb671-165">После завершения восстановления размещения</span><span class="sxs-lookup"><span data-stu-id="bb671-165">After failback completion</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bb671-166">Просмотр сведений о присутствии затронутого пользователя</span><span class="sxs-lookup"><span data-stu-id="bb671-166">Viewing presence of affected user</span></span></p></td>
<td><p><span data-ttu-id="bb671-167">Отображается последнее состояние присутствия, заданное затронутым пользователем.</span><span class="sxs-lookup"><span data-stu-id="bb671-167">Shows the last presence state set by the affected user.</span></span></p></td>
<td><p><span data-ttu-id="bb671-p112">Незатронутые пользователи могут просматривать обновленные сведения о присутствии затронутых пользователей.</span><span class="sxs-lookup"><span data-stu-id="bb671-p112">Working. Unaffected users see updates made by affected users.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb671-170">Текущие конференции, созданные затронутым пользователем</span><span class="sxs-lookup"><span data-stu-id="bb671-170">Ongoing conferences organized by affected user</span></span></p></td>
<td><p><span data-ttu-id="bb671-171">Все модальности конференции приостанавливаются.</span><span class="sxs-lookup"><span data-stu-id="bb671-171">All modalities of conference are terminated.</span></span></p></td>
<td><p><span data-ttu-id="bb671-p113">Все модальности работают. Для повторного присоединения к конференции участникам требуется нажать кнопку "Повторно присоединиться".</span><span class="sxs-lookup"><span data-stu-id="bb671-p113">All modalities now work. Every participant needs to click to rejoin the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb671-174">Текущие конференции, созданные незатронутым пользователем</span><span class="sxs-lookup"><span data-stu-id="bb671-174">Ongoing conferences organized by unaffected user</span></span></p></td>
<td><p><span data-ttu-id="bb671-175">Конференция будет продолжена, затронутый пользователь может остаться в конференции, и все модальности будут работать.</span><span class="sxs-lookup"><span data-stu-id="bb671-175">Conference continues, and affected user can stay in the conference and all modalities work.</span></span></p></td>
<td><p><span data-ttu-id="bb671-176">Конференция будет продолжена, затронутый пользователь может остаться в конференции, и все модальности будут работать.</span><span class="sxs-lookup"><span data-stu-id="bb671-176">Conference continues, and affected user can stay in the conference and all modalities work.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb671-177">Все одноранговые сеансы и модальности</span><span class="sxs-lookup"><span data-stu-id="bb671-177">All peer-to-peer sessions and modalities</span></span></p></td>
<td><p><span data-ttu-id="bb671-178">Доступно</span><span class="sxs-lookup"><span data-stu-id="bb671-178">Available</span></span></p></td>
<td><p><span data-ttu-id="bb671-179">Доступно</span><span class="sxs-lookup"><span data-stu-id="bb671-179">Available</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="bb671-180">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bb671-180">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

