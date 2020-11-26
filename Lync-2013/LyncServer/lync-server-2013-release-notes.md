---
title: 'Lync Server 2013: примечания к выпуску'
description: Заметки о выпуске Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Release notes
ms:assetid: 9f9e864c-3365-4800-803c-5289bd8fd363
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205120(v=OCS.15)
ms:contentKeyID: 48184930
ms.date: 12/09/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 33fabb0912d7ea3defd91014df732368eced909e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436554"
---
# <a name="release-notes-for-lync-server-2013"></a><span data-ttu-id="62e19-103">Примечания к выпуску для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="62e19-103">Release notes for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="62e19-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="62e19-104">

<span> </span></span></span>

<span data-ttu-id="62e19-105">_**Тема последнего изменения:** 2016-12-08_</span><span class="sxs-lookup"><span data-stu-id="62e19-105">_**Topic Last Modified:** 2016-12-08_</span></span>

<span data-ttu-id="62e19-106">Добро пожаловать в заметки о выпуске Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="62e19-106">Welcome to the Lync Server 2013 Release Notes.</span></span> <span data-ttu-id="62e19-107">Сведения об известных проблемах, связанных с Lync Server 2013, содержатся в этом файле.</span><span class="sxs-lookup"><span data-stu-id="62e19-107">Refer to this file for information regarding known issues about Lync Server 2013.</span></span>

<div>

## <a name="about-this-document"></a><span data-ttu-id="62e19-108">Об этом документе</span><span class="sxs-lookup"><span data-stu-id="62e19-108">About this document</span></span>

<span data-ttu-id="62e19-109">В этом документе содержатся важные сведения, которые необходимо знать перед развертыванием и использованием Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="62e19-109">This document contains important information that you should know before you deploy and use Lync Server 2013.</span></span> <span data-ttu-id="62e19-110">Подробные сведения о Lync Server 2013 можно найти в документации [Microsoft Lync server 2013](microsoft-lync-server-2013.md) .</span><span class="sxs-lookup"><span data-stu-id="62e19-110">For details about Lync Server 2013, refer to the [Microsoft Lync Server 2013](microsoft-lync-server-2013.md) documentation.</span></span>

<span data-ttu-id="62e19-111">Этот документ включает следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="62e19-111">This document contains the following sections:</span></span>

  - <span data-ttu-id="62e19-112">Клиент Lync 2013</span><span class="sxs-lookup"><span data-stu-id="62e19-112">Lync 2013 client</span></span>

  - <span data-ttu-id="62e19-113">Lync Server</span><span class="sxs-lookup"><span data-stu-id="62e19-113">Lync Server</span></span>

  - <span data-ttu-id="62e19-114">Установка</span><span class="sxs-lookup"><span data-stu-id="62e19-114">Installation</span></span>

  - <span data-ttu-id="62e19-115">Мобильность</span><span class="sxs-lookup"><span data-stu-id="62e19-115">Mobility</span></span>

  - <span data-ttu-id="62e19-116">Конференц-связь</span><span class="sxs-lookup"><span data-stu-id="62e19-116">Conferencing</span></span>

  - <span data-ttu-id="62e19-117">Корпоративная голосовая связь</span><span class="sxs-lookup"><span data-stu-id="62e19-117">Enterprise Voice</span></span>

  - <span data-ttu-id="62e19-118">Присутствие</span><span class="sxs-lookup"><span data-stu-id="62e19-118">Presence</span></span>

  - <span data-ttu-id="62e19-119">Приложение группы ответа и приложение парковки вызовов</span><span class="sxs-lookup"><span data-stu-id="62e19-119">Response Group Application and Call Park Application</span></span>

  - <span data-ttu-id="62e19-120">Панель управления Lync Server, построитель топологий и средство планирования</span><span class="sxs-lookup"><span data-stu-id="62e19-120">Lync Server Control Panel, Topology Builder, and Planning Tool</span></span>

  - <span data-ttu-id="62e19-121">Локализации</span><span class="sxs-lookup"><span data-stu-id="62e19-121">Localization</span></span>

  - <span data-ttu-id="62e19-122">1996</span><span class="sxs-lookup"><span data-stu-id="62e19-122">Copyright</span></span>

</div>

<span id="LyncClient"></span>

<div>

## <a name="lync-2013-client"></a><span data-ttu-id="62e19-123">Клиент Lync 2013</span><span class="sxs-lookup"><span data-stu-id="62e19-123">Lync 2013 client</span></span>

<div>

## <a name="transferring-a-file-in-an-instant-message-fails-if-the-file-is-open-in-another-application"></a><span data-ttu-id="62e19-124">Передача файла в мгновенном сообщении завершается сбоем, если файл открыт в другом приложении</span><span class="sxs-lookup"><span data-stu-id="62e19-124">Transferring a file in an instant message fails if the file is open in another application</span></span>

<span data-ttu-id="62e19-125">**Проблемах**</span><span class="sxs-lookup"><span data-stu-id="62e19-125">**Issue:**</span></span>

<span data-ttu-id="62e19-126">Если вы пытаетесь передать файл, например документ Word, включив его в мгновенное сообщение другому пользователю Lync, передача будет выполнена успешно, но в действительности может возникнуть сбой при передаче файла.</span><span class="sxs-lookup"><span data-stu-id="62e19-126">If you attempt to transfer a file, such as a Word document, by including it in an instant message to another Lync user, the transfer will appear to succeed but may actually fail to transfer the file.</span></span> <span data-ttu-id="62e19-127">В клиенте Lync отображается значок для типа файлов, но этот файл нельзя открыть с помощью предполагаемого получателя.</span><span class="sxs-lookup"><span data-stu-id="62e19-127">An icon for the file type will be displayed in the Lync client, but the file cannot be opened by the intended receiver.</span></span> <span data-ttu-id="62e19-128">Выводится сообщение об ошибке, в котором сообщается о том, что передача данных завершилась неудачно.</span><span class="sxs-lookup"><span data-stu-id="62e19-128">No error message is displayed to inform you that the transfer was not successfull.</span></span>

<span data-ttu-id="62e19-129">**Смысла**</span><span class="sxs-lookup"><span data-stu-id="62e19-129">**Workaround:**</span></span>

<span data-ttu-id="62e19-130">Чтобы устранить эту ошибку, закройте открытый файл или приложение, которое оно открыто, прежде чем пытаться передать его в мгновенное сообщение.</span><span class="sxs-lookup"><span data-stu-id="62e19-130">To work around this issue, close the open file or application that has it open before attempting to transfer the file in an instant message.</span></span>

</div>

</div>

<span id="LyncServer"></span>

<div>

## <a name="lync-server"></a><span data-ttu-id="62e19-131">Lync Server</span><span class="sxs-lookup"><span data-stu-id="62e19-131">Lync Server</span></span>

<div>

## <a name="if-lync-server-storage-service-data-replication-fails-administrators-will-need-to-check-performance-counters-for-stale-storage-service-queue-items"></a><span data-ttu-id="62e19-132">Если служба хранилища данных Lync Server не может выполнить репликацию, администраторы должны будут проверять счетчики производительности для устаревших элементов очереди службы хранилища.</span><span class="sxs-lookup"><span data-stu-id="62e19-132">If Lync Server Storage Service data replication fails, administrators will need to check performance counters for stale Storage Service queue items</span></span>

<span data-ttu-id="62e19-133">**Проблемах**</span><span class="sxs-lookup"><span data-stu-id="62e19-133">**Issue:**</span></span>

<span data-ttu-id="62e19-134">Служба хранилища Lync Server использует Windows Fabric для репликации.</span><span class="sxs-lookup"><span data-stu-id="62e19-134">The Lync Server Storage Service uses Windows Fabric for replication.</span></span> <span data-ttu-id="62e19-135">Если данные удаляются на основном сервере переднего плана, но удаление на дополнительном сервере переднего плана завершается сбоем (например, при неожиданном завершении работы или ошибках на сервере переднего плана), данные могут быть оставлены и "потерянные".</span><span class="sxs-lookup"><span data-stu-id="62e19-135">If data is deleted on a primary Front End Server, but the deletion on a secondary Front End Server fails—for example, if there is an unexpected shutdown or error on the Front End Server—data can be left behind and "orphaned."</span></span> <span data-ttu-id="62e19-136">Потерянные данные могут привести к снижению производительности и потреблению свободного места на диске.</span><span class="sxs-lookup"><span data-stu-id="62e19-136">The orphaned data can cause performance to degrade and waste drive space.</span></span>

<span data-ttu-id="62e19-137">**Смысла**</span><span class="sxs-lookup"><span data-stu-id="62e19-137">**Workaround:**</span></span>

<span data-ttu-id="62e19-138">Чтобы обойти эту ошибку, если события LYSS DB, в которых используется база данных с \_ \_ \_ \_ ошибкой (ID = 32058) и LYSS \_ \_ пространство, \_ используемое \_ в журнале событий, администраторы должны проверить счетчик производительности на сервере переднего плана в разделе **Ls: LYSS-API службы хранилища** с именем **LYSS — текущее количество устаревших элементов очереди для службы хранилища**.</span><span class="sxs-lookup"><span data-stu-id="62e19-138">To work around this issue, if the events LYSS\_DB\_SPACE\_USED\_ERROR (Id=32058) and LYSS\_DB\_SPACE\_USED\_CRITICAL (Id=32059) are generated in the event log, administrators should check the performance counter on the Front End Server under **LS:LYSS - Storage Service API** with a name of **LYSS - Current number of Storage Service stale queue items**.</span></span> <span data-ttu-id="62e19-139">Если этот счетчик производительности имеет высокое значение (например, более 50 000), администратор должен запустить средство CleanuUpStorageServiceData.exe в наборе ресурсов Lync Server 2013, в котором будут удалены все потерянные данные из пула.</span><span class="sxs-lookup"><span data-stu-id="62e19-139">If this performance counter has a high value—for example, greater than 50,000—then the administrator should run the CleanuUpStorageServiceData.exe tool in the Lync Server 2013 Resource Kit, which will delete all orphaned data from the pool.</span></span> <span data-ttu-id="62e19-140">Подробнее об этом средстве можно найти в документации по набору ресурсов Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="62e19-140">For details about the tool, see the Lync Server 2013 Resource Kit documentation.</span></span>

</div>

<div>

## <a name="whenever-the-ip-address-configuration-is-changed-for-a-server-or-pool-lync-server-services-need-to-be-restarted"></a><span data-ttu-id="62e19-141">При изменении конфигурации IP-адреса для сервера или пула необходимо перезапустить службы Lync Server.</span><span class="sxs-lookup"><span data-stu-id="62e19-141">Whenever the IP Address configuration is changed for a server or pool, Lync Server services need to be restarted</span></span>

<span data-ttu-id="62e19-142">**Проблемах**</span><span class="sxs-lookup"><span data-stu-id="62e19-142">**Issue:**</span></span>

<span data-ttu-id="62e19-143">При изменении конфигурации IP-адреса для развертывания Lync Server 2013, например перехода с IPv4 на сдвоенный или из двух стеков в IPv6, не все серверные компоненты изменяют конфигурацию до тех пор, пока не будут перезапускаются эти службы.</span><span class="sxs-lookup"><span data-stu-id="62e19-143">When the IP Address configuration is changed for a Lync Server 2013 deployment, such as changing from IPv4 to Dual Stack, or from Dual Stack to Ipv6, not all server components pick up the configuration change until the services are restarted.</span></span>

<span data-ttu-id="62e19-144">**Смысла**</span><span class="sxs-lookup"><span data-stu-id="62e19-144">**Workaround:**</span></span>

<span data-ttu-id="62e19-145">Чтобы обойти эту ошибку, перезапустите службы Lync Server после изменения конфигурации IP-адреса для развертывания.</span><span class="sxs-lookup"><span data-stu-id="62e19-145">To work around this issue, restart Lync Server services after changing the IP Address configuration for the deployment.</span></span> <span data-ttu-id="62e19-146">Для этого выполните в командной консоли Lync Server следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="62e19-146">To do so, run the following cmdlets in the Lync Server Management Shell:</span></span>

   ```PowerShell
    Stop-CsWindowsService -graceful
   ```

   ```PowerShell
    Start-CsWindowsService
   ```

</div>

<div>

## <a name="the-dial-in-conferencing-synthetic-transaction-cmdlet-is-no-longer-available-in-the-lync-server-2013-management-pack"></a><span data-ttu-id="62e19-147">Командлет искусственной транзакции конференц-связи с телефонным подключением больше не доступен в пакете управления Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="62e19-147">The dial-in conferencing synthetic transaction cmdlet is no longer available in the Lync Server 2013 Management Pack</span></span>

<span data-ttu-id="62e19-148">**Проблемах**</span><span class="sxs-lookup"><span data-stu-id="62e19-148">**Issue:**</span></span>

<span data-ttu-id="62e19-149">Командлет "синтетическая транзакция конференц-связи с телефонным подключением" **— CsDialInConferencing** больше не доступен в пакете управления Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="62e19-149">The dial-in conferencing synthetic transaction cmdlet **Test-CsDialInConferencing** is no longer available in the Lync Server 2013 Management Pack.</span></span>

<span data-ttu-id="62e19-150">**Смысла**</span><span class="sxs-lookup"><span data-stu-id="62e19-150">**Workaround:**</span></span>

<span data-ttu-id="62e19-151">Использование командлета "Виртуальная транзакция конференц-связи с телефонным подключением" **— CsDialInConferencing** поддерживается только внутри предприятия.</span><span class="sxs-lookup"><span data-stu-id="62e19-151">Use of the Dial-In Conferencing Synthetic Transaction cmdlet **Test-CsDialInConferencing** is supported only internally to an enterprise.</span></span>

<span data-ttu-id="62e19-152">Администраторы могут продолжать использовать командлет в командной консоли Lync Server для устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="62e19-152">Administrators may continue to use the cmdlet in Lync Server Management Shell for troubleshooting purposes.</span></span> <span data-ttu-id="62e19-153">В случае необходимости предприятие также может разработать частный пакет управления, чтобы выполнить командлет внутренне.</span><span class="sxs-lookup"><span data-stu-id="62e19-153">If required, an enterprise can also develop a private management pack to run the cmdlet internally.</span></span>

</div>

<div>

## <a name="the-centralized-logging-service-stops-if-network-traffic-is-disrupted-when-log-files-are-being-copied-to-network-share"></a><span data-ttu-id="62e19-154">Служба централизованного ведения журналов останавливается, если сетевой трафик недоступен при копировании файлов журнала в сетевой ресурс</span><span class="sxs-lookup"><span data-stu-id="62e19-154">The Centralized Logging Service stops if network traffic is disrupted when log files are being copied to network share</span></span>

<span data-ttu-id="62e19-155">**Проблемах**</span><span class="sxs-lookup"><span data-stu-id="62e19-155">**Issue:**</span></span>

<span data-ttu-id="62e19-156">Если Служба централизованного ведения журналов настроена на использование сетевого пути (значение параметра CacheFileNetworkFolder командлета **Get-CsClsConfiguration** — допустимый путь в формате UNC), кэшированные файлы журнала копируются в сетевую папку.</span><span class="sxs-lookup"><span data-stu-id="62e19-156">When the Centralized Logging Service is configured to use a network path (the value of the CacheFileNetworkFolder parameter of the **Get-CsClsConfiguration** cmdlet is a valid UNC path), cached log files are copied to the network share.</span></span> <span data-ttu-id="62e19-157">Если при копировании файлов происходит перерыв в сетевом трафике, произойдет исключение, которое вызовет остановку службы централизованного протоколирования.</span><span class="sxs-lookup"><span data-stu-id="62e19-157">If there is a disruption in network traffic while the files are being copied, an exception will occur that will cause the centralized logging service to stop.</span></span>

<span data-ttu-id="62e19-158">Служба настроена на автоматическую перезагрузку в три значения, поэтому служба будет восстанавливаться из первых трех исключений.</span><span class="sxs-lookup"><span data-stu-id="62e19-158">The service is configured to automatically restart up to three times, so the service will recover from the first three exceptions.</span></span>

<span data-ttu-id="62e19-159">**Смысла**</span><span class="sxs-lookup"><span data-stu-id="62e19-159">**Workaround:**</span></span>

<span data-ttu-id="62e19-160">Для этой проблемы не существует обходного пути.</span><span class="sxs-lookup"><span data-stu-id="62e19-160">There is no workaround for this issue.</span></span> <span data-ttu-id="62e19-161">Чтобы определить причину ошибки, проследите за журналом событий для события с кодом 7031 от диспетчера управления службами, которые регистрируются в журнале при внезапном завершении работы службы «Служба централизованного ведения журнала» Lync Server.</span><span class="sxs-lookup"><span data-stu-id="62e19-161">To identify the issue, monitor the event log for Event ID 7031 from the "Service Control Manager" that logs when the "Lync Server Centralized Logging Service Agent" service has terminated unexpectedly.</span></span> <span data-ttu-id="62e19-162">Если это происходит более трех вхождений, перезапустите службу вручную с помощью командлета **Start-CsWindowService** .</span><span class="sxs-lookup"><span data-stu-id="62e19-162">If this happens more than three times, manually restart the service by using the **Start-CsWindowService** cmdlet.</span></span>

</div>

<div>

## <a name="storage-service-queue-items-need-to-be-imported-manually"></a><span data-ttu-id="62e19-163">Элементы очереди обслуживания хранилища нужно импортировать вручную</span><span class="sxs-lookup"><span data-stu-id="62e19-163">Storage Service Queue Items need to be imported manually</span></span>

<span data-ttu-id="62e19-164">**Проблемах**</span><span class="sxs-lookup"><span data-stu-id="62e19-164">**Issue:**</span></span>

<span data-ttu-id="62e19-165">В Lync Server 2013 хранятся данные о конференциях и обмен мгновенными сообщениями, в том числе архивированные сообщения и запись сведений о вызове (CDR) для базы данных на каждом сервере переднего плана.</span><span class="sxs-lookup"><span data-stu-id="62e19-165">Lync Server 2013 stores data about conferencing and instant messaging, such as archived messages and call detail recording (CDR), on a database on each Front End Server.</span></span> <span data-ttu-id="62e19-166">Данные хранятся в базе данных во время ее обработки до того момента, когда они будут переданы в целевое место назначения.</span><span class="sxs-lookup"><span data-stu-id="62e19-166">The data is stored in the database while it is being processed before being delivered to the intended destination.</span></span> <span data-ttu-id="62e19-167">Для повышения производительности Lync Server 2013 периодически экспортирует элементы очереди из локальной базы данных, которые не обрабатываются в течение длительного периода времени, и сохраняет их в хранилище файлов.</span><span class="sxs-lookup"><span data-stu-id="62e19-167">To improve performance, Lync Server 2013 periodically exports the queue items from the local database that are not processed for an extended period of time, and saves them on the file store.</span></span> <span data-ttu-id="62e19-168">Если хранилище файлов недоступно, элементы хранятся на каждом сервере переднего плана.</span><span class="sxs-lookup"><span data-stu-id="62e19-168">If the file store is unavailable, the items are stored on each Front End Server.</span></span> <span data-ttu-id="62e19-169">Эта же операция возникает для предотвращения потери данных во время перемещения пула.</span><span class="sxs-lookup"><span data-stu-id="62e19-169">The same operation occurs to prevent data loss during pool failover.</span></span>

<span data-ttu-id="62e19-170">В ходе операции экспорта служба хранилища Lync Server записывает все этапы в журнале событий с кодами событий 32075 (полная очистка), 32076 (полная очистка завершена), 32082 (запись на уровне обслуживания — Started), 32083 (выполняется сброс уровня сопровождения), 32089 (время на обслуживание)</span><span class="sxs-lookup"><span data-stu-id="62e19-170">During the export operation, the Lync Server Storage Service records every stage in the event log with event IDs of 32075 (full flush operation is started), 32076 (full flush is completed), 32082 (maintenance level flush is started), 32083 (maintenance level flush is completed), 32089 (flush occurred due to filling up of database).</span></span> <span data-ttu-id="62e19-171">Эти данные не будут автоматически импортированы в систему и будут обрабатываться и доставляться в конечное расположение (SQL Server или Exchange Server).</span><span class="sxs-lookup"><span data-stu-id="62e19-171">This data will not automatically be imported back to the system to be processed and delivered to its final destination (SQL Server or Exchange Server).</span></span>

