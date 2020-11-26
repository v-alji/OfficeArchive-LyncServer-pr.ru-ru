---
title: Удаление базы данных SQL Server для сервера мониторинга
description: Удалите базу данных SQL Server для сервера мониторинга.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Remove the SQL Server database for a Monitoring server
ms:assetid: aed5e394-d63e-4ad4-af40-f12d3a044344
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721848(v=OCS.15)
ms:contentKeyID: 49733781
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 99bf734f0a9978fe14055fb36b01ce37f77e14a8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440257"
---
# <a name="remove-the-sql-server-database-for-a-monitoring-server"></a><span data-ttu-id="4854f-103">Удаление базы данных SQL Server для сервера мониторинга</span><span class="sxs-lookup"><span data-stu-id="4854f-103">Remove the SQL Server database for a Monitoring server</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4854f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4854f-104">

<span> </span></span></span>

<span data-ttu-id="4854f-105">_**Тема последнего изменения:** 2012-10-04_</span><span class="sxs-lookup"><span data-stu-id="4854f-105">_**Topic Last Modified:** 2012-10-04_</span></span>

<span data-ttu-id="4854f-106">После удаления сервера мониторинга Microsoft Lync Server 2010 вы можете удалить базы данных SQL Server, на которых размещены данные сервера.</span><span class="sxs-lookup"><span data-stu-id="4854f-106">After you remove a Microsoft Lync Server 2010 Monitoring Server, you can remove the SQL Server databases that hosted the server data.</span></span> <span data-ttu-id="4854f-107">Используйте описанные ниже процедуры для удаления определений из построителя топологии и удаления файлов базы данных и журнала с сервера базы данных.</span><span class="sxs-lookup"><span data-stu-id="4854f-107">Use the following procedures to remove the definitions from Topology Builder, and then remove the database and log files from the database server.</span></span>

<div>

## <a name="to-remove-the-sql-server-database-using-topology-builder"></a><span data-ttu-id="4854f-108">Удаление базы данных SQL Server с помощью построителя топологии</span><span class="sxs-lookup"><span data-stu-id="4854f-108">To remove the SQL Server database using Topology Builder</span></span>

1.  <span data-ttu-id="4854f-109">На сервере переднего плана Lync Server 2013 откройте "Построитель топологии".</span><span class="sxs-lookup"><span data-stu-id="4854f-109">On the Lync Server 2013 Front End Server, open Topology Builder.</span></span>

2.  <span data-ttu-id="4854f-110">В построителе топологии откройте раздел **Общие компоненты** , а затем — **хранилище SQL Server**, щелкните правой кнопкой мыши экземпляр SQL Server, связанный с удаленным или перенастроенным сервером мониторинга, и выберите команду **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="4854f-110">In Topology Builder, navigate to **Shared Components** and then **SQL Server Stores**, right-click the SQL Server instance associated with the removed or reconfigured Monitoring Server, and then click **Delete**.</span></span>

3.  <span data-ttu-id="4854f-111">Опубликуйте топологию и проверьте состояние репликации.</span><span class="sxs-lookup"><span data-stu-id="4854f-111">Publish the topology, and then check replication status.</span></span>

</div>

<div>

## <a name="to-remove-the-database-files-from-the-sql-server"></a><span data-ttu-id="4854f-112">Удаление файлов базы данных из SQL Server</span><span class="sxs-lookup"><span data-stu-id="4854f-112">To remove the database files from the SQL Server</span></span>

1.  <span data-ttu-id="4854f-113">Для удаления баз данных на сервере SQL Server необходимо быть членом группы "Администраторы SQL Server" для сервера SQL Server, на котором нужно удалить файлы базы данных.</span><span class="sxs-lookup"><span data-stu-id="4854f-113">To remove the databases on the SQL Server-based server, you must be a member of the SQL Server sysadmins group for the SQL Server server where you are removing the database files.</span></span>

2.  <span data-ttu-id="4854f-114">Откройте командную консоль Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="4854f-114">Open the Lync Server Management Shell.</span></span>

3.  <span data-ttu-id="4854f-115">В командной строке введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="4854f-115">At the command line, type the following:</span></span>
    
        Uninstall-CsDataBase -DatabaseType Monitoring -SqlServerFqdn <FQDN> [-SqlInstanceName <instance>]
    
    <span data-ttu-id="4854f-116">Где \<FQDN\> находится полное доменное имя сервера базы данных и \<instance\> является необязательным именем экземпляра базы данных.</span><span class="sxs-lookup"><span data-stu-id="4854f-116">Where \<FQDN\> is the fully qualified domain name (FQDN) of the database server, and \<instance\> is the optional named database instance.</span></span>

4.  <span data-ttu-id="4854f-117">Когда командлет **uninstall-CsDataBase** предложит вам подтвердить действия, прочтите информацию, а затем нажмите клавишу **Y** (или клавишу ВВОД), чтобы продолжить, **или клавишу с, чтобы** остановить командлет (то есть ошибки).</span><span class="sxs-lookup"><span data-stu-id="4854f-117">When the **Uninstall-CsDataBase** cmdlet prompts you to confirm actions, read the information, and then press **Y** (or press Enter) to proceed, or press **N** and then Enter if you want to stop the cmdlet (that is, in case there errors).</span></span>

<span data-ttu-id="4854f-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4854f-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

