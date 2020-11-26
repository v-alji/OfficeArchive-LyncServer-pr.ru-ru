---
title: 'Lync Server 2013: журналы резервного копирования и восстановления'
description: 'Lync Server 2013: журналы резервного копирования и восстановления.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Backup and restoration worksheets
ms:assetid: 26c78155-0306-41ac-845b-7ad58000a1d6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202169(v=OCS.15)
ms:contentKeyID: 51541460
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1713e291ae7132cc96309fa499bd97bf7f4f5016
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437961"
---
# <a name="backup-and-restoration-worksheets-for-lync-server-2013"></a><span data-ttu-id="ca5f5-103">Журналы резервного копирования и восстановления для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ca5f5-103">Backup and restoration worksheets for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ca5f5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ca5f5-104">

<span> </span></span></span>

<span data-ttu-id="ca5f5-105">_**Тема последнего изменения:** 2013-02-18_</span><span class="sxs-lookup"><span data-stu-id="ca5f5-105">_**Topic Last Modified:** 2013-02-18_</span></span>

<span data-ttu-id="ca5f5-106">План резервного копирования и восстановления для Организации должен содержать сведения о том, как и когда вы захотите создать резервную копию данных и параметров.</span><span class="sxs-lookup"><span data-stu-id="ca5f5-106">The backup and restoration plan for your organization should contain details about how and when you back up data and settings.</span></span> <span data-ttu-id="ca5f5-107">Вы можете использовать представленные здесь листы, которые помогут вам документировать эти сведения о конкретном развертывании, а также о требованиях к резервному копированию и восстановлению в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="ca5f5-107">You can use the worksheets presented here to help you document this information for your specific deployment and for your organization's backup and restoration requirements.</span></span>

<span data-ttu-id="ca5f5-108">С помощью следующих листов вы можете записать сведения, необходимые для резервного копирования и восстановления базы данных, хранилища файлов и параметров для пула Lync Server или стандартного сервера Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="ca5f5-108">Use the following worksheets to record the information that you need to back up and restore database, File Store, and settings information for a Lync Server pool or Standard Edition server.</span></span> <span data-ttu-id="ca5f5-109">Храните одну или несколько копий этих листов в безопасном месте, чтобы они были доступны, если вам нужно восстановить Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ca5f5-109">Keep one or more copies of these worksheets in a secure location so that they are readily accessible if you need to restore Lync Server.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="ca5f5-110">На листах в этом разделе рассматриваются только те данные, которые необходимы для восстановления данных и параметров баз данных и серверов Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ca5f5-110">The worksheets in this section cover only the information that is required to restore the data and settings of Lync Server databases and servers.</span></span> <span data-ttu-id="ca5f5-111">Если вам нужно документировать другие данные для восстановления, например сведения для переустановки операционной системы и другого программного обеспечения, используйте планы развертывания и резервные копии и планы восстановления Организации, чтобы устранить эти требования.</span><span class="sxs-lookup"><span data-stu-id="ca5f5-111">If you need to document other restoration information, such as the information for reinstalling operating systems and other software, use your organization's deployment plans and backup and restoration plans to address those requirements.</span></span>



</div>

<div>

## <a name="database-backup-and-restoration-worksheet"></a><span data-ttu-id="ca5f5-112">Журнал резервного копирования и восстановления базы данных</span><span class="sxs-lookup"><span data-stu-id="ca5f5-112">Database Backup and Restoration Worksheet</span></span>

<span data-ttu-id="ca5f5-113">Ниже приведена таблица, в которой записываются сведения, необходимые для резервного копирования и восстановления баз данных Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ca5f5-113">Use the following table to record the information that you need to back up and restore Lync Server databases.</span></span>

