---
title: 'Lync Server 2013: проверка журналов событий'
description: 'Lync Server 2013: проверка журналов событий.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Checking event logs
ms:assetid: 5500720d-c628-4dbd-84bc-a5becc39b99c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720914(v=OCS.15)
ms:contentKeyID: 63969602
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6617bde846fd38ab3282fd023b16e0a921f48920
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434930"
---
# <a name="checking-event-logs-in-lync-server-2013"></a><span data-ttu-id="cf496-103">Проверка журналов событий в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cf496-103">Checking event logs in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cf496-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cf496-104">

<span> </span></span></span>

<span data-ttu-id="cf496-105">_**Тема последнего изменения:** 2014-08-06_</span><span class="sxs-lookup"><span data-stu-id="cf496-105">_**Topic Last Modified:** 2014-08-06_</span></span>

<span data-ttu-id="cf496-106">Вы можете использовать [средство просмотра событий Windows](https://go.microsoft.com/fwlink/p/?linkid=314067) для просмотра журналов событий и получения сведений о сбоях служб, ошибках репликации в СЛУЖБАХ AD DS и предупреждениях о системных ресурсах, таких как виртуальная память и место на диске.</span><span class="sxs-lookup"><span data-stu-id="cf496-106">You can use [Windows Event Viewer](https://go.microsoft.com/fwlink/p/?linkid=314067) to view event logs and obtain information about service failures, replication errors in the AD DS, and warnings about system resources such as virtual memory and disk space.</span></span> <span data-ttu-id="cf496-107">Средство просмотра событий входит в состав Windows Server 2008 и 2012.</span><span class="sxs-lookup"><span data-stu-id="cf496-107">Event Viewer is included with Windows Server 2008 and 2012.</span></span>

<span data-ttu-id="cf496-108">В средстве ведения журнала Lync Server 2013 по завершении сеанса отладки выберите пункт **Анализ файлов журнала** для просмотра файлов журнала с помощью средства snooper.</span><span class="sxs-lookup"><span data-stu-id="cf496-108">In the Lync Server 2013 Logging Tool, when you end the debug session, click **Analyze Log Files** to view the log files by using the Snooper tool.</span></span>

<span data-ttu-id="cf496-109">В средстве просмотра событий хранятся журналы событий приложений, безопасности и системы.</span><span class="sxs-lookup"><span data-stu-id="cf496-109">Event Viewer maintains logs about application, security, and system events on the computer.</span></span> <span data-ttu-id="cf496-110">В журналах событий в приложениях Lync Server 2013 и Windows выводятся предупреждения и условия возникновения ошибок.</span><span class="sxs-lookup"><span data-stu-id="cf496-110">Both Lync Server 2013 and Windows report warnings and error conditions to the event logs.</span></span> <span data-ttu-id="cf496-111">Поэтому следует просматривать журналы событий ежедневно.</span><span class="sxs-lookup"><span data-stu-id="cf496-111">Therefore, review event logs daily.</span></span>

<span data-ttu-id="cf496-112">С помощью средства просмотра событий можно выполнять следующие действия:</span><span class="sxs-lookup"><span data-stu-id="cf496-112">Use Event Viewer to:</span></span>

  - <span data-ttu-id="cf496-113">Просмотр журналов событий и управление ими.</span><span class="sxs-lookup"><span data-stu-id="cf496-113">View and manage event logs.</span></span>

  - <span data-ttu-id="cf496-114">Получение сведений о проблемах оборудования, программного обеспечения и системы, которые необходимо устранить.</span><span class="sxs-lookup"><span data-stu-id="cf496-114">Obtain information about hardware, software, and system issues that must be resolved.</span></span>

  - <span data-ttu-id="cf496-115">Определение тенденций, требующих дальнейших действий.</span><span class="sxs-lookup"><span data-stu-id="cf496-115">Identify trends that require future action.</span></span>

<span data-ttu-id="cf496-116">Сервер, на котором работает Lync Server в операционной системе Windows Server, записывает события из четырех типов журналов.</span><span class="sxs-lookup"><span data-stu-id="cf496-116">A server that is running Lync Server on a Windows Server operating system records events in four types of logs:</span></span>

  - <span data-ttu-id="cf496-117">**Журналы приложений**   В журнале приложений содержатся события, зафиксированные приложениями или программами.</span><span class="sxs-lookup"><span data-stu-id="cf496-117">**Application logs**   The Application log contains events logged by applications or programs.</span></span> <span data-ttu-id="cf496-118">Разработчики определяют, какие события нужно заносить в журнал.</span><span class="sxs-lookup"><span data-stu-id="cf496-118">Developers determine which events to log.</span></span> <span data-ttu-id="cf496-119">Например, программа для базы данных может записать ошибку файла в журнал приложений.</span><span class="sxs-lookup"><span data-stu-id="cf496-119">For example, a database program might record a file error in the Application log.</span></span> <span data-ttu-id="cf496-120">Большинство событий, связанных с Lync Server 2013, отображаются в журнале приложений.</span><span class="sxs-lookup"><span data-stu-id="cf496-120">Most Lync Server 2013-related events appear in the Application log.</span></span>

  - <span data-ttu-id="cf496-121">**Журналы безопасности**   В журнал безопасности записываются такие события, как допустимые и недопустимые попытки входа в систему в дополнение к событиям, связанным с использованием ресурсов, таких как создание, открытие и удаление файлов или других объектов.</span><span class="sxs-lookup"><span data-stu-id="cf496-121">**Security logs**   The Security log records events such as valid and not valid logon tries in addition to events related to resource use such as creating, opening, or deleting files or other objects.</span></span> <span data-ttu-id="cf496-122">Например, если включен аудит входа, попытки входа в систему записываются в журнал безопасности.</span><span class="sxs-lookup"><span data-stu-id="cf496-122">For example, if logon auditing is enabled, attempts to log on to the system are recorded in the Security log.</span></span>

  - <span data-ttu-id="cf496-123">**Журналы системы**   Журнал системы включает события, зафиксированные системными компонентами Windows.</span><span class="sxs-lookup"><span data-stu-id="cf496-123">**System logs**   The System log contains events logged by Windows system components.</span></span> <span data-ttu-id="cf496-124">Например, сбой драйвера или другого системного компонента для загрузки при запуске записывается в системный журнал.</span><span class="sxs-lookup"><span data-stu-id="cf496-124">For example, the failure of a driver or other system component to load during startup is recorded in the System log.</span></span> <span data-ttu-id="cf496-125">Типы событий, зафиксированных компонентами системы, предварительно определены сервером.</span><span class="sxs-lookup"><span data-stu-id="cf496-125">The event types logged by system components are predetermined by the server.</span></span>

  - <span data-ttu-id="cf496-126">**Lync Server 2013**   В средстве ведения журнала записываются важные события, связанные с проверкой подлинности, соединениями и действиями пользователей.</span><span class="sxs-lookup"><span data-stu-id="cf496-126">**Lync Server 2013**   The logging tool records significant events related to authentication, connections, and user actions.</span></span> <span data-ttu-id="cf496-127">После включения диагностического протоколирования вы можете просматривать записи в журнале в средстве просмотра событий.</span><span class="sxs-lookup"><span data-stu-id="cf496-127">After enabling diagnostic logging, you can view the log entries in Event Viewer.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="cf496-128">Мы не рекомендуем использовать параметры максимального ведения журнала, если только вы не предоставили это в службе поддержки пользователей корпорации Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="cf496-128">We do not recommend that you use the maximum logging settings unless you are instructed to do this by Microsoft Customer Support Services.</span></span> <span data-ttu-id="cf496-129">При максимальном ведении журнала загружаются существенные ресурсы, а также все "ложные положительные", то есть ошибки, которые регистрируются только при максимальном ведении журнала, но являются ожидаемыми и не являются причиной проблемы.</span><span class="sxs-lookup"><span data-stu-id="cf496-129">Maximum logging drains significant resources and can give many “false positives,” that is, errors that get logged only at maximum logging but are really expected and are not a cause of concern.</span></span> <span data-ttu-id="cf496-130">Кроме того, мы рекомендуем не включать функцию диагностического протоколирования без возможности восстановления.</span><span class="sxs-lookup"><span data-stu-id="cf496-130">We also recommend that you do not enable diagnostic logging permanently.</span></span> <span data-ttu-id="cf496-131">Используйте его только при устранении неполадок.</span><span class="sxs-lookup"><span data-stu-id="cf496-131">Use it only when troubleshooting.</span></span>



</div>

<span data-ttu-id="cf496-132">В каждом журнале средства просмотра событий в Lync Server 2013 записываются информационные и предупреждающие сообщения и события ошибок.</span><span class="sxs-lookup"><span data-stu-id="cf496-132">Within each Event Viewer log, Lync Server 2013 records informational, warning, and error events.</span></span> <span data-ttu-id="cf496-133">Тщательно отслеживайте эти журналы, чтобы отслеживать типы транзакций, выполняемых на серверах Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="cf496-133">Monitor these logs closely to track the types of transactions being conducted on the Lync Server 2013 servers.</span></span> <span data-ttu-id="cf496-134">Вы должны периодически архивировать журналы или использовать автоматическую смену, чтобы не заполнять место.</span><span class="sxs-lookup"><span data-stu-id="cf496-134">You should periodically archive the logs or use automatic rollover to avoid running out of space.</span></span> <span data-ttu-id="cf496-135">Поскольку файлы журнала могут занимать конечное пространство, следует увеличивать размер журнала (например, до 50 МБ) и настроить его на перезапись, чтобы сервер Lync Server 2013 мог продолжать создавать новые события.</span><span class="sxs-lookup"><span data-stu-id="cf496-135">Because log files can occupy a finite amount of space, increase the log size (for example, to 50 MB) and set it to overwrite so that the Lync Server 2013 Server can continue to write new events.</span></span>

<span data-ttu-id="cf496-136">Вы также можете автоматизировать администрирование журнала событий с помощью следующих средств и технологий:</span><span class="sxs-lookup"><span data-stu-id="cf496-136">You can also automate event log administration by using the following tools and technologies:</span></span>

  - <span data-ttu-id="cf496-137">System Center Operations Manager наблюдает за работоспособностью и использованием серверов Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="cf496-137">System Center Operations Manager monitors the health and use of Lync Server 2013 servers.</span></span> <span data-ttu-id="cf496-138">Пакет управления Lync Server 2013 для Operations Manager расширяет возможности Operations Manager, предоставляя специализированный мониторинг для серверов, на которых запущен Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="cf496-138">Lync Server 2013 Management Pack for Operations Manager extends Operations Manager by providing specialized monitoring for servers that are running Lync Server 2013.</span></span>

  - <span data-ttu-id="cf496-139">Пакет управления Lync Server 2013 для Operations Manager наблюдает за стандартом и корпоративным выпуском Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="cf496-139">The Lync Server 2013 Management Pack for Operations Manager monitors Standard and Enterprise Edition of Lync Server 2013.</span></span> <span data-ttu-id="cf496-140">Кроме того, в этом выпуске установлен пакет управления качеством качества (QoE), который ранее был создан в отдельном пакете управления.</span><span class="sxs-lookup"><span data-stu-id="cf496-140">This release also incorporates the Quality of Experience (QoE) Management Pack which was previously a separate management pack.</span></span>

<span data-ttu-id="cf496-141">Отслеживаемые типы — это записи журнала событий, счетчики производительности и мониторинг состояния QoE.</span><span class="sxs-lookup"><span data-stu-id="cf496-141">Monitored types are event log entries, performance counters and stateful monitoring of QoE.</span></span> <span data-ttu-id="cf496-142">Эта версия пакета управления наблюдает только для Lync Server 2013 и 2010 и не может использоваться для мониторинга Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="cf496-142">This version of the management pack only monitors Lync Server 2013 and 2010, and cannot be used to monitor Office Communications Server 2007.</span></span>

<span data-ttu-id="cf496-143">Пакет управления предоставляет следующие возможности:</span><span class="sxs-lookup"><span data-stu-id="cf496-143">The management pack provides the following features:</span></span>

  - <span data-ttu-id="cf496-144">Оповещения о событиях, влияющих на обслуживание</span><span class="sxs-lookup"><span data-stu-id="cf496-144">Alerts indicating service affecting events</span></span>

  - <span data-ttu-id="cf496-145">Оповещения, указывающие на конфигурацию и другие проблемы, не связанные с обслуживанием</span><span class="sxs-lookup"><span data-stu-id="cf496-145">Alerts indicating configuration, and other non-service impacting issues</span></span>

  - <span data-ttu-id="cf496-146">Наблюдение за состоянием служб Lync Server</span><span class="sxs-lookup"><span data-stu-id="cf496-146">State monitoring of Lync Server services</span></span>

  - <span data-ttu-id="cf496-147">Сведения о продукте: причина и решение обнаруженных проблем</span><span class="sxs-lookup"><span data-stu-id="cf496-147">Product knowledge: Cause and resolution of identified issues</span></span>

<span data-ttu-id="cf496-148">Дополнительные сведения о пакете управления Lync Server 2013 можно найти в разделе [мониторинг сервера Lync server 2013 с помощью System Center Operations Manager](lync-server-2013-monitoring-lync-server-with-system-center-operations-manager.md).</span><span class="sxs-lookup"><span data-stu-id="cf496-148">For more information about Lync Server 2013 Management Pack, refer to [Monitoring Lync Server 2013 with System Center Operations Manager](lync-server-2013-monitoring-lync-server-with-system-center-operations-manager.md).</span></span>

<span data-ttu-id="cf496-149">**Объединение событий**   Инструмент «объединение событий» собирает отдельные события из журналов событий нескольких компьютеров в единое место.</span><span class="sxs-lookup"><span data-stu-id="cf496-149">**Event Comb**   The Event Comb tool collects specific events from the event logs of several computers to one central location.</span></span> <span data-ttu-id="cf496-150">Он позволяет сообщать только о кодах событий и их источниках событий.</span><span class="sxs-lookup"><span data-stu-id="cf496-150">It lets you report on only the event IDs or event sources it specifies.</span></span> <span data-ttu-id="cf496-151">Дополнительные сведения о событии можно найти на веб-сайте [блокировки учетных записей и средств управления](https://go.microsoft.com/fwlink/?linkid=35607) .</span><span class="sxs-lookup"><span data-stu-id="cf496-151">For more information about Event Comb, see the [Account Lockout and Management Tools](https://go.microsoft.com/fwlink/?linkid=35607) website.</span></span>

<span data-ttu-id="cf496-152">**Триггеры событий**   В Windows Server 2012 вы можете "прикрепить задачу к этому событию" в окне просмотра событий Windows, в котором администратор может либо запустить программу, либо отправить сообщение электронной почты или отобразить сообщение на экране.</span><span class="sxs-lookup"><span data-stu-id="cf496-152">**Event triggers**   In Windows Server 2012 you can "Attach a Task to This Event" within the Windows Event Viewer—where an administrator can either run a program, send an email message or display an on-screen message.</span></span> <span data-ttu-id="cf496-153">Дополнительные сведения об этой функции можно найти в разделе Windows Server 2008 R2 [выполнение задачи в ответ на данное событие](https://technet.microsoft.com/library/cc748900.aspx).</span><span class="sxs-lookup"><span data-stu-id="cf496-153">For more information about this feature, see the Windows Server 2008 R2 topic [Run a Task in Response to a Given Event](https://technet.microsoft.com/library/cc748900.aspx).</span></span> <span data-ttu-id="cf496-154">Кроме того, вы можете использовать средства командной строки, такие как "Eventtrigger.exe", для создания и запроса журналов событий и связывания программ с определенным протоколированием событий.</span><span class="sxs-lookup"><span data-stu-id="cf496-154">You can also use command-line tools such as ‘Eventtrigger.exe’ to create and query event logs and associate programs with particular logged events.</span></span> <span data-ttu-id="cf496-155">С помощью Eventtriggers.exe вы можете создавать триггеры событий, которые запускают программы при возникновении конкретных событий.</span><span class="sxs-lookup"><span data-stu-id="cf496-155">By using Eventtriggers.exe, you can create event triggers that run programs when specific events occur.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="cf496-156">См. также</span><span class="sxs-lookup"><span data-stu-id="cf496-156">See Also</span></span>


[<span data-ttu-id="cf496-157">Средство просмотра событий Windows</span><span class="sxs-lookup"><span data-stu-id="cf496-157">Windows Event Viewer</span></span>](https://go.microsoft.com/fwlink/p/?linkid=314067)  
  

<span data-ttu-id="cf496-158"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cf496-158"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

