---
title: 'Lync Server 2013: тест аварийного восстановления'
description: 'Lync Server 2013: Проверка аварийного восстановления.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Disaster recovery test
ms:assetid: 04f5e747-d837-4350-9fc0-8605dbf025a7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn747887(v=OCS.15)
ms:contentKeyID: 63969571
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fa22abd37f656134c54381d63f29d3160ff85257
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437835"
---
# <a name="disaster-recovery-test-in-lync-server-2013"></a><span data-ttu-id="1f6df-103">Тест аварийного восстановления в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1f6df-103">Disaster recovery test in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1f6df-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1f6df-104">

<span> </span></span></span>

<span data-ttu-id="1f6df-105">_**Тема последнего изменения:** 2015-01-26_</span><span class="sxs-lookup"><span data-stu-id="1f6df-105">_**Topic Last Modified:** 2015-01-26_</span></span>

<span data-ttu-id="1f6df-106">Выполните восстановление системы для сервера Lync Server 2013 пула, чтобы протестировать задокументированный процесс аварийного восстановления.</span><span class="sxs-lookup"><span data-stu-id="1f6df-106">Perform a system recovery for a Lync Server 2013 pool server to test your documented disaster recovery process.</span></span> <span data-ttu-id="1f6df-107">Данный тест смоделирует полный сбой в работе оборудования для одного сервера, а также поможет гарантировать, что ресурсы, планы и данные будут доступны для восстановления.</span><span class="sxs-lookup"><span data-stu-id="1f6df-107">This test will simulate a complete hardware failure for one server, and will help guarantee that the resources, plans, and data is available for recovery.</span></span> <span data-ttu-id="1f6df-108">Попробуйте менять ориентир теста каждый месяц, чтобы в организации каждый раз проверялись сбои в работе разных серверов или других компонентов оборудования.</span><span class="sxs-lookup"><span data-stu-id="1f6df-108">Try to rotate the focus of the test each month so that your organization tests the failure of a different server or other piece of equipment every time.</span></span>

<span data-ttu-id="1f6df-p102">Обратите внимание, что расписание выполнения организациями проверки аварийного восстановления будет отличаться. Очень важно, чтобы проверка аварийного восстановления выполнялась.</span><span class="sxs-lookup"><span data-stu-id="1f6df-p102">Note that the schedule by which organizations perform Disaster Recovery testing will vary. It is very important that disaster recovery testing is not ignored or neglected.</span></span>

<div>


<span data-ttu-id="1f6df-111">Экспортируйте топологию, политики и параметры конфигурации Lync Server 2013 в файл.</span><span class="sxs-lookup"><span data-stu-id="1f6df-111">Export your Lync Server 2013 topology, policies, and configuration settings to a file.</span></span> <span data-ttu-id="1f6df-112">Помимо прочего, данный файл может быть использован для восстановления данной информации в центральном хранилище управления после обновления, сбоя в работе оборудования или некоторых других неполадок, в результате которых произошла потеря данных.</span><span class="sxs-lookup"><span data-stu-id="1f6df-112">Among other things, this file can then be used to restore this information to the Central Management store after an upgrade, a hardware failure, or some other issue has resulted in data loss.</span></span>

<span data-ttu-id="1f6df-113">Импортируйте топологию, политики и параметры конфигурации Lync Server 2013 в хранилище Центрального управления или на локальный компьютер, как показано в следующих командах:</span><span class="sxs-lookup"><span data-stu-id="1f6df-113">Import your Lync Server 2013 topology, policies, and configuration settings to either the Central Management store or to the local computer as shown in the following commands:</span></span>

`Import-CsConfiguration -ByteInput <Byte[]> [-Force <SwitchParameter>] [-LocalStore <SwitchParameter>]`

`Import-CsConfiguration -FileName <String> [-Force <SwitchParameter>] [-LocalStore <SwitchParameter>]`

