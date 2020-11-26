---
title: 'Lync Server 2013: планирование высокой доступности и аварийного восстановления'
description: 'Lync Server 2013: Планирование высокой доступности и аварийного восстановления.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for high availability and disaster recovery
ms:assetid: 15a72073-0336-45dd-b2a0-35e7522c6000
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204703(v=OCS.15)
ms:contentKeyID: 48183497
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6bb5f430201c48738421c4fbe72151ca58173898
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442959"
---
# <a name="planning-for-high-availability-and-disaster-recovery-in-lync-server-2013"></a><span data-ttu-id="b3a72-103">Планирование высокой доступности и аварийного восстановления в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b3a72-103">Planning for high availability and disaster recovery in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b3a72-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b3a72-104">

<span> </span></span></span>

<span data-ttu-id="b3a72-105">_**Тема последнего изменения:** 2013-10-31_</span><span class="sxs-lookup"><span data-stu-id="b3a72-105">_**Topic Last Modified:** 2013-10-31_</span></span>

<span data-ttu-id="b3a72-106">Как и в Lync Server 2010, основная схема высокой доступности для большинства ролей сервера в Lync Server 2013 базируется на избыточности сервера посредством группировки.</span><span class="sxs-lookup"><span data-stu-id="b3a72-106">As in Lync Server 2010, the main high availability scheme for most server roles in Lync Server 2013 is based on server redundancy via pooling.</span></span> <span data-ttu-id="b3a72-107">При сбое сервера с определенными ролями остальные серверы в пуле с такими же ролями берут на себя нагрузку этого сервера.</span><span class="sxs-lookup"><span data-stu-id="b3a72-107">If a server running a certain server role fails, the other servers in the pool running the same role take the load of that server.</span></span> <span data-ttu-id="b3a72-108">Это касается серверов переднего плана, пограничных серверов, серверов-посредников и Директоров.</span><span class="sxs-lookup"><span data-stu-id="b3a72-108">This applies to Front End Servers, Edge Servers, Mediation Servers, and Directors.</span></span>

<span data-ttu-id="b3a72-109">Lync Server 2013 добавляет новые показатели аварийного восстановления для пулов переднего плана с помощью географических dispersement серверов в двух центрах обработки данных для предоставления услуг по продолжению всего пула или сайта.</span><span class="sxs-lookup"><span data-stu-id="b3a72-109">Lync Server 2013 adds new disaster recovery measures for Front End pools by introducing geographical dispersement of your servers into two data centers to provide continuation of service should one entire pool or site go down.</span></span>

<span data-ttu-id="b3a72-110">Lync Server 2013 также повышает уровень высокой доступности сервера благодаря поддержке синхронного зеркального отображения SQL для серверных баз данных.</span><span class="sxs-lookup"><span data-stu-id="b3a72-110">Lync Server 2013 also enhances Back End Server high availability, by supporting synchronous SQL mirroring for your Back End databases.</span></span>

<span data-ttu-id="b3a72-111">В этом разделе объясняются основные возможности высокой доступности и аварийного восстановления, а также описаны действия, которые можно выполнить для обеспечения высокой доступности и аварийного восстановления для других ролей сервера.</span><span class="sxs-lookup"><span data-stu-id="b3a72-111">This section explains these major high availability and disaster recovery features, and also covers what steps you can take for high availability and disaster recovery for your other server roles as well.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="b3a72-112">Содержание</span><span class="sxs-lookup"><span data-stu-id="b3a72-112">In This Section</span></span>

  - [<span data-ttu-id="b3a72-113">Аварийное восстановление пула переднего плана в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b3a72-113">Front End pool disaster recovery in Lync Server 2013</span></span>](lync-server-2013-front-end-pool-disaster-recovery.md)

  - [<span data-ttu-id="b3a72-114">Аварийное восстановление пограничного сервера в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b3a72-114">Edge Server disaster recovery in Lync Server 2013</span></span>](lync-server-2013-edge-server-disaster-recovery.md)

  - [<span data-ttu-id="b3a72-115">Планирование устойчивости корпоративной голосовой связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b3a72-115">Planning for Enterprise Voice resiliency in Lync Server 2013</span></span>](lync-server-2013-planning-for-enterprise-voice-resiliency.md)

  - [<span data-ttu-id="b3a72-116">Функции управления вызовами для аварийного восстановления в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b3a72-116">Call management features for disaster recovery in Lync Server 2013</span></span>](lync-server-2013-call-management-features-for-disaster-recovery.md)

  - [<span data-ttu-id="b3a72-117">Настройка сервера сохраняемого чата для обеспечения высокой доступности и аварийного восстановления в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b3a72-117">Configuring Persistent Chat Server for high availability and disaster recovery in Lync Server 2013</span></span>](lync-server-2013-configuring-persistent-chat-server-for-high-availability-and-disaster-recovery.md)

  - [<span data-ttu-id="b3a72-118">Устойчивость главного сайта Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="b3a72-118">Lync Server 2010 metropolitan site resiliency</span></span>](lync-server-2013-compatibility-with-lync-server-2010-metropolitan-site-resiliency.md)

<span data-ttu-id="b3a72-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b3a72-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

