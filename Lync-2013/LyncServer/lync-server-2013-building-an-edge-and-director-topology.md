---
title: 'Lync Server 2013: создание топологии пограничных серверов и директора'
description: 'Lync Server 2013: создание топологии EDGE и Director.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Building an edge and Director topology
ms:assetid: 11e5759e-d69f-4c39-8994-f467c279c558
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398202(v=OCS.15)
ms:contentKeyID: 48183451
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bcb2d422136cf0a421c68ebc2adba50f03c5cc85
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435938"
---
# <a name="building-an-edge-and-director-topology-in-lync-server-2013"></a>Создание топологии пограничных серверов и директора в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-09-08_

Построение топологии включает следующие задачи планирования и развертывания.

  - **Планирование**   Необходимо определить подходящую топологию для своей организации и определить компоненты, необходимые для ее развертывания. Это стандартные действия, которые можно выполнить в процессе планирования. Microsoft Lync Server 2013, средство планирования, предоставленное в Lync Server 2013, упрощает процесс планирования, а также позволяет легко вносить изменения при завершении требований и планов.

  - **Развертывание**   Топология, определенная с помощью Topology Builder, очень важна для развертывания любого сервера Lync Server 2013. Если вы не закончите определение и публикацию топологии с помощью построителя топологии в ходе планирования, необходимо завершить ее и опубликовать топологию перед развертыванием пограничных серверов.

Вы не можете развертывать компоненты пограничного сервера, пока не разворачиваете по крайней мере один внутренний пул, и вам необходимо установить построитель топологии, чтобы развернуть внутренний пул. В этом разделе не рассматривается установка Topology Builder, так как это является частью процесса установки внутреннего пула.

Подробнее об этих средствах см. [в разделе Контрольный список развертывания для внешних пользователей Access в Lync Server 2013](lync-server-2013-deployment-checklist-for-external-user-access.md).

<div>


> [!NOTE]  
> Если вы ранее использовали Topology Builder, чтобы определить полную топологию, включая топологию пограничного, вы можете пропустить <A href="lync-server-2013-define-your-edge-topology.md">Определение топологии пограничного сервера в Lync server 2013</A> и <A href="lync-server-2013-publish-your-topology.md">опубликовать свою топологию в Lync Server 2013</A> для задач, описанных в этом разделе, но вам нужно выполнить <A href="lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md">экспорт топологии сервера Lync Server 2013 и скопировать ее на внешние носители для установки пограничного устройства</A> .



</div>

<div>

## <a name="in-this-section"></a>Содержание

  - [Определение пограничной топологии в Lync Server 2013](lync-server-2013-define-your-edge-topology.md)

  - [Определение дополнительных топологий директоров в топологии для Lync Server 2013](lync-server-2013-define-optional-director-topologies-in-your-topology.md)

  - [Публикация топологии в Lync Server 2013](lync-server-2013-publish-your-topology.md)

  - [Экспорт топологии Lync Server 2013 и ее копирование на внешние носители для установки в пограничной топологии](lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md)

</div>

</div>

<span> </span>

</div>

</div>

</div>

