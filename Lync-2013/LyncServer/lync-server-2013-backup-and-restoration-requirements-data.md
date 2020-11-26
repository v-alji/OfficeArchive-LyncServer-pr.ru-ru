---
title: 'Lync Server 2013: требования к резервному копированию и восстановлению: данные'
description: 'Lync Server 2013: требования к резервному копированию и восстановлению: Data.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: 'Backup and restoration requirements: data'
ms:assetid: ecfb8e4d-cb4f-476d-9772-4486bd683c04
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202194(v=OCS.15)
ms:contentKeyID: 51541526
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7e135f09706d31ff3f0efa54c8687546de9fab78
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437989"
---
# <a name="backup-and-restoration-requirements-in-lync-server-2013-data"></a><span data-ttu-id="6fd9f-103">Требования к резервному копированию и восстановлению в Lync Server 2013: данные</span><span class="sxs-lookup"><span data-stu-id="6fd9f-103">Backup and restoration requirements in Lync Server 2013: data</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6fd9f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6fd9f-104">

<span> </span></span></span>

<span data-ttu-id="6fd9f-105">_**Тема последнего изменения:** 2013-03-26_</span><span class="sxs-lookup"><span data-stu-id="6fd9f-105">_**Topic Last Modified:** 2013-03-26_</span></span>

<span data-ttu-id="6fd9f-106">Lync Server использует параметры и сведения о конфигурации, хранящиеся в базе данных, и данные, хранящиеся в базах данных и хранилищах файлов.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-106">Lync Server uses settings and configuration information that are stored in databases, and data that is stored in databases and file stores.</span></span> <span data-ttu-id="6fd9f-107">В этой статье описаны данные, которые необходимо зарезервировать для восстановления служб, если в вашей организации возникла ошибка или сбой, а также указаны данные и компоненты, используемые Lync Server, для которого необходимо создать резервную копию отдельно.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-107">This topic describes the data that you need to back up to be able to restore service if your organization experiences a failure or outage, and also identifies the data and components used by Lync Server that you need to back up separately.</span></span>

<div>

## <a name="settings-and-configuration-requirements"></a><span data-ttu-id="6fd9f-108">Параметры и требования к конфигурации</span><span class="sxs-lookup"><span data-stu-id="6fd9f-108">Settings and Configuration Requirements</span></span>

<span data-ttu-id="6fd9f-109">Этот раздел содержит процедуры для резервного копирования и восстановления параметров и данных конфигурации, необходимых для восстановления службы Lync Server.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-109">This topic includes procedures for backing up and restoring the settings and configuration information that is required for recovery of Lync Server service.</span></span> <span data-ttu-id="6fd9f-110">Сведения о конфигурации находятся в хранилище Центрального управления или в другой серверной базе данных или на сервере Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-110">The configuration information is located in the Central Management store or on another back-end database or on Standard Edition server.</span></span>

<span data-ttu-id="6fd9f-111">В приведенной ниже таблице указаны параметры и сведения о конфигурации, необходимые для резервного копирования и восстановления.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-111">The following table identifies the settings and configuration information that you need to back up and restore.</span></span>

