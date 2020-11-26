---
title: Средства набора ресурсов сохраняемого чата для Lync Server 2013
description: Средства для работы с набором ресурсов для Lync Server 2013 для сохраненного чата.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Lync Server 2013 Persistent Chat Resource Kit Tools
ms:assetid: 7a34d2ba-eb25-4e22-92d1-b9baf81b102c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945599(v=OCS.15)
ms:contentKeyID: 51541423
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 336e81c97da73da47eee654161a7d8d8956f9edb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438422"
---
# <a name="lync-server-2013-persistent-chat-resource-kit-tools"></a><span data-ttu-id="25f3a-103">Средства набора ресурсов сохраняемого чата для Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="25f3a-103">Lync Server 2013 Persistent Chat Resource Kit Tools</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="25f3a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="25f3a-104">

<span> </span></span></span>

<span data-ttu-id="25f3a-105">_**Тема последнего изменения:** 2013-02-24_</span><span class="sxs-lookup"><span data-stu-id="25f3a-105">_**Topic Last Modified:** 2013-02-24_</span></span>

<span data-ttu-id="25f3a-106">Средства набора ресурсов сохраняемый чат для Lync Server 2013 помогают упростить выполнение повседневных задач для ИТ – администраторов, которые развертывают и управляют сервером Lync Server 2013 с сохраненным чат.</span><span class="sxs-lookup"><span data-stu-id="25f3a-106">The Lync Server 2013 Persistent Chat Resource Kit tools help to make routine tasks easier for IT administrators who deploy and manage Lync Server 2013 Persistent Chat Server.</span></span> <span data-ttu-id="25f3a-107">В дополнение к инструкциям по установке в этом разделе описывается назначение каждого инструмента и примеры его использования.</span><span class="sxs-lookup"><span data-stu-id="25f3a-107">In addition to installation instructions, this topic describes the purpose of each tool, and examples of its use.</span></span>

<div>

## <a name="installation-of-the-resource-kit-tools"></a><span data-ttu-id="25f3a-108">Установка средств из набора ресурсов</span><span class="sxs-lookup"><span data-stu-id="25f3a-108">Installation of the Resource Kit Tools</span></span>

<span data-ttu-id="25f3a-109">Чтобы установить Lync Server 2013, средства набора ресурсов, скачайте **PersistentChatReskit.msi**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-109">To install the Lync Server 2013, Resource Kit Tools, download **PersistentChatReskit.msi**.</span></span> <span data-ttu-id="25f3a-110">Запустите **PersistentChatReskit.msi** , чтобы выполнить простую установку.</span><span class="sxs-lookup"><span data-stu-id="25f3a-110">Run **PersistentChatReskit.msi** to do a simple installation.</span></span> <span data-ttu-id="25f3a-111">MSI устанавливает все инструменты, описанные в следующем пути: \\ **Program Files \\ Microsoft Lync Server 2013, \\ Пакет ресурсов** для работы сервера.</span><span class="sxs-lookup"><span data-stu-id="25f3a-111">The .msi installs all the tools in the following path: \\**Program Files\\ Microsoft Lync Server 2013\\Persistent Chat Server Resource Kit**.</span></span> <span data-ttu-id="25f3a-112">Инструменты, представляющие собой автономные исполняемые файлы, находятся непосредственно в этой папке.</span><span class="sxs-lookup"><span data-stu-id="25f3a-112">Tools that are self-contained executables are in this folder.</span></span> <span data-ttu-id="25f3a-113">Инструменты, у которых также есть файлы, находятся в своих вложенных папках.</span><span class="sxs-lookup"><span data-stu-id="25f3a-113">Tools that also have files are in their own subfolders.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="25f3a-114">После установки пакета Lync Server 2013, средства набора ресурсов необходимо установить <STRONG>PsExec.exe</STRONG> и скопировать <STRONG>PsExec.exe</STRONG> по следующему адресу: \\ <STRONG>Program Files \ Microsoft Lync Server 2013, серверный ресурс Kit\ChatStressTool</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="25f3a-114">After installing the Lync Server 2013, Resource Kit Tools, you must install <STRONG>PsExec.exe</STRONG> and copy <STRONG>PsExec.exe</STRONG> to the following path: \\<STRONG>Program Files\ Microsoft Lync Server 2013\Persistent Chat Server Resource Kit\ChatStressTool</STRONG>.</span></span> <span data-ttu-id="25f3a-115">Если вы не копируете <STRONG>PsExec.exe</STRONG>, средство "постоянная стресс чата" вызывает исключение ошибки и не работает должным образом.</span><span class="sxs-lookup"><span data-stu-id="25f3a-115">If you do not copy <STRONG>PsExec.exe</STRONG>, the Persistent Chat Stress Tool will throw an error exception, and not perform correctly.</span></span> <span data-ttu-id="25f3a-116">Перед запуском средства убедитесь в том, что вы отвечаете этим требованиям предварительной версии.</span><span class="sxs-lookup"><span data-stu-id="25f3a-116">Make sure that you meet this prerequisite requirement prior to running the tool.</span></span> <span data-ttu-id="25f3a-117">Подробнее об установке <STRONG>PsExec.exe</STRONG>можно найти в разделе <A href="https://go.microsoft.com/fwlink/p/?linkid=282246">https://go.microsoft.com/fwlink/p/?LinkId=282246</A> .</span><span class="sxs-lookup"><span data-stu-id="25f3a-117">For details about installing <STRONG>PsExec.exe</STRONG>, see <A href="https://go.microsoft.com/fwlink/p/?linkid=282246">https://go.microsoft.com/fwlink/p/?LinkId=282246</A>.</span></span>



</div>

</div>

<div>

## <a name="supported-environments"></a><span data-ttu-id="25f3a-118">Поддерживаемые среды</span><span class="sxs-lookup"><span data-stu-id="25f3a-118">Supported Environments</span></span>

<span data-ttu-id="25f3a-119">Для оптимальной производительности в Lync Server 2013 вы сможете установить средства набора ресурсов в той же среде и те же спецификации, которые необходимы для Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="25f3a-119">For optimal performance, the Lync Server 2013, Resource Kit Tools should be installed in the same environment and with the same specifications that are required for Lync Server 2013.</span></span>

</div>

<div>

## <a name="resource-kit-tools-overview"></a><span data-ttu-id="25f3a-120">Обзор средств из набора ресурсов</span><span class="sxs-lookup"><span data-stu-id="25f3a-120">Resource Kit Tools Overview</span></span>

