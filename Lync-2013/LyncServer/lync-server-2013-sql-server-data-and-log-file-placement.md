---
title: 'Lync Server 2013: размещение данных и файла журнала SQL Server'
description: 'Lync Server 2013: расположение данных и файлов журнала SQL Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: SQL Server data and log file placement
ms:assetid: 67aa525b-8aa3-474f-827e-8e1d4697f30f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398479(v=OCS.15)
ms:contentKeyID: 48184395
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a127254fec41a734136df9b63fc6cc8929745df7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444597"
---
# <a name="sql-server-data-and-log-file-placement-for-lync-server-2013"></a><span data-ttu-id="ec9d9-103">Размещение данных и файла журнала SQL Server для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ec9d9-103">SQL Server data and log file placement for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ec9d9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ec9d9-104">

<span> </span></span></span>

<span data-ttu-id="ec9d9-105">_**Тема последнего изменения:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="ec9d9-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="ec9d9-106">При планировании и развертывании Microsoft SQL Server 2012 или Microsoft SQL Server 2008 R2 SP1 для пула Lync Server 2013, важно помнить, что при работе с данными и файлами журнала на физических жестких дисках будет размещаться файл данных и журнал.</span><span class="sxs-lookup"><span data-stu-id="ec9d9-106">During the planning and deployment of Microsoft SQL Server 2012 or Microsoft SQL Server 2008 R2 SP1 for your Lync Server 2013 Front End pool, an important consideration is the placement of data and log files onto physical hard disks for performance.</span></span> <span data-ttu-id="ec9d9-107">Рекомендуемая конфигурация диска — это реализация 1 + 0 RAID-массива с использованием шести дисков.</span><span class="sxs-lookup"><span data-stu-id="ec9d9-107">The recommended disk configuration is to implement a 1+0 RAID set using 6 spindles.</span></span> <span data-ttu-id="ec9d9-108">Если вы размещаете все файлы баз данных и журналов, которые используются интерфейсным пулом и связанными ролями и службами сервера (то есть сервер архивации и мониторинга, служба группы ответа на Lync Server, служба обслуживания звонков в Lync Server), на диск RAID с помощью мастера развертывания Lync Server вы сможете настроить конфигурацию, которая была протестирована на хорошую производительность.</span><span class="sxs-lookup"><span data-stu-id="ec9d9-108">Placing all database and log files that are used by the Front End pool and associated server roles and services (that is, Archiving and Monitoring Server, Lync Server Response Group service, Lync Server Call Park service) onto the RAID drive set using the Lync Server Deployment Wizard will result in a configuration that has been tested for good performance.</span></span> <span data-ttu-id="ec9d9-109">Файлы базы данных и их ответственные описаны в таблице ниже.</span><span class="sxs-lookup"><span data-stu-id="ec9d9-109">The database files and what they are responsible for is detailed in the following table.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="ec9d9-110">Если ваши политики и конфигурации SQL Server требуют более специализированной установки, файлы базы данных и журнала можно установить в любое предопределенное расположение с помощью командной консоли Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="ec9d9-110">If your policies and SQL Server configurations require a more specialized installation, the database and log files can be installed to any pre-defined location using the Lync Server Management Shell.</span></span> <span data-ttu-id="ec9d9-111">Дополнительные сведения о том, как <A href="lync-server-2013-database-installation-using-lync-server-management-shell.md">установить базу данных с помощью командной консоли Lync Server Management Shell, вы увидите в Lync server 2013</A> .</span><span class="sxs-lookup"><span data-stu-id="ec9d9-111">See <A href="lync-server-2013-database-installation-using-lync-server-management-shell.md">Database installation using Lync Server Management Shell in Lync Server 2013</A> for more details.</span></span>



</div>

