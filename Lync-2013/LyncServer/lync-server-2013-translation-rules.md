---
title: 'Lync Server 2013: правила перевода'
description: 'Lync Server 2013: правила перевода.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Translation rules
ms:assetid: 6e067bd4-4931-4385-81ac-2acae45a16d8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398520(v=OCS.15)
ms:contentKeyID: 48184460
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 65ee21459123ea09f54eb52e65a4d9ecba61c386
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49397873"
---
# <a name="translation-rules-in-lync-server-2013"></a><span data-ttu-id="6303e-103">Правила перевода в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6303e-103">Translation rules in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6303e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6303e-104">

<span> </span></span></span>

<span data-ttu-id="6303e-105">_**Тема последнего изменения:** 2012-10-05_</span><span class="sxs-lookup"><span data-stu-id="6303e-105">_**Topic Last Modified:** 2012-10-05_</span></span>

<span data-ttu-id="6303e-106">Для Lync Server 2013 Enterprise Voice требуется, чтобы все строки набора номера были нормализованы в формат E. 164 для целей обратного просмотра номера (RNL).</span><span class="sxs-lookup"><span data-stu-id="6303e-106">Lync Server 2013 Enterprise Voice requires that all dial strings be normalized to E.164 format for the purpose of performing reverse number lookup (RNL).</span></span> <span data-ttu-id="6303e-107">В Microsoft Lync Server 2010 правила перевода поддерживаются только для вызываемых номеров.</span><span class="sxs-lookup"><span data-stu-id="6303e-107">In Microsoft Lync Server 2010, translation rules are supported only for called numbers.</span></span> <span data-ttu-id="6303e-108">Новые возможности Microsoft Lync Server 2013 для звонков также поддерживаются правила перевода.</span><span class="sxs-lookup"><span data-stu-id="6303e-108">New in Microsoft Lync Server 2013, translation rules are also supported for calling numbers.</span></span> <span data-ttu-id="6303e-109">Для *магистрального однорангового узла* (т.е. связанного шлюза, УАТС или SIP-канала) может потребоваться, чтобы номера были в формате местного набора.</span><span class="sxs-lookup"><span data-stu-id="6303e-109">The *trunk peer* (that is, the associated gateway, private branch exchange (PBX), or SIP trunk) may require that numbers be in a local dialing format.</span></span> <span data-ttu-id="6303e-110">Чтобы преобразовать номера из формата E.164 в формат местного набора, вы можете установить правила преобразования для работы с URI запроса перед его направлением в магистральный узел.</span><span class="sxs-lookup"><span data-stu-id="6303e-110">To translate numbers from E.164 format to a local dialing format, you can define one or more translation rules to manipulate the request URI before you route it to the trunk peer.</span></span> <span data-ttu-id="6303e-111">Например, можно написать правило преобразования, чтобы заменить +44 в начале строки набора на 0144.</span><span class="sxs-lookup"><span data-stu-id="6303e-111">For example, you could write a translation rule to remove +44 from the beginning of a dial string and replace it with 0144.</span></span>

<span data-ttu-id="6303e-112">Выполняя преобразование исходящего маршрута на сервере, вы можете снизить требования конфигурации в каждом отдельном магистральном узле для трансляции телефонных номеров в формат местного набора.</span><span class="sxs-lookup"><span data-stu-id="6303e-112">By performing outbound route translation on the server, you can reduce the configuration requirements on each individual trunk peer in order to translate phone numbers into a local dialing format.</span></span> <span data-ttu-id="6303e-113">При планировании выбора шлюзов и количества шлюзов, связанных с определенным кластером серверов обновлений, может быть полезно сгруппировать одноранговые узлы с использованием одинаковых местных требований для набора номера.</span><span class="sxs-lookup"><span data-stu-id="6303e-113">When you plan which gateways, and how many gateways, to associate with a specific Mediation Server cluster, it may be useful to group trunk peers with similar local dialing requirements.</span></span> <span data-ttu-id="6303e-114">Это позволяет сократить количество необходимых правил преобразования и сэкономить время, затрачиваемое на их создание.</span><span class="sxs-lookup"><span data-stu-id="6303e-114">This can reduce the number of required translation rules and the time it takes to write them.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="6303e-115">Связывание одного или нескольких правил трансляции с конфигурацией магистрали корпоративной голосовой связи следует использовать в качестве альтернативы настройке правил перевода на магистральном одноранговом узле.</span><span class="sxs-lookup"><span data-stu-id="6303e-115">Associating one or more translation rules with an Enterprise Voice trunk configuration should be used as an alternative to configuring translation rules on the trunk peer.</span></span> <span data-ttu-id="6303e-116">Не применяйте правила перевода с конфигурацией корпоративной магистрали, если вы настроили правила трансляции для однорангового канала, так как эти правила могут конфликтовать.</span><span class="sxs-lookup"><span data-stu-id="6303e-116">Do not associate translation rules with an Enterprise Voice trunk configuration if you have configured translation rules on the trunk peer, because the two rules might conflict.</span></span>



</div>

<div>

## <a name="example-translation-rules"></a><span data-ttu-id="6303e-117">Примеры правил преобразования</span><span class="sxs-lookup"><span data-stu-id="6303e-117">Example Translation Rules</span></span>

