---
title: 'Lync Server 2013: Просмотр сведений о связи с сетевым регионом'
description: 'Lync Server 2013: Просмотр сведений о ссылке на сетевой регион.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Viewing network region link information
ms:assetid: 7b6b2ea2-83d8-4376-afb2-70e5d2cf6444
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688102(v=OCS.15)
ms:contentKeyID: 49733701
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0134ded9942ebda91050c1f7b0bbcfef018451a3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446207"
---
# <a name="viewing-network-region-link-information-in-lync-server-2013"></a>Просмотр сведений о связи по сетевому региону в Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Тема последнего изменения:** 2013-02-23_

Вы можете просматривать ссылки между двумя сетевыми областями в рамках управления допуском звонков (CAC). Регионы в сети связаны по ГЛОБАЛЬным сетевым подключениям. Вы можете просмотреть существующую ссылку между двумя областями сети с помощью панели управления Lync Server. Дополнительные сведения о создании и изменении ссылки на сетевой регион можно найти [в разделе Настройка ссылок на сетевые регионы в Lync Server 2013](lync-server-2013-configuring-network-region-links.md).

<div>

## <a name="to-view-a-network-region-link-in-lync-server-control-panel"></a>Просмотр ссылки на сетевой регион на панели управления Lync Server

1.  Войдите на любой компьютер, находящийся во внутреннем развертывании, с использованием учетной записи, входящей в группу RTCUniversalServerAdmins (или имеющей равнозначные права пользователя) либо назначенной роли CsAdministrator.

2.  Откройте окно браузера и введите URL-адрес администратора, чтобы открыть панель управления Lync Server. Дополнительные сведения о различных способах, которые можно использовать для запуска панели управления Lync Server, приведены в разделе [Открытие меню администрирования Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).

3.  На панели навигации слева выберите пункт **Настройка сети** , а затем щелкните **ссылку Region (регион**).

4.  На странице " **ссылка на регион** " щелкните ссылку "регион", которую вы хотите просмотреть.
    
    <div>
    

    > [!NOTE]  
    > Вы можете просматривать сведения только о одной ссылке на регион за один раз.

    
    </div>

5.  В меню **Правка** выберите пункт **Показать подробности**.

</div>

<div>

## <a name="viewing-network-region-link-information-by-using-windows-powershell-cmdlets"></a>Просмотр сведений о связи по сетевому региону с помощью командлетов Windows PowerShell

Вы можете просматривать ссылки на сетевую область с помощью Windows PowerShell и командлета **Get-CsNetworkRegionLink** . Этот командлет можно выполнить из управляющей оболочки Lync Server 2013 или из удаленного сеанса Windows PowerShell. Подробнее об использовании удаленной оболочки Windows PowerShell для подключения к серверу Lync Server можно найти в статье "Краткое руководство по работе с Microsoft Lync Server 2010 с помощью удаленной оболочки PowerShell" на веб-сервере Lync Server Windows PowerShell [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .

<div>

## <a name="to-view-network-region-link-information"></a>Просмотр сведений о связи по сетевому региону

  - Чтобы просмотреть сведения о ссылках на сетевой регион, введите следующую команду в командной консоли Lync Server Management Shell и нажмите клавишу ВВОД.
    
        Get-CsNetworkRegionLink
    
    Этой командой возвращается информация, аналогичная следующим сведениям:
    
        Identity            : NorthwestToCalifornia
        BWPolicyProfileID   :
        NetworkRegionLinkID : NorthwestToCalifornia
        NetworkRegionID1    : Pacific Northwest
        NetworkRegionID2    : California

</div>

Подробности можно найти в [статьях Get-CsNetworkRegionLink](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkRegionLink).

</div>

<div>

## <a name="see-also"></a>См. также


[Настройка связей сайтов сети в Lync Server 2013](lync-server-2013-configuring-network-site-links.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

