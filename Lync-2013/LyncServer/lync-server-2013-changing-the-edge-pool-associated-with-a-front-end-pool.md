---
title: 'Lync Server 2013: изменение пограничного пула, связанного с пулом переднего плана'
description: 'Lync Server 2013: изменение пула EDGE, связанного с пулом переднего плана.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Changing the Edge pool associated with a Front End pool
ms:assetid: 369468c7-2c0b-48cc-bbc3-825dad7b85aa
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688023(v=OCS.15)
ms:contentKeyID: 49733613
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ab22ba35420341e291d51a1ff012459840e63a56
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435049"
---
# <a name="changing-the-edge-pool-associated-with-a-front-end-pool-in-lync-server-2013"></a><span data-ttu-id="7db4c-103">Изменение пограничного пула, связанного с пулом переднего плана в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7db4c-103">Changing the Edge pool associated with a Front End pool in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7db4c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7db4c-104">

<span> </span></span></span>

<span data-ttu-id="7db4c-105">_**Тема последнего изменения:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="7db4c-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="7db4c-106">Если пул пограничного пула отключается, но пул переднего плана на этом же сайте по-прежнему работает, вы должны настроить интерфейс пула на использование пограничного пула на другом сайте, пока не произойдет восстановление пула Edge.</span><span class="sxs-lookup"><span data-stu-id="7db4c-106">If an Edge pool goes down but the Front End pool at the same site is still running, you will need to set the Front End pool to use an Edge pool at a different site until the failed Edge pool is restored.</span></span>

<div>

## <a name="changing-the-edge-pool-associated-with-a-front-end-pool"></a><span data-ttu-id="7db4c-107">Изменение пула EDGE, связанного с пулом переднего плана</span><span class="sxs-lookup"><span data-stu-id="7db4c-107">Changing the Edge Pool Associated with a Front End Pool</span></span>

1.  <span data-ttu-id="7db4c-108">В построителе топологии найдите имя пула переднего плана, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="7db4c-108">In Topology Builder, navigate to the name of the Front End pool you need to change.</span></span>

2.  <span data-ttu-id="7db4c-109">Щелкните пул правой кнопкой мыши и выберите команду **изменить свойства**.</span><span class="sxs-lookup"><span data-stu-id="7db4c-109">Right-click the pool, and then click **Edit Properties**.</span></span>

3.  <span data-ttu-id="7db4c-110">В разделе **связи** в группе **сопоставление краевого пула (для компонентов мультимедиа)** выберите в раскрывающемся списке пул краев, который вы хотите связать с этим пулом переднего плана.</span><span class="sxs-lookup"><span data-stu-id="7db4c-110">In the **Associations** section, under **Associate Edge Pool (for media components)**, use the drop down box to select the Edge pool you want to associate this Front End pool with.</span></span>

4.  <span data-ttu-id="7db4c-111">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="7db4c-111">Click **OK**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="7db4c-112">См. также</span><span class="sxs-lookup"><span data-stu-id="7db4c-112">See Also</span></span>


[<span data-ttu-id="7db4c-113">Аварийное восстановление пограничного сервера в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7db4c-113">Edge Server disaster recovery in Lync Server 2013</span></span>](lync-server-2013-edge-server-disaster-recovery.md)  
  

<span data-ttu-id="7db4c-114"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7db4c-114"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

