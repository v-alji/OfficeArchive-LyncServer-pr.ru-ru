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
# <a name="lync-server-2013-persistent-chat-resource-kit-tools"></a>Средства набора ресурсов сохраняемого чата для Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2013-02-24_

Средства набора ресурсов сохраняемый чат для Lync Server 2013 помогают упростить выполнение повседневных задач для ИТ – администраторов, которые развертывают и управляют сервером Lync Server 2013 с сохраненным чат. В дополнение к инструкциям по установке в этом разделе описывается назначение каждого инструмента и примеры его использования.

<div>

## <a name="installation-of-the-resource-kit-tools"></a>Установка средств из набора ресурсов

Чтобы установить Lync Server 2013, средства набора ресурсов, скачайте **PersistentChatReskit.msi**. Запустите **PersistentChatReskit.msi** , чтобы выполнить простую установку. MSI устанавливает все инструменты, описанные в следующем пути: \\ **Program Files \\ Microsoft Lync Server 2013, \\ Пакет ресурсов** для работы сервера. Инструменты, представляющие собой автономные исполняемые файлы, находятся непосредственно в этой папке. Инструменты, у которых также есть файлы, находятся в своих вложенных папках.

<div>


> [!IMPORTANT]  
> После установки пакета Lync Server 2013, средства набора ресурсов необходимо установить <STRONG>PsExec.exe</STRONG> и скопировать <STRONG>PsExec.exe</STRONG> по следующему адресу: \\ <STRONG>Program Files \ Microsoft Lync Server 2013, серверный ресурс Kit\ChatStressTool</STRONG>. Если вы не копируете <STRONG>PsExec.exe</STRONG>, средство "постоянная стресс чата" вызывает исключение ошибки и не работает должным образом. Перед запуском средства убедитесь в том, что вы отвечаете этим требованиям предварительной версии. Подробнее об установке <STRONG>PsExec.exe</STRONG>можно найти в разделе <A href="https://go.microsoft.com/fwlink/p/?linkid=282246">https://go.microsoft.com/fwlink/p/?LinkId=282246</A> .



</div>

</div>

<div>

## <a name="supported-environments"></a>Поддерживаемые среды

Для оптимальной производительности в Lync Server 2013 вы сможете установить средства набора ресурсов в той же среде и те же спецификации, которые необходимы для Lync Server 2013.

</div>

<div>

## <a name="resource-kit-tools-overview"></a>Обзор средств из набора ресурсов

Ниже приведены средства, доступные в наборе ресурсов для работы с пакетом Resource Chat для Lync Server 2013. В следующем разделе представлено описание всех инструментов, в том числе требования и использование примера использования.

  - AffCheck

  - ChatMonitoringSummary

  - Инструмент ChatStress

  - ChatUpgradeVerifier

  - ChatUsageReport

  - ScheduleADSyncforPrincipal

</div>

<div>

## <a name="affcheck"></a>AffCheck

<div>

## <a name="description"></a>Описание

Средство AffCheck подтверждает, что записи, заданные пользователем базы данных и принадлежности к группе, совпадают с учетными записями доменных служб Active Directory.

</div>

<div>

## <a name="requirements"></a>Требования

Средство устанавливается вместе с установщиком PersistentChatResKit на компьютере, подключенном к домену.

Учетная запись пользователя, от имени которой запускается средство, должна иметь доступ на чтение к сохраняемой резервной базе данных чата и доменным службам Active Directory.

</div>

<div>

## <a name="usage"></a>Режим

Настройте файл AffCheck.exe.config в соответствии с инструкциями в файле конфигурации и запустите средство AffCheck без параметров командной строки. Ниже приведено содержимое AffCheck.exe.config по умолчанию.

**AffCheck.exe.config:**

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

## <a name="chatmonitoringsummary"></a>ChatMonitoringSummary

<div>

## <a name="description"></a>Описание

Средство PersistentChatMonitoringSummary перемещает сохраняемые данные чата из базы данных мониторинга в указанный файл журнала CSV.

CSV-файл содержит подразделение сеансов сохраняемого чата на общее количество сеансов, успешные сеансы, непредвиденные сбои, ожидаемые ошибки и разделение на непредвиденные сбои с помощью идентификатора диагностики, количества сбоев и описания сбоя.

