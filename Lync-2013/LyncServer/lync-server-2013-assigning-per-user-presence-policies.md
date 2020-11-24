---
title: 'Lync Server 2013: назначение политик присутствия на уровне пользователей'
description: 'Lync Server 2013: назначение политик присутствия на уровне пользователей.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Assigning per-user presence policies
ms:assetid: fd1097b7-248d-4b78-8c43-456b03257c18
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182614(v=OCS.15)
ms:contentKeyID: 48185955
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5c3d4b4bda0c4bb85065d546fdbb4b2578db0e3f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399973"
---
# <a name="assigning-per-user-presence-policies-in-lync-server-2013"></a><span data-ttu-id="47216-103">Назначение политик присутствия по каждому пользователю в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="47216-103">Assigning per-user presence policies in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="47216-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="47216-104">

<span> </span></span></span>

<span data-ttu-id="47216-105">_**Тема последнего изменения:** 2012-10-11_</span><span class="sxs-lookup"><span data-stu-id="47216-105">_**Topic Last Modified:** 2012-10-11_</span></span>

<span data-ttu-id="47216-106">Политика присутствия — это набор ограничений и ограничений, влияющих на присутствие.</span><span class="sxs-lookup"><span data-stu-id="47216-106">A presence policy is a set of limits and restrictions that affect presence.</span></span> <span data-ttu-id="47216-107">В приведенной ниже таблице описаны параметры политики присутствия, доступные в Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="47216-107">The following table describes the presence policy settings available in Lync Server 2013.</span></span>

### <a name="presence-policy-settings"></a><span data-ttu-id="47216-108">Параметры политики присутствия</span><span class="sxs-lookup"><span data-stu-id="47216-108">Presence Policy Settings</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="47216-109">Имя XML</span><span class="sxs-lookup"><span data-stu-id="47216-109">XML name</span></span></th>
<th><span data-ttu-id="47216-110">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="47216-110">Display name</span></span></th>
<th><span data-ttu-id="47216-111">Описание</span><span class="sxs-lookup"><span data-stu-id="47216-111">Description</span></span></th>
<th><span data-ttu-id="47216-112">Тип</span><span class="sxs-lookup"><span data-stu-id="47216-112">Type</span></span></th>
<th><span data-ttu-id="47216-113">Значение</span><span class="sxs-lookup"><span data-stu-id="47216-113">Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="47216-114">CategorySubscriptions</span><span class="sxs-lookup"><span data-stu-id="47216-114">CategorySubscriptions</span></span></p></td>
<td><p><span data-ttu-id="47216-115">Максимальное число подписок на категорию подписчика</span><span class="sxs-lookup"><span data-stu-id="47216-115">Maximum Number of Subscriber Category Subscriptions</span></span></p></td>
<td><p><span data-ttu-id="47216-116">Ограничивает число подписок на категорию подписчиков.</span><span class="sxs-lookup"><span data-stu-id="47216-116">Limits the number of subscriber category subscriptions.</span></span> <span data-ttu-id="47216-117">Например, если программа Communicator подписалась на присутствие пользователя, она получает подписку на категорию для каждой карточки контакта, данных календаря, заметок, служб и категорий состояний.</span><span class="sxs-lookup"><span data-stu-id="47216-117">For example, when Communicator subscribes to a user’s presence, it obtains a category subscription for each of the contact card, calendar data, notes, services, and state categories.</span></span></p>
<p><span data-ttu-id="47216-118">Значение 0 означает, что пользователь или объект контакта не может подписаться другим пользователям.</span><span class="sxs-lookup"><span data-stu-id="47216-118">A setting of 0 means that the user or contact object cannot be subscribed to by others.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="47216-119">Этот параметр может существенно повлиять на производительность, если его значение установлено на большое число, а в среднем пользователь имеет большое количество пользователей, которые подписались на его присутствие.</span><span class="sxs-lookup"><span data-stu-id="47216-119">This setting can have a significant impact on performance if it is set to a high number, and the average user has a large number of users subscribing to his or her presence.</span></span>


