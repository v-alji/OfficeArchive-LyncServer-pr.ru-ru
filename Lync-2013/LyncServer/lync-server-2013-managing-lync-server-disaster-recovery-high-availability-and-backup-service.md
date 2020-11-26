---
title: Управление аварийным восстановлением Lync Server, высокой доступностью и службой резервного копирования
description: Управление аварийным восстановлением Lync Server, высокой доступностью и службой резервного копирования.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing Lync Server disaster recovery, high availability, and Backup Service
ms:assetid: f4cd36fb-ffd6-48fa-b761-e11b3bcff91a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721939(v=OCS.15)
ms:contentKeyID: 49733876
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3e440c8c72ab5e66d27a86dfce963368dff804bc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437318"
---
# <a name="managing-lync-server-2013-disaster-recovery-high-availability-and-backup-service"></a><span data-ttu-id="98f05-103">Управление аварийным восстановлением, высокой доступностью и службой резервного копирования Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="98f05-103">Managing Lync Server 2013 disaster recovery, high availability, and Backup Service</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="98f05-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="98f05-104">

<span> </span></span></span>

<span data-ttu-id="98f05-105">_**Тема последнего изменения:** 2012-11-12_</span><span class="sxs-lookup"><span data-stu-id="98f05-105">_**Topic Last Modified:** 2012-11-12_</span></span>

<span data-ttu-id="98f05-106">В этом разделе содержатся процедуры для операций аварийного восстановления, а также обслуживания службы резервного копирования, которая синхронизирует данные в связанных пулах серверных интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="98f05-106">This section contains procedures for disaster recovery operations, as well as for maintaining the Backup Service which synchronizes the data in paired Front End pools.</span></span>

<span data-ttu-id="98f05-107">Процедуры аварийного восстановления, как в случае сбоя, так и для перемещения после сбоя, выполняются вручную.</span><span class="sxs-lookup"><span data-stu-id="98f05-107">Disaster recovery procedures, both failover and failback, are manual.</span></span> <span data-ttu-id="98f05-108">При возникновении аварии администратор должен вручную вызвать процедуры перемещения.</span><span class="sxs-lookup"><span data-stu-id="98f05-108">If there is a disaster, the administrator must manually invoke the failover procedures.</span></span> <span data-ttu-id="98f05-109">Это применимо к восстановлению после восстановления пула.</span><span class="sxs-lookup"><span data-stu-id="98f05-109">The same applies to failback after the pool is repaired.</span></span>

<span data-ttu-id="98f05-110">Процедуры аварийного восстановления в оставшейся части этого раздела предполагают следующее:</span><span class="sxs-lookup"><span data-stu-id="98f05-110">The disaster recovery procedures in the rest of this section assume the following:</span></span>

  - <span data-ttu-id="98f05-111">У вас есть развертывание с подключенными пулами переднего плана, расположенными на разных сайтах, как описано в разделе [Планирование обеспечения высокой доступности и аварийного восстановления в Lync Server 2013](lync-server-2013-planning-for-high-availability-and-disaster-recovery.md).</span><span class="sxs-lookup"><span data-stu-id="98f05-111">You have a deployment with paired Front End pools, located in different sites, as described in [Planning for high availability and disaster recovery in Lync Server 2013](lync-server-2013-planning-for-high-availability-and-disaster-recovery.md).</span></span> <span data-ttu-id="98f05-112">Служба архивации запущена на этих подключенных пулах, чтобы синхронизировать их.</span><span class="sxs-lookup"><span data-stu-id="98f05-112">The Backup Service has been running on these paired pools to keep them synchronized.</span></span>

  - <span data-ttu-id="98f05-113">Если хранилище Центрального управления размещено на любом из пулов, оно установлено и запущено на обоих из них, с одним из них, где размещается активный хозяин, и другой пул, на котором размещается резерв.</span><span class="sxs-lookup"><span data-stu-id="98f05-113">If the Central Management store is hosted on either pool, it is installed and running on both of the paired pools, with one of those pools hosting the active master and the other pool hosting the standby.</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="98f05-114">В описанных ниже процедурах параметр <EM>PoolFQDN</EM> указывает на полное доменное имя пула, на которое влияет авария, а не тот, на который перенаправлены пользователи, а не в пул.</span><span class="sxs-lookup"><span data-stu-id="98f05-114">In the following procedures, the <EM>PoolFQDN</EM> parameter refers to the FQDN of the pool that is affected by disaster, not the pool that affected users are being redirected from.</span></span> <span data-ttu-id="98f05-115">Для одного и того же набора затронутых пользователей он ссылается на один и тот же пул командлетов перемещения при сбое и восстановления размещения (то есть, пул, который сначала размещает пользователей перед переходом на другой ресурс).</span><span class="sxs-lookup"><span data-stu-id="98f05-115">For the same set of affected users, it refers to the same pool in both failover and failback cmdlets (that is, the pool that first homed the users before the failover).</span></span><BR><span data-ttu-id="98f05-116">Например, предположим, что для всех пользователей, использующих пул P1, не удалось выполнить резервное копирование в распределенный пул P2.</span><span class="sxs-lookup"><span data-stu-id="98f05-116">For example, assume a case in which all users homed on a pool P1 were failed over to the backup pool, P2.</span></span> <span data-ttu-id="98f05-117">Если администратор хочет переместить всех пользователей, обслуживаемых в P2, для обслуживания с помощью P1, администратор должен выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="98f05-117">If the administrator wants to move all the users currently serviced by P2 to be serviced by P1, the administrator must perform the following steps:</span></span> 