<span data-ttu-id="62e19-172">**Смысла**</span><span class="sxs-lookup"><span data-stu-id="62e19-172">**Workaround:**</span></span>

<span data-ttu-id="62e19-173">Для импорта данных в систему администраторам потребуется средство ImportStorageServiceData в наборе ресурсов Lync Server Resource Kit, который добавляет данные обратно в систему для обработки и доставляется в конечную точку.</span><span class="sxs-lookup"><span data-stu-id="62e19-173">To import the data to the system, administrators will need to use the ImportStorageServiceData tool in the Lync Server Resource Kit, which will add the data back into the system to be processed and delivered to its final destination.</span></span>

</div>

<div>

## <a name="address-book-web-query-searches-will-fail-if-the-default-value-for-usenormalizationrules-is-changed-to-false"></a><span data-ttu-id="62e19-174">Поиск в веб-книге не выполняется, если значение по умолчанию для UseNormalizationRules изменено на "ложь"</span><span class="sxs-lookup"><span data-stu-id="62e19-174">Address Book Web Query searches will fail if the default value for UseNormalizationRules is changed to False</span></span>

<span data-ttu-id="62e19-175">**Проблемах**</span><span class="sxs-lookup"><span data-stu-id="62e19-175">**Issue:**</span></span>

<span data-ttu-id="62e19-176">Если значение по умолчанию для UseNormalizationRules изменено на "false", поиск в адресной книге веб-запроса завершается сбоем.</span><span class="sxs-lookup"><span data-stu-id="62e19-176">If the default value for UseNormalizationRules is changed to False, Address Book Web Query searches will fail.</span></span> <span data-ttu-id="62e19-177">После того как значение по умолчанию будет изменено, пользователи клиента Lync не смогут использовать веб-запрос адресной книги Lync для поиска пользователей.</span><span class="sxs-lookup"><span data-stu-id="62e19-177">After the default value is changed, Lync Client users will not be able to use Lync Address Book web query to search for users.</span></span>

<span data-ttu-id="62e19-178">**Смысла**</span><span class="sxs-lookup"><span data-stu-id="62e19-178">**Workaround:**</span></span>

<span data-ttu-id="62e19-179">Если в качестве значения по умолчанию для UseNormalizationRules задано значение false, чтобы пользователи могли использовать номера телефонов, определенные в доменных службах Active Directory 2013 без применения правил нормализации, обойти эту ошибку, выполнив указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="62e19-179">If the default value for UseNormalizationRules is set to False so that users can use phone numbers as defined in Active Directory Domain Services without Lync Server 2013 applying normalization rules, work around this issue by doing the following:</span></span>

1.  <span data-ttu-id="62e19-180">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="62e19-180">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="62e19-181">Выполните одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="62e19-181">Do one of the following:</span></span>
    
      - <span data-ttu-id="62e19-182">Если в развертывании есть только серверы Lync Server 2013, выполните следующий командлет на глобальном уровне, чтобы изменить значения UseNormalizationRules и IgnoreGenericRules на true:</span><span class="sxs-lookup"><span data-stu-id="62e19-182">If your deployment includes only Lync Server 2013 servers, run the following cmdlet at the global level to change the values for UseNormalizationRules and IgnoreGenericRules to True:</span></span>
        
            Set-CsAddressBookConfiguration -identity <XdsIdentity> -UseNormalizationRules=$true -IgnoreGenericRules=$true
    
      - <span data-ttu-id="62e19-183">Если в развертывании есть сочетание Lync Server 2013 и Lync Server 2010 или Office Communications Server 2007 R2, запустите следующий командлет и назначьте его каждому пулу Lync Server 2013 в топологии.</span><span class="sxs-lookup"><span data-stu-id="62e19-183">If your deployment includes a combination of Lync Server 2013 and Lync Server 2010 or Office Communications Server 2007 R2, run the following cmdlet and assign it to each Lync Server 2013 pool in the topology:</span></span>
        
            new-csAddressBookConfiguration -identity <XdsIdentity> -UseNormalizationRules=$true -IgnoreGenericRules=$true

3.  <span data-ttu-id="62e19-184">Дождитесь появления репликации CMS на всех пулах.</span><span class="sxs-lookup"><span data-stu-id="62e19-184">Wait for CMS replication to occur on all pools.</span></span>

4.  <span data-ttu-id="62e19-185">Измените файл правил нормализации телефона для развертывания, чтобы очистить содержимое.</span><span class="sxs-lookup"><span data-stu-id="62e19-185">Modify the phone normalization rules file for your deployment to clear the content.</span></span> <span data-ttu-id="62e19-186">Файл находится в общей папке каждого пула Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="62e19-186">The file is on the file share of each Lync Server 2013 pool.</span></span> <span data-ttu-id="62e19-187">Если файл не отображается, создайте пустой файл с именем " \_ \_ нормализация номера телефона компании \_ \_Rules.txt".</span><span class="sxs-lookup"><span data-stu-id="62e19-187">If the file is not present, then create an empty file named "Company\_Phone\_Number\_Normalization\_Rules.txt."</span></span>

5.  <span data-ttu-id="62e19-188">Подождите несколько минут, пока все клиентские пулы смогут прочитать новые файлы.</span><span class="sxs-lookup"><span data-stu-id="62e19-188">Wait several minutes for all Front End pools to read the new files.</span></span>

6.  <span data-ttu-id="62e19-189">Выполните следующий командлет на каждом пуле Lync Server 2013 в развертывании.</span><span class="sxs-lookup"><span data-stu-id="62e19-189">Run the following cmdlet on each Lync Server 2013 pool in your deployment.</span></span>
    
        Update-csAddressBook

</div>

<div>

## <a name="address-book-server-error-event-21054-is-generated-once-daily-for-each-lync-2013-pool"></a><span data-ttu-id="62e19-190">Сообщение об ошибке сервера адресной книги 21054 формируется один раз для каждого пула Lync 2013</span><span class="sxs-lookup"><span data-stu-id="62e19-190">Address Book Server error event 21054 is generated once daily for each Lync 2013 pool</span></span>

<span data-ttu-id="62e19-191">**Проблемах**</span><span class="sxs-lookup"><span data-stu-id="62e19-191">**Issue:**</span></span>

<span data-ttu-id="62e19-192">Lync Server 2013 Server Book создает событие ошибки 21054 один раз в день, когда выполняется ежедневное обслуживание.</span><span class="sxs-lookup"><span data-stu-id="62e19-192">Lync Server 2013 Address Book Server will generate error event 21054 once every day when performing daily maintenance.</span></span> <span data-ttu-id="62e19-193">Это сообщение об ошибке также генерируется каждый раз, когда администратор выполняет командлет **Update-csAddressBook** , даже если обновление прошло успешно.</span><span class="sxs-lookup"><span data-stu-id="62e19-193">The error is also generated every time an administrator runs the **Update-csAddressBook** cmdlet, even when the update is successful.</span></span> <span data-ttu-id="62e19-194">Однако это событие ошибки можно спокойно проигнорировать после успешного обновления.</span><span class="sxs-lookup"><span data-stu-id="62e19-194">However, this error event can safely be ignored when the update is successful.</span></span>

<span data-ttu-id="62e19-195">**Смысла**</span><span class="sxs-lookup"><span data-stu-id="62e19-195">**Workaround:**</span></span>

<span data-ttu-id="62e19-196">При возникновении этого события с ошибкой запустите следующий командлет:</span><span class="sxs-lookup"><span data-stu-id="62e19-196">When you encounter this error event, run the following cmdlet:</span></span>

    Debug-csAddressBookReplication -Poolfqdn <Pool FQDN for which the event was generated>

<span data-ttu-id="62e19-197">Если в командлете сообщается, что нет неиндексированных или отброшенных объектов, событие Error 21054 может быть проигнорировано.</span><span class="sxs-lookup"><span data-stu-id="62e19-197">If the cmdlet reports that there are no unindexed or abandoned objects, the error event 21054 can be safely ignored.</span></span>

<span data-ttu-id="62e19-198">Кроме того, индикатор работоспособности ключа (KHI) "правильно индексированные пользователи в адресной книге" должен быть отключен в System Center Operations Manager.</span><span class="sxs-lookup"><span data-stu-id="62e19-198">Additionally, the Key Health Indicator (KHI) "Address Book Users Correctly Indexed" should be turned off in System Center Operations Manager.</span></span>

</div>

<div>

## <a name="requests-may-fail-when-ipv6-is-configured-on-an-edge-pool"></a><span data-ttu-id="62e19-199">Возможен сбой запросов при настройке IPv6 на пограничном пуле</span><span class="sxs-lookup"><span data-stu-id="62e19-199">Requests may fail when IPv6 is configured on an Edge pool</span></span>

<span data-ttu-id="62e19-200">**Проблемах**</span><span class="sxs-lookup"><span data-stu-id="62e19-200">**Issue:**</span></span>

<span data-ttu-id="62e19-201">Если в пуле Edge настроен протокол IPv6, некоторые запросы к пулу Edge могут завершиться сбоем.</span><span class="sxs-lookup"><span data-stu-id="62e19-201">When IPv6 is configured on an Edge pool, some requests to the Edge pool may fail.</span></span>

<span data-ttu-id="62e19-202">**Смысла**</span><span class="sxs-lookup"><span data-stu-id="62e19-202">**Workaround:**</span></span>

<span data-ttu-id="62e19-203">Для решения этой проблемы не настраивайте для пула пограничного сервера IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="62e19-203">To work around this issue, do not configure an Edge pool with IPv6.</span></span>

</div>

<div>

## <a name="the-invoke-cspoolfailback-cmdlet-may-fail-during-pool-failback"></a><span data-ttu-id="62e19-204">Во время восстановления пула может произойти сбой командлет Invoke-csPoolFailback</span><span class="sxs-lookup"><span data-stu-id="62e19-204">The invoke-csPoolFailback cmdlet may fail during pool failback</span></span>

<span data-ttu-id="62e19-205">**Проблемах**</span><span class="sxs-lookup"><span data-stu-id="62e19-205">**Issue:**</span></span>

<span data-ttu-id="62e19-206">При попытке восстановления пула может произойти сбой командлет **Invoke-csPoolFailback** , но после повторяющихся попыток сообщение "не удалось завершить процесс Hydration".</span><span class="sxs-lookup"><span data-stu-id="62e19-206">When attempting to fail back a pool, the **invoke-csPoolFailback** cmdlet may fail with the error, "Failed to complete hydration process after repeated attempts."</span></span>

<span data-ttu-id="62e19-207">**Смысла**</span><span class="sxs-lookup"><span data-stu-id="62e19-207">**Workaround:**</span></span>

<span data-ttu-id="62e19-208">Чтобы устранить эту ошибку, запустите командлет повторно и дождитесь, пока командлет не завершится успешно.</span><span class="sxs-lookup"><span data-stu-id="62e19-208">To work around this issue, run the cmdlet again, and wait until the cmdlet succeeds.</span></span> <span data-ttu-id="62e19-209">Обратите внимание, что процесс восстановления после сбоя может занять несколько минут.</span><span class="sxs-lookup"><span data-stu-id="62e19-209">Note that the failback process can take several minutes to complete.</span></span> <span data-ttu-id="62e19-210">Для пула с 20 000 пользователей может потребоваться до 60 минут.</span><span class="sxs-lookup"><span data-stu-id="62e19-210">It may take up to 60 minutes for a pool with 20,000 users.</span></span>

</div>

<div>

## <a name="data-loss-may-occur-when-you-add-a-front-end-server-to-an-already-established-pool--hybrid-skype-for-business-online"></a><span data-ttu-id="62e19-211">При добавлении сервера переднего плана в уже установленный пул (гибридная среда, Skype для бизнеса Online) может произойти потеря данных</span><span class="sxs-lookup"><span data-stu-id="62e19-211">Data loss may occur when you add a Front End Server to an already established pool – Hybrid, Skype for Business Online</span></span>

<span data-ttu-id="62e19-212">**Проблемах**</span><span class="sxs-lookup"><span data-stu-id="62e19-212">**Issue:**</span></span>

<span data-ttu-id="62e19-213">Эта проблема может возникать в среде, в которой в пуле есть более одного сервера переднего плана, и вы либо перезагрузите один из серверов переднего плана, либо добавьте новый сервер переднего плана, который ранее не был частью пула.</span><span class="sxs-lookup"><span data-stu-id="62e19-213">You may encounter this issue in an environment where a pool has more than one Front End Server, and you either restart one of the Front End Servers, or add a new Front End Server that was not previously part of the pool.</span></span>

<span data-ttu-id="62e19-214">Пользователи, чьи данные архивируются, могут столкнуться с потерей данных до тех пор, пока не будет установлено стабильное распределение архивации данных для пула.</span><span class="sxs-lookup"><span data-stu-id="62e19-214">Users whose data is being archived may experience data loss until a stable distribution of data archiving is established for the pool.</span></span> <span data-ttu-id="62e19-215">Этот период возможной потери данных ограничен 15 минутами общения между абонентами и 30 минут для конференц-связи.</span><span class="sxs-lookup"><span data-stu-id="62e19-215">This period of potential data loss is limited to 15 minutes for person-to-person conversations, and 30 minutes for conferences.</span></span>

<span data-ttu-id="62e19-216">**Смысла**</span><span class="sxs-lookup"><span data-stu-id="62e19-216">**Workaround:**</span></span>

<span data-ttu-id="62e19-217">Если вы выполняете обслуживание, вместо того, чтобы запускать серверы переднего плана в пуле по одному, вы должны выполнить переключение из пула в другой пул, а затем выполнить на серверах задачи обслуживания.</span><span class="sxs-lookup"><span data-stu-id="62e19-217">When you perform maintenance, instead of starting Front End Servers in the pool one by one, you should fail over the pool to another pool, and then perform maintenance tasks on the servers.</span></span> <span data-ttu-id="62e19-218">Вы также можете сделать службу недоступной, прежде чем выполнять задачи обслуживания, а затем восстановить доступность по завершении обслуживания.</span><span class="sxs-lookup"><span data-stu-id="62e19-218">You can also make the service unavailable before performing maintenance tasks, and then restore availability when maintenance is complete.</span></span>

</div>

<div>

## <a name="administrators-cannot-get-licensee-count-by-using-the-get-csclientaccesslicense-cmdlet"></a><span data-ttu-id="62e19-219">Администраторам не удается получить подсчеты лицензий с помощью командлета Get-CsClientAccessLicense</span><span class="sxs-lookup"><span data-stu-id="62e19-219">Administrators cannot get licensee count by using the Get-CsClientAccessLicense cmdlet</span></span>

<span data-ttu-id="62e19-220">**Проблемах**</span><span class="sxs-lookup"><span data-stu-id="62e19-220">**Issue:**</span></span>

<span data-ttu-id="62e19-221">Администраторам не удается получить точную информацию об использовании клиентских лицензий с помощью командлета **Get-CsClientAccessLicense** .</span><span class="sxs-lookup"><span data-stu-id="62e19-221">Administrators cannot get accurate client license usage by using the **Get-CsClientAccessLicense** cmdlet.</span></span>

<span data-ttu-id="62e19-222">**Смысла**</span><span class="sxs-lookup"><span data-stu-id="62e19-222">**Workaround:**</span></span>

<span data-ttu-id="62e19-223">Для проверки типа лицензий сервера можно выполнить командлет **Get-CsService** , чтобы получить полные доменные имена (FDQNs) всех баз данных.</span><span class="sxs-lookup"><span data-stu-id="62e19-223">To check the server license type, you can run the **Get-CsService** cmdlet to retrieve the fully qualified domain names (FDQNs) of all databases.</span></span> <span data-ttu-id="62e19-224">Если полное доменное имя сервера переднего плана совпадает с полным доменным именем серверной базы данных, лицензия является лицензией Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="62e19-224">If the FQDN of the Front End Server is the same as the FQDN of the back-end database, the license is a Standard edition license.</span></span> <span data-ttu-id="62e19-225">В противном случае лицензия является лицензией Enterprise Edition.</span><span class="sxs-lookup"><span data-stu-id="62e19-225">Otherwise, the license is an Enterprise edition license.</span></span>

</div>

<div>

## <a name="client-licensee-count-is-not-accurately-reported"></a><span data-ttu-id="62e19-226">Счетчик клиентских лицензий не сообщается точно</span><span class="sxs-lookup"><span data-stu-id="62e19-226">Client licensee count is not accurately reported</span></span>

<span data-ttu-id="62e19-227">**Проблемах**</span><span class="sxs-lookup"><span data-stu-id="62e19-227">**Issue:**</span></span>

<span data-ttu-id="62e19-228">При определении счетчиков клиентских лицензий могут возникать указанные ниже условия.</span><span class="sxs-lookup"><span data-stu-id="62e19-228">When determining client license counts, you may experience the following conditions:</span></span>

1.  <span data-ttu-id="62e19-229">**Неверное число лицензий для мобильных пользователей**</span><span class="sxs-lookup"><span data-stu-id="62e19-229">**Inaccurate license count for mobile users**</span></span>
    
    <span data-ttu-id="62e19-230">Количество лицензий зависит от количества уникальных IP-адресов для пользователей, работающих с устройством.</span><span class="sxs-lookup"><span data-stu-id="62e19-230">The license count is based on the number of unique IP addresses for device-based users.</span></span> <span data-ttu-id="62e19-231">Число лицензий будет ограничено указанными ниже способами.</span><span class="sxs-lookup"><span data-stu-id="62e19-231">The license count will be limited in the following ways:</span></span>
    
      - <span data-ttu-id="62e19-232">Если IP-адрес пользователя изменяется во время сеансов Lync, лицензии будут перечислены.</span><span class="sxs-lookup"><span data-stu-id="62e19-232">Licenses will be overcounted if the IP address for the user changes during Lync sessions.</span></span> <span data-ttu-id="62e19-233">Это может произойти, если пользователь подключается к серверу Lync Server из нескольких местоположений с помощью настольного клиента.</span><span class="sxs-lookup"><span data-stu-id="62e19-233">This can occur when a user connects to Lync Server from more than one location with a desktop client.</span></span>
    
      - <span data-ttu-id="62e19-234">Лицензии будут подсчитываться, если пользователь подключается к мобильному клиенту, так как не удается определить IP-адрес устройства.</span><span class="sxs-lookup"><span data-stu-id="62e19-234">Licenses will be undercounted if a user connects with a mobile client, because the IP address for the device cannot be determined.</span></span>

2.  <span data-ttu-id="62e19-235">**Лицензии используются дважды для звонков по коммутируемой телефонной сети, а клиент Lync — на линии PSTN и звонки из Lync, переадресованные в PSTN-линии**</span><span class="sxs-lookup"><span data-stu-id="62e19-235">**Licenses are counted twice for public switched telephone network (PSTN) calls to Lync client, Lync client calls to PSTN lines, and Lync calls forwarded to PSTN lines**</span></span>
    
    <span data-ttu-id="62e19-236">В следующих сценариях вместо одной будет учитываться две дополнительные лицензии, так как номер телефона и пользователь Lync будут учитываться для определения количества используемых лицензий.</span><span class="sxs-lookup"><span data-stu-id="62e19-236">In the following scenarios, two additional licenses will be counted instead of one because both the phone number and the Lync user are counted to determine the number of licenses used.</span></span> <span data-ttu-id="62e19-237">Чтобы получить точные данные о лицензировании, вручную удалите лицензии, созданные с помощью номера телефона.</span><span class="sxs-lookup"><span data-stu-id="62e19-237">To obtain accurate licensing data, manually remove the licenses generated by a phone number.</span></span>
    
      - <span data-ttu-id="62e19-238">Телефонный звонок в Lync по телефонной линии</span><span class="sxs-lookup"><span data-stu-id="62e19-238">A PSTN phone call to Lync</span></span>
    
      - <span data-ttu-id="62e19-239">Вызов Lync на линии PSTN</span><span class="sxs-lookup"><span data-stu-id="62e19-239">A Lync call to a PSTN line</span></span>
    
      - <span data-ttu-id="62e19-240">КОММУТИРУЕМый Звонок в Lync, а затем Lync пересылает Звонок на телефон PSTN.</span><span class="sxs-lookup"><span data-stu-id="62e19-240">A PSTN call to Lync, and then Lync forwards the call to a PSTN line.</span></span> <span data-ttu-id="62e19-241">Будет учитываться одна из линий PSTN.</span><span class="sxs-lookup"><span data-stu-id="62e19-241">One of the PSTN lines will be counted.</span></span>

