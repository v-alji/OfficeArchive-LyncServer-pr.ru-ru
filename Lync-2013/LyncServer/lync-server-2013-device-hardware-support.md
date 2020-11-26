---
title: 'Lync Server 2013: поддержка аппаратных устройств'
description: Поддержка аппаратных устройств для Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Device hardware support
ms:assetid: ba07ca91-32b4-49cf-801c-47a2d1d96e18
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412908(v=OCS.15)
ms:contentKeyID: 48185222
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: cd03936d35fbc3a639a3ba4596a4357e8e379719
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429455"
---
# <a name="device-hardware-support-in-lync-server-2013"></a>Поддержка аппаратных устройств в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2012-12-14_

Перед развертыванием IP-телефонов и аналоговых устройств необходимо установить определенные конфигурации оборудования.

IP-телефоны с Lync Phone Edition поддерживают обнаружение уровня связи Protocol-Media обнаружение конечных точек (LLDP-MED) и Power over Ethernet (PoE). Чтобы воспользоваться преимуществами LLDP-MED, коммутатор должен поддерживать IEEE 802.1 AB и ANSI/TIA-1057. Чтобы воспользоваться преимуществами PoE, коммутатор должен поддерживать PoE 802.3 AF или 802.3 по адресу.

Чтобы включить LLDP-MED, администратор должен включить LLDP с помощью окна переключения консоли и настройте сетевую политику LLDP-MED с правильным ИДЕНТИФИКАТОРом виртуальной ЛС для голосовой связи.

Кроме того, если в развертывании используются аналоговые устройства, необходимо настроить аналоговый шлюз для использования Lync Server, а шлюз должен быть одним из следующих:

  - Аналоговый телефонный адаптер (ATA)

  - Аналоговый шлюз PSTN

  - Бесперебойно работающее устройство филиалов, включающее аналоговый шлюз PSTN

  - Бесперебойно работающее устройство филиалов, которое включает шлюз PSTN, взаимодействующий с ATA.

Сведения о настройке аналогового шлюза можно найти в статье Планирование развертывания аналоговых устройств на сайте [https://go.microsoft.com/fwlink/p/?LinkId=268537](https://go.microsoft.com/fwlink/p/?linkid=268537) Lync Server 2010 в библиотеке TechNet. (Аналоговые устройства работают аналогичным образом в Lync Server 2013, как это делается в Lync Server 2010.)

<div>


> [!IMPORTANT]  
> Вы можете настроить переключатель для улучшенной 9-1-1 (E9-1-1), если она поддерживается коммутатором.



</div>

</div>

<span> </span>

</div>

</div>

</div>

