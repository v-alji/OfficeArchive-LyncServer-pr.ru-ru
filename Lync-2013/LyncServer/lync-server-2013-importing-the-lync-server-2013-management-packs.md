---
title: 'Lync Server 2013: Импорт пакетов управления Lync Server 2013'
description: 'Lync Server 2013: Импорт пакетов управления Lync Server 2013.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Importing the Lync Server 2013 management packs
ms:assetid: 846287e1-660f-453f-bdba-b2137b5f0ea1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205052(v=OCS.15)
ms:contentKeyID: 48184690
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c9615e559baf2f1c8b99015f1e407230559ff770
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427329"
---
# <a name="importing-the-lync-server-2013-management-packs"></a>Импорт пакетов управления Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-10-22_

Вы можете расширять возможности System Center Operations Manager, устанавливая пакеты управления (программное обеспечение, которое определяет, какие элементы отслеживается System Center Operations Manager) и как должны отслеживаться эти элементы, а также как они должны быть отправлены и переданы. Lync Server 2013 включает два пакета управления System Center Operations Manager, которые предоставляют следующие возможности:

  - Пакет управления компонентом и пользовательским интерфейсом (Microsoft.LS.2013.Monitoring.ComponentAndUser.mp) отслеживает проблемы Lync Server, записанные счетчиками производительности, которые регистрируются в журналах событий или записываются в записи сведений о вызовах (CDR) или в базе данных качества взаимодействия (QoE). Для критических проблем можно настроить System Center Operations Manager для немедленного уведомления администраторов с помощью электронной почты, обмена мгновенными сообщениями или службы коротких сообщений (SMS). SMS — это технология, используемая для отправки текстовых сообщений с одного мобильного устройства на другое.
    
    <div>
    

    > [!NOTE]  
    > Дополнительные сведения о настройке уведомлений Operations Manager можно найти в уведомлении о настройке в библиотеке TechNet по адресу <A href="https://go.microsoft.com/fwlink/p/?linkid=268785">https://go.microsoft.com/fwlink/p/?LinkId=268785</A> .

    
    </div>

  - Активный пакет управления мониторингом (Microsoft.LS.2013.Monitoring.ActiveMonitoring.mp) выполняет упреждающее тестирование основных компонентов сервера Lync, таких как вход в систему, Обмен мгновенными сообщениями и звонки на телефоны, находящиеся в телефонной сети общего пользования (PSTN). Эти тесты выполняются с помощью виртуальных командлетов транзакций Lync Server. Например, с помощью командлета **Test-CsIM** можно смоделировать беседу между пользователями (мгновенными сообщениями) между парой тестовых пользователей. Если это имитируемый разговор не порождает предупреждение.

Вам нужно импортировать пакеты управления. Если вы не импортируете пакеты управления, нельзя использовать Operations Manager для мониторинга событий сервера Lync Server и выполнения виртуальных транзакций Lync Server.

Пакет управления компонентом и пользовательским интерфейсом используется только для мониторинга сервера Lync Server 2013. Если у вас есть сценарий сосуществования, на котором установлены оба сервера Lync Server 2013 и Lync Server 2010, вы должны продолжать использовать пакеты управления Lync Server 2010 для компьютеров Lync Server 2010.

<div>


> [!NOTE]  
> Пакеты управления для Lync Server 2010 включают пакет управления для мониторинга Lync Server 2010 и пакет управления "Мониторинг группового чата" для Lync Server 2010.



</div>

Для импорта пакетов управления можно использовать следующие средства:

  - **System Center Operations Manager**   С помощью этого метода вы можете добавить мониторинг для Lync Server с помощью Operations Manager.

  - **Оболочка Operations Manager**   Для импорта и устранения проблем, возникающих при импорте пакетов управления с помощью консоли System Center Operations Manager, можно использовать командную консоль Operations Manager.

<div>

## <a name="importing-the-management-packs-by-using-system-center-operations-manager"></a>Импорт пакетов управления с помощью System Center Operations Manager

1.  Скачайте файлы Microsoft.LS.2013.Monitoring.ActiveMonitoring.mp и Microsoft.LS.2013.Monitoring.ComponentAndUser.mp.