### <a name="settings-and-configuration-data"></a><span data-ttu-id="6fd9f-112">Параметры и данные конфигурации</span><span class="sxs-lookup"><span data-stu-id="6fd9f-112">Settings and Configuration Data</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6fd9f-113">Тип данных</span><span class="sxs-lookup"><span data-stu-id="6fd9f-113">Type of data</span></span></th>
<th><span data-ttu-id="6fd9f-114">Где хранится</span><span class="sxs-lookup"><span data-stu-id="6fd9f-114">Where stored</span></span></th>
<th><span data-ttu-id="6fd9f-115">Описание и время резервного копирования</span><span class="sxs-lookup"><span data-stu-id="6fd9f-115">Description / When to back up</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6fd9f-116">Сведения о конфигурации топологии</span><span class="sxs-lookup"><span data-stu-id="6fd9f-116">Topology configuration information</span></span></p></td>
<td><p><span data-ttu-id="6fd9f-117">Хранилище Центрального управления (база данных: XDS. mdf)</span><span class="sxs-lookup"><span data-stu-id="6fd9f-117">Central Management store (database: Xds.mdf)</span></span></p></td>
<td><p><span data-ttu-id="6fd9f-118">Параметры топологии, политики и конфигурации.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-118">Topology, policy, and configuration settings.</span></span></p>
<p><span data-ttu-id="6fd9f-119">Создавайте резервные копии с помощью обычных резервных копий и создавайте настройки и политики, используя панель управления или командлеты Lync Server.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-119">Back up with your regular backups and after you use Lync Server Control Panel or cmdlets to modify your configuration or policies.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6fd9f-120">Сведения о расположении</span><span class="sxs-lookup"><span data-stu-id="6fd9f-120">Location information</span></span></p></td>
<td><p><span data-ttu-id="6fd9f-121">Хранилище Central Management (база данных: LIS. mdf)</span><span class="sxs-lookup"><span data-stu-id="6fd9f-121">Central Management store (database: Lis.mdf)</span></span></p></td>
<td><p><span data-ttu-id="6fd9f-122">Информация о конфигурации 9-1-1 (E9-1-1) Enterprise Voice Enhanced.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-122">Enterprise Voice Enhanced 9-1-1 (E9-1-1) configuration information.</span></span> <span data-ttu-id="6fd9f-123">Эта информация обычно является статичной.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-123">This information is generally static.</span></span></p>
<p><span data-ttu-id="6fd9f-124">Создавайте резервные копии с помощью регулярного резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-124">Back up with your regular backups.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6fd9f-125">Сведения о конфигурации группы ответа</span><span class="sxs-lookup"><span data-stu-id="6fd9f-125">Response Group configuration information</span></span></p></td>
<td><p><span data-ttu-id="6fd9f-126">Сервер-сервер или стандартный выпуск Standard (база данных: RgsConfig. mdf)</span><span class="sxs-lookup"><span data-stu-id="6fd9f-126">Back End Server or Standard Edition server (database: RgsConfig.mdf)</span></span></p></td>
<td><p><span data-ttu-id="6fd9f-127">Группы агента группы ответа, очереди и рабочие процессы.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-127">Response Group agent groups, queues, and workflows.</span></span></p>
<p><span data-ttu-id="6fd9f-128">Создавайте резервные копии с помощью регулярного резервного копирования, а затем добавляйте или изменяйте группы агентов, очереди или рабочие процессы.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-128">Back up with your regular backups and after you add or change agent groups, queues, or workflows.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="data-requirements"></a><span data-ttu-id="6fd9f-129">Требования к данным</span><span class="sxs-lookup"><span data-stu-id="6fd9f-129">Data Requirements</span></span>

<span data-ttu-id="6fd9f-130">Ниже приведен список данных сервера Lync, которые необходимо создать для резервного копирования, чтобы можно было восстановить службу Lync Server в случае сбоя.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-130">Here is a list of the Lync Server data that you need to back up so that you can restore Lync Server service in the event of a failure.</span></span>

<span data-ttu-id="6fd9f-131">Обратите внимание, что некоторые типы данных не требуются для восстановления.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-131">Note that some types of data are not required for recovery.</span></span> <span data-ttu-id="6fd9f-132">В этой статье не содержатся процедуры для резервного копирования данных этих типов, в том числе следующие:</span><span class="sxs-lookup"><span data-stu-id="6fd9f-132">This topic does not contain procedures for backing up these types of data, which include the following:</span></span>

  - <span data-ttu-id="6fd9f-133">Временные данные пользователя, такие как конечные точки и подписки, серверы активных конференций и промежуточные состояния конференц-связи (база данных: RtcDyn. mdf)</span><span class="sxs-lookup"><span data-stu-id="6fd9f-133">Transient user data, such as endpoints and subscriptions, active conferencing servers, and transient conferencing states (database: RtcDyn.mdf)</span></span>

  - <span data-ttu-id="6fd9f-134">Данные адресной книги (базы данных: Rtcab. mdf и Rtcab1. mdf).</span><span class="sxs-lookup"><span data-stu-id="6fd9f-134">Address Book data (databases: Rtcab.mdf and Rtcab1.mdf).</span></span> <span data-ttu-id="6fd9f-135">База данных адресной книги автоматически генерируется из доменных служб Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-135">The Address Book database is regenerated automatically from Active Directory Domain Services.</span></span>

  - <span data-ttu-id="6fd9f-136">Динамическая информация для приложения для парковки звонков (база данных: CpsDyn. mdf)</span><span class="sxs-lookup"><span data-stu-id="6fd9f-136">Dynamic information for the Call Park application (database: CpsDyn.mdf)</span></span>

  - <span data-ttu-id="6fd9f-137">Временные данные группы ответа, например состояние входа агента и сведения о ожидании звонка (база данных: RgsDyn. mdf)</span><span class="sxs-lookup"><span data-stu-id="6fd9f-137">Transient Response Group data, such as agent sign-in state and call waiting information (database: RgsDyn.mdf)</span></span>

  - <span data-ttu-id="6fd9f-138">База данных соответствия для сохраняемого чата (база данных: MgcComp. mdf).</span><span class="sxs-lookup"><span data-stu-id="6fd9f-138">The compliance database for Persistent Chat (database: MgcComp.mdf).</span></span> <span data-ttu-id="6fd9f-139">Если на вашем компьютере включена постоянная совместимость с друзьями, данные в постоянной базе данных соответствия требованиям к Skype будут переходить на временный период до тех пор, пока адаптер настроен для чтения данных из нее и преобразования их в альтернативный формат.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-139">If you have Persistent Chat compliance enabled, the information in the Persistent Chat Compliance database is transient as long as you have an adapter configured to read information from the database and convert it to an alternate format.</span></span> <span data-ttu-id="6fd9f-140">Таким образом, база данных соответствия для сохраняемого чата считается временной.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-140">Hence the compliance database for Persistent Chat is considered transient.</span></span>
    
    <span data-ttu-id="6fd9f-141">Сервер Lync Server 2013 с сохраненным чат-адаптером входит в комплект поставки адаптера XML.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-141">Lync Server 2013 Persistent Chat Server ships with an XML adapter.</span></span> <span data-ttu-id="6fd9f-142">Вы также можете установить пользовательские адаптеры, принимающие эти данные, и переместить их в другие источники, например на размещенные в Exchange архивы.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-142">You can also install custom adapters that take this data and move it to other sources, such as Exchange Hosted Archives.</span></span>

