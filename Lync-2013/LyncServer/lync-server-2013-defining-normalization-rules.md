---
title: 'Lync Server 2013: определение правил нормализации'
description: 'Lync Server 2013: определение правил нормализации.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Defining normalization rules
ms:assetid: ed31d56c-00b5-4f72-bd9f-beb4100d441f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399071(v=OCS.15)
ms:contentKeyID: 48185741
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3a123e17b1d3256781ff34e4cade2b344ba8fe14
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430996"
---
# <a name="defining-normalization-rules-in-lync-server-2013"></a><span data-ttu-id="1092a-103">Определение правил нормализации в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1092a-103">Defining normalization rules in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1092a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1092a-104">

<span> </span></span></span>

<span data-ttu-id="1092a-105">_**Тема последнего изменения:** 2014-04-22_</span><span class="sxs-lookup"><span data-stu-id="1092a-105">_**Topic Last Modified:** 2014-04-22_</span></span>

<span data-ttu-id="1092a-106">В правилах нормализации Lync Server 2013 используются регулярные выражения .NET Framework для перевода телефонных номеров с набором в формат E. 164. другими словами, правила нормализации принимают номер телефона, набранный пользователем, и преобразуют его в формат, используемый приложением Lync Server для внутренних целей.</span><span class="sxs-lookup"><span data-stu-id="1092a-106">Lync Server 2013 normalization rules use .NET Framework regular expressions to translate dialed phone numbers to E.164 format; in other words, normalization rules take the phone number dialed by a user and convert that number to the format used internally by Lync Server.</span></span> <span data-ttu-id="1092a-107">Каждой абонентской группе должно быть назначено хотя бы одно правило нормализации.</span><span class="sxs-lookup"><span data-stu-id="1092a-107">Each dial plan must be assigned one or more normalization rules.</span></span>

<span data-ttu-id="1092a-108">Дополнительные сведения о правилах нормализации приведены [в разделе планы и правила нормализации в Lync Server 2013](lync-server-2013-dial-plans-and-normalization-rules.md) в документации по планированию.</span><span class="sxs-lookup"><span data-stu-id="1092a-108">For details about normalization rules, see [Dial plans and normalization rules in Lync Server 2013](lync-server-2013-dial-plans-and-normalization-rules.md) in the Planning documentation.</span></span>

<span data-ttu-id="1092a-109">Сведения о том, как создавать регулярные выражения, приведены в разделе "регулярные выражения .NET Framework" [https://go.microsoft.com/fwlink/p/?linkId=140927](https://go.microsoft.com/fwlink/p/?linkid=140927) .</span><span class="sxs-lookup"><span data-stu-id="1092a-109">For details about how to write regular expressions, see ".NET Framework Regular Expressions" at [https://go.microsoft.com/fwlink/p/?linkId=140927](https://go.microsoft.com/fwlink/p/?linkid=140927).</span></span>

<span data-ttu-id="1092a-110">Чтобы определить или изменить правило нормализации, можно использовать один из указанных ниже способов.</span><span class="sxs-lookup"><span data-stu-id="1092a-110">You can use either of the following methods to define or edit a normalization rule:</span></span>

  - <span data-ttu-id="1092a-111">С помощью средства **создания правил нормализации** укажите значения для начальных цифр, длину, цифр для удаления и цифр, которые нужно добавить, а затем откройте на панели управления Lync Server соответствующие шаблон сопоставления и правило перевода.</span><span class="sxs-lookup"><span data-stu-id="1092a-111">Use the **Build a Normalization Rule** tool to specify values for the starting digits, length, digits to remove and digits to add, and then let Lync Server Control Panel generate the corresponding matching pattern and translation rule for you.</span></span>

  - <span data-ttu-id="1092a-112">Напишите регулярные выражения вручную, чтобы задать шаблон сопоставления и правило трансляции.</span><span class="sxs-lookup"><span data-stu-id="1092a-112">Write regular expressions manually to define the matching pattern and translation rule.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="1092a-113">Содержание</span><span class="sxs-lookup"><span data-stu-id="1092a-113">In This Section</span></span>

  - [<span data-ttu-id="1092a-114">Создание и изменение правила нормализации с помощью сборки правила нормализации в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1092a-114">Create or modify a normalization rule by using Build a Normalization Rule in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-normalization-rule-by-using-build-a-normalization-rule.md)

  - [<span data-ttu-id="1092a-115">Создание или изменение правила нормализации вручную в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1092a-115">Create or modify a normalization rule manually in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-normalization-rule-manually.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="1092a-116">См. также</span><span class="sxs-lookup"><span data-stu-id="1092a-116">See Also</span></span>


[<span data-ttu-id="1092a-117">Создание абонентской группы в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1092a-117">Create a dial plan in Lync Server 2013</span></span>](lync-server-2013-create-a-dial-plan.md)  
[<span data-ttu-id="1092a-118">Изменение абонентской группы в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1092a-118">Modify a dial plan in Lync Server 2013</span></span>](lync-server-2013-modify-a-dial-plan.md)  
  

<span data-ttu-id="1092a-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1092a-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