</div>

<div>

## <a name="requirements"></a>Требования

Установите средства набора ресурсов сохраняемого чата на компьютере, подключенном к домену, который имеет доступ к базе данных мониторинга.

Учетная запись пользователя, под которой запускается средство, должна иметь доступ на чтение к базе данных мониторинга.

Файл PersistentChatMonitoringSummary.exe.config должен содержать \<connectionStrings\> раздел, который определяет строку подключения к базе данных мониторинга. Оно также должно содержать ключ для PersistentChatEndpointUri, для которого будут собираться данные мониторинга, и путь к файлу для CSV-файла, который будет создан. Ознакомьтесь с примерами установленного файла конфигурации. Файл должен находиться в той же папке, что и инструмент.

</div>

<div>

## <a name="usage"></a>Режим

```Batch
    PersistentChatMonitoringSummary [-StartDateTime <date>] [-EndDateTime <date>]
```

Эти параметры определяют выбор данных:

**StartDateTime:** При необходимости указывается дата начала периода выбора. По умолчанию: 1/1/1753 12:00:00 AM

**EndDateTime:** Дополнительно определяет последнюю дату периода выбора. По умолчанию: Now

</div>

<div>

## <a name="example"></a>Пример

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

## <a name="persistent-chat-stress-tool"></a>Инструмент «стресс» сохраняемого чата

<div>

## <a name="description"></a>Описание

Инструмент «стресс» сохраняемый чат обеспечивает простой способ моделирования использования сохраняемого чата для тестирования реальной производительности, включая различные пользовательские модели, чтобы лучше соответствовать ожидаемым сценариям использования.

</div>

<div>

## <a name="requirements"></a>Требования

Установите средства набора ресурсов сохраняемого чата на компьютер, подключенный к домену, который имеет доступ к сохраняемой резервной базе данных чата.

В дополнение к этому компьютеру *контроллера* вам понадобятся несколько машин *Loader* . Для каждых 10 000 пользователей в пользовательской модели вам понадобится не менее 4 ГБ оперативной памяти на машине загрузчика. Например, для работы с пользователями 80K потребуется около 32 ГБ ОЗУ на всех машинах загрузчика. Мы рекомендуем использовать как минимум три компьютера загрузчика, независимо от ожидаемой нагрузки.

На компьютерах загрузчика должна быть установлена платформа .NET 4,5, а также распространяемый компонент Visual C++ 2012.

</div>

<div>

## <a name="configuration"></a>Конфигурация

Скопируйте файлы ChatStressTool в общую папку, доступную на всех машинах загрузчика.

Создание пользователей и каналов для использования в нагрузочном прогоне.

  - Создавайте как можно больше пользователей, для которых используется модель пользователя, включите их в Lync и установите для них параметр "сохраняемая политика чата".

  - Создайте категорию для каналов стресс-, а затем создайте столько комнат, сколько необходимо для этой категории. У категории должны быть все повременные пользователи в списке **разрешенных** пользователей (с учетом их подразделений), а в помещениях для нагрузки должны быть установлены параметры конфиденциальности **Open**.

  - Мы рекомендуем создавать дополнительные помещения для нагрузки. Для создания комнат 50 000 можно использовать следующую команду интерфейса командной строки Windows PowerShell:
    ```Powershell
        for ($i = 0; $i -le 50000; $i++) { New-CsPersistentChatRoom -Category <parent category> -Name "StressChan_$i" -Privacy Open }
    ```    

Измените файлы конфигурации в соответствии с вашей топологией.

В **LoaderProcess.exe.config** замените значение "Controller.contoso.com" на полное доменное имя (FQDN) контроллера компьютера.

В **StressLauncher.exe.config:**

1.  Измените значение параметра "LoaderBinary" на путь к общей папке.

2.  Измените "AdminUser"/"AdminPassword" на учетные данные, которые имеют административный доступ к компьютерам загрузчика.

3.  Измените "ChannelCategory" на название категории, для которой созданы каналы нагрузки.

4.  Измените "UserNamePattern" и "UserPasswordPattern" на шаблон, соответствующий вашим учетным данным пользователя. {0} заменяется номером индекса пользователя.

