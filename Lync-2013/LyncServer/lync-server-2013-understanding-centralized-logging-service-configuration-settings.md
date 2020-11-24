---
title: Общие сведения о централизованных параметрах конфигурации службы ведения журнала
description: Общие сведения о централизованных параметрах конфигурации службы ведения журнала.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Understanding Centralized Logging Service configuration settings
ms:assetid: 3c34e600-0b91-43dc-b4cc-90b6a70ee12e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688029(v=OCS.15)
ms:contentKeyID: 49733619
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0f99dbffe15c4b3f0dc13d231c3a2732a8554397
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399496"
---
# <a name="understanding-centralized-logging-service-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="d35a6-103">Общие сведения о централизованных параметрах конфигурации службы ведения журналов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d35a6-103">Understanding Centralized Logging Service configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d35a6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d35a6-104">

<span> </span></span></span>

<span data-ttu-id="d35a6-105">_**Тема последнего изменения:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="d35a6-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="d35a6-106">Служба централизованного ведения журналов настраивается для определения того, как должна собираться служба ведения журнала, как она будет собирать данные, откуда она собирается и какие параметры журнала.</span><span class="sxs-lookup"><span data-stu-id="d35a6-106">The Centralized Logging Service is configured to define what the logging service is intended to collect, how it collects, where it will collect from, and what the log settings are.</span></span> <span data-ttu-id="d35a6-107">You define these settings globally (that is, for the entire deployment) or for a site (that is, a named site in your deployment).</span><span class="sxs-lookup"><span data-stu-id="d35a6-107">You define these settings globally (that is, for the entire deployment) or for a site (that is, a named site in your deployment).</span></span> <span data-ttu-id="d35a6-108">Any logging that you define will use the settings that are appropriate for the identity that you use for commands to start, stop, flush, and search logs.</span><span class="sxs-lookup"><span data-stu-id="d35a6-108">Any logging that you define will use the settings that are appropriate for the identity that you use for commands to start, stop, flush, and search logs.</span></span>

<div>

## <a name="to-display-the-current-centralized-logging-service-configuration"></a><span data-ttu-id="d35a6-109">Чтобы отобразить текущую конфигурацию централизованной службы ведения журнала</span><span class="sxs-lookup"><span data-stu-id="d35a6-109">To display the current Centralized Logging Service configuration</span></span>

