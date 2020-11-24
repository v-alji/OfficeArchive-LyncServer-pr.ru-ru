---
title: 'Lync Server 2013: tblADCookie'
description: 'Lync Server 2013: tblADCookie.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblADCookie
ms:assetid: 0a9102c4-47aa-40ea-8a0d-20e72ab09848
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558610(v=OCS.15)
ms:contentKeyID: 48183366
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 41c3dde3730ede07b204a473c7fe0a5ab68054d3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398728"
---
# <a name="tbladcookie-in-lync-server-2013"></a><span data-ttu-id="e386d-103">tblADCookie в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e386d-103">tblADCookie in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e386d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e386d-104">

<span> </span></span></span>

<span data-ttu-id="e386d-105">_**Тема последнего изменения:** 2012-06-25_</span><span class="sxs-lookup"><span data-stu-id="e386d-105">_**Topic Last Modified:** 2012-06-25_</span></span>

<span data-ttu-id="e386d-106">tblADCookie включает в себя текущие cookie-файлы для синхронизации протокола Lightweight Directory Access.</span><span class="sxs-lookup"><span data-stu-id="e386d-106">tblADCookie contains the current Lightweight Directory Access Protocol (LDAP) Sync cookies.</span></span>

### <a name="columns"></a><span data-ttu-id="e386d-107">Столбцов</span><span class="sxs-lookup"><span data-stu-id="e386d-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e386d-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="e386d-108">Column</span></span></th>
<th><span data-ttu-id="e386d-109">Тип</span><span class="sxs-lookup"><span data-stu-id="e386d-109">Type</span></span></th>
<th><span data-ttu-id="e386d-110">Описание</span><span class="sxs-lookup"><span data-stu-id="e386d-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e386d-111">prinGuid</span><span class="sxs-lookup"><span data-stu-id="e386d-111">prinGuid</span></span></p></td>
<td><p><span data-ttu-id="e386d-112">GUID, а не NULL</span><span class="sxs-lookup"><span data-stu-id="e386d-112">GUID, not null</span></span></p></td>
<td><p><span data-ttu-id="e386d-113">Идентификатор GUID участника отслеживаемого домена.</span><span class="sxs-lookup"><span data-stu-id="e386d-113">Principal GUID of the domain being monitored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e386d-114">prinDCHost</span><span class="sxs-lookup"><span data-stu-id="e386d-114">prinDCHost</span></span></p></td>
<td><p><span data-ttu-id="e386d-115">nvarchar (255)</span><span class="sxs-lookup"><span data-stu-id="e386d-115">nvarchar (255)</span></span></p></td>
<td><p><span data-ttu-id="e386d-116">Полное доменное имя (FQDN) текущего контроллера домена, используемого для синхронизации доменных служб Active Directory. Имеет информационное значение.</span><span class="sxs-lookup"><span data-stu-id="e386d-116">Fully qualified domain name (FQDN) of the current domain controller used for Active Directory Domain Services Sync. Has informational value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e386d-117">adcContent</span><span class="sxs-lookup"><span data-stu-id="e386d-117">adcContent</span></span></p></td>
<td><p><span data-ttu-id="e386d-118">изображение (двоичное)</span><span class="sxs-lookup"><span data-stu-id="e386d-118">image (binary)</span></span></p></td>
<td><p><span data-ttu-id="e386d-119">Cookie синхронизации Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e386d-119">Active Directory Sync cookie.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e386d-120">lastUpdated</span><span class="sxs-lookup"><span data-stu-id="e386d-120">lastUpdated</span></span></p></td>
<td><p><span data-ttu-id="e386d-121">datetime</span><span class="sxs-lookup"><span data-stu-id="e386d-121">datetime</span></span></p></td>
<td><p><span data-ttu-id="e386d-122">Метка времени со временем обновления строки.</span><span class="sxs-lookup"><span data-stu-id="e386d-122">Time stamp with the row update time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e386d-123">lockedUntil</span><span class="sxs-lookup"><span data-stu-id="e386d-123">lockedUntil</span></span></p></td>
<td><p><span data-ttu-id="e386d-124">datetime</span><span class="sxs-lookup"><span data-stu-id="e386d-124">datetime</span></span></p></td>
<td><p><span data-ttu-id="e386d-125">Время, по истечении которого изменения строки будут заблокированы.</span><span class="sxs-lookup"><span data-stu-id="e386d-125">Time until the row is locked for changes.</span></span> <span data-ttu-id="e386d-126">Это является частью механизма программного обеспечения, который гарантирует, что только одна из служб чата выполняет синхронизацию службы каталогов Active Directory за один раз.</span><span class="sxs-lookup"><span data-stu-id="e386d-126">This is part of a software interlock mechanism that ensures that only one of the chat services does the Active Directory Sync at a time.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="e386d-127">Параметры</span><span class="sxs-lookup"><span data-stu-id="e386d-127">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e386d-128">Столбцы (-ы)</span><span class="sxs-lookup"><span data-stu-id="e386d-128">Column(s)</span></span></th>
<th><span data-ttu-id="e386d-129">Описание</span><span class="sxs-lookup"><span data-stu-id="e386d-129">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e386d-130">prinGuid</span><span class="sxs-lookup"><span data-stu-id="e386d-130">prinGuid</span></span></p></td>
<td><p><span data-ttu-id="e386d-131">Первичный ключ.</span><span class="sxs-lookup"><span data-stu-id="e386d-131">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e386d-132">prinGuid</span><span class="sxs-lookup"><span data-stu-id="e386d-132">prinGuid</span></span></p></td>
<td><p><span data-ttu-id="e386d-133">Внешний ключ с подстановкой в таблице Principal. prinGuid.</span><span class="sxs-lookup"><span data-stu-id="e386d-133">Foreign key with lookup in Principal.prinGuid table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="e386d-134">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e386d-134">


</div>

<span> </span>

</div>

</div>

</span></span></div>