<span data-ttu-id="25f3a-121">Ниже приведены средства, доступные в наборе ресурсов для работы с пакетом Resource Chat для Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="25f3a-121">Here are the tools that are provided in the Lync Server 2013 Persistent Chat Resource Kit.</span></span> <span data-ttu-id="25f3a-122">В следующем разделе представлено описание всех инструментов, в том числе требования и использование примера использования.</span><span class="sxs-lookup"><span data-stu-id="25f3a-122">The following section provides a description of each tool, including requirements and example usage.</span></span>

  - <span data-ttu-id="25f3a-123">AffCheck</span><span class="sxs-lookup"><span data-stu-id="25f3a-123">AffCheck</span></span>

  - <span data-ttu-id="25f3a-124">ChatMonitoringSummary</span><span class="sxs-lookup"><span data-stu-id="25f3a-124">ChatMonitoringSummary</span></span>

  - <span data-ttu-id="25f3a-125">Инструмент ChatStress</span><span class="sxs-lookup"><span data-stu-id="25f3a-125">ChatStress Tool</span></span>

  - <span data-ttu-id="25f3a-126">ChatUpgradeVerifier</span><span class="sxs-lookup"><span data-stu-id="25f3a-126">ChatUpgradeVerifier</span></span>

  - <span data-ttu-id="25f3a-127">ChatUsageReport</span><span class="sxs-lookup"><span data-stu-id="25f3a-127">ChatUsageReport</span></span>

  - <span data-ttu-id="25f3a-128">ScheduleADSyncforPrincipal</span><span class="sxs-lookup"><span data-stu-id="25f3a-128">ScheduleADSyncforPrincipal</span></span>

</div>

<div>

## <a name="affcheck"></a><span data-ttu-id="25f3a-129">AffCheck</span><span class="sxs-lookup"><span data-stu-id="25f3a-129">AffCheck</span></span>

<div>

## <a name="description"></a><span data-ttu-id="25f3a-130">Описание</span><span class="sxs-lookup"><span data-stu-id="25f3a-130">Description</span></span>

<span data-ttu-id="25f3a-131">Средство AffCheck подтверждает, что записи, заданные пользователем базы данных и принадлежности к группе, совпадают с учетными записями доменных служб Active Directory.</span><span class="sxs-lookup"><span data-stu-id="25f3a-131">The AffCheck tool confirms that the Persistent Chat back-end database user and group affiliation records match that of Active Directory Domain Services.</span></span>

</div>

<div>

## <a name="requirements"></a><span data-ttu-id="25f3a-132">Требования</span><span class="sxs-lookup"><span data-stu-id="25f3a-132">Requirements</span></span>

<span data-ttu-id="25f3a-133">Средство устанавливается вместе с установщиком PersistentChatResKit на компьютере, подключенном к домену.</span><span class="sxs-lookup"><span data-stu-id="25f3a-133">The tool is installed with the PersistentChatResKit installer on a domain joined machine.</span></span>

<span data-ttu-id="25f3a-134">Учетная запись пользователя, от имени которой запускается средство, должна иметь доступ на чтение к сохраняемой резервной базе данных чата и доменным службам Active Directory.</span><span class="sxs-lookup"><span data-stu-id="25f3a-134">The user account under which the tool is run must have Read access to the Persistent Chat back-end database and Active Directory Domain Services.</span></span>

</div>

<div>

## <a name="usage"></a><span data-ttu-id="25f3a-135">Режим</span><span class="sxs-lookup"><span data-stu-id="25f3a-135">Usage</span></span>

<span data-ttu-id="25f3a-136">Настройте файл AffCheck.exe.config в соответствии с инструкциями в файле конфигурации и запустите средство AffCheck без параметров командной строки.</span><span class="sxs-lookup"><span data-stu-id="25f3a-136">Configure the AffCheck.exe.config file according to the instructions in the config file and run the AffCheck tool without command-line parameters.</span></span> <span data-ttu-id="25f3a-137">Ниже приведено содержимое AffCheck.exe.config по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="25f3a-137">Following are the contents of the default AffCheck.exe.config.</span></span>

<span data-ttu-id="25f3a-138">**AffCheck.exe.config:**</span><span class="sxs-lookup"><span data-stu-id="25f3a-138">**AffCheck.exe.config:**</span></span>

```XML
    <?xml version="1.0" encoding="utf-8" ?>
    <configuration>
      <appSettings>
        <!--Domain Controller IP Address-->
        <add key="LDAP" value="LDAP://0.0.0.0/"/>
        
        <!-- Domain DN  This is case sensitive, it must match exactly-->
        <add key="DomainComponent" value ="DC=DOMAIN,DC=COM"/>
        
        <!--Domain Administrator Login and Password-->
        <add key="DomainLogin" value="DOMAIN\Administrator"/>
        <add key="DomainPassword" value ="password"/>
        
        <!-- Connection string to Group Chat Database-->
        <add key="ConnectionString" value="data source=SQL_SERVER\INSTANCE;initial catalog=DATABASE_NAME;integrated security=SSPI"/>
        
        <!--Check group affiliations-->
        <add key="CheckGroups" value="true"/>
        
        <!--Check user affilations-->
        <add key="CheckUsers" value="true"/>
        
        <!--List all affiliations if there is a mismatch between database and active directory-->
        <add key="ListAffiliations" value="true"/>
    
        <!--If you need to offset the results of the number of affilations in AD(can be negative to add to AD parent count)-->
        <add key="Offset" value ="0"/>
    
        <!--If you need to ignore certain parents, provide a semi colon delimitted list.-->
        <add key="Ignore" value ="DC=uatest,DC=test,DC=contoso,DC=com;DC=test,DC=contoso,DC=com"/>
      </appSettings>
    </configuration>
  ```
</div>

</div>

<div>

## <a name="chatmonitoringsummary"></a><span data-ttu-id="25f3a-139">ChatMonitoringSummary</span><span class="sxs-lookup"><span data-stu-id="25f3a-139">ChatMonitoringSummary</span></span>

<div>

## <a name="description"></a><span data-ttu-id="25f3a-140">Описание</span><span class="sxs-lookup"><span data-stu-id="25f3a-140">Description</span></span>

<span data-ttu-id="25f3a-141">Средство PersistentChatMonitoringSummary перемещает сохраняемые данные чата из базы данных мониторинга в указанный файл журнала CSV.</span><span class="sxs-lookup"><span data-stu-id="25f3a-141">The PersistentChatMonitoringSummary tool moves Persistent Chat monitoring information from the monitoring database into a specified CSV log file.</span></span>

