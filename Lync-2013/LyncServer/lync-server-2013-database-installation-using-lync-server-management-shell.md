---
title: 'Lync Server 2013: установка базы данных с помощью командной консоли Lync Server'
description: 'Lync Server 2013: Установка базы данных с помощью командной консоли Lync Server Management Shell.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Database installation using Lync Server Management Shell
ms:assetid: c90a6449-4dd5-4b18-b21c-ea2c2a64dc3c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398832(v=OCS.15)
ms:contentKeyID: 48185401
ms.date: 06/16/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2d572984c94d280723b12c5343a92ddfaa12d4f0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431255"
---
# <a name="database-installation-using-lync-server-management-shell-in-lync-server-2013"></a>Установка базы данных с помощью командной консоли Lync Server в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2016-06-16_

Разделение ролей и обязанностей между администраторами сервера и администраторами SQL Server может привести к задержкам при реализации. Lync Server 2013 использует управление доступом на основе ролей (RBAC) для устранения этих проблем. В некоторых случаях администратор SQL Server должен управлять установкой баз данных на сервере SQL Server за пределами RBAC. Командная консоль Lync Server 2013 позволяет администратору SQL Server выполнять командлеты Windows PowerShell, предназначенные для настройки баз данных с правильными данными и файлами журнала. Дополнительные сведения можно найти [в разделе разрешения на развертывание SQL Server в Lync server 2013](lync-server-2013-deployment-permissions-for-sql-server.md).

<div class=" ">


> [!IMPORTANT]  
> В описанной ниже процедуре предполагается, что на сервере Lync Server 2013 OCSCore.msi, SQL Server Native Client (sqlncli.msi) управляющие объекты Microsoft SQL Server 2012, типы среды CLR для Microsoft SQL Server 2012 и Microsoft SQL Server 2012 ADOMD.NET установлены. OCSCore.msi расположен на установочном носителе в каталоге \Setup\AMD64\Setup. Остальные компоненты находятся в \Setup\amd64. Кроме того, подготовка Active Directory для Lync Server 2013 успешно завершена.



</div>

**Install-CsDatabase** — это командлет Windows PowerShell, который вы используете для установки баз данных. Командлет **Install-CsDatabase** имеет большое количество параметров, и только некоторые из них обсуждаются здесь. Подробнее об этих параметрах можно найти в документации по командной консоли Lync Server 2013.

<div class=" ">


> [!WARNING]  
> Чтобы избежать проблем с производительностью и возможной задержкой, всегда используйте полные доменные имена (FQDN) при ссылке на серверы SQL Server. Старайтесь не использовать только ссылки на имена узлов. Например, используйте sqlbe01.contoso.net, но не используйте SQLBE01.



</div>

Для установки баз данных **Установка-CsDatabase** использует три основных метода размещения баз данных на подготовленном сервере SQL Server.

  - Запустите **Install-CsDatabase** без DatabasePaths или UseDefaultSqlPath. Командлет использует встроенный алгоритм для определения наилучшего размещения журнала и файлов данных. Алгоритм работает только для отдельных реализаций SQL Server.

  - Запустите **Install-CsDatabase** с параметром DatabasePaths. Встроенный алгоритм для оптимизации расположения файлов журнала и данных не используется, если определен параметр DatabasePaths. С помощью этого параметра можно задать расположение для развертывания файлов журнала и данных.

  - Запустите **Install-CsDatabase** с UseDefaultSqlPaths. Этот параметр не использует встроенный алгоритм для оптимизации расположения файлов журнала и данных. Файлы журнала и данных развертываются в соответствии с параметрами по умолчанию, заданными администратором SQL Server. Эти пути обычно устанавливаются для автоматического администрирования файлов журнала и данных на сервере SQL Server и не связаны с установкой Lync Server 2013.

  - Параметр DatabasePathMap также можно использовать для явного задания местоположения для каждой базы данных и соответствующего файла журнала.

<div>

## <a name="to-use-windows-powershell-cmdlets-to-configure-the-sql-server-central-management-store"></a>Использование командлетов Windows PowerShell для настройки хранилища SQL Server Central Management

