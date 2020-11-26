---
title: 'Lync Server 2013: отработка отказа и восстановление после сбоя сервера сохраняемого чата'
description: 'Lync Server 2013: сбой при обратном и неудачном восстановлении сервера сохраняемого чата.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Failing over and failing back Persistent Chat Server
ms:assetid: bc9a791f-d15c-48c8-8682-1a8ad19d8c75
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205214(v=OCS.15)
ms:contentKeyID: 48185259
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a86a9f809a853d48103a8c50a04773e4625a2b8a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428260"
---
# <a name="failing-over-and-failing-back-persistent-chat-server-in-lync-server-2013"></a><span data-ttu-id="c9a65-103">Отработка отказа и восстановление после сбоя сервера сохраняемого чата в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c9a65-103">Failing over and failing back Persistent Chat Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c9a65-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c9a65-104">

<span> </span></span></span>

<span data-ttu-id="c9a65-105">_**Тема последнего изменения:** 2012-08-03_</span><span class="sxs-lookup"><span data-stu-id="c9a65-105">_**Topic Last Modified:** 2012-08-03_</span></span>

<span data-ttu-id="c9a65-106">Чтобы отдать отказ и отдать отказ на переход на сервер Lync Server 2013, постоянный чат, вам необходимо ознакомиться с процессами репликации и перемещения при сбое для Microsoft SQL Server 2008 R2 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="c9a65-106">To fail over and fail back Lync Server 2013, Persistent Chat Server, you should be familiar with replication and failover processes for Microsoft SQL Server 2008 R2 and later.</span></span> <span data-ttu-id="c9a65-107">Кроме того, необходимо ознакомиться со службами сервера сохраняемого чата.</span><span class="sxs-lookup"><span data-stu-id="c9a65-107">You should also be familiar with the Persistent Chat Server services.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="c9a65-108">Содержание</span><span class="sxs-lookup"><span data-stu-id="c9a65-108">In This Section</span></span>

  - [<span data-ttu-id="c9a65-109">Отработка отказа сервером сохраняемого чата в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c9a65-109">Failing over Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-failing-over-persistent-chat-server.md)

  - [<span data-ttu-id="c9a65-110">Восстановление сервера сохраняемого чата после сбоя в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c9a65-110">Failing back Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-failing-back-persistent-chat-server.md)

<span data-ttu-id="c9a65-111"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c9a65-111"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

