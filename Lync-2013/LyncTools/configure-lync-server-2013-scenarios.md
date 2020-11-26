---
title: Настройка сценариев Lync Server 2013
description: Настройте сценарии Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure Lync Server 2013 Scenarios
ms:assetid: 6705346b-1512-4af3-85e4-64dfa6ee6f80
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945596(v=OCS.15)
ms:contentKeyID: 51541420
ms.date: 12/28/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c4a5b7bd271191067779ac358807cc54918b16bc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440075"
---
# <a name="configure-lync-server-2013-scenarios"></a>Настройка сценариев Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2016-12-28_

Для запуска средства нагрузки и производительности Lync Server 2013 (LyncPerfTool) необходимо сначала настроить топологию Lync Server 2013 для сценариев, которые будут выполняться. Если Lync Server 2013 не настроен или настроен неправильно, в большинстве случаев происходит сбой нагрузочного моделирования. С помощью средства нагрузки и производительности Lync Server 2013 мы предоставили примеры сценариев командной консоли Lync Server Management Shell и базовых файлов ресурсов, которые можно использовать в качестве отправной точки для настройки Lync Server 2013. В этом разделе описаны указанные примеры Windows PowerShell. Обратите внимание, что этот раздел не предназначен для того, чтобы описать, как настроить Lync Server 2013 в целом. Подробные сведения о работе с Windows PowerShell в Lync Server 2013 можно найти в документации по оболочке Lync Server Management Shell по адресу <https://technet.microsoft.com/library/gg398474.aspx> .

<div>

## <a name="about-running-lync-server-management-shell-scripts"></a>Сведения о выполнении сценариев оболочки Lync Server Management Shell

Мы предоставили примеры сценариев командной консоли Lync Server, которые можно использовать для подготовки к запуску моделирования нагрузки. Так как сценарии предназначены для моделирования нагрузки, они являются простыми и разрешительнои и, следовательно, могут быть не подходящими к производству. Все сценарии являются примерами и должны быть проверены, а в некоторых случаях — в соответствии с вашей топологией. Как минимум, мы ожидаем, что сценарий службы группы ответа потребуется изменить, чтобы указать агенты, назначенные группам агента. Однако у вас есть возможность не моделировать эту загрузку.

<div>


> [!WARNING]  
> Будьте внимательны и позаботьтесь о том, как ознакомиться с приведенными примерами. Сценарии будут переопределять любые существующие параметры в топологии.



</div>

<div>


> [!NOTE]  
> Подробнее об использовании Windows PowerShell и командной консоли Lync Server можно найти в блоге Lync Server 2013 Windows PowerShell по адресу <A href="https://go.microsoft.com/fwlink/?linkid=203150">https://go.microsoft.com/fwlink/?LinkId=203150</A> .



</div>

</div>

<div>

## <a name="stress-and-performance-tool-client-version-monikers"></a>Специальные имена в клиентской программе для средства нагрузки и производительности

Если вы изменили настройки из значений по умолчанию, вам может потребоваться настроить политику проверки версии клиента. Подробные сведения можно найти в разделе "Настройка поддерживаемых клиентских версий" <https://technet.microsoft.com/library/gg412832(v=ocs.15).aspx> . При общении с Lync Server 2013 средство "стресс и производительность" Lync Server 2013 по умолчанию использует следующие версии агента пользователя.

  - LSPT/15.0.0.0 (средство для Lync Server 2013 с функцией нагрузки и производительности)

  - OCPHONE/.0.522

Они предназначены для клиента Mobility (UCWA) в LyncPerfTool:

  - Средство для Ucwa производительности и веб-конференции

  - Средство для Ucwa производительности и мобильные телефоны

</div>

</div>

<span> </span>

</div>

</div>

</div>

