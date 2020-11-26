---
title: 'Lync Server 2013: восстановление пула сервера Lync Server'
description: 'Lync Server 2013: восстановление пула сервера Lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Restoring a Lync Server pool
ms:assetid: 6fe80fb3-38ad-4931-a07b-1763b61aa448
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202176(v=OCS.15)
ms:contentKeyID: 51541488
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 02e92b4e7af9cf782d49c265425006e0118b9161
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442602"
---
# <a name="restoring-a-lync-server-pool-in-lync-server-2013"></a><span data-ttu-id="3f25e-103">Восстановление пула сервера Lync Server в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3f25e-103">Restoring a Lync Server pool in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3f25e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3f25e-104">

<span> </span></span></span>

<span data-ttu-id="3f25e-105">_**Тема последнего изменения:** 2013-02-18_</span><span class="sxs-lookup"><span data-stu-id="3f25e-105">_**Topic Last Modified:** 2013-02-18_</span></span>

<span data-ttu-id="3f25e-106">Развертывание Lync Server может включать следующие типы пулов:</span><span class="sxs-lookup"><span data-stu-id="3f25e-106">Your Lync Server deployment may include any of the following types of pools:</span></span>

  - <span data-ttu-id="3f25e-107">переднего плана</span><span class="sxs-lookup"><span data-stu-id="3f25e-107">Front End Server</span></span>

  - <span data-ttu-id="3f25e-108">Сервер-посредник</span><span class="sxs-lookup"><span data-stu-id="3f25e-108">Mediation Server</span></span>

  - <span data-ttu-id="3f25e-109">Сервер сохраняемого чата</span><span class="sxs-lookup"><span data-stu-id="3f25e-109">Persistent Chat Server</span></span>

  - <span data-ttu-id="3f25e-110">Пограничный сервер</span><span class="sxs-lookup"><span data-stu-id="3f25e-110">Edge Server</span></span>

<span data-ttu-id="3f25e-111">Если в пуле всего происходит отключение, выполните следующие действия для каждого сервера в пуле.</span><span class="sxs-lookup"><span data-stu-id="3f25e-111">If an entire pool experiences an outage, follow these procedures for each member server in the pool.</span></span>

  - <span data-ttu-id="3f25e-112">Для пула переднего плана сначала восстановите сервер обратного доступа, а затем восстановите каждый сервер переднего плана.</span><span class="sxs-lookup"><span data-stu-id="3f25e-112">For a Front End pool, restore the Back End Server first, and then restore each Front End Server.</span></span> <span data-ttu-id="3f25e-113">Дополнительные сведения можно найти [в разделе Восстановление сервера выпуска Enterprise Edition в Lync server 2013](lync-server-2013-restoring-an-enterprise-edition-back-end-server.md) и [Восстановление рядового сервера Enterprise Edition в Lync Server 2013](lync-server-2013-restoring-an-enterprise-edition-member-server.md).</span><span class="sxs-lookup"><span data-stu-id="3f25e-113">For details, see [Restoring an Enterprise Edition Back End Server in Lync Server 2013](lync-server-2013-restoring-an-enterprise-edition-back-end-server.md) and [Restoring an Enterprise Edition member server in Lync Server 2013](lync-server-2013-restoring-an-enterprise-edition-member-server.md).</span></span>

  - <span data-ttu-id="3f25e-114">Для всех остальных типов пулов, восстановите каждый сервер участника.</span><span class="sxs-lookup"><span data-stu-id="3f25e-114">For all other types of pools, restore each member server.</span></span> <span data-ttu-id="3f25e-115">Подробные сведения можно найти [в разделе Восстановление сервера в составе корпоративного выпуска Lync server 2013](lync-server-2013-restoring-an-enterprise-edition-member-server.md).</span><span class="sxs-lookup"><span data-stu-id="3f25e-115">For details, see [Restoring an Enterprise Edition member server in Lync Server 2013](lync-server-2013-restoring-an-enterprise-edition-member-server.md).</span></span>

<span data-ttu-id="3f25e-116"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3f25e-116"></div>

<span> </span>

</div>

</div>

</span></span></div>