<span data-ttu-id="6fd9f-143">В приведенной ниже таблице указаны данные, для которых требуется выполнить резервное копирование и восстановление.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-143">The following table identifies the data that you need to back up and restore.</span></span>

### <a name="data-stored-in-databases"></a><span data-ttu-id="6fd9f-144">Данные, хранящиеся в базе данных</span><span class="sxs-lookup"><span data-stu-id="6fd9f-144">Data Stored in Databases</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6fd9f-145">Тип данных</span><span class="sxs-lookup"><span data-stu-id="6fd9f-145">Type of data</span></span></th>
<th><span data-ttu-id="6fd9f-146">Где хранится</span><span class="sxs-lookup"><span data-stu-id="6fd9f-146">Where stored</span></span></th>
<th><span data-ttu-id="6fd9f-147">Описание и время резервного копирования</span><span class="sxs-lookup"><span data-stu-id="6fd9f-147">Description / When to back up</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6fd9f-148">Постоянные данные пользователя</span><span class="sxs-lookup"><span data-stu-id="6fd9f-148">Persistent user data</span></span></p></td>
<td><p><span data-ttu-id="6fd9f-149">Сервер-сервер или стандартный выпуск Standard (база данных: RTCXDS. mdf)</span><span class="sxs-lookup"><span data-stu-id="6fd9f-149">Back End Server or Standard Edition server (database: RTCXDS.mdf)</span></span></p></td>
<td><p><span data-ttu-id="6fd9f-150">Пользовательские права, списки контактов пользователей, данные сервера или пула, запланированные конференции и т. д.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-150">User rights, user Contacts lists, server or pool data, scheduled conferences, and so on.</span></span> <span data-ttu-id="6fd9f-151">Эти данные пользователя не включают содержимое, отправленное на конференцию.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-151">This user data does not include content uploaded to a conference.</span></span></p>
<p><span data-ttu-id="6fd9f-152">Создавайте резервные копии с помощью регулярного резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-152">Back up with your regular backups.</span></span> <span data-ttu-id="6fd9f-153">Эта информация является динамической, но потеря обновлений не является критическим для Lync Server, если вам необходимо восстановить последнюю обычную резервную копию.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-153">This information is dynamic, but the loss of updates is not catastrophic to Lync Server if you need to restore to your last regular backup.</span></span> <span data-ttu-id="6fd9f-154">Если список контактов важен для вашей организации, вы можете создавать резервные копии этих данных чаще.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-154">If Contacts lists are critical to your organization, you can back up this data more frequently.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6fd9f-155">Архивирование данных</span><span class="sxs-lookup"><span data-stu-id="6fd9f-155">Archiving data</span></span></p></td>
<td><p><span data-ttu-id="6fd9f-156">Архивация базы данных (база данных: LcsLog. mdf)</span><span class="sxs-lookup"><span data-stu-id="6fd9f-156">Archiving database (database: LcsLog.mdf)</span></span></p>
<p><span data-ttu-id="6fd9f-157">Эти данные могут храниться в Exchange 2013, если вы включили параметр интеграции Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-157">This data may be stored on Exchange 2013, if you have enabled the Microsoft Exchange integration option.</span></span> <span data-ttu-id="6fd9f-158">В противном случае эти данные хранятся в базе данных архивации Lync Server, которая может быть размещена вместе с другой базой данных сервера Lync или отдельно на другом сервере базы данных.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-158">Otherwise, this data is kept in a Lync Server Archiving database, which may be collocated with another Lync Server database, or stand-alone on a separate database server.</span></span></p></td>
<td><p><span data-ttu-id="6fd9f-159">Обмен мгновенными сообщениями и содержимое собрания;</span><span class="sxs-lookup"><span data-stu-id="6fd9f-159">Instant messaging (IM) and meeting content.</span></span></p>
<p><span data-ttu-id="6fd9f-160">Эти данные не очень важны для Lync Server, но это может быть важно для Организации в соответствии с нормативными потребностями.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-160">This data is not critical to Lync Server, but it may be critical to your organization for regulatory purposes.</span></span> <span data-ttu-id="6fd9f-161">Определите расписание резервного копирования соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-161">Determine your back up schedule accordingly.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6fd9f-162">Наблюдение за данными</span><span class="sxs-lookup"><span data-stu-id="6fd9f-162">Monitoring data</span></span></p></td>
<td><p><span data-ttu-id="6fd9f-163">Мониторинг баз данных (LcsCDR. mdf и QoeMetrics. mdf)</span><span class="sxs-lookup"><span data-stu-id="6fd9f-163">Monitoring databases (LcsCDR.mdf and QoeMetrics.mdf)</span></span></p>
<p><span data-ttu-id="6fd9f-164">Эти базы данных могут быть выровнены вместе с другой базой данных сервера Lync или изолированными на отдельном сервере базы данных.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-164">These databases may be collocated with another Lync Server database, or stand-alone on a separate database server.</span></span></p></td>
<td><p><span data-ttu-id="6fd9f-165">Записи с подробными сведениями о звонке (LcsCDR. mdf) и качество качества (QoE) (QoeMetrics. mdf).</span><span class="sxs-lookup"><span data-stu-id="6fd9f-165">Call detail records (LcsCDR.mdf) and Quality of Experience (QoE) metrics (QoeMetrics.mdf).</span></span></p>
<p><span data-ttu-id="6fd9f-166">Записи с подробными сведениями о звонке являются динамическими и могут быть важными для вашего бизнеса.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-166">Call detail records are dynamic and may be critical to your business.</span></span> <span data-ttu-id="6fd9f-167">Определите, нужно ли учитывать эти записи в соответствии с нормативными соображениями, в зависимости от требований к резервному плану.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-167">Determine your back up schedule by considering whether you need these records for regulatory reasons.</span></span></p>
<p><span data-ttu-id="6fd9f-168">Сведения о том, как это можно улучшить, — динамические.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-168">Quality of experience information is dynamic.</span></span> <span data-ttu-id="6fd9f-169">Потеря данных QoE не является критической для работы Lync Server, но может быть очень важна для вашего бизнеса.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-169">Loss of QoE data is not critical for the operation of Lync Server, but it may be critical to your business.</span></span> <span data-ttu-id="6fd9f-170">Определение расписания архивации в зависимости от того, насколько важной является эта информация для вашей организации.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-170">Determine your back up schedule based on how critical this information is to your organization.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6fd9f-171">Сохраняемые данные чата</span><span class="sxs-lookup"><span data-stu-id="6fd9f-171">Persistent Chat data</span></span></p></td>
<td><p><span data-ttu-id="6fd9f-172">База данных сохраняемого чата (MGD. mdf).</span><span class="sxs-lookup"><span data-stu-id="6fd9f-172">Persistent Chat database (mgd.mdf).</span></span></p>
<p><span data-ttu-id="6fd9f-173">Эта база данных может быть размещена вместе с другой базой данных сервера Lync или изолированной на отдельном сервере базы данных.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-173">This database may be collocated with another Lync Server database, or stand-alone on a separate database server.</span></span></p></td>
<td><p><span data-ttu-id="6fd9f-174">Сохраняемые данные чата — это реальное содержимое чата, которое публикуется в комнатах чата.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-174">Persistent Chat Data is actual chat content being posted in chat rooms.</span></span> <span data-ttu-id="6fd9f-175">Эти данные чаще всего важны для бизнеса.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-175">This data is often business critical.</span></span></p>
<p><span data-ttu-id="6fd9f-176">Вы можете выбрать использование резервной копии SQL Server или экспортировать базу данных с помощью командлета <strong>Export-CsPersistentChatData</strong> , предоставленного в Lync Server.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-176">You can choose to use SQL Server backup, or export the database by using the <strong>Export-CsPersistentChatData</strong> cmdlet that is provided in Lync Server.</span></span> <span data-ttu-id="6fd9f-177">Для восстановления данных вы можете импортировать и восстановить базу данных в точке последнего полного резервного копирования, что означает, что вы не сможете восстановить базу данных до точки сбоя.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-177">For recovery of the data, you can import and restore the database to the point of the last full backup, which means you cannot restore the database to the point of failure.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="file-store-data-requirements"></a><span data-ttu-id="6fd9f-178">Требования к данным в хранилище файлов</span><span class="sxs-lookup"><span data-stu-id="6fd9f-178">File Store Data Requirements</span></span>

