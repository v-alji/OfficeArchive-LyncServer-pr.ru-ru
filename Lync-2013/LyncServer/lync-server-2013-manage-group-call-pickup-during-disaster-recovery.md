---
title: 'Lync Server 2013: Управление расведением группового звонка во время аварийного восстановления'
description: 'Lync Server 2013: Управление расведением группового звонка во время аварийного восстановления.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Manage Group Call Pickup during disaster recovery
ms:assetid: 2d32f19f-c649-4a72-a4fb-edd338e3a7cc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945618(v=OCS.15)
ms:contentKeyID: 51541455
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 04d85bc83cfe35571c2b0f47f707c9dcd8037d80
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426106"
---
# <a name="manage-group-call-pickup-during-disaster-recovery-in-lync-server-2013"></a><span data-ttu-id="e8e4f-103">Управление расведением группового звонка во время восстановления после аварии в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e8e4f-103">Manage Group Call Pickup during disaster recovery in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e8e4f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e8e4f-104">

<span> </span></span></span>

<span data-ttu-id="e8e4f-105">_**Тема последнего изменения:** 2013-01-30_</span><span class="sxs-lookup"><span data-stu-id="e8e4f-105">_**Topic Last Modified:** 2013-01-30_</span></span>

<span data-ttu-id="e8e4f-106">Когда пул переднего плана становится недоступен из-за незапланированного инцидента, служба переключается на резервный пул.</span><span class="sxs-lookup"><span data-stu-id="e8e4f-106">When a Front End pool becomes unavailable due an unplanned incident, service is failed over to the backup pool.</span></span> <span data-ttu-id="e8e4f-107">При переходе на другой ресурс в пул резервной копии пользователи перенаправляются в пул резервных копий и в режиме устойчивости.</span><span class="sxs-lookup"><span data-stu-id="e8e4f-107">During failover to the backup pool, users are redirected to the backup pool and are in resiliency mode.</span></span> <span data-ttu-id="e8e4f-108">В режиме устойчивости пользователи не могут принимать звонки других пользователей или звонить другим пользователям.</span><span class="sxs-lookup"><span data-stu-id="e8e4f-108">While in resiliency mode, users cannot pick up other users' calls or have their calls picked up by other users.</span></span> <span data-ttu-id="e8e4f-109">После завершения перехода на другой ресурс пользователи могут снова использовать функцию отправки групп.</span><span class="sxs-lookup"><span data-stu-id="e8e4f-109">When failover is complete, users can again use Group Call Pickup as usual.</span></span>

<span data-ttu-id="e8e4f-110">При восстановлении из основного пула пользователи перенаправляются в основной пул и снова находятся в режиме устойчивости.</span><span class="sxs-lookup"><span data-stu-id="e8e4f-110">During failback to the primary pool, users are redirected to the primary pool and are again in resiliency mode.</span></span> <span data-ttu-id="e8e4f-111">Функция отправки группового звонка недоступна, пока пользователи не выходили из режима устойчивости.</span><span class="sxs-lookup"><span data-stu-id="e8e4f-111">Group Call Pickup functionality is not available until the users are out of resiliency mode.</span></span>

<span data-ttu-id="e8e4f-112">В этом разделе рассматриваются вопросы, касающиеся отправки группового звонка во время аварийного восстановления, а также описание взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="e8e4f-112">This section discusses some considerations for Group Call Pickup during disaster recovery and also describes the user experience.</span></span>

<div>

## <a name="considerations-for-group-call-pickup-during-disaster-recovery"></a><span data-ttu-id="e8e4f-113">Рекомендации по выбору группового звонка во время аварийного восстановления</span><span class="sxs-lookup"><span data-stu-id="e8e4f-113">Considerations for Group Call Pickup During Disaster Recovery</span></span>

<span data-ttu-id="e8e4f-114">При аварийном восстановлении пользователи, которые были перенаправлены в резервный пул в рамках процесса перемещения, используют приложение для остановки звонков в пуле резервных копий для номеров групп для отправки звонков.</span><span class="sxs-lookup"><span data-stu-id="e8e4f-114">During disaster recovery, users who have been redirected to the backup pool as part of the failover process use the Call Park application running in the backup pool for the call pickup group numbers.</span></span> <span data-ttu-id="e8e4f-115">Следовательно, для поддержки отправки группового звонка во время аварийного восстановления необходимо, чтобы приложение парковки на использование было развернуто и включено как в основном пуле, так и в пуле резервных копий.</span><span class="sxs-lookup"><span data-stu-id="e8e4f-115">Therefore, support for Group Call Pickup during disaster recovery requires the Call Park application to be deployed and enabled in both the primary pool and the backup pool.</span></span>

