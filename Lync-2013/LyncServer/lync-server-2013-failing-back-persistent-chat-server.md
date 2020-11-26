---
title: 'Lync Server 2013: восстановление сервера сохраняемого чата после сбоя'
description: 'Lync Server 2013: не удается вернуть сервер сохраняемого чата.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Failing back Persistent Chat Server
ms:assetid: 67b91de4-6ddc-43e6-9812-5e1aa84a7980
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204970(v=OCS.15)
ms:contentKeyID: 48184396
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2fa36562b3892c0e22960677ffcba4b862e708c4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428309"
---
# <a name="failing-back-persistent-chat-server-in-lync-server-2013"></a><span data-ttu-id="5a6f3-103">Восстановление сервера сохраняемого чата после сбоя в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5a6f3-103">Failing back Persistent Chat Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5a6f3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5a6f3-104">

<span> </span></span></span>

<span data-ttu-id="5a6f3-105">_**Тема последнего изменения:** 2014-02-05_</span><span class="sxs-lookup"><span data-stu-id="5a6f3-105">_**Topic Last Modified:** 2014-02-05_</span></span>

<span data-ttu-id="5a6f3-106">В этой процедуре описаны действия, которые необходимо выполнить для восстановления после отказа сервера с постоянным чат, и для повторного выполнения операций из основного центра обработки данных.</span><span class="sxs-lookup"><span data-stu-id="5a6f3-106">This procedure outlines the steps necessary to recover from a Persistent Chat Server failure, and to reestablish operations from the primary data center.</span></span>

<span data-ttu-id="5a6f3-107">В случае отказа сервера сохраняемого чата в основном центре обработки данных снижается полный сбой, и основная и зеркальная базы данных становятся недоступными.</span><span class="sxs-lookup"><span data-stu-id="5a6f3-107">During Persistent Chat Server failure, the primary data center suffers complete outage, and the primary and mirror databases become unavailable.</span></span> <span data-ttu-id="5a6f3-108">Основной центр обработки данных переключается на резервный сервер.</span><span class="sxs-lookup"><span data-stu-id="5a6f3-108">The primary data center fails over to the backup server.</span></span>

<span data-ttu-id="5a6f3-109">Ниже описывается процедура возобновления нормальной работы после восстановления базы данных-источника и подключения серверов.</span><span class="sxs-lookup"><span data-stu-id="5a6f3-109">The following procedure restores normal operation after the primary data center is back up, and the servers have been rebuilt.</span></span> <span data-ttu-id="5a6f3-110">В этой процедуре предполагается, что основной центр обработки данных восстановлен из общего отключения и что база данных MGC и база данных mgccomp были перестроены и переустановлены с помощью построителя топологии.</span><span class="sxs-lookup"><span data-stu-id="5a6f3-110">The procedure assumes that the primary data center has been recovered from total outage, and that the mgc database and the mgccomp database have been rebuilt and reinstalled by using Topology Builder.</span></span>

<span data-ttu-id="5a6f3-111">Кроме того, в этой процедуре предполагается, что новые зеркальные и резервные серверы не были развернуты в течение периода перехода на другой ресурс, и что развернут только сервер резервного копирования и зеркальный сервер, который определен в [случае сбоя на постоянном сервере чата в Lync server 2013](lync-server-2013-failing-over-persistent-chat-server.md).</span><span class="sxs-lookup"><span data-stu-id="5a6f3-111">The procedure also assumes that no new mirror and backup servers were deployed during the failover period, and that the only server deployed is the backup server and its mirror server, as defined in [Failing over Persistent Chat Server in Lync Server 2013](lync-server-2013-failing-over-persistent-chat-server.md).</span></span>

<span data-ttu-id="5a6f3-112">Данные инструкции служат для восстановления исходной конфигурации, которая существовала до сбоя, приведшего к переключению с основного на резервный сервер.</span><span class="sxs-lookup"><span data-stu-id="5a6f3-112">These steps are designed to recover configuration as it existed prior to the disaster, resulting in failover from the primary server to the backup server.</span></span>

<div>

## <a name="to-fail-back-persistent-chat-server"></a><span data-ttu-id="5a6f3-113">Чтобы вернуть сервер сохраняемого чата</span><span class="sxs-lookup"><span data-stu-id="5a6f3-113">To fail back Persistent Chat Server</span></span>

