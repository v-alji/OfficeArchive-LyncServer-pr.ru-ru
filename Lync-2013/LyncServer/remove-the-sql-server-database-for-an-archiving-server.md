---
title: Удаление базы данных SQL Server для сервера архивирования
description: Удалите базу данных SQL Server для сервера архивирования.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Remove the SQL Server database for an Archiving server
ms:assetid: 6e8a1fcd-ed09-43b0-82c9-60e7ce116a01
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688087(v=OCS.15)
ms:contentKeyID: 49733686
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 738f82f297e1ccb3c6f23f9ecea25657d409f0a6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440250"
---
# <a name="remove-the-sql-server-database-for-an-archiving-server"></a><span data-ttu-id="cc119-103">Удаление базы данных SQL Server для сервера архивирования</span><span class="sxs-lookup"><span data-stu-id="cc119-103">Remove the SQL Server database for an Archiving server</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cc119-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cc119-104">

<span> </span></span></span>

<span data-ttu-id="cc119-105">_**Тема последнего изменения:** 2012-10-04_</span><span class="sxs-lookup"><span data-stu-id="cc119-105">_**Topic Last Modified:** 2012-10-04_</span></span>

<span data-ttu-id="cc119-106">После удаления сервера архивации Microsoft Lync Server 2010 вы можете удалить базы данных SQL Server, на которых размещены данные пула.</span><span class="sxs-lookup"><span data-stu-id="cc119-106">After you remove a Microsoft Lync Server 2010 Archiving Server, you can remove the SQL Server databases that hosted the pool data.</span></span> <span data-ttu-id="cc119-107">Используйте описанные ниже процедуры для удаления определений из построителя топологии и удаления файлов базы данных и журнала с сервера базы данных.</span><span class="sxs-lookup"><span data-stu-id="cc119-107">Use the following procedures to remove the definitions from Topology Builder, and then remove the database and log files from the database server.</span></span>

<div>

## <a name="to-remove-the-sql-server-database-using-topology-builder"></a><span data-ttu-id="cc119-108">Удаление базы данных SQL Server с помощью построителя топологии</span><span class="sxs-lookup"><span data-stu-id="cc119-108">To remove the SQL Server database using Topology Builder</span></span>

1.  <span data-ttu-id="cc119-109">На сервере переднего плана Lync Server 2013 откройте "Построитель топологии".</span><span class="sxs-lookup"><span data-stu-id="cc119-109">On the Lync Server 2013 Front End Server, open Topology Builder.</span></span>

2.  <span data-ttu-id="cc119-110">В построителе топологии откройте раздел **Общие компоненты** , а затем — **хранилище SQL Server**, щелкните правой кнопкой мыши экземпляр SQL Server, связанный с удаленным или перенастроенным сервером архивации, а затем выберите команду **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="cc119-110">In Topology Builder, navigate to **Shared Components** and then **SQL Server Stores**, right-click the SQL Server instance associated with the removed or reconfigured Archiving Server, and then click **Delete**.</span></span>

3.  <span data-ttu-id="cc119-111">Опубликуйте топологию и проверьте состояние репликации.</span><span class="sxs-lookup"><span data-stu-id="cc119-111">Publish the topology, and then check replication status.</span></span>

</div>

<div>

## <a name="to-remove-the-database-files-from-the-sql-server"></a><span data-ttu-id="cc119-112">Удаление файлов базы данных из SQL Server</span><span class="sxs-lookup"><span data-stu-id="cc119-112">To remove the database files from the SQL Server</span></span>

1.  <span data-ttu-id="cc119-113">Для удаления баз данных на сервере SQL Server необходимо быть членом группы "Администраторы SQL Server" для сервера SQL Server, на котором нужно удалить файлы базы данных.</span><span class="sxs-lookup"><span data-stu-id="cc119-113">To remove the databases on the SQL Server, you must be a member of the SQL Server sysadmins group for the SQL Server where you are removing the database files.</span></span>

2.  <span data-ttu-id="cc119-114">Откройте командную консоль Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="cc119-114">Open the Lync Server Management Shell.</span></span>

3.  <span data-ttu-id="cc119-115">В командной строке введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="cc119-115">At the command line, type the following:</span></span>
    
        Uninstall-CsDataBase -DatabaseType Archiving -SqlServerFqdn <FQDN> [-SqlInstanceName <instance>]
    
    <span data-ttu-id="cc119-116">Здесь \<FQDN\> указано полное доменное имя сервера базы данных (FQDN) и \<instance\> — именованный экземпляр базы данных (то есть, если он был определен).</span><span class="sxs-lookup"><span data-stu-id="cc119-116">Where \<FQDN\> is the fully qualified domain name (FQDN) of the database server, and \<instance\> is the named database instance (that is, if one was defined).</span></span>

4.  <span data-ttu-id="cc119-117">Когда командлет **uninstall-CsDataBase** предложит вам подтвердить действия, прочтите информацию, а затем нажмите клавишу **Y** (или клавишу ВВОД), чтобы продолжить, **или клавишу с, чтобы** остановить командлет (то есть ошибки).</span><span class="sxs-lookup"><span data-stu-id="cc119-117">When the **Uninstall-CsDataBase** cmdlet prompts you to confirm actions, read the information, and then press **Y** (or press Enter) to proceed, or press **N** and then Enter if you want to stop the cmdlet (that is, in case there errors).</span></span>

<span data-ttu-id="cc119-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cc119-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