### <a name="data-and-log-files-for-central-management-store"></a><span data-ttu-id="ec9d9-112">Файлы данных и журналов для централизованного управления хранилищем</span><span class="sxs-lookup"><span data-stu-id="ec9d9-112">Data and Log Files for Central Management Store</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ec9d9-113">Файлы баз данных централизованного управления хранилищем</span><span class="sxs-lookup"><span data-stu-id="ec9d9-113">Central Management store database files</span></span></th>
<th><span data-ttu-id="ec9d9-114">Файл данных или назначение журнала</span><span class="sxs-lookup"><span data-stu-id="ec9d9-114">Data file or log purpose</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ec9d9-115">XDS. ldf</span><span class="sxs-lookup"><span data-stu-id="ec9d9-115">Xds.ldf</span></span></p></td>
<td><p><span data-ttu-id="ec9d9-116">Файл журнала транзакций для хранилища центрального управления</span><span class="sxs-lookup"><span data-stu-id="ec9d9-116">Transaction log file for the Central Management store</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec9d9-117">XDS. mdf</span><span class="sxs-lookup"><span data-stu-id="ec9d9-117">Xds.mdf</span></span></p></td>
<td><p><span data-ttu-id="ec9d9-118">Сохраняет конфигурацию текущей топологии Lync Server 2013, определенную и опубликованную с помощью построителя топологии.</span><span class="sxs-lookup"><span data-stu-id="ec9d9-118">Maintains the configuration of the current Lync Server 2013 topology, as defined and published by Topology Builder</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec9d9-119">LIS. mdf</span><span class="sxs-lookup"><span data-stu-id="ec9d9-119">Lis.mdf</span></span></p></td>
<td><p><span data-ttu-id="ec9d9-120">Файл данных службы сведений о расположении</span><span class="sxs-lookup"><span data-stu-id="ec9d9-120">Location Information service data file</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec9d9-121">LIS. ldf</span><span class="sxs-lookup"><span data-stu-id="ec9d9-121">Lis.ldf</span></span></p></td>
<td><p><span data-ttu-id="ec9d9-122">Журнал транзакций для файла данных службы сведений о расположении</span><span class="sxs-lookup"><span data-stu-id="ec9d9-122">Transaction log for the Location Information service data file</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="data-and-log-files-for-user-conferencing-and-address-book"></a><span data-ttu-id="ec9d9-123">Файлы данных и журналов для пользователей, конференций и адресной книги</span><span class="sxs-lookup"><span data-stu-id="ec9d9-123">Data and Log files for User, Conferencing, and Address Book</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ec9d9-124">Файлы базы данных основного Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ec9d9-124">Core Lync Server 2013 database files</span></span></th>
<th><span data-ttu-id="ec9d9-125">Файл данных или назначение журнала</span><span class="sxs-lookup"><span data-stu-id="ec9d9-125">Data file or log purpose</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ec9d9-126">RTC. mdf</span><span class="sxs-lookup"><span data-stu-id="ec9d9-126">Rtc.mdf</span></span></p></td>
<td><p><span data-ttu-id="ec9d9-127">Постоянные данные пользователя (например, списки управления доступом (ACL), контакты, запланированные конференции)</span><span class="sxs-lookup"><span data-stu-id="ec9d9-127">Persistent user data (for example, access control lists (ACLs), contacts, scheduled conferences)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec9d9-128">RTC. ldf</span><span class="sxs-lookup"><span data-stu-id="ec9d9-128">Rtc.ldf</span></span></p></td>
<td><p><span data-ttu-id="ec9d9-129">Журнал транзакций для данных RTC</span><span class="sxs-lookup"><span data-stu-id="ec9d9-129">Transaction log for Rtc data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec9d9-130">RTCDyn. mdf</span><span class="sxs-lookup"><span data-stu-id="ec9d9-130">Rtcdyn.mdf</span></span></p></td>
<td><p><span data-ttu-id="ec9d9-131">Поддерживает временные пользовательские данные (данные среды выполнения присутствия)</span><span class="sxs-lookup"><span data-stu-id="ec9d9-131">Maintains transient user data (presence runtime data)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec9d9-132">RTCDyn. ldf</span><span class="sxs-lookup"><span data-stu-id="ec9d9-132">Rtcdyn.ldf</span></span></p></td>
<td><p><span data-ttu-id="ec9d9-133">Журнал транзакций для данных RTCDyn</span><span class="sxs-lookup"><span data-stu-id="ec9d9-133">Transaction log for Rtcdyn data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec9d9-134">Rtcab. mdf</span><span class="sxs-lookup"><span data-stu-id="ec9d9-134">Rtcab.mdf</span></span></p></td>
<td><p><span data-ttu-id="ec9d9-135">База данных адресной книги в реальном времени (RTC) — это репозиторий SQL Server, в котором хранятся сведения о службе адресной книги</span><span class="sxs-lookup"><span data-stu-id="ec9d9-135">Real-time communications (RTC) address book database is the SQL Server repository where Address Book service information is stored</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec9d9-136">Rtcab. ldf</span><span class="sxs-lookup"><span data-stu-id="ec9d9-136">Rtcab.ldf</span></span></p></td>
<td><p><span data-ttu-id="ec9d9-137">Журнал транзакций для службы «адресная книга»</span><span class="sxs-lookup"><span data-stu-id="ec9d9-137">Transaction log for Address Book Service</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec9d9-138">Rtclocal. mdb</span><span class="sxs-lookup"><span data-stu-id="ec9d9-138">Rtclocal.mdb</span></span></p></td>
<td><p><span data-ttu-id="ec9d9-139">Размещение каталога конференций</span><span class="sxs-lookup"><span data-stu-id="ec9d9-139">Hosts the conference directory</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec9d9-140">Rtcxds. mdf</span><span class="sxs-lookup"><span data-stu-id="ec9d9-140">Rtcxds.mdf</span></span></p></td>
<td><p><span data-ttu-id="ec9d9-141">Сохранение резервной копии данных пользователя</span><span class="sxs-lookup"><span data-stu-id="ec9d9-141">Maintains the backup for user data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec9d9-142">Rtcxds. ldf</span><span class="sxs-lookup"><span data-stu-id="ec9d9-142">Rtcxds.ldf</span></span></p></td>
<td><p><span data-ttu-id="ec9d9-143">Журнал транзакций для данных Rtcxds</span><span class="sxs-lookup"><span data-stu-id="ec9d9-143">Transaction log for Rtcxds data</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="data-and-log-files-for-call-park-and-response-group"></a><span data-ttu-id="ec9d9-144">Файлы данных и журналов для парковки звонков и группы ответа</span><span class="sxs-lookup"><span data-stu-id="ec9d9-144">Data and Log Files for Call Park and Response Group</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ec9d9-145">данных приложения</span><span class="sxs-lookup"><span data-stu-id="ec9d9-145">Application database</span></span></th>
<th><span data-ttu-id="ec9d9-146">Файл данных или назначение журнала</span><span class="sxs-lookup"><span data-stu-id="ec9d9-146">Data file or log purpose</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ec9d9-147">Cpsdyn. mdf</span><span class="sxs-lookup"><span data-stu-id="ec9d9-147">Cpsdyn.mdf</span></span></p></td>
<td><p><span data-ttu-id="ec9d9-148">Динамическая информационная база данных для приложения парковки звонков</span><span class="sxs-lookup"><span data-stu-id="ec9d9-148">Dynamic information database for the Call Park application</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec9d9-149">Cpsdyn. ldf</span><span class="sxs-lookup"><span data-stu-id="ec9d9-149">Cpsdyn.ldf</span></span></p></td>
<td><p><span data-ttu-id="ec9d9-150">Журнал транзакций для файла данных приложения с приостановкой звонков</span><span class="sxs-lookup"><span data-stu-id="ec9d9-150">Transaction log for Call Park application data file</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec9d9-151">Rgsconfig. mdf</span><span class="sxs-lookup"><span data-stu-id="ec9d9-151">Rgsconfig.mdf</span></span></p></td>
<td><p><span data-ttu-id="ec9d9-152">Файл данных службы группы ответа Lync Server для настройки служб</span><span class="sxs-lookup"><span data-stu-id="ec9d9-152">Lync Server Response Group service data file for the configuration of the services</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec9d9-153">Rgsconfig. ldf</span><span class="sxs-lookup"><span data-stu-id="ec9d9-153">Rgsconfig.ldf</span></span></p></td>
<td><p><span data-ttu-id="ec9d9-154">Файл журнала транзакций для конфигурации приложения группы ответа</span><span class="sxs-lookup"><span data-stu-id="ec9d9-154">Transaction log file for the Response Group application configuration</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec9d9-155">Rgsdyn. mdf</span><span class="sxs-lookup"><span data-stu-id="ec9d9-155">Rgsdyn.mdf</span></span></p></td>
<td><p><span data-ttu-id="ec9d9-156">Файл данных службы группы ответа для операций среды выполнения</span><span class="sxs-lookup"><span data-stu-id="ec9d9-156">Response Group service data file for runtime operations</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec9d9-157">Rgsdyn. ldf</span><span class="sxs-lookup"><span data-stu-id="ec9d9-157">Rgsdyn.ldf</span></span></p></td>
<td><p><span data-ttu-id="ec9d9-158">Журнал транзакций для файла данных среды выполнения службы группы ответа</span><span class="sxs-lookup"><span data-stu-id="ec9d9-158">Transaction log for the Response Group service runtime data file</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="data-and-log-files-for-archiving-and-monitoring-server"></a><span data-ttu-id="ec9d9-159">Файлы данных и журналов для архивации и мониторинга сервера</span><span class="sxs-lookup"><span data-stu-id="ec9d9-159">Data and Log Files for Archiving and Monitoring Server</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ec9d9-160">Архивирование и мониторинг файлов базы данных</span><span class="sxs-lookup"><span data-stu-id="ec9d9-160">Archiving and Monitoring database files</span></span></th>
<th><span data-ttu-id="ec9d9-161">Файл данных или назначение журнала</span><span class="sxs-lookup"><span data-stu-id="ec9d9-161">Data file or log purpose</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ec9d9-162">LcsCdr. mdf</span><span class="sxs-lookup"><span data-stu-id="ec9d9-162">LcsCdr.mdf</span></span></p></td>
<td><p><span data-ttu-id="ec9d9-163">Хранилище данных для процесса записи сведений о звонке (CDR) на сервере мониторинга</span><span class="sxs-lookup"><span data-stu-id="ec9d9-163">Data store for the call detail recording (CDR) process of the Monitoring Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec9d9-164">LcsCdr. ldf</span><span class="sxs-lookup"><span data-stu-id="ec9d9-164">LcsCdr.ldf</span></span></p></td>
<td><p><span data-ttu-id="ec9d9-165">Журнал транзакций для данных записи сведений о звонке (CDR)</span><span class="sxs-lookup"><span data-stu-id="ec9d9-165">Transaction log for call detail recording (CDR) data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec9d9-166">QoEMetrics. mdf</span><span class="sxs-lookup"><span data-stu-id="ec9d9-166">QoEMetrics.mdf</span></span></p></td>
<td><p><span data-ttu-id="ec9d9-167">Файл данных качества взаимодействия, хранящийся на сервере мониторинга</span><span class="sxs-lookup"><span data-stu-id="ec9d9-167">Quality of Experience data file stored from the Monitoring Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec9d9-168">QoEMetrics. ldf</span><span class="sxs-lookup"><span data-stu-id="ec9d9-168">QoEMetrics.ldf</span></span></p></td>
<td><p><span data-ttu-id="ec9d9-169">Журнал транзакций для наблюдения за данными</span><span class="sxs-lookup"><span data-stu-id="ec9d9-169">Transaction log for Monitoring data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec9d9-170">Lcslog. mdf</span><span class="sxs-lookup"><span data-stu-id="ec9d9-170">Lcslog.mdf</span></span></p></td>
<td><p><span data-ttu-id="ec9d9-171">Файл данных для хранения данных о мгновенных сообщениях и конференц-связи на сервере архивации</span><span class="sxs-lookup"><span data-stu-id="ec9d9-171">Data file for the retention of instant messaging and conferencing data on an Archiving Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec9d9-172">Lcslog. ldf</span><span class="sxs-lookup"><span data-stu-id="ec9d9-172">Lcslog.ldf</span></span></p></td>
<td><p><span data-ttu-id="ec9d9-173">Журнал транзакций для архивации данных</span><span class="sxs-lookup"><span data-stu-id="ec9d9-173">Transaction log for Archiving data</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ec9d9-174">В этом разделе приведены ссылки на диск и на наборы RAID.</span><span class="sxs-lookup"><span data-stu-id="ec9d9-174">In this topic, references are made to disk and to RAID set.</span></span> <span data-ttu-id="ec9d9-175">Обратите внимание, что в конфигурации ресурсов SQL Server обращение к диску означает, что это одно аппаратное устройство.</span><span class="sxs-lookup"><span data-stu-id="ec9d9-175">Note that in the configuration of SQL Server resources, referring to a disk means a single hardware device.</span></span> <span data-ttu-id="ec9d9-176">Жесткий диск с двумя разделами, один из которых хранит файлы журнала и другой раздел, содержащий файлы данных, отличается от двух дисков, каждый из которых предназначен для файлов журнала или данных.</span><span class="sxs-lookup"><span data-stu-id="ec9d9-176">A hard disk drive with two partitions, one holding log files and the other partition holding data files, is not the same as two disks, each dedicated to either log or data files.</span></span>

