---
title: 'Lync Server 2013: настройка доставки журналов SQL Server для основной базы данных сервера сохраняемого чата'
description: 'Lync Server 2013: Настройка доставки журналов SQL Server для базы данных сервера сохраняемого чата.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up SQL Server Log Shipping for the Persistent Chat Server primary database
ms:assetid: 088ea1c2-d592-4a11-b3b8-f1e2f8beae93
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204653(v=OCS.15)
ms:contentKeyID: 48183337
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 72b7e68bd0cb7b9f544b86a15204d3e832692ec1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399640"
---
# <a name="setting-up-sql-server-log-shipping-in-lync-server-2013-for-the-persistent-chat-server-primary-database"></a><span data-ttu-id="26cda-103">Настройка доставки журналов SQL Server в Lync Server 2013 для основной базы данных сервера сохраняемого чата</span><span class="sxs-lookup"><span data-stu-id="26cda-103">Setting up SQL Server Log Shipping in Lync Server 2013 for the Persistent Chat Server primary database</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="26cda-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="26cda-104">

<span> </span></span></span>

<span data-ttu-id="26cda-105">_**Тема последнего изменения:** 2012-11-12_</span><span class="sxs-lookup"><span data-stu-id="26cda-105">_**Topic Last Modified:** 2012-11-12_</span></span>

<span data-ttu-id="26cda-106">Используя SQL Server Management Studio, подключитесь к дополнительному экземпляру базы данных доставки журналов сервера чатов и убедитесь, что агент SQL Server запущен.</span><span class="sxs-lookup"><span data-stu-id="26cda-106">Using SQL Server Management Studio, connect to the Persistent Chat Server secondary Log Shipping database instance, and be sure that SQL Server Agent is running.</span></span>

<span data-ttu-id="26cda-107">С помощью SQL Server Management Studio, подключенного к экземпляру базы данных сохраняемого чата, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="26cda-107">Using SQL Server Management Studio connected to the Persistent Chat primary database instance, perform the following steps:</span></span>

1.  <span data-ttu-id="26cda-108">Убедитесь, что агент SQL Server запущен.</span><span class="sxs-lookup"><span data-stu-id="26cda-108">Be sure that the SQL Server Agent is running.</span></span>

2.  <span data-ttu-id="26cda-109">Щелкните базу данных mgc правой кнопкой мыши и выберите **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="26cda-109">Right-click the mgc database, and then click **Properties**.</span></span>

3.  <span data-ttu-id="26cda-110">В области **Выбор страницы** выберите **Доставка журналов транзакций**.</span><span class="sxs-lookup"><span data-stu-id="26cda-110">Under **Select a page**, click **Transaction Log Shipping**.</span></span>

4.  <span data-ttu-id="26cda-111">Установите флажок **Включить эту базу данных в качестве источника в конфигурацию доставки журналов**.</span><span class="sxs-lookup"><span data-stu-id="26cda-111">Select the **Enable this as a primary database in a log shipping configuration** check box.</span></span>

5.  <span data-ttu-id="26cda-112">В области **Резервные копии журналов транзакций** щелкните элемент **Параметры копирования**.</span><span class="sxs-lookup"><span data-stu-id="26cda-112">Under **Transaction log backups**, click **Backup Settings**.</span></span>

6.  <span data-ttu-id="26cda-113">В поле **Сетевой путь к каталогу резервной копии** введите сетевой путь к общей папке, созданной для резервных копий журналов транзакций.</span><span class="sxs-lookup"><span data-stu-id="26cda-113">In the **Network path to the backup folder** box, type the network path to the share that you created for the transaction log backup folder.</span></span>

7.  <span data-ttu-id="26cda-114">Если папка резервная копия находится на сервере-источнике, введите локальный путь к папке резервного копирования в папке резервная копия **на сервере-источнике, а затем введите локальный путь к папке (например: c: \\ Backup)** .</span><span class="sxs-lookup"><span data-stu-id="26cda-114">If the backup folder is located on the primary server, type the local path to the backup folder in the **If the backup folder is located on the primary server, type a local path to the folder (example: c:\\backup)** box.</span></span> <span data-ttu-id="26cda-115">(Если резервная папка находится не на основном сервере, вы можете оставить это поле пустым.)</span><span class="sxs-lookup"><span data-stu-id="26cda-115">(If the backup folder is not on the primary server, you can leave this box empty.)</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="26cda-116">Если учетная запись службы SQL Server на сервере-источнике работает под учетной записью локальной системы, необходимо создать ее на сервере-источнике и указать локальный путь к этой папке.</span><span class="sxs-lookup"><span data-stu-id="26cda-116">If the SQL Server service account on your primary server runs under the local system account, you must create your backup folder on the primary server and specify a local path to that folder.</span></span>

    
    </div>

8.  <span data-ttu-id="26cda-117">Настройте параметры **Удалить файлы, созданные ранее** и **Предупредить, если резервное копирование не произошло в течение**.</span><span class="sxs-lookup"><span data-stu-id="26cda-117">Configure the **Delete files older than** and **Alert if no backup occurs within** parameters.</span></span>

