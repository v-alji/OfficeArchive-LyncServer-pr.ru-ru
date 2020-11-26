---
title: 'Lync Server 2013: отработка отказа с использованием зеркальной базы данных'
description: 'Lync Server 2013: переход на зеркальную базу данных завершается сбоем.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Failing over a mirrored database
ms:assetid: 70185476-e3d4-440a-9316-fa24b226343e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204991(v=OCS.15)
ms:contentKeyID: 48184450
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fc7c401157c79762f674721ca717296c0fe502db
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428295"
---
# <a name="failing-over-a-mirrored-database-in-lync-server-2013"></a><span data-ttu-id="17c59-103">Отработка отказа с использованием зеркальной базы данных в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="17c59-103">Failing over a mirrored database in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="17c59-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="17c59-104">

<span> </span></span></span>

<span data-ttu-id="17c59-105">_**Тема последнего изменения:** 2014-03-14_</span><span class="sxs-lookup"><span data-stu-id="17c59-105">_**Topic Last Modified:** 2014-03-14_</span></span>

<span data-ttu-id="17c59-106">Если вы настроили серверную базу данных для использования синхронизированного отражения с следящим сервером, переход на другой ресурс выполняется автоматически.</span><span class="sxs-lookup"><span data-stu-id="17c59-106">If you have configured your back-end database to use synchronized mirroring with a witness, failover is automatic.</span></span> <span data-ttu-id="17c59-107">Если вы настроили синхронизацию зеркального отображения без следящего сервера, вы можете использовать следующие процедуры для перемещения по резервной копии и восстановления базы данных.</span><span class="sxs-lookup"><span data-stu-id="17c59-107">If you have configured synchronized mirroring without a witness, you can use the following procedures to failover and failback your database.</span></span> <span data-ttu-id="17c59-108">Вы также можете использовать эти процедуры для перемещения по резервной конфигурации вручную и восстановления баз данных, даже если вы настроили следящий сервер.</span><span class="sxs-lookup"><span data-stu-id="17c59-108">You can also use these procedures to manually failover and failback your databases even if you have configured a witness.</span></span>

<div>

## <a name="to-fail-over-your-back-end-database"></a><span data-ttu-id="17c59-109">Переключение на серверную базу данных</span><span class="sxs-lookup"><span data-stu-id="17c59-109">To fail over your back-end database</span></span>

1.  <span data-ttu-id="17c59-110">Прежде чем переходить, определите, какая серверная база данных является участником и что является зеркалом, введя следующий командлет:</span><span class="sxs-lookup"><span data-stu-id="17c59-110">Before failing over, determine which back-end database is the principal and which is the mirror by typing the following cmdlet:</span></span>
    
        Get-CsDatabaseMirrorState -PoolFqdn <poolFQDN> -DatabaseType User

2.  <span data-ttu-id="17c59-111">Если хранилище Central Management размещено в этом пуле, введите следующий командлет, чтобы определить, какой из них является основным и зеркалом для центрального хранилища.</span><span class="sxs-lookup"><span data-stu-id="17c59-111">If the Central Management store is hosted in this pool, type the following cmdlet to determine which is the principal and which is the mirror for the Central Management store:</span></span>
    
        Get-CsDatabaseMirrorState -PoolFqdn <poolFQDN> -DatabaseType CentralMgmt

3.  <span data-ttu-id="17c59-112">Выполнение отработки отказа базы данных пользователей.</span><span class="sxs-lookup"><span data-stu-id="17c59-112">Perform the failover of the user database:</span></span>
    
      - <span data-ttu-id="17c59-113">Если основной сервер завершился сбоем и вы перейдете на зеркало, введите:</span><span class="sxs-lookup"><span data-stu-id="17c59-113">If the primary has failed and you are failing over to the mirror, type:</span></span>
        
            Invoke-CsDatabaseFailover -PoolFqdn <poolFQDN> -DatabaseType User -NewPrincipal mirror -Verbose
    
      - <span data-ttu-id="17c59-114">Если зеркало завершилось сбоем и вы перейдете на основной, введите:</span><span class="sxs-lookup"><span data-stu-id="17c59-114">If the mirror has failed and you are failing over to the primary, type:</span></span>
        
            Invoke-CsDatabaseFailover -PoolFqdn <poolFQDN> -DatabaseType User -NewPrincipal primary -Verbose

4.  <span data-ttu-id="17c59-115">Если в пуле размещается Центральный сервер управления, выполните отработку отказа центрального хранилища управления.</span><span class="sxs-lookup"><span data-stu-id="17c59-115">If the pool hosts the Central Management Server, perform the failover of the Central Management store.</span></span>
    
      - <span data-ttu-id="17c59-116">Если основной сервер завершился сбоем и вы перейдете на зеркало, введите:</span><span class="sxs-lookup"><span data-stu-id="17c59-116">If the primary has failed and you are failing over to the mirror, type:</span></span>
        
            Invoke-CsDatabaseFailover -PoolFqdn <poolFQDN> -DatabaseType CentralMgmt -NewPrincipal mirror -Verbose
    
      - <span data-ttu-id="17c59-117">Если зеркало завершилось сбоем и вы перейдете на основной, введите:</span><span class="sxs-lookup"><span data-stu-id="17c59-117">If the mirror has failed and you are failing over to the primary, type:</span></span>
        
            Invoke-CsDatabaseFailover -PoolFqdn <poolFQDN> -DatabaseType CentralMgmt -NewPrincipal primary -Verbose

<span data-ttu-id="17c59-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="17c59-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