<span data-ttu-id="1f6df-114">Чтобы выполнить резервное копирование данных рабочего сервера Lync Server 2013, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="1f6df-114">To back up production Lync Server 2013 data:</span></span>

  - <span data-ttu-id="1f6df-115">Создавайте резервные копии баз данных RTC и LCSLog, используя стандартный процесс резервного копирования SQL Server, чтобы выгрузить ее из файла или накопительного дампа.</span><span class="sxs-lookup"><span data-stu-id="1f6df-115">Back up the RTC and LCSLog databases by using the standard SQL Server backup process to dump the database to a file or tape dump device.</span></span>

  - <span data-ttu-id="1f6df-116">Используйте стороннее приложение резервного копирования для создания резервной копии данных в файле или на ленте.</span><span class="sxs-lookup"><span data-stu-id="1f6df-116">Use third-party backup application to back up the data to file or to tape.</span></span>

  - <span data-ttu-id="1f6df-117">Используйте командлет Export-CsUserData для создания экспорта XML всей базы данных RTC полностью.</span><span class="sxs-lookup"><span data-stu-id="1f6df-117">Use the Export-CsUserData cmdlet to create an XML export of the whole RTC database.</span></span>

  - <span data-ttu-id="1f6df-118">Используйте резервное копирование файловой системы или стороннего производителя для создания резервной копии содержимого собрания и журналов соответствия.</span><span class="sxs-lookup"><span data-stu-id="1f6df-118">Use the file system backup or third-party to back up meeting content and compliance logs.</span></span>

  - <span data-ttu-id="1f6df-119">С помощью средства командной строки Export-CsConfiguration можно создавать резервные копии параметров Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1f6df-119">Use the Export-CsConfiguration command-line tool to back up Lync Server 2013 settings.</span></span>

<span data-ttu-id="1f6df-120">Первый этап процедуры обхода неисправностей содержит принудительное перемещение пользователей из производственного пула в пул аварийного восстановления.</span><span class="sxs-lookup"><span data-stu-id="1f6df-120">The first step in the failover procedure includes a forced move of users from the production pool to the Disaster Recovery pool.</span></span>

<span data-ttu-id="1f6df-121">Данное перемещение будет принудительным, потому что производственный пул не будет доступен для принятия перемещения пользователей.</span><span class="sxs-lookup"><span data-stu-id="1f6df-121">This will be a forced move because the production pool won't be available to accept the user relocation.</span></span>

<span data-ttu-id="1f6df-122">В дополнение к обновлению записи в базе данных сервера реального времени на сервере Lync Server 2013 можно изменить атрибут объекта учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="1f6df-122">The Lync Server 2013 move user process is effectively a change to an attribute on the user account object in addition to a record update on the RTC SQL database.</span></span>

<span data-ttu-id="1f6df-123">Эти данные можно восстановить с помощью двух следующих процессов.</span><span class="sxs-lookup"><span data-stu-id="1f6df-123">This data can be restored through the following two processes:</span></span>

  - <span data-ttu-id="1f6df-124">Базу данных RTC можно восстановить из исходного устройства резервного копирования на рабочем сервере SQL Server с помощью стандартного процесса восстановления SQL Server или с помощью сторонней программы резервного копирования и восстановления.</span><span class="sxs-lookup"><span data-stu-id="1f6df-124">RTC database can be restored from the original backup dump device from the production SQL Server using the standard SQL Server restore process, or using a third-party backup/restore utility.</span></span>

  - <span data-ttu-id="1f6df-125">Контактные данные пользователя можно восстановить с помощью служебной программы DBIMPEXP.exe, используя файл XML, который был создан из экспорта производственного сервера SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1f6df-125">User contact data can be restored with the DBIMPEXP.exe utility using the XML file that was created from the production SQL Server export.</span></span>

<span data-ttu-id="1f6df-126">После восстановления эти данные пользователи могут подключаться к аварийному восстановлению Lync Server 2013 и работать в обычном режиме.</span><span class="sxs-lookup"><span data-stu-id="1f6df-126">After this data is restored, users can effectively connect to the Disaster Recovery Lync Server 2013 pool, and operate as usual.</span></span>

<span data-ttu-id="1f6df-127">Чтобы разрешить пользователям подключаться к службе аварийного восстановления Lync Server 2013, потребуется изменение DNS-записи.</span><span class="sxs-lookup"><span data-stu-id="1f6df-127">To enable users to connect to the Disaster Recovery Lync Server 2013 pool, a DNS record change will be required.</span></span>

