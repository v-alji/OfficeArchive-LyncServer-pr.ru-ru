---
title: 'Lync Server 2013: требования к резервному копированию и восстановлению: инструменты и разрешения'
description: 'Lync Server 2013: требования к резервному копированию и восстановлению: инструменты и разрешения.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: 'Backup and restoration requirements: tools and permissions'
ms:assetid: 35ec2e33-f33e-4f84-9e64-6550fd78aa52
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202171(v=OCS.15)
ms:contentKeyID: 51541465
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 36327d1214854586b44024f126bbd87acad6c4b2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437982"
---
# <a name="backup-and-restoration-requirements-in-lync-server-2013-tools-and-permissions"></a><span data-ttu-id="ee4c5-103">Требования к резервному копированию и восстановлению в Lync Server 2013: инструменты и разрешения</span><span class="sxs-lookup"><span data-stu-id="ee4c5-103">Backup and restoration requirements in Lync Server 2013: tools and permissions</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ee4c5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ee4c5-104">

<span> </span></span></span>

<span data-ttu-id="ee4c5-105">_**Тема последнего изменения:** 2013-02-17_</span><span class="sxs-lookup"><span data-stu-id="ee4c5-105">_**Topic Last Modified:** 2013-02-17_</span></span>

<span data-ttu-id="ee4c5-106">В этой статье описаны средства, с помощью которых можно создавать резервные копии и восстанавливать Lync Server 2013, нужные разрешения, а также можно ли выполнять команды удаленно или локально.</span><span class="sxs-lookup"><span data-stu-id="ee4c5-106">This topic identifies the tools that you can use to back up and restore Lync Server 2013, the permissions that you need, and whether you can run commands remotely or locally.</span></span> <span data-ttu-id="ee4c5-107">В частности, этот раздел посвящен средствам, которые предоставляются в Lync Server для резервного копирования и восстановления.</span><span class="sxs-lookup"><span data-stu-id="ee4c5-107">Specifically, this topic focuses on tools that are provided with Lync Server for backup and restoration.</span></span>

<div>

## <a name="backups"></a><span data-ttu-id="ee4c5-108">Архиваци</span><span class="sxs-lookup"><span data-stu-id="ee4c5-108">Backups</span></span>

<span data-ttu-id="ee4c5-109">Для резервного копирования сервера Lync Server используйте инструменты, описанные в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="ee4c5-109">To back up Lync Server, use the tools identified in the following table.</span></span> <span data-ttu-id="ee4c5-110">Все команды, необходимые для создания резервной копии сервера Lync Server, могут быть внесены в сценарий и могут быть запущены удаленно.</span><span class="sxs-lookup"><span data-stu-id="ee4c5-110">All the commands that you need to back up Lync Server can be scripted and can be run remotely.</span></span>