<span data-ttu-id="6fd9f-179">В развертывании Enterprise Edition хранилище файлов Lync Server обычно находится на файловом сервере.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-179">In an Enterprise Edition deployment, the Lync Server file store is typically located on a file server.</span></span> <span data-ttu-id="6fd9f-180">В стандартном развертывании выпуска хранилище файлов Lync Server по умолчанию расположено на сервере Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-180">In a Standard Edition deployment, the Lync Server file store is located by default on the Standard Edition server.</span></span> <span data-ttu-id="6fd9f-181">Обычно существует одно хранилище файлов Lync Server, которое является общим для сайта.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-181">Typically, there is one Lync Server file store that is shared for a site.</span></span> <span data-ttu-id="6fd9f-182">В хранилище файлов сохраняемого чата используется тот же общий доступ к файлам, что и в хранилище файлов Lync Server.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-182">The Persistent Chat file store uses the same file share as the Lync Server file store.</span></span>

<span data-ttu-id="6fd9f-183">Расположение хранилища файлов идентифицировано как \\ \\ \\ имя общего сервера.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-183">File store locations are identified as \\\\server\\share name.</span></span> <span data-ttu-id="6fd9f-184">Чтобы найти определенные места хранения файлов, откройте "Построитель топологии" и просмотрите раздел " **хранилища файлов** ".</span><span class="sxs-lookup"><span data-stu-id="6fd9f-184">To find the specific locations of your file stores, open Topology Builder and look in the **File stores** node.</span></span>