<span data-ttu-id="1f6df-128">На рабочем месте рабочего 2013 сервера Lync Server будут ссылаться клиенты, использующие записи автоматической настройки и DNS SRV:</span><span class="sxs-lookup"><span data-stu-id="1f6df-128">The production Lync Server 2013 pool will be referenced by clients using the auto-configuration and DNS SRV records of:</span></span>

  - <span data-ttu-id="1f6df-129">SRV: \_ SIP. \_ TLS.\<domain\></span><span class="sxs-lookup"><span data-stu-id="1f6df-129">SRV: \_sip.\_tls.\<domain\></span></span> <span data-ttu-id="1f6df-130">/CNAME: SIP.\<domain\></span><span class="sxs-lookup"><span data-stu-id="1f6df-130">/CNAME: SIP.\<domain\></span></span>

  - <span data-ttu-id="1f6df-131">CNAME: SIP.\<domain\></span><span class="sxs-lookup"><span data-stu-id="1f6df-131">CNAME: SIP.\<domain\></span></span> <span data-ttu-id="1f6df-132">/cvc-pool-1.\<domain\></span><span class="sxs-lookup"><span data-stu-id="1f6df-132">/cvc-pool-1.\<domain\></span></span>

<span data-ttu-id="1f6df-133">Для облегчения процедуры отработки отказа данная запись CNAME должна быть обновлена с помощью ссылки на DROCSPool FQDN:</span><span class="sxs-lookup"><span data-stu-id="1f6df-133">To facilitate the failover, this CNAME record must be updated to reference the DROCSPool FQDN:</span></span>

  - <span data-ttu-id="1f6df-134">CNAME: SIP.\<domain\></span><span class="sxs-lookup"><span data-stu-id="1f6df-134">CNAME: SIP.\<domain\></span></span> <span data-ttu-id="1f6df-135">/DROCSPool.\<domain\></span><span class="sxs-lookup"><span data-stu-id="1f6df-135">/DROCSPool.\<domain\></span></span>

  - <span data-ttu-id="1f6df-136">Установка.\<domain\></span><span class="sxs-lookup"><span data-stu-id="1f6df-136">Sip.\<domain\></span></span>

  - <span data-ttu-id="1f6df-137">Звука.\<domain\></span><span class="sxs-lookup"><span data-stu-id="1f6df-137">AV.\<domain\></span></span>

  - <span data-ttu-id="1f6df-138">"".\<domain\></span><span class="sxs-lookup"><span data-stu-id="1f6df-138">webconf.\<domain\></span></span>

  - <span data-ttu-id="1f6df-139">OCSServices.\<domain\></span><span class="sxs-lookup"><span data-stu-id="1f6df-139">OCSServices.\<domain\></span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="1f6df-140">Подробное описание процедур администрирования и управления см. в разделе <A href="lync-server-2013-backing-up-and-restoring-lync-server.md">резервное копирование и восстановление сервера Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="1f6df-140">For detailed administration and management procedures, see <A href="lync-server-2013-backing-up-and-restoring-lync-server.md">Backing up and restoring Lync Server 2013</A>.</span></span>



</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="1f6df-141">См. также</span><span class="sxs-lookup"><span data-stu-id="1f6df-141">See Also</span></span>


[<span data-ttu-id="1f6df-142">Планирование высокой доступности и аварийного восстановления в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1f6df-142">Planning for high availability and disaster recovery in Lync Server 2013</span></span>](lync-server-2013-planning-for-high-availability-and-disaster-recovery.md)  
[<span data-ttu-id="1f6df-143">Командлеты резервного копирования и высокой доступности в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1f6df-143">Backup and high availability cmdlets in Lync Server 2013</span></span>](https://docs.microsoft.com/powershell/module/skype/?view=skype-ps)  


[<span data-ttu-id="1f6df-144">Import-CsConfiguration</span><span class="sxs-lookup"><span data-stu-id="1f6df-144">Import-CsConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Import-CsConfiguration)  
[<span data-ttu-id="1f6df-145">Резервное копирование и восстановление Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1f6df-145">Backing up and restoring Lync Server 2013</span></span>](lync-server-2013-backing-up-and-restoring-lync-server.md)  
[<span data-ttu-id="1f6df-146">Управление аварийным восстановлением, высокой доступностью и службой резервного копирования Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1f6df-146">Managing Lync Server 2013 disaster recovery, high availability, and Backup Service</span></span>](lync-server-2013-managing-lync-server-disaster-recovery-high-availability-and-backup-service.md)  
  

<span data-ttu-id="1f6df-147"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1f6df-147"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

