---
title: 'Lync Server 2013: еженедельные задачи'
description: 'Lync Server 2013: еженедельные задачи.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Weekly tasks
ms:assetid: d564839b-b49d-4c5d-b67e-dc5abb0f6980
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn722432(v=OCS.15)
ms:contentKeyID: 63969650
ms.date: 08/20/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d818e1140141a470bb57a1471bb04931f505a6bd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443848"
---
# <a name="weekly-tasks-in-lync-server-2013"></a><span data-ttu-id="937c1-103">Еженедельные задачи в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="937c1-103">Weekly tasks in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="937c1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="937c1-104">

<span> </span></span></span>

<span data-ttu-id="937c1-105">_**Тема последнего изменения:** 2015-08-17_</span><span class="sxs-lookup"><span data-stu-id="937c1-105">_**Topic Last Modified:** 2015-08-17_</span></span>

<span data-ttu-id="937c1-106">Еженедельные задачи обычно связаны с сбором и анализом журналов и отчетов.</span><span class="sxs-lookup"><span data-stu-id="937c1-106">Weekly tasks are generally related to collecting and analyzing logs and reports.</span></span>

<div>

## <a name="archive-event-logs"></a><span data-ttu-id="937c1-107">Архивация журналов событий</span><span class="sxs-lookup"><span data-stu-id="937c1-107">Archive event logs</span></span>

<span data-ttu-id="937c1-108">Если журналы событий не настроены на перезапись событий, они должны быть регулярно заархивированы и удалены.</span><span class="sxs-lookup"><span data-stu-id="937c1-108">If event logs are not configured to overwrite events as required, they must be regularly archived and deleted.</span></span> <span data-ttu-id="937c1-109">Это действие особенно важно для журналов безопасности, которые могут потребоваться при исследовании попыток нарушения безопасности.</span><span class="sxs-lookup"><span data-stu-id="937c1-109">This action is especially important for security logs, which may be required when investigating attempted security breaches.</span></span>

<span data-ttu-id="937c1-110">Организация должна определять политики и процедуры для архивации журнала.</span><span class="sxs-lookup"><span data-stu-id="937c1-110">Your organization will have to define policies and procedures for log archiving.</span></span>

</div>

<div>

## <a name="create-reports"></a><span data-ttu-id="937c1-111">Создание отчетов</span><span class="sxs-lookup"><span data-stu-id="937c1-111">Create reports</span></span>

<span data-ttu-id="937c1-112">Создание отчетов о состоянии, помогающих при планировании ресурсов, проверках SLA и анализе производительности.</span><span class="sxs-lookup"><span data-stu-id="937c1-112">Create status reports to help with capacity planning, SLA reviews, and performance analysis.</span></span> <span data-ttu-id="937c1-113">Используйте ежедневные данные из журнала событий и системного монитора для создания отчетов об использовании диска, памяти и ЦП.</span><span class="sxs-lookup"><span data-stu-id="937c1-113">Use daily data from event log and System Monitor to create reports on disk, memory, and CPU usage.</span></span> <span data-ttu-id="937c1-114">С помощью System Center Operations Manager Создавайте отчеты о доступности и работоспособности.</span><span class="sxs-lookup"><span data-stu-id="937c1-114">Use System Center Operations Manager to generate uptime and availability reports.</span></span>

<span data-ttu-id="937c1-115">Организация должна определять политики и процедуры для отчетов о состоянии.</span><span class="sxs-lookup"><span data-stu-id="937c1-115">Your organization will have to define policies and procedures for status reports.</span></span>

</div>

<div>

## <a name="incident-reports"></a><span data-ttu-id="937c1-116">Отчеты об инцидентах</span><span class="sxs-lookup"><span data-stu-id="937c1-116">Incident reports</span></span>