### <a name="database-information-for-backup-and-restoration"></a><span data-ttu-id="ca5f5-114">Сведения о базе данных для резервного копирования и восстановления</span><span class="sxs-lookup"><span data-stu-id="ca5f5-114">Database Information for Backup and Restoration</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ca5f5-115">База</span><span class="sxs-lookup"><span data-stu-id="ca5f5-115">Database</span></span></th>
<th><span data-ttu-id="ca5f5-116">Имя сервера (FQDN)</span><span class="sxs-lookup"><span data-stu-id="ca5f5-116">Server name (FQDN)</span></span></th>
<th><span data-ttu-id="ca5f5-117">Расписание резервного копирования</span><span class="sxs-lookup"><span data-stu-id="ca5f5-117">Backup schedule</span></span></th>
<th><span data-ttu-id="ca5f5-118">Средство резервного копирования базы данных</span><span class="sxs-lookup"><span data-stu-id="ca5f5-118">Database backup tool</span></span></th>
<th><span data-ttu-id="ca5f5-119">Резервный наборы данных</span><span class="sxs-lookup"><span data-stu-id="ca5f5-119">Backup set</span></span></th>
<th><span data-ttu-id="ca5f5-120">Место назначения резервной копии</span><span class="sxs-lookup"><span data-stu-id="ca5f5-120">Backup destination</span></span></th>
<th><span data-ttu-id="ca5f5-121">Notes</span><span class="sxs-lookup"><span data-stu-id="ca5f5-121">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ca5f5-122">База данных RTC на обратном стороне сервера для данных пользователя</span><span class="sxs-lookup"><span data-stu-id="ca5f5-122">Rtc database on Back End Server for user data</span></span></p></td>
<td><p>                    </p></td>
<td><p>                    </p></td>
<td><p><span data-ttu-id="ca5f5-123">Командлет <strong>Export-CsUserData</strong></span><span class="sxs-lookup"><span data-stu-id="ca5f5-123"><strong>Export-CsUserData</strong> cmdlet</span></span></p></td>
<td><p><span data-ttu-id="ca5f5-124">Псевдоним</span><span class="sxs-lookup"><span data-stu-id="ca5f5-124">Name:</span></span></p>
<p><span data-ttu-id="ca5f5-125">Окончания срока действия</span><span class="sxs-lookup"><span data-stu-id="ca5f5-125">Expiration:</span></span></p>
<p>                   </p></td>
<td><p>                    </p></td>
<td><p>                    </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca5f5-126">База данных LcsLog (имя по умолчанию) на сервере архивации базы данных</span><span class="sxs-lookup"><span data-stu-id="ca5f5-126">LcsLog (default name) database on Archiving database server</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ca5f5-127">Средство управления SQL Server</span><span class="sxs-lookup"><span data-stu-id="ca5f5-127">SQL Server management tool</span></span></p></td>
<td><p><span data-ttu-id="ca5f5-128">Псевдоним</span><span class="sxs-lookup"><span data-stu-id="ca5f5-128">Name:</span></span></p>
<p><span data-ttu-id="ca5f5-129">Окончания срока действия</span><span class="sxs-lookup"><span data-stu-id="ca5f5-129">Expiration:</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ca5f5-130">База данных LcsCdr на сервере мониторинга для записей сведений о вызовах (CDRs)</span><span class="sxs-lookup"><span data-stu-id="ca5f5-130">LcsCdr database on Monitoring database server for call detail records (CDRs)</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ca5f5-131">Средство управления SQL Server</span><span class="sxs-lookup"><span data-stu-id="ca5f5-131">SQL Server management tool</span></span></p></td>
<td><p><span data-ttu-id="ca5f5-132">Псевдоним</span><span class="sxs-lookup"><span data-stu-id="ca5f5-132">Name:</span></span></p>
<p><span data-ttu-id="ca5f5-133">Окончания срока действия</span><span class="sxs-lookup"><span data-stu-id="ca5f5-133">Expiration:</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca5f5-134">QoEMetrics Database на сервере базы данных для отслеживания качества взаимодействия (QoE)</span><span class="sxs-lookup"><span data-stu-id="ca5f5-134">QoEMetrics database on Monitoring database server for Quality of Experience (QoE) data</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ca5f5-135">Средство управления SQL Server</span><span class="sxs-lookup"><span data-stu-id="ca5f5-135">SQL Server management tool</span></span></p></td>
<td><p><span data-ttu-id="ca5f5-136">Псевдоним</span><span class="sxs-lookup"><span data-stu-id="ca5f5-136">Name:</span></span></p>
<p><span data-ttu-id="ca5f5-137">Окончания срока действия</span><span class="sxs-lookup"><span data-stu-id="ca5f5-137">Expiration:</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ca5f5-138">База данных сохраняемого чата</span><span class="sxs-lookup"><span data-stu-id="ca5f5-138">Persistent Chat Database</span></span></p></td>
<td></td>
<td></td>
<td><p><span data-ttu-id="ca5f5-139">Средство управления SQL Server или командлет <strong>Export-CsPersistentChatData</strong></span><span class="sxs-lookup"><span data-stu-id="ca5f5-139">SQL Server management tool or <strong>Export-CsPersistentChatData</strong> cmdlet</span></span></p></td>
<td><p><span data-ttu-id="ca5f5-140">Псевдоним</span><span class="sxs-lookup"><span data-stu-id="ca5f5-140">Name:</span></span></p>
<p><span data-ttu-id="ca5f5-141">Окончания срока действия</span><span class="sxs-lookup"><span data-stu-id="ca5f5-141">Expiration:</span></span></p></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ca5f5-142">Для следующих баз данных резервное копирование и восстановление не требуется:</span><span class="sxs-lookup"><span data-stu-id="ca5f5-142">No backup or restoration is required of the following databases:</span></span>

  - <span data-ttu-id="ca5f5-143">Rtcdyn.</span><span class="sxs-lookup"><span data-stu-id="ca5f5-143">Rtcdyn.</span></span> <span data-ttu-id="ca5f5-144">Временные данные пользователя в этой базе данных не требуются для восстановления служб.</span><span class="sxs-lookup"><span data-stu-id="ca5f5-144">The transient user data in this database is not necessary for restoration of service.</span></span>

  - <span data-ttu-id="ca5f5-145">Rtcab.</span><span class="sxs-lookup"><span data-stu-id="ca5f5-145">Rtcab.</span></span> <span data-ttu-id="ca5f5-146">База данных адресной книги автоматически воссоздается в глобальном списке адресов (GAL) доменных служб Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ca5f5-146">The Address Book database is automatically recreated from the Global Address List (GAL) in Active Directory Domain Services.</span></span>

  - <span data-ttu-id="ca5f5-147">Rgsdyn.</span><span class="sxs-lookup"><span data-stu-id="ca5f5-147">Rgsdyn.</span></span> <span data-ttu-id="ca5f5-148">Промежуточные данные службы группы ответа в этой базе данных не требуются для восстановления служб.</span><span class="sxs-lookup"><span data-stu-id="ca5f5-148">The transient Response Group service data in this database is not necessary for restoration of service.</span></span>

  - <span data-ttu-id="ca5f5-149">Cpsdyn.</span><span class="sxs-lookup"><span data-stu-id="ca5f5-149">Cpsdyn.</span></span> <span data-ttu-id="ca5f5-150">Динамическая информация для приложения парковки на приостановке не требуется для восстановления служб.</span><span class="sxs-lookup"><span data-stu-id="ca5f5-150">The dynamic information for the Call Park application is not necessary for restoration of service.</span></span>

  - <span data-ttu-id="ca5f5-151">MgcComp.</span><span class="sxs-lookup"><span data-stu-id="ca5f5-151">MgcComp.</span></span> <span data-ttu-id="ca5f5-152">База данных соответствия требованиям для сохраняемого чата не требуется для восстановления служб.</span><span class="sxs-lookup"><span data-stu-id="ca5f5-152">The compliance database for Persistent Chat is not necessary for restoration of service.</span></span>