<span data-ttu-id="6303e-118">Следующие примеры правил преобразования показывают, как можно разрабатывать правила на сервере для преобразования номеров из формата E.164 в местный формат для магистрального узла.</span><span class="sxs-lookup"><span data-stu-id="6303e-118">The following examples of translation rules show how you can develop rules on the server to translate numbers from E.164 format to a local format for the trunk peer.</span></span>

<span data-ttu-id="6303e-119">Подробнее о том, как применять правила перевода, можно найти [в разделе Определение правил перевода в Lync Server 2013](lync-server-2013-defining-translation-rules.md) в документации по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="6303e-119">For details about how to implement translation rules, see [Defining translation rules in Lync Server 2013](lync-server-2013-defining-translation-rules.md) in the Deployment documentation.</span></span>


<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6303e-120">Описание</span><span class="sxs-lookup"><span data-stu-id="6303e-120">Description</span></span></th>
<th><span data-ttu-id="6303e-121">Цифры в начале</span><span class="sxs-lookup"><span data-stu-id="6303e-121">Starting Digits</span></span></th>
<th><span data-ttu-id="6303e-122">Длина</span><span class="sxs-lookup"><span data-stu-id="6303e-122">Length</span></span></th>
<th><span data-ttu-id="6303e-123">Цифры для удаления</span><span class="sxs-lookup"><span data-stu-id="6303e-123">Digits to Remove</span></span></th>
<th><span data-ttu-id="6303e-124">Цифры для добавления</span><span class="sxs-lookup"><span data-stu-id="6303e-124">Digits to Add</span></span></th>
<th><span data-ttu-id="6303e-125">Шаблон соответствия</span><span class="sxs-lookup"><span data-stu-id="6303e-125">Matching Pattern</span></span></th>
<th><span data-ttu-id="6303e-126">Преобразование</span><span class="sxs-lookup"><span data-stu-id="6303e-126">Translation</span></span></th>
<th><span data-ttu-id="6303e-127">Пример</span><span class="sxs-lookup"><span data-stu-id="6303e-127">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6303e-128">Обычный междугородний звонок в США</span><span class="sxs-lookup"><span data-stu-id="6303e-128">Conventional long-distance dialing in U.S.</span></span></p>
<p><span data-ttu-id="6303e-129">(убирается ‘+’)</span><span class="sxs-lookup"><span data-stu-id="6303e-129">(strip out the ‘+’)</span></span></p></td>
<td><p><span data-ttu-id="6303e-130">+1</span><span class="sxs-lookup"><span data-stu-id="6303e-130">+1</span></span></p></td>
<td><p><span data-ttu-id="6303e-131">Ровно 12</span><span class="sxs-lookup"><span data-stu-id="6303e-131">Exactly 12</span></span></p></td>
<td><p><span data-ttu-id="6303e-132">1</span><span class="sxs-lookup"><span data-stu-id="6303e-132">1</span></span></p></td>
<td><p><span data-ttu-id="6303e-133">до</span><span class="sxs-lookup"><span data-stu-id="6303e-133">0</span></span></p></td>
<td><p><span data-ttu-id="6303e-134">^\+(1 \ d {10} ) $</span><span class="sxs-lookup"><span data-stu-id="6303e-134">^\+(1\d{10})$</span></span></p></td>
<td><p><span data-ttu-id="6303e-135">$1</span><span class="sxs-lookup"><span data-stu-id="6303e-135">$1</span></span></p></td>
<td><p><span data-ttu-id="6303e-136">+14255551010 преобразуется в 14255551010</span><span class="sxs-lookup"><span data-stu-id="6303e-136">+14255551010 becomes 14255551010</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6303e-137">Международный звонок из США</span><span class="sxs-lookup"><span data-stu-id="6303e-137">U.S. international long-distance dialing</span></span></p>
<p><span data-ttu-id="6303e-138">(убирается "+" и добавляются цифры 011)</span><span class="sxs-lookup"><span data-stu-id="6303e-138">(strip out ‘+’ and add 011)</span></span></p></td>
<td><p>+</p></td>
<td><p><span data-ttu-id="6303e-139">Не менее 11</span><span class="sxs-lookup"><span data-stu-id="6303e-139">At least 11</span></span></p></td>
<td><p><span data-ttu-id="6303e-140">1</span><span class="sxs-lookup"><span data-stu-id="6303e-140">1</span></span></p></td>
<td><p><span data-ttu-id="6303e-141">011</span><span class="sxs-lookup"><span data-stu-id="6303e-141">011</span></span></p></td>
<td><p><span data-ttu-id="6303e-142">^\+(\d {9} \d +) $</span><span class="sxs-lookup"><span data-stu-id="6303e-142">^\+(\d{9}\d+)$</span></span></p></td>
<td><p><span data-ttu-id="6303e-143">011$1</span><span class="sxs-lookup"><span data-stu-id="6303e-143">011$1</span></span></p></td>
<td><p><span data-ttu-id="6303e-144">+441235551010 преобразуется в 011441235551010</span><span class="sxs-lookup"><span data-stu-id="6303e-144">+441235551010 becomes 011441235551010</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="6303e-145">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6303e-145">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