<span data-ttu-id="6fd9f-185">В следующей таблице указаны хранилища файлов, для которых необходимо создать резервную копию и восстановить.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-185">The following table identifies the file stores you need to back up and restore.</span></span>

### <a name="file-stores"></a><span data-ttu-id="6fd9f-186">Хранилища файлов</span><span class="sxs-lookup"><span data-stu-id="6fd9f-186">File Stores</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6fd9f-187">Тип данных</span><span class="sxs-lookup"><span data-stu-id="6fd9f-187">Type of data</span></span></th>
<th><span data-ttu-id="6fd9f-188">Где хранится</span><span class="sxs-lookup"><span data-stu-id="6fd9f-188">Where stored</span></span></th>
<th><span data-ttu-id="6fd9f-189">Описание и время резервного копирования</span><span class="sxs-lookup"><span data-stu-id="6fd9f-189">Description / when to back up</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6fd9f-190">Хранилище файлов Lync Server</span><span class="sxs-lookup"><span data-stu-id="6fd9f-190">Lync Server file store</span></span></p></td>
<td><p><span data-ttu-id="6fd9f-191">Обычно на файловом сервере, кластере файлов или стандартном сервере выпуска</span><span class="sxs-lookup"><span data-stu-id="6fd9f-191">Typically on a file server, file cluster, or a Standard Edition server</span></span></p></td>
<td><p><span data-ttu-id="6fd9f-192">Содержимое собрания, метаданные содержимого собраний, журналы соответствия требованиям к собранию, файлы данных приложения, файлы обновлений для обновления устройства, звуковые файлы для группы ответа, регистрация звонков и файлы, отправленные в сохраняемые комнаты чатов.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-192">Meeting content, meeting content metadata, meeting compliance logs, application data files, update files for device updates, audio files for Response Group, Call Park, and Announcement applications, and files posted into Persistent Chat rooms.</span></span></p>
<p><span data-ttu-id="6fd9f-193">Создавайте резервные копии с помощью регулярного резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-193">Back up with your regular backups.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="additional-backup-requirements"></a><span data-ttu-id="6fd9f-194">Дополнительные требования к резервной копии</span><span class="sxs-lookup"><span data-stu-id="6fd9f-194">Additional Backup Requirements</span></span>

