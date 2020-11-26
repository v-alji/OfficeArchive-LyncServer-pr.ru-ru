---
title: 'Lync Server 2013: Просмотр сведений о сетевом интерфейсе'
description: 'Lync Server 2013: Просмотр сведений о сетевом интерфейсе.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Viewing network interface information
ms:assetid: e7dbb1ec-62b3-48be-a419-c493df5740e6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721916(v=OCS.15)
ms:contentKeyID: 49733850
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 12bf844116c048fb8c55e7aac1de46a7dffce4cd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443939"
---
# <a name="viewing-network-interface-information-in-lync-server-2013"></a>Просмотр сведений о сетевом интерфейсе в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2013-02-23_

Вы можете просматривать сведения о сетевом интерфейсе с помощью Windows PowerShell и командлета **Get-CsNetworkInterface** . Этот командлет можно выполнить из управляющей оболочки Lync Server 2013 или из удаленного сеанса Windows PowerShell. Подробнее об использовании удаленной оболочки Windows PowerShell для подключения к серверу Lync Server можно найти в статье "Краткое руководство по работе с Microsoft Lync Server 2010 с помощью удаленной оболочки PowerShell" на веб-сервере Lync Server Windows PowerShell [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .

<div>

## <a name="to-view-network-interface-information"></a>Просмотр сведений о сетевом интерфейсе

  - Чтобы просмотреть сведения о сетевом интерфейсе, введите следующую команду в командной консоли Lync Server Management Shell и нажмите клавишу ВВОД.
    
        Get-CsNetworkInterface
    
    Эта команда возвращает сведения о каждом сетевом интерфейсе, как показано ниже.
    
        Identity              : dc.vdomain.com/Primary/1
        ComputerFqdn          : dc.vdomain.com
        IPAddress             : 0.0.0.0
        IPv6Address           :
        Interface             : Primary
        InterfaceNumber       : 1
        ConfiguredFqdn        :
        ConfiguredIPAddress   :
        ConfiguredIPv6Address :
    
    Подробности можно найти в [статьях Get-CsNetworkInterface](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkInterface).

</div>

</div>

<span> </span>

</div>

</div>

</div>

