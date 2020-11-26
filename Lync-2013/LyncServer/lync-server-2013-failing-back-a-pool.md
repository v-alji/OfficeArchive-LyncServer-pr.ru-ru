---
title: 'Lync Server 2013: отработка отказа для пула'
description: 'Lync Server 2013: сбой обратной связи с пулом.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Failing back a pool
ms:assetid: 6232b644-ef57-4c9c-abec-14ff8ffc9fe7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204945(v=OCS.15)
ms:contentKeyID: 48184289
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1c1fc0ea4514d2f951dd936521590d47b809db38
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428330"
---
# <a name="failing-back-a-pool-in-lync-server-2013"></a><span data-ttu-id="1f44c-103">Отработка отказа для пула в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1f44c-103">Failing back a pool in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1f44c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1f44c-104">

<span> </span></span></span>

<span data-ttu-id="1f44c-105">_**Тема последнего изменения:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="1f44c-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="1f44c-106">После того как пул, в котором произошел сбой, перейдет в оперативный режим (то есть Pool1 в этом примере), выполните указанные ниже действия, чтобы восстановить состояние развертывания для обычного рабочего состояния.</span><span class="sxs-lookup"><span data-stu-id="1f44c-106">After the pool that experienced the disaster is back online (that is, Pool1 in this example), take the following steps to restore your deployment to regular working status.</span></span>

<span data-ttu-id="1f44c-107">Обратите внимание, что процесс восстановления после сбоя занимает несколько минут.</span><span class="sxs-lookup"><span data-stu-id="1f44c-107">Note that the failback process takes several minute to complete.</span></span>  <span data-ttu-id="1f44c-108">Следует исходить из длительности 60 минут для пула, в котором работает 20 000 пользователей.</span><span class="sxs-lookup"><span data-stu-id="1f44c-108">For reference, it is expected to take up to 60 minutes for a pool of 20,000 users.</span></span>

1.  <span data-ttu-id="1f44c-109">Не изменяйте пользователей, которые изначально были размещены в Pool1, и произошел сбой при переходе на Pool2, введя следующий командлет:</span><span class="sxs-lookup"><span data-stu-id="1f44c-109">Fail back the users who were originally homed in Pool1 and have been failed over to Pool2 by typing the following cmdlet:</span></span>
    
        Invoke-CsPoolFailback -PoolFQDN <Pool1 FQDN> -Verbose

<span data-ttu-id="1f44c-110">Никаких других действий не требуется.</span><span class="sxs-lookup"><span data-stu-id="1f44c-110">No other steps are necessary.</span></span> <span data-ttu-id="1f44c-111">Если вы отошел сбой на центральном сервере управления, вы можете оставить его в Pool2.</span><span class="sxs-lookup"><span data-stu-id="1f44c-111">If you failed over the Central Management Server, you can leave it in Pool2.</span></span>

<span data-ttu-id="1f44c-112"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1f44c-112"></div>

<span> </span>

</div>

</div>

</span></span></div>