### <a name="tools-for-backing-up-lync-server"></a><span data-ttu-id="ee4c5-111">Инструменты для резервного копирования сервера Lync Server</span><span class="sxs-lookup"><span data-stu-id="ee4c5-111">Tools for Backing Up Lync Server</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ee4c5-112">Чтобы создать резервную копию, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="ee4c5-112">To back up this:</span></span></th>
<th><span data-ttu-id="ee4c5-113">Используйте это средство или командлет:</span><span class="sxs-lookup"><span data-stu-id="ee4c5-113">Use this tool or cmdlet:</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ee4c5-114">Данные конфигурации топологии (XDS. mdf)</span><span class="sxs-lookup"><span data-stu-id="ee4c5-114">Topology configuration data (Xds.mdf)</span></span></p></td>
<td><p><span data-ttu-id="ee4c5-115">Export-CsConfiguration</span><span class="sxs-lookup"><span data-stu-id="ee4c5-115">Export-CsConfiguration</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee4c5-116">Служба сведений о расположении (E9-1-1) Data (LIS. mdf)</span><span class="sxs-lookup"><span data-stu-id="ee4c5-116">Location information service (E9-1-1) data (Lis.mdf)</span></span></p></td>
<td><p><span data-ttu-id="ee4c5-117">Export-CsLisConfiguration</span><span class="sxs-lookup"><span data-stu-id="ee4c5-117">Export-CsLisConfiguration</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee4c5-118">Данные конфигурации группы ответа (RgsConfig. mdf)</span><span class="sxs-lookup"><span data-stu-id="ee4c5-118">Response Group configuration data (RgsConfig.mdf)</span></span></p></td>
<td><p><span data-ttu-id="ee4c5-119">Export-CsRgsConfiguration</span><span class="sxs-lookup"><span data-stu-id="ee4c5-119">Export-CsRgsConfiguration</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee4c5-120">Постоянные данные пользователя (Rtcxds. mdf)</span><span class="sxs-lookup"><span data-stu-id="ee4c5-120">Persistent user data (Rtcxds.mdf database)</span></span></p>
<p><span data-ttu-id="ee4c5-121">Идентификаторы конференций</span><span class="sxs-lookup"><span data-stu-id="ee4c5-121">Conference IDs</span></span></p></td>
<td><p><span data-ttu-id="ee4c5-122">Export-CsUserData</span><span class="sxs-lookup"><span data-stu-id="ee4c5-122">Export-CsUserData</span></span></p></td>
</tr>
<tr class="odd">
<td><ul>
<li><p><span data-ttu-id="ee4c5-123">Архивирование базы данных (LcsLog. mdf)</span><span class="sxs-lookup"><span data-stu-id="ee4c5-123">Archiving database (LcsLog.mdf)</span></span></p></li>
<li><p><span data-ttu-id="ee4c5-124">Наблюдение за базой данных записи сведений о вызовах (LcsCDR. mdf)</span><span class="sxs-lookup"><span data-stu-id="ee4c5-124">Monitoring call detail record database (LcsCDR.mdf)</span></span></p></li>
<li><p><span data-ttu-id="ee4c5-125">Мониторинг QoE базы данных (QoEMetrics. mdf)</span><span class="sxs-lookup"><span data-stu-id="ee4c5-125">Monitoring QoE database (QoEMetrics.mdf)</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="ee4c5-126">Средство для создания баз данных SQL Server, например SQL Server Management Studio</span><span class="sxs-lookup"><span data-stu-id="ee4c5-126">SQL Server database tool, such as SQL Server Management Studio</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee4c5-127">База данных сохраняемого чата (MGC. mdf)</span><span class="sxs-lookup"><span data-stu-id="ee4c5-127">Persistent Chat database (Mgc.mdf)</span></span></p></td>
<td><p><span data-ttu-id="ee4c5-128">Процедуры резервного копирования SQL Server или Export-CsPersistentChatData.</span><span class="sxs-lookup"><span data-stu-id="ee4c5-128">SQL Server backup procedures or Export-CsPersistentChatData.</span></span> <span data-ttu-id="ee4c5-129">Export-CsPersistentChatData экспорт сохраненных данных чата в файл.</span><span class="sxs-lookup"><span data-stu-id="ee4c5-129">Export-CsPersistentChatData exports Persistent Chat data as a file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee4c5-130">Все хранилища файлов: хранилище файлов Lync Server, архивное хранилище файлов</span><span class="sxs-lookup"><span data-stu-id="ee4c5-130">All file stores: Lync Server file store, Archiving file store</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="ee4c5-131">Файлы с именем <STRONG>Meeting. Active</STRONG> не следует архивировать.</span><span class="sxs-lookup"><span data-stu-id="ee4c5-131">Files named <STRONG>Meeting.Active</STRONG> should not be backed up.</span></span> <span data-ttu-id="ee4c5-132">Эти файлы используются и заблокированы во время собрания.</span><span class="sxs-lookup"><span data-stu-id="ee4c5-132">These files are in use and locked while a meeting takes place.</span></span>


</div></td>
<td><p><span data-ttu-id="ee4c5-133">Стандартная программа управления файловой системой, например Robocopy.</span><span class="sxs-lookup"><span data-stu-id="ee4c5-133">Standard file system management tool, such as Robocopy.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="restoration"></a><span data-ttu-id="ee4c5-134">Восстановление</span><span class="sxs-lookup"><span data-stu-id="ee4c5-134">Restoration</span></span>