</div>

<div>

## <a name="file-store-backup-and-restoration-worksheet"></a><span data-ttu-id="ca5f5-153">Журнал резервного копирования и восстановления хранилища файлов</span><span class="sxs-lookup"><span data-stu-id="ca5f5-153">File Store Backup and Restoration Worksheet</span></span>

<span data-ttu-id="ca5f5-154">Ниже приведена таблица, в которой записываются сведения, необходимые для резервного копирования и восстановления хранилища файлов.</span><span class="sxs-lookup"><span data-stu-id="ca5f5-154">Use the following table to record the information that you need to back up and restore the File Stores.</span></span> <span data-ttu-id="ca5f5-155">В хранилищах файлов содержатся данные, такие как метаданные контента собраний, журналы соответствия собраний, журналы обновлений для устройств и звуковые файлы для групп ответа, приостановки звонков и объявлений.</span><span class="sxs-lookup"><span data-stu-id="ca5f5-155">File Stores contain data such as meeting content metadata, meeting compliance logs, update logs for device updates, and audio files for the Response Group, Call Park, and Announcement applications.</span></span>

### <a name="file-store-information-for-backup-and-restoration"></a><span data-ttu-id="ca5f5-156">Сведения о хранилище файлов для резервного копирования и восстановления</span><span class="sxs-lookup"><span data-stu-id="ca5f5-156">File Store Information for Backup and Restoration</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ca5f5-157">Содержимое</span><span class="sxs-lookup"><span data-stu-id="ca5f5-157">Content</span></span></th>
<th><span data-ttu-id="ca5f5-158">Имя сервера (FQDN)</span><span class="sxs-lookup"><span data-stu-id="ca5f5-158">Server name (FQDN)</span></span></th>
<th><span data-ttu-id="ca5f5-159">Расписание резервного копирования</span><span class="sxs-lookup"><span data-stu-id="ca5f5-159">Backup schedule</span></span></th>
<th><span data-ttu-id="ca5f5-160">Средство архивации файловой системы</span><span class="sxs-lookup"><span data-stu-id="ca5f5-160">File system backup tool</span></span></th>
<th><span data-ttu-id="ca5f5-161">Вы хотите создать резервную копию файла \*?</span><span class="sxs-lookup"><span data-stu-id="ca5f5-161">File share to be backed up \*</span></span></th>
<th><span data-ttu-id="ca5f5-162">Место назначения резервной копии</span><span class="sxs-lookup"><span data-stu-id="ca5f5-162">Backup destination</span></span></th>
<th><span data-ttu-id="ca5f5-163">Notes</span><span class="sxs-lookup"><span data-stu-id="ca5f5-163">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ca5f5-164">Хранилище файлов Lync Server</span><span class="sxs-lookup"><span data-stu-id="ca5f5-164">Lync Server File Store</span></span></p></td>
<td></td>
<td></td>
<td><p><span data-ttu-id="ca5f5-165">Стандартный инструмент резервного копирования, например Robocopy</span><span class="sxs-lookup"><span data-stu-id="ca5f5-165">Standard backup tool, such as Robocopy</span></span></p></td>
<td><p><span data-ttu-id="ca5f5-166">На файловом сервере для Enterprise Edition.</span><span class="sxs-lookup"><span data-stu-id="ca5f5-166">On file server for Enterprise Edition.</span></span> <span data-ttu-id="ca5f5-167">В стандартном выпуске по умолчанию для развертывания в стандартном выпуске.</span><span class="sxs-lookup"><span data-stu-id="ca5f5-167">On Standard Edition by default, for Standard Edition deployment.</span></span> <span data-ttu-id="ca5f5-168">Как правило, по одному на сайт.</span><span class="sxs-lookup"><span data-stu-id="ca5f5-168">Typically, one per site.</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ca5f5-169">Файлы с именем <strong>Meeting. Active</strong> не следует архивировать.</span><span class="sxs-lookup"><span data-stu-id="ca5f5-169">Files named <strong>Meeting.Active</strong> should not be backed up.</span></span> <span data-ttu-id="ca5f5-170">Эти файлы используются и заблокированы во время собрания.</span><span class="sxs-lookup"><span data-stu-id="ca5f5-170">These files are in use and are locked while a meeting takes place.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="settings-backup-and-restoration-worksheet"></a><span data-ttu-id="ca5f5-171">Журнал резервного копирования и восстановления параметров</span><span class="sxs-lookup"><span data-stu-id="ca5f5-171">Settings Backup and Restoration Worksheet</span></span>

