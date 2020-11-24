---
title: Удаление экземпляров и баз данных SQL Server на внутреннем сервере
description: Удаление экземпляров и баз данных SQL Server на обратном стороне сервера.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Remove SQL Server instances and databases on the Back End Server
ms:assetid: 32457df9-7dd9-4fca-9362-ea4de26b0296
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688016(v=OCS.15)
ms:contentKeyID: 49733606
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c87426a3496e6def2ad65775f5dadb1a0141ae3f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49400096"
---
# <a name="remove-sql-server-instances-and-databases-on-the-back-end-server"></a><span data-ttu-id="85b31-103">Удаление экземпляров и баз данных SQL Server на внутреннем сервере</span><span class="sxs-lookup"><span data-stu-id="85b31-103">Remove SQL Server instances and databases on the Back End Server</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="85b31-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="85b31-104">

<span> </span></span></span>

<span data-ttu-id="85b31-105">_**Тема последнего изменения:** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="85b31-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="85b31-106">Вы удаляете базы данных и экземпляры Microsoft SQL Server после удаления серверов с Lync Server 2010, которые зависят от них, или после перенастройки серверов с Lync Server 2010 для использования другой базы данных.</span><span class="sxs-lookup"><span data-stu-id="85b31-106">You remove the Microsoft SQL Server databases and instances after you remove the servers running Lync Server 2010 that are dependent on them, or after you reconfigure the servers running Lync Server 2010 to use another database.</span></span> <span data-ttu-id="85b31-107">При отмене текущего SQL Server или изменении конфигурации текущего сервера, на котором работает Lync Server 2010, необходимо выполнить описанные ниже действия, чтобы сделать базы данных устаревшими или недоступными.</span><span class="sxs-lookup"><span data-stu-id="85b31-107">You need to perform the procedure in this topic when you retire the current SQL Server or reconfigure the current server running Lync Server 2010 in such a way that it renders the databases obsolete or unavailable.</span></span>

<span data-ttu-id="85b31-108">Чтобы удалить базы данных или экземпляры сервера архивирования или сервера мониторинга, необходимо сначала удалить роль сервера.</span><span class="sxs-lookup"><span data-stu-id="85b31-108">To remove the databases or instances for the Archiving Server or Monitoring Server, you must first remove the server role.</span></span> <span data-ttu-id="85b31-109">Аналогичным образом для удаления экземпляров или баз данных в пуле переднего плана необходимо сначала удалить или перенастроить роль зависимого сервера.</span><span class="sxs-lookup"><span data-stu-id="85b31-109">Similarly, to remove the instances or databases for Front End pool, you must first remove or reconfigure the dependent server role.</span></span> <span data-ttu-id="85b31-110">Эти процедуры не различаются между выровненными базами данных и отдельными экземплярами серверов.</span><span class="sxs-lookup"><span data-stu-id="85b31-110">These procedures make no distinction between collocated databases or separate instances for servers.</span></span> <span data-ttu-id="85b31-111">Расгруппировка баз данных не влияет на эти процедуры.</span><span class="sxs-lookup"><span data-stu-id="85b31-111">The procedures are unaffected by the collocation of databases.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="85b31-112">Содержание</span><span class="sxs-lookup"><span data-stu-id="85b31-112">In This Section</span></span>

  - [<span data-ttu-id="85b31-113">Удаление базы данных SQL Server для пула переднего плана</span><span class="sxs-lookup"><span data-stu-id="85b31-113">Remove the SQL Server database for a Front End pool</span></span>](remove-the-sql-server-database-for-a-front-end-pool.md)

  - [<span data-ttu-id="85b31-114">Удаление базы данных SQL Server для сервера мониторинга</span><span class="sxs-lookup"><span data-stu-id="85b31-114">Remove the SQL Server database for a Monitoring server</span></span>](remove-the-sql-server-database-for-a-monitoring-server.md)

  - [<span data-ttu-id="85b31-115">Удаление базы данных SQL Server для сервера архивирования</span><span class="sxs-lookup"><span data-stu-id="85b31-115">Remove the SQL Server database for an Archiving server</span></span>](remove-the-sql-server-database-for-an-archiving-server.md)

<span data-ttu-id="85b31-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="85b31-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

