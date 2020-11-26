---
title: 'Lync Server 2013: подготовка схемы Active Directory'
description: 'Lync Server 2013: подготовка схемы Active Directory.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Preparing the Active Directory schema
ms:assetid: 067726ae-fd3f-4133-a32f-26d2603ac674
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398119(v=OCS.15)
ms:contentKeyID: 48183300
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3df7533dcbabe278fd366b441cfd8daa83f54b23
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424116"
---
# <a name="preparing-the-active-directory-schema-in-lync-server-2013"></a>Подготовка схемы Active Directory в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-08-27_

Прежде чем приступить к подготовке доменных служб Active Directory, вы можете открыть файлы схемы в текстовом редакторе, например в блокноте Windows, или [2013](lync-server-2013-active-directory-schema-extensions-classes-and-attributes-used-by-lync-server.md) ознакомиться с расширениями схемы доменных служб Active Directory, которые будут изменены для lync Server 2013. Lync Server использует четыре файла схемы:

  - ExternalSchema. ldf, который используется для взаимодействия с сервером Microsoft Exchange Server

  - ServerSchema. ldf, являющийся основным файлом схемы Lync Server 2013

  - BackCompatSchema. ldf, который используется для взаимодействия с любыми компонентами предыдущих выпусков

  - VersionSchema. ldf, который используется для получения сведений о версии подготовленной схемы

Все LDF-файлы устанавливаются во время подготовки схемы, независимо от того, выполняется ли миграция из предыдущего выпуска или выполняется чистая установка. Эти файлы схемы устанавливаются в последовательности, указанной в предыдущем списке, и находятся в \\ \\ папке схемы поддержки на установочном носителе.

Расширения схемы Lync Server реплицируются по всем доменам, что влияет на сетевой трафик. Выполняйте подготовку схемы по истечении уровня использования сети.

<div>


> [!NOTE]  
> Если вам нужно добавить поддержку для Microsoft® Office Communicator Mobile 2007 R2 для Java и Microsoft® Office Communicator Mobile 1,0 для мобильных клиентов в среде Lync Server 2013, вам нужно подготовить схему Active Directory для Microsoft Office Communications Server 2007 R2 во время установки Lync Server 2013. Необходимое программное обеспечение и документацию можно найти в разделе <A href="https://go.microsoft.com/fwlink/p/?linkid=207172">https://go.microsoft.com/fwlink/p/?linkId=207172</A> .



</div>

<div>

## <a name="adsi-edit"></a>Редактирование ADSI

Редактор интерфейсов служб Active Directory (Редактирование ADSI) — это средство администрирования доменных служб, которое можно использовать для проверки подготовки и репликации схемы.

Редактирование ADSI устанавливается по умолчанию при установке роли AD DS, чтобы сделать сервер контроллером домена. В Windows Server 2008 и Windows Server 2008 R2 средство редактирования ADSI (adsiedit. msc) входит в состав средств удаленного администрирования сервера (RSAT). Вы также можете установить RSAT на рядовые серверы домена или отдельные серверы. Пакет RSAT копируется на эти серверы по умолчанию при установке Windows, но не устанавливается по умолчанию. Отдельные инструменты устанавливаются с помощью диспетчера сервера. Редактирование ADSI входит в раздел **средства администрирования ролей**, **средства доменных служб Active Directory**, **средства контроллера домена Active Directory**.

В Windows Server 2003 Редактирование ADSI входит в состав средств поддержки. Средства поддержки доступны на компакт-диске Windows Server 2003 в \\ \\ папке "средства поддержки", а также в разделе "windows Server 2003 с пакетом обновления 2 32-разрядная версия для поддержки" [https://go.microsoft.com/fwlink/p/?linkId=125770](https://go.microsoft.com/fwlink/p/?linkid=125770) . Инструкции по установке средств поддержки с компакт-диска продукта можно найти в разделе "Установка средств поддержки Windows" на сайте [https://go.microsoft.com/fwlink/p/?linkId=125771](https://go.microsoft.com/fwlink/p/?linkid=125771) . Adsiedit.dll автоматически регистрируется при установке средств поддержки. Тем не менее, если вы скопировали файлы на свой компьютер, необходимо выполнить команду **regsvr32** , чтобы зарегистрировать файл adsiedit.dll, прежде чем можно будет запустить средство.

</div>

<div>

## <a name="in-this-section"></a>Содержание

  - [Проведение подготовки схемы Active Directory в Lync Server 2013](lync-server-2013-running-schema-preparation.md)

  - [Проверка репликации схемы в Lync Server 2013](lync-server-2013-verifying-schema-replication.md)

</div>

<div>

## <a name="see-also"></a>См. также


[Подготовка леса для Lync Server 2013](lync-server-2013-preparing-the-forest.md)  
[Подготовка доменов для Lync Server 2013](lync-server-2013-preparing-domains.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

