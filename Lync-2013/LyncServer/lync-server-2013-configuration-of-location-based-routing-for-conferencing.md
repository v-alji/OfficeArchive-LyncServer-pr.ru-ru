---
title: 'Lync Server 2013: конфигурация маршрутизации на основе расположения для конференций'
description: 'Lync Server 2013: Настройка маршрутизации Location-Based для конференц-связи.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuration of Location-Based Routing for conferencing
ms:assetid: d8c708cc-a1b1-48b1-808c-a64df15f7701
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362846(v=OCS.15)
ms:contentKeyID: 56335088
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6a87f9c799e565f64b0dd30ce025a4e7a3174625
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399949"
---
# <a name="configuration-of-location-based-routing-for-conferencing-in-lync-server-2013"></a>Конфигурация маршрутизации на основе расположения для конференций в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2013-09-11_

Приложение для конференц-связи Location-Based использует конфигурацию Lync Server 2013 Location-Based Routing. Основные конфигурации следующие:

  - Местоположение участников, присоединяющихся к собранию, определяется на основе их сетевого сайта. Чтобы обеспечить Location-Based маршрутизацию, необходимо определить сайт сети и связанные с ним подсети в Lync Server.

  - Для обеспечения Location-Based маршрутизации собраний участники Lync должны быть включены для Location-Based маршрутизации.

  - Чтобы обеспечить Location-Based маршрутизацию конечных точек PSTN, присоединяющихся к собраниям, необходимо настроить магистральную сеть SIP, используемую для подключения конечных точек PSTN, для Location-Based маршрутизации.

Дополнительные сведения о том, как развертывать и настраивать сервер Lync Server 2013 Location-Based Routing, можно найти в разделе Настройка [маршрутизации на основе местоположения](lync-server-2013-configuring-location-based-routing.md).

<div>

## <a name="enabling-the-location-based-routing-conferencing-application"></a>Включение приложения для конференц-связи Location-Based

Приложение для конференц-связи по Location-Based отключено по умолчанию. Перед включением этого приложения необходимо определить и назначить для него правильное значение приоритета. Чтобы определить этот приоритет, выполните в командной консоли Lync Server следующий командлет:

```powershell
Get-CsServerApplication -Identity Service:Registrar:<Pool FQDN>
```

В этом командлете \<Pool FQDN\> — это пул, в котором должно быть включено приложение для конференц-связи Location-Based.

Этот командлет вернет список приложений, размещенных на сервере Lync Server, и значение приоритета для каждого из них. Приложению для конференц-связи Location-Based необходимо назначить значение приоритета, большее, чем приложение "UdcAgent", и меньше, чем приложения "DefaultRouting", "ExumRouting" и "OutboundRouting". Мы рекомендуем назначить приложению для конференц-связи Location-Based значение приоритета, равное одной точке выше значения приоритета для приложения "UdcAgent".

Например, если для приложения "UdcAgent" задано значение приоритета "2", в приложении "DefaultRouting" задано значение приоритета "8", а для приложения "ExumRouting" задано значение приоритета "9", а в приложении "OutboundRouting" задано значение приоритета "10", необходимо назначить приложению для конференц-связи Location-Based значение приоритета "3". В этом случае приоритет приложений будет выстроен в следующем порядке: другие приложения (приоритеты: от 0 до 1), "UdcAgent" (приоритет: 2), приложение для конференций с маршрутизацией на основе расположения (приоритет: 3), другие приложения (приоритеты: от 4 до 8), "DefaultRouting" (приоритет: 9), "ExumRouting" (приоритет: 10) и "OutboundRouting" (приоритет: 11).

После того как вы найдете правильное значение приоритета для приложения для конференц-связи Location-Based, введите следующий командлет для каждого пула Front-End или сервера Standard Edition, для которого включены пользователи для маршрутизации Location-Based:

```powershell
New-CsServerApplication -Identity Service:Registrar:<Pool FQDN>/LBRouting -Priority <Application Priority> -Enabled $true -Critical $true -Uri http://www.microsoft.com/LCS/LBRouting
```

Например:

```powershell
New-CsServerApplication -Identity Service:Registrar:LS2013CU2LBRPool.contoso.com/LBRouting -Priority 3 -Enabled $true -Critical $true -Uri http://www.microsoft.com/LCS/LBRouting
```

После использования этого командлета перезапустите все серверы переднего плана в пуле или на серверах стандартных выпусков, где разрешено приложение для конференц-связи Location-Based.

<div>


> [!IMPORTANT]  
> Location-Based принудительные маршруты к конференциям или consultative передач не будут применены, пока не будут перезапусканы все серверы переднего плана в соответствующих пулах или стандартные серверы выпуска.



</div>

После того как приложение для конференц-связи Location-Based успешно включено и все применимые серверы Lync будут перезапущены, все конференции пользователей Lync, включенные для Location-Based маршрутизации, отслеживаются в целях предотвращения бесплатных вызовов по коммутируемой телефонной связи.

</div>

</div>

<span> </span>

</div>

</div>

</div>

