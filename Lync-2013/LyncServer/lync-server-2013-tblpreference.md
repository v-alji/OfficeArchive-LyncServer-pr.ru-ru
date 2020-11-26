---
title: 'Lync Server 2013: tblPreference'
description: 'Lync Server 2013: tblPreference.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblPreference
ms:assetid: f94eb128-f782-42ff-a568-ed3529573bc8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615052(v=OCS.15)
ms:contentKeyID: 48185913
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 86e8b81a6af93e9bf1d7673e54492579a1bed08e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441377"
---
# <a name="tblpreference-in-lync-server-2013"></a><span data-ttu-id="a9f50-103">tblPreference в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a9f50-103">tblPreference in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a9f50-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a9f50-104">

<span> </span></span></span>

<span data-ttu-id="a9f50-105">_**Тема последнего изменения:** 2012-09-24_</span><span class="sxs-lookup"><span data-stu-id="a9f50-105">_**Topic Last Modified:** 2012-09-24_</span></span>

<span data-ttu-id="a9f50-106">tblPreference включает клиентские настройки пользователей.</span><span class="sxs-lookup"><span data-stu-id="a9f50-106">tblPreference contains the users’ client preferences.</span></span> <span data-ttu-id="a9f50-107">Обычно используется клиентами, предшествующими Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="a9f50-107">This is generally used by clients previous to Lync 2013.</span></span>

### <a name="columns"></a><span data-ttu-id="a9f50-108">Столбцов</span><span class="sxs-lookup"><span data-stu-id="a9f50-108">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a9f50-109">Столбец</span><span class="sxs-lookup"><span data-stu-id="a9f50-109">Column</span></span></th>
<th><span data-ttu-id="a9f50-110">Тип</span><span class="sxs-lookup"><span data-stu-id="a9f50-110">Type</span></span></th>
<th><span data-ttu-id="a9f50-111">Описание</span><span class="sxs-lookup"><span data-stu-id="a9f50-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a9f50-112">prefLabel</span><span class="sxs-lookup"><span data-stu-id="a9f50-112">prefLabel</span></span></p></td>
<td><p><span data-ttu-id="a9f50-113">nvarchar (255), NOT NULL</span><span class="sxs-lookup"><span data-stu-id="a9f50-113">nvarchar (255), not null</span></span></p></td>
<td><p><span data-ttu-id="a9f50-114">Надпись с таким же форматом, как: &lt; URI SIP пользователя &gt; , | имя пользователя. &lt; Наборы параметров &gt; .</span><span class="sxs-lookup"><span data-stu-id="a9f50-114">Label with a format such as: &lt;user sip uri&gt;|username.&lt;preference set&gt;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9f50-115">prefSeqID</span><span class="sxs-lookup"><span data-stu-id="a9f50-115">prefSeqID</span></span></p></td>
<td><p><span data-ttu-id="a9f50-116">int, NOT NULL</span><span class="sxs-lookup"><span data-stu-id="a9f50-116">int, not null</span></span></p></td>
<td><p><span data-ttu-id="a9f50-117">Последовательный номер (на метку) для целей управления версиями.</span><span class="sxs-lookup"><span data-stu-id="a9f50-117">A sequential number (per label) for versioning purposes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9f50-118">prefContent</span><span class="sxs-lookup"><span data-stu-id="a9f50-118">prefContent</span></span></p></td>
<td><p><span data-ttu-id="a9f50-119">nvarchar (max)</span><span class="sxs-lookup"><span data-stu-id="a9f50-119">nvarchar (max)</span></span></p></td>
<td><p><span data-ttu-id="a9f50-120">Закодированное содержимое.</span><span class="sxs-lookup"><span data-stu-id="a9f50-120">Encoded content.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9f50-121">lastModifiedBy</span><span class="sxs-lookup"><span data-stu-id="a9f50-121">lastModifiedBy</span></span></p></td>
<td><p><span data-ttu-id="a9f50-122">int, NOT NULL</span><span class="sxs-lookup"><span data-stu-id="a9f50-122">int, not null</span></span></p></td>
<td><p><span data-ttu-id="a9f50-123">Идентификатор участника, который обновил предпочтение.</span><span class="sxs-lookup"><span data-stu-id="a9f50-123">ID of the principal that updated the preference.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="key"></a><span data-ttu-id="a9f50-124">Ключ</span><span class="sxs-lookup"><span data-stu-id="a9f50-124">Key</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a9f50-125">Столбец</span><span class="sxs-lookup"><span data-stu-id="a9f50-125">Column</span></span></th>
<th><span data-ttu-id="a9f50-126">Описание</span><span class="sxs-lookup"><span data-stu-id="a9f50-126">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a9f50-127">&lt;prefLabel, prefSeqID&gt;</span><span class="sxs-lookup"><span data-stu-id="a9f50-127">&lt;prefLabel, prefSeqID&gt;</span></span></p></td>
<td><p><span data-ttu-id="a9f50-128">Первичный ключ.</span><span class="sxs-lookup"><span data-stu-id="a9f50-128">Primary key.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="a9f50-129">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a9f50-129">


</div>

<span> </span>

</div>

</div>

</span></span></div>

