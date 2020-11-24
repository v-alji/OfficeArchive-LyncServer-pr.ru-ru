---
title: 'Lync Server 2013: отработка отказа сервером сохраняемого чата'
description: 'Lync Server 2013: сбой на сервере сохраняемого чата.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Failing over Persistent Chat Server
ms:assetid: 2cd79ffd-fee6-44ce-96cf-b98bf25e2690
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204772(v=OCS.15)
ms:contentKeyID: 48183726
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 42a3a8f5df203cc23be39a4a691ad713330eab59
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398473"
---
# <a name="failing-over-persistent-chat-server-in-lync-server-2013"></a><span data-ttu-id="cf2d3-103">Отработка отказа сервером сохраняемого чата в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cf2d3-103">Failing over Persistent Chat Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cf2d3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cf2d3-104">

<span> </span></span></span>

<span data-ttu-id="cf2d3-105">_**Тема последнего изменения:** 2014-02-05_</span><span class="sxs-lookup"><span data-stu-id="cf2d3-105">_**Topic Last Modified:** 2014-02-05_</span></span>

<span data-ttu-id="cf2d3-106">Отработка отказа для сервера сохраняемого чата разработана в основном как процесс вручную.</span><span class="sxs-lookup"><span data-stu-id="cf2d3-106">Failover for Persistent Chat Server is designed to be mainly a manual process.</span></span>

<span data-ttu-id="cf2d3-107">Процедура отработки отказа основывается на предположении, что дополнительный центр обработки данных работает, но службы сервера сохраняемого чата, в которых находится первичная база данных чата, полностью недоступны, в том числе следующие:</span><span class="sxs-lookup"><span data-stu-id="cf2d3-107">The failover procedure is based on the assumption that the secondary data center is up and running, but the Persistent Chat Server services where the primary Persistent Chat database is located are completely unavailable, including the following:</span></span>

  - <span data-ttu-id="cf2d3-108">База данных основного сервера и зеркальный сервер сохраняемого чата.</span><span class="sxs-lookup"><span data-stu-id="cf2d3-108">Persistent Chat Server primary database and Persistent Chat Server mirror database are down.</span></span>

  - <span data-ttu-id="cf2d3-109">Сервер переднего плана Lync Server не работает.</span><span class="sxs-lookup"><span data-stu-id="cf2d3-109">Lync Server Front End Server is down.</span></span>

<span data-ttu-id="cf2d3-110">Вся процедура состоит из двух основных этапов:</span><span class="sxs-lookup"><span data-stu-id="cf2d3-110">The procedure is based on two basic steps:</span></span>

  - <span data-ttu-id="cf2d3-111">Восстановите первичную базу данных сохраняемого чата (MGC).</span><span class="sxs-lookup"><span data-stu-id="cf2d3-111">Recover the primary Persistent Chat database (mgc).</span></span>

  - <span data-ttu-id="cf2d3-112">Реализация зеркального отображения для новой базы данных-источника.</span><span class="sxs-lookup"><span data-stu-id="cf2d3-112">Establish mirroring for the new primary database.</span></span>

<span data-ttu-id="cf2d3-113">Не отменяется переключение на базу данных соответствия требованиям в отношении сохраняемого чата (mgccomp).</span><span class="sxs-lookup"><span data-stu-id="cf2d3-113">The Persistent Chat compliance database (mgccomp) is not failed over.</span></span> <span data-ttu-id="cf2d3-114">Содержимое этой базы данных является временным и очищается по мере обработки данных адаптером соответствия.</span><span class="sxs-lookup"><span data-stu-id="cf2d3-114">The contents of this database are transient and are purged as the compliance adapter processes the data.</span></span> <span data-ttu-id="cf2d3-115">Это ваша ответственность в том, чтобы правильно управлять выводом адаптера, чтобы избежать потери данных.</span><span class="sxs-lookup"><span data-stu-id="cf2d3-115">It is your responsibility, as Persistent Chat Administrator, to correctly manage the adapter output to avoid data loss.</span></span>

<div>

