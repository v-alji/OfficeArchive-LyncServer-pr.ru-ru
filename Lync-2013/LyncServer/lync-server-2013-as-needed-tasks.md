---
title: 'Lync Server 2013: задачи, необходимые для выполнения задач'
description: 'Lync Server 2013: задачи, необходимые для выполнения задач.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: As-needed tasks
ms:assetid: b66bc6fe-f138-4cf4-ba7f-aee9a3e0497e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn722431(v=OCS.15)
ms:contentKeyID: 63969643
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 91fe249d9615bb619426c58b22606c3ef182f9a7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440551"
---
# <a name="as-needed-tasks-in-lync-server-2013"></a><span data-ttu-id="7ea99-103">Задачи, необходимые для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7ea99-103">As-needed tasks in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7ea99-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7ea99-104">

<span> </span></span></span>

<span data-ttu-id="7ea99-105">_**Тема последнего изменения:** 2014-08-18_</span><span class="sxs-lookup"><span data-stu-id="7ea99-105">_**Topic Last Modified:** 2014-08-18_</span></span>

<span data-ttu-id="7ea99-106">При необходимости выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="7ea99-106">Perform the following tasks as necessary.</span></span> <span data-ttu-id="7ea99-107">Они часто покрываются в стандартных процедурах:</span><span class="sxs-lookup"><span data-stu-id="7ea99-107">They are frequently also covered by standard procedures:</span></span>

  - <span data-ttu-id="7ea99-108">\* \* Полный аудит безопасности \* \* вы можете регулярно выполнять этот аудит в ответ на обновление или переработание системы обмена сообщениями, а также в ответ на попытку (или успешно) нарушение безопасности.</span><span class="sxs-lookup"><span data-stu-id="7ea99-108">\*\*Full Security Auditing   \*\*You can perform this audit regularly, in response to an upgrade or redesign of the messaging system, or in response to an attempted (or successful) security breach.</span></span> <span data-ttu-id="7ea99-109">Процедура может включать сканирование порта на серверах и брандмауэрах, аудит исправлений системы безопасности и тестов проникновения сторонних разработчиков.</span><span class="sxs-lookup"><span data-stu-id="7ea99-109">The procedure may involve port scans on servers and firewalls, audits of security fixes, and third-party penetration tests.</span></span>

  - <span data-ttu-id="7ea99-110">**Замена сертификатов сроком действия**   Проверка сертификатов в Lync Server — это один из регулярных еженедельных задач, а в процессе процедуры администратор должен иметь запись о сроках действия всех сертификатов.</span><span class="sxs-lookup"><span data-stu-id="7ea99-110">**Replace Certificates about to Expire**   Checking Lync Server Certificates is one of regular weekly tasks, and as part of the procedure an administrator should have a record of all certificates’ expiry dates.</span></span> <span data-ttu-id="7ea99-111">Эта запись позволяет администратору создать уведомление о том, что срок действия определенного сертификата уже истек и заменяется нужным образом.</span><span class="sxs-lookup"><span data-stu-id="7ea99-111">This record enables an administrator to create a notification when a particular certificate is about to be expired and replaced as needed.</span></span>

  - <span data-ttu-id="7ea99-112">**Обновление базовых показателей производительности**   Обновите базовые показатели производительности после обновления или изменения конфигурации.</span><span class="sxs-lookup"><span data-stu-id="7ea99-112">**Updating Performance Baselines**   Update performance baselines after an upgrade or configuration change.</span></span> <span data-ttu-id="7ea99-113">Ваша организация может использовать базовые показатели для измерения изменений производительности и для выявления проблем, влияющих на производительность системы.</span><span class="sxs-lookup"><span data-stu-id="7ea99-113">Your organization can use baselines to measure performance changes and to detect issues that affect system performance.</span></span>

  - <span data-ttu-id="7ea99-114">**Управление корпоративным пулом**   Начальная настройка пулов предприятий, серверов Standard Edition и других серверов в среде Организации была выполнена во время развертывания отдельных серверов.</span><span class="sxs-lookup"><span data-stu-id="7ea99-114">**Managing Enterprise Pool**   Initial configuration of Enterprise pools, Standard Edition servers, and any other servers in your organization's environment were done during deployment of the individual servers.</span></span> <span data-ttu-id="7ea99-115">Ниже перечислены задачи, которые следует выполнять после развертывания серверов и пулов для серверов стандартных выпусков и пулов предприятий.</span><span class="sxs-lookup"><span data-stu-id="7ea99-115">Post-deployment management of servers and pools for Standard Edition servers and Enterprise pools includes the following tasks:</span></span>
    
      - <span data-ttu-id="7ea99-116">Управление серверами переднего плана</span><span class="sxs-lookup"><span data-stu-id="7ea99-116">Managing Front End Servers</span></span>
    
      - <span data-ttu-id="7ea99-117">Управление веб-конференциями</span><span class="sxs-lookup"><span data-stu-id="7ea99-117">Managing Web Conferencing</span></span>
    
      - <span data-ttu-id="7ea99-118">Управление конференциями</span><span class="sxs-lookup"><span data-stu-id="7ea99-118">Managing Conferencing</span></span>
    
      - <span data-ttu-id="7ea99-119">Изменение учетных данных учетной записи службы</span><span class="sxs-lookup"><span data-stu-id="7ea99-119">Changing Service Account Credentials</span></span>
    
      - <span data-ttu-id="7ea99-120">Управление базами данных</span><span class="sxs-lookup"><span data-stu-id="7ea99-120">Managing Databases</span></span>
    
      - <span data-ttu-id="7ea99-121">Запуск и остановка служб и отключение ролей сервера</span><span class="sxs-lookup"><span data-stu-id="7ea99-121">Starting and Stopping Services and Deactivating Server Roles</span></span>
    
      - <span data-ttu-id="7ea99-122">Удаление серверов и ролей сервера, удаление пулов и списание серверов и пулов</span><span class="sxs-lookup"><span data-stu-id="7ea99-122">Removing Servers and Server Roles, Removing Pools, and Decommissioning Servers and Pools</span></span>

  - <span data-ttu-id="7ea99-123">**Управление использованием**   Вы можете настроить Lync Server 2013 для предоставления функциональных возможностей и функций, наиболее подходящих для вашей организации.</span><span class="sxs-lookup"><span data-stu-id="7ea99-123">**Managing Usage**   You can configure Lync Server 2013 to provide the features and functionality that are most appropriate for your organization.</span></span> <span data-ttu-id="7ea99-124">Доступны следующие политики:</span><span class="sxs-lookup"><span data-stu-id="7ea99-124">This includes the following:</span></span>
    
      - <span data-ttu-id="7ea99-125">Управление поддержкой локальных собраний веб-конференций</span><span class="sxs-lookup"><span data-stu-id="7ea99-125">Managing Support for On-Premise Web Conferencing Meetings</span></span>
    
      - <span data-ttu-id="7ea99-126">Управление использованием групп рассылки для отправки мгновенных сообщений</span><span class="sxs-lookup"><span data-stu-id="7ea99-126">Managing the Use of Distribution Groups to Send Instant Messages</span></span>
    
      - <span data-ttu-id="7ea99-127">Управление контактами, присутствием и запросами</span><span class="sxs-lookup"><span data-stu-id="7ea99-127">Managing Contacts, Presence, and Queries</span></span>
    
      - <span data-ttu-id="7ea99-128">Настройка фильтрации клиентских версий</span><span class="sxs-lookup"><span data-stu-id="7ea99-128">Configuring Client Version Filtering</span></span>
    
      - <span data-ttu-id="7ea99-129">Настройка фильтрации интеллектуального обмена мгновенными сообщениями</span><span class="sxs-lookup"><span data-stu-id="7ea99-129">Configuring Intelligent IM Filtering</span></span>
    
      - <span data-ttu-id="7ea99-130">Настройка архивации, записи звонков и соответствия собранию</span><span class="sxs-lookup"><span data-stu-id="7ea99-130">Configuring Archiving, Call Detail Recording, and Meeting Compliance</span></span>

  - <span data-ttu-id="7ea99-131">**Управление подключением пограничного сервера**   Текущее управление серверами и параметрами, необходимыми для обеспечения внешней связи, включает в себя следующее:</span><span class="sxs-lookup"><span data-stu-id="7ea99-131">**Managing Edge Server Connectivity**   Ongoing management of the servers and settings required to provide external connectivity includes the following:</span></span>
    
      - <span data-ttu-id="7ea99-132">Управление подключением между внутренними серверами и пограничными серверами</span><span class="sxs-lookup"><span data-stu-id="7ea99-132">Managing Connectivity between Internal Servers and Edge Servers</span></span>
    
      - <span data-ttu-id="7ea99-133">Настройка внутренних и внешних интерфейсов и сертификатов для пограничных серверов</span><span class="sxs-lookup"><span data-stu-id="7ea99-133">Configuring Internal and External Interfaces and Certificates for Edge Servers</span></span>
    
      - <span data-ttu-id="7ea99-134">Управление доступом к федеративного партнера</span><span class="sxs-lookup"><span data-stu-id="7ea99-134">Managing Federated Partner Access</span></span>

  - <span data-ttu-id="7ea99-135">**Администрирование адресной книги**   Администрирование серверов адресных книг включает в себя следующие возможности:</span><span class="sxs-lookup"><span data-stu-id="7ea99-135">**Administering the Address Book**   Administering Address Book Servers includes the following:</span></span>
    
      - <span data-ttu-id="7ea99-136">Настройка нормализации телефонной книги сервера в адресной книге</span><span class="sxs-lookup"><span data-stu-id="7ea99-136">Configuring Address Book Server phone normalization</span></span>
    
      - <span data-ttu-id="7ea99-137">Управление сервером адресной книги из командной строки</span><span class="sxs-lookup"><span data-stu-id="7ea99-137">Managing the Address Book Server from the command line</span></span>

  - <span data-ttu-id="7ea99-138">**Управление учетными записями пользователей**   Управление учетными записями пользователей включает в себя указанные ниже возможности.</span><span class="sxs-lookup"><span data-stu-id="7ea99-138">**Managing User Accounts**   Management of user accounts includes the following:</span></span>
    
      - <span data-ttu-id="7ea99-139">Включение учетных записей пользователей для Lync Server</span><span class="sxs-lookup"><span data-stu-id="7ea99-139">Enabling User Accounts for Lync Server</span></span>
    
      - <span data-ttu-id="7ea99-140">Настройка пользователей Lync Server с помощью мастера</span><span class="sxs-lookup"><span data-stu-id="7ea99-140">Configuring Lync Server Users using the Wizard</span></span>
    
      - <span data-ttu-id="7ea99-141">Настройка отдельных свойств учетной записи пользователя в Lync Server</span><span class="sxs-lookup"><span data-stu-id="7ea99-141">Configuring Individual Lync Server User Account Properties</span></span>
    
      - <span data-ttu-id="7ea99-142">Поиск пользователей Lync Server</span><span class="sxs-lookup"><span data-stu-id="7ea99-142">Searching for Lync Server Users</span></span>
    
      - <span data-ttu-id="7ea99-143">Перемещение пользователей Lync Server</span><span class="sxs-lookup"><span data-stu-id="7ea99-143">Moving Lync Server Users</span></span>
    
      - <span data-ttu-id="7ea99-144">Удаление пользователей Lync Server</span><span class="sxs-lookup"><span data-stu-id="7ea99-144">Deleting Lync Server Users</span></span>

  - <span data-ttu-id="7ea99-145">**Анализ файлов журнала Lync Server 2013**   Одним из полезных средств, обычно используемых для устранения неполадок, является средство ведения журнала Lync Server 2013, подробно описанное [с помощью средства ведения журнала Lync server 2013](https://technet.microsoft.com/library/gg558599.aspx).</span><span class="sxs-lookup"><span data-stu-id="7ea99-145">**Analyzing Lync Server 2013 Log Files**   One very helpful tool, generally used for troubleshooting, is the Lync Server 2013 Logging Tool described in detail in [Using Lync Server 2013 Logging Tool](https://technet.microsoft.com/library/gg558599.aspx).</span></span>

<span data-ttu-id="7ea99-146">Поскольку средство ведения журнала создает файлы журнала (отдельно для каждого сервера), эти файлы журнала можно просмотреть и проанализировать с помощью средства snooper, если на компьютере установлены средства Microsoft Office Server 12 Resource Kit.</span><span class="sxs-lookup"><span data-stu-id="7ea99-146">Because the Logging Tool generates log files (on a per-server basis), these log files can be viewed and analyzed by using the Snooper tool, if the Microsoft Office Server 12 Resource Kit Tools are installed on the computer.</span></span> <span data-ttu-id="7ea99-147">В противном случае журналы также можно проанализировать с помощью текстового редактора, который значительно менее прозрачен и сложнее, чем использование служебной программы Snooper.</span><span class="sxs-lookup"><span data-stu-id="7ea99-147">Otherwise, logs can also be analyzed by using a text editor, which is much less transparent and more complex than using the Snooper utility.</span></span>

<span data-ttu-id="7ea99-148">Просмотр и анализ сообщений протокола</span><span class="sxs-lookup"><span data-stu-id="7ea99-148">To View and Analyze Protocol Messages</span></span>

<span data-ttu-id="7ea99-149">В средстве ведения журнала после завершения сеанса отладки выберите пункт анализ файлов журнала для просмотра файлов журнала с помощью средства snooper.</span><span class="sxs-lookup"><span data-stu-id="7ea99-149">In the Logging Tool, when you have ended the debug session, click Analyze Log Files to view the log files by using the Snooper tool.</span></span> <span data-ttu-id="7ea99-150">Журналы протоколов можно анализировать для следующих компонентов:</span><span class="sxs-lookup"><span data-stu-id="7ea99-150">You can analyze protocol logs for the following components:</span></span>

  - <span data-ttu-id="7ea99-151">Lync Server SipStack (SIP)</span><span class="sxs-lookup"><span data-stu-id="7ea99-151">Lync Server SipStack (SIP)</span></span>

  - <span data-ttu-id="7ea99-152">Lync Server S4 (SIP)</span><span class="sxs-lookup"><span data-stu-id="7ea99-152">Lync Server S4 (SIP)</span></span>

  - <span data-ttu-id="7ea99-153">Трафик сигналов для конференц-связи Lync Server (C3P), включая MCU бесC3P и Focus C3P</span><span class="sxs-lookup"><span data-stu-id="7ea99-153">Lync Server Conferencing signaling traffic (C3P), including MCU Infra C3P and Focus C3P</span></span>

  - <span data-ttu-id="7ea99-154">Трафик веб-конференций Lync Server (PSOM)</span><span class="sxs-lookup"><span data-stu-id="7ea99-154">Lync Server Web conferencing traffic (PSOM)</span></span>

  - <span data-ttu-id="7ea99-155">Клиент клиентской платформы единой системы обмена сообщениями Lync Server (UCCP)</span><span class="sxs-lookup"><span data-stu-id="7ea99-155">Lync Server Unified Communications Client Platform client (UCCP)</span></span>

  - <span data-ttu-id="7ea99-156">Отчеты об ошибках из базы данных архивации</span><span class="sxs-lookup"><span data-stu-id="7ea99-156">Error reports from the archiving database</span></span>

<span data-ttu-id="7ea99-157">Сведения о том, как выполнять задачи по мере необходимости, можно найти в разделе Контрольный список операций As-Needed.</span><span class="sxs-lookup"><span data-stu-id="7ea99-157">To help organize the performance of as-needed tasks, see As-Needed Operations Checklist.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="7ea99-158">Подробное описание процедур администрирования и управления можно найти в руководстве по администрированию Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="7ea99-158">For detailed administration and management procedures, see the Microsoft Lync Server 2013 Administration Guide.</span></span>



</div>

<div>

## <a name="backup-and-restore-policies-or-configuration-settings"></a><span data-ttu-id="7ea99-159">Резервное копирование (и восстановление) политик или параметров конфигурации</span><span class="sxs-lookup"><span data-stu-id="7ea99-159">Backup (and restore) policies or configuration settings</span></span>

<span data-ttu-id="7ea99-160">Lync Server 2013 обеспечивает резервное копирование и восстановление всей системы.</span><span class="sxs-lookup"><span data-stu-id="7ea99-160">Lync Server 2013 lets you back up and restore the whole system.</span></span> <span data-ttu-id="7ea99-161">IIf, для которого нужно создать резервную копию (и, возможно, удастся восстановить) единственной политики или единственной коллекцией параметров конфигурации, получить соответствующую политику, а затем передать этот объект в командлет Export-Clixml, который сохраняет сведения о политике в виде XML-файла.</span><span class="sxs-lookup"><span data-stu-id="7ea99-161">Iif you want to back up (and then maybe someday restore) a single policy or a single collection of configuration settings, retrieve the appropriate policy, and then pipe that object to the Export-Clixml cmdlet, which saves the policy information as an XML file:</span></span>

`Get-CsClientPolicy -Identity "RedmondClientPolicy" | Export-Clixml -Path C:\Backup\RedmondClientPolicy.xml`

<span data-ttu-id="7ea99-162">Теперь вы можете поэкспериментировать с RedmondClientPolicy и изменить множество параметров.</span><span class="sxs-lookup"><span data-stu-id="7ea99-162">You may now experiment with RedmondClientPolicy and change lots of the settings.</span></span> <span data-ttu-id="7ea99-163">Если вы решите восстановить старую политику, введите:</span><span class="sxs-lookup"><span data-stu-id="7ea99-163">If you decide instead to restore the old policy, enter:</span></span>

`$x = Import-Clixml -Path C:\Backup\RedmondClientPolicy.xml`

`Set-CsClientPolicy -Instance $x`

<span data-ttu-id="7ea99-164">Обратите внимание, что этот подход работает для большинства политик и параметров, но он не будет работать с некоторыми более сложными элементами — элементами, которые содержат несколько подобъектов (например, параметры конфигурации маршрутизации, которые содержат множество отдельных голосовых маршрутов).</span><span class="sxs-lookup"><span data-stu-id="7ea99-164">Note that this approach will work for most policies and settings but it won't work with some of the more complex items—items that contain multiple sub-objects (like routing configuration settings, which contain many separate voice routes).</span></span>

<span data-ttu-id="7ea99-165"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7ea99-165"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