<span data-ttu-id="ec9d9-177">В ссылках на массивы RAID существуют различные технологии RAID различных производителей.</span><span class="sxs-lookup"><span data-stu-id="ec9d9-177">In reference to RAID sets, there are a number of different RAID technologies from various vendors.</span></span> <span data-ttu-id="ec9d9-178">И с ростом числа сетей хранения данных (SAN) наборы RAID, выделенные для одной системы, rarer.</span><span class="sxs-lookup"><span data-stu-id="ec9d9-178">And, with the proliferation of storage area networks (SAN), RAID sets dedicated to a single system are rarer.</span></span> <span data-ttu-id="ec9d9-179">Вы должны обратиться к поставщику RAID или сети хранения данных, чтобы определить оптимальную конфигурацию для вашего макета диска при настройке производительности SQL Server с помощью Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ec9d9-179">You should consult with your RAID or SAN vendor to determine what the best configuration is for your disk layout when configuring for SQL Server performance with Lync Server 2013.</span></span>

<span data-ttu-id="ec9d9-180">Кроме того, обратите внимание на то, что не все диски создаются одинаково. Некоторые действия выполняются лучше, чем другие.</span><span class="sxs-lookup"><span data-stu-id="ec9d9-180">Note also that not all disk drives are created equally; some perform better than others.</span></span> <span data-ttu-id="ec9d9-181">Даже диски одного и того же производителя могут варьироваться в зависимости от скорости вращения, размера кэша оборудования и других факторов.</span><span class="sxs-lookup"><span data-stu-id="ec9d9-181">Even drives from the same manufacturer can vary in performance because of rotational speed, hardware cache size, and other factors.</span></span>

<span data-ttu-id="ec9d9-182"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ec9d9-182"></div>

<span> </span>

</div>

</div>

</span></span></div>

