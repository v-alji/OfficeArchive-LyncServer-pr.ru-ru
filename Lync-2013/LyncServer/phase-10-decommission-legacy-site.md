---
title: 'Этап 10: списание устаревшего сайта'
description: 'Этап 10: списание устаревшего сайта.'
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: 'Phase 10: Decommission legacy site'
ms:assetid: d591a310-3b5c-4092-b19e-0349616e40df
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205300(v=OCS.15)
ms:contentKeyID: 48185540
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9692301a1da38cfd69780ce2524f00dd428454e5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443274"
---
# <a name="phase-10-decommission-legacy-site"></a>Этап 10: списание устаревшего сайта

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-10-16_

В следующих разделах приведены рекомендации по удалению пулов и отключению серверов и пулов из устаревшего развертывания Office Communications Server 2007 R2. Не все процедуры, перечисленные в этом разделе, являются обязательными. Ознакомьтесь со сведениями в каждом из этих разделов, чтобы определить, какую процедуру списания следует использовать.

<div>


> [!WARNING]  
> Если вы импортировали каталоги конференций для конференц-связи с телефонным подключением на Lync Server 2013, важно перейти в каталог конференции на Lync Server 2013, прежде чем приступить к списанию пулов. Если вы списать пул без предварительного перехода в каталог конференц-связи, функция телефонного подключения для всех перенесенных собраний перестанет работать. Вы должны выполнить шаг для смены владельца для каждой из каталогов конференции в пуле старого.



</div>

<div>


> [!IMPORTANT]  
> Сведения о переносе и обновлении приложений для управляемых API Microsoft Unified Communications (UCMA) перед списанием устаревшей среды можно найти в разделе <A href="https://go.microsoft.com/fwlink/p/?linkid=269555">https://go.microsoft.com/fwlink/p/?LinkId=269555</A>



</div>

<div>

## <a name="in-this-section"></a>Содержание

  - [Перемещение каталогов конференций](move-conference-directories.md)

  - [Обновление записей DNS SRV](update-dns-srv-records.md)

  - [Списание серверов и групп](decommissioning-servers-and-pools.md)

  - [Удалить BackCompatSite](remove-backcompatsite.md)

</div>

</div>

<span> </span>

</div>

</div>

</div>