1.  <span data-ttu-id="d35a6-110">Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="d35a6-110">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="d35a6-111">Введите следующую команду в командной строке:</span><span class="sxs-lookup"><span data-stu-id="d35a6-111">Type the following at a command-line prompt:</span></span>
    
        Get-CsClsConfiguration
    
    <div>
    

    > [!TIP]
    > <span data-ttu-id="d35a6-112">Вы можете сузить или расширить область параметров конфигурации, возвращаемых определением <CODE>-Identity</CODE> и областью, например "site: Redmond", чтобы возвращать только CsClsConfiguration для Redmond сайта.</span><span class="sxs-lookup"><span data-stu-id="d35a6-112">You can narrow or expand the scope of the configuration settings that are returned by defining <CODE>-Identity</CODE> and a scope, such as "Site:Redmond" to return only the CsClsConfiguration for the site Redmond.</span></span> <span data-ttu-id="d35a6-113">Если вы хотите получить подробные сведения о конкретной части конфигурации, вы можете передать эти данные в другой командлет Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d35a6-113">If you want details about a given portion of the configuration, you can pipe the output into another Windows PowerShell cmdlet.</span></span> <span data-ttu-id="d35a6-114">Например, чтобы получить подробные сведения о сценариях, определенных в конфигурации для сайта Redmond, введите: <CODE>Get-CsClsConfiguration -Identity "site:Redmond" | Select-Object -ExpandPropery Scenarios</CODE></span><span class="sxs-lookup"><span data-stu-id="d35a6-114">For example, to get details about the scenarios defined in the configuration for site "Redmond", type: <CODE>Get-CsClsConfiguration -Identity "site:Redmond" | Select-Object -ExpandPropery Scenarios</CODE></span></span>

    
    </div>
    
    <span data-ttu-id="d35a6-115">![Выход выборки из Get-CsClsConfiguration.](images/JJ688029.23f98ddc-fc48-499a-b6c5-752611f2a0b0(OCS.15).jpg "Выход выборки из Get-CsClsConfiguration.")</span><span class="sxs-lookup"><span data-stu-id="d35a6-115">![Sample output from Get-CsClsConfiguration.](images/JJ688029.23f98ddc-fc48-499a-b6c5-752611f2a0b0(OCS.15).jpg "Sample output from Get-CsClsConfiguration.")</span></span>
    
    <span data-ttu-id="d35a6-116">Результат командлета выводит текущую конфигурацию централизованной службы ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="d35a6-116">The result from the cmdlet displays the current configuration of the Centralized Logging Service.</span></span>
    
    
    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="d35a6-117">Параметр конфигурации</span><span class="sxs-lookup"><span data-stu-id="d35a6-117">Configuration Setting</span></span></th>
    <th><span data-ttu-id="d35a6-118">Описание</span><span class="sxs-lookup"><span data-stu-id="d35a6-118">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="d35a6-119"><strong>Identity</strong></span><span class="sxs-lookup"><span data-stu-id="d35a6-119"><strong>Identity</strong></span></span></p></td>
    <td><p><span data-ttu-id="d35a6-p103">Определяет область действия и имя данной конфигурации.  Существует одна глобальная конфигурация и по одной конфигурации для каждого сайта.</span><span class="sxs-lookup"><span data-stu-id="d35a6-p103">Identifies the scope and name for this configuration. There is only one Global configuration, and one configuration per site.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="d35a6-122"><strong>Scenarios</strong></span><span class="sxs-lookup"><span data-stu-id="d35a6-122"><strong>Scenarios</strong></span></span></p></td>
    <td><p><span data-ttu-id="d35a6-123">Список всех сценариев, определенных для данной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="d35a6-123">Listing of all scenarios that are defined for this configuration.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="d35a6-124"><strong>SearchTerms</strong></span><span class="sxs-lookup"><span data-stu-id="d35a6-124"><strong>SearchTerms</strong></span></span></p></td>
    <td><p><span data-ttu-id="d35a6-125">Определенные поисковые запросы для этой конфигурации.</span><span class="sxs-lookup"><span data-stu-id="d35a6-125">Defined search terms for the configuration.</span></span> <span data-ttu-id="d35a6-126">Office 365 или Microsoft 365, а не локальное развертывание.</span><span class="sxs-lookup"><span data-stu-id="d35a6-126">Office 365 or Microsoft 365, not on-premises deployments.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="d35a6-127"><strong>SecurityGroups</strong></span><span class="sxs-lookup"><span data-stu-id="d35a6-127"><strong>SecurityGroups</strong></span></span></p></td>
    <td><p><span data-ttu-id="d35a6-128">Определенные группы безопасности, которые управляют кто (т. е. участники групп безопасности) могут просматривать компьютеры на основе сайта их размещения.</span><span class="sxs-lookup"><span data-stu-id="d35a6-128">Defined security groups that control who (that is, members of the security groups) can see computers based on the site they are located in.</span></span> <span data-ttu-id="d35a6-129">Сайт в данном контексте — сайт, определенный в построителе топологии.</span><span class="sxs-lookup"><span data-stu-id="d35a6-129">Site, in this context, is the site as defined in Topology Builder.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="d35a6-130"><strong>Regions</strong></span><span class="sxs-lookup"><span data-stu-id="d35a6-130"><strong>Regions</strong></span></span></p></td>
    <td><p><span data-ttu-id="d35a6-131">Определенные регионы используются для сбора групп безопасности по регионам, например EMEA (страны Европы, Ближнего Востока и Африки).</span><span class="sxs-lookup"><span data-stu-id="d35a6-131">Defined regions are used to collect SecurityGroups into a region, for example EMEA.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="d35a6-132"><strong>EtlFileFolder</strong></span><span class="sxs-lookup"><span data-stu-id="d35a6-132"><strong>EtlFileFolder</strong></span></span></p></td>
    <td><p><span data-ttu-id="d35a6-133">Определенный путь к расположению, в котором файлы журнала записываются на компьютеры.</span><span class="sxs-lookup"><span data-stu-id="d35a6-133">Defined path to the location where log files are written on computers.</span></span> <span data-ttu-id="d35a6-134">CLSAgent записывает файлы журнала и запускается в контексте сетевой службы.</span><span class="sxs-lookup"><span data-stu-id="d35a6-134">CLSAgent writes the log files and runs under the context of the Network Service.</span></span> <span data-ttu-id="d35a6-135">В этом случае% TEMP% разворачивается до%WINDIR%\ServiceProfiles\NetworkService\AppData\Local</span><span class="sxs-lookup"><span data-stu-id="d35a6-135">In this case, %TEMP% expands to %WINDIR%\ServiceProfiles\NetworkService\AppData\Local</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="d35a6-136"><strong>EtlFileRolloverSizeMB</strong></span><span class="sxs-lookup"><span data-stu-id="d35a6-136"><strong>EtlFileRolloverSizeMB</strong></span></span></p></td>
    <td><p><span data-ttu-id="d35a6-p107">Данный параметры указывает максимальный размер файла журнала до создания нового файла трассировки журнала (.etl). Новый файл журнала создается при достижении определенного размера, даже если не было достигнуто значение, заданное в параметре EtlFileRolloverMinutes.</span><span class="sxs-lookup"><span data-stu-id="d35a6-p107">The parameter indicates the maximum size of the log file before a new event trace log (.etl) file is created. A new log file is created when the defined size is reached even if the maximum time set in EtlFileRolloverMinutes has not yet been reached.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="d35a6-139"><strong>EtlFileRolloverMinutes</strong></span><span class="sxs-lookup"><span data-stu-id="d35a6-139"><strong>EtlFileRolloverMinutes</strong></span></span></p></td>
    <td><p><span data-ttu-id="d35a6-p108">Определенное максимальное время существования журнала (в минутах) до создания нового ETL-файла. Новый файл журнала создается по завершении таймера, даже если еще не было достигнуто значение максимального размера, заданное в параметре EtlFileRolloverSizeMB.</span><span class="sxs-lookup"><span data-stu-id="d35a6-p108">Defined maximum amount of time, in minutes, that a log can elapse before a new .etl file is created. A new log file is created when the timer expires even if the maximum size set in EtlFileRolloverSizeMB has not yet been reached.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="d35a6-142"><strong>TmfFileSearchPath</strong></span><span class="sxs-lookup"><span data-stu-id="d35a6-142"><strong>TmfFileSearchPath</strong></span></span></p></td>
    <td><p><span data-ttu-id="d35a6-143">Местоположение для поиска файлов формата трассировки сообщений.</span><span class="sxs-lookup"><span data-stu-id="d35a6-143">Location to search for the trace message format files.</span></span> <span data-ttu-id="d35a6-144">Файлы формата сообщений трассировки используются для преобразования двоичных файлов в формат, пригодный для восприятия.</span><span class="sxs-lookup"><span data-stu-id="d35a6-144">The trace message format files are used to convert the binary files into a human readable format.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="d35a6-145"><strong>CacheFileLocalFolders</strong></span><span class="sxs-lookup"><span data-stu-id="d35a6-145"><strong>CacheFileLocalFolders</strong></span></span></p></td>
    <td><p><span data-ttu-id="d35a6-p110">Определенный путь к месту сохранения файлов кэша на компьютерах. CLSAgent записывает файлы кэша и работает в контексте сетевой службы. В этом случае значением переменной %TEMP% является %WINDIR%\ServiceProfiles\NetworkService\AppData\Local. По умолчанию файлы кэша и файлы журнала записываются в один каталог.</span><span class="sxs-lookup"><span data-stu-id="d35a6-p110">Defined path to the location where cache files are written on computers. CLSAgent writes the cache files and runs under the context of the Network Service. In this case, %TEMP% expands to %WINDIR%\ServiceProfiles\NetworkService\AppData\Local. By default, cache files and log files are written to the same directory.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="d35a6-150"><strong>CacheFileNetworkFolder</strong></span><span class="sxs-lookup"><span data-stu-id="d35a6-150"><strong>CacheFileNetworkFolder</strong></span></span></p></td>
    <td><p><span data-ttu-id="d35a6-151">Можно определить UNC-путь для получения файлов кэша во время операций ведения журналов.</span><span class="sxs-lookup"><span data-stu-id="d35a6-151">You can define a universal naming convention (UNC) path to receive the cache files during logging operations.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="d35a6-152"><strong>CacheFileLocalRetentionPeriod</strong></span><span class="sxs-lookup"><span data-stu-id="d35a6-152"><strong>CacheFileLocalRetentionPeriod</strong></span></span></p></td>
    <td><p><span data-ttu-id="d35a6-153">Определяется как максимальное время в днях для сохранения файлов кэша.</span><span class="sxs-lookup"><span data-stu-id="d35a6-153">Defined as the maximum time, in days, that cache files are retained.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="d35a6-154"><strong>CacheFileMaxDiskUsage</strong></span><span class="sxs-lookup"><span data-stu-id="d35a6-154"><strong>CacheFileMaxDiskUsage</strong></span></span></p></td>
    <td><p><span data-ttu-id="d35a6-155">Определяется как часть дискового пространства (выраженное в процентах), которое может использоваться под файлы кэша.</span><span class="sxs-lookup"><span data-stu-id="d35a6-155">Defined as the percentage of disk space that can be used by the cache files.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="d35a6-156"><strong>ComponentThrottleLimit</strong></span><span class="sxs-lookup"><span data-stu-id="d35a6-156"><strong>ComponentThrottleLimit</strong></span></span></p></td>
    <td><p><span data-ttu-id="d35a6-157">Определяется как максимальное количество трассировок в секунду, которое может создавать компонент до активации автоматического ограничителя.</span><span class="sxs-lookup"><span data-stu-id="d35a6-157">Defined as the maximum number of traces per second that a component can produce before the automatic throttle limiter is triggered.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="d35a6-158"><strong>ComponentThrottleSample</strong></span><span class="sxs-lookup"><span data-stu-id="d35a6-158"><strong>ComponentThrottleSample</strong></span></span></p></td>
    <td><p><span data-ttu-id="d35a6-159">Количество превышений значения ComponentThrottleLimit в течение 60 секунд.</span><span class="sxs-lookup"><span data-stu-id="d35a6-159">Number of times in 60 seconds that the ComponentThrottleLimit can be exceeded.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="d35a6-160"><strong>MinimumClsAgentServiceVersion</strong></span><span class="sxs-lookup"><span data-stu-id="d35a6-160"><strong>MinimumClsAgentServiceVersion</strong></span></span></p></td>
    <td><p><span data-ttu-id="d35a6-161">Минимальная версия CLSAgent, допустимая для запуска.</span><span class="sxs-lookup"><span data-stu-id="d35a6-161">The minimum version of the CLSAgent allowed to run.</span></span> <span data-ttu-id="d35a6-162">Этот элемент предназначен для Office 365 или Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="d35a6-162">This element is intended for Office 365 or Microsoft 365.</span></span></p></td>
    </tr>
    </tbody>
    </table>