<span data-ttu-id="25f3a-142">CSV-файл содержит подразделение сеансов сохраняемого чата на общее количество сеансов, успешные сеансы, непредвиденные сбои, ожидаемые ошибки и разделение на непредвиденные сбои с помощью идентификатора диагностики, количества сбоев и описания сбоя.</span><span class="sxs-lookup"><span data-stu-id="25f3a-142">The CSV file will contain a breakdown of Persistent Chat sessions by number of total sessions, successful sessions, unexpected failures, expected failures, and a breakdown of the unexpected failures by diagnostic ID, number of failures, and failure description.</span></span>

</div>

<div>

## <a name="requirements"></a><span data-ttu-id="25f3a-143">Требования</span><span class="sxs-lookup"><span data-stu-id="25f3a-143">Requirements</span></span>

<span data-ttu-id="25f3a-144">Установите средства набора ресурсов сохраняемого чата на компьютере, подключенном к домену, который имеет доступ к базе данных мониторинга.</span><span class="sxs-lookup"><span data-stu-id="25f3a-144">Install the Persistent Chat Resource Kit tools on a domain-joined machine that has access to the Monitoring database.</span></span>

<span data-ttu-id="25f3a-145">Учетная запись пользователя, под которой запускается средство, должна иметь доступ на чтение к базе данных мониторинга.</span><span class="sxs-lookup"><span data-stu-id="25f3a-145">The user account under which the tool runs must have Read access to the Monitoring database.</span></span>

<span data-ttu-id="25f3a-146">Файл PersistentChatMonitoringSummary.exe.config должен содержать \<connectionStrings\> раздел, который определяет строку подключения к базе данных мониторинга.</span><span class="sxs-lookup"><span data-stu-id="25f3a-146">The file, PersistentChatMonitoringSummary.exe.config, must contain a \<connectionStrings\> section that defines the connection string to the Monitoring database.</span></span> <span data-ttu-id="25f3a-147">Оно также должно содержать ключ для PersistentChatEndpointUri, для которого будут собираться данные мониторинга, и путь к файлу для CSV-файла, который будет создан.</span><span class="sxs-lookup"><span data-stu-id="25f3a-147">It must also contain a key for the PersistentChatEndpointUri that the monitoring data will be gathered for, and a file path to a location for the CSV file that will be generated.</span></span> <span data-ttu-id="25f3a-148">Ознакомьтесь с примерами установленного файла конфигурации.</span><span class="sxs-lookup"><span data-stu-id="25f3a-148">Refer to the installed config file for examples.</span></span> <span data-ttu-id="25f3a-149">Файл должен находиться в той же папке, что и инструмент.</span><span class="sxs-lookup"><span data-stu-id="25f3a-149">The file must be located in the same directory as the tool.</span></span>

</div>

<div>

## <a name="usage"></a><span data-ttu-id="25f3a-150">Режим</span><span class="sxs-lookup"><span data-stu-id="25f3a-150">Usage</span></span>

```Batch
    PersistentChatMonitoringSummary [-StartDateTime <date>] [-EndDateTime <date>]
```

<span data-ttu-id="25f3a-151">Эти параметры определяют выбор данных:</span><span class="sxs-lookup"><span data-stu-id="25f3a-151">These parameters define the selection of data:</span></span>

<span data-ttu-id="25f3a-152">**StartDateTime:** При необходимости указывается дата начала периода выбора.</span><span class="sxs-lookup"><span data-stu-id="25f3a-152">**StartDateTime:** Optionally specifies the start date of the selection period.</span></span> <span data-ttu-id="25f3a-153">По умолчанию: 1/1/1753 12:00:00 AM</span><span class="sxs-lookup"><span data-stu-id="25f3a-153">Default: 1/1/1753 12:00:00 AM</span></span>

<span data-ttu-id="25f3a-154">**EndDateTime:** Дополнительно определяет последнюю дату периода выбора.</span><span class="sxs-lookup"><span data-stu-id="25f3a-154">**EndDateTime:** Optionally specifies the last date of the selection period.</span></span> <span data-ttu-id="25f3a-155">По умолчанию: Now</span><span class="sxs-lookup"><span data-stu-id="25f3a-155">Default: Now</span></span>

</div>

<div>

## <a name="example"></a><span data-ttu-id="25f3a-156">Пример</span><span class="sxs-lookup"><span data-stu-id="25f3a-156">Example</span></span>

```Batch
    C:\Users\Administrator.VDOMAIN>Desktop\PersistentChatMonitoringSummary.exe
    Reading database connection information, Persistent Chat endpoint uri, and csv output path information from the application config file...
    Connecting to Monitoring database with connection string specified in the application config file...
    Gathering Persistent Chat Session Summary information between "1/1/1753 12:00:00 AM" and "11/19/2012 10:11:25 AM" for Persistent Chat Endpoint Uri "persistentChatEndpointUri@domain.com"...
    Press enter to continue or hit ctr-c if these settings are incorrect...
    
    The summary information about Persistent Chat sessions from the Monitoring database has been output to C:\PersistentChatMonitoring_dd4ace24-4c8a-4a3d-8fd4-591bdfacf47b.csv
    Press enter to exit...
```

</div>

</div>

<div>

## <a name="persistent-chat-stress-tool"></a><span data-ttu-id="25f3a-157">Инструмент «стресс» сохраняемого чата</span><span class="sxs-lookup"><span data-stu-id="25f3a-157">Persistent Chat Stress Tool</span></span>

<div>

## <a name="description"></a><span data-ttu-id="25f3a-158">Описание</span><span class="sxs-lookup"><span data-stu-id="25f3a-158">Description</span></span>

<span data-ttu-id="25f3a-159">Инструмент «стресс» сохраняемый чат обеспечивает простой способ моделирования использования сохраняемого чата для тестирования реальной производительности, включая различные пользовательские модели, чтобы лучше соответствовать ожидаемым сценариям использования.</span><span class="sxs-lookup"><span data-stu-id="25f3a-159">The Persistent Chat Stress tool provides an easy way to simulate usage of Persistent Chat to test real-world performance, including varied user models to better fit your expected usage scenarios.</span></span>

</div>

<div>

## <a name="requirements"></a><span data-ttu-id="25f3a-160">Требования</span><span class="sxs-lookup"><span data-stu-id="25f3a-160">Requirements</span></span>

