---
title: 'Lync Server 2013: tblFileToken'
description: 'Lync Server 2013: tblFileToken.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblFileToken
ms:assetid: 49e7dd79-1607-443c-818a-88c160e4ed06
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558646(v=OCS.15)
ms:contentKeyID: 48184073
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9c0a0465bd769cff5c23c00a98f79e2346232175
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423535"
---
# <a name="tblfiletoken-in-lync-server-2013"></a><span data-ttu-id="ab502-103">tblFileToken в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ab502-103">tblFileToken in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ab502-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ab502-104">

<span> </span></span></span>

<span data-ttu-id="ab502-105">_**Тема последнего изменения:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="ab502-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="ab502-106">tblFileToken включает временные маркеры для целей обмена файлами.</span><span class="sxs-lookup"><span data-stu-id="ab502-106">tblFileToken contains temporary tokens for file transfer purposes.</span></span>

### <a name="columns"></a><span data-ttu-id="ab502-107">Столбцов</span><span class="sxs-lookup"><span data-stu-id="ab502-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ab502-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="ab502-108">Column</span></span></th>
<th><span data-ttu-id="ab502-109">Тип</span><span class="sxs-lookup"><span data-stu-id="ab502-109">Type</span></span></th>
<th><span data-ttu-id="ab502-110">Описание</span><span class="sxs-lookup"><span data-stu-id="ab502-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ab502-111">fileToken</span><span class="sxs-lookup"><span data-stu-id="ab502-111">fileToken</span></span></p></td>
<td><p><span data-ttu-id="ab502-112">nvarchar (50), NOT NULL</span><span class="sxs-lookup"><span data-stu-id="ab502-112">nvarchar (50), not null</span></span></p></td>
<td><p><span data-ttu-id="ab502-113">Уникальный маркер (GUID).</span><span class="sxs-lookup"><span data-stu-id="ab502-113">Unique token (a GUID).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ab502-114">fileTokenUserID</span><span class="sxs-lookup"><span data-stu-id="ab502-114">fileTokenUserID</span></span></p></td>
<td><p><span data-ttu-id="ab502-115">int, NOT NULL</span><span class="sxs-lookup"><span data-stu-id="ab502-115">int, not null</span></span></p></td>
<td><p><span data-ttu-id="ab502-116">Идентификатор участника, который передает файл.</span><span class="sxs-lookup"><span data-stu-id="ab502-116">ID of the principal that is transferring the file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ab502-117">fileTokenChannelID</span><span class="sxs-lookup"><span data-stu-id="ab502-117">fileTokenChannelID</span></span></p></td>
<td><p><span data-ttu-id="ab502-118">GUID, а не NULL</span><span class="sxs-lookup"><span data-stu-id="ab502-118">GUID, not null</span></span></p></td>
<td><p><span data-ttu-id="ab502-119">GUID узла комнаты чата.</span><span class="sxs-lookup"><span data-stu-id="ab502-119">GUID of the chat room node.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ab502-120">fileTokenExpireDate</span><span class="sxs-lookup"><span data-stu-id="ab502-120">fileTokenExpireDate</span></span></p></td>
<td><p><span data-ttu-id="ab502-121">DateTime, NOT NULL</span><span class="sxs-lookup"><span data-stu-id="ab502-121">datetime, not null</span></span></p></td>
<td><p><span data-ttu-id="ab502-122">Время окончания срока действия.</span><span class="sxs-lookup"><span data-stu-id="ab502-122">Expiration time.</span></span> <span data-ttu-id="ab502-123">(Срок действия токенов истекает через 30 минут, за исключением случаев, когда они закреплены (в этой статье описаны следующие описания).</span><span class="sxs-lookup"><span data-stu-id="ab502-123">(Tokens expire after 30 minutes, unless pinned (see the following descriptions in this column).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ab502-124">fileTokenComplianceFileUrl</span><span class="sxs-lookup"><span data-stu-id="ab502-124">fileTokenComplianceFileUrl</span></span></p></td>
<td><p><span data-ttu-id="ab502-125">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="ab502-125">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="ab502-126">URL-адрес перенесенного файла (для использования службы соответствия требованиям).</span><span class="sxs-lookup"><span data-stu-id="ab502-126">URL of the transferred file (for Compliance service use).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ab502-127">fileTokenComplianceThumbnailUrl</span><span class="sxs-lookup"><span data-stu-id="ab502-127">fileTokenComplianceThumbnailUrl</span></span></p></td>
<td><p><span data-ttu-id="ab502-128">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="ab502-128">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="ab502-129">URL-адрес миниатюры перенесенного файла (для использования службой соответствия требованиям).</span><span class="sxs-lookup"><span data-stu-id="ab502-129">URL of the thumbnail for the transferred file (for Compliance service use).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ab502-130">fileTokenComplianceTime</span><span class="sxs-lookup"><span data-stu-id="ab502-130">fileTokenComplianceTime</span></span></p></td>
<td><p><span data-ttu-id="ab502-131">datetime2</span><span class="sxs-lookup"><span data-stu-id="ab502-131">datetime2</span></span></p></td>
<td><p><span data-ttu-id="ab502-132">Метка времени для фактической операции передачи файлов (для использования службой соответствия требованиям).</span><span class="sxs-lookup"><span data-stu-id="ab502-132">Timestamp for the actual file transfer operation (for Compliance service use).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ab502-133">fileTokenComplianceIsUpload</span><span class="sxs-lookup"><span data-stu-id="ab502-133">fileTokenComplianceIsUpload</span></span></p></td>
<td><p><span data-ttu-id="ab502-134">бит</span><span class="sxs-lookup"><span data-stu-id="ab502-134">bit</span></span></p></td>
<td><p><span data-ttu-id="ab502-135">Значение true, если отправка; Значение false, если Download (для использования службы соответствия требованиям).</span><span class="sxs-lookup"><span data-stu-id="ab502-135">True if upload; False if download (for Compliance service use).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ab502-136">fileTokenCompliancePinned</span><span class="sxs-lookup"><span data-stu-id="ab502-136">fileTokenCompliancePinned</span></span></p></td>
<td><p><span data-ttu-id="ab502-137">bit, NOT NULL</span><span class="sxs-lookup"><span data-stu-id="ab502-137">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="ab502-138">Значение true, если маркер закреплен.</span><span class="sxs-lookup"><span data-stu-id="ab502-138">True if token is pinned.</span></span> <span data-ttu-id="ab502-139">Она используется для хранения токенов в таблице до тех пор, пока служба соответствия требованиям не сможет получить из нее нужные поля.</span><span class="sxs-lookup"><span data-stu-id="ab502-139">It’s used to keep the token in the table until Compliance service has a chance to retrieve the relevant fields from it.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="ab502-140">Параметры</span><span class="sxs-lookup"><span data-stu-id="ab502-140">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ab502-141">Столбец</span><span class="sxs-lookup"><span data-stu-id="ab502-141">Column</span></span></th>
<th><span data-ttu-id="ab502-142">Описание</span><span class="sxs-lookup"><span data-stu-id="ab502-142">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ab502-143">fileToken</span><span class="sxs-lookup"><span data-stu-id="ab502-143">fileToken</span></span></p></td>
<td><p><span data-ttu-id="ab502-144">Первичный ключ.</span><span class="sxs-lookup"><span data-stu-id="ab502-144">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ab502-145">fileTokenChannelID</span><span class="sxs-lookup"><span data-stu-id="ab502-145">fileTokenChannelID</span></span></p></td>
<td><p><span data-ttu-id="ab502-146">Внешний ключ с подстановкой в таблице tblNode. nodeGuid.</span><span class="sxs-lookup"><span data-stu-id="ab502-146">Foreign key with lookup in tblNode.nodeGuid table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="ab502-147">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ab502-147">


</div>

<span> </span>

</div>

</div>

</span></span></div>