1.  На любом компьютере войдите в систему с учетными данными администратора для создания баз данных на сервере SQL Server. Дополнительные сведения можно найти [в разделе разрешения на развертывание SQL Server в Lync server 2013](lync-server-2013-deployment-permissions-for-sql-server.md).

2.  Откройте консоль управления Lync Server 2013. Если вы не настроили политику выполнения для Windows PowerShell, необходимо настроить политику, чтобы разрешить запуск сценариев Windows PowerShell. Подробные сведения можно найти в разделе Проверка политики выполнения [https://go.microsoft.com/fwlink/p/?linkId=203093](https://go.microsoft.com/fwlink/p/?linkid=203093) .

3.  С помощью командлета **Install-CsDatabase** Установите центральное хранилище управления.
    
       ```powershell
        Install-CsDatabase -CentralManagementDatabase -SqlServerFqdn <fully qualified domain name of SQL Server> 
        -SqlInstanceName <named instance> -DatabasePaths <logfile path>,<database file path> 
        -Report <path to report file>
       ```
    
       ```powershell
        Install-CsDatabase -CentralManagementDatabase -SqlServerFqdn sqlbe.contoso.net -SqlInstanceName rtc -DatabasePaths "C:\CSDB-Logs","C:\CSDB-CMS" -Report "C:\Logs\InstallDatabases.html"
       ```
    
    <div class=" ">
    

    > [!TIP]  
    > Параметр Report является необязательным, но он полезен, если вы собираетесь документировать процесс установки.

    
    </div>

4.  **Установка-CsDatabase – DatabasePaths** может использовать до шести параметров пути, каждый из которых определяет пути к дискам, заданным в данных SQL Server и размещении файлов журнала. По логическим правилам конфигурации базы данных в Lync Server 2013 диски разбиваются на сегменты двух, четырех или шести. В зависимости от конфигурации SQL Server и количества сегментов вы будете указывать два пути, четыре пути или шесть путей.
    
    Если у вас три диска, журнал получает приоритет и файлы данных распределяются после. Пример для сервера SQL Server, настроенного на шесть дисков:
    ```powershell
    Install-CsDatabase -ConfiguredDatases -SqlServerFqdn sqlbe.contoso.net -DatabasePaths "D:\CSDynLogs","E:\CSRtcLogs","F:\MonCdrArcLogs","G:\MonCdrArchData","H:\AbsAppLog","I:\DynRtcAbsAppData" -Report "C:\Logs\InstallDatabases.html"
    ```
5.  После завершения установки базы данных вы можете закрыть командную консоль Lync Server 2013 или перейти к установке баз данных Lync Server 2013, указанных в построителе топологии.

</div>

<div>

## <a name="to-use-windows-powershell-cmdlets-to-configure-the-sql-server-topology-configured-databases"></a>Использование командлетов Windows PowerShell для настройки баз данных топологии SQL Server

1.  Чтобы установить базу данных Topology Builder для Lync Server 2013, администратор Lync Server 2013 должен опубликовать топологию. Подробности можно найти [в разделе Публикация топологии в Lync Server 2013](lync-server-2013-publish-the-topology.md) в документации по развертыванию.

2.  На любом компьютере войдите в систему с учетными данными администратора для создания баз данных на сервере SQL Server. В этой статье содержатся [разрешения на развертывание SQL Server в Lync server 2013](lync-server-2013-deployment-permissions-for-sql-server.md).
    
    <div class=" ">
    

    > [!IMPORTANT]  
    > Чтобы настроить базы данных SQL Server, убедитесь в том, что учетная запись администратора SQL Server, используемая для выполнения описанных здесь действий, также входит в группу "Администраторы" (или аналогичную) на сервере SQL Server и удерживает роль сервера центрального управления. Это особенно важно для проверки наличия дополнительных пулов Lync Server 2013, в которых требуется установка или Настройка базы данных SQL Server. Например, если вы развертываете второй пул (pool02), но роль сервера центрального управления удерживает pool01. Группа системного администратора SQL Server (или ее эквивалент) должна иметь разрешения на доступ к обеим базам данных SQL Server.

    
    </div>

3.  Откройте консоль управления Lync Server 2013, если она еще не открыта.

4.  С помощью командлета **Install-CsDatabase** установите базу данных, настроенную на основе Topology Builder.
    
       ```powershell
        Install-CsDatabase -ConfiguredDatabases -SqlServerFqdn <fully qualified domain name of SQL Server> 
         -DatabasePaths <logfile path>,<database file path> -Report <path to report file>
       ```
    
       ```powershell
        Install-CsDatabase -ConfiguredDatabases -SqlServerFqdn sqlbe.contoso.net 
        -Report "C:\Logs\InstallDatabases.html"
       ```
    
    <div class=" ">
    

    > [!TIP]  
    > Параметр Report является необязательным, но он полезен, если вы собираетесь документировать процесс установки.

    
    </div>

5.  После завершения установки базы данных закройте консоль управления Lync Server 2013.

</div>

<div>

## <a name="to-use-windows-powershell-cmdlets-to-configure-the-sql-server-topology-using-the-databasepathmap-parameter"></a>Использование командлетов Windows PowerShell для настройки топологии SQL Server с помощью параметра DatabasePathMap

1.  Чтобы установить базу данных для Lync Server 2013, администратор Lync Server должен создать пути и развернуть файлы баз данных и файлы журнала согласно предопределенному набору правил.

2.  На любом компьютере войдите в систему с учетными данными администратора для создания баз данных на сервере SQL Server. В этой статье содержатся [разрешения на развертывание SQL Server в Lync server 2013](lync-server-2013-deployment-permissions-for-sql-server.md).
    
    <div class=" ">
    

    > [!IMPORTANT]  
    > Чтобы настроить базы данных SQL Server, убедитесь в том, что учетная запись администратора SQL Server, используемая для выполнения описанных здесь действий, также входит в группу "Администраторы" (или аналогичную) на сервере SQL Server и удерживает роль сервера центрального управления. Это особенно важно для проверки наличия дополнительных пулов серверов Lync, в которых требуется установка или Настройка базы данных SQL Server. Например, если вы развертываете второй пул (pool02), но роль сервера центрального управления удерживает pool01. Группа системного администратора SQL Server (или ее эквивалент) должна иметь разрешения на доступ к обеим базам данных SQL Server.

    
    </div>

3.  Откройте консоль управления Lync Server, если она еще не открыта.

4.  С помощью командлета **Install-CsDatabase** с параметром DatabasePathMap и хэш-таблицей PowerShell установите базу данных, настроенную на основе Topology Builder.

5.  В примере кода пути, определенные для баз данных, можно определить с помощью параметра – DatabasePathMap и определенной хэш-таблицы, как показано ниже (в примере используется "C: \\ CSData" для всех файлов базы данных (MDF) и "C: \\ CSLogFiles" для всех файлов журнала (LDF). При необходимости будет создана папка Install-CsDatabase):
    ```powershell
    $pathmap = @{
    "BackendStore:BlobStore:DbPath"="C:\CsData";"BackendStore:BlobStore:LogPath"="C:\CsLogFiles"
    "BackendStore:RtcSharedDatabase:DbPath"="C:\CsData";"BackendStore:RtcSharedDatabase:LogPath"="C:\CsLogFiles"
    "ABSStore:AbsDatabase:DbPath"="C:\CsData";"ABSStore:AbsDatabase:LogPath"="C:\CsLogFiles"
    "ApplicationStore:RgsConfigDatabase:DbPath"="C:\CsData";"ApplicationStore:RgsConfigDatabase:LogPath"="C:\CsLogFiles"
    "ApplicationStore:RgsDynDatabase:DbPath"="C:\CsData";"ApplicationStore:RgsDynDatabase:LogPath"="C:\CsLogFiles"
    "ApplicationStore:CpsDynDatabase:DbPath"="C:\CsData";"ApplicationStore:CpsDynDatabase:LogPath"="C:\CsLogFiles"
    "ArchivingStore:ArchivingDatabase:DbPath"="C:\CsData";"ArchivingStore:ArchivingDatabase:LogPath"="C:\CsLogFiles"
    "MonitoringStore:MonitoringDatabase:DbPath"="C:\CsData";"MonitoringStore:MonitoringDatabase:LogPath"="C:\CsLogFiles"
    "MonitoringStore:QoEMetricsDatabase:DbPath"="C:\CsData";"MonitoringStore:QoEMetricsDatabase:LogPath"="C:\CsLogFiles"
    }
    Install-CsDatabase -ConfigureDatabases -SqlServerFqdn sqlbe01.contoso.net -DatabasePathMap $pathmap
    ```
6.  Так как файлы базы данных и журнала явным образом названы на целевом сервере базы данных, вы можете задать конкретные расположения для базы данных и журнала для каждого типа службы. В следующем примере базы данных размещаются для каждого определенного типа службы на разных дисках, а связанные файлы журнала — на другом. Например:
    
      - Все базы данных RTC в "D: \\ RTCDatabase"
    
      - Все файлы журнала RTC на "E: \\ RTCLogs"
    
      - Все базы данных магазина приложений в "F: \\ CPSDatabases"
    
      - Все журналы приложений для магазина в "G: \\ CPSLogs"
    
      - Все базы данных магазина группы ответа в "H: \\ RGSDatabases"
    
      - Все журналы магазина группы ответа в "I: \\ RGSLogs"
    
      - Все базы данных из хранилища адресных книг в "J: \\ ABSDatabases"
    
      - Все файлы журнала для хранения адресной книги в "K: \\ ABSLogs"
    
      - Все базы данных архивов из Store в "L: \\ ArchivingDatabases"
    
      - Все журналы архивирования в хранилище "м: \\ ArchivingLogs"
    
      - Все базы данных магазина мониторинга в "N: \\ MonitoringDatabases"
    
      - Все файлы журнала мониторинга в магазине для "O: \\ MonitoringLogfiles"
    
    <!-- end list -->
    
    ```powershell    
    $pathmap = @{
    "BackendStore:BlobStore:DbPath"="D:\RTCDatabase";"BackendStore:BlobStore:LogPath"="E:\RTCLogs"
    "BackendStore:RtcSharedDatabase:DbPath"="D:\RTCDatabase";"BackendStore:RtcSharedDatabase:LogPath"="E:\RTCLogs"
    "ABSStore:AbsDatabase:DbPath"="J:\ABSDatabases";"ABSStore:AbsDatabase:LogPath"="K:\ABSLogs"
    "ApplicationStore:RgsConfigDatabase:DbPath"="H:\RGSDatabases";"ApplicationStore:RgsConfigDatabase:LogPath"="G:\CPSLogs"
    "ApplicationStore:RgsDynDatabase:DbPath"="H:\RGSDatabases";"ApplicationStore:RgsDynDatabase:LogPath"="I:\RGSLogs"
    "ApplicationStore:CpsDynDatabase:DbPath"="F:\CPSDatabases";"ApplicationStore:CpsDynDatabase:LogPath"="G:\CsLogFiles"
    "ArchivingStore:ArchivingDatabase:DbPath"="M:\ArchivingLogs";"ArchivingStore:ArchivingDatabase:LogPath"="N:\MonitoringDatabases"
    "MonitoringStore:MonitoringDatabase:DbPath"="N:\MonitoringDatabases";"MonitoringStore:MonitoringDatabase:LogPath"="O:\MonitoringLogfiles"
    "MonitoringStore:QoEMetricsDatabase:DbPath"="N:\MonitoringDatabases";"MonitoringStore:QoEMetricsDatabase:LogPath"="O:\MonitoringLogfiles"
    }
    
    Install-CsDatabase -ConfiguredDatabases -SqlServerFqdn sqlbe01.contoso.net -DatabasePathMap $pathmap
    ```
    
    С помощью параметра – DatabasePathMap вы можете определить любую комбинацию сопоставления букв логических дисков, которая обеспечивает наилучшее решение для требований к производительности и размещению SQL Server.

Если вы настроили файлы данных и журналы базы данных с помощью метода **DatabasePathMap** , вам потребуется внести небольшие изменения в обычный процесс при использовании Topology Builder. Обычно определяются варианты топологии, публикуются топология и выбирается развертывание выбранных баз данных.

Если вы использовали **DatabasePathMap** , вы уже выполнили третью часть процесса Topology Builder. В случае, если сервер базы данных полностью настроен на предварительный запуск построителя топологии, вы можете определить все роли и параметры сервера, но отменить выбор параметра для создания баз данных.

</div>

</div>

<span> </span>

</div>

</div>

</div>