<span data-ttu-id="25f3a-161">Установите средства набора ресурсов сохраняемого чата на компьютер, подключенный к домену, который имеет доступ к сохраняемой резервной базе данных чата.</span><span class="sxs-lookup"><span data-stu-id="25f3a-161">Install the Persistent Chat Resource Kit tools onto a domain-joined machine that has access to the Persistent Chat back-end database.</span></span>

<span data-ttu-id="25f3a-162">В дополнение к этому компьютеру *контроллера* вам понадобятся несколько машин *Loader* .</span><span class="sxs-lookup"><span data-stu-id="25f3a-162">In addition to this *controller* machine, you will need several *loader* machines.</span></span> <span data-ttu-id="25f3a-163">Для каждых 10 000 пользователей в пользовательской модели вам понадобится не менее 4 ГБ оперативной памяти на машине загрузчика.</span><span class="sxs-lookup"><span data-stu-id="25f3a-163">For every 10K users in your user model, you will need at least 4GB of free RAM on a loader machine.</span></span> <span data-ttu-id="25f3a-164">Например, для работы с пользователями 80K потребуется около 32 ГБ ОЗУ на всех машинах загрузчика.</span><span class="sxs-lookup"><span data-stu-id="25f3a-164">For example, a run with 80K users will require about 32GB of RAM spread across all loader machines.</span></span> <span data-ttu-id="25f3a-165">Мы рекомендуем использовать как минимум три компьютера загрузчика, независимо от ожидаемой нагрузки.</span><span class="sxs-lookup"><span data-stu-id="25f3a-165">We recommend that you have at least three loader machines, regardless of expected load.</span></span>

<span data-ttu-id="25f3a-166">На компьютерах загрузчика должна быть установлена платформа .NET 4,5, а также распространяемый компонент Visual C++ 2012.</span><span class="sxs-lookup"><span data-stu-id="25f3a-166">Loader machines must have the .NET 4.5 Framework as well as the Visual C++ 2012 Redistributable installed.</span></span>

</div>

<div>

## <a name="configuration"></a><span data-ttu-id="25f3a-167">Конфигурация</span><span class="sxs-lookup"><span data-stu-id="25f3a-167">Configuration</span></span>

<span data-ttu-id="25f3a-168">Скопируйте файлы ChatStressTool в общую папку, доступную на всех машинах загрузчика.</span><span class="sxs-lookup"><span data-stu-id="25f3a-168">Copy ChatStressTool files into a shared folder accessible from all loader machines.</span></span>

<span data-ttu-id="25f3a-169">Создание пользователей и каналов для использования в нагрузочном прогоне.</span><span class="sxs-lookup"><span data-stu-id="25f3a-169">Create users and channels for use in the stress run:</span></span>

  - <span data-ttu-id="25f3a-170">Создавайте как можно больше пользователей, для которых используется модель пользователя, включите их в Lync и установите для них параметр "сохраняемая политика чата".</span><span class="sxs-lookup"><span data-stu-id="25f3a-170">Create as many users as your user model calls for, enable them for Lync, and set their Persistent Chat policy to Enabled.</span></span>

  - <span data-ttu-id="25f3a-171">Создайте категорию для каналов стресс-, а затем создайте столько комнат, сколько необходимо для этой категории.</span><span class="sxs-lookup"><span data-stu-id="25f3a-171">Create a category for your stress channels, and then create as many rooms as are needed under that category.</span></span> <span data-ttu-id="25f3a-172">У категории должны быть все повременные пользователи в списке **разрешенных** пользователей (с учетом их подразделений), а в помещениях для нагрузки должны быть установлены параметры конфиденциальности **Open**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-172">The category should have all stress users in its **Allowed** list (by way of adding their OU), and stress rooms should have a privacy setting of **Open**.</span></span>

  - <span data-ttu-id="25f3a-173">Мы рекомендуем создавать дополнительные помещения для нагрузки.</span><span class="sxs-lookup"><span data-stu-id="25f3a-173">We recommend creating extra stress rooms.</span></span> <span data-ttu-id="25f3a-174">Для создания комнат 50 000 можно использовать следующую команду интерфейса командной строки Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="25f3a-174">You can create 50,000 rooms with the following Windows PowerShell command-line interface command:</span></span>
    ```Powershell
        for ($i = 0; $i -le 50000; $i++) { New-CsPersistentChatRoom -Category <parent category> -Name "StressChan_$i" -Privacy Open }
    ```    

<span data-ttu-id="25f3a-175">Измените файлы конфигурации в соответствии с вашей топологией.</span><span class="sxs-lookup"><span data-stu-id="25f3a-175">Edit the configuration files to fit your topology:</span></span>

<span data-ttu-id="25f3a-176">В **LoaderProcess.exe.config** замените значение "Controller.contoso.com" на полное доменное имя (FQDN) контроллера компьютера.</span><span class="sxs-lookup"><span data-stu-id="25f3a-176">In **LoaderProcess.exe.config**, change “controller.contoso.com” to the controller machine’s fully qualified domain name (FQDN).</span></span>

<span data-ttu-id="25f3a-177">В **StressLauncher.exe.config:**</span><span class="sxs-lookup"><span data-stu-id="25f3a-177">In **StressLauncher.exe.config:**</span></span>

1.  <span data-ttu-id="25f3a-178">Измените значение параметра "LoaderBinary" на путь к общей папке.</span><span class="sxs-lookup"><span data-stu-id="25f3a-178">Change the “LoaderBinary” setting value to the shared folder’s path.</span></span>

2.  <span data-ttu-id="25f3a-179">Измените "AdminUser"/"AdminPassword" на учетные данные, которые имеют административный доступ к компьютерам загрузчика.</span><span class="sxs-lookup"><span data-stu-id="25f3a-179">Change “AdminUser”/”AdminPassword” to credentials that have admin access to loader machines.</span></span>

3.  <span data-ttu-id="25f3a-180">Измените "ChannelCategory" на название категории, для которой созданы каналы нагрузки.</span><span class="sxs-lookup"><span data-stu-id="25f3a-180">Change “ChannelCategory” to the name of the category that stress channels have been created under.</span></span>

4.  <span data-ttu-id="25f3a-181">Измените "UserNamePattern" и "UserPasswordPattern" на шаблон, соответствующий вашим учетным данным пользователя.</span><span class="sxs-lookup"><span data-stu-id="25f3a-181">Change “UserNamePattern” and “UserPasswordPattern” to a template that matches your stress user credentials.</span></span> <span data-ttu-id="25f3a-182">{0} заменяется номером индекса пользователя.</span><span class="sxs-lookup"><span data-stu-id="25f3a-182">{0} is replaced with the user’s index number.</span></span>