## <a name="to-fail-over-persistent-chat-server"></a><span data-ttu-id="cf2d3-116">Переключение на сохраняемый сервер чата</span><span class="sxs-lookup"><span data-stu-id="cf2d3-116">To fail over Persistent Chat Server</span></span>

1.  <span data-ttu-id="cf2d3-117">Удалите доставку журналов из базы данных для резервного копирования журналов на сервере.</span><span class="sxs-lookup"><span data-stu-id="cf2d3-117">Remove log shipping from the Persistent Chat Server Backup Log Shipping database.</span></span>
    
    1.  <span data-ttu-id="cf2d3-118">С помощью SQL Server Management Studio подключитесь к экземпляру базы данных, в котором находится база данных MGC сервера сохраняемого чата.</span><span class="sxs-lookup"><span data-stu-id="cf2d3-118">Using SQL Server Management Studio, connect to the database instance where the Persistent Chat Server backup mgc database is located.</span></span>
    
    2.  <span data-ttu-id="cf2d3-119">Откройте окно отправки запроса в базу данных master.</span><span class="sxs-lookup"><span data-stu-id="cf2d3-119">Open a query window to the master database.</span></span>
    
    3.  <span data-ttu-id="cf2d3-120">Используйте следующую команду для сброса доставки журналов:</span><span class="sxs-lookup"><span data-stu-id="cf2d3-120">Use the following command to drop log shipping:</span></span>
        
            exec sp_delete_log_shipping_secondary_database mgc

2.  <span data-ttu-id="cf2d3-121">Скопируйте все нескопированные файлы резервных копий из общей папки резервных копий в конечную папку копирования на резервном сервере.</span><span class="sxs-lookup"><span data-stu-id="cf2d3-121">Copy any uncopied backup files from the backup share to the copy destination folder of the backup server.</span></span>

3.  <span data-ttu-id="cf2d3-122">По порядку примените все непримененные резервные копии журналов транзакций к базе данных-получателю.</span><span class="sxs-lookup"><span data-stu-id="cf2d3-122">Apply any unapplied transaction log backups in sequence to the secondary database.</span></span> <span data-ttu-id="cf2d3-123">Подробные сведения можно найти в разделе Инструкции: применение резервной копии журнала транзакций (Transact-SQL) https://go.microsoft.com/fwlink/p/?linkid=247428 .</span><span class="sxs-lookup"><span data-stu-id="cf2d3-123">For details, see "How to: Apply a Transaction Log Backup (Transact-SQL)" at https://go.microsoft.com/fwlink/p/?linkid=247428.</span></span>

4.  <span data-ttu-id="cf2d3-p103">Подключите резервную базу данных mgc к сети. В окне запроса, которое было открыто в действии 1b, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="cf2d3-p103">Bring the backup mgc database online. Using the query window that opens in step 1b, do the following:</span></span>
    
    1.  <span data-ttu-id="cf2d3-126">Завершите все подключения к базе данных mgc при их наличии:</span><span class="sxs-lookup"><span data-stu-id="cf2d3-126">End all connections to the mgc database, if there are any:</span></span>
        
        1.  <span data-ttu-id="cf2d3-127">**exec SP \_ who2** для идентификации подключений к базе данных mgc.</span><span class="sxs-lookup"><span data-stu-id="cf2d3-127">**exec sp\_who2** to identify connections to the mgc database.</span></span>
        
        2.  <span data-ttu-id="cf2d3-128">**Kill \<spid\> (закрыть** ) чтобы завершить эти подключения.</span><span class="sxs-lookup"><span data-stu-id="cf2d3-128">**kill \<spid\>** to end these connections.</span></span>
    
    2.  <span data-ttu-id="cf2d3-129">Подключите базу данных к сети:</span><span class="sxs-lookup"><span data-stu-id="cf2d3-129">Bring the database online:</span></span>
        
        1.  <span data-ttu-id="cf2d3-130">**restore database mgc with recovery**.</span><span class="sxs-lookup"><span data-stu-id="cf2d3-130">**restore database mgc with recovery**.</span></span>

