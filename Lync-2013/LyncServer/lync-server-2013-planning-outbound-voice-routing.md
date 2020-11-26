---
title: 'Lync Server 2013: планирование маршрутизации исходящей голосовой почты'
description: 'Lync Server 2013: Планирование исходящей голосовой маршрутизации.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning outbound voice routing
ms:assetid: 37c55fa4-175a-4190-b9e4-c2e5ac7b9261
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425853(v=OCS.15)
ms:contentKeyID: 48183835
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 057f81b995e231c2025a9fcb07e675086a662efe
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442854"
---
# <a name="planning-outbound-voice-routing-in-lync-server-2013"></a><span data-ttu-id="51096-103">Планирование маршрутизации исходящей голосовой почты в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="51096-103">Planning outbound voice routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="51096-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="51096-104">

<span> </span></span></span>

<span data-ttu-id="51096-105">_**Тема последнего изменения:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="51096-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="51096-106">Маршрутизация исходящих вызовов применяется к вызовам, которые предназначены для шлюза коммутируемой телефонной сети (PSTN), магистрального канала или частного обмена филиалами (АТС).</span><span class="sxs-lookup"><span data-stu-id="51096-106">Outbound call routing applies to calls that are destined for a public switched telephone network (PSTN) gateway, trunk, or private branch exchange (PBX).</span></span> <span data-ttu-id="51096-107">Когда пользователь попытается позвонить, сервер нормализует номер телефона на формат E. 164, если необходимо, и пытается сопоставить его с URI SIP.</span><span class="sxs-lookup"><span data-stu-id="51096-107">When a user places a call, the server normalizes the phone number to E.164 format, if necessary, and attempts to match it to a SIP URI.</span></span> <span data-ttu-id="51096-108">При невозможности сопоставления на сервере применяется логическая схема маршрутизации исходящих вызовов на основе представленной строки набора.</span><span class="sxs-lookup"><span data-stu-id="51096-108">If the server cannot make the match, it applies outbound call routing logic based on the supplied dial string.</span></span> <span data-ttu-id="51096-109">Эта логическая схема задается путем настройки параметров сервера, описание которых приведено в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="51096-109">You define that logic by configuring the server settings that are described in the following table.</span></span>