</div>

<div>

## <a name="see-also"></a><span data-ttu-id="d35a6-163">См. также</span><span class="sxs-lookup"><span data-stu-id="d35a6-163">See Also</span></span>


[<span data-ttu-id="d35a6-164">Общие сведения об централизованной службе ведения журналов в Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d35a6-164">Overview of the Centralized Logging Service in Lync Server 2013</span></span>](lync-server-2013-overview-of-the-centralized-logging-service.md)  


<span data-ttu-id="d35a6-165">[Set-CsClsConfiguration](https://technet.microsoft.com/library/JJ619182(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="d35a6-165">[Set-CsClsConfiguration](https://technet.microsoft.com/library/JJ619182(v=OCS.15))</span></span>  
<span data-ttu-id="d35a6-166">[Remove-CsClsConfiguration](https://technet.microsoft.com/library/JJ619191(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="d35a6-166">[Remove-CsClsConfiguration](https://technet.microsoft.com/library/JJ619191(v=OCS.15))</span></span>  
<span data-ttu-id="d35a6-167">[New-CsClsConfiguration](https://technet.microsoft.com/library/JJ619177(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="d35a6-167">[New-CsClsConfiguration](https://technet.microsoft.com/library/JJ619177(v=OCS.15))</span></span>  
<span data-ttu-id="d35a6-168">[Get-CsClsConfiguration](https://technet.microsoft.com/library/JJ619179(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="d35a6-168">[Get-CsClsConfiguration](https://technet.microsoft.com/library/JJ619179(v=OCS.15))</span></span>  
  

<span data-ttu-id="d35a6-169"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d35a6-169"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