<span data-ttu-id="ee4c5-135">Чтобы восстановить Lync Server, воспользуйтесь инструментами, приведенными в таблице ниже.</span><span class="sxs-lookup"><span data-stu-id="ee4c5-135">To restore Lync Server, use the tools in the following table.</span></span> <span data-ttu-id="ee4c5-136">Все команды, необходимые для восстановления сервера Lync Server, могут быть внесены в сценарий.</span><span class="sxs-lookup"><span data-stu-id="ee4c5-136">All the commands that you need to restore Lync Server can be scripted.</span></span> <span data-ttu-id="ee4c5-137">Некоторые из них можно запускать удаленно, но другие должны выполняться локально, как указано в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="ee4c5-137">Some can be run remotely, but others need to be run locally, as specified in the following table.</span></span>

### <a name="tools-for-restoring-lync-server"></a><span data-ttu-id="ee4c5-138">Инструменты для восстановления сервера Lync Server</span><span class="sxs-lookup"><span data-stu-id="ee4c5-138">Tools for Restoring Lync Server</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ee4c5-139">Для этого выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="ee4c5-139">To do this:</span></span></th>
<th><span data-ttu-id="ee4c5-140">Используйте это средство или командлет:</span><span class="sxs-lookup"><span data-stu-id="ee4c5-140">Use this tool or cmdlet:</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ee4c5-141">Создание нового или очистка компьютера</span><span class="sxs-lookup"><span data-stu-id="ee4c5-141">Build a new or clean computer</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="ee4c5-142">Программное обеспечение для установки операционной системы Windows</span><span class="sxs-lookup"><span data-stu-id="ee4c5-142">Windows operating system installation software</span></span></p></li>
<li><p><span data-ttu-id="ee4c5-143">Программное обеспечение SQL Server для установки</span><span class="sxs-lookup"><span data-stu-id="ee4c5-143">SQL Server installation software</span></span></p></li>
<li><p><span data-ttu-id="ee4c5-144">Оснастка консоли управления Microsoft Management Console (MMC), если вы восстанавливаете сертификаты с помощью экспортируемого закрытого ключа</span><span class="sxs-lookup"><span data-stu-id="ee4c5-144">Certificates Microsoft Management Console (MMC) snap-in, if restoring certificates with an exportable private key</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee4c5-145">Восстановление данных из хранилища файлов</span><span class="sxs-lookup"><span data-stu-id="ee4c5-145">Restore file store data</span></span></p></td>
<td><p><span data-ttu-id="ee4c5-146">Стандартная программа управления файловой системой, например Robocopy</span><span class="sxs-lookup"><span data-stu-id="ee4c5-146">Standard file system management tool, such as Robocopy</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee4c5-147">Повторно создайте пустые базы данных и настройте разрешения для указанных ниже параметров.</span><span class="sxs-lookup"><span data-stu-id="ee4c5-147">Recreate empty databases and set permissions for the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="ee4c5-148">управления</span><span class="sxs-lookup"><span data-stu-id="ee4c5-148">Central Management store</span></span></p></li>
<li><p><span data-ttu-id="ee4c5-149">внутренний сервер</span><span class="sxs-lookup"><span data-stu-id="ee4c5-149">Back End Server</span></span></p></li>
<li><p><span data-ttu-id="ee4c5-150">база данных мониторинга;</span><span class="sxs-lookup"><span data-stu-id="ee4c5-150">Monitoring database</span></span></p></li>
<li><p><span data-ttu-id="ee4c5-151">база данных архивации;</span><span class="sxs-lookup"><span data-stu-id="ee4c5-151">Archiving database</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="ee4c5-152">Install-CsDatabase</span><span class="sxs-lookup"><span data-stu-id="ee4c5-152">Install-CsDatabase</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee4c5-153">Восстановление указателя доменных служб Active Directory в хранилище Центрального управления</span><span class="sxs-lookup"><span data-stu-id="ee4c5-153">Restore the Active Directory Domain Services pointer to the Central Management store</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="ee4c5-154">Если вы в любой момент потеряли точку соединения службы, вы можете повторно запустить этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ee4c5-154">If you lose the service connection point at any time, you can rerun this cmdlet.</span></span>