<span data-ttu-id="e8e4f-116">Диапазоны номеров раскладки для групповых звонков в таблице "приостановить Звонок" необходимо перенаправлять в пул резервных копий после завершения процесса перемещения в пул резервной копии.</span><span class="sxs-lookup"><span data-stu-id="e8e4f-116">The Group Call Pickup number ranges in the call park orbit table must be redirected to the backup pool after the failover process to the backup pool is complete.</span></span> <span data-ttu-id="e8e4f-117">После завершения процесса восстановления размещения для основного пула диапазоны номеров необходимо перенаправлять обратно в основной пул.</span><span class="sxs-lookup"><span data-stu-id="e8e4f-117">The number ranges must be redirected back to the primary pool after the failback process to the primary pool is complete.</span></span> <span data-ttu-id="e8e4f-118">Чтобы перенаправить диапазоны отправки для групповых звонков, используйте командлет **Set-CsCallParkOrbit** .</span><span class="sxs-lookup"><span data-stu-id="e8e4f-118">To redirect the Group Call Pickup ranges, use the **Set-CsCallParkOrbit** cmdlet.</span></span>

<span data-ttu-id="e8e4f-119">При развертывании нового пула с использованием другого полного доменного имени (FQDN) для замены основного пула необходимо переназначить все диапазоны номеров отправки групповых звонков, которые были связаны с основным пулом, в полное доменное имя нового пула.</span><span class="sxs-lookup"><span data-stu-id="e8e4f-119">If you deploy a new pool with a different fully qualified domain name (FQDN) to replace the primary pool, you need to reassign all the Group Call Pickup number ranges that were associated with the primary pool to the FQDN of the new pool.</span></span> <span data-ttu-id="e8e4f-120">Чтобы переназначить диапазоны номеров в новый пул, можно использовать командлет **Set-CsCallParkOrbit** .</span><span class="sxs-lookup"><span data-stu-id="e8e4f-120">To reassign number ranges to the new pool, you can use the **Set-CsCallParkOrbit** cmdlet.</span></span> <span data-ttu-id="e8e4f-121">Подробные сведения о командлете **Set-CsCallParkOrbit** можно найти в статьях [Set-CsCallParkOrbit](https://docs.microsoft.com/powershell/module/skype/Set-CsCallParkOrbit).</span><span class="sxs-lookup"><span data-stu-id="e8e4f-121">For details about the **Set-CsCallParkOrbit** cmdlet, see [Set-CsCallParkOrbit](https://docs.microsoft.com/powershell/module/skype/Set-CsCallParkOrbit).</span></span>

</div>

<div>

## <a name="group-call-pickup-experience-during-pool-failure"></a><span data-ttu-id="e8e4f-122">Использование функции отправки группового звонка в случае сбоя пула</span><span class="sxs-lookup"><span data-stu-id="e8e4f-122">Group Call Pickup Experience During Pool Failure</span></span>

<span data-ttu-id="e8e4f-123">В приведенной ниже таблице описаны возможности отправки групповых звонков с помощью этапов восстановления после аварии.</span><span class="sxs-lookup"><span data-stu-id="e8e4f-123">The following table summarizes the Group Call Pickup experience through the phases of disaster recovery.</span></span>

### <a name="user-experience-during-disaster-recovery"></a><span data-ttu-id="e8e4f-124">Взаимодействие с пользователем во время аварийного восстановления</span><span class="sxs-lookup"><span data-stu-id="e8e4f-124">User Experience During Disaster Recovery</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e8e4f-125">Состояние звонка</span><span class="sxs-lookup"><span data-stu-id="e8e4f-125">Call state</span></span></th>
<th><span data-ttu-id="e8e4f-126">Отработка отказа для резервного пула</span><span class="sxs-lookup"><span data-stu-id="e8e4f-126">Failover to backup pool</span></span></th>
<th><span data-ttu-id="e8e4f-127">Восстановление размещения для основного пула</span><span class="sxs-lookup"><span data-stu-id="e8e4f-127">Failback to primary pool</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e8e4f-128">Новые звонки</span><span class="sxs-lookup"><span data-stu-id="e8e4f-128">New calls</span></span></p></td>
<td><p><span data-ttu-id="e8e4f-129"><strong>В процессе отработки отказа:</strong></span><span class="sxs-lookup"><span data-stu-id="e8e4f-129"><strong>During failover process:</strong></span></span></p>
<ul>
<li><p><span data-ttu-id="e8e4f-130">Отправка группового звонка недоступна для пользователей в режиме устойчивости</span><span class="sxs-lookup"><span data-stu-id="e8e4f-130">Group Call Pickup not available for users in resiliency mode</span></span></p></li>
</ul>
<p><span data-ttu-id="e8e4f-131"><strong>После завершения отработки отказа:</strong></span><span class="sxs-lookup"><span data-stu-id="e8e4f-131"><strong>After failover is complete:</strong></span></span></p>
<ul>
<li><p><span data-ttu-id="e8e4f-132">Функция отправки группового звонка доступна, когда пользователь выходит из диапазона номеров для отправки и нумерации для групповых звонков, которые перенаправляются в пул резервного копирования</span><span class="sxs-lookup"><span data-stu-id="e8e4f-132">Group Call Pickup available when users out of resiliency and Group Call Pickup number ranges are redirected to backup pool</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="e8e4f-133"><strong>В процессе восстановления размещения:</strong></span><span class="sxs-lookup"><span data-stu-id="e8e4f-133"><strong>During failback process:</strong></span></span></p>
<ul>
<li><p><span data-ttu-id="e8e4f-134">Отправка группового звонка недоступна для пользователей в режиме устойчивости</span><span class="sxs-lookup"><span data-stu-id="e8e4f-134">Group Call Pickup not available for users in resiliency mode</span></span></p></li>
</ul>
<p><span data-ttu-id="e8e4f-135"><strong>После завершения восстановления после сбоя выполните указанные ниже действия.</strong></span><span class="sxs-lookup"><span data-stu-id="e8e4f-135"><strong>After failback is complete:</strong></span></span></p>
<ul>
<li><p><span data-ttu-id="e8e4f-136">Функция отправки группового вызова доступна, когда пользователь выходит из диапазонов устойчивости и номеров для отправки групповых вызовов, перенаправляется обратно в основной пул</span><span class="sxs-lookup"><span data-stu-id="e8e4f-136">Group Call Pickup available when users out of resiliency and Group Call Pickup number ranges are redirected back to primary pool</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8e4f-137">В очереди раскладки звонков в групповых звонках</span><span class="sxs-lookup"><span data-stu-id="e8e4f-137">Calls in Group Call Pickup queue</span></span></p></td>
<td><p><span data-ttu-id="e8e4f-138"><strong>В процессе отработки отказа:</strong></span><span class="sxs-lookup"><span data-stu-id="e8e4f-138"><strong>During failover process:</strong></span></span></p>
<ul>
<li><p><span data-ttu-id="e8e4f-139">Звонки из очереди нельзя отвечать на запросы с помощью группового звонка.</span><span class="sxs-lookup"><span data-stu-id="e8e4f-139">Calls in queue cannot be answered through Group Call Pickup.</span></span></p></li>
</ul>
<p><span data-ttu-id="e8e4f-140"><strong>После завершения отработки отказа:</strong></span><span class="sxs-lookup"><span data-stu-id="e8e4f-140"><strong>After failover is complete:</strong></span></span></p>
<ul>
<li><p><span data-ttu-id="e8e4f-141">Нет вызовов в этом состоянии</span><span class="sxs-lookup"><span data-stu-id="e8e4f-141">No calls in this state</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="e8e4f-142"><strong>В процессе восстановления размещения:</strong></span><span class="sxs-lookup"><span data-stu-id="e8e4f-142"><strong>During failback process:</strong></span></span></p>
<ul>
<li><p><span data-ttu-id="e8e4f-143">Звонки из очереди нельзя отвечать на запросы с помощью группового звонка.</span><span class="sxs-lookup"><span data-stu-id="e8e4f-143">Calls in queue cannot be answered through Group Call Pickup.</span></span></p></li>
</ul>
<p><span data-ttu-id="e8e4f-144"><strong>После завершения восстановления после сбоя выполните указанные ниже действия.</strong></span><span class="sxs-lookup"><span data-stu-id="e8e4f-144"><strong>After failback is complete:</strong></span></span></p>
<ul>
<li><p><span data-ttu-id="e8e4f-145">Звонки из очереди нельзя отвечать на запросы с помощью группового звонка.</span><span class="sxs-lookup"><span data-stu-id="e8e4f-145">Calls in queue cannot be answered through Group Call Pickup.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8e4f-146">Установленный Звонок</span><span class="sxs-lookup"><span data-stu-id="e8e4f-146">Established call</span></span></p></td>
<td><p><span data-ttu-id="e8e4f-147"><strong>В процессе отработки отказа:</strong></span><span class="sxs-lookup"><span data-stu-id="e8e4f-147"><strong>During failover process:</strong></span></span></p>
<ul>
<li><p><span data-ttu-id="e8e4f-148">Звонки остаются подключенными</span><span class="sxs-lookup"><span data-stu-id="e8e4f-148">Calls stay connected</span></span></p></li>
</ul>
<p><span data-ttu-id="e8e4f-149"><strong>После завершения отработки отказа:</strong></span><span class="sxs-lookup"><span data-stu-id="e8e4f-149"><strong>After failover is complete:</strong></span></span></p>
<ul>
<li><p><span data-ttu-id="e8e4f-150">Звонки остаются подключенными</span><span class="sxs-lookup"><span data-stu-id="e8e4f-150">Calls stay connected</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="e8e4f-151"><strong>В процессе восстановления размещения:</strong></span><span class="sxs-lookup"><span data-stu-id="e8e4f-151"><strong>During failback process:</strong></span></span></p>
<ul>
<li><p><span data-ttu-id="e8e4f-152">Звонки остаются подключенными</span><span class="sxs-lookup"><span data-stu-id="e8e4f-152">Calls stay connected</span></span></p></li>
</ul>
<p><span data-ttu-id="e8e4f-153"><strong>После завершения восстановления после сбоя выполните указанные ниже действия.</strong></span><span class="sxs-lookup"><span data-stu-id="e8e4f-153"><strong>After failback is complete:</strong></span></span></p>
<ul>
<li><p><span data-ttu-id="e8e4f-154">Звонки остаются подключенными</span><span class="sxs-lookup"><span data-stu-id="e8e4f-154">Calls stay connected</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table><span data-ttu-id="e8e4f-155">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e8e4f-155">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