2.  В System Center Operations Manager щелкните элемент **Администрирование**.

3.  В области " **Администрирование** " щелкните правой кнопкой мыши **пакеты управления** и выберите пункт **Импорт пакетов управления**.

4.  В диалоговом окне **Выберите пакеты управления** нажмите кнопку **Добавить**, затем щелкните **Добавить с диска**.

5.  В диалоговом окне **Подключение к каталогу в сети** нажмите кнопку **Отмена** , чтобы не допустить подключения Operations Manager к сети, чтобы узнать, существуют ли зависимости для пакетов управления Lync Server. Если вы используете System Center Operations Manager 2012, нажмите кнопку **нет**.

6.  В диалоговом окне **Выбор пакетов управления для импорта** найдите и выберите файлы **Microsoft.ls.2013.Monitoring.ActiveMonitoring.MP** и **Microsoft.ls.2013.Monitoring.ComponentAndUser.MP** , а затем нажмите кнопку **Открыть**. Чтобы выбрать несколько файлов в диалоговом окне, щелкните первый файл, удерживая нажатой клавишу CTRL, а затем щелкните второй файл.

7.  В диалоговом окне **Выберите пакеты управления** нажмите кнопку **Установить**. Сообщение об ошибке и сбой установки, как правило, указывают на то, что папка, в которой находятся файлы пакетов управления, защищена функцией контроля учетных записей Windows. Если это случится, скопируйте файлы в другую папку, а затем перезапустите процесс импорта и установки.

8.  В диалоговом окне **Выберите пакеты управления** нажмите кнопку **Закрыть**. Обратите внимание, что для завершения процесса импорта и установки может потребоваться несколько минут.

</div>

<div>

## <a name="importing-management-packs-by-using-the-operations-manager-shell"></a>Импорт пакетов управления с помощью оболочки Operations Manager

Обычно проще импортировать пакеты управления с помощью Operations Manager. Однако если возникает ошибка и импорт завершается сбоем, консоль не всегда предоставляет адекватные отчеты об ошибках. По сравнению с оболочкой Operations Manager выводятся подробные сведения. Если вы используете Operations Manager и при импорте пакета управления выполняются проблемы, импортируйте пакет с помощью оболочки Operations Manager. В командной консоли Operations Manager содержатся дополнительные сведения, которые могут помочь определить причину сбоя импорта.

Если вы используете System Center Operations Manager 2007 R2, выполните указанные ниже действия.

1.  Нажмите кнопку **Пуск**, выберите **все программы**, а затем **System Center Operations Manager 2007 R2** и выберите **Shell Operations Manager**.

2.  В командной строке Operations Manager введите указанную ниже команду, используя фактический путь к копии файла Microsoft.LS.2013.Monitoring.ActiveMonitoring.mp, и нажмите клавишу ВВОД.
    
        MPImport.exe D:\MP\Microsoft.LS.2013.Monitoring.ActiveMonitoring.mp

3.  После импорта первого пакета управления повторите процесс, указав путь к копии файла Microsoft.LS.2013.Monitoring.ComponentAndUser.mp:
    
        MPImport.exe D:\MP\Microsoft.LS.2013.Monitoring.ComponentAndUser.mp

4.  Закройте интерпретатор Operations Manager.

Если вы используете System Center Operations Manager 2012, выполните указанные ниже действия.

1.  Нажмите кнопку **Пуск** и щелкните **Все программы**, **Microsoft System Center 2012**, **Operations Manager**, затем **Оболочка Operations Manager**.

2.  В командной строке Operations Manager введите указанную ниже команду, используя фактический путь к копии файла Microsoft.LS.2013.Monitoring.ActiveMonitoring.mp, и нажмите клавишу ВВОД.
    
        Import-SCOMManagementPack -FullName "D:\MP\ Microsoft.LS.2013.Monitoring.ActiveMonitoring.mp"

3.  После импорта первого пакета управления повторите процесс, указав путь к копии файла Microsoft.LS.2013.Monitoring.ComponentAndUser.mp:
    
        Import-SCOMManagementPack -FullName "D:\MP\ Microsoft.LS.2013.Monitoring.ComponentAndUser.mp"

</div>

</div>

<span> </span>

</div>

</div>

</div>

