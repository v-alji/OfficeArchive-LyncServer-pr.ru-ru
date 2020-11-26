---
title: 'Lync Server 2013: требования к инфраструктуре Active Directory'
description: 'Lync Server 2013: требования инфраструктуры Active Directory.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Active Directory infrastructure requirements
ms:assetid: c2086f7b-662f-4179-ab99-2c0311ebd903
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412955(v=OCS.15)
ms:contentKeyID: 48185318
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 62218605c9b3fac20743d0b6bb475515c9498f9a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439417"
---
# <a name="active-directory-infrastructure-requirements-for-lync-server-2013"></a>Требования к инфраструктуре Active Directory для Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2013-11-07_

Прежде чем приступить к подготовке доменных служб Active Directory для Lync Server 2013, убедитесь, что инфраструктура Active Directory удовлетворяет следующим требованиям:

  - Все контроллеры домена (включая все серверы глобального каталога) в лесу, где развертывается сервер Lync Server, работают под управлением одной из следующих операционных систем.
    
      - Операционная система Windows Server 2012 R2
    
      - Операционная система Windows Server 2012
    
      - Операционная система Windows Server 2008 R2
    
      - Операционная система Windows Server 2008
    
      - Windows Server 2008 Enterprise 32-bit
    
      - 32-разрядная или 64-разрядная версии операционной системы Windows Server 2003 R2
    
      - 32-разрядная или 64-разрядная версии операционной системы Windows Server 2003

  - Все домены, в которых развертывается сервер Lync Server, порождаются на функциональном уровне домена Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2, Windows Server 2008 или не ниже Windows Server 2003.

  - Лес, в котором развертывается сервер Lync Server, передается на функциональный уровень леса Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2, Windows Server 2008 или хотя бы Windows Server 2003 или более поздней версии.
    
    <div>
    

    > [!NOTE]  
    > Чтобы изменить функциональный уровень домена или леса, ознакомьтесь со статьей "создание функциональных уровней домена и леса" в библиотеке TechNet по адресу <A href="https://go.microsoft.com/fwlink/p/?linkid=263775">https://go.microsoft.com/fwlink/p/?LinkId=263775</A> .

    
    </div>

  - Глобальный каталог разворачивается во всех доменах, где развертываются компьютеры или пользователи Lync Server.

Lync Server 2013 поддерживает универсальные группы в операционных системах Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2, Windows Server 2008 и Windows Server 2003. Members of universal groups can include other groups and accounts from any domain in the domain tree or forest and can be assigned permissions in any domain in the domain tree or forest. Поддержка универсальной группы в сочетании с делегированием администратора упрощает управление развертыванием Lync Server. For example, it is not necessary to add one domain to another to enable an administrator to manage both.

</div>

<span> </span>

</div>

</div>

</div>

