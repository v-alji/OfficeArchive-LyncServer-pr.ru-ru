---
title: 'Lync Server 2013: представление ConferenceMessageCount'
description: 'Lync Server 2013: ConferenceMessageCount View.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ConferenceMessageCount view
ms:assetid: 8ee3ee95-fb78-4d4e-bcdd-6ce5a0a23b44
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688129(v=OCS.15)
ms:contentKeyID: 49733727
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 212d6e1a346253809fb70806424350cc7fc0dfe2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434433"
---
# <a name="conferencemessagecount-view-in-lync-server-2013"></a><span data-ttu-id="6ca44-103">ConferenceMessageCount представления в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6ca44-103">ConferenceMessageCount view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6ca44-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6ca44-104">

<span> </span></span></span>

<span data-ttu-id="6ca44-105">_**Тема последнего изменения:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="6ca44-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="6ca44-106">В представлении ConferenceMessageCount хранятся сведения о количестве сообщений, отправленных пользователем на конференцию.</span><span class="sxs-lookup"><span data-stu-id="6ca44-106">The ConferenceMessageCount view stores information about how many messages were sent by a user to a conference.</span></span> <span data-ttu-id="6ca44-107">Это представление было представлено в Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6ca44-107">This view was introduced in Microsoft Lync Server 2013.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="6ca44-108">В представлении ConferenceMessageCount содержатся все столбцы в <A href="lync-server-2013-conferencesessiondetails-view.md">представлении ConferenceSessionDetails в Lync Server 2013</A> в дополнение к столбцам, перечисленным ниже.</span><span class="sxs-lookup"><span data-stu-id="6ca44-108">The ConferenceMessageCount view contains all of the columns in the <A href="lync-server-2013-conferencesessiondetails-view.md">ConferenceSessionDetails view in Lync Server 2013</A> in addition the columns listed below.</span></span>



</div>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6ca44-109">Столбец</span><span class="sxs-lookup"><span data-stu-id="6ca44-109">Column</span></span></th>
<th><span data-ttu-id="6ca44-110">Тип данных</span><span class="sxs-lookup"><span data-stu-id="6ca44-110">Data Type</span></span></th>
<th><span data-ttu-id="6ca44-111">Подробности</span><span class="sxs-lookup"><span data-stu-id="6ca44-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6ca44-112"><strong>UserUri</strong></span><span class="sxs-lookup"><span data-stu-id="6ca44-112"><strong>UserUri</strong></span></span></p></td>
<td><p><span data-ttu-id="6ca44-113">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="6ca44-113">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="6ca44-114">Универсальный код ресурса (URI) пользователя, отправившего сообщение.</span><span class="sxs-lookup"><span data-stu-id="6ca44-114">URI of the user who sent the message.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ca44-115"><strong>UserUriType</strong></span><span class="sxs-lookup"><span data-stu-id="6ca44-115"><strong>UserUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="6ca44-116">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="6ca44-116">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="6ca44-117">Тип URI пользователя, отправившего сообщения.</span><span class="sxs-lookup"><span data-stu-id="6ca44-117">Type of URI of the user who sent the messages.</span></span> <span data-ttu-id="6ca44-118">Для получения дополнительных сведений ознакомьтесь с <a href="lync-server-2013-uritypes-table.md">таблицей UriTypes в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="6ca44-118">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ca44-119"><strong>UserTenant</strong></span><span class="sxs-lookup"><span data-stu-id="6ca44-119"><strong>UserTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="6ca44-120">идентификатора</span><span class="sxs-lookup"><span data-stu-id="6ca44-120">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="6ca44-121">Клиент пользователя, отправившего сообщения.</span><span class="sxs-lookup"><span data-stu-id="6ca44-121">Tenant of user who sent the messages.</span></span> <span data-ttu-id="6ca44-122">Дополнительные сведения приведены в <a href="lync-server-2013-tenants-table.md">таблице "клиенты" в Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="6ca44-122">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ca44-123"><strong>UserMessageCount</strong></span><span class="sxs-lookup"><span data-stu-id="6ca44-123"><strong>UserMessageCount</strong></span></span></p></td>
<td><p><span data-ttu-id="6ca44-124">smallint</span><span class="sxs-lookup"><span data-stu-id="6ca44-124">smallint</span></span></p></td>
<td><p><span data-ttu-id="6ca44-125">Количество сообщений, отправленных пользователем во время сеанса конференции.</span><span class="sxs-lookup"><span data-stu-id="6ca44-125">Number of messages sent by the user during the conference session.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="6ca44-126">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6ca44-126">


</div>

<span> </span>

</div>

</div>

</span></span></div>