</div></td>
<td><p><span data-ttu-id="ee4c5-155">Set-CsConfigurationStoreLocation</span><span class="sxs-lookup"><span data-stu-id="ee4c5-155">Set-CsConfigurationStoreLocation</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee4c5-156">Импорт топологии, политик и параметров конфигурации в хранилище Центрального управления (XDS. mdf)</span><span class="sxs-lookup"><span data-stu-id="ee4c5-156">Import the topology, policies, and configuration settings to the Central Management store (Xds.mdf)</span></span></p></td>
<td><p><span data-ttu-id="ee4c5-157">Import-CsConfiguration</span><span class="sxs-lookup"><span data-stu-id="ee4c5-157">Import-CsConfiguration</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee4c5-158">Публикация и включение топологии</span><span class="sxs-lookup"><span data-stu-id="ee4c5-158">Publish and enable the topology</span></span></p></td>
<td><p><span data-ttu-id="ee4c5-159">топологий</span><span class="sxs-lookup"><span data-stu-id="ee4c5-159">Topology Builder</span></span></p>
<p><span data-ttu-id="ee4c5-160">/</span><span class="sxs-lookup"><span data-stu-id="ee4c5-160">-or-</span></span></p>
<p><span data-ttu-id="ee4c5-161">Publish-CsTopology и Enable-CsTopology</span><span class="sxs-lookup"><span data-stu-id="ee4c5-161">Publish-CsTopology and Enable-CsTopology</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee4c5-162">Включение последней опубликованной топологии</span><span class="sxs-lookup"><span data-stu-id="ee4c5-162">Enable the last published topology</span></span></p></td>
<td><p><span data-ttu-id="ee4c5-163">Enable-CsTopology</span><span class="sxs-lookup"><span data-stu-id="ee4c5-163">Enable-CsTopology</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee4c5-164">Переустановка серверных компонентов Lync</span><span class="sxs-lookup"><span data-stu-id="ee4c5-164">Reinstall Lync Server components</span></span></p></td>
<td><p><span data-ttu-id="ee4c5-165">Настройка сервера Lync Server</span><span class="sxs-lookup"><span data-stu-id="ee4c5-165">Lync Server Setup</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="ee4c5-166">Находится в папке установки Lync Server или мультимедиа на \setup\amd64\Setup.exe.</span><span class="sxs-lookup"><span data-stu-id="ee4c5-166">Located in the Lync Server installation folder or media at \setup\amd64\Setup.exe.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee4c5-167">Восстановление сведений о расположении (E9-1-1) Data (LIS. mdf)</span><span class="sxs-lookup"><span data-stu-id="ee4c5-167">Restore location information (E9-1-1) data (Lis.mdf)</span></span></p></td>
<td><p><span data-ttu-id="ee4c5-168">Import-CsLisConfiguration</span><span class="sxs-lookup"><span data-stu-id="ee4c5-168">Import-CsLisConfiguration</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee4c5-169">Восстановление постоянных данных пользователя (Rtcxds. mdf)</span><span class="sxs-lookup"><span data-stu-id="ee4c5-169">Restore persistent user data (Rtcxds.mdf)</span></span></p></td>
<td><p><span data-ttu-id="ee4c5-170">Import-CsUserData</span><span class="sxs-lookup"><span data-stu-id="ee4c5-170">Import-CsUserData</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee4c5-171">Восстановление данных конфигурации группы ответа (RgsConfig. mdf)</span><span class="sxs-lookup"><span data-stu-id="ee4c5-171">Restore Response Group configuration data (RgsConfig.mdf)</span></span></p></td>
<td><p><span data-ttu-id="ee4c5-172">Import-CsRgsConfiguration</span><span class="sxs-lookup"><span data-stu-id="ee4c5-172">Import-CsRgsConfiguration</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="ee4c5-173">Если конфигурация восстанавливается в только что развернутом пуле, в базе данных которого нет данных о группе ответа, следует использовать параметр – OverwriteOwner.</span><span class="sxs-lookup"><span data-stu-id="ee4c5-173">If the configuration is being restored in a newly deployed pool that has no Response Group data in the database, then you should use the –OverwriteOwner option.</span></span> <span data-ttu-id="ee4c5-174">Используйте этот параметр, даже если восстанавливаемые данные находятся в пуле с таким же полным доменным именем (FQDN).</span><span class="sxs-lookup"><span data-stu-id="ee4c5-174">Use this option even if the data being restored is in a pool with the same fully qualified domain name (FQDN).</span></span> <span data-ttu-id="ee4c5-175">В противном случае импорт завершится сбоем из-за объектов контакта с группами ответа, уже существующими в службе каталогов Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ee4c5-175">Otherwise, the import will not succeed, due to the contact objects to the Response Groups already existing in Active Directory.</span></span>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee4c5-176">Восстановите следующие базы данных:</span><span class="sxs-lookup"><span data-stu-id="ee4c5-176">Restore the following databases:</span></span></p>
<ul>
<li><p><span data-ttu-id="ee4c5-177">Архивирование базы данных (LcsLog. mdf)</span><span class="sxs-lookup"><span data-stu-id="ee4c5-177">Archiving database (LcsLog.mdf)</span></span></p></li>
<li><p><span data-ttu-id="ee4c5-178">Наблюдение за базами данных: база данных записей с данными о вызовах (LcsCDR. mdf) и QoE Database (QoEMetrics. mdf)</span><span class="sxs-lookup"><span data-stu-id="ee4c5-178">Monitoring databases: call detail record database (LcsCDR.mdf) and QoE database (QoEMetrics.mdf)</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="ee4c5-179">Средства управления базами данных SQL Server</span><span class="sxs-lookup"><span data-stu-id="ee4c5-179">SQL Server database management tools</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee4c5-180">База данных сохраняемого чата (MGS. mdf)</span><span class="sxs-lookup"><span data-stu-id="ee4c5-180">Persistent Chat database (Mgs.mdf)</span></span></p></td>
<td><p><span data-ttu-id="ee4c5-181">Процедуры восстановления SQL Server или импорт-CsPersistentChatData.</span><span class="sxs-lookup"><span data-stu-id="ee4c5-181">SQL Server restore procedures or Import-CsPersistentChatData.</span></span> <span data-ttu-id="ee4c5-182">Вы можете использовать Import-CsPersistentChatData с файлом, созданным с помощью Export-CsPersistentChatData, и данные будут импортированы в базу данных сохраняемого чата.</span><span class="sxs-lookup"><span data-stu-id="ee4c5-182">You can use Import-CsPersistentChatData with a file created by Export-CsPersistentChatData, and the data will be imported into the Persistent Chat database.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="required-permissions"></a><span data-ttu-id="ee4c5-183">Необходимые разрешения</span><span class="sxs-lookup"><span data-stu-id="ee4c5-183">Required Permissions</span></span>