5.  Замените слово Domain на домен SIP для топологии тестирования.

6.  Измените "ConnectionString" на строку подключения для сохраняемой серверной базы данных чата.

7.  Замените значение "UserIndexStart" индексом первого пользователя, который повлияет на погрузку.

8.  Измените значение "LyncFQDN" на полное доменное имя пула переднего плана.

9.  Измените список "machines", чтобы включить имена компьютеров для всех компьютеров загрузчика.

10. Измените значение baseAddress конечной точки службы (по умолчанию — "controller.contoso.com") до полного доменного имени компьютера контроллера.

</div>

<div>

## <a name="usage"></a>Режим

После завершения настройки откройте StressLauncher.exe на компьютере контроллера. Вы можете запустить StressLauncher как любой пользователь. Учетные данные, под которыми запускается процесс загрузчика на компьютерах загрузчика, должны быть указаны в файле конфигурации. Кроме того, необходимо предоставить строку подключения, которая имеет доступ на чтение к сохраняемой серверной базе данных чата. Если строка подключения использует встроенную проверку подлинности Windows, необходимо запустить StressLauncher как пользователя с этим доступом.

При необходимости измените параметры пользовательской модели. Нажмите кнопку **начать загрузку** , чтобы начать выполнение. После минуты пользователь начнет вход в систему, а индикатор выполнения начнет заполняться. На этом этапе вы можете использовать контроллеры компьютера и получить измерения производительности.

</div>

</div>

<div>

## <a name="chatupgradeverifier"></a>ChatUpgradeVerifier

<div>

## <a name="description"></a>Описание

ChatUpgradeVerifier — это специальный инструмент для сравнения баз данных в чате. Это средство сравнивает базу данных группового чата 2007 R2 или Group Chat 2010 (2007/2010Db) с базой данных сохраняемого чата 2013 (2013Db).

Это средство проверит, отображается ли оно на одной категории, в области "сохраняемый чат", а надстройка в выпуске в Office 2007 или 2010Db. Сравнение включает проверку всех параметров в категории, комнаты чата или надстройки, любые участники в области в этой категории и любые участники роли в этой категории либо в комнате чата. Если категория или комната чата не отображаются должным образом в 2013Db, эти различия будут выводиться в файл конфликтов. Если после завершения обновления Office 2007 или 2010Db изменится, а затем запускается это средство, в файле конфликтов будет выводиться разница. Обратите внимание, что это приложение является только средством сравнения баз данных и не проверяет процесс обновления.

</div>

<div>

## <a name="requirements"></a>Требования

Установка средств набора ресурсов сохраняемого чата на компьютере, подключенном к домену, который имеет доступ к сохраняемым внутренним базам данных чата (предыдущим и текущим версиям для сохраняемого чата).

Учетная запись пользователя, с помощью которой запускается средство, должна иметь доступ на чтение к базам данных сохраняемого чата.

Файл ChatUpgradeVerifier.exe.config должен содержать либо параметр GroupChat2007R2Db, либо параметр GroupChat2010Db со строкой подключения к соответствующей базе данных группового чата (Groupchat 2007R2 или 2010). Кроме того, он должен содержать параметр PersistentChat2013Db со строкой соединения с базой данных сохраняемого чата-2013.

</div>

<div>

## <a name="usage"></a>Режим

Запустите **ChatUpgradeVerifier** без каких бы то ни было параметров.

</div>

<div>

## <a name="example"></a>Пример

![Запуск ChatUpgradeVerifier.exe.](images/JJ945599.4c273bc3-7926-47c7-ade7-34522721ebf9(OCS.15).jpg "Запуск ChatUpgradeVerifier.exe.")

</div>

</div>

<div>

## <a name="persistent-chat-usage-report"></a>Отчет об использовании сохраняемого чата

<div>

## <a name="description"></a>Описание

Средство ChatUsageReport создает HTML-отчет по использованию службы сохраняемого чата.

</div>

<div>

## <a name="requirements"></a>Требования

Установите средства набора ресурсов сохраняемого чата на компьютере, подключенном к домену, который имеет доступ к сохраняемой резервной базе данных чата.

Учетная запись пользователя, с помощью которой запускается инструмент, должна иметь доступ на чтение к сохраняемой обратной стороне чата.

