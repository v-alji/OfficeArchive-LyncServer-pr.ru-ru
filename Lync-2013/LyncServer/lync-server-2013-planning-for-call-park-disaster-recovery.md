---
title: 'Lync Server 2013: планирование аварийного восстановления парковки вызовов'
description: 'Lync Server 2013: Планирование аварийного восстановления звонков.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for Call Park disaster recovery
ms:assetid: f7cf3958-177b-4340-a864-35a6f44d6d88
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205395(v=OCS.15)
ms:contentKeyID: 48185867
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e1d05503f1d8c30f4dd4446a995442d5e2500dbc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49397894"
---
# <a name="planning-for-call-park-disaster-recovery-in-lync-server-2013"></a><span data-ttu-id="0eb66-103">Планирование аварийного восстановления парковки вызовов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0eb66-103">Planning for Call Park disaster recovery in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0eb66-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0eb66-104">

<span> </span></span></span>

<span data-ttu-id="0eb66-105">_**Тема последнего изменения:** 2012-10-30_</span><span class="sxs-lookup"><span data-stu-id="0eb66-105">_**Topic Last Modified:** 2012-10-30_</span></span>

<span data-ttu-id="0eb66-106">В этом разделе описаны некоторые способы подготовки приложения на приостановке звонков для аварийного восстановления и некоторых вопросов, которые необходимо выполнить в процессе восстановления после сбоя.</span><span class="sxs-lookup"><span data-stu-id="0eb66-106">This section describes some ways to prepare the Call Park application for disaster recovery and some considerations for the disaster recovery process.</span></span>

<div>

## <a name="preparing-for-call-park-disaster-recovery"></a><span data-ttu-id="0eb66-107">Подготовка к аварийному восстановлению на припаркованных звонках</span><span class="sxs-lookup"><span data-stu-id="0eb66-107">Preparing for Call Park Disaster Recovery</span></span>

<span data-ttu-id="0eb66-108">При подготовке и выполнении процедур аварийного восстановления учитывайте следующее:</span><span class="sxs-lookup"><span data-stu-id="0eb66-108">Keep the following in mind when preparing for and carrying out disaster recovery procedures.</span></span>

  - <span data-ttu-id="0eb66-109">Планирование аварийного восстановления при планировании производственных мощностей.</span><span class="sxs-lookup"><span data-stu-id="0eb66-109">Plan for disaster recovery when you do your capacity planning.</span></span> <span data-ttu-id="0eb66-110">Для производительности аварийного восстановления каждый пул в сопряженном пуле должен поддерживать рабочие нагрузки служб приостановки звонков в обоих пулах.</span><span class="sxs-lookup"><span data-stu-id="0eb66-110">For disaster recovery capacity, each pool in a paired pool should be able to handle the workloads of the Call Park services in both pools.</span></span> <span data-ttu-id="0eb66-111">Дополнительные сведения о планировании мощности при приостановке звонков можно найти [в разделе Планирование мощностей для парковки звонков в Lync Server 2013](lync-server-2013-capacity-planning-for-call-park.md).</span><span class="sxs-lookup"><span data-stu-id="0eb66-111">For details about Call Park capacity planning, see [Capacity planning for Call Park in Lync Server 2013](lync-server-2013-capacity-planning-for-call-park.md).</span></span>

  - <span data-ttu-id="0eb66-112">При аварийном восстановлении пользователи, которые были перенаправлены в резервный пул в рамках процесса перемещения, используют службу "переадресация звонков", запущенную в пуле резервных копий.</span><span class="sxs-lookup"><span data-stu-id="0eb66-112">During disaster recovery, users who have been redirected to the backup pool as part of the failover process use the Call Park service running in the backup pool.</span></span> <span data-ttu-id="0eb66-113">Таким образом, при аварийном восстановлении служба поддержки приостановки звонков требует, чтобы приложение парковки для приема звонков было развернуто и включено как в основном пуле, так и в пуле резервных копий.</span><span class="sxs-lookup"><span data-stu-id="0eb66-113">Therefore, support for Call Park during disaster recovery requires the Call Park application to be deployed and enabled in both the primary pool and the backup pool.</span></span>

  - <span data-ttu-id="0eb66-114">У каждого пула должен быть допустимый диапазон значений орбиты для пользователей, которые находятся в этом пуле, чтобы использовать для вызовов парковки.</span><span class="sxs-lookup"><span data-stu-id="0eb66-114">Each pool must have a valid range of orbit numbers for users who are homed in that pool to use for parking calls.</span></span>

  - <span data-ttu-id="0eb66-115">Всегда сохраняйте отдельную резервную копию всех настроенных на удержании музыкальных файлов, которые были отправлены для приостановки звонка.</span><span class="sxs-lookup"><span data-stu-id="0eb66-115">Always keep a separate backup copy of any customized music on hold that has been uploaded for Call Park.</span></span> <span data-ttu-id="0eb66-116">Эти файлы не заархивированы в рамках процесса аварийного восстановления Lync Server 2013 и будут потеряны, если файлы, отправленные в пул, повреждены, повреждены или удалены.</span><span class="sxs-lookup"><span data-stu-id="0eb66-116">These files are not backed up as part of the Lync Server 2013 disaster recovery process and will be lost if the files uploaded to the pool are damaged, corrupted, or erased.</span></span>

