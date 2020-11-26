---
title: 'Lync Server 2013: восстановление данных и параметров'
description: 'Lync Server 2013: восстановление данных и параметров.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Restoring data and settings
ms:assetid: b07f5dd7-7bed-4819-8cb5-617f5acd478e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202185(v=OCS.15)
ms:contentKeyID: 51541503
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 694b1e362d729d354b08367d31c47e8ca866dd91
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442532"
---
# <a name="restoring-data-and-settings-in-lync-server-2013"></a><span data-ttu-id="2fd22-103">Восстановление данных и параметров в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2fd22-103">Restoring data and settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2fd22-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2fd22-104">

<span> </span></span></span>

<span data-ttu-id="2fd22-105">_**Тема последнего изменения:** 2013-02-17_</span><span class="sxs-lookup"><span data-stu-id="2fd22-105">_**Topic Last Modified:** 2013-02-17_</span></span>

<span data-ttu-id="2fd22-106">Если вы реализовали топологию аварийного восстановления с объединенными пулами, а один из этих пулов переднего плана отключился и вам нужно быстро восстановить службу для пользователей, ознакомьтесь [с разработкой отказа в пуле в Lync Server 2013](lync-server-2013-failing-over-a-pool.md).</span><span class="sxs-lookup"><span data-stu-id="2fd22-106">If you have implemented a disaster recovery topology with paired pools, and one of those Front End pools has gone down and you need to quickly restore service to your users, see [Failing over a pool in Lync Server 2013](lync-server-2013-failing-over-a-pool.md).</span></span> <span data-ttu-id="2fd22-107">В противном случае используйте сведения из указанных ниже разделов, а также листы [резервного копирования и восстановления для Lync server 2013](lync-server-2013-backup-and-restoration-worksheets.md)для восстановления сервера Lync после сбоя или сбоя.</span><span class="sxs-lookup"><span data-stu-id="2fd22-107">Otherwise, use the information in the following topics, along with the worksheets in [Backup and restoration worksheets for Lync Server 2013](lync-server-2013-backup-and-restoration-worksheets.md), to restore Lync Server after a failure or outage.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="2fd22-108">Чтобы сократить время бездействия и возможной потери данных, выполните процедуры восстановления, описанные в этом документе, только в том случае, если процедуры устранения неполадок не дают результатов для выявления и устранения проблемы.</span><span class="sxs-lookup"><span data-stu-id="2fd22-108">To reduce downtime and potential data loss, perform the restoration procedures described in this document only if troubleshooting procedures are not effective in identifying and correcting the problem.</span></span> <span data-ttu-id="2fd22-109">Во время устранения неполадок попробуйте минимизировать влияние на другие серверы и компоненты при завершении работы и перезапуске серверов.</span><span class="sxs-lookup"><span data-stu-id="2fd22-109">During troubleshooting, try to minimize the impact on other servers and components as you shut down and restart servers.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="2fd22-110">Содержание</span><span class="sxs-lookup"><span data-stu-id="2fd22-110">In This Section</span></span>

  - [<span data-ttu-id="2fd22-111">Подготовка к восстановлению Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2fd22-111">Preparing to restore Lync Server 2013</span></span>](lync-server-2013-preparing-to-restore-lync-server.md)

  - [<span data-ttu-id="2fd22-112">Восстановление сервера Standard Edition в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2fd22-112">Restoring a Standard Edition server in Lync Server 2013</span></span>](lync-server-2013-restoring-a-standard-edition-server.md)

  - [<span data-ttu-id="2fd22-113">Восстановление сервера, на котором размещается центральное хранилище для управления в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2fd22-113">Restoring the server hosting the Central Management store in Lync Server 2013</span></span>](lync-server-2013-restoring-the-server-hosting-the-central-management-store.md)

  - [<span data-ttu-id="2fd22-114">Восстановление сервера выпуска Enterprise Edition в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2fd22-114">Restoring an Enterprise Edition Back End Server in Lync Server 2013</span></span>](lync-server-2013-restoring-an-enterprise-edition-back-end-server.md)

  - [<span data-ttu-id="2fd22-115">Восстановление сервера участника Enterprise Edition в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2fd22-115">Restoring an Enterprise Edition member server in Lync Server 2013</span></span>](lync-server-2013-restoring-an-enterprise-edition-member-server.md)

  - [<span data-ttu-id="2fd22-116">Восстановление пула сервера Lync Server в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2fd22-116">Restoring a Lync Server pool in Lync Server 2013</span></span>](lync-server-2013-restoring-a-lync-server-pool.md)

  - [<span data-ttu-id="2fd22-117">Выполнение отработки отказа в пуле переднего плана для электронной стороны в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2fd22-117">Performing an ABC Front End pool failover in Lync Server 2013</span></span>](lync-server-2013-performing-an-abc-front-end-pool-failover.md)

  - [<span data-ttu-id="2fd22-118">Восстановление хранилища файлов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2fd22-118">Restoring a file store in Lync Server 2013</span></span>](lync-server-2013-restoring-a-file-store.md)

  - [<span data-ttu-id="2fd22-119">Восстановление данных мониторинга или архивации в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2fd22-119">Restoring monitoring or archiving data in Lync Server 2013</span></span>](lync-server-2013-restoring-monitoring-or-archiving-data.md)

  - [<span data-ttu-id="2fd22-120">Восстановление данных из сохраняемого чата в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2fd22-120">Restoring Persistent Chat data in Lync Server 2013</span></span>](lync-server-2013-restoring-persistent-chat-data.md)

<span data-ttu-id="2fd22-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2fd22-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