5.  <span data-ttu-id="25f3a-183">Замените слово Domain на домен SIP для топологии тестирования.</span><span class="sxs-lookup"><span data-stu-id="25f3a-183">Change “Domain” to the SIP domain of your test topology.</span></span>

6.  <span data-ttu-id="25f3a-184">Измените "ConnectionString" на строку подключения для сохраняемой серверной базы данных чата.</span><span class="sxs-lookup"><span data-stu-id="25f3a-184">Change “ConnectionString” to a connection string for your Persistent Chat back-end database.</span></span>

7.  <span data-ttu-id="25f3a-185">Замените значение "UserIndexStart" индексом первого пользователя, который повлияет на погрузку.</span><span class="sxs-lookup"><span data-stu-id="25f3a-185">Change “UserIndexStart” to the index of the first stress user.</span></span>

8.  <span data-ttu-id="25f3a-186">Измените значение "LyncFQDN" на полное доменное имя пула переднего плана.</span><span class="sxs-lookup"><span data-stu-id="25f3a-186">Change “LyncFQDN” to the FQDN of your Front End pool.</span></span>

9.  <span data-ttu-id="25f3a-187">Измените список "machines", чтобы включить имена компьютеров для всех компьютеров загрузчика.</span><span class="sxs-lookup"><span data-stu-id="25f3a-187">Modify the “Machines” list to include machine names for all of your loader machines.</span></span>

10. <span data-ttu-id="25f3a-188">Измените значение baseAddress конечной точки службы (по умолчанию — "controller.contoso.com") до полного доменного имени компьютера контроллера.</span><span class="sxs-lookup"><span data-stu-id="25f3a-188">Change the baseAddress of the service endpoint (default is “controller.contoso.com”) to the FQDN of your controller machine.</span></span>

</div>

<div>

## <a name="usage"></a><span data-ttu-id="25f3a-189">Режим</span><span class="sxs-lookup"><span data-stu-id="25f3a-189">Usage</span></span>

<span data-ttu-id="25f3a-190">После завершения настройки откройте StressLauncher.exe на компьютере контроллера.</span><span class="sxs-lookup"><span data-stu-id="25f3a-190">After configuration is complete, open StressLauncher.exe on the controller machine.</span></span> <span data-ttu-id="25f3a-191">Вы можете запустить StressLauncher как любой пользователь.</span><span class="sxs-lookup"><span data-stu-id="25f3a-191">You can launch StressLauncher as any user.</span></span> <span data-ttu-id="25f3a-192">Учетные данные, под которыми запускается процесс загрузчика на компьютерах загрузчика, должны быть указаны в файле конфигурации.</span><span class="sxs-lookup"><span data-stu-id="25f3a-192">The credentials under which the loader processes start on the loader machines must be specified in the config file.</span></span> <span data-ttu-id="25f3a-193">Кроме того, необходимо предоставить строку подключения, которая имеет доступ на чтение к сохраняемой серверной базе данных чата.</span><span class="sxs-lookup"><span data-stu-id="25f3a-193">You also must give a connection string that has Read access to the Persistent Chat back-end database.</span></span> <span data-ttu-id="25f3a-194">Если строка подключения использует встроенную проверку подлинности Windows, необходимо запустить StressLauncher как пользователя с этим доступом.</span><span class="sxs-lookup"><span data-stu-id="25f3a-194">If this connection string uses integrated Windows authentication, you must launch StressLauncher as a user that has this access.</span></span>

<span data-ttu-id="25f3a-195">При необходимости измените параметры пользовательской модели.</span><span class="sxs-lookup"><span data-stu-id="25f3a-195">Alter the user model settings as needed.</span></span> <span data-ttu-id="25f3a-196">Нажмите кнопку **начать загрузку** , чтобы начать выполнение.</span><span class="sxs-lookup"><span data-stu-id="25f3a-196">Click **Start Load** to initiate a run.</span></span> <span data-ttu-id="25f3a-197">После минуты пользователь начнет вход в систему, а индикатор выполнения начнет заполняться.</span><span class="sxs-lookup"><span data-stu-id="25f3a-197">After a minute or so, users will start being signed in, and the progress bar will begin to fill.</span></span> <span data-ttu-id="25f3a-198">На этом этапе вы можете использовать контроллеры компьютера и получить измерения производительности.</span><span class="sxs-lookup"><span data-stu-id="25f3a-198">At this point, you may can the controller machine working and take performance measurements.</span></span>

</div>

</div>

<div>

## <a name="chatupgradeverifier"></a><span data-ttu-id="25f3a-199">ChatUpgradeVerifier</span><span class="sxs-lookup"><span data-stu-id="25f3a-199">ChatUpgradeVerifier</span></span>

<div>

## <a name="description"></a><span data-ttu-id="25f3a-200">Описание</span><span class="sxs-lookup"><span data-stu-id="25f3a-200">Description</span></span>

<span data-ttu-id="25f3a-201">ChatUpgradeVerifier — это специальный инструмент для сравнения баз данных в чате.</span><span class="sxs-lookup"><span data-stu-id="25f3a-201">ChatUpgradeVerifier is a Persistent Chat specific database comparison tool.</span></span> <span data-ttu-id="25f3a-202">Это средство сравнивает базу данных группового чата 2007 R2 или Group Chat 2010 (2007/2010Db) с базой данных сохраняемого чата 2013 (2013Db).</span><span class="sxs-lookup"><span data-stu-id="25f3a-202">The tool compares either the Group Chat 2007 R2 or Group Chat 2010 Database (2007/2010Db) to the Persistent Chat 2013 Database (2013Db).</span></span>