3.  <span data-ttu-id="62e19-242">**Лицензия не будет учитываться при входе в систему Lync на телефоне**</span><span class="sxs-lookup"><span data-stu-id="62e19-242">**A license will not be counted for a logged-on Lync phone**</span></span>
    
    <span data-ttu-id="62e19-243">Если пользователь использует телефон, сертифицированный Lync, если телефон входит в систему и остается подключенным, то есть состояние входа в систему, но при этом номер телефона не будет считаться на использование лицензии, если запрос на лицензии произошел после входа в систему.</span><span class="sxs-lookup"><span data-stu-id="62e19-243">When a user uses a Lync-certified phone, if the phone logs in and stays connected, which retains its logon status, the phone will not be counted as using a license if the query for licenses occurs after the phone logged in.</span></span>

4.  <span data-ttu-id="62e19-244">**Лицензии, подсчитанные для КОММУТИРУЕМых телефонов, соединяющих конференции**</span><span class="sxs-lookup"><span data-stu-id="62e19-244">**Licenses counted for PSTN phones joining conferences**</span></span>
    
    <span data-ttu-id="62e19-245">Когда пользователь присоединяется к Конференции с помощью телефонной сети PSTN, лицензия будет считаться неточной для присоединения к Конференции.</span><span class="sxs-lookup"><span data-stu-id="62e19-245">When a user joins a conference with a PSTN phone, a license will inaccurately be counted for joining the conference.</span></span> <span data-ttu-id="62e19-246">Тем не менее, для присоединения к Конференции с помощью телефонной сети PSTN лицензия не требуется.</span><span class="sxs-lookup"><span data-stu-id="62e19-246">However, no license is needed to join a conference with a PSTN phone.</span></span>

<span data-ttu-id="62e19-247">**Смысла**</span><span class="sxs-lookup"><span data-stu-id="62e19-247">**Workaround:**</span></span>

1.  <span data-ttu-id="62e19-248">**Неверное число лицензий для мобильных пользователей**</span><span class="sxs-lookup"><span data-stu-id="62e19-248">**Inaccurate license count for mobile users**</span></span>
    
      - <span data-ttu-id="62e19-249">Вы можете вручную идентифицировать IP-адреса, которые принадлежат тому же устройству, а затем удалить один из них в подсчете лицензий.</span><span class="sxs-lookup"><span data-stu-id="62e19-249">You can manually identify the IP addresses that belong to the same device and then remove one of them in the license count.</span></span>
    
      - <span data-ttu-id="62e19-250">Для этой проблемы не существует обходного пути для мобильных устройств, которые подключаются с помощью клиента Lync.</span><span class="sxs-lookup"><span data-stu-id="62e19-250">There is no workaround for this issue with mobile devices connecting with Lync client.</span></span>

2.  <span data-ttu-id="62e19-251">**Лицензии используются дважды для звонков по коммутируемой телефонной линии в клиенте Lync, клиентам Lync для звонков по сети PSTN и звонков в Lync, пересылаемых на линии PSTN**</span><span class="sxs-lookup"><span data-stu-id="62e19-251">**Licenses are counted twice for PSTN calls to Lync client, Lync client calls to PSTN lines, and Lync calls forwarded to PSTN lines**</span></span>
    
    <span data-ttu-id="62e19-252">Вам потребуется вручную указать номер телефона КТСОП и удалить число лицензий, созданное для него.</span><span class="sxs-lookup"><span data-stu-id="62e19-252">You will need to manually identify the PSTN phone number and remove the license count generated for it.</span></span>

3.  <span data-ttu-id="62e19-253">**Лицензия не будет учитываться для входного телефона Lync**</span><span class="sxs-lookup"><span data-stu-id="62e19-253">**A license will not be counted for a logged-in Lync phone**</span></span>
    
    <span data-ttu-id="62e19-254">Вы можете настроить телефон Lync для выхода из системы, а затем снова войти в систему через определенный интервал, например каждые 3 месяца.</span><span class="sxs-lookup"><span data-stu-id="62e19-254">You can configure the Lync phone to log off, and then log on again, at a regular interval, such as every 3 months.</span></span>

4.  <span data-ttu-id="62e19-255">**Лицензии, подсчитанные для КОММУТИРУЕМых телефонов, соединяющих конференции**</span><span class="sxs-lookup"><span data-stu-id="62e19-255">**Licenses counted for PSTN phones joining conferences**</span></span>
    
    <span data-ttu-id="62e19-256">Вы можете вручную идентифицировать телефонный номер PSTN, который используется для присоединения к Конференции, и удалить лицензию, созданную номером телефона.</span><span class="sxs-lookup"><span data-stu-id="62e19-256">You can manually identify the PSTN phone number that is used to join the conference and remove the license generated by the phone number.</span></span>

</div>

<div>

## <a name="the-lync-server-control-panel-stops-working-in-a-vmware-environment-after-upgrading-to-silverlight-5"></a><span data-ttu-id="62e19-257">После обновления до Silverlight 5 панель управления Lync Server перестает работать в среде VMware</span><span class="sxs-lookup"><span data-stu-id="62e19-257">The Lync Server Control Panel stops working in a VMware environment after upgrading to Silverlight 5</span></span>

<span data-ttu-id="62e19-258">**Проблемах**</span><span class="sxs-lookup"><span data-stu-id="62e19-258">**Issue:**</span></span>

<span data-ttu-id="62e19-259">Если вы используете панель управления Lync Server в среде VMware, то после обновления Microsoft Silverlight до версии 5 панель управления Lync Server может перестать работать.</span><span class="sxs-lookup"><span data-stu-id="62e19-259">If you use the Lync Server Control Panel in a VMware environment, the Lync Server Control Panel may stop working after you upgrade Microsoft Silverlight to version 5.</span></span>

<span data-ttu-id="62e19-260">**Смысла**</span><span class="sxs-lookup"><span data-stu-id="62e19-260">**Workaround:**</span></span>