Файл ChatUsageReport.exe.config должен содержать \<connectionStrings\> раздел, определяющий строку подключения для сохраняемой серверной базы данных чата. Содержимое файла конфигурации по умолчанию включается здесь для ссылки.

</div>

<div>

## <a name="usage"></a>Режим

```Powershell
    ChatUsageReport [-StartDate {date}] [-EndDate {date}] [-TopActiveUsers {n}] [-TopActiveRooms {n}] [-LeastActiveRooms {n}] [-RoomsInactiveSince {Date}] [-OutputFolder {path}]
```
Эти параметры определяют выбор данных:

**StartDate (Дата** начала): При необходимости определяет дату начала периода выбора в формате UTC. По умолчанию: ранняя дата

**Дата окончания:** При необходимости определяет дату окончания периода выбора в формате UTC. По умолчанию: Now

Эти параметры определяют, как и какие данные отображаются.

**TopActiveUsers:** Если указан этот параметр, в отчет будут включены n наиболее активных пользователей в соответствии с количеством сообщений, опубликованных пользователем в комнате чата в течение выбранного периода. По умолчанию: 10

**TopActiveRooms:** Если указан этот параметр, в отчет будут включены n самых активных комнат чата в соответствии с количеством сообщений, опубликованных в комнате за выбранный период. По умолчанию: 10

**LeastActiveRooms:** Если указан этот параметр, в отчете будут содержаться как минимум активные комнаты чата в соответствии с количеством сообщений, опубликованных в комнате чата за выбранный период. У комнат будет хотя бы одно сообщение. По умолчанию: 10

**RoomsInactiveSince:** Если задано значение, отчет будет включать список комнат чатов, которые были неактивны с момента указанной даты. По умолчанию: все время

**OutputFolder:** Папка, в которой будут помещены ChatUsageReport.html и рисунки диаграммы. Это значение должно быть определено в файле конфигурации или в командной строке.

Все значения параметров командной строки также можно указать в файле ChatUsageReport.exe.config, который находится в том же каталоге, что и инструмент. Если в файле конфигурации и в командной строке задано какое либо значение, значение из командной строки будет переопределяться в файле конфигурации.

</div>

<div>

## <a name="output"></a>Выходные данные

В отчет всегда будут включены следующие выходные данные:

  - Первые n самых активных комнат чата по количеству записей в сообщении за выбранный период.

  - Первые n наиболее активных пользователей по количеству записей сообщений за выбранный период.

  - Первые n наименее активные комнаты чата по количеству записей в сообщении за выбранный период.

  - Комнаты чата, неактивные для полного существования базы данных или в соответствии с указанной датой.

  - Ежедневная Разноска сообщения за выбранный период.

  - Еженедельное сообщение о тенденциях за выбранный период.

  - Месячная тенденция сообщения за выбранный период.

  - Общее количество записей в сообщении за выбранный период.

  - Общее количество включенных комнат.

</div>

<div>

## <a name="example"></a>Пример

В следующем примере показано создание отчета об использовании для всего 2001 года и последующее сообщение будет помещено в OutputFolder, указанное в ChatUsageReport.exe.config.

```Powershell
    ChatUsageReport -RoomsInactiveSince 06-20-2010
```
ChatUsageReport.exe.config:

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

## <a name="scheduleadsyncforprincipal"></a>ScheduleADSyncForPrincipal

<div>

## <a name="description"></a>Описание

ScheduleADSyncForPrincipal — это сценарий Microsoft SQL Server 2012, который необходимо запускать непосредственно из SQL Server Management Studio при подключении к сохраняемой обратной стороне чата в базе данных. Этот сценарий позволяет принудительно использовать сохраняемый чат для синхронизации записей пользователя с данными из доменных служб Active Directory, а не ждать запланированного времени синхронизации.

</div>

<div>

## <a name="requirements"></a>Требования

Учетная запись пользователя, под которой запускается сценарий, должна иметь доступ владельца к сохраняемой резервной базе данных чата.

</div>

<div>

## <a name="usage"></a>Режим

Ниже приведено содержимое сценария по умолчанию.

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

</div>

</div>

</div>

<span> </span>

</div>

</div>

</div>