1.  <span data-ttu-id="5a6f3-114">Удалите все серверы из списка "активный сервер чата", используя `Set-CsPersistentChatActiveServer` командлет из командной консоли Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="5a6f3-114">Clear all servers from the Persistent Chat Server Active Server list by using the `Set-CsPersistentChatActiveServer` cmdlet from the Lync Server Management Shell.</span></span> <span data-ttu-id="5a6f3-115">Это прекратит выполнение всех постоянных серверов чата при подключении к базе данных MGC и базе данных mgccomp во время восстановления после сбоя.</span><span class="sxs-lookup"><span data-stu-id="5a6f3-115">This stops all Persistent Chat Servers from connecting to the mgc database and the mgccomp database during failback.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="5a6f3-116">Агент SQL Server на дополнительном сервере сервера сохраняемого обратного чата должен выполняться под привилегированной учетной записью.</span><span class="sxs-lookup"><span data-stu-id="5a6f3-116">The SQL Server agent on the secondary Persistent Chat Server Back End Server should be running under a privileged account.</span></span> <span data-ttu-id="5a6f3-117">В частности, эта учетная запись должна иметь следующие разрешения:</span><span class="sxs-lookup"><span data-stu-id="5a6f3-117">Specifically, the account must include:</span></span> 
    > <UL>
    > <LI>
    > <P><span data-ttu-id="5a6f3-118">доступ на чтение к сетевой папке, в которую помещаются резервные копии;</span><span class="sxs-lookup"><span data-stu-id="5a6f3-118">Read access to the network share that backups are being placed in.</span></span></P>
    > <LI>
    > <P><span data-ttu-id="5a6f3-119">доступ на запись к локальному каталогу, в который они копируются.</span><span class="sxs-lookup"><span data-stu-id="5a6f3-119">Write access to the specific local directory that the backups are being copied to.</span></span></P></LI></UL>

    
    </div>

2.  <span data-ttu-id="5a6f3-120">Отключите зеркальное отображение для резервной базы данных mgc.</span><span class="sxs-lookup"><span data-stu-id="5a6f3-120">Disable mirroring on the backup mgc database:</span></span>
    
    1.  <span data-ttu-id="5a6f3-121">С помощью SQL Server Management Studio подключитесь к экземпляру резервной копии mgc.</span><span class="sxs-lookup"><span data-stu-id="5a6f3-121">Using SQL Server Management Studio, connect to the backup mgc instance.</span></span>
    
    2.  <span data-ttu-id="5a6f3-122">Щелкните правой кнопкой мыши базу данных mgc, наведите указатель на пункт **Задачи** и выберите пункт **Зеркальное отображение**.</span><span class="sxs-lookup"><span data-stu-id="5a6f3-122">Right-click the mgc database, point to **Tasks**, and then click **Mirror**.</span></span>
    
    3.  <span data-ttu-id="5a6f3-123">Щелкните **Удалить зеркальное отображение**.</span><span class="sxs-lookup"><span data-stu-id="5a6f3-123">Click **Remove Mirroring**.</span></span>
    
    4.  <span data-ttu-id="5a6f3-124">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5a6f3-124">Click **OK**.</span></span>
    
    5.  <span data-ttu-id="5a6f3-125">Выполните те же действия для базы данных mgccomp.</span><span class="sxs-lookup"><span data-stu-id="5a6f3-125">Perform the same steps with the mgccomp database.</span></span>

