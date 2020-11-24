---
title: Настройка DNS-записей для пула переднего плана или сервера Standard Edition
description: Настроить записи DNS для интерфейса пула и сервера Standard Edition.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure DNS records for a Front End pool or Standard Edition server
ms:assetid: 02871f2f-6c99-49e6-b441-cd21b16d38ee
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398079(v=OCS.15)
ms:contentKeyID: 48183244
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3b41bddc147c8d95dde0f9c0db129574fb87f38c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399886"
---
# <a name="configure-dns-records-in-lync-server-2013-for-a-front-end-pool-or-standard-edition-server"></a><span data-ttu-id="6c8f4-103">Настройка DNS-записей в Lync Server 2013 для пула переднего плана или сервера Standard Edition</span><span class="sxs-lookup"><span data-stu-id="6c8f4-103">Configure DNS records in Lync Server 2013 for a Front End pool or Standard Edition server</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6c8f4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6c8f4-104">

<span> </span></span></span>

<span data-ttu-id="6c8f4-105">_**Тема последнего изменения:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="6c8f4-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="6c8f4-106">Lync Server 2013 использует систему доменных имен (DNS), чтобы регистрировать и поддерживать записи для правильного доменного имени в разрешении IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="6c8f4-106">Lync Server 2013 uses the Domain Name System (DNS) to register and maintain records for proper domain name to IP address resolution.</span></span> <span data-ttu-id="6c8f4-107">Прежде чем приступать к работе с сервером Standard Edition или пулом переднего плана, необходимо настроить необходимые записи DNS для развертывания.</span><span class="sxs-lookup"><span data-stu-id="6c8f4-107">You need to configure required DNS records for your deployment prior to operating the Standard Edition server or Front End pool.</span></span> <span data-ttu-id="6c8f4-108">Ниже приведены ссылки на рекомендации о том, какие записи необходимо создавать для обеспечения правильного функционирования Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6c8f4-108">The following links will provide guidance on what records need to be created to allow for the proper operation of Lync Server 2013.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="6c8f4-109">Содержание</span><span class="sxs-lookup"><span data-stu-id="6c8f4-109">In This Section</span></span>

  - [<span data-ttu-id="6c8f4-110">Настройка DNS для балансировки нагрузки в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6c8f4-110">Configure DNS for load balancing in Lync Server 2013</span></span>](lync-server-2013-configure-dns-for-load-balancing.md)

  - [<span data-ttu-id="6c8f4-111">Настройка записей узлов DNS для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6c8f4-111">Configure DNS Host records for Lync Server 2013</span></span>](lync-server-2013-configure-dns-host-records.md)

  - [<span data-ttu-id="6c8f4-112">Создание и проверка записей DNS SRV в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6c8f4-112">Create and verify DNS SRV records in Lync Server 2013</span></span>](lync-server-2013-create-and-verify-dns-srv-records.md)

<span data-ttu-id="6c8f4-113"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6c8f4-113"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