<span data-ttu-id="ee4c5-184">Для выполнения всех команд, описанных в этом разделе, пользователи должны быть членами группы **RTCUniversalServerAdmins** .</span><span class="sxs-lookup"><span data-stu-id="ee4c5-184">Users must be a member of the **RTCUniversalServerAdmins** group to perform all the commands described in this topic.</span></span> <span data-ttu-id="ee4c5-185">Большинство команд резервного копирования и восстановления не поддерживают управление доступом на основе ролей (RBAC).</span><span class="sxs-lookup"><span data-stu-id="ee4c5-185">Most backup and restore commands do not support role-based access control (RBAC).</span></span> <span data-ttu-id="ee4c5-186">Два исключения — это командлеты сохраняемого чата Export-CsPersistentChatData и Import-CsPersistentChatData, которые должны выполняться пользователем, который является членом группы CsPersistentChatAdministrator.</span><span class="sxs-lookup"><span data-stu-id="ee4c5-186">Two exceptions are the Persistent Chat cmdlets Export-CsPersistentChatData and Import-CsPersistentChatData, which must be run by a user who is a member of the CsPersistentChatAdministrator group.</span></span> <span data-ttu-id="ee4c5-187">Чтобы запустить мастер развертывания Lync Server, пользователь также должен быть членом локальной группы Adminstrators.</span><span class="sxs-lookup"><span data-stu-id="ee4c5-187">To run Lync Server Deployment Wizard, a user must also be a member of the Local Adminstrators group.</span></span>

<span data-ttu-id="ee4c5-188"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ee4c5-188"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