3.  <span data-ttu-id="5a6f3-126">Создайте резервную копию базы данных mgc, чтобы ее можно было восстановить в новой основной базе данных.</span><span class="sxs-lookup"><span data-stu-id="5a6f3-126">Back up the mgc database so that it can be restored to the new primary database:</span></span>
    
    1.  <span data-ttu-id="5a6f3-127">С помощью SQL Server Management Studio подключитесь к экземпляру резервной копии mgc.</span><span class="sxs-lookup"><span data-stu-id="5a6f3-127">Using SQL Server Management Studio, connect to the backup mgc instance.</span></span>
    
    2.  <span data-ttu-id="5a6f3-p105">Щелкните правой кнопкой мыши базу данных mgc, наведите указатель на пункт **Задачи** и выберите пункт **Создать резервную копию**. Появится диалоговое окно **Резервное копирование базы данных**.</span><span class="sxs-lookup"><span data-stu-id="5a6f3-p105">Right-click the mgc database, point to **Tasks**, and then click **Back Up**. The **Back Up Database** dialog box appears.</span></span>
    
    3.  <span data-ttu-id="5a6f3-130">В списке **Тип резервной копии** выберите пункт **Полная**.</span><span class="sxs-lookup"><span data-stu-id="5a6f3-130">In **Backup type**, select **Full**.</span></span>
    
    4.  <span data-ttu-id="5a6f3-131">В списке **Компонент резервного копирования** выберите пункт **База данных**.</span><span class="sxs-lookup"><span data-stu-id="5a6f3-131">For **Backup component**, click **Database**.</span></span>
    
    5.  <span data-ttu-id="5a6f3-132">В поле **Имя** оставьте имя резервного набора данных по умолчанию или введите другое имя.</span><span class="sxs-lookup"><span data-stu-id="5a6f3-132">Either accept the default backup set name suggested in **Name**, or enter a different name for the backup set.</span></span>
    
    6.  <span data-ttu-id="5a6f3-133">*\<Optional\>* В поле **Описание** введите описание набора резервных копий.</span><span class="sxs-lookup"><span data-stu-id="5a6f3-133">*\<Optional\>* In **Description**, enter a description of the backup set.</span></span>
    
    7.  <span data-ttu-id="5a6f3-134">Удалите расположение резервной копии по умолчанию из списка назначений.</span><span class="sxs-lookup"><span data-stu-id="5a6f3-134">Remove the default backup location from the destination list.</span></span>
    
    8.  <span data-ttu-id="5a6f3-p106">Добавьте в список файл, указав путь к общей папке, которую вы выбрали для доставки журналов. Этот путь доступен как для основной, так и для резервной баз данных.</span><span class="sxs-lookup"><span data-stu-id="5a6f3-p106">Add a file to the list by using the path to the share location that you established for log shipping. This path is available to the primary database and to the backup database.</span></span>
    
    9.  <span data-ttu-id="5a6f3-137">Нажмите кнопку **ОК**, чтобы закрыть диалоговое окно и начать процесс резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="5a6f3-137">Click **OK** to close the dialog box and begin the backup process.</span></span>

4.  <span data-ttu-id="5a6f3-138">Восстановите основную базу данных с помощью резервной копии, созданной в предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="5a6f3-138">Restore the primary database by using the backup database created in the previous step.</span></span>
    
    1.  <span data-ttu-id="5a6f3-139">С помощью SQL Server Management Studio подключитесь к экземпляру основного mgc.</span><span class="sxs-lookup"><span data-stu-id="5a6f3-139">Using SQL Server Management Studio, connect to the primary mgc instance.</span></span>
    
    2.  <span data-ttu-id="5a6f3-p107">Щелкните правой кнопкой мыши базу данных mgc, наведите указатель на пункт **Задачи**, выберите пункт **Восстановить**, а затем **База данных**. Появится диалоговое окно **Восстановление базы данных**.</span><span class="sxs-lookup"><span data-stu-id="5a6f3-p107">Right-click the mgc database, point to **Tasks**, point to **Restore**, and then click **Database**. The **Restore Database** dialog box appears.</span></span>
    
    3.  <span data-ttu-id="5a6f3-142">Выберите пункт **С устройства**.</span><span class="sxs-lookup"><span data-stu-id="5a6f3-142">Select **From Device**.</span></span>
    
    4.  <span data-ttu-id="5a6f3-p108">Нажмите кнопку "Обзор". Откроется диалоговое окно **Указание резервной копии**. В списке **Резервные носители** выберите пункт **Файл**. Нажмите кнопку **Добавить**, выберите файл резервной копии, созданный в шаге 3, и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5a6f3-p108">Click the browse button, which opens the **Specify Backup** dialog box. In **Backup media**, select **File**. Click **Add**, select the backup file that you created in step 3, and then click **OK**.</span></span>
    
    5.  <span data-ttu-id="5a6f3-146">В таблице **Выберите резервные наборы данных для восстановления** выберите резервную копию.</span><span class="sxs-lookup"><span data-stu-id="5a6f3-146">In **Select the backup sets to restore**, select the backup.</span></span>
    
    6.  <span data-ttu-id="5a6f3-147">В области **Выбор страницы** щелкните **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="5a6f3-147">Click **Options** in the **Select a page** pane.</span></span>
    
    7.  <span data-ttu-id="5a6f3-148">В разделе **Параметры восстановления** выберите пункт **Перезаписать существующую базу данных**.</span><span class="sxs-lookup"><span data-stu-id="5a6f3-148">In **Restore options**, select **Overwrite the existing database**.</span></span>
    
    8.  <span data-ttu-id="5a6f3-149">На панели **Состояние восстановления** выберите пункт **Оставить базу данных готовой к использованию**.</span><span class="sxs-lookup"><span data-stu-id="5a6f3-149">In **Recovery State**, select **Leave the database ready to use**.</span></span>
    
    9.  <span data-ttu-id="5a6f3-150">Нажмите кнопку **ОК**, чтобы начать процесс восстановления.</span><span class="sxs-lookup"><span data-stu-id="5a6f3-150">Click **OK** to begin the restoration process.</span></span>