<span data-ttu-id="25f3a-203">Это средство проверит, отображается ли оно на одной категории, в области "сохраняемый чат", а надстройка в выпуске в Office 2007 или 2010Db.</span><span class="sxs-lookup"><span data-stu-id="25f3a-203">The tool will check, one by one, each category, Persistent Chat room, and add-in in 2007/2010Db to see if it appears in the 2013Db.</span></span> <span data-ttu-id="25f3a-204">Сравнение включает проверку всех параметров в категории, комнаты чата или надстройки, любые участники в области в этой категории и любые участники роли в этой категории либо в комнате чата.</span><span class="sxs-lookup"><span data-stu-id="25f3a-204">The comparison includes checking all settings on the category, chat room, or add-in, any principals in scope on the category, and any principal in a role on either the category or the chat room.</span></span> <span data-ttu-id="25f3a-205">Если категория или комната чата не отображаются должным образом в 2013Db, эти различия будут выводиться в файл конфликтов.</span><span class="sxs-lookup"><span data-stu-id="25f3a-205">If a category or a chat room does not appear correctly in the 2013Db, the differences will be output to a conflicts file.</span></span> <span data-ttu-id="25f3a-206">Если после завершения обновления Office 2007 или 2010Db изменится, а затем запускается это средство, в файле конфликтов будет выводиться разница.</span><span class="sxs-lookup"><span data-stu-id="25f3a-206">If, after the upgrade has occurred, the 2007/2010Db is changed and then this tool is run, there will be a differences output to the conflicts file.</span></span> <span data-ttu-id="25f3a-207">Обратите внимание, что это приложение является только средством сравнения баз данных и не проверяет процесс обновления.</span><span class="sxs-lookup"><span data-stu-id="25f3a-207">Note that this application is a database comparison tool only and does not validate the upgrade process.</span></span>

</div>

<div>

## <a name="requirements"></a><span data-ttu-id="25f3a-208">Требования</span><span class="sxs-lookup"><span data-stu-id="25f3a-208">Requirements</span></span>

<span data-ttu-id="25f3a-209">Установка средств набора ресурсов сохраняемого чата на компьютере, подключенном к домену, который имеет доступ к сохраняемым внутренним базам данных чата (предыдущим и текущим версиям для сохраняемого чата).</span><span class="sxs-lookup"><span data-stu-id="25f3a-209">Install the Persistent Chat Resource Kit tools on a domain-joined machine that has access to the Persistent Chat back-end databases (previous and current versions for Persistent Chat).</span></span>

<span data-ttu-id="25f3a-210">Учетная запись пользователя, с помощью которой запускается средство, должна иметь доступ на чтение к базам данных сохраняемого чата.</span><span class="sxs-lookup"><span data-stu-id="25f3a-210">The user account under which the tool runs must have Read access to the Persistent Chat databases.</span></span>

<span data-ttu-id="25f3a-211">Файл ChatUpgradeVerifier.exe.config должен содержать либо параметр GroupChat2007R2Db, либо параметр GroupChat2010Db со строкой подключения к соответствующей базе данных группового чата (Groupchat 2007R2 или 2010).</span><span class="sxs-lookup"><span data-stu-id="25f3a-211">The ChatUpgradeVerifier.exe.config file must contain either the GroupChat2007R2Db parameter or the GroupChat2010Db parameter, with a connection string to the appropriate Group Chat database (either Groupchat 2007R2 or 2010).</span></span> <span data-ttu-id="25f3a-212">Кроме того, он должен содержать параметр PersistentChat2013Db со строкой соединения с базой данных сохраняемого чата-2013.</span><span class="sxs-lookup"><span data-stu-id="25f3a-212">It must also contain a PersistentChat2013Db parameter, with a connection string to the Persistent Chat 2013 database.</span></span>

</div>

<div>

## <a name="usage"></a><span data-ttu-id="25f3a-213">Режим</span><span class="sxs-lookup"><span data-stu-id="25f3a-213">Usage</span></span>

<span data-ttu-id="25f3a-214">Запустите **ChatUpgradeVerifier** без каких бы то ни было параметров.</span><span class="sxs-lookup"><span data-stu-id="25f3a-214">Run **ChatUpgradeVerifier** without any parameters.</span></span>

</div>

<div>

## <a name="example"></a><span data-ttu-id="25f3a-215">Пример</span><span class="sxs-lookup"><span data-stu-id="25f3a-215">Example</span></span>

<span data-ttu-id="25f3a-216">![Запуск ChatUpgradeVerifier.exe.](images/JJ945599.4c273bc3-7926-47c7-ade7-34522721ebf9(OCS.15).jpg "Запуск ChatUpgradeVerifier.exe.")</span><span class="sxs-lookup"><span data-stu-id="25f3a-216">![Running ChatUpgradeVerifier.exe.](images/JJ945599.4c273bc3-7926-47c7-ade7-34522721ebf9(OCS.15).jpg "Running ChatUpgradeVerifier.exe.")</span></span>

</div>

</div>

<div>

## <a name="persistent-chat-usage-report"></a><span data-ttu-id="25f3a-217">Отчет об использовании сохраняемого чата</span><span class="sxs-lookup"><span data-stu-id="25f3a-217">Persistent Chat Usage Report</span></span>

<div>

## <a name="description"></a><span data-ttu-id="25f3a-218">Описание</span><span class="sxs-lookup"><span data-stu-id="25f3a-218">Description</span></span>

<span data-ttu-id="25f3a-219">Средство ChatUsageReport создает HTML-отчет по использованию службы сохраняемого чата.</span><span class="sxs-lookup"><span data-stu-id="25f3a-219">The ChatUsageReport tool generates an HTML report of Persistent Chat service usage.</span></span>

</div>

<div>

## <a name="requirements"></a><span data-ttu-id="25f3a-220">Требования</span><span class="sxs-lookup"><span data-stu-id="25f3a-220">Requirements</span></span>

<span data-ttu-id="25f3a-221">Установите средства набора ресурсов сохраняемого чата на компьютере, подключенном к домену, который имеет доступ к сохраняемой резервной базе данных чата.</span><span class="sxs-lookup"><span data-stu-id="25f3a-221">Install the Persistent Chat Resource Kit tools on a domain-joined machine that has access to the Persistent Chat back-end database.</span></span>

<span data-ttu-id="25f3a-222">Учетная запись пользователя, с помощью которой запускается инструмент, должна иметь доступ на чтение к сохраняемой обратной стороне чата.</span><span class="sxs-lookup"><span data-stu-id="25f3a-222">The user account under which the tool is run must have Read access to the Persistent Chat back-end database.</span></span>

<span data-ttu-id="25f3a-223">Файл ChatUsageReport.exe.config должен содержать \<connectionStrings\> раздел, определяющий строку подключения для сохраняемой серверной базы данных чата.</span><span class="sxs-lookup"><span data-stu-id="25f3a-223">The file, ChatUsageReport.exe.config, must contain a \<connectionStrings\> section defining the connection string to the Persistent Chat back-end database.</span></span> <span data-ttu-id="25f3a-224">Содержимое файла конфигурации по умолчанию включается здесь для ссылки.</span><span class="sxs-lookup"><span data-stu-id="25f3a-224">The contents of the default config file are included here, for your reference.</span></span>

