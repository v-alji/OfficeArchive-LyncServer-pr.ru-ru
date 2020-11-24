---
title: 'Lync Server 2013: технические требования к парковке вызовов'
description: 'Lync Server 2013: технические требования для приостановки звонка.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Technical requirements for Call Park
ms:assetid: 38bcf302-2b72-4492-9266-f6dc31b566e1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204818(v=OCS.15)
ms:contentKeyID: 48183897
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6ddc17b40f78c42c090d1a87b4580ebdad0a07f6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399232"
---
# <a name="technical-requirements-for-call-park-in-lync-server-2013"></a>Технические требования к парковке вызовов в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2013-11-07_

В этом разделе описаны указанные ниже технические требования к приостановке звонков.

  - Требования к оборудованию

  - Требования к программному обеспечению

  - Требования к портам

  - Требования к звуковым файлам

<div>

## <a name="hardware-requirements"></a>Требования к оборудованию

Приложение для парковки звонков имеет те же аппаратные требования, что и внешние серверы. Сведения о требованиях к оборудованию можно найти в документации [серверные платформы для Lync server 2013](lync-server-2013-server-hardware-platforms.md) .

</div>

<div>

## <a name="software-requirements"></a>Требования к программному обеспечению

Приложение для парковки звонков имеет те же требования к операционной системе и необходимые компоненты по отношению к серверам переднего плана. Подробные сведения о требованиях к программному обеспечению можно найти [в разделе Поддержка серверов и средств операционной системы в Lync Server 2013](lync-server-2013-server-and-tools-operating-system-support.md) в документации по поддержке.

На всех серверах переднего плана и стандартных серверах, где развернуто приложение для остановки приема звонков, должна быть установлена среда выполнения формата Windows Media для серверов с операционной системой Windows Server 2008 R2 или Microsoft Media Foundation для серверов под управлением Windows Server 2012 или Windows Server 2012 R2. В операционной системе Windows Server 2008 R2 на компьютере с Windows можно установить среду выполнения формата Windows Media Format. Формат среды выполнения Windows Media Audio (WMA), необходимый для воспроизведений музыкальных файлов, используется для воспроизведения музыки на удержании.

</div>

<div>

## <a name="port-requirements"></a>Требования к портам

Приложение для парковки звонков использует следующий порт:

  - **Порт 5075**   Служит для запросов на прослушивание по протоколу SIP.

<div>


> [!NOTE]  
> Этот порт — это параметр по умолчанию, который можно изменить с помощью командлета <STRONG>Set-CsApplicationServer</STRONG> . Подробные сведения об этом командлете можно найти в документации по оболочке Lync Server Management Shell.



</div>

</div>

<div>

## <a name="audio-file-requirements"></a>Требования к аудиофайлам

Приложение для парковки звонков поддерживает только файлы Windows Media Audio (WMA) для музыки на удержании. Чтобы настроить файлы для воспроизведения в качестве музыки в режиме удержания, можно использовать Microsoft Expression Encoder 4. Загрузить Expression Encoder 4 можно в разделе "Expression Encoder 4" [https://go.microsoft.com/fwlink/p/?linkId=202843](https://go.microsoft.com/fwlink/p/?linkid=202843) . Это средство используется для преобразования файлов в формат WMA. Рекомендуемый формат музыкальных файлов на входе в службу для парковки — это Media Audio 9, 44 кГц, 16 бит, моно, CBR, 32 кбит/с.

<div>


> [!NOTE]  
> Преобразованный файл воспроизводится на телефоне только при 16 кГц, даже если он был записан при 44 кГц.



</div>

</div>

</div>

<span> </span>

</div>

</div>

</div>