<span data-ttu-id="6fd9f-195">Чтобы обеспечить возможность восстановления служб Lync Server в случае сбоя, необходимо выполнить резервное копирование некоторых необходимых компонентов, которые не входят в состав Lync Server.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-195">To help ensure your ability to restore Lync Server services in the event of a failure, you must back up some necessary components that are not part of Lync Server itself.</span></span> <span data-ttu-id="6fd9f-196">Следующие компоненты не заархивированы или восстановлены в рамках процесса резервного копирования и восстановления на Lync Server, описанного в этом документе:</span><span class="sxs-lookup"><span data-stu-id="6fd9f-196">The following components are not backed up or restored as part of the Lync Server backup and restoration process described in this document:</span></span>

  - <span data-ttu-id="6fd9f-197">**Доменные службы Active Directory**   Вам необходимо создать резервную копию доменных служб Active Directory с помощью средств службы каталогов, а затем создать резервную копию сервера Lync Server.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-197">**Active Directory Domain Services**   You need to back up AD DS by using Active Directory tools at the same time that you back up Lync Server.</span></span> <span data-ttu-id="6fd9f-198">Чтобы избежать проблем, которые могут возникать в случае, когда приложение Lync Server считает объекты контакта, не соответствующие этим данным, в AD DS, необходимо поддерживать синхронизацию доменных служб Active Directory с Lync Server.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-198">It is important to keep AD DS synchronized with Lync Server, to avoid problems that can occur when Lync Server expects contact objects that do not match those in AD DS.</span></span> <span data-ttu-id="6fd9f-199">Доменные службы Active Directory хранят следующие параметры, используемые приложением Lync Server.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-199">AD DS stores the following settings which are used by Lync Server:</span></span>
    
      - <span data-ttu-id="6fd9f-200">Универсальный код ресурса (URI) пользователя SIP и другие параметры пользователя.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-200">User SIP URI and other user settings.</span></span>
    
      - <span data-ttu-id="6fd9f-201">Объекты контактов для таких приложений, как группа ответа и конференция.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-201">Contact objects for applications such as Response Group and Conferencing Attendant.</span></span>
    
      - <span data-ttu-id="6fd9f-202">Указатель на хранилище Центрального управления.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-202">A pointer to the Central Management Store.</span></span>
    
      - <span data-ttu-id="6fd9f-203">Учетная запись проверки подлинности Kerberos (необязательный объект компьютера) и группы безопасности Lync Server.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-203">Kerberos Authentication Account (an optional computer object) and Lync Server security groups.</span></span>
    
    <span data-ttu-id="6fd9f-204">Подробные сведения о резервном копировании и восстановлении доменных служб Active Directory в Windows Server 2008 можно найти в разделе "резервное копирование и восстановление доменных служб Active Directory" на этапе [https://go.microsoft.com/fwlink/p/?linkId=209105](https://go.microsoft.com/fwlink/p/?linkid=209105) .</span><span class="sxs-lookup"><span data-stu-id="6fd9f-204">For details about backing up and restoring AD DS in Windows Server 2008, see "AD DS Backup and Recovery Step-by-Step Guide" at [https://go.microsoft.com/fwlink/p/?linkId=209105](https://go.microsoft.com/fwlink/p/?linkid=209105).</span></span>

  - <span data-ttu-id="6fd9f-205">**Центр сертификации и сертификаты**   С помощью политики Организации создавайте резервные копии центра сертификации (ЦС) и сертификатов.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-205">**Certification authority and certificates**   Use your organization's policy for backing up your certification authority (CA) and certificates.</span></span> <span data-ttu-id="6fd9f-206">Если вы используете экспортируемые закрытые ключи, вы можете создавать резервные копии сертификата и закрытого ключа, а затем экспортировать их, если вы используете процедуры, описанные в этом документе, для восстановления Lync Server.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-206">If you use exportable private keys, you can back up the certificate and the private key, and then export them if you use the procedures in this document to restore Lync Server.</span></span> <span data-ttu-id="6fd9f-207">Если вы используете внутренний центр сертификации, вы можете повторно подать заявку, если вам нужно восстановить Lync Server.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-207">If you use an internal CA, you can re-enroll if you need to restore Lync Server.</span></span> <span data-ttu-id="6fd9f-208">Важно сохранить закрытый ключ в безопасном месте, где оно будет доступно в случае сбоя компьютера.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-208">It is important that you retain the private key in a secure location where it will be available if a computer fails.</span></span>

  - <span data-ttu-id="6fd9f-209">**System Center Operations Manager**   Если вы используете Microsoft System Center Operations Manager (прежнее название — Microsoft Operations Manager) для наблюдения за развертыванием Lync Server, вы можете при необходимости создать резервные копии данных, создаваемых на этапе мониторинга сервера Lync Server.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-209">**System Center Operations Manager**   If you use Microsoft System Center Operations Manager (formerly Microsoft Operations Manager) to monitor your Lync Server deployment, you can optionally back up the data it creates while it is monitoring Lync Server.</span></span> <span data-ttu-id="6fd9f-210">Используйте стандартный процесс архивации SQL Server для резервного копирования файлов System Center Operations Manager.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-210">Use your standard SQL Server backup process to back up System Center Operations Manager files.</span></span> <span data-ttu-id="6fd9f-211">Эти файлы не восстанавливаются во время восстановления.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-211">These files are not restored during recovery.</span></span>

  - <span data-ttu-id="6fd9f-212">**Настройка шлюза общественной коммутируемой телефонной сети (КТСОП)**   Если вы используете корпоративную голосовую или бесперебойную подразделение, вам необходимо создать резервную копию конфигурации шлюза PSTN.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-212">**Public switched telephone network (PSTN) gateway configuration**   If you use Enterprise Voice or Survivable Branch Appliances, you need to back up the PSTN gateway configuration.</span></span> <span data-ttu-id="6fd9f-213">Сведения о том, как создавать резервные копии и восстанавливать конфигурации шлюза PSTN, можно получить у своего поставщика.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-213">See your vendor for details about backing up and restoring PSTN gateway configurations.</span></span>

  - <span data-ttu-id="6fd9f-214">**Содействующие версии Lync Server или Office Communications Server**   Если вы используете развертывание Lync Server 2013 с помощью Lync Server 2010 или более ранней версии Office Communications Server, вы не сможете использовать процедуры, описанные в этом документе, для резервного копирования или восстановления более ранней версии.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-214">**Coexisting versions of Lync Server or Office Communications Server**   If your Lync Server 2013 deployment coexists with Lync Server 2010 or an earlier version of Office Communications Server, you can’t use the procedures in this document for backing up or restoring the earlier version.</span></span> <span data-ttu-id="6fd9f-215">Вместо этого необходимо использовать процедуры резервного копирования и восстановления, описанные специально для вашей более ранней версии.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-215">Instead, you must use the backup and restoration procedures documented specifically for your earlier version.</span></span> <span data-ttu-id="6fd9f-216">Подробные сведения об архивации и восстановлении сервера Lync Server 2010 можно найти в разделе [https://go.microsoft.com/fwlink/p/?linkId=265417](https://go.microsoft.com/fwlink/p/?linkid=265417) .</span><span class="sxs-lookup"><span data-stu-id="6fd9f-216">For details about backing up and restoring Lync Server 2010, see [https://go.microsoft.com/fwlink/p/?linkId=265417](https://go.microsoft.com/fwlink/p/?linkid=265417) .</span></span> <span data-ttu-id="6fd9f-217">Подробные сведения об архивации и восстановлении Microsoft Office Communications Server 2007 R2 можно найти в разделе [https://go.microsoft.com/fwlink/p/?linkId=168162](https://go.microsoft.com/fwlink/p/?linkid=168162) .</span><span class="sxs-lookup"><span data-stu-id="6fd9f-217">For details about backing up and restoring Microsoft Office Communications Server 2007 R2, see [https://go.microsoft.com/fwlink/p/?linkId=168162](https://go.microsoft.com/fwlink/p/?linkid=168162).</span></span>

  - <span data-ttu-id="6fd9f-218">**Сведения о инфраструктуре**   Вам необходимо создать резервную копию сведений о вашей инфраструктуре, например о конфигурации брандмауэра, конфигурации балансировки нагрузки, конфигурации IIS, записях DNS и IP-адресах, а также в конфигурации протокола динамической конфигурации Host Configuration (DHCP).</span><span class="sxs-lookup"><span data-stu-id="6fd9f-218">**Infrastructure information**   You need to back up information about your infrastructure, such as your firewall configuration, load balancing configuration, Internet Information Services (IIS) configuration, Domain Name System (DNS) records and IP addresses, and Dynamic Host Configuration Protocol (DHCP) configuration.</span></span> <span data-ttu-id="6fd9f-219">Подробнее об архивации этих компонентов можно узнать у соответствующих поставщиков.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-219">For details about backing up these components, check with their respective vendors.</span></span>

  - <span data-ttu-id="6fd9f-220">**Microsoft Exchange и единая система обмена сообщениями Exchange (UM)**   Создайте резервные копии и восстановление Microsoft Exchange и Exchange UM, как описано в документации по Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-220">**Microsoft Exchange and Exchange Unified Messaging (UM)**   Backup and restore Microsoft Exchange and Exchange UM as described in the Microsoft Exchange documentation.</span></span> <span data-ttu-id="6fd9f-221">Подробные сведения об архивации и восстановлении Exchange Server 2013 можно найти в статьях [https://go.microsoft.com/fwlink/?LinkId=285384](https://go.microsoft.com/fwlink/?linkid=285384) .</span><span class="sxs-lookup"><span data-stu-id="6fd9f-221">For details about backing up and restoring Exchange Server 2013, see [https://go.microsoft.com/fwlink/?LinkId=285384](https://go.microsoft.com/fwlink/?linkid=285384).</span></span> <span data-ttu-id="6fd9f-222">Подробные сведения об архивации и восстановлении Exchange Server 2010 можно найти в статьях [https://go.microsoft.com/fwlink/p/?linkId=209179](https://go.microsoft.com/fwlink/p/?linkid=209179) .</span><span class="sxs-lookup"><span data-stu-id="6fd9f-222">For details about backing up and restoring Exchange Server 2010, see [https://go.microsoft.com/fwlink/p/?linkId=209179](https://go.microsoft.com/fwlink/p/?linkid=209179).</span></span>
    
    <span data-ttu-id="6fd9f-223">Обратите внимание, что в Lync Server 2013 введена возможность иметь списки контактов пользователей, пользовательские фотографии High Definition и архивированные данные, хранящиеся в Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-223">Note that Lync Server 2013 introduces the ability to have user contact lists, high definition user photos, and archiving data stored in Exchange 2013.</span></span> <span data-ttu-id="6fd9f-224">Чтобы узнать, как создавать резервные копии этих типов данных, ознакомьтесь со списком ниже.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-224">See the following list to see how to back up these types of data:</span></span>
    
      - <span data-ttu-id="6fd9f-225">**Фотографии с высоким разрешением** записываются в резервную копию Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-225">**High definition photos** are backed up as part of the Exchange Server backup.</span></span>
    
      - <span data-ttu-id="6fd9f-226">**Единое хранилище контактов** представлено в Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-226">**Unified contact store** is introduced in Lync Server 2013.</span></span> <span data-ttu-id="6fd9f-227">Единое хранилище контактов позволяет пользователям хранить все контактные данные в Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-227">Unified contact store enables users to keep all their contact information in Exchange 2013.</span></span>
        
        <span data-ttu-id="6fd9f-228">Необходимо убедиться в том, что резервные копии обновлены для пользователей в зависимости от того, хранятся ли контакты пользователей в едином банке контактов или на обратном сервере Lync.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-228">You should make sure that backups are up-to-date for users in terms of whether their user contacts are stored in the unified contact store or on the Lync Back End Server.</span></span> <span data-ttu-id="6fd9f-229">В следующих сценариях показано, как переносить контакты пользователей в единое хранилище контактов может вызвать проблемы с процессом резервного копирования и восстановления.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-229">The following scenarios illustrate where migrating user contacts to the unified contact store can cause issues for the backup and restore process.</span></span>
        
        <span data-ttu-id="6fd9f-230">**Сценарий 1:** Контакты пользователей переносятся в единое хранилище контактов, и восстановление выполняется из резервной копии сервера Lync, сделанного до миграции контактов пользователей.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-230">**Scenario 1:** User contacts are migrated to the unified contact store, and a restore is performed from a Lync Server backup taken prior to the migration of user contacts.</span></span> <span data-ttu-id="6fd9f-231">В этом сценарии пользователь получит состояние устаревших контактов в течение одного дня, пока задача миграции сервера Lync не начнет перенос контактов пользователей в Exchange.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-231">In this scenario, the user will have a state of outdated contacts for up to one day until Lync Server Migration Task begins migrating user contacts to Exchange.</span></span> <span data-ttu-id="6fd9f-232">(Обратите внимание, что из-за того, что контакты пользователей были ранее перенесены в единое хранилище контактов, будет использоваться Контактная информация Exchange).</span><span class="sxs-lookup"><span data-stu-id="6fd9f-232">(Note that because the user contacts were previously migrated to the unified contact store, the Exchange contact information will be used).</span></span> <span data-ttu-id="6fd9f-233">В этом сценарии вмешательство администратора не требуется.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-233">No administrator intervention is needed in this scenario.</span></span>
        
        <span data-ttu-id="6fd9f-234">**Сценарий 2.** Контакты пользователей ранее хранились в едином хранилище контактов, но затем откатываются.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-234">**Scenario 2:** User contacts were previously stored in the unified contact store, but then rolled back.</span></span> <span data-ttu-id="6fd9f-235">Восстановление выполняется из резервной копии сервера Lync, которая создается, когда контакты пользователей хранились в едином банке контактов.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-235">A restore is performed from a Lync Server backup taken when the user contacts were stored in the unified contact store.</span></span> <span data-ttu-id="6fd9f-236">В этом сценарии сообщение об ошибке `Error: Incorrect Exchange Version` в журналах сервера клиента или Lyss может указывать на ошибку.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-236">In this scenario, an error message of `Error: Incorrect Exchange Version` in the client or Lyss server logs may indicate this as an issue.</span></span> <span data-ttu-id="6fd9f-237">Пользователь сможет получить доступ к списку контактов в Lync 2013 прямо из Exchange, но состояние клиента не будет совпадать с состоянием сервера Lync Server.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-237">The user will be able to access their contact list in Lync 2013 directly from Exchange, but client’s state will not match the Lync Server state.</span></span> <span data-ttu-id="6fd9f-238">Чтобы устранить эту проблему, администратору потребуется выполнить командлеты **Invoke-CsUCSRollback** для пользователей, которых вы затронули.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-238">To fix this, an administrator will need to run the **Invoke-CsUCSRollback** cmdlets for the affected users.</span></span>
    
      - <span data-ttu-id="6fd9f-239">**Данные для архивации** могут храниться в Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-239">**Archiving Data** can be stored in Exchange 2013.</span></span> <span data-ttu-id="6fd9f-240">Эти данные не очень важны для Lync Server, но это может быть важно для Организации в соответствии с нормативными потребностями.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-240">This data is not critical to Lync Server, but it may be critical to your organization for regulatory purposes.</span></span> <span data-ttu-id="6fd9f-241">Если данные архивации хранятся в Exchange и важны для вашей организации, следуйте процедурам резервного копирования и восстановления Exchange.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-241">If archiving data is stored in Exchange and is critical to your organization, then follow Exchange backup and restore procedures.</span></span> <span data-ttu-id="6fd9f-242">Обратите внимание, что архивированные данные, хранящиеся в Exchange, невозможно вернуть на сервер Lync Server.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-242">Note that archiving data stored in Exchange cannot be moved back to Lync Server.</span></span> <span data-ttu-id="6fd9f-243">Кроме того, невозможно переместить данные, которые уже хранятся в базе данных архивации Lync, в Exchange.</span><span class="sxs-lookup"><span data-stu-id="6fd9f-243">Additionally, there is no way to move data already stored in the Lync archiving database to Exchange.</span></span>

<span data-ttu-id="6fd9f-244"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6fd9f-244"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

