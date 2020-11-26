---
title: 'Lync Server 2013: масштабируемость'
description: Масштабируемость Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Scalability
ms:assetid: 46fa0cb5-1507-4a12-ad3f-ba64585e2dc4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg417160(v=OCS.15)
ms:contentKeyID: 48183995
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 28cd5820755ffd1eb863ed6f2369b5756a7ae3f5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442119"
---
# <a name="scalability-with-lync-server-2013"></a><span data-ttu-id="a7406-103">Масштабируемость с Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a7406-103">Scalability with Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a7406-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a7406-104">

<span> </span></span></span>

<span data-ttu-id="a7406-105">_**Тема последнего изменения:** 2012-06-25_</span><span class="sxs-lookup"><span data-stu-id="a7406-105">_**Topic Last Modified:** 2012-06-25_</span></span>

<span data-ttu-id="a7406-106">Lync Server предлагается в двух выпусках, Enterprise Edition и Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="a7406-106">Lync Server is offered in two editions, Enterprise Edition and Standard Edition.</span></span> <span data-ttu-id="a7406-107">Различные выпуски предназначены преимущественно для разных размеров организаций.</span><span class="sxs-lookup"><span data-stu-id="a7406-107">The different editions are intended primarily for different sizes of organizations.</span></span> <span data-ttu-id="a7406-108">Как показано в приведенной ниже таблице, оба издания поддерживают все функции во всех рабочих нагрузках, кроме случаев высокой доступности и аварийного восстановления.</span><span class="sxs-lookup"><span data-stu-id="a7406-108">As shown in the following table, both editions support all functionality in all workloads, except for high availability and disaster recovery.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a7406-109">Компонент</span><span class="sxs-lookup"><span data-stu-id="a7406-109">Feature</span></span></th>
<th><span data-ttu-id="a7406-110">Поддерживается в корпоративном выпуске?</span><span class="sxs-lookup"><span data-stu-id="a7406-110">Supported in Enterprise Edition?</span></span></th>
<th><span data-ttu-id="a7406-111">Поддерживается в стандартном выпуске?</span><span class="sxs-lookup"><span data-stu-id="a7406-111">Supported in Standard Edition?</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a7406-112">Обмен мгновенными сообщениями и присутствие</span><span class="sxs-lookup"><span data-stu-id="a7406-112">Instant messaging (IM) and presence</span></span></p></td>
<td><p><span data-ttu-id="a7406-113">Да</span><span class="sxs-lookup"><span data-stu-id="a7406-113">Yes</span></span></p></td>
<td><p><span data-ttu-id="a7406-114">Да</span><span class="sxs-lookup"><span data-stu-id="a7406-114">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a7406-115">Конференц-связь</span><span class="sxs-lookup"><span data-stu-id="a7406-115">Conferencing</span></span></p></td>
<td><p><span data-ttu-id="a7406-116">Да</span><span class="sxs-lookup"><span data-stu-id="a7406-116">Yes</span></span></p></td>
<td><p><span data-ttu-id="a7406-117">Да</span><span class="sxs-lookup"><span data-stu-id="a7406-117">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a7406-118">A/V conferencing (Аудио- и видеоконференции)</span><span class="sxs-lookup"><span data-stu-id="a7406-118">A/V conferencing</span></span></p></td>
<td><p><span data-ttu-id="a7406-119">Да</span><span class="sxs-lookup"><span data-stu-id="a7406-119">Yes</span></span></p></td>
<td><p><span data-ttu-id="a7406-120">Да</span><span class="sxs-lookup"><span data-stu-id="a7406-120">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a7406-121">Конференц-связь с телефонным подключением</span><span class="sxs-lookup"><span data-stu-id="a7406-121">Dial-in conferencing</span></span></p></td>
<td><p><span data-ttu-id="a7406-122">Да</span><span class="sxs-lookup"><span data-stu-id="a7406-122">Yes</span></span></p></td>
<td><p><span data-ttu-id="a7406-123">Да</span><span class="sxs-lookup"><span data-stu-id="a7406-123">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a7406-124">Корпоративная голосовая связь</span><span class="sxs-lookup"><span data-stu-id="a7406-124">Enterprise Voice</span></span></p></td>
<td><p><span data-ttu-id="a7406-125">Да</span><span class="sxs-lookup"><span data-stu-id="a7406-125">Yes</span></span></p></td>
<td><p><span data-ttu-id="a7406-126">Да</span><span class="sxs-lookup"><span data-stu-id="a7406-126">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a7406-127">Виртуализаци</span><span class="sxs-lookup"><span data-stu-id="a7406-127">Virtualization</span></span></p></td>
<td><p><span data-ttu-id="a7406-128">Да</span><span class="sxs-lookup"><span data-stu-id="a7406-128">Yes</span></span></p></td>
<td><p><span data-ttu-id="a7406-129">Да</span><span class="sxs-lookup"><span data-stu-id="a7406-129">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a7406-130">Высокий уровень доступности, отказов и аварийного восстановления</span><span class="sxs-lookup"><span data-stu-id="a7406-130">High availability, failover, and disaster recovery</span></span></p></td>
<td><p><span data-ttu-id="a7406-131">Да</span><span class="sxs-lookup"><span data-stu-id="a7406-131">Yes</span></span></p></td>
<td><p><span data-ttu-id="a7406-132">Нет</span><span class="sxs-lookup"><span data-stu-id="a7406-132">No</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="a7406-133">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a7406-133">


</div>

<span> </span>

</div>

</div>

</span></span></div>