</div>

<div>

## <a name="call-park-disaster-recovery-considerations"></a><span data-ttu-id="0eb66-117">Рекомендации по аварийному восстановлению звонков</span><span class="sxs-lookup"><span data-stu-id="0eb66-117">Call Park Disaster Recovery Considerations</span></span>

<span data-ttu-id="0eb66-118">Вы можете определить только один набор параметров конфигурации приложения для парковки и один настроенный звуковой файл на хранение музыки на каждом пуле.</span><span class="sxs-lookup"><span data-stu-id="0eb66-118">You can define only one set of Call Park application configuration settings and one customized music-on-hold audio file per pool.</span></span> <span data-ttu-id="0eb66-119">Эти параметры включают пороговое значение тайм-аута, музыку на удержании, максимальное количество попыток отправки звонков и URI времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="0eb66-119">These settings include the timeout threshold, music on hold, maximum call pickup attempts, and timeout URI.</span></span> <span data-ttu-id="0eb66-120">Чтобы просмотреть эти параметры конфигурации, запустите командлет **Get-CsCpsConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="0eb66-120">To view these configuration settings, run the **Get-CsCpsConfiguration** cmdlet.</span></span> <span data-ttu-id="0eb66-121">Дополнительные сведения о командлете **Get-CsCpsConfiguration** можно найти в [статьях Get-CsCpsConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsCpsConfiguration).</span><span class="sxs-lookup"><span data-stu-id="0eb66-121">For details about the **Get-CsCpsConfiguration** cmdlet, see [Get-CsCpsConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsCpsConfiguration).</span></span>

<span data-ttu-id="0eb66-122">Во время аварийного восстановления при использовании функции "Приостановка звонка" в пуле резервных копий используется приложение парковки звонков, поэтому параметры в основном пуле не заархивированы.</span><span class="sxs-lookup"><span data-stu-id="0eb66-122">During disaster recovery, Call Park uses the Call Park application in the backup pool, so settings in the primary pool are not backed up.</span></span> <span data-ttu-id="0eb66-123">Если основной пул не поддается восстановлению и вы разворачиваете новый пул для замены основного пула, параметры из основного пула теряются, и вам необходимо изменить параметры парковки на звонки и все настроенные звуковые файлы для музыки в новом пуле.</span><span class="sxs-lookup"><span data-stu-id="0eb66-123">If the primary pool can't be recovered and you deploy a new pool to replace the primary pool, the settings from the primary pool are lost, and you need to reconfigure the Call Park settings and any customized music-on-hold audio files in the new pool.</span></span>

<span data-ttu-id="0eb66-124">При развертывании нового пула с использованием другого полного доменного имени (FQDN) для замены основного пула необходимо переназначить все диапазоны орбиты, связанные с основным пулом, до полного доменного имени нового пула.</span><span class="sxs-lookup"><span data-stu-id="0eb66-124">If you deploy a new pool with a different fully qualified domain name (FQDN) to replace the primary pool, you need to reassign all the Call Park orbit ranges that were associated with the primary pool to the FQDN of the new pool.</span></span> <span data-ttu-id="0eb66-125">Чтобы переназначить диапазоны орбиты в новый пул, вы можете использовать либо панель управления Lync Server, либо командлет **Set-CsCallParkOrbit** .</span><span class="sxs-lookup"><span data-stu-id="0eb66-125">To reassign orbit ranges to the new pool, you can use either Lync Server Control Panel or the **Set-CsCallParkOrbit** cmdlet.</span></span> <span data-ttu-id="0eb66-126">Подробные сведения о командлете **Set-CsCallParkOrbit** можно найти в статьях [Set-CsCallParkOrbit](https://docs.microsoft.com/powershell/module/skype/Set-CsCallParkOrbit).</span><span class="sxs-lookup"><span data-stu-id="0eb66-126">For details about the **Set-CsCallParkOrbit** cmdlet, see [Set-CsCallParkOrbit](https://docs.microsoft.com/powershell/module/skype/Set-CsCallParkOrbit).</span></span>

<span data-ttu-id="0eb66-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0eb66-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