5.  <span data-ttu-id="5a6f3-151">Настройте доставку журналов SQL Server для базы данных PRIMARY.</span><span class="sxs-lookup"><span data-stu-id="5a6f3-151">Configure SQL Server Log Shipping for the primary database.</span></span> <span data-ttu-id="5a6f3-152">Выполните действия, описанные в разделе [Настройка сервера сохраняемого чата для обеспечения высокой доступности и аварийного восстановления в Lync Server 2013](lync-server-2013-configuring-persistent-chat-server-for-high-availability-and-disaster-recovery.md) , чтобы создать доставку журналов для первичной базы данных mgc.</span><span class="sxs-lookup"><span data-stu-id="5a6f3-152">Follow the procedures in [Configuring Persistent Chat Server for high availability and disaster recovery in Lync Server 2013](lync-server-2013-configuring-persistent-chat-server-for-high-availability-and-disaster-recovery.md) to establish log shipping for the primary mgc database.</span></span>

6.  <span data-ttu-id="5a6f3-153">Установите для сервера сохраняемые активные серверы чата.</span><span class="sxs-lookup"><span data-stu-id="5a6f3-153">Set the Persistent Chat Server active servers.</span></span> <span data-ttu-id="5a6f3-154">В командной консоли Lync Server используйте командлет **Set-CsPersistentChatActiveServer** , чтобы настроить список активных серверов.</span><span class="sxs-lookup"><span data-stu-id="5a6f3-154">From the Lync Server Management Shell, use the **Set-CsPersistentChatActiveServer** cmdlet to set the list of active servers.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="5a6f3-155">Все активные серверы должны быть расположены в том же центре обработки данных, что и новая база данных-источник, или подключенном к ней через соединение с низкой задержкой и высокой пропускной способностью.</span><span class="sxs-lookup"><span data-stu-id="5a6f3-155">All the active servers must be located within the same data center as the new primary database, or in a data center that has a low latency/high bandwidth connection to the database.</span></span>

    
    </div>

<span data-ttu-id="5a6f3-156">Восстановите состояние пула в обычном режиме, выполнив следующую команду Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="5a6f3-156">The restore the pool to its normal state run the following Windows PowerShell command:</span></span>

    Set-CsPersistentChatState -Identity "service: lyncpc.dci.discovery.com" -PoolState Normal

<span data-ttu-id="5a6f3-157">Для получения дополнительных сведений ознакомьтесь с разделом справки для командлета [Set-CsPersistentChatState](https://docs.microsoft.com/powershell/module/skype/Set-CsPersistentChatState) .</span><span class="sxs-lookup"><span data-stu-id="5a6f3-157">See the help topic for the [Set-CsPersistentChatState](https://docs.microsoft.com/powershell/module/skype/Set-CsPersistentChatState) cmdlet for more information.</span></span>

<span data-ttu-id="5a6f3-158"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5a6f3-158"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