<span data-ttu-id="937c1-117">Еженедельный аудит отчетов об инцидентах Организации, связанных с Lync Server.</span><span class="sxs-lookup"><span data-stu-id="937c1-117">Perform a weekly audit of your organization’s incident reports that relate to Lync Server.</span></span> <span data-ttu-id="937c1-118">Этот аудит должен включать в себя следующее:</span><span class="sxs-lookup"><span data-stu-id="937c1-118">This audit should include the following:</span></span>

  - <span data-ttu-id="937c1-119">Самые популярные, разрешенные и незавершенные инциденты.</span><span class="sxs-lookup"><span data-stu-id="937c1-119">The top generated, resolved, and pending incidents.</span></span>

  - <span data-ttu-id="937c1-120">Решения для неразрешенных происшествий.</span><span class="sxs-lookup"><span data-stu-id="937c1-120">Solutions for unresolved incidents.</span></span>

  - <span data-ttu-id="937c1-121">Обновление отчетов для включения новых билетов на проблемы.</span><span class="sxs-lookup"><span data-stu-id="937c1-121">Updating reports to include new trouble tickets.</span></span>

  - <span data-ttu-id="937c1-122">Обновление репозитория документов для руководств, посвященных устранению неполадок, и публикация неустранимых проблем.</span><span class="sxs-lookup"><span data-stu-id="937c1-122">Updating a document repository for troubleshooting guides and post mortems about outages.</span></span>

<span data-ttu-id="937c1-123">Поскольку система отслеживания происшествий Организации является вариантом выбора, независимого от Lync Server, некоторые инструкции или указатели недоступны.</span><span class="sxs-lookup"><span data-stu-id="937c1-123">Since your organization’s incident tracking system is a choice independent of Lync Server, specific instructions or pointers are not available.</span></span> <span data-ttu-id="937c1-124">Ознакомьтесь с документацией для системы, выбранной вашей организацией.</span><span class="sxs-lookup"><span data-stu-id="937c1-124">Consult the documentation for the system your organization chose.</span></span>

</div>

<div>

## <a name="check-iis-logs-and-performance"></a><span data-ttu-id="937c1-125">Проверка журналов и производительности IIS</span><span class="sxs-lookup"><span data-stu-id="937c1-125">Check IIS logs and performance</span></span>

