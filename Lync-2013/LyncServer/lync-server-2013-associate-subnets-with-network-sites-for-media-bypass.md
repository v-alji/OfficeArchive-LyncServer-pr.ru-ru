---
title: 'Lync Server 2013: связывание подсетей с сетевыми сайтами для обхода мультимедиа'
description: 'Lync Server 2013: сопоставьте подсети с сетевыми сайтами для обхода мультимедиа.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Associate subnets with network sites for media bypass
ms:assetid: 5bc632b7-1446-470f-b332-48ea0ca4d1fd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398401(v=OCS.15)
ms:contentKeyID: 48184244
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ee03b51d29a88ff634cb87385c5889c35acd8884
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399955"
---
# <a name="associate-subnets-with-network-sites-for-media-bypass-in-lync-server-2013"></a><span data-ttu-id="9bb53-103">Связывание подсетей с сетевыми сайтами для обхода мультимедиа в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9bb53-103">Associate subnets with network sites for media bypass in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9bb53-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9bb53-104">

<span> </span></span></span>

<span data-ttu-id="9bb53-105">_**Тема последнего изменения:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="9bb53-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="9bb53-106">В этой статье предполагается, что вы настроили обход глобальных параметров в мультимедиа и что вы настроили сетевой регион и сетевые сайты для обхода мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="9bb53-106">This topic assumes that you have configured media bypass global settings and that you have configured network region and network sites for media bypass.</span></span>



</div>

<span data-ttu-id="9bb53-107">Каждая подсеть в сети должна быть связана с определенным сетевым сайтом.</span><span class="sxs-lookup"><span data-stu-id="9bb53-107">Every subnet in your network must be associated with a specific network site.</span></span> <span data-ttu-id="9bb53-108">Это связано с тем, что сведения о подсети используются для определения сетевого сайта, на котором находится конечная точка.</span><span class="sxs-lookup"><span data-stu-id="9bb53-108">This is because subnet information is used to determine the network site on which an endpoint is located.</span></span> <span data-ttu-id="9bb53-109">Если в сеансе известны расположение обеих сторон сеанса, обход мультимедиа может определять, куда отправлять мультимедиа для обработки.</span><span class="sxs-lookup"><span data-stu-id="9bb53-109">When the locations of both parties in a session are known, media bypass can determine where to send media for processing.</span></span>

<span data-ttu-id="9bb53-110">В пропуске мультимедиа отсутствуют особые требования для сопоставления подсетей с сетевыми сайтами.</span><span class="sxs-lookup"><span data-stu-id="9bb53-110">Media bypass does not have any special requirements for associating subnets with network sites.</span></span> <span data-ttu-id="9bb53-111">Чтобы создать связь между подсетями и сетевыми сайтами в вашей топологии, выполните действия, описанные в разделе [связывание подсети с сетевым сайтом в Lync Server 2013](lync-server-2013-associate-a-subnet-with-a-network-site.md).</span><span class="sxs-lookup"><span data-stu-id="9bb53-111">To create an association between the subnets and network sites in your topology, follow the procedures in [Associate a subnet with a network site in Lync Server 2013](lync-server-2013-associate-a-subnet-with-a-network-site.md).</span></span>

<div>

## <a name="next-steps-create-bandwidth-policy-profiles"></a><span data-ttu-id="9bb53-112">Дальнейшие действия: создание профилей политики пропускной способности</span><span class="sxs-lookup"><span data-stu-id="9bb53-112">Next Steps: Create Bandwidth Policy Profiles</span></span>

<span data-ttu-id="9bb53-113">После связывания подсетей с сетевыми сайтами для обхода мультимедиа необходимо создать один или несколько профилей политики пропускной способности, которые будут разбивать подсети на разделы с хорошим подключением и без них, в целях обхода мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="9bb53-113">After you associate subnets with network sites for media bypass, you must create one or more bandwidth policy profiles that will partition subnets into those with good connectivity and those without, for the purposes of media bypass.</span></span> <span data-ttu-id="9bb53-114">Все подсети в сетевом регионе с сетевыми сайтами, не имеющими ограничений пропускной способности, имеют хорошее соединение и, следовательно, такие подсети могут использовать обход мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="9bb53-114">All subnets within a network region with network sites that do not have bandwidth constraints have good connectivity, and, therefore, those subnets can use media bypass.</span></span>

<span data-ttu-id="9bb53-115">Инструкции по настройке профилей политики пропускной способности описаны [в разделе Создание профилей политики пропускной способности в Lync Server 2013](lync-server-2013-create-bandwidth-policy-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="9bb53-115">For procedures to configure bandwidth policy profiles, see [Create bandwidth policy profiles in Lync Server 2013](lync-server-2013-create-bandwidth-policy-profiles.md).</span></span>

<span data-ttu-id="9bb53-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9bb53-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

