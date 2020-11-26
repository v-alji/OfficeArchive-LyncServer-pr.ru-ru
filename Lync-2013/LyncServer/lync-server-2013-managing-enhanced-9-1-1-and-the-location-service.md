---
title: 'Lync Server 2013: управление службой Enhanced 9-1-1 и службой расположения'
description: 'Lync Server 2013: Управление расширенными 9-1-1ми и служба расположения.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing Enhanced 9-1-1 and the Location service
ms:assetid: 307c5aeb-9917-46a2-a95d-de30dea27beb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688012(v=OCS.15)
ms:contentKeyID: 49733600
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 942d7780a54d7e61052469410a1c03943babd56f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437478"
---
# <a name="managing-enhanced-9-1-1-and-the-location-service-in-lync-server-2013"></a><span data-ttu-id="9eaa8-103">Управление службой Enhanced 9-1-1 и службой расположения в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9eaa8-103">Managing Enhanced 9-1-1 and the Location service in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9eaa8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9eaa8-104">

<span> </span></span></span>

<span data-ttu-id="9eaa8-105">_**Тема последнего изменения:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="9eaa8-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="9eaa8-106">Lync Server 2013 поддерживает вызов улучшенных 9-1-1 (E9-1-1) на клиентах Lync и устройствах Lync Phone Edition.</span><span class="sxs-lookup"><span data-stu-id="9eaa8-106">Lync Server 2013 supports Enhanced 9-1-1 (E9-1-1) calling from Lync clients and Lync Phone Edition devices.</span></span> <span data-ttu-id="9eaa8-107">Если вы настроили Lync Server 2013 для E9-1-1, экстренные вызовы, размещенные в Lync 2013 или Lync Phone Edition, включают в себя сведения о местоположении ответа на аварийную информацию (ERL) из базы данных службы сведений о расположении.</span><span class="sxs-lookup"><span data-stu-id="9eaa8-107">When you configure Lync Server 2013 for E9-1-1, emergency calls placed from Lync 2013 or Lync Phone Edition include Emergency Response Location (ERL) information from the Location Information service database.</span></span> <span data-ttu-id="9eaa8-108">С помощью описанных в этом разделе процедур можно управлять политикой расположения.</span><span class="sxs-lookup"><span data-stu-id="9eaa8-108">Use the procedures in this section to manage location policy.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="9eaa8-109">Подробнее о том, как развертывать дополнительные функции голосовой связи, такие как E9-1-1 и служба сведений о местоположении, можно узнать <A href="lync-server-2013-deploying-advanced-enterprise-voice-features.md">в разделе развертывание расширенных функций голосовой связи в Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="9eaa8-109">For details on deploying advanced Enterprise Voice features, such as E9-1-1 and the Location Information service, see <A href="lync-server-2013-deploying-advanced-enterprise-voice-features.md">Deploying advanced Enterprise Voice features in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="9eaa8-110">Содержание</span><span class="sxs-lookup"><span data-stu-id="9eaa8-110">In This Section</span></span>

  - [<span data-ttu-id="9eaa8-111">Управление политикой расположения в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9eaa8-111">Managing location policy in Lync Server 2013</span></span>](lync-server-2013-managing-location-policy.md)

<span data-ttu-id="9eaa8-112"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9eaa8-112"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

