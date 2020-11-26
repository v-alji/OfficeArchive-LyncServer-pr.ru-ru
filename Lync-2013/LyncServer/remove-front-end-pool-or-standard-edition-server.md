---
title: Удаление пула переднего плана или сервера Standard Edition
description: Удалите интерфейс пула переднего плана или сервер Standard Edition.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Remove Front End pool or Standard Edition server
ms:assetid: 83c39a36-49a1-4ac6-9cc5-b0e441b1fdec
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688115(v=OCS.15)
ms:contentKeyID: 49733713
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c878d56b073558f4f4b50f31b6742fd581c80241
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440278"
---
# <a name="remove-front-end-pool-or-standard-edition-server"></a><span data-ttu-id="31c18-103">Удаление пула переднего плана или сервера Standard Edition</span><span class="sxs-lookup"><span data-stu-id="31c18-103">Remove Front End pool or Standard Edition server</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="31c18-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="31c18-104">

<span> </span></span></span>

<span data-ttu-id="31c18-105">_**Тема последнего изменения:** 2012-10-04_</span><span class="sxs-lookup"><span data-stu-id="31c18-105">_**Topic Last Modified:** 2012-10-04_</span></span>

<span data-ttu-id="31c18-106">В этой статье описано, как удалить интерфейс переднего плана или сервер стандартного выпуска Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="31c18-106">This topic guides you through the process of removing a Front End pool or a Standard Edition Front End Server.</span></span> <span data-ttu-id="31c18-107">При удалении пула переднего плана удаляется каждый сервер переднего плана, который входит в состав пула, в процессе удаления пула.</span><span class="sxs-lookup"><span data-stu-id="31c18-107">When you remove a Front End pool, you remove each Front End Server that belongs to the pool as a part of the pool removal process.</span></span> <span data-ttu-id="31c18-108">При удалении стандартного внешнего сервера выпусков необходимо удалить определение хранилища SQL из построителя топологии.</span><span class="sxs-lookup"><span data-stu-id="31c18-108">When you remove a Standard Edition Front End Server, you must remove the SQL Store definition from Topology Builder.</span></span>

<div>

## <a name="to-remove-a-front-end-server-pool"></a><span data-ttu-id="31c18-109">Удаление пула серверов переднего плана</span><span class="sxs-lookup"><span data-stu-id="31c18-109">To remove a Front End Server pool</span></span>

1.  <span data-ttu-id="31c18-110">Открытие построителя топологии.</span><span class="sxs-lookup"><span data-stu-id="31c18-110">Open Topology Builder.</span></span>

2.  <span data-ttu-id="31c18-111">Перейдите на узел Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="31c18-111">Navigate to the Lync Server 2010 node.</span></span>

3.  <span data-ttu-id="31c18-112">Разверните **Пулы переднего плана Enterprise Edition**, разверните пул переднего плана, щелкните правой кнопкой мыши пул переднего плана, который вы хотите удалить, и выберите команду **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="31c18-112">Expand **Enterprise Edition Front End pools**, expand the Front End pool, right-click the Front End pool that you want to remove, and then click **Delete**.</span></span>

4.  <span data-ttu-id="31c18-113">Опубликуйте топологию, проверьте состояние репликации, а затем при необходимости запустите мастер развертывания Lync Server.</span><span class="sxs-lookup"><span data-stu-id="31c18-113">Publish the topology, check replication status, and then run the Lync Server Deployment Wizard as needed.</span></span>

</div>

<div>

## <a name="to-remove-a-standard-edition-front-end-server"></a><span data-ttu-id="31c18-114">Удаление стандартного внешнего сервера выпуска</span><span class="sxs-lookup"><span data-stu-id="31c18-114">To remove a Standard Edition Front End server</span></span>

1.  <span data-ttu-id="31c18-115">Открытие построителя топологии.</span><span class="sxs-lookup"><span data-stu-id="31c18-115">Open Topology Builder.</span></span>

2.  <span data-ttu-id="31c18-116">Перейдите на узел Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="31c18-116">Navigate to the Lync Server 2010 node.</span></span>

3.  <span data-ttu-id="31c18-117">Разверните узел **стандартные базовые серверы выпусков**, щелкните правой кнопкой мыши сервер переднего плана, который вы хотите удалить, и выберите команду **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="31c18-117">Expand **Standard Edition Front End servers**, right-click the Front End Server that you want to remove, and then click **Delete**.</span></span>

4.  <span data-ttu-id="31c18-118">Разверните **хранилища SQL**, щелкните правой кнопкой мыши базу данных SQL Server, связанную со стандартным сервером переднего плана выпуска, и выберите команду **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="31c18-118">Expand **SQL stores**, right-click the SQL Server database that is associated with the Standard Edition Front End Server, and then click **Delete**.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="31c18-119">Необходимо удалить определение размещенных баз данных SQL Server на стандартном внешнем сервере выпуска.</span><span class="sxs-lookup"><span data-stu-id="31c18-119">You must remove the definition of the collocated SQL Server databases from the Standard Edition Front End Server.</span></span>

    
    </div>

5.  <span data-ttu-id="31c18-120">Опубликуйте топологию, проверьте состояние репликации, а затем при необходимости запустите мастер развертывания Lync Server.</span><span class="sxs-lookup"><span data-stu-id="31c18-120">Publish the topology, check replication status, and then run the Lync Server Deployment Wizard as needed.</span></span>

<span data-ttu-id="31c18-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="31c18-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

