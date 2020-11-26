---
title: 'Lync Server 2013: настройка брандмауэров и портов для доступа внешних пользователей'
description: 'Lync Server 2013: Настройка брандмауэров и портов для внешнего доступа пользователей.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure firewalls and ports for external user access
ms:assetid: cacb3832-f8db-4009-bfcf-6f5c15c236ed
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398848(v=OCS.15)
ms:contentKeyID: 48185430
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 68ccb382c3b3632b113b2b0a36846500700c1b9f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433971"
---
# <a name="configure-firewalls-and-ports-for-external-user-access-in-lync-server-2013"></a><span data-ttu-id="3dc40-103">Настройка брандмауэров и портов для доступа внешних пользователей в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3dc40-103">Configure firewalls and ports for external user access in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3dc40-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3dc40-104">

<span> </span></span></span>

<span data-ttu-id="3dc40-105">_**Тема последнего изменения:** 2012-05-21_</span><span class="sxs-lookup"><span data-stu-id="3dc40-105">_**Topic Last Modified:** 2012-05-21_</span></span>

<span data-ttu-id="3dc40-106">Чтобы настроить брандмауэры и порты, необходимо настроить их для пограничных серверов, обратного прокси-сервера и подсистемы балансировки нагрузки для оборудования (для масштабируемого развертывания без использования балансировки нагрузки DNS).</span><span class="sxs-lookup"><span data-stu-id="3dc40-106">To configure firewalls and ports, you need to configure them for Edge Servers, reverse proxy servers, and possibly hardware load balancers (for a scaled deployment that does not use DNS load balancing).</span></span> <span data-ttu-id="3dc40-107">В этом разделе приводятся сведения о требованиях к брандмауэру и порту для всех компонентов пограничного сервера и конфигурации портов брандмауэра для пограничных серверов.</span><span class="sxs-lookup"><span data-stu-id="3dc40-107">This section provides information about firewall and port requirements for all Edge Server components and the configuration of firewall ports for Edge Servers.</span></span> <span data-ttu-id="3dc40-108">Дополнительные сведения о настройке портов для обратного прокси-сервера приведены в разделе [Настройка обратного прокси-сервера для Lync Server 2013](lync-server-2013-setting-up-reverse-proxy-servers.md).</span><span class="sxs-lookup"><span data-stu-id="3dc40-108">For details about configuring ports for reverse proxy servers, see [Setting up reverse proxy servers for Lync Server 2013](lync-server-2013-setting-up-reverse-proxy-servers.md).</span></span> <span data-ttu-id="3dc40-109">Если вы разворачиваете топологию с масштабированием и планируете использовать аппаратную балансировку нагрузки вместо балансировки нагрузки DNS, ознакомьтесь [с масштабируемым консолидированным краем с аппаратным балансировщикм нагрузки в Lync Server 2013](lync-server-2013-scaled-consolidated-edge-with-hardware-load-balancers.md) в документации по планированию для получения подробных сведений о настройке портов для подсистемы балансировки нагрузки для оборудования.</span><span class="sxs-lookup"><span data-stu-id="3dc40-109">If you are deploying a scaled edge topology and are using hardware load balancing instead of DNS load balancing, see [Scaled consolidated edge with hardware load balancers in Lync Server 2013](lync-server-2013-scaled-consolidated-edge-with-hardware-load-balancers.md) in the Planning documentation for details about configuring ports for hardware load balancers.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="3dc40-110">См. также</span><span class="sxs-lookup"><span data-stu-id="3dc40-110">See Also</span></span>


[<span data-ttu-id="3dc40-111">Определение требований к внешнему брандмауэру аудио- и видеосвязи и портам для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3dc40-111">Determine external A/V firewall and port requirements for Lync Server 2013</span></span>](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md)  
  

<span data-ttu-id="3dc40-112"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3dc40-112"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