<span data-ttu-id="ca5f5-172">Ниже приведена таблица, в которой записываются сведения, необходимые для резервного копирования и восстановления параметров.</span><span class="sxs-lookup"><span data-stu-id="ca5f5-172">Use the following table to record the information that you need to back up and restore settings.</span></span>

### <a name="settings-information-for-backup-and-restoration"></a><span data-ttu-id="ca5f5-173">Сведения о параметрах для резервного копирования и восстановления</span><span class="sxs-lookup"><span data-stu-id="ca5f5-173">Settings Information for Backup and Restoration</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ca5f5-174">База</span><span class="sxs-lookup"><span data-stu-id="ca5f5-174">Database</span></span></th>
<th><span data-ttu-id="ca5f5-175">Имя сервера (FQDN)</span><span class="sxs-lookup"><span data-stu-id="ca5f5-175">Server name (FQDN)</span></span></th>
<th><span data-ttu-id="ca5f5-176">Расписание резервного копирования</span><span class="sxs-lookup"><span data-stu-id="ca5f5-176">Backup schedule</span></span></th>
<th><span data-ttu-id="ca5f5-177">Средство резервного копирования</span><span class="sxs-lookup"><span data-stu-id="ca5f5-177">Backup tool</span></span></th>
<th><span data-ttu-id="ca5f5-178">Имя файла конфигурации (XML)</span><span class="sxs-lookup"><span data-stu-id="ca5f5-178">Configuration file (.xml) name</span></span></th>
<th><span data-ttu-id="ca5f5-179">Расположение резервной копии</span><span class="sxs-lookup"><span data-stu-id="ca5f5-179">Backup location</span></span></th>
<th><span data-ttu-id="ca5f5-180">Notes</span><span class="sxs-lookup"><span data-stu-id="ca5f5-180">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ca5f5-181">База данных XDS в хранилище для централизованного управления конфигурацией топологии (Global)</span><span class="sxs-lookup"><span data-stu-id="ca5f5-181">Xds database in Central Management store for topology configuration (global)</span></span></p></td>
<td><p>                    </p></td>
<td><p>                    </p></td>
<td><p><span data-ttu-id="ca5f5-182">Командлет <strong>Export-CsConfiguration</strong></span><span class="sxs-lookup"><span data-stu-id="ca5f5-182"><strong>Export-CsConfiguration</strong> cmdlet</span></span></p></td>
<td><p>                   </p></td>
<td><p>                    </p></td>
<td><p>                   </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca5f5-183">База данных LIS в хранилище для централизованного управления E9 — 1 – 1 — сведения о расположении (Global)</span><span class="sxs-lookup"><span data-stu-id="ca5f5-183">Lis database in Central Management store for E9-1-1 location information (global)</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ca5f5-184">Командлет <strong>Export-CsLisConfiguration</strong></span><span class="sxs-lookup"><span data-stu-id="ca5f5-184"><strong>Export-CsLisConfiguration</strong> cmdlet</span></span></p></td>
<td></td>
<td><p> </p></td>
<td><p>                    </p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ca5f5-185">Конфигурация группы ответа RgsConfig базы данных сервера на обратном сервере.</span><span class="sxs-lookup"><span data-stu-id="ca5f5-185">RgsConfig database on Back End Server for Response Group configuration (pool)</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ca5f5-186">Командлет <strong>Export-CsRgsConfiguration</strong></span><span class="sxs-lookup"><span data-stu-id="ca5f5-186"><strong>Export-CsRgsConfiguration</strong> cmdlet</span></span></p></td>
<td></td>
<td><p> </p></td>
<td><p>                    </p></td>
</tr>
</tbody>
</table><span data-ttu-id="ca5f5-187">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ca5f5-187">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

