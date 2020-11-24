---
title: 'Lync Server 2013: публикация топологии'
description: 'Lync Server 2013: публикация топологии.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Publish the topology
ms:assetid: 3b5a744b-b3a8-4538-a55e-e2e4f72dff47
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425880(v=OCS.15)
ms:contentKeyID: 48183866
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 453fe186a02c88a5dcd7308096b661058fc04aa6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399052"
---
# <a name="publish-the-topology-in-lync-server-2013"></a><span data-ttu-id="6835d-103">Публикация топологии в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6835d-103">Publish the topology in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6835d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6835d-104">

<span> </span></span></span>

<span data-ttu-id="6835d-105">_**Тема последнего изменения:** 2013-10-01_</span><span class="sxs-lookup"><span data-stu-id="6835d-105">_**Topic Last Modified:** 2013-10-01_</span></span>

<span data-ttu-id="6835d-106">Чтобы успешно публиковать, включать и отключать топологию при добавлении или удалении роли сервера, вы должны войти в систему как пользователь, который является членом группы администраторов RTCUniversalServerAdmins и domain.</span><span class="sxs-lookup"><span data-stu-id="6835d-106">To successfully publish, enable, or disable a topology when adding or removing a server role, you should be logged in as a user who is a member of the RTCUniversalServerAdmins and Domain Admins groups.</span></span> <span data-ttu-id="6835d-107">Кроме того, можно делегировать права и разрешения администраторам.</span><span class="sxs-lookup"><span data-stu-id="6835d-107">It is also possible to delegate the proper administrator rights and permissions.</span></span> <span data-ttu-id="6835d-108">Дополнительные сведения можно найти [в разделе Делегирование разрешений на настройку в Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="6835d-108">For details, see [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span> <span data-ttu-id="6835d-109">Для других изменений конфигурации требуется только членство в группе RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="6835d-109">For other configuration changes, only membership in the RTCUniversalServerAdmins group is required.</span></span>

<span data-ttu-id="6835d-110">Определив топологию в построителе топологии, необходимо опубликовать топологию в хранилище Центрального управления.</span><span class="sxs-lookup"><span data-stu-id="6835d-110">After you define your topology in Topology Builder, you must publish the topology to the Central Management store.</span></span> <span data-ttu-id="6835d-111">Хранилище Central Management предоставляет надежное хранилище schematized данных, необходимое для определения, настройки, обслуживания, администрирования, описания и работы с развертыванием Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6835d-111">The Central Management store provides a robust, schematized storage of the data needed to define, set up, maintain, administer, describe, and operate a Lync Server 2013 deployment.</span></span> <span data-ttu-id="6835d-112">Она также проверяет данные для обеспечения согласованности конфигураций.</span><span class="sxs-lookup"><span data-stu-id="6835d-112">It also validates the data to help ensure configuration consistency.</span></span> <span data-ttu-id="6835d-113">Все изменения данных конфигурации вносятся через центральное хранилище управления, что избавляет от проблем рассинхронизации.</span><span class="sxs-lookup"><span data-stu-id="6835d-113">All changes to this configuration data happen at the Central Management store, eliminating “out-of-sync” issues.</span></span> <span data-ttu-id="6835d-114">Копии данных, предназначенные только для чтения, реплицируются на все серверы в топологии, в том числе на пограничные серверы.</span><span class="sxs-lookup"><span data-stu-id="6835d-114">Read-only copies of the data are replicated to all servers in the topology, including Edge Servers.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="6835d-115">Для успешной публикации начальной топологии и создания центрального сервера управления серверу SQL Server требуется не менее 20 ГБ свободного места на диске.</span><span class="sxs-lookup"><span data-stu-id="6835d-115">SQL Server needs a minimum of 20 GB of free disk space to successfully publish the initial topology and create the Central Management Server.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="6835d-116">Только для корпоративных выпусков: чтобы опубликовать топологию, сервер SQL Server с интерфейсом должен находиться в сети и иметь доступ к исключениям брандмауэра на месте.</span><span class="sxs-lookup"><span data-stu-id="6835d-116">For Enterprise Edition only: In order to publish the topology, the SQL Server-based Back End Server must be online and accessible with firewall exceptions in place.</span></span> <span data-ttu-id="6835d-117">Подробнее об указании исключений межсетевого экрана можно узнать <A href="lync-server-2013-understanding-firewall-requirements-for-sql-server.md">в разделе сведения о требованиях к межсетевому экрану SQL Server с помощью Lync server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="6835d-117">For details about specifying firewall exceptions, see <A href="lync-server-2013-understanding-firewall-requirements-for-sql-server.md">Understanding firewall requirements for SQL Server with Lync Server 2013</A>.</span></span> <span data-ttu-id="6835d-118">Дополнительные сведения о настройке SQL Server можно найти в разделе <A href="lync-server-2013-configure-sql-server-for-lync-server.md">Настройка SQL Server для Lync server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="6835d-118">For details about configuring SQL Server, see <A href="lync-server-2013-configure-sql-server-for-lync-server.md">Configure SQL Server for Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="to-publish-a-topology"></a><span data-ttu-id="6835d-119">Публикация топологии</span><span class="sxs-lookup"><span data-stu-id="6835d-119">To publish a topology</span></span>

1.  <span data-ttu-id="6835d-120">Запустить построитель топологии: нажмите кнопку **Пуск**, выберите пункт **все программы**, а затем — **Microsoft Lync Server 2013** и нажмите кнопку **Построитель топологии Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="6835d-120">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>

2.  <span data-ttu-id="6835d-121">Выберите этот пункт, чтобы открыть топологию из локального файла.</span><span class="sxs-lookup"><span data-stu-id="6835d-121">Select to open the topology from a local file.</span></span> <span data-ttu-id="6835d-122">Если вы используете компьютер, на котором вы определили топологию, это значение будет находиться в том месте, где вы его сохранили.</span><span class="sxs-lookup"><span data-stu-id="6835d-122">If you are on the computer where you defined the topology, this will be in the location where you saved it in earlier steps.</span></span> <span data-ttu-id="6835d-123">Обычно это будет папка "документы" пользователя, который настроил топологию.</span><span class="sxs-lookup"><span data-stu-id="6835d-123">Typically, this will be the Documents folder of the user who configured the topology.</span></span>

3.  <span data-ttu-id="6835d-124">Щелкните правой кнопкой мыши узел **Lync Server 2013** и выберите команду **топология публикации**.</span><span class="sxs-lookup"><span data-stu-id="6835d-124">Right-click the **Lync Server 2013** node, and then click **Publish Topology**.</span></span>

4.  <span data-ttu-id="6835d-125">На странице **Публикация топологии** нажмите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="6835d-125">On the **Publish the topology** page, click **Next**.</span></span>

5.  <span data-ttu-id="6835d-126">На странице **Создание баз данных** выберите базы данных, которые вы хотите опубликовать.</span><span class="sxs-lookup"><span data-stu-id="6835d-126">On the **Create databases** page, select the databases you want to publish.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="6835d-127">Если у вас нет действительных прав на создание определенных баз данных, вы можете снять флажки рядом с этими базами данных, чтобы позже их мог создать другой пользователь с необходимыми правами.</span><span class="sxs-lookup"><span data-stu-id="6835d-127">If you don’t have the appropriate rights to create the databases, you can clear the check boxes next to those databases, and someone with appropriate rights can later create the databases.</span></span> <span data-ttu-id="6835d-128">Дополнительные сведения можно найти <A href="lync-server-2013-deployment-permissions-for-sql-server.md">в разделе разрешения на развертывание SQL Server в Lync server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="6835d-128">For details, see <A href="lync-server-2013-deployment-permissions-for-sql-server.md">Deployment permissions for SQL Server in Lync Server 2013</A>.</span></span>

    
    </div>

6.  <span data-ttu-id="6835d-129">Можно также щелкнуть элемент **Дополнительно**.</span><span class="sxs-lookup"><span data-stu-id="6835d-129">Optionally click **Advanced**.</span></span> <span data-ttu-id="6835d-130">Дополнительные параметры размещения файлов данных SQL Server позволяют выбрать один из указанных ниже вариантов.</span><span class="sxs-lookup"><span data-stu-id="6835d-130">The Advanced SQL Server data file placement options let you select between the following options:</span></span>
    
      - <span data-ttu-id="6835d-131">**Автоматически определять расположение файла базы данных** — этот параметр определяет оптимальную производительность на основе конфигурации диска на сервере SQL Server путем распространения файлов журнала и данных в оптимальное расположение.</span><span class="sxs-lookup"><span data-stu-id="6835d-131">**Automatically determine database file location** – This option will determine the best operational performance based on the disk configuration on your SQL Server-based server by distributing the log and data files to the best location.</span></span>
    
      - <span data-ttu-id="6835d-p107">**Использовать параметры по умолчанию экземпляра SQL Server** — этот параметр помещает файлы данных и журналов на сервер SQL Server, используя настройки экземпляра. Этот параметр не использует рабочие функциональные возможности сервера SQL Server, чтобы определить оптимальные расположения для журналов и данных. Обычно администратор SQL Server перемещает файлы данных и журналов в расположения, удобные для сервера SQL Server и процедур управления организацией.</span><span class="sxs-lookup"><span data-stu-id="6835d-p107">**Use SQL Server instance defaults** – This option puts log and data files onto the SQL Server-based server by using the instance settings. This option does not use the operational functionality of the SQL Server-based server to determine optimal locations for logs and data. The SQL Server administrator would typically move the log and data files to locations that are appropriate for the SQL Server-based server and organization management procedures.</span></span>
    
    <span data-ttu-id="6835d-135">Нажмите кнопку **ОК**, а затем кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="6835d-135">Click **OK**, and then click **Next**.</span></span>

7.  <span data-ttu-id="6835d-136">На странице **Выбор сервера центрального управления** выберите пул переднего плана.</span><span class="sxs-lookup"><span data-stu-id="6835d-136">On the **Select Central Management Server** page, select a Front End pool.</span></span>

8.  <span data-ttu-id="6835d-137">Можно также щелкнуть элемент **Дополнительно**.</span><span class="sxs-lookup"><span data-stu-id="6835d-137">Optionally click **Advanced**.</span></span> <span data-ttu-id="6835d-138">Дополнительные параметры размещения файлов данных SQL Server позволяют выбрать один из указанных ниже вариантов.</span><span class="sxs-lookup"><span data-stu-id="6835d-138">The Advanced SQL Server data file placement options enables you to select between the following options:</span></span>
    
      - <span data-ttu-id="6835d-139">**Автоматически определять расположение файла базы данных** — этот параметр определяет оптимальную производительность на основе конфигурации диска на сервере SQL Server путем распространения файлов журнала и данных в оптимальное расположение.</span><span class="sxs-lookup"><span data-stu-id="6835d-139">**Automatically determine database file location** – This option will determine the best operational performance based on the disk configuration on your SQL Server-based server by distributing the log and data files to the best location.</span></span>
    
      - <span data-ttu-id="6835d-p109">**Использовать параметры по умолчанию экземпляра SQL Server** — этот параметр помещает файлы данных и журналов на сервер SQL Server, используя настройки экземпляра. Этот параметр не использует рабочие функциональные возможности сервера SQL Server, чтобы определить оптимальные расположения для журналов и данных. Обычно администратор SQL Server перемещает файлы данных и журналов в расположения, удобные для сервера SQL Server и процедур управления организацией.</span><span class="sxs-lookup"><span data-stu-id="6835d-p109">**Use SQL Server instance defaults** – This option puts log and data files onto the SQL Server-based server by using the instance settings. This option does not use the operational functionality of the SQL Server-based server to determine optimal locations for logs and data. The SQL Server administrator would typically move the log and data files to locations that are appropriate for the SQL Server-based server and organization management procedures.</span></span>
    
    <span data-ttu-id="6835d-143">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="6835d-143">Click **OK**.</span></span>

9.  <span data-ttu-id="6835d-144">Нажмите кнопку **Далее** для завершения процесса публикации.</span><span class="sxs-lookup"><span data-stu-id="6835d-144">Click **Next** to complete the publishing process.</span></span>

10. <span data-ttu-id="6835d-145">После завершения процесса публикации нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="6835d-145">When the publish process has completed, click **Finish**.</span></span>
    
    <span data-ttu-id="6835d-146">После того как топология успешно опубликована, вы можете приступить к установке локальной реплики центрального хранилища управления на каждом сервере, работающем под управлением Lync Server 2013 в вашей топологии.</span><span class="sxs-lookup"><span data-stu-id="6835d-146">When the topology has been published successfully, you can begin installing a local replica of the Central Management store on each server running Lync Server 2013 in your topology.</span></span> <span data-ttu-id="6835d-147">Мы рекомендуем вас начать с первого интерфейсного пула.</span><span class="sxs-lookup"><span data-stu-id="6835d-147">We recommend that you begin with the first Front End pool.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="6835d-148">См. также</span><span class="sxs-lookup"><span data-stu-id="6835d-148">See Also</span></span>


[<span data-ttu-id="6835d-149">Настройка серверов и пулов переднего плана для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6835d-149">Setting up Front End Servers and Front End pools for Lync Server 2013</span></span>](lync-server-2013-setting-up-front-end-servers-and-front-end-pools.md)  
  

<span data-ttu-id="6835d-150"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6835d-150"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