5.  <span data-ttu-id="cf2d3-131">В командной консоли Lync Server используйте команду **Set-CsPersistentChatState-Identity (Service: ATL-CS-001.litwareinc.com "– PoolState FailedOver** для переключения на базу данных MGC резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="cf2d3-131">In Lync Server Management Shell, use the command **Set-CsPersistentChatState -Identity "service:atl-cs-001.litwareinc.com" –PoolState FailedOver** to fail over to the mgc backup database.</span></span> <span data-ttu-id="cf2d3-132">Обязательно замените полное доменное имя в пуле Persistent Chat для узла atl-cs-001.litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="cf2d3-132">Be sure to substitute the fully qualified domain name of your Persistent Chat pool for atl-cs-001.litwareinc.com.</span></span>
    
    <span data-ttu-id="cf2d3-133">Резервная база данных mgc теперь выступает в качестве базы данных-источника.</span><span class="sxs-lookup"><span data-stu-id="cf2d3-133">The mgc backup database now serves as the primary database.</span></span>

6.  <span data-ttu-id="cf2d3-134">В командной консоли Lync Server используйте командлет **Install-CsMirrorDatabase** , чтобы установить зеркало высокой доступности для резервной базы данных, которая теперь является базой данных-источником.</span><span class="sxs-lookup"><span data-stu-id="cf2d3-134">In Lync Server Management Shell, use the **Install-CsMirrorDatabase** cmdlet to establish a high availability mirror for the backup database that now serves as the primary database.</span></span> <span data-ttu-id="cf2d3-135">Используйте экземпляр резервной базы данных в качестве базы данных-источника и экземпляр резервной зеркальной базы данных в качестве экземпляра зеркала.</span><span class="sxs-lookup"><span data-stu-id="cf2d3-135">Use the backup database instance as the primary database and the backup mirror database instance as the mirror instance.</span></span> <span data-ttu-id="cf2d3-136">Это не то же самое зеркало, которое изначально было настроено для базы данных-источника в процессе установки.</span><span class="sxs-lookup"><span data-stu-id="cf2d3-136">This is not the same mirror as the one that was initially configured for the primary database during setup.</span></span> <span data-ttu-id="cf2d3-137">Подробные сведения можно найти в разделе "использование командлетов командной консоли Lync Server" [для развертывания зеркального отображения SQL для сервера высокой доступности в Lync server 2013](lync-server-2013-deploying-sql-mirroring-for-back-end-server-high-availability.md).</span><span class="sxs-lookup"><span data-stu-id="cf2d3-137">For details, see the section "Using Lync Server Management Shell Cmdlets" in [Deploying SQL mirroring for Back End Server high availability in Lync Server 2013](lync-server-2013-deploying-sql-mirroring-for-back-end-server-high-availability.md).</span></span>

7.  <span data-ttu-id="cf2d3-138">Установите для сервера сохраняемые активные серверы чата.</span><span class="sxs-lookup"><span data-stu-id="cf2d3-138">Set the Persistent Chat Server active servers.</span></span> <span data-ttu-id="cf2d3-139">В командной оболочке Lync Server используйте командлет **Set-CsPersistentChatActiveServer** , чтобы настроить список активных серверов.</span><span class="sxs-lookup"><span data-stu-id="cf2d3-139">From the Lync Server Command Shell, use the **Set-CsPersistentChatActiveServer** cmdlet to set the list of active servers.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="cf2d3-140">Все активные серверы должны быть расположены в том же центре обработки данных, что и новая база данных-источник, или подключенном к ней через соединение с низкой задержкой и высокой пропускной способностью.</span><span class="sxs-lookup"><span data-stu-id="cf2d3-140">All the active servers must be located within the same data center as the new primary database, or in a data center that has a low latency/high bandwidth connection to the database.</span></span>

    
    </div>
    
    <span data-ttu-id="cf2d3-141">На этом этапе резервная копия базы данных сервера сохраняемого чата будет успешно выполнена для базы данных архивации сервера сохраняемого чата.</span><span class="sxs-lookup"><span data-stu-id="cf2d3-141">At this point, the failover from the Persistent Chat Server primary database to the Persistent Chat Server backup database completes successfully.</span></span>

<span data-ttu-id="cf2d3-142"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cf2d3-142"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

