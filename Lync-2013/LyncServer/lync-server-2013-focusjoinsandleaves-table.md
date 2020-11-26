---
title: 'Lync Server 2013: таблица FocusJoinsAndLeaves'
description: 'Таблица Lync Server 2013: FocusJoinsAndLeaves.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: FocusJoinsAndLeaves table
ms:assetid: e6f0212c-67e9-4061-8720-d0296e855991
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399026(v=OCS.15)
ms:contentKeyID: 48185690
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5796de16ed204ce4f33935d937cbaa425d63a67f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428111"
---
# <a name="focusjoinsandleaves-table-in-lync-server-2013"></a><span data-ttu-id="26259-103">Таблица FocusJoinsAndLeaves в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="26259-103">FocusJoinsAndLeaves table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="26259-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="26259-104">

<span> </span></span></span>

<span data-ttu-id="26259-105">_**Тема последнего изменения:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="26259-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="26259-106">В каждой записи в этой таблице содержатся сведения о CDR для одного пользователя и о том, что нужно оставлять на одной конференции.</span><span class="sxs-lookup"><span data-stu-id="26259-106">Each record in this table contains the CDR information about one user’s join and leave information for one conference.</span></span> <span data-ttu-id="26259-107">Каждая конференция представлена в этой таблице одной записью каждый раз, когда пользователь присоединяется к Конференции и оставляет ее.</span><span class="sxs-lookup"><span data-stu-id="26259-107">Each conference is represented in this table by one record for each time a user joins and leaves the conference.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="26259-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="26259-108">Column</span></span></th>
<th><span data-ttu-id="26259-109">Тип данных</span><span class="sxs-lookup"><span data-stu-id="26259-109">Data Type</span></span></th>
<th><span data-ttu-id="26259-110">Ключ/индекс</span><span class="sxs-lookup"><span data-stu-id="26259-110">Key/Index</span></span></th>
<th><span data-ttu-id="26259-111">Сведения</span><span class="sxs-lookup"><span data-stu-id="26259-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="26259-112"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="26259-112"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="26259-113">datetime</span><span class="sxs-lookup"><span data-stu-id="26259-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="26259-114">Основной, внешний</span><span class="sxs-lookup"><span data-stu-id="26259-114">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="26259-115">Время экземпляра Конференции.</span><span class="sxs-lookup"><span data-stu-id="26259-115">Time of conference instance.</span></span> <span data-ttu-id="26259-116">Используется в сочетании с <strong>SessionIdSeq</strong> для уникальной идентификации экземпляра Конференции.</span><span class="sxs-lookup"><span data-stu-id="26259-116">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a conference instance.</span></span> <span data-ttu-id="26259-117">Дополнительные сведения приведены <a href="lync-server-2013-conferences-table.md">в таблице конференции для Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="26259-117">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26259-118"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="26259-118"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="26259-119">целое</span><span class="sxs-lookup"><span data-stu-id="26259-119">int</span></span></p></td>
<td><p><span data-ttu-id="26259-120">Основной, внешний</span><span class="sxs-lookup"><span data-stu-id="26259-120">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="26259-121">ИДЕНТИФИКАЦИОНный номер для идентификации экземпляра Конференции.</span><span class="sxs-lookup"><span data-stu-id="26259-121">ID number to identify the conference instance.</span></span> <span data-ttu-id="26259-122">Используется в сочетании с <strong>SessionIdTime</strong> для уникальной идентификации экземпляра Конференции.</span><span class="sxs-lookup"><span data-stu-id="26259-122">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a conference instance.</span></span> <span data-ttu-id="26259-123">Дополнительные сведения приведены <a href="lync-server-2013-conferences-table.md">в таблице конференции для Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="26259-123">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26259-124"><strong>DialogSessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="26259-124"><strong>DialogSessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="26259-125">datetime</span><span class="sxs-lookup"><span data-stu-id="26259-125">datetime</span></span></p></td>
<td><p><span data-ttu-id="26259-126">Основной, внешний</span><span class="sxs-lookup"><span data-stu-id="26259-126">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="26259-127">Время запроса сеанса.</span><span class="sxs-lookup"><span data-stu-id="26259-127">Time of session request.</span></span> <span data-ttu-id="26259-128">Используется в сочетании с <strong>SessionIdSeq</strong> для уникальной идентификации сеанса.</span><span class="sxs-lookup"><span data-stu-id="26259-128">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="26259-129">Дополнительные сведения приведены <a href="lync-server-2013-dialogs-table.md">в таблице диалоговые окна Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="26259-129">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26259-130"><strong>DialogSessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="26259-130"><strong>DialogSessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="26259-131">целое</span><span class="sxs-lookup"><span data-stu-id="26259-131">int</span></span></p></td>
<td><p><span data-ttu-id="26259-132">Основной, внешний</span><span class="sxs-lookup"><span data-stu-id="26259-132">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="26259-133">ИДЕНТИФИКАЦИОНный номер для идентификации сеанса.</span><span class="sxs-lookup"><span data-stu-id="26259-133">ID number to identify the session.</span></span> <span data-ttu-id="26259-134">Используется в сочетании с <strong>SessionIdTime</strong> для уникальной идентификации сеанса.</span><span class="sxs-lookup"><span data-stu-id="26259-134">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.</span></span> <span data-ttu-id="26259-135">Дополнительные сведения приведены <a href="lync-server-2013-dialogs-table.md">в таблице диалоговые окна Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="26259-135">see the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26259-136"><strong>Идентификатора пользователя</strong></span><span class="sxs-lookup"><span data-stu-id="26259-136"><strong>UserId</strong></span></span></p></td>
<td><p><span data-ttu-id="26259-137">целое</span><span class="sxs-lookup"><span data-stu-id="26259-137">int</span></span></p></td>
<td><p><span data-ttu-id="26259-138">Другом</span><span class="sxs-lookup"><span data-stu-id="26259-138">Foreign</span></span></p></td>
<td><p><span data-ttu-id="26259-139">Уникальный номер, идентифицирующий этого пользователя, на который ссылается <a href="lync-server-2013-users-table.md">Таблица "Пользователи" в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="26259-139">Unique number identifying this user, referenced from the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26259-140"><strong>FocusUserInstance</strong></span><span class="sxs-lookup"><span data-stu-id="26259-140"><strong>FocusUserInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="26259-141">целое</span><span class="sxs-lookup"><span data-stu-id="26259-141">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="26259-142">Если пользователь входит в систему на нескольких компьютерах или устройствах одновременно, <strong>UserInstance</strong> используется для уникальной идентификации комбинации пользователей и устройств.</span><span class="sxs-lookup"><span data-stu-id="26259-142">If a user is logged on at multiple computers or devices at the same time, <strong>UserInstance</strong> is used to uniquely identify the user/device combination.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26259-143"><strong>IsUserInternal</strong></span><span class="sxs-lookup"><span data-stu-id="26259-143"><strong>IsUserInternal</strong></span></span></p></td>
<td><p><span data-ttu-id="26259-144">бит</span><span class="sxs-lookup"><span data-stu-id="26259-144">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="26259-145">Вне зависимости от того, вошел ли пользователь из внутреннего или нет.</span><span class="sxs-lookup"><span data-stu-id="26259-145">Whether the user logged on from internal or not.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26259-146"><strong>UserRole</strong></span><span class="sxs-lookup"><span data-stu-id="26259-146"><strong>UserRole</strong></span></span></p></td>
<td><p><span data-ttu-id="26259-147">целое</span><span class="sxs-lookup"><span data-stu-id="26259-147">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="26259-148">Роль этого пользователя на Конференции, например докладчика или участника.</span><span class="sxs-lookup"><span data-stu-id="26259-148">This user’s role in the conference, such as Presenter or Attendee.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26259-149"><strong>UserJoinTime</strong></span><span class="sxs-lookup"><span data-stu-id="26259-149"><strong>UserJoinTime</strong></span></span></p></td>
<td><p><span data-ttu-id="26259-150">datetime</span><span class="sxs-lookup"><span data-stu-id="26259-150">datetime</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="26259-151">Время присоединения пользователя к Конференции.</span><span class="sxs-lookup"><span data-stu-id="26259-151">The time this user joins the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26259-152"><strong>UserLeaveTime</strong></span><span class="sxs-lookup"><span data-stu-id="26259-152"><strong>UserLeaveTime</strong></span></span></p></td>
<td><p><span data-ttu-id="26259-153">datetime</span><span class="sxs-lookup"><span data-stu-id="26259-153">datetime</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="26259-154">Время, когда пользователь покидает Конференцию.</span><span class="sxs-lookup"><span data-stu-id="26259-154">The time this user leaves the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26259-155"><strong>ClientVerId</strong></span><span class="sxs-lookup"><span data-stu-id="26259-155"><strong>ClientVerId</strong></span></span></p></td>
<td><p><span data-ttu-id="26259-156">целое</span><span class="sxs-lookup"><span data-stu-id="26259-156">int</span></span></p></td>
<td><p><span data-ttu-id="26259-157">Другом</span><span class="sxs-lookup"><span data-stu-id="26259-157">Foreign</span></span></p></td>
<td><p><span data-ttu-id="26259-158">Версия клиентского программного обеспечения пользователя, на которую ссылается <a href="lync-server-2013-clientversions-table.md">Таблица ClientVersions в Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="26259-158">Version of the user’s client software, referenced to the <a href="lync-server-2013-clientversions-table.md">ClientVersions table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26259-159"><strong>UserEndpointId</strong></span><span class="sxs-lookup"><span data-stu-id="26259-159"><strong>UserEndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="26259-160">Идентификатора</span><span class="sxs-lookup"><span data-stu-id="26259-160">uniqueIdentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="26259-161">Глобальный уникальный идентификатор (GUID) конечной точки, используемой в Конференции.</span><span class="sxs-lookup"><span data-stu-id="26259-161">Globally unique identifier (GUID) of the endpoint used in the conference.</span></span></p>
<p><span data-ttu-id="26259-162">Это поле было введено в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="26259-162">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="26259-163">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="26259-163">


</div>

<span> </span>

</div>

</div>

</span></span></div>