<span data-ttu-id="62e19-261">Чтобы устранить эту ошибку, выполните одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="62e19-261">To work around this issue, do one of the following:</span></span>

  - <span data-ttu-id="62e19-262">Удалите Silverlight 5 и установите Silverlight 4 [https://go.microsoft.com/fwlink/p/?LinkID=149156](https://go.microsoft.com/fwlink/p/?linkid=149156) .</span><span class="sxs-lookup"><span data-stu-id="62e19-262">Uninstall Silverlight 5, and install Silverlight 4 from [https://go.microsoft.com/fwlink/p/?LinkID=149156](https://go.microsoft.com/fwlink/p/?linkid=149156).</span></span>

  - <span data-ttu-id="62e19-263">Получить доступ к панели управления Lync Server с компьютера, который не является виртуальным компьютером VMware.</span><span class="sxs-lookup"><span data-stu-id="62e19-263">Access the Lync Server Control Panel from a computer that is not a VMware virtual computer.</span></span>
    
    <span data-ttu-id="62e19-264">Для этого вы можете открыть панель управления Lync Server в меню " **Пуск** " на сервере, если на компьютере установлены средства администрирования Lync Server.</span><span class="sxs-lookup"><span data-stu-id="62e19-264">To do so, you can start the Lync Server Control Panel from the Windows **Start** menu on the server, if the Lync Server Administration tools are installed on the computer.</span></span>
    
    <span data-ttu-id="62e19-265">Вы также можете получить доступ к панели управления Lync Server с помощью веб-браузера.</span><span class="sxs-lookup"><span data-stu-id="62e19-265">You can also access the Lync Server Control Panel by using a web browser.</span></span> <span data-ttu-id="62e19-266">URL-адрес будет похож на https:// \<frontend\_pool\_fqdn\> /cscp.</span><span class="sxs-lookup"><span data-stu-id="62e19-266">The URL will be similar to https://\<frontend\_pool\_fqdn\>/cscp.</span></span>

</div>

<div>

## <a name="user-information-in-the-address-book-service-is-not-updated-after-the-distinguished-name-for-the-user-is-modified-in-active-directory"></a><span data-ttu-id="62e19-267">Сведения о пользователе в службе адресной книги не обновляются после изменения различающегося имени пользователя в Active Directory</span><span class="sxs-lookup"><span data-stu-id="62e19-267">User information in the Address Book Service is not updated after the distinguished name for the user is modified in Active Directory</span></span>

<span data-ttu-id="62e19-268">**Проблемах**</span><span class="sxs-lookup"><span data-stu-id="62e19-268">**Issue:**</span></span>

<span data-ttu-id="62e19-269">Если в доменных службах Active Directory изменилось различающееся имя пользователя (DN), все дополнительные изменения не будут обновлены в службе «адресная книга» (ABS).</span><span class="sxs-lookup"><span data-stu-id="62e19-269">If a user’s distinguished name (also known as DN) is changed in Active Directory Domain Services, any additional changes will not be updated in the Address Book Service (ABS).</span></span> <span data-ttu-id="62e19-270">Это не повлияет на вход или присутствие для пользователя, но предотвращает обмен данными для пользователя, если адрес SIP также изменился, так как при поиске будет возвращен устаревший адрес SIP.</span><span class="sxs-lookup"><span data-stu-id="62e19-270">This does not affect sign-in or presence for the user, but it will prevent communication for the user if the SIP address is also changed, because searches will return an outdated SIP address.</span></span>

<span data-ttu-id="62e19-271">**Смысла**</span><span class="sxs-lookup"><span data-stu-id="62e19-271">**Workaround:**</span></span>

<span data-ttu-id="62e19-272">Для решения этой проблемы не изменяйте DN пользователя.</span><span class="sxs-lookup"><span data-stu-id="62e19-272">To work around this issue, do not change a user’s DN.</span></span> <span data-ttu-id="62e19-273">Если вы меняете DN для пользователя на предыдущее, обновления будут отражаться в службе адресной книги.</span><span class="sxs-lookup"><span data-stu-id="62e19-273">If you revert the DN for the user to the previous value, updates will be reflected in the Address Book Service.</span></span>

</div>

</div>

<span id="Installation"></span>

<div>

## <a name="installation"></a><span data-ttu-id="62e19-274">Установка</span><span class="sxs-lookup"><span data-stu-id="62e19-274">Installation</span></span>

<div>

## <a name="using-non-ascii-characters-may-result-in-lync-server-failing-to-start"></a><span data-ttu-id="62e19-275">Использование знаков, отличных от ASCII, может привести к сбою при запуске Lync Server</span><span class="sxs-lookup"><span data-stu-id="62e19-275">Using non-ASCII characters may result in Lync server failing to start</span></span>

<span data-ttu-id="62e19-276">**Проблемах**</span><span class="sxs-lookup"><span data-stu-id="62e19-276">**Issue:**</span></span>

<span data-ttu-id="62e19-277">Программа установки завершится сбоем, если имя конечной папки содержит знаки, не входящие в набор ASCII (в том числе Юникод, набор двухбайтовых знаков (DBCS), UTF-8 и UTF-16).</span><span class="sxs-lookup"><span data-stu-id="62e19-277">Setup will fail if the destination folder name includes non-ASCII characters (including UNICODE, double-byte character set (DBCS), UTF-8, and UTF-16).</span></span> <span data-ttu-id="62e19-278">Кроме того, программа установки может быть успешно выполнена, но сервер не будет запускаться, если символы, не входящие в набор ASCII, находятся в одном из указанных ниже вариантов.</span><span class="sxs-lookup"><span data-stu-id="62e19-278">In addition, Setup may succeed but the server will not start if non-ASCII characters are contained in any of the following:</span></span>

  - <span data-ttu-id="62e19-279">Имя компьютера</span><span class="sxs-lookup"><span data-stu-id="62e19-279">Computer name</span></span>

  - <span data-ttu-id="62e19-280">Имя домена</span><span class="sxs-lookup"><span data-stu-id="62e19-280">Domain name</span></span>

  - <span data-ttu-id="62e19-281">Имя пользователя</span><span class="sxs-lookup"><span data-stu-id="62e19-281">User name</span></span>

  - <span data-ttu-id="62e19-282">URI пользователя SIP</span><span class="sxs-lookup"><span data-stu-id="62e19-282">User SIP URI</span></span>

  - <span data-ttu-id="62e19-283">Имя учетной записи службы</span><span class="sxs-lookup"><span data-stu-id="62e19-283">Service account name</span></span>

<span data-ttu-id="62e19-284">**Смысла**</span><span class="sxs-lookup"><span data-stu-id="62e19-284">**Workaround:**</span></span>

<span data-ttu-id="62e19-285">Используйте только знаки ASCII в имени конечной папки, имени компьютера, имени домена, имени пользователя, URI пользователя SIP и именах учетных записей служб.</span><span class="sxs-lookup"><span data-stu-id="62e19-285">Use only ASCII characters in the destination folder name, computer name, domain name, user name, user SIP URI, and service account names.</span></span>

</div>

<div>

## <a name="the-hotfix-for-heap-corruption-occurs-when-a-module-calls-the-insertentitybody-method-in-iis-75-must-be-installed-prior-to-installing-lync-server-2013"></a><span data-ttu-id="62e19-286">Исправление "повреждение кучи возникает, когда модуль вызывает метод InsertEntityBody в IIS 7,5", прежде чем устанавливать Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="62e19-286">The hotfix for "Heap corruption occurs when a module calls the InsertEntityBody method in IIS 7.5" must be installed prior to installing Lync Server 2013</span></span>

<span data-ttu-id="62e19-287">**Проблемах**</span><span class="sxs-lookup"><span data-stu-id="62e19-287">**Issue:**</span></span>

<span data-ttu-id="62e19-288">Исправление "повреждение кучи" возникает, когда модуль вызывает метод InsertEntityBody в IIS 7,5 "( [https://go.microsoft.com/fwlink/p/?LinkId=268602](https://go.microsoft.com/fwlink/p/?linkid=268602) ), описанный в статье базы знаний майкрософт 264886 ( [https://go.microsoft.com/fwlink/p/?LinkId=268603](https://go.microsoft.com/fwlink/p/?linkid=268603) ), перед установкой Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="62e19-288">The hotfix for "Heap corruption occurs when a module calls the InsertEntityBody method in IIS 7.5" ([https://go.microsoft.com/fwlink/p/?LinkId=268602](https://go.microsoft.com/fwlink/p/?linkid=268602)), described in Microsoft Knowledge Base article 264886 ([https://go.microsoft.com/fwlink/p/?LinkId=268603](https://go.microsoft.com/fwlink/p/?linkid=268603)), must be installed prior to installing Lync Server 2013.</span></span>

<span data-ttu-id="62e19-289">**Смысла**</span><span class="sxs-lookup"><span data-stu-id="62e19-289">**Workaround:**</span></span>

<span data-ttu-id="62e19-290">Скачайте и установите исправление в центре загрузки Майкрософт по адресу [https://go.microsoft.com/fwlink/p/?LinkId=268602](https://go.microsoft.com/fwlink/p/?linkid=268602) .</span><span class="sxs-lookup"><span data-stu-id="62e19-290">Download and install the hotfix from the Microsoft Download Center at [https://go.microsoft.com/fwlink/p/?LinkId=268602](https://go.microsoft.com/fwlink/p/?linkid=268602).</span></span>

</div>

<div>

## <a name="lync-server-2013-fails-to-install-on-ita-windows-server-2012-os-rtm-version"></a><span data-ttu-id="62e19-291">Не удается установить Lync Server 2013 в операционной системе Windows Server 2012 версии RTM</span><span class="sxs-lookup"><span data-stu-id="62e19-291">Lync Server 2013 fails to install on ITA Windows Server 2012 OS RTM version</span></span>

<span data-ttu-id="62e19-292">**Проблемах**</span><span class="sxs-lookup"><span data-stu-id="62e19-292">**Issue:**</span></span>

<span data-ttu-id="62e19-293">Не удается установить Lync Server 2013 на сервер ITA Windows Server 2012 из-за сбоя установки Windows Fabric.</span><span class="sxs-lookup"><span data-stu-id="62e19-293">Lync Server 2013 installation fails on ITA Windows Server 2012 due to Windows Fabric installation failing.</span></span>

<span data-ttu-id="62e19-294">Установка Windows Fabric завершается сбоем, так как при этом трассировка структуры создается с использованием формата времени ЧЧ: мм: СС.</span><span class="sxs-lookup"><span data-stu-id="62e19-294">Windows Fabric installation fails because fabric traces are created with the time format of HH:MM:SS.</span></span> <span data-ttu-id="62e19-295">Однако в операционной системе Windows Server ITA формат времени — чч. MM.SS.</span><span class="sxs-lookup"><span data-stu-id="62e19-295">However, in ITA Windows Server, the time format is HH.MM.SS.</span></span>

<span data-ttu-id="62e19-296">**Смысла**</span><span class="sxs-lookup"><span data-stu-id="62e19-296">**Workaround:**</span></span>

<span data-ttu-id="62e19-297">Чтобы устранить эту ошибку, обновите системный реестр перед установкой Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="62e19-297">To work around this issue, update the system registry before installing Lync Server 2013.</span></span> <span data-ttu-id="62e19-298">Раздел реестра, который необходимо обновить: HKEY \_ Пользователи \\ . Международная sTimeFormat по УМОЛЧАНИю для \\ панели управления \\ \\ .</span><span class="sxs-lookup"><span data-stu-id="62e19-298">The registry key that needs to be updated is: HKEY\_USERS\\.DEFAULT\\Control Panel\\International\\sTimeFormat.</span></span> <span data-ttu-id="62e19-299">Измените значение sTimeFormat на чч: мм: СС с помощью интерфейса командной строки Windows PowerShell следующим образом:</span><span class="sxs-lookup"><span data-stu-id="62e19-299">Change the value of sTimeFormat to HH:mm:ss by using the Windows PowerShell command-line interface as follows:</span></span>

1.  <span data-ttu-id="62e19-300">Запустите Windows PowerShell и выполните следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="62e19-300">Start Windows PowerShell and run the following cmdlets:</span></span>
    
       ```PowerShell
        New-PSDrive -Name HKU -PSProvider Registry -Root HKEY_USERS
       ```
    
       ```PowerShell
        $a="HKU:\.Default\Control Panel\International"
       ```

2.  <span data-ttu-id="62e19-301">Чтобы просмотреть текущее значение, выполните следующий командлет:</span><span class="sxs-lookup"><span data-stu-id="62e19-301">To view the current value, run the following cmdlet:</span></span>
    
        Get-itemproperty $a -Name sTimeFormat
    
    <span data-ttu-id="62e19-302">Запишите текущее значение для sTimeFormat, чтобы его можно было восстановить после завершения установки.</span><span class="sxs-lookup"><span data-stu-id="62e19-302">Make note of the current value for sTimeFormat so it can be restored after the installation is complete.</span></span>

3.  <span data-ttu-id="62e19-303">Чтобы установить новое значение, выполните следующий командлет:</span><span class="sxs-lookup"><span data-stu-id="62e19-303">To set to new value, run the following cmdlet:</span></span>
    
        Set-ItemProperty $a -Name sTimeFormat -Value "HH:mm:ss"

4.  <span data-ttu-id="62e19-304">После успешной установки Lync Server 2013 восстановите исходное значение для sTimeFormat, выполнив следующий командлет:</span><span class="sxs-lookup"><span data-stu-id="62e19-304">After Lync Server 2013 has been successfully installed, restore the original value for the sTimeFormat by running the following cmdlet:</span></span>
    
        - <span data-ttu-id="62e19-305">Set-ItemProperty значение <$a-Value ", указанное в действии 3.</span><span class="sxs-lookup"><span data-stu-id="62e19-305">Set-ItemProperty $a -Name sTimeFormat -Value "<Value noted down in Step 3.</span></span> <span data-ttu-id="62e19-306">выше> "</span><span class="sxs-lookup"><span data-stu-id="62e19-306">above>"</span></span>

</div>

</div>

<span id="Mobility"></span>

<div>

## <a name="mobility"></a><span data-ttu-id="62e19-307">Мобильность</span><span class="sxs-lookup"><span data-stu-id="62e19-307">Mobility</span></span>

<div>

## <a name="issues-for-mobile-clients-during-the-server-failover-process"></a><span data-ttu-id="62e19-308">Проблемы, связанные с мобильными клиентами в процессе отработки отказа сервера</span><span class="sxs-lookup"><span data-stu-id="62e19-308">Issues for mobile clients during the server failover process</span></span>

<span data-ttu-id="62e19-309">**Проблемах**</span><span class="sxs-lookup"><span data-stu-id="62e19-309">**Issue:**</span></span>

<span data-ttu-id="62e19-310">Если происходит сбой сервера Lync и начинается процесс отработки отказа, пользователи мобильных клиентов могут столкнуться со следующими проблемами:</span><span class="sxs-lookup"><span data-stu-id="62e19-310">When a Lync Server fails and the failover process begins, the following issues may affect mobile client users:</span></span>

  - <span data-ttu-id="62e19-311">Не удается выполнить входящий звонок или сигнал Lync в течение 10 минут после перехода на другой ресурс.</span><span class="sxs-lookup"><span data-stu-id="62e19-311">No incoming Lync call or signal for up to 10 minutes after failover begins.</span></span>

  - <span data-ttu-id="62e19-312">Не удается приема входящих запросов чата</span><span class="sxs-lookup"><span data-stu-id="62e19-312">Cannot accept incoming Chat requests</span></span>

  - <span data-ttu-id="62e19-313">Не удается присоединиться к собранию, если сервер с ошибкой является домашним сервером для пользователя</span><span class="sxs-lookup"><span data-stu-id="62e19-313">Cannot join meetings if the failed server is the home server for the user</span></span>

<span data-ttu-id="62e19-314">**Смысла**</span><span class="sxs-lookup"><span data-stu-id="62e19-314">**Workaround:**</span></span>

<span data-ttu-id="62e19-315">Для этой проблемы не существует обходного пути.</span><span class="sxs-lookup"><span data-stu-id="62e19-315">There is no workaround for this issue.</span></span> <span data-ttu-id="62e19-316">После завершения процесса отработки отказа обычно будут восстановлены обычные функции.</span><span class="sxs-lookup"><span data-stu-id="62e19-316">Normal functionality will be restored once the failover process is complete.</span></span>

</div>

<div>

## <a name="if-a-mobile-user-declines-an-incoming-call-from-another-lync-endpoint-the-call-is-displayed-as-a-missed-conversion-on-lync-mobile-clients"></a><span data-ttu-id="62e19-317">Если пользователь мобильного устройства отклоняет входящий звонок из другой конечной точки Lync, этот звонок отображается как пропущенное преобразование на мобильных клиентах Lync.</span><span class="sxs-lookup"><span data-stu-id="62e19-317">If a mobile user declines an incoming call from another Lync endpoint, the call is displayed as a missed conversion on Lync Mobile clients</span></span>

<span data-ttu-id="62e19-318">**Проблемах**</span><span class="sxs-lookup"><span data-stu-id="62e19-318">**Issue:**</span></span>

<span data-ttu-id="62e19-319">Если пользователь мобильного устройства отклоняет входящий звонок, а вызов происходит из другой конечной точки Lync, этот звонок отображается как пропущенный разговор в мобильном клиенте Lync, а не на вызов в списке звонков.</span><span class="sxs-lookup"><span data-stu-id="62e19-319">If a mobile user declines an incoming call, and the call originated from another Lync endpoint, the call is displayed as a missed conversation in the Lync Mobile client instead of a call in the device call list.</span></span>

<span data-ttu-id="62e19-320">**Смысла**</span><span class="sxs-lookup"><span data-stu-id="62e19-320">**Workaround:**</span></span>

<span data-ttu-id="62e19-321">Для этой проблемы не существует обходного пути.</span><span class="sxs-lookup"><span data-stu-id="62e19-321">There is no workaround for this issue.</span></span>

</div>

<div>

## <a name="the-mobile-client-may-not-display-a-federated-contacts-display-name-when-searching-for-contacts"></a><span data-ttu-id="62e19-322">Мобильный клиент может не отображать отображаемое имя федеративного контакта при поиске контактов.</span><span class="sxs-lookup"><span data-stu-id="62e19-322">The mobile client may not display a federated contact’s display name when searching for contacts</span></span>

<span data-ttu-id="62e19-323">**Проблемах**</span><span class="sxs-lookup"><span data-stu-id="62e19-323">**Issue:**</span></span>

<span data-ttu-id="62e19-324">Отображаемое имя для федеративных контактов может не отображаться в некоторых сценариях, например при поиске федеративного контакта в списке контактов.</span><span class="sxs-lookup"><span data-stu-id="62e19-324">The display name for federated contacts may not be displayed in some scenarios, such as when searching for a federated contact in the contact list.</span></span> <span data-ttu-id="62e19-325">Это может произойти, если в клиенте Lync Mobile отсутствует активная подписка на присутствие для контакта.</span><span class="sxs-lookup"><span data-stu-id="62e19-325">This can occur when the there is no active presence subscription for the contact from the Lync mobile client.</span></span>

<span data-ttu-id="62e19-326">**Смысла**</span><span class="sxs-lookup"><span data-stu-id="62e19-326">**Workaround:**</span></span>

<span data-ttu-id="62e19-327">Для этой проблемы не существует обходного пути.</span><span class="sxs-lookup"><span data-stu-id="62e19-327">There is no workaround for this issue.</span></span>

</div>

<div>

## <a name="in-the-mobile-client-invitee-and-timestamp-information-are-missing-from-a-missed-conversation-that-is-an-invitation-to-a-conference"></a><span data-ttu-id="62e19-328">В мобильном клиенте отсутствуют сведения о приглашенных и временных метках для пропущенной беседы, которая является приглашением на конференцию</span><span class="sxs-lookup"><span data-stu-id="62e19-328">In the mobile client, invitee and timestamp information are missing from a missed conversation that is an invitation to a conference</span></span>

<span data-ttu-id="62e19-329">**Проблемах**</span><span class="sxs-lookup"><span data-stu-id="62e19-329">**Issue:**</span></span>

<span data-ttu-id="62e19-330">В мобильном клиенте, когда пропущенный разговор является приглашением на Конференц-связь, в сообщении о приглашении и отметке экрана отсутствует информация.</span><span class="sxs-lookup"><span data-stu-id="62e19-330">In the mobile client, when a missed conversation is an invitation to a conference, the invitee and timestamp information is missing from the missed conversation message.</span></span>

<span data-ttu-id="62e19-331">**Смысла**</span><span class="sxs-lookup"><span data-stu-id="62e19-331">**Workaround:**</span></span>

<span data-ttu-id="62e19-332">Для этой проблемы не существует обходного пути.</span><span class="sxs-lookup"><span data-stu-id="62e19-332">There is no workaround for this issue.</span></span>

</div>

<div>

## <a name="mobile-client-users-making-calls-using-voip-are-not-be-able-to-leave-voice-mail-for-users-whose-voice-mail-is-configured-in-exchange-2010-or-earlier-versions"></a><span data-ttu-id="62e19-333">Пользователи мобильных клиентов, совершающие звонки по протоколу VoIP, не смогут покинуть голосовую почту для пользователей, для которых настроена Голосовая почта в Exchange 2010 или более ранних версиях.</span><span class="sxs-lookup"><span data-stu-id="62e19-333">Mobile client users making calls using VoIP are not be able to leave voice mail for users whose voice mail is configured in Exchange 2010 or earlier versions</span></span>

<span data-ttu-id="62e19-334">**Проблемах**</span><span class="sxs-lookup"><span data-stu-id="62e19-334">**Issue:**</span></span>

<span data-ttu-id="62e19-335">Если пользователь мобильного клиента использует VoIP для звонков, пользователь не сможет оставлять сообщения голосовой почты для пользователей, настроенных на использование голосовой почты в Microsoft Exchange Server 2007 или Microsoft Exchange Server 2010.</span><span class="sxs-lookup"><span data-stu-id="62e19-335">If a mobile client user is using VoIP to place calls, the user will not be able to leave voice mail messages for users configured to use voice mail in Microsoft Exchange Server 2007 or Microsoft Exchange Server 2010.</span></span>

<span data-ttu-id="62e19-336">**Смысла**</span><span class="sxs-lookup"><span data-stu-id="62e19-336">**Workaround:**</span></span>

<span data-ttu-id="62e19-337">Для решения этой проблемы используйте Exchange 2010 с пакетом обновления 1 (SP1) или более поздней версии Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="62e19-337">To work around this issue, use Exchange 2010 with SP1 or later version of Microsoft Exchange Server.</span></span>

</div>

<div>

## <a name="when-using-block-with-url-for-client-version-configuration-on-mobile-clients-an-incorrect-error-message-may-be-displayed"></a><span data-ttu-id="62e19-338">При использовании блока с URL-адресом для конфигурации версии клиента на мобильных клиентах может отображаться неправильное сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="62e19-338">When using Block with URL for Client Version Configuration on mobile clients, an incorrect error message may be displayed</span></span>

<span data-ttu-id="62e19-339">**Проблемах**</span><span class="sxs-lookup"><span data-stu-id="62e19-339">**Issue:**</span></span>

<span data-ttu-id="62e19-340">При использовании **блока с URL-адресом** конфигурации клиентской версии на мобильных клиентах, если клиентская версия не поддерживается, может отображаться неправильное сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="62e19-340">When using **Block with URL** for Client Version Configuration on mobile clients, an incorrect error message may be displayed when the client version is not supported.</span></span>

<span data-ttu-id="62e19-341">**Смысла**</span><span class="sxs-lookup"><span data-stu-id="62e19-341">**Workaround:**</span></span>

<span data-ttu-id="62e19-342">Чтобы обойти эту ошибку, настройте конфигурацию клиентской версии так, чтобы она использовала **блок** , а не **блок с URL-адресом**.</span><span class="sxs-lookup"><span data-stu-id="62e19-342">To work around this issue, configure Client Version Configuration to use **Block** instead of **Block with URL**.</span></span>

</div>

</div>

<span id="Conferencing"></span>

<div>

## <a name="conferencing"></a><span data-ttu-id="62e19-343">Конференц-связь</span><span class="sxs-lookup"><span data-stu-id="62e19-343">Conferencing</span></span>

<div>

## <a name="antivirus-software-running-on-lync-server-2013-front-end-servers-can-cause-application-domain-recycling-which-temporarily-interrupts-service-for-lync-web-app-2013-lync-mobile-2010-and-lync-mobile-2013-clients"></a><span data-ttu-id="62e19-344">Антивирусное программное обеспечение, работающее на серверах переднего плана Lync Server 2013, может вызвать повторное использование домена приложения, что временно прерывает работу служб для Lync Web App 2013, Lync Mobile 2010 и Lync Mobile 2013 клиенты</span><span class="sxs-lookup"><span data-stu-id="62e19-344">Antivirus software running on Lync Server 2013 Front End Servers can cause Application Domain recycling, which temporarily interrupts service for Lync Web App 2013, Lync Mobile 2010, and Lync Mobile 2013 clients</span></span>

<span data-ttu-id="62e19-345">**Проблемах**</span><span class="sxs-lookup"><span data-stu-id="62e19-345">**Issue:**</span></span>

<span data-ttu-id="62e19-346">Антивирусное программное обеспечение может инициировать перезапуск домена приложения, что может привести к тому, что клиентские приложения служб Windows Mobility Service 2013 и единой системы обмена сообщениями (UC) веб-API (Lync Web App 2013, Lync Mobile 2010 и Lync Mobile 2013) теряют свое состояние.</span><span class="sxs-lookup"><span data-stu-id="62e19-346">Antivirus software can trigger application domain restarts, which can result in Lync Mobility Service 2013 and unified communications (UC) Web API client applications (Lync Web App 2013, Lync Mobile 2010, and Lync Mobile 2013) to lose their state.</span></span>

<span data-ttu-id="62e19-347">**Смысла**</span><span class="sxs-lookup"><span data-stu-id="62e19-347">**Workaround:**</span></span>

<span data-ttu-id="62e19-348">Для решения этой проблемы исключите из антивирусной программы папки, содержащие веб-компоненты и платформу .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="62e19-348">To work around this issue, exclude the folders containing Web components and .NET framework from antivirus scanning.</span></span> <span data-ttu-id="62e19-349">Дополнительные сведения можно найти в статье 312592 базы знаний Майкрософт "PRB: restarts (приложение перезапустится вместе с приложением") в ASP.NET, "at [https://go.microsoft.com/fwlink/p/?linkid=3052\&kbid=312592](https://go.microsoft.com/fwlink/p/?linkid=3052%26kbid=312592) .</span><span class="sxs-lookup"><span data-stu-id="62e19-349">For details, see Microsoft Knowledge Base article 312592, "PRB: Random application restarts with 'Application is restarting' error in ASP.NET," at [https://go.microsoft.com/fwlink/p/?linkid=3052\&kbid=312592](https://go.microsoft.com/fwlink/p/?linkid=3052%26kbid=312592).</span></span>

<span data-ttu-id="62e19-350">Следует исключить следующие папки:</span><span class="sxs-lookup"><span data-stu-id="62e19-350">The following folders should be excluded:</span></span>

  - <span data-ttu-id="62e19-351">% ProgramFiles% \\ Microsoft Lync Server 2013 \\ веб-компоненты \\ MCX \\ рсш</span><span class="sxs-lookup"><span data-stu-id="62e19-351">%ProgramFiles%\\Microsoft Lync Server 2013\\Web Components\\Mcx\\Ext</span></span>

  - <span data-ttu-id="62e19-352">% ProgramFiles% \\ Microsoft Lync Server 2013 \\ веб-компоненты \\ MCX \\ int</span><span class="sxs-lookup"><span data-stu-id="62e19-352">%ProgramFiles%\\Microsoft Lync Server 2013\\Web Components\\Mcx\\Int</span></span>

  - <span data-ttu-id="62e19-353">% ProgramFiles% \\ Microsoft Lync Server 2013 \\ веб-компоненты \\ Ucwa \\ int</span><span class="sxs-lookup"><span data-stu-id="62e19-353">%ProgramFiles%\\Microsoft Lync Server 2013\\Web Components\\Ucwa\\Int</span></span>

  - <span data-ttu-id="62e19-354">% ProgramFiles% \\ Microsoft Lync Server 2013 \\ веб-компоненты \\ Ucwa \\ рсш</span><span class="sxs-lookup"><span data-stu-id="62e19-354">%ProgramFiles%\\Microsoft Lync Server 2013\\Web Components\\Ucwa\\Ext</span></span>

  - <span data-ttu-id="62e19-355">% WINDIR% \\ Microsoft.NET \\ Framework64 \\ v 4.0.30319 \\ config</span><span class="sxs-lookup"><span data-stu-id="62e19-355">%Windir%\\Microsoft.NET\\Framework64\\v4.0.30319\\Config</span></span>

</div>

<div>

## <a name="activex-controls-or-native-xmlhttp-support-must-be-enabled-in-windows-internet-explorer-to-successfully-join-conferences"></a><span data-ttu-id="62e19-356">Для успешного присоединения к конференциям в Windows Internet Explorer необходимо включить элементы ActiveX или собственную поддержку XMLHTTP</span><span class="sxs-lookup"><span data-stu-id="62e19-356">ActiveX Controls or native XMLHTTP support must be enabled in Windows Internet Explorer to successfully join conferences</span></span>

<span data-ttu-id="62e19-357">**Проблемах**</span><span class="sxs-lookup"><span data-stu-id="62e19-357">**Issue:**</span></span>

<span data-ttu-id="62e19-358">Если пользователь отключил оба элемента ActiveX и поддержку собственного XMLHTTP в Windows Internet Explorer, пользователь не сможет присоединиться к собранию, если Internet Explorer выбран в качестве браузера по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="62e19-358">If a user has disabled both ActiveX Controls and native XMLHTTP support in Windows Internet Explorer Internet browser settings, the user will not be able to join a meeting if Internet Explorer is selected as the default browser.</span></span>

<span data-ttu-id="62e19-359">**Смысла**</span><span class="sxs-lookup"><span data-stu-id="62e19-359">**Workaround:**</span></span>

<span data-ttu-id="62e19-360">Включите в Internet Explorer либо элементы ActiveX, либо встроенную поддержку XMLHTTP.</span><span class="sxs-lookup"><span data-stu-id="62e19-360">Enable either ActiveX Controls or "native XMLHTTP support" in Internet Explorer.</span></span>

</div>

<div>

## <a name="lync-server-web-conferencing-service-cannot-recover-from-critical-mode"></a><span data-ttu-id="62e19-361">Служба веб-конференций Lync Server не может восстановить базу в критическом режиме</span><span class="sxs-lookup"><span data-stu-id="62e19-361">Lync Server Web Conferencing service cannot recover from critical mode</span></span>

<span data-ttu-id="62e19-362">**Проблемах**</span><span class="sxs-lookup"><span data-stu-id="62e19-362">**Issue:**</span></span>

<span data-ttu-id="62e19-363">Если для архивации включен критический режим, в случае сбоев системы будет запущен критический режим, и Конференции больше не будут работать для участников.</span><span class="sxs-lookup"><span data-stu-id="62e19-363">If critical mode is turned for archiving, in case of system failures, critical mode will start and the conferences will no longer work for the participants.</span></span> <span data-ttu-id="62e19-364">После того как администратор исправит системные ошибки (например, исправить проблему с базой данных), служба конференц-связи с данными не будет восстановлена автоматически, а администратор должен вручную перезапустить службу конференц-связи для последующего возобновления Конференции.</span><span class="sxs-lookup"><span data-stu-id="62e19-364">After the administrator fixes the system failures (such as fixing a database issue), the data conferencing service doesn't automatically recover, and the administrator must manually restart the conferencing service for conferencing to resume.</span></span>

<span data-ttu-id="62e19-365">**Смысла**</span><span class="sxs-lookup"><span data-stu-id="62e19-365">**Workaround:**</span></span>

<span data-ttu-id="62e19-366">Администратору потребуется вручную перезапустить службу конференц-связи после устранения сбоя системы.</span><span class="sxs-lookup"><span data-stu-id="62e19-366">An administrator needs to manually restart the conferencing service after the system failure is fixed.</span></span>

</div>

<div>

## <a name="web-conferencing-service-ignores-the-http-proxy-for-external-office-web-app-servers"></a><span data-ttu-id="62e19-367">Служба веб-конференций пропускает HTTP-прокси для внешних серверов Office Web App</span><span class="sxs-lookup"><span data-stu-id="62e19-367">Web Conferencing service ignores the HTTP proxy for external Office Web App Servers</span></span>

<span data-ttu-id="62e19-368">**Проблемах**</span><span class="sxs-lookup"><span data-stu-id="62e19-368">**Issue:**</span></span>

<span data-ttu-id="62e19-369">Если вы развернули сервер Office Web Apps, внешний по отношению к службе веб-конференций (то есть серверу, не подключенному к внутренней корпоративной сети) в Интернете, сети периметра, и службе веб-конференций требуется HTTP-прокси для подключения к нему, обнаружение сервера Office Web Apps завершается сбоем.</span><span class="sxs-lookup"><span data-stu-id="62e19-369">If you have deployed an Office Web Apps Server external to the Web Conferencing service (that is, a server that is not in the internal corporate network) in the Internet, perimeter network, and the Web Conferencing service requires an HTTP proxy to connect to this, the Office Web Apps Server discovery will fail.</span></span> <span data-ttu-id="62e19-370">Служба веб-конференций пропускает параметр HTTP-прокси, как определено в построителе топологии для настройки сервера Office Web Apps.</span><span class="sxs-lookup"><span data-stu-id="62e19-370">The Web Conferencing service ignores the HTTP proxy setting, as defined in Topology Builder for Office Web Apps Server setup.</span></span> <span data-ttu-id="62e19-371">В результате клиент Lync не сможет предоставить общий доступ к Microsoft PowerPoint 2010 другим участникам Конференции.</span><span class="sxs-lookup"><span data-stu-id="62e19-371">As a result, the Lync client will not be able to do Microsoft PowerPoint 2010 sharing with other participants in the conference.</span></span> <span data-ttu-id="62e19-372">При установке локального сервера Lync Server и настройке локального сервера Office Web Apps во внутренней сети конфигурация прокси-сервера не требуется.</span><span class="sxs-lookup"><span data-stu-id="62e19-372">If you are installing Lync Server on-premises and also configure Office Web Apps Server on-premises in the internal network, a proxy configuration is not required.</span></span>

<span data-ttu-id="62e19-373">**Смысла**</span><span class="sxs-lookup"><span data-stu-id="62e19-373">**Workaround:**</span></span>

<span data-ttu-id="62e19-374">Единственным обходным решением является отсутствие конфигурации развертывания, требующей использования прокси-сервера HTTP для связи с внешним сервером Office Web Apps.</span><span class="sxs-lookup"><span data-stu-id="62e19-374">The only workaround is to not have a deployment configuration that requires the use of HTTP proxy to communicate with an external Office Web Apps Server.</span></span>

</div>

<div>

## <a name="adding-video-to-an-audio-conferencing-provider-conference-is-not-supported"></a><span data-ttu-id="62e19-375">Добавление видео к Конференции поставщика голосовой конференц-связи не поддерживается</span><span class="sxs-lookup"><span data-stu-id="62e19-375">Adding video to an audio conferencing provider conference is not supported</span></span>

<span data-ttu-id="62e19-376">**Проблемах**</span><span class="sxs-lookup"><span data-stu-id="62e19-376">**Issue:**</span></span>

<span data-ttu-id="62e19-377">Добавление видео не поддерживается, если пользователь присоединен к Конференции поставщика видеоконференций для звука.</span><span class="sxs-lookup"><span data-stu-id="62e19-377">Adding a video is not supported if the user is joined to an audio conferencing provider conference for audio.</span></span>

<span data-ttu-id="62e19-378">**Смысла**</span><span class="sxs-lookup"><span data-stu-id="62e19-378">**Workaround:**</span></span>

<span data-ttu-id="62e19-379">Для этой проблемы не существует обходного пути.</span><span class="sxs-lookup"><span data-stu-id="62e19-379">There is no workaround for this issue.</span></span>

</div>

<div>

## <a name="topologies-with-ipv6-enabled-force-the-lync-web-app-silverlight-plug-in-auto-update-to-ensure-screen-sharing-functionality-can-work-from-lync-web-app"></a><span data-ttu-id="62e19-380">Топологии с включенным параметром IPv6. принудительное автоматическое обновление Lync Web App Silverlight для обеспечения возможности демонстрации экрана с помощью Lync Web App</span><span class="sxs-lookup"><span data-stu-id="62e19-380">Topologies with IPv6 enabled force the Lync Web App Silverlight plug-in auto-update to ensure screen sharing functionality can work from Lync Web App</span></span>

<span data-ttu-id="62e19-381">**Проблемах**</span><span class="sxs-lookup"><span data-stu-id="62e19-381">**Issue:**</span></span>

<span data-ttu-id="62e19-382">Если топология настроена с поддержкой IPv6, пользователи не могут демонстрировать экран в клиенте Lync Web App, если уже установлена более ранняя версия плагина для совместного доступа к экрану.</span><span class="sxs-lookup"><span data-stu-id="62e19-382">When a topology is configured with IPv6 enabled, users cannot share their screen from the Lync Web App client if an earlier version of the screen-sharing plug-in is already installed.</span></span>

<span data-ttu-id="62e19-383">**Смысла**</span><span class="sxs-lookup"><span data-stu-id="62e19-383">**Workaround:**</span></span>

<span data-ttu-id="62e19-384">Чтобы принудительно присоединиться к последней версии плагина для совместного использования экрана при присоединении к собранию через Lync Web App, измените значение **MinSupportedBuildVersion** с "4.0.7457.0" на "4.0.7577.380" в обоих следующих файлах:</span><span class="sxs-lookup"><span data-stu-id="62e19-384">To force an update to the most recent version of the screen-sharing plug-in when joining meeting via Lync Web App, modify the value of **MinSupportedBuildVersion** from "4.0.7457.0" to "4.0.7577.380" in both of the following files:</span></span>

  - <span data-ttu-id="62e19-385">% ProgramFiles% \\ веб-компоненты Microsoft Lync Server 15 \\ \\ достигают \\ \\ клиентские \\ подключаемые модули \\ReachAppShPluginProperties.xml</span><span class="sxs-lookup"><span data-stu-id="62e19-385">%ProgramFiles%\\Microsoft Lync Server 15\\Web Components\\Reach\\Int\\Client\\Plugins\\ReachAppShPluginProperties.xml</span></span>

  - <span data-ttu-id="62e19-386">% ProgramFiles% \\ веб-компоненты Microsoft Lync Server 15 \\ \\ достигают \\ \\ \\ подключаемых модулей расширения клиента \\ReachAppShPluginProperties.xml</span><span class="sxs-lookup"><span data-stu-id="62e19-386">%ProgramFiles%\\Microsoft Lync Server 15\\Web Components\\Reach\\Ext\\Client\\Plugins\\ReachAppShPluginProperties.xml</span></span>

</div>

</div>

<span id="EnterpriseVoice"></span>

<div>

## <a name="enterprise-voice"></a><span data-ttu-id="62e19-387">Корпоративная голосовая связь</span><span class="sxs-lookup"><span data-stu-id="62e19-387">Enterprise Voice</span></span>

<div>

## <a name="in-some-cases-a-lync-client-running-on-a-computer-configured-to-use-ipv4-and-ipv6-dual-stack-might-not-support-capabilities-that-rely-in-the-ip-subnet-of-the-computer-such-as-e911-media-bypass-call-admission-control-and-location-based-routing"></a><span data-ttu-id="62e19-388">В некоторых случаях клиент Lync, работающий на компьютере, который настроен на использование IPv4 и IPv6, может не поддерживать возможности, которые используют подсеть IP компьютера, такую как E911, обход мультимедиа, управление допуском звонков и маршрутизация на основе местоположения.</span><span class="sxs-lookup"><span data-stu-id="62e19-388">In some cases, a Lync client running on a computer configured to use IPv4 and IPv6 dual stack might not support capabilities that rely in the IP subnet of the computer such as E911, Media Bypass, Call Admission Control and Location Based Routing</span></span>

<div class="">


> [!NOTE]  
> <span data-ttu-id="62e19-389">Сведения, представленные в данном разделе, относятся к накопительным обновлениям для Lync Server 2013: февраль 2013 г.</span><span class="sxs-lookup"><span data-stu-id="62e19-389">The information in this section pertains to Cumulative Updates for Lync Server 2013: February 2013.</span></span>



</div>

<span data-ttu-id="62e19-390">**Проблемах**</span><span class="sxs-lookup"><span data-stu-id="62e19-390">**Issue:**</span></span>

<span data-ttu-id="62e19-391">Если клиент Lync запущен на компьютере, на котором включена поддержка двух стеков IPv4 и IPv6, и основан на разрешении DNS для прокси-сервера, клиент может использовать адрес IPv6 компьютера для входа.</span><span class="sxs-lookup"><span data-stu-id="62e19-391">When a Lync client is running on a computer that is enabled for IPv4 and IPv6 dual stack and based on the DNS resolution of the proxy server, the client may use the IPv6 address of the computer to sign in.</span></span> <span data-ttu-id="62e19-392">После этого клиент Lync будет поддерживать только возможности, поддерживаемые протоколом IPv6, исключив E911, обход мультимедиа, управление допуском звонков и маршрутизацию на основе местоположения.</span><span class="sxs-lookup"><span data-stu-id="62e19-392">After doing so, the Lync Client will support only the capabilities supported for IPv6, which excludes E911, Media Bypass, Call Admission Control and Location Based Routing.</span></span>

<span data-ttu-id="62e19-393">**Смысла**</span><span class="sxs-lookup"><span data-stu-id="62e19-393">**Workaround:**</span></span>

<span data-ttu-id="62e19-394">Чтобы обойти эту ошибку, отключите поддержку IPv6 на клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="62e19-394">To work around this issue, disable IPv6 support on the client computer.</span></span>

</div>

<div>

## <a name="if-enterprise-voice-is-not-configured-for-a-user-the-user-will-need-to-use-e164-format-to-dial-out-from-a-conference"></a><span data-ttu-id="62e19-395">Если для пользователя не настроена Корпоративная голосовая связь, пользователю потребуется использовать формат E164 для исходящих звонков с конференции</span><span class="sxs-lookup"><span data-stu-id="62e19-395">If Enterprise Voice is not configured for a user, the user will need to use E164 format to dial out from a conference</span></span>

<span data-ttu-id="62e19-396">**Проблемах**</span><span class="sxs-lookup"><span data-stu-id="62e19-396">**Issue:**</span></span>

<span data-ttu-id="62e19-397">Если для пользователя не настроена Корпоративная голосовая связь, этот пользователь должен будет использовать формат E164 для успешного набора номера из конференции.</span><span class="sxs-lookup"><span data-stu-id="62e19-397">If Enterprise Voice is not configured for a user, that user will need to use the E164 format to successfully dial out from a conference.</span></span> <span data-ttu-id="62e19-398">Если формат E164 не используется, пользователь не сможет звонить с конференции.</span><span class="sxs-lookup"><span data-stu-id="62e19-398">If the E164 format is not used, the user will not be able to dial out from the conference.</span></span>

<span data-ttu-id="62e19-399">**Смысла**</span><span class="sxs-lookup"><span data-stu-id="62e19-399">**Workaround:**</span></span>

<span data-ttu-id="62e19-400">Для решения этой проблемы пользователи, не поддерживающие корпоративную голосовую почту, должны звонить с конференции, используя номера в формате e164.</span><span class="sxs-lookup"><span data-stu-id="62e19-400">To work around this issue, users who are not enabled for Enterprise Voice should dial out from a conference by using numbers in the E164 format.</span></span>

</div>

</div>

<span id="Presence"></span>

<div>

## <a name="presence"></a><span data-ttu-id="62e19-401">Присутствие</span><span class="sxs-lookup"><span data-stu-id="62e19-401">Presence</span></span>

<div>

## <a name="if-a-user-has-selected-block-all-invites-and-communications-while-the-unified-contact-store-is-turned-on-for-the-user-presence-status-is-not-rejected-when-it-should-be"></a><span data-ttu-id="62e19-402">Если пользователь выбрал параметр "блокировать все приглашения и обмениваться сообщениями", а единое хранилище контактов включается для пользователя, состояние присутствия не будет отвергнуто, если оно должно быть</span><span class="sxs-lookup"><span data-stu-id="62e19-402">If a user has selected "Block all invites and communications" while the unified contact store is turned on for the user, Presence status is not rejected when it should be</span></span>

<span data-ttu-id="62e19-403">**Проблемах**</span><span class="sxs-lookup"><span data-stu-id="62e19-403">**Issue:**</span></span>

<span data-ttu-id="62e19-404">Если пользователь выбрал параметр "блокировать все приглашения и обмениваться сообщениями", а единое хранилище контактов включается для пользователя, состояние присутствия не будет отвергнуто, когда оно должно быть.</span><span class="sxs-lookup"><span data-stu-id="62e19-404">If a user has selected "Block all invites and communications" while the unified contact store is turned on for the user, Presence status is not rejected when it should be.</span></span>

<span data-ttu-id="62e19-405">**Смысла**</span><span class="sxs-lookup"><span data-stu-id="62e19-405">**Workaround:**</span></span>

<span data-ttu-id="62e19-406">Для решения этой проблемы можно отключить единое хранилище контактов для пользователя.</span><span class="sxs-lookup"><span data-stu-id="62e19-406">To work around this issue, you can turn off the unified contact store for the user.</span></span> <span data-ttu-id="62e19-407">Для этого выполните следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="62e19-407">To do so, run the following cmdlets:</span></span>

    Set-CsUserServicesPolicy -Identity "<user display name>" -UcsAllowed $False

<span data-ttu-id="62e19-408">Например:</span><span class="sxs-lookup"><span data-stu-id="62e19-408">For example:</span></span>

    Set-CsUserServicesPolicy -Identity "Ken Myer" -UcsAllowed $False

</div>

<div>

## <a name="office-communications-server-2007-r2-users-homed-on-premises-are-not-able-to-see-the-presence-status-of-skype-for-business-online-users-in-hybrid-deployments---hybrid"></a><span data-ttu-id="62e19-409">Пользователи Office Communications Server 2007 R2, расположенные в локальной среде, не видят состояние присутствия пользователей Skype для бизнеса Online в гибридных развертываниях — Гибридная версия</span><span class="sxs-lookup"><span data-stu-id="62e19-409">Office Communications Server 2007 R2 users homed on-premises are not able to see the Presence status of Skype for Business Online users in hybrid deployments - Hybrid</span></span>

<span data-ttu-id="62e19-410">**Проблемах**</span><span class="sxs-lookup"><span data-stu-id="62e19-410">**Issue:**</span></span>

<span data-ttu-id="62e19-411">Эта неполадка может возникнуть в гибридном развертывании при использовании Lync Server 2013 Director.</span><span class="sxs-lookup"><span data-stu-id="62e19-411">The issue may occur in a hybrid deployment when you are using a Lync Server 2013 Director.</span></span>

<span data-ttu-id="62e19-412">Состояние присутствия для пользователей, подключенных к Skype для бизнеса Online, отображается как неизвестное для локальных пользователей.</span><span class="sxs-lookup"><span data-stu-id="62e19-412">Presence status for users homed to Skype for Business Online is displayed as Presence Unknown for on-premises users.</span></span> <span data-ttu-id="62e19-413">Кроме того, пользователи, подключенные к Skype для бизнеса Online, не видят состояние присутствия для локальных пользователей Office Communications Server R2.</span><span class="sxs-lookup"><span data-stu-id="62e19-413">Also, users homed to Skype for Business Online are not able to see presence status for Office Communications Server R2 on-premises users.</span></span>

<span data-ttu-id="62e19-414">**Смысла**</span><span class="sxs-lookup"><span data-stu-id="62e19-414">**Workaround:**</span></span>

<span data-ttu-id="62e19-415">Чтобы частично обойти эту ошибку, измените основной сервер (msRTCSIP-presencehomeserver) пользователей Skype для бизнеса Online, чтобы он указывал на локальный пул Lync Server 2013, а не в директории Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="62e19-415">To partially work around this issue, change the Home Server (msrtcsip-presencehomeserver) of the Skype for Business Online users to point to a Lync Server 2013 on-premises pool instead of the Lync Server 2013 Director.</span></span> <span data-ttu-id="62e19-416">Этот параметр можно изменить на локальном сервере переднего плана.</span><span class="sxs-lookup"><span data-stu-id="62e19-416">You can modify this setting on the on-premises Front End Server.</span></span>

<span data-ttu-id="62e19-417">Это временное решение правильно показывает состояние присутствия пользователей, которые появятся в Office Communications Server 2007 R2 для пользователей Skype для бизнеса Online.</span><span class="sxs-lookup"><span data-stu-id="62e19-417">This workaround will correctly display the Presence status of users homed to Office Communications Server 2007 R2 to Skype for Business Online users.</span></span>

</div>

</div>

<span id="ResponseGroup"></span>

<div>

## <a name="response-group-application-call-park-application-and-group-call-pickup"></a><span data-ttu-id="62e19-418">Приложение группы ответа, приложение для приостановки звонков и Отправка группового звонка</span><span class="sxs-lookup"><span data-stu-id="62e19-418">Response Group application, Call Park application, and Group Call Pickup</span></span>

<div>

## <a name="a-caller-might-hear-one-second-of-music-on-hold-during-the-establishment-of-a-call-with-the-retrieving-party"></a><span data-ttu-id="62e19-419">Вызывающий абонент может услышать одну секунду музыки на удержание во время установки звонка с помощью абонента.</span><span class="sxs-lookup"><span data-stu-id="62e19-419">A caller might hear one second of music-on-hold during the establishment of a call with the retrieving party</span></span>

<div class="">


> [!NOTE]  
> <span data-ttu-id="62e19-420">Сведения, представленные в данном разделе, относятся к накопительным обновлениям для Lync Server 2013: февраль 2013 г.</span><span class="sxs-lookup"><span data-stu-id="62e19-420">The information in this section pertains to Cumulative Updates for Lync Server 2013: February 2013.</span></span>



</div>

<span data-ttu-id="62e19-421">**Проблемах**</span><span class="sxs-lookup"><span data-stu-id="62e19-421">**Issue:**</span></span>

<span data-ttu-id="62e19-422">Когда звонок извлекается с помощью отправки группового звонка, вызывающий абонент может услышать одну секунду музыки на удержание во время установки звонка с субъекта-получатель.</span><span class="sxs-lookup"><span data-stu-id="62e19-422">When a call is retrieved via Group Call Pickup, the caller might hear one second of music-on-hold during the establishment of the call with the retriever party.</span></span>

<span data-ttu-id="62e19-423">**Смысла**</span><span class="sxs-lookup"><span data-stu-id="62e19-423">**Workaround:**</span></span>

<span data-ttu-id="62e19-424">Для этой проблемы не существует обходного пути.</span><span class="sxs-lookup"><span data-stu-id="62e19-424">There is no workaround for this issue.</span></span>

</div>

<div>

## <a name="a-response-group-agent-can-sign-in-and-sign-out-through-a-lync-server-2010-agent-console-to-lync-server-2010-formal-agent-groups-only"></a><span data-ttu-id="62e19-425">Агент группы ответа может войти в службу, а затем выйти из нее с помощью консоли агента Lync Server 2010 на сайте Lync Server 2010 формальную группу агента</span><span class="sxs-lookup"><span data-stu-id="62e19-425">A Response Group agent can sign in and sign out through a Lync Server 2010 Agent Console to Lync Server 2010 formal Agent Groups only</span></span>

<span data-ttu-id="62e19-426">**Проблемах**</span><span class="sxs-lookup"><span data-stu-id="62e19-426">**Issue:**</span></span>

<span data-ttu-id="62e19-427">Агент группы ответа Lync Server 2013 может войти в службу и выйти из нее с помощью консоли агента Lync Server 2010 на Lync Server 2010 только для групп с формальными агентами.</span><span class="sxs-lookup"><span data-stu-id="62e19-427">A Lync Server 2013 Response Group agent can sign in and sign out through a Lync Server 2010 Agent Console to Lync Server 2010 formal Agent Groups only.</span></span> <span data-ttu-id="62e19-428">В консоли агента Lync Server 2010 пользователи могут видеть только ту группу ответа Lync Server 2010, в которую она входит.</span><span class="sxs-lookup"><span data-stu-id="62e19-428">In the Lync Server 2010 Agent Console, users can see only the Lync Server 2010 Response Group that they belong to.</span></span> <span data-ttu-id="62e19-429">Пользователи не увидят ни одной из групп ответа Lync Server 2013, к которым они относятся.</span><span class="sxs-lookup"><span data-stu-id="62e19-429">They cannot see any of the Lync Server 2013 Response Groups that they belong to.</span></span>

<span data-ttu-id="62e19-430">**Смысла**</span><span class="sxs-lookup"><span data-stu-id="62e19-430">**Workaround:**</span></span>

<span data-ttu-id="62e19-431">Если агент группы ответа — пользователь Lync Server 2013 и часть группы "формальный агент" Lync Server 2013, пользователь должен получить доступ к консоли Lync Server 2013 с помощью веб-ссылки в браузере, чтобы выполнить вход и выйти из групп Lync Server 2013 Agent.</span><span class="sxs-lookup"><span data-stu-id="62e19-431">If the Response Group agent is a Lync Server 2013 user, and part of a Lync Server 2013 formal Agent Group, the user must access the Lync Server 2013 Agent Console directly via a web link in a browser to sign in to and sign out from Lync Server 2013 Agent Groups.</span></span>

</div>

<div>

## <a name="a-lync-server-2010-response-group-agent-cannot-place-calls-on-behalf-of-a-lync-server-2013-response-group"></a><span data-ttu-id="62e19-432">Агент группы ответа Lync Server 2010 не может звонить по поручению Lync Server 2013 группы ответа.</span><span class="sxs-lookup"><span data-stu-id="62e19-432">A Lync Server 2010 Response Group agent cannot place calls on behalf of a Lync Server 2013 Response Group</span></span>

<span data-ttu-id="62e19-433">**Проблемах**</span><span class="sxs-lookup"><span data-stu-id="62e19-433">**Issue:**</span></span>

<span data-ttu-id="62e19-434">Пользователь Lync Server 2010, который является агентом группы ответа Lync Server 2013, не может установить звонок от имени группы ответа.</span><span class="sxs-lookup"><span data-stu-id="62e19-434">A Lync Server 2010 user who is an Agent of a Lync Server 2013 Response Group is not able to place a call on behalf of the Response Group.</span></span> <span data-ttu-id="62e19-435">Группа ответа Lync Server 2013 будет недоступна в клиенте Lync, чтобы позвонить.</span><span class="sxs-lookup"><span data-stu-id="62e19-435">The Lync Server 2013 Response Group will not be available in the Lync Client to place a call.</span></span>

<span data-ttu-id="62e19-436">**Смысла**</span><span class="sxs-lookup"><span data-stu-id="62e19-436">**Workaround:**</span></span>

<span data-ttu-id="62e19-437">Для решения этой проблемы необходимо переместить пользователя Lync Server 2010 в Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="62e19-437">To work around this issue, you must move the Lync Server 2010 user to Lync Server 2013.</span></span>

</div>

<div>

## <a name="removing-a-response-group-from-lync-server-2010-after-it-has-been-migrated-to-lync-server-2013-will-prevent-the-response-group-from-accepting-any-incoming-calls"></a><span data-ttu-id="62e19-438">Удаление группы ответа из Lync Server 2010 после миграции на Lync Server 2013 запрещает группе ответа принимать входящие звонки</span><span class="sxs-lookup"><span data-stu-id="62e19-438">Removing a Response Group from Lync Server 2010 after it has been migrated to Lync Server 2013 will prevent the Response Group from accepting any incoming calls</span></span>

<span data-ttu-id="62e19-439">**Проблемах**</span><span class="sxs-lookup"><span data-stu-id="62e19-439">**Issue:**</span></span>

<span data-ttu-id="62e19-440">Если группа ответа, которая была перенесена из Lync Server 2010 в Lync Server 2013, будет удалена с Lync Server 2010 на панели управления Lync Server 2013 или в командной консоли Lync Server, группа ответа в Lync Server прекратит получать входящие звонки.</span><span class="sxs-lookup"><span data-stu-id="62e19-440">If a Response Group that has been migrated from Lync Server 2010 to Lync Server 2013 is removed from Lync Server 2010 through the Lync Server Control Panel or the Lync Server Management Shell, the Response Group in Lync Server 2013 will stop receiving any incoming calls.</span></span>

<span data-ttu-id="62e19-441">**Смысла**</span><span class="sxs-lookup"><span data-stu-id="62e19-441">**Workaround:**</span></span>

<span data-ttu-id="62e19-442">Для решения этой проблемы не удаляйте группы ответа из Lync Server 2010, которые были перенесены с Lync Server 2010 на Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="62e19-442">To work around this issue, do not remove any Response Groups from Lync Server 2010 that have been migrated from Lync Server 2010 to Lync Server 2013.</span></span>

<span data-ttu-id="62e19-443">Если группа ответа уже была удалена, вы должны повторно развернуть ее в Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="62e19-443">If the Response Group has already been removed, you should redeploy it in Lync Server 2013.</span></span>

</div>

<div>

## <a name="when-a-new-managed-workflow-is-set-to-inactive-when-created-deployment-of-the-workflow-will-fail"></a><span data-ttu-id="62e19-444">Если при создании нового управляемого рабочего процесса будет задано значение "неактивен", развертывание рабочего процесса завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="62e19-444">When a new managed workflow is set to inactive when created, deployment of the workflow will fail</span></span>

<span data-ttu-id="62e19-445">**Проблемах**</span><span class="sxs-lookup"><span data-stu-id="62e19-445">**Issue:**</span></span>

<span data-ttu-id="62e19-446">Если при создании нового управляемого рабочего процесса будет задано значение "неактивен", развертывание рабочего процесса завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="62e19-446">When a new managed workflow is set to inactive when created, deployment of the workflow will fail.</span></span> <span data-ttu-id="62e19-447">Эта проблема возникает, если во время создания рабочего процесса в рабочем процессе задано значение неактивен, но не влияет на рабочий процесс, который редактируется, чтобы сделать его неактивным после развертывания.</span><span class="sxs-lookup"><span data-stu-id="62e19-447">This issue is encountered when the workflow is set to inactive when created, but does not affect a workflow that is edited to set it to inactive after is has been deployed.</span></span>

<span data-ttu-id="62e19-448">**Смысла**</span><span class="sxs-lookup"><span data-stu-id="62e19-448">**Workaround:**</span></span>

<span data-ttu-id="62e19-449">При создании и развертывании рабочего процесса настройте рабочий процесс как активный и затем разверните его.</span><span class="sxs-lookup"><span data-stu-id="62e19-449">When creating and deploying a workflow, set the workflow as active and then deploy it.</span></span> <span data-ttu-id="62e19-450">После успешного развертывания рабочего процесса его можно изменить и установить на неактивный.</span><span class="sxs-lookup"><span data-stu-id="62e19-450">After the workflow is successfully deployed, the workflow can be edited and set to inactive.</span></span>

</div>

<div>

## <a name="removing-a-response-group-from-the-owner-pool-will-prevent-the-response-group-of-the-backup-pool-from-accepting-any-incoming-calls-during-failover-if-the-response-group-has-been-imported-to-the-backup-pool"></a><span data-ttu-id="62e19-451">Удаление группы ответа из пула владельца не позволит группе ответа в пуле резервных копий принимать входящие звонки во время отработки отказа, если группа ответа была импортирована в пул резервных копий</span><span class="sxs-lookup"><span data-stu-id="62e19-451">Removing a Response Group from the Owner pool will prevent the Response Group of the Backup pool from accepting any incoming calls during failover if the Response Group has been imported to the Backup pool</span></span>

<span data-ttu-id="62e19-452">**Проблемах**</span><span class="sxs-lookup"><span data-stu-id="62e19-452">**Issue:**</span></span>

<span data-ttu-id="62e19-453">Если группа ответа, принадлежащая основным пулам, импортирована в пул резервных копий без перезаписи владельца, а группа ответа удалена из пула владельцев, группа ответа в пуле резервных копий не будет отвечать на входящие звонки во время отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="62e19-453">If a Response Group that is owned by the primary pool has been imported to the backup pool without overwriting the owner, and the Response Group is removed from the owner pool, the Response Group in the Backup pool will not accept any incoming calls during failover.</span></span>

<span data-ttu-id="62e19-454">**Смысла**</span><span class="sxs-lookup"><span data-stu-id="62e19-454">**Workaround:**</span></span>

<span data-ttu-id="62e19-455">Вы должны повторно развернуть группу ответа в основном пуле.</span><span class="sxs-lookup"><span data-stu-id="62e19-455">You will need to redeploy the Response Group in the Primary pool.</span></span> <span data-ttu-id="62e19-456">Затем нужно будет экспортировать конфигурацию группы ответа из основного пула и снова импортировать ее в пул резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="62e19-456">You will then need to export the Response Group configuration from the Primary pool and import it to the Backup pool again.</span></span>

<span data-ttu-id="62e19-457">Вы также можете повторно создать группу ответа в пуле резервных копий.</span><span class="sxs-lookup"><span data-stu-id="62e19-457">You can also recreate the Response Group in the Backup pool.</span></span> <span data-ttu-id="62e19-458">В этом случае пул резервных копий станет пулом владельцев группы ответа.</span><span class="sxs-lookup"><span data-stu-id="62e19-458">In this case, the Backup pool will be the owner pool of the Response Group.</span></span>

</div>

<div>

## <a name="a-parked-call-cant-be-retrieved-from-the-call-park-application-if-the-retrieve-request-is-done-on-behalf-of-a-response-group"></a><span data-ttu-id="62e19-459">Припаркованный звонок не может быть получен из приложения для остановки звонка, если запрос на получение получения выполнен от имени группы ответа.</span><span class="sxs-lookup"><span data-stu-id="62e19-459">A parked call can't be retrieved from the Call Park application if the retrieve request is done on behalf of a Response Group</span></span>

<span data-ttu-id="62e19-460">**Проблемах**</span><span class="sxs-lookup"><span data-stu-id="62e19-460">**Issue:**</span></span>

<span data-ttu-id="62e19-461">Если выполняются указанные ниже условия, запрос на извлечение для приостановленного звонка завершится сбоем:</span><span class="sxs-lookup"><span data-stu-id="62e19-461">When the following conditions are true, a retrieve request for a parked call will fail:</span></span>

  - <span data-ttu-id="62e19-462">Агент входит в группу анонимных ответов.</span><span class="sxs-lookup"><span data-stu-id="62e19-462">An agent is part of an anonymous Response Group</span></span>

  - <span data-ttu-id="62e19-463">Агент пытается получить припаркованный вызов из приложения парковки на дозвонку через анонимную группу ответа.</span><span class="sxs-lookup"><span data-stu-id="62e19-463">The agent attempts to retrieve a parked call from the Call Park application through the anonymous Response Group</span></span>

  - <span data-ttu-id="62e19-464">Агент пытается получить звонок, набрав номер орбиты с помощью параметра "позвонить от имени" или с помощью того же параметра в клиенте Lync Attendant</span><span class="sxs-lookup"><span data-stu-id="62e19-464">The agent attempts to retrieve the call by dialing the orbit number through the Call On Behalf option or through the same option in the Lync attendant client</span></span>

<span data-ttu-id="62e19-465">**Смысла**</span><span class="sxs-lookup"><span data-stu-id="62e19-465">**Workaround:**</span></span>

<span data-ttu-id="62e19-466">Для этой проблемы не существует обходного пути.</span><span class="sxs-lookup"><span data-stu-id="62e19-466">There are no workarounds for this issue.</span></span> <span data-ttu-id="62e19-467">Припаркованный звонок следует извлечь, не выполняя ее от имени группы ответа.</span><span class="sxs-lookup"><span data-stu-id="62e19-467">The parked call should be retrieved without doing so on behalf of a Response Group.</span></span>

</div>

</div>

<span id="TopoBuilder"></span>

<div>

## <a name="lync-server-control-panel-topology-builder-and-planning-tool"></a><span data-ttu-id="62e19-468">Панель управления Lync Server, построитель топологий и средство планирования</span><span class="sxs-lookup"><span data-stu-id="62e19-468">Lync Server Control Panel, Topology Builder, and Planning Tool</span></span>

<div>

## <a name="planning-tool-limitations"></a><span data-ttu-id="62e19-469">Ограничения средств планирования</span><span class="sxs-lookup"><span data-stu-id="62e19-469">Planning Tool Limitations</span></span>

<div class="">


> [!NOTE]  
> <span data-ttu-id="62e19-470">Сведения, представленные в данном разделе, относятся к накопительным обновлениям для Lync Server 2013: февраль 2013 г.</span><span class="sxs-lookup"><span data-stu-id="62e19-470">The information in this section pertains to Cumulative Updates for Lync Server 2013: February 2013.</span></span>



</div>

<span data-ttu-id="62e19-471">**Проблемах**</span><span class="sxs-lookup"><span data-stu-id="62e19-471">**Issue:**</span></span>

<span data-ttu-id="62e19-472">При планировании развертывания средство планирования имеет перечисленные ниже ограничения.</span><span class="sxs-lookup"><span data-stu-id="62e19-472">The Planning Tool has the following limitations when planning for your deployment:</span></span>

  - <span data-ttu-id="62e19-473">Поддерживается не более 10 центральных сайтов</span><span class="sxs-lookup"><span data-stu-id="62e19-473">There is a maximum of 10 central sites supported</span></span>

  - <span data-ttu-id="62e19-474">Каждый центральный сайт может иметь не более 14 сайтов филиалов</span><span class="sxs-lookup"><span data-stu-id="62e19-474">Each central site can have a maximum of 14 branch sites</span></span>

  - <span data-ttu-id="62e19-475">Каждый центральный сайт может иметь не более 240 000 пользователей.</span><span class="sxs-lookup"><span data-stu-id="62e19-475">Each central site can have a maximum of 240,000 users</span></span>

<span data-ttu-id="62e19-476">Кроме того, при вычислении рекомендуемой топологии в инструменте "планирование" не включаются значения, указанные ниже.</span><span class="sxs-lookup"><span data-stu-id="62e19-476">In addition, the Planning Tool does not include values for the following when calculating the recommended topology:</span></span>

  - <span data-ttu-id="62e19-477">Количество пользователей, которые были размещены в сети</span><span class="sxs-lookup"><span data-stu-id="62e19-477">The number of users that are homed online</span></span>

  - <span data-ttu-id="62e19-478">Процент пользователей, для которых включена Федерация XMPP</span><span class="sxs-lookup"><span data-stu-id="62e19-478">The percentage of users that are enabled for XMPP federation</span></span>

  - <span data-ttu-id="62e19-479">Процент пользователей, использующих приложение Lync Web App</span><span class="sxs-lookup"><span data-stu-id="62e19-479">Percentage of users that are using Lync Web App</span></span>

<span data-ttu-id="62e19-480">**Смысла**</span><span class="sxs-lookup"><span data-stu-id="62e19-480">**Workaround:**</span></span>

<span data-ttu-id="62e19-481">Для этих проблем не существует обходного пути.</span><span class="sxs-lookup"><span data-stu-id="62e19-481">There is no workaround for these issues.</span></span> <span data-ttu-id="62e19-482">Дополнительные сведения о средстве планирования можно найти в разделе [проектирование топологии для Lync Server 2013 с помощью средства планирования](lync-server-2013-designing-the-topology-by-using-the-planning-tool.md).</span><span class="sxs-lookup"><span data-stu-id="62e19-482">For more information about the Planning Tool, see [Designing the topology for Lync Server 2013 by using the Planning Tool](lync-server-2013-designing-the-topology-by-using-the-planning-tool.md).</span></span>

</div>

<div>

## <a name="planning-tool-may-not-use-previously-defined-ip-addresses-for-the-edge-network-when-updating-options"></a><span data-ttu-id="62e19-483">Средство планирования может не использовать ранее определенные IP-адреса для пограничной сети при обновлении параметров</span><span class="sxs-lookup"><span data-stu-id="62e19-483">Planning Tool may not use previously defined IP addresses for the Edge network when updating options</span></span>

<span data-ttu-id="62e19-484">**Проблемах**</span><span class="sxs-lookup"><span data-stu-id="62e19-484">**Issue:**</span></span>

<span data-ttu-id="62e19-485">После того как вы закончите оформление с помощью средства планирования, после внесения изменений в параметры пограничной сети, вместо того, чтобы обновлять существующие IP-адреса, можно добавить в макет дополнительные IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="62e19-485">After you complete your design using the Planning Tool, if you make changes to the Edge Network options, additional IP addresses may be added to the design instead of updating the existing IP addresses.</span></span> <span data-ttu-id="62e19-486">Это может произойти, если вы просматриваете сведения о схеме пограничного сетевого файла, выбираете **ссылку Щелкните здесь, чтобы обновить параметры**, а затем в диалоговом окне Параметры конфигурации Выбери подходящие **полные доменные имена и IP-адреса, но разные порты для служб EDGE на пограничном сервере**.</span><span class="sxs-lookup"><span data-stu-id="62e19-486">This can occur when you are viewing the details of the Edge Network Diagram, select **Click here to update your options**, and then, on the Configuration Options dialog, you select Edge Network select **I want to use the same FQDNs and IP addresses, but different ports for the edge services on my Edge Server**.</span></span> <span data-ttu-id="62e19-487">Применение изменений может привести к тому, что новые IP-адреса и пограничные серверы будут добавлены в проект.</span><span class="sxs-lookup"><span data-stu-id="62e19-487">Applying any changes may result in new IP addresses and Edge servers being added to the design.</span></span>

<span data-ttu-id="62e19-488">**Смысла**</span><span class="sxs-lookup"><span data-stu-id="62e19-488">**Workaround:**</span></span>

<span data-ttu-id="62e19-489">В настоящее время решения этой проблемы не существует.</span><span class="sxs-lookup"><span data-stu-id="62e19-489">There is no workaround for this issue at this time.</span></span>

</div>

<div>

## <a name="in-lync-server-control-panel-move-all-users-to-pool-may-not-work-as-expected"></a><span data-ttu-id="62e19-490">На панели управления Lync Server "перемещение всех пользователей в пул" может не работать должным образом</span><span class="sxs-lookup"><span data-stu-id="62e19-490">In Lync Server Control Panel, "Move all users to pool" may not work as expected</span></span>

<span data-ttu-id="62e19-491">**Проблемах**</span><span class="sxs-lookup"><span data-stu-id="62e19-491">**Issue:**</span></span>

<span data-ttu-id="62e19-492">При использовании панели управления Lync Server для перемещения всех пользователей из одной группы в другую в сложной среде Active Directory, например с несколькими контроллерами домена и родительскими и дочерними доменами, может быть возвращено сообщение об ошибке: "указанный пользователь не является устаревшим пользователем, вместо него используется Move-CsUser командлет".</span><span class="sxs-lookup"><span data-stu-id="62e19-492">When using the Lync Server Control Panel to move all users from one pool to another pool in a complex Active Directory environment, such as one with multiple Domain Controllers and parent/child domains, an error message may be returned that states, “Specified user is not a legacy user, use Move-CsUser cmdlet instead.”</span></span> <span data-ttu-id="62e19-493">Это является результатом продолжительных операций репликации в сложных средах Active Directory.</span><span class="sxs-lookup"><span data-stu-id="62e19-493">This is a result of longer replication times in complex Active Directory environments.</span></span>

<span data-ttu-id="62e19-494">**Смысла**</span><span class="sxs-lookup"><span data-stu-id="62e19-494">**Workaround:**</span></span>

<span data-ttu-id="62e19-495">Чтобы устранить эту ошибку, выполните одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="62e19-495">To work around this issue, do one of the following:</span></span>

  - <span data-ttu-id="62e19-496">Использование фильтров на панели управления Lync Server для поиска устаревших пользователей, выбор пользователей и использование **команды переместить выбранных пользователей в группу** вместо **перемещения всех пользователей в пул**.</span><span class="sxs-lookup"><span data-stu-id="62e19-496">Use filters in the Lync Server Control Panel to search for legacy users, select those users, and then use the **Move selected users to pool command** instead of **Move all users to pool**.</span></span>

  - <span data-ttu-id="62e19-497">Используйте командную консоль Lync Server для перемещения пользователей из прежних версий в пакеты с помощью командлетов Lync Server.</span><span class="sxs-lookup"><span data-stu-id="62e19-497">Use the Lync Server Management Shell to move legacy users in batches by using Lync Server cmdlets.</span></span>

</div>

<div>

## <a name="the-lync-server-control-panel-stops-working-in-a-vmware-environment-after-the-microsoft-silverlight-browser-plug-in-is-updated-to-version-5"></a><span data-ttu-id="62e19-498">После обновления подключаемого модуля Microsoft Silverlight для браузера до версии 5 панель управления Lync Server перестает работать в среде VMware.</span><span class="sxs-lookup"><span data-stu-id="62e19-498">The Lync Server Control Panel stops working in a VMware environment after the Microsoft Silverlight browser plug-in is updated to version 5</span></span>

<span data-ttu-id="62e19-499">**Проблемах**</span><span class="sxs-lookup"><span data-stu-id="62e19-499">**Issue:**</span></span>

<span data-ttu-id="62e19-500">Если вы используете панель управления Lync Server в среде VMware, то после обновления Silverlight до версии 5 панель управления Lync Server может перестать работать.</span><span class="sxs-lookup"><span data-stu-id="62e19-500">If you use the Lync Server Control Panel in a VMware environment, the Lync Server Control Panel may stop working after you upgrade Silverlight to version 5.</span></span>

<span data-ttu-id="62e19-501">**Смысла**</span><span class="sxs-lookup"><span data-stu-id="62e19-501">**Workaround:**</span></span>

<span data-ttu-id="62e19-502">Чтобы устранить эту ошибку, выполните одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="62e19-502">To work around this issue, do one of the following:</span></span>

  - <span data-ttu-id="62e19-503">Удалите Silverlight 5, а затем установите Silverlight 4 [https://go.microsoft.com/fwlink/p/?LinkID=149156\&v=4.0](https://go.microsoft.com/fwlink/p/?linkid=149156%26v=4.0) .</span><span class="sxs-lookup"><span data-stu-id="62e19-503">Uninstall Silverlight 5, and then install Silverlight 4 from [https://go.microsoft.com/fwlink/p/?LinkID=149156\&v=4.0](https://go.microsoft.com/fwlink/p/?linkid=149156%26v=4.0).</span></span>

  - <span data-ttu-id="62e19-504">Откройте панель управления Lync Server на компьютере, который не является виртуальным компьютером VMware.</span><span class="sxs-lookup"><span data-stu-id="62e19-504">Open the Lync Server Control Panel from a computer that is not a VMware virtual computer.</span></span>
    
    <span data-ttu-id="62e19-505">Чтобы открыть панель управления Lync Server на удаленном компьютере, установите на нем средства администрирования Lync Server и откройте панель управления Lync Server в меню " **Пуск** " Windows.</span><span class="sxs-lookup"><span data-stu-id="62e19-505">To open the Lync Server Control Panel from a remote computer, install Lync Server Administration tools on the computer, and then start the Lync Server Control Panel from the Windows **Start** menu.</span></span>
    
    <span data-ttu-id="62e19-506">Вы также можете открыть панель управления Lync Server, введя URL-адрес в браузере.</span><span class="sxs-lookup"><span data-stu-id="62e19-506">You can also open the Lync Server Control Panel by entering the URL in a web browser.</span></span> <span data-ttu-id="62e19-507">URL-адрес будет похож на https:// \<frontend\_pool\_fqdn\> /cscp.</span><span class="sxs-lookup"><span data-stu-id="62e19-507">The URL will be similar to https://\<frontend\_pool\_fqdn\>/cscp.</span></span>

</div>

<div>

## <a name="an-administrator-cannot-run-the-uninstall-csmirrordb-cmdlet-after-removing-the-mirroring-database-in-topology-builder"></a><span data-ttu-id="62e19-508">Администратор не может запустить командлет Uninstall-csMirrorDB после удаления зеркальной базы данных в построителе топологии</span><span class="sxs-lookup"><span data-stu-id="62e19-508">An administrator cannot run the Uninstall-csMirrorDB cmdlet after removing the mirroring database in Topology Builder</span></span>

<span data-ttu-id="62e19-509">**Проблемах**</span><span class="sxs-lookup"><span data-stu-id="62e19-509">**Issue:**</span></span>

<span data-ttu-id="62e19-510">Если администратор отключает зеркальную базу данных в построителе топологии, а затем удаляет зеркальную базу данных в построителе топологии, в списке дел появляется сообщение о том, что для удаления зеркального отображения с сервера SQL Server необходимо, чтобы администратор выпустил командлет **uninstall-csMirrorDatabase** .</span><span class="sxs-lookup"><span data-stu-id="62e19-510">When an administrator disables a mirroring database in Topology Builder, and then deletes the mirroring database in Topology Builder, a message is displayed in the To do list for the administrator to run the **Uninstall-csMirrorDatabase** cmdlet to remove mirroring from SQL Server.</span></span> <span data-ttu-id="62e19-511">При попытке администратора выполнить командлет происходит сбой.</span><span class="sxs-lookup"><span data-stu-id="62e19-511">When the administrator attempts to run the cmdlet, it fails.</span></span>

<span data-ttu-id="62e19-512">**Смысла**</span><span class="sxs-lookup"><span data-stu-id="62e19-512">**Workaround:**</span></span>

<span data-ttu-id="62e19-513">Для удаления зеркального отображения SQL пула в построителе топологии необходимо сначала использовать командлет для удаления зеркала в SQL Server.</span><span class="sxs-lookup"><span data-stu-id="62e19-513">To remove SQL mirroring of a pool in Topology Builder, you must first use a cmdlet to remove the mirror in SQL Server.</span></span> <span data-ttu-id="62e19-514">Затем вы можете использовать построитель топологий, чтобы удалить зеркало из топологии.</span><span class="sxs-lookup"><span data-stu-id="62e19-514">You can then use Topology Builder to remove the mirror from the topology.</span></span> <span data-ttu-id="62e19-515">Чтобы сделать это в SQL Server, запустите следующий командлет:</span><span class="sxs-lookup"><span data-stu-id="62e19-515">To remove the mirror in SQL Server, use the following cmdlet:</span></span>

    Uninstall-CsMirrorDatabase -SqlServerFqdn <SQLServer FQDN> [-SqlInstanceName <SQLServer instance name>] -DatabaseType <Application | Archiving | CentralMgmt | Monitoring | User | BIStaging | PersistentChat | PersistentChatCompliance> [-DropExistingDatabasesOnMirror] [-Verbose]

<span data-ttu-id="62e19-516">Например, чтобы удалить зеркальное отображение и удалить базы данных пользователей, введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="62e19-516">For example, to remove mirroring and drop the databases for the user databases, type the following:</span></span>

    Uninstall-CsMirrorDatabase -SqlServerFqdn primaryBE.contoso.com -SqlInstanceName rtc -Verbose -DatabaseType User -DropExistingDatabasesOnMirror

<span data-ttu-id="62e19-517">Параметр *DropExistingDatabasesOnMirror* приводит к удалению затронутых баз данных из зеркала.</span><span class="sxs-lookup"><span data-stu-id="62e19-517">The *DropExistingDatabasesOnMirror* parameter causes the affected databases to be deleted from the mirror.</span></span> <span data-ttu-id="62e19-518">Чтобы затем удалить это зеркальное отображение из топологии, выполните одно из следующих действий:</span><span class="sxs-lookup"><span data-stu-id="62e19-518">Then, to remove the mirror from the topology, do the following:</span></span>

1.  <span data-ttu-id="62e19-519">В построителе топологии щелкните пул правой кнопкой мыши и выберите пункт **Изменить свойства**.</span><span class="sxs-lookup"><span data-stu-id="62e19-519">In Topology Builder, right-click the pool and click **Edit Properties**.</span></span>

2.  <span data-ttu-id="62e19-520">Снимите флажок **включить зеркальное отображение хранилища SQL** и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="62e19-520">Clear **Enable SQL Store Mirroring** and click **OK**.</span></span>

3.  <span data-ttu-id="62e19-521">Опубликуйте топологию.</span><span class="sxs-lookup"><span data-stu-id="62e19-521">Publish the topology.</span></span>

<div class="">


> [!IMPORTANT]  
> <span data-ttu-id="62e19-522">Каждый раз, когда вы вносите изменения в отношение зеркального отображения базы данных, необходимо перезапустить все серверы переднего плана в пуле.</span><span class="sxs-lookup"><span data-stu-id="62e19-522">Whenever you make a change to a back-end database mirroring relationship, you must restart all the Front End Servers in the pool.</span></span>



</div>

</div>

<div>

## <a name="validation-errors-are-returned-in-topology-builder-when-an-administrator-attempts-to-remove-a-deployment-with-a-front-end-pool-that-has-an-associated-witness-store"></a><span data-ttu-id="62e19-523">Ошибки проверки возвращены в построителе топологии при попытке администратора удалить развертывание с пулом переднего плана, на котором есть связанный с ним Банк-свидетель</span><span class="sxs-lookup"><span data-stu-id="62e19-523">Validation errors are returned in Topology Builder when an administrator attempts to remove a deployment with a Front End pool that has an associated witness store</span></span>

<span data-ttu-id="62e19-524">**Проблемах**</span><span class="sxs-lookup"><span data-stu-id="62e19-524">**Issue:**</span></span>

<span data-ttu-id="62e19-525">Если администратор попытается использовать команду **удалить развертывание** в построителе топологии для удаления развертывания, включающего пул переднего плана с соответствующим хранилищем следящего сервера, в построителе топологии появится ошибка проверки подлинности, и действие не будет продолжено.</span><span class="sxs-lookup"><span data-stu-id="62e19-525">If an administrator attempts to use the **Remove Deployment** command in Topology Builder to remove a deployment that includes a Front End pool with an associated witness store, a validation error is displayed in Topology Builder and the action will not proceed.</span></span>

<span data-ttu-id="62e19-526">**Смысла**</span><span class="sxs-lookup"><span data-stu-id="62e19-526">**Workaround:**</span></span>

<span data-ttu-id="62e19-527">Чтобы устранить эту ошибку, выполните одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="62e19-527">To work around this issue, do one of the following:</span></span>

  - <span data-ttu-id="62e19-528">Удалите хранилище следящего сервера, прежде чем пытаться удалить развертывание.</span><span class="sxs-lookup"><span data-stu-id="62e19-528">Remove the witness store before attempting to remove the deployment.</span></span>

  - <span data-ttu-id="62e19-529">Добавьте хранилище следящего сервера для пула переднего плана и удалите его.</span><span class="sxs-lookup"><span data-stu-id="62e19-529">Add a witness store for the Front End pool and then remove it.</span></span>

</div>

<div>

## <a name="persistent-chat-server-deployment-information-is-inconsistent-between-the-planning-tool-and-topology-builder"></a><span data-ttu-id="62e19-530">Сведения о развертывании сервера сохраняемого чата в средстве планирования и Topology Builder не совпадают</span><span class="sxs-lookup"><span data-stu-id="62e19-530">Persistent Chat Server deployment information is inconsistent between the Planning Tool and Topology Builder</span></span>

<span data-ttu-id="62e19-531">**Проблемах**</span><span class="sxs-lookup"><span data-stu-id="62e19-531">**Issue:**</span></span>

<span data-ttu-id="62e19-532">Когда Lync Server 2013, средство планирования выводит схему топологии сайта для развертывания сервера для постоянного чата, если включена возможность аварийного восстановления, схема топологии сайта включает несколько (физических) сайтов, в том числе на каждом сайте с одинаковым набором постоянных серверов чата.</span><span class="sxs-lookup"><span data-stu-id="62e19-532">When the Lync Server 2013, Planning Tool outputs the site topology diagram for a Persistent Chat Server deployment with disaster recovery enabled, the site topology diagram includes multiple (physical) sites, with evenly assigned Persistent Chat Servers at each site.</span></span> <span data-ttu-id="62e19-533">В построителе топологии все сохраняемые серверы чата представлены как относящиеся к одному (логическому) сайту и указаны в том же узле пула серверов сохраняемого чата.</span><span class="sxs-lookup"><span data-stu-id="62e19-533">In Topology Builder, all Persistent Chat Servers are represented as belonging to a single (logical) site, and are listed under the same Persistent Chat Server pool node.</span></span>

<span data-ttu-id="62e19-534">**Смысла**</span><span class="sxs-lookup"><span data-stu-id="62e19-534">**Workaround:**</span></span>

<span data-ttu-id="62e19-535">В настоящее время для этой проблемы не существует обходного пути.</span><span class="sxs-lookup"><span data-stu-id="62e19-535">Currently, we do not have a workaround for this issue.</span></span> <span data-ttu-id="62e19-536">Пользователь должен проанализировать выходные данные средства планирования для развертывания сервера сохраняемого чата, а также изменить план в соответствии с конкретными потребностями.</span><span class="sxs-lookup"><span data-stu-id="62e19-536">The user should analyze the output of the Planning Tool for the Persistent Chat Server deployment, and modify the plan to meet their specific needs.</span></span>

</div>

</div>

<span id="Localization"></span>

<div>

## <a name="localization"></a><span data-ttu-id="62e19-537">Локализации</span><span class="sxs-lookup"><span data-stu-id="62e19-537">Localization</span></span>

<div>

## <a name="monitoring"></a><span data-ttu-id="62e19-538">Мониторинг</span><span class="sxs-lookup"><span data-stu-id="62e19-538">Monitoring</span></span>

<div>

## <a name="the-deploy-monitoring-reports-wizard-displays-incorrect-characters-under-certain-circumstances-when-using-the-east-asian-version-of-lync-server"></a><span data-ttu-id="62e19-539">При использовании восточно-азиатской версии Lync Server мастер развертывания отчетов мониторинга отображает неверные символы при определенных обстоятельствах</span><span class="sxs-lookup"><span data-stu-id="62e19-539">The Deploy Monitoring Reports wizard displays incorrect characters under certain circumstances when using the East Asian version of Lync Server</span></span>

<span data-ttu-id="62e19-540">**Проблемах**</span><span class="sxs-lookup"><span data-stu-id="62e19-540">**Issue:**</span></span>

<span data-ttu-id="62e19-541">При использовании восточноазиатских версий Lync Server 2013 (например, китайский (упрощенное письмо), китайский (традиционное письмо), японский или корейский — в операционной системе, в которой язык системы не настроен на использование восточноазиатских языков, в мастере развертывания отчетов мониторинга отображаются вопросительные знаки и другие символы вместо локализованных сообщений.</span><span class="sxs-lookup"><span data-stu-id="62e19-541">When using an East Asian version of Lync Server 2013—for example, Chinese (Simplified), Chinese (Traditional), Japanese, or Korean—on an operating system that has the system locale not set to an East Asian language, the Deploy Monitoring Reports wizard will display question marks or other characters instead of localized messages.</span></span>

<span data-ttu-id="62e19-542">**Смысла**</span><span class="sxs-lookup"><span data-stu-id="62e19-542">**Workaround:**</span></span>

<span data-ttu-id="62e19-543">Чтобы устранить эту ошибку, настройте языковой стандарт для операционной системы и Lync Server 2013 на тот же язык, после чего будут правильно отображены все сообщения.</span><span class="sxs-lookup"><span data-stu-id="62e19-543">To correct this issue, set the locale for the operating system and Lync Server 2013 to the same language, which will display all messages correctly.</span></span>

</div>

</div>

<div>

## <a name="lync-server-control-panel"></a><span data-ttu-id="62e19-544">Панель управления Lync Server</span><span class="sxs-lookup"><span data-stu-id="62e19-544">Lync Server Control Panel</span></span>

<div>

## <a name="in-certain-cases-the-first-item-in-the-top-navigation-bar-on-a-page-of-lync-server-control-panel-disappears-when-the-last-item-in-the-top-navigation-bar-is-clicked"></a><span data-ttu-id="62e19-545">В некоторых случаях первый элемент верхней панели навигации на странице панели управления Lync Server исчезает, когда вы щелкните последний элемент на верхней панели навигации.</span><span class="sxs-lookup"><span data-stu-id="62e19-545">In certain cases, the first item in the top navigation bar on a page of Lync Server Control Panel disappears when the last item in the top navigation bar is clicked</span></span>

<span data-ttu-id="62e19-546">**Проблемах**</span><span class="sxs-lookup"><span data-stu-id="62e19-546">**Issue:**</span></span>

<span data-ttu-id="62e19-547">В большинстве случаев, когда щелчок последнего элемента на верхней панели навигации на странице сервера Lync Server приводит к исчезновению первого элемента в верхней панели навигации:</span><span class="sxs-lookup"><span data-stu-id="62e19-547">There are three known cases where clicking the last item in the top navigation bar on a page of the Lync Server Control Panel will cause the first item in the top navigation bar to disappear:</span></span>

  - <span data-ttu-id="62e19-548">На французском языке на странице "Féderation et Accès extern" элемент "stratégie d'accès extern" исчезнет после нажатия кнопки "Partenaires fédérés XMPP".</span><span class="sxs-lookup"><span data-stu-id="62e19-548">In the French of version, on the page "Féderation et accès externe," the item "Stratégie d'accès externe" will disappear when "Partenaires fédérés XMPP" is clicked.</span></span>

  - <span data-ttu-id="62e19-549">В немецкой версии на странице "клиенты" элемент "Clientversionskonfiguration" исчезает при нажатии кнопки "Pushbenachrichtigungskonfiguration".</span><span class="sxs-lookup"><span data-stu-id="62e19-549">In the German version, on the "Clients" page, the item "Clientversionskonfiguration" disappears when "Pushbenachrichtigungskonfiguration" is clicked.</span></span>

  - <span data-ttu-id="62e19-550">В русской версии на странице "Конфигурация сети" элемент "глобально" исчезает при нажатии кнопки "маршрут региона".</span><span class="sxs-lookup"><span data-stu-id="62e19-550">In the Russian version, on "Конфигурация сети" page, the item "Глобально" disappears when "Маршрут региона" is clicked.</span></span>

<span data-ttu-id="62e19-551">**Смысла**</span><span class="sxs-lookup"><span data-stu-id="62e19-551">**Workaround:**</span></span>

<span data-ttu-id="62e19-552">Чтобы устранить эту ошибку, обновите страницу панели управления Lync Server в браузере.</span><span class="sxs-lookup"><span data-stu-id="62e19-552">To work around this issue, refresh the page of the Lync Server Control Panel in your browser.</span></span> <span data-ttu-id="62e19-553">Страница будет загружена в браузере, где все элементы верхней панели навигации будут отображены.</span><span class="sxs-lookup"><span data-stu-id="62e19-553">The page will load in the browser with all of the items in the top navigation bar displayed.</span></span>

</div>

</div>

<div>

## <a name="address-book"></a><span data-ttu-id="62e19-554">Адресная книга</span><span class="sxs-lookup"><span data-stu-id="62e19-554">Address Book</span></span>

<div>

## <a name="indexing-in-the-address-book-does-not-work-as-expected-in-some-languages"></a><span data-ttu-id="62e19-555">Индексирование в адресной книге не работает должным образом в некоторых языках</span><span class="sxs-lookup"><span data-stu-id="62e19-555">Indexing in the Address Book does not work as expected in some languages</span></span>

<div class="">


> [!NOTE]  
> <span data-ttu-id="62e19-556">Сведения, представленные в данном разделе, относятся к накопительным обновлениям для Lync Server 2013: февраль 2013 г.</span><span class="sxs-lookup"><span data-stu-id="62e19-556">The information in this section pertains to Cumulative Updates for Lync Server 2013: February 2013.</span></span>



</div>

<span data-ttu-id="62e19-557">Если в свойствах пользователя содержится индексированное поле, а в поле содержатся только те символы, которые не могут быть проиндексированы, пользователь не будет отображаться в области поиска, выполненной в адресной книге.</span><span class="sxs-lookup"><span data-stu-id="62e19-557">If a user’s properties contain an indexed field, and that field contains only characters that cannot be indexed, then the user will not appear in searches performed in the Address Book.</span></span>

<span data-ttu-id="62e19-558">Следующие символы и языковые стандарты не подлежат индексированию:</span><span class="sxs-lookup"><span data-stu-id="62e19-558">The following characters and locales cannot be indexed:</span></span>

  - <span data-ttu-id="62e19-559">Прописные, греческие и армянские символы в верхнем регистре</span><span class="sxs-lookup"><span data-stu-id="62e19-559">Upper-case Cyrillic, Greek, and Armenian characters</span></span>

  - <span data-ttu-id="62e19-560">Прописные с надстрочными знаками</span><span class="sxs-lookup"><span data-stu-id="62e19-560">Upper-case accented characters</span></span>

  - <span data-ttu-id="62e19-561">тайский</span><span class="sxs-lookup"><span data-stu-id="62e19-561">Thai</span></span>

  - <span data-ttu-id="62e19-562">Лаос</span><span class="sxs-lookup"><span data-stu-id="62e19-562">Lao</span></span>

  - <span data-ttu-id="62e19-563">Мьянма</span><span class="sxs-lookup"><span data-stu-id="62e19-563">Myanmar</span></span>

  - <span data-ttu-id="62e19-564">Деванагари</span><span class="sxs-lookup"><span data-stu-id="62e19-564">Devanagari</span></span>

  - <span data-ttu-id="62e19-565">Эфиопский</span><span class="sxs-lookup"><span data-stu-id="62e19-565">Ethiopic</span></span>

  - <span data-ttu-id="62e19-566">Тибетский</span><span class="sxs-lookup"><span data-stu-id="62e19-566">Tibetan</span></span>

  - <span data-ttu-id="62e19-567">бенгальский</span><span class="sxs-lookup"><span data-stu-id="62e19-567">Bengali</span></span>

  - <span data-ttu-id="62e19-568">гуджарати</span><span class="sxs-lookup"><span data-stu-id="62e19-568">Gujarati</span></span>

  - <span data-ttu-id="62e19-569">телугу</span><span class="sxs-lookup"><span data-stu-id="62e19-569">Telugu</span></span>

  - <span data-ttu-id="62e19-570">Все другие индийские наборы знаков</span><span class="sxs-lookup"><span data-stu-id="62e19-570">All other Indic scripts</span></span>

</div>

</div>

<div>

## <a name="lync-web-app-web-scheduler-and-web-components"></a><span data-ttu-id="62e19-571">Lync Web App, веб-планировщик и веб-компоненты</span><span class="sxs-lookup"><span data-stu-id="62e19-571">Lync Web App, Web Scheduler, and Web components</span></span>

<div>

## <a name="language-fallback-for-certain-languages-in-lync-web-scheduler-dial-in-join-launcher-persistent-chat-room-management-and-octab-might-not-work-as-expected"></a><span data-ttu-id="62e19-572">Резервные языковые параметры для некоторых языков в веб-планировщике Lync, подключение к Интернету, средство запуска присоединения к сети, управление комнатой чата и OCTab могут не работать должным образом</span><span class="sxs-lookup"><span data-stu-id="62e19-572">Language fallback for certain languages in Lync Web Scheduler, Dial-In, Join Launcher, Persistent Chat Room Management, and OCTab might not work as expected</span></span>

<span data-ttu-id="62e19-573">**Проблемах**</span><span class="sxs-lookup"><span data-stu-id="62e19-573">**Issue:**</span></span>

<span data-ttu-id="62e19-574">При выборе нейтрального языкового стандарта в веб-браузере (в Internet Explorer) например, имя языка без дополнительных спецификаций, например "Норвежский \[ номер \] "), а не языковой стандарт, задающий язык, сценарий и языковой стандарт (например, "Норвежский, букмол (Норвегия) \[ -нет \] ") может привести к неожиданному поведению отображения для некоторых языков в веб</span><span class="sxs-lookup"><span data-stu-id="62e19-574">When selecting a neutral locale in a web browser (in Internet Explorer, for example, the language name without further specification, like "Norwegian \[no\]") instead of a locale specifying language, script and locale (such as "Norwegian, Bokmål (Norway) \[nb-NO\]") might lead to unexpected display behavior for certain languages in Lync Web Scheduler, Dial-In, Join Launcher, Persistent Chat Room Management, and OCTab.</span></span> <span data-ttu-id="62e19-575">Например, пользователи могут видеть страницу на английском языке, если выбран один из указанных ниже языков.</span><span class="sxs-lookup"><span data-stu-id="62e19-575">For example, users might see the English page when one of the following languages is selected:</span></span>

  - <span data-ttu-id="62e19-576">норвежский</span><span class="sxs-lookup"><span data-stu-id="62e19-576">Norwegian</span></span>

  - <span data-ttu-id="62e19-577">Португальский</span><span class="sxs-lookup"><span data-stu-id="62e19-577">Portuguese</span></span>

  - <span data-ttu-id="62e19-578">сербский</span><span class="sxs-lookup"><span data-stu-id="62e19-578">Serbian</span></span>

<span data-ttu-id="62e19-579">**Смысла**</span><span class="sxs-lookup"><span data-stu-id="62e19-579">**Workaround:**</span></span>

<span data-ttu-id="62e19-580">Если вы хотите выбрать язык со нейтральным региональным стандартом, всегда убедитесь, что вы также добавляете язык с определенным языковым стандартом (с использованием сценария и/или кода страны) в качестве дополнительного языка в списке языковых параметров вашего браузера.</span><span class="sxs-lookup"><span data-stu-id="62e19-580">If you want to select a language with a neutral locale, always make sure that you also add the language with a specific locale (with script and/or country code) as an additional language in your browser's language preference list.</span></span>

</div>

<div>

## <a name="there-is-limited-support-for-azeri-and-uzbek-locales-when-using-lync-web-scheduler-dial-in-join-launcher-persistent-chat-room-management-and-octab-in-some-web-browsers"></a><span data-ttu-id="62e19-581">Ограниченная поддержка национальных настроек азербайджанский и узбекский при использовании веб-планировщика Lync, подключение к сети, средство запуска присоединения к Интернету, управление комнатой чата и OCTab в некоторых веб-браузерах</span><span class="sxs-lookup"><span data-stu-id="62e19-581">There is limited support for Azeri and Uzbek locales when using Lync Web Scheduler, Dial-In, Join Launcher, Persistent Chat Room Management, and OCTab in some web browsers</span></span>

<div class="">


> [!NOTE]  
> <span data-ttu-id="62e19-582">Сведения, представленные в данном разделе, относятся к накопительным обновлениям для Lync Server 2013: февраль 2013 г.</span><span class="sxs-lookup"><span data-stu-id="62e19-582">The information in this section pertains to Cumulative Updates for Lync Server 2013: February 2013.</span></span>



</div>

<span data-ttu-id="62e19-583">**Проблемах**</span><span class="sxs-lookup"><span data-stu-id="62e19-583">**Issue:**</span></span>

<span data-ttu-id="62e19-584">Если вы используете Internet Explorer 8 или Internet Explorer 9 и устанавливаете для языка браузера значение Азербайджанский (латиница) или узбекский (латиница), страницы средства запуска для подключения к Интернету и присоединения будут отображаться на английском языке или на предпочтительном языке, выбранном в браузере.</span><span class="sxs-lookup"><span data-stu-id="62e19-584">When you use Internet Explorer 8 or Internet Explorer 9, and set the browser language to Azeri (Latin) or Uzbek (Latin), the Dial-in and Join Launcher pages will be displayed in English or the preferred language set in the browser.</span></span>

<span data-ttu-id="62e19-585">При использовании браузеров Firefox или Chrome и настройке языка браузера на азербайджанский (латиница) или узбекский (латиница), веб-приложение Lync Web App, веб-планировщик Lync и RGS OCTab будут отображаться на английском языке или на предпочтительном языке, установленном для браузера.</span><span class="sxs-lookup"><span data-stu-id="62e19-585">When you use Firefox or Chrome browsers, and you set the browser language to Azeri (Latin) or Uzbek (Latin), the Lync Web App, Lync Web Scheduler, and RGS OCTab will be shown in English or the preferred language set for the browser.</span></span>

<span data-ttu-id="62e19-586">Язык "узбекский (латиница)" не поддерживается в браузере Safari.</span><span class="sxs-lookup"><span data-stu-id="62e19-586">The Uzbek (Latin) locale is not supported in the Safari browser.</span></span>

<span data-ttu-id="62e19-587">**Смысла**</span><span class="sxs-lookup"><span data-stu-id="62e19-587">**Workaround:**</span></span>

<span data-ttu-id="62e19-588">Для этих проблем не существует обходного пути.</span><span class="sxs-lookup"><span data-stu-id="62e19-588">There is not workaround for these issues.</span></span>

</div>

</div>

<div>

## <a name="the-drop-down-arrow-is-missing-for-join-meeting-from-list-in-the-romanian-version-of-lync-web-app"></a><span data-ttu-id="62e19-589">Отсутствует стрелка раскрывающегося списка "присоединиться к собранию из" в румынского версии Lync Web App</span><span class="sxs-lookup"><span data-stu-id="62e19-589">The drop-down arrow is missing for "Join meeting from" list in the Romanian version of Lync Web App</span></span>

<span data-ttu-id="62e19-590">**Проблемах**</span><span class="sxs-lookup"><span data-stu-id="62e19-590">**Issue:**</span></span>

<span data-ttu-id="62e19-591">Если пользователь, использующий версию Lync Web App, выполняет описанные ниже действия, в раскрывающемся списке **присоединиться к собранию** не отображается стрелка раскрывающегося списка.</span><span class="sxs-lookup"><span data-stu-id="62e19-591">When a user who is using the Romanian version of Lync Web App performs the following steps, the drop-down arrow is not displayed for **Join meeting** in drop-down list:</span></span>

1.  <span data-ttu-id="62e19-592">На вкладке **Общие** установите флажок **Запомнить меня на этом компьютере** .</span><span class="sxs-lookup"><span data-stu-id="62e19-592">Select **Remember me on this computer** on the **General** tab.</span></span>

2.  <span data-ttu-id="62e19-593">Откройте вкладку **Телефон** .</span><span class="sxs-lookup"><span data-stu-id="62e19-593">Select the **Phone** tab.</span></span>

3.  <span data-ttu-id="62e19-594">Щелкните раскрывающийся список **присоединиться к собранию**.</span><span class="sxs-lookup"><span data-stu-id="62e19-594">Click the drop-down list for **Join meeting from**.</span></span>
    
    <span data-ttu-id="62e19-595">Пользователи не увидят стрелки, указывающей на то, что в **Lync Web App** есть больше параметров, которые включают: **не присоединять звук** (в румынская, "ню SE asociaža La компонент) и **новый номер**" (на румынского, "Număr Nou").</span><span class="sxs-lookup"><span data-stu-id="62e19-595">Users will not see an arrow that indicates that there are more options than the default **Lync Web App**, which include: **Don't join audio** (in Romanian, "Nu se asociaža la componenta audio") and **New number**" (in Romanian, "Număr nou").</span></span>

<span data-ttu-id="62e19-596">**Смысла**</span><span class="sxs-lookup"><span data-stu-id="62e19-596">**Workaround:**</span></span>

<span data-ttu-id="62e19-597">Несмотря на то, что стрелка для этого раскрывающегося списка не отображается, пользователи могут по-прежнему выбирать дополнительные параметры в списке, щелкая значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="62e19-597">Even though the arrow for this drop-down list is not displayed, users can still select the additional settings in the list by clicking on the default value.</span></span>

</div>

<div>

## <a name="when-using-the-turkish-version-of-lync-web-scheduler-a-meeting-cannot-be-saved-when-using-the-people-i-choose-option-under-who-is-a-presenter"></a><span data-ttu-id="62e19-598">При использовании турецкой версии веб-планировщика Lync не удается сохранить собрание при использовании параметра "люди, выбранные" в разделе "кто является выступающим"</span><span class="sxs-lookup"><span data-stu-id="62e19-598">When using the Turkish version of Lync Web Scheduler, a meeting cannot be saved when using the "People I choose" option under "Who is a presenter"</span></span>

<span data-ttu-id="62e19-599">**Проблемах**</span><span class="sxs-lookup"><span data-stu-id="62e19-599">**Issue:**</span></span>

<span data-ttu-id="62e19-600">При создании и редактировании собрания в турецком варианте веб-планировщика Lync параметр "люди, выбранные пользователем" в разделе "кто является выступающим" не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="62e19-600">When creating or editing a meeting in the Turkish version of the Lync Web Scheduler, the option "People I choose" under "Who is a presenter" is not supported.</span></span> <span data-ttu-id="62e19-601">Если выбран этот параметр, собрание невозможно сохранить.</span><span class="sxs-lookup"><span data-stu-id="62e19-601">When this option is selected, the meeting can't be saved.</span></span> <span data-ttu-id="62e19-602">Вместо этого появляется сообщение об ошибке, указывающее на то, что один или несколько пользователей нельзя сделать выступающими.</span><span class="sxs-lookup"><span data-stu-id="62e19-602">Instead, an error message appears, indicating that one or more people cannot be made presenters.</span></span>

<span data-ttu-id="62e19-603">**Смысла**</span><span class="sxs-lookup"><span data-stu-id="62e19-603">**Workaround:**</span></span>

<span data-ttu-id="62e19-604">Для решения этой проблемы пользователи могут использовать параметр по умолчанию "люди из моей организации" или любой другой вариант, например "только организатор" или "все, включая пользователей за пределами моей компании".</span><span class="sxs-lookup"><span data-stu-id="62e19-604">To work around this issue, users can use the default option of "People from my company," or any other choice, such as "Only Organizer" or "Everyone including people outside of my company."</span></span> <span data-ttu-id="62e19-605">После того как вы присоединяется к собранию, организатор может понизить или переместить людей на их правильную роль.</span><span class="sxs-lookup"><span data-stu-id="62e19-605">The organizer can demote or promote people to their correct roles later, after they have joined the meeting.</span></span>

<span data-ttu-id="62e19-606">Кроме того, пользователи, знакомые с другим языком, могут изменить язык, выбранный в браузере, на один из языков, поддерживаемых 43, и попытаться использовать параметр "люди, которые вы выбираете".</span><span class="sxs-lookup"><span data-stu-id="62e19-606">Alternatively, users who understand another language can change the language selection in their browser to one of the other 43 supported languages and attempt to use the “People I choose” option.</span></span>

</div>

</div>

<span id="Copyright"></span>

<div>

## <a name="copyright"></a><span data-ttu-id="62e19-607">1996</span><span class="sxs-lookup"><span data-stu-id="62e19-607">Copyright</span></span>

<span data-ttu-id="62e19-608">Этот документ поддерживает предварительную версию программного продукта, который может быть изменен перед окончательным коммерческой выпуском, а также конфиденциальной информацией и сведениями о собственности Microsoft Corporation.</span><span class="sxs-lookup"><span data-stu-id="62e19-608">This document supports a preliminary release of a software product that may be changed substantially prior to final commercial release, and is the confidential and proprietary information of Microsoft Corporation.</span></span> <span data-ttu-id="62e19-609">Оно раскрывается в соответствии с соглашением о неразглашении между получателем и корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="62e19-609">It is disclosed pursuant to a non-disclosure agreement between the recipient and Microsoft.</span></span> <span data-ttu-id="62e19-610">Этот документ предоставляется исключительно в информационных целях, и корпорация Майкрософт не дает никаких гарантий, явных и подразумеваемых, в этом документе.</span><span class="sxs-lookup"><span data-stu-id="62e19-610">This document is provided for informational purposes only and Microsoft makes no warranties, either express or implied, in this document.</span></span> <span data-ttu-id="62e19-611">Информация в этом документе, включая URL-адреса и другие ссылки на веб-сайты, может быть изменена без предварительного уведомления.</span><span class="sxs-lookup"><span data-stu-id="62e19-611">Information in this document, including URL and other Internet website references, is subject to change without notice.</span></span> <span data-ttu-id="62e19-612">Весь риск за использование или результаты использования этого документа сохраняется вместе с пользователем.</span><span class="sxs-lookup"><span data-stu-id="62e19-612">The entire risk of the use or the results from the use of this document remains with the user.</span></span> <span data-ttu-id="62e19-613">Если не указано иное, компании, Организации, товары, доменные имена, адреса электронной почты, логотипы, люди, места и события, показанные в приведенных ниже примерах, являются вымышленными.</span><span class="sxs-lookup"><span data-stu-id="62e19-613">Unless otherwise noted, the companies, organizations, products, domain names, email addresses, logos, people, places, and events depicted in examples herein are fictitious.</span></span> <span data-ttu-id="62e19-614">Никаких связей с реальными компаниями, организациями, продуктами, доменными именами, адресами электронной почты, логотипами, лицами, местами и событиями является случайным образом.</span><span class="sxs-lookup"><span data-stu-id="62e19-614">No association with any real company, organization, product, domain name, email address, logo, person, place, or event is intended or should be inferred.</span></span> <span data-ttu-id="62e19-615">Ответственность за соблюдение всех применимых законов об авторском праве лежит на пользователе.</span><span class="sxs-lookup"><span data-stu-id="62e19-615">Complying with all applicable copyright laws is the responsibility of the user.</span></span> <span data-ttu-id="62e19-616">Без ограничения прав, описанных в разделе авторские права, никакие части этого документа нельзя воспроизводить, хранить или использовать в системе поиска или передавать в любой форме или любым способом (электронные, механические, фотокопирование, запись и т. д.) или в любых целях без специального письменного разрешения корпорации Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="62e19-616">Without limiting the rights under copyright, no part of this document may be reproduced, stored in or introduced into a retrieval system, or transmitted in any form or by any means (electronic, mechanical, photocopying, recording, or otherwise), or for any purpose, without the express written permission of Microsoft Corporation.</span></span>

<span data-ttu-id="62e19-617">Корпорация Майкрософт может иметь патенты, патентные приложения, торговые марки, авторские права и другие права на интеллектуальную собственность, касающиеся темы в этом документе.</span><span class="sxs-lookup"><span data-stu-id="62e19-617">Microsoft may have patents, patent applications, trademarks, copyrights, or other intellectual property rights covering subject matter in this document.</span></span> <span data-ttu-id="62e19-618">За исключением случаев, явно оговоренных в письменных лицензионных соглашениях от корпорации Майкрософт, предоставление этого документа не дает вам лицензии на эти патенты, товарные знаки, авторские права и другую интеллектуальную собственность.</span><span class="sxs-lookup"><span data-stu-id="62e19-618">Except as expressly provided in any written license agreement from Microsoft, the furnishing of this document does not give you any license to these patents, trademarks, copyrights, or other intellectual property.</span></span>

<span data-ttu-id="62e19-619">© 2012 Корпорация Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="62e19-619">© 2012 Microsoft Corporation.</span></span> <span data-ttu-id="62e19-620">Все права защищены.</span><span class="sxs-lookup"><span data-stu-id="62e19-620">All rights reserved.</span></span>

<span data-ttu-id="62e19-621">Microsoft, Windows, Windows Live, Internet Explorer, MSN, Outlook и SQL Server — охраняемые товарные знаки или охраняемые товарные знаки Microsoft Corporation в США и/или других странах или регионах.</span><span class="sxs-lookup"><span data-stu-id="62e19-621">Microsoft, Windows, Windows Live, Active Directory, Internet Explorer, MSN, Outlook, and SQL Server are either registered trademarks or trademarks of Microsoft Corporation in the United States and/or other countries/regions.</span></span>

<span data-ttu-id="62e19-622">Все прочие товарные знаки являются собственностью соответствующих владельцев.</span><span class="sxs-lookup"><span data-stu-id="62e19-622">All other trademarks are property of their respective owners.</span></span>

<span data-ttu-id="62e19-623"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="62e19-623"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

