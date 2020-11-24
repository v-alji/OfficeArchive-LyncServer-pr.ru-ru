---
title: Удаление базы данных SQL Server для пула переднего плана
description: Удалите базу данных SQL Server для пула переднего плана.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Remove the SQL Server database for a Front End pool
ms:assetid: 6bb932df-3ed7-49b6-ae17-61e4c6a5fe82
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688084(v=OCS.15)
ms:contentKeyID: 49733681
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 01c5d47e4c52197c5792fa3b7770da7bbd1b26cb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49400075"
---
# <a name="remove-the-sql-server-database-for-a-front-end-pool"></a>Удаление базы данных SQL Server для пула переднего плана

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-10-04_

После удаления пула переднего плана Microsoft Lync Server 2010 или повторной настройки пула для использования другой базы данных вы можете удалить базы данных SQL Server, на которых размещены данные пула. Используйте описанные ниже процедуры для удаления определений из построителя топологии и удаления файлов базы данных и журнала с сервера базы данных.

<div>

## <a name="to-remove-the-sql-server-database-using-topology-builder"></a>Удаление базы данных SQL Server с помощью построителя топологии

1.  На сервере переднего плана Lync Server 2013 откройте "Построитель топологии" и скачайте существующую топологию.

2.  В построителе топологии выберите **Общие компоненты** , а затем — **хранилище SQL Server**, щелкните правой кнопкой мыши экземпляр SQL Server, связанный с удаленным или перенастроенным пулом переднего плана, и выберите команду **Удалить**.

3.  Опубликуйте топологию и проверьте состояние репликации.

</div>

<div>

## <a name="to-remove-user-and-application-databases-from-the-sql-server"></a>Удаление баз данных пользователей и приложений из SQL Server

1.  Для удаления баз данных на сервере SQL Server необходимо быть членом группы "Администраторы SQL Server" для сервера SQL Server, на котором нужно удалить файлы базы данных.

2.  Открытие командной консоли Lync Server

3.  Чтобы удалить базу данных из хранилища пользователей пула, введите:
    
        Uninstall-CsDataBase -DatabaseType User -SqlServerFqdn <FQDN> [-SqlInstanceName <instance>]
    
    Здесь \<FQDN\> указано полное доменное имя сервера базы данных (FQDN) и \<instance\> — именованный экземпляр базы данных (то есть, если он был определен).

4.  Чтобы удалить базу данных из хранилища приложений пула, введите:
    
        Uninstall-CsDataBase -DatabaseType Application -SqlServerFqdn <FQDN> [-SqlInstanceName <instance>]
    
    Где \<FQDN\> находится полное доменное имя сервера базы данных и \<instance\> является экземпляром именованной базы данных (то есть, если оно определено).

5.  Когда командлет **uninstall-CsDataBase** предложит вам подтвердить действия, прочтите информацию, а затем нажмите клавишу **Y** (или клавишу ВВОД), чтобы продолжить, **или клавишу с, чтобы** остановить командлет (то есть ошибки).

</div>

</div>

<span> </span>

</div>

</div>

</div>