</div></td>
<td><p><span data-ttu-id="47216-120">Целое число</span><span class="sxs-lookup"><span data-stu-id="47216-120">Integer</span></span></p></td>
<td><p><span data-ttu-id="47216-121">0-3000</span><span class="sxs-lookup"><span data-stu-id="47216-121">0-3000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47216-122">PromptedSubscribers</span><span class="sxs-lookup"><span data-stu-id="47216-122">PromptedSubscribers</span></span></p></td>
<td><p><span data-ttu-id="47216-123">Максимальное количество уведомлений о подписке на состояние присутствия в очереди</span><span class="sxs-lookup"><span data-stu-id="47216-123">Maximum Number of Queued Presence Subscription Alerts</span></span></p></td>
<td><p><span data-ttu-id="47216-124">Ограничивает количество записей в таблице "запрашиваемые абоненты".</span><span class="sxs-lookup"><span data-stu-id="47216-124">Limits the number of entries in the prompted subscribers table.</span></span> <span data-ttu-id="47216-125">Этот параметр определяет максимальное количество запросов, которые можно поместить в очередь для определенного пользователя.</span><span class="sxs-lookup"><span data-stu-id="47216-125">This setting determines the maximum number of prompts that can be queued for a given user.</span></span> <span data-ttu-id="47216-126">Например, если пользователь A подписался на присутствие пользователя B, пользователь B получает сообщение о том, что пользователь A теперь подписан на пользователя B, и в таблице подписчиков пользователя B создается запрос подтверждения.</span><span class="sxs-lookup"><span data-stu-id="47216-126">For example, when user A subscribes to user B’s presence, user B receives a prompt that user A is now subscribed to user B, and an acknowledgement prompt is created in user B’s prompted subscribers table.</span></span> <span data-ttu-id="47216-127">После того как пользователь B подтвердит, что подписку будет удалена, запрос подтверждения удаляется из таблицы подписчиков пользователя B.</span><span class="sxs-lookup"><span data-stu-id="47216-127">After user B accepts, or acknowledges, the subscription, the acknowledgement prompt is removed from user B’s prompted subscribers table.</span></span></p>
<p><span data-ttu-id="47216-128">Нулевое значение означает, что пользователю не будет предлагаться подписаться на свое присутствие.</span><span class="sxs-lookup"><span data-stu-id="47216-128">A setting of 0 means that the user is not prompted when someone subscribes to his or her presence.</span></span></p></td>
<td><p><span data-ttu-id="47216-129">Целое число или маркер</span><span class="sxs-lookup"><span data-stu-id="47216-129">Integer or Token</span></span></p></td>
<td><p><span data-ttu-id="47216-130">0-500</span><span class="sxs-lookup"><span data-stu-id="47216-130">0-500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="47216-131">По умолчанию политика и **Служба** **по умолчанию** устанавливаются при развертывании сервера Lync Server.</span><span class="sxs-lookup"><span data-stu-id="47216-131">By default, the **Default Policy** and **Service: Medium** presence policies are installed when you deploy Lync Server.</span></span> <span data-ttu-id="47216-132">В приведенной ниже таблице описаны конкретные параметры двух политик присутствия.</span><span class="sxs-lookup"><span data-stu-id="47216-132">The following table describes the specific settings of the two presence policies.</span></span>

### <a name="presence-policies"></a><span data-ttu-id="47216-133">Политики присутствия</span><span class="sxs-lookup"><span data-stu-id="47216-133">Presence Policies</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="47216-134">Название политики</span><span class="sxs-lookup"><span data-stu-id="47216-134">Policy name</span></span></th>
<th><span data-ttu-id="47216-135">Описание</span><span class="sxs-lookup"><span data-stu-id="47216-135">Description</span></span></th>
<th><span data-ttu-id="47216-136">CategorySubscriptions</span><span class="sxs-lookup"><span data-stu-id="47216-136">CategorySubscriptions</span></span></th>
<th><span data-ttu-id="47216-137">PromptedSubscribers</span><span class="sxs-lookup"><span data-stu-id="47216-137">PromptedSubscribers</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="47216-138">Политика по умолчанию</span><span class="sxs-lookup"><span data-stu-id="47216-138">Default Policy</span></span></p></td>
<td><p><span data-ttu-id="47216-139">Политика для обычных пользователей.</span><span class="sxs-lookup"><span data-stu-id="47216-139">Policy for typical users.</span></span> <span data-ttu-id="47216-140">Это политика присутствия по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="47216-140">This is the default presence policy.</span></span></p></td>
<td><p><span data-ttu-id="47216-141">1000</span><span class="sxs-lookup"><span data-stu-id="47216-141">1000</span></span></p></td>
<td><p><span data-ttu-id="47216-142">200</span><span class="sxs-lookup"><span data-stu-id="47216-142">200</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47216-143">Служба: средняя</span><span class="sxs-lookup"><span data-stu-id="47216-143">Service: Medium</span></span></p></td>
<td><p><span data-ttu-id="47216-144">Политика для приложений, которым больше пользователей нужно подписаться на присутствие объекта.</span><span class="sxs-lookup"><span data-stu-id="47216-144">Policy for applications that require more users to subscribe to the object’s presence.</span></span></p></td>
<td><p><span data-ttu-id="47216-145">1000</span><span class="sxs-lookup"><span data-stu-id="47216-145">1000</span></span></p></td>
<td><p><span data-ttu-id="47216-146">до</span><span class="sxs-lookup"><span data-stu-id="47216-146">0</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="47216-147">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="47216-147">


</div>

<span> </span>

</div>

</div>

</span></span></div>

