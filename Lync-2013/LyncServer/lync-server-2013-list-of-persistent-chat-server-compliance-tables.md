---
title: 'Lync Server 2013: список таблиц соблюдения требований для сервера сохраняемого чата'
description: 'Lync Server 2013: список таблиц соответствия требованиям сервера для работы с постоянной версией чата.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: List of Persistent Chat Server compliance tables
ms:assetid: 8563446e-90cc-47cc-8a8e-4883decfe195
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ215878(v=OCS.15)
ms:contentKeyID: 48706007
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 47cb28a0ca4180327c2adc48d80e9e41171a7bfc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426580"
---
# <a name="list-of-persistent-chat-server-compliance-tables-in-lync-server-2013"></a><span data-ttu-id="b375f-103">Список таблиц соблюдения требований для сервера сохраняемого чата в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b375f-103">List of Persistent Chat Server compliance tables in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b375f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b375f-104">

<span> </span></span></span>

<span data-ttu-id="b375f-105">_**Тема последнего изменения:** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="b375f-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="b375f-106">Схема базы данных соответствия требованиям к сохраненным Чатам состоит из следующих таблиц.</span><span class="sxs-lookup"><span data-stu-id="b375f-106">The Persistent Chat compliance database schema consists of the following tables.</span></span>

<div>

## <a name="list-of-persistent-chat-server-compliance-tables"></a><span data-ttu-id="b375f-107">Список таблиц соответствия требованиям сервера для работы с постоянной версией чата</span><span class="sxs-lookup"><span data-stu-id="b375f-107">List of Persistent Chat Server Compliance Tables</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b375f-108">Таблица</span><span class="sxs-lookup"><span data-stu-id="b375f-108">Table</span></span></th>
<th><span data-ttu-id="b375f-109">Описание</span><span class="sxs-lookup"><span data-stu-id="b375f-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b375f-110"><a href="lync-server-2013-tblcompliancedata.md">tblComplianceData в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="b375f-110"><a href="lync-server-2013-tblcompliancedata.md">tblComplianceData in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="b375f-111">Содержит события соответствия требованиям, которые еще не были обработаны настроенным адаптером.</span><span class="sxs-lookup"><span data-stu-id="b375f-111">Contains the compliance events that have not yet been processed by the configured adapter.</span></span></p>
<p><span data-ttu-id="b375f-112">В этой таблице содержатся сохраняемые события, связанные с чат, такие как сообщения чата и загружаемые файлы.</span><span class="sxs-lookup"><span data-stu-id="b375f-112">This table includes Persistent Chat-related events, such as chat messages and file downloads.</span></span> <span data-ttu-id="b375f-113">(События участников отслеживаются таблицей tblComplianceParticipant.)</span><span class="sxs-lookup"><span data-stu-id="b375f-113">(Participant events are tracked by the tblComplianceParticipant table.)</span></span></p>
<p><span data-ttu-id="b375f-114">(Серверы, обработавшие события в этой таблице, перечислены в таблице tblComplianceFanout).</span><span class="sxs-lookup"><span data-stu-id="b375f-114">(The servers that processed the events in this table are listed in the tblComplianceFanout table.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b375f-115"><a href="lync-server-2013-tblcompliancefanout.md">tblComplianceFanout в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="b375f-115"><a href="lync-server-2013-tblcompliancefanout.md">tblComplianceFanout in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="b375f-116">Содержат серверы, которые обрабатывали событие соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="b375f-116">Contains the servers that processed a compliance event.</span></span> <span data-ttu-id="b375f-117">Эта таблица тесно связана с таблицей tblComplianceData.</span><span class="sxs-lookup"><span data-stu-id="b375f-117">This table is tightly coupled with the tblComplianceData table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b375f-118"><a href="lync-server-2013-tblcomplianceparticipant.md">tblComplianceParticipant в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="b375f-118"><a href="lync-server-2013-tblcomplianceparticipant.md">tblComplianceParticipant in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="b375f-119">Включает в себя текущих участников для каждой службы чата и для каждого сервера.</span><span class="sxs-lookup"><span data-stu-id="b375f-119">Contains current participants per chat service and per server.</span></span> <span data-ttu-id="b375f-120">Она поддерживается на основе событий присоединения и частей соответствия, полученных от службы сохраняемого чата.</span><span class="sxs-lookup"><span data-stu-id="b375f-120">It is maintained based on join and part compliance events received from the Persistent Chat service.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b375f-121"><a href="lync-server-2013-tblcompliancestate.md">tblComplianceState в Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="b375f-121"><a href="lync-server-2013-tblcompliancestate.md">tblComplianceState in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="b375f-122">Сведения о состоянии соответствия требованиям всего пула.</span><span class="sxs-lookup"><span data-stu-id="b375f-122">Contains pool-wide compliance state information.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="b375f-123">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b375f-123">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

