---
title: 'Lync Server 2013: время восстановления при отработке отказа пулом и восстановления пула после сбоя'
description: Время восстановления для Lync Server 2013 для отработки отказа пула и восстановления размещения в пуле.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Recovery time for pool failover and pool failback
ms:assetid: 902c658f-8442-4d0d-b3ad-bf795ecd550d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205079(v=OCS.15)
ms:contentKeyID: 48184786
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1bb09c32ac4d062358a511464dc21aa7346ee034
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436680"
---
# <a name="recovery-time-for-pool-failover-and-pool-failback-in-lync-server-2013"></a><span data-ttu-id="ae749-103">Время восстановления при отработке отказа пулом и восстановления пула после сбоя в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ae749-103">Recovery time for pool failover and pool failback in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ae749-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ae749-104">

<span> </span></span></span>

<span data-ttu-id="ae749-105">_**Тема последнего изменения:** 2012-09-10_</span><span class="sxs-lookup"><span data-stu-id="ae749-105">_**Topic Last Modified:** 2012-09-10_</span></span>

<span data-ttu-id="ae749-106">Для цели обслуживания отказов в пуле и восстановления размещения в пуле необходимо 30 минут, так как Целевая цель проектирования для времени восстановления (RTO).</span><span class="sxs-lookup"><span data-stu-id="ae749-106">For pool failover and pool failback, the engineering target for recovery time objective (RTO) is 30 minutes.</span></span> <span data-ttu-id="ae749-107">Это время, необходимое для выполнения отработки отказа, после того как администраторы определили аварии и инициировали процедуры перехода на другой ресурс.</span><span class="sxs-lookup"><span data-stu-id="ae749-107">This is the time required for the failover to happen, after administrators have determined there was a disaster and initiated the failover procedures.</span></span> <span data-ttu-id="ae749-108">Этот срок не включает в себя время, необходимое администраторам для оценки ситуации и принятия решения, а также не включает в себя время, необходимое пользователям для повторного входа после завершения отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="ae749-108">It does not include the time for administrators to assess the situation and make a decision, nor does it include the time for users to sign in again after failover is complete.</span></span>

<span data-ttu-id="ae749-109">В случае отработки отказа пула и восстановления из пула, Целевая цель разработки для цели точки восстановления (RPO) составляет 30 минут.</span><span class="sxs-lookup"><span data-stu-id="ae749-109">For pool failover and pool failback, the engineering target for recovery point objective (RPO) is 30 minutes.</span></span> <span data-ttu-id="ae749-110">Она представляет временную меру данных, которые могут быть потеряны вследствие аварии в связи с задержкой репликации данных службы резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="ae749-110">This represents the time measure of data that could be lost due to the disaster, due to replication latency of the Backup Service.</span></span> <span data-ttu-id="ae749-111">Например, если пул переходит на 10:00 утра, а RPO составляет 30 минут, данные из него записываются в пул между 9:30 утра.</span><span class="sxs-lookup"><span data-stu-id="ae749-111">For example, if a pool goes down at 10:00 A.M., and the RPO is 30 minutes, data written to the pool between 9:30 A.M.</span></span> <span data-ttu-id="ae749-112">и 10:00 A. м. возможно, она не была реплицирована в пул резервных копий и будет потеряна.</span><span class="sxs-lookup"><span data-stu-id="ae749-112">and 10:00 A.M.might not have replicated to the backup pool, and would be lost.</span></span>

<span data-ttu-id="ae749-113">В настоящем документе для всех значений RTO и RPO предполагается, что два центра обработки данных размещены в одном мировом регионе с высокоскоростным транспортом без задержек между двумя узлами.</span><span class="sxs-lookup"><span data-stu-id="ae749-113">All RTO and RPO numbers in this document assume that the two data centers are located within the same world region with high-speed, low-latency transport between the two sites.</span></span> <span data-ttu-id="ae749-114">Эти значения измеряются для пула с 40 000 одновременно активных пользователей и 200 000 пользователей, активированных для применения Lync в соответствии с предварительно заданной моделью пользователей, в которой при репликации данных нет невыполненных операций.</span><span class="sxs-lookup"><span data-stu-id="ae749-114">These numbers are measured for a pool with 40,000 concurrently active users and 200,000 users enabled for Lync with respect to a pre-defined user model where there is no backlog in data replication.</span></span> <span data-ttu-id="ae749-115">Они могут изменяться после тестирования производительности и проверки.</span><span class="sxs-lookup"><span data-stu-id="ae749-115">They are subject to change based on performance testing and validation.</span></span>

<span data-ttu-id="ae749-116"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ae749-116"></div>

<span> </span>

</div>

</div>

</span></span></div>