</div>

<div>

## <a name="usage"></a><span data-ttu-id="25f3a-225">Режим</span><span class="sxs-lookup"><span data-stu-id="25f3a-225">Usage</span></span>

```Powershell
    ChatUsageReport [-StartDate {date}] [-EndDate {date}] [-TopActiveUsers {n}] [-TopActiveRooms {n}] [-LeastActiveRooms {n}] [-RoomsInactiveSince {Date}] [-OutputFolder {path}]
```
<span data-ttu-id="25f3a-226">Эти параметры определяют выбор данных:</span><span class="sxs-lookup"><span data-stu-id="25f3a-226">These parameters define the selection of data:</span></span>

<span data-ttu-id="25f3a-227">**StartDate (Дата** начала): При необходимости определяет дату начала периода выбора в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="25f3a-227">**StartDate:** Optionally specifies the UTC start date of the selection period.</span></span> <span data-ttu-id="25f3a-228">По умолчанию: ранняя дата</span><span class="sxs-lookup"><span data-stu-id="25f3a-228">Default: Earliest Date</span></span>

<span data-ttu-id="25f3a-229">**Дата окончания:** При необходимости определяет дату окончания периода выбора в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="25f3a-229">**EndDate:** Optionally specifies the UTC end date of the selection period.</span></span> <span data-ttu-id="25f3a-230">По умолчанию: Now</span><span class="sxs-lookup"><span data-stu-id="25f3a-230">Default: Now</span></span>

<span data-ttu-id="25f3a-231">Эти параметры определяют, как и какие данные отображаются.</span><span class="sxs-lookup"><span data-stu-id="25f3a-231">These parameters define how and what data is displayed:</span></span>

<span data-ttu-id="25f3a-232">**TopActiveUsers:** Если указан этот параметр, в отчет будут включены n наиболее активных пользователей в соответствии с количеством сообщений, опубликованных пользователем в комнате чата в течение выбранного периода.</span><span class="sxs-lookup"><span data-stu-id="25f3a-232">**TopActiveUsers:** If this is specified, the report will include the n most active users in terms of the number of messages the user has posted in the chat room for the selected period.</span></span> <span data-ttu-id="25f3a-233">По умолчанию: 10</span><span class="sxs-lookup"><span data-stu-id="25f3a-233">Default: 10</span></span>

<span data-ttu-id="25f3a-234">**TopActiveRooms:** Если указан этот параметр, в отчет будут включены n самых активных комнат чата в соответствии с количеством сообщений, опубликованных в комнате за выбранный период.</span><span class="sxs-lookup"><span data-stu-id="25f3a-234">**TopActiveRooms:** If this is specified, the report will include the n most active chat rooms in terms of the number of messages posted in the room for the selected period.</span></span> <span data-ttu-id="25f3a-235">По умолчанию: 10</span><span class="sxs-lookup"><span data-stu-id="25f3a-235">Default: 10</span></span>

<span data-ttu-id="25f3a-236">**LeastActiveRooms:** Если указан этот параметр, в отчете будут содержаться как минимум активные комнаты чата в соответствии с количеством сообщений, опубликованных в комнате чата за выбранный период.</span><span class="sxs-lookup"><span data-stu-id="25f3a-236">**LeastActiveRooms:** If this is specified, the report will include the n least active chat rooms in terms of the number of messages posted in the chat room for the selected period.</span></span> <span data-ttu-id="25f3a-237">У комнат будет хотя бы одно сообщение.</span><span class="sxs-lookup"><span data-stu-id="25f3a-237">Rooms will have at least one message posted.</span></span> <span data-ttu-id="25f3a-238">По умолчанию: 10</span><span class="sxs-lookup"><span data-stu-id="25f3a-238">Default: 10</span></span>

<span data-ttu-id="25f3a-239">**RoomsInactiveSince:** Если задано значение, отчет будет включать список комнат чатов, которые были неактивны с момента указанной даты.</span><span class="sxs-lookup"><span data-stu-id="25f3a-239">**RoomsInactiveSince:** If this is specified, the report will include a list of chat rooms that have been inactive since the specified date.</span></span> <span data-ttu-id="25f3a-240">По умолчанию: все время</span><span class="sxs-lookup"><span data-stu-id="25f3a-240">Default: Entire Time</span></span>

<span data-ttu-id="25f3a-241">**OutputFolder:** Папка, в которой будут помещены ChatUsageReport.html и рисунки диаграммы.</span><span class="sxs-lookup"><span data-stu-id="25f3a-241">**OutputFolder:** The folder where the ChatUsageReport.html and the graph images will be placed.</span></span> <span data-ttu-id="25f3a-242">Это значение должно быть определено в файле конфигурации или в командной строке.</span><span class="sxs-lookup"><span data-stu-id="25f3a-242">This must be defined in the config file or on the command line.</span></span>

<span data-ttu-id="25f3a-243">Все значения параметров командной строки также можно указать в файле ChatUsageReport.exe.config, который находится в том же каталоге, что и инструмент.</span><span class="sxs-lookup"><span data-stu-id="25f3a-243">All of the command line parameter values can also be specified in the ChatUsageReport.exe.config file that is located in the same directory as the tool.</span></span> <span data-ttu-id="25f3a-244">Если в файле конфигурации и в командной строке задано какое либо значение, значение из командной строки будет переопределяться в файле конфигурации.</span><span class="sxs-lookup"><span data-stu-id="25f3a-244">If any value is specified in both the config file and the command line, the command line value will override the config file value.</span></span>

</div>

<div>

## <a name="output"></a><span data-ttu-id="25f3a-245">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="25f3a-245">Output</span></span>