> <OL>
> <LI>
> <P><span data-ttu-id="98f05-118">Не удается вернуть все пользователи, изначально размещенные в P1, из P2 в P1 с помощью командлета восстановления размещения.</span><span class="sxs-lookup"><span data-stu-id="98f05-118">Fail back all the users originally homed on P1 from P2 to P1 using the failback cmdlet.</span></span> <span data-ttu-id="98f05-119">В этом случае <EM>PoolFQDN</EM> — P1's FQDN.</span><span class="sxs-lookup"><span data-stu-id="98f05-119">In this case, the <EM>PoolFQDN</EM> is P1’s FQDN.</span></span></P>
> <LI>
> <P><span data-ttu-id="98f05-120">Отработка отказа всех пользователей, первоначально подключенных к P2, с помощью командлета failover.</span><span class="sxs-lookup"><span data-stu-id="98f05-120">Fail over all the users originally homed on P2 to P1 using the failover cmdlet.</span></span> <span data-ttu-id="98f05-121">В этом случае <EM>PoolFQDN</EM> — P2's FQDN.</span><span class="sxs-lookup"><span data-stu-id="98f05-121">In this case, the <EM>PoolFQDN</EM> is P2’s FQDN.</span></span></P>
> <LI>
> <P><span data-ttu-id="98f05-122">Если в дальнейшем администратор хочет вернуть пользователей P2 в P2, <EM>PoolFQDN</EM> — P2's FQDN.</span><span class="sxs-lookup"><span data-stu-id="98f05-122">If the administrator later wants to fail back those P2 users back to P2, the <EM>PoolFQDN</EM> is P2’s FQDN.</span></span></P></LI></OL><span data-ttu-id="98f05-123">Обратите внимание, что шаг 1 описанный выше должен выполняться перед шагом 2, чтобы сохранить целостность пула.</span><span class="sxs-lookup"><span data-stu-id="98f05-123">Note that step 1 above must be performed before step 2 to preserve pool integrity.</span></span> <span data-ttu-id="98f05-124">Если вы попытаетесь выполнить действие 2 перед шагом 1, командлет Step 2 завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="98f05-124">If you try step 2 before step 1, the step 2 cmdlet will fail.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="98f05-125">Содержание</span><span class="sxs-lookup"><span data-stu-id="98f05-125">In This Section</span></span>

  - [<span data-ttu-id="98f05-126">Настройка и мониторинг службы резервного копирования в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="98f05-126">Configuring and monitoring the Backup Service in Lync Server 2013</span></span>](lync-server-2013-configuring-and-monitoring-the-backup-service.md)

  - [<span data-ttu-id="98f05-127">Отработка отказа для пула в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="98f05-127">Failing over a pool in Lync Server 2013</span></span>](lync-server-2013-failing-over-a-pool.md)

  - [<span data-ttu-id="98f05-128">Отработка отказа для пула в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="98f05-128">Failing back a pool in Lync Server 2013</span></span>](lync-server-2013-failing-back-a-pool.md)

  - [<span data-ttu-id="98f05-129">Отработка отказа с использованием зеркальной базы данных в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="98f05-129">Failing over a mirrored database in Lync Server 2013</span></span>](lync-server-2013-failing-over-a-mirrored-database.md)

  - [<span data-ttu-id="98f05-130">Отработка отказа для пограничного пула, используемого для федерации Lync Server в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="98f05-130">Failing over the Edge pool used for Lync Server federation in Lync Server 2013</span></span>](lync-server-2013-failing-over-the-edge-pool-used-for-lync-server-federation.md)

  - [<span data-ttu-id="98f05-131">Отработка отказа для пограничного пула, используемого для федерации XMPP в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="98f05-131">Failing over the Edge pool used for XMPP federation in Lync Server 2013</span></span>](lync-server-2013-failing-over-the-edge-pool-used-for-xmpp-federation.md)

  - [<span data-ttu-id="98f05-132">Отработка отказа для пограничного пула, используемого для федерации Lync Server или федерации XMPP в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="98f05-132">Failing back the Edge pool used for Lync Server federation or XMPP federation in Lync Server 2013</span></span>](lync-server-2013-failing-back-the-edge-pool-used-for-lync-server-federation-or-xmpp-federation.md)

  - [<span data-ttu-id="98f05-133">Изменение пограничного пула, связанного с пулом переднего плана в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="98f05-133">Changing the Edge pool associated with a Front End pool in Lync Server 2013</span></span>](lync-server-2013-changing-the-edge-pool-associated-with-a-front-end-pool.md)

  - [<span data-ttu-id="98f05-134">Восстановление содержимого конференций с помощью службы резервного копирования в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="98f05-134">Restoring conference contents using the Backup Service in Lync Server 2013</span></span>](lync-server-2013-restoring-conference-contents-using-the-backup-service.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="98f05-135">См. также</span><span class="sxs-lookup"><span data-stu-id="98f05-135">See Also</span></span>


[<span data-ttu-id="98f05-136">Планирование высокой доступности и аварийного восстановления в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="98f05-136">Planning for high availability and disaster recovery in Lync Server 2013</span></span>](lync-server-2013-planning-for-high-availability-and-disaster-recovery.md)  
  

<span data-ttu-id="98f05-137"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="98f05-137"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