9.  <span data-ttu-id="26cda-118">Просмотрите расписание резервного копирования, приведенное в поле **Расписание** в разделе **Задание резервного копирования**.</span><span class="sxs-lookup"><span data-stu-id="26cda-118">Look at the backup schedule listed in the **Schedule** box under **Backup job**.</span></span> <span data-ttu-id="26cda-119">Чтобы настроить расписание установки, нажмите кнопку **Расписание** и настройте расписание агента SQL Server в соответствии с требованиями.</span><span class="sxs-lookup"><span data-stu-id="26cda-119">To customize the schedule for your installation, click **Schedule**, and adjust the SQL Server Agent schedule as required.</span></span>

10. <span data-ttu-id="26cda-120">В разделе **Сжатие** выберите флажок **Использовать параметр сервера по умолчанию** и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="26cda-120">Under **Compression**, select **Use the default server setting**, and then click **OK**.</span></span>

11. <span data-ttu-id="26cda-121">В области **Экземпляры сервера-получателя и базы данных** нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="26cda-121">Under **Secondary server instances and databases**, click **Add**.</span></span>

12. <span data-ttu-id="26cda-122">Нажмите кнопку **подключить** и подключитесь к экземпляру SQL Server, который вы настроили как дополнительный сервер.</span><span class="sxs-lookup"><span data-stu-id="26cda-122">Click **Connect** and connect to the instance of SQL Server that you have configured as your secondary server.</span></span>

13. <span data-ttu-id="26cda-123">В поле **База данных-получатель** выберите в списке базу данных **mgc**.</span><span class="sxs-lookup"><span data-stu-id="26cda-123">In the **Secondary Database** box, select the **mgc** database from the list.</span></span>

14. <span data-ttu-id="26cda-124">На вкладке **Инициализация базы данных-получателя** выберите вариант **Да**, создайте полную резервную копию базы данных-источника и выполните восстановление из нее в базу данных-получатель (и создайте базу данных-получатель, если она не существует).</span><span class="sxs-lookup"><span data-stu-id="26cda-124">On the **Initialize Secondary database** tab, choose the option **Yes, generate a full backup of the primary database and restore it into the secondary database (and create the secondary database if it doesn't exist)**.</span></span>

15. <span data-ttu-id="26cda-p103">На вкладке **Копирование файлов** в поле **Папка назначения для копирования файлов** введите путь к папке, в которую необходимо копировать резервные копии журналов транзакций. Эта папка часто находится на дополнительном сервере.</span><span class="sxs-lookup"><span data-stu-id="26cda-p103">On the **Copy Files** tab, in the **Destination folder for copied files** box, type the path of the folder into which the transaction logs backups should be copied. This folder is often located on the secondary server.</span></span>

16. <span data-ttu-id="26cda-127">Обратите внимание на расписание копирования, приведенное в поле **Расписание** в разделе **Задание копирования**.</span><span class="sxs-lookup"><span data-stu-id="26cda-127">Note the copy schedule listed in the **Schedule** box under **Copy job**.</span></span> <span data-ttu-id="26cda-128">Чтобы настроить расписание установки, нажмите кнопку **Расписание** и настройте расписание агента SQL Server в соответствии с требованиями.</span><span class="sxs-lookup"><span data-stu-id="26cda-128">To customize the schedule for your installation, click **Schedule**, and adjust the SQL Server Agent schedule as required.</span></span> <span data-ttu-id="26cda-129">Это расписание должно приблизительно совпадать с расписанием резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="26cda-129">This schedule should be approximately the same as the backup schedule.</span></span>

17. <span data-ttu-id="26cda-130">На вкладке **Восстановление** в разделе **Папка назначения для копирования файлов** выберите вариант **Режим без восстановления**.</span><span class="sxs-lookup"><span data-stu-id="26cda-130">On the **Restore** tab, under **Database state when restoring backups**, choose the **No recovery mode** option.</span></span>

18. <span data-ttu-id="26cda-131">В списке **Отложить восстановление резервных копий по крайней мере на** выберите значение **0 минут**.</span><span class="sxs-lookup"><span data-stu-id="26cda-131">Under **Delay restoring backups at least:**, select **0 minutes**.</span></span>

19. <span data-ttu-id="26cda-132">В поле **Предупреждение, если восстановление не выполнено в течение** выберите порог оповещений.</span><span class="sxs-lookup"><span data-stu-id="26cda-132">Choose an alert threshold under **Alert if no restore occurs within**.</span></span>

20. <span data-ttu-id="26cda-133">Просмотрите расписание восстановления в поле **Расписание** в разделе **Задание восстановления**.</span><span class="sxs-lookup"><span data-stu-id="26cda-133">Look at the restore schedule listed in the **Schedule** box under **Restore job**.</span></span> <span data-ttu-id="26cda-134">Чтобы настроить расписание установки, нажмите кнопку **Расписание**, настройте расписание агента SQL Server и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="26cda-134">To customize the schedule for your installation, click **Schedule**, adjust the SQL Server Agent schedule as required, and click **OK**.</span></span> <span data-ttu-id="26cda-135">Это расписание должно приблизительно совпадать с расписанием резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="26cda-135">This schedule should be approximately the same as the backup schedule.</span></span>

21. <span data-ttu-id="26cda-136">В диалоговом окне **Свойства базы данных** нажмите кнопку **ОК**, чтобы приступить к настройке.</span><span class="sxs-lookup"><span data-stu-id="26cda-136">On the **Database Properties** dialog box, click **OK** to begin the configuration process.</span></span>

<span data-ttu-id="26cda-137"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="26cda-137"></div>

<span> </span>

</div>

</div>

</span></span></div>