### <a name="lync-server-outbound-call-routing-settings"></a><span data-ttu-id="51096-110">Параметры маршрутизации исходящих вызовов Lync Server</span><span class="sxs-lookup"><span data-stu-id="51096-110">Lync Server Outbound Call Routing Settings</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="51096-111">Объект</span><span class="sxs-lookup"><span data-stu-id="51096-111">Object</span></span></th>
<th><span data-ttu-id="51096-112">Описание</span><span class="sxs-lookup"><span data-stu-id="51096-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="51096-113">Абонентская группа</span><span class="sxs-lookup"><span data-stu-id="51096-113">Dial Plan</span></span></p></td>
<td><p><span data-ttu-id="51096-114">Абонентская группа — это именованный набор правил нормализации, которые преобразуют номера телефонов для именованного расположения, отдельного пользователя или контактного объекта в единый стандартный формат (E.164) для авторизации телефонов и маршрутизации вызовов.</span><span class="sxs-lookup"><span data-stu-id="51096-114">A dial plan is a named set of normalization rules that translates phone numbers for a named location, individual user, or contact object into a single standard (E.164) format for purposes of phone authorization and call routing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51096-115">Правило нормализации</span><span class="sxs-lookup"><span data-stu-id="51096-115">Normalization rule</span></span></p></td>
<td><p><span data-ttu-id="51096-p102">Правила нормализации указывают, как телефонные номера, выраженные в разных форматах, должны маршрутизироваться для каждого конкретного расположения, пользователя или контактного объекта. Одна и та же строка набора может интерпретироваться и преобразовываться по-разному в зависимости от местоположения, из которого она была набрана, и лица или контактного объекта, выполнившего вызов. Ряд правил нормализации, связанный с конкретным расположением, составляет абонентскую группу.</span><span class="sxs-lookup"><span data-stu-id="51096-p102">Normalization rules define how phone numbers expressed in various formats are to be routed for each specified location, user, or contact object. The same dial string may be interpreted and translated differently, depending on the location from which it is dialed and the person or contact object that makes the call. A set of normalization rules associated with a particular location constitutes a dial plan.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51096-119">Политика голосовой связи</span><span class="sxs-lookup"><span data-stu-id="51096-119">Voice policy</span></span></p></td>
<td><p><span data-ttu-id="51096-p103">Политика голосовой связи связывает одну или несколько записей режима работы с ТСОП с одним пользователем или группой пользователей. Политика голосовой связи также предоставляет список функций вызовов, которые можно включать или отключать.</span><span class="sxs-lookup"><span data-stu-id="51096-p103">A voice policy associates one or more PSTN usage records with one user or a group of users. A voice policy also provides a list of calling features that you can enable or disable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51096-122">Запись режима работы с ТСОП</span><span class="sxs-lookup"><span data-stu-id="51096-122">PSTN usage record</span></span></p></td>
<td><p><span data-ttu-id="51096-123">Запись режима работы с ТСОП задает класс вызовов (например, внутренний, местный или междугородный), которые могут выполняться разными пользователями или группами пользователей в организации.</span><span class="sxs-lookup"><span data-stu-id="51096-123">A PSTN usage record specifies a class of call (such as internal, local, or long distance) that can be made by various users, or groups of users, in an organization.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51096-124">Маршрут вызова</span><span class="sxs-lookup"><span data-stu-id="51096-124">Call Route</span></span></p></td>
<td><p><span data-ttu-id="51096-p104">Маршрут вызова связывает телефонные номера назначения с конкретными каналами и записями режимов работы с ТСОП. Шлюз ТСОП рассматривается как магистраль.</span><span class="sxs-lookup"><span data-stu-id="51096-p104">A call route associates destination phone numbers with particular trunks and PSTN usage records. A PSTN gateway is considered a trunk.</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="in-this-section"></a><span data-ttu-id="51096-127">Содержание</span><span class="sxs-lookup"><span data-stu-id="51096-127">In This Section</span></span>

<span data-ttu-id="51096-128">В этом разделе приводятся рекомендации по настройке следующих параметров сервера маршрутизации исходящих вызовов.</span><span class="sxs-lookup"><span data-stu-id="51096-128">This section provides guidelines for configuring the following outbound call routing server settings:</span></span>

  - <span></span>  
    [<span data-ttu-id="51096-129">Абонентские группы и правила нормализации в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="51096-129">Dial plans and normalization rules in Lync Server 2013</span></span>](lync-server-2013-dial-plans-and-normalization-rules.md)

  - <span></span>  
    [<span data-ttu-id="51096-130">Политики голосовой связи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="51096-130">Voice policies in Lync Server 2013</span></span>](lync-server-2013-voice-policies.md)

  - <span></span>  
    [<span data-ttu-id="51096-131">Записи использования ТСОП в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="51096-131">PSTN usage records in Lync Server 2013</span></span>](lync-server-2013-pstn-usage-records.md)

  - <span></span>  
    [<span data-ttu-id="51096-132">Маршруты голосовых вызовов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="51096-132">Voice routes in Lync Server 2013</span></span>](lync-server-2013-voice-routes.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="51096-133">См. также</span><span class="sxs-lookup"><span data-stu-id="51096-133">See Also</span></span>


[<span data-ttu-id="51096-134">Магистральные линии SIP в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="51096-134">SIP trunking in Lync Server 2013</span></span>](lync-server-2013-sip-trunking.md)  
[<span data-ttu-id="51096-135">Прямые подключения по протоколу SIP в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="51096-135">Direct SIP connections in Lync Server 2013</span></span>](lync-server-2013-direct-sip-connections.md)  
  

<span data-ttu-id="51096-136"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="51096-136"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

