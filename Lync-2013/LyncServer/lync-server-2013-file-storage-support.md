---
title: 'Lync Server 2013: поддержка хранения файлов'
description: Поддержка хранения файлов в Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: File storage support
ms:assetid: ed66430d-3c19-4267-938c-956a51005073
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399073(v=OCS.15)
ms:contentKeyID: 48185743
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 03b7c3379c6aad6283f6a55b991ebaec50044bda
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428183"
---
# <a name="file-storage-support-in-lync-server-2013"></a>Поддержка хранения файлов в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-10-16_

Lync Server 2013 использует одно и то же хранилище файлов для хранения всех файлов. Поддержка хранения файлов включает следующие возможности:

  - Файловый общий доступ на запоминающем устройстве (DAS) или в сети хранения данных (SAN), включая распределенную файловую систему (DFS), а также на резервный массив независимых дисков (RAID) для хранения файлов. Сведения о требованиях к хранению можно найти в статьях [технические требования к серверам переднего плана, мгновенным сообщениям и сведениям о присутствии в Lync server 2013](lync-server-2013-technical-requirements-for-front-end-servers-instant-messaging-and-presence.md) , а также [о требованиях к оборудованию и программному обеспечению для директора в Lync Server 2013](lync-server-2013-hardware-and-software-requirements-for-the-director.md) Подробные сведения о DFS для операционной системы Windows Server 2008 можно найти в пошаговом руководстве по DFS для Windows Server 2008 по адресу [https://go.microsoft.com/fwlink/p/?linkId=202835](https://go.microsoft.com/fwlink/p/?linkid=202835) .

  - Общий кластер для общего доступа к файлам. Если вы пользуетесь общим кластером, вы должны использовать кластерные серверы под управлением Windows Server 2008 или Windows Server 2008 R2. Использование серверов кластера, работающих под управлением более ранней версии Windows, может привести к проблемам с разрешениями, которые не позволяют получить доступ к некоторым функциям. Для создания общих файловых ресурсов используйте администратор кластеров. Подробнее об использовании администратора кластера можно найти в статье 284838 базы знаний Майкрософт, посвященной созданию общего файлового файла кластера сервера с Cluster.exe " [https://go.microsoft.com/fwlink/p/?linkId=140899](https://go.microsoft.com/fwlink/p/?linkid=140899) .

</div>

<span> </span>

</div>

</div>

</div>