<span data-ttu-id="937c1-126">Еженедельное рецензирование журналов служб IIS и производительность.</span><span class="sxs-lookup"><span data-stu-id="937c1-126">Perform a weekly review of Internet Information Services (IIS) logs and performance.</span></span> <span data-ttu-id="937c1-127">Дополнительные сведения о мониторинге журналов и производительности IIS можно найти в статье [Обзор ведения журнала событий служб IIS для Windows Server 2003](https://go.microsoft.com/fwlink/?linkid=36077).</span><span class="sxs-lookup"><span data-stu-id="937c1-127">For more information about how to monitor IIS logs and performance, see [Windows Server 2003 Internet Information Services (IIS) Event Logging Overview](https://go.microsoft.com/fwlink/?linkid=36077).</span></span> <span data-ttu-id="937c1-128">Проверка должна включать следующее:</span><span class="sxs-lookup"><span data-stu-id="937c1-128">The review should include the following:</span></span>

  - <span data-ttu-id="937c1-129">Счетчики кэша веб-службы для контроля кэша службы WWW.</span><span class="sxs-lookup"><span data-stu-id="937c1-129">Web Service Cache counters to monitor the WWW service cache.</span></span>

  - <span data-ttu-id="937c1-130">Счетчики ASP-страниц (ASPs) для наблюдения за приложениями, которые выполняются как ASPs.</span><span class="sxs-lookup"><span data-stu-id="937c1-130">Active Server Pages (ASPs) counters to monitor applications that run as ASPs.</span></span>

</div>

<div>

## <a name="generate-database-reports"></a><span data-ttu-id="937c1-131">Создание отчетов базы данных</span><span class="sxs-lookup"><span data-stu-id="937c1-131">Generate database reports</span></span>

<span data-ttu-id="937c1-132">**Создание отчетов в базе данных SQL**</span><span class="sxs-lookup"><span data-stu-id="937c1-132">**To generate reports on the SQL Database**</span></span>

1.  <span data-ttu-id="937c1-133">Откройте Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="937c1-133">Open Lync Server 2013.</span></span>

2.  <span data-ttu-id="937c1-134">В дереве консоли разверните узел леса, разверните **Пулы предприятий** и выберите пул, для которого требуется создать отчет базы данных.</span><span class="sxs-lookup"><span data-stu-id="937c1-134">In the console tree, expand the forest node, expand **Enterprise pools**, and then click the pool for which you want to generate a database report.</span></span>

3.  <span data-ttu-id="937c1-135">В области сведений откройте вкладку **база данных** .</span><span class="sxs-lookup"><span data-stu-id="937c1-135">In the details pane, click the **Database** tab.</span></span>

4.  <span data-ttu-id="937c1-136">На вкладке **база данных** выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="937c1-136">On the **Database** tab, do the following:</span></span>
    
    1.  <span data-ttu-id="937c1-137">Чтобы просмотреть имя базы данных, разверните раздел **Общие параметры** и просмотрите имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="937c1-137">To view the name of the database, expand **General Settings**, and view the database name.</span></span>
    
    2.  <span data-ttu-id="937c1-138">Чтобы получить сводную статистику текущего пользователя для пула, разверните раздел **Сводные отчеты пользователей**, нажмите кнопку **Перейти** и просмотрите результаты.</span><span class="sxs-lookup"><span data-stu-id="937c1-138">To retrieve current user summary statistics for the pool, expand **User Summary Reports**, click **Go**, and view the results.</span></span>
    
    3.  <span data-ttu-id="937c1-139">Чтобы получить текущие данные пользователя для одного пользователя пула, разверните раздел **отчеты для каждого пользователя**, введите URI SIP пользователя, нажмите кнопку **Перейти** и просмотрите результаты.</span><span class="sxs-lookup"><span data-stu-id="937c1-139">To retrieve current per-user data for a single user of the pool, expand **Per-User Reports**, type the user’s SIP URI, click **Go**, and view the results.</span></span>

<span data-ttu-id="937c1-140">Чтобы получить текущую сводную статистику для пула, разверните **Сводные отчеты по** конференциям, нажмите кнопку **Перейти** и просмотрите результаты.</span><span class="sxs-lookup"><span data-stu-id="937c1-140">To retrieve current conference summary statistics for the pool, expand **Conference Summary Reports**, click **Go**, and view the results.</span></span>

</div>

<div>

## <a name="check-for-security-and-lync-server-updates"></a><span data-ttu-id="937c1-141">Проверка обновлений для системы безопасности и Lync Server</span><span class="sxs-lookup"><span data-stu-id="937c1-141">Check for security and Lync Server updates</span></span>

<span data-ttu-id="937c1-142">Определите новые пакеты обновления, исправления и обновления.</span><span class="sxs-lookup"><span data-stu-id="937c1-142">Identify any new service packs, hotfixes, or updates.</span></span> <span data-ttu-id="937c1-143">При необходимости проверьте эти данные в тестовой лаборатории и используйте процедуры управления изменениями для упорядочения развертывания на рабочих серверах.</span><span class="sxs-lookup"><span data-stu-id="937c1-143">If appropriate, test these in a test lab, and use the change control procedures to arrange for deployment to the production servers.</span></span> <span data-ttu-id="937c1-144">Кроме того, обновления компонентов Lync Server теперь доступны в составе центра обновления Windows.</span><span class="sxs-lookup"><span data-stu-id="937c1-144">Also, Lync Server component updates are now available as part of Windows update.</span></span> <span data-ttu-id="937c1-145">Все обновления компонентов Lync Server необходимо обновлять одновременно на всех серверах, на которых работает Lync Server, для которых применимы обновления.</span><span class="sxs-lookup"><span data-stu-id="937c1-145">All Lync Server component updates must be updated at the same time on all of the servers that are running Lync Server for which the updates are applicable.</span></span>

</div>

<div>

## <a name="run-the-lync-server-2013-best-practice-analyzer"></a><span data-ttu-id="937c1-146">Запуск анализатора соответствия рекомендациям для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="937c1-146">Run the Lync Server 2013 Best Practice Analyzer</span></span>

<span data-ttu-id="937c1-147">Анализатор соответствия рекомендациям для Lync Server 2013 — средство диагностики, которое собирает сведения о конфигурации и определяет, задана ли конфигурация согласно рекомендациям Microsoft.</span><span class="sxs-lookup"><span data-stu-id="937c1-147">The Lync Server 2013 Best Practices Analyzer Tool is a diagnostic tool that collects configuration information and determines whether the configuration is set according to Microsoft best practices.</span></span> <span data-ttu-id="937c1-148">Документация по этому средству — [анализатор соответствия рекомендациям для Lync Server 2013](lync-server-2013-lync-server-best-practices-analyzer.md).</span><span class="sxs-lookup"><span data-stu-id="937c1-148">Documentation for this tool is at [Lync Server 2013 Best Practices Analyzer](lync-server-2013-lync-server-best-practices-analyzer.md).</span></span>

<span data-ttu-id="937c1-149">Это средство сравнивает данные конфигурации развертывания с набором предопределенных правил для Lync Server и сообщает о потенциальных проблемах.</span><span class="sxs-lookup"><span data-stu-id="937c1-149">The tool compares your deployment’s configuration data against a set of pre-defined rules for Lync Server, and reports potential issues.</span></span> <span data-ttu-id="937c1-150">Для каждой обнаруженной ошибки средство предоставляет текущую конфигурацию в среде Lync Server и рекомендуемую конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="937c1-150">For every issue reported, the tool provides the current configuration in the Lync Server environment, and the recommended configuration.</span></span>

<span data-ttu-id="937c1-151">При правильном доступе к сети средство может проанализировать службы AD DS и серверы, на которых работает Lync Server 2013, и выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="937c1-151">With the correct network access, the tool can examine your AD DS and servers that are running Lync Server 2013 to do the following:</span></span>

  - <span data-ttu-id="937c1-152">Упреждающее выполнение проверок работоспособности, проверка настройки конфигурации согласно рекомендуемым рекомендациям</span><span class="sxs-lookup"><span data-stu-id="937c1-152">Proactively perform health checks, verifying that the configuration is set according to recommended best practices</span></span>

  - <span data-ttu-id="937c1-153">Создание списка проблем (например, неоптимальных параметров конфигурации или неподдерживаемых или рекомендуемых параметров)</span><span class="sxs-lookup"><span data-stu-id="937c1-153">Generate a list of issues, such as suboptimal configuration settings or unsupported or not recommended options</span></span>

  - <span data-ttu-id="937c1-154">Оценить общее состояние системы</span><span class="sxs-lookup"><span data-stu-id="937c1-154">Judge the general health of a system</span></span>

  - <span data-ttu-id="937c1-155">Помощь в устранении конкретных проблем</span><span class="sxs-lookup"><span data-stu-id="937c1-155">Help troubleshoot specific issues</span></span>

  - <span data-ttu-id="937c1-156">Запрос на скачивание обновлений (если они доступны)</span><span class="sxs-lookup"><span data-stu-id="937c1-156">Prompt you to download updates if they are available</span></span>

  - <span data-ttu-id="937c1-157">Предоставление сведений об ошибках, связанных с электронной и локальной документацией, и включение советов по устранению неполадок</span><span class="sxs-lookup"><span data-stu-id="937c1-157">Provide online and local documentation about reported issues, and include troubleshooting tips</span></span>

  - <span data-ttu-id="937c1-158">Создание сведений о конфигурации, которые можно записать для последующего просмотра</span><span class="sxs-lookup"><span data-stu-id="937c1-158">Generate configuration information that can be captured for later review</span></span>

<span data-ttu-id="937c1-159">Убедитесь, что RTCBPA.msi установлен на всех серверах Lync Server 2013 и создает еженедельный отчет о работоспособности.</span><span class="sxs-lookup"><span data-stu-id="937c1-159">Ensure that the RTCBPA.msi is installed on all Lync Server 2013 servers, and generate a weekly Health Check Report.</span></span> <span data-ttu-id="937c1-160">Обратите внимание на результаты и, при необходимости, правильность.</span><span class="sxs-lookup"><span data-stu-id="937c1-160">Note the results and correct, if necessary.</span></span>

</div>

<div>

## <a name="review-sla-performance-figures"></a><span data-ttu-id="937c1-161">Проверка показателей эффективности соглашения об уровне обслуживания</span><span class="sxs-lookup"><span data-stu-id="937c1-161">Review SLA performance figures</span></span>

<span data-ttu-id="937c1-162">Проверьте ключевые данные о производительности за предыдущую неделю.</span><span class="sxs-lookup"><span data-stu-id="937c1-162">Check the key performance data for the previous week.</span></span> <span data-ttu-id="937c1-163">Просматривайте производительность в соответствии с требованиями соглашения об уровне обслуживания.</span><span class="sxs-lookup"><span data-stu-id="937c1-163">Review performance against the requirements of the SLA.</span></span> <span data-ttu-id="937c1-164">Определите тенденции и элементы, которые не соответствуют их целям.</span><span class="sxs-lookup"><span data-stu-id="937c1-164">Identify trends and items that have not met their targets.</span></span>

</div>

<div>

## <a name="review-system-center-operations-manager-management-pack-and-quality-of-experience-reports"></a><span data-ttu-id="937c1-165">Просмотр отчетов по пакету управления System Center Operations Manager и улучшения качества обслуживания</span><span class="sxs-lookup"><span data-stu-id="937c1-165">Review System Center Operations Manager Management Pack and quality of experience reports</span></span>

<span data-ttu-id="937c1-166">Получите и ознакомьтесь с отчетами по пакету управления Lync Server 2013 и качественным опытом.</span><span class="sxs-lookup"><span data-stu-id="937c1-166">Obtain and review Lync Server 2013 Management Pack and Quality of Experience reports.</span></span>

</div>

<div>

## <a name="generating-and-viewing-database-reports-for-enterprise-pools"></a><span data-ttu-id="937c1-167">Создание и просмотр отчетов базы данных для корпоративных пулов</span><span class="sxs-lookup"><span data-stu-id="937c1-167">Generating and viewing database reports for enterprise pools</span></span>

<span data-ttu-id="937c1-168">**Создание отчетов пула**</span><span class="sxs-lookup"><span data-stu-id="937c1-168">**To generate pool reports**</span></span>

1.  <span data-ttu-id="937c1-169">Откройте Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="937c1-169">Open Lync Server 2013.</span></span>

2.  <span data-ttu-id="937c1-170">В дереве консоли разверните узел леса, разверните **Пулы предприятий** и выберите пул, для которого требуется создать отчет базы данных.</span><span class="sxs-lookup"><span data-stu-id="937c1-170">In the console tree, expand the forest node, expand **Enterprise pools**, and then click the pool for which you want to generate a database report.</span></span>

3.  <span data-ttu-id="937c1-171">В области сведений откройте вкладку **база данных** .</span><span class="sxs-lookup"><span data-stu-id="937c1-171">In the details pane, click the **Database** tab.</span></span>

4.  <span data-ttu-id="937c1-172">На вкладке **база данных** выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="937c1-172">On the **Database** tab, do the following:</span></span>
    
    1.  <span data-ttu-id="937c1-173">Чтобы просмотреть имя базы данных, разверните раздел **Общие параметры** и просмотрите имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="937c1-173">To view the name of the database, expand **General Settings**, and view the database name.</span></span>
    
    2.  <span data-ttu-id="937c1-174">Чтобы получить сводную статистику текущего пользователя для пула, разверните раздел **Сводные отчеты пользователей**, нажмите кнопку **Перейти** и просмотрите результаты.</span><span class="sxs-lookup"><span data-stu-id="937c1-174">To retrieve current user summary statistics for the pool, expand **User Summary Reports**, click **Go**, and view the results.</span></span>
    
    3.  <span data-ttu-id="937c1-175">Чтобы получить текущие данные пользователя для одного пользователя пула, разверните раздел **отчеты для каждого пользователя**, введите URI SIP пользователя, нажмите кнопку **Перейти** и просмотрите результаты.</span><span class="sxs-lookup"><span data-stu-id="937c1-175">To retrieve current per-user data for a single user of the pool, expand **Per-User Reports**, type the user’s SIP URI, click **Go**, and view the results.</span></span>

<span data-ttu-id="937c1-176">Чтобы получить текущую сводную статистику для пула, разверните **Сводные отчеты по** конференциям, нажмите кнопку **Перейти** и просмотрите результаты.</span><span class="sxs-lookup"><span data-stu-id="937c1-176">To retrieve current conference summary statistics for the pool, expand **Conference Summary Reports**, click **Go**, and view the results.</span></span>

<span data-ttu-id="937c1-177">Для каждого пула предприятий администраторы могут использовать вкладку **Database (база данных** ) для просмотра имени базы данных, а также для получения и просмотра отчетов из этой базы данных.</span><span class="sxs-lookup"><span data-stu-id="937c1-177">For each Enterprise Pool, administrators can use the **Database** tab to view the database name and retrieve and view reports from the database.</span></span>

### <a name="database-reports-and-descriptions"></a><span data-ttu-id="937c1-178">Отчеты и описания баз данных</span><span class="sxs-lookup"><span data-stu-id="937c1-178">Database Reports and Descriptions</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="937c1-179">Раздел</span><span class="sxs-lookup"><span data-stu-id="937c1-179">Section</span></span></th>
<th><span data-ttu-id="937c1-180">Описание</span><span class="sxs-lookup"><span data-stu-id="937c1-180">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="937c1-181">Сводные отчеты пользователей</span><span class="sxs-lookup"><span data-stu-id="937c1-181">User Summary Reports</span></span></p></td>
<td><p><span data-ttu-id="937c1-182">Dbanalyze/v/Report: DIAG [/SQLServer: значение]</span><span class="sxs-lookup"><span data-stu-id="937c1-182">Dbanalyze /v /report:diag [/sqlserver:value]</span></span></p>
<p><span data-ttu-id="937c1-183">В этом разделе выводятся обобщенные сведения о пользователях в пуле, например количество включенных пользователей, среднее количество контактов на пользователя и количество пользователей для определенных функций.</span><span class="sxs-lookup"><span data-stu-id="937c1-183">This section displays aggregate information about users in a pool, such as the number of enabled users, the average number of contacts per user, and the number of users for specific features.</span></span></p>
<p><span data-ttu-id="937c1-184">При использовании этих отчетов могут быть полезны следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="937c1-184">When using these reports, the following information may be helpful:</span></span></p>
<ul>
<li><p><span data-ttu-id="937c1-185">Включенный пользователь — это пользователь, который поддерживает Lync Server 2013 с помощью оснастки "пользователи и компьютеры Active Directory".</span><span class="sxs-lookup"><span data-stu-id="937c1-185">An enabled user is a user who is enabled for Lync Server 2013 by using the Active Directory Users and Computers Snap-in.</span></span></p></li>
<li><p><span data-ttu-id="937c1-186">Активный пользователь — это пользователь, который вошел в систему или зарегистрировался.</span><span class="sxs-lookup"><span data-stu-id="937c1-186">An active user is a user who has logged on or registered.</span></span></p></li>
<li><p><span data-ttu-id="937c1-187">Сводные отчеты также предлагают набор статистических сведений о контактах.</span><span class="sxs-lookup"><span data-stu-id="937c1-187">The summary reports also offer a set of statistical information about contacts.</span></span> <span data-ttu-id="937c1-188">Эти статистические данные действительны только для совокупности пользователей, которые вошли хотя бы один раз, и у кого есть хотя бы один контакт.</span><span class="sxs-lookup"><span data-stu-id="937c1-188">These statistics are only valid for the population of users who have logged on at least one time, and who have at least one contact.</span></span> <span data-ttu-id="937c1-189">Как правило, вы обычно не видите минимальное количество контактов, равное 0.</span><span class="sxs-lookup"><span data-stu-id="937c1-189">Consequently, you'll typically not see a minimum number of contacts of 0.</span></span> <span data-ttu-id="937c1-190">Из-за такого поведения в случае, если пользователь не имеет контактных данных (но активен, зарегистрирован ли пользователь), &lt; &gt; для некоторых полей статистики можно увидеть: пусто.</span><span class="sxs-lookup"><span data-stu-id="937c1-190">Because of this behavior, if a user has no contacts (but is active, in that the user has registered), you may see: &lt;empty&gt; for some statistics fields.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="937c1-191">Отчеты о Per-User</span><span class="sxs-lookup"><span data-stu-id="937c1-191">Per-User Reports</span></span></p></td>
<td><p><span data-ttu-id="937c1-192">Dbanalyze/v/Report: диск [/SQLServer: значение]</span><span class="sxs-lookup"><span data-stu-id="937c1-192">Dbanalyze /v /report:disk [/sqlserver:value]</span></span></p>
<p><span data-ttu-id="937c1-193">В отличие от сводных отчетов, которые рассчитываются по Генеральной совокупности пользователей, они представляют собой отчеты об определенном пользователе.</span><span class="sxs-lookup"><span data-stu-id="937c1-193">Unlike the summary reports, which are calculated over a user population, these are reports about a specific user.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="937c1-194">Сводные отчеты по конференциям</span><span class="sxs-lookup"><span data-stu-id="937c1-194">Conference Summary Reports</span></span></p></td>
<td><p><span data-ttu-id="937c1-195">Dbanalyze/v/Report: conf [/SQLServer: значение]</span><span class="sxs-lookup"><span data-stu-id="937c1-195">Dbanalyze /v /report:conf [/sqlserver:value]</span></span></p>
<p><span data-ttu-id="937c1-196">В этом разделе выводятся общие сведения о статистике собраний для пула, например количество активных конференций и общее количество участников.</span><span class="sxs-lookup"><span data-stu-id="937c1-196">This section displays aggregate information about conference summary statistics for the pool, such as the number of active conferences and total number of participants.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="running-bandwidth-utilization-analyzer"></a><span data-ttu-id="937c1-197">Запуск анализатора использования пропускной способности</span><span class="sxs-lookup"><span data-stu-id="937c1-197">Running Bandwidth Utilization Analyzer</span></span>

<span data-ttu-id="937c1-198">Анализатор использования полосы пропускания — это средство, которое создает отчеты о различных аспектах использования полосы пропускания каналов глобальной сети конечными точками объединенных коммуникаций в корпоративной сети.</span><span class="sxs-lookup"><span data-stu-id="937c1-198">Bandwidth Utilization Analyzer is a tool that creates reports about various views of bandwidth consumption by the UC endpoints across WAN links in the enterprise network.</span></span> <span data-ttu-id="937c1-199">Эти отчеты можно использовать для понимания текущего шаблона потребления для пропускной способности и для планирования пропускной способности по мощности.</span><span class="sxs-lookup"><span data-stu-id="937c1-199">These reports can be used to understand the current bandwidth consumption pattern and to help with bandwidth capacity planning.</span></span> <span data-ttu-id="937c1-200">Оно также позволяет просматривать полосу пропускания, назначенную различным каналам.</span><span class="sxs-lookup"><span data-stu-id="937c1-200">It also iterates on the bandwidth capacity that is assigned to various links.</span></span>

<span data-ttu-id="937c1-201">Это средство предоставляет следующие возможности:</span><span class="sxs-lookup"><span data-stu-id="937c1-201">This tool does the following:</span></span>

  - <span data-ttu-id="937c1-202">Создание специальных отчетов по использованию звука в сети</span><span class="sxs-lookup"><span data-stu-id="937c1-202">Generates specific reports for audio usage over the network</span></span>

  - <span data-ttu-id="937c1-203">позволяет более эффективно планировать емкость и распределять полосы пропускания, назначенные различным каналам.</span><span class="sxs-lookup"><span data-stu-id="937c1-203">Helps with more effective capacity planning and iteration on the bandwidth capacity that is assigned to various links</span></span>

<span data-ttu-id="937c1-204">Анализатор использования пропускной способности может создавать графические представления о емкости и отчетах об использовании пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="937c1-204">Bandwidth Utilization Analyzer can generate graphical plots of bandwidth capacity and usage reports.</span></span> <span data-ttu-id="937c1-205">Они перечислены ниже.</span><span class="sxs-lookup"><span data-stu-id="937c1-205">They are as follows:</span></span>

  - <span data-ttu-id="937c1-206">для всех каналов глобальной сети в корпоративной сети;</span><span class="sxs-lookup"><span data-stu-id="937c1-206">All the WAN links in the enterprise network</span></span>

  - <span data-ttu-id="937c1-207">Отфильтровано по выбранным глобальным каналам связи</span><span class="sxs-lookup"><span data-stu-id="937c1-207">Filtered by selected WAN links that were chosen</span></span>

  - <span data-ttu-id="937c1-208">для каналов глобальной сети, емкость которых превышена;</span><span class="sxs-lookup"><span data-stu-id="937c1-208">Filtered by WAN links that have exceeded link capacity</span></span>

  - <span data-ttu-id="937c1-209">Фильтрация по каналам глобальной сети, которые использовали подготовленную пропускную способность</span><span class="sxs-lookup"><span data-stu-id="937c1-209">Filtered by WAN links that were under-using the provisioned bandwidth</span></span>

  - <span data-ttu-id="937c1-210">Фильтрация по глобальным каналам связи (использование пропускной способности, превышающее 90 процента пропускной способности ссылки WAN)</span><span class="sxs-lookup"><span data-stu-id="937c1-210">Filter by WAN links that were reaching critical levels (a bandwidth usage that is greater than 90 percent of bandwidth capacity of the WAN link)</span></span>

  - <span data-ttu-id="937c1-211">Фильтрация по типу ссылки WAN — ссылки на сайты, межсетевые ссылки и ссылки на сайте</span><span class="sxs-lookup"><span data-stu-id="937c1-211">Filtered by WAN link type—network-site links, interregional links, and links inside a site</span></span>

  - <span data-ttu-id="937c1-212">с фильтрацией по области сети.</span><span class="sxs-lookup"><span data-stu-id="937c1-212">Filtered by network region</span></span>

<span data-ttu-id="937c1-213">Документация по этому средству можно найти в [документации по средствам для Lync Server 2013 Resource Kit](https://go.microsoft.com/fwlink/?linkid=623245).</span><span class="sxs-lookup"><span data-stu-id="937c1-213">Documentation for this tool is available at [Lync Server 2013 Resource Kit Tools Documentation](https://go.microsoft.com/fwlink/?linkid=623245).</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="937c1-214">См. также</span><span class="sxs-lookup"><span data-stu-id="937c1-214">See Also</span></span>


[<span data-ttu-id="937c1-215">Контрольный список для еженедельных задач</span><span class="sxs-lookup"><span data-stu-id="937c1-215">Weekly task checklist</span></span>](lync-server-2013-operations-checklists.md)  
  

<span data-ttu-id="937c1-216"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="937c1-216"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

