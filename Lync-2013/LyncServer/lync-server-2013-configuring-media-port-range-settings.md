---
title: 'Lync Server 2013: Настройка параметров диапазона портов мультимедиа'
description: 'Lync Server 2013: Настройка параметров диапазона портов мультимедиа.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring media port range settings
ms:assetid: 2c4b7c0b-0dce-48f4-a489-336d6e526f7c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204770(v=OCS.15)
ms:contentKeyID: 48183723
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1a7670284c593197068c366f43bbb3faaaad8f63
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432915"
---
# <a name="configuring-media-port-range-settings-in-lync-server-2013"></a>Настройка параметров диапазона портов мультимедиа в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-10-18_

Параметры диапазона портов мультимедиа могут значительно повлиять на производительность клиента и должны настраиваться. Эти параметры можно настроить с помощью командной консоли Lync Server Management Shell.

### <a name="media-port-range-settings"></a>Параметры диапазона портов мультимедиа

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Параметр</th>
<th>Описание</th>
<th>Командлет командной консоли Lync Server Management Shell</th>
<th>Параметры командлета</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Portrange\Enabled</p></td>
<td><p>Указывает, следует ли использовать для мультимедиа и сигналов диапазоны портов, отправленные сервером. Используется вместе с подзначениями MinMediaPort и MaxMediaPort.</p></td>
<td><p><strong>CsConferencingConfiguration</strong></p></td>
<td><p>ClientMediaPortRangeEnabled</p></td>
</tr>
<tr class="even">
<td><p>Portrange\MinMediaPort</p></td>
<td><p>Задает начальный номер порта, который будет использоваться для мультимедиа. Объединяется с MaxMediaPort, чтобы указать диапазон портов. Рекомендуемый минимальный диапазон составляет 40 портов.</p></td>
<td><p><strong>CsConferencingConfiguration</strong></p></td>
<td><p>ClientMediaPort (представляет начальный номер порта, используемый для мультимедиа клиента).</p></td>
</tr>
<tr class="odd">
<td><p>Portrange\MaxMediaPort</p></td>
<td><p>Указывает самый высокий номер порта, который будет использоваться для мультимедиа. Объединяется с MinMediaPort, чтобы указать диапазон портов. Рекомендуемый минимальный диапазон составляет 40 портов.</p></td>
<td><p><strong>CsConferencingConfiguration</strong></p></td>
<td><p>ClientMediaPortRange (указывает общее количество портов, доступных для клиентского носителя; значение по умолчанию — 40).</p></td>
</tr>
</tbody>
</table>


<div>

## <a name="to-configure-media-port-range-settings"></a>Настройка параметров диапазона портов мультимедиа

1.  Запустите командную консоль Lync Server Management Shell: нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft Lync Server 2013**, а затем — **Командная консоль Lync Server Management Shell**.

2.  Выполнить следующий командлет:
    
        Get-CsConferencingConfiguration
    
    Этот командлет возвращает параметры конфигурации Конференции.

3.  Выполните следующий командлет с параметрами и значениями, которые вы хотите изменить (Дополнительные сведения о параметрах этого командлета можно найти в документации на Lync Server Management Shell).
    
        Set-CsConferencingConfiguration
    
    <div>
    

    > [!NOTE]  
    > Вы можете создавать дополнительные наборы параметров настройки конференц-связи для определенных сайтов. Используйте командлет <STRONG>New-CsConferencingConfiguration</STRONG> с удостоверением сайта. При создании новых параметров конфигурации конференций для сайтов параметры сайта имеют приоритет над глобальными параметрами. Подробные сведения можно найти в руководстве по среде Lync Server Management Shell.

    
    </div>

</div>

</div>

<span> </span>

</div>

</div>

</div>

