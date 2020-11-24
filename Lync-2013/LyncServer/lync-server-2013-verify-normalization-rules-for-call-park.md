---
title: 'Lync Server 2013: Проверка правил нормализации для приостановки звонка'
description: 'Lync Server 2013: Проверка правил нормализации для приостановки звонка.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Verify normalization rules for Call Park
ms:assetid: deaa170f-041e-45cb-8eab-f02931ab541e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398981(v=OCS.15)
ms:contentKeyID: 48185646
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2ac4c15091141e3069e7b77533d0e4148459f570
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399760"
---
# <a name="verify-normalization-rules-for-call-park-in-lync-server-2013"></a><span data-ttu-id="78022-103">Проверка правил нормализации для парковки звонков в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="78022-103">Verify normalization rules for Call Park in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="78022-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="78022-104">

<span> </span></span></span>

<span data-ttu-id="78022-105">_**Тема последнего изменения:** 2012-09-11_</span><span class="sxs-lookup"><span data-stu-id="78022-105">_**Topic Last Modified:** 2012-09-11_</span></span>

<span data-ttu-id="78022-106">Орбиты для приостановки звонка не должны быть нормализованы.</span><span class="sxs-lookup"><span data-stu-id="78022-106">Call Park orbits must not be normalized.</span></span> <span data-ttu-id="78022-107">Check your dial plans to be sure that your orbit numbers are not normalized.</span><span class="sxs-lookup"><span data-stu-id="78022-107">Check your dial plans to be sure that your orbit numbers are not normalized.</span></span> <span data-ttu-id="78022-108">Если необходимо создать дополнительное правило нормализации, чтобы не допустить нормализации, выполните действия, описанные в разделе [Создание абонентской группы в Lync Server 2013](lync-server-2013-create-a-dial-plan.md) , чтобы определить новое правило нормализации, чтобы **шаблон соответствовал** диапазону орбиты, а **шаблон перевода** — **$1**.</span><span class="sxs-lookup"><span data-stu-id="78022-108">If you must create an additional normalization rule to prevent your orbits from being normalized, follow the procedure in [Create a dial plan in Lync Server 2013](lync-server-2013-create-a-dial-plan.md) to define a new normalization rule, so that **Pattern to match** identifies the orbit range and **Translation pattern** is **$1**.</span></span> <span data-ttu-id="78022-109">Например, если диапазон на повороте на поворот по орбите равен 7000 – 7999, **шаблон соответствует** **^ (7 \\ d {3} ) $** , а **шаблон перевода** — **$1**.</span><span class="sxs-lookup"><span data-stu-id="78022-109">For example, if your Call Park orbit range is 7000 – 7999, the **Pattern to match** is **^(7\\d{3})$** and **Translation pattern** is **$1**.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="78022-110">Be sure that the default normalization rule in your dial plans does not contain <STRONG>^(\d\*)</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="78022-110">Be sure that the default normalization rule in your dial plans does not contain <STRONG>^(\d\*)</STRONG>.</span></span> <span data-ttu-id="78022-111">В противном случае правило нормализации для приостановки вызова никогда не будет выполняться.</span><span class="sxs-lookup"><span data-stu-id="78022-111">Otherwise, your Call Park normalization rule will never run.</span></span>



</div>

<div>

## <a name="see-also"></a><span data-ttu-id="78022-112">См. также</span><span class="sxs-lookup"><span data-stu-id="78022-112">See Also</span></span>


[<span data-ttu-id="78022-113">Создание абонентской группы в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="78022-113">Create a dial plan in Lync Server 2013</span></span>](lync-server-2013-create-a-dial-plan.md)  
  

<span data-ttu-id="78022-114"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="78022-114"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