<span data-ttu-id="25f3a-246">В отчет всегда будут включены следующие выходные данные:</span><span class="sxs-lookup"><span data-stu-id="25f3a-246">The report will always include the following output:</span></span>

  - <span data-ttu-id="25f3a-247">Первые n самых активных комнат чата по количеству записей в сообщении за выбранный период.</span><span class="sxs-lookup"><span data-stu-id="25f3a-247">Top n most active chat rooms by number of message posts for selected period.</span></span>

  - <span data-ttu-id="25f3a-248">Первые n наиболее активных пользователей по количеству записей сообщений за выбранный период.</span><span class="sxs-lookup"><span data-stu-id="25f3a-248">Top n most active users by number of message posts for selected period.</span></span>

  - <span data-ttu-id="25f3a-249">Первые n наименее активные комнаты чата по количеству записей в сообщении за выбранный период.</span><span class="sxs-lookup"><span data-stu-id="25f3a-249">Top n least active chat rooms by number of message posts for selected period.</span></span>

  - <span data-ttu-id="25f3a-250">Комнаты чата, неактивные для полного существования базы данных или в соответствии с указанной датой.</span><span class="sxs-lookup"><span data-stu-id="25f3a-250">Chat rooms that are inactive for the entire life of the database, or since the specified date.</span></span>

  - <span data-ttu-id="25f3a-251">Ежедневная Разноска сообщения за выбранный период.</span><span class="sxs-lookup"><span data-stu-id="25f3a-251">Daily message post trend for selected period.</span></span>

  - <span data-ttu-id="25f3a-252">Еженедельное сообщение о тенденциях за выбранный период.</span><span class="sxs-lookup"><span data-stu-id="25f3a-252">Weekly message post trend for selected period.</span></span>

  - <span data-ttu-id="25f3a-253">Месячная тенденция сообщения за выбранный период.</span><span class="sxs-lookup"><span data-stu-id="25f3a-253">Monthly message post trend for selected period.</span></span>

  - <span data-ttu-id="25f3a-254">Общее количество записей в сообщении за выбранный период.</span><span class="sxs-lookup"><span data-stu-id="25f3a-254">Total message posts for selected period.</span></span>

  - <span data-ttu-id="25f3a-255">Общее количество включенных комнат.</span><span class="sxs-lookup"><span data-stu-id="25f3a-255">Total number of enabled rooms.</span></span>

</div>

<div>

## <a name="example"></a><span data-ttu-id="25f3a-256">Пример</span><span class="sxs-lookup"><span data-stu-id="25f3a-256">Example</span></span>

<span data-ttu-id="25f3a-257">В следующем примере показано создание отчета об использовании для всего 2001 года и последующее сообщение будет помещено в OutputFolder, указанное в ChatUsageReport.exe.config.</span><span class="sxs-lookup"><span data-stu-id="25f3a-257">The following example generates a usage report for the entire year 2001 and places the report in the OutputFolder specified in the ChatUsageReport.exe.config.</span></span>

```Powershell
    ChatUsageReport -RoomsInactiveSince 06-20-2010
```
<span data-ttu-id="25f3a-258">ChatUsageReport.exe.config:</span><span class="sxs-lookup"><span data-stu-id="25f3a-258">ChatUsageReport.exe.config:</span></span>

```XML
    <?xml version="1.0" encoding="utf-8" ?>
    <configuration>
      <connectionStrings>
        <!-- The PersistentChat connection string must be defined in this file. -->
        <add name="PersistentChat" connectionString="Data Source=contoso.com\RTC;Initial Catalog=mgc;Integrated Security=SSPI"/>
      </connectionStrings>
      <appSettings>
        <!-- The OutputFolder must be defined here or on the command line. -->
        <add key="OutputFolder" value="."/>
        <!-- The values below are the same as the application defaults. -->
        <add key="StartDate" value="01/01/0001"/>
        <add key="EndDate" value="12/31/9999"/>
        <add key="TopActiveUsers" value="10"/>
        <add key="TopActiveRooms" value="10"/>
        <add key="LeastActiveRooms" value="10"/>
        <add key="RoomsInactiveSince" value="01/01/0001"/>
      </appSettings>
    </configuration></configuration>
```
</div>

</div>

<div>

## <a name="scheduleadsyncforprincipal"></a><span data-ttu-id="25f3a-259">ScheduleADSyncForPrincipal</span><span class="sxs-lookup"><span data-stu-id="25f3a-259">ScheduleADSyncForPrincipal</span></span>

<div>

## <a name="description"></a><span data-ttu-id="25f3a-260">Описание</span><span class="sxs-lookup"><span data-stu-id="25f3a-260">Description</span></span>

<span data-ttu-id="25f3a-261">ScheduleADSyncForPrincipal — это сценарий Microsoft SQL Server 2012, который необходимо запускать непосредственно из SQL Server Management Studio при подключении к сохраняемой обратной стороне чата в базе данных.</span><span class="sxs-lookup"><span data-stu-id="25f3a-261">ScheduleADSyncForPrincipal is a Microsoft SQL Server 2012 script that must be run directly from within SQL Server Management Studio when connected to the Persistent Chat back-end database.</span></span> <span data-ttu-id="25f3a-262">Этот сценарий позволяет принудительно использовать сохраняемый чат для синхронизации записей пользователя с данными из доменных служб Active Directory, а не ждать запланированного времени синхронизации.</span><span class="sxs-lookup"><span data-stu-id="25f3a-262">This script enables you to force Persistent Chat to synchronize its records of a user with those of Active Directory Domain Services, rather than waiting for the scheduled synchronization time.</span></span>

</div>

<div>

## <a name="requirements"></a><span data-ttu-id="25f3a-263">Требования</span><span class="sxs-lookup"><span data-stu-id="25f3a-263">Requirements</span></span>

<span data-ttu-id="25f3a-264">Учетная запись пользователя, под которой запускается сценарий, должна иметь доступ владельца к сохраняемой резервной базе данных чата.</span><span class="sxs-lookup"><span data-stu-id="25f3a-264">The user account under which the script is run must have owner access to the Persistent Chat back-end database.</span></span>

</div>

<div>

## <a name="usage"></a><span data-ttu-id="25f3a-265">Режим</span><span class="sxs-lookup"><span data-stu-id="25f3a-265">Usage</span></span>

<span data-ttu-id="25f3a-266">Ниже приведено содержимое сценария по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="25f3a-266">Following are the contents of the default script:</span></span>

```Powershell
    /*
    This script will schedule a principal for a forced AD synchronization cycle
    
    If you're using Sql Server Management Studio, pressing Ctrl+Shift+M will 
    allow you to specify values for the template parameter.
    */
    
        insert into
          tblPrincipalMeta
          (
           prinID
          ,prinAffiliationsDirty
          ,prinAttributesDirty
          ,prinDeleted
          )
          select
            prinID
           ,1
           ,1
           ,0
          from
            tblPrincipal
          where
            prinID not in (select prinID from tblPrincipalMeta) and
            prinID = <PrinID,int,0>
     
        update
          tblPrincipalMeta
        set
          prinAffiliationsDirty = 1
         ,prinAttributesDirty = 1
         ,tryCount = 0
         ,nextTry = null
        where
         prinID = <PrinID,int,0>
```

<span data-ttu-id="25f3a-267"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="25f3a-267"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

